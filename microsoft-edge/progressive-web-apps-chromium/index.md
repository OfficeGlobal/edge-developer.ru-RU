---
description: Прогрессивные веб-приложения (Chromium) изначально работают в Windows 10.  Вот все, что вам нужно знать как веб-разработчик.
title: Прогрессивные веб-приложения для Windows
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/01/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: pwa
keywords: прогрессивные веб-приложения, PWA, EDGE, JavaScript, Windows, UWP, Microsoft Store
ms.openlocfilehash: a9fa08a9c84ee5da8eab3c9c3edeea34439b6557
ms.sourcegitcommit: be76feed0d616a96c77ea2748a9f0d6c0c06284b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/07/2020
ms.locfileid: "11103944"
---
# Прогрессивные веб-приложения для Windows  

[Прогрессивные веб-приложения][MDNApps] \ (PWAs \) предоставляют доступ к открытым веб-технологиям для взаимодействия между платформами и предоставляют пользователям собственный интерфейс, подобный приложению, настроенный для своих устройств.  PWAs — это веб-сайты, которые будут [последовательно расширены][AListApartUnderstandingProgressiveEnhancement] для работы, например собственные приложения на поддерживаемых платформах.  В приложениях PWA объединены лучшие качестве веб- и собственных приложения.  

:::row:::
    :::column:::
        :::image type="icon" source="./media/i_search.png":::
        ### [Обнаруживаемым][MDNPwaAdvantagesDiscoverable]
        Из результатов поиска в Интернете и поддержки магазинов приложений
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_package.png":::
        ### [Устанавливаемый][MDNPwaAdvantagesInstallable]
        Закрепление и запуск на начальном экране, меню "Пуск", панели задач и т. д.
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_push-notification.png":::
        ### [Повторное участие][MDNPwaAdvantagesReEngageable]
        Отправлять push-уведомления, даже если приложение неактивно
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        :::image type="icon" source="./media/i_offline.png":::
        ### [Сетевая независимость][MDNPwaAdvantagesNetworkIndependent]
        Работа в автономном режиме и в условиях низкой сети
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_progressive.png":::
        ### [JPEG][MDNPwaAdvantagesProgressive]
        Работа с возможностями устройства в масштабе (или в меньшую сторону)
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_security.png":::
        ### [Безопасной][MDNPwaAdvantagesSafe]
        Обеспечивает защищенную конечную точку HTTPS и другие меры для защиты от пользователей
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        :::image type="icon" source="./media/i_responsive.png":::
        ### [Хорошая скорость отклика][MDNPwaAdvantagesResponsive]
        Адаптируется к размеру экрана или ориентации и методу ввода для пользователя
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_link.png":::
        ### [Связь][MDNPwaAdvantagesLinkable]
        Предоставление общего доступа к файлу и его запуск с помощью стандартной гиперссылки
    :::column-end:::
    :::column:::
        &nbsp;  
    :::column-end:::
:::row-end:::  


Создайте или преобразуйте существующий веб-сайт в Project Web App, чтобы улучшить свое сотрудничество с пользователями.  Усовершенствования включают push-уведомления, интеграцию с приложением и поддержку в автономном режиме.  Продолжайте разрабатывать аудитории в открытом веб-браузере, чтобы пользователи обнаружили, что вы можете найти в PWA с помощью поиска и совместного использования ссылок.  Для этого ваше приложение Обновлено с использованием кода веб-сервера.  

## PWAs в Microsoft EDGE (Chromium)  

При создании последовательного веб-приложения, нацеленного на веб-интерфейс API, приложение может быть развернуто на разных платформах и устройствах и использовать возможности, доступные для конкретных устройств.  PWAs в Microsoft Edge \ (Chromium \) добавьте следующие преимущества на ваш веб-сайт.  

*   Ваше приложение строится на веб-платформе, основанной на стандартах.  
*   Позволяет пользователям устанавливать приложение прямо из браузера.  
*   Позволяет пользователям устанавливать приложение без развертывания и регистрации на основе магазина.  
    
Классическое PWAs поддерживается на любой из платформ Microsoft Edge \ (Chromium \). Microsoft Edge \ (Chromium \) доступен в Windows 7, Windows 10 и macOS.  Включены следующие преимущества:  

*   Приложения можно устанавливать прямо из браузера с помощью значка **установки** на панели навигации.  
    
    :::image type="complex" source="./media/install_pwa_icon.png" alt-text="Всплывающее меню и значок установки приложения" lightbox="./media/install_pwa_icon.png":::
       Всплывающее меню и значок установки приложения  
    :::image-end:::  
    
*   Кроме того, в меню " **Параметры**" приложения можно устанавливать, запускать и управлять приложениями.  >  **Apps**  
    
    :::image type="complex" source="./media/app_menus.png" alt-text="Всплывающее меню и значок установки приложения" lightbox="./media/app_menus.png":::
       Элементы меню "приложение" в разделе "Параметры"  
    :::image-end:::  
    
*   Веб-уведомления интегрированы в систему уведомлений Windows  
*   Общее хранилище файлов cookie с профилем браузера, в котором установлено приложение  
*   Доступ к другим функциям браузера с помощью меню " **Настройка" и других** параметров \ ( `...` \), включая проверку сертификата, разрешения сайтов, защиту от слежения и расширения браузера.  
*   Полный доступ к [Microsoft Edge DevTools][DevtoolsProgressiveWebApps] для отладки приложения  
    
> [!IMPORTANT]
> Чтобы настроить PWAs специально для Windows 10, которые делают запросы API WinRT с помощью JavaScript, перейдите в [документацию, относящуюся к функциям EDGEHTML PWA][PwaEdgehtmlIndex].  Узнайте больше о том, как тестировать PWA в Windows 10 и распространять его в Microsoft Store.  

> [!NOTE]
> Дополнительные сведения о преимуществах PWA, предстоящих функциях и кратких видеодемонстрациях можно найти в разделе [Сборка сеанса 2020 PWA][BuildVideo]. 

## Требования  

Для работы в качестве PWA веб-приложение, размещенное на сервере, должно включать следующие минимальные требования.  

:::row:::
   :::column span="1":::
      [HTTPS][WikiHttps]  
   :::column-end:::
   :::column span="2":::
      Защищает пользователей, обеспечивая безопасное подключение для обмена данными между сервером и приложением.  Сотрудники служб и другие технологии PWA работают только с веб-ресурсами, обслуживаемыми в безопасном соединении (или в `localhost` целях отладки).  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Служебные сценарии][MDNServiceWorkerApi]  
   :::column-end:::
   :::column span="2":::
      Использует рабочие потоки службы, чтобы выступать в качестве сетевых прокси между сервером и клиентским приложением.  Рабочие потоки служб предоставляют поддержку в автономном режиме, кэширование ресурсов, Push-уведомления, фоновую синхронизацию данных и оптимизации производительности загрузки страниц.    
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Манифест веб-приложения][MDNWebAppManifest]  
   :::column-end:::
   :::column span="2":::
      Предоставляет файл метаданных на основе JSON, в котором описаны ключевые сведения о вашем веб-приложении, так что Windows 10 и другие платформы узла предоставляют пользователям PWA возможности устанавливаемого и собственного приложения.  Ключевые сведения включают значки, язык и точку входа URL-адреса. 
   :::column-end:::
:::row-end:::  

Для того чтобы стать прекрасным PWA, ваше приложение должно также отвечать указанным ниже требованиям.  

:::row:::
   :::column span="1":::
      [Совместимость с различными браузерами][MDNCrossBrowserTesting]  
   :::column-end:::
   :::column span="2":::
      Убедитесь, что веб-приложение PWA [работает в разных][MicrosoftDeveloperEdgeToolsRemote] браузерах и средах.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Адаптивный дизайн][WikiResponsiveWebDesign]  
   :::column-end:::
   :::column span="2":::
      Применение жидких макетов и гибких изображений.  Высокореагируый дизайн включает следующие элементы, которые адаптирует пользовательский интерфейс к устройству пользователя.  
      
      *   [Сетка][MDNCssGridLayout] CSS  
      *   [расположен][MDNCssFlexibleBoxLayout]  
      *   Сетка и [Гибкая][MDNCssFlexibleBoxLayout] [Таблица][MDNCssGridLayout] CSS  
      *   [запросы мультимедиа][MDNMediaQueries]  
      *   [отклики изображений][MDNResponsiveImages]  
      
      Использует [средства эмуляции устройства][DevToolsGuide|::ref1::|] в браузере для проверки локально или создания [сеанса удаленной отладки][DevToolsProtocolClientsEdgeDevToolsPreview] для проверки непосредственно на целевом устройстве.
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Глубокая связь][WikiDeepLinking]  
   :::column-end:::
   :::column span="2":::
      Каждая страница сайта отправляется на уникальный URL-адрес, чтобы пользователи могли использовать более обширную аудиторию через функцию совместного использования социальных сетей.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Рекомендации по проверке и тестированию][Webhint]  
   :::column-end:::
   :::column span="2":::
      Использование средств качества кода, таких как Linter веб – [Подсказка][Webhint] , для оптимизации эффективности, надежности, безопасности и специальных возможностей вашего приложения.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Контрольный список для Chromium PWA][WebDevGoodPwaChecklist]  
   :::column-end:::
   :::column span="2":::
      Проверка PWA на соответствие контрольному списку Google Baseline Access.  
   :::column-end:::
:::row-end:::  

> [!NOTE]
> Чтобы преобразовать PWA в приложение [Microsoft Store][MicrosoftDeveloperStore] , перейдите в [раздел прогрессивные веб-приложения (EdgeHTML) в Microsoft Store][PwaEdgehtmlMicrosoftStore].  
  
## См. также  

*   [Myth Busting PWAs][Davrous20191018MythBustingPwasNewEdgeEdition]  
*   [Прогрессивный план для последовательного веб-приложения][CloudfourThinksProgressiveRoadmapYourWebApp]  
*   [Автономные публикации с прогрессивными веб-приложениями][MediumWebEdgeOfflinePostsProgressiveWebApps]  
*   [PWA Q&A][AaronGustafsonNotebookPwaQa]  
*   [Ставкам в Интернете][JoretegBlogBettingWeb]  
*   [Именование последовательного веб-приложения][Fberriman20170626NamingProgressiveWebApps]  
*   [Проектирование и создание последовательного веб-приложения без структуры (часть 1)][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart1]  
*   [Проектирование и создание последовательного веб-приложения без структуры (часть 2)][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart2]  
*   [Проектирование и создание последовательного веб-приложения без структуры (часть 3)][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart3]  
    
<!-- links -->  

[DevToolsProtocolClientsEdgeDevToolsPreview]: ../devtools-protocol/0.1/clients.md#microsoft-edge-devtools-preview "Предварительный просмотр Средств разработчика в Microsoft Edge — Клиенты протокола средств разработчика"  
[DevToolsGuideEmulation]: ../devtools-guide/emulation.md "Эмуляция"  
[DevtoolsProgressiveWebApps]: ../devtools-guide-chromium/progressive-web-apps.md "Отладка последовательного веб-приложения"  
[DevGuideWhatsNewEdgeHtml17]: ../dev-guide/whats-new/edgehtml-17.md "Новые возможности EdgeHTML 17"  
[DevGuideWhatsNewEdgeHtml14]: ../dev-guide/whats-new/edgehtml-14.md "Новые возможности EdgeHTML 14"  
[PwaEdgehtmlIndex]: ../progressive-web-apps-edgehtml/index.md "Прогрессивные веб-приложения (EdgeHTML) в Windows"  
[PwaEdgehtmlMicrosoftStore]: ../progressive-web-apps-edgehtml/microsoft-store.md "Прогрессивные веб-приложения в Microsoft Store"
<!--PwaEdgehtmlMicrosoftStoreCriteriaAutomaticSubmission]: ../progressive-web-apps-edgehtml/microsoft-store.md#criteria-for-automatic-submission "Criteria for automatic submission - Progressive Web Apps in the Microsoft Store"  -->  

[WindowsUWPControlsPatternTilesNotificationsWns]: /windows/uwp/controls-and-patterns/tiles-and-notifications-windows-push-notification-services--wns--overview.md "Общие сведения о службах push-уведомлений Windows \ (WNS \)"  
[WindowsUWPDesignDevicesDesigningTv]: /windows/uwp/design/devices/designing-for-tv.md "Проектирование для Xbox и телевизора"  
[WindowsUWPDesignDevicesIndex]: /windows/uwp/design/devices/index.md "Вопросы пользовательского интерфейса для устройств UWP"  
[WindowsUWPGetStartedGuide]: /windows/uwp/get-started/universal-application-platform-guide.md "Что такое приложение универсальной платформы Windows (UWP)?"  
[WindowsUWPLaunchResumeBackgroundTasks]: /windows/uwp/launch-resume/support-your-app-with-background-tasks.md "Поддержка приложения с помощью фоновых задач"  
[WindowsUWPPublishIndex]: /windows/uwp/publish/index.md "Публикация приложений и игр для Windows"  
[WindowsUWPPublishDeveloperAccount]: /windows/uwp/publish/opening-a-developer-account.md "Открытие учетной записи разработчика"  

[WindowsBlogsWelcomingPWAsEdgeWindows]: https://blogs.windows.com/msedgedev/2018/02/06/welcoming-progressive-web-apps-edge-windows-10/#56z7mJwKsykfbR4I.97 "Welcoming последовательного веб-приложения в Microsoft EDGE и Windows 10 — блоги Windows"  
[MicrosoftDeveloperEdgePlatformStatusBackgroundSync]: https://developer.microsoft.com/microsoft-edge/platform/status/backgroundsyncapi "API фоновой синхронизации — состояние платформы Microsoft Edge"  
[MicrosoftDeveloperEdgePlatformStatusWebApplicationManifest]: https://developer.microsoft.com/microsoft-edge/platform/status/webapplicationmanifest "Манифест веб-приложения — состояние платформы Microsoft Edge"  
[MicrosoftDeveloperEdgeToolsRemote]: https://developer.microsoft.com/microsoft-edge/tools/remote "Мгновенное Тестирование"  
[MicrosoftDeveloperWindowsMixedReality]: https://developer.microsoft.com/windows/mixed-reality "Смешанная реальность для разработчиков"  
[MicrosoftDeveloperWindowsSurfaceHub]: https://developer.microsoft.com/windows/surfacehub "Microsoft Surface HUB"  
[MicrosoftDeveloperStore]: https://developer.microsoft.com/store "Магазин Microsoft Developer"  
[MicrosoftEdge]: https://www.microsoft.com/edge "Скачать новый браузер Microsoft Edge"  
[MicrosoftSupportWindowsFocusAssist]: https://support.microsoft.com/help/4026996/windows-10-turn-focus-assist-on-or-off "Включение и отключение фокусной помощи в Windows 10"  
[MicrosoftSupportWindowsNotificationSettings]: https://support.microsoft.com/help/4028678/windows-10-change-notification-settings "Изменение параметров уведомлений в Windows 10"  

[AaronGustafsonNotebookPwaQa]: https://www.aaron-gustafson.com/notebook/pwa-qa "PWA Q&A"  

[AListApartUnderstandingProgressiveEnhancement]: https://alistapart.com/article/understandingprogressiveenhancement "Раскрывающийся список "последовательное расширение""  

[MDNApps]: https://developer.mozilla.org/Apps/Progressive "приложения | MDN"  
[MDNCache]: https://developer.mozilla.org/docs/Web/API/Cache "Кэш | MDN"  
[MDNCrossBrowserTesting]: https://developer.mozilla.org/docs/Learn/Tools_and_testing/Cross_browser_testing "Тестирование нескольких браузеров | MDN"  
[MDNCssFlexibleBoxLayout]: https://developer.mozilla.org/docs/Web/CSS/CSS_Flexible_Box_Layout "Макет гибких полей CSS | MDN"  
[MDNCssGridLayout]: https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout "Макет сетки CSS | MDN"  
[MDNFetchApi]: https://developer.mozilla.org/docs/Web/API/Fetch_API "Получить API | MDN"  
[MDNMediaQueries]: https://developer.mozilla.org/docs/Web/CSS/Media_Queries "Запросы мультимедиа | MDN"  
[MDNNotificationsApi]: https://developer.mozilla.org/docs/Web/API/Notifications_API "API уведомлений | MDN"  
[MDNPushApi]: https://developer.mozilla.org/docs/Web/API/Push_API "API push-уведомлений | MDN"  
[MDNPwaAdvantagesDiscoverable]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Discoverable "Возможности, которые могут быть обнаружены последовательностью веб-приложения"  
[MDNPwaAdvantagesInstallable]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Installable "Преимущества устанавливаемого веб-приложения с прогрессивным управлением"  
[MDNPwaAdvantagesLinkable]: https://developer.mozilla.org/Apps/Progressive/Advantages#Linkable "Преимущества веб-приложений, поддерживающих связь"  
[MDNPwaAdvantagesNetworkIndependent]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Network_independent "Преимущества независимых от сети веб-приложений"  
[MDNPwaAdvantagesProgressive]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Progressive "Преимущества последовательного веб-приложения"  
[MDNPwaAdvantagesReEngageable]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Re-engageable "Повторное подключение к веб-приложениям с последовательной подобщением"  
[MDNPwaAdvantagesResponsive]: https://developer.mozilla.org/Apps/Progressive/Advantages#Responsive "Преимущества использования веб-приложения с откликом"  
[MDNPwaAdvantagesSafe]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Safe "Преимущества надежного веб-приложения"  
[MDNResponsiveImages]: https://developer.mozilla.org/docs/Learn/HTML/Multimedia_and_embedding/Responsive_images "Изображения с откликом | MDN"  
[MDNServiceWorkerApi]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API "API рабочего процесса службы | MDN"  
[MDNSyncManager]: https://developer.mozilla.org/docs/Web/API/SyncManager "SyncManager | MDN"  
[MDNWebAppManifest]: https://developer.mozilla.org/docs/Web/Manifest "Манифест веб-приложения | MDN"  

[BuildVideo]: https://www.youtube.com/watch?v=y4p_QHZtMKM "Видео PWA"  

[CloudfourThinksProgressiveRoadmapYourWebApp]: https://cloudfour.com/thinks/a-progressive-roadmap-for-your-progressive-web-app "Прогрессивный план для последовательного веб-приложения"  

[Davrous20191018MythBustingPwasNewEdgeEdition]: https://www.davrous.com/2019/10/18/myth-busting-pwas-the-new-edge-edition "Myth busting PWAs — новый выпуск Edge"  

[Fberriman20170626NamingProgressiveWebApps]: https://fberriman.com/2017/06/26/naming-progressive-web-apps "Именование последовательного веб-приложения"  

[JoretegBlogBettingWeb]: https://joreteg.com/blog/betting-on-the-web "Ставкам в Интернете"  

[MediumWebEdgeOfflinePostsProgressiveWebApps]: https://medium.com/web-on-the-edge/offline-posts-with-progressive-web-apps-fc2dc4ad895 "Автономные публикации с прогрессивными веб-приложениями"  

[PWABuilder]: https://www.pwabuilder.com "PWABuilder"  

[Smashingmagazine201907ProgressiveWebApplicationFrameworkPart1]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-1 "Проектирование и создание последовательного веб-приложения без структуры (часть 1)"  

[Smashingmagazine201907ProgressiveWebApplicationFrameworkPart2]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-2 "Проектирование и создание последовательного веб-приложения без структуры (часть 2)"  

[Smashingmagazine201907ProgressiveWebApplicationFrameworkPart3]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-3 "Проектирование и создание последовательного веб-приложения без структуры (часть 3)"  

[WebDevGoodPwaChecklist]: https://web.dev/pwa-checklist "Что делает подходящее прогрессивное веб-приложение? | Web. dev"  

[Webhint]: https://webhint.io "Подсказка"  

[WikiDeepLinking]: https://en.wikipedia.org/wiki/Deep_linking "Глубокая связь — Википедии"  
[WikiHttps]: https://en.wikipedia.org/wiki/HTTPS "HTTPS-Википедии"  
[WikiResponsiveWebDesign]: https://en.wikipedia.org/wiki/Responsive_web_design "Отклики на веб-дизайн — Википедии"  
