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
# <span data-ttu-id="2a73b-105">Прогрессивные веб-приложения для Windows</span><span class="sxs-lookup"><span data-stu-id="2a73b-105">Progressive Web Apps on Windows</span></span>  

<span data-ttu-id="2a73b-106">[Прогрессивные веб-приложения][MDNApps] \ (PWAs \) предоставляют доступ к открытым веб-технологиям для взаимодействия между платформами и предоставляют пользователям собственный интерфейс, подобный приложению, настроенный для своих устройств.</span><span class="sxs-lookup"><span data-stu-id="2a73b-106">[Progressive Web Apps][MDNApps] \(PWAs\) provide access to open web technologies for cross-platform interoperability and provide your users with a native, app-like experience customized for their devices.</span></span>  <span data-ttu-id="2a73b-107">PWAs — это веб-сайты, которые будут [последовательно расширены][AListApartUnderstandingProgressiveEnhancement] для работы, например собственные приложения на поддерживаемых платформах.</span><span class="sxs-lookup"><span data-stu-id="2a73b-107">PWAs are websites that are [progressively enhanced][AListApartUnderstandingProgressiveEnhancement] to function like native apps on supporting platforms.</span></span>  <span data-ttu-id="2a73b-108">В приложениях PWA объединены лучшие качестве веб- и собственных приложения.</span><span class="sxs-lookup"><span data-stu-id="2a73b-108">The qualities of a PWA combine the best of the web and native apps.</span></span>  

:::row:::
    :::column:::
        :::image type="icon" source="./media/i_search.png":::
        ### [<span data-ttu-id="2a73b-109">Обнаруживаемым</span><span class="sxs-lookup"><span data-stu-id="2a73b-109">Discoverable</span></span>][MDNPwaAdvantagesDiscoverable]
        <span data-ttu-id="2a73b-110">Из результатов поиска в Интернете и поддержки магазинов приложений</span><span class="sxs-lookup"><span data-stu-id="2a73b-110">From web search results and supporting app stores</span></span>
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_package.png":::
        ### [<span data-ttu-id="2a73b-111">Устанавливаемый</span><span class="sxs-lookup"><span data-stu-id="2a73b-111">Installable</span></span>][MDNPwaAdvantagesInstallable]
        <span data-ttu-id="2a73b-112">Закрепление и запуск на начальном экране, меню "Пуск", панели задач и т. д.</span><span class="sxs-lookup"><span data-stu-id="2a73b-112">Pin and launch from the home screen, Start Menu, Taskbar, and so on</span></span>
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_push-notification.png":::
        ### [<span data-ttu-id="2a73b-113">Повторное участие</span><span class="sxs-lookup"><span data-stu-id="2a73b-113">Re-engageable</span></span>][MDNPwaAdvantagesReEngageable]
        <span data-ttu-id="2a73b-114">Отправлять push-уведомления, даже если приложение неактивно</span><span class="sxs-lookup"><span data-stu-id="2a73b-114">Send push notifications, even when the app is not active</span></span>
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        :::image type="icon" source="./media/i_offline.png":::
        ### [<span data-ttu-id="2a73b-115">Сетевая независимость</span><span class="sxs-lookup"><span data-stu-id="2a73b-115">Network Independent</span></span>][MDNPwaAdvantagesNetworkIndependent]
        <span data-ttu-id="2a73b-116">Работа в автономном режиме и в условиях низкой сети</span><span class="sxs-lookup"><span data-stu-id="2a73b-116">Works offline and in low-network conditions</span></span>
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_progressive.png":::
        ### [<span data-ttu-id="2a73b-117">JPEG</span><span class="sxs-lookup"><span data-stu-id="2a73b-117">Progressive</span></span>][MDNPwaAdvantagesProgressive]
        <span data-ttu-id="2a73b-118">Работа с возможностями устройства в масштабе (или в меньшую сторону)</span><span class="sxs-lookup"><span data-stu-id="2a73b-118">Experience scales up (or down) with device capabilities</span></span>
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_security.png":::
        ### [<span data-ttu-id="2a73b-119">Безопасной</span><span class="sxs-lookup"><span data-stu-id="2a73b-119">Safe</span></span>][MDNPwaAdvantagesSafe]
        <span data-ttu-id="2a73b-120">Обеспечивает защищенную конечную точку HTTPS и другие меры для защиты от пользователей</span><span class="sxs-lookup"><span data-stu-id="2a73b-120">Provides a secure HTTPS endpoint and other user safeguards</span></span>
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        :::image type="icon" source="./media/i_responsive.png":::
        ### [<span data-ttu-id="2a73b-121">Хорошая скорость отклика</span><span class="sxs-lookup"><span data-stu-id="2a73b-121">Responsive</span></span>][MDNPwaAdvantagesResponsive]
        <span data-ttu-id="2a73b-122">Адаптируется к размеру экрана или ориентации и методу ввода для пользователя</span><span class="sxs-lookup"><span data-stu-id="2a73b-122">Adapts to the user's screen size or orientation and input method</span></span>
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_link.png":::
        ### [<span data-ttu-id="2a73b-123">Связь</span><span class="sxs-lookup"><span data-stu-id="2a73b-123">Linkable</span></span>][MDNPwaAdvantagesLinkable]
        <span data-ttu-id="2a73b-124">Предоставление общего доступа к файлу и его запуск с помощью стандартной гиперссылки</span><span class="sxs-lookup"><span data-stu-id="2a73b-124">Share and launch from a standard hyperlink</span></span>
    :::column-end:::
    :::column:::
        &nbsp;  
    :::column-end:::
:::row-end:::  


<span data-ttu-id="2a73b-125">Создайте или преобразуйте существующий веб-сайт в Project Web App, чтобы улучшить свое сотрудничество с пользователями.</span><span class="sxs-lookup"><span data-stu-id="2a73b-125">Build \(or convert\) your existing website to a PWA to enhance your engagement with your users.</span></span>  <span data-ttu-id="2a73b-126">Усовершенствования включают push-уведомления, интеграцию с приложением и поддержку в автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="2a73b-126">Enhancements include push notifications, app-like integration, and offline support.</span></span>  <span data-ttu-id="2a73b-127">Продолжайте разрабатывать аудитории в открытом веб-браузере, чтобы пользователи обнаружили, что вы можете найти в PWA с помощью поиска и совместного использования ссылок.</span><span class="sxs-lookup"><span data-stu-id="2a73b-127">Continue to build your audience on the open web for users to discover your PWA through search and link-sharing.</span></span>  <span data-ttu-id="2a73b-128">Для этого ваше приложение Обновлено с использованием кода веб-сервера.</span><span class="sxs-lookup"><span data-stu-id="2a73b-128">Best of all, your app is updated in using your web server code.</span></span>  

## <span data-ttu-id="2a73b-129">PWAs в Microsoft EDGE (Chromium)</span><span class="sxs-lookup"><span data-stu-id="2a73b-129">PWAs on Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="2a73b-130">При создании последовательного веб-приложения, нацеленного на веб-интерфейс API, приложение может быть развернуто на разных платформах и устройствах и использовать возможности, доступные для конкретных устройств.</span><span class="sxs-lookup"><span data-stu-id="2a73b-130">When you build a Progressive Web App targeting web standard APIs, your application may be deployed across platforms and devices and take advantage of the device-specific capabilities as available.</span></span>  <span data-ttu-id="2a73b-131">PWAs в Microsoft Edge \ (Chromium \) добавьте следующие преимущества на ваш веб-сайт.</span><span class="sxs-lookup"><span data-stu-id="2a73b-131">PWAs in Microsoft Edge \(Chromium\) add the following advantages to your website.</span></span>  

*   <span data-ttu-id="2a73b-132">Ваше приложение строится на веб-платформе, основанной на стандартах.</span><span class="sxs-lookup"><span data-stu-id="2a73b-132">Your app is built on a standards-based web platform.</span></span>  
*   <span data-ttu-id="2a73b-133">Позволяет пользователям устанавливать приложение прямо из браузера.</span><span class="sxs-lookup"><span data-stu-id="2a73b-133">Enables your users to install your app directly from the browser.</span></span>  
*   <span data-ttu-id="2a73b-134">Позволяет пользователям устанавливать приложение без развертывания и регистрации на основе магазина.</span><span class="sxs-lookup"><span data-stu-id="2a73b-134">Enables your users to install your app without a Store-based deployment or registration.</span></span>  
    
<span data-ttu-id="2a73b-135">Классическое PWAs поддерживается на любой из платформ Microsoft Edge \ (Chromium \).</span><span class="sxs-lookup"><span data-stu-id="2a73b-135">Desktop PWAs are supported on any of the platforms Microsoft Edge \(Chromium\) is available.</span></span> <span data-ttu-id="2a73b-136">Microsoft Edge \ (Chromium \) доступен в Windows 7, Windows 10 и macOS.</span><span class="sxs-lookup"><span data-stu-id="2a73b-136">Microsoft Edge \(Chromium\) is available on Windows 7, Windows 10, and macOS.</span></span>  <span data-ttu-id="2a73b-137">Включены следующие преимущества:</span><span class="sxs-lookup"><span data-stu-id="2a73b-137">The following benefits are included.</span></span>  

*   <span data-ttu-id="2a73b-138">Приложения можно устанавливать прямо из браузера с помощью значка **установки** на панели навигации.</span><span class="sxs-lookup"><span data-stu-id="2a73b-138">Applications may be installed directly from within the browser using the **Install** icon in the navigation bar.</span></span>  
    
    :::image type="complex" source="./media/install_pwa_icon.png" alt-text="Всплывающее меню и значок установки приложения" lightbox="./media/install_pwa_icon.png":::
       <span data-ttu-id="2a73b-140">Всплывающее меню и значок установки приложения</span><span class="sxs-lookup"><span data-stu-id="2a73b-140">Install application flyout and icon</span></span>  
    :::image-end:::  
    
*   <span data-ttu-id="2a73b-141">Кроме того, в меню " **Параметры**" приложения можно устанавливать, запускать и управлять приложениями.  >  **Apps**</span><span class="sxs-lookup"><span data-stu-id="2a73b-141">Applications may also be installed, run, and managed from the **Settings** > **Apps** menu</span></span>  
    
    :::image type="complex" source="./media/app_menus.png" alt-text="Всплывающее меню и значок установки приложения" lightbox="./media/app_menus.png":::
       <span data-ttu-id="2a73b-143">Элементы меню "приложение" в разделе "Параметры"</span><span class="sxs-lookup"><span data-stu-id="2a73b-143">Application menu items under settings</span></span>  
    :::image-end:::  
    
*   <span data-ttu-id="2a73b-144">Веб-уведомления интегрированы в систему уведомлений Windows</span><span class="sxs-lookup"><span data-stu-id="2a73b-144">Web Notifications are integrated into the Windows notification system</span></span>  
*   <span data-ttu-id="2a73b-145">Общее хранилище файлов cookie с профилем браузера, в котором установлено приложение</span><span class="sxs-lookup"><span data-stu-id="2a73b-145">Shared cookie store with the browser profile that installed the app</span></span>  
*   <span data-ttu-id="2a73b-146">Доступ к другим функциям браузера с помощью меню " **Настройка" и других** параметров \ ( `...` \), включая проверку сертификата, разрешения сайтов, защиту от слежения и расширения браузера.</span><span class="sxs-lookup"><span data-stu-id="2a73b-146">Access to other browser features using the **Setting and more** \(`...`\) menu including certificate validation, site permissions, tracking protection, and browser extensions</span></span>  
*   <span data-ttu-id="2a73b-147">Полный доступ к [Microsoft Edge DevTools][DevtoolsProgressiveWebApps] для отладки приложения</span><span class="sxs-lookup"><span data-stu-id="2a73b-147">Full access to [Microsoft Edge DevTools][DevtoolsProgressiveWebApps] for debugging your app</span></span>  
    
> [!IMPORTANT]
> <span data-ttu-id="2a73b-148">Чтобы настроить PWAs специально для Windows 10, которые делают запросы API WinRT с помощью JavaScript, перейдите в [документацию, относящуюся к функциям EDGEHTML PWA][PwaEdgehtmlIndex].</span><span class="sxs-lookup"><span data-stu-id="2a73b-148">To tailor PWAs specifically for Windows 10 that make WinRT API requests using JavaScript, navigate to [documentation specific to the EdgeHTML PWA features][PwaEdgehtmlIndex].</span></span>  <span data-ttu-id="2a73b-149">Узнайте больше о том, как тестировать PWA в Windows 10 и распространять его в Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="2a73b-149">Learn more about testing your PWA on Windows 10 and distributing it in the Microsoft Store.</span></span>  

> [!NOTE]
> <span data-ttu-id="2a73b-150">Дополнительные сведения о преимуществах PWA, предстоящих функциях и кратких видеодемонстрациях можно найти в разделе [Сборка сеанса 2020 PWA][BuildVideo].</span><span class="sxs-lookup"><span data-stu-id="2a73b-150">For more information about PWA benefits, upcoming features, and short demos, navigate to [Build 2020 PWA session][BuildVideo].</span></span> 

## <span data-ttu-id="2a73b-151">Требования</span><span class="sxs-lookup"><span data-stu-id="2a73b-151">Requirements</span></span>  

<span data-ttu-id="2a73b-152">Для работы в качестве PWA веб-приложение, размещенное на сервере, должно включать следующие минимальные требования.</span><span class="sxs-lookup"><span data-stu-id="2a73b-152">To run as a PWA, your server-hosted web app should include following minimum requirements.</span></span>  

:::row:::
   :::column span="1":::
      [<span data-ttu-id="2a73b-153">HTTPS</span><span class="sxs-lookup"><span data-stu-id="2a73b-153">HTTPS</span></span>][WikiHttps]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="2a73b-154">Защищает пользователей, обеспечивая безопасное подключение для обмена данными между сервером и приложением.</span><span class="sxs-lookup"><span data-stu-id="2a73b-154">Protects your users by providing a secure connection for server or app communication.</span></span>  <span data-ttu-id="2a73b-155">Сотрудники служб и другие технологии PWA работают только с веб-ресурсами, обслуживаемыми в безопасном соединении (или в `localhost` целях отладки).</span><span class="sxs-lookup"><span data-stu-id="2a73b-155">Service Workers and other PWA technologies only work with web resources served over a secure connection \(or from `localhost` for debugging purposes\).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="2a73b-156">Служебные сценарии</span><span class="sxs-lookup"><span data-stu-id="2a73b-156">Service Workers</span></span>][MDNServiceWorkerApi]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="2a73b-157">Использует рабочие потоки службы, чтобы выступать в качестве сетевых прокси между сервером и клиентским приложением.</span><span class="sxs-lookup"><span data-stu-id="2a73b-157">Uses Service Worker threads to act as network proxies between your server and client app.</span></span>  <span data-ttu-id="2a73b-158">Рабочие потоки служб предоставляют поддержку в автономном режиме, кэширование ресурсов, Push-уведомления, фоновую синхронизацию данных и оптимизации производительности загрузки страниц.</span><span class="sxs-lookup"><span data-stu-id="2a73b-158">Service Worker threads provide offline support, resource caching, push notifications, background data sync, and  page-load performance optimizations.</span></span>    
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="2a73b-159">Манифест веб-приложения</span><span class="sxs-lookup"><span data-stu-id="2a73b-159">Web App Manifest</span></span>][MDNWebAppManifest]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="2a73b-160">Предоставляет файл метаданных на основе JSON, в котором описаны ключевые сведения о вашем веб-приложении, так что Windows 10 и другие платформы узла предоставляют пользователям PWA возможности устанавливаемого и собственного приложения.</span><span class="sxs-lookup"><span data-stu-id="2a73b-160">Provides a JSON-based metadata file that describes key information about your web app, so that Windows 10 and other host platforms provide your PWA users with an installable, native app-like experience.</span></span>  <span data-ttu-id="2a73b-161">Ключевые сведения включают значки, язык и точку входа URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="2a73b-161">Key information includes icons, language, and URL entry point.</span></span> 
   :::column-end:::
:::row-end:::  

<span data-ttu-id="2a73b-162">Для того чтобы стать прекрасным PWA, ваше приложение должно также отвечать указанным ниже требованиям.</span><span class="sxs-lookup"><span data-stu-id="2a73b-162">To be a great PWA, your app must also meet the following requirements.</span></span>  

:::row:::
   :::column span="1":::
      [<span data-ttu-id="2a73b-163">Совместимость с различными браузерами</span><span class="sxs-lookup"><span data-stu-id="2a73b-163">Cross-browser compatibility</span></span>][MDNCrossBrowserTesting]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="2a73b-164">Убедитесь, что веб-приложение PWA [работает в разных][MicrosoftDeveloperEdgeToolsRemote] браузерах и средах.</span><span class="sxs-lookup"><span data-stu-id="2a73b-164">Ensure your PWA works by [testing][MicrosoftDeveloperEdgeToolsRemote] in different browsers and environments.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="2a73b-165">Адаптивный дизайн</span><span class="sxs-lookup"><span data-stu-id="2a73b-165">Responsive design</span></span>][WikiResponsiveWebDesign]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="2a73b-166">Применение жидких макетов и гибких изображений.</span><span class="sxs-lookup"><span data-stu-id="2a73b-166">Employs fluid layouts and flexible images.</span></span>  <span data-ttu-id="2a73b-167">Высокореагируый дизайн включает следующие элементы, которые адаптирует пользовательский интерфейс к устройству пользователя.</span><span class="sxs-lookup"><span data-stu-id="2a73b-167">Responsive design includes the following elements that adapt your UX to your user's device.</span></span>  
      
      *   <span data-ttu-id="2a73b-168">[Сетка][MDNCssGridLayout] CSS</span><span class="sxs-lookup"><span data-stu-id="2a73b-168">CSS [grid][MDNCssGridLayout]</span></span>  
      *   [<span data-ttu-id="2a73b-169">расположен</span><span class="sxs-lookup"><span data-stu-id="2a73b-169">flexbox</span></span>][MDNCssFlexibleBoxLayout]  
      *   <span data-ttu-id="2a73b-170">Сетка и [Гибкая][MDNCssFlexibleBoxLayout] [Таблица][MDNCssGridLayout] CSS</span><span class="sxs-lookup"><span data-stu-id="2a73b-170">CSS [grid][MDNCssGridLayout] and [flexbox][MDNCssFlexibleBoxLayout]</span></span>  
      *   [<span data-ttu-id="2a73b-171">запросы мультимедиа</span><span class="sxs-lookup"><span data-stu-id="2a73b-171">media queries</span></span>][MDNMediaQueries]  
      *   [<span data-ttu-id="2a73b-172">отклики изображений</span><span class="sxs-lookup"><span data-stu-id="2a73b-172">responsive images</span></span>][MDNResponsiveImages]  
      
      <span data-ttu-id="2a73b-173">Использует [средства эмуляции устройства][DevToolsGuide|::ref1::|] в браузере для проверки локально или создания [сеанса удаленной отладки][DevToolsProtocolClientsEdgeDevToolsPreview] для проверки непосредственно на целевом устройстве.</span><span class="sxs-lookup"><span data-stu-id="2a73b-173">Uses [device emulation tools][DevToolsGuide|::ref1::|] from your browser to locally test, or create a [remote debugging session][DevToolsProtocolClientsEdgeDevToolsPreview] to test directly on a target device.</span></span>
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="2a73b-174">Глубокая связь</span><span class="sxs-lookup"><span data-stu-id="2a73b-174">Deep linking</span></span>][WikiDeepLinking]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="2a73b-175">Каждая страница сайта отправляется на уникальный URL-адрес, чтобы пользователи могли использовать более обширную аудиторию через функцию совместного использования социальных сетей.</span><span class="sxs-lookup"><span data-stu-id="2a73b-175">Routes each page of your site to a unique URL so existing users may help you engage an even broader audience through social media sharing.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="2a73b-176">Рекомендации по проверке и тестированию</span><span class="sxs-lookup"><span data-stu-id="2a73b-176">Validation and testing practices</span></span>][Webhint]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="2a73b-177">Использование средств качества кода, таких как Linter веб – [Подсказка][Webhint] , для оптимизации эффективности, надежности, безопасности и специальных возможностей вашего приложения.</span><span class="sxs-lookup"><span data-stu-id="2a73b-177">Uses code quality tools like the [Webhint][Webhint] linter to optimize the efficiency, robustness, safety, and accessibility of your app.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="2a73b-178">Контрольный список для Chromium PWA</span><span class="sxs-lookup"><span data-stu-id="2a73b-178">Chromium PWA Checklist</span></span>][WebDevGoodPwaChecklist]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="2a73b-179">Проверка PWA на соответствие контрольному списку Google Baseline Access.</span><span class="sxs-lookup"><span data-stu-id="2a73b-179">Verifies your PWA against the Google baseline PWA checklist.</span></span>  
   :::column-end:::
:::row-end:::  

> [!NOTE]
> <span data-ttu-id="2a73b-180">Чтобы преобразовать PWA в приложение [Microsoft Store][MicrosoftDeveloperStore] , перейдите в [раздел прогрессивные веб-приложения (EdgeHTML) в Microsoft Store][PwaEdgehtmlMicrosoftStore].</span><span class="sxs-lookup"><span data-stu-id="2a73b-180">To turn your PWA into a [Microsoft Store][MicrosoftDeveloperStore] application, navigate to [Progressive Web Apps (EdgeHTML) in the Microsoft Store][PwaEdgehtmlMicrosoftStore].</span></span>  
  
## <span data-ttu-id="2a73b-181">См. также</span><span class="sxs-lookup"><span data-stu-id="2a73b-181">See also</span></span>  

*   [<span data-ttu-id="2a73b-182">Myth Busting PWAs</span><span class="sxs-lookup"><span data-stu-id="2a73b-182">Myth Busting PWAs</span></span>][Davrous20191018MythBustingPwasNewEdgeEdition]  
*   [<span data-ttu-id="2a73b-183">Прогрессивный план для последовательного веб-приложения</span><span class="sxs-lookup"><span data-stu-id="2a73b-183">A Progressive Roadmap for your Progressive Web App</span></span>][CloudfourThinksProgressiveRoadmapYourWebApp]  
*   [<span data-ttu-id="2a73b-184">Автономные публикации с прогрессивными веб-приложениями</span><span class="sxs-lookup"><span data-stu-id="2a73b-184">Offline POSTs with Progressive Web Apps</span></span>][MediumWebEdgeOfflinePostsProgressiveWebApps]  
*   [<span data-ttu-id="2a73b-185">PWA Q&A</span><span class="sxs-lookup"><span data-stu-id="2a73b-185">PWA Q&A</span></span>][AaronGustafsonNotebookPwaQa]  
*   [<span data-ttu-id="2a73b-186">Ставкам в Интернете</span><span class="sxs-lookup"><span data-stu-id="2a73b-186">Betting on the Web</span></span>][JoretegBlogBettingWeb]  
*   [<span data-ttu-id="2a73b-187">Именование последовательного веб-приложения</span><span class="sxs-lookup"><span data-stu-id="2a73b-187">Naming Progressive Web Apps</span></span>][Fberriman20170626NamingProgressiveWebApps]  
*   [<span data-ttu-id="2a73b-188">Проектирование и создание последовательного веб-приложения без структуры (часть 1)</span><span class="sxs-lookup"><span data-stu-id="2a73b-188">Designing And Building A Progressive Web Application Without A Framework (Part 1)</span></span>][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart1]  
*   [<span data-ttu-id="2a73b-189">Проектирование и создание последовательного веб-приложения без структуры (часть 2)</span><span class="sxs-lookup"><span data-stu-id="2a73b-189">Designing And Building A Progressive Web Application Without A Framework (Part 2)</span></span>][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart2]  
*   [<span data-ttu-id="2a73b-190">Проектирование и создание последовательного веб-приложения без структуры (часть 3)</span><span class="sxs-lookup"><span data-stu-id="2a73b-190">Designing And Building A Progressive Web Application Without A Framework (Part 3)</span></span>][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart3]  
    
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
