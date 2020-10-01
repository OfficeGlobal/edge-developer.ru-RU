---
description: Соответствие сочетаний клавиш для кода Visual Studio, Эмуляция Surface Duo и Samsung Galaxy сгиб, улучшения каскадных таблиц стилей и т. д.
title: Новые возможности DevTools (Microsoft Edge 86)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/08/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 943eca7e73385513b264feb74ec37c450d5c5a2f
ms.sourcegitcommit: 6b577cb118f34f3ff2c65eab2908b65f155dc151
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/09/2020
ms.locfileid: "11004228"
---
# <span data-ttu-id="e445b-104">Новые возможности DevTools (Microsoft Edge 86)</span><span class="sxs-lookup"><span data-stu-id="e445b-104">What's New In DevTools (Microsoft Edge 86)</span></span>  

## <span data-ttu-id="e445b-105">Объявления из группы Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="e445b-105">Announcements from the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

### <span data-ttu-id="e445b-106">Соответствие сочетаний клавиш в DevTools с кодом Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e445b-106">Match keyboard shortcuts in DevTools to Visual Studio Code</span></span>  

<span data-ttu-id="e445b-107">В Microsoft Edge 86 вы можете использовать сочетания клавиш в DevTools для сочетаний клавиш в [коде Visual Studio][VisualStudioCode].</span><span class="sxs-lookup"><span data-stu-id="e445b-107">In Microsoft Edge 86, you may match keyboard shortcuts in the DevTools to your shortcuts in [Visual Studio Code][VisualStudioCode].</span></span> 

:::image type="complex" source="../../media/2020/08/keyboard-shortcut.msft.png" alt-text="Соответствие сочетаний клавиш в DevTools с кодом Visual Studio" lightbox="../../media/2020/08/keyboard-shortcut.msft.png":::
   <span data-ttu-id="e445b-109">Соответствие сочетаний клавиш в DevTools с кодом Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e445b-109">Match keyboard shortcuts in the DevTools to Visual Studio Code</span></span>  
:::image-end:::  

<span data-ttu-id="e445b-110">Для активации этой функции перейдите в [раздел Настройка сочетаний клавиш в Microsoft Edge DevTools][DevtoolsCustomizeShortcuts].</span><span class="sxs-lookup"><span data-stu-id="e445b-110">To activate this feature, navigate to [Customize keyboard shortcuts in the Microsoft Edge DevTools][DevtoolsCustomizeShortcuts].</span></span>  

<span data-ttu-id="e445b-111">Например, с помощью сочетания клавиш можно приостановить или продолжить выполнение сценария в [Visual Studio][VisualStudioCodeShortcutsKeyboardWindows] `F5` .</span><span class="sxs-lookup"><span data-stu-id="e445b-111">For example, the keyboard shortcut for pausing or continuing running a script in [Visual Studio Code][VisualStudioCodeShortcutsKeyboardWindows] is `F5`.</span></span>  <span data-ttu-id="e445b-112">В стиле **DevTools (по умолчанию)** это тот же ярлык в DevTools `F8` , но если вы выбрали стиль **кода Visual Studio** , это сочетание клавиш также будет использоваться `F5` .</span><span class="sxs-lookup"><span data-stu-id="e445b-112">With the **DevTools (Default)** preset, that same shortcut in the DevTools is `F8`, but when you choose the **Visual Studio Code** preset, that shortcut is now also `F5`.</span></span>  

<span data-ttu-id="e445b-113">[#174309][CR174309] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="e445b-113">Chromium issue [#174309][CR174309]</span></span>  

### <span data-ttu-id="e445b-114">Эмуляция Surface Duo и Samsung Galaxy сгиб</span><span class="sxs-lookup"><span data-stu-id="e445b-114">Emulate Surface Duo and Samsung Galaxy Fold</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Соответствие сочетаний клавиш в DevTools с кодом Visual Studio":::
   <span data-ttu-id="e445b-116">Экспериментальная функция</span><span class="sxs-lookup"><span data-stu-id="e445b-116">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="e445b-117">Теперь вы можете проверить внешний вид и функции вашего веб-сайта или приложения на двух новых устройствах:  [Surface Duo][MicrosoftSurfaceDevicesDuo] и [Samsung Galaxy сгиб][SamsungMobileGalaxyFold] в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="e445b-117">You are now able to test the look and feel of your website or app on two new devices:  [Surface Duo][MicrosoftSurfaceDevicesDuo] and [Samsung Galaxy Fold][SamsungMobileGalaxyFold] in Microsoft Edge.</span></span>  

<span data-ttu-id="e445b-118">Чтобы повысить качество веб-сайта или приложения для двойного экрана и складная устройств, используйте следующие возможности при [эмуляции устройства][DevtoolsDeviceModeIndex].</span><span class="sxs-lookup"><span data-stu-id="e445b-118">To help enhance your website or app for the dual-screen and foldable devices, use the following features when [emulating the device][DevtoolsDeviceModeIndex].</span></span>  

*   <span data-ttu-id="e445b-119">[Объединение][DevtoolsExperimentalFeaturesTestingOnFoldableDualScreenDevices], которое появляется, когда ваш веб-сайт (или приложение \) отображается на обоих экранах.</span><span class="sxs-lookup"><span data-stu-id="e445b-119">[Spanning][DevtoolsExperimentalFeaturesTestingOnFoldableDualScreenDevices], which is when your website \(or app\) appears across both screens.</span></span>
*   <span data-ttu-id="e445b-120">[Отрисовка стыка][DualScreenIntroductionHowWorkSeam], то есть расстояния между двумя экранами.</span><span class="sxs-lookup"><span data-stu-id="e445b-120">[Rendering the seam][DualScreenIntroductionHowWorkSeam], which is the space between the two screens.</span></span>
*   <span data-ttu-id="e445b-121">[Включение API экспериментальной веб-платформы][DevtoolsExperimentalFeaturesEnableExperimentalApis] для доступа к новой [функции многофункционального экрана CSS][DualScreenWebCssMediaSpanning] и [API JavaScript getWindowSegments][DualScreenWebJavascriptGetwindowsegments].</span><span class="sxs-lookup"><span data-stu-id="e445b-121">[Enabling experimental Web Platform APIs][DevtoolsExperimentalFeaturesEnableExperimentalApis] to access the new [CSS media screen-spanning feature][DualScreenWebCssMediaSpanning] and [JavaScript getWindowSegments API][DualScreenWebJavascriptGetwindowsegments].</span></span>  

:::image type="complex" source="../../media/2020/08/surface-duo-device-emulation.msft.png" alt-text="Соответствие сочетаний клавиш в DevTools с кодом Visual Studio" lightbox="../../media/2020/08/surface-duo-device-emulation.msft.png":::
   <span data-ttu-id="e445b-123">Эмуляция устройства для ИБП Surface Duo</span><span class="sxs-lookup"><span data-stu-id="e445b-123">Device emulation for Surface Duo</span></span>  
:::image-end:::  

<span data-ttu-id="e445b-124">Чтобы включить эту функцию, перейдите к разделу [Включение экспериментальных функций][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] и установите флажок рядом с параметром **Эмуляция: поддержка двух режимов экрана**.</span><span class="sxs-lookup"><span data-stu-id="e445b-124">To turn on this experimental feature, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] and choose the checkbox next to **Emulation: Support dual screen mode**.</span></span>  

<span data-ttu-id="e445b-125">Дополнительные сведения об этом эксперименте можно найти в разделе [Эмуляция: поддержка двух режимов экрана][DevtoolsExperimentalFeaturesEmulationSupportDualScreenMode].</span><span class="sxs-lookup"><span data-stu-id="e445b-125">For more information about this experiment, navigate to [Emulation: Support dual screen mode][DevtoolsExperimentalFeaturesEmulationSupportDualScreenMode].</span></span>  

<span data-ttu-id="e445b-126">Ошибка Chromium: [#1054281][CR1054281]</span><span class="sxs-lookup"><span data-stu-id="e445b-126">Chromium issue: [#1054281][CR1054281]</span></span>  

### <span data-ttu-id="e445b-127">Усовершенствования каскадных наложений сетки CSS и новые возможности экспериментальной сетки</span><span class="sxs-lookup"><span data-stu-id="e445b-127">CSS grid overlay improvements and new experimental grid features</span></span>  

<span data-ttu-id="e445b-128">Благодарим вас за позитивную обратную связь об улучшенных наложения сетки CSS.</span><span class="sxs-lookup"><span data-stu-id="e445b-128">Thank you for the positive feedback about the improved CSS grid overlays.</span></span>  <span data-ttu-id="e445b-129">Наложения сетки CSS теперь включены по умолчанию и не требуют включения эксперимента.</span><span class="sxs-lookup"><span data-stu-id="e445b-129">The CSS grid overlays are now enabled by default and do not require you to turn on an experiment.</span></span>  

:::image type="complex" source="../../media/2020/08/css-grid-overlay-article.msft.png" alt-text="Соответствие сочетаний клавиш в DevTools с кодом Visual Studio" lightbox="../../media/2020/08/css-grid-overlay-article.msft.png":::
   <span data-ttu-id="e445b-131">Наложение сетки CSS для `article` элемента</span><span class="sxs-lookup"><span data-stu-id="e445b-131">CSS grid overlay for `article` element</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="e445b-132">Дополнительные сведения о наложении сетки можно найти в статьях [функции отладки сетки каскадных стилей][DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures].</span><span class="sxs-lookup"><span data-stu-id="e445b-132">For more information about grid overlays, go to [CSS grid debugging features][DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures].</span></span>  

<span data-ttu-id="e445b-133">Группа Microsoft Edge DevTools и группа "Chrome DevTools" совместно работают с дополнительными функциями.</span><span class="sxs-lookup"><span data-stu-id="e445b-133">The Microsoft Edge DevTools team and the Chrome DevTools team collaborate on additional features.</span></span>  <span data-ttu-id="e445b-134">Новые возможности включают в себя несколько наложений, которые сохраняются и настраиваются в новой области **макета** на панели " **элементы** ".</span><span class="sxs-lookup"><span data-stu-id="e445b-134">The new features include multiple overlays that are persistent and configurable from a new **Layout** pane on the **Elements** panel.</span></span>  

<span data-ttu-id="e445b-135">Чтобы включить эту функцию, перейдите к разделу [Включение экспериментальных функций][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] и установите флажок **включить новые функции отладки сетки CSS (параметры конфигурации, доступные в области Макет в элементах после перезапуска)**.</span><span class="sxs-lookup"><span data-stu-id="e445b-135">To turn on this experimental feature, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] and choose the checkbox next to **Enable new CSS Grid debugging features (configuration options available in Layout sidebar pane in Elements after restart)**.</span></span>  

<span data-ttu-id="e445b-136">Чтобы получить дополнительные сведения об этом эксперименте, перейдите к разделу [Включение новых функций отладки сетки каскадных стилей][DevtoolsExperimentalFeaturesEnableNewCssGridDebuggingFeatures].</span><span class="sxs-lookup"><span data-stu-id="e445b-136">For more information about this experiment, navigate to [Enable new CSS grid debugging features][DevtoolsExperimentalFeaturesEnableNewCssGridDebuggingFeatures].</span></span>  

<span data-ttu-id="e445b-137">Ошибка Chromium: [#1047356][CR1047356]</span><span class="sxs-lookup"><span data-stu-id="e445b-137">Chromium issue: [#1047356][CR1047356]</span></span>  

### <span data-ttu-id="e445b-138">Таблица, скопированная из консоли сохраняет форматирование</span><span class="sxs-lookup"><span data-stu-id="e445b-138">Table copied from the Console preserves formatting</span></span>  

<span data-ttu-id="e445b-139">В Microsoft Edge 85 или более ранней версии форматирование скопированных данных `console.table` было разорвано.</span><span class="sxs-lookup"><span data-stu-id="e445b-139">In Microsoft Edge 85 or earlier, the formatting of a copied `console.table` was lost.</span></span>  <span data-ttu-id="e445b-140">При копировании результатов из API консоли [таблицы][DevtoolsConsoleApiTable] и вставке в нее сохраняется только текст таблицы.</span><span class="sxs-lookup"><span data-stu-id="e445b-140">If you copied the output from the [table][DevtoolsConsoleApiTable] Console API, and pasted it, only the text of the table was kept.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-beta.msft.png" alt-text="Соответствие сочетаний клавиш в DevTools с кодом Visual Studio" lightbox="../../media/2020/08/console-table-beta.msft.png":::
         `table` <span data-ttu-id="e445b-142">Выходные данные API консоли в Microsoft Edge 85 или более ранней версии</span><span class="sxs-lookup"><span data-stu-id="e445b-142">Console API output in Microsoft Edge 85 or earlier</span></span>  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-beta-paste-visual-studio-code.msft.png" alt-text="Соответствие сочетаний клавиш в DevTools с кодом Visual Studio" lightbox="../../media/2020/08/console-table-beta-paste-visual-studio-code.msft.png":::
         `table` <span data-ttu-id="e445b-144">Выходные данные API консоли из Microsoft Edge 85 или более ранней версии, вставленные в код Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e445b-144">Console API output from Microsoft Edge 85 or earlier pasted into Visual Studio Code</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="e445b-145">В Microsoft Edge 86 или более поздней версии при копировании таблицы с **консоли**форматирование будет сохранено.</span><span class="sxs-lookup"><span data-stu-id="e445b-145">In Microsoft Edge 86 or later, when you copy a table from the **Console**, the formatting is now preserved.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-canary.msft.png" alt-text="Соответствие сочетаний клавиш в DevTools с кодом Visual Studio" lightbox="../../media/2020/08/console-table-canary.msft.png":::
         `table` <span data-ttu-id="e445b-147">Выходные данные API консоли в Microsoft Edge 86 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="e445b-147">Console API output in Microsoft Edge 86 or later</span></span>  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-canary-paste-visual-studio-code.msft.png" alt-text="Соответствие сочетаний клавиш в DevTools с кодом Visual Studio" lightbox="../../media/2020/08/console-table-canary-paste-visual-studio-code.msft.png":::
         `table` <span data-ttu-id="e445b-149">Выходные данные API консоли из Microsoft Edge 86 или более поздней версии, вставленные в код Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e445b-149">Console API output from Microsoft Edge 86 or later pasted into Visual Studio Code</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="e445b-150">Ошибка Chromium: [#1115011] [CR1115011]</span><span class="sxs-lookup"><span data-stu-id="e445b-150">Chromium issue: [#1115011][CR1115011]</span></span>  

### <span data-ttu-id="e445b-151">Средство просмотра заказов исходного кода для упрощения тестирования специальных возможностей</span><span class="sxs-lookup"><span data-stu-id="e445b-151">Source Order Viewer for easier accessibility testing</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Соответствие сочетаний клавиш в DevTools с кодом Visual Studio":::
   <span data-ttu-id="e445b-153">Экспериментальная функция</span><span class="sxs-lookup"><span data-stu-id="e445b-153">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="e445b-154">Новый вспомогательный модуль специальных возможностей отображает порядок элементов в источнике.</span><span class="sxs-lookup"><span data-stu-id="e445b-154">The new accessibility helper displays the order of elements in the source.</span></span>  

:::image type="complex" source="../../media/2020/08/source-order-viewer.msft.png" alt-text="Соответствие сочетаний клавиш в DevTools с кодом Visual Studio" lightbox="../../media/2020/08/source-order-viewer.msft.png":::
   <span data-ttu-id="e445b-156">Активация **порядка отображения исходного кода**</span><span class="sxs-lookup"><span data-stu-id="e445b-156">Activate **Show source order**</span></span>  
:::image-end:::  

<span data-ttu-id="e445b-157">Эта функция упрощает тестирование того, как пользователи с помощью средства чтения с экрана и клавиатуры смогут работать на веб-сайте или в приложении.</span><span class="sxs-lookup"><span data-stu-id="e445b-157">This feature makes it easier to test the way screen reader and keyboard users experience your website or app.</span></span>  <span data-ttu-id="e445b-158">Средства чтения с экрана и навигация с помощью клавиатуры зависят от содержимого, которое размещается в определенном порядке в исходном коде вашего веб-сайта или приложения, чтобы оно соответствовало отображаемой странице.</span><span class="sxs-lookup"><span data-stu-id="e445b-158">Screen readers and keyboard navigation depend on content being placed in a particular order in the source code of your website or app, so that it matches the rendered page.</span></span>  <span data-ttu-id="e445b-159">В средстве просмотра исходного порядка отображаются потенциальные отличия между обработанной страницей и исходным кодом.</span><span class="sxs-lookup"><span data-stu-id="e445b-159">The Source Order Viewer displays potential differences in order between the rendered page and the source code.</span></span>  

<span data-ttu-id="e445b-160">Чтобы включить эту функцию экспериментальных, перейдите к разделу [Включение экспериментальных функций][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] и установите флажок **включить средство просмотра заказов исходным кодом**.</span><span class="sxs-lookup"><span data-stu-id="e445b-160">To turn on this experimental feature, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] and choose the checkbox next to **Enable Source Order Viewer**.</span></span>  

<span data-ttu-id="e445b-161">Чтобы получить дополнительные сведения об этом эксперименте, перейдите в раздел [Включение средства просмотра заказов исходного кода][DevtoolsExperimentalFeaturesEnableSourceOrderViewer].</span><span class="sxs-lookup"><span data-stu-id="e445b-161">For more information about this experiment, navigate to [Enable Source Order Viewer][DevtoolsExperimentalFeaturesEnableSourceOrderViewer].</span></span>  

<span data-ttu-id="e445b-162">Ошибка Chromium: [#1094406][CR1094406]</span><span class="sxs-lookup"><span data-stu-id="e445b-162">Chromium issue: [#1094406][CR1094406]</span></span>  

<!--
### DevTools language enhancements  

Your feedback and internal discoveries uncovered which text strings used in the Microsoft Edge feedback should remain untranslated or create confusion when translated.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/localization-improvements-chinese-complex-stable.msft.png" alt-text="Соответствие сочетаний клавиш в DevTools с кодом Visual Studio" lightbox="localization-improvements-chinese-complex-stable.msft.png":::
         Microsoft Edge DevTools 85 and earlier in Traditional Chinese  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/localization-improvements-chinese-complex-canary.msft.png" alt-text="Соответствие сочетаний клавиш в DevTools с кодом Visual Studio" lightbox="../../media/2020/08/localization-improvements-chinese-complex-canary.msft.png":::
         Microsoft Edge DevTools 86  or later in Traditional Chinese  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

To meet your translation needs, the Microsoft Edge DevTools team is focused on improving translation quality.  

The current effort to improve translation quality enables easier support for more languages in the future.  
-->  

### <span data-ttu-id="e445b-163">Инструмент "выделение всех результатов поиска" в элементах</span><span class="sxs-lookup"><span data-stu-id="e445b-163">Highlight all search results in Elements tool</span></span>  

<span data-ttu-id="e445b-164">В Microsoft Edge 84 и 85 первый результат поиска на панели **элементов** не выделяются.</span><span class="sxs-lookup"><span data-stu-id="e445b-164">In Microsoft Edge 84 and 85, the first search result in the **Elements** panel did not highlight.</span></span>  <span data-ttu-id="e445b-165">Оставшиеся результаты поиска выделены правильно.</span><span class="sxs-lookup"><span data-stu-id="e445b-165">The remaining search results were highlighted correctly.</span></span>  

<span data-ttu-id="e445b-166">Благодарим вас за отправку отзыва и помощь в улучшении Chromium.</span><span class="sxs-lookup"><span data-stu-id="e445b-166">Thank you for sending your feedback and helping improve Chromium.</span></span>  <span data-ttu-id="e445b-167">В проекте Chromium Open-Source возникла ошибка, связанная с [не#1103316ой][CR1103316] отзыва.</span><span class="sxs-lookup"><span data-stu-id="e445b-167">Your feedback uncovered Issue [#1103316][CR1103316] in the open-source Chromium project.</span></span>  

:::image type="complex" source="../../media/2020/08/elements- search-highlight-fixed.msft.png" alt-text="Соответствие сочетаний клавиш в DevTools с кодом Visual Studio" lightbox="../../media/2020/08/elements- search-highlight-fixed.msft.png":::
   <span data-ttu-id="e445b-169">Выделенный первый результат поиска на панели " **элементы** " в Microsoft Edge 84 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="e445b-169">Highlighted first search result on **Elements** panel in Microsoft Edge 84 or later</span></span>  
:::image-end:::  

<span data-ttu-id="e445b-170">Теперь проблема устранена во всех версиях Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="e445b-170">The issue is now fixed in all versions of Microsoft Edge.</span></span>  

<span data-ttu-id="e445b-171">Ошибка Chromium: [#1103316][CR1103316]</span><span class="sxs-lookup"><span data-stu-id="e445b-171">Chromium issue: [#1103316][CR1103316]</span></span>  

## <span data-ttu-id="e445b-172">Объявления из проекта Chromium</span><span class="sxs-lookup"><span data-stu-id="e445b-172">Announcements from the Chromium project</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <span data-ttu-id="e445b-173">Новая панель мультимедиа</span><span class="sxs-lookup"><span data-stu-id="e445b-173">New Media panel</span></span>  

<span data-ttu-id="e445b-174">DevTools теперь отображает сведения о проигрывателях мультимедиа на панели " [мультимедиа][DevtoolsMediaIndex] ".</span><span class="sxs-lookup"><span data-stu-id="e445b-174">DevTools now displays media players information in the [Media][DevtoolsMediaIndex] panel.</span></span>  

<span data-ttu-id="e445b-175">Чтобы открыть новую панель **мультимедиа** , выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="e445b-175">To open the new **Media** panel, complete the following step.</span></span>  

1.  <span data-ttu-id="e445b-176">Нажмите кнопку **Настройка и выберите DevTools** \ ( `...` \) > **другие инструменты**  >  **мультимедиа**.</span><span class="sxs-lookup"><span data-stu-id="e445b-176">Choose **Customize and control DevTools** \(`...`\) > **More tools** > **Media**.</span></span>  
    
    :::image type="complex" source="../../media/2020/08/media-panel.msft.png" alt-text="Соответствие сочетаний клавиш в DevTools с кодом Visual Studio" lightbox="../../media/2020/08/media-panel.msft.png":::
       <span data-ttu-id="e445b-178">Новая панель **мультимедиа**</span><span class="sxs-lookup"><span data-stu-id="e445b-178">New **Media** panel</span></span>  
    :::image-end:::  

<span data-ttu-id="e445b-179">Перед новой панелью **мультимедиа** в DevTools сведения о регистрации и отладке видеопроигрывателей находятся в разделе " **последние игрока** ".</span><span class="sxs-lookup"><span data-stu-id="e445b-179">Before the new **Media** panel in DevTools, the logging and debug information about video players was located under the **Recent Players** setting.</span></span>  <span data-ttu-id="e445b-180">Чтобы открыть параметр " **недавние игрока** ", перейдите на `edge://media-internals` вкладку **игрока** и щелкните ее.</span><span class="sxs-lookup"><span data-stu-id="e445b-180">To open the **Recent Players** setting, go to `edge://media-internals` and choose the **Players** tab.</span></span>  

<span data-ttu-id="e445b-181">Просматривайте содержимое в реальном времени и отучите возможные проблемы быстрее, в том числе в следующих примерах.</span><span class="sxs-lookup"><span data-stu-id="e445b-181">View live content and inspect potential issues more quickly, including the following examples.</span></span>  

*   <span data-ttu-id="e445b-182">Почему кадры удаляются?</span><span class="sxs-lookup"><span data-stu-id="e445b-182">Why frames are dropped?</span></span>  
*   <span data-ttu-id="e445b-183">Почему JavaScript взаимодействует с проигрывателем непредсказуемым образом?</span><span class="sxs-lookup"><span data-stu-id="e445b-183">Why JavaScript is interacting with the player in an unexpected way?</span></span>  

### <span data-ttu-id="e445b-184">Захват снимков узлов с помощью контекстного меню панели элементов</span><span class="sxs-lookup"><span data-stu-id="e445b-184">Capture node screenshots using the Elements panel context menu</span></span>  

<span data-ttu-id="e445b-185">Теперь вы можете захватывать снимки узлов с помощью контекстного меню на панели " **элементы** ".</span><span class="sxs-lookup"><span data-stu-id="e445b-185">You may now capture node screenshots using the context menu in the **Elements** panel.</span></span>  

<span data-ttu-id="e445b-186">Например, чтобы сделать снимок экрана оглавлением, наведите на него указатель мыши, откройте контекстное меню, а затем выберите пункт **захватить снимок экрана узла**.</span><span class="sxs-lookup"><span data-stu-id="e445b-186">For example, to take a screenshot of the table of contents, hover on the element, open the contextual menu \(right-click\), and select **Capture node screenshot**.</span></span>  

:::image type="complex" source="../../media/2020/08/capture-node-screenshot.msft.png" alt-text="Соответствие сочетаний клавиш в DevTools с кодом Visual Studio" lightbox="../../media/2020/08/capture-node-screenshot.msft.png":::
   <span data-ttu-id="e445b-188">Снимок экрана захвата узлов</span><span class="sxs-lookup"><span data-stu-id="e445b-188">Capture node screenshots</span></span>  
:::image-end:::  

<span data-ttu-id="e445b-189">Ошибка Chromium: [#1100253][CR1100253]</span><span class="sxs-lookup"><span data-stu-id="e445b-189">Chromium issue: [#1100253][CR1100253]</span></span>  

### <span data-ttu-id="e445b-190">Обновления средства устранения проблем</span><span class="sxs-lookup"><span data-stu-id="e445b-190">Issues tool updates</span></span>  

<span data-ttu-id="e445b-191">Панель предупреждения "проблемы" на панели **консоли** теперь заменяется обычным сообщением.</span><span class="sxs-lookup"><span data-stu-id="e445b-191">The Issues warning bar on the **Console** panel is now replaced with a regular message.</span></span>  

<!--todo: this figure need to be updated  -->  

:::image type="complex" source="../../media/2020/08/issue-console-msg.msft.png" alt-text="Соответствие сочетаний клавиш в DevTools с кодом Visual Studio" lightbox="../../media/2020/08/issue-console-msg.msft.png":::
   <span data-ttu-id="e445b-193">Проблемы в сообщении консоли</span><span class="sxs-lookup"><span data-stu-id="e445b-193">Issues in console message</span></span>  
:::image-end:::  

<span data-ttu-id="e445b-194">Сторонние файлы cookie теперь по умолчанию скрыты в инструменте " **вопросы** ".</span><span class="sxs-lookup"><span data-stu-id="e445b-194">Third-party cookie issues are now hidden by default in the **Issues** tool.</span></span>  <span data-ttu-id="e445b-195">Чтобы просмотреть список проблем, установите флажок **Включить сторонние файлы cookie** .</span><span class="sxs-lookup"><span data-stu-id="e445b-195">Enable the new **Include third-party cookie issues** checkbox to view the issues.</span></span>  

:::image type="complex" source="../../media/2020/08/third-party-cookies.msft.png" alt-text="Соответствие сочетаний клавиш в DevTools с кодом Visual Studio" lightbox="../../media/2020/08/third-party-cookies.msft.png":::
   <span data-ttu-id="e445b-197">флажок "вопросы и сторонние файлы cookie"</span><span class="sxs-lookup"><span data-stu-id="e445b-197">third-party cookie issues checkbox</span></span>  
:::image-end:::  

<span data-ttu-id="e445b-198">Проблемы с Chromium: [1096481][CR1096481], [1068116][CR1068116], [1080589][CR1080589]</span><span class="sxs-lookup"><span data-stu-id="e445b-198">Chromium issues: [1096481][CR1096481], [1068116][CR1068116], [1080589][CR1080589]</span></span>  

### <span data-ttu-id="e445b-199">Эмуляция отсутствующих локальных шрифтов</span><span class="sxs-lookup"><span data-stu-id="e445b-199">Emulate missing local fonts</span></span>  

<span data-ttu-id="e445b-200">Откройте [средство подготовки][DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance] и воспользуйтесь новым компонентом **Отключить локальные шрифты** для эмуляции отсутствующих `local()` источников в `@font-face` правилах.</span><span class="sxs-lookup"><span data-stu-id="e445b-200">Open the [Rendering tool][DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance] and use the new **Disable local fonts** feature to emulate missing `local()` sources in `@font-face` rules.</span></span>  

<span data-ttu-id="e445b-201">Например, если `Rubik` шрифт установлен на устройстве, а `@font-face src` правило использует его в качестве `local()` шрифта, Microsoft Edge использует локальный файл шрифта на устройстве.</span><span class="sxs-lookup"><span data-stu-id="e445b-201">For example, when the `Rubik` font is installed on your device and the `@font-face src` rule uses it as a `local()` font, Microsoft Edge uses the local font file from your device.</span></span>  

<span data-ttu-id="e445b-202">При включении функции **Отключить локальные шрифты** DevTools игнорирует `local()` шрифты и извлекает их из сети.</span><span class="sxs-lookup"><span data-stu-id="e445b-202">When **Disable local fonts** is enabled, DevTools ignores the `local()` fonts and fetches each from the network.</span></span>  

:::image type="complex" source="../../media/2020/08/disable-font.msft.png" alt-text="Соответствие сочетаний клавиш в DevTools с кодом Visual Studio" lightbox="../../media/2020/08/disable-font.msft.png":::
   <span data-ttu-id="e445b-204">Эмуляция отсутствующих локальных шрифтов</span><span class="sxs-lookup"><span data-stu-id="e445b-204">Emulate missing local fonts</span></span>  
:::image-end:::  

<span data-ttu-id="e445b-205">При использовании двух разных копий одного и того же шрифта в процессе разработки (например, в приведенных ниже примерах).</span><span class="sxs-lookup"><span data-stu-id="e445b-205">If you use two different copies of the same font during development, such as the following examples.</span></span>  

*   <span data-ttu-id="e445b-206">Локальный шрифт для средств разработки.</span><span class="sxs-lookup"><span data-stu-id="e445b-206">A local font for your design tools.</span></span>  
*   <span data-ttu-id="e445b-207">Веб-шрифт для вашего кода.</span><span class="sxs-lookup"><span data-stu-id="e445b-207">A web font for your code.</span></span>  

<span data-ttu-id="e445b-208">Используйте **функцию отключить локальные шрифты** , чтобы упростить выполнение описанных ниже задач.</span><span class="sxs-lookup"><span data-stu-id="e445b-208">Use **Disable local fonts** to make it easier for you to complete the following tasks.</span></span>  

*   <span data-ttu-id="e445b-209">Отладка и оценка скорости загрузки и оптимизации веб-шрифтов.</span><span class="sxs-lookup"><span data-stu-id="e445b-209">Debug and measure loading performance and optimization of web fonts.</span></span>  
*   <span data-ttu-id="e445b-210">Проверьте точность `@font-face` правил CSS.</span><span class="sxs-lookup"><span data-stu-id="e445b-210">Verify accuracy of your CSS `@font-face` rules.</span></span>  
*   <span data-ttu-id="e445b-211">Обнаружение различий между локальными версиями, установленными на устройстве, и веб-шрифтом.</span><span class="sxs-lookup"><span data-stu-id="e445b-211">Discover differences between local versions installed on your device and a web font.</span></span>  

<span data-ttu-id="e445b-212">Ошибка Chromium: [#384968][CR384968]</span><span class="sxs-lookup"><span data-stu-id="e445b-212">Chromium issue: [#384968][CR384968]</span></span>  

### <span data-ttu-id="e445b-213">Эмуляция неактивных пользователей</span><span class="sxs-lookup"><span data-stu-id="e445b-213">Emulate inactive users</span></span>  

<span data-ttu-id="e445b-214">[API обнаружения простоя][WebDevIdleDetection] позволяет разработчикам обнаруживать неактивные пользователи и реагировать на изменения состояния простоя.</span><span class="sxs-lookup"><span data-stu-id="e445b-214">The [Idle Detection API][WebDevIdleDetection] allows developers to detect inactive users and react on idle state changes.</span></span>  <span data-ttu-id="e445b-215">Теперь вы можете использовать DevTools для эмуляции изменений состояния простоя в инструменте " **датчики** " и для состояния пользователя, и для состояния экрана вместо того, чтобы ждать изменения фактического состояния простоя.</span><span class="sxs-lookup"><span data-stu-id="e445b-215">You are now able to use DevTools to emulate idle state changes in the **Sensors** tool for both the user state and the screen state instead of waiting for the actual idle state to change.</span></span>  <span data-ttu-id="e445b-216">Вы можете открыть инструмент **Sensors (датчики** ) из [ящика][DevtoolsCustomizeIndexDrawer].</span><span class="sxs-lookup"><span data-stu-id="e445b-216">You may open the **Sensors** tool from the [Drawer][DevtoolsCustomizeIndexDrawer].</span></span>  

:::image type="complex" source="../../media/2020/08/emulate-idle.msft.png" alt-text="Соответствие сочетаний клавиш в DevTools с кодом Visual Studio" lightbox="../../media/2020/08/emulate-idle.msft.png":::
   <span data-ttu-id="e445b-218">Эмуляция неактивных пользователей</span><span class="sxs-lookup"><span data-stu-id="e445b-218">Emulate inactive users</span></span>  
:::image-end:::  

<span data-ttu-id="e445b-219">Ошибка Chromium: [#1090802][CR1090802]</span><span class="sxs-lookup"><span data-stu-id="e445b-219">Chromium issue: [#1090802][CR1090802]</span></span>  

### <span data-ttu-id="e445b-220">Предпочтительные эмуляции — сокращенные данные</span><span class="sxs-lookup"><span data-stu-id="e445b-220">Emulate prefers-reduced-data</span></span>  

> [!NOTE]
> <span data-ttu-id="e445b-221">Чтобы включить эту функцию в Microsoft Edge 86, перейдите на вкладку `edge://flags#enable-experimental-web-platform-features` **экспериментальные веб-платформа** и включите этот флажок.</span><span class="sxs-lookup"><span data-stu-id="e445b-221">In Microsoft Edge 86, to enable this feature, go to `edge://flags#enable-experimental-web-platform-features` and turn on the **Experimental Web Platform features** flag.</span></span>  <span data-ttu-id="e445b-222">Параметр эмуляции отображается только в том случае, если включен флаг.</span><span class="sxs-lookup"><span data-stu-id="e445b-222">The emulation option is only displayed if the flag is enabled.</span></span>  

<span data-ttu-id="e445b-223">Запрос " [предпочтительный"-][CsswgDraftsMediaqueries5DescdefMediaPrefersReducedData] "мультимедиа" — это обнаружение параметров содержимого пользователя для уменьшения объема данных.</span><span class="sxs-lookup"><span data-stu-id="e445b-223">The [prefers-reduced-data][CsswgDraftsMediaqueries5DescdefMediaPrefersReducedData] media query detects user content preferences for reduced data.</span></span>  <span data-ttu-id="e445b-224">Если этот флажок установлен, пользователь получает содержимое страницы, которое использует меньшие данные.</span><span class="sxs-lookup"><span data-stu-id="e445b-224">If selected, the user receives alternate page content that uses less data.</span></span>  

<span data-ttu-id="e445b-225">Теперь вы можете использовать DevTools для эмуляции `prefers-reduced-data` запроса мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="e445b-225">You may now use DevTools to emulate the `prefers-reduced-data` media query.</span></span>  

:::image type="complex" source="../../media/2020/08/emulate-prefers-reduced-data.msft.png" alt-text="Соответствие сочетаний клавиш в DevTools с кодом Visual Studio" lightbox="../../media/2020/08/emulate-prefers-reduced-data.msft.png":::
   <span data-ttu-id="e445b-227">Предпочтительные эмуляции — сокращенные данные</span><span class="sxs-lookup"><span data-stu-id="e445b-227">Emulate prefers-reduced-data</span></span>  
:::image-end:::  

<span data-ttu-id="e445b-228">Ошибка Chromium: [#1096068][CR1096068]</span><span class="sxs-lookup"><span data-stu-id="e445b-228">Chromium issue: [#1096068][CR1096068]</span></span>  

### <span data-ttu-id="e445b-229">Поддержка новых функций JavaScript</span><span class="sxs-lookup"><span data-stu-id="e445b-229">Support for new JavaScript features</span></span>  

<span data-ttu-id="e445b-230">DevTools теперь обладают улучшенными возможностями поддержки следующих функций языка JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e445b-230">DevTools now have better supported the following JavaScript language features.</span></span>  

| <span data-ttu-id="e445b-231">Функция языка JavaScript</span><span class="sxs-lookup"><span data-stu-id="e445b-231">JavaScript language feature</span></span> | <span data-ttu-id="e445b-232">Сведения</span><span class="sxs-lookup"><span data-stu-id="e445b-232">Details</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="e445b-233">Логические операторы присваивания</span><span class="sxs-lookup"><span data-stu-id="e445b-233">Logical assignment operators</span></span>][V8FeaturesLogicalAssignment] | <span data-ttu-id="e445b-234">DevTools теперь поддерживает логическое назначение с помощью новых операторов "" "" " `&&=` `||=` и" `??=` "" на панели " **консоль** " и " **источники** ".</span><span class="sxs-lookup"><span data-stu-id="e445b-234">DevTools now supports logical assignment with the new `&&=`, `||=`, and `??=` operators in the **Console** and **Sources** panels.</span></span>  |  
| <span data-ttu-id="e445b-235">Некачественная печать [числовых разделителей][V8FeaturesNumericSeparators]</span><span class="sxs-lookup"><span data-stu-id="e445b-235">Pretty-print [numeric separators][V8FeaturesNumericSeparators]</span></span> | <span data-ttu-id="e445b-236">Теперь DevTools правильно — печатает на панели « **источники** » числовые разделители.</span><span class="sxs-lookup"><span data-stu-id="e445b-236">DevTools now properly pretty-prints the numeric separators in the **Sources** panel.</span></span>  |  

<span data-ttu-id="e445b-237">Проблемы с Chromium: [1086817][CR1086817], [1080569][CR1080569]</span><span class="sxs-lookup"><span data-stu-id="e445b-237">Chromium issues: [1086817][CR1086817], [1080569][CR1080569]</span></span>  

### <span data-ttu-id="e445b-238">Lighthouse 6,2 на панели Lighthouse</span><span class="sxs-lookup"><span data-stu-id="e445b-238">Lighthouse 6.2 in the Lighthouse panel</span></span>  

<span data-ttu-id="e445b-239">Панель **Lighthouse** теперь работает под управлением Lighthouse 6,2.</span><span class="sxs-lookup"><span data-stu-id="e445b-239">The **Lighthouse** panel is now running Lighthouse 6.2.</span></span>  <span data-ttu-id="e445b-240">Полный список изменений можно найти в [заметках о выпуске Lighthouse][GithubGooglechromeLighthouseV620].</span><span class="sxs-lookup"><span data-stu-id="e445b-240">For a full list of changes, go to the [Lighthouse release notes][GithubGooglechromeLighthouseV620].</span></span>  

<span data-ttu-id="e445b-241">Ошибка Chromium: [#772558][CR772558]</span><span class="sxs-lookup"><span data-stu-id="e445b-241">Chromium issue: [#772558][CR772558]</span></span>  

### <span data-ttu-id="e445b-242">Устаревшие сведения о других источниках, перечисленные в области "работники службы"</span><span class="sxs-lookup"><span data-stu-id="e445b-242">Deprecation of other origins listing in the Service Workers pane</span></span>  

<span data-ttu-id="e445b-243">DevTools теперь предоставляет ссылку из области "работа с **сотрудниками** \" (панель**приложения** > область " **сотрудники** "), чтобы просмотреть полный список работников служб из других источников.</span><span class="sxs-lookup"><span data-stu-id="e445b-243">DevTools now provides a link from the **Service workers** pane \(**Application** panel > **Service workers** pane\) to view the full list of service workers from other origins.</span></span>  <span data-ttu-id="e445b-244">Чтобы получить доступ к списку, не открывая DevTools, перейдите на `edge://service-worker-internals/?devtools` .</span><span class="sxs-lookup"><span data-stu-id="e445b-244">To access the list without opening the DevTools, go to `edge://service-worker-internals/?devtools`.</span></span>  

<span data-ttu-id="e445b-245">Ранее DevTools отображал список, вложенный в панель **приложения** , > области "работа с **сотрудниками службы** ".</span><span class="sxs-lookup"><span data-stu-id="e445b-245">Previously DevTools displayed a list nested under the **Application** panel > **Service workers** pane.</span></span>  

:::image type="complex" source="../../media/2020/08/sw-other-origins.msft.png" alt-text="Соответствие сочетаний клавиш в DevTools с кодом Visual Studio" lightbox="../../media/2020/08/sw-other-origins.msft.png":::
   <span data-ttu-id="e445b-247">Ссылка на другие источники</span><span class="sxs-lookup"><span data-stu-id="e445b-247">Link to other origins</span></span>  
:::image-end:::  

<span data-ttu-id="e445b-248">Ошибка Chromium: [#807440][CR807440]</span><span class="sxs-lookup"><span data-stu-id="e445b-248">Chromium issue: [#807440][CR807440]</span></span>  

### <span data-ttu-id="e445b-249">Отображение сводки о покрытии для отфильтрованных элементов</span><span class="sxs-lookup"><span data-stu-id="e445b-249">Show coverage summary for filtered items</span></span>  

<span data-ttu-id="e445b-250">DevTools сейчас пересчитайте и отобразите сводную информацию о покрытии динамическими.</span><span class="sxs-lookup"><span data-stu-id="e445b-250">DevTools now recalculate and display a summary of coverage information dynamically.</span></span>  <span data-ttu-id="e445b-251">Динамическое отображение инициируется, когда фильтры применяются в инструменте [Coverage][DevtoolsCoverageIndex] .</span><span class="sxs-lookup"><span data-stu-id="e445b-251">The dynamic display is triggered when filters are applied in the [Coverage][DevtoolsCoverageIndex] tool.</span></span>  <span data-ttu-id="e445b-252">Перед тем, как средство **покрытия** всегда выводит сводку по всем сведениям о покрытии.</span><span class="sxs-lookup"><span data-stu-id="e445b-252">Before the **Coverage** tool always displayed a summary of all coverage information.</span></span>  

<span data-ttu-id="e445b-253">На первой из приведенных ниже рисунков сводка первоначально отображается `344 kB of 1.7 MB (20%) used so far.  1.4 MB unused.` и на второй из приведенных ниже рисунков показывается, `26.8 kB of 408 kB (7%) used so far.  381 kB unused.` когда будет применена фильтрация CSS.</span><span class="sxs-lookup"><span data-stu-id="e445b-253">In the first of the following figures, the summary initially displays `344 kB of 1.7 MB (20%) used so far.  1.4 MB unused.` and in the second of the following figures, the summary displays `26.8 kB of 408 kB (7%) used so far.  381 kB unused.` after CSS filtering is applied.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/coverage-compare.msft.png" alt-text="Соответствие сочетаний клавиш в DevTools с кодом Visual Studio" lightbox="../../media/2020/08/coverage-compare.msft.png":::
         <span data-ttu-id="e445b-255">Сводка о покрытии</span><span class="sxs-lookup"><span data-stu-id="e445b-255">Coverage summary</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/coverage-compare-css-filter.msft.png" alt-text="Соответствие сочетаний клавиш в DevTools с кодом Visual Studio" lightbox="../../media/2020/08/coverage-compare-css-filter.msft.png":::
         <span data-ttu-id="e445b-257">Сводка покрытия для отфильтрованных элементов</span><span class="sxs-lookup"><span data-stu-id="e445b-257">Coverage summary for filtered items</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

<span data-ttu-id="e445b-258">Ошибка Chromium: [#1061385][CR1090802]</span><span class="sxs-lookup"><span data-stu-id="e445b-258">Chromium issue: [#1061385][CR1090802]</span></span>  

### <span data-ttu-id="e445b-259">Новый вид сведений о кадре на панели приложения</span><span class="sxs-lookup"><span data-stu-id="e445b-259">New frame details view in Application panel</span></span>  

<span data-ttu-id="e445b-260">DevTools теперь показывать подробное представление для каждого кадра.</span><span class="sxs-lookup"><span data-stu-id="e445b-260">DevTools now show a detailed view for each frame.</span></span>  <span data-ttu-id="e445b-261">Для доступа к нему выберите рамку в меню " **кадры** " на панели **приложения** .</span><span class="sxs-lookup"><span data-stu-id="e445b-261">To access it, choose a frame under the **Frames** menu in the **Application** panel.</span></span>  

:::image type="complex" source="../../media/2020/08/frame-details.msft.png" alt-text="Соответствие сочетаний клавиш в DevTools с кодом Visual Studio" lightbox="../../media/2020/08/frame-details.msft.png":::
   <span data-ttu-id="e445b-263">Новый подробный вид рамки на панели **приложения**</span><span class="sxs-lookup"><span data-stu-id="e445b-263">New detailed view for a frame in **Application** panel</span></span>  
:::image-end:::  

<span data-ttu-id="e445b-264">Ошибка Chromium: [#1093247][CR1093247]</span><span class="sxs-lookup"><span data-stu-id="e445b-264">Chromium issue: [#1093247][CR1093247]</span></span>  

#### <span data-ttu-id="e445b-265">Сведения о кадре для открытых окон</span><span class="sxs-lookup"><span data-stu-id="e445b-265">Frame details for opened windows</span></span>  

<span data-ttu-id="e445b-266">Теперь в дереве фреймов отображаются открытые окна и всплывающие окна.</span><span class="sxs-lookup"><span data-stu-id="e445b-266">Open windows and pop-up windows now display under the frame tree as well.</span></span>  <span data-ttu-id="e445b-267">Подробное представление открытых окон включает дополнительные сведения о безопасности.</span><span class="sxs-lookup"><span data-stu-id="e445b-267">The detailed view of the opened windows includes additional security information.</span></span>  

:::image type="complex" source="../../media/2020/08/window-opener.msft.png" alt-text="Соответствие сочетаний клавиш в DevTools с кодом Visual Studio" lightbox="../../media/2020/08/window-opener.msft.png":::
   <span data-ttu-id="e445b-269">Подробный обзор нового кадра для открытых окон</span><span class="sxs-lookup"><span data-stu-id="e445b-269">New frame detailed view for opened windows</span></span>  
:::image-end:::  

<span data-ttu-id="e445b-270">Ошибка Chromium: [#1107766] [CR1107766]</span><span class="sxs-lookup"><span data-stu-id="e445b-270">Chromium issue: [#1107766][CR1107766]</span></span>  

#### <span data-ttu-id="e445b-271">Сведения о безопасности и изоляции</span><span class="sxs-lookup"><span data-stu-id="e445b-271">Security and isolation information</span></span>  

<span data-ttu-id="e445b-272">В разделе сведения о кадре отображаются безопасный контекст, [Политика встраивания с Межисточниками (COEP)][WebDevCoopCoep], а также меж- [Openerная политика (Coop)][WebDevCoopCoep] .</span><span class="sxs-lookup"><span data-stu-id="e445b-272">Secure context, [Cross-Origin-Embedder-Policy (COEP)][WebDevCoopCoep], and [Cross-Origin-Opener-Policy (COOP)][WebDevCoopCoep] are now displayed in the frame details.</span></span>  

:::image type="complex" source="../../media/2020/08/coep-coop.msft.png" alt-text="Соответствие сочетаний клавиш в DevTools с кодом Visual Studio" lightbox="../../media/2020/08/coep-coop.msft.png":::
   <span data-ttu-id="e445b-274">Сведения о безопасности и изоляции</span><span class="sxs-lookup"><span data-stu-id="e445b-274">Security and isolation information</span></span>  
:::image-end:::  

<span data-ttu-id="e445b-275">В будущем группа Microsoft Edge DevTools и группа Chrome DevTools планирует добавить дополнительные сведения о безопасности в сведения о кадре.</span><span class="sxs-lookup"><span data-stu-id="e445b-275">In the future, the Microsoft Edge DevTools team and the Chrome DevTools team are planning to add more security information to the frame details.</span></span>  

<span data-ttu-id="e445b-276">Ошибка Chromium: [#1051466][CR1051466]</span><span class="sxs-lookup"><span data-stu-id="e445b-276">Chromium issue: [#1051466][CR1051466]</span></span>  

### <span data-ttu-id="e445b-277">Элементы и обновления панели сети</span><span class="sxs-lookup"><span data-stu-id="e445b-277">Elements and Network panel updates</span></span>  

#### <span data-ttu-id="e445b-278">Специальные возможности цвета в области "стили"</span><span class="sxs-lookup"><span data-stu-id="e445b-278">Accessible color suggestion in the Styles pane</span></span>  

<span data-ttu-id="e445b-279">DevTools теперь предлагает варианты цветов для текста с низким контрастом цвета.</span><span class="sxs-lookup"><span data-stu-id="e445b-279">DevTools now provides color suggestions for low color contrast text.</span></span>  

<span data-ttu-id="e445b-280">В примере ниже `h1` есть текст с низким контрастом.</span><span class="sxs-lookup"><span data-stu-id="e445b-280">In the example below, `h1` has low contrast text.</span></span>  <span data-ttu-id="e445b-281">Чтобы исправить ошибку, откройте окно выбора цвета `color` свойства в области **стили** .</span><span class="sxs-lookup"><span data-stu-id="e445b-281">To fix it, open the color picker of the `color` property in the **Styles** pane.</span></span>  <span data-ttu-id="e445b-282">После того как вы развернете раздел **коэффициент контрастности** , DevTools предоставляет варианты цветов AA и AAA.</span><span class="sxs-lookup"><span data-stu-id="e445b-282">After you expand the **Contrast ratio** section, DevTools provides AA and AAA color suggestions.</span></span>  <span data-ttu-id="e445b-283">Выберите предложенный цвет, чтобы применить его.</span><span class="sxs-lookup"><span data-stu-id="e445b-283">Select the suggested color to apply the color.</span></span>  

:::image type="complex" source="../../media/2020/08/contrast-color-suggestion.msft.png" alt-text="Соответствие сочетаний клавиш в DevTools с кодом Visual Studio" lightbox="../../media/2020/08/contrast-color-suggestion.msft.png":::
   <span data-ttu-id="e445b-285">Средство выбора цвета предлагает варианты цветов AA и AAA</span><span class="sxs-lookup"><span data-stu-id="e445b-285">Color picker suggests AA and AAA color suggestions</span></span>  
:::image-end:::  

<span data-ttu-id="e445b-286">Ошибка Chromium: [#1093227][CR1093227]</span><span class="sxs-lookup"><span data-stu-id="e445b-286">Chromium issue: [#1093227][CR1093227]</span></span>  

#### <span data-ttu-id="e445b-287">Область "восстановить свойства" на панели "элементы"</span><span class="sxs-lookup"><span data-stu-id="e445b-287">Reinstate Properties pane in the Elements panel</span></span>  

<span data-ttu-id="e445b-288">Область **свойств** будет возвращена.</span><span class="sxs-lookup"><span data-stu-id="e445b-288">The **Properties** pane is back.</span></span>  <span data-ttu-id="e445b-289">Она была [признана устаревшей в Microsoft Edge 84][DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsPanel].</span><span class="sxs-lookup"><span data-stu-id="e445b-289">It was [deprecated in Microsoft Edge 84][DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsPanel].</span></span>  <span data-ttu-id="e445b-290">Группа Microsoft Edge DevTools и группа "Chrome DevTools" предназначены для планирования улучшений для проверки свойств элементов.</span><span class="sxs-lookup"><span data-stu-id="e445b-290">The Microsoft Edge DevTools team and the Chrome DevTools team are planning improvements for inspecting properties of elements.</span></span>  

:::image type="complex" source="../../media/2020/08/properties-pane.msft.png" alt-text="Соответствие сочетаний клавиш в DevTools с кодом Visual Studio" lightbox="../../media/2020/08/properties-pane.msft.png":::
   <span data-ttu-id="e445b-292">Область " **Свойства** " на панели " **элементы** "</span><span class="sxs-lookup"><span data-stu-id="e445b-292">**Properties** pane in the **Elements** panel</span></span>  
:::image-end:::  

<span data-ttu-id="e445b-293">Ошибка Chromium:</span><span class="sxs-lookup"><span data-stu-id="e445b-293">Chromium issue:</span></span>  <!--  [#1105205][CR1105205],  -->  <span data-ttu-id="e445b-294">[#1116085] [CR1116085]</span><span class="sxs-lookup"><span data-stu-id="e445b-294">[#1116085][CR1116085]</span></span>  

<!--  
#### Human-readable X-Client-Data header values in the Network panel  

When inspecting a network resource in the Network panel, DevTools now formats any `X-Client-Data` header values in **Headers** pane as code.  

The `X-Client-Data` HTTP header contains a list of experiment IDs and Microsoft Edge flags that are enabled in your browser.  The raw header values look like opaque strings since the values are `base-64-encoded`, serialized [protocol buffers][GoogleDevelopersProtocolBuffers].  To make the contents more transparent to developers, DevTools now shows the decoded values.  

:::image type="complex" source="../../media/2020/08/x-client-data.msft.png" alt-text="Соответствие сочетаний клавиш в DevTools с кодом Visual Studio" lightbox="../../media/2020/08/x-client-data.msft.png":::
   Human-readable `X-Client-Data` header values  
:::image-end:::  

Chromium issue: [#1103854][CR1103854]  
-->  

#### <span data-ttu-id="e445b-295">Автозаполнение настраиваемых шрифтов в области "стили"</span><span class="sxs-lookup"><span data-stu-id="e445b-295">Autocomplete custom fonts in the Styles pane</span></span>  

<span data-ttu-id="e445b-296">Импортированные фрагменты шрифта теперь добавляются в список автозавершения CSS при редактировании `font-family` свойства в области **стили** .</span><span class="sxs-lookup"><span data-stu-id="e445b-296">Imported font faces are now added to the list of CSS autocompletion when editing the `font-family` property in the **Styles** pane.</span></span>  

<span data-ttu-id="e445b-297">Например, если `monospace` на локальном компьютере установлен настраиваемый шрифт, он отображается в списке завершения CSS.</span><span class="sxs-lookup"><span data-stu-id="e445b-297">For example, if `monospace` is a custom font installed on the local machine, it's displayed in the CSS completion list.</span></span> <span data-ttu-id="e445b-298">В предыдущих версиях Microsoft Edge шрифт не отображался.</span><span class="sxs-lookup"><span data-stu-id="e445b-298">In previous versions of Microsoft Edge, the font wasn't displayed.</span></span>

:::image type="complex" source="../../media/2020/08/font-auto-complete.msft.png" alt-text="Соответствие сочетаний клавиш в DevTools с кодом Visual Studio" lightbox="../../media/2020/08/font-auto-complete.msft.png":::
   <span data-ttu-id="e445b-300">Автозаполнение настраиваемых шрифтов</span><span class="sxs-lookup"><span data-stu-id="e445b-300">Autocomplete custom fonts</span></span>  
:::image-end:::  

<span data-ttu-id="e445b-301">Ошибка Chromium: [#1106221] [CR1106221]</span><span class="sxs-lookup"><span data-stu-id="e445b-301">Chromium issue: [#1106221][CR1106221]</span></span>  

#### <span data-ttu-id="e445b-302">Согласованное отображение типа ресурсов на панели "сеть"</span><span class="sxs-lookup"><span data-stu-id="e445b-302">Consistently display resource type in Network panel</span></span>  

<span data-ttu-id="e445b-303">DevTools теперь будет отображать тот же тип ресурса, что и исходный, и добавляет `/ Redirect` к значению столбца **Type** , когда происходит перенаправление \ (код состояния HTTP 302 \).</span><span class="sxs-lookup"><span data-stu-id="e445b-303">DevTools now consistently display the same resource type as the original network request and appends `/ Redirect` to the **Type** column value when redirection \(HTTP status code 302\) happens.</span></span>  

<span data-ttu-id="e445b-304">Ранее DevTools изменил тип на " `Other` иногда".</span><span class="sxs-lookup"><span data-stu-id="e445b-304">Previously DevTools changed the type to `Other` sometimes.</span></span>  

:::image type="complex" source="../../media/2020/08/network-redirect.msft.png" alt-text="Соответствие сочетаний клавиш в DevTools с кодом Visual Studio" lightbox="../../media/2020/08/network-redirect.msft.png":::
   <span data-ttu-id="e445b-306">Вывод типа ресурса перенаправления</span><span class="sxs-lookup"><span data-stu-id="e445b-306">Display redirect resource type</span></span>  
:::image-end:::  

<span data-ttu-id="e445b-307">Ошибка Chromium: [#997694][CR997694]</span><span class="sxs-lookup"><span data-stu-id="e445b-307">Chromium issue: [#997694][CR997694]</span></span>  

#### <span data-ttu-id="e445b-308">Кнопки "очистить" на панелях "элементы" и "сеть"</span><span class="sxs-lookup"><span data-stu-id="e445b-308">Clear buttons in the Elements and Network panels</span></span>  

<span data-ttu-id="e445b-309">В следующих текстовых полях теперь есть кнопки " **очистить** ".</span><span class="sxs-lookup"><span data-stu-id="e445b-309">The following text boxes now have **Clear** buttons.</span></span>  

*   <span data-ttu-id="e445b-310">Текстовые поля "фильтр" в области " **стили** " и на панели " **сеть** ".</span><span class="sxs-lookup"><span data-stu-id="e445b-310">The filter text boxes in the **Styles** pane and **Network** panel.</span></span>  
*   <span data-ttu-id="e445b-311">Текстовое поле "Поиск DOM" на панели " **элементы** ".</span><span class="sxs-lookup"><span data-stu-id="e445b-311">The DOM search text box in the **Elements** panel.</span></span>  

<span data-ttu-id="e445b-312">Нажмите кнопку **очистить** , чтобы удалить введенный текст.</span><span class="sxs-lookup"><span data-stu-id="e445b-312">Choose the **Clear** button to remove any inputted text.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/clear-button-elements.msft.png" alt-text="Соответствие сочетаний клавиш в DevTools с кодом Visual Studio" lightbox="../../media/2020/08/clear-button-elements.msft.png":::
         <span data-ttu-id="e445b-314">Кнопки "очистить" на панелях **элементов**</span><span class="sxs-lookup"><span data-stu-id="e445b-314">Clear buttons in the **Elements** panels</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/clear-button-network.msft.png" alt-text="Соответствие сочетаний клавиш в DevTools с кодом Visual Studio" lightbox="../../media/2020/08/clear-button-network.msft.png":::
         <span data-ttu-id="e445b-316">Кнопки "очистить" на панели "  **сеть** "</span><span class="sxs-lookup"><span data-stu-id="e445b-316">Clear buttons in the  **Network** panels</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="e445b-317">Ошибка Chromium: [#1067184][CR1067184]</span><span class="sxs-lookup"><span data-stu-id="e445b-317">Chromium issue: [#1067184][CR1067184]</span></span>  

## <span data-ttu-id="e445b-318">Загрузка каналов предварительной версии Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="e445b-318">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="e445b-319">Если вы используете Windows или macOS, рассматривайте в качестве браузера по умолчанию использование [каналов предварительного просмотра Microsoft Edge][MicrosoftEdgePreviewChannels] .</span><span class="sxs-lookup"><span data-stu-id="e445b-319">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="e445b-320">Каналы предварительного просмотра предоставляют доступ к последним функциям DevTools.</span><span class="sxs-lookup"><span data-stu-id="e445b-320">The preview channels give you access to the latest DevTools features.</span></span>  

## <span data-ttu-id="e445b-321">Знакомство с Microsoft Edge DevTools Team</span><span class="sxs-lookup"><span data-stu-id="e445b-321">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- image links -->  

[ImageSettingsIcon]: /microsoft-edge/devtools-guide-chromium/media/settings-icon.msft.png "Значок параметров DevTools"  

<!-- links -->  

[DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsPanel]: ../05/devtools.md#deprecation-of-the-properties-pane-in-the-elements-panel "Устаревшая область свойств на панели "элементы" — новые возможности DevTools (Microsoft Edge 84) | Документы Microsoft"  
[DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures]: ../06/devtools.md#css-grid-debugging-features "Функции отладки сетки CSS: новые возможности DevTools (Microsoft Edge 85) | Документы Microsoft"  

[DevtoolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index "Эмуляция мобильных устройств в Microsoft Edge DevTools | Документы Microsoft"  
[DevtoolsCustomizeShortcuts]: /microsoft-edge/devtools-guide-chromium/customize/shortcuts "Настройка сочетаний клавиш в Microsoft Edge DevTools | Документы Microsoft"  
[DevtoolsExperimentalFeaturesEnableExperimentalApis]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-experimental-apis "Включите экспериментальные API — экспериментальные функции | Документы Microsoft"  
[DevtoolsExperimentalFeaturesEnableNewCssGridDebuggingFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-new-css-grid-debugging-features "Эмуляция: поддержка двух режимов экрана — экспериментальные функции | Документы Microsoft"  
[DevtoolsExperimentalFeaturesEnableSourceOrderViewer]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-source-order-viewer "Включение средства просмотра заказов на исходный номер — экспериментальные функции | Документы Microsoft"
[DevtoolsExperimentalFeaturesEmulationSupportDualScreenMode]: https://review.docs.microsoft.com/microsoft-edge/devtools-guide-chromium/experimental-features?branch=user/zoghadya/dual-screen-experiment#emulation-support-dual-screen-mode "Эмуляция: поддержка двух режимов экрана — экспериментальные функции | Документы Microsoft"  
[DevtoolsExperimentalFeaturesTestingOnFoldableDualScreenDevices]: /microsoft-edge/devtools-guide-chromium/experimental-features#testing-on-foldable-and-dual-screen-devices "Тестирование на складная и устройствах с двумя экранами — экспериментальные функции | Документы Microsoft"  
[DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features#turn-on-experimental-features "Включите экспериментальные функции — экспериментальные функции | Документы Microsoft"  
[DevtoolsConsoleApiTable]: /microsoft-edge/devtools-guide-chromium/console/api#table "Справочник по API для консоли "Таблица" | Документы Microsoft"  
[DevtoolsCoverageIndex]: /microsoft-edge/devtools-guide-chromium/coverage/index "Поиск неиспользуемых кодов JavaScript и CSS с помощью вкладки "покрытие" в Microsoft Edge DevTools | Документы Microsoft"  
[DevtoolsCustomizeIndexDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Ящик — настройка Microsoft Edge DevTools | Документы Microsoft"  
[DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#analyze-rendering-performance-with-the-rendering-tab "Анализ производительности отрисовки с помощью вкладки "рендеринг" — Справка по анализу производительности | Документы Microsoft"  
[DevtoolsMediaIndex]: /microsoft-edge/devtools-guide-chromium/media/index "Просмотр и отладка сведений о проигрывателях мультимедиа | Документы Microsoft"  

[DualScreenIntroductionHowWorkSeam]:  /dual-screen/introduction#how-to-work-with-the-seam "Работа с стыками — введение в работу с устройствами с двумя экранами | Документы Microsoft"  
[DualScreenWebCssMediaSpanning]: /dual-screen/web/css-media-spanning "Функция многоэкранной группировки с экрана в каскадных таблицах CSS | Документы Microsoft"  
[DualScreenWebJavascriptGetwindowsegments]: /dual-screen/web/javascript-getwindowsegments "API getWindowSegments JavaScript для устройств с двумя экранами | Документы Microsoft"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Каналы предварительной версии Microsoft Edge"  

[VisualStudioCode]: https://code.visualstudio.com "Код Visual Studio "  
[VisualStudioCodeShortcutsKeyboardWindows]: https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf "Сочетания клавиш в Visual Studio Code для Windows"  

[MicrosoftSurfaceDevicesDuo]: https://www.microsoft.com/surface/devices/surface-duo "Новая поверхность Surface Duo"  

[EdgeDevToolsTwitterAccount]: https://twitter.com/EdgeDevTools "@EdgeDevTools учетной записи Twitter"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Ошибки Chromium"  

[CR174309]: https://crbug.com/174309 "DevTools: разрешение на настройку сочетаний клавиш и привязок клавиш | Ошибки Chromium"
[CR384968]: https://crbug.com/384968 "Параметр, позволяющий игнорировать локальные шрифты () | Ошибки Chromium"  
[CR772558]: https://crbug.com/772558 "DevTools: обновление до последней версии Lighthouse | Ошибки Chromium"  
[CR807440]: https://crbug.com/807440 "Блокировка хрома с большим количеством SWs | Ошибки Chromium"  
[CR997694]: https://crbug.com/997694 "Запросы XHR с состоянием 302 не отображаются в разделе \ "XHR \" на панели "сеть" | Ошибки Chromium"  
[CR1047356]: https://crbug.com/1047356 "Инструменты сетки/гибкого бокса или таблицы CSS"  
[CR1051466]: https://crbug.com/1051466 "Поддержка отладки COOP/COEP в DevTools | Ошибки Chromium"  
[CR1054281]: https://crbug.com/1054281 "Запрос функции: DevTools должен эмулировать складная и устройства с двумя экранами | Ошибки Chromium"  
[CR1067184]: https://crbug.com/1067184 "Запрос компонента: очистить кнопку "фильтр" в элементах & сети — > фильтрах фильтров | Ошибки Chromium"  
[CR1068116]: https://crbug.com/1068116 "☂ "Доставка проблем" | Ошибки Chromium"  
[CR1080569]: https://crbug.com/1080569 "Acorn не поддерживает логические операторы присваивания | Ошибки Chromium"  
[CR1080589]: https://crbug.com/1080589 "Классификация проблем сторонним лицом или первым абонентом | Ошибки Chromium"  
[CR1086817]: https://crbug.com/1086817 "Acorn не поддерживает цифровые разделители | Ошибки Chromium"  
[CR1090802]: https://crbug.com/1090802 "Имитация изменений состояния простоя из API обнаружения в режиме ожидания | Ошибки Chromium"  
[CR1093227]: https://crbug.com/1093227 "DevTools: Предложите наиболее близкий доступный цвет | Ошибки Chromium"  
[CR1093247]: https://crbug.com/1093247 "Вывод сведений о кадрах на панели приложения | Ошибки Chromium"  
[CR1094406]: https://crbug.com/1094406 "Разработчикам требуется средство просмотра заказов исходного кода на https://webwewant.fyi/wants/64/"  
[CR1096068]: https://crbug.com/1096068 "DevTools: поддерживает эмуляцию предпочтительных возможностей мультимедиа с данными Ошибки Chromium"  
[CR1096481]: https://crbug.com/1096481 "Расположение заголовков вопросов | Ошибки Chromium"  
[CR1100253]: https://crbug.com/1100253 "Клавиша "добавить узел снимка экрана" в контекстном меню элемента | Ошибки Chromium"  
[CR1103316]: https://crbug.com/1103316 "Поиск элементов не resolveNode (выделит текст и т. д.) при первом результатах поиска | Ошибки Chromium"  
[CR1103854]: https://crbug.com/1103854 "Отмена запутывания X-Client-значения данных в средствах разработчика | Ошибки Chromium"  
<!--  [CR1105205]: https://crbug.com/1105205 "Issue 1105205 | Chromium bugs"  -->  
[CR1106221]: https://crbug.com/1106221 "Добавить импортированные шрифты в Автозаполнение" семейство шрифтов "на панели" стили | "| Chromium ошибки "  
[CR1107766]: https://crbug.com/1107766 "Показать сведения о кадрах, созданных с помощью" Window. Open () "в дереве кадров | Chromium ошибки "  
[CR1115011]: https://crbug.com/1115011 "при копировании таблицы из консоли структура таблицы не сохраняется | Chromium ошибки "  
[CR1116085]: https://crbug.com/1116085 "Пожалуйста, вернитесь в инспектор свойств DevTools | Chromium ошибки "  

[CsswgDraftsMediaqueries5DescdefMediaPrefersReducedData]: https://drafts.csswg.org/mediaqueries-5#descdef-media-prefers-reduced-data "предпочитать количество запросов мультимедиа на уровне 5 | Черновики редакторов рабочих групп W3C CSS"  

[GithubGooglechromeLighthouseV620]: https://github.com/GoogleChrome/lighthouse/releases/tag/v6.2.0 "v 6.2.0-GoogleChrome/Lighthouse | GitHub"  

[GoogleDevelopersProtocolBuffers]: https://developers.google.com/protocol-buffers "Буферы протоколов | Разработчики Google"  

[SamsungMobileGalaxyFold]: https://www.samsung.com/us/mobile/galaxy-fold "Galaxy, сгиб | Samsung US"  

[V8FeaturesLogicalAssignment]: https://v8.dev/features/logical-assignment "Логическое назначение | V8"  
[V8FeaturesNumericSeparators]: https://v8.dev/features/numeric-separators "Число разделителей | V8"  

[WebDevCoopCoep]: https://web.dev/coop-coep "Создание изолированного веб-сайта \ "межисточник \" с помощью COOP и COEP | Web. dev"  
[WebDevIdleDetection]: https://web.dev/idle-detection "Обнаружение неактивных пользователей с помощью API обнаружения бездействия | Web. dev"  
[WebDevNonCompositedAnimations]: https://web.dev/non-composited-animations "Предотвращение несложных анимаций | Web. dev"  

> [!NOTE]
> <span data-ttu-id="e445b-382">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e445b-382">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="e445b-383">Исходная страница [будет найдена, и](https://developers.google.com/web/updates/2020/08/devtools/index) ее можно создать с помощью [Jecelyn Yeen][JecelynYeen] \ (разработчик отвечает, Chrome DevTools \).</span><span class="sxs-lookup"><span data-stu-id="e445b-383">The original page is found [here](https://developers.google.com/web/updates/2020/08/devtools/index) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="e445b-385">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e445b-385">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
