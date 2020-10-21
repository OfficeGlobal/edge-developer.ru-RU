---
description: Учебник по наиболее распространенным функциям, связанным с сетью, в Microsoft Edge DevTools.
title: Проверка активности сети в Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: a55ff05e29817c483cbf13b8713ef37cf96424d5
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125428"
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

# <span data-ttu-id="46dbf-104">Проверка активности сети в Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="46dbf-104">Inspect network activity in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="46dbf-105">В этом практическом занятии описаны некоторые из наиболее часто используемых функций DevTools, связанных с проанализом активности сети для страницы.</span><span class="sxs-lookup"><span data-stu-id="46dbf-105">This is a hands-on tutorial of some of the most commonly-used DevTools features related to inspecting network activity for a page.</span></span>  

<span data-ttu-id="46dbf-106">Для просмотра функциональных возможностей используйте [ссылку сетевая ссылка][DevtoolsNetworkReference] .</span><span class="sxs-lookup"><span data-stu-id="46dbf-106">See [Network Reference][DevtoolsNetworkReference] if you want to browse features instead.</span></span>  

<!--TODO: This entire section needs a Microsoft Edge DevTools re-write  -->

<!-- Read on, or watch the video version of this tutorial:  -->  

<!--
> [!VIDEO embed/e1gAyQuIFQo]  
-->

## <span data-ttu-id="46dbf-107">Когда следует использовать панель "сеть"</span><span class="sxs-lookup"><span data-stu-id="46dbf-107">When to use the Network panel</span></span>  

<span data-ttu-id="46dbf-108">В общем случае следует использовать панель "сеть", чтобы убедиться в том, что ресурсы загружаются или загружаются должным образом.</span><span class="sxs-lookup"><span data-stu-id="46dbf-108">In general, use the Network panel when you need to make sure that resources are being downloaded or uploaded as expected.</span></span>  <span data-ttu-id="46dbf-109">Наиболее распространенными вариантами использования панели "сеть" являются:</span><span class="sxs-lookup"><span data-stu-id="46dbf-109">The most common use cases for the Network panel are:</span></span>  

*   <span data-ttu-id="46dbf-110">Убедитесь в том, что ресурсы действительно отправляются или загружаются вообще.</span><span class="sxs-lookup"><span data-stu-id="46dbf-110">Making sure that resources are actually being uploaded or downloaded at all.</span></span>  
*   <span data-ttu-id="46dbf-111">Проверка свойств отдельного ресурса, например HTTP-заголовков, содержимого, размера и т. д.</span><span class="sxs-lookup"><span data-stu-id="46dbf-111">Inspecting the properties of an individual resource, such as the HTTP headers, content, size, and so on.</span></span>  
    
<span data-ttu-id="46dbf-112">Если вы ищете способы повышения быстродействия загрузки страниц, **не** начинайте с панели "сеть".</span><span class="sxs-lookup"><span data-stu-id="46dbf-112">If you are looking for ways to improve page load performance, **do not** start with the Network panel.</span></span>  <span data-ttu-id="46dbf-113">Существует множество типов проблем с производительностью нагрузки, не связанных с работой сети.</span><span class="sxs-lookup"><span data-stu-id="46dbf-113">There are many types of load performance issues that are not related to network activity.</span></span>  <span data-ttu-id="46dbf-114">Начните работу с панели аудита, так как она содержит рекомендации по улучшению страницы.</span><span class="sxs-lookup"><span data-stu-id="46dbf-114">Start with the Audits panel because it gives you targeted suggestions on how to improve your page.</span></span>  <span data-ttu-id="46dbf-115">Ознакомьтесь со [скоростью оптимизации веб-сайта][DevtoolsSpeedGetStarted].</span><span class="sxs-lookup"><span data-stu-id="46dbf-115">See [Optimize Website Speed][DevtoolsSpeedGetStarted].</span></span>  

## <span data-ttu-id="46dbf-116">Открытие панели "сеть"</span><span class="sxs-lookup"><span data-stu-id="46dbf-116">Open the Network panel</span></span>  

<span data-ttu-id="46dbf-117">Чтобы максимально эффективно пользоваться этим учебником, откройте демонстрацию и ознакомьтесь с функциями на странице Demo.</span><span class="sxs-lookup"><span data-stu-id="46dbf-117">To get the most out of this tutorial, open up the demo and try out the features on the demo page.</span></span>  

1.  <span data-ttu-id="46dbf-118">Откройте [демонстрацию Приступая к работе][GlitchNetworkGetStarted].</span><span class="sxs-lookup"><span data-stu-id="46dbf-118">Open the [Get Started Demo][GlitchNetworkGetStarted].</span></span>  
    
    :::image type="complex" source="../media/network-glitch-inspect-network-activity-demo.msft.png" alt-text="Демонстрация" lightbox="../media/network-glitch-inspect-network-activity-demo.msft.png":::
       <span data-ttu-id="46dbf-120">Демонстрация</span><span class="sxs-lookup"><span data-stu-id="46dbf-120">The demo</span></span>  
    :::image-end:::  
    
    <!--You may prefer to move the demo to a separate window.  -->  
    
    <!--
    :::image type="complex" source="../media/network-tutorial/windows.msft.png" alt-text="Демонстрация" lightbox="../media/network-tutorial/windows.msft.png":::
       The demo in one window and this tutorial in a different window  
    :::image-end:::  
    -->
    
1.  <span data-ttu-id="46dbf-121">[Откройте DevTools][DevToolsOpen] , нажав клавиши `Control` + `Shift` + `J` \ (Windows, Linux \) или `Command` + `Option` + `J` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="46dbf-121">[Open DevTools][DevToolsOpen] by pressing `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\).</span></span>  <span data-ttu-id="46dbf-122">Откроется панель **консоли** .</span><span class="sxs-lookup"><span data-stu-id="46dbf-122">The **Console** panel opens.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-console.msft.png" alt-text="Демонстрация" lightbox="../media/network-glitch-console.msft.png":::
       <span data-ttu-id="46dbf-124">На **консоли**</span><span class="sxs-lookup"><span data-stu-id="46dbf-124">The **Console**</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="46dbf-125">Вы можете [закрепить DevTools в нижней части окна][DevToolsCustomizePlacement].</span><span class="sxs-lookup"><span data-stu-id="46dbf-125">You may prefer to [dock DevTools to the bottom of your window][DevToolsCustomizePlacement].</span></span>  
    
    :::image type="complex" source="../media/network-glitch-console-bottom.msft.png" alt-text="Демонстрация" lightbox="../media/network-glitch-console-bottom.msft.png":::
       <span data-ttu-id="46dbf-127">DevTools закреплено в нижней части окна</span><span class="sxs-lookup"><span data-stu-id="46dbf-127">DevTools docked to the bottom of the window</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="46dbf-128">Откройте вкладку **сеть** .  Откроется панель **Network (сеть** ).</span><span class="sxs-lookup"><span data-stu-id="46dbf-128">Select the **Network** tab.  The **Network** panel opens.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-bottom.msft.png" alt-text="Демонстрация" lightbox="../media/network-glitch-network-bottom.msft.png":::
       <span data-ttu-id="46dbf-130">Инструмент **консоли** в DevTools закрепленной в нижней части окна</span><span class="sxs-lookup"><span data-stu-id="46dbf-130">**Console** tool in the DevTools docked to the bottom of the window</span></span>  
    :::image-end:::  
    
<span data-ttu-id="46dbf-131">Прямо сейчас панель Network (сеть) пуста.</span><span class="sxs-lookup"><span data-stu-id="46dbf-131">Right now the Network panel is empty.</span></span>  <span data-ttu-id="46dbf-132">DevTools только записывает сетевые активности после того, как вы откроете ее и не произошел никаких сетевых операций после того, как вы открыли DevTools.</span><span class="sxs-lookup"><span data-stu-id="46dbf-132">DevTools only logs network activity after you open it and no network activity has occurred since you opened DevTools.</span></span>  

## <span data-ttu-id="46dbf-133">Регистрация активности в сети</span><span class="sxs-lookup"><span data-stu-id="46dbf-133">Log network activity</span></span>  

<span data-ttu-id="46dbf-134">Чтобы просмотреть сетевую активность, которая вызывается страницей, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="46dbf-134">To view the network activity that a page causes:</span></span>  

1.  <span data-ttu-id="46dbf-135">Перезагрузите страницу.</span><span class="sxs-lookup"><span data-stu-id="46dbf-135">Reload the page.</span></span>  <span data-ttu-id="46dbf-136">На панели Network (сеть) регистрируются все сетевые активности в **журнале сети**.</span><span class="sxs-lookup"><span data-stu-id="46dbf-136">The Network panel logs all network activity in the **Network Log**.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network.msft.png" alt-text="Демонстрация" lightbox="../media/network-glitch-network.msft.png":::
       <span data-ttu-id="46dbf-138">**Журнал сети**</span><span class="sxs-lookup"><span data-stu-id="46dbf-138">The **Network Log**</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="46dbf-139">Каждая строка **журнала сети** представляет ресурс.</span><span class="sxs-lookup"><span data-stu-id="46dbf-139">Each row of the **Network Log** represents a resource.</span></span>  <span data-ttu-id="46dbf-140">По умолчанию ресурсы указаны в хронологическом порядке.</span><span class="sxs-lookup"><span data-stu-id="46dbf-140">By default the resources are listed chronologically.</span></span>  <span data-ttu-id="46dbf-141">Самый верхний ресурс обычно является основным HTML-документом.</span><span class="sxs-lookup"><span data-stu-id="46dbf-141">The top resource is usually the main HTML document.</span></span>  <span data-ttu-id="46dbf-142">Самый нижний ресурс — это тот, который запрашивался последним.</span><span class="sxs-lookup"><span data-stu-id="46dbf-142">The bottom resource is whatever was requested last.</span></span>  
    
    <span data-ttu-id="46dbf-143">Каждый столбец представляет сведения о ресурсе.</span><span class="sxs-lookup"><span data-stu-id="46dbf-143">Each column represents information about a resource.</span></span>  <span data-ttu-id="46dbf-144">На приведенном выше рисунке отображаются столбцы по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="46dbf-144">In the previous figure the default columns are displayed.</span></span>  

    *   <span data-ttu-id="46dbf-145">**Состояние**.</span><span class="sxs-lookup"><span data-stu-id="46dbf-145">**Status**.</span></span>  <span data-ttu-id="46dbf-146">Код состояния HTTP для ответа.</span><span class="sxs-lookup"><span data-stu-id="46dbf-146">The HTTP status code for response.</span></span>  
    *   <span data-ttu-id="46dbf-147">**Тип**.</span><span class="sxs-lookup"><span data-stu-id="46dbf-147">**Type**.</span></span>  <span data-ttu-id="46dbf-148">Тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="46dbf-148">The resource type.</span></span>  
    *   <span data-ttu-id="46dbf-149">**Инициатор**.</span><span class="sxs-lookup"><span data-stu-id="46dbf-149">**Initiator**.</span></span>  <span data-ttu-id="46dbf-150">Причина запроса ресурса.</span><span class="sxs-lookup"><span data-stu-id="46dbf-150">The cause of the resource request.</span></span>  <span data-ttu-id="46dbf-151">При выборе ссылки в столбце инициатора осуществляется переход к исходному коду, вызвавшему запрос.</span><span class="sxs-lookup"><span data-stu-id="46dbf-151">Selecting a link in the Initiator column takes you to the source code that caused the request.</span></span>  
    *   <span data-ttu-id="46dbf-152">**Time (время**).</span><span class="sxs-lookup"><span data-stu-id="46dbf-152">**Time**.</span></span>  <span data-ttu-id="46dbf-153">Продолжительность запроса.</span><span class="sxs-lookup"><span data-stu-id="46dbf-153">The duration of the request.</span></span>  
    *   <span data-ttu-id="46dbf-154">**Каскадом**.</span><span class="sxs-lookup"><span data-stu-id="46dbf-154">**Waterfall**.</span></span>  <span data-ttu-id="46dbf-155">Графическое представление различных стадий запроса.</span><span class="sxs-lookup"><span data-stu-id="46dbf-155">A graphical representation of the different stages of the request.</span></span>  <span data-ttu-id="46dbf-156">Наведите указатель мыши на Каскад, чтобы увидеть разбивку.</span><span class="sxs-lookup"><span data-stu-id="46dbf-156">Hover over a Waterfall to see a breakdown.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="46dbf-157">Диаграмма, расположенная над сетевым журналом, называется обзором.</span><span class="sxs-lookup"><span data-stu-id="46dbf-157">The graph above the Network Log is called the Overview.</span></span>  <span data-ttu-id="46dbf-158">Вы не будете использовать граф обзора в этом учебнике, поэтому вы можете скрыть его.</span><span class="sxs-lookup"><span data-stu-id="46dbf-158">You will not use the Overview graph in this tutorial, so you may hide it.</span></span>  <span data-ttu-id="46dbf-159">Ознакомьтесь [со статьей скрыть область "Общие сведения"][DevtoolsReferenceHideOverview].</span><span class="sxs-lookup"><span data-stu-id="46dbf-159">See [Hide the Overview pane][DevtoolsReferenceHideOverview].</span></span>
    
1.  <span data-ttu-id="46dbf-160">После открытия DevTools записывает в журнал сети активность сети.</span><span class="sxs-lookup"><span data-stu-id="46dbf-160">After you open DevTools, it records network activity in the Network Log.</span></span>  
    <span data-ttu-id="46dbf-161">Чтобы продемонстрировать это, сначала ознакомьтесь с нижней частью **журнала сети** и запомните о том, что последнее действие будет заглянуть в эту оценку.</span><span class="sxs-lookup"><span data-stu-id="46dbf-161">To demonstrate this, first look at the bottom of the **Network Log** and make a mental note of the last activity.</span></span>  
1.  <span data-ttu-id="46dbf-162">Теперь нажмите кнопку " **получить данные** " в демонстрационной версии.</span><span class="sxs-lookup"><span data-stu-id="46dbf-162">Now, select the **Get Data** button in the demo.</span></span>  
1.  <span data-ttu-id="46dbf-163">Снова посмотрите на нижнюю часть **сетевого журнала** .</span><span class="sxs-lookup"><span data-stu-id="46dbf-163">Look at the bottom of the **Network Log** again.</span></span>  <span data-ttu-id="46dbf-164">Вы должны увидеть новый ресурс под названием "" `getstarted.json` .</span><span class="sxs-lookup"><span data-stu-id="46dbf-164">You should see a new resource called `getstarted.json`.</span></span>  <span data-ttu-id="46dbf-165">Нажатие кнопки " **получить данные** " привела к тому, что страница запрашивает этот файл.</span><span class="sxs-lookup"><span data-stu-id="46dbf-165">Selecting the **Get Data** button caused the page to request this file.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-new-resource.msft.png" alt-text="Демонстрация" lightbox="../media/network-glitch-network-new-resource.msft.png":::
       <span data-ttu-id="46dbf-167">Новый ресурс в **сетевом журнале**</span><span class="sxs-lookup"><span data-stu-id="46dbf-167">A new resource in the **Network Log**</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="46dbf-168">Показать дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="46dbf-168">Show more information</span></span>  

<span data-ttu-id="46dbf-169">Столбцы сетевого журнала можно настраивать.</span><span class="sxs-lookup"><span data-stu-id="46dbf-169">The columns of the Network Log are configurable.</span></span>  <span data-ttu-id="46dbf-170">Столбцы, которые вы не используете, могут быть скрыты.</span><span class="sxs-lookup"><span data-stu-id="46dbf-170">You may hide columns that you are not using.</span></span>  
<span data-ttu-id="46dbf-171">Кроме того, существует множество столбцов, которые по умолчанию скрыты, что может оказаться полезным.</span><span class="sxs-lookup"><span data-stu-id="46dbf-171">There are also many columns that are hidden by default which you may find useful.</span></span>  

1.  <span data-ttu-id="46dbf-172">Щелкните правой кнопкой мыши заголовок таблицы журнала сети и выберите команду **Domain (домен**).</span><span class="sxs-lookup"><span data-stu-id="46dbf-172">Right-click the header of the Network Log table and choose **Domain**.</span></span>  <span data-ttu-id="46dbf-173">Теперь отображается домен каждого ресурса.</span><span class="sxs-lookup"><span data-stu-id="46dbf-173">The domain of each resource is now shown.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-edit-column.msft.png" alt-text="Демонстрация" lightbox="../media/network-glitch-network-edit-column.msft.png":::
       <span data-ttu-id="46dbf-175">Включение столбца Domain (домен)</span><span class="sxs-lookup"><span data-stu-id="46dbf-175">Enable the Domain column</span></span>  
    :::image-end:::  
    
    > [!TIP]
    > <span data-ttu-id="46dbf-176">Просмотр полного URL-адреса ресурса при наведении указателя мыши на ячейку в столбце **имя** .</span><span class="sxs-lookup"><span data-stu-id="46dbf-176">See the full URL of a resource by hovering over the cell in the **Name** column.</span></span>  
    
## <span data-ttu-id="46dbf-177">Имитация медленных подключений к сети</span><span class="sxs-lookup"><span data-stu-id="46dbf-177">Simulate a slower network connection</span></span>  

<span data-ttu-id="46dbf-178">Сетевое подключение компьютера, используемого для создания сайтов, скорее всего быстрее, чем сетевые подключения мобильных устройств ваших пользователей.</span><span class="sxs-lookup"><span data-stu-id="46dbf-178">The network connection of the computer that you use to build sites is probably faster than the network connections of the mobile devices of your users.</span></span>  <span data-ttu-id="46dbf-179">Перетаскивая страницу, вы получите более общее представление о том, как долго страница будет загружаться на мобильном устройстве.</span><span class="sxs-lookup"><span data-stu-id="46dbf-179">By throttling the page, you get a better idea of how long a page takes to load on a mobile device.</span></span>  

1.  <span data-ttu-id="46dbf-180">Выберите раскрывающийся список **регулирования** , для которого по умолчанию установлено значение в **сети** .</span><span class="sxs-lookup"><span data-stu-id="46dbf-180">Select the **Throttling** dropdown, which is set to **Online** by default.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-throttling.msft.png" alt-text="Демонстрация" lightbox="../media/network-glitch-network-throttling.msft.png":::
       <span data-ttu-id="46dbf-182">Включение регулирования</span><span class="sxs-lookup"><span data-stu-id="46dbf-182">Enable throttling</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="46dbf-183">Выберите **медленное 3G**.</span><span class="sxs-lookup"><span data-stu-id="46dbf-183">Choose **Slow 3G**.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-throttling-slow-3g.msft.png" alt-text="Демонстрация" lightbox="../media/network-glitch-network-throttling-slow-3g.msft.png":::
       <span data-ttu-id="46dbf-185">Выбор медленной сети 3G</span><span class="sxs-lookup"><span data-stu-id="46dbf-185">Select Slow 3G</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="46dbf-186">Нажмите кнопку **перезагрузить** ![ ][ImageRefreshIcon] , а затем выберите **пустой кэш и принудительную перезагрузку**.</span><span class="sxs-lookup"><span data-stu-id="46dbf-186">Long-press **Reload** \(![Reload][ImageRefreshIcon]\) and then choose **Empty Cache And Hard Reload**.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-empty-cache-and-hard-reset.msft.png" alt-text="Демонстрация" lightbox="../media/network-glitch-empty-cache-and-hard-reset.msft.png":::
       **<span data-ttu-id="46dbf-188">Пустой кэш и окончательная перезагрузка</span><span class="sxs-lookup"><span data-stu-id="46dbf-188">Empty Cache And Hard Reload</span></span>**  
    :::image-end:::  
    
    <span data-ttu-id="46dbf-189">При повторном посещении браузер обычно обслуживает некоторые файлы из [кэша][MDNHTTPCache], что ускоряет загрузку страницы.</span><span class="sxs-lookup"><span data-stu-id="46dbf-189">On repeat visits, the browser usually serves some files from the [cache][MDNHTTPCache], which speeds up the page load.</span></span>  <span data-ttu-id="46dbf-190">**Пустой кэш, и при принудительной перезагрузке** браузер перейдет в сеть для всех ресурсов.</span><span class="sxs-lookup"><span data-stu-id="46dbf-190">**Empty Cache And Hard Reload** forces the browser to go the network for all resources.</span></span>  <span data-ttu-id="46dbf-191">Это полезно, если вы хотите узнать, как в первый раз происходит загрузка страницы посетителем.</span><span class="sxs-lookup"><span data-stu-id="46dbf-191">This is helpful when you want to see how a first-time visitor experiences a page load.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="46dbf-192">**Пустой кэш и рабочий процесс повторной загрузки** доступны только в том случае, если открыт DevTools.</span><span class="sxs-lookup"><span data-stu-id="46dbf-192">The **Empty Cache And Hard Reload** workflow is only available when DevTools is open.</span></span>  
    
## <span data-ttu-id="46dbf-193">Захват снимков экрана</span><span class="sxs-lookup"><span data-stu-id="46dbf-193">Capture screenshots</span></span>  

<span data-ttu-id="46dbf-194">С помощью снимков экрана можно увидеть, как страница была найдена во время загрузки.</span><span class="sxs-lookup"><span data-stu-id="46dbf-194">Screenshots let you see how a page looked over time while it was loading.</span></span>  

1.  <span data-ttu-id="46dbf-195">Выберите \ ( ![ Параметры сети ][ImageSettingsIcon] \) и установите флажок **захватить снимки экрана** .</span><span class="sxs-lookup"><span data-stu-id="46dbf-195">Select \(![Network settings][ImageSettingsIcon]\) and select the **Capture screenshots** checkbox.</span></span>
1.  <span data-ttu-id="46dbf-196">Снова загрузите страницу с помощью **пустого кэша и окончательной повторной загрузки** .</span><span class="sxs-lookup"><span data-stu-id="46dbf-196">Reload the page again via the **Empty Cache And Hard Reload** workflow.</span></span>  <span data-ttu-id="46dbf-197">Если вам нужно напоминание о том, как это сделать, ознакомьтесь [с](#simulate-a-slower-network-connection) разрешениями.</span><span class="sxs-lookup"><span data-stu-id="46dbf-197">See [Simulate a slower connection](#simulate-a-slower-network-connection) if you need a reminder on how to do this.</span></span>  
    <span data-ttu-id="46dbf-198">В области снимков экрана представлены эскизы того, как страница рассмотрелась на разных этапах процесса загрузки.</span><span class="sxs-lookup"><span data-stu-id="46dbf-198">The Screenshots pane provides thumbnails of how the page looked at various points during the loading process.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-screenshots.msft.png" alt-text="Демонстрация" lightbox="../media/network-glitch-network-screenshots.msft.png":::
       <span data-ttu-id="46dbf-200">Снимки экрана загрузки страницы</span><span class="sxs-lookup"><span data-stu-id="46dbf-200">Screenshots of the page load</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="46dbf-201">Выберите первый эскиз.</span><span class="sxs-lookup"><span data-stu-id="46dbf-201">Select the first thumbnail.</span></span>  <span data-ttu-id="46dbf-202">DevTools показывает, какая сетевая активность происходила в данный момент времени.</span><span class="sxs-lookup"><span data-stu-id="46dbf-202">DevTools shows you what network activity was occurring at that moment in time.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-screenshots-first.msft.png" alt-text="Демонстрация" lightbox="../media/network-glitch-network-screenshots-first.msft.png":::
       <span data-ttu-id="46dbf-204">Сетевая активность, происходящий на первом снимке экрана</span><span class="sxs-lookup"><span data-stu-id="46dbf-204">The network activity that was happening during the first screenshot</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="46dbf-205">Нажмите кнопку \ ( ![ Параметры сети ][ImageSettingsIcon] \) еще раз и снимите флажок **захватить снимки экрана** , чтобы закрыть область снимки экрана.</span><span class="sxs-lookup"><span data-stu-id="46dbf-205">Select \(![Network settings][ImageSettingsIcon]\) again and deselect the **Capture screenshots** checkbox to close the Screenshots pane.</span></span>
1.  <span data-ttu-id="46dbf-206">Повторно загрузите страницу.</span><span class="sxs-lookup"><span data-stu-id="46dbf-206">Reload the page again.</span></span>  
    
## <span data-ttu-id="46dbf-207">Проверка сведений о ресурсе</span><span class="sxs-lookup"><span data-stu-id="46dbf-207">Inspect the details of the resource</span></span>  

<span data-ttu-id="46dbf-208">Выберите ресурс, чтобы получить дополнительные сведения о нем.</span><span class="sxs-lookup"><span data-stu-id="46dbf-208">Select a resource to learn more information about it.</span></span>  <span data-ttu-id="46dbf-209">Попробуйте вот так:</span><span class="sxs-lookup"><span data-stu-id="46dbf-209">Try it now:</span></span>  

1.  <span data-ttu-id="46dbf-210">Выберите `getstarted.html` .</span><span class="sxs-lookup"><span data-stu-id="46dbf-210">Select `getstarted.html`.</span></span>  <span data-ttu-id="46dbf-211">Показана вкладка " **заголовки** ".</span><span class="sxs-lookup"><span data-stu-id="46dbf-211">The **Headers** tab is shown.</span></span>  <span data-ttu-id="46dbf-212">Используйте эту вкладку для проверки заголовков HTTP.</span><span class="sxs-lookup"><span data-stu-id="46dbf-212">Use this tab to inspect HTTP headers.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-resources-headers.msft.png" alt-text="Демонстрация" lightbox="../media/network-glitch-network-resources-headers.msft.png":::
       <span data-ttu-id="46dbf-214">Вкладка " **заголовки** "</span><span class="sxs-lookup"><span data-stu-id="46dbf-214">The **Headers** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="46dbf-215">Откройте вкладку **Предварительный просмотр** .  Отобразится основной рендеринг HTML-кода.</span><span class="sxs-lookup"><span data-stu-id="46dbf-215">Select the **Preview** tab.  A basic rendering of the HTML is shown.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-resources-preview.msft.png" alt-text="Демонстрация" lightbox="../media/network-glitch-network-resources-preview.msft.png":::
       <span data-ttu-id="46dbf-217">Вкладка " **Предварительный просмотр** "</span><span class="sxs-lookup"><span data-stu-id="46dbf-217">The **Preview** tab</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="46dbf-218">Эта вкладка полезна, если API возвращает код ошибки в HTML.</span><span class="sxs-lookup"><span data-stu-id="46dbf-218">This tab is helpful when an API returns an error code in HTML.</span></span>  <span data-ttu-id="46dbf-219">Возможно, вам будет проще прочитать обработанный HTML, чем исходный HTML-код или просматривает изображения.</span><span class="sxs-lookup"><span data-stu-id="46dbf-219">You may find it easier to read the rendered HTML than the HTML source code, or when you inspect images.</span></span>  

1.  <span data-ttu-id="46dbf-220">Откройте вкладку **ответ** .  Отобразится исходный код HTML.</span><span class="sxs-lookup"><span data-stu-id="46dbf-220">Select the **Response** tab.  The HTML source code is shown.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-resources-response.msft.png" alt-text="Демонстрация" lightbox="../media/network-glitch-network-resources-response.msft.png":::
       <span data-ttu-id="46dbf-222">Вкладка " **ответ** "</span><span class="sxs-lookup"><span data-stu-id="46dbf-222">The **Response** tab</span></span>  
    :::image-end:::  
    
    > [!TIP]
    > <span data-ttu-id="46dbf-223">Когда файл minified, при нажатии кнопки **Формат** \ ( ![ Формат ][ImageFormatIcon] \) в нижней части вкладки **ответа** повторно форматирует содержимое файла для чтения.</span><span class="sxs-lookup"><span data-stu-id="46dbf-223">When a file is minified, selecting the **Format** \(![Format][ImageFormatIcon]\) button at the bottom of the **Response** tab re-formats the contents of the file for readability.</span></span>  
    
1.  <span data-ttu-id="46dbf-224">Откройте вкладку **время** .  Показана сетевая подразделение активности для этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="46dbf-224">Select the **Timing** tab.  A breakdown of the network activity for this resource is shown.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-resources-timing.msft.png" alt-text="Демонстрация" lightbox="../media/network-glitch-network-resources-timing.msft.png":::
       <span data-ttu-id="46dbf-226">Вкладка **время**</span><span class="sxs-lookup"><span data-stu-id="46dbf-226">The **Timing** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="46dbf-227">**Close** ![ ][ImageCloseIcon] Чтобы снова просмотреть журнал сети, нажмите Закрыть (закрыть).</span><span class="sxs-lookup"><span data-stu-id="46dbf-227">Choose **Close** \(![Close][ImageCloseIcon]\) to view the Network Log again.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-resources-close-tabs.msft.png" alt-text="Демонстрация" lightbox="../media/network-glitch-network-resources-close-tabs.msft.png":::
       <span data-ttu-id="46dbf-229">Кнопка " **Закрыть** "</span><span class="sxs-lookup"><span data-stu-id="46dbf-229">The **Close** button</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="46dbf-230">Поиск заголовков и ответов в сети</span><span class="sxs-lookup"><span data-stu-id="46dbf-230">Search network headers and responses</span></span>  

<span data-ttu-id="46dbf-231">Используйте область **поиска** , если вам нужно найти заголовки HTTP и ответы по всем ресурсам для определенной строки или регулярного выражения.</span><span class="sxs-lookup"><span data-stu-id="46dbf-231">Use the **Search** pane when you need to search the HTTP headers and responses of all resources for a certain string or regular expression.</span></span>  

<span data-ttu-id="46dbf-232">Например, предположим, что вы хотите убедиться, что ваши ресурсы используют разумные **политики кэширования**.</span><span class="sxs-lookup"><span data-stu-id="46dbf-232">For example, suppose you want to verify that your resources are using reasonable **cache policies**.</span></span>  

<!--TODO: add cache policies section when available  -->

1.  <span data-ttu-id="46dbf-233">Нажмите **Поиск** \ ( ![ Поиск ][ImageSearchIcon] \).</span><span class="sxs-lookup"><span data-stu-id="46dbf-233">Choose **Search** \(![Search][ImageSearchIcon]\).</span></span>  <span data-ttu-id="46dbf-234">Область поиска откроется слева от сетевого журнала.</span><span class="sxs-lookup"><span data-stu-id="46dbf-234">The Search pane opens to the left of the Network log.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-search-empty.msft.png" alt-text="Демонстрация" lightbox="../media/network-glitch-network-search-empty.msft.png":::
       <span data-ttu-id="46dbf-236">Область " **Поиск** "</span><span class="sxs-lookup"><span data-stu-id="46dbf-236">The **Search** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="46dbf-237">Введите текст `Cache-Control` и выберите его `Enter` .</span><span class="sxs-lookup"><span data-stu-id="46dbf-237">Type `Cache-Control` and select `Enter`.</span></span>  <span data-ttu-id="46dbf-238">В области поиска перечислены все вхождения `Cache-Control` , найденные в заголовках или содержимом ресурсов.</span><span class="sxs-lookup"><span data-stu-id="46dbf-238">The Search pane lists all instances of `Cache-Control` that it finds in resource headers or content.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-search-cache-control.msft.png" alt-text="Демонстрация" lightbox="../media/network-glitch-network-search-cache-control.msft.png":::
       <span data-ttu-id="46dbf-240">Результаты поиска по запросу </span><span class="sxs-lookup"><span data-stu-id="46dbf-240">Search results for</span></span> `Cache-Control`  
    :::image-end:::  
    
1.  <span data-ttu-id="46dbf-241">Выберите результат, чтобы просмотреть ресурс, в котором был найден результат.</span><span class="sxs-lookup"><span data-stu-id="46dbf-241">Select a result to view the resource in which the result was found.</span></span>  <span data-ttu-id="46dbf-242">Если вы видите сведения о ресурсе, выберите результат, чтобы перейти непосредственно к нему.</span><span class="sxs-lookup"><span data-stu-id="46dbf-242">If you are looking at the details of the resource, select a result to go directly to it.</span></span>  <span data-ttu-id="46dbf-243">Например, если запрос был найден в заголовке, откроется вкладка Заголовки.</span><span class="sxs-lookup"><span data-stu-id="46dbf-243">For example, if the query was found in a header, the Headers tab opens.</span></span>   <span data-ttu-id="46dbf-244">Если запрос найден в содержимом, откроется вкладка **ответ** .</span><span class="sxs-lookup"><span data-stu-id="46dbf-244">If the query was found in content, the **Response** tab opens.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-search-cache-control-headers-response-headers.msft.png" alt-text="Демонстрация" lightbox="../media/network-glitch-network-search-cache-control-headers-response-headers.msft.png":::
       <span data-ttu-id="46dbf-246">Результат поиска, выделенный на вкладке " **заголовки** "</span><span class="sxs-lookup"><span data-stu-id="46dbf-246">A search result highlighted in the **Headers** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="46dbf-247">Закройте область поиска и вкладку заголовки.</span><span class="sxs-lookup"><span data-stu-id="46dbf-247">Close the Search pane and the Headers tab.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-search-close.msft.png" alt-text="Демонстрация" lightbox="../media/network-glitch-network-search-close.msft.png":::
       <span data-ttu-id="46dbf-249">Кнопки " **Закрыть** "</span><span class="sxs-lookup"><span data-stu-id="46dbf-249">The **Close** buttons</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="46dbf-250">Фильтрация ресурсов</span><span class="sxs-lookup"><span data-stu-id="46dbf-250">Filter resources</span></span>  

<span data-ttu-id="46dbf-251">DevTools предоставляет множество рабочих процессов для фильтрации ресурсов, не относящихся к поставленной задаче.</span><span class="sxs-lookup"><span data-stu-id="46dbf-251">DevTools provides numerous workflows for filtering out resources that are not relevant to the task at hand.</span></span>  

:::image type="complex" source="../media/network-glitch-network-filter-empty.msft.png" alt-text="Демонстрация" lightbox="../media/network-glitch-network-filter-empty.msft.png":::
   <span data-ttu-id="46dbf-253">Панель инструментов " **фильтры** "</span><span class="sxs-lookup"><span data-stu-id="46dbf-253">The **Filters** toolbar</span></span>  
:::image-end:::  

<span data-ttu-id="46dbf-254">Панель инструментов " **фильтры** " должна быть включена по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="46dbf-254">The **Filters** toolbar should be enabled by default.</span></span>  <span data-ttu-id="46dbf-255">Если не так:</span><span class="sxs-lookup"><span data-stu-id="46dbf-255">If not:</span></span>  

1.  <span data-ttu-id="46dbf-256">Щелкните **Фильтр** \ ( ![ фильтр ][ImageFilterIcon] \), чтобы отобразить его.</span><span class="sxs-lookup"><span data-stu-id="46dbf-256">Choose **Filter** \(![Filter][ImageFilterIcon]\) to show it.</span></span>  
    
### <span data-ttu-id="46dbf-257">Фильтрация по строке, регулярному выражению или свойству</span><span class="sxs-lookup"><span data-stu-id="46dbf-257">Filter by string, regular expression, or property</span></span>  

<span data-ttu-id="46dbf-258">Текстовое поле « **Фильтр** » поддерживает различные типы фильтрации.</span><span class="sxs-lookup"><span data-stu-id="46dbf-258">The **Filter** text box supports many different types of filtering.</span></span>  

1.  <span data-ttu-id="46dbf-259">Введите `png` текст в текстовое поле **Фильтр** .</span><span class="sxs-lookup"><span data-stu-id="46dbf-259">Type `png` into the **Filter** text box.</span></span>  <span data-ttu-id="46dbf-260">Отображаются только файлы, содержащие текст `png` .</span><span class="sxs-lookup"><span data-stu-id="46dbf-260">Only the files that contain the text `png` are shown.</span></span>  <span data-ttu-id="46dbf-261">В этом случае только файлы, соответствующие фильтру, являются изображениями в формате PNG.</span><span class="sxs-lookup"><span data-stu-id="46dbf-261">In this case the only files that match the filter are the PNG images.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-png.msft.png" alt-text="Демонстрация" lightbox="../media/network-glitch-network-filter-png.msft.png":::
       <span data-ttu-id="46dbf-263">Строковый фильтр</span><span class="sxs-lookup"><span data-stu-id="46dbf-263">A string filter</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="46dbf-264">Введите `/.*\.[cj]s+$/`.</span><span class="sxs-lookup"><span data-stu-id="46dbf-264">Type `/.*\.[cj]s+$/`.</span></span>  <span data-ttu-id="46dbf-265">DevTools отфильтровать все ресурсы с именем файла, которое не оканчивается на a, а `j` `c` затем с 1 или более `s` символами.</span><span class="sxs-lookup"><span data-stu-id="46dbf-265">DevTools filters out any resource with a filename that does not end with a `j` or a `c` followed by 1 or more `s` characters.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-regex.msft.png" alt-text="Демонстрация" lightbox="../media/network-glitch-network-filter-regex.msft.png":::
       <span data-ttu-id="46dbf-267">Фильтр регулярных выражений</span><span class="sxs-lookup"><span data-stu-id="46dbf-267">A regular expression filter</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="46dbf-268">Введите `-main.css`.</span><span class="sxs-lookup"><span data-stu-id="46dbf-268">Type `-main.css`.</span></span>  <span data-ttu-id="46dbf-269">DevTools отфильтровать `main.css` .</span><span class="sxs-lookup"><span data-stu-id="46dbf-269">DevTools filters out `main.css`.</span></span>  <span data-ttu-id="46dbf-270">Если какой – либо другой файл соответствует шаблону, он также будет исключен.</span><span class="sxs-lookup"><span data-stu-id="46dbf-270">If any other file matched the pattern they would also be filtered out.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-negative-statement.msft.png" alt-text="Демонстрация" lightbox="../media/network-glitch-network-filter-negative-statement.msft.png":::
       <span data-ttu-id="46dbf-272">Отрицательный фильтр</span><span class="sxs-lookup"><span data-stu-id="46dbf-272">A negative filter</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="46dbf-273">Введите `domain:cdn.glitch.com` текст в текстовое поле **Фильтр** .</span><span class="sxs-lookup"><span data-stu-id="46dbf-273">Type `domain:cdn.glitch.com` into the **Filter** text box.</span></span>  <span data-ttu-id="46dbf-274">DevTools отфильтровать все ресурсы с URL-адресом, который не соответствует этому домену.</span><span class="sxs-lookup"><span data-stu-id="46dbf-274">DevTools filters out any resource with a URL that does not match this domain.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-property-value.msft.png" alt-text="Демонстрация" lightbox="../media/network-glitch-network-filter-property-value.msft.png":::
       <span data-ttu-id="46dbf-276">Фильтр свойств</span><span class="sxs-lookup"><span data-stu-id="46dbf-276">A property filter</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="46dbf-277">Просмотрите [запросы фильтрации по свойствам][DevtoolsReferenceProperty] для полного списка фильтруемых свойств.</span><span class="sxs-lookup"><span data-stu-id="46dbf-277">See [Filter requests by properties][DevtoolsReferenceProperty] for the full list of filterable properties.</span></span>  
    
1.  <span data-ttu-id="46dbf-278">Очистите текстовое поле " **Фильтр** " в любом тексте.</span><span class="sxs-lookup"><span data-stu-id="46dbf-278">Clear the **Filter** text box of any text.</span></span>  
    
### <span data-ttu-id="46dbf-279">Фильтрация по типу ресурсов</span><span class="sxs-lookup"><span data-stu-id="46dbf-279">Filter by resource type</span></span>  

<span data-ttu-id="46dbf-280">Чтобы сосредоточиться на файле определенного типа, например в таблицах стилей, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="46dbf-280">To focus in on a certain type of file, such as stylesheets:</span></span>  

1.  <span data-ttu-id="46dbf-281">Выберите **CSS**.</span><span class="sxs-lookup"><span data-stu-id="46dbf-281">Choose **CSS**.</span></span>  <span data-ttu-id="46dbf-282">Все остальные типы файлов будут отфильтрованы.</span><span class="sxs-lookup"><span data-stu-id="46dbf-282">All other file types are filtered out.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-file-type-css.msft.png" alt-text="Демонстрация" lightbox="../media/network-glitch-network-filter-file-type-css.msft.png":::
       <span data-ttu-id="46dbf-284">Показывать только CSS – файлы</span><span class="sxs-lookup"><span data-stu-id="46dbf-284">Show CSS files only</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="46dbf-285">Чтобы также просмотреть сценарии, удерживайте клавишу `Control` \ (Windows, Linux \) или `Command` \ (macOS \), а затем выберите **JS**.</span><span class="sxs-lookup"><span data-stu-id="46dbf-285">To also see scripts, hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and then choose **JS**.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-file-type-css-js.msft.png" alt-text="Демонстрация" lightbox="../media/network-glitch-network-filter-file-type-css-js.msft.png":::
       <span data-ttu-id="46dbf-287">Показывать только файлы CSS и JS</span><span class="sxs-lookup"><span data-stu-id="46dbf-287">Show CSS and JS files only</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="46dbf-288">Нажмите кнопку **все** , чтобы удалить фильтры и снова просмотреть все ресурсы.</span><span class="sxs-lookup"><span data-stu-id="46dbf-288">Choose **All** to remove the filters and see all resources again.</span></span>  
    
<span data-ttu-id="46dbf-289">Просмотр [запросов фильтрации][DevtoolsNetworkReferenceFilter] для других рабочих процессов фильтрации.</span><span class="sxs-lookup"><span data-stu-id="46dbf-289">See [Filter requests][DevtoolsNetworkReferenceFilter] for other filtering workflows.</span></span>  

## <span data-ttu-id="46dbf-290">Блокировать запросы</span><span class="sxs-lookup"><span data-stu-id="46dbf-290">Block requests</span></span>  

<span data-ttu-id="46dbf-291">Как выглядит и работает страница при недоступности некоторых ресурсов страницы?</span><span class="sxs-lookup"><span data-stu-id="46dbf-291">How does a page look and behave when some of the page resources are not available?</span></span>  <span data-ttu-id="46dbf-292">Не удается полностью завершить его или он по-прежнему работает?</span><span class="sxs-lookup"><span data-stu-id="46dbf-292">Does it fail completely, or is it still somewhat functional?</span></span>  <span data-ttu-id="46dbf-293">Блокировка запросов на определение:</span><span class="sxs-lookup"><span data-stu-id="46dbf-293">Block requests to find out:</span></span>  

1.  <span data-ttu-id="46dbf-294">Выберите `Control` + `Shift` + `P` \ (Windows, Linux \) или `Command` + `Shift` + `P` \ (macOS \), чтобы открыть **меню команд**.</span><span class="sxs-lookup"><span data-stu-id="46dbf-294">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-cli-empty.msft.png" alt-text="Демонстрация" lightbox="../media/network-glitch-network-cli-empty.msft.png":::
       <span data-ttu-id="46dbf-296">**Меню команд**</span><span class="sxs-lookup"><span data-stu-id="46dbf-296">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="46dbf-297">Введите `block` команду **Показать блокировку запросов**и нажмите кнопку `Enter` .</span><span class="sxs-lookup"><span data-stu-id="46dbf-297">Type `block`, choose **Show Request Blocking**, and select `Enter`.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-cli-block.msft.png" alt-text="Демонстрация" lightbox="../media/network-glitch-network-cli-block.msft.png":::
       **<span data-ttu-id="46dbf-299">Показать блокировку запросов</span><span class="sxs-lookup"><span data-stu-id="46dbf-299">Show Request Blocking</span></span>**  
    :::image-end:::  
    
1.  <span data-ttu-id="46dbf-300">Нажмите кнопку **Добавить узор** \ ( ![ Добавить шаблон ][ImageAddIcon] \).</span><span class="sxs-lookup"><span data-stu-id="46dbf-300">Choose **Add Pattern** \(![Add Pattern][ImageAddIcon]\).</span></span>  
1.  <span data-ttu-id="46dbf-301">Введите `main.css`.</span><span class="sxs-lookup"><span data-stu-id="46dbf-301">Type `main.css`.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-cli-block-add-pattern.msft.png" alt-text="Демонстрация" lightbox="../media/network-glitch-network-cli-block-add-pattern.msft.png":::
       <span data-ttu-id="46dbf-303">Снижающи</span><span class="sxs-lookup"><span data-stu-id="46dbf-303">Blocking</span></span> `main.css`  
    :::image-end:::  
    
1.  <span data-ttu-id="46dbf-304">Нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="46dbf-304">Choose **Add**.</span></span>  
1.  <span data-ttu-id="46dbf-305">Перезагрузите страницу.</span><span class="sxs-lookup"><span data-stu-id="46dbf-305">Reload the page.</span></span>  <span data-ttu-id="46dbf-306">Как и предполагалось, стиль страницы немного изменился, так как основная таблица стилей заблокирована.</span><span class="sxs-lookup"><span data-stu-id="46dbf-306">As expected, the styling of the page is slightly messed up because the main stylesheet has been blocked.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="46dbf-307">`main.css`Строка в сетевом журнале.</span><span class="sxs-lookup"><span data-stu-id="46dbf-307">The `main.css` row in the Network Log.</span></span>  <span data-ttu-id="46dbf-308">Красный текст означает, что ресурс заблокирован.</span><span class="sxs-lookup"><span data-stu-id="46dbf-308">The red text means that the resource was blocked.</span></span>
    
    :::image type="complex" source="../media/network-glitch-network-cli-block-main-css.msft.png" alt-text="Демонстрация" lightbox="../media/network-glitch-network-cli-block-main-css.msft.png":::
       `main.css` <span data-ttu-id="46dbf-310">заблокирован</span><span class="sxs-lookup"><span data-stu-id="46dbf-310">has been blocked</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="46dbf-311">Снимите флажок **включить блокировку запросов** .</span><span class="sxs-lookup"><span data-stu-id="46dbf-311">Deselect the **Enable request blocking** checkbox.</span></span>  

## <span data-ttu-id="46dbf-312">Заключение</span><span class="sxs-lookup"><span data-stu-id="46dbf-312">Conclusion</span></span>  

<span data-ttu-id="46dbf-313">Поздравляем, вы завершили обучение.</span><span class="sxs-lookup"><span data-stu-id="46dbf-313">Congratulations, you have completed the tutorial.</span></span>  <span data-ttu-id="46dbf-314">Теперь вы знаете, как использовать панель " **сеть** " в Microsoft Edge DevTools!</span><span class="sxs-lookup"><span data-stu-id="46dbf-314">You now know how to use the **Network** panel in the Microsoft Edge DevTools!</span></span>

<span data-ttu-id="46dbf-315">Перейдите по [ссылке Network (сеть][DevtoolsNetworkReference] ), чтобы найти другие функции DevTools, связанные с проанализом активности сети.</span><span class="sxs-lookup"><span data-stu-id="46dbf-315">Navigate to the [Network Reference][DevtoolsNetworkReference] to discover more DevTools features related to inspecting network activity.</span></span>  

## <span data-ttu-id="46dbf-316">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="46dbf-316">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageAddIcon]: ../media/add-icon.msft.png  
[ImageCloseIcon]: ../media/close-icon.msft.png  
[ImageFilterIcon]: ../media/filter-icon.msft.png  
[ImageFormatIcon]: ../media/format-icon.msft.png  
[ImageRefreshIcon]: ../media/refresh-icon.msft.png  
[ImageScreenshotsIcon]: ../media/screenshots-icon.msft.png  
[ImageSearchIcon]: ../media/search-icon.msft.png  
[ImageSettingsIcon]: ../media/settings-icon.msft.png

<!-- links -->  

<!--[CachePolicies]: ../../../web/tools/lighthouse/audits/cache-policy ""  -->  

[DevToolsCustomizePlacement]: ../customize/placement.md "Изменение положения Microsoft Edge DevTools | Документы Microsoft"  
[DevtoolsNetworkReference]: ./reference.md "Справка по анализу сети | Документы Microsoft"
[DevtoolsNetworkReferenceFilter]: ./reference.md#filter-requests "Запросы фильтрации — Справочник по анализу сети | Документы Microsoft"  
[DevtoolsReferenceHideOverview]: ./reference.md#hide-the-overview-pane "Скрыть область обзора — Справка по анализу сети | Документы Microsoft"
[DevtoolsReferenceProperty]: ./reference.md#filter-requests-by-properties "Фильтрация запросов по свойствам-Справка по анализу сети | Документы Microsoft"
[DevToolsOpen]: ../open.md "Открыть Microsoft Edge DevTools | Документы Microsoft"  
[DevtoolsSpeedGetStarted]: ../speed/get-started.md "Оптимизация скорости веб-сайта с помощью Microsoft Edge DevTools | Документы Microsoft"  

[GlitchNetworkGetStarted]: https://microsoft-edge-chromium-devtools.glitch.me/static/network/getstarted.html "Пример проверки активности сети | Цепь"  

[MDNHTTPCache]: https://developer.mozilla.org/docs/Web/HTTP/Caching "Кэширование HTTP | MDN"  

> [!NOTE]
> <span data-ttu-id="46dbf-326">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="46dbf-326">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="46dbf-327">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/network/index) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="46dbf-327">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/network/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="46dbf-329">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="46dbf-329">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
