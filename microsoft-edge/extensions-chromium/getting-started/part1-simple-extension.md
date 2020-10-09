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
# <span data-ttu-id="24ac1-104">Учебник по созданию расширения — часть 1</span><span class="sxs-lookup"><span data-stu-id="24ac1-104">Create an extension tutorial - Part 1</span></span>  

## <span data-ttu-id="24ac1-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="24ac1-105">Overview</span></span>  

<span data-ttu-id="24ac1-106">Цель этого учебника состоит в том, чтобы создать расширение Microsoft EDGE (Chromium), начиная с пустого каталога.</span><span class="sxs-lookup"><span data-stu-id="24ac1-106">The goal for this tutorial is to build a Microsoft Edge (Chromium) extension starting with an empty directory.</span></span> <span data-ttu-id="24ac1-107">Мы создадим расширение, которое будет выводится в виде фотографии на вашем дне NASA.</span><span class="sxs-lookup"><span data-stu-id="24ac1-107">We'll build an extension that pops up the NASA picture of the day.</span></span> <span data-ttu-id="24ac1-108">В этом учебнике вы узнаете, как создать расширение, выполнив следующие действия:</span><span class="sxs-lookup"><span data-stu-id="24ac1-108">In this tutorial, you'll learn how to create an extension by:</span></span>

*   <span data-ttu-id="24ac1-109">Создание `manifest.json` файла.</span><span class="sxs-lookup"><span data-stu-id="24ac1-109">Creating a `manifest.json` file.</span></span>  
*   <span data-ttu-id="24ac1-110">Добавление значков.</span><span class="sxs-lookup"><span data-stu-id="24ac1-110">Adding icons.</span></span>  
*   <span data-ttu-id="24ac1-111">Открытие всплывающего окна по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="24ac1-111">Opening a default pop-up dialog.</span></span>  

## <span data-ttu-id="24ac1-112">Подготовка</span><span class="sxs-lookup"><span data-stu-id="24ac1-112">Before you Begin</span></span>

<span data-ttu-id="24ac1-113">Если вы хотите протестировать заполненное расширение, которое будет построено в этом учебнике, скачайте [Исходный код][ArchiveExtensionGettingStartedPart1].</span><span class="sxs-lookup"><span data-stu-id="24ac1-113">If you'd like to test out the completed extension that you'll build in this tutorial, download the [source code][ArchiveExtensionGettingStartedPart1].</span></span>  

## <span data-ttu-id="24ac1-114">Действие 1: создание `manifest.json` файла</span><span class="sxs-lookup"><span data-stu-id="24ac1-114">Step 1: Create a `manifest.json` file</span></span>

<span data-ttu-id="24ac1-115">У каждого пакета расширения должен быть `manifest.json` файл в корне.</span><span class="sxs-lookup"><span data-stu-id="24ac1-115">Every extension package must have a `manifest.json` file at the root.</span></span>  <span data-ttu-id="24ac1-116">Манифест предоставляет сведения о расширении, версию пакета расширения, имя и описание расширения и т. д.</span><span class="sxs-lookup"><span data-stu-id="24ac1-116">The manifest provides details of your extension, the extension package version, the extension name and description, and so on.</span></span>  

<span data-ttu-id="24ac1-117">В приведенном ниже фрагменте кода отображаются основные сведения, необходимые для `manifest.json` файла.</span><span class="sxs-lookup"><span data-stu-id="24ac1-117">The following code snippet outlines the basic information needed in your `manifest.json` file.</span></span>  

```json
{
    "name": "NASA picture of the day viewer",
    "version": "0.0.0.1",
    "manifest_version": 2,
    "description": "A Chromium extension to display the NASA picture of the day."
}
```  

## <span data-ttu-id="24ac1-118">Действие 2: Добавление значков</span><span class="sxs-lookup"><span data-stu-id="24ac1-118">Step 2: Add icons</span></span>  

<span data-ttu-id="24ac1-119">Начните с создания `icons` каталога в проекте для хранения файлов изображений значков.</span><span class="sxs-lookup"><span data-stu-id="24ac1-119">Start by creating the `icons` directory in your project to store the icon image files.</span></span>  <span data-ttu-id="24ac1-120">Значки используются для фонового изображения кнопки, которую пользователь выбирает для запуска расширения.</span><span class="sxs-lookup"><span data-stu-id="24ac1-120">The icons are used for the background image of the button that users select to launch the extension.</span></span>  

:::image type="complex" source="./media/part1-badge1.png" alt-text="Значок на панели инструментов, чтобы открыть расширение":::
   <span data-ttu-id="24ac1-122">Значок на панели инструментов, чтобы открыть расширение</span><span class="sxs-lookup"><span data-stu-id="24ac1-122">Icon on the toolbar to open your extension</span></span>
:::image-end:::

<span data-ttu-id="24ac1-123">Для значков рекомендуется использовать:</span><span class="sxs-lookup"><span data-stu-id="24ac1-123">For icons, we recommend using:</span></span> 
*   `PNG` <span data-ttu-id="24ac1-124">формат значков, но вы также можете использовать `BMP` , `GIF` `ICO` или `JPEG` Форматировать.</span><span class="sxs-lookup"><span data-stu-id="24ac1-124">format for icons, but you may also use `BMP`, `GIF`, `ICO` or `JPEG` formats.</span></span>  
*   <span data-ttu-id="24ac1-125">Изображения размером 128 x 128 px, которые при необходимости изменяются в браузере.</span><span class="sxs-lookup"><span data-stu-id="24ac1-125">Images that are 128 x 128 px, which are resized by the browser if necessary.</span></span>  

<span data-ttu-id="24ac1-126">Каталоги проекта должны выглядеть так, как показано в приведенной ниже структуре.</span><span class="sxs-lookup"><span data-stu-id="24ac1-126">The directories of your project should be similar to the following structure.</span></span>   

```shell
└── part1
    ├── _manifest.json
    └── icons
        ├── nasapod16x16.png
        ├── nasapod32x32.png
        ├── nasapod48x48.png
        └── nasapod128x128.png
```  

<span data-ttu-id="24ac1-127">Затем добавьте значки в `manifest.json` файл.</span><span class="sxs-lookup"><span data-stu-id="24ac1-127">Next, add the icons to the `manifest.json` file.</span></span> <span data-ttu-id="24ac1-128">Обновите `manifest.json` файл со сведениями о значке, чтобы он соответствовал следующему фрагменту кода.</span><span class="sxs-lookup"><span data-stu-id="24ac1-128">Update your `manifest.json` file with the icons information so that it matches the following code snippet.</span></span> <span data-ttu-id="24ac1-129">`png`Файлы, перечисленные в приведенном ниже коде, доступны в файле download, упомянутом ранее в этой статье.</span><span class="sxs-lookup"><span data-stu-id="24ac1-129">The `png` files listed in the following code are available in the download file mentioned earlier in this article.</span></span>  

```json
{
    "name": "NASA picture of the day viewer",
    "version": "0.0.0.1",
    "manifest_version": 2,
    "description": "A chromium extension to show the NASA picture of the day.",
    "icons": {
        "16": "icons/nasapod16x16.png",
        "32": "icons/nasapod32x32.png",
        "48": "icons/nasapod48x48.png",
        "128": "icons/nasapod128x128.png"
    }
}
```  

## <span data-ttu-id="24ac1-130">Шаг 3: открытие всплывающего окна, используемого по умолчанию</span><span class="sxs-lookup"><span data-stu-id="24ac1-130">Step 3: Open a default pop-up dialog</span></span>  

<span data-ttu-id="24ac1-131">Теперь создайте `HTML` файл, который запускается, когда пользователь запускает расширение.</span><span class="sxs-lookup"><span data-stu-id="24ac1-131">Now, create a `HTML` file that's run when the user launches your extension.</span></span>  <span data-ttu-id="24ac1-132">Создайте HTML-файл, вызываемый `popup.html` в каталоге с именем `popup` .</span><span class="sxs-lookup"><span data-stu-id="24ac1-132">Create the HTML file called `popup.html` in a directory called `popup`.</span></span>  <span data-ttu-id="24ac1-133">Когда пользователи выбирают этот значок для запуска расширения, `popup/popup.html` он отображается как модальное диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="24ac1-133">When users select the icon to launch the extension, `popup/popup.html` is displayed as a modal dialog.</span></span>  

<span data-ttu-id="24ac1-134">Добавьте код из следующего фрагмента кода, чтобы `popup.html` отобразить изображение звезды.</span><span class="sxs-lookup"><span data-stu-id="24ac1-134">Add the code from the following code snippet to `popup.html` to display the stars image.</span></span>  

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

<span data-ttu-id="24ac1-135">Убедитесь, что вы добавите файл изображения `images/stars.jpeg` в папку изображений.</span><span class="sxs-lookup"><span data-stu-id="24ac1-135">Ensure that you add the image file `images/stars.jpeg` to the images folder.</span></span>  <span data-ttu-id="24ac1-136">Каталоги проекта должны выглядеть так, как показано в приведенной ниже структуре.</span><span class="sxs-lookup"><span data-stu-id="24ac1-136">The directories of your project should be similar to the following structure.</span></span>   

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

<span data-ttu-id="24ac1-137">Наконец, убедитесь, что вы зарегистрировали всплывающее окно в `manifest.json` разделе `browser_action` , как показано в следующем фрагменте кода.</span><span class="sxs-lookup"><span data-stu-id="24ac1-137">Finally, ensure you register the pop-up in `manifest.json` under `browser_action`, as shown in the following code snippet.</span></span>  

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

## <span data-ttu-id="24ac1-138">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="24ac1-138">Next steps</span></span>
<span data-ttu-id="24ac1-139">Это все, что вам нужно, чтобы разработать рабочее расширение.</span><span class="sxs-lookup"><span data-stu-id="24ac1-139">That's everything you need to develop a working extension.</span></span> <span data-ttu-id="24ac1-140">Теперь продолжайте неопубликованного и проверяйте свое расширение.</span><span class="sxs-lookup"><span data-stu-id="24ac1-140">Now, continue on to sideload and test your extension.</span></span> <span data-ttu-id="24ac1-141">Дополнительные сведения можно найти в разделе [неопубликованного расширения][TestExtensionSideload].</span><span class="sxs-lookup"><span data-stu-id="24ac1-141">For more information, see [Sideload an extension][TestExtensionSideload].</span></span>  


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
