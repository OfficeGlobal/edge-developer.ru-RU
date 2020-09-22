---
description: Сведения об отладке элементов управления WebView2.
title: Приступая к отладке приложений WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/21/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 78c0fb982de8ccce71a8df2b59447b55f64fdc2f
ms.sourcegitcommit: 24151cc65bad92d751a8e7a868c102e1121456e3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/22/2020
ms.locfileid: "11052160"
---
# <span data-ttu-id="f1639-104">Приступая к отладке приложений WebView2</span><span class="sxs-lookup"><span data-stu-id="f1639-104">Get started debugging WebView2 applications</span></span>  

<span data-ttu-id="f1639-105">Цель элемента управления Microsoft Edge WebView2 заключается в том, чтобы сочетать лучший из функций разработки веб-и собственных приложений, а также средств и инструментов.</span><span class="sxs-lookup"><span data-stu-id="f1639-105">The goal of the Microsoft Edge WebView2 control is to combine the best of both the web and native application development features and tools.</span></span>  <span data-ttu-id="f1639-106">Когда вы разрабатываете приложение WebView2, необходимо выполнить отладку приложения.</span><span class="sxs-lookup"><span data-stu-id="f1639-106">When you develop your WebView2 application, you should debug your application.</span></span>  <span data-ttu-id="f1639-107">В этой статье описаны различные инструменты для отладки вашего веб-и собственного кода в приложении WebView2.</span><span class="sxs-lookup"><span data-stu-id="f1639-107">This article outlines the different tools to use to debug both your web and native code in your WebView2 application.</span></span>  

## [<span data-ttu-id="f1639-108">Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="f1639-108">Microsoft Edge DevTools</span></span>](#tab/devtools)  

<span data-ttu-id="f1639-109">Используйте [средства разработчика Microsoft EDGE (Chromium)][DevtoolsGuideChromiumMain] для отладки содержимого веб-страницы, отображаемого в элементах управления WebView2, таким же образом, как и при отладке на других страницах, отображаемых в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="f1639-109">Use [Microsoft Edge (Chromium) Developer Tools][DevtoolsGuideChromiumMain] to debug web content displayed in WebView2 controls, in the same way that you may debug for another webpage displayed in Microsoft Edge.</span></span>  <span data-ttu-id="f1639-110">Чтобы открыть DevTools, установите фокус на элементе управления WebView, а затем выполните одно из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="f1639-110">To open the DevTools, set focus on the WebView control and then use one of the following actions.</span></span>  

*   <span data-ttu-id="f1639-111">Выберите `F12` .</span><span class="sxs-lookup"><span data-stu-id="f1639-111">Select `F12`.</span></span>  
*   <span data-ttu-id="f1639-112">Выберите `Ctrl` + `Shift` + `I` .</span><span class="sxs-lookup"><span data-stu-id="f1639-112">Select `Ctrl`+`Shift`+`I`.</span></span>  
*   <span data-ttu-id="f1639-113">Откройте контекстное меню, а затем щелкните правой кнопкой мыши и выберите команду `Inspect` .</span><span class="sxs-lookup"><span data-stu-id="f1639-113">Open the context menu \(right-click\) and choose `Inspect`.</span></span>  

<span data-ttu-id="f1639-114">Дополнительные сведения можно найти в разделе [Общие сведения о DevTools][DevtoolsGuideChromiumMain].</span><span class="sxs-lookup"><span data-stu-id="f1639-114">For more information, see [DevTools overview][DevtoolsGuideChromiumMain].</span></span>  

:::image type="complex" source="./media/f12.png" alt-text="Отладка DevTools" lightbox="./media/f12.png":::
   <span data-ttu-id="f1639-116">Отладка DevTools</span><span class="sxs-lookup"><span data-stu-id="f1639-116">DevTools debugging</span></span>  
:::image-end:::  

## [<span data-ttu-id="f1639-117">VisualStudio</span><span class="sxs-lookup"><span data-stu-id="f1639-117">Visual Studio</span></span>](#tab/visualstudio)  

<span data-ttu-id="f1639-118">Visual Studio предоставляет различные инструменты отладки для веб-и машинного кода в приложениях WebView2.</span><span class="sxs-lookup"><span data-stu-id="f1639-118">Visual Studio provides various debugging tools for web and native code in WebView2 applications.</span></span>  <span data-ttu-id="f1639-119">В разделе Visual Studio основным фокусом является Отладка элементов управления WebView, однако другие методы отладки в Visual Studio можно использовать в обычном режиме.</span><span class="sxs-lookup"><span data-stu-id="f1639-119">In the Visual Studio section, the primary focus is debugging WebView controls, however the other methods of debugging in Visual Studio are available as usual.</span></span>  <span data-ttu-id="f1639-120">Используйте следующий процесс для отладки веб-и машинного кода в приложениях Win32 или только для надстроек Office.</span><span class="sxs-lookup"><span data-stu-id="f1639-120">Use the following process to debug web and native code in Win32 applications or Office Add-ins only.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="f1639-121">При отладке приложения в Visual Studio с присоединенным отладчиком машинного кода выбор `F12` может инициировать собственный отладчик вместо средств разработчика.</span><span class="sxs-lookup"><span data-stu-id="f1639-121">When you debug your application in Visual Studio with the native debugger attached, selecting `F12` may trigger the native debugger instead of Developer Tools.</span></span>  <span data-ttu-id="f1639-122">`Ctrl` + `Shift` + `I` Чтобы избежать ситуации, выберите или используйте контекстное меню \ (щелкните правой кнопкой мыши).</span><span class="sxs-lookup"><span data-stu-id="f1639-122">Select `Ctrl`+`Shift`+`I`, or use the context menu \(right-click\) to avoid the situation.</span></span>  

<span data-ttu-id="f1639-123">Прежде чем начать, убедитесь, что выполнены следующие требования.</span><span class="sxs-lookup"><span data-stu-id="f1639-123">Before you begin, ensure the following requirements are met.</span></span>  

*   <span data-ttu-id="f1639-124">Для отладки скриптов приложение должно быть запущено в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="f1639-124">To debug scripts, the app must be launched from within Visual Studio.</span></span>  
*   <span data-ttu-id="f1639-125">Вы не можете прикрепить отладчик к выполняющемуся процессу WebView2.</span><span class="sxs-lookup"><span data-stu-id="f1639-125">You cannot attach a debugger to a running WebView2 process.</span></span>  
*   <span data-ttu-id="f1639-126">Установите Visual Studio 2019 версии 16,4 Preview 2 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="f1639-126">Install Visual Studio 2019 version 16.4 Preview 2 or later.</span></span>  

<span data-ttu-id="f1639-127">Установка и настройка средств отладки сценариев в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="f1639-127">Install and set up the script debugger tools in Visual Studio.</span></span>  

1.  <span data-ttu-id="f1639-128">Выполните указанные ниже действия, чтобы установить компонент **диагностики JavaScript** в **классических разработках с + +**.</span><span class="sxs-lookup"><span data-stu-id="f1639-128">Complete the following actions to install the **JavaScript diagnostics** component in **Desktop development with C++**.</span></span>  

    1. <span data-ttu-id="f1639-129">На панели проводника Windows введите `Visual Studio Installer` .</span><span class="sxs-lookup"><span data-stu-id="f1639-129">In the Windows Explorer bar, type `Visual Studio Installer`.</span></span>  
    1. <span data-ttu-id="f1639-130">Щелкните **Установщик Visual Studio** , чтобы открыть его.</span><span class="sxs-lookup"><span data-stu-id="f1639-130">Choose **Visual Studio Installer** to open it.</span></span>  
    1. <span data-ttu-id="f1639-131">В установщике Visual Studio на установленной версии нажмите кнопку **Дополнительно** , а затем выберите команду **изменить**.</span><span class="sxs-lookup"><span data-stu-id="f1639-131">In the Visual Studio Installer, on the installed version, choose the **More** button, and then choose **Modify**.</span></span>  
    1. <span data-ttu-id="f1639-132">В Visual Studio в разделе **рабочие нагрузки**выберите параметр **Разработка классической среды на C++** .</span><span class="sxs-lookup"><span data-stu-id="f1639-132">In Visual Studio, under **Workloads**, choose the **Desktop Development in C++** setting.</span></span>  
        
        :::image type="complex" source="./media/workloads.png" alt-text="Экран изменения рабочей нагрузки в Visual Studio" lightbox="./media/workloads.png":::
            <span data-ttu-id="f1639-134">Экран изменения рабочей нагрузки в Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f1639-134">Visual Studio Modifying Workloads Screen</span></span> :::image-end:::  
        
    1.  <span data-ttu-id="f1639-135">Выберите **отдельные компоненты**.</span><span class="sxs-lookup"><span data-stu-id="f1639-135">Choose **Individual components**.</span></span>  
    1.  <span data-ttu-id="f1639-136">В поле поиска введите `JavaScript diagnostics` .</span><span class="sxs-lookup"><span data-stu-id="f1639-136">In the search box, enter `JavaScript diagnostics`.</span></span>  
    1.  <span data-ttu-id="f1639-137">Выберите параметр **диагностики JavaScript** .</span><span class="sxs-lookup"><span data-stu-id="f1639-137">Choose the **JavaScript diagnostics** setting.</span></span>  
    1.  <span data-ttu-id="f1639-138">Нажмите кнопку **изменить**.</span><span class="sxs-lookup"><span data-stu-id="f1639-138">Choose **Modify**.</span></span> 
        
        :::image type="complex" source="./media/indivcomp.png" alt-text="Вкладка "изменение отдельных компонентов" в Visual Studio" lightbox="./media/indivcomp.png":::
           <span data-ttu-id="f1639-140">Вкладка "изменение отдельных компонентов" в Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f1639-140">Visual Studio Modifying Individual Components Tab</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="f1639-141">Включите отладку сценариев для приложений WebView2.</span><span class="sxs-lookup"><span data-stu-id="f1639-141">Enable script debugging for WebView2 applications.</span></span>  
    1.  <span data-ttu-id="f1639-142">В проекте WebView2 откройте контекстное меню, а затем щелкните правой кнопкой мыши и выберите пункт **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="f1639-142">In your WebView2 project, open the context menu \(right-click\), and choose **Properties**.</span></span>  
    1.  <span data-ttu-id="f1639-143">В разделе **Свойства конфигурации**выберите пункт **Отладка**.</span><span class="sxs-lookup"><span data-stu-id="f1639-143">Under the **Configuration Properties**, choose **Debugging**.</span></span>  
    1.  <span data-ttu-id="f1639-144">В разделе **Тип отладчика**выберите **JavaScript (WebView2)**.</span><span class="sxs-lookup"><span data-stu-id="f1639-144">Under the **Debugger Type**, choose **JavaScript (WebView2)**.</span></span>  
        
        :::image type="complex" source="./media/enbjs.png" alt-text="Свойство конфигурации отладки в Visual Studio" lightbox="./media/enbjs.png":::
           <span data-ttu-id="f1639-146">Свойство конфигурации **отладки** в Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f1639-146">Visual Studio **Debugging** Configuration Property</span></span>  
        :::image-end:::  
        
<span data-ttu-id="f1639-147">Выполните указанные ниже действия, чтобы выполнить отладку приложения WebView2.</span><span class="sxs-lookup"><span data-stu-id="f1639-147">Complete the following actions to debug your WebView2 application.</span></span>  

1.  <span data-ttu-id="f1639-148">Чтобы задать точку останова в исходном коде, наведите указатель мыши на левый номер строки и выберите точку останова.</span><span class="sxs-lookup"><span data-stu-id="f1639-148">To set a breakpoint in your source code, hover to the left of the line number, and choose to set a breakpoint.</span></span>  <span data-ttu-id="f1639-149">Адаптеры отладки JS-и ст не выполняют сопоставление исходного пути.</span><span class="sxs-lookup"><span data-stu-id="f1639-149">The JS/TS debug adapter does not perform source path mapping.</span></span>  <span data-ttu-id="f1639-150">Вы должны открыть именно тот же путь, связанный с вашим WebView2.</span><span class="sxs-lookup"><span data-stu-id="f1639-150">You must open the exact same path associated with your WebView2.</span></span>  
    
    :::image type="complex" source="./media/breakpoint.png" alt-text="Добавление точки останова в Visual Studio" lightbox="./media/breakpoint.png"::: 
       <span data-ttu-id="f1639-152">Добавление точки останова в Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f1639-152">Visual Studio add breakpoint</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f1639-153">Чтобы запустить отладчик, выберите битовый Размер платформы, а затем нажмите зеленую кнопку воспроизведения рядом с **местным отладчиком Windows**.</span><span class="sxs-lookup"><span data-stu-id="f1639-153">To run the debugger, choose the bit size of the platform, and then choose the green play button next to **Local Windows Debugger**.</span></span>  <span data-ttu-id="f1639-154">Приложение запустится, и отладчик подключится к первому процессу WebView2, который вы создали.</span><span class="sxs-lookup"><span data-stu-id="f1639-154">The application runs and the debugger connects to the first WebView2 process that is created.</span></span>  
    
    :::image type="complex" source="./media/run.png" alt-text=" Локальный отладчик Windows для Visual Studio" lightbox="./media/run.png"::: 
       <span data-ttu-id="f1639-156">**Локальный отладчик Windows** для Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f1639-156">Visual Studio **Local Windows Debugger**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f1639-157">В **консоли отладки**найдите выходные данные отладчика.</span><span class="sxs-lookup"><span data-stu-id="f1639-157">In the **Debug Console**, find the output from the debugger.</span></span>  
    
    :::image type="complex" source="./media/console.png" alt-text=" Консоль отладки Visual Studio" lightbox="./media/console.png"::: 
       <span data-ttu-id="f1639-159">**Консоль отладки** Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f1639-159">Visual Studio **Debug Console**</span></span>  
    :::image-end:::  
    
## [<span data-ttu-id="f1639-160">Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="f1639-160">Visual Studio Code</span></span>](#tab/visualstudiocode)  

<span data-ttu-id="f1639-161">Используйте код Microsoft Visual Studio для отладки сценариев, которые выполняются в элементах управления WebView2.</span><span class="sxs-lookup"><span data-stu-id="f1639-161">Use Microsoft Visual Studio Code to debug scripts that run in WebView2 controls.</span></span>  <!--Ensure that you're using Visual Studio Code version [insert build here] or later.  -->  

<span data-ttu-id="f1639-162">В коде Visual Studio выполните указанные ниже действия, чтобы выполнить отладку кода.</span><span class="sxs-lookup"><span data-stu-id="f1639-162">In Visual Studio Code, complete the following actions to debug your code.</span></span> 

1.  <span data-ttu-id="f1639-163">Для вашего проекта требуется `launch.json` файл.</span><span class="sxs-lookup"><span data-stu-id="f1639-163">Your project is required to have a `launch.json` file.</span></span>  <span data-ttu-id="f1639-164">Если в проекте нет `launch.json` файла, скопируйте приведенный ниже фрагмент кода и создайте новый `launch.json` файл.</span><span class="sxs-lookup"><span data-stu-id="f1639-164">If your project doesn't have a `launch.json` file, copy the following code snippet and create a new `launch.json` file.</span></span>  
        
    ```json
        "name": "Hello debug world",
        "type": "pwa-msedge",
        "port": 9222, // The port value is optional, and the default value is 9222.
        "request": "launch",
        "runtimeExecutable": "C:/path/to/your/webview2/application.exe",
        "env": {
            // Customize for your application location if needed
            "Path": "%path%;e:/path/to/your/application/location; "
        },
        "useWebView": true,
    ```  
        
1.  <span data-ttu-id="f1639-165">Чтобы задать точку останова в исходном коде, наведите указатель мыши на строку и выберите</span><span class="sxs-lookup"><span data-stu-id="f1639-165">To set a breakpoint in your source code, hover on the line, and select</span></span> `F9`
    
    :::image type="complex" source="./media/breakpointvs.png" alt-text="Точка останова, заданная в коде Visual Studio" lightbox="./media/breakpointvs.png":::
       <span data-ttu-id="f1639-167">Точка останова, заданная в коде Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f1639-167">Breakpoint is set in Visual Studio Code</span></span>  
    :::image-end:::
    
    > [!NOTE]
    > <span data-ttu-id="f1639-168">Поскольку код Visual Studio не выполняет сопоставление источника, убедитесь, что точки останова задаются в том же файле, который WebView2 использует.</span><span class="sxs-lookup"><span data-stu-id="f1639-168">Because Visual Studio Code does not perform source mapping, ensure you set breakpoints in the same file that WebView2 uses.</span></span>  <span data-ttu-id="f1639-169">Если пути не совпадают, код Visual Studio не приостанавливает выполнение кода в точке останова.</span><span class="sxs-lookup"><span data-stu-id="f1639-169">If the paths do not match, Visual Studio Code does not pause the running code at the breakpoint.</span></span>  
    
1.  <span data-ttu-id="f1639-170">Запустите код.</span><span class="sxs-lookup"><span data-stu-id="f1639-170">Run the code.</span></span>  
    1.  <span data-ttu-id="f1639-171">На вкладке " **выполнить** " в раскрывающемся меню выберите пункт "Настройка запуска".</span><span class="sxs-lookup"><span data-stu-id="f1639-171">On the **Run** tab, choose the launch configuration from the dropdown menu.</span></span>  
    1.  <span data-ttu-id="f1639-172">Чтобы начать отладку приложения, нажмите кнопку начать отладку, которая является зеленым треугольником рядом с раскрывающимся списком настройки запуска.</span><span class="sxs-lookup"><span data-stu-id="f1639-172">To start debugging your application, choose Start Debugging, which is the green triangle next to the launch configuration drop down.</span></span>  
        
        :::image type="complex" source="./media/runvs.png" alt-text=" Вкладка "запуск кода" в Visual Studio" lightbox="./media/runvs.png":::
           <span data-ttu-id="f1639-174">Вкладка "запуск кода" в Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f1639-174">Visual Studio Code Run tab</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="f1639-175">Откройте **консоль отладки** , чтобы просмотреть результаты отладки и ошибки.</span><span class="sxs-lookup"><span data-stu-id="f1639-175">Open **Debug Console** to view the debug output and errors.</span></span>  
    
    :::image type="complex" source="./media/resultsvs.png" alt-text=" Консоль отладки кода Visual Studio" lightbox="./media/resultsvs.png":::
       <span data-ttu-id="f1639-177">Консоль отладки кода Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f1639-177">Visual Studio Code Debug Console</span></span>  
    :::image-end:::  
    
<span data-ttu-id="f1639-178">**Дополнительные параметры**.</span><span class="sxs-lookup"><span data-stu-id="f1639-178">**Advanced Settings**:</span></span>  

*   <span data-ttu-id="f1639-179">Целевая Отладка WebView.</span><span class="sxs-lookup"><span data-stu-id="f1639-179">Targeted Webview debugging.</span></span> 

    <span data-ttu-id="f1639-180">В некоторых приложениях WebView2 можно использовать более одного элемента управления WebView2.</span><span class="sxs-lookup"><span data-stu-id="f1639-180">In some WebView2 applications, you may use more than one WebView2 control.</span></span> <span data-ttu-id="f1639-181">Выбор элемента управления WebView2 для отладки в этой ситуации можно использовать целевую отладку WebView2</span><span class="sxs-lookup"><span data-stu-id="f1639-181">To pick the WebView2 control to debug in this situation you can use targeted webview2 debugging</span></span> 
    
    <span data-ttu-id="f1639-182">Откройте `launch.json` и выполните следующие действия, чтобы использовать целевую отладку WebView.</span><span class="sxs-lookup"><span data-stu-id="f1639-182">Open `launch.json` and complete the following actions to use targeted Webview debugging.</span></span>  
    
    1.  <span data-ttu-id="f1639-183">Убедитесь, что `useWebview` для параметра задано значение `true` .</span><span class="sxs-lookup"><span data-stu-id="f1639-183">Confirm that the `useWebview` parameter is set to `true`.</span></span>  
    1.  <span data-ttu-id="f1639-184">Добавьте `urlFilter` параметр.</span><span class="sxs-lookup"><span data-stu-id="f1639-184">Add the `urlFilter` parameter.</span></span>  <span data-ttu-id="f1639-185">Когда элемент управления WebView2 переходит по URL-адресу, `urlFilter` значение параметра используется для сравнения строк, которые отображаются в URL-адресе.</span><span class="sxs-lookup"><span data-stu-id="f1639-185">When the WebView2 control navigates to a URL, the `urlFilter` parameter value is used to compare strings that appear in the URL.</span></span>  
    
    ```json
    "useWebview": "true",
    "urlFilter": "*index.ts",
    
    // Other urlFilter options.
    
    urlFilter="*index.ts"    // Match any url that ends with index.ts, and ignore all leading characters. 
    urlFilter="*index*"      // Match any url that contains the string index anywhere in the URL.  
    urlFilter="file://C:/path/to/my/index.ts," // To match explicit file called index.ts.  
    ```  
    
    <span data-ttu-id="f1639-186">При отладке приложения может потребоваться шаг с заходом в начало процесса рендеринга.</span><span class="sxs-lookup"><span data-stu-id="f1639-186">When debugging your application, you may need to step through the code from the beginning of the rendering process.</span></span> <span data-ttu-id="f1639-187">Если вы обрабатываете веб-страницы на сайтах, но у вас нет доступа к исходному коду, вы можете использовать этот `?=value`  параметр, так как на веб-страницах пропускаются нераспознанные параметры.</span><span class="sxs-lookup"><span data-stu-id="f1639-187">If you are rendering webpages on sites and you don't have access to the source code, you can use the `?=value` option, because webpages ignore unrecognized parameters.</span></span>   
    
    > [!IMPORTANT]
    > <span data-ttu-id="f1639-188">После того как первое соответствие найдено в URL-адресе, отладчик остановится.</span><span class="sxs-lookup"><span data-stu-id="f1639-188">After the first match is found in the URL, the debugger stops.</span></span>  <span data-ttu-id="f1639-189">Одновременная отладка двух элементов управления WebView2 не поддерживается, так как порт CDP является общим для всех элементов управления WebView2 и использует один номер порта.</span><span class="sxs-lookup"><span data-stu-id="f1639-189">You cannot debug two WebView2 controls at the same time because the CDP port is shared by all WebView2 controls, and uses a single port number.</span></span>  
    
*   <span data-ttu-id="f1639-190">Отладка запущенных процессов</span><span class="sxs-lookup"><span data-stu-id="f1639-190">Debug running processes</span></span>  
    
    <span data-ttu-id="f1639-191">Возможно, потребуется присоединить отладчик для выполнения процессов WebView2.</span><span class="sxs-lookup"><span data-stu-id="f1639-191">You may need to attach the debugger to running WebView2 processes.</span></span> <span data-ttu-id="f1639-192">Чтобы сделать это, установите `launch.json` `request` для параметра значение `attach` .</span><span class="sxs-lookup"><span data-stu-id="f1639-192">To do that, in `launch.json`, update the `request` parameter to `attach`.</span></span>
        
    ```json
        "name": "Hello debugging world",
        "type": "pwa-msedge",
        "port": 9222, 
        "request": "attach",
        "runtimeExecutable": "C:/path/to/your/webview2/application.exe",  
        "env": {
            "Path": "%path%;e:/path/to/your/build/location; "  
        },
        "useWebView": true
    ```  
        
    <span data-ttu-id="f1639-193">Элемент управления WebView2 должен открыть порт CDP, чтобы разрешить отладку элемента управления WebView2.</span><span class="sxs-lookup"><span data-stu-id="f1639-193">Your WebView2 control must open the CDP port to allow debugging of the WebView2 control.</span></span>  <span data-ttu-id="f1639-194">Код должен быть построен так, чтобы только один WebView2 элемент управления был открыт портом CDP, прежде чем запускать отладчик.</span><span class="sxs-lookup"><span data-stu-id="f1639-194">Your code must be built to ensure that only one WebView2 control has a Chrome Developer Protocol (CDP) port open, before starting the debugger.</span></span>  
    
*   <span data-ttu-id="f1639-195">Параметры трассировки отладки</span><span class="sxs-lookup"><span data-stu-id="f1639-195">Debug tracing options</span></span>  
    
    <span data-ttu-id="f1639-196">Добавьте `trace` параметр в launch.json, чтобы включить трассировку отладки.</span><span class="sxs-lookup"><span data-stu-id="f1639-196">Add the `trace` parameter to launch.json to enable debug tracing.</span></span>  
    
    1.  <span data-ttu-id="f1639-197">Добавить `trace` параметр.</span><span class="sxs-lookup"><span data-stu-id="f1639-197">Add `trace` parameter.</span></span>  
        
 
        
        :::row:::
           :::column span="":::
              ```json
                "name": "Hello debugging world",
                "type": "pwa-msedge",
                "port": 9222, 
                "request": "attach",
                "runtimeExecutable": "C:/path/to/your/webview2/application.exe",  
                "env": {
                "Path": "%path%;e:/path/to/your/build/location; "  
                },
                "useWebView": true
                ,"trace": true  // Turn on  debug tracing, and save the output to a log file.
              ```  
              
              :::image type="complex" source="./media/tracelog.png" alt-text=" Сохранение выходных данных отладки в файле журнала." lightbox="./media/tracelog.png":::
                 <span data-ttu-id="f1639-199">Сохранение выходных данных отладки в файле журнала</span><span class="sxs-lookup"><span data-stu-id="f1639-199">Save debug output to a log file</span></span>  
              :::image-end:::  
           :::column-end:::
           :::column span="":::
              ```json
              ,"trace": "verbose"  // Turn on verbose tracing in the Debug Output pane.
              ```  
              
              :::image type="complex" source="./media/verbose.png" alt-text=" Подробный вывод" lightbox="./media/verbose.png":::
                 <span data-ttu-id="f1639-201">Отладочный вывод кода Visual Studio с включенной подробной трассировкой</span><span class="sxs-lookup"><span data-stu-id="f1639-201">Visual Studio Code Debug Output with verbose tracing turned on</span></span>  
              :::image-end:::  
           :::column-end:::
        :::row-end:::  
        
*   <span data-ttu-id="f1639-202">Отладка надстроек для Office.</span><span class="sxs-lookup"><span data-stu-id="f1639-202">Debug Office Add-ins.</span></span>
    
    <span data-ttu-id="f1639-203">При отладке надстроек Office откройте исходный код надстройки в отдельном экземпляре кода Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="f1639-203">If you're debugging Office Add-ins, open the add-in source code in a separate instance of Visual Studio Code.</span></span>  <span data-ttu-id="f1639-204">Откройте launch.jsв приложении WebView2 и добавьте следующий фрагмент кода, чтобы прикрепить отладчик к надстройке Office.</span><span class="sxs-lookup"><span data-stu-id="f1639-204">Open launch.json in your WebView2 application and add the following code snippet to attach the debugger to the Office add-in.</span></span>
    
    ```json
    ,"debugServer": 4711
    ```  
    
*   <span data-ttu-id="f1639-205">Устранение неполадок отладчика</span><span class="sxs-lookup"><span data-stu-id="f1639-205">Troubleshooting the debugger</span></span>  
    
    <span data-ttu-id="f1639-206">При использовании отладчика вы можете столкнуться со следующими сценариями.</span><span class="sxs-lookup"><span data-stu-id="f1639-206">You may encounter the following scenarios when using the debugger.</span></span>  

    *   <span data-ttu-id="f1639-207">Отладчик не остановится на точке останова, и у вас есть отладочный вывод.</span><span class="sxs-lookup"><span data-stu-id="f1639-207">The debugger doesn't stop at the breakpoint, and you have debug output.</span></span>  <span data-ttu-id="f1639-208">Чтобы устранить эту проблему, убедитесь, что файл с точкой останова является тем же файлом, который используется элементом управления WebView2.</span><span class="sxs-lookup"><span data-stu-id="f1639-208">To solve the issue, confirm that the file with the breakpoint is the same file that's used by the WebView2 control.</span></span>  <span data-ttu-id="f1639-209">Отладчик не выполняет сопоставление исходного пути.</span><span class="sxs-lookup"><span data-stu-id="f1639-209">The debugger doesn't perform source path mapping.</span></span>  
    *   <span data-ttu-id="f1639-210">Вы не можете присоединиться к выполняющемуся процессу, и вы получаете сообщение об ошибке тайм-аута.</span><span class="sxs-lookup"><span data-stu-id="f1639-210">You can't attach to a running process, and you get a timeout error.</span></span>  <span data-ttu-id="f1639-211">Чтобы устранить эту проблему, убедитесь, что элемент управления WebView2 открыл порт CDP.</span><span class="sxs-lookup"><span data-stu-id="f1639-211">To solve the issue, confirm that the WebView2 control opened the CDP port.</span></span>  <span data-ttu-id="f1639-212">Убедитесь  `additionalBrowserArguments`  , что значение в реестре введено правильно, или параметры указаны правильно.</span><span class="sxs-lookup"><span data-stu-id="f1639-212">Ensure your `additionalBrowserArguments` value in the registry is correct, or the options are correct.</span></span>  <span data-ttu-id="f1639-213">Дополнительные сведения можно найти в разделе [additionalBrowserArguments для DotNet] [Webview2ReferenceDotnet09515MicrosoftWebWebview2CoreCorewebview2environmentoptionsAdditionalbrowserarguments] и [additionalBrowserArguments для Win32] [Webview2ReferenceWin3209538Webview2IdlParameters].</span><span class="sxs-lookup"><span data-stu-id="f1639-213">For more information, see [additionalBrowserArguments for dotnet][Webview2ReferenceDotnet09515MicrosoftWebWebview2CoreCorewebview2environmentoptionsAdditionalbrowserarguments] and [additionalBrowserArguments for Win32][Webview2ReferenceWin3209538Webview2IdlParameters].</span></span>  
    
* * *  


* * *  

## <span data-ttu-id="f1639-214">См. также</span><span class="sxs-lookup"><span data-stu-id="f1639-214">See also</span></span>  

*   <span data-ttu-id="f1639-215">Чтобы приступить к работе с WebView2, ознакомьтесь со статьей [руководства Приступая к работе с WebView2][Webview2MainGettingStarted].</span><span class="sxs-lookup"><span data-stu-id="f1639-215">To get started using WebView2, see [WebView2 Getting Started Guides][Webview2MainGettingStarted].</span></span>  
*   <span data-ttu-id="f1639-216">Полный пример возможностей WebView2 можно найти в репозитории [WebView2Samples][GithubMicrosoftedgeWebview2samples] на GitHub.</span><span class="sxs-lookup"><span data-stu-id="f1639-216">For a comprehensive example of WebView2 capabilities, see the [WebView2Samples][GithubMicrosoftedgeWebview2samples] repo on GitHub.</span></span>
*   <span data-ttu-id="f1639-217">Более подробную информацию об API WebView2 можно найти в [справочнике API][Webview2ApiReference].</span><span class="sxs-lookup"><span data-stu-id="f1639-217">For more detailed information about WebView2 APIs, see [API reference][Webview2ApiReference].</span></span>
*   <span data-ttu-id="f1639-218">Дополнительные сведения о WebView2ах можно найти в статьях [ресурсы WebView2][Webview2MainNextSteps].</span><span class="sxs-lookup"><span data-stu-id="f1639-218">For more information about WebView2, see [WebView2 Resources][Webview2MainNextSteps].</span></span>

## <span data-ttu-id="f1639-219">Знакомство с командой Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="f1639-219">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../../devtools-guide-chromium.md "Инструменты разработчика Microsoft EDGE (Chromium)"  

[Webview2ReferenceDotnet09628MicrosoftWebWebview2CoreCorewebview2environmentoptionsAdditionalbrowserarguments]: ../reference/dotnet/0-9-628/microsoft-web-webview2-core-corewebview2environmentoptions.md#additionalbrowserarguments "Класс AdditionalBrowserArguments-0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2EnvironmentOptions | Документы Microsoft"  
[Webview2ReferenceWin3209622Webview2IdlParameters]: ../reference/win32/0-9-622/webview2-idl.md#createcorewebview2environment  "CreateCoreWebView2Environment-Globals | Документы Microsoft"  
[Webview2ApiReference]: ../webview2-api-reference.md "Справочник по API Microsoft Edge WebView2 | Документы Microsoft"  
[Webview2MainNextSteps]: ../index.md#next-steps "Дальнейшие действия — введение в Microsoft Edge WebView2 (Предварительная версия) | Документы Microsoft"  
[Webview2MainGettingStarted]: ../index.md#getting-started "Приступая к работе: знакомство с Microsoft Edge WebView2 (Предварительная версия) | Документы Microsoft"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView Feedback-MicrosoftEdge/WebViewFeedback | GitHub"  
[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2 Samples-MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftVscodeJSDebugWhatsNew]: https://github.com/microsoft/vscode-js-debug#whats-new "Новые возможности -Отладчик JavaScript для Visual Studio Code-Microsoft/vscode-JS-Debug | GitHub"  

[GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications]: https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications "Microsoft EDGE (Chromium) WebView Applications-Debugger (код Visual Studio) — отладчик для Microsoft Edge-Microsoft/vscode-Edge-debug2 | GitHub"  
