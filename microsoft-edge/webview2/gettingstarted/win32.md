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
# Начало работы с WebView2  

Приведенное ниже содержимое познакомит вас с помощью часто используемых функций [WebView2][Webview2Index] и предоставляет отправную точку для создания первого приложения WebView2.  Дополнительные сведения об индивидуальных API WebView2 можно найти в [справочнике API][Webview2ReferenceWin32].  

## Предварительные условия  

*   [WebView2][Webview2Installer] или любой [Microsoft EDGE (Chromium), который не является стабильным каналом][MicrosoftedgeinsiderDownload] , установленным в поддерживаемой ОС \ (в настоящее время windows 10, Windows 8,1 и Windows 7).  
    
    > [!NOTE]
    > Группа WebView рекомендует использовать канал Канарские и минимальную требуемую версию — 82.0.488.0.  
    
*   [Visual Studio][MicrosoftVisualstudioMain] 2015 или более поздней версии с установленной поддержкой C++.  

## Шаг 1: создание приложения Win32 с одним окном  

Начните с базового проекта для настольных компьютеров, содержащего одно главное окно.  Чтобы лучше сосредоточиться на пошаговом руководстве, вы используете модифицированный образец кода из [пошагового руководства: создание традиционного классического приложения для Windows (C++)][CppWindowsWalkthroughCreatingDesktopApplication] для примера приложения.  Чтобы загрузить модифицированный образец и начать работу, перейдите в [WebView2 Samples][GithubMicrosoftedgeWebview2samplesGettingStartedGuide].  

В Visual Studio откройте `WebView2GettingStarted.sln` .  Если вы используете более старую версию Visual Studio, наведите указатель мыши на проект **WebView2GettingStarted** , откройте контекстное меню (щелкните правой кнопкой мыши \) и выберите пункт **свойства**.  В разделе **Свойства конфигурации**  >  **Общие**измените **версию Windows SDK** и **набор инструментов платформы** , чтобы использовать пакет SDK Win10 и Visual Studio Tools \ (набор инструментов VS).  

:::image type="complex" source="../media/tool-version.png" alt-text="Версия инструмента" lightbox="../media/tool-version.png":::
   Версия инструмента  
:::image-end:::  

Visual Studio может показывать некоторые ошибки из-за отсутствующего файла заголовка WebView2, который должен выйти после завершения действия 2.  

## Шаг 2. Установка WebView2 SDK  

Добавьте в проект WebView2 SDK.  Вы можете установить пакет SDK для Win32 с помощью NuGet.  

1.  Наведите указатель мыши на проект, откройте контекстное меню (щелкните правой кнопкой мыши \) и выберите пункт **Управление пакетами NuGet**.  
    
    :::image type="complex" source="../media/manage-nuget-packages.png" alt-text="Версия инструмента" lightbox="../media/manage-nuget-packages.png":::
       Управление пакетами NuGet  
    :::image-end:::  
    
1.  Установите библиотеку реализации Windows.  
    1.  Введите `Microsoft.Windows.ImplementationLibrary` в строке поиска параметр **Microsoft. Windows. ImplementationLibrary** и выберите пункт **установить** в правой части окна.  NuGet загрузит пакет SDK на ваш компьютер.  
        
        > [!NOTE] 
        > Библиотека [реализации Windows][GithubMicrosoftWilMain] и [Библиотека шаблонов C++ среды выполнения Windows][CppCxWrlTemplateLibraryVS2019] являются необязательными и добавлены для УПРОЩЕНия работы с COM в этом примере.  
        
        :::image type="complex" source="../media/wil.png" alt-text="Версия инструмента" lightbox="../media/wil.png":::
           Библиотека реализации Windows  
        :::image-end:::  
        
1.  Установите пакет SDK для WebView2.  
    1.  Введите `Microsoft.Web.WebView2` в строке поиска параметр **Microsoft. Web. WebView2** и выберите пункт **установить** в правой части окна.  NuGet загрузит пакет SDK на ваш компьютер.  
        
        :::image type="complex" source="../media/nuget.png" alt-text="Версия инструмента" lightbox="../media/nuget.png":::
           Диспетчер пакетов NuGet
        :::image-end:::  
        
1.  Добавьте в проект заголовок WebView2.  
    :::row:::
       :::column span="1":::
          `HelloWebView.cpp`Скопируйте приведенный ниже фрагмент кода и вставьте его `HelloWebView.cpp` после последней `#include` строки.  
          
          ```cpp
          // include WebView2 header
          #include "WebView2.h"
          ```  
       :::column-end:::
       :::column span="1":::
          Раздел включения должен выглядеть так, как показано в следующем фрагменте кода.  
          
          ```cpp
          ...
          #include <wrl.h>
          #include <wil/com.h>
          // include WebView2 header
          #include "WebView2.h"
          ```  
       :::column-end:::
    :::row-end:::
    
Все готово для использования и сборки в API WebView2.  

### Создание пустого примера приложения  

Выберите `F5` для сборки и запуска примера приложения.  Откроется пустое окно приложения.  

:::image type="complex" source="../media/empty-app.png" alt-text="Версия инструмента" lightbox="../media/empty-app.png":::
   Пустое приложение  
:::image-end:::  

## Шаг 3: создание единого WebView в родительском окне  

Добавьте WebView в главное окно.  Используйте этот `CreateCoreWebView2Environment` метод для настройки среды и поиска в браузере Microsoft Edge \ (Chromium \) включения и выключения элемента управления.  Кроме того, вы можете использовать этот `CreateCoreWebView2EnvironmentWithOptions` метод, если вы хотите указать расположение браузера, папку пользователя, флаги браузера и т. д., вместо использования параметра по умолчанию.  После завершения `CreateCoreWebView2Environment` метода вы можете выполнить `ICoreWebView2Environment::CreateCoreWebView2Controller` метод в `ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler` обратном вызове и выполнить `ICoreWebView2Controller::get_CoreWebView2` метод для получения связанного WebView.  

В обратном вызове задайте несколько дополнительных параметров, измените размер WebView, чтобы получить 100% родительского окна, и перейдите в Bing.  

Скопируйте приведенный ниже фрагмент кода и вставьте `HelloWebView.cpp` его после `// <-- WebView2 sample code starts here -->` заметки и перед `// <-- WebView2 sample code ends here -->` заметкой.  

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

### Создание примера приложения Bing  

Выберите `F5` , чтобы выполнить сборку и запустить приложение.  Теперь у вас есть окно WebView, в котором отображается страница Bing.  

:::image type="complex" source="../media/bing-window.png" alt-text="Версия инструмента" lightbox="../media/bing-window.png":::
   Окно Bing  
:::image-end:::  

## Шаг 4 — события навигации  

Команда WebView уже покрыла навигацию по URL-адресу, используя `ICoreWebView2::Navigate` метод на последнем этапе.  Во время навигации WebView инициирует последовательность событий, для которых узел может прослушаться.  

1.  `NavigationStarting`  
1.  `SourceChanged`  
1.  `ContentLoading`  
1.  `HistoryChanged`   
1.  `NavigationCompleted`   

Дополнительные сведения можно найти в разделе [события навигации][Webview2ConceptsNavigationEvents].  

:::image type="complex" source="../media/navigation-events.png" alt-text="Версия инструмента" lightbox="../media/navigation-events.png":::
   События навигации  
:::image-end:::  

В случае ошибок может возникнуть одно или несколько из указанных ниже событий в зависимости от того, проявляется ли переход на страницу ошибки.  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`

Если возникает Переадресация HTTP, `NavigationStarting` в строке есть несколько событий.  

В качестве примера использования событий Зарегистрируйте обработчик для `NavigationStarting` события, чтобы отменить любые запросы, не относящиеся к HTTPS.  Скопируйте приведенный ниже фрагмент кода и вставьте его в `HelloWebView.cpp` .  

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

Теперь приложение не будет перемещаться на сайты, не поддерживающие HTTPS.  Вы можете использовать сходный механизм для выполнения других задач, например для ограничения навигации в рамках собственного домена.  

## Шаг 5: создание сценариев  

Ведущее приложение может также внедрить JavaScript в WebView.  Вы можете WebView задачу, чтобы запустить произвольный сценарий JavaScript или добавить сценарии инициализации.  Добавленные сценарии инициализации применяются ко всем будущим документам верхнего уровня и дочерним элементам навигации, пока они не будут удалены.  Сценарии инициализации выполняются после создания глобального объекта и выполнения любого другого сценария, включенного в документ HTML.  

Скопируйте приведенный ниже фрагмент кода и вставьте его в `HelloWebView.cpp` .  

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

Теперь WebView должен всегда закреплять `Object` объект и возвращать документ страницы один раз.  

> [!NOTE] 
> API внедрения сценария \ (и некоторые другие API WebView2 \) являются асинхронными, следует использовать обратные вызовы, если код должен выполняться в определенном порядке.  

## Шаг 6 — взаимодействие между узлом и веб-контентом  

Основное приложение и веб-содержимое также могут взаимодействовать друг с другом через `postMessage` метод.  Веб-содержимое, запущенное в WebView, может публиковаться на узле с помощью `window.chrome.webview.postMessage` метода, а сообщение обрабатывается любым зарегистрированным `ICoreWebView2WebMessageReceivedEventHandler` обработчиком событий на узле.  Аналогичным образом ведущее приложение может выдать сообщение в виде веб-содержимого с помощью `ICoreWebView2::PostWebMessageAsString` или `ICoreWebView2::PostWebMessageAsJSON` метода, которое перехватывается обработчиками, добавленными из `window.chrome.webview.addEventListener` прослушивателя.  Механизм связи позволяет веб-контенту использовать собственные возможности путем передачи сообщений, чтобы запрашивать хост запускать собственные API.  

В качестве примера для понимания механизма можно выполнить следующие действия при печати URL-адреса документа в WebView.  

1.  Основное приложение регистрирует обработчик, чтобы вернуть полученное сообщение обратно в веб-содержимое.  
1.  Ведущее приложение вставляет сценарий в веб-содержимое, которое регистрирует обработчик для печати сообщения с узла.  
1.  Ведущее приложение вставляет сценарий в веб-содержимое, которое отправляет URL-адрес узлу.  
1.  Обработчик узла активируется и возвращает сообщение \ (URL-адрес) в веб-содержимое.  
1.  Обработчик веб-содержимого активируется и печатает сообщение от узла \ (URL-адрес)  

Скопируйте приведенный ниже фрагмент кода и вставьте его в `HelloWebView.cpp` .    

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

### Создание примера приложения "Показать URL-адрес"  

Выберите `F5` , чтобы выполнить сборку и запустить приложение.  URL-адрес отображается во всплывающем окне перед переходом на страницу.  

:::image type="complex" source="../media/show-url.png" alt-text="Версия инструмента" lightbox="../media/show-url.png":::
   Показать URL-адрес  
:::image-end:::  

Поздравляем! вы только что создали первое приложение WebView2.  

## Дальнейшие действия  

Многие функции WebView2, не описанные на этой странице, в следующем разделе представлены дополнительные ресурсы.  

### См. также  

*   Полный пример возможностей WebView2 можно найти в [примере WEBVIEW2 API][GithubMicrosoftedgeWebview2samplesApisample].  
*   Для примера приложения, созданного с помощью WebView2, перейдите на [WebView2Browser][GithubMicrosoftedgeWebview2browser].  
*   Для получения подробных сведений о API WebView2 перейдите на [ссылку API][Webview2ReferenceWin32].  

## Знакомство с командой Microsoft Edge WebView  

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
