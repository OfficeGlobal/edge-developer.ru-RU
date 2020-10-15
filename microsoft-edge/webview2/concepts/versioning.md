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
# <span data-ttu-id="b84bc-104">Общие сведения о версиях SDK для WebView2</span><span class="sxs-lookup"><span data-stu-id="b84bc-104">Understand WebView2 SDK versions</span></span>  

<span data-ttu-id="b84bc-105">WebView2 зависит от Microsoft Edge для функционирования.</span><span class="sxs-lookup"><span data-stu-id="b84bc-105">WebView2 depends on Microsoft Edge to function.</span></span>  <span data-ttu-id="b84bc-106">Для каждого WebView2 SDK требуется, чтобы была установлена минимальная версия браузера.</span><span class="sxs-lookup"><span data-stu-id="b84bc-106">Each WebView2 SDK requires that a minimum browser version is installed.</span></span>  <span data-ttu-id="b84bc-107">Минимальная версия отражается в версии пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="b84bc-107">The minimum version is reflected in the package version of the SDK.</span></span>  <span data-ttu-id="b84bc-108">Например, если вы используете этот параметр `SDK package version 0.9.488` , необходимо установить Microsoft Edge с номером сборки 488 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="b84bc-108">For example, if you use the `SDK package version 0.9.488`, then you must install Microsoft Edge with a build number of 488 or later.</span></span>  <span data-ttu-id="b84bc-109">Версия браузера также указывается в [заметках о выпуске][Releasenotes]WebView2.</span><span class="sxs-lookup"><span data-stu-id="b84bc-109">The browser version is also specified in the WebView2 [Release Notes][Releasenotes].</span></span>  <span data-ttu-id="b84bc-110">Дополнительные сведения о последнем выпуске браузера Microsoft EDGE можно найти в разделе [каналы браузера][DeployedgeChannels].</span><span class="sxs-lookup"><span data-stu-id="b84bc-110">For more information about the latest release of the Microsoft Edge browser, navigate to [Browser Channels][DeployedgeChannels].</span></span>  

> [!NOTE]
> <span data-ttu-id="b84bc-111">WebView2 в настоящее время является предварительной версией.</span><span class="sxs-lookup"><span data-stu-id="b84bc-111">WebView2 is currently in preview.</span></span>  <span data-ttu-id="b84bc-112">Несмотря на то, что группа WebView стремится обеспечить обратную совместимость между версиями браузеров и пакетами SDK, она не гарантируется, так как более поздние версии браузера могут не поддерживать предыдущие версии SDK.</span><span class="sxs-lookup"><span data-stu-id="b84bc-112">While the WebView team strives to ensure backward compatibility between browser versions and SDKs, it is not guaranteed because newer versions of the browser may not support previous SDK versions.</span></span>  <span data-ttu-id="b84bc-113">Если между версиями браузеров и пакетами SDK есть коренные изменения, они задаются в [заметках о выпуске][Releasenotes].</span><span class="sxs-lookup"><span data-stu-id="b84bc-113">If there are breaking changes between browser versions and SDKs, the changes are specified in the [Release Notes][Releasenotes].</span></span>  

<span data-ttu-id="b84bc-114">В будущем группа WebView планирует изменить модель распространения для WebView2 приложений.</span><span class="sxs-lookup"><span data-stu-id="b84bc-114">In the future, the WebView team plans to change the distribution model for WebView2 apps.</span></span>  <span data-ttu-id="b84bc-115">Дополнительные сведения можно найти в [режиме распространения Evergreen][DistributionEvergreenMode].</span><span class="sxs-lookup"><span data-stu-id="b84bc-115">For more information, navigate to [Evergreen distribution mode][DistributionEvergreenMode].</span></span>  

## <span data-ttu-id="b84bc-116">Выпуск и предварительная версия пакета</span><span class="sxs-lookup"><span data-stu-id="b84bc-116">Release and prerelease package</span></span>  

<span data-ttu-id="b84bc-117">В предварительной версии пакет выпусков включает указанные ниже.</span><span class="sxs-lookup"><span data-stu-id="b84bc-117">In preview, the release package contains the following.</span></span>  

*   <span data-ttu-id="b84bc-118">[API C/C++ для Win32][ReferenceWin32]: API в SDK, которые должны оставаться прежними.</span><span class="sxs-lookup"><span data-stu-id="b84bc-118">[Win32 C/C++ APIs][ReferenceWin32]: APIs in the SDK that are expected to remain the same at GA.</span></span>  

<span data-ttu-id="b84bc-119">В предварительной версии пакет предварительного выпуска включает следующие компоненты:</span><span class="sxs-lookup"><span data-stu-id="b84bc-119">In preview, the prerelease package contains the following components.</span></span>  

*   <span data-ttu-id="b84bc-120">API-интерфейсы .NET: [WPF][DotnetMicrosoftWebWebview2WpfNamespace], [WinForms][DotnetMicrosoftWebWebview2WinformsNamespace]и [ядро][DotnetMicrosoftWebWebview2CoreNamespace]</span><span class="sxs-lookup"><span data-stu-id="b84bc-120">.NET APIs: [WPF][DotnetMicrosoftWebWebview2WpfNamespace], [WinForms][DotnetMicrosoftWebWebview2WinformsNamespace], and [Core][DotnetMicrosoftWebWebview2CoreNamespace]</span></span>  
*   <span data-ttu-id="b84bc-121">Экспериментальные API.</span><span class="sxs-lookup"><span data-stu-id="b84bc-121">Experimental APIs.</span></span>  <span data-ttu-id="b84bc-122">Дополнительные сведения можно найти в разделе [экспериментальные API-интерфейсы](#experimental-apis) .</span><span class="sxs-lookup"><span data-stu-id="b84bc-122">For more information, see the [Experimental APIs](#experimental-apis) section.</span></span>  

## <span data-ttu-id="b84bc-123">Экспериментальные API-интерфейсы</span><span class="sxs-lookup"><span data-stu-id="b84bc-123">Experimental APIs</span></span>  

<span data-ttu-id="b84bc-124">Команда WebView тестирует экспериментальные API-интерфейсы, которые могут представлять будущие функции.</span><span class="sxs-lookup"><span data-stu-id="b84bc-124">The WebView team is testing experimental APIs that may represent future functionality.</span></span>  <span data-ttu-id="b84bc-125">Экспериментальные API-интерфейсы помечены как `experimental` в SDK.</span><span class="sxs-lookup"><span data-stu-id="b84bc-125">The experimental APIs are marked as `experimental` in the SDK.</span></span>  <span data-ttu-id="b84bc-126">Экспериментальные API-интерфейсы могут поставляться в пакете выпуска как полностью стабильные API-интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="b84bc-126">Experimental APIs may ship as fully stable APIs in the release package.</span></span>  <span data-ttu-id="b84bc-127">Вы должны ожидать, что все экспериментальные API будут изменяться перед выпуском.</span><span class="sxs-lookup"><span data-stu-id="b84bc-127">You should expect all experimental APIs to change before release.</span></span>  <span data-ttu-id="b84bc-128">Пожалуйста, оцените экспериментальные API-интерфейсы и поделитесь отзывами с помощью [WebViewа обратной связи][GithubMicrosoftedgeWebviewfeedback].</span><span class="sxs-lookup"><span data-stu-id="b84bc-128">Please evaluate the Experimental APIs and share feedback using the [WebView feedback repo][GithubMicrosoftedgeWebviewfeedback].</span></span>  

> [!CAUTION]
> <span data-ttu-id="b84bc-129">Старайтесь не использовать экспериментальные API в производственных приложениях.</span><span class="sxs-lookup"><span data-stu-id="b84bc-129">Avoid using the experimental APIs in production apps.</span></span>  

## <span data-ttu-id="b84bc-130">Соответствие версий среды выполнения WebView2</span><span class="sxs-lookup"><span data-stu-id="b84bc-130">Matching WebView2 Runtime versions</span></span>  

<span data-ttu-id="b84bc-131">При написании приложения WebView2 с использованием определенной версии SDK приложение Users может работать с различными совместимыми версиями среды выполнения WebView2.</span><span class="sxs-lookup"><span data-stu-id="b84bc-131">When writing a WebView2 app using a particular SDK version, the users fo you app may run your it with various compatible versions of the WebView2 Runtime.</span></span>  <span data-ttu-id="b84bc-132">В будущем новая совместимая версия среды выполнения WebView2 включает все неэкспериментальные API-интерфейсы из устаревшей совместимой версии среды выполнения WebView2 и дополнительные новые API-интерфейсы, не являющиеся экспериментальными.</span><span class="sxs-lookup"><span data-stu-id="b84bc-132">In the future, a newer compatible WebView2 Runtime version contains all the non-experimental APIs from an older compatible WebView2 Runtime version plus additional new non-experimental APIs.</span></span>  

*   <span data-ttu-id="b84bc-133">Разработчики **C/C++** при использовании `QueryInterface` для получения нового интерфейса должны проверить возвращаемое значение `E_NOINTERFACE` , которое может указывать на то, что среда выполнения WebView2 является устаревшей и не поддерживает этот конкретный интерфейс.</span><span class="sxs-lookup"><span data-stu-id="b84bc-133">**Win32 C/C++** developers, when using `QueryInterface` to obtain a new interface, should check for a return value of `E_NOINTERFACE`, which may indicate that the WebView2 Runtime is older and does not support that particular interface.</span></span>  
*   <span data-ttu-id="b84bc-134">Разработчики **.NET и WinUI** должны проверять наличие `No such interface supported` исключений при использовании методов, свойств и событий, добавленных в последующих пакетах SDK, которые могут возникать, если среда выполнения WebView2 является устаревшей и не поддерживает эти интерфейсы API.</span><span class="sxs-lookup"><span data-stu-id="b84bc-134">**.NET and WinUI** developers should check for a `No such interface supported` exception when using methods, properties, and events added in later SDKs which may occur when the WebView2 Runtime is older and does not support those particular APIs.</span></span>  

<span data-ttu-id="b84bc-135">Если API недоступен, расрешите отключение связанного компонента, если это возможно, или иным образом информирует конечного пользователя о необходимости обновления версии среды выполнения WebView2.</span><span class="sxs-lookup"><span data-stu-id="b84bc-135">If an API is unavailable, consider disabling the associated feature, if possible, or otherwise informing the end user they need to update their WebView2 Runtime version.</span></span>  

<span data-ttu-id="b84bc-136">Экспериментальные API-интерфейсы могут быть введены, изменены и удалены из SDK в SDK.</span><span class="sxs-lookup"><span data-stu-id="b84bc-136">Experimental APIs may be introduced, modified, and removed from SDK to SDK.</span></span>  <span data-ttu-id="b84bc-137">При попытке использования экспериментального API-интерфейса, который недоступен в среде выполнения WebView2, вы можете ознакомиться с описанным выше поведением.</span><span class="sxs-lookup"><span data-stu-id="b84bc-137">When attempting to use an experimental API that is not available in the WebView2 Runtime you may observe the same previously described behavior.</span></span>  

## <span data-ttu-id="b84bc-138">Стратегия</span><span class="sxs-lookup"><span data-stu-id="b84bc-138">Roadmap</span></span>  

<span data-ttu-id="b84bc-139">После того как WebView2 пойдет в устойчивое общее доступное состояние, пакет выпуска включает все стабильные, поддерживаемые API Win32 C/C++ и .NET.</span><span class="sxs-lookup"><span data-stu-id="b84bc-139">After WebView2 reaches a stable general available state, the release package contains all of the stable, supported Win32 C/C++ and .NET APIs.</span></span>  <span data-ttu-id="b84bc-140">Пакет предварительной версии включает экспериментальные API-интерфейсы, которые изменяются на основе отзыва и общего аналитического содержимого.</span><span class="sxs-lookup"><span data-stu-id="b84bc-140">The prerelease package contains experimental APIs that are subject to change based upon your feedback and shared insights.</span></span>  

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
