---
description: Сведения о том, как протестировать веб-сайт или приложение в Microsoft EDGE, а также автоматизировать браузер с помощью Web Drive.
title: WebDriver (Chromium)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft EDGE, веб-разработка, HTML, CSS, сценарий JavaScript, разработчик, веб-дисковод, Selenium, тестирование, инструменты, Автоматизация и тестирование
ms.openlocfilehash: 8170820d7809f7c4c07f21c815f17a9438016305
ms.sourcegitcommit: b88d2a55a59db8373ff2bac275d3730977bf19c9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "10986215"
---
# <span data-ttu-id="23217-104">Использование Chromium для автоматизации тестов</span><span class="sxs-lookup"><span data-stu-id="23217-104">Use WebDriver (Chromium) for test automation</span></span>  

<span data-ttu-id="23217-105">С помощью этого устройства разработчики могут создавать автоматические тесты, имитирующие взаимодействие с пользователем.</span><span class="sxs-lookup"><span data-stu-id="23217-105">WebDriver enables developers to create automated tests that simulate user interaction.</span></span>  <span data-ttu-id="23217-106">Проверки и имитации для модулей-накопителей отличаются от модульных тестов JavaScript по следующим причинам.</span><span class="sxs-lookup"><span data-stu-id="23217-106">WebDriver tests and simulations differ from JavaScript unit tests because of the following reasons.</span></span> 
*   <span data-ttu-id="23217-107">Доступ к функциям и сведениям, недоступным для JavaScript, которые выполняются в браузерах.</span><span class="sxs-lookup"><span data-stu-id="23217-107">Accesses functionality and information not available to JavaScript running in browsers.</span></span>  
*   <span data-ttu-id="23217-108">Более точное моделирование событий пользователей и событий на уровне операционной системы.</span><span class="sxs-lookup"><span data-stu-id="23217-108">Simulates user events or OS-level events more accurately.</span></span>  
*   <span data-ttu-id="23217-109">Управление тестированием между несколькими окнами, вкладками и веб-страницами в одном тестовом сеансе.</span><span class="sxs-lookup"><span data-stu-id="23217-109">Manages testing across multiple windows, tabs, and webpages in a single test session.</span></span>  
*   <span data-ttu-id="23217-110">Запуск нескольких сеансов Microsoft EDGE на определенном компьютере.</span><span class="sxs-lookup"><span data-stu-id="23217-110">Runs multiple sessions of Microsoft Edge on a specific machine.</span></span>  

<span data-ttu-id="23217-111">В следующем разделе описано, как приступить к работе с веб-диском Microsoft Edge \ (Chromium \).</span><span class="sxs-lookup"><span data-stu-id="23217-111">The following section describes how to get started with WebDriver for Microsoft Edge \(Chromium\).</span></span>  

## <span data-ttu-id="23217-112">Установка Microsoft EDGE (Chromium)</span><span class="sxs-lookup"><span data-stu-id="23217-112">Install Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="23217-113">Убедитесь в том, что вы установили [Microsoft EDGE (Chromium)][MicrosoftEdge].</span><span class="sxs-lookup"><span data-stu-id="23217-113">Ensure you install [Microsoft Edge (Chromium)][MicrosoftEdge].</span></span>  <span data-ttu-id="23217-114">Чтобы убедиться в том, что у вас установлен Microsoft EDGE (Chromium), перейдите `edge://settings/help` в браузер и проверьте номер версии 75 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="23217-114">To confirm that you have Microsoft Edge (Chromium) installed, go to `edge://settings/help` in the browser, and verify the version number is Version 75 or later.</span></span>  

## <span data-ttu-id="23217-115">Скачать драйвер Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="23217-115">Download Microsoft Edge Driver</span></span>  

<span data-ttu-id="23217-116">Чтобы приступить к автоматизации тестов, выполните указанные ниже действия, чтобы убедиться, что версия веб – диска, установленная на вашем компьютере, совпадает с вашей версией браузера.</span><span class="sxs-lookup"><span data-stu-id="23217-116">To begin automating tests, use the following steps to ensure that the WebDriver version you install matches your browser version.</span></span>  

1.  <span data-ttu-id="23217-117">Перейдите в раздел, `edge://settings/help` чтобы получить версию Edge.</span><span class="sxs-lookup"><span data-stu-id="23217-117">Go to `edge://settings/help` to get the version of Edge.</span></span>  
    
    :::image type="complex" source="./media/webdriver-chromium/edge-version.png" alt-text="Номер сборки Microsoft Edge Канарские 14 января 2020 г.":::
       <span data-ttu-id="23217-119">Рисунок 1.</span><span class="sxs-lookup"><span data-stu-id="23217-119">Figure 1.</span></span>  <span data-ttu-id="23217-120">Номер сборки Microsoft Edge Канарские 14 января 2020 г.</span><span class="sxs-lookup"><span data-stu-id="23217-120">The build number for Microsoft Edge Canary on January 14, 2020</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="23217-121">Перейдите на страницу [загрузки драйвера Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriverDownloads] и скачайте драйвер, который соответствует номеру версии Edge.</span><span class="sxs-lookup"><span data-stu-id="23217-121">Navigate to the [Microsoft Edge Driver downloads][MicrosoftDeveloperEdgeToolsWebdriverDownloads] page and download the driver that matches the Edge version number.</span></span>  
    
    :::image type="complex" source="./media/webdriver-chromium/edge-driver-install.png" alt-text="Номер сборки Microsoft Edge Канарские 14 января 2020 г.":::
       <span data-ttu-id="23217-123">Рисунок 2.</span><span class="sxs-lookup"><span data-stu-id="23217-123">Figure 2.</span></span>  <span data-ttu-id="23217-124">Раздел "загружаемые файлы" на странице [драйвера Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriver]</span><span class="sxs-lookup"><span data-stu-id="23217-124">The Downloads section of the [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriver] page</span></span>
    :::image-end:::  
    
    > [!NOTE] 
    > <span data-ttu-id="23217-125">Дополнительные сведения об автоматизации тестирования с помощью Microsoft EDGE (EdgeHTML) можно найти в [веб-накопителе Microsoft для Microsoft EDGE (EdgeHTML)][Webdriver].</span><span class="sxs-lookup"><span data-stu-id="23217-125">For more information about test automation using Microsoft Edge (EdgeHTML), see [Microsoft WebDriver for Microsoft Edge (EdgeHTML)][Webdriver].</span></span>  

## <span data-ttu-id="23217-126">Выбор языковой привязки для веб-дисков</span><span class="sxs-lookup"><span data-stu-id="23217-126">Choose a WebDriver language binding</span></span>  

<span data-ttu-id="23217-127">Последний компонент, который необходимо скачать, — это языковый драйвер клиента для перевода кода \ (Python, Java, C \ #, Ruby, JavaScript \) в команды, которые драйвер Microsoft EDGE работает в Microsoft Edge \ (Chromium \).</span><span class="sxs-lookup"><span data-stu-id="23217-127">The last component you must download is a language-specific client driver to translate your code \(Python, Java, C\#, Ruby, JavaScript\) into commands the Microsoft Edge Driver runs in Microsoft Edge \(Chromium\).</span></span>  

<span data-ttu-id="23217-128">[Скачайте выбранную вами языковую привязку веб дисков][SeleniumDownloads].</span><span class="sxs-lookup"><span data-stu-id="23217-128">[Download the WebDriver language binding of your choice][SeleniumDownloads].</span></span>  <span data-ttu-id="23217-129">Команда Microsoft Edge рекомендует [Selenium 4,00-alpha05][NugetPackagesSeleniumWebdriver400alpha05] или более поздней версии, так как она поддерживает Microsoft Edge \ (Chromium \).</span><span class="sxs-lookup"><span data-stu-id="23217-129">The Microsoft Edge team recommends [Selenium 4.00-alpha05][NugetPackagesSeleniumWebdriver400alpha05] or later, because it supports Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="23217-130">Тем не менее, вы можете управлять Microsoft Edge \ (Chromium \) во всех более ранних версиях Selenium, включая текущую стабильную версию Selenium 3.</span><span class="sxs-lookup"><span data-stu-id="23217-130">However, you are able to control Microsoft Edge \(Chromium\) in all older versions of Selenium, including the current stable Selenium 3 release.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="23217-131">Если вы уже выполняли автоматизацию или тестирование Microsoft Edge \ (Chromium \) с использованием `ChromeDriver` и `ChromeOptions` классами, код веб-дисковода не будет работать в Microsoft Edge версии 80 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="23217-131">If you were previously automating or testing Microsoft Edge \(Chromium\) using `ChromeDriver` and `ChromeOptions` classes, your WebDriver code does not run on Microsoft Edge Version 80 or later.</span></span>  <span data-ttu-id="23217-132">Чтобы устранить эту проблему, обновите тесты, чтобы использовать этот `EdgeOptions` класс и установить [драйвер Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriver].</span><span class="sxs-lookup"><span data-stu-id="23217-132">To solve this problem, update your tests to use the `EdgeOptions` class and install [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriver].</span></span>  

### <span data-ttu-id="23217-133">Использование Selenium 3</span><span class="sxs-lookup"><span data-stu-id="23217-133">Use Selenium 3</span></span>  

<span data-ttu-id="23217-134">Если вы уже используете [Selenium 3][|::ref1::|], возможно, у вас есть тестирование браузера и хотите добавить покрытие для Microsoft Edge \ (Chromium \) без изменения версии Selenium.</span><span class="sxs-lookup"><span data-stu-id="23217-134">If you already use [Selenium 3][|::ref1::|], you may have existing browser tests and want to add coverage for Microsoft Edge \(Chromium\) without changing your version of Selenium.</span></span>  <span data-ttu-id="23217-135">Чтобы использовать [Selenium 3][|::ref2::|] для написания автоматических тестов как для Microsoft Edge \ (EdgeHTML \), так и для Microsoft Edge \ (Chromium \), установите для него пакет [средств Selenium для Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] , чтобы использовать обновленный драйвер.</span><span class="sxs-lookup"><span data-stu-id="23217-135">To use [Selenium 3][|::ref2::|] to write automated tests for both Microsoft Edge \(EdgeHTML\) and Microsoft Edge \(Chromium\), install the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] package to use the updated driver.</span></span>  <span data-ttu-id="23217-136">`EdgeDriver`Классы и `EdgeDriverService` компоненты, включенные в эти инструменты, полностью совместимы с встроенными эквивалентами в Selenium 4.</span><span class="sxs-lookup"><span data-stu-id="23217-136">The `EdgeDriver` and `EdgeDriverService` classes included in the tools are fully compatible with the built-in equivalents in Selenium 4.</span></span>  

<span data-ttu-id="23217-137">Чтобы добавить в проект [инструменты Selenium для Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] и [Selenium 3][|::ref3::|] , выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="23217-137">Use the following steps to add the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] and [Selenium 3][|::ref3::|] to your project.</span></span>

#### [<span data-ttu-id="23217-138">C#</span><span class="sxs-lookup"><span data-stu-id="23217-138">C#</span></span>](#tab/c-sharp/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="23217-139">Добавьте пакеты [Microsoft. Edge. SeleniumTools][NugetPackagesMicrosoftEdgeSeleniumtools] и [Selenium.][NugetPackagesSeleniumWebdriver31410] Package в проект .NET с помощью [инфраструктуры NuGet][NugetCLI] или [Visual Studio][VisualStudio].</span><span class="sxs-lookup"><span data-stu-id="23217-139">Add the [Microsoft.Edge.SeleniumTools][NugetPackagesMicrosoftEdgeSeleniumtools] and [Selenium.WebDriver][NugetPackagesSeleniumWebdriver31410] packages to your .NET project using the [NuGet CLI][NugetCLI] or [Visual Studio][VisualStudio].</span></span>

#### [<span data-ttu-id="23217-140">Языке</span><span class="sxs-lookup"><span data-stu-id="23217-140">Python</span></span>](#tab/python/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="23217-141">Используйте [PIP][PythonPip] для установки пакетов [msedge-Selenium-Tools][PythonSeleniumTools] и [Selenium][PythonSelenium] :</span><span class="sxs-lookup"><span data-stu-id="23217-141">Use [pip][PythonPip] to install the [msedge-selenium-tools][PythonSeleniumTools] and [selenium][PythonSelenium] packages:</span></span>

```python
pip install msedge-selenium-tools selenium==3.141
```  

#### [<span data-ttu-id="23217-142">JavaScript</span><span class="sxs-lookup"><span data-stu-id="23217-142">JavaScript</span></span>](#tab/javascript/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="23217-143">Использование [NPM][JavaScript|::ref4::|] для установки пакетов [Edge-Selenium-Tools][JavaScriptSeleniumTools] и [Selenium-][JavaScriptSelenium] :</span><span class="sxs-lookup"><span data-stu-id="23217-143">Use [npm][JavaScript|::ref4::|] to install the [edge-selenium-tools][JavaScriptSeleniumTools] and [selenium-webdriver][JavaScriptSelenium] packages:</span></span>

```javascript
npm install @microsoft/edge-selenium-tools selenium-webdriver
```  

* * *  

## <span data-ttu-id="23217-144">Использование веб-накопителя (Microsoft EDGE (Chromium))</span><span class="sxs-lookup"><span data-stu-id="23217-144">Use Microsoft Edge (Chromium) with WebDriver</span></span>

<span data-ttu-id="23217-145">Вы можете использовать следующие примеры с помощью Selenium 3 или 4.</span><span class="sxs-lookup"><span data-stu-id="23217-145">You may run the following examples using either Selenium 3 or 4.</span></span>  <span data-ttu-id="23217-146">Для использования с Selenium 3 необходимо установить пакет [средств Selenium для Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] .</span><span class="sxs-lookup"><span data-stu-id="23217-146">To use with Selenium 3, the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] package must be installed.</span></span>  

### <span data-ttu-id="23217-147">Основное использование</span><span class="sxs-lookup"><span data-stu-id="23217-147">Basic Usage</span></span>  

<span data-ttu-id="23217-148">Для использования в Microsoft Edge \ (EdgeHTML \) просто создайте экземпляр класса по умолчанию `EdgeDriver` .</span><span class="sxs-lookup"><span data-stu-id="23217-148">To use with Microsoft Edge \(EdgeHTML\), simply create a default instance of the `EdgeDriver` class.</span></span>

#### [<span data-ttu-id="23217-149">C#</span><span class="sxs-lookup"><span data-stu-id="23217-149">C#</span></span>](#tab/c-sharp/)  

<a id="basic-usage-code"></a>  

```csharp
var driver = new EdgeDriver();
```  

#### [<span data-ttu-id="23217-150">Языке</span><span class="sxs-lookup"><span data-stu-id="23217-150">Python</span></span>](#tab/python/)  

<a id="basic-usage-code"></a>  

```python
driver = Edge()
```  

#### [<span data-ttu-id="23217-151">JavaScript</span><span class="sxs-lookup"><span data-stu-id="23217-151">JavaScript</span></span>](#tab/javascript/)  

<a id="basic-usage-code"></a>  

```javascript
let driver = edge.Driver.createSession();
```  

* * *  

### <span data-ttu-id="23217-152">Управление Microsoft EDGE (Chromium)</span><span class="sxs-lookup"><span data-stu-id="23217-152">Driving Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="23217-153">Для использования с Microsoft Edge \ (Chromium \) создайте новый `EdgeDriver` класс и передайте ему `EdgeOptions` объект со `UseChromium` свойством, для которого задано значение `true` .</span><span class="sxs-lookup"><span data-stu-id="23217-153">To use with Microsoft Edge \(Chromium\), create a new `EdgeDriver` class and pass it the `EdgeOptions` object with the `UseChromium` property set to `true`.</span></span>  

#### [<span data-ttu-id="23217-154">C#</span><span class="sxs-lookup"><span data-stu-id="23217-154">C#</span></span>](#tab/c-sharp/)  

<a id="driving-microsoft-edge-chromium-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;

var driver = new EdgeDriver(options);
```  

#### [<span data-ttu-id="23217-155">Языке</span><span class="sxs-lookup"><span data-stu-id="23217-155">Python</span></span>](#tab/python/)  

<a id="driving-microsoft-edge-chromium-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True

driver = Edge(options)
```  

#### [<span data-ttu-id="23217-156">JavaScript</span><span class="sxs-lookup"><span data-stu-id="23217-156">JavaScript</span></span>](#tab/javascript/)  

<a id="driving-microsoft-edge-chromium-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);

let driver = edge.Driver.createSession(options);
```  

* * *  

> [!NOTE]
> <span data-ttu-id="23217-157">Если задано значение политики [DeveloperToolsAvailability][DeployedgePoliciesDevelopertoolsavailability] `2` , [драйвер Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriver] не может использовать Microsoft Edge [(Chromium)][MicrosoftEdge] , так как в драйвере используется [Microsoft Edge DevTools][DevToolsMain].</span><span class="sxs-lookup"><span data-stu-id="23217-157">If the [DeveloperToolsAvailability][DeployedgePoliciesDevelopertoolsavailability] policy is set to `2`, [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriver] is not be able to drive [Microsoft Edge (Chromium)][MicrosoftEdge] because the driver uses the [Microsoft Edge DevTools][DevToolsMain].</span></span>  <span data-ttu-id="23217-158">Убедитесь, что вы установили для политики [DeveloperToolsAvailability][DeployedgePoliciesDevelopertoolsavailability] значение " `0` или" `1` автоматизировать [Microsoft EDGE (Chromium)][MicrosoftEdge].</span><span class="sxs-lookup"><span data-stu-id="23217-158">Ensure you set the [DeveloperToolsAvailability][DeployedgePoliciesDevelopertoolsavailability] policy to `0` or `1` to automate [Microsoft Edge (Chromium)][MicrosoftEdge].</span></span>  

### <span data-ttu-id="23217-159">Выбор определенных двоичных файлов браузера (только Chromium)</span><span class="sxs-lookup"><span data-stu-id="23217-159">Choosing Specific Browser Binaries (Chromium-Only)</span></span>  

<span data-ttu-id="23217-160">Вы можете использовать этот `EdgeOptions` класс с определенными двоичными объектами Microsoft EDGE (Chromium).</span><span class="sxs-lookup"><span data-stu-id="23217-160">You may use the `EdgeOptions` class with specific binaries of Microsoft Edge (Chromium).</span></span>  <span data-ttu-id="23217-161">Например, вы можете выполнять тесты с помощью [каналов предварительной версии Microsoft Edge][MicrosoftedgeinsiderDownload] , таких как Microsoft Edge Beta.</span><span class="sxs-lookup"><span data-stu-id="23217-161">For example, you may run tests using the [Microsoft Edge preview channels][MicrosoftedgeinsiderDownload] such as Microsoft Edge Beta.</span></span>  

#### [<span data-ttu-id="23217-162">C#</span><span class="sxs-lookup"><span data-stu-id="23217-162">C#</span></span>](#tab/c-sharp/)  

<a id="choosing-specific-browser-binaries-chrome-only-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.BinaryLocation = @"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe";

var driver = new EdgeDriver(options);
```  

#### [<span data-ttu-id="23217-163">Языке</span><span class="sxs-lookup"><span data-stu-id="23217-163">Python</span></span>](#tab/python/)  

<a id="choosing-specific-browser-binaries-chrome-only-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.binary_location = r"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe"

driver = Edge(options)
```  

#### [<span data-ttu-id="23217-164">JavaScript</span><span class="sxs-lookup"><span data-stu-id="23217-164">JavaScript</span></span>](#tab/javascript/)  

<a id="choosing-specific-browser-binaries-chrome-only-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.setBinaryPath("C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe");

let driver = edge.Driver.createSession(options);
```  

* * *  

### <span data-ttu-id="23217-165">Настройка службы драйвера Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="23217-165">Customizing the Microsoft Edge Driver Service</span></span>  

#### [<span data-ttu-id="23217-166">C#</span><span class="sxs-lookup"><span data-stu-id="23217-166">C#</span></span>](#tab/c-sharp/)  

<a id="customizing-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="23217-167">Когда `EdgeDriver` экземпляр класса создается с помощью `EdgeOptions` класса, он создает и запускает соответствующий `EdgeDriverService` класс для Microsoft Edge \ (EdgeHTML \) или Microsoft Edge \ (Chromium \).</span><span class="sxs-lookup"><span data-stu-id="23217-167">When an `EdgeDriver` class instance is created using `EdgeOptions` class, it creates and launches the appropriate `EdgeDriverService` class for either Microsoft Edge \(EdgeHTML\) or Microsoft Edge \(Chromium\).</span></span>  

<span data-ttu-id="23217-168">Если вы хотите создать объект `EdgeDriverService` для Microsoft Edge \ (Chromium \) с помощью метода, создайте его `CreateChromiumService()` .</span><span class="sxs-lookup"><span data-stu-id="23217-168">If you want to create an `EdgeDriverService`, create one configured for Microsoft Edge \(Chromium\) using the `CreateChromiumService()` method.</span></span>  <span data-ttu-id="23217-169">Вы можете использовать дополнительные настройки, такие как включение подробного вывода журнала в приведенном ниже коде.</span><span class="sxs-lookup"><span data-stu-id="23217-169">You may find it useful for additional customizations like enabling verbose log output in the following code.</span></span>  

```csharp
using (var service = EdgeDriverService.CreateChromiumService())
{
    service.UseVerboseLogging = true;

    var driver = new EdgeDriver(service);
}
```  

> [!NOTE] 
><span data-ttu-id="23217-170">Вам не нужно предоставлять `EdgeOptions` объект при передаче `EdgeDriverService` `EdgeDriver` экземпляру.</span><span class="sxs-lookup"><span data-stu-id="23217-170">You do not need to provide the `EdgeOptions` object when passing `EdgeDriverService` to the `EdgeDriver` instance.</span></span> <span data-ttu-id="23217-171">`EdgeDriver`Класс использует параметры по умолчанию для Microsoft Edge \ (EdgeHTML \) или Microsoft Edge \ (Chromium \) в зависимости от предоставленной услуги.</span><span class="sxs-lookup"><span data-stu-id="23217-171">The `EdgeDriver` class uses the default options for either Microsoft Edge \(EdgeHTML\) or Microsoft Edge \(Chromium\) depending on the service you provide.</span></span>  
> <span data-ttu-id="23217-172">Тем не менее, если вы хотите предоставить `EdgeDriverService` оба `EdgeOptions` класса и классы, убедитесь, что они настроены для одной и той же версии Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="23217-172">However, if you want to provide both `EdgeDriverService` and `EdgeOptions` classes, ensure that both are configured for the same version of Microsoft Edge.</span></span>  <span data-ttu-id="23217-173">Например, невозможно использовать класс по умолчанию Microsoft EDGE (EdgeHTML) `EdgeDriverService` и свойства Chromium в `EdgeOptions` классе.</span><span class="sxs-lookup"><span data-stu-id="23217-173">For example, it is not possible to use a default Microsoft Edge (EdgeHTML) `EdgeDriverService` class and Chromium properties in the `EdgeOptions` class.</span></span>  <span data-ttu-id="23217-174">`EdgeDriver`Класс вызывает ошибку, чтобы предотвратить использование разных версий.</span><span class="sxs-lookup"><span data-stu-id="23217-174">The `EdgeDriver` class throws an error to prevent using different versions.</span></span>  

#### [<span data-ttu-id="23217-175">Языке</span><span class="sxs-lookup"><span data-stu-id="23217-175">Python</span></span>](#tab/python/)  

<a id="customizing-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="23217-176">При использовании Python `Edge` объект создает и управляет `EdgeService` .</span><span class="sxs-lookup"><span data-stu-id="23217-176">When using Python, the `Edge` object creates and manages the `EdgeService`.</span></span>  <span data-ttu-id="23217-177">Чтобы настроить `EdgeService` , передайте дополнительные аргументы объекту, `Edge` как указано в приведенном ниже коде.</span><span class="sxs-lookup"><span data-stu-id="23217-177">To configure the `EdgeService`, pass additional arguments to the `Edge` object as indicated in the following code.</span></span>  

```python
service_args = ['--verbose']
driver = Edge(service_args = service_args)
```  

#### [<span data-ttu-id="23217-178">JavaScript</span><span class="sxs-lookup"><span data-stu-id="23217-178">JavaScript</span></span>](#tab/javascript/)  

<a id="customizing-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="23217-179">При использовании JavaScript создайте и настройте `Service` класс с помощью `ServiceBuilder` класса.</span><span class="sxs-lookup"><span data-stu-id="23217-179">When using JavaScript, create and configure a `Service` with the `ServiceBuilder` class.</span></span>  <span data-ttu-id="23217-180">При необходимости вы можете передать `Service` объект в объект, `Driver` который запускает и останавливает службу.</span><span class="sxs-lookup"><span data-stu-id="23217-180">You may optionally pass the `Service` object to the `Driver` object which starts and stops the service for you.</span></span>  
<span data-ttu-id="23217-181">Чтобы настроить `Service` , выполните дополнительные методы в `ServiceBuilder` классе перед использованием `build()` метода.</span><span class="sxs-lookup"><span data-stu-id="23217-181">To configure the `Service`, run additional methods in the `ServiceBuilder` class before using the `build()` method.</span></span>  <span data-ttu-id="23217-182">Затем передается в `service` `Driver.createSession()` методе как параметр.</span><span class="sxs-lookup"><span data-stu-id="23217-182">Then pass the `service` as a parameter in the `Driver.createSession()` method.</span></span>  

```javascript
let service = new edge.ServiceBuilder().enableVerboseLogging().build();
let driver = edge.Driver.createSession(options, service);
```  

* * * 

### <span data-ttu-id="23217-183">Использование параметров, специфичных для Chromium</span><span class="sxs-lookup"><span data-stu-id="23217-183">Use Chromium-Specific Options</span></span>  

<span data-ttu-id="23217-184">Если `UseChromium` для свойства задано значение `true` , вы можете использовать `EdgeOptions` Этот класс для доступа к таким же [свойствам и методам Chromium][SeleniumWebDriverChromeoptionsClass] , что и при автоматизации других браузеров Chromium.</span><span class="sxs-lookup"><span data-stu-id="23217-184">If you set the `UseChromium` property to `true`, you are able to use the `EdgeOptions` class to access the same [Chromium-specific properties and methods][SeleniumWebDriverChromeoptionsClass] as when you automate other Chromium browsers.</span></span>  

#### [<span data-ttu-id="23217-185">C#</span><span class="sxs-lookup"><span data-stu-id="23217-185">C#</span></span>](#tab/c-sharp/)  

<a id="using-chromium-specific-options-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.AddArgument("headless");
options.AddArgument("disable-gpu");
```  

#### [<span data-ttu-id="23217-186">Языке</span><span class="sxs-lookup"><span data-stu-id="23217-186">Python</span></span>](#tab/python/)  

<a id="using-chromium-specific-options-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.add_argument("headless")
options.add_argument("disable-gpu")
```  

#### [<span data-ttu-id="23217-187">JavaScript</span><span class="sxs-lookup"><span data-stu-id="23217-187">JavaScript</span></span>](#tab/javascript/)  

<a id="using-chromium-specific-options-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.addArguments("headless");
options.addArguments("disable-gpu");
```

* * *  
> [!NOTE]
> <span data-ttu-id="23217-188">Если `UseChromium` свойство имеет значение `true` , вы не можете пользоваться свойствами и методами для Microsoft Edge \ (EdgeHTML \).</span><span class="sxs-lookup"><span data-stu-id="23217-188">If the `UseChromium` property is set to `true`, you are not able to use properties and methods for Microsoft Edge \(EdgeHTML\).</span></span>  

## <span data-ttu-id="23217-189">Дополнительные параметры установки для устройства добавления новых устройств</span><span class="sxs-lookup"><span data-stu-id="23217-189">Additional WebDriver installation options</span></span>  

### <span data-ttu-id="23217-190">Шоколад</span><span class="sxs-lookup"><span data-stu-id="23217-190">Chocolatey</span></span>  

<span data-ttu-id="23217-191">Если вы используете [шоколад][Chocolatey] в качестве диспетчера пакетов, установите драйвер Microsoft EDGE, выполнив следующую команду:</span><span class="sxs-lookup"><span data-stu-id="23217-191">If you use [Chocolatey][Chocolatey] as your package manager, install the Microsoft Edge Driver by running the following command.</span></span>  

```console
choco install selenium-chromium-edge-driver
```  

<span data-ttu-id="23217-192">Дополнительные сведения можно найти [в разделе драйвер Selenium Chromium EDGE на шоколаде][ChocolateyPackagesSeleniumChromiumEdgeDriver].</span><span class="sxs-lookup"><span data-stu-id="23217-192">For more information, see [Selenium Chromium Edge Driver on Chocolatey][ChocolateyPackagesSeleniumChromiumEdgeDriver].</span></span>  

### <span data-ttu-id="23217-193">Docker</span><span class="sxs-lookup"><span data-stu-id="23217-193">Docker</span></span>  

<span data-ttu-id="23217-194">Если вы используете [закрепление][DockerHub], скачайте предварительно настроенное изображение с помощью Microsoft Edge \ (Chromium \) и [Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriver] , которое предустановлено, выполнив следующую команду:</span><span class="sxs-lookup"><span data-stu-id="23217-194">If you use [Docker][DockerHub], download a pre-configured image with Microsoft Edge \(Chromium\) and [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriver] pre-installed by running the following command.</span></span>  

```console
docker run -d -p 9515:9515 mcr.microsoft.com/msedge/msedgedriver
```  

<span data-ttu-id="23217-195">Дополнительные сведения можно найти [в разделе контейнер в центре Dock][DockerHubMsedgedriver].</span><span class="sxs-lookup"><span data-stu-id="23217-195">For more information, see [container on Docker Hub][DockerHubMsedgedriver].</span></span>  

## <span data-ttu-id="23217-196">Знакомство с командой Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="23217-196">Getting in touch with the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="23217-197">Группа Microsoft Edge – это информация о том, как использовать веб – диски, Selenium и Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="23217-197">The Microsoft Edge team is eager to hear your feedback about using WebDriver, Selenium, and Microsoft Edge.</span></span>  <span data-ttu-id="23217-198">С помощью значка **обратной связи** в Microsoft Edge DevTools или твит [@EdgeDevTools][TwitterTweetEdgeDevTools] , чтобы команда знала, что вы думаете.</span><span class="sxs-lookup"><span data-stu-id="23217-198">Use the **Feedback** icon in the Microsoft Edge DevTools or tweet [@EdgeDevTools][TwitterTweetEdgeDevTools] to let the team know what you think.</span></span>  


:::image type="complex" source="./devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png" alt-text="Номер сборки Microsoft Edge Канарские 14 января 2020 г.":::
   <span data-ttu-id="23217-200">Значок " **Отправить отзыв** " в Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="23217-200">The **Send Feedback** icon in the Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!-- image links -->  

<!-- links -->  

[DevToolsMain]: ./devtools-guide-chromium.md "Инструменты разработчика Microsoft EDGE (Chromium) | Документы Microsoft"
[Webdriver]: ./webdriver.md "[EdgeHTML) | Документы Microsoft"  

[DeployedgePoliciesDevelopertoolsavailability]: /deployedge/microsoft-edge-policies#developertoolsavailability "DeveloperToolsAvailability-Microsoft Edge-Policies | Документы Microsoft"  

[Chocolatey]: https://chocolatey.org "Шоколад | Шоколадное программное обеспечение"  
[ChocolateyPackagesSeleniumChromiumEdgeDriver]: https://chocolatey.org/packages/selenium-chromium-edge-driver "Драйвер Selenium Chromium Edge | Шоколад"  

[DockerHub]: https://hub.docker.com "Закрепляемый центр"  
[DockerHubMsedgedriver]: https://hub.docker.com/_/microsoft-msedge-msedgedriver?tab=description "msedgedriver | Закрепляемый центр"  

[GithubMicrosoftEdgeSeleniumTools]: https://github.com/microsoft/edge-selenium-tools "Microsoft/Edge-Selenium-Tools | GitHub"  
[GithubSeleniumHq]: https://github.com/SeleniumHQ/selenium "SeleniumHQ/Selenium | GitHub"  

[JavaScriptnpm]: https://www.npmjs.com/ "NPM"
[JavaScriptSeleniumTools]: https://www.npmjs.com/package/@microsoft/edge-selenium-tools "@microsoft/Edge-Selenium-Tools | NPM"
[JavaScriptSelenium]: https://www.npmjs.com/package/selenium-webdriver "Selenium-стример | NPM"

[MicrosoftDeveloperEdgeToolsWebdriver]: https://developer.microsoft.com/microsoft-edge/tools/webdriver "[Стример] | Разработчик Майкрософт"
[MicrosoftDeveloperEdgeToolsWebdriverDownloads]: https://developer.microsoft.com/microsoft-edge/tools/webdriver/#downloads "Загружаемые файлы — "[стример" | Разработчик Майкрософт"  

[MicrosoftEdge]: https://www.microsoft.com/edge "Скачать новый браузер Microsoft Edge"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Скачайте каналы предварительной оценки Microsoft Edge"  

[NugetCLI]:https://www.nuget.org/packages/NuGet.CommandLine/ "NuGet. CommandLine | Коллекция NuGet"
[NugetPackagesMicrosoftEdgeSeleniumtools]: https://www.nuget.org/packages/Microsoft.Edge.SeleniumTools "Microsoft. Edge. SeleniumTools | Коллекция NuGet"  
[NugetPackagesSeleniumWebdriver31410]: https://www.nuget.org/packages/Selenium.WebDriver/3.141.0 "Selenium. 3.141.0 | Коллекция NuGet"  
[NugetPackagesSeleniumWebdriver400alpha05]: https://www.nuget.org/packages/Selenium.WebDriver/4.0.0-alpha05 "Selenium. 4.0.0-alpha05 | Коллекция NuGet"  

[PythonPip]: https://pypi.org/project/pip/ "точка | PyPI"
[PythonSeleniumTools]: https://pypi.org/project/msedge-selenium-tools/ "msedge-Selenium-Tools | PyPI"
[PythonSelenium]: https://pypi.org/project/selenium/ "Selenium | PyPI"

[SeleniumHQ]: https://www.selenium.dev "SeleniumHQ"  
[SeleniumDownloads]: https://selenium.dev/downloads "Загрузки | Selenium"  
[SeleniumWebDriverChromeoptionsClass]: https://www.selenium.dev/selenium/docs/api/dotnet/?topic=html/T_OpenQA_Selenium_Chrome_ChromeOptions.htm "Класс ChromeOptions-стример | Selenium"  

[TwitterTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Публикация твита"  

[VisualStudio]: https://visualstudio.microsoft.com/ "Visual Studio"

[W3CWebdriver]: https://w3.org/TR/webdriver2 "Довода"  

[WikiHeadlessBrowser]: https://en.wikipedia.org/wiki/Headless_browser "Автономный браузер | Википедии"  
