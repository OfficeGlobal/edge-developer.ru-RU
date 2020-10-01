---
description: Сведения о том, как использовать Microsoft Edge DevTools для просмотра и изменения CSS-страниц.
title: Начало работы с просмотром и редактированием CSS
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: f055606ff6140652341627097e7fe7b270dc929c
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993067"
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

# <span data-ttu-id="82fec-104">Начало работы с просмотром и редактированием CSS</span><span class="sxs-lookup"><span data-stu-id="82fec-104">Get Started With Viewing And Changing CSS</span></span>  

<span data-ttu-id="82fec-105">Эти интерактивные учебники помогут вам ознакомиться с основными принципами просмотра и изменения CSS для страниц с помощью Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="82fec-105">Complete these interactive tutorials to learn the basics of viewing and changing the CSS for a page using Microsoft Edge DevTools.</span></span>  

## <span data-ttu-id="82fec-106">Открытие примеров CSS</span><span class="sxs-lookup"><span data-stu-id="82fec-106">Open CSS Examples</span></span>  

1.  <span data-ttu-id="82fec-107">Удерживайте клавишу `Control` \ (Windows \) или `Command` \ (macOS \) и выберите **примеры CSS** , которые нужно открыть в новом окне.</span><span class="sxs-lookup"><span data-stu-id="82fec-107">Hold `Control` \(Windows\) or `Command` \(macOS\) and select **CSS Examples** to open in a new window.</span></span>  
    
    [<span data-ttu-id="82fec-108">Примеры CSS</span><span class="sxs-lookup"><span data-stu-id="82fec-108">CSS Examples</span></span>][GlitchDevToolsCssExamples]  
    
    > [!NOTE]
    > <span data-ttu-id="82fec-109">Если вы хотите [закрепить окно DevTools][DevToolsCustomizePlacement] справа от окна просмотра \ (на рисунке ниже), выберите **Настройка и управление DevTools** `...` .</span><span class="sxs-lookup"><span data-stu-id="82fec-109">If you want to [dock your DevTools window][DevToolsCustomizePlacement] to the right of your viewport \(displayed in the following figure\), select **Customize and control DevTools** `...`.</span></span>  <span data-ttu-id="82fec-110">В раскрывающемся меню **Настройка и управление DevTools** в разделе **закрепляемая на стороне** экрана выберите пункт **закрепить по правому**краю.</span><span class="sxs-lookup"><span data-stu-id="82fec-110">On the **Customize and control DevTools** drop-down menu, in the **Dock side** section, select **Dock to right**.</span></span>  
    
## <span data-ttu-id="82fec-111">Просмотр CSS для элемента</span><span class="sxs-lookup"><span data-stu-id="82fec-111">View the CSS for an element</span></span>  

1.  <span data-ttu-id="82fec-112">[Откройте примеры CSS](#open-css-examples).</span><span class="sxs-lookup"><span data-stu-id="82fec-112">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="82fec-113">Наведите указатель мыши на `Inspect Me!` текст, откройте контекстное меню, а затем выберите команду **проверить**.</span><span class="sxs-lookup"><span data-stu-id="82fec-113">Hover on the `Inspect Me!` text, open the contextual menu \(right-click\), and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="82fec-114">В DevTools на панели " **элементы** " на вкладке " **дерево DOM** " `Inspect Me!` выделена кнопка "элемент".</span><span class="sxs-lookup"><span data-stu-id="82fec-114">In DevTools, on the **Elements** panel, in the **DOM Tree** tab, the `Inspect Me!` element is highlighted.</span></span>  
        
        :::image type="complex" source="../media/css-elements-inspect-me.msft.png" alt-text="Проверяемый элемент выделен в дереве DOM" lightbox="../media/css-elements-inspect-me.msft.png":::
           <span data-ttu-id="82fec-116">Рисунок 1: в **дереве DOM** выделено проверенный элемент</span><span class="sxs-lookup"><span data-stu-id="82fec-116">Figure 1:  The inspected element is highlighted in the **DOM Tree**</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="82fec-117">`Inspect Me!`Найдите значение атрибута в элементе `data-message` и скопируйте его.</span><span class="sxs-lookup"><span data-stu-id="82fec-117">In the `Inspect Me!` element, find the value of the `data-message` attribute and copy it.</span></span>  
1.  <span data-ttu-id="82fec-118">На странице в поле **значение `data-message` :** введите значение.</span><span class="sxs-lookup"><span data-stu-id="82fec-118">On the page, in the **Value of `data-message`:** textbox, enter the value.</span></span>  
1.  <span data-ttu-id="82fec-119">Наведите указатель мыши на `Inspect Me!` текст, откройте контекстное меню, а затем выберите команду **проверить**.</span><span class="sxs-lookup"><span data-stu-id="82fec-119">Hover on the `Inspect Me!` text, open the contextual menu \(right-click\), and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="82fec-120">В DevTools на панели **элементы** откройте вкладку **стили** .</span><span class="sxs-lookup"><span data-stu-id="82fec-120">In DevTools, on the **Elements** panel, select the **Styles** tab.</span></span>  
    1.  <span data-ttu-id="82fec-121">На вкладке **стили** `Inspect Me!` элемент выделен.</span><span class="sxs-lookup"><span data-stu-id="82fec-121">In the **Styles** tab, the `Inspect Me!` element is highlighted.</span></span>  
    1.  <span data-ttu-id="82fec-122">В `Inspect Me!` элементе найдите `aloha` правило класса.</span><span class="sxs-lookup"><span data-stu-id="82fec-122">In the `Inspect Me!` element, find the `aloha` class rule.</span></span>  
        
        > [!NOTE]
        > <span data-ttu-id="82fec-123">Вы видите это правило, так как оно применяется к `Inspect Me!` элементу.</span><span class="sxs-lookup"><span data-stu-id="82fec-123">You see this rule because it is being applied to the `Inspect Me!` element.</span></span>  
        
    1.  <span data-ttu-id="82fec-124">В `aloha` классе найдите значение для `padding` стиля и скопируйте его.</span><span class="sxs-lookup"><span data-stu-id="82fec-124">In the `aloha` class, find the value for the `padding` style and copy it.</span></span>  
        
        :::image type="complex" source="../media/css-elements-inspect-me-styles.msft.png" alt-text="Проверяемый элемент выделен в дереве DOM" lightbox="../media/css-elements-inspect-me-styles.msft.png":::
           <span data-ttu-id="82fec-126">Рисунок 2: классы CSS, примененные к выбранному элементу, такие как `aloha` , отображаются на вкладке **стили**</span><span class="sxs-lookup"><span data-stu-id="82fec-126">Figure 2:  CSS classes being applied to the selected element, such as `aloha`, are displayed in the **Styles** tab</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="82fec-127">На странице в поле **значение `padding` :** введите значение.</span><span class="sxs-lookup"><span data-stu-id="82fec-127">On the page, in the **Value of `padding`:** textbox, enter the value.</span></span>  

## <span data-ttu-id="82fec-128">Добавление объявления CSS в элемент</span><span class="sxs-lookup"><span data-stu-id="82fec-128">Add a CSS declaration to an element</span></span>  

<span data-ttu-id="82fec-129">Используйте вкладку **стили** , если вы хотите изменить или добавить объявления CSS к элементу.</span><span class="sxs-lookup"><span data-stu-id="82fec-129">Use the **Styles** tab when you want to change or add CSS declarations to an element.</span></span>  

> [!NOTE]
> <span data-ttu-id="82fec-130">Завершите [Просмотр CSS для](#view-the-css-for-an-element) учебника по элементу, прежде чем сделать это.</span><span class="sxs-lookup"><span data-stu-id="82fec-130">Complete the [View the CSS for an element](#view-the-css-for-an-element) tutorial before doing this one.</span></span>  

1.  <span data-ttu-id="82fec-131">[Откройте примеры CSS](#open-css-examples).</span><span class="sxs-lookup"><span data-stu-id="82fec-131">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="82fec-132">Наведите указатель мыши на `Add A Background Color To Me!` текст, откройте контекстное меню, а затем выберите команду **проверить**.</span><span class="sxs-lookup"><span data-stu-id="82fec-132">Hover on the `Add A Background Color To Me!` text, open the contextual menu \(right-click\), and select **Inspect**.</span></span>  
1.  <span data-ttu-id="82fec-133">Нажмите кнопку в `element.style` верхней части вкладки **стили** .</span><span class="sxs-lookup"><span data-stu-id="82fec-133">Select `element.style` near the top of the **Styles** tab.</span></span>  
1.  <span data-ttu-id="82fec-134">Введите текст `background-color` и нажмите клавишу `Enter` .</span><span class="sxs-lookup"><span data-stu-id="82fec-134">Type `background-color` and press `Enter`.</span></span>  
1.  <span data-ttu-id="82fec-135">Введите текст `honeydew` и нажмите клавишу `Enter` .</span><span class="sxs-lookup"><span data-stu-id="82fec-135">Type `honeydew` and press `Enter`.</span></span>  <span data-ttu-id="82fec-136">В **дереве DOM** вы увидите, что к элементу применено объявление встроенного стиля.</span><span class="sxs-lookup"><span data-stu-id="82fec-136">In the **DOM Tree** you should see that an inline style declaration was applied to the element.</span></span>  
    
    :::image type="complex" source="../media/css-elements-add-background-color-to-me-styles-p.msft.png" alt-text="Проверяемый элемент выделен в дереве DOM" lightbox="../media/css-elements-add-background-color-to-me-styles-p.msft.png":::
       <span data-ttu-id="82fec-138">Рисунок 3: `background-color:honeydew` объявление применено к элементу с помощью `element.style` раздела вкладки " **стили** "</span><span class="sxs-lookup"><span data-stu-id="82fec-138">Figure 3:  The `background-color:honeydew` declaration has been applied to the element using the `element.style` section of the **Styles** tab</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="82fec-139">Добавление класса CSS в элемент</span><span class="sxs-lookup"><span data-stu-id="82fec-139">Add a CSS class to an element</span></span>  

<span data-ttu-id="82fec-140">С помощью вкладки " **стили** " можно увидеть, как выглядит элемент, когда класс CSS применяется к элементу или удаляется из него.</span><span class="sxs-lookup"><span data-stu-id="82fec-140">Use the **Styles** tab to see how an element looks when a CSS class is applied to or removed from an element.</span></span>  

> [!NOTE]
> <span data-ttu-id="82fec-141">Завершите [Просмотр CSS для](#view-the-css-for-an-element) учебника по элементу, прежде чем сделать это.</span><span class="sxs-lookup"><span data-stu-id="82fec-141">Complete the [View the CSS for an element](#view-the-css-for-an-element) tutorial before doing this one.</span></span>  

1.  <span data-ttu-id="82fec-142">[Откройте примеры CSS](#open-css-examples).</span><span class="sxs-lookup"><span data-stu-id="82fec-142">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="82fec-143">Наведите указатель мыши на `Add A Class To Me!` текст, откройте контекстное меню, а затем выберите команду **проверить**.</span><span class="sxs-lookup"><span data-stu-id="82fec-143">Hover on the `Add A Class To Me!` text, open the contextual menu \(right-click\), and select **Inspect**.</span></span>  
1.  <span data-ttu-id="82fec-144">Выберите **. CLS**.</span><span class="sxs-lookup"><span data-stu-id="82fec-144">Select **.cls**.</span></span>  <span data-ttu-id="82fec-145">DevTools открывает текстовое поле, в котором можно добавлять классы к выбранному элементу.</span><span class="sxs-lookup"><span data-stu-id="82fec-145">DevTools reveals a text box where you may add classes to the selected element.</span></span>  
1.  <span data-ttu-id="82fec-146">Введите `color_me` текст в текстовом поле **Добавить новый класс** и нажмите клавишу `Enter` .</span><span class="sxs-lookup"><span data-stu-id="82fec-146">Type `color_me` in the **Add new class** text box and then press `Enter`.</span></span>  <span data-ttu-id="82fec-147">Флажок отображается под текстовым полем " **Добавить новый класс** ", в котором можно включить или отключить класс.</span><span class="sxs-lookup"><span data-stu-id="82fec-147">A checkbox appears below the **Add new class** text box, where you may toggle the class on and off.</span></span>  <span data-ttu-id="82fec-148">Если `Add A Class To Me!` к элементу применены другие классы, вы также можете переключаться между ними.</span><span class="sxs-lookup"><span data-stu-id="82fec-148">If the `Add A Class To Me!` element has any other classes applied to it, you are also able to toggle each from here.</span></span>  
    
    :::image type="complex" source="../media/css-elements-add-a-class-to-me-styles-cls.msft.png" alt-text="Проверяемый элемент выделен в дереве DOM" lightbox="../media/css-elements-add-a-class-to-me-styles-cls.msft.png":::
       <span data-ttu-id="82fec-150">Рисунок 4: `color_me` класс применен к элементу с помощью раздела **. CLS** на вкладке " **стили** ".</span><span class="sxs-lookup"><span data-stu-id="82fec-150">Figure 4:  The `color_me` class has been applied to the element using the **.cls** section of the **Styles** tab</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="82fec-151">Добавление PseudoState в класс</span><span class="sxs-lookup"><span data-stu-id="82fec-151">Add a pseudostate to a class</span></span>  

<span data-ttu-id="82fec-152">С помощью вкладки **стили** вы можете навсегда применить CSS-PseudoState к элементу.</span><span class="sxs-lookup"><span data-stu-id="82fec-152">Use the **Styles** tab to permanently apply a CSS pseudostate to an element.</span></span>  <span data-ttu-id="82fec-153">DevTools поддерживает `:active` , `:focus` , `:hover` , и `:visited` .</span><span class="sxs-lookup"><span data-stu-id="82fec-153">DevTools supports `:active`, `:focus`, `:hover`, and `:visited`.</span></span>  

> [!NOTE]
> <span data-ttu-id="82fec-154">Завершите [Просмотр CSS для](#view-the-css-for-an-element) учебника по элементу, прежде чем сделать это.</span><span class="sxs-lookup"><span data-stu-id="82fec-154">Complete the [View the CSS for an element](#view-the-css-for-an-element) tutorial before doing this one.</span></span>  

1.  <span data-ttu-id="82fec-155">[Откройте примеры CSS](#open-css-examples).</span><span class="sxs-lookup"><span data-stu-id="82fec-155">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="82fec-156">Наведите указатель мыши на `Hover Over Me!` текст.</span><span class="sxs-lookup"><span data-stu-id="82fec-156">Hover over the `Hover Over Me!` text.</span></span>  <span data-ttu-id="82fec-157">Цвет фона изменится.</span><span class="sxs-lookup"><span data-stu-id="82fec-157">The background color changes.</span></span>  
1.  <span data-ttu-id="82fec-158">Наведите указатель мыши на `Hover Over Me!` текст, откройте контекстное меню, а затем выберите команду **проверить**.</span><span class="sxs-lookup"><span data-stu-id="82fec-158">Hover on the `Hover Over Me!` text, open the contextual menu \(right-click\), and select **Inspect**.</span></span>  
1.  <span data-ttu-id="82fec-159">На вкладке **стили** выберите **: Hov**.</span><span class="sxs-lookup"><span data-stu-id="82fec-159">In the **Styles** tab, select **:hov**.</span></span>  
1.  <span data-ttu-id="82fec-160">Установите флажок **: наведение указателя мыши** .</span><span class="sxs-lookup"><span data-stu-id="82fec-160">Check the **:hover** checkbox.</span></span>  <span data-ttu-id="82fec-161">Цвет фона изменится так же, как и раньше, несмотря на то, что вы не наводите указатель мыши на элемент.</span><span class="sxs-lookup"><span data-stu-id="82fec-161">The background color changes like before, even though you are not actually hovering over the element.</span></span>  
    
    :::image type="complex" source="../media/css-elements-hover-over-me-styles-hov-hover.msft.png" alt-text="Проверяемый элемент выделен в дереве DOM" lightbox="../media/css-elements-hover-over-me-styles-hov-hover.msft.png":::
       <span data-ttu-id="82fec-163">Рисунок 5: Переключение `:hover` PseudoState на элементе</span><span class="sxs-lookup"><span data-stu-id="82fec-163">Figure 5:  Toggling the `:hover` pseudostate on an element</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="82fec-164">Изменение размеров элемента</span><span class="sxs-lookup"><span data-stu-id="82fec-164">Change the dimensions of an element</span></span>  

<span data-ttu-id="82fec-165">С помощью интерактивной схемы **"модель Box** " на вкладке " **стили** " можно изменить ширину, высоту, заполнение, границу или длину границы элемента.</span><span class="sxs-lookup"><span data-stu-id="82fec-165">Use the **Box Model** interactive diagram in the **Styles** tab to change the width, height, padding, margin, or border length of an element.</span></span>  

> [!NOTE]
> <span data-ttu-id="82fec-166">Завершите [Просмотр CSS для](#view-the-css-for-an-element) учебника по элементу, прежде чем сделать это.</span><span class="sxs-lookup"><span data-stu-id="82fec-166">Complete the [View the CSS for an element](#view-the-css-for-an-element) tutorial before doing this one.</span></span>  

1.  <span data-ttu-id="82fec-167">[Откройте примеры CSS](#open-css-examples).</span><span class="sxs-lookup"><span data-stu-id="82fec-167">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="82fec-168">Наведите указатель мыши на `Change My Margin!` текст, откройте контекстное меню, а затем выберите команду **проверить**.</span><span class="sxs-lookup"><span data-stu-id="82fec-168">Hover on the `Change My Margin!` text, open the contextual menu \(right-click\), and select **Inspect**.</span></span>  
1.  <span data-ttu-id="82fec-169">На схеме **модель Box** на вкладке **стили** наведите указатель мыши на **Заполнение**.</span><span class="sxs-lookup"><span data-stu-id="82fec-169">In the **Box Model** diagram in the **Styles** tab, hover over **padding**.</span></span>  <span data-ttu-id="82fec-170">Заполнение элемента выделено в окне просмотра.</span><span class="sxs-lookup"><span data-stu-id="82fec-170">The padding of an element is highlighted in the viewport.</span></span>  

    > [!NOTE]
    > <span data-ttu-id="82fec-171">В зависимости от размера окна DevTools, возможно, потребуется прокрутить в нижнюю часть вкладки **стили** , чтобы увидеть **модель Box**.</span><span class="sxs-lookup"><span data-stu-id="82fec-171">Depending on the size of your DevTools window, you may need to scroll to the bottom of the **Styles** tab to see the **Box Model**.</span></span>  

1.  <span data-ttu-id="82fec-172">Дважды щелкните левое поле в **модели Box**, которое в настоящее время имеет значение `-` , означающее, что у элемента нет левого поля.</span><span class="sxs-lookup"><span data-stu-id="82fec-172">Double-click the left margin in the **Box Model**, which currently has a value of `-` meaning that the element does not have a left-margin.</span></span>  
1.  <span data-ttu-id="82fec-173">Введите текст `100px` и нажмите клавишу `Enter` .</span><span class="sxs-lookup"><span data-stu-id="82fec-173">Type `100px` and press `Enter`.</span></span>  <span data-ttu-id="82fec-174">**Модель Box** по умолчанию имеет значения пикселей, но также принимает другие значения, например `25%` или `10vw` .</span><span class="sxs-lookup"><span data-stu-id="82fec-174">The **Box Model** defaults to pixels, but it also accepts other values, such as `25%`, or `10vw`.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/css-elements-change-my-margin-styles-padding.msft.png" alt-text="Проверяемый элемент выделен в дереве DOM" lightbox="../media/css-elements-change-my-margin-styles-padding.msft.png":::
             <span data-ttu-id="82fec-176">Рисунок 6: наведение указателя мыши на заполнение элемента</span><span class="sxs-lookup"><span data-stu-id="82fec-176">Figure 6:  Hovering over the padding of the element</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/css-elements-change-my-margin-styles-margin-edit.msft.png" alt-text="Проверяемый элемент выделен в дереве DOM" lightbox="../media/css-elements-change-my-margin-styles-margin-edit.msft.png":::
             <span data-ttu-id="82fec-178">Рисунок 7: изменение левого поля элемента</span><span class="sxs-lookup"><span data-stu-id="82fec-178">Figure 7:  Changing the left-margin of the element</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
## <span data-ttu-id="82fec-179">Отладка запросов мультимедиа</span><span class="sxs-lookup"><span data-stu-id="82fec-179">Debugging Media Queries</span></span>  

<span data-ttu-id="82fec-180">С помощью [запросов мультимедиа][MDNUsingMediaGueries] можно сделать так, чтобы ваш веб-продукт реагировал на изменения параметров конфигурации для каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="82fec-180">[Media Queries][MDNUsingMediaGueries] are a way to make your web product react to changes in the configuration settings for each user.</span></span>  <span data-ttu-id="82fec-181">Наиболее важным вариантом использования является предоставление для продукта другого макета CSS в зависимости от размеров окна просмотра.</span><span class="sxs-lookup"><span data-stu-id="82fec-181">The most significant use case is to provide your product a different CSS layout depending on the dimensions of the viewport.</span></span>  <span data-ttu-id="82fec-182">Использование раздельных макетов позволяет создавать макеты с одним столбцом для мобильных устройств и многостолбцовый макет, если доступно больше свободного пространства на экране.</span><span class="sxs-lookup"><span data-stu-id="82fec-182">Using separate layouts allows for a one-column layout for mobile devices and multi-column layouts when there is more screen estate available.</span></span>  

<span data-ttu-id="82fec-183">Чтобы выполнить отладку или тестирование запросов мультимедиа, определенных в таблице CSS, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="82fec-183">If you want to debug or test the Media Queries you defined in your CSS, use the following steps.</span></span>  

1.  <span data-ttu-id="82fec-184">Откройте Инструменты разработчика и выберите значок **Переключить панель инструментов** на вкладке на верхнем левом углу или нажмите клавиши `Ctrl` + `Shift` + `M` \ ( `Cmd` + `Shift` + `M` на macOS \).</span><span class="sxs-lookup"><span data-stu-id="82fec-184">Open the developer tools and select the **Toggle device toolbar** icon second on the top-left, or press `Ctrl`+`Shift`+`M` \(`Cmd`+`Shift`+`M` on macOS\).</span></span>  
    
    :::image type="complex" source="../media/css-elements-media-queries-open-device-toolbar.msft.png" alt-text="Проверяемый элемент выделен в дереве DOM" lightbox="../media/css-elements-media-queries-open-device-toolbar.msft.png":::
       <span data-ttu-id="82fec-186">Рисунок 8: Открытие панели инструментов устройства</span><span class="sxs-lookup"><span data-stu-id="82fec-186">Figure 8:  Opening the device toolbar</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="82fec-187">На панели инструментов устройства откройте `...` меню в правом верхнем углу и выберите **просмотреть запросы мультимедиа**.</span><span class="sxs-lookup"><span data-stu-id="82fec-187">With the device toolbar open, select the `...` menu on the top-right and select **View Media Queries**.</span></span>  <span data-ttu-id="82fec-188">На экран выводится цветная полоса, представляющая различные запросы мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="82fec-188">You should see colored bars above the display of the page that represent the different media queries.</span></span>  
    
    :::image type="complex" source="../media/css-elements-media-queries-showing-mq.msft.png" alt-text="Проверяемый элемент выделен в дереве DOM" lightbox="../media/css-elements-media-queries-showing-mq.msft.png":::
       <span data-ttu-id="82fec-190">Рис. 9: отображение запросов мультимедиа на панели инструментов устройства</span><span class="sxs-lookup"><span data-stu-id="82fec-190">Figure 9:  Showing Media Queries in Device Toolbar</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="82fec-191">Наведите указатель мыши на границу линии, чтобы просмотреть значения различных запросов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="82fec-191">Hover over the boundaries in the bars to see the values of the different media queries.</span></span> <span data-ttu-id="82fec-192">Выберите каждый из них, чтобы изменить размер веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="82fec-192">Select each to resize the web page to match.</span></span>  
    
    :::image type="complex" source="../media/css-elements-media-queries-select-bar.msft.png" alt-text="Проверяемый элемент выделен в дереве DOM" lightbox="../media/css-elements-media-queries-select-bar.msft.png":::
       <span data-ttu-id="82fec-194">Рисунок 10: выбор запроса мультимедиа из панели предварительного просмотра</span><span class="sxs-lookup"><span data-stu-id="82fec-194">Figure 10:  Selecting Media Query from preview bar</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="82fec-195">Чтобы выполнить отладку запросов мультимедиа и открыть CSS-файл в `Sources` редакторе, наведите указатель мыши на любой из сегментов отрезков, откройте контекстное меню, а затем выберите команду `reveal in source code` .</span><span class="sxs-lookup"><span data-stu-id="82fec-195">To debug media queries and open the CSS file in the `Sources` editor; hover on any of the bar segments, open the contextual menu \(right-click\), and select `reveal in source code`.</span></span>  
    
    :::image type="complex" source="../media/css-elements-media-queries-reveal-in-sources.msft.png" alt-text="Проверяемый элемент выделен в дереве DOM" lightbox="../media/css-elements-media-queries-reveal-in-sources.msft.png":::
       <span data-ttu-id="82fec-197">Рисунок 11: отображение запросов мультимедиа в редакторе источников</span><span class="sxs-lookup"><span data-stu-id="82fec-197">Figure 11:  Revealing Media Queries in Sources Editor</span></span>  
    :::image-end:::  
    
<!-- links -->  

[DevToolsCustomizePlacement]: /microsoft-edge/devtools-guide-chromium/customize/placement "Изменение положения DevTools Microsoft EDGE (Отстыковка, закрепить в нижней части, закрепить слева)"  

[GlitchDevToolsCssExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/css/examples/ecma.html "Примеры CSS — Microsoft EDGE (Chromium) DevTools | Цепь"  

[MDNUsingMediaGueries]: https://developer.mozilla.org/docs/Web/CSS/Media_Queries/Using_media_queries "Использование мультимедийных запросов | MDN"  

> [!NOTE]
> <span data-ttu-id="82fec-201">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="82fec-201">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="82fec-202">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/css/index) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="82fec-202">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/css/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="82fec-204">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="82fec-204">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
