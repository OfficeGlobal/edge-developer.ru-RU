---
description: Соглашения об API для Win32 C++ WebView2
title: Соглашения об API для Win32 C++ WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/14/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения WPF, WPF, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "браузер", HTML Edge
ms.openlocfilehash: 42f0b5c9970b2e4a6424eb70458c58a98ec8dbc7
ms.sourcegitcommit: 61cc15d2fc89aee3e09cec48ef1e0e5bbf8d289a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/15/2020
ms.locfileid: "11118977"
---
# <span data-ttu-id="bc89f-104">Соглашения об API для Win32 C++ WebView2</span><span class="sxs-lookup"><span data-stu-id="bc89f-104">Win32 C++ WebView2 API conventions</span></span>  

## <span data-ttu-id="bc89f-105">Асинхронные методы</span><span class="sxs-lookup"><span data-stu-id="bc89f-105">Async Methods</span></span>  

<span data-ttu-id="bc89f-106">Асинхронные методы в API-интерфейсе WebView2 Win32 используют делегаты для обратного вызова, чтобы указать, когда асинхронный метод завершился, код успеха или ошибки, а также для некоторых результатов.</span><span class="sxs-lookup"><span data-stu-id="bc89f-106">Asynchronous methods in the WebView2 Win32 C++ API use a delegate interface to callback to you to indicate when the async method has completed, the success or failure code, and for some, the result of the asynchronous method.</span></span>  <span data-ttu-id="bc89f-107">Последний параметр для всех асинхронных методов — указатель на интерфейс делегата, для которого предоставляется реализация.</span><span class="sxs-lookup"><span data-stu-id="bc89f-107">The final parameter for all asynchronous methods is a pointer to a delegate interface of which you provide an implementation.</span></span>  

<span data-ttu-id="bc89f-108">У интерфейса делегата есть единственный `Invoke` метод, который принимает в качестве первого параметра `HRESULT` код успеха или ошибки.</span><span class="sxs-lookup"><span data-stu-id="bc89f-108">The delegate interface has a single `Invoke` method that takes as a first parameter an `HRESULT` of the success or failure code.</span></span>  <span data-ttu-id="bc89f-109">Кроме того, может быть вторым параметром, который является результатом метода, если он имеет результат.</span><span class="sxs-lookup"><span data-stu-id="bc89f-109">Additionally there may be a second parameter that is the result of the method if the method has a result.</span></span>  <span data-ttu-id="bc89f-110">Например, метод [ICoreWebView2:: CapturePreview][Webview2ReferenceWin32Icorewebview2CapturePreview] принимает в качестве последнего параметра `ICoreWebView2CapturePreviewCompletedHandler` указатель.</span><span class="sxs-lookup"><span data-stu-id="bc89f-110">For example, the [ICoreWebView2::CapturePreview][Webview2ReferenceWin32Icorewebview2CapturePreview] method takes as the final parameter an `ICoreWebView2CapturePreviewCompletedHandler` pointer.</span></span>  <span data-ttu-id="bc89f-111">Чтобы отправить `CapturePreview` запрос на метод, необходимо предоставить экземпляр класса `ICoreWebView2CapturePreviewCompletedHandler` , который вы реализуете.</span><span class="sxs-lookup"><span data-stu-id="bc89f-111">To send a `CapturePreview` method request, you provide an instance of the `ICoreWebView2CapturePreviewCompletedHandler` pointer that you implement.</span></span>  <span data-ttu-id="bc89f-112">В следующем фрагменте кода используется один метод для реализации.</span><span class="sxs-lookup"><span data-stu-id="bc89f-112">The following code snippet uses one method to implement.</span></span>  

```cpp
HRESULT Invoke(HRESULT result)
```  

<span data-ttu-id="bc89f-113">Вы реализуете `Invoke` метод и `CoreWebView2` запрашиваете `Invoke` метод по `CapturePreview` завершении запроса.</span><span class="sxs-lookup"><span data-stu-id="bc89f-113">You implement the `Invoke` method and `CoreWebView2` requests your `Invoke` method when `CapturePreview` request completes.</span></span>  <span data-ttu-id="bc89f-114">Единственный параметр — это `HRESULT` Описание кода успеха или ошибки `CapturePreview` запроса.</span><span class="sxs-lookup"><span data-stu-id="bc89f-114">The single parameter is the `HRESULT` describing the success or failure code of the `CapturePreview` request.</span></span>  

<span data-ttu-id="bc89f-115">Кроме того `ICoreWebView2::ExecuteScript` , вы предоставляете экземпляр, в `ICoreWebView2ExecuteScriptCompletedHandler` котором есть `Invoke` метод, который предоставляет код успеха или ошибки `ExecuteScript` запроса, а второй параметр `resultObjectAsJson` — JSON результата выполнения сценария.</span><span class="sxs-lookup"><span data-stu-id="bc89f-115">Or for `ICoreWebView2::ExecuteScript`, you provide an instance of `ICoreWebView2ExecuteScriptCompletedHandler` which has an `Invoke` method that provides you with the success or failure code of the `ExecuteScript` request as well as the second parameter `resultObjectAsJson` which is the JSON of the result of running the script.</span></span>  

<span data-ttu-id="bc89f-116">Вы можете вручную реализовать `CompleteHandler` интерфейсы делегатов, или вы можете использовать [функцию обратного вызова WRL][CppCxWrlCallbackFunction].</span><span class="sxs-lookup"><span data-stu-id="bc89f-116">You may manually implement the `CompleteHandler` delegate interfaces, or you may use the [WRL Callback function][CppCxWrlCallbackFunction].</span></span>  <span data-ttu-id="bc89f-117">Функция обратного вызова используется в следующем фрагменте кода WebView2.</span><span class="sxs-lookup"><span data-stu-id="bc89f-117">The Callback function is used throughout the following WebView2 code snippet.</span></span>  

```cpp
void ScriptComponent::InjectScript()
{
    TextInputDialog dialog(
        m_appWindow->GetMainWindow(),
        L"Inject Script",
        L"Enter script code:",
        L"Enter the JavaScript code to run in the webview.",
        L"window.getComputedStyle(document.body).backgroundColor");
    if (dialog.confirmed)
    {
        m_webView->ExecuteScript(dialog.input.c_str(),
            Callback<ICoreWebView2ExecuteScriptCompletedHandler>(
                [](HRESULT error, PCWSTR result) -> HRESULT
        {
            if (error != S_OK) {
                ShowFailure(error, L"ExecuteScript failed");
            }
            MessageBox(nullptr, result, L"ExecuteScript Result", MB_OK);
            return S_OK;
        }).Get());
    }
}
```  

## <span data-ttu-id="bc89f-118">Мероприятия</span><span class="sxs-lookup"><span data-stu-id="bc89f-118">Events</span></span>  

<span data-ttu-id="bc89f-119">События в API-интерфейсе WebView2 Win32 с `add_EventName` использованием `remove_EventName` пары "и" для подписки и отмены подписки на события.</span><span class="sxs-lookup"><span data-stu-id="bc89f-119">Events in the WebView2 Win32 C++ API use the `add_EventName` and `remove_EventName` method pair to subscribe and unsubscribe from events.</span></span>  <span data-ttu-id="bc89f-120">Этот `add_EventName` метод принимает интерфейс делегата обработчика событий и возвращает для него обратное значение в `EventRegistrationToken` качестве выходного параметра.</span><span class="sxs-lookup"><span data-stu-id="bc89f-120">The `add_EventName` method takes an event handler delegate interface and gives back an `EventRegistrationToken` as an out parameter.</span></span>  <span data-ttu-id="bc89f-121">Этот метод принимает и отменяет подписку на `remove_EventName` `EventRegistrationToken` соответствующую подписку на событие.</span><span class="sxs-lookup"><span data-stu-id="bc89f-121">The `remove_EventName` method takes an `EventRegistrationToken` and unsubscribes the corresponding event subscription.</span></span>  

<span data-ttu-id="bc89f-122">Интерфейсы делегатов обработчиков событий очень сходны с интерфейсами делегатов асинхронных обработчиков.</span><span class="sxs-lookup"><span data-stu-id="bc89f-122">Event handler delegate interfaces work very similarly to the async method completed handler delegate interfaces.</span></span>  <span data-ttu-id="bc89f-123">Вы реализуете интерфейс делегата обработчика событий и `CoreWebView2` отправляете обратный вызов каждый раз при срабатывании события.</span><span class="sxs-lookup"><span data-stu-id="bc89f-123">You implement the event handler delegate interface and `CoreWebView2` sends a callback whenever the event fires.</span></span>  <span data-ttu-id="bc89f-124">Каждый интерфейс делегата обработчика событий имеет один `Invoke` метод с параметром sender, а затем параметром аргументов события.</span><span class="sxs-lookup"><span data-stu-id="bc89f-124">Every event handler delegate interface has a single `Invoke` method that has a sender parameter followed by an event args parameter.</span></span>  <span data-ttu-id="bc89f-125">Отправитель — это экземпляр объекта, на который вы подписаны для событий.</span><span class="sxs-lookup"><span data-stu-id="bc89f-125">The sender is the instance of the object on which you subscribed for events.</span></span>  <span data-ttu-id="bc89f-126">Параметр args событий — это интерфейс, который содержит сведения о событиях, выполняемых в данный момент.</span><span class="sxs-lookup"><span data-stu-id="bc89f-126">The event args parameter is an interface that contains information about the currently firing event.</span></span>  

<span data-ttu-id="bc89f-127">Например, `NavigationCompleted` событие On `ICoreWebView2` имеет `ICoreWebView2::add_NavigationCompleted` `ICoreWebView2::remove_NavigationCompleted` пару метод и.</span><span class="sxs-lookup"><span data-stu-id="bc89f-127">For instance the `NavigationCompleted` event on `ICoreWebView2` has the `ICoreWebView2::add_NavigationCompleted` and `ICoreWebView2::remove_NavigationCompleted` method pair.</span></span>  <span data-ttu-id="bc89f-128">Когда вы запрашиваете добавить, вы предоставляете экземпляр, `ICoreWebView2NavigationCompletedEventHandler` в котором вы ранее реализовали `Invoke` метод.</span><span class="sxs-lookup"><span data-stu-id="bc89f-128">When you request add you provide an instance of `ICoreWebView2NavigationCompletedEventHandler` in which you previously implemented `Invoke` method.</span></span>  <span data-ttu-id="bc89f-129">При `NavigationCompleted` срабатывании события `Invoke` запрашивается метод.</span><span class="sxs-lookup"><span data-stu-id="bc89f-129">When the `NavigationCompleted` event fires, your `Invoke` method is requested.</span></span>  <span data-ttu-id="bc89f-130">Первый параметр, `ICoreWebView2` который срабатывает на `NavigationCompleted` событие.</span><span class="sxs-lookup"><span data-stu-id="bc89f-130">The first parameter is the `ICoreWebView2` which is firing the `NavigationCompleted` event.</span></span>  <span data-ttu-id="bc89f-131">Второй параметр, `ICoreWebView2NavigationCompletedEventArgs` содержащий сведения о том, успешно ли была выполнена Навигация и так далее.</span><span class="sxs-lookup"><span data-stu-id="bc89f-131">The second parameter is the `ICoreWebView2NavigationCompletedEventArgs` which contains information about if the navigation completed successfully and so on.</span></span>  

<span data-ttu-id="bc89f-132">Точно так же, как и в случае с интерфейсом делегата "асинхронный обработчик", вы можете реализовать его напрямую, или вы можете использовать функцию обратного вызова WRL, которая используется в следующем фрагменте кода WebView2.</span><span class="sxs-lookup"><span data-stu-id="bc89f-132">Similarly to the async method completed handler delegate interface you are able to implement it yourself directly, or you may use the WRL Callback function that is used in the following WebView2 code snippet.</span></span>  

```cpp
// Register a handler for the NavigationCompleted event.
// Check whether the navigation succeeded, and if not, do something.
// Also update the Cancel buttons.
CHECK_FAILURE(m_webView->add_NavigationCompleted(
    Callback<ICoreWebView2NavigationCompletedEventHandler>(
        [this](ICoreWebView2* sender, ICoreWebView2NavigationCompletedEventArgs* args)
            -> HRESULT {
            BOOL success;
            CHECK_FAILURE(args->get_IsSuccess(&success));
            if (!success)
            {
                COREWEBVIEW2_WEB_ERROR_STATUS webErrorStatus;
                CHECK_FAILURE(args->get_WebErrorStatus(&webErrorStatus));
                if (webErrorStatus == COREWEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED)
                {
                    // Do something here if you want to handle a specific error case.
                    // In most cases it is not necessary, because the WebView
                    // displays an error page automatically.
                }
            }
            m_toolbar->SetItemEnabled(Toolbar::Item_CancelButton, false);
            m_toolbar->SetItemEnabled(Toolbar::Item_ReloadButton, true);
            return S_OK;
        })
        .Get(),
    &m_navigationCompletedToken));
```  

## <span data-ttu-id="bc89f-133">Строковых</span><span class="sxs-lookup"><span data-stu-id="bc89f-133">Strings</span></span>  

<span data-ttu-id="bc89f-134">Выходными параметрами строки являются `LPWSTR` строки, заканчивающиеся нулем.</span><span class="sxs-lookup"><span data-stu-id="bc89f-134">String out parameters are `LPWSTR` null-terminated strings.</span></span>  <span data-ttu-id="bc89f-135">Инициатор запроса выделяет строку с помощью `CoTaskMemAlloc` .</span><span class="sxs-lookup"><span data-stu-id="bc89f-135">The requester allocates the string using `CoTaskMemAlloc`.</span></span>  <span data-ttu-id="bc89f-136">Владение передается инициатору запроса, и он может использовать инициатор запроса, чтобы освободить память `CoTaskMemFree` .</span><span class="sxs-lookup"><span data-stu-id="bc89f-136">Ownership is transferred to the requester and it is up to the requester to free the memory using `CoTaskMemFree`.</span></span>  

<span data-ttu-id="bc89f-137">Строка in в параметрах — это `LPCWSTR` строки, заканчивающиеся нулем.</span><span class="sxs-lookup"><span data-stu-id="bc89f-137">String in parameters are `LPCWSTR` null-terminated strings.</span></span>  <span data-ttu-id="bc89f-138">Автор запроса гарантирует допустимость строки в течение запроса синхронной функции.</span><span class="sxs-lookup"><span data-stu-id="bc89f-138">The requester ensures the string is valid for the duration of the synchronous function request.</span></span>  <span data-ttu-id="bc89f-139">Если получатель должен сохранить это значение в некоторой точке после завершения запроса функции, получатель должен выделять связанную копию строкового значения.</span><span class="sxs-lookup"><span data-stu-id="bc89f-139">If the receiver must retain that value to some point after the function request completes, the receiver must allocate an associated copy of the string value.</span></span>  

## <span data-ttu-id="bc89f-140">Синтаксический анализ URI и JSON</span><span class="sxs-lookup"><span data-stu-id="bc89f-140">URI and JSON parsing</span></span>  

<span data-ttu-id="bc89f-141">Различные методы предоставляют или допускают URI и JSON в виде строк.</span><span class="sxs-lookup"><span data-stu-id="bc89f-141">Various methods provide or accept URIs and JSON as strings.</span></span>  <span data-ttu-id="bc89f-142">Для синтаксического анализа и создания строк используйте собственную библиотеку предпочтительных.</span><span class="sxs-lookup"><span data-stu-id="bc89f-142">Please use your own preferred library for parsing and generating the strings.</span></span>  

<span data-ttu-id="bc89f-143">Если приложение WinRT доступно для вашего приложения, вы можете использовать `RuntimeClass_Windows_Data_Json_JsonObject` методы и `IJsonObjectStatics` для синтаксического анализа или создания строк или `RuntimeClass_Windows_Foundation_Uri` `IUriRuntimeClassFactory` методов JSON для синтаксического анализа и создания URI.</span><span class="sxs-lookup"><span data-stu-id="bc89f-143">If WinRT is available for your app, you may use the `RuntimeClass_Windows_Data_Json_JsonObject` and `IJsonObjectStatics` methods to parse or produce JSON strings or `RuntimeClass_Windows_Foundation_Uri` and `IUriRuntimeClassFactory` methods to parse and produce URIs.</span></span>  <span data-ttu-id="bc89f-144">Оба метода работают в приложениях Win32.</span><span class="sxs-lookup"><span data-stu-id="bc89f-144">Both of methods work in Win32 apps.</span></span>  

<span data-ttu-id="bc89f-145">Если вы используете `IUri` и `CreateUri` проанализируете URI, вам может потребоваться использовать следующие флаги создания URI для `CreateUri` более точного соответствия синтаксическому анализу URI в WebView.</span><span class="sxs-lookup"><span data-stu-id="bc89f-145">If you use `IUri` and `CreateUri` to parse URIs, you may want to use the following URI creation flags to have `CreateUri` behavior more closely match the URI parsing in the WebView.</span></span>  

```json
Uri_CREATE_ALLOW_IMPLICIT_FILE_SCHEME | Uri_CREATE_NO_DECODE_EXTRA_INFO
```  

<!-- links -->  

[Webview2ReferenceWin32Icorewebview2CapturePreview]: /microsoft-edge/webview2/reference/win32/icorewebview2#capturepreview "CapturePreview-Interface ICoreWebView2 | Документы Microsoft"  

[CppCxWrlCallbackFunction]: /cpp/cppcx/wrl/callback-function-wrl "Функция обратного вызова (WRL) | Документы Microsoft"  
