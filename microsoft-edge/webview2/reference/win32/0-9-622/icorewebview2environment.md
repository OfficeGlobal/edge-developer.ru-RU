---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2Environment
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2Environment
ms.openlocfilehash: edf573bc7c4c83c7882005937db29a068ab7b015
ms.sourcegitcommit: 2d57b515d6ccbbe24cb3a8c8f44f9c3a26fc17a4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "11115787"
---
# <span data-ttu-id="96b63-104">интерфейс ICoreWebView2Environment</span><span class="sxs-lookup"><span data-stu-id="96b63-104">interface ICoreWebView2Environment</span></span> 

```
interface ICoreWebView2Environment
  : public IUnknown
```

<span data-ttu-id="96b63-105">Представляет среду WebView2.</span><span class="sxs-lookup"><span data-stu-id="96b63-105">This represents the WebView2 Environment.</span></span>

## <span data-ttu-id="96b63-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="96b63-106">Summary</span></span>

 <span data-ttu-id="96b63-107">Участников</span><span class="sxs-lookup"><span data-stu-id="96b63-107">Members</span></span>                        | <span data-ttu-id="96b63-108">Описания</span><span class="sxs-lookup"><span data-stu-id="96b63-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="96b63-109">add_NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="96b63-109">add_NewBrowserVersionAvailable</span></span>](#add_newbrowserversionavailable) | <span data-ttu-id="96b63-110">Добавьте обработчик событий для события NewBrowserVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="96b63-110">Add an event handler for the NewBrowserVersionAvailable event.</span></span>
[<span data-ttu-id="96b63-111">CreateCoreWebView2Controller</span><span class="sxs-lookup"><span data-stu-id="96b63-111">CreateCoreWebView2Controller</span></span>](#createcorewebview2controller) | <span data-ttu-id="96b63-112">Асинхронно создайте новый WebView.</span><span class="sxs-lookup"><span data-stu-id="96b63-112">Asynchronously create a new WebView.</span></span>
[<span data-ttu-id="96b63-113">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="96b63-113">CreateWebResourceResponse</span></span>](#createwebresourceresponse) | <span data-ttu-id="96b63-114">Создание нового объекта ответа на веб-ресурс.</span><span class="sxs-lookup"><span data-stu-id="96b63-114">Create a new web resource response object.</span></span>
[<span data-ttu-id="96b63-115">get_BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="96b63-115">get_BrowserVersionString</span></span>](#get_browserversionstring) | <span data-ttu-id="96b63-116">Сведения о версии браузера для текущего [ICoreWebView2Environment](), включая имя канала, если он не является стабильным каналом.</span><span class="sxs-lookup"><span data-stu-id="96b63-116">The browser version info of the current [ICoreWebView2Environment](), including channel name if it is not the stable channel.</span></span>
[<span data-ttu-id="96b63-117">remove_NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="96b63-117">remove_NewBrowserVersionAvailable</span></span>](#remove_newbrowserversionavailable) | <span data-ttu-id="96b63-118">Удалите обработчик событий, добавленный ранее add_NewBrowserVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="96b63-118">Remove an event handler previously added with add_NewBrowserVersionAvailable.</span></span>

<span data-ttu-id="96b63-119">Веб – представления, созданные из среды, выполняются в процессе браузера, указанном в параметрах среды, и объекты, созданные из среды, должны использоваться в одной среде.</span><span class="sxs-lookup"><span data-stu-id="96b63-119">WebViews created from an environment run on the browser process specified with environment parameters and objects created from an environment should be used in the same environment.</span></span> <span data-ttu-id="96b63-120">Использование этой функции в разных средах не гарантирует совместимость и может привести к сбою.</span><span class="sxs-lookup"><span data-stu-id="96b63-120">Using it in different environments are not guaranteed to be compatible and may fail.</span></span>

## <span data-ttu-id="96b63-121">Участников</span><span class="sxs-lookup"><span data-stu-id="96b63-121">Members</span></span>

#### <span data-ttu-id="96b63-122">add_NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="96b63-122">add_NewBrowserVersionAvailable</span></span> 

<span data-ttu-id="96b63-123">Добавьте обработчик событий для события NewBrowserVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="96b63-123">Add an event handler for the NewBrowserVersionAvailable event.</span></span>

> <span data-ttu-id="96b63-124">общедоступные значения HRESULT [add_NewBrowserVersionAvailable](#add_newbrowserversionavailable)([ICoreWebView2NewBrowserVersionAvailableEventHandler](icorewebview2newbrowserversionavailableeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="96b63-124">public HRESULT [add_NewBrowserVersionAvailable](#add_newbrowserversionavailable)([ICoreWebView2NewBrowserVersionAvailableEventHandler](icorewebview2newbrowserversionavailableeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="96b63-125">NewBrowserVersionAvailable активируется, когда установлена более новая версия браузера EDGE и доступна для использования через WebView2.</span><span class="sxs-lookup"><span data-stu-id="96b63-125">NewBrowserVersionAvailable fires when a newer version of the Edge browser is installed and available for use via WebView2.</span></span> <span data-ttu-id="96b63-126">Для использования более новой версии браузера необходимо создать новую среду и WebView.</span><span class="sxs-lookup"><span data-stu-id="96b63-126">To use the newer version of the browser you must create a new environment and WebView.</span></span> <span data-ttu-id="96b63-127">Это событие будет инициировано только для новой версии из того же канала, из которого выполняется код.</span><span class="sxs-lookup"><span data-stu-id="96b63-127">This event will only be fired for new version from the same Edge channel that the code is running from.</span></span> <span data-ttu-id="96b63-128">Если вы не используете установленный EDGE, событие не срабатывает.</span><span class="sxs-lookup"><span data-stu-id="96b63-128">When not running with installed Edge, no event will be fired.</span></span>

<span data-ttu-id="96b63-129">Поскольку папка данных пользователя может использоваться только одним процессом браузера за один раз, если вы хотите использовать одну и ту же папку данных пользователя в веб-представлении с помощью новой версии браузера, необходимо сначала закрыть среду и веб-представления, которые используют более старую версию браузера.</span><span class="sxs-lookup"><span data-stu-id="96b63-129">Because a user data folder can only be used by one browser process at a time, if you want to use the same user data folder in the WebViews using the new version of the browser, you must close the environment and WebViews that are using the older version of the browser first.</span></span> <span data-ttu-id="96b63-130">Или просто запросите пользователя перезапустить приложение.</span><span class="sxs-lookup"><span data-stu-id="96b63-130">Or simply prompt the user to restart the app.</span></span>

```cpp
    // After the environment is successfully created,
    // register a handler for the NewBrowserVersionAvailable event.
    // This handler tells when there is a new Edge version available on the machine.
    CHECK_FAILURE(m_webViewEnvironment->add_NewBrowserVersionAvailable(
        Callback<ICoreWebView2NewBrowserVersionAvailableEventHandler>(
            [this](ICoreWebView2Environment* sender, IUnknown* args) -> HRESULT {
                std::wstring message = L"We detected there is a new version for the browser.";
                if (m_webView)
                {
                    message += L"Do you want to restart the app? \n\n";
                    message += L"Click No if you only want to re-create the webviews. \n";
                    message += L"Click Cancel for no action. \n";
                }
                int response = MessageBox(
                    m_mainWindow, message.c_str(), L"New available version",
                    m_webView ? MB_YESNOCANCEL : MB_OK);

                if (response == IDYES)
                {
                    RestartApp();
                }
                else if (response == IDNO)
                {
                    ReinitializeWebViewWithNewBrowser();
                }
                else
                {
                    // do nothing
                }

                return S_OK;
            })
            .Get(),
        nullptr));
```

#### <span data-ttu-id="96b63-131">CreateCoreWebView2Controller</span><span class="sxs-lookup"><span data-stu-id="96b63-131">CreateCoreWebView2Controller</span></span> 

<span data-ttu-id="96b63-132">Асинхронно создайте новый WebView.</span><span class="sxs-lookup"><span data-stu-id="96b63-132">Asynchronously create a new WebView.</span></span>

> <span data-ttu-id="96b63-133">общедоступные значения HRESULT [CreateCoreWebView2Controller](#createcorewebview2controller)(HWND ParentWindow, [ICoreWebView2CreateCoreWebView2ControllerCompletedHandler](icorewebview2createcorewebview2controllercompletedhandler.md) \* обработчик)</span><span class="sxs-lookup"><span data-stu-id="96b63-133">public HRESULT [CreateCoreWebView2Controller](#createcorewebview2controller)(HWND parentWindow, [ICoreWebView2CreateCoreWebView2ControllerCompletedHandler](icorewebview2createcorewebview2controllercompletedhandler.md) \* handler)</span></span>

<span data-ttu-id="96b63-134">parentWindow — HWND, в котором нужно отобразить WebView и из которого принимаются входные данные.</span><span class="sxs-lookup"><span data-stu-id="96b63-134">parentWindow is the HWND in which the WebView should be displayed and from which receive input.</span></span> <span data-ttu-id="96b63-135">WebView добавит дочернее окно в заданное окно во время создания WebView.</span><span class="sxs-lookup"><span data-stu-id="96b63-135">The WebView will add a child window to the provided window during WebView creation.</span></span> <span data-ttu-id="96b63-136">Z-порядок и другие элементы, которые влияют на родственный порядок окон, будут затронуты соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="96b63-136">Z-order and other things impacted by sibling window order will be affected accordingly.</span></span>

<span data-ttu-id="96b63-137">Рекомендуется, чтобы идентификатор пользовательской модели приложения "Настройка приложения" для процесса или окна приложения был установлен.</span><span class="sxs-lookup"><span data-stu-id="96b63-137">It is recommended that the application set Application User Model ID for the process or the application window.</span></span> <span data-ttu-id="96b63-138">Если не задано значение None, во время создания WebView для созданного идентификатора пользовательской модели приложения задается корневое окно parentWindow.</span><span class="sxs-lookup"><span data-stu-id="96b63-138">If none is set, during WebView creation a generated Application User Model ID is set to root window of parentWindow.</span></span> 
```cpp
// Create or recreate the WebView and its environment.
void AppWindow::InitializeWebView()
{
    // To ensure browser switches get applied correctly, we need to close
    // the existing WebView. This will result in a new browser process
    // getting created which will apply the browser switches.
    CloseWebView();
    m_dcompDevice = nullptr;
    m_wincompCompositor = nullptr;
    LPCWSTR subFolder = nullptr;

    if (m_creationModeId == IDM_CREATION_MODE_VISUAL_DCOMP ||
        m_creationModeId == IDM_CREATION_MODE_TARGET_DCOMP)
    {
        HRESULT hr = DCompositionCreateDevice2(nullptr, IID_PPV_ARGS(&m_dcompDevice));
        if (!SUCCEEDED(hr))
        {
            MessageBox(
                m_mainWindow,
                L"Attempting to create WebView using DComp Visual is not supported.\r\n"
                "DComp device creation failed.\r\n"
                "Current OS may not support DComp.",
                L"Create with Windowless DComp Visual Failed", MB_OK);
            return;
        }
    }
    else if (m_creationModeId == IDM_CREATION_MODE_VISUAL_WINCOMP)
    {
        HRESULT hr = TryCreateDispatcherQueue();
        if (!SUCCEEDED(hr))
        {
            MessageBox(
                m_mainWindow,
                L"Attempting to create WebView using WinComp Visual is not supported.\r\n"
                "WinComp compositor creation failed.\r\n"
                "Current OS may not support WinComp.",
                L"Create with Windowless WinComp Visual Failed", MB_OK);
            return;
        }
        m_wincompCompositor = winrtComp::Compositor();
    }
    auto options = Microsoft::WRL::Make<CoreWebView2EnvironmentOptions>();
    CHECK_FAILURE(options->put_AllowSingleSignOnUsingOSPrimaryAccount(
        m_AADSSOEnabled ? TRUE : FALSE));
    if (!m_language.empty())
        CHECK_FAILURE(options->put_Language(m_language.c_str()));
    HRESULT hr = CreateCoreWebView2EnvironmentWithOptions(
        subFolder, nullptr, options.Get(),
        Callback<ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler>(
            this, &AppWindow::OnCreateEnvironmentCompleted)
            .Get());
    if (!SUCCEEDED(hr))
    {
        if (hr == HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND))
        {
            MessageBox(
                m_mainWindow,
                L"Couldn't find Edge installation. "
                "Do you have a version installed that's compatible with this "
                "WebView2 SDK version?",
                nullptr, MB_OK);
        }
        else
        {
            ShowFailure(hr, L"Failed to create webview environment");
        }
    }
}
// This is the callback passed to CreateWebViewEnvironmentWithOptions.
// Here we simply create the WebView.
HRESULT AppWindow::OnCreateEnvironmentCompleted(
    HRESULT result, ICoreWebView2Environment* environment)
{
    CHECK_FAILURE(result);
    m_webViewEnvironment = environment;

    auto webViewExperimentalEnvironment =
        m_webViewEnvironment.try_query<ICoreWebView2ExperimentalEnvironment>();
    if (webViewExperimentalEnvironment && (m_dcompDevice || m_wincompCompositor))
    {
        CHECK_FAILURE(webViewExperimentalEnvironment->CreateCoreWebView2CompositionController(
            m_mainWindow,
            Callback<
                ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler>(
                [this](
                    HRESULT result,
                    ICoreWebView2ExperimentalCompositionController* compositionController) -> HRESULT {
                    auto controller =
                        wil::com_ptr<ICoreWebView2ExperimentalCompositionController>(compositionController)
                            .query<ICoreWebView2Controller>();
                    return OnCreateCoreWebView2ControllerCompleted(result, controller.get());
                })
                .Get()));
    }
    else
    {
        CHECK_FAILURE(m_webViewEnvironment->CreateCoreWebView2Controller(
            m_mainWindow, Callback<ICoreWebView2CreateCoreWebView2ControllerCompletedHandler>(
                              this, &AppWindow::OnCreateCoreWebView2ControllerCompleted)
                              .Get()));
    }

    return S_OK;
}
```
 <span data-ttu-id="96b63-139">Рекомендуется, чтобы приложение обрабатывало сообщения диспетчера перезапуска, чтобы его можно было перезапустить надлежащим образом в случае, когда приложение использует Edge для WebView с определенной установкой и удаляется установка.</span><span class="sxs-lookup"><span data-stu-id="96b63-139">It is recommended that the application handles restart manager messages so that it can be restarted gracefully in the case when the app is using Edge for WebView from a certain installation and that installation is being uninstalled.</span></span> <span data-ttu-id="96b63-140">Например, если пользователь устанавливает ребро с канала разработки и использует ребро с этого канала для тестирования приложения, а затем удаляет Edge из него, не закрывая приложение, приложение будет перезапущена, чтобы разрешить удаление канала разработки для успешного выполнения.</span><span class="sxs-lookup"><span data-stu-id="96b63-140">For example, if a user installs Edge from Dev channel and opts to use Edge from that channel for testing the app, and then uninstalls Edge from that channel without closing the app, the app will be restarted to allow uninstallation of the dev channel to succeed.</span></span> 
```cpp
    case WM_QUERYENDSESSION:
    {
        // yes, we can shut down
        // Register how we might be restarted
        RegisterApplicationRestart(L"--restore", RESTART_NO_CRASH | RESTART_NO_HANG);
        *result = TRUE;
        return true;
    }
    break;
    case WM_ENDSESSION:
    {
        if (wParam == TRUE)
        {
            // save app state and exit.
            PostQuitMessage(0);
            return true;
        }
    }
    break;
```
 <span data-ttu-id="96b63-141">Когда приложение попытается CreateCoreWebView2Controller после сбоя, рекомендуется перезапустить приложение от создания новой среды WebView2.</span><span class="sxs-lookup"><span data-stu-id="96b63-141">When the application retries CreateCoreWebView2Controller upon failure, it is recommended that the application restarts from creating a new WebView2 Environment.</span></span> <span data-ttu-id="96b63-142">Если происходит обновление EDGE, версия, связанная с WebView2 средой, может быть удалена и привела к тому, что объект перестанет работать.</span><span class="sxs-lookup"><span data-stu-id="96b63-142">If an Edge update happens, the version associated with a WebView2 Environment could have been removed and causing the object to no longer work.</span></span> <span data-ttu-id="96b63-143">Создание новой среды WebView2 будет работать в том случае, если она использует последнюю версию.</span><span class="sxs-lookup"><span data-stu-id="96b63-143">Creating a new WebView2 Environment will work as it uses the latest version.</span></span>

<span data-ttu-id="96b63-144">Создание WebView завершится сбоем, если запущенный экземпляр уже используется в той же папке данных пользователя, а у объектов среды другой EnvironmentOptions или HWND parentWindows имеет разные разрешения DPI.</span><span class="sxs-lookup"><span data-stu-id="96b63-144">WebView creation will fail if there is already a running instance using the same user data folder, and the Environment objects have different EnvironmentOptions or the HWND parentWindows have different DPI awareness.</span></span> <span data-ttu-id="96b63-145">Например, если уже имеется WebView, созданный на одном языке, попытка создать WebView на другом языке с использованием той же папки данных пользователя завершается сбоем.</span><span class="sxs-lookup"><span data-stu-id="96b63-145">For example, if there is already a WebView created with one language, trying to create a WebView with a different language using the same user data folder will fail.</span></span>

#### <span data-ttu-id="96b63-146">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="96b63-146">CreateWebResourceResponse</span></span> 

<span data-ttu-id="96b63-147">Создание нового объекта ответа на веб-ресурс.</span><span class="sxs-lookup"><span data-stu-id="96b63-147">Create a new web resource response object.</span></span>

> <span data-ttu-id="96b63-148">общедоступные значения HRESULT [CreateWebResourceResponse](#createwebresourceresponse)(IStream \* Content, int STATUSCODE, LPCWSTR REASONPHRASE, LPCWSTR Headers, [ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \* \* Response)</span><span class="sxs-lookup"><span data-stu-id="96b63-148">public HRESULT [CreateWebResourceResponse](#createwebresourceresponse)(IStream \* content, int statusCode, LPCWSTR reasonPhrase, LPCWSTR headers, [ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \*\* response)</span></span>

<span data-ttu-id="96b63-149">Заголовки — это строка заголовков необработанного ответа, ограниченная символом новой строки.</span><span class="sxs-lookup"><span data-stu-id="96b63-149">The headers is the raw response header string delimited by newline.</span></span> <span data-ttu-id="96b63-150">Кроме того, можно создать этот объект с пустой строкой заголовков, а затем использовать [ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md) для создания заголовков построчно.</span><span class="sxs-lookup"><span data-stu-id="96b63-150">It's also possible to create this object with empty headers string and then use the [ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md) to construct the headers line by line.</span></span> <span data-ttu-id="96b63-151">Сведения о других параметрах смотрите в [ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md).</span><span class="sxs-lookup"><span data-stu-id="96b63-151">For information on other parameters see [ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md).</span></span>

```cpp
        if (m_blockImages)
        {
            m_webView->AddWebResourceRequestedFilter(L"*", COREWEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE);
            CHECK_FAILURE(m_webView->add_WebResourceRequested(
                Callback<ICoreWebView2WebResourceRequestedEventHandler>(
                    [this](
                        ICoreWebView2* sender,
                        ICoreWebView2WebResourceRequestedEventArgs* args) {
                        COREWEBVIEW2_WEB_RESOURCE_CONTEXT resourceContext;
                        CHECK_FAILURE(
                            args->get_ResourceContext(&resourceContext));
                        // Ensure that the type is image
                        if (resourceContext != COREWEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE)
                        {
                            return E_INVALIDARG;
                        }
                        // Override the response with an empty one to block the image.
                        // If put_Response is not called, the request will continue as normal.
                        wil::com_ptr<ICoreWebView2WebResourceResponse> response;
                        CHECK_FAILURE(m_webViewEnvironment->CreateWebResourceResponse(
                            nullptr, 403 /*NoContent*/, L"Blocked", L"", &response));
                        CHECK_FAILURE(args->put_Response(response.get()));
                        return S_OK;
                    })
                    .Get(),
                &m_webResourceRequestedTokenForImageBlocking));
        }
        else
        {
            CHECK_FAILURE(m_webView->remove_WebResourceRequested(
                m_webResourceRequestedTokenForImageBlocking));
        }
```

#### <span data-ttu-id="96b63-152">get_BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="96b63-152">get_BrowserVersionString</span></span> 

<span data-ttu-id="96b63-153">Сведения о версии браузера для текущего [ICoreWebView2Environment](), включая имя канала, если он не является стабильным каналом.</span><span class="sxs-lookup"><span data-stu-id="96b63-153">The browser version info of the current [ICoreWebView2Environment](), including channel name if it is not the stable channel.</span></span>

> <span data-ttu-id="96b63-154">общедоступные значения HRESULT [get_BrowserVersionString](#get_browserversionstring)(LPWSTR \* versionInfo)</span><span class="sxs-lookup"><span data-stu-id="96b63-154">public HRESULT [get_BrowserVersionString](#get_browserversionstring)(LPWSTR \* versionInfo)</span></span>

<span data-ttu-id="96b63-155">Это соответствует формату API GetAvailableCoreWebView2BrowserVersionString.</span><span class="sxs-lookup"><span data-stu-id="96b63-155">This matches the format of the GetAvailableCoreWebView2BrowserVersionString API.</span></span> <span data-ttu-id="96b63-156">Названия каналов: "бета-версия", "Dev" и "Канарские".</span><span class="sxs-lookup"><span data-stu-id="96b63-156">Channel names are 'beta', 'dev', and 'canary'.</span></span>

```cpp
        wil::unique_cotaskmem_string version_info;
        m_webViewEnvironment->get_BrowserVersionString(&version_info);
        MessageBox(
            m_mainWindow, version_info.get(), L"Browser Version Info After WebView Creation",
            MB_OK);
```

#### <span data-ttu-id="96b63-157">remove_NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="96b63-157">remove_NewBrowserVersionAvailable</span></span> 

<span data-ttu-id="96b63-158">Удалите обработчик событий, добавленный ранее add_NewBrowserVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="96b63-158">Remove an event handler previously added with add_NewBrowserVersionAvailable.</span></span>

> <span data-ttu-id="96b63-159">общедоступные значения HRESULT [remove_NewBrowserVersionAvailable](#remove_newbrowserversionavailable)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="96b63-159">public HRESULT [remove_NewBrowserVersionAvailable](#remove_newbrowserversionavailable)(EventRegistrationToken token)</span></span>

