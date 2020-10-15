---
description: Сведения об отладке элементов управления WebView2.
title: Приступая к отладке приложений WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/14/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 25a710796b499a78a43045266058029caa890b78
ms.sourcegitcommit: 61cc15d2fc89aee3e09cec48ef1e0e5bbf8d289a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/15/2020
ms.locfileid: "11119110"
---
# Приступая к отладке приложений WebView2  

Цель элемента управления Microsoft Edge WebView2 заключается в том, чтобы сочетать лучший из функций разработки веб-и собственных приложений, а также средств и инструментов.  Когда вы разрабатываете приложение WebView2, необходимо выполнить отладку приложения.  В этой статье описаны различные инструменты для отладки вашего веб-и собственного кода в приложении WebView2.  

## [Microsoft Edge DevTools](#tab/devtools)  

Используйте [средства разработчика Microsoft EDGE (Chromium)][DevtoolsGuideChromiumMain] для отладки содержимого веб-страницы, отображаемого в элементах управления WebView2, таким же образом, как и при отладке на других страницах, отображаемых в Microsoft Edge.  Чтобы открыть DevTools, установите фокус на элементе управления WebView, а затем выполните одно из указанных ниже действий.  

*   Выберите `F12` .  
*   Выберите `Ctrl` + `Shift` + `I` .  
*   Откройте контекстное меню, а затем щелкните правой кнопкой мыши и выберите команду `Inspect` .  

Дополнительные сведения можно найти в разделе [Общие сведения о DevTools][DevtoolsGuideChromiumMain].  

:::image type="complex" source="./media/f12.png" alt-text="Отладка DevTools" lightbox="./media/f12.png":::
   Отладка DevTools  
:::image-end:::  

## [VisualStudio](#tab/visualstudio)  

Visual Studio предоставляет различные инструменты отладки для веб-и машинного кода в приложениях WebView2.  В разделе Visual Studio основным фокусом является Отладка элементов управления WebView, однако другие методы отладки в Visual Studio можно использовать в обычном режиме.  Используйте следующий процесс для отладки веб-и машинного кода в приложениях Win32 или только для надстроек Office.  

> [!IMPORTANT]
> При отладке приложения в Visual Studio с присоединенным отладчиком машинного кода выбор `F12` может инициировать собственный отладчик вместо средств разработчика.  `Ctrl` + `Shift` + `I` Чтобы избежать ситуации, выберите или используйте контекстное меню \ (щелкните правой кнопкой мыши).  

Прежде чем начать, убедитесь, что выполнены следующие требования.  

*   Для отладки скриптов приложение должно быть запущено в Visual Studio.  
*   Вы не можете прикрепить отладчик к выполняющемуся процессу WebView2.  
*   Установите Visual Studio 2019 версии 16,4 Preview 2 или более поздней версии.  

Установка и настройка средств отладки сценариев в Visual Studio.  

1.  Выполните указанные ниже действия, чтобы установить компонент **диагностики JavaScript** в **классических разработках с + +**.  

    1. На панели проводника Windows введите `Visual Studio Installer` .  
    1. Щелкните **Установщик Visual Studio** , чтобы открыть его.  
    1. В установщике Visual Studio на установленной версии нажмите кнопку **Дополнительно** , а затем выберите команду **изменить**.  
    1. В Visual Studio в разделе **рабочие нагрузки**выберите параметр **Разработка классической среды на C++** .  
        
        :::image type="complex" source="./media/workloads.png" alt-text="Отладка DevTools" lightbox="./media/workloads.png":::
            Экран изменения рабочей нагрузки в Visual Studio :::image-end:::  
        
    1.  Выберите **отдельные компоненты**.  
    1.  В поле поиска введите `JavaScript diagnostics` .  
    1.  Выберите параметр **диагностики JavaScript** .  
    1.  Нажмите кнопку **изменить**. 
        
        :::image type="complex" source="./media/indivcomp.png" alt-text="Отладка DevTools" lightbox="./media/indivcomp.png":::
           Вкладка "изменение отдельных компонентов" в Visual Studio  
        :::image-end:::  
        
1.  Включите отладку сценариев для приложений WebView2.  
    1.  В проекте WebView2 откройте контекстное меню, а затем щелкните правой кнопкой мыши и выберите пункт **Свойства**.  
    1.  В разделе **Свойства конфигурации**выберите пункт **Отладка**.  
    1.  В разделе **Тип отладчика**выберите **JavaScript (WebView2)**.  
        
        :::image type="complex" source="./media/enbjs.png" alt-text="Отладка DevTools" lightbox="./media/enbjs.png":::
           Свойство конфигурации **отладки** в Visual Studio  
        :::image-end:::  
        
Выполните указанные ниже действия, чтобы выполнить отладку приложения WebView2.  

1.  Чтобы задать точку останова в исходном коде, наведите указатель мыши на левый номер строки и выберите точку останова.  Адаптеры отладки JS-и ст не выполняют сопоставление исходного пути.  Вы должны открыть именно тот же путь, связанный с вашим WebView2.  
    
    :::image type="complex" source="./media/breakpoint.png" alt-text="Отладка DevTools" lightbox="./media/breakpoint.png"::: 
       Добавление точки останова в Visual Studio  
    :::image-end:::  
    
1.  Чтобы запустить отладчик, выберите битовый Размер платформы, а затем нажмите зеленую кнопку воспроизведения рядом с **местным отладчиком Windows**.  Приложение запустится, и отладчик подключится к первому процессу WebView2, который вы создали.  
    
    :::image type="complex" source="./media/run.png" alt-text="Отладка DevTools" lightbox="./media/run.png"::: 
       **Локальный отладчик Windows** для Visual Studio  
    :::image-end:::  
    
1.  В **консоли отладки**найдите выходные данные отладчика.  
    
    :::image type="complex" source="./media/console.png" alt-text="Отладка DevTools" lightbox="./media/console.png"::: 
       **Консоль отладки** Visual Studio  
    :::image-end:::  
    
## [Visual Studio Code](#tab/visualstudiocode)  

Используйте код Microsoft Visual Studio для отладки сценариев, которые выполняются в элементах управления WebView2.  <!--Ensure that you're using Visual Studio Code version [insert build here] or later.  -->  

В коде Visual Studio выполните указанные ниже действия, чтобы выполнить отладку кода. 

1.  Для вашего проекта требуется `launch.json` файл.  Если в проекте нет `launch.json` файла, скопируйте приведенный ниже фрагмент кода и создайте новый `launch.json` файл.  
        
    ```json
        "name": "Hello debug world",
        "type": "pwa-msedge",
        "port": 9222, // The port value is optional, and the default value is 9222.
        "request": "launch",
        "runtimeExecutable": "C:/path/to/your/webview2/application.exe",
        "env": {
            // Customize for your application location if needed
            "Path": "%path%;e:/path/to/your/application/location; "
        },
        "useWebView": true,
    ```  
        
1.  Чтобы задать точку останова в исходном коде, наведите указатель мыши на строку и выберите `F9`
    
    :::image type="complex" source="./media/breakpointvs.png" alt-text="Отладка DevTools" lightbox="./media/breakpointvs.png":::
       Точка останова, заданная в коде Visual Studio  
    :::image-end:::
    
    > [!NOTE]
    > Поскольку код Visual Studio не выполняет сопоставление источника, убедитесь, что точки останова задаются в том же файле, который WebView2 использует.  Если пути не совпадают, код Visual Studio не приостанавливает выполнение кода в точке останова.  
    
1.  Запустите код.  
    1.  На вкладке " **выполнить** " в раскрывающемся меню выберите пункт "Настройка запуска".  
    1.  Чтобы начать отладку приложения, нажмите кнопку начать отладку, которая является зеленым треугольником рядом с раскрывающимся списком настройки запуска.  
        
        :::image type="complex" source="./media/runvs.png" alt-text="Отладка DevTools" lightbox="./media/runvs.png":::
           Вкладка "запуск кода" в Visual Studio  
        :::image-end:::  
        
1.  Откройте **консоль отладки** , чтобы просмотреть результаты отладки и ошибки.  
    
    :::image type="complex" source="./media/resultsvs.png" alt-text="Отладка DevTools" lightbox="./media/resultsvs.png":::
       Консоль отладки кода Visual Studio  
    :::image-end:::  
    
**Дополнительные параметры**.  

*   Целевая Отладка WebView. 

    В некоторых приложениях WebView2 можно использовать более одного элемента управления WebView2. Выбор элемента управления WebView2 для отладки в этой ситуации можно использовать целевую отладку WebView2 
    
    Откройте `launch.json` и выполните следующие действия, чтобы использовать целевую отладку WebView.  
    
    1.  Убедитесь, что `useWebview` для параметра задано значение `true` .  
    1.  Добавьте `urlFilter` параметр.  Когда элемент управления WebView2 переходит по URL-адресу, `urlFilter` значение параметра используется для сравнения строк, которые отображаются в URL-адресе.  
    
    ```json
    "useWebview": "true",
    "urlFilter": "*index.ts",
    
    // Other urlFilter options.
    
    urlFilter="*index.ts"    // Match any url that ends with index.ts, and ignore all leading characters. 
    urlFilter="*index*"      // Match any url that contains the string index anywhere in the URL.  
    urlFilter="file://C:/path/to/my/index.ts," // To match explicit file called index.ts.  
    ```  
    
    При отладке приложения может потребоваться шаг с заходом в начало процесса рендеринга. Если вы обрабатываете веб-страницы на сайтах, но у вас нет доступа к исходному коду, вы можете использовать этот `?=value`  параметр, так как на веб-страницах пропускаются нераспознанные параметры.   
    
    > [!IMPORTANT]
    > После того как первое соответствие найдено в URL-адресе, отладчик остановится.  Одновременная отладка двух элементов управления WebView2 не поддерживается, так как порт CDP является общим для всех элементов управления WebView2 и использует один номер порта.  
    
*   Отладка запущенных процессов  
    
    Возможно, потребуется присоединить отладчик для выполнения процессов WebView2. Чтобы сделать это, установите `launch.json` `request` для параметра значение `attach` .
        
    ```json
        "name": "Hello debugging world",
        "type": "pwa-msedge",
        "port": 9222, 
        "request": "attach",
        "runtimeExecutable": "C:/path/to/your/webview2/application.exe",  
        "env": {
            "Path": "%path%;e:/path/to/your/build/location; "  
        },
        "useWebView": true
    ```  
        
    Элемент управления WebView2 должен открыть порт CDP, чтобы разрешить отладку элемента управления WebView2.  Код должен быть построен так, чтобы только один WebView2 элемент управления был открыт портом CDP, прежде чем запускать отладчик.  
    
*   Параметры трассировки отладки  
    
    Добавьте `trace` параметр в launch.json, чтобы включить трассировку отладки.  
    
    1.  Добавить `trace` параметр.  
        
 
        
        :::row:::
           :::column span="":::
              ```json
                "name": "Hello debugging world",
                "type": "pwa-msedge",
                "port": 9222, 
                "request": "attach",
                "runtimeExecutable": "C:/path/to/your/webview2/application.exe",  
                "env": {
                "Path": "%path%;e:/path/to/your/build/location; "  
                },
                "useWebView": true
                ,"trace": true  // Turn on  debug tracing, and save the output to a log file.
              ```  
              
              :::image type="complex" source="./media/tracelog.png" alt-text="Отладка DevTools" lightbox="./media/tracelog.png":::
                 Сохранение выходных данных отладки в файле журнала  
              :::image-end:::  
           :::column-end:::
           :::column span="":::
              ```json
              ,"trace": "verbose"  // Turn on verbose tracing in the Debug Output pane.
              ```  
              
              :::image type="complex" source="./media/verbose.png" alt-text="Отладка DevTools" lightbox="./media/verbose.png":::
                 Отладочный вывод кода Visual Studio с включенной подробной трассировкой  
              :::image-end:::  
           :::column-end:::
        :::row-end:::  
        
*   Отладка надстроек для Office.
    
    При отладке надстроек Office откройте исходный код надстройки в отдельном экземпляре кода Visual Studio.  Откройте launch.jsв приложении WebView2 и добавьте следующий фрагмент кода, чтобы прикрепить отладчик к надстройке Office.
    
    ```json
    ,"debugServer": 4711
    ```  
    
*   Устранение неполадок отладчика  
    
    При использовании отладчика вы можете столкнуться со следующими сценариями.  

    *   Отладчик не остановится на точке останова, и у вас есть отладочный вывод.  Чтобы устранить эту проблему, убедитесь, что файл с точкой останова является тем же файлом, который используется элементом управления WebView2.  Отладчик не выполняет сопоставление исходного пути.  
    *   Вы не можете присоединиться к выполняющемуся процессу, и вы получаете сообщение об ошибке тайм-аута.  Чтобы устранить эту проблему, убедитесь, что элемент управления WebView2 открыл порт CDP.  Убедитесь  `additionalBrowserArguments`  , что значение в реестре введено правильно, или параметры указаны правильно.  Дополнительные сведения можно найти в разделе [additionalBrowserArguments для DotNet][Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2environmentoptionsAdditionalbrowserarguments] и [additionalBrowserArguments для Win32][Webview2ReferenceWin32Webview2IdlParameters].  
    
* * *  


* * *  

## См. также  

*   Чтобы приступить к работе с WebView2, ознакомьтесь со статьей [руководства Приступая к работе с WebView2][Webview2MainGettingStarted].  
*   Полный пример возможностей WebView2 можно найти в репозитории [WebView2Samples][GithubMicrosoftedgeWebview2samples] на GitHub.
*   Более подробную информацию об API WebView2 можно найти в [справочнике API][Webview2ApiReference].
*   Дополнительные сведения о WebView2ах можно найти в статьях [ресурсы WebView2][Webview2MainNextSteps].

## Знакомство с командой Microsoft Edge WebView  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../../devtools-guide-chromium.md "Инструменты разработчика Microsoft EDGE (Chromium)"  

[Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2environmentoptionsAdditionalbrowserarguments]: /dotnet/api/microsoft.web.webview2.core.corewebview2environmentoptions.additionalbrowserarguments "Свойство CoreWebView2EnvironmentOptions. AdditionalBrowserArguments (Microsoft. Web. WebView2. Core) | Документы Microsoft"  
[Webview2ReferenceWin32Webview2IdlParameters]: /microsoft-edge/webview2/reference/win32/webview2-idl#createcorewebview2environmentwithoptions  "CreateCoreWebView2Environment-Globals | Документы Microsoft"  
[Webview2ApiReference]: ../webview2-api-reference.md "Справочник по API Microsoft Edge WebView2 | Документы Microsoft"  
[Webview2MainNextSteps]: ../index.md#next-steps "Дальнейшие действия — введение в Microsoft Edge WebView2 (Предварительная версия) | Документы Microsoft"  
[Webview2MainGettingStarted]: ../index.md#getting-started "Приступая к работе: знакомство с Microsoft Edge WebView2 (Предварительная версия) | Документы Microsoft"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView Feedback-MicrosoftEdge/WebViewFeedback | GitHub"  
[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2 Samples-MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftVscodeJSDebugWhatsNew]: https://github.com/microsoft/vscode-js-debug#whats-new "Новые возможности -Отладчик JavaScript для Visual Studio Code-Microsoft/vscode-JS-Debug | GitHub"  

[GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications]: https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications "Microsoft EDGE (Chromium) WebView Applications-Debugger (код Visual Studio) — отладчик для Microsoft Edge-Microsoft/vscode-Edge-debug2 | GitHub"  
