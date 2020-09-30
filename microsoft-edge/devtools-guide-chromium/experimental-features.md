---
description: Последние экспериментальные функции в Microsoft Edge DevTools
title: Экспериментальные функции
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools, эксперименты
ms.openlocfilehash: ae2058ad2beb2d8d3b19061e0935b92173392f23
ms.sourcegitcommit: c24884cc154d6c4809e05ae37d170cb674c408b9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/30/2020
ms.locfileid: "11091536"
---
# <span data-ttu-id="99e15-104">Экспериментальные функции</span><span class="sxs-lookup"><span data-stu-id="99e15-104">Experimental features</span></span>  

<span data-ttu-id="99e15-105">Microsoft Edge DevTools предоставляет доступ к экспериментальным функциям, которые все еще находятся на стадии разработки.</span><span class="sxs-lookup"><span data-stu-id="99e15-105">Microsoft Edge DevTools provide access to experimental features that are still in development.</span></span>  <span data-ttu-id="99e15-106">Вы можете протестировать и[отдать отзыв](#providing-feedback-on-experimental-features) , прежде чем каждый компонент будет выпущен.</span><span class="sxs-lookup"><span data-stu-id="99e15-106">You may test and p[provide feedback](#providing-feedback-on-experimental-features) before each feature is released.</span></span>  

<span data-ttu-id="99e15-107">Хотя экспериментальные функции доступны во всех каналах Microsoft EDGE, вы можете получить последние экспериментальные функции с помощью канала Microsoft Edge Канарские Channel.</span><span class="sxs-lookup"><span data-stu-id="99e15-107">While experimental features are available in all channels of Microsoft Edge, you may get the latest experimental features using the Microsoft Edge Canary channel.</span></span>  

## <span data-ttu-id="99e15-108">Включение экспериментальных функций</span><span class="sxs-lookup"><span data-stu-id="99e15-108">Turn on experimental features</span></span>  

<span data-ttu-id="99e15-109">Чтобы включить экспериментальные функции в Microsoft EDGE, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="99e15-109">Use the following steps to turn on \(or off\) experimental features in Microsoft Edge.</span></span>  

1.  <span data-ttu-id="99e15-110">[Откройте DevTools][DevtoolsOpen].</span><span class="sxs-lookup"><span data-stu-id="99e15-110">[Open DevTools][DevtoolsOpen].</span></span>  
     *   <span data-ttu-id="99e15-111">Выберите `Control` + `Shift` + `I` \ (Windows \) или `Command` + `Option` + `I` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="99e15-111">Select `Control`+`Shift`+`I` \(Windows\) or `Command`+`Option`+`I` \(macOS\).</span></span>  <span data-ttu-id="99e15-112">Дополнительные сведения можно найти в разделе [сочетания клавиш Microsoft Edge DevTools][DevToolsShortcuts].</span><span class="sxs-lookup"><span data-stu-id="99e15-112">For more information, navigate to [Microsoft Edge DevTools keyboard shortcuts][DevToolsShortcuts].</span></span>  
1.  <span data-ttu-id="99e15-113">Открытие области [параметров][DevToolsCustomizeSettings] .</span><span class="sxs-lookup"><span data-stu-id="99e15-113">Open the [Settings][DevToolsCustomizeSettings] pane.</span></span>  
    *   <span data-ttu-id="99e15-114">Выберите `Shift` + `?` .</span><span class="sxs-lookup"><span data-stu-id="99e15-114">Select `Shift`+`?`.</span></span>  <span data-ttu-id="99e15-115">Дополнительные сведения можно найти в разделе [сочетания клавиш Microsoft Edge DevTools][DevToolsShortcuts].</span><span class="sxs-lookup"><span data-stu-id="99e15-115">For more information, navigate to [Microsoft Edge DevTools keyboard shortcuts][DevToolsShortcuts].</span></span>  
1.  <span data-ttu-id="99e15-116">В левой части области **параметров** выберите раздел **эксперименты** .</span><span class="sxs-lookup"><span data-stu-id="99e15-116">On the left side of the **Settings** pane, choose the **Experiments** section.</span></span>  
    
    :::image type="complex" source="./media/experiments-devtools.msft.png" alt-text="Список экспериментов в параметрах DevTools" lightbox="./media/experiments-devtools.msft.png":::
       <span data-ttu-id="99e15-118">Список экспериментов в параметрах DevTools</span><span class="sxs-lookup"><span data-stu-id="99e15-118">List of experiments in DevTools Settings</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="99e15-119">На странице " **эксперименты** " прокрутите список всех доступных экспериментальных функций и установите флажок рядом с каждым компонентом, который нужно протестировать.</span><span class="sxs-lookup"><span data-stu-id="99e15-119">On the **Experiments** page, scroll through the list of all available experimental features and choose the checkbox next to each feature that you want to test.</span></span>  
1.  <span data-ttu-id="99e15-120">Закройте и снова откройте Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="99e15-120">Close and reopen Microsoft Edge DevTools.</span></span>  

> [!NOTE]
> <span data-ttu-id="99e15-121">Экспериментальные функции постоянно обновляются и могут привести к проблемам с производительностью.</span><span class="sxs-lookup"><span data-stu-id="99e15-121">Experimental features are constantly being updated and may cause performance issues.</span></span>  <span data-ttu-id="99e15-122">Чтобы отключить экспериментальную функцию, откройте страницу **эксперименты** и снимите флажок экспериментальной функции, которую вы хотите отключить.</span><span class="sxs-lookup"><span data-stu-id="99e15-122">To turn off an experimental feature, open the **Experiments** page and clear the checkbox of the experimental feature that you want to turn off.</span></span>  

## <span data-ttu-id="99e15-123">Выделены экспериментальные функции</span><span class="sxs-lookup"><span data-stu-id="99e15-123">Highlighted experimental features</span></span>  

<span data-ttu-id="99e15-124">В следующих разделах описаны новые экспериментальные функции, доступные в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="99e15-124">The following sections describe the new experimental features that are available in Microsoft Edge.</span></span>  

| <span data-ttu-id="99e15-125">Экспериментальная функция</span><span class="sxs-lookup"><span data-stu-id="99e15-125">Experimental feature</span></span> | <span data-ttu-id="99e15-126">Версия Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="99e15-126">Microsoft Edge version</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="99e15-127">Эмуляция: поддержка двух режимов экрана</span><span class="sxs-lookup"><span data-stu-id="99e15-127">Emulation: Support dual screen mode</span></span>](#emulation-support-dual-screen-mode) | <span data-ttu-id="99e15-128">84 или более поздняя версия</span><span class="sxs-lookup"><span data-stu-id="99e15-128">84 or later</span></span> |  
| [<span data-ttu-id="99e15-129">Включение новых функций отладки CSS Grid</span><span class="sxs-lookup"><span data-stu-id="99e15-129">Enable new CSS grid debugging features</span></span>](#enable-new-css-grid-debugging-features) | <span data-ttu-id="99e15-130">85 или более поздняя версия</span><span class="sxs-lookup"><span data-stu-id="99e15-130">85 or later</span></span> |  
| [<span data-ttu-id="99e15-131">Включение поддержки перемещения вкладок между панелями</span><span class="sxs-lookup"><span data-stu-id="99e15-131">Enable support to move tabs between panels</span></span>](#enable-support-to-move-tabs-between-panels) | <span data-ttu-id="99e15-132">85 или более поздняя версия</span><span class="sxs-lookup"><span data-stu-id="99e15-132">85 or later</span></span> |  
| [<span data-ttu-id="99e15-133">Включить подсказку</span><span class="sxs-lookup"><span data-stu-id="99e15-133">Enable webhint</span></span>](#enable-webhint) | <span data-ttu-id="99e15-134">85 или более поздняя версия</span><span class="sxs-lookup"><span data-stu-id="99e15-134">85 or later</span></span> |  
| [<span data-ttu-id="99e15-135">Включение сетевой консоли</span><span class="sxs-lookup"><span data-stu-id="99e15-135">Enable Network Console</span></span>](#enable-network-console) | <span data-ttu-id="99e15-136">85 или более поздняя версия</span><span class="sxs-lookup"><span data-stu-id="99e15-136">85 or later</span></span> |  
| [<span data-ttu-id="99e15-137">Средство просмотра исходного порядка</span><span class="sxs-lookup"><span data-stu-id="99e15-137">Source Order Viewer</span></span>](#source-order-viewer) | <span data-ttu-id="99e15-138">86 или более поздняя версия</span><span class="sxs-lookup"><span data-stu-id="99e15-138">86 or later</span></span> |  

### <span data-ttu-id="99e15-139">Эмуляция: поддержка двух режимов экрана</span><span class="sxs-lookup"><span data-stu-id="99e15-139">Emulation: Support dual screen mode</span></span>  

<span data-ttu-id="99e15-140">Предоставляет дополнительные функции для эмуляции двух новых двух экранов и устройств складная в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="99e15-140">Provides additional features for emulating two new dual-screen and foldable devices in Microsoft Edge.</span></span>  

*   [<span data-ttu-id="99e15-141">Surface Duo</span><span class="sxs-lookup"><span data-stu-id="99e15-141">Surface Duo</span></span>][SurfaceDevicesDuo]  
*   [<span data-ttu-id="99e15-142">Samsung Galaxy сгиб</span><span class="sxs-lookup"><span data-stu-id="99e15-142">Samsung Galaxy Fold</span></span>][SamsungMobileGalaxyFold]  

<span data-ttu-id="99e15-143">Эмулирует устройства и переключаться между следующими элементами.</span><span class="sxs-lookup"><span data-stu-id="99e15-143">Emulate the devices and toggle between the following postures.</span></span>  

*   <span data-ttu-id="99e15-144">режим с одним экраном или сложением</span><span class="sxs-lookup"><span data-stu-id="99e15-144">single-screen or folded posture</span></span>  
*   <span data-ttu-id="99e15-145">возможность установки на два экрана или несложенный</span><span class="sxs-lookup"><span data-stu-id="99e15-145">dual-screen or unfolded posture</span></span>  
    
<span data-ttu-id="99e15-146">[Включите экспериментальные API веб-платформ](#enable-experimental-apis) и используйте [функцию многоэкранной][DualScreenDocsCssMedia] группировки с экрана CSS и [API JavaScript getWindowSegments][DualScreenDocsJSAPI] для расширения вашего веб-сайта (или приложения) на двойном экране и на складная устройствах.</span><span class="sxs-lookup"><span data-stu-id="99e15-146">[Enable experimental Web Platform APIs](#enable-experimental-apis) and use the [CSS media screen-spanning feature][DualScreenDocsCssMedia] and [JavaScript getWindowSegments API][DualScreenDocsJSAPI] to enhance your website \(or app\) for dual-screen and foldable devices.</span></span>  

:::image type="complex" source="./media/experiments-surface-duo-emulation.msft.png" alt-text="Список экспериментов в параметрах DevTools" lightbox="./media/experiments-surface-duo-emulation.msft.png":::  
   <span data-ttu-id="99e15-148">Эмуляция Surface Duo в Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="99e15-148">Emulate Surface Duo in Microsoft Edge</span></span>  
:::image-end:::  

#### <span data-ttu-id="99e15-149">Включение экспериментальных API</span><span class="sxs-lookup"><span data-stu-id="99e15-149">Enable experimental APIs</span></span>  

<span data-ttu-id="99e15-150">Чтобы использовать [функцию многоэкранной области экрана CSS][DualScreenDocsCssMedia] и [API JavaScript getWindowSegments][DualScreenDocsJSAPI], включите `Experimental Web Platform features` флажок в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="99e15-150">To use the [CSS media screen-spanning feature][DualScreenDocsCssMedia] and [JavaScript getWindowSegments API][DualScreenDocsJSAPI], turn on the `Experimental Web Platform features` flag in Microsoft Edge.</span></span>  <span data-ttu-id="99e15-151">Выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="99e15-151">Complete the following steps.</span></span>  

1.  <span data-ttu-id="99e15-152">Перейдите к `edge://flags` .</span><span class="sxs-lookup"><span data-stu-id="99e15-152">Navigate to `edge://flags`.</span></span>  
1.  <span data-ttu-id="99e15-153">В текстовом поле **Флаги поиска** введите `Experimental Web Platform features` , выберите " **экспериментальные компоненты веб-платформы** ", а затем **Enabled**— " **Отключить** ".</span><span class="sxs-lookup"><span data-stu-id="99e15-153">In the **Search flags** textbox, enter `Experimental Web Platform features`, choose the **Experimental Web Platform features** flag, and change **Disabled** to **Enabled**.</span></span>  
1.  <span data-ttu-id="99e15-154">Перезапустите Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="99e15-154">Restart Microsoft Edge.</span></span>  

:::image type="complex" source="./media/experiments-dual-screen-emulation-edge-flags.msft.png" alt-text="Список экспериментов в параметрах DevTools" lightbox="./media/experiments-dual-screen-emulation.msft.png":::
   <span data-ttu-id="99e15-156">Флажок включения функций экспериментальной веб-платформы</span><span class="sxs-lookup"><span data-stu-id="99e15-156">Enable the Experimental Web Platform features flag</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="99e15-157">Если вы используете запросы на поиск [мультимедиа в каскадных таблицах][DualScreenDocsCssMedia] или [API-интерфейс перечисления сегмента Windows (JavaScript][DualScreenDocsJSAPI] ) для повышения качества сайта или приложения для служб [Surface Duo][SurfaceDevicesDuo], необходимо также включить флажок **экспериментальные возможности веб-платформы** в [приложении Android Microsoft Edge][GooglePlayMicrosoftEdge] на устройстве [Surface Duo][SurfaceDevicesDuo] .</span><span class="sxs-lookup"><span data-stu-id="99e15-157">If you are using [CSS media queries][DualScreenDocsCssMedia] or the [JavaScript Windows Segment Enumeration API][DualScreenDocsJSAPI] to enhance your website or app for the [Surface Duo][SurfaceDevicesDuo], you must also enable the **Experimental Web Platform features** flag in the [Android Microsoft Edge app][GooglePlayMicrosoftEdge] on your [Surface Duo][SurfaceDevicesDuo] device.</span></span>  
> 
> <span data-ttu-id="99e15-158">Если флажок **"экспериментальные веб-платформа** " включен [в классическом приложении Microsoft][MicrosoftEdge] EDGE и отключен для [приложения Android (Microsoft Edge][GooglePlayMicrosoftEdge]), поведение вашего веб-сайта или приложения в эмуляторе Duo Surface в классическом приложении Microsoft EDGE не совпадает с [приложением Android Microsoft][GooglePlayMicrosoftEdge] EDGE на [Surface Duo][SurfaceDevicesDuo].</span><span class="sxs-lookup"><span data-stu-id="99e15-158">If the **Experimental Web Platform features** flag is enabled in [desktop Microsoft Edge][MicrosoftEdge] and disabled in the [Android Microsoft Edge app][GooglePlayMicrosoftEdge], the behavior of your website or app in the Surface Duo emulator in desktop Microsoft Edge does not match with the [Android Microsoft Edge app][GooglePlayMicrosoftEdge] on [Surface Duo][SurfaceDevicesDuo].</span></span>  <span data-ttu-id="99e15-159">Убедитесь в том, что для устройств Android и Desktop Microsoft Edge успешно используются Эмуляторы Surface Duo в классической платформе [Microsoft Edge][MicrosoftEdge].</span><span class="sxs-lookup"><span data-stu-id="99e15-159">Ensure that the flags are matching across Android and desktop Microsoft Edge to successfully use the Surface Duo emulator in [desktop Microsoft Edge][MicrosoftEdge].</span></span>  

#### <span data-ttu-id="99e15-160">Тестирование на устройствах складная и на двух экранах</span><span class="sxs-lookup"><span data-stu-id="99e15-160">Testing on foldable and dual-screen devices</span></span>  

<span data-ttu-id="99e15-161">При эмуляции [Duo Surface][SurfaceDevicesDuo] в Microsoft Edge с двумя экранами на экране добавляется стык \ (расстояние между двумя экранами), нарисованный на веб-сайте или в приложении.</span><span class="sxs-lookup"><span data-stu-id="99e15-161">When you emulate the [Surface Duo][SurfaceDevicesDuo] in a dual-screen posture in Microsoft Edge, the seam \(the space between the two screens\) is drawn over your website or app.</span></span>  

<span data-ttu-id="99e15-162">Эмуляция дисплея соответствует способу обработки веб-сайта \ (или приложения \) в [приложении Microsoft Edge][GooglePlayMicrosoftEdge] на платформе [Surface Duo][SurfaceDevicesDuo].</span><span class="sxs-lookup"><span data-stu-id="99e15-162">The emulated display matches the way your website \(or app\) renders in the [Microsoft Edge Android app][GooglePlayMicrosoftEdge] on [Surface Duo][SurfaceDevicesDuo].</span></span>  <span data-ttu-id="99e15-163">Возможно, вам потребуется обновить ваш веб-сайт \ (или приложение \), чтобы он лучше отображался на стыке.</span><span class="sxs-lookup"><span data-stu-id="99e15-163">You may have to update your website \(or app\) to display better along the seam.</span></span>  <span data-ttu-id="99e15-164">Для получения дополнительных сведений о адаптации веб-сайта к стыку (или внешнему приложению) перейдите к разделу [Работа с стыком][DualScreenIntroductionHowWorkSeam] в документации Surface Duo.</span><span class="sxs-lookup"><span data-stu-id="99e15-164">For more information about adapting your website \(or app\) to the seam, navigate to [How to work with the seam][DualScreenIntroductionHowWorkSeam] in the Surface Duo documentation.</span></span>  

<span data-ttu-id="99e15-165">На [панели инструментов устройства][DevtoolsDeviceModeIndexSimulateMobileViewport] есть дополнительные функции, с помощью которых можно протестировать веб-сайт или приложение в нескольких элементах управления и ориентации.</span><span class="sxs-lookup"><span data-stu-id="99e15-165">The [Device Toolbar][DevtoolsDeviceModeIndexSimulateMobileViewport] has additional features to help you test your website or app in multiple postures and orientations.</span></span>  <span data-ttu-id="99e15-166">**Rotate** ![ ][ImageRotateIcon] Чтобы повернуть окно просмотра на альбомную ориентацию, нажмите поворот на (повернуть).</span><span class="sxs-lookup"><span data-stu-id="99e15-166">Choose **Rotate** \(![Rotate][ImageRotateIcon]\) to rotate the viewport to landscape orientation.</span></span> <span data-ttu-id="99e15-167">Объедините функцию с **диапазоном** \ ( ![ Span ][ImageSpanIcon] \), чтобы переключаться между одним экраном или сложением, а также с двойным экраном или без сгиба.</span><span class="sxs-lookup"><span data-stu-id="99e15-167">Combine the feature with **Span** \(![Span][ImageSpanIcon]\) to toggle between single-screen or folded and dual-screen or unfolded postures.</span></span>  <span data-ttu-id="99e15-168">Вместе функции позволяют тестировать ваш веб-сайт или приложение во всех четырех возможностях и ориентациях.</span><span class="sxs-lookup"><span data-stu-id="99e15-168">Together, the features enable testing your website or app in all four possible postures and orientations.</span></span>  

:::image type="complex" source="./media/experiments-dual-screen-emulation-rotate-span.msft.png" alt-text="Список экспериментов в параметрах DevTools" lightbox="./media/experiments-dual-screen-emulation-rotate-span.msft.png":::
   <span data-ttu-id="99e15-170">Матрица геоуровней и ориентации для двухпроцессорных и складная устройств</span><span class="sxs-lookup"><span data-stu-id="99e15-170">Matrix of postures and orientations for dual-screen and foldable devices</span></span>  
:::image-end:::  

<span data-ttu-id="99e15-171">Значок " **экспериментальные веб-платформы** " \ ( ![ ExperimentalApis ][ImageExperimentalApisIcon] \) отображает состояние флага " **экспериментальные веб-платформы** ".</span><span class="sxs-lookup"><span data-stu-id="99e15-171">The **Experimental Web Platform features** \(![ExperimentalApis][ImageExperimentalApisIcon]\) icon displays the state of the **Experimental Web Platform features** flag.</span></span>  <span data-ttu-id="99e15-172">Если пометка включена, значок выделена.</span><span class="sxs-lookup"><span data-stu-id="99e15-172">If the flag is turned on, the icon is highlighted.</span></span>  <span data-ttu-id="99e15-173">Если флажок выключен, значок не выделяется.</span><span class="sxs-lookup"><span data-stu-id="99e15-173">If the flag is turned off, the icon is not highlighted.</span></span>  <span data-ttu-id="99e15-174">Чтобы включить параметр \ (или выключить), найдите `edge://flags` и переключите флажок.</span><span class="sxs-lookup"><span data-stu-id="99e15-174">To turn on \(or off\) the flag, navigate to `edge://flags` and toggle the flag.</span></span>  

<!-- Commenting out until the icon issue is fixed in Edge Canary
The **Experimental Web Platform features** \(![ExperimentalApis][ImageExperimentalApisIcon]\) icon displays the state of the **Experimental Web Platform features** flag.  If the flag is turned on, the icon is highlighted.  If the flag is turned off, the icon is not highlighted.  To turn on \(or off\) the flag, either choose the icon or navigate to `edge://flags` and toggle the flag.   -->  

<span data-ttu-id="99e15-175">Ниже приведены дополнительные ресурсы, которые помогут вам повысить качество вашего веб-сайта (или приложения) на устройствах с двумя экранами.</span><span class="sxs-lookup"><span data-stu-id="99e15-175">Here are additional resources that may help you enhance your website \(or app\) for dual-screen devices:</span></span>
*   <span data-ttu-id="99e15-176">Дополнительные сведения о веб-разработке на устройствах с двумя экранами можно найти на [веб-сайте с двумя экранами][DualScreenWebIndex].</span><span class="sxs-lookup"><span data-stu-id="99e15-176">For more information about web development on dual-screen devices, navigate to [Dual-screen web experiences][DualScreenWebIndex].</span></span>  
*   <span data-ttu-id="99e15-177">Установите [эмулятор Surface Duo][DualScreenAndroidUseEmulator].</span><span class="sxs-lookup"><span data-stu-id="99e15-177">Install the [Surface Duo emulator][DualScreenAndroidUseEmulator].</span></span>  <span data-ttu-id="99e15-178">Он отличается от эмулятора в Microsoft EDGE, эмулирует центр Surface Duo с Android и интегрируется с [Android][AndroidDeveloperStudio].</span><span class="sxs-lookup"><span data-stu-id="99e15-178">It is different from the emulator in Microsoft Edge, emulates the Surface Duo running Android, and integrates with [Android Studio][AndroidDeveloperStudio].</span></span>  <span data-ttu-id="99e15-179">Дополнительные сведения можно найти в [пакете SDK Surface Duo][DualScreenAndroidGetDuoSdk].</span><span class="sxs-lookup"><span data-stu-id="99e15-179">For more information, navigate to [Get the Surface Duo SDK][DualScreenAndroidGetDuoSdk].</span></span>  

> [!NOTE]
> <span data-ttu-id="99e15-180">Ниже приведен список текущих известных проблем.</span><span class="sxs-lookup"><span data-stu-id="99e15-180">The following is a list of current known issues.</span></span>  
> 
> *   <span data-ttu-id="99e15-181">При использовании [клиента удаленного рабочего стола Microsoft][RemoteDesktopClientDocs] для подключения к удаленному компьютеру и эмуляции [Galaxyого сгиба][SamsungMobileGalaxyFold] [Surface Duo][SurfaceDevicesDuo] или Samsung, указатель может стабилизации видеоизображения или перебоям.</span><span class="sxs-lookup"><span data-stu-id="99e15-181">When using a [Microsoft Remote Desktop client][RemoteDesktopClientDocs] to connect to a remote PC and emulate the [Surface Duo][SurfaceDevicesDuo] or [Samsung Galaxy Fold][SamsungMobileGalaxyFold], the pointer may shake or stutter.</span></span>  <span data-ttu-id="99e15-182">Если вы столкнулись с проблемой, [отправьте отзыв](#providing-feedback-on-experimental-features).</span><span class="sxs-lookup"><span data-stu-id="99e15-182">If you run into the issue, [send feedback](#providing-feedback-on-experimental-features).</span></span>  

### <span data-ttu-id="99e15-183">Включение новых функций отладки CSS Grid</span><span class="sxs-lookup"><span data-stu-id="99e15-183">Enable new CSS grid debugging features</span></span>  

<span data-ttu-id="99e15-184">Эта экспериментальная функция предоставляет ряд новых визуализаций, которые помогут вам в отладке макетов сетки CSS.</span><span class="sxs-lookup"><span data-stu-id="99e15-184">This experimental feature provides a number of new visualizations to help you debug CSS grid layouts.</span></span>  <span data-ttu-id="99e15-185">Чтобы просмотреть последние экспериментальные функции, [Включите этот эксперимент](#turn-on-experimental-features) и перезагрузите DevTools.</span><span class="sxs-lookup"><span data-stu-id="99e15-185">To preview the latest experimental features, [enable this experiment](#turn-on-experimental-features) and reload DevTools.</span></span>  <span data-ttu-id="99e15-186">Этот эксперимент включен по умолчанию в 87 EDGE и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="99e15-186">This experiment is on by default in Edge 87 and later.</span></span>  

#### <span data-ttu-id="99e15-187">Просмотр наложенных указателей сетки с помощью средства проверки</span><span class="sxs-lookup"><span data-stu-id="99e15-187">Viewing on-hover grid overlays with the Inspect tool</span></span>  

<span data-ttu-id="99e15-188">С помощью средства **проверки** можно быстро определить и визуализировать макеты сетки CSS на веб-сайте, наведя на них указатель мыши.</span><span class="sxs-lookup"><span data-stu-id="99e15-188">The **Inspect** tool provides a quick way to identify and visualize CSS Grid layouts in a website by hovering over them with the mouse.</span></span>  <span data-ttu-id="99e15-189">Щелкните значок **проверить** \ ( ![ проверить ](./media/inspect-icon.msft.png) \) в левом верхнем углу DevTools.</span><span class="sxs-lookup"><span data-stu-id="99e15-189">Choose the **Inspect** \(![Inspect](./media/inspect-icon.msft.png)\) icon in the top-left corner of DevTools.</span></span>  <span data-ttu-id="99e15-190">Затем наведите указатель мыши на элемент Grid на веб-сайте, который вы отлаживается.</span><span class="sxs-lookup"><span data-stu-id="99e15-190">Then, hover over a Grid element on the website you are debugging.</span></span>  <span data-ttu-id="99e15-191">Контуры отображаются вокруг сетки, а Заливка обозначает расположение зазоров сетки, если они есть.</span><span class="sxs-lookup"><span data-stu-id="99e15-191">Outlines are displayed around the grid, and shading indicates the location of grid gaps if present.</span></span>  

:::image type="complex" source="./media/grid-inspect.msft.png" alt-text="Список экспериментов в параметрах DevTools" lightbox="./media/grid-inspect.msft.png":::
   <span data-ttu-id="99e15-193">Просмотр сеток с помощью средства "Проверка"</span><span class="sxs-lookup"><span data-stu-id="99e15-193">Viewing grids with the Inspect tool</span></span>  
:::image-end:::  

#### <span data-ttu-id="99e15-194">Просмотр наложенных закрытий сетки</span><span class="sxs-lookup"><span data-stu-id="99e15-194">Viewing persistent grid overlays</span></span>  

<span data-ttu-id="99e15-195">В Microsoft Edge 86 и более поздних версиях функция «экспериментальная сетка каскадных стилей» также обеспечивает возможность включения постоянны наложенные линии сетки.</span><span class="sxs-lookup"><span data-stu-id="99e15-195">In Edge 86 and later, the experimental CSS grid feature also offers the option to enable persistent Grid overlays.</span></span>  <span data-ttu-id="99e15-196">Сохраняемые перекрытия предоставляют несколько преимуществ.</span><span class="sxs-lookup"><span data-stu-id="99e15-196">The persistent overlays provide several benefits.</span></span>  

*   <span data-ttu-id="99e15-197">После прокрутки на странице сохраняются сохраняемые наложения, перемещайте мышь и используйте другие функции DevTools.</span><span class="sxs-lookup"><span data-stu-id="99e15-197">The persistent overlays remain visible on the page as you scroll, move your mouse, and use other features of the DevTools.</span></span>  
*   <span data-ttu-id="99e15-198">Одновременно может быть включена несколько постоянных наложений, что позволяет одновременно просматривать несколько макетов сетки.</span><span class="sxs-lookup"><span data-stu-id="99e15-198">Multiple persistent overlays can be enabled at the same time, allowing you to review numerous grid layouts at once.</span></span>  
*   <span data-ttu-id="99e15-199">Постоянная наложение предлагает множество параметров настройки, например скрытие или отображение имен областей сетки, зазоров сетки, размеров дорожек и т. д.</span><span class="sxs-lookup"><span data-stu-id="99e15-199">Persistent overlays offer many configuration options, such as hiding or showing grid area names, grid gaps, track sizes, and more.</span></span>  

<span data-ttu-id="99e15-200">Два способа включения режима постоянной перекрытия сетки.</span><span class="sxs-lookup"><span data-stu-id="99e15-200">The two ways to toggle a persistent grid overlay.</span></span>  

*   <span data-ttu-id="99e15-201">Нажмите кнопку **Grid** lozenge рядом с элементом Grid, показанным в дереве DOM инструмента **элементы** .</span><span class="sxs-lookup"><span data-stu-id="99e15-201">Choose the **Grid** lozenge next to any Grid element shown in the DOM tree of the **Elements** tool.</span></span>  
    
    :::image type="complex" source="./media/grid-adorner.msft.png" alt-text="Список экспериментов в параметрах DevTools" lightbox="./media/grid-adorner.msft.png":::
       <span data-ttu-id="99e15-203">Lozenge сетки в инструменте "элементы"</span><span class="sxs-lookup"><span data-stu-id="99e15-203">Grid lozenge in Elements tool</span></span>  
    :::image-end:::  
    
*   <span data-ttu-id="99e15-204">Откройте новую панель **макета** , расположенную в инструменте элементы, и установите флажок рядом с каждым элементом Grid, который вы хотите подчеркнуть.</span><span class="sxs-lookup"><span data-stu-id="99e15-204">Open the new **Layout** panel located in the Elements tool, and choose the checkbox next to each Grid element you want to highlight.</span></span>  
    
    :::image type="complex" source="./media/grid-layout-zoom.msft.png" alt-text="Список экспериментов в параметрах DevTools" lightbox="./media/grid-layout-zoom.msft.png":::
       <span data-ttu-id="99e15-206">Панель макета</span><span class="sxs-lookup"><span data-stu-id="99e15-206">Layout panel</span></span>  
    :::image-end:::  
    
#### <span data-ttu-id="99e15-207">Настройка постоянных наложений</span><span class="sxs-lookup"><span data-stu-id="99e15-207">Configuring persistent overlays</span></span>  

<span data-ttu-id="99e15-208">Новая панель **макета** , расположенная в инструменте " **элементы** " рядом с полями **стили** и **вычисляемые** вкладки в EDGE 86 и более поздних версий — параметры конфигурации для постоянных наложений.</span><span class="sxs-lookup"><span data-stu-id="99e15-208">The new **Layout** panel, located in the **Elements** tool alongside the **Styles** and **Computed** tabs in Edge 86 and later, surfaces configuration options for persistent overlays.</span></span>  

:::image type="complex" source="./media/experiments-grid.msft.png" alt-text="Список экспериментов в параметрах DevTools" lightbox="./media/experiments-grid.msft.png":::
   <span data-ttu-id="99e15-210">Функция отладки сетки каскадных стилей</span><span class="sxs-lookup"><span data-stu-id="99e15-210">CSS grid debugging feature</span></span>  
:::image-end:::  

### <span data-ttu-id="99e15-211">Включение поддержки перемещения вкладок между панелями</span><span class="sxs-lookup"><span data-stu-id="99e15-211">Enable support to move tabs between panels</span></span>  

<span data-ttu-id="99e15-212">Обычно такие инструменты, как **элементы** и **сеть** , могут открываться только в главной панели, расположенной в верхней части DevTools.</span><span class="sxs-lookup"><span data-stu-id="99e15-212">Normally, tools such as **Elements** and **Network** may only open in the main panel that is located at the top of the DevTools.</span></span>  <span data-ttu-id="99e15-213">Такие инструменты, как **трехмерные представления** и **проблемы** , которые обычно закрываются на панели **ящика** , которая находится в нижней части DevTools.</span><span class="sxs-lookup"><span data-stu-id="99e15-213">Tools like **3D View** and **Issues** which normally only open in the **Drawer** panel that is located at the bottom of the DevTools.</span></span>  <span data-ttu-id="99e15-214">После выбора эксперимента вы можете перемещать инструменты между верхней и нижней панелями.</span><span class="sxs-lookup"><span data-stu-id="99e15-214">After you choose the experiment, you may move tools between the top and bottom panels.</span></span>  <span data-ttu-id="99e15-215">Чтобы переместить инструмент, наведите на него указатель мыши, откройте контекстное меню, а затем выберите команду **переместить в начало** или **Переместить вниз**.</span><span class="sxs-lookup"><span data-stu-id="99e15-215">To move a tool, hover on the tab, open the contextual menu \(right-click\), and choose **Move to top** or **Move to bottom**.</span></span>   <span data-ttu-id="99e15-216">Этот эксперимент позволяет настроить макет DevTools.</span><span class="sxs-lookup"><span data-stu-id="99e15-216">This experiment allows you to customize your DevTools layout.</span></span>  <span data-ttu-id="99e15-217">Чтобы показать или скрыть панель **ящика** , нажмите кнопку `Escape` .</span><span class="sxs-lookup"><span data-stu-id="99e15-217">To show or hide the **Drawer** panel, select `Escape`.</span></span>  

:::image type="complex" source="./media/experiments-move-panels.msft.png" alt-text="Список экспериментов в параметрах DevTools" lightbox="./media/experiments-move-panels.msft.png":::
   <span data-ttu-id="99e15-219">Перемещение вкладок между панелями</span><span class="sxs-lookup"><span data-stu-id="99e15-219">Moving tabs between panels</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="99e15-220">Включить подсказку</span><span class="sxs-lookup"><span data-stu-id="99e15-220">Enable webhint</span></span>  

<span data-ttu-id="99e15-221">веб- [Подсказка][WebhintMain] — это средство с открытым исходным кодом, которое предоставляет отзыв в реальном времени для веб-сайтов и локальных веб-страниц.</span><span class="sxs-lookup"><span data-stu-id="99e15-221">[webhint][WebhintMain] is an open-source tool that provides real-time feedback for websites and local web pages.</span></span>  <span data-ttu-id="99e15-222">Тип обратной связи, предоставляемой функцией " [Подсказка][WebhintMain]".</span><span class="sxs-lookup"><span data-stu-id="99e15-222">The type of feedback provided by [webhint][WebhintMain].</span></span>  

*   <span data-ttu-id="99e15-223">специальные возможности</span><span class="sxs-lookup"><span data-stu-id="99e15-223">accessibility</span></span>  
*   <span data-ttu-id="99e15-224">совместимость с различными браузерами</span><span class="sxs-lookup"><span data-stu-id="99e15-224">cross-browser compatibility</span></span>  
*   <span data-ttu-id="99e15-225">безопасность"</span><span class="sxs-lookup"><span data-stu-id="99e15-225">security</span></span>  
*   <span data-ttu-id="99e15-226">эффективности</span><span class="sxs-lookup"><span data-stu-id="99e15-226">performance</span></span>  
*   <span data-ttu-id="99e15-227">Приложения PWA</span><span class="sxs-lookup"><span data-stu-id="99e15-227">PWAs</span></span>  
*   <span data-ttu-id="99e15-228">другие распространенные проблемы с веб-разработками</span><span class="sxs-lookup"><span data-stu-id="99e15-228">other common web development issues</span></span>  

<span data-ttu-id="99e15-229">Эксперименты с этой [подсказкой][WebhintMain] отображаются на панели " [вопросы][DevtoolsIssues] " в виде обратной связи.</span><span class="sxs-lookup"><span data-stu-id="99e15-229">The [webhint][WebhintMain] experiment displays the webhint feedback in the [Issues][DevtoolsIssues] panel.</span></span>  <span data-ttu-id="99e15-230">Выберите вопрос для отображения документации решения и списка уязвимых ресурсов на вашем веб-сайте.</span><span class="sxs-lookup"><span data-stu-id="99e15-230">Select an issue to display solution documentation and a list of the affected resources on your website.</span></span>  <span data-ttu-id="99e15-231">Выберите ссылку на ресурс, чтобы открыть область " **сеть**, **источники**или **элементы** " в DevTools.</span><span class="sxs-lookup"><span data-stu-id="99e15-231">Select a resource link to open the relevant **Network**, **Sources**, or **Elements** pane in DevTools.</span></span>  

:::image type="complex" source="./media/experiments-webhint.msft.png" alt-text="Список экспериментов в параметрах DevTools" lightbox="./media/experiments-webhint.msft.png":::
   <span data-ttu-id="99e15-233">Обратная связь по этой подсказке на панели " **вопросы** "</span><span class="sxs-lookup"><span data-stu-id="99e15-233">webhint feedback in the **Issues** panel</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="99e15-234">Включение сетевой консоли</span><span class="sxs-lookup"><span data-stu-id="99e15-234">Enable Network Console</span></span>  

<span data-ttu-id="99e15-235">**Сетевая консоль** — это рабочее название эксперимента для создания искусственных сетевых запросов по протоколу HTTP.</span><span class="sxs-lookup"><span data-stu-id="99e15-235">**Network Console** is the working title of an experiment to make synthetic network requests over HTTP.</span></span>  <span data-ttu-id="99e15-236">Вы можете использовать эксперименты с **сетевой консолью** для отправки запросов на веб-API.</span><span class="sxs-lookup"><span data-stu-id="99e15-236">You may use the **Network Console** experiment to send web API requests.</span></span>  

<span data-ttu-id="99e15-237">После включения эксперимента убедитесь, что вы перезапустите DevTools.</span><span class="sxs-lookup"><span data-stu-id="99e15-237">After enabling the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="99e15-238">Чтобы использовать **консоль "сеть**", выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="99e15-238">To use the **Network Console**, use the following steps.</span></span>  

1.  <span data-ttu-id="99e15-239">Открытие области " **сеть** ".</span><span class="sxs-lookup"><span data-stu-id="99e15-239">Open the **Network** pane.</span></span>  
1.  <span data-ttu-id="99e15-240">Найдите сетевой запрос, который вы хотите изменить и отправить повторно.</span><span class="sxs-lookup"><span data-stu-id="99e15-240">Find the network request that you want to change and resend.</span></span>  
1.  <span data-ttu-id="99e15-241">Откройте контекстное меню \ (щелкните правой кнопкой мыши и выберите команду **изменить и воспроизвести**).</span><span class="sxs-lookup"><span data-stu-id="99e15-241">Open the contextual menu \(right-click\), and choose **Edit and Replay**.</span></span>  
1.  <span data-ttu-id="99e15-242">Когда откроется **Сетевая консоль** , измените сведения о сетевом запросе.</span><span class="sxs-lookup"><span data-stu-id="99e15-242">When the **Network Console** opens, edit the network request information.</span></span>  
1.  <span data-ttu-id="99e15-243">Нажмите кнопку **Отправить**.</span><span class="sxs-lookup"><span data-stu-id="99e15-243">Select **Send**.</span></span>  

:::image type="complex" source="./media/network-network-console.msft.png" alt-text="Список экспериментов в параметрах DevTools" lightbox="./media/network-network-console.msft.png":::
   <span data-ttu-id="99e15-245">**Сетевая консоль** в **консольном** ящике</span><span class="sxs-lookup"><span data-stu-id="99e15-245">**Network Console** in the **Console** drawer</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="99e15-246">Средство просмотра исходного порядка</span><span class="sxs-lookup"><span data-stu-id="99e15-246">Source Order Viewer</span></span>  

<span data-ttu-id="99e15-247">**Средство просмотра исходного порядка** — это эксперимент, в котором отображается порядок элементов в источнике страницы.</span><span class="sxs-lookup"><span data-stu-id="99e15-247">**Source Order Viewer** is an experiment that displays the order of elements in the page source.</span></span>  <span data-ttu-id="99e15-248">Порядок отображения на экране может отличаться от порядка источников, который в своюмся случае будет использовать средство чтения с экрана и пользователи клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="99e15-248">The on-screen display order may differ from the order of the source, which confuses screen reader and keyboard users.</span></span>  <span data-ttu-id="99e15-249">Для поиска различий между порядком отображения на экране и порядком расположения источника используйте эксперимент в **средстве просмотра исходного порядка** .</span><span class="sxs-lookup"><span data-stu-id="99e15-249">Use the **Source Order Viewer** experiment to find the differences between on-screen display order and the order of the source.</span></span>  

<span data-ttu-id="99e15-250">После включения эксперимента убедитесь, что вы перезапустите DevTools.</span><span class="sxs-lookup"><span data-stu-id="99e15-250">After enabling the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="99e15-251">Чтобы использовать **средство просмотра заказов исходного кода**, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="99e15-251">To use **Source Order Viewer**, use the following steps.</span></span>  

1.  <span data-ttu-id="99e15-252">Откройте область **элементы** .</span><span class="sxs-lookup"><span data-stu-id="99e15-252">Open the **Elements** pane.</span></span>  
1.  <span data-ttu-id="99e15-253">Откройте область **Специальные возможности** на панели ящик \ (Нижняя \).</span><span class="sxs-lookup"><span data-stu-id="99e15-253">Open the **Accessibility** pane in the drawer \(bottom\) panel.</span></span>  
1.  <span data-ttu-id="99e15-254">В разделе **средство просмотра исходного заказа** установите флажок **Показать порядок источников** .</span><span class="sxs-lookup"><span data-stu-id="99e15-254">Under the **Source Order Viewer** section, select the **Show Source Order** checkbox.</span></span>  
1.  <span data-ttu-id="99e15-255">Выделит любой HTML-элемент, чтобы отобразить наложение, порядок расположения которых указан в источнике страницы.</span><span class="sxs-lookup"><span data-stu-id="99e15-255">Highlight any HTML element to display an overlay that the order in the page source.</span></span>  

:::image type="complex" source="./media/experiments-source-order-viewer.msft.png" alt-text="Список экспериментов в параметрах DevTools" lightbox="./media/experiments-source-order-viewer.msft.png":::
   <span data-ttu-id="99e15-257">**Средство просмотра исходного порядка** на панели " **Специальные возможности** "</span><span class="sxs-lookup"><span data-stu-id="99e15-257">**Source Order Viewer** in the **Accessibility** pane</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 86 and later.  -->  

## <span data-ttu-id="99e15-258">Предыдущие экспериментальные функции</span><span class="sxs-lookup"><span data-stu-id="99e15-258">Previous experimental features</span></span>  

*   <span data-ttu-id="99e15-259">Теперь [трехмерный вид][Devtools3dViewIndex] доступен и включен по умолчанию в Microsoft Edge версии 83 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="99e15-259">[3D View][Devtools3dViewIndex] is now available and turned on by default in Microsoft Edge version 83 or later.</span></span>  
*   <span data-ttu-id="99e15-260">[Настройка сочетаний клавиш][DevtoolsCustomKeyboardShortcuts] теперь доступна и включена по умолчанию в Microsoft Edge версии 86 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="99e15-260">[Customize Keyboard Shortcuts][DevtoolsCustomKeyboardShortcuts] is now available and turned on by default in Microsoft Edge version 86 or later.</span></span>  

## <span data-ttu-id="99e15-261">Отзывы о экспериментальных функциях</span><span class="sxs-lookup"><span data-stu-id="99e15-261">Providing feedback on experimental features</span></span>  

<span data-ttu-id="99e15-262">Чтобы оставить отзыв о экспериментах Microsoft Edge DevTools или каких-либо других связанных с DevTools.</span><span class="sxs-lookup"><span data-stu-id="99e15-262">To provide feedback on Microsoft Edge DevTools experiments, or anything else related to DevTools.</span></span>  

*   <span data-ttu-id="99e15-263">Отправка отзыва с помощью значка " **Отправить отзыв** " в DevTools</span><span class="sxs-lookup"><span data-stu-id="99e15-263">Send your feedback using the **Send Feedback** icon in the DevTools</span></span>  
*   <span data-ttu-id="99e15-264">Твит на [@EdgeDevTools][TwitterEdgedevtools]</span><span class="sxs-lookup"><span data-stu-id="99e15-264">Tweet at [@EdgeDevTools][TwitterEdgedevtools]</span></span>  

:::image type="complex" source="./media/bing-devtools-send-feedback.msft.png" alt-text="Список экспериментов в параметрах DevTools" lightbox="./media/bing-devtools-send-feedback.msft.png":::
   <span data-ttu-id="99e15-266">Значок " **Отправить отзыв** " в Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="99e15-266">The **Send Feedback** icon in Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!--  
## Getting in touch with the Microsoft Edge DevTools team  

[!INCLUDE [contact DevTools team note](./includes/contact-devtools-team-note.md)]  
-->  

<!-- image links -->  

[ImageRotateIcon]: ./media/rotate-dark-icon.msft.png  
[ImageSpanIcon]: ./media/span-dark-icon.msft.png  
[ImageExperimentalApisIcon]: ./media/experimental-apis-dark-icon.msft.png  

<!-- links -->  

[Devtools3dViewIndex]: ./3d-view/index.md "Трехмерный вид | Документы Microsoft"  
[DevToolsCustomizeSettings]: ./customize/index.md#settings "Параметры: Настройка Microsoft Edge DevTools | Документы Microsoft"  
[DevtoolsDeviceModeIndexSimulateMobileViewport]: ./device-mode/index.md#simulate-a-mobile-viewport "Эмуляция мобильных устройств с помощью режима устройства в Microsoft Edge DevTools | Microsoft Edge"  
[DevtoolsIssues]: ./issues/index.md "Поиск и устранение проблем с помощью средства Microsoft Edge DevTools "вопросы" | Документы Microsoft"  
[DevToolsShortcuts]: ./shortcuts.md "Сочетания клавиш в Microsoft Edge DevTools | Документы Microsoft"  
[DevtoolsOpen]: ./open.md "Открыть Microsoft Edge DevTools | Документы Microsoft"  
[DevtoolsCustomKeyboardShortcuts]: ./customize/shortcuts.md "Настройка сочетаний клавиш в Microsoft Edge DevTools | Документы Microsoft"

[DualScreenWebIndex]: /dual-screen/web/index "Веб-интерфейс на базе двух экранов | Документы Microsoft"  
[DualScreenAndroidGetDuoSdk]: /dual-screen/android/get-duo-sdk "Получение эмулятора Surface Duo | Документы Microsoft"  
[DualScreenIntroductionHowWorkSeam]: /dual-screen/introduction#how-to-work-with-the-seam "Работа с стыками — введение в работу с устройствами с двумя экранами | Документы Microsoft"  
[DualScreenAndroidUseEmulator]: /dual-screen/android/use-emulator "Использование эмулятора Surface Duo | Документы Microsoft"  
[DualScreenDocsCssMedia]: /dual-screen/web/css-media-spanning "Функция многоэкранной группировки с экрана в каскадных таблицах CSS | Документы Microsoft"  
[DualScreenDocsJSAPI]: /dual-screen/web/javascript-getwindowsegments "API getWindowSegments JavaScript для устройств с двумя экранами | Документы Microsoft"  

[RemoteDesktopClientDocs]: /windows-server/remote/remote-desktop-services/clients/remote-desktop-clients "Клиенты удаленных рабочих столов | Документы Microsoft"

[MicrosoftEdge]: https://www.microsoft.com/edge "Microsoft Edge"  

[SurfaceDevicesDuo]: https://www.microsoft.com/surface/devices/surface-duo "Surface Duo | Microsoft Surface"  

[AndroidDeveloperStudio]: https://developer.android.com/studio/ "Android Studio"  

[GooglePlayMicrosoftEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Microsoft Edge | Google Play"  

[SamsungMobileGalaxyFold]: https://www.samsung.com/mobile/galaxy-fold/ "Galaxy, сгиб | Samsung"  

[TwitterEdgedevtools]: https://www.twitter.com/EdgeDevTools "Microsoft Edge DevTools | Контента"  

[WebhintMain]: https://webhint.io "Подсказка"  
