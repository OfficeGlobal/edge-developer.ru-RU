---
description: Отладка фоновой выборки, фоновой синхронизации, уведомлений и Push-сообщений с помощью Microsoft Edge DevTools.
title: Отладка фоновых служб с помощью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 1724bd3a5e45734555650c3d46e377161a3a7c65
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/02/2020
ms.locfileid: "10992871"
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





# <span data-ttu-id="df971-104">Отладка фоновых служб с помощью Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="df971-104">Debug Background Services With Microsoft Edge DevTools</span></span>   



<span data-ttu-id="df971-105">Раздел " **фоновые службы** " Microsoft Edge DevTools — это набор средств для API JavaScript, который позволяет веб-сайту отправлять и получать обновления даже в том случае, если ваш веб-сайт не открыт.</span><span class="sxs-lookup"><span data-stu-id="df971-105">The **Background Services** section of Microsoft Edge DevTools is a collection of tools for the JavaScript APIs that enables your website to send and receive updates even when a user does not have your website open.</span></span>  
<span data-ttu-id="df971-106">Фоновая служба функционально напоминает [фоновый процесс] [WikiBackgroundProcess].</span><span class="sxs-lookup"><span data-stu-id="df971-106">A background service is functionally similar to a [background process][WikiBackgroundProcess].</span></span>  
<span data-ttu-id="df971-107">Microsoft Edge DevTools считает каждый из указанных ниже API фоновой службой.</span><span class="sxs-lookup"><span data-stu-id="df971-107">Microsoft Edge DevTools considers each of the following APIs to be a background service:</span></span>  

*   [<span data-ttu-id="df971-108">Фоновая выборка</span><span class="sxs-lookup"><span data-stu-id="df971-108">Background Fetch</span></span>](#background-fetch)  
*   [<span data-ttu-id="df971-109">Фоновая синхронизация</span><span class="sxs-lookup"><span data-stu-id="df971-109">Background Sync</span></span>](#background-sync)  
*   [<span data-ttu-id="df971-110">Уведомления</span><span class="sxs-lookup"><span data-stu-id="df971-110">Notifications</span></span>](#notifications)  
*   [<span data-ttu-id="df971-111">Push-сообщения</span><span class="sxs-lookup"><span data-stu-id="df971-111">Push Messages</span></span>](#push-messages)  
    
<span data-ttu-id="df971-112">Microsoft Edge DevTools может записывать события фоновой службы в течение 3 дней, даже если DevTools не открыт.</span><span class="sxs-lookup"><span data-stu-id="df971-112">Microsoft Edge DevTools can log background service events for 3 days, even when DevTools is not open.</span></span>  
<span data-ttu-id="df971-113">Это поможет вам убедиться в том, что события отправляются и принимаются должным образом.</span><span class="sxs-lookup"><span data-stu-id="df971-113">This can help you make sure that events are being sent and received as expected.</span></span>  <span data-ttu-id="df971-114">Кроме того, вы можете просмотреть сведения о каждом событии.</span><span class="sxs-lookup"><span data-stu-id="df971-114">You may also inspect the details of each event.</span></span>  

:::image type="complex" source="../media/javascript-application-background-services-push-messaging.msft.png" alt-text="Просмотр сведений о событии в области Push-сообщений" lightbox="../media/javascript-application-background-services-push-messaging.msft.png":::
   <span data-ttu-id="df971-116">Просмотр сведений о событии в области **Push-сообщений**</span><span class="sxs-lookup"><span data-stu-id="df971-116">View the details of an event in the **Push Messaging** pane</span></span>  
:::image-end:::  

## <span data-ttu-id="df971-117">Фоновая выборка</span><span class="sxs-lookup"><span data-stu-id="df971-117">Background Fetch</span></span>   

<span data-ttu-id="df971-118">*Интерфейс API фоновой выборки*\* позволяет **сотруднику службы** надежно загружать большие ресурсы, например фильмы и подкасты, в качестве фоновой службы.</span><span class="sxs-lookup"><span data-stu-id="df971-118">The *Background Fetch API*\* enables a **service worker** to reliably download large resources, like movies or podcasts, as a background service.</span></span>  <span data-ttu-id="df971-119">Для записи события фоновой выборки в течение 3 дней, даже если DevTools не открыт:</span><span class="sxs-lookup"><span data-stu-id="df971-119">To log Background Fetch event for 3 days, even when DevTools is not open:</span></span>  

<!--Todo: add background fetch api section when available -->  

1.  <span data-ttu-id="df971-120">[Откройте DevTools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="df971-120">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="df971-121">Откройте панель **приложения** .</span><span class="sxs-lookup"><span data-stu-id="df971-121">Open the **Application** panel.</span></span>  
1.  <span data-ttu-id="df971-122">Открытие области " **Фоновая выборка** ".</span><span class="sxs-lookup"><span data-stu-id="df971-122">Open the **Background Fetch** pane.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch-empty.msft.png" alt-text="Просмотр сведений о событии в области Push-сообщений" lightbox="../media/javascript-application-background-services-background-fetch-empty.msft.png":::
       <span data-ttu-id="df971-124">Область " **Фоновая выборка** "</span><span class="sxs-lookup"><span data-stu-id="df971-124">The **Background Fetch** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="df971-125">Нажмите **запись** \ ( ![ запись ][ImageRecordIcon] \).</span><span class="sxs-lookup"><span data-stu-id="df971-125">Click **Record** \(![Record][ImageRecordIcon]\).</span></span>  
   <span data-ttu-id="df971-126">После запуска некоторых операций фоновой выборки DevTools регистрирует события в таблице.</span><span class="sxs-lookup"><span data-stu-id="df971-126">After triggering some Background Fetch activity, DevTools logs the events to the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch.msft.png" alt-text="Просмотр сведений о событии в области Push-сообщений" lightbox="../media/javascript-application-background-services-background-fetch.msft.png":::
       <span data-ttu-id="df971-128">Журнал событий в области " **Фоновая выборка** "</span><span class="sxs-lookup"><span data-stu-id="df971-128">A log of events in the **Background Fetch** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="df971-129">Щелкните событие, чтобы просмотреть сведения о нем в пространстве под таблицей.</span><span class="sxs-lookup"><span data-stu-id="df971-129">Click an event to view its details in the space below the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch-details.msft.png" alt-text="Просмотр сведений о событии в области Push-сообщений" lightbox="../media/javascript-application-background-services-background-fetch-details.msft.png":::
       <span data-ttu-id="df971-131">Просмотр сведений о событии в области " **Фоновая выборка** "</span><span class="sxs-lookup"><span data-stu-id="df971-131">View the details of an event in the **Background Fetch** pane</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="df971-132">Фоновая синхронизация</span><span class="sxs-lookup"><span data-stu-id="df971-132">Background Sync</span></span>   

<span data-ttu-id="df971-133">**API фоновой синхронизации** позволяет автономному **рабочему специалисту** отправлять данные на сервер после повторного установления надежного Интернет-соединения.</span><span class="sxs-lookup"><span data-stu-id="df971-133">The **Background Sync API** enables an offline **service worker** to send data to a server once it has re-established a reliable internet connection.</span></span>  <span data-ttu-id="df971-134">Чтобы записать события фоновой синхронизации в течение 3 дней, даже если DevTools не открыт, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="df971-134">To log Background Sync events for 3 days, even when DevTools is not open:</span></span>  

<!--Todo: add background sync api section when available -->  

1.  <span data-ttu-id="df971-135">[Откройте DevTools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="df971-135">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="df971-136">Откройте панель **приложения** .</span><span class="sxs-lookup"><span data-stu-id="df971-136">Open the **Application** panel.</span></span>  
1.  <span data-ttu-id="df971-137">Откройте область **фоновая синхронизация** .</span><span class="sxs-lookup"><span data-stu-id="df971-137">Open the **Background Sync** pane.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync-empty.msft.png" alt-text="Просмотр сведений о событии в области Push-сообщений" lightbox="../media/javascript-application-background-services-background-sync-empty.msft.png":::
       <span data-ttu-id="df971-139">Область " **фоновая синхронизация** "</span><span class="sxs-lookup"><span data-stu-id="df971-139">The **Background Sync** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="df971-140">Нажмите **запись** \ ( ![ запись ][ImageRecordIcon] \).</span><span class="sxs-lookup"><span data-stu-id="df971-140">Click **Record** \(![Record][ImageRecordIcon]\).</span></span>  
   <span data-ttu-id="df971-141">После запуска некоторых операций синхронизации в фоновом режиме DevTools регистрирует события в таблице.</span><span class="sxs-lookup"><span data-stu-id="df971-141">After triggering some Background Sync activity, DevTools logs the events to the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync.msft.png" alt-text="Просмотр сведений о событии в области Push-сообщений" lightbox="../media/javascript-application-background-services-background-sync.msft.png":::
       <span data-ttu-id="df971-143">Журнал событий в области " **фоновая синхронизация** "</span><span class="sxs-lookup"><span data-stu-id="df971-143">A log of events in the **Background Sync** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="df971-144">Щелкните событие, чтобы просмотреть сведения о нем в пространстве под таблицей.</span><span class="sxs-lookup"><span data-stu-id="df971-144">Click an event to view its details in the space below the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync-details.msft.png" alt-text="Просмотр сведений о событии в области Push-сообщений" lightbox="../media/javascript-application-background-services-background-sync-details.msft.png":::
       <span data-ttu-id="df971-146">Просмотр сведений о событии в области **фоновой синхронизации**</span><span class="sxs-lookup"><span data-stu-id="df971-146">View the details of an event in the **Background Sync** pane</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="df971-147">Уведомления</span><span class="sxs-lookup"><span data-stu-id="df971-147">Notifications</span></span> 

<span data-ttu-id="df971-148">После того как **сотрудник службы** получил [Push-сообщение][MDNPush] с сервера, сотрудник службы использует [API уведомлений][MDNNotifications] для отображения данных для пользователя.</span><span class="sxs-lookup"><span data-stu-id="df971-148">After a **service worker** has received a [Push Message][MDNPush] from a server, the service worker uses the [Notifications API][MDNNotifications] to display the data to a user.</span></span>  <span data-ttu-id="df971-149">Для ведения журнала уведомлений в течение 3 дней, даже если DevTools не открыт:</span><span class="sxs-lookup"><span data-stu-id="df971-149">To log Notifications for 3 days, even when DevTools is not open:</span></span>  

1.  <span data-ttu-id="df971-150">[Откройте DevTools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="df971-150">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="df971-151">Откройте панель **приложения** .</span><span class="sxs-lookup"><span data-stu-id="df971-151">Open the **Application** panel.</span></span>  
1.  <span data-ttu-id="df971-152">Открытие области **уведомлений** .</span><span class="sxs-lookup"><span data-stu-id="df971-152">Open the **Notifications** pane.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications-empty.msft.png" alt-text="Просмотр сведений о событии в области Push-сообщений" lightbox="../media/javascript-application-background-services-notifications-empty.msft.png":::
       <span data-ttu-id="df971-154">Область **уведомлений**</span><span class="sxs-lookup"><span data-stu-id="df971-154">The **Notifications** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="df971-155">Нажмите **запись** \ ( ![ запись ][ImageRecordIcon] \).</span><span class="sxs-lookup"><span data-stu-id="df971-155">Click **Record** \(![Record][ImageRecordIcon]\).</span></span>  
   <span data-ttu-id="df971-156">После запуска некоторых действий с уведомлениями DevTools регистрирует события в таблице.</span><span class="sxs-lookup"><span data-stu-id="df971-156">After triggering some Notifications activity, DevTools logs the events to the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications.msft.png" alt-text="Просмотр сведений о событии в области Push-сообщений" lightbox="../media/javascript-application-background-services-notifications.msft.png":::
       <span data-ttu-id="df971-158">Журнал событий в области **уведомлений**</span><span class="sxs-lookup"><span data-stu-id="df971-158">A log of events in the **Notifications** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="df971-159">Щелкните событие, чтобы просмотреть сведения о нем в пространстве под таблицей.</span><span class="sxs-lookup"><span data-stu-id="df971-159">Click an event to view its details in the space below the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications-details.msft.png" alt-text="Просмотр сведений о событии в области Push-сообщений" lightbox="../media/javascript-application-background-services-notifications-details.msft.png":::
       <span data-ttu-id="df971-161">Просмотр сведений о событии в области **уведомлений**</span><span class="sxs-lookup"><span data-stu-id="df971-161">View the details of an event in the **Notifications** pane</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="df971-162">Push-сообщения</span><span class="sxs-lookup"><span data-stu-id="df971-162">Push Messages</span></span> 

<span data-ttu-id="df971-163">Чтобы отобразить push-уведомление для пользователя, **сотрудник службы** должен сначала использовать [API Push-сообщений][MDNPush] для получения данных с сервера.</span><span class="sxs-lookup"><span data-stu-id="df971-163">To display a push notification to a user, a **service worker** must first use the [Push Message API][MDNPush] to receive data from a server.</span></span>  <span data-ttu-id="df971-164">Когда сотрудник службы готов отобразить уведомление, он использует [API уведомлений][MDNNotifications].</span><span class="sxs-lookup"><span data-stu-id="df971-164">When the service worker is ready to display the notification, it uses the [Notifications API][MDNNotifications].</span></span>  <span data-ttu-id="df971-165">Чтобы регистрировать push-сообщения в течение 3 дней, даже если DevTools не открыт, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="df971-165">To log Push Messages for 3 days, even when DevTools is not open:</span></span>  

1.  <span data-ttu-id="df971-166">[Откройте DevTools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="df971-166">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="df971-167">Откройте панель **приложения** .</span><span class="sxs-lookup"><span data-stu-id="df971-167">Open the **Application** panel.</span></span>  
1.  <span data-ttu-id="df971-168">Открыть область **Push-сообщений** .</span><span class="sxs-lookup"><span data-stu-id="df971-168">Open the **Push Messaging** pane.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging-empty.msft.png" alt-text="Просмотр сведений о событии в области Push-сообщений" lightbox="../media/javascript-application-background-services-push-messaging-empty.msft.png":::
       <span data-ttu-id="df971-170">Область **Push-сообщений**</span><span class="sxs-lookup"><span data-stu-id="df971-170">The **Push Messaging** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="df971-171">Нажмите **запись** \ ( ![ запись ][ImageRecordIcon] \).</span><span class="sxs-lookup"><span data-stu-id="df971-171">Click **Record** \(![Record][ImageRecordIcon]\).</span></span>  
    <span data-ttu-id="df971-172">После запуска некоторых действий Push-сообщений DevTools регистрирует события в таблице.</span><span class="sxs-lookup"><span data-stu-id="df971-172">After triggering some Push Message activity, DevTools logs the events to the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging.msft.png" alt-text="Просмотр сведений о событии в области Push-сообщений" lightbox="../media/javascript-application-background-services-push-messaging.msft.png":::
       <span data-ttu-id="df971-174">Журнал событий в области Push- **сообщений**</span><span class="sxs-lookup"><span data-stu-id="df971-174">A log of events in the **Push Messaging** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="df971-175">Щелкните событие, чтобы просмотреть сведения о нем в пространстве под таблицей.</span><span class="sxs-lookup"><span data-stu-id="df971-175">Click an event to view its details in the space below the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging-details.msft.png" alt-text="Просмотр сведений о событии в области Push-сообщений" lightbox="../media/javascript-application-background-services-push-messaging-details.msft.png":::
       <span data-ttu-id="df971-177">Просмотр сведений о событии в области **Push-сообщений**</span><span class="sxs-lookup"><span data-stu-id="df971-177">View the details of an event in the **Push Messaging** pane</span></span>  
    :::image-end:::  
    
<!--  
 


-->  

<!-- image links -->  

[ImageRecordIcon]: ../media/record-icon.msft.png  

<!-- links -->  

<!--[BackgroundFetchAPI]: ../../../microsoft-edge/devtools-guide-chromium/whats-new/2018/12/background-fetch.md "Background Fetch API"  -->  
<!--[BackgroundSyncAPI]: ../../../microsoft-edge/devtools-guide-chromium/whats-new/2015/12/background-sync.md  "Background Sync API"  -->

[OpenDevTools]: ../open.md "Открытие средств разработчика Microsoft EDGE (Chromium) | Документы Microsoft"  

[MDNNotifications]: https://developer.mozilla.org/docs/Web/API/Notifications_API "API уведомлений | MDN"  
[MDNPush]: https://developer.mozilla.org/docs/Web/API/Push_API "API push-уведомлений | MDN"  
<!--[ServiceWorkerCacheStorage]: https://alphabet.dev/service-workers-cache-storage "Service workers and the Cache Storage API | alphabet.dev"  -->
[WikiBackgroundProcess]: https://en.wikipedia.org/wiki/Background_process "фоновый процесс — Википедии"  

> [!NOTE]
> <span data-ttu-id="df971-182">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="df971-182">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="df971-183">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/javascript/background-services) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="df971-183">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/background-services) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  
[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="df971-185">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="df971-185">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
