---
description: Сведения о том, как оценивать производительность среды выполнения в Microsoft Edge DevTools.
title: Приступая к анализу производительности среды выполнения
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 7cb1d8f073cdb8a43093514dd7dea86d72102011
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "11124987"
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

# <span data-ttu-id="c3046-104">Приступая к анализу производительности среды выполнения</span><span class="sxs-lookup"><span data-stu-id="c3046-104">Get started with analyzing Runtime performance</span></span>  

> [!NOTE]
> <span data-ttu-id="c3046-105">Чтобы получить сведения о том, как ускорить загрузку страниц, перейдите к разделу [Оптимизация веб-сайта][DevtoolsSpeedGetStarted].</span><span class="sxs-lookup"><span data-stu-id="c3046-105">To learn how to make your pages load faster, navigate to [Optimize Website Speed][DevtoolsSpeedGetStarted].</span></span>  

<span data-ttu-id="c3046-106">Производительность во время выполнения — это то, как страница выполняется при ее запуске, а не в виде загрузки.</span><span class="sxs-lookup"><span data-stu-id="c3046-106">Runtime performance is how your page performs when it is running, as opposed to loading.</span></span>  <span data-ttu-id="c3046-107">В следующей статье учебника объясняется, как использовать панель производительности Microsoft Edge DevTools для анализа производительности среды выполнения.</span><span class="sxs-lookup"><span data-stu-id="c3046-107">The following tutorial article teaches you how to use the Microsoft Edge DevTools Performance panel to analyze runtime performance.</span></span>  <span data-ttu-id="c3046-108">В плане модели **салазок** уровни опыта, описанные в этом учебнике, полезны для анализа отклика, анимации и этапов простоя страницы.</span><span class="sxs-lookup"><span data-stu-id="c3046-108">In terms of the **RAIL** model, the skills you learn in this tutorial are useful for analyzing the Response, Animation, and Idle phases of your page.</span></span>  

<!--todo: add rail link when section is ready -->  

## <span data-ttu-id="c3046-109">Начало работы</span><span class="sxs-lookup"><span data-stu-id="c3046-109">Get started</span></span>  

<span data-ttu-id="c3046-110">В следующем учебнике вы откроете DevTools на реальной странице и с помощью панели " **производительность** " найдите узкое место на странице.</span><span class="sxs-lookup"><span data-stu-id="c3046-110">In the following tutorial, you open DevTools on a live page and use the **Performance** panel to find a performance bottleneck on the page.</span></span>  

1.  <span data-ttu-id="c3046-111">Откройте Microsoft EDGE в **режиме InPrivate**.</span><span class="sxs-lookup"><span data-stu-id="c3046-111">Open Microsoft Edge in **InPrivate Mode**.</span></span>  <span data-ttu-id="c3046-112">Режим InPrivate обеспечивает выполнение Microsoft EDGE в чистом состоянии.</span><span class="sxs-lookup"><span data-stu-id="c3046-112">InPrivate Mode ensures that Microsoft Edge runs in a clean state.</span></span>  <span data-ttu-id="c3046-113">Например, если на вашем компьютере установлено большое количество расширений, эти расширения могут создать шум в измерениях производительности.</span><span class="sxs-lookup"><span data-stu-id="c3046-113">For example, if you have a lot of extensions installed, the extensions may create noise in your performance measurements.</span></span>  
    
    <!--TODO: replace section when updated for new Edge  -->
    
1.  <span data-ttu-id="c3046-114">Загрузите следующую страницу в окне InPrivate.</span><span class="sxs-lookup"><span data-stu-id="c3046-114">Load the following page in your InPrivate window.</span></span>  <span data-ttu-id="c3046-115">Страница — это демонстрационный ролик, который вы собираетесь профилировать.</span><span class="sxs-lookup"><span data-stu-id="c3046-115">The page is the demo that you are going to profile.</span></span>  <span data-ttu-id="c3046-116">На странице показан ряд маленьких значков, перемещаясь вверх и вниз.</span><span class="sxs-lookup"><span data-stu-id="c3046-116">The page shows a bunch of little icons moving up and down.</span></span>  
    
    ```https
    https://microsoft-edge-chromium-devtools.glitch.me/sluggish/
    ```  
    
1.  <span data-ttu-id="c3046-117">Выберите `Control` + `Shift` + `I` \ (Windows, Linux \) или `Command` + `Option` + `I` \ (macOS \), чтобы открыть DevTools.</span><span class="sxs-lookup"><span data-stu-id="c3046-117">Select `Control`+`Shift`+`I` \(Windows, Linux\) or `Command`+`Option`+`I` \(macOS\) to open DevTools.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-get-started-side-by-side.msft.png" alt-text="Демонстрация слева и DevTools справа" lightbox="../media/evaluate-performance-get-started-side-by-side.msft.png":::
       <span data-ttu-id="c3046-119">Демонстрация слева и DevTools справа</span><span class="sxs-lookup"><span data-stu-id="c3046-119">The demo on the left, and DevTools on the right</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="c3046-120">В остальных рисунках DevTools [отсоединяется в отдельном окне][DevtoolsCustomizePlacement] , чтобы лучше сосредоточиться на содержимом.</span><span class="sxs-lookup"><span data-stu-id="c3046-120">For the rest of the figures, DevTools is [undocked to a separate window][DevtoolsCustomizePlacement] to better focus on the contents.</span></span>  
    
### <span data-ttu-id="c3046-121">Имитация мобильного ЦП</span><span class="sxs-lookup"><span data-stu-id="c3046-121">Simulate a mobile CPU</span></span>  

<span data-ttu-id="c3046-122">На мобильных устройствах больше энергии ЦП, чем на настольных компьютерах и ноутбуках.</span><span class="sxs-lookup"><span data-stu-id="c3046-122">Mobile devices have much less CPU power than desktops and laptops.</span></span>  <span data-ttu-id="c3046-123">Каждый раз, когда вы профилем страницы, используйте метод регулирования ЦП для моделирования того, как страница работает на мобильных устройствах.</span><span class="sxs-lookup"><span data-stu-id="c3046-123">Whenever you profile a page, use CPU Throttling to simulate how your page performs on mobile devices.</span></span>  

1.  <span data-ttu-id="c3046-124">В DevTools выберите вкладку **Performance (производительность** ).</span><span class="sxs-lookup"><span data-stu-id="c3046-124">In DevTools, choose the **Performance** tab.</span></span>  
1.  <span data-ttu-id="c3046-125">Убедитесь, что флажок **снимки экрана** включен.</span><span class="sxs-lookup"><span data-stu-id="c3046-125">Make sure that the **Screenshots** checkbox is enabled.</span></span>  
1.  <span data-ttu-id="c3046-126">Выберите **Параметры захвата** \ (! [ Параметры захвата] [ImageCaptureSettingsIcon] \).</span><span class="sxs-lookup"><span data-stu-id="c3046-126">Choose **Capture Settings** \(![Capture Settings][ImageCaptureSettingsIcon]\).</span></span>  <span data-ttu-id="c3046-127">DevTools показывает параметры, связанные с тем, как они захватывают метрики производительности.</span><span class="sxs-lookup"><span data-stu-id="c3046-127">DevTools reveals settings related to how it captures performance metrics.</span></span>  
1.  <span data-ttu-id="c3046-128">Для использования **ЦП**выберите пункт **замедление 4X**.</span><span class="sxs-lookup"><span data-stu-id="c3046-128">For **CPU**, choose **4x slowdown**.</span></span>  <span data-ttu-id="c3046-129">DevTools загружает ЦП так, чтобы он был 4 медленнее, чем обычно.</span><span class="sxs-lookup"><span data-stu-id="c3046-129">DevTools throttles your CPU so that it is 4 times slower than usual.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-capture-settings.msft.png" alt-text="Демонстрация слева и DevTools справа" lightbox="../media/evaluate-performance-performance-capture-settings.msft.png":::
       <span data-ttu-id="c3046-131">Интервал регулирования ЦП</span><span class="sxs-lookup"><span data-stu-id="c3046-131">CPU throttle</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="c3046-132">При тестировании других страниц; Если вы хотите, чтобы каждая страница хорошо работала на мобильных устройствах с низким интерфейсом, установите для ускорения ЦП **6X**скорость.</span><span class="sxs-lookup"><span data-stu-id="c3046-132">When testing other pages; if you want to ensure that each page works well on low-end mobile devices, set CPU Throttling to **6x slowdown**.</span></span>  <span data-ttu-id="c3046-133">Демонстрационный ролик не работает с 6xем замедления, поэтому он просто использует 4X для целей.</span><span class="sxs-lookup"><span data-stu-id="c3046-133">The demo does not work well with 6x slowdown, so it just uses 4x slowdown for instructional purposes.</span></span>  
    
### <span data-ttu-id="c3046-134">Настройка ролика</span><span class="sxs-lookup"><span data-stu-id="c3046-134">Set up the demo</span></span>  

<span data-ttu-id="c3046-135">Очень сложно создать демонстрацию производительности во время выполнения, который постоянно подходит для всех читателей веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="c3046-135">It is hard to create a runtime performance demo that works consistently for all readers of the website.</span></span>  <span data-ttu-id="c3046-136">В следующем разделе описано, как настроить демонстрацию, чтобы убедиться в том, что взаимодействие между снимками экрана и описаниями не зависит от конкретной настройки.</span><span class="sxs-lookup"><span data-stu-id="c3046-136">The following section lets you customize the demo to ensure that your experience is relatively consistent with the screenshots and descriptions, regardless of your particular set up.</span></span>

1.  <span data-ttu-id="c3046-137">Нажмите кнопку " **Добавить 10** ", чтобы синий значок не перемещался заметно медленнее.</span><span class="sxs-lookup"><span data-stu-id="c3046-137">Choose the **Add 10** button until the blue icons move noticeably slower than before.</span></span>  <span data-ttu-id="c3046-138">На высоком уровне компьютера вы можете выбрать его в течение 20 появлений.</span><span class="sxs-lookup"><span data-stu-id="c3046-138">On a high-end machine, you may to choose it about 20 times.</span></span>  
1.  <span data-ttu-id="c3046-139">Нажмите кнопку **оптимизировать**.</span><span class="sxs-lookup"><span data-stu-id="c3046-139">Choose **Optimize**.</span></span>  <span data-ttu-id="c3046-140">Синие значки должны двигаться быстрее и более гладко.</span><span class="sxs-lookup"><span data-stu-id="c3046-140">The blue icons should move faster and more smoothly.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="c3046-141">Для лучшего отображения различий между оптимизированными и неоптимизированными версиями нажмите кнопку " **вычесть 10** " несколько раз, а затем повторите попытку.</span><span class="sxs-lookup"><span data-stu-id="c3046-141">To better display a difference between the optimized and un-optimized versions, choose the **Subtract 10** button a few times and try again.</span></span>  
    > <span data-ttu-id="c3046-142">Если вы добавите слишком много синих значков, вы можете получить максимум ресурсов ЦП, и вы можете не заметить существенных различий в результатах двух версий.</span><span class="sxs-lookup"><span data-stu-id="c3046-142">If you add too many blue icons, you may max out the CPU and then you may not observe a major difference in the results for the two versions.</span></span>  
    
1.  <span data-ttu-id="c3046-143">Нажмите **Отмена оптимизации**.</span><span class="sxs-lookup"><span data-stu-id="c3046-143">Choose **Un-Optimize**.</span></span>  <span data-ttu-id="c3046-144">Синие значки перемещаются медленнее и с более низкой скоростью.</span><span class="sxs-lookup"><span data-stu-id="c3046-144">The blue icons move slower and with more sluggishness again.</span></span>  
    
### <span data-ttu-id="c3046-145">Запись производительности среды выполнения</span><span class="sxs-lookup"><span data-stu-id="c3046-145">Record runtime performance</span></span>  

<span data-ttu-id="c3046-146">Когда вы запустили оптимизированную версию страницы, синие значки перемещаются быстрее.</span><span class="sxs-lookup"><span data-stu-id="c3046-146">When you ran the optimized version of the page, the blue icons move faster.</span></span>  <span data-ttu-id="c3046-147">Почему так?</span><span class="sxs-lookup"><span data-stu-id="c3046-147">Why is that?</span></span>  <span data-ttu-id="c3046-148">Обе версии предназначены для того, чтобы переместить значки в одинаковые промежутки времени.</span><span class="sxs-lookup"><span data-stu-id="c3046-148">Both versions are supposed to move the icons the same amount of space in the same amount of time.</span></span>  <span data-ttu-id="c3046-149">Чтобы выяснить, как выявить узкие места производительности в неоптимизированной версии, сделайте запись на панели производительности.</span><span class="sxs-lookup"><span data-stu-id="c3046-149">Take a recording in the Performance panel to learn how to detect the performance bottleneck in the un-optimized version.</span></span>  

1.  <span data-ttu-id="c3046-150">В DevTools выберите **запись** \ (! [ Record] [ImageRecordIcon] \).</span><span class="sxs-lookup"><span data-stu-id="c3046-150">In DevTools, choose **Record** \(![Record][ImageRecordIcon]\).</span></span>  <span data-ttu-id="c3046-151">DevTools захватывает метрики производительности по мере выполнения страницы.</span><span class="sxs-lookup"><span data-stu-id="c3046-151">DevTools captures performance metrics as the page runs.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-profiling.msft.png" alt-text="Демонстрация слева и DevTools справа" lightbox="../media/evaluate-performance-performance-profiling.msft.png":::
       <span data-ttu-id="c3046-153">Профилирование страницы</span><span class="sxs-lookup"><span data-stu-id="c3046-153">Profile the page</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c3046-154">Подождите несколько секунд.</span><span class="sxs-lookup"><span data-stu-id="c3046-154">Wait a few seconds.</span></span>  
1.  <span data-ttu-id="c3046-155">Нажмите кнопку **остановить**.</span><span class="sxs-lookup"><span data-stu-id="c3046-155">Choose **Stop**.</span></span>  <span data-ttu-id="c3046-156">DevTools останавливает запись, обрабатывает данные, а затем отображает результаты на панели Performance.</span><span class="sxs-lookup"><span data-stu-id="c3046-156">DevTools stops recording, processes the data, then displays the results on the Performance panel.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-capture-results.msft.png" alt-text="Демонстрация слева и DevTools справа" lightbox="../media/evaluate-performance-performance-capture-results.msft.png":::
       <span data-ttu-id="c3046-158">Результаты профиля</span><span class="sxs-lookup"><span data-stu-id="c3046-158">The results of the profile</span></span>  
    :::image-end:::  
    
<span data-ttu-id="c3046-159">Wow, это является большим объемом данных.</span><span class="sxs-lookup"><span data-stu-id="c3046-159">Wow, that is an overwhelming amount of data.</span></span>  <span data-ttu-id="c3046-160">не беспокойтесь, в скором времени процесс становится более понятным.</span><span class="sxs-lookup"><span data-stu-id="c3046-160">do not worry, soon the process makes more sense.</span></span>  

## <span data-ttu-id="c3046-161">Анализ результатов</span><span class="sxs-lookup"><span data-stu-id="c3046-161">Analyze the results</span></span>  

<span data-ttu-id="c3046-162">После того как вы зарегистрируете производительность страницы, измерьте качество ее функционирования и получите все причины.</span><span class="sxs-lookup"><span data-stu-id="c3046-162">After you record the performance of the page, measure the quality of the performance of the page and find the any causes.</span></span>  

### <span data-ttu-id="c3046-163">Анализ кадров в секунду</span><span class="sxs-lookup"><span data-stu-id="c3046-163">Analyze frames per second</span></span>  

<span data-ttu-id="c3046-164">Основная метрика для измерения производительности любой анимации — число кадров в секунду с повтором (кадр/с).</span><span class="sxs-lookup"><span data-stu-id="c3046-164">The main metric for measuring the performance of any animation is frames per second \(FPS\).</span></span>  <span data-ttu-id="c3046-165">Пользователи будут рады, что анимации работают в 60 кадр/с.</span><span class="sxs-lookup"><span data-stu-id="c3046-165">Users are happy when animations run at 60 FPS.</span></span>  

1.  <span data-ttu-id="c3046-166">Посмотрите на диаграмму в **кадре** .</span><span class="sxs-lookup"><span data-stu-id="c3046-166">Look at the **FPS** chart.</span></span>  <span data-ttu-id="c3046-167">Если вы видите красную полосу над **кадром кадров**, это означает, что частота кадров, отброшенных таким образом, что она может повредить взаимодействие с пользователем.</span><span class="sxs-lookup"><span data-stu-id="c3046-167">Whenever you see a red bar above **FPS**, it means that the framerate dropped so low that it is probably harming the user experience.</span></span>  <span data-ttu-id="c3046-168">Как правило, чем больше зеленая полоса, тем выше кадр кадров.</span><span class="sxs-lookup"><span data-stu-id="c3046-168">In general, the higher the green bar, the higher the FPS.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-fps-chart.msft.png" alt-text="Демонстрация слева и DevTools справа" lightbox="../media/evaluate-performance-performance-fps-chart.msft.png":::
       <span data-ttu-id="c3046-170">Диаграмма **кадр/** с</span><span class="sxs-lookup"><span data-stu-id="c3046-170">The **FPS** chart</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c3046-171">Под диаграммой с **кадром кадров** вы видите диаграмму **ЦП** .</span><span class="sxs-lookup"><span data-stu-id="c3046-171">Below the **FPS** chart you see the **CPU** chart.</span></span>  <span data-ttu-id="c3046-172">Цвета на диаграмме **ЦП** соответствуют цветам на вкладке " **Сводка** " в нижней части панели "производительность".</span><span class="sxs-lookup"><span data-stu-id="c3046-172">The colors in the **CPU** chart correspond to the colors in the **Summary** tab, at the bottom of the Performance panel.</span></span>  <span data-ttu-id="c3046-173">Тот факт, что диаграмма **ЦП** заполнена цветом, означает, что ЦП был maxed во время записи.</span><span class="sxs-lookup"><span data-stu-id="c3046-173">The fact that the **CPU** chart is full of color means that the CPU was maxed out during the recording.</span></span>  <span data-ttu-id="c3046-174">Всякий раз, когда вы видите maxed ЦП в течение длительного времени, это подсказка для поиска способов уменьшения объема работы.</span><span class="sxs-lookup"><span data-stu-id="c3046-174">Whenever you see the CPU maxed out for long periods, it is a cue to find ways to do less work.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-cpu-chart.msft.png" alt-text="Демонстрация слева и DevTools справа" lightbox="../media/evaluate-performance-performance-cpu-chart.msft.png":::
       <span data-ttu-id="c3046-176">Вкладка "Диаграмма **ЦП** " и " **Сводка** "</span><span class="sxs-lookup"><span data-stu-id="c3046-176">The **CPU** chart and **Summary** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c3046-177">Наведите указатель мыши на диаграммы **кадров**, **ЦП**или **нетто** .</span><span class="sxs-lookup"><span data-stu-id="c3046-177">Hover on the **FPS**, **CPU**, or **NET** charts.</span></span>  <span data-ttu-id="c3046-178">В DevTools показан снимок страницы на данный момент времени.</span><span class="sxs-lookup"><span data-stu-id="c3046-178">DevTools shows a screenshot of the page at that point in time.</span></span>  <span data-ttu-id="c3046-179">Чтобы воспроизвести запись, передвиньте указатель влево и вправо.</span><span class="sxs-lookup"><span data-stu-id="c3046-179">Move your mouse left and right to replay the recording.</span></span>  <span data-ttu-id="c3046-180">Действие, на которое указывает ссылка, используется как элемент очистки, и его можно использовать для анализа хода анимации вручную.</span><span class="sxs-lookup"><span data-stu-id="c3046-180">The action is referenced as scrubbing, and it is useful for manually analyzing the progression of animations.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-screenshot-hover.msft.png" alt-text="Демонстрация слева и DevTools справа" lightbox="../media/evaluate-performance-performance-screenshot-hover.msft.png":::
       <span data-ttu-id="c3046-182">Просмотр снимка страницы в 2500ms отметке записи</span><span class="sxs-lookup"><span data-stu-id="c3046-182">View a screenshot of the page around the 2500ms mark of the recording</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c3046-183">В разделе **кадры** наведите указатель мыши на один из зеленых квадратиков.</span><span class="sxs-lookup"><span data-stu-id="c3046-183">In the **Frames** section, hover on one of the green squares.</span></span>  <span data-ttu-id="c3046-184">DevTools показывает, что этот конкретный кадр находится в кадре/сек.</span><span class="sxs-lookup"><span data-stu-id="c3046-184">DevTools shows you the FPS for that particular frame.</span></span>  <span data-ttu-id="c3046-185">Скорее всего, каждый кадр расположен ниже целевого числа 60 кадр/с.</span><span class="sxs-lookup"><span data-stu-id="c3046-185">Each frame is probably well below the target of 60 FPS.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-frame-hover.msft.png" alt-text="Демонстрация слева и DevTools справа" lightbox="../media/evaluate-performance-performance-frame-hover.msft.png":::
       <span data-ttu-id="c3046-187">Наведение указателя мыши на рамку</span><span class="sxs-lookup"><span data-stu-id="c3046-187">Hover on a frame</span></span>  
    :::image-end:::  
    
<span data-ttu-id="c3046-188">Разумеется, вы увидите, что страница не работает должным образом.</span><span class="sxs-lookup"><span data-stu-id="c3046-188">Of course, you should see that the page is not performing well.</span></span>  <span data-ttu-id="c3046-189">Но в реальных сценариях это может быть не так понятно, так что все средства, позволяющие делать измерения, будут полезны.</span><span class="sxs-lookup"><span data-stu-id="c3046-189">But in real scenarios, it may not be so clear, so having all of the tools to make measurements comes in handy.</span></span>  

#### <span data-ttu-id="c3046-190">Премия: открытие индикатора кадров</span><span class="sxs-lookup"><span data-stu-id="c3046-190">Bonus: Open the FPS meter</span></span>  

<span data-ttu-id="c3046-191">Еще одним удобным инструментом является индикатор между КАДРами, который обеспечивает оценки в реальном времени при выполнении страницы.</span><span class="sxs-lookup"><span data-stu-id="c3046-191">Another handy tool is the FPS meter, which provides real-time estimates for FPS as the page runs.</span></span>  

1.  <span data-ttu-id="c3046-192">Выберите `Control` + `Shift` + `P` \ (Windows, Linux \) или `Command` + `Shift` + `P` \ (macOS \), чтобы открыть **меню команд**.</span><span class="sxs-lookup"><span data-stu-id="c3046-192">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
1.  <span data-ttu-id="c3046-193">Начните вводить текст `Rendering` в **меню команд** и выберите пункт **Показать отрисовку**.</span><span class="sxs-lookup"><span data-stu-id="c3046-193">Start typing `Rendering` in the **Command Menu** and choose **Show Rendering**.</span></span>  
1.  <span data-ttu-id="c3046-194">На вкладке " **рендеринг** " Включите **индикатор кадров**.</span><span class="sxs-lookup"><span data-stu-id="c3046-194">In the **Rendering** tab, enable **FPS Meter**.</span></span>  <span data-ttu-id="c3046-195">В правом верхнем углу окна просмотра появится новая наложение.</span><span class="sxs-lookup"><span data-stu-id="c3046-195">A new overlay appears in the top-right of your viewport.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-fps-meter-overlay.msft.png" alt-text="Демонстрация слева и DevTools справа" lightbox="../media/evaluate-performance-fps-meter-overlay.msft.png":::
       <span data-ttu-id="c3046-197">**Индикатор кадров в кадре**</span><span class="sxs-lookup"><span data-stu-id="c3046-197">The **FPS meter**</span></span>  
        :::image-end:::  
    
1.  <span data-ttu-id="c3046-198">Отключите **индикатор кадров** и щелкните `Escape` , чтобы закрыть вкладку **Отображение** .  В этом учебнике не используется **индикатор в кадре** .</span><span class="sxs-lookup"><span data-stu-id="c3046-198">Disable the **FPS Meter** and select `Escape` to close the **Rendering** tab.  You are not using **FPS Meter** in this tutorial.</span></span>  
    
### <span data-ttu-id="c3046-199">Определение узкого места</span><span class="sxs-lookup"><span data-stu-id="c3046-199">Find the bottleneck</span></span>  

<span data-ttu-id="c3046-200">После того как вы зайдете и проверите, что анимация не работает, следующий шаг — ответить на вопрос "Зачем?".</span><span class="sxs-lookup"><span data-stu-id="c3046-200">After you measured and verified that the animation is not performing well, the next step is to answer the question "why?".</span></span>  

1.  <span data-ttu-id="c3046-201">Если не выбрано ни одного события, на вкладке **Сводка** показана разбивка действий.</span><span class="sxs-lookup"><span data-stu-id="c3046-201">When no events are selected, the **Summary** tab shows you a breakdown of activity.</span></span>  <span data-ttu-id="c3046-202">Страница потратила большую часть времени на отрисовку.</span><span class="sxs-lookup"><span data-stu-id="c3046-202">The page spent most of the time rendering.</span></span>  <span data-ttu-id="c3046-203">Так как производительность — это изображение, которое уменьшает трудозатраты, цель состоит в том, чтобы уменьшить время, затраченное на обработку результатов.</span><span class="sxs-lookup"><span data-stu-id="c3046-203">Since performance is the art of doing less work, your goal is to reduce the amount of time spent doing rendering work.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-summary-tab.msft.png" alt-text="Демонстрация слева и DevTools справа" lightbox="../media/evaluate-performance-performance-summary-tab.msft.png":::
       <span data-ttu-id="c3046-205">Вкладка " **Сводка** "</span><span class="sxs-lookup"><span data-stu-id="c3046-205">The **Summary** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c3046-206">Разверните раздел **основной** .</span><span class="sxs-lookup"><span data-stu-id="c3046-206">Expand the **Main** section.</span></span>  <span data-ttu-id="c3046-207">DevTools показывает flameную диаграмму активности в главном потоке с течением времени.</span><span class="sxs-lookup"><span data-stu-id="c3046-207">DevTools shows you a flame chart of activity on the main thread, over time.</span></span>  <span data-ttu-id="c3046-208">С течением времени ось x представляет запись.</span><span class="sxs-lookup"><span data-stu-id="c3046-208">The x-axis represents the recording, over time.</span></span>  <span data-ttu-id="c3046-209">Каждая строка представляет событие.</span><span class="sxs-lookup"><span data-stu-id="c3046-209">Each bar represents an event.</span></span>  <span data-ttu-id="c3046-210">Более широкий отрезок означает, что событие занимает больше времени.</span><span class="sxs-lookup"><span data-stu-id="c3046-210">A wider bar means that event took longer.</span></span>  <span data-ttu-id="c3046-211">Ось y представляет стек вызова.</span><span class="sxs-lookup"><span data-stu-id="c3046-211">The y-axis represents the call stack.</span></span>  <span data-ttu-id="c3046-212">Если вы видите события, наложенные друг на друга, это означает, что события верхнего уровня приводили к появлению младших событий.</span><span class="sxs-lookup"><span data-stu-id="c3046-212">When you see events stacked on top of each other, it means the upper events caused the lower events.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-main.msft.png" alt-text="Демонстрация слева и DevTools справа" lightbox="../media/evaluate-performance-performance-main.msft.png":::
       <span data-ttu-id="c3046-214">**Основной** раздел</span><span class="sxs-lookup"><span data-stu-id="c3046-214">The **Main** section</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c3046-215">В записи много данных.</span><span class="sxs-lookup"><span data-stu-id="c3046-215">There is a lot of data in the recording.</span></span>  <span data-ttu-id="c3046-216">Изменение масштаба одного события; Выберите, удерживайте и наведите указатель мыши на **Обзор**, который включает в себя раздел с диаграммами в **кадрах**, **ЦП**и **сети** .</span><span class="sxs-lookup"><span data-stu-id="c3046-216">To Zoom into a single event; choose, hold, and dragg your cursor over the **Overview**, which is the section that includes the **FPS**, **CPU**, and **NET** charts.</span></span>  <span data-ttu-id="c3046-217">В **главном** разделе и на вкладке " **Сводка** " отображаются только сведения о выбранной части записи.</span><span class="sxs-lookup"><span data-stu-id="c3046-217">The **Main** section and **Summary** tab only display information for the selected portion of the recording.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-main-zoomed.msft.png" alt-text="Демонстрация слева и DevTools справа" lightbox="../media/evaluate-performance-performance-main-zoomed.msft.png":::
       <span data-ttu-id="c3046-219">Изменение размера события</span><span class="sxs-lookup"><span data-stu-id="c3046-219">Zoom into an event</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="c3046-220">Кроме того, можно изменить масштаб, сосредоточиться на **главном** разделе, выбрать фоновый рисунок или событие, а затем выбрать `W` , `A` , `S` или `D` .</span><span class="sxs-lookup"><span data-stu-id="c3046-220">Another way to zoom, focus the **Main** section, choose the background or an event, and select `W`, `A`, `S`, or `D`.</span></span>  
    
    1.  <span data-ttu-id="c3046-221">Сосредоточьтесь на красном треугольнике в правой верхней части события **анимации Frame, которое активировалось** .</span><span class="sxs-lookup"><span data-stu-id="c3046-221">Focus on the red triangle in the top-right of the **Animation Frame Fired** event.</span></span>  <span data-ttu-id="c3046-222">Если вы видите красный треугольник, это предупреждение может быть связано с проблемой, связанной с событием.</span><span class="sxs-lookup"><span data-stu-id="c3046-222">Whenever you see a red triangle, it is a warning that there may be an issue related to the event.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="c3046-223">Событие **анимации Frame срабатывает** при каждом запуске [ `requestAnimationFrame()` обратного вызова][MDNWebRequestAnimationFrame] .</span><span class="sxs-lookup"><span data-stu-id="c3046-223">The **Animation Frame Fired** event occurs whenever a [`requestAnimationFrame()` callback][MDNWebRequestAnimationFrame] is run.</span></span>  
    
1.  <span data-ttu-id="c3046-224">Выберите событие **кадр анимации, которое активировалось** .</span><span class="sxs-lookup"><span data-stu-id="c3046-224">Choose the **Animation Frame Fired** event.</span></span>  <span data-ttu-id="c3046-225">На вкладке **Сводка** теперь отображаются сведения об этом событии.</span><span class="sxs-lookup"><span data-stu-id="c3046-225">The **Summary** tab now shows you information about that event.</span></span>  <span data-ttu-id="c3046-226">Обратите внимание на ссылку " **Показать** ".</span><span class="sxs-lookup"><span data-stu-id="c3046-226">Note the **Reveal** link.</span></span>  <span data-ttu-id="c3046-227">После того как вы выберете его, DevTools выделит событие, которое инициировало событие **кадра анимации** .</span><span class="sxs-lookup"><span data-stu-id="c3046-227">After you choose it, DevTools to highlights the event that initiated the **Animation Frame Fired** event.</span></span>  <span data-ttu-id="c3046-228">Кроме того, обратите внимание на ссылку **app.js:95** .</span><span class="sxs-lookup"><span data-stu-id="c3046-228">Also, focus on the **app.js:95** link.</span></span>  <span data-ttu-id="c3046-229">После того как вы выберете его, отобразится соответствующая строка исходного кода.</span><span class="sxs-lookup"><span data-stu-id="c3046-229">After you choose it, the relevant line in the source code is displayed.</span></span>
    
    :::image type="complex" source="../media/evaluate-performance-performance-animation-frame-fired.msft.png" alt-text="Демонстрация слева и DevTools справа" lightbox="../media/evaluate-performance-performance-animation-frame-fired.msft.png":::
       <span data-ttu-id="c3046-231">Дополнительные сведения о событии **анимации запускаемого кадра**</span><span class="sxs-lookup"><span data-stu-id="c3046-231">More information about the **Animation Frame Fired** event</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="c3046-232">После выбора события с помощью клавиш со стрелками выберите события рядом с ним.</span><span class="sxs-lookup"><span data-stu-id="c3046-232">After selecting an event, use the arrow keys to select the events next to it.</span></span>  
    
1.  <span data-ttu-id="c3046-233">В рамках события **app. Update** существует множество фиолетовых событий.</span><span class="sxs-lookup"><span data-stu-id="c3046-233">Under the **app.update** event, there is a bunch of purple events.</span></span>  <span data-ttu-id="c3046-234">Если каждое фиолетовое событие было расширено, оно выглядит так, как будто каждый из них может иметь красный треугольник.</span><span class="sxs-lookup"><span data-stu-id="c3046-234">If each purple event was wider, it looks as though each one may have a red triangle on it.</span></span>  
1.  <span data-ttu-id="c3046-235">Выберите одно из фиолетовых событий **макета** .</span><span class="sxs-lookup"><span data-stu-id="c3046-235">Choose one of the purple **Layout** events.</span></span>  <span data-ttu-id="c3046-236">DevTools предоставляет дополнительные сведения о событии на вкладке " **Сводка** ".  В действительности есть предупреждение о принудительном передвижении \ (другое слово для макета \).</span><span class="sxs-lookup"><span data-stu-id="c3046-236">DevTools provides more information about the event in the **Summary** tab.  Indeed, there is a warning about forced reflows \(another word for layout\).</span></span>  
    
1.  <span data-ttu-id="c3046-237">На вкладке **Сводка** щелкните ссылку **app.js:71** в разделе **Макет принудительно**.</span><span class="sxs-lookup"><span data-stu-id="c3046-237">In the **Summary** tab, choose the **app.js:71** link under **Layout Forced**.</span></span>  <span data-ttu-id="c3046-238">DevTools перенесет вас в строку кода, которая замещает макет.</span><span class="sxs-lookup"><span data-stu-id="c3046-238">DevTools takes you to the line of code that forced the layout.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-sources-app-update.msft.png" alt-text="Демонстрация слева и DevTools справа" lightbox="../media/evaluate-performance-sources-app-update.msft.png":::
       <span data-ttu-id="c3046-240">Строка кода, вызвавшая принудительный макет.</span><span class="sxs-lookup"><span data-stu-id="c3046-240">The line of code that caused the forced layout</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="c3046-241">Проблема с кодом состоит в том, что в каждом кадре анимации каждый из них изменяет стиль каждого значка, а затем запрашивает расположение каждого значка на странице.</span><span class="sxs-lookup"><span data-stu-id="c3046-241">The problem with the code is that, in each animation frame, it changes the style for each icon, and then queries the position of each icon on the page.</span></span>  <span data-ttu-id="c3046-242">Поскольку стили изменились, браузер не может определить, изменилось ли положение каждого значка, поэтому для вычисления нового положения необходимо изменить макет значка.</span><span class="sxs-lookup"><span data-stu-id="c3046-242">Because the styles changed, the browser does not know if each icon position changed, so it has to re-layout the icon in order to compute the new position.</span></span>  <!--  > See [Avoid forced synchronous layouts][RenderingAvoidSynchronousLayouts] to learn more.  -->
    
<!-- todo: add layouts section when available -->

<span data-ttu-id="c3046-243">Это было очень мало для обучения.</span><span class="sxs-lookup"><span data-stu-id="c3046-243">That was a lot to learn.</span></span>  <span data-ttu-id="c3046-244">Теперь у вас есть надежная основа базового рабочего процесса для анализа производительности среды выполнения.</span><span class="sxs-lookup"><span data-stu-id="c3046-244">You now have a solid foundation in the basic workflow for analyzing runtime performance.</span></span>  <span data-ttu-id="c3046-245">Молодец.</span><span class="sxs-lookup"><span data-stu-id="c3046-245">Good job.</span></span>  

### <span data-ttu-id="c3046-246">Премия: анализ оптимизированной версии</span><span class="sxs-lookup"><span data-stu-id="c3046-246">Bonus: Analyze the optimized version</span></span>  

<span data-ttu-id="c3046-247">Используй рабочие процессы и инструменты, которые вы только что узнали, нажмите кнопку **оптимизировать** на демонстрационной версии, чтобы включить оптимизированный код, а затем выберите другую запись и проанализируйте результаты.</span><span class="sxs-lookup"><span data-stu-id="c3046-247">Using the workflows and tools that you just learned, choose **Optimize** on the demo to enable the optimized code, take another performance recording, and then analyze the results.</span></span>  <span data-ttu-id="c3046-248">С улучшенной частотой кадров, направленной на сокращение событий в диаграмме Flame в **главном** разделе, вы можете видеть, что оптимизированная версия приложения работает гораздо меньше усилий, что повышает производительность.</span><span class="sxs-lookup"><span data-stu-id="c3046-248">From the improved framerate to the reduction in events in the flame chart in the **Main** section, you are able to see that the optimized version of the app does much less work, resulting in better performance.</span></span>  

> [!NOTE]
> <span data-ttu-id="c3046-249">Даже оптимизированная версия не имеет ничего удобного, так как она управляет `top` свойством каждого значка.</span><span class="sxs-lookup"><span data-stu-id="c3046-249">Even the optimized version is not great, because it manipulates the `top` property of every icon.</span></span>  <span data-ttu-id="c3046-250">Лучший подход — придерживаться свойств, которые влияют только на композицию.</span><span class="sxs-lookup"><span data-stu-id="c3046-250">A better approach is to stick to properties that only affect compositing.</span></span>  <!--  > See [Use transform and opacity changes for animations][RenderingCompositor] for more information.  -->  

<!--todo: add rendering section when available -->

## <span data-ttu-id="c3046-251">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="c3046-251">Next steps</span></span>

<!--The foundation for understanding performance is the RAIL model.  The RAIL model teaches you the performance metrics that are most important to your users.  
See [Measure Performance With The RAIL Model][RAIL] to learn more.  -->  

<span data-ttu-id="c3046-252">Для более удобного функционирования с помощью панели "производительность" лучше всего сделать это.</span><span class="sxs-lookup"><span data-stu-id="c3046-252">To get more comfortable with the Performance panel, practice makes perfect.</span></span>  <span data-ttu-id="c3046-253">Попробуйте выполнить профилирование страниц и проанализировать результаты.</span><span class="sxs-lookup"><span data-stu-id="c3046-253">Try profiling your pages and analyzing the results.</span></span>  <span data-ttu-id="c3046-254">Если у вас возникли вопросы по поводу ваших результатов, используйте значок **Отправить отзыв** , выберите `Alt` + `Shift` + `I` \ (Windows, Linux \), выберите `Option` + `Shift` + `I` \ (macOS \) или [твит в группу DevTools][TwitterEdgeDevtools].</span><span class="sxs-lookup"><span data-stu-id="c3046-254">If you have any questions about your results, use the **Send Feedback** icon, select `Alt`+`Shift`+`I` \(Windows, Linux\), select `Option`+`Shift`+`I` \(macOS\), or [tweet the DevTools team][TwitterEdgeDevtools].</span></span>  <span data-ttu-id="c3046-255">Включите снимки экрана или ссылки на воспроизводимые страницы, если это возможно.</span><span class="sxs-lookup"><span data-stu-id="c3046-255">Include screenshots or links to reproducible pages, if possible.</span></span>  

:::image type="complex" source="../media/evaluate-performance-feedback-icon.msft.png" alt-text="Демонстрация слева и DevTools справа" lightbox="../media/evaluate-performance-feedback-icon.msft.png":::
   <span data-ttu-id="c3046-257">Значок " **Отправить отзыв** " в Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="c3046-257">The **Send Feedback** icon in the Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!-- To really become an expert in runtime performance, you must learn how the browser translates HTML, CSS, and JS into pixels on a screen.  The best place to start is the [Rendering Performance Overview][RenderingPerformance].  [The Anatomy Of A Frame][FrameAnatomy] dives into even more detail.  -->  

<span data-ttu-id="c3046-258">Наконец, существует множество способов улучшить производительность во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="c3046-258">Last, there are many ways to improve runtime performance.</span></span>  <span data-ttu-id="c3046-259">В этой статье рассказывается о узком узким местах анимации, чтобы дать вам сфокусированный обзор на панели производительности, но это лишь один из многих узких мест.</span><span class="sxs-lookup"><span data-stu-id="c3046-259">This article focused on one particular animation bottleneck to give you a focused tour through the Performance panel, but it is only one of many bottlenecks you may encounter.</span></span>  <!--  The rest of the Rendering Performance series has a lot of good tips for improving various aspects of runtime performance, such as:  -->

<!--
*   [Optimizing JS Execution][RenderingOptimizeJS]  
*   [Reduce The Scope And Complexity Of Style Calculations][RenderingReduceScope]  
*   [Avoid Large, Complex Layouts And Layout Thrashing][RenderingAvoidThrashing]  
*   [Simplify Paint Complexity And Reduce Paint Areas][RenderingSimplifyPaint]  
*   [Stick To Compositor-Only Properties And Manage Layer Count][RenderingManageLayers]  
*   [Debounce Your Input Handlers][RenderingDebounceInputs]  
-->

## <span data-ttu-id="c3046-260">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="c3046-260">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->

[DevtoolsCustomizePlacement]: ../customize/placement.md "Изменение положения DevTools Microsoft EDGE (Отстыковка, закрепить в нижней части, закрепить слева)"  
[DevtoolsSpeedGetStarted]: ../speed/get-started.md "Оптимизация скорости веб-сайта с помощью Microsoft Edge DevTools"  

[TwitterEdgeDevtools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "EdgeDevTools-опубликовать твит | Контента"  

[MDNWebRequestAnimationFrame]: https://developer.mozilla.org/docs/Web/API/window/requestAnimationFrame "Window. requestAnimationFrame \ (\) | MDN"  

<!--[InPrivate]: https://support.microsoft.com/help/4026200/microsoft-edge-browse-inprivate "Browse InPrivate in Microsoft Edge"  -->

<!--[FrameAnatomy]: https://aerotwist.com/blog/the-anatomy-of-a-frame  -->  

<!--[RAIL]: /web/fundamentals/performance/rail  -->  
<!--[RenderingAvoidSynchronousLayouts]: /web/fundamentals/performance/rendering/avoid-large-complex-layouts-and-layout-thrashing#avoid_forced_synchronous_layouts  -->  
<!--[RenderingAvoidThrashing]: /web/fundamentals/performance/rendering/avoid-large-complex-layouts-and-layout-thrashing  -->  
<!--[RenderingCompositor]: /web/fundamentals/performance/rendering/stick-to-compositor-only-properties-and-manage-layer-count#use_transform_and_opacity_changes_for_animations  -->  
<!--[RenderingDebounceInputs]: /web/fundamentals/performance/rendering/debounce-your-input-handlers  -->
<!--[RenderingManageLayers]: /web/fundamentals/performance/rendering/stick-to-compositor-only-properties-and-manage-layer-count  -->  
<!--[RenderingOptimizeJS]: /web/fundamentals/performance/rendering/optimize-javascript-execution  -->  
<!--[RenderingPerformance]: /web/fundamentals/performance/rendering  -->  
<!--[RenderingReduceScope]: /web/fundamentals/performance/rendering/reduce-the-scope-and-complexity-of-style-calculations  -->  
<!--[RenderingSimplifyPaint]: /web/fundamentals/performance/rendering/simplify-paint-complexity-and-reduce-paint-areas  -->  

<!--[StackOverflowAlphabetBrowserDevtools]: https://stackoverflow.com/questions/ask?tags=alphabet-browser-devtools "Alphabet Browser - Stack Overflow"  -->  

> [!NOTE]
> <span data-ttu-id="c3046-265">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c3046-265">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="c3046-266">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/index) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="c3046-266">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="c3046-268">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c3046-268">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
