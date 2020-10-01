---
description: Ссылки на все способы записи и анализа производительности в Microsoft Edge DevTools.
title: Справочные материалы по анализу производительности
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 0e81cb89f0e690533bdd9c8fdbfce272610be783
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/02/2020
ms.locfileid: "10992906"
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







# <span data-ttu-id="6ea68-104">Справочные материалы по анализу производительности</span><span class="sxs-lookup"><span data-stu-id="6ea68-104">Performance analysis reference</span></span>   



<span data-ttu-id="6ea68-105">На этой странице представлен полный справочник по функциям Microsoft Edge DevTools, относящимися к анализу производительности.</span><span class="sxs-lookup"><span data-stu-id="6ea68-105">This page is a comprehensive reference of Microsoft Edge DevTools features related to analyzing performance.</span></span>  

<span data-ttu-id="6ea68-106">Ознакомьтесь [со статьей анализ производительности среды выполнения][DevtoolsEvaluatePerformanceGettingStarted] для учебного руководства по анализу производительности страницы с помощью [Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span><span class="sxs-lookup"><span data-stu-id="6ea68-106">See [Get Started With Analyzing Runtime Performance][DevtoolsEvaluatePerformanceGettingStarted] for a guided tutorial on how to analyze the performance of a page using [Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span></span>  

## <span data-ttu-id="6ea68-107">Запись производительности</span><span class="sxs-lookup"><span data-stu-id="6ea68-107">Record performance</span></span>   

### <span data-ttu-id="6ea68-108">Запись производительности среды выполнения</span><span class="sxs-lookup"><span data-stu-id="6ea68-108">Record runtime performance</span></span>   

<span data-ttu-id="6ea68-109">Записывайте производительность во время выполнения, когда необходимо проанализировать производительность страницы по мере ее выполнения, а не загрузку.</span><span class="sxs-lookup"><span data-stu-id="6ea68-109">Record runtime performance when you want to analyze the performance of a page as it is running, as opposed to loading.</span></span>  

1.  <span data-ttu-id="6ea68-110">Перейдите на страницу, которую вы хотите проанализировать.</span><span class="sxs-lookup"><span data-stu-id="6ea68-110">Go to the page that you want to analyze.</span></span>  
1.  <span data-ttu-id="6ea68-111">Откройте вкладку **производительность** в DevTools.</span><span class="sxs-lookup"><span data-stu-id="6ea68-111">Click the **Performance** tab in DevTools.</span></span>  
1.  <span data-ttu-id="6ea68-112">Нажмите **запись** \ ( ![ запись ][ImageRecordIcon] \).</span><span class="sxs-lookup"><span data-stu-id="6ea68-112">Click **Record** \(![Record][ImageRecordIcon]\).</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-record-highlight.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-record-highlight.msft.png":::
       **<span data-ttu-id="6ea68-114">Record</span><span class="sxs-lookup"><span data-stu-id="6ea68-114">Record</span></span>**  
    :::image-end:::  
    
1.  <span data-ttu-id="6ea68-115">Взаимодействие со страницей.</span><span class="sxs-lookup"><span data-stu-id="6ea68-115">Interact with the page.</span></span>  <span data-ttu-id="6ea68-116">DevTools записывает все действия страниц, которые выполняются в результате взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="6ea68-116">DevTools records all page activity that occurs as a result of your interactions.</span></span>  
1.  <span data-ttu-id="6ea68-117">Нажмите кнопку **запись** еще раз или кнопку **остановить** , чтобы остановить запись.</span><span class="sxs-lookup"><span data-stu-id="6ea68-117">Click **Record** again or click **Stop** to stop recording.</span></span>  
    
### <span data-ttu-id="6ea68-118">Скорость загрузки записей</span><span class="sxs-lookup"><span data-stu-id="6ea68-118">Record load performance</span></span>   

<span data-ttu-id="6ea68-119">Запишите производительность загрузки, когда необходимо проанализировать производительность страницы при ее загрузке, а не на выполнение.</span><span class="sxs-lookup"><span data-stu-id="6ea68-119">Record load performance when you want to analyze the performance of a page as it is loading, as opposed to running.</span></span>  

1.  <span data-ttu-id="6ea68-120">Перейдите на страницу, которую вы хотите проанализировать.</span><span class="sxs-lookup"><span data-stu-id="6ea68-120">Go to the page that you want to analyze.</span></span>  
1.  <span data-ttu-id="6ea68-121">Откройте панель " **производительность** " DevTools.</span><span class="sxs-lookup"><span data-stu-id="6ea68-121">Open the **Performance** panel of DevTools.</span></span>  
1.  <span data-ttu-id="6ea68-122">Нажмите кнопку **обновить страницу** \ ( ![ обновить страницу ][ImageRefreshPageIcon] \).</span><span class="sxs-lookup"><span data-stu-id="6ea68-122">Click **Refresh page** \(![Refresh Page][ImageRefreshPageIcon]\).</span></span>  <span data-ttu-id="6ea68-123">DevTools записывает метрики производительности во время обновления страницы, а затем автоматически останавливает запись спустя пару секунд после завершения загрузки.</span><span class="sxs-lookup"><span data-stu-id="6ea68-123">DevTools records performance metrics while the page refreshes and then automatically stops the recording a couple seconds after the load finishes.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-refresh-button.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-refresh-button.msft.png":::
       **<span data-ttu-id="6ea68-125">Обновить страницу</span><span class="sxs-lookup"><span data-stu-id="6ea68-125">Refresh page</span></span>**  
    :::image-end:::  
    
<span data-ttu-id="6ea68-126">DevTools автоматически масштабирует часть записи, в которой возникло большинство действий.</span><span class="sxs-lookup"><span data-stu-id="6ea68-126">DevTools automatically zooms in on the portion of the recording where most of the activity occurred.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-refreshed.msft.png":::
   <span data-ttu-id="6ea68-128">Запись загрузки страницы</span><span class="sxs-lookup"><span data-stu-id="6ea68-128">A page-load recording</span></span>  
:::image-end:::  

### <span data-ttu-id="6ea68-129">Снимки экрана при записи</span><span class="sxs-lookup"><span data-stu-id="6ea68-129">Capture screenshots while recording</span></span>   

<span data-ttu-id="6ea68-130">Установите флажок **снимки экрана** , чтобы зафиксировать снимок экрана для каждого кадра во время записи.</span><span class="sxs-lookup"><span data-stu-id="6ea68-130">Enable the **Screenshots** checkbox to capture a screenshot of every frame while recording.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-capture-screenshots-checkbox.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-capture-screenshots-checkbox.msft.png":::
   <span data-ttu-id="6ea68-132">Флажок " **снимки экрана** "</span><span class="sxs-lookup"><span data-stu-id="6ea68-132">The **Screenshots** checkbox</span></span>  
:::image-end:::  

<span data-ttu-id="6ea68-133">Сведения о том, как работать с снимками экрана, можно найти в разделе [Просмотр снимка экрана](#view-a-screenshot) .</span><span class="sxs-lookup"><span data-stu-id="6ea68-133">See [View a screenshot](#view-a-screenshot) to learn how to interact with screenshots.</span></span>  

### <span data-ttu-id="6ea68-134">Принудительная сборка мусора во время записи</span><span class="sxs-lookup"><span data-stu-id="6ea68-134">Force garbage collection while recording</span></span>   

<span data-ttu-id="6ea68-135">Во время записи страницы нажмите **собрать мусор** \ ( ![ сбор мусора ][ImageCollectGarbageIcon] ) для принудительного сбора мусора.</span><span class="sxs-lookup"><span data-stu-id="6ea68-135">While you are recording a page, click **Collect garbage** \(![Collect garbage][ImageCollectGarbageIcon]\) to force garbage collection.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-collect-garbage-button.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-collect-garbage-button.msft.png":::
   <span data-ttu-id="6ea68-137">Сбор мусора</span><span class="sxs-lookup"><span data-stu-id="6ea68-137">Collect garbage</span></span>  
:::image-end:::  

### <span data-ttu-id="6ea68-138">Показать параметры записи</span><span class="sxs-lookup"><span data-stu-id="6ea68-138">Show recording settings</span></span>   

<span data-ttu-id="6ea68-139">Нажмите кнопку **захвата параметров** \ ( ![ Параметры захвата ][ImageCaptureSettingsIcon] ), чтобы предоставить доступ к дополнительным параметрам, связанным с тем, как DevTools захватывает записи производительности.</span><span class="sxs-lookup"><span data-stu-id="6ea68-139">Click **Capture settings** \(![Capture settings][ImageCaptureSettingsIcon]\) to expose more settings related to how DevTools captures performance recordings.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-capture-settings-button-open-drawer.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-capture-settings-button-open-drawer.msft.png":::
   <span data-ttu-id="6ea68-141">Раздел " **Параметры захвата** "</span><span class="sxs-lookup"><span data-stu-id="6ea68-141">The **Capture Settings** section</span></span>  
:::image-end:::  

### <span data-ttu-id="6ea68-142">Отключение примеров JavaScript</span><span class="sxs-lookup"><span data-stu-id="6ea68-142">Disable JavaScript samples</span></span>   

<span data-ttu-id="6ea68-143">По умолчанию **основной** раздел записи содержит подробные стеки вызовов функций JavaScript, которые были вызваны во время записи.</span><span class="sxs-lookup"><span data-stu-id="6ea68-143">By default, the **Main** section of a recording displays detailed call stacks of JavaScript functions that were called during the recording.</span></span>  <span data-ttu-id="6ea68-144">Чтобы отключить эти стеки звонков, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="6ea68-144">To disable these call stacks:</span></span>  

1.  <span data-ttu-id="6ea68-145">Открытие меню " **Параметры захвата** ".</span><span class="sxs-lookup"><span data-stu-id="6ea68-145">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="6ea68-146">В разделе [Показать параметры записи](#show-recording-settings).</span><span class="sxs-lookup"><span data-stu-id="6ea68-146">See [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="6ea68-147">Установите флажок **Отключить образцы JavaScript** .</span><span class="sxs-lookup"><span data-stu-id="6ea68-147">Enable the **Disable JavaScript Samples** checkbox.</span></span>  
1.  <span data-ttu-id="6ea68-148">Запишите страницу.</span><span class="sxs-lookup"><span data-stu-id="6ea68-148">Take a recording of the page.</span></span>  
    
<span data-ttu-id="6ea68-149">На следующих двух рисунках показана разница между отключением и включением образцов JavaScript.</span><span class="sxs-lookup"><span data-stu-id="6ea68-149">The following 2 figures display the difference between disabling and enabling JavaScript samples.</span></span>  <span data-ttu-id="6ea68-150">**Основной** раздел записи становится более коротким, так как выборка отключена, так как при этом не будут выпускаться все стеки вызовов JavaScript.</span><span class="sxs-lookup"><span data-stu-id="6ea68-150">The **Main** section of the recording is much shorter when sampling is disabled, because it omits all of the JavaScript call stacks.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-on.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-on.msft.png":::
         <span data-ttu-id="6ea68-152">Пример записи при отключенных примерах JS</span><span class="sxs-lookup"><span data-stu-id="6ea68-152">An example of a recording when JS samples are disabled</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off.msft.png":::
         <span data-ttu-id="6ea68-154">Пример записи при включенных примерах JS</span><span class="sxs-lookup"><span data-stu-id="6ea68-154">An example of a recording when JS samples are enabled</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

### <span data-ttu-id="6ea68-155">Регулирование сети во время записи</span><span class="sxs-lookup"><span data-stu-id="6ea68-155">Throttle the network while recording</span></span>   

<span data-ttu-id="6ea68-156">Чтобы перерегулировать сеть при записи, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="6ea68-156">To throttle the network while recording:</span></span>  

1.  <span data-ttu-id="6ea68-157">Открытие меню " **Параметры захвата** ".</span><span class="sxs-lookup"><span data-stu-id="6ea68-157">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="6ea68-158">В разделе [Показать параметры записи](#show-recording-settings).</span><span class="sxs-lookup"><span data-stu-id="6ea68-158">See [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="6ea68-159">Настройте **сеть** для нужного уровня регулирования.</span><span class="sxs-lookup"><span data-stu-id="6ea68-159">Set **Network** to the desired level of throttling.</span></span>  
    
### <span data-ttu-id="6ea68-160">Регулирование ЦП во время записи</span><span class="sxs-lookup"><span data-stu-id="6ea68-160">Throttle the CPU while recording</span></span>   

<span data-ttu-id="6ea68-161">Чтобы перерегулировать ЦП во время записи, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="6ea68-161">To throttle the CPU while recording:</span></span>  

1.  <span data-ttu-id="6ea68-162">Открытие меню " **Параметры захвата** ".</span><span class="sxs-lookup"><span data-stu-id="6ea68-162">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="6ea68-163">В разделе [Показать параметры записи](#show-recording-settings).</span><span class="sxs-lookup"><span data-stu-id="6ea68-163">See [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="6ea68-164">Установите для **ЦП** требуемый уровень регулирования.</span><span class="sxs-lookup"><span data-stu-id="6ea68-164">Set **CPU** to the desired level of throttling.</span></span>  
    
<span data-ttu-id="6ea68-165">Регулирование производится относительно возможностей компьютера.</span><span class="sxs-lookup"><span data-stu-id="6ea68-165">Throttling is relative to the capabilities of your computer.</span></span>  <span data-ttu-id="6ea68-166">Например, параметр "интервал по **промедлению** " обеспечивает работу ЦП 2 раза ниже обычного.</span><span class="sxs-lookup"><span data-stu-id="6ea68-166">For example, the **2x slowdown** option makes your CPU operate 2 times slower than normal.</span></span>  <span data-ttu-id="6ea68-167">DevTools не имитируют процессоры мобильных устройств, так как архитектура мобильных устройств значительно отличается от настольных компьютеров и ноутбуков.</span><span class="sxs-lookup"><span data-stu-id="6ea68-167">DevTools do not truly simulate the CPUs of mobile devices, because the architecture of mobile devices is very different from that of desktops and laptops.</span></span>  

### <span data-ttu-id="6ea68-168">Включение расширенного инструментария рисования</span><span class="sxs-lookup"><span data-stu-id="6ea68-168">Enable advanced paint instrumentation</span></span>   

<span data-ttu-id="6ea68-169">Чтобы просмотреть подробные инструменты для рисования, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="6ea68-169">To view detailed paint instrumentation:</span></span>  

1.  <span data-ttu-id="6ea68-170">Открытие меню " **Параметры захвата** ".</span><span class="sxs-lookup"><span data-stu-id="6ea68-170">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="6ea68-171">В разделе [Показать параметры записи](#show-recording-settings).</span><span class="sxs-lookup"><span data-stu-id="6ea68-171">See [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="6ea68-172">Установите флажок **включить дополнительные возможности инструментирования краски (медленно)** .</span><span class="sxs-lookup"><span data-stu-id="6ea68-172">Check the **Enable advanced paint instrumentation (slow)** checkbox.</span></span>  

<span data-ttu-id="6ea68-173">Сведения о том, как взаимодействовать с данными краски, можно найти в статье [Просмотр слоев](#view-layers-information) и [профилировщика Paint](#view-paint-profiler).</span><span class="sxs-lookup"><span data-stu-id="6ea68-173">To learn how to interact with the paint information, see [View layers](#view-layers-information) and [View paint profiler](#view-paint-profiler).</span></span>  

## <span data-ttu-id="6ea68-174">Сохранение записи</span><span class="sxs-lookup"><span data-stu-id="6ea68-174">Save a recording</span></span>   

<span data-ttu-id="6ea68-175">Чтобы сохранить запись, щелкните ее правой кнопкой мыши и выберите команду **Сохранить профиль**.</span><span class="sxs-lookup"><span data-stu-id="6ea68-175">To save a recording, right-click and select **Save Profile**.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-save-profile.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-save-profile.msft.png":::
   **<span data-ttu-id="6ea68-177">Сохранить профиль</span><span class="sxs-lookup"><span data-stu-id="6ea68-177">Save Profile</span></span>**  
:::image-end:::  

## <span data-ttu-id="6ea68-178">Загрузка записи</span><span class="sxs-lookup"><span data-stu-id="6ea68-178">Load a recording</span></span>   

<span data-ttu-id="6ea68-179">Чтобы загрузить запись, щелкните ее правой кнопкой мыши и выберите команду " **загрузить профиль**".</span><span class="sxs-lookup"><span data-stu-id="6ea68-179">To load a recording, right-click and select **Load Profile**.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-load-profile.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-load-profile.msft.png":::
   **<span data-ttu-id="6ea68-181">Загрузить профиль</span><span class="sxs-lookup"><span data-stu-id="6ea68-181">Load Profile</span></span>**  
:::image-end:::  

## <span data-ttu-id="6ea68-182">Удаление предыдущей записи</span><span class="sxs-lookup"><span data-stu-id="6ea68-182">Clear the previous recording</span></span>   

<span data-ttu-id="6ea68-183">После внесения записи нажмите **Очистить запись** и ( ![ Очистить запись ][ImageClearRecordingIcon] ), чтобы очистить эту запись на панели **производительности** .</span><span class="sxs-lookup"><span data-stu-id="6ea68-183">After making a recording, press **Clear recording** \(![Clear recording][ImageClearRecordingIcon]\) to clear that recording from the **Performance** panel.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-clear-button.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-clear-button.msft.png":::
   **<span data-ttu-id="6ea68-185">Очистка записи</span><span class="sxs-lookup"><span data-stu-id="6ea68-185">Clear recording</span></span>**  
:::image-end:::  

## <span data-ttu-id="6ea68-186">Анализ записи производительности</span><span class="sxs-lookup"><span data-stu-id="6ea68-186">Analyze a performance recording</span></span>   

<span data-ttu-id="6ea68-187">После того как вы [зарегистрируете производительность во время выполнения](#record-runtime-performance) или [скорость загрузки записи](#record-load-performance), на панели **производительности** можно получить большое количество данных для анализа производительности.</span><span class="sxs-lookup"><span data-stu-id="6ea68-187">After you [record runtime performance](#record-runtime-performance) or [record load performance](#record-load-performance), the **Performance** panel provides a lot of data for analyzing the performance of what just happened.</span></span>  

### <span data-ttu-id="6ea68-188">Выбор части записи</span><span class="sxs-lookup"><span data-stu-id="6ea68-188">Select a portion of a recording</span></span>   

<span data-ttu-id="6ea68-189">Чтобы выделить часть записи, перетащите указатель мыши по левому или правому краю **обзора** .</span><span class="sxs-lookup"><span data-stu-id="6ea68-189">Drag your mouse left or right across the **Overview** to select a portion of a recording.</span></span>  <span data-ttu-id="6ea68-190">**Обзор** — это раздел, содержащий диаграммы в **кадрах**, **ЦП**и **сети** .</span><span class="sxs-lookup"><span data-stu-id="6ea68-190">The **Overview** is the section that contains the **FPS**, **CPU**, and **NET** charts.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-zoom-highlighted.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-zoom-highlighted.msft.png":::
   <span data-ttu-id="6ea68-192">Перетащите указатель мыши по **обзору** , чтобы увеличить масштаб</span><span class="sxs-lookup"><span data-stu-id="6ea68-192">Drag the mouse across the **Overview** to zoom</span></span>  
:::image-end:::  

<span data-ttu-id="6ea68-193">Чтобы выбрать часть с помощью клавиатуры, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="6ea68-193">To select a portion using the keyboard:</span></span>  

1.  <span data-ttu-id="6ea68-194">Щелкните фон **основного** раздела или любой раздел рядом с ним, например **взаимодействия**, **сеть**или **графический процессор**.</span><span class="sxs-lookup"><span data-stu-id="6ea68-194">Click on the background of the **Main** section, or any of the sections next to it, such as **Interactions**, **Network**, or **GPU**.</span></span>  <span data-ttu-id="6ea68-195">Этот рабочий процесс клавиатуры работает только в том случае, если в фокусе находится один из этих разделов.</span><span class="sxs-lookup"><span data-stu-id="6ea68-195">This keyboard workflow only works when one of these sections is in focus.</span></span>  
1.  <span data-ttu-id="6ea68-196">С помощью `W` клавиш,, `A` `S` ,, `D` клавиши для увеличения, перемещения влево, уменьшения и перемещения вправо соответственно.</span><span class="sxs-lookup"><span data-stu-id="6ea68-196">Use the `W`, `A`, `S`, `D` keys to zoom in, move left, zoom out, and move right, respectively.</span></span>  

<span data-ttu-id="6ea68-197">Чтобы выбрать часть с помощью сенсорной панели, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="6ea68-197">To select a portion using a trackpad:</span></span>  

1.  <span data-ttu-id="6ea68-198">Наведите указатель мыши на раздел **Общие сведения** или на раздел **сведения** .</span><span class="sxs-lookup"><span data-stu-id="6ea68-198">Hover your mouse over the **Overview** section or the **Details** section.</span></span>  <span data-ttu-id="6ea68-199">Раздел **Обзор** — это область, содержащая диаграммы в **кадрах**, **ЦП**и **сети** .</span><span class="sxs-lookup"><span data-stu-id="6ea68-199">The **Overview** section is the area containing the **FPS**, **CPU**, and **NET** charts.</span></span>  <span data-ttu-id="6ea68-200">Раздел " **сведения** " — это область, содержащая **основной** раздел, раздел " **взаимодействия** " и т. д.</span><span class="sxs-lookup"><span data-stu-id="6ea68-200">The **Details** section is the area containing the **Main** section, the **Interactions** section, and so on.</span></span>  
1.  <span data-ttu-id="6ea68-201">С помощью двух пальцев проведите пальцем вверх, проведите пальцем влево, чтобы переместить влево, проведите пальцем вниз, чтобы увеличить масштаб, и проведите пальцем вправо, чтобы перейти вправо.</span><span class="sxs-lookup"><span data-stu-id="6ea68-201">Using two fingers, swipe up to zoom out, swipe left to move left, swipe down to zoom in, and swipe right to move right.</span></span>  

<span data-ttu-id="6ea68-202">Для прокрутки длинной Flame диаграммы в **главном** разделе или любом из соседей щелкните и удерживайте клавишу во время перетаскивания вверх и вниз.</span><span class="sxs-lookup"><span data-stu-id="6ea68-202">To scroll a long flame chart in the **Main** section or any of the neighbors, click and hold while dragging up and down.</span></span>  <span data-ttu-id="6ea68-203">Чтобы переместить выделенную часть записи, перетащите левую и правую клавишу.</span><span class="sxs-lookup"><span data-stu-id="6ea68-203">Drag left and right to move what portion of the recording is selected.</span></span>  

### <span data-ttu-id="6ea68-204">Поиск действий</span><span class="sxs-lookup"><span data-stu-id="6ea68-204">Search activities</span></span>   

<span data-ttu-id="6ea68-205">Нажмите клавиши `Control` + `F` \ (Windows \) или `Command` + `F` \ (macOS \), чтобы открыть поле поиска в нижней части панели " **производительность** ".</span><span class="sxs-lookup"><span data-stu-id="6ea68-205">Press `Control`+`F` \(Windows\) or `Command`+`F` \(macOS\) to open the search box at the bottom of the **Performance** panel.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-search-regex.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-search-regex.msft.png":::
   <span data-ttu-id="6ea68-207">Поле поиска</span><span class="sxs-lookup"><span data-stu-id="6ea68-207">The search box</span></span>  
:::image-end:::  

<span data-ttu-id="6ea68-208">Чтобы перейти к действиям, которые соответствуют запросу, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="6ea68-208">To navigate activities that match your query:</span></span>  

*   <span data-ttu-id="6ea68-209">Используйте кнопки **назад** ( ![ предыдущее ][ImagePreviousIcon] ) и **Далее** \ ( ![ Далее ][ImageNextIcon] \).</span><span class="sxs-lookup"><span data-stu-id="6ea68-209">Use the **Previous** \(![Previous][ImagePreviousIcon]\) and **Next** \(![Next][ImageNextIcon]\) buttons.</span></span>  
*   <span data-ttu-id="6ea68-210">Нажмите кнопку, `Shift` + `Enter` чтобы выбрать предыдущую или `Enter` следующую команду.</span><span class="sxs-lookup"><span data-stu-id="6ea68-210">Press `Shift`+`Enter` to select the previous or `Enter` to select the next.</span></span>  

<span data-ttu-id="6ea68-211">Чтобы изменить параметры запроса, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="6ea68-211">To modify query settings:</span></span>  

*   <span data-ttu-id="6ea68-212">Нажмите клавишу **с учетом регистра** \ (с ![ учетом регистра ][ImageSearchCaseIcon] ), чтобы сделать запрос чувствительным к регистру.</span><span class="sxs-lookup"><span data-stu-id="6ea68-212">Press **Case sensitive** \(![Case sensitive][ImageSearchCaseIcon]\) to make the query case sensitive.</span></span>  
*   <span data-ttu-id="6ea68-213">Нажмите **регулярные** выражения \ ( ![ Regex ][ImageSearchRegexIcon] \), чтобы использовать регулярное выражение в запросе.</span><span class="sxs-lookup"><span data-stu-id="6ea68-213">Press **Regex** \(![Regex][ImageSearchRegexIcon]\) to use a regular expression in your query.</span></span>  

<span data-ttu-id="6ea68-214">Чтобы скрыть поле поиска, нажмите кнопку **Отмена**.</span><span class="sxs-lookup"><span data-stu-id="6ea68-214">To hide the search box, press **Cancel**.</span></span>  

### <span data-ttu-id="6ea68-215">Просмотр основного действия потока</span><span class="sxs-lookup"><span data-stu-id="6ea68-215">View main thread activity</span></span>   

<span data-ttu-id="6ea68-216">Используйте **главный** раздел для просмотра действий, которые произошли в основном потоке страницы.</span><span class="sxs-lookup"><span data-stu-id="6ea68-216">Use the **Main** section to view activity that occurred on the main thread of the page.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-main-zoomed.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-main-zoomed.msft.png":::
   <span data-ttu-id="6ea68-218">**Основной** раздел</span><span class="sxs-lookup"><span data-stu-id="6ea68-218">The **Main** section</span></span>  
:::image-end:::  

<span data-ttu-id="6ea68-219">Щелкните событие, чтобы просмотреть дополнительные сведения о нем на вкладке **Сводка** .  DevTools выделеет выбранное событие.</span><span class="sxs-lookup"><span data-stu-id="6ea68-219">Click on an event to view more information about it in the **Summary** tab.  DevTools outlines the selected event.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-summary-me.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-summary-me.msft.png":::
   <span data-ttu-id="6ea68-221">Дополнительные сведения о `anonymous` функции на вкладке " **Сводка** "</span><span class="sxs-lookup"><span data-stu-id="6ea68-221">More information about the `anonymous` function in the **Summary** tab</span></span>  
:::image-end:::  

<span data-ttu-id="6ea68-222">DevTools представляет главную активность потока с Flame диаграммой.</span><span class="sxs-lookup"><span data-stu-id="6ea68-222">DevTools represents main thread activity with a flame chart.</span></span>  <span data-ttu-id="6ea68-223">Ось x обозначает запись с течением времени.</span><span class="sxs-lookup"><span data-stu-id="6ea68-223">The x-axis represents the recording over time.</span></span>  <span data-ttu-id="6ea68-224">Ось y представляет стек вызова.</span><span class="sxs-lookup"><span data-stu-id="6ea68-224">The y-axis represents the call stack.</span></span>  <span data-ttu-id="6ea68-225">Событие Top приводит к возникновению событий, указанных ниже.</span><span class="sxs-lookup"><span data-stu-id="6ea68-225">The events on top cause the events below it.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-main-flame-chart.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-main-flame-chart.msft.png":::
   <span data-ttu-id="6ea68-227">Flame диаграмма</span><span class="sxs-lookup"><span data-stu-id="6ea68-227">A flame chart</span></span>  
:::image-end:::  

<span data-ttu-id="6ea68-228">На предыдущем рисунке `click` событие вызвало `Function Call` в `activitytabs.js` строке 53.</span><span class="sxs-lookup"><span data-stu-id="6ea68-228">In the previous figure, a `click` event caused a `Function Call` in `activitytabs.js` on line 53.</span></span>  <span data-ttu-id="6ea68-229">Ниже `Function Call` показано, что была вызвана анонимная функция.</span><span class="sxs-lookup"><span data-stu-id="6ea68-229">Below `Function Call` you see that an anonymous function was called.</span></span>  <span data-ttu-id="6ea68-230">Анонимная функция, вызываемая, которая вызывается `a` `wait` `Minor GC` .</span><span class="sxs-lookup"><span data-stu-id="6ea68-230">The anonymous function called `a`, which called `wait`, which called `Minor GC`.</span></span>  

<span data-ttu-id="6ea68-231">DevTools назначает сценарии случайные цвета.</span><span class="sxs-lookup"><span data-stu-id="6ea68-231">DevTools assigns scripts random colors.</span></span>  <span data-ttu-id="6ea68-232">На предыдущем рисунке вызовы функций из одного сценария окрашены в зеленый цвет.</span><span class="sxs-lookup"><span data-stu-id="6ea68-232">In the previous figure, function calls from one script are colored light green.</span></span>  <span data-ttu-id="6ea68-233">Вызов из другого сценария имеет цветный бежевый.</span><span class="sxs-lookup"><span data-stu-id="6ea68-233">Calls from another script are colored beige.</span></span>  <span data-ttu-id="6ea68-234">Темным желтым обозначенными действиями в сценариях, а фиолетовые — действия отрисовки.</span><span class="sxs-lookup"><span data-stu-id="6ea68-234">The darker yellow represents scripting activity, and the purple event represents rendering activity.</span></span>  <span data-ttu-id="6ea68-235">Эти темные желтые и фиолетовые события будут согласованы во всех записях.</span><span class="sxs-lookup"><span data-stu-id="6ea68-235">These darker yellow and purple events are consistent across all recordings.</span></span>  

<span data-ttu-id="6ea68-236">Если вы хотите скрыть подробную flameную диаграмму вызовов JavaScript, просмотрите раздел [Отключение примеров JavaScript](#disable-javascript-samples) .</span><span class="sxs-lookup"><span data-stu-id="6ea68-236">See [Disable JavaScript samples](#disable-javascript-samples) if you want to hide the detailed flame chart of JavaScript calls.</span></span>  <span data-ttu-id="6ea68-237">При отключенных примерах JS отображаются только события высокого уровня, такие как `Event: click` и на `Function Call` предыдущем рисунке.</span><span class="sxs-lookup"><span data-stu-id="6ea68-237">When JS samples are disabled, you only see high-level events such as `Event: click` and `Function Call` from the previous figure.</span></span>  

### <span data-ttu-id="6ea68-238">Просмотр действий в таблице</span><span class="sxs-lookup"><span data-stu-id="6ea68-238">View activities in a table</span></span>   

<span data-ttu-id="6ea68-239">После записи страницы, чтобы проанализировать действия, не нужно полагаться только на **основной** раздел.</span><span class="sxs-lookup"><span data-stu-id="6ea68-239">After recording a page, you do not need to rely solely on the **Main** section to analyze activities.</span></span>  <span data-ttu-id="6ea68-240">DevTools также предоставляет три табличных представления для анализа действий.</span><span class="sxs-lookup"><span data-stu-id="6ea68-240">DevTools also provides three tabular views for analyzing activities.</span></span>  <span data-ttu-id="6ea68-241">Каждое представление предлагает различные варианты действий:</span><span class="sxs-lookup"><span data-stu-id="6ea68-241">Each view gives you a different perspective on the activities:</span></span>  

*   <span data-ttu-id="6ea68-242">Если вы хотите просмотреть корневые действия, которые приводят к большинству работ, используйте [вкладку "дерево вызовов"](#the-call-tree-tab).</span><span class="sxs-lookup"><span data-stu-id="6ea68-242">When you want to view the root activities that cause the most work, use [the Call Tree tab](#the-call-tree-tab).</span></span>  
*   <span data-ttu-id="6ea68-243">Если вы хотите просмотреть действия, в которых больше всего потратили время, используйте [вкладку снизу вверх](#the-bottom-up-tab).</span><span class="sxs-lookup"><span data-stu-id="6ea68-243">When you want to view the activities where the most time was directly spent, use [the Bottom-Up tab](#the-bottom-up-tab).</span></span>  
*   <span data-ttu-id="6ea68-244">Если вы хотите просмотреть действия в том порядке, в котором они были обнаружены во время записи, используйте [вкладку Журнал событий](#the-event-log-tab).</span><span class="sxs-lookup"><span data-stu-id="6ea68-244">When you want to view the activities in the order in which they occurred during the recording, use [the Event Log tab](#the-event-log-tab).</span></span>  
    
> [!NOTE]
> <span data-ttu-id="6ea68-245">Следующие три раздела относятся к одной и той же демонстрации.</span><span class="sxs-lookup"><span data-stu-id="6ea68-245">The next three sections all refer to the same demo.</span></span>  <span data-ttu-id="6ea68-246">Запустите демонстрацию самостоятельно на [вкладке "действия" демонстрации][ActivityTabsDemo].</span><span class="sxs-lookup"><span data-stu-id="6ea68-246">Run the demo yourself at [Activity Tabs Demo][ActivityTabsDemo].</span></span>  

#### <span data-ttu-id="6ea68-247">Корневые действия</span><span class="sxs-lookup"><span data-stu-id="6ea68-247">Root activities</span></span>   

<span data-ttu-id="6ea68-248">Ниже приведено описание концепции **корневых действий** , упомянутой на вкладке " **дерево вызовов** ", вкладке " **снизу вверх** " и в разделе " **журнал событий** ".</span><span class="sxs-lookup"><span data-stu-id="6ea68-248">Here is an explanation of the **root activities** concept that is mentioned in the **Call Tree** tab, **Bottom-Up** tab, and **Event Log** sections.</span></span>  

<span data-ttu-id="6ea68-249">Корневые действия — это те, которые приводят к тому, что браузер выполняет определенную работу.</span><span class="sxs-lookup"><span data-stu-id="6ea68-249">Root activities are those which cause the browser to do some work.</span></span>  <span data-ttu-id="6ea68-250">Например, при щелчке страницы браузер запускает `Event` действие в качестве корневого действия.</span><span class="sxs-lookup"><span data-stu-id="6ea68-250">For example, when you click a page, the browser fires an `Event` activity as the root activity.</span></span>  <span data-ttu-id="6ea68-251">Это `Event` может привести к запуску обработчика и т. д.</span><span class="sxs-lookup"><span data-stu-id="6ea68-251">That `Event` might cause a handler to run, and so on.</span></span>  

<span data-ttu-id="6ea68-252">В диаграмме Flame **основного** раздела корневые действия находятся в верхней части диаграммы.</span><span class="sxs-lookup"><span data-stu-id="6ea68-252">In the flame chart of the **Main** section, root activities are at the top of the chart.</span></span>  <span data-ttu-id="6ea68-253">В **дереве вызовов** и на вкладках **журнал событий** корневые действия — это элементы верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="6ea68-253">In the **Call Tree** and **Event Log** tabs, root activities are the top-level items.</span></span>  

<span data-ttu-id="6ea68-254">Пример корневых действий вы видите [на вкладке "дерево вызовов"](#the-call-tree-tab) .</span><span class="sxs-lookup"><span data-stu-id="6ea68-254">See [The Call Tree tab](#the-call-tree-tab) for an example of root activities.</span></span>  

#### <span data-ttu-id="6ea68-255">Вкладка "дерево вызовов"</span><span class="sxs-lookup"><span data-stu-id="6ea68-255">The Call Tree tab</span></span>   

<span data-ttu-id="6ea68-256">С помощью вкладки " **дерево вызовов** " можно просмотреть, какие [корневые действия](#root-activities) приводят к наибольшему работоспособности.</span><span class="sxs-lookup"><span data-stu-id="6ea68-256">Use the **Call Tree** tab to view which [root activities](#root-activities) cause the most work.</span></span>  

<span data-ttu-id="6ea68-257">На вкладке " **дерево вызовов** " отображаются только действия в выбранной части записи.</span><span class="sxs-lookup"><span data-stu-id="6ea68-257">The **Call Tree** tab only displays activities during the selected portion of the recording.</span></span>  <span data-ttu-id="6ea68-258">Ознакомьтесь с разделом [Выбор части записи](#select-a-portion-of-a-recording) , чтобы узнать, как выделять части.</span><span class="sxs-lookup"><span data-stu-id="6ea68-258">See [Select a portion of a recording](#select-a-portion-of-a-recording) to learn how to select portions.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-call-tree.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-call-tree.msft.png":::
   <span data-ttu-id="6ea68-260">Вкладка " **дерево вызовов** "</span><span class="sxs-lookup"><span data-stu-id="6ea68-260">The **Call Tree** tab</span></span>  
:::image-end:::  

<span data-ttu-id="6ea68-261">На приведенном выше рисунке сверху находятся элементы в столбце " **действия** ", `Evaluate Script` а также `Parse HTML` корневые действия.</span><span class="sxs-lookup"><span data-stu-id="6ea68-261">In the previous figure, the top-level of items in the **Activity** column, such as `Evaluate Script` and `Parse HTML` are root activities.</span></span>  <span data-ttu-id="6ea68-262">Вложенный объект представляет стек вызова.</span><span class="sxs-lookup"><span data-stu-id="6ea68-262">The nesting represents the call stack.</span></span>  <span data-ttu-id="6ea68-263">Например, на предыдущем рисунке, `Parse HTML` вызвавшем `Evaluate Script` причины `Compile Script` и `(anonymous)` .</span><span class="sxs-lookup"><span data-stu-id="6ea68-263">For example, in the previous figure, `Parse HTML` which caused `Evaluate Script` which caused `Compile Script` and `(anonymous)`.</span></span>  

<span data-ttu-id="6ea68-264">**Собственное время** — это время, которое прямо затрачено на это действие.</span><span class="sxs-lookup"><span data-stu-id="6ea68-264">**Self Time** represents the time directly spent in that activity.</span></span>  <span data-ttu-id="6ea68-265">**Общее время** представляет время, затраченное на выполнение этого мероприятия или любого из дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="6ea68-265">**Total Time** represents the time spent in that activity or any of the children.</span></span>  

<span data-ttu-id="6ea68-266">Щелкните **собственное время**, **Общее время**или **активность** , чтобы отсортировать таблицу по этому столбцу.</span><span class="sxs-lookup"><span data-stu-id="6ea68-266">Click **Self Time**, **Total Time**, or **Activity** to sort the table by that column.</span></span>  

<span data-ttu-id="6ea68-267">Используйте текстовое поле " **Фильтр** " для фильтрации событий по имени действия.</span><span class="sxs-lookup"><span data-stu-id="6ea68-267">Use the **Filter** text box to filter events by activity name.</span></span>  

<span data-ttu-id="6ea68-268">По умолчанию для меню **Группировка** выбрано значение **Нет группировки**.</span><span class="sxs-lookup"><span data-stu-id="6ea68-268">By default the **Grouping** menu is set to **No Grouping**.</span></span>  <span data-ttu-id="6ea68-269">Используйте меню **Группировка** для сортировки таблицы действий на основе различных условий.</span><span class="sxs-lookup"><span data-stu-id="6ea68-269">Use the **Grouping** menu to sort the activity table based on various criteria.</span></span>  

<span data-ttu-id="6ea68-270">Нажмите кнопку **Показать стоп** -таблицу с максимальным ![ объемом \ (Показать стопку с наиболее тяжелых ][ImageShowHeaviestStackIcon] ), чтобы отобразить другую ячейку справа от таблицы " **действия** ".</span><span class="sxs-lookup"><span data-stu-id="6ea68-270">Click **Show Heaviest Stack** \(![Show Heaviest Stack][ImageShowHeaviestStackIcon]\) to reveal another table to the right of the **Activity** table.</span></span>  <span data-ttu-id="6ea68-271">Щелкните действие, чтобы заполнить таблицу с самым **максимальным** .</span><span class="sxs-lookup"><span data-stu-id="6ea68-271">Click on an activity to populate the **Heaviest Stack** table.</span></span>  <span data-ttu-id="6ea68-272">В таблице наиболее **плотного стека** показано, какие дочерние элементы выбранного действия занимали наибольшее время.</span><span class="sxs-lookup"><span data-stu-id="6ea68-272">The **Heaviest Stack** table shows you which children of the selected activity took the longest time to run.</span></span>  

#### <span data-ttu-id="6ea68-273">Вкладка "снизу вверх"</span><span class="sxs-lookup"><span data-stu-id="6ea68-273">The Bottom-Up tab</span></span>   

<span data-ttu-id="6ea68-274">С помощью вкладки " **снизу вверх** " можно просмотреть, какие действия немедленно потратили на общее время в агрегате.</span><span class="sxs-lookup"><span data-stu-id="6ea68-274">Use the **Bottom-Up** tab to view which activities directly took up the most time in aggregate.</span></span>  

<span data-ttu-id="6ea68-275">На вкладке " **снизу вверх** " отображаются только действия в выбранной части записи.</span><span class="sxs-lookup"><span data-stu-id="6ea68-275">The **Bottom-Up** tab only displays activities during the selected portion of the recording.</span></span>  <span data-ttu-id="6ea68-276">Ознакомьтесь с разделом [Выбор части записи](#select-a-portion-of-a-recording) , чтобы узнать, как выделять части.</span><span class="sxs-lookup"><span data-stu-id="6ea68-276">See [Select a portion of a recording](#select-a-portion-of-a-recording) to learn how to select portions.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-bottoms-up.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-bottoms-up.msft.png":::
   <span data-ttu-id="6ea68-278">Вкладка " **снизу вверх** "</span><span class="sxs-lookup"><span data-stu-id="6ea68-278">The **Bottom-Up** tab</span></span>  
:::image-end:::  

<span data-ttu-id="6ea68-279">В разделе **основной** Flame диаграммы на предыдущем рисунке показано, что почти практически все время затрачено на работу `Parse HTML` .</span><span class="sxs-lookup"><span data-stu-id="6ea68-279">In the **Main** section flame chart of the previous figure, see that almost practically all of the time was spent running `Parse HTML`.</span></span>  <span data-ttu-id="6ea68-280">Верхнее действие на вкладке " **снизу вверх** " на предыдущем рисунке `Parse HTML` .</span><span class="sxs-lookup"><span data-stu-id="6ea68-280">The top activity in the **Bottom-Up** tab of the previous figure is `Parse HTML`.</span></span>  <!--In the flame chart of the previous figure, the yellow below the calls to `wait` are actually thousands of `Minor GC` calls.  -->  <span data-ttu-id="6ea68-281">На вкладке " **снизу вверх** " в списке ниже приведены наиболее ресурсоемкие действия `Layout` .</span><span class="sxs-lookup"><span data-stu-id="6ea68-281">See in the **Bottom-Up** tab, the next most expensive activity is `Layout`.</span></span>  

<span data-ttu-id="6ea68-282">Столбец " **собственное время** " представляет агрегированное время, проведенное непосредственно в этом действии, для всех вхождений.</span><span class="sxs-lookup"><span data-stu-id="6ea68-282">The **Self Time** column represents the aggregated time spent directly in that activity, across all of the occurrences.</span></span>  

<span data-ttu-id="6ea68-283">Столбец " **Общее время** " представляет объединенное время, затраченное на это действие или любые дочерние элементы.</span><span class="sxs-lookup"><span data-stu-id="6ea68-283">The **Total Time** column represents aggregated time spent in that activity or any of the children.</span></span>  

#### <span data-ttu-id="6ea68-284">Вкладка "журнал событий"</span><span class="sxs-lookup"><span data-stu-id="6ea68-284">The Event Log tab</span></span>   

<span data-ttu-id="6ea68-285">Используйте вкладку **журнал событий** , чтобы просмотреть действия в том порядке, в котором они были обнаружены во время записи.</span><span class="sxs-lookup"><span data-stu-id="6ea68-285">Use the **Event Log** tab to view activities in the order in which they occurred during the recording.</span></span>  

<span data-ttu-id="6ea68-286">На вкладке **журнал событий** отображаются только действия в выбранной части записи.</span><span class="sxs-lookup"><span data-stu-id="6ea68-286">The **Event Log** tab only displays activities during the selected portion of the recording.</span></span>  <span data-ttu-id="6ea68-287">Ознакомьтесь с разделом [Выбор части записи](#select-a-portion-of-a-recording) , чтобы узнать, как выделять части.</span><span class="sxs-lookup"><span data-stu-id="6ea68-287">See [Select a portion of a recording](#select-a-portion-of-a-recording) to learn how to select portions.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-event-log.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-event-log.msft.png":::
   <span data-ttu-id="6ea68-289">Вкладка " **журнал событий** "</span><span class="sxs-lookup"><span data-stu-id="6ea68-289">The **Event Log** tab</span></span>  
:::image-end:::  

<span data-ttu-id="6ea68-290">Столбец " **время начала** " представляет точку, в которой началось действие, относительно начала записи.</span><span class="sxs-lookup"><span data-stu-id="6ea68-290">The **Start Time** column represents the point at which that activity started, relative to the start of the recording.</span></span>  <span data-ttu-id="6ea68-291">Например, время начала `175.7 ms` для выделенного элемента на предыдущем рисунке означает, что действие началось 175,7 MS после начала записи.</span><span class="sxs-lookup"><span data-stu-id="6ea68-291">For example, the start time of `175.7 ms` for the selected item in the previous figure means that activity started 175.7 ms after the recording started.</span></span>  

<span data-ttu-id="6ea68-292">Столбец " **собственное время** " представляет время, затраченное непосредственно на это действие.</span><span class="sxs-lookup"><span data-stu-id="6ea68-292">The **Self Time** column represents the time spent directly in that activity.</span></span>  

<span data-ttu-id="6ea68-293">Столбцы « **Общее время** » обозначают время, затраченное непосредственно на это действие или в любой из дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="6ea68-293">The **Total Time** columns represents time spent directly in that activity or in any of the children.</span></span>  

<span data-ttu-id="6ea68-294">Щелкните **время начала**, **собственное время**или **Общее время** для сортировки таблицы по этому столбцу.</span><span class="sxs-lookup"><span data-stu-id="6ea68-294">Click **Start Time**, **Self Time**, or **Total Time** to sort the table by that column.</span></span>

<span data-ttu-id="6ea68-295">Используйте текстовое поле **Фильтр** , чтобы отфильтровать действия по имени.</span><span class="sxs-lookup"><span data-stu-id="6ea68-295">Use the **Filter** text box to filter activities by name.</span></span>  

<span data-ttu-id="6ea68-296">С помощью меню " **Длительность** " можно отфильтровать все действия, которые заняли менее 1 мс или 15 мс.</span><span class="sxs-lookup"><span data-stu-id="6ea68-296">Use the **Duration** menu to filter out any activities that took less than 1 ms or 15 ms.</span></span>  <span data-ttu-id="6ea68-297">По умолчанию для меню **Duration** задано значение **все**, что означает, что отображаются все действия.</span><span class="sxs-lookup"><span data-stu-id="6ea68-297">By default the **Duration** menu is set to **All**, meaning all activities are shown.</span></span>  

<span data-ttu-id="6ea68-298">Отключите флажки " **Загрузка**", " **Создание сценариев**", " **Подготовка**" и " **раскраска** ", чтобы отфильтровать все действия из этих категорий.</span><span class="sxs-lookup"><span data-stu-id="6ea68-298">Disable the **Loading**, **Scripting**, **Rendering**, or **Painting** checkboxes to filter out all activities from those categories.</span></span>  

### <span data-ttu-id="6ea68-299">Просмотр действий GPU</span><span class="sxs-lookup"><span data-stu-id="6ea68-299">View GPU activity</span></span>   

<span data-ttu-id="6ea68-300">Просматривайте активность GPU в разделе **GPU** .</span><span class="sxs-lookup"><span data-stu-id="6ea68-300">View GPU activity in the **GPU** section.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-gpu-zoomed.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-gpu-zoomed.msft.png":::
   <span data-ttu-id="6ea68-302">Раздел **GPU**</span><span class="sxs-lookup"><span data-stu-id="6ea68-302">The **GPU** section</span></span>  
:::image-end:::  

### <span data-ttu-id="6ea68-303">Просмотр растровых операций</span><span class="sxs-lookup"><span data-stu-id="6ea68-303">View raster activity</span></span>   

<span data-ttu-id="6ea68-304">Просматривайте растровые действия в разделе " **растр** ".</span><span class="sxs-lookup"><span data-stu-id="6ea68-304">View raster activity in the **Raster** section.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-raster.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-raster.msft.png":::
   <span data-ttu-id="6ea68-306">**Разточечный** раздел</span><span class="sxs-lookup"><span data-stu-id="6ea68-306">The **Raster** section</span></span>  
:::image-end:::  

### <span data-ttu-id="6ea68-307">Просмотр взаимодействия</span><span class="sxs-lookup"><span data-stu-id="6ea68-307">View interactions</span></span>   

<span data-ttu-id="6ea68-308">В разделе " **взаимодействия** " можно найти и проанализировать взаимодействие с пользователями, произошедшие во время записи.</span><span class="sxs-lookup"><span data-stu-id="6ea68-308">Use the **Interactions** section to find and analyze user interactions that happened during the recording.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-interactions-animation.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-interactions-animation.msft.png":::
   <span data-ttu-id="6ea68-310">Раздел " **взаимодействия** "</span><span class="sxs-lookup"><span data-stu-id="6ea68-310">The **Interactions** section</span></span>  
:::image-end:::  

<span data-ttu-id="6ea68-311">Красная линия в нижней части взаимодействия представляет время, затраченное на ожидание основного потока.</span><span class="sxs-lookup"><span data-stu-id="6ea68-311">A red line at the bottom of an interaction represents time spent waiting for the main thread.</span></span>  

<span data-ttu-id="6ea68-312">Щелкните взаимодействие, чтобы просмотреть дополнительные сведения о нем на вкладке **Сводка** .</span><span class="sxs-lookup"><span data-stu-id="6ea68-312">Click an interaction to view more information about it in the **Summary** tab.</span></span>  

### <span data-ttu-id="6ea68-313">Анализ кадров в секунду (кадр/с)</span><span class="sxs-lookup"><span data-stu-id="6ea68-313">Analyze frames per second (FPS)</span></span>   

<span data-ttu-id="6ea68-314">DevTools предлагает многочисленные способы анализа кадров в секунду.</span><span class="sxs-lookup"><span data-stu-id="6ea68-314">DevTools provides numerous ways to analyze frames per second:</span></span>  

*   <span data-ttu-id="6ea68-315">Используйте [диаграмму в кадре](#the-fps-chart) , чтобы получить обзор кадров в кадре в течение не более чем на продолжительность записи.</span><span class="sxs-lookup"><span data-stu-id="6ea68-315">Use [the FPS chart](#the-fps-chart) to get an overview of FPS over the duration of the recording.</span></span>  
*   <span data-ttu-id="6ea68-316">С помощью [раздела кадры](#the-frames-section) вы можете узнать, сколько времени занимает определенный кадр.</span><span class="sxs-lookup"><span data-stu-id="6ea68-316">Use [the Frames section](#the-frames-section) to view how long a particular frame took.</span></span>  
*   <span data-ttu-id="6ea68-317">Используйте **индикатор кадров между кадрами** для оценки в режиме реального времени при выполнении страницы.</span><span class="sxs-lookup"><span data-stu-id="6ea68-317">Use the **FPS meter** for a realtime estimate of FPS as the page runs.</span></span>  <span data-ttu-id="6ea68-318">Показать [количество кадров в секунду в режиме реального времени с индикатором кадров](#view-frames-per-second-in-realtime-with-the-fps-meter).</span><span class="sxs-lookup"><span data-stu-id="6ea68-318">See [View frames per second in realtime with the FPS meter](#view-frames-per-second-in-realtime-with-the-fps-meter).</span></span>  
    
#### <span data-ttu-id="6ea68-319">Диаграмма кадр/с</span><span class="sxs-lookup"><span data-stu-id="6ea68-319">The FPS chart</span></span>   

<span data-ttu-id="6ea68-320">Диаграмма **кадр/** с — это обзор частоты кадров во время записи.</span><span class="sxs-lookup"><span data-stu-id="6ea68-320">The **FPS** chart provides an overview of the frame rate across the duration of a recording.</span></span>  <span data-ttu-id="6ea68-321">Как правило, чем больше зеленая полоса, тем выше частота кадров.</span><span class="sxs-lookup"><span data-stu-id="6ea68-321">In general, the higher the green bar, the better the frame rate.</span></span>  

<span data-ttu-id="6ea68-322">Красная черта над диаграммой с индикатором **кадров** — это предупреждение о том, что частота кадров отброшена настолько, что она может повредить взаимодействие с пользователем.</span><span class="sxs-lookup"><span data-stu-id="6ea68-322">A red bar above the **FPS** chart is a warning that the frame rate dropped so low that it probably harmed the user's experience.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-fps-highlight.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-fps-highlight.msft.png":::
   <span data-ttu-id="6ea68-324">Диаграмма **кадр/** с</span><span class="sxs-lookup"><span data-stu-id="6ea68-324">The **FPS** chart</span></span>  
:::image-end:::  

#### <span data-ttu-id="6ea68-325">Раздел "кадры"</span><span class="sxs-lookup"><span data-stu-id="6ea68-325">The Frames section</span></span>   

<span data-ttu-id="6ea68-326">Раздел **кадры** содержит сведения о том, сколько времени занимает определенный кадр.</span><span class="sxs-lookup"><span data-stu-id="6ea68-326">The **Frames** section tells you exactly how long a particular frame took.</span></span>  

<span data-ttu-id="6ea68-327">Наведите указатель мыши на кадр, чтобы просмотреть всплывающую подсказку с дополнительными сведениями.</span><span class="sxs-lookup"><span data-stu-id="6ea68-327">Hover over a frame to view a tooltip with more information about it.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-frames-hover.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-frames-hover.msft.png":::
   <span data-ttu-id="6ea68-329">Наведение указателя мыши на рамку</span><span class="sxs-lookup"><span data-stu-id="6ea68-329">Hover over a frame</span></span>  
:::image-end:::  

<span data-ttu-id="6ea68-330">Щелкните рамку, чтобы просмотреть дополнительные сведения о кадре на вкладке " **Сводка** ".  DevTools выделеет выделенный кадр синим цветом.</span><span class="sxs-lookup"><span data-stu-id="6ea68-330">Click on a frame to view even more information about the frame in the **Summary** tab.  DevTools outlines the selected frame in blue.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-frames-summary.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-frames-summary.msft.png":::
   <span data-ttu-id="6ea68-332">Просмотр кадра на вкладке " **Сводка** "</span><span class="sxs-lookup"><span data-stu-id="6ea68-332">View a frame in the **Summary** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="6ea68-333">Просмотр сетевых запросов</span><span class="sxs-lookup"><span data-stu-id="6ea68-333">View network requests</span></span>   

<span data-ttu-id="6ea68-334">Разверните раздел **сеть** , чтобы просмотреть каскадные сетевые запросы, которые произошли во время записи.</span><span class="sxs-lookup"><span data-stu-id="6ea68-334">Expand the **Network** section to view a waterfall of network requests that occurred during the recording.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-network.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-network.msft.png":::
   <span data-ttu-id="6ea68-336">Раздел " **сеть** "</span><span class="sxs-lookup"><span data-stu-id="6ea68-336">The **Network** section</span></span>  
:::image-end:::  

<span data-ttu-id="6ea68-337">Запросы записываются цветом следующим образом:</span><span class="sxs-lookup"><span data-stu-id="6ea68-337">Requests are color-coded as follows:</span></span>  

*   <span data-ttu-id="6ea68-338">HTML: синий</span><span class="sxs-lookup"><span data-stu-id="6ea68-338">HTML: Blue</span></span>  
*   <span data-ttu-id="6ea68-339">CSS: фиолетовый</span><span class="sxs-lookup"><span data-stu-id="6ea68-339">CSS: Purple</span></span>  
*   <span data-ttu-id="6ea68-340">JS: желтый</span><span class="sxs-lookup"><span data-stu-id="6ea68-340">JS: Yellow</span></span>  
*   <span data-ttu-id="6ea68-341">Изображения: зеленые</span><span class="sxs-lookup"><span data-stu-id="6ea68-341">Images: Green</span></span>  
    
<span data-ttu-id="6ea68-342">Щелкните запрос, чтобы просмотреть дополнительные сведения о нем на вкладке " **Сводка** ".  Например, на предыдущем рисунке на вкладке " **Сводка** " отображаются дополнительные сведения о синем запросе, выбранном в разделе " **сеть** ".</span><span class="sxs-lookup"><span data-stu-id="6ea68-342">Click on a request to view more information about it in the **Summary** tab.  For example, in the previous figure, the **Summary** tab is displaying more information about the blue request that is selected in the **Network** section.</span></span>  

<span data-ttu-id="6ea68-343">Темно-синий квадрат в верхней левой части запроса означает, что это запрос более высокого приоритета.</span><span class="sxs-lookup"><span data-stu-id="6ea68-343">A darker-blue square in the top-left of a request means it is a higher-priority request.</span></span>  <span data-ttu-id="6ea68-344">Более светлый квадрат — более низкий приоритет.</span><span class="sxs-lookup"><span data-stu-id="6ea68-344">A lighter-blue square means lower-priority.</span></span>  <span data-ttu-id="6ea68-345">Например, на предыдущем рисунке синий, выбранный запрос имеет более высокий приоритет, а зеленый — более низкий приоритет.</span><span class="sxs-lookup"><span data-stu-id="6ea68-345">For example, in the previous figure, the blue, selected request is higher-priority, and the green one below it is lower-priority.</span></span>  

<span data-ttu-id="6ea68-346">На первой из приведенных ниже рисунков запрос `www.bing.com` будет представлен линией слева, полосой в середине, темной частью и светлой частью и линией справа.</span><span class="sxs-lookup"><span data-stu-id="6ea68-346">In the 1st of the following figures, the request for `www.bing.com` is represented by a line on the left, a bar in the middle with a dark portion and a light portion, and a line on the right.</span></span>  <span data-ttu-id="6ea68-347">На втором рисунке показаны соответствующие представления одного и того же запроса на вкладке **время** на панели **сеть** .</span><span class="sxs-lookup"><span data-stu-id="6ea68-347">In the 2nd of the following figures shows the corresponding representation of the same request in the **Timing** tab of the **Network** panel.</span></span>  <span data-ttu-id="6ea68-348">Ниже показано, как эти два представления соотносятся друг с другом.</span><span class="sxs-lookup"><span data-stu-id="6ea68-348">Here is how these two representations map to each other:</span></span>

*   <span data-ttu-id="6ea68-349">Левая строка — это все, что нужно для `Connection Start` группы событий (включительно).</span><span class="sxs-lookup"><span data-stu-id="6ea68-349">The left line is everything up to the `Connection Start` group of events, inclusive.</span></span>  <span data-ttu-id="6ea68-350">Другими словами, это все, что раньше `Request Sent` , исключительно.</span><span class="sxs-lookup"><span data-stu-id="6ea68-350">In other words, it is everything before `Request Sent`, exclusive.</span></span>  
*   <span data-ttu-id="6ea68-351">Светлая часть панели — `Request Sent` и `Waiting (TTFB)` .</span><span class="sxs-lookup"><span data-stu-id="6ea68-351">The light portion of the bar is `Request Sent` and `Waiting (TTFB)`.</span></span>  
*   <span data-ttu-id="6ea68-352">Темная часть панели `Content Download` .</span><span class="sxs-lookup"><span data-stu-id="6ea68-352">The dark portion of the bar is `Content Download`.</span></span>  
*   <span data-ttu-id="6ea68-353">В настоящее время в течение всего времени, затраченного на ожидание основного потока, в правой строке.</span><span class="sxs-lookup"><span data-stu-id="6ea68-353">The right line is essentially time spent waiting for the main thread.</span></span>  <span data-ttu-id="6ea68-354">Этот параметр не отображается на вкладке **время** .</span><span class="sxs-lookup"><span data-stu-id="6ea68-354">This is not represented in the **Timing** tab.</span></span>  
    
:::row:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-bing-performance-network.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-bing-performance-network.msft.png":::
         <span data-ttu-id="6ea68-356">Представление запроса в виде строки на строке `www.bing.com`</span><span class="sxs-lookup"><span data-stu-id="6ea68-356">The line-bar representation of the `www.bing.com` request</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-bing-network-timing.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-bing-network-timing.msft.png":::
         <span data-ttu-id="6ea68-358">Раздел " **сеть** "</span><span class="sxs-lookup"><span data-stu-id="6ea68-358">The **Network** section</span></span>  
<span data-ttu-id="6ea68-359">::: Image-End:::</span><span class="sxs-lookup"><span data-stu-id="6ea68-359">:      ::image-end:::</span></span>  
   :::column-end:::
:::row-end:::

### <span data-ttu-id="6ea68-360">Просмотр метрик памяти</span><span class="sxs-lookup"><span data-stu-id="6ea68-360">View memory metrics</span></span>   

<span data-ttu-id="6ea68-361">Включите флажок **память** , чтобы просмотреть метрики памяти от последней записи.</span><span class="sxs-lookup"><span data-stu-id="6ea68-361">Enable the **Memory** checkbox to view memory metrics from the last recording.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-memory-highlight.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-memory-highlight.msft.png":::
   <span data-ttu-id="6ea68-363">Флажок " **память** "</span><span class="sxs-lookup"><span data-stu-id="6ea68-363">The **Memory** checkbox</span></span>  
:::image-end:::  

<span data-ttu-id="6ea68-364">DevTools выводит новую диаграмму с **памятью** над вкладкой **Сводка** .  Кроме того, вы также можете создать новую диаграмму под **чистой** диаграммой, называемой **кучей**.</span><span class="sxs-lookup"><span data-stu-id="6ea68-364">DevTools displays a new **Memory** chart, above the **Summary** tab.  There is also a new chart below the **NET** chart, called **HEAP**.</span></span>  <span data-ttu-id="6ea68-365">Диаграмма **кучи** предоставляет те же данные, что и в линии **кучи JS** в диаграмме с **памятью** .</span><span class="sxs-lookup"><span data-stu-id="6ea68-365">The **HEAP** chart provides the same information as the **JS Heap** line in the **Memory** chart.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-memory-chart.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-memory-chart.msft.png":::
   <span data-ttu-id="6ea68-367">Метрики памяти</span><span class="sxs-lookup"><span data-stu-id="6ea68-367">Memory metrics</span></span>  
:::image-end:::  

<span data-ttu-id="6ea68-368">Цветные линии на диаграмме сопоставляются с цветными флажками над диаграммой.</span><span class="sxs-lookup"><span data-stu-id="6ea68-368">The colored lines on the chart map to the colored checkboxes above the chart.</span></span>  
<span data-ttu-id="6ea68-369">Отключите флажок, чтобы скрыть эту категорию на диаграмме.</span><span class="sxs-lookup"><span data-stu-id="6ea68-369">Disable a checkbox to hide that category from the chart.</span></span>  

<span data-ttu-id="6ea68-370">На диаграмме отображается только область текущей записи.</span><span class="sxs-lookup"><span data-stu-id="6ea68-370">The chart only displays the region of the recording that is currently selected.</span></span>  <span data-ttu-id="6ea68-371">Например, на предыдущем рисунке диаграмма **памяти** показывает использование памяти только вокруг 400 MS, помечая его на 1750 MS.</span><span class="sxs-lookup"><span data-stu-id="6ea68-371">For example, in the previous figure, the **Memory** chart is only showing memory usage from around the 400 ms mark to the 1750 ms mark.</span></span>  

### <span data-ttu-id="6ea68-372">Просмотр длительности части записи</span><span class="sxs-lookup"><span data-stu-id="6ea68-372">View the duration of a portion of a recording</span></span>   

<span data-ttu-id="6ea68-373">При анализе раздела, например " **сеть** " или " **основной**", иногда требуется более точная оценка продолжительности определенных событий.</span><span class="sxs-lookup"><span data-stu-id="6ea68-373">When analyzing a section like **Network** or **Main**, sometimes you need a more precise estimate of how long certain events took.</span></span>  <span data-ttu-id="6ea68-374">`Shift`Чтобы выделить часть записи, перетащите указатель влево или вправо, удерживая нажатой клавишу CTRL.</span><span class="sxs-lookup"><span data-stu-id="6ea68-374">Hold `Shift`, click and hold, and drag left or right to select a portion of the recording.</span></span>  <span data-ttu-id="6ea68-375">В нижней части выделенного фрагмента DevTools показывает, сколько времени заняло эта часть.</span><span class="sxs-lookup"><span data-stu-id="6ea68-375">At the bottom of your selection, DevTools shows how long that portion took.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-main-duration.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-main-duration.msft.png":::
   <span data-ttu-id="6ea68-377">Просмотр длительности части записи</span><span class="sxs-lookup"><span data-stu-id="6ea68-377">View the duration of a portion of a recording</span></span>  
:::image-end:::  

### <span data-ttu-id="6ea68-378">Просмотр снимка экрана</span><span class="sxs-lookup"><span data-stu-id="6ea68-378">View a screenshot</span></span>   

<span data-ttu-id="6ea68-379">Сведения о включении снимков экрана можно найти в разделе [запись снимков экрана](#capture-screenshots-while-recording) .</span><span class="sxs-lookup"><span data-stu-id="6ea68-379">See [Capture screenshots while recording](#capture-screenshots-while-recording) to learn how to enable screenshots.</span></span>  

<span data-ttu-id="6ea68-380">Наведите указатель мыши на **Обзор** , чтобы просмотреть снимок экрана, на котором размещается страница в этот момент записи.</span><span class="sxs-lookup"><span data-stu-id="6ea68-380">Hover over the **Overview** to view a screenshot of how the page looked during that moment of the recording.</span></span>  <span data-ttu-id="6ea68-381">**Обзор** — это раздел, содержащий диаграммы **ЦП**, **кадров между кадрами**и **сети** .</span><span class="sxs-lookup"><span data-stu-id="6ea68-381">The **Overview** is the section that contains the **CPU**, **FPS**, and **NET** charts.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-screenshots-hover.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-screenshots-hover.msft.png":::
   <span data-ttu-id="6ea68-383">Просмотр снимка экрана</span><span class="sxs-lookup"><span data-stu-id="6ea68-383">View a screenshot</span></span>  
:::image-end:::  

<span data-ttu-id="6ea68-384">Вы также можете просмотреть снимки экрана, щелкнув кадр в разделе **кадры** .</span><span class="sxs-lookup"><span data-stu-id="6ea68-384">You may also view screenshots by clicking a frame in the **Frames** section.</span></span>  <span data-ttu-id="6ea68-385">DevTools отображает маленькую версию снимка экрана на вкладке " **Сводка** ".</span><span class="sxs-lookup"><span data-stu-id="6ea68-385">DevTools displays a small version of the screenshot in the **Summary** tab.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-summary-preview.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-summary-preview.msft.png":::
   <span data-ttu-id="6ea68-387">Просмотр снимка экрана на вкладке " **Сводка** "</span><span class="sxs-lookup"><span data-stu-id="6ea68-387">View a screenshot in the **Summary** tab</span></span>  
:::image-end:::  

<span data-ttu-id="6ea68-388">Щелкните эскиз на вкладке " **Сводка** ", чтобы увеличить масштаб на снимке экрана.</span><span class="sxs-lookup"><span data-stu-id="6ea68-388">Click the thumbnail in the **Summary** tab to zoom in on the screenshot.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-summary-preview-select.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-summary-preview-select.msft.png":::
   <span data-ttu-id="6ea68-390">Изменение масштаба экрана на вкладке " **Сводка** "</span><span class="sxs-lookup"><span data-stu-id="6ea68-390">Zoom into a screenshot from the **Summary** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="6ea68-391">Просмотр сведений о слоях</span><span class="sxs-lookup"><span data-stu-id="6ea68-391">View layers information</span></span>   

<span data-ttu-id="6ea68-392">Чтобы просмотреть дополнительные сведения о кадре, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="6ea68-392">To view advanced layers information about a frame:</span></span>  

1.  <span data-ttu-id="6ea68-393">[Включите дополнительные инструменты рисования](#enable-advanced-paint-instrumentation).</span><span class="sxs-lookup"><span data-stu-id="6ea68-393">[Enable advanced paint instrumentation](#enable-advanced-paint-instrumentation).</span></span>  
1.  <span data-ttu-id="6ea68-394">Выберите кадр в разделе **кадры** .</span><span class="sxs-lookup"><span data-stu-id="6ea68-394">Select a frame in the **Frames** section.</span></span>  <span data-ttu-id="6ea68-395">DevTools отображает сведения о слоях на вкладке Создание **слоев** рядом с вкладкой **журнал событий** .</span><span class="sxs-lookup"><span data-stu-id="6ea68-395">DevTools displays information about the layers in the new **Layers** tab, next to the **Event Log** tab.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-layers-all.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-layers-all.msft.png":::
       <span data-ttu-id="6ea68-397">Область **слоев**</span><span class="sxs-lookup"><span data-stu-id="6ea68-397">The **Layers** pane</span></span>  
    :::image-end:::  
    
<span data-ttu-id="6ea68-398">Наведите указатель мыши на слой, чтобы выделить его на схеме.</span><span class="sxs-lookup"><span data-stu-id="6ea68-398">Hover over a layer to highlight it in the diagram.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-frames-document-nav-bar-highlighted.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-frames-document-nav-bar-highlighted.msft.png":::
   <span data-ttu-id="6ea68-400">Выделение слоя</span><span class="sxs-lookup"><span data-stu-id="6ea68-400">Highlight a layer</span></span>  
:::image-end:::  

<span data-ttu-id="6ea68-401">Чтобы переместить схему, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="6ea68-401">To move the diagram:</span></span>  

*   <span data-ttu-id="6ea68-402">Щелкните **режим панорамирования** \ ( ![ режим панорамирования ][ImagePanModeIcon] ), чтобы перемещаться вдоль осей X и Y.</span><span class="sxs-lookup"><span data-stu-id="6ea68-402">Click **Pan Mode** \(![Pan Mode][ImagePanModeIcon]\) to move along the X and Y axes.</span></span>  
*   <span data-ttu-id="6ea68-403">Выберите **режим поворота** \ ( ![ режим поворота ][ImageRotateModeIcon] \) для поворота вдоль оси Z.</span><span class="sxs-lookup"><span data-stu-id="6ea68-403">Click **Rotate Mode** \(![Rotate Mode][ImageRotateModeIcon]\) to rotate along the Z axis.</span></span>  
*   <span data-ttu-id="6ea68-404">Нажмите кнопку **Сброс преобразования** \ ( ![ Сброс преобразования ][ImageResetTransformIcon] ), чтобы восстановить исходное расположение схемы.</span><span class="sxs-lookup"><span data-stu-id="6ea68-404">Click **Reset Transform** \(![Reset Transform][ImageResetTransformIcon]\) to reset the diagram to the original position.</span></span>  
    
### <span data-ttu-id="6ea68-405">Просмотр профилировщика Paint</span><span class="sxs-lookup"><span data-stu-id="6ea68-405">View paint profiler</span></span>   

<span data-ttu-id="6ea68-406">Чтобы просмотреть дополнительные сведения о событии Paint, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="6ea68-406">To view advanced information about a paint event:</span></span>  

1.  <span data-ttu-id="6ea68-407">[Включите дополнительные инструменты рисования](#enable-advanced-paint-instrumentation).</span><span class="sxs-lookup"><span data-stu-id="6ea68-407">[Enable advanced paint instrumentation](#enable-advanced-paint-instrumentation).</span></span>  
1.  <span data-ttu-id="6ea68-408">Выберите событие **Paint** в **главном** разделе.</span><span class="sxs-lookup"><span data-stu-id="6ea68-408">Select a **Paint** event in the **Main** section.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-paint-profiler.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-paint-profiler.msft.png":::
       <span data-ttu-id="6ea68-410">Вкладка " **профилировщик Paint** "</span><span class="sxs-lookup"><span data-stu-id="6ea68-410">The **Paint Profiler** tab</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="6ea68-411">Анализ производительности отрисовки с помощью вкладки "рендеринг"</span><span class="sxs-lookup"><span data-stu-id="6ea68-411">Analyze rendering performance with the Rendering tab</span></span>   

<span data-ttu-id="6ea68-412">С помощью функций вкладки " **отрисовка** " можно визуализировать эффективность отрисовки страницы.</span><span class="sxs-lookup"><span data-stu-id="6ea68-412">Use the features of the **Rendering** tab to help visualize the rendering performance of your page.</span></span>  

<span data-ttu-id="6ea68-413">Чтобы открыть вкладку **рендеринга** , выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="6ea68-413">To open the **Rendering** tab:</span></span>  

1.  <span data-ttu-id="6ea68-414">[Открытие меню команд][DevToolsCommandMenu].</span><span class="sxs-lookup"><span data-stu-id="6ea68-414">[Open the Command Menu][DevToolsCommandMenu].</span></span>  
1.  <span data-ttu-id="6ea68-415">Начните вводить текст `Rendering` и выберите его `Show Rendering` .</span><span class="sxs-lookup"><span data-stu-id="6ea68-415">Start typing `Rendering` and select `Show Rendering`.</span></span>  <span data-ttu-id="6ea68-416">DevTools отображает вкладку **рендеринг** в нижней части окна DevTools.</span><span class="sxs-lookup"><span data-stu-id="6ea68-416">DevTools displays the **Rendering** tab at the bottom of your DevTools window.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-console-drawer-rendering.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-console-drawer-rendering.msft.png":::
       <span data-ttu-id="6ea68-418">Вкладка « **рендеринг** »</span><span class="sxs-lookup"><span data-stu-id="6ea68-418">The **Rendering** tab</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="6ea68-419">Просмотр кадров в секунду в режиме реального времени с индикатором кадров</span><span class="sxs-lookup"><span data-stu-id="6ea68-419">View frames per second in realtime with the FPS meter</span></span>   

<span data-ttu-id="6ea68-420">**Индикатор кадров в кадрах** — это наложение, которое отображается в правом верхнем углу окна просмотра.</span><span class="sxs-lookup"><span data-stu-id="6ea68-420">The **FPS meter** is an overlay that appears in the top-right corner of your viewport.</span></span>  <span data-ttu-id="6ea68-421">Она предоставляет оценку кадров в реальном времени при выполнении страницы.</span><span class="sxs-lookup"><span data-stu-id="6ea68-421">It provides a realtime estimate of FPS as the page runs.</span></span>  <span data-ttu-id="6ea68-422">Чтобы открыть **индикатор кадров**, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="6ea68-422">To open the **FPS meter**:</span></span>  

1.  <span data-ttu-id="6ea68-423">Открытие вкладки " **рендеринг** ".  Ознакомьтесь с разработкой [Анализ производительности отрисовки с помощью вкладки рендеринг](#analyze-rendering-performance-with-the-rendering-tab).</span><span class="sxs-lookup"><span data-stu-id="6ea68-423">Open the **Rendering** tab.  See [Analyze rendering performance with the Rendering tab](#analyze-rendering-performance-with-the-rendering-tab).</span></span>  
1.  <span data-ttu-id="6ea68-424">Включите флажок **индикатор кадров в кадре** .</span><span class="sxs-lookup"><span data-stu-id="6ea68-424">Enable the **FPS Meter** checkbox.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-jank-console-rendering-frame-rate.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-jank-console-rendering-frame-rate.msft.png":::
       <span data-ttu-id="6ea68-426">**Индикатор кадров в кадре**</span><span class="sxs-lookup"><span data-stu-id="6ea68-426">The **FPS meter**</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="6ea68-427">Просмотр событий рисования в реальном времени с помощью помигания Paint</span><span class="sxs-lookup"><span data-stu-id="6ea68-427">View painting events in realtime with Paint Flashing</span></span>   

<span data-ttu-id="6ea68-428">Чтобы получить представление о всех событиях рисования на странице в реальном времени, используйте Paint.</span><span class="sxs-lookup"><span data-stu-id="6ea68-428">Use Paint Flashing to get a realtime view of all paint events on the page.</span></span>  <span data-ttu-id="6ea68-429">Каждый раз, когда часть страницы зарисуется повторно, DevTools разменяет его зеленым цветом.</span><span class="sxs-lookup"><span data-stu-id="6ea68-429">Whenever a part of the page gets re-painted, DevTools outlines that section in green.</span></span>  

<span data-ttu-id="6ea68-430">Чтобы включить мигание краски, сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="6ea68-430">To enable Paint Flashing:</span></span>  

1.  <span data-ttu-id="6ea68-431">Открытие вкладки " **рендеринг** ".  Ознакомьтесь с разработкой [Анализ производительности отрисовки с помощью вкладки рендеринг](#analyze-rendering-performance-with-the-rendering-tab).</span><span class="sxs-lookup"><span data-stu-id="6ea68-431">Open the **Rendering** tab.  See [Analyze rendering performance with the Rendering tab](#analyze-rendering-performance-with-the-rendering-tab).</span></span>  
1.  <span data-ttu-id="6ea68-432">Установите флажок **закрасить мигающий** .</span><span class="sxs-lookup"><span data-stu-id="6ea68-432">Enable the **Paint Flashing** checkbox.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-jank-console-rendering-paint-flashing.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-jank-console-rendering-paint-flashing.msft.png":::
       **<span data-ttu-id="6ea68-434">Мигание краски</span><span class="sxs-lookup"><span data-stu-id="6ea68-434">Paint Flashing</span></span>**  
    :::image-end:::  
    
### <span data-ttu-id="6ea68-435">Просмотр наложения слоев с границами слоев</span><span class="sxs-lookup"><span data-stu-id="6ea68-435">View an overlay of layers with Layer Borders</span></span>   

<span data-ttu-id="6ea68-436">Используйте **границы слоев** для просмотра наложенных границ слоев и плиток в верхней части страницы.</span><span class="sxs-lookup"><span data-stu-id="6ea68-436">Use **Layer Borders** to view an overlay of layer borders and tiles on top of the page.</span></span>  

<span data-ttu-id="6ea68-437">Чтобы включить границы слоев, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="6ea68-437">To enable Layer Borders:</span></span>  

1.  <span data-ttu-id="6ea68-438">Открытие вкладки " **рендеринг** ".  Ознакомьтесь с разработкой [Анализ производительности отрисовки с помощью вкладки рендеринг](#analyze-rendering-performance-with-the-rendering-tab).</span><span class="sxs-lookup"><span data-stu-id="6ea68-438">Open the **Rendering** tab.  See [Analyze rendering performance with the Rendering tab](#analyze-rendering-performance-with-the-rendering-tab).</span></span>  
1.  <span data-ttu-id="6ea68-439">Установите флажок **границы слоя** .</span><span class="sxs-lookup"><span data-stu-id="6ea68-439">Enable the **Layer Borders** checkbox.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-devtools-console-rendering-layer-borders.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-devtools-console-rendering-layer-borders.msft.png":::
       **<span data-ttu-id="6ea68-441">Границы слоев</span><span class="sxs-lookup"><span data-stu-id="6ea68-441">Layer Borders</span></span>**  
    :::image-end:::  
    
<span data-ttu-id="6ea68-442">Ознакомьтесь с комментариями [`debug_colors.cc`][ChromiumDebugColors] , изложенными в разделе Описание цветовых кодирования.</span><span class="sxs-lookup"><span data-stu-id="6ea68-442">See the comments in [`debug_colors.cc`][ChromiumDebugColors] for an explanation of the color-codings.</span></span>  

### <span data-ttu-id="6ea68-443">Поиск проблем с производительностью прокрутки в реальном времени</span><span class="sxs-lookup"><span data-stu-id="6ea68-443">Find scroll performance issues in realtime</span></span>   

<span data-ttu-id="6ea68-444">Используйте проблемы с производительностью прокрутки, чтобы идентифицировать элементы страницы, которые содержат прослушиватели событий, связанные с прокруткой, которые могут повредить производительность страницы.</span><span class="sxs-lookup"><span data-stu-id="6ea68-444">Use Scrolling Performance Issues to identify elements of the page that have event listeners related to scrolling that may harm the performance of the page.</span></span>  
<span data-ttu-id="6ea68-445">DevTools поменяет потенциально проблематичные элементы в синем тексте.</span><span class="sxs-lookup"><span data-stu-id="6ea68-445">DevTools outlines the potentially-problematic elements in teal.</span></span>  

<span data-ttu-id="6ea68-446">Для просмотра проблем с производительностью прокрутки:</span><span class="sxs-lookup"><span data-stu-id="6ea68-446">To view scroll performance issues:</span></span>  

1.  <span data-ttu-id="6ea68-447">Открытие вкладки " **рендеринг** ".  Ознакомьтесь с разработкой [Анализ производительности отрисовки с помощью вкладки рендеринг](#analyze-rendering-performance-with-the-rendering-tab).</span><span class="sxs-lookup"><span data-stu-id="6ea68-447">Open the **Rendering** tab.  See [Analyze rendering performance with the Rendering tab](#analyze-rendering-performance-with-the-rendering-tab).</span></span>  
1.  <span data-ttu-id="6ea68-448">Включите флажок **проблемы с прокруткой** .</span><span class="sxs-lookup"><span data-stu-id="6ea68-448">Enable the **Scrolling Performance Issues** checkbox.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-bing-console-drawer-rendering-scrolling-performance-issues.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-bing-console-drawer-rendering-scrolling-performance-issues.msft.png":::
       <span data-ttu-id="6ea68-450">**Прокрутка проблем с производительностью** указывает на то, что объекты просмотра, не связанные с разслойю, могут повредить производительность при прокрутке.</span><span class="sxs-lookup"><span data-stu-id="6ea68-450">**Scrolling Performance Issues** indicates that non-layer viewport-constrained objects may harm scroll performance</span></span>  
    :::image-end:::  
    
<!--  
<!--    


-->  

<!-- image links -->  

[ImageCaptureSettingsIcon]: ../media/capture-settings-icon.msft.png  
[ImageClearRecordingIcon]: ../media/clear-recording-icon.msft.png  
[ImageCollectGarbageIcon]: ../media/collect-garbage-icon.msft.png  
[ImageNextIcon]: ../media/next-icon.msft.png  
[ImagePanModeIcon]: ../media/pan-mode-icon.msft.png  
[ImagePreviousIcon]: ../media/previous-icon.msft.png  
[ImageRecordIcon]: ../media/record-icon.msft.png
[ImageRefreshPageIcon]: ../media/refresh-page-icon.msft.png  
[ImageResetTransformIcon]: ../media/reset-transform-icon.msft.png  
[ImageRotateModeIcon]: ../media/rotate-mode-icon.msft.png  
[ImageSearchCaseIcon]: ../media/search-case-icon.msft.png  
[ImageSearchRegexIcon]: ../media/search-regex-icon.msft.png  
[ImageShowHeaviestStackIcon]: ../media/show-heaviest-stack-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Инструменты разработчика Microsoft EDGE (Chromium) | Документы Microsoft"  
[DevToolsCommandMenu]: ../command-menu/index.md#open-the-command-menu "Открытие меню команд — команды "выполнить" с помощью меню "команда" Microsoft Edge DevTools | Документы Microsoft"  
[DevtoolsEvaluatePerformanceGettingStarted]: ./index.md "Приступая к анализу производительности среды выполнения | Документы Microsoft"  

[ActivityTabsDemo]: https://microsoft-edge-chromium-devtools.glitch.me/perf/activitytabs.html "Пример вкладки "действия" | цепь"  

[ChromiumDebugColors]: https://cs.chromium.org/chromium/src/cc/debug/debug_colors.cc "debug_colors поиска CC-Code"  

> [!NOTE]
> <span data-ttu-id="6ea68-456">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="6ea68-456">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="6ea68-457">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/reference) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="6ea68-457">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="6ea68-459">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="6ea68-459">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
