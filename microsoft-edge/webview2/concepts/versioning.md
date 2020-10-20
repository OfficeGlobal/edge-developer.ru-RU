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
# <span data-ttu-id="16d03-104">Общие сведения о версиях SDK для WebView2</span><span class="sxs-lookup"><span data-stu-id="16d03-104">Understand WebView2 SDK versions</span></span>  

<span data-ttu-id="16d03-105">Чтобы разработать приложение WebView2, необходимо установить либо [среду выполнения WebView2][MicrosoftDeveloperEdgeWebview2] , либо [нестабильный канал Microsoft Edge][MicrosoftedgeinsiderDownload].</span><span class="sxs-lookup"><span data-stu-id="16d03-105">To develop a WebView2 application, you must install either the [WebView2 Runtime][MicrosoftDeveloperEdgeWebview2] or a [non-stable Microsoft Edge channel][MicrosoftedgeinsiderDownload].</span></span>  <span data-ttu-id="16d03-106">Минимальная требуемая версия включена в версию пакета NuGet SDK.</span><span class="sxs-lookup"><span data-stu-id="16d03-106">The minimum version that's required is included in the NuGet package version of the SDK.</span></span>  <span data-ttu-id="16d03-107">Например, при использовании этого параметра `SDK package version 0.9.488` необходимо установить либо [среду выполнения WebView2][MicrosoftDeveloperEdgeWebview2] , либо [нестабильный канал Microsoft Edge][MicrosoftedgeinsiderDownload] с номером сборки 488 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="16d03-107">For example, if you use the `SDK package version 0.9.488`, then you must install either the [WebView2 Runtime][MicrosoftDeveloperEdgeWebview2] or a [non-stable Microsoft Edge channel][MicrosoftedgeinsiderDownload] with a build number of 488 or later.</span></span>  <span data-ttu-id="16d03-108">Минимальная требуемая версия также указывается в [заметках о выпуске][Releasenotes]WebView2.</span><span class="sxs-lookup"><span data-stu-id="16d03-108">The minimum version required is also specified in the WebView2 [Release Notes][Releasenotes].</span></span>  <span data-ttu-id="16d03-109">Новые версии пакета WebView2 SDK поставляются в тот же Общий тариф, что и браузер Microsoft Edge \ (Chromium \), примерно каждые шесть недель.</span><span class="sxs-lookup"><span data-stu-id="16d03-109">New versions of the WebView2 SDK are shipped at the same general cadence as the Microsoft Edge \(Chromium\) browser, which is approximately every six weeks.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="16d03-110">При разработке приложений Evergreen WebView2 регулярно проверяйте приложение на соответствие последним версиям среды выполнения WebView2 и нестабильным браузерам Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="16d03-110">When developing Evergreen WebView2 applications, regularly test your application against the latest versions of the WebView2 Runtime and non-stable Microsoft Edge browsers.</span></span>  <span data-ttu-id="16d03-111">Поскольку веб-платформа постоянно развивается, регулярное тестирование является лучшим способом обеспечения надлежащей работы приложения.</span><span class="sxs-lookup"><span data-stu-id="16d03-111">Because the web platform is constantly evolving, regular testing is the best way to ensure your application performs as intended.</span></span>  

## <span data-ttu-id="16d03-112">Выпуск и предварительная версия пакета</span><span class="sxs-lookup"><span data-stu-id="16d03-112">Release and prerelease package</span></span>  

<span data-ttu-id="16d03-113">Пакет NuGet WebView2 включает в себя пакет для выпуска и предварительной версии.</span><span class="sxs-lookup"><span data-stu-id="16d03-113">The WebView2 NuGet package contains both a release and pre-release package.</span></span>  

<span data-ttu-id="16d03-114">Пакет выпусков совместим с переадресацией и содержит [API-интерфейсы C/C++ для Win32][ReferenceWin32].</span><span class="sxs-lookup"><span data-stu-id="16d03-114">The release package is forward compatible and contains the [Win32 C/C++ APIs][ReferenceWin32].</span></span>  <span data-ttu-id="16d03-115">API в этом SDK полностью поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="16d03-115">APIs in this SDK are fully supported.</span></span>  

<span data-ttu-id="16d03-116">Пакет предварительной версии — это надмножество пакета выпуска с дополнительными компонентами, перечисленными ниже.</span><span class="sxs-lookup"><span data-stu-id="16d03-116">The prerelease package is a superset of the release package with the additional components listed below.</span></span>  

*   <span data-ttu-id="16d03-117">API-интерфейсы .NET: [WPF][DotnetMicrosoftWebWebview2WpfNamespace], [WinForms][DotnetMicrosoftWebWebview2WinformsNamespace]и [ядро][DotnetMicrosoftWebWebview2CoreNamespace]</span><span class="sxs-lookup"><span data-stu-id="16d03-117">.NET APIs: [WPF][DotnetMicrosoftWebWebview2WpfNamespace], [WinForms][DotnetMicrosoftWebWebview2WinformsNamespace], and [Core][DotnetMicrosoftWebWebview2CoreNamespace]</span></span>  
*   <span data-ttu-id="16d03-118">Экспериментальные API-интерфейсы: Дополнительные сведения можно найти в разделе [экспериментальные API-интерфейсы](#experimental-apis) .</span><span class="sxs-lookup"><span data-stu-id="16d03-118">Experimental APIs:  For more information, navigate to the [Experimental APIs](#experimental-apis) section.</span></span>  

## <span data-ttu-id="16d03-119">Экспериментальные API-интерфейсы</span><span class="sxs-lookup"><span data-stu-id="16d03-119">Experimental APIs</span></span>  

<span data-ttu-id="16d03-120">Команда WebView тестирует экспериментальные API-интерфейсы, которые могут быть включены в будущие выпуски.</span><span class="sxs-lookup"><span data-stu-id="16d03-120">The WebView team is testing experimental APIs that may be included in future releases.</span></span>  <span data-ttu-id="16d03-121">Экспериментальные API-интерфейсы помечены как `experimental` в SDK.</span><span class="sxs-lookup"><span data-stu-id="16d03-121">The experimental APIs are marked as `experimental` in the SDK.</span></span>  <span data-ttu-id="16d03-122">Экспериментальные API-интерфейсы могут поставляться в пакете выпуска как полностью стабильные API-интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="16d03-122">Experimental APIs may ship as fully stable APIs in the release package.</span></span>  <span data-ttu-id="16d03-123">Вы можете оценить экспериментальные API-интерфейсы и поделиться обратной связью с помощью [репозитория обратной связи WebView][GithubMicrosoftedgeWebviewfeedback].</span><span class="sxs-lookup"><span data-stu-id="16d03-123">You can evaluate the Experimental APIs and share feedback using the [WebView feedback repo][GithubMicrosoftedgeWebviewfeedback].</span></span>  

> [!CAUTION]
> <span data-ttu-id="16d03-124">Старайтесь не использовать экспериментальные API в производственных приложениях.</span><span class="sxs-lookup"><span data-stu-id="16d03-124">Avoid using the experimental APIs in production apps.</span></span>  

## <span data-ttu-id="16d03-125">Соответствие версий среды выполнения WebView2</span><span class="sxs-lookup"><span data-stu-id="16d03-125">Matching WebView2 Runtime versions</span></span>  

<span data-ttu-id="16d03-126">При написании приложения WebView2 с использованием определенной версии SDK пользователи вашего приложения могут запускать ее с несколькими совместимыми версиями среды выполнения WebView2.</span><span class="sxs-lookup"><span data-stu-id="16d03-126">When writing a WebView2 app using a particular SDK version, users of your app may run it with several compatible versions of the WebView2 Runtime.</span></span>  <span data-ttu-id="16d03-127">Группа WebView работает над совместимой версией среды выполнения WebView2, которая содержит неэкспериментальные API-интерфейсы из предыдущих версий среды выполнения и новых API, не являющихся экспериментальными.</span><span class="sxs-lookup"><span data-stu-id="16d03-127">The WebView team is working on a compatible WebView2 Runtime version that contains non-experimental APIs from previous versions of the Runtime and new non-experimental APIs.</span></span>  

<span data-ttu-id="16d03-128">В зависимости от того, какой пакет SDK вы используете, рассматривайте следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="16d03-128">Depending on which SDK you use, consider the following items:</span></span> 

*   <span data-ttu-id="16d03-129">**Win32 C/C++**.</span><span class="sxs-lookup"><span data-stu-id="16d03-129">**Win32 C/C++**.</span></span>  <span data-ttu-id="16d03-130">При использовании `QueryInterface` для получения нового интерфейса проверьте возвращаемое значение `E_NOINTERFACE` .</span><span class="sxs-lookup"><span data-stu-id="16d03-130">When using `QueryInterface` to obtain a new interface, check for a return value of `E_NOINTERFACE`.</span></span>  <span data-ttu-id="16d03-131">Это значение может указывать на то, что среда выполнения WebView2 является предыдущей версией и не поддерживает этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="16d03-131">This value may indicate that the WebView2 Runtime is a previous version, and doesn't support that interface.</span></span>  
*   <span data-ttu-id="16d03-132">**.NET и WinUI**.</span><span class="sxs-lookup"><span data-stu-id="16d03-132">**.NET and WinUI**.</span></span>  <span data-ttu-id="16d03-133">Проверка наличия `No such interface supported` исключения при использовании методов, свойств и событий, добавленных в последние пакеты SDK.</span><span class="sxs-lookup"><span data-stu-id="16d03-133">Check for a `No such interface supported` exception when using methods, properties, and events that were added to more recent SDKs.</span></span>  <span data-ttu-id="16d03-134">Это исключение может возникнуть, если среда выполнения WebView2 является предыдущей версией и не поддерживает эти API.</span><span class="sxs-lookup"><span data-stu-id="16d03-134">This exception may occur when the WebView2 Runtime is a previous version, and doesn't support those APIs.</span></span>  

<span data-ttu-id="16d03-135">Если API недоступен, расрешите Удаление связанного компонента или сообщите пользователям о том, что им нужно обновить свою версию среды выполнения WebView2.</span><span class="sxs-lookup"><span data-stu-id="16d03-135">If an API is unavailable, consider removing the associated feature, or inform your users that they need to update their version of the WebView2 Runtime.</span></span>  

<span data-ttu-id="16d03-136">Экспериментальные API-интерфейсы могут быть введены, изменены и удалены из SDK в SDK.</span><span class="sxs-lookup"><span data-stu-id="16d03-136">Experimental APIs may be introduced, modified, and removed from SDK to SDK.</span></span>  <span data-ttu-id="16d03-137">Экспериментальные API-интерфейсы могут быть недоступны в установленной версии среды выполнения WebView2.</span><span class="sxs-lookup"><span data-stu-id="16d03-137">Experimental APIs may not be available in your installed version of the WebView2 Runtime.</span></span>  

## <span data-ttu-id="16d03-138">Стратегия</span><span class="sxs-lookup"><span data-stu-id="16d03-138">Roadmap</span></span>  

<span data-ttu-id="16d03-139">Пакет выпуска включает все стабильные, поддерживаемые API Win32 C/C++.</span><span class="sxs-lookup"><span data-stu-id="16d03-139">The release package contains all of the stable, supported Win32 C/C++ APIs.</span></span>  <span data-ttu-id="16d03-140">В будущем пакет выпуска будет содержать все стабильные, поддерживаемые API .NET, когда они становятся общедоступными.</span><span class="sxs-lookup"><span data-stu-id="16d03-140">In the future, the release package will contain all stable, supported .NET APIs when they are made generally available.</span></span>  <span data-ttu-id="16d03-141">Пакет предварительной версии включает экспериментальные API-интерфейсы, которые изменяются на основе отзыва и общего аналитического содержимого.</span><span class="sxs-lookup"><span data-stu-id="16d03-141">The prerelease package contains experimental APIs that are subject to change based upon your feedback and shared insights.</span></span>  

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
