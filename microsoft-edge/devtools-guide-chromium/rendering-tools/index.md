---
description: Пользователи ожидают интерактивные и плавные страницы.  Каждый этап конвейера на пиксельах представляет возможность введения Jank.  Узнайте о средствах и стратегиях, позволяющих выявить и устранить распространенные проблемы, которые замедляют производительность во время выполнения.
title: Анализ производительности среды выполнения
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: f7ca848712268110700fac2c5fb75fe1751812bf
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/02/2020
ms.locfileid: "10992709"
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
   limitations under the License.  -->

# <span data-ttu-id="ba337-106">Анализ производительности среды выполнения</span><span class="sxs-lookup"><span data-stu-id="ba337-106">Analyze runtime performance</span></span> 

<span data-ttu-id="ba337-107">Пользователи ожидают интерактивные и плавные страницы.</span><span class="sxs-lookup"><span data-stu-id="ba337-107">Users expects interactive and smooth pages.</span></span>  <span data-ttu-id="ba337-108">Каждый этап конвейера на пиксельах представляет возможность введения Jank.</span><span class="sxs-lookup"><span data-stu-id="ba337-108">Each stage in the pixel pipeline represents an opportunity to introduce jank.</span></span>  <span data-ttu-id="ba337-109">Узнайте о средствах и стратегиях, позволяющих выявить и устранить распространенные проблемы, которые замедляют производительность во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="ba337-109">Learn about tools and strategies to identify and fix common problems that slow down runtime performance.</span></span>  

### <span data-ttu-id="ba337-110">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="ba337-110">Summary</span></span>  

*   <span data-ttu-id="ba337-111">Не записывайте JavaScript, который заставляет браузер обновить макет.</span><span class="sxs-lookup"><span data-stu-id="ba337-111">Do not write JavaScript that forces the browser to recalculate layout.</span></span>  <span data-ttu-id="ba337-112">Разделяйте функции чтения и записи, а затем выполняйте операции чтения первыми.</span><span class="sxs-lookup"><span data-stu-id="ba337-112">Separate read and write functions, and perform reads first.</span></span>  
*   <span data-ttu-id="ba337-113">Не переусложняйте CSS.</span><span class="sxs-lookup"><span data-stu-id="ba337-113">Do not over-complicate your CSS.</span></span>  <span data-ttu-id="ba337-114">Используйте меньший CSS, чтобы сделать селекторы CSS простыми.</span><span class="sxs-lookup"><span data-stu-id="ba337-114">Use less CSS and keep your CSS selectors simple.</span></span>  
*   <span data-ttu-id="ba337-115">Старайтесь не использовать разметку максимально возможной.</span><span class="sxs-lookup"><span data-stu-id="ba337-115">Avoid layout as much as possible.</span></span>  <span data-ttu-id="ba337-116">Выберите CSS, для которого не запущен макет.</span><span class="sxs-lookup"><span data-stu-id="ba337-116">Choose CSS that does not trigger layout at all.</span></span>  
*   <span data-ttu-id="ba337-117">Рисование может занимать больше времени, чем любые другие действия рендеринга.</span><span class="sxs-lookup"><span data-stu-id="ba337-117">Painting may take up more time than any other rendering activity.</span></span>  <span data-ttu-id="ba337-118">Посмотрите, как узкие места закрашивания закраски.</span><span class="sxs-lookup"><span data-stu-id="ba337-118">Watch out for paint bottlenecks.</span></span>  
    
## <span data-ttu-id="ba337-119">JavaScript</span><span class="sxs-lookup"><span data-stu-id="ba337-119">JavaScript</span></span>  

<span data-ttu-id="ba337-120">Вычисления JavaScript, особенно те, которые вызывают сложные визуальные изменения, могут привести к снижению производительности приложения.</span><span class="sxs-lookup"><span data-stu-id="ba337-120">JavaScript calculations, especially ones that trigger extensive visual changes, may stall application performance.</span></span>  <span data-ttu-id="ba337-121">Не разрешать неправильное или долгое выполнение JavaScript, мешая взаимодействию с пользователем.</span><span class="sxs-lookup"><span data-stu-id="ba337-121">Do not let badly-timed or long-running JavaScript interfere with user interactions.</span></span>  

### <span data-ttu-id="ba337-122">JavaScript: инструменты</span><span class="sxs-lookup"><span data-stu-id="ba337-122">JavaScript: Tools</span></span>  

<span data-ttu-id="ba337-123">Сделайте запись на панели " **производительность** " и найдите подозрительные `Evaluate Script` события.</span><span class="sxs-lookup"><span data-stu-id="ba337-123">Take a recording in the **Performance** panel and look for suspiciously long `Evaluate Script` events.</span></span>  <!--If you find any, you are able to enable the **JS Profiler** and re-do your recording to get more detailed information about exactly which JavaScript functions were used and how long each took.  -->  

<!--todo: add Recording section when available  -->  
<!--todo: add Profile JavaScript (JS Profiler) section when available  -->  

<span data-ttu-id="ba337-124">е, что вы проjankе в JavaScript, вам может потребоваться выполнить анализ следующего уровня и собрать профиль ЦП JavaScript.</span><span class="sxs-lookup"><span data-stu-id="ba337-124">f you noticing quite a bit of jank in your JavaScript, you may need to take your analysis to the next level and collect a JavaScript CPU profile.</span></span>  <span data-ttu-id="ba337-125">В профилях ЦП показано, где в функциях страницы потратила среда выполнения.</span><span class="sxs-lookup"><span data-stu-id="ba337-125">CPU profiles show where runtime is spent within the functions of your page.</span></span>  <span data-ttu-id="ba337-126">В этой статье объясняется, как создавать профили ЦП с использованием [ускорения выполнения JavaScript][DevtoolsRenderingToolsJavascriptRuntime].</span><span class="sxs-lookup"><span data-stu-id="ba337-126">Learn how to create CPU profiles in [Speed Up JavaScript Runtime][DevtoolsRenderingToolsJavascriptRuntime].</span></span>

### <span data-ttu-id="ba337-127">JavaScript: проблемы</span><span class="sxs-lookup"><span data-stu-id="ba337-127">JavaScript: Problems</span></span>  

<span data-ttu-id="ba337-128">В приведенной ниже таблице описаны некоторые распространенные проблемы JavaScript и возможные решения.</span><span class="sxs-lookup"><span data-stu-id="ba337-128">The following table describes some common JavaScript problems and potential solutions:</span></span>  

| <span data-ttu-id="ba337-129">Проблема</span><span class="sxs-lookup"><span data-stu-id="ba337-129">Problem</span></span> | <span data-ttu-id="ba337-130">Пример.</span><span class="sxs-lookup"><span data-stu-id="ba337-130">Example</span></span> | <span data-ttu-id="ba337-131">Решение</span><span class="sxs-lookup"><span data-stu-id="ba337-131">Solution</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="ba337-132">Ресурсоемкие обработчики входных данных, влияющие на отклик или анимацию.</span><span class="sxs-lookup"><span data-stu-id="ba337-132">Expensive input handlers affecting response or animation.</span></span>  | <span data-ttu-id="ba337-133">Сенсор, параллакс прокрутку.</span><span class="sxs-lookup"><span data-stu-id="ba337-133">Touch, parallax scrolling.</span></span>  | <span data-ttu-id="ba337-134">Разрешите браузеру управлять сенсорными и прокруткой или привяжите прослушиватель как можно позже.</span><span class="sxs-lookup"><span data-stu-id="ba337-134">Let the browser handle touch and scrolls, or bind the listener as late as possible.</span></span>  <span data-ttu-id="ba337-135">Просмотр [ресурсоемких обработчиков ввода в контрольном списке производительности в пол Lewis and "][WebPerformanceCalendarRuntimeChecklist].</span><span class="sxs-lookup"><span data-stu-id="ba337-135">See [Expensive Input Handlers in Paul Lewis' runtime performance checklist][WebPerformanceCalendarRuntimeChecklist].</span></span>  |  
| <span data-ttu-id="ba337-136">Некорректное применение JavaScript, которое влияет на отклик, анимацию, загрузку.</span><span class="sxs-lookup"><span data-stu-id="ba337-136">Badly-timed JavaScript affecting response, animation, load.</span></span>  | <span data-ttu-id="ba337-137">Пользователь выполняет прокрутку сразу после загрузки страницы, setTimeout/setInterval.</span><span class="sxs-lookup"><span data-stu-id="ba337-137">User scrolls right after page load, setTimeout / setInterval.</span></span>  | <span data-ttu-id="ba337-138">Оптимизация среды выполнения JavaScript: использование `requestAnimationFrame` , распространение управления DOM на кадры и использование [веб-рабочих процессов][MDNUsingWebWorkers].</span><span class="sxs-lookup"><span data-stu-id="ba337-138">Optimize JavaScript runtime: use `requestAnimationFrame`, spread DOM manipulation over frames, use [Web Workers][MDNUsingWebWorkers].</span></span>  |  
| <span data-ttu-id="ba337-139">Длительное выполнение ответа на JavaScript.</span><span class="sxs-lookup"><span data-stu-id="ba337-139">Long-running JavaScript affecting response.</span></span>  | <span data-ttu-id="ba337-140">[Событие DOMContentLoaded][MDNUsingWebWorkers] останавливается, так как оно вашего удобства с помощью JS.</span><span class="sxs-lookup"><span data-stu-id="ba337-140">The [DOMContentLoaded event][MDNUsingWebWorkers] stalls as it is swamped with JS work.</span></span>  | <span data-ttu-id="ba337-141">Перевод чистых вычислительных трудозатрат на [веб-рабочие процессы][MDNUsingWebWorkers].</span><span class="sxs-lookup"><span data-stu-id="ba337-141">Move pure computational work to [Web Workers][MDNUsingWebWorkers].</span></span>  <span data-ttu-id="ba337-142">Если вам нужен доступ DOM, используйте `requestAnimationFrame` .</span><span class="sxs-lookup"><span data-stu-id="ba337-142">If you need DOM access, use `requestAnimationFrame`.</span></span>  <!--See also [Optimize JavaScript Execution][WebFundamentalsPerformanceRenderingOptimizeJavascriptRuntime].  -->  |  
| <span data-ttu-id="ba337-143">Сценарии сборки мусора, влияющие на ответ или анимацию.</span><span class="sxs-lookup"><span data-stu-id="ba337-143">Garbage-y scripts affecting response or animation.</span></span>  | <span data-ttu-id="ba337-144">Сбор мусора может происходить везде, где бы вы ни находились</span><span class="sxs-lookup"><span data-stu-id="ba337-144">Garbage collection may happen anywhere.</span></span>  | <span data-ttu-id="ba337-145">Создавать менее сценарии сборки мусора.</span><span class="sxs-lookup"><span data-stu-id="ba337-145">Write less garbage-y scripts.</span></span>  <span data-ttu-id="ba337-146">Ознакомьтесь со [сборкой мусора в анимации в контрольном списке производительности в пол Lewis and "][WebPerformanceCalendarRuntimeChecklist].</span><span class="sxs-lookup"><span data-stu-id="ba337-146">See [Garbage Collection in Animation in Paul Lewis' runtime performance checklist][WebPerformanceCalendarRuntimeChecklist].</span></span>  |  

<!--todo: add Optimize JavaScript runtime section when available  -->  

## <span data-ttu-id="ba337-147">Стиль</span><span class="sxs-lookup"><span data-stu-id="ba337-147">Style</span></span>  

<span data-ttu-id="ba337-148">Изменение стиля — это дорогостоящие особенности, особенно если эти изменения влияют на более чем один элемент в DOM.</span><span class="sxs-lookup"><span data-stu-id="ba337-148">Style changes are costly, especially if those changes affect more than one element in the DOM.</span></span>  <span data-ttu-id="ba337-149">Каждый раз, когда к элементу применяются стили, браузер отражает влияние на все связанные элементы, пересчитывать макет и перекрашивать.</span><span class="sxs-lookup"><span data-stu-id="ba337-149">Any time you apply styles to an element, the browser figures out the impact on all related elements, recalculates the layout, and repaints.</span></span>  

<!--Related Guides:  

*   [Reduce the Scope and Complexity of Styles Calculations][WebFundamentalsPerformanceRenderingReduceScope]  
-->  

<!--todo: add Reduce the Scope and Complexity of Styles Calculations section when available -->  

### <span data-ttu-id="ba337-150">Стиль: инструменты</span><span class="sxs-lookup"><span data-stu-id="ba337-150">Style: Tools</span></span>  

<span data-ttu-id="ba337-151">Сделайте запись на панели " **производительность** ".</span><span class="sxs-lookup"><span data-stu-id="ba337-151">Take a recording in the **Performance** panel.</span></span>  <span data-ttu-id="ba337-152">Проверка записи для больших `Recalculate Style` событий (отображается фиолетовым).</span><span class="sxs-lookup"><span data-stu-id="ba337-152">Check the recording for large `Recalculate Style` events \(displayed in purple\).</span></span>  

<!--todo: add Recording section when available  -->  

<span data-ttu-id="ba337-153">Щелкните событие, `Recalculate Style` чтобы просмотреть дополнительные сведения о нем в области **сведений** .</span><span class="sxs-lookup"><span data-stu-id="ba337-153">Click on a `Recalculate Style` event to view more information about it in the **Details** pane.</span></span>  <span data-ttu-id="ba337-154">Если изменение стиля занимает много времени, это снижение производительности.</span><span class="sxs-lookup"><span data-stu-id="ba337-154">If the style changes are taking a long time, that is a performance hit.</span></span>  <span data-ttu-id="ba337-155">Если вычисления стиля влияют на большое количество элементов, это еще одна область с комнатой для улучшения.</span><span class="sxs-lookup"><span data-stu-id="ba337-155">If the style calculations are affecting a large number of elements, that is another area with room for improvement.</span></span>  

:::image type="complex" source="../media/rendering-tools-performance-recalculate-style-summary.msft.png" alt-text="Длинный стиль пересчета" lightbox="../media/rendering-tools-performance-recalculate-style-summary.msft.png":::
   <span data-ttu-id="ba337-157">Длинный стиль пересчета</span><span class="sxs-lookup"><span data-stu-id="ba337-157">Long recalculate style</span></span>  
:::image-end:::  

<span data-ttu-id="ba337-158">Чтобы уменьшить влияние событий, `Recalculate Style` сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="ba337-158">To reduce the impact of `Recalculate Style` events:</span></span>  

*   <span data-ttu-id="ba337-159">Используйте [триггеры CSS][CssTriggers] , чтобы выяснить, какие свойства CSS активируют макет, Paint и Composite.</span><span class="sxs-lookup"><span data-stu-id="ba337-159">Use the [CSS Triggers][CssTriggers] to learn which CSS properties trigger layout, paint, and composite.</span></span>  <span data-ttu-id="ba337-160">Эти свойства имеют наихудшее влияние на производительность отрисовки.</span><span class="sxs-lookup"><span data-stu-id="ba337-160">These properties have the worst impact on rendering performance.</span></span>  
*   <span data-ttu-id="ba337-161">Переключиться на свойства с меньшим влиянием.</span><span class="sxs-lookup"><span data-stu-id="ba337-161">Switch to properties that have less impact.</span></span>  <!--See [Stick to compositor-only properties and manage layer count][WebFundamentalsPerformanceRenderingCompositorOnlyProperties] for more guidance.  -->  
    
<!--todo: add Stick to compositor-only properties and manage layer count section when available -->  

### <span data-ttu-id="ba337-162">Стиль: проблемы</span><span class="sxs-lookup"><span data-stu-id="ba337-162">Style: Problems</span></span>  

<span data-ttu-id="ba337-163">В таблице ниже описаны некоторые распространенные проблемы стиля и возможные решения.</span><span class="sxs-lookup"><span data-stu-id="ba337-163">The following table describes some common style problems and potential solutions:</span></span>  

| <span data-ttu-id="ba337-164">Проблема</span><span class="sxs-lookup"><span data-stu-id="ba337-164">Problem</span></span> | <span data-ttu-id="ba337-165">Пример.</span><span class="sxs-lookup"><span data-stu-id="ba337-165">Example</span></span> | <span data-ttu-id="ba337-166">Решение</span><span class="sxs-lookup"><span data-stu-id="ba337-166">Solution</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="ba337-167">Дорогостоящие расчеты стиля, влияющие на отклик или анимацию.</span><span class="sxs-lookup"><span data-stu-id="ba337-167">Expensive style calculations affecting response or animation.</span></span>  | <span data-ttu-id="ba337-168">Любое свойство CSS, которое изменяет геометрию элемента, например ширину, высоту или расположение; Браузер проверяет все другие элементы и пересчитывает макет.</span><span class="sxs-lookup"><span data-stu-id="ba337-168">Any CSS property that changes the geometry of an element, like the width, height, or position; the browser checks all other elements and recalculates the layout.</span></span>  | <span data-ttu-id="ba337-169">Старайтесь не использовать CSS, которые инициируют макеты</span><span class="sxs-lookup"><span data-stu-id="ba337-169">Avoid CSS that triggers layouts</span></span> |  
| <span data-ttu-id="ba337-170">Сложные селекторы, влияющие на отклик или анимацию.</span><span class="sxs-lookup"><span data-stu-id="ba337-170">Complex selectors affecting response or animation.</span></span>  | <span data-ttu-id="ba337-171">Вложенные элементы выбора заставляют браузер знать все о всех остальных элементах, включая родительские и дочерние элементы.</span><span class="sxs-lookup"><span data-stu-id="ba337-171">Nested selectors force the browser to know everything about all the other elements, including parents and children.</span></span>  | <span data-ttu-id="ba337-172">Сослаться на элемент в таблице CSS только с помощью класса.</span><span class="sxs-lookup"><span data-stu-id="ba337-172">Reference an element in your CSS with just a class.</span></span>  |  

<!--todo: add Avoid CSS that triggers layouts section when available -->  
<!--todo: add Reduce the Scope and Complexity of Styles Calculations (Reference an element in your CSS with just a class) section when available -->  

<!--Related Guides:  

*   [Reduce the Scope and Complexity of Styles Calculations][WebFundamentalsPerformanceRenderingReduceScope]  -->  

<!--todo: add Reduce the Scope and Complexity of Styles Calculations section when available -->  

## <span data-ttu-id="ba337-173">Макет</span><span class="sxs-lookup"><span data-stu-id="ba337-173">Layout</span></span>  

<span data-ttu-id="ba337-174">Макет (или перекомпоновка в Firefox) — это процесс, с помощью которого браузер вычисляет позиции и размеры всех элементов на странице.</span><span class="sxs-lookup"><span data-stu-id="ba337-174">Layout (or reflow in Firefox) is the process by which the browser calculates the positions and sizes of all the elements on a page.</span></span>  <span data-ttu-id="ba337-175">Модель макета веба означает, что один элемент может повлиять на других пользователей; Например, ширина `<body>` элемента обычно влияет на ширину дочерних элементов и т. д., так же, как и вниз по дереву.</span><span class="sxs-lookup"><span data-stu-id="ba337-175">The layout model of the web means that one element may affect others; for example, the width of the `<body>` element typically affects the widths of any child elements, and so on, all the way up and down the tree.</span></span>  <span data-ttu-id="ba337-176">Процесс может быть довольно вовлеченным в браузер.</span><span class="sxs-lookup"><span data-stu-id="ba337-176">The process may be quite involved for the browser.</span></span>  

<span data-ttu-id="ba337-177">Как правило, если вы запрашиваете значение геометрического значения из DOM перед завершением кадра, вы собираетесь найти себя с помощью принудительно синхронных макетов, что может привести к значительному снижению производительности, если часто приходится создавать большое дерево DOM.</span><span class="sxs-lookup"><span data-stu-id="ba337-177">As a general rule of thumb, if you ask for a geometric value back from the DOM before a frame is complete, you are going to find yourself with "forced synchronous layouts", which may be a big performance bottleneck if repeated frequently or performed for a large DOM tree.</span></span>  

<!--Related Guides:  

*   [Avoid Layout Thrashing][WebFundamentalsPerformanceRenderingAvoidLargeComplexLayouts]  
*   [Diagnose Forced Synchronous Layouts][DevtoolsRenderingToolsForcedSynchronousLayouts]  -->  

<!--todo: add Avoid CSS that triggers layouts (Avoid Layout Thrashing) section when available -->  
<!--todo: add Diagnose Forced Synchronous Layouts section when available  -->  

### <span data-ttu-id="ba337-178">Макет: инструменты</span><span class="sxs-lookup"><span data-stu-id="ba337-178">Layout: Tools</span></span>  

<span data-ttu-id="ba337-179">Область **производительности** определяет, когда страница вызывает принудительно синхронные макеты.</span><span class="sxs-lookup"><span data-stu-id="ba337-179">The **Performance** pane identifies when a page causes forced synchronous layouts.</span></span>  <span data-ttu-id="ba337-180">Эти `Layout` события помечены красными отрезками.</span><span class="sxs-lookup"><span data-stu-id="ba337-180">These `Layout` events are marked with red bars.</span></span>  

:::image type="complex" source="../media/rendering-tools-jank-performance-recalculate-style-summary.msft.png" alt-text="Длинный стиль пересчета" lightbox="../media/rendering-tools-jank-performance-recalculate-style-summary.msft.png":::
   <span data-ttu-id="ba337-182">Принудительно синхронный макет</span><span class="sxs-lookup"><span data-stu-id="ba337-182">Forced synchronous layout</span></span>  
:::image-end:::  

<span data-ttu-id="ba337-183">"Макет Thrashing" — это повторение принудительно синхронно заданных условий макета.</span><span class="sxs-lookup"><span data-stu-id="ba337-183">"Layout thrashing" is a repetition of forced synchronous layout conditions.</span></span>  <span data-ttu-id="ba337-184">Это происходит, когда JavaScript пишет и считывает из DOM многократно, что приводит к пересчету макета в браузере.</span><span class="sxs-lookup"><span data-stu-id="ba337-184">This occurs when JavaScript writes and reads from the DOM repeatedly, which forces the browser to recalculate the layout over and over.</span></span>  <span data-ttu-id="ba337-185">Чтобы определить макет Thrashing, найдите шаблон с несколькими принудительно синхронными предупреждениями макета.</span><span class="sxs-lookup"><span data-stu-id="ba337-185">To identify layout thrashing, look for a pattern of multiple forced synchronous layout warnings.</span></span>  <span data-ttu-id="ba337-186">Просмотреть предыдущий рисунок.</span><span class="sxs-lookup"><span data-stu-id="ba337-186">See the previous figure.</span></span>  

### <span data-ttu-id="ba337-187">Макет: проблемы</span><span class="sxs-lookup"><span data-stu-id="ba337-187">Layout: Problems</span></span>  

<span data-ttu-id="ba337-188">В таблице ниже описаны некоторые типичные проблемы с макетами и возможные решения.</span><span class="sxs-lookup"><span data-stu-id="ba337-188">The following table describes some common layout problems and potential solutions:</span></span>  

| <span data-ttu-id="ba337-189">Проблема</span><span class="sxs-lookup"><span data-stu-id="ba337-189">Problem</span></span> | <span data-ttu-id="ba337-190">Пример.</span><span class="sxs-lookup"><span data-stu-id="ba337-190">Example</span></span> | <span data-ttu-id="ba337-191">Решение</span><span class="sxs-lookup"><span data-stu-id="ba337-191">Solution</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="ba337-192">Принудительно синхронный макет, влияющий на ответ или анимацию.</span><span class="sxs-lookup"><span data-stu-id="ba337-192">Forced synchronous layout affecting response or animation.</span></span>  | <span data-ttu-id="ba337-193">Принудительное выполнение браузером более ранней версии в конвейере пикселей, что приводит к повторяющимся действиям в процессе отрисовки.</span><span class="sxs-lookup"><span data-stu-id="ba337-193">Forcing the browser to perform layout earlier in the pixel pipeline, resulting in repeating steps in the rendering process.</span></span>  | <span data-ttu-id="ba337-194">Предварительно заполните свой стиль, а затем выполните все операции записи.</span><span class="sxs-lookup"><span data-stu-id="ba337-194">Batch your style reads first, then do any writes.</span></span>  <!--See also [Avoid large, complex layouts and layout thrashing][WebFundamentalsPerformanceRenderingAvoidLargeComplexLayouts].  -->  |  
| <span data-ttu-id="ba337-195">Макет Thrashing влияет на отклик или анимацию.</span><span class="sxs-lookup"><span data-stu-id="ba337-195">Layout thrashing affecting response or animation.</span></span>  | <span data-ttu-id="ba337-196">Цикл, покрывающий браузер, в цикле чтения и записи-чтения, который принудительно пересчитывает макет, переключаясь в браузер.</span><span class="sxs-lookup"><span data-stu-id="ba337-196">A loop that puts the browser into a read-write-read-write cycle, forcing the browser to recalculate layout over and over again.</span></span>  | <span data-ttu-id="ba337-197">Автоматическая обработка пакетных операций чтения и записи с помощью [библиотеки FastDom][GitHubWilsonpageFastdom].</span><span class="sxs-lookup"><span data-stu-id="ba337-197">Automatically batch read-write operations using [FastDom library][GitHubWilsonpageFastdom].</span></span>  |  

<!--todo: add Avoid CSS that triggers layouts (Avoid large, complex layouts and layout thrashing) section when available -->  

## <span data-ttu-id="ba337-198">Рисование и совмещение цветов</span><span class="sxs-lookup"><span data-stu-id="ba337-198">Paint and composite</span></span>  

<span data-ttu-id="ba337-199">Заливка — это процесс заполнения пикселов.</span><span class="sxs-lookup"><span data-stu-id="ba337-199">Paint is the process of filling in pixels.</span></span>  <span data-ttu-id="ba337-200">Это часто является наиболее дорогостоящей частью процесса отрисовки.</span><span class="sxs-lookup"><span data-stu-id="ba337-200">It is often the most costly part of the rendering process.</span></span>  <span data-ttu-id="ba337-201">Если вы заметили, что ваша страница janky, возможно, у вас возникли проблемы с окрашиванием.</span><span class="sxs-lookup"><span data-stu-id="ba337-201">If you noticed that your page is janky in any way, it is likely that you have paint problems.</span></span>  

<span data-ttu-id="ba337-202">Композиция — это область, в которой окрашенные части страницы размещаются вместе для отображения на экране.</span><span class="sxs-lookup"><span data-stu-id="ba337-202">Compositing is where the painted parts of the page are put together for displaying on screen.</span></span>  <span data-ttu-id="ba337-203">В большинстве случаев, если вы перейдете на свойства, предназначенные только для компоновщика, и не можете вообще обрисовываться, вы увидите значительную улучшенность в производительности, но вам нужно пронаблюдать за избыточными счетчиками слоев.</span><span class="sxs-lookup"><span data-stu-id="ba337-203">For the most part, if you stick to compositor-only properties and avoid paint altogether, you should see a major improvement in performance, but you need to watch out for excessive layer counts.</span></span>  <!--See also [Stick to compositor-only properties and manage layer count][WebFundamentalsPerformanceRenderingCompositorOnlyProperties].  -->  

<!--todo: add Stick to compositor-only properties and manage layer count section when available  -->  

### <span data-ttu-id="ba337-204">Рисование и совмещение: инструменты</span><span class="sxs-lookup"><span data-stu-id="ba337-204">Paint and composite: Tools</span></span>  

<span data-ttu-id="ba337-205">Хотите узнать, как долго рисуются и как часто происходит рисование?</span><span class="sxs-lookup"><span data-stu-id="ba337-205">Want to know how long painting takes or how often painting occurs?</span></span>  <span data-ttu-id="ba337-206">Установите флажок [включить дополнительные возможности инструментирования Paint][DevtoolsChromiumEvaluatePerformanceReferenceEnableadvancedpaintinstrumentation] на панели **производительности** и сделайте запись.</span><span class="sxs-lookup"><span data-stu-id="ba337-206">Check the [Enable advanced paint instrumentation][DevtoolsChromiumEvaluatePerformanceReferenceEnableadvancedpaintinstrumentation] setting in the **Performance** panel and then take a recording.</span></span>  <span data-ttu-id="ba337-207">Если большая часть времени отрисовки потратила на рисование, у вас возникли проблемы с рисованием.</span><span class="sxs-lookup"><span data-stu-id="ba337-207">If most of your rendering time is spent painting, you have paint problems.</span></span>  

<!--
:::image type="complex" source="../media/rendering-tools-jank-performance-advanced-paint-instrumentation-summary.msft.png" alt-text="Длинный стиль пересчета" lightbox="../media/rendering-tools-jank-performance-advanced-paint-instrumentation-summary.msft.png":::
   Long paint times in timeline recording  
:::image-end:::  
-->  

<!--
Check out the **Rendering** panel for further configurations that are able to help you diagnose paint problems.  -->  

<!--todo: link Rendering panel in ../evaluate-performance/timeline-tool  sub-section when live  -->  

### <span data-ttu-id="ba337-208">Раскрашивание и совмещение: проблемы</span><span class="sxs-lookup"><span data-stu-id="ba337-208">Paint and composite: Problems</span></span>  

<span data-ttu-id="ba337-209">В таблице ниже описаны некоторые распространенные проблемы, возникающие при работе с закрасками и комплексными решениями.</span><span class="sxs-lookup"><span data-stu-id="ba337-209">The following table describes some common paint and composite problems and potential solutions:</span></span>  

| <span data-ttu-id="ba337-210">Проблема</span><span class="sxs-lookup"><span data-stu-id="ba337-210">Problem</span></span> | <span data-ttu-id="ba337-211">Пример.</span><span class="sxs-lookup"><span data-stu-id="ba337-211">Example</span></span> | <span data-ttu-id="ba337-212">Решение</span><span class="sxs-lookup"><span data-stu-id="ba337-212">Solution</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="ba337-213">Эффекты рисования влияют на реакцию или анимацию.</span><span class="sxs-lookup"><span data-stu-id="ba337-213">Paint storms affecting response or animation.</span></span>  | <span data-ttu-id="ba337-214">Большие области или дорогостоящие краски влияют на реакцию или анимацию.</span><span class="sxs-lookup"><span data-stu-id="ba337-214">Big paint areas or expensive paints affecting response or animation.</span></span>  | <span data-ttu-id="ba337-215">Избегайте рисования, продвижение элементов, которые перемещаются в собственный слой, использование преобразований и непрозрачности.</span><span class="sxs-lookup"><span data-stu-id="ba337-215">Avoid paint, promote elements that are moving to their own layer, use transforms and opacity.</span></span>  <!--See [Simplify paint complexity and reduce paint areas][WebFundamentalsPerformanceRenderingSimplifyPaintComplexity].  -->  |  
| <span data-ttu-id="ba337-216">Развертывание слоев влияет на анимацию.</span><span class="sxs-lookup"><span data-stu-id="ba337-216">Layer explosions affecting animations.</span></span>  | <span data-ttu-id="ba337-217">Превышение избыточного продвижения слишком большого количества элементов `translateZ(0)` заметно влияет на производительность анимации.</span><span class="sxs-lookup"><span data-stu-id="ba337-217">Overpromotion of too many elements with `translateZ(0)` greatly affects animation performance.</span></span>  | <span data-ttu-id="ba337-218">Придвигайте к слоям экономно и только в том случае, если вы знаете, что она содержит существенные улучшения.</span><span class="sxs-lookup"><span data-stu-id="ba337-218">Promote to layers sparingly, and only when you know it offers tangible improvements.</span></span>  <!--See [Stick to composite-only properties and manage layer count][WebFundamentalsPerformanceRenderingCompositorOnlyProperties].  -->  |  

<!--todo: add Simplify paint complexity and reduce paint areas section when available  -->  
<!--todo: add Stick to compositor-only properties and manage layer count section when available  -->  

## <span data-ttu-id="ba337-219">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ba337-219">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsRenderingToolsJavascriptRuntime]: ./js-runtime.md "Ускорение выполнения JavaScript | Документы Microsoft"  
[DevtoolsChromiumEvaluatePerformanceReferenceEnableadvancedpaintinstrumentation]: ../evaluate-performance/reference.md#enable-advanced-paint-instrumentation "Включение расширенного инструментария рисования — Справка по анализу производительности | Документы Microsoft"

<!--[DevtoolsRenderingToolsForcedSynchronousLayouts]: ./rendering-tools/forced-synchronous-layouts.md "Diagnose Forced Synchronous Layouts | Microsoft Docs"  -->  

<!-- The Timeline Tool page is deprecated  -->  
<!--[DevtoolsEvaluatePerformanceTimelineToolProfileJavascript]: ../evaluate-performance/timeline-tool#profile-javascript "Profile JavaScript - How to Use the Timeline Tool | Microsoft Docs"  -->  
<!--[DevtoolsEvaluatePerformanceTimelineToolProfilePainting]: ../evaluate-performance/timeline-tool#profile-painting "Profile painting - How to Use the Timeline Tool | Microsoft Docs"  -->  
<!--[DevtoolsEvaluatePerformanceTimelineToolRecording]: ../evaluate-performance/timeline-tool#make-a-recording "Make a recording - How to Use the Timeline Tool | Microsoft Docs"  -->  
<!--[DevtoolsEvaluatePerformanceTimelineToolRenderingSettings]: ../evaluate-performance/timeline-tool#rendering-settings "Rendering settings - How to Use the Timeline Tool | Microsoft Docs"  -->  

<!--[WebFundamentalsPerformanceRenderingAvoidLargeComplexLayouts]: /web/fundamentals/performance/rendering/avoid-large-complex-layouts-and-layout-thrashing "Avoid Large, Complex Layouts, and Layout Thrashing"  -->  
<!--[WebFundamentalsPerformanceRenderingOptimizeJavascriptRuntime]: /web/fundamentals/performance/rendering/optimize-javascript-execution "Optimize JavaScript Runtime"  -->  
<!--[WebFundamentalsPerformanceRenderingReduceScope]: /web/fundamentals/performance/rendering/reduce-the-scope-and-complexity-of-style-calculations "Reduce the Scope and Complexity of Style Calculations"  -->  
<!--[WebFundamentalsPerformanceRenderingSimplifyPaintComplexity]: /web/fundamentals/performance/rendering/simplify-paint-complexity-and-reduce-paint-areas "Simplify Paint Complexity and Reduce Paint Areas"  -->  
<!--[WebFundamentalsPerformanceRenderingCompositorOnlyProperties]: /web/fundamentals/performance/rendering/stick-to-compositor-only-properties-and-manage-layer-count "Stick to Compositor-Only Properties and Manage Layer Count"  -->  

[CssTriggers]: https://csstriggers.com "Триггеры CSS"  

[MDNUsingWebWorkers]: https://developer.mozilla.org/docs/Web/API/Web_Workers_API/Using_web_workers "Использование веб-сотрудников | MDN"  

[WebPerformanceCalendarRuntimeChecklist]: https://calendar.perfplanet.com/2013/the-runtime-performance-checklist/ "Контрольный список производительности во время выполнения — Календарь веб-производительности"  

[GitHubWilsonpageFastdom]: https://github.com/wilsonpage/fastdom "wilsonpage/fastdom | GitHub"  

> [!NOTE]
> <span data-ttu-id="ba337-226">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ba337-226">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="ba337-227">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/index) и [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \) и [Meggin Kearney][MegginKearney] \ (технический редактор \).</span><span class="sxs-lookup"><span data-stu-id="ba337-227">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) and [Meggin Kearney][MegginKearney] \(Tech Writer\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="ba337-229">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ba337-229">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
