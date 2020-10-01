---
description: Упорядочивайте ресурсы по кадрам, доменам, типам и другим критериям.
title: Просмотр ресурсов страницы с помощью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 4f90927cc4044c722d9a62ab4b0427aa2753e4c5
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993592"
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





# <span data-ttu-id="27834-104">Просмотр ресурсов страницы с помощью Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="27834-104">View page resources with Microsoft Edge DevTools</span></span>   

  

<span data-ttu-id="27834-105">В этом руководстве рассказывается, как использовать Microsoft Edge DevTools для просмотра ресурсов веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="27834-105">This guide teaches you how to use Microsoft Edge DevTools to view the resources of a web page.</span></span>  <span data-ttu-id="27834-106">Ресурсы — это файлы, необходимые для правильного отображения страницы.</span><span class="sxs-lookup"><span data-stu-id="27834-106">Resources are the files that a page needs in order to display correctly.</span></span>  <span data-ttu-id="27834-107">Примеры ресурсов включают CSS, JavaScript и HTML-файлы, а также изображения.</span><span class="sxs-lookup"><span data-stu-id="27834-107">Examples of resources include CSS, JavaScript, and HTML files, as well as images.</span></span>  

<span data-ttu-id="27834-108">В этом руководстве предполагается, что вы знакомы с основами [веб-разработки][MDNLearnWebDevelopment] и [Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span><span class="sxs-lookup"><span data-stu-id="27834-108">This guide assumes that you are familiar with the basics of [web development][MDNLearnWebDevelopment] and [Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span></span>  

## <span data-ttu-id="27834-109">Открытие ресурсов</span><span class="sxs-lookup"><span data-stu-id="27834-109">Open resources</span></span>   

<span data-ttu-id="27834-110">Если вы знаете имя ресурса, который вы хотите проверить, **меню команд** предоставляет быстрый способ открытия ресурса.</span><span class="sxs-lookup"><span data-stu-id="27834-110">When you know the name of the resource that you want to inspect, the **Command Menu** provides a fast way of opening the resource.</span></span>  

1.  <span data-ttu-id="27834-111">Нажмите клавиши `Control` + `P` \ (Windows \) или `Command` + `P` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="27834-111">Press `Control`+`P` \(Windows\) or `Command`+`P` \(macOS\).</span></span>  <span data-ttu-id="27834-112">Откроется диалоговое окно **Открытие файла** .</span><span class="sxs-lookup"><span data-stu-id="27834-112">The **Open File** dialog opens.</span></span>  
    
    :::image type="complex" source="../media/resources-command-menu-empty.msft.png" alt-text="Диалоговое окно «Открытие файла»" lightbox="../media/resources-command-menu-empty.msft.png":::
       <span data-ttu-id="27834-114">Диалоговое окно « **Открытие файла** »</span><span class="sxs-lookup"><span data-stu-id="27834-114">The **Open File** dialog</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="27834-115">Выберите файл из раскрывающегося списка или введите имя файла и нажмите `Enter` один раз, чтобы выделить его в поле "Автозаполнение".</span><span class="sxs-lookup"><span data-stu-id="27834-115">Select the file from the dropdown, or start typing the filename and press `Enter` once the correct file is highlighted in the autocomplete box.</span></span>  
    
    :::image type="complex" source="../media/resources-command-menu-file-search.msft.png" alt-text="Диалоговое окно «Открытие файла»" lightbox="../media/resources-command-menu-file-search.msft.png":::
       <span data-ttu-id="27834-117">Введите имя файла в диалоговом окне " **Открытие файла** "</span><span class="sxs-lookup"><span data-stu-id="27834-117">Type a filename in the **Open File** dialog</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="27834-118">Открытие ресурсов на панели "сеть"</span><span class="sxs-lookup"><span data-stu-id="27834-118">Open resources in the Network panel</span></span>   

<span data-ttu-id="27834-119">Ознакомьтесь [с подробными сведениями о ресурсе][DevtoolsNetworkInspectDetailsResource].</span><span class="sxs-lookup"><span data-stu-id="27834-119">See [Inspect the details of a resource][DevtoolsNetworkInspectDetailsResource].</span></span>  

:::image type="complex" source="../media/resources-network-response.msft.png" alt-text="Диалоговое окно «Открытие файла»" lightbox="../media/resources-network-response.msft.png":::
   <span data-ttu-id="27834-121">Проверка ресурса на панели " **сеть** "</span><span class="sxs-lookup"><span data-stu-id="27834-121">Inspect a resource in the **Network** panel</span></span>  
:::image-end:::  

### <span data-ttu-id="27834-122">Показать ресурсы на панели "сеть" с других панелей</span><span class="sxs-lookup"><span data-stu-id="27834-122">Reveal resources in the Network panel from other panels</span></span>   

<span data-ttu-id="27834-123">В разделе [Обзор ресурсов](#browse-resources) ниже показано, как просматривать ресурсы из различных частей пользовательского интерфейса DevTools.</span><span class="sxs-lookup"><span data-stu-id="27834-123">The [Browse resources](#browse-resources) section below shows you how to view resources from various parts of the DevTools UI.</span></span>  <span data-ttu-id="27834-124">Если вы когда-нибудь хотите просмотреть ресурс на панели **сеть** , щелкните ресурс правой кнопкой мыши и выберите пункт **Показать на панели "сеть**".</span><span class="sxs-lookup"><span data-stu-id="27834-124">If you ever want to inspect a resource in the **Network** panel, right-click the resource and select **Reveal in Network panel**.</span></span>  

:::image type="complex" source="../media/resources-sources-page-reveal-in-network-panel.msft.png" alt-text="Диалоговое окно «Открытие файла»" lightbox="../media/resources-sources-page-reveal-in-network-panel.msft.png":::
   **<span data-ttu-id="27834-126">Панель "Показать в сети"</span><span class="sxs-lookup"><span data-stu-id="27834-126">Reveal in Network panel</span></span>**  
:::image-end:::  

## <span data-ttu-id="27834-127">Просмотр ресурсов</span><span class="sxs-lookup"><span data-stu-id="27834-127">Browse resources</span></span>   

### <span data-ttu-id="27834-128">Просмотр ресурсов на панели «Сеть»</span><span class="sxs-lookup"><span data-stu-id="27834-128">Browse resources in the Network panel</span></span>   

<span data-ttu-id="27834-129">Просмотр [журнала активности сети][DevtoolsNetworkLogActivity].</span><span class="sxs-lookup"><span data-stu-id="27834-129">See [Log network activity][DevtoolsNetworkLogActivity].</span></span>  

:::image type="complex" source="../media/resources-network-resources.msft.png" alt-text="Диалоговое окно «Открытие файла»" lightbox="../media/resources-network-resources.msft.png":::
   <span data-ttu-id="27834-131">Ресурсы страницы в журнале **сети**</span><span class="sxs-lookup"><span data-stu-id="27834-131">Page resources in the **Network** Log</span></span>  
:::image-end:::  

### <span data-ttu-id="27834-132">Просмотр по каталогу</span><span class="sxs-lookup"><span data-stu-id="27834-132">Browse by directory</span></span>   

<span data-ttu-id="27834-133">Чтобы просмотреть ресурсы на странице, упорядоченные по каталогу, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="27834-133">To view the resources of a page organized by directory:</span></span>  

1.  <span data-ttu-id="27834-134">Перейдите на вкладку **источники** , чтобы открыть панель " **источники** ".</span><span class="sxs-lookup"><span data-stu-id="27834-134">Click the **Sources** tab to open the **Sources** panel.</span></span>  
1.  <span data-ttu-id="27834-135">Щелкните вкладку **страницы** , чтобы показать ресурсы страницы.</span><span class="sxs-lookup"><span data-stu-id="27834-135">Click the **Page** tab to show the resources of the page.</span></span>  <span data-ttu-id="27834-136">Откроется область **страница** .</span><span class="sxs-lookup"><span data-stu-id="27834-136">The **Page** pane opens.</span></span>  
    
    :::image type="complex" source="../media/resources-sources-page-empty.msft.png" alt-text="Диалоговое окно «Открытие файла»" lightbox="../media/resources-sources-page-empty.msft.png":::
       <span data-ttu-id="27834-138">Область **страницы**</span><span class="sxs-lookup"><span data-stu-id="27834-138">The **Page** pane</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="27834-139">Ниже приведено разделение неочевидных элементов на предыдущем рисунке.</span><span class="sxs-lookup"><span data-stu-id="27834-139">Here is a breakdown of the non-obvious items in the previous figure.</span></span>  
    
    | <span data-ttu-id="27834-140">Элемент страницы</span><span class="sxs-lookup"><span data-stu-id="27834-140">Page item</span></span> | <span data-ttu-id="27834-141">Описание</span><span class="sxs-lookup"><span data-stu-id="27834-141">Description</span></span> |  
    |:--- |:--- |  
    | `top` | <span data-ttu-id="27834-142">Основной [контекст обзора][MDNInlineFrame]документов.</span><span class="sxs-lookup"><span data-stu-id="27834-142">The main document [browsing context][MDNInlineFrame].</span></span> |  
    | `airhorner.com` | <span data-ttu-id="27834-143">Домен.</span><span class="sxs-lookup"><span data-stu-id="27834-143">The domain.</span></span>  <span data-ttu-id="27834-144">Все ресурсы, вложенные в него, поступают из этого домена.</span><span class="sxs-lookup"><span data-stu-id="27834-144">All resources nested under it come from that domain.</span></span>  <span data-ttu-id="27834-145">Например, может быть задан полный URL-адрес `comlink.global.j` файла `https://airhorner.com/scripts/comlink.global.js` .</span><span class="sxs-lookup"><span data-stu-id="27834-145">For example, the full URL of the `comlink.global.j` file is probably `https://airhorner.com/scripts/comlink.global.js`.</span></span> |  
    | `scripts` | <span data-ttu-id="27834-146">Каталог.</span><span class="sxs-lookup"><span data-stu-id="27834-146">A directory.</span></span> |  
    | `(index)` | <span data-ttu-id="27834-147">Основной HTML-документ.</span><span class="sxs-lookup"><span data-stu-id="27834-147">The main HTML document.</span></span> |  
    | `sw.js` | <span data-ttu-id="27834-148">Контекст среды выполнения рабочего процесса службы.</span><span class="sxs-lookup"><span data-stu-id="27834-148">A service worker runtime context.</span></span> |  
    
1.  <span data-ttu-id="27834-149">Щелкните ресурс, чтобы просмотреть его в **редакторе**.</span><span class="sxs-lookup"><span data-stu-id="27834-149">Click a resource to view it in the **Editor**.</span></span>  
    
    :::image type="complex" source="../media/resources-sources-page-resource.msft.png" alt-text="Диалоговое окно «Открытие файла»" lightbox="../media/resources-sources-page-resource.msft.png":::
       <span data-ttu-id="27834-151">Просмотр файла в **редакторе**</span><span class="sxs-lookup"><span data-stu-id="27834-151">View a file in the **Editor**</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="27834-152">Просмотр по имени файла</span><span class="sxs-lookup"><span data-stu-id="27834-152">Browse by filename</span></span>   

<span data-ttu-id="27834-153">По умолчанию в области **страницы** ресурсы группируются по каталогам.</span><span class="sxs-lookup"><span data-stu-id="27834-153">By default the **Page** pane groups resources by directory.</span></span>  <span data-ttu-id="27834-154">Чтобы отключить эту группировку и просмотреть ресурсы для каждого домена в виде плоского списка, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="27834-154">To disable this grouping and view the resources for each domain as a flat list:</span></span>  

1.  <span data-ttu-id="27834-155">Открытие области **страницы** .</span><span class="sxs-lookup"><span data-stu-id="27834-155">Open the **Page** pane.</span></span>  <span data-ttu-id="27834-156">Просмотр [по каталогу](#browse-by-directory).</span><span class="sxs-lookup"><span data-stu-id="27834-156">See [Browse by directory](#browse-by-directory).</span></span>  
1.  <span data-ttu-id="27834-157">Нажмите кнопку **Дополнительные параметры** `...` и отключите функцию **Группировка по папкам**.</span><span class="sxs-lookup"><span data-stu-id="27834-157">Click **More Options** `...` and disable **Group By Folder**.</span></span>  
    
    :::image type="complex" source="../media/resources-sources-page-resource-group-by-folder.msft.png" alt-text="Диалоговое окно «Открытие файла»" lightbox="../media/resources-sources-page-resource-group-by-folder.msft.png":::
       <span data-ttu-id="27834-159">Параметр **Группировка по папке**</span><span class="sxs-lookup"><span data-stu-id="27834-159">The **Group By Folder** option</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="27834-160">Ресурсы упорядочены по типам файлов.</span><span class="sxs-lookup"><span data-stu-id="27834-160">Resources are organized by file type.</span></span>  <span data-ttu-id="27834-161">В каждом типе файла ресурсы упорядочены по алфавиту.</span><span class="sxs-lookup"><span data-stu-id="27834-161">Within each file type the resources are organized alphabetically.</span></span>  
    
    :::image type="complex" source="../media/resources-sources-page-resources-empty-not-grouped-by-folder.msft.png" alt-text="Диалоговое окно «Открытие файла»" lightbox="../media/resources-sources-page-resources-empty-not-grouped-by-folder.msft.png":::
       <span data-ttu-id="27834-163">Область **страницы** после отключения **группировки по папке**</span><span class="sxs-lookup"><span data-stu-id="27834-163">The **Page** pane after disabling **Group By Folder**</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="27834-164">Просмотр по типу файла</span><span class="sxs-lookup"><span data-stu-id="27834-164">Browse by file type</span></span>   

<span data-ttu-id="27834-165">Чтобы сгруппировать ресурсы в зависимости от типа файла:</span><span class="sxs-lookup"><span data-stu-id="27834-165">To group resources together based on their file type:</span></span>  

1.  <span data-ttu-id="27834-166">Откройте вкладку **приложение** .  Откроется панель **приложения** .</span><span class="sxs-lookup"><span data-stu-id="27834-166">Click the **Application** tab.  The **Application** panel opens.</span></span>  <span data-ttu-id="27834-167">По умолчанию область **манифеста** обычно открывается в первую очередь.</span><span class="sxs-lookup"><span data-stu-id="27834-167">By default the **Manifest** pane usually opens first.</span></span>  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner.msft.png" alt-text="Диалоговое окно «Открытие файла»" lightbox="../media/resources-application-mainfest-airhorner.msft.png":::
       <span data-ttu-id="27834-169">Панель **приложения**</span><span class="sxs-lookup"><span data-stu-id="27834-169">The **Application** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="27834-170">Прокрутите страницу вниз до области **рамок** .</span><span class="sxs-lookup"><span data-stu-id="27834-170">Scroll down to the **Frames** pane.</span></span>  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner-frames-expanded.msft.png" alt-text="Диалоговое окно «Открытие файла»" lightbox="../media/resources-application-mainfest-airhorner-frames-expanded.msft.png":::
       <span data-ttu-id="27834-172">Область **рамок**</span><span class="sxs-lookup"><span data-stu-id="27834-172">The **Frames** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="27834-173">Разверните разделы, в которых вы заинтересованы.</span><span class="sxs-lookup"><span data-stu-id="27834-173">Expand the sections in which you are interested.</span></span>  
1.  <span data-ttu-id="27834-174">Щелкните ресурс, чтобы просмотреть его.</span><span class="sxs-lookup"><span data-stu-id="27834-174">Click a resource to view it.</span></span>  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner-expanded-resources.msft.png" alt-text="Диалоговое окно «Открытие файла»" lightbox="../media/resources-application-mainfest-airhorner-expanded-resources.msft.png":::
       <span data-ttu-id="27834-176">Просмотр ресурса на панели « **приложение** »</span><span class="sxs-lookup"><span data-stu-id="27834-176">View a resource in the **Application** panel</span></span>  
    :::image-end:::  
    
#### <span data-ttu-id="27834-177">Просмотр файлов по типу на панели «Сеть»</span><span class="sxs-lookup"><span data-stu-id="27834-177">Browse files by type in the Network panel</span></span>   

<span data-ttu-id="27834-178">Просмотреть [Фильтр по типу ресурсов][DevtoolsNetworkFilterByResourceType].</span><span class="sxs-lookup"><span data-stu-id="27834-178">See [Filter by resource type][DevtoolsNetworkFilterByResourceType].</span></span>  

:::image type="complex" source="../media/resources-network-resources-filter-css.msft.png" alt-text="Диалоговое окно «Открытие файла»" lightbox="../media/resources-network-resources-filter-css.msft.png":::
   <span data-ttu-id="27834-180">Фильтр для CSS в **сетевом** журнале</span><span class="sxs-lookup"><span data-stu-id="27834-180">Filter for CSS in the **Network** Log</span></span>  
:::image-end:::  

<!--  
  


-->  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Инструменты разработчика Microsoft EDGE (Chromium) | Документы Microsoft"  
[DevtoolsNetworkFilterByResourceType]: ../network/index.md#filter-by-resource-type "Фильтрация по типу ресурсов: Проверка активности сети в Microsoft Edge DevTools | Документы Microsoft"  
[DevtoolsNetworkInspectDetailsResource]: ../network/index.md#inspect-the-details-of-the-resource "Просмотрите сведения об активности в сети для проверки ресурсов в Microsoft Edge DevTools | Документы Microsoft"  
[DevtoolsNetworkLogActivity]: ../network/index.md#log-network-activity "Регистрация активности сети — проверка активности сети в Microsoft Edge DevTools | Документы Microsoft"  

[MDNInlineFrame]: https://developer.mozilla.org/docs/Web/HTML/Element/iframe "<> IFRAME: элемент встроенной рамки | MDN"  
[MDNLearnWebDevelopment]: https://developer.mozilla.org/docs/Learn "Знакомство с веб-разработкой | MDN"  

> [!NOTE]
> <span data-ttu-id="27834-187">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="27834-187">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="27834-188">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/resources/index) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="27834-188">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/resources/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="27834-190">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="27834-190">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
