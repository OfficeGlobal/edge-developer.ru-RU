---
description: Эмуляция концепции deficiencies, закрепление слева в меню команд и т. д.
title: Новые возможности DevTools (Microsoft Edge 83)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: f9eb306ab7b30495c91ff4a70797898459d7e722
ms.sourcegitcommit: b337717957529239434b4e8e1e167aebf0543518
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/15/2020
ms.locfileid: "11015484"
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

# <span data-ttu-id="0d3bc-104">Новые возможности DevTools (Microsoft Edge 83)</span><span class="sxs-lookup"><span data-stu-id="0d3bc-104">What's New In DevTools (Microsoft Edge 83)</span></span>  

<span data-ttu-id="0d3bc-105">Согласно обновленному календарному плану Chromium мы настраивая наше расписание для предстоящих выпусков Microsoft EDGE и отменив выпуск Microsoft Edge 82.</span><span class="sxs-lookup"><span data-stu-id="0d3bc-105">Following the updated Chromium schedule, we are adjusting our schedule for upcoming Microsoft Edge releases and cancelling the Microsoft Edge 82 release.</span></span> <span data-ttu-id="0d3bc-106">Дополнительные сведения находятся в записи [блога][WindowsBlogStableRelease] .</span><span class="sxs-lookup"><span data-stu-id="0d3bc-106">Check out our [blog post][WindowsBlogStableRelease] for more info.</span></span>  

<span data-ttu-id="0d3bc-107">Ниже описаны новые возможности, доступные в DevTools в Microsoft Edge 83.</span><span class="sxs-lookup"><span data-stu-id="0d3bc-107">Here are the new features available in the DevTools in Microsoft Edge 83.</span></span>  

## <span data-ttu-id="0d3bc-108">Объявления из группы Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="0d3bc-108">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="0d3bc-109">В следующих разделах представлен список извещений, которые вы могли не получить в Microsoft Edge DevTools Teams!</span><span class="sxs-lookup"><span data-stu-id="0d3bc-109">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team!</span></span> <span data-ttu-id="0d3bc-110">Узнайте, как использовать новые функции в DevTools, расширения кода Visual Studio и многое другое.</span><span class="sxs-lookup"><span data-stu-id="0d3bc-110">Check them out to try new features in the DevTools, Visual Studio Code extensions, and more.</span></span>  <span data-ttu-id="0d3bc-111">Чтобы оставаться на связи с самыми последними и более свежими возможностями, скачайте на веб – [каналы предварительной версии Microsoft Edge][MicrosoftEdgePreviewChannels] и [следуйте указаниям Twitter][EdgeDevToolsTwitterAccount].</span><span class="sxs-lookup"><span data-stu-id="0d3bc-111">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow us on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <span data-ttu-id="0d3bc-112">Удаленная отладка Microsoft EDGE на устройствах с Windows 10</span><span class="sxs-lookup"><span data-stu-id="0d3bc-112">Remotely debug Microsoft Edge on Windows 10 Devices</span></span>  

<span data-ttu-id="0d3bc-113">Приложение [Remote Tools для Microsoft Edge \ (бета-версия)][RemoteTools] теперь доступно в [магазине Microsoft Store][MicrosoftStore].</span><span class="sxs-lookup"><span data-stu-id="0d3bc-113">The [Remote Tools for Microsoft Edge \(Beta\)][RemoteTools] app is now available in the [Microsoft Store][MicrosoftStore].</span></span>  <span data-ttu-id="0d3bc-114">С помощью этого приложения, которое расширяет [портал устройств Windows][WindowsUwpDebugTestPerfDevicePortal], вы можете подключаться из экземпляра Microsoft EDGE, запущенного на компьютере разработки, на удаленное устройство с Windows 10, просмотреть список конечных объектов \ (все вкладки в Microsoft EDGE и [PWAs][PprgressiveWebAppsChromiumIndex] открыть на устройстве с Windows 10 \) и использовать DevTools на своем компьютере для разработки по отношению к целевому объекту на удаленном устройстве с Windows 10.</span><span class="sxs-lookup"><span data-stu-id="0d3bc-114">Using this app, which extends the [Windows Device Portal][WindowsUwpDebugTestPerfDevicePortal], you are able to connect from the instance of Microsoft Edge running on your development machine to a remote Windows 10 device, see a list of targets \(all tabs in Microsoft Edge and [PWAs][PprgressiveWebAppsChromiumIndex] open on the Windows 10 device\), and use the DevTools on your development machine against a target running on the remote Windows 10 device.</span></span>  

:::image type="complex" source="../../media/2020/03/remote-tools.msft.png" alt-text="Приложение Remote Tools для Microsoft EDGE (бета-версия), доступное в Microsoft Store" lightbox="../../media/2020/03/remote-tools.msft.png":::
   <span data-ttu-id="0d3bc-116">Приложение [Remote Tools для Microsoft EDGE (бета-версия)][RemoteTools] , доступное в [Microsoft Store][MicrosoftStore]</span><span class="sxs-lookup"><span data-stu-id="0d3bc-116">The [Remote Tools for Microsoft Edge (Beta)][RemoteTools] app available in the [Microsoft Store][MicrosoftStore]</span></span>  
:::image-end:::  

<span data-ttu-id="0d3bc-117">[Ознакомьтесь с руководством по настройке устройства с Windows 10 и компьютера для разработки удаленной отладки][DevtoolsRemoteDebuggingWindows].</span><span class="sxs-lookup"><span data-stu-id="0d3bc-117">[Read our guide for setting up your Windows 10 device and your development machine for remote debugging][DevtoolsRemoteDebuggingWindows].</span></span>  <span data-ttu-id="0d3bc-118">Сообщите нам об удаленной отладке, выполнив [твит][PostTweetEdgeDevTools] или щелкнув значок " [Отправить отзыв](#getting-in-touch-with-microsoft-edge-devtools-team) "!</span><span class="sxs-lookup"><span data-stu-id="0d3bc-118">Let us know about your remote debugging experience by [tweeting][PostTweetEdgeDevTools] or clicking the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

### <span data-ttu-id="0d3bc-119">Новые способы доступа к параметрам</span><span class="sxs-lookup"><span data-stu-id="0d3bc-119">New ways to access Settings</span></span>  

<span data-ttu-id="0d3bc-120">Существует множество параметров для DevTools, которые можно настроить таким образом, чтобы DevTools внешний вид, оформление и работу.</span><span class="sxs-lookup"><span data-stu-id="0d3bc-120">There are tons of settings for the DevTools that you are able to customize to make the DevTools look, feel, and work the way you need.</span></span> <span data-ttu-id="0d3bc-121">В Microsoft Edge 83 доступ к [параметрам][DevtoolsCustomizeIndexSettings] в DevTools теперь стал более простым.</span><span class="sxs-lookup"><span data-stu-id="0d3bc-121">In Microsoft Edge 83, accessing [Settings][DevtoolsCustomizeIndexSettings] in the DevTools is now much easier.</span></span> <span data-ttu-id="0d3bc-122">Откройте параметры с помощью значка шестеренки рядом с пунктом оповещения консоли и главное меню.</span><span class="sxs-lookup"><span data-stu-id="0d3bc-122">Open Settings with the gear icon next to Console alerts and the main menu.</span></span>  

:::image type="complex" source="../../media/2020/03/settings.msft.png" alt-text="Приложение Remote Tools для Microsoft EDGE (бета-версия), доступное в Microsoft Store" lightbox="../../media/2020/03/settings.msft.png":::
   <span data-ttu-id="0d3bc-124">Значок шестеренки, чтобы открыть **Параметры** в DevTools</span><span class="sxs-lookup"><span data-stu-id="0d3bc-124">The gear icon opens **Settings** in the DevTools</span></span>  
:::image-end:::  

<span data-ttu-id="0d3bc-125">Вы также можете открыть [Параметры][DevtoolsCustomizeIndexSettings] из **главного меню** в разделе **Дополнительные инструменты**.</span><span class="sxs-lookup"><span data-stu-id="0d3bc-125">You are also able to open [Settings][DevtoolsCustomizeIndexSettings] from the **Main Menu** under **More tools**.</span></span>

:::image type="complex" source="../../media/2020/03/settings2.msft.png" alt-text="Приложение Remote Tools для Microsoft EDGE (бета-версия), доступное в Microsoft Store" lightbox="../../media/2020/03/settings2.msft.png":::
   <span data-ttu-id="0d3bc-127">**Главное меню**  >  **Дополнительные инструменты**  >  **Параметры**</span><span class="sxs-lookup"><span data-stu-id="0d3bc-127">**Main Menu** > **More tools** > **Settings**</span></span>  
:::image-end:::  

<span data-ttu-id="0d3bc-128">[#1050855][CR1050855] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="0d3bc-128">Chromium issue [#1050855][CR1050855]</span></span>

### <span data-ttu-id="0d3bc-129">Новые и улучшенные infobars</span><span class="sxs-lookup"><span data-stu-id="0d3bc-129">New and improved infobars</span></span>

<span data-ttu-id="0d3bc-130">В DevTools теперь есть улучшенные возможности, которые появятся на панелях уведомлений \ (infobars \) на информационной панели.</span><span class="sxs-lookup"><span data-stu-id="0d3bc-130">Informational notification bars \(infobars\) in DevTools now have an improved look and more functionality.</span></span> <span data-ttu-id="0d3bc-131">В Microsoft Edge 83 infobars более удобны для чтения и предоставляют кнопки, чтобы можно было принять нужное действие прямо сейчас.</span><span class="sxs-lookup"><span data-stu-id="0d3bc-131">In Microsoft Edge 83, infobars are easier to read and provide buttons so you are able to take the relevant action right away.</span></span>  

:::image type="complex" source="../../media/2020/03/infobar.msft.png" alt-text="Приложение Remote Tools для Microsoft EDGE (бета-версия), доступное в Microsoft Store" lightbox="../../media/2020/03/infobar.msft.png":::
   <span data-ttu-id="0d3bc-133">Информационная панель для печати файла minified в Microsoft Edge версии 83</span><span class="sxs-lookup"><span data-stu-id="0d3bc-133">Infobar for pretty-printing a minified file in Microsoft Edge Version 83</span></span>  
:::image-end:::  

<span data-ttu-id="0d3bc-134">[#1056348][CR1056348] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="0d3bc-134">Chromium issue [#1056348][CR1056348]</span></span>

### <span data-ttu-id="0d3bc-135">Навигация в окне выбора цвета с помощью клавиатуры</span><span class="sxs-lookup"><span data-stu-id="0d3bc-135">Navigate the Color Picker with your keyboard</span></span>  

<span data-ttu-id="0d3bc-136">[Палитра цветов][DevtoolsCssReferenceColorPicker] — это графический интерфейс пользователя на [панели «элементы»][DevtoolsCssIndex] для изменения `color` и `background-color` объявлений.</span><span class="sxs-lookup"><span data-stu-id="0d3bc-136">The [Color Picker][DevtoolsCssReferenceColorPicker] is a GUI in the [Elements panel][DevtoolsCssIndex] for changing `color` and `background-color` declarations.</span></span>  <span data-ttu-id="0d3bc-137">В предыдущих версиях Microsoft Edge вы не смогли перемещаться по разделу " **тени** " в [палитре цветов][DevtoolsCssReferenceColorPicker] с помощью клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="0d3bc-137">In previous versions of Microsoft Edge, you were not able to navigate the **Shades** section of the [Color Picker][DevtoolsCssReferenceColorPicker] with the keyboard.</span></span>  

:::image type="complex" source="../../media/2020/03/color-picker.msft.png" alt-text="Приложение Remote Tools для Microsoft EDGE (бета-версия), доступное в Microsoft Store" lightbox="../../media/2020/03/color-picker.msft.png":::
   <span data-ttu-id="0d3bc-139">Теперь вы можете использовать клавиатуру для перемещения селектора в разделе " **тени** " [палитры цветов][DevtoolsCssReferenceColorPicker]</span><span class="sxs-lookup"><span data-stu-id="0d3bc-139">You are now able to use your keyboard to move the selector in the **Shades** section of the [Color Picker][DevtoolsCssReferenceColorPicker]</span></span>  
:::image-end:::  

<span data-ttu-id="0d3bc-140">В Microsoft Edge 83 теперь можно использовать клавиатуру для перемещения селектора в разделе **тени** окна выбора цвета.</span><span class="sxs-lookup"><span data-stu-id="0d3bc-140">In Microsoft Edge 83, you are now able to use the keyboard to move the selector in the **Shades** section of the Color Picker.</span></span>  

<span data-ttu-id="0d3bc-141">[#963183][CR963183] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="0d3bc-141">Chromium issue [#963183][CR963183]</span></span>  

### <span data-ttu-id="0d3bc-142">Вкладка "Свойства" теперь заполняется после обновления страницы</span><span class="sxs-lookup"><span data-stu-id="0d3bc-142">Properties tab now populates after a page refresh</span></span>  

<span data-ttu-id="0d3bc-143">В Microsoft Edge 81 и более ранних версий **вкладка Свойства** на [панели элементы][DevtoolsCssIndex] была разорвана обновлениями страницы.</span><span class="sxs-lookup"><span data-stu-id="0d3bc-143">In Microsoft Edge 81 and earlier, the **Properties tab** in the [Elements panel][DevtoolsCssIndex] was broken by page refreshes.</span></span>  <span data-ttu-id="0d3bc-144">После обновления страницы на **вкладке Свойства** не заполнятся свойства элемента, выбранного в данный момент.</span><span class="sxs-lookup"><span data-stu-id="0d3bc-144">When you refreshed the page, the **Properties tab** did not populate the properties of the currently-selected element.</span></span>  

:::image type="complex" source="../../media/2020/03/properties-in-81.msft.png" alt-text="Приложение Remote Tools для Microsoft EDGE (бета-версия), доступное в Microsoft Store" lightbox="../../media/2020/03/properties-in-81.msft.png":::
   <span data-ttu-id="0d3bc-146">В Microsoft Edge 81 и более ранних версий **вкладка Свойства** была пуста после обновления страницы</span><span class="sxs-lookup"><span data-stu-id="0d3bc-146">In Microsoft Edge 81 and earlier, the **Properties tab** was blank after a page refresh</span></span>  
:::image-end:::  

<span data-ttu-id="0d3bc-147">В Microsoft Edge 83 теперь вы можете видеть свойства элемента, выбранного в данный момент, после обновления страницы на **вкладке Свойства**.</span><span class="sxs-lookup"><span data-stu-id="0d3bc-147">In Microsoft Edge 83, you are now able to see the properties of the currently-selected element after a page refresh in the **Properties tab**.</span></span>  

:::image type="complex" source="../../media/2020/03/properties-in-82.msft.png" alt-text="Приложение Remote Tools для Microsoft EDGE (бета-версия), доступное в Microsoft Store" lightbox="../../media/2020/03/properties-in-82.msft.png":::
   <span data-ttu-id="0d3bc-149">В Microsoft Edge 83 на **вкладке Свойства** отображаются свойства элемента, выбранного в данный момент, после обновления страницы.</span><span class="sxs-lookup"><span data-stu-id="0d3bc-149">In Microsoft Edge 83, the **Properties tab** displays the properties of the currently-selected element after a page refresh</span></span>  
:::image-end:::  

<span data-ttu-id="0d3bc-150">[#1050999][CR1050999] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="0d3bc-150">Chromium issue [#1050999][CR1050999]</span></span>  

### <span data-ttu-id="0d3bc-151">Используйте клавиши со стрелками для прокрутки в инструменте "изменения"</span><span class="sxs-lookup"><span data-stu-id="0d3bc-151">Use the arrow keys to scroll in the Changes tool</span></span>  

<span data-ttu-id="0d3bc-152">**Средство "изменения** " отслеживает все изменения, внесенные в CSS или JavaScript, в DevTools.</span><span class="sxs-lookup"><span data-stu-id="0d3bc-152">The **Changes tool** tracks any changes you have made to CSS or JavaScript in the DevTools.</span></span>  <span data-ttu-id="0d3bc-153">Вы можете использовать **средство "изменения** ", чтобы быстро просмотреть все изменения и вернуть их в редактор или интегрированную среду разработки.</span><span class="sxs-lookup"><span data-stu-id="0d3bc-153">You are able to use the **Changes tool** to quickly see all your changes and take those back to your editor/IDE.</span></span>  

<span data-ttu-id="0d3bc-154">Откройте **инструмент "изменения** ", нажав `Ctrl` + `Shift` + `P` в DevTools, чтобы открыть [меню команд][DevToolsCommandMenuIndex] и ввести текст `changes` .</span><span class="sxs-lookup"><span data-stu-id="0d3bc-154">Open the **Changes tool** by pressing `Ctrl`+`Shift`+`P` in the DevTools to open the [Command Menu][DevToolsCommandMenuIndex] and typing `changes`.</span></span>  <span data-ttu-id="0d3bc-155">Выберите и запустите команду **Показать изменения** , чтобы открыть **средство "изменения** " в DevToolsном ящике.</span><span class="sxs-lookup"><span data-stu-id="0d3bc-155">Select and run the **Show Changes** command to open the **Changes tool** in the DevTools drawer.</span></span>  

<span data-ttu-id="0d3bc-156">После внесения изменений в файл minified **инструмент "изменения** " позволяет выполнить горизонтальную прокрутку для просмотра всего кода minified.</span><span class="sxs-lookup"><span data-stu-id="0d3bc-156">When you have made a change to a minified file, the **Changes tool** enables you to scroll horizontally to see all of your minified code.</span></span>  <span data-ttu-id="0d3bc-157">Начиная с Microsoft Edge 83, теперь можно прокручивать по горизонтали с помощью клавиш со стрелками на клавиатуре.</span><span class="sxs-lookup"><span data-stu-id="0d3bc-157">Starting in Microsoft Edge 83, you may now scroll horizontally using the arrow keys on your keyboard.</span></span>  

:::image type="complex" source="../../media/2020/03/changes.msft.png" alt-text="Приложение Remote Tools для Microsoft EDGE (бета-версия), доступное в Microsoft Store" lightbox="../../media/2020/03/changes.msft.png":::
   <span data-ttu-id="0d3bc-159">В Microsoft Edge 83 вы можете выполнить горизонтальную прокрутку с помощью клавиш со стрелками, чтобы просмотреть изменения, внесенные в код minified в **инструменте "изменения** ".</span><span class="sxs-lookup"><span data-stu-id="0d3bc-159">In Microsoft Edge 83, you may scroll horizontally with the arrow keys to see the changes you made to your minified code in the **Changes tool**</span></span>  
:::image-end:::  

<span data-ttu-id="0d3bc-160">Если вы используете средства чтения с экрана или клавиатуру для навигации по DevTools, отправьте нам свой отзыв, выполнив [твит][PostTweetEdgeDevTools] в США или щелкнув значок [Отправить отзыв](#getting-in-touch-with-microsoft-edge-devtools-team) !</span><span class="sxs-lookup"><span data-stu-id="0d3bc-160">If you use screen readers or the keyboard to navigate around the DevTools, send us your feedback by [tweeting][PostTweetEdgeDevTools] at us or clicking the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="0d3bc-161">[#963183][CR963183] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="0d3bc-161">Chromium issue [#963183][CR963183]</span></span>  

## <span data-ttu-id="0d3bc-162">Объявления из проекта Chromium</span><span class="sxs-lookup"><span data-stu-id="0d3bc-162">Announcements from the Chromium project</span></span>  

<span data-ttu-id="0d3bc-163">В следующих разделах описаны дополнительные возможности, доступные в Microsoft Edge 83, которые были задействованы в проекте Open Source Chromium.</span><span class="sxs-lookup"><span data-stu-id="0d3bc-163">The following sections announce additional features available in Microsoft Edge 83 that were contributed to the open source Chromium project.</span></span>  

### <span data-ttu-id="0d3bc-164">Эмуляция видения deficiencies</span><span class="sxs-lookup"><span data-stu-id="0d3bc-164">Emulate vision deficiencies</span></span>  

<span data-ttu-id="0d3bc-165">Откройте [вкладку рендеринг][DevtoolsEvaluatePreformanceReferenceAnalyzeRenderingTab] и воспользуйтесь новой функцией **эмуляции deficiencies** , чтобы лучше понять, как люди с разными типами концепций deficienciesют свой сайт.</span><span class="sxs-lookup"><span data-stu-id="0d3bc-165">Open the [Rendering tab][DevtoolsEvaluatePreformanceReferenceAnalyzeRenderingTab] and use the new **Emulate vision deficiencies** feature to get a better idea of how people with different types of vision deficiencies experience your site.</span></span>  

:::image type="complex" source="../../media/2020/03/vision.msft.png" alt-text="Приложение Remote Tools для Microsoft EDGE (бета-версия), доступное в Microsoft Store" lightbox="../../media/2020/03/vision.msft.png":::
   <span data-ttu-id="0d3bc-167">Имитация размытого видения</span><span class="sxs-lookup"><span data-stu-id="0d3bc-167">Emulating blurred vision</span></span>  
:::image-end:::  

<span data-ttu-id="0d3bc-168">DevTools может эмулировать размытое видение и следующие [типы концепций цветопередачи deficiencies][ColorBlindnessTypes].</span><span class="sxs-lookup"><span data-stu-id="0d3bc-168">DevTools is able to emulate blurred vision and the following [types of color vision deficiencies][ColorBlindnessTypes].</span></span>  

| <span data-ttu-id="0d3bc-169">Некоторая концепция цвета</span><span class="sxs-lookup"><span data-stu-id="0d3bc-169">Color Vision Deficiency</span></span> | <span data-ttu-id="0d3bc-170">Сведения</span><span class="sxs-lookup"><span data-stu-id="0d3bc-170">Details</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="0d3bc-171">Protanopia</span><span class="sxs-lookup"><span data-stu-id="0d3bc-171">Protanopia</span></span> | <span data-ttu-id="0d3bc-172">Невозможность воспринимать красный индикатор.</span><span class="sxs-lookup"><span data-stu-id="0d3bc-172">The inability to perceive any red light.</span></span> |  
| <span data-ttu-id="0d3bc-173">Deuteranopia</span><span class="sxs-lookup"><span data-stu-id="0d3bc-173">Deuteranopia</span></span> | <span data-ttu-id="0d3bc-174">Невозможность воспринимать зеленый свет.</span><span class="sxs-lookup"><span data-stu-id="0d3bc-174">The inability to perceive any green light.</span></span> |  
| <span data-ttu-id="0d3bc-175">Tritanopia</span><span class="sxs-lookup"><span data-stu-id="0d3bc-175">Tritanopia</span></span> | <span data-ttu-id="0d3bc-176">Невозможность воспринимать любой синий индикатор.</span><span class="sxs-lookup"><span data-stu-id="0d3bc-176">The inability to perceive any blue light.</span></span> |  
| <span data-ttu-id="0d3bc-177">Achromatopsia</span><span class="sxs-lookup"><span data-stu-id="0d3bc-177">Achromatopsia</span></span> | <span data-ttu-id="0d3bc-178">Невозможность воспринимать любой цвет, за исключением оттенков серого \ (очень редких).</span><span class="sxs-lookup"><span data-stu-id="0d3bc-178">The inability to perceive any color, except for shades of grey \(extremely rare\).</span></span> |  

<span data-ttu-id="0d3bc-179">Ниже указаны менее экстремальные версии deficiencies, и в действительности они являются более распространенными.</span><span class="sxs-lookup"><span data-stu-id="0d3bc-179">Less extreme versions of these color vision deficiencies exist, and in fact they are more common.</span></span>  
<span data-ttu-id="0d3bc-180">Например, Protanomaly — это уменьшенная чувствительность к красному свету (в отличие от Protanopia, что является полноценным невозможностью воспринимать красный свет).</span><span class="sxs-lookup"><span data-stu-id="0d3bc-180">For example, protanomaly is a reduced sensitivity to red light (as opposed to protanopia, which is the complete inability to perceive red light).</span></span> <span data-ttu-id="0d3bc-181">Тем не менее, omaly концепция deficiencies не так четко: каждый человек, имеющий такой интерес, отличается от того, кто имеет такой же интерес, и может по-разному видеть различные варианты (которые могут выпустить больше или меньше подходящих цветов).</span><span class="sxs-lookup"><span data-stu-id="0d3bc-181">However, these -omaly vision deficiencies are not as clearly defined: every person with such a vision deficiency is different and might see things differently (being able to perceive more/less of the relevant colors).</span></span>  

<span data-ttu-id="0d3bc-182">Благодаря разработке для более экстремальных эмуляций в DevTools веб-приложения будут гарантированно доступны людям с protanomaly, Deuteranomaly, Tritanomaly и achromatomaly.</span><span class="sxs-lookup"><span data-stu-id="0d3bc-182">By designing for the more extreme simulations in DevTools, your web apps are guaranteed to be accessible to people with protanomaly, deuteranomaly, tritanomaly, and achromatomaly as well.</span></span>  

<span data-ttu-id="0d3bc-183">Отправьте отзыв, выполнив [твит][PostTweetEdgeDevTools] или щелкнув значок " [Отправить отзыв](#getting-in-touch-with-microsoft-edge-devtools-team) "!</span><span class="sxs-lookup"><span data-stu-id="0d3bc-183">Send your feedback by [tweeting][PostTweetEdgeDevTools] or clicking the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="0d3bc-184">[#1003700][CR1003700] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="0d3bc-184">Chromium issue [#1003700][CR1003700]</span></span>  

### <span data-ttu-id="0d3bc-185">Эмуляция языков</span><span class="sxs-lookup"><span data-stu-id="0d3bc-185">Emulate locales</span></span>  

<span data-ttu-id="0d3bc-186">Эмуляция региональных стандартов путем задания местоположения в **Sensors**  >  **расположениях**датчиков.</span><span class="sxs-lookup"><span data-stu-id="0d3bc-186">Emulate locales by setting a location in **Sensors** > **Location**.</span></span> <span data-ttu-id="0d3bc-187">[Открыть **меню команд** ][DevToolsCommandMenuIndex] и ввести текст `Sensors` для доступа к вкладке **Sensors (датчики** ).  После выполнения этих действий DevTools изменяет текущий языковой стандарт по умолчанию, влияя на приведенный ниже код.</span><span class="sxs-lookup"><span data-stu-id="0d3bc-187">[Open the **Command Menu**][DevToolsCommandMenuIndex] and type `Sensors` to access the **Sensors** tab.  After performing these actions, DevTools modifies the current default locale, affecting the following code.</span></span>  

*   `Intl.*` <span data-ttu-id="0d3bc-188">API, например:</span><span class="sxs-lookup"><span data-stu-id="0d3bc-188">APIs, for example:</span></span> `new Intl.NumberFormat().resolvedOptions().locale`  
*   <span data-ttu-id="0d3bc-189">Другие API JavaScript, поддерживающие национальные настройки `String.prototype.localeCompare` , такие как и `*.prototype.toLocaleString` , например:</span><span class="sxs-lookup"><span data-stu-id="0d3bc-189">Other locale-aware JavaScript APIs such as `String.prototype.localeCompare` and `*.prototype.toLocaleString`, for example:</span></span> `123_456..toLocaleString()`  
*   <span data-ttu-id="0d3bc-190">API DOM, например `navigator.language` и</span><span class="sxs-lookup"><span data-stu-id="0d3bc-190">DOM APIs such as `navigator.language` and</span></span> `navigator.languages`  
*   <span data-ttu-id="0d3bc-191">Заголовок HTTP-запроса для [приема на языке][MDNAcceptLanguage]</span><span class="sxs-lookup"><span data-stu-id="0d3bc-191">The [Accept-Language][MDNAcceptLanguage] HTTP request header</span></span>  

> [!NOTE]
> <span data-ttu-id="0d3bc-192">Обновляются `navigator.language` и `navigator.languages` не отображаются немедленно, но только после следующей навигации или обновления страницы.</span><span class="sxs-lookup"><span data-stu-id="0d3bc-192">Updates to `navigator.language` and `navigator.languages` are not visible immediately, but only after the next navigation or page refresh.</span></span>  <span data-ttu-id="0d3bc-193">Изменения в `Accept-Language` заголовке HTTP отражаются только для последующих запросов.</span><span class="sxs-lookup"><span data-stu-id="0d3bc-193">Changes to the `Accept-Language` HTTP header are only reflected for subsequent requests.</span></span>  

:::image type="complex" source="../../media/2020/03/locale.msft.png" alt-text="Приложение Remote Tools для Microsoft EDGE (бета-версия), доступное в Microsoft Store" lightbox="../../media/2020/03/locale.msft.png":::
   <span data-ttu-id="0d3bc-195">Эмуляция языкового стандарта</span><span class="sxs-lookup"><span data-stu-id="0d3bc-195">Emulating a locale</span></span>  
:::image-end:::  

<span data-ttu-id="0d3bc-196">Чтобы попробовать посмотреть демонстрацию, ознакомьтесь с [примером кода, зависящим от языкового стандарта][MathiasByensLocaleDemo].</span><span class="sxs-lookup"><span data-stu-id="0d3bc-196">To try a demo, see [Locale-dependent code example][MathiasByensLocaleDemo].</span></span>

<span data-ttu-id="0d3bc-197">[#1051822][CR1051822] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="0d3bc-197">Chromium issue [#1051822][CR1051822]</span></span>

### <span data-ttu-id="0d3bc-198">Отладка политики встраивания по началу (COEP)</span><span class="sxs-lookup"><span data-stu-id="0d3bc-198">Cross-Origin Embedder Policy (COEP) debugging</span></span>  

<span data-ttu-id="0d3bc-199">На панели Network (сеть) теперь представлена отладочная информация о [политике встраивания][COEP] .</span><span class="sxs-lookup"><span data-stu-id="0d3bc-199">The Network panel now provides [Cross-Origin Embedder Policy][COEP] debugging information.</span></span>  

<span data-ttu-id="0d3bc-200">Столбец **Status** теперь содержит краткое описание причины блокировки запроса, а также ссылку на просмотр заголовков этого запроса для дальнейшей отладки.</span><span class="sxs-lookup"><span data-stu-id="0d3bc-200">The **Status** column now provides a quick explanation of why a request was blocked as well as a link to view the headers of that request for further debugging:</span></span>  

:::image type="complex" source="../../media/2020/03/status.msft.png" alt-text="Приложение Remote Tools для Microsoft EDGE (бета-версия), доступное в Microsoft Store" lightbox="../../media/2020/03/status.msft.png":::
   <span data-ttu-id="0d3bc-202">Заблокированные запросы в столбце " **состояние** "</span><span class="sxs-lookup"><span data-stu-id="0d3bc-202">Blocked requests in the **Status** column</span></span>  
:::image-end:::  

<span data-ttu-id="0d3bc-203">В разделе **заголовки ответа** вкладки **заголовки** содержатся дополнительные инструкции по устранению проблем.</span><span class="sxs-lookup"><span data-stu-id="0d3bc-203">The **Response Headers** section of the **Headers** tab provides more guidance on how to resolve the issues:</span></span>  

:::image type="complex" source="../../media/2020/03/guidance.msft.png" alt-text="Приложение Remote Tools для Microsoft EDGE (бета-версия), доступное в Microsoft Store" lightbox="../../media/2020/03/guidance.msft.png":::
   <span data-ttu-id="0d3bc-205">Другие рекомендации в разделе " **заголовки ответа** "</span><span class="sxs-lookup"><span data-stu-id="0d3bc-205">More guidance in the **Response Headers** section</span></span>  
:::image-end:::  

<span data-ttu-id="0d3bc-206">Отправьте отзыв, выполнив [твит][PostTweetEdgeDevTools] или щелкнув значок " [Отправить отзыв](#getting-in-touch-with-microsoft-edge-devtools-team) "!</span><span class="sxs-lookup"><span data-stu-id="0d3bc-206">Send your feedback by [tweeting][PostTweetEdgeDevTools] or clicking the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="0d3bc-207">[#1051466][CR1051466] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="0d3bc-207">Chromium issue [#1051466][CR1051466]</span></span>  

### <span data-ttu-id="0d3bc-208">Новые значки для точек останова, условных точек останова и logpoints</span><span class="sxs-lookup"><span data-stu-id="0d3bc-208">New icons for breakpoints, conditional breakpoints, and logpoints</span></span>  

<span data-ttu-id="0d3bc-209">На панели «источники» есть новые значки для точек останова, условных точек останова и logpoints:</span><span class="sxs-lookup"><span data-stu-id="0d3bc-209">The Sources panel has new icons for breakpoints, conditional breakpoints, and logpoints:</span></span>  

*   <span data-ttu-id="0d3bc-210">Точки останова \ (</span><span class="sxs-lookup"><span data-stu-id="0d3bc-210">Breakpoints \(</span></span>![Точкой](../../media/2020/03/breakpoint.msft.png)<span data-ttu-id="0d3bc-212">\) представлены красными кружками.</span><span class="sxs-lookup"><span data-stu-id="0d3bc-212">\) are represented by red circles.</span></span>  
*   <span data-ttu-id="0d3bc-213">Условные точки останова \ (</span><span class="sxs-lookup"><span data-stu-id="0d3bc-213">Conditional Breakpoints \(</span></span>![Условная точка останова](../../media/2020/03/conditional.msft.png)<span data-ttu-id="0d3bc-215">\) представлены в виде кружков из половины белых.</span><span class="sxs-lookup"><span data-stu-id="0d3bc-215">\) are represented by half-red half-white circles.</span></span>  
*   <span data-ttu-id="0d3bc-216">Logpoints \(</span><span class="sxs-lookup"><span data-stu-id="0d3bc-216">Logpoints \(</span></span>![Logpoint](../../media/2020/03/logpoint.msft.png)<span data-ttu-id="0d3bc-218">\) представлены красными кружками с помощью значков консоли.</span><span class="sxs-lookup"><span data-stu-id="0d3bc-218">\) are represented by red circles with Console icons.</span></span>  

<span data-ttu-id="0d3bc-219">Мотивация для новых значков — сделать пользовательский интерфейс более подродным с помощью других средств отладки графического интерфейса (обычно это цветовые точки останова), чтобы облегчить различение трех функций.</span><span class="sxs-lookup"><span data-stu-id="0d3bc-219">The motivation for the new icons was to make the UI more consistent with other GUI debugging tools \(which usually color breakpoints red\) and to make it easier to distinguish between the 3 features at a glance.</span></span>  

<span data-ttu-id="0d3bc-220">[#1041830][CR1041830] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="0d3bc-220">Chromium issue [#1041830][CR1041830]</span></span>  

### <span data-ttu-id="0d3bc-221">Просмотр сетевых запросов, заданных для определенного пути к файлу cookie</span><span class="sxs-lookup"><span data-stu-id="0d3bc-221">View network requests that set a specific cookie path</span></span>  

<span data-ttu-id="0d3bc-222">С помощью нового `cookie-path` ключевого слова фильтра на панели **Network (сеть** ) можно сосредоточиться на запросах в сети, которые задают определенный [путь к файлу cookie][MDNCookiePath].</span><span class="sxs-lookup"><span data-stu-id="0d3bc-222">Use the new `cookie-path` filter keyword in the **Network** panel to focus on the network requests that set a specific [cookie path][MDNCookiePath].</span></span>  

<span data-ttu-id="0d3bc-223">Изучите [запросы фильтра по свойствам][DevtoolsNetworkReferenceFilterRequestsProperties] , чтобы найти другие ключевые слова, такие как `cookie-path` .</span><span class="sxs-lookup"><span data-stu-id="0d3bc-223">Check out [Filter requests by properties][DevtoolsNetworkReferenceFilterRequestsProperties] to discover more keywords like `cookie-path`.</span></span>

### <span data-ttu-id="0d3bc-224">Закрепить слева от меню команд</span><span class="sxs-lookup"><span data-stu-id="0d3bc-224">Dock to left from the Command Menu</span></span>  

<span data-ttu-id="0d3bc-225">Откройте [меню команд][DevToolsCommandMenuIndex] и выполните команду, `Dock to left` чтобы переместить DevTools в левой части окна просмотра.</span><span class="sxs-lookup"><span data-stu-id="0d3bc-225">Open the [Command Menu][DevToolsCommandMenuIndex] and run the `Dock to left` command to move DevTools to the left of your viewport.</span></span>  

:::image type="complex" source="../../media/2020/03/dock-to-left.msft.png" alt-text="Приложение Remote Tools для Microsoft EDGE (бета-версия), доступное в Microsoft Store" lightbox="../../media/2020/03/dock-to-left.msft.png":::
   <span data-ttu-id="0d3bc-227">DevTools закреплен в левой части окна просмотра</span><span class="sxs-lookup"><span data-stu-id="0d3bc-227">DevTools docked to the left of the viewport</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="0d3bc-228">Функция " **прикрепить к левому краю** " была доступна после выпуска Microsoft Edge 75, но ранее она была доступна только в [главном меню][DevtoolsCustomizePlacementsChangeMainMenu].</span><span class="sxs-lookup"><span data-stu-id="0d3bc-228">The **Dock to left** feature has been available since Microsoft Edge 75, but it was previously only accessible from the [Main Menu][DevtoolsCustomizePlacementsChangeMainMenu].</span></span>  <span data-ttu-id="0d3bc-229">Новая функция в Microsoft Edge 83 — теперь вы можете получить доступ к этой функции в меню команд.</span><span class="sxs-lookup"><span data-stu-id="0d3bc-229">The new feature in Microsoft Edge 83 is that you may now access this feature from the Command Menu.</span></span>  

<span data-ttu-id="0d3bc-230">Отправьте отзыв, выполнив [твит][PostTweetEdgeDevTools] или щелкнув значок " [Отправить отзыв](#getting-in-touch-with-microsoft-edge-devtools-team) "!</span><span class="sxs-lookup"><span data-stu-id="0d3bc-230">Send your feedback by [tweeting][PostTweetEdgeDevTools] or clicking the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="0d3bc-231">[#1011679][CR1011679] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="0d3bc-231">Chromium issue [#1011679][CR1011679]</span></span>  

### <span data-ttu-id="0d3bc-232">Панель "Аудит" теперь является панелью Lighthouse</span><span class="sxs-lookup"><span data-stu-id="0d3bc-232">The Audits panel is now the Lighthouse panel</span></span>  

<span data-ttu-id="0d3bc-233">Группа DevTools часто получила отзыв от веб-разработчиков, которые могли бы запустить [Lighthouse][GithubGoogleChromeLighthouse] из DevTools, когда они могли бы не найти панель "Lighthouse", и панель **аудиторий** стала на панели " **Lighthouse** ".</span><span class="sxs-lookup"><span data-stu-id="0d3bc-233">The DevTools team frequently got feedback from web developers that while it was possible to run [Lighthouse][GithubGoogleChromeLighthouse] from DevTools, when they tried it out they were not able to find the "Lighthouse" panel, so the **Audits** panel is now the **Lighthouse** panel.</span></span>  

:::image type="complex" source="../../media/2020/03/lighthouse.msft.png" alt-text="Приложение Remote Tools для Microsoft EDGE (бета-версия), доступное в Microsoft Store" lightbox="../../media/2020/03/lighthouse.msft.png":::
   <span data-ttu-id="0d3bc-235">Панель Lighthouse</span><span class="sxs-lookup"><span data-stu-id="0d3bc-235">The Lighthouse panel</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="0d3bc-236">Панель **Lighthouse** содержит ссылки на содержимое, размещенное на сторонних веб-сайтах.</span><span class="sxs-lookup"><span data-stu-id="0d3bc-236">The **Lighthouse** panel provides links to content hosted on third-party websites.</span></span>  <span data-ttu-id="0d3bc-237">Корпорация Майкрософт не несет ответственности за содержимое этих сайтов и любые данные, которые могут быть собраны, и не может управлять ими.</span><span class="sxs-lookup"><span data-stu-id="0d3bc-237">Microsoft is not responsible for and has no control over the content of these sites and any data they may collect.</span></span>  

### <span data-ttu-id="0d3bc-238">Удаление всех локальных переопределений в папке</span><span class="sxs-lookup"><span data-stu-id="0d3bc-238">Delete all Local Overrides in a folder</span></span>  

<span data-ttu-id="0d3bc-239">После настройки **локальных переопределений** вы можете щелкнуть папку правой кнопкой мыши и выбрать команду создать **все переопределение** для удаления всех локальных переопределений в этой папке.</span><span class="sxs-lookup"><span data-stu-id="0d3bc-239">After setting up **Local Overrides** you may right-click a folder and select the new **Delete all overrides** option to delete all Local Overrides in that folder.</span></span>  

:::image type="complex" source="../../media/2020/03/overrides.msft.png" alt-text="Приложение Remote Tools для Microsoft EDGE (бета-версия), доступное в Microsoft Store" lightbox="../../media/2020/03/overrides.msft.png":::
   <span data-ttu-id="0d3bc-241">Удаление всех переопределений</span><span class="sxs-lookup"><span data-stu-id="0d3bc-241">Delete all overrides</span></span>  
:::image-end:::  

<span data-ttu-id="0d3bc-242">Отправьте отзыв, выполнив [твит][PostTweetEdgeDevTools] или щелкнув значок " [Отправить отзыв](#getting-in-touch-with-microsoft-edge-devtools-team) "!</span><span class="sxs-lookup"><span data-stu-id="0d3bc-242">Send your feedback by [tweeting][PostTweetEdgeDevTools] or clicking the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="0d3bc-243">[#1016501][CR1016501] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="0d3bc-243">Chromium issue [#1016501][CR1016501]</span></span>  

### <span data-ttu-id="0d3bc-244">Обновленный пользовательский интерфейс длительных задач</span><span class="sxs-lookup"><span data-stu-id="0d3bc-244">Updated Long tasks UI</span></span>  

<span data-ttu-id="0d3bc-245">**Длинная задача** — это код JavaScript, который занимает много времени, что приводит к закреплениям веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="0d3bc-245">A **Long Task** is JavaScript code that monopolizes the main thread for a long time, causing a web page to freeze.</span></span>  

<span data-ttu-id="0d3bc-246">На панели производительности вы можете [визуализировать длинные задачи][DevtoolsEvaluatePerformanceReferenceViewMainThreadActivity] , но в Microsoft Edge 83 пользовательский интерфейс визуализации задач на панели производительности обновлен.</span><span class="sxs-lookup"><span data-stu-id="0d3bc-246">You have been able to [visualize Long Tasks in the Performance panel][DevtoolsEvaluatePerformanceReferenceViewMainThreadActivity] for a while now, but in Microsoft Edge 83 the Long Task visualization UI in the Performance panel has been updated.</span></span>  <span data-ttu-id="0d3bc-247">Область задач "Долгая задача" теперь окрашена на красный фон с чередованием.</span><span class="sxs-lookup"><span data-stu-id="0d3bc-247">The Long Task portion of a task is now colored with a striped red background.</span></span>  

:::image type="complex" source="../../media/2020/03/long-task.msft.png" alt-text="Приложение Remote Tools для Microsoft EDGE (бета-версия), доступное в Microsoft Store" lightbox="../../media/2020/03/long-task.msft.png":::
   <span data-ttu-id="0d3bc-249">Новый пользовательский интерфейс длительной задачи</span><span class="sxs-lookup"><span data-stu-id="0d3bc-249">The new Long Task UI</span></span>  
:::image-end:::  

<span data-ttu-id="0d3bc-250">Отправьте отзыв, выполнив [твит][PostTweetEdgeDevTools] или щелкнув значок " [Отправить отзыв](#getting-in-touch-with-microsoft-edge-devtools-team) "!</span><span class="sxs-lookup"><span data-stu-id="0d3bc-250">Send your feedback by [tweeting][PostTweetEdgeDevTools] or clicking the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="0d3bc-251">[#1054447][CR1054447] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="0d3bc-251">Chromium issue [#1054447][CR1054447]</span></span>  

### <span data-ttu-id="0d3bc-252">Поддержка маскированных значков в области манифеста</span><span class="sxs-lookup"><span data-stu-id="0d3bc-252">Maskable icon support in the Manifest pane</span></span>  

<span data-ttu-id="0d3bc-253">В Oreo Android появились адаптивные значки, которые отображают значки приложений в различных моделях устройств.</span><span class="sxs-lookup"><span data-stu-id="0d3bc-253">Android Oreo introduced adaptive icons, which display app icons in a variety of shapes across different device models.</span></span>  <span data-ttu-id="0d3bc-254">**Маскированные значки** — это новый формат значков, поддерживающий адаптивные значки, которые позволяют убедиться, что на устройствах, поддерживающих стандарт маскированных значков, будет хорошо выглядеть значок [PWA][PprgressiveWebAppsChromiumIndex] .</span><span class="sxs-lookup"><span data-stu-id="0d3bc-254">**Maskable icons** are a new icon format that support adaptive icons, which enable you to ensure that your [PWA][PprgressiveWebAppsChromiumIndex] icon looks good on devices that support the maskable icons standard.</span></span>  

<span data-ttu-id="0d3bc-255">Установите флажок **Показывать только минимальную безопасную область для маскированных значков** в области **манифеста** , чтобы убедиться в том, что маскирующий значок хорошо подходит для устройств с Android Oreo.</span><span class="sxs-lookup"><span data-stu-id="0d3bc-255">Enable the new **Show only the minimum safe area for maskable icons** checkbox in the **Manifest** pane to check that your maskable icon looks good on Android Oreo devices.</span></span>  

<!-- Check out [Are my current icons ready?] to learn more.  -->  

:::image type="complex" source="../../media/2020/03/maskable-icons.msft.png" alt-text="Приложение Remote Tools для Microsoft EDGE (бета-версия), доступное в Microsoft Store" lightbox="../../media/2020/03/maskable-icons.msft.png":::
   <span data-ttu-id="0d3bc-257">Флажок **Показать только минимальную безопасную область для маскированных значков**</span><span class="sxs-lookup"><span data-stu-id="0d3bc-257">The **Show only the minimum safe area for maskable icons** checkbox</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="0d3bc-258">Этот компонент запущен в Microsoft Edge 81.</span><span class="sxs-lookup"><span data-stu-id="0d3bc-258">This feature launched in Microsoft Edge 81.</span></span>  <span data-ttu-id="0d3bc-259">Обновления, описанные здесь в Microsoft Edge 83, не были освещены в статье [новые возможности DevTools (Microsoft Edge 81)][WhatsNew81].</span><span class="sxs-lookup"><span data-stu-id="0d3bc-259">The updates covered here in Microsoft Edge 83 were not covered in [What's New In DevTools (Microsoft Edge 81)][WhatsNew81].</span></span>  

## <span data-ttu-id="0d3bc-260">Загрузка каналов предварительной версии Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="0d3bc-260">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="0d3bc-261">Если вы используете Windows или macOS, рассматривайте в качестве браузера по умолчанию использование [каналов предварительного просмотра Microsoft Edge][MicrosoftEdgePreviewChannels] .</span><span class="sxs-lookup"><span data-stu-id="0d3bc-261">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="0d3bc-262">Каналы предварительного просмотра предоставляют доступ к последним функциям DevTools.</span><span class="sxs-lookup"><span data-stu-id="0d3bc-262">The preview channels give you access to the latest DevTools features.</span></span>  

## <span data-ttu-id="0d3bc-263">Знакомство с Microsoft Edge DevTools Team</span><span class="sxs-lookup"><span data-stu-id="0d3bc-263">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[WhatsNew81]: ../01/devtools.md "Новые возможности DevTools (Microsoft Edge 81) | Документы Microsoft"  

[DevToolsCommandMenuIndex]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Выполнение команд с помощью командного меню Microsoft Edge DevTools | Документы Microsoft"  
[DevtoolsCssReferenceColorPicker]: /microsoft-edge/devtools-guide-chromium/css/reference#change-colors-with-the-color-picker "Изменение цвета с помощью средства выбора цвета | Документы Microsoft"  
[DevtoolsCssIndex]: /microsoft-edge/devtools-guide-chromium/css/index "Начало просмотра и изменения CSS | Документы Microsoft"  
[DevtoolsCustomizePlacementsChangeMainMenu]: /microsoft-edge/devtools-guide-chromium/customize/placement#change-placement-from-the-main-menu "Изменение положения в главном меню | Документы Microsoft"  
[DevtoolsEvaluatePerformanceReferenceViewMainThreadActivity]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#view-main-thread-activity "Просмотр основного действия потока | Документы Microsoft"  
[DevtoolsEvaluatePreformanceReferenceAnalyzeRenderingTab]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#analyze-rendering-performance-with-the-rendering-tab "Анализ производительности отрисовки с помощью вкладки "рендеринг" | Документы Microsoft"  
[PprgressiveWebAppsChromiumIndex]: /microsoft-edge/progressive-web-apps-chromium/index "Прогрессивные веб-приложения в Windows | Документы Microsoft"  
[DevtoolsRemoteDebuggingWindows]: /microsoft-edge/devtools-guide-chromium/remote-debugging/windows "Начало работы с удаленной отладкой на устройствах с Windows 10 | Документы Microsoft"  
[DevtoolsJavascriptBreakpointsLineCode]: /microsoft-edge/devtools-guide-chromium/javascript/breakpoints#line-of-code-breakpoints "Точки останова по строке кода: как приостановить выполнение кода с точки останова в Microsoft Edge DevTools | Документы Microsoft"
[DevtoolsNetworkReferenceFilterRequestsProperties]: /microsoft-edge/devtools-guide-chromium/network/reference#filter-requests-by-properties "Фильтрация запросов по свойствам-Справка по анализу сети | Документы Microsoft"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Параметры: Настройка Microsoft Edge DevTools | Документы Microsoft"  

[WindowsUwpDebugTestPerfDevicePortal]: /windows/uwp/debug-test-perf/device-portal "Общие сведения о портале устройств Windows"  

[RemoteTools]: https://www.microsoft.com/store/apps/9P6CMFV44ZLT "Удаленные инструменты для Microsoft EDGE (бета-версия)"  
[MicrosoftStore]: https://www.microsoft.com/store/apps/windows "Microsoft Store"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Каналы предварительной версии Microsoft Edge"  

[WindowsBlogStableRelease]: https://blogs.windows.com/msedgedev/2020/03/20 "Обновление в стабильных выпусках канала для Microsoft Edge"  

[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=[DevTools%20Docs%20Feedback] "Новая ошибка — MicrosoftDocs/Edge-разработчик-GitHub"  

[MicrosoftVisualstudio]: https://visualstudio.microsoft.com "Visual Studio"  

[VisualstudioCode]: https://code.visualstudio.com "Код Visual Studio"  

[PostTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Публикация твита"  
[EdgeDevToolsTwitterAccount]: https://twitter.com/EdgeDevTools "@EdgeDevTools учетной записи Twitter"  
[TheWebWeWant]: https://webwewant.fyi "Требуемый веб-сайт"  

[ColorBlindnessTypes]: http://www.colourblindawareness.org/colour-blindness/types-of-colour-blindness "Типы цветовой жалюзи"  

[MDNAcceptLanguage]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Accept-Language "Одобрение-язык | MDN"  
[MDNCookiePath]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie#Directives "Set-cookie | MDN"  

[MathiasByensLocaleDemo]: https://mathiasbynens.be/demo/locale "Пример кода, зависящий от языкового стандарта"  

[CR963183]: https://crbug.com/963183 "Ошибка 963183: DevTools не соответствует требованиям WCAG"  
[CR1003700]: https://crbug.com/1003700 "Вопрос 1003700: Добавление поддержки DevTools в целях моделирования недостатков для представления цвета"  
[CR1011679]: https://crbug.com/1011679 "Ошибка 1011679: ввод "закрепить влево" с помощью меню команд"  
[CR1016501]: https://crbug.com/1016501 "Ошибка 1016501: запрос компонента: кнопка для удаления всех локальных переопределений"  
[CR1050999]: https://crbug.com/1050999 "Ошибка 1050999: вкладка "Свойства""  
[CR1051466]: https://crbug.com/1051466 "Ошибка 1051466: поддержка отладки COOP/COEP в DevTools"  
[CR1054447]: https://crbug.com/1054447 "Ошибка 1054447: обновление метрик производительности на временной шкале DevTools"  
[CR1051822]: https://crbug.com/1051822 "Ошибка 1051822: DevTools: Добавление пользовательского интерфейса для эмуляции национальной настройки"
[CR1041830]: https://crbug.com/1041830 "Ошибка 1041830: улучшение цветопередачи для точек останова"
[CR1050855]: https://crbug.com/1050855 "Неполадка 1050855: Просмотр параметров затрудняет обнаружение"
[CR1056348]: https://crbug.com/1056348 "Ошибка 1056348: обновление компонента на информационной панели"

[COOP]: https://docs.google.com/document/d/1zDlfvfTJ_9e8Jdc8ehuV4zMEu9ySMCiTGMS9y0GU92k/edit#bookmark=id.tu4hyy6v12wn "Описание COOP и COEP — политика opener для разных источников"  
[COEP]: https://docs.google.com/document/d/1zDlfvfTJ_9e8Jdc8ehuV4zMEu9ySMCiTGMS9y0GU92k/edit#bookmark=id.uo6kivyh0ge2 "Объяснение COOP и COEP — политика для внедрения разных источников"  

[GithubGoogleChromeLighthouse]: https://github.com/GoogleChrome/lighthouse "Lighthouse | GitHub"  

> [!NOTE]
> <span data-ttu-id="0d3bc-305">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="0d3bc-305">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="0d3bc-306">Исходная страница будет найдена [здесь](https://developers.google.com/web/updates/2020/03/devtools/index) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="0d3bc-306">The original page is found [here](https://developers.google.com/web/updates/2020/03/devtools/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="0d3bc-308">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="0d3bc-308">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
