---
description: Режим IE и Microsoft EDGE (Chromium) DevTools
title: Режим Internet Explorer и DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/08/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools, ie11, Internet Explorer 11, режим IE
ms.openlocfilehash: b059cae3ff48a45fe92cbf69e37ad692e329b200
ms.sourcegitcommit: 6b577cb118f34f3ff2c65eab2908b65f155dc151
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/09/2020
ms.locfileid: "11003975"
---
# <span data-ttu-id="770cf-104">Режим Internet Explorer и DevTools</span><span class="sxs-lookup"><span data-stu-id="770cf-104">Internet Explorer mode and the DevTools</span></span>  

<span data-ttu-id="770cf-105">В этой статье описывается интеграция режима Internet Explorer \ (режим IE) с Microsoft Edge \ (Chromium \) DevTools.</span><span class="sxs-lookup"><span data-stu-id="770cf-105">This article describes how Internet Explorer mode \(IE mode\) integrates with the Microsoft Edge \(Chromium\) DevTools.</span></span>  

## <span data-ttu-id="770cf-106">Общие сведения о режиме IE</span><span class="sxs-lookup"><span data-stu-id="770cf-106">Understanding IE mode</span></span>  

<span data-ttu-id="770cf-107">Режим IE позволяет компаниям указывать список веб-сайтов, которые работают только в Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="770cf-107">IE mode allows enterprises to specify a list of web sites that only work in Internet Explorer 11.</span></span>  <span data-ttu-id="770cf-108">При переходе на такие веб-сайты в Microsoft Edge \ (Chromium \) экземпляр браузера Internet Explorer 11 запускается и отображает сайт на вкладке.  Эта функция позволяет предприятиям управлять совместимостью с технологиями, которые в настоящее время не совместимы с современными веб-браузерами.</span><span class="sxs-lookup"><span data-stu-id="770cf-108">When you navigate to these web sites in Microsoft Edge \(Chromium\), an instance of Internet Explorer 11 runs and renders the site in a tab.  The functionality allows enterprises to manage compatibility with technologies that are currently not compatible with any modern web browsers.</span></span>  <span data-ttu-id="770cf-109">Поддержка следующих технологий включена в режим IE.</span><span class="sxs-lookup"><span data-stu-id="770cf-109">Support for the following technologies is included in IE mode.</span></span>  

*   <span data-ttu-id="770cf-110">Режимы работы с документами в IE</span><span class="sxs-lookup"><span data-stu-id="770cf-110">IE document modes</span></span>  
*   <span data-ttu-id="770cf-111">элементы ActiveX;</span><span class="sxs-lookup"><span data-stu-id="770cf-111">ActiveX controls</span></span>  
*   <span data-ttu-id="770cf-112">другие устаревшие компоненты</span><span class="sxs-lookup"><span data-stu-id="770cf-112">other legacy components</span></span>  

<span data-ttu-id="770cf-113">В режиме IE процесс отрисовки основан на Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="770cf-113">In IE mode, the rendering process is based on Internet Explorer 11.</span></span>  <span data-ttu-id="770cf-114">Диспетчер обработки Microsoft Edge \ (Chromium \) обрабатывает жизненный цикл процесса отрисовки.</span><span class="sxs-lookup"><span data-stu-id="770cf-114">The Microsoft Edge \(Chromium\) process manager handles the lifetime of the rendering process.</span></span>  <span data-ttu-id="770cf-115">Оно ограничено временем существования вкладки для определенного сайта \ (или приложения \).</span><span class="sxs-lookup"><span data-stu-id="770cf-115">It is constrained to the lifetime of the tab for a specific site \(or app\).</span></span>  <span data-ttu-id="770cf-116">При отображении вкладки в режиме IE в адресной строке на вкладке появляется индикатор.</span><span class="sxs-lookup"><span data-stu-id="770cf-116">When a tab renders in IE mode, a badge appears in the address bar for the specific tab.</span></span>  

:::image type="complex" source="./media/ie-mode-badge.msft.png" alt-text="Значок режима IE в адресной строке" lightbox="./media/ie-mode-badge.msft.png":::
   <span data-ttu-id="770cf-118">Значок режима IE в адресной строке</span><span class="sxs-lookup"><span data-stu-id="770cf-118">IE mode badge in the address bar</span></span>  
:::image-end:::  

<span data-ttu-id="770cf-119">В настоящее время режим Internet Explorer доступен в Windows 10 версии 1903 \ (обновление Май 2019), но скоро задействуется на все поддерживаемые платформы Windows.</span><span class="sxs-lookup"><span data-stu-id="770cf-119">IE mode is currently available on Windows 10 Version 1903 \(May 2019 Update\), but is coming soon to all supported Windows platforms.</span></span>  

## <span data-ttu-id="770cf-120">Запуск DevTools на вкладке в режиме IE</span><span class="sxs-lookup"><span data-stu-id="770cf-120">Launching the DevTools on a tab in IE mode</span></span>  

<span data-ttu-id="770cf-121">Если вы пытаетесь просмотреть режим документов на веб-сайте в режиме IE, выберите индикатор в адресной строке.</span><span class="sxs-lookup"><span data-stu-id="770cf-121">If you are trying to view the document mode of a web site in IE mode, choose the badge in the address bar.</span></span>  

:::image type="complex" source="./media/ie-mode-badge-doc-mode.msft.png" alt-text="Значок режима IE в адресной строке" lightbox="./media/ie-mode-badge-doc-mode.msft.png":::
   <span data-ttu-id="770cf-123">Просмотр режима документов с помощью эмблемы в режиме IE</span><span class="sxs-lookup"><span data-stu-id="770cf-123">View document mode using IE mode badge</span></span>  
:::image-end:::  

<span data-ttu-id="770cf-124">Если вкладка используется в режиме IE, DevTools не работает и выполняются следующие условия.</span><span class="sxs-lookup"><span data-stu-id="770cf-124">If a tab is using IE mode, the DevTools do not work and the following conditions occur.</span></span>

*   <span data-ttu-id="770cf-125">Если вы выберете `F12` или выберете `Ctrl` + `Shift` + `I` пустой экземпляр Microsoft Edge \ (Chromium \) DevTools, появится следующее сообщение.</span><span class="sxs-lookup"><span data-stu-id="770cf-125">If you select `F12` or select `Ctrl`+`Shift`+`I`, a blank instance of the Microsoft Edge \(Chromium\) DevTools is launched displays the following message.</span></span>  
    
    ```text
    Developer Tools are not available in Internet Explorer mode.  To debug the page, open it in Internet Explorer 11.
    ```  
    
*   <span data-ttu-id="770cf-126">Если вы открыли контекстное меню \ (щелкните правой кнопкой мыши \) и выберите команду **Просмотреть источник**, запускается блокнот.</span><span class="sxs-lookup"><span data-stu-id="770cf-126">If you open a contextual menu \(right-click\) and choose **View Source**, Notepad is launched.</span></span>  
*   <span data-ttu-id="770cf-127">Если открыть контекстное меню \ (щелкните правой кнопкой мыши \), элемент " **проверить** " не будет виден.</span><span class="sxs-lookup"><span data-stu-id="770cf-127">If you open a contextual menu \(right-click\), the **Inspect Element** is not visible.</span></span>  

<span data-ttu-id="770cf-128">Причина, по которой не работают некоторые инструменты в DevTools \ (например, **сеть** и **производительность** ), — средство визуализации переключается с Chromium на Internet Explorer 11 в режиме IE.</span><span class="sxs-lookup"><span data-stu-id="770cf-128">The reason that a number of the tools within the DevTools \(like the **Network** and **Performance** tools\) do not work is the rendering engine switches from Chromium to Internet Explorer 11 in IE mode.</span></span>  <span data-ttu-id="770cf-129">Чтобы отправить отзыв, перейдите к [разделу знакомство с командой Microsoft Edge DevTools](#getting-in-touch-with-the-microsoft-edge-devtools-team).</span><span class="sxs-lookup"><span data-stu-id="770cf-129">To provide feedback, navigate to [Getting in touch with the Microsoft Edge DevTools team](#getting-in-touch-with-the-microsoft-edge-devtools-team).</span></span>  

:::image type="complex" source="./media/ie-mode-devtools.msft.png" alt-text="Значок режима IE в адресной строке" lightbox="./media/ie-mode-devtools.msft.png":::
   <span data-ttu-id="770cf-131">DevTools запущен в режиме IE</span><span class="sxs-lookup"><span data-stu-id="770cf-131">DevTools launched in IE mode</span></span>  
:::image-end:::  

<span data-ttu-id="770cf-132">Чтобы протестировать веб-сайт на базе Internet Explorer 11 (или приложение \) в Internet Explorer 11 и IE, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="770cf-132">To test your Internet Explorer 11-based website \(or app\) in Internet Explorer 11 and IE mode, perform the following steps.</span></span>  

1.  <span data-ttu-id="770cf-133">Откройте Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="770cf-133">Open Internet Explorer 11.</span></span>  
    *   <span data-ttu-id="770cf-134">В Windows 10 найдите ярлык для Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="770cf-134">On Windows 10, locate the shortcut for Internet Explorer 11.</span></span>
        1.  <span data-ttu-id="770cf-135">Меню "Пуск" **Start Menu**  >  **Аксессуары**  >  для Windows **Internet Explorer 11**.</span><span class="sxs-lookup"><span data-stu-id="770cf-135">**Start Menu** > **Windows Accessories** > **Internet Explorer 11**.</span></span>  
    *   <span data-ttu-id="770cf-136">В Windows 7 найдите Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="770cf-136">On Windows 7, locate Internet Explorer 11.</span></span>
        1.  <span data-ttu-id="770cf-137">Меню "Пуск" **Start Menu**  >  **Internet Explorer 11**.</span><span class="sxs-lookup"><span data-stu-id="770cf-137">**Start Menu** > **Internet Explorer 11**.</span></span>  
1.  <span data-ttu-id="770cf-138">В Internet Explorer 11 откройте ту же веб-страницу.</span><span class="sxs-lookup"><span data-stu-id="770cf-138">In Internet Explorer 11, open the same webpage.</span></span>  
1.  <span data-ttu-id="770cf-139">Запустите Internet Explorer DevTools.</span><span class="sxs-lookup"><span data-stu-id="770cf-139">Launch the Internet Explorer DevTools.</span></span>  
    *   <span data-ttu-id="770cf-140">Выберите `F12` .</span><span class="sxs-lookup"><span data-stu-id="770cf-140">Select `F12`.</span></span>  
    *   <span data-ttu-id="770cf-141">Наведите указатель мыши на любое место, откройте контекстное меню, а затем нажмите кнопку **проверить элемент**.</span><span class="sxs-lookup"><span data-stu-id="770cf-141">Hover anywhere, open a contextual menu \(right-click\), and choose **Inspect element**.</span></span>  <span data-ttu-id="770cf-142">Дополнительные сведения об использовании этих средств можно найти в разделе [использование средств разработчика F12][PreviousVersionsWindowsInternetExplorerDeveloperSamplesbg182326].</span><span class="sxs-lookup"><span data-stu-id="770cf-142">For more information about how to use those tools, navigate to [Using the F12 developer tools][PreviousVersionsWindowsInternetExplorerDeveloperSamplesbg182326].</span></span>  

## <span data-ttu-id="770cf-143">Удаленная отладка и режим IE</span><span class="sxs-lookup"><span data-stu-id="770cf-143">Remote debugging and IE mode</span></span>  

<span data-ttu-id="770cf-144">Запустите Microsoft Edge \ (Chromium \) с включенной удаленной отладкой с помощью интерфейса командной строки.</span><span class="sxs-lookup"><span data-stu-id="770cf-144">Launch Microsoft Edge \(Chromium\) with remote debugging turned on from the command-line interface.</span></span>  <span data-ttu-id="770cf-145">Visual Studio, Visual Studio и другие средства разработки обычно выполняют команду для запуска Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="770cf-145">Visual Studio, Visual Studio Code, and other development tools typically run a command to launch Microsoft Edge.</span></span>  <span data-ttu-id="770cf-146">Следующая команда запускает Microsoft Edge с установленным портом удаленной отладки `9222` .</span><span class="sxs-lookup"><span data-stu-id="770cf-146">The following command launches Microsoft Edge with the remote debugging port set to `9222`.</span></span>  

```shell
start msedge --remote-debugging-port=9222
```  

<span data-ttu-id="770cf-147">После запуска Microsoft Edge \ (Chromium \) с помощью аргумента командной строки режим IE будет недоступен.</span><span class="sxs-lookup"><span data-stu-id="770cf-147">After you launch Microsoft Edge \(Chromium\) using a command-line argument, IE mode is unavailable.</span></span>  <span data-ttu-id="770cf-148">Вы по-прежнему можете переходить к веб-сайтам, которые в противном случае отображались бы в режиме IE.</span><span class="sxs-lookup"><span data-stu-id="770cf-148">You may still navigate to websites \(or apps\) that would otherwise display in IE mode.</span></span> <span data-ttu-id="770cf-149">Контент веб-сайта \ (или приложения \) будет обрабатываться с помощью Chromium, а не Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="770cf-149">The website \(or app\) content renders using Chromium, not Internet Explorer 11.</span></span>  <span data-ttu-id="770cf-150">Ожидается, что части страниц, зависящие от IE11, такие как элементы ActiveX, не отображаются должным образом.</span><span class="sxs-lookup"><span data-stu-id="770cf-150">Expect the parts of the pages that rely on IE11, such as ActiveX controls, to not render correctly.</span></span>  <span data-ttu-id="770cf-151">Значок "режим IE" не отображается в адресной строке.</span><span class="sxs-lookup"><span data-stu-id="770cf-151">The IE mode badge does not appear in the address bar.</span></span>  

<span data-ttu-id="770cf-152">Режим IE останется недоступным, пока вы не закроете и не перезапустите Microsoft Edge \ (Chromium \).</span><span class="sxs-lookup"><span data-stu-id="770cf-152">IE mode remains unavailable until you completely close and restart Microsoft Edge \(Chromium\).</span></span>  

## <span data-ttu-id="770cf-153">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="770cf-153">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](./includes/contact-devtools-team-note.md)]  

<!-- links -->  

[PreviousVersionsWindowsInternetExplorerDeveloperSamplesbg182326]: /previous-versions/windows/internet-explorer/ie-developer/samples/bg182326(v%3dvs.85) "Использование средств разработчика F12 | Документы Microsoft"  