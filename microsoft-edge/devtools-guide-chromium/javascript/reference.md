---
description: Ознакомьтесь с новыми рабочими процессами отладки в этой полной справке функций отладки Microsoft Edge DevTools.
title: Справочник по отладке JavaScript
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: f11dfb52e97dcec20d1e6c4f3adeee7010857a33
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993424"
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

# <span data-ttu-id="ea21f-104">Справочник по febugging JavaScript</span><span class="sxs-lookup"><span data-stu-id="ea21f-104">JavaScript febugging reference</span></span>  

<span data-ttu-id="ea21f-105">Вы узнаете о новых рабочих процессах отладки со следующими полным справочником по функциям отладки Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="ea21f-105">Discover new debugging workflows with the following comprehensive reference of Microsoft Edge DevTools debugging features.</span></span>  

<span data-ttu-id="ea21f-106">Подробнее об отладке можно найти [в статье Начало работы с отладкой JavaScript в Microsoft Edge DevTools][DevToolsJavascriptGetStarted] .</span><span class="sxs-lookup"><span data-stu-id="ea21f-106">See [Get Started With Debugging JavaScript In Microsoft Edge DevTools][DevToolsJavascriptGetStarted] to learn the basics of debugging.</span></span>  

## <span data-ttu-id="ea21f-107">Приостановка кода с точки останова</span><span class="sxs-lookup"><span data-stu-id="ea21f-107">Pause code with breakpoints</span></span>  

<span data-ttu-id="ea21f-108">Установите точку останова, чтобы можно было приостановить выполнение кода в середине среды выполнения.</span><span class="sxs-lookup"><span data-stu-id="ea21f-108">Set a breakpoint so that you are able to pause your code in the middle of the runtime.</span></span>  

<span data-ttu-id="ea21f-109">Сведения о том, как задавать точки останова, можно найти в разделе [приостановка кода с точки останова][DevToolsJavascriptBreakpoints] .</span><span class="sxs-lookup"><span data-stu-id="ea21f-109">See [Pause Your Code With Breakpoints][DevToolsJavascriptBreakpoints] to learn how to set breakpoints.</span></span>  

## <span data-ttu-id="ea21f-110">Пошаговое руководство по коду</span><span class="sxs-lookup"><span data-stu-id="ea21f-110">Step through code</span></span>  

<span data-ttu-id="ea21f-111">Когда код приостанавливается, проведите по одной строке за раз, изменяя поток управления и значения свойств по своему пути.</span><span class="sxs-lookup"><span data-stu-id="ea21f-111">Once your code is paused, step through it, one line at a time, investigating control flow and property values along the way.</span></span>  

### <span data-ttu-id="ea21f-112">Шаг с заходом в строке кода</span><span class="sxs-lookup"><span data-stu-id="ea21f-112">Step over line of code</span></span>  

<span data-ttu-id="ea21f-113">При приостановке в строке кода, содержащей функцию, которая не связана с проблемой, которую вы используете для отладки, нажмите кнопку **шаг за** шагом \ ( ![ Шаг с заходом ][ImageStepOverIcon] в конце), чтобы запустить функцию без пошагового выполнения.</span><span class="sxs-lookup"><span data-stu-id="ea21f-113">When paused on a line of code containing a function that is not relevant to the problem you are debugging, click the **Step over** \(![Step over][ImageStepOverIcon]\) button to run the function without stepping into it.</span></span>  

:::image type="complex" source="../media/javascript-source-page-debugger-step-over-next-function-call.msft.png" alt-text="Нажмите кнопку &quot;шаг за шагом&quot;" lightbox="../media/javascript-source-page-debugger-step-over-next-function-call.msft.png":::
   <span data-ttu-id="ea21f-115">Нажмите кнопку " **шаг за шагом** "</span><span class="sxs-lookup"><span data-stu-id="ea21f-115">Select **Step over**</span></span>  
:::image-end:::  

<span data-ttu-id="ea21f-116">Например, предположим, что выполняется отладка следующего фрагмента кода.</span><span class="sxs-lookup"><span data-stu-id="ea21f-116">For example, suppose you are debugging the following code snippet.</span></span>  

```javascript
function updateHeader() {
    var day = new Date().getDay();
    var name = getName(); // A
    updateName(name); // D
}
function getName() {
    var name = app.first + ' ' + app.last; // B
    return name; // C
}
```  

<span data-ttu-id="ea21f-117">Вы приостанавливаете `A` .</span><span class="sxs-lookup"><span data-stu-id="ea21f-117">You are paused on `A`.</span></span>  <span data-ttu-id="ea21f-118">Нажимая клавишу " **шаг за шагом**", DevTools запускает весь код в функции, для которой выполняется пошаговое выполнение, `B` а именно `C` .</span><span class="sxs-lookup"><span data-stu-id="ea21f-118">By pressing **Step over**, DevTools runs all the code in the function that you are stepping over, which is `B` and `C`.</span></span>  <span data-ttu-id="ea21f-119">Затем DevTools приостанавливает `D` .</span><span class="sxs-lookup"><span data-stu-id="ea21f-119">DevTools then pauses on `D`.</span></span>  

### <span data-ttu-id="ea21f-120">Шаг с заходом в строку кода</span><span class="sxs-lookup"><span data-stu-id="ea21f-120">Step into line of code</span></span>  

<span data-ttu-id="ea21f-121">При приостановке в строке кода, содержащей вызов функции, связанный с проблемой, в которой выполняется отладка, нажмите кнопку **Шаг с заходом** \ (шаг с заходом в начало ![ ), ][ImageStepIntoIcon] чтобы более подробно изучить эту функцию.</span><span class="sxs-lookup"><span data-stu-id="ea21f-121">When paused on a line of code containing a function call that is related to the problem you are debugging, click the **Step into** \(![Step into][ImageStepIntoIcon]\) button to investigate that function further.</span></span>  

:::image type="complex" source="../media/javascript-source-page-debugger-step-into-next-function-call.msft.png" alt-text="Нажмите кнопку &quot;шаг за шагом&quot;" lightbox="../media/javascript-source-page-debugger-step-into-next-function-call.msft.png":::
   <span data-ttu-id="ea21f-123">Нажмите кнопку " **Шаг с заходом** "</span><span class="sxs-lookup"><span data-stu-id="ea21f-123">Select **Step into**</span></span>  
:::image-end:::  

<span data-ttu-id="ea21f-124">Например, предположим, что выполняется отладка следующего фрагмента кода.</span><span class="sxs-lookup"><span data-stu-id="ea21f-124">For example, suppose you are debugging the following code snippet.</span></span>  

```javascript
function updateHeader() {
    var day = new Date().getDay();
    var name = getName(); // A
    updateName(name);
}
function getName() {
    var name = app.first + ' ' + app.last; // B
    return name;
}
```  

<span data-ttu-id="ea21f-125">Вы приостанавливаете `A` .</span><span class="sxs-lookup"><span data-stu-id="ea21f-125">You are paused on `A`.</span></span>  <span data-ttu-id="ea21f-126">Нажимая кнопку " **Шаг с заходом**", DevTools запускает эту строку кода, а затем приостанавливает выполнение `B` .</span><span class="sxs-lookup"><span data-stu-id="ea21f-126">By pressing **Step into**, DevTools runs this line of code, then pauses on `B`.</span></span>  

### <span data-ttu-id="ea21f-127">Пошаговое руководство из строки кода</span><span class="sxs-lookup"><span data-stu-id="ea21f-127">Step out of line of code</span></span>  

<span data-ttu-id="ea21f-128">При приостановке внутри функции, которая не связана с проблемой, которую вы выполняете Отладка, нажмите кнопку **шаг** с выходом \ ( ![ Шаг с выходом ][ImageStepOutIcon] ), чтобы выполнить оставшуюся часть кода функции.</span><span class="sxs-lookup"><span data-stu-id="ea21f-128">When paused inside of a function that is not related to the problem you are debugging, click the **Step out** \(![Step out][ImageStepOutIcon]\) button to run the rest of the code of the function.</span></span>  

:::image type="complex" source="../media/javascript-source-page-debugger-step-out-of-current-function.msft.png" alt-text="Нажмите кнопку &quot;шаг за шагом&quot;" lightbox="../media/javascript-source-page-debugger-step-out-of-current-function.msft.png":::
   <span data-ttu-id="ea21f-130">Нажмите кнопку " **Шаг с выходом** "</span><span class="sxs-lookup"><span data-stu-id="ea21f-130">Select **Step out**</span></span>  
:::image-end:::  

<span data-ttu-id="ea21f-131">Например, предположим, что выполняется отладка следующего фрагмента кода.</span><span class="sxs-lookup"><span data-stu-id="ea21f-131">For example, suppose you are debugging the following code snippet.</span></span>  

```javascript
function updateHeader() {
    var day = new Date().getDay();
    var name = getName();
    updateName(name); // C
}
function getName() {
    var name = app.first + ' ' + app.last; // A
    return name; // B
}
```  

<span data-ttu-id="ea21f-132">Вы приостанавливаете `A` .</span><span class="sxs-lookup"><span data-stu-id="ea21f-132">You are paused on `A`.</span></span>  <span data-ttu-id="ea21f-133">Нажимая кнопку " **Шаг с выходом**", DevTools запускает оставшуюся часть кода в `getName()` `B` этом примере, а затем приостанавливает выполнение `C` .</span><span class="sxs-lookup"><span data-stu-id="ea21f-133">By pressing **Step out**, DevTools runs the rest of the code in `getName()`, which is just `B` in this example, and then pauses on `C`.</span></span>  

### <span data-ttu-id="ea21f-134">Выполнение всего кода до определенной строки</span><span class="sxs-lookup"><span data-stu-id="ea21f-134">Run all code up to a specific line</span></span>  

<span data-ttu-id="ea21f-135">При отладке длительных функций может возникнуть большой объем кода, не относящегося к той проблеме, которую вы размещаете в отладке.</span><span class="sxs-lookup"><span data-stu-id="ea21f-135">When debugging a long function, there may be a lot of code that is not related to the problem you are debugging.</span></span>  

<span data-ttu-id="ea21f-136">Вы можете пошагово пройти все строки, но это утомительно.</span><span class="sxs-lookup"><span data-stu-id="ea21f-136">You may choose to step through all the lines, but that is tedious.</span></span>  <span data-ttu-id="ea21f-137">Вы можете указать точку останова для строки кода в строке, в которой вы заинтересованы, и нажать кнопку **возобновить выполнение сценария** \ ( ![ возобновить выполнение скрипта ][ImageResumeScriptExecutionIcon] \), но это происходит быстрее.</span><span class="sxs-lookup"><span data-stu-id="ea21f-137">You may choose to set a line-of-code breakpoint on the line in which you are interested and then click the **Resume Script Execution** \(![Resume Script Execution][ImageResumeScriptExecutionIcon]\) button, but there is a faster way.</span></span>  

<span data-ttu-id="ea21f-138">Щелкните правой кнопкой мыши строку кода, в которой вы хотите заинтересовать, и выберите команду **продолжить**.</span><span class="sxs-lookup"><span data-stu-id="ea21f-138">Right-click the line of code in which you are interested, and select **Continue to here**.</span></span>  <span data-ttu-id="ea21f-139">DevTools запускает весь код до этого момента, а затем приостанавливает выполнение на этой линии.</span><span class="sxs-lookup"><span data-stu-id="ea21f-139">DevTools runs all of the code up to that point, and then pauses on that line.</span></span>  

:::image type="complex" source="../media/javascript-source-page-continue-to-here.msft.png" alt-text="Нажмите кнопку &quot;шаг за шагом&quot;" lightbox="../media/javascript-source-page-continue-to-here.msft.png":::
   <span data-ttu-id="ea21f-141">Нажмите кнопку **"перейти сюда"**</span><span class="sxs-lookup"><span data-stu-id="ea21f-141">Select **Continue to here**</span></span>  
:::image-end:::  

### <span data-ttu-id="ea21f-142">Перезапустить функцию TOP в стеке вызовов</span><span class="sxs-lookup"><span data-stu-id="ea21f-142">Restart the top function of the call stack</span></span>  

<span data-ttu-id="ea21f-143">Наведя указатель на строку кода, щелкните правой кнопкой мыши в любом месте области **стека звонков** и выберите команду **перезапустить кадр** , чтобы приостановить работу на первой строке функции Top в стеке вызовов.</span><span class="sxs-lookup"><span data-stu-id="ea21f-143">While paused on a line of code, right-click anywhere in the **Call Stack** pane and select **Restart Frame** to pause on the first line of the top function in your call stack.</span></span>  <span data-ttu-id="ea21f-144">Функция Top — это последняя выполненная функция.</span><span class="sxs-lookup"><span data-stu-id="ea21f-144">The top function is the last function that was run.</span></span>  

<span data-ttu-id="ea21f-145">В приведенном ниже фрагменте кода показан пример с пошаговыми операциями.</span><span class="sxs-lookup"><span data-stu-id="ea21f-145">The following code snippet is an example for you to step-through.</span></span>  

```javascript
function factorial(n) {
    var product = 0; // B
    for (var i = 1; i <= n; i++) {
      product += i;
    }
    return product; // A
}
```  

<span data-ttu-id="ea21f-146">Вы приостанавливаете `A` .</span><span class="sxs-lookup"><span data-stu-id="ea21f-146">You are paused on `A`.</span></span>  <span data-ttu-id="ea21f-147">После нажатия кнопки **перезапустить**вы должны быть приостановлены `B` , пока не задана точка останова или нажата клавиша **возобновления выполнения сценария**.</span><span class="sxs-lookup"><span data-stu-id="ea21f-147">After clicking **Restart Frame**, you should be paused on `B`, without ever setting a breakpoint or pressing **Resume script execution**.</span></span>  

:::image type="complex" source="../media/javascript-source-page-debugger-restart-frame.msft.png" alt-text="Нажмите кнопку &quot;шаг за шагом&quot;" lightbox="../media/javascript-source-page-debugger-restart-frame.msft.png":::
   <span data-ttu-id="ea21f-149">Нажмите кнопку " **перезапустить рамку** "</span><span class="sxs-lookup"><span data-stu-id="ea21f-149">Select **Restart Frame**</span></span>  
:::image-end:::  

### <span data-ttu-id="ea21f-150">Среда выполнения сценария возобновления</span><span class="sxs-lookup"><span data-stu-id="ea21f-150">Resume script runtime</span></span>  

<span data-ttu-id="ea21f-151">Чтобы продолжить выполнение после паузы в сценарии, нажмите кнопку **возобновить исполнение сценария** \ ( ![ возобновить выполнение сценария \ ][ImageResumeScriptExecutionIcon] ).</span><span class="sxs-lookup"><span data-stu-id="ea21f-151">To continue the runtime after a pause of your script, click the **Resume Script Execution** \(![Resume Script Execution][ImageResumeScriptExecutionIcon]\) button.</span></span>  <span data-ttu-id="ea21f-152">DevTools запускает сценарий до следующей точки останова (при наличии).</span><span class="sxs-lookup"><span data-stu-id="ea21f-152">DevTools runs the script up until the next breakpoint, if any.</span></span>  

:::image type="complex" source="../media/javascript-sources-get-started-js-resume-script-runtime.msft.png" alt-text="Нажмите кнопку &quot;шаг за шагом&quot;" lightbox="../media/javascript-sources-get-started-js-resume-script-runtime.msft.png":::
   <span data-ttu-id="ea21f-154">Выбор **выполнения сценария возобновления**</span><span class="sxs-lookup"><span data-stu-id="ea21f-154">Select **Resume script execution**</span></span>  
:::image-end:::  

#### <span data-ttu-id="ea21f-155">Выполнение принудительного выполнения сценария</span><span class="sxs-lookup"><span data-stu-id="ea21f-155">Force script runtime</span></span>  

<span data-ttu-id="ea21f-156">Чтобы пропустить все точки останова и принудительно возобновить выполнение сценария, нажмите и удерживайте кнопку запустить выполнение **сценария** \ ( ![ возобновить выполнение скрипта \ ][ImageResumeScriptExecutionIcon] ) и выберите команду **принудительное** выполнение сценария \ ( ![ принудительное выполнение сценария \ ][ImageForceScriptExecutionIcon] ).</span><span class="sxs-lookup"><span data-stu-id="ea21f-156">To ignore all breakpoints and force your script to resume running, click and hold the **Resume Script Execution** \(![Resume Script Execution][ImageResumeScriptExecutionIcon]\) button and then select the **Force script execution** \(![Force script execution][ImageForceScriptExecutionIcon]\) button.</span></span>  

:::image type="complex" source="../media/javascript-sources-get-started-js-force-script-runtime.msft.png" alt-text="Нажмите кнопку &quot;шаг за шагом&quot;" lightbox="../media/javascript-sources-get-started-js-force-script-runtime.msft.png":::
   <span data-ttu-id="ea21f-158">Выберите **принудительное выполнение сценария**</span><span class="sxs-lookup"><span data-stu-id="ea21f-158">Select **Force script execution**</span></span>  
:::image-end:::  

### <span data-ttu-id="ea21f-159">Изменить контекст потока</span><span class="sxs-lookup"><span data-stu-id="ea21f-159">Change thread context</span></span>  

<span data-ttu-id="ea21f-160">При работе с веб-сотрудниками или сотрудниками служб щелкните контекст, указанный в области **потоки** , чтобы переключиться на этот контекст.</span><span class="sxs-lookup"><span data-stu-id="ea21f-160">When working with web workers or service workers, click on a context listed in the **Threads** pane to switch to that context.</span></span>  <span data-ttu-id="ea21f-161">Синий значок стрелки соответствует контексту, выбранному в данный момент.</span><span class="sxs-lookup"><span data-stu-id="ea21f-161">The blue arrow icon represents which context is currently selected.</span></span>  

:::image type="complex" source="../media/javascript-sources-main-min-js-threads.msft.png" alt-text="Нажмите кнопку &quot;шаг за шагом&quot;" lightbox="../media/javascript-sources-main-min-js-threads.msft.png":::
   <span data-ttu-id="ea21f-163">Область « **потоки** »</span><span class="sxs-lookup"><span data-stu-id="ea21f-163">The **Threads** pane</span></span>  
:::image-end:::  

<span data-ttu-id="ea21f-164">Например, предположим, что вы придерживаетесь точки останова как в основном, так и на рабочем скрипте службы.</span><span class="sxs-lookup"><span data-stu-id="ea21f-164">For example, suppose that you are paused on a breakpoint in both your main script and your service worker script.</span></span>  <span data-ttu-id="ea21f-165">Вы хотите просмотреть локальные и глобальные свойства для контекста рабочего процесса службы, но на панели **источники** отображается контекст основного сценария.</span><span class="sxs-lookup"><span data-stu-id="ea21f-165">You want to view the local and global properties for the service worker context, but the **Sources** panel is showing the main script context.</span></span>  <span data-ttu-id="ea21f-166">Нажимая кнопку "сервисный рабочий процесс" на панели " **потоки** ", вы сможете перейти в этот контекст.</span><span class="sxs-lookup"><span data-stu-id="ea21f-166">By clicking on the service worker entry in the **Threads** pane, you should be able to switch to that context.</span></span>  

## <span data-ttu-id="ea21f-167">Просмотр и изменение локальных, закрытых и глобальных свойств</span><span class="sxs-lookup"><span data-stu-id="ea21f-167">View and edit local, closure, and global properties</span></span>  

<span data-ttu-id="ea21f-168">При приостановке в строке кода используйте область **область** для просмотра и изменения значений свойств и переменных в локальных, закрытых и глобальных областях.</span><span class="sxs-lookup"><span data-stu-id="ea21f-168">While paused on a line of code, use the **Scope** pane to view and edit the values of properties and variables in the local, closure, and global scopes.</span></span>  

*   <span data-ttu-id="ea21f-169">Дважды щелкните значение свойства, чтобы изменить его.</span><span class="sxs-lookup"><span data-stu-id="ea21f-169">Double-click a property value to change it.</span></span>  
*   <span data-ttu-id="ea21f-170">Неперечислимые свойства затенены.</span><span class="sxs-lookup"><span data-stu-id="ea21f-170">Non-enumerable properties are greyed out.</span></span>  

:::image type="complex" source="../media/javascript-sources-get-started-js-scope.msft.png" alt-text="Нажмите кнопку &quot;шаг за шагом&quot;" lightbox="../media/javascript-sources-get-started-js-scope.msft.png":::
   <span data-ttu-id="ea21f-172">Область " **область** "</span><span class="sxs-lookup"><span data-stu-id="ea21f-172">The **Scope** pane</span></span>  
:::image-end:::  

## <span data-ttu-id="ea21f-173">Просмотр текущего стека вызовов</span><span class="sxs-lookup"><span data-stu-id="ea21f-173">View the current call stack</span></span>  

<span data-ttu-id="ea21f-174">При приостановке на строке кода используйте область **Стек вызовов** для просмотра стека вызовов, в котором вы набрались этим моментом.</span><span class="sxs-lookup"><span data-stu-id="ea21f-174">While paused on a line of code, use the **Call Stack** pane to view the call stack that got you to this point.</span></span>  

<!--If you are working with async code, check the **Async** checkbox to enable async call stacks.  -->  

<span data-ttu-id="ea21f-175">Щелкните запись, чтобы перейти к строке кода, в которой была вызвана эта функция.</span><span class="sxs-lookup"><span data-stu-id="ea21f-175">Click on an entry to jump to the line of code where that function was called.</span></span>  <span data-ttu-id="ea21f-176">Синий значок стрелки показывает, какая функция DevTools выделяется в данный момент.</span><span class="sxs-lookup"><span data-stu-id="ea21f-176">The blue arrow icon represents which function DevTools is currently highlighting.</span></span>  

:::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty.msft.png" alt-text="Нажмите кнопку &quot;шаг за шагом&quot;" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty.msft.png":::
   <span data-ttu-id="ea21f-178">Область « **Стек вызовов** »</span><span class="sxs-lookup"><span data-stu-id="ea21f-178">The **Call Stack** pane</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="ea21f-179">Если в строке кода не присвоена значение, область **стека вызовов** пуста.</span><span class="sxs-lookup"><span data-stu-id="ea21f-179">When not paused on a line of code, the **Call Stack** pane is empty.</span></span>  

### <span data-ttu-id="ea21f-180">Копирование трассировки стека</span><span class="sxs-lookup"><span data-stu-id="ea21f-180">Copy stack trace</span></span>  

<!--
This should be moved to an "Export debug data" H2 section when there is enough content for that, but there is not right now, so it is here.
-->

<span data-ttu-id="ea21f-181">Щелкните правой кнопкой мыши в любом месте области **стека звонков** и выберите команду **Копировать трассировку стека** , чтобы скопировать текущий стек вызовов в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="ea21f-181">Right-click anywhere in the **Call Stack** pane and select **Copy stack trace** to copy the current call stack to the clipboard.</span></span>  

:::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-copy-stack-trace.msft.png" alt-text="Нажмите кнопку &quot;шаг за шагом&quot;" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-copy-stack-trace.msft.png":::
   <span data-ttu-id="ea21f-183">Нажмите кнопку **Копировать трассировку стека** .</span><span class="sxs-lookup"><span data-stu-id="ea21f-183">Select **Copy Stack Trace**</span></span>  
:::image-end:::  

<span data-ttu-id="ea21f-184">В приведенном ниже фрагменте кода показан пример выходных данных.</span><span class="sxs-lookup"><span data-stu-id="ea21f-184">The following code snippet is an example of the output.</span></span>  

```javascript
getNumber1 (get-started.js:35)
inputsAreEmpty (get-started.js:22)
onClick (get-started.js:15)
```  

## <span data-ttu-id="ea21f-185">Игнорировать сценарий или шаблон сценариев</span><span class="sxs-lookup"><span data-stu-id="ea21f-185">Ignore a script or pattern of scripts</span></span>  

<span data-ttu-id="ea21f-186">Помечайте сценарий как код библиотеки, если вы хотите пропустить этот сценарий во время отладки.</span><span class="sxs-lookup"><span data-stu-id="ea21f-186">Mark a script as Library code when you want to ignore that script while debugging.</span></span>  <span data-ttu-id="ea21f-187">При пометке в виде кода библиотеки сценарий скрывается в области **стека вызовов** , и вы никогда не просматриваете функции сценария при пошаговом выполнении кода.</span><span class="sxs-lookup"><span data-stu-id="ea21f-187">When marked as Library code, a script is obscured in the **Call Stack** pane, and you never step into the functions of the script when you step through your code.</span></span>  

<span data-ttu-id="ea21f-188">В приведенном ниже фрагменте кода показан пример с пошаговыми операциями.</span><span class="sxs-lookup"><span data-stu-id="ea21f-188">The following code snippet is an example for you to step-through.</span></span>  

```javascript
function animate() {
    prepare();
    lib.doFancyStuff(); // A
    render();
}
```  

`A` <span data-ttu-id="ea21f-189">— это библиотека стороннего поставщика, которой вы доверяете.</span><span class="sxs-lookup"><span data-stu-id="ea21f-189">is a third-party library that you trust.</span></span>  <span data-ttu-id="ea21f-190">Если вы уверены, что проблема, выполняемая при отладке, не связана с библиотекой стороннего поставщика, имеет смысл помечать сценарий как **код библиотеки**.</span><span class="sxs-lookup"><span data-stu-id="ea21f-190">If you are confident that the problem you are debugging is not related to the third-party library, then it makes sense to mark the script as **Library code**.</span></span>  

### <span data-ttu-id="ea21f-191">Пометка сценария как кода библиотеки в области "редактор"</span><span class="sxs-lookup"><span data-stu-id="ea21f-191">Mark a script as Library code from the Editor pane</span></span>  

<span data-ttu-id="ea21f-192">Выполните указанные ниже действия, чтобы помечать сценарий как **код библиотеки** на панели **редактора** .</span><span class="sxs-lookup"><span data-stu-id="ea21f-192">Complete the following actions to mark a script as **Library code** from the **Editor** pane.</span></span>  

1.  <span data-ttu-id="ea21f-193">Откройте файл.</span><span class="sxs-lookup"><span data-stu-id="ea21f-193">Open the file.</span></span>  
1.  <span data-ttu-id="ea21f-194">Щелкните правой кнопкой мыши в любом месте.</span><span class="sxs-lookup"><span data-stu-id="ea21f-194">Right-click anywhere.</span></span>  
1.  <span data-ttu-id="ea21f-195">Нажмите кнопку **помечать как код библиотеки**.</span><span class="sxs-lookup"><span data-stu-id="ea21f-195">Select **Mark as Library code**.</span></span>  
    
    :::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-editor-mark-as-library-code.msft.png" alt-text="Нажмите кнопку &quot;шаг за шагом&quot;" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-editor-mark-as-library-code.msft.png":::
       <span data-ttu-id="ea21f-197">Пометка сценария как **кода библиотеки** в области " **Редактор** "</span><span class="sxs-lookup"><span data-stu-id="ea21f-197">Mark a script as **Library code** from the **Editor** pane</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="ea21f-198">Пометка сценария как кода библиотеки на панели «стек вызовов»</span><span class="sxs-lookup"><span data-stu-id="ea21f-198">Mark a script as Library code from the Call Stack pane</span></span>  

<span data-ttu-id="ea21f-199">Compelte действия folliwng, чтобы помечать сценарий как **код библиотеки** из области " **Стек вызовов** ".</span><span class="sxs-lookup"><span data-stu-id="ea21f-199">Compelte the folliwng actions to mark a script as **Library code** from the **Call Stack** pane.</span></span>  

1.  <span data-ttu-id="ea21f-200">Щелкните правой кнопкой мыши функцию в сценарии.</span><span class="sxs-lookup"><span data-stu-id="ea21f-200">Right-click on a function from the script.</span></span>  
1.  <span data-ttu-id="ea21f-201">Нажмите кнопку **помечать как код библиотеки**.</span><span class="sxs-lookup"><span data-stu-id="ea21f-201">Select **Mark as Library code**.</span></span>  
    
    :::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-call-stack-mark-as-library-code.msft.png" alt-text="Нажмите кнопку &quot;шаг за шагом&quot;" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-call-stack-mark-as-library-code.msft.png":::
       <span data-ttu-id="ea21f-203">Пометка сценария как **кода библиотеки** на панели « **Стек вызовов** »</span><span class="sxs-lookup"><span data-stu-id="ea21f-203">Mark a script as **Library code** from the **Call Stack** pane</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="ea21f-204">Пометка сценария как кода библиотеки из параметров</span><span class="sxs-lookup"><span data-stu-id="ea21f-204">Mark a script as Library code from Settings</span></span>  

<span data-ttu-id="ea21f-205">Выполните указанные ниже действия, чтобы помечать один сценарий или шаблон сценариев из **параметров**.</span><span class="sxs-lookup"><span data-stu-id="ea21f-205">Complete the following actions to mark a single script or pattern of scripts from **Settings**.</span></span>  

1.  <span data-ttu-id="ea21f-206">Откройте [Параметры][DevToolsCustomize].</span><span class="sxs-lookup"><span data-stu-id="ea21f-206">Open [Settings][DevToolsCustomize].</span></span>  
1.  <span data-ttu-id="ea21f-207">Перейдите на вкладку **код библиотеки** .</span><span class="sxs-lookup"><span data-stu-id="ea21f-207">Go to the **Library code** tab.</span></span>  
1.  <span data-ttu-id="ea21f-208">Нажмите кнопку **Добавить узор**.</span><span class="sxs-lookup"><span data-stu-id="ea21f-208">Click **Add pattern**.</span></span>  
1.  <span data-ttu-id="ea21f-209">Введите имя сценария или шаблон регулярного выражения для имен сценариев, чтобы помечать его как **код библиотеки**.</span><span class="sxs-lookup"><span data-stu-id="ea21f-209">Enter the script name or a regex pattern of script names to mark as **Library code**.</span></span>  
1.  <span data-ttu-id="ea21f-210">Щелкните **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="ea21f-210">Click **Add**.</span></span>  
    
    :::image type="complex" source="../media/javascript-framework-library-code.msft.png" alt-text="Нажмите кнопку &quot;шаг за шагом&quot;" lightbox="../media/javascript-framework-library-code.msft.png":::
       <span data-ttu-id="ea21f-212">Пометка сценария как **кода библиотеки** из **параметров**</span><span class="sxs-lookup"><span data-stu-id="ea21f-212">Mark a script as **Library code** from **Settings**</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="ea21f-213">Выполнение фрагментов кода отладки на любой странице</span><span class="sxs-lookup"><span data-stu-id="ea21f-213">Run snippets of debug code from any page</span></span>   

<span data-ttu-id="ea21f-214">Если вы обнаружите, что вы используете один и тот же код отладки в консоли, рассматривайте фрагменты кода.</span><span class="sxs-lookup"><span data-stu-id="ea21f-214">If you find yourself running the same debug code in the Console over and over, consider Snippets.</span></span>  <span data-ttu-id="ea21f-215">Фрагменты — это сценарии среды выполнения, созданные, сохраняемые и выполняемые в DevTools.</span><span class="sxs-lookup"><span data-stu-id="ea21f-215">Snippets are runtime scripts that you author, store, and run within DevTools.</span></span>  

<span data-ttu-id="ea21f-216">Дополнительные сведения можно найти в разделе [выполнение фрагментов кода на любой странице][DevToolsJavascriptSnippets] .</span><span class="sxs-lookup"><span data-stu-id="ea21f-216">See [Run Snippets of Code From Any Page][DevToolsJavascriptSnippets] to learn more.</span></span>  

## <span data-ttu-id="ea21f-217">Просмотр значений настраиваемых выражений JavaScript</span><span class="sxs-lookup"><span data-stu-id="ea21f-217">Watch the values of custom JavaScript expressions</span></span>  

<span data-ttu-id="ea21f-218">Используйте область **контрольных** значений для просмотра значений настраиваемых выражений.</span><span class="sxs-lookup"><span data-stu-id="ea21f-218">Use the **Watch** pane to watch the values of custom expressions.</span></span>  <span data-ttu-id="ea21f-219">Вы можете просмотреть любое допустимое выражение JavaScript.</span><span class="sxs-lookup"><span data-stu-id="ea21f-219">You may watch any valid JavaScript expression.</span></span>  

:::image type="complex" source="../media/javascript-sources-get-started-js-watch.msft.png" alt-text="Нажмите кнопку &quot;шаг за шагом&quot;" lightbox="../media/javascript-sources-get-started-js-watch.msft.png":::
   <span data-ttu-id="ea21f-221">Область **контрольных значений**</span><span class="sxs-lookup"><span data-stu-id="ea21f-221">The **Watch** pane</span></span>  
:::image-end:::  

*   <span data-ttu-id="ea21f-222">Нажмите кнопку **Добавить выражение** \ ( ![ Добавить выражение ][ImageAddExpressionIcon] \), чтобы создать новое выражение контрольного значения.</span><span class="sxs-lookup"><span data-stu-id="ea21f-222">Click the **Add Expression** \(![Add Expression][ImageAddExpressionIcon]\) button to create a new watch expression.</span></span>  
*   <span data-ttu-id="ea21f-223">Нажмите кнопку " **Обновить** \ ![ " (обновить ][ImageRefreshIcon] ), чтобы обновить значения всех существующих выражений.</span><span class="sxs-lookup"><span data-stu-id="ea21f-223">Click the **Refresh** \(![Refresh][ImageRefreshIcon]\) button to refresh the values of all existing expressions.</span></span>  <span data-ttu-id="ea21f-224">Значения автоматически обновляются при пошаговом выполнении кода.</span><span class="sxs-lookup"><span data-stu-id="ea21f-224">Values automatically refresh while stepping through code.</span></span>  
*   <span data-ttu-id="ea21f-225">Наведите указатель мыши на выражение и нажмите кнопку **удалить выражение** \ ( ![ удалить выражение ][ImageDeleteExpressionIcon] \), чтобы удалить его.</span><span class="sxs-lookup"><span data-stu-id="ea21f-225">Hover over an expression and click the **Delete Expression** \(![Delete Expression][ImageDeleteExpressionIcon]\) button to delete it.</span></span>  

## <span data-ttu-id="ea21f-226">Создание читаемого файла minified</span><span class="sxs-lookup"><span data-stu-id="ea21f-226">Make a minified file readable</span></span>  

<span data-ttu-id="ea21f-227">Нажмите кнопку **Формат** \ ( ![ Формат ][ImageFormatIcon] \), чтобы сделать файл minified удобным для восприятия.</span><span class="sxs-lookup"><span data-stu-id="ea21f-227">Click the **Format** \(![Format][ImageFormatIcon]\) button to make a minified file human-readable.</span></span>  

:::image type="complex" source="../media/javascript-sources-html-non-minified.msft.png" alt-text="Нажмите кнопку &quot;шаг за шагом&quot;" lightbox="../media/javascript-sources-html-non-minified.msft.png":::
   <span data-ttu-id="ea21f-229">Кнопка " **Формат** "</span><span class="sxs-lookup"><span data-stu-id="ea21f-229">The **Format** button</span></span>  
:::image-end:::  

## <span data-ttu-id="ea21f-230">Изменение сценария</span><span class="sxs-lookup"><span data-stu-id="ea21f-230">Edit a script</span></span>   

<span data-ttu-id="ea21f-231">При исправлении ошибки часто требуется протестировать некоторые изменения в коде JavaScript.</span><span class="sxs-lookup"><span data-stu-id="ea21f-231">When fixing a bug, you often want to test out some changes to your JavaScript code.</span></span>  <span data-ttu-id="ea21f-232">Вам не нужно вносить изменения в внешний редактор или интегрированную среду разработки и повторно загрузить страницу.</span><span class="sxs-lookup"><span data-stu-id="ea21f-232">You do not need to make the changes in an external editor or IDE and then reload the page.</span></span>  <span data-ttu-id="ea21f-233">Вы можете редактировать сценарий в DevTools.</span><span class="sxs-lookup"><span data-stu-id="ea21f-233">You may edit your script in DevTools.</span></span>  

<span data-ttu-id="ea21f-234">Чтобы изменить сценарий, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="ea21f-234">Complete the following actions to edit a script.</span></span>  

1.  <span data-ttu-id="ea21f-235">Откройте файл в области " **Редактор** " на панели " **источники** ".</span><span class="sxs-lookup"><span data-stu-id="ea21f-235">Open the file in the **Editor** pane of the **Sources** panel.</span></span>  
1.  <span data-ttu-id="ea21f-236">Внесите изменения в область " **Редактор** ".</span><span class="sxs-lookup"><span data-stu-id="ea21f-236">Make your changes in the **Editor** pane.</span></span>  
1.  <span data-ttu-id="ea21f-237">Чтобы сохранить, нажмите клавиши `Ctrl` + `S` \ (Windows \) или `Command` + `S` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="ea21f-237">Press `Ctrl`+`S` \(Windows\) or `Command`+`S` \(macOS\) to save.</span></span>  <span data-ttu-id="ea21f-238">DevTools заменяет весь JS – файл в механизме JavaScript Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ea21f-238">DevTools patches the entire JS file into the JavaScript engine of Microsoft Edge.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-html-minified.msft.png" alt-text="Нажмите кнопку &quot;шаг за шагом&quot;" lightbox="../media/javascript-sources-html-minified.msft.png":::
       <span data-ttu-id="ea21f-240">Область " **Редактор** "</span><span class="sxs-lookup"><span data-stu-id="ea21f-240">The **Editor** pane</span></span>  
    :::image-end:::  
     
## <span data-ttu-id="ea21f-241">Отключение JavaScript</span><span class="sxs-lookup"><span data-stu-id="ea21f-241">Disable JavaScript</span></span>   

<span data-ttu-id="ea21f-242">[В разделе Отключение JavaScript с Microsoft Edge DevTools][DevToolsJavascriptDisable].</span><span class="sxs-lookup"><span data-stu-id="ea21f-242">See [Disable JavaScript with Microsoft Edge DevTools][DevToolsJavascriptDisable].</span></span>  

## <span data-ttu-id="ea21f-243">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ea21f-243">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageStepOverIcon]: ../media/step-over-icon.msft.png  
[ImageStepIntoIcon]: ../media/step-into-icon.msft.png  
[ImageStepOutIcon]: ../media/step-out-icon.msft.png  
[ImageResumeScriptExecutionIcon]: ../media/resume-script-run-icon.msft.png  
[ImageForceScriptExecutionIcon]: ../media/force-script-run-icon.msft.png  
[ImageAddExpressionIcon]: ../media/add-expression-icon.msft.png  
[ImageRefreshIcon]: ../media/refresh-icon.msft.png  
[ImageDeleteExpressionIcon]: ../media/delete-expression-icon.msft.png  
[ImageFormatIcon]: ../media/format-icon.msft.png  

<!-- links -->  

[DevToolsJavascriptBreakpoints]: ./breakpoints.md "Приостановка кода с точки останова в Microsoft Edge DevTools | Документы Microsoft"  
[DevToolsJavascriptDisable]: ./disable.md "Отключение JavaScript в Microsoft Edge DevTools | Документы Microsoft"  
[DevToolsJavascriptGetStarted]: ./index.md "Начало работы с отладкой JavaScript в Microsoft Edge DevTools | Документы Microsoft"  
[DevToolsJavascriptSnippets]: ./snippets.md "Выполнение фрагментов кода JavaScript на любой странице с Microsoft Edge DevTools | Документы Microsoft"  
[DevToolsCustomize]: ../customize/index.md "Настройка Microsoft Edge DevTools | Документы Microsoft"  

> [!NOTE]
> <span data-ttu-id="ea21f-249">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ea21f-249">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="ea21f-250">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/javascript/reference) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="ea21f-250">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="ea21f-252">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ea21f-252">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
