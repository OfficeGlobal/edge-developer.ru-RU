---
description: Автоматизация и тестирование в Microsoft Edge с помощью Puppeteer
title: Puppeteer
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft EDGE, веб-разработка, разработчик, инструменты, Автоматизация и тестирование
ms.openlocfilehash: bef3f0d7472f7bc595998829546fb540041f20fc
ms.sourcegitcommit: b88d2a55a59db8373ff2bac275d3730977bf19c9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "10986159"
---
# <span data-ttu-id="cd7b6-104">Puppeteer</span><span class="sxs-lookup"><span data-stu-id="cd7b6-104">Puppeteer</span></span>  

<span data-ttu-id="cd7b6-105">[Puppeteer][|::ref1::|Main] — это библиотека [узлов][NodejsMain] , которая предоставляет интерфейс API высокого уровня для управления Microsoft Edge \ (Chromium \) по [протоколу DevTools][GithubChromedevtoolsProtocol].</span><span class="sxs-lookup"><span data-stu-id="cd7b6-105">[Puppeteer][|::ref1::|Main] is a [Node][NodejsMain] library which provides a high-level API to control Microsoft Edge \(Chromium\) over the [DevTools Protocol][GithubChromedevtoolsProtocol].</span></span>  <span data-ttu-id="cd7b6-106">Puppeteer по умолчанию работает без [монитора][WikiHeadlessBrowser] , что означает, что пользовательский интерфейс не отображается, а вместо этого необходимо использовать командную строку.</span><span class="sxs-lookup"><span data-stu-id="cd7b6-106">Puppeteer runs [headless][WikiHeadlessBrowser] by default, which means that you do not see a UI, and instead must use the command-line.</span></span>  <span data-ttu-id="cd7b6-107">Вы также можете настроить Puppeteer на выполнение полных \ (без монитора \) Microsoft EDGE или Chromium.</span><span class="sxs-lookup"><span data-stu-id="cd7b6-107">You may also configure Puppeteer to run full \(non-headless\) Microsoft Edge or Chromium as well.</span></span>  

<span data-ttu-id="cd7b6-108">По умолчанию при установке Puppeteer программа установки загружает последнюю версию [Chromium][ChromiumHome]— обозреватель Open-Source, на котором [также построен Microsoft Edge][MicrosoftBlogsWindowsExperience20181206].</span><span class="sxs-lookup"><span data-stu-id="cd7b6-108">By default, when you install Puppeteer, the installer downloads a recent version of [Chromium][ChromiumHome], the open-source browser that [Microsoft Edge is also built upon][MicrosoftBlogsWindowsExperience20181206].</span></span>  <span data-ttu-id="cd7b6-109">Если у вас установлен Microsoft Edge \ (Chromium \), вы можете использовать [puppeteer-Core][PuppeteerApivscore].</span><span class="sxs-lookup"><span data-stu-id="cd7b6-109">If you have Microsoft Edge \(Chromium\) installed, you may use [puppeteer-core][PuppeteerApivscore].</span></span>  `puppeteer-core` <span data-ttu-id="cd7b6-110">— Это упрощенная версия Puppeteer, которая запускает уже установленный браузер, например Microsoft Edge \ (Chromium \).</span><span class="sxs-lookup"><span data-stu-id="cd7b6-110">is a lightweight version of Puppeteer that launches an existing browser installation, like Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="cd7b6-111">Чтобы скачать Microsoft Edge \ (Chromium \), обратитесь к разделу [Загрузка каналов предварительной оценки Microsoft Edge][MicrosoftedgeinsiderDownload].</span><span class="sxs-lookup"><span data-stu-id="cd7b6-111">To download Microsoft Edge \(Chromium\), see [Download Microsoft Edge Insider Channels][MicrosoftedgeinsiderDownload].</span></span>

## <span data-ttu-id="cd7b6-112">Установка puppeteer-Core</span><span class="sxs-lookup"><span data-stu-id="cd7b6-112">Installing puppeteer-core</span></span>  

<span data-ttu-id="cd7b6-113">Вы можете добавить `puppeteer-core` на веб-сайт или в приложение одну из указанных ниже команд.</span><span class="sxs-lookup"><span data-stu-id="cd7b6-113">You may add `puppeteer-core` to your website or app with one of the following commands.</span></span>  

```shell
npm i puppeteer-core
```  

```shell
yarn add puppeteer-core
```  

## <span data-ttu-id="cd7b6-114">Запуск Microsoft Edge с puppeteer (Core)</span><span class="sxs-lookup"><span data-stu-id="cd7b6-114">Launch Microsoft Edge with puppeteer-core</span></span>  

> [!NOTE]
> `puppeteer-core` <span data-ttu-id="cd7b6-115">опирается на узел v 8.9.0 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="cd7b6-115">relies on Node v8.9.0 or later.</span></span>  <span data-ttu-id="cd7b6-116">В примере ниже используется элемент `async` / `await` , который поддерживается только в node v 7.6.0 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="cd7b6-116">The example below uses `async`/`await` which is only supported in Node v7.6.0 or later.</span></span>  <span data-ttu-id="cd7b6-117">Запустите `node -v` из командной строки, чтобы убедиться, что у вас есть совместимая версия Node.js.</span><span class="sxs-lookup"><span data-stu-id="cd7b6-117">Run `node -v` from the command-line to ensure you have a compatible version of Node.js.</span></span>  

`puppeteer-core` <span data-ttu-id="cd7b6-118">Знакомство с пользователями других платформ тестирования браузера, таких как веб- [дисковод][WebDriverEdgehtmlMain].</span><span class="sxs-lookup"><span data-stu-id="cd7b6-118">should be familiar to users of other browser-testing-frameworks like [WebDriver][WebDriverEdgehtmlMain].</span></span>  <span data-ttu-id="cd7b6-119">Вы создаете экземпляр браузера, открываете страницу, а затем управляете ею с помощью API Puppeteer.</span><span class="sxs-lookup"><span data-stu-id="cd7b6-119">You create an instance of the browser, open a page, and then manipulate it with the Puppeteer API.</span></span>  <span data-ttu-id="cd7b6-120">В приведенном ниже примере кода `puppeteer-core` запускается Microsoft Edge \ (Chromium \), осуществляется переход на `https://www.microsoftedgeinsider.com` снимок экрана и сохранение его как `example.png` .</span><span class="sxs-lookup"><span data-stu-id="cd7b6-120">In the following code sample, `puppeteer-core` launches Microsoft Edge \(Chromium\), navigates to `https://www.microsoftedgeinsider.com`, and saves a screenshot as `example.png`.</span></span>  

<span data-ttu-id="cd7b6-121">Скопируйте приведенный ниже пример кода и сохраните его как `example.js` .</span><span class="sxs-lookup"><span data-stu-id="cd7b6-121">Copy the code sample below and save it as `example.js`.</span></span>  

```javascript
const puppeteer = require('puppeteer-core');

(async () => {
  const browser = await puppeteer.launch({
    executablePath: 'C:\\Program Files (x86)\\Microsoft\\Edge Dev\\Application\\msedge.exe'
  });
  const page = await browser.newPage();
  await page.goto('https://www.microsoftedgeinsider.com');
  await page.screenshot({path: 'example.png'});

  await browser.close();
})();
```  

<span data-ttu-id="cd7b6-122">Измените `executablePath` этот элемент, чтобы он указывал на установленный Microsoft Edge \ (Chromium \).</span><span class="sxs-lookup"><span data-stu-id="cd7b6-122">Change `executablePath` to point to your installation of Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="cd7b6-123">Например, в macOS `executablePath` для Microsoft Edge Канарские должно быть установлено значение `/Applications/Microsoft\ Edge\ Canary.app/` .</span><span class="sxs-lookup"><span data-stu-id="cd7b6-123">For example, on macOS, the `executablePath` for Microsoft Edge Canary should be set to `/Applications/Microsoft\ Edge\ Canary.app/`.</span></span>  <span data-ttu-id="cd7b6-124">Чтобы найти `executablePath` `edge://version` путь к **исполняемому** файлу на этой странице, найдите и скопируйте его и установите пакет [Edge-paths][npmEdgePaths] с помощью одной из указанных ниже команд.</span><span class="sxs-lookup"><span data-stu-id="cd7b6-124">To find the `executablePath`, navigate to `edge://version` and copy the **Executable path** on that page or install the [edge-paths][npmEdgePaths] package with one of the following commands.</span></span>  

```shell
npm i edge-paths
```  

```shell
yarn add edge-paths
```  
 
<span data-ttu-id="cd7b6-125">В примере кода ниже используется пакет [Edge-paths][npmEdgePaths] , чтобы программным образом найти путь к установке Microsoft Edge \ (Chromium \) в операционной системе.</span><span class="sxs-lookup"><span data-stu-id="cd7b6-125">The code sample below uses the [edge-paths][npmEdgePaths] package to programmatically find the path to your installation of Microsoft Edge \(Chromium\) on your OS.</span></span>

```javascript
const edgePaths = require("edge-paths");

const EDGE_PATH = edgePaths.getEdgePath();
```

<span data-ttu-id="cd7b6-126">И, наконец, Set `executablePath: EDGE_PATH` in `example.js` .</span><span class="sxs-lookup"><span data-stu-id="cd7b6-126">Finally, set `executablePath: EDGE_PATH` in `example.js`.</span></span>  <span data-ttu-id="cd7b6-127">В конце необходимо сохранить изменения.</span><span class="sxs-lookup"><span data-stu-id="cd7b6-127">Save your changes.</span></span>  

> [!NOTE]
> <span data-ttu-id="cd7b6-128">Microsoft Edge \ (EdgeHTML \) не работает с другими приложениями `puppeteer-core` .</span><span class="sxs-lookup"><span data-stu-id="cd7b6-128">Microsoft Edge \(EdgeHTML\) does not work with `puppeteer-core`.</span></span>  <span data-ttu-id="cd7b6-129">Чтобы продолжить работу в этом примере, необходимо установить [каналы предварительной оценки Microsoft Edge][MicrosoftedgeinsiderDownload] .</span><span class="sxs-lookup"><span data-stu-id="cd7b6-129">You must install the [Microsoft Edge Insider channels][MicrosoftedgeinsiderDownload] to continue following this example.</span></span>  

<span data-ttu-id="cd7b6-130">Теперь запустите `example.js` из командной строки.</span><span class="sxs-lookup"><span data-stu-id="cd7b6-130">Now run `example.js` from the command-line.</span></span>  

```shell
node example.js
```  

`puppeteer-core` <span data-ttu-id="cd7b6-131">запускает Microsoft EDGE, переходит `https://www.microsoftedgeinsider.com` и сохраняет снимок экрана 800px x 600px страницы.</span><span class="sxs-lookup"><span data-stu-id="cd7b6-131">launches Microsoft Edge, navigates to `https://www.microsoftedgeinsider.com` and saves an 800px x 600px screenshot of the page.</span></span>  <span data-ttu-id="cd7b6-132">Вы можете настроить размер страницы с помощью [Page. setViewport ()][PuppeteerApipagesetviewport].</span><span class="sxs-lookup"><span data-stu-id="cd7b6-132">You are able to customize the page size with [page.setViewport()][PuppeteerApipagesetviewport].</span></span>  

:::image type="complex" source="./media/puppeteer-example.png" alt-text="Файл example.png, созданный example.js":::
   <span data-ttu-id="cd7b6-134">Рисунок 1: `example.png` файл, созданный с помощью</span><span class="sxs-lookup"><span data-stu-id="cd7b6-134">Figure 1:  The `example.png` file produced by</span></span> `example.js`  
:::image-end:::  

<!--  
> ##### Figure 1  
> The `example.png` file produced by `example.js`  
> ![The example.png file produced by example.js](./media/puppeteer-example.png)  
-->  

<span data-ttu-id="cd7b6-135">Это простой пример сценариев автоматизации и тестирования, включенных в Puppeteer и `puppeteer-core` .</span><span class="sxs-lookup"><span data-stu-id="cd7b6-135">This is just a simple example of the automation and testing scenarios enabled by Puppeteer and `puppeteer-core`.</span></span>  <span data-ttu-id="cd7b6-136">Дополнительные сведения о Puppeteer и том, как это работает, можно найти в статьях [Puppeteer][|::ref2::|Main].</span><span class="sxs-lookup"><span data-stu-id="cd7b6-136">For more information about Puppeteer and how it works, see [Puppeteer][|::ref2::|Main].</span></span>  

## <span data-ttu-id="cd7b6-137">Знакомство с командой Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="cd7b6-137">Getting in touch with the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="cd7b6-138">Группа разработчиков Microsoft Edge может услышать отзывы об использовании Puppeteer `puppeteer-core` и Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="cd7b6-138">The Microsoft Edge Developer team is eager to hear your feedback about using Puppeteer, `puppeteer-core`, and Microsoft Edge.</span></span>  <span data-ttu-id="cd7b6-139">С помощью значка " **Отправить отзыв** " в Microsoft Edge DevTools или твит [@EdgeDevTools][TwitterIntentTweetEdgedevtools] , чтобы группа Microsoft Edge знала, что вы думаете.</span><span class="sxs-lookup"><span data-stu-id="cd7b6-139">Use the **Send Feedback** icon in the Microsoft Edge DevTools or tweet [@EdgeDevTools][TwitterIntentTweetEdgedevtools] to let the Microsoft Edge team know what you think.</span></span>  


:::image type="complex" source="./devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png" alt-text="Файл example.png, созданный example.js":::
   <span data-ttu-id="cd7b6-141">Значок " **Отправить отзыв** " в Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="cd7b6-141">The **Send Feedback** icon in the Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!--  
> ##### Figure 2  
> The **Feedback** icon in the Microsoft Edge DevTools  
> ![The Feedback icon in the Microsoft Edge DevTools](./devtools-guide-chromium/media/devtools-feedback.png)  
-->  

<!--## See also  

*   [WebDriver (Chromium)][WebdriverChromiumMain]  
*   [WebDriver (EdgeHTML)][WebdriverEdgehtmlMain]  
*   [Chrome DevTools Protocol Viewer on GitHub][GithubChromedevtoolsProtocol]  
*   [Microsoft Edge: Making the web better through more open source collaboration on Microsoft Experience Blog][MicrosoftBlogsWindowsExperience20181206]  
*   [Download Microsoft Edge Insider Channels][MicrosoftedgeinsiderDownload]  
*   [Chromium on The Chromium Projects][ChromiumHome]  
*   [Node.js][NodejsMain]  
*   [Puppeteer][PuppeteerMain]  
*   [puppeteer vs. puppeteer-core][PuppeteerApivscore]  
*   [page.setViewport() on Puppeteer][PuppeteerApipagesetviewport]  
*   [Headless browser on Wikipedia][WikiHeadlessBrowser]  -->  

<!-- image links -->  

<!-- links -->  

[WebdriverChromiumMain]: ./webdriver-chromium.md "Chromium"  
[WebdriverEdgehtmlMain]: ./webdriver.md "EdgeHTML"  

[GithubChromedevtoolsProtocol]: https://chromedevtools.github.io/devtools-protocol "Средство просмотра протоколов Chrome DevTools | GitHub"  

[MicrosoftBlogsWindowsExperience20181206]: https://blogs.windows.com/windowsexperience/2018/12/06/microsoft-edge-making-the-web-better-through-more-open-source-collaboration "Microsoft Edge: улучшение веб-сайта с помощью более эффективной работы в открытых источниках | Блог Microsoft Experience"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Скачайте каналы предварительной оценки Microsoft Edge"  

[ChromiumHome]: https://www.chromium.org/Home "Chromium | Проекты Chromium"  

[NodejsMain]: https://nodejs.org "Node.js"  

[npmEdgePaths]: https://www.npmjs.com/package/edge-paths "NPM | Пути к краям"

[PuppeteerMain]: https://pptr.dev "Puppeteer"  
[PuppeteerApivscore]: https://pptr.dev/#?product=Puppeteer&version=v2.0.0&show=api-puppeteer-vs-puppeteer-core "puppeteer и puppeteer-Core | Puppeteer"  
[PuppeteerApipagesetviewport]: https://pptr.dev/#?product=Puppeteer&version=v2.0.0&show=api-pagesetviewportviewport "Page. setViewport (окно просмотра) | Puppeteer"  

[TwitterIntentTweetEdgedevtools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools-опубликовать твит | Контента"  

[WikiHeadlessBrowser]: https://en.wikipedia.org/wiki/Headless_browser "Автономный браузер | Википедии"  
