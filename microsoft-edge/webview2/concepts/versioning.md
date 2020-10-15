---
description: Модели управления версиями, используемые для Microsoft Edge WebView2
title: Управление версиями Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/14/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения WPF, WPF, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "браузер", HTML Edge
ms.openlocfilehash: b673a2b250e46959a2eabaeb88cd8535f9a271e4
ms.sourcegitcommit: 61cc15d2fc89aee3e09cec48ef1e0e5bbf8d289a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/15/2020
ms.locfileid: "11118984"
---
# Общие сведения о версиях SDK для WebView2  

WebView2 зависит от Microsoft Edge для функционирования.  Для каждого WebView2 SDK требуется, чтобы была установлена минимальная версия браузера.  Минимальная версия отражается в версии пакета SDK.  Например, если вы используете этот параметр `SDK package version 0.9.488` , необходимо установить Microsoft Edge с номером сборки 488 или более поздней.  Версия браузера также указывается в [заметках о выпуске][Releasenotes]WebView2.  Дополнительные сведения о последнем выпуске браузера Microsoft EDGE можно найти в разделе [каналы браузера][DeployedgeChannels].  

> [!NOTE]
> WebView2 в настоящее время является предварительной версией.  Несмотря на то, что группа WebView стремится обеспечить обратную совместимость между версиями браузеров и пакетами SDK, она не гарантируется, так как более поздние версии браузера могут не поддерживать предыдущие версии SDK.  Если между версиями браузеров и пакетами SDK есть коренные изменения, они задаются в [заметках о выпуске][Releasenotes].  

В будущем группа WebView планирует изменить модель распространения для WebView2 приложений.  Дополнительные сведения можно найти в [режиме распространения Evergreen][DistributionEvergreenMode].  

## Выпуск и предварительная версия пакета  

В предварительной версии пакет выпусков включает указанные ниже.  

*   [API C/C++ для Win32][ReferenceWin32]: API в SDK, которые должны оставаться прежними.  

В предварительной версии пакет предварительного выпуска включает следующие компоненты:  

*   API-интерфейсы .NET: [WPF][DotnetMicrosoftWebWebview2WpfNamespace], [WinForms][DotnetMicrosoftWebWebview2WinformsNamespace]и [ядро][DotnetMicrosoftWebWebview2CoreNamespace]  
*   Экспериментальные API.  Дополнительные сведения можно найти в разделе [экспериментальные API-интерфейсы](#experimental-apis) .  

## Экспериментальные API-интерфейсы  

Команда WebView тестирует экспериментальные API-интерфейсы, которые могут представлять будущие функции.  Экспериментальные API-интерфейсы помечены как `experimental` в SDK.  Экспериментальные API-интерфейсы могут поставляться в пакете выпуска как полностью стабильные API-интерфейсы.  Вы должны ожидать, что все экспериментальные API будут изменяться перед выпуском.  Пожалуйста, оцените экспериментальные API-интерфейсы и поделитесь отзывами с помощью [WebViewа обратной связи][GithubMicrosoftedgeWebviewfeedback].  

> [!CAUTION]
> Старайтесь не использовать экспериментальные API в производственных приложениях.  

## Соответствие версий среды выполнения WebView2  

При написании приложения WebView2 с использованием определенной версии SDK приложение Users может работать с различными совместимыми версиями среды выполнения WebView2.  В будущем новая совместимая версия среды выполнения WebView2 включает все неэкспериментальные API-интерфейсы из устаревшей совместимой версии среды выполнения WebView2 и дополнительные новые API-интерфейсы, не являющиеся экспериментальными.  

*   Разработчики **C/C++** при использовании `QueryInterface` для получения нового интерфейса должны проверить возвращаемое значение `E_NOINTERFACE` , которое может указывать на то, что среда выполнения WebView2 является устаревшей и не поддерживает этот конкретный интерфейс.  
*   Разработчики **.NET и WinUI** должны проверять наличие `No such interface supported` исключений при использовании методов, свойств и событий, добавленных в последующих пакетах SDK, которые могут возникать, если среда выполнения WebView2 является устаревшей и не поддерживает эти интерфейсы API.  

Если API недоступен, расрешите отключение связанного компонента, если это возможно, или иным образом информирует конечного пользователя о необходимости обновления версии среды выполнения WebView2.  

Экспериментальные API-интерфейсы могут быть введены, изменены и удалены из SDK в SDK.  При попытке использования экспериментального API-интерфейса, который недоступен в среде выполнения WebView2, вы можете ознакомиться с описанным выше поведением.  

## Стратегия  

После того как WebView2 пойдет в устойчивое общее доступное состояние, пакет выпуска включает все стабильные, поддерживаемые API Win32 C/C++ и .NET.  Пакет предварительной версии включает экспериментальные API-интерфейсы, которые изменяются на основе отзыва и общего аналитического содержимого.  

<!--## Versioning  

After you have used a particular version of the SDK to build your app, your app may end up running with an older or newer version of installed browser binaries.  Until version 1.0.0.0 of WebView2 there may be breaking changes during updates that prevent your SDK from working with different versions of installed browser binaries.  After version 1.0.0.0, different versions of the SDK may work with different versions of the installed browser by using the following best practices.  

1.  To account for breaking changes to the API be sure to check for failure when requesting the DLL export `CreateCoreWebView2Environment` and when running `QueryInterface` on any `CoreWebView2` object.  A return value of `E_NOINTERFACE` indicates that the SDK is not compatible with the Microsoft Edge browser binaries.  
1.  Checking for failure from `QueryInterface` also accounts for cases where the SDK is newer than the version of the Microsoft Edge browser and your app attempts to use an interface of which the Microsoft Edge browser is unaware.  

1.  When an interface is unavailable, you may consider disabling the associated feature if possible, or otherwise informing your users to update their browsers.  -->  

<!--links -->

[DistributionEvergreenMode]: ./distribution.md#evergreen-distribution-mode "Режим распространения Evergreen — распространение приложений с помощью WebView2 | Документы Microsoft"  
[DotnetMicrosoftWebWebview2CoreNamespace]: /dotnet/api/microsoft.web.webview2.core "Пространство имен Microsoft. Web. WebView2. Core | Документы Microsoft"
[DotnetMicrosoftWebWebview2WpfNamespace]: /dotnet/api/microsoft.web.webview2.wpf "Пространство имен Microsoft. Web. WebView2. WPF | Документы Microsoft"
[DotnetMicrosoftWebWebview2WinformsNamespace]: /dotnet/api/microsoft.web.webview2.winforms "Пространство имен Microsoft. Web. WebView2. WinForms | Документы Microsoft"
[ReferenceWin32]: /microsoft-edge/webview2/reference/win32 "Справочник по WebView2 Win32 C++ | Документы Microsoft"  
[Releasenotes]: ../releasenotes.md "Заметки о выпуске для WebView2 SDK | Документы Microsoft"  

[DeployedgeChannels]: /deployedge/microsoft-edge-channels "Общие сведения о каналах Microsoft Edge | Документы Microsoft"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView Feedback-MicrosoftEdge/WebViewFeedback | GitHub"  
