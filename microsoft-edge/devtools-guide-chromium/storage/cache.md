---
description: Инструкции по просмотру данных из кэша на панели приложения Microsoft Edge DevTools.
title: Просмотр данных кэша с помощью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 5ab5fd0b3b504443e495f1d5108907a4551e6ac6
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125442"
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

# <span data-ttu-id="40c7d-104">Просмотр данных кэша с помощью Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="40c7d-104">View cache data with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="40c7d-105">В этом руководстве описано, как использовать [Microsoft Edge DevTools][MicrosoftEdgeDevTools] для проверки данных [кэша][MDNCache] .</span><span class="sxs-lookup"><span data-stu-id="40c7d-105">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to inspect [Cache][MDNCache] data.</span></span>  

<span data-ttu-id="40c7d-106">Если вы пытаетесь проверить данные [кэша HTTP][MDNHTTPCaching] , это не значит, что вам нужно.</span><span class="sxs-lookup"><span data-stu-id="40c7d-106">If you are trying to inspect [HTTP cache][MDNHTTPCaching] data, this is not the guide you want.</span></span>  <span data-ttu-id="40c7d-107">Найдите данные в столбце " **Размер** " в **сетевом журнале**.</span><span class="sxs-lookup"><span data-stu-id="40c7d-107">Look for the information in the **Size** column of the **Network Log**.</span></span>  <span data-ttu-id="40c7d-108">Просмотр [журнала активности сети][DevtoolsNetworkLogActivity].</span><span class="sxs-lookup"><span data-stu-id="40c7d-108">See [Log network activity][DevtoolsNetworkLogActivity].</span></span>  

## <span data-ttu-id="40c7d-109">Просмотр данных кэша</span><span class="sxs-lookup"><span data-stu-id="40c7d-109">View cache data</span></span>  

1.  <span data-ttu-id="40c7d-110">Перейдите на вкладку **приложение** , чтобы открыть панель **приложения** .</span><span class="sxs-lookup"><span data-stu-id="40c7d-110">Select the **Application** tab to open the **Application** panel.</span></span>  <span data-ttu-id="40c7d-111">Обычно область **манифеста** открывается по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="40c7d-111">The **Manifest** pane usually opens by default.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-manifest.msft.png":::
       <span data-ttu-id="40c7d-113">Область « **Манифест** »</span><span class="sxs-lookup"><span data-stu-id="40c7d-113">The **Manifest** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="40c7d-114">Разверните раздел **хранилище кэша** , чтобы просмотреть доступные кэши.</span><span class="sxs-lookup"><span data-stu-id="40c7d-114">Expand the **Cache Storage** section to view available caches.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-cache-storage.msft.png":::
       <span data-ttu-id="40c7d-116">Доступные кэши</span><span class="sxs-lookup"><span data-stu-id="40c7d-116">Available caches</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="40c7d-117">Выберите кэш, чтобы просмотреть его содержимое.</span><span class="sxs-lookup"><span data-stu-id="40c7d-117">Select a cache to view the contents.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-root-headers.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-cache-storage-domain-root-headers.msft.png":::
       <span data-ttu-id="40c7d-119">Просмотр содержимого кэша</span><span class="sxs-lookup"><span data-stu-id="40c7d-119">View the contents of a cache</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="40c7d-120">Выберите ресурс для просмотра заголовков HTTP в разделе под таблицей.</span><span class="sxs-lookup"><span data-stu-id="40c7d-120">Select a resource to view the HTTP headers in the section below the table.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-index-headers.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-cache-storage-index-headers.msft.png":::
       <span data-ttu-id="40c7d-122">Просмотр заголовков HTTP для ресурса</span><span class="sxs-lookup"><span data-stu-id="40c7d-122">View the HTTP headers of a resource</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="40c7d-123">Нажмите кнопку **Предварительный просмотр** , чтобы просмотреть содержимое ресурса.</span><span class="sxs-lookup"><span data-stu-id="40c7d-123">Choose **Preview** to view the content of a resource.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-js-preview.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-cache-storage-domain-js-preview.msft.png":::
       <span data-ttu-id="40c7d-125">Просмотр содержимого ресурса</span><span class="sxs-lookup"><span data-stu-id="40c7d-125">View the content of a resource</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="40c7d-126">Обновление ресурса</span><span class="sxs-lookup"><span data-stu-id="40c7d-126">Refresh a resource</span></span>  

1.  <span data-ttu-id="40c7d-127">[Просмотр данных для кэша](#view-cache-data).</span><span class="sxs-lookup"><span data-stu-id="40c7d-127">[View the data for a cache](#view-cache-data).</span></span>  
1.  <span data-ttu-id="40c7d-128">Выберите ресурс, который вы хотите обновить.</span><span class="sxs-lookup"><span data-stu-id="40c7d-128">Select the resource that you want to refresh.</span></span>  <span data-ttu-id="40c7d-129">DevTools выделит ее, чтобы показать, что она выбрана.</span><span class="sxs-lookup"><span data-stu-id="40c7d-129">DevTools highlights it to indicate that it is selected.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-refresh.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-cache-storage-domain-refresh.msft.png":::
       <span data-ttu-id="40c7d-131">Выберите ресурс, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="40c7d-131">Select a resource to refresh</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="40c7d-132">Нажмите кнопку **Обновить** \ ( ![ обновить ][ImageRefreshIcon] \).</span><span class="sxs-lookup"><span data-stu-id="40c7d-132">Choose **Refresh** \(![Refresh][ImageRefreshIcon]\).</span></span>  
    
## <span data-ttu-id="40c7d-133">Фильтрация ресурсов</span><span class="sxs-lookup"><span data-stu-id="40c7d-133">Filter resources</span></span>  

1.  <span data-ttu-id="40c7d-134">[Просмотр данных для кэша](#view-cache-data).</span><span class="sxs-lookup"><span data-stu-id="40c7d-134">[View the data for a cache](#view-cache-data).</span></span>  
1.  <span data-ttu-id="40c7d-135">С помощью текстового поля **Фильтр по пути** можно отфильтровать ресурсы, которые не соответствуют указанному вами пути.</span><span class="sxs-lookup"><span data-stu-id="40c7d-135">Use the **Filter by Path** text box to filter out any resources that do not match the path that you provide.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-filter.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-cache-storage-filter.msft.png":::
       <span data-ttu-id="40c7d-137">Фильтрация ресурсов, не соответствующих указанному пути</span><span class="sxs-lookup"><span data-stu-id="40c7d-137">Filter out resources that do not match the specified path</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="40c7d-138">Удаление ресурса</span><span class="sxs-lookup"><span data-stu-id="40c7d-138">Delete a resource</span></span>  

1.  <span data-ttu-id="40c7d-139">[Просмотр данных для кэша](#view-cache-data).</span><span class="sxs-lookup"><span data-stu-id="40c7d-139">[View the data for a cache](#view-cache-data).</span></span>  
1.  <span data-ttu-id="40c7d-140">Выберите ресурс, который вы хотите удалить.</span><span class="sxs-lookup"><span data-stu-id="40c7d-140">Select the resource that you want to delete.</span></span>  <span data-ttu-id="40c7d-141">DevTools выделит ее, чтобы показать, что она выбрана.</span><span class="sxs-lookup"><span data-stu-id="40c7d-141">DevTools highlights it to indicate that it is selected.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-delete-selected.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-cache-storage-delete-selected.msft.png":::
       <span data-ttu-id="40c7d-143">Выберите ресурс для удаления</span><span class="sxs-lookup"><span data-stu-id="40c7d-143">Select a resource to delete</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="40c7d-144">Нажмите кнопку " **Удалить** ![ ", а затем "удалить выбрано ][ImageDeleteIcon] ".</span><span class="sxs-lookup"><span data-stu-id="40c7d-144">Choose **Delete Selected** \(![Delete Selected][ImageDeleteIcon]\).</span></span>  
    
## <span data-ttu-id="40c7d-145">Удаление всех данных из кэша</span><span class="sxs-lookup"><span data-stu-id="40c7d-145">Delete all cache data</span></span>  

1.  <span data-ttu-id="40c7d-146">Откройте **приложение**  >  , чтобы**Очистить хранилище**.</span><span class="sxs-lookup"><span data-stu-id="40c7d-146">Open **Application** > **Clear Storage**.</span></span>  
1.  <span data-ttu-id="40c7d-147">Убедитесь, что флажок **хранилище кэша** включен.</span><span class="sxs-lookup"><span data-stu-id="40c7d-147">Make sure that the **Cache Storage** checkbox is enabled.</span></span>  
    
    :::image type="complex" source="../media/storage-application-clear-storage-cache-storage-checkbox.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-clear-storage-cache-storage-checkbox.msft.png":::
       <span data-ttu-id="40c7d-149">Флажок " **хранилище кэша** "</span><span class="sxs-lookup"><span data-stu-id="40c7d-149">The **Cache Storage** checkbox</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="40c7d-150">Выберите команду **Очистить данные сайта**.</span><span class="sxs-lookup"><span data-stu-id="40c7d-150">Choose **Clear site data**.</span></span>  
    
    :::image type="complex" source="../media/storage-application-clear-storage-cache-storage-checkbox-clear-site-data-button.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-clear-storage-cache-storage-checkbox-clear-site-data-button.msft.png":::
       <span data-ttu-id="40c7d-152">Кнопка " **Очистить данные сайта** "</span><span class="sxs-lookup"><span data-stu-id="40c7d-152">The **Clear Site Data** button</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="40c7d-153">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="40c7d-153">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageDeleteIcon]: ../media/delete-icon.msft.png  
[ImageRefreshIcon]: ../media/refresh-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Инструменты разработчика Microsoft EDGE (Chromium) | Документы Microsoft"  
[DevtoolsNetworkLogActivity]: ../network/index.md#log-network-activity  "Регистрация активности в сети | Документы Microsoft"  

[MDNCache]: https://developer.mozilla.org/docs/Web/API/Cache "Кэш | MDN"  
[MDNHTTPCaching]: https://developer.mozilla.org/docs/Web/HTTP/Caching "Кэширование HTTP | MDN"  

> [!NOTE]
> <span data-ttu-id="40c7d-158">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="40c7d-158">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="40c7d-159">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/storage/cache) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="40c7d-159">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/cache) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="40c7d-161">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="40c7d-161">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
