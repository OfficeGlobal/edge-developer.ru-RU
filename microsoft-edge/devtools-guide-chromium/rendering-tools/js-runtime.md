---
description: Нахождение ресурсоемких функций с помощью панели DevTools Memory (Microsoft EDGE).
title: Ускорение среды выполнения JavaScript
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 27afe999083470cde0cc0fabf76d0d1ab54e6562
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993585"
---
<!-- Copyright Kayce Basques and Meggin Kearney

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License. -->

# <span data-ttu-id="3d09b-104">Ускорение выполнения JavaScript</span><span class="sxs-lookup"><span data-stu-id="3d09b-104">Speed up JavaScript runtime</span></span>  

<span data-ttu-id="3d09b-105">Нахождение ресурсоемких функций с помощью панели **памяти** .</span><span class="sxs-lookup"><span data-stu-id="3d09b-105">Identify expensive functions using the **Memory** panel.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png" alt-text="Образцы профилей" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png":::
   <span data-ttu-id="3d09b-107">Образцы профилей</span><span class="sxs-lookup"><span data-stu-id="3d09b-107">Sample Profiles</span></span>  
:::image-end:::  

### <span data-ttu-id="3d09b-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="3d09b-108">Summary</span></span>  

*   <span data-ttu-id="3d09b-109">Записывайте именно те функции, которые были вызваны, и объем памяти, необходимый для выделения ресурсов, на панели **памяти** .</span><span class="sxs-lookup"><span data-stu-id="3d09b-109">Record exactly which functions were called and how much memory each requires with Allocation Sampling in the **Memory** panel.</span></span>  
*   <span data-ttu-id="3d09b-110">Визуализируйте свои профили как flameную диаграмму.</span><span class="sxs-lookup"><span data-stu-id="3d09b-110">Visualize your profiles as a flame chart.</span></span>  
    
## <span data-ttu-id="3d09b-111">Запись профиля выборки</span><span class="sxs-lookup"><span data-stu-id="3d09b-111">Record a Sampling Profile</span></span>  

<span data-ttu-id="3d09b-112">Если вы заметили, что Jank в коде JavaScript, соберите профиль выборки.</span><span class="sxs-lookup"><span data-stu-id="3d09b-112">If you notice jank in your JavaScript, collect a Sampling Profile.</span></span>  <span data-ttu-id="3d09b-113">Профили выборки показывают, где на странице потратило время выполнения.</span><span class="sxs-lookup"><span data-stu-id="3d09b-113">Sampling Profiles show where running time is spent on functions in your page.</span></span>  

1.  <span data-ttu-id="3d09b-114">Откройте панель **память** в DevTools.</span><span class="sxs-lookup"><span data-stu-id="3d09b-114">Go to the **Memory** panel of DevTools.</span></span>  
1.  <span data-ttu-id="3d09b-115">Установите переключатель **выборка распределения** .</span><span class="sxs-lookup"><span data-stu-id="3d09b-115">Select the **Allocation sampling** radio button.</span></span>  
1.  <span data-ttu-id="3d09b-116">Нажмите кнопку **Пуск**.</span><span class="sxs-lookup"><span data-stu-id="3d09b-116">Select **Start**.</span></span>  
1.  <span data-ttu-id="3d09b-117">В зависимости от того, что вы пытаетесь проанализировать, вы можете либо повторно загрузить страницу, взаимодействовать со страницей, либо просто разрешить выполнение страницы.</span><span class="sxs-lookup"><span data-stu-id="3d09b-117">Depending on what you are trying to analyze, you may either reload the page, interact with the page, or just let the page run.</span></span>  
1.  <span data-ttu-id="3d09b-118">Когда все будет готово, нажмите кнопку **остановить** .</span><span class="sxs-lookup"><span data-stu-id="3d09b-118">Select the **Stop** button when you are finished.</span></span>  
    
> [!NOTE]
> <span data-ttu-id="3d09b-119">Вы также можете использовать [API консольных утилит][DevtoolsConsoleUtilities] для записи и группировки профилей из командной строки.</span><span class="sxs-lookup"><span data-stu-id="3d09b-119">You may also use the [Console Utilities API][DevtoolsConsoleUtilities] to record and group profiles from the command line.</span></span>  

## <span data-ttu-id="3d09b-120">Просмотр профиля выборки</span><span class="sxs-lookup"><span data-stu-id="3d09b-120">View Sampling Profile</span></span>  

<span data-ttu-id="3d09b-121">Когда вы закончите запись, DevTools автоматически заполнит панель **памяти** в разделе **Профили выборки** с данными из записи.</span><span class="sxs-lookup"><span data-stu-id="3d09b-121">When you finish recording, DevTools automatically populates the **Memory** panel under **SAMPLING PROFILES** with the data from your recording.</span></span>  

<span data-ttu-id="3d09b-122">Представление по умолчанию имеет **большой вид \ (снизу вверх)**.</span><span class="sxs-lookup"><span data-stu-id="3d09b-122">The default view is **Heavy \(Bottom Up\)**.</span></span>  <span data-ttu-id="3d09b-123">Это представление позволяет узнать, какие функции приводили к снижению производительности и как проанализировать пути вызова для этих функций.</span><span class="sxs-lookup"><span data-stu-id="3d09b-123">This view enables you to see which functions had the most impact on performance and examine the calling paths to those functions.</span></span>  

### <span data-ttu-id="3d09b-124">Изменение порядка сортировки</span><span class="sxs-lookup"><span data-stu-id="3d09b-124">Change sort order</span></span>  

<span data-ttu-id="3d09b-125">Чтобы изменить порядок сортировки, щелкните раскрывающееся меню рядом с **выделенной функцией фокуса** , ![ ][ImageFocusIcon] а затем выберите один из указанных ниже вариантов.</span><span class="sxs-lookup"><span data-stu-id="3d09b-125">To change the sorting order, select the dropdown menu next to the **focus selected function** \(![focus selected function][ImageFocusIcon]\) icon and then choose one of the following options.</span></span>

<span data-ttu-id="3d09b-126">**Диаграмма**.</span><span class="sxs-lookup"><span data-stu-id="3d09b-126">**Chart**.</span></span>  <span data-ttu-id="3d09b-127">Диаграмма, на которой показана Хронология записи.</span><span class="sxs-lookup"><span data-stu-id="3d09b-127">Displays a chronological chart of the recording.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png" alt-text="Образцы профилей" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png":::
   <span data-ttu-id="3d09b-129">Flame диаграмма</span><span class="sxs-lookup"><span data-stu-id="3d09b-129">Flame chart</span></span>  
:::image-end:::  

<span data-ttu-id="3d09b-130">**Тяжелая – (снизу вверх)**.</span><span class="sxs-lookup"><span data-stu-id="3d09b-130">**Heavy \(Bottom Up\)**.</span></span>  <span data-ttu-id="3d09b-131">Перечисление функций, влияющих на производительность, и позволяет исследовать пути вызова функций.</span><span class="sxs-lookup"><span data-stu-id="3d09b-131">Lists functions by impact on performance and enables you to examine the calling paths to the functions.</span></span>  <span data-ttu-id="3d09b-132">Это представление по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3d09b-132">This is the default view.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png" alt-text="Образцы профилей" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png":::
   <span data-ttu-id="3d09b-134">Тяжелая диаграмма</span><span class="sxs-lookup"><span data-stu-id="3d09b-134">Heavy chart</span></span>  
:::image-end:::  

<span data-ttu-id="3d09b-135">**Дерево \ (сверху вниз)**.</span><span class="sxs-lookup"><span data-stu-id="3d09b-135">**Tree \(Top Down\)**.</span></span>  <span data-ttu-id="3d09b-136">Показывает общую картину структуры вызова, начиная с верхней части стека вызова.</span><span class="sxs-lookup"><span data-stu-id="3d09b-136">Shows an overall picture of the calling structure, starting at the top of the call stack.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-tree-top-down.msft.png" alt-text="Образцы профилей" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-tree-top-down.msft.png":::
   <span data-ttu-id="3d09b-138">Древовидная диаграмма</span><span class="sxs-lookup"><span data-stu-id="3d09b-138">Tree chart</span></span>  
:::image-end:::  

### <span data-ttu-id="3d09b-139">Исключить функции</span><span class="sxs-lookup"><span data-stu-id="3d09b-139">Exclude functions</span></span>  

<span data-ttu-id="3d09b-140">Чтобы исключить функцию из профиля выборочной выборки, выберите ее и нажмите кнопку **исключить выбранную функцию** \ (исключить выбранную функцию \ ![ ][ImageExcludeIcon] ).</span><span class="sxs-lookup"><span data-stu-id="3d09b-140">To exclude a function from your Sampling Profile, select it and then select the **exclude selected function** \(![exclude selected function][ImageExcludeIcon]\) button.</span></span>  <span data-ttu-id="3d09b-141">Функция запроса \ (родительский элемент) исключенной функции \ (дочерней) оценивается выделенной памятью, назначенной исключенной функции \ (дочерняя).</span><span class="sxs-lookup"><span data-stu-id="3d09b-141">The requesting function \(parent\) of the excluded function \(child\) is charged with the allocated memory assigned to the excluded function \(child\).</span></span>  

<span data-ttu-id="3d09b-142">Нажмите кнопку **восстановить все функции** \ ( ![ восстановить все функции ][ImageRestoreIcon] \), чтобы восстановить все исключенные функции, возвращенные в запись.</span><span class="sxs-lookup"><span data-stu-id="3d09b-142">Select the **restore all functions** \(![restore all functions][ImageRestoreIcon]\) button to restore all excluded functions back into the recording.</span></span>  

## <span data-ttu-id="3d09b-143">Просмотр профиля выборки как диаграммы</span><span class="sxs-lookup"><span data-stu-id="3d09b-143">View Sampling Profile as Chart</span></span>  

<span data-ttu-id="3d09b-144">Представление Диаграмма обеспечивает визуальное представление профиля выборки с течением времени.</span><span class="sxs-lookup"><span data-stu-id="3d09b-144">The Chart view provides a visual representation of the Sampling Profile over time.</span></span>  

<span data-ttu-id="3d09b-145">После [записи профиля выборочной](#record-a-sampling-profile)настройки просмотрите запись в виде Flame диаграммы, [изменив порядок сортировки](#change-sort-order) на **Chart**.</span><span class="sxs-lookup"><span data-stu-id="3d09b-145">After you [record a Sampling Profile](#record-a-sampling-profile), view the recording as a flame chart by [changing the sort order](#change-sort-order) to **Chart**.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png" alt-text="Образцы профилей" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png":::
   <span data-ttu-id="3d09b-147">Flame представления диаграммы</span><span class="sxs-lookup"><span data-stu-id="3d09b-147">Flame chart view</span></span>  
:::image-end:::  

<span data-ttu-id="3d09b-148">Flame диаграмма делится на две части.</span><span class="sxs-lookup"><span data-stu-id="3d09b-148">The flame chart is split into two parts.</span></span>  

| <span data-ttu-id="3d09b-149">индекса</span><span class="sxs-lookup"><span data-stu-id="3d09b-149">index</span></span> | <span data-ttu-id="3d09b-150">Составляющая</span><span class="sxs-lookup"><span data-stu-id="3d09b-150">Part</span></span> | <span data-ttu-id="3d09b-151">Описание</span><span class="sxs-lookup"><span data-stu-id="3d09b-151">Description</span></span> |  
| --- |:--- |:--- |  
| <span data-ttu-id="3d09b-152">1,1</span><span class="sxs-lookup"><span data-stu-id="3d09b-152">1</span></span> | <span data-ttu-id="3d09b-153">Обзор</span><span class="sxs-lookup"><span data-stu-id="3d09b-153">Overview</span></span> | <span data-ttu-id="3d09b-154">Представление всей записи в Birds взгляда.</span><span class="sxs-lookup"><span data-stu-id="3d09b-154">A birds-eye view of the entire recording.</span></span>  <span data-ttu-id="3d09b-155">Высота отрезков соответствует глубине стека вызова.</span><span class="sxs-lookup"><span data-stu-id="3d09b-155">The height of the bars correspond to the depth of the call stack.</span></span>  <span data-ttu-id="3d09b-156">Таким образом, чем выше отрезок, тем глубже стека вызовов.</span><span class="sxs-lookup"><span data-stu-id="3d09b-156">So, the higher the bar, the deeper the call stack.</span></span>  |  
| <span data-ttu-id="3d09b-157">2</span><span class="sxs-lookup"><span data-stu-id="3d09b-157">2</span></span> | <span data-ttu-id="3d09b-158">Стеки вызовов</span><span class="sxs-lookup"><span data-stu-id="3d09b-158">Call Stacks</span></span> | <span data-ttu-id="3d09b-159">Это подробное представление функций, которые были вызваны во время записи.</span><span class="sxs-lookup"><span data-stu-id="3d09b-159">This is an in-depth view of the functions that were called during the recording.</span></span>  <span data-ttu-id="3d09b-160">Горизонтальная ось — это время и вертикальная ось — стек вызовов.</span><span class="sxs-lookup"><span data-stu-id="3d09b-160">The horizontal axis is time and vertical axis is the call stack.</span></span>  <span data-ttu-id="3d09b-161">Стеки организованы сверху вниз.</span><span class="sxs-lookup"><span data-stu-id="3d09b-161">The stacks are organized top-down.</span></span>  <span data-ttu-id="3d09b-162">Таким образом, функция сверху вызывается под ней и т. д.</span><span class="sxs-lookup"><span data-stu-id="3d09b-162">So, the function on top called the one below it, and so on.</span></span>  |  

<span data-ttu-id="3d09b-163">Функции окрашены в случайном порядке.</span><span class="sxs-lookup"><span data-stu-id="3d09b-163">Functions are colored randomly.</span></span>  <span data-ttu-id="3d09b-164">Нет связи с цветами, используемыми в других панелях.</span><span class="sxs-lookup"><span data-stu-id="3d09b-164">There is no correlation to the colors used in the other panels.</span></span>  <span data-ttu-id="3d09b-165">Однако функции всегда выделяются одинаково во всех вызовах, чтобы можно было видеть закономерности в каждой среде выполнения.</span><span class="sxs-lookup"><span data-stu-id="3d09b-165">However, functions are always colored the same across invocations so that you are able to see patterns in each runtime.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-highlighted.msft.png" alt-text="Образцы профилей" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-highlighted.msft.png":::
   <span data-ttu-id="3d09b-167">Диаграмма с аннотированными Flame</span><span class="sxs-lookup"><span data-stu-id="3d09b-167">Annotated flame chart</span></span>  
:::image-end:::  

<span data-ttu-id="3d09b-168">Высокий стек вызовов не обязательно важен, это означает, что было вызвано много функций.</span><span class="sxs-lookup"><span data-stu-id="3d09b-168">A tall call stack is not necessarily significant, it just means that a lot of functions were called.</span></span>  <span data-ttu-id="3d09b-169">Но широкий отрезок означает, что выполнение функции заняло много времени.</span><span class="sxs-lookup"><span data-stu-id="3d09b-169">But a wide bar means that a function took a long time to complete.</span></span>  <span data-ttu-id="3d09b-170">Они являются кандидатами для оптимизации.</span><span class="sxs-lookup"><span data-stu-id="3d09b-170">These are candidates for optimization.</span></span>  

### <span data-ttu-id="3d09b-171">Масштабирование отдельных частей записи</span><span class="sxs-lookup"><span data-stu-id="3d09b-171">Zoom in on specific parts of recording</span></span>  

<span data-ttu-id="3d09b-172">Выберите, удерживайте и перетащите указатель мыши по левому краю обзора и проведите по экрану, чтобы увеличить масштаб отдельных частей стека вызова.</span><span class="sxs-lookup"><span data-stu-id="3d09b-172">Select, hold, and drag your mouse left and right across the overview to zoom in on particular parts of the call stack.</span></span>  <span data-ttu-id="3d09b-173">После масштабирования стек вызовов автоматически отображает выбранную часть записи.</span><span class="sxs-lookup"><span data-stu-id="3d09b-173">After you zoom, the call stack automatically displays the portion of the recording that you selected.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-zoomed.msft.png" alt-text="Образцы профилей" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-zoomed.msft.png":::
   <span data-ttu-id="3d09b-175">Диаграмма с увеличенным масштабом</span><span class="sxs-lookup"><span data-stu-id="3d09b-175">Chart zoomed</span></span>  
:::image-end:::  

### <span data-ttu-id="3d09b-176">Просмотр сведений о функции</span><span class="sxs-lookup"><span data-stu-id="3d09b-176">View function details</span></span>  

<span data-ttu-id="3d09b-177">Выберите функцию, чтобы просмотреть ее определение на панели « **источники** ».</span><span class="sxs-lookup"><span data-stu-id="3d09b-177">Select on a function to view the definition in the **Sources** panel.</span></span>  

<span data-ttu-id="3d09b-178">Наведите указатель мыши на функцию, чтобы отобразить имя и данные о времени.</span><span class="sxs-lookup"><span data-stu-id="3d09b-178">Hover over a function to display the name and timing data.</span></span>  <span data-ttu-id="3d09b-179">Ниже приведены сведения.</span><span class="sxs-lookup"><span data-stu-id="3d09b-179">The following information is provided.</span></span>  

| <span data-ttu-id="3d09b-180">Подробнее</span><span class="sxs-lookup"><span data-stu-id="3d09b-180">Detail</span></span> | <span data-ttu-id="3d09b-181">Описание</span><span class="sxs-lookup"><span data-stu-id="3d09b-181">Description</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="3d09b-182">Name</span><span class="sxs-lookup"><span data-stu-id="3d09b-182">Name</span></span>** | <span data-ttu-id="3d09b-183">Имя функции.</span><span class="sxs-lookup"><span data-stu-id="3d09b-183">The name of the function.</span></span>  |  
| **<span data-ttu-id="3d09b-184">Сам размер</span><span class="sxs-lookup"><span data-stu-id="3d09b-184">Self size</span></span>** | <span data-ttu-id="3d09b-185">Размер текущего вызова функции, включая только инструкции в функции.</span><span class="sxs-lookup"><span data-stu-id="3d09b-185">The size of the current invocation of the function, including only the statements in the function.</span></span>  |  
| **<span data-ttu-id="3d09b-186">Общий размер</span><span class="sxs-lookup"><span data-stu-id="3d09b-186">Total size</span></span>** | <span data-ttu-id="3d09b-187">Размер текущего вызова функции и всех ее вызываемых функций.</span><span class="sxs-lookup"><span data-stu-id="3d09b-187">The size of the current invocation of this function and any functions that it called.</span></span>  |  
| **<span data-ttu-id="3d09b-188">URL-адрес</span><span class="sxs-lookup"><span data-stu-id="3d09b-188">URL</span></span>** | <span data-ttu-id="3d09b-189">Расположение определения функции в форме `base.js:261` Where `base.js` — имя файла, в котором определена функция, и `261` является номером строки определения.</span><span class="sxs-lookup"><span data-stu-id="3d09b-189">The location of the function definition in the form of `base.js:261` where `base.js` is the name of the file where the function is defined and `261` is the line number of the definition.</span></span>  |  
<!--*   **Aggregated self time**.  Aggregate time for all invocations of the function across the recording, not including functions called by this function.  -->  
<!--*   **Aggregated total time**.  Aggregate total time for all invocations of the function, including functions called by this function.  -->  
<!--*   **Not optimized**.  If the profiler has detected a potential optimization for the function it lists it here.  -->  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-hover.msft.png" alt-text="Образцы профилей" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-hover.msft.png":::
   <span data-ttu-id="3d09b-191">Просмотр сведений о функциях на диаграмме</span><span class="sxs-lookup"><span data-stu-id="3d09b-191">View functions details in chart</span></span>  
:::image-end:::  

## <span data-ttu-id="3d09b-192">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="3d09b-192">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageExcludeIcon]: ../media/exclude-icon.msft.png  
[ImageFocusIcon]: ../media/focus-icon.msft.png  
[ImageRestoreIcon]: ../media/restore-icon.msft.png  

<!-- links -->  

[DevtoolsConsoleUtilities]: ../console/utilities.md "Справочник по API служебных программ для консоли | Документы Microsoft"  
[DevtoolsConsoleUtilitiesProfile]: ../console/utilities.md#profile "Profile — Справочник по API для служебных программ консоли | Документы Microsoft"  
[DevtoolsConsoleUtilitiesProfileEnd]: ../console/utilities.md#profileend "Справочник по API для служебных программ на консоли profileEnd | Документы Microsoft"  

> [!NOTE]
> <span data-ttu-id="3d09b-196">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="3d09b-196">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="3d09b-197">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/js-execution) и [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \) и [Meggin Kearney][MegginKearney] \ (технический редактор \).</span><span class="sxs-lookup"><span data-stu-id="3d09b-197">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/js-execution) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) and [Meggin Kearney][MegginKearney] \(Tech Writer\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="3d09b-199">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="3d09b-199">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
