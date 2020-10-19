---
description: Создание расширения, которое выводится на картину месяца на NASA
title: Учебник по созданию расширения — часть 1
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/23/2020
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: Edge — Chromium, Web Development, HTML, CSS, JavaScript, разработчик, расширения
ms.openlocfilehash: 3809bfac714621cf97184127132487ed93958a2f
ms.sourcegitcommit: 845a0d53a86bee3678f421adee26b3372cefce57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/08/2020
ms.locfileid: "11104709"
---
# Учебник по созданию расширения — часть 1  

## Обзор  

Цель этого учебника состоит в том, чтобы создать расширение Microsoft EDGE (Chromium), начиная с пустого каталога. Мы создадим расширение, которое будет выводится в виде фотографии на вашем дне NASA. В этом учебнике вы узнаете, как создать расширение, выполнив следующие действия:

*   Создание `manifest.json` файла.  
*   Добавление значков.  
*   Открытие всплывающего окна по умолчанию.  

## Подготовка

Если вы хотите протестировать заполненное расширение, которое будет построено в этом учебнике, скачайте [Исходный код][ArchiveExtensionGettingStartedPart1].  

## Действие 1: создание `manifest.json` файла

У каждого пакета расширения должен быть `manifest.json` файл в корне.  Манифест предоставляет сведения о расширении, версию пакета расширения, имя и описание расширения и т. д.  

В приведенном ниже фрагменте кода отображаются основные сведения, необходимые для `manifest.json` файла.  

```json
{
    "name": "NASA picture of the day viewer",
    "version": "0.0.0.1",
    "manifest_version": 2,
    "description": "A Chromium extension to display the NASA picture of the day."
}
```  

## Действие 2: Добавление значков  

Начните с создания `icons` каталога в проекте для хранения файлов изображений значков.  Значки используются для фонового изображения кнопки, которую пользователь выбирает для запуска расширения.  

:::image type="complex" source="./media/part1-badge1.png" alt-text="Значок на панели инструментов, чтобы открыть расширение":::
   Значок на панели инструментов, чтобы открыть расширение
:::image-end:::

Для значков рекомендуется использовать: 
*   `PNG` формат значков, но вы также можете использовать `BMP` , `GIF` `ICO` или `JPEG` Форматировать.  
*   Изображения размером 128 x 128 px, которые при необходимости изменяются в браузере.  

Каталоги проекта должны выглядеть так, как показано в приведенной ниже структуре.   

```shell
└── part1
    ├── _manifest.json
    └── icons
        ├── nasapod16x16.png
        ├── nasapod32x32.png
        ├── nasapod48x48.png
        └── nasapod128x128.png
```  

Затем добавьте значки в `manifest.json` файл. Обновите `manifest.json` файл со сведениями о значке, чтобы он соответствовал следующему фрагменту кода. `png`Файлы, перечисленные в приведенном ниже коде, доступны в файле download, упомянутом ранее в этой статье.  

```json
{
    &quot;name&quot;: &quot;NASA picture of the day viewer&quot;,
    &quot;version&quot;: &quot;0.0.0.1&quot;,
    &quot;manifest_version&quot;: 2,
    &quot;description&quot;: &quot;A chromium extension to show the NASA picture of the day.&quot;,
    &quot;icons&quot;: {
        &quot;16&quot;: &quot;icons/nasapod16x16.png&quot;,
        &quot;32&quot;: &quot;icons/nasapod32x32.png&quot;,
        &quot;48&quot;: &quot;icons/nasapod48x48.png&quot;,
        &quot;128&quot;: &quot;icons/nasapod128x128.png"
    }
}
```  

## Шаг 3: открытие всплывающего окна, используемого по умолчанию  

Теперь создайте `HTML` файл, который запускается, когда пользователь запускает расширение.  Создайте HTML-файл, вызываемый `popup.html` в каталоге с именем `popup` .  Когда пользователи выбирают этот значок для запуска расширения, `popup/popup.html` он отображается как модальное диалоговое окно.  

Добавьте код из следующего фрагмента кода, чтобы `popup.html` отобразить изображение звезды.  

```html
<html lang="en">
    <head>
        <meta charset="UTF-8" />
        <title>NASA picture of the day</title>
    </head>
    <body>
        <div>
            <img src="/images/stars.jpeg" alt="Display the stars image" />
        </div>
    </body>
</html>
```  

Убедитесь, что вы добавите файл изображения `images/stars.jpeg` в папку изображений.  Каталоги проекта должны выглядеть так, как показано в приведенной ниже структуре.   

```shell
└── part1
    ├── _manifest.json
    ├── icons
    │   ├── nasapod16x16.png
    │   ├── nasapod32x32.png
    │   ├── nasapod48x48.png
    │   └── nasapod128x128.png
    ├── images
    │   └── stars.jpeg
    └── popup
        └── popup.html
```  

Наконец, убедитесь, что вы зарегистрировали всплывающее окно в `manifest.json` разделе `browser_action` , как показано в следующем фрагменте кода.  

```json
{
    "name": "NASA picture of the day viewer",
    "version": "0.0.0.1",
    "manifest_version": 2,
    "description": "A chromium extension to display the NASA picture of the day.",
    "icons": {
        "16": "icons/nasapod16x16.png",
        "32": "icons/nasapod32x32.png",
        "48": "icons/nasapod48x48.png",
        "128": "icons/nasapod128x128.png"
    },
    "browser_action": {
        "default_popup": "popup/popup.html"
    }
}
```  

## Дальнейшие действия
Это все, что вам нужно, чтобы разработать рабочее расширение. Теперь продолжайте неопубликованного и проверяйте свое расширение. Дополнительные сведения можно найти в разделе [неопубликованного расширения][TestExtensionSideload].  


<!-- image links -->  

<!--[ImagePart1Heirarchy]: ./media/part1-heirarchy.png "Directory Structure"  -->  
<!--[ImagePart1Badge1]: ./media/part1-badge1.png "Toolbar Badge Icon"  -->  
<!--[ImagePart1Heirarchy1]: ./media/part1-heirarchy1.png "Directory Structure for Extension"  -->  
<!--[ImagePart1Threedots]: ./media/part1-threedots.png "Choose Extensions"  -->  
<!--[ImagePart1DevelopermodeToggle]: ./media/part1-developermode-toggle.png "Enable Developer Mode"  -->  
<!--[ImagePart1InstalledExtension]: ./media/part1-installed-extension.png "Installed Extensions"  -->  

<!-- links -->  

[ArchiveExtensionGettingStartedPart1]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/extension-getting-started-part1/part1 "Завершен источник пакета расширения | Документы Microsoft"

[TestExtensionSideload]: ./extension-sideloading.md "Проверка расширения (для неопубликованных приложений) | Документы Microsoft"
