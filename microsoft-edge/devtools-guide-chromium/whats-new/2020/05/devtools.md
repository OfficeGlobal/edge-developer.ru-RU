---
description: Использование DevTools в режиме высокой контрастности Windows, соответствие сочетаний клавиш в коде DevTools и в Visual Studio, а также многое другое.
title: Новые возможности DevTools (Microsoft Edge 84)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 2752dec8bc7c4eec34ddde05a7dedff7bebef05f
ms.sourcegitcommit: b337717957529239434b4e8e1e167aebf0543518
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/15/2020
ms.locfileid: "11015491"
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

# <span data-ttu-id="7d51b-104">Новые возможности DevTools (Microsoft Edge 84)</span><span class="sxs-lookup"><span data-stu-id="7d51b-104">What's new in DevTools (Microsoft Edge 84)</span></span>  

## <span data-ttu-id="7d51b-105">Объявления из группы Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="7d51b-105">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="7d51b-106">В следующих разделах представлен список извещений, которые вы могли не получить в Microsoft Edge DevTools Teams!</span><span class="sxs-lookup"><span data-stu-id="7d51b-106">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team!</span></span> <span data-ttu-id="7d51b-107">Узнайте, как использовать новые функции в DevTools, расширения кода Visual Studio и многое другое.</span><span class="sxs-lookup"><span data-stu-id="7d51b-107">Check them out to try new features in the DevTools, Visual Studio Code extensions, and more.</span></span>  <span data-ttu-id="7d51b-108">Чтобы оставаться на связи с самыми последними и более свежими возможностями, скачайте на веб – [каналы предварительной версии Microsoft Edge][MicrosoftEdgePreviewChannels] и [следуйте указаниям Twitter][EdgeDevToolsTwitterAccount].</span><span class="sxs-lookup"><span data-stu-id="7d51b-108">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow us on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <span data-ttu-id="7d51b-109">Использование DevTools в режиме высокой контрастности Windows</span><span class="sxs-lookup"><span data-stu-id="7d51b-109">Use the DevTools in Windows high contrast mode</span></span>

<span data-ttu-id="7d51b-110">Microsoft Edge DevTools теперь отображается в режиме высокой контрастности, когда Windows находится в режиме высокой контрастности.</span><span class="sxs-lookup"><span data-stu-id="7d51b-110">The Microsoft Edge DevTools are now displayed in high contrast mode when Windows is in high contrast mode.</span></span>  

:::image type="complex" source="../../media/2020/05/high-contrast.msft.png" alt-text="Microsoft Edge DevTools в режиме высокой контрастности" lightbox="../../media/2020/05/high-contrast.msft.png":::
   <span data-ttu-id="7d51b-112">Microsoft Edge DevTools в режиме высокой контрастности</span><span class="sxs-lookup"><span data-stu-id="7d51b-112">The Microsoft Edge DevTools in high contrast mode</span></span>  
:::image-end:::  

<span data-ttu-id="7d51b-113">[Следуйте инструкциям, чтобы включить режим высокой контрастности в Windows][MicrosoftSupportWindows10HighContrastMode].</span><span class="sxs-lookup"><span data-stu-id="7d51b-113">[Follow the instructions to turn on high contrast mode in Windows][MicrosoftSupportWindows10HighContrastMode].</span></span>  <span data-ttu-id="7d51b-114">Откройте DevTools в Microsoft EDGE, нажав `F12` или `Ctrl` + `Shift` + `I` .</span><span class="sxs-lookup"><span data-stu-id="7d51b-114">Open the DevTools in Microsoft Edge by pressing `F12` or `Ctrl`+`Shift`+`I`.</span></span>  <span data-ttu-id="7d51b-115">DevTools отображаются в режиме высокой контрастности.</span><span class="sxs-lookup"><span data-stu-id="7d51b-115">The DevTools are displayed in high contrast mode.</span></span>  

> [!NOTE]
> <span data-ttu-id="7d51b-116">Microsoft Edge DevTools в настоящее время поддерживает режим высокой контрастности в Windows, но не на macOS.</span><span class="sxs-lookup"><span data-stu-id="7d51b-116">The Microsoft Edge DevTools currently support high contrast mode on Windows but not on macOS.</span></span> 

<span data-ttu-id="7d51b-117">[#1048378][CR1048378] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="7d51b-117">Chromium issue [#1048378][CR1048378]</span></span>  

### <span data-ttu-id="7d51b-118">Соответствие сочетаний клавиш в DevTools с кодом Visual Studio</span><span class="sxs-lookup"><span data-stu-id="7d51b-118">Match keyboard shortcuts in the DevTools to Visual Studio Code</span></span>  

<span data-ttu-id="7d51b-119">Из вашего [отзыва](#getting-in-touch-with-microsoft-edge-devtools-team) и средства [отслеживания общедоступных проблем Chromium][CRIssuesList]в Microsoft Edge DevTools была рассказано о том, что вы решили настроить сочетания клавиш в DevTools.</span><span class="sxs-lookup"><span data-stu-id="7d51b-119">From your [feedback](#getting-in-touch-with-microsoft-edge-devtools-team) and the [Chromium public issue tracker][CRIssuesList], the Microsoft Edge DevTools team learned that you wanted the ability to customize keyboard shortcuts in the DevTools.</span></span>  <span data-ttu-id="7d51b-120">В Microsoft Edge 84 теперь вы можете сопоставить сочетания клавиш в DevTools с [кодом Visual Studio][VSCode], который является только одной из функций, над которыми работает команда для настройки ярлыков.</span><span class="sxs-lookup"><span data-stu-id="7d51b-120">In Microsoft Edge 84, you are now able to match keyboard shortcuts in the DevTools to [Visual Studio Code][VSCode], which is just one of the features the team is working on for shortcut customization.</span></span>  

:::image type="complex" source="../../media/2020/05/keyboard-shortcut.msft.png" alt-text="Microsoft Edge DevTools в режиме высокой контрастности" lightbox="../../media/2020/05/keyboard-shortcut.msft.png":::
   <span data-ttu-id="7d51b-122">Microsoft Edge DevTools в режиме высокой контрастности</span><span class="sxs-lookup"><span data-stu-id="7d51b-122">The Microsoft Edge DevTools in high contrast mode</span></span>  
:::image-end:::  

<span data-ttu-id="7d51b-123">Чтобы попробовать эксперимент, откройте параметры DevTools, нажав `?` или выделив значок ![ параметров DevTools ][ImageSettingsIcon] в правом верхнем углу DevTools.</span><span class="sxs-lookup"><span data-stu-id="7d51b-123">To try the experiment, open DevTools Settings by pressing `?` or selecting the ![DevTools Settings icon][ImageSettingsIcon] icon in the top-right corner of the DevTools.</span></span>  <span data-ttu-id="7d51b-124">Перейдите к разделу " **эксперименты** " и установите флажок **включить пользовательские сочетания клавиш (требуется повторная загрузка)**.</span><span class="sxs-lookup"><span data-stu-id="7d51b-124">Navigate to the **Experiments** section and check **Enable custom keyboard shortcuts settings tab (requires reload)**.</span></span>  <span data-ttu-id="7d51b-125">Теперь повторно Загрузи DevTools, снова откройте параметры и перейдите к разделу **сочетания клавиш** .</span><span class="sxs-lookup"><span data-stu-id="7d51b-125">Now reload the DevTools, open Settings again, and navigate to the **Shortcuts** section.</span></span>  

<span data-ttu-id="7d51b-126">Выберите **DevTools (по умолчанию)** в раскрывающемся списке **искать сочетания клавиш из предварительной настройки** и выберите **код Visual Studio**.</span><span class="sxs-lookup"><span data-stu-id="7d51b-126">Select **DevTools (Default)** in the **Match shortcuts from preset** dropdown and select **Visual Studio Code**.</span></span>  <span data-ttu-id="7d51b-127">Сочетания клавиш в DevTools теперь соответствуют сочетаниям клавиш для эквивалентных действий в коде Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="7d51b-127">The keyboard shortcuts in the DevTools now match the shortcuts for equivalent actions in Visual Studio Code.</span></span>  

<span data-ttu-id="7d51b-128">Например, с помощью сочетания клавиш можно приостановить или продолжить выполнение сценария в [Visual Studio][VSCodeShortcuts] `F5` .</span><span class="sxs-lookup"><span data-stu-id="7d51b-128">For example, the keyboard shortcut for pausing or continuing running a script in [Visual Studio Code][VSCodeShortcuts] is `F5`.</span></span>  <span data-ttu-id="7d51b-129">В стиле **DevTools (Default)** это же сочетание клавиш в DevTools имеет тот же самый ярлык `F8` , что и в **Visual Studio** , но теперь этот ярлык также доступен `F5` .</span><span class="sxs-lookup"><span data-stu-id="7d51b-129">With the **DevTools (Default)** preset, that same shortcut in the DevTools is `F8` but with the **Visual Studio Code** preset, that shortcut is now also `F5`.</span></span>  

<span data-ttu-id="7d51b-130">В настоящее время эта функция доступна в Microsoft Edge 84 в качестве эксперимента, поэтому Поделитесь своим [мнением](#getting-in-touch-with-microsoft-edge-devtools-team) с командой!</span><span class="sxs-lookup"><span data-stu-id="7d51b-130">The feature is currently available in Microsoft Edge 84 as an experiment, so please share your [feedback](#getting-in-touch-with-microsoft-edge-devtools-team) with the team!</span></span>  

<span data-ttu-id="7d51b-131">[#174309][CR174309] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="7d51b-131">Chromium issue [#174309][CR174309]</span></span>  

### <span data-ttu-id="7d51b-132">Эмуляторы Surface Duo удаленной отладки</span><span class="sxs-lookup"><span data-stu-id="7d51b-132">Remote debug Surface Duo emulators</span></span>  

<span data-ttu-id="7d51b-133">Теперь вы можете выполнять удаленную отладку веб-содержимого, работающего в [эмуляторе Duo Surface][DualScreensAndroidEmulator] , используя полную мощь [Microsoft Edge DevTools][DevToolsChromiumGuide].</span><span class="sxs-lookup"><span data-stu-id="7d51b-133">You are now able to remotely debug your web content running in the [Surface Duo emulator][DualScreensAndroidEmulator] using the full power of the [Microsoft Edge DevTools][DevToolsChromiumGuide].</span></span>  

<span data-ttu-id="7d51b-134">С помощью [эмулятора Surface Duo][DualScreensAndroidEmulator]вы можете протестировать отображение веб-содержимого в новом классе складная и на устройствах с двумя экранами.</span><span class="sxs-lookup"><span data-stu-id="7d51b-134">With the [Surface Duo emulator][DualScreensAndroidEmulator], you are able to test how your web content renders on a new class of foldable and dual-screen devices.</span></span>  <span data-ttu-id="7d51b-135">Эмулятор запускает операционную систему Android и предоставляет [приложение Microsoft Edge Android][AndroidEdge].</span><span class="sxs-lookup"><span data-stu-id="7d51b-135">The emulator runs the Android operating system and provides the [Microsoft Edge Android app][AndroidEdge].</span></span>  <span data-ttu-id="7d51b-136">Загрузи веб-содержимое в [приложении Microsoft Edge][AndroidEdge] и отлаживать его с помощью [Microsoft Edge DevTools][DevToolsChromiumGuide].</span><span class="sxs-lookup"><span data-stu-id="7d51b-136">Load your web content in the [Microsoft Edge app][AndroidEdge] and debug it with the [Microsoft Edge DevTools][DevToolsChromiumGuide].</span></span>  

:::image type="complex" source="../../media/2020/05/surface-duo-emulator.msft.png" alt-text="Microsoft Edge DevTools в режиме высокой контрастности" lightbox="../../media/2020/05/surface-duo-emulator.msft.png":::
   <span data-ttu-id="7d51b-138">Приложение Microsoft EDGE на эмуляторе Duo Surface</span><span class="sxs-lookup"><span data-stu-id="7d51b-138">The Microsoft Edge app on the Surface Duo emulator</span></span>  
:::image-end:::  

<span data-ttu-id="7d51b-139">`edge://inspect`Страница в экземпляре [Microsoft Edge][DesktopEdge] на рабочем столе показывает **SurfaceDuoEmulator** со списком открытых вкладок или [PWAs][PwaIndex] , которые выполняются в [эмуляторе Duo Surface][DualScreensAndroidEmulator].</span><span class="sxs-lookup"><span data-stu-id="7d51b-139">The `edge://inspect` page in a desktop instance of [Microsoft Edge][DesktopEdge] shows the **SurfaceDuoEmulator** with a list of the open tabs or [PWAs][PwaIndex] that are running on the [Surface Duo emulator][DualScreensAndroidEmulator].</span></span>  

:::image type="complex" source="../../media/2020/05/edge-inspect.msft.png" alt-text="Microsoft Edge DevTools в режиме высокой контрастности" lightbox="../../media/2020/05/edge-inspect.msft.png":::
   <span data-ttu-id="7d51b-141">На `edge://inspect` странице отображается список вкладок в приложении Microsoft EDGE, работающем в эмуляторе.</span><span class="sxs-lookup"><span data-stu-id="7d51b-141">The `edge://inspect` page displays a list of the open tabs in the Microsoft Edge app running on the emulator</span></span>
:::image-end:::  

<span data-ttu-id="7d51b-142">Если выбрать пункт **Проверка** для ВКЛАДКИ или PWA, для которых нужно выполнить отладку, откроется [Microsoft Edge DevTools][DevToolsChromiumGuide].</span><span class="sxs-lookup"><span data-stu-id="7d51b-142">Selecting **inspect** for the tab or PWA that you want to debug opens the [Microsoft Edge DevTools][DevToolsChromiumGuide].</span></span>  <span data-ttu-id="7d51b-143">Следуйте пошаговым инструкциям, [чтобы выполнить удаленную отладку веб-содержимого в эмуляторе Surface Duo][DevToolsRemoteDebugDuoEmulator].</span><span class="sxs-lookup"><span data-stu-id="7d51b-143">[Follow the step-by-step guide to remotely debug your web content on the Surface Duo emulator][DevToolsRemoteDebugDuoEmulator].</span></span>  

### <span data-ttu-id="7d51b-144">Упрощенное изменение размера DevToolsого ящика</span><span class="sxs-lookup"><span data-stu-id="7d51b-144">Resize the DevTools drawer more easily</span></span>  

<span data-ttu-id="7d51b-145">В Microsoft Edge 83 или более ранней версии вы смогли изменить размер [DevToolsого ящика][DevToolsDrawer] , наведя указатель мыши на панель инструментов ящика.</span><span class="sxs-lookup"><span data-stu-id="7d51b-145">In Microsoft Edge 83 or earlier, you were only able to resize the [DevTools Drawer][DevToolsDrawer] by hovering inside the Drawer's toolbar.</span></span>  <span data-ttu-id="7d51b-146">Денежный ящик ведет себя иначе, чем другие элементы управления изменением размера для областей в DevTools, где вы наводите указатель мыши на границу области, чтобы изменить ее размер.</span><span class="sxs-lookup"><span data-stu-id="7d51b-146">The Drawer behaved differently than the other resize controls for panes in the DevTools where you hover over the border of the pane to resize it.</span></span>  <span data-ttu-id="7d51b-147">Чтобы узнать, как изменить размер ящика, который работал в версии 83 или более ранней версии Microsoft EDGE, выберите приведенный ниже рисунок.</span><span class="sxs-lookup"><span data-stu-id="7d51b-147">Select the following image to see how resizing the Drawer worked in version 83 or earlier of Microsoft Edge.</span></span>  

:::image type="complex" source="../../media/2020/05/drawer-83.msft.png" alt-text="Microsoft Edge DevTools в режиме высокой контрастности" lightbox="../../media/2020/05/drawer-83.msft.gif":::
   <span data-ttu-id="7d51b-149">Изменение размера DevTools денежных средств в Microsoft Edge 83</span><span class="sxs-lookup"><span data-stu-id="7d51b-149">Resizing the DevTools Drawer in Microsoft Edge 83</span></span>
:::image-end:::  

<!--todo:  create png that represents the gif information  -->  

<span data-ttu-id="7d51b-150">Начиная с Microsoft Edge 84, вы можете изменить размер денежного ящика, наведя указатель мыши на границу денежного ящика.</span><span class="sxs-lookup"><span data-stu-id="7d51b-150">Starting with Microsoft Edge 84, you are now able to resize the Drawer by hovering over the border of the Drawer.</span></span>  <span data-ttu-id="7d51b-151">Это изменение выровнять поведение, изменяя размер DevToolsого ящика с учетом того, как вы измените размеры других областей в DevTools.</span><span class="sxs-lookup"><span data-stu-id="7d51b-151">This change aligns the behavior resizing the DevTools Drawer with the way you resize other panes in the DevTools.</span></span>  <span data-ttu-id="7d51b-152">Чтобы изменить размер в действии в Microsoft Edge 84, выберите приведенный ниже рисунок.</span><span class="sxs-lookup"><span data-stu-id="7d51b-152">Select the following image to see resizing in action in Microsoft Edge 84.</span></span>  

:::image type="complex" source="../../media/2020/05/drawer-84.msft.png" alt-text="Microsoft Edge DevTools в режиме высокой контрастности" lightbox="../../media/2020/05/drawer-84.msft.gif":::
   <span data-ttu-id="7d51b-154">Изменение размера DevTools денежных средств в Microsoft Edge 84</span><span class="sxs-lookup"><span data-stu-id="7d51b-154">Resizing the DevTools Drawer in Microsoft Edge 84</span></span>
:::image-end:::  

<!--todo:  create png that represents the gif information  -->  

<span data-ttu-id="7d51b-155">[#1076112][CR1076112] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="7d51b-155">Chromium issue [#1076112][CR1076112]</span></span>  

### <span data-ttu-id="7d51b-156">Отображение фокуса на кнопках навигации для презентаций</span><span class="sxs-lookup"><span data-stu-id="7d51b-156">Screencasting navigation buttons display focus</span></span>  

<span data-ttu-id="7d51b-157">При удаленной отладке [устройства с Android][DevToolsRemoteDebugAndroid], [устройства с Windows 10][DevToolsRemoteDebugWindows]или [эмулятора Surface Duo][DevToolsRemoteDebugDuoEmulator]вы можете переключаться между экранной презентацией с помощью ![ значка "Показать презентацию" ][ImageScreencastingIcon] в левом верхнем углу окна DevTools.</span><span class="sxs-lookup"><span data-stu-id="7d51b-157">When remote debugging an [Android device][DevToolsRemoteDebugAndroid], a [Windows 10 device][DevToolsRemoteDebugWindows], or a [Surface Duo emulator][DevToolsRemoteDebugDuoEmulator], you are able to toggle screencasting with the ![Toggle Screencast][ImageScreencastingIcon] icon in the top-left corner of the DevTools.</span></span>  <span data-ttu-id="7d51b-158">При включенной презентации вы можете перемещаться по вкладке в Microsoft EDGE на удаленном устройстве из окна DevTools.</span><span class="sxs-lookup"><span data-stu-id="7d51b-158">With screencasting enabled, you are able to navigate the tab in Microsoft Edge on the remote device from the DevTools window.</span></span>  <span data-ttu-id="7d51b-159">В Microsoft Edge 84 эти кнопки навигации теперь также доступны для клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="7d51b-159">In Microsoft Edge 84, these navigation buttons are now also keyboard accessible.</span></span>  

:::image type="complex" source="../../media/2020/05/screencasting-nav.msft.png" alt-text="Microsoft Edge DevTools в режиме высокой контрастности" lightbox="../../media/2020/05/screencasting-nav.msft.png":::
   <span data-ttu-id="7d51b-161">При нажатии на `Shift` + `Tab` отрезке экранного URL-адреса появляется фокус на кнопке " **Обновить** "</span><span class="sxs-lookup"><span data-stu-id="7d51b-161">Pressing `Shift`+`Tab` from the screencasted URL bar shows focus on the **Refresh** button</span></span>
:::image-end:::  

<span data-ttu-id="7d51b-162">[#1081486][CR1081486] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="7d51b-162">Chromium issue [#1081486][CR1081486]</span></span>  

### <span data-ttu-id="7d51b-163">Область сведений на панели "сеть" теперь доступна</span><span class="sxs-lookup"><span data-stu-id="7d51b-163">Network panel Details pane is now accessible</span></span>  

<span data-ttu-id="7d51b-164">В Microsoft Edge 84 [область сведений][DevToolsNetworkDetails] на панели " **сеть** " теперь получает фокус при открытии ресурса в [сетевом журнале][DevToolsNetworkLog].</span><span class="sxs-lookup"><span data-stu-id="7d51b-164">In Microsoft Edge 84, the [Details pane][DevToolsNetworkDetails] in the **Network** panel now takes focus when you open it for a resource in the [Network Log][DevToolsNetworkLog].</span></span>  <span data-ttu-id="7d51b-165">Это изменение позволяет средствам чтения с экрана читать и взаимодействовать с содержимым области **сведений** .</span><span class="sxs-lookup"><span data-stu-id="7d51b-165">This change allows screen readers to read out and interact with the content of the **Details** pane.</span></span>  

:::image type="complex" source="../../media/2020/05/network-details.msft.png" alt-text="Microsoft Edge DevTools в режиме высокой контрастности" lightbox="../../media/2020/05/network-details.msft.png":::
   <span data-ttu-id="7d51b-167">При открытии области **сведений** на панели " **сеть** " выводится фокус</span><span class="sxs-lookup"><span data-stu-id="7d51b-167">The **Details** pane in the **Network** panel takes focus when opened</span></span>
:::image-end:::  

<span data-ttu-id="7d51b-168">[#963183][CR963183] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="7d51b-168">Chromium issue [#963183][CR963183]</span></span>  

## <span data-ttu-id="7d51b-169">Объявления из проекта Chromium</span><span class="sxs-lookup"><span data-stu-id="7d51b-169">Announcements from the Chromium project</span></span>  

<span data-ttu-id="7d51b-170">В следующих разделах описаны дополнительные возможности, доступные в Microsoft Edge 84, которые были задействованы в проекте Open Source Chromium.</span><span class="sxs-lookup"><span data-stu-id="7d51b-170">The following sections announce additional features available in Microsoft Edge 84 that were contributed to the open source Chromium project.</span></span>  

### <span data-ttu-id="7d51b-171">Устранение проблем с сайтом с помощью средства "новые проблемы" в DevToolsном ящике</span><span class="sxs-lookup"><span data-stu-id="7d51b-171">Fix site issues with the new Issues tool in the DevTools Drawer</span></span>

<span data-ttu-id="7d51b-172">В DevToolsном лотке была создана функция новых **проблем** , позволяющая уменьшить усталость уведомлений и бессрочные элементы **консоли**.</span><span class="sxs-lookup"><span data-stu-id="7d51b-172">The new **Issues** tool in the DevTools Drawer was built to help reduce the notification fatigue and clutter of the **Console**.</span></span>  <span data-ttu-id="7d51b-173">В настоящее время **консоль** — это центральное место для разработчиков веб-сайтов, библиотек, платформ и Microsoft Edge для записи сообщений, предупреждений и ошибок.</span><span class="sxs-lookup"><span data-stu-id="7d51b-173">Currently, the **Console** is the central place for website developers, libraries, frameworks, and Microsoft Edge to log messages, warnings, and errors.</span></span>  <span data-ttu-id="7d51b-174">Средство " **проблемы** " объединяет предупреждения из браузера в структурированном, статистическом и определенном виде, а также ссылки на уязвимые ресурсы в Microsoft Edge DevTools и инструкции по устранению проблем.</span><span class="sxs-lookup"><span data-stu-id="7d51b-174">The **Issues** tool aggregates warnings from the browser in a structured, aggregated, and actionable way, links to affected resources within Microsoft Edge DevTools, and provides guidance on how to fix the issues.</span></span>  <span data-ttu-id="7d51b-175">С течением времени вы должны видеть больше и больше предупреждений в Microsoft Edge использование в инструменте " **проблемы** ", а не на **консоли**, что поможет вам уменьшить ненужные элементы на **консоли**.</span><span class="sxs-lookup"><span data-stu-id="7d51b-175">Over time, you should see more and more warnings in Microsoft Edge surfacing in the **Issues** tool rather than the **Console**, which should help reduce the clutter in the **Console**.</span></span>  

<span data-ttu-id="7d51b-176">Чтобы приступить к работе, ознакомьтесь со статьей [Поиск и устранение проблем с помощью средства Microsoft Edge DevToolss][DevtoolsIssuesIndex].</span><span class="sxs-lookup"><span data-stu-id="7d51b-176">To get started, see [Find And Fix Problems With The Microsoft Edge DevTools Issues tool][DevtoolsIssuesIndex].</span></span>  

:::image type="complex" source="../../media/2020/05/issues.msft.png" alt-text="Microsoft Edge DevTools в режиме высокой контрастности" lightbox="../../media/2020/05/issues.msft.png":::
   <span data-ttu-id="7d51b-178">Инструмент " **проблемы** " в DevTools ящике</span><span class="sxs-lookup"><span data-stu-id="7d51b-178">The **Issues** tool in the DevTools Drawer</span></span>  
:::image-end:::  

<span data-ttu-id="7d51b-179">[#1068116][CR1068116] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="7d51b-179">Chromium issue [#1068116][CR1068116]</span></span>  

### <span data-ttu-id="7d51b-180">Просмотр сведений о специальных возможностях в подсказке режима проверки</span><span class="sxs-lookup"><span data-stu-id="7d51b-180">View accessibility information in the Inspect Mode tooltip</span></span>  

<span data-ttu-id="7d51b-181">Всплывающая подсказка **режима проверки** теперь указывает, имеет ли элемент доступное [имя и роль][WebhintHintsAxeNameRoleValue] , и это может быть [фокус клавиатуры][WebhintHintsAxeKeyboard].</span><span class="sxs-lookup"><span data-stu-id="7d51b-181">The **Inspect Mode** tooltip now indicates whether the element has an accessible [name and role][WebhintHintsAxeNameRoleValue] and is [keyboard-focusable][WebhintHintsAxeKeyboard].</span></span>  

<!--todo:  add link inspect mode tooltip (WebdevCls) when section is live  -->  
<!--todo:  add link name and role (WebdevLabelsText) when section is live  -->  
<!--todo:  add link keyboard-focusable (WebdevControlFocus) when section is live  -->  

:::image type="complex" source="../../media/2020/05/a11y.msft.png" alt-text="Microsoft Edge DevTools в режиме высокой контрастности" lightbox="../../media/2020/05/a11y.msft.png":::
  <span data-ttu-id="7d51b-183">Всплывающая подсказка **режима проверки** с информацией о специальных возможностях</span><span class="sxs-lookup"><span data-stu-id="7d51b-183">The **Inspect Mode** tooltip with accessibility information</span></span>  
:::image-end:::  

<span data-ttu-id="7d51b-184">[#1040025][CR1040025] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="7d51b-184">Chromium issue [#1040025][CR1040025]</span></span>  

### <span data-ttu-id="7d51b-185">Обновления панели "производительность"</span><span class="sxs-lookup"><span data-stu-id="7d51b-185">Performance panel updates</span></span>  

#### <span data-ttu-id="7d51b-186">Просмотр общих сведений о времени блокировки в нижнем колонтитуле</span><span class="sxs-lookup"><span data-stu-id="7d51b-186">View Total Blocking Time information in the footer</span></span>  

<span data-ttu-id="7d51b-187">После того как вы запустите производительность загрузки, на панели **производительности** теперь выводятся общие сведения о времени блокировки (TBT \) в нижнем колонтитуле.</span><span class="sxs-lookup"><span data-stu-id="7d51b-187">After recording your load performance, the **Performance** panel now shows Total Blocking Time \(TBT\) information in the footer.</span></span>  <span data-ttu-id="7d51b-188">TBT — это метрика производительности нагрузки, которая помогает количественно оценить время, затрачиваемое на использование страницы.</span><span class="sxs-lookup"><span data-stu-id="7d51b-188">TBT is a load performance metric that helps quantify how long a page takes to become usable.</span></span>  <span data-ttu-id="7d51b-189">Он по сути определяет, как долго страница может быть использована для работы, а не в том случае, если содержимое отображается на экране. но фактически не годен для использования, так как JavaScript блокирует основной поток, поэтому страница не отвечает на ввод данных пользователем.</span><span class="sxs-lookup"><span data-stu-id="7d51b-189">It essentially measures how long a page appears to be usable \(because the content is rendered to the screen\); but is not actually usable, because JavaScript is blocking the main thread and therefore the page does not respond to user input.</span></span>  <span data-ttu-id="7d51b-190">TBT — это основная метрика для приближения первой задержки ввода.</span><span class="sxs-lookup"><span data-stu-id="7d51b-190">TBT is the main metric for approximating First Input Delay.</span></span>  

<!--todo:  add link Total Blocking Time (TBT) (WebdevTbt) when section is live  -->  
<!--todo:  add link lab metric (WebdevMeasureSpeedLabField) when section is live  -->  
<!--todo:  add link Core Web Vitals (WebdevCoreWebVitals) when section is live  -->  

<span data-ttu-id="7d51b-191">Чтобы получить общую информацию о времени блокировки, не используйте рабочий процесс обновления **страницы** ![ ][ImageRefreshPageIcon] для записи загрузки страниц с помощью значка страницы обновить.</span><span class="sxs-lookup"><span data-stu-id="7d51b-191">To get Total Blocking Time information, do not use the **Refresh Page** ![Refresh page icon][ImageRefreshPageIcon] workflow for recording page load performance.</span></span>  

<span data-ttu-id="7d51b-192">Вместо этого нажмите значок **записи записи** ![ ][ImageRecordIcon] , вручную перезагрузить страницу, дождитесь загрузки страницы и остановите запись.</span><span class="sxs-lookup"><span data-stu-id="7d51b-192">Instead, select **Record** ![Record icon][ImageRecordIcon], manually reload the page, wait for the page to load, and then stop recording.</span></span>  

<span data-ttu-id="7d51b-193">Если вы видите `Total Blocking Time: Unavailable` , Microsoft Edge DevTools не получил нужные сведения из внутренних данных профилирования в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="7d51b-193">If you see `Total Blocking Time: Unavailable`, Microsoft Edge DevTools did not get the required information from the internal profiling data in Microsoft Edge.</span></span>  

:::image type="complex" source="../../media/2020/05/tbt.msft.png" alt-text="Microsoft Edge DevTools в режиме высокой контрастности" lightbox="../../media/2020/05/tbt.msft.png":::
   <span data-ttu-id="7d51b-195">Общие сведения о времени блокировки в нижнем колонтитуле записи панели " **производительность** "</span><span class="sxs-lookup"><span data-stu-id="7d51b-195">Total Blocking Time information in the footer of a **Performance** panel recording</span></span>  
:::image-end:::  

<span data-ttu-id="7d51b-196">[#1054381][CR1054381] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="7d51b-196">Chromium issue [#1054381][CR1054381]</span></span>  

#### <span data-ttu-id="7d51b-197">События смещения макета в разделе "новый интерфейс"</span><span class="sxs-lookup"><span data-stu-id="7d51b-197">Layout Shift events in the new Experience section</span></span>  

<span data-ttu-id="7d51b-198">С помощью раздела "новый **интерфейс** " на панели " **производительность** " можно определять смену макета.</span><span class="sxs-lookup"><span data-stu-id="7d51b-198">The new **Experience** section of the **Performance** panel helps you detect layout shifts.</span></span>  <span data-ttu-id="7d51b-199">Интегральная схема сдвига \ (CLS \) — это метрика, которая помогает оценить нежелательные визуальные нестабильность.</span><span class="sxs-lookup"><span data-stu-id="7d51b-199">Cumulative Layout Shift \(CLS\) is a metric that helps you quantify unwanted visual instability.</span></span>

<!--todo:  add link Core Web Vitals (WebdevCoreWebVitals) when section is live  -->  
<!--todo:  add link layout shifts (WebdevCls) when section is live  -->  

<span data-ttu-id="7d51b-200">Выберите событие **сдвиг макета** , чтобы просмотреть сведения о смене макета в области **Сводка** .</span><span class="sxs-lookup"><span data-stu-id="7d51b-200">Select the **Layout Shift** event to see the details of the layout shift in the **Summary** pane.</span></span>  <span data-ttu-id="7d51b-201">Наведите указатель мыши на поле **переместить из** и **переместили в** поля, чтобы увидеть, где произошел сдвиг макета.</span><span class="sxs-lookup"><span data-stu-id="7d51b-201">Hover over the **Moved from** and **Moved to** fields to visualize where the layout shift occurred.</span></span>  

:::image type="complex" source="../../media/2020/05/cls.msft.png" alt-text="Microsoft Edge DevTools в режиме высокой контрастности" lightbox="../../media/2020/05/cls.msft.png":::
   <span data-ttu-id="7d51b-203">Сведения о смене макета</span><span class="sxs-lookup"><span data-stu-id="7d51b-203">The details of a layout shift</span></span>  
:::image-end:::  

### <span data-ttu-id="7d51b-204">Более точная терминология по обещанию на консоли</span><span class="sxs-lookup"><span data-stu-id="7d51b-204">More accurate promise terminology in the Console</span></span>  

<span data-ttu-id="7d51b-205">При входе в систему `Promise` **консоль** неправильно предоставила `PromiseStatus` значение, равное `resolved` .</span><span class="sxs-lookup"><span data-stu-id="7d51b-205">When logging a `Promise`, the **Console** incorrectly provided `PromiseStatus` value set to `resolved`.</span></span>  

:::image type="complex" source="../../media/2020/05/resolved.msft.png" alt-text="Microsoft Edge DevTools в режиме высокой контрастности" lightbox="../../media/2020/05/resolved.msft.png":::
   <span data-ttu-id="7d51b-207">Пример **консоли** с помощью старой `resolved` терминологии</span><span class="sxs-lookup"><span data-stu-id="7d51b-207">An example of the **Console** using the old `resolved` terminology</span></span>  
:::image-end:::  

<span data-ttu-id="7d51b-208">Теперь **консоль** использует термин, который выводится `fulfilled` в соответствии со `Promise` спецификацией.</span><span class="sxs-lookup"><span data-stu-id="7d51b-208">The **Console** now uses the term `fulfilled`, which aligns with the `Promise` specification.</span></span>  <span data-ttu-id="7d51b-209">Дополнительные сведения о `Promise` спецификации можно найти в статьях [состояния и Fates на GitHub](https://github.com/domenic/promises-unwrapping/blob/master/docs/states-and-fates.md).</span><span class="sxs-lookup"><span data-stu-id="7d51b-209">For more information about the `Promise` specification, see [States and Fates on GitHub](https://github.com/domenic/promises-unwrapping/blob/master/docs/states-and-fates.md).</span></span>  

:::image type="complex" source="../../media/2020/05/fulfilled.msft.png" alt-text="Microsoft Edge DevTools в режиме высокой контрастности" lightbox="../../media/2020/05/fulfilled.msft.png":::
  <span data-ttu-id="7d51b-211">Пример **консоли** , в которой используется новая `fulfilled` терминология</span><span class="sxs-lookup"><span data-stu-id="7d51b-211">An example of the **Console** using the new `fulfilled` terminology</span></span>  
:::image-end:::  

<span data-ttu-id="7d51b-212">[#6751][CRV86751] проблем с V8</span><span class="sxs-lookup"><span data-stu-id="7d51b-212">V8 issue [#6751][CRV86751]</span></span>  

### <span data-ttu-id="7d51b-213">Обновления области "стили"</span><span class="sxs-lookup"><span data-stu-id="7d51b-213">Styles pane updates</span></span>  

#### <span data-ttu-id="7d51b-214">Поддержка ключевого слова "вернуть"</span><span class="sxs-lookup"><span data-stu-id="7d51b-214">Support for the revert keyword</span></span>  

<span data-ttu-id="7d51b-215">Пользовательский интерфейс "Автозаполнение" области " **стили** " теперь определяет ключевое слово " [вернуть][MDNRevert] CSS", которое возвращает каскадное значение свойства к предыдущему значению, примененному к стилю элемента.</span><span class="sxs-lookup"><span data-stu-id="7d51b-215">The autocomplete UI of the **Styles** pane now detects the [revert][MDNRevert] CSS keyword, which reverts the cascaded value of a property to the previous value applied to the styling of the element.</span></span>  

:::image type="complex" source="../../media/2020/05/revert.msft.png" alt-text="Microsoft Edge DevTools в режиме высокой контрастности" lightbox="../../media/2020/05/revert.msft.png":::
  <span data-ttu-id="7d51b-217">Установка значения свойства "вернуть"</span><span class="sxs-lookup"><span data-stu-id="7d51b-217">Setting the value of a property to revert</span></span>  
:::image-end:::  

<span data-ttu-id="7d51b-218">[#1075437][CR1075437] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="7d51b-218">Chromium issue [#1075437][CR1075437]</span></span>  

#### <span data-ttu-id="7d51b-219">Предварительный просмотр изображений</span><span class="sxs-lookup"><span data-stu-id="7d51b-219">Image previews</span></span>  

<span data-ttu-id="7d51b-220">Наведите указатель мыши на `background-image` значение в области **стили** , чтобы просмотреть изображение во всплывающей подсказке.</span><span class="sxs-lookup"><span data-stu-id="7d51b-220">Hover over a `background-image` value in the **Styles** pane to see a preview of the image in a tooltip.</span></span>  

:::image type="complex" source="../../media/2020/05/image-preview.msft.png" alt-text="Microsoft Edge DevTools в режиме высокой контрастности" lightbox="../../media/2020/05/image-preview.msft.png":::
  <span data-ttu-id="7d51b-222">Наведение указателя мыши на `background-image` значение</span><span class="sxs-lookup"><span data-stu-id="7d51b-222">Hovering over a `background-image` value</span></span>  
:::image-end:::  

<span data-ttu-id="7d51b-223">[#1040019][CR1040019] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="7d51b-223">Chromium issue [#1040019][CR1040019]</span></span>  

#### <span data-ttu-id="7d51b-224">Средство выбора цвета теперь использует нотацию функционального цвета, отделенную от пробелов</span><span class="sxs-lookup"><span data-stu-id="7d51b-224">Color Picker now uses space-separated functional color notation</span></span>  

<span data-ttu-id="7d51b-225">[Модуль цветов CSS Level 4][CSSWGDraftsColor4Changes3] указывает, что функции цвета, такие как `rgb()` , должны поддерживать аргументы, разделенные пробелами.</span><span class="sxs-lookup"><span data-stu-id="7d51b-225">[CSS Color Module Level 4][CSSWGDraftsColor4Changes3] specifies that color functions, such as `rgb()`, should support space-separated arguments.</span></span>  <span data-ttu-id="7d51b-226">Например, команда `rgb(0, 0, 0)` эквивалентна `rbg(0 0 0)`.</span><span class="sxs-lookup"><span data-stu-id="7d51b-226">For example, `rgb(0, 0, 0)` is equivalent to `rbg(0 0 0)`.</span></span>  

<span data-ttu-id="7d51b-227">При выборе цветов с помощью [палитры][DevtoolsCssReferenceColorPicker] цветов или переключения между цветовыми представлениями в области **стили** при нажатии `Shift` и выделении `background-color` значения должен отобразиться синтаксис аргументов, разделенных пробелами.</span><span class="sxs-lookup"><span data-stu-id="7d51b-227">When you choose colors with the [Color Picker][DevtoolsCssReferenceColorPicker] or alternate between color representations in the **Styles** pane by holding `Shift` and selecting the `background-color` value, you should see the space-separated argument syntax.</span></span>  

:::image type="complex" source="../../media/2020/05/color.msft.png" alt-text="Microsoft Edge DevTools в режиме высокой контрастности" lightbox="../../media/2020/05/color.msft.png":::
  <span data-ttu-id="7d51b-229">Использование аргументов, разделенных пробелами, в области " **стили** "</span><span class="sxs-lookup"><span data-stu-id="7d51b-229">Using space-separated arguments in the **Styles** pane</span></span>  
:::image-end:::  

<span data-ttu-id="7d51b-230">Также следует ознакомиться с синтаксисом в области **вычисляемый** раздел и подсказкой **режима проверки** .</span><span class="sxs-lookup"><span data-stu-id="7d51b-230">You should also see the syntax in the **Computed** pane and the **Inspect Mode** tooltip.</span></span>  

<span data-ttu-id="7d51b-231">Microsoft Edge DevTools использует новый синтаксис, так как предстоящие функции CSS, например [Color ()][CSSWGDraftsColor4Property] , не поддерживают устаревший синтаксис аргументов, разделенных запятыми.</span><span class="sxs-lookup"><span data-stu-id="7d51b-231">Microsoft Edge DevTools is using the new syntax because upcoming CSS features such as [color()][CSSWGDraftsColor4Property] do not support the deprecated comma-separated argument syntax.</span></span>  

<span data-ttu-id="7d51b-232">В большинстве браузеров поддерживается синтаксис аргументов, разделенных пробелами.</span><span class="sxs-lookup"><span data-stu-id="7d51b-232">The space-separated argument syntax has been supported in most browsers for a while.</span></span>  <span data-ttu-id="7d51b-233">Более подробную информацию можно найти в [статье возможность использования: нотация функциональных цветов, разделенных с помощью пробелов][CaniuseMDNSpaceSeparatedFunctionalColorNotations]</span><span class="sxs-lookup"><span data-stu-id="7d51b-233">For more information, see [Can I use: Space-separated functional color notations?][CaniuseMDNSpaceSeparatedFunctionalColorNotations]</span></span>  

<span data-ttu-id="7d51b-234">[#1072952][CR1072952] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="7d51b-234">Chromium issue [#1072952][CR1072952]</span></span>  

### <span data-ttu-id="7d51b-235">Устаревшее окно "Свойства" на панели "элементы"</span><span class="sxs-lookup"><span data-stu-id="7d51b-235">Deprecation of the Properties pane in the Elements panel</span></span>  

<span data-ttu-id="7d51b-236">Область " **Свойства** " на панели " **элементы** " устарела.</span><span class="sxs-lookup"><span data-stu-id="7d51b-236">The **Properties** pane in the **Elements** panel is deprecated.</span></span>  <span data-ttu-id="7d51b-237">Запустите `console.dir($0)` на **консоли** .</span><span class="sxs-lookup"><span data-stu-id="7d51b-237">Run `console.dir($0)` in the **Console** instead.</span></span>  

:::image type="complex" source="../../media/2020/05/properties.msft.png" alt-text="Microsoft Edge DevTools в режиме высокой контрастности" lightbox="../../media/2020/05/properties.msft.png":::
   <span data-ttu-id="7d51b-239">Область "устаревшие **Свойства** "</span><span class="sxs-lookup"><span data-stu-id="7d51b-239">The deprecated **Properties** pane</span></span>  
:::image-end:::  

#### <span data-ttu-id="7d51b-240">Ссылок</span><span class="sxs-lookup"><span data-stu-id="7d51b-240">References</span></span>  

*   [<span data-ttu-id="7d51b-241">Console. dir ()</span><span class="sxs-lookup"><span data-stu-id="7d51b-241">console.dir()</span></span>][DevtoolsConsoleApiDir]  
*   [<span data-ttu-id="7d51b-242">$0</span><span class="sxs-lookup"><span data-stu-id="7d51b-242">$0</span></span>][DevtoolsConsoleUtilitiesDom]  

### <span data-ttu-id="7d51b-243">Поддержка клавиш со встроенными приложениями в области манифеста</span><span class="sxs-lookup"><span data-stu-id="7d51b-243">App shortcuts support in the Manifest pane</span></span>  

<span data-ttu-id="7d51b-244">Сочетания клавиш для работы с приложениями помогают пользователям быстро запускать наиболее распространенные или Рекомендуемые задачи в веб-приложении.</span><span class="sxs-lookup"><span data-stu-id="7d51b-244">App shortcuts help users quickly start common or recommended tasks within a web app.</span></span>  <span data-ttu-id="7d51b-245">Меню "ярлыки приложения" отображается только для [последовательного веб-приложений][PwaIndex] , установленных на настольном компьютере или мобильном устройстве пользователя.</span><span class="sxs-lookup"><span data-stu-id="7d51b-245">The app shortcuts menu is shown only for [Progressive Web Apps][PwaIndex] that are installed on the user's desktop or mobile device.</span></span>  

<!--For more information, see [Get things done quickly with app shortcuts][WebdevAppShortcuts].  -->  

<!--todo:  add link Get things done quickly with app shortcuts (WebdevAppShortcuts) when section is live -->  

:::image type="complex" source="../../media/2020/05/app-shortcuts.msft.png" alt-text="Microsoft Edge DevTools в режиме высокой контрастности" lightbox="../../media/2020/05/app-shortcuts.msft.png":::
  <span data-ttu-id="7d51b-247">Ярлыки приложений в области **манифеста**</span><span class="sxs-lookup"><span data-stu-id="7d51b-247">App shortcuts in the **Manifest** pane</span></span>  
:::image-end:::  

## <span data-ttu-id="7d51b-248">Загрузка каналов предварительной версии Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="7d51b-248">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="7d51b-249">Если вы используете Windows или macOS, рассматривайте в качестве браузера по умолчанию использование [каналов предварительного просмотра Microsoft Edge][MicrosoftEdgePreviewChannels] .</span><span class="sxs-lookup"><span data-stu-id="7d51b-249">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="7d51b-250">Каналы предварительного просмотра предоставляют доступ к последним функциям DevTools.</span><span class="sxs-lookup"><span data-stu-id="7d51b-250">The preview channels give you access to the latest DevTools features.</span></span>  

## <span data-ttu-id="7d51b-251">Знакомство с Microsoft Edge Devtools Team</span><span class="sxs-lookup"><span data-stu-id="7d51b-251">Getting in touch with Microsoft Edge Devtools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- image links -->  

[ImageSettingsIcon]: /microsoft-edge/devtools-guide-chromium/remote-debugging/media/settings-icon.msft.png  
[ImageScreencastingIcon]: /microsoft-edge/devtools-guide-chromium/remote-debugging/media/toggle-screencast-icon.msft.png  
[ImageRefreshPageIcon]: /microsoft-edge/devtools-guide-chromium/remote-debugging/media/refresh-page-icon.msft.png  
[ImageRecordIcon]: /microsoft-edge/devtools-guide-chromium/remote-debugging/media/record-icon.msft.png  

<!-- links -->  

[DualScreensAndroidEmulator]: /dual-screen/android/use-emulator "Использование эмулятора Surface Duo | Документы Microsoft"

[DevtoolsConsoleApiDir]: /microsoft-edge/devtools-guide-chromium/console/api#dir "Справочник по API dir-Console | Документы Microsoft"  
[DevtoolsConsoleUtilitiesDom]: /microsoft-edge/devtools-guide-chromium/console/utilities#recently-selected-element-or-javascript-object "Недавно выбранный элемент или объект JavaScript: Справочник по API служебных программ для консоли | Документы Microsoft"  
[DevtoolsCssReferenceColorPicker]: /microsoft-edge/devtools-guide-chromium/css/reference#change-colors-with-the-color-picker "Изменение цвета с помощью палитры цветов — Справка по CSS | Документы Microsoft"  
[DevToolsDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Ящик: Настройка обзора | Документы Microsoft"  
[DevToolsChromiumGuide]: /microsoft-edge/devtools-guide-chromium "Инструменты разработчика Microsoft EDGE (Chromium) | Документы Microsoft"  
[DevtoolsIssuesIndex]: /microsoft-edge/devtools-guide-chromium/issues/index "Поиск и устранение проблем с вкладкой Microsoft Edge DevTools "вопросы" | Документы Microsoft"  
[DevToolsRemoteDebugAndroid]: /microsoft-edge/devtools-guide-chromium/remote-debugging/index "Начало работы с удаленными отладочными устройствами Android | Документы Microsoft"  
[DevToolsRemoteDebugDuoEmulator]: /microsoft-edge/devtools-guide-chromium/remote-debugging/surface-duo-emulator "Начало работы с эмуляторами Surface Duo удаленной отладки | Документы Microsoft"  
[DevToolsRemoteDebugWindows]: /microsoft-edge/devtools-guide-chromium/remote-debugging/windows "Начало работы с удаленной отладкой на устройствах с Windows 10 | Документы Microsoft"  
[DevToolsNetworkDetails]: /microsoft-edge/devtools-guide-chromium/network/index#inspect-the-details-of-the-resource "Проверка сведений о ресурсе | Документы Microsoft"  
[DevToolsNetworkLog]: /microsoft-edge/devtools-guide-chromium/network/index#log-network-activity "Регистрация активности в сети | Документы Microsoft"  
[PwaIndex]: /microsoft-edge/progressive-web-apps-chromium/index "Прогрессивные веб-приложения в Windows | Документы Microsoft"  
<!--[DevtoolsWhatsNew201901Inspect]: /microsoft-edge/devtools-guide-chromium/whats-new/2019/01/devtools#inspect "Detailed tooltips in Inspect Mode - What's New In DevTools (Edge 73) | Microsoft Docs"  -->  

[AndroidEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Приложение Microsoft Edge для Android"

[CaniuseMDNSpaceSeparatedFunctionalColorNotations]: https://caniuse.com/#feat=mdn-css_types_color_space_separated_functional_notation "Представления функциональных цветов, разделенные пробелами — MDN | Можно ли использовать"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Ошибки Chromium"

[CR174309]: https://crbug.com/174309 "DevTools: разрешение на настройку сочетаний клавиш и привязок клавиш | Ошибки Chromium"  
[CR963183]: https://crbug.com/963183 "DevTools не соответствуют требованиям WCAG | Ошибки Chromium"  
[CR1040019]: https://crbug.com/1040019 "DevTools: простое предварительное Просмотр изображений и фоновых изображений в области "стили" | Ошибки Chromium"  
[CR1040025]: https://crbug.com/1040025 "DevTools: Показывать основные сведения о a11y в элементе popover | Ошибки Chromium"  
[CR1048378]: https://crbug.com/1048378 "Поддержка пользовательского интерфейса DevTools для режима высокой контрастности | Ошибки Chromium"  
[CR1054381]: https://crbug.com/1054381 "CR 1054381 | Ошибки Chromium"  
[CR1068116]: https://crbug.com/1068116 "Панель отправки вопросов | Ошибки Chromium"  
[CR1072952]: https://crbug.com/1072952 "DevTools: средство выбора цвета должно создавать современный синтаксис цвета CSS | Ошибки Chromium"  
[CR1075437]: https://crbug.com/1075437 "DevTools: добавьте поддержку для ключевого слова "вернуть" и значений для CSS | Ошибки Chromium"  
[CR1076112]: https://crbug.com/1076112 "Devtools Персонализация — изменение размера лотка"  
[CR1081486]: https://crbug.com/1081486 "Фокус клавиатуры не отображается для кнопок навигации в режиме презентации | Ошибки Chromium"  
[CRV86751]: https://bugs.chromium.org/p/v8/issues/detail?id=6751 "PromiseStatus должен быть "выполнены", а не "разрешено" | Ошибки V8"  

[CSSWGDraftsColor4Changes3]: https://drafts.csswg.org/css-color#changes-from-3 "Изменения цвета 3 — цветовой модуль CSS уровня 4 | Черновики редакторов рабочих групп W3C CSS"  
[CSSWGDraftsColor4Property]: https://drafts.csswg.org/css-color#the-color-property "3. цвет переднего плана: "цветная" — уровень модуля цветовой поддержки CSS 4 | Черновики редакторов рабочих групп W3C CSS"  

[DesktopEdge]: https://www.microsoft.com/edge/ "Знакомство с новым Microsoft Edge"  

[GithubDomenicPromiseUnwrappingStatesFates]: https://github.com/domenic/promises-unwrapping/blob/master/docs/states-and-fates.md "Состояния и Fates-Domenic/обещания — разтекание | GitHub"  

[MDNRevert]: https://developer.mozilla.org/docs/Web/CSS/revert "вернуть | MDN"  
[MDNRevertBrowserCompatibility]: https://developer.mozilla.org/docs/Web/CSS/revert#Browser_compatibility "Совместимость с браузерами | MDN"  

[VSCode]: https://code.visualstudio.com/ "Код Visual Studio"  
[VSCodeShortcuts]: https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf "Сочетания клавиш в Visual Studio Code для Windows"  

[WebhintHintsAxeKeyboard]: https://webhint.io/docs/user-guide/hints/hint-axe/keyboard/ "Axe: клавиатура | Подсказка"  
[WebhintHintsAxeNameRoleValue]: https://webhint.io/docs/user-guide/hints/hint-axe/name-role-value/ "Axe: Name значение роли | Подсказка"  

[MicrosoftSupportWindows10HighContrastMode]: https://support.microsoft.com/help/4026951/windows-10-turn-high-contrast-mode-on-or-off "Включение и отключение режима высокой контрастности в Windows | Поддержка Windows"  

[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Публикация твита"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools учетной записи Twitter"  
[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Новая ошибка — MicrosoftDocs/Edge-разработчик"  
[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Каналы предварительной версии Microsoft Edge"  
[TheWebWeWant]: https://aka.ms/webwewant "Требуемый веб-сайт"  

<!--[WebdevAppShortcuts]: https://alphabet-dev/app-shortcuts "Get things done quickly with app shortcuts | alphabet-dev"  -->  
<!--[WebdevCls]: https://alphabet-dev/cls "Cumulative Layout Shift (CLS) | alphabet-dev"  -->  
<!--[WebdevControlFocus]: https://alphabet-dev/control-focus-with-tabindex "Control focus with tabindex | alphabet-dev"  -->  
<!--[WebdevMeasureSpeedLabField]: https://alphabet-dev/how-to-measure-speed#lab-data-vs-field-data "Lab data vs Field data - How to measure speed? | alphabet-dev"  -->  
<!--[WebdevLabelsText]: https://alphabet-dev/labels-and-text-alternatives "Labels and text alternatives | alphabet-dev"  -->  
<!--[WebdevTbt]: https://alphabet-dev/tbt "Total Blocking Time (TBT) | alphabet-dev"  -->  
<!--[WebdevCoreWebVitals]: https://alphabet-dev/vitals#core-web-vitals "Core Web Vitals | alphabet-dev"  -->  

> [!NOTE]
> <span data-ttu-id="7d51b-296">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="7d51b-296">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="7d51b-297">Исходная страница будет найдена [здесь](https://developers.google.com/web/updates/2020/05/devtools/index) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="7d51b-297">The original page is found [here](https://developers.google.com/web/updates/2020/05/devtools/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="7d51b-299">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="7d51b-299">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
