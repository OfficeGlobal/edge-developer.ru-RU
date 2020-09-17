---
description: Расширение "Начало работы", часть 2
title: Динамическое добавление изображения NASA под тегом текста страницы с помощью сценариев содержимого
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge — Chromium, Web Development, HTML, CSS, JavaScript, разработчик, расширения
ms.openlocfilehash: fd2276c069116a7f69f06ae50f201e284b60f3ea
ms.sourcegitcommit: 744e2ecf42bcc427ae33e5dadbf6cd48ee0ab6a5
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/17/2020
ms.locfileid: "11016731"
---
# Динамическое добавление изображения NASA под тегом текста страницы с помощью сценариев содержимого  

<!--  
[Completed Extension Package Source for This Part][ArchiveExtensionGettingStartedPart2]  
-->  

## Обзор  

В части 2 Вы намерены обновить всплывающее меню таким образом, чтобы в нем не отображалось статическое изображение, которое вы раньше, но заменить это изображение заголовком и стандартной кнопкой HTML.  Эта кнопка, если она выбрана, передает изображение звезды, внедренное в расширение, на страницу содержимого.  Это изображение будет вставлено на вкладку активного браузера.  

*   Технологии расширения, описанные в этом руководстве  
    *   Добавление библиотек JavaScript в расширение  
    *   Предоставление расширений ресурсов вкладкам браузера  
    *   Включение страниц содержимого на существующие вкладки браузера  
    *   Прослушивание сообщений на страницах с содержимым из всплывающих окон и ответа на них  

## Удаление изображения из всплывающего окна и замена его на кнопку  

Сначала обновите `popup.html` файл с помощью перенаправленной текстовой разметки, в которой отображается заголовок и кнопка.  Эта кнопка вскоре будет программироваться, но теперь просто включите ссылку на пустой файл JavaScript `popup.js` .  Вот обновление HTML.  

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
        <h1>Show the NASA Picture of the Day</h1>
        <h2>(select the image to remove)</h2>
        <button id="sendmessageid">Display</button>
        <script src="popup.js"></script>
    </body>
</html>
```  

После того как вы обновите свое расширение и настроили значок запуска расширения, появится следующее всплывающее окно, содержащее кнопку отображения.  

:::image type="complex" source="./media/part2-popupdialog.png" alt-text="После нажатия значка расширения popup.html":::
   После нажатия значка расширения popup.html
:::image-end:::

<!--![popup.html display after pressing the Extension icon][ImagePart2Popupdialog]  -->  

## Обновлена стратегия отображения изображения в верхней части вкладки браузера  

После добавления кнопки Следующая задача — сделать так, чтобы она выместит `images/stars.jpeg` файл изображения в верхней части активной вкладки.  

Помните, что каждая вкладка имеет уникальный собственный поток, и расширение имеет отдельный поток.  Таким образом, необходимо сначала создать сценарий содержимого и внедрить этот сценарий содержимого на страницу вкладки.  После этого вы должны отправить сообщение с помощью всплывающего окна на странице вкладки, в которой будет отображаться этот сценарий содержимого и как его отобразить.  

## Создание всплывающего сценария JavaScript для отправки сообщения  

Сначала нужно создать `popup/popup.js` и добавить код, чтобы отправить сообщение в несозданный сценарий содержимого, который вы должны создать и внедрить на вкладку браузера.  Для этого следующий код добавляет `onclick` событие в всплывающую кнопку отображения.  

```javascript
const sendMessageId = document.getElementById("sendmessageid");
if (sendMessageId) {
  sendMessageId.onclick = function() {
    // do something
  };
}
```  

В `onclick` событии необходимо найти текущую вкладку браузера \ (если у вас есть только один из них, она будет находиться в одном случае).  После того как вы найдете эту вкладку, используйте `chrome.tabs.sendmessage` API-интерфейс расширения для отправки сообщения на эту вкладку.  

В этом сообщении нужно добавить URL-адрес изображения, которое вы хотите отобразить, и вы хотите отправить уникальный идентификатор, который должен быть назначен этому вставленному изображению.  Вы можете выбрать, чтобы JavaScript мог создавать содержимое, но для более поздних причин создать этот уникальный идентификатор здесь `popup.js` и передать его в сценарий содержимого, который еще не создан.  

Обновленный `popup/popup.js` файл.  Кроме того, вы можете передать текущий идентификатор табуляции, который вам понадобится в более позднем разделе, но пока не будет использован.  

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

## Создание звезд. JPEG, доступного на любой вкладке браузера  

Возможно, вы захотите заинтересовать причины, по которым следует `images/stars.jpeg` использовать `chrome.extension.getURL` API расширения Chrome вместо того, чтобы просто передавать относительный URL-адрес без дополнительного префикса, как в предыдущем разделе.  Таким образом, этот дополнительный префикс, возвращаемый `getUrl` с подключенным изображением, выглядит примерно так, как показано ниже.  

```http
extension://inigobacliaghocjiapeaaoemkjifjhp/images/stars.jpeg
```  

Причина в том, что вы вставляете изображение с помощью `src` атрибута `img` элемента на странице содержимого.  Страница содержимого выполняется в отдельном потоке, не совпадающем с потоком, на котором запущено расширение.  Для правильной работы вы должны предоставить статический файл изображения в качестве веб-актива.  

Для этого необходимо добавить в файл еще одну запись `manifest.json` .  Вы должны объявить изображение доступным на любом из вкладок браузера.  Этот параметр является следующим: \ (вы должны увидеть его в полном `manifest.json` файле ниже, когда вы добавите объявление сценария содержимого, которое появится на странице \).  

```json
"web_accessible_resources": [
    "images/*.jpeg"
]
```  

Теперь вы написали код в `popup.js` файле для отправки сообщения на страницу содержимого, внедренную на текущую активную вкладку, но вы не создали и не добавили эту страницу содержимого.  Сделайте это прямо сейчас.  

## Обновление manifest.jsдля контента и веб-доступа  

Обновленный `manifest.json` , который включает в себя `content-scripts` и `web_accessible_resources` следующий.  

```json
{
    "name": "NASA Picture of the day viewer",
    "version": "0.0.0.1",
    "manifest_version": 2,
    "description": "A Chromium Extension to show the NASA Picture of the Day.",
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

Добавленный раздел `content_scripts` .  Этот атрибут `matches` указывает на то `<all_urls>` , что все файлы, упомянутые в разделе " **content_scripts** ", вставляются во все вкладки браузера при загрузке каждой страницы.  Допустимые типы файлов, которые можно внедрить здесь: JavaScript и CSS.  Кроме того, вы добавите `libjquery.min.js` .  Вы можете включить эти возможности из файла download, упомянутого в верхней части раздела.  

## Добавление jQuery и понимание связанного потока  

В сценариях содержимого, которые вы вставляете, спланируйте использование jQuery \ ( `$` \).  Вы добавили версию minified для jQuery и помещаем ее в пакет расширения как `lib\jquery.min.js` .  Эти сценарии содержимого выполняются в отдельной изолированной среде сортировки, что означает, что jQuery, вставленный в `popup.js` страницу, не предоставляет доступ к содержимому.  

Имейте в виду, что даже если на вкладке браузер запущен JavaScript на загруженной веб-странице, доступ к содержимому не имеет доступа.  Этот внедренный JavaScript просто имеет доступ к фактической загруженной модели DOM на вкладке "браузер".  

## Добавление прослушивателя сообщений сценария содержимого  

Здесь показано, что `content-scripts\content.js` файл, который добавляется в каждую вкладку браузера на основе вашего `manifest.json` `content-scripts` раздела.  

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

Обратите внимание, что все указанные выше сценарии JavaScript — это регистрация `listener` с помощью `chrome.runtime.onMessage.addListener` метода API расширения.  Этот прослушиватель ждет сообщения, которые вы отправили ранее из `popup.js` описанных выше `chrome.tabs.sendMessage` методов расширения API.  

Первый параметр `addListener` метода — это функция, первый параметр которой — Request, — сведения о переданном сообщении.  Не забывайте, что `popup.js` при использовании `sendMessage` метода эти атрибуты первого параметра — `url` и `imageDivId` .  

Если событие обрабатывается прослушивателем, выполняется функция, которая является первым параметром.  Первый параметр этой функции — объект, которому назначены атрибуты `sendMessage` .  Эта функция просто обрабатывает три строки сценария jQuery.  

*   Первый динамически вставляет в заголовок DOM **\<style\>** раздел, который необходимо назначить `slide-image` `img` элементу как класс.  
*   Вторая — добавляет `img` элемент прямо под `body` вкладкой браузера, которому назначен класс, а также `slide-image` `imageDivId` как идентификатор этого элемента изображения.  
*   Третья добавляет `click` событие, которое охватывает все изображение, позволяя пользователю выбрать место на изображении и удалить его из страницы \ (вместе с прослушивателем событий \).  

## Добавление функции для удаления отображаемого изображения при выделении  

Теперь при переходе на любую страницу и выборе значка **расширения** всплывающее меню отображается следующим образом.  

:::image type="complex" source="./media/part2-popupdialog.png" alt-text="После нажатия значка расширения popup.html":::
   После нажатия значка расширения popup.html
:::image-end:::

<!--![popup.html display after pressing the Extension icon][ImagePart2Popupdialog]  -->  

После `Display` нажатия кнопки вы получите более ранний вариант.  Если вы выберете в любом месте `stars.jpeg` изображения, то этот элемент изображения удаляется, а страницы вкладок — на то, что было первоначально отображено.  

:::image type="complex" source="./media/part2-showingimage.png" alt-text="Изображение, показанное в браузере":::
   Изображение, показанное в браузере
:::image-end:::

<!--![The image showing in browser][ImagePart2Showingimage]  -->  

Вы создали расширение, которое успешно отправляет сообщение из всплывающего окна значка расширения, в динамически вставленный сценарий JavaScript, выполняющийся как содержимое на вкладке "браузер".  Введенное содержимое задает элемент изображения для отображения статичных звезд JPEG.  

<!-- image links -->  

<!--[ImagePart2Popupdialog]: ./media/part2-popupdialog.png "popup.html display after pressing the Extension icon"  -->  
<!--[ImagePart2Showingimage]: ./media/part2-showingimage.png "The image showing in browser"  -->

<!-- links -->  

[ArchiveExtensionGettingStartedPart2]: ./extension-source/extension-getting-started-part2.zip "Источник пакета расширения для этой части завершен | Документы Microsoft"  
