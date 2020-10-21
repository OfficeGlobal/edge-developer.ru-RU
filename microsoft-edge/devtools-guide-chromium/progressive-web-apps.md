---
description: С помощью панели приложения можно просматривать, изменять и отлаживать манифесты веб-приложения, рабочие процессы служб и служебные кэши служб.
title: Отладка последовательного веб-приложения
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 80475ebcbbdd3fb04fd0196e993c933e0bdcf090
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125393"
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

# <span data-ttu-id="537c4-104">Отладка последовательного веб-приложения</span><span class="sxs-lookup"><span data-stu-id="537c4-104">Debug Progressive Web Apps</span></span>  

<span data-ttu-id="537c4-105">С помощью панели **приложения** можно просматривать, изменять и отлаживать манифесты веб-приложения, рабочие процессы служб и служебные кэши служб.</span><span class="sxs-lookup"><span data-stu-id="537c4-105">Use the **Application** panel to inspect, modify, and debug web app manifests, service workers, and service worker caches.</span></span>  

<!--Related Guides:  

*   [Progressive Web Apps](/web/progressive-web-apps)  -->

<!--TODO:  Link web "Progressive Web Apps" section when available. -->

<span data-ttu-id="537c4-106">В этом руководстве рассматриваются только прогрессивные возможности веб-приложений на панели **приложения** .</span><span class="sxs-lookup"><span data-stu-id="537c4-106">This guide only discusses the Progressive Web App features of the **Application** panel.</span></span>  <!--If you're looking for help on the other panes, check out the last section of this guide, [Other Application panel guides](#other-application-panel-guides).  -->

<!--TODO:  Link to sections when available. -->

### <span data-ttu-id="537c4-107">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="537c4-107">Summary</span></span>  

*   <span data-ttu-id="537c4-108">Используйте область **манифеста** для проверки манифеста веб-приложения и триггера Add to начальный экран Events.</span><span class="sxs-lookup"><span data-stu-id="537c4-108">Use the **Manifest** pane to inspect your web app manifest and trigger Add to Homescreen events.</span></span>  
*   <span data-ttu-id="537c4-109">Область " **сотрудники службы** " используется для целого ряда задач, связанных с рабочими процессами, например для отмены регистрации или обновления службы, эмуляции извещающих событий, перехода в автономный режим или остановки рабочего процесса.</span><span class="sxs-lookup"><span data-stu-id="537c4-109">Use the **Service Workers** pane for a whole range of service-worker-related tasks, like unregistering or updating a service, emulating push events, going offline, or stopping a service worker.</span></span>  
*   <span data-ttu-id="537c4-110">Просмотр кэша рабочих процессов службы из области **хранилища кэша** .</span><span class="sxs-lookup"><span data-stu-id="537c4-110">View your service worker cache from the **Cache Storage** pane.</span></span>  
*   <span data-ttu-id="537c4-111">Отмена регистрации сотрудника службы и удаление всех хранилищ и кэшей с одним нажатием кнопки из области **очистки хранилища** .</span><span class="sxs-lookup"><span data-stu-id="537c4-111">Unregister a service worker and clear all storage and caches with a single button click from the **Clear storage** pane.</span></span>  
    
## <span data-ttu-id="537c4-112">Манифест веб-приложения</span><span class="sxs-lookup"><span data-stu-id="537c4-112">Web app manifest</span></span>  

<span data-ttu-id="537c4-113">Если вы хотите, чтобы пользователи смогли добавить ваше приложение на свой мобильный homescreens, вам понадобится манифест веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="537c4-113">If you want your users to be able to add your app to their mobile homescreens, you need a web app manifest.</span></span>  <span data-ttu-id="537c4-114">Манифест определяет, как приложение появляется на начальный экран, где можно направить пользователя при запуске из начальный экран и что приложение будет выглядеть при запуске.</span><span class="sxs-lookup"><span data-stu-id="537c4-114">The manifest defines how the app appears on the homescreen, where to direct the user when launching from homescreen, and what the app looks like on launch.</span></span>  

<!--Related Guides:  

*   [Improve user experiences with a Web App Manifest](/web/fundamentals/web-app-manifest)  
*   [Using App Install Banners](/web/fundamentals/app-install-banners)  -->

<!--TODO:  Link to sections when available. -->

<span data-ttu-id="537c4-115">После настройки манифеста вы можете проверить ее с помощью панели " **Манифест** " на панели " **приложение** ".</span><span class="sxs-lookup"><span data-stu-id="537c4-115">After you have your manifest set up, you can use the **Manifest** pane of the **Application** panel to inspect it.</span></span>  

:::image type="complex" source="./media/manifest-pane.msft.png" alt-text="Область «манифест»" lightbox="./media/manifest-pane.msft.png":::
   <span data-ttu-id="537c4-117">Область « **Манифест** »</span><span class="sxs-lookup"><span data-stu-id="537c4-117">The **Manifest** Pane</span></span>  
:::image-end:::  

*   <span data-ttu-id="537c4-118">Чтобы просмотреть источник манифеста, щелкните ссылку под меткой **манифест приложения** \ ( `https://airhorner.com/manifest.json` на предыдущем рисунке).</span><span class="sxs-lookup"><span data-stu-id="537c4-118">To look at the manifest source, click the link below **App Manifest** label \(`https://airhorner.com/manifest.json` in the previous figure\).</span></span>  
<!-- *   Press the **Add to homescreen** button to simulate an Add to Homescreen event.  Check out the next section for more information.  -->  
*   <span data-ttu-id="537c4-119">В разделах " **удостоверение** " и " **Презентация** " отображаются только поля из источника манифеста в более удобном для пользователя дисплее.</span><span class="sxs-lookup"><span data-stu-id="537c4-119">The **Identity** and **Presentation** sections just display fields from the manifest source in a more user-friendly display.</span></span>  
*   <span data-ttu-id="537c4-120">В разделе **значков** появится каждый заданный вами значок.</span><span class="sxs-lookup"><span data-stu-id="537c4-120">The **Icons** section displays every icon that you've specified.</span></span>  
    
<!--### Simulate Add to Homescreen events  -->

<!--A web app can only be added to a homescreen when the site is visited at least twice, with at least five minutes between visits.  While developing or debugging your Add to Homescreen workflow, this criteria can be inconvenient.  
The **Add to homescreen** button on the **App Manifest** pane lets you simulate Add to Homescreen events whenever you want.  -->

<!--You can test out this feature with the [Microsoft I/O 2016 progressive web app](https://events.alpahabet.com/io2016/), which has proper support for Add to Homescreen.  Clicking on **Add to Homescreen** while the app is open prompts Microsoft Edge to display the "add this site to your shelf" banner, which is the desktop equivalent of the "add to homescreen" banner for mobile devices.  -->

<!--  
:::image type="complex" source="./media/io.msft.png" alt-text="Область «манифест»" lightbox="./media/io.msft.png":::
   Add to desktop shelf  
:::image-end:::
-->  

<!--
> [!Tip]
> Keep the **Console** drawer open while simulating Add to Homescreen events.  The Console tells you if your manifest has any issues and logs other information about the Add to Homescreen lifecycle.  -->

<!--The **Add to Homescreen** feature cannot yet simulate the workflow for mobile devices.  Notice how the "add to shelf" prompt was triggered in the screenshot above, even though DevTools is in Device Mode.  However, if you can successfully add your app to your desktop shelf, then it'll work for mobile, too.  -->

<!-- TODO: Rework content after sample app is created. -->

<!--If you want to test out the genuine mobile experience, you can connect a real mobile device to DevTools via **remote debugging**, and then click the **Add to Homescreen** button \(on DevTools\) to trigger the "add to homescreen" prompt on the connected mobile device.  -->

<!--TODO:  Link Debug "remote debugging" sections when available. -->

## <span data-ttu-id="537c4-121">Служебные сценарии</span><span class="sxs-lookup"><span data-stu-id="537c4-121">Service workers</span></span>  

<span data-ttu-id="537c4-122">ИТ-специалисты — это фундаментальная технология в будущем.</span><span class="sxs-lookup"><span data-stu-id="537c4-122">Service workers are a fundamental technology in the future web platform.</span></span>  <span data-ttu-id="537c4-123">Они представляют собой сценарии, которые браузер работает в фоновом режиме, отделенные от веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="537c4-123">They are scripts that the browser runs in the background, separate from a web page.</span></span>  <span data-ttu-id="537c4-124">Эти сценарии позволяют получить доступ к функциям, для которых не требуется взаимодействие с веб-страницей или пользователем, например извещающих уведомлений, фоновой синхронизации и автономным режимом работы.</span><span class="sxs-lookup"><span data-stu-id="537c4-124">These scripts enable you to access features that don't need a web page or user interaction, like push notifications, background sync, and offline experiences.</span></span>  

<!--Related Guides:  

*   [Intro to Service Workers](/web/fundamentals/primers/service-worker)  
*   [Push Notifications: Timely, Relevant, and Precise](/web/fundamentals/push-notifications)  -->  
    
<!--TODO:  Link to sections when available. -->  

<span data-ttu-id="537c4-125">Область " **сотрудники службы** " на панели **приложения** — это основное место в DevTools для проверки и отладки рабочих сотрудников.</span><span class="sxs-lookup"><span data-stu-id="537c4-125">The **Service Workers** pane in the **Application** panel is the main place in DevTools to inspect and debug service workers.</span></span>  

:::image type="complex" source="./media/service-workers-pane.msft.png" alt-text="Область «манифест»" lightbox="./media/service-workers-pane.msft.png":::
   <span data-ttu-id="537c4-127">Область " **сотрудники службы** "</span><span class="sxs-lookup"><span data-stu-id="537c4-127">The **Service Workers** pane</span></span>  
:::image-end:::  

*   <span data-ttu-id="537c4-128">Если сервисный сотрудник установлен на текущую открытую страницу, вы увидите ее в списке на этой панели.</span><span class="sxs-lookup"><span data-stu-id="537c4-128">If a service worker is installed to the currently open page, then you'll see it listed on this pane.</span></span>  <span data-ttu-id="537c4-129">Например, на предыдущем рисунке имеется сотрудник службы, установленный для области `https://weather-pwa-sample.firebaseapp.com` .</span><span class="sxs-lookup"><span data-stu-id="537c4-129">For example, in the previous figure, there is a service worker installed for the scope of `https://weather-pwa-sample.firebaseapp.com`.</span></span>  
*   <span data-ttu-id="537c4-130">Флажок **offline** перевод DevTools в автономный режим.</span><span class="sxs-lookup"><span data-stu-id="537c4-130">The **Offline** checkbox puts DevTools into offline mode.</span></span>  <span data-ttu-id="537c4-131">Это эквивалентно автономному режиму, доступному на панели " **сеть** ", или `Go offline` параметром в [меню "команды][DevtoolsCommandMenuIndex]".</span><span class="sxs-lookup"><span data-stu-id="537c4-131">This is equivalent to the offline mode available from the **Network** panel, or the `Go offline` option in the [Command Menu][DevtoolsCommandMenuIndex].</span></span>  
*   <span data-ttu-id="537c4-132">Флажок **обновить при повторной загрузке** вызывает принудительное обновление сотрудника службы при каждой загрузке страницы.</span><span class="sxs-lookup"><span data-stu-id="537c4-132">The **Update on reload** checkbox forces the service worker to update on every page load.</span></span>  
*   <span data-ttu-id="537c4-133">Флажок **пропускать из сети** обходит сотрудника службы и заставляет браузер перейти к сети для запрашиваемых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="537c4-133">The **Bypass for network** checkbox bypasses the service worker and forces the browser to go to the network for requested resources.</span></span>  
*   <span data-ttu-id="537c4-134">Кнопка " **Обновить** " выполняет разовое обновление указанного сотрудника службы.</span><span class="sxs-lookup"><span data-stu-id="537c4-134">The **Update** button performs a one-time update of the specified service worker.</span></span>  
*   <span data-ttu-id="537c4-135">Кнопка " **Отправить** " эмулирует push-уведомление без полезной нагрузки \ (также называемой **Tickle**).</span><span class="sxs-lookup"><span data-stu-id="537c4-135">The **Push** button emulates a push notification without a payload \(also known as a **tickle**\).</span></span>  
*   <span data-ttu-id="537c4-136">Кнопка " **синхронизировать** " эмулирует событие синхронизации в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="537c4-136">The **Sync** button emulates a background sync event.</span></span>  
*   <span data-ttu-id="537c4-137">Кнопка Отмена **регистрации** отменяет регистрацию указанного сотрудника службы.</span><span class="sxs-lookup"><span data-stu-id="537c4-137">The **Unregister** button unregisters the specified service worker.</span></span>  <span data-ttu-id="537c4-138">Снимите флажок [Очистить хранилище](#clear-storage) , чтобы отменить регистрацию сотрудника службы и очистить хранение и кэширование при нажатии одной кнопки.</span><span class="sxs-lookup"><span data-stu-id="537c4-138">Check out [Clear storage](#clear-storage) for a way to unregister a service worker and wipe storage and caches with a single button click.</span></span>  
*   <span data-ttu-id="537c4-139">**Исходная** строка, указывающая на то, что текущий запущенный сервисный рабочий процесс был установлен.</span><span class="sxs-lookup"><span data-stu-id="537c4-139">The **Source** line tells you when the currently running service worker was installed.</span></span>  <span data-ttu-id="537c4-140">Ссылка — это имя исходного файла сотрудника службы.</span><span class="sxs-lookup"><span data-stu-id="537c4-140">The link is the name of the service worker's source file.</span></span>  <span data-ttu-id="537c4-141">Если щелкнуть ссылку, вы отправляете вам источник сотрудника службы.</span><span class="sxs-lookup"><span data-stu-id="537c4-141">Clicking on the link sends you to the service worker's source.</span></span>  
*   <span data-ttu-id="537c4-142">Строка **состояния** показывает состояние сотрудника службы.</span><span class="sxs-lookup"><span data-stu-id="537c4-142">The **Status** line tells you the status of the service worker.</span></span>  <span data-ttu-id="537c4-143">ИДЕНТИФИКАЦИОНный номер рядом с зеленым индикатором состояния \ ( `#36` на предыдущем рисунке \) — для текущего активного сотрудника службы.</span><span class="sxs-lookup"><span data-stu-id="537c4-143">The ID number next to the green status indicator \(`#36` in previous figure\) is for the currently active Service Worker.</span></span>  <span data-ttu-id="537c4-144">Рядом с состоянием отображается кнопка " **Пуск** ", а также кнопка " **остановить** " (если сотрудник службы остановлен)</span><span class="sxs-lookup"><span data-stu-id="537c4-144">Next to the status you'll see a **start** button \(if the service worker is stopped\) or a **stop** button \(if the service worker is running\).</span></span>  <span data-ttu-id="537c4-145">Сотрудники служб должны быть остановлены и запущены браузером в любое время.</span><span class="sxs-lookup"><span data-stu-id="537c4-145">Service workers are designed to be stopped and started by the browser at any time.</span></span>  <span data-ttu-id="537c4-146">Явная остановка сотрудника службы с помощью кнопки " **остановить** " может смоделировать ее.</span><span class="sxs-lookup"><span data-stu-id="537c4-146">Explicitly stopping your service worker using the **stop** button can simulate that.</span></span>  <span data-ttu-id="537c4-147">Остановка рабочего процесса — это отличный способ проверить работу вашего кода при запуске сотрудника службы.</span><span class="sxs-lookup"><span data-stu-id="537c4-147">Stopping your service worker is a great way to test how your code behaves when the service worker starts back up again.</span></span>  <span data-ttu-id="537c4-148">Она часто обнаруживает ошибки из-за неправильного предположения о постоянном глобальном состоянии.</span><span class="sxs-lookup"><span data-stu-id="537c4-148">It frequently reveals bugs due to faulty assumptions about persistent global state.</span></span>  
*   <span data-ttu-id="537c4-149">Строка " **Клиенты** " указывает источник, на область которого выдается сотрудник службы.</span><span class="sxs-lookup"><span data-stu-id="537c4-149">The **Clients** line tells you the origin that the service worker is scoped to.</span></span>  <span data-ttu-id="537c4-150">Кнопка " **фокус** " особенно полезна, если вы включили флажок **Показать все** .</span><span class="sxs-lookup"><span data-stu-id="537c4-150">The **focus** button is mostly useful when you've enabled the **show all** checkbox.</span></span>  <span data-ttu-id="537c4-151">Если этот флажок установлен, в списке будут перечислены все зарегистрированные работники службы.</span><span class="sxs-lookup"><span data-stu-id="537c4-151">When that checkbox is enabled, all registered service workers are listed.</span></span>  <span data-ttu-id="537c4-152">При нажатии кнопки **фокуса** рядом с сервисным сотрудником, работающим на другой вкладке, Microsoft Edge фокусируется на этой вкладке.</span><span class="sxs-lookup"><span data-stu-id="537c4-152">If you click on the **focus** button next to a service worker that is running in a different tab, Microsoft Edge focuses on that tab.</span></span>  
    
<span data-ttu-id="537c4-153">Если сервисный рабочий процесс вызывает ошибки, появляется новая метка **ошибки** .</span><span class="sxs-lookup"><span data-stu-id="537c4-153">If the service worker causes any errors, a new label called **Errors** shows up.</span></span>  

<!--  
:::image type="complex" source="./media/sw-error.msft.png" alt-text="Область «манифест»" lightbox="./media/sw-error.msft.png":::
   Service worker with errors  
:::image-end:::
-->  

<!--TODO:  Capture Service Worker Errors sample when available. -->
<!--TODO:  Link Web "How tickle works" sections when available. -->

## <span data-ttu-id="537c4-154">Кэши рабочих процессов служб</span><span class="sxs-lookup"><span data-stu-id="537c4-154">Service worker caches</span></span>  

<span data-ttu-id="537c4-155">Область **кэширования кэша** предоставляет доступный только для чтения список ресурсов, которые были кэшированы с помощью [API кэша][MDNWebCacheAPI]\ (рабочий процесс-служба).</span><span class="sxs-lookup"><span data-stu-id="537c4-155">The **Cache Storage** pane provides a read-only list of resources that have been cached using the \(service worker\) [Cache API][MDNWebCacheAPI].</span></span>  

:::image type="complex" source="./media/cache-pane-cache-storage-resources.msft.png" alt-text="Область «манифест»" lightbox="./media/cache-pane-cache-storage-resources.msft.png":::
   <span data-ttu-id="537c4-157">Область " **хранение кэша** "</span><span class="sxs-lookup"><span data-stu-id="537c4-157">The **Cache Storage** Pane</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="537c4-158">При первом открытии кэша и добавлении в него ресурсов DevTools может не обнаружить изменения.</span><span class="sxs-lookup"><span data-stu-id="537c4-158">The first time you open a cache and add a resource to it, DevTools might not detect the change.</span></span>  <span data-ttu-id="537c4-159">Перезагрузите страницу, и вы увидите кэш.</span><span class="sxs-lookup"><span data-stu-id="537c4-159">Reload the page and you should see the cache.</span></span>  

<span data-ttu-id="537c4-160">Если открыто два или более кэша, вы увидите их в списке под раскрывающимся списком для **хранения кэша** .</span><span class="sxs-lookup"><span data-stu-id="537c4-160">If you have two or more caches open, you'll see them listed below the **Cache Storage** dropdown.</span></span>  

:::image type="complex" source="./media/cache-pane-cache-storage.msft.png" alt-text="Область «манифест»" lightbox="./media/cache-pane-cache-storage.msft.png":::
   <span data-ttu-id="537c4-162">Раскрывающийся список **хранилища кэша**</span><span class="sxs-lookup"><span data-stu-id="537c4-162">The **Cache Storage** dropdown</span></span>  
:::image-end:::  

## <span data-ttu-id="537c4-163">Использование квоты</span><span class="sxs-lookup"><span data-stu-id="537c4-163">Quota usage</span></span>  

<span data-ttu-id="537c4-164">Некоторые ответы в области **хранилища кэша** можно пометить как "непрозрачный".</span><span class="sxs-lookup"><span data-stu-id="537c4-164">Some responses within the **Cache Storage** pane may be flagged as being "opaque".</span></span>  <span data-ttu-id="537c4-165">Это относится к ответу, извлекаемому из другого источника, например из сети **CDN** или удаленного API, когда функция [CORS][FetchHttpCorsProtocol] не включена.</span><span class="sxs-lookup"><span data-stu-id="537c4-165">This refers to a response retrieved from a different origin, like from a **CDN** or remote API, when [CORS][FetchHttpCorsProtocol] is not enabled.</span></span>  

<!--TODO:  Link Web "CDN" section when available. -->  
<!--TODO:  Link Web "opaque" section when available. -->

<span data-ttu-id="537c4-166">Чтобы не допустить утечек междоменных данных, нужно добавить дополнительное дополнение к размеру непрозрачного ответа, используемого для вычисления предельных квот хранилища \ (например, `QuotaExceeded` вызывается ли исключение \) и сообщается `navigator.storage` API.</span><span class="sxs-lookup"><span data-stu-id="537c4-166">In order to avoid leakage of cross-domain information, there's significant padding added to the size of an opaque response used for calculating storage quota limits \(for example whether a `QuotaExceeded` exception is thrown\) and reported by the `navigator.storage` API.</span></span>  

<!--TODO:  Link Estimating "`navigator.storage` API" sections when available. -->

<span data-ttu-id="537c4-167">Сведения об этом заполнении отличаются в зависимости от браузера, но для Microsoft Edge это означает, что **Минимальный размер** любого отдельного кэшированного непрозрачного ответа составляет [примерно 7 мегабайт][ChromiumIssues796060#c17].</span><span class="sxs-lookup"><span data-stu-id="537c4-167">The details of this padding vary from browser to browser, but for Microsoft Edge, this means that the **minimum size** that any single cached opaque response contributes to the overall storage usage is [approximately 7 megabytes][ChromiumIssues796060#c17].</span></span>  <span data-ttu-id="537c4-168">Это необходимо учитывать при определении количества непрозрачных ответов, которые вы хотите кэшировать, так как вы можете легко превысить ограничения квоты хранилища, так как в противном случае вы ожидаете фактический размер непрозрачных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="537c4-168">You should keep this in mind when determining how many opaque responses you want to cache, since you could easily exceeded storage quota limitations much sooner than you'd otherwise expect based on the actual size of the opaque resources.</span></span>  

<span data-ttu-id="537c4-169">Связанные направляющие:</span><span class="sxs-lookup"><span data-stu-id="537c4-169">Related Guides:</span></span>  

*   [<span data-ttu-id="537c4-170">Переполнение стека: какие ограничения применяются к непрозрачным откликам?</span><span class="sxs-lookup"><span data-stu-id="537c4-170">Stack Overflow: What limitations apply to opaque responses?</span></span>][StackOverflowLimitationsForOpaqueResponses]  
<!--*   [Alphabet work container: Understanding Storage Quota](/web/tools/Alphabet-work-container/guides/storage-quota#beware_of_opaque_responses)  -->
    
<!--TODO:  Link Work container storage quota for opaque responses section when available. -->

## <span data-ttu-id="537c4-171">Очистка хранилища</span><span class="sxs-lookup"><span data-stu-id="537c4-171">Clear storage</span></span>  

<span data-ttu-id="537c4-172">При разработке последовательного веб-приложения удобнее использовать область **очистки хранилища** .</span><span class="sxs-lookup"><span data-stu-id="537c4-172">The **Clear Storage** pane is a very useful feature when developing progressive web apps.</span></span>  <span data-ttu-id="537c4-173">В этой области можно отменить регистрацию сотрудников службы и очистить все кэши и хранилище с помощью одного нажатия кнопки.</span><span class="sxs-lookup"><span data-stu-id="537c4-173">This pane lets you unregister service workers and clear all caches and storage with a single button click.</span></span>  <!--Check out the section below to learn more.  -->

<!--Related Guides:  

*   [Clear Storage](/iterate/manage-data/local-storage#clear-storage)  -->
    
<!--TODO:  Link to sections when available. -->

<!--## Other Application panel guides   

Check out the guides below for more help on the other panes of the **Application** panel.  

Related Guides:  

*   [Inspect page resources](/iterate/manage-data/page-resources)  
*   [Inspect and manage local storage and caches](/iterate/manage-data/local-storage)  -->
    
## <span data-ttu-id="537c4-174">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="537c4-174">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](./includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsCommandMenuIndex]: ./command-menu/index.md "Выполнение команд с помощью командного меню Microsoft Edge DevTools | Документы Microsoft"  

[ChromiumIssues796060#c17]: https://bugs.chromium.org/p/chromium/issues/detail?id=796060#c17 "Chromium дата_выпуска 796060: значение хранилища кэша выводится при каждом обновлении, когда код аналитики находится в HTML"  

[FetchHttpCorsProtocol]: https://fetch.spec.whatwg.org/#http-cors-protocol  

[MDNWebCacheAPI]: https://developer.mozilla.org/docs/Web/API/Cache "Cache-API | MDN"  

[StackOverflowLimitationsForOpaqueResponses]: https://stackoverflow.com/q/39109789/385997 "Переполнение стека: какие ограничения применяются к непрозрачным откликам?"  

<!--[WebEstimatingAvailableStorageSpace]: whats-new/2017/08/estimating-available-storage-space  -->
<!--[RemoteDebugging]: /debug/remote-debugging/remote-debugging  -->

<!--[WebHowPushWorks]: /web/fundamentals/push-notifications/how-push-works  -->  
<!--[WebGlossaryCDN]: /web/fundamentals/glossary#CDN  -->
<!--[WebGlossaryOpaque]: /web/fundamentals/glossary#opaque-response  -->

> [!NOTE]
> <span data-ttu-id="537c4-179">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="537c4-179">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="537c4-180">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/progressive-web-apps) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="537c4-180">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/progressive-web-apps) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="537c4-182">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="537c4-182">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
