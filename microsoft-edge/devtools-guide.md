---
description: Ознакомьтесь с названием средств разработчика Microsoft Edge (EdgeHTML)
title: Автор средств разработчика Microsoft Edge (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: microsoft edge, web development, f12 tools, devtools
experimental: true
experiment_id: "51fe4b97-3e55-41"
ms.localizationpriority: high
---

# Средства разработчика Microsoft Edge (EdgeHTML)  

[!ВКЛЮЧИТЬ [new-devtools-version-note](includes/new-devtools-version-note.md)]  

Средства разработчика Microsoft Edge (EdgeHTML) созданы с использованием [TypeScript][TypeScriptIndex], работают на основе[ открытого исходного кода][GithubMicrosoftChakracore], оптимизированы для современных рабочих процессов внешнего интерфейса и теперь доступны как [отдельное приложение для Windows 10][MicrosoftStoreEdgeDevtoolsPreview] в Microsoft Store!  

Дополнительные сведения о новых возможностях см. в разделе [Средства разработчика в последнем обновлении Windows 10 (EdgeHTML 18)][DevtoolsGuideEdgehtmlWhatsnew].  

## Основные инструменты  

:::image type="complex" source="./devtools-guide/media/devtools.png" alt-text="Microsoft Edge (EdgeHTML) DevTools":::
  Средства разработчика Microsoft Edge (EdgeHTML)
:::image-end:::

<!--![Microsoft Edge \(EdgeHTML\) DevTools][ImageDevtoolsEdgehtml]  -->  

Средства разработчика Microsoft Edge (EdgeHTML) включают:  

*   Панель [элементов][DevtoolsGuideEdgehtmlElements] для редактирования HTML и CSS, проверки свойств специальных возможностей, просмотра слушателей событий и настройки точек останова изменений DOM  
*   [Консоль][DevtoolsGuideEdgehtmlConsole] для просмотра и фильтрации сообщений журнала, проверки объектов JavaScript и узлов DOM и запуска JavaScript в контексте выбранного окна или рамки  
*   [Отладчик][DevtoolsGuideEdgehtmlDebugger] для пошагового выполнения кода, настройки часов и точек останова, редактирования кода в реальном времени и проверки веб-хранилища и кешей файлов cookie  
*   [Сетевая][DevtoolsGuideEdgehtmlNetwork] панель для мониторинга и проверки запросов и ответов из сети и кеша браузера  
*   Панель [производительности][DevtoolsGuideEdgehtmlPerformance] для профилирования времени и системных ресурсов, необходимых сайту  
*   Панель [памяти][DevtoolsGuideEdgehtmlMemory] для измерения использования ресурсов памяти и сравнения снимков кучи в разных состояниях выполнения кода  
*   Панель [хранилища][DevtoolsGuideEdgehtmlStorage] для проверки и управления веб-хранилищем, IndexedDB, файлами cookie и данными кеша  
*   Панель [Сервисные рабочие процессы][DevtoolsGuideEdgehtmlServiceworkers] для управления и отладки ваших сервисных рабочих процессов  
*   Панель [эмуляции][DevtoolsGuideEdgehtmlEmulation] для тестирования сайта с различными профилями браузера, разрешениями экрана и координатами расположения GPS  

Отправляйте ваши [отзывы и предложения](#getting-in-touch-with-the-microsoft-edge-devtools-team)!  

> [!СОВЕТ]
> [Выполняйте тест на Microsoft Edge (EdgeHTML) бесплатно в любом браузере][BrowserstackEdgehtml].  
> Команда Microsoft Edge объединилась с [BrowserStack][BrowserstackEdgehtml], чтобы предоставить бесплатное автоматическое тестирование Microsoft Edge (EdgeHTML) в реальном времени.  

## Приложение Microsoft Store  

**Средства разработчика Microsoft Edge (EdgeHTML)**[теперь доступны][DevtoolsGuideEdgehtmlWhatsnew] как отдельное [приложение для Windows 10 в Microsoft Store][MicrosoftStoreEdgeDevtoolsPreview], в дополнение к встроенным инструментам в браузере (`F12`). В версии для магазина есть панель **выбора** для подключения к открытым локальным и удаленным целевым страницам, а также макет с вкладками для удобного переключения между экземплярами средств разработчика.  

### Локальная отладка  

Чтобы выполнить отладку страницы локально, запустите приложение средств разработчика Microsoft Edge. **Локальная** панель средств выбора отображает все активные процессы содержимого EdgeHTML, включая открытые вкладки браузера Edge, запущенные [PWA][PwasEdgehtmlIndex] (процессы `WWAHost.exe`) и элементы управления [веб-просмотром][HostingWebview]. Выберите желаемую цель для прикрепления и откройте новый экземпляр вкладки средств разработчика.  

:::image type="complex" source="./devtools-guide/media/chooser_local.png" alt-text="DevTools app Local panel":::
  Локальная панель приложения средств разработчика
:::image-end:::

<!--![DevTools app Local panel][ImageDevtoolsGuideEdgehtmlChooselocal]  -->  

### Удаленная отладка  

Приложение средств разработчика Microsoft Edge представляет базовую поддержку для отладки страниц на удаленном компьютере с помощью нашего недавно выпущенного [протокола средств разработчика][DevtoolsProtocolEdgehtmlIndex]. В последнем выпуске предоставляется удаленный доступ к основным функциям на панелях: [«Отладчик»][DevtoolsGuideEdgehtmlDebugger], [«Элементы»][DevtoolsGuideEdgehtmlElements] (для операций только для чтения) и [Консоль»][DevtoolsGuideEdgehtmlConsole]. Удаленная отладка ограничена Microsoft Edge (EdgeHTML), на котором запущены узлы рабочего стола, с поддержкой других узлов EdgeHTML и устройств Windows 10, которые появятся в последующих выпусках.  

Для начала работы, ознакомьтесь с разделом [*Средства разработчика Microsoft Edge*][DevtoolsProtocolEdgehtmlClientsEdgePreview] документов [протокола средств разработчика][DevtoolsProtocolEdgehtmlIndex].  

:::image type="complex" source="./devtools-guide/media/chooser_remote.png" alt-text="DevTools app Remote panel":::
  Удаленная панель приложения средств разработчика
:::image-end:::

<!--![DevTools app Remote panel][ImageDevtoolsGuideEdgehtmlRemote]  -->  

## Общие сочетания клавиш  

> [!ВАЖНО]
> Все сочетания клавиш проверены в самой последней версии Windows.  
> Если вам не удается использовать сочетания клавиш, обновите вашу копию Windows.  

Эти сочетания клавиш управляют главным окном средств разработчика и должны работать со всеми средствами.  

| Действие | Сочетание клавиш |  
|:--- |:--- |  
| Показать или скрыть средства разработчика (открывает последнюю просмотренную панель) | `F12`, `Ctrl`+`Shift`+`I` |  
| Переключить закрепление (Отмена закрепления/Снизу/Справа) | `Ctrl`+`Shift`+`D` |  
| Открыть файл | `Ctrl`+`P`, `Ctrl`+`O` |  
| Показать нередактируемый исходный код HTML в отладчике | `Ctrl`+`U` |  
| Показать или скрыть консоль в нижней части любого другого средства | `Ctrl`+`` ` `` |  
| Переключиться на элементы (проводник DOM) | `Ctrl`+`1` |  
| Переключиться на консоль | `Ctrl`+`2` |  
| Переключиться на отладчик | `Ctrl`+`3` |  
| Переключиться в сеть | `Ctrl`+`4` |  
| Переключиться на производительность | `Ctrl`+`5` |  
| Переключиться в память | `Ctrl`+`6` |  
| Переключиться в эмуляцию | `Ctrl`+`7` |  
| Справочная документация | `F1` |  
| Следующее средство | `Ctrl`+`F6` |  
| Предыдущее средство | `Ctrl`+`Shift`+`F6` |  
| Предыдущее средство (из истории) | `Ctrl`+`Shift`+`[` |  
| Следующее средство (из истории) | `Ctrl`+`Shift`+`[` |  
| Следующий подфрейм | `F6` |  
| Предыдущий подфрейм | `Shift`+`F6` |  
| Следующее совпадение в поле поиска | `F3` |  
| Предыдущее совпадение в поле поиска | `Shift`+`F3` |  
| Поиск в поле поиска | `Ctrl`+`F` |  
| Перемещение фокуса на консоль в нижней части страницы | `Alt`+`Shift`+`I` |  
| Запустить средства разработчика на консоли | `Ctrl`+`Shift`+`J` |  
| Обновить страницу | `Ctrl`+`Shift`+`F5`, `Ctrl`+`R` |  

> [! ПРИМЕЧАНИЕ]
> Если при выполнении отладки и остановке на точке останова, действие **Обновить страницу** сначала возобновляет время выполнения.  

## Свяжитесь с командой средств разработчика Microsoft Edge  

Отправляйте ваши отзывы для улучшения средств разработчика Microsoft Edge (EdgeHTML)! Просто откройте средства (`F12`) и нажмите кнопку [Отправить отзыв](#microsoft-edge-edgehtml-developer-tools).  

Станьте [участником программы предварительной оценки Windows][WindowsInsiderProgram], чтобы [ознакомиться с новейшими функциями средств разработчика][DevtoolsGuideEdgehtmlWhatsnew]. Используйте приложение Центра отзывов о Windows, чтобы публиковать сообщения, голосовать, отслеживать и получать поддержку по общим предложениям и проблемам Windows.  

<!-- image links  -->  

<!--[ImageDevtoolsEdgehtml]: /microsoft-edge/devtools-guide/media/devtools.png "Microsoft Edge (EdgeHTML) DevTools"  -->  
<!--[ImageDevtoolsGuideEdgehtmlChooselocal]: /microsoft-edge/devtools-guide/media/chooser_local.png "DevTools app Local panel"  -->  
<!--[ImageDevtoolsGuideEdgehtmlRemote]: /microsoft-edge/devtools-guide/media/chooser_remote.png "DevTools app Remote panel"  -->  

<!-- links  -->  

[DevtoolsGuideEdgehtmlConsole]: /microsoft-edge/devtools-guide/console "Консоль"  
[DevtoolsGuideEdgehtmlDebugger]: /microsoft-edge/devtools-guide/debugger "Отладчик"  
[DevtoolsGuideEdgehtmlElements]: /microsoft-edge/devtools-guide/elements "Элементы"  
[DevtoolsGuideEdgehtmlEmulation]: /microsoft-edge/devtools-guide/emulation "Эмуляция"  
[DevtoolsGuideEdgehtmlMemory]: /microsoft-edge/devtools-guide/memory "Память"  
[DevtoolsGuideEdgehtmlNetwork]: /microsoft-edge/devtools-guide/network "Сеть"  
[DevtoolsGuideEdgehtmlPerformance]: /microsoft-edge/devtools-guide/performance "Производительность"  
[DevtoolsGuideEdgehtmlServiceworkers]: /microsoft-edge/devtools-guide/service-workers "Сервисные рабочие процессы"  
[DevtoolsGuideEdgehtmlStorage]: /microsoft-edge/devtools-guide/storage "Хранилище"  
[DevtoolsGuideEdgehtmlWhatsnew]: /microsoft-edge/devtools-guide/whats-new "Средства разработчика в последнем обновлении Windows 10 (EdgeHTML 18)"  
[DevtoolsProtocolEdgehtmlIndex]: /microsoft-edge/devtools-protocol/index "Протокол средств разработчика Microsoft Edge (EdgeHTML)"  
[DevtoolsProtocolEdgehtmlClientsEdgePreview]: /microsoft-edge/devtools-protocol/0.1/clients.md#microsoft-edge-devtools-preview "Предварительная версия средств разработчика Microsoft Edge — клиенты протокола средств разработчика"  
[HostingWebview]: /microsoft-edge/hosting/webview "Веб-просмотр (EdgeHTML) для приложений Windows 10"  
[PwasEdgehtmlIndex]: /microsoft-edge/progressive-web-apps-edgehtml/index "Прогрессивные веб-приложения (EdgeHTML) в Windows"  

[MicrosoftStoreEdgeDevtoolsPreview]: https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj "Предварительная версия средств разработчика Microsoft Edge"  

[WindowsInsiderProgram]: https://insider.windows.com "Программа предварительной оценки Windows"  

[BrowserstackEdgehtml]: https://www.browserstack.com/test-on-microsoft-edge-browser "Тестирование браузера Microsoft Edge бесплатно | BrowserStack"  

[GithubMicrosoftChakracore]: https://github.com/Microsoft/ChakraCore "microsoft/ChakraCore | GitHub"  

[TypeScriptIndex]: https://www.typescriptlang.org "TypeScript"  
