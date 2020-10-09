---
description: Динамическое добавление изображения NASA под тегом текста страницы с помощью сценариев содержимого
title: Создание учебника по расширению (часть 2)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge — Chromium, Web Development, HTML, CSS, JavaScript, разработчик, расширения
ms.openlocfilehash: 755b70635c93d7331ef3ac985625ba7ac5689679
ms.sourcegitcommit: 845a0d53a86bee3678f421adee26b3372cefce57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/08/2020
ms.locfileid: "11104716"
---
# <span data-ttu-id="718c4-104">Создание учебника по расширению (часть 2)</span><span class="sxs-lookup"><span data-stu-id="718c4-104">Create an extension tutorial Part 2</span></span>  
  
[<span data-ttu-id="718c4-105">Источник пакета расширения для этой части завершен</span><span class="sxs-lookup"><span data-stu-id="718c4-105">Completed Extension Package Source for This Part</span></span>][ArchiveExtensionGettingStartedPart2]    

## <span data-ttu-id="718c4-106">Обзор</span><span class="sxs-lookup"><span data-stu-id="718c4-106">Overview</span></span>  

<span data-ttu-id="718c4-107">В этом руководстве рассматриваются следующие технологии расширения.</span><span class="sxs-lookup"><span data-stu-id="718c4-107">This tutorial covers the following extension technologies.</span></span>
*   <span data-ttu-id="718c4-108">Добавление библиотек JavaScript в расширение</span><span class="sxs-lookup"><span data-stu-id="718c4-108">Injecting JavaScript libraries into extension</span></span>  
*   <span data-ttu-id="718c4-109">Предоставление расширений ресурсов вкладкам браузера</span><span class="sxs-lookup"><span data-stu-id="718c4-109">Exposing extension assets to browser tabs</span></span>  
*   <span data-ttu-id="718c4-110">Включение страниц содержимого на существующие вкладки браузера</span><span class="sxs-lookup"><span data-stu-id="718c4-110">Including content pages in existing browser tabs</span></span>  
*   <span data-ttu-id="718c4-111">Прослушивание сообщений на страницах с содержимым из всплывающих окон и ответа на них</span><span class="sxs-lookup"><span data-stu-id="718c4-111">Having content pages listen for messages from pop-ups and respond</span></span>  

<span data-ttu-id="718c4-112">Вы узнаете, как обновить всплывающее меню, чтобы заменить статичный запуск изображения на заголовок и стандартную кнопку HTML.</span><span class="sxs-lookup"><span data-stu-id="718c4-112">You'll learn to update your pop-up menu to replace your static starts image with a title and a standard HTML button.</span></span>  <span data-ttu-id="718c4-113">Эта кнопка, если она выбрана, передает изображение звезды, внедренное в расширение, на страницу содержимого.</span><span class="sxs-lookup"><span data-stu-id="718c4-113">That button, when selected, passes that stars image, which is embedded in the extension, to the content page.</span></span>  <span data-ttu-id="718c4-114">Это изображение будет вставлено на вкладку активного браузера. Чтобы получить дополнительные сведения, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="718c4-114">That image, is inserted into the active browser tab. Follow the below steps for further details.</span></span>

1.  <span data-ttu-id="718c4-115">Удаление изображения из всплывающего окна и замена его на кнопку</span><span class="sxs-lookup"><span data-stu-id="718c4-115">Remove the image from the pop-up and replace it with a button</span></span>  

<span data-ttu-id="718c4-116">Сначала обновите `popup.html` файл с помощью перенаправленной текстовой разметки, в которой отображается заголовок и кнопка.</span><span class="sxs-lookup"><span data-stu-id="718c4-116">First, update your `popup.html` file with some straight forward markup that displays a title and a button.</span></span>  <span data-ttu-id="718c4-117">Эта кнопка вскоре будет программироваться, но теперь просто включите ссылку на пустой файл JavaScript `popup.js` .</span><span class="sxs-lookup"><span data-stu-id="718c4-117">You'll program that button shortly, but for now, just include a reference to an empty JavaScript file `popup.js`.</span></span>  <span data-ttu-id="718c4-118">Вот обновление HTML.</span><span class="sxs-lookup"><span data-stu-id="718c4-118">Here is update HTML.</span></span>  

```html
<html>
    <head>
        <meta charset="utf-8" />
        <style>
            body {
                width: 500px;
            }
            button {
                background-color: #336dab;
                border: none;
                color: white;
                padding: 15px 32px;
                text-align: center;
                font-size: 16px;
            }
        </style>
    </head>
    <body>
        <h1>Show the NASA picture of the day</h1>
        <h2>(select the image to remove)</h2>
        <button id="sendmessageid">Display</button>
        <script src="popup.js"></script>
    </body>
</html>
```  

<span data-ttu-id="718c4-119">После того как вы обновите и откроете расширение, появится всплывающее окно с кнопкой "Показать".</span><span class="sxs-lookup"><span data-stu-id="718c4-119">After updating and opening the extension, a pop-up opens with a display button.</span></span>  

:::image type="complex" source="./media/part2-popupdialog.png" alt-text="После нажатия значка расширения popup.html":::
   <span data-ttu-id="718c4-121">После нажатия значка расширения popup.html</span><span class="sxs-lookup"><span data-stu-id="718c4-121">popup.html display after pressing the Extension icon</span></span>
:::image-end:::

<!--![popup.html display after pressing the Extension icon][ImagePart2Popupdialog]  -->  

2.  <span data-ttu-id="718c4-122">Стратегия обновления для отображения изображения в верхней части вкладки браузера</span><span class="sxs-lookup"><span data-stu-id="718c4-122">Update strategy to display image at the top of the browser tab</span></span>  

<span data-ttu-id="718c4-123">После добавления кнопки Следующая задача — сделать так, чтобы она выместит `images/stars.jpeg` файл изображения в верхней части активной вкладки.</span><span class="sxs-lookup"><span data-stu-id="718c4-123">After adding the button, the next task is to make it bring up the `images/stars.jpeg` image file at the top of the active tab page.</span></span>  

<span data-ttu-id="718c4-124">Не забывайте, что каждая вкладка запускается в собственном потоке.</span><span class="sxs-lookup"><span data-stu-id="718c4-124">Remember, each tab page runs in its own thread.</span></span> <span data-ttu-id="718c4-125">Кроме того, расширение использует другой поток.</span><span class="sxs-lookup"><span data-stu-id="718c4-125">Also, the extension uses a different thread.</span></span>  <span data-ttu-id="718c4-126">Сначала нужно создать сценарий содержимого, который будет добавлен на вкладку.</span><span class="sxs-lookup"><span data-stu-id="718c4-126">First, create a content script that is injected into the tab page.</span></span>  <span data-ttu-id="718c4-127">Затем отправьте сообщение со всплывающего окна на этот сценарий содержимого, запущенный на странице вкладки.</span><span class="sxs-lookup"><span data-stu-id="718c4-127">Then, send a message from your pop-up to that content script running on the tab page.</span></span> <span data-ttu-id="718c4-128">Сценарий содержимого получает сообщение, которое описывает изображение, которое должно отображаться.</span><span class="sxs-lookup"><span data-stu-id="718c4-128">The content script receives the message, which describes which image should be displayed.</span></span>  

3. <span data-ttu-id="718c4-129">Создание всплывающего сценария JavaScript для отправки сообщения</span><span class="sxs-lookup"><span data-stu-id="718c4-129">Create the pop-up JavaScript to send a message</span></span>  

<span data-ttu-id="718c4-130">Сначала нужно создать `popup/popup.js` и добавить код, чтобы отправить сообщение в несозданный сценарий содержимого, который вы должны создать и внедрить на вкладку браузера.  Для этого следующий код добавляет `onclick` событие в всплывающую кнопку отображения.</span><span class="sxs-lookup"><span data-stu-id="718c4-130">First, create `popup/popup.js` and add code to send a message to your not-yet-created content script that you must momentarily create and inject into your browser tab.  To do that, the following code adds an `onclick` event to your pop-up display button.</span></span>  

```javascript
const sendMessageId = document.getElementById("sendmessageid");
if (sendMessageId) {
  sendMessageId.onclick = function() {
    // do something
  };
}
```  

<span data-ttu-id="718c4-131">В `onclick` событии найдите текущую вкладку браузера.  Затем используйте `chrome.tabs.sendmessage` API расширения для отправки сообщения на эту вкладку.</span><span class="sxs-lookup"><span data-stu-id="718c4-131">In the `onclick` event, find the current browser tab.  Then, use the `chrome.tabs.sendmessage` Extension API to send a message to that tab.</span></span>  

<span data-ttu-id="718c4-132">В этом сообщении нужно добавить URL-адрес изображения, которое вы хотите отобразить.</span><span class="sxs-lookup"><span data-stu-id="718c4-132">In that message you must include the URL to the image you want to display.</span></span> <span data-ttu-id="718c4-133">Кроме того, можно отправить уникальный код для назначения вставленному изображению.</span><span class="sxs-lookup"><span data-stu-id="718c4-133">Also, send a unique ID to assign to the inserted image.</span></span>  <span data-ttu-id="718c4-134">Вы можете выбрать, чтобы JavaScript мог создавать содержимое, но для более поздних причин создать этот уникальный идентификатор здесь `popup.js` и передать его в сценарий содержимого, который еще не создан.</span><span class="sxs-lookup"><span data-stu-id="718c4-134">You may choose to let the content insertion JavaScript generate that, but for reasons that become apparent later, generate that unique ID here in `popup.js` and pass it to the not-yet-created content script.</span></span>  

<span data-ttu-id="718c4-135">В следующем фрагменте кода описан обновленный код в `popup/popup.js` .</span><span class="sxs-lookup"><span data-stu-id="718c4-135">The following code snippet outlines the updated code in `popup/popup.js`.</span></span>  <span data-ttu-id="718c4-136">Кроме того, передайте текущий идентификатор табуляции, который используется далее в этой статье.</span><span class="sxs-lookup"><span data-stu-id="718c4-136">Also, pass in the current tab ID, which is used later in this article.</span></span>  

```javascript
const sendMessageId = document.getElementById("sendmessageid");
if (sendMessageId) {
    sendMessageId.onclick = function() {
        chrome.tabs.query({ active: true, currentWindow: true }, function(tabs) {
            chrome.tabs.sendMessage(
                tabs[0].id,
                {
                    url: chrome.extension.getURL("images/stars.jpeg"),
                    imageDivId: `${guidGenerator()}`,
                    tabId: tabs[0].id
                },
                function(response) {
                    window.close();
                }
            );
            function guidGenerator() {
                const S4 = function () {
                    return (((1 + Math.random()) * 0x10000) | 0).toString(16).substring(1);
                };
                return (S4() + S4() + "-" + S4() + "-" + S4() + "-" + S4() + "-" + S4() + S4() + S4());
            }
        });
    };
}
```  

4. <span data-ttu-id="718c4-137">Создание звезд. JPEG, доступного на любой вкладке браузера</span><span class="sxs-lookup"><span data-stu-id="718c4-137">Make your stars.jpeg available from any browser tab</span></span>  

<span data-ttu-id="718c4-138">Вы, скорее всего, захотите заинтересовать причины, по которым следует `images/stars.jpeg` использовать `chrome.extension.getURL` API расширения Chrome вместо того, чтобы просто передавать относительный URL-адрес без дополнительного префикса, как в предыдущем разделе.</span><span class="sxs-lookup"><span data-stu-id="718c4-138">You're probably wondering why, when you pass the `images/stars.jpeg` must you use the `chrome.extension.getURL` chrome Extension API instead of just passing in the relative URL without the extra prefix like in the previous section.</span></span>  <span data-ttu-id="718c4-139">Таким образом, этот дополнительный префикс, возвращаемый `getUrl` с подключенным изображением, выглядит примерно так, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="718c4-139">By the way, that extra prefix, returned by `getUrl` with the image attached looks something like the following.</span></span>  

```http
extension://inigobacliaghocjiapeaaoemkjifjhp/images/stars.jpeg
```  

<span data-ttu-id="718c4-140">Причина заключается в том, что вы вставляете изображение с помощью `src` атрибута `img` элемента на странице содержимого.</span><span class="sxs-lookup"><span data-stu-id="718c4-140">The reason is that you're injecting the image using the `src` attribute of the `img` element into the content page.</span></span>  <span data-ttu-id="718c4-141">Страница содержимого выполняется в отдельном потоке, не совпадающем с потоком, на котором запущено расширение.</span><span class="sxs-lookup"><span data-stu-id="718c4-141">The content page is running on a unique thread that isn't the same as the thread running the Extension.</span></span>  <span data-ttu-id="718c4-142">Для правильной работы вы должны предоставить статический файл изображения в качестве веб-актива.</span><span class="sxs-lookup"><span data-stu-id="718c4-142">You must expose the static image file as a web asset for it to work correctly.</span></span>  

<span data-ttu-id="718c4-143">Добавьте в файл еще одну запись `manifest.json` , чтобы объявить, что изображение доступно для всех вкладок браузера.</span><span class="sxs-lookup"><span data-stu-id="718c4-143">Add another entry in the `manifest.json` file to declare that the image is available to all browser tabs.</span></span>  <span data-ttu-id="718c4-144">Этот параметр является следующим: \ (вы должны увидеть его в полном `manifest.json` файле ниже, когда вы добавите объявление сценария содержимого, которое появится на странице \).</span><span class="sxs-lookup"><span data-stu-id="718c4-144">That entry is as follows \(you should see it in the full `manifest.json` file below when you add the content script declaration coming up\).</span></span>  

```json
"web_accessible_resources": [
    "images/*.jpeg"
]
```  

<span data-ttu-id="718c4-145">Теперь вы написали код в `popup.js` файле для отправки сообщения на страницу содержимого, внедренную на текущую активную вкладку, но вы не создали и не добавите эту страницу содержимого.</span><span class="sxs-lookup"><span data-stu-id="718c4-145">You've now written the code in your `popup.js` file to send a message to the content page that is embedded on the current active tab page, but you haven't created and injected that content page.</span></span>  <span data-ttu-id="718c4-146">Сделайте это прямо сейчас.</span><span class="sxs-lookup"><span data-stu-id="718c4-146">Do that now.</span></span>  

5.  <span data-ttu-id="718c4-147">Обновление manifest.jsдля контента и веб-доступа</span><span class="sxs-lookup"><span data-stu-id="718c4-147">Update your manifest.json for content and web access</span></span>  

<span data-ttu-id="718c4-148">Обновленный `manifest.json` , который включает в себя `content-scripts` и `web_accessible_resources` следующий.</span><span class="sxs-lookup"><span data-stu-id="718c4-148">The updated `manifest.json` that includes the `content-scripts` and `web_accessible_resources` is as follows.</span></span>  

```json
{
    "name": "NASA picture of the day viewer",
    "version": "0.0.0.1",
    "manifest_version": 2,
    "description": "A Chromium extension to show the NASA picture of the day.",
    "icons": {
        "16": "icons/nasapod16x16.png",
        "32": "icons/nasapod32x32.png",
        "48": "icons/nasapod48x48.png",
        "128": "icons/nasapod128x128.png"
    },
    "browser_action": {
        "default_popup": "popup/popup.html"
    },
    "content_scripts": [
        {
            "matches": [
              "<all_urls>"
            ],
            "js": ["lib/jquery.min.js","content-scripts/content.js"]
        }
    ],
    "web_accessible_resources": [
        "images/*.jpeg"
    ]
}
```  

<span data-ttu-id="718c4-149">Добавленный раздел `content_scripts` .</span><span class="sxs-lookup"><span data-stu-id="718c4-149">The section you added is `content_scripts`.</span></span>  <span data-ttu-id="718c4-150">`matches`Для этого атрибута задано значение `<all_urls>` , которое означает, что все файлы на `content_scripts` вкладках браузера будут добавлены при загрузке каждой вкладки.</span><span class="sxs-lookup"><span data-stu-id="718c4-150">The `matches` attribute is set to `<all_urls>`, which means that all files in `content_scripts` are injected into all browser tab pages when each tab is loaded.</span></span>  <span data-ttu-id="718c4-151">Допустимые типы файлов, которые можно внедрить — это JavaScript и CSS.</span><span class="sxs-lookup"><span data-stu-id="718c4-151">The allowed files types that can be injected are JavaScript and CSS.</span></span>  <span data-ttu-id="718c4-152">Кроме того, вы добавите `libjquery.min.js` .</span><span class="sxs-lookup"><span data-stu-id="718c4-152">You also added `libjquery.min.js`.</span></span>  <span data-ttu-id="718c4-153">Вы можете включить эти возможности из скачивания, упомянутого в верхней части раздела.</span><span class="sxs-lookup"><span data-stu-id="718c4-153">You're able to include that from the download mentioned at the top of the section.</span></span>  

6. <span data-ttu-id="718c4-154">Добавление jQuery и понимание связанного потока</span><span class="sxs-lookup"><span data-stu-id="718c4-154">Add jQuery and understanding the associated thread</span></span>  

<span data-ttu-id="718c4-155">В сценариях содержимого, которые вы добавляете, спланируйте использование jQuery \ ( `$` \).</span><span class="sxs-lookup"><span data-stu-id="718c4-155">In the content scripts that you're injecting, plan on using jQuery \(`$`\).</span></span>  <span data-ttu-id="718c4-156">Вы добавили версию minified для jQuery и помещаем ее в пакет расширения как `lib\jquery.min.js` .</span><span class="sxs-lookup"><span data-stu-id="718c4-156">You added a minified version of jQuery and put it in your Extension package as `lib\jquery.min.js`.</span></span>  <span data-ttu-id="718c4-157">Эти сценарии содержимого выполняются в отдельных изолированных средах, что означает, что jQuery, вставленный в `popup.js` страницу, не является общим для содержимого.</span><span class="sxs-lookup"><span data-stu-id="718c4-157">These content scripts run in individual sandboxes, which means that the jQuery injected into the `popup.js` page isn't shared with the content.</span></span>  

<span data-ttu-id="718c4-158">Имейте в виду, что даже если на вкладке "браузер" запущен JavaScript на странице загруженной веб-страницы, доступ к содержимому не имеет.</span><span class="sxs-lookup"><span data-stu-id="718c4-158">Keep in mind that even if the browser tab has JavaScript running on it on the loaded web page, any content injected doesn't have access to that.</span></span>  <span data-ttu-id="718c4-159">Этот внедренный JavaScript просто имеет доступ к фактической загруженной модели DOM на вкладке "браузер".</span><span class="sxs-lookup"><span data-stu-id="718c4-159">That injected JavaScript just has access to the actual DOM loaded in that browser tab.</span></span>  

7. <span data-ttu-id="718c4-160">Добавление прослушивателя сообщений сценария содержимого</span><span class="sxs-lookup"><span data-stu-id="718c4-160">Add the content script message listener</span></span>  

<span data-ttu-id="718c4-161">Здесь показано, что `content-scripts\content.js` файл, который добавляется в каждую вкладку браузера на основе вашего `manifest.json` `content-scripts` раздела.</span><span class="sxs-lookup"><span data-stu-id="718c4-161">Here is that `content-scripts\content.js` file that gets injected into every browser tab page based on your `manifest.json` `content-scripts` section.</span></span>  

```javascript
chrome.runtime.onMessage.addListener(function(request, sender, sendResponse) {
    $("body").prepend(
        `<img  src="${request.url}" id="${request.imageDivId}"
               class="slide-image" /> `
    );
    $("head").prepend(
        `<style>
          .slide-image {
              height: auto;
              width: 100vw;
          }
        </style>`
    );
    $(`#${request.imageDivId}`).click(function() {
        $(`#${request.imageDivId}`).remove(`#${request.imageDivId}`);
    });
    sendResponse({ fromcontent: "This message is from content.js" });
});
```  

<span data-ttu-id="718c4-162">Обратите внимание, что все указанные выше сценарии JavaScript — это регистрация `listener` с помощью `chrome.runtime.onMessage.addListener` метода API расширения.</span><span class="sxs-lookup"><span data-stu-id="718c4-162">Notice that all the above JavaScript does is to register a `listener` using the `chrome.runtime.onMessage.addListener` Extension API method.</span></span>  <span data-ttu-id="718c4-163">Этот прослушиватель ждет сообщения, которые вы отправили ранее из `popup.js` описанных выше `chrome.tabs.sendMessage` методов расширения API.</span><span class="sxs-lookup"><span data-stu-id="718c4-163">This listener waits for messages like the one you sent from the `popup.js` described earlier with the `chrome.tabs.sendMessage` Extension API method.</span></span>  

<span data-ttu-id="718c4-164">Первый параметр `addListener` метода — это функция, первый параметр которой — Request, — сведения о переданном сообщении.</span><span class="sxs-lookup"><span data-stu-id="718c4-164">The first parameter of the `addListener` method is a function whose first parameter, request, is the details of the message being passed in.</span></span>  <span data-ttu-id="718c4-165">Не забывайте, что `popup.js` при использовании `sendMessage` метода эти атрибуты первого параметра — `url` и `imageDivId` .</span><span class="sxs-lookup"><span data-stu-id="718c4-165">Remember, from `popup.js`, when you used the `sendMessage` method, those attributes of the first parameter are `url` and `imageDivId`.</span></span>  

<span data-ttu-id="718c4-166">Если событие обрабатывается прослушивателем, выполняется функция, которая является первым параметром.</span><span class="sxs-lookup"><span data-stu-id="718c4-166">When an event is processed by the listener, the function that is the first parameter is run.</span></span>  <span data-ttu-id="718c4-167">Первый параметр этой функции — объект, которому назначены атрибуты `sendMessage` .</span><span class="sxs-lookup"><span data-stu-id="718c4-167">The first parameter of that function is an object that has attributes as assigned by `sendMessage`.</span></span>  <span data-ttu-id="718c4-168">Эта функция просто обрабатывает три строки сценария jQuery.</span><span class="sxs-lookup"><span data-stu-id="718c4-168">That function simply processes the three jQuery script lines.</span></span>  

*   <span data-ttu-id="718c4-169">Первая строка сценария динамически вставляется в заголовок DOM в **\<style\>** раздел, который необходимо назначить `slide-image` `img` элементу как класс.</span><span class="sxs-lookup"><span data-stu-id="718c4-169">The first script line dynamically inserts into the DOM header a **\<style\>** section that you must assign as a `slide-image` class to your `img` element.</span></span>  
*   <span data-ttu-id="718c4-170">Вторая строка сценария добавляет `img` элемент прямо под `body` вкладкой браузера, которому назначен класс, а также `slide-image` `imageDivId` как идентификатор этого элемента изображения.</span><span class="sxs-lookup"><span data-stu-id="718c4-170">The second script line appends an `img` element right below the `body` of your browser tab that has the `slide-image` class assigned as well as the `imageDivId` as the ID of that image element.</span></span>  
*   <span data-ttu-id="718c4-171">Третья строка сценария добавляет `click` событие, которое охватывает все изображение, позволяя пользователю выбрать любое место на изображении, и это изображение удаляется из страницы \ (вместе с прослушивателем событий \).</span><span class="sxs-lookup"><span data-stu-id="718c4-171">The third script line adds a `click` event that covers the entire image allowing the user to select anywhere on the image and that image is removed from the page \(along with it is event listener\).</span></span>  

8. <span data-ttu-id="718c4-172">Добавление функции для удаления отображаемого изображения при выделении</span><span class="sxs-lookup"><span data-stu-id="718c4-172">Add functionality to remove the displayed image when selected</span></span>  

<span data-ttu-id="718c4-173">Теперь при переходе на любую страницу и выборе значка **расширения** всплывающее меню отображается следующим образом.</span><span class="sxs-lookup"><span data-stu-id="718c4-173">Now, when you browse to any page and select your **Extension** icon, the pop-up menu is displayed as follows.</span></span>  

:::image type="complex" source="./media/part2-popupdialog.png" alt-text="После нажатия значка расширения popup.html":::
   <span data-ttu-id="718c4-175">После нажатия значка расширения popup.html</span><span class="sxs-lookup"><span data-stu-id="718c4-175">popup.html display after pressing the Extension icon</span></span>
:::image-end:::

<!--![popup.html display after pressing the Extension icon][ImagePart2Popupdialog]  -->  

<span data-ttu-id="718c4-176">После `Display` нажатия кнопки вы получите более ранний вариант.</span><span class="sxs-lookup"><span data-stu-id="718c4-176">When you select the `Display` button, you get what is below.</span></span>  <span data-ttu-id="718c4-177">Если вы выберете в любом месте `stars.jpeg` изображения, то этот элемент изображения удаляется, а страницы вкладок — на то, что было первоначально отображено.</span><span class="sxs-lookup"><span data-stu-id="718c4-177">If you select anywhere on the `stars.jpeg` image, that image element is removed and tab pages collapses back to what was originally displayed.</span></span>  

:::image type="complex" source="./media/part2-showingimage.png" alt-text="После нажатия значка расширения popup.html":::
   <span data-ttu-id="718c4-179">Изображение, показанное в браузере</span><span class="sxs-lookup"><span data-stu-id="718c4-179">The image showing in browser</span></span>
:::image-end:::

<span data-ttu-id="718c4-180">Вы создали расширение, которое успешно отправляет сообщение из всплывающего окна значка расширения, и динамически вставляет JavaScript, выполняющийся как содержимое на вкладке "браузер".  Введенное содержимое задает элемент изображения для отображения статичных звезд JPEG.</span><span class="sxs-lookup"><span data-stu-id="718c4-180">You've created an Extension that successfully sends a message from the extension icon pop-up, and dynamically inserted JavaScript running as content on the browser tab.  The injected content sets the image element to display your static stars jpeg.</span></span>  

<!-- image links -->  


<!-- links -->  

[ArchiveExtensionGettingStartedPart2]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/extension-getting-started-part2/extension-getting-started-part2 "Завершен источник пакета расширения | Документы Microsoft"  
