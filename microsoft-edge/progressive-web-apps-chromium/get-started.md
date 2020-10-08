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
# <span data-ttu-id="7c529-104">Приступая к работе с прогрессивными веб-приложениями (Chromium)</span><span class="sxs-lookup"><span data-stu-id="7c529-104">Get started with Progressive Web Apps (Chromium)</span></span>  

<span data-ttu-id="7c529-105">Прогрессивные веб-приложения \ (PWAs \) — это веб-приложения, которые являются [последовательно улучшенными][WikiProgressiveEnhancement].</span><span class="sxs-lookup"><span data-stu-id="7c529-105">Progressive Web Apps \(PWAs\) are web apps that are [progressively enhanced][WikiProgressiveEnhancement].</span></span>  <span data-ttu-id="7c529-106">Улучшенные возможности, такие как установка, Автономная поддержка и Push-уведомления, включают в себя подобные функции приложения.</span><span class="sxs-lookup"><span data-stu-id="7c529-106">The progressive enhancements include app-like features, such as installation, offline support, and push notifications.</span></span>  <span data-ttu-id="7c529-107">Кроме того, вы можете упаковать веб – приложение PWA для магазинов приложений.</span><span class="sxs-lookup"><span data-stu-id="7c529-107">You may also package your PWA for app stores.</span></span>  <span data-ttu-id="7c529-108">Возможно, в магазинах приложений есть магазин Microsoft Store, Google Play, Mac App Store и многое другое.</span><span class="sxs-lookup"><span data-stu-id="7c529-108">Possible app stores include the Microsoft Store, Google Play, Mac App Store, and more.</span></span>  <span data-ttu-id="7c529-109">Microsoft Store — это коммерческое приложение, встроенное в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="7c529-109">The Microsoft Store is the commercial app store built into Windows 10.</span></span>  

<span data-ttu-id="7c529-110">В приведенном ниже руководстве представлен обзор основ PWA, создание простого веб-приложения и расширение его как PWA.</span><span class="sxs-lookup"><span data-stu-id="7c529-110">The following guide gives you an overview of PWA basics by creating a simple web app and extending it as a PWA.</span></span>  <span data-ttu-id="7c529-111">Готовый проект работает в современных браузерах.</span><span class="sxs-lookup"><span data-stu-id="7c529-111">The finished project works across modern browsers.</span></span>  

> [!TIP]
> <span data-ttu-id="7c529-112">Вы можете использовать [PWABuilder][PwaBuilder] для создания нового PWA, улучшения существующего веб-приложения PWA или упаковки для магазина приложений PWA.</span><span class="sxs-lookup"><span data-stu-id="7c529-112">You may use [PWABuilder][PwaBuilder] to create a new PWA, enhance your existing PWA, or package your PWA for app stores.</span></span>  

## <span data-ttu-id="7c529-113">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="7c529-113">Prerequisites</span></span>  

*   <span data-ttu-id="7c529-114">Используйте [код Visual Studio][VisualstudioCodeMain] для редактирования ИСХОДНОГО кода PWA.</span><span class="sxs-lookup"><span data-stu-id="7c529-114">Use [Visual Studio Code][VisualstudioCodeMain] to edit your PWA source code.</span></span>  
*   <span data-ttu-id="7c529-115">Используйте [Node.js][NodejsMain] в качестве локального веб-сервера.</span><span class="sxs-lookup"><span data-stu-id="7c529-115">Use [Node.js][NodejsMain] as your local web server.</span></span>  

## <span data-ttu-id="7c529-116">Создание простого веб-приложения</span><span class="sxs-lookup"><span data-stu-id="7c529-116">Create a basic web app</span></span>  

<span data-ttu-id="7c529-117">Чтобы создать пустое веб-приложение, выполните действия, описанные в статье [генератор приложений для приложения Express][ExpressjsApplicationGenerator], и назовите свое приложение `MySamplePwa` .</span><span class="sxs-lookup"><span data-stu-id="7c529-117">To create an empty web app, follow the steps in [Node Express App Generator][ExpressjsApplicationGenerator], and name your app `MySamplePwa`.</span></span>  

<span data-ttu-id="7c529-118">В командной строке выполните указанные ниже команды.</span><span class="sxs-lookup"><span data-stu-id="7c529-118">In the prompt, run the following commands.</span></span>  

```shell
npx express-generator --no-view
```  

```shell
npm install
```  

<span data-ttu-id="7c529-119">Команды создают пустое веб-приложение и устанавливают все зависимости.</span><span class="sxs-lookup"><span data-stu-id="7c529-119">The commands create an empty web app and install any dependencies.</span></span>  

<span data-ttu-id="7c529-120">Теперь у вас есть простое функциональное веб-приложение.</span><span class="sxs-lookup"><span data-stu-id="7c529-120">You now have a simple, functional web app.</span></span>  <span data-ttu-id="7c529-121">Чтобы запустить веб-приложение, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="7c529-121">To start your web app, run the following command.</span></span>  

```shell
npm start
```  

<span data-ttu-id="7c529-122">Теперь можно перейти к `http://localhost:3000` просмотру нового веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="7c529-122">Now browse to `http://localhost:3000` to view your new web app.</span></span>  

:::image type="complex" source="./media/vs-nodejs-express-index.png" alt-text="Выполнение нового PWA на localhost" lightbox="./media/vs-nodejs-express-index.png":::
   <span data-ttu-id="7c529-124">Выполнение нового PWA на localhost</span><span class="sxs-lookup"><span data-stu-id="7c529-124">Running your new PWA on localhost</span></span>
:::image-end:::

## <span data-ttu-id="7c529-125">Начало создания PWA</span><span class="sxs-lookup"><span data-stu-id="7c529-125">Get started building a PWA</span></span>  

<span data-ttu-id="7c529-126">Теперь, когда у вас есть простое веб-приложение, расширьте его как PWA, добавив три требования для PWAs</span><span class="sxs-lookup"><span data-stu-id="7c529-126">Now that you have a simple web app, extend it as a PWA by adding the three requirements for PWAs</span></span><!--[3 requirements for PWAs][PwaEdgehtmlIndexRequirements]--><span data-ttu-id="7c529-127">: [HTTPS](#step-1---use-https), [Манифест веб-приложения](#step-2---create-a-web-app-manifest)и [сотрудник службы](#step-3---add-a-service-worker).</span><span class="sxs-lookup"><span data-stu-id="7c529-127">: [HTTPS](#step-1---use-https), a [Web App Manifest](#step-2---create-a-web-app-manifest), and a [Service Worker](#step-3---add-a-service-worker).</span></span>  

### <span data-ttu-id="7c529-128">Этап 1: использование HTTPS</span><span class="sxs-lookup"><span data-stu-id="7c529-128">Step 1 - Use HTTPS</span></span>  

<span data-ttu-id="7c529-129">Ключевые части платформы PWA, например [работники служб][MDNServiceWorkerApi], требуют использования HTTPS.</span><span class="sxs-lookup"><span data-stu-id="7c529-129">Key parts of the PWA platform, such as [Service Workers][MDNServiceWorkerApi], require the use of HTTPS.</span></span>  <span data-ttu-id="7c529-130">Когда PWA разйдет в реальном времени, необходимо опубликовать его в URL-адресе HTTPS.</span><span class="sxs-lookup"><span data-stu-id="7c529-130">When your PWA goes live, you must publish it to an HTTPS URL.</span></span>  

<span data-ttu-id="7c529-131">В целях отладки Microsoft EDGE также допускает `http://localhost` Использование API PWA.</span><span class="sxs-lookup"><span data-stu-id="7c529-131">For debugging purposes, Microsoft Edge also permits `http://localhost` to use the PWA APIs.</span></span>  

<span data-ttu-id="7c529-132">[Опубликуйте веб-приложение как активный сайт][VisualStudioNodejsTutorialPublishAzureAppService], но убедитесь, что сервер НАСТРОЕН для HTTPS.</span><span class="sxs-lookup"><span data-stu-id="7c529-132">[Publish your web app as a live site][VisualStudioNodejsTutorialPublishAzureAppService], but ensure your server is configured for HTTPS.</span></span>  <span data-ttu-id="7c529-133">Например, вы можете создать [бесплатную учетную запись Azure][AzureCreateFreeAccount].</span><span class="sxs-lookup"><span data-stu-id="7c529-133">For example, you may create an [Azure free account][AzureCreateFreeAccount].</span></span>  <span data-ttu-id="7c529-134">Разработайте сайт в [службе приложений Microsoft Azure][AzureWebApps] , и он по умолчанию обрабатывается по протоколу HTTPS.</span><span class="sxs-lookup"><span data-stu-id="7c529-134">Host your site on the [Microsoft Azure App Service][AzureWebApps] and it is served over HTTPS by default.</span></span>  

<span data-ttu-id="7c529-135">В следующем руководстве описано, `http://localhost` как выполнить СБОРКУ PWA.</span><span class="sxs-lookup"><span data-stu-id="7c529-135">The following guide, use `http://localhost` to build your PWA.</span></span>  

### <span data-ttu-id="7c529-136">Шаг 2: создание манифеста веб-приложения</span><span class="sxs-lookup"><span data-stu-id="7c529-136">Step 2 - Create a Web App Manifest</span></span>  

<span data-ttu-id="7c529-137">[Манифест веб-приложения][MDNWebAppManifest] — это файл в формате JSON, содержащий метаданные вашего приложения, такие как имя, описание, значки и т. д.</span><span class="sxs-lookup"><span data-stu-id="7c529-137">A [Web App Manifest][MDNWebAppManifest] is a JSON file containing metadata about your app, such as name, description, icons, and more.</span></span>  

<span data-ttu-id="7c529-138">Чтобы добавить в веб-приложение манифест приложения, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="7c529-138">To add an app manifest to the web app:</span></span>  

1.  <span data-ttu-id="7c529-139">В коде Visual Studio выберите **File**  >  **Открыть папку** файл и выберите каталог, `MySamplePwa` созданный ранее.</span><span class="sxs-lookup"><span data-stu-id="7c529-139">In Visual Studio Code, choose **File** > **Open Folder** and choose the `MySamplePwa` directory you created earlier.</span></span>  
1.  <span data-ttu-id="7c529-140">Выберите, `Ctrl` + `N` чтобы создать новый файл, и вставьте следующий фрагмент кода.</span><span class="sxs-lookup"><span data-stu-id="7c529-140">Select `Ctrl`+`N` to create a new file, and paste in the following code snippet.</span></span>  
    
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
    
1.  <span data-ttu-id="7c529-141">Сохраните файл как `/MySamplePwa/public/manifest.json` .</span><span class="sxs-lookup"><span data-stu-id="7c529-141">Save the file as `/MySamplePwa/public/manifest.json`.</span></span>  
1.  <span data-ttu-id="7c529-142">Добавление изображения значка приложения 512x512 с именем " `icon512.png` Кому" `/MySamplePwa/public/images` .</span><span class="sxs-lookup"><span data-stu-id="7c529-142">Add a 512x512 app icon image named `icon512.png` to `/MySamplePwa/public/images`.</span></span>  <span data-ttu-id="7c529-143">[Образец изображения][ImagePwa] можно использовать в целях тестирования.</span><span class="sxs-lookup"><span data-stu-id="7c529-143">You may use the [sample image][ImagePwa] for testing purposes.</span></span>  
1.  <span data-ttu-id="7c529-144">В коде Visual Studio откройте `/public/index.html` и добавьте следующий фрагмент кода в `<head>` тег.</span><span class="sxs-lookup"><span data-stu-id="7c529-144">In Visual Studio Code, open `/public/index.html`, and add the following code snippet inside the `<head>` tag.</span></span>  
    
    ```html
    <link rel="manifest" href="/manifest.json">
    ```   
    
### <span data-ttu-id="7c529-145">Шаг 3: Добавление сотрудника службы</span><span class="sxs-lookup"><span data-stu-id="7c529-145">Step 3 - Add a Service Worker</span></span>  

<span data-ttu-id="7c529-146">ИТ – это ключевая технология для PWAs, позволяющая выполнять сценарии, такие как поддержка в автономном режиме, дополнительное кэширование и выполнение фоновых задач, которые ранее были ограничены собственными приложениями.</span><span class="sxs-lookup"><span data-stu-id="7c529-146">Service workers are the key technology behind PWAs, enabling scenarios like offline support, advanced caching, and running background tasks previously limited to native apps.</span></span>  

<span data-ttu-id="7c529-147">Служебные работники — это фоновые задачи, которые перехватывают сетевые запросы из вашего веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="7c529-147">Service workers are background tasks that intercept network requests from your web app.</span></span>  <span data-ttu-id="7c529-148">Работники служб пытаются выполнить задачи, даже если PWA не запущен.</span><span class="sxs-lookup"><span data-stu-id="7c529-148">Service workers attempt to complete tasks, even when your PWA is not running.</span></span>  <span data-ttu-id="7c529-149">Задачи включают указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="7c529-149">Tasks include the following actions.</span></span>  

*   <span data-ttu-id="7c529-150">Обслуживание запрошенных ресурсов из кэша</span><span class="sxs-lookup"><span data-stu-id="7c529-150">Serving requested resources from a cache</span></span>  
*   <span data-ttu-id="7c529-151">Отправка push-уведомлений</span><span class="sxs-lookup"><span data-stu-id="7c529-151">Sending push notifications</span></span>  
*   <span data-ttu-id="7c529-152">Выполнение задач фоновой выборки</span><span class="sxs-lookup"><span data-stu-id="7c529-152">Running background fetch tasks</span></span>  
*   <span data-ttu-id="7c529-153">Значки индикаторах событий</span><span class="sxs-lookup"><span data-stu-id="7c529-153">Badging icons</span></span>  
*   <span data-ttu-id="7c529-154">и многое другое</span><span class="sxs-lookup"><span data-stu-id="7c529-154">and more</span></span>  

<span data-ttu-id="7c529-155">Служебные сотрудники определяются в специальном файле JavaScript.</span><span class="sxs-lookup"><span data-stu-id="7c529-155">Service workers are defined in a special JavaScript file.</span></span>  <span data-ttu-id="7c529-156">Для получения дополнительных сведений перейдите к разделу [Использование рабочих процессов служб][MDNUsingServiceWorkers] и [API служб][MDNServiceWorkerApi].</span><span class="sxs-lookup"><span data-stu-id="7c529-156">For more information, navigate to [Using Service Workers][MDNUsingServiceWorkers] and [Service Worker API][MDNServiceWorkerApi].</span></span>  

<span data-ttu-id="7c529-157">Чтобы создать сотрудника службы в проекте, используйте рецепт роли " **первый из кэша** " в [построителе PWA][PwaBuilderServiceWorker].</span><span class="sxs-lookup"><span data-stu-id="7c529-157">To build a service worker in your project, use the **Cache-first network** service worker recipe from [PWA Builder][PwaBuilderServiceWorker].</span></span>  

1.  <span data-ttu-id="7c529-158">Перейдите к [pwabuilder.com/serviceworker][PwaBuilderServiceWorker], выберите сотрудника, который является **первым из кэша** , и нажмите кнопку **скачать** .</span><span class="sxs-lookup"><span data-stu-id="7c529-158">Navigate to [pwabuilder.com/serviceworker][PwaBuilderServiceWorker], select the **Cache-first network** service worker, and select the **Download** button.</span></span>  <span data-ttu-id="7c529-159">Загруженный файл включает следующие файлы:</span><span class="sxs-lookup"><span data-stu-id="7c529-159">The downloaded file contains the following files:</span></span>
    
    *   `pwabuilder-sw-register.js`  
    *   `pwabuilder-sw.js`  
    
1.  <span data-ttu-id="7c529-160">Скопируйте Скачанные файлы в `public` папку в проекте веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="7c529-160">Copy the downloaded files to the `public` folder in your web app project.</span></span>  
    
1.  <span data-ttu-id="7c529-161">В коде Visual Studio откройте `/public/index.html` и добавьте следующий фрагмент кода в `<head>` тег.</span><span class="sxs-lookup"><span data-stu-id="7c529-161">In Visual Studio Code, open `/public/index.html` and add the following code snippet inside the `<head>` tag.</span></span>  
    
    ```html
    <script type="module" src="/pwabuilder-sw-register.js"></script>
    ```  
    
<span data-ttu-id="7c529-162">У вашего веб-приложения теперь есть сотрудник службы, использующий стратегию кэширования.</span><span class="sxs-lookup"><span data-stu-id="7c529-162">Your web app now has a service worker that uses the cache-first strategy.</span></span>  <span data-ttu-id="7c529-163">Новый сотрудник службы сначала извлекает ресурсы из кэша, а не из сети, по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="7c529-163">You new service worker fetches resources from the cache first, and from the network only as needed.</span></span>  <span data-ttu-id="7c529-164">Кэшированные ресурсы включают изображения, JavaScript, CSS и HTML.</span><span class="sxs-lookup"><span data-stu-id="7c529-164">Cached resources include images, JavaScript, CSS, and HTML.</span></span>

<span data-ttu-id="7c529-165">Выполните указанные ниже действия, чтобы подтвердить выполнение рабочего процесса службы.</span><span class="sxs-lookup"><span data-stu-id="7c529-165">Use the following steps to confirm that your service worker runs.</span></span>  

1.  <span data-ttu-id="7c529-166">Перейдите к веб-приложению с помощью `http://localhost:3000` .</span><span class="sxs-lookup"><span data-stu-id="7c529-166">Navigate to your web app using `http://localhost:3000`.</span></span>  <span data-ttu-id="7c529-167">Если веб-приложение недоступно, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="7c529-167">If your web app is not available, run the following command.</span></span>   
    
    ```shell
    npm start
    ```
    
1.  <span data-ttu-id="7c529-168">В Microsoft Edge щелкните, `F12` чтобы открыть Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="7c529-168">In Microsoft Edge, select `F12` to open the Microsoft Edge DevTools.</span></span>  <span data-ttu-id="7c529-169">Выберите **приложение**, а затем — **сотрудники службы** , чтобы просмотреть сотрудников службы.</span><span class="sxs-lookup"><span data-stu-id="7c529-169">Select **Application**, then **Service Workers** to view the service workers.</span></span>  <span data-ttu-id="7c529-170">Если сотрудник службы не отображается, обновите страницу.</span><span class="sxs-lookup"><span data-stu-id="7c529-170">If the service worker is not displayed, refresh the page.</span></span>  
     
    :::image type="complex" source="./media/devtools-sw-overview.png" alt-text="Выполнение нового PWA на localhost" lightbox="./media/devtools-sw-overview.png":::
       <span data-ttu-id="7c529-172">Общие сведения о рабочем процессе службы Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="7c529-172">Microsoft Edge DevTools Service Worker overview</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="7c529-173">Просмотрите кэш рабочих процессов службы, развернув **хранилище кэша** , и выберите **pwabuilder — предварительный кэш**.</span><span class="sxs-lookup"><span data-stu-id="7c529-173">View the service worker cache by expanding **Cache Storage** and select **pwabuilder-precache**.</span></span>  <span data-ttu-id="7c529-174">Должны отобразиться все ресурсы, кэшируемые сотрудником службы.</span><span class="sxs-lookup"><span data-stu-id="7c529-174">All of the resources cached by the service worker should be displayed.</span></span>  <span data-ttu-id="7c529-175">Ресурсы, кэшируемые сотрудником службы, включают значок приложения, манифест приложения, CSS и файлы JavaScript.</span><span class="sxs-lookup"><span data-stu-id="7c529-175">The resources cached by the service worker include the app icon, app manifest, CSS, and JavaScript files.</span></span>  
    
    :::image type="complex" source="./media/devtools-cache.png" alt-text="Выполнение нового PWA на localhost" lightbox="./media/devtools-cache.png":::
       <span data-ttu-id="7c529-177">Кэш рабочих процессов службы в Microsoft Edge DevTools (F12)</span><span class="sxs-lookup"><span data-stu-id="7c529-177">Service Worker cache in Microsoft Edge DevTools (F12)</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="7c529-178">Попробуйте использование PWA в качестве автономного приложения.</span><span class="sxs-lookup"><span data-stu-id="7c529-178">Try your PWA as an offline app.</span></span>  <span data-ttu-id="7c529-179">В Microsoft Edge DevTools \ ( `F12` \) выберите **Network (сеть** ) и измените сетевой статус **Offline**на "не в сети". **Online**</span><span class="sxs-lookup"><span data-stu-id="7c529-179">In Microsoft Edge DevTools \(`F12`\), choose **Network** then change the **Online** status to **Offline**.</span></span>  
    
    :::image type="complex" source="./media/devtools-offline.png" alt-text="Выполнение нового PWA на localhost" lightbox="./media/devtools-offline.png":::
       <span data-ttu-id="7c529-181">Установка автономного режима приложения в Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="7c529-181">Setting app to offline mode in Microsoft Edge DevTools</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="7c529-182">Обновите приложение, и оно должно отобразить механизм автономного режима для обслуживания ресурсов вашего приложения из кэша.</span><span class="sxs-lookup"><span data-stu-id="7c529-182">Refresh your app and it should display the offline mechanism for serving the resources of your app from the cache.</span></span>  
    
    :::image type="complex" source="./media/vs-nodejs-express-index.png" alt-text="Выполнение нового PWA на localhost" lightbox="./media/vs-nodejs-express-index.png":::
       <span data-ttu-id="7c529-184">PWA работает в автономном режиме</span><span class="sxs-lookup"><span data-stu-id="7c529-184">PWA running offline</span></span>
    :::image-end:::
    
## <span data-ttu-id="7c529-185">Добавление push-уведомлений к PWA</span><span class="sxs-lookup"><span data-stu-id="7c529-185">Add push notifications to your PWA</span></span>  

<span data-ttu-id="7c529-186">Вы можете создать PWAs, поддерживающий push-уведомления, выполнив указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="7c529-186">You may create PWAs that support push notifications by completing the following tasks.</span></span>  

1.  <span data-ttu-id="7c529-187">Подписка на службу сообщений с помощью [API push-уведомлений][MDNPushApi]</span><span class="sxs-lookup"><span data-stu-id="7c529-187">Subscribe to a messaging service using the [Push API][MDNPushApi]</span></span>  
1.  <span data-ttu-id="7c529-188">Показывать всплывающее сообщение при получении сообщения от службы с помощью [API уведомлений][MDNNotificationsApi]</span><span class="sxs-lookup"><span data-stu-id="7c529-188">Display a toast message when a message is received from the service using the [Notifications API][MDNNotificationsApi]</span></span>  
    
<span data-ttu-id="7c529-189">Как и в случае с сотрудниками служб, API push-уведомлений являются API на основе стандартов.</span><span class="sxs-lookup"><span data-stu-id="7c529-189">Just like with Service Workers, the push notification APIs are standards-based APIs.</span></span>  <span data-ttu-id="7c529-190">API push-уведомлений работают в разных браузерах, поэтому ваш код должен работать везде, где поддерживаются PWAs.</span><span class="sxs-lookup"><span data-stu-id="7c529-190">The push notification APIs work across browsers, so your code should work everywhere that PWAs are supported.</span></span>  <span data-ttu-id="7c529-191">Чтобы получить дополнительные сведения о том, как отправлять push-сообщения в другие браузеры на сервере, перейдите на [страницу веб-принудительно][NPMWebPush].</span><span class="sxs-lookup"><span data-stu-id="7c529-191">For more information about delivering push messages to different browsers on your server, navigate to [Web-Push][NPMWebPush].</span></span>  

<span data-ttu-id="7c529-192">Описанные ниже действия были адаптированы с помощью демона "Push-Cookbook" в [службе обслуживания сотрудников][ServiceWorkerCookbookPushRichDemo] , предоставляемой Mozilla, которая имеет ряд других полезных рецептов для отправки по Интернету и обслуживания рабочих процессов.</span><span class="sxs-lookup"><span data-stu-id="7c529-192">The following steps have been adapted from the Push Rich Demo in [Service Worker Cookbook][ServiceWorkerCookbookPushRichDemo] provided by Mozilla, which has a number of other useful Web Push and service worker recipes.</span></span>  

### <span data-ttu-id="7c529-193">Шаг 1. Создание VAPIDных ключей</span><span class="sxs-lookup"><span data-stu-id="7c529-193">Step 1 - Generate VAPID keys</span></span>  

<span data-ttu-id="7c529-194">Для отправки push-сообщений в клиент PWA требуется VAPID \ (код добровольного сервера приложений) с помощью извещающих уведомлений.</span><span class="sxs-lookup"><span data-stu-id="7c529-194">Push notifications require VAPID \(Voluntary Application Server Identification\) keys in order to send push messages to the PWA client.</span></span>  <span data-ttu-id="7c529-195">Доступно несколько VAPIDных генераторов ключей в Интернете (например, [vapidkeys.com][VapidkeysMain]\).</span><span class="sxs-lookup"><span data-stu-id="7c529-195">There are several VAPID key generators available online \(for example, [vapidkeys.com][VapidkeysMain]\).</span></span>  <span data-ttu-id="7c529-196">После создания необходимо получить объект JSON, содержащий открытый и закрытый ключи.</span><span class="sxs-lookup"><span data-stu-id="7c529-196">After generation, you should get a JSON object containing a public and private key.</span></span>  <span data-ttu-id="7c529-197">Сохраните клавиши для последующих шагов в следующем учебнике.</span><span class="sxs-lookup"><span data-stu-id="7c529-197">Save the keys for later steps in the following tutorial.</span></span>  <span data-ttu-id="7c529-198">Сведения о VAPID и браузере VAPID можно найти, [отправив сообщение о том, что уведомления о событиях в службе push-уведомлений][MozillaServicesSendingVapidWebPushNotificationsPush]передаются по протоколу Mozilla.</span><span class="sxs-lookup"><span data-stu-id="7c529-198">For information about VAPID and WebPush, navigate to [Sending VAPID identified WebPush Notifications using the Mozilla Push Service][MozillaServicesSendingVapidWebPushNotificationsPush].</span></span>  

### <span data-ttu-id="7c529-199">Шаг 2: подписаться на push-уведомления</span><span class="sxs-lookup"><span data-stu-id="7c529-199">Step 2 - Subscribe to push notifications</span></span>  

<span data-ttu-id="7c529-200">Работники обслуживания обрабатывают события push-уведомлений и взаимодействие с всплывающими уведомлениями в PWA.</span><span class="sxs-lookup"><span data-stu-id="7c529-200">Service workers handle push events and toast notification interactions in your PWA.</span></span>  <span data-ttu-id="7c529-201">Чтобы оформить подписку на push-уведомления сервера PWA, убедитесь, что выполнены указанные ниже условия.</span><span class="sxs-lookup"><span data-stu-id="7c529-201">To subscribe the PWA to server push notifications, ensure the following conditions are met.</span></span>  

*   <span data-ttu-id="7c529-202">Установленный, активный и регистрируемый PWA</span><span class="sxs-lookup"><span data-stu-id="7c529-202">Your PWA is installed, active, and registered</span></span>  
*   <span data-ttu-id="7c529-203">Код для завершения задачи подписки — в основном потоке пользовательского интерфейса PWA</span><span class="sxs-lookup"><span data-stu-id="7c529-203">Your code to complete the subscription task is on the main UI thread of the PWA</span></span>  
*   <span data-ttu-id="7c529-204">Вы подключены к сети</span><span class="sxs-lookup"><span data-stu-id="7c529-204">You have network connectivity</span></span>  
    
<span data-ttu-id="7c529-205">Перед созданием новой принудительной подписки Microsoft Edge проверяет, предоставил ли пользователь разрешение на получение уведомлений в PWA.</span><span class="sxs-lookup"><span data-stu-id="7c529-205">Before a new push subscription is created, Microsoft Edge verifies if the user granted the PWA permission to receive notifications.</span></span>  <span data-ttu-id="7c529-206">В противном случае пользователю будет предложено разрешить браузеру.</span><span class="sxs-lookup"><span data-stu-id="7c529-206">If not, the user is prompted by the browser for permission.</span></span>  <span data-ttu-id="7c529-207">Если разрешение закрыто, запрос `registration.pushManager.subscribe` генерирует исключение `DOMException` , которое должно быть обработано.</span><span class="sxs-lookup"><span data-stu-id="7c529-207">If the permission is denied, the request to `registration.pushManager.subscribe` throws a `DOMException`, which must be handled.</span></span>  <span data-ttu-id="7c529-208">Дополнительные сведения об управлении разрешениями можно найти в [разделе push-уведомления в Microsoft Edge][WindowsBlogsWebNotificationsEdge].</span><span class="sxs-lookup"><span data-stu-id="7c529-208">For more on permission management, navigate to [Push Notifications in Microsoft Edge][WindowsBlogsWebNotificationsEdge].</span></span>  

<span data-ttu-id="7c529-209">Добавьте в `pwabuilder-sw-register.js` файл следующий фрагмент кода.</span><span class="sxs-lookup"><span data-stu-id="7c529-209">In your `pwabuilder-sw-register.js` file, append the following code snippet.</span></span>  

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

<span data-ttu-id="7c529-210">Дополнительные сведения можно найти в разделе [PushManager][MDNPushManager] и [отправить по Интернету][NPMWebPushUsage].</span><span class="sxs-lookup"><span data-stu-id="7c529-210">For more information, navigate to [PushManager][MDNPushManager] and [Web-Push][NPMWebPushUsage].</span></span>  

### <span data-ttu-id="7c529-211">Шаг 3: прослушивание push-уведомлений</span><span class="sxs-lookup"><span data-stu-id="7c529-211">Step 3 - Listen for push notifications</span></span>  

<span data-ttu-id="7c529-212">После того как вы создадите подписку в PWA, добавьте обработчики для сотрудника службы, чтобы реагировать на события push-уведомлений.</span><span class="sxs-lookup"><span data-stu-id="7c529-212">After a subscription is created in your PWA, add handlers to the service worker to respond to push events.</span></span>  <span data-ttu-id="7c529-213">Push-уведомления отправляются с сервера для отображения всплывающих уведомлений.</span><span class="sxs-lookup"><span data-stu-id="7c529-213">Push event are sent from the server to display toast notifications.</span></span>  <span data-ttu-id="7c529-214">Всплывающие уведомления отображают данные полученного сообщения.</span><span class="sxs-lookup"><span data-stu-id="7c529-214">Toast notifications display data for a received message.</span></span>  <span data-ttu-id="7c529-215">Для выполнения следующих задач необходимо добавить обработчик нажатия.</span><span class="sxs-lookup"><span data-stu-id="7c529-215">To complete the following tasks, you must add a click handler.</span></span>  

*   <span data-ttu-id="7c529-216">Закрыть всплывающее уведомление</span><span class="sxs-lookup"><span data-stu-id="7c529-216">Dismiss the toast notification</span></span>  
*   <span data-ttu-id="7c529-217">Открыть, сфокусировать или открыть и сфокусировать любые открытые окна</span><span class="sxs-lookup"><span data-stu-id="7c529-217">Open, focus, or open and focus any open windows</span></span>  
*   <span data-ttu-id="7c529-218">Открытие нового окна и фокусирование для отображения страницы клиента PWA</span><span class="sxs-lookup"><span data-stu-id="7c529-218">Open and focus a new window to display a PWA client page</span></span>  
    
<span data-ttu-id="7c529-219">В `pwabuilder-sw.js` файле добавьте следующие обработчики.</span><span class="sxs-lookup"><span data-stu-id="7c529-219">In your `pwabuilder-sw.js` file, add the following handlers.</span></span>  

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

### <span data-ttu-id="7c529-220">Шаг 4: попробуйте.</span><span class="sxs-lookup"><span data-stu-id="7c529-220">Step 4 - Try it out</span></span>  

<span data-ttu-id="7c529-221">Чтобы проверить push-уведомления для PWA, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="7c529-221">To test push notifications for your PWA, complete the following steps.</span></span>  

1.  <span data-ttu-id="7c529-222">Перейдите на веб – PWA по адресу `http://localhost:3000` .</span><span class="sxs-lookup"><span data-stu-id="7c529-222">Navigate to your PWA at `http://localhost:3000`.</span></span>  <span data-ttu-id="7c529-223">Когда сотрудник службы активируется и пытается оформить подписку на PWA для push-уведомлений, Microsoft Edge предлагает вам разрешить просмотр уведомлений на PWA.</span><span class="sxs-lookup"><span data-stu-id="7c529-223">When your service worker activates and attempts to subscribe your PWA to push notifications, Microsoft Edge prompts you to allow your PWA to show notifications.</span></span>  <span data-ttu-id="7c529-224">Нажмите кнопку **Разрешить**.</span><span class="sxs-lookup"><span data-stu-id="7c529-224">Select **Allow**.</span></span>  
    
    :::image type="complex" source="./media/notification-permission.png" alt-text="Выполнение нового PWA на localhost" lightbox="./media/notification-permission.png":::
       <span data-ttu-id="7c529-226">Диалоговое окно разрешений для включения уведомлений</span><span class="sxs-lookup"><span data-stu-id="7c529-226">Permission dialog for enabling notifications</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="7c529-227">Имитировать push-уведомление на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="7c529-227">Simulate a server-side push notification.</span></span>  <span data-ttu-id="7c529-228">Откройте веб – приложение Project Web App `http://localhost:3000` в браузере и нажмите кнопку, `F12` чтобы открыть DevTools.</span><span class="sxs-lookup"><span data-stu-id="7c529-228">With your PWA opened at `http://localhost:3000` in your browser, select `F12` to open the DevTools.</span></span>  <span data-ttu-id="7c529-229">Нажмите **кнопку**отправить,  >  **Service Worker**  >  **Push** чтобы отправить тестовое push-уведомление на PWA.</span><span class="sxs-lookup"><span data-stu-id="7c529-229">Choose **Application** > **Service Worker** > **Push** to send a test push notification to your PWA.</span></span>  
    :::row:::
       :::column span="":::
          <span data-ttu-id="7c529-230">На панели задач должно отобразиться push-уведомление.</span><span class="sxs-lookup"><span data-stu-id="7c529-230">A push notification should display near the taskbar.</span></span>  
          
          :::image type="complex" source="./media/devtools-push.png" alt-text="Выполнение нового PWA на localhost" lightbox="./media/devtools-push.png":::
             <span data-ttu-id="7c529-232">Отправка уведомления из DevTools</span><span class="sxs-lookup"><span data-stu-id="7c529-232">Push a notification from DevTools</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          <span data-ttu-id="7c529-233">Если вы не выберете параметр \ (или активировать) всплывающее уведомление, система автоматически закрывает ее через несколько секунд и помещает ее в свой центр уведомлений Windows.</span><span class="sxs-lookup"><span data-stu-id="7c529-233">If you do not select \(or activate\) a toast notification, the system automatically dismisses it after several seconds and queues it in your Windows Action Center.</span></span>  
          
          :::image type="complex" source="./media/windows-action-center.png" alt-text="Выполнение нового PWA на localhost" lightbox="./media/windows-action-center.png":::
             <span data-ttu-id="7c529-235">Уведомления в центре уведомлений Windows</span><span class="sxs-lookup"><span data-stu-id="7c529-235">Notifications in Windows Action Center</span></span> :::image-end:::
       :::column-end:::
    :::row-end:::  
    
## <span data-ttu-id="7c529-236">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="7c529-236">Next steps</span></span>  

<span data-ttu-id="7c529-237">Следующие действия включают дополнительные задачи, которые помогут вам разобраться в создании реальных PWAs.</span><span class="sxs-lookup"><span data-stu-id="7c529-237">The following steps include additional tasks to help you understand building real-world PWAs.</span></span>  

*   <span data-ttu-id="7c529-238">Управление принудительными подписками и их хранение</span><span class="sxs-lookup"><span data-stu-id="7c529-238">Manage and store push subscriptions</span></span>  
*   <span data-ttu-id="7c529-239">[Шифрование][NPMWebPushEncrypt] полезных данных</span><span class="sxs-lookup"><span data-stu-id="7c529-239">[Encrypt][NPMWebPushEncrypt] payload data</span></span>  
*   <span data-ttu-id="7c529-240">Адаптивный дизайн</span><span class="sxs-lookup"><span data-stu-id="7c529-240">Responsive design</span></span>  
*   <span data-ttu-id="7c529-241">Глубокая связь</span><span class="sxs-lookup"><span data-stu-id="7c529-241">Deep-linking</span></span>  
*   [<span data-ttu-id="7c529-242">Тестирование в нескольких браузерах</span><span class="sxs-lookup"><span data-stu-id="7c529-242">Cross-browser testing</span></span>][BrowserStackTestEdgeBrowser]  
*   <span data-ttu-id="7c529-243">Реализация методов проверки и тестирования, таких как " [Подсказка][Webhint] "</span><span class="sxs-lookup"><span data-stu-id="7c529-243">Implement validation and testing practices such as [Webhint][Webhint]</span></span>  
   
## <span data-ttu-id="7c529-244">См. также</span><span class="sxs-lookup"><span data-stu-id="7c529-244">See also</span></span>  

*   [<span data-ttu-id="7c529-245">Прогрессивные веб-приложения на MDN веб-документах</span><span class="sxs-lookup"><span data-stu-id="7c529-245">Progressive Web Apps on MDN web docs</span></span>][MDNProgressiveWebApps]  
*   [<span data-ttu-id="7c529-246">Прогрессивные веб-приложения на веб-сайте. dev</span><span class="sxs-lookup"><span data-stu-id="7c529-246">Progressive Web Apps on web.dev</span></span>][WebDevProgressiveWebApps]  
*   <span data-ttu-id="7c529-247">[Средства чтения новостей, такие как прогрессивные веб-приложения,][HackerNewsProgressiveWebApps] сравнивают различные платформы и шаблоны производительности для реализации примера \ (средство чтения новостей с помощью хакеров \) PWA.</span><span class="sxs-lookup"><span data-stu-id="7c529-247">[Hacker News readers as Progressive Web Apps][HackerNewsProgressiveWebApps] - Compares different frameworks and performance patterns for implementing a sample \(Hacker News reader\) PWA.</span></span>  
*   [<span data-ttu-id="7c529-248">Myth Busting PWAs</span><span class="sxs-lookup"><span data-stu-id="7c529-248">Myth Busting PWAs</span></span>][Davrous20191018MythBustingPwasNewEdgeEdition]  
*   [<span data-ttu-id="7c529-249">Прогрессивный план для последовательного веб-приложения</span><span class="sxs-lookup"><span data-stu-id="7c529-249">A Progressive Roadmap for your Progressive Web App</span></span>][CloudfourThinksProgressiveRoadmapYourWebApp]  
*   [<span data-ttu-id="7c529-250">Автономные публикации с прогрессивными веб-приложениями</span><span class="sxs-lookup"><span data-stu-id="7c529-250">Offline POSTs with Progressive Web Apps</span></span>][MediumWebEdgeOfflinePostsProgressiveWebApps]  
*   [<span data-ttu-id="7c529-251">PWA Q&A</span><span class="sxs-lookup"><span data-stu-id="7c529-251">PWA Q&A</span></span>][AaronGustafsonNotebookPwaQa]  
*   [<span data-ttu-id="7c529-252">Ставкам в Интернете</span><span class="sxs-lookup"><span data-stu-id="7c529-252">Betting on the Web</span></span>][JoretegBlogBettingWeb]  
*   [<span data-ttu-id="7c529-253">Именование последовательного веб-приложения</span><span class="sxs-lookup"><span data-stu-id="7c529-253">Naming Progressive Web Apps</span></span>][Fberriman20170626NamingProgressiveWebApps]  
*   [<span data-ttu-id="7c529-254">Проектирование и создание последовательного веб-приложения без структуры (часть 1)</span><span class="sxs-lookup"><span data-stu-id="7c529-254">Designing And Building A Progressive Web Application Without A Framework (Part 1)</span></span>][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart1]  
*   [<span data-ttu-id="7c529-255">Проектирование и создание последовательного веб-приложения без структуры (часть 2)</span><span class="sxs-lookup"><span data-stu-id="7c529-255">Designing And Building A Progressive Web Application Without A Framework (Part 2)</span></span>][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart2]  
*   [<span data-ttu-id="7c529-256">Проектирование и создание последовательного веб-приложения без структуры (часть 3)</span><span class="sxs-lookup"><span data-stu-id="7c529-256">Designing And Building A Progressive Web Application Without A Framework (Part 3)</span></span>][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart3]  
    
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
