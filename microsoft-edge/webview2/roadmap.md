---
description: Узнайте о том, что дальше в WebView2
title: План для Microsoft Edge WebView 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 52a2f6d9ef3447955554a5507c3eaab39e6b6a9e
ms.sourcegitcommit: af91bfc3e6d8afc51f0fbbc0fe392262f424225c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/19/2020
ms.locfileid: "11120370"
---
# <span data-ttu-id="eb82d-104">WebView2ная схема Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="eb82d-104">Microsoft Edge WebView2 roadmap</span></span>  

##### <span data-ttu-id="eb82d-105">Последнее обновление: Oct 2020</span><span class="sxs-lookup"><span data-stu-id="eb82d-105">Last Updated: Oct 2020</span></span>  

<span data-ttu-id="eb82d-106">Элемент управления WebView2 позволяет разработчикам внедрять веб-технологии в собственные приложения.</span><span class="sxs-lookup"><span data-stu-id="eb82d-106">The WebView2 control allows developers to embed web technologies in their native applications.</span></span>  <span data-ttu-id="eb82d-107">На следующей странице приведена схема перспективной схемы для WebView2.</span><span class="sxs-lookup"><span data-stu-id="eb82d-107">The following page outlines the prospective roadmap for WebView2.</span></span>  

> [!NOTE]
> <span data-ttu-id="eb82d-108">WebView2 находится в активном состоянии, а план продолжает развиваться, основываясь на изменениях рынка и отзывах пользователей, поэтому обратите внимание на то, что описанные здесь планы не являются исчерпывающими, и их может изменить.</span><span class="sxs-lookup"><span data-stu-id="eb82d-108">WebView2 is under active development and the roadmap continues to evolve based on market changes and customer feedback, so please note that the plans outlined here are not exhaustive and are subject to change.</span></span>  

<span data-ttu-id="eb82d-109">Если у вас есть проблемы или вопросы по поводу плана, предоставьте отзыв в [репозитории обратной связи][GithubMicrosoftedgeWebviewfeedbackMain].</span><span class="sxs-lookup"><span data-stu-id="eb82d-109">If you have concerns or questions about the Roadmap, provide your feedback in the [feedback repo][GithubMicrosoftedgeWebviewfeedbackMain].</span></span>  

<span data-ttu-id="eb82d-110">Для будущих обновлений группа разработчиков WebView2 планирует следующие основные усилия.</span><span class="sxs-lookup"><span data-stu-id="eb82d-110">The WebView2 team is planning the following major efforts for future updates.</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="eb82d-111">Установщик среды выполнения WebView2</span><span class="sxs-lookup"><span data-stu-id="eb82d-111">WebView2 Runtime Installer</span></span>  
   :::column-end:::
   :::column span="2":::
      *   <span data-ttu-id="eb82d-112">4 квартал 2020</span><span class="sxs-lookup"><span data-stu-id="eb82d-112">Q4 2020</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      <span data-ttu-id="eb82d-113">Фиксированная версия</span><span class="sxs-lookup"><span data-stu-id="eb82d-113">Fixed Version</span></span>  
   :::column-end:::
   :::column span="2":::
      *   <span data-ttu-id="eb82d-114">4 квартал 2020</span><span class="sxs-lookup"><span data-stu-id="eb82d-114">Q4 2020</span></span>  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      <span data-ttu-id="eb82d-115">Общая доступность</span><span class="sxs-lookup"><span data-stu-id="eb82d-115">General Availability</span></span>  
   :::column-end:::
   :::column span="2":::
      *   <span data-ttu-id="eb82d-116">Win32 C/C++ \ (Q4 2020 \)</span><span class="sxs-lookup"><span data-stu-id="eb82d-116">Win32 C/C++ \(Q4 2020\)</span></span>  
      *   <span data-ttu-id="eb82d-117">.NET \ (Q4 2020 \)</span><span class="sxs-lookup"><span data-stu-id="eb82d-117">.NET \(Q4 2020\)</span></span>  
      *   [<span data-ttu-id="eb82d-118">WinUI3.0</span><span class="sxs-lookup"><span data-stu-id="eb82d-118">WinUI 3.0</span></span>][GithubMicrosoftUiXamlRoadmap]  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="eb82d-119">Среда выполнения и установщик WebView2</span><span class="sxs-lookup"><span data-stu-id="eb82d-119">WebView2 Runtime and Installer</span></span>  

<span data-ttu-id="eb82d-120">[Модель распространения Evergreen][ConceptDistributionEvergreenModel] позволяет целевому объекту или цепочке установить среду выполнения WebView2 на компьютер пользователя.</span><span class="sxs-lookup"><span data-stu-id="eb82d-120">[Evergreen distribution model][ConceptDistributionEvergreenModel] allows you to target or chain install the WebView2 Runtime onto your user's machine.</span></span>  <span data-ttu-id="eb82d-121">В среде выполнения и установщике Evergreen WebView2 достигнут общий доступ \ (GA \).</span><span class="sxs-lookup"><span data-stu-id="eb82d-121">The Evergreen WebView2 Runtime and installer has reached General Availability \(GA\).</span></span>  

## <span data-ttu-id="eb82d-122">Фиксированная версия</span><span class="sxs-lookup"><span data-stu-id="eb82d-122">Fixed version</span></span>  

<span data-ttu-id="eb82d-123">С помощью [фиксированной модели распространения версий][ConceptsDistributionFixedVersionModel] можно упаковать двоичные файлы Microsoft EDGE в собственное приложение.</span><span class="sxs-lookup"><span data-stu-id="eb82d-123">[Fixed version distribution model][ConceptsDistributionFixedVersionModel] allows you to package the Microsoft Edge binaries inside your native application.</span></span>  <span data-ttu-id="eb82d-124">В настоящее время она находится в режиме предварительного просмотра и ориентирована на ДЖй квартал 2020.</span><span class="sxs-lookup"><span data-stu-id="eb82d-124">It is currently under preview and targeted to GA Q4 2020.</span></span>  

## <span data-ttu-id="eb82d-125">Общая доступность</span><span class="sxs-lookup"><span data-stu-id="eb82d-125">General availability</span></span>  

### <span data-ttu-id="eb82d-126">Win32 C/C++</span><span class="sxs-lookup"><span data-stu-id="eb82d-126">Win32 C/C++</span></span>  

<span data-ttu-id="eb82d-127">Пакет SDK для Win32 C/C++ достиг GA.</span><span class="sxs-lookup"><span data-stu-id="eb82d-127">The Win32 C/C++ SDK has reached GA.</span></span>  

### <span data-ttu-id="eb82d-128">.NET</span><span class="sxs-lookup"><span data-stu-id="eb82d-128">.NET</span></span>  

<span data-ttu-id="eb82d-129">.NET SDK упаковывает пакет SDK C/C++ для Win32.</span><span class="sxs-lookup"><span data-stu-id="eb82d-129">The .NET SDK wraps the Win32 C/C++ SDK.</span></span>  <span data-ttu-id="eb82d-130">Предполагается, что пакет .NET SDK вскоре скоро будет после того, как Win32 C/C++ GA в 4 квартале 2020.</span><span class="sxs-lookup"><span data-stu-id="eb82d-130">The .NET SDK is expected to GA shortly after the Win32 C/C++ GA in Q4 2020.</span></span>  

### <span data-ttu-id="eb82d-131">WinUI3.0</span><span class="sxs-lookup"><span data-stu-id="eb82d-131">WinUI 3.0</span></span>  

<span data-ttu-id="eb82d-132">Вы можете получить доступ к WebView2 в приложениях UWP с помощью [Win UI 3,0][UwpToolkitsWinui3Index], в настоящее время в Alpha.</span><span class="sxs-lookup"><span data-stu-id="eb82d-132">You are able to access WebView2 in your UWP applications using [Win UI 3.0][UwpToolkitsWinui3Index], currently in alpha.</span></span>  <span data-ttu-id="eb82d-133">Дополнительные сведения о том, как своевременно поддерживаться, можно найти в разделе [планы библиотеки пользовательского интерфейса Windows][GithubMicrosoftUiXamlRoadmap].</span><span class="sxs-lookup"><span data-stu-id="eb82d-133">For more information about keeping up to date, see [Windows UI Library Roadmap][GithubMicrosoftUiXamlRoadmap].</span></span>  

<!-- links -->  

[ConceptDistributionEvergreenModel]: ./concepts/distribution.md#evergreen-distribution-mode "Модель распространения Evergreen — распространение приложений с помощью WebView2 | Документы Microsoft"  
[ConceptsDistributionFixedVersionModel]: ./concepts/distribution.md#fixed-version-distribution-mode "Стандартная модель распространения версий — распространение приложений с помощью WebView2 | Документы Microsoft"  

[UwpToolkitsWinui3Index]: /uwp/toolkits/winui3/index "Библиотека пользовательского интерфейса Windows 3,0 Preview 1 (Май 2020) | Документы Microsoft"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView Feedback-MicrosoftEdge/WebViewFeedback | GitHub"  

[GithubMicrosoftUiXamlRoadmap]: https://github.com/microsoft/microsoft-ui-xaml/blob/master/docs/roadmap.md "План библиотеки пользовательского интерфейса Windows — Microsoft/Microsoft-UI-XAML | GitHub"  
