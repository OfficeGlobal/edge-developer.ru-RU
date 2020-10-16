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
ms.openlocfilehash: a25bd85c8a6b17bdf8712c954eb7b7cc28738eb2
ms.sourcegitcommit: 442de63da52d00c6dc27fa08ccdb736534127566
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "11120075"
---
# Статическая связь библиотеки загрузчика WebView2  

## Контекст  

Что такое WebView2Loader.dll?  

*   WebView2 SDK включает файл заголовка, `WebView2Loader.dll.` а также `IDL` файл. `WebView2Loader.dll` — Это небольшой компонент, который помогает приложениям найти на устройстве среду выполнения WebView2 (или нестабильные каналы Microsoft EDGE).  

Для приложений, которые имеют одну среду выполнения и не хотят отгрузить их `WebView2Loader.dll` , выполните **описанные** ниже действия.  

## Процедура  

1.  Откройте `.vcxproj` файл проекта для вашего приложения в текстовом редакторе, например в коде Visual Studio.  
    
    > [!NOTE]
    > `.vcproj`Файл проекта может быть скрытым файлом, что означает, что он не отображается в Visual Studio.  Используйте командную строку для поиска скрытого файла.  
    
1.  Найдите раздел в коде, куда вы хотите добавить целевые файлы пакета NuGet WebView2.  Место в коде выделено на рисунке ниже.  
    
    :::image type="complex" source="./media/inserthere.png" alt-text="Фрагмент кода для файлов проекта" lightbox="./media/inserthere.png"::: 
       Фрагмент кода для файлов проекта  
    :::image-end:::  
    
1.  Скопируйте приведенный ниже фрагмент кода и вставьте его везде, где вы `Microsoft.Web.WebView2.targets` включены.  

    > [!NOTE]
    > Например, включите его после следующего блока кода.  
    > 
    > ```csharp
    > <Import Project="..\packages\Microsoft.Web.WebView2.0.9.579-prerelease\build\native\Microsoft.Web.WebView2.targets" Condition="Exists('..\packages\Microsoft.Web.WebView2.0.9.579-prerelease\build\native\Microsoft.Web.WebView2.targets')" />
    > ```  
    
    ```csharp
    <PropertyGroup> <WebView2LoaderPreference>Static</WebView2LoaderPreference> </PropertyGroup>
    ```
    
    :::image type="complex" source="./media/staticlib.png" alt-text="Фрагмент кода для файлов проекта" lightbox="./media/staticlib.png"::: 
       Вставлен фрагмент кода  
    :::image-end:::  
    
1.  Измените дополнительные зависимости конфигурации сборки для вашего приложения.  Для начала найдите все `<AdditionalDependencies>` теги.  
1.  Добавьте в `version.lib` `.vcxproj` файл для вашего приложения дополнительные зависимости для каждой другой конфигурации сборки в файле.  
    
    :::image type="complex" source="./media/versionlib.png" alt-text="Фрагмент кода для файлов проекта" lightbox="./media/versionlib.png"::: 
       Добавление `version.lib` в `ItemDefinitionGroups`  
    :::image-end:::  
    
    > [!NOTE]
    > Команда WebView2 стремится автоматизировать дополнительный этап зависимости в будущих выпусках.  
    
Скомпилируйте и разместите приложение.  Ошибкой.  

## См. также  

*   Чтобы приступить к работе с WebView2, перейдите в раздел [WebView2 начало работы][Webview2MainGettingStarted].  
*   Чтобы получить исчерпывающий пример возможностей WebView2, перейдите на [WebView2Samples][GithubMicrosoftedgeWebview2samples] в GitHub.
*   Более подробные сведения об API WebView2 можно найти в [справочнике по API][Webview2ApiReference].
*   Чтобы получить дополнительные сведения о WebView2, перейдите в раздел [ресурсы WebView2][Webview2MainNextSteps].

## Связь с командой WebView2  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../../devtools-guide-chromium.md "Инструменты разработчика Microsoft EDGE (Chromium) | Документы Microsoft"  

[Webview2ApiReference]: ../webview2-api-reference.md "Справочник по API Microsoft Edge WebView2 | Документы Microsoft"  
[Webview2MainNextSteps]: ../index.md#next-steps "Дальнейшие действия — введение в Microsoft Edge WebView2 (Предварительная версия) | Документы Microsoft"  
[Webview2MainGettingStarted]: ../index.md#getting-started "Приступая к работе: знакомство с Microsoft Edge WebView2 (Предварительная версия) | Документы Microsoft"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView Feedback-MicrosoftEdge/WebViewFeedback | GitHub"  
[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2 Samples-MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftVscodeJSDebugWhatsNew]: https://github.com/microsoft/vscode-js-debug#whats-new "Новые возможности -Отладчик JavaScript для Visual Studio Code-Microsoft/vscode-JS-Debug | GitHub"  

[GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications]: https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications "Microsoft EDGE (Chromium) WebView Applications-Debugger (код Visual Studio) — отладчик для Microsoft Edge-Microsoft/vscode-Edge-debug2 | GitHub"  
