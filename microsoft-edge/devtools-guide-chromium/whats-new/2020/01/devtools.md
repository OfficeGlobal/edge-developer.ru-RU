---
description: Трехмерное представление, интеграция Visual Studio с Microsoft EDGE и многое другое.
title: Новые возможности DevTools (Microsoft Edge 81)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 3081ebb256a9ede637aaaddc3c3cdf7a70a201bb
ms.sourcegitcommit: b337717957529239434b4e8e1e167aebf0543518
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/15/2020
ms.locfileid: "11015477"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  

# <span data-ttu-id="f3316-104">Новые возможности DevTools (Microsoft Edge 81)</span><span class="sxs-lookup"><span data-stu-id="f3316-104">What's New In DevTools (Microsoft Edge 81)</span></span>  

## <span data-ttu-id="f3316-105">Объявления из группы Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="f3316-105">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="f3316-106">В следующих разделах представлен список извещений, которые вы могли не получить в Microsoft Edge DevTools Teams!</span><span class="sxs-lookup"><span data-stu-id="f3316-106">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team!</span></span> <span data-ttu-id="f3316-107">Узнайте, как использовать новые функции в DevTools, расширения кода Visual Studio и многое другое.</span><span class="sxs-lookup"><span data-stu-id="f3316-107">Check them out to try new features in the DevTools, Visual Studio Code extensions, and more.</span></span>  <span data-ttu-id="f3316-108">Чтобы оставаться на связи с самыми последними и более свежими возможностями, скачайте на веб – [каналы предварительной версии Microsoft Edge][MicrosoftEdgePreviewChannels] и [следуйте указаниям Twitter][EdgeDevToolsTwitterAccount].</span><span class="sxs-lookup"><span data-stu-id="f3316-108">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow us on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <span data-ttu-id="f3316-109">Улучшение специальных возможностей в DevTools</span><span class="sxs-lookup"><span data-stu-id="f3316-109">Accessibility improvements to the DevTools</span></span>  

<span data-ttu-id="f3316-110">Группа DevTools изменила 170 в Chromium для устранения проблем с высокой контрастностью цвета, клавиатуры и средства чтения с экрана в DevTools.</span><span class="sxs-lookup"><span data-stu-id="f3316-110">The DevTools team has contributed 170 changes to Chromium to address high-impact color contrast, keyboard, and screen reader issues in the DevTools.</span></span>  <span data-ttu-id="f3316-111">Каждый разработчик, создающий веб-сайт, должен иметь возможность использовать DevTools.</span><span class="sxs-lookup"><span data-stu-id="f3316-111">Every developer building the web should be able to use the DevTools.</span></span>  

:::image type="complex" source="../../images/2020/01/a11y-performance-tool.msft.gif" alt-text="Средство &quot;производительность&quot; в DevTools с улучшенной навигацией с помощью клавиатуры и средства чтения с экрана" lightbox="../../images/2020/01/a11y-performance-tool.msft.gif":::
   <span data-ttu-id="f3316-113">Средство " **производительность** " в DevTools с улучшенной навигацией с помощью клавиатуры и средства чтения с экрана</span><span class="sxs-lookup"><span data-stu-id="f3316-113">The **Performance** tool in the DevTools with the keyboard navigation and screen reader improvements</span></span>  
:::image-end:::  

<span data-ttu-id="f3316-114">Сведения о том, как сделать веб-страницу доступной для всех пользователей?</span><span class="sxs-lookup"><span data-stu-id="f3316-114">Want to learn how to make your web page accessible to all of your users?</span></span>  <span data-ttu-id="f3316-115">Скачайте [расширения для][WebhintBrowserExtension] Microsoft Edge " [Специальные возможности][AccessibilityInsights] ", чтобы приступить к работе.</span><span class="sxs-lookup"><span data-stu-id="f3316-115">Download the [Accessibility Insights][AccessibilityInsights] and [webhint][WebhintBrowserExtension] extensions for Microsoft Edge to get started.</span></span>  

<span data-ttu-id="f3316-116">Если вы используете средства чтения с экрана или клавиатуру для навигации по DevTools, отправьте нам свой отзыв, выполнив [твит][PostTweetEdgeDevTools] в США или щелкнув значок [Отправить отзыв](#getting-in-touch-with-microsoft-edge-devtools-team) !</span><span class="sxs-lookup"><span data-stu-id="f3316-116">If you use screen readers or the keyboard to navigate around the DevTools, send us your feedback by [tweeting][PostTweetEdgeDevTools] at us or clicking the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="f3316-117">[#963183][CR963183] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="f3316-117">Chromium issue [#963183][CR963183]</span></span>  

### <span data-ttu-id="f3316-118">Использование DevTools на других языках</span><span class="sxs-lookup"><span data-stu-id="f3316-118">Using the DevTools in other languages</span></span>  

<span data-ttu-id="f3316-119">Многие разработчики используют другие инструменты разработчика, такие как StackOverflow и код Visual Studio, на родном языке, а не только на английском языке.</span><span class="sxs-lookup"><span data-stu-id="f3316-119">Many developers use other developer tools, like StackOverflow and Visual Studio Code, in their native language, not just in English.</span></span>  <span data-ttu-id="f3316-120">Мы рады объявить локализацию для DevTools, который теперь вы можете использовать на одном из 10 языков, кроме английского.</span><span class="sxs-lookup"><span data-stu-id="f3316-120">We’re excited to announce localization for the DevTools, which you are now able to use in one of 10 languages besides English:</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="f3316-121">Китайский (упрощенное письмо) —  &#20013;&#25991;&#65288;&#31616;&#20307;&#65289;</span><span class="sxs-lookup"><span data-stu-id="f3316-121">Chinese \(Simplified\) - &#20013;&#25991;&#65288;&#31616;&#20307;&#65289;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="f3316-122">Китайский (традиционное письмо) —  &#20013;&#25991;&#65288;&#32321;&#39636;&#65289;</span><span class="sxs-lookup"><span data-stu-id="f3316-122">Chinese \(Traditional\) - &#20013;&#25991;&#65288;&#32321;&#39636;&#65289;</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="f3316-123">Французский — Fran&#231;AIS</span><span class="sxs-lookup"><span data-stu-id="f3316-123">French – fran&#231;ais</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="f3316-124">Немецкий — Deutsch</span><span class="sxs-lookup"><span data-stu-id="f3316-124">German - deutsch</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="f3316-125">Итальянский — Italiano</span><span class="sxs-lookup"><span data-stu-id="f3316-125">Italian - italiano</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="f3316-126">Японская  &#26085;&#26412;&#35486;</span><span class="sxs-lookup"><span data-stu-id="f3316-126">Japanese - &#26085;&#26412;&#35486;</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="f3316-127">Корейский —  &#54620;&#44397;&#50612;</span><span class="sxs-lookup"><span data-stu-id="f3316-127">Korean - &#54620;&#44397;&#50612;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="f3316-128">Португальский (portugu&#234;s)</span><span class="sxs-lookup"><span data-stu-id="f3316-128">Portuguese - portugu&#234;s</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="f3316-129">Русский —  &#1088;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081;</span><span class="sxs-lookup"><span data-stu-id="f3316-129">Russian – &#1088;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="f3316-130">Испанская — ESPA&#241;OL</span><span class="sxs-lookup"><span data-stu-id="f3316-130">Spanish - espa&#241;ol</span></span>
   :::column-end:::
:::row-end:::

<!--  
|  |  |  
|:--- |:--- |  
| Chinese (Simplified) - 中文(简体)（简体）| Chinese (Traditional) - 中文(繁體)（繁體）|  
| French – français | German - deutsch |  
| Italian - italiano | Portuguese - português |  
| Korean - 한국어 | Japanese - 日本語 |  
| Russian – русский | Spanish - español |  
-->  

<span data-ttu-id="f3316-131">DevTools автоматически соответствует языку, который вы используете для Microsoft Edge in `edge://settings/languages` .</span><span class="sxs-lookup"><span data-stu-id="f3316-131">The DevTools automatically match the language you use for Microsoft Edge in `edge://settings/languages`.</span></span>  

<span data-ttu-id="f3316-132">Если вы хотите, чтобы Microsoft Edge выоставался на одном языке, а DevTools на русском языке, нажмите кнопку `F1` DevTools, чтобы открыть вкладку [Параметры][Settings] и отключить **язык браузера**.</span><span class="sxs-lookup"><span data-stu-id="f3316-132">If you want Microsoft Edge to be in one language and your DevTools to remain in English, press `F1` in the DevTools to open [Settings][Settings] and disable **Match browser language**.</span></span>  

:::image type="complex" source="../../images/2020/01/localized-devtools.msft.png" alt-text="Средство &quot;производительность&quot; в DevTools с улучшенной навигацией с помощью клавиатуры и средства чтения с экрана" lightbox="../../images/2020/01/localized-devtools.msft.png":::
   <span data-ttu-id="f3316-134">DevTools на немецком языке</span><span class="sxs-lookup"><span data-stu-id="f3316-134">The DevTools in German</span></span>  
:::image-end:::  

<span data-ttu-id="f3316-135">Сообщения **консоли** не локализуются.</span><span class="sxs-lookup"><span data-stu-id="f3316-135">**Console** messages are not localized.</span></span>  <span data-ttu-id="f3316-136">На языке, используемом для Microsoft EDGE, отображаются только строки, используемые в пользовательском интерфейсе DevTools.</span><span class="sxs-lookup"><span data-stu-id="f3316-136">Only the strings used in the DevTools UI are displayed in the language you use for Microsoft Edge.</span></span>  

<span data-ttu-id="f3316-137">Если вы хотите использовать DevTools на языке, отличном от того, на котором они доступны, [твит][PostTweetEdgeDevTools] в США или щелкните значок [Отправить отзыв](#getting-in-touch-with-microsoft-edge-devtools-team) .</span><span class="sxs-lookup"><span data-stu-id="f3316-137">If you want to use the DevTools in a different language than the ones that are available, [tweet][PostTweetEdgeDevTools] at us or click the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon.</span></span>  

<span data-ttu-id="f3316-138">[#941561][CR941561] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="f3316-138">Chromium issue [#941561][CR941561]</span></span>  

### <span data-ttu-id="f3316-139">Веб – подсказка с расширением Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="f3316-139">webhint Microsoft Edge extension</span></span>  

<span data-ttu-id="f3316-140">Расширение веб-подсказки Microsoft EDGE позволяет легко находить и получать отзывы о специальных возможностях, совместимости с браузерами, безопасности, производительности и других средствах в DevTools.</span><span class="sxs-lookup"><span data-stu-id="f3316-140">The webhint Microsoft Edge extension allows you to easily scan your web page and get feedback on accessibility, browser compatibility, security, performance, and more within the DevTools.</span></span>  <span data-ttu-id="f3316-141">Узнайте больше о [https://webhint.io][Webhint] .</span><span class="sxs-lookup"><span data-stu-id="f3316-141">Read more at [https://webhint.io][Webhint].</span></span>  

:::image type="complex" source="../../images/2020/01/webhint-browser-extension.msft.png" alt-text="Средство &quot;производительность&quot; в DevTools с улучшенной навигацией с помощью клавиатуры и средства чтения с экрана" lightbox="../../images/2020/01/webhint-browser-extension.msft.png":::
   <span data-ttu-id="f3316-143">Вкладка **"Подсказка** " в DevTools, если установлено расширение браузера веб.</span><span class="sxs-lookup"><span data-stu-id="f3316-143">The **Hints** tab in the DevTools when the webhint browser extension is installed</span></span>  
:::image-end:::  

<span data-ttu-id="f3316-144">[Попробуйте расширение браузера веб для подсказки в Microsoft Edge][MicrosoftEdgeInsiderAddons].</span><span class="sxs-lookup"><span data-stu-id="f3316-144">[Try the webhint browser extension in Microsoft Edge][MicrosoftEdgeInsiderAddons].</span></span>  <span data-ttu-id="f3316-145">После установки расширения откройте DevTools и перейдите на вкладку подсказки.  В этой статье запустите настраиваемое сканирование сайта.</span><span class="sxs-lookup"><span data-stu-id="f3316-145">Once you install the extension, open the DevTools and select the Hints tab.  From here, run a customizable site scan.</span></span>  <span data-ttu-id="f3316-146">Чтобы получить дополнительные сведения, [заwebhint.IO][WebhintBrowserExtension] в голову.</span><span class="sxs-lookup"><span data-stu-id="f3316-146">Head over to [webhint.io][WebhintBrowserExtension] to learn more.</span></span>  

### <span data-ttu-id="f3316-147">Трехмерное представление</span><span class="sxs-lookup"><span data-stu-id="f3316-147">3D View</span></span>  

<span data-ttu-id="f3316-148">С помощью **трехмерного представления** вы можете выполнять отладку своего веб-приложения, перемещаясь по [объектной модели документов \ (DOM)][MDNDocumentObjectModel] или контексту стека [z-индексов][MDNZIndex] .</span><span class="sxs-lookup"><span data-stu-id="f3316-148">Use the **3D View** to debug your web application by navigating through the [Document Object Model \(DOM\)][MDNDocumentObjectModel] or the [z-index][MDNZIndex] stacking context.</span></span>  

:::image type="complex" source="../../images/2020/01/3dview.msft.png" alt-text="Средство &quot;производительность&quot; в DevTools с улучшенной навигацией с помощью клавиатуры и средства чтения с экрана" lightbox="../../images/2020/01/3dview.msft.png":::
   <span data-ttu-id="f3316-150">Трехмерное представление в DevTools</span><span class="sxs-lookup"><span data-stu-id="f3316-150">The 3D View in the DevTools</span></span>  
:::image-end:::  

<span data-ttu-id="f3316-151">Для доступа к трехмерному представлению нажмите клавишу `Ctrl`  +  `Shift`  +  `P` Ввод в **режиме 3D-представления** и выберите **Показать 3D-представление**.</span><span class="sxs-lookup"><span data-stu-id="f3316-151">To access the 3D View, press `Ctrl` + `Shift` + `P`, type in **3D View** and select **Show 3D View**.</span></span>  

<span data-ttu-id="f3316-152">Мы работаем над ИНТЕРФЕЙСом и добавляем дополнительные функции в 3D-представление, поэтому отправьте нам свой [отзыв](#getting-in-touch-with-microsoft-edge-devtools-team).</span><span class="sxs-lookup"><span data-stu-id="f3316-152">We're working on the UI and adding more functionality to the 3D View, so please send us your [feedback](#getting-in-touch-with-microsoft-edge-devtools-team).</span></span>  

<span data-ttu-id="f3316-153">[#987787][CR987787] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="f3316-153">Chromium issue [#987787][CR987787]</span></span>  

### <span data-ttu-id="f3316-154">Расширения кода Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f3316-154">Visual Studio Code extensions</span></span>  

<span data-ttu-id="f3316-155">Кроме того, в команде DevTools были выпущены некоторые расширения для [кода Visual Studio][VisualStudioCode] , позволяющие использовать возможности DevTools прямо из текстового редактора.</span><span class="sxs-lookup"><span data-stu-id="f3316-155">The DevTools team has also released some extensions for [Visual Studio Code][VisualStudioCode] that let you use the power of the DevTools directly from your text editor!</span></span> <span data-ttu-id="f3316-156">Ознакомьтесь с приведенными ниже расширениями.</span><span class="sxs-lookup"><span data-stu-id="f3316-156">Check out the extensions below:</span></span>  

#### <span data-ttu-id="f3316-157">Элементы Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="f3316-157">Elements for Microsoft Edge</span></span>  

<span data-ttu-id="f3316-158">Используйте инструмент "элементы" в коде Visual Studio, добавив [элементы для расширения кода Microsoft Edge \ (Chromium \)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="f3316-158">Use the Elements tool from within Visual Studio Code by adding the [Elements for Microsoft Edge \(Chromium\)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] Visual Studio Code extension.</span></span>  

:::image type="complex" source="../../images/2020/01/elements-for-edge.msft.png" alt-text="Средство &quot;производительность&quot; в DevTools с улучшенной навигацией с помощью клавиатуры и средства чтения с экрана" lightbox="../../images/2020/01/elements-for-edge.msft.png":::
   <span data-ttu-id="f3316-160">Инструмент " **элементы** " в коде Visual Studio с использованием элементов для расширения Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="f3316-160">The **Elements** tool in Visual Studio Code using the Elements for Microsoft Edge extension</span></span>  
:::image-end:::  

<span data-ttu-id="f3316-161">Для получения дополнительных сведений изучите [элементы для расширения кода Microsoft Edge Visual Studio][VisualStudioCodeElementEdgeExtension].</span><span class="sxs-lookup"><span data-stu-id="f3316-161">For more information, check out [Elements for Microsoft Edge Visual Studio Code extension][VisualStudioCodeElementEdgeExtension].</span></span>  

#### <span data-ttu-id="f3316-162">Отладчик для Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="f3316-162">Debugger for Microsoft Edge</span></span>  

<span data-ttu-id="f3316-163">С помощью [отладчика для расширения кода Microsoft Edge][VisualStudioMarketplaceDebuggerEdge] Visual Studio выполните отладку JavaScript, который выполняется в Microsoft EDGE, прямо из кода Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="f3316-163">With the [Debugger for Microsoft Edge][VisualStudioMarketplaceDebuggerEdge] Visual Studio Code extension, debug JavaScript running in Microsoft Edge directly from Visual Studio Code.</span></span>  

:::image type="complex" source="../../images/2020/01/vscode-debugger.msft.png" alt-text="Средство &quot;производительность&quot; в DevTools с улучшенной навигацией с помощью клавиатуры и средства чтения с экрана" lightbox="../../images/2020/01/vscode-debugger.msft.png":::
   <span data-ttu-id="f3316-165">Отладчик для расширения Microsoft EDGE в Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f3316-165">The Debugger for Microsoft Edge Extension in Visual Studio Code</span></span>  
:::image-end:::  

<span data-ttu-id="f3316-166">Дополнительные сведения [об отладке Microsoft Edge из кода Visual Studio можно найти в этой процедуре][VisualStudioCodeDebuggerEdgeExtension].</span><span class="sxs-lookup"><span data-stu-id="f3316-166">For more information, check out [how to debug Microsoft Edge from Visual Studio Code][VisualStudioCodeDebuggerEdgeExtension].</span></span>  

#### <span data-ttu-id="f3316-167">webhint</span><span class="sxs-lookup"><span data-stu-id="f3316-167">webhint</span></span>  

<span data-ttu-id="f3316-168">Расширение [кода Visual Studio, которое используется][VisualStudioMarketplaceWebhintExtension] `webhint` для усовершенствования веб-страницы во время их написания!</span><span class="sxs-lookup"><span data-stu-id="f3316-168">The [webhint][VisualStudioMarketplaceWebhintExtension] Visual Studio Code extension uses `webhint` to improve your web page while you're writing it!</span></span> <span data-ttu-id="f3316-169">Это расширение запускает и сообщает диагностику файлов рабочей области на основе `webhint` анализа.</span><span class="sxs-lookup"><span data-stu-id="f3316-169">This extension runs and reports diagnostics on your workspace files based on `webhint` analysis.</span></span>  

:::image type="complex" source="../../images/2020/01/webhint-vscode-extension.msft.png" alt-text="Средство &quot;производительность&quot; в DevTools с улучшенной навигацией с помощью клавиатуры и средства чтения с экрана" lightbox="../../images/2020/01/webhint-vscode-extension.msft.png":::
   <span data-ttu-id="f3316-171">Расширение кода Visual Studio «веб-подсказка» для анализа `.tsx` файла в коде Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f3316-171">The webhint Visual Studio Code extension analyzing a `.tsx` file in Visual Studio Code</span></span>  
:::image-end:::  

<span data-ttu-id="f3316-172">[Узнайте больше о расширении подсказки кода Visual Studio][WebhintVisualStudioCodeExtension].</span><span class="sxs-lookup"><span data-stu-id="f3316-172">[Learn more about the Visual Studio Code webhint extension][WebhintVisualStudioCodeExtension].</span></span>  

### <span data-ttu-id="f3316-173">Интеграция с Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f3316-173">Visual Studio integration</span></span>  

<span data-ttu-id="f3316-174">В Visual Studio 2019 версии 16,2 или более поздней Используйте отладчик Visual Studio для отладки JavaScript, который выполняется в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="f3316-174">In Visual Studio 2019 version 16.2 or later, use the Visual Studio debugger to debug JavaScript running in Microsoft Edge.</span></span>  <span data-ttu-id="f3316-175">[Загрузите Visual Studio 2019][MicrosoftVisualStudioDownloads] , чтобы попробовать эту функцию!</span><span class="sxs-lookup"><span data-stu-id="f3316-175">[Download Visual Studio 2019][MicrosoftVisualStudioDownloads] to try this feature out!</span></span>  

:::image type="complex" source="../../images/2020/01/vs.msft.png" alt-text="Средство &quot;производительность&quot; в DevTools с улучшенной навигацией с помощью клавиатуры и средства чтения с экрана" lightbox="../../images/2020/01/vs.msft.png":::
   <span data-ttu-id="f3316-177">Visual Studio с возможностью запуска веб-приложения в Microsoft Edge Канарские, dev или Beta</span><span class="sxs-lookup"><span data-stu-id="f3316-177">Visual Studio with the option to launch your web app in Microsoft Edge Canary, Dev, or Beta</span></span>  
:::image-end:::  

<span data-ttu-id="f3316-178">Дополнительные [сведения об отладке Microsoft Edge из Visual Studio][MicrosoftVisualStudio].</span><span class="sxs-lookup"><span data-stu-id="f3316-178">[Learn more about debugging Microsoft Edge from Visual Studio][MicrosoftVisualStudio].</span></span>  

### <span data-ttu-id="f3316-179">Сообщения консоли предотвращения отслеживания</span><span class="sxs-lookup"><span data-stu-id="f3316-179">Tracking prevention Console messages</span></span>  

<span data-ttu-id="f3316-180">Защита от слежения — это уникальная функция в Microsoft EDGE, которая защищает вас от отслеживания веб-сайтов, которые вы еще не посещаете.</span><span class="sxs-lookup"><span data-stu-id="f3316-180">Tracking prevention is a unique feature in Microsoft Edge that protects you from being tracked by websites you haven't visited before.</span></span>  <span data-ttu-id="f3316-181">Параметр предотвращения отслеживания по умолчанию — это режим балансировки, который блокирует средства отслеживания и известных злоумышленников, чтобы обеспечить баланс конфиденциальности и веб-совместимости.</span><span class="sxs-lookup"><span data-stu-id="f3316-181">The default tracking prevention setting is Balanced mode, which blocks 3rd party trackers and known malicious trackers for an experience that balances privacy and web compatibility.</span></span>  <span data-ttu-id="f3316-182">Чтобы получить более подробную информацию о совместимости веб-страницы, если некоторые средства отслеживания заблокированы, мы также добавили предупреждающие сообщения на консоли, когда средство отслеживания заблокировано.</span><span class="sxs-lookup"><span data-stu-id="f3316-182">To give you more insight into the compatibility of your web page when certain trackers are blocked, we've also added warning messages in the Console when a tracker is blocked.</span></span>  

:::image type="complex" source="../../images/2020/01/tracking-prevention.msft.png" alt-text="Средство &quot;производительность&quot; в DevTools с улучшенной навигацией с помощью клавиатуры и средства чтения с экрана" lightbox="../../images/2020/01/tracking-prevention.msft.png":::
   <span data-ttu-id="f3316-184">Сообщения на консоли, когда предотвращение отслеживания блокирует доступ к хранилищу для средства отслеживания</span><span class="sxs-lookup"><span data-stu-id="f3316-184">Messages in the Console when tracking prevention blocks access to storage for a tracker</span></span>  
:::image-end:::  

<span data-ttu-id="f3316-185">[Узнайте больше о предотвращении отслеживания и балансе между конфиденциальностью и веб-совместимостью][TrackingPrevention].</span><span class="sxs-lookup"><span data-stu-id="f3316-185">[Read more about tracking prevention and the balance between privacy and web compatibility][TrackingPrevention].</span></span>  

## <span data-ttu-id="f3316-186">Объявления из проекта Chromium</span><span class="sxs-lookup"><span data-stu-id="f3316-186">Announcements from the Chromium project</span></span>  

<span data-ttu-id="f3316-187">В следующих разделах описаны дополнительные возможности, доступные в Microsoft Edge 81, которые были задействованы в проекте Open Source Chromium.</span><span class="sxs-lookup"><span data-stu-id="f3316-187">The following sections announce additional features available in Microsoft Edge 81 that were contributed to the open source Chromium project.</span></span>  

### <span data-ttu-id="f3316-188">Поддержка Moto G4 в режиме устройства</span><span class="sxs-lookup"><span data-stu-id="f3316-188">Moto G4 support in Device Mode</span></span>  

<span data-ttu-id="f3316-189">После [включения панели инструментов устройства][DeviceToolbar]имитируйте размеры окна просмотра Moto G4 в списке **устройств** .</span><span class="sxs-lookup"><span data-stu-id="f3316-189">After [enabling the Device Toolbar][DeviceToolbar], simulate the dimensions of a Moto G4 viewport from the **Device** list.</span></span>  

:::image type="complex" source="../../images/2020/01/motog4.msft.png" alt-text="Средство &quot;производительность&quot; в DevTools с улучшенной навигацией с помощью клавиатуры и средства чтения с экрана" lightbox="../../images/2020/01/motog4.msft.png":::
   <span data-ttu-id="f3316-191">Имитация окна просмотра Moto G4</span><span class="sxs-lookup"><span data-stu-id="f3316-191">Simulating a Moto G4 viewport</span></span>  
:::image-end:::  

<span data-ttu-id="f3316-192">Щелкните [Показать рамку устройства][DeviceFrame] , чтобы показать аппаратуру Moto G4 в окне просмотра.</span><span class="sxs-lookup"><span data-stu-id="f3316-192">Click [Show Device Frame][DeviceFrame] to show the Moto G4 hardware around the viewport.</span></span>  

:::image type="complex" source="../../images/2020/01/motog4frame.msft.png" alt-text="Средство &quot;производительность&quot; в DevTools с улучшенной навигацией с помощью клавиатуры и средства чтения с экрана" lightbox="../../images/2020/01/motog4frame.msft.png":::
   <span data-ttu-id="f3316-194">Аппаратное обеспечение Moto G4</span><span class="sxs-lookup"><span data-stu-id="f3316-194">Showing the Moto G4 hardware</span></span>  
:::image-end:::  

<span data-ttu-id="f3316-195">Дополнительные возможности:</span><span class="sxs-lookup"><span data-stu-id="f3316-195">Related features:</span></span>  

*   <span data-ttu-id="f3316-196">Откройте [меню команд][CommandMenu] и выполните команду, `Capture screenshot` чтобы сделать снимок экрана просмотра, включающий оборудование Moto G4 (после включения команды **Показать рамку устройства**).</span><span class="sxs-lookup"><span data-stu-id="f3316-196">Open the [Command Menu][CommandMenu] and run the `Capture screenshot` command to take a screenshot of the viewport that includes the Moto G4 hardware (after enabling **Show Device Frame**).</span></span>  
*   <span data-ttu-id="f3316-197">[Регулирование сети и ЦП][ThrottleNetworkAndCpu] для более точной имитации условий просмотра веб-страниц пользователя на мобильном устройстве.</span><span class="sxs-lookup"><span data-stu-id="f3316-197">[Throttle the network and CPU][ThrottleNetworkAndCpu] to more accurately simulate a mobile user's web browsing conditions.</span></span>  

<span data-ttu-id="f3316-198">[#924693][CR924693] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="f3316-198">Chromium issue [#924693][CR924693]</span></span>  

### <span data-ttu-id="f3316-199">Обновления, связанные с файлами cookie</span><span class="sxs-lookup"><span data-stu-id="f3316-199">Cookie-related updates</span></span>  

#### <span data-ttu-id="f3316-200">Заблокированные cookie-файлы в области "cookie"</span><span class="sxs-lookup"><span data-stu-id="f3316-200">Blocked cookies in the Cookies pane</span></span>  

<span data-ttu-id="f3316-201">В области "файлы cookie" на панели приложения теперь отображаются заблокированные файлы cookie с желтым фоном.</span><span class="sxs-lookup"><span data-stu-id="f3316-201">The Cookies pane in the Application panel now displays blocked cookies with a yellow background.</span></span>  

:::image type="complex" source="../../images/2020/01/blockedcookies.msft.png" alt-text="Средство &quot;производительность&quot; в DevTools с улучшенной навигацией с помощью клавиатуры и средства чтения с экрана" lightbox="../../images/2020/01/blockedcookies.msft.png":::
   <span data-ttu-id="f3316-203">Заблокированные cookie-файлы в области "cookie" на панели приложения</span><span class="sxs-lookup"><span data-stu-id="f3316-203">Blocked cookies in the Cookies pane of the Application panel</span></span>  
:::image-end:::  

<span data-ttu-id="f3316-204">[#1030258][CR1030258] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="f3316-204">Chromium issue [#1030258][CR1030258]</span></span>  <!-- inaccessible  -->  

#### <span data-ttu-id="f3316-205">Приоритет cookie-файлов в области "cookie"</span><span class="sxs-lookup"><span data-stu-id="f3316-205">Cookie priority in the Cookie pane</span></span>  

<span data-ttu-id="f3316-206">Таблицы cookie на панелях сеть и приложения теперь включают столбец **приоритета** .</span><span class="sxs-lookup"><span data-stu-id="f3316-206">The Cookies tables in the Network and Application panels now include a **Priority** column.</span></span>  

> [!CAUTION]
> <span data-ttu-id="f3316-207">Chromiumные браузеры, такие как Microsoft EDGE, — это единственные браузеры, поддерживающие приоритет cookie-файлов.</span><span class="sxs-lookup"><span data-stu-id="f3316-207">Chromium-based browsers, like Microsoft Edge, are the only browsers that support cookie priority.</span></span>  

<span data-ttu-id="f3316-208">[#1026879][CR1026879] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="f3316-208">Chromium issue [#1026879][CR1026879]</span></span>  

#### <span data-ttu-id="f3316-209">Изменение всех значений cookie-файлов</span><span class="sxs-lookup"><span data-stu-id="f3316-209">Edit all cookie values</span></span>  

<span data-ttu-id="f3316-210">Все ячейки в таблицах cookie теперь доступны для редактирования, кроме ячеек в столбце **Размер** , так как этот столбец представляет размер файла cookie в байтах.</span><span class="sxs-lookup"><span data-stu-id="f3316-210">All cells in the Cookie tables are editable now, except cells in the **Size** column because that column represents the network size of the cookie, in bytes.</span></span>  <span data-ttu-id="f3316-211">Просмотрите [поля][CookiesFields] , поясняющие каждый столбец.</span><span class="sxs-lookup"><span data-stu-id="f3316-211">See [Fields][CookiesFields] for an explanation of each column.</span></span>  

:::image type="complex" source="../../images/2020/01/editcookie.msft.png" alt-text="Средство &quot;производительность&quot; в DevTools с улучшенной навигацией с помощью клавиатуры и средства чтения с экрана" lightbox="../../images/2020/01/editcookie.msft.png":::
   <span data-ttu-id="f3316-213">Изменение значения cookie-файла</span><span class="sxs-lookup"><span data-stu-id="f3316-213">Editing a cookie value</span></span>  
:::image-end:::  

#### <span data-ttu-id="f3316-214">Копирование как Node.js выбор для включения данных cookie</span><span class="sxs-lookup"><span data-stu-id="f3316-214">Copy as Node.js fetch to include cookie data</span></span>  

<span data-ttu-id="f3316-215">Щелкните правой кнопкой мыши по сетевому запросу и выберите команду **Копировать**  >  **копию как Node.js извлечь** , чтобы получить `fetch` выражение, включающее данные cookie.</span><span class="sxs-lookup"><span data-stu-id="f3316-215">Right-click a network request and select **Copy** > **Copy as Node.js fetch** to get a `fetch` expression that includes cookie data.</span></span>  

:::image type="complex" source="../../images/2020/01/fetchcookies.msft.png" alt-text="Средство &quot;производительность&quot; в DevTools с улучшенной навигацией с помощью клавиатуры и средства чтения с экрана" lightbox="../../images/2020/01/fetchcookies.msft.png":::
   <span data-ttu-id="f3316-217">Копирование как Node.js выборка</span><span class="sxs-lookup"><span data-stu-id="f3316-217">Copy as Node.js fetch</span></span>  
:::image-end:::  

<span data-ttu-id="f3316-218">[#1029826][CR1029826] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="f3316-218">Chromium issue [#1029826][CR1029826]</span></span>  

### <span data-ttu-id="f3316-219">Более точные значки манифеста веб-приложения</span><span class="sxs-lookup"><span data-stu-id="f3316-219">More accurate web app manifest icons</span></span>  

<span data-ttu-id="f3316-220">Ранее область манифеста на панели приложения отправляет свои собственные запросы для отображения значков манифеста веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="f3316-220">Previously, the Manifest pane in the Application panel sent its own requests in order to display web app manifest icons.</span></span>  <span data-ttu-id="f3316-221">DevTools теперь показывает тот же значок манифеста, который использует Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="f3316-221">DevTools now shows the exact same manifest icon that Microsoft Edge uses.</span></span>  

:::image type="complex" source="../../images/2020/01/manifesticons.msft.png" alt-text="Средство &quot;производительность&quot; в DevTools с улучшенной навигацией с помощью клавиатуры и средства чтения с экрана" lightbox="../../images/2020/01/manifesticons.msft.png":::
   <span data-ttu-id="f3316-223">Значки в области «манифест»</span><span class="sxs-lookup"><span data-stu-id="f3316-223">Icons in the Manifest pane</span></span>  
:::image-end:::  

<span data-ttu-id="f3316-224">[#985402][CR985402] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="f3316-224">Chromium issue [#985402][CR985402]</span></span>  

### <span data-ttu-id="f3316-225">Наведите указатель мыши на свойства содержимого CSS, чтобы увидеть неэкранированные значения</span><span class="sxs-lookup"><span data-stu-id="f3316-225">Hover over CSS content properties to see unescaped values</span></span>  

<span data-ttu-id="f3316-226">Наведите указатель мыши на значение `content` свойства, чтобы увидеть неэкранированную версию значения.</span><span class="sxs-lookup"><span data-stu-id="f3316-226">Hover over the value of a `content` property to see the unescaped version of the value.</span></span>  

<span data-ttu-id="f3316-227">Например, в этой статье вы узнаете [о том,][CSSContentDemo] что на `p::after` панели Стили отображается строка с escape-символами.</span><span class="sxs-lookup"><span data-stu-id="f3316-227">For example, in this [demo][CSSContentDemo] when you inspect the `p::after` pseudo-element you see an escaped string in the Styles pane:</span></span>  

:::image type="complex" source="../../images/2020/01/escapedstring.msft.png" alt-text="Средство &quot;производительность&quot; в DevTools с улучшенной навигацией с помощью клавиатуры и средства чтения с экрана" lightbox="../../images/2020/01/escapedstring.msft.png":::
   <span data-ttu-id="f3316-229">Строка с escape-символом</span><span class="sxs-lookup"><span data-stu-id="f3316-229">The escaped string</span></span>  
:::image-end:::  

<span data-ttu-id="f3316-230">При наведении указателя мыши на значение, которое `content` отображается в неэкранированном значении:</span><span class="sxs-lookup"><span data-stu-id="f3316-230">When you hover over the `content` value you see the unescaped value:</span></span>  

:::image type="complex" source="../../images/2020/01/unescapedstring.msft.png" alt-text="Средство &quot;производительность&quot; в DevTools с улучшенной навигацией с помощью клавиатуры и средства чтения с экрана" lightbox="../../images/2020/01/unescapedstring.msft.png":::
   <span data-ttu-id="f3316-232">Неэкранированное значение</span><span class="sxs-lookup"><span data-stu-id="f3316-232">The unescaped value</span></span>  
:::image-end:::  

### <span data-ttu-id="f3316-233">Дополнительные сведения об ошибках на карте исходного кода на консоли</span><span class="sxs-lookup"><span data-stu-id="f3316-233">More detailed source map errors in the Console</span></span>  

<span data-ttu-id="f3316-234">Теперь консоль содержит более подробные сведения о том, почему не удалось загрузить или проанализировать исходную карту.</span><span class="sxs-lookup"><span data-stu-id="f3316-234">The Console now provides more detail on why a source map failed to load or parse.</span></span>  <span data-ttu-id="f3316-235">Ранее она только что предоставила ошибку, не объясняющую, что пошло не так.</span><span class="sxs-lookup"><span data-stu-id="f3316-235">Previously it just provided an error without explaining what went wrong.</span></span>  

:::image type="complex" source="../../images/2020/01/sourcemap.msft.png" alt-text="Средство &quot;производительность&quot; в DevTools с улучшенной навигацией с помощью клавиатуры и средства чтения с экрана" lightbox="../../images/2020/01/sourcemap.msft.png":::
   <span data-ttu-id="f3316-237">Ошибка при загрузке карты исходного кода на консоли</span><span class="sxs-lookup"><span data-stu-id="f3316-237">A source map loading error in the Console</span></span>  
:::image-end:::  

### <span data-ttu-id="f3316-238">Настройка отключения прокрутки за пределами файла</span><span class="sxs-lookup"><span data-stu-id="f3316-238">Setting for disabling scrolling past the end of a file</span></span>  

<span data-ttu-id="f3316-239">Откройте [Параметры][Settings] и выберите Отключить **Preferences**  >  **исходные**настройки.  >  **разрешите прокрутку за** пределами файла, чтобы отключить поведение пользовательского интерфейса по умолчанию, позволяющее прокручивать прокрутку за пределами файла на панели « **источники** ».</span><span class="sxs-lookup"><span data-stu-id="f3316-239">Open [Settings][Settings] and then disable **Preferences** > **Sources** > **Allow scrolling past end of file** to disable the default UI behavior that allows you to scroll well past the end of a file in the **Sources** panel.</span></span>  

:::image type="complex" source="../../images/2020/01/settings.msft.png" alt-text="Средство &quot;производительность&quot; в DevTools с улучшенной навигацией с помощью клавиатуры и средства чтения с экрана" lightbox="../../images/2020/01/settings.msft.png":::
   <span data-ttu-id="f3316-241">Отключение **разрешения на прокрутку за** пределами файла в параметрах</span><span class="sxs-lookup"><span data-stu-id="f3316-241">Disabling **Allow scrolling past end of file** in Settings</span></span>  
:::image-end:::  

:::image type="complex" source="../../images/2020/01/scrollingsources.msft.png" alt-text="Средство &quot;производительность&quot; в DevTools с улучшенной навигацией с помощью клавиатуры и средства чтения с экрана" lightbox="../../images/2020/01/scrollingsources.msft.png":::
   <span data-ttu-id="f3316-243">Прокрутка за пределами файла теперь отключена на панели «источники»</span><span class="sxs-lookup"><span data-stu-id="f3316-243">Scrolling past the end of a file is now disabled in the Sources panel</span></span>  
:::image-end:::  

## <span data-ttu-id="f3316-244">Загрузка каналов предварительной версии Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="f3316-244">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="f3316-245">Если вы используете Windows или macOS, рассматривайте в качестве браузера по умолчанию использование [каналов предварительного просмотра Microsoft Edge][MicrosoftEdgePreviewChannels] .</span><span class="sxs-lookup"><span data-stu-id="f3316-245">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="f3316-246">Каналы предварительного просмотра предоставляют доступ к последним функциям DevTools.</span><span class="sxs-lookup"><span data-stu-id="f3316-246">The preview channels give you access to the latest DevTools features.</span></span>  

## <span data-ttu-id="f3316-247">Знакомство с Microsoft Edge DevTools Team</span><span class="sxs-lookup"><span data-stu-id="f3316-247">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DeviceToolbar]: /microsoft-edge/devtools-guide-chromium/device-mode/index#simulate-a-mobile-viewport "Имитировать окно просмотра для мобильных устройств: Эмуляция мобильных устройств с помощью режима устройства в Microsoft Edge DevTools | Документы Microsoft"
[DeviceFrame]: /microsoft-edge/devtools-guide-chromium/device-mode/index#show-device-frame "Показать рамку устройства — имитировать мобильные устройства с помощью режима устройства в Microsoft Edge DevTools | Документы Microsoft"
[CommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Выполнение команд с помощью командного меню Microsoft Edge DevTools | Документы Microsoft"  
[ThrottleNetworkAndCpu]: /microsoft-edge/devtools-guide-chromium/device-mode/index#throttle-the-network-and-cpu "Регулирование сети и ЦП — Эмуляция мобильных устройств с помощью режима устройства в Microsoft Edge DevTools | Документы Microsoft"
[Settings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Параметры: Настройка Microsoft Edge DevTools | Документы Microsoft"
[MicrosoftVisualStudio]: /microsoft-edge/visual-studio/index "Visual Studio | Документы Microsoft"  
[CookiesFields]: /microsoft-edge/devtools-guide-chromium/storage/cookies#fields "Поля — просмотр, изменение и удаление cookie-файлов в Microsoft Edge DevTools | Документы Microsoft"  

[VisualStudioCodeDebuggerEdgeExtension]: /microsoft-edge/visual-studio-code/debugger-for-edge "Отладчик для расширения кода Microsoft Edge Visual Studio"  
[VisualStudioCodeElementEdgeExtension]: /microsoft-edge/visual-studio-code/elements-for-edge "Элементы расширения кода Microsoft Edge Visual Studio"  

[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Каналы предварительной версии Microsoft Edge"  

[VisualStudioCode]: https://aka.ms/vscode "Код Visual Studio"  
[VisualStudioMarketplaceDebuggerEdge]: https://aka.ms/debugger4code "Отладчик для Microsoft Edge-Visual Studio Marketplace"  
[VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension]: https://aka.ms/elements4code "Элементы для Microsoft Edge \ (Chromium \) — Visual Studio Marketplace"  
[VisualStudioMarketplaceWebhintExtension]: https://aka.ms/webhint4code ""Подсказка" — Visual Studio Marketplace"

[TrackingPrevention]: https://aka.ms/microsoftedge/tracking-prevention-blog "Улучшение защиты от слежения в блоге Microsoft Edge"

[MicrosoftEdgeInsiderAddons]: https://aka.ms/webhint/edge-extension "Надстройки Microsoft Edge для участников программы предварительной оценки"  
[MicrosoftVisualStudioDownloads]: https://aka.ms/vs/download "Скачайте Visual Studio 2019 для Windows & Mac"  

[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Публикация твита"  

[CR924693]: https://crbug.com/924693 "Запрос функции: Добавление Moto G4 в список режимов устройства | Ошибки Chromium"  
[CR1030258]: https://crbug.com/1030258 "CR 1030258 | Ошибки Chromium"  
[CR1026879]: https://crbug.com/1026879 "На вкладке cookie на консоли разработки больше не отображается приоритет | Ошибки Chromium"  
[CR1029826]: https://crbug.com/1029826 "Вкладка "сеть" — > щелкнуть правой кнопкой мыши, чтобы запрашивать > копирование > копирование в качестве выборке не копирует файлы cookie | Ошибки Chromium"  
[CR985402]: https://crbug.com/985402 "строки ошибки значка манифеста веб-приложения — это запутанная | Ошибки Chromium"  
[CR963183]: https://crbug.com/963183 "DevTools не соответствуют требованиям WCAG | Ошибки Chromium"  
[CR941561]: https://crbug.com/941561 "Локализуемость DevTools | Ошибки Chromium"  
[CR987787]: https://crbug.com/987787 "3D-представление DOM | Ошибки Chromium"  

[CSSContentDemo]: https://mathiasbynens.github.io/css-dbg-stories/css-escapes.html "Демонстрация для без последовательного содержимого CSS"  

[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Новая ошибка — MicrosoftDocs/Edge-разработчик"  

[TheWebWeWant]: https://aka.ms/webwewant "Требуемый веб-сайт"  
[AccessibilityInsights]: https://aka.ms/a11yinsights "Аналитические сведения о специальных возможностях"  
[MDNDocumentObjectModel]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model "Объектная модель документов (DOM) | MDN"  
[MDNZIndex]: https://developer.mozilla.org/docs/Web/CSS/z-index "z-индекс | MDN"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools учетной записи Twitter"  

[Webhint]: https://aka.ms/webhint "Подсказка"  

[WebhintBrowserExtension]: https://aka.ms/webhint/browser-extension "Расширение браузеров веб – подсказок | Документация по подсказкам"  
[WebhintVisualStudioCodeExtension]: https://aka.ms/webhint/code-extension "Расширение кода Visual Studio "Подсказка" | Документация по подсказкам"  

> [!NOTE]
> <span data-ttu-id="f3316-284">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f3316-284">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="f3316-285">Исходная страница будет найдена [здесь](https://developers.google.com/web/updates/2020/01/devtools/index) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="f3316-285">The original page is found [here](https://developers.google.com/web/updates/2020/01/devtools/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="f3316-287">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f3316-287">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  