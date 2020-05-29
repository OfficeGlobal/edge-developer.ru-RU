---
description: Используйте механизм JavaScript, основанный на стандартах Chakra, для добавления возможностей сценария в приложение для Windows.
title: Размещение среды выполнения JavaScript | Документы Microsoft
ms.custom: ''
ms.date: 01/15/2020
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 30ec744e-57cc-4ef5-8fe1-d2c27b946548
caps.latest.revision: 14
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 9077284d96ff0d9ae22e152329efe9304081ae39
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571483"
---
# Размещение среды выполнения JavaScript
API среды выполнения JavaScript (JsRT) обеспечивают способ добавления в приложение возможностей для настольных систем, магазина Windows и серверных приложений, работающих в операционной системе Windows, с помощью основанного на стандартах обработчика JavaScript Chakra, который также используется Microsoft EDGE и Internet Explorer. Эти API-интерфейсы доступны в Windows 10 и в любой версии операционной системы Windows, в которой установлен Internet Explorer версии 11,0 на компьютере. Дополнительные сведения можно найти в статье [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md). Сведения о том, как использовать JsRT в приложениях Магазина Windows, можно найти в статье [JsRT и универсальной платформы Windows](#Windows).  
  
> [!NOTE]
>  В этом документе предполагается, что вы знакомы с языком JavaScript.  
  
## Понятия  
 Общие сведения о размещении обработчика JavaScript с помощью API JsRT зависит от двух ключевых концепций: среды выполнения и контексты выполнения.  
  
 *Среда выполнения* представляет полную среду выполнения JavaScript. Каждая созданная среда выполнения имеет собственную изолированную кучу, собранную сборщиком мусора, и, по умолчанию, собственный поток JIT-компилятора и поток сборщика мусора (GC). *Контекст выполнения* представляет среду JavaScript, у которой есть собственный глобальный объект JavaScript, отличный от всех других контекстов выполнения. Одна среда выполнения может содержать несколько контекстов выполнения, и в таких случаях все контексты выполнения совместно содержат JIT-компилятор и поток GC, связанный со средой выполнения.  
  
 Среды выполнения представляют собой один поток выполнения. Только одна среда выполнения может быть активна в конкретном потоке в каждый момент времени, и среда выполнения может быть активна только в одном потоке. Среда выполнения является потоком аренды, поэтому среда выполнения, которая не активна в данный момент в потоке (например, не выполняется ни один из кодов JavaScript или не отвечает на звонки из хоста), может использоваться в любом потоке, у которого еще нет активной среды выполнения.  
  
 Контексты выполнения связаны с определенной средой выполнения и исполняемым кодом в этой среде выполнения. В отличие от сред выполнения, несколько контекстов выполнения могут быть активными в потоке одновременно. Так что ведущее приложение может вызвать контекст выполнения, так как этот контекст выполнения может вызвать метод на хосте, и хост может сделать вызов в другой контекст выполнения.  
  
 ![Несколько контекстов выполнения](../chakra-hosting/media/js-chakra-hosting.png "JS_Chakra_Hosting")  
  
 На практике вы можете использовать один контекст выполнения, если только хосту не требуется выполнять код в раздельных средах. Точно так же, если хост не должен одновременно работать с несколькими фрагментами кода, достаточно одной среды выполнения.  
  
## Управление памятью  
 JavaScript — это язык сборки мусора, поэтому есть несколько моментов, которые необходимо учитывать при работе с API JsRT на другом языке.  
  
 Основной вопрос состоит в том, что сборщик мусора JavaScript может видеть только ссылки на значения в двух местах: из кучи среды выполнения и стека. Таким образом, ссылка на значение JavaScript, которое хранится в другом значении JavaScript или в локальной переменной в стеке, всегда будет отображаться сборщиком мусора. Однако ссылки, хранящиеся в других расположениях, таких как кучи, управляемые ведущим приложением или системой, не будут рассматриваться сборщиком мусора и могут привести к преждевременному сбору значений, которые по-прежнему используются узлом.  
  
> [!IMPORTANT]
>  Некоторые языковые компиляторы (такие как компилятор Visual Studio C++) будут оптимизировать локальные переменные, если это возможно. Будьте внимательны, чтобы убедиться в том, что локальные переменные, ссылающиеся на значения JavaScript, находятся в стеке, если предполагается, что они должны поддерживать активность этих значений.  
  
 Если ссылка на значение JavaScript будет храниться в расположении, невидимом для сборщика мусора, ведущее приложение должно вручную добавить и удалить ссылки с помощью API JsRT.  
  
## Обработка исключений  
 При возникновении исключения JavaScript во время выполнения сценария содержащаяся среда выполнения помещается в состояние исключения. В состоянии исключения код не может выполняться, и все вызовы API завершатся сбоем с кодом ошибки, `JsErrorInExceptionState` пока хост не извлекает и не очищает исключение с помощью `JsGetAndClearException` API. Если ведущее приложение возвращается из обратного вызова JavaScript, но не очищает среду выполнения из состояния исключения, то после того как управление передается обратно в обработчик JavaScript, будет выдано повторное создание исключения JavaScript. Это также позволяет обратным вызовам узла "выдавать" исключение JavaScript, задавая среду выполнения в состояние исключения и возвращая ее из обратного вызова хоста.  
  
 Ведущему приложению не разрешается разрешать своим внутренним исключениям распространяться по обратному вызову узла — любые методы обратного вызова должны перехватывать все исключения хоста, прежде чем возвращать управление среде выполнения.  
  
## Использование ресурсов среды выполнения  
 API JsRT предоставляют ряд способов мониторинга и изменения способа использования ресурсов средой выполнения. Как правило, они разбиваются на следующие категории:  
  
-   **Использование потоков**. По умолчанию каждый из сред выполнения создаст выделенный поток JIT-компилятора и выделенный поток GC, обслуживающий эту среду выполнения. Если среда выполнения создана с `JsRuntimeAttributeDisableBackgroundWork` флагом, то для каждого из них будет выполняться процесс JIT и GC, а не отдельные фоновые потоки. Ведущее приложение может также предоставлять вызов службы потока обратного вызова `JsCreateRuntime` , что позволяет основному приложению планировать работу JIT-и GC в любом направлении.  
  
-   **Использование памяти**. Существует несколько способов мониторинга и изменения использования памяти средой выполнения. Если среда выполнения будет выполняться в течение длительного времени, ведущее приложение может задать `JsRuntimeAttributeEnableIdleProcessing` флаг при создании среды выполнения, а затем вызвать, `JsIdle` когда узел находится в состоянии простоя. Это позволяет подсистеме откладывать некоторые операции очистки памяти и бухгалтерского учета, пока не будет определено время простоя.  
  
     Основное приложение может отслеживать сбор мусора с помощью вызова `JsSetRuntimeBeforeCollectCallback` . Кроме того, он может отслеживать выделение памяти, сделанных кучей, вызывая `JsSetRuntimeMemoryAllocationCallback` . Обратите внимание, что этот API не вызывает обратно для каждого выделения JavaScript, просто когда для кучи среды выполнения потребуется больше места для выделения. Обратный вызов выделения памяти может отклонить запрос, что приводит к инициированию сборки мусора и, если объем памяти недоступен, в среде выполнения возникает ошибка "недостаточно памяти".  
  
     Основное приложение также может вызвать `JsSetRuntimeMemoryLimit` для установки ограничения объема памяти, который может использовать среда выполнения. Если среда выполнения достигает предельного значения, она инициирует сборку мусора и, если память не доступна, среда выполнения вызывает ошибку нехватки памяти.  
  
-   **Прерывание и оценку сценария**. Основное приложение может вызвать `JsDisableRuntimeExecution` прекращение выполнения в среде выполнения. Этот звонок можно выполнить в любое время и из любого потока. Так как завершение сценария зависит от того, какие точки защиты вставляются в код, сценарий может не завершиться в течение определенного времени, но вскоре позже. По умолчанию контрольные точки увольнения размещаются в созданном коде и могут не охватывать все ситуации, например бесконечный цикл. Создание среды выполнения с помощью `JsRuntimeAttributeAllowScriptInterrupt` флага приводит к тому, что среда выполнения будет вставлять дополнительные проверки для бесконечного цикла, часто за счет небольшого объема производительности.  
  
     Если основное приложение не может запретить создание машинного кода с помощью JIT-компилятора, можно задать `JsRuntimeAttributeDisableNativeCodeGeneration` флаг. Кроме того, узел может запретить выполнение сценариев с динамическим запуском сценариев, указав `JsRuntimeAttributeDisableEval` флаг.  
  
## Отладка и профилирование  
 API JsRT поддерживает отладку и профилирование с помощью активной технологии сценариев.  
  
 Начиная с Windows 10, обработчик JavaScript Chakra поддерживает устаревший обработчик Internet Explorer (MSHTML) и новый обработчик Microsoft EDGE (EdgeHTML), и вы можете ориентироваться в JsRT (Дополнительные сведения можно найти в разделе [Настройка Microsoft EDGE и устаревшие ядра](../chakra-hosting/targeting-edge-vs-legacy-engines-in-jsrt-apis.md) ). Отладка сценария в Visual Studio работает не так, как в старом обработчике и Microsoft Edge. С помощью устаревшего модуля хост должен предоставить указатель [интерфейса IDebugApplication](/scripting/winscript/reference/idebugapplication-interface) , который можно получить из экземпляра [интерфейса IProcessDebugManager](/scripting/winscript/reference/iprocessdebugmanager-interface) . С помощью подсистемы Microsoft Edge `IDebugApplication` является устаревшим, а подсистема Chakra поддерживает возможности отладки в собственном и пользовательском интерфейсе с помощью отладчика Visual Studio, не требуя `IDebugApplication` от него реализации.  
  
 Чтобы скрипты в контекстах выполнения были отлаженными, обработчику Chakra нужно переключиться на использование менее эффективных методов выполнения кода. Таким образом, отлаживаемый код обычно работает медленнее, чем неотлаживаемый код. В результате с помощью устаревшего модуля хост может либо запустить отладку в контексте выполнения с начала, добавив `IDebugApplication` указатель вверх `JsCreateContext` , либо подождать, пока требуется отладка, а затем вызвать `JsStartDebugging` . С помощью подсистемы Microsoft Edge `JsCreateContext` больше не принимает `IDebugApplication` параметр, и в результате сценарий будет отлажен только после `JsStartDebugging` вызова. При отладке с использованием Visual Studio параметр отладчика "сценарии" должен быть включен.  
  
 Код JavaScript в контексте выполнения может быть профилировщиком одним из двух способов. Профилировщик Visual Studio (VSPerf. exe) командной строки можно использовать в Windows 8,1 и более поздних версиях с помощью переключателя/JS для создания отчета, предназначенного для выполнения кода JavaScript в приложении. Кроме того, хост может напрямую вызывать метод `JsStartProfiling` и `JsStopProfiling` обеспечивать обратный вызов для самостоятельного профилирования. Ведущее приложение может также проверять состояние кучи, в которой собрано мусора, путем вызова `JsEnumerateHeap` . Профилирование в JsRT работает таким же образом, как и для старой версии, и для ядра Microsoft Edge. Однако JsRT API профилирования (, `JsStartProfiling` `JsStopProfiling` , `JsEnumerateHeap` и) недоступны `JsIsEnumeratingHeap` для универсальных приложений для Windows.  
  
<a name="Windows"></a>   
## JsRT и универсальная платформа Windows  

Вы можете использовать API JsRT для добавления возможностей сценария в универсальное приложение для Windows. Универсальное приложение для Windows, использующее API JsRT, должно нацелиться на API Microsoft Edge JSRT, которые, в свою очередь, предназначены для обработчика Chakra Edge. Дополнительные сведения можно найти в разделе [назначение Microsoft EDGE и устаревших ядер](../chakra-hosting/targeting-edge-vs-legacy-engines-in-jsrt-apis.md). Полный API JsRT доступен для универсальных приложений для Windows, за исключением случаев, когда поддерживается профилирование и перечисление кучи ( `JsStartProfiling` , `JsStopProfiling` `JsEnumerateHeap` и `JsIsEnumeratingHeap` не поддерживается).  
  
JsRT также позволяет сценариям осуществлять собственный доступ к любым [API универсальной платформы Windows (UWP)](https://msdn.microsoft.com/library/windows/apps/br211377.aspx) после предоставления пространства имен API через API Microsoft Edge JsRT `JsProjectWinRTNamespace` . Несмотря на то, что для универсальных приложений для Windows не требуется настройка, помимо проецирования необходимых пространств имен, в классическом приложении Windows (Win32) необходимо включить механизм перебора, инициализированный COM, чтобы `JsSetProjectionEnqueueCallback` включить события и асинхронные API. В следующем примере Win32 используются асинхронные API UWP, чтобы создать HTTP-клиент для получения содержимого из универсального кода ресурса (URI).  
  
```cpp  
typedef struct _jsCall {  
    JsProjectionCallback jsCallback;  
    JsProjectionCallbackContext jsContext;  
    HANDLE event;  
} jsCall;  
  
// Set up delegated pumping mechanism; not necessary in UWP applications.  
jsCall outstandingCall = {};  
CoInitializeEx(nullptr, COINIT_MULTITHREADED);  
JsSetProjectionEnqueueCallback([](JsProjectionCallback jsCallback,   
JsProjectionCallbackContext jsContext, void *callbackState) {  
    jsCall* call = (jsCall*)callbackState;  
    call->jsCallback = jsCallback;  
    call->jsContext = jsContext;  
    SetEvent(call->event);  
    },  
&outstandingCall);  
HANDLE event = CreateEventEx(NULL, NULL, CREATE_EVENT_MANUAL_RESET, EVENT_ALL_ACCESS);  
outstandingCall.event = event;  
  
// Project necessary namespaces.  
JsProjectWinRTNamespace(L"Windows.Foundation");  
JsProjectWinRTNamespace(L"Windows.Web");  
  
// Get content from an Uri.  
JsRunScript(L"var uri = new Windows.Foundation.Uri(\"http://somedatasource.com\"); " \  
    L"var httpClient = new Windows.Web.Http.HttpClient();" \  
    L"httpClient.getStringAsync(uri).done(function (content) { " \  
    L"    // do something with the string content " \    
    L"}, onError); " \  
    L"function onError(reason) { " \  
    L"    // error handling " \        
    L"}",   
    currentSourceContext, L"", &result);  
  
// Wait for async call to come in and then execute; not necessary in UWP applications.  
WaitForSingleObjectEx(outstandingCall.event, 10000, FALSE) == WAIT_OBJECT_0;  
outstandingCall.jsCallback(outstandingCall.jsContext);  
  
```  
  
## См. также  
 [Пример приложения среды выполнения JavaScript](https://go.microsoft.com/fwlink/p/?LinkID=306674&clcid=0x409)   
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)   
 [Размещение среды выполнения JavaScript](../javascript-runtime-hosting.md)  
 