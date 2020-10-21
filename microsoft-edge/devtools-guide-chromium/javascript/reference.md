---
description: Ознакомьтесь с новыми рабочими процессами отладки в этой полной справке функций отладки Microsoft Edge DevTools.
title: Справочник по отладке JavaScript
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: c1d6b9d301ff2bc696900b48d80a3d5352f8fd58
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "11124805"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->

# Справочник по отладке JavaScript  

Вы узнаете о новых рабочих процессах отладки со следующими полным справочником по функциям отладки Microsoft Edge DevTools.  

Подробнее об отладке можно найти [в статье Начало работы с отладкой JavaScript в Microsoft Edge DevTools][DevToolsJavascriptGetStarted] .  

## Приостановка кода с точки останова  

Установите точку останова, чтобы можно было приостановить выполнение кода в середине среды выполнения.  

Сведения о том, как задавать точки останова, можно найти в разделе [приостановка кода с точки останова][DevToolsJavascriptBreakpoints] .  

## Пошаговое руководство по коду  

Когда код приостанавливается, проведите по одной строке за раз, изменяя поток управления и значения свойств по своему пути.  

### Шаг с заходом в строке кода  

При приостановке в строке кода, содержащей функцию, которая не связана с проблемой, которую вы используете для отладки, нажмите кнопку **шаг за** шагом \ ( ![ Шаг с заходом ][ImageStepOverIcon] в конце), чтобы запустить функцию без пошагового выполнения.  

:::image type="complex" source="../media/javascript-source-page-debugger-step-over-next-function-call.msft.png" alt-text="Нажмите кнопку &quot;шаг за шагом&quot;" lightbox="../media/javascript-source-page-debugger-step-over-next-function-call.msft.png":::
   Нажмите кнопку " **шаг за шагом** "  
:::image-end:::  

Например, предположим, что выполняется отладка следующего фрагмента кода.  

```javascript
function updateHeader() {
    var day = new Date().getDay();
    var name = getName(); // A
    updateName(name); // D
}
function getName() {
    var name = app.first + ' ' + app.last; // B
    return name; // C
}
```  

Вы приостанавливаете `A` .  Нажимая клавишу " **шаг за шагом**", DevTools запускает весь код в функции, для которой выполняется пошаговое выполнение, `B` а именно `C` .  Затем DevTools приостанавливает `D` .  

### Шаг с заходом в строку кода  

При приостановке в строке кода, содержащей вызов функции, связанный с проблемой, в которой выполняется отладка, нажмите кнопку **Шаг с заходом** \ (шаг с заходом в начало ![ ), ][ImageStepIntoIcon] чтобы более подробно изучить эту функцию.  

:::image type="complex" source="../media/javascript-source-page-debugger-step-into-next-function-call.msft.png" alt-text="Нажмите кнопку &quot;шаг за шагом&quot;" lightbox="../media/javascript-source-page-debugger-step-into-next-function-call.msft.png":::
   Нажмите " **Шаг с заходом** "  
:::image-end:::  

Например, предположим, что выполняется отладка следующего фрагмента кода.  

```javascript
function updateHeader() {
    var day = new Date().getDay();
    var name = getName(); // A
    updateName(name);
}
function getName() {
    var name = app.first + ' ' + app.last; // B
    return name;
}
```  

Вы приостанавливаете `A` .  Нажимая кнопку " **Шаг с заходом**", DevTools запускает эту строку кода, а затем приостанавливает выполнение `B` .  

### Пошаговое руководство из строки кода  

При приостановке внутри функции, которая не связана с проблемой, которую вы выполняете Отладка, нажмите кнопку **шаг** с выходом \ ( ![ Шаг с выходом ][ImageStepOutIcon] ), чтобы выполнить оставшуюся часть кода функции.  

:::image type="complex" source="../media/javascript-source-page-debugger-step-out-of-current-function.msft.png" alt-text="Нажмите кнопку &quot;шаг за шагом&quot;" lightbox="../media/javascript-source-page-debugger-step-out-of-current-function.msft.png":::
   Нажмите кнопку " **Шаг с выходом** "  
:::image-end:::  

Например, предположим, что выполняется отладка следующего фрагмента кода.  

```javascript
function updateHeader() {
    var day = new Date().getDay();
    var name = getName();
    updateName(name); // C
}
function getName() {
    var name = app.first + ' ' + app.last; // A
    return name; // B
}
```  

Вы приостанавливаете `A` .  Нажимая кнопку " **Шаг с выходом**", DevTools запускает оставшуюся часть кода в `getName()` `B` этом примере, а затем приостанавливает выполнение `C` .  

### Выполнение всего кода до определенной строки  

При отладке длительных функций может возникнуть большой объем кода, не относящегося к той проблеме, которую вы размещаете в отладке.  

Вы можете пошагово пройти все строки, но это утомительно.  Вы можете указать точку останова для строки кода в строке, в которой вы заинтересованы, и нажать кнопку **возобновить выполнение сценария** \ ( ![ возобновить выполнение скрипта ][ImageResumeScriptExecutionIcon] \), но это происходит быстрее.  

Щелкните правой кнопкой мыши строку кода, в которой вы заинтересованы, и выберите пункт **Перейти к**этому разделу.  DevTools запускает весь код до этого момента, а затем приостанавливает выполнение на этой линии.  

:::image type="complex" source="../media/javascript-source-page-continue-to-here.msft.png" alt-text="Нажмите кнопку &quot;шаг за шагом&quot;" lightbox="../media/javascript-source-page-continue-to-here.msft.png":::
   Нажмите кнопку **"продолжить"**  
:::image-end:::  

### Перезапустить функцию TOP в стеке вызовов  

Наведя указатель на строку кода, щелкните правой кнопкой мыши в любом месте области **стека звонков** и выберите команду **перезапустить кадр** , чтобы приостановить выполнение первой строки функции Top в стеке вызовов.  Функция Top — это последняя выполненная функция.  

В приведенном ниже фрагменте кода показан пример с пошаговыми операциями.  

```javascript
function factorial(n) {
    var product = 0; // B
    for (var i = 1; i <= n; i++) {
      product += i;
    }
    return product; // A
}
```  

Вы приостанавливаете `A` .  После нажатия кнопки **перезапустить**вы должны быть приостановлены `B` , не задавая точку останова или не выбирая команду **возобновить выполнение сценария**.  

:::image type="complex" source="../media/javascript-source-page-debugger-restart-frame.msft.png" alt-text="Нажмите кнопку &quot;шаг за шагом&quot;" lightbox="../media/javascript-source-page-debugger-restart-frame.msft.png":::
   Выберите команду " **перезапустить рамку** "  
:::image-end:::  

### Среда выполнения сценария возобновления  

Чтобы продолжить выполнение после паузы сценария, нажмите кнопку **возобновить исполнение сценария** \ ( ![ возобновить выполнение скрипта ][ImageResumeScriptExecutionIcon] \).  DevTools запускает сценарий до следующей точки останова (при наличии).  

:::image type="complex" source="../media/javascript-sources-get-started-js-resume-script-runtime.msft.png" alt-text="Нажмите кнопку &quot;шаг за шагом&quot;" lightbox="../media/javascript-sources-get-started-js-resume-script-runtime.msft.png":::
   Выбор **выполнения скрипта возобновления**  
:::image-end:::  

#### Выполнение принудительного выполнения сценария  

Чтобы пропустить все точки останова и принудительно возобновить выполнение сценария, выберите и удерживайте нажатой кнопку "возобновить выполнение **скрипта** \", ![ ][ImageResumeScriptExecutionIcon] а затем выберите команду **принудительное** выполнение сценария \ ( ![ принудительное выполнение сценария \ ][ImageForceScriptExecutionIcon] ).  

:::image type="complex" source="../media/javascript-sources-get-started-js-force-script-runtime.msft.png" alt-text="Нажмите кнопку &quot;шаг за шагом&quot;" lightbox="../media/javascript-sources-get-started-js-force-script-runtime.msft.png":::
   Выберите **принудительное выполнение сценария**  
:::image-end:::  

### Изменить контекст потока  

При работе с веб-сотрудниками или сотрудниками служб выберите контекст, указанный в области **потоки** , чтобы переключиться на этот контекст.  Синий значок стрелки соответствует контексту, выбранному в данный момент.  

:::image type="complex" source="../media/javascript-sources-main-min-js-threads.msft.png" alt-text="Нажмите кнопку &quot;шаг за шагом&quot;" lightbox="../media/javascript-sources-main-min-js-threads.msft.png":::
   Область « **потоки** »  
:::image-end:::  

Например, предположим, что вы придерживаетесь точки останова как в основном, так и на рабочем скрипте службы.  Вы хотите просмотреть локальные и глобальные свойства для контекста рабочего процесса службы, но на панели **источники** отображается контекст основного сценария.  Выбирая элемент "сотрудник службы" на панели " **потоки** ", вы можете переключиться на этот контекст.  

## Просмотр и изменение локальных, закрытых и глобальных свойств  

При приостановке в строке кода используйте область **область** для просмотра и изменения значений свойств и переменных в локальных, закрытых и глобальных областях.  

*   Дважды щелкните значение свойства, чтобы изменить его.  
*   Неперечислимые свойства затенены.  

:::image type="complex" source="../media/javascript-sources-get-started-js-scope.msft.png" alt-text="Нажмите кнопку &quot;шаг за шагом&quot;" lightbox="../media/javascript-sources-get-started-js-scope.msft.png":::
   Область " **область** "  
:::image-end:::  

## Просмотр текущего стека вызовов  

При приостановке на строке кода используйте область **Стек вызовов** для просмотра стека вызовов, в котором вы набрались этим моментом.  

<!--If you are working with async code, check the **Async** checkbox to enable async call stacks.  -->  

Выберите запись, чтобы перейти к строке кода, в которой была вызвана эта функция.  Синий значок стрелки показывает, какая функция DevTools выделяется в данный момент.  

:::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty.msft.png" alt-text="Нажмите кнопку &quot;шаг за шагом&quot;" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty.msft.png":::
   Область « **Стек вызовов** »  
:::image-end:::  

> [!NOTE]
> Если в строке кода не присвоена значение, область **стека вызовов** пуста.  

### Копирование трассировки стека  

<!--
This should be moved to an "Export debug data" H2 section when there is enough content for that, but there is not right now, so it is here.
-->

Щелкните правой кнопкой мыши в любом месте области **стека звонков** и выберите команду **Копировать трассировку стека** , чтобы скопировать текущий стек вызовов в буфер обмена.  

:::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-copy-stack-trace.msft.png" alt-text="Нажмите кнопку &quot;шаг за шагом&quot;" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-copy-stack-trace.msft.png":::
   Выберите команду **Копировать трассировку стека** .  
:::image-end:::  

В приведенном ниже фрагменте кода показан пример выходных данных.  

```javascript
getNumber1 (get-started.js:35)
inputsAreEmpty (get-started.js:22)
onClick (get-started.js:15)
```  

## Игнорировать сценарий или шаблон сценариев  

Помечайте сценарий как код библиотеки, если вы хотите пропустить этот сценарий во время отладки.  При пометке в виде кода библиотеки сценарий скрывается в области **стека вызовов** , и вы никогда не просматриваете функции сценария при пошаговом выполнении кода.  

В приведенном ниже фрагменте кода показан пример с пошаговыми операциями.  

```javascript
function animate() {
    prepare();
    lib.doFancyStuff(); // A
    render();
}
```  

`A` — это библиотека стороннего поставщика, которой вы доверяете.  Если вы уверены, что проблема, выполняемая при отладке, не связана с библиотекой стороннего поставщика, имеет смысл помечать сценарий как **код библиотеки**.  

### Пометка сценария как кода библиотеки в области "редактор"  

Выполните указанные ниже действия, чтобы помечать сценарий как **код библиотеки** на панели **редактора** .  

1.  Откройте файл.  
1.  Щелкните правой кнопкой мыши в любом месте.  
1.  Нажмите кнопку **помечать как код библиотеки**.  
    
    :::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-editor-mark-as-library-code.msft.png" alt-text="Нажмите кнопку &quot;шаг за шагом&quot;" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-editor-mark-as-library-code.msft.png":::
       Пометка сценария как **кода библиотеки** в области " **Редактор** "  
    :::image-end:::  
    
### Пометка сценария как кода библиотеки на панели «стек вызовов»  

Compelte действия folliwng, чтобы помечать сценарий как **код библиотеки** из области " **Стек вызовов** ".  

1.  Щелкните правой кнопкой мыши функцию в сценарии.  
1.  Нажмите кнопку **помечать как код библиотеки**.  
    
    :::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-call-stack-mark-as-library-code.msft.png" alt-text="Нажмите кнопку &quot;шаг за шагом&quot;" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-call-stack-mark-as-library-code.msft.png":::
       Пометка сценария как **кода библиотеки** на панели « **Стек вызовов** »  
    :::image-end:::  
    
### Пометка сценария как кода библиотеки из параметров  

Выполните указанные ниже действия, чтобы помечать один сценарий или шаблон сценариев из **параметров**.  

1.  Откройте [Параметры][DevToolsCustomize].  
1.  Перейдите на вкладку **код библиотеки** .  
1.  Нажмите кнопку **Добавить шаблон**.  
1.  Введите имя сценария или шаблон регулярного выражения для имен сценариев, чтобы помечать его как **код библиотеки**.  
1.  Нажмите кнопку **Добавить**.  
    
    :::image type="complex" source="../media/javascript-framework-library-code.msft.png" alt-text="Нажмите кнопку &quot;шаг за шагом&quot;" lightbox="../media/javascript-framework-library-code.msft.png":::
       Пометка сценария как **кода библиотеки** из **параметров**  
    :::image-end:::  
    
## Выполнение фрагментов кода отладки на любой странице  

Если вы обнаружите, что вы используете один и тот же код отладки в консоли, рассматривайте фрагменты кода.  Фрагменты — это сценарии среды выполнения, созданные, сохраняемые и выполняемые в DevTools.  

Дополнительные сведения можно найти в разделе [выполнение фрагментов кода на любой странице][DevToolsJavascriptSnippets] .  

## Просмотр значений настраиваемых выражений JavaScript  

Используйте область **контрольных** значений для просмотра значений настраиваемых выражений.  Вы можете просмотреть любое допустимое выражение JavaScript.  

:::image type="complex" source="../media/javascript-sources-get-started-js-watch.msft.png" alt-text="Нажмите кнопку &quot;шаг за шагом&quot;" lightbox="../media/javascript-sources-get-started-js-watch.msft.png":::
   Область **контрольных значений**  
:::image-end:::  

*   Нажмите кнопку **Добавить выражение** \ ( ![ Добавить выражение ][ImageAddExpressionIcon] \), чтобы создать новое выражение контрольного значения.  
*   Нажмите кнопку " **Обновить** \ ![ " (обновить ][ImageRefreshIcon] ), чтобы обновить значения всех существующих выражений.  Значения автоматически обновляются при пошаговом выполнении кода.  
*   Наведите указатель мыши на выражение и нажмите кнопку **удалить выражение** \ ( ![ удалить выражение ][ImageDeleteExpressionIcon] \), чтобы удалить его.  

## Создание читаемого файла minified  

**Format** ![ ][ImageFormatIcon] Чтобы сделать файл minified удобным для чтения, нажмите кнопку Формат \ (формат \).  

:::image type="complex" source="../media/javascript-sources-html-non-minified.msft.png" alt-text="Нажмите кнопку &quot;шаг за шагом&quot;" lightbox="../media/javascript-sources-html-non-minified.msft.png":::
   Кнопка " **Формат** "  
:::image-end:::  

## Изменение сценария  

При исправлении ошибки часто требуется протестировать некоторые изменения в коде JavaScript.  Вам не нужно вносить изменения в внешний редактор или интегрированную среду разработки и повторно загрузить страницу.  Вы можете редактировать сценарий в DevTools.  

Чтобы изменить сценарий, выполните указанные ниже действия.  

1.  Откройте файл в области " **Редактор** " на панели " **источники** ".  
1.  Внесите изменения в область " **Редактор** ".  
1.  Выберите `Ctrl` + `S` \ (Windows, Linux \) или `Command` + `S` \ (macOS \), чтобы сохранить его.  DevTools заменяет весь JS – файл в механизме JavaScript Microsoft Edge.  
    
    :::image type="complex" source="../media/javascript-sources-html-minified.msft.png" alt-text="Нажмите кнопку &quot;шаг за шагом&quot;" lightbox="../media/javascript-sources-html-minified.msft.png":::
       Область " **Редактор** "  
    :::image-end:::  
     
## Отключение JavaScript  

Перейдите к разделу [Отключение JavaScript с помощью Microsoft Edge DevTools][DevToolsJavascriptDisable].  

## Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageStepOverIcon]: ../media/step-over-icon.msft.png  
[ImageStepIntoIcon]: ../media/step-into-icon.msft.png  
[ImageStepOutIcon]: ../media/step-out-icon.msft.png  
[ImageResumeScriptExecutionIcon]: ../media/resume-script-run-icon.msft.png  
[ImageForceScriptExecutionIcon]: ../media/force-script-run-icon.msft.png  
[ImageAddExpressionIcon]: ../media/add-expression-icon.msft.png  
[ImageRefreshIcon]: ../media/refresh-icon.msft.png  
[ImageDeleteExpressionIcon]: ../media/delete-expression-icon.msft.png  
[ImageFormatIcon]: ../media/format-icon.msft.png  

<!-- links -->  

[DevToolsJavascriptBreakpoints]: ./breakpoints.md "Приостановка кода с точки останова в Microsoft Edge DevTools | Документы Microsoft"  
[DevToolsJavascriptDisable]: ./disable.md "Отключение JavaScript в Microsoft Edge DevTools | Документы Microsoft"  
[DevToolsJavascriptGetStarted]: ./index.md "Начало работы с отладкой JavaScript в Microsoft Edge DevTools | Документы Microsoft"  
[DevToolsJavascriptSnippets]: ./snippets.md "Выполнение фрагментов кода JavaScript на любой странице с Microsoft Edge DevTools | Документы Microsoft"  
[DevToolsCustomize]: ../customize/index.md "Настройка Microsoft Edge DevTools | Документы Microsoft"  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/javascript/reference) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
