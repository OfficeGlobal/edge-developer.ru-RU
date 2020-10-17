---
description: Сведения о том, как статическая связь библиотеки загрузчика WebView2.
title: Статическая связь библиотеки загрузчика WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/15/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 880e9ed809dc268ee0b30b6ee3b5996711f54300
ms.sourcegitcommit: 0ded671914aae231493f418dd7645a04361dca1b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "11120126"
---
# Статическая связь с библиотекой загрузчика WebView2  

Возможно, вы захотите распространить приложение с помощью одного исполняемого файла, а не из множества файлов. Чтобы создать один исполняемый файл или уменьшить размер пакета, необходимо статически связать WebView2Loader-файлы. WebView2 SDK включает файл заголовка, `WebView2Loader.dll` а также `IDL` файл. `WebView2Loader.dll` — Это небольшой компонент, который помогает приложениям найти на устройстве среду выполнения WebView2 или нестабильные каналы Microsoft Edge.  

Для приложений, для которых не требуется отгрузка `WebView2Loader.dll` , выполните указанные ниже действия.  

1.  Откройте `.vcxproj` файл проекта для вашего приложения в текстовом редакторе, например в коде Visual Studio.  
    
    > [!NOTE]
    > `.vcproj`Файл проекта может быть скрытым файлом, что означает, что он не отображается в Visual Studio.  Используйте командную строку для поиска скрытых файлов.  
    
1.  Найдите раздел в коде, куда вы хотите добавить целевые файлы пакета NuGet WebView2.  Место в коде выделено на рисунке ниже.  

    :::image type="complex" source="./media/inserthere.png" alt-text="Фрагмент кода для файлов проекта" lightbox="./media/inserthere.png":::
       Фрагмент кода для файлов проекта   
    :::image-end:::  
  
1.  Скопируйте приведенный ниже фрагмент кода и вставьте его в том месте, где он `Microsoft.Web.WebView2.targets` включен.  

    ```xaml
    <PropertyGroup> 
        <WebView2LoaderPreference>Static</WebView2LoaderPreference> 
    </PropertyGroup>
    ```
      
    :::image type="complex" source="./media/staticlib.png" alt-text="Фрагмент кода для файлов проекта" lightbox="./media/staticlib.png":::
       Вставлен фрагмент кода  
    :::image-end:::  
    
1.  Измените дополнительные зависимости конфигурации сборки для вашего приложения.  Для начала найдите все `<AdditionalDependencies>` теги. Каждый из них добавляется `version.lib` как дополнительная зависимость к каждой конфигурации сборки в `.vcxproj` файле.  
    
    :::image type="complex" source="./media/versionlib.png" alt-text="Фрагмент кода для файлов проекта" lightbox="./media/versionlib.png":::
       Добавление `version.lib` в `ItemDefinitionGroups`  
    :::image-end:::  
    
    > [!NOTE]
    > Команда WebView2 стремится автоматизировать добавление дополнительной зависимости в будущих выпусках.  
    
1. Скомпилируйте и запустите приложение.

### Связь с командой WebView2  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

### См. также  

*   Чтобы приступить к работе с WebView2, перейдите в раздел [WebView2 начало работы][Webview2MainGettingStarted].  
*   Чтобы получить исчерпывающий пример возможностей WebView2, перейдите на [WebView2Samples][GithubMicrosoftedgeWebview2samples] в GitHub.
*   Более подробные сведения об API WebView2 можно найти в [справочнике по API][Webview2ApiReference].
*   Чтобы получить дополнительные сведения о WebView2, перейдите в раздел [ресурсы WebView2][Webview2MainNextSteps].

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../../devtools-guide-chromium.md "Инструменты разработчика Microsoft EDGE (Chromium) | Документы Microsoft"  

[Webview2ApiReference]: ../webview2-api-reference.md "Справочник по API Microsoft Edge WebView2 | Документы Microsoft"  
[Webview2MainNextSteps]: ../index.md#next-steps "Дальнейшие действия — введение в Microsoft Edge WebView2 (Предварительная версия) | Документы Microsoft"  
[Webview2MainGettingStarted]: ../index.md#getting-started "Приступая к работе: знакомство с Microsoft Edge WebView2 (Предварительная версия) | Документы Microsoft"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView Feedback-MicrosoftEdge/WebViewFeedback | GitHub"  
[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2 Samples-MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftVscodeJSDebugWhatsNew]: https://github.com/microsoft/vscode-js-debug#whats-new "Новые возможности -Отладчик JavaScript для Visual Studio Code-Microsoft/vscode-JS-Debug | GitHub"  

[GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications]: https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications "Microsoft EDGE (Chromium) WebView Applications-Debugger (код Visual Studio) — отладчик для Microsoft Edge-Microsoft/vscode-Edge-debug2 | GitHub"  
