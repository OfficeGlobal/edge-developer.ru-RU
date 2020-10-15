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
# Рекомендации по разработке защищенных приложений WebView2  

[Элемент управления WebView2][Webview2Main] позволяет разработчикам размещать веб-содержимое в приложениях на родном языке. При правильном использовании для размещения веб-содержимого предусмотрено несколько преимуществ, например использование пользовательского интерфейса в Интернете, доступ к функциям, совместное использование кода и межплатформенной платформы, и т. д.  Чтобы избежать уязвимостей, которые могут возникнуть при размещении веб-содержимого, не забудьте разработать приложение WebView2, чтобы точно отслеживать взаимодействие между веб-содержимым и ведущим приложением.  

1.  Считать все веб-содержимое небезопасным.  
    *   Проверка веб-сообщений и параметров объекта хоста перед использованием каждого из них, поскольку веб-сообщения и параметры могут быть неправильно сформированы \ (непреднамеренно или злонамеренно) и привести к неожиданному поведению приложения.
    *   Всегда проверяйте источник документа, который выполняется в WebView2, и оцените надежность содержимого.  
1.  Разрабатывать конкретные веб-сообщения и взаимодействия объектов Host вместо обычных прокси.  
1.  Задайте следующие параметры, чтобы ограничить функциональность веб-содержимого, изменив [ICoreWebView2Settings (Win32)][Webview2ReferenceWin32Icorewebview2settings] или [CoreWebView2Settings (.NET)][Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2settings].  
    *   `AreHostObjectsAllowed` `false` Если вы не предполагаете, что веб-контенту нужно получить доступ к объектам Host, установите значение на.  
    *   `IsWebMessageEnabled` `false` Если вы не ожидаете, что веб-содержимое будет отправлять веб-сообщения в собственное приложение, сделайте это.  
    *   `IsScriptEnabled` `false` Если вы не ожидаете, что веб-содержимое будет выполняться в сценариях (например, при отображении статического содержимого HTML).  
    *   `AreDefaultScriptDialogsEnabled` `false` Если вы не хотите, чтобы веб-содержимое отображалось `alert` или диалоговых окон не ожидалось, установите значение на `prompt` .  
1.  Ниже приведены инструкции по `NavigationStarting` `FrameNavigationStarting` обновлению параметров на основе источника новой страницы с помощью событий и.  
    1.  Чтобы запретить приложению переходить на определенные страницы, используйте события, чтобы проверить, а затем заблокировать навигацию для страниц и фреймов.  
    1.  При переходе на новую страницу может потребоваться настроить значения свойств для [ICoreWebView2Settings (Win32)][Webview2ReferenceWin32Icorewebview2settings] или [CoreWebView2Settings (.NET)][Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2settings] , как описано выше.  
1.  При переходе к новому документу используйте `ContentLoading` событие для удаления предоставленных объектов узла с помощью `RemoveHostObjectFromScript` .  

<!--## Security

Always check the Source property of the WebView before using `ExecuteScript`, `PostWebMessageAsJson`, `PostWebMessageAsString`, or any other method to send information into the WebView. The WebView may have navigated to another page via the end user interacting with the page or script in the page causing navigation. Similarly, be very careful with `AddScriptToExecuteOnDocumentCreated`. All future `navigations` run the same script and if it provides access to information intended only for a certain origin, any HTML document may have access.

When examining the result of an `ExecuteScript` method call, a `WebMessageReceived` event, always check the Source of the sender, or any other mechanism of receiving information from an HTML document in a WebView validate the URI of the HTML document is what you expect.

When constructing a message to send into a WebView, prefer using `PostWebMessageAsJson` and construct the JSON string parameter using a JSON library. This avoids any potential accidents of encoding information into a JSON string or script and ensure no attacker controlled input can modify the rest of the JSON message or run arbitrary script. -->  

<!-- links -->  

[Webview2Main]: ../index.md "Введение в Microsoft Edge WebView2 (Предварительная версия) | Документы Microsoft"  

[Webview2ReferenceWin32Icorewebview2settings]: /microsoft-edge/webview2/reference/win32/icorewebview2settings "интерфейс ICoreWebView2Settings | Документы Microsoft"  

[Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2settings]: /dotnet/api/microsoft.web.webview2.core.corewebview2settings "Класс CoreWebView2Settings (Microsoft. Web. WebView2. Core) | Документы Microsoft"  
