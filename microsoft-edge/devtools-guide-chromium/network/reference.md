---
description: Полный справочник по функциям панели DevTools сети Microsoft Edge.
title: Справочник по анализу сети
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 758623482ab2179987c6467f8e30c72d8893d710
ms.sourcegitcommit: addfd27bb765c92880a59f259dc702f6e4e1bf28
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/30/2020
ms.locfileid: "11092316"
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

# <span data-ttu-id="90a74-104">Справочник по анализу сети</span><span class="sxs-lookup"><span data-stu-id="90a74-104">Network Analysis reference</span></span>  

<span data-ttu-id="90a74-105">Ознакомьтесь с новыми способами для анализа того, как страница загружается в этой полной версии справочника по функциям сетевого анализа Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="90a74-105">Discover new ways to analyze how your page loads in this comprehensive reference of Microsoft Edge DevTools network analysis features.</span></span>  

<!--
> [!NOTE]
> This reference is based on Microsoft Edge 58.  If you use another version of Microsoft Edge, the UI, and features of DevTools may be different.  To verify which version of Microsoft Edge you are running, navigate to `edge://help`.  
-->

## <span data-ttu-id="90a74-106">Запись сетевых запросов</span><span class="sxs-lookup"><span data-stu-id="90a74-106">Record network requests</span></span>  

<span data-ttu-id="90a74-107">По умолчанию DevTools запись всех сетевых запросов на панели "сеть", пока открыта DevTools.</span><span class="sxs-lookup"><span data-stu-id="90a74-107">By default, DevTools record all network requests in the Network panel, so long as DevTools is open.</span></span>  

:::image type="complex" source="../media/network-network-panel.msft.png" alt-text="Панель &quot;сеть&quot;" lightbox="../media/network-network-panel.msft.png":::
   <span data-ttu-id="90a74-109">Панель " **сеть** "</span><span class="sxs-lookup"><span data-stu-id="90a74-109">The **Network** panel</span></span>  
:::image-end:::  

### <span data-ttu-id="90a74-110">Прекращение записи сетевых запросов</span><span class="sxs-lookup"><span data-stu-id="90a74-110">Stop recording network requests</span></span>  

<span data-ttu-id="90a74-111">Чтобы остановить запись запросов, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="90a74-111">To stop recording requests, complete the following steps.</span></span>  

1.  <span data-ttu-id="90a74-112">Выберите **остановить запись журнала сети** \ ( ![ остановить запись сетевого журнала ][ImageRecordOnIcon] \) на панели **сеть** .</span><span class="sxs-lookup"><span data-stu-id="90a74-112">Select **Stop recording network log** \(![Stop recording network log][ImageRecordOnIcon]\) on the **Network** panel.</span></span>  <span data-ttu-id="90a74-113">Оно превращается в серый, чтобы показать, что DevTools больше не записывает запросы.</span><span class="sxs-lookup"><span data-stu-id="90a74-113">It turns grey to indicate that DevTools is no longer recording requests.</span></span>  
1.  <span data-ttu-id="90a74-114">Нажимайте клавиши `Control` + `E` \ (Windows \) или `Command` + `E` \ (macOS \), пока фокус находится на панели " **сеть** ".</span><span class="sxs-lookup"><span data-stu-id="90a74-114">Press `Control`+`E` \(Windows\) or `Command`+`E` \(macOS\) while the **Network** panel is in focus.</span></span>  

### <span data-ttu-id="90a74-115">Очистка запросов</span><span class="sxs-lookup"><span data-stu-id="90a74-115">Clear requests</span></span>  

<span data-ttu-id="90a74-116">На панели Network (сеть) выберите **clear** \ ( ![ очистить ][ImageClearIcon] \), чтобы удалить все запросы из таблицы запросы.</span><span class="sxs-lookup"><span data-stu-id="90a74-116">Select **Clear** \(![Clear][ImageClearIcon]\) on the Network panel to clear all requests from the Requests table.</span></span>  

:::image type="complex" source="../media/network-network-clear-button.msft.png" alt-text="Панель &quot;сеть&quot;" lightbox="../media/network-network-clear-button.msft.png":::
   <span data-ttu-id="90a74-118">Кнопка " **очистить** "</span><span class="sxs-lookup"><span data-stu-id="90a74-118">The **Clear** button</span></span>  
:::image-end:::  

### <span data-ttu-id="90a74-119">Сохранение запросов на загрузку страниц</span><span class="sxs-lookup"><span data-stu-id="90a74-119">Save requests across page loads</span></span>  

<span data-ttu-id="90a74-120">Для сохранения запросов на страницах загрузок на панели "сеть" установите флажок **сохранить журнал** .</span><span class="sxs-lookup"><span data-stu-id="90a74-120">To save requests across page loads, check the **Preserve log** checkbox on the Network panel.</span></span>  <span data-ttu-id="90a74-121">DevTools сохраняет все запросы, пока не отключайте параметр **сохранить журнал**.</span><span class="sxs-lookup"><span data-stu-id="90a74-121">DevTools saves all requests until you disable **Preserve log**.</span></span>  

:::image type="complex" source="../media/network-network-preserve-log.msft.png" alt-text="Панель &quot;сеть&quot;" lightbox="../media/network-network-preserve-log.msft.png":::
   <span data-ttu-id="90a74-123">Флажок " **сохранить журнал** "</span><span class="sxs-lookup"><span data-stu-id="90a74-123">The **Preserve Log** checkbox</span></span>  
:::image-end:::  

### <span data-ttu-id="90a74-124">Захват снимков экрана при загрузке страницы</span><span class="sxs-lookup"><span data-stu-id="90a74-124">Capture screenshots during page load</span></span>  

<span data-ttu-id="90a74-125">Выведите снимки экрана, чтобы проанализировать, какие дисплеи отображаются для пользователей во время ожидания загрузки страницы.</span><span class="sxs-lookup"><span data-stu-id="90a74-125">Capture screenshots to analyze what displays for users while waiting for your page to load.</span></span>  

<span data-ttu-id="90a74-126">Чтобы включить снимки экрана, нажмите кнопку **Параметры сети** и выберите команду **захватить снимки экрана** на панели " **сеть** ".</span><span class="sxs-lookup"><span data-stu-id="90a74-126">To enable screenshots, select **Network settings** and select **Capture screenshots** checkbox on the **Network** panel.</span></span>  

<span data-ttu-id="90a74-127">Обновите страницу, когда фокус находится на панели " **сеть** ", чтобы захватить снимки экрана.</span><span class="sxs-lookup"><span data-stu-id="90a74-127">Refresh the page while the **Network** panel is in focus to capture screenshots.</span></span>  

<span data-ttu-id="90a74-128">После захвата снимка экрана вы взаимодействуете с ним следующими способами.</span><span class="sxs-lookup"><span data-stu-id="90a74-128">After capturing a screenshot, you interact with it in the following ways.</span></span>  

*   <span data-ttu-id="90a74-129">Наведите указатель мыши на снимок экрана, чтобы просмотреть точку, в которой был записан снимок экрана.</span><span class="sxs-lookup"><span data-stu-id="90a74-129">Hover over a screenshot to view the point at which that screenshot was captured.</span></span>  <span data-ttu-id="90a74-130">На панели **обзора** появится желтая линия.</span><span class="sxs-lookup"><span data-stu-id="90a74-130">A yellow line is displayed on the **Overview** pane.</span></span>  
*   <span data-ttu-id="90a74-131">Щелкните эскиз экрана, чтобы отфильтровать все запросы, произошедшие после захвата снимка экрана.</span><span class="sxs-lookup"><span data-stu-id="90a74-131">Select the thumbnail of a screen to filter out any requests that occurred after the screenshot was captured.</span></span>  
*   <span data-ttu-id="90a74-132">Дважды щелкните эскиз, чтобы увеличить его.</span><span class="sxs-lookup"><span data-stu-id="90a74-132">Double-click a thumbnail to zoom into it.</span></span>  

:::image type="complex" source="../media/network-network-screenshot-hover.msft.png" alt-text="Панель &quot;сеть&quot;" lightbox="../media/network-network-screenshot-hover.msft.png":::
   <span data-ttu-id="90a74-134">Наведение указателя на снимок экрана</span><span class="sxs-lookup"><span data-stu-id="90a74-134">Hovering over a screenshot</span></span>  
:::image-end:::  

<!--  ### Replay XHR request  -->

<!--  To replay an XHR request, hover on the request in the Requests table, open the contextual menu \(right-click\), and select **Replay XHR**.  -->

<!--  
:::image type="complex" source="../media/network-replay-xhr.msft.png" alt-text="Панель &quot;сеть&quot;" lightbox="../media/network-replay-xhr.msft.png":::
   Selecting Replay XHR  
:::image-end:::  
-->  

## <span data-ttu-id="90a74-135">Изменение поведения при загрузке</span><span class="sxs-lookup"><span data-stu-id="90a74-135">Change loading behavior</span></span>  

### <span data-ttu-id="90a74-136">Эмуляция первого времени посетителя с помощью отключения кэша браузера</span><span class="sxs-lookup"><span data-stu-id="90a74-136">Emulate a first-time visitor by disabling the browser cache</span></span>  

<span data-ttu-id="90a74-137">Чтобы эмулировать, как пользователь попытается получить доступ к сайту, установите флажок **отключить кэш** .</span><span class="sxs-lookup"><span data-stu-id="90a74-137">To emulate how a first-time user experiences your site, check the **Disable cache** checkbox.</span></span>  <span data-ttu-id="90a74-138">DevTools отключает кэш браузера.</span><span class="sxs-lookup"><span data-stu-id="90a74-138">DevTools disables the browser cache.</span></span>  <span data-ttu-id="90a74-139">Эта функция более точно эмулирует взаимодействие с пользователем при первом запуске, так как запросы размещаются из кэша браузера на повторных посещениях.</span><span class="sxs-lookup"><span data-stu-id="90a74-139">This feature more accurately emulates a first-time user's experience, because requests are served from the browser cache on repeat visits.</span></span>  

:::image type="complex" source="../media/network-network-disable-cache-checkbox.msft.png" alt-text="Панель &quot;сеть&quot;" lightbox="../media/network-network-disable-cache-checkbox.msft.png":::
   <span data-ttu-id="90a74-141">Флажок " **отключить кэш** "</span><span class="sxs-lookup"><span data-stu-id="90a74-141">The **Disable Cache** checkbox</span></span>  
:::image-end:::  

#### <span data-ttu-id="90a74-142">Отключение кэша браузера из денежных ящиков условий сети</span><span class="sxs-lookup"><span data-stu-id="90a74-142">Disable the browser cache from the Network Conditions drawer</span></span>  

<span data-ttu-id="90a74-143">Если вы хотите отключить кэш при работе с другими панелями DevTools, используйте денежные ящики условия сети.</span><span class="sxs-lookup"><span data-stu-id="90a74-143">If you want to disable the cache while working in other DevTools panels, use the Network Conditions drawer.</span></span>  

1.  <span data-ttu-id="90a74-144">Откройте денежный ящик **условий сети** .</span><span class="sxs-lookup"><span data-stu-id="90a74-144">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="90a74-145">Установите или снимите флажок **отключить кэш** .</span><span class="sxs-lookup"><span data-stu-id="90a74-145">Check or uncheck the **Disable cache** checkbox.</span></span>  

<!--todo: add network condition section when available -->  

### <span data-ttu-id="90a74-146">Очистка кэша браузера вручную</span><span class="sxs-lookup"><span data-stu-id="90a74-146">Manually clear the browser cache</span></span>  

<span data-ttu-id="90a74-147">Чтобы вручную очистить кэш браузера в любое время, откройте контекстное меню (щелкните правой кнопкой мыши в любом месте таблицы запросов и выберите пункт **очистить кэш браузера**).</span><span class="sxs-lookup"><span data-stu-id="90a74-147">To manually clear the browser cache at any time, open the contextual menu \(right-click\) anywhere in the Requests table and select **Clear Browser Cache**.</span></span>  

:::image type="complex" source="../media/network-network-clear-browser-cache.msft.png" alt-text="Панель &quot;сеть&quot;" lightbox="../media/network-network-clear-browser-cache.msft.png":::
   <span data-ttu-id="90a74-149">Выбор **очистки кэша браузера**</span><span class="sxs-lookup"><span data-stu-id="90a74-149">Selecting **Clear Browser Cache**</span></span>  
:::image-end:::  

### <span data-ttu-id="90a74-150">Эмуляция в автономном режиме</span><span class="sxs-lookup"><span data-stu-id="90a74-150">Emulate offline</span></span>  

<span data-ttu-id="90a74-151">Новый класс веб-приложений, именуемых [прогрессивными веб-приложениями][DevtoolsProgressiveWebApps], не будет работать в автономном режиме с помощью **обслуживания сотрудников**.</span><span class="sxs-lookup"><span data-stu-id="90a74-151">A new class of web apps, named [Progressive Web Apps][DevtoolsProgressiveWebApps], functions offline with the help of **service workers**.</span></span>  <span data-ttu-id="90a74-152">Возможно, вам будет удобно быстро смоделировать устройство, которое не имеет подключения к данным, при построении такого типа приложения.</span><span class="sxs-lookup"><span data-stu-id="90a74-152">You may find it useful to quickly simulate a device that has no data connection when you are building this type of app.</span></span>  

<!--[ServiceWorkers]: /web/fundamentals/getting-started/primers/service-workers  -->

<span data-ttu-id="90a74-153">Щелкните раскрывающееся меню **онлайн** , выполните поиск в разделе **пресеты**и выберите пункт в **автономном режиме** , чтобы имитировать автономный режим работы сети.</span><span class="sxs-lookup"><span data-stu-id="90a74-153">Select the **Online** dropdown menu, search under **Presets**, and select **Offline** to simulate an offline network experience.</span></span>  

:::image type="complex" source="../media/network-network-offline-dropdown.msft.png" alt-text="Панель &quot;сеть&quot;" lightbox="../media/network-network-offline-dropdown.msft.png":::
   <span data-ttu-id="90a74-155">Раскрывающееся меню " **автономный режим** "</span><span class="sxs-lookup"><span data-stu-id="90a74-155">The **Offline** dropdown menu</span></span>  
:::image-end:::  

### <span data-ttu-id="90a74-156">Эмуляция медленных сетевых подключений</span><span class="sxs-lookup"><span data-stu-id="90a74-156">Emulate slow network connections</span></span>  

<span data-ttu-id="90a74-157">Эмуляция медленной сети 3G, Fast 3G и других скоростей соединения из раскрывающегося меню **Online** .</span><span class="sxs-lookup"><span data-stu-id="90a74-157">Emulate Slow 3G, Fast 3G, and other connection speeds from the **Online** dropdown menu.</span></span>  

:::image type="complex" source="../media/network-network-throttling-menu.msft.png" alt-text="Панель &quot;сеть&quot;" lightbox="../media/network-network-throttling-menu.msft.png":::
   <span data-ttu-id="90a74-159">Раскрывающееся меню **регулирования**</span><span class="sxs-lookup"><span data-stu-id="90a74-159">The **Throttling** dropdown menu</span></span>  
:::image-end:::  

<span data-ttu-id="90a74-160">Вы можете выбрать один из различных наборов параметров, например "медленный" или "Быстрая 3G".</span><span class="sxs-lookup"><span data-stu-id="90a74-160">You may select from different presets, such as Slow 3G or Fast 3G.</span></span>  <span data-ttu-id="90a74-161">Вы также можете добавить собственные пользовательские стили, открыв меню регулирования и выбрав пункт **настраиваемое**  >  **Добавление**.</span><span class="sxs-lookup"><span data-stu-id="90a74-161">You may also add your own custom presets by opening the Throttling menu and selecting **Custom** > **Add**.</span></span>  

<span data-ttu-id="90a74-162">DevTools отображает значок предупреждения рядом с вкладкой **сеть** , чтобы напомнить вам, что регулирование разрешено.</span><span class="sxs-lookup"><span data-stu-id="90a74-162">DevTools displays a warning icon next to the **Network** tab to remind you that throttling is enabled.</span></span>  

#### <span data-ttu-id="90a74-163">Эмуляция медленных сетевых подключений из денежных ящиков условий сети</span><span class="sxs-lookup"><span data-stu-id="90a74-163">Emulate slow network connections from the Network Conditions drawer</span></span>  

<span data-ttu-id="90a74-164">Если вы хотите регулировать сетевое соединение при работе с другими панелями DevTools, используйте денежные ящики условий сети.</span><span class="sxs-lookup"><span data-stu-id="90a74-164">If you want to throttle the network connection while working in other DevTools panels, use the Network Conditions drawer.</span></span>  

1.  <span data-ttu-id="90a74-165">Откройте денежный ящик **условий сети** .</span><span class="sxs-lookup"><span data-stu-id="90a74-165">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="90a74-166">Выберите скорость соединения в меню **регулирования** .</span><span class="sxs-lookup"><span data-stu-id="90a74-166">Select your connection speed from the **Throttling** menu.</span></span>  

<!--todo: add network condition section when available -->  

### <span data-ttu-id="90a74-167">Очистка файлов cookie браузера вручную</span><span class="sxs-lookup"><span data-stu-id="90a74-167">Manually clear browser cookies</span></span>  

<span data-ttu-id="90a74-168">Чтобы вручную удалить cookie-файлы браузера в любое время, откройте контекстное меню (щелкните правой кнопкой мыши, где угодно в таблице запросов и выберите команду **Очистить cookie-файлы браузера**).</span><span class="sxs-lookup"><span data-stu-id="90a74-168">To manually clear browser cookies at any time, open the contextual menu \(right-click\) anywhere in the Requests table and select **Clear Browser Cookies**.</span></span>  

:::image type="complex" source="../media/network-network-clear-browser-cookies.msft.png" alt-text="Панель &quot;сеть&quot;" lightbox="../media/network-network-clear-browser-cookies.msft.png":::
   <span data-ttu-id="90a74-170">Выбор **очистки cookie-файлов браузера**</span><span class="sxs-lookup"><span data-stu-id="90a74-170">Selecting **Clear Browser Cookies**</span></span>  
:::image-end:::  

### <span data-ttu-id="90a74-171">Переопределение агента пользователя</span><span class="sxs-lookup"><span data-stu-id="90a74-171">Override the user agent</span></span>  

<span data-ttu-id="90a74-172">Чтобы вручную переопределить агент пользователя, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="90a74-172">To manually override the user agent, use the following steps.</span></span>  

1.  <span data-ttu-id="90a74-173">Откройте денежный ящик **условий сети** .</span><span class="sxs-lookup"><span data-stu-id="90a74-173">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="90a74-174">Снимите флажок **автоматически**.</span><span class="sxs-lookup"><span data-stu-id="90a74-174">Uncheck **Select automatically**.</span></span>  
1.  <span data-ttu-id="90a74-175">Выберите в меню пункт агента пользователя или введите его в текстовом поле.</span><span class="sxs-lookup"><span data-stu-id="90a74-175">Choose a user agent option from the menu, or enter a custom one in the text box.</span></span>  

<!--todo: add network condition section when available -->  

## <span data-ttu-id="90a74-176">Фильтрация запросов</span><span class="sxs-lookup"><span data-stu-id="90a74-176">Filter requests</span></span>  

### <span data-ttu-id="90a74-177">Фильтрация запросов по свойствам</span><span class="sxs-lookup"><span data-stu-id="90a74-177">Filter requests by properties</span></span>  

<span data-ttu-id="90a74-178">С помощью текстового поля **Фильтр** можно отфильтровать запросы по свойствам, таким как домен или размер запроса.</span><span class="sxs-lookup"><span data-stu-id="90a74-178">Use the **Filter** text box to filter requests by properties, such as the domain or size of the request.</span></span>  

<span data-ttu-id="90a74-179">Если текстовое поле не отображается, возможно, область **фильтры** скрыта.</span><span class="sxs-lookup"><span data-stu-id="90a74-179">If the text box is not displayed, the **Filters** pane is probably hidden.</span></span>  
<span data-ttu-id="90a74-180">Чтобы получить дополнительные сведения, перейдите в раздел [скрыть область фильтров](#hide-the-filters-pane).</span><span class="sxs-lookup"><span data-stu-id="90a74-180">For more information, navigate to [Hide the Filters pane](#hide-the-filters-pane).</span></span>  

:::image type="complex" source="../media/network-network-filters-textbox.msft.png" alt-text="Панель &quot;сеть&quot;" lightbox="../media/network-network-filters-textbox.msft.png":::
   <span data-ttu-id="90a74-182">Текстовое поле " **Фильтр** "</span><span class="sxs-lookup"><span data-stu-id="90a74-182">The **Filter** text box</span></span>  
:::image-end:::  

<span data-ttu-id="90a74-183">Вы можете использовать несколько свойств одновременно, разделяя каждое свойство пробелами.</span><span class="sxs-lookup"><span data-stu-id="90a74-183">You may use multiple properties simultaneously by separating each property with a space.</span></span>  <span data-ttu-id="90a74-184">Например, `mime-type:image/png larger-than:1K` отображает все PNGs, размер которых больше 1 Кбайт.</span><span class="sxs-lookup"><span data-stu-id="90a74-184">For example, `mime-type:image/png larger-than:1K` displays all PNGs that are larger than 1 kilobyte.</span></span>  <span data-ttu-id="90a74-185">Фильтры с несколькими свойствами эквивалентны `AND` операциям.</span><span class="sxs-lookup"><span data-stu-id="90a74-185">The multi-property filters are equivalent to `AND` operations.</span></span>  `OR` <span data-ttu-id="90a74-186">операции в настоящее время не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="90a74-186">operations are currently not supported.</span></span>  

<span data-ttu-id="90a74-187">Полный список поддерживаемых свойств.</span><span class="sxs-lookup"><span data-stu-id="90a74-187">The complete list of supported properties.</span></span>  

| <span data-ttu-id="90a74-188">Свойство</span><span class="sxs-lookup"><span data-stu-id="90a74-188">Property</span></span> | <span data-ttu-id="90a74-189">Сведения</span><span class="sxs-lookup"><span data-stu-id="90a74-189">Details</span></span> |  
|:--- | :--- |  
| `domain` | <span data-ttu-id="90a74-190">Отображать только ресурсы из указанного домена.</span><span class="sxs-lookup"><span data-stu-id="90a74-190">Only display resources from the specified domain.</span></span>  <span data-ttu-id="90a74-191">Вы можете использовать подстановочный знак "\ `*` ", чтобы включить несколько доменов.</span><span class="sxs-lookup"><span data-stu-id="90a74-191">You may use a wildcard character \(`*`\) to include multiple domains.</span></span>  <span data-ttu-id="90a74-192">Например, `*.com` отображаются ресурсы из всех доменных имен, которые заканчиваются на `.com` .</span><span class="sxs-lookup"><span data-stu-id="90a74-192">For example, `*.com` displays resources from all domain names ending in `.com`.</span></span>  <span data-ttu-id="90a74-193">DevTools Заполнение раскрывающегося меню "Автозаполнение" всеми найденными доменами.</span><span class="sxs-lookup"><span data-stu-id="90a74-193">DevTools populate the autocomplete dropdown menu with all of the domains that are found.</span></span> |  
| `has-response-header` | <span data-ttu-id="90a74-194">Выводит ресурсы, содержащие указанный заголовок HTTP-ответа.</span><span class="sxs-lookup"><span data-stu-id="90a74-194">Displays the resources that contain the specified HTTP response header.</span></span>  <span data-ttu-id="90a74-195">DevTools заполнить раскрывающийся список автозавершения всеми найденными заголовками ответов.</span><span class="sxs-lookup"><span data-stu-id="90a74-195">DevTools populate the autocomplete dropdown with all of the response headers that are found.</span></span> |  
| `is` | <span data-ttu-id="90a74-196">Используется `is:running` для поиска `WebSocket` ресурсов.</span><span class="sxs-lookup"><span data-stu-id="90a74-196">Use `is:running` to find `WebSocket` resources.</span></span> |  
| `larger-than` | <span data-ttu-id="90a74-197">Отображаются ресурсы, размер которых превышает указанный в байтах.</span><span class="sxs-lookup"><span data-stu-id="90a74-197">Displays resources that are larger than the specified size, in bytes.</span></span>  <span data-ttu-id="90a74-198">Установка значения эквивалентно значению свойства `1000` `1k` .</span><span class="sxs-lookup"><span data-stu-id="90a74-198">Setting a value of `1000` is equivalent to setting a value of `1k`.</span></span> |  
| `method` | <span data-ttu-id="90a74-199">Отображает ресурсы, полученные с помощью указанного типа метода HTTP.</span><span class="sxs-lookup"><span data-stu-id="90a74-199">Displays resources that were retrieved over a specified HTTP method type.</span></span>  <span data-ttu-id="90a74-200">DevTools заполнить раскрывающийся список всеми найденными методами HTTP.</span><span class="sxs-lookup"><span data-stu-id="90a74-200">DevTools populate the dropdown with all of the HTTP methods  that are found.</span></span> |  
| `mime-type` | <span data-ttu-id="90a74-201">Выводит ресурсы указанного типа MIME.</span><span class="sxs-lookup"><span data-stu-id="90a74-201">Displays resources of a specified MIME type.</span></span>  <span data-ttu-id="90a74-202">DevTools заполнить раскрывающийся список всеми найденными типами MIME.</span><span class="sxs-lookup"><span data-stu-id="90a74-202">DevTools populate the dropdown with all MIME types  that are found.</span></span> |  
| `mixed-content` | <span data-ttu-id="90a74-203">Показать все смешанные ресурсы контента \ ( `mixed-content:all` \) или только те из них, которые в данный момент отображаются \ ( `mixed-content:displayed` \).</span><span class="sxs-lookup"><span data-stu-id="90a74-203">Show all mixed content resources \(`mixed-content:all`\) or just the ones that are currently displayed \(`mixed-content:displayed`\).</span></span> |  
| `scheme` | <span data-ttu-id="90a74-204">Отображаются ресурсы, полученные по незащищенным HTTP-( `scheme:http` \) или защищенным HTTPS-( `scheme:https` \).</span><span class="sxs-lookup"><span data-stu-id="90a74-204">Displays resources retrieved over unprotected HTTP \(`scheme:http`\) or protected HTTPS \(`scheme:https`\).</span></span> |  
| `set-cookie-domain` | <span data-ttu-id="90a74-205">Отображает ресурсы с `Set-Cookie` заголовком с `Domain` атрибутом, соответствующим указанному значению.</span><span class="sxs-lookup"><span data-stu-id="90a74-205">Displays resources that have a `Set-Cookie` header with a `Domain` attribute that matches the specified value.</span></span>  <span data-ttu-id="90a74-206">DevTools заполнить Автозаполнение всеми найденными доменами cookie-файлов.</span><span class="sxs-lookup"><span data-stu-id="90a74-206">DevTools populate the autocomplete with all of the cookie domains that are found.</span></span> |  
| `set-cookie-name` | <span data-ttu-id="90a74-207">Отображаются ресурсы, у которых есть `Set-Cookie` заголовок с именем, соответствующим указанному значению.</span><span class="sxs-lookup"><span data-stu-id="90a74-207">Displays resources that have a `Set-Cookie` header with a name that matches the specified value.</span></span>  <span data-ttu-id="90a74-208">DevTools заполните Автозаполнение всеми найденными именами cookie-файлов.</span><span class="sxs-lookup"><span data-stu-id="90a74-208">DevTools populate the autocomplete with all of the cookie names that are found.</span></span> |  
| `set-cookie-value` | <span data-ttu-id="90a74-209">Отображает ресурсы с `Set-Cookie` заголовком со значением, которое соответствует указанному значению.</span><span class="sxs-lookup"><span data-stu-id="90a74-209">Displays resources that have a `Set-Cookie` header with a value that matches the specified value.</span></span>  <span data-ttu-id="90a74-210">DevTools заполнить Автозаполнение всеми найденными значениями cookie-файлов.</span><span class="sxs-lookup"><span data-stu-id="90a74-210">DevTools populate the autocomplete with all of the cookie values that are found.</span></span> |  
| `status-code` | <span data-ttu-id="90a74-211">Отображает ресурсы, соответствующие указанному коду состояния HTTP.</span><span class="sxs-lookup"><span data-stu-id="90a74-211">Displays resources that match the specific HTTP status code.</span></span>  <span data-ttu-id="90a74-212">DevTools заполняет раскрывающееся меню автозаполнения всеми найденными кодами состояния.</span><span class="sxs-lookup"><span data-stu-id="90a74-212">DevTools populates the autocomplete dropdown menu with all of the status codes that are found.</span></span> |  

### <span data-ttu-id="90a74-213">Фильтрация запросов по типу</span><span class="sxs-lookup"><span data-stu-id="90a74-213">Filter requests by type</span></span>  

<span data-ttu-id="90a74-214">Чтобы отфильтровать запросы по типу запроса, выберите один из указанных ниже кнопок на панели **сеть** .</span><span class="sxs-lookup"><span data-stu-id="90a74-214">To filter requests by request type, select the one of the following buttons on the **Network** panel.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="90a74-215">XHR</span><span class="sxs-lookup"><span data-stu-id="90a74-215">XHR</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="90a74-216">JS</span><span class="sxs-lookup"><span data-stu-id="90a74-216">JS</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="90a74-217">CSS</span><span class="sxs-lookup"><span data-stu-id="90a74-217">CSS</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="90a74-218">IMG</span><span class="sxs-lookup"><span data-stu-id="90a74-218">Img</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="90a74-219">Мультимедиа</span><span class="sxs-lookup"><span data-stu-id="90a74-219">Media</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="90a74-220">Шрифт</span><span class="sxs-lookup"><span data-stu-id="90a74-220">Font</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="90a74-221">Тов</span><span class="sxs-lookup"><span data-stu-id="90a74-221">Doc</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="90a74-222">WS</span><span class="sxs-lookup"><span data-stu-id="90a74-222">WS</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="90a74-223">WebSocket.</span><span class="sxs-lookup"><span data-stu-id="90a74-223">WebSocket.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="90a74-224">Является</span><span class="sxs-lookup"><span data-stu-id="90a74-224">Manifest</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="90a74-225">Other</span><span class="sxs-lookup"><span data-stu-id="90a74-225">Other</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="90a74-226">Любые другие типы не указаны в списке.</span><span class="sxs-lookup"><span data-stu-id="90a74-226">Any other type not listed.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="90a74-227">Если кнопки не отображаются, область **фильтров** может быть скрыта.</span><span class="sxs-lookup"><span data-stu-id="90a74-227">If the buttons do not display, the **Filters** pane may be hidden.</span></span>  
<span data-ttu-id="90a74-228">Чтобы получить дополнительные сведения, перейдите в раздел [скрыть область фильтров](#hide-the-filters-pane).</span><span class="sxs-lookup"><span data-stu-id="90a74-228">For more information, navigate to [Hide the Filters pane](#hide-the-filters-pane).</span></span>  

<span data-ttu-id="90a74-229">Чтобы включить множественные фильтры типов одновременно, удерживайте клавишу `Control` \ (Windows \) или `Command` \ (macOS \) и выберите.</span><span class="sxs-lookup"><span data-stu-id="90a74-229">To enable multiple type filters simultaneously, hold `Control` \(Windows\) or `Command` \(macOS\) and then select.</span></span>  

:::image type="complex" source="../media/network-network-type-filters.msft.png" alt-text="Панель &quot;сеть&quot;" lightbox="../media/network-network-type-filters.msft.png":::
   <span data-ttu-id="90a74-231">Использование фильтров типов для отображения ресурсов JS, CSS и документов</span><span class="sxs-lookup"><span data-stu-id="90a74-231">Using the Type filters to display JS, CSS, and Document resources</span></span>  
:::image-end:::  

### <span data-ttu-id="90a74-232">Фильтрация запросов по времени</span><span class="sxs-lookup"><span data-stu-id="90a74-232">Filter requests by time</span></span>  

<span data-ttu-id="90a74-233">Чтобы отобразить только те запросы, которые были активны в течение этого времени, выберите и перетащите его влево или вправо в области "Обзор".</span><span class="sxs-lookup"><span data-stu-id="90a74-233">Select and drag left or right on the Overview pane to only display requests that were active during that time frame.</span></span>  <span data-ttu-id="90a74-234">Фильтр является инклюзивным.</span><span class="sxs-lookup"><span data-stu-id="90a74-234">The filter is inclusive.</span></span>  <span data-ttu-id="90a74-235">Отображается любой запрос, который был активен в течение выбранного периода времени.</span><span class="sxs-lookup"><span data-stu-id="90a74-235">Any request that was active during the highlighted time is shown.</span></span>  

:::image type="complex" source="../media/network-network-overview-filter.msft.png" alt-text="Панель &quot;сеть&quot;" lightbox="../media/network-network-overview-filter.msft.png":::
   <span data-ttu-id="90a74-237">Фильтрация запросов, которые были неактивны около 300 MS</span><span class="sxs-lookup"><span data-stu-id="90a74-237">Filtering out any requests that were inactive around 300 ms</span></span>  
:::image-end:::  

### <span data-ttu-id="90a74-238">Скрыть URL-адреса данных</span><span class="sxs-lookup"><span data-stu-id="90a74-238">Hide data URLs</span></span>  

<span data-ttu-id="90a74-239">[URL-адреса данных][MDNHTTPDataURIs] — это небольшие файлы, внедренные в другие документы.</span><span class="sxs-lookup"><span data-stu-id="90a74-239">[Data URLs][MDNHTTPDataURIs] are small files embedded into other documents.</span></span>  <span data-ttu-id="90a74-240">Любые запросы, которые отображаются в таблице запросов, которая начинается с `data:` URL-адреса данных.</span><span class="sxs-lookup"><span data-stu-id="90a74-240">Any request that displays in the Requests table that starts with `data:` is a data URL.</span></span>  

<span data-ttu-id="90a74-241">Установите флажок **скрыть URL-адреса данных** , чтобы скрыть запросы.</span><span class="sxs-lookup"><span data-stu-id="90a74-241">Check the **Hide data URLs** checkbox to hide the requests.</span></span>  

:::image type="complex" source="../media/network-network-hide-data-urls.msft.png" alt-text="Панель &quot;сеть&quot;" lightbox="../media/network-network-hide-data-urls.msft.png":::
   <span data-ttu-id="90a74-243">Флажок " **скрыть URL-адреса данных** "</span><span class="sxs-lookup"><span data-stu-id="90a74-243">The **Hide Data URLs** checkbox</span></span>  
:::image-end:::  

## <span data-ttu-id="90a74-244">Запросы сортировки</span><span class="sxs-lookup"><span data-stu-id="90a74-244">Sort requests</span></span>  

<span data-ttu-id="90a74-245">По умолчанию запросы в таблице запросов сортируются по времени запуска, но вы можете отсортировать таблицу с помощью других условий.</span><span class="sxs-lookup"><span data-stu-id="90a74-245">By default, the requests in the Requests table are sorted by initiation time, but you may sort the table using other criteria.</span></span>  

### <span data-ttu-id="90a74-246">Сортировка по столбцам</span><span class="sxs-lookup"><span data-stu-id="90a74-246">Sort by column</span></span>  

<span data-ttu-id="90a74-247">Выберите верхний колонтитул любого столбца в списке запросы для сортировки запросов по этому столбцу.</span><span class="sxs-lookup"><span data-stu-id="90a74-247">Select the header of any column in the Requests to sort requests by that column.</span></span>  

### <span data-ttu-id="90a74-248">Этап сортировки по действию</span><span class="sxs-lookup"><span data-stu-id="90a74-248">Sort by activity phase</span></span>  

<span data-ttu-id="90a74-249">Чтобы изменить способ сортировки запросов, наведите указатель мыши на заголовок таблицы запросы, откройте контекстное меню, наведите указатель мыши на пункт **Каскад**и выберите один из следующих вариантов.</span><span class="sxs-lookup"><span data-stu-id="90a74-249">To change how the Waterfall sorts requests, hover on the header of the Requests table, open the contextual menu \(right-click\), hover over **Waterfall**, and select one of the following options.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="90a74-250">Время начала</span><span class="sxs-lookup"><span data-stu-id="90a74-250">Start Time</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="90a74-251">Первый инициированный запрос находится наверху.</span><span class="sxs-lookup"><span data-stu-id="90a74-251">The first request that was initiated is at the top.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="90a74-252">Время ответа</span><span class="sxs-lookup"><span data-stu-id="90a74-252">Response Time</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="90a74-253">Первый запрос, загруженный в верхней части экрана.</span><span class="sxs-lookup"><span data-stu-id="90a74-253">The first request that started downloading is at the top.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="90a74-254">Время окончания</span><span class="sxs-lookup"><span data-stu-id="90a74-254">End Time</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="90a74-255">Первый завершенный запрос вверху.</span><span class="sxs-lookup"><span data-stu-id="90a74-255">The first request that finished is at the top.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="90a74-256">Общая длительность</span><span class="sxs-lookup"><span data-stu-id="90a74-256">Total Duration</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="90a74-257">В верхней части запроса с минимальными параметрами подключения и запроса или ответа.</span><span class="sxs-lookup"><span data-stu-id="90a74-257">The request with the shortest connection settings and request or response is at the top.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="90a74-258">Задержка</span><span class="sxs-lookup"><span data-stu-id="90a74-258">Latency</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="90a74-259">Запрос, который ожидает наиболее короткий момент ответа, находится наверху.</span><span class="sxs-lookup"><span data-stu-id="90a74-259">The request that waited the shortest time for a response is at the top.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="90a74-260">В этих описаниях предполагается, что каждый из вариантов имеет приоритет от кратчайшего к наиболее продолжительному.</span><span class="sxs-lookup"><span data-stu-id="90a74-260">These descriptions assume that each respective option is ranked from shortest to longest.</span></span>  <span data-ttu-id="90a74-261">Если выбрать верхний колонтитул столбца **каскадом** , порядок будет изменен на противоположный.</span><span class="sxs-lookup"><span data-stu-id="90a74-261">Selecting the header of the **Waterfall** column reverses the order.</span></span>  

:::image type="complex" source="../media/network-network-waterfall-total-duration.msft.png" alt-text="Панель &quot;сеть&quot;" lightbox="../media/network-network-waterfall-total-duration.msft.png":::
   <span data-ttu-id="90a74-263">Сортировка каскадом по общей длительности \ (светлая часть каждого элемента диаграммы затратила время ожидания, а темная часть — это время, затраченное на загрузку байтов)</span><span class="sxs-lookup"><span data-stu-id="90a74-263">Sorting the Waterfall by total duration  \(The lighter portion of each bar is time spent waiting and the darker portion is time spent downloading bytes\)</span></span>  
:::image-end:::  

## <span data-ttu-id="90a74-264">Анализ запросов</span><span class="sxs-lookup"><span data-stu-id="90a74-264">Analyze requests</span></span>  

<span data-ttu-id="90a74-265">Пока DevTools открыты, все запросы на панели "сеть" записываются в журнал.</span><span class="sxs-lookup"><span data-stu-id="90a74-265">So long as DevTools are open, it logs all requests in the Network panel.</span></span>  
<span data-ttu-id="90a74-266">Проанализируйте запросы с помощью панели "сеть".</span><span class="sxs-lookup"><span data-stu-id="90a74-266">Use the Network panel to analyze requests.</span></span>  

### <span data-ttu-id="90a74-267">Просмотр журнала запросов</span><span class="sxs-lookup"><span data-stu-id="90a74-267">View a log of requests</span></span>  

<span data-ttu-id="90a74-268">С помощью таблицы "запросы" можно просмотреть журнал всех запросов, выполненных, когда DevTools открыты.</span><span class="sxs-lookup"><span data-stu-id="90a74-268">Use the Requests table to view a log of all requests made while DevTools have been open.</span></span>  <span data-ttu-id="90a74-269">При выборе или наведении указателя мыши на запросы открывается больше сведений о каждом элементе.</span><span class="sxs-lookup"><span data-stu-id="90a74-269">Selecting or hovering over requests reveals more information about each item.</span></span>  

:::image type="complex" source="../media/network-network-requests-table.msft.png" alt-text="Панель &quot;сеть&quot;" lightbox="../media/network-network-requests-table.msft.png":::
   <span data-ttu-id="90a74-271">Таблица запросов</span><span class="sxs-lookup"><span data-stu-id="90a74-271">The Requests table</span></span>  
:::image-end:::  

<span data-ttu-id="90a74-272">По умолчанию в таблице запросов отображаются следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="90a74-272">The Requests table displays the following columns by default.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="90a74-273">Имя</span><span class="sxs-lookup"><span data-stu-id="90a74-273">Name</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="90a74-274">Имя или идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="90a74-274">The filename of, or an identifier for, the resource.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="90a74-275">Состояние</span><span class="sxs-lookup"><span data-stu-id="90a74-275">Status</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="90a74-276">Код состояния HTTP.</span><span class="sxs-lookup"><span data-stu-id="90a74-276">The HTTP status code.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="90a74-277">Тип</span><span class="sxs-lookup"><span data-stu-id="90a74-277">Type</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="90a74-278">Тип MIME запрашиваемого ресурса.</span><span class="sxs-lookup"><span data-stu-id="90a74-278">The MIME type of the requested resource.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="90a74-279">Владельцы</span><span class="sxs-lookup"><span data-stu-id="90a74-279">Initiator</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="90a74-280">Следующие объекты или процессы инициируют запросы.</span><span class="sxs-lookup"><span data-stu-id="90a74-280">The following objects or processes initiate requests.</span></span>  
      
      *   <span data-ttu-id="90a74-281">**Средство синтаксического анализа**  Средство синтаксического анализа HTML для Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="90a74-281">**Parser**  The HTML parser for Microsoft Edge.</span></span>  
      *   <span data-ttu-id="90a74-282">**Redirect (перенаправление**  )  Переадресация HTTP.</span><span class="sxs-lookup"><span data-stu-id="90a74-282">**Redirect**  An HTTP redirect.</span></span>  
      *   <span data-ttu-id="90a74-283">**Сценарий**  Функция JavaScript.</span><span class="sxs-lookup"><span data-stu-id="90a74-283">**Script**  A JavaScript function.</span></span>  
      *   <span data-ttu-id="90a74-284">**Другие**  Некоторые другие процессы или действия, например переход на страницу с помощью ссылки или ввод URL-адреса в адресную строку.</span><span class="sxs-lookup"><span data-stu-id="90a74-284">**Other**  Some other process or action, such as navigating to a page using a link or entering a URL in the address bar.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="90a74-285">Size</span><span class="sxs-lookup"><span data-stu-id="90a74-285">Size</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="90a74-286">Объединенный размер заголовков ответа и текст ответа, доставленный сервером.</span><span class="sxs-lookup"><span data-stu-id="90a74-286">The combined size of the response headers plus the response body, as delivered by the server.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="90a74-287">Время</span><span class="sxs-lookup"><span data-stu-id="90a74-287">Time</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="90a74-288">Общая продолжительность от начала запроса до получения последнего байта в ответе.</span><span class="sxs-lookup"><span data-stu-id="90a74-288">The total duration, from the start of the request to the receipt of the final byte in the response.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="90a74-289">Каскад</span><span class="sxs-lookup"><span data-stu-id="90a74-289">Waterfall</span></span>](#view-the-timing-relationship-of-requests)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="90a74-290">Визуальная декомпозиция мероприятия для каждого запроса.</span><span class="sxs-lookup"><span data-stu-id="90a74-290">A visual breakdown of the activity for each request.</span></span>  
   :::column-end:::
:::row-end:::  

#### <span data-ttu-id="90a74-291">Добавление и удаление столбцов</span><span class="sxs-lookup"><span data-stu-id="90a74-291">Add or remove columns</span></span>  

<span data-ttu-id="90a74-292">Наведите указатель мыши на заголовок таблицы запросы, откройте контекстное меню (щелкните правой кнопкой мыши \) и выберите один из вариантов, чтобы скрыть или отобразить его.</span><span class="sxs-lookup"><span data-stu-id="90a74-292">Hover on the header of the Requests table, open the contextual menu \(right-click\), and select an option to hide or show it.</span></span>  <span data-ttu-id="90a74-293">Параметры, отображаемые в данный момент, отмечены флажками рядом с каждым элементом.</span><span class="sxs-lookup"><span data-stu-id="90a74-293">Currently displayed options have checkmarks next to each item.</span></span>  

:::image type="complex" source="../media/network-network-requests-add-column.msft.png" alt-text="Панель &quot;сеть&quot;" lightbox="../media/network-network-requests-add-column.msft.png":::
   <span data-ttu-id="90a74-295">Добавление столбца в таблицу "запросы"</span><span class="sxs-lookup"><span data-stu-id="90a74-295">Adding a column to the Requests table</span></span>  
:::image-end:::  

#### <span data-ttu-id="90a74-296">Добавление настраиваемых столбцов</span><span class="sxs-lookup"><span data-stu-id="90a74-296">Add custom columns</span></span>  

<span data-ttu-id="90a74-297">Чтобы добавить настраиваемый столбец в таблицу запросы, наведите указатель мыши на заголовок таблицы запросы, откройте контекстное меню (щелкните правой кнопкой мыши \) и выберите **заголовки ответов**  >  .**Управление столбцами заголовков**.</span><span class="sxs-lookup"><span data-stu-id="90a74-297">To add a custom column to the Requests table, hover on the header of the Requests table, open the contextual menu \(right-click\), and select **Response Headers** > **Manage Header Columns**.</span></span>  

:::image type="complex" source="../media/network-network-requests-add-custom.msft.png" alt-text="Панель &quot;сеть&quot;" lightbox="../media/network-network-requests-add-custom.msft.png":::
   <span data-ttu-id="90a74-299">Добавление настраиваемого столбца в таблицу "запросы"</span><span class="sxs-lookup"><span data-stu-id="90a74-299">Adding a custom column to the Requests table</span></span>  
:::image-end:::  

### <span data-ttu-id="90a74-300">Просмотр отношения времени между запросами</span><span class="sxs-lookup"><span data-stu-id="90a74-300">View the timing relationship of requests</span></span>  

<span data-ttu-id="90a74-301">Используйте Каскад для просмотра межвременных отношений запросов.</span><span class="sxs-lookup"><span data-stu-id="90a74-301">Use the Waterfall to view the timing relationships of requests.</span></span>  
<span data-ttu-id="90a74-302">В структуре, используемой по умолчанию для каскадов, используется время начала запроса.</span><span class="sxs-lookup"><span data-stu-id="90a74-302">The default organization of the Waterfall uses the start time of the requests.</span></span>  
<span data-ttu-id="90a74-303">Таким образом, запросы, которые раньше приступили к началу, чем те, которые находятся дальше по правому краю.</span><span class="sxs-lookup"><span data-stu-id="90a74-303">So, requests that are farther to the left started earlier than the requests that are farther to the right.</span></span>  

<span data-ttu-id="90a74-304">Чтобы просмотреть различные способы сортировки каскадов, перейдите на [фазу "Сортировка по действию](#sort-by-activity-phase)".</span><span class="sxs-lookup"><span data-stu-id="90a74-304">To review the different ways that you may sort the Waterfall, navigate to [Sort by activity phase](#sort-by-activity-phase).</span></span>  

:::image type="complex" source="../media/network-network-requests-waterfall.msft.png" alt-text="Панель &quot;сеть&quot;" lightbox="../media/network-network-requests-waterfall.msft.png":::
   <span data-ttu-id="90a74-306">Столбец "Каскад" на панели " **запросы** "</span><span class="sxs-lookup"><span data-stu-id="90a74-306">The Waterfall column of the **Requests** pane</span></span>  
:::image-end:::  

<!-- ### Analyze the frames of a WebSocket Connection  -->

<!--To view the frames of a WebSocket connection, use the following steps.  

1.  Select the URL of the WebSocket connection, under the **Name** column of the Requests table.  
1.  Select the **Frames** tab.  The table shows the last 100 frames.  

To refresh the table, re-select the name of the WebSocket connection under the **Name** column of the Requests table.  -->

<!--
:::image type="complex" source="../media/network-frames.msft.png" alt-text="Панель &quot;сеть&quot;" lightbox="../media/network-frames.msft.png":::
   The **Frames** tab  
:::image-end:::  
-->

<!--The table contains the following three columns.  

*   **Data**.  The message payload.  If the message is plain text, it is displayed here.  For binary opcodes, this column displays the name and code of the opcode.  The following opcodes are supported: Continuation Frame, Binary Frame, Connection Close Frame, Ping Frame, and Pong Frame.  
*   **Length**.  The length of the message payload, in bytes.  
*   **Time**.  The time when the message was received or sent.  -->

<!--Messages are color-coded according to each type.  

*   Outgoing text messages are light-green.  
*   Incoming text messages are white.  
*   WebSocket opcodes are light-yellow.  
*   Errors are light-red.  -->

### <span data-ttu-id="90a74-307">Предварительный просмотр тела ответа</span><span class="sxs-lookup"><span data-stu-id="90a74-307">View a preview of a response body</span></span>  

<span data-ttu-id="90a74-308">Для предварительного просмотра текста ответа выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="90a74-308">To view a preview of a response body, use the following steps.</span></span>  

1.  <span data-ttu-id="90a74-309">Выберите URL-адрес запроса в столбце " **имя** " таблицы "запросы".</span><span class="sxs-lookup"><span data-stu-id="90a74-309">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="90a74-310">Откройте вкладку **Предварительный просмотр** .</span><span class="sxs-lookup"><span data-stu-id="90a74-310">Select the **Preview** tab.</span></span>  

<span data-ttu-id="90a74-311">Эта вкладка особенно полезна для просмотра изображений.</span><span class="sxs-lookup"><span data-stu-id="90a74-311">This tab is mostly useful for viewing images.</span></span>  

:::image type="complex" source="../media/network-network-resources-preview.msft.png" alt-text="Панель &quot;сеть&quot;" lightbox="../media/network-network-resources-preview.msft.png":::
   <span data-ttu-id="90a74-313">Вкладка " **Предварительный просмотр** "</span><span class="sxs-lookup"><span data-stu-id="90a74-313">The **Preview** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="90a74-314">Просмотр текста ответа</span><span class="sxs-lookup"><span data-stu-id="90a74-314">View a response body</span></span>  

<span data-ttu-id="90a74-315">Чтобы просмотреть текст ответа на запрос, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="90a74-315">To view the response body to a request, use the following steps.</span></span>  

1.  <span data-ttu-id="90a74-316">Выберите URL-адрес запроса в столбце " **имя** " таблицы "запросы".</span><span class="sxs-lookup"><span data-stu-id="90a74-316">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="90a74-317">Откройте вкладку **ответ** .</span><span class="sxs-lookup"><span data-stu-id="90a74-317">Select the **Response** tab.</span></span>  

:::image type="complex" source="../media/network-network-resources-response.msft.png" alt-text="Панель &quot;сеть&quot;" lightbox="../media/network-network-resources-response.msft.png":::
   <span data-ttu-id="90a74-319">Вкладка " **ответ** "</span><span class="sxs-lookup"><span data-stu-id="90a74-319">The **Response** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="90a74-320">Просмотр заголовков HTTP</span><span class="sxs-lookup"><span data-stu-id="90a74-320">View HTTP headers</span></span>  

<span data-ttu-id="90a74-321">Чтобы просмотреть данные заголовка HTTP для запроса, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="90a74-321">To view HTTP header data about a request, use the following steps.</span></span>  

1.  <span data-ttu-id="90a74-322">Выберите URL-адрес запроса в столбце " **имя** " таблицы "запросы".</span><span class="sxs-lookup"><span data-stu-id="90a74-322">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="90a74-323">Откройте вкладку **заголовки** .</span><span class="sxs-lookup"><span data-stu-id="90a74-323">Select the **Headers** tab.</span></span>  

:::image type="complex" source="../media/network-resources-headers.msft.png" alt-text="Панель &quot;сеть&quot;" lightbox="../media/network-resources-headers.msft.png":::
   <span data-ttu-id="90a74-325">Вкладка " **заголовки** "</span><span class="sxs-lookup"><span data-stu-id="90a74-325">The **Headers** tab</span></span>  
:::image-end:::  

#### <span data-ttu-id="90a74-326">Просмотр источника заголовков HTTP</span><span class="sxs-lookup"><span data-stu-id="90a74-326">View HTTP header source</span></span>  

<span data-ttu-id="90a74-327">По умолчанию на вкладке заголовки отображаются имена заголовков в алфавитном порядке.</span><span class="sxs-lookup"><span data-stu-id="90a74-327">By default, the Headers tab shows header names alphabetically.</span></span>  <span data-ttu-id="90a74-328">Чтобы просмотреть имена HTTP-заголовков в полученном порядке, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="90a74-328">To view the HTTP header names in the order received, use the following steps.</span></span>  

1.  <span data-ttu-id="90a74-329">Открытие вкладки " **заголовки** " для запроса, который вас интересует.</span><span class="sxs-lookup"><span data-stu-id="90a74-329">Open the **Headers** tab for the request that interests you.</span></span>  <span data-ttu-id="90a74-330">Дополнительные сведения можно найти в разделе [Просмотр заголовков HTTP](#view-http-headers).</span><span class="sxs-lookup"><span data-stu-id="90a74-330">For more information, navigate to [View HTTP headers](#view-http-headers).</span></span>  
1.  <span data-ttu-id="90a74-331">Нажмите кнопку **источник**, рядом с разделом **заголовок запроса** или **заголовок ответа** .</span><span class="sxs-lookup"><span data-stu-id="90a74-331">Select **view source**, next to the **Request Header** or **Response Header** section.</span></span>  

### <span data-ttu-id="90a74-332">Просмотр параметров строки запроса</span><span class="sxs-lookup"><span data-stu-id="90a74-332">View query string parameters</span></span>  

<span data-ttu-id="90a74-333">Чтобы просмотреть параметры строки запроса URL-адреса в удобочитаемом формате, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="90a74-333">To view the query string parameters of a URL in a human-readable format, use the following steps.</span></span>  

1.  <span data-ttu-id="90a74-334">Открытие вкладки " **заголовки** " для запроса, который вас интересует.</span><span class="sxs-lookup"><span data-stu-id="90a74-334">Open the **Headers** tab for the request that interests you.</span></span>  <span data-ttu-id="90a74-335">Дополнительные сведения можно найти в разделе [Просмотр заголовков HTTP](#view-http-headers).</span><span class="sxs-lookup"><span data-stu-id="90a74-335">For more information, navigate to [View HTTP headers](#view-http-headers).</span></span>  
1.  <span data-ttu-id="90a74-336">Перейдите к разделу **Параметры строки запроса** .</span><span class="sxs-lookup"><span data-stu-id="90a74-336">Go to the **Query String Parameters** section.</span></span>  

:::image type="complex" source="../media/network-network-resources-headers-query-string-parameters.msft.png" alt-text="Панель &quot;сеть&quot;" lightbox="../media/network-network-resources-headers-query-string-parameters.msft.png":::
   <span data-ttu-id="90a74-338">Раздел " **Параметры строки запроса** "</span><span class="sxs-lookup"><span data-stu-id="90a74-338">The **Query String Parameters** section</span></span>  
:::image-end:::  

#### <span data-ttu-id="90a74-339">Просмотр источника параметров строки запроса</span><span class="sxs-lookup"><span data-stu-id="90a74-339">View query string parameters source</span></span>  

<span data-ttu-id="90a74-340">Чтобы просмотреть источник параметра строки запроса для запроса, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="90a74-340">To view the query string parameter source of a request, use the following steps.</span></span>  

1.  <span data-ttu-id="90a74-341">Перейдите к разделу Параметры строки запроса.</span><span class="sxs-lookup"><span data-stu-id="90a74-341">Go to the Query String Parameters section.</span></span>  <span data-ttu-id="90a74-342">Дополнительные сведения можно найти в разделе [Просмотр параметров строки запроса](#view-query-string-parameters).</span><span class="sxs-lookup"><span data-stu-id="90a74-342">For more information, navigate to [View query string parameters](#view-query-string-parameters).</span></span>  
1.  <span data-ttu-id="90a74-343">Нажмите кнопку **Просмотр источника**.</span><span class="sxs-lookup"><span data-stu-id="90a74-343">Select **view source**.</span></span>  

#### <span data-ttu-id="90a74-344">Просмотр строковых параметров запроса в кодировке URL</span><span class="sxs-lookup"><span data-stu-id="90a74-344">View URL-encoded query string parameters</span></span>  

<span data-ttu-id="90a74-345">Чтобы просмотреть параметры строки запроса в удобочитаемом формате, но с сохранением кодировки, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="90a74-345">To view query string parameters in a human-readable format, but with encodings preserved, use the following steps.</span></span>  

1.  <span data-ttu-id="90a74-346">Перейдите к разделу Параметры строки запроса.</span><span class="sxs-lookup"><span data-stu-id="90a74-346">Go to the Query String Parameters section.</span></span>  <span data-ttu-id="90a74-347">Дополнительные сведения можно найти в разделе [Просмотр параметров строки запроса](#view-query-string-parameters).</span><span class="sxs-lookup"><span data-stu-id="90a74-347">For more information, navigate to [View query string parameters](#view-query-string-parameters).</span></span>  
1.  <span data-ttu-id="90a74-348">Выберите команду **Просмотреть закодированный URL-адрес**.</span><span class="sxs-lookup"><span data-stu-id="90a74-348">Select **view URL encoded**.</span></span>  

### <span data-ttu-id="90a74-349">Просмотр файлов cookie</span><span class="sxs-lookup"><span data-stu-id="90a74-349">View cookies</span></span>  

<span data-ttu-id="90a74-350">Чтобы просмотреть cookie-файлы, отправленные в заголовке запроса HTTP, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="90a74-350">To view the cookies sent in the HTTP header of a request, use the following steps.</span></span>  

1.  <span data-ttu-id="90a74-351">Выберите URL-адрес запроса в столбце " **имя** " таблицы "запросы".</span><span class="sxs-lookup"><span data-stu-id="90a74-351">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="90a74-352">Перейдите на вкладку " **cookie** ".</span><span class="sxs-lookup"><span data-stu-id="90a74-352">Select the **Cookies** tab.</span></span>  

<!--For more information about each of the columns, navigate to [Fields][ManageDataCookiesFields].  -->  

<!--[ManageDataCookiesFields]: manage-data/cookies#fields  -->  
<!--TODO: add link when section is available -->  

:::image type="complex" source="../media/network-network-resources-cookies.msft.png" alt-text="Панель &quot;сеть&quot;" lightbox="../media/network-network-resources-cookies.msft.png":::
   <span data-ttu-id="90a74-354">Вкладка "cookie"</span><span class="sxs-lookup"><span data-stu-id="90a74-354">The Cookies tab</span></span>  
:::image-end:::  

### <span data-ttu-id="90a74-355">Просмотр разбиения по времени для запроса</span><span class="sxs-lookup"><span data-stu-id="90a74-355">View the timing breakdown of a request</span></span>  

<span data-ttu-id="90a74-356">Чтобы просмотреть межвременную разбивку запроса, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="90a74-356">To view the timing breakdown of a request, use the following steps.</span></span>  

1.  <span data-ttu-id="90a74-357">Выберите URL-адрес запроса в столбце " **имя** " таблицы "запросы".</span><span class="sxs-lookup"><span data-stu-id="90a74-357">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="90a74-358">Откройте вкладку **время** .</span><span class="sxs-lookup"><span data-stu-id="90a74-358">Select the **Timing** tab.</span></span>  

<span data-ttu-id="90a74-359">Для более удобного доступа к данным перейдите к разделу [Предварительный просмотр разбивки времени](#preview-a-timing-breakdown).</span><span class="sxs-lookup"><span data-stu-id="90a74-359">For a faster way to access the data, navigate to [Preview a timing breakdown](#preview-a-timing-breakdown).</span></span>  

<span data-ttu-id="90a74-360">Дополнительные сведения о каждой из фаз, которые могут отображаться на вкладке **время** , можно найти в разделе [этапы разбивки по времени](#timing-breakdown-phases-explained).</span><span class="sxs-lookup"><span data-stu-id="90a74-360">For more information about each of the phases that may be displayed in the **Timing** tab, navigate to [Timing breakdown phases explained](#timing-breakdown-phases-explained).</span></span>  

:::image type="complex" source="../media/network-network-resources-timing.msft.png" alt-text="Панель &quot;сеть&quot;" lightbox="../media/network-network-resources-timing.msft.png":::
   <span data-ttu-id="90a74-362">Вкладка **время**</span><span class="sxs-lookup"><span data-stu-id="90a74-362">The **Timing** tab</span></span>  
:::image-end:::  

<span data-ttu-id="90a74-363">Дополнительные сведения о каждой из фаз.</span><span class="sxs-lookup"><span data-stu-id="90a74-363">More information about each of the phases.</span></span>  

<span data-ttu-id="90a74-364">Для получения дополнительных сведений о доступе к представлению перейдите в раздел [Просмотр временных интервалов](#view-the-timing-breakdown-of-a-request).</span><span class="sxs-lookup"><span data-stu-id="90a74-364">For more information about accessing the view, navigate to [View timing breakdown](#view-the-timing-breakdown-of-a-request).</span></span>  

#### <span data-ttu-id="90a74-365">Предварительный просмотр разбивки по времени</span><span class="sxs-lookup"><span data-stu-id="90a74-365">Preview a timing breakdown</span></span>  

<span data-ttu-id="90a74-366">Чтобы просмотреть сведения о разбиении по времени для запроса, наведите указатель мыши на запись запроса в столбце " **Каскад** " таблицы "запросы".</span><span class="sxs-lookup"><span data-stu-id="90a74-366">To view a preview of the timing breakdown of a request, in the **Waterfall** column of the Requests table, hover on the entry for the request.</span></span>  

<span data-ttu-id="90a74-367">Дополнительные сведения о том, как получить доступ к данным без наведения указателя мыши, можно найти, [просмотрев временные разбивки запроса](#view-the-timing-breakdown-of-a-request).</span><span class="sxs-lookup"><span data-stu-id="90a74-367">For more information about how to access the data without hovering, navigate to [View the timing breakdown of a request](#view-the-timing-breakdown-of-a-request).</span></span>  

:::image type="complex" source="../media/network-network-resources-waterfall-hover.msft.png" alt-text="Панель &quot;сеть&quot;" lightbox="../media/network-network-resources-waterfall-hover.msft.png":::
   <span data-ttu-id="90a74-369">Предварительный просмотр разбиения по времени для запроса</span><span class="sxs-lookup"><span data-stu-id="90a74-369">Previewing the timing breakdown of a request</span></span>  
:::image-end:::  

#### <span data-ttu-id="90a74-370">Описание этапов разделения времени</span><span class="sxs-lookup"><span data-stu-id="90a74-370">Timing breakdown phases explained</span></span>  

<span data-ttu-id="90a74-371">Дополнительные сведения о каждой из фаз, которые могут отображаться на вкладке **время** .</span><span class="sxs-lookup"><span data-stu-id="90a74-371">More information about each of the phases that may display in the **Timing** tab.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="90a74-372">Очередь</span><span class="sxs-lookup"><span data-stu-id="90a74-372">Queueing</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="90a74-373">Браузер помещает запросы в очередь, если выполняется одно из следующих условий.</span><span class="sxs-lookup"><span data-stu-id="90a74-373">The browser queues requests when any of the following are true.</span></span>  
      *   <span data-ttu-id="90a74-374">Существуют запросы с более высокими приоритетами.</span><span class="sxs-lookup"><span data-stu-id="90a74-374">Higher priority requests exist.</span></span>  
      *   <span data-ttu-id="90a74-375">Шесть подключений TCP открыты для одного и того же источника, что является ограничением.</span><span class="sxs-lookup"><span data-stu-id="90a74-375">Six TCP connections are open for the same origin, which is the limit.</span></span>  <span data-ttu-id="90a74-376">Применимо только к HTTP/1.0 и HTTP/1.1.</span><span class="sxs-lookup"><span data-stu-id="90a74-376">Applies to HTTP/1.0 and HTTP/1.1 only.</span></span>  
      *   <span data-ttu-id="90a74-377">Браузер временно выделяет место в кэше на диске.</span><span class="sxs-lookup"><span data-stu-id="90a74-377">The browser is briefly allocating space in the disk cache.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="90a74-378">Блокированы</span><span class="sxs-lookup"><span data-stu-id="90a74-378">Stalled</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="90a74-379">Запрос будет остановлен в любой из причин, описанных в разделе **очереди**.</span><span class="sxs-lookup"><span data-stu-id="90a74-379">The request is stalled for any of the reasons described in **Queueing**.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="90a74-380">Поиск DNS</span><span class="sxs-lookup"><span data-stu-id="90a74-380">DNS Lookup</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="90a74-381">Браузер разрешает IP-адрес запроса.</span><span class="sxs-lookup"><span data-stu-id="90a74-381">The browser is resolving the IP address for the request.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="90a74-382">Начальное соединение</span><span class="sxs-lookup"><span data-stu-id="90a74-382">Initial connection</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="90a74-383">Браузер устанавливает подключение, в том числе подтверждения TCP, повторы TCP и согласовывающие безопасный уровень сокетов.</span><span class="sxs-lookup"><span data-stu-id="90a74-383">The browser establishes a connection including TCP handshakes, TCP retries, and negotiates a Secure Socket Layer.</span></span>
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="90a74-384">Согласование прокси-сервера</span><span class="sxs-lookup"><span data-stu-id="90a74-384">Proxy negotiation</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="90a74-385">Браузер согласовывает запрос с [прокси-сервером][WikiProxyServer].</span><span class="sxs-lookup"><span data-stu-id="90a74-385">The browser is negotiating the request with a [proxy server][WikiProxyServer].</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="90a74-386">Отправлено запросов</span><span class="sxs-lookup"><span data-stu-id="90a74-386">Request sent</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="90a74-387">Запрос отправляется.</span><span class="sxs-lookup"><span data-stu-id="90a74-387">The request is being sent.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="90a74-388">Подготовка ServiceWorker</span><span class="sxs-lookup"><span data-stu-id="90a74-388">ServiceWorker Preparation</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="90a74-389">Браузер запускает сотрудника службы.</span><span class="sxs-lookup"><span data-stu-id="90a74-389">The browser is starting the service worker.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="90a74-390">Запрос на ServiceWorker</span><span class="sxs-lookup"><span data-stu-id="90a74-390">Request to ServiceWorker</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="90a74-391">Запрос отправляется сотруднику службы.</span><span class="sxs-lookup"><span data-stu-id="90a74-391">The request is being sent to the service worker.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="90a74-392">Ожидание \ (TTFB \)</span><span class="sxs-lookup"><span data-stu-id="90a74-392">Waiting \(TTFB\)</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="90a74-393">Браузер ожидает первый байт ответа.</span><span class="sxs-lookup"><span data-stu-id="90a74-393">The browser is waiting for the first byte of a response.</span></span>  <span data-ttu-id="90a74-394">TTFB означает время для первого байта.</span><span class="sxs-lookup"><span data-stu-id="90a74-394">TTFB stands for Time To First Byte.</span></span>  <span data-ttu-id="90a74-395">Это время включает один цикл обработки задержки и время, затраченное сервером на подготовку ответа.</span><span class="sxs-lookup"><span data-stu-id="90a74-395">This timing includes one round trip of latency and the time the server took to prepare the response.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="90a74-396">Загрузка содержимого</span><span class="sxs-lookup"><span data-stu-id="90a74-396">Content Download</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="90a74-397">Браузер получает ответ.</span><span class="sxs-lookup"><span data-stu-id="90a74-397">The browser is receiving the response.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="90a74-398">Получение push-уведомлений</span><span class="sxs-lookup"><span data-stu-id="90a74-398">Receiving Push</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="90a74-399">Браузер получает данные для этого ответа через HTTP/2 серверную извещающую передачу.</span><span class="sxs-lookup"><span data-stu-id="90a74-399">The browser is receiving data for this response via HTTP/2 Server Push.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="90a74-400">Чтение push-уведомлений</span><span class="sxs-lookup"><span data-stu-id="90a74-400">Reading Push</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="90a74-401">Браузер читает локальные данные, полученные ранее.</span><span class="sxs-lookup"><span data-stu-id="90a74-401">The browser is reading the local data previously received.</span></span>  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="90a74-402">Просмотр инициаторов и зависимостей</span><span class="sxs-lookup"><span data-stu-id="90a74-402">View initiators and dependencies</span></span>  

<span data-ttu-id="90a74-403">Чтобы просмотреть инициаторы и зависимости запроса, удерживайте `Shift` и наведите указатель мыши на запрос в таблице запросы.</span><span class="sxs-lookup"><span data-stu-id="90a74-403">To view the initiators and dependencies of a request, hold `Shift`and hover over the request in the Requests table.</span></span>  <span data-ttu-id="90a74-404">DevTools цвета: инициаторы отображаются зеленым цветом, а зависимости — красным.</span><span class="sxs-lookup"><span data-stu-id="90a74-404">DevTools colors: initiators are shown in green and dependencies are shown in red.</span></span>  

:::image type="complex" source="../media/network-network-resources-initiators-dependencies.msft.png" alt-text="Панель &quot;сеть&quot;" lightbox="../media/network-network-resources-initiators-dependencies.msft.png":::
   <span data-ttu-id="90a74-406">Просмотр инициаторов и зависимостей запроса</span><span class="sxs-lookup"><span data-stu-id="90a74-406">Viewing the initiators and dependencies of a request</span></span>  
:::image-end:::  

<span data-ttu-id="90a74-407">Если таблица запросы упорядочивается хронологически, при наведении указателя мыши на строку, предшествующую ей, выводится зеленый запрос.</span><span class="sxs-lookup"><span data-stu-id="90a74-407">When the Requests table is ordered chronologically, if you hover on a line, the line preceding it displays a green request.</span></span>  <span data-ttu-id="90a74-408">Зеленый запрос — инициатор зависимости.</span><span class="sxs-lookup"><span data-stu-id="90a74-408">The green request is the initiator of the dependency.</span></span>  <span data-ttu-id="90a74-409">Если в строке перед этим отображается еще один зеленый запрос, это более высокий запрос является инициатором инициатора.</span><span class="sxs-lookup"><span data-stu-id="90a74-409">If another green request is displayed on the line before that, that higher request is the initiator of the initiator.</span></span>  <span data-ttu-id="90a74-410">И так далее.</span><span class="sxs-lookup"><span data-stu-id="90a74-410">And so on.</span></span>  

### <span data-ttu-id="90a74-411">Просмотр событий загрузки</span><span class="sxs-lookup"><span data-stu-id="90a74-411">View load events</span></span>  

<span data-ttu-id="90a74-412">DevTools отображает время показа `DOMContentLoaded` `load` событий в нескольких местах на панели "сеть".</span><span class="sxs-lookup"><span data-stu-id="90a74-412">DevTools displays the timing of the `DOMContentLoaded` and `load` events in multiple places on the Network panel.</span></span>  <span data-ttu-id="90a74-413">`DOMContentLoaded`Событие окрашивается синим цветом, а `load` событие — красным.</span><span class="sxs-lookup"><span data-stu-id="90a74-413">The `DOMContentLoaded` event is colored blue, and the `load` event is red.</span></span>  

:::image type="complex" source="../media/network-network-requests-load-events.msft.png" alt-text="Панель &quot;сеть&quot;" lightbox="../media/network-network-requests-load-events.msft.png":::
   <span data-ttu-id="90a74-415">Расположение `DOMContentLoaded` событий "и" `load` на панели "сеть"</span><span class="sxs-lookup"><span data-stu-id="90a74-415">The locations of the `DOMContentLoaded` and `load` events on the Network panel</span></span>  
:::image-end:::  

### <span data-ttu-id="90a74-416">Просмотр общего числа запросов</span><span class="sxs-lookup"><span data-stu-id="90a74-416">View the total number of requests</span></span>  

<span data-ttu-id="90a74-417">Общее количество запросов можно найти в области сводки в нижней части панели "сеть".</span><span class="sxs-lookup"><span data-stu-id="90a74-417">The total number of requests is listed in the Summary pane, at the bottom of the Network panel.</span></span>  

> [!CAUTION]
> <span data-ttu-id="90a74-418">Этот номер отслеживает только те запросы, которые были зарегистрированы с момента открытия DevTools.</span><span class="sxs-lookup"><span data-stu-id="90a74-418">This number only tracks requests that have been logged since DevTools was opened.</span></span>  <span data-ttu-id="90a74-419">Если при открытии DevTools возникли другие запросы, эти запросы не учитываются.</span><span class="sxs-lookup"><span data-stu-id="90a74-419">If other requests occurred before DevTools was opened, those requests are not counted.</span></span>  

:::image type="complex" source="../media/network-network-total-requests.msft.png" alt-text="Панель &quot;сеть&quot;" lightbox="../media/network-network-total-requests.msft.png":::
   <span data-ttu-id="90a74-421">Общее количество запросов с момента открытия DevTools</span><span class="sxs-lookup"><span data-stu-id="90a74-421">The total number of requests since DevTools were opened</span></span>  
:::image-end:::  

### <span data-ttu-id="90a74-422">Просмотр общего объема загружаемого файла</span><span class="sxs-lookup"><span data-stu-id="90a74-422">View the total download size</span></span>  

<span data-ttu-id="90a74-423">Общий объем загруженных запросов отображается в области Сводка в нижней части панели "сеть".</span><span class="sxs-lookup"><span data-stu-id="90a74-423">The total download size of requests is listed in the Summary pane, at the bottom of the Network panel.</span></span>  

> [!CAUTION]
> <span data-ttu-id="90a74-424">Этот номер отслеживает только те запросы, которые были зарегистрированы с момента открытия DevTools.</span><span class="sxs-lookup"><span data-stu-id="90a74-424">This number only tracks requests that have been logged since DevTools was opened.</span></span>  <span data-ttu-id="90a74-425">Если при открытии DevTools возникли другие запросы, предыдущие запросы не учитываются.</span><span class="sxs-lookup"><span data-stu-id="90a74-425">If other requests occurred before DevTools was opened, the previous requests are not counted.</span></span>  

:::image type="complex" source="../media/network-network-total-download-size.msft.png" alt-text="Панель &quot;сеть&quot;" lightbox="../media/network-network-total-download-size.msft.png":::
   <span data-ttu-id="90a74-427">Общий объем загруженных запросов</span><span class="sxs-lookup"><span data-stu-id="90a74-427">The total download size of requests</span></span>  
:::image-end:::  

<span data-ttu-id="90a74-428">Чтобы убедиться в том, что после того как браузер распаковать все элементы, перейдите к разделу [Просмотр несжатого размера ресурса](#view-the-uncompressed-size-of-a-resource).</span><span class="sxs-lookup"><span data-stu-id="90a74-428">To verify how large resources are after the browser uncompresses each item, navigate to [View the uncompressed size of a resource](#view-the-uncompressed-size-of-a-resource).</span></span>  

### <span data-ttu-id="90a74-429">Просмотр трассировки стека, которая привела к запросу</span><span class="sxs-lookup"><span data-stu-id="90a74-429">View the stack trace that caused a request</span></span>  

<span data-ttu-id="90a74-430">После того, как инструкция JavaScript запрашивает ресурс, наведите указатель мыши на столбец **инициатора** , чтобы просмотреть трассировку стека, выступающей в запрос.</span><span class="sxs-lookup"><span data-stu-id="90a74-430">After a JavaScript statement requests a resource, hover over the **Initiator** column to view the stack trace leading up to the request.</span></span>  

<!-- [codepen.io/contoso/pen/yLBrOWa?editors=0010#0](https://codepen.io/contoso/pen/yLBrOWa?editors=0010#0) -->  

<!--
```javascript
function init() {
  getData();
}

function getData() {
  fetch('https:/httpbin.org/get?message=hi');
}

init();
```  
-->  

:::image type="complex" source="../media/network-network-requests-initiator-stack.msft.png" alt-text="Панель &quot;сеть&quot;" lightbox="../media/network-network-requests-initiator-stack.msft.png":::
   <span data-ttu-id="90a74-432">Трассировка стека, ведущая к запросу ресурсов</span><span class="sxs-lookup"><span data-stu-id="90a74-432">The stack trace leading up to a resource request</span></span>  
:::image-end:::  

### <span data-ttu-id="90a74-433">Просмотр несжатого размера ресурса</span><span class="sxs-lookup"><span data-stu-id="90a74-433">View the uncompressed size of a resource</span></span>  

<span data-ttu-id="90a74-434">Установите флажок **использовать строки большого запроса** , а затем посмотрите на нижнее значение столбца **Размер** .</span><span class="sxs-lookup"><span data-stu-id="90a74-434">Select the **Use large request rows** checkbox and then look at the bottom value of the **Size** column.</span></span>  

:::image type="complex" source="../media/network-network-requests-uncompressed-compare.msft.png" alt-text="Панель &quot;сеть&quot;" lightbox="../media/network-network-requests-uncompressed-compare.msft.png":::
   <span data-ttu-id="90a74-436">Пример несжатых ресурсов \ (сжатый размер `jquery-3.3.1.min.js` файла, отправленного по сети `29.9 KB` , в то время как несжатый размер `84.9 KB` )</span><span class="sxs-lookup"><span data-stu-id="90a74-436">An example of uncompressed resources  \(The compressed size of the `jquery-3.3.1.min.js` file that was sent over the network was `29.9 KB`, whereas the uncompressed size was `84.9 KB`\)</span></span>  
:::image-end:::  

## <span data-ttu-id="90a74-437">Данные запросов на экспорт</span><span class="sxs-lookup"><span data-stu-id="90a74-437">Export requests data</span></span>  

### <span data-ttu-id="90a74-438">Сохранение всех сетевых запросов в файле HAR</span><span class="sxs-lookup"><span data-stu-id="90a74-438">Save all network requests to a HAR file</span></span>  

<span data-ttu-id="90a74-439">Чтобы сохранить все сетевые запросы в файле HAR, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="90a74-439">To save all network requests to a HAR file, complete the following steps.</span></span>  

1.  <span data-ttu-id="90a74-440">Наведите указатель мыши на любой запрос в таблице запросов и откройте контекстное меню (щелкните правой кнопкой мыши \).</span><span class="sxs-lookup"><span data-stu-id="90a74-440">Hover on any request in the Requests table and open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="90a74-441">Выберите команду **Сохранить как HAR с содержимым**.</span><span class="sxs-lookup"><span data-stu-id="90a74-441">Select **Save as HAR with Content**.</span></span>  <span data-ttu-id="90a74-442">DevTools сохраняет все запросы, произошедшие после того, как вы открыли DevTools в файл HAR.</span><span class="sxs-lookup"><span data-stu-id="90a74-442">DevTools saves all requests that have occurred since you opened DevTools to the HAR file.</span></span>  <span data-ttu-id="90a74-443">Вы не можете фильтровать запросы.</span><span class="sxs-lookup"><span data-stu-id="90a74-443">You are not able to filter requests.</span></span>  <span data-ttu-id="90a74-444">Вы также не можете сохранить один запрос.</span><span class="sxs-lookup"><span data-stu-id="90a74-444">You are also not able to save a single request.</span></span>  

<span data-ttu-id="90a74-445">После того как вы сохраните файл HAR, вы можете импортировать его обратно в DevTools для анализа.</span><span class="sxs-lookup"><span data-stu-id="90a74-445">Once you save a HAR file, you may import it back into DevTools for analysis.</span></span>  <span data-ttu-id="90a74-446">Просто перетащите файл HAR в таблицу запросы.</span><span class="sxs-lookup"><span data-stu-id="90a74-446">Just drag-and-drop the HAR file into the Requests table.</span></span>  
<!--For more information, navigate to also [HAR Analyzer][HARAnalyzer].  -->  

<!--[HARAnalyzer]: https://toolbox.alphabetapps.com/apps/har_analyzer  -->  
<!--Todo: add section link when content is available  -->  

:::image type="complex" source="../media/network-network-requests-save-har-content.msft.png" alt-text="Панель &quot;сеть&quot;" lightbox="../media/network-network-requests-save-har-content.msft.png":::
   <span data-ttu-id="90a74-448">Выбор команды " **Сохранить как HAR с контентом** "</span><span class="sxs-lookup"><span data-stu-id="90a74-448">Selecting **Save as HAR with Content**</span></span>  
:::image-end:::  

### <span data-ttu-id="90a74-449">Копирование одного или нескольких запросов в буфер обмена</span><span class="sxs-lookup"><span data-stu-id="90a74-449">Copy one or more requests to the clipboard</span></span>  

<span data-ttu-id="90a74-450">В столбце **имя** таблицы запросы наведите указатель мыши на запрос, откройте контекстное меню (щелкните правой кнопкой мыши \), наведите указатель на пункт **Копировать**и выберите один из следующих вариантов.</span><span class="sxs-lookup"><span data-stu-id="90a74-450">Under the **Name** column of the Requests table, hover on a request, open the contextual menu \(right-click\), hover over **Copy**, and select one of the following options.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="90a74-451">Копировать адрес ссылки</span><span class="sxs-lookup"><span data-stu-id="90a74-451">Copy Link Address</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="90a74-452">Скопируйте URL-адрес запроса в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="90a74-452">Copy the URL of the request to the clipboard.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="90a74-453">Копирование ответа</span><span class="sxs-lookup"><span data-stu-id="90a74-453">Copy Response</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="90a74-454">Скопировать текст ответа в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="90a74-454">Copy the response body to the clipboard.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="90a74-455">Копировать как выборку</span><span class="sxs-lookup"><span data-stu-id="90a74-455">Copy as Fetch</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="90a74-456">Копирование в виде изогнутого документа</span><span class="sxs-lookup"><span data-stu-id="90a74-456">Copy as cURL</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="90a74-457">Копирование запроса в виде текстовой команды.</span><span class="sxs-lookup"><span data-stu-id="90a74-457">Copy the request as a cURL command.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="90a74-458">Копировать все как выборку</span><span class="sxs-lookup"><span data-stu-id="90a74-458">Copy All as Fetch</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="90a74-459">Копирование в виде изогнутого документа</span><span class="sxs-lookup"><span data-stu-id="90a74-459">Copy All as cURL</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="90a74-460">Копирование всех запросов в виде последовательности команд с фигурой.</span><span class="sxs-lookup"><span data-stu-id="90a74-460">Copy all requests as a chain of cURL commands.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="90a74-461">Копирование всех как HAR</span><span class="sxs-lookup"><span data-stu-id="90a74-461">Copy All as HAR</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="90a74-462">Скопируйте все запросы как данные HAR.</span><span class="sxs-lookup"><span data-stu-id="90a74-462">Copy all requests as HAR data.</span></span>  
   :::column-end:::
:::row-end:::  

:::image type="complex" source="../media/network-network-requests-copy-response.msft.png" alt-text="Панель &quot;сеть&quot;" lightbox="../media/network-network-requests-copy-response.msft.png":::
   <span data-ttu-id="90a74-464">Выбор пункта " **Копировать ответ** "</span><span class="sxs-lookup"><span data-stu-id="90a74-464">Selecting **Copy Response**</span></span>  
:::image-end:::  

## <span data-ttu-id="90a74-465">Изменение макета панели "сеть"</span><span class="sxs-lookup"><span data-stu-id="90a74-465">Change the layout of the Network panel</span></span>  

<span data-ttu-id="90a74-466">Вы можете развернуть или свернуть разделы пользовательского интерфейса панели "сеть", чтобы сосредоточиться на важных сведениях.</span><span class="sxs-lookup"><span data-stu-id="90a74-466">You may expand or collapse sections of the Network panel UI to focus important information.</span></span>  

### <span data-ttu-id="90a74-467">Скрытие области фильтров</span><span class="sxs-lookup"><span data-stu-id="90a74-467">Hide the Filters pane</span></span>  

<span data-ttu-id="90a74-468">По умолчанию DevTools отображает **область фильтров**.</span><span class="sxs-lookup"><span data-stu-id="90a74-468">By default, DevTools show the **Filters pane**.</span></span>  
<span data-ttu-id="90a74-469">Щелкните **Фильтр** \ ( ![ фильтр ][ImageFilterIcon] \), чтобы скрыть его.</span><span class="sxs-lookup"><span data-stu-id="90a74-469">Select **Filter** \(![Filter][ImageFilterIcon]\) to hide it.</span></span>  

:::image type="complex" source="../media/network-network-resources-hide-filters-button.msft.png" alt-text="Панель &quot;сеть&quot;" lightbox="../media/network-network-resources-hide-filters-button.msft.png":::
   <span data-ttu-id="90a74-471">Кнопка "скрыть фильтры"</span><span class="sxs-lookup"><span data-stu-id="90a74-471">The Hide Filters button</span></span>  
:::image-end:::  

### <span data-ttu-id="90a74-472">Использование строк большого запроса</span><span class="sxs-lookup"><span data-stu-id="90a74-472">Use large request rows</span></span>  

<span data-ttu-id="90a74-473">Используйте большие строки, если вы хотите, чтобы в таблице сетевых запросов больше пробелов.</span><span class="sxs-lookup"><span data-stu-id="90a74-473">Use large rows when you want more whitespace in your network requests table.</span></span>  <span data-ttu-id="90a74-474">Некоторые столбцы также содержат дополнительные сведения при использовании больших строк.</span><span class="sxs-lookup"><span data-stu-id="90a74-474">Some columns also provide a little more information when using large rows.</span></span>  <span data-ttu-id="90a74-475">Например, минимальное значение столбца « **Размер** » — это несжатый размер запроса.</span><span class="sxs-lookup"><span data-stu-id="90a74-475">For example, the bottom value of the **Size** column is the uncompressed size of a request.</span></span>  

:::image type="complex" source="../media/network-network-requests-large-request-rows.msft.png" alt-text="Панель &quot;сеть&quot;" lightbox="../media/network-network-requests-large-request-rows.msft.png":::
   <span data-ttu-id="90a74-477">Пример строк большого запроса в области " **запросы** "</span><span class="sxs-lookup"><span data-stu-id="90a74-477">An example of large request rows in the **Requests** pane</span></span>  
:::image-end:::  

<span data-ttu-id="90a74-478">Установите флажок **использовать строки большого запроса** , чтобы включить большие строки.</span><span class="sxs-lookup"><span data-stu-id="90a74-478">Select the **Use large request rows** checkbox to enable large rows.</span></span>  

:::image type="complex" source="../media/network-network-requests-use-large-request-rows-on.msft.png" alt-text="Панель &quot;сеть&quot;" lightbox="../media/network-network-requests-use-large-request-rows-on.msft.png":::
   <span data-ttu-id="90a74-480">Флажок " **использовать строки большого запроса** "</span><span class="sxs-lookup"><span data-stu-id="90a74-480">The **Use large request rows** checkbox</span></span>  
:::image-end:::  

### <span data-ttu-id="90a74-481">Скрытие области обзора</span><span class="sxs-lookup"><span data-stu-id="90a74-481">Hide the Overview pane</span></span>  

<span data-ttu-id="90a74-482">По умолчанию DevTools отображает **область "Общие сведения**".</span><span class="sxs-lookup"><span data-stu-id="90a74-482">By default, DevTools show the **Overview pane**.</span></span>  <span data-ttu-id="90a74-483">Снимите флажок **Показать общие сведения** , чтобы скрыть его.</span><span class="sxs-lookup"><span data-stu-id="90a74-483">Deselect the **Show Overview** checkbox to hide it.</span></span>  

:::image type="complex" source="../media/network-network-requests-show-overview-off.msft.png" alt-text="Панель &quot;сеть&quot;" lightbox="../media/network-network-requests-show-overview-off.msft.png":::
   <span data-ttu-id="90a74-485">Флажок " **Показать общие сведения** "</span><span class="sxs-lookup"><span data-stu-id="90a74-485">The **Show Overview** checkbox</span></span>  
:::image-end:::  

<!-- image links -->  

[ImageCaptureScreenshotsIcon]: ../media/capture-screenshots-icon.msft.png  
[ImageClearIcon]: ../media/clear-requests-icon.msft.png  
[ImageFilterIcon]: ../media/filter-icon.msft.png  
[ImageHideIcon]: ../media/hide-overview-icon.msft.png  
[ImageLargeResourceRowsIcon]: ../media/large-resource-rows-button-icon.msft.png  
[ImageRecordOnIcon]: ../media/record-on-icon.msft.png  

<!-- links -->  

[DevtoolsProgressiveWebApps]: ../progressive-web-apps.md "Отладка последовательного веб-приложения | Документы Microsoft"  

<!--[NetworkConditions]: /microsoft-edge/devtools-guide-chromium/network/network-conditions "Optimize Performance Under Varying Network Conditions | Microsoft Docs"  -->  

[MDNHTTPDataURIs]: https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/Data_URIs "URL-адреса данных | MDN"  

[WikiProxyServer]: https://en.wikipedia.org/wiki/Proxy_server "Прокси-сервер — Википедии"  

> [!NOTE]
> <span data-ttu-id="90a74-489">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="90a74-489">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="90a74-490">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/network/reference) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="90a74-490">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/network/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="90a74-492">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="90a74-492">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
