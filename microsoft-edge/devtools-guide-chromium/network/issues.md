---
description: Сведения о том, как найти сетевые проблемы на панели "сеть" в Microsoft Edge DevTools.
title: Справочные материалы по неполадкам в сети
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: ccd78c34a50bf235416df58aad28df9253b1b24e
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993375"
---
<!-- Copyright Kayce Basques and Jonathan Garbee

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->





# <span data-ttu-id="0d8c7-104">Руководство по сетевым проблемам</span><span class="sxs-lookup"><span data-stu-id="0d8c7-104">Network issues guide</span></span>   




<span data-ttu-id="0d8c7-105">В этом руководстве показано, как определить сетевые проблемы или возможности оптимизации на панели "сеть" Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="0d8c7-105">This guide shows you how to detect network issues or optimization opportunities in the Network panel of Microsoft Edge DevTools.</span></span>  

<span data-ttu-id="0d8c7-106">Ознакомьтесь со [статьей][NetworkPerformance] "Начало работы", чтобы ознакомиться с основными понятиями панели " **сеть** ".</span><span class="sxs-lookup"><span data-stu-id="0d8c7-106">See [Get Started][NetworkPerformance] to learn the basics of the **Network** panel.</span></span>  

## <span data-ttu-id="0d8c7-107">Запросы, поставленные в очередь или остановленные</span><span class="sxs-lookup"><span data-stu-id="0d8c7-107">Queued or stalled requests</span></span>   

**<span data-ttu-id="0d8c7-108">Симптомы</span><span class="sxs-lookup"><span data-stu-id="0d8c7-108">Symptoms</span></span>**  

<span data-ttu-id="0d8c7-109">Шесть запросов загружаются одновременно.</span><span class="sxs-lookup"><span data-stu-id="0d8c7-109">Six requests are downloading simultaneously.</span></span>  <span data-ttu-id="0d8c7-110">После этого серии запросов будут помещены в очередь или остановлены.</span><span class="sxs-lookup"><span data-stu-id="0d8c7-110">After that, a series of requests are queued or stalled.</span></span>  <span data-ttu-id="0d8c7-111">После завершения одного из шести первых запросов запускается один из запросов в очереди.</span><span class="sxs-lookup"><span data-stu-id="0d8c7-111">Once one of the first six requests finishes, one of the requests in the queue starts.</span></span>  

<span data-ttu-id="0d8c7-112">На **каскаде** на приведенном ниже рисунке первые шесть запросов `edge-iconx1024.msft.png` актива запускаются одновременно.</span><span class="sxs-lookup"><span data-stu-id="0d8c7-112">In the **Waterfall** in the following figure, the first six requests for the `edge-iconx1024.msft.png` asset start simultaneously.</span></span>  <span data-ttu-id="0d8c7-113">Последующие запросы загружаются до тех пор, пока не завершится один из этих шести первоначальных элементов.</span><span class="sxs-lookup"><span data-stu-id="0d8c7-113">The subsequent requests are stalled until one of the original six finishes.</span></span>  

:::image type="complex" source="../media/network-network-disabled-cache-resources-queue.msft.png" alt-text="Пример списка в очереди или остановленного ряда на панели &quot;сеть&quot;" lightbox="../media/network-network-disabled-cache-resources-queue.msft.png":::
   <span data-ttu-id="0d8c7-115">Пример списка в очереди или остановленного ряда на панели " **сеть** "</span><span class="sxs-lookup"><span data-stu-id="0d8c7-115">An example of a queued or stalled series in the **Network** panel</span></span>  
:::image-end:::  

**<span data-ttu-id="0d8c7-116">Причины</span><span class="sxs-lookup"><span data-stu-id="0d8c7-116">Causes</span></span>**  

<span data-ttu-id="0d8c7-117">Слишком много запросов выполняется в одном домене.</span><span class="sxs-lookup"><span data-stu-id="0d8c7-117">Too many requests are being made on a single domain.</span></span>  <span data-ttu-id="0d8c7-118">Для подключений HTTP/1.0 или HTTP/1.1 Microsoft Edge допускает не более шести одновременных подключений TCP на одном узле.</span><span class="sxs-lookup"><span data-stu-id="0d8c7-118">On HTTP/1.0 or HTTP/1.1 connections, Microsoft Edge allows a maximum of six simultaneous TCP connections per host.</span></span>  

**<span data-ttu-id="0d8c7-119">Исправления</span><span class="sxs-lookup"><span data-stu-id="0d8c7-119">Fixes</span></span>**  

*   <span data-ttu-id="0d8c7-120">Реализуйте сегментирование доменов, если необходимо использовать HTTP/1.0 или HTTP/1.1.</span><span class="sxs-lookup"><span data-stu-id="0d8c7-120">Implement domain sharding if you must use HTTP/1.0 or HTTP/1.1.</span></span>  
*   <span data-ttu-id="0d8c7-121">Используйте HTTP/2.</span><span class="sxs-lookup"><span data-stu-id="0d8c7-121">Use HTTP/2.</span></span>  <span data-ttu-id="0d8c7-122">Не используйте сегментирование доменов с протоколом HTTP/2.</span><span class="sxs-lookup"><span data-stu-id="0d8c7-122">Do not use domain sharding with HTTP/2.</span></span>  
*   <span data-ttu-id="0d8c7-123">Удалите или отложите ненужные запросы, чтобы загрузить критические запросы.</span><span class="sxs-lookup"><span data-stu-id="0d8c7-123">Remove or defer unnecessary requests so that critical requests download earlier.</span></span>  
    
## <span data-ttu-id="0d8c7-124">Медленное время до первого байта (TTFB)</span><span class="sxs-lookup"><span data-stu-id="0d8c7-124">Slow Time To First Byte (TTFB)</span></span>   

**<span data-ttu-id="0d8c7-125">Симптомы</span><span class="sxs-lookup"><span data-stu-id="0d8c7-125">Symptoms</span></span>**  

<span data-ttu-id="0d8c7-126">Запрос тратит много времени на ожидание получения первого байта с сервера.</span><span class="sxs-lookup"><span data-stu-id="0d8c7-126">A request spends a long time waiting to receive the first byte from the server.</span></span>  

<span data-ttu-id="0d8c7-127">На рисунке ниже показана длинная зеленая полоса в **каскаде** , указывающая на то, что запрос был выполнен в течение длительного времени.</span><span class="sxs-lookup"><span data-stu-id="0d8c7-127">In the following figure, the long, green bar in the **Waterfall** indicates that the request was waiting a long time.</span></span>  <span data-ttu-id="0d8c7-128">Это было смоделировано с помощью профиля, ограничивающего скорость сети и добавляя задержку.</span><span class="sxs-lookup"><span data-stu-id="0d8c7-128">This was simulated using a profile to restrict network speed and add a delay.</span></span>  

:::image type="complex" source="../media/network-network-resources-using-dial-up-profile.msft.png" alt-text="Пример списка в очереди или остановленного ряда на панели &quot;сеть&quot;" lightbox="../media/network-network-resources-using-dial-up-profile.msft.png":::
   <span data-ttu-id="0d8c7-130">Пример запроса с медленным временем до получения первого байта</span><span class="sxs-lookup"><span data-stu-id="0d8c7-130">An example of a request with a slow Time To First Byte</span></span>  
:::image-end:::  

**<span data-ttu-id="0d8c7-131">Причины</span><span class="sxs-lookup"><span data-stu-id="0d8c7-131">Causes</span></span>**  

*   <span data-ttu-id="0d8c7-132">Соединение между клиентом и сервером происходит медленно.</span><span class="sxs-lookup"><span data-stu-id="0d8c7-132">The connection between the client and server is slow.</span></span>  
*   <span data-ttu-id="0d8c7-133">Скорость ответа сервера не отвечает.</span><span class="sxs-lookup"><span data-stu-id="0d8c7-133">The server is slow to respond.</span></span>  <span data-ttu-id="0d8c7-134">Разведите сервер на локальный компьютер, чтобы определить, является ли это подключение или медленный сервер.</span><span class="sxs-lookup"><span data-stu-id="0d8c7-134">Host the server locally to determine if it is the connection or server that is slow.</span></span>  <span data-ttu-id="0d8c7-135">Если вы по-прежнему получаете очень много времени на первый байт \ (TTFB \) при доступе к локальному серверу, сервер работает медленно.</span><span class="sxs-lookup"><span data-stu-id="0d8c7-135">If you still get a slow Time To First Byte \(TTFB\) when accessing a local server, then the server is slow.</span></span>  
    
**<span data-ttu-id="0d8c7-136">Исправления</span><span class="sxs-lookup"><span data-stu-id="0d8c7-136">Fixes</span></span>**  

*   <span data-ttu-id="0d8c7-137">Если соединение медленное, разрешите размещение содержимого в сети CDN или изменение поставщиков услуг размещения.</span><span class="sxs-lookup"><span data-stu-id="0d8c7-137">If the connection is slow, consider hosting your content on a CDN or changing hosting providers.</span></span>  
*   <span data-ttu-id="0d8c7-138">Если сервер работает медленно, рассматривайте запросы к базе данных, реализуйте кэш или изменяйте конфигурацию сервера.</span><span class="sxs-lookup"><span data-stu-id="0d8c7-138">If the server is slow, consider optimizing database queries, implementing a cache, or modifying your server configuration.</span></span>  
    
## <span data-ttu-id="0d8c7-139">Медленная загрузка содержимого</span><span class="sxs-lookup"><span data-stu-id="0d8c7-139">Slow content download</span></span>   

**<span data-ttu-id="0d8c7-140">Симптомы</span><span class="sxs-lookup"><span data-stu-id="0d8c7-140">Symptoms</span></span>**  

<span data-ttu-id="0d8c7-141">Загрузка запроса занимает много времени.</span><span class="sxs-lookup"><span data-stu-id="0d8c7-141">A request takes a long time to download.</span></span>  

<span data-ttu-id="0d8c7-142">На приведенном ниже рисунке показана длинная синяя полоса в **каскаде** рядом с форматом PNG, поэтому загрузка занимает много времени.</span><span class="sxs-lookup"><span data-stu-id="0d8c7-142">In the following figure, the long, blue bar in the **Waterfall** next to the png means it took a long time to download.</span></span>  

:::image type="complex" source="../media/network-network-resources-edge-devtools.msft.png" alt-text="Пример списка в очереди или остановленного ряда на панели &quot;сеть&quot;" lightbox="../media/network-network-resources-edge-devtools.msft.png":::
   <span data-ttu-id="0d8c7-144">Пример запроса, загрузка которого занимает много времени</span><span class="sxs-lookup"><span data-stu-id="0d8c7-144">An example of a request that takes a long time to download</span></span>  
:::image-end:::  

**<span data-ttu-id="0d8c7-145">Причины</span><span class="sxs-lookup"><span data-stu-id="0d8c7-145">Causes</span></span>**  

*   <span data-ttu-id="0d8c7-146">Соединение между клиентом и сервером происходит медленно.</span><span class="sxs-lookup"><span data-stu-id="0d8c7-146">The connection between the client and server is slow.</span></span>  
*   <span data-ttu-id="0d8c7-147">Загружается много контента.</span><span class="sxs-lookup"><span data-stu-id="0d8c7-147">A lot of content is being downloaded.</span></span>  
    
**<span data-ttu-id="0d8c7-148">Исправления</span><span class="sxs-lookup"><span data-stu-id="0d8c7-148">Fixes</span></span>**  

*   <span data-ttu-id="0d8c7-149">Возможно, вы размещаете содержимое в сети CDN или меняете поставщиков услуг размещения.</span><span class="sxs-lookup"><span data-stu-id="0d8c7-149">Consider hosting your content on a CDN or changing hosting providers.</span></span>  
*   <span data-ttu-id="0d8c7-150">Уменьшите количество байтов, оптимизируя запросы.</span><span class="sxs-lookup"><span data-stu-id="0d8c7-150">Send fewer bytes by optimizing your requests.</span></span>  
    
## <span data-ttu-id="0d8c7-151">Сведения о Contribute</span><span class="sxs-lookup"><span data-stu-id="0d8c7-151">Contribute knowledge</span></span>  

<span data-ttu-id="0d8c7-152">Есть ли у вас сетевая проблема, которая должна быть добавлена в это руководство?</span><span class="sxs-lookup"><span data-stu-id="0d8c7-152">Do you have a network issue that should be added to this guide?</span></span>  

*   <span data-ttu-id="0d8c7-153">Отправить твит на [@EdgeDevTools][MicrosoftEdgeTweet].</span><span class="sxs-lookup"><span data-stu-id="0d8c7-153">Send a tweet to [@EdgeDevTools][MicrosoftEdgeTweet].</span></span>  
*   <span data-ttu-id="0d8c7-154">Выберите **Отправить отзыв** \ ( ![ Отправить отзыв ][ImageSendFeedbackIcon] \) в DevTools или нажмите клавиши `Alt` + `Shift` + `I` \ (Windows \) или `Option` + `Shift` + `I` \ (macOS \), чтобы предоставить отзыв или запрос функций.</span><span class="sxs-lookup"><span data-stu-id="0d8c7-154">Select **Send Feedback** \(![Send Feedback][ImageSendFeedbackIcon]\) in the DevTools or press `Alt`+`Shift`+`I` \(Windows\) or `Option`+`Shift`+`I` \(macOS\) to provide feedback or feature requests.</span></span>  
*   <span data-ttu-id="0d8c7-155">[Открыть вопрос][WebFundamentalsIssue] в репозитории документов.</span><span class="sxs-lookup"><span data-stu-id="0d8c7-155">[Open an issue][WebFundamentalsIssue] on the docs repo.</span></span>  
    
<!--  
  


-->  

<!-- image links -->  

[ImageSendFeedbackIcon]: ../media/smile-icon.msft.png  

<!-- links -->  

[NetworkPerformance]: ./index.md "Проверка активности сети в Microsoft Edge DevTools | Документы Microsoft"  

[MicrosoftEdgeTweet]: https://twitter.com/intent/tweet?text=@EdgeDevTools%20[Network%20Issues%20Guide%20Suggestion]  

[WebFundamentalsIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=%5BDevTools%20Network%20Issues%20Guide%20Suggestion%5D "Новая ошибка — MicrosoftDocs/Edge-разработчик"  

> [!NOTE]
> <span data-ttu-id="0d8c7-158">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="0d8c7-158">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="0d8c7-159">Исходная страница размещается [здесь](https://developers.google.com/web/tools/chrome-devtools/network/issues) и разрабатывается с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \) и [Джонатан-искаженного][JonathanGarbee] (эксперта Google Developer, для Web Technology).</span><span class="sxs-lookup"><span data-stu-id="0d8c7-159">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/network/issues) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) and [Jonathan Garbee][JonathanGarbee] \(Google Developer Expert for Web Technology\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="0d8c7-161">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="0d8c7-161">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[JonathanGarbee]: https://developers.google.com/web/resources/contributors/jonathangarbee
