---
description: Узнайте, как использовать Microsoft Edge DevTools для поиска и исправления ошибок JavaScript.
title: Начало работы с отладкой JavaScript в Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: f8846388f92ba330940b4b6842964d96d9bbce4d
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993396"
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







# <span data-ttu-id="c715e-104">Начало работы с отладкой JavaScript в Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="c715e-104">Get started with debugging JavaScript in Microsoft Edge DevTools</span></span>   



<span data-ttu-id="c715e-105">В этом учебнике вы научитесь основным рабочим процессом для отладки проблем JavaScript в DevTools.</span><span class="sxs-lookup"><span data-stu-id="c715e-105">This tutorial teaches you the basic workflow for debugging any JavaScript issue in DevTools.</span></span>  

## <span data-ttu-id="c715e-106">Шаг 1: воспроизведение ошибки</span><span class="sxs-lookup"><span data-stu-id="c715e-106">Step 1: Reproduce the bug</span></span>   

<span data-ttu-id="c715e-107">Поиск серии действий, которые постоянно воспроизводит ошибки, всегда является первым этапом отладки.</span><span class="sxs-lookup"><span data-stu-id="c715e-107">Finding a series of actions that consistently reproduces a bug is always the first step to debugging.</span></span>  

1.  <span data-ttu-id="c715e-108">Нажмите кнопку **Открыть демонстрацию**.</span><span class="sxs-lookup"><span data-stu-id="c715e-108">Click **Open Demo**.</span></span>  <span data-ttu-id="c715e-109">Удерживайте клавишу `Control` \ (Windows \) или `Command` \ (macOS \) и открывайте демонстрацию на новой вкладке.</span><span class="sxs-lookup"><span data-stu-id="c715e-109">Hold `Control` \(Windows\) or `Command` \(macOS\) and open the demo in a new tab.</span></span>  
    
    [<span data-ttu-id="c715e-110">Открыть демонстрацию</span><span class="sxs-lookup"><span data-stu-id="c715e-110">Open Demo</span></span>][OpenDebugJSDemo]  
    
1.  <span data-ttu-id="c715e-111">Введите `5` текст в текстовом поле **число 1** .</span><span class="sxs-lookup"><span data-stu-id="c715e-111">Enter `5` in the **Number 1** text box.</span></span>  
1.  <span data-ttu-id="c715e-112">Введите `1` текст в текстовое поле **число 2** .</span><span class="sxs-lookup"><span data-stu-id="c715e-112">Enter `1` in the **Number 2** text box.</span></span>  
1.  <span data-ttu-id="c715e-113">Нажмите кнопку **Добавить номер 1 и номер 2**.</span><span class="sxs-lookup"><span data-stu-id="c715e-113">Click **Add Number 1 and Number 2**.</span></span>  <span data-ttu-id="c715e-114">Надпись под кнопкой содержит сообщение `5 + 1 = 51` .</span><span class="sxs-lookup"><span data-stu-id="c715e-114">The label below the button says `5 + 1 = 51`.</span></span>  <span data-ttu-id="c715e-115">Результат должен быть `6` .</span><span class="sxs-lookup"><span data-stu-id="c715e-115">The result should be `6`.</span></span>  <span data-ttu-id="c715e-116">Это ошибка, которую вы собираетесь исправить.</span><span class="sxs-lookup"><span data-stu-id="c715e-116">This is the bug you are going to fix.</span></span>  
    
    :::image type="complex" source="../media/javascript-js-demo-bad.msft.png" alt-text="Результатом 5 + 1 является 51, а должно быть 6." lightbox="../media/javascript-js-demo-bad.msft.png":::
       <span data-ttu-id="c715e-118">Результат состоит в `5 + 1` том `51` , что</span><span class="sxs-lookup"><span data-stu-id="c715e-118">The result of `5 + 1` is `51`, but should be</span></span> `6`  
    :::image-end:::  
    
## <span data-ttu-id="c715e-119">Шаг 2: знакомство с пользовательским интерфейсом панели «источники»</span><span class="sxs-lookup"><span data-stu-id="c715e-119">Step 2: Get familiar with the Sources panel UI</span></span>   

<span data-ttu-id="c715e-120">DevTools предоставляет множество различных инструментов для различных задач, таких как изменение CSS, профилирование нагрузки страниц и мониторинг сетевых запросов.</span><span class="sxs-lookup"><span data-stu-id="c715e-120">DevTools provides a lot of different tools for different tasks, such as changing CSS, profiling page load performance, and monitoring network requests.</span></span>  <span data-ttu-id="c715e-121">На панели « **источники** » можно выполнить отладку JavaScript.</span><span class="sxs-lookup"><span data-stu-id="c715e-121">The **Sources** panel is where you debug JavaScript.</span></span>  

1.  <span data-ttu-id="c715e-122">Откройте DevTools, нажав клавиши `Control` + `Shift` + `J` \ (Windows \) или `Command` + `Option` + `J` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="c715e-122">Open DevTools by pressing `Control`+`Shift`+`J` \(Windows\) or `Command`+`Option`+`J` \(macOS\) .</span></span>  <span data-ttu-id="c715e-123">С помощью этого ярлыка открывается панель **консоли** .</span><span class="sxs-lookup"><span data-stu-id="c715e-123">This shortcut opens the **Console** panel.</span></span>  
    
    :::image type="complex" source="../media/javascript-console-empty.msft.png" alt-text="Результатом 5 + 1 является 51, а должно быть 6." lightbox="../media/javascript-console-empty.msft.png":::
       <span data-ttu-id="c715e-125">Панель **консоли**</span><span class="sxs-lookup"><span data-stu-id="c715e-125">The **Console** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c715e-126">Откройте вкладку **источники** .</span><span class="sxs-lookup"><span data-stu-id="c715e-126">Click the **Sources** tab.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-sections.msft.png" alt-text="Результатом 5 + 1 является 51, а должно быть 6." lightbox="../media/javascript-sources-sections.msft.png":::
       <span data-ttu-id="c715e-128">Панель « **источники** »</span><span class="sxs-lookup"><span data-stu-id="c715e-128">The **Sources** panel</span></span>  
    :::image-end:::  
    
<span data-ttu-id="c715e-129">В пользовательском интерфейсе панели « **источники** » есть 3 части.</span><span class="sxs-lookup"><span data-stu-id="c715e-129">The **Sources** panel UI has 3 parts.</span></span>  

:::image type="complex" source="../media/javascript-sources-sections-annotated.msft.png" alt-text="Результатом 5 + 1 является 51, а должно быть 6." lightbox="../media/javascript-sources-sections-annotated.msft.png":::
   <span data-ttu-id="c715e-131">3 части пользовательского интерфейса панели « **источники** »</span><span class="sxs-lookup"><span data-stu-id="c715e-131">The 3 parts of the **Sources** panel UI</span></span>  
:::image-end:::  

1.  <span data-ttu-id="c715e-132">Область " **Навигатор файлов** " \ (раздел 1 на предыдущем рисунке).</span><span class="sxs-lookup"><span data-stu-id="c715e-132">The **File Navigator** pane \(Section 1 in the previous figure\).</span></span>  <span data-ttu-id="c715e-133">Здесь перечислены все файлы, на которые поступают запросы страниц.</span><span class="sxs-lookup"><span data-stu-id="c715e-133">Every file that the page requests is listed here.</span></span>  
1.  <span data-ttu-id="c715e-134">Область **редактора кода** \ (раздел 2 на предыдущем рисунке).</span><span class="sxs-lookup"><span data-stu-id="c715e-134">The **Code Editor** pane \(Section 2 in the previous figure\).</span></span>  <span data-ttu-id="c715e-135">После того как вы выберете файл в области **навигатора по файлам** , здесь отображается содержимое этого файла.</span><span class="sxs-lookup"><span data-stu-id="c715e-135">After selecting a file in the **File Navigator** pane, the contents of that file are displayed here.</span></span>  
1.  <span data-ttu-id="c715e-136">Область **отладки JavaScript** \ (раздел 3 на предыдущем рисунке).</span><span class="sxs-lookup"><span data-stu-id="c715e-136">The **JavaScript Debugging** pane \(Section 3 in the previous figure\).</span></span>  <span data-ttu-id="c715e-137">Различные инструменты для проверки JavaScript на странице.</span><span class="sxs-lookup"><span data-stu-id="c715e-137">Various tools for inspecting the JavaScript for the page.</span></span>  <span data-ttu-id="c715e-138">Если окно DevTools имеет ширину, эта область отображается справа от области **редактора кода** .</span><span class="sxs-lookup"><span data-stu-id="c715e-138">If your DevTools window is wide, this pane is displayed to the right of the **Code Editor** pane.</span></span>  
    
## <span data-ttu-id="c715e-139">Шаг 3: Приостановка кода с помощью точки останова</span><span class="sxs-lookup"><span data-stu-id="c715e-139">Step 3: Pause the code with a breakpoint</span></span>   

<span data-ttu-id="c715e-140">Наиболее распространенный способ отладки такого сбоя — Вставка в код большого количества инструкций для `console.log()` проверки значений по мере выполнения сценария.</span><span class="sxs-lookup"><span data-stu-id="c715e-140">A common method for debugging a problem like this is to insert a lot of `console.log()` statements into the code, in order to inspect values as the script runs.</span></span>  <span data-ttu-id="c715e-141">Например:</span><span class="sxs-lookup"><span data-stu-id="c715e-141">For example:</span></span>  

```javascript
function updateLabel() {
    var addend1 = getNumber1();
    console.log('addend1:', addend1);
    var addend2 = getNumber2();
    console.log('addend2:', addend2);
    var sum = addend1 + addend2;
    console.log('sum:', sum);
    label.textContent = addend1 + ' + ' + addend2 + ' = ' + sum;
}
```  

<span data-ttu-id="c715e-142">Этот `console.log()` метод может быть выполнен, но **точки останова** могут сделать ее более быстрой.</span><span class="sxs-lookup"><span data-stu-id="c715e-142">The `console.log()` method may get the job done, but **breakpoints** are able to get it done faster.</span></span>  <span data-ttu-id="c715e-143">С помощью точки останова можно приостановить выполнение кода в середине среды выполнения и проанализировать все значения в данный момент времени.</span><span class="sxs-lookup"><span data-stu-id="c715e-143">A breakpoint lets you pause your code in the middle of the runtime, and examine all values at that moment in time.</span></span>  <span data-ttu-id="c715e-144">В методе точки останова есть несколько преимуществ `console.log()` .</span><span class="sxs-lookup"><span data-stu-id="c715e-144">Breakpoints have a few advantages over the `console.log()` method:</span></span>  

*   <span data-ttu-id="c715e-145">Кроме `console.log()` того, необходимо вручную открыть исходный код, найти нужный код, вставить `console.log()` инструкции, а затем снова загрузить страницу, чтобы просмотреть сообщения на консоли.</span><span class="sxs-lookup"><span data-stu-id="c715e-145">With `console.log()`, you need to manually open the source code, find the relevant code, insert the `console.log()` statements, and then reload the page in order to see the messages in the Console.</span></span>  <span data-ttu-id="c715e-146">С помощью точек останова вы можете приостановить выполнение нужного кода, даже не зная структуру кода.</span><span class="sxs-lookup"><span data-stu-id="c715e-146">With breakpoints, you may pause on the relevant code without even knowing how the code is structured.</span></span>  
*   <span data-ttu-id="c715e-147">В `console.log()` инструкции Вам необходимо явным образом указать каждое значение, которое нужно проверить.</span><span class="sxs-lookup"><span data-stu-id="c715e-147">In your `console.log()` statements you need to explicitly specify each value that you want to inspect.</span></span>  <span data-ttu-id="c715e-148">С помощью точек останова DevTools показывает значения всех переменных в данный момент времени.</span><span class="sxs-lookup"><span data-stu-id="c715e-148">With breakpoints, DevTools shows you the values of all variables at that moment in time.</span></span>  <span data-ttu-id="c715e-149">Иногда есть переменные, влияющие на ваш код, на который вы еще не осведомлены.</span><span class="sxs-lookup"><span data-stu-id="c715e-149">Sometimes there are variables affecting your code that you are not even aware of.</span></span>  

<span data-ttu-id="c715e-150">Короче говоря, точки останова могут помочь вам находить и устранять ошибки быстрее, чем `console.log()` метод.</span><span class="sxs-lookup"><span data-stu-id="c715e-150">In short, breakpoints may help you find and fix bugs faster than the `console.log()` method.</span></span>  

<span data-ttu-id="c715e-151">Если вы перейдете на шаг назад и хотите подумать о том, как работает приложение, вы можете сделать обоснованную оценку того, что в `5 + 1 = 51` `click` прослушиватель событий, связанный с кнопкой " **добавить число 1" и "номер 2** ", вычисляется неправильное значение Sum ().</span><span class="sxs-lookup"><span data-stu-id="c715e-151">If you take a step back and think about how the app works, you are able to make an educated guess that the incorrect sum (`5 + 1 = 51`) gets computed in the `click` event listener that is associated to the **Add Number 1 and Number 2** button.</span></span>  <span data-ttu-id="c715e-152">Таким образом, вам, возможно, потребуется приостановить код на время `click` выполнения слушателя.</span><span class="sxs-lookup"><span data-stu-id="c715e-152">Therefore, you probably want to pause the code around the time that the `click` listener runs.</span></span>  <span data-ttu-id="c715e-153">**Точки останова для прослушивателей событий** позволяют точно так:</span><span class="sxs-lookup"><span data-stu-id="c715e-153">**Event Listener Breakpoints** let you do exactly that:</span></span>  

1.  <span data-ttu-id="c715e-154">В области **Отладка JavaScript** щелкните **точки останова прослушивателя событий** , чтобы развернуть раздел.</span><span class="sxs-lookup"><span data-stu-id="c715e-154">In the **JavaScript Debugging** pane, click **Event Listener Breakpoints** to expand the section.</span></span>  <span data-ttu-id="c715e-155">DevTools открывает список категорий расширяемых событий, таких как **анимация** и **буфер обмена**.</span><span class="sxs-lookup"><span data-stu-id="c715e-155">DevTools reveals a list of expandable event categories, such as **Animation** and **Clipboard**.</span></span>  
1.  <span data-ttu-id="c715e-156">Рядом с категорией событие **мыши** нажмите кнопку **развернуть** \ ( ![ развернуть значок ][ImageExpandIcon] \).</span><span class="sxs-lookup"><span data-stu-id="c715e-156">Next to the **Mouse** event category, click **Expand** \(![Expand icon][ImageExpandIcon]\).</span></span>  <span data-ttu-id="c715e-157">DevTools открывает список событий мыши, например **Click** и **MouseDown**.</span><span class="sxs-lookup"><span data-stu-id="c715e-157">DevTools reveals a list of mouse events, such as **click** and **mousedown**.</span></span>  <span data-ttu-id="c715e-158">Рядом с каждым событием установлен флажок.</span><span class="sxs-lookup"><span data-stu-id="c715e-158">Each event has a checkbox next to it.</span></span>  
1.  <span data-ttu-id="c715e-159">Установите флажок **щелкнуть** .</span><span class="sxs-lookup"><span data-stu-id="c715e-159">Check the **click** checkbox.</span></span>  <span data-ttu-id="c715e-160">DevTools теперь настроен на автоматическую приостановку при запуске *любого* `click` прослушивателя событий.</span><span class="sxs-lookup"><span data-stu-id="c715e-160">DevTools is now set up to automatically pause when *any* `click` event listener runs.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-event-listener-breakpoint-mouse-click.msft.png" alt-text="Результатом 5 + 1 является 51, а должно быть 6." lightbox="../media/javascript-sources-event-listener-breakpoint-mouse-click.msft.png":::
       <span data-ttu-id="c715e-162">Флажок " **Нажатие кнопки** " включен</span><span class="sxs-lookup"><span data-stu-id="c715e-162">The **click** checkbox is enabled</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c715e-163">Вернитесь на демонстрацию, нажмите кнопку **Добавить номер 1 и номер 2** еще раз.</span><span class="sxs-lookup"><span data-stu-id="c715e-163">Back on the demo, click **Add Number 1 and Number 2** again.</span></span>  <span data-ttu-id="c715e-164">DevTools приостанавливает демонстрацию и выделяет строку кода на панели « **источники** ».</span><span class="sxs-lookup"><span data-stu-id="c715e-164">DevTools pauses the demo and highlights a line of code in the **Sources** panel.</span></span>  <span data-ttu-id="c715e-165">DevTools должен быть приостановлен в строке 16 `get-started.js` .</span><span class="sxs-lookup"><span data-stu-id="c715e-165">DevTools should pause on line 16 in `get-started.js`.</span></span>  
    
    ```javascript
    if (inputsAreEmpty()) {
    ```  
    
    <span data-ttu-id="c715e-166">Если наведите указатель мыши на другую строку кода, нажмите кнопку **возобновить выполнение сценария** и ( ![ возобновить выполнение сценария ][ImageResumeIcon] ), пока вы не нажмете указатель мыши на нужной строке.</span><span class="sxs-lookup"><span data-stu-id="c715e-166">If you pause on a different line of code, press **Resume Script Execution** \(![Resume Script Execution][ImageResumeIcon]\) until you pause on the correct line.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="c715e-167">Если вы приостановили другую строку, у вас есть расширение браузера, которое регистрирует `click` прослушиватель событий на каждой странице, которую вы посещаете.</span><span class="sxs-lookup"><span data-stu-id="c715e-167">If you paused on a different line, you have a browser extension that registers a `click` event listener on every page that you visit.</span></span>  <span data-ttu-id="c715e-168">Вы приостановили `click` прослушиватель расширения.</span><span class="sxs-lookup"><span data-stu-id="c715e-168">You were paused in the `click` listener of the extension.</span></span>  <span data-ttu-id="c715e-169">Если вы используете режим InPrivate для **просмотра личных**данных, который отключает все расширения, вы можете увидеть, что вы приостанавливаете каждую из них в нужной строке кода.</span><span class="sxs-lookup"><span data-stu-id="c715e-169">If you use InPrivate Mode to **browse in private**, which disables all extensions, you may see that you pause on the desired line of code every time.</span></span>  

<!--todo: add inprivate section when available -->  

<span data-ttu-id="c715e-170">**Точки останова для прослушивателей событий** — это только один из многих типов точек останова, доступных в DevTools.</span><span class="sxs-lookup"><span data-stu-id="c715e-170">**Event Listener Breakpoints** are just one of many types of breakpoints available in DevTools.</span></span>  <span data-ttu-id="c715e-171">Стоит запомнить все различные типы, поскольку каждый из них в конечном итоге поможет вам быстрее отлаживать различные сценарии.</span><span class="sxs-lookup"><span data-stu-id="c715e-171">It is worth memorizing all the different types, because each type ultimately helps you debug different scenarios as quickly as possible.</span></span>  <!--See [Pause Your Code With Breakpoints][JSBreakpoints] to learn when and how to use each type.  -->  

## <span data-ttu-id="c715e-172">Шаг 4: пошаговое руководство по коду</span><span class="sxs-lookup"><span data-stu-id="c715e-172">Step 4: Step through the code</span></span>   

<span data-ttu-id="c715e-173">Одной из распространенных причин ошибок является то, что сценарий выполняется в неправильном порядке.</span><span class="sxs-lookup"><span data-stu-id="c715e-173">One common cause of bugs is when a script runs in the wrong order.</span></span>  <span data-ttu-id="c715e-174">Пошаговое выполнение кода позволяет проанализировать исполняющую среду вашего кода, по одной строке и точно определить, в каком порядке она работает, не превышающие ожидаемый.</span><span class="sxs-lookup"><span data-stu-id="c715e-174">Stepping through your code enables you to walk through the runtime of your code, one line at a time, and figure out exactly where it is running in a different order than you expected.</span></span>  <span data-ttu-id="c715e-175">Попробуйте вот так:</span><span class="sxs-lookup"><span data-stu-id="c715e-175">Try it now:</span></span>  

1.  <span data-ttu-id="c715e-176">Нажмите кнопку " **Перейти к следующему вызову функции** " ( ![ шаг за следующий вызов функции ][ImageOverIcon] ).</span><span class="sxs-lookup"><span data-stu-id="c715e-176">Click **Step over next function call** \(![Step over next function call][ImageOverIcon]\).</span></span>  <span data-ttu-id="c715e-177">DevTools запускает следующий код без пошагового выполнения.</span><span class="sxs-lookup"><span data-stu-id="c715e-177">DevTools runs the following code without stepping into it.</span></span>  
    
    ```javascript
    if (inputsAreEmpty()) {
    ```  
    
    > [!NOTE]
    > <span data-ttu-id="c715e-178">DevTools пропускает несколько строк кода.</span><span class="sxs-lookup"><span data-stu-id="c715e-178">DevTools skips a few lines of code.</span></span>  <span data-ttu-id="c715e-179">Это происходит из-за того `inputsAreEmpty()` , что результатом вычисления является значение ложь, поэтому блок кода для `if` инструкции не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c715e-179">This is because `inputsAreEmpty()` evaluates as false, so the block of code for the `if` statement does not run.</span></span>  
    
1.  <span data-ttu-id="c715e-180">На панели **источники** DevTools выберите команду Шаг с **заходом к следующей функции** \ ( ![ Шаг с заходом в следующую функцию ][ImageIntoIcon] ), чтобы пошагово пройти все `updateLabel()` время выполнения функции, по одной строке за раз.</span><span class="sxs-lookup"><span data-stu-id="c715e-180">On the **Sources** panel of DevTools, click **Step into next function call** \(![Step into next function call][ImageIntoIcon]\) to step through the runtime of the `updateLabel()` function, one line at a time.</span></span>  
    
<span data-ttu-id="c715e-181">Это основная идея пошагового выполнения кода.</span><span class="sxs-lookup"><span data-stu-id="c715e-181">That is the basic idea of stepping through code.</span></span>  <span data-ttu-id="c715e-182">Если посмотреть на код в `get-started.js` , вы увидите, что ошибка может находиться где-то в `updateLabel()` функции.</span><span class="sxs-lookup"><span data-stu-id="c715e-182">If you look at the code in `get-started.js`, you see that the bug is probably somewhere in the `updateLabel()` function.</span></span>  <span data-ttu-id="c715e-183">Вместо того чтобы пошагово пройти все строки кода, вы можете использовать другой тип точки останова, чтобы приостановить код ближе к вероятному расположению ошибки.</span><span class="sxs-lookup"><span data-stu-id="c715e-183">Rather than stepping through every line of code, you may use another type of breakpoint to pause the code closer to the probable location of the bug.</span></span>  

## <span data-ttu-id="c715e-184">Шаг 5. Установка точки останова в коде строки</span><span class="sxs-lookup"><span data-stu-id="c715e-184">Step 5: Set a line-of-code breakpoint</span></span>   

<span data-ttu-id="c715e-185">Точки останова по строкам кода — это наиболее распространенный тип точки останова.</span><span class="sxs-lookup"><span data-stu-id="c715e-185">Line-of-code breakpoints are the most common type of breakpoint.</span></span>  <span data-ttu-id="c715e-186">Когда вы получаете определенную строку кода, которую вы хотите приостановить, используйте точку останова для строки кода:</span><span class="sxs-lookup"><span data-stu-id="c715e-186">When you get the specific line of code that you want to pause on, use a line-of-code breakpoint:</span></span>  

1.  <span data-ttu-id="c715e-187">Рассмотрим последнюю строку кода `updateLabel()` :</span><span class="sxs-lookup"><span data-stu-id="c715e-187">Look at the last line of code in `updateLabel()`:</span></span>  
    
    ```javascript
    label.textContent = addend1 + ' + ' + addend2 + ' = ' + sum;
    ```  
    
1.  <span data-ttu-id="c715e-188">Слева от кода отображается номер строки данной строки кода, **33**.</span><span class="sxs-lookup"><span data-stu-id="c715e-188">To the left of the code you see the line number of this particular line of code, which is **33**.</span></span>  <span data-ttu-id="c715e-189">Щелкните **33**.</span><span class="sxs-lookup"><span data-stu-id="c715e-189">Click on **33**.</span></span>  <span data-ttu-id="c715e-190">DevTools помещает красный значок слева от **33**.</span><span class="sxs-lookup"><span data-stu-id="c715e-190">DevTools puts a red icon to the left of **33**.</span></span>  <span data-ttu-id="c715e-191">Это означает, что в этой строке есть точка останова из строки кода.</span><span class="sxs-lookup"><span data-stu-id="c715e-191">This means that there is a line-of-code breakpoint on this line.</span></span>  <span data-ttu-id="c715e-192">DevTools теперь всегда задерживается перед выполнением этой строки кода.</span><span class="sxs-lookup"><span data-stu-id="c715e-192">DevTools now always pauses before this line of code is run.</span></span>  
1.  <span data-ttu-id="c715e-193">Нажмите кнопку **возобновить выполнение сценария** ( ![ возобновить выполнение сценария ][ImageResumeIcon] ).</span><span class="sxs-lookup"><span data-stu-id="c715e-193">Click **Resume script execution** \(![Resume script execution][ImageResumeIcon]\).</span></span>  <span data-ttu-id="c715e-194">Сценарий продолжит работу, пока не достигнет строки 33.</span><span class="sxs-lookup"><span data-stu-id="c715e-194">The script continues running until it reaches line 33.</span></span>  <span data-ttu-id="c715e-195">В строках с 30, 31 и 32 DevTools распечатывает значения и `addend1` `addend2` `sum` справа от точки с запятой в каждой строке.</span><span class="sxs-lookup"><span data-stu-id="c715e-195">On lines 30, 31, and 32, DevTools prints out the values of `addend1`, `addend2`, and `sum` to the right of the semi-colon on each line.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-breakpoint-paused.msft.png" alt-text="Результатом 5 + 1 является 51, а должно быть 6." lightbox="../media/javascript-sources-breakpoint-paused.msft.png":::
       <span data-ttu-id="c715e-197">DevTools приостанавливается на точке останова строки кода в строке 32</span><span class="sxs-lookup"><span data-stu-id="c715e-197">DevTools pauses on the line-of-code breakpoint on line 32</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="c715e-198">Шаг 6: Проверка значений переменной</span><span class="sxs-lookup"><span data-stu-id="c715e-198">Step 6: Check variable values</span></span>   

<span data-ttu-id="c715e-199">Значения `addend1` `addend2` и `sum` вид подозрительных.</span><span class="sxs-lookup"><span data-stu-id="c715e-199">The values of `addend1`, `addend2`, and `sum` look suspicious.</span></span>  <span data-ttu-id="c715e-200">Они заключены в кавычки, что означает, что они являются строками.</span><span class="sxs-lookup"><span data-stu-id="c715e-200">They are wrapped in quotes, which means that they are strings.</span></span>  <span data-ttu-id="c715e-201">Это хорошая гипотеза, объясняющая причину ошибки.</span><span class="sxs-lookup"><span data-stu-id="c715e-201">This is a good hypothesis for the explaining the cause of the bug.</span></span>  <span data-ttu-id="c715e-202">Теперь пора собрать дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="c715e-202">Now it is time to gather more information.</span></span>  <span data-ttu-id="c715e-203">DevTools предоставляет множество инструментов для проверки значений переменных.</span><span class="sxs-lookup"><span data-stu-id="c715e-203">DevTools provides a lot of tools for examining variable values.</span></span>  

### <span data-ttu-id="c715e-204">Способ 1: область "область"</span><span class="sxs-lookup"><span data-stu-id="c715e-204">Method 1: The Scope pane</span></span>   

<span data-ttu-id="c715e-205">Когда вы наводите указатель на строку кода, область " **область** " показывает, какие локальные и глобальные переменные определяются в настоящее время, а также значения каждой переменной.</span><span class="sxs-lookup"><span data-stu-id="c715e-205">When you pause on a line of code, the **Scope** pane shows you what local and global variables are currently defined, along with the value of each variable.</span></span>  <span data-ttu-id="c715e-206">Кроме того, при необходимости отображаются переменные замыкания.</span><span class="sxs-lookup"><span data-stu-id="c715e-206">It also shows closure variables, when applicable.</span></span>  <span data-ttu-id="c715e-207">Дважды щелкните значение переменной, чтобы изменить его.</span><span class="sxs-lookup"><span data-stu-id="c715e-207">Double-click a variable value to edit it.</span></span>  <span data-ttu-id="c715e-208">Если вы не надерживаетесь в строке кода, область " **область** " пуста.</span><span class="sxs-lookup"><span data-stu-id="c715e-208">When you are not paused on a line of code, the **Scope** pane is empty.</span></span>  

:::image type="complex" source="../media/javascript-sources-breakpoint-paused-scope.msft.png" alt-text="Результатом 5 + 1 является 51, а должно быть 6." lightbox="../media/javascript-sources-breakpoint-paused-scope.msft.png":::
   <span data-ttu-id="c715e-210">Область " **область** "</span><span class="sxs-lookup"><span data-stu-id="c715e-210">The **Scope** pane</span></span>  
:::image-end:::  

### <span data-ttu-id="c715e-211">Способ 2: контрольные выражения</span><span class="sxs-lookup"><span data-stu-id="c715e-211">Method 2: Watch Expressions</span></span>   

<span data-ttu-id="c715e-212">С помощью вкладки " **выражения контрольного значения** " можно отслеживать значения переменных с течением времени.</span><span class="sxs-lookup"><span data-stu-id="c715e-212">The **Watch Expressions** tab lets you monitor the values of variables over time.</span></span>  <span data-ttu-id="c715e-213">Как и названия, выражения контрольного значения не ограничиваются только переменными.</span><span class="sxs-lookup"><span data-stu-id="c715e-213">As the name implies, Watch Expressions are not just limited to variables.</span></span>  <span data-ttu-id="c715e-214">Вы можете хранить любое допустимое выражение JavaScript в выражении Watch.</span><span class="sxs-lookup"><span data-stu-id="c715e-214">You are able to store any valid JavaScript expression in a Watch Expression.</span></span>  <span data-ttu-id="c715e-215">Попробуйте вот так:</span><span class="sxs-lookup"><span data-stu-id="c715e-215">Try it now:</span></span>  

1.  <span data-ttu-id="c715e-216">Откройте вкладку **Контрольные значения** .</span><span class="sxs-lookup"><span data-stu-id="c715e-216">Click the **Watch** tab.</span></span>  
1.  <span data-ttu-id="c715e-217">Нажмите кнопку **Добавить выражение** \ ( ![ Добавить выражение ][ImageAddIcon] \).</span><span class="sxs-lookup"><span data-stu-id="c715e-217">Click **Add Expression** \(![Add Expression][ImageAddIcon]\).</span></span>  
1.  <span data-ttu-id="c715e-218">Введите `typeof sum`.</span><span class="sxs-lookup"><span data-stu-id="c715e-218">Type `typeof sum`.</span></span>  
1.  <span data-ttu-id="c715e-219">Нажмите клавишу `Enter` .</span><span class="sxs-lookup"><span data-stu-id="c715e-219">Press `Enter`.</span></span>  <span data-ttu-id="c715e-220">DevTools показан `typeof sum: "string"` .</span><span class="sxs-lookup"><span data-stu-id="c715e-220">DevTools shows `typeof sum: "string"`.</span></span>  <span data-ttu-id="c715e-221">Значение справа от двоеточия является результатом вашего выражения контрольного значения.</span><span class="sxs-lookup"><span data-stu-id="c715e-221">The value to the right of the colon is the result of your Watch Expression.</span></span>  
    
> [!NOTE]
> <span data-ttu-id="c715e-222">В области выражения для контрольных значений \ (внизу справа) на рисунке ниже `typeof sum` показано выражение Watch.</span><span class="sxs-lookup"><span data-stu-id="c715e-222">In the Watch Expression pane \(bottom-right\) in in the following figure, the `typeof sum` Watch Expression is displayed.</span></span>  <span data-ttu-id="c715e-223">Если окно DevTools велико, область выражения контрольных значений находится справа над областью **точки останова прослушивателя событий** .</span><span class="sxs-lookup"><span data-stu-id="c715e-223">If your DevTools window is large, the Watch Expression pane is on the right above the **Event Listener Breakpoints** pane.</span></span>  

:::image type="complex" source="../media/javascript-sources-breakpoint-paused-watch.msft.png" alt-text="Результатом 5 + 1 является 51, а должно быть 6." lightbox="../media/javascript-sources-breakpoint-paused-watch.msft.png":::
   <span data-ttu-id="c715e-225">Область " **выражение контрольного значения** "</span><span class="sxs-lookup"><span data-stu-id="c715e-225">The **Watch Expression** pane</span></span>  
:::image-end:::  

<span data-ttu-id="c715e-226">Как и `sum` предполагается, вычисляется как строка, когда она должна быть числом.</span><span class="sxs-lookup"><span data-stu-id="c715e-226">As suspected, `sum` is being evaluated as a string, when it should be a number.</span></span>  <span data-ttu-id="c715e-227">Теперь вы подтверждаете, что это причина ошибки.</span><span class="sxs-lookup"><span data-stu-id="c715e-227">You have now confirmed that this is the cause of the bug.</span></span>  

### <span data-ttu-id="c715e-228">Способ 3: консоль</span><span class="sxs-lookup"><span data-stu-id="c715e-228">Method 3: The Console</span></span>   

<span data-ttu-id="c715e-229">Помимо просмотра `console.log()` сообщений, вы также можете использовать консоль для оценки произвольных операторов JavaScript.</span><span class="sxs-lookup"><span data-stu-id="c715e-229">In addition to viewing `console.log()` messages, you may also use the Console to evaluate arbitrary JavaScript statements.</span></span>  <span data-ttu-id="c715e-230">С точки зрения отладки вы можете использовать консоль для проверки возможных исправлений ошибок.</span><span class="sxs-lookup"><span data-stu-id="c715e-230">In terms of debugging, you may use the Console to test out potential fixes for bugs.</span></span>  <span data-ttu-id="c715e-231">Попробуйте вот так:</span><span class="sxs-lookup"><span data-stu-id="c715e-231">Try it now:</span></span>  

1.  <span data-ttu-id="c715e-232">Если вы не открыли ящик консоли, нажмите, `Escape` чтобы открыть его.</span><span class="sxs-lookup"><span data-stu-id="c715e-232">If you do not have the Console drawer open, press `Escape` to open it.</span></span>  <span data-ttu-id="c715e-233">Она откроется в нижней части окна DevTools.</span><span class="sxs-lookup"><span data-stu-id="c715e-233">It opens at the bottom of your DevTools window.</span></span>  
1.  <span data-ttu-id="c715e-234">В окне консоли введите `parseInt(addend1) + parseInt(addend2)` .</span><span class="sxs-lookup"><span data-stu-id="c715e-234">In the Console, type `parseInt(addend1) + parseInt(addend2)`.</span></span>  <span data-ttu-id="c715e-235">Эта инструкция работает, так как вы придерживаетесь к строке кода, `addend1` в которой и `addend2` находятся в области.</span><span class="sxs-lookup"><span data-stu-id="c715e-235">This statement works because you are paused on a line of code where `addend1` and `addend2` are in scope.</span></span>  
1.  <span data-ttu-id="c715e-236">Нажмите клавишу `Enter` .</span><span class="sxs-lookup"><span data-stu-id="c715e-236">Press `Enter`.</span></span>  <span data-ttu-id="c715e-237">DevTools оценивает оператор и печатает `6` результаты, что является результатом, который вы ожидаете.</span><span class="sxs-lookup"><span data-stu-id="c715e-237">DevTools evaluates the statement and prints out `6`, which is the result you expect the demo to produce.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-breakpoint-paused-console.msft.png" alt-text="Результатом 5 + 1 является 51, а должно быть 6." lightbox="../media/javascript-sources-breakpoint-paused-console.msft.png":::
       <span data-ttu-id="c715e-239">Входной ящик **консоли** после оценки</span><span class="sxs-lookup"><span data-stu-id="c715e-239">The **Console** drawer, after evaluating</span></span> `parseInt(addend1) + parseInt(addend2)`  
    :::image-end:::  
    
## <span data-ttu-id="c715e-240">Шаг 7: применение исправления</span><span class="sxs-lookup"><span data-stu-id="c715e-240">Step 7: Apply a fix</span></span>   

<span data-ttu-id="c715e-241">Если вы нашли исправление ошибки, исправьте его, изменив код и повторно выполнив демонстрацию.</span><span class="sxs-lookup"><span data-stu-id="c715e-241">If you find a fix for the bug, try out your fix by editing the code and re-running the demo.</span></span>  <span data-ttu-id="c715e-242">Для применения исправления вам не нужно выходить из DevTools.</span><span class="sxs-lookup"><span data-stu-id="c715e-242">You do not need to leave DevTools to apply the fix.</span></span>  <span data-ttu-id="c715e-243">Вы можете редактировать код JavaScript прямо в пользовательском интерфейсе DevTools.</span><span class="sxs-lookup"><span data-stu-id="c715e-243">You are able to edit JavaScript code directly within the DevTools UI.</span></span>  <span data-ttu-id="c715e-244">Попробуйте вот так:</span><span class="sxs-lookup"><span data-stu-id="c715e-244">Try it now:</span></span>  

1.  <span data-ttu-id="c715e-245">Нажмите кнопку **возобновить выполнение сценария** ( ![ возобновить выполнение сценария ][ImageResumeIcon] ).</span><span class="sxs-lookup"><span data-stu-id="c715e-245">Click **Resume script execution** \(![Resume script execution][ImageResumeIcon]\).</span></span>  
1.  <span data-ttu-id="c715e-246">В **редакторе кода**замените строку 32, `var sum = addend1 + addend2` с `var sum = parseInt(addend1) + parseInt(addend2)` .</span><span class="sxs-lookup"><span data-stu-id="c715e-246">In the **Code Editor**, replace line 32, `var sum = addend1 + addend2`, with `var sum = parseInt(addend1) + parseInt(addend2)`.</span></span>  
1.  <span data-ttu-id="c715e-247">`Control` + `S` Чтобы сохранить изменения, нажмите клавиши \ (Windows \) или `Command` + `S` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="c715e-247">Press `Control`+`S` \(Windows\) or `Command`+`S` \(macOS\) to save your change.</span></span>  
1.  <span data-ttu-id="c715e-248">Щелкните **отключить точки останова** \ ( ![ отключить точки останова ][ImageDeactivateIcon] \).</span><span class="sxs-lookup"><span data-stu-id="c715e-248">Click **Deactivate breakpoints** \(![Deactivate breakpoints][ImageDeactivateIcon]\).</span></span>  <span data-ttu-id="c715e-249">Она изменится на синий, чтобы показать, что она активна.</span><span class="sxs-lookup"><span data-stu-id="c715e-249">It changes blue to indicate that it is active.</span></span>  <span data-ttu-id="c715e-250">Несмотря на то, что этот параметр установлен, DevTools игнорирует любые точки останова, заданные вами.</span><span class="sxs-lookup"><span data-stu-id="c715e-250">While this is set, DevTools ignores any breakpoints you set.</span></span>  
1.  <span data-ttu-id="c715e-251">Попробуйте использовать демонстрационную версию с разными значениями.</span><span class="sxs-lookup"><span data-stu-id="c715e-251">Try out the demo with different values.</span></span>  <span data-ttu-id="c715e-252">Демонстрация будет правильно рассчитывается.</span><span class="sxs-lookup"><span data-stu-id="c715e-252">The demo now calculates correctly.</span></span>  
    
> [!CAUTION]
> <span data-ttu-id="c715e-253">Этот рабочий процесс применяет исправление только к коду, который выполняется в браузере.</span><span class="sxs-lookup"><span data-stu-id="c715e-253">This workflow only applies a fix to the code that is running in your browser.</span></span>  <span data-ttu-id="c715e-254">Она не исправляет код для всех пользователей, которые посещает страницу.</span><span class="sxs-lookup"><span data-stu-id="c715e-254">It does not fix the code for all users that visit your page.</span></span>  <span data-ttu-id="c715e-255">Для этого вам нужно исправить код, который находится на сервере.</span><span class="sxs-lookup"><span data-stu-id="c715e-255">To do that, you need to fix the code that is on your servers.</span></span>  

## <span data-ttu-id="c715e-256">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="c715e-256">Next steps</span></span>   

<span data-ttu-id="c715e-257">Поздравляем!</span><span class="sxs-lookup"><span data-stu-id="c715e-257">Congratulations!</span></span>  <span data-ttu-id="c715e-258">Теперь вы знаете, как максимально эффективно использовать Microsoft Edge DevTools при отладке JavaScript.</span><span class="sxs-lookup"><span data-stu-id="c715e-258">You now know how to make the most of Microsoft Edge DevTools when debugging JavaScript.</span></span>  <span data-ttu-id="c715e-259">Средства и методы, описанные в этом учебнике, помогут вам сэкономить бесчисленные часы.</span><span class="sxs-lookup"><span data-stu-id="c715e-259">The tools and methods you learned in this tutorial may save you countless hours.</span></span>  

<span data-ttu-id="c715e-260">В этом учебнике показано два способа задания точек останова.</span><span class="sxs-lookup"><span data-stu-id="c715e-260">This tutorial only showed you two ways to set breakpoints.</span></span>  <span data-ttu-id="c715e-261">DevTools включает в себя множество других способов, включая следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="c715e-261">DevTools offers many other ways including the following settings.</span></span>  

*   <span data-ttu-id="c715e-262">Условные точки останова, которые запускаются только в случае, если предоставленное условие истинно.</span><span class="sxs-lookup"><span data-stu-id="c715e-262">Conditional breakpoints that are only triggered when the condition that you provide is true.</span></span>  
*   <span data-ttu-id="c715e-263">Точки останова в перехваченных или неперехваченных исключениях.</span><span class="sxs-lookup"><span data-stu-id="c715e-263">Breakpoints on caught or uncaught exceptions.</span></span>  
*   <span data-ttu-id="c715e-264">XHR точки останова, которые инициируются, когда запрашиваемый URL-адрес соответствует подстроке, которую вы задаете.</span><span class="sxs-lookup"><span data-stu-id="c715e-264">XHR breakpoints that are triggered when the requested URL matches a substring that you provide.</span></span>  
    
<span data-ttu-id="c715e-265">Для получения дополнительных сведений о том, когда и как использовать каждый из типов, перейдите к разделу [Остановка кода с точки останова][DevtoolsJavscriptBreakpoints].</span><span class="sxs-lookup"><span data-stu-id="c715e-265">For more information about when and how to use each type, go to [Pause Your Code With Breakpoints][DevtoolsJavscriptBreakpoints].</span></span>  

<span data-ttu-id="c715e-266">В этом учебнике описаны несколько элементов управления пошаговым выполнением кода.</span><span class="sxs-lookup"><span data-stu-id="c715e-266">There are a couple of code stepping controls that were not explained in this tutorial.</span></span>  <span data-ttu-id="c715e-267">Дополнительные сведения можно найти на странице [Шаг с заходом в строке кода][DevtoolsJavascriptReferenceStepThroughCode].</span><span class="sxs-lookup"><span data-stu-id="c715e-267">For more information, go to [Step over line of code][DevtoolsJavascriptReferenceStepThroughCode].</span></span>  

<!--  
 


-->  

<!-- image links -->  

[ImageAddIcon]: ../media/add-expression-icon.msft.png  
[ImageDeactivateIcon]: ../media/deactivate-breakpoints-button-icon.msft.png  
[ImageExpandIcon]: ../media/expand-icon.msft.png  
[ImageIntoIcon]: ../media/step-into-icon.msft.png  
[ImageOverIcon]: ../media/step-over-icon.msft.png  
[ImageResumeIcon]: ../media/resume-script-run-icon.msft.png  

<!-- links -->  

[DevtoolsJavscriptBreakpoints]: ./breakpoints.md "Приостановка кода с точки останова в Microsoft Edge DevTools | Документы Microsoft"
[DevtoolsJavascriptReferenceStepThroughCode]: ./reference.md#step-through-code "Пошаговое руководство по отладке кода-JavaScript | Документы Microsoft"

<!--[inPrivate]: https://support.alphabet.com/alphabet-browser/answer/95464  -->  

[OpenDebugJSDemo]: https://microsoft-edge-chromium-devtools.glitch.me/debug-js/get-started.html "Открыть демонстрацию | Цепь"  

> [!NOTE]
> <span data-ttu-id="c715e-271">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c715e-271">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="c715e-272">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/javascript/index) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="c715e-272">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="c715e-274">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c715e-274">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
