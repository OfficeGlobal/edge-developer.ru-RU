---
description: Проверка расширения с помощью неопубликованных приложений в браузере
title: Неопубликованного расширение
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge — Chromium, Web Development, HTML, CSS, JavaScript, разработчик, расширения
ms.openlocfilehash: 7070878b9608e6d239179078390f2315e0b289a1
ms.sourcegitcommit: 845a0d53a86bee3678f421adee26b3372cefce57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/08/2020
ms.locfileid: "11104777"
---
# <span data-ttu-id="713ed-104">Неопубликованного расширение</span><span class="sxs-lookup"><span data-stu-id="713ed-104">Sideload an extension</span></span>

<span data-ttu-id="713ed-105">Во время разработки вы можете использовать браузер Microsoft Edge \ (Chromium \) для безопасного запуска и отладки расширения.</span><span class="sxs-lookup"><span data-stu-id="713ed-105">During development, you may use the Microsoft Edge \(Chromium\) browser to run and debug your extension safely.</span></span> <span data-ttu-id="713ed-106">С помощью неопубликованного веб-приложения в браузере вы можете запустить и протестировать свое расширение.</span><span class="sxs-lookup"><span data-stu-id="713ed-106">By sideloading your extension locally in your browser, you can run and test your extension.</span></span> <span data-ttu-id="713ed-107">В этой статье объясняется, как неопубликованного расширения в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="713ed-107">This article explains how to sideload extensions into Microsoft Edge.</span></span>

<span data-ttu-id="713ed-108">Чтобы неопубликованного расширение, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="713ed-108">To sideload your extension, follow these steps.</span></span>

1.  <span data-ttu-id="713ed-109">Откройте `edge://extensions` страницу, щелкнув три точки в верхней части окна браузера и выбрав пункт **расширения**.</span><span class="sxs-lookup"><span data-stu-id="713ed-109">Open the `edge://extensions` page by choosing the three dots at the top of your browser, and then selecting **Extensions**.</span></span>

       :::image type="complex" source="./media/part1-threedots.png" alt-text="Открытие страницы edge://extensions":::
          <span data-ttu-id="713ed-111">Открытие страницы edge://extensions</span><span class="sxs-lookup"><span data-stu-id="713ed-111">Open the edge://extensions page</span></span> :::image-end:::

1.  <span data-ttu-id="713ed-112">На странице Управление расширением `edge://extensions` включите **режим разработчика** , воспользовавшись переключателем в нижней части страницы.</span><span class="sxs-lookup"><span data-stu-id="713ed-112">On the extension management page at `edge://extensions`, turn on **Developer mode** using the toggle at the bottom left of the page.</span></span>

       :::image type="complex" source="./media/part1-developermode-toggle.png" alt-text="Открытие страницы edge://extensions":::
          <span data-ttu-id="713ed-114">Включение режима разработчика</span><span class="sxs-lookup"><span data-stu-id="713ed-114">Turn on Developer Mode</span></span> :::image-end:::

1.  <span data-ttu-id="713ed-115">При первом запуске расширения выберите пункт **загрузить распакованные**.</span><span class="sxs-lookup"><span data-stu-id="713ed-115">When installing your extension for the first time, choose **Load Unpacked**.</span></span>  <span data-ttu-id="713ed-116">Вам будет предложено указать каталог с исходными файлами расширения.</span><span class="sxs-lookup"><span data-stu-id="713ed-116">You'll be prompted for the directory with your extension source files.</span></span>  <span data-ttu-id="713ed-117">Расширение устанавливается в браузере, аналогично расширениям, установленным из магазина.</span><span class="sxs-lookup"><span data-stu-id="713ed-117">Your extension is installed in your browser, similar to extensions installed from the store.</span></span>  

       :::image type="complex" source="./media/part1-installed-extension.png" alt-text="Открытие страницы edge://extensions":::
          <span data-ttu-id="713ed-119">Страница установленных расширений, на которой показано расширение неопубликованного</span><span class="sxs-lookup"><span data-stu-id="713ed-119">Installed extensions page showing a sideloaded extension</span></span> :::image-end:::

<span data-ttu-id="713ed-120">В процессе разработки также может потребоваться выполнить следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="713ed-120">During development, you may also need to perform the following tasks.</span></span>
* <span data-ttu-id="713ed-121">Обновите расширение.</span><span class="sxs-lookup"><span data-stu-id="713ed-121">Update the extension.</span></span> <span data-ttu-id="713ed-122">Перейдите к разделу `edge://extensions` , а затем выберите пункт **перезагрузить** , чтобы обновить расширение.</span><span class="sxs-lookup"><span data-stu-id="713ed-122">Navigate to `edge://extensions`, and then select **Reload** to update your extension.</span></span>  
* <span data-ttu-id="713ed-123">Удалите расширение из браузера.</span><span class="sxs-lookup"><span data-stu-id="713ed-123">Remove the extension from your browser.</span></span> <span data-ttu-id="713ed-124">Перейдите к `edge://extensions` `Remove` своему расширению и выберите его.</span><span class="sxs-lookup"><span data-stu-id="713ed-124">Navigate to `edge://extensions`, and then select `Remove` on your extension.</span></span>