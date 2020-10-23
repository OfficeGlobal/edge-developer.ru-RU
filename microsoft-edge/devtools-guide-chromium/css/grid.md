---
description: Сведения о том, как использовать Microsoft Edge DevTools для просмотра и изменения CSS для страниц CSS.
title: Проверка сетки CSS в Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/22/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 150aea57aa676580b554cc74292671ed567a0a2c
ms.sourcegitcommit: 6e2b26d41a0aa56ac34e6edc7dddd852ddb415b1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/23/2020
ms.locfileid: "11134152"
---
# <span data-ttu-id="d9592-104">Проверка сетки CSS</span><span class="sxs-lookup"><span data-stu-id="d9592-104">Inspect CSS Grid</span></span>  

<span data-ttu-id="d9592-105">В этой статье описано, как определить сетки CSS на веб-сайте и выявить проблемы макета сетки с помощью настраиваемых наложений сетки.</span><span class="sxs-lookup"><span data-stu-id="d9592-105">This article walks you through identifying CSS grids on a website and debugging grid layout issues using customizable grid overlays.</span></span>  

<span data-ttu-id="d9592-106">Примеры, используемые на рисунках в этой статье, взяты из следующих веб-страниц.</span><span class="sxs-lookup"><span data-stu-id="d9592-106">The examples used in the figures in this article are taken from the following webpages.</span></span>  

*   [<span data-ttu-id="d9592-107">Поле "фруктов"</span><span class="sxs-lookup"><span data-stu-id="d9592-107">Fruit box</span></span>][JecFyiDemoCssGridFruit]  
*   [<span data-ttu-id="d9592-108">Поле питанию</span><span class="sxs-lookup"><span data-stu-id="d9592-108">Snack box</span></span>][JecFyiDemoCssGridSnack]  

## <span data-ttu-id="d9592-109">Перед началом работы</span><span class="sxs-lookup"><span data-stu-id="d9592-109">Before you begin</span></span>  

<span data-ttu-id="d9592-110">Сетка CSS — это мощная парадигма макета для веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="d9592-110">CSS Grid is a powerful layout paradigm for the web.</span></span>  <span data-ttu-id="d9592-111">Это удобное место для изучения сетки каскадных стилей, а многие функции — руководство по [макету сетки CSS][MdnCssGridLayout] на MDN.</span><span class="sxs-lookup"><span data-stu-id="d9592-111">A great place to get started learning about CSS Grid and the many features is the [CSS Grid Layout guide][MdnCssGridLayout] on MDN.</span></span>  

## <span data-ttu-id="d9592-112">Знакомство с таблицами CSS</span><span class="sxs-lookup"><span data-stu-id="d9592-112">Discover CSS grids</span></span>  

<span data-ttu-id="d9592-113">Если на странице применен HTML-элемент `display: grid` , на `display: inline-grid` `grid` панели " [элементы][DevtoolsGuideChromiumOpen] " рядом с ним отображается индикатор.</span><span class="sxs-lookup"><span data-stu-id="d9592-113">When an HTML element on your page has `display: grid` or `display: inline-grid` applied to it, a `grid` badge is displayed next to it in the [Elements][DevtoolsGuideChromiumOpen] panel.</span></span>  

:::image type="complex" source="../media/grid-discover-grid.msft.png" alt-text="Сетка &quot;Поиск&quot;" lightbox="../media/grid-discover-grid.msft.png":::
   <span data-ttu-id="d9592-115">Сетка "Поиск"</span><span class="sxs-lookup"><span data-stu-id="d9592-115">Discover grid</span></span>  
:::image-end:::  

<span data-ttu-id="d9592-116">Щелкните значок, чтобы включить или отключить наложение сетки на странице.</span><span class="sxs-lookup"><span data-stu-id="d9592-116">Select the badge to toggle the display of a grid overlay on the page.</span></span>  <span data-ttu-id="d9592-117">Для отображения положения линий сетки и дорожек на элементе появляется наложенный указатель на элемент в виде сетки.</span><span class="sxs-lookup"><span data-stu-id="d9592-117">The overlay appears over the element, laid out like a grid to display the position of the grid lines and tracks:</span></span>  

:::image type="complex" source="../media/grid-highlight-grid.msft.png" alt-text="Сетка &quot;Поиск&quot;" lightbox="../media/grid-highlight-grid.msft.png":::
   <span data-ttu-id="d9592-119">Отображение значка сетки</span><span class="sxs-lookup"><span data-stu-id="d9592-119">Toggle grid badge</span></span>  
:::image-end:::  

<span data-ttu-id="d9592-120">Открытие области " **Макет** ".</span><span class="sxs-lookup"><span data-stu-id="d9592-120">Open the **Layout** pane.</span></span>  <span data-ttu-id="d9592-121">Если на странице включены сетки, в области **макетов** имеется раздел **Grid** , содержащий ряд параметров для просмотра сетки.</span><span class="sxs-lookup"><span data-stu-id="d9592-121">When grids are included on a page, the **Layout** pane includes a **Grid** section containing a number of options for viewing the grids.</span></span>  

:::image type="complex" source="../media/grid-layout-pane.msft.png" alt-text="Сетка &quot;Поиск&quot;" lightbox="../media/grid-layout-pane.msft.png":::
   <span data-ttu-id="d9592-123">Область " **Макет** "</span><span class="sxs-lookup"><span data-stu-id="d9592-123">**Layout** pane</span></span>  
:::image-end:::  

<span data-ttu-id="d9592-124">Раздел **Grid** в области " **Макет** " включает следующие 2 подраздела.</span><span class="sxs-lookup"><span data-stu-id="d9592-124">The **Grid** section in the **Layout** pane contains the following 2 sub-sections.</span></span>  

*   <span data-ttu-id="d9592-125">Параметры отображения наложения</span><span class="sxs-lookup"><span data-stu-id="d9592-125">Overlay display settings</span></span>  
*   <span data-ttu-id="d9592-126">Наложения сетки</span><span class="sxs-lookup"><span data-stu-id="d9592-126">Grid overlays</span></span>  

<!--todo: @zoher verify the details for each of the sub-sections.  -->  

## <span data-ttu-id="d9592-127">Параметры отображения наложения</span><span class="sxs-lookup"><span data-stu-id="d9592-127">Overlay display settings</span></span>  

<span data-ttu-id="d9592-128">**Параметры отображения наложения** состоят из следующих двух частей.</span><span class="sxs-lookup"><span data-stu-id="d9592-128">The **Overlay display settings** consists of following 2 parts.</span></span>  

*   <span data-ttu-id="d9592-129">В раскрывающемся меню выберите один из следующих параметров.</span><span class="sxs-lookup"><span data-stu-id="d9592-129">Choose one of the following options from the dropdown menu.</span></span>  
    
    | <span data-ttu-id="d9592-130">Параметр линии</span><span class="sxs-lookup"><span data-stu-id="d9592-130">Line option</span></span> | <span data-ttu-id="d9592-131">Сведения</span><span class="sxs-lookup"><span data-stu-id="d9592-131">Details</span></span> |  
    |:--- |:--- |  
    | **<span data-ttu-id="d9592-132">Скрытие меток линий</span><span class="sxs-lookup"><span data-stu-id="d9592-132">Hide line labels</span></span>** | <span data-ttu-id="d9592-133">Скрыть метки линий для каждой наложения сетки.</span><span class="sxs-lookup"><span data-stu-id="d9592-133">Hide the labels of the lines for each grid overlay.</span></span> |  
    | **<span data-ttu-id="d9592-134">Показывать номера строк</span><span class="sxs-lookup"><span data-stu-id="d9592-134">Show line numbers</span></span>** | <span data-ttu-id="d9592-135">Отображение номеров строк для каждого перекрытия сетки \ (выбрано по умолчанию \).</span><span class="sxs-lookup"><span data-stu-id="d9592-135">Display the numbers of the lines for each grid overlay \(selected by default\).</span></span> |  
    | **<span data-ttu-id="d9592-136">Показывать названия строк</span><span class="sxs-lookup"><span data-stu-id="d9592-136">Show line names</span></span>** | <span data-ttu-id="d9592-137">Отображение названий строк для каждого перекрытия сетки при указании имен.</span><span class="sxs-lookup"><span data-stu-id="d9592-137">Display the names of the lines for each grid overlay when names are provided.</span></span> |  
    
*  <span data-ttu-id="d9592-138">Установите флажок рядом с приведенными ниже параметрами.</span><span class="sxs-lookup"><span data-stu-id="d9592-138">Choose the checkbox next the following options.</span></span>  
    
    | <span data-ttu-id="d9592-139">Параметр</span><span class="sxs-lookup"><span data-stu-id="d9592-139">Option</span></span> | <span data-ttu-id="d9592-140">Сведения</span><span class="sxs-lookup"><span data-stu-id="d9592-140">Details</span></span> |  
    |:--- |:--- |  
    | **<span data-ttu-id="d9592-141">Показать размеры дорожек</span><span class="sxs-lookup"><span data-stu-id="d9592-141">Show track sizes</span></span>**  | <span data-ttu-id="d9592-142">Отображение и скрытие размера дорожек.</span><span class="sxs-lookup"><span data-stu-id="d9592-142">Display \(or hide\) the sizes of the tracks.</span></span> |  
    | **<span data-ttu-id="d9592-143">Показать имена областей</span><span class="sxs-lookup"><span data-stu-id="d9592-143">Show area names</span></span>** | <span data-ttu-id="d9592-144">Выводится название области (или скрыть ее), когда указаны имена.</span><span class="sxs-lookup"><span data-stu-id="d9592-144">Display \(or hide\) the names of the area, when names are provided.</span></span> |  
    | **<span data-ttu-id="d9592-145">Увеличение линий сетки</span><span class="sxs-lookup"><span data-stu-id="d9592-145">Extend grid lines</span></span>** | <span data-ttu-id="d9592-146">Отображает (или скрывает) расширения размеров сетки вдоль каждой оси.</span><span class="sxs-lookup"><span data-stu-id="d9592-146">Displays \(or hides\) the extensions of the grid dimensions along each axis.</span></span>  <span data-ttu-id="d9592-147">По умолчанию линии сетки отображаются только в элементе с `display: grid` `display: inline-grid` установленным для него или CSS.</span><span class="sxs-lookup"><span data-stu-id="d9592-147">By default, grid lines are only shown inside the element with `display: grid` or `display: inline-grid` CSS set on it.</span></span> |  
    
<span data-ttu-id="d9592-148">В следующих разделах приведены подробные сведения о каждом из **параметров отображения наложения**.</span><span class="sxs-lookup"><span data-stu-id="d9592-148">The following sections provide details for each of the **Overlay display settings**.</span></span>  

### <span data-ttu-id="d9592-149">Показывать номера строк</span><span class="sxs-lookup"><span data-stu-id="d9592-149">Show line numbers</span></span>  

<span data-ttu-id="d9592-150">По умолчанию в наложение сетки отображаются положительные и отрицательные номера строк.</span><span class="sxs-lookup"><span data-stu-id="d9592-150">By default, the positive and negative line numbers are displayed on the grid overlay.</span></span>  

<span data-ttu-id="d9592-151">Для получения дополнительных сведений об отрицательных числах в наложение сетки перейдите в раздел [расположение на строке с таблицей каскадных стилей][MdnLineBasedPlacementCssGrid].</span><span class="sxs-lookup"><span data-stu-id="d9592-151">For more information about negative numbers in the grid overlay, navigate to [Line-based placement with CSS Grid][MdnLineBasedPlacementCssGrid].</span></span>  

:::image type="complex" source="../media/grid-show-line-numbers.msft.png" alt-text="Сетка &quot;Поиск&quot;" lightbox="../media/grid-show-line-numbers.msft.png":::
   <span data-ttu-id="d9592-153">Отображение номеров строк</span><span class="sxs-lookup"><span data-stu-id="d9592-153">Display line numbers</span></span>  
:::image-end:::  

### <span data-ttu-id="d9592-154">Скрытие меток линий</span><span class="sxs-lookup"><span data-stu-id="d9592-154">Hide line labels</span></span>  

<span data-ttu-id="d9592-155">Выберите команду **Скрыть метки линии** , чтобы скрыть номера строк.</span><span class="sxs-lookup"><span data-stu-id="d9592-155">Select **Hide line labels** to hide the line numbers.</span></span>  

:::image type="complex" source="../media/grid-hide-line-labels.msft.png" alt-text="Сетка &quot;Поиск&quot;" lightbox="../media/grid-hide-line-labels.msft.png":::
   <span data-ttu-id="d9592-157">Скрытие меток линий</span><span class="sxs-lookup"><span data-stu-id="d9592-157">Hide line labels</span></span>  
:::image-end:::  

### <span data-ttu-id="d9592-158">Показывать названия строк</span><span class="sxs-lookup"><span data-stu-id="d9592-158">Show line names</span></span>  

<!--todo: @rachel verify the link and text for line name -->  
<span data-ttu-id="d9592-159">Чтобы получить дополнительные сведения о названиях линий в наложения сетки, перейдите в раздел [макет с помощью именованных линий сетки][MdnLayoutUsingNamedGridLines].</span><span class="sxs-lookup"><span data-stu-id="d9592-159">For more information about line names in the grid overlay, navigate to [Layout using named grid lines][MdnLayoutUsingNamedGridLines].</span></span>  

<span data-ttu-id="d9592-160">Выберите **Показывать названия строк** , чтобы просмотреть названия строк вместо чисел.</span><span class="sxs-lookup"><span data-stu-id="d9592-160">Select **Show line names** to view the line names instead of numbers.</span></span>  <span data-ttu-id="d9592-161">В примере 4 строки имеют имена: `left` , `middle1` , `middle2` и `right` .</span><span class="sxs-lookup"><span data-stu-id="d9592-161">In the example, 4 lines have names: `left`, `middle1`, `middle2`, and `right`.</span></span>  

<!--In the demo, **orange** element spans from left to right, with `grid-column: left` and `grid-column: right` CSS.  Showing line names makes it easier to visualize the start and end position of the element.  -->  

:::image type="complex" source="../media/grid-show-line-names.msft.png" alt-text="Сетка &quot;Поиск&quot;" lightbox="../media/grid-show-line-names.msft.png":::
   **<span data-ttu-id="d9592-163">Показывать названия строк</span><span class="sxs-lookup"><span data-stu-id="d9592-163">Show line names</span></span>**  
:::image-end:::  

### <span data-ttu-id="d9592-164">Показать размеры дорожек</span><span class="sxs-lookup"><span data-stu-id="d9592-164">Show track sizes</span></span>  

<span data-ttu-id="d9592-165">Установите флажок **Показывать размеры дорожек** для просмотра размеров сетки.</span><span class="sxs-lookup"><span data-stu-id="d9592-165">Enable the **Show track sizes** checkbox to view the track sizes of the grid.</span></span>  

<span data-ttu-id="d9592-166">DevTools отображает `[authored size]` и `[computed size]` в каждой метке строки.</span><span class="sxs-lookup"><span data-stu-id="d9592-166">DevTools displays `[authored size]` and `[computed size]` in each line label.</span></span>  

| <span data-ttu-id="d9592-167">Size</span><span class="sxs-lookup"><span data-stu-id="d9592-167">Size</span></span> | <span data-ttu-id="d9592-168">Сведения</span><span class="sxs-lookup"><span data-stu-id="d9592-168">Details</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="d9592-169">Авторский размер</span><span class="sxs-lookup"><span data-stu-id="d9592-169">authored size</span></span>** | <span data-ttu-id="d9592-170">Размер, определенный в таблице стилей \ (опущено, если не определено).</span><span class="sxs-lookup"><span data-stu-id="d9592-170">The size defined in stylesheet \(omitted if not defined\).</span></span> |  
| **<span data-ttu-id="d9592-171">вычисляемый размер</span><span class="sxs-lookup"><span data-stu-id="d9592-171">computed size</span></span>** | <span data-ttu-id="d9592-172">Реальный размер на экране.</span><span class="sxs-lookup"><span data-stu-id="d9592-172">The actual size on screen.</span></span> |  

<span data-ttu-id="d9592-173">В роликах `snack-box` размеры столбцов определяются в `grid-template-columns:1fr 2fr;` CSS.</span><span class="sxs-lookup"><span data-stu-id="d9592-173">In the demo, the `snack-box` column sizes are defined in the `grid-template-columns:1fr 2fr;` CSS.</span></span>  <span data-ttu-id="d9592-174">Таким образом, Метки строк столбцов выводят как созданные, так и вычисляемые размеры.</span><span class="sxs-lookup"><span data-stu-id="d9592-174">Therefore, the column line labels display both authored and computed sizes.</span></span>  

| <span data-ttu-id="d9592-175">Размер дорожки</span><span class="sxs-lookup"><span data-stu-id="d9592-175">Track size</span></span> | <span data-ttu-id="d9592-176">Авторский размер</span><span class="sxs-lookup"><span data-stu-id="d9592-176">Authored size</span></span> | <span data-ttu-id="d9592-177">Вычисляемый размер</span><span class="sxs-lookup"><span data-stu-id="d9592-177">Computed size</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="d9592-178">**1fr** &#x2022; **96.66 px**</span><span class="sxs-lookup"><span data-stu-id="d9592-178">**1fr** &#x2022; **96.66px**</span></span> | <span data-ttu-id="d9592-179">1fr</span><span class="sxs-lookup"><span data-stu-id="d9592-179">1fr</span></span> | <span data-ttu-id="d9592-180">96.66 px</span><span class="sxs-lookup"><span data-stu-id="d9592-180">96.66px</span></span> |  
| <span data-ttu-id="d9592-181">**2fr** &#x2022; **193.32 px**</span><span class="sxs-lookup"><span data-stu-id="d9592-181">**2fr** &#x2022; **193.32px**</span></span> | <span data-ttu-id="d9592-182">2fr</span><span class="sxs-lookup"><span data-stu-id="d9592-182">2fr</span></span> | <span data-ttu-id="d9592-183">193.32 px</span><span class="sxs-lookup"><span data-stu-id="d9592-183">193.32px</span></span> |  

<span data-ttu-id="d9592-184">В названиях строк строки отображаются только вычисляемые размеры, так как в таблице стилей не определена ни одна из размеров строк.</span><span class="sxs-lookup"><span data-stu-id="d9592-184">The row line labels display only computed sizes, since there are no row sizes defined in the stylesheet.</span></span>  

| <span data-ttu-id="d9592-185">Размер дорожки</span><span class="sxs-lookup"><span data-stu-id="d9592-185">Track size</span></span> | <span data-ttu-id="d9592-186">Авторский размер</span><span class="sxs-lookup"><span data-stu-id="d9592-186">Authored size</span></span> | <span data-ttu-id="d9592-187">Вычисляемый размер</span><span class="sxs-lookup"><span data-stu-id="d9592-187">Computed size</span></span> |  
|:--- |:--- |:--- |  
| **<span data-ttu-id="d9592-188">80px</span><span class="sxs-lookup"><span data-stu-id="d9592-188">80px</span></span>** | &nbsp;| <span data-ttu-id="d9592-189">80px</span><span class="sxs-lookup"><span data-stu-id="d9592-189">80px</span></span> |  
| **<span data-ttu-id="d9592-190">80px</span><span class="sxs-lookup"><span data-stu-id="d9592-190">80px</span></span>** | &nbsp;| <span data-ttu-id="d9592-191">80px</span><span class="sxs-lookup"><span data-stu-id="d9592-191">80px</span></span> |  

:::image type="complex" source="../media/grid-show-track-sizes.msft.png" alt-text="Сетка &quot;Поиск&quot;" lightbox="../media/grid-show-track-sizes.msft.png":::
   **<span data-ttu-id="d9592-193">Показать размеры дорожек</span><span class="sxs-lookup"><span data-stu-id="d9592-193">Show track sizes</span></span>**  
:::image-end:::  

### <span data-ttu-id="d9592-194">Показать имена областей</span><span class="sxs-lookup"><span data-stu-id="d9592-194">Show area names</span></span>  

<span data-ttu-id="d9592-195">Чтобы просмотреть названия областей, установите флажок **Показывать имена областей** .</span><span class="sxs-lookup"><span data-stu-id="d9592-195">To view the area names, enable the **Show area names** checkbox.</span></span>  <span data-ttu-id="d9592-196">В примере таблица Grid имеет три области: **Top**, **bottom1** и **bottom2**.</span><span class="sxs-lookup"><span data-stu-id="d9592-196">In the example, there are 3 areas in the grid: **top**, **bottom1** and **bottom2**.</span></span>  

:::image type="complex" source="../media/grid-show-area-names.msft.png" alt-text="Сетка &quot;Поиск&quot;" lightbox="../media/grid-show-area-names.msft.png":::
   **<span data-ttu-id="d9592-198">Показать имена областей</span><span class="sxs-lookup"><span data-stu-id="d9592-198">Show area names</span></span>**  
:::image-end:::  

### <span data-ttu-id="d9592-199">Увеличение линий сетки</span><span class="sxs-lookup"><span data-stu-id="d9592-199">Extend grid lines</span></span>  

<span data-ttu-id="d9592-200">Установите флажок **удлинить линии сетки** , чтобы распространить линии сетки по краям окна просмотра на каждой оси.</span><span class="sxs-lookup"><span data-stu-id="d9592-200">Enable the **Extend grid lines** checkbox to extend the grid lines to the edge of the viewport along each axis.</span></span>  

:::image type="complex" source="../media/grid-extend-grid-lines.msft.png" alt-text="Сетка &quot;Поиск&quot;" lightbox="../media/grid-extend-grid-lines.msft.png":::
   **<span data-ttu-id="d9592-202">Увеличение линий сетки</span><span class="sxs-lookup"><span data-stu-id="d9592-202">Extend grid lines</span></span>**  
:::image-end:::  

## <span data-ttu-id="d9592-203">Наложения сетки</span><span class="sxs-lookup"><span data-stu-id="d9592-203">Grid overlays</span></span>  

<span data-ttu-id="d9592-204">Раздел ' ' **наложенные сетки** ' ' включает список сеток, присутствующих на странице, каждый с флажком, а также различные параметры.</span><span class="sxs-lookup"><span data-stu-id="d9592-204">The **Grid overlays** section contains a list of grids that are present on the page, each with a checkbox, along with various options.</span></span>  

### <span data-ttu-id="d9592-205">Включение многоналоженных представлений нескольких сеток</span><span class="sxs-lookup"><span data-stu-id="d9592-205">Enable overlay views of multiple grids</span></span>  

<!--todo: @zoher verify and provide updates -->  

<span data-ttu-id="d9592-206">Чтобы отобразить наложение сетки для нескольких сеток, установите флажок рядом с именем сетки.</span><span class="sxs-lookup"><span data-stu-id="d9592-206">To display the overlay grid for multiple grids, choose the checkbox next to each name of the grid.</span></span>  <span data-ttu-id="d9592-207">В примере используются два наложенных перекрытия сетки, каждый из которых представлен различными цветами.</span><span class="sxs-lookup"><span data-stu-id="d9592-207">In the example, there are 2 grid overlays enabled that are each represented with different colors.</span></span>  

*   `main`  
*   `div.snack-box`  
    
:::image type="complex" source="../media/grid-grid-overlays.msft.png" alt-text="Сетка &quot;Поиск&quot;" lightbox="../media/grid-grid-overlays.msft.png":::
   <span data-ttu-id="d9592-209">Включение многоналоженных представлений нескольких сеток</span><span class="sxs-lookup"><span data-stu-id="d9592-209">Enable overlay views of multiple grids</span></span>  
:::image-end:::  

### <span data-ttu-id="d9592-210">Настройка цвета наложения сетки</span><span class="sxs-lookup"><span data-stu-id="d9592-210">Customize the grid overlay color</span></span>  

<span data-ttu-id="d9592-211">Чтобы открыть окно выбора цвета и настроить цвет наложения сетки, установите флажок рядом с именем наложения сетки.</span><span class="sxs-lookup"><span data-stu-id="d9592-211">To open the color picker and customize the grid overlay color, choose the box next to the name of the grid overlay.</span></span>  

:::image type="complex" source="../media/grid-grid-overlays-color.msft.png" alt-text="Сетка &quot;Поиск&quot;" lightbox="../media/grid-grid-overlays-color.msft.png":::
   <span data-ttu-id="d9592-213">Настройка цвета наложения сетки</span><span class="sxs-lookup"><span data-stu-id="d9592-213">Customize the grid overlay color</span></span>  
:::image-end:::  

### <span data-ttu-id="d9592-214">Выделение сетки</span><span class="sxs-lookup"><span data-stu-id="d9592-214">Highlight the grid</span></span>  

<span data-ttu-id="d9592-215">Чтобы выделиь элемент HTML на панели **элементы** и прокрутить его на веб-странице, выберите **элемент Показать на панели элементы** \ ( ![ Показать элемент на значке панели элементов \ ][ImageShowElementInElementsPanelIcon] ).</span><span class="sxs-lookup"><span data-stu-id="d9592-215">To highlight the HTML element in the **Elements** panel and scroll to it on the webpage, choose the **Show element in the Elements panel** \(![Show element in the Elements panel icon][ImageShowElementInElementsPanelIcon]\) icon.</span></span>  

:::image type="complex" source="../media/grid-grid-overlays-highlight.msft.png" alt-text="Сетка &quot;Поиск&quot;" lightbox="../media/grid-grid-overlays-highlight.msft.png":::
   <span data-ttu-id="d9592-217">Выделение сетки</span><span class="sxs-lookup"><span data-stu-id="d9592-217">Highlight the grid</span></span>  
:::image-end:::  

## <span data-ttu-id="d9592-218">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="d9592-218">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageShowElementInElementsPanelIcon]: ../media/show-element-in-element-panel-icon.msft.png  

<!-- links -->  

[DevtoolsGuideChromiumOpen]: ../open.md "Открыть Microsoft Edge DevTools | Документы Microsoft"  

[JecFyiDemoCssGridFruit]: https://jec.fyi/demo/css-grid-fruit "Сетка CSS | JEC к сведению"  
[JecFyiDemoCssGridSnack]: https://jec.fyi/demo/css-grid-snack "Сетка CSS | JEC к сведению"  

[MdnCssGridLayout]: https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout "Макет сетки CSS | MDN"  
[MdnLayoutUsingNamedGridLines]: https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout/Layout_using_Named_Grid_Lines "Макет с помощью именованных линий сетки | MDN"  
[MdnLineBasedPlacementCssGrid]: https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout/Line-based_Placement_with_CSS_Grid "Размещение на основе строк с сеткой CSS | MDN"  

> [!NOTE]
> <span data-ttu-id="d9592-225">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="d9592-225">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="d9592-226">Исходная страница [будет найдена, и](https://developers.google.com/web/tools/chrome-devtools/css/grid) ее можно создать с помощью [Jecelyn Yeen][JecelynYeen] \ (разработчик отвечает, Chrome DevTools \).</span><span class="sxs-lookup"><span data-stu-id="d9592-226">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/css/grid) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="d9592-228">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="d9592-228">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
