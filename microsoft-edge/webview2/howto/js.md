---
description: Сведения об использовании JavaScript в сложных сценариях в приложениях WebView2
title: Использование JavaScript в приложениях WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/15/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 0fd4e33b7cfc16dcd19a850147b6efbca8922a8e
ms.sourcegitcommit: 442de63da52d00c6dc27fa08ccdb736534127566
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "11120073"
---
# Использование JavaScript в WebView для расширенных сценариев  

Использование JavaScript в элементах управления WebView2 позволяет настраивать собственные приложения в соответствии с вашими потребностями.  В этой статье рассказывается о том, как использовать JavaScript в WebView2, а также о том, как разрабатывать дополнительные функции и функции WebView2.  

## Перед началом работы  

В этой статье предполагается, что у вас уже есть рабочий проект.  Если у вас нет проекта и вы хотите подписаться на него, перейдите в [Руководство Приступая к работе с WebView2][Webview2GettingstartedWpf].  

## Основные функции WebView2  

Чтобы приступить к внедрению JavaScript в приложение WebView, воспользуйтесь приведенными ниже функциями.  

| API  | Описание  |
|:--- |:--- |  
| [ExecuteScriptAsync][Webview2ReferenceWpfMicrosoftWebExecutescriptasync] | Запустите JavaScript в элементе управления WebView. Дополнительные сведения можно найти в учебнике Приступая к работе. |
| [OnDocumentCreatedAsync][Webview2ReferenceWin32Icorewebview2Addscripttoexecuteondocumentcreated] | Выполняется, когда создается объектная модель документа \ (DOM \). |
      
## Сценарий: Запуск выделенного файла сценария  

В этом разделе можно получить доступ к выделенному файлу JavaScript из элемента управления WebView2.  

> [!NOTE]
> Несмотря на то, что написание встроенного кода JavaScript может быть эффективным для быстрых команд JavaScript, вы теряете цветовые темы и форматирование линий JavaScript, что затрудняет создание больших фрагментов кода в Visual Studio.  

Чтобы решить эту проблему, создайте отдельный файл JavaScript с кодом, а затем передайте ссылку на этот файл с помощью `ExecuteScriptAsync` параметров.  

1.  Создайте `.js` файл в проекте и добавьте код JavaScript, который необходимо выполнить.  Например, создайте файл с именем `script.js` .  
1.  Преобразуйте файл JavaScript в строку, которая передается `ExecuteScriptAsync` .  
    1.  Чтобы преобразовать файл JavaScript в строку, скопируйте следующий фрагмент кода.  
        
        ```csharp
        string text = System.IO.File.ReadAllText(@"C:\PATH_TO_YOUR_FILE\script.js");
        ```  
        
    1.  Вставьте код в `MainWindow.xaml.cs` .  
1.  Передайте текстовую переменную с помощью `ExecuteScriptAsync` .  
    
    ```csharp
    await webView.CoreWebView2.ExecuteScriptAsync(text);
    ```  

## Сценарий: Удаление функции перетаскивания  

В этом разделе вы можете удалить функцию перетаскивания из элемента управления WebView2 с помощью JavaScript.  

Для начала ознакомьтесь с текущими возможностями перетаскивания.  

1.  Создание `.txt` файла для перетаскивания.  Например, можно создать файл с именем `contoso.txt` и добавить в него текст.  
1.  Запустите проект.  
1.  Перетащите `contoso.txt` файл на элемент управления WebView.  Откроется новое окно, которое является результатом кода в примере проекта.  
    
    :::image type="complex" source="./media/dragtext.png" alt-text="Результат перетаскивания contoso.txt" lightbox="./media/dragtext.png":::
       Результат перетаскивания contoso.txt  
    :::image-end:::  

Теперь добавьте код для удаления функции перетаскивания из элемента управления WebView2.  

1.  Скопируйте и вставьте следующий фрагмент кода `InitializeAsync()` в `MainWindow.xaml.cs` .   
            
    ```csharp   
    await webView.CoreWebView2.ExecuteScriptAsync("window.addEventListener('dragover',function(e){e.preventDefault();},false);");
    
    await webView.CoreWebView2.ExecuteScriptAsync("window.addEventListener('drop',function(e){" +
    "e.preventDefault();" +
    "console.log(e.dataTransfer);" +
    "console.log(e.dataTransfer.files[0])" +
    "}, false);");
    ```  
          
1.  Запустите проект.  
1.  Попробуйте перетащить `contoso.txt` .  Убедитесь, что вы не можете перетаскивать.  

## Сценарий: удаление контекстного меню  

В этом разделе удалите контекстное меню по умолчанию из элемента управления WebView2.  

Для начала ознакомьтесь с текущими функциями контекстного меню.  

1.  Запустите проект.  
1.  Наведите указатель мыши на элемент управления WebView2 и откройте контекстное меню, щелкнув его правой кнопкой мыши.  В контекстном меню отображаются варианты по умолчанию.  
    
    :::image type="complex" source="./media/contextmenu.png" alt-text="Результат перетаскивания contoso.txt" lightbox="./media/contextmenu.png":::
       Контекстное меню, в котором отображаются варианты по умолчанию  
    :::image-end:::  
    
Теперь добавьте код для удаления функциональных возможностей контекстного меню из элемента управления WebView2.  

1.  Скопируйте и вставьте следующий фрагмент кода `InitializeAsync()` в `MainWindow.xaml.cs` .    
        
    ```csharp   
    await webView.CoreWebView2.ExecuteScriptAsync("window.addEventListener('contextmenu', window => {window.preventDefault();});");
    ```  

1.  Запустите код еще раз.  Убедитесь, что вы не можете открыть контекстное меню, щелкнув правой кнопкой мыши.  
   
## См. также  

*   Подробнее о том, как приступить к работе с WebView2, можно найти в разделе [WebView2 Start Guides][Webview2MainGettingStarted](начало работы).  
*   Чтобы получить исчерпывающий пример возможностей WebView2, перейдите в репозиторий [WebView2Samples][GithubMicrosoftedgeWebview2samples] на GitHub.  
*   Подробные сведения о API WebView2 можно найти в [справочнике по API][Webview2ApiReference].  
*   Для получения дополнительных сведений о WebView2 перейдите в раздел [WebView2 Resources (ресурсы][Webview2MainNextSteps]).  

## Знакомство с командой Microsoft Edge WebView  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../../devtools-guide-chromium.md "Инструменты разработчика Microsoft EDGE (Chromium) | Документы Microsoft"  


[Webview2ApiReference]: ../webview2-api-reference.md "Справочник по API Microsoft Edge WebView2 | Документы Microsoft"  
[Webview2GettingstartedWpf]: ../gettingstarted/wpf.md "Начало работы с WebView2 в WPF (Предварительная версия) | Документы Microsoft"  
[Webview2MainGettingStarted]: ../index.md#getting-started "Приступая к работе: знакомство с Microsoft Edge WebView2 (Предварительная версия) | Документы Microsoft"  
[Webview2MainNextSteps]: ../index.md#next-steps "Дальнейшие действия — введение в Microsoft Edge WebView2 (Предварительная версия) | Документы Microsoft"  
[Webview2ReferenceWin32Icorewebview2Addscripttoexecuteondocumentcreated]: /microsoft-edge/webview2/reference/win32/icorewebview2#addscripttoexecuteondocumentcreated "AddScriptToExecuteOnDocumentCreated-0.9.579-Interface ICoreWebView2 | Документы Microsoft"  
[Webview2ReferenceWpfMicrosoftWebExecutescriptasync]: /dotnet/api/microsoft.web.webview2.wpf.webview2.executescriptasync "WebView2.ExecuteScriptAsync (String) method (Microsoft. Web. WebView2. WPF) | Документы Microsoft"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2 Samples-MicrosoftEdge/WebView2Samples | GitHub"  
