---
description: Начало работы с CSS
title: 'DevTools для начинающих: Приступая к работе с CSS'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: fe87b4f840c6d9dde3cdf6455700161ea8d8d31e
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993305"
---
<!-- Copyright Katherine Jackson 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->

# <span data-ttu-id="2f445-104">DevTools для начинающих: Приступая к работе с CSS</span><span class="sxs-lookup"><span data-stu-id="2f445-104">DevTools for beginners: Get started with CSS</span></span>  

<span data-ttu-id="2f445-105">В этом учебнике вы узнаете, как использовать CSS для стиля веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="2f445-105">In this tutorial, you learn how to use CSS to style a web page.</span></span>  <span data-ttu-id="2f445-106">Кроме того, вы узнаете, как использовать Microsoft Edge DevTools для экспериментов с изменениями CSS.</span><span class="sxs-lookup"><span data-stu-id="2f445-106">You also learn how to use Microsoft Edge DevTools to experiment with CSS changes.</span></span>  

<span data-ttu-id="2f445-107">В следующей статье приведен второй учебник из серии руководств, в которых рассматриваются основы разработки веб-приложений и Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="2f445-107">The following article is the second tutorial in a series of tutorials that teaches you the basics of web development and Microsoft Edge DevTools.</span></span>  <span data-ttu-id="2f445-108">Вы получаете практический опыт, завершив создание собственного веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="2f445-108">You gain hands-on experience by actually building your own website.</span></span>  <span data-ttu-id="2f445-109">Перед вторым учебником вам не нужно выполнять первый из них.</span><span class="sxs-lookup"><span data-stu-id="2f445-109">You do not have to complete the first tutorial before following the second.</span></span>  <span data-ttu-id="2f445-110">[Настройка кода](#set-up-your-code) показывает, как это сделать.</span><span class="sxs-lookup"><span data-stu-id="2f445-110">[Set up your code](#set-up-your-code) shows you how to get set up.</span></span>  

> [!NOTE]
> <span data-ttu-id="2f445-111">Этот учебник предназначен для абсолютных новичков и специализируется на **основах разработки веб-приложений** и основах использования DevTools для экспериментов с CSS.</span><span class="sxs-lookup"><span data-stu-id="2f445-111">This tutorial is designed for absolute beginners and focuses on both the **fundamentals of web development** and the basics of using DevTools to experiment with CSS.</span></span>  <span data-ttu-id="2f445-112">Если вам нужен учебник, который фокусируется только на DevTools, ознакомьтесь [со статьей Приступая к просмотру и изменению CSS][DevtoolsCssIndex].</span><span class="sxs-lookup"><span data-stu-id="2f445-112">If you want a tutorial that only focuses on DevTools, see [Get Started with Viewing and Changing CSS][DevtoolsCssIndex].</span></span>  

<span data-ttu-id="2f445-113">В начале учебника ваш сайт должен выглядеть так, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="2f445-113">At the beginning of the tutorial, your site should look like the following figure.</span></span>  

:::image type="complex" source="../media/beginners-css-intro1.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-intro1.msft.png":::
   <span data-ttu-id="2f445-115">Как выглядит ваш веб-сайт</span><span class="sxs-lookup"><span data-stu-id="2f445-115">What your site currently looks like</span></span>  
:::image-end:::  

<span data-ttu-id="2f445-116">После того как вы закончите обучение, сайт должен выглядеть так, как показано на рисунке ниже.</span><span class="sxs-lookup"><span data-stu-id="2f445-116">After you complete the tutorial, you site should look like the following figure.</span></span>  

:::image type="complex" source="../media/beginners-css-intro2.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-intro2.msft.png":::
   <span data-ttu-id="2f445-118">Сведения о том, как должен выглядеть сайт в конце учебника</span><span class="sxs-lookup"><span data-stu-id="2f445-118">What your site should look like at the end of the tutorial</span></span>  
:::image-end:::  

## <span data-ttu-id="2f445-119">Цели</span><span class="sxs-lookup"><span data-stu-id="2f445-119">Goals</span></span>  

<span data-ttu-id="2f445-120">Следуйте этим рекомендациям, чтобы лучше разобраться в описанных ниже концепциях и задачах.</span><span class="sxs-lookup"><span data-stu-id="2f445-120">Follow this tutorial to better understand the following concepts and tasks.</span></span>  

*   <span data-ttu-id="2f445-121">Использование CSS для стиля веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="2f445-121">How to use CSS to style a web page.</span></span>  
*   <span data-ttu-id="2f445-122">Использование Microsoft Edge DevTools для экспериментов с CSS.</span><span class="sxs-lookup"><span data-stu-id="2f445-122">How to use Microsoft Edge DevTools to experiment with CSS.</span></span>  
*   <span data-ttu-id="2f445-123">Разница между платформами CSS и CSS.</span><span class="sxs-lookup"><span data-stu-id="2f445-123">The difference between CSS and CSS frameworks.</span></span>  

<span data-ttu-id="2f445-124">Вы собираетесь создать реальный веб-сайт.</span><span class="sxs-lookup"><span data-stu-id="2f445-124">You are building a real website.</span></span>  

## <span data-ttu-id="2f445-125">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="2f445-125">Prerequisites</span></span>  

<span data-ttu-id="2f445-126">Перед началом работы с учебником заполните следующие предварительные требования.</span><span class="sxs-lookup"><span data-stu-id="2f445-126">Before attempting this tutorial, complete the following prerequisites.</span></span>  

*   <span data-ttu-id="2f445-127">Закончите [работу с HTML и моделью DOM][DevtoolsBeginnersHtml] или убедитесь в том, что вы знаете HTML и модель DOM, похожую на то, что научились в этом учебнике.</span><span class="sxs-lookup"><span data-stu-id="2f445-127">Complete [Get Started with HTML and the DOM][DevtoolsBeginnersHtml] or make sure that you have an understanding of HTML and the DOM similar to what is taught in that tutorial.</span></span>  
*   <span data-ttu-id="2f445-128">Скачайте веб-браузер [Microsoft Edge][MicrosoftEdgeInsider] .</span><span class="sxs-lookup"><span data-stu-id="2f445-128">Download the [Microsoft Edge][MicrosoftEdgeInsider] web browser.</span></span>  <span data-ttu-id="2f445-129">В следующем учебнике используется набор средств разработки веб-приложений, которые называются Microsoft Edge DevTools, которые встроены в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2f445-129">The following tutorial uses a set of web development tools, called the Microsoft Edge DevTools, that are built into Microsoft Edge.</span></span>  

## <span data-ttu-id="2f445-130">Настройка кода</span><span class="sxs-lookup"><span data-stu-id="2f445-130">Set up your code</span></span>  

<span data-ttu-id="2f445-131">Чтобы создать сайт, необходимо выполнить описанные ниже действия, чтобы настроить код.</span><span class="sxs-lookup"><span data-stu-id="2f445-131">To create your site, you must first complete the following actions to set up your code.</span></span>  

> [!NOTE]
> <span data-ttu-id="2f445-132">Если вы уже завершили первый учебник в ряду, перейдите к следующему разделу.</span><span class="sxs-lookup"><span data-stu-id="2f445-132">If you have already completed the first tutorial in the series, skip to the next section.</span></span>  <span data-ttu-id="2f445-133">Продолжайте использовать код из последнего учебника, Приступая к [работе с HTML и DOM][DevtoolsBeginnersHtml].</span><span class="sxs-lookup"><span data-stu-id="2f445-133">Continue using your code from the last tutorial, [Get Started with HTML and the DOM][DevtoolsBeginnersHtml].</span></span>  

1.  <span data-ttu-id="2f445-134">Откройте [Исходный код][GlitchCookedAmphibianIndex].</span><span class="sxs-lookup"><span data-stu-id="2f445-134">Open the [source code][GlitchCookedAmphibianIndex].</span></span>  <span data-ttu-id="2f445-135">Ссылка на вкладку "на фокус" в браузере указана как **вкладка "Редактирование"**.</span><span class="sxs-lookup"><span data-stu-id="2f445-135">The in-focus tab of your browser is referenced as the **editing tab**.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-setup1.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-setup1.msft.png":::
       <span data-ttu-id="2f445-137">Вкладка " **Редактирование** "</span><span class="sxs-lookup"><span data-stu-id="2f445-137">The **editing** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="2f445-138">Выберите **готовил-amphibian**.</span><span class="sxs-lookup"><span data-stu-id="2f445-138">Choose **cooked-amphibian**.</span></span>  <span data-ttu-id="2f445-139">Всплывающее меню.</span><span class="sxs-lookup"><span data-stu-id="2f445-139">A menu pops up.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-setup2.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-setup2.msft.png":::
       <span data-ttu-id="2f445-141">Меню "Параметры проекта"</span><span class="sxs-lookup"><span data-stu-id="2f445-141">The Project Options menu</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="2f445-142">Выберите **Remix проект**.</span><span class="sxs-lookup"><span data-stu-id="2f445-142">Choose **Remix Project**.</span></span>  <span data-ttu-id="2f445-143">Сбой создает копию проекта, которую вы можете редактировать.</span><span class="sxs-lookup"><span data-stu-id="2f445-143">Glitch creates a copy of the project that you are able to edit.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="2f445-144">Сбой генерирует случайное имя для нового проекта.</span><span class="sxs-lookup"><span data-stu-id="2f445-144">Glitch generates a random name for the new project.</span></span>  
    
1.  <span data-ttu-id="2f445-145">Нажмите кнопку **Показать** и выберите **в новом окне**.</span><span class="sxs-lookup"><span data-stu-id="2f445-145">Choose **Show** and select **In a New Window**.</span></span>  <span data-ttu-id="2f445-146">Откроется другая вкладка с активным представлением сайта.</span><span class="sxs-lookup"><span data-stu-id="2f445-146">Another tab opens with a live view of your site.</span></span>  <span data-ttu-id="2f445-147">На вкладку, которая находится в фокусе браузера, указывается **вкладка Динамический**.</span><span class="sxs-lookup"><span data-stu-id="2f445-147">The in-focus tab of your browser is referenced as the **live tab**.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-setup3.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-setup3.msft.png":::
       <span data-ttu-id="2f445-149">**Вкладка "динамический"**</span><span class="sxs-lookup"><span data-stu-id="2f445-149">The **live tab**</span></span>  
    :::image-end:::  

## <span data-ttu-id="2f445-150">Общие сведения о CSS</span><span class="sxs-lookup"><span data-stu-id="2f445-150">Understand CSS</span></span>  

<span data-ttu-id="2f445-151">**CSS** — это язык компьютера, который определяет макет и стиль веб-страниц.</span><span class="sxs-lookup"><span data-stu-id="2f445-151">**CSS** is a computer language that determines the layout and styling of web pages.</span></span>  <span data-ttu-id="2f445-152">На приведенном ниже рисунке показан абзац с границей.</span><span class="sxs-lookup"><span data-stu-id="2f445-152">The following figure is a paragraph with a border.</span></span>  

:::image type="complex" source="../media/beginners-css-red_paragraph.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-red_paragraph.msft.png":::
   <span data-ttu-id="2f445-154">Текст был добавлен в таблицу каскадных стилей (CSS)</span><span class="sxs-lookup"><span data-stu-id="2f445-154">The text has been styled with CSS</span></span>  
:::image-end:::  

<span data-ttu-id="2f445-155">Следующий фрагмент кода — это код HTML и CSS, который используется для создания абзаца на предыдущем рисунке.</span><span class="sxs-lookup"><span data-stu-id="2f445-155">The following code snippet is the HTML and CSS code used to create the paragraph in the previous figure.</span></span>  

```html
<p style="border: 1px dashed red; padding: 5px;">
    This has been styled with CSS.
</p>
```  

`style="border: 1px dashed red; padding: 5px;"` <span data-ttu-id="2f445-156">возможно, вам покажется, что у вас новый.</span><span class="sxs-lookup"><span data-stu-id="2f445-156">probably looks new to you.</span></span>  <span data-ttu-id="2f445-157">Остальные должны выглядеть знакомым.</span><span class="sxs-lookup"><span data-stu-id="2f445-157">The rest should look familiar.</span></span>  <span data-ttu-id="2f445-158">Если это не так, сначала приступайте [к работе с HTML и моделью DOM,][DevtoolsBeginnersHtml] прежде чем выполнять следующие разделы.</span><span class="sxs-lookup"><span data-stu-id="2f445-158">If not, complete [Get Started with HTML and the DOM][DevtoolsBeginnersHtml] before attempting the following sections.</span></span>  

## <span data-ttu-id="2f445-159">Добавление встроенных стилей</span><span class="sxs-lookup"><span data-stu-id="2f445-159">Add inline styles</span></span>  

<span data-ttu-id="2f445-160">Выполните указанные ниже действия, чтобы применить стили к одному элементу с помощью **встроенных стилей** .</span><span class="sxs-lookup"><span data-stu-id="2f445-160">Complete the following actions to use **inline styles** to apply styles to a single element.</span></span>  

1.  <span data-ttu-id="2f445-161">Вернитесь на вкладку Правка и откройте окно `index.html` .</span><span class="sxs-lookup"><span data-stu-id="2f445-161">Go back to the editing tab and open `index.html`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-inline1.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-inline1.msft.png":::
       <span data-ttu-id="2f445-163">Открытие `index.html` на вкладке "Редактирование"</span><span class="sxs-lookup"><span data-stu-id="2f445-163">Open `index.html` in the editing tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="2f445-164">Добавить `style="background-color: aliceblue;"` в `<nav>` .</span><span class="sxs-lookup"><span data-stu-id="2f445-164">Add `style="background-color: aliceblue;"` to your `<nav>`.</span></span>  <span data-ttu-id="2f445-165">В блоке кода, приведенном ниже, четвертая строка кода имеет тот же адрес, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="2f445-165">In the code block below, the fourth line of code is the one you need to change.</span></span>  <span data-ttu-id="2f445-166">Остальное – это просто, так что вы можете сделать так, чтобы новый код замещается в нужном расположении.</span><span class="sxs-lookup"><span data-stu-id="2f445-166">The rest is just there, so you are able to ensure that you are putting the new code in the right place.</span></span>  
    
    ```html
    <header>
        <p>Welcome to my site!</p>
    </header>
    <nav style="background-color: aliceblue;">
        <ul>
            <li><a href="/">Home</a></li>
            ...
        ...
    ...
    ```  
    
1.  <span data-ttu-id="2f445-167">Перейдите на **вкладку динамический** , чтобы увидеть изменения.</span><span class="sxs-lookup"><span data-stu-id="2f445-167">Go to the **live tab** to see the changes!</span></span>  <span data-ttu-id="2f445-168">`<nav>`Теперь фон раздела синего цвета.</span><span class="sxs-lookup"><span data-stu-id="2f445-168">The background of the `<nav>` section is now blue.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-inline2.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-inline2.msft.png":::
       <span data-ttu-id="2f445-170">Цвет фона, который находится за **домашней страницей** и ссылками на **Контакты** , стал синей</span><span class="sxs-lookup"><span data-stu-id="2f445-170">The background color behind the **Home** and **Contact** links is now blue</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="2f445-171">Повторное использование стилей на одной странице с внутренними таблицами стилей</span><span class="sxs-lookup"><span data-stu-id="2f445-171">Re-use styles on a single page with internal stylesheets</span></span>  

<span data-ttu-id="2f445-172">В предыдущем фрагменте кода встроенный стиль применяет стиль для одного `<p>` тега.</span><span class="sxs-lookup"><span data-stu-id="2f445-172">In a previous code snippet, an inline style applied a style to a single `<p>` tag.</span></span>  

```html
<p style="border: 1px dashed red; padding: 5px;">
    This has been styled with CSS.
</p>
```  

<span data-ttu-id="2f445-173">Что делать, если вы хотите `<p>` , чтобы все элементы на веб-странице были применены таким же образом?</span><span class="sxs-lookup"><span data-stu-id="2f445-173">What if you wanted all of the `<p>` elements on your webpage to be styled the same way?</span></span>  <span data-ttu-id="2f445-174">Код необходимо скопировать и вставить в каждый один `<p>` тег на вашем сайте.</span><span class="sxs-lookup"><span data-stu-id="2f445-174">You would have to copy and paste the code into every single `<p>` tag on your site.</span></span>  <span data-ttu-id="2f445-175">Это немало времени и сил.</span><span class="sxs-lookup"><span data-stu-id="2f445-175">That is a lot of time and effort.</span></span>  <span data-ttu-id="2f445-176">Если вы хотите внести изменения, вам придется заново изменить все теги.</span><span class="sxs-lookup"><span data-stu-id="2f445-176">And, if you needed to make an edit, you would have to change every tag again.</span></span>  <span data-ttu-id="2f445-177">Выполните указанные ниже действия, чтобы использовать **внутреннюю таблицу стилей** для создания CSS, чтобы она применялась к нескольким элементам.</span><span class="sxs-lookup"><span data-stu-id="2f445-177">Complete the following actions to use an **Internal stylesheet** to write your CSS once so that it applies to multiple elements.</span></span>  

1.  <span data-ttu-id="2f445-178">На вкладке "динамический" нажмите " **контакт** ", чтобы перейти на страницу контакта.</span><span class="sxs-lookup"><span data-stu-id="2f445-178">In the live tab, choose **Contact** to go to the contact page.</span></span>  <span data-ttu-id="2f445-179">Обратите внимание на шрифт **домашних** и **контактных**данных.</span><span class="sxs-lookup"><span data-stu-id="2f445-179">Notice the font of **Home** and **Contact**.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-internal1.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-internal1.msft.png":::
       <span data-ttu-id="2f445-181">Страница "контакт"</span><span class="sxs-lookup"><span data-stu-id="2f445-181">The Contact page</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="2f445-182">На **вкладке "редактор**" перейдите в раздел `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="2f445-182">In the **editor tab**, go to `contact.html`.</span></span>  
1.  <span data-ttu-id="2f445-183">Добавьте следующий код `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="2f445-183">Add the following code to `contact.html`.</span></span>  <span data-ttu-id="2f445-184">Помните, что вам нужно добавить строки, начинающиеся с `<style>` и заканчивая данными `</style>` .</span><span class="sxs-lookup"><span data-stu-id="2f445-184">Remember, the lines starting with `<style>` and ending with `</style>` are what you need to add.</span></span>  <span data-ttu-id="2f445-185">Другой код — это только то, что вы знаете, где разместить новый код.</span><span class="sxs-lookup"><span data-stu-id="2f445-185">The other code is just there so you know where to put the new code.</span></span>  
    
    ```html
    ...
        <head>
            ...
            <meta name="viewport" content="width=device-width, initial-scale=1">
            <style>
                li a {
                  font-family: 'Courier New', Courier, Serif;
                }
            </style>
            ...
        </head>
        ...
    ...
    ```  
    
1.  <span data-ttu-id="2f445-186">Вернитесь на **вкладку динамический**.</span><span class="sxs-lookup"><span data-stu-id="2f445-186">Go back to the **live tab**.</span></span>  
1.  <span data-ttu-id="2f445-187">Нажмите кнопку " **контакт** ", чтобы вернуться на страницу контакта.</span><span class="sxs-lookup"><span data-stu-id="2f445-187">Choose **Contact** to go back to the contact page.</span></span>  <span data-ttu-id="2f445-188">Изменился шрифт " **Главная** " и " **контакт** ".</span><span class="sxs-lookup"><span data-stu-id="2f445-188">The font of **Home** and **Contact** has changed.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-internal2.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-internal2.msft.png":::
       <span data-ttu-id="2f445-190">Изменен шрифт ссылок на **домашнюю страницу** и **контакт контакта**</span><span class="sxs-lookup"><span data-stu-id="2f445-190">The font of the **Home** and **Contact** links has changed</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="2f445-191">Общие сведения о внутренних таблицах стилей</span><span class="sxs-lookup"><span data-stu-id="2f445-191">Understand internal stylesheets</span></span>  

<span data-ttu-id="2f445-192">Внутренние таблицы стилей. Примените стили с помощью **селекторов**.</span><span class="sxs-lookup"><span data-stu-id="2f445-192">Internal stylesheets apply styles using **selectors**.</span></span>  <span data-ttu-id="2f445-193">Селекторы — это шаблоны, которые могут применяться к одному или нескольким элементам HTML.</span><span class="sxs-lookup"><span data-stu-id="2f445-193">Selectors are patterns that may apply to one or more HTML elements.</span></span>  <span data-ttu-id="2f445-194">Предыдущий фрагмент кода добавил следующий стиль.</span><span class="sxs-lookup"><span data-stu-id="2f445-194">The previous code snippet added the following style.</span></span>  

```html
<style>
    li a {
      font-family: 'Courier New', Courier, Serif;
    }
</style>
```  

`li a` <span data-ttu-id="2f445-195">— Это селектор, который преобразуется в "любой `<li>` элемент, содержащий `<a>` элемент".</span><span class="sxs-lookup"><span data-stu-id="2f445-195">is a selector that translates to "any `<li>` element that contains an `<a>` element".</span></span>  <span data-ttu-id="2f445-196">Браузер изменит шрифт **домашних** и **контактных** ссылок, так как каждая из групп тегов соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="2f445-196">The browser changes the font of the **Home** and **Contact** links because each of the tag groups match the pattern.</span></span>  

```html
<li><a href="/">Home</a></li>
<li><a href="/contact.html">Contact</a></li>
```  

`font-family: 'Courier New', Courier, serif` <span data-ttu-id="2f445-197">является **объявлением**.</span><span class="sxs-lookup"><span data-stu-id="2f445-197">is a **declaration**.</span></span>  <span data-ttu-id="2f445-198">Объявление состоит из двух частей:</span><span class="sxs-lookup"><span data-stu-id="2f445-198">A declaration is made of following two parts.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="2f445-199">Property</span><span class="sxs-lookup"><span data-stu-id="2f445-199">property</span></span>**  
   :::column-end:::
   :::column span="1":::
      `font-family`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="2f445-200">Это свойство описывает общий способ изменения стиля элемента.</span><span class="sxs-lookup"><span data-stu-id="2f445-200">The property describes a general way that you are able to change the style of the element.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="2f445-201">value</span><span class="sxs-lookup"><span data-stu-id="2f445-201">value</span></span>**  
   :::column-end:::
   :::column span="1":::
      `'Courier New', Courier, serif`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="2f445-202">Значение точно описывает способ изменения стиля элемента.</span><span class="sxs-lookup"><span data-stu-id="2f445-202">The value describes exactly how the style of the element should change.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="2f445-203">Например, `font-family: 'Courier New', Courier, serif` предоставляет браузеру следующую инструкцию: "Установка шрифта для элементов, которые соответствуют шаблону `li a` `'Courier New'` .</span><span class="sxs-lookup"><span data-stu-id="2f445-203">For example, `font-family: 'Courier New', Courier, serif` gives the browser the following instruction:  "Set the font of elements that match the pattern `li a` to `'Courier New'`.</span></span>  <span data-ttu-id="2f445-204">Если этот шрифт недоступен, используйте `Courier` .</span><span class="sxs-lookup"><span data-stu-id="2f445-204">If that font is not available, use `Courier`.</span></span>  <span data-ttu-id="2f445-205">Если это недоступно, используйте `serif` ".</span><span class="sxs-lookup"><span data-stu-id="2f445-205">If that is not available, use `serif`."</span></span>  

### <span data-ttu-id="2f445-206">Добавление нескольких селекторов в набор правил</span><span class="sxs-lookup"><span data-stu-id="2f445-206">Add multiple selectors to a ruleset</span></span>  

<span data-ttu-id="2f445-207">Блок кода CSS вроде того, что вы видите ниже, называется набором **правил**.</span><span class="sxs-lookup"><span data-stu-id="2f445-207">A block of CSS code like what you see below is called a **ruleset**.</span></span>  

```css
li a {
  font-family: 'Courier New', Courier, monospace;
}
```  

<span data-ttu-id="2f445-208">Выполните следующие действия, чтобы добавить несколько селекторов в RuleSet с помощью запятых.</span><span class="sxs-lookup"><span data-stu-id="2f445-208">Complete the following actions to use commas to add multiple selectors to a ruleset.</span></span>  

1.  <span data-ttu-id="2f445-209">На **вкладке Редактор**откройте `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="2f445-209">In the **editor tab**, open `contact.html`.</span></span>  
1.  <span data-ttu-id="2f445-210">После `li a` ввода `, h1` .</span><span class="sxs-lookup"><span data-stu-id="2f445-210">After `li a` type `, h1`.</span></span>  
    
    ```html
    <style>
        li a, h1 {
          font-family: 'Courier New', Courier, Serif;
        }
    </style>
    ```  
    
    <span data-ttu-id="2f445-211">Предыдущий фрагмент кода указывает браузеру на элементы стиля `<h1>` таким же образом, как и элементы, которые соответствуют шаблону `li a` .</span><span class="sxs-lookup"><span data-stu-id="2f445-211">The previous code snippet tells the browser to style `<h1>` elements the same way that it styles elements that match the pattern `li a`.</span></span>  
    
1.  <span data-ttu-id="2f445-212">Перейдите на **вкладку динамический**.</span><span class="sxs-lookup"><span data-stu-id="2f445-212">Go to the **live tab**.</span></span>  
1.  <span data-ttu-id="2f445-213">Щелкните ссылку **контакт** , чтобы вернуться на страницу контакта.</span><span class="sxs-lookup"><span data-stu-id="2f445-213">Choose the **Contact** link to go back to the contact page.</span></span>  <span data-ttu-id="2f445-214">Теперь **свяжитесь со мной!**</span><span class="sxs-lookup"><span data-stu-id="2f445-214">Now, **Contact Me!**</span></span> <span data-ttu-id="2f445-215">имеет тот же шрифт, что и ссылки для навигации.</span><span class="sxs-lookup"><span data-stu-id="2f445-215">has the same font as the navigation links.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-multiple1.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-multiple1.msft.png":::
       <span data-ttu-id="2f445-218">Текстовые **Контакты!**</span><span class="sxs-lookup"><span data-stu-id="2f445-218">The text **Contact Me!**</span></span> <span data-ttu-id="2f445-219">Теперь тот же шрифт, что и ссылки на **домашнюю** и **контактный**</span><span class="sxs-lookup"><span data-stu-id="2f445-219">now has the same font as the **Home** and **Contact** links</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="2f445-220">Поэкспериментировать с DevTools</span><span class="sxs-lookup"><span data-stu-id="2f445-220">Experiment with DevTools</span></span>  

<span data-ttu-id="2f445-221">По мере того как вы продолжите свое путешествие, чтобы стать экспертом при разработке веб-приложений, возможно, вы обнаружите, что CSS очень сложны.</span><span class="sxs-lookup"><span data-stu-id="2f445-221">As you continue your journey to become an expert in web development, you may find that CSS is tricky.</span></span>  <span data-ttu-id="2f445-222">Вы можете написать каскадную таблицу стилей, чтобы она отображалась одним способом, но браузер делает что-то совершенно другое.</span><span class="sxs-lookup"><span data-stu-id="2f445-222">You may write some CSS and expect it to display one way, but the browser does something completely different.</span></span>  <span data-ttu-id="2f445-223">Microsoft Edge DevTools упрощает эксперименты с изменениями и немедленно показывает, как изменения повлияют на страницу.</span><span class="sxs-lookup"><span data-stu-id="2f445-223">Microsoft Edge DevTools makes it easy to experiment with changes and immediately see how the changes affect the page.</span></span>  

### <span data-ttu-id="2f445-224">Добавление объявления к существующему правилу в DevTools</span><span class="sxs-lookup"><span data-stu-id="2f445-224">Add a declaration to an existing rulest in DevTools</span></span>  

<span data-ttu-id="2f445-225">Выполните указанные ниже действия, чтобы выполнить итерацию по стилю существующего элемента, добавив объявление к существующему набору правил.</span><span class="sxs-lookup"><span data-stu-id="2f445-225">Complete the following actions to iterate on the style of an existing element, add a declaration to an existing ruleset.</span></span>  

1.  <span data-ttu-id="2f445-226">Наведите указатель мыши на **домашнюю** ссылку, откройте контекстное меню, а затем выберите команду **проверить**.</span><span class="sxs-lookup"><span data-stu-id="2f445-226">Hover on the **Home** link, open the contextual menu \(right-click\), and select **Inspect**.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-add1.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-add1.msft.png":::
       <span data-ttu-id="2f445-228">Проверка ссылки на домашнюю страницу</span><span class="sxs-lookup"><span data-stu-id="2f445-228">Inspect the Home link</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="2f445-229">DevTools открывается вместе со страницей.</span><span class="sxs-lookup"><span data-stu-id="2f445-229">DevTools opens up alongside your page.</span></span>  <span data-ttu-id="2f445-230">Код, представляющий ссылку на домашнюю страницу, `<a href="/">Home</a>` выделяется синим цветом в дереве DOM.</span><span class="sxs-lookup"><span data-stu-id="2f445-230">The code that represents the Home link, `<a href="/">Home</a>` is highlighted blue in the DOM Tree.</span></span>  <span data-ttu-id="2f445-231">Фрагмент кода и предварительный просмотр должны быть знакомы с тем, как начать [работу с HTML и моделью DOM][DevtoolsBeginnersHtml].</span><span class="sxs-lookup"><span data-stu-id="2f445-231">The code snippet and preview should be familiar from [Get Started with HTML and the DOM][DevtoolsBeginnersHtml].</span></span>  
    
    :::row:::
       :::column span="":::
          <span data-ttu-id="2f445-232">На приведенном ниже рисунке `font-family: 'Courier New', Courier, serif` объявление, добавленное ранее, отображается `contact.html` на вкладке **стили** под деревом DOM.</span><span class="sxs-lookup"><span data-stu-id="2f445-232">In the following figure, the `font-family: 'Courier New', Courier, serif` declaration that you previously added to `contact.html` is seen in the **Styles** tab below the DOM Tree.</span></span>  
          
          :::image type="complex" source="../media/beginners-css-add2.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-add2.msft.png":::
             <span data-ttu-id="2f445-234">Вкладка " **стили** " находится под ДЕРЕВОм DOM</span><span class="sxs-lookup"><span data-stu-id="2f445-234">The **Styles** tab is below the DOM Tree</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          <span data-ttu-id="2f445-235">Если окно DevTools является широкой страницей, вкладка стили находится справа от дерева DOM.</span><span class="sxs-lookup"><span data-stu-id="2f445-235">If your DevTools window is wide, the Styles tab is to the right of the DOM Tree.</span></span>  
          
          :::image type="complex" source="../media/beginners-css-add3.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-add3.msft.png":::
             <span data-ttu-id="2f445-237">Вкладка " **стили** " справа от дерева DOM</span><span class="sxs-lookup"><span data-stu-id="2f445-237">The **Styles** tab is to the right of the DOM Tree</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  <span data-ttu-id="2f445-238">Чтобы добавить новое объявление, выберите пустую строку ниже `font-family: 'Courier New', Courier, Serif` .</span><span class="sxs-lookup"><span data-stu-id="2f445-238">Choose the empty line below `font-family: 'Courier New', Courier, Serif` to add a new declaration.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-add4.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-add4.msft.png":::
       <span data-ttu-id="2f445-240">Добавление нового объявления</span><span class="sxs-lookup"><span data-stu-id="2f445-240">Add a new declaration</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="2f445-241">Введите текст `color` и выберите его `Enter` .</span><span class="sxs-lookup"><span data-stu-id="2f445-241">Type `color` and select `Enter`.</span></span>  <span data-ttu-id="2f445-242">Пользовательский интерфейс автозаполнения предлагает параметры по мере ввода.</span><span class="sxs-lookup"><span data-stu-id="2f445-242">The autocomplete UI suggests options as you type.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-add5.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-add5.msft.png":::
       <span data-ttu-id="2f445-244">Тип</span><span class="sxs-lookup"><span data-stu-id="2f445-244">Type</span></span> `color`  
    :::image-end:::  
    
1.  <span data-ttu-id="2f445-245">Введите текст `magenta` и выберите его `Enter` .</span><span class="sxs-lookup"><span data-stu-id="2f445-245">Type `magenta` and select `Enter`.</span></span>  <span data-ttu-id="2f445-246">Весь текст на странице контакта стал пурпурным.</span><span class="sxs-lookup"><span data-stu-id="2f445-246">All of the text on the contact page is now magenta.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-add6.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-add6.msft.png":::
       <span data-ttu-id="2f445-248">Тип</span><span class="sxs-lookup"><span data-stu-id="2f445-248">Type</span></span> `magenta`  
    :::image-end:::  
    
### <span data-ttu-id="2f445-249">Изменение объявления в DevTools</span><span class="sxs-lookup"><span data-stu-id="2f445-249">Edit a declaration in DevTools</span></span>  

<span data-ttu-id="2f445-250">Чтобы изменить существующие объявления в DevTools, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="2f445-250">Complete the following actions to edit existing declarations in DevTools.</span></span>  

1.  <span data-ttu-id="2f445-251">Выберите пурпурный квадрат рядом с `magenta` .</span><span class="sxs-lookup"><span data-stu-id="2f445-251">Choose the magenta square next to `magenta`.</span></span>  <span data-ttu-id="2f445-252">Появится палитра выбора цвета.</span><span class="sxs-lookup"><span data-stu-id="2f445-252">A color picker pops up.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-edit1.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-edit1.msft.png":::
       <span data-ttu-id="2f445-254">Выбор цвета</span><span class="sxs-lookup"><span data-stu-id="2f445-254">The Color Picker</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="2f445-255">С помощью средства выбора цвета измените текст шрифта на нужный цвет.</span><span class="sxs-lookup"><span data-stu-id="2f445-255">Use the color picker to change the font text to a color that you like.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-edit2.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-edit2.msft.png":::
       <span data-ttu-id="2f445-257">Изменение цвета шрифта на фиолетовый с помощью средства выбора цвета</span><span class="sxs-lookup"><span data-stu-id="2f445-257">Change the font color to purple with the Color Picker</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="2f445-258">Добавление нового набора правил в DevTools</span><span class="sxs-lookup"><span data-stu-id="2f445-258">Add a new ruleset in DevTools</span></span>  

<span data-ttu-id="2f445-259">Чтобы добавить новые наборы правил в DevTools, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="2f445-259">Complete the following actions to add new rulesets in DevTools.</span></span>  

1.  <span data-ttu-id="2f445-260">Выберите **новое правило стиля** \ ( ![ новое правило стиля ][ImageNewStyleRuleIcon] \), которое находится рядом с **. CLS**.</span><span class="sxs-lookup"><span data-stu-id="2f445-260">Choose **New Style Rule** \(![New Style Rule][ImageNewStyleRuleIcon]\) which is next to **.cls**.</span></span>  <span data-ttu-id="2f445-261">В качестве Selector появится пустой набор правил `a` .</span><span class="sxs-lookup"><span data-stu-id="2f445-261">An empty ruleset appears with `a` as the selector.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-rule1.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-rule1.msft.png":::
       <span data-ttu-id="2f445-263">Добавление нового правила</span><span class="sxs-lookup"><span data-stu-id="2f445-263">Add a new rule</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="2f445-264">Заменить `a` на `a:hover` .</span><span class="sxs-lookup"><span data-stu-id="2f445-264">Replace `a` with `a:hover`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-rule2.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-rule2.msft.png":::
       <span data-ttu-id="2f445-266">Заменить `a` на</span><span class="sxs-lookup"><span data-stu-id="2f445-266">Replace `a` with</span></span> `a:hover`  
    :::image-end:::  
    
    `:hover` <span data-ttu-id="2f445-267">является **псевдо-классом**.</span><span class="sxs-lookup"><span data-stu-id="2f445-267">is a **pseudo-class**.</span></span>  <span data-ttu-id="2f445-268">Используйте псевдо-классы для элементов стиля, которые могут вводить особые состояния.</span><span class="sxs-lookup"><span data-stu-id="2f445-268">Use pseudo-classes for style elements that may enter special states.</span></span>  <span data-ttu-id="2f445-269">Например, `a:hover` стиль вступает в силу только при наведении указателя мыши на `<a>` элемент.</span><span class="sxs-lookup"><span data-stu-id="2f445-269">For example, the `a:hover` style only takes effect when you are hovering over an `<a>` element.</span></span>  
    
1.  <span data-ttu-id="2f445-270">Выберите между скобками, чтобы добавить новое объявление.</span><span class="sxs-lookup"><span data-stu-id="2f445-270">Choose between the brackets to add a new declaration.</span></span>  
1.  <span data-ttu-id="2f445-271">Введите `background-color` имя объявления и нажмите кнопку `Enter` .</span><span class="sxs-lookup"><span data-stu-id="2f445-271">Type `background-color` for the declaration name and select `Enter`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-rule3.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-rule3.msft.png":::
       <span data-ttu-id="2f445-273">Тип</span><span class="sxs-lookup"><span data-stu-id="2f445-273">Type</span></span> `background-color`  
    :::image-end:::  
    
1.  <span data-ttu-id="2f445-274">Введите `green` значение объявления и нажмите кнопку `Enter` .</span><span class="sxs-lookup"><span data-stu-id="2f445-274">Type `green` for the declaration value and select `Enter`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-rule4.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-rule4.msft.png":::
       <span data-ttu-id="2f445-276">Тип</span><span class="sxs-lookup"><span data-stu-id="2f445-276">Type</span></span> `green`  
    :::image-end:::  
    
1.  <span data-ttu-id="2f445-277">Наведите указатель мыши на ссылку " **Домашняя страница** ".</span><span class="sxs-lookup"><span data-stu-id="2f445-277">Hover your mouse over the **Home** link.</span></span>  <span data-ttu-id="2f445-278">Фон ссылки становится зеленым.</span><span class="sxs-lookup"><span data-stu-id="2f445-278">The background of the link turns green.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-rule5.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-rule5.msft.png":::
       <span data-ttu-id="2f445-280">Наведите указатель мыши на домашнюю ссылку, чтобы отобразить зеленый фон</span><span class="sxs-lookup"><span data-stu-id="2f445-280">Hover over the Home link to reveal its green background</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="2f445-281">Повторное использование стилей на разных страницах с внешними таблицами стилей</span><span class="sxs-lookup"><span data-stu-id="2f445-281">Re-use styles across pages with external stylesheets</span></span>  

<span data-ttu-id="2f445-282">На предыдущем этапе вы добавили следующий фрагмент кода в качестве внутренней таблицы стилей `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="2f445-282">In a previous step, you added the following code snippet as an internal stylesheet to `contact.html`.</span></span>  

```html
...
    ...
        ...
        <style>
            li a, h1 {
              font-family: 'Courier New', Courier, Serif;
            }
        </style>
        ...
    ...
...
```  

<span data-ttu-id="2f445-283">Что делать, если вы захотите стиль `index.html` одинаково?</span><span class="sxs-lookup"><span data-stu-id="2f445-283">What if you wanted to style `index.html` the same way?</span></span>  <span data-ttu-id="2f445-284">Что делать, если вы хотите применить стили к большому количеству страниц?</span><span class="sxs-lookup"><span data-stu-id="2f445-284">What if you had a large number of pages to which you wanted to apply your styles?</span></span>  <span data-ttu-id="2f445-285">Необходимо скопировать и вставить внутреннюю таблицу стилей в каждую веб-страницу на сайте.</span><span class="sxs-lookup"><span data-stu-id="2f445-285">You would have to copy and paste the internal stylesheet into every single web page on your site.</span></span>  <span data-ttu-id="2f445-286">Выполните указанные ниже действия, чтобы добавить **внешнюю таблицу стилей** , которая позволит вам создавать CSS один раз и применять ее к нескольким страницам.</span><span class="sxs-lookup"><span data-stu-id="2f445-286">Complete the following actions to add an **External stylesheet** to allow you to write your CSS once and apply it to multiple pages.</span></span>  

1.  <span data-ttu-id="2f445-287">Сначала перезагрузите вкладку Live, чтобы удалить изменения, внесенные в DevTools.</span><span class="sxs-lookup"><span data-stu-id="2f445-287">First, reload the live tab to remove the changes that you made in DevTools.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external1.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-external1.msft.png":::
        <span data-ttu-id="2f445-289">После обновления страницы изменения, внесенные в DevTools, исчезают</span><span class="sxs-lookup"><span data-stu-id="2f445-289">After you refresh the page, the changes that were made in DevTools are gone</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="2f445-290">Вернитесь на **вкладку Редактор** и откройте ее `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="2f445-290">Go back to the **editor tab** and open `contact.html`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external2.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-external2.msft.png":::
       <span data-ttu-id="2f445-292">contact.html</span><span class="sxs-lookup"><span data-stu-id="2f445-292">contact.html</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="2f445-293">Удалить все между `<style>` и `</style>` , включая `<style>` и `</style>` .</span><span class="sxs-lookup"><span data-stu-id="2f445-293">Delete everything between `<style>` and `</style>`, including `<style>` and `</style>`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external3.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-external3.msft.png":::
       <span data-ttu-id="2f445-295">Тег Style был удален</span><span class="sxs-lookup"><span data-stu-id="2f445-295">The style tag has been removed</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="2f445-296">Перейдите к `index.html` тегу и удалите `style="background-color: aliceblue;"` его `<nav>` .</span><span class="sxs-lookup"><span data-stu-id="2f445-296">Go to `index.html` and remove `style="background-color: aliceblue;"` from the `<nav>` tag.</span></span>  <span data-ttu-id="2f445-297">Теперь вы удалили все CSS-таблицы, которые вы ранее добавили на сайт.</span><span class="sxs-lookup"><span data-stu-id="2f445-297">You have now removed all of the CSS that you previously added to your site.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external4.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-external4.msft.png":::
       <span data-ttu-id="2f445-299">Встроенный стиль удален из элемента навигации</span><span class="sxs-lookup"><span data-stu-id="2f445-299">The inline style has been removed from the nav element</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="2f445-300">Выберите команду **создать файл**.</span><span class="sxs-lookup"><span data-stu-id="2f445-300">Choose **New File**.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external5.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-external5.msft.png":::
       <span data-ttu-id="2f445-302">Диалоговое окно "Создание файла"</span><span class="sxs-lookup"><span data-stu-id="2f445-302">The new file dialog</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="2f445-303">Замените `cool-file.js` на `style.css` и выберите команду **Добавить файл**.</span><span class="sxs-lookup"><span data-stu-id="2f445-303">Replace `cool-file.js` with `style.css` and choose **Add File**.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external6.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-external6.msft.png":::
       <span data-ttu-id="2f445-305">Тип</span><span class="sxs-lookup"><span data-stu-id="2f445-305">Type</span></span> `style.css`  
    :::image-end:::  
    
1.  <span data-ttu-id="2f445-306">Добавьте в файл следующий фрагмент кода `style.css` .</span><span class="sxs-lookup"><span data-stu-id="2f445-306">Add the following code snippet to your `style.css` file.</span></span>  
    
    ```css
    li a, h1 {
      font-family: 'Courier New', Courier, Serif;
    }
    a:hover {
      background-color: green;
    }
    nav {
      background-color: aliceblue;
    }
    ```  
    
    :::image type="complex" source="../media/beginners-css-external7.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-external7.msft.png":::
       <span data-ttu-id="2f445-308">Добавление кода в</span><span class="sxs-lookup"><span data-stu-id="2f445-308">Add code to</span></span> `style.css`  
    :::image-end:::  
    
    <span data-ttu-id="2f445-309">Убедитесь, что создана внешняя таблица стилей.</span><span class="sxs-lookup"><span data-stu-id="2f445-309">Ensure that you have created an external stylesheet.</span></span> <span data-ttu-id="2f445-310">Ваш HTML-код не знает, что он существует.</span><span class="sxs-lookup"><span data-stu-id="2f445-310">Your HTML is not aware that it exists.</span></span>  
    
1.  <span data-ttu-id="2f445-311">Open (открыть) `index.html` .</span><span class="sxs-lookup"><span data-stu-id="2f445-311">Open `index.html`.</span></span>  
1.  <span data-ttu-id="2f445-312">Добавьте `<link rel="stylesheet" href="style.css">` в свой HTML-код.</span><span class="sxs-lookup"><span data-stu-id="2f445-312">Add `<link rel="stylesheet" href="style.css">` to your HTML.</span></span>  
    
    ```html
    <head>
        ...
        <meta name="viewport" content="width=device-width, initial-scale=1">
        <link rel="stylesheet" href="style.css">
    </head>
    ```  
    
    :::image type="complex" source="../media/beginners-css-external8.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-external8.msft.png":::
       <span data-ttu-id="2f445-314">Ссылка на</span><span class="sxs-lookup"><span data-stu-id="2f445-314">Link to</span></span> `style.css`  
    :::image-end:::  
    
1.  <span data-ttu-id="2f445-315">Откройте `contact.html` файл и добавьте ссылку на него.</span><span class="sxs-lookup"><span data-stu-id="2f445-315">Open the `contact.html` file and add the link there.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external9.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-external9.msft.png":::
       <span data-ttu-id="2f445-317">Ссылка `style.css` в</span><span class="sxs-lookup"><span data-stu-id="2f445-317">Link to `style.css` in</span></span> `contact.html`  
    :::image-end:::  
    
1.  <span data-ttu-id="2f445-318">Перейдите на **вкладку динамический**.  Домашняя страница теперь имеет тот же шрифт, что и в последнем разделе, и в синем разделе навигации.</span><span class="sxs-lookup"><span data-stu-id="2f445-318">Go to the **live tab**.  The home page now has the same font from the last section and a blue navigation section.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external10.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-external10.msft.png":::
       <span data-ttu-id="2f445-320">Домашняя страница</span><span class="sxs-lookup"><span data-stu-id="2f445-320">The home page</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="2f445-321">Щелкните ссылку **контакт** , чтобы перейти на страницу контакта.</span><span class="sxs-lookup"><span data-stu-id="2f445-321">Choose the **Contact** link to go to the contact page.</span></span>  <span data-ttu-id="2f445-322">Страница контакта имеет тот же формат, что и домашняя страница.</span><span class="sxs-lookup"><span data-stu-id="2f445-322">The contact page has the same formatting as the home page.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external11.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-external11.msft.png":::
       <span data-ttu-id="2f445-324">Страница "контакт"</span><span class="sxs-lookup"><span data-stu-id="2f445-324">The contact page</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="2f445-325">Использование платформы CSS</span><span class="sxs-lookup"><span data-stu-id="2f445-325">Use a CSS framework</span></span>  

<span data-ttu-id="2f445-326">**Платформы CSS** — это коллекции стилей, разработанных другими разработчиками, которые упрощают создание привлекательных веб-сайтов.</span><span class="sxs-lookup"><span data-stu-id="2f445-326">**CSS frameworks** are collections of styles built by other developers that make it easier to create attractive web sites.</span></span>  <span data-ttu-id="2f445-327">Вместо того чтобы определять стили самостоятельно, платформа предоставляет коллекцию стилей, которые вы можете использовать в элементах страницы.</span><span class="sxs-lookup"><span data-stu-id="2f445-327">Instead of defining styles yourself, a framework provides you a collection of styles that you are able to use on your page elements.</span></span>  

1.  <span data-ttu-id="2f445-328">Скопируйте приведенный ниже код.</span><span class="sxs-lookup"><span data-stu-id="2f445-328">Copy the following code:</span></span>  
    
    ```html
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.1/css/bootstrap.min.css">
    ```  
    
1.  <span data-ttu-id="2f445-329">Перейдите на вкладку Правка и вставьте код в `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="2f445-329">Go to the editing tab and paste the code into `contact.html`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-framework1.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-framework1.msft.png":::
       <span data-ttu-id="2f445-331">Ссылка на платформу в</span><span class="sxs-lookup"><span data-stu-id="2f445-331">Link to the framework in</span></span> `contact.html`  
    :::image-end:::  
    
1.  <span data-ttu-id="2f445-332">Откройте `index.html` файл и добавьте в него код.</span><span class="sxs-lookup"><span data-stu-id="2f445-332">Open the `index.html` file and add the code there.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-framework2.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-framework2.msft.png":::
       <span data-ttu-id="2f445-334">Ссылка на платформу в</span><span class="sxs-lookup"><span data-stu-id="2f445-334">Link to the framework in</span></span> `index.html`  
    :::image-end:::  
    
1.  <span data-ttu-id="2f445-335">Вернитесь на вкладку динамический, чтобы просмотреть изменения.</span><span class="sxs-lookup"><span data-stu-id="2f445-335">Go back to the live tab to view your changes.</span></span>  <span data-ttu-id="2f445-336">Несмотря на то, что цвет фона `<nav>` элемента и шрифта `<li>` `<a>` элементов and одинаков, изменился шрифт остальных элементов.</span><span class="sxs-lookup"><span data-stu-id="2f445-336">While the background color of the `<nav>` element and the font of the `<li>` and `<a>` elements are the same, the font of the other elements has changed.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-framework3.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-framework3.msft.png":::
       <span data-ttu-id="2f445-338">Некоторые шрифты на домашней странице изменились из-за платформы</span><span class="sxs-lookup"><span data-stu-id="2f445-338">Some of the font on the home page changed because of the framework</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="2f445-339">Использование класса</span><span class="sxs-lookup"><span data-stu-id="2f445-339">Use a class</span></span>  

<span data-ttu-id="2f445-340">В последнем разделе вы добавили начальную загрузку на веб-страницы, которая изменила шрифты для некоторых элементов на вашем сайте.</span><span class="sxs-lookup"><span data-stu-id="2f445-340">In the last section, you added Bootstrap to your web pages, which changed the fonts of some of the elements on your site.</span></span>  <span data-ttu-id="2f445-341">Структуры CSS помогают вносить существенные изменения на странице с помощью очень небольшого количества кода.</span><span class="sxs-lookup"><span data-stu-id="2f445-341">CSS frameworks help you make major changes to your page with very little code.</span></span>  <span data-ttu-id="2f445-342">Чтобы изменить верхний колонтитул, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="2f445-342">Complete the following actions to change your header.</span></span>  

1.  <span data-ttu-id="2f445-343">Скопируйте следующий фрагмент кода.</span><span class="sxs-lookup"><span data-stu-id="2f445-343">Copy the following code snippet.</span></span>  
    
    ```html
    class="jumbotron jumbotron-fluid"  
    ```  
    
1.  <span data-ttu-id="2f445-344">Добавьте предыдущий фрагмент кода в `<header>` тег `index.html` .</span><span class="sxs-lookup"><span data-stu-id="2f445-344">Add the previous code snippet to your `<header>` tag in `index.html`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-jumbotron1.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-jumbotron1.msft.png":::
       <span data-ttu-id="2f445-346">Добавление классов в</span><span class="sxs-lookup"><span data-stu-id="2f445-346">Add classes in</span></span> `index.html`  
    :::image-end:::  
    
1.  <span data-ttu-id="2f445-347">Добавьте код в `<header>` тег `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="2f445-347">Add the code to your `<header>` tag in `contact.html`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-jumbotron2.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-jumbotron2.msft.png":::
       <span data-ttu-id="2f445-349">Добавление классов в</span><span class="sxs-lookup"><span data-stu-id="2f445-349">Add classes in</span></span> `contact.html`  
    :::image-end:::  
    
1.  <span data-ttu-id="2f445-350">Просмотрите изменения на вкладке "живые".  Вокруг заголовка есть большое затененное поле.</span><span class="sxs-lookup"><span data-stu-id="2f445-350">View your changes in the live tab.  There is a big, grey box around your header.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-jumbotron3.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-jumbotron3.msft.png":::
       <span data-ttu-id="2f445-352">Теперь верхний колонтитул имеет большой серый прямоугольник вокруг него.</span><span class="sxs-lookup"><span data-stu-id="2f445-352">The header now has a big, grey box around it</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="2f445-353">Общие сведения о классах</span><span class="sxs-lookup"><span data-stu-id="2f445-353">Understand classes</span></span>  

<span data-ttu-id="2f445-354">Классы позволяют назначать коллекции стилей произвольным элементам.</span><span class="sxs-lookup"><span data-stu-id="2f445-354">Classes let you assign collections of styles to arbitrary elements.</span></span>  <span data-ttu-id="2f445-355">Используйте следующий фрагмент кода, чтобы применить к `<header>` элементу несколько стилей после присвоения `class` атрибуту значения `jumbotron` .</span><span class="sxs-lookup"><span data-stu-id="2f445-355">Use the following code snippet to apply several styles to the `<header>` element after you set the `class` attribute to `jumbotron`.</span></span>  

```css
.jumbotron {
  padding: 2rem 1rem;
  margin-bottom: 2rem;
  background-color: #e9ecef;
  border-radius: .3rem;
}
```  

<span data-ttu-id="2f445-356">Одно из преимуществ класса состоит в том, что он позволяет применять стили к любым нужным элементам.</span><span class="sxs-lookup"><span data-stu-id="2f445-356">One advantage of a class is that it lets you apply styles to whatever elements you want.</span></span>  <span data-ttu-id="2f445-357">Например, предположим, что вам нужно установить для некоторых элементов цвет фона `<p>` , который будет фиолетовым, но не все `<p>` элементы.</span><span class="sxs-lookup"><span data-stu-id="2f445-357">For example, suppose you want to set the background color of some `<p>` elements to purple, but not all `<p>` elements.</span></span>  <span data-ttu-id="2f445-358">Используйте следующий фрагмент кода, чтобы определить стиль в классе.</span><span class="sxs-lookup"><span data-stu-id="2f445-358">Use the following code snippet to define the style in a class.</span></span>  

```css
.custom-background {
  background-color: purple;
}
```  

<span data-ttu-id="2f445-359">Затем примените класс только к тем `<p>` элементам, для которых вы хотите применить стиль.</span><span class="sxs-lookup"><span data-stu-id="2f445-359">Next, apply the class to only the `<p>` elements that you want to style.</span></span>  

```html
<p>The text is not purple.</p>
<p class="custom-background">The text is purple.</p>
<p>The text is not purple.</p>
<p class="custom-background">The text is purple.</p>
```  

### <span data-ttu-id="2f445-360">Выравнивание элементов</span><span class="sxs-lookup"><span data-stu-id="2f445-360">Align elements</span></span>  

<span data-ttu-id="2f445-361">Выполните указанные ниже действия, чтобы выполнить загрузку и предоставить классы для выравнивания элементов.</span><span class="sxs-lookup"><span data-stu-id="2f445-361">Complete the following actions to bootstrap and provide classes for aligning elements.</span></span>  

1.  <span data-ttu-id="2f445-362">Вернитесь на вкладку Редактор и откройте ее `index.html` .</span><span class="sxs-lookup"><span data-stu-id="2f445-362">Go back to the editor tab and open `index.html`.</span></span>  
1.  <span data-ttu-id="2f445-363">Добавьте `class="container-fluid"` в свой `<body>` тег.</span><span class="sxs-lookup"><span data-stu-id="2f445-363">Add `class="container-fluid"` to your `<body>` tag.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-align1.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-align1.msft.png":::
       <span data-ttu-id="2f445-365">Добавьте `container-fluid` класс</span><span class="sxs-lookup"><span data-stu-id="2f445-365">Add the `container-fluid` class</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="2f445-366">Обтекание `<nav>` `<main>` элементов `<div class="row">` .</span><span class="sxs-lookup"><span data-stu-id="2f445-366">Wrap your `<nav>` and `<main>` elements in `<div class="row">`.</span></span>  <span data-ttu-id="2f445-367">`</div>`Чтобы правильно закрыть новый тег, убедитесь в том, что вы хотите сделать `</main>` это.</span><span class="sxs-lookup"><span data-stu-id="2f445-367">Make sure to put `</div>` after `</main>` in order to properly close the new tag.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-align2.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-align2.msft.png":::
       <span data-ttu-id="2f445-369">Добавление строки</span><span class="sxs-lookup"><span data-stu-id="2f445-369">Add a row</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="2f445-370">Добавьте `class="col-3"` теги в тег `<nav>` и `class="col-9"` в `<main>` тег.</span><span class="sxs-lookup"><span data-stu-id="2f445-370">Add `class="col-3"` to your `<nav>` tag and `class="col-9"` to your `<main>` tag.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-align3.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-align3.msft.png":::
       <span data-ttu-id="2f445-372">Добавление `col-3` классов и `col-9`</span><span class="sxs-lookup"><span data-stu-id="2f445-372">Add the `col-3` and `col-9` classes</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="2f445-373">Просмотрите изменения на вкладке "живые".</span><span class="sxs-lookup"><span data-stu-id="2f445-373">View your changes in the live tab.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-align4.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-align4.msft.png":::
       <span data-ttu-id="2f445-375">Содержимое элемента навигации теперь находится слева от основного содержимого.</span><span class="sxs-lookup"><span data-stu-id="2f445-375">The nav content is now to the left of the main content</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="2f445-376">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="2f445-376">Next steps</span></span>  

<span data-ttu-id="2f445-377">Поздравляем, вы закончите.</span><span class="sxs-lookup"><span data-stu-id="2f445-377">Congratulations, you are done.</span></span>  

*   <span data-ttu-id="2f445-378">Лучший способ улучшить качество веб-приложений — создать дополнительные сайты.</span><span class="sxs-lookup"><span data-stu-id="2f445-378">The best way to get better at web development is to build more sites.</span></span>  <span data-ttu-id="2f445-379">Не беспокойтесь о нарушениях.</span><span class="sxs-lookup"><span data-stu-id="2f445-379">Do not worry about breaking stuff.</span></span>  <span data-ttu-id="2f445-380">Просто восприятие и обучение очень удобно.</span><span class="sxs-lookup"><span data-stu-id="2f445-380">Just have fun and learn as much as possible along the way.</span></span>  
*   <span data-ttu-id="2f445-381">Чтобы узнать больше о стилях веб-страниц, ознакомьтесь со статьей общие сведения о [CSS][MDNCssFirstSteps].</span><span class="sxs-lookup"><span data-stu-id="2f445-381">To learn more about styling web pages, see [Introduction to CSS][MDNCssFirstSteps].</span></span>  
*   <span data-ttu-id="2f445-382">Дополнительные сведения о том, как использовать DevTools для экспериментов с CSS-страницей, можно найти в статье Начало [работы с помощью просмотра и изменения CSS][DevtoolsCssIndex].</span><span class="sxs-lookup"><span data-stu-id="2f445-382">To learn more about how to use DevTools to experiment with the CSS of a page, see [Get Started with Viewing and Changing CSS][DevtoolsCssIndex].</span></span>  

<!--- image links --->  

[ImageNewStyleRuleIcon]: ../media/new-style-rule-icon.msft.png  

<!--- links  --->  

[DevtoolsBeginnersHtml]: ./html.md "DevTools для начинающих: Приступая к работе с HTML и моделью DOM | Документы Microsoft"  
[DevtoolsCssIndex]: ../css/index.md "Начало просмотра и изменения CSS | Документы Microsoft"  

[MicrosoftEdgeInsider]: https://www.microsoftedgeinsider.com "Предварительная оценка Microsoft Edge"  

[GlitchCookedAmphibianIndex]: https://glitch.com/edit/#!/cooked-amphibian?path=index.html "index.html-готовил-amphibian | Цепь"  

[MDNCssFirstSteps]: https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS "Первые шаги CSS | MDN"  

> [!NOTE]
> <span data-ttu-id="2f445-388">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="2f445-388">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="2f445-389">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/beginners/css) и [Katherine Джексон][KatherineJackson] \ (помощник службы технической поддержки, Chrome DevTools \).</span><span class="sxs-lookup"><span data-stu-id="2f445-389">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/beginners/css) and is authored by [Katherine Jackson][KatherineJackson] \(Technical Writer Intern, Chrome DevTools\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="2f445-391">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="2f445-391">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[KatherineJackson]: https://developers.google.com/web/resources/contributors/katjackson  
