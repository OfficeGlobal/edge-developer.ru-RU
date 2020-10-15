---
description: Узнайте, как разрабатывать безопасные WebView2 приложения.
title: Рекомендации по разработке защищенных приложений WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/14/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, управление браузером, EDGE HTML, безопасность
ms.openlocfilehash: d53417cc1ac98b44565692edbaec06216f7c110b
ms.sourcegitcommit: 61cc15d2fc89aee3e09cec48ef1e0e5bbf8d289a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/15/2020
ms.locfileid: "11119004"
---
# <span data-ttu-id="89899-104">Рекомендации по разработке защищенных приложений WebView2</span><span class="sxs-lookup"><span data-stu-id="89899-104">Best practices for developing secure WebView2 applications</span></span>  

<span data-ttu-id="89899-105">[Элемент управления WebView2][Webview2Main] позволяет разработчикам размещать веб-содержимое в приложениях на родном языке.</span><span class="sxs-lookup"><span data-stu-id="89899-105">The [WebView2 control][Webview2Main] allows developers to host web content in the native applications.</span></span> <span data-ttu-id="89899-106">При правильном использовании для размещения веб-содержимого предусмотрено несколько преимуществ, например использование пользовательского интерфейса в Интернете, доступ к функциям, совместное использование кода и межплатформенной платформы, и т. д.</span><span class="sxs-lookup"><span data-stu-id="89899-106">When used correctly, hosting web content offers several advantages, such as using web-based UI, accessing features of the web platform, sharing code cross-platform, and so on.</span></span>  <span data-ttu-id="89899-107">Чтобы избежать уязвимостей, которые могут возникнуть при размещении веб-содержимого, не забудьте разработать приложение WebView2, чтобы точно отслеживать взаимодействие между веб-содержимым и ведущим приложением.</span><span class="sxs-lookup"><span data-stu-id="89899-107">To avoid vulnerabilities that can arise from hosting web content, make sure to design your WebView2 application to closely monitor interactions between the web content and the host application.</span></span>  

1.  <span data-ttu-id="89899-108">Считать все веб-содержимое небезопасным.</span><span class="sxs-lookup"><span data-stu-id="89899-108">Treat all web content as insecure.</span></span>  
    *   <span data-ttu-id="89899-109">Проверка веб-сообщений и параметров объекта хоста перед использованием каждого из них, поскольку веб-сообщения и параметры могут быть неправильно сформированы \ (непреднамеренно или злонамеренно) и привести к неожиданному поведению приложения.</span><span class="sxs-lookup"><span data-stu-id="89899-109">Validate web messages and host object parameters before consuming each, because web messages and parameters can be malformed \(unintentionally or maliciously\) and cause the app to behave unexpectedly.</span></span>
    *   <span data-ttu-id="89899-110">Всегда проверяйте источник документа, который выполняется в WebView2, и оцените надежность содержимого.</span><span class="sxs-lookup"><span data-stu-id="89899-110">Always check the origin of the document running inside WebView2 and assess the trustworthiness of the content.</span></span>  
1.  <span data-ttu-id="89899-111">Разрабатывать конкретные веб-сообщения и взаимодействия объектов Host вместо обычных прокси.</span><span class="sxs-lookup"><span data-stu-id="89899-111">Design specific web messages and host object interactions instead of using generic proxies.</span></span>  
1.  <span data-ttu-id="89899-112">Задайте следующие параметры, чтобы ограничить функциональность веб-содержимого, изменив [ICoreWebView2Settings (Win32)][Webview2ReferenceWin32Icorewebview2settings] или [CoreWebView2Settings (.NET)][Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2settings].</span><span class="sxs-lookup"><span data-stu-id="89899-112">Set the following options to restrict web content functionality by modifying [ICoreWebView2Settings (Win32)][Webview2ReferenceWin32Icorewebview2settings] or [CoreWebView2Settings (.NET)][Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2settings].</span></span>  
    *   <span data-ttu-id="89899-113">`AreHostObjectsAllowed` `false` Если вы не предполагаете, что веб-контенту нужно получить доступ к объектам Host, установите значение на.</span><span class="sxs-lookup"><span data-stu-id="89899-113">Set `AreHostObjectsAllowed` to `false`, if you do not expect the web content to access host objects.</span></span>  
    *   <span data-ttu-id="89899-114">`IsWebMessageEnabled` `false` Если вы не ожидаете, что веб-содержимое будет отправлять веб-сообщения в собственное приложение, сделайте это.</span><span class="sxs-lookup"><span data-stu-id="89899-114">Set `IsWebMessageEnabled` to `false`, if you do not expect the web content to post web messages to your native application.</span></span>  
    *   <span data-ttu-id="89899-115">`IsScriptEnabled` `false` Если вы не ожидаете, что веб-содержимое будет выполняться в сценариях (например, при отображении статического содержимого HTML).</span><span class="sxs-lookup"><span data-stu-id="89899-115">Set `IsScriptEnabled` to `false`, if you do not expect the web content to run scripts \(for example, when showing static html content\).</span></span>  
    *   <span data-ttu-id="89899-116">`AreDefaultScriptDialogsEnabled` `false` Если вы не хотите, чтобы веб-содержимое отображалось `alert` или диалоговых окон не ожидалось, установите значение на `prompt` .</span><span class="sxs-lookup"><span data-stu-id="89899-116">Set `AreDefaultScriptDialogsEnabled` to `false`, if you do not expect the web content to show `alert` or `prompt` dialog boxes.</span></span>  
1.  <span data-ttu-id="89899-117">Ниже приведены инструкции по `NavigationStarting` `FrameNavigationStarting` обновлению параметров на основе источника новой страницы с помощью событий и.</span><span class="sxs-lookup"><span data-stu-id="89899-117">In the following steps, use the `NavigationStarting` and `FrameNavigationStarting` events to update settings based on the origin of the new page.</span></span>  
    1.  <span data-ttu-id="89899-118">Чтобы запретить приложению переходить на определенные страницы, используйте события, чтобы проверить, а затем заблокировать навигацию для страниц и фреймов.</span><span class="sxs-lookup"><span data-stu-id="89899-118">To prevent your application from navigating to certain pages, use the events to check and then block page or frame navigation.</span></span>  
    1.  <span data-ttu-id="89899-119">При переходе на новую страницу может потребоваться настроить значения свойств для [ICoreWebView2Settings (Win32)][Webview2ReferenceWin32Icorewebview2settings] или [CoreWebView2Settings (.NET)][Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2settings] , как описано выше.</span><span class="sxs-lookup"><span data-stu-id="89899-119">When navigating to a new page, you may need to adjust the property values on [ICoreWebView2Settings (Win32)][Webview2ReferenceWin32Icorewebview2settings] or [CoreWebView2Settings (.NET)][Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2settings] as previously described.</span></span>  
1.  <span data-ttu-id="89899-120">При переходе к новому документу используйте `ContentLoading` событие для удаления предоставленных объектов узла с помощью `RemoveHostObjectFromScript` .</span><span class="sxs-lookup"><span data-stu-id="89899-120">When navigating to a new document, use the `ContentLoading` event to remove exposed host objects using `RemoveHostObjectFromScript`.</span></span>  

<!--## Security

Always check the Source property of the WebView before using `ExecuteScript`, `PostWebMessageAsJson`, `PostWebMessageAsString`, or any other method to send information into the WebView. The WebView may have navigated to another page via the end user interacting with the page or script in the page causing navigation. Similarly, be very careful with `AddScriptToExecuteOnDocumentCreated`. All future `navigations` run the same script and if it provides access to information intended only for a certain origin, any HTML document may have access.

When examining the result of an `ExecuteScript` method call, a `WebMessageReceived` event, always check the Source of the sender, or any other mechanism of receiving information from an HTML document in a WebView validate the URI of the HTML document is what you expect.

When constructing a message to send into a WebView, prefer using `PostWebMessageAsJson` and construct the JSON string parameter using a JSON library. This avoids any potential accidents of encoding information into a JSON string or script and ensure no attacker controlled input can modify the rest of the JSON message or run arbitrary script. -->  

<!-- links -->  

[Webview2Main]: ../index.md "Введение в Microsoft Edge WebView2 (Предварительная версия) | Документы Microsoft"  

[Webview2ReferenceWin32Icorewebview2settings]: /microsoft-edge/webview2/reference/win32/icorewebview2settings "интерфейс ICoreWebView2Settings | Документы Microsoft"  

[Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2settings]: /dotnet/api/microsoft.web.webview2.core.corewebview2settings "Класс CoreWebView2Settings (Microsoft. Web. WebView2. Core) | Документы Microsoft"  
