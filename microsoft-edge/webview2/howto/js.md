---
description: Сведения об использовании JavaScript в сложных сценариях в приложениях WebView2
title: Использование JavaScript в приложениях WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/14/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: f6e59acb0c4bf8ad5357aba87e0359d3b103ed63
ms.sourcegitcommit: 61cc15d2fc89aee3e09cec48ef1e0e5bbf8d289a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/15/2020
ms.locfileid: "11119068"
---
# <span data-ttu-id="407f5-104">Использование JavaScript в WebView для расширенных сценариев</span><span class="sxs-lookup"><span data-stu-id="407f5-104">Use JavaScript in WebView for extended scenarios</span></span>  

<span data-ttu-id="407f5-105">Использование JavaScript в элементах управления WebView2 позволяет настраивать собственные приложения в соответствии с вашими потребностями.</span><span class="sxs-lookup"><span data-stu-id="407f5-105">Using JavaScript in WebView2 controls allows you to customize native apps to meet your requirements.</span></span>  <span data-ttu-id="407f5-106">В этой статье рассказывается о том, как использовать JavaScript в WebView2, а также о том, как разрабатывать дополнительные функции и функции WebView2.</span><span class="sxs-lookup"><span data-stu-id="407f5-106">This article explores how to use JavaScript in WebView2, and reviews how to develop using advanced WebView2 features and functionality.</span></span>  

## <span data-ttu-id="407f5-107">Перед началом работы</span><span class="sxs-lookup"><span data-stu-id="407f5-107">Before you begin</span></span>  

<span data-ttu-id="407f5-108">В этой статье предполагается, что у вас уже есть рабочий проект.</span><span class="sxs-lookup"><span data-stu-id="407f5-108">This article assumes that you already have a working project.</span></span>  <span data-ttu-id="407f5-109">Если у вас нет проекта и вы хотите подписаться на него, перейдите в [Руководство Приступая к работе с WebView2][Webview2GettingstartedWpf].</span><span class="sxs-lookup"><span data-stu-id="407f5-109">If you do not have a project and want to follow along, navigate to the [WebView2 Getting Started Guide][Webview2GettingstartedWpf].</span></span>  

## <span data-ttu-id="407f5-110">Основные функции WebView2</span><span class="sxs-lookup"><span data-stu-id="407f5-110">Basic WebView2 Functions</span></span>  

<span data-ttu-id="407f5-111">Чтобы приступить к внедрению JavaScript в приложение WebView, воспользуйтесь приведенными ниже функциями.</span><span class="sxs-lookup"><span data-stu-id="407f5-111">Use the following functions to begin embedding JavaScript in your WebView app.</span></span>  

| <span data-ttu-id="407f5-112">API</span><span class="sxs-lookup"><span data-stu-id="407f5-112">API</span></span>  | <span data-ttu-id="407f5-113">Описание</span><span class="sxs-lookup"><span data-stu-id="407f5-113">Description</span></span>  |
|:--- |:--- |  
| [<span data-ttu-id="407f5-114">ExecuteScriptAsync</span><span class="sxs-lookup"><span data-stu-id="407f5-114">ExecuteScriptAsync</span></span>][Webview2ReferenceWpf09515MicrosoftWebExecutescriptasync] | <span data-ttu-id="407f5-115">Запустите JavaScript в элементе управления WebView.</span><span class="sxs-lookup"><span data-stu-id="407f5-115">Run JavaScript in a WebView control.</span></span> <span data-ttu-id="407f5-116">Дополнительные сведения можно найти в учебнике Приступая к работе.</span><span class="sxs-lookup"><span data-stu-id="407f5-116">For more information, navigate to the Getting Started tutorial.</span></span> |
| [<span data-ttu-id="407f5-117">OnDocumentCreatedAsync</span><span class="sxs-lookup"><span data-stu-id="407f5-117">OnDocumentCreatedAsync</span></span>][Webview2ReferenceWin3209538Icorewebview2Addscripttoexecuteondocumentcreated] | <span data-ttu-id="407f5-118">Выполняется, когда создается объектная модель документа \ (DOM \).</span><span class="sxs-lookup"><span data-stu-id="407f5-118">Runs when the Document Object Model \(DOM\) is created.</span></span> |
      
## <span data-ttu-id="407f5-119">Сценарий: Запуск выделенного файла сценария</span><span class="sxs-lookup"><span data-stu-id="407f5-119">Scenario:  Running a dedicated script file</span></span>  

<span data-ttu-id="407f5-120">В этом разделе можно получить доступ к выделенному файлу JavaScript из элемента управления WebView2.</span><span class="sxs-lookup"><span data-stu-id="407f5-120">In this section, access a dedicated JavaScript file from your WebView2 control.</span></span>  

> [!NOTE]
> <span data-ttu-id="407f5-121">Несмотря на то, что написание встроенного кода JavaScript может быть эффективным для быстрых команд JavaScript, вы теряете цветовые темы и форматирование линий JavaScript, что затрудняет создание больших фрагментов кода в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="407f5-121">Although writing JavaScript inline may be efficient for quick JavaScript commands, you lose JavaScript color themes and line formatting that makes it difficult to write large sections of code in Visual Studio.</span></span>  

<span data-ttu-id="407f5-122">Чтобы решить эту проблему, создайте отдельный файл JavaScript с кодом, а затем передайте ссылку на этот файл с помощью `ExecuteScriptAsync` параметров.</span><span class="sxs-lookup"><span data-stu-id="407f5-122">To solve the problem, create a separate JavaScript file with your code, and then pass a reference to that file using the `ExecuteScriptAsync` parameters.</span></span>  

1.  <span data-ttu-id="407f5-123">Создайте `.js` файл в проекте и добавьте код JavaScript, который необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="407f5-123">Create a `.js` file in your project, and add the JavaScript code that you want to run.</span></span>  <span data-ttu-id="407f5-124">Например, создайте файл с именем `script.js` .</span><span class="sxs-lookup"><span data-stu-id="407f5-124">For example, create a file called `script.js`.</span></span>  
1.  <span data-ttu-id="407f5-125">Преобразуйте файл JavaScript в строку, которая передается `ExecuteScriptAsync` .</span><span class="sxs-lookup"><span data-stu-id="407f5-125">Convert the JavaScript file to a string that is passed to `ExecuteScriptAsync`.</span></span>  
    1.  <span data-ttu-id="407f5-126">Чтобы преобразовать файл JavaScript в строку, скопируйте следующий фрагмент кода.</span><span class="sxs-lookup"><span data-stu-id="407f5-126">To convert your JavaScript file into a string, copy the following code snippet.</span></span>  
        
        ```csharp
        string text = System.IO.File.ReadAllText(@"C:\PATH_TO_YOUR_FILE\script.js");
        ```  
        
    1.  <span data-ttu-id="407f5-127">Вставьте код в `MainWindow.xaml.cs` .</span><span class="sxs-lookup"><span data-stu-id="407f5-127">Paste the code into `MainWindow.xaml.cs`.</span></span>  
1.  <span data-ttu-id="407f5-128">Передайте текстовую переменную с помощью `ExecuteScriptAsync` .</span><span class="sxs-lookup"><span data-stu-id="407f5-128">Pass your text variable using `ExecuteScriptAsync`.</span></span>  
    
    ```csharp
    await webView.CoreWebView2.ExecuteScriptAsync(text);
    ```  

## <span data-ttu-id="407f5-129">Сценарий: Удаление функции перетаскивания</span><span class="sxs-lookup"><span data-stu-id="407f5-129">Scenario:  Remove drag-and-drop functionality</span></span>  

<span data-ttu-id="407f5-130">В этом разделе вы можете удалить функцию перетаскивания из элемента управления WebView2 с помощью JavaScript.</span><span class="sxs-lookup"><span data-stu-id="407f5-130">In this section, use JavaScript to remove the drag-and-drop functionality from your WebView2 control.</span></span>  

<span data-ttu-id="407f5-131">Для начала ознакомьтесь с текущими возможностями перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="407f5-131">To begin, explore the current drag-and-drop functionality.</span></span>  

1.  <span data-ttu-id="407f5-132">Создание `.txt` файла для перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="407f5-132">Create a `.txt` file in order to drag-and-drop.</span></span>  <span data-ttu-id="407f5-133">Например, можно создать файл с именем `contoso.txt` и добавить в него текст.</span><span class="sxs-lookup"><span data-stu-id="407f5-133">For example, create a file named `contoso.txt` and add text to it.</span></span>  
1.  <span data-ttu-id="407f5-134">Запустите проект.</span><span class="sxs-lookup"><span data-stu-id="407f5-134">Run your project.</span></span>  
1.  <span data-ttu-id="407f5-135">Перетащите `contoso.txt` файл на элемент управления WebView.</span><span class="sxs-lookup"><span data-stu-id="407f5-135">Drag-and-drop the `contoso.txt` file onto the WebView control.</span></span>  <span data-ttu-id="407f5-136">Откроется новое окно, которое является результатом кода в примере проекта.</span><span class="sxs-lookup"><span data-stu-id="407f5-136">A new window opens, which is the result of the code in your sample project.</span></span>  
    
    :::image type="complex" source="./media/dragtext.png" alt-text="Результат перетаскивания contoso.txt" lightbox="./media/dragtext.png":::
       <span data-ttu-id="407f5-138">Результат перетаскивания contoso.txt</span><span class="sxs-lookup"><span data-stu-id="407f5-138">Result of dragging and dropping contoso.txt</span></span>  
    :::image-end:::  

<span data-ttu-id="407f5-139">Теперь добавьте код для удаления функции перетаскивания из элемента управления WebView2.</span><span class="sxs-lookup"><span data-stu-id="407f5-139">Now, add code to remove the drag-and-drop functionality from the WebView2 control.</span></span>  

1.  <span data-ttu-id="407f5-140">Скопируйте и вставьте следующий фрагмент кода `InitializeAsync()` в `MainWindow.xaml.cs` .</span><span class="sxs-lookup"><span data-stu-id="407f5-140">Copy and paste the following code snippet into `InitializeAsync()` in `MainWindow.xaml.cs`.</span></span>   
            
    ```csharp   
    await webView.CoreWebView2.ExecuteScriptAsync("window.addEventListener('dragover',function(e){e.preventDefault();},false);");
    
    await webView.CoreWebView2.ExecuteScriptAsync("window.addEventListener('drop',function(e){" +
    "e.preventDefault();" +
    "console.log(e.dataTransfer);" +
    "console.log(e.dataTransfer.files[0])" +
    "}, false);");
    ```  
          
1.  <span data-ttu-id="407f5-141">Запустите проект.</span><span class="sxs-lookup"><span data-stu-id="407f5-141">Run your project.</span></span>  
1.  <span data-ttu-id="407f5-142">Попробуйте перетащить `contoso.txt` .</span><span class="sxs-lookup"><span data-stu-id="407f5-142">Try to drag-and-drop `contoso.txt`.</span></span>  <span data-ttu-id="407f5-143">Убедитесь, что вы не можете перетаскивать.</span><span class="sxs-lookup"><span data-stu-id="407f5-143">Confirm that you are not able to drag-and-drop.</span></span>  

## <span data-ttu-id="407f5-144">Сценарий: удаление контекстного меню</span><span class="sxs-lookup"><span data-stu-id="407f5-144">Scenario:  Removing the Context Menu</span></span>  

<span data-ttu-id="407f5-145">В этом разделе удалите контекстное меню по умолчанию из элемента управления WebView2.</span><span class="sxs-lookup"><span data-stu-id="407f5-145">In this section, remove the default context menu from your WebView2 control.</span></span>  

<span data-ttu-id="407f5-146">Для начала ознакомьтесь с текущими функциями контекстного меню.</span><span class="sxs-lookup"><span data-stu-id="407f5-146">To begin, explore the current contextual menu functionality.</span></span>  

1.  <span data-ttu-id="407f5-147">Запустите проект.</span><span class="sxs-lookup"><span data-stu-id="407f5-147">Run your project.</span></span>  
1.  <span data-ttu-id="407f5-148">Наведите указатель мыши на элемент управления WebView2 и откройте контекстное меню, щелкнув его правой кнопкой мыши.</span><span class="sxs-lookup"><span data-stu-id="407f5-148">Hover anywhere on the WebView2 control and open the context menu \(right-click\).</span></span>  <span data-ttu-id="407f5-149">В контекстном меню отображаются варианты по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="407f5-149">The context menu displays the default choices.</span></span>  
    
    :::image type="complex" source="./media/contextmenu.png" alt-text="Результат перетаскивания contoso.txt" lightbox="./media/contextmenu.png":::
       <span data-ttu-id="407f5-151">Контекстное меню, в котором отображаются варианты по умолчанию</span><span class="sxs-lookup"><span data-stu-id="407f5-151">The context menu showing the default choices</span></span>  
    :::image-end:::  
    
<span data-ttu-id="407f5-152">Теперь добавьте код для удаления функциональных возможностей контекстного меню из элемента управления WebView2.</span><span class="sxs-lookup"><span data-stu-id="407f5-152">Now add code to remove the contextual menu functionality from the WebView2 control.</span></span>  

1.  <span data-ttu-id="407f5-153">Скопируйте и вставьте следующий фрагмент кода `InitializeAsync()` в `MainWindow.xaml.cs` .</span><span class="sxs-lookup"><span data-stu-id="407f5-153">Copy and paste the following code snippet into `InitializeAsync()` in `MainWindow.xaml.cs`.</span></span>    
        
    ```csharp   
    await webView.CoreWebView2.ExecuteScriptAsync("window.addEventListener('contextmenu', window => {window.preventDefault();});");
    ```  

1.  <span data-ttu-id="407f5-154">Запустите код еще раз.</span><span class="sxs-lookup"><span data-stu-id="407f5-154">Run the code again.</span></span>  <span data-ttu-id="407f5-155">Убедитесь, что вы не можете открыть контекстное меню, щелкнув правой кнопкой мыши.</span><span class="sxs-lookup"><span data-stu-id="407f5-155">Confirm that you're not able to open a context menu \(right-click\).</span></span>  
   
## <span data-ttu-id="407f5-156">См. также</span><span class="sxs-lookup"><span data-stu-id="407f5-156">See also</span></span>  

*   <span data-ttu-id="407f5-157">Подробнее о том, как приступить к работе с WebView2, можно найти в разделе [WebView2 Start Guides][Webview2MainGettingStarted](начало работы).</span><span class="sxs-lookup"><span data-stu-id="407f5-157">For more information on getting started using WebView2, navigate to [WebView2 Getting Started Guides][Webview2MainGettingStarted].</span></span>  
*   <span data-ttu-id="407f5-158">Чтобы получить исчерпывающий пример возможностей WebView2, перейдите в репозиторий [WebView2Samples][GithubMicrosoftedgeWebview2samples] на GitHub.</span><span class="sxs-lookup"><span data-stu-id="407f5-158">For a comprehensive example of WebView2 capabilities, navigate to the [WebView2Samples][GithubMicrosoftedgeWebview2samples] repo on GitHub.</span></span>  
*   <span data-ttu-id="407f5-159">Подробные сведения о API WebView2 можно найти в [справочнике по API][Webview2ApiReference].</span><span class="sxs-lookup"><span data-stu-id="407f5-159">For detailed information on WebView2 APIs, navigate to [API reference][Webview2ApiReference].</span></span>  
*   <span data-ttu-id="407f5-160">Для получения дополнительных сведений о WebView2 перейдите в раздел [WebView2 Resources (ресурсы][Webview2MainNextSteps]).</span><span class="sxs-lookup"><span data-stu-id="407f5-160">For more information on WebView2, navigate to [WebView2 Resources][Webview2MainNextSteps].</span></span>  

## <span data-ttu-id="407f5-161">Знакомство с командой Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="407f5-161">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../../devtools-guide-chromium.md "Инструменты разработчика Microsoft EDGE (Chromium) | Документы Microsoft"  


[Webview2ApiReference]: ../webview2-api-reference.md "Справочник по API Microsoft Edge WebView2 | Документы Microsoft"  
[Webview2GettingstartedWpf]: ../gettingstarted/wpf.md "Начало работы с WebView2 в WPF (Предварительная версия) | Документы Microsoft"  
[Webview2MainGettingStarted]: ../index.md#getting-started "Приступая к работе: знакомство с Microsoft Edge WebView2 (Предварительная версия) | Документы Microsoft"  
[Webview2MainNextSteps]: ../index.md#next-steps "Дальнейшие действия — введение в Microsoft Edge WebView2 (Предварительная версия) | Документы Microsoft"  
[Webview2ReferenceWin3209538Icorewebview2Addscripttoexecuteondocumentcreated]: ../reference/win32/0-9-538/icorewebview2.md#addscripttoexecuteondocumentcreated "AddScriptToExecuteOnDocumentCreated-0.9.579-Interface ICoreWebView2 | Документы Microsoft"  
[Webview2ReferenceWpf09515MicrosoftWebExecutescriptasync]: ../reference/wpf/0-9-515/microsoft-web-webview2-wpf-webview2.md#executescriptasync "Класс ExecuteScriptAsync-Microsoft. Web. WebView2. WPF. WebView2 | Документы Microsoft"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2 Samples-MicrosoftEdge/WebView2Samples | GitHub"  
