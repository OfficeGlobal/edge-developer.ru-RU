---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2ExperimentalEnvironment
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2ExperimentalEnvironment
ms.openlocfilehash: 468920744308ee1138dc6c5abf0d6c85b5b6ada7
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012531"
---
# <span data-ttu-id="e1822-104">интерфейс ICoreWebView2ExperimentalEnvironment</span><span class="sxs-lookup"><span data-stu-id="e1822-104">interface ICoreWebView2ExperimentalEnvironment</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalEnvironment
  : public IUnknown
```

<span data-ttu-id="e1822-105">Этот интерфейс является расширением [ICoreWebView2Environment](icorewebview2environment.md).</span><span class="sxs-lookup"><span data-stu-id="e1822-105">This interface is an extension of the [ICoreWebView2Environment](icorewebview2environment.md).</span></span>

## <span data-ttu-id="e1822-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="e1822-106">Summary</span></span>

 <span data-ttu-id="e1822-107">Участников</span><span class="sxs-lookup"><span data-stu-id="e1822-107">Members</span></span>                        | <span data-ttu-id="e1822-108">Описания</span><span class="sxs-lookup"><span data-stu-id="e1822-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e1822-109">CreateCoreWebView2CompositionController</span><span class="sxs-lookup"><span data-stu-id="e1822-109">CreateCoreWebView2CompositionController</span></span>](#createcorewebview2compositioncontroller) | <span data-ttu-id="e1822-110">Асинхронно создайте новый WebView для использования с визуальным размещением.</span><span class="sxs-lookup"><span data-stu-id="e1822-110">Asynchronously create a new WebView for use with visual hosting.</span></span>
[<span data-ttu-id="e1822-111">CreateCoreWebView2PointerInfo</span><span class="sxs-lookup"><span data-stu-id="e1822-111">CreateCoreWebView2PointerInfo</span></span>](#createcorewebview2pointerinfo) | <span data-ttu-id="e1822-112">Создание пустого [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md).</span><span class="sxs-lookup"><span data-stu-id="e1822-112">Create an empty [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md).</span></span>
[<span data-ttu-id="e1822-113">GetProviderForHwnd</span><span class="sxs-lookup"><span data-stu-id="e1822-113">GetProviderForHwnd</span></span>](#getproviderforhwnd) | <span data-ttu-id="e1822-114">Возвращает поставщик модели автоматизации пользовательского интерфейса для ICoreWebView2CompositionController, соответствующего данному дескриптору HWND.</span><span class="sxs-lookup"><span data-stu-id="e1822-114">Returns the UI Automation Provider for the ICoreWebView2CompositionController that corresponds with the given HWND.</span></span>

<span data-ttu-id="e1822-115">Объект, реализующий интерфейс [ICoreWebView2ExperimentalEnvironment]() , также будет реализовывать [ICoreWebView2Environment](icorewebview2environment.md).</span><span class="sxs-lookup"><span data-stu-id="e1822-115">An object implementing the [ICoreWebView2ExperimentalEnvironment]() interface will also implement [ICoreWebView2Environment](icorewebview2environment.md).</span></span>

## <span data-ttu-id="e1822-116">Участников</span><span class="sxs-lookup"><span data-stu-id="e1822-116">Members</span></span>

#### <span data-ttu-id="e1822-117">CreateCoreWebView2CompositionController</span><span class="sxs-lookup"><span data-stu-id="e1822-117">CreateCoreWebView2CompositionController</span></span> 

<span data-ttu-id="e1822-118">Асинхронно создайте новый WebView для использования с визуальным размещением.</span><span class="sxs-lookup"><span data-stu-id="e1822-118">Asynchronously create a new WebView for use with visual hosting.</span></span>

> <span data-ttu-id="e1822-119">общедоступные значения HRESULT [CreateCoreWebView2CompositionController](#createcorewebview2compositioncontroller)(HWND ParentWindow, [ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler](icorewebview2experimentalcreatecorewebview2compositioncontrollercompletedhandler.md) \* обработчик)</span><span class="sxs-lookup"><span data-stu-id="e1822-119">public HRESULT [CreateCoreWebView2CompositionController](#createcorewebview2compositioncontroller)(HWND parentWindow, [ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler](icorewebview2experimentalcreatecorewebview2compositioncontrollercompletedhandler.md) \* handler)</span></span>

<span data-ttu-id="e1822-120">parentWindow — это HWND, в котором приложение будет подключаться к визуальному дереву WebView.</span><span class="sxs-lookup"><span data-stu-id="e1822-120">parentWindow is the HWND in which the app will connect the visual tree of the WebView.</span></span> <span data-ttu-id="e1822-121">Это HWND того, что приложение получит ввод указателя или мыши, предназначенное для WebView (и для пересылки потребуется функция SendMouseInput/SendPointerInput).</span><span class="sxs-lookup"><span data-stu-id="e1822-121">This will be the HWND that the app will receive pointer/ mouse input meant for the WebView (and will need to use SendMouseInput/ SendPointerInput to forward).</span></span> <span data-ttu-id="e1822-122">Если приложение перемещает визуальное дерево WebView в другое окно, ему нужно вызвать put_ParentWindow, чтобы обновить новый родительский дескриптор HWND визуального дерева.</span><span class="sxs-lookup"><span data-stu-id="e1822-122">If the app moves the WebView visual tree to underneath a different window, then it needs to call put_ParentWindow to update the new parent HWND of the visual tree.</span></span>

<span data-ttu-id="e1822-123">Используйте put_RootVisualTarget в созданном CoreWebView2CompositionController, чтобы предоставить визуальное приложение для размещения визуального дерева браузера.</span><span class="sxs-lookup"><span data-stu-id="e1822-123">Use put_RootVisualTarget on the created CoreWebView2CompositionController to provide a visual to host the browser's visual tree.</span></span>

<span data-ttu-id="e1822-124">Рекомендуется, чтобы идентификатор пользовательской модели приложения "Настройка приложения" для процесса или окна приложения был установлен.</span><span class="sxs-lookup"><span data-stu-id="e1822-124">It is recommended that the application set Application User Model ID for the process or the application window.</span></span> <span data-ttu-id="e1822-125">Если не задано значение None, во время создания WebView для созданного идентификатора пользовательской модели приложения задается корневое окно parentWindow.</span><span class="sxs-lookup"><span data-stu-id="e1822-125">If none is set, during WebView creation a generated Application User Model ID is set to root window of parentWindow.</span></span> 
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
 <span data-ttu-id="e1822-126">Рекомендуется, чтобы приложение обрабатывало сообщения диспетчера перезапуска, чтобы его можно было перезапустить надлежащим образом в случае, когда приложение использует Edge для WebView с определенной установкой и удаляется установка.</span><span class="sxs-lookup"><span data-stu-id="e1822-126">It is recommended that the application handles restart manager messages so that it can be restarted gracefully in the case when the app is using Edge for webview from a certain installation and that installation is being uninstalled.</span></span> <span data-ttu-id="e1822-127">Например, если пользователь устанавливает ребро с канала разработки и использует ребро с этого канала для тестирования приложения, а затем удаляет Edge из него, не закрывая приложение, приложение будет перезапущена, чтобы разрешить удаление канала разработки для успешного выполнения.</span><span class="sxs-lookup"><span data-stu-id="e1822-127">For example, if a user installs Edge from Dev channel and opts to use Edge from that channel for testing the app, and then uninstalls Edge from that channel without closing the app, the app will be restarted to allow uninstallation of the dev channel to succeed.</span></span> 
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

#### <span data-ttu-id="e1822-128">CreateCoreWebView2PointerInfo</span><span class="sxs-lookup"><span data-stu-id="e1822-128">CreateCoreWebView2PointerInfo</span></span> 

<span data-ttu-id="e1822-129">Создание пустого [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md).</span><span class="sxs-lookup"><span data-stu-id="e1822-129">Create an empty [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md).</span></span>

> <span data-ttu-id="e1822-130">общедоступные значения HRESULT [CreateCoreWebView2PointerInfo](#createcorewebview2pointerinfo)([ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) \* \* pointerInfo)</span><span class="sxs-lookup"><span data-stu-id="e1822-130">public HRESULT [CreateCoreWebView2PointerInfo](#createcorewebview2pointerinfo)([ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) \*\* pointerInfo)</span></span>

<span data-ttu-id="e1822-131">Возвращенные [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) должны быть заполнены всеми соответствующими сведениями перед вызовом SendPointerInput.</span><span class="sxs-lookup"><span data-stu-id="e1822-131">The returned [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) needs to be populated with all of the relevant info before calling SendPointerInput.</span></span>

#### <span data-ttu-id="e1822-132">GetProviderForHwnd</span><span class="sxs-lookup"><span data-stu-id="e1822-132">GetProviderForHwnd</span></span> 

<span data-ttu-id="e1822-133">Возвращает поставщик модели автоматизации пользовательского интерфейса для ICoreWebView2CompositionController, соответствующего данному дескриптору HWND.</span><span class="sxs-lookup"><span data-stu-id="e1822-133">Returns the UI Automation Provider for the ICoreWebView2CompositionController that corresponds with the given HWND.</span></span>

> <span data-ttu-id="e1822-134">общедоступные значения HRESULT [GetProviderForHwnd](#getproviderforhwnd)(HWND HWND \* Provider)</span><span class="sxs-lookup"><span data-stu-id="e1822-134">public HRESULT [GetProviderForHwnd](#getproviderforhwnd)(HWND hwnd, IUnknown \*\* provider)</span></span>
