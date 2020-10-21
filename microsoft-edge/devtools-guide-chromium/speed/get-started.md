---
description: Узнайте, как использовать Microsoft Edge DevTools для поиска возможностей, позволяющих быстрее загружать веб-сайты.
title: Оптимизация скорости веб-сайта с помощью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: af655941fdc836759651e8d8202e41d8d03331c5
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125491"
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

# <span data-ttu-id="d5e48-104">Оптимизация скорости веб-сайта с помощью Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="d5e48-104">Optimize website speed with Microsoft Edge DevTools</span></span>  

## <span data-ttu-id="d5e48-105">Цель учебника</span><span class="sxs-lookup"><span data-stu-id="d5e48-105">Goal of tutorial</span></span>  

<span data-ttu-id="d5e48-106">В этом учебнике объясняется, как использовать Microsoft Edge DevTools, чтобы найти способы быстрой загрузки веб-сайтов.</span><span class="sxs-lookup"><span data-stu-id="d5e48-106">This tutorial teaches you how to use Microsoft Edge DevTools to find ways to make your websites load faster.</span></span>  

## <span data-ttu-id="d5e48-107">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="d5e48-107">Prerequisites</span></span>  

*   <span data-ttu-id="d5e48-108">У вас должен быть базовый интерфейс разработки веб-приложений, аналогично тому, что научились в этом [Знакомство с классом веб-разработки][CourseraIntroductionWebDevelopmentClass].</span><span class="sxs-lookup"><span data-stu-id="d5e48-108">You should have basic web development experience, similar to what is taught in this [Introduction to Web Development class][CourseraIntroductionWebDevelopmentClass].</span></span>  
*   <span data-ttu-id="d5e48-109">Вам ничего не нужно знать о быстродействии нагрузки.</span><span class="sxs-lookup"><span data-stu-id="d5e48-109">You do not need to know anything about load performance.</span></span>  <span data-ttu-id="d5e48-110">В этом учебнике вы узнаете об этом.</span><span class="sxs-lookup"><span data-stu-id="d5e48-110">You learn about it in this tutorial!</span></span>  

## <span data-ttu-id="d5e48-111">Введение</span><span class="sxs-lookup"><span data-stu-id="d5e48-111">Introduction</span></span>  

<span data-ttu-id="d5e48-112">Это Илья.</span><span class="sxs-lookup"><span data-stu-id="d5e48-112">This is Tony.</span></span>  <span data-ttu-id="d5e48-113">Илья чрезвычайно знаменита в отношении Cat общества.</span><span class="sxs-lookup"><span data-stu-id="d5e48-113">Tony is very famous in cat society.</span></span>  <span data-ttu-id="d5e48-114">Он создал веб-сайт, чтобы его вентиляторы могли узнать о своем любимом продуктов.</span><span class="sxs-lookup"><span data-stu-id="d5e48-114">He has built a website so that his fans are able to learn about his favorite foods.</span></span>  <span data-ttu-id="d5e48-115">Его вентиляторы понравятся на сайте, но в Илья сохраняются жалобы, которые медленно загружаются на сайт.</span><span class="sxs-lookup"><span data-stu-id="d5e48-115">His fans love the site, but Tony keeps hearing complaints that the site loads slowly.</span></span>  <span data-ttu-id="d5e48-116">Илья предложит вам помочь ему ускорить работу сайта.</span><span class="sxs-lookup"><span data-stu-id="d5e48-116">Tony has asked you to help him speed the site up.</span></span>  

:::image type="complex" source="../media/speed-tony.msft.png" alt-text="Илья CAT" lightbox="../media/speed-tony.msft.png":::
   <span data-ttu-id="d5e48-118">Илья CAT</span><span class="sxs-lookup"><span data-stu-id="d5e48-118">Tony the cat</span></span>  
:::image-end:::  

## <span data-ttu-id="d5e48-119">Действие 1: аудит сайта</span><span class="sxs-lookup"><span data-stu-id="d5e48-119">Step 1: Audit the site</span></span>  

<span data-ttu-id="d5e48-120">Всякий раз, когда вы захотите улучшить производительность загрузки сайта, **всегда начинайте с аудита**.</span><span class="sxs-lookup"><span data-stu-id="d5e48-120">Whenever you set out to improve the load performance of a site, **always start with an audit**.</span></span>  
<span data-ttu-id="d5e48-121">Аудитория имеет 2 важные функции.</span><span class="sxs-lookup"><span data-stu-id="d5e48-121">The audit has 2 important functions:</span></span>  

*   <span data-ttu-id="d5e48-122">Она создает **базовый план** для измерения последующих изменений.</span><span class="sxs-lookup"><span data-stu-id="d5e48-122">It creates a **baseline** for you to measure subsequent changes against.</span></span>  
*   <span data-ttu-id="d5e48-123">Здесь вы найдете **Советы** , которые помогут вам изменить наиболее благоприятные изменения.</span><span class="sxs-lookup"><span data-stu-id="d5e48-123">It gives you **actionable tips** on what changes have the most impact.</span></span>  
    
### <span data-ttu-id="d5e48-124">Настройка</span><span class="sxs-lookup"><span data-stu-id="d5e48-124">Set up</span></span>  

<span data-ttu-id="d5e48-125">Сначала необходимо настроить сайт, чтобы вы могли вносить в него изменения позже.</span><span class="sxs-lookup"><span data-stu-id="d5e48-125">First, you must set up the site so that you are able to make changes to it later.</span></span>  

1.  <span data-ttu-id="d5e48-126">[Откройте исходный код для сайта](https://glitch.com/edit/#!/tony).</span><span class="sxs-lookup"><span data-stu-id="d5e48-126">[Open the source code for the site](https://glitch.com/edit/#!/tony).</span></span>  <span data-ttu-id="d5e48-127">Эта вкладка называется **вкладкой "редактор"**.</span><span class="sxs-lookup"><span data-stu-id="d5e48-127">This tab is referred to as the **editor tab**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-server-js.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-server-js.msft.png":::
       <span data-ttu-id="d5e48-129">**Вкладка "редактор"**</span><span class="sxs-lookup"><span data-stu-id="d5e48-129">The **editor tab**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d5e48-130">Выберите **Илья**.</span><span class="sxs-lookup"><span data-stu-id="d5e48-130">Choose **tony**.</span></span>  <span data-ttu-id="d5e48-131">Откроется меню.</span><span class="sxs-lookup"><span data-stu-id="d5e48-131">A menu appears.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-server-js-remix-project.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-server-js-remix-project.msft.png":::
       <span data-ttu-id="d5e48-133">Меню, которое появляется после нажатия кнопки **Илья**</span><span class="sxs-lookup"><span data-stu-id="d5e48-133">The menu that appears after clicking **tony**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d5e48-134">Выберите **Remix проект**.</span><span class="sxs-lookup"><span data-stu-id="d5e48-134">Choose **Remix Project**.</span></span>  <span data-ttu-id="d5e48-135">Имя проекта меняется с **Илья** на случайное сгенерированное имя.</span><span class="sxs-lookup"><span data-stu-id="d5e48-135">The name of the project changes from **tony** to some randomly-generated name.</span></span>  <span data-ttu-id="d5e48-136">Теперь у вас есть Редактируемая копия кода.</span><span class="sxs-lookup"><span data-stu-id="d5e48-136">You now have your own editable copy of the code.</span></span>  <span data-ttu-id="d5e48-137">Позже вы можете внести изменения в этот код.</span><span class="sxs-lookup"><span data-stu-id="d5e48-137">Later on, you may make changes to this code.</span></span>  
1.  <span data-ttu-id="d5e48-138">Нажмите кнопку **Показать** и выберите **в новом окне**.</span><span class="sxs-lookup"><span data-stu-id="d5e48-138">Choose **Show** and choose **In a New Window**.</span></span>  <span data-ttu-id="d5e48-139">Демонстрационный ролик откроется на новой вкладке.  Эта вкладка упоминается как **вкладка Demo**.  Загрузка сайта может занять некоторое время.</span><span class="sxs-lookup"><span data-stu-id="d5e48-139">The demo opens in a new tab.  This tab is be referred to as the **demo tab**.  It may take a while for the site to load.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-show-live.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-show-live.msft.png":::
       <span data-ttu-id="d5e48-141">Вкладка "демонстрация"</span><span class="sxs-lookup"><span data-stu-id="d5e48-141">The demo tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d5e48-142">Выберите `Control` + `Shift` + `J` \ (Windows, Linux \) или `Command` + `Option` + `J` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="d5e48-142">Select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\).</span></span>  <span data-ttu-id="d5e48-143">Рядом с демоном DevTools откроется Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="d5e48-143">Microsoft Edge DevTools opens up alongside the demo.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-show-live-console.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-show-live-console.msft.png":::
       <span data-ttu-id="d5e48-145">DevTools и демонстрация</span><span class="sxs-lookup"><span data-stu-id="d5e48-145">DevTools and the demo</span></span>  
    :::image-end:::  
    
<span data-ttu-id="d5e48-146">Для остальных снимков экрана в этом учебнике DevTools отображается в отдельном окне.</span><span class="sxs-lookup"><span data-stu-id="d5e48-146">For the rest of the screenshots in this tutorial, DevTools is shown in a separate window.</span></span>  <span data-ttu-id="d5e48-147">Выберите `Control` + `Shift` + `P` \ (Windows, Linux \) или `Command` + `Shift` + `P` \ (macOS \), чтобы открыть меню команд, введите его `Undock` и выберите команду **открепить в отдельном окне**.</span><span class="sxs-lookup"><span data-stu-id="d5e48-147">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu, typing `Undock`, and then selecting **Undock into separate window**.</span></span>  

:::image type="complex" source="../media/speed-console.msft.png" alt-text="Илья CAT" lightbox="../media/speed-console.msft.png":::
   <span data-ttu-id="d5e48-149">Незакрепленные DevTools</span><span class="sxs-lookup"><span data-stu-id="d5e48-149">Undocked DevTools</span></span>  
:::image-end:::  

### <span data-ttu-id="d5e48-150">Создание базового плана</span><span class="sxs-lookup"><span data-stu-id="d5e48-150">Establish a baseline</span></span>  

<span data-ttu-id="d5e48-151">Базовый план — это запись того, как выполняется сайт, прежде чем вы внесли улучшения производительности.</span><span class="sxs-lookup"><span data-stu-id="d5e48-151">The baseline is a record of how the site performed before you made any performance improvements.</span></span>  

1.  <span data-ttu-id="d5e48-152">Перейдите на вкладку **Аудит** .  Она может быть скрыта за кнопкой " **Дополнительные панели** " \ "дополнительные панели ![ ][ImageMorePanelsIcon] \".</span><span class="sxs-lookup"><span data-stu-id="d5e48-152">Select the **Audits** tab.  It may be hidden behind the **More Panels** \(![More Panels][ImageMorePanelsIcon]\) button.</span></span>  <span data-ttu-id="d5e48-153">На этой панели есть Lighthouse, так как проект, который включает панель «аудиты», называется **Lighthouse**.</span><span class="sxs-lookup"><span data-stu-id="d5e48-153">There is a Lighthouse on this panel because the project that powers the Audits panel is named **Lighthouse**.</span></span>  
    
    [!INCLUDE [audits-panel-note](../includes/audits-panel-note.md)]  
    
    :::image type="complex" source="../media/speed-audits-performance.msft.png" alt-text="Илья CAT" lightbox="../media/speed-audits-performance.msft.png":::
       <span data-ttu-id="d5e48-155">Панель « **Аудит** »</span><span class="sxs-lookup"><span data-stu-id="d5e48-155">The **Audits** panel</span></span>  
    :::image-end:::  
    
    <!--todo: add link to Lighthouse when section is available  -->  
    <!-- /web/tools/lighthouse  -->  
    
1.  <span data-ttu-id="d5e48-156">Соответствие параметров конфигурации аудита с параметрами, приведенными на предыдущем рисунке.</span><span class="sxs-lookup"><span data-stu-id="d5e48-156">Match your audit configuration settings to those in the previous figure.</span></span>  <span data-ttu-id="d5e48-157">Ниже приведено описание различных параметров.</span><span class="sxs-lookup"><span data-stu-id="d5e48-157">Here is an explanation of the different options:</span></span>  
    
    *   <span data-ttu-id="d5e48-158">**Устройства**.</span><span class="sxs-lookup"><span data-stu-id="d5e48-158">**Device**.</span></span>  <span data-ttu-id="d5e48-159">При настройке на **мобильном устройстве** изменяется строка агента пользователя и имитируется мобильное окно просмотра.</span><span class="sxs-lookup"><span data-stu-id="d5e48-159">Setting to **Mobile** changes the user agent string and simulates a mobile viewport.</span></span>  <span data-ttu-id="d5e48-160">Настройка для **настольного компьютера** очень просто отключает изменения на **мобильном устройстве** .</span><span class="sxs-lookup"><span data-stu-id="d5e48-160">Setting to **Desktop** pretty much just disables the **Mobile** changes.</span></span>  
    *   <span data-ttu-id="d5e48-161">**Аудита**.</span><span class="sxs-lookup"><span data-stu-id="d5e48-161">**Audits**.</span></span>  <span data-ttu-id="d5e48-162">Отключение категории не позволяет панели аудита выполнять эти проверки и исключает из отчета эти проверки.</span><span class="sxs-lookup"><span data-stu-id="d5e48-162">Disabling a category prevents the Audits panel from running those audits, and excludes those audits from your report.</span></span>  <span data-ttu-id="d5e48-163">Если вы хотите просмотреть предоставленные типы рекомендаций, оставьте другие доступные категории.</span><span class="sxs-lookup"><span data-stu-id="d5e48-163">Leave the other categories enabled, if you want to see the types of recommendations that are provide.</span></span>  <span data-ttu-id="d5e48-164">Отключение категорий немного ускоряет процесс аудита.</span><span class="sxs-lookup"><span data-stu-id="d5e48-164">Disabling categories slightly speeds up the auditing process.</span></span>  
    *   <span data-ttu-id="d5e48-165">**Регулирование**.</span><span class="sxs-lookup"><span data-stu-id="d5e48-165">**Throttling**.</span></span>  <span data-ttu-id="d5e48-166">Для **эмуляции медленного 4G, скорость процессора 4X** эмулирует типичные условия обзора на мобильном устройстве.</span><span class="sxs-lookup"><span data-stu-id="d5e48-166">Setting to **Simulated Slow 4G, 4x CPU Slowdown** simulates the typical conditions of browsing on a mobile device.</span></span>  <span data-ttu-id="d5e48-167">Она называется смоделированной, так как панель "Аудит" не выполняет никаких действий по регулированию в процессе аудита.</span><span class="sxs-lookup"><span data-stu-id="d5e48-167">It is named "simulated" because the Audits panel does not actually throttle during the auditing process.</span></span>  <span data-ttu-id="d5e48-168">Вместо этого оно просто экстраполяция того, сколько времени займет загрузка страницы в условиях мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="d5e48-168">Instead, it just extrapolates how long the page would take to load under mobile conditions.</span></span>  <span data-ttu-id="d5e48-169">Параметр " **применено...** ", в свою очередь, в действительности регулирует производительность процессора и сети с компромиссом более продолжительного процесса аудита.</span><span class="sxs-lookup"><span data-stu-id="d5e48-169">The **Applied...** setting, on the other hand, actually throttles your CPU and network, with the tradeoff of a longer auditing process.</span></span>  
    *   <span data-ttu-id="d5e48-170">**Очистите хранилище**.</span><span class="sxs-lookup"><span data-stu-id="d5e48-170">**Clear Storage**.</span></span>  <span data-ttu-id="d5e48-171">При установке этого флажка все хранилище, связанное со страницей, будет очищено перед каждым аудитом.</span><span class="sxs-lookup"><span data-stu-id="d5e48-171">Enabling this checkbox clears all storage associated with the page before every audit.</span></span>  <span data-ttu-id="d5e48-172">Оставьте этот параметр, если вы хотите подвергать аудиту, как посетители в первый раз будут работать на вашем сайте.</span><span class="sxs-lookup"><span data-stu-id="d5e48-172">Leave this setting on if you want to audit how first-time visitors experience your site.</span></span>  <span data-ttu-id="d5e48-173">Отключите этот параметр, если вы хотите использовать функцию повторного посещения.</span><span class="sxs-lookup"><span data-stu-id="d5e48-173">Disable this setting when you want the repeat-visit experience.</span></span>  
    
1.  <span data-ttu-id="d5e48-174">Выберите команду **запустить аудиты**.</span><span class="sxs-lookup"><span data-stu-id="d5e48-174">Choose **Run Audits**.</span></span>  <span data-ttu-id="d5e48-175">После 10 – 30 секунд на панели «аудиты» отображается отчет о быстродействии сайта.</span><span class="sxs-lookup"><span data-stu-id="d5e48-175">After 10 to 30 seconds, the Audits panel shows you a report of the performance of the site.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed.msft.png":::
       <span data-ttu-id="d5e48-177">Отчет для панели «аудит» для производительности сайта</span><span class="sxs-lookup"><span data-stu-id="d5e48-177">The report for the Audits panel of the performance of the site</span></span>  
    :::image-end:::  
    
#### <span data-ttu-id="d5e48-178">Обработка ошибок отчета</span><span class="sxs-lookup"><span data-stu-id="d5e48-178">Handling report errors</span></span>  

<span data-ttu-id="d5e48-179">Если вы когда-либо получаете сообщение об ошибке в отчете на панели аудиты, попробуйте запустить вкладку Demo из окна **InPrivate** без открытия других вкладок.</span><span class="sxs-lookup"><span data-stu-id="d5e48-179">If you ever get an error in your Audits panel report, try running the demo tab from an **InPrivate** window with no other tabs open.</span></span>  <span data-ttu-id="d5e48-180">Это гарантирует, что вы используете Microsoft Edge из чистого состояния.</span><span class="sxs-lookup"><span data-stu-id="d5e48-180">This ensures that you are running Microsoft Edge from a clean state.</span></span>  <span data-ttu-id="d5e48-181">Определенные расширения Microsoft Edge часто мешают процессу аудита.</span><span class="sxs-lookup"><span data-stu-id="d5e48-181">Microsoft Edge Extensions in particular often interfere with the auditing process.</span></span>  

<!--todo: add screen capture for error in audit -->  
<!--
:::image type="complex" source="../media/speed-.msft.png" alt-text="Илья CAT" lightbox="../media/speed-.msft.png":::
   A report that errored  
:::image-end:::  
-->  

### <span data-ttu-id="d5e48-182">Понимание отчета</span><span class="sxs-lookup"><span data-stu-id="d5e48-182">Understand your report</span></span>  

<span data-ttu-id="d5e48-183">Число в верхней части отчета является общим показателем эффективности сайта.</span><span class="sxs-lookup"><span data-stu-id="d5e48-183">The number at the top of your report is the overall performance score for the site.</span></span>  <span data-ttu-id="d5e48-184">После внесения изменений в код вы должны увидеть этот номер.</span><span class="sxs-lookup"><span data-stu-id="d5e48-184">Later, as you make changes to the code, you should see this number rise.</span></span>  <span data-ttu-id="d5e48-185">Более высокие баллы означают более высокую производительность.</span><span class="sxs-lookup"><span data-stu-id="d5e48-185">A higher score means better performance.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-metrics-highlighted.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-metrics-highlighted.msft.png":::
   <span data-ttu-id="d5e48-187">Общая оценка производительности</span><span class="sxs-lookup"><span data-stu-id="d5e48-187">The overall performance score</span></span>  
:::image-end:::  

<span data-ttu-id="d5e48-188">Раздел **метрики** содержит количественные измерения производительности сайта.</span><span class="sxs-lookup"><span data-stu-id="d5e48-188">The **Metrics** section provides quantitative measurements of the performance of the site.</span></span>  <span data-ttu-id="d5e48-189">Каждая метрика обеспечивает различные аспекты производительности.</span><span class="sxs-lookup"><span data-stu-id="d5e48-189">Each metric provides insight into a different aspect of the performance.</span></span>  <span data-ttu-id="d5e48-190">Например, при первом обобщении с **содержимым** появляется сообщение о том, что содержимое сначала закрашено на экран, что является важной вехой в восприятии загрузки страницы, в то время как в **интерактивном режиме** отмечается тот момент, когда страница будет готова для обработки взаимодействия с пользователем.</span><span class="sxs-lookup"><span data-stu-id="d5e48-190">For example, **First Contentful Paint** tells you when content is first painted to the screen, which is an important milestone in the user's perception of the page load, whereas **Time To Interactive** marks the point at which the page appears ready enough to handle user interactions.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-highlighted.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-highlighted.msft.png":::
   <span data-ttu-id="d5e48-192">Раздел **метрики**</span><span class="sxs-lookup"><span data-stu-id="d5e48-192">The **Metrics** section</span></span>  
:::image-end:::  

<span data-ttu-id="d5e48-193">Щелкните выделенный выключатель на приведенном ниже рисунке, чтобы просмотреть описание каждой метрики, а затем нажмите **Дополнительные сведения** , чтобы прочитать его документацию.</span><span class="sxs-lookup"><span data-stu-id="d5e48-193">Select the highlighted toggle button in the following figure to see a description for each metric, and choose **Learn More** to read documentation about it.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-expanded.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-expanded.msft.png":::
   <span data-ttu-id="d5e48-195">Щелкните выделенный выключатель, чтобы развернуть элементы метрик</span><span class="sxs-lookup"><span data-stu-id="d5e48-195">Select the highlighted toggle button to expand the Metrics items</span></span>  
:::image-end:::  

<span data-ttu-id="d5e48-196">Под метриками представлен набор снимков экрана, показывающий, как страница выглядит как загруженная.</span><span class="sxs-lookup"><span data-stu-id="d5e48-196">Below Metrics is a collection of screenshots that show you how the page looked as it loaded.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png":::
   <span data-ttu-id="d5e48-198">Снимки экрана, посвященные загрузке страницы</span><span class="sxs-lookup"><span data-stu-id="d5e48-198">Screenshots of how the page looked while loading</span></span>  
:::image-end:::  

<span data-ttu-id="d5e48-199">В разделе " **возможности** " представлены конкретные советы по повышению производительности загрузки данной страницы.</span><span class="sxs-lookup"><span data-stu-id="d5e48-199">The **Opportunities** section provides specific tips on how to improve the load performance of this specific page.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png":::
   <span data-ttu-id="d5e48-201">Раздел " **возможности** "</span><span class="sxs-lookup"><span data-stu-id="d5e48-201">The **Opportunities** section</span></span>  
:::image-end:::  

<span data-ttu-id="d5e48-202">Выберите возможность, чтобы узнать больше о ней.</span><span class="sxs-lookup"><span data-stu-id="d5e48-202">Select an opportunity to learn more about it.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-opportunities-expanded.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-remix-audits-performance-opportunities-expanded.msft.png":::
   <span data-ttu-id="d5e48-204">**Исключение ресурсов блокировки рендеринга** возможная сделка</span><span class="sxs-lookup"><span data-stu-id="d5e48-204">**Eliminate render-blocking resources** opportunity</span></span>  
:::image-end:::  

<span data-ttu-id="d5e48-205">Выберите дополнительные **сведения** , чтобы просмотреть документацию о важности возможной сделки и конкретные рекомендации по ее устранению.</span><span class="sxs-lookup"><span data-stu-id="d5e48-205">Choose **Learn More** to see documentation about why an opportunity is important, and specific recommendations on how to fix it.</span></span>  

:::image type="complex" source="../media/speed-web-dev-performance-audits.msft.png" alt-text="Илья CAT" lightbox="../media/speed-web-dev-performance-audits.msft.png":::
   <span data-ttu-id="d5e48-207">Документация по **устранению ресурсов с блокировкой рендеринга** возможная сделка</span><span class="sxs-lookup"><span data-stu-id="d5e48-207">Documentation for the **Eliminate render-blocking resources** opportunity</span></span>  
:::image-end:::  

<span data-ttu-id="d5e48-208">Раздел **Диагностика** содержит дополнительные сведения о факторах, которые влияют на время загрузки страницы.</span><span class="sxs-lookup"><span data-stu-id="d5e48-208">The **Diagnostics** section provides more information about factors that contribute to the load time of the page.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-diagnostics.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-remix-audits-performance-diagnostics.msft.png":::
   <span data-ttu-id="d5e48-210">Раздел " **Диагностика** "</span><span class="sxs-lookup"><span data-stu-id="d5e48-210">The **Diagnostics** section</span></span>  
:::image-end:::  

<span data-ttu-id="d5e48-211">В разделе **переданные аудиты** показано, что делает сайт правильно.</span><span class="sxs-lookup"><span data-stu-id="d5e48-211">The **Passed Audits** section shows you what the site is doing correctly.</span></span>  <span data-ttu-id="d5e48-212">Выберите этот пункт, чтобы развернуть раздел.</span><span class="sxs-lookup"><span data-stu-id="d5e48-212">Select to expand the section.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-passed-audits.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-remix-audits-performance-passed-audits.msft.png":::
   <span data-ttu-id="d5e48-214">Раздел " **пройденные аудиты** "</span><span class="sxs-lookup"><span data-stu-id="d5e48-214">The **Passed Audits** section</span></span>  
:::image-end:::  

## <span data-ttu-id="d5e48-215">Этап 2: эксперименты</span><span class="sxs-lookup"><span data-stu-id="d5e48-215">Step 2: Experiment</span></span>  

<span data-ttu-id="d5e48-216">Раздел "возможности" в отчете об аудите содержит советы по улучшению производительности страницы.</span><span class="sxs-lookup"><span data-stu-id="d5e48-216">The Opportunities section of your audit report gives you tips on how to improve the performance of the page.</span></span>  <span data-ttu-id="d5e48-217">В этом разделе вы реализуете рекомендованные изменения в базе кода, проведя аудит сайта после каждого изменения, чтобы определить, как оно влияет на скорость сайта.</span><span class="sxs-lookup"><span data-stu-id="d5e48-217">In this section, you implement the recommended changes to the codebase, auditing the site after each change to measure how it affects site speed.</span></span>  

### <span data-ttu-id="d5e48-218">Включение сжатия текста</span><span class="sxs-lookup"><span data-stu-id="d5e48-218">Enable text compression</span></span>  

<span data-ttu-id="d5e48-219">В отчете говорится, что отсутствие огромных полезных данных сети является одной из самых первых возможностей для повышения производительности страницы.</span><span class="sxs-lookup"><span data-stu-id="d5e48-219">Your report says that avoiding enormous network payloads is one of the top opportunities for improving the performance of the page.</span></span>  <span data-ttu-id="d5e48-220">Включить сжатие текста — это возможность улучшить производительность страницы.</span><span class="sxs-lookup"><span data-stu-id="d5e48-220">Enabling text compression is an opportunity to improve the performance of the page.</span></span>  

<span data-ttu-id="d5e48-221">Сжатие текста — это сокращение размера текстового файла перед отправкой по сети, а также его сжатие.</span><span class="sxs-lookup"><span data-stu-id="d5e48-221">Text compression is when you reduce, or compress, the size of a text file before sending it over the network.</span></span>  <span data-ttu-id="d5e48-222">Например, вы можете почтовые индексы, чтобы уменьшить размер папки.</span><span class="sxs-lookup"><span data-stu-id="d5e48-222">Kind of like how you might zip a folder before emailing it to reduce the size.</span></span>  

<span data-ttu-id="d5e48-223">Перед включением сжатия вы можете вручную проверить, сжимаются ли текстовые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="d5e48-223">Before you enable compression, here are a couple of ways to manually check whether text resources are compressed.</span></span>  

1.  <span data-ttu-id="d5e48-224">Откройте вкладку **сеть** .</span><span class="sxs-lookup"><span data-stu-id="d5e48-224">Select the **Network** tab.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-remix-network.msft.png":::
       <span data-ttu-id="d5e48-226">Панель " **сеть** "</span><span class="sxs-lookup"><span data-stu-id="d5e48-226">The **Network** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d5e48-227">Выберите значок **Параметры сети** .</span><span class="sxs-lookup"><span data-stu-id="d5e48-227">Select the **Network setting** icon.</span></span>  
1.  <span data-ttu-id="d5e48-228">Установите флажок **использовать строки большого запроса** .</span><span class="sxs-lookup"><span data-stu-id="d5e48-228">Select the **Use Large Request Rows** checkbox.</span></span>  <span data-ttu-id="d5e48-229">Высота строк в таблице сетевых запросов возрастает.</span><span class="sxs-lookup"><span data-stu-id="d5e48-229">The height of the rows in the table of network requests increases.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-use-large-request-rows.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-remix-network-use-large-request-rows.msft.png":::
       <span data-ttu-id="d5e48-231">Большие строки в таблице "сетевые запросы"</span><span class="sxs-lookup"><span data-stu-id="d5e48-231">Large rows in the network requests table</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d5e48-232">Если столбец **Размер** не отображается в таблице сетевых запросов, щелкните заголовок таблицы и выберите команду **Размер**.</span><span class="sxs-lookup"><span data-stu-id="d5e48-232">If you do not see the **Size** column in the table of network requests, click the table header and then choose **Size**.</span></span>  

<span data-ttu-id="d5e48-233">В каждой ячейке **размера** отображаются два значения.</span><span class="sxs-lookup"><span data-stu-id="d5e48-233">Each **Size** cell shows two values.</span></span>  <span data-ttu-id="d5e48-234">Верхнее значение — размер загруженного ресурса.</span><span class="sxs-lookup"><span data-stu-id="d5e48-234">The top value is the size of the downloaded resource.</span></span>  
<span data-ttu-id="d5e48-235">Минимальное значение — размер несжатого ресурса.</span><span class="sxs-lookup"><span data-stu-id="d5e48-235">The bottom value is the size of the uncompressed resource.</span></span>  <span data-ttu-id="d5e48-236">Если оба значения совпадают, значит, ресурс не сжимается, когда он отправляется по сети.</span><span class="sxs-lookup"><span data-stu-id="d5e48-236">If the two values are the same, then the resource is not being compressed when it is sent over the network.</span></span>  <span data-ttu-id="d5e48-237">Например, на предыдущем рисунке значения Top и Bottom для параметров "" `bundle.js` — " `1.2 MB` и" `1.2 MB` ... ".</span><span class="sxs-lookup"><span data-stu-id="d5e48-237">For example, in the previous figure, the top and bottom values for `bundle.js` are `1.2 MB` and `1.2 MB`.</span></span>  

<span data-ttu-id="d5e48-238">Проверка на наличие сжатия с помощью проверки заголовков HTTP ресурса.</span><span class="sxs-lookup"><span data-stu-id="d5e48-238">Check for compression by inspecting the HTTP headers of a resource:</span></span>  

1.  <span data-ttu-id="d5e48-239">Выберите **bundle.js**.</span><span class="sxs-lookup"><span data-stu-id="d5e48-239">Choose **bundle.js**.</span></span>  
1.  <span data-ttu-id="d5e48-240">Откройте вкладку **заголовки** .</span><span class="sxs-lookup"><span data-stu-id="d5e48-240">Select the **Headers** tab.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-use-large-request-rows-bundle-js.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-remix-network-use-large-request-rows-bundle-js.msft.png":::
       <span data-ttu-id="d5e48-242">Вкладка " **заголовки** "</span><span class="sxs-lookup"><span data-stu-id="d5e48-242">The **Headers** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d5e48-243">Поиск заголовка в разделе **заголовков ответа** `content-encoding` .</span><span class="sxs-lookup"><span data-stu-id="d5e48-243">Search the **Response Headers** section for a `content-encoding` header.</span></span>  <span data-ttu-id="d5e48-244">Вы не видите один из них, то есть `bundle.js` не был сжат.</span><span class="sxs-lookup"><span data-stu-id="d5e48-244">You should not see one, meaning that `bundle.js` was not compressed.</span></span>  <span data-ttu-id="d5e48-245">Когда ресурс сжимается, этот верхний колонтитул обычно имеет значение `gzip` , `deflate` или `br` .</span><span class="sxs-lookup"><span data-stu-id="d5e48-245">When a resource is compressed, this header is usually set to `gzip`, `deflate`, or `br`.</span></span>  <span data-ttu-id="d5e48-246">Описание этих значений показано в разделе [директивы][MDNContentEncodingDirectives] .</span><span class="sxs-lookup"><span data-stu-id="d5e48-246">See [Directives][MDNContentEncodingDirectives] for an explanation of these values.</span></span>  

<span data-ttu-id="d5e48-247">Достаточно с пояснениями.</span><span class="sxs-lookup"><span data-stu-id="d5e48-247">Enough with the explanations.</span></span>  <span data-ttu-id="d5e48-248">Время, чтобы внести некоторые изменения!</span><span class="sxs-lookup"><span data-stu-id="d5e48-248">Time to make some changes!</span></span>  <span data-ttu-id="d5e48-249">Включите сжатие текста, добавив несколько строк кода.</span><span class="sxs-lookup"><span data-stu-id="d5e48-249">Enable text compression by adding a couple of lines of code:</span></span>  

1.  <span data-ttu-id="d5e48-250">На вкладке "редактор" выберите **server.js**.</span><span class="sxs-lookup"><span data-stu-id="d5e48-250">In the editor tab, choose **server.js**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-server-js.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-remix-server-js.msft.png":::
       <span data-ttu-id="d5e48-252">Edit</span><span class="sxs-lookup"><span data-stu-id="d5e48-252">Edit</span></span> `server.js`  
    :::image-end:::  
    
1.  <span data-ttu-id="d5e48-253">Добавьте следующий код для **server.js**.</span><span class="sxs-lookup"><span data-stu-id="d5e48-253">Add the following code to **server.js**.</span></span>  <span data-ttu-id="d5e48-254">Убедитесь, что он должен быть помещен `app.use(compression())` `app.use(express.static('build'))` .</span><span class="sxs-lookup"><span data-stu-id="d5e48-254">Make sure to put `app.use(compression())` before `app.use(express.static('build'))`.</span></span>  

    ```javascript
    const express = require('express');
    const app = express();
    const fs = require('fs');
    const compression = require('compression');

    app.use(compression());
    app.use(express.static('build'));
    
    const listener = app.listen(process.env.PORT || 1234, function () {
        console.log(`Listening on port ${listener.address().port}`);
    });
    ```  
    
    > [!NOTE]
    > <span data-ttu-id="d5e48-255">Как правило, вы должны установить `compression` пакет с помощью какого-либо вида `npm i -S compression` , но это еще не сделано.</span><span class="sxs-lookup"><span data-stu-id="d5e48-255">Usually, you have to install the `compression` package via something like `npm i -S compression`, but this has already been done for you.</span></span>  
    
1.  <span data-ttu-id="d5e48-256">Дождитесь, пока не будет развернуто новая сборка сайта.</span><span class="sxs-lookup"><span data-stu-id="d5e48-256">Wait for Glitch to deploy the new build of the site.</span></span>  <span data-ttu-id="d5e48-257">Неузорная анимация рядом с **инструментами** означает, что сайт перестраивается и повторно развертывается.</span><span class="sxs-lookup"><span data-stu-id="d5e48-257">The fancy animation next to **Tools** means that the site is getting rebuilt and redeployed.</span></span>  <span data-ttu-id="d5e48-258">Изменение будет готово, когда анимация рядом с пунктом " **инструменты** " исчезает.</span><span class="sxs-lookup"><span data-stu-id="d5e48-258">The change is ready when the animation next to **Tools** goes away.</span></span>  <span data-ttu-id="d5e48-259">Выберите команду **Показать** , а затем еще раз выберите **в новом окне** .</span><span class="sxs-lookup"><span data-stu-id="d5e48-259">Choose **Show** and choose **In a New Window** again.</span></span>  
    
    <!--
    :::image type="complex" source="../media/speed-glitch-tony-remix-server-js-edited.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-remix-server-js-edited.msft.png":::
       The animation that indicates that the site is getting built  
    :::image-end:::  
    -->  
    
<span data-ttu-id="d5e48-260">Используйте рабочие процессы, которые вы узнали ранее, чтобы вручную проверить, работает ли сжатие.</span><span class="sxs-lookup"><span data-stu-id="d5e48-260">Use the workflows that you learned earlier to manually check that the compression is working:</span></span>  

1.  <span data-ttu-id="d5e48-261">Вернитесь на вкладку Demo и повторно загрузите страницу.</span><span class="sxs-lookup"><span data-stu-id="d5e48-261">Go back to the demo tab and reload the page.</span></span>  <span data-ttu-id="d5e48-262">Столбец « **Размер** » теперь должен показывать 2 разных значения для текстовых ресурсов `bundle.js` , таких как.</span><span class="sxs-lookup"><span data-stu-id="d5e48-262">The **Size** column should now show 2 different values for text resources like `bundle.js`.</span></span>  <span data-ttu-id="d5e48-263">На рисунке после следующего значения аргумента " `256 KB` `bundle.js` равно" — Размер файла, отправленного по сети, а в качестве нижнего значения `1.2 MB` — несжатый размер файла.</span><span class="sxs-lookup"><span data-stu-id="d5e48-263">In the figure after the following, the top value of `256 KB` for `bundle.js` is the size of the file that was sent over the network, and the bottom value of `1.2 MB` is the uncompressed file size.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-main.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-remix-network-main.msft.png":::
       <span data-ttu-id="d5e48-265">В столбце " **Размер** " теперь показано 2 разных значения для текстовых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d5e48-265">The **Size** column now shows 2 different values for text resources</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d5e48-266">В разделе **заголовки ответа** `bundle.js` теперь должен быть указан `content-encoding: gzip` верхний колонтитул.</span><span class="sxs-lookup"><span data-stu-id="d5e48-266">The **Response Headers** section for `bundle.js` should now include a `content-encoding: gzip` header.</span></span>
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-bundle-js-headers-response.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-remix-network-bundle-js-headers-response.msft.png":::
       <span data-ttu-id="d5e48-268">Раздел **заголовки ответа** теперь содержат заголовок Content-Encoding</span><span class="sxs-lookup"><span data-stu-id="d5e48-268">The **Response Headers** section now contains a content-encoding header</span></span>  
    :::image-end:::  
    
<span data-ttu-id="d5e48-269">Проведите аудит страницы, чтобы оценить, какое влияние сжатие текста влияет на производительность загрузки страницы:</span><span class="sxs-lookup"><span data-stu-id="d5e48-269">Audit the page again to measure what kind of impact text compression has on the load performance of the page:</span></span>  

1.  <span data-ttu-id="d5e48-270">Перейдите на вкладку **Аудит** .</span><span class="sxs-lookup"><span data-stu-id="d5e48-270">Select the **Audits** tab.</span></span>  
1.  <span data-ttu-id="d5e48-271">Выберите команду **выполнить аудит** \ ( ![ выполнить аудит ][ImagePerformIcon] \).</span><span class="sxs-lookup"><span data-stu-id="d5e48-271">Choose **Perform an audit** \(![Perform an audit][ImagePerformIcon]\).</span></span>  
1.  <span data-ttu-id="d5e48-272">Параметры не совпадают.</span><span class="sxs-lookup"><span data-stu-id="d5e48-272">Leave the settings the same as before.</span></span>  
1.  <span data-ttu-id="d5e48-273">Выберите команду **запустить аудит**.</span><span class="sxs-lookup"><span data-stu-id="d5e48-273">Choose **Run audit**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance.msft.png":::
       <span data-ttu-id="d5e48-275">Отчет "Аудит" после включения сжатия текста</span><span class="sxs-lookup"><span data-stu-id="d5e48-275">An Audits report after enabling text compression</span></span>  
    :::image-end:::  
    
<!--  Woohoo!  That looks like progress.  -->  <span data-ttu-id="d5e48-276">Общая оценка производительности должна быть увеличена, а это значит, что сайт быстрее.</span><span class="sxs-lookup"><span data-stu-id="d5e48-276">Your overall performance score should have increased, meaning that the site is getting faster.</span></span>  

#### <span data-ttu-id="d5e48-277">Сжатие текста в реальном мире</span><span class="sxs-lookup"><span data-stu-id="d5e48-277">Text compression in the real world</span></span>  

<span data-ttu-id="d5e48-278">На большинстве серверов есть простые решения, подобные этим, чтобы включить сжатие.</span><span class="sxs-lookup"><span data-stu-id="d5e48-278">Most servers really do have simple fixes like this for enabling compression!</span></span>  <span data-ttu-id="d5e48-279">Просто выполните поиск, чтобы настроить любой сервер, который вы используете для сжатия текста.</span><span class="sxs-lookup"><span data-stu-id="d5e48-279">Just do a search on how to configure whatever server you use to compress text.</span></span>  

### <span data-ttu-id="d5e48-280">Изменение размера изображения</span><span class="sxs-lookup"><span data-stu-id="d5e48-280">Resize images</span></span>  

<span data-ttu-id="d5e48-281">Отчет о том, что не следует избегать огромных полезных данных сети, является одной из самых первых возможностей для повышения производительности страницы.</span><span class="sxs-lookup"><span data-stu-id="d5e48-281">Your report indicates that avoiding enormous network payloads is one of the top opportunities for improving the performance of the page.</span></span>  <span data-ttu-id="d5e48-282">Изменение размеров изображений помогает уменьшить размер полезных данных в сети.</span><span class="sxs-lookup"><span data-stu-id="d5e48-282">Resizing images helps reduce the size of the network payload.</span></span>  <span data-ttu-id="d5e48-283">Если пользователь просматривает изображения на экране мобильного устройства размером 500 в пикселах, это не значит, что при отправке изображения в масштабе не более 1500 точек.</span><span class="sxs-lookup"><span data-stu-id="d5e48-283">If your user is viewing your images on a mobile device screen that is 500-pixels-wide, there is really no point in sending a 1500-pixel-wide image.</span></span>  <span data-ttu-id="d5e48-284">В идеале вы отправляете изображение в 500 в масштабе по пикселю.</span><span class="sxs-lookup"><span data-stu-id="d5e48-284">Ideally, you send a 500-pixel-wide image, at most.</span></span>  

1.  <span data-ttu-id="d5e48-285">В отчете выберите **исключить огромные полезные данные сети** , чтобы узнать, какие изображения нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="d5e48-285">In your report, choose **Avoid enormous network payloads** to see which images should be resized.</span></span>  <span data-ttu-id="d5e48-286">Похоже, что 2 файлов JPG — более 2000 КБ, что больше не требуется.</span><span class="sxs-lookup"><span data-stu-id="d5e48-286">It looks like 2 of the jpg files are over 2000 KB, which is bigger than necessary.</span></span>  
    
    <!--
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-opportunities-expanded.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-opportunities-expanded.msft.png":::
       Details about the properly size images opportunity  
    :::image-end:::  
    -->
    
1.  <span data-ttu-id="d5e48-287">Вернувшись на вкладку Редактор, открыть `src/model.js` .</span><span class="sxs-lookup"><span data-stu-id="d5e48-287">Back in the editor tab, open `src/model.js`.</span></span>  
1.  <span data-ttu-id="d5e48-288">Заменить `const dir = 'big'` на `const dir = 'small'` .</span><span class="sxs-lookup"><span data-stu-id="d5e48-288">Replace `const dir = 'big'` with `const dir = 'small'`.</span></span>  <span data-ttu-id="d5e48-289">Этот каталог содержит копии тех же изображений, размер которых был изменен.</span><span class="sxs-lookup"><span data-stu-id="d5e48-289">This directory contains copies of the same images which have been resized.</span></span>  
1.  <span data-ttu-id="d5e48-290">Вновь проведите аудит страницы, чтобы увидеть, как это изменение влияет на производительность загрузки.</span><span class="sxs-lookup"><span data-stu-id="d5e48-290">Audit the page again to see how this change affects load performance.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-compression-small-images-audits-performance.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-compression-small-images-audits-performance.msft.png":::
       <span data-ttu-id="d5e48-292">Отчет об аудите после изменения размеров изображений</span><span class="sxs-lookup"><span data-stu-id="d5e48-292">An Audits report after resizing images</span></span>  
    :::image-end:::  
    
<span data-ttu-id="d5e48-293">Похоже, что изменение имеет незначительный уровень влияния на общую оценку производительности.</span><span class="sxs-lookup"><span data-stu-id="d5e48-293">Looks like the change only has a minor affect on the overall performance score.</span></span>  <span data-ttu-id="d5e48-294">Тем не менее, в этом случае баллы не показываются четко, так как данные сети, которые вы сохраняете, не отображаются.</span><span class="sxs-lookup"><span data-stu-id="d5e48-294">However, one thing that the score does not show clearly is how much network data you are saving your users.</span></span>  <span data-ttu-id="d5e48-295">Общий размер старой фотографии — около 5,3 мегабайт, в то время как теперь это не более 0,18 МБ.</span><span class="sxs-lookup"><span data-stu-id="d5e48-295">The total size of the old photos was around 5.3 megabytes, whereas now it is only about 0.18 megabytes.</span></span>  

#### <span data-ttu-id="d5e48-296">Изменение размеров изображений в реальном мире</span><span class="sxs-lookup"><span data-stu-id="d5e48-296">Resizing images in the real world</span></span>  

<span data-ttu-id="d5e48-297">В случае с небольшим приложением вы можете использовать один из этих способов, так как это может быть достаточно хорошим.</span><span class="sxs-lookup"><span data-stu-id="d5e48-297">For a small app, doing a one-off resize like this may be good enough.</span></span>  <span data-ttu-id="d5e48-298">Но для больших приложений это очевидно не масштабируется.</span><span class="sxs-lookup"><span data-stu-id="d5e48-298">But for a large app, this obviously is not scalable.</span></span>  <span data-ttu-id="d5e48-299">Ниже приведены некоторые стратегии управления изображениями в крупных приложениях.</span><span class="sxs-lookup"><span data-stu-id="d5e48-299">Here are some strategies for managing images in large apps:</span></span>  

*   <span data-ttu-id="d5e48-300">Изменение размера изображения во время процесса сборки.</span><span class="sxs-lookup"><span data-stu-id="d5e48-300">Resize images during your build process.</span></span>  
*   <span data-ttu-id="d5e48-301">Создавайте несколько размеров изображения во время процесса сборки, а затем используйте `srcset` их в коде.</span><span class="sxs-lookup"><span data-stu-id="d5e48-301">Create multiple sizes of each image during the build process and then use `srcset` in your code.</span></span>  <span data-ttu-id="d5e48-302">Во время выполнения браузер берет на себя выбор оптимального размера для устройства.</span><span class="sxs-lookup"><span data-stu-id="d5e48-302">At runtime, the browser takes care of choosing which size is best for the device.</span></span>  
    <!--See [Relative-sized images][relative].  -->
    
<!--[relative]: /web/fundamentals/design-and-ux/responsive/images#relative_sized_images  -->  

*   <span data-ttu-id="d5e48-303">Использование сети CDN изображений, позволяющей динамически изменять размер изображения при запросе.</span><span class="sxs-lookup"><span data-stu-id="d5e48-303">Use an image CDN that lets you dynamically resize an image when you request it.</span></span>  
*   <span data-ttu-id="d5e48-304">По крайней мере, оптимизируйте каждое изображение.</span><span class="sxs-lookup"><span data-stu-id="d5e48-304">At the very least, optimize each image.</span></span>  <span data-ttu-id="d5e48-305">Это может создать огромный выигрыш.</span><span class="sxs-lookup"><span data-stu-id="d5e48-305">This may create huge savings.</span></span>  
  <span data-ttu-id="d5e48-306">Оптимизация — это время, когда вы запускаете изображение с помощью специальной программы, которая уменьшает размер файла изображения.</span><span class="sxs-lookup"><span data-stu-id="d5e48-306">Optimization is when you run an image through a special program that reduces the size of the image file.</span></span>  <span data-ttu-id="d5e48-307">Дополнительные советы приведены в статье основные сведения об [оптимизации изображений][EssentialImageOptimization] .</span><span class="sxs-lookup"><span data-stu-id="d5e48-307">See [Essential Image Optimization][EssentialImageOptimization] for more tips.</span></span>  
    
### <span data-ttu-id="d5e48-308">Исключение ресурсов блокировки рендеринга</span><span class="sxs-lookup"><span data-stu-id="d5e48-308">Eliminate render-blocking resources</span></span>  

<span data-ttu-id="d5e48-309">В последней версии отчета говорится о том, что в настоящее время ресурсы, блокирующие рендеринг, стали самой большой возможностью.</span><span class="sxs-lookup"><span data-stu-id="d5e48-309">Your latest report says that eliminating render-blocking resources is now the biggest opportunity.</span></span>  

<span data-ttu-id="d5e48-310">Ресурс блокировки обработки — это внешний файл JavaScript или CSS, который браузер должен загрузить, проанализировать и выполнить, прежде чем отобразить страницу.</span><span class="sxs-lookup"><span data-stu-id="d5e48-310">A render-blocking resource is an external JavaScript or CSS file that the browser must download, parse, and run before it displays the page.</span></span>  <span data-ttu-id="d5e48-311">Цель состоит в том, чтобы запустить только основной код CSS и JavaScript, необходимый для правильного отображения страницы.</span><span class="sxs-lookup"><span data-stu-id="d5e48-311">The goal is to only run the core CSS and JavaScript code that is required to display the page properly.</span></span>  

<span data-ttu-id="d5e48-312">Первая задача — это поиск кода, который не нужно выполнять при загрузке страницы.</span><span class="sxs-lookup"><span data-stu-id="d5e48-312">The first task, then, is to find code that you do not need to run on page load.</span></span>  

1.  <span data-ttu-id="d5e48-313">Чтобы просмотреть блокируемые ресурсы, нажмите кнопку **удалить ресурсы блокировки рендеринга** .</span><span class="sxs-lookup"><span data-stu-id="d5e48-313">Choose **Eliminate render-blocking resources** to see the resources that are blocking:</span></span>  
    `lodash.js` <span data-ttu-id="d5e48-314">и `jquery.js` .</span><span class="sxs-lookup"><span data-stu-id="d5e48-314">and `jquery.js`.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded.msft.png":::
       <span data-ttu-id="d5e48-316">Дополнительные сведения о **ресурсах блокировки обработки** с возможностью устранения</span><span class="sxs-lookup"><span data-stu-id="d5e48-316">More information about the **Eliminate render-blocking resources** opportunity</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d5e48-317">Выберите `Control` + `Shift` + `P` \ (Windows, Linux \) или `Command` + `Shift` + `P` \ (macOS \), чтобы открыть меню команд, начните вводить текст `Coverage` , а затем выберите команду **Показать покрытие**.</span><span class="sxs-lookup"><span data-stu-id="d5e48-317">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu, start typing `Coverage`, and then choose **Show Coverage**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-command-coverage.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-command-coverage.msft.png":::
       <span data-ttu-id="d5e48-319">Открытие меню "команд" на панели " **Аудит** "</span><span class="sxs-lookup"><span data-stu-id="d5e48-319">Open the Command Menu from the **Audits** panel</span></span>  
    :::image-end:::  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage.msft.png":::
       <span data-ttu-id="d5e48-321">Вкладка " **покрытие** "</span><span class="sxs-lookup"><span data-stu-id="d5e48-321">The **Coverage** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d5e48-322">Нажмите кнопку **Обновить** \ ( ![ обновить ][ImageRefreshIcon] \).</span><span class="sxs-lookup"><span data-stu-id="d5e48-322">Choose **Refresh** \(![Refresh][ImageRefreshIcon]\).</span></span>  <span data-ttu-id="d5e48-323">На вкладке " **покрытие** " представлены общие сведения о том, какая часть `bundle.js` кода `jquery.js` и `lodash.js` выполняется при загрузке страницы.</span><span class="sxs-lookup"><span data-stu-id="d5e48-323">The **Coverage** tab provides an overview of how much of the code in `bundle.js`, `jquery.js`, and `lodash.js` runs while the page loads.</span></span>  <span data-ttu-id="d5e48-324">На рисунке ниже показано, что около 76% и 30% файлов jQuery и Lodash не используются соответственно.</span><span class="sxs-lookup"><span data-stu-id="d5e48-324">In the figure after the following, about 76% and 30% of the jQuery and Lodash files are not used, respectively.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage-reloaded.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage-reloaded.msft.png":::
       <span data-ttu-id="d5e48-326">Отчет о покрытии</span><span class="sxs-lookup"><span data-stu-id="d5e48-326">The Coverage report</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d5e48-327">Выделите строку **jquery.js** .</span><span class="sxs-lookup"><span data-stu-id="d5e48-327">Select the **jquery.js** row.</span></span>  <span data-ttu-id="d5e48-328">DevTools откроет файл на панели «источники».</span><span class="sxs-lookup"><span data-stu-id="d5e48-328">DevTools opens the file in the Sources panel.</span></span>  <span data-ttu-id="d5e48-329">Строка кода была выполнена, если рядом с ней есть синяя полоска.</span><span class="sxs-lookup"><span data-stu-id="d5e48-329">A line of code ran if it has a blue bar next to it.</span></span>  <span data-ttu-id="d5e48-330">Красная черта означает, что она не была выполнена и определенно не требуется при загрузке страницы.</span><span class="sxs-lookup"><span data-stu-id="d5e48-330">A red bar means it was not run, and is definitely not needed on page load.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-sources-drawer-coverage-reloaded-jquery-js.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-remix-updated-sources-drawer-coverage-reloaded-jquery-js.msft.png":::
       <span data-ttu-id="d5e48-332">Просмотр файла jQuery на панели « **источники** »</span><span class="sxs-lookup"><span data-stu-id="d5e48-332">Viewing the jQuery file in the **Sources** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d5e48-333">Прокрутите код jQuery на немного.</span><span class="sxs-lookup"><span data-stu-id="d5e48-333">Scroll through the jQuery code a bit.</span></span>  <span data-ttu-id="d5e48-334">Некоторые строки, которые получают слово "выполнить", на самом деле представляют собой комментарии.</span><span class="sxs-lookup"><span data-stu-id="d5e48-334">Some of the lines that get "run" are actually just comments.</span></span>  <span data-ttu-id="d5e48-335">Выполнение этого кода с помощью Minifier, который содержит примечания, — еще один способ уменьшить размер файла.</span><span class="sxs-lookup"><span data-stu-id="d5e48-335">Running this code through a minifier that strips comments is another way to reduce the size of this file.</span></span>  

<span data-ttu-id="d5e48-336">Коротко говоря, при работе с собственным кодом вкладка "покрытие" помогает проанализировать код, построчно и поставлять только код, необходимый для загрузки страницы.</span><span class="sxs-lookup"><span data-stu-id="d5e48-336">In short, when you are working with your own code, the Coverage tab helps you analyze your code, line-by-line, and only ship the code that is needed for page load.</span></span>  

<span data-ttu-id="d5e48-337">Нужны ли `jquery.js` `lodash.js` файлы и даже для загрузки страницы?</span><span class="sxs-lookup"><span data-stu-id="d5e48-337">Are the `jquery.js` and `lodash.js` files even needed to load the page?</span></span>  <span data-ttu-id="d5e48-338">На вкладке Блокировка запроса показано, что происходит, когда ресурсы недоступны.</span><span class="sxs-lookup"><span data-stu-id="d5e48-338">The Request Blocking tab displays what happens when resources are not available.</span></span>  

1.  <span data-ttu-id="d5e48-339">Откройте вкладку **сеть** .</span><span class="sxs-lookup"><span data-stu-id="d5e48-339">Select the **Network** tab.</span></span>  
1.  <span data-ttu-id="d5e48-340">Выберите `Control` + `Shift` + `P` \ (Windows, Linux \) или `Command` + `Shift` + `P` \ (macOS \), чтобы снова открыть меню команд.</span><span class="sxs-lookup"><span data-stu-id="d5e48-340">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu again.</span></span>  
1.  <span data-ttu-id="d5e48-341">Начните вводить данные `blocking` и выберите команду **Показать блокировку запросов**.</span><span class="sxs-lookup"><span data-stu-id="d5e48-341">Start typing `blocking` and then choose **Show Request Blocking**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-empty.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-empty.msft.png":::
       <span data-ttu-id="d5e48-343">Вкладка " **Блокировка запросов** "</span><span class="sxs-lookup"><span data-stu-id="d5e48-343">The **Request Blocking** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d5e48-344">Нажмите кнопку **Добавить узор** \ ( ![ Добавить шаблон ][ImageAddPatternIcon] \), введите `/libs/*` и выберите `Enter` для подтверждения.</span><span class="sxs-lookup"><span data-stu-id="d5e48-344">Choose **Add Pattern** \(![Add Pattern][ImageAddPatternIcon]\), type `/libs/*`, and then select `Enter` to confirm.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-added.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-added.msft.png":::
       <span data-ttu-id="d5e48-346">Добавление шаблона для блокирования запросов в `libs` Каталог</span><span class="sxs-lookup"><span data-stu-id="d5e48-346">Add a pattern to block any request to the `libs` directory</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d5e48-347">Обновите страницу.</span><span class="sxs-lookup"><span data-stu-id="d5e48-347">Refresh the page.</span></span>  <span data-ttu-id="d5e48-348">Запросы jQuery и Lodash красного цвета, означающие, что запросы были заблокированы.</span><span class="sxs-lookup"><span data-stu-id="d5e48-348">The jQuery and Lodash requests are red, meaning that the requests were blocked.</span></span>   <span data-ttu-id="d5e48-349">Страница по-прежнему загружается и является интерактивной, поэтому она выглядит так, как это не требуется.</span><span class="sxs-lookup"><span data-stu-id="d5e48-349">The page still loads and is interactive, so it looks like these resources are not needed whatsoever!</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-network-reloaded-drawer-request-blocking-added.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-remix-updated-network-reloaded-drawer-request-blocking-added.msft.png":::
       <span data-ttu-id="d5e48-351">На панели **Network (сеть** ) показано, что запросы заблокированы</span><span class="sxs-lookup"><span data-stu-id="d5e48-351">The **Network** panel shows that the requests have been blocked</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d5e48-352">Выберите команду **удалить все шаблоны** \ ( ![ удалить все шаблоны ][ImageRemoveIcon] \), чтобы удалить `/libs/*` шаблон блокировки.</span><span class="sxs-lookup"><span data-stu-id="d5e48-352">Choose **Remove all patterns** \(![Remove all patterns][ImageRemoveIcon]\) to delete the `/libs/*` blocking pattern.</span></span>  
    
<span data-ttu-id="d5e48-353">Как правило, вкладка "блокировка запросов" полезна для имитации того, как работает страница, если какой-либо из указанных ресурсов недоступен.</span><span class="sxs-lookup"><span data-stu-id="d5e48-353">In general, the Request Blocking tab is useful for simulating how your page behaves when any given resource is not available.</span></span>  

<span data-ttu-id="d5e48-354">Теперь удалите ссылки на эти файлы из кода и выполните аудит страницы еще раз:</span><span class="sxs-lookup"><span data-stu-id="d5e48-354">Now, remove the references to these files from the code and audit the page again:</span></span>  

1.  <span data-ttu-id="d5e48-355">Вернувшись на вкладку Редактор, открыть `template.html` .</span><span class="sxs-lookup"><span data-stu-id="d5e48-355">Back in the editor tab, open `template.html`.</span></span>  
1.  <span data-ttu-id="d5e48-356">Удалите `<script src="/libs/lodash.js">` и `<script src="/libs/jquery.js"></script>`.</span><span class="sxs-lookup"><span data-stu-id="d5e48-356">Delete `<script src="/libs/lodash.js">` and `<script src="/libs/jquery.js"></script>`.</span></span>  
1.  <span data-ttu-id="d5e48-357">Дождитесь повторного создания и повторного развертывания сайта.</span><span class="sxs-lookup"><span data-stu-id="d5e48-357">Wait for the site to re-build and re-deploy.</span></span>  
1.  <span data-ttu-id="d5e48-358">Снова проведите аудит страницы с помощью панели **аудита** .</span><span class="sxs-lookup"><span data-stu-id="d5e48-358">Audit the page again from the **Audits** panel.</span></span>  <span data-ttu-id="d5e48-359">Ваши общие баллы должны быть улучшены.</span><span class="sxs-lookup"><span data-stu-id="d5e48-359">Your overall score should have improved again.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-2-audits-performance.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-remix-updated-2-audits-performance.msft.png":::
       <span data-ttu-id="d5e48-361">Отчет об **аудите** после удаления ресурсов блокировки рендеринга</span><span class="sxs-lookup"><span data-stu-id="d5e48-361">An **Audits** report after removing the render-blocking resources</span></span>  
    :::image-end:::  
    
#### <span data-ttu-id="d5e48-362">Оптимизация критического пути отрисовки в реальном мире</span><span class="sxs-lookup"><span data-stu-id="d5e48-362">Optimizing the Critical Rendering Path in the real-world</span></span>  

<span data-ttu-id="d5e48-363">**Критический путь рендеринга** указывает на код, необходимый для загрузки страницы.</span><span class="sxs-lookup"><span data-stu-id="d5e48-363">The **Critical Rendering Path** refers to the code that you need to load a page.</span></span>  <span data-ttu-id="d5e48-364">Как правило, скорость загрузки страницы повышается за счет отправки критического кода только при загрузке страницы, а затем — через отложенную загрузку всех остальных.</span><span class="sxs-lookup"><span data-stu-id="d5e48-364">In general, speed up page load by only shipping critical code during the page load, and then lazy-loading everything else.</span></span>  

<!--[CRP]: /web/fundamentals/performance/critical-rendering-path/  -->  

*   <span data-ttu-id="d5e48-365">Маловероятно, что вы можете найти сценарии, которые можно удалить прямо, но вы можете найти большое количество сценариев, которые вам не нужно запрашивать во время загрузки страницы, и, возможно, они будут запрашиваться асинхронно.</span><span class="sxs-lookup"><span data-stu-id="d5e48-365">It is unlikely that you are able to find scripts that you are able to remove outright, but you may find many scripts that you do not need to request during the page load, and instead may be requested asynchronously.</span></span>  <!--See [Using async or defer][async].  -->  
*   <span data-ttu-id="d5e48-366">Если вы используете платформу, убедитесь в том, что у нее есть производственный режим.</span><span class="sxs-lookup"><span data-stu-id="d5e48-366">If you are using a framework, check if it has a production mode.</span></span>  <span data-ttu-id="d5e48-367">Этот режим может использовать такие функции, как [Tree встряхнув][WebpackTreeShaking] , для удаления ненужного кода, блокирующего критический рендеринг.</span><span class="sxs-lookup"><span data-stu-id="d5e48-367">This mode may use a feature such as [tree shaking][WebpackTreeShaking] in order to eliminate unnecessary code that is blocking the critical render.</span></span>  
    
<!--[async]: /web/fundamentals/performance/optimizing-content-efficiency/loading-third-party-javascript/#use_async_or_defer  -->  

### <span data-ttu-id="d5e48-368">Работа менее основного потока</span><span class="sxs-lookup"><span data-stu-id="d5e48-368">Do less main thread work</span></span>  

<span data-ttu-id="d5e48-369">В последней версии отчета представлены некоторые небольшие возможности по экономии средств в разделе "возможности", но если вы просмотрии раздел "Диагностика", это похоже на то, что наибольший узкий участок слишком велик для основного потока.</span><span class="sxs-lookup"><span data-stu-id="d5e48-369">Your latest report shows some minor potential savings in the Opportunities section, but if you look down in the Diagnostics section, it looks like the biggest bottleneck is too much main thread activity.</span></span>  

<span data-ttu-id="d5e48-370">Основной поток — это тот случай, когда браузер выполняет большую часть работы, необходимой для отображения страницы, например синтаксического анализа и выполнения HTML, CSS и JavaScript.</span><span class="sxs-lookup"><span data-stu-id="d5e48-370">The main thread is where the browser does most of the work needed to display a page, such as parsing and running HTML, CSS, and JavaScript.</span></span>  

<span data-ttu-id="d5e48-371">Цель состоит в том, чтобы проанализировать трудозатраты, выполняемые основным потоком при загрузке страницы, и найти способы задержать или удалить ненужные данные.</span><span class="sxs-lookup"><span data-stu-id="d5e48-371">The goal is to use the Performance panel to analyze what work the main thread is doing while the page loads, and find ways to defer or remove unnecessary work.</span></span>  

1.  <span data-ttu-id="d5e48-372">Откройте вкладку **производительность** .</span><span class="sxs-lookup"><span data-stu-id="d5e48-372">Select the **Performance** tab.</span></span>  
1.  <span data-ttu-id="d5e48-373">Выберите **Параметры захвата** \ ( ![ Параметры захвата ][ImageCaptureIcon] ).</span><span class="sxs-lookup"><span data-stu-id="d5e48-373">Choose **Capture Settings** \(![Capture Settings][ImageCaptureIcon]\).</span></span>  
1.  <span data-ttu-id="d5e48-374">Настройте **сеть** на **медленное 3G** и **ЦП** , чтобы **6X замедление**.</span><span class="sxs-lookup"><span data-stu-id="d5e48-374">Set **Network** to **Slow 3G** and **CPU** to **6x slowdown**.</span></span>  <span data-ttu-id="d5e48-375">На мобильных устройствах обычно используются больше ограничений на оборудование, чем на ноутбуках или настольных компьютерах, поэтому эти параметры позволяют загрузить страницу так, как если бы вы использовали менее мощное устройство.</span><span class="sxs-lookup"><span data-stu-id="d5e48-375">Mobile devices typically have more hardware constraints than laptops or desktops, so these settings let you experience the page load as if you were using a less powerful device.</span></span>  
1.  <span data-ttu-id="d5e48-376">Нажмите кнопку **Обновить** \ ( ![ обновить ][ImageRefreshIcon] \).</span><span class="sxs-lookup"><span data-stu-id="d5e48-376">Choose **Refresh** \(![Refresh][ImageRefreshIcon]\).</span></span>  <span data-ttu-id="d5e48-377">DevTools обновляет страницу и создает визуализацию всей выполненной работы, чтобы загрузить страницу.</span><span class="sxs-lookup"><span data-stu-id="d5e48-377">DevTools refreshes the page and then produces a visualization of all the work performed in order to load the page.</span></span>  <span data-ttu-id="d5e48-378">Этот зрительный образ называется **трассировкой**.</span><span class="sxs-lookup"><span data-stu-id="d5e48-378">This visualization is referred to as the **trace**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu.msft.png":::
       <span data-ttu-id="d5e48-380">Трассировка загрузки страницы на панели **производительности**</span><span class="sxs-lookup"><span data-stu-id="d5e48-380">The **Performance** panel trace of the page load</span></span>  
    :::image-end:::  
    
<span data-ttu-id="d5e48-381">Трассировка отображает операцию в хронологическом порядке, слева направо.</span><span class="sxs-lookup"><span data-stu-id="d5e48-381">The trace shows activity chronologically, from left to right.</span></span>  <span data-ttu-id="d5e48-382">На диаграммах с частотой кадров, ЦП и нетто в верхней части экрана дается обзор кадров в секунду, активности ЦП и активности сети.</span><span class="sxs-lookup"><span data-stu-id="d5e48-382">The FPS, CPU, and NET charts at the top give you an overview of frames per second, CPU activity, and network activity.</span></span>  <span data-ttu-id="d5e48-383">Выделенный блок желтого цвета, показанный на рисунке после следующего, ЦП полностью загружен с действиями в сценарии.</span><span class="sxs-lookup"><span data-stu-id="d5e48-383">The block of yellow selected that you see in the figure after the following, the CPU was completely busy with scripting activity.</span></span>  <span data-ttu-id="d5e48-384">Это говорит о том, что вы можете ускорить загрузку страницы, выполнив меньше действий JavaScript.</span><span class="sxs-lookup"><span data-stu-id="d5e48-384">This is a clue that you may be able to speed up page load by doing less JavaScript work.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main-highlight.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main-highlight.msft.png":::
   <span data-ttu-id="d5e48-386">Раздел обзора трассировки</span><span class="sxs-lookup"><span data-stu-id="d5e48-386">The Overview section of the trace</span></span>  
:::image-end:::  

<span data-ttu-id="d5e48-387">Изучите трассировку, чтобы найти способы выполнения меньшей работы в JavaScript.</span><span class="sxs-lookup"><span data-stu-id="d5e48-387">Investigate the trace to find ways to do less JavaScript work:</span></span>  

1.  <span data-ttu-id="d5e48-388">Щелкните раздел **время показа** , чтобы развернуть его.</span><span class="sxs-lookup"><span data-stu-id="d5e48-388">Select the **Timings** section to expand it.</span></span>  <span data-ttu-id="d5e48-389">В зависимости от того факта, что существует ряд мер [времени][MDNUserTimingApi] , не отклика, может показаться, что приложение Илья использует режим разработки реагируй.</span><span class="sxs-lookup"><span data-stu-id="d5e48-389">Based on the fact that there may be a bunch of [Timings][MDNUserTimingApi] measures from React, it seems like Tony's app is using the development mode of React.</span></span>  <span data-ttu-id="d5e48-390">Переключение в режим рабочего режима может привести к снижению производительности WINS.</span><span class="sxs-lookup"><span data-stu-id="d5e48-390">Switching to the production mode of React may yield some easy performance wins.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings.msft.png":::
       <span data-ttu-id="d5e48-392">Раздел " **временные интервалы** "</span><span class="sxs-lookup"><span data-stu-id="d5e48-392">The **Timings** section</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d5e48-393">Чтобы свернуть этот раздел, выберите **время показа** еще раз.</span><span class="sxs-lookup"><span data-stu-id="d5e48-393">Choose **Timings** again to collapse that section.</span></span>  
1.  <span data-ttu-id="d5e48-394">Просмотрите **основной** раздел.</span><span class="sxs-lookup"><span data-stu-id="d5e48-394">Browse the **Main** section.</span></span>  <span data-ttu-id="d5e48-395">В этом разделе показан хронологический журнал основных операций потока, слева направо.</span><span class="sxs-lookup"><span data-stu-id="d5e48-395">This section shows a chronological log of main thread activity, from left to right.</span></span>  <span data-ttu-id="d5e48-396">Ось y (сверху вниз) показывает причины возникновения событий.</span><span class="sxs-lookup"><span data-stu-id="d5e48-396">The y-axis (top to bottom) shows why events occurred.</span></span>  <span data-ttu-id="d5e48-397">Например, в figyre после указанных ниже `Evaluate Script` событий событие привело `(anonymous)` к выполнению функции, которое привело к выполнению `(anonymous)` `__webpack__require__` и т. д.</span><span class="sxs-lookup"><span data-stu-id="d5e48-397">For example, in the figyre after the following, the `Evaluate Script` event caused the `(anonymous)` function to run, which caused `(anonymous)` to run, which caused `__webpack__require__` to run, and so on.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main.msft.png":::
       <span data-ttu-id="d5e48-399">**Основной** раздел</span><span class="sxs-lookup"><span data-stu-id="d5e48-399">The **Main** section</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d5e48-400">Прокрутите страницу вниз до конца **основного** раздела.</span><span class="sxs-lookup"><span data-stu-id="d5e48-400">Scroll down to the bottom of the **Main** section.</span></span>  <span data-ttu-id="d5e48-401">При использовании платформы большая часть верхнего действия вызывается платформой, которая обычно находится в вашем элементе управления.</span><span class="sxs-lookup"><span data-stu-id="d5e48-401">When you use a framework, most of the upper activity is caused by the framework, which is usually out of your control.</span></span>  <span data-ttu-id="d5e48-402">Действия, вызванные вашим приложением, обычно находятся в нижней части экрана.</span><span class="sxs-lookup"><span data-stu-id="d5e48-402">The activity caused by your app is usually at the bottom.</span></span>  <span data-ttu-id="d5e48-403">В этом приложении это похоже на функцию с именем, которая `App` вызывает большое количество запросов к `mineBitcoin` функции.</span><span class="sxs-lookup"><span data-stu-id="d5e48-403">In this app, it seems like a function named `App` is causing a lot of requests to a `mineBitcoin` function.</span></span>  <span data-ttu-id="d5e48-404">Это звучит так, как Илья может использовать устройства своего вентилятора для cryptocurrency...</span><span class="sxs-lookup"><span data-stu-id="d5e48-404">It sounds like Tony might be using the devices of his fans to mine cryptocurrency...</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-minebitcoin.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-minebitcoin.msft.png":::
       <span data-ttu-id="d5e48-406">Наведение указателя на `mineBitcoin` мероприятие</span><span class="sxs-lookup"><span data-stu-id="d5e48-406">Hover on the `mineBitcoin` activity</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="d5e48-407">Несмотря на то что запросы вашей платформы обычно прерываются из вашего элемента управления, иногда вы можете структурировать приложение таким образом, чтобы она выполнялась неэффективно.</span><span class="sxs-lookup"><span data-stu-id="d5e48-407">Although the requests that your framework makes are usually out of your control, sometimes you may structure your app in a way that causes the framework to run inefficiently.</span></span>  <span data-ttu-id="d5e48-408">Реструктуризация приложения для эффективного использования инфраструктуры — это способ выполнения менее основного потока работ.</span><span class="sxs-lookup"><span data-stu-id="d5e48-408">Restructuring your app to use the framework efficiently is a way to do less main thread work.</span></span>  <span data-ttu-id="d5e48-409">Тем не менее, для этого необходимо глубокое понимание того, как работает ваша платформа, и какие изменения вносятся в вашем собственном коде для более эффективной работы с платформой.</span><span class="sxs-lookup"><span data-stu-id="d5e48-409">However, this requires a deep understanding of how your framework works, and what kind of changes you make in your own code in order to use the framework more efficiently.</span></span>  
    
1.  <span data-ttu-id="d5e48-410">Разверните раздел **снизу вверх** .</span><span class="sxs-lookup"><span data-stu-id="d5e48-410">Expand the **Bottom-Up** section.</span></span>  <span data-ttu-id="d5e48-411">На этой вкладке прерываются действия, которые выполнялись в течение всего времени.</span><span class="sxs-lookup"><span data-stu-id="d5e48-411">This tab breaks down what activities took up the most time.</span></span>  <span data-ttu-id="d5e48-412">Если вы ничего не видите в разделе Bottom-Up, щелкните надпись для **основного** раздела.</span><span class="sxs-lookup"><span data-stu-id="d5e48-412">If you do not see anything in the Bottom-Up section, click the label for **Main** section.</span></span>  <span data-ttu-id="d5e48-413">В разделе " **снизу вверх** " отображаются только сведения о каких-либо действиях или группах действий, которые вы уже выбрали.</span><span class="sxs-lookup"><span data-stu-id="d5e48-413">The **Bottom-Up** section only shows information for whatever activity, or group of activity, you have currently selected.</span></span>  <span data-ttu-id="d5e48-414">Например, если вы `mineBitcoin` **настроили** одно из действий, в разделе снизу вверх будет отображаться только информация для этого действия.</span><span class="sxs-lookup"><span data-stu-id="d5e48-414">For example, if you clicked on one of the `mineBitcoin` activities, the **Bottom-Up** section is only going to show information for that one activity.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-summary-minebitcoin.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-summary-minebitcoin.msft.png":::
       <span data-ttu-id="d5e48-416">Вкладка " **снизу вверх** "</span><span class="sxs-lookup"><span data-stu-id="d5e48-416">The **Bottom-Up** tab</span></span>  
    :::image-end:::  
    
<span data-ttu-id="d5e48-417">В столбце " **собственное время** " показано, сколько времени было затрачено непосредственно на каждое действие.</span><span class="sxs-lookup"><span data-stu-id="d5e48-417">The **Self Time** column shows you how much time was spent directly in each activity.</span></span>  <span data-ttu-id="d5e48-418">Например, на приведенном ниже рисунке около 63% времени основного потока было затрачено на выполнение `mineBitcoin` функции.</span><span class="sxs-lookup"><span data-stu-id="d5e48-418">For example, in the following figure, about 63% of main thread time was spent on the `mineBitcoin` function.</span></span>  

<span data-ttu-id="d5e48-419">Время от времени до того, чтобы узнать, используется ли производственный режим и уменьшается активность JavaScript, может ускорить загрузку страницы.</span><span class="sxs-lookup"><span data-stu-id="d5e48-419">Time to see whether using production mode and reducing JavaScript activity may speed up the page load.</span></span>  <span data-ttu-id="d5e48-420">Начните работу в режиме "в производство":</span><span class="sxs-lookup"><span data-stu-id="d5e48-420">Start with production mode:</span></span>  

1.  <span data-ttu-id="d5e48-421">На вкладке Редактор откройте `webpack.config.js` .</span><span class="sxs-lookup"><span data-stu-id="d5e48-421">In the editor tab, open `webpack.config.js`.</span></span>  
1.  <span data-ttu-id="d5e48-422">Заменить `"mode":"development"` на `"mode":"production"` .</span><span class="sxs-lookup"><span data-stu-id="d5e48-422">Change `"mode":"development"` to `"mode":"production"`.</span></span>  
1.  <span data-ttu-id="d5e48-423">Дождитесь завершения развертывания новой сборки.</span><span class="sxs-lookup"><span data-stu-id="d5e48-423">Wait for the new build to deploy.</span></span>  
1.  <span data-ttu-id="d5e48-424">Вновь проведите аудит страницы.</span><span class="sxs-lookup"><span data-stu-id="d5e48-424">Audit the page again.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-3-audits-performance.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-remix-updated-3-audits-performance.msft.png":::
       <span data-ttu-id="d5e48-426">Отчет по аудиту после настройки пакета для использования режима "в производство"</span><span class="sxs-lookup"><span data-stu-id="d5e48-426">An Audits report after configuring webpack to use production mode</span></span>  
    :::image-end:::  
    
<span data-ttu-id="d5e48-427">Сокращение действий JavaScript путем удаления запроса на `mineBitcoin` :</span><span class="sxs-lookup"><span data-stu-id="d5e48-427">Reduce JavaScript activity by removing the request to `mineBitcoin`:</span></span>  

1.  <span data-ttu-id="d5e48-428">На вкладке Редактор откройте `src/App.jsx` .</span><span class="sxs-lookup"><span data-stu-id="d5e48-428">In the editor tab, open `src/App.jsx`.</span></span>  
1.  <span data-ttu-id="d5e48-429">Закомментируйте запрос `this.mineBitcoin(1500)` в `constructor` .</span><span class="sxs-lookup"><span data-stu-id="d5e48-429">Comment out the request to `this.mineBitcoin(1500)` in the `constructor`.</span></span>  
1.  <span data-ttu-id="d5e48-430">Дождитесь завершения развертывания новой сборки.</span><span class="sxs-lookup"><span data-stu-id="d5e48-430">Wait for the new build to deploy.</span></span>  
1.  <span data-ttu-id="d5e48-431">Вновь проведите аудит страницы.</span><span class="sxs-lookup"><span data-stu-id="d5e48-431">Audit the page again.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-4-audits-performance.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-remix-updated-4-audits-performance.msft.png":::
       <span data-ttu-id="d5e48-433">Отчет по аудиту после удаления ненужных действий JavaScript</span><span class="sxs-lookup"><span data-stu-id="d5e48-433">An Audits report after removing unnecessary JavaScript work</span></span>  
    :::image-end:::  
    
<span data-ttu-id="d5e48-434">Похоже, что Последнее изменение вызвало значительный переход в производительности!</span><span class="sxs-lookup"><span data-stu-id="d5e48-434">Looks like that last change caused a massive jump in performance!</span></span>  

> [!NOTE]
> <span data-ttu-id="d5e48-435">Этот раздел предоставил краткое введение в панель производительности.</span><span class="sxs-lookup"><span data-stu-id="d5e48-435">This section provided a rather brief introduction to the Performance panel.</span></span>  <span data-ttu-id="d5e48-436">Дополнительные сведения о том, как анализировать производительность страниц, можно найти в статье [Анализ производительности][DevtoolsEvaluatePerformanceReference] .</span><span class="sxs-lookup"><span data-stu-id="d5e48-436">See [Performance Analysis Reference][DevtoolsEvaluatePerformanceReference] to learn more about how to analyze page performance.</span></span>  

<!--todo: add section when available -->  

#### <span data-ttu-id="d5e48-437">Выполнение менее основного потока работ в реальном мире</span><span class="sxs-lookup"><span data-stu-id="d5e48-437">Doing less main thread work in the real world</span></span>  

<span data-ttu-id="d5e48-438">Как правило, панель **производительности** является наиболее распространенным способом для понимания того, какие действия выполняет загружаемый сайт, и Узнайте о способах удаления ненужных действий.</span><span class="sxs-lookup"><span data-stu-id="d5e48-438">In general, the **Performance** panel is the most common way to understand what activity your site does as it loads, and find ways to remove unnecessary activity.</span></span>  

<span data-ttu-id="d5e48-439">Если вы предпочитаете использовать более похожий подход `console.log()` , Пользовательский API для работы с [временными][MDNUserTimingApi] сведениями позволяет вам произвольно помечать определенные этапы жизненного цикла приложения, чтобы отслеживать продолжительность каждого из этих фаз.</span><span class="sxs-lookup"><span data-stu-id="d5e48-439">If you prefer an approach that feels more like `console.log()`, the [User Timing API][MDNUserTimingApi] enables you to arbitrarily mark up certain phases of your app lifecycle, in order to track how long each of those phases takes.</span></span>  

## <span data-ttu-id="d5e48-440">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="d5e48-440">Summary</span></span>  

*   <span data-ttu-id="d5e48-441">Каждый раз, когда вы задаете оптимальное качество нагрузки для сайта, всегда начинайте с аудита.</span><span class="sxs-lookup"><span data-stu-id="d5e48-441">Whenever you set out to optimize the load performance of a site, always start with an audit.</span></span>  <span data-ttu-id="d5e48-442">Аудит определяет базовые показатели и предоставляет советы по улучшению.</span><span class="sxs-lookup"><span data-stu-id="d5e48-442">The audit establishes a baseline, and gives you tips on how to improve.</span></span>  
*   <span data-ttu-id="d5e48-443">За один раз сделайте одно изменение и проведите аудит страницы после каждого изменения, чтобы увидеть, как это изолированное изменение влияет на производительность.</span><span class="sxs-lookup"><span data-stu-id="d5e48-443">Make one change at a time, and audit the page after each change in order to see how that isolated change affects performance.</span></span>  

<!--
## Next steps  

*   Run audits on your own site!  If you need help interpreting your report, or finding ways to improve your load performance, check out [Feedback](#feedback) for ways to get help from the DevTools community.  Stack Overflow, the mailing list, or Twitter are probably best for these types of questions.  
*   Please leave [feedback](#feedback) on this tutorial.  I really do use the data to make better tutorials for you.  
-->  

## <span data-ttu-id="d5e48-444">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="d5e48-444">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageAddPatternIcon]: ../media/add-pattern-icon.msft.png  
[ImageCaptureIcon]: ../media/capture-icon.msft.png  
[ImageLargeResourceRowsButtonIcon]: ../media/large-resource-rows-button-icon.msft.png  
[ImageMorePanelsIcon]: ../media/more-panels-icon.msft.png  
[ImagePerformIcon]: ../media/perform-icon.msft.png  
[ImageRefreshIcon]: ../media/reload-icon.msft.png  
[ImageRemoveIcon]: ../media/remove-icon.msft.png  
<!-- links -->  

[DevtoolsEvaluatePerformanceReference]: ../evaluate-performance/reference.md "Справка по анализу производительности | Документы Microsoft"  

[CourseraIntroductionWebDevelopmentClass]: https://www.coursera.org/learn/web-development#syllabus "Знакомство с классом веб-разработки | Coursera"  

[EssentialImageOptimization]: https://images.guide "Оптимизация изображений"  

[MDNContentEncodingDirectives]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Content-Encoding#Directives "Директивы-кодировка содержимого | MDN"  
[MDNUserTimingApi]: https://developer.mozilla.org/docs/Web/API/User_Timing_API "API времени пользователя | MDN"  

[WebpackTreeShaking]: https://webpack.js.org/guides/tree-shaking "Tree встряхнув | упаковать"  

> [!NOTE]
> <span data-ttu-id="d5e48-451">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="d5e48-451">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="d5e48-452">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/speed/get-started) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="d5e48-452">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/speed/get-started) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="d5e48-454">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="d5e48-454">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
