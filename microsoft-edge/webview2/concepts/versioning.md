---
description: Модели управления версиями, используемые для Microsoft Edge WebView2
title: Управление версиями Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения WPF, WPF, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "браузер", HTML Edge
ms.openlocfilehash: a47c7295e87cf4295f8cdf898b62aa3b550aa9a5
ms.sourcegitcommit: af91bfc3e6d8afc51f0fbbc0fe392262f424225c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/19/2020
ms.locfileid: "11120341"
---
# Общие сведения о версиях SDK для WebView2  

Чтобы разработать приложение WebView2, необходимо установить либо [среду выполнения WebView2][MicrosoftDeveloperEdgeWebview2] , либо [нестабильный канал Microsoft Edge][MicrosoftedgeinsiderDownload].  Минимальная требуемая версия включена в версию пакета NuGet SDK.  Например, при использовании этого параметра `SDK package version 0.9.488` необходимо установить либо [среду выполнения WebView2][MicrosoftDeveloperEdgeWebview2] , либо [нестабильный канал Microsoft Edge][MicrosoftedgeinsiderDownload] с номером сборки 488 или более поздней.  Минимальная требуемая версия также указывается в [заметках о выпуске][Releasenotes]WebView2.  Новые версии пакета WebView2 SDK поставляются в тот же Общий тариф, что и браузер Microsoft Edge \ (Chromium \), примерно каждые шесть недель.  

> [!IMPORTANT]
> При разработке приложений Evergreen WebView2 регулярно проверяйте приложение на соответствие последним версиям среды выполнения WebView2 и нестабильным браузерам Microsoft Edge.  Поскольку веб-платформа постоянно развивается, регулярное тестирование является лучшим способом обеспечения надлежащей работы приложения.  

## Выпуск и предварительная версия пакета  

Пакет NuGet WebView2 включает в себя пакет для выпуска и предварительной версии.  

Пакет выпусков совместим с переадресацией и содержит [API-интерфейсы C/C++ для Win32][ReferenceWin32].  API в этом SDK полностью поддерживаются.  

Пакет предварительной версии — это надмножество пакета выпуска с дополнительными компонентами, перечисленными ниже.  

*   API-интерфейсы .NET: [WPF][DotnetMicrosoftWebWebview2WpfNamespace], [WinForms][DotnetMicrosoftWebWebview2WinformsNamespace]и [ядро][DotnetMicrosoftWebWebview2CoreNamespace]  
*   Экспериментальные API-интерфейсы: Дополнительные сведения можно найти в разделе [экспериментальные API-интерфейсы](#experimental-apis) .  

## Экспериментальные API-интерфейсы  

Команда WebView тестирует экспериментальные API-интерфейсы, которые могут быть включены в будущие выпуски.  Экспериментальные API-интерфейсы помечены как `experimental` в SDK.  Экспериментальные API-интерфейсы могут поставляться в пакете выпуска как полностью стабильные API-интерфейсы.  Вы можете оценить экспериментальные API-интерфейсы и поделиться обратной связью с помощью [репозитория обратной связи WebView][GithubMicrosoftedgeWebviewfeedback].  

> [!CAUTION]
> Старайтесь не использовать экспериментальные API в производственных приложениях.  

## Соответствие версий среды выполнения WebView2  

При написании приложения WebView2 с использованием определенной версии SDK пользователи вашего приложения могут запускать ее с несколькими совместимыми версиями среды выполнения WebView2.  Группа WebView работает над совместимой версией среды выполнения WebView2, которая содержит неэкспериментальные API-интерфейсы из предыдущих версий среды выполнения и новых API, не являющихся экспериментальными.  

В зависимости от того, какой пакет SDK вы используете, рассматривайте следующие элементы: 

*   **Win32 C/C++**.  При использовании `QueryInterface` для получения нового интерфейса проверьте возвращаемое значение `E_NOINTERFACE` .  Это значение может указывать на то, что среда выполнения WebView2 является предыдущей версией и не поддерживает этот интерфейс.  
*   **.NET и WinUI**.  Проверка наличия `No such interface supported` исключения при использовании методов, свойств и событий, добавленных в последние пакеты SDK.  Это исключение может возникнуть, если среда выполнения WebView2 является предыдущей версией и не поддерживает эти API.  

Если API недоступен, расрешите Удаление связанного компонента или сообщите пользователям о том, что им нужно обновить свою версию среды выполнения WebView2.  

Экспериментальные API-интерфейсы могут быть введены, изменены и удалены из SDK в SDK.  Экспериментальные API-интерфейсы могут быть недоступны в установленной версии среды выполнения WebView2.  

## Стратегия  

Пакет выпуска включает все стабильные, поддерживаемые API Win32 C/C++.  В будущем пакет выпуска будет содержать все стабильные, поддерживаемые API .NET, когда они становятся общедоступными.  Пакет предварительной версии включает экспериментальные API-интерфейсы, которые изменяются на основе отзыва и общего аналитического содержимого.  

<!--## Versioning  

After you have used a particular version of the SDK to build your app, your app may end up running with an older or newer version of installed browser binaries.  Until version 1.0.0.0 of WebView2 there may be breaking changes during updates that prevent your SDK from working with different versions of installed browser binaries.  After version 1.0.0.0, different versions of the SDK may work with different versions of the installed browser by using the following best practices.  

1.  To account for breaking changes to the API be sure to check for failure when requesting the DLL export `CreateCoreWebView2Environment` and when running `QueryInterface` on any `CoreWebView2` object.  A return value of `E_NOINTERFACE` indicates that the SDK is not compatible with the Microsoft Edge browser binaries.  
1.  Checking for failure from `QueryInterface` also accounts for cases where the SDK is newer than the version of the Microsoft Edge browser and your app attempts to use an interface of which the Microsoft Edge browser is unaware.  

1.  When an interface is unavailable, you may consider disabling the associated feature if possible, or otherwise informing your users to update their browsers.  -->  

<!--links -->  

[Releasenotes]: ../releasenotes.md "Заметки о выпуске для WebView2 SDK | Документы Microsoft"  

[DeployedgeChannels]: /deployedge/microsoft-edge-channels "Общие сведения о каналах Microsoft Edge | Документы Microsoft"  

[DotnetMicrosoftWebWebview2CoreNamespace]: /dotnet/api/microsoft.web.webview2.core "Пространство имен Microsoft. Web. WebView2. Core | Документы Microsoft"  
[DotnetMicrosoftWebWebview2WpfNamespace]: /dotnet/api/microsoft.web.webview2.wpf "Пространство имен Microsoft. Web. WebView2. WPF | Документы Microsoft"  
[DotnetMicrosoftWebWebview2WinformsNamespace]: /dotnet/api/microsoft.web.webview2.winforms "Пространство имен Microsoft. Web. WebView2. WinForms | Документы Microsoft"  
[ReferenceWin32]: /microsoft-edge/webview2/reference/win32 "Справочник по WebView2 Win32 C++ | Документы Microsoft"  

[MicrosoftDeveloperEdgeWebview2]: https://developer.microsoft.com/microsoft-edge/webview2/ "Microsoft Edge WebView2 | Разработчик Майкрософт"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView Feedback-MicrosoftEdge/WebViewFeedback | GitHub"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Скачайте каналы предварительной оценки Microsoft Edge"  
