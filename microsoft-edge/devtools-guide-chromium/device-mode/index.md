---
description: Используйте виртуальные устройства в Microsoft Edge для создания веб-сайтов для мобильных устройств.
title: Эмуляция мобильных устройств в Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools, Эмуляция, устройство, Эмуляция, мобильный
ms.openlocfilehash: 8b636a20fcb1c55630009031ec8bf300624d03d7
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125106"
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

# <span data-ttu-id="4ce47-104">Эмуляция мобильных устройств в Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="4ce47-104">Emulate mobile devices in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="4ce47-105">Использование **эмуляции устройства** для оценки того, как страница выглядит и отвечает на мобильном устройстве.</span><span class="sxs-lookup"><span data-stu-id="4ce47-105">Use **Device emulation** to approximate how your page looks and responds on a mobile device.</span></span>  <span data-ttu-id="4ce47-106">Microsoft Edge DevTools предоставляет набор функций, которые помогут вам эмулировать мобильные устройства.</span><span class="sxs-lookup"><span data-stu-id="4ce47-106">The Microsoft Edge DevTools provide a collection of features to help you emulate mobile devices.</span></span>  <span data-ttu-id="4ce47-107">Коллекция включает следующие функции.</span><span class="sxs-lookup"><span data-stu-id="4ce47-107">The collection includes the following features.</span></span>  

*   [<span data-ttu-id="4ce47-108">Имитация окна просмотра для мобильных устройств</span><span class="sxs-lookup"><span data-stu-id="4ce47-108">Simulate a mobile viewport</span></span>](#simulate-a-mobile-viewport)  
*   [<span data-ttu-id="4ce47-109">Регулирование сети</span><span class="sxs-lookup"><span data-stu-id="4ce47-109">Throttle the network</span></span>](#throttle-the-network-only)  
*   [<span data-ttu-id="4ce47-110">Регулирование ЦП</span><span class="sxs-lookup"><span data-stu-id="4ce47-110">Throttle the CPU</span></span>](#throttle-the-cpu-only)  
*   [<span data-ttu-id="4ce47-111">Имитация географического положения</span><span class="sxs-lookup"><span data-stu-id="4ce47-111">Simulate geolocation</span></span>](#override-geolocation)  
*   [<span data-ttu-id="4ce47-112">Настройка ориентации</span><span class="sxs-lookup"><span data-stu-id="4ce47-112">Set orientation</span></span>](#set-orientation)  
*   [<span data-ttu-id="4ce47-113">Установка строки агента пользователя</span><span class="sxs-lookup"><span data-stu-id="4ce47-113">Set the user agent string</span></span>](#set-user-agent-string)  

## <span data-ttu-id="4ce47-114">Ограничения</span><span class="sxs-lookup"><span data-stu-id="4ce47-114">Limitations</span></span>  

<span data-ttu-id="4ce47-115">**Эмуляция устройства** — это [приближенная аппроксимация][WikiApproximation] внешнего вида и функций страницы на мобильном устройстве.</span><span class="sxs-lookup"><span data-stu-id="4ce47-115">**Device emulation** is a [first-order approximation][WikiApproximation] of the look and feel of your page on a mobile device.</span></span>  <span data-ttu-id="4ce47-116">**Эмуляция устройства** фактически не запускает ваш код на мобильном устройстве.</span><span class="sxs-lookup"><span data-stu-id="4ce47-116">**Device emulation** does not actually run your code on a mobile device.</span></span>  <span data-ttu-id="4ce47-117">Вместо этого вы имитируете взаимодействие с пользователем на мобильном устройстве или компьютере.</span><span class="sxs-lookup"><span data-stu-id="4ce47-117">Instead you simulate the mobile user experience from your laptop or desktop.</span></span>  

<span data-ttu-id="4ce47-118">Некоторые аспекты мобильных устройств не имитируются в DevTools.</span><span class="sxs-lookup"><span data-stu-id="4ce47-118">Some aspects of mobile devices are never emulated in DevTools.</span></span>  <span data-ttu-id="4ce47-119">Например, архитектура мобильных процессоров отличается от архитектуры компьютеров или процессоров для настольных ПК.</span><span class="sxs-lookup"><span data-stu-id="4ce47-119">For example, the architecture of mobile CPUs is different than the architecture of laptop or desktop CPUs.</span></span>  <span data-ttu-id="4ce47-120">Если вы сомневаетесь, лучше использовать страницу на мобильном устройстве.</span><span class="sxs-lookup"><span data-stu-id="4ce47-120">When in doubt, your best bet is to actually run your page on a mobile device.</span></span>  <span data-ttu-id="4ce47-121">Используйте [удаленную отладку] [DevToolsRemoteDebugging], чтобы взаимодействовать с кодом страницы с компьютера, когда страница фактически выполняется на мобильном устройстве.</span><span class="sxs-lookup"><span data-stu-id="4ce47-121">Use [Remote Debugging][DevToolsRemoteDebugging] to interact with the code of a page from your machine while your page actually runs on a mobile device.</span></span>  <span data-ttu-id="4ce47-122">Вы можете просматривать, изменять, выполнять отладку или все четыре сеанса, пока вы не будете взаимодействовать с этим кодом.</span><span class="sxs-lookup"><span data-stu-id="4ce47-122">You may view, change, debug, profile, or all four while you interact with the code.</span></span>  <span data-ttu-id="4ce47-123">Ваш компьютер может представлять собой записную книжку или настольный компьютер.</span><span class="sxs-lookup"><span data-stu-id="4ce47-123">Your machine may be a notebook or desktop computer.</span></span>  

## <span data-ttu-id="4ce47-124">Имитация окна просмотра для мобильных устройств</span><span class="sxs-lookup"><span data-stu-id="4ce47-124">Simulate a mobile viewport</span></span>  

<span data-ttu-id="4ce47-125">Нажмите кнопку **Переключить эмуляцию устройства**  \ ( ![ Переключить панель инструментов устройства ][ImageDeviceToolbarIcon] ) или щелкните **настроить DevTools** \ ( `...` \) > **эмуляцию устройства** , чтобы открыть пользовательский интерфейс, позволяющий имитировать окно просмотра для мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="4ce47-125">Choose **Toggle device emulation**  \(![Toggle Device Toolbar][ImageDeviceToolbarIcon]\) or choose **Customize and control DevTools** \(`...`\) > **Device emulation** to open the UI that enables you to simulate a mobile viewport.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="Панель инструментов &quot;устройства&quot;" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
    <span data-ttu-id="4ce47-127">Панель инструментов "устройства"</span><span class="sxs-lookup"><span data-stu-id="4ce47-127">The Device Toolbar</span></span>  
:::image-end:::  

<span data-ttu-id="4ce47-128">По умолчанию панель инструментов устройства открывается в режиме отклика окна просмотра.</span><span class="sxs-lookup"><span data-stu-id="4ce47-128">By default the Device Toolbar opens in Responsive Viewport Mode.</span></span>  

### <span data-ttu-id="4ce47-129">Режим окна просмотра с откликом</span><span class="sxs-lookup"><span data-stu-id="4ce47-129">Responsive Viewport Mode</span></span>  

<span data-ttu-id="4ce47-130">Чтобы быстро проверить внешний вид страницы на нескольких размерах экрана, перетащите маркеры, чтобы изменить размер окна просмотра до нужных размеров.</span><span class="sxs-lookup"><span data-stu-id="4ce47-130">To quickly test the look and feel of your page across multiple screen sizes, drag the handles to resize the viewport to your required dimensions.</span></span>  <span data-ttu-id="4ce47-131">Вы также можете ввести определенные значения в полях Ширина и высота.</span><span class="sxs-lookup"><span data-stu-id="4ce47-131">You may also enter specific values in the width and height boxes.</span></span>  <span data-ttu-id="4ce47-132">На приведенном ниже рисунке задана ширина `626` и высота задана `516` .</span><span class="sxs-lookup"><span data-stu-id="4ce47-132">In the following figure, the width is set to `626` and the height is set to `516`.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-handles-highlighted.msft.png" alt-text="Панель инструментов &quot;устройства&quot;" lightbox="../media/device-mode-toggle-device-toolbar-handles-highlighted.msft.png":::
    <span data-ttu-id="4ce47-134">Дескрипторы для изменения размеров окна просмотра в отклике режима просмотра</span><span class="sxs-lookup"><span data-stu-id="4ce47-134">The handles for changing the dimensions of the viewport when in Responsive Viewport Mode</span></span>  
:::image-end:::  

#### <span data-ttu-id="4ce47-135">Показать мультимедийные запросы</span><span class="sxs-lookup"><span data-stu-id="4ce47-135">Show media queries</span></span>  

<span data-ttu-id="4ce47-136">Если вы определили на странице запросы мультимедиа, переходите к измерениям просмотра, в которых эти запросы мультимедиа вступают в силу, отображая точки останова в запросах мультимедиа над окном просмотра.</span><span class="sxs-lookup"><span data-stu-id="4ce47-136">If you have defined media queries on your page, jump to the viewport dimensions where those media queries take effect by showing media query breakpoints above your viewport.</span></span>  <span data-ttu-id="4ce47-137">Нажмите кнопку **Дополнительные параметры**  >  , чтобы**отобразить запросы мультимедиа**.</span><span class="sxs-lookup"><span data-stu-id="4ce47-137">Choose **More options** > **Show media queries**.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-options-show-media-queries.msft.png" alt-text="Панель инструментов &quot;устройства&quot;" lightbox="../media/device-mode-toggle-device-toolbar-more-options-show-media-queries.msft.png":::
   **<span data-ttu-id="4ce47-139">Показать мультимедийные запросы</span><span class="sxs-lookup"><span data-stu-id="4ce47-139">Show media queries</span></span>**  
:::image-end:::  

<span data-ttu-id="4ce47-140">Выберите точку останова, чтобы изменить ширину окна просмотра таким образом, чтобы был запущен запрос мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="4ce47-140">Choose a breakpoint to change the width of the viewport so that the media query gets triggered.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-click-breakpoint.msft.png" alt-text="Панель инструментов &quot;устройства&quot;" lightbox="../media/device-mode-toggle-device-toolbar-click-breakpoint.msft.png":::
   <span data-ttu-id="4ce47-142">Выбор точки останова для изменения ширины окна просмотра</span><span class="sxs-lookup"><span data-stu-id="4ce47-142">Choose a breakpoint to change the width of the viewport</span></span>  
:::image-end:::  

#### <span data-ttu-id="4ce47-143">Настройка типа устройства</span><span class="sxs-lookup"><span data-stu-id="4ce47-143">Set the device type</span></span>  

<span data-ttu-id="4ce47-144">Используйте список **типов устройств** для имитации мобильного устройства или настольного устройства.</span><span class="sxs-lookup"><span data-stu-id="4ce47-144">Use the **Device Type** list to simulate a mobile device or desktop device.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-type-list.msft.png" alt-text="Панель инструментов &quot;устройства&quot;" lightbox="../media/device-mode-toggle-device-toolbar-device-type-list.msft.png":::
   <span data-ttu-id="4ce47-146">Список **типов устройств**</span><span class="sxs-lookup"><span data-stu-id="4ce47-146">The **Device Type** list</span></span>  
:::image-end:::  

<span data-ttu-id="4ce47-147">В приведенной ниже таблице описаны различия между доступными параметрами типа устройства.</span><span class="sxs-lookup"><span data-stu-id="4ce47-147">The following table describes the differences between the available device type options.</span></span>  <span data-ttu-id="4ce47-148">Столбец «метод рендеринга» указывает, будет ли Microsoft Edge обрабатывать страницу в качестве окна просмотра на мобильном или рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="4ce47-148">The Rendering method column refers to whether Microsoft Edge renders the page as a mobile or desktop viewport.</span></span>  <span data-ttu-id="4ce47-149">Столбец значка курсора указывает на тип курсора, который отображается при наведении указателя на страницу.</span><span class="sxs-lookup"><span data-stu-id="4ce47-149">The Cursor icon column refers to what type of cursor you see when you hover on the page.</span></span>  <span data-ttu-id="4ce47-150">Столбец, в котором запущены события, указывает на то, следует ли выполнять триггеры страницы `touch` или `click` события при взаимодействии со страницей.</span><span class="sxs-lookup"><span data-stu-id="4ce47-150">The Events triggered column refers to whether the page triggers `touch` or `click` events when you interact with the page.</span></span>  

| <span data-ttu-id="4ce47-151">Параметр</span><span class="sxs-lookup"><span data-stu-id="4ce47-151">Option</span></span> | <span data-ttu-id="4ce47-152">Метод отрисовки</span><span class="sxs-lookup"><span data-stu-id="4ce47-152">Rendering method</span></span> | <span data-ttu-id="4ce47-153">Значок курсора</span><span class="sxs-lookup"><span data-stu-id="4ce47-153">Cursor icon</span></span> | <span data-ttu-id="4ce47-154">Инициированные события</span><span class="sxs-lookup"><span data-stu-id="4ce47-154">Events triggered</span></span> |  
|:--- |:--- |:--- |:--- |  
| <span data-ttu-id="4ce47-155">Мобильные устройства</span><span class="sxs-lookup"><span data-stu-id="4ce47-155">Mobile</span></span> | <span data-ttu-id="4ce47-156">Мобильные устройства</span><span class="sxs-lookup"><span data-stu-id="4ce47-156">Mobile</span></span> | <span data-ttu-id="4ce47-157">Круг</span><span class="sxs-lookup"><span data-stu-id="4ce47-157">Circle</span></span> | <span data-ttu-id="4ce47-158">Сенсорный ввод</span><span class="sxs-lookup"><span data-stu-id="4ce47-158">touch</span></span> |  
| <span data-ttu-id="4ce47-159">Мобильный – (без сенсорных устройств)</span><span class="sxs-lookup"><span data-stu-id="4ce47-159">Mobile \(no touch\)</span></span> | <span data-ttu-id="4ce47-160">Мобильные устройства</span><span class="sxs-lookup"><span data-stu-id="4ce47-160">Mobile</span></span> | <span data-ttu-id="4ce47-161">Обычный</span><span class="sxs-lookup"><span data-stu-id="4ce47-161">Normal</span></span> | <span data-ttu-id="4ce47-162"> нажмите </span><span class="sxs-lookup"><span data-stu-id="4ce47-162">click</span></span> |  
| <span data-ttu-id="4ce47-163">Desktop</span><span class="sxs-lookup"><span data-stu-id="4ce47-163">Desktop</span></span> | <span data-ttu-id="4ce47-164">Desktop</span><span class="sxs-lookup"><span data-stu-id="4ce47-164">Desktop</span></span> | <span data-ttu-id="4ce47-165">Обычный</span><span class="sxs-lookup"><span data-stu-id="4ce47-165">Normal</span></span> | <span data-ttu-id="4ce47-166"> нажмите </span><span class="sxs-lookup"><span data-stu-id="4ce47-166">click</span></span> |  
| <span data-ttu-id="4ce47-167">Классическое приложение (касание)</span><span class="sxs-lookup"><span data-stu-id="4ce47-167">Desktop \(touch\)</span></span> | <span data-ttu-id="4ce47-168">Desktop</span><span class="sxs-lookup"><span data-stu-id="4ce47-168">Desktop</span></span> | <span data-ttu-id="4ce47-169">Круг</span><span class="sxs-lookup"><span data-stu-id="4ce47-169">Circle</span></span> | <span data-ttu-id="4ce47-170">Сенсорный ввод</span><span class="sxs-lookup"><span data-stu-id="4ce47-170">touch</span></span> |  

> [!NOTE]
> <span data-ttu-id="4ce47-171">Если список **тип устройства** не отображается, выберите пункт **Дополнительные параметры**  >  **Добавить тип устройства**.</span><span class="sxs-lookup"><span data-stu-id="4ce47-171">If the **Device Type** list is not displayed, choose **More options** > **Add device type**.</span></span>  

### <span data-ttu-id="4ce47-172">Режим просмотра на мобильном устройстве</span><span class="sxs-lookup"><span data-stu-id="4ce47-172">Mobile Device Viewport Mode</span></span>  

<span data-ttu-id="4ce47-173">Чтобы смоделировать размеры определенного мобильного устройства, выберите нужное устройство из списка **устройств** .</span><span class="sxs-lookup"><span data-stu-id="4ce47-173">To simulate the dimensions of a specific mobile device, select the device from the **Device** list.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-list.msft.png" alt-text="Панель инструментов &quot;устройства&quot;" lightbox="../media/device-mode-toggle-device-toolbar-device-list.msft.png":::
   <span data-ttu-id="4ce47-175">Список **устройств**</span><span class="sxs-lookup"><span data-stu-id="4ce47-175">The **Device** list</span></span>  
:::image-end:::  

#### <span data-ttu-id="4ce47-176">Поворот окна просмотра на альбомную ориентацию</span><span class="sxs-lookup"><span data-stu-id="4ce47-176">Rotate the viewport to landscape orientation</span></span>  

<span data-ttu-id="4ce47-177">Протестируйте веб-страницу в альбомной ориентации.</span><span class="sxs-lookup"><span data-stu-id="4ce47-177">Test your webpage in landscape orientation.</span></span>  

*   <span data-ttu-id="4ce47-178">Чтобы повернуть окно просмотра на альбомную ориентацию, нажмите кнопку **повернуть** \ ( ![ повернуть ][ImageRotateIcon] \).</span><span class="sxs-lookup"><span data-stu-id="4ce47-178">To rotate the viewport to landscape orientation, choose **Rotate** \(![Rotate][ImageRotateIcon]\).</span></span>  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-landscape.msft.png" alt-text="Панель инструментов &quot;устройства&quot;" lightbox="../media/device-mode-toggle-device-toolbar-landscape.msft.png":::
       <span data-ttu-id="4ce47-180">Страница отображается в альбомной ориентации</span><span class="sxs-lookup"><span data-stu-id="4ce47-180">Page displayed in landscape orientation</span></span>  
    :::image-end:::  
    
> [!NOTE]
> <span data-ttu-id="4ce47-181">Кнопка **повернуть** исчезнет, если **панель инструментов на устройстве** является узкой.</span><span class="sxs-lookup"><span data-stu-id="4ce47-181">The **Rotate** button disappears if your **Device Toolbar** is narrow.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="Панель инструментов &quot;устройства&quot;" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
   <span data-ttu-id="4ce47-183">**Панель инструментов "устройства** "</span><span class="sxs-lookup"><span data-stu-id="4ce47-183">The **Device Toolbar**</span></span>  
:::image-end:::  

<span data-ttu-id="4ce47-184">Дополнительные сведения можно найти на странице [Настройка ориентации](#set-orientation).</span><span class="sxs-lookup"><span data-stu-id="4ce47-184">For more information, go to [Set orientation](#set-orientation).</span></span>  

#### <span data-ttu-id="4ce47-185">Показать рамку устройства</span><span class="sxs-lookup"><span data-stu-id="4ce47-185">Show device frame</span></span>  

<span data-ttu-id="4ce47-186">Показывать рамку физического устройства вокруг окна просмотра, когда вы моделируете размеры определенного мобильного устройства, например iPhone 6.</span><span class="sxs-lookup"><span data-stu-id="4ce47-186">Display the physical device frame around the viewport when you simulate the dimensions of a specific mobile device such as an iPhone 6.</span></span>  

1.  <span data-ttu-id="4ce47-187">Откройте **диалоговое окно Дополнительные параметры**.</span><span class="sxs-lookup"><span data-stu-id="4ce47-187">Open **More options**.</span></span>  
1.  <span data-ttu-id="4ce47-188">Выберите пункт **Показать рамку устройства**.</span><span class="sxs-lookup"><span data-stu-id="4ce47-188">Choose **Show device frame**.</span></span>  

> [!NOTE]
> <span data-ttu-id="4ce47-189">Если вы не видите рамку устройства для определенного устройства, это означает, что DevTools не имеет рисунка для этого параметра.</span><span class="sxs-lookup"><span data-stu-id="4ce47-189">If you do not see a device frame for a particular device, it means that DevTools does not have art for that option.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-option-show-device-frame.msft.png" alt-text="Панель инструментов &quot;устройства&quot;" lightbox="../media/device-mode-toggle-device-toolbar-option-show-device-frame.msft.png":::
         <span data-ttu-id="4ce47-191">Показать рамку устройства</span><span class="sxs-lookup"><span data-stu-id="4ce47-191">Show device frame</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-options-device-frame-iphone-6.msft.png" alt-text="Панель инструментов &quot;устройства&quot;" lightbox="../media/device-mode-toggle-device-toolbar-options-device-frame-iphone-6.msft.png":::
         <span data-ttu-id="4ce47-193">Рамка устройства для iPhone 6</span><span class="sxs-lookup"><span data-stu-id="4ce47-193">The device frame for the iPhone 6</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

#### <span data-ttu-id="4ce47-194">Добавление настраиваемого мобильного устройства</span><span class="sxs-lookup"><span data-stu-id="4ce47-194">Add a custom mobile device</span></span>  

<span data-ttu-id="4ce47-195">Если необходимый параметр мобильного устройства отсутствует в списке по умолчанию, вы можете добавить настраиваемое устройство.</span><span class="sxs-lookup"><span data-stu-id="4ce47-195">If the mobile device option that you need is not included on the default list, you may add a custom device.</span></span>  <span data-ttu-id="4ce47-196">Чтобы добавить настраиваемое устройство, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="4ce47-196">To add a custom device, complete the following steps.</span></span>  

1.  <span data-ttu-id="4ce47-197">Выберите список **устройств** > **изменить**.</span><span class="sxs-lookup"><span data-stu-id="4ce47-197">Choose the **Device** list > **Edit**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-list-edit.msft.png" alt-text="Панель инструментов &quot;устройства&quot;" lightbox="../media/device-mode-toggle-device-toolbar-device-list-edit.msft.png":::
       <span data-ttu-id="4ce47-199">Нажмите кнопку **изменить** .</span><span class="sxs-lookup"><span data-stu-id="4ce47-199">Choose **Edit**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="4ce47-200">Выберите **Добавить настраиваемое устройство**.</span><span class="sxs-lookup"><span data-stu-id="4ce47-200">Choose **Add custom device**.</span></span>  
1.  <span data-ttu-id="4ce47-201">На **эмулированных устройствах**введите имя устройства, ширину экрана и высоту экрана для настраиваемого устройства.</span><span class="sxs-lookup"><span data-stu-id="4ce47-201">On **Emulated Devices**, enter a device name, screen width, and screen height for the custom device.</span></span>  <span data-ttu-id="4ce47-202">Поля « [отношение к пикселям][MDNWindowDevicePixelRatio]», « [строка агента пользователя][MDNUserAgent]» и « [тип устройства](#set-the-device-type) » являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="4ce47-202">The [device pixel ratio][MDNWindowDevicePixelRatio], [user agent string][MDNUserAgent], and [device type](#set-the-device-type) fields are optional.</span></span>  <span data-ttu-id="4ce47-203">Поле «Тип устройства» по умолчанию имеет значение **мобильный**.</span><span class="sxs-lookup"><span data-stu-id="4ce47-203">The device type field defaults to **Mobile**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-settings-emulated-devices-add.msft.png" alt-text="Панель инструментов &quot;устройства&quot;" lightbox="../media/device-mode-toggle-device-toolbar-settings-emulated-devices-add.msft.png":::
       <span data-ttu-id="4ce47-205">Создание настраиваемого устройства</span><span class="sxs-lookup"><span data-stu-id="4ce47-205">Create a custom device</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="4ce47-206">Отображение линеек</span><span class="sxs-lookup"><span data-stu-id="4ce47-206">Show rulers</span></span>  

<span data-ttu-id="4ce47-207">Если требуется измерение размеров экрана, вы можете использовать линейки для измерения размера экрана в пикселях.</span><span class="sxs-lookup"><span data-stu-id="4ce47-207">If you need to measure screen dimensions, you may use rulers to measure the screen size in pixels.</span></span>  <span data-ttu-id="4ce47-208">Нажмите кнопку **Дополнительные параметры**  >  , чтобы отобразить**линейки** сверху и слева от окна просмотра.</span><span class="sxs-lookup"><span data-stu-id="4ce47-208">Choose **More options** > **Show rulers** to display rulers above and to the left of your viewport.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-options-show-rulers.msft.png" alt-text="Панель инструментов &quot;устройства&quot;" lightbox="../media/device-mode-toggle-device-toolbar-options-show-rulers.msft.png":::
         <span data-ttu-id="4ce47-210">Элемент меню для отображения линеек</span><span class="sxs-lookup"><span data-stu-id="4ce47-210">Menu item to display rulers</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-rulers.msft.png" alt-text="Панель инструментов &quot;устройства&quot;" lightbox="../media/device-mode-toggle-device-toolbar-rulers.msft.png":::
         <span data-ttu-id="4ce47-212">Линейки сверху и слева от окна просмотра</span><span class="sxs-lookup"><span data-stu-id="4ce47-212">Rulers above and to the left of the viewport</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="4ce47-213">Изменение масштаба просмотра</span><span class="sxs-lookup"><span data-stu-id="4ce47-213">Zoom the viewport</span></span>  

<span data-ttu-id="4ce47-214">Для проверки внешнего вида страницы на нескольких уровнях масштабирования используйте в списке **масштаб** , чтобы увеличить или уменьшить масштаб.</span><span class="sxs-lookup"><span data-stu-id="4ce47-214">To test the look and feel of your page at multiple zoom levels, use the **Zoom** list to zoom in or out.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-zoom.msft.png" alt-text="Панель инструментов &quot;устройства&quot;" lightbox="../media/device-mode-toggle-device-toolbar-zoom.msft.png":::
   **<span data-ttu-id="4ce47-216">Масштаб</span><span class="sxs-lookup"><span data-stu-id="4ce47-216">Zoom</span></span>**  
:::image-end:::  

## <span data-ttu-id="4ce47-217">Регулирование сети и ЦП</span><span class="sxs-lookup"><span data-stu-id="4ce47-217">Throttle the network and CPU</span></span>  

<span data-ttu-id="4ce47-218">Для мобильных устройств часто используются ограничения сети и ЦП.</span><span class="sxs-lookup"><span data-stu-id="4ce47-218">Mobile devices often have network and CPU constraints.</span></span>  <span data-ttu-id="4ce47-219">Убедитесь, что вы протестируете, как быстро загружается страница и как она реагирует на разные скорости в Интернете и ЦП.</span><span class="sxs-lookup"><span data-stu-id="4ce47-219">Ensure you test how quickly your page loads and how it responds at different internet and CPU speeds.</span></span>  

<span data-ttu-id="4ce47-220">Регулирование сети и ЦП.</span><span class="sxs-lookup"><span data-stu-id="4ce47-220">Throttle the network and CPU.</span></span>  

1.  <span data-ttu-id="4ce47-221">Выберите пункт **перерегулировать** список и измените стиль на " **средний" Мобильный** или **низкий уровень мобильного**.</span><span class="sxs-lookup"><span data-stu-id="4ce47-221">Choose **Throttle** list and change the preset to **Mid-tier mobile** or **Low-end mobile**.</span></span>  
    *   <span data-ttu-id="4ce47-222">**Мобильные видеосвязи** моделируются и заменяют `fast 3G` ЦП.</span><span class="sxs-lookup"><span data-stu-id="4ce47-222">**Mid-tier mobile** simulates `fast 3G` and throttles your CPU.</span></span>  <span data-ttu-id="4ce47-223">Это происходит четыре часа ниже, чем обычно.</span><span class="sxs-lookup"><span data-stu-id="4ce47-223">It is four times slower than normal.</span></span>  
    *   <span data-ttu-id="4ce47-224">С помощью низкоуровневых эмуляций на **мобильном устройстве** осуществляется `slow 3G` регулирование центрального процессора.</span><span class="sxs-lookup"><span data-stu-id="4ce47-224">**Low-end mobile** simulates `slow 3G` and throttles your CPU.</span></span>  <span data-ttu-id="4ce47-225">Оно не менее шести, чем обычно.</span><span class="sxs-lookup"><span data-stu-id="4ce47-225">It is six times slower than normal.</span></span>  
    
<span data-ttu-id="4ce47-226">Все регулировки зависят от нормальной работы ноутбука или настольного компьютера.</span><span class="sxs-lookup"><span data-stu-id="4ce47-226">All of the throttling is based upon the normal capability of your laptop or desktop.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-throttle.msft.png" alt-text="Панель инструментов &quot;устройства&quot;" lightbox="../media/device-mode-toggle-device-toolbar-throttle.msft.png":::
   <span data-ttu-id="4ce47-228">Список **регулирования** на панели инструментов устройства</span><span class="sxs-lookup"><span data-stu-id="4ce47-228">The **Throttle** list in the Device Toolbar</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="4ce47-229">Если **список регулирования** скрыт, **панель инструментов устройства** слишком мала.</span><span class="sxs-lookup"><span data-stu-id="4ce47-229">If the **Throttle list** is hidden, your **Device Toolbar** is too narrow.</span></span>  <span data-ttu-id="4ce47-230">Чтобы получить доступ к **списку регулирования**, увеличите ширину **панели инструментов устройства**.</span><span class="sxs-lookup"><span data-stu-id="4ce47-230">To access the **Throttle list**, increase the width of the **Device Toolbar**.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="Панель инструментов &quot;устройства&quot;" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
   <span data-ttu-id="4ce47-232">**Панель инструментов "устройства** "</span><span class="sxs-lookup"><span data-stu-id="4ce47-232">The **Device Toolbar**</span></span>  
:::image-end:::  

### <span data-ttu-id="4ce47-233">Регулирование только ЦП</span><span class="sxs-lookup"><span data-stu-id="4ce47-233">Throttle the CPU only</span></span>  

<span data-ttu-id="4ce47-234">Чтобы перерегулировать только ЦП, а не сеть, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="4ce47-234">To throttle the CPU only and not the network, complete the following steps.</span></span>

1.  <span data-ttu-id="4ce47-235">Выберите панель " **производительность** " и нажмите кнопку " **Параметры** захвата ![ " (параметры записи ][ImageCaptureIcon] ).</span><span class="sxs-lookup"><span data-stu-id="4ce47-235">Choose the **Performance** panel, and choose **Capture Settings** \(![Capture Settings][ImageCaptureIcon]\).</span></span>
1.  <span data-ttu-id="4ce47-236">Выберите **ЦП**  >  **4X** или **6X замедление**.</span><span class="sxs-lookup"><span data-stu-id="4ce47-236">Choose **CPU** > **4x slowdown** or **6x slowdown**.</span></span>
    
    :::image type="complex" source="../media/device-mode-performance-cpu-throttle.msft.png" alt-text="Панель инструментов &quot;устройства&quot;" lightbox="../media/device-mode-performance-cpu-throttle.msft.png":::
       <span data-ttu-id="4ce47-238">Список **ЦП** на панели " **производительность** "</span><span class="sxs-lookup"><span data-stu-id="4ce47-238">The **CPU** list in the **Performance** panel</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="4ce47-239">Регулирование сети только</span><span class="sxs-lookup"><span data-stu-id="4ce47-239">Throttle the network only</span></span>  

<span data-ttu-id="4ce47-240">Чтобы перерегулировать сеть, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="4ce47-240">To throttle the network only, complete the following steps.</span></span>

1.  <span data-ttu-id="4ce47-241">Выберите панель **Network (сеть** ).</span><span class="sxs-lookup"><span data-stu-id="4ce47-241">Choose the **Network** panel.</span></span>
1.  <span data-ttu-id="4ce47-242">Выберите **онлайновый режим**  >  **3G** или **медленное 3G**.</span><span class="sxs-lookup"><span data-stu-id="4ce47-242">Choose **Online** > **Fast 3G** or **Slow 3G**.</span></span>
    
    :::image type="complex" source="../media/device-mode-network-throttle.msft.png" alt-text="Панель инструментов &quot;устройства&quot;" lightbox="../media/device-mode-network-throttle.msft.png":::
       <span data-ttu-id="4ce47-244">Список **регулирования** на панели "сеть"</span><span class="sxs-lookup"><span data-stu-id="4ce47-244">The **Throttle** list in the Network panel</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="4ce47-245">Или выберите `Control` + `Shift` + `P` \ (Windows, Linux \) или `Command` + `Shift` + `P` \ (macOS \), чтобы открыть **меню команд**, введите `3G` и выберите **включить быстрое регулирование сети 3G** или **включить медленное регулирование сети 3G**.</span><span class="sxs-lookup"><span data-stu-id="4ce47-245">Or select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**, type `3G`, and choose **Enable fast 3G throttling** or **Enable slow 3G throttling**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-command-menu-throttle.msft.png" alt-text="Панель инструментов &quot;устройства&quot;" lightbox="../media/device-mode-command-menu-throttle.msft.png":::
       <span data-ttu-id="4ce47-247">**Меню команд**</span><span class="sxs-lookup"><span data-stu-id="4ce47-247">The **Command Menu**</span></span>  
    :::image-end:::  
    
<span data-ttu-id="4ce47-248">Вы также можете настроить регулирование сети на панели **Performance** .</span><span class="sxs-lookup"><span data-stu-id="4ce47-248">You may also set network throttling from the **Performance** panel.</span></span>  

1.  <span data-ttu-id="4ce47-249">Выберите **Параметры захвата** \ ( ![ Параметры захвата ][ImageCaptureIcon] ) и щелкните список **сетей** и измените стиль на " **Быстрый 3G** " или " **медленный 3G**".</span><span class="sxs-lookup"><span data-stu-id="4ce47-249">Choose **Capture Settings** \(![Capture Settings][ImageCaptureIcon]\) and choose the **Network** list and change the preset to **Fast 3G** or **Slow 3G**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-performance-network-throttle.msft.png" alt-text="Панель инструментов &quot;устройства&quot;" lightbox="../media/device-mode-performance-network-throttle.msft.png":::
       <span data-ttu-id="4ce47-251">Настройка регулирования сети с помощью панели " **производительность** "</span><span class="sxs-lookup"><span data-stu-id="4ce47-251">Set network throttling from the **Performance** panel</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="4ce47-252">Переопределение геолокации</span><span class="sxs-lookup"><span data-stu-id="4ce47-252">Override geolocation</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="4ce47-253">Если страница зависит от данных географического расположения на мобильном устройстве, для правильного отображения укажите различные географическое положение с помощью пользовательского интерфейса переопределения географического расположения.</span><span class="sxs-lookup"><span data-stu-id="4ce47-253">If your page depends on geolocation information from a mobile device to render properly, provide different geolocations using the geolocation overriding UI.</span></span>  

      1.  <span data-ttu-id="4ce47-254">Нажмите кнопку **Настройка и** выберите пункт DevTools \ ( `...` \) > **другие инструменты**  >  **датчики**.</span><span class="sxs-lookup"><span data-stu-id="4ce47-254">Choose **Customize and control DevTools** \(`...`\) > **More tools** > **Sensors**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png" alt-text="Панель инструментов &quot;устройства&quot;" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png":::
         <span data-ttu-id="4ce47-256">**Датчики** для географического местоположения</span><span class="sxs-lookup"><span data-stu-id="4ce47-256">**Sensors** for geolocation</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      1.  <span data-ttu-id="4ce47-257">Открытие меню команд.</span><span class="sxs-lookup"><span data-stu-id="4ce47-257">Open the Command Menu.</span></span>  
          *   <span data-ttu-id="4ce47-258">Выберите `Control` + `Shift` + `P` \ (Windows, Linux \) или `Command` + `Shift` + `P` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="4ce47-258">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\).</span></span>  
      1. <span data-ttu-id="4ce47-259">Введите текст `Sensors` и выберите пункт **Показать датчики**.</span><span class="sxs-lookup"><span data-stu-id="4ce47-259">Type `Sensors`, and choose **Show Sensors**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png" alt-text="Панель инструментов &quot;устройства&quot;" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png":::
         <span data-ttu-id="4ce47-261">**Показать датчики** для географического положения</span><span class="sxs-lookup"><span data-stu-id="4ce47-261">**Show Sensors** for geolocation</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="4ce47-262">На панели **Sensors (датчики** ) вы можете выбрать одно из расположений, указанных в DevTools, с помощью раскрывающегося меню **Расположение** .</span><span class="sxs-lookup"><span data-stu-id="4ce47-262">On the **Sensors** panel, you may select one of the preset locations included in DevTools using the **Location** drop-down menu.</span></span>  <span data-ttu-id="4ce47-263">Чтобы ввести другое расположение, выберите пункт **другие...**</span><span class="sxs-lookup"><span data-stu-id="4ce47-263">To enter a custom location, choose **Other…**</span></span> <span data-ttu-id="4ce47-264">и введите координаты вашего собственного местоположения.</span><span class="sxs-lookup"><span data-stu-id="4ce47-264">and enter the coordinates of your custom location.</span></span>  <span data-ttu-id="4ce47-265">Чтобы протестировать страницу в состоянии ошибки, если сведения о расположении недоступны, выберите пункт **расположение недоступно**.</span><span class="sxs-lookup"><span data-stu-id="4ce47-265">To test your page in an error state when location information is unavailable, choose **Location unavailable**.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-sensors-tokyo.msft.png" alt-text="Панель инструментов &quot;устройства&quot;" lightbox="../media/device-mode-toggle-device-toolbar-sensors-tokyo.msft.png":::
    <span data-ttu-id="4ce47-267">Панель « **датчики** » с выбранным расположением.</span><span class="sxs-lookup"><span data-stu-id="4ce47-267">**Sensors** panel with a preset location selected.</span></span>  
:::image-end:::

## <span data-ttu-id="4ce47-268">Настройка ориентации</span><span class="sxs-lookup"><span data-stu-id="4ce47-268">Set orientation</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="4ce47-269">Если страница зависит от сведений о ориентации на мобильном устройстве для правильной обработки, откройте пользовательский интерфейс ориентации.</span><span class="sxs-lookup"><span data-stu-id="4ce47-269">If your page depends on orientation information from a mobile device to render properly, open the orientation UI.</span></span>  

      1.  <span data-ttu-id="4ce47-270">Нажмите кнопку **Настройка и** выберите пункт DevTools \ ( `...` \) > **другие инструменты**  >  **датчики**.</span><span class="sxs-lookup"><span data-stu-id="4ce47-270">Choose **Customize and control DevTools** \(`...`\) > **More tools** > **Sensors**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png" alt-text="Панель инструментов &quot;устройства&quot;" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png":::
         <span data-ttu-id="4ce47-272">**Датчики** для ориентации</span><span class="sxs-lookup"><span data-stu-id="4ce47-272">**Sensors** for orientation</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      1.  <span data-ttu-id="4ce47-273">Открытие меню команд.</span><span class="sxs-lookup"><span data-stu-id="4ce47-273">Open the Command Menu.</span></span>  
          *   <span data-ttu-id="4ce47-274">Выберите `Control` + `Shift` + `P` \ (Windows, Linux \) или `Command` + `Shift` + `P` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="4ce47-274">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\).</span></span>  
      1. <span data-ttu-id="4ce47-275">Введите текст `Sensors` и выберите пункт **Показать датчики**.</span><span class="sxs-lookup"><span data-stu-id="4ce47-275">Type `Sensors`, and choose **Show Sensors**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png" alt-text="Панель инструментов &quot;устройства&quot;" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png":::
         <span data-ttu-id="4ce47-277">**Отображение датчиков** для ориентации</span><span class="sxs-lookup"><span data-stu-id="4ce47-277">**Show Sensors** for orientation</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="4ce47-278">На панели **Sensors (датчики** ) можно выбрать стандартную ориентацию в раскрывающемся меню **ориентация** .</span><span class="sxs-lookup"><span data-stu-id="4ce47-278">On the **Sensors** panel, you may select a preset orientation from the **Orientation** drop-down menu.</span></span>  <span data-ttu-id="4ce47-279">Чтобы задать собственную ориентацию, выберите пункт **Настраиваемая ориентация**и введите значения [альфа][MDNDeviceOrientaitonAlpha], [бета][MDNDeviceOrientaitonBeta]и [гамма][MDNDeviceOrientaitonGamma] .</span><span class="sxs-lookup"><span data-stu-id="4ce47-279">To enter your own orientation, choose **Custom orientation**, and enter your own [alpha][MDNDeviceOrientaitonAlpha], [beta][MDNDeviceOrientaitonBeta], and [gamma][MDNDeviceOrientaitonGamma] values.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-sensors-tokyo-portrait-upside-down.msft.png" alt-text="Панель инструментов &quot;устройства&quot;" lightbox="../media/device-mode-toggle-device-toolbar-sensors-tokyo-portrait-upside-down.msft.png":::
    <span data-ttu-id="4ce47-281">Параметры **ориентации** на панели **датчиков**</span><span class="sxs-lookup"><span data-stu-id="4ce47-281">**Orientation** options on the **Sensors** panel</span></span>  
:::image-end:::  

## <span data-ttu-id="4ce47-282">Установка строки агента пользователя</span><span class="sxs-lookup"><span data-stu-id="4ce47-282">Set user agent string</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="4ce47-283">Если страница зависит от строки агента пользователя на мобильном устройстве для правильного отображения, используйте панель " **условия сети** " для предоставления разных строк пользовательского агента.</span><span class="sxs-lookup"><span data-stu-id="4ce47-283">If your page depends on the user agent string from a mobile device to render properly, use the **Network conditions** panel to provide different user agent strings.</span></span>  
      
      1.  <span data-ttu-id="4ce47-284">Нажмите кнопку **Настройка и** выберите пункт DevTools \ ( `...` \), > **Дополнительные инструменты**,  >  **сетевые условия**.</span><span class="sxs-lookup"><span data-stu-id="4ce47-284">Choose **Customize and control DevTools** \(`...`\) > **More tools** > **Network conditions**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-network-conditions.msft.png" alt-text="Панель инструментов &quot;устройства&quot;" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-network-conditions.msft.png":::
         <span data-ttu-id="4ce47-286">Элемент " **условия сети** " в меню " **другие инструменты** "</span><span class="sxs-lookup"><span data-stu-id="4ce47-286">**Network conditions** entry in the **More tools** menu</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      1.  <span data-ttu-id="4ce47-287">Открытие меню команд.</span><span class="sxs-lookup"><span data-stu-id="4ce47-287">Open the Command Menu.</span></span>  
          *   <span data-ttu-id="4ce47-288">Выберите `Control` + `Shift` + `P` \ (Windows, Linux \) или `Command` + `Shift` + `P` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="4ce47-288">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\).</span></span>  
      1. <span data-ttu-id="4ce47-289">Введите текст `Network conditions` и выберите пункт **Показать условия сети**.</span><span class="sxs-lookup"><span data-stu-id="4ce47-289">Type `Network conditions`, and choose **Show Network conditions**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-network-conditions.msft.png" alt-text="Панель инструментов &quot;устройства&quot;" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-network-conditions.msft.png":::
         **<span data-ttu-id="4ce47-291">Показывать условия сети</span><span class="sxs-lookup"><span data-stu-id="4ce47-291">Show Network conditions</span></span>**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="4ce47-292">Рядом с **агентом пользователя**снимите флажок **выбрать автоматически** .</span><span class="sxs-lookup"><span data-stu-id="4ce47-292">Next to **User agent**, clear the **Select automatically** checkbox.</span></span>  <span data-ttu-id="4ce47-293">Затем выберите **Custom...** , чтобы выбрать из списка предварительно заданных строк агента пользователя.</span><span class="sxs-lookup"><span data-stu-id="4ce47-293">Then, choose **Custom...** to select from a list of predefined user agent strings.</span></span>  <span data-ttu-id="4ce47-294">Чтобы ввести собственную строку агента пользователя, введите ее в поле **введите настраиваемый агент пользователя**.</span><span class="sxs-lookup"><span data-stu-id="4ce47-294">To enter your own user agent string, enter the string in **Enter a custom user agent**.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-network-conditions-macos.msft.png" alt-text="Панель инструментов &quot;устройства&quot;" lightbox="../media/device-mode-toggle-device-toolbar-network-conditions-macos.msft.png":::
    <span data-ttu-id="4ce47-296">Установка строки агента пользователя в Microsoft EDGE на macOS</span><span class="sxs-lookup"><span data-stu-id="4ce47-296">Set the user agent string to Microsoft Edge on macOS</span></span>  
:::image-end:::  

## <span data-ttu-id="4ce47-297">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="4ce47-297">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageCaptureIcon]: ../media/capture-settings-icon.msft.png  
[ImageDeviceToolbarIcon]: ../media/toggle-device-toolbar-dark-icon.msft.png  
[ImageRotateIcon]: ../media/rotate-dark-icon.msft.png  

<!-- links -->  

<!--[DevToolsCommunity]: ../index.md#community "Join the DevTools community | Microsoft Docs"  -->
[DevToolsRemoteDebugging]: .. /Remote-Debugging/index.md "Начало работы с удаленными отладочными устройствами Android | Microsoft Docs»  

[MDNWindowDevicePixelRatio]: https://developer.mozilla.org/docs/Web/API/Window/devicePixelRatio "Window. devicePixelRatio | MDN"  
[MDNUserAgent]: https://developer.mozilla.org/docs/Glossary/User_agent "Агент пользователя | MDN"  
[MDNDeviceOrientaitonAlpha]: https://developer.mozilla.org/en-US/docs/Web/API/DeviceOrientationEvent/alpha "DeviceOrientationEvent. Alpha | MDN"  
[MDNDeviceOrientaitonBeta]: https://developer.mozilla.org/en-US/docs/Web/API/DeviceOrientationEvent/beta "DeviceOrientationEvent. бета | MDN"  
[MDNDeviceOrientaitonGamma]: https://developer.mozilla.org/en-US/docs/Web/API/DeviceOrientationEvent/gamma "DeviceOrientationEvent. гамма | MDN"  

[WikiApproximation]: https://en.wikipedia.org/wiki/Order_of_approximation#First-order "Порядок приближения — первый-заказ — Википедии"  

> [!NOTE]
> <span data-ttu-id="4ce47-305">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="4ce47-305">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="4ce47-306">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/device-mode/index) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="4ce47-306">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/device-mode/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="4ce47-308">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="4ce47-308">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
