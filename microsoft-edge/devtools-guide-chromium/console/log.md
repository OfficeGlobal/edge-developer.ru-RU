---
description: Сведения о том, как записывать сообщения на консоль.
title: Начало работы с сообщениями журнала на консоли
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 96e3ad76fb86e32cf58abe6187fa0d6e75a2c00a
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125274"
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

# <span data-ttu-id="e72df-104">Начало работы с сообщениями журнала на консоли</span><span class="sxs-lookup"><span data-stu-id="e72df-104">Get Started With Logging Messages In The Console</span></span>  

<span data-ttu-id="e72df-105">В этом интерактивном учебнике показано, как записывать и фильтровать сообщения на консоли [Microsoft Edge DevTools][MicrosoftEdgeDevTools] .</span><span class="sxs-lookup"><span data-stu-id="e72df-105">This interactive tutorial shows you how to log and filter messages in the [Microsoft Edge DevTools][MicrosoftEdgeDevTools] console.</span></span>  

:::image type="complex" source="../media/console-ars-technica-console-onload.msft.png" alt-text="Сообщения на консоли" lightbox="../media/console-ars-technica-console-onload.msft.png":::
   <span data-ttu-id="e72df-107">Сообщения на **консоли**</span><span class="sxs-lookup"><span data-stu-id="e72df-107">Messages in the **Console**</span></span>  
:::image-end:::  

<span data-ttu-id="e72df-108">Этот учебник предназначен для выполнения в нужном порядке.</span><span class="sxs-lookup"><span data-stu-id="e72df-108">This tutorial is intended to be completed in order.</span></span>  <span data-ttu-id="e72df-109">Предполагается, что вы знакомы с основами веб-разработки, например с помощью JavaScript для добавления интерактивности на страницу.</span><span class="sxs-lookup"><span data-stu-id="e72df-109">It assumes that you understand the fundamentals of web development, such as how to use JavaScript to add interactivity to a page.</span></span>  

## <span data-ttu-id="e72df-110">Настройка ролика и DevTools</span><span class="sxs-lookup"><span data-stu-id="e72df-110">Set up the demo and DevTools</span></span>  

<span data-ttu-id="e72df-111">Этот учебник разработан таким образом, чтобы вы могли открыть демонстрацию и попробовать все рабочие процессы самостоятельно.</span><span class="sxs-lookup"><span data-stu-id="e72df-111">This tutorial is designed so that you are able to open up the demo and try all the workflows yourself.</span></span>  <span data-ttu-id="e72df-112">После того как вы будете физически подписаться на нее, вы, наверное, захотите запомнить рабочие процессы позже.</span><span class="sxs-lookup"><span data-stu-id="e72df-112">When you physically follow along, you are more likely to remember the workflows later.</span></span>  

1.  <span data-ttu-id="e72df-113">Удерживайте клавишу `Control` \ (Windows, Linux \) или `Command` \ (macOS \) и выберите **примеры журнала консоли** , которые нужно открыть на новой вкладке.</span><span class="sxs-lookup"><span data-stu-id="e72df-113">Hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and choose **Console Log Examples** to open in a new tab.</span></span>  
    
    [<span data-ttu-id="e72df-114">Примеры журнала консоли</span><span class="sxs-lookup"><span data-stu-id="e72df-114">Console Log Examples</span></span>][GlitchDevToolsConsoleLogExamples]
    
    <!--
    > [!TIP]
    > Move the demo to a separate window.  
    > 
    > :::image type="complex" source="../media/log-set-up-1.msft.png" alt-text="Сообщения на консоли" lightbox="../media/log-set-up-1.msft.png":::
    >    The tutorial on the left, and the demo on the right  
    > :::image-end:::  
    -->
    
1.  <span data-ttu-id="e72df-115">Чтобы открыть DevTools, сосредоточьте демонстрацию и выберите `Control` + `Shift` + `J` \ (Windows, Linux \) или `Command` + `Option` + `J` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="e72df-115">Focus the demo and then select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\) to open DevTools.</span></span>  <span data-ttu-id="e72df-116">По умолчанию DevTools открывается справа от демонстрации.</span><span class="sxs-lookup"><span data-stu-id="e72df-116">By default DevTools opens to the right of the demo.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/console-example-devtools-right-console.msft.png" alt-text="Сообщения на консоли" lightbox="../media/console-example-devtools-right-console.msft.png":::
             <span data-ttu-id="e72df-118">DevTools открывается справа от демонстрации</span><span class="sxs-lookup"><span data-stu-id="e72df-118">DevTools opens to the right of the demo</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          > [!TIP]
          > <span data-ttu-id="e72df-119">[Закрепите DevTools в нижней части окна][DevToolsCustomizePlacement].</span><span class="sxs-lookup"><span data-stu-id="e72df-119">[Dock DevTools to the bottom of the window][DevToolsCustomizePlacement].</span></span>  
          
          :::image type="complex" source="../media/console-example-devtools-bottom-console.msft.png" alt-text="Сообщения на консоли" lightbox="../media/console-example-devtools-bottom-console.msft.png":::
             <span data-ttu-id="e72df-121">DevTools закреплено в нижней части демонстрации</span><span class="sxs-lookup"><span data-stu-id="e72df-121">DevTools docked to the bottom of the demo</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    :::row:::
       :::column span="":::
          > [!TIP]
          > <span data-ttu-id="e72df-122">[Открепите DevTools в отдельном окне][DevToolsCustomizePlacement].</span><span class="sxs-lookup"><span data-stu-id="e72df-122">[Undock DevTools into a separate window][DevToolsCustomizePlacement].</span></span>  
          
          :::image type="complex" source="../media/console-example-devtools-separate-console-browse.msft.png" alt-text="Сообщения на консоли" lightbox="../media/console-example-devtools-separate-console-browse.msft.png":::
             <span data-ttu-id="e72df-124">Браузер в отдельном окне</span><span class="sxs-lookup"><span data-stu-id="e72df-124">Browser in a separate window</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          > [!TIP]
          > <span data-ttu-id="e72df-125">[Открепите DevTools в отдельном окне][DevToolsCustomizePlacement].</span><span class="sxs-lookup"><span data-stu-id="e72df-125">[Undock DevTools into a separate window][DevToolsCustomizePlacement].</span></span>  
          
          :::image type="complex" source="../media/console-example-devtools-separate-console-devtools.msft.png" alt-text="Сообщения на консоли" lightbox="../media/console-example-devtools-separate-console-devtools.msft.png":::
             <span data-ttu-id="e72df-127">DevTools отсоединяется в отдельном окне</span><span class="sxs-lookup"><span data-stu-id="e72df-127">DevTools undocked in a separate window</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
## <span data-ttu-id="e72df-128">Просмотр сообщений, записанных из JavaScript</span><span class="sxs-lookup"><span data-stu-id="e72df-128">View messages logged from JavaScript</span></span>  

<span data-ttu-id="e72df-129">Большинство сообщений, которые вы видите на консоли, поступают от веб-разработчиков, которые написали JavaScript страницы.</span><span class="sxs-lookup"><span data-stu-id="e72df-129">Most messages that you see in the Console come from the web developers who wrote the JavaScript of the page.</span></span>  <span data-ttu-id="e72df-130">Цель этого раздела — рассказать вам о различных типах сообщений, которые вы, вероятно, видите на консоли, и объясните, как можно вести журнал для каждого типа сообщений.</span><span class="sxs-lookup"><span data-stu-id="e72df-130">The goal of this section is to introduce you to the different message types that you are likely to see in the Console, and explain how you may log each message type yourself from your own JavaScript.</span></span>  

1.  <span data-ttu-id="e72df-131">Нажмите кнопку " **сведения о журнале** " в демонстрационной версии.</span><span class="sxs-lookup"><span data-stu-id="e72df-131">Click the **Log Info** button in the demo.</span></span>  `Hello, Console!` <span data-ttu-id="e72df-132">Получает запись в журнал консоли.</span><span class="sxs-lookup"><span data-stu-id="e72df-132">gets logged to the Console.</span></span>
    
    :::image type="complex" source="../media/console-log-info.msft.png" alt-text="Сообщения на консоли" lightbox="../media/console-log-info.msft.png":::
       <span data-ttu-id="e72df-134">**Консоль** после нажатия кнопки " **сведения о журнале** "</span><span class="sxs-lookup"><span data-stu-id="e72df-134">The **Console** after clicking **Log Info**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e72df-135">Рядом с `Hello, Console!` сообщением на консоли выберите **log.js:2**.</span><span class="sxs-lookup"><span data-stu-id="e72df-135">Next to the `Hello, Console!` message in the Console choose **log.js:2**.</span></span>  <span data-ttu-id="e72df-136">Откроется панель источники, в которой выделена строка кода, которая привела к тому, что сообщение будет записано на консоль.</span><span class="sxs-lookup"><span data-stu-id="e72df-136">The Sources panel opens and highlights the line of code that caused the message to get logged to the Console.</span></span>  <span data-ttu-id="e72df-137">Сообщение было занесено в журнал при выполнении кода JavaScript на странице `console.log('Hello, Console!')` .</span><span class="sxs-lookup"><span data-stu-id="e72df-137">The message was logged when the JavaScript of the page ran `console.log('Hello, Console!')`.</span></span>
    
    :::image type="complex" source="../media/console-sources-logjs.msft.png" alt-text="Сообщения на консоли" lightbox="../media/console-sources-logjs.msft.png":::
       <span data-ttu-id="e72df-139">DevTools открывает панель « **источники** » после нажатия кнопки</span><span class="sxs-lookup"><span data-stu-id="e72df-139">DevTools opens the **Sources** panel after you click</span></span> `log.js:2`  
    :::image-end:::  
    
1.  <span data-ttu-id="e72df-140">Вернитесь на **консоль** с помощью одного из следующих рабочих процессов:</span><span class="sxs-lookup"><span data-stu-id="e72df-140">Navigate back to the **Console** using any of the following workflows:</span></span>  
    
    *   <span data-ttu-id="e72df-141">Откройте вкладку **консоль** .</span><span class="sxs-lookup"><span data-stu-id="e72df-141">Click the **Console** tab.</span></span>  
    *   <span data-ttu-id="e72df-142">Выберите `Control` + `[` \ (Windows, Linux \) или `Command` + `[` \ (macOS \), пока панель консоли не станет фокусом.</span><span class="sxs-lookup"><span data-stu-id="e72df-142">Select `Control`+`[` \(Windows, Linux\) or `Command`+`[` \(macOS\) until the Console panel is in focus.</span></span>  
    *   <span data-ttu-id="e72df-143">[Откройте меню команд][DevToolsCommandMenu], начните вводить текст `Console` , выберите команду **Показать панель консоли** , а затем нажмите кнопку `Enter` .</span><span class="sxs-lookup"><span data-stu-id="e72df-143">[Open the Command Menu][DevToolsCommandMenu], start typing `Console`, select the **Show Console Panel** command, and then select `Enter`.</span></span>  
    
1.  <span data-ttu-id="e72df-144">Нажмите кнопку **предупреждение журнала** в демонстрационной версии.</span><span class="sxs-lookup"><span data-stu-id="e72df-144">Click the **Log Warning** button in the demo.</span></span>  `Abandon Hope All Ye Who Enter` <span data-ttu-id="e72df-145">Получает запись в журнал консоли.</span><span class="sxs-lookup"><span data-stu-id="e72df-145">gets logged to the Console.</span></span>  <span data-ttu-id="e72df-146">Сообщения, которые форматируются таким образом, представляют собой предупреждения.</span><span class="sxs-lookup"><span data-stu-id="e72df-146">Messages formatted like this are warnings.</span></span>  
    
    :::image type="complex" source="../media/console-log-warning.msft.png" alt-text="Сообщения на консоли" lightbox="../media/console-log-warning.msft.png":::
       <span data-ttu-id="e72df-148">**Консоль** после выбора команды " **log Warning** "</span><span class="sxs-lookup"><span data-stu-id="e72df-148">The **Console** after you choose **Log Warning**</span></span>  
    :::image-end:::  
    
    > [!TIP]
    > <span data-ttu-id="e72df-149">Если вы хотите просмотреть код, который привел к тому, что сообщение записалось определенным образом, нажмите на сценарий \ (например, `log.js:12` \), чтобы просмотреть код, который привел к форматированию сообщения.</span><span class="sxs-lookup"><span data-stu-id="e72df-149">If you want to see the code that caused a message to get logged a certain way, click on a script \(such as `log.js:12`\) to view the code that caused the message to get formatted.</span></span>  

1.  <span data-ttu-id="e72df-150">Щелкните значок **expand** ( ![ Развернуть ][ImageExpandIcon] ) перед `Abandon Hope All Ye Who Enter` .</span><span class="sxs-lookup"><span data-stu-id="e72df-150">Click the **Expand** \(![Expand][ImageExpandIcon]\) icon in front of `Abandon Hope All Ye Who Enter`.</span></span>  <span data-ttu-id="e72df-151">DevTools показывает [трассировку стека][WikiStackTrace] , ведущая к вызову.</span><span class="sxs-lookup"><span data-stu-id="e72df-151">DevTools shows the [stack trace][WikiStackTrace] leading up to the call.</span></span>  
    
    :::image type="complex" source="../media/console-log-warning-expanded.msft.png" alt-text="Сообщения на консоли" lightbox="../media/console-log-warning-expanded.msft.png":::
       <span data-ttu-id="e72df-153">Трассировка стека</span><span class="sxs-lookup"><span data-stu-id="e72df-153">A stack trace</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="e72df-154">Трассировка стека указывает на то, что вызвана функция с именем `logWarning` , которая, в свою очередь, вызывает функцию с именем `quoteDante` .</span><span class="sxs-lookup"><span data-stu-id="e72df-154">The stack trace is telling you that a function named `logWarning` was called, which in turn called a function named `quoteDante`.</span></span>  <span data-ttu-id="e72df-155">Другими словами, вызов, который произошел первым, находится в нижней части трассировки стека.</span><span class="sxs-lookup"><span data-stu-id="e72df-155">In other words, the call that happened first is at the bottom of the stack trace.</span></span>  <span data-ttu-id="e72df-156">Вы можете регистрировать трассировку стека в любое время, вызывая `console.trace()` .</span><span class="sxs-lookup"><span data-stu-id="e72df-156">You may log stack traces at any time by calling `console.trace()`.</span></span>  

1.  <span data-ttu-id="e72df-157">Выберите пункт **Ошибка журнала**.</span><span class="sxs-lookup"><span data-stu-id="e72df-157">Choose **Log Error**.</span></span>  <span data-ttu-id="e72df-158">Регистрируется следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="e72df-158">The following error message gets logged:</span></span> `I'm sorry, Dave.  I'm afraid I can't do that.`  
    
    :::image type="complex" source="../media/console-log-error.msft.png" alt-text="Сообщения на консоли" lightbox="../media/console-log-error.msft.png":::
       <span data-ttu-id="e72df-160">Сообщение об ошибке</span><span class="sxs-lookup"><span data-stu-id="e72df-160">An error message</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e72df-161">Выберите пункт **таблица журнала**.</span><span class="sxs-lookup"><span data-stu-id="e72df-161">Choose **Log Table**.</span></span>  <span data-ttu-id="e72df-162">Таблица, посвященная знаменитым исполнителям, записывается на консоль.</span><span class="sxs-lookup"><span data-stu-id="e72df-162">A table about famous artists gets logged to the Console.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="e72df-163">`birthday`Столбец заполняется только для одной строки.</span><span class="sxs-lookup"><span data-stu-id="e72df-163">The `birthday` column is only populated for one row.</span></span>  <span data-ttu-id="e72df-164">Проверьте код, чтобы определить причину.</span><span class="sxs-lookup"><span data-stu-id="e72df-164">Review the code to determine why that is.</span></span>
    
    :::image type="complex" source="../media/console-log-table.msft.png" alt-text="Сообщения на консоли" lightbox="../media/console-log-table.msft.png":::
       <span data-ttu-id="e72df-166">Таблица в **консоли**</span><span class="sxs-lookup"><span data-stu-id="e72df-166">A table in the **Console**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e72df-167">Выберите команду **Группа журналов**.</span><span class="sxs-lookup"><span data-stu-id="e72df-167">Choose **Log Group**.</span></span>  <span data-ttu-id="e72df-168">Названия четырех знаменитых turtlesных, преступных, группируются под `Adolescent Irradiated Espionage Tortoises` меткой.</span><span class="sxs-lookup"><span data-stu-id="e72df-168">The names of 4 famous, crime-fighting turtles are grouped under the `Adolescent Irradiated Espionage Tortoises` label.</span></span>  
    
    :::image type="complex" source="../media/console-log-group.msft.png" alt-text="Сообщения на консоли" lightbox="../media/console-log-group.msft.png":::
       <span data-ttu-id="e72df-170">Группа сообщений на **консоли**</span><span class="sxs-lookup"><span data-stu-id="e72df-170">A group of messages in the **Console**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e72df-171">Выберите пункт **Журнал настраиваемого**.</span><span class="sxs-lookup"><span data-stu-id="e72df-171">Choose **Log Custom**.</span></span>  <span data-ttu-id="e72df-172">Сообщение с красной рамкой и синим фоном записываются в консоль.</span><span class="sxs-lookup"><span data-stu-id="e72df-172">A message with a red border and blue background gets logged to the Console.</span></span>  
    
    :::image type="complex" source="../media/console-log-custom.msft.png" alt-text="Сообщения на консоли" lightbox="../media/console-log-custom.msft.png":::
       <span data-ttu-id="e72df-174">Сообщение с настраиваемым форматированием в **консоли**</span><span class="sxs-lookup"><span data-stu-id="e72df-174">A message with custom formatting in the **Console**</span></span>  
    :::image-end:::  
    
<span data-ttu-id="e72df-175">Основная идея здесь заключается в том, что если вы хотите записывать сообщения на консоль из JavaScript, используйте один из этих `console` методов.</span><span class="sxs-lookup"><span data-stu-id="e72df-175">The main idea here is that when you want to log messages to the Console from your JavaScript, you use one of the `console` methods.</span></span>  <span data-ttu-id="e72df-176">Каждый метод форматирует сообщения по-разному.</span><span class="sxs-lookup"><span data-stu-id="e72df-176">Each method formats messages differently.</span></span>  

<span data-ttu-id="e72df-177">В этом разделе есть еще больше методов, чем было показано ниже.</span><span class="sxs-lookup"><span data-stu-id="e72df-177">There are even more methods than what has been demonstrated in this section.</span></span>  <span data-ttu-id="e72df-178">В этом учебнике показано, как ознакомиться с другими методами.</span><span class="sxs-lookup"><span data-stu-id="e72df-178">This tutorial shows you how to explore the rest of the methods.</span></span>  

## <span data-ttu-id="e72df-179">Просмотр сообщений, записанных браузером</span><span class="sxs-lookup"><span data-stu-id="e72df-179">View messages logged by the browser</span></span>  

<span data-ttu-id="e72df-180">Браузер также регистрирует сообщения на консоли.</span><span class="sxs-lookup"><span data-stu-id="e72df-180">The browser logs messages to the Console, too.</span></span>  <span data-ttu-id="e72df-181">Обычно это происходит при возникновении проблемы со страницей.</span><span class="sxs-lookup"><span data-stu-id="e72df-181">This usually happens when there is a problem with the page.</span></span>  

1.  <span data-ttu-id="e72df-182">Выберите **причина 404**.</span><span class="sxs-lookup"><span data-stu-id="e72df-182">Choose **Cause 404**.</span></span>  <span data-ttu-id="e72df-183">Браузер регистрирует код состояния HTTP `404` ошибки сети, так как сценарий JavaScript пытается получить несуществующий файл.</span><span class="sxs-lookup"><span data-stu-id="e72df-183">The browser logs an HTTP status code of `404` network error because the JavaScript of the page tried to fetch a file that does not exist.</span></span>  
    
    :::image type="complex" source="../media/console-cause-404.msft.png" alt-text="Сообщения на консоли" lightbox="../media/console-cause-404.msft.png":::
       <span data-ttu-id="e72df-185">`404`Ошибка в **консоли**</span><span class="sxs-lookup"><span data-stu-id="e72df-185">A `404` error in the **Console**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e72df-186">Выберите " **Причина ошибки**".</span><span class="sxs-lookup"><span data-stu-id="e72df-186">Choose **Cause Error**.</span></span>  <span data-ttu-id="e72df-187">Браузер регистрирует неперехваченные записи, `TypeError` так как JavaScript пытается обновить несуществующий узел DOM.</span><span class="sxs-lookup"><span data-stu-id="e72df-187">The browser logs an uncaught `TypeError` because the JavaScript is trying to update a DOM node that does not exist.</span></span>  
    
    :::image type="complex" source="../media/console-cause-error.msft.png" alt-text="Сообщения на консоли" lightbox="../media/console-cause-error.msft.png":::
       <span data-ttu-id="e72df-189">А на `TypeError` **консоли**</span><span class="sxs-lookup"><span data-stu-id="e72df-189">A `TypeError` in the **Console**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e72df-190">Щелкните раскрывающийся список **уровни журнала** и включите параметр **подробный** , если он отключен.</span><span class="sxs-lookup"><span data-stu-id="e72df-190">Click the **Log Levels** dropdown and enable the **Verbose** option if it is disabled.</span></span>  <span data-ttu-id="e72df-191">Подробнее о фильтрации можно узнать в следующем разделе.</span><span class="sxs-lookup"><span data-stu-id="e72df-191">You learn more about filtering in the next section.</span></span>  <span data-ttu-id="e72df-192">Это необходимо сделать, чтобы убедиться в том, что следующее сообщение отображается в журнале.</span><span class="sxs-lookup"><span data-stu-id="e72df-192">You need to do this to make sure that the next message you log is visible.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="e72df-193">Если раскрывающийся список уровни по умолчанию отключен, может потребоваться закрыть панель **консоли** .</span><span class="sxs-lookup"><span data-stu-id="e72df-193">If the Default Levels dropdown is disabled, you may need to close the **Console** Sidebar.</span></span>  <span data-ttu-id="e72df-194">Отфильтровать по источнику сообщения, чтобы получить дополнительные сведения о боковой панели **консоли** .</span><span class="sxs-lookup"><span data-stu-id="e72df-194">Filter by Message Source below for more information about the **Console** Sidebar.</span></span>
    
    :::image type="complex" source="../media/console-cause-error-log-levels.msft.png" alt-text="Сообщения на консоли" lightbox="../media/console-cause-error-log-levels.msft.png":::
       <span data-ttu-id="e72df-196">Включение подробного уровня ведения журнала</span><span class="sxs-lookup"><span data-stu-id="e72df-196">Enabling the Verbose log level</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e72df-197">Выберите команду **вызвать нарушение**.</span><span class="sxs-lookup"><span data-stu-id="e72df-197">Choose **Cause Violation**.</span></span>  <span data-ttu-id="e72df-198">Страница перестает отвечать на запросы в течение нескольких секунд, а затем браузер заносит сообщение `[Violation] 'click' handler took 3000ms` на консоль.</span><span class="sxs-lookup"><span data-stu-id="e72df-198">The page becomes unresponsive for a few seconds and then the browser logs the message `[Violation] 'click' handler took 3000ms` to the Console.</span></span>  <span data-ttu-id="e72df-199">Точная длительность может отличаться.</span><span class="sxs-lookup"><span data-stu-id="e72df-199">The exact duration may vary.</span></span>  
    
    :::image type="complex" source="../media/console-cause-violation.msft.png" alt-text="Сообщения на консоли" lightbox="../media/console-cause-violation.msft.png":::
       <span data-ttu-id="e72df-201">Нарушение в **консоли**</span><span class="sxs-lookup"><span data-stu-id="e72df-201">A violation in the **Console**</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="e72df-202">Фильтрация сообщений</span><span class="sxs-lookup"><span data-stu-id="e72df-202">Filter messages</span></span>  

<span data-ttu-id="e72df-203">На некоторых страницах вы видите консоль с сообщениями.</span><span class="sxs-lookup"><span data-stu-id="e72df-203">On some pages you see the Console get flooded with messages.</span></span>  <span data-ttu-id="e72df-204">DevTools предоставляет множество различных способов фильтрации сообщений, которые не связаны с задачей.</span><span class="sxs-lookup"><span data-stu-id="e72df-204">DevTools provides many different ways to filter out messages that are not relevant to the task at hand.</span></span>  

### <span data-ttu-id="e72df-205">Фильтрация по уровню ведения журнала</span><span class="sxs-lookup"><span data-stu-id="e72df-205">Filter by log level</span></span>  

<span data-ttu-id="e72df-206">Каждому `console` методу назначается уровень серьезности: `Verbose` , `Info` , `Warning` или `Error` .</span><span class="sxs-lookup"><span data-stu-id="e72df-206">Each `console` method is assigned a severity level: `Verbose`, `Info`, `Warning`, or `Error`.</span></span>  <span data-ttu-id="e72df-207">Например, `console.log()` `Info` сообщение на уровне, в то время как `console.error()` сообщение на `Error` уровне.</span><span class="sxs-lookup"><span data-stu-id="e72df-207">For example, `console.log()` is an `Info`-level message, whereas `console.error()` is an `Error`-level message.</span></span>  

1.  <span data-ttu-id="e72df-208">Щелкните раскрывающийся список **уровни журнала** и отключите **ошибки**.</span><span class="sxs-lookup"><span data-stu-id="e72df-208">Click the **Log Levels** dropdown and disable **Errors**.</span></span>  <span data-ttu-id="e72df-209">Уровень отключается, если рядом с ним больше нет метки.</span><span class="sxs-lookup"><span data-stu-id="e72df-209">A level is disabled when there is no longer a checkmark next to it.</span></span>  <span data-ttu-id="e72df-210">`Error`Сообщения на уровне пропадают.</span><span class="sxs-lookup"><span data-stu-id="e72df-210">The `Error`-level messages disappear.</span></span>  
    
    :::image type="complex" source="../media/console-cause-violation-log-levels.msft.png" alt-text="Сообщения на консоли" lightbox="../media/console-cause-violation-log-levels.msft.png":::
       <span data-ttu-id="e72df-212">Отключение сообщений уровня ошибки на **консоли**</span><span class="sxs-lookup"><span data-stu-id="e72df-212">Disabling Error-level messages in the **Console**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e72df-213">Снова щелкните в раскрывающемся списке **уровни журнала** и повторно включите **ошибки**.</span><span class="sxs-lookup"><span data-stu-id="e72df-213">Click the **Log Levels** dropdown again and re-enable **Errors**.</span></span>  <span data-ttu-id="e72df-214">`Error`Снова появятся сообщения уровня.</span><span class="sxs-lookup"><span data-stu-id="e72df-214">The `Error`-level messages reappear.</span></span>  

### <span data-ttu-id="e72df-215">Фильтрация по тексту</span><span class="sxs-lookup"><span data-stu-id="e72df-215">Filter by text</span></span>  

<span data-ttu-id="e72df-216">Если вы хотите только просматривать сообщения, содержащие точную строку, введите эту строку в текстовом поле **Фильтр** .</span><span class="sxs-lookup"><span data-stu-id="e72df-216">When you want to only view messages that include an exact string, type that string into the **Filter** text box.</span></span>  

1.  <span data-ttu-id="e72df-217">Введите `Dave` текст в текстовое поле **Фильтр** .</span><span class="sxs-lookup"><span data-stu-id="e72df-217">Type `Dave` into the **Filter** text box.</span></span>  <span data-ttu-id="e72df-218">Все сообщения, в которых не указана строка `Dave` , скрыты.</span><span class="sxs-lookup"><span data-stu-id="e72df-218">All messages that do not include the string `Dave` are hidden.</span></span>  <span data-ttu-id="e72df-219">Кроме того, вы можете увидеть `Adolescent Irradiated Espionage Tortoises` метку.</span><span class="sxs-lookup"><span data-stu-id="e72df-219">You might also see the `Adolescent Irradiated Espionage Tortoises` label.</span></span>  <span data-ttu-id="e72df-220">Это ошибка.</span><span class="sxs-lookup"><span data-stu-id="e72df-220">That is a bug.</span></span>  
    
    :::image type="complex" source="../media/console-all-messages-text-filter.msft.png" alt-text="Сообщения на консоли" lightbox="../media/console-all-messages-text-filter.msft.png":::
       <span data-ttu-id="e72df-222">Фильтрация сообщений, которые не включают</span><span class="sxs-lookup"><span data-stu-id="e72df-222">Filtering out any message that does not include</span></span> `Dave`  
    :::image-end:::  
    
1.  <span data-ttu-id="e72df-223">`Dave`"Удалить" из текстового поля " **Фильтр** ".</span><span class="sxs-lookup"><span data-stu-id="e72df-223">Delete `Dave` from the **Filter** text box.</span></span>  <span data-ttu-id="e72df-224">Все сообщения снова появятся.</span><span class="sxs-lookup"><span data-stu-id="e72df-224">All the messages reappear.</span></span>  

### <span data-ttu-id="e72df-225">Фильтрация по регулярному выражению</span><span class="sxs-lookup"><span data-stu-id="e72df-225">Filter by regular expression</span></span>  

<span data-ttu-id="e72df-226">Если вы хотите отобразить все сообщения, которые содержат шаблон текста, а не определенную строку, используйте [регулярное выражение][MDNRegularExpressions].</span><span class="sxs-lookup"><span data-stu-id="e72df-226">When you want to show all messages that include a pattern of text, rather than a specific string, use a [regular expression][MDNRegularExpressions].</span></span>  

1.  <span data-ttu-id="e72df-227">Введите `/^[AH]/` текст в текстовое поле **Фильтр** .</span><span class="sxs-lookup"><span data-stu-id="e72df-227">Type `/^[AH]/` into the **Filter** text box.</span></span>  <span data-ttu-id="e72df-228">Введите этот шаблон в [Regex][|::ref1::|Main] , чтобы узнать, что он делает.</span><span class="sxs-lookup"><span data-stu-id="e72df-228">Type this pattern into [RegExr][|::ref1::|Main] for an explanation of what it is doing.</span></span>  
    
    :::image type="complex" source="../media/console-all-messages-regex-filter.msft.png" alt-text="Сообщения на консоли" lightbox="../media/console-all-messages-regex-filter.msft.png":::
       <span data-ttu-id="e72df-230">Фильтрация сообщений, не соответствующих шаблону</span><span class="sxs-lookup"><span data-stu-id="e72df-230">Filtering out any message that does not match the pattern</span></span> `/^[AH]/`  
    :::image-end:::  
    
1.  <span data-ttu-id="e72df-231">`/^[AH]/`"Удалить" из текстового поля " **Фильтр** ".</span><span class="sxs-lookup"><span data-stu-id="e72df-231">Delete `/^[AH]/` from the **Filter** text box.</span></span>  <span data-ttu-id="e72df-232">Все сообщения будут снова видны.</span><span class="sxs-lookup"><span data-stu-id="e72df-232">All messages are visible again.</span></span>  

### <span data-ttu-id="e72df-233">Фильтрация по источнику сообщения</span><span class="sxs-lookup"><span data-stu-id="e72df-233">Filter by message source</span></span>  

<span data-ttu-id="e72df-234">Если вы хотите только просматривать сообщения, поступившие с определенного URL-адреса, используйте **боковую панель**.</span><span class="sxs-lookup"><span data-stu-id="e72df-234">When you want to only view the messages that came from a certain URL, use the **Sidebar**.</span></span>  

1.  <span data-ttu-id="e72df-235">Нажмите кнопку **Показать боковую панель консоли** \ ( ![ Показать боковую панель консоли ][ImageShowConsoleSidebarIcon] ).</span><span class="sxs-lookup"><span data-stu-id="e72df-235">Choose **Show Console Sidebar** \(![Show Console Sidebar][ImageShowConsoleSidebarIcon]\).</span></span>  
    
    :::image type="complex" source="../media/console-sidebar-all-messages.msft.png" alt-text="Сообщения на консоли" lightbox="../media/console-sidebar-all-messages.msft.png":::
       <span data-ttu-id="e72df-237">Боковая панель</span><span class="sxs-lookup"><span data-stu-id="e72df-237">The Sidebar</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e72df-238">Щелкните значок " **развернуть** " и " ![ Развернуть" ][ImageExpandIcon] рядом с количеством сообщений.</span><span class="sxs-lookup"><span data-stu-id="e72df-238">Click the **Expand** \(![Expand][ImageExpandIcon]\) icon next to the number of messages.</span></span>  <span data-ttu-id="e72df-239">На приведенном ниже рисунке количество сообщений обозначено **13 сообщениями**.</span><span class="sxs-lookup"><span data-stu-id="e72df-239">In the following figure, the number of messages is indicated as **13 Messages**.</span></span>  <span data-ttu-id="e72df-240">На **боковой панели** отображается список URL-адресов, которые привели к тому, что сообщения записываются в журнал.</span><span class="sxs-lookup"><span data-stu-id="e72df-240">The **Sidebar** shows a list of URLs that caused messages to be logged.</span></span>  <span data-ttu-id="e72df-241">Например, это `log.js` связано с 11 сообщениями.</span><span class="sxs-lookup"><span data-stu-id="e72df-241">For example, `log.js` caused 11 messages.</span></span>  
    
    :::image type="complex" source="../media/console-sidebar-expanded-all-messages.msft.png" alt-text="Сообщения на консоли" lightbox="../media/console-sidebar-expanded-all-messages.msft.png":::
       <span data-ttu-id="e72df-243">Просмотр источника сообщений на боковой панели</span><span class="sxs-lookup"><span data-stu-id="e72df-243">Viewing the source of messages in the Sidebar</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="e72df-244">Фильтрация по пользовательским сообщениям</span><span class="sxs-lookup"><span data-stu-id="e72df-244">Filter by user messages</span></span>  

<span data-ttu-id="e72df-245">Более того, после того, как вы щелкните **сведения журнала**, сценарий вызывается `console.log('Hello, Console!')` для записи сообщения на консоль.</span><span class="sxs-lookup"><span data-stu-id="e72df-245">Earlier, when you clicked **Log Info**, a script called `console.log('Hello, Console!')` in order to log the message to the Console.</span></span>  <span data-ttu-id="e72df-246">Сообщения, которые регистрируются из сценария JavaScript вроде этого, называются **сообщениями пользователей**.</span><span class="sxs-lookup"><span data-stu-id="e72df-246">Messages logged from JavaScript like this are called **user messages**.</span></span>  <span data-ttu-id="e72df-247">В отличие от того, когда вы щелкните **Причина ошибки 404**, браузер записал `Error` сообщение о том, что запрошенный ресурс не найден.</span><span class="sxs-lookup"><span data-stu-id="e72df-247">In contrast, when you clicked **Cause 404**, the browser logged an `Error`-level message stating that the requested resource could not be found.</span></span>  <span data-ttu-id="e72df-248">Такие сообщения считаются **сообщениями браузера**.</span><span class="sxs-lookup"><span data-stu-id="e72df-248">Messages like that are considered **browser messages**.</span></span>  <span data-ttu-id="e72df-249">Используйте **боковую панель** , чтобы отфильтровать сообщения браузера и показать только сообщения пользователей.</span><span class="sxs-lookup"><span data-stu-id="e72df-249">Use the **Sidebar** to filter out browser messages and only show user messages.</span></span>  

1.  <span data-ttu-id="e72df-250">Выберите **9 пользовательских сообщений**.</span><span class="sxs-lookup"><span data-stu-id="e72df-250">Choose **9 User Messages**.</span></span>  <span data-ttu-id="e72df-251">Сообщения браузера скрыты.</span><span class="sxs-lookup"><span data-stu-id="e72df-251">The browser messages are hidden.</span></span>  
    
    :::image type="complex" source="../media/console-sidebar-user-messages.msft.png" alt-text="Сообщения на консоли" lightbox="../media/console-sidebar-user-messages.msft.png":::
       <span data-ttu-id="e72df-253">Фильтрация сообщений браузера</span><span class="sxs-lookup"><span data-stu-id="e72df-253">Filtering out browser messages</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e72df-254">Выберите **13 сообщений** , чтобы снова Показать все сообщения.</span><span class="sxs-lookup"><span data-stu-id="e72df-254">Choose **13 Messages** to show all messages again.</span></span>  

## <span data-ttu-id="e72df-255">Использование консоли рядом с любой другой панелью</span><span class="sxs-lookup"><span data-stu-id="e72df-255">Use the Console alongside any other panel</span></span>  

<span data-ttu-id="e72df-256">Что делать, если стили редактируются, но вам нужно быстро проверить журнал консоли на что-то?</span><span class="sxs-lookup"><span data-stu-id="e72df-256">What if you are editing styles, but you need to quickly check the Console log for something?</span></span>  <span data-ttu-id="e72df-257">Используйте денежный ящик.</span><span class="sxs-lookup"><span data-stu-id="e72df-257">Use the Drawer.</span></span>  

1.  <span data-ttu-id="e72df-258">Откройте вкладку **элементы** .</span><span class="sxs-lookup"><span data-stu-id="e72df-258">Click the **Elements** tab.</span></span>  
1.  <span data-ttu-id="e72df-259">Выберите `Escape` .</span><span class="sxs-lookup"><span data-stu-id="e72df-259">Select `Escape`.</span></span>  <span data-ttu-id="e72df-260">Откроется вкладка " **консоль** " для **ящика** .</span><span class="sxs-lookup"><span data-stu-id="e72df-260">The **Console** tab of the **Drawer** opens.</span></span>  <span data-ttu-id="e72df-261">У него есть все функции панели консоли, которые использовались в этом учебнике.</span><span class="sxs-lookup"><span data-stu-id="e72df-261">It has all of the features of the Console panel that you have been using throughout this tutorial.</span></span>  
    
    :::image type="complex" source="../media/console-elements-drawer-console-sidebar-all-messages.msft.png" alt-text="Сообщения на консоли" lightbox="../media/console-elements-drawer-console-sidebar-all-messages.msft.png":::
         <span data-ttu-id="e72df-263">Вкладка « **консоль** » в **ящике**</span><span class="sxs-lookup"><span data-stu-id="e72df-263">The **Console** tab in the **Drawer**</span></span>  
    :::image-end:::  
    
<!--## Next steps  -->

<!--
*   See [Console Reference][DevToolsConsoleApi] to explore more features and workflows related to the Console UI.
*   See [Console API Reference][DevToolsConsoleReference] to learn more about all of the `console` methods that were demonstrated in [View messages logged from JavaScript(#view-messages-logged-from-javascript) and explore the other `console` methods that were not covered in this tutorial.  
*   See [Get Started](/microsoft-edge/devtools-guide-chromium/#start) to explore what else you are able to do with DevTools.  -->  

## <span data-ttu-id="e72df-264">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="e72df-264">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageExpandIcon]: ../media/expand-icon.msft.png  
[ImageShowConsoleSidebarIcon]: ../media/show-console-sidebar-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Microsoft Edge \ (Chromium \) Инструменты разработчика | Документы Microsoft"  
[DevToolsCommandMenu]: ../command-menu/index.md "Выполнение команд с помощью командного меню Microsoft Edge DevTools | Документы Microsoft"  
[DevToolsCustomizePlacement]: ../customize/placement.md "Изменение положения Microsoft Edge DevTools | Документы Microsoft"  
[DevToolsConsoleApi]: ./api.md "Справочник по API консоли | Документы Microsoft"  
[DevToolsConsoleReference]: ./reference.md "Справочник по консоли | Документы Microsoft"  

[GlitchDevToolsConsoleLogExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/console/log.html "Начало работы с сообщениями в журнале | Цепь"  

[MDNRegularExpressions]: https://developer.mozilla.org/docs/Web/JavaScript/Guide/Regular_Expressions "Регулярные выражения | MDN"  

[RegExrMain]: https://regexr.com "Регулярное выражение"  

[WikiStackTrace]: https://en.wikipedia.org/wiki/Stack_trace "Трассировка стека — Википедии"  
> [!NOTE]
> <span data-ttu-id="e72df-274">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e72df-274">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="e72df-275">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/console/log) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="e72df-275">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/log) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="e72df-277">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e72df-277">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
