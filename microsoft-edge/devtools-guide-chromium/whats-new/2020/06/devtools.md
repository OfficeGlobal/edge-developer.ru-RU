---
description: Функции отладки сетки CSS, запросы на изменение и воспроизведение с помощью консоли сети и многое другое.
title: Новые возможности DevTools (Microsoft Edge 85)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 01651bdf0f36f7c175f843655c275695a680b6c1
ms.sourcegitcommit: b337717957529239434b4e8e1e167aebf0543518
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/15/2020
ms.locfileid: "11015463"
---
# <span data-ttu-id="ba8d9-104">Новые возможности DevTools (Microsoft Edge 85)</span><span class="sxs-lookup"><span data-stu-id="ba8d9-104">What's New In DevTools (Microsoft Edge 85)</span></span>  

## <span data-ttu-id="ba8d9-105">Объявления из группы Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="ba8d9-105">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="ba8d9-106">В следующих разделах представлен список извещений, которые могут быть пропущены командой Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="ba8d9-106">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team.</span></span>  <span data-ttu-id="ba8d9-107">Просмотрите объявления, чтобы ознакомиться с новыми возможностями в DevTools, расширениях кода Visual Studio и многое другое.</span><span class="sxs-lookup"><span data-stu-id="ba8d9-107">See the announcements to try new features in the DevTools, Visual Studio Code extensions, and more.</span></span>  <span data-ttu-id="ba8d9-108">Чтобы всегда оставаться на связи с самыми последними и более свежими возможностями, скачайте на веб – [каналы предварительного просмотра Microsoft Edge][MicrosoftEdgePreviewChannels] и [следуйте указаниям Microsoft Edge DevTools Team для Twitter][EdgeDevToolsTwitterAccount].</span><span class="sxs-lookup"><span data-stu-id="ba8d9-108">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow the Microsoft Edge DevTools team on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <span data-ttu-id="ba8d9-109">Функции отладки сетки каскадных стилей</span><span class="sxs-lookup"><span data-stu-id="ba8d9-109">CSS grid debugging features</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Экспериментальная функция":::
   <span data-ttu-id="ba8d9-111">Экспериментальная функция</span><span class="sxs-lookup"><span data-stu-id="ba8d9-111">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="ba8d9-112">Группа Microsoft Edge DevTools — совместная работа с группой Chrome DevTools и Chromium, чтобы добавить в DevTools новые функции отладки сетки каскадных стилей.</span><span class="sxs-lookup"><span data-stu-id="ba8d9-112">The Microsoft Edge DevTools team is collaborating with the Chrome DevTools team and Chromium community to add new CSS grid debugging features to DevTools.</span></span>  <span data-ttu-id="ba8d9-113">Теперь вы можете отображать номера линий сетки, зазоры сетки и дополнительные линии сетки в качестве наложений на страницы.</span><span class="sxs-lookup"><span data-stu-id="ba8d9-113">You are now able to display grid line numbers, grid gaps, and extended grid lines as an on-page overlay.</span></span>  <span data-ttu-id="ba8d9-114">Кроме того, в скором времени становятся более улучшены инструменты сетки.</span><span class="sxs-lookup"><span data-stu-id="ba8d9-114">Plus, more improvements to the grid tools are coming soon.</span></span>  

:::image type="complex" source="../../media/2020/06/experiments-grid.msft.png" alt-text="Экспериментальная функция" lightbox="../../media/2020/06/experiments-grid.msft.png":::
   <span data-ttu-id="ba8d9-116">Функции отладки сетки каскадных стилей</span><span class="sxs-lookup"><span data-stu-id="ba8d9-116">CSS grid debugging features</span></span>
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="ba8d9-117">Чтобы включить эксперимент, ознакомьтесь со следующей страницей [Включение экспериментальных функций][DevtoolsExperimentalFeaturesTurnOn] и установите флажок **включить новые возможности отладки сетки каскадных стилей**.</span><span class="sxs-lookup"><span data-stu-id="ba8d9-117">To enable the experiment, see [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOn] and select the checkbox next to **Enable new CSS Grid debugging features**.</span></span>  
> 
> <span data-ttu-id="ba8d9-118">Чтобы опробовать эксперимент с образцом, ознакомьтесь со статьей [Пример планировщика сетки каскадных стилей][CodepenRachelweilYzwBzKM].</span><span class="sxs-lookup"><span data-stu-id="ba8d9-118">To try out the experiment with a sample, see [CSS Grid planner example][CodepenRachelweilYzwBzKM].</span></span>  

<span data-ttu-id="ba8d9-119">[#1047356][CR1047356] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="ba8d9-119">Chromium issue [#1047356][CR1047356]</span></span>  

### <span data-ttu-id="ba8d9-120">Изменение и повторное воспроизведение запросов с помощью сетевой консоли</span><span class="sxs-lookup"><span data-stu-id="ba8d9-120">Edit and Replay requests with the Network Console</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Экспериментальная функция":::
   <span data-ttu-id="ba8d9-122">Экспериментальная функция</span><span class="sxs-lookup"><span data-stu-id="ba8d9-122">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="ba8d9-123">Теперь вы можете использовать команду " **изменить и воспроизвести** " на запросах в [сетевом журнале][DevtoolsNetworkIndexLogActivity] с помощью **сетевой консоли**.</span><span class="sxs-lookup"><span data-stu-id="ba8d9-123">You are now able to use **Edit and Replay** on requests in the [Network Log][DevtoolsNetworkIndexLogActivity] using the **Network Console**.</span></span>  

:::image type="complex" source="../../media/2020/06/experiments-network-console-edit-and-replay.msft.png" alt-text="Экспериментальная функция" lightbox="../../media/2020/06/experiments-network-console-edit-and-replay.msft.png":::
   <span data-ttu-id="ba8d9-125">Изменение и повторное воспроизведение запроса в [NetworkLog][DevtoolsNetworkIndexLogActivity] с помощью **сетевой консоли**</span><span class="sxs-lookup"><span data-stu-id="ba8d9-125">Edit and Replay a request in the [NetworkLog][DevtoolsNetworkIndexLogActivity] with the **Network Console**</span></span>  
:::image-end:::  

<span data-ttu-id="ba8d9-126">Новая панель, **Сетевая консоль** открывается в [ящике DevTools][DevtoolsCustomizeIndexDrawer] и автоматически заполняется данными для HTTP-запроса.</span><span class="sxs-lookup"><span data-stu-id="ba8d9-126">A new panel, the **Network Console** opens in the [DevTools Drawer][DevtoolsCustomizeIndexDrawer] and automatically populates with information for the HTTP request.</span></span>  <span data-ttu-id="ba8d9-127">Чтобы просмотреть ответ, возвращенный сервером, измените запрос и нажмите кнопку **Отправить**.</span><span class="sxs-lookup"><span data-stu-id="ba8d9-127">To see the response returned from the server, edit the request \(if needed\) and select **Send**.</span></span>  

<span data-ttu-id="ba8d9-128">Вы также можете использовать **консоль сети** для создания и отправки HTTP-запросов непосредственно из DevTools.</span><span class="sxs-lookup"><span data-stu-id="ba8d9-128">You may also use the **Network Console** to create and send HTTP requests directly from the DevTools.</span></span>  

:::image type="complex" source="../../media/2020/06/experiments-network-console.msft.png" alt-text="Экспериментальная функция" lightbox="../../media/2020/06/experiments-network-console.msft.png":::
   <span data-ttu-id="ba8d9-130">Панель " **Сетевая консоль** "</span><span class="sxs-lookup"><span data-stu-id="ba8d9-130">The **Network Console** panel</span></span>  
:::image-end:::  

> [!TIP]
> <span data-ttu-id="ba8d9-131">Чтобы увидеть **сетевую консоль** в главной панели \ (Top \), а не в [DevTools][DevtoolsCustomizeIndexDrawer], ознакомьтесь с разделами [Перемещение инструментов между панелями](#move-tools-between-panels).</span><span class="sxs-lookup"><span data-stu-id="ba8d9-131">To see **Network Console** in the main \(top\) panel instead of the [DevTools Drawer][DevtoolsCustomizeIndexDrawer], see [moving tools between panels](#move-tools-between-panels).</span></span>  

> [!NOTE]
> <span data-ttu-id="ba8d9-132">Чтобы включить эксперимент, ознакомьтесь со следующей командой [Включение экспериментальных функций][DevtoolsExperimentalFeaturesTurnOn] и установите флажок **включить сетевую консоль**.</span><span class="sxs-lookup"><span data-stu-id="ba8d9-132">To enable the experiment, see [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOn] and select the checkbox next to **Enable Network Console**.</span></span>  
> 
> <span data-ttu-id="ba8d9-133">Откройте [Журнал сети][DevtoolsNetworkIndexLogActivity], откройте контекстное меню (щелкните правой кнопкой мыши и выберите команду **изменить и воспроизвести**).</span><span class="sxs-lookup"><span data-stu-id="ba8d9-133">Open the [Network Log][DevtoolsNetworkIndexLogActivity], open the contextual menu \(right-click\), and select **Edit and Replay**.</span></span>  

<span data-ttu-id="ba8d9-134">[#1093687][CR1093687] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="ba8d9-134">Chromium issue [#1093687][CR1093687]</span></span>  

### <span data-ttu-id="ba8d9-135">События respondWith рабочего процесса на вкладке время</span><span class="sxs-lookup"><span data-stu-id="ba8d9-135">Service worker respondWith events in the Timing tab</span></span>  

<span data-ttu-id="ba8d9-136">Вкладка **время** на панели " **сеть** " теперь включает `respondWith` события рабочих процессов служб.</span><span class="sxs-lookup"><span data-stu-id="ba8d9-136">The **Timing** tab of the **Network** panel now includes `respondWith` service worker events.</span></span>  <span data-ttu-id="ba8d9-137">`respondWith`Событие "сотрудник службы" показывает продолжительность, начиная с момента, `fetch` когда обработчик событий сотрудника службы начнет выполняться до того момента, когда `respondWith` `fetch` будет сопоставлено обещание обработчика.</span><span class="sxs-lookup"><span data-stu-id="ba8d9-137">The `respondWith` service worker event shows the duration from the time immediately before the service worker `fetch` event handler starts running to the time when the `respondWith` promise of the `fetch` handler is settled.</span></span>  

:::image type="complex" source="../../media/2020/06/timing-tab.msft.png" alt-text="Экспериментальная функция" lightbox="../../media/2020/06/timing-tab.msft.png":::
   <span data-ttu-id="ba8d9-139">`respondWith`Событие "сотрудник службы" на вкладке " **время** " на панели " **сеть** "</span><span class="sxs-lookup"><span data-stu-id="ba8d9-139">The `respondWith` service worker event in the **Timing** tab of the **Network** panel</span></span>  
:::image-end:::  

<span data-ttu-id="ba8d9-140">Развернутый **ответ получен** , чтобы просмотреть дополнительные сведения из `fetch` ответа, например, `CacheStorageCacheName` `serviceWorkerResponseSource` и `ResponseTime` .</span><span class="sxs-lookup"><span data-stu-id="ba8d9-140">Expand **Response received** to see additional information from the `fetch` response like `CacheStorageCacheName`, `serviceWorkerResponseSource`, and `ResponseTime`.</span></span>  

:::image type="complex" source="../../media/2020/06/timing-tab2.msft.png" alt-text="Экспериментальная функция" lightbox="../../media/2020/06/timing-tab2.msft.png":::
   <span data-ttu-id="ba8d9-142">**Получен ответ на запрос** Expand для просмотра дополнительных сведений из `fetch` ответа</span><span class="sxs-lookup"><span data-stu-id="ba8d9-142">Expand **Response received** to see additional information from the `fetch` response</span></span>  
:::image-end:::  

<span data-ttu-id="ba8d9-143">[#1066579][CR1066579] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="ba8d9-143">Chromium issue [#1066579][CR1066579]</span></span>  

### <span data-ttu-id="ba8d9-144">Обратная связь по этой подсказке на панели "вопросы"</span><span class="sxs-lookup"><span data-stu-id="ba8d9-144">webhint feedback in the Issues panel</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Экспериментальная функция":::
   <span data-ttu-id="ba8d9-146">Экспериментальная функция</span><span class="sxs-lookup"><span data-stu-id="ba8d9-146">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="ba8d9-147">веб- [Подсказка][WebhintMain] — это средство с открытым исходным кодом, которое обеспечивает обратную связь в режиме реального времени для обеспечения специальных возможностей, совместимости, безопасности, производительности, PWAs и других распространенных проблем, возникающих при работе в Интернете.</span><span class="sxs-lookup"><span data-stu-id="ba8d9-147">[webhint][WebhintMain] is an open-source tool that provides real-time feedback on the accessibility, cross-browser compatibility, security, performance, PWAs, and other common web development issues of websites.</span></span>  <span data-ttu-id="ba8d9-148">Теперь вы можете увидеть отзыв по этой подсказке на панели " [вопросы][DevtoolsIssues] ".</span><span class="sxs-lookup"><span data-stu-id="ba8d9-148">You are now able to see webhint feedback in the [Issues][DevtoolsIssues] panel.</span></span>  

:::image type="complex" source="../../media/2020/06/experiments-webhint.msft.png" alt-text="Экспериментальная функция" lightbox="../../media/2020/06/experiments-webhint.msft.png":::
   <span data-ttu-id="ba8d9-150">Обратная связь по этой подсказке на панели "вопросы"</span><span class="sxs-lookup"><span data-stu-id="ba8d9-150">webhint feedback in the Issues panel</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="ba8d9-151">Чтобы включить эксперимент, ознакомьтесь со следующей страницей [Включение экспериментальных функций][DevtoolsExperimentalFeaturesTurnOn] и установите флажок **включить подсказку**.</span><span class="sxs-lookup"><span data-stu-id="ba8d9-151">To enable the experiment, see [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOn] and select the checkbox next to **Enable webhint**.</span></span>  
> 
> <span data-ttu-id="ba8d9-152">Откройте панель " [проблемы][DevtoolsIssues] ", чтобы увидеть отзыв из подсказки.</span><span class="sxs-lookup"><span data-stu-id="ba8d9-152">Open the [Issues][DevtoolsIssues] panel to see feedback from webhint.</span></span>  

<span data-ttu-id="ba8d9-153">[#1070378][CR1070378] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="ba8d9-153">Chromium issue [#1070378][CR1070378]</span></span>  

### <span data-ttu-id="ba8d9-154">Перемещение инструментов между панелями</span><span class="sxs-lookup"><span data-stu-id="ba8d9-154">Move tools between panels</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Экспериментальная функция":::
   <span data-ttu-id="ba8d9-156">Экспериментальная функция</span><span class="sxs-lookup"><span data-stu-id="ba8d9-156">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="ba8d9-157">Обычно такие инструменты, как **элементы** и **сеть** , можно открывать только на главной панели \ (Top \) DevTools.</span><span class="sxs-lookup"><span data-stu-id="ba8d9-157">Normally, tools such as **Elements** and **Network** may only be opened in the main \(top\) panel of DevTools.</span></span>  <span data-ttu-id="ba8d9-158">Аналогичным образом такие инструменты, как **трехмерный вид** и **проблемы** , можно открывать только на панели ящик \ (Нижняя \) DevTools.</span><span class="sxs-lookup"><span data-stu-id="ba8d9-158">Similarly, tools such as **3D View** and **Issues** may only be opened in the drawer \(bottom\) panel of DevTools.</span></span>  <span data-ttu-id="ba8d9-159">Теперь вы можете настраивать макет DevTools, перемещая инструменты между верхней и нижней панелями.</span><span class="sxs-lookup"><span data-stu-id="ba8d9-159">You are now able to customize your DevTools layout by moving tools between the top and bottom panels.</span></span>  

:::image type="complex" source="../../media/2020/06/experiments-move-panels.msft.png" alt-text="Экспериментальная функция" lightbox="../../media/2020/06/experiments-move-panels.msft.png":::
   <span data-ttu-id="ba8d9-161">Перемещение вкладок между панелями</span><span class="sxs-lookup"><span data-stu-id="ba8d9-161">Moving tabs between panels</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="ba8d9-162">Чтобы включить эксперимент, ознакомьтесь со следующей страницей [Включение экспериментальных функций][DevtoolsExperimentalFeaturesTurnOn] и установите флажок **включить функцию поддержки для перемещения вкладок между панелями**.</span><span class="sxs-lookup"><span data-stu-id="ba8d9-162">To enable the experiment, see [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOn] and select the checkbox next to **Enable support to move tabs between panels**.</span></span>  

<span data-ttu-id="ba8d9-163">[#897944][CR897944] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="ba8d9-163">Chromium issue [#897944][CR897944]</span></span>  

### <span data-ttu-id="ba8d9-164">Улучшенная всплывающая подсказка инициатора на панели "сеть"</span><span class="sxs-lookup"><span data-stu-id="ba8d9-164">Improved Initiator tooltip in the Network panel</span></span>  

<span data-ttu-id="ba8d9-165">В Microsoft Edge 83 и 84 с помощью всплывающих подсказок для столбца инициаторов, в котором отображается причина запроса ресурсов, в [сетевом журнале][DevtoolsNetworkIndexLogActivity] отображается горизонтальная полоса прокрутки.</span><span class="sxs-lookup"><span data-stu-id="ba8d9-165">In Microsoft Edge 83 and 84, tooltips for the Initiator column, which shows the cause of the resource request, in the [Network Log][DevtoolsNetworkIndexLogActivity] displayed with a horizontal scrollbar.</span></span>  <span data-ttu-id="ba8d9-166">Вы можете видеть стек вызовов, который инициировал запрос, прокручивать по горизонтали в подсказке.</span><span class="sxs-lookup"><span data-stu-id="ba8d9-166">You were only able to see the call stack that initiated the request by scrolling horizontally in the tooltip.</span></span>  

:::image type="complex" source="../../media/2020/06/initiator-tooltip-84.msft.png" alt-text="Экспериментальная функция" lightbox="../../media/2020/06/initiator-tooltip-84.msft.png":::
   <span data-ttu-id="ba8d9-168">Всплывающая подсказка инициатора в Microsoft Edge 84</span><span class="sxs-lookup"><span data-stu-id="ba8d9-168">The Initiator tooltip in Microsoft Edge 84</span></span>  
:::image-end:::  

<span data-ttu-id="ba8d9-169">Начиная с Microsoft Edge 85, теперь вы можете видеть стек вызовов инициаторов в подсказке без горизонтальной прокрутки.</span><span class="sxs-lookup"><span data-stu-id="ba8d9-169">Starting with Microsoft Edge 85, you are now able to see the Initiator call stack in the tooltip without scrolling horizontally.</span></span>  

:::image type="complex" source="../../media/2020/06/initiator-tooltip-85.msft.png" alt-text="Экспериментальная функция" lightbox="../../media/2020/06/initiator-tooltip-85.msft.png":::
   <span data-ttu-id="ba8d9-171">Всплывающая подсказка инициатора в Microsoft Edge 85</span><span class="sxs-lookup"><span data-stu-id="ba8d9-171">The Initiator tooltip in Microsoft Edge 85</span></span>
:::image-end:::  

<span data-ttu-id="ba8d9-172">[#1069404][CR1069404] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="ba8d9-172">Chromium issue [#1069404][CR1069404]</span></span>  

## <span data-ttu-id="ba8d9-173">Объявления из проекта Chromium</span><span class="sxs-lookup"><span data-stu-id="ba8d9-173">Announcements from the Chromium project</span></span>  

<span data-ttu-id="ba8d9-174">В следующих разделах описаны дополнительные возможности, доступные в Microsoft Edge 85, которые были задействованы в проекте Open Source Chromium.</span><span class="sxs-lookup"><span data-stu-id="ba8d9-174">The following sections announce additional features available in Microsoft Edge 85 that were contributed to the open source Chromium project.</span></span>  

### <span data-ttu-id="ba8d9-175">Редактирование стилей для платформ CSS в JS</span><span class="sxs-lookup"><span data-stu-id="ba8d9-175">Style editing for CSS-in-JS frameworks</span></span>  

<span data-ttu-id="ba8d9-176">Панель " **стили** " теперь обеспечивает улучшенную поддержку редактирования стилей, созданных с помощью API [объектной модели CSS (CSSOM)][CsswgDraftsCssom] .</span><span class="sxs-lookup"><span data-stu-id="ba8d9-176">The **Styles** pane now has better support for editing styles that were created with the [CSS Object Model (CSSOM)][CsswgDraftsCssom] APIs.</span></span>  <span data-ttu-id="ba8d9-177">Во многих платформах и библиотеках, использующих CSS из JS, для конструирования стилей используются API CSSOM в разделе "внутри".</span><span class="sxs-lookup"><span data-stu-id="ba8d9-177">Many CSS-in-JS frameworks and libraries use the CSSOM APIs under the hood to construct styles.</span></span>  

<span data-ttu-id="ba8d9-178">Теперь вы можете изменять стили, добавленные в JavaScript с помощью [построенных таблиц стилей][WicgConstructStylesheet].</span><span class="sxs-lookup"><span data-stu-id="ba8d9-178">You are now able to edit styles added in JavaScript using [Constructable Stylesheets][WicgConstructStylesheet].</span></span>  <span data-ttu-id="ba8d9-179">Создаваемые таблицы стилей — это новый способ создания и распространения многократно используемых стилей при использовании [теневой модели DOM][MdnShadowDom].</span><span class="sxs-lookup"><span data-stu-id="ba8d9-179">Constructable Stylesheets are a new way to create and distribute reusable styles when using [Shadow DOM][MdnShadowDom].</span></span>  

<span data-ttu-id="ba8d9-180">Например, стили, `h1` добавленные с помощью `CSSStyleSheet` \ (CSSOM API \), не были изменены ранее.</span><span class="sxs-lookup"><span data-stu-id="ba8d9-180">For example, the `h1` styles added with `CSSStyleSheet` \(CSSOM APIs\) were not editable previously.</span></span>  <span data-ttu-id="ba8d9-181">Теперь стили доступны для редактирования в области **стили** .</span><span class="sxs-lookup"><span data-stu-id="ba8d9-181">The styles are editable now in the **Styles** pane.</span></span>  

:::image type="complex" source="../../media/2020/06/css-in-js.msft.png" alt-text="Экспериментальная функция" lightbox="../../media/2020/06/css-in-js.msft.png":::
   <span data-ttu-id="ba8d9-183">Изменение `background` свойства `h1` стиля, добавленного в значение `CSSStyleSheet` FROM `pink` `lightblue` .</span><span class="sxs-lookup"><span data-stu-id="ba8d9-183">Changing the `background` property of the `h1` styles added with `CSSStyleSheet` from `pink` to `lightblue`.</span></span>
:::image-end:::  

<span data-ttu-id="ba8d9-184">Придайте этой функции [пример с использованием CSS-in-JS][CodepenZoherghadyaliAbdgrpz].</span><span class="sxs-lookup"><span data-stu-id="ba8d9-184">Give this feature a try with a [sample that uses CSS-in-JS][CodepenZoherghadyaliAbdgrpz].</span></span>

<span data-ttu-id="ba8d9-185">[#946975][CR946975] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="ba8d9-185">Chromium issue [#946975][CR946975]</span></span>  

### <span data-ttu-id="ba8d9-186">Lighthouse 6 на панели Lighthouse</span><span class="sxs-lookup"><span data-stu-id="ba8d9-186">Lighthouse 6 in the Lighthouse panel</span></span>  

<span data-ttu-id="ba8d9-187">Панель **Lighthouse** теперь работает под управлением Lighthouse 6.</span><span class="sxs-lookup"><span data-stu-id="ba8d9-187">The **Lighthouse** panel is now running Lighthouse 6.</span></span>  <span data-ttu-id="ba8d9-188">Полный список всех изменений можно найти в разделе [заметки о выпуске 6.0.0][GithubGoogleChromeLighthouse600].</span><span class="sxs-lookup"><span data-stu-id="ba8d9-188">For a full list of all changes, see [v6.0.0 release notes][GithubGoogleChromeLighthouse600].</span></span>  

<span data-ttu-id="ba8d9-189">Lighthouse 6,0 предлагает три новые метрики для отчета: самую крупную краску \ (LCP \), интегральная схема сдвига \ (CLS \) и общее время блокировки \ (TBT \).</span><span class="sxs-lookup"><span data-stu-id="ba8d9-189">Lighthouse 6.0 introduces three new metrics to the report:  Largest Contentful Paint \(LCP\), Cumulative Layout Shift \(CLS\), and Total Blocking Time \(TBT\).</span></span>  

<span data-ttu-id="ba8d9-190">Формула оценки производительности также была изменена в соответствии с тем, чтобы лучше понять процесс загрузки пользователя.</span><span class="sxs-lookup"><span data-stu-id="ba8d9-190">The performance score formula has also been reweighted to better reflect the loading experience of the user.</span></span>  

<span data-ttu-id="ba8d9-191">[#772558][CR772558] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="ba8d9-191">Chromium issue [#772558][CR772558]</span></span>  

#### <span data-ttu-id="ba8d9-192">Устаревшее изображение для первого осмысленного изображения</span><span class="sxs-lookup"><span data-stu-id="ba8d9-192">First Meaningful Paint deprecation</span></span>  

<span data-ttu-id="ba8d9-193">Первый значащий графический редактор (FMP \ "\" \ "\") устарел в Lighthouse 6,0.</span><span class="sxs-lookup"><span data-stu-id="ba8d9-193">First Meaningful Paint \(FMP\) is deprecated in Lighthouse 6.0.</span></span>  <span data-ttu-id="ba8d9-194">FMP также был удален из панели **Performance** .</span><span class="sxs-lookup"><span data-stu-id="ba8d9-194">FMP has also been removed from the **Performance** panel.</span></span>  <span data-ttu-id="ba8d9-195">**Самая крупная краска с содержимым** — Рекомендуемая замена для fmp.</span><span class="sxs-lookup"><span data-stu-id="ba8d9-195">**Largest Contentful Paint** is the recommended replacement for FMP.</span></span>  <!--See [First Meaningful Paint][WebDevFirstMeaningfulPaint] for an explanation of why it was deprecated.  -->  

<!--todo: add Largest Contentful Paint when section available  -->  
<!--todo: add First Meaningful Paint link and note when available  -->  

<span data-ttu-id="ba8d9-196">[#1096008][CR1096008] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="ba8d9-196">Chromium issue [#1096008][CR1096008]</span></span>  

### <span data-ttu-id="ba8d9-197">Поддержка новых функций JavaScript</span><span class="sxs-lookup"><span data-stu-id="ba8d9-197">Support for new JavaScript features</span></span>  

<span data-ttu-id="ba8d9-198">В DevTools теперь улучшена поддержка некоторых последних языковых функций JavaScript.</span><span class="sxs-lookup"><span data-stu-id="ba8d9-198">DevTools now has better support for some of the latest JavaScript language features.</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="ba8d9-199">[Необязательное автозавершение цепочки цепочек][V8DevOptionalChaining]</span><span class="sxs-lookup"><span data-stu-id="ba8d9-199">[Optional chaining][V8DevOptionalChaining] syntax autocompletion</span></span>  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="ba8d9-200">Автоматическое завершение свойств в **консоли** теперь поддерживает дополнительный синтаксис цепочек, например  `name?.` теперь он работает и в дополнение к нему `name.` `name[` .</span><span class="sxs-lookup"><span data-stu-id="ba8d9-200">Property auto-completion in the **Console** now supports optional chaining syntax, for example,  `name?.` now works in addition to `name.` and `name[`.</span></span>  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      <span data-ttu-id="ba8d9-201">Подсветка синтаксиса для [закрытых полей][V8DevClassFieldsPrivate]</span><span class="sxs-lookup"><span data-stu-id="ba8d9-201">Syntax highlighting for [private fields][V8DevClassFieldsPrivate]</span></span>  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="ba8d9-202">закрытые поля класса теперь правильно выделены синтаксисом и печатаются на панели « **источники** ».</span><span class="sxs-lookup"><span data-stu-id="ba8d9-202">private class fields are now properly syntax-highlighted and pretty-printed in the **Sources** panel.</span></span>  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      <span data-ttu-id="ba8d9-203">Выделение синтаксиса для [непустого оператора слияния][V8DevNullishCoalescing]</span><span class="sxs-lookup"><span data-stu-id="ba8d9-203">Syntax highlighting for [Nullish coalescing operator][V8DevNullishCoalescing]</span></span>
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="ba8d9-204">DevTools правильно — печатает на панели « **источники** » оператор объединения без значений NULL.</span><span class="sxs-lookup"><span data-stu-id="ba8d9-204">DevTools now properly pretty-prints the nullish coalescing operator in the **Sources** panel.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="ba8d9-205">Проблемы с Chromium [#1073903][CR1073903], [#1083214][CR1083214] [#1083797][CR1083797]</span><span class="sxs-lookup"><span data-stu-id="ba8d9-205">Chromium issues [#1073903][CR1073903], [#1083214][CR1083214], [#1083797][CR1083797]</span></span>  

### <span data-ttu-id="ba8d9-206">Новые предупреждения о сочетаниях клавиш для приложения в области манифеста</span><span class="sxs-lookup"><span data-stu-id="ba8d9-206">New app shortcut warnings in the Manifest pane</span></span>  

<span data-ttu-id="ba8d9-207">**Сочетания клавиш** для работы с приложениями помогают пользователям быстро запускать наиболее распространенные или Рекомендуемые задачи в веб-приложении.</span><span class="sxs-lookup"><span data-stu-id="ba8d9-207">**App shortcuts** help users quickly start common or recommended tasks within a web app.</span></span>  

<!--todo: add App shortcuts when section is live  -->  

<span data-ttu-id="ba8d9-208">В области **манифеста** отображаются предупреждения для указанных ниже условий.</span><span class="sxs-lookup"><span data-stu-id="ba8d9-208">The **Manifest** pane now shows warnings for the following conditions.</span></span>  

* <span data-ttu-id="ba8d9-209">Значки сочетаний клавиш приложения меньше 96x96 пикселей</span><span class="sxs-lookup"><span data-stu-id="ba8d9-209">The app shortcut icons are smaller than 96x96 pixels</span></span>  
* <span data-ttu-id="ba8d9-210">Значки сочетаний клавиш приложения и манифеста не квадратны \ (так как значки игнорируются)</span><span class="sxs-lookup"><span data-stu-id="ba8d9-210">The app shortcut icons and manifest icons are not square \(since the icons are ignored\)</span></span>  

:::image type="complex" source="../../media/2020/06/app-shortcut-warnings.msft.png" alt-text="Экспериментальная функция" lightbox="../../media/2020/06/app-shortcut-warnings.msft.png":::
   <span data-ttu-id="ba8d9-212">Предупреждения о сочетаниях клавиш для приложения</span><span class="sxs-lookup"><span data-stu-id="ba8d9-212">App shortcut warnings</span></span>  
:::image-end:::  

<span data-ttu-id="ba8d9-213">[#955497][CR955497] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="ba8d9-213">Chromium issue [#955497][CR955497]</span></span>  

### <span data-ttu-id="ba8d9-214">Последовательная отображение вычисляемой области</span><span class="sxs-lookup"><span data-stu-id="ba8d9-214">Consistent display of the Computed pane</span></span>  

<span data-ttu-id="ba8d9-215">**Вычисляемая** область на панели " **элементы** " теперь отображается единообразно в виде области на всех размерах окна просмотра.</span><span class="sxs-lookup"><span data-stu-id="ba8d9-215">The **Computed** pane in the **Elements** panel now displays consistently as a pane across all viewport sizes.</span></span>  <span data-ttu-id="ba8d9-216">Ранее **Вычисляемая** область была объединена в области " **стили** ", когда ширина окна просмотра DevTools была узкой.</span><span class="sxs-lookup"><span data-stu-id="ba8d9-216">Previously the **Computed** pane merged inside the **Styles** pane when the width of the DevTools viewport was narrow.</span></span>  

:::image type="complex" source="../../media/2020/06/computed-pane.msft.png" alt-text="Экспериментальная функция" lightbox="../../media/2020/06/computed-pane.msft.png":::
   <span data-ttu-id="ba8d9-218">**Вычисляемая** область последовательно отображается как отдельная область, даже если DevTools узким.</span><span class="sxs-lookup"><span data-stu-id="ba8d9-218">The **Computed** pane consistently displays as a separate pane even when the DevTools are narrow.</span></span>
:::image-end:::  

<span data-ttu-id="ba8d9-219">[#1073899][CR1073899] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="ba8d9-219">Chromium issue [#1073899][CR1073899]</span></span>  

### <span data-ttu-id="ba8d9-220">Смещения байт-кода для файлов сборки</span><span class="sxs-lookup"><span data-stu-id="ba8d9-220">Bytecode offsets for WebAssembly files</span></span>  

<span data-ttu-id="ba8d9-221">DevTools теперь использует смещения байт-кода для отображения номеров строк Wasm дизассемблированного кода.</span><span class="sxs-lookup"><span data-stu-id="ba8d9-221">DevTools now uses bytecode offsets for displaying line numbers of Wasm disassembly.</span></span>  
<span data-ttu-id="ba8d9-222">Номера строк упрощают просмотр двоичных данных и более последовательную работу, так как среда выполнения Wasm ссылается на расположение.</span><span class="sxs-lookup"><span data-stu-id="ba8d9-222">The line numbers make it clearer that you are looking at binary data, and is more consistent with how the Wasm runtime references locations.</span></span>  

<span data-ttu-id="ba8d9-223">[#1071432][CR1071432] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="ba8d9-223">Chromium issue [#1071432][CR1071432]</span></span>  

### <span data-ttu-id="ba8d9-224">Построчное копирование и вырезание на панели «источники»</span><span class="sxs-lookup"><span data-stu-id="ba8d9-224">Line-wise copy and cut in Sources Panel</span></span>  

<span data-ttu-id="ba8d9-225">При копировании или вырезании без выделения в [редакторе палитры «источники][DevtoolsSourcesEditCssJavascript]» DevTools копирует или вырезает текущую строку содержимого.</span><span class="sxs-lookup"><span data-stu-id="ba8d9-225">When performing copy or cut with no selection in the [Sources panel editor][DevtoolsSourcesEditCssJavascript], DevTools copies or cuts the current line of content.</span></span>  

:::image type="complex" source="../../media/2020/06/line-wise-cut.msft.png" alt-text="Экспериментальная функция" lightbox="../../media/2020/06/line-wise-cut.msft.png":::
   <span data-ttu-id="ba8d9-227">С курсором в конце строки 5 копируется вся строка из **pen.js** в DevTools и вставляется в [код Visual Studio][VSCode].</span><span class="sxs-lookup"><span data-stu-id="ba8d9-227">With the cursor at the end of Line 5, copying the whole line from **pen.js** in the DevTools and pasting in [Visual Studio Code][VSCode].</span></span>
:::image-end:::  

<span data-ttu-id="ba8d9-228">[#800028][CR800028] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="ba8d9-228">Chromium issue [#800028][CR800028]</span></span>

### <span data-ttu-id="ba8d9-229">Обновления параметров консоли</span><span class="sxs-lookup"><span data-stu-id="ba8d9-229">Console Settings updates</span></span>  

#### <span data-ttu-id="ba8d9-230">Разгруппирование одинаковых сообщений консоли</span><span class="sxs-lookup"><span data-stu-id="ba8d9-230">Ungroup same console messages</span></span>  

<span data-ttu-id="ba8d9-231">Для повторяющихся сообщений **Группа одинаковый** переключатель в разделе Параметры консоли будет применена.</span><span class="sxs-lookup"><span data-stu-id="ba8d9-231">The **Group similar** toggle in Console Settings now applies to duplicate messages.</span></span>  <span data-ttu-id="ba8d9-232">Ранее она была применена к аналогичным сообщениям.</span><span class="sxs-lookup"><span data-stu-id="ba8d9-232">Previously it just applied to similar messages.</span></span>  

<span data-ttu-id="ba8d9-233">Например, ранее DevTools не разгруппирование сообщений, несмотря на то, что `hello` флажок **Group похоже** не установлен.</span><span class="sxs-lookup"><span data-stu-id="ba8d9-233">For example, previously, DevTools did not ungroup the `hello` messages even though **Group similar** is unchecked.</span></span>  <span data-ttu-id="ba8d9-234">Теперь `hello` сообщения разгруппированы.</span><span class="sxs-lookup"><span data-stu-id="ba8d9-234">Now, the `hello` messages are ungrouped.</span></span>  

:::image type="complex" source="../../media/2020/06/ungroup-similar.msft.png" alt-text="Экспериментальная функция" lightbox="../../media/2020/06/ungroup-similar.msft.png":::
   <span data-ttu-id="ba8d9-236">Если флажок " **Группировать как** " не установлен, `hello` сообщения разносятся в разгруппирование</span><span class="sxs-lookup"><span data-stu-id="ba8d9-236">When **Group similar** is unchecked, the `hello` messages are ungrouped</span></span>
:::image-end:::  

<span data-ttu-id="ba8d9-237">Придайте этой функции [пример, который отправляет на консоль повторяющиеся сообщения][CodepenZoherghadyaliZyrjgdJ].</span><span class="sxs-lookup"><span data-stu-id="ba8d9-237">Give this feature a try with a [sample that sends duplicate messages to the Console][CodepenZoherghadyaliZyrjgdJ].</span></span>  

<span data-ttu-id="ba8d9-238">[#1082963][CR1082963] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="ba8d9-238">Chromium issue [#1082963][CR1082963]</span></span>  

### <span data-ttu-id="ba8d9-239">Сохранение только выбранных контекстных параметров</span><span class="sxs-lookup"><span data-stu-id="ba8d9-239">Persisting Selected context only settings</span></span>  

<span data-ttu-id="ba8d9-240">**Выбранный контекст** теперь сохраняется только в параметрах консоли.</span><span class="sxs-lookup"><span data-stu-id="ba8d9-240">The **Selected context only** settings in Console Settings is now persisted.</span></span>  <span data-ttu-id="ba8d9-241">Ранее параметры были сброшены каждый раз при закрытии и повторном открытии DevTools.</span><span class="sxs-lookup"><span data-stu-id="ba8d9-241">Previously the settings were reset every time you closed and reopened DevTools.</span></span>  <span data-ttu-id="ba8d9-242">Изменение приводит к поведению параметров с другими параметрами консоли.</span><span class="sxs-lookup"><span data-stu-id="ba8d9-242">The change makes the setting behavior consistent with other Console Settings options.</span></span>  

:::image type="complex" source="../../media/2020/06/selected-context.msft.png" alt-text="Экспериментальная функция" lightbox="../../media/2020/06/selected-context.msft.png":::
   <span data-ttu-id="ba8d9-244">Параметр " **только выбранный контекст** "</span><span class="sxs-lookup"><span data-stu-id="ba8d9-244">**Selected context only** setting</span></span>  
:::image-end:::  

<span data-ttu-id="ba8d9-245">[#1055875][CR1055875] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="ba8d9-245">Chromium issue [#1055875][CR1055875]</span></span>  

### <span data-ttu-id="ba8d9-246">Обновления панели "производительность"</span><span class="sxs-lookup"><span data-stu-id="ba8d9-246">Performance panel updates</span></span>  

#### <span data-ttu-id="ba8d9-247">Информация кэша компиляции для JavaScript на панели "производительность"</span><span class="sxs-lookup"><span data-stu-id="ba8d9-247">JavaScript compilation cache information in Performance panel</span></span>  

<span data-ttu-id="ba8d9-248">[Данные кэша компиляции для JavaScript][V8DevCodeCaching] теперь всегда отображаются на вкладке "Сводка" на панели "производительность".</span><span class="sxs-lookup"><span data-stu-id="ba8d9-248">[JavaScript compilation cache information][V8DevCodeCaching] is now always displayed in the Summary tab of the Performance panel.</span></span>  <span data-ttu-id="ba8d9-249">Ранее DevTools не показывает ничего, связанного с кэшированием кода, если кэширование кода не произошло.</span><span class="sxs-lookup"><span data-stu-id="ba8d9-249">Previously, DevTools did not show anything related to code caching if code caching did not happen.</span></span>  

:::image type="complex" source="../../media/2020/06/js-compilation-cache.msft.png" alt-text="Экспериментальная функция" lightbox="../../media/2020/06/js-compilation-cache.msft.png":::
   <span data-ttu-id="ba8d9-251">Данные кэша компиляции для JavaScript</span><span class="sxs-lookup"><span data-stu-id="ba8d9-251">JavaScript compilation cache information</span></span>  
:::image-end:::  

<span data-ttu-id="ba8d9-252">[#912581][CR912581] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="ba8d9-252">Chromium issue [#912581][CR912581]</span></span>  

#### <span data-ttu-id="ba8d9-253">Выравнивание времени навигации на панели «производительность»</span><span class="sxs-lookup"><span data-stu-id="ba8d9-253">Navigation timing alignment in the Performance panel</span></span>  

<span data-ttu-id="ba8d9-254">Панель **производительности** , используемая для отображения времени на линейках на основе начала записи.</span><span class="sxs-lookup"><span data-stu-id="ba8d9-254">The **Performance** panel used to show times in the rulers based on when the recording started.</span></span>  <span data-ttu-id="ba8d9-255">Время ожидания изменилось для записей, в которых пользователь осуществляет переход, где DevTools теперь показывает время линейки относительно навигации.</span><span class="sxs-lookup"><span data-stu-id="ba8d9-255">The timing has now changed for recordings where the user navigates, where DevTools now shows ruler times relative to the navigation instead.</span></span>  

:::image type="complex" source="../../media/2020/06/nav-timing.msft.png" alt-text="Экспериментальная функция" lightbox="../../media/2020/06/nav-timing.msft.png":::
   <span data-ttu-id="ba8d9-257">Выравнивание времени навигации на панели « **производительность** »</span><span class="sxs-lookup"><span data-stu-id="ba8d9-257">Align navigation timing in **Performance** panel</span></span>  
:::image-end:::  

<span data-ttu-id="ba8d9-258">Время, для которого `DOMContentLoaded` Первая краска, первая краска и наибольшее количество событий, связанных с содержимым, обновляется в соответствии с началом навигации, а это значит, что время соответствует значению времени, указанное в `PerformanceObserver` .</span><span class="sxs-lookup"><span data-stu-id="ba8d9-258">The times for `DOMContentLoaded`, First Paint, First Contentful Paint, and Largest Contentful Paint events are updated to be relative to the start of the navigation, which means the timing matches the timings reported by `PerformanceObserver`.</span></span>  

<span data-ttu-id="ba8d9-259">[#974550][CR974550] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="ba8d9-259">Chromium issue [#974550][CR974550]</span></span>  

### <span data-ttu-id="ba8d9-260">Новые значки для точек останова, условных точек останова и logpoints</span><span class="sxs-lookup"><span data-stu-id="ba8d9-260">New icons for breakpoints, conditional breakpoints, and logpoints</span></span>  

<span data-ttu-id="ba8d9-261">На панели « **источники** » есть новые дизайны для точек останова, условных точек останова и logpoints.</span><span class="sxs-lookup"><span data-stu-id="ba8d9-261">The **Sources** panel has new designs for breakpoints, conditional breakpoints, and logpoints.</span></span>  <span data-ttu-id="ba8d9-262">Точки останова представлены на красном круге, точно так же, как и в [Visual Studio][VSCode] , и в [Visual Studio][VS].</span><span class="sxs-lookup"><span data-stu-id="ba8d9-262">Breakpoints are represented by a red circle, just like [Visual Studio Code][VSCode] and [Visual Studio][VS].</span></span>  <span data-ttu-id="ba8d9-263">Значки добавляются для различения условных точек останова и logpoints.</span><span class="sxs-lookup"><span data-stu-id="ba8d9-263">Icons are added to differentiate conditional breakpoints and logpoints.</span></span>  

:::image type="complex" source="../../media/2020/06/breakpoints.msft.png" alt-text="Экспериментальная функция" lightbox="../../media/2020/06/breakpoints.msft.png":::
   <span data-ttu-id="ba8d9-265">Точки останова</span><span class="sxs-lookup"><span data-stu-id="ba8d9-265">Breakpoints</span></span>  
:::image-end:::  

<span data-ttu-id="ba8d9-266">[#1041830][CR1041830] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="ba8d9-266">Chromium issue [#1041830][CR1041830]</span></span>  

## <span data-ttu-id="ba8d9-267">Загрузка каналов предварительной версии Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ba8d9-267">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="ba8d9-268">Если вы используете Windows или macOS, рассматривайте в качестве браузера по умолчанию использование [каналов предварительного просмотра Microsoft Edge][MicrosoftEdgePreviewChannels] .</span><span class="sxs-lookup"><span data-stu-id="ba8d9-268">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="ba8d9-269">Каналы предварительного просмотра предоставляют доступ к последним функциям DevTools.</span><span class="sxs-lookup"><span data-stu-id="ba8d9-269">The preview channels give you access to the latest DevTools features.</span></span>  

## <span data-ttu-id="ba8d9-270">Знакомство с Microsoft Edge DevTools Team</span><span class="sxs-lookup"><span data-stu-id="ba8d9-270">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DevtoolsMain]: /microsoft-edge/devtools-guide-chromium "Инструменты разработчика Microsoft EDGE (Chromium) | Документы Microsoft"  
[DevtoolsCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu "Выполнение команд с помощью командного меню Microsoft Edge DevTools | Документы Microsoft"
[DevtoolsCustomizeIndexDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Ящик — настройка Microsoft Edge DevTools | Документы Microsoft"
[DevtoolsExperimentalFeaturesTurnOn]: /microsoft-edge/devtools-guide-chromium/experimental-features#turn-on-experimental-features "Включите экспериментальные функции — экспериментальные функции | Документы Microsoft"  
[DevtoolsIssues]: /microsoft-edge/devtools-guide-chromium/issues "Поиск и устранение проблем с помощью средства Microsoft Edge DevTools "вопросы" | Документы Microsoft"
[DevtoolsSourcesEditCssJavascript]: /microsoft-edge/devtools-guide-chromium/sources#edit-css-and-javascript "Общие сведения об панели редактирования CSS и JavaScript-sources | Документы Microsoft"  
[DevtoolsNetworkIndexLogActivity]: /microsoft-edge/devtools-guide-chromium/network/index#log-network-activity "Регистрация активности сети — проверка активности сети в Microsoft Edge DevTools | Документы Microsoft"

[CodepenZoherghadyaliAbdgrpz]: https://codepen.io/zoherghadyali/full/abdGrPZ "Редактирование стилей для платформ CSS-JS | CodePen"
[CodepenZoherghadyaliZyrjgdJ]: https://codepen.io/zoherghadyali/full/zYrjgdJ "Отправлять повторяющиеся сообщения на консоль | CodePen"
[CodepenRachelweilYzwBzKM]: https://codepen.io/hxlnt/full/YzwBzKM "Пример планировщика сетки CSS | CodePen"

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Ошибки Chromium"  

[CR772558]: https://crbug.com/772558 "DevTools: обновление до последней версии Lighthouse | Ошибки Chromium"  
[CR800028]: https://crbug.com/800028 "Повторяющийся ярлык строки в редакторе средств разработчика не работает после обновления Chrome | Ошибки Chromium"  
[CR912581]: https://crbug.com/912581 "Предоставление сценариев, которые были бы кэшированы в коде с помощью V8 в DevTools/about: Tracing | Ошибки Chromium"  
[CR946975]: https://crbug.com/946975 "Боковая панель "стили DevTools" не работает с сконструированными таблицами стилей | Ошибки Chromium"  
[CR955497]: https://crbug.com/955497 "Контекстное меню значка приложения для PWAs | Ошибки Chromium"  
[CR974550]: https://crbug.com/974550 "Несоответствие метрик между панелью производительности и performanceObserver | Ошибки Chromium"  
[CR1041830]: https://crbug.com/1041830 "Улучшение цветопередачи для точек останова | Ошибки Chromium"  
[CR1055875]: https://crbug.com/1055875 "Значение выбранного контекста параметр консоли не сохраняется после закрытия и повторного открытия средств разработчика | Ошибки Chromium"  
[CR1066579]: https://crbug.com/1066579 "DevTools: Показать ServiceWorkers выбор временной шкалы для запроса на панели "сеть" | Ошибки Chromium"  
[CR1071432]: https://crbug.com/1071432 "Базовые возможности для разработчиков Wasm | Ошибки Chromium"  
[CR1073899]: https://crbug.com/1073899 "Вкладка "вычисляемый стиль" исчезает в режиме отклика | Ошибки Chromium"  
[CR1073903]: https://crbug.com/1073903 "DevTools: выделение синтаксических конструкций не работает с закрытыми полями | Ошибки Chromium"  
[CR1082963]: https://crbug.com/1082963 "Не удается отключить поведение группировки аналогичных сообщений в консоли | Ошибки Chromium"  
[CR1083214]: https://crbug.com/1083214 "Acorn не поддерживает дополнительное объединение | Ошибки Chromium"  
[CR1083797]: https://crbug.com/1083797 "Неправильное распечатка для ненулевого объединения | Ошибки Chromium"  
[CR1096008]: https://crbug.com/1096008 "Удалить FMP | Ошибки Chromium"  
[CR1047356]: https://crbug.com/1047356 "Сетка CSS/гибкая таблица/подсказка для таблиц | Ошибки Chromium"  
[CR1093687]: https://crbug.com/1093687 "Инструмент "создать" для создания и воспроизведения запросов виртуальных сетей | Ошибки Chromium"  
[CR1070378]: https://crbug.com/1070378 "Интегрировать подсказку в DevTools | Ошибки Chromium"  
[CR1069404]: https://crbug.com/1069404 "[Средства разработки] всплывающие элементы мини-приложения слишком узкие | Ошибки Chromium"  
[CR897944]: https://crbug.com/897944 "Перетаскиваемые панели DevTool | Ошибки Chromium"

[GithubGoogleChromeLighthouse600]: https://github.com/GoogleChrome/lighthouse/releases/tag/v6.0.0 "v 6.0.0-GoogleChrome/Lighthouse | GitHub"  

[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=[DevTools%20Docs%20Feedback] "Новая ошибка — MicrosoftDocs/Edge-разработчик"  

[MdnShadowDom]: https://developer.mozilla.org/docs/Web/Web_Components/Using_shadow_DOM "Использование теневой модели DOM | MDN"

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download/ "Каналы предварительной версии Microsoft Edge"  

[VS]: https://visualstudio.microsoft.com/ "Visual Studio"
[VSCode]: https://code.visualstudio.com/ "Код Visual Studio"  

[CsswgDraftsCssom]: https://drafts.csswg.org/cssom "Объектная модель CSS (CSSOM) | Черновики редакторов рабочих групп W3C CSS"  

[PostTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Публикация твита"  
[EdgeDevToolsTwitterAccount]: https://twitter.com/EdgeDevTools "@EdgeDevTools учетной записи Twitter"  

[V8DevClassFieldsPrivate]: https://v8.dev/features/class-fields#private-class-fields "Закрытые поля класса — открытые и закрытые поля класса | V8. Разработки"  
[V8DevCodeCaching]: https://v8.dev/blog/code-caching-for-devs "Кэширование кода для разработчиков JavaScript | V8. Разработки"  
[V8DevNullishCoalescing]: https://v8.dev/features/nullish-coalescing "Ненулевое объединение | V8. Разработки"  
[V8DevOptionalChaining]: https://v8.dev/features/optional-chaining "Дополнительные сцепления | V8. Разработки"  

[WebhintMain]: https://webhint.io "Подсказка"  

[WicgConstructStylesheet]: https://wicg.github.io/construct-stylesheets/ "Объекты стилей, которые вы создаете? Веб-Incubator CG"

<!--[WebDevLighthouseWhatsNew60]: https://web.dev/lighthouse-whats-new-6.0 "What's New in Lighthouse 6.0 | Web.Dev"  -->  
<!--[WebDevVitalsCoreWeb]: https://web.dev/vitals#core-web-vitals "Core Web Vitals - Web Vitals | Web.Dev"  -->  
<!--[WebdevAppShortcuts]: https://alphabet-dev/app-shortcuts "Get things done quickly with app shortcuts | alphabet-dev"  -->  
<!--[WebdevCls]: https://alphabet-dev/cls "Cumulative Layout Shift (CLS) | alphabet-dev"  -->  
<!--[WebdevControlFocus]: https://alphabet-dev/control-focus-with-tabindex "Control focus with tabindex | alphabet-dev"  -->  
<!--[WebdevMeasureSpeedLabField]: https://alphabet-dev/how-to-measure-speed#lab-data-vs-field-data "Lab data vs Field data - How to measure speed? | alphabet-dev"  -->  
<!--[WebdevLabelsText]: https://alphabet-dev/labels-and-text-alternatives "Labels and text alternatives | alphabet-dev"  -->  
<!--[WebdevTbt]: https://alphabet-dev/tbt "Total Blocking Time (TBT) | alphabet-dev"  -->  
<!--[WebFundamentalComponentsShadowdom]: /web/fundamentals/web-components/shadowdom  -->  
<!--[WebDevLcp]: https://web.dev/lcp "Largest Contentful Paint (LCP) | Web.Dev"  -->  
<!--[WebDevFirstMeaningfulPaint]: https://web.dev/first-meaningful-paint "First Meaningful Paint | Web.Dev"  -->  
<!--[WhatsNew201902ConstructableStylesheets]: ../../2019/02/constructable-stylesheets.md "Constructable Stylesheets: seamless reusable styles | Microsoft Docs"  -->  

[TheWebWeWant]: https://webwewant.fyi/ "Требуемый веб-сайт"  

> [!NOTE]
> <span data-ttu-id="ba8d9-319">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ba8d9-319">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="ba8d9-320">Исходная страница [будет найдена, и](https://developers.google.com/web/updates/2020/06/devtools/index) ее можно создать с помощью [Jecelyn Yeen][JecelynYeen] \ (разработчик отвечает, Chrome DevTools \).</span><span class="sxs-lookup"><span data-stu-id="ba8d9-320">The original page is found [here](https://developers.google.com/web/updates/2020/06/devtools/index) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="ba8d9-322">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ba8d9-322">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
