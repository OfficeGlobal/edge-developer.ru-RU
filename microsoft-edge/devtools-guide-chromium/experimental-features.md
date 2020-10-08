---
description: Последние экспериментальные функции в Microsoft Edge DevTools
title: Экспериментальные функции
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools, эксперименты
ms.openlocfilehash: f885201ddfb7553a2b9c58a07dd52b7a77c4137a
ms.sourcegitcommit: 0326a4082064e9cdfa602736f3f9ce7d8d294604
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/05/2020
ms.locfileid: "11094935"
---
# Экспериментальные функции  

Microsoft Edge DevTools предоставляет доступ к экспериментальным функциям, которые все еще находятся на стадии разработки.  Вы можете протестировать и [оставить отзыв](#providing-feedback-on-experimental-features) , прежде чем каждый компонент будет выпущен.  

Хотя экспериментальные функции доступны во всех каналах Microsoft EDGE, вы можете получить последние экспериментальные функции с помощью канала Microsoft Edge Канарские Channel.  

## Включение экспериментальных функций  

Чтобы включить экспериментальные функции в Microsoft EDGE, выполните указанные ниже действия.  

1.  [Откройте DevTools][DevtoolsOpen].  
     *   Выберите `Control` + `Shift` + `I` \ (Windows \) или `Command` + `Option` + `I` \ (macOS \).  Дополнительные сведения можно найти в разделе [сочетания клавиш Microsoft Edge DevTools][DevToolsShortcuts].  
1.  Открытие области [параметров][DevToolsCustomizeSettings] .  
    *   Выберите `Shift` + `?` .  Дополнительные сведения можно найти в разделе [сочетания клавиш Microsoft Edge DevTools][DevToolsShortcuts].  
1.  В левой части области **параметров** выберите раздел **эксперименты** .  
    
    :::image type="complex" source="./media/experiments-devtools.msft.png" alt-text="Список экспериментов в параметрах DevTools" lightbox="./media/experiments-devtools.msft.png":::
       Список экспериментов в параметрах DevTools  
    :::image-end:::  
    
1.  На странице " **эксперименты** " прокрутите список всех доступных экспериментальных функций и установите флажок рядом с каждым компонентом, который нужно протестировать.  
1.  Закройте и снова откройте Microsoft Edge DevTools.  

> [!NOTE]
> Экспериментальные функции постоянно обновляются и могут привести к проблемам с производительностью.  Чтобы отключить экспериментальную функцию, откройте страницу **эксперименты** и снимите флажок экспериментальной функции, которую вы хотите отключить.  

## Выделены экспериментальные функции  

В следующих разделах описаны новые экспериментальные функции, доступные в Microsoft Edge.  

| Экспериментальная функция | Версия Microsoft Edge |  
|:--- |:--- |  
| [Эмуляция: поддержка двух режимов экрана](#emulation-support-dual-screen-mode) | 84 или более поздняя версия |  
| [Включение новых функций отладки CSS Grid](#enable-new-css-grid-debugging-features) | 85 или более поздняя версия |  
| [Включение поддержки перемещения вкладок между панелями](#enable-support-to-move-tabs-between-panels) | 85 или более поздняя версия |  
| [Включить подсказку](#enable-webhint) | 85 или более поздняя версия |  
| [Включение сетевой консоли](#enable-network-console) | 85 или более поздняя версия |  
| [Средство просмотра исходного порядка](#source-order-viewer) | 86 или более поздняя версия |  

### Эмуляция: поддержка двух режимов экрана  

Предоставляет дополнительные функции для эмуляции двух новых двух экранов и устройств складная в Microsoft Edge.  

*   [Surface Duo][SurfaceDevicesDuo]  
*   [Samsung Galaxy сгиб][SamsungMobileGalaxyFold]  

Эмулирует устройства и переключаться между следующими элементами.  

*   режим с одним экраном или сложением  
*   возможность установки на два экрана или несложенный  
    
[Включите экспериментальные API веб-платформ](#enable-experimental-apis) и используйте [функцию многоэкранной][DualScreenDocsCssMedia] группировки с экрана CSS и [API JavaScript getWindowSegments][DualScreenDocsJSAPI] для расширения вашего веб-сайта (или приложения) на двойном экране и на складная устройствах.  

:::image type="complex" source="./media/experiments-surface-duo-emulation.msft.png" alt-text="Список экспериментов в параметрах DevTools" lightbox="./media/experiments-surface-duo-emulation.msft.png":::  
   Эмуляция Surface Duo в Microsoft Edge  
:::image-end:::  

#### Включение экспериментальных API  

Чтобы использовать [функцию многоэкранной области экрана CSS][DualScreenDocsCssMedia] и [API JavaScript getWindowSegments][DualScreenDocsJSAPI], включите `Experimental Web Platform features` флажок в Microsoft Edge.  Выполните указанные ниже действия.  

1.  Перейдите к `edge://flags` .  
1.  В текстовом поле **Флаги поиска** введите `Experimental Web Platform features` , выберите " **экспериментальные компоненты веб-платформы** ", а затем **Enabled**— " **Отключить** ".  
1.  Перезапустите Microsoft Edge.  

:::image type="complex" source="./media/experiments-dual-screen-emulation-edge-flags.msft.png" alt-text="Список экспериментов в параметрах DevTools" lightbox="./media/experiments-dual-screen-emulation.msft.png":::
   Флажок включения функций экспериментальной веб-платформы  
:::image-end:::  

> [!NOTE]
> Если вы используете запросы на поиск [мультимедиа в каскадных таблицах][DualScreenDocsCssMedia] или [API-интерфейс перечисления сегмента Windows (JavaScript][DualScreenDocsJSAPI] ) для повышения качества сайта или приложения для служб [Surface Duo][SurfaceDevicesDuo], необходимо также включить флажок **экспериментальные возможности веб-платформы** в [приложении Android Microsoft Edge][GooglePlayMicrosoftEdge] на устройстве [Surface Duo][SurfaceDevicesDuo] .  
> 
> Если флажок **"экспериментальные веб-платформа** " включен [в классическом приложении Microsoft][MicrosoftEdge] EDGE и отключен для [приложения Android (Microsoft Edge][GooglePlayMicrosoftEdge]), поведение вашего веб-сайта или приложения в эмуляторе Duo Surface в классическом приложении Microsoft EDGE не совпадает с [приложением Android Microsoft][GooglePlayMicrosoftEdge] EDGE на [Surface Duo][SurfaceDevicesDuo].  Убедитесь в том, что для устройств Android и Desktop Microsoft Edge успешно используются Эмуляторы Surface Duo в классической платформе [Microsoft Edge][MicrosoftEdge].  

#### Тестирование на устройствах складная и на двух экранах  

При эмуляции [Duo Surface][SurfaceDevicesDuo] в Microsoft Edge с двумя экранами на экране добавляется стык \ (расстояние между двумя экранами), нарисованный на веб-сайте или в приложении.  

Эмуляция дисплея соответствует способу обработки веб-сайта \ (или приложения \) в [приложении Microsoft Edge][GooglePlayMicrosoftEdge] на платформе [Surface Duo][SurfaceDevicesDuo].  Возможно, вам потребуется обновить ваш веб-сайт \ (или приложение \), чтобы он лучше отображался на стыке.  Для получения дополнительных сведений о адаптации веб-сайта к стыку (или внешнему приложению) перейдите к разделу [Работа с стыком][DualScreenIntroductionHowWorkSeam] в документации Surface Duo.  

На [панели инструментов устройства][DevtoolsDeviceModeIndexSimulateMobileViewport] есть дополнительные функции, с помощью которых можно протестировать веб-сайт или приложение в нескольких элементах управления и ориентации.  **Rotate** ![ ][ImageRotateIcon] Чтобы повернуть окно просмотра на альбомную ориентацию, нажмите поворот на (повернуть). Объедините функцию с **диапазоном** \ ( ![ Span ][ImageSpanIcon] \), чтобы переключаться между одним экраном или сложением, а также с двойным экраном или без сгиба.  Вместе функции позволяют тестировать ваш веб-сайт или приложение во всех четырех возможностях и ориентациях.  

:::image type="complex" source="./media/experiments-dual-screen-emulation-rotate-span.msft.png" alt-text="Список экспериментов в параметрах DevTools" lightbox="./media/experiments-dual-screen-emulation-rotate-span.msft.png":::
   Матрица геоуровней и ориентации для двухпроцессорных и складная устройств  
:::image-end:::  

Значок " **экспериментальные веб-платформы** " \ ( ![ ExperimentalApis ][ImageExperimentalApisIcon] \) отображает состояние флага " **экспериментальные веб-платформы** ".  Если пометка включена, значок выделена.  Если флажок выключен, значок не выделяется.  Чтобы включить параметр \ (или выключить), найдите `edge://flags` и переключите флажок.  

<!-- Commenting out until the icon issue is fixed in Edge Canary
The **Experimental Web Platform features** \(![ExperimentalApis][ImageExperimentalApisIcon]\) icon displays the state of the **Experimental Web Platform features** flag.  If the flag is turned on, the icon is highlighted.  If the flag is turned off, the icon is not highlighted.  To turn on \(or off\) the flag, either choose the icon or navigate to `edge://flags` and toggle the flag.   -->  

Ниже приведены дополнительные ресурсы, которые помогут вам повысить качество вашего веб-сайта (или приложения) на устройствах с двумя экранами.
*   Дополнительные сведения о веб-разработке на устройствах с двумя экранами можно найти на [веб-сайте с двумя экранами][DualScreenWebIndex].  
*   Установите [эмулятор Surface Duo][DualScreenAndroidUseEmulator].  Он отличается от эмулятора в Microsoft EDGE, эмулирует центр Surface Duo с Android и интегрируется с [Android][AndroidDeveloperStudio].  Дополнительные сведения можно найти в [пакете SDK Surface Duo][DualScreenAndroidGetDuoSdk].  

> [!NOTE]
> Ниже приведен список текущих известных проблем.  
> 
> *   При использовании [клиента удаленного рабочего стола Microsoft][RemoteDesktopClientDocs] для подключения к удаленному компьютеру и эмуляции [Galaxyого сгиба][SamsungMobileGalaxyFold] [Surface Duo][SurfaceDevicesDuo] или Samsung, указатель может стабилизации видеоизображения или перебоям.  Если вы столкнулись с проблемой, [отправьте отзыв](#providing-feedback-on-experimental-features).  

### Включение новых функций отладки CSS Grid  

Эта экспериментальная функция предоставляет ряд новых визуализаций, которые помогут вам в отладке макетов сетки CSS.  Чтобы просмотреть последние экспериментальные функции, [Включите этот эксперимент](#turn-on-experimental-features) и перезагрузите DevTools.  Этот эксперимент включен по умолчанию в 87 EDGE и более поздних версий.  

#### Просмотр наложенных указателей сетки с помощью средства проверки  

С помощью средства **проверки** можно быстро определить и визуализировать макеты сетки CSS на веб-сайте, наведя на них указатель мыши.  Щелкните значок **проверить** \ ( ![ проверить ](./media/inspect-icon.msft.png) \) в левом верхнем углу DevTools.  Затем наведите указатель мыши на элемент Grid на веб-сайте, который вы отлаживается.  Контуры отображаются вокруг сетки, а Заливка обозначает расположение зазоров сетки, если они есть.  

:::image type="complex" source="./media/grid-inspect.msft.png" alt-text="Список экспериментов в параметрах DevTools" lightbox="./media/grid-inspect.msft.png":::
   Просмотр сеток с помощью средства "Проверка"  
:::image-end:::  

#### Просмотр наложенных закрытий сетки  

В Microsoft Edge 86 и более поздних версиях функция «экспериментальная сетка каскадных стилей» также обеспечивает возможность включения постоянны наложенные линии сетки.  Сохраняемые перекрытия предоставляют несколько преимуществ.  

*   После прокрутки на странице сохраняются сохраняемые наложения, перемещайте мышь и используйте другие функции DevTools.  
*   Одновременно может быть включена несколько постоянных наложений, что позволяет одновременно просматривать несколько макетов сетки.  
*   Постоянная наложение предлагает множество параметров настройки, например скрытие или отображение имен областей сетки, зазоров сетки, размеров дорожек и т. д.  

Два способа включения режима постоянной перекрытия сетки.  

*   Нажмите кнопку **Grid** lozenge рядом с элементом Grid, показанным в дереве DOM инструмента **элементы** .  
    
    :::image type="complex" source="./media/grid-adorner.msft.png" alt-text="Список экспериментов в параметрах DevTools" lightbox="./media/grid-adorner.msft.png":::
       Lozenge сетки в инструменте "элементы"  
    :::image-end:::  
    
*   Откройте новую панель **макета** , расположенную в инструменте элементы, и установите флажок рядом с каждым элементом Grid, который вы хотите подчеркнуть.  
    
    :::image type="complex" source="./media/grid-layout-zoom.msft.png" alt-text="Список экспериментов в параметрах DevTools" lightbox="./media/grid-layout-zoom.msft.png":::
       Панель макета  
    :::image-end:::  
    
#### Настройка постоянных наложений  

Новая панель **макета** , расположенная в инструменте " **элементы** " рядом с полями **стили** и **вычисляемые** вкладки в EDGE 86 и более поздних версий — параметры конфигурации для постоянных наложений.  

:::image type="complex" source="./media/experiments-grid.msft.png" alt-text="Список экспериментов в параметрах DevTools" lightbox="./media/experiments-grid.msft.png":::
   Функция отладки сетки каскадных стилей  
:::image-end:::  

### Включение поддержки перемещения вкладок между панелями  

Обычно такие инструменты, как **элементы** и **сеть** , могут открываться только в главной панели, расположенной в верхней части DevTools.  Такие инструменты, как **трехмерные представления** и **проблемы** , которые обычно закрываются на панели **ящика** , которая находится в нижней части DevTools.  После выбора эксперимента вы можете перемещать инструменты между верхней и нижней панелями.  Чтобы переместить инструмент, наведите на него указатель мыши, откройте контекстное меню, а затем выберите команду **переместить в начало** или **Переместить вниз**.   Этот эксперимент позволяет настроить макет DevTools.  Чтобы показать или скрыть панель **ящика** , нажмите кнопку `Escape` .  

:::image type="complex" source="./media/experiments-move-panels.msft.png" alt-text="Список экспериментов в параметрах DevTools" lightbox="./media/experiments-move-panels.msft.png":::
   Перемещение вкладок между панелями  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Включить подсказку  

веб- [Подсказка][WebhintMain] — это средство с открытым исходным кодом, которое предоставляет отзыв в реальном времени для веб-сайтов и локальных веб-страниц.  Тип обратной связи, предоставляемой функцией " [Подсказка][WebhintMain]".  

*   специальные возможности  
*   совместимость с различными браузерами  
*   безопасность"  
*   эффективности  
*   Приложения PWA  
*   другие распространенные проблемы с веб-разработками  

Эксперименты с этой [подсказкой][WebhintMain] отображаются на панели " [вопросы][DevtoolsIssues] " в виде обратной связи.  Выберите вопрос для отображения документации решения и списка уязвимых ресурсов на вашем веб-сайте.  Выберите ссылку на ресурс, чтобы открыть область " **сеть**, **источники**или **элементы** " в DevTools.  

:::image type="complex" source="./media/experiments-webhint.msft.png" alt-text="Список экспериментов в параметрах DevTools" lightbox="./media/experiments-webhint.msft.png":::
   Обратная связь по этой подсказке на панели " **вопросы** "  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Включение сетевой консоли  

**Сетевая консоль** — это рабочее название эксперимента для создания искусственных сетевых запросов по протоколу HTTP.  Вы можете использовать эксперименты с **сетевой консолью** для отправки запросов на веб-API.  

После включения эксперимента убедитесь, что вы перезапустите DevTools.  Чтобы использовать **консоль "сеть**", выполните указанные ниже действия.  

1.  Открытие области " **сеть** ".  
1.  Найдите сетевой запрос, который вы хотите изменить и отправить повторно.  
1.  Откройте контекстное меню \ (щелкните правой кнопкой мыши и выберите команду **изменить и воспроизвести**).  
1.  Когда откроется **Сетевая консоль** , измените сведения о сетевом запросе.  
1.  Нажмите кнопку **Отправить**.  

:::image type="complex" source="./media/network-network-console.msft.png" alt-text="Список экспериментов в параметрах DevTools" lightbox="./media/network-network-console.msft.png":::
   **Сетевая консоль** в **консольном** ящике  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Средство просмотра исходного порядка  

**Средство просмотра исходного порядка** — это эксперимент, в котором отображается порядок элементов в источнике страницы.  Порядок отображения на экране может отличаться от порядка источников, который в своюмся случае будет использовать средство чтения с экрана и пользователи клавиатуры.  Для поиска различий между порядком отображения на экране и порядком расположения источника используйте эксперимент в **средстве просмотра исходного порядка** .  

После включения эксперимента убедитесь, что вы перезапустите DevTools.  Чтобы использовать **средство просмотра заказов исходного кода**, выполните указанные ниже действия.  

1.  Откройте область **элементы** .  
1.  Откройте область **Специальные возможности** на панели ящик \ (Нижняя \).  
1.  В разделе **средство просмотра исходного заказа** установите флажок **Показать порядок источников** .  
1.  Выделит любой HTML-элемент, чтобы отобразить наложение, порядок расположения которых указан в источнике страницы.  

:::image type="complex" source="./media/experiments-source-order-viewer.msft.png" alt-text="Список экспериментов в параметрах DevTools" lightbox="./media/experiments-source-order-viewer.msft.png":::
   **Средство просмотра исходного порядка** на панели " **Специальные возможности** "  
:::image-end:::  

<!--Available in Microsoft Edge version 86 and later.  -->  

## Предыдущие экспериментальные функции  

*   Теперь [трехмерный вид][Devtools3dViewIndex] доступен и включен по умолчанию в Microsoft Edge версии 83 или более поздней.  
*   [Настройка сочетаний клавиш][DevtoolsCustomKeyboardShortcuts] теперь доступна и включена по умолчанию в Microsoft Edge версии 86 или более поздней.  

## Отзывы о экспериментальных функциях  

Чтобы оставить отзыв о экспериментах Microsoft Edge DevTools или каких-либо других связанных с DevTools.  

*   Отправка отзыва с помощью значка " **Отправить отзыв** " в DevTools  
*   Твит на [@EdgeDevTools][TwitterEdgedevtools]  

:::image type="complex" source="./media/bing-devtools-send-feedback.msft.png" alt-text="Список экспериментов в параметрах DevTools" lightbox="./media/bing-devtools-send-feedback.msft.png":::
   Значок " **Отправить отзыв** " в Microsoft Edge DevTools  
:::image-end:::  

<!--  
## Getting in touch with the Microsoft Edge DevTools team  

[!INCLUDE [contact DevTools team note](./includes/contact-devtools-team-note.md)]  
-->  

<!-- image links -->  

[ImageRotateIcon]: ./media/rotate-dark-icon.msft.png  
[ImageSpanIcon]: ./media/span-dark-icon.msft.png  
[ImageExperimentalApisIcon]: ./media/experimental-apis-dark-icon.msft.png  

<!-- links -->  

[Devtools3dViewIndex]: ./3d-view/index.md "Трехмерный вид | Документы Microsoft"  
[DevToolsCustomizeSettings]: ./customize/index.md#settings "Параметры: Настройка Microsoft Edge DevTools | Документы Microsoft"  
[DevtoolsDeviceModeIndexSimulateMobileViewport]: ./device-mode/index.md#simulate-a-mobile-viewport "Эмуляция мобильных устройств с помощью режима устройства в Microsoft Edge DevTools | Microsoft Edge"  
[DevtoolsIssues]: ./issues/index.md "Поиск и устранение проблем с помощью средства Microsoft Edge DevTools "вопросы" | Документы Microsoft"  
[DevToolsShortcuts]: ./shortcuts.md "Сочетания клавиш в Microsoft Edge DevTools | Документы Microsoft"  
[DevtoolsOpen]: ./open.md "Открыть Microsoft Edge DevTools | Документы Microsoft"  
[DevtoolsCustomKeyboardShortcuts]: ./customize/shortcuts.md "Настройка сочетаний клавиш в Microsoft Edge DevTools | Документы Microsoft"

[DualScreenWebIndex]: /dual-screen/web/index "Веб-интерфейс на базе двух экранов | Документы Microsoft"  
[DualScreenAndroidGetDuoSdk]: /dual-screen/android/get-duo-sdk "Получение эмулятора Surface Duo | Документы Microsoft"  
[DualScreenIntroductionHowWorkSeam]: /dual-screen/introduction#how-to-work-with-the-seam "Работа с стыками — введение в работу с устройствами с двумя экранами | Документы Microsoft"  
[DualScreenAndroidUseEmulator]: /dual-screen/android/use-emulator "Использование эмулятора Surface Duo | Документы Microsoft"  
[DualScreenDocsCssMedia]: /dual-screen/web/css-media-spanning "Функция многоэкранной группировки с экрана в каскадных таблицах CSS | Документы Microsoft"  
[DualScreenDocsJSAPI]: /dual-screen/web/javascript-getwindowsegments "API getWindowSegments JavaScript для устройств с двумя экранами | Документы Microsoft"  

[RemoteDesktopClientDocs]: /windows-server/remote/remote-desktop-services/clients/remote-desktop-clients "Клиенты удаленных рабочих столов | Документы Microsoft"

[MicrosoftEdge]: https://www.microsoft.com/edge "Microsoft Edge"  

[SurfaceDevicesDuo]: https://www.microsoft.com/surface/devices/surface-duo "Surface Duo | Microsoft Surface"  

[AndroidDeveloperStudio]: https://developer.android.com/studio/ "Android Studio"  

[GooglePlayMicrosoftEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Microsoft Edge | Google Play"  

[SamsungMobileGalaxyFold]: https://www.samsung.com/mobile/galaxy-fold/ "Galaxy, сгиб | Samsung"  

[TwitterEdgedevtools]: https://www.twitter.com/EdgeDevTools "Microsoft Edge DevTools | Контента"  

[WebhintMain]: https://webhint.io "Подсказка"  
