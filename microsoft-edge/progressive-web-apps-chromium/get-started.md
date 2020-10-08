---
description: В этом руководстве вы найдете общие сведения о базовых данных и средствах для создания последовательного веб-приложения (Chromium) в Windows.
title: Приступая к работе с прогрессивными веб-приложениями (Chromium)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/01/2020
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: прогрессивные веб-приложения, PWA, EDGE, Windows, PWABuilder, веб-манифест, специалист по обслуживанию, отправка
ms.openlocfilehash: 065ced3afa8ecd4165325fd4f10a673d86c72fa7
ms.sourcegitcommit: be76feed0d616a96c77ea2748a9f0d6c0c06284b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/07/2020
ms.locfileid: "11103926"
---
# Приступая к работе с прогрессивными веб-приложениями (Chromium)  

Прогрессивные веб-приложения \ (PWAs \) — это веб-приложения, которые являются [последовательно улучшенными][WikiProgressiveEnhancement].  Улучшенные возможности, такие как установка, Автономная поддержка и Push-уведомления, включают в себя подобные функции приложения.  Кроме того, вы можете упаковать веб – приложение PWA для магазинов приложений.  Возможно, в магазинах приложений есть магазин Microsoft Store, Google Play, Mac App Store и многое другое.  Microsoft Store — это коммерческое приложение, встроенное в Windows 10.  

В приведенном ниже руководстве представлен обзор основ PWA, создание простого веб-приложения и расширение его как PWA.  Готовый проект работает в современных браузерах.  

> [!TIP]
> Вы можете использовать [PWABuilder][PwaBuilder] для создания нового PWA, улучшения существующего веб-приложения PWA или упаковки для магазина приложений PWA.  

## Предварительные условия  

*   Используйте [код Visual Studio][VisualstudioCodeMain] для редактирования ИСХОДНОГО кода PWA.  
*   Используйте [Node.js][NodejsMain] в качестве локального веб-сервера.  

## Создание простого веб-приложения  

Чтобы создать пустое веб-приложение, выполните действия, описанные в статье [генератор приложений для приложения Express][ExpressjsApplicationGenerator], и назовите свое приложение `MySamplePwa` .  

В командной строке выполните указанные ниже команды.  

```shell
npx express-generator --no-view
```  

```shell
npm install
```  

Команды создают пустое веб-приложение и устанавливают все зависимости.  

Теперь у вас есть простое функциональное веб-приложение.  Чтобы запустить веб-приложение, выполните следующую команду:  

```shell
npm start
```  

Теперь можно перейти к `http://localhost:3000` просмотру нового веб-приложения.  

:::image type="complex" source="./media/vs-nodejs-express-index.png" alt-text="Выполнение нового PWA на localhost" lightbox="./media/vs-nodejs-express-index.png":::
   Выполнение нового PWA на localhost
:::image-end:::

## Начало создания PWA  

Теперь, когда у вас есть простое веб-приложение, расширьте его как PWA, добавив три требования для PWAs<!--[3 requirements for PWAs][PwaEdgehtmlIndexRequirements]-->: [HTTPS](#step-1---use-https), [Манифест веб-приложения](#step-2---create-a-web-app-manifest)и [сотрудник службы](#step-3---add-a-service-worker).  

### Этап 1: использование HTTPS  

Ключевые части платформы PWA, например [работники служб][MDNServiceWorkerApi], требуют использования HTTPS.  Когда PWA разйдет в реальном времени, необходимо опубликовать его в URL-адресе HTTPS.  

В целях отладки Microsoft EDGE также допускает `http://localhost` Использование API PWA.  

[Опубликуйте веб-приложение как активный сайт][VisualStudioNodejsTutorialPublishAzureAppService], но убедитесь, что сервер НАСТРОЕН для HTTPS.  Например, вы можете создать [бесплатную учетную запись Azure][AzureCreateFreeAccount].  Разработайте сайт в [службе приложений Microsoft Azure][AzureWebApps] , и он по умолчанию обрабатывается по протоколу HTTPS.  

В следующем руководстве описано, `http://localhost` как выполнить СБОРКУ PWA.  

### Шаг 2: создание манифеста веб-приложения  

[Манифест веб-приложения][MDNWebAppManifest] — это файл в формате JSON, содержащий метаданные вашего приложения, такие как имя, описание, значки и т. д.  

Чтобы добавить в веб-приложение манифест приложения, выполните указанные ниже действия.  

1.  В коде Visual Studio выберите **File**  >  **Открыть папку** файл и выберите каталог, `MySamplePwa` созданный ранее.  
1.  Выберите, `Ctrl` + `N` чтобы создать новый файл, и вставьте следующий фрагмент кода.  
    
    ```json
    {
        "lang": "en-us",
        "name": "My Sample PWA",
        "short_name": "SamplePWA",
        "description": "A sample PWA for testing purposes",
        "start_url": "/",
        "background_color": "#2f3d58",
        "theme_color": "#2f3d58",        
        "orientation": "any",
        "display": "standalone",
        "icons": [
            {
                "src": "/icon512.png",
                "sizes": "512x512"
            }
        ]
    }
    ```  
    
1.  Сохраните файл как `/MySamplePwa/public/manifest.json` .  
1.  Добавление изображения значка приложения 512x512 с именем " `icon512.png` Кому" `/MySamplePwa/public/images` .  [Образец изображения][ImagePwa] можно использовать в целях тестирования.  
1.  В коде Visual Studio откройте `/public/index.html` и добавьте следующий фрагмент кода в `<head>` тег.  
    
    ```html
    <link rel="manifest" href="/manifest.json">
    ```   
    
### Шаг 3: Добавление сотрудника службы  

ИТ – это ключевая технология для PWAs, позволяющая выполнять сценарии, такие как поддержка в автономном режиме, дополнительное кэширование и выполнение фоновых задач, которые ранее были ограничены собственными приложениями.  

Служебные работники — это фоновые задачи, которые перехватывают сетевые запросы из вашего веб-приложения.  Работники служб пытаются выполнить задачи, даже если PWA не запущен.  Задачи включают указанные ниже действия.  

*   Обслуживание запрошенных ресурсов из кэша  
*   Отправка push-уведомлений  
*   Выполнение задач фоновой выборки  
*   Значки индикаторах событий  
*   и многое другое  

Служебные сотрудники определяются в специальном файле JavaScript.  Для получения дополнительных сведений перейдите к разделу [Использование рабочих процессов служб][MDNUsingServiceWorkers] и [API служб][MDNServiceWorkerApi].  

Чтобы создать сотрудника службы в проекте, используйте рецепт роли " **первый из кэша** " в [построителе PWA][PwaBuilderServiceWorker].  

1.  Перейдите к [pwabuilder.com/serviceworker][PwaBuilderServiceWorker], выберите сотрудника, который является **первым из кэша** , и нажмите кнопку **скачать** .  Загруженный файл включает следующие файлы:
    
    *   `pwabuilder-sw-register.js`  
    *   `pwabuilder-sw.js`  
    
1.  Скопируйте Скачанные файлы в `public` папку в проекте веб-приложения.  
    
1.  В коде Visual Studio откройте `/public/index.html` и добавьте следующий фрагмент кода в `<head>` тег.  
    
    ```html
    <script type="module" src="/pwabuilder-sw-register.js"></script>
    ```  
    
У вашего веб-приложения теперь есть сотрудник службы, использующий стратегию кэширования.  Новый сотрудник службы сначала извлекает ресурсы из кэша, а не из сети, по мере необходимости.  Кэшированные ресурсы включают изображения, JavaScript, CSS и HTML.

Выполните указанные ниже действия, чтобы подтвердить выполнение рабочего процесса службы.  

1.  Перейдите к веб-приложению с помощью `http://localhost:3000` .  Если веб-приложение недоступно, выполните следующую команду:   
    
    ```shell
    npm start
    ```
    
1.  В Microsoft Edge щелкните, `F12` чтобы открыть Microsoft Edge DevTools.  Выберите **приложение**, а затем — **сотрудники службы** , чтобы просмотреть сотрудников службы.  Если сотрудник службы не отображается, обновите страницу.  
     
    :::image type="complex" source="./media/devtools-sw-overview.png" alt-text="Выполнение нового PWA на localhost" lightbox="./media/devtools-sw-overview.png":::
       Общие сведения о рабочем процессе службы Microsoft Edge DevTools
    :::image-end:::
    
1.  Просмотрите кэш рабочих процессов службы, развернув **хранилище кэша** , и выберите **pwabuilder — предварительный кэш**.  Должны отобразиться все ресурсы, кэшируемые сотрудником службы.  Ресурсы, кэшируемые сотрудником службы, включают значок приложения, манифест приложения, CSS и файлы JavaScript.  
    
    :::image type="complex" source="./media/devtools-cache.png" alt-text="Выполнение нового PWA на localhost" lightbox="./media/devtools-cache.png":::
       Кэш рабочих процессов службы в Microsoft Edge DevTools (F12)
    :::image-end:::
    
1.  Попробуйте использование PWA в качестве автономного приложения.  В Microsoft Edge DevTools \ ( `F12` \) выберите **Network (сеть** ) и измените сетевой статус **Offline**на "не в сети". **Online**  
    
    :::image type="complex" source="./media/devtools-offline.png" alt-text="Выполнение нового PWA на localhost" lightbox="./media/devtools-offline.png":::
       Установка автономного режима приложения в Microsoft Edge DevTools
    :::image-end:::
    
1.  Обновите приложение, и оно должно отобразить механизм автономного режима для обслуживания ресурсов вашего приложения из кэша.  
    
    :::image type="complex" source="./media/vs-nodejs-express-index.png" alt-text="Выполнение нового PWA на localhost" lightbox="./media/vs-nodejs-express-index.png":::
       PWA работает в автономном режиме
    :::image-end:::
    
## Добавление push-уведомлений к PWA  

Вы можете создать PWAs, поддерживающий push-уведомления, выполнив указанные ниже действия.  

1.  Подписка на службу сообщений с помощью [API push-уведомлений][MDNPushApi]  
1.  Показывать всплывающее сообщение при получении сообщения от службы с помощью [API уведомлений][MDNNotificationsApi]  
    
Как и в случае с сотрудниками служб, API push-уведомлений являются API на основе стандартов.  API push-уведомлений работают в разных браузерах, поэтому ваш код должен работать везде, где поддерживаются PWAs.  Чтобы получить дополнительные сведения о том, как отправлять push-сообщения в другие браузеры на сервере, перейдите на [страницу веб-принудительно][NPMWebPush].  

Описанные ниже действия были адаптированы с помощью демона "Push-Cookbook" в [службе обслуживания сотрудников][ServiceWorkerCookbookPushRichDemo] , предоставляемой Mozilla, которая имеет ряд других полезных рецептов для отправки по Интернету и обслуживания рабочих процессов.  

### Шаг 1. Создание VAPIDных ключей  

Для отправки push-сообщений в клиент PWA требуется VAPID \ (код добровольного сервера приложений) с помощью извещающих уведомлений.  Доступно несколько VAPIDных генераторов ключей в Интернете (например, [vapidkeys.com][VapidkeysMain]\).  После создания необходимо получить объект JSON, содержащий открытый и закрытый ключи.  Сохраните клавиши для последующих шагов в следующем учебнике.  Сведения о VAPID и браузере VAPID можно найти, [отправив сообщение о том, что уведомления о событиях в службе push-уведомлений][MozillaServicesSendingVapidWebPushNotificationsPush]передаются по протоколу Mozilla.  

### Шаг 2: подписаться на push-уведомления  

Работники обслуживания обрабатывают события push-уведомлений и взаимодействие с всплывающими уведомлениями в PWA.  Чтобы оформить подписку на push-уведомления сервера PWA, убедитесь, что выполнены указанные ниже условия.  

*   Установленный, активный и регистрируемый PWA  
*   Код для завершения задачи подписки — в основном потоке пользовательского интерфейса PWA  
*   Вы подключены к сети  
    
Перед созданием новой принудительной подписки Microsoft Edge проверяет, предоставил ли пользователь разрешение на получение уведомлений в PWA.  В противном случае пользователю будет предложено разрешить браузеру.  Если разрешение закрыто, запрос `registration.pushManager.subscribe` генерирует исключение `DOMException` , которое должно быть обработано.  Дополнительные сведения об управлении разрешениями можно найти в [разделе push-уведомления в Microsoft Edge][WindowsBlogsWebNotificationsEdge].  

Добавьте в `pwabuilder-sw-register.js` файл следующий фрагмент кода.  

```javascript
// Ask the user for permission to send push notifications.
navigator.serviceWorker.ready
    .then(function (registration) {
        // Check if the user has an existing subscription
        return registration.pushManager.getSubscription()
            .then(function (subscription) {
                if (subscription) {
                    return subscription;
                }
                
                const vapidPublicKey = "PASTE YOUR PUBLIC VAPID KEY HERE";             
                return registration.pushManager.subscribe({
                    userVisibleOnly: true,
                    applicationServerKey: urlBase64ToUint8Array(vapidPublicKey)
                });
            });
    });

// Utility function for browser interoperability
function urlBase64ToUint8Array(base64String) {
    var padding = '='.repeat((4 - base64String.length % 4) % 4);
    var base64 = (base64String + padding)
        .replace(/\-/g, '+')
        .replace(/_/g, '/');
        
    var rawData = window.atob(base64);
    var outputArray = new Uint8Array(rawData.length);
    
    for (var i = 0; i < rawData.length; ++i) {
        outputArray[i] = rawData.charCodeAt(i);
    }
    return outputArray;
}
```  

Дополнительные сведения можно найти в разделе [PushManager][MDNPushManager] и [отправить по Интернету][NPMWebPushUsage].  

### Шаг 3: прослушивание push-уведомлений  

После того как вы создадите подписку в PWA, добавьте обработчики для сотрудника службы, чтобы реагировать на события push-уведомлений.  Push-уведомления отправляются с сервера для отображения всплывающих уведомлений.  Всплывающие уведомления отображают данные полученного сообщения.  Для выполнения следующих задач необходимо добавить обработчик нажатия.  

*   Закрыть всплывающее уведомление  
*   Открыть, сфокусировать или открыть и сфокусировать любые открытые окна  
*   Открытие нового окна и фокусирование для отображения страницы клиента PWA  
    
В `pwabuilder-sw.js` файле добавьте следующие обработчики.  

```javascript
// Respond to a server push with a user notification.
self.addEventListener('push', function (event) {
    if (Notification.permission === "granted") {
        const notificationText = event.data.text();
        const showNotification = self.registration.showNotification('Sample PWA', {
            body: notificationText,
            icon: 'images/icon512.png'
        });
        // Ensure the toast notification is displayed before exiting the function.
        event.waitUntil(showNotification);
    }
});

// Respond to the user selecting the toast notification.
self.addEventListener('notificationclick', function (event) {
    console.log('On notification click: ', event.notification.tag);
    event.notification.close();
    
    // This attempts to display the current notification if it is already open and then focuses on it.
    event.waitUntil(clients.matchAll({
        type: 'window'
    }).then(function (clientList) {
        for (var i = 0; i < clientList.length; i++) {
            var client = clientList[i];
            if (client.url == 'http://localhost:1337/' && 'focus' in client)
                return client.focus();
        }
        if (clients.openWindow)
            return clients.openWindow('/');
    }));
});
```  

### Шаг 4: попробуйте.  

Чтобы проверить push-уведомления для PWA, выполните указанные ниже действия.  

1.  Перейдите на веб – PWA по адресу `http://localhost:3000` .  Когда сотрудник службы активируется и пытается оформить подписку на PWA для push-уведомлений, Microsoft Edge предлагает вам разрешить просмотр уведомлений на PWA.  Нажмите кнопку **Разрешить**.  
    
    :::image type="complex" source="./media/notification-permission.png" alt-text="Выполнение нового PWA на localhost" lightbox="./media/notification-permission.png":::
       Диалоговое окно разрешений для включения уведомлений
    :::image-end:::
    
1.  Имитировать push-уведомление на стороне сервера.  Откройте веб – приложение Project Web App `http://localhost:3000` в браузере и нажмите кнопку, `F12` чтобы открыть DevTools.  Нажмите **кнопку**отправить,  >  **Service Worker**  >  **Push** чтобы отправить тестовое push-уведомление на PWA.  
    :::row:::
       :::column span="":::
          На панели задач должно отобразиться push-уведомление.  
          
          :::image type="complex" source="./media/devtools-push.png" alt-text="Выполнение нового PWA на localhost" lightbox="./media/devtools-push.png":::
             Отправка уведомления из DevTools  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          Если вы не выберете параметр \ (или активировать) всплывающее уведомление, система автоматически закрывает ее через несколько секунд и помещает ее в свой центр уведомлений Windows.  
          
          :::image type="complex" source="./media/windows-action-center.png" alt-text="Выполнение нового PWA на localhost" lightbox="./media/windows-action-center.png":::
             Уведомления в центре уведомлений Windows :::image-end:::
       :::column-end:::
    :::row-end:::  
    
## Дальнейшие действия  

Следующие действия включают дополнительные задачи, которые помогут вам разобраться в создании реальных PWAs.  

*   Управление принудительными подписками и их хранение  
*   [Шифрование][NPMWebPushEncrypt] полезных данных  
*   Адаптивный дизайн  
*   Глубокая связь  
*   [Тестирование в нескольких браузерах][BrowserStackTestEdgeBrowser]  
*   Реализация методов проверки и тестирования, таких как " [Подсказка][Webhint] "  
   
## См. также  

*   [Прогрессивные веб-приложения на MDN веб-документах][MDNProgressiveWebApps]  
*   [Прогрессивные веб-приложения на веб-сайте. dev][WebDevProgressiveWebApps]  
*   [Средства чтения новостей, такие как прогрессивные веб-приложения,][HackerNewsProgressiveWebApps] сравнивают различные платформы и шаблоны производительности для реализации примера \ (средство чтения новостей с помощью хакеров \) PWA.  
*   [Myth Busting PWAs][Davrous20191018MythBustingPwasNewEdgeEdition]  
*   [Прогрессивный план для последовательного веб-приложения][CloudfourThinksProgressiveRoadmapYourWebApp]  
*   [Автономные публикации с прогрессивными веб-приложениями][MediumWebEdgeOfflinePostsProgressiveWebApps]  
*   [PWA Q&A][AaronGustafsonNotebookPwaQa]  
*   [Ставкам в Интернете][JoretegBlogBettingWeb]  
*   [Именование последовательного веб-приложения][Fberriman20170626NamingProgressiveWebApps]  
*   [Проектирование и создание последовательного веб-приложения без структуры (часть 1)][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart1]  
*   [Проектирование и создание последовательного веб-приложения без структуры (часть 2)][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart2]  
*   [Проектирование и создание последовательного веб-приложения без структуры (часть 3)][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart3]  
    
<!-- image links -->  

[ImagePwa]: ./media/pwa.png  

<!-- links -->  

<!--[PwaEdgehtmlIndexRequirements]: ../progressive-web-apps-edgehtml/index.md#requirements "Requirements - Progressive Web Apps \(EdgeHTML\) on Windows | Microsoft Docs"  -->  

[VisualStudioNodejsTutorialPublishAzureAppService]: /azure/javascript/tutorial-vscode-azure-app-service-node-03 "Развертывание приложения Node.js в Azure с помощью Visual Studio Code | Документы Microsoft"  

[AzureCreateFreeAccount]: https://azure.microsoft.com/free "Создать бесплатную учетную запись Azure | Microsoft Azure"  
[AzureWebApps]: https://azure.microsoft.com/services/app-service/web "Веб-приложения | Microsoft Azure"  

[WindowsBlogsWebNotificationsEdge]: https://blogs.windows.com/msedgedev/2016/05/16/web-notifications-microsoft-edge#UAbvU2ymUlHO8EUV.97 "Веб-уведомления в Microsoft Edge | Блоги Windows"  

[VisualstudioCodeMain]: https://code.visualstudio.com "Код Visual Studio"  

[AaronGustafsonNotebookPwaQa]: https://www.aaron-gustafson.com/notebook/pwa-qa "PWA Q&A"  

[BrowserStackTestEdgeBrowser]: https://www.browserstack.com/test-on-microsoft-edge-browser "Бесплатное тестирование браузера Microsoft EDGE в Windows 10 | BrowserStack"  

[CloudfourThinksProgressiveRoadmapYourWebApp]: https://cloudfour.com/thinks/a-progressive-roadmap-for-your-progressive-web-app "Прогрессивный план для последовательного веб-приложения"  

[Davrous20191018MythBustingPwasNewEdgeEdition]: https://www.davrous.com/2019/10/18/myth-busting-pwas-the-new-edge-edition "Myth busting PWAs — новый выпуск Edge"  

[ExpressjsApplicationGenerator]: https://expressjs.com/starter/generator.html "Генератор приложений для Экспресс | Предоставлен" 

[Fberriman20170626NamingProgressiveWebApps]: https://fberriman.com/2017/06/26/naming-progressive-web-apps "Именование последовательного веб-приложения"  

[HackerNewsProgressiveWebApps]: https://hnpwa.com "Средства чтения новостей от хакеров в виде последовательного веб-приложения"  

[JoretegBlogBettingWeb]: https://joreteg.com/blog/betting-on-the-web "Ставкам в Интернете"  

[MDNDedicatedWorkerGlobalScopePostMessage]: https://developer.mozilla.org/docs/Web/API/
[MDNNotificationsApi]: https://developer.mozilla.org/docs/Web/API/Notifications_API "API уведомлений | MDN"  
[MDNProgressiveWebApps]: https://developer.mozilla.org/Apps/Progressive "Прогрессивные веб-приложения \ (PWAs) | MDN"  
[MDNPushApi]: https://developer.mozilla.org/docs/Web/API/Push_API "API push-уведомлений | MDN"  
[MDNPushManager]: https://developer.mozilla.org/docs/Web/API/PushManager "PushManager | MDN"  
[MDNServiceWorkerApi]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API "API рабочего процесса службы | MDN"  
[MDNUsingServiceWorkers]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API/Using_Service_Workers "Работа с сотрудниками службы | MDN"  
[MDNWebAppManifest]: https://developer.mozilla.org/docs/Web/Manifest "Манифест веб-приложения | MDN"  

[MediumWebEdgeOfflinePostsProgressiveWebApps]: https://medium.com/web-on-the-edge/offline-posts-with-progressive-web-apps-fc2dc4ad895 "Автономные публикации с прогрессивными веб-приложениями"  

[MozillaServicesSendingVapidWebPushNotificationsPush]: https://blog.mozilla.org/services/2016/08/23/sending-vapid-identified-webpush-notifications-via-mozillas-push-service "Отправка VAPID идентифицированных уведомлений о событиях через службу Push-сообщений для Mozilla | Службы Mozilla"  

[NodejsMain]: https://nodejs.org "Node.js"  

[NPMWebPush]: https://www.npmjs.com/package/web-push "веб-отправка | NPM"  
[NPMWebPushEncrypt]: https://www.npmjs.com/package/web-push#encryptuserpublickey-userauth-payload-contentencoding "Encrypt (userPublicKey, userAuth, полезные данные, contentEncoding) — веб-отправка | NPM"  
[NPMWebPushUsage]: https://www.npmjs.com/package/web-push#usage "Использование-веб-Push | NPM"  

[ProgressiveWebApps]: https://pwa.rocks "Прогрессивные веб-приложения"  

[PwaBuilder]: https://www.pwabuilder.com "Конструктор PWA"  
[PwaBuilderServiceWorker]: https://www.pwabuilder.com/serviceworker "Сервисный сотрудник | Конструктор PWA"  

[ServiceWorkerCookbookPushRichDemo]: https://serviceworke.rs/push-rich_demo.html "Push-ролик с богатыми возможностями | ServiceWorker Cookbook"  

[Smashingmagazine201907ProgressiveWebApplicationFrameworkPart1]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-1 "Проектирование и создание последовательного веб-приложения без структуры (часть 1)"  

[Smashingmagazine201907ProgressiveWebApplicationFrameworkPart2]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-2 "Проектирование и создание последовательного веб-приложения без структуры (часть 2)"  

[Smashingmagazine201907ProgressiveWebApplicationFrameworkPart3]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-3 "Проектирование и создание последовательного веб-приложения без структуры (часть 3)"  

[VapidkeysMain]: https://vapidkeys.com "VAPID Secure Key | VapidKeys" 

[Webhint]: https://webhint.io "Подсказка"  

[WebDevProgressiveWebApps]: https://developers.google.com/web/progressive-web-apps "Прогрессивные веб-приложения | Web. dev"  

[WikiProgressiveEnhancement]: https://en.wikipedia.org/wiki/Progressive_enhancement "Улучшенное последовательное расширение | Википедии"  
