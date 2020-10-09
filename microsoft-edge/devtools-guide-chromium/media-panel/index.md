---
description: С помощью панели мультимедиа вы можете просматривать сведения и отлаживать проигрыватели мультимедиа на вкладке "браузер".
title: Просмотр и отладка сведений о проигрывателях мультимедиа
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/08/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: dfcf17861c0296e347007bc3a1a02a2b80661e6f
ms.sourcegitcommit: 912609aa49864e3363aaa3b245ff2aa4bec3fc3e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/08/2020
ms.locfileid: "11105213"
---
# <span data-ttu-id="b9b71-104">Просмотр и отладка сведений о проигрывателях мультимедиа</span><span class="sxs-lookup"><span data-stu-id="b9b71-104">View and debug media players information</span></span>  

<span data-ttu-id="b9b71-105">С помощью панели **медиа** в Microsoft Edge DevTools можно просматривать сведения и отлаживать проигрыватели мультимедиа на вкладке "браузер".</span><span class="sxs-lookup"><span data-stu-id="b9b71-105">Use the **Media** panel in Microsoft Edge DevTools to view information and debug the media players per browser tab.</span></span>  

## <span data-ttu-id="b9b71-106">Открытие панели мультимедиа</span><span class="sxs-lookup"><span data-stu-id="b9b71-106">Open the Media panel</span></span>  

<span data-ttu-id="b9b71-107">Панель " **мультимедиа** " — это основное место в DevTools для проверки проигрывателя мультимедиа на веб-странице.</span><span class="sxs-lookup"><span data-stu-id="b9b71-107">The **Media** panel is the main place in DevTools for inspecting the media player of a webpage.</span></span>

1.  <span data-ttu-id="b9b71-108">[Откройте DevTools][DevtoolsGuideChromiumOpen].</span><span class="sxs-lookup"><span data-stu-id="b9b71-108">[Open DevTools][DevtoolsGuideChromiumOpen].</span></span>  
1.  <span data-ttu-id="b9b71-109">Чтобы открыть панель " **мультимедиа** ", нажмите кнопку **Настройка и управление DevTools** `...`  >  **дополнительных средств**  >  **мультимедиа**.</span><span class="sxs-lookup"><span data-stu-id="b9b71-109">To open the **Media** panel, choose **Customize and control DevTools** `...` > **More tools** > **Media**.</span></span>  
    
    :::image type="complex" source="../media/media-panel-empty.msft.png" alt-text="Панель мультимедиа" lightbox="../media/media-panel-empty.msft.png":::
       <span data-ttu-id="b9b71-111">Панель **мультимедиа**</span><span class="sxs-lookup"><span data-stu-id="b9b71-111">**Media** panel</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="b9b71-112">Просмотр сведений о проигрывателях мультимедиа</span><span class="sxs-lookup"><span data-stu-id="b9b71-112">View media players information</span></span>  

1.  <span data-ttu-id="b9b71-113">Перейдите на веб-страницу с помощью универсального проигрывателя, например следующей веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="b9b71-113">Navigate to a webpage with a media player, such as the following webpage.</span></span>  
    
    [<span data-ttu-id="b9b71-114">Максимизация производительности с помощью средств разработчика Edge</span><span class="sxs-lookup"><span data-stu-id="b9b71-114">Maximizing productivity with the Edge Developer Tools</span></span>][BingVideosSearchViewDetailMidE0BA14EC0E0D18C06C8DE0BA14EC0E0D18C06C8]  
    
1.  <span data-ttu-id="b9b71-115">В меню **игрока** отображается проигрыватель мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="b9b71-115">Under the **Players** menu, a media player is displayed.</span></span>  
1.  <span data-ttu-id="b9b71-116">Выберите игрока.</span><span class="sxs-lookup"><span data-stu-id="b9b71-116">Select the player.</span></span>  <span data-ttu-id="b9b71-117">На вкладке **Свойства** отображаются свойства универсального проигрывателя.</span><span class="sxs-lookup"><span data-stu-id="b9b71-117">The **Properties** tab displays the properties of the media player.</span></span>  
    
    :::image type="complex" source="../media/media-panel-view.msft.png" alt-text="Панель мультимедиа" lightbox="../media/media-panel-view.msft.png":::
       <span data-ttu-id="b9b71-119">Свойства мультимедиа</span><span class="sxs-lookup"><span data-stu-id="b9b71-119">Media properties</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b9b71-120">Чтобы просмотреть все события проигрывателя мультимедиа, перейдите на вкладку **события** .</span><span class="sxs-lookup"><span data-stu-id="b9b71-120">To view all the media player events, choose the **Events** tab.</span></span>  
    
    :::image type="complex" source="../media/media-panel-events.msft.png" alt-text="Панель мультимедиа" lightbox="../media/media-panel-events.msft.png":::
       <span data-ttu-id="b9b71-122">События мультимедиа</span><span class="sxs-lookup"><span data-stu-id="b9b71-122">Media events</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b9b71-123">Чтобы просмотреть журналы сообщений проигрывателя мультимедиа, выберите вкладку **сообщения** .  Вы можете отфильтровать сообщения по уровню или строке журнала.</span><span class="sxs-lookup"><span data-stu-id="b9b71-123">To view the media player message logs, choose the **Messages** tab.  You may filter the messages by log level or string.</span></span>  
    
    :::image type="complex" source="../media/media-panel-messages.msft.png" alt-text="Панель мультимедиа" lightbox="../media/media-panel-messages.msft.png":::
       <span data-ttu-id="b9b71-125">Мультимедийные сообщения</span><span class="sxs-lookup"><span data-stu-id="b9b71-125">Media messages</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b9b71-126">На вкладке **временная шкала** воспроизведение мультимедиа и состояние буфера отображаются в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="b9b71-126">On the **Timeline** tab, the media playback and buffer status is displayed live.</span></span>  
    
    :::image type="complex" source="../media/media-panel-timeline.msft.png" alt-text="Панель мультимедиа" lightbox="../media/media-panel-timeline.msft.png":::
       <span data-ttu-id="b9b71-128">Временная шкала мультимедиа</span><span class="sxs-lookup"><span data-stu-id="b9b71-128">Media timeline</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="b9b71-129">Удаленная отладка</span><span class="sxs-lookup"><span data-stu-id="b9b71-129">Remote debugging</span></span>  

<span data-ttu-id="b9b71-130">Просмотр сведений о проигрывателях мультимедиа на устройстве с ОС Windows или macOS с компьютера Android.</span><span class="sxs-lookup"><span data-stu-id="b9b71-130">View the media players information on an Android device from your Windows or macOS computer.</span></span>  

1.  <span data-ttu-id="b9b71-131">Чтобы настроить удаленную отладку, перейдите в раздел Начало [работы с удаленно удаленной отладкой устройств с Android][DevtoolsGuideChromiumRemoteDebuggingIndex].</span><span class="sxs-lookup"><span data-stu-id="b9b71-131">To set up remote debugging, navigate to [Get started with remote debugging Android devices][DevtoolsGuideChromiumRemoteDebuggingIndex].</span></span>  
1.  <span data-ttu-id="b9b71-132">Удаленное Просмотр сведений о проигрывателях мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="b9b71-132">View the media players information remotely.</span></span>  
    
    <!-- TODO: recreate image using an Android device -->  
    <!--  
    :::image type="complex" source="../media/media-panel-remote-debug.msft.png" alt-text="Панель мультимедиа" lightbox="../media/media-panel-remote-debug.msft.png":::
       Remote debugging  
    :::image-end:::  
    -->  
    
## <span data-ttu-id="b9b71-133">Скрытие и отображение проигрывателей мультимедиа</span><span class="sxs-lookup"><span data-stu-id="b9b71-133">Hide and show media players</span></span>  

<span data-ttu-id="b9b71-134">Иногда вы запускаете несколько проигрывателей мультимедиа на веб-странице или с помощью одной вкладки браузера для просмотра различных веб-страниц с помощью мультимедийных проигрывателей.</span><span class="sxs-lookup"><span data-stu-id="b9b71-134">Sometimes you run more than one media player on a webpage, or use the same browser tab to browse different webpages, each with media players.</span></span>

<span data-ttu-id="b9b71-135">Вы можете скрыть \ (или показать) каждый проигрыватель мультимедиа для более удобного процесса отладки.</span><span class="sxs-lookup"><span data-stu-id="b9b71-135">You may choose to hide \(or show\) each media player for an easier debugging experience.</span></span>  

1.  <span data-ttu-id="b9b71-136">Переход на несколько различных веб-страниц видео с помощью одной вкладки браузера.</span><span class="sxs-lookup"><span data-stu-id="b9b71-136">Browse to several different video webpages using the same browser tab.</span></span>  
1.  <span data-ttu-id="b9b71-137">Чтобы скрыть проигрыватели мультимедиа, выполните одно из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="b9b71-137">To hide media players, complete one of the following actions.</span></span>  
    *   <span data-ttu-id="b9b71-138">Чтобы скрыть один проигрыватель мультимедиа, наведите на него указатель мыши, откройте контекстное меню, а затем выберите команду **Скрыть проигрыватель**.</span><span class="sxs-lookup"><span data-stu-id="b9b71-138">To hide one media player, hover on a media player, open the contextual menu \(right-click\), and choose **Hide player**.</span></span>  
    *   <span data-ttu-id="b9b71-139">Чтобы скрыть все другие проигрыватели мультимедиа, наведите указатель мыши на проигрыватель мультимедиа, откройте контекстное меню, а затем выберите команду **Скрыть все другие**.</span><span class="sxs-lookup"><span data-stu-id="b9b71-139">To hide all of the other media players, hover on a media player, open the contextual menu \(right-click\), and choose **Hide all others**.</span></span>  
    
    :::image type="complex" source="../media/media-panel-hide-show.msft.png" alt-text="Панель мультимедиа" lightbox="../media/media-panel-hide-show.msft.png":::
       <span data-ttu-id="b9b71-141">Скрытие проигрывателей мультимедиа</span><span class="sxs-lookup"><span data-stu-id="b9b71-141">Hide media players</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="b9b71-142">Экспорт сведений о проигрывателе мультимедиа</span><span class="sxs-lookup"><span data-stu-id="b9b71-142">Export media player information</span></span>  

1.  <span data-ttu-id="b9b71-143">Чтобы загрузить сведения о проигрывателе мультимедиа в формате JSON, наведите указатель мыши на проигрыватель мультимедиа, откройте контекстное меню (щелкните правой кнопкой мыши и выберите команду **сохранить сведения о проигрывателе**).</span><span class="sxs-lookup"><span data-stu-id="b9b71-143">To download the media player info as a JSON file, hover on a media player, open the contextual menu \(right-click\), and choose **Save player info**.</span></span>  
    
    :::image type="complex" source="../media/media-panel-save.msft.png" alt-text="Панель мультимедиа" lightbox="../media/media-panel-save.msft.png":::
       <span data-ttu-id="b9b71-145">Экспорт мультимедийных данных</span><span class="sxs-lookup"><span data-stu-id="b9b71-145">Export media information</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="b9b71-146">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="b9b71-146">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumOpen]: ../open.md "Открыть Microsoft Edge DevTools"  

[DevtoolsGuideChromiumRemoteDebuggingIndex]: ../remote-debugging/index.md "Начало работы с удаленными отладочными устройствами Android | Документы Microsoft"  

[BingVideosSearchViewDetailMidE0BA14EC0E0D18C06C8DE0BA14EC0E0D18C06C8]: https://www.bing.com/videos/search?view=detail&mid=DE0BA14EC0E0D18C06C8DE0BA14EC0E0D18C06C8 "Максимально подвысьте производительность с помощью средств разработчика Edge | Видеоролик Bing"  

> [!NOTE]
> <span data-ttu-id="b9b71-150">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b9b71-150">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="b9b71-151">Исходная страница [будет найдена, и](https://developers.google.com/web/tools/chrome-devtools/media-panel/index) ее можно создать с помощью [Jecelyn Yeen][JecelynYeen] \ (разработчик отвечает, Chrome DevTools \).</span><span class="sxs-lookup"><span data-stu-id="b9b71-151">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/media-panel/index) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="b9b71-153">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b9b71-153">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  

