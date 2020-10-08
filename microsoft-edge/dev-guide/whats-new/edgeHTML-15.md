---
description: В этом руководстве вы найдете общие сведения о функциях и стандартах разработчика, включенных в EdgeHTML 15.
title: Новые функции и API-интерфейсы в EdgeHTML 15
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/02/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: EDGE, веб-разработка, HTML, CSS, JavaScript, разработчик
ms.custom: seodec18
ms.openlocfilehash: 4fd0bbc06d27bace424ea99cfe9941aabc737fee
ms.sourcegitcommit: 204a284e21bf2da5cdc862c5e8b5839245abbbbc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/02/2020
ms.locfileid: "11094363"
---
# Новые возможности EdgeHTML 15  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

Ниже описаны изменения, которые поставляются с текущим выпуском платформы Microsoft EDGE, в соответствии с [обновлением Windows 10 Creators](https://blogs.windows.com/buildingapps/2017/04/05/windows-10-creators-update-creators-update-sdk-released/#MMhK2OdcrR12Vi6u.97) \ (04/2017, сборка 15063 \).  Общие сведения об изменениях, внесенных в общий браузер Microsoft EDGE, приведены в [статье новые возможности Microsoft EDGE в обновлении Windows 10 Creators](https://blogs.windows.com/msedgedev/2017/04/11).  

Изменения, внесенные в последующих сборках Insider Preview для Windows, приведены [в разделе новые возможности EdgeHTML](../whats-new.md).  

Ниже приведен список постоянных  [https://aka.ms/devguide_edgehtml_15](./edgehtml-15.md) изменений.  

## Новые возможности  

### Пользовательские свойства CSS  

Microsoft EDGE теперь поддерживает [пользовательские свойства CSS](https://drafts.csswg.org/css-variables), переменные CSS. k..  Переменные CSS позволяют создавать пользовательские свойства CSS, которые можно повторно использовать во всех таблицах стилей для уменьшения количества повторяющихся данных, таких как повторяющиеся цвета.  Использование переменных CSS очень просто:  

```css
/* define a custom property by using two dashes and assign it a value */
body {   
   --default-color: #3390b1
}

/* reference it in your stylesheet with the "var()" function */
h1 {
   color: var(--default-color);
}
```  

### Наблюдатель пересечения  

EdgeHTML 15 представляет спецификацию [API наблюдателей пересечения](https://w3c.github.io/IntersectionObserver) .  API наблюдателя для пересечения позволяет асинхронно запрашивать расположение и видимость элементов DOM относительно других элементов или глобального окна просмотра.  Этот API исключает необходимость специального дорогостоящего кода, создавая метод для эффективного уведомления элементов в представлении.  

### JavaScript  

Оптимизация производительности занимает центральное состояние с помощью EdgeHTML 15 версии обработчика JavaScript для Chakra.  С помощью обновления Windows 10 Creators Chakra экономит память, изменяя функции и оптимизируя аргументы кучи и повышая производительность для minified кода.  

Кроме того, в EdgeHTML 15 представлены следующие предварительные обзоры функций:  

#### Экспериментальные функции JavaScript  

Включено с `about:flags`  

*   [Сборка](https://developer.microsoft.com/microsoft-edge/platform/status/webassemblymvp/?q=WebAssembly) ([демонстрация](https://webassembly.org/demo))  
*   [Общая память и атомарные](https://developer.microsoft.com/microsoft-edge/platform/status/sharedmemoryandatomics/?q=Atomics)  

Более подробную информацию [можно найти в разделе Улучшенная производительность JavaScript, сборка и общая память в Microsoft Edge](https://blogs.windows.com/msedgedev/2017/04/20) .  

### API запроса оплаты  

[Интерфейс обработки запросов на оплату](https://w3.org/TR/payment-request) теперь поддерживается, что позволяет упростить оформление и оплату через Интернет на компьютерах и телефонах с Windows 10.  Этот API позволяет Microsoft Edge выступать в качестве посредника между продавцами, клиентами и методами оплаты \ (например, кредитные карты \), которые хранятся у потребителей в облаке.  Дополнительные сведения об API запроса на оплату можно найти в статье [упрощенные веб-платежи: знакомство с API запроса на оплату](https://blogs.windows.com/msedgedev/2016/12/15) и руководство по API для разработчиков [запросов на оплату](/microsoft-edge/dev-guide/device/payment-request-api) .  

### TCP Fast Open (TFO)  
TCP Fast Open — это функция, которая сокращает количество циклов обработки, необходимых для открытия TCP-соединения, повышая производительность сети в браузере.  Дополнительные сведения можно найти [в разделе Создание более быстрой и безопасной веб-страницы с помощью TCP Fast Open](https://blogs.windows.com/msedgedev/2016/06/15).  Из-за различий в взаимодействии с различными сетевыми топологиями эти функции не включены по умолчанию в Microsoft Edge.  Чтобы включить его, введите `about:flags` адресную строку и установите флажок **включить TCP Fast Open** в разделе **сеть** .  

### WebRTC и поддержка видеокодека, поддерживающего взаимодействие с кодеками реального времени  

EdgeHTML 15 поддерживает подмножество API WebRTC 1,0 для обеспечения совместимости с приложениями, созданными в более ранних версиях консорциума W3C WebRTC-PC API Circa 2015.  Подробности вы видите в [справочнике по API WebRTC](/previous-versions//mt806139(v=vs.85)) .  

Для использования самых современных функций голосовой и видеосвязи в одноранговых режимах рекомендуется использовать [объект API для обмена данными в реальном времени](https://ortc.org).  API ORTC лучше всего подходит для случаев, когда вы хотите настроить групповую видеосвязь и видеозвонки, а также прямо управлять индивидуальными объектами транспорта, отправителей и приемников.  

Microsoft EDGE поддерживает как H. 264, AVC, так и VP8 видео с помощью ORTC и WebRTC 1,0, а также предоставляет следующие функции для поддержки обоих типов кодеков: [ABS-время отправки](https://webrtc.org/experiments/rtp-hdrext/abs-send-time), [GOOG-Remb](https://tools.ietf.org/html/draft-alvestrand-rmcat-remb-03), [Индикатор потери изображения и общий Nack отзыв](https://tools.ietf.org/html/rfc4585), [Повторная передача RTP](https://tools.ietf.org/html/rfc4588).  

Дополнительные сведения можно найти [в статье Знакомство с WebRTC 1,0 и взаимодействующими связями в режиме реального времени в Microsoft Edge](https://blogs.windows.com/msedgedev/2017/01/31).  

### WebVR  

Microsoft EDGE теперь поддерживает [WebVR](https://immersive-web.github.io/webxr)— экспериментальный API-интерфейс, соединяющий дисплеи Windows Mixed Reality с установленными заголовками и Microsoft Edge.  Это подключение включает в себя доступ к содержимому VR на веб-сайте, что означает, что современные функциональные возможности больше не ограничиваются классским приложениям.  

Виртуальная реальность в Microsoft EDGE на платформе WebGL — API JavaScript для отрисовки трехмерной и двухмерной графики.  WebGL приложения и приложения, созданные с помощью библиотек WebGL, таких как BabylonJS, поддерживаются.  После подключения WebVR отправляет визуальные элементы, соответствующие положению и сведениям о датчиках вокруг гарнитуры.  API WebVR также поддерживает пространственные контроллеры благодаря расширению [API игровой планшет](../dom/gamepad-api.md).  Этот API включен по умолчанию, поэтому не нужно переключать флаг.  

Ознакомьтесь со справочными материалами по API [WEBVR API](/previous-versions//mt806281(v=vs.85)) и [игровой планшета](https://developer.mozilla.org/docs/Web/API/Gamepad_API) для получения подробных сведений.  

 > [!NOTE] 
 > Поскольку спецификация WebVR по-прежнему находится на стадии разработки, реализация Microsoft Edge может измениться позже.  

## Обновленные функции  

### Политика безопасности содержимого (уровень 2)  

Сайты, уже использующие CSP 1, должны продолжать работать со службой поддержки Microsoft Edge для CSP 2, однако лучше переключать любые `frame-src` директивы, которые загружают сценарии рабочих процессов в новую `child-src` директиву для проверки правописания для сайта в будущем.  \ (В CSP 3 `frame-src` больше не будет применяться к сотрудникам). \) CSP 2 также добавляет следующее:  

:::row:::
   :::column span="1":::
      Новые директивы  
   :::column-end:::
   :::column span="2":::
      `base-uri`, `child-src` , `form-action` `frame-ancestors` и `plugin-types` .  Дополнительные сведения о том, как узнать, [поддерживаются директивы поставщика служб Microsoft Edge](../security/content-security-policy.md) .  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Поддержка сотрудников  
   :::column-end:::
   :::column span="2":::
      Фоновые сценарии рабочего процесса управляются собственной политикой, отделенной от политики загрузки документа.  Как и в случае с документами размещения, вы можете настроить CSP для исполнителя в заголовке ответа.  Кроме того, Новая возможность в CSP 2 — это то, что  `allow-scripts` `allow-same-origin` Флаги `sandbox` директивы теперь влияют на создание рабочего потока.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Встроенные сценарии и стили  
   :::column-end:::
   :::column span="2":::
      CSP 2 допускает выполнение встроенных сценариев и блоков стилей, предоставляя nonces и хэши в качестве механизма разрешающего списка.  Nonces — это случайные значения Base-64, созданные при каждой загрузке страницы, которая отображается как в политике CSP, так и в тегах сценария на странице.  Когда страница динамически генерируется при загрузке, сервер создает значение nonce, вставляет его в NonceToken на странице, а также объявляет его в HTTP-заголовке политики безопасности содержимого.  Хэши — это статические значения (с использованием алгоритмов SHA256, SHA384 или SHA512) из содержимого `<script>` `<style>` элемента или элемент, которые затем указаны \ (использование `script-src` или `style-src` директивы \) в политике CSP.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Отчет о нарушениях CSP  
   :::column-end:::
   :::column span="2":::
      Новое событие `SecurityPolicyViolationEvent` теперь срабатывает при нарушениях CSP.  Более ранний механизм составления отчетов CSP `report-uri` продолжает поддерживаться.  В общие отчеты о нарушениях добавлены несколько новых полей, в том числе `effectiveDirective` \ (политика, которая была нарушена), `statusCode` \ (код HTTP-ответа \), \ (URL-адрес, на который указывает `sourceFile` ресурс, вызывающий ошибку), `lineNumber` и `columnNumber` .  
   :::column-end:::
:::row-end:::  

### Проверка подлинности в Интернете  

Служба поддержки Microsoft Edge для нового [API проверки подлинности для веб-](../device/web-authentication.md) приложения с помощью биометрии [Windows Hello](https://www.microsoft.com/windows/comprehensive-security) обновлена с учетом указанных ниже изменений.  

*   Начальная реализация API экспериментальной веб-проверки подлинности, представленной в [EdgeHTML 14](https://blogs.windows.com/msedgedev/2016/08/04) \ (обновление годовщины для Windows 10, сборка 10240, 7/2016 \), была предоставлена посредством API с префиксами, предустановленными в MS. \ (интерфейс [MSCredentials](/previous-versions//mt697639(v=vs.85)) \).  Несмотря на то что эти API по-прежнему доступны в EdgeHTML 15, они теперь не рекомендуются в пользу нестандартных API-интерфейсов и поведения, определенных в более [поздних](https://w3.org/TR/2016/WD-webauthn-20160928) версиях спецификаций, и, возможно, они будут продолжать изменяться в соответствии с характеристиками стандартизации.  

*   Новейшая реализация Microsoft Edge по умолчанию отключена и поставляется за пометкой \ (введите `about:flags` адресную строку, чтобы включить ее).  

*   Microsoft Edge пока не поддерживает внешние учетные данные, такие как USB-ключи или устройства Bluetooth.  Текущий API ограничивается внедренными учетными данными, хранящимися в TPM.  Если на устройстве нет доверенного платформенного модуля, используется резервный вариант программного обеспечения.  

*   Учетная запись пользователя Windows, зарегистрированная в системе, должна поддерживать по крайней мере ПИН-код, а предпочтительнее или биометрию отпечатков пальцев.  Это необходимо для того, чтобы система Windows могла проверить подлинность доступа к доверенному платформенному модулю.  

*   Из [предварительно определенных расширений](https://w3.org/TR/webauthn/#extension-predef) , описанных в этой спецификации, Microsoft EDGE поддерживает только [Fido AppID](https://w3.org/TR/webauthn/#extension-appid) \ ( `webauthn_txAuthSimple` \) в данный момент.  

*  Этот `timeoutSeconds` параметр в настоящее время не вычисляется  

### WebDriver  

EdgeHTML 15 предлагает несколько обновлений для веб-дисководов, включая поддержку для флагов автоматической командной строки и новых конечных точек команд:  

| Метод | Шаблон URI | Команда |  
|:--- |:---  |:--- |    
| POST | /Session/{Session ID}/Alert/Accept | [Уведомление о принятии](https://w3c.github.io/webdriver/webdriver-spec.html#dfn-accept-alert) |  
| POST | /Session/{Session ID}/Alert/dismiss | [Закрыть оповещение](https://w3c.github.io/webdriver/webdriver-spec.html#dfn-dismiss-alert) |  
| GET | /Session/{Session ID}/Alert/Text | [Получение текста оповещения](https://w3c.github.io/webdriver/webdriver-spec.html#dfn-get-alert-text) |  
| POST | /Session/{Session ID}/Alert/Text | [Отправка текста оповещения](https://w3c.github.io/webdriver/webdriver-spec.html#dfn-send-alert-text) |  
| POST | /Session/{Session ID}/Execute/Async | [Выполнение сценария Async](https://w3c.github.io/webdriver/webdriver-spec.html#dfn-execute-async-script) |  
| POST | /Session/{Session ID}/Execute/Sync | [Выполнение сценария](https://w3c.github.io/webdriver/webdriver-spec.html#dfn-execute-script) |  
| GET | /Session/{Session ID}/Window | [Получение маркера окна](https://w3c.github.io/webdriver/webdriver-spec.html#get-window-handle) |  
| GET | /Session/{Session ID}/Window/Handles | [Получение дескрипторов окон](https://w3c.github.io/webdriver/webdriver-spec.html#dfn-get-window-handles) |  

Дополнительные сведения и состояние других функций для работы с такими сетевыми накопителями можно найти в этом сетевом [накопителе](../../webdriver.md).  

## Новые API-интерфейсы в EdgeHTML 15  

Ниже приведен полный список новых API-интерфейсов в EdgeHTML 15.  Они перечислены в формате `[interface name].[api name]` .  

<iframe height='582' scrolling='no' title='Новые API EdgeHTML15' src='//codepen.io/MicrosoftEdgeDocumentation/embed/evRjjZ/?height=582&theme-id=23761&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>Ознакомьтесь с <a href='http://codepen.io/MicrosoftEdgeDocumentation/pen/evRjjZ/'> новыми API EdgeHTML15 в </a> Microsoft Edge Docs ( <a href='http://codepen.io/MicrosoftEdgeDocumentation'> @MicrosoftEdgeDocumentation </a> ) на <a href='http://codepen.io'> CodePen </a> .</iframe>  

## Предыдущие выпуски EdgeHTML  

[EdgeHTML 12/Windows Build 10240 (7/2015)](./edgehtml-12.md)  

[EdgeHTML 13/Windows Build 10586 (11/2015)](./edgehtml-13.md)  

[EdgeHTML 14/Windows Build 14393 (8/2016)](./edgehtml-14.md)  
