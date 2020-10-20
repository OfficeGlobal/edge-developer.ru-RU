---
description: Руководство по началу работы с WebView2 для приложений Win32
title: Приступая к работе с WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 20d830e2c8b95213b223da46f9afd9f69a137946
ms.sourcegitcommit: af91bfc3e6d8afc51f0fbbc0fe392262f424225c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/19/2020
ms.locfileid: "11120384"
---
# <span data-ttu-id="80e14-104">Начало работы с WebView2</span><span class="sxs-lookup"><span data-stu-id="80e14-104">Getting started with WebView2</span></span>  

<span data-ttu-id="80e14-105">Приведенное ниже содержимое познакомит вас с помощью часто используемых функций [WebView2][Webview2Index] и предоставляет отправную точку для создания первого приложения WebView2.</span><span class="sxs-lookup"><span data-stu-id="80e14-105">The following content walks you through the commonly used functionalities of [WebView2][Webview2Index] and provides a starting point for creating your first WebView2 app.</span></span>  <span data-ttu-id="80e14-106">Дополнительные сведения об индивидуальных API WebView2 можно найти в [справочнике API][Webview2ReferenceWin32].</span><span class="sxs-lookup"><span data-stu-id="80e14-106">For more information about individual WebView2 APIs, see [API reference][Webview2ReferenceWin32].</span></span>  

## <span data-ttu-id="80e14-107">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="80e14-107">Prerequisites</span></span>  

*   <span data-ttu-id="80e14-108">[WebView2][Webview2Installer] или любой [Microsoft EDGE (Chromium), который не является стабильным каналом][MicrosoftedgeinsiderDownload] , установленным в поддерживаемой ОС \ (в настоящее время windows 10, Windows 8,1 и Windows 7).</span><span class="sxs-lookup"><span data-stu-id="80e14-108">[WebView2 Runtime][Webview2Installer] or any [Microsoft Edge (Chromium) non-stable channel][MicrosoftedgeinsiderDownload] installed on supported OS \(currently Windows 10, Windows 8.1, and Windows 7\).</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="80e14-109">Группа WebView рекомендует использовать канал Канарские и минимальную требуемую версию — 82.0.488.0.</span><span class="sxs-lookup"><span data-stu-id="80e14-109">The WebView team recommends using the Canary channel and the minimum required version is 82.0.488.0.</span></span>  
    
*   <span data-ttu-id="80e14-110">[Visual Studio][MicrosoftVisualstudioMain] 2015 или более поздней версии с установленной поддержкой C++.</span><span class="sxs-lookup"><span data-stu-id="80e14-110">[Visual Studio][MicrosoftVisualstudioMain] 2015 or later with C++ support installed.</span></span>  

## <span data-ttu-id="80e14-111">Шаг 1: создание приложения Win32 с одним окном</span><span class="sxs-lookup"><span data-stu-id="80e14-111">Step 1 - Create a single-window win32 app</span></span>  

<span data-ttu-id="80e14-112">Начните с базового проекта для настольных компьютеров, содержащего одно главное окно.</span><span class="sxs-lookup"><span data-stu-id="80e14-112">Start with a basic desktop project that contains a single main window.</span></span>  <span data-ttu-id="80e14-113">Чтобы лучше сосредоточиться на пошаговом руководстве, вы используете модифицированный образец кода из [пошагового руководства: создание традиционного классического приложения для Windows (C++)][CppWindowsWalkthroughCreatingDesktopApplication] для примера приложения.</span><span class="sxs-lookup"><span data-stu-id="80e14-113">To better focus the walkthrough, you are using modified sample code from [Walkthrough: Create a traditional Windows Desktop application (C++)][CppWindowsWalkthroughCreatingDesktopApplication] for your sample app.</span></span>  <span data-ttu-id="80e14-114">Чтобы загрузить модифицированный образец и начать работу, перейдите в [WebView2 Samples][GithubMicrosoftedgeWebview2samplesGettingStartedGuide].</span><span class="sxs-lookup"><span data-stu-id="80e14-114">To download the modified sample and get started, navigate to [WebView2 Samples][GithubMicrosoftedgeWebview2samplesGettingStartedGuide].</span></span>  

<span data-ttu-id="80e14-115">В Visual Studio откройте `WebView2GettingStarted.sln` .</span><span class="sxs-lookup"><span data-stu-id="80e14-115">In Visual Studio, open `WebView2GettingStarted.sln`.</span></span>  <span data-ttu-id="80e14-116">Если вы используете более старую версию Visual Studio, наведите указатель мыши на проект **WebView2GettingStarted** , откройте контекстное меню (щелкните правой кнопкой мыши \) и выберите пункт **свойства**.</span><span class="sxs-lookup"><span data-stu-id="80e14-116">If you are using an older version of Visual Studio, hover on the **WebView2GettingStarted** project, open the contextual menu \(right-click\), and select **Properties**.</span></span>  <span data-ttu-id="80e14-117">В разделе **Свойства конфигурации**  >  **Общие**измените **версию Windows SDK** и **набор инструментов платформы** , чтобы использовать пакет SDK Win10 и Visual Studio Tools \ (набор инструментов VS).</span><span class="sxs-lookup"><span data-stu-id="80e14-117">Under **Configuration Properties** > **General**, modify **Windows SDK Version** and **Platform Toolset** to use the Win10 SDK and Visual Studio toolset \(VS toolset\) available to you.</span></span>  

:::image type="complex" source="../media/tool-version.png" alt-text="Версия инструмента" lightbox="../media/tool-version.png":::
   <span data-ttu-id="80e14-119">Версия инструмента</span><span class="sxs-lookup"><span data-stu-id="80e14-119">Tool version</span></span>  
:::image-end:::  

<span data-ttu-id="80e14-120">Visual Studio может показывать некоторые ошибки из-за отсутствующего файла заголовка WebView2, который должен выйти после завершения действия 2.</span><span class="sxs-lookup"><span data-stu-id="80e14-120">Visual Studio may show some errors because of the missing WebView2 header file, which should go away after Step 2 is completed.</span></span>  

## <span data-ttu-id="80e14-121">Шаг 2. Установка WebView2 SDK</span><span class="sxs-lookup"><span data-stu-id="80e14-121">Step 2 - Install WebView2 SDK</span></span>  

<span data-ttu-id="80e14-122">Добавьте в проект WebView2 SDK.</span><span class="sxs-lookup"><span data-stu-id="80e14-122">Add the WebView2 SDK into the project.</span></span>  <span data-ttu-id="80e14-123">Вы можете установить пакет SDK для Win32 с помощью NuGet.</span><span class="sxs-lookup"><span data-stu-id="80e14-123">You may install the Win32 SDK using NuGet.</span></span>  

1.  <span data-ttu-id="80e14-124">Наведите указатель мыши на проект, откройте контекстное меню (щелкните правой кнопкой мыши \) и выберите пункт **Управление пакетами NuGet**.</span><span class="sxs-lookup"><span data-stu-id="80e14-124">Hover on the project, open the contextual menu \(right-click\), and select **Manage NuGet Packages**.</span></span>  
    
    :::image type="complex" source="../media/manage-nuget-packages.png" alt-text="Версия инструмента" lightbox="../media/manage-nuget-packages.png":::
       <span data-ttu-id="80e14-126">Управление пакетами NuGet</span><span class="sxs-lookup"><span data-stu-id="80e14-126">Manage NuGet packages</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="80e14-127">Установите библиотеку реализации Windows.</span><span class="sxs-lookup"><span data-stu-id="80e14-127">Install the Windows Implementation Library.</span></span>  
    1.  <span data-ttu-id="80e14-128">Введите `Microsoft.Windows.ImplementationLibrary` в строке поиска параметр **Microsoft. Windows. ImplementationLibrary** и выберите пункт **установить** в правой части окна.</span><span class="sxs-lookup"><span data-stu-id="80e14-128">Enter `Microsoft.Windows.ImplementationLibrary` in the search bar, select **Microsoft.Windows.ImplementationLibrary** from the results, and select **Install** in the right-hand side window.</span></span>  <span data-ttu-id="80e14-129">NuGet загрузит пакет SDK на ваш компьютер.</span><span class="sxs-lookup"><span data-stu-id="80e14-129">NuGet downloads the SDK to your machine.</span></span>  
        
        > [!NOTE] 
        > <span data-ttu-id="80e14-130">Библиотека [реализации Windows][GithubMicrosoftWilMain] и [Библиотека шаблонов C++ среды выполнения Windows][CppCxWrlTemplateLibraryVS2019] являются необязательными и добавлены для УПРОЩЕНия работы с COM в этом примере.</span><span class="sxs-lookup"><span data-stu-id="80e14-130">The [Windows Implementation Library][GithubMicrosoftWilMain] and [Windows Runtime C++ Template Library][CppCxWrlTemplateLibraryVS2019] are optional and were added to make working with COM easier for the example.</span></span>  
        
        :::image type="complex" source="../media/wil.png" alt-text="Версия инструмента" lightbox="../media/wil.png":::
           <span data-ttu-id="80e14-132">Библиотека реализации Windows</span><span class="sxs-lookup"><span data-stu-id="80e14-132">Windows Implementation Library</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="80e14-133">Установите пакет SDK для WebView2.</span><span class="sxs-lookup"><span data-stu-id="80e14-133">Install the WebView2 SDK.</span></span>  
    1.  <span data-ttu-id="80e14-134">Введите `Microsoft.Web.WebView2` в строке поиска параметр **Microsoft. Web. WebView2** и выберите пункт **установить** в правой части окна.</span><span class="sxs-lookup"><span data-stu-id="80e14-134">Enter `Microsoft.Web.WebView2` in the search bar, select **Microsoft.Web.WebView2** from the results, and select **Install** in the right-hand side window.</span></span>  <span data-ttu-id="80e14-135">NuGet загрузит пакет SDK на ваш компьютер.</span><span class="sxs-lookup"><span data-stu-id="80e14-135">NuGet downloads the SDK to your machine.</span></span>  
        
        :::image type="complex" source="../media/nuget.png" alt-text="Версия инструмента" lightbox="../media/nuget.png":::
           <span data-ttu-id="80e14-137">Диспетчер пакетов NuGet</span><span class="sxs-lookup"><span data-stu-id="80e14-137">Nuget Package Manager</span></span>
        :::image-end:::  
        
1.  <span data-ttu-id="80e14-138">Добавьте в проект заголовок WebView2.</span><span class="sxs-lookup"><span data-stu-id="80e14-138">Add WebView2 header to your project.</span></span>  
    :::row:::
       :::column span="1":::
          <span data-ttu-id="80e14-139">`HelloWebView.cpp`Скопируйте приведенный ниже фрагмент кода и вставьте его `HelloWebView.cpp` после последней `#include` строки.</span><span class="sxs-lookup"><span data-stu-id="80e14-139">Open `HelloWebView.cpp`, copy the following code snippet and paste into `HelloWebView.cpp` after last `#include` line.</span></span>  
          
          ```cpp
          // include WebView2 header
          #include "WebView2.h"
          ```  
       :::column-end:::
       :::column span="1":::
          <span data-ttu-id="80e14-140">Раздел включения должен выглядеть так, как показано в следующем фрагменте кода.</span><span class="sxs-lookup"><span data-stu-id="80e14-140">The include section should look similar to the following code snippet.</span></span>  
          
          ```cpp
          ...
          #include <wrl.h>
          #include <wil/com.h>
          // include WebView2 header
          #include "WebView2.h"
          ```  
       :::column-end:::
    :::row-end:::
    
<span data-ttu-id="80e14-141">Все готово для использования и сборки в API WebView2.</span><span class="sxs-lookup"><span data-stu-id="80e14-141">You are all set to use and build against the WebView2 API.</span></span>  

### <span data-ttu-id="80e14-142">Создание пустого примера приложения</span><span class="sxs-lookup"><span data-stu-id="80e14-142">Build your empty sample app</span></span>  

<span data-ttu-id="80e14-143">Выберите `F5` для сборки и запуска примера приложения.</span><span class="sxs-lookup"><span data-stu-id="80e14-143">Select `F5` to build and run the sample app.</span></span>  <span data-ttu-id="80e14-144">Откроется пустое окно приложения.</span><span class="sxs-lookup"><span data-stu-id="80e14-144">An app displaying an empty window appears.</span></span>  

:::image type="complex" source="../media/empty-app.png" alt-text="Версия инструмента" lightbox="../media/empty-app.png":::
   <span data-ttu-id="80e14-146">Пустое приложение</span><span class="sxs-lookup"><span data-stu-id="80e14-146">Empty app</span></span>  
:::image-end:::  

## <span data-ttu-id="80e14-147">Шаг 3: создание единого WebView в родительском окне</span><span class="sxs-lookup"><span data-stu-id="80e14-147">Step 3 - Create a single WebView within the parent window</span></span>  

<span data-ttu-id="80e14-148">Добавьте WebView в главное окно.</span><span class="sxs-lookup"><span data-stu-id="80e14-148">Add a WebView to the main window.</span></span>  <span data-ttu-id="80e14-149">Используйте этот `CreateCoreWebView2Environment` метод для настройки среды и поиска в браузере Microsoft Edge \ (Chromium \) включения и выключения элемента управления.</span><span class="sxs-lookup"><span data-stu-id="80e14-149">Use the `CreateCoreWebView2Environment` method to set up the environment and locate the Microsoft Edge \(Chromium\) browser powering the control.</span></span>  <span data-ttu-id="80e14-150">Кроме того, вы можете использовать этот `CreateCoreWebView2EnvironmentWithOptions` метод, если вы хотите указать расположение браузера, папку пользователя, флаги браузера и т. д., вместо использования параметра по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="80e14-150">You may also use the `CreateCoreWebView2EnvironmentWithOptions` method if you want to specify browser location, user folder, browser flags, and so on, instead of using the default setting.</span></span>  <span data-ttu-id="80e14-151">После завершения `CreateCoreWebView2Environment` метода вы можете выполнить `ICoreWebView2Environment::CreateCoreWebView2Controller` метод в `ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler` обратном вызове и выполнить `ICoreWebView2Controller::get_CoreWebView2` метод для получения связанного WebView.</span><span class="sxs-lookup"><span data-stu-id="80e14-151">Upon the completion of the `CreateCoreWebView2Environment` method, you are able to run the `ICoreWebView2Environment::CreateCoreWebView2Controller` method inside the `ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler` callback and run the `ICoreWebView2Controller::get_CoreWebView2` method to get the associated WebView.</span></span>  

<span data-ttu-id="80e14-152">В обратном вызове задайте несколько дополнительных параметров, измените размер WebView, чтобы получить 100% родительского окна, и перейдите в Bing.</span><span class="sxs-lookup"><span data-stu-id="80e14-152">In the callback, set a few additional settings, resize the WebView to take 100% of the parent window, and navigate to Bing.</span></span>  

<span data-ttu-id="80e14-153">Скопируйте приведенный ниже фрагмент кода и вставьте `HelloWebView.cpp` его после `// <-- WebView2 sample code starts here -->` заметки и перед `// <-- WebView2 sample code ends here -->` заметкой.</span><span class="sxs-lookup"><span data-stu-id="80e14-153">Copy the following code snippet and paste into `HelloWebView.cpp` after the `// <-- WebView2 sample code starts here -->` note and before the `// <-- WebView2 sample code ends here -->` note.</span></span>  

```cpp
// Step 3 - Create a single WebView within the parent window
// Locate the browser and set up the environment for WebView
CreateCoreWebView2EnvironmentWithOptions(nullptr, nullptr, nullptr,
    Callback<ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler>(
        [hWnd](HRESULT result, ICoreWebView2Environment* env) -> HRESULT {
        
            // Create a CoreWebView2Controller and get the associated CoreWebView2 whose parent is the main window hWnd
            env->CreateCoreWebView2Controller(hWnd, Callback<ICoreWebView2CreateCoreWebView2ControllerCompletedHandler>(
                [hWnd](HRESULT result, ICoreWebView2Controller* controller) -> HRESULT {
                if (controller != nullptr) {
                    webviewController = controller;
                    webviewController->get_CoreWebView2(&webviewWindow);
                }
                
                // Add a few settings for the webview
                // The demo step is redundant since the values are the default settings
                ICoreWebView2Settings* Settings;
                webviewWindow->get_Settings(&Settings);
                Settings->put_IsScriptEnabled(TRUE);
                Settings->put_AreDefaultScriptDialogsEnabled(TRUE);
                Settings->put_IsWebMessageEnabled(TRUE);
                
                // Resize WebView to fit the bounds of the parent window
                RECT bounds;
                GetClientRect(hWnd, &bounds);
                webviewController->put_Bounds(bounds);
                
                // Schedule an async task to navigate to Bing
                webviewWindow->Navigate(L"https://www.bing.com/");
                
                // Step 4 - Navigation events
                
                // Step 5 - Scripting
                
                // Step 6 - Communication between host and web content
                
                return S_OK;
            }).Get());
        return S_OK;
    }).Get());
```  

### <span data-ttu-id="80e14-154">Создание примера приложения Bing</span><span class="sxs-lookup"><span data-stu-id="80e14-154">Build your Bing sample app</span></span>  

<span data-ttu-id="80e14-155">Выберите `F5` , чтобы выполнить сборку и запустить приложение.</span><span class="sxs-lookup"><span data-stu-id="80e14-155">Select `F5` to build and run the app.</span></span>  <span data-ttu-id="80e14-156">Теперь у вас есть окно WebView, в котором отображается страница Bing.</span><span class="sxs-lookup"><span data-stu-id="80e14-156">Now you have a WebView window displaying the Bing page.</span></span>  

:::image type="complex" source="../media/bing-window.png" alt-text="Версия инструмента" lightbox="../media/bing-window.png":::
   <span data-ttu-id="80e14-158">Окно Bing</span><span class="sxs-lookup"><span data-stu-id="80e14-158">Bing window</span></span>  
:::image-end:::  

## <span data-ttu-id="80e14-159">Шаг 4 — события навигации</span><span class="sxs-lookup"><span data-stu-id="80e14-159">Step 4 - Navigation events</span></span>  

<span data-ttu-id="80e14-160">Команда WebView уже покрыла навигацию по URL-адресу, используя `ICoreWebView2::Navigate` метод на последнем этапе.</span><span class="sxs-lookup"><span data-stu-id="80e14-160">The WebView team already covered navigating to URL using the `ICoreWebView2::Navigate` method in the last step.</span></span>  <span data-ttu-id="80e14-161">Во время навигации WebView инициирует последовательность событий, для которых узел может прослушаться.</span><span class="sxs-lookup"><span data-stu-id="80e14-161">During navigation, WebView fires a sequence of events to which the host may listen.</span></span>  

1.  `NavigationStarting`  
1.  `SourceChanged`  
1.  `ContentLoading`  
1.  `HistoryChanged`   
1.  `NavigationCompleted`   

<span data-ttu-id="80e14-162">Дополнительные сведения можно найти в разделе [события навигации][Webview2ConceptsNavigationEvents].</span><span class="sxs-lookup"><span data-stu-id="80e14-162">For more information, navigate to [Navigation events][Webview2ConceptsNavigationEvents].</span></span>  

:::image type="complex" source="../media/navigation-events.png" alt-text="Версия инструмента" lightbox="../media/navigation-events.png":::
   <span data-ttu-id="80e14-164">События навигации</span><span class="sxs-lookup"><span data-stu-id="80e14-164">Navigation events</span></span>  
:::image-end:::  

<span data-ttu-id="80e14-165">В случае ошибок может возникнуть одно или несколько из указанных ниже событий в зависимости от того, проявляется ли переход на страницу ошибки.</span><span class="sxs-lookup"><span data-stu-id="80e14-165">In error cases, one or more of the following events may occur depending on whether the navigation is continued to an error page.</span></span>  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`

<span data-ttu-id="80e14-166">Если возникает Переадресация HTTP, `NavigationStarting` в строке есть несколько событий.</span><span class="sxs-lookup"><span data-stu-id="80e14-166">If an HTTP redirect occurs, there are multiple `NavigationStarting` events in a row.</span></span>  

<span data-ttu-id="80e14-167">В качестве примера использования событий Зарегистрируйте обработчик для `NavigationStarting` события, чтобы отменить любые запросы, не относящиеся к HTTPS.</span><span class="sxs-lookup"><span data-stu-id="80e14-167">As an example of using the events, register a handler for the `NavigationStarting` event to cancel any non-https requests.</span></span>  <span data-ttu-id="80e14-168">Скопируйте приведенный ниже фрагмент кода и вставьте его в `HelloWebView.cpp` .</span><span class="sxs-lookup"><span data-stu-id="80e14-168">Copy the following code snippet and paste into `HelloWebView.cpp`.</span></span>  

```cpp
// register an ICoreWebView2NavigationStartingEventHandler to cancel any non-https navigation
EventRegistrationToken token;
webviewWindow->add_NavigationStarting(Callback<ICoreWebView2NavigationStartingEventHandler>(
    [](ICoreWebView2* webview, ICoreWebView2NavigationStartingEventArgs * args) -> HRESULT {
        PWSTR uri;
        args->get_Uri(&uri);
        std::wstring source(uri);
        if (source.substr(0, 5) != L"https") {
            args->put_Cancel(true);
        }
        CoTaskMemFree(uri);
        return S_OK;
    }).Get(), &token);
```  

<span data-ttu-id="80e14-169">Теперь приложение не будет перемещаться на сайты, не поддерживающие HTTPS.</span><span class="sxs-lookup"><span data-stu-id="80e14-169">Now the app is not navigating to any non-https sites.</span></span>  <span data-ttu-id="80e14-170">Вы можете использовать сходный механизм для выполнения других задач, например для ограничения навигации в рамках собственного домена.</span><span class="sxs-lookup"><span data-stu-id="80e14-170">You may use similar mechanism to accomplish other tasks, such as restricting navigation to within your own domain.</span></span>  

## <span data-ttu-id="80e14-171">Шаг 5: создание сценариев</span><span class="sxs-lookup"><span data-stu-id="80e14-171">Step 5 - Scripting</span></span>  

<span data-ttu-id="80e14-172">Ведущее приложение может также внедрить JavaScript в WebView.</span><span class="sxs-lookup"><span data-stu-id="80e14-172">The hosting app may also inject JavaScript into WebView.</span></span>  <span data-ttu-id="80e14-173">Вы можете WebView задачу, чтобы запустить произвольный сценарий JavaScript или добавить сценарии инициализации.</span><span class="sxs-lookup"><span data-stu-id="80e14-173">You may task WebView to run arbitrary JavaScript or add initialization scripts.</span></span>  <span data-ttu-id="80e14-174">Добавленные сценарии инициализации применяются ко всем будущим документам верхнего уровня и дочерним элементам навигации, пока они не будут удалены.</span><span class="sxs-lookup"><span data-stu-id="80e14-174">Added initialization scripts apply to all future top-level document and child frame navigation until removed.</span></span>  <span data-ttu-id="80e14-175">Сценарии инициализации выполняются после создания глобального объекта и выполнения любого другого сценария, включенного в документ HTML.</span><span class="sxs-lookup"><span data-stu-id="80e14-175">The initialization scripts run after creating the global object and before running any other script included by the HTML document.</span></span>  

<span data-ttu-id="80e14-176">Скопируйте приведенный ниже фрагмент кода и вставьте его в `HelloWebView.cpp` .</span><span class="sxs-lookup"><span data-stu-id="80e14-176">Copy the following code snippet and paste into `HelloWebView.cpp`.</span></span>  

```cpp
// Schedule an async task to add initialization script that freezes the Object object
webviewWindow->AddScriptToExecuteOnDocumentCreated(L"Object.freeze(Object);", nullptr);
// Schedule an async task to get the document URL
webviewWindow->ExecuteScript(L"window.document.URL;", Callback<ICoreWebView2ExecuteScriptCompletedHandler>(
    [](HRESULT errorCode, LPCWSTR resultObjectAsJson) -> HRESULT {
        LPCWSTR URL = resultObjectAsJson;
        //doSomethingWithURL(URL);
        return S_OK;
    }).Get());
```  

<span data-ttu-id="80e14-177">Теперь WebView должен всегда закреплять `Object` объект и возвращать документ страницы один раз.</span><span class="sxs-lookup"><span data-stu-id="80e14-177">Now, WebView should always freeze the `Object` object and returns the page document once.</span></span>  

> [!NOTE] 
> <span data-ttu-id="80e14-178">API внедрения сценария \ (и некоторые другие API WebView2 \) являются асинхронными, следует использовать обратные вызовы, если код должен выполняться в определенном порядке.</span><span class="sxs-lookup"><span data-stu-id="80e14-178">The script injection APIs \(and some other WebView2 APIs\) are asynchronous, you should use callbacks if code is must be run in a specific order.</span></span>  

## <span data-ttu-id="80e14-179">Шаг 6 — взаимодействие между узлом и веб-контентом</span><span class="sxs-lookup"><span data-stu-id="80e14-179">Step 6 - Communication between host and web content</span></span>  

<span data-ttu-id="80e14-180">Основное приложение и веб-содержимое также могут взаимодействовать друг с другом через `postMessage` метод.</span><span class="sxs-lookup"><span data-stu-id="80e14-180">The host and the web content may also communicate with each other through the `postMessage` method.</span></span>  <span data-ttu-id="80e14-181">Веб-содержимое, запущенное в WebView, может публиковаться на узле с помощью `window.chrome.webview.postMessage` метода, а сообщение обрабатывается любым зарегистрированным `ICoreWebView2WebMessageReceivedEventHandler` обработчиком событий на узле.</span><span class="sxs-lookup"><span data-stu-id="80e14-181">The web content running within a WebView may post to the host through the `window.chrome.webview.postMessage` method, and the message is handled by any registered the `ICoreWebView2WebMessageReceivedEventHandler` event handler on the host.</span></span>  <span data-ttu-id="80e14-182">Аналогичным образом ведущее приложение может выдать сообщение в виде веб-содержимого с помощью `ICoreWebView2::PostWebMessageAsString` или `ICoreWebView2::PostWebMessageAsJSON` метода, которое перехватывается обработчиками, добавленными из `window.chrome.webview.addEventListener` прослушивателя.</span><span class="sxs-lookup"><span data-stu-id="80e14-182">Likewise, the host may message the web content through `ICoreWebView2::PostWebMessageAsString` or `ICoreWebView2::PostWebMessageAsJSON` method, which is caught by handlers added from `window.chrome.webview.addEventListener` listener.</span></span>  <span data-ttu-id="80e14-183">Механизм связи позволяет веб-контенту использовать собственные возможности путем передачи сообщений, чтобы запрашивать хост запускать собственные API.</span><span class="sxs-lookup"><span data-stu-id="80e14-183">The communication mechanism allows the web content to use native capabilities by passing messages to ask the host to run native APIs.</span></span>  

<span data-ttu-id="80e14-184">В качестве примера для понимания механизма можно выполнить следующие действия при печати URL-адреса документа в WebView.</span><span class="sxs-lookup"><span data-stu-id="80e14-184">As an example to understand the mechanism, the following steps occur when you try printing out the document URL in WebView.</span></span>  

1.  <span data-ttu-id="80e14-185">Основное приложение регистрирует обработчик, чтобы вернуть полученное сообщение обратно в веб-содержимое.</span><span class="sxs-lookup"><span data-stu-id="80e14-185">The host registers a handler to return received message back to the web content</span></span>  
1.  <span data-ttu-id="80e14-186">Ведущее приложение вставляет сценарий в веб-содержимое, которое регистрирует обработчик для печати сообщения с узла.</span><span class="sxs-lookup"><span data-stu-id="80e14-186">The host injects a script to the web content that registers a handler to print message from the host</span></span>  
1.  <span data-ttu-id="80e14-187">Ведущее приложение вставляет сценарий в веб-содержимое, которое отправляет URL-адрес узлу.</span><span class="sxs-lookup"><span data-stu-id="80e14-187">The host injects a script to the web content that posts the URL to the host</span></span>  
1.  <span data-ttu-id="80e14-188">Обработчик узла активируется и возвращает сообщение \ (URL-адрес) в веб-содержимое.</span><span class="sxs-lookup"><span data-stu-id="80e14-188">The handler of the host is triggered and returns the message \(the URL\) to the web content</span></span>  
1.  <span data-ttu-id="80e14-189">Обработчик веб-содержимого активируется и печатает сообщение от узла \ (URL-адрес)</span><span class="sxs-lookup"><span data-stu-id="80e14-189">The handler of the web content is triggered and prints message from the host \(the URL\)</span></span>  

<span data-ttu-id="80e14-190">Скопируйте приведенный ниже фрагмент кода и вставьте его в `HelloWebView.cpp` .</span><span class="sxs-lookup"><span data-stu-id="80e14-190">Copy the following code snippet and paste into `HelloWebView.cpp`.</span></span>    

```cpp
// Set an event handler for the host to return received message back to the web content
webviewWindow->add_WebMessageReceived(Callback<ICoreWebView2WebMessageReceivedEventHandler>(
    [](ICoreWebView2* webview, ICoreWebView2WebMessageReceivedEventArgs * args) -> HRESULT {
        PWSTR message;
        args->TryGetWebMessageAsString(&message);
        // processMessage(&message);
        webview->PostWebMessageAsString(message);
        CoTaskMemFree(message);
        return S_OK;
    }).Get(), &token);

// Schedule an async task to add initialization script that
// 1) Add an listener to print message from the host
// 2) Post document URL to the host
webviewWindow->AddScriptToExecuteOnDocumentCreated(
    L"window.chrome.webview.addEventListener(\'message\', event => alert(event.data));" \
    L"window.chrome.webview.postMessage(window.document.URL);",
nullptr);
```  

### <span data-ttu-id="80e14-191">Создание примера приложения "Показать URL-адрес"</span><span class="sxs-lookup"><span data-stu-id="80e14-191">Build your show URL sample app</span></span>  

<span data-ttu-id="80e14-192">Выберите `F5` , чтобы выполнить сборку и запустить приложение.</span><span class="sxs-lookup"><span data-stu-id="80e14-192">Select `F5` to build and run the app.</span></span>  <span data-ttu-id="80e14-193">URL-адрес отображается во всплывающем окне перед переходом на страницу.</span><span class="sxs-lookup"><span data-stu-id="80e14-193">The URL appears in a pop-up window before navigating to a page.</span></span>  

:::image type="complex" source="../media/show-url.png" alt-text="Версия инструмента" lightbox="../media/show-url.png":::
   <span data-ttu-id="80e14-195">Показать URL-адрес</span><span class="sxs-lookup"><span data-stu-id="80e14-195">Show url</span></span>  
:::image-end:::  

<span data-ttu-id="80e14-196">Поздравляем! вы только что создали первое приложение WebView2.</span><span class="sxs-lookup"><span data-stu-id="80e14-196">Congratulations, you just built your first WebView2 app.</span></span>  

## <span data-ttu-id="80e14-197">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="80e14-197">Next steps</span></span>  

<span data-ttu-id="80e14-198">Многие функции WebView2, не описанные на этой странице, в следующем разделе представлены дополнительные ресурсы.</span><span class="sxs-lookup"><span data-stu-id="80e14-198">Many of the WebView2 functionalities that are not covered on this page, the following section provided additional resources.</span></span>  

### <span data-ttu-id="80e14-199">См. также</span><span class="sxs-lookup"><span data-stu-id="80e14-199">See also</span></span>  

*   <span data-ttu-id="80e14-200">Полный пример возможностей WebView2 можно найти в [примере WEBVIEW2 API][GithubMicrosoftedgeWebview2samplesApisample].</span><span class="sxs-lookup"><span data-stu-id="80e14-200">For a comprehensive example of WebView2 capabilities, navigate to [WebView2 API Sample][GithubMicrosoftedgeWebview2samplesApisample].</span></span>  
*   <span data-ttu-id="80e14-201">Для примера приложения, созданного с помощью WebView2, перейдите на [WebView2Browser][GithubMicrosoftedgeWebview2browser].</span><span class="sxs-lookup"><span data-stu-id="80e14-201">For a sample application built using WebView2, navigate to [WebView2Browser][GithubMicrosoftedgeWebview2browser].</span></span>  
*   <span data-ttu-id="80e14-202">Для получения подробных сведений о API WebView2 перейдите на [ссылку API][Webview2ReferenceWin32].</span><span class="sxs-lookup"><span data-stu-id="80e14-202">For detailed information about the WebView2 API, navigate to [API reference][Webview2ReferenceWin32].</span></span>  

## <span data-ttu-id="80e14-203">Знакомство с командой Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="80e14-203">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[Webview2Index]: ../index.md "Введение в Microsoft Edge WebView2 (Предварительная версия) | Документы Microsoft"  
[Webview2ReferenceWin32]: /microsoft-edge/webview2/reference/win32 "Справочник по WebView2 Win32 C++ | Документы Microsoft"  
[Webview2ConceptsNavigationEvents]: ../concepts/navigation-events.md "События навигации | Документы Microsoft"  

[CppCxWrlTemplateLibraryVS2019]: /cpp/cppcx/wrl/windows-runtime-cpp-template-library-wrl?view=vs-2019&preserve-view=true "Библиотека шаблонов C++ среды выполнения Windows (WRL) | Документы Microsoft"  
[CppWindowsWalkthroughCreatingDesktopApplication]: /cpp/windows/walkthrough-creating-windows-desktop-applications-cpp?view=vs-2019&preserve-view=true "Пошаговое руководство: создание традиционного классического приложения для Windows (C++) | Документы Microsoft"  

[GithubMicrosoftedgeWebview2browser]: https://github.com/MicrosoftEdge/WebView2Browser "WebView2Browser-MicrosoftEdge/WebView2Browser | GitHub"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView Feedback-MicrosoftEdge/WebViewFeedback | GitHub"  

[GithubMicrosoftedgeWebview2samplesApisample]: https://github.com/MicrosoftEdge/WebView2Samples/blob/master/SampleApps/WebView2APISample/README.md "Образец API WebView2-MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesGettingStartedGuide]: https://github.com/MicrosoftEdge/WebView2Samples#1-getting-started-guide "WebView2 Samples-MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftWilMain]: https://github.com/Microsoft/wil "Библиотеки реализации Windows (будет) — Microsoft/будет | GitHub"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Скачайте каналы предварительной оценки Microsoft Edge"  

[MicrosoftVisualstudioMain]: https://visualstudio.microsoft.com "Visual Studio"  

[Webview2Installer]: https://developer.microsoft.com/microsoft-edge/webview2 "Установщик WebView2"  
