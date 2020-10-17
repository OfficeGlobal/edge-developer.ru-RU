---
description: Узнайте о том, как обновить расширение с манифеста v2 на v3
title: Подготовка к обновлению расширений из манифеста v2 в v3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/13/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-Chromium, Разработка расширений, расширения EDGE, расширения для браузеров, надстройки, разработчик, манифест v3, миграция в манифест v3
ms.openlocfilehash: 262a5cab54dd23f596791c93ec1238619e247333
ms.sourcegitcommit: 1ad087b00df16fd7718a5d95226de57e29b335e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/14/2020
ms.locfileid: "11117833"
---
# <span data-ttu-id="a28bd-104">Подготовка к обновлению расширений из манифеста v2 в v3</span><span class="sxs-lookup"><span data-stu-id="a28bd-104">Prepare to update your extensions from Manifest v2 to v3</span></span> 

<span data-ttu-id="a28bd-105">В этом документе перечислены важные изменения, реализуемые в рамках манифеста v3, который является следующей версией платформы расширений Chromium.</span><span class="sxs-lookup"><span data-stu-id="a28bd-105">This document lists important changes that's being implemented as part of Manifest v3, which is the next version of the Chromium Extensions platform.</span></span> <span data-ttu-id="a28bd-106">В ходе реализации мы будем обновлять этот документ.</span><span class="sxs-lookup"><span data-stu-id="a28bd-106">We'll update this document as the implementation progresses.</span></span> <span data-ttu-id="a28bd-107">Подробное руководство по переносу расширения на манифест v3 можно найти в разделе [Миграция на манифест v3][Google_Migrate_to_MV3].</span><span class="sxs-lookup"><span data-stu-id="a28bd-107">For detailed guidance on migrating your extension to Manifest v3, navigate to [Migrating to Manifest V3][Google_Migrate_to_MV3].</span></span> 

## <span data-ttu-id="a28bd-108">Удаленно размещенный код</span><span class="sxs-lookup"><span data-stu-id="a28bd-108">Remotely hosted code</span></span>  

<span data-ttu-id="a28bd-109">Сегодня расширения могут размещать части кода в удаленном режиме, а не включать их в пакет расширения во время проверки.</span><span class="sxs-lookup"><span data-stu-id="a28bd-109">Today, extensions can host parts of their code remotely, and not include it as part of the extension package during the validation process.</span></span> <span data-ttu-id="a28bd-110">Несмотря на то что это обеспечивает гибкость для изменения кода без повторной отправки расширения в магазин, этот код можно использовать после установки.</span><span class="sxs-lookup"><span data-stu-id="a28bd-110">While this offers flexibility to change code without resubmitting the extension to the store, the code can be exploited after installation.</span></span> <span data-ttu-id="a28bd-111">Чтобы убедиться в том, что [надстройки Microsoft Edge][EdgeAddons] имеют проверенные расширения, мы не допускайте использование удаленно управляемого кода расширениями.</span><span class="sxs-lookup"><span data-stu-id="a28bd-111">To ensure [Microsoft Edge Add-ons][EdgeAddons] lists validated extensions, we're disallowing extensions from using remotely hosted code.</span></span> <span data-ttu-id="a28bd-112">Это изменение повышает безопасность расширений.</span><span class="sxs-lookup"><span data-stu-id="a28bd-112">This change makes extensions more secure.</span></span> <span data-ttu-id="a28bd-113">Разработчикам потребуется упаковать и отправить весь код, который используется расширением для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="a28bd-113">Developers will need to package and submit all code that's used by the extension for validation.</span></span> <span data-ttu-id="a28bd-114">Кроме того, разработчики могут использовать функцию eval () в [изолированной среде][sandboxingEval].</span><span class="sxs-lookup"><span data-stu-id="a28bd-114">Alternatively, developers can use the eval() function in a [sandboxed environment][sandboxingEval].</span></span> 

## <span data-ttu-id="a28bd-115">Разрешения узла во время выполнения</span><span class="sxs-lookup"><span data-stu-id="a28bd-115">Run-time host permissions</span></span>  

<span data-ttu-id="a28bd-116">В процессе установки расширения могут запросить общие разрешения на доступ ко всем сайтам и контенту.</span><span class="sxs-lookup"><span data-stu-id="a28bd-116">At installation time, extensions may request blanket permissions to access all sites and content.</span></span> <span data-ttu-id="a28bd-117">Эти разрешения разрешают расширениям работу с минимальным вмешательством и создают риск для обеспечения конфиденциальности и безопасности пользователей.</span><span class="sxs-lookup"><span data-stu-id="a28bd-117">These permissions allow extensions to operate with minimum intervention, and create a risk to user privacy and security.</span></span> <span data-ttu-id="a28bd-118">Для улучшения прозрачности мы предоставляем пользователям элементы управления для разрешения или ограничения доступа к веб-сайтам во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="a28bd-118">To improve transparency, we're providing controls for users to allow or restrict access to websites at runtime.</span></span> 

## <span data-ttu-id="a28bd-119">Запросы между источниками в сценариях содержимого</span><span class="sxs-lookup"><span data-stu-id="a28bd-119">Cross-origin requests in content scripts</span></span>  

<span data-ttu-id="a28bd-120">Сегодня сценарии контента могут запросить доступ к любой происхождению, в том числе к источникам, которые не разрешены на веб-сайте.</span><span class="sxs-lookup"><span data-stu-id="a28bd-120">Today content scripts can request access to any origin including origins that aren't allowed by the website.</span></span> <span data-ttu-id="a28bd-121">Это поведение разбивается на источники, которые не являются принципами.</span><span class="sxs-lookup"><span data-stu-id="a28bd-121">This behavior breaks cross-origin principles.</span></span> <span data-ttu-id="a28bd-122">После пересылки вам понадобятся сценарии содержимого, чтобы иметь те же разрешения, что и страница, в которую они были добавлены, и закрыв потенциальные loophole безопасности.</span><span class="sxs-lookup"><span data-stu-id="a28bd-122">Going forward, we'll require content scripts to have the same permissions as the page they're injected into, closing a potential security loophole.</span></span> <span data-ttu-id="a28bd-123">Для выполнения запросов между источниками необходимо использовать фоновые сценарии для ретрансляции ответов на сценарии содержимого.</span><span class="sxs-lookup"><span data-stu-id="a28bd-123">To perform cross-origin requests, you'll need to use background scripts to relay responses back to content scripts.</span></span> <span data-ttu-id="a28bd-124">Эти изменения доступны и отстает от отметки.</span><span class="sxs-lookup"><span data-stu-id="a28bd-124">These changes are available and behind a flag.</span></span> <span data-ttu-id="a28bd-125">Для получения дополнительных сведений перейдите к этому [документу][CORS].</span><span class="sxs-lookup"><span data-stu-id="a28bd-125">For more information, navigate to this [document][CORS].</span></span> 

## <span data-ttu-id="a28bd-126">API веб-запросов</span><span class="sxs-lookup"><span data-stu-id="a28bd-126">Web Request API</span></span>  

<span data-ttu-id="a28bd-127">Мы заменяем [API веб-запросов][WebRequestAPI] на [ДЕКЛАРАТИВНЫЙ сетевой интерфейс API][DeclarativeNetRequestAPI], но продолжат отслеживать возможности наблюдения для веб-запросов.</span><span class="sxs-lookup"><span data-stu-id="a28bd-127">We're replacing [Web Request API][WebRequestAPI] with [Declarative Net Request API][DeclarativeNetRequestAPI], but will continue to keep Web Request API's observational capabilities.</span></span> <span data-ttu-id="a28bd-128">За исключением некоторых конкретных ситуаций, в которых для расширения необходимы возможности API веб-запросов, рекомендуется использовать только API DNR.</span><span class="sxs-lookup"><span data-stu-id="a28bd-128">Except in some specific scenarios where observational capabilities of the Web Request API are required by the extension, we recommend using the DNR APIs only.</span></span> <span data-ttu-id="a28bd-129">Мы считаем, что это изменение повлияет на расширения, которые используют сложные декларативные возможности.</span><span class="sxs-lookup"><span data-stu-id="a28bd-129">We believe this change will have positive impact on extensions that use feature-rich declarative capabilities.</span></span> <span data-ttu-id="a28bd-130">Как и в случае с дополнительными расширениями API DNR, это изменение улучшит конфиденциальность пользователей, которое способствует повышению уровня доверия при использовании расширений.</span><span class="sxs-lookup"><span data-stu-id="a28bd-130">As more extensions transition to the DNR APIs, this change will improve user privacy, which contributes to enhancing trust in the use of extensions.</span></span>
<span data-ttu-id="a28bd-131">Предприятия могут продолжать использовать функцию блокировки API веб-запросов для расширений, управляемых через политики предприятия.</span><span class="sxs-lookup"><span data-stu-id="a28bd-131">Enterprises can continue to use the blocking behavior of the Web Request API for extensions managed through enterprise policies.</span></span> <span data-ttu-id="a28bd-132">Для получения дополнительных сведений о политиках расширения перейдите в раздел [Microsoft Edge – политики][MicrosoftEdgePolicies].</span><span class="sxs-lookup"><span data-stu-id="a28bd-132">For more information about extension policies, navigate to [Microsoft Edge – Policies][MicrosoftEdgePolicies].</span></span> 

## <span data-ttu-id="a28bd-133">Фоновые работники служб</span><span class="sxs-lookup"><span data-stu-id="a28bd-133">Background service workers</span></span>  
 
<span data-ttu-id="a28bd-134">Сотрудники службы доступны для тестирования в Канарские.</span><span class="sxs-lookup"><span data-stu-id="a28bd-134">Service workers are available for testing in Canary.</span></span> <span data-ttu-id="a28bd-135">Для переноса расширений с фоновых страниц на сотрудников служб ознакомьтесь со [страницами переход с фоновых страниц на служебные][ServiceWorkers].</span><span class="sxs-lookup"><span data-stu-id="a28bd-135">To migrate your extensions from background pages to service workers, refer to [Migrating from Background Pages to Service Workers][ServiceWorkers].</span></span> <span data-ttu-id="a28bd-136">Мы рекомендуем & оценить влияние этого изменения на то, что это изменение повлияет на пользователей и разработчиков.</span><span class="sxs-lookup"><span data-stu-id="a28bd-136">We're evaluating & investigating the impact that this change brings to both developers and users.</span></span> <span data-ttu-id="a28bd-137">Дополнительные сведения об этом изменении этого документа будут добавлены в будущем.</span><span class="sxs-lookup"><span data-stu-id="a28bd-137">We'll add  additional details on this change to this document in the future.</span></span> 

## <span data-ttu-id="a28bd-138">Когда эти изменения будут доступны в Microsoft Edge?</span><span class="sxs-lookup"><span data-stu-id="a28bd-138">When will these changes be available in Microsoft Edge?</span></span>

<span data-ttu-id="a28bd-139">Текущая декларативная реализация интерфейса API сетевого запроса доступна в стабильных и бета-каналах.</span><span class="sxs-lookup"><span data-stu-id="a28bd-139">The current declarative net request API implementation is available in our Stable and Beta channels.</span></span> <span data-ttu-id="a28bd-140">Разработчики могут протестировать эти изменения и оставить отзыв.</span><span class="sxs-lookup"><span data-stu-id="a28bd-140">Developers can test these changes, and provide feedback.</span></span> <span data-ttu-id="a28bd-141">Мы будем вносить усилия в разработку и проанализировать другие изменения.</span><span class="sxs-lookup"><span data-stu-id="a28bd-141">We'll contribute to development efforts and investigate further changes.</span></span> 

| <span data-ttu-id="a28bd-142">Имя канала</span><span class="sxs-lookup"><span data-stu-id="a28bd-142">Channel name</span></span> | <span data-ttu-id="a28bd-143">Описание</span><span class="sxs-lookup"><span data-stu-id="a28bd-143">Description</span></span> |
|:--- |:--- |  
| <span data-ttu-id="a28bd-144">Microsoft Edge 84 стабильный</span><span class="sxs-lookup"><span data-stu-id="a28bd-144">Microsoft Edge 84 Stable</span></span> | <span data-ttu-id="a28bd-145">API DNR доступен для тестирования</span><span class="sxs-lookup"><span data-stu-id="a28bd-145">DNR API is available for testing</span></span> |  
| <span data-ttu-id="a28bd-146">Бета-версия Microsoft Edge 85</span><span class="sxs-lookup"><span data-stu-id="a28bd-146">Microsoft Edge 85 Beta</span></span> | <span data-ttu-id="a28bd-147">Доступна поддержка изменения заголовка</span><span class="sxs-lookup"><span data-stu-id="a28bd-147">Header modification support is available</span></span>| 

<span data-ttu-id="a28bd-148">Когда изменения вносятся в Chromium, мы будем делиться временными шкалами, чтобы разработчики могли обновить свой код и повторно опубликовать расширения в магазине.</span><span class="sxs-lookup"><span data-stu-id="a28bd-148">When the changes are made to Chromium, we'll share timelines so that developers can update their code and republish extensions to the store.</span></span> 

<span data-ttu-id="a28bd-149">Мы будем продолжать публиковать обновления в нашем блоге.</span><span class="sxs-lookup"><span data-stu-id="a28bd-149">We'll continue publishing updates on our blog.</span></span> <span data-ttu-id="a28bd-150">Вы можете отправить свой отзыв по этим изменениям с помощью [TechCommunity][TechCommunity].</span><span class="sxs-lookup"><span data-stu-id="a28bd-150">You can provide your feedback on these changes through [TechCommunity][TechCommunity].</span></span>

<!-- links -->  

[EdgeAddons]: https://microsoftedge.microsoft.com/addons/ "Надстройки Microsoft Edge"  
[MicrosoftBlog]: https://blogs.windows.com/windowsexperience/2018/12/06/microsoft-edge-making-the-web-better-through-more-open-source-collaboration/  
[MicrosoftEdgePolicies]: https://docs.microsoft.com/deployedge/microsoft-edge-policies#extensions 

[TechCommunity]: https://techcommunity.microsoft.com/t5/articles/manifest-v3-changes-are-now-available-in-microsoft-edge/m-p/1780254 "Сообщество специалистов"  


[Google_Migrate_to_MV3]: https://developer.chrome.com/extensions/migrating_to_manifest_v3   
[SandboxingEval]: https://developer.chrome.com/apps/sandboxingEval "Использование eval в расширениях Chrome. Извлечен."
[CORS]: https://www.chromium.org/Home/chromium-security/extension-content-script-fetches "Изменения запросов на запросы между источниками в сценариях расширения содержимого"
[WebRequestAPI]: https://developer.chrome.com/extensions/webRequest "API веб-запросов"  
[DeclarativeNetRequestAPI]: https://developer.chrome.com/extensions/declarativeNetRequest/ "API-интерфейс декларативного сетевого запроса"
[ServiceWorkers]:  https://developers.chrome.com/extensions/migrating_to_service_workers

