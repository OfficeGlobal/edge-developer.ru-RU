---
description: Последние экспериментальные функции в Microsoft Edge DevTools
title: Экспериментальные функции
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/08/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools, эксперименты
ms.openlocfilehash: ce8388e8065055e6002bd8541101bef658c7a403
ms.sourcegitcommit: 744e2ecf42bcc427ae33e5dadbf6cd48ee0ab6a5
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/17/2020
ms.locfileid: "11016750"
---
# <span data-ttu-id="ba388-104">Экспериментальные функции</span><span class="sxs-lookup"><span data-stu-id="ba388-104">Experimental features</span></span>  

<span data-ttu-id="ba388-105">Microsoft Edge DevTools предоставляет доступ к экспериментальным функциям, которые все еще находятся на стадии разработки.</span><span class="sxs-lookup"><span data-stu-id="ba388-105">Microsoft Edge DevTools provide access to experimental features that are still in development.</span></span>  <span data-ttu-id="ba388-106">Вы можете протестировать и[отдать отзыв](#providing-feedback-on-experimental-features) , прежде чем каждый компонент будет выпущен.</span><span class="sxs-lookup"><span data-stu-id="ba388-106">You may test and p[provide feedback](#providing-feedback-on-experimental-features) before each feature is released.</span></span>  

<span data-ttu-id="ba388-107">Хотя экспериментальные функции доступны во всех каналах Microsoft EDGE, вы можете получить последние экспериментальные функции с помощью канала Microsoft Edge Канарские Channel.</span><span class="sxs-lookup"><span data-stu-id="ba388-107">While experimental features are available in all channels of Microsoft Edge, you may get the latest experimental features using the Microsoft Edge Canary channel.</span></span>  

## <span data-ttu-id="ba388-108">Включение экспериментальных функций</span><span class="sxs-lookup"><span data-stu-id="ba388-108">Turn on experimental features</span></span>  

<span data-ttu-id="ba388-109">Чтобы включить экспериментальные функции в Microsoft EDGE, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="ba388-109">Use the following steps to turn on \(or off\) experimental features in Microsoft Edge.</span></span>  

1.  <span data-ttu-id="ba388-110">[Откройте DevTools][DevtoolsOpen].</span><span class="sxs-lookup"><span data-stu-id="ba388-110">[Open DevTools][DevtoolsOpen].</span></span>  
     *   <span data-ttu-id="ba388-111">Выберите `Control` + `Shift` + `I` \ (Windows \) или `Command` + `Option` + `I` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="ba388-111">Select `Control`+`Shift`+`I` \(Windows\) or `Command`+`Option`+`I` \(macOS\).</span></span>  <span data-ttu-id="ba388-112">Дополнительные сведения можно найти в разделе [сочетания клавиш Microsoft Edge DevTools][DevToolsShortcuts].</span><span class="sxs-lookup"><span data-stu-id="ba388-112">For more information, see [Microsoft Edge DevTools keyboard shortcuts][DevToolsShortcuts].</span></span>  
1.  <span data-ttu-id="ba388-113">Открытие области [параметров][DevToolsCustomizeSettings] .</span><span class="sxs-lookup"><span data-stu-id="ba388-113">Open the [Settings][DevToolsCustomizeSettings] pane.</span></span>  
    *   <span data-ttu-id="ba388-114">Выберите `Shift` + `?` .</span><span class="sxs-lookup"><span data-stu-id="ba388-114">Select `Shift`+`?`.</span></span>  <span data-ttu-id="ba388-115">Дополнительные сведения можно найти в разделе [сочетания клавиш Microsoft Edge DevTools][DevToolsShortcuts].</span><span class="sxs-lookup"><span data-stu-id="ba388-115">For more information, navigate to [Microsoft Edge DevTools keyboard shortcuts][DevToolsShortcuts].</span></span>  
1.  <span data-ttu-id="ba388-116">В левой части области **параметров** выберите раздел **эксперименты** .</span><span class="sxs-lookup"><span data-stu-id="ba388-116">On the left side of the **Settings** pane, choose the **Experiments** section.</span></span>  
    
    :::image type="complex" source="./media/experiments-devtools.msft.png" alt-text="Список экспериментов в параметрах DevTools" lightbox="./media/experiments-devtools.msft.png":::
       <span data-ttu-id="ba388-118">Список экспериментов в параметрах DevTools</span><span class="sxs-lookup"><span data-stu-id="ba388-118">List of experiments in DevTools Settings</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ba388-119">На странице " **эксперименты** " прокрутите список всех доступных экспериментальных функций и установите флажок рядом с каждым компонентом, который нужно протестировать.</span><span class="sxs-lookup"><span data-stu-id="ba388-119">On the **Experiments** page, scroll through the list of all available experimental features and choose the checkbox next to each feature that you want to test.</span></span>  
1.  <span data-ttu-id="ba388-120">Закройте и снова откройте Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="ba388-120">Close and reopen Microsoft Edge DevTools.</span></span>  

> [!NOTE]
> <span data-ttu-id="ba388-121">Экспериментальные функции постоянно обновляются и могут привести к проблемам с производительностью.</span><span class="sxs-lookup"><span data-stu-id="ba388-121">Experimental features are constantly being updated and may cause performance issues.</span></span>  <span data-ttu-id="ba388-122">Чтобы отключить экспериментальную функцию, откройте страницу **эксперименты** и снимите флажок экспериментальной функции, которую вы хотите отключить.</span><span class="sxs-lookup"><span data-stu-id="ba388-122">To turn off an experimental feature, open the **Experiments** page and clear the checkbox of the experimental feature that you want to turn off.</span></span>  

## <span data-ttu-id="ba388-123">Выделены экспериментальные функции</span><span class="sxs-lookup"><span data-stu-id="ba388-123">Highlighted experimental features</span></span>  

<span data-ttu-id="ba388-124">В следующих разделах описаны новые экспериментальные функции, доступные в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ba388-124">The following sections describe the new experimental features that are available in Microsoft Edge.</span></span>  

| <span data-ttu-id="ba388-125">Экспериментальная функция</span><span class="sxs-lookup"><span data-stu-id="ba388-125">Experimental feature</span></span> | <span data-ttu-id="ba388-126">Версия Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ba388-126">Microsoft Edge version</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="ba388-127">Эмуляция: поддержка двух режимов экрана</span><span class="sxs-lookup"><span data-stu-id="ba388-127">Emulation: Support dual screen mode</span></span>](#emulation-support-dual-screen-mode) | <span data-ttu-id="ba388-128">84 или более поздняя версия</span><span class="sxs-lookup"><span data-stu-id="ba388-128">84 or later</span></span> |  
| [<span data-ttu-id="ba388-129">Включение новых функций отладки CSS Grid</span><span class="sxs-lookup"><span data-stu-id="ba388-129">Enable new CSS grid debugging features</span></span>](#enable-new-css-grid-debugging-features) | <span data-ttu-id="ba388-130">85 или более поздняя версия</span><span class="sxs-lookup"><span data-stu-id="ba388-130">85 or later</span></span> |  
| [<span data-ttu-id="ba388-131">Включение поддержки перемещения вкладок между панелями</span><span class="sxs-lookup"><span data-stu-id="ba388-131">Enable support to move tabs between panels</span></span>](#enable-support-to-move-tabs-between-panels) | <span data-ttu-id="ba388-132">85 или более поздняя версия</span><span class="sxs-lookup"><span data-stu-id="ba388-132">85 or later</span></span> |  
| [<span data-ttu-id="ba388-133">Включить подсказку</span><span class="sxs-lookup"><span data-stu-id="ba388-133">Enable webhint</span></span>](#enable-webhint) | <span data-ttu-id="ba388-134">85 или более поздняя версия</span><span class="sxs-lookup"><span data-stu-id="ba388-134">85 or later</span></span> |  
| [<span data-ttu-id="ba388-135">Включение сетевой консоли</span><span class="sxs-lookup"><span data-stu-id="ba388-135">Enable Network Console</span></span>](#enable-network-console) | <span data-ttu-id="ba388-136">85 или более поздняя версия</span><span class="sxs-lookup"><span data-stu-id="ba388-136">85 or later</span></span> |  
| [<span data-ttu-id="ba388-137">Включение средства просмотра заказов исходным кодом</span><span class="sxs-lookup"><span data-stu-id="ba388-137">Enable Source Order Viewer</span></span>](#enable-source-order-viewer) | <span data-ttu-id="ba388-138">86 или более поздняя версия</span><span class="sxs-lookup"><span data-stu-id="ba388-138">86 or later</span></span> |  

### <span data-ttu-id="ba388-139">Эмуляция: поддержка двух режимов экрана</span><span class="sxs-lookup"><span data-stu-id="ba388-139">Emulation: Support dual screen mode</span></span>  

<span data-ttu-id="ba388-140">Предоставляет дополнительные функции для эмуляции двух новых двух экранов и устройств складная в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ba388-140">Provides additional features for emulating two new dual-screen and foldable devices in Microsoft Edge.</span></span>  

*   [<span data-ttu-id="ba388-141">Surface Duo</span><span class="sxs-lookup"><span data-stu-id="ba388-141">Surface Duo</span></span>][SurfaceDevicesDuo]  
*   [<span data-ttu-id="ba388-142">Samsung Galaxy сгиб</span><span class="sxs-lookup"><span data-stu-id="ba388-142">Samsung Galaxy Fold</span></span>][SamsungMobileGalaxyFold]  

<span data-ttu-id="ba388-143">Эмулирует устройства и переключаться между следующими элементами.</span><span class="sxs-lookup"><span data-stu-id="ba388-143">Emulate the devices and toggle between the following postures.</span></span>  

*   <span data-ttu-id="ba388-144">режим с одним экраном или сложением</span><span class="sxs-lookup"><span data-stu-id="ba388-144">single-screen or folded posture</span></span>  
*   <span data-ttu-id="ba388-145">возможность установки на два экрана или несложенный</span><span class="sxs-lookup"><span data-stu-id="ba388-145">dual-screen or unfolded posture</span></span>  
 
<span data-ttu-id="ba388-146">[Включите экспериментальные API веб-платформ](#enable-experimental-apis) и используйте [функцию многоэкранной][DualScreenDocsCssMedia] группировки с экрана CSS и [API JavaScript getWindowSegments][DualScreenDocsJSAPI] для расширения вашего веб-сайта (или приложения) на двойном экране и на складная устройствах.</span><span class="sxs-lookup"><span data-stu-id="ba388-146">[Enable experimental Web Platform APIs](#enable-experimental-apis) and use the [CSS media screen-spanning feature][DualScreenDocsCssMedia] and [JavaScript getWindowSegments API][DualScreenDocsJSAPI] to enhance your website \(or app\) for dual-screen and foldable devices.</span></span>

:::image type="complex" source="./media/experiments-surface-duo-emulation.msft.png" alt-text="Эмуляция Surface Duo в Microsoft Edge" lightbox="./media/experiments-surface-duo-emulation.msft.png":::  
   <span data-ttu-id="ba388-148">Эмуляция Surface Duo в Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ba388-148">Emulate Surface Duo in Microsoft Edge</span></span>  
:::image-end:::  

#### <span data-ttu-id="ba388-149">Включение экспериментальных API</span><span class="sxs-lookup"><span data-stu-id="ba388-149">Enable experimental APIs</span></span>  

<span data-ttu-id="ba388-150">Чтобы использовать [функцию многоэкранной области экрана CSS][DualScreenDocsCssMedia] и [API JavaScript getWindowSegments][DualScreenDocsJSAPI], включите `Experimental Web Platform features` флажок в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ba388-150">To use the [CSS media screen-spanning feature][DualScreenDocsCssMedia] and [JavaScript getWindowSegments API][DualScreenDocsJSAPI], turn on the `Experimental Web Platform features` flag in Microsoft Edge.</span></span>  <span data-ttu-id="ba388-151">Выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="ba388-151">Complete the following steps.</span></span>

1.  <span data-ttu-id="ba388-152">Перейдите к `edge://flags` .</span><span class="sxs-lookup"><span data-stu-id="ba388-152">Navigate to `edge://flags`.</span></span>  
1.  <span data-ttu-id="ba388-153">В текстовом поле **Флаги поиска** введите `Experimental Web Platform features` , выберите " **экспериментальные компоненты веб-платформы** ", а затем **Enabled**— " **Отключить** ".</span><span class="sxs-lookup"><span data-stu-id="ba388-153">In the **Search flags** textbox, enter `Experimental Web Platform features`, choose the **Experimental Web Platform features** flag, and change **Disabled** to **Enabled**.</span></span>  
1.  <span data-ttu-id="ba388-154">Перезапустите Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ba388-154">Restart Microsoft Edge.</span></span>  

:::image type="complex" source="./media/experiments-dual-screen-emulation-edge-flags.msft.png" alt-text="Флажок включения функций экспериментальной веб-платформы" lightbox="./media/experiments-dual-screen-emulation.msft.png":::
   <span data-ttu-id="ba388-156">Флажок включения функций экспериментальной веб-платформы</span><span class="sxs-lookup"><span data-stu-id="ba388-156">Enable the Experimental Web Platform features flag</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="ba388-157">Если вы используете запросы на поиск [мультимедиа в каскадных таблицах][DualScreenDocsCssMedia] или [API-интерфейс перечисления сегмента Windows (JavaScript][DualScreenDocsJSAPI] ) для повышения качества сайта или приложения для служб [Surface Duo][SurfaceDevicesDuo], необходимо также включить флажок **экспериментальные возможности веб-платформы** в [приложении Android Microsoft Edge][GooglePlayMicrosoftEdge] на устройстве [Surface Duo][SurfaceDevicesDuo] .</span><span class="sxs-lookup"><span data-stu-id="ba388-157">If you are using [CSS media queries][DualScreenDocsCssMedia] or the [JavaScript Windows Segment Enumeration API][DualScreenDocsJSAPI] to enhance your website or app for the [Surface Duo][SurfaceDevicesDuo], you must also enable the **Experimental Web Platform features** flag in the [Android Microsoft Edge app][GooglePlayMicrosoftEdge] on your [Surface Duo][SurfaceDevicesDuo] device.</span></span>
> 
> <span data-ttu-id="ba388-158">Если флажок **"экспериментальные веб-платформа** " включен [в классическом приложении Microsoft][MicrosoftEdge] EDGE и отключен для [приложения Android Microsoft Edge][GooglePlayMicrosoftEdge], поведение вашего веб-сайта или приложения в эмуляторе Lane Duo в классическом приложении Microsoft EDGE не будет совпадать с [приложением Android Microsoft][GooglePlayMicrosoftEdge] EDGE на [Surface Duo][SurfaceDevicesDuo].</span><span class="sxs-lookup"><span data-stu-id="ba388-158">If the **Experimental Web Platform features** flag is enabled in [desktop Microsoft Edge][MicrosoftEdge] and disabled in the [Android Microsoft Edge app][GooglePlayMicrosoftEdge], the behavior of your website or app in the Surface Duo emulator in desktop Microsoft Edge will not match with the [Android Microsoft Edge app][GooglePlayMicrosoftEdge] on [Surface Duo][SurfaceDevicesDuo].</span></span>  <span data-ttu-id="ba388-159">Убедитесь в том, что для устройств Android и Desktop Microsoft Edge успешно используются Эмуляторы Surface Duo в классической платформе [Microsoft Edge][MicrosoftEdge].</span><span class="sxs-lookup"><span data-stu-id="ba388-159">Ensure that the flags are matching across Android and desktop Microsoft Edge to successfully use the Surface Duo emulator in [desktop Microsoft Edge][MicrosoftEdge].</span></span>  

#### <span data-ttu-id="ba388-160">Тестирование на устройствах складная и на двух экранах</span><span class="sxs-lookup"><span data-stu-id="ba388-160">Testing on foldable and dual-screen devices</span></span>  

<span data-ttu-id="ba388-161">При эмуляции [Duo Surface][SurfaceDevicesDuo] в Microsoft Edge с двумя экранами на экране добавляется стык \ (расстояние между двумя экранами), нарисованный на веб-сайте или в приложении.</span><span class="sxs-lookup"><span data-stu-id="ba388-161">When you emulate the [Surface Duo][SurfaceDevicesDuo] in a dual-screen posture in Microsoft Edge, the seam \(the space between the two screens\) is drawn over your website or app.</span></span>  

<span data-ttu-id="ba388-162">Эмуляция дисплея соответствует способу отображения вашего веб-сайта (или приложения \) в [приложении Microsoft Edge][GooglePlayMicrosoftEdge] на платформе [Surface Duo][SurfaceDevicesDuo].</span><span class="sxs-lookup"><span data-stu-id="ba388-162">The emulated display matches the way your website \(or app\) will render in the [Microsoft Edge Android app][GooglePlayMicrosoftEdge] on [Surface Duo][SurfaceDevicesDuo].</span></span>  <span data-ttu-id="ba388-163">Возможно, вам потребуется обновить ваш веб-сайт \ (или приложение \), чтобы он лучше отображался на стыке.</span><span class="sxs-lookup"><span data-stu-id="ba388-163">You may have to update your website \(or app\) to display better along the seam.</span></span>  <span data-ttu-id="ba388-164">Для получения дополнительных сведений о адаптации веб-сайта к стыку (или внешнему приложению) перейдите к разделу [Работа с стыком][DualScreenIntroductionHowWorkSeam] в документации Surface Duo.</span><span class="sxs-lookup"><span data-stu-id="ba388-164">For more information about adapting your website \(or app\) to the seam, navigate to [How to work with the seam][DualScreenIntroductionHowWorkSeam] in the Surface Duo documentation.</span></span>  

<span data-ttu-id="ba388-165">На [панели инструментов устройства][DevtoolsDeviceModeIndexSimulateMobileViewport] есть дополнительные функции, с помощью которых можно протестировать веб-сайт или приложение в нескольких элементах управления и ориентации.</span><span class="sxs-lookup"><span data-stu-id="ba388-165">The [Device Toolbar][DevtoolsDeviceModeIndexSimulateMobileViewport] has additional features to help you test your website or app in multiple postures and orientations.</span></span>  <span data-ttu-id="ba388-166">**Rotate** ![ ][ImageRotateIcon] Чтобы повернуть окно просмотра на альбомную ориентацию, нажмите поворот на (повернуть).</span><span class="sxs-lookup"><span data-stu-id="ba388-166">Choose **Rotate** \(![Rotate][ImageRotateIcon]\) to rotate the viewport to landscape orientation.</span></span> <span data-ttu-id="ba388-167">Объедините функцию с **диапазоном** \ ( ![ Span ][ImageSpanIcon] \), чтобы переключаться между одним экраном или сложением, а также с двойным экраном или без сгиба.</span><span class="sxs-lookup"><span data-stu-id="ba388-167">Combine the feature with **Span** \(![Span][ImageSpanIcon]\) to toggle between single-screen or folded and dual-screen or unfolded postures.</span></span>  <span data-ttu-id="ba388-168">Вместе функции позволяют тестировать ваш веб-сайт или приложение во всех четырех возможностях и ориентациях.</span><span class="sxs-lookup"><span data-stu-id="ba388-168">Together, the features enable testing your website or app in all four possible postures and orientations.</span></span>  

:::image type="complex" source="./media/experiments-dual-screen-emulation-rotate-span.msft.png" alt-text="Матрица геоуровней и ориентации для двухпроцессорных и складная устройств" lightbox="./media/experiments-dual-screen-emulation-rotate-span.msft.png":::
   <span data-ttu-id="ba388-170">Матрица геоуровней и ориентации для двухпроцессорных и складная устройств</span><span class="sxs-lookup"><span data-stu-id="ba388-170">Matrix of postures and orientations for dual-screen and foldable devices</span></span>  
:::image-end:::  

<span data-ttu-id="ba388-171">Значок " **экспериментальные веб-платформы** " \ ( ![ ExperimentalApis ][ImageExperimentalApisIcon] \) отображает состояние флага " **экспериментальные веб-платформы** ".</span><span class="sxs-lookup"><span data-stu-id="ba388-171">The **Experimental Web Platform features** \(![ExperimentalApis][ImageExperimentalApisIcon]\) icon displays the state of the **Experimental Web Platform features** flag.</span></span>  <span data-ttu-id="ba388-172">Если пометка включена, значок выделена.</span><span class="sxs-lookup"><span data-stu-id="ba388-172">If the flag is turned on, the icon is highlighted.</span></span>  <span data-ttu-id="ba388-173">Если флажок выключен, значок не выделяется.</span><span class="sxs-lookup"><span data-stu-id="ba388-173">If the flag is turned off, the icon is not highlighted.</span></span>  <span data-ttu-id="ba388-174">Чтобы включить параметр \ (или выключить), найдите `edge://flags` и переключите флажок.</span><span class="sxs-lookup"><span data-stu-id="ba388-174">To turn on \(or off\) the flag, navigate to `edge://flags` and toggle the flag.</span></span>  

<!-- Commenting out until the icon issue is fixed in Edge Canary
The **Experimental Web Platform features** \(![ExperimentalApis][ImageExperimentalApisIcon]\) icon displays the state of the **Experimental Web Platform features** flag.  If the flag is turned on, the icon is highlighted.  If the flag is turned off, the icon is not highlighted.  To turn on \(or off\) the flag, either choose the icon or navigate to `edge://flags` and toggle the flag.   -->

<span data-ttu-id="ba388-175">Ниже приведены дополнительные ресурсы, которые помогут вам повысить качество вашего веб-сайта (или приложения) на устройствах с двумя экранами.</span><span class="sxs-lookup"><span data-stu-id="ba388-175">Here are additional resources that may help you enhance your website \(or app\) for dual-screen devices:</span></span>
*   <span data-ttu-id="ba388-176">Дополнительные сведения о веб-разработке на устройствах с двумя экранами можно найти на [веб-сайте с двумя экранами][DualScreenWebIndex].</span><span class="sxs-lookup"><span data-stu-id="ba388-176">For more information about web development on dual-screen devices, navigate to [Dual-screen web experiences][DualScreenWebIndex].</span></span>  
*   <span data-ttu-id="ba388-177">Установите [эмулятор Surface Duo][DualScreenAndroidUseEmulator].</span><span class="sxs-lookup"><span data-stu-id="ba388-177">Install the [Surface Duo emulator][DualScreenAndroidUseEmulator].</span></span>  <span data-ttu-id="ba388-178">Он отличается от эмулятора в Microsoft EDGE, эмулирует центр Surface Duo с Android и интегрируется с [Android][AndroidDeveloperStudio].</span><span class="sxs-lookup"><span data-stu-id="ba388-178">It is different from the emulator in Microsoft Edge, emulates the Surface Duo running Android, and integrates with [Android Studio][AndroidDeveloperStudio].</span></span>  <span data-ttu-id="ba388-179">Дополнительные сведения можно найти в [пакете SDK Surface Duo][DualScreenAndroidGetDuoSdk].</span><span class="sxs-lookup"><span data-stu-id="ba388-179">For more information, navigate to [Get the Surface Duo SDK][DualScreenAndroidGetDuoSdk].</span></span>  

> [!NOTE]
> <span data-ttu-id="ba388-180">Ниже приведен список текущих известных проблем.</span><span class="sxs-lookup"><span data-stu-id="ba388-180">The following is a list of current known issues:</span></span>
> *   <span data-ttu-id="ba388-181">При использовании [клиента удаленного рабочего стола Microsoft][RemoteDesktopClientDocs] для подключения к удаленному компьютеру и эмуляции [Galaxyого сгиба][SamsungMobileGalaxyFold] [Surface Duo][SurfaceDevicesDuo] или Samsung, указатель может стабилизации видеоизображения или перебоям.</span><span class="sxs-lookup"><span data-stu-id="ba388-181">When using a [Microsoft Remote Desktop client][RemoteDesktopClientDocs] to connect to a remote PC and emulate the [Surface Duo][SurfaceDevicesDuo] or [Samsung Galaxy Fold][SamsungMobileGalaxyFold], the pointer may shake or stutter.</span></span>  <span data-ttu-id="ba388-182">Если вы столкнулись с этой проблемой, [отправьте отзыв](#providing-feedback-on-experimental-features).</span><span class="sxs-lookup"><span data-stu-id="ba388-182">If you run into this issue, [send feedback](#providing-feedback-on-experimental-features).</span></span>  

### <span data-ttu-id="ba388-183">Включение новых функций отладки CSS Grid</span><span class="sxs-lookup"><span data-stu-id="ba388-183">Enable new CSS grid debugging features</span></span>  

<span data-ttu-id="ba388-184">Улучшена визуализация на странице при отладке веб-сайтов с макетами сетки CSS.</span><span class="sxs-lookup"><span data-stu-id="ba388-184">Improves on-page visualizations when you debug websites that have CSS grid layouts.</span></span>  <span data-ttu-id="ba388-185">Вы можете настроить перекрытия в DevTools параметров.</span><span class="sxs-lookup"><span data-stu-id="ba388-185">You may further customize the overlays in DevTools Settings.</span></span>  

:::image type="complex" source="./media/experiments-grid.msft.png" alt-text="Функция отладки сетки каскадных стилей" lightbox="./media/experiments-grid.msft.png":::
   <span data-ttu-id="ba388-187">Функция отладки сетки каскадных стилей</span><span class="sxs-lookup"><span data-stu-id="ba388-187">CSS grid debugging feature</span></span>  
:::image-end:::  

<span data-ttu-id="ba388-188">Чтобы просмотреть последние экспериментальные функции, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="ba388-188">To preview the latest experimental features, complete the following actions.</span></span>  

1.  <span data-ttu-id="ba388-189">В разделе **эксперименты** выберите параметр **включить параметры отладки для новой сетки каскадных стилей (элементы конфигурации, доступные в области Макет в элементах после перезапуска)** .</span><span class="sxs-lookup"><span data-stu-id="ba388-189">In the **Experiments** section, choose the **Enable new CSS Grid debugging features (configuration options available in Layout sidebar pane in Elements after restart)** checkbox.</span></span>  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="ba388-190">Включение поддержки перемещения вкладок между панелями</span><span class="sxs-lookup"><span data-stu-id="ba388-190">Enable support to move tabs between panels</span></span>  

<span data-ttu-id="ba388-191">Обычно такие инструменты, как **элементы** и **сеть** , могут открываться только в главной панели, расположенной в верхней части DevTools.</span><span class="sxs-lookup"><span data-stu-id="ba388-191">Normally, tools such as **Elements** and **Network** may only open in the main panel that is located at the top of the DevTools.</span></span>  <span data-ttu-id="ba388-192">Такие инструменты, как **трехмерные представления** и **проблемы** , которые обычно закрываются на панели **ящика** , которая находится в нижней части DevTools.</span><span class="sxs-lookup"><span data-stu-id="ba388-192">Tools like **3D View** and **Issues** which normally only open in the **Drawer** panel that is located at the bottom of the DevTools.</span></span>  <span data-ttu-id="ba388-193">После выбора эксперимента вы можете перемещать инструменты между верхней и нижней панелями.</span><span class="sxs-lookup"><span data-stu-id="ba388-193">After you choose the experiment, you may move tools between the top and bottom panels.</span></span>  <span data-ttu-id="ba388-194">Чтобы переместить инструмент, наведите на него указатель мыши, откройте контекстное меню, а затем выберите команду **переместить в начало** или **Переместить вниз**.</span><span class="sxs-lookup"><span data-stu-id="ba388-194">To move a tool, hover on the tab, open the contextual menu \(right-click\), and choose **Move to top** or **Move to bottom**.</span></span>   <span data-ttu-id="ba388-195">Этот эксперимент позволяет настроить макет DevTools.</span><span class="sxs-lookup"><span data-stu-id="ba388-195">This experiment allows you to customize your DevTools layout.</span></span>  <span data-ttu-id="ba388-196">Чтобы показать или скрыть панель **ящика** , нажмите кнопку `Escape` .</span><span class="sxs-lookup"><span data-stu-id="ba388-196">To show or hide the **Drawer** panel, select `Escape`.</span></span>  

:::image type="complex" source="./media/experiments-move-panels.msft.png" alt-text="Перемещение вкладок между панелями" lightbox="./media/experiments-move-panels.msft.png":::
   <span data-ttu-id="ba388-198">Перемещение вкладок между панелями</span><span class="sxs-lookup"><span data-stu-id="ba388-198">Moving tabs between panels</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="ba388-199">Включить подсказку</span><span class="sxs-lookup"><span data-stu-id="ba388-199">Enable webhint</span></span>  

<span data-ttu-id="ba388-200">веб- [Подсказка][WebhintMain] — это средство с открытым исходным кодом, которое предоставляет отзыв в реальном времени для веб-сайтов и локальных веб-страниц.</span><span class="sxs-lookup"><span data-stu-id="ba388-200">[webhint][WebhintMain] is an open-source tool that provides real-time feedback for websites and local web pages.</span></span>  <span data-ttu-id="ba388-201">Тип обратной связи, предоставляемой функцией " [Подсказка][WebhintMain]".</span><span class="sxs-lookup"><span data-stu-id="ba388-201">The type of feedback provided by [webhint][WebhintMain].</span></span>  

*   <span data-ttu-id="ba388-202">специальные возможности</span><span class="sxs-lookup"><span data-stu-id="ba388-202">accessibility</span></span>  
*   <span data-ttu-id="ba388-203">совместимость с различными браузерами</span><span class="sxs-lookup"><span data-stu-id="ba388-203">cross-browser compatibility</span></span>  
*   <span data-ttu-id="ba388-204">безопасность"</span><span class="sxs-lookup"><span data-stu-id="ba388-204">security</span></span>  
*   <span data-ttu-id="ba388-205">эффективности</span><span class="sxs-lookup"><span data-stu-id="ba388-205">performance</span></span>  
*   <span data-ttu-id="ba388-206">Приложения PWA</span><span class="sxs-lookup"><span data-stu-id="ba388-206">PWAs</span></span>  
*   <span data-ttu-id="ba388-207">другие распространенные проблемы с веб-разработками</span><span class="sxs-lookup"><span data-stu-id="ba388-207">other common web development issues</span></span>  

<span data-ttu-id="ba388-208">Эксперименты с этой [подсказкой][WebhintMain] отображаются на панели " [вопросы][DevtoolsIssues] " в виде обратной связи.</span><span class="sxs-lookup"><span data-stu-id="ba388-208">The [webhint][WebhintMain] experiment displays the webhint feedback in the [Issues][DevtoolsIssues] panel.</span></span>  <span data-ttu-id="ba388-209">Выберите вопрос для отображения документации решения и списка уязвимых ресурсов на вашем веб-сайте.</span><span class="sxs-lookup"><span data-stu-id="ba388-209">Select an issue to display solution documentation and a list of the affected resources on your website.</span></span>  <span data-ttu-id="ba388-210">Выберите ссылку на ресурс, чтобы открыть область " **сеть**, **источники**или **элементы** " в DevTools.</span><span class="sxs-lookup"><span data-stu-id="ba388-210">Select a resource link to open the relevant **Network**, **Sources**, or **Elements** pane in DevTools.</span></span>  

:::image type="complex" source="./media/experiments-webhint.msft.png" alt-text="Обратная связь по этой подсказке на панели "вопросы"" lightbox="./media/experiments-webhint.msft.png":::
   <span data-ttu-id="ba388-212">Обратная связь по этой подсказке на панели " **вопросы** "</span><span class="sxs-lookup"><span data-stu-id="ba388-212">webhint feedback in the **Issues** panel</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="ba388-213">Включение сетевой консоли</span><span class="sxs-lookup"><span data-stu-id="ba388-213">Enable Network Console</span></span>  

<span data-ttu-id="ba388-214">**Сетевая консоль** — это рабочее название эксперимента для создания искусственных сетевых запросов по протоколу HTTP.</span><span class="sxs-lookup"><span data-stu-id="ba388-214">**Network Console** is the working title of an experiment to make synthetic network requests over HTTP.</span></span>  <span data-ttu-id="ba388-215">Вы можете использовать эксперименты с **сетевой консолью** для отправки запросов на веб-API.</span><span class="sxs-lookup"><span data-stu-id="ba388-215">You may use the **Network Console** experiment to send web API requests.</span></span>  

<span data-ttu-id="ba388-216">После включения эксперимента убедитесь, что вы перезапустите DevTools.</span><span class="sxs-lookup"><span data-stu-id="ba388-216">After enabling the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="ba388-217">Чтобы использовать **консоль "сеть**", выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="ba388-217">To use the **Network Console**, use the following steps.</span></span>    

1.  <span data-ttu-id="ba388-218">Открытие области " **сеть** ".</span><span class="sxs-lookup"><span data-stu-id="ba388-218">Open the **Network** pane.</span></span>  
1.  <span data-ttu-id="ba388-219">Найдите сетевой запрос, который вы хотите изменить и отправить повторно.</span><span class="sxs-lookup"><span data-stu-id="ba388-219">Find the network request that you want to change and resend.</span></span>  
1.  <span data-ttu-id="ba388-220">Откройте контекстное меню \ (щелкните правой кнопкой мыши и выберите команду **изменить и воспроизвести**).</span><span class="sxs-lookup"><span data-stu-id="ba388-220">Open the contextual menu \(right-click\), and choose **Edit and Replay**.</span></span>  
1.  <span data-ttu-id="ba388-221">Когда откроется **Сетевая консоль** , измените сведения о сетевом запросе.</span><span class="sxs-lookup"><span data-stu-id="ba388-221">When the **Network Console** opens, edit the network request information.</span></span>  
1.  <span data-ttu-id="ba388-222">Нажмите кнопку **Отправить**.</span><span class="sxs-lookup"><span data-stu-id="ba388-222">Select **Send**.</span></span>  

:::image type="complex" source="./media/network-network-console.msft.png" alt-text="Сетевая консоль в консольном ящике" lightbox="./media/network-network-console.msft.png":::
   <span data-ttu-id="ba388-224">**Сетевая консоль** в **консольном** ящике</span><span class="sxs-lookup"><span data-stu-id="ba388-224">**Network Console** in the **Console** drawer</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="ba388-225">Включение средства просмотра заказов исходным кодом</span><span class="sxs-lookup"><span data-stu-id="ba388-225">Enable Source Order Viewer</span></span>  

<span data-ttu-id="ba388-226">**Средство просмотра исходного порядка** — это эксперимент, в котором отображается порядок элементов в источнике страницы.</span><span class="sxs-lookup"><span data-stu-id="ba388-226">**Source Order Viewer** is an experiment that displays the order of elements in the page source.</span></span>  <span data-ttu-id="ba388-227">Порядок отображения на экране может отличаться от порядка источников, который в своюмся случае будет использовать средство чтения с экрана и пользователи клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="ba388-227">The on-screen display order may differ from the order of the source, which confuses screen reader and keyboard users.</span></span>  <span data-ttu-id="ba388-228">Для поиска различий между порядком отображения на экране и порядком расположения источника используйте эксперимент в **средстве просмотра исходного порядка** .</span><span class="sxs-lookup"><span data-stu-id="ba388-228">Use the **Source Order Viewer** experiment to find the differences between on-screen display order and the order of the source.</span></span>  

<span data-ttu-id="ba388-229">После включения эксперимента убедитесь, что вы перезапустите DevTools.</span><span class="sxs-lookup"><span data-stu-id="ba388-229">After enabling the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="ba388-230">Чтобы использовать средство просмотра заказов исходного кода, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="ba388-230">To use Source Order Viewer:</span></span>  

1.  <span data-ttu-id="ba388-231">Откройте область **элементы** .</span><span class="sxs-lookup"><span data-stu-id="ba388-231">Open the **Elements** pane.</span></span>  
1.  <span data-ttu-id="ba388-232">Откройте область **Специальные возможности** на панели ящик \ (Нижняя \).</span><span class="sxs-lookup"><span data-stu-id="ba388-232">Open the **Accessibility** pane in the drawer \(bottom\) panel.</span></span>  
1.  <span data-ttu-id="ba388-233">В разделе **средство просмотра исходного заказа** установите флажок **Показать порядок источников** .</span><span class="sxs-lookup"><span data-stu-id="ba388-233">Under the **Source Order Viewer** section, select the **Show Source Order** checkbox.</span></span>  
1.  <span data-ttu-id="ba388-234">Выделит любой HTML-элемент, чтобы отобразить наложение, порядок расположения которых указан в источнике страницы.</span><span class="sxs-lookup"><span data-stu-id="ba388-234">Highlight any HTML element to display an overlay that the order in the page source.</span></span>  

:::image type="complex" source="./media/experiments-source-order-viewer.msft.png" alt-text="Средство просмотра исходного порядка на панели "Специальные возможности"" lightbox="./media/experiments-source-order-viewer.msft.png":::
   <span data-ttu-id="ba388-236">**Средство просмотра исходного порядка** на панели " **Специальные возможности** "</span><span class="sxs-lookup"><span data-stu-id="ba388-236">**Source Order Viewer** in the **Accessibility** pane</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 86 and later.  -->  

## <span data-ttu-id="ba388-237">Предыдущие экспериментальные функции</span><span class="sxs-lookup"><span data-stu-id="ba388-237">Previous experimental features</span></span>  

*   <span data-ttu-id="ba388-238">Теперь [трехмерный вид][Devtools3dViewIndex] доступен и включен по умолчанию в Microsoft Edge версии 83 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="ba388-238">[3D View][Devtools3dViewIndex] is now available and turned on by default in Microsoft Edge version 83 or later.</span></span>  
*   <span data-ttu-id="ba388-239">[Настройка сочетаний клавиш][DevtoolsCustomKeyboardShortcuts] теперь доступна и включена по умолчанию в Microsoft Edge версии 86 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="ba388-239">[Customize Keyboard Shortcuts][DevtoolsCustomKeyboardShortcuts] is now available and turned on by default in Microsoft Edge version 86 or later.</span></span>  

## <span data-ttu-id="ba388-240">Отзывы о экспериментальных функциях</span><span class="sxs-lookup"><span data-stu-id="ba388-240">Providing feedback on experimental features</span></span>  

<span data-ttu-id="ba388-241">Чтобы оставить отзыв о экспериментах Microsoft Edge DevTools или каких-либо других связанных с DevTools.</span><span class="sxs-lookup"><span data-stu-id="ba388-241">To provide feedback on Microsoft Edge DevTools experiments, or anything else related to DevTools.</span></span>  

*   <span data-ttu-id="ba388-242">Отправка отзыва с помощью значка " **Отправить отзыв** " в DevTools</span><span class="sxs-lookup"><span data-stu-id="ba388-242">Send your feedback using the **Send Feedback** icon in the DevTools</span></span>  
*   <span data-ttu-id="ba388-243">Твит на [@EdgeDevTools][TwitterEdgedevtools]</span><span class="sxs-lookup"><span data-stu-id="ba388-243">Tweet at [@EdgeDevTools][TwitterEdgedevtools]</span></span>  

:::image type="complex" source="./media/bing-devtools-send-feedback.msft.png" alt-text="Значок "Отправить отзыв" в Microsoft Edge DevTools" lightbox="./media/bing-devtools-send-feedback.msft.png":::
   <span data-ttu-id="ba388-245">Значок " **Отправить отзыв** " в Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="ba388-245">The **Send Feedback** icon in Microsoft Edge DevTools</span></span>  
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
