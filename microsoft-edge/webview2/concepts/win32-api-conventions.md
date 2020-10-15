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
# Соглашения об API для Win32 C++ WebView2  

## Асинхронные методы  

Асинхронные методы в API-интерфейсе WebView2 Win32 используют делегаты для обратного вызова, чтобы указать, когда асинхронный метод завершился, код успеха или ошибки, а также для некоторых результатов.  Последний параметр для всех асинхронных методов — указатель на интерфейс делегата, для которого предоставляется реализация.  

У интерфейса делегата есть единственный `Invoke` метод, который принимает в качестве первого параметра `HRESULT` код успеха или ошибки.  Кроме того, может быть вторым параметром, который является результатом метода, если он имеет результат.  Например, метод [ICoreWebView2:: CapturePreview][Webview2ReferenceWin32Icorewebview2CapturePreview] принимает в качестве последнего параметра `ICoreWebView2CapturePreviewCompletedHandler` указатель.  Чтобы отправить `CapturePreview` запрос на метод, необходимо предоставить экземпляр класса `ICoreWebView2CapturePreviewCompletedHandler` , который вы реализуете.  В следующем фрагменте кода используется один метод для реализации.  

```cpp
HRESULT Invoke(HRESULT result)
```  

Вы реализуете `Invoke` метод и `CoreWebView2` запрашиваете `Invoke` метод по `CapturePreview` завершении запроса.  Единственный параметр — это `HRESULT` Описание кода успеха или ошибки `CapturePreview` запроса.  

Кроме того `ICoreWebView2::ExecuteScript` , вы предоставляете экземпляр, в `ICoreWebView2ExecuteScriptCompletedHandler` котором есть `Invoke` метод, который предоставляет код успеха или ошибки `ExecuteScript` запроса, а второй параметр `resultObjectAsJson` — JSON результата выполнения сценария.  

Вы можете вручную реализовать `CompleteHandler` интерфейсы делегатов, или вы можете использовать [функцию обратного вызова WRL][CppCxWrlCallbackFunction].  Функция обратного вызова используется в следующем фрагменте кода WebView2.  

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

## Мероприятия  

События в API-интерфейсе WebView2 Win32 с `add_EventName` использованием `remove_EventName` пары "и" для подписки и отмены подписки на события.  Этот `add_EventName` метод принимает интерфейс делегата обработчика событий и возвращает для него обратное значение в `EventRegistrationToken` качестве выходного параметра.  Этот метод принимает и отменяет подписку на `remove_EventName` `EventRegistrationToken` соответствующую подписку на событие.  

Интерфейсы делегатов обработчиков событий очень сходны с интерфейсами делегатов асинхронных обработчиков.  Вы реализуете интерфейс делегата обработчика событий и `CoreWebView2` отправляете обратный вызов каждый раз при срабатывании события.  Каждый интерфейс делегата обработчика событий имеет один `Invoke` метод с параметром sender, а затем параметром аргументов события.  Отправитель — это экземпляр объекта, на который вы подписаны для событий.  Параметр args событий — это интерфейс, который содержит сведения о событиях, выполняемых в данный момент.  

Например, `NavigationCompleted` событие On `ICoreWebView2` имеет `ICoreWebView2::add_NavigationCompleted` `ICoreWebView2::remove_NavigationCompleted` пару метод и.  Когда вы запрашиваете добавить, вы предоставляете экземпляр, `ICoreWebView2NavigationCompletedEventHandler` в котором вы ранее реализовали `Invoke` метод.  При `NavigationCompleted` срабатывании события `Invoke` запрашивается метод.  Первый параметр, `ICoreWebView2` который срабатывает на `NavigationCompleted` событие.  Второй параметр, `ICoreWebView2NavigationCompletedEventArgs` содержащий сведения о том, успешно ли была выполнена Навигация и так далее.  

Точно так же, как и в случае с интерфейсом делегата "асинхронный обработчик", вы можете реализовать его напрямую, или вы можете использовать функцию обратного вызова WRL, которая используется в следующем фрагменте кода WebView2.  

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

## Строковых  

Выходными параметрами строки являются `LPWSTR` строки, заканчивающиеся нулем.  Инициатор запроса выделяет строку с помощью `CoTaskMemAlloc` .  Владение передается инициатору запроса, и он может использовать инициатор запроса, чтобы освободить память `CoTaskMemFree` .  

Строка in в параметрах — это `LPCWSTR` строки, заканчивающиеся нулем.  Автор запроса гарантирует допустимость строки в течение запроса синхронной функции.  Если получатель должен сохранить это значение в некоторой точке после завершения запроса функции, получатель должен выделять связанную копию строкового значения.  

## Синтаксический анализ URI и JSON  

Различные методы предоставляют или допускают URI и JSON в виде строк.  Для синтаксического анализа и создания строк используйте собственную библиотеку предпочтительных.  

Если приложение WinRT доступно для вашего приложения, вы можете использовать `RuntimeClass_Windows_Data_Json_JsonObject` методы и `IJsonObjectStatics` для синтаксического анализа или создания строк или `RuntimeClass_Windows_Foundation_Uri` `IUriRuntimeClassFactory` методов JSON для синтаксического анализа и создания URI.  Оба метода работают в приложениях Win32.  

Если вы используете `IUri` и `CreateUri` проанализируете URI, вам может потребоваться использовать следующие флаги создания URI для `CreateUri` более точного соответствия синтаксическому анализу URI в WebView.  

```json
Uri_CREATE_ALLOW_IMPLICIT_FILE_SCHEME | Uri_CREATE_NO_DECODE_EXTRA_INFO
```  

<!-- links -->  

[Webview2ReferenceWin32Icorewebview2CapturePreview]: /microsoft-edge/webview2/reference/win32/icorewebview2#capturepreview "CapturePreview-Interface ICoreWebView2 | Документы Microsoft"  

[CppCxWrlCallbackFunction]: /cpp/cppcx/wrl/callback-function-wrl "Функция обратного вызова (WRL) | Документы Microsoft"  
