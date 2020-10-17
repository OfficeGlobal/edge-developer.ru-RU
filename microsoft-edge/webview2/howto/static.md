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
# <span data-ttu-id="c1dc8-104">Статическая связь с библиотекой загрузчика WebView2</span><span class="sxs-lookup"><span data-stu-id="c1dc8-104">Statically link the WebView2 loader library</span></span>  

<span data-ttu-id="c1dc8-105">Возможно, вы захотите распространить приложение с помощью одного исполняемого файла, а не из множества файлов.</span><span class="sxs-lookup"><span data-stu-id="c1dc8-105">You may want to distribute your application with a single executable file, instead of a package of many files.</span></span> <span data-ttu-id="c1dc8-106">Чтобы создать один исполняемый файл или уменьшить размер пакета, необходимо статически связать WebView2Loader-файлы.</span><span class="sxs-lookup"><span data-stu-id="c1dc8-106">To create a single executable file, or to reduce the size of your package, you should statically link the WebView2Loader files.</span></span> <span data-ttu-id="c1dc8-107">WebView2 SDK включает файл заголовка, `WebView2Loader.dll` а также `IDL` файл.</span><span class="sxs-lookup"><span data-stu-id="c1dc8-107">The WebView2 SDK contains a header file, `WebView2Loader.dll`, and the `IDL` file.</span></span> `WebView2Loader.dll` <span data-ttu-id="c1dc8-108">— Это небольшой компонент, который помогает приложениям найти на устройстве среду выполнения WebView2 или нестабильные каналы Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c1dc8-108">is a small component that helps apps locate the WebView2 Runtime, or non-stable channels of Microsoft Edge, on the device.</span></span>  

<span data-ttu-id="c1dc8-109">Для приложений, для которых не требуется отгрузка `WebView2Loader.dll` , выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="c1dc8-109">For apps that don't want to ship a `WebView2Loader.dll`, complete the following steps.</span></span>  

1.  <span data-ttu-id="c1dc8-110">Откройте `.vcxproj` файл проекта для вашего приложения в текстовом редакторе, например в коде Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="c1dc8-110">Open the `.vcxproj` project file for your app in a text editor, such as Visual Studio Code.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="c1dc8-111">`.vcproj`Файл проекта может быть скрытым файлом, что означает, что он не отображается в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="c1dc8-111">The `.vcproj` project file may be a hidden file, meaning it does not display in Visual Studio.</span></span>  <span data-ttu-id="c1dc8-112">Используйте командную строку для поиска скрытых файлов.</span><span class="sxs-lookup"><span data-stu-id="c1dc8-112">Use the command-line to find hidden files.</span></span>  
    
1.  <span data-ttu-id="c1dc8-113">Найдите раздел в коде, куда вы хотите добавить целевые файлы пакета NuGet WebView2.</span><span class="sxs-lookup"><span data-stu-id="c1dc8-113">Locate the section in the code where you include the WebView2 NuGet package target files.</span></span>  <span data-ttu-id="c1dc8-114">Место в коде выделено на рисунке ниже.</span><span class="sxs-lookup"><span data-stu-id="c1dc8-114">The location in the code is highlighted in the following figure.</span></span>  

    :::image type="complex" source="./media/inserthere.png" alt-text="Фрагмент кода для файлов проекта" lightbox="./media/inserthere.png":::
       <span data-ttu-id="c1dc8-116">Фрагмент кода для файлов проекта</span><span class="sxs-lookup"><span data-stu-id="c1dc8-116">Project Files code snippet</span></span>   
    :::image-end:::  
  
1.  <span data-ttu-id="c1dc8-117">Скопируйте приведенный ниже фрагмент кода и вставьте его в том месте, где он `Microsoft.Web.WebView2.targets` включен.</span><span class="sxs-lookup"><span data-stu-id="c1dc8-117">Copy the following code snippet and paste it where the `Microsoft.Web.WebView2.targets` is included.</span></span>  

    ```xaml
    <PropertyGroup> 
        <WebView2LoaderPreference>Static</WebView2LoaderPreference> 
    </PropertyGroup>
    ```
      
    :::image type="complex" source="./media/staticlib.png" alt-text="Фрагмент кода для файлов проекта" lightbox="./media/staticlib.png":::
       <span data-ttu-id="c1dc8-119">Вставлен фрагмент кода</span><span class="sxs-lookup"><span data-stu-id="c1dc8-119">Inserted code snippet</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c1dc8-120">Измените дополнительные зависимости конфигурации сборки для вашего приложения.</span><span class="sxs-lookup"><span data-stu-id="c1dc8-120">Edit the additional dependencies of the build configuration for your app.</span></span>  <span data-ttu-id="c1dc8-121">Для начала найдите все `<AdditionalDependencies>` теги.</span><span class="sxs-lookup"><span data-stu-id="c1dc8-121">To begin, find all of the `<AdditionalDependencies>` tags.</span></span> <span data-ttu-id="c1dc8-122">Каждый из них добавляется `version.lib` как дополнительная зависимость к каждой конфигурации сборки в `.vcxproj` файле.</span><span class="sxs-lookup"><span data-stu-id="c1dc8-122">For each, add `version.lib` as an additional dependency to every different build configuration in the `.vcxproj` file.</span></span>  
    
    :::image type="complex" source="./media/versionlib.png" alt-text="Фрагмент кода для файлов проекта" lightbox="./media/versionlib.png":::
       <span data-ttu-id="c1dc8-124">Добавление `version.lib` в</span><span class="sxs-lookup"><span data-stu-id="c1dc8-124">Adding `version.lib` to</span></span> `ItemDefinitionGroups`  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="c1dc8-125">Команда WebView2 стремится автоматизировать добавление дополнительной зависимости в будущих выпусках.</span><span class="sxs-lookup"><span data-stu-id="c1dc8-125">The WebView2 team aims to automate adding the additional dependency in future releases.</span></span>  
    
1. <span data-ttu-id="c1dc8-126">Скомпилируйте и запустите приложение.</span><span class="sxs-lookup"><span data-stu-id="c1dc8-126">Compile and run your app.</span></span>

### <span data-ttu-id="c1dc8-127">Связь с командой WebView2</span><span class="sxs-lookup"><span data-stu-id="c1dc8-127">Getting in touch with the WebView2 team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

### <span data-ttu-id="c1dc8-128">См. также</span><span class="sxs-lookup"><span data-stu-id="c1dc8-128">See also</span></span>  

*   <span data-ttu-id="c1dc8-129">Чтобы приступить к работе с WebView2, перейдите в раздел [WebView2 начало работы][Webview2MainGettingStarted].</span><span class="sxs-lookup"><span data-stu-id="c1dc8-129">To get started using WebView2, navigate to [WebView2 Getting Started Guides][Webview2MainGettingStarted].</span></span>  
*   <span data-ttu-id="c1dc8-130">Чтобы получить исчерпывающий пример возможностей WebView2, перейдите на [WebView2Samples][GithubMicrosoftedgeWebview2samples] в GitHub.</span><span class="sxs-lookup"><span data-stu-id="c1dc8-130">For a comprehensive example of WebView2 capabilities, navigate to [WebView2Samples][GithubMicrosoftedgeWebview2samples] on GitHub.</span></span>
*   <span data-ttu-id="c1dc8-131">Более подробные сведения об API WebView2 можно найти в [справочнике по API][Webview2ApiReference].</span><span class="sxs-lookup"><span data-stu-id="c1dc8-131">For more detailed information about WebView2 APIs, navigate to [API reference][Webview2ApiReference].</span></span>
*   <span data-ttu-id="c1dc8-132">Чтобы получить дополнительные сведения о WebView2, перейдите в раздел [ресурсы WebView2][Webview2MainNextSteps].</span><span class="sxs-lookup"><span data-stu-id="c1dc8-132">For more information about WebView2, navigate to [WebView2 Resources][Webview2MainNextSteps].</span></span>

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../../devtools-guide-chromium.md "Инструменты разработчика Microsoft EDGE (Chromium) | Документы Microsoft"  

[Webview2ApiReference]: ../webview2-api-reference.md "Справочник по API Microsoft Edge WebView2 | Документы Microsoft"  
[Webview2MainNextSteps]: ../index.md#next-steps "Дальнейшие действия — введение в Microsoft Edge WebView2 (Предварительная версия) | Документы Microsoft"  
[Webview2MainGettingStarted]: ../index.md#getting-started "Приступая к работе: знакомство с Microsoft Edge WebView2 (Предварительная версия) | Документы Microsoft"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView Feedback-MicrosoftEdge/WebViewFeedback | GitHub"  
[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2 Samples-MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftVscodeJSDebugWhatsNew]: https://github.com/microsoft/vscode-js-debug#whats-new "Новые возможности -Отладчик JavaScript для Visual Studio Code-Microsoft/vscode-JS-Debug | GitHub"  

[GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications]: https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications "Microsoft EDGE (Chromium) WebView Applications-Debugger (код Visual Studio) — отладчик для Microsoft Edge-Microsoft/vscode-Edge-debug2 | GitHub"  
