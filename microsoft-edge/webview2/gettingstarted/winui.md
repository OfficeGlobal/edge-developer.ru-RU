---
description: Руководство по началу работы с WebView2 для WinUI приложений
title: Приступая к работе с WebView2 для WinUI приложений
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/14/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, WebView2, WebView, WebView, winui, winui, EDGE, CoreWebView2, Browser Control, EDGE HTML, Приступая к работе, Приступая к работе, .NET
ms.openlocfilehash: df6ee7a7391337635a63a961f62317e5b8a67334
ms.sourcegitcommit: 61cc15d2fc89aee3e09cec48ef1e0e5bbf8d289a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/15/2020
ms.locfileid: "11119096"
---
# Начало работы с WebView2 в WinUI3 (Предварительная версия)  

В этой статье приступите к созданию первого приложения WebView2 с помощью WinUI3 и ознакомьтесь с основными возможностями [знакомства с Microsoft Edge WebView2 (Предварительная версия)][Webview2Index].  Дополнительные сведения об отдельных API можно найти в [справочнике API][GithubMicrosoftUiXamlSpecsWebview2].  

## Предварительные условия  

Перед переходом к следующей статье убедитесь, что вы установили приведенный ниже список предварительных условий.  

*   Windows 10 версии 1803 \ (сборка 17134 \) или более поздней версии.  Дополнительные сведения можно найти в [центре обновления Windows: вопросы и ответы][MicrosoftSupport12373].  
*   [Microsoft EDGE (Chromium) Канарские Channel][MicrosoftedgeinsiderDownload] в Windows 10, Windows 8,1 или Windows 7.  
*   Visual Studio 2019, версия 16,7 Preview 1.  Дополнительные сведения можно найти в разделе [Библиотека пользовательского интерфейса Windows версии 3 (июль 2020][WindowsAppsWinui3ConfigureYourDevEnvironment]г.).  
*   Версии [x64][WindowsDotnetcliBlobCoreSdk50100Preview4202681X64] и [x86][WindowsDotnetcliBlobCoreSdk50100Preview4202681X86] версии .NET 5 Preview 4.  
*   Расширение [шаблонов проектов WinUI 3][VisualstudioMarketplaceWinUiprojecttemplates] для Visual Studio 2019.  
Убедитесь, что вы [включите режим разработчика][WindowsUwpGetStartedEnableYourDeviceForDevelopment] , чтобы убедиться в том, что у вас есть доступ ко всем функциям Visual Studio.  

## Шаг 1: Создание проекта  

Начните с базового классического проекта, содержащего одно главное окно.  

1.  В Visual Studio выберите **создать новый проект**.  
1.  В раскрывающемся списке Проект выберите **C#**, **Windows**и **WinUI** соответственно.  
    
    :::image type="complex" source="./media/winui-gettingstarted-selections.png" alt-text="Диалоговое окно создания проекта Visual Studio для WinUI" lightbox="./media/winui-gettingstarted-selections.png":::
       Диалоговое окно создания проекта Visual Studio для WinUI  
    :::image-end:::  
    
1.  Выберите **пустое приложение, упакованное (WinUI на рабочем столе)**, а затем нажмите кнопку **Далее**.  
1.  Введите имя проекта, выберите нужные параметры и нажмите кнопку **создать**.  
1.  В **новом проекте универсальной платформы Windows**выберите указанные ниже значения, а затем нажмите кнопку **ОК**.  
    *   Целевая версия: **Windows 10, версия 1903 (сборка 18362)** или более поздняя.  
    *   Минимальная версия: **Windows 10, версия 1803 (сборка 17134)**.  
    
    :::image type="complex" source="./media/winui-gettingstarted-projecttype.png" alt-text="Диалоговое окно создания проекта Visual Studio для WinUI" lightbox="./media/winui-gettingstarted-projecttype.png":::
       Диалоговое окно создания проекта универсальной платформы Windows с выбранными значениями для целевой версии и минимальной версии.
    :::image-end:::  
    
1.  В обозревателе решений создаются два проекта.  
    *   **Название проекта (классическое приложение)**. Этот проект включает код для вашего приложения.  **App.XAML.CS** определяет `Application` класс, представляющий экземпляр приложения. **MainWindow.XAML.CS** определяет `MainWindow` класс, представляющий главное окно, которое отображается в экземпляре приложения.  Эти классы являются производными от типов в `Microsoft.UI.Xaml` пространстве имен WinUI.  
    
    *   **Имя проекта (пакет)**.  Этот проект — aWindows пакетов приложений Projectthat настроен для сборки приложения в MSIXный пакет для развертывания.  Проект содержит thepackage manifestfor вашего приложения, и по умолчанию он является запускаемым проектом для вашего решения. Дополнительные сведения можно найти [в разделе Настройка классического приложения для MSIX упаковки в Visual Studio][WindowsMsixDesktopToUwpPackagingDotNet] и [Справочник по схеме манифеста пакета для Windows 10][UwpSchemasAppxpackageUapmanifestRoot].
    
1.  В обозревателе решений откройте окно **MainWindow. XAML** , чтобы отобразить код.  Выберите `F5` , чтобы запустить проект и отобразить окно с кнопкой.  
    
## Шаг 2: Добавление элемента управления WebView2 в проект  

Затем добавьте элемент управления WebView2 в проект.  

1.  Open (открыть) `MainWindow.xaml` .  Добавьте пространство имен XAML WebView2 с помощью вставки в тег следующей строки `<Window/>` .  
    
    ```xml
    xmlns:controls="using:Microsoft.UI.Xaml.Controls"
    ```  
    
    Убедитесь, что ваш код `MainWindow.xaml` похож на следующий фрагмент кода.  
    
    ```xml
    <Window
          x:Class="WinUI_Sample.MainWindow"
          xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
          xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
          xmlns:local="using:WinUI_Sample"
          xmlns:d="http://schemas.microsoft.com/expression/blend/2008"
          xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
          mc:Ignorable="d"
          xmlns:controls="using:Microsoft.UI.Xaml.Controls"
          >
        
          <StackPanel Orientation="Horizontal" HorizontalAlignment="Center" VerticalAlignment="Center">
            <Button x:Name="myButton" Click="myButton_Click">Click Me</Button>
          </StackPanel>
    
    </Window>
    ```  
    
1.  Чтобы добавить элемент управления WebView2, замените `<StackPanel>` теги на следующий фрагмент кода.  `Source`Свойство задает начальный URI, отображаемый в элементе управления WebView2.  
    
    ```xml  
    <Grid>

        <Grid.RowDefinitions>
            <RowDefinition Height="Auto" />
            <RowDefinition Height="*" />
        </Grid.RowDefinitions>
        <Grid.ColumnDefinitions>
            <ColumnDefinition Width="*" />
            <ColumnDefinition Width="Auto" />
        </Grid.ColumnDefinitions>
        
        <controls:WebView2 x:Name="MyWebView"  Grid.Row="1" Grid.ColumnSpan="2" 
            Source="https://www.microsoft.com" HorizontalAlignment="Stretch" VerticalAlignment="Stretch" />
    
    </Grid>
    ```  
    
1.  Откройте `MainWindow.xaml.cs` следующую строку и закомментируйте ее.
    
    ```xml
        // myButton.Content = "Clicked";     
    ```  
    
1.  Выберите `F5` , чтобы выполнить сборку и запустить проект.  Убедитесь, что ваш элемент управления WebView2 отображается [https://www.microsoft.com][|::ref1::|Main] .  
    
    :::image type="complex" source="./media/winui-gettingstarted-part3.png" alt-text="Диалоговое окно создания проекта Visual Studio для WinUI" lightbox="./media/winui-gettingstarted-part3.png":::
       Элемент управления WebView2, на котором отображается сайт microsoft.com.  
    :::image-end:::  
    
## Шаг 3: Добавление элементов управления навигацией  

Разрешите пользователям управлять веб-страницей, которая отображается в элементе управления WebView2, добавив адресную строку в приложение. 

1.  В файле **MainWindow. XAML**скопируйте и вставьте следующий фрагмент кода внутри `Grid` элемента, содержащего `WebView2` элемент.  
    
    ```xml
        <TextBox Name="addressBar" Grid.Column="0"/>
        <Button x:Name="myButton" Grid.Column="1" Click="myButton_Click">Go</Button>
    ```  
    
    Убедитесь, что `Grid` элемент `MainWindow.xaml` похож на следующий фрагмент кода.  
    
    ```xml
    <Grid>
    
        <Grid.RowDefinitions>
            <RowDefinition Height="Auto" />
            <RowDefinition Height="*" />
        </Grid.RowDefinitions>
        <Grid.ColumnDefinitions>
            <ColumnDefinition Width="*" />
            <ColumnDefinition Width="Auto" />
        </Grid.ColumnDefinitions>
    
        <TextBox Name="addressBar" Grid.Column="0"/>
        <Button x:Name="myButton" Grid.Column="1" Click="myButton_Click">Go</Button>
        
        <WebView2 x:Name="MyWebView"  Grid.Row="1" Grid.ColumnSpan="2" 
            Source="https://www.microsoft.com" HorizontalAlignment="Stretch" VerticalAlignment="Stretch" />
    
    </Grid>
    ```  
    
1.  В **MainWindow.XAML.CS**Скопируйте приведенный ниже фрагмент кода `myButton_Click` , на который будет перемещаться по элементу управления WebView2 на URL-адрес, введенный в адресной строке.  
    
    ```csharp
    private void myButton_Click(object sender, RoutedEventArgs e)
    {
        try
        {
            Uri targetUri = new Uri(addressBar.Text);
            MyWebView.Source = targetUri;
        }
        catch (FormatException ex)
        {
            // Incorrect address entered.
        }
    }
    ```  
    
    Выберите `F5` , чтобы выполнить сборку и запустить проект.  Введите новый URL-адрес в адресной строке и нажмите кнопку **Перейти**.  Например, введите `https://www.bing.com` . 
    
    > [!NOTE]
    > Убедитесь в том, что в адресной строке используются полные URL-адреса. `ArgumentException` Если URL-адрес не начинается с or, возникают `http://` исключения `https://` .  
    
    :::image type="complex" source="./media/winui-gettingstarted-bing.png" alt-text="Диалоговое окно создания проекта Visual Studio для WinUI" lightbox="./media/winui-gettingstarted-bing.png":::
       Bing.com  
    :::image-end:::  
    
## Шаг 4 — события навигации  

Приложения, на которых размещаются элементы управления WebView2, прослушивают следующие события, возникающие в элементах управления WebView2 на этапе навигации веб-страницы.  

*   `NavigationStarting`  
*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
*   `NavigationCompleted`  

> [!NOTE]
> Переадресация HTTP вызывает несколько `NavigationStarting` событий.  

Дополнительные сведения можно найти в разделе [события навигации][Webviews2ConceptsNavigationEvents].  

При возникновении ошибок возникают следующие события, которые могут перейти на страницу ошибки.  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
     
В качестве примера использования событий Зарегистрируйте обработчик для `NavigationStarting` него, чтобы отменить все запросы, не ИСПОЛЬЗУЮЩИЕ HTTPS. `MainWindow.xaml.cs`Измените конструктор, чтобы `EnsureHttps` он регистрировал, и добавьте `EnsureHttps` функцию так, чтобы она соответствовала следующему фрагменту кода.  

```csharp
public MainWindow()
{
    InitializeComponent();
    MyWebView.NavigationStarting += EnsureHttps;
}

private void EnsureHttps(WebView2 sender, WebView2NavigationStartingEventArgs args)
{
    String uri = args.Uri;
    if (!uri.StartsWith("https://"))
    {
        args.Cancel = true;
    }
    else
    {
        addressBar.Text = uri;
    }
}
```  

Выберите `F5` , чтобы выполнить сборку и запустить проект.  Убедитесь, что Навигация заблокирована на сайтах HTTP и разрешена для HTTPS-сайтов.  

## Шаг 5: создание сценариев  

Ведущее приложение может внедрять код JavaScript в элементы управления WebView2 во время выполнения.  Вставленный JavaScript применяется ко всем новым документам верхнего уровня и дочерним кадрам до тех пор, пока не будет удален JavaScript.  Вставленный JavaScript запускается после создания глобального объекта, а также перед запуском любого другого сценария, включенного в документ HTML.  

В качестве примера добавьте сценарии, отправляющие предупреждение, когда пользователь переходит на сайты, не поддерживающие HTTPS.  Измените `EnsureHttps` функцию, чтобы внедрить сценарий в веб-содержимое с помощью [ExecuteScriptAsync][Webviews2ReferenceWpfMicrosoftWebExecutescriptasync].  

```csharp
private void EnsureHttps(WebView2 sender, WebView2NavigationStartingEventArgs args)
{
    String uri = args.Uri;
    if (!uri.StartsWith("https://"))
    {
        MyWebView.ExecuteScriptAsync($"alert('{uri} is not safe, try an https link')");
        args.Cancel = true;
    }
    else
    {
        addressBar.Text = uri;
    }
}
```  

Выберите `F5` , чтобы выполнить сборку и запустить проект.  Убедитесь, что ваше приложение отображает оповещение при переходе на сайт, который не использует HTTPS.  

:::image type="complex" source="./media/winui-gettingstarted-script.png" alt-text="Диалоговое окно создания проекта Visual Studio для WinUI" lightbox="./media/winui-gettingstarted-script.png":::
   Элемент управления WebView2, в котором отображается диалоговое окно оповещения
:::image-end:::  

Поздравляем! вы создали первое приложение WebView2.  

## Дальнейшие действия  

Наша группа в настоящее время использует дополнительные API WebView2.  Дополнительные сведения о текущем состоянии WebView2 API можно найти в описании [спецификации WebView2][GithubMicrosoftUiXamlSpecsWebview2].  

> [!NOTE]
> Объект CoreWebView2 WinRT может быть недоступен на момент отгрузки API WebView2. Чтобы узнать, какие API доступны для WebView2 элементов управления, ознакомьтесь со списком доступных API-интерфейсов в [WebView2 спецификации][GithubMicrosoftUiXamlSpecsWebview2] . 

Дополнительные сведения о возможностях WebView2: [WebView2 концепциям и руководствами по How-Toм][Webview2IndexNextSteps]и [репозиторием примеров использования WebView2][GithubMicrosoftedgeWebview2samplesMain].  

## Знакомство с командой Microsoft Edge WebView  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[Webview2Index]: ../index.md "Введение в Microsoft Edge WebView2 (Предварительная версия) | Документы Microsoft"  
[Webview2IndexNextSteps]: ../index.md#next-steps "Дальнейшие действия — введение в Microsoft Edge WebView2 (Предварительная версия) | Документы Microsoft"  
[Webviews2ConceptsNavigationEvents]: ../concepts/navigation-events.md "События навигации | Документы Microsoft"  
[Webviews2ReferenceWpfMicrosoftWebExecutescriptasync]: /dotnet/api/microsoft.web.webview2.wpf.webview2.executescriptasync "WebView2.ExecuteScriptAsync (String) method (Microsoft. Web. WebView2. WPF) | Документы Microsoft"  

[UwpSchemasAppxpackageUapmanifestRoot]: /uwp/schemas/appxpackage/uapmanifestschema/schema-root "Справочник по схеме манифеста пакета для Windows 10 | Документы Microsoft"  

[WindowsAppsWinui3ConfigureYourDevEnvironment]: /windows/apps/winui/winui3#configure-your-dev-environment "Настройка среды разработки — библиотеки пользовательского интерфейса Windows 3,0 Preview (Май 2020) | Документы Microsoft"  
[WindowsMsixDesktopToUwpPackagingDotNet]: /windows/msix/desktop/desktop-to-uwp-packaging-dot-net "Настройка классического приложения для MSIX упаковки в Visual Studio | Документы Microsoft"  
[WindowsUwpGetStartedEnableYourDeviceForDevelopment]: /windows/uwp/get-started/enable-your-device-for-development "Активация устройства для разработки | Документы Microsoft"  

[GithubMicrosoftUiXamlSpecsWebview2]: https://github.com/microsoft/microsoft-ui-xaml-specs/blob/master/active/WebView2/WebView2_spec.md "WebView2 Spec-Microsoft/Microsoft-UI-XAML-specs | GitHub"  

[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2 Samples-MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView Feedback-MicrosoftEdge/WebViewFeedback | GitHub"  

[MicrosoftMain]: https://www.microsoft.com "SMTP"  

[MicrosoftSupport12373]: https://support.microsoft.com/help/12373 "Обновление Windows: вопросы и ответы"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Скачайте каналы предварительной оценки Microsoft Edge"  

[WindowsDotnetcliBlobCoreSdk50100Preview4202681X86]: https://dotnetcli.blob.core.windows.net/dotnet/Sdk/5.0.100-preview.4.20268.1/dotnet-sdk-5.0.100-preview.4.20268.1-win-x86.exe "Скачать dotnet-sdk-5.0.100-preview.4.20268.1-win-x86.exe"  

[WindowsDotnetcliBlobCoreSdk50100Preview4202681X64]: https://dotnetcli.blob.core.windows.net/dotnet/Sdk/5.0.100-preview.4.20268.1/dotnet-sdk-5.0.100-preview.4.20268.1-win-x64.exe " dotnet-sdk-5.0.100-preview.4.20268.1-win-x64.exe"  

[VisualstudioMarketplaceWinUiprojecttemplates]: https://marketplace.visualstudio.com/items?itemName=Microsoft-WinUI.WinUIProjectTemplates "Шаблоны проектов WinUI 3"  
