---
description: Исчерпывающая Справка по специальным возможностям в Microsoft Edge DevTools.
title: Справка по специальным возможностям
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: de8f4bee6fef7725af9b97fb80ab45582dfa2286
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125316"
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

# <span data-ttu-id="d6728-104">Справка по специальным возможностям</span><span class="sxs-lookup"><span data-stu-id="d6728-104">Accessibility reference</span></span>  

<span data-ttu-id="d6728-105">Эта страница является исчерпывающей ссылкой на специальные возможности в Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="d6728-105">This page is a comprehensive reference of accessibility features in Microsoft Edge DevTools.</span></span>  <span data-ttu-id="d6728-106">Оно предназначено для веб-разработчиков, которые:</span><span class="sxs-lookup"><span data-stu-id="d6728-106">It is intended for web developers who:</span></span>  

*   <span data-ttu-id="d6728-107">Разработайте основные принципы DevTools, например, как открыть ее.</span><span class="sxs-lookup"><span data-stu-id="d6728-107">Have a basic understanding of DevTools, such as how to open it.</span></span>  
*   <span data-ttu-id="d6728-108">Знакомы с [принципами специальных возможностей и][MDNAccessibility]рекомендациями.</span><span class="sxs-lookup"><span data-stu-id="d6728-108">Are familiar with [accessibility principles and best practices][MDNAccessibility].</span></span>  
    
<span data-ttu-id="d6728-109">Цель этой ссылки — помочь вам найти все средства, доступные в DevTools, которые помогут вам изучить специальные возможности на странице.</span><span class="sxs-lookup"><span data-stu-id="d6728-109">The purpose of this reference is to help you discover all of the tools available in DevTools that help you examine the accessibility of a page.</span></span>  

<span data-ttu-id="d6728-110">Если вы ищете справку по переходу на DevTools с помощью специальных возможностей, таких как средство чтения с экрана, вы узнаете о том, что нужно сделать для навигации по [Microsoft Edge DevTools с технологией специальных возможностей][DevtoolsAccessibilityNavigation] .</span><span class="sxs-lookup"><span data-stu-id="d6728-110">See [Navigating Microsoft Edge DevTools With Assistive Technology][DevtoolsAccessibilityNavigation] if you are looking for help on navigating DevTools with an assistive technology like a screen reader.</span></span>  

## <span data-ttu-id="d6728-111">Общие сведения о специальных возможностях в Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="d6728-111">Overview of accessibility features in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="d6728-112">В этом разделе объясняется, как DevTools в общий набор средств для специальных возможностей.</span><span class="sxs-lookup"><span data-stu-id="d6728-112">This section explains how DevTools fits into your overall accessibility toolkit.</span></span>  

<span data-ttu-id="d6728-113">Если вы решите, что страница доступна, вам нужно будет 2 общих вопросов.</span><span class="sxs-lookup"><span data-stu-id="d6728-113">When determining whether a page is accessible, you need to have 2 general questions in mind:</span></span>  

1.  <span data-ttu-id="d6728-114">Вы можете перемещаться по странице с помощью клавиатуры или [средства чтения с экрана][MDNScreenReader]?</span><span class="sxs-lookup"><span data-stu-id="d6728-114">Are you able to navigate the page with a keyboard or [screen reader][MDNScreenReader]?</span></span>  
1.  <span data-ttu-id="d6728-115">Правильно ли помечены элементы страницы для средств чтения с экрана?</span><span class="sxs-lookup"><span data-stu-id="d6728-115">Are the elements of the page properly marked up for screen readers?</span></span>  
    
<span data-ttu-id="d6728-116">Как правило, DevTools поможет устранить ошибки, связанные с вопросами #2, так как эти ошибки легко выявить автоматически.</span><span class="sxs-lookup"><span data-stu-id="d6728-116">In general, DevTools should help you fix errors related to question #2, because these errors are easy to detect in an automated fashion.</span></span>  <span data-ttu-id="d6728-117">Вопрос #1 так же важен, но, к сожалению, DevTools не поможет вам.</span><span class="sxs-lookup"><span data-stu-id="d6728-117">Question #1 is just as important, but unfortunately DevTools does not help you there.</span></span>  <span data-ttu-id="d6728-118">Единственный способ найти ошибки, связанные с вопросом #1, — попытаться использовать страницу с помощью клавиатуры или средства чтения с экрана самостоятельно.</span><span class="sxs-lookup"><span data-stu-id="d6728-118">The only way to find errors related to question #1 is to try using a page with a keyboard or screen reader yourself.</span></span>  <!--See [How To Do An Accessibility Review][AccessibilityReview] to learn more.  -->  

<!--[AccessibilityReview]: /web/fundamentals/accessibility/how-to-review  -->  

## <span data-ttu-id="d6728-119">Аудит специальных возможностей страницы</span><span class="sxs-lookup"><span data-stu-id="d6728-119">Audit the accessibility of a page</span></span>  

> [!NOTE]
> <span data-ttu-id="d6728-120">Панель **Аудит** содержит ссылки на содержимое, размещенное на сторонних веб-сайтах.</span><span class="sxs-lookup"><span data-stu-id="d6728-120">The **Audits** panel provides links to content hosted on third-party websites.</span></span>  <span data-ttu-id="d6728-121">Корпорация Майкрософт не несет ответственности за контент этих сайтов и любые данные, которые могут быть собраны, и не может контролировать их.</span><span class="sxs-lookup"><span data-stu-id="d6728-121">Microsoft is not responsible for and has no control over the content of these sites and any data that may be collected.</span></span>  

<span data-ttu-id="d6728-122">Как правило, с помощью панели аудит вы можете определить, есть ли в следующих случаях:</span><span class="sxs-lookup"><span data-stu-id="d6728-122">In general, use the Audits panel to determine if:</span></span>  

*   <span data-ttu-id="d6728-123">Страница правильно помечена для средств чтения с экрана.</span><span class="sxs-lookup"><span data-stu-id="d6728-123">A page is properly marked up for screen readers.</span></span>  
*   <span data-ttu-id="d6728-124">Элементы текста на странице имеют достаточные коэффициенты контрастности.</span><span class="sxs-lookup"><span data-stu-id="d6728-124">The text elements on a page have sufficient contrast ratios.</span></span>  <span data-ttu-id="d6728-125">Посмотрите [Просмотр коэффициента контрастности текстового элемента в средстве выбора цвета](#view-the-contrast-ratio-of-a-text-element-in-the-color-picker).</span><span class="sxs-lookup"><span data-stu-id="d6728-125">See [View the contrast ratio of a text element in the Color Picker](#view-the-contrast-ratio-of-a-text-element-in-the-color-picker).</span></span>  

<span data-ttu-id="d6728-126">Чтобы выполнить аудит страницы, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="d6728-126">To audit a page:</span></span>  

1.  <span data-ttu-id="d6728-127">Перейдите к URL-адресу, на который вы хотите подвестись.</span><span class="sxs-lookup"><span data-stu-id="d6728-127">Go to the URL that you want to audit.</span></span>  
1.  <span data-ttu-id="d6728-128">В DevTools откройте вкладку **аудитория** .  DevTools показывает различные параметры конфигурации.</span><span class="sxs-lookup"><span data-stu-id="d6728-128">In DevTools, click the **Audits** tab.  DevTools shows you various configuration options.</span></span>  
    
    :::image type="complex" source="../media/accessibility-audits-pane.msft.png" alt-text="Настройка аудита" lightbox="../media/accessibility-audits-pane.msft.png":::
       <span data-ttu-id="d6728-130">Настройка аудита</span><span class="sxs-lookup"><span data-stu-id="d6728-130">Configure audits</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="d6728-131">Снимки экрана в этом разделе собраны в версии 79 Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="d6728-131">The screenshots in this section were taken with version 79 of Microsoft Edge.</span></span>  <span data-ttu-id="d6728-132">Вы можете проверить, на какой версии вы работаете `edge://version` .</span><span class="sxs-lookup"><span data-stu-id="d6728-132">You may check what version you are running at `edge://version`.</span></span>  <span data-ttu-id="d6728-133">В более ранних версиях Microsoft Edge пользовательский интерфейс панели **аудита** выглядит иначе, но общий рабочий процесс одинаков.</span><span class="sxs-lookup"><span data-stu-id="d6728-133">The **Audits** panel UI looks different in earlier versions of Microsoft Edge, but the general workflow is the same.</span></span>  
    
1.  <span data-ttu-id="d6728-134">Для **устройства**выберите **мобильные** устройства, если вы хотите имитировать мобильное устройство.</span><span class="sxs-lookup"><span data-stu-id="d6728-134">For **Device**, choose **Mobile** if you want to simulate a mobile device.</span></span>  <span data-ttu-id="d6728-135">Этот параметр позволяет изменить строку вашего агента пользователя и изменить размер окна просмотра.</span><span class="sxs-lookup"><span data-stu-id="d6728-135">This option changes your user agent string and resizes the viewport.</span></span>  <span data-ttu-id="d6728-136">Если Мобильная версия страницы отображается не так, как для классической версии, этот параметр может существенно повлиять на результаты аудита.</span><span class="sxs-lookup"><span data-stu-id="d6728-136">If the mobile version of the page displays differently than the desktop version, this option could have a significant effect on the results of your audit.</span></span>  
1.  <span data-ttu-id="d6728-137">Убедитесь, что в разделе " **Аудит** " включен параметр " **Специальные возможности** ".</span><span class="sxs-lookup"><span data-stu-id="d6728-137">In the **Audits** section, make sure that **Accessibility** is enabled.</span></span>  <span data-ttu-id="d6728-138">Отключите другие категории, если вы хотите исключить их из отчета.</span><span class="sxs-lookup"><span data-stu-id="d6728-138">Disable the other categories if you want to exclude them from your report.</span></span>  <span data-ttu-id="d6728-139">Если вы хотите найти другие способы улучшить качество страницы, оставьте это поле пустым.</span><span class="sxs-lookup"><span data-stu-id="d6728-139">Leave them enabled if you want to discover other ways to improve the quality of your page.</span></span>  
1.  <span data-ttu-id="d6728-140">Раздел **регулирования** позволяет регулировать сеть и ЦП, что бывает полезно при анализе производительности нагрузки.</span><span class="sxs-lookup"><span data-stu-id="d6728-140">The **Throttling** section lets you throttle the network and CPU, which is useful when analyzing load performance.</span></span>  <span data-ttu-id="d6728-141">Этот параметр должен быть неважен для оценки доступности, поэтому вы можете использовать любой из них.</span><span class="sxs-lookup"><span data-stu-id="d6728-141">This option should be irrelevant to your accessibility score, so you may use whatever you prefer.</span></span>  
1.  <span data-ttu-id="d6728-142">Флажок **clear Storage (очистить хранилище** ) позволяет очистить все хранилище перед загрузкой страницы или сохранением хранилища между загрузкой страниц.</span><span class="sxs-lookup"><span data-stu-id="d6728-142">The **Clear Storage** checkbox lets you clear all storage before loading the page, or preserve storage between page loads.</span></span>  <span data-ttu-id="d6728-143">Этот параметр также может быть неважен для оценки доступности, поэтому вы можете использовать любой из них.</span><span class="sxs-lookup"><span data-stu-id="d6728-143">This option is also probably irrelevant to your accessibility score, so you may use whatever you prefer.</span></span>  
1.  <span data-ttu-id="d6728-144">Выберите команду **запустить аудиты**.</span><span class="sxs-lookup"><span data-stu-id="d6728-144">Choose **Run Audits**.</span></span> <span data-ttu-id="d6728-145">После 10 – 30 секунд DevTools предоставляет отчет.</span><span class="sxs-lookup"><span data-stu-id="d6728-145">After 10 to 30 seconds, DevTools provides a report.</span></span>  <span data-ttu-id="d6728-146">В отчете приводятся различные советы по улучшению доступности страницы.</span><span class="sxs-lookup"><span data-stu-id="d6728-146">Your report gives you various tips on how to improve the accessibility of the page.</span></span>  
    
    :::image type="complex" source="../media/accessibility-audits-run-audits-result.msft.png" alt-text="Настройка аудита" lightbox="../media/accessibility-audits-run-audits-result.msft.png":::
       <span data-ttu-id="d6728-148">Отчет</span><span class="sxs-lookup"><span data-stu-id="d6728-148">A report</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d6728-149">Щелкните аудиторию, чтобы получить дополнительные сведения о нем.</span><span class="sxs-lookup"><span data-stu-id="d6728-149">Click an audit to learn more about it.</span></span>  
    
    :::image type="complex" source="../media/accessibility-audits-run-audits-result-issues-expanded.msft.png" alt-text="Настройка аудита" lightbox="../media/accessibility-audits-run-audits-result-issues-expanded.msft.png":::
       <span data-ttu-id="d6728-151">Дополнительные сведения об аудите</span><span class="sxs-lookup"><span data-stu-id="d6728-151">More information about an audit</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d6728-152">Выберите дополнительные **сведения** , чтобы просмотреть документацию по аудиту.</span><span class="sxs-lookup"><span data-stu-id="d6728-152">Choose **Learn More** to view the documentation of that audit.</span></span>  
    
    :::image type="complex" source="../media/accessibility-web-dev-accessibility-audits-learn-more.msft.png" alt-text="Настройка аудита" lightbox="../media/accessibility-web-dev-accessibility-audits-learn-more.msft.png":::
       <span data-ttu-id="d6728-154">Просмотр документации по аудиту</span><span class="sxs-lookup"><span data-stu-id="d6728-154">View the documentation of an audit</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="d6728-155">Дополнительные сведения: расширение aXe</span><span class="sxs-lookup"><span data-stu-id="d6728-155">See also: aXe extension</span></span>  

<span data-ttu-id="d6728-156">Вы можете использовать [расширение aXe][ChromeWebStoreAxe] , а не панель **аудита** .</span><span class="sxs-lookup"><span data-stu-id="d6728-156">You may prefer to use the [aXe extension][ChromeWebStoreAxe] rather than the **Audits** panel.</span></span>  
<span data-ttu-id="d6728-157">Расширение aXe обычно предоставляет те же сведения, так как это базовый обработчик, который включает в себя панель аудита.</span><span class="sxs-lookup"><span data-stu-id="d6728-157">The aXe extension generally provides the same information, since it is the underlying engine that powers the Audits panel.</span></span>  <span data-ttu-id="d6728-158">Расширение aXe имеет другой пользовательский интерфейс и описывает аудит слегка разными способами.</span><span class="sxs-lookup"><span data-stu-id="d6728-158">The aXe extension has a different UI and describes audits slightly differently.</span></span>  
<span data-ttu-id="d6728-159">Одно из преимуществ, которое имеет расширение aXe на панели **аудитов** , состоит в том, что она позволяет проверять и вымечать узлы, в которых произошел сбой.</span><span class="sxs-lookup"><span data-stu-id="d6728-159">One advantage that the aXe extension has over the **Audits** panel is that it enables you to inspect and highlight failing nodes.</span></span>  

:::image type="complex" source="../media/accessibility-devtools-extension-axe-panel.msft.png" alt-text="Настройка аудита" lightbox="../media/accessibility-devtools-extension-axe-panel.msft.png":::
   <span data-ttu-id="d6728-161">Расширение aXe</span><span class="sxs-lookup"><span data-stu-id="d6728-161">The aXe extension</span></span>  
:::image-end:::  

## <span data-ttu-id="d6728-162">Область "Специальные возможности"</span><span class="sxs-lookup"><span data-stu-id="d6728-162">The Accessibility pane</span></span>  

<span data-ttu-id="d6728-163">В области " **Специальные возможности** " можно просмотреть дерево специальных возможностей, атрибуты ARIA и вычисляемые свойства специальных возможностей узлов DOM.</span><span class="sxs-lookup"><span data-stu-id="d6728-163">The **Accessibility** pane is where you view the accessibility tree, ARIA attributes, and computed accessibility properties of DOM nodes.</span></span>  

<span data-ttu-id="d6728-164">Чтобы открыть область " **Специальные возможности** ", выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="d6728-164">To open the **Accessibility** pane:</span></span>  

1.  <span data-ttu-id="d6728-165">Откройте вкладку **элементы** .</span><span class="sxs-lookup"><span data-stu-id="d6728-165">Click the **Elements** tab.</span></span>  
1.  <span data-ttu-id="d6728-166">В **дереве DOM**выберите элемент, который нужно проверить.</span><span class="sxs-lookup"><span data-stu-id="d6728-166">In the **DOM Tree**, select the element which you want to inspect.</span></span>  
1.  <span data-ttu-id="d6728-167">Откройте вкладку **Специальные возможности** .  Эта вкладка может быть скрыта за кнопкой **другие вкладки** \ ( ![ другие вкладки ][ImageMoreTabsIcon] \).</span><span class="sxs-lookup"><span data-stu-id="d6728-167">Click the **Accessibility** tab.  This tab may be hidden behind the **More Tabs** \(![More Tabs][ImageMoreTabsIcon]\) button.</span></span>  

:::image type="complex" source="../media/accessibility-elements-accessibility.msft.png" alt-text="Настройка аудита" lightbox="../media/accessibility-elements-accessibility.msft.png":::
   <span data-ttu-id="d6728-169">Проверка `h1` элемента домашней страницы DevTools в области " **Специальные возможности** "</span><span class="sxs-lookup"><span data-stu-id="d6728-169">Inspect the `h1` element of the DevTools homepage in the **Accessibility** pane</span></span>  
:::image-end:::  

### <span data-ttu-id="d6728-170">Просмотр положения элемента в дереве специальных возможностей</span><span class="sxs-lookup"><span data-stu-id="d6728-170">View the position of an element in the accessibility tree</span></span>  

<span data-ttu-id="d6728-171">[Дерево специальных возможностей][MDNAccessibilityTree] — это подмножество дерева DOM.</span><span class="sxs-lookup"><span data-stu-id="d6728-171">The [accessibility tree][MDNAccessibilityTree] is a subset of the DOM tree.</span></span>  <span data-ttu-id="d6728-172">Она включает только элементы из дерева DOM, которые являются важными и полезны для отображения содержимого страницы в средстве чтения с экрана.</span><span class="sxs-lookup"><span data-stu-id="d6728-172">It only contains elements from the DOM tree that are relevant and useful for displaying the contents of a page in a screen reader.</span></span>  

<span data-ttu-id="d6728-173">Проверьте расположение элемента в дереве специальных возможностей в [области "Специальные возможности](#the-accessibility-pane)".</span><span class="sxs-lookup"><span data-stu-id="d6728-173">Inspect the position of an element in the accessibility tree from the [Accessibility pane](#the-accessibility-pane).</span></span>  

:::image type="complex" source="../media/accessibility-elements-accessibility-tree.msft.png" alt-text="Настройка аудита" lightbox="../media/accessibility-elements-accessibility-tree.msft.png":::
   <span data-ttu-id="d6728-175">Раздел **дерева специальных возможностей**</span><span class="sxs-lookup"><span data-stu-id="d6728-175">The **Accessibility Tree** section</span></span>  
:::image-end:::  

### <span data-ttu-id="d6728-176">Просмотр атрибутов ARIA элемента</span><span class="sxs-lookup"><span data-stu-id="d6728-176">View the ARIA attributes of an element</span></span>  

<span data-ttu-id="d6728-177">Атрибуты ARIA гарантируют, что средства чтения с экрана имеют всю необходимую информацию для правильного представления содержимого страницы.</span><span class="sxs-lookup"><span data-stu-id="d6728-177">ARIA attributes ensure that screen readers have all of the information that they need in order to properly represent the contents of a page.</span></span>  

<span data-ttu-id="d6728-178">Просмотрите атрибуты ARIA элемента в [области "Специальные возможности](#the-accessibility-pane)".</span><span class="sxs-lookup"><span data-stu-id="d6728-178">View the ARIA attributes of an element in the [Accessibility pane](#the-accessibility-pane).</span></span>  

:::image type="complex" source="../media/accessibility-elements-accessibility-aria-attributes.msft.png" alt-text="Настройка аудита" lightbox="../media/accessibility-elements-accessibility-aria-attributes.msft.png":::
   <span data-ttu-id="d6728-180">Раздел **атрибутов ARIA**</span><span class="sxs-lookup"><span data-stu-id="d6728-180">The **ARIA Attributes** section</span></span>  
:::image-end:::  

### <span data-ttu-id="d6728-181">Просмотр вычисляемых свойств специальных возможностей для элемента</span><span class="sxs-lookup"><span data-stu-id="d6728-181">View the computed accessibility properties of an element</span></span>  

> [!NOTE]
> <span data-ttu-id="d6728-182">Если вы ищете вычисляемые свойства CSS, перейдите в раздел [Вычисляемая вкладка][DevtoolsCssReferenceViewActuallyAppliedElements].</span><span class="sxs-lookup"><span data-stu-id="d6728-182">If you are looking for computed CSS properties, navigate to [Computed tab][DevtoolsCssReferenceViewActuallyAppliedElements].</span></span>  

<span data-ttu-id="d6728-183">Некоторые свойства специальных возможностей динамически рассчитываются браузером.</span><span class="sxs-lookup"><span data-stu-id="d6728-183">Some accessibility properties are dynamically calculated by the browser.</span></span>  <span data-ttu-id="d6728-184">Эти свойства отображаются в разделе " **вычисляемые свойства** " области " **Специальные возможности** ".</span><span class="sxs-lookup"><span data-stu-id="d6728-184">These properties are displayed in the **Computed Properties** section of the **Accessibility** pane.</span></span>  

<span data-ttu-id="d6728-185">Просмотр вычисляемых свойств специальных возможностей для элемента в [области специальных возможностей](#the-accessibility-pane).</span><span class="sxs-lookup"><span data-stu-id="d6728-185">View the computed accessibility properties of an element in the [Accessibility pane](#the-accessibility-pane).</span></span>  

:::image type="complex" source="../media/accessibility-elements-accessibility-computed-properties.msft.png" alt-text="Настройка аудита" lightbox="../media/accessibility-elements-accessibility-computed-properties.msft.png":::
   <span data-ttu-id="d6728-187">Раздел " **вычисляемые свойства** " области " **Специальные возможности** "</span><span class="sxs-lookup"><span data-stu-id="d6728-187">The **Computed Properties** section of the **Accessibility** pane</span></span>  
:::image-end:::  

## <span data-ttu-id="d6728-188">Просмотр коэффициента контрастности текстового элемента в палитре цветов</span><span class="sxs-lookup"><span data-stu-id="d6728-188">View the contrast ratio of a text element in the Color Picker</span></span>  

<span data-ttu-id="d6728-189">Некоторые люди со слабым зрением не видят области как очень яркие или очень темные.</span><span class="sxs-lookup"><span data-stu-id="d6728-189">Some people with low vision do not see areas as very bright or very dark.</span></span>  <span data-ttu-id="d6728-190">Все обычно выводятся примерно одинаковая яркость, что делает ее более четкими и контурами.</span><span class="sxs-lookup"><span data-stu-id="d6728-190">Everything tends to appear at about the same brightness, which makes it hard to distinguish outlines and edges.</span></span>  

<span data-ttu-id="d6728-191">Коэффициент контрастности измеряет разницу яркости между передним и фоном текста.</span><span class="sxs-lookup"><span data-stu-id="d6728-191">Contrast ratio measures the difference in brightness between the foreground and background of text.</span></span>  <span data-ttu-id="d6728-192">Если текст имеет низкую степень контрастности, пользователи с низким зрением могут в буквальном смысле работать с вашим сайтом в качестве пустого экрана.</span><span class="sxs-lookup"><span data-stu-id="d6728-192">If your text has a low contrast ratio, then these low vision users may literally experience your site as a blank screen.</span></span>  

<span data-ttu-id="d6728-193">С помощью средства выбора цвета вы можете убедиться, что текст соответствует рекомендуемым уровням контрастности:</span><span class="sxs-lookup"><span data-stu-id="d6728-193">The Color Picker helps you verify that your text meets recommended contrast ratio levels:</span></span>  

1.  <span data-ttu-id="d6728-194">Откройте вкладку **элементы** .</span><span class="sxs-lookup"><span data-stu-id="d6728-194">Click the **Elements** tab.</span></span>  
1.  <span data-ttu-id="d6728-195">В **дереве DOM**выделите текстовый элемент, который нужно проверить.</span><span class="sxs-lookup"><span data-stu-id="d6728-195">In the **DOM Tree**, select the text element that you want to inspect.</span></span>  
    
    :::image type="complex" source="../media/accessibility-elements-paragraph-highlight.msft.png" alt-text="Настройка аудита" lightbox="../media/accessibility-elements-paragraph-highlight.msft.png":::
       <span data-ttu-id="d6728-197">Проверка абзаца в **дереве DOM**</span><span class="sxs-lookup"><span data-stu-id="d6728-197">Inspect a paragraph in the **DOM Tree**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d6728-198">В области **стили** щелкните квадратик цвета рядом со `color` значением элемента.</span><span class="sxs-lookup"><span data-stu-id="d6728-198">In the **Styles** pane, click the color square next to the `color` value of the element.</span></span>  
    
    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color.msft.png" alt-text="Настройка аудита" lightbox="../media/accessibility-elements-styles-paragraph-highlight-color.msft.png":::
       <span data-ttu-id="d6728-200">`color`Свойство элемента</span><span class="sxs-lookup"><span data-stu-id="d6728-200">The `color` property of the element</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d6728-201">Проверьте раздел **коэффициент контрастности** в палитре цветов.</span><span class="sxs-lookup"><span data-stu-id="d6728-201">Check the **Contrast Ratio** section of the Color Picker.</span></span>  <span data-ttu-id="d6728-202">Один флажок означает, что элемент соответствует [минимальным рекомендациям][W3CContrastMinimum].</span><span class="sxs-lookup"><span data-stu-id="d6728-202">One checkmark means that the element meets the [minimum recommendation][W3CContrastMinimum].</span></span>  <span data-ttu-id="d6728-203">Два флажка означают, что они соответствуют [улучшенным рекомендациям][W3CContrastEnhanced].</span><span class="sxs-lookup"><span data-stu-id="d6728-203">Two checkmarks means that it meets the [enhanced recommendation][W3CContrastEnhanced].</span></span>  
    
    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color-picker.msft.png" alt-text="Настройка аудита" lightbox="../media/accessibility-elements-styles-paragraph-highlight-color-picker.msft.png":::
       <span data-ttu-id="d6728-205">В разделе " **степень контрастности** " в окне выбора цвета показаны 2 метки и значение</span><span class="sxs-lookup"><span data-stu-id="d6728-205">The **Contrast Ratio** section of the Color Picker shows 2 checkmarks and a value of</span></span> `13.97`  
    :::image-end:::  
    
1.  <span data-ttu-id="d6728-206">Щелкните раздел **коэффициент контрастности** , чтобы просмотреть дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="d6728-206">Click the **Contrast Ratio** section to see more information.</span></span>  <span data-ttu-id="d6728-207">В визуальном элементе выбора в верхней части окна выбора цвета появится линия.</span><span class="sxs-lookup"><span data-stu-id="d6728-207">A line appears in the visual picker at the top of the Color Picker.</span></span>  <span data-ttu-id="d6728-208">Если текущий цвет соответствует рекомендациям, то все элементы на одной и той же стороне линии также соответствуют рекомендациям.</span><span class="sxs-lookup"><span data-stu-id="d6728-208">If the current color meets recommendations, then anything on the same side of the line also meets recommendations.</span></span>  <span data-ttu-id="d6728-209">Если текущий цвет не соответствует рекомендациям, то на одном и том же стороне не будут выводится соответствие рекомендациям.</span><span class="sxs-lookup"><span data-stu-id="d6728-209">If the current color does not meet recommendations, then anything on the same side also does not meet recommendations.</span></span>  
    
    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color-picker-contrast-ratio-details.msft.png" alt-text="Настройка аудита" lightbox="../media/accessibility-elements-styles-paragraph-highlight-color-picker-contrast-ratio-details.msft.png":::
       <span data-ttu-id="d6728-211">Линия **коэффициента контрастности** в средстве выбора визуальных элементов</span><span class="sxs-lookup"><span data-stu-id="d6728-211">The **Contrast Ratio** Line in the visual picker</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="d6728-212">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="d6728-212">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageMoreTabsIcon]: ../media/more-tabs-icon.msft.png  

<!-- links -->  

[DevtoolsAccessibilityNavigation]: ./navigation.md "Навигация в Microsoft Edge DevTools с технологией специальных возможностей | Документы Microsoft"  
[DevtoolsCssReferenceViewActuallyAppliedElements]: ../css/reference.md#view-only-the-css-that-is-actually-applied-to-an-element "Просмотр только CSS, которая фактически применяется к ссылке element-CSS | Документы Microsoft"  

[ChromeWebStoreAxe]: https://chrome.google.com/webstore/detail/axe/lhdoppojpmngadmnindnejefpokejbdd?hl=en-US "Axe — тестирование специальных возможностей в Интернете-веб-магазин Chrome"  

[MDNAccessibilityTree]: https://developer.mozilla.org/docs/Glossary/AOM "Дерево специальных возможностей (AOM) | MDN"  
[MDNAccessibility]: https://developer.mozilla.org/docs/Web/Accessibility "Специальные возможности | MDN"  
[MDNScreenReader]: https://developer.mozilla.org/docs/Glossary/Screen_reader "Средство чтения с экрана | MDN"  

[W3CContrastEnhanced]: https://www.w3.org/WAI/WCAG21/quickref/#contrast-enhanced "Контрастность (улучшенная) уровень AAA | PNG"  
[W3CContrastMinimum]: https://www.w3.org/WAI/WCAG21/quickref/#contrast-minimum "Контрастность (минимум) уровень AA | PNG"  

> [!NOTE]
> <span data-ttu-id="d6728-221">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="d6728-221">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="d6728-222">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="d6728-222">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="d6728-224">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="d6728-224">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
