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





# Отладка фоновых служб с помощью Microsoft Edge DevTools   



Раздел " **фоновые службы** " Microsoft Edge DevTools — это набор средств для API JavaScript, который позволяет веб-сайту отправлять и получать обновления даже в том случае, если ваш веб-сайт не открыт.  
Фоновая служба функционально напоминает [фоновый процесс] [WikiBackgroundProcess].  
Microsoft Edge DevTools считает каждый из указанных ниже API фоновой службой.  

*   [Фоновая выборка](#background-fetch)  
*   [Фоновая синхронизация](#background-sync)  
*   [Уведомления](#notifications)  
*   [Push-сообщения](#push-messages)  
    
Microsoft Edge DevTools может записывать события фоновой службы в течение 3 дней, даже если DevTools не открыт.  
Это поможет вам убедиться в том, что события отправляются и принимаются должным образом.  Кроме того, вы можете просмотреть сведения о каждом событии.  

:::image type="complex" source="../media/javascript-application-background-services-push-messaging.msft.png" alt-text="Просмотр сведений о событии в области Push-сообщений" lightbox="../media/javascript-application-background-services-push-messaging.msft.png":::
   Просмотр сведений о событии в области **Push-сообщений**  
:::image-end:::  

## Фоновая выборка   

*Интерфейс API фоновой выборки** позволяет **сотруднику службы** надежно загружать большие ресурсы, например фильмы и подкасты, в качестве фоновой службы.  Для записи события фоновой выборки в течение 3 дней, даже если DevTools не открыт:  

<!--Todo: add background fetch api section when available -->  

1.  [Откройте DevTools][OpenDevTools].  
1.  Откройте панель **приложения** .  
1.  Открытие области " **Фоновая выборка** ".  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch-empty.msft.png" alt-text="Просмотр сведений о событии в области Push-сообщений" lightbox="../media/javascript-application-background-services-background-fetch-empty.msft.png":::
       Область " **Фоновая выборка** "  
    :::image-end:::  
    
1.  Нажмите **запись** \ ( ![ запись ][ImageRecordIcon] \).  
   После запуска некоторых операций фоновой выборки DevTools регистрирует события в таблице.  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch.msft.png" alt-text="Просмотр сведений о событии в области Push-сообщений" lightbox="../media/javascript-application-background-services-background-fetch.msft.png":::
       Журнал событий в области " **Фоновая выборка** "  
    :::image-end:::  
    
1.  Щелкните событие, чтобы просмотреть сведения о нем в пространстве под таблицей.  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch-details.msft.png" alt-text="Просмотр сведений о событии в области Push-сообщений" lightbox="../media/javascript-application-background-services-background-fetch-details.msft.png":::
       Просмотр сведений о событии в области " **Фоновая выборка** "  
    :::image-end:::  
    
## Фоновая синхронизация   

**API фоновой синхронизации** позволяет автономному **рабочему специалисту** отправлять данные на сервер после повторного установления надежного Интернет-соединения.  Чтобы записать события фоновой синхронизации в течение 3 дней, даже если DevTools не открыт, выполните указанные ниже действия.  

<!--Todo: add background sync api section when available -->  

1.  [Откройте DevTools][OpenDevTools].  
1.  Откройте панель **приложения** .  
1.  Откройте область **фоновая синхронизация** .  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync-empty.msft.png" alt-text="Просмотр сведений о событии в области Push-сообщений" lightbox="../media/javascript-application-background-services-background-sync-empty.msft.png":::
       Область " **фоновая синхронизация** "  
    :::image-end:::  
    
1.  Нажмите **запись** \ ( ![ запись ][ImageRecordIcon] \).  
   После запуска некоторых операций синхронизации в фоновом режиме DevTools регистрирует события в таблице.  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync.msft.png" alt-text="Просмотр сведений о событии в области Push-сообщений" lightbox="../media/javascript-application-background-services-background-sync.msft.png":::
       Журнал событий в области " **фоновая синхронизация** "  
    :::image-end:::  
    
1.  Щелкните событие, чтобы просмотреть сведения о нем в пространстве под таблицей.  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync-details.msft.png" alt-text="Просмотр сведений о событии в области Push-сообщений" lightbox="../media/javascript-application-background-services-background-sync-details.msft.png":::
       Просмотр сведений о событии в области **фоновой синхронизации**  
    :::image-end:::  
    
## Уведомления 

После того как **сотрудник службы** получил [Push-сообщение][MDNPush] с сервера, сотрудник службы использует [API уведомлений][MDNNotifications] для отображения данных для пользователя.  Для ведения журнала уведомлений в течение 3 дней, даже если DevTools не открыт:  

1.  [Откройте DevTools][OpenDevTools].  
1.  Откройте панель **приложения** .  
1.  Открытие области **уведомлений** .  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications-empty.msft.png" alt-text="Просмотр сведений о событии в области Push-сообщений" lightbox="../media/javascript-application-background-services-notifications-empty.msft.png":::
       Область **уведомлений**  
    :::image-end:::  
    
1.  Нажмите **запись** \ ( ![ запись ][ImageRecordIcon] \).  
   После запуска некоторых действий с уведомлениями DevTools регистрирует события в таблице.  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications.msft.png" alt-text="Просмотр сведений о событии в области Push-сообщений" lightbox="../media/javascript-application-background-services-notifications.msft.png":::
       Журнал событий в области **уведомлений**  
    :::image-end:::  
    
1.  Щелкните событие, чтобы просмотреть сведения о нем в пространстве под таблицей.  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications-details.msft.png" alt-text="Просмотр сведений о событии в области Push-сообщений" lightbox="../media/javascript-application-background-services-notifications-details.msft.png":::
       Просмотр сведений о событии в области **уведомлений**  
    :::image-end:::  
    
## Push-сообщения 

Чтобы отобразить push-уведомление для пользователя, **сотрудник службы** должен сначала использовать [API Push-сообщений][MDNPush] для получения данных с сервера.  Когда сотрудник службы готов отобразить уведомление, он использует [API уведомлений][MDNNotifications].  Чтобы регистрировать push-сообщения в течение 3 дней, даже если DevTools не открыт, выполните указанные ниже действия.  

1.  [Откройте DevTools][OpenDevTools].  
1.  Откройте панель **приложения** .  
1.  Открыть область **Push-сообщений** .  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging-empty.msft.png" alt-text="Просмотр сведений о событии в области Push-сообщений" lightbox="../media/javascript-application-background-services-push-messaging-empty.msft.png":::
       Область **Push-сообщений**  
    :::image-end:::  
    
1.  Нажмите **запись** \ ( ![ запись ][ImageRecordIcon] \).  
    После запуска некоторых действий Push-сообщений DevTools регистрирует события в таблице.  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging.msft.png" alt-text="Просмотр сведений о событии в области Push-сообщений" lightbox="../media/javascript-application-background-services-push-messaging.msft.png":::
       Журнал событий в области Push- **сообщений**  
    :::image-end:::  
    
1.  Щелкните событие, чтобы просмотреть сведения о нем в пространстве под таблицей.  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging-details.msft.png" alt-text="Просмотр сведений о событии в области Push-сообщений" lightbox="../media/javascript-application-background-services-push-messaging-details.msft.png":::
       Просмотр сведений о событии в области **Push-сообщений**  
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
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/javascript/background-services) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  
[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
