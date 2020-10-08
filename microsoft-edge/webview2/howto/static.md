---
description: Сведения о том, как статическая связь библиотеки загрузчика WebView2.
title: Статическая связь библиотеки загрузчика WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/01/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: b7e0ec70cb00f318d4eb67254f37fcec79a5fcf6
ms.sourcegitcommit: 903524ab85321ade278facd741d6487e8cabe33f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/06/2020
ms.locfileid: "11100317"
---
# <span data-ttu-id="62960-104">Статическая связь библиотеки загрузчика WebView2</span><span class="sxs-lookup"><span data-stu-id="62960-104">How to Statically link the WebView2 loader library</span></span>  

## <span data-ttu-id="62960-105">Контекст</span><span class="sxs-lookup"><span data-stu-id="62960-105">Context</span></span>  

<span data-ttu-id="62960-106">Что такое WebView2Loader.dll?</span><span class="sxs-lookup"><span data-stu-id="62960-106">What is the WebView2Loader.dll?</span></span>  

*   <span data-ttu-id="62960-107">WebView2 SDK включает файл заголовка, `WebView2Loader.dll.` а также `IDL` файл.</span><span class="sxs-lookup"><span data-stu-id="62960-107">The WebView2 SDK contains a header file, `WebView2Loader.dll.`, and the `IDL` file.</span></span> `WebView2Loader.dll` <span data-ttu-id="62960-108">— Это небольшой компонент, который помогает приложениям найти на устройстве среду выполнения WebView2 (или нестабильные каналы Microsoft EDGE).</span><span class="sxs-lookup"><span data-stu-id="62960-108">is a small component that helps apps locate the WebView2 Runtime (or non-stable Microsoft Edge channels) on the device.</span></span>  

<span data-ttu-id="62960-109">Для приложений, которые имеют одну среду выполнения и не хотят отгрузить их `WebView2Loader.dll` , выполните **описанные** ниже действия.</span><span class="sxs-lookup"><span data-stu-id="62960-109">For apps that have a single runtime, and do not want to ship a `WebView2Loader.dll`, complete the following **Procedure** steps.</span></span>  

## <span data-ttu-id="62960-110">Процедура</span><span class="sxs-lookup"><span data-stu-id="62960-110">Procedure</span></span>  

1.  <span data-ttu-id="62960-111">Откройте `.vcxproj` файл проекта для вашего приложения в текстовом редакторе, например в коде Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="62960-111">Open the `.vcxproj` project file for your app in a text editor, such as Visual Studio Code.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="62960-112">`.vcproj`Файл проекта может быть скрытым файлом, что означает, что он не отображается в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="62960-112">The `.vcproj` project file may be a hidden file, meaning it does not display in Visual Studio.</span></span>  <span data-ttu-id="62960-113">Используйте командную строку для поиска скрытого файла.</span><span class="sxs-lookup"><span data-stu-id="62960-113">Use the command-line to find a hidden file.</span></span>  
    
1.  <span data-ttu-id="62960-114">Найдите раздел в коде, куда вы хотите добавить целевые файлы пакета NuGet WebView2.</span><span class="sxs-lookup"><span data-stu-id="62960-114">Locate the section in the code where you include the WebView2 NuGet package target files.</span></span>  <span data-ttu-id="62960-115">Место в коде выделено на рисунке ниже.</span><span class="sxs-lookup"><span data-stu-id="62960-115">The location in the code is highlighted in the following figure.</span></span>  
    
    :::image type="complex" source="./media/inserthere.png" alt-text="Фрагмент кода для файлов проекта" lightbox="./media/inserthere.png"::: 
       <span data-ttu-id="62960-117">Фрагмент кода для файлов проекта</span><span class="sxs-lookup"><span data-stu-id="62960-117">Project Files code snippet</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="62960-118">Скопируйте приведенный ниже фрагмент кода и вставьте его везде, где вы `Microsoft.Web.WebView2.targets` включены.</span><span class="sxs-lookup"><span data-stu-id="62960-118">Copy the following code snippet and paste it everywhere the `Microsoft.Web.WebView2.targets` is included.</span></span>  

    > [!NOTE]
    > <span data-ttu-id="62960-119">Например, включите его после следующего блока кода.</span><span class="sxs-lookup"><span data-stu-id="62960-119">For example, include it after the following code block.</span></span>  
    > 
    > ```csharp
    > <Import Project="..\packages\Microsoft.Web.WebView2.0.9.579-prerelease\build\native\Microsoft.Web.WebView2.targets" Condition="Exists('..\packages\Microsoft.Web.WebView2.0.9.579-prerelease\build\native\Microsoft.Web.WebView2.targets')" />
    > ```  
    
    ```csharp
    <PropertyGroup> <WebView2LoaderPreference>Static</WebView2LoaderPreference> </PropertyGroup>
    ```
    
    :::image type="complex" source="./media/staticlib.png" alt-text="Фрагмент кода для файлов проекта" lightbox="./media/staticlib.png"::: 
       <span data-ttu-id="62960-121">Вставлен фрагмент кода</span><span class="sxs-lookup"><span data-stu-id="62960-121">Inserted code snippet</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="62960-122">Измените дополнительные зависимости конфигурации сборки для вашего приложения.</span><span class="sxs-lookup"><span data-stu-id="62960-122">Edit the additional dependencies of the build configuration for your app.</span></span>  <span data-ttu-id="62960-123">Для начала найдите все `<AdditionalDependencies>` теги.</span><span class="sxs-lookup"><span data-stu-id="62960-123">To begin, find all of the `<AdditionalDependencies>` tags.</span></span>  
1.  <span data-ttu-id="62960-124">Добавьте в `version.lib` `.vcxproj` файл для вашего приложения дополнительные зависимости для каждой другой конфигурации сборки в файле.</span><span class="sxs-lookup"><span data-stu-id="62960-124">Add `version.lib` as an additional dependency to every different build configuration in the `.vcxproj` file for your app.</span></span>  
    
    :::image type="complex" source="./media/versionlib.png" alt-text="Фрагмент кода для файлов проекта" lightbox="./media/versionlib.png"::: 
       <span data-ttu-id="62960-126">Добавление `version.lib` в</span><span class="sxs-lookup"><span data-stu-id="62960-126">Adding `version.lib` to</span></span> `ItemDefinitionGroups`  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="62960-127">Команда WebView2 стремится автоматизировать дополнительный этап зависимости в будущих выпусках.</span><span class="sxs-lookup"><span data-stu-id="62960-127">The WebView2 team aims to automate the additional dependency step in future releases.</span></span>  
    
<span data-ttu-id="62960-128">Скомпилируйте и разместите приложение.</span><span class="sxs-lookup"><span data-stu-id="62960-128">Compile and deploy your app.</span></span>  <span data-ttu-id="62960-129">Ошибкой.</span><span class="sxs-lookup"><span data-stu-id="62960-129">Success.</span></span>  

## <span data-ttu-id="62960-130">См. также</span><span class="sxs-lookup"><span data-stu-id="62960-130">See also</span></span>  

*   <span data-ttu-id="62960-131">Чтобы приступить к работе с WebView2, перейдите в раздел [WebView2 начало работы][Webview2MainGettingStarted].</span><span class="sxs-lookup"><span data-stu-id="62960-131">To get started using WebView2, navigate to [WebView2 Getting Started Guides][Webview2MainGettingStarted].</span></span>  
*   <span data-ttu-id="62960-132">Чтобы получить исчерпывающий пример возможностей WebView2, перейдите на [WebView2Samples][GithubMicrosoftedgeWebview2samples] в GitHub.</span><span class="sxs-lookup"><span data-stu-id="62960-132">For a comprehensive example of WebView2 capabilities, navigate to [WebView2Samples][GithubMicrosoftedgeWebview2samples] on GitHub.</span></span>
*   <span data-ttu-id="62960-133">Более подробные сведения об API WebView2 можно найти в [справочнике по API][Webview2ApiReference].</span><span class="sxs-lookup"><span data-stu-id="62960-133">For more detailed information about WebView2 APIs, navigate to [API reference][Webview2ApiReference].</span></span>
*   <span data-ttu-id="62960-134">Чтобы получить дополнительные сведения о WebView2, перейдите в раздел [ресурсы WebView2][Webview2MainNextSteps].</span><span class="sxs-lookup"><span data-stu-id="62960-134">For more information about WebView2, navigate to [WebView2 Resources][Webview2MainNextSteps].</span></span>

## <span data-ttu-id="62960-135">Связь с командой WebView2</span><span class="sxs-lookup"><span data-stu-id="62960-135">Getting in touch with the WebView2 team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../../devtools-guide-chromium.md "Инструменты разработчика Microsoft EDGE (Chromium) | Документы Microsoft"  

[Webview2ReferenceDotnet09628MicrosoftWebWebview2CoreCorewebview2environmentoptionsAdditionalbrowserarguments]: ../reference/dotnet/0-9-628/microsoft-web-webview2-core-corewebview2environmentoptions.md#additionalbrowserarguments "Класс AdditionalBrowserArguments-0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2EnvironmentOptions | Документы Microsoft"  
[Webview2ReferenceWin3209622Webview2IdlParameters]: ../reference/win32/0-9-622/webview2-idl.md#createcorewebview2environment  "CreateCoreWebView2Environment-Globals | Документы Microsoft"  
[Webview2ApiReference]: ../webview2-api-reference.md "Справочник по API Microsoft Edge WebView2 | Документы Microsoft"  
[Webview2MainNextSteps]: ../index.md#next-steps "Дальнейшие действия — введение в Microsoft Edge WebView2 (Предварительная версия) | Документы Microsoft"  
[Webview2MainGettingStarted]: ../index.md#getting-started "Приступая к работе: знакомство с Microsoft Edge WebView2 (Предварительная версия) | Документы Microsoft"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView Feedback-MicrosoftEdge/WebViewFeedback | GitHub"  
[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2 Samples-MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftVscodeJSDebugWhatsNew]: https://github.com/microsoft/vscode-js-debug#whats-new "Новые возможности -Отладчик JavaScript для Visual Studio Code-Microsoft/vscode-JS-Debug | GitHub"  

[GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications]: https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications "Microsoft EDGE (Chromium) WebView Applications-Debugger (код Visual Studio) — отладчик для Microsoft Edge-Microsoft/vscode-Edge-debug2 | GitHub"  
