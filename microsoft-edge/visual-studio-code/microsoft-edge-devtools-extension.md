---
description: Использование элементов для Microsoft EDGE (Chromium) из кода Visual Studio
title: Элементы для Microsoft EDGE (Chromium) из кода Visual Studio
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/26/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools, код VS, код Visual Studio, элементы
ms.openlocfilehash: 81488c08a76a16b80a415cbd17cd0617df916f54
ms.sourcegitcommit: 1cfcf2c8970a6c2221cfbf09a23d36b08bd60690
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "11135502"
---
# <span data-ttu-id="7caed-104">Расширение кода Microsoft Edge DevTools для Visual Studio</span><span class="sxs-lookup"><span data-stu-id="7caed-104">Microsoft Edge DevTools for Visual Studio Code extension</span></span>  

<span data-ttu-id="7caed-105">Использование</span><span class="sxs-lookup"><span data-stu-id="7caed-105">Use</span></span> <!--the [Microsoft Edge DevTools for Visual Studio Code][VisualstudioMarketplaceElementsMicrosoftEdgeChromium] --><span data-ttu-id="7caed-106">Это расширение для Access в Microsoft Edge DevTools в [коде Visual Studio][VisualstudioCode].</span><span class="sxs-lookup"><span data-stu-id="7caed-106">this extension to access in Microsoft Edge DevTools inside [Visual Studio Code][VisualstudioCode].</span></span>  <span data-ttu-id="7caed-107">У вас есть доступ к **элементам** и **сетевым** инструментам в Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="7caed-107">You have access to the **Elements** and **Network** tools in Microsoft Edge DevTools.</span></span>  <span data-ttu-id="7caed-108">Вы можете запустить или присоединиться к экземпляру Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="7caed-108">You may either launch or attach to an instance of Microsoft Edge.</span></span>  <span data-ttu-id="7caed-109">После подключения вы можете отобразить структуру HTML среды выполнения, изменить макет, устранить проблемы со стилизацией и проанализировать сетевой трафик.</span><span class="sxs-lookup"><span data-stu-id="7caed-109">After you connect you may display the runtime HTML structure, alter the layout, fix styling issues, and inspect network traffic.</span></span>  

## <span data-ttu-id="7caed-110">Инструмент "элементы"</span><span class="sxs-lookup"><span data-stu-id="7caed-110">Elements tool</span></span>  

<span data-ttu-id="7caed-111">По умолчанию расширение запускает экземпляр браузера в уникальном окне и предоставляет вам функциональные возможности **элементов** Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="7caed-111">By default, the extension launches a browser instance in a unique window and gives you the **Elements** functionality of Microsoft Edge DevTools.</span></span>  

:::image type="complex" source="./media/edge-devtools-for-vscode-windowed.png" alt-text="Microsoft Edge DevTools для кода Visual Studio, работающего в полном окне браузера" lightbox="./media/edge-devtools-for-vscode-windowed.png":::
   <span data-ttu-id="7caed-113">Microsoft Edge DevTools для кода Visual Studio, работающего в полном окне браузера</span><span class="sxs-lookup"><span data-stu-id="7caed-113">Microsoft Edge DevTools for Visual Studio Code running with a full browser window</span></span>  
:::image-end:::  

<span data-ttu-id="7caed-114">В параметрах расширения вы можете включить дополнительные функции, такие как **режим Бездисплейной** **сети и сеть**.</span><span class="sxs-lookup"><span data-stu-id="7caed-114">In the extension settings, you may enable more functionality like **Headless Mode** and **Network**.</span></span>  

:::image type="complex" source="./media/edge-devtools-for-vscode-settings.png" alt-text="Включение (отключение) режима без монитора и проверки сети в параметрах расширения" lightbox="./media/edge-devtools-for-vscode-settings.png":::
   <span data-ttu-id="7caed-116">Включение и отключение режима без монитора и проверки сети в параметрах расширения</span><span class="sxs-lookup"><span data-stu-id="7caed-116">Enabling \(or disabling\) headless mode and Network inspection in the extension settings</span></span>  
:::image-end:::  

## <span data-ttu-id="7caed-117">Режим без монитора</span><span class="sxs-lookup"><span data-stu-id="7caed-117">Headless Mode</span></span>  

<span data-ttu-id="7caed-118">В режиме бездисплейного режима это расширение не запускает полный экземпляр браузера для отладки.</span><span class="sxs-lookup"><span data-stu-id="7caed-118">In headless mode, this extension does not launch a full browser instance to debug.</span></span>  <span data-ttu-id="7caed-119">Он запускает экземпляр в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="7caed-119">It runs an instance in the background.</span></span>  <span data-ttu-id="7caed-120">Возможно, вам придется оставаться внутри редактора и взаимодействовать с внедренным браузером.</span><span class="sxs-lookup"><span data-stu-id="7caed-120">You may have to stay inside the editor and interact with the embedded browser.</span></span>  <span data-ttu-id="7caed-121">На панели задач не отображается дополнительный значок браузера.</span><span class="sxs-lookup"><span data-stu-id="7caed-121">An extra browser icon is not be displayed in your task bar.</span></span>  

:::image type="complex" source="./media/edge-devtools-for-vscode-headless.png" alt-text="Microsoft Edge DevTools для кода Visual Studio, работающего без монитора" lightbox="./media/edge-devtools-for-vscode-headless.png":::
   <span data-ttu-id="7caed-123">Microsoft Edge DevTools для кода Visual Studio, работающего в автономном браузере</span><span class="sxs-lookup"><span data-stu-id="7caed-123">Microsoft Edge DevTools for Visual Studio Code running with a headless browser</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="7caed-124">В macOS следует включить режим без монитора в качестве предпочтительного режима.</span><span class="sxs-lookup"><span data-stu-id="7caed-124">On macOS, you should turn on headless mode as your preferred mode.</span></span>  <span data-ttu-id="7caed-125">При использовании режима без монитора необходимо решить проблему, в которой окно браузера выводится, если окно не отображается `Not Active` .</span><span class="sxs-lookup"><span data-stu-id="7caed-125">Using headless mode should solve an issue where, if the window is not visible, the browser window reports that it is `Not Active`.</span></span>  

## <span data-ttu-id="7caed-126">Инструмент "сеть"</span><span class="sxs-lookup"><span data-stu-id="7caed-126">Network tool</span></span>  

<span data-ttu-id="7caed-127">Если вы также хотите проверить сетевой трафик вашего приложения, откройте параметры и включите вкладку **сеть** .</span><span class="sxs-lookup"><span data-stu-id="7caed-127">If you also want to inspect the network traffic of your application, open the settings and turn on the **Network** tab.</span></span>  

:::image type="complex" source="./media/edge-devtools-for-vscode-network.png" alt-text="Проверка сети в Microsoft Edge DevTools для кода Visual Studio" lightbox="./media/edge-devtools-for-vscode-network.png":::
    <span data-ttu-id="7caed-129">Проверка сети в Microsoft Edge DevTools для кода Visual Studio</span><span class="sxs-lookup"><span data-stu-id="7caed-129">Network inspection in Microsoft Edge DevTools for Visual Studio Code</span></span>  
:::image-end:::  

## <span data-ttu-id="7caed-130">Запуск Microsoft Edge из расширения</span><span class="sxs-lookup"><span data-stu-id="7caed-130">Launching Microsoft Edge From the extension</span></span>  

<span data-ttu-id="7caed-131">На **панели действий**перейдите в раздел "Инструменты Microsoft Edge".</span><span class="sxs-lookup"><span data-stu-id="7caed-131">Navigate to Microsoft Edge Tools in the **Activity Bar**.</span></span>  <span data-ttu-id="7caed-132">Рядом с надписью **Microsoft Edge Tools: targets ("цели")** есть знак "плюс", который открывает браузер для вашего приложения.</span><span class="sxs-lookup"><span data-stu-id="7caed-132">Next to where it says **Microsoft Edge Tools: Targets,** there is a plus sign that opens the browser for your app.</span></span>  <span data-ttu-id="7caed-133">Если вы выбрали параметр **about: Blank** , то для его отображения на панели **элементы** в коде Visual Studio необходимо перейти в браузере для этого веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="7caed-133">If you choose the **about:blank** option, you must navigate to your web app in the browser for it to appear in the **Elements** panel in Visual Studio Code.</span></span>  

## <span data-ttu-id="7caed-134">Запуск Microsoft Edge из представления отладки</span><span class="sxs-lookup"><span data-stu-id="7caed-134">Launching Microsoft Edge from the Debug view</span></span>  

<span data-ttu-id="7caed-135">Если вы привыкли использовать представление отладку в коде Visual Studio, вы можете получить доступ к Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="7caed-135">If you are accustomed to using the Debug view in Visual Studio Code, access Microsoft Edge DevTools from it.</span></span>  

1.  <span data-ttu-id="7caed-136">В коде Visual Studio перейдите в представление Отладка</span><span class="sxs-lookup"><span data-stu-id="7caed-136">In Visual Studio Code, navigate to the Debug view</span></span> 
    *   <span data-ttu-id="7caed-137">Выберите `Ctrl` + `Shift` + `D` в Windows или Linux \ ( `Command` + `Shift` + `D` на macOS \).</span><span class="sxs-lookup"><span data-stu-id="7caed-137">Select `Ctrl`+`Shift`+`D` on Windows/Linux  \(`Command`+`Shift`+`D` on macOS\).</span></span>  

<!--TODO:  Is this section intended to be optional  -->  
> [!NOTE]
> 1.  <span data-ttu-id="7caed-138">Если у вас нет каких – либо конфигураций в коде Visual Studio, выполните одно из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="7caed-138">If you do not have any configurations in Visual Studio Code, complete one of the following actions.</span></span>  
>     *   <span data-ttu-id="7caed-139">Выберите `F5` .</span><span class="sxs-lookup"><span data-stu-id="7caed-139">Select `F5`.</span></span>  
>     *   <span data-ttu-id="7caed-140">Нажмите кнопку **воспроизвести** \ (зеленый \).</span><span class="sxs-lookup"><span data-stu-id="7caed-140">Choose the **Play** \(green\) button.</span></span>  
> 1.  <span data-ttu-id="7caed-141">В раскрывающемся списке выберите пункт **край** в раскрывающемся списке.</span><span class="sxs-lookup"><span data-stu-id="7caed-141">In the dropdown, choose **Edge** in the dropdown.</span></span>  
> 1.  <span data-ttu-id="7caed-142">`launch.json`Должен отобразиться файл, содержащий указанную ниже конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="7caed-142">A `launch.json` file should be displayed that contains the following configuration.</span></span>  
>     
>     ```json
>     {
>       "version": "0.2.0",
>       "configurations": [
>         {
>           "name": "Launch Microsoft Edge and open the Edge DevTools",
>           "request": "launch",
>           "type": "vscode-edge-devtools.debug",
>           "url": "http://localhost:8080"
>         }
>       ]
>     }
>     ```  
>     
> <span data-ttu-id="7caed-143">После загрузки правильной конфигурации выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="7caed-143">After you load the correct configuration, complete the following action.</span></span>  

1.  <span data-ttu-id="7caed-144">Чтобы запустить инструмент **элементы** из кода Visual Studio, выполните одно из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="7caed-144">To launch the **Elements** tool from Visual Studio Code, complete one of the following actions.</span></span> 
    *   <span data-ttu-id="7caed-145">Выберите `F5` .</span><span class="sxs-lookup"><span data-stu-id="7caed-145">Select `F5`.</span></span>  
    *   <span data-ttu-id="7caed-146">Нажмите кнопку **воспроизвести** \ (зеленый \).</span><span class="sxs-lookup"><span data-stu-id="7caed-146">Choose the **Play** \(green\) button.</span></span>  
         
<span data-ttu-id="7caed-147">Теперь вы можете выполнить указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="7caed-147">Now, you may do the following actions.</span></span>  

*   <span data-ttu-id="7caed-148">Открыть презентацию в браузере.</span><span class="sxs-lookup"><span data-stu-id="7caed-148">Access a screencast of your browser.</span></span>  
*   <span data-ttu-id="7caed-149">Проверьте модель DOM и стиль компонентов на странице.</span><span class="sxs-lookup"><span data-stu-id="7caed-149">Inspect the DOM and the styling of the components on your page.</span></span>  

## <span data-ttu-id="7caed-150">Присоединение к Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="7caed-150">Attaching to Microsoft Edge</span></span>  

<span data-ttu-id="7caed-151">Чтобы открыть браузер и присоединить экземпляр к коду Visual Studio, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="7caed-151">To open a browser and attach the instance to Visual Studio Code, complete the following steps.</span></span> 

1.  <span data-ttu-id="7caed-152">Чтобы открыть экземпляр Microsoft Edge \ (Chromium \), скопируйте и выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="7caed-152">To open an instance of Microsoft Edge \(Chromium\), copy and run the following command.</span></span>  
    
    ```shell
    start msedge --remote-debugging-port=9222
    ```  
    
1.  <span data-ttu-id="7caed-153">После того как экземпляр запустится, скопируйте и вставьте следующий фрагмент кода в `launch.json` файл.</span><span class="sxs-lookup"><span data-stu-id="7caed-153">After the instance launches, copy and paste the following code snippet into your `launch.json` file.</span></span>  
    
    ```json
    {
        "type": "vscode-edge-devtools.debug",
        "request": "attach",
        "name": "Attach to Microsoft Edge and open the developer tools",
        "url": "http://localhost:3000/",
        "webRoot": "${workspaceFolder}/out",
        "port": 9222
    }
    ```  
    
1.  <span data-ttu-id="7caed-154">В коде Visual Studio откройте раскрывающееся меню **отладчик** и выберите команду **присоединиться к Microsoft EDGE и откройте Инструменты разработчика**.</span><span class="sxs-lookup"><span data-stu-id="7caed-154">In Visual Studio Code, open the **Debugger** drop-down menu and choose **Attach to Microsoft Edge and open the developer tools**.</span></span>  
1.  <span data-ttu-id="7caed-155">Чтобы запустить инструмент **элементы** из кода Visual Studio, выполните одно из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="7caed-155">To launch the **Elements** tool from Visual Studio Code, complete one of the following actions.</span></span> 
    *   <span data-ttu-id="7caed-156">Выберите `F5` .</span><span class="sxs-lookup"><span data-stu-id="7caed-156">Select `F5`.</span></span>  
    *   <span data-ttu-id="7caed-157">Нажмите кнопку **воспроизвести** \ (зеленый \).</span><span class="sxs-lookup"><span data-stu-id="7caed-157">Choose the **Play** \(green\) button.</span></span>  
         
<span data-ttu-id="7caed-158">Теперь вы можете выполнить указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="7caed-158">Now, you may do the following actions.</span></span>  

*   <span data-ttu-id="7caed-159">Открыть презентацию в браузере.</span><span class="sxs-lookup"><span data-stu-id="7caed-159">Access a screencast of your browser.</span></span>  
*   <span data-ttu-id="7caed-160">Проверьте модель DOM и стиль компонентов на странице.</span><span class="sxs-lookup"><span data-stu-id="7caed-160">Inspect the DOM and the styling of the components on your page.</span></span>  
    
## <span data-ttu-id="7caed-161">Знакомство с командой Microsoft Edge DevTools для расширения кода Visual Studio</span><span class="sxs-lookup"><span data-stu-id="7caed-161">Getting in touch with the Microsoft Edge DevTools for Visual Studio Code extension team</span></span>  

<span data-ttu-id="7caed-162">Отправьте отзыв, выполнив [архивацию][GithubMicrosoftVscodeEdgeDevtoolsNewIssue] в [репозитории GitHub][GithubMicrosoftVscodeEdgeDevtools] в расширении.</span><span class="sxs-lookup"><span data-stu-id="7caed-162">Send your feedback by [filing an issue][GithubMicrosoftVscodeEdgeDevtoolsNewIssue] against the [GitHub repo][GithubMicrosoftVscodeEdgeDevtools] of the extension.</span></span>  

<span data-ttu-id="7caed-163">Сведения о том, что нужно сделать</span><span class="sxs-lookup"><span data-stu-id="7caed-163">If you want to help make</span></span> <!--the Microsoft Edge DevTools for Visual Studio Code --><span data-ttu-id="7caed-164">Это расширение лучше, ваши публикации — Добро пожаловать.</span><span class="sxs-lookup"><span data-stu-id="7caed-164">this extension better, your contributions are welcome.</span></span>  <span data-ttu-id="7caed-165">Найдите все, что нужно, чтобы начать работу в [репозитории GitHub][GithubMicrosoftVscodeEdgeDevtools] на расширение.</span><span class="sxs-lookup"><span data-stu-id="7caed-165">Find everything you need to get started in the [GitHub repo][GithubMicrosoftVscodeEdgeDevtools] of the extension.</span></span>  

<!--links -->  

[VisualstudioCode]: https://code.visualstudio.com "Код Visual Studio"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Документация | Код Visual Studio"   

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/Microsoft/vscode-edge-devtools "Microsoft/vscode-Edge-Devtools | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsNewIssue]: https://github.com/Microsoft/vscode-edge-devtools/issues/new "Новая ошибка — Microsoft/vscode-Edge-Devtools | GitHub"

[VisualstudioMarketplaceElementsMicrosoftEdgeChromium]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Инструменты Microsoft Edge для кода VS"  
