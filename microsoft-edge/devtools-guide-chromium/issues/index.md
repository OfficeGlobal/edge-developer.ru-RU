---
title: Поиск и устранение проблем с помощью средства Microsoft Edge DevTools "вопросы"
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: bad9e9d99f0d2f3179784920fc334823289b9f99
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/02/2020
ms.locfileid: "10992822"
---
<!-- Copyright Sam Dutton 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  

# <span data-ttu-id="73a4d-103">Поиск и устранение проблем с помощью средства Microsoft Edge DevTools "вопросы"</span><span class="sxs-lookup"><span data-stu-id="73a4d-103">Find and fix problems with the Microsoft Edge DevTools Issues tool</span></span>  

<span data-ttu-id="73a4d-104">Инструмент " **вопросы** " в Microsoft Edge DevTools сокращает усталость уведомлений и бессрочные элементы **консоли**.</span><span class="sxs-lookup"><span data-stu-id="73a4d-104">The **Issues** tool in Microsoft Edge DevTools reduces the notification fatigue and clutter of the **Console**.</span></span>  <span data-ttu-id="73a4d-105">Используйте его для поиска решений проблем, обнаруженных браузером, например проблем с файлами cookie и смешанного содержимого.</span><span class="sxs-lookup"><span data-stu-id="73a4d-105">Use it to find solutions to problems detected by the browser, such as cookie issues and mixed content.</span></span>  

> [!NOTE]
> <span data-ttu-id="73a4d-106">В Microsoft Edge 84 средство " **проблемы** " поддерживает три типа проблемы:</span><span class="sxs-lookup"><span data-stu-id="73a4d-106">In Microsoft Edge 84, the **Issues** tool supports three types of issue:</span></span>  
> *   [<span data-ttu-id="73a4d-107">Проблемы с cookie-файлами</span><span class="sxs-lookup"><span data-stu-id="73a4d-107">Cookie problems</span></span>][MDNSameSiteCookies]  
> *   [<span data-ttu-id="73a4d-108">Смешанное содержимое</span><span class="sxs-lookup"><span data-stu-id="73a4d-108">Mixed content</span></span>][MDNMixedContent]  
> *   [<span data-ttu-id="73a4d-109">Проблемы с COEP</span><span class="sxs-lookup"><span data-stu-id="73a4d-109">COEP issues</span></span>][W3CCOEPSpec]
> 
> <span data-ttu-id="73a4d-110">Планы Microsoft Edge DevTools Teams, чтобы поддерживать дополнительные типы проблем в будущих версиях Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="73a4d-110">The Microsoft Edge DevTools team plans to support more issue types in future versions of Microsoft Edge.</span></span>  

## <span data-ttu-id="73a4d-111">Открытие инструмента "проблемы" в ящике DevTools</span><span class="sxs-lookup"><span data-stu-id="73a4d-111">Open the Issues tool in the DevTools drawer</span></span>  

1.  <span data-ttu-id="73a4d-112">Посетите страницу, например [SameSite-Sandbox.glitch.Me][GlitchSamesiteSandbox], которая включает проблемы, которые необходимо устранить.</span><span class="sxs-lookup"><span data-stu-id="73a4d-112">Visit a page, such as [samesite-sandbox.glitch.me][GlitchSamesiteSandbox], that contains issues to fix.</span></span>  
1.  <span data-ttu-id="73a4d-113">[Откройте DevTools][DevtoolsOpen].</span><span class="sxs-lookup"><span data-stu-id="73a4d-113">[Open DevTools][DevtoolsOpen].</span></span>  
1.  :::row:::
       :::column span="":::
          <span data-ttu-id="73a4d-114">Нажмите кнопку **Перейти к разделу "проблемы** " на желтой панели предупреждения.</span><span class="sxs-lookup"><span data-stu-id="73a4d-114">Select the **Go to Issues** button in the yellow warning bar.</span></span>  
          
          :::image type="complex" source="../media/issues-open-issues-tab.msft.png" alt-text="Нажатие кнопки &quot;проблемы&quot; на желтой полосе предупреждения при обнаружении проблем" lightbox="../media/issues-open-issues-tab.msft.png":::
             <span data-ttu-id="73a4d-116">Кнопка **Перейти к проблемам** на желтой полосе предупреждения при обнаружении проблем.</span><span class="sxs-lookup"><span data-stu-id="73a4d-116">The **Go to Issues** button in the yellow warning bar when Issues are detected.</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          <span data-ttu-id="73a4d-117">Кроме того, можно выбрать пункт " **проблемы** " в меню " **другие инструменты** ".</span><span class="sxs-lookup"><span data-stu-id="73a4d-117">Alternatively, select **Issues** from the **More tools** menu.</span></span>  
          
          :::image type="complex" source="../media//issues-more-tools-menu.msft.png" alt-text="Нажатие кнопки &quot;проблемы&quot; на желтой полосе предупреждения при обнаружении проблем" lightbox="../media//issues-more-tools-menu.msft.png":::
             <span data-ttu-id="73a4d-119">Средство " **вопросы** " в меню " **другие инструменты** "</span><span class="sxs-lookup"><span data-stu-id="73a4d-119">**Issues** tool in **More tools** menu</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
1.  <span data-ttu-id="73a4d-120">При необходимости нажмите кнопку **перезагрузить страницу** .</span><span class="sxs-lookup"><span data-stu-id="73a4d-120">Select the **Reload page** button, if necessary.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-before-refresh.msft.png" alt-text="Нажатие кнопки &quot;проблемы&quot; на желтой полосе предупреждения при обнаружении проблем" lightbox="../media/issues-tab-before-refresh.msft.png":::
       <span data-ttu-id="73a4d-122">Инструмент " **проблемы** " в DevTools ящике с кнопкой " **перезагрузить страницу** "</span><span class="sxs-lookup"><span data-stu-id="73a4d-122">**Issues** tool in the DevTools Drawer with **Reload page** button</span></span>  
    :::image-end:::  

    <span data-ttu-id="73a4d-123">Проблемы, обнаруженные в **консоли** , довольно сложно понять, например предупреждения о cookie-файлах на рисунке ниже.</span><span class="sxs-lookup"><span data-stu-id="73a4d-123">The issues reported in the **Console** are quite hard to understand, such as the cookie warnings in the following image.</span></span>  <span data-ttu-id="73a4d-124">На основе обнаруженных проблем может быть не ясно, что необходимо сделать.</span><span class="sxs-lookup"><span data-stu-id="73a4d-124">Based upon the reported issues, it may not be clear what you must do.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-after-refresh.msft.png" alt-text="Нажатие кнопки &quot;проблемы&quot; на желтой полосе предупреждения при обнаружении проблем" lightbox="../media/issues-tab-after-refresh.msft.png":::
       <span data-ttu-id="73a4d-126">Инструмент " **проблемы** " в денежном ящике DevTools с тремя неполадками с файлами cookie</span><span class="sxs-lookup"><span data-stu-id="73a4d-126">**Issues** tool in the DevTools Drawer with three cookie issues</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="73a4d-127">Просмотр элементов в инструменте "проблемы"</span><span class="sxs-lookup"><span data-stu-id="73a4d-127">View items in the Issues tool</span></span>  

<span data-ttu-id="73a4d-128">Инструмент " **проблемы** " в ящике DevTools представляет предупреждения в структурированных, агрегатных и возможных действиях.</span><span class="sxs-lookup"><span data-stu-id="73a4d-128">The **Issues** tool in the DevTools Drawer presents warnings in a structured, aggregated, and actionable way.</span></span>  

1.  <span data-ttu-id="73a4d-129">Выберите элемент в инструменте " **вопросы** ", чтобы получить инструкции по устранению проблемы и поиску затронутых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="73a4d-129">Select an item in the **Issues** tool to get guidance on how to fix the issue and find affected resources.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-issue-open.msft.png" alt-text="Нажатие кнопки &quot;проблемы&quot; на желтой полосе предупреждения при обнаружении проблем" lightbox="../media/issues-tab-issue-open.msft.png":::
       <span data-ttu-id="73a4d-131">**Пометка cookie-файлов другого сайта как безопасной проблемы при** открытии в инструменте " **вопросы** "</span><span class="sxs-lookup"><span data-stu-id="73a4d-131">**Mark cross-site cookies as Secure** issue open in the **Issues** tool</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="73a4d-132">Каждый элемент состоит из четырех компонентов:</span><span class="sxs-lookup"><span data-stu-id="73a4d-132">Each item has four components:</span></span>  
    
    *   <span data-ttu-id="73a4d-133">Заголовок, описывающий эту ошибку.</span><span class="sxs-lookup"><span data-stu-id="73a4d-133">A headline describing the issue.</span></span>  
    *   <span data-ttu-id="73a4d-134">Описание, предоставляющее контекст и решение.</span><span class="sxs-lookup"><span data-stu-id="73a4d-134">A description providing the context and the solution.</span></span>  
    *   <span data-ttu-id="73a4d-135">Раздел " **уязвимые ресурсы** ", который содержит ссылки на ресурсы в соответствующем DevTools контексте, например на панели "сеть".</span><span class="sxs-lookup"><span data-stu-id="73a4d-135">An **AFFECTED RESOURCES** section that links to resources within the appropriate DevTools context such as the Network panel.</span></span>  
    *   <span data-ttu-id="73a4d-136">Ссылки на другие инструкции.</span><span class="sxs-lookup"><span data-stu-id="73a4d-136">Links to further guidance.</span></span>  
    
1.  <span data-ttu-id="73a4d-137">Чтобы просмотреть подробные сведения, выберите элементы в **затронутых ресурсах** .</span><span class="sxs-lookup"><span data-stu-id="73a4d-137">Select items in **AFFECTED RESOURCES** to view details.</span></span>  <span data-ttu-id="73a4d-138">В следующем примере **cookie-файлы межсайтового сайта как безопасные** вопросы влияют на один файл cookie и два запроса.</span><span class="sxs-lookup"><span data-stu-id="73a4d-138">In the following example, the **Mark cross-site cookies as Secure** issue affects one cookie and two requests.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-affected-resources.msft.png" alt-text="Нажатие кнопки &quot;проблемы&quot; на желтой полосе предупреждения при обнаружении проблем" lightbox="../media/issues-tab-affected-resources.msft.png":::
       <span data-ttu-id="73a4d-140">Затронутые ресурсы, открытые в инструменте " **вопросы** " в ящике DevTools</span><span class="sxs-lookup"><span data-stu-id="73a4d-140">Affected resources open in the **Issues** tool in the DevTools Drawer</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="73a4d-141">Просмотр проблем в контексте</span><span class="sxs-lookup"><span data-stu-id="73a4d-141">View issues in context</span></span>  

1.  <span data-ttu-id="73a4d-142">Выберите ссылку на ресурс, чтобы просмотреть элемент в соответствующем контексте в DevTools.</span><span class="sxs-lookup"><span data-stu-id="73a4d-142">Select a resource link to view the item in the appropriate context within DevTools.</span></span>  <span data-ttu-id="73a4d-143">В следующем примере выберите `samesite-sandbox.glitch.me` в разделе **запросы** для отображения файлов cookie, вложенных в запрос.</span><span class="sxs-lookup"><span data-stu-id="73a4d-143">In the following example, select `samesite-sandbox.glitch.me` under **Requests** to show the cookies attached to that request.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-view-request.msft.png" alt-text="Нажатие кнопки &quot;проблемы&quot; на желтой полосе предупреждения при обнаружении проблем" lightbox="../media/issues-tab-view-request.msft.png":::
       <span data-ttu-id="73a4d-145">Просмотр затрагиваемого cookie-файла на панели DevTools **Network**</span><span class="sxs-lookup"><span data-stu-id="73a4d-145">View the affected cookie in the DevTools **Network** panel</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="73a4d-146">Прокрутите экран, чтобы просмотреть элемент с проблемой: в следующем примере показан `ck02` объект cookie.</span><span class="sxs-lookup"><span data-stu-id="73a4d-146">Scroll to view the item with a problem: for the following example, the `ck02` cookie.</span></span>  <span data-ttu-id="73a4d-147">Наведите указатель мыши на столбец **SameSite** , чтобы увидеть `None` значение, которое обнаружено проблемой.</span><span class="sxs-lookup"><span data-stu-id="73a4d-147">Hover over the **SameSite** column to see the `None` value that the issue detected.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-view-issue.msft.png" alt-text="Нажатие кнопки &quot;проблемы&quot; на желтой полосе предупреждения при обнаружении проблем" lightbox="../media/issues-tab-view-issue.msft.png":::
       `None` <span data-ttu-id="73a4d-149">значение в столбце " **SameSite** " для `ck02` файла cookie на панели DevTools **Network (сеть** )</span><span class="sxs-lookup"><span data-stu-id="73a4d-149">value in the **SameSite** column for the `ck02` cookie in the DevTools **Network** panel</span></span>  
    :::image-end:::  

## <span data-ttu-id="73a4d-150">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="73a4d-150">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsOpen]: ../open.md "Открыть Microsoft Edge DevTools | Документы Microsoft"  

[GlitchSamesiteSandbox]: https://samesite-sandbox.glitch.me "Проверка файлов cookie SameSite | Цепь"  

[MDNSameSiteCookies]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie/SameSite "SameSite cookie-файлы | MDN"  
[MDNMixedContent]: https://developer.mozilla.org/docs/Web/Security/Mixed_content "Смешанное содержимое | MDN"  

[W3CCOEPSpec]: https://wicg.github.io/cross-origin-embedder-policy "Политика внедрения для разных источников | Группа сообщества веб-Incubator"  

> [!NOTE]
> <span data-ttu-id="73a4d-156">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="73a4d-156">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="73a4d-157">Исходная страница [будет найдена, и](https://developers.google.com/web/tools/chrome-devtools/issues/index) ее можно создать с помощью [SAM Dutton][SamDutton] \ (разработчик отвечает \).</span><span class="sxs-lookup"><span data-stu-id="73a4d-157">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/issues/index) and is authored by [Sam Dutton][SamDutton] \(Developer Advocate\).</span></span>  
[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="73a4d-159">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="73a4d-159">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[SamDutton]: https://developers.google.com/web/resources/contributors/samdutton  
