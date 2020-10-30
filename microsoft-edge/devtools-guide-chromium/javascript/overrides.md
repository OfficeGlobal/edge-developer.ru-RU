---
description: Функция Overrides — это функция, которая находится в инструменте источники Microsoft Edge DevTools, позволяющей копировать ресурсы веб-страниц на жесткий диск.  Когда вы обновите веб-страницу, DevTools не загружайте ресурс, а вместо этого замените его локальной копией.
title: Переопределение ресурсов веб-страниц с помощью локальных копий в Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 579ebe92dc50571837e7e3caf8fb7c1a9989bc59
ms.sourcegitcommit: 9dcaf598f3930bcfab9f93ff63463beb98274de0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/30/2020
ms.locfileid: "11145197"
---
# <span data-ttu-id="d1b18-105">Переопределение ресурсов веб-страниц с помощью локальных копий в Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="d1b18-105">Override webpage resources with local copies using Microsoft Edge DevTools</span></span>  

<span data-ttu-id="d1b18-106">Иногда вам нужно исправить проблему на веб-странице, в которой нет доступа к данным или исправлениям, которые используют процесс создания медленной и сложной сборки.</span><span class="sxs-lookup"><span data-stu-id="d1b18-106">Sometimes you need to fix a problem on a webpage that you do not have access to or fixes involve a slow and complex build process.</span></span>  <span data-ttu-id="d1b18-107">Вы можете выполнять отладку и устранять неполадки всех типов в DevTools.</span><span class="sxs-lookup"><span data-stu-id="d1b18-107">You may debug and fix all kind of problems in DevTools.</span></span> <span data-ttu-id="d1b18-108">Но проблема в том, что изменения не сохраняются.</span><span class="sxs-lookup"><span data-stu-id="d1b18-108">But the problem is the changes do not persist.</span></span>  <span data-ttu-id="d1b18-109">После обновления файла вся работа будет пропала.</span><span class="sxs-lookup"><span data-stu-id="d1b18-109">After you refresh the file, all your work is gone.</span></span>  

<span data-ttu-id="d1b18-110">Функция Overrides в инструменте " [источники][DevToolsSourcesTool] " помогает решить эту проблему.</span><span class="sxs-lookup"><span data-stu-id="d1b18-110">The Overrides feature in the [Sources][DevToolsSourcesTool] tool helps you solve this problem.</span></span>  

<span data-ttu-id="d1b18-111">Теперь вы можете сделать ресурс текущей веб-страницей и сохранить ее локально.</span><span class="sxs-lookup"><span data-stu-id="d1b18-111">You may now take a resource of the current webpage and store it locally.</span></span>  <span data-ttu-id="d1b18-112">Когда вы обновите веб-страницу, браузер не загрузит ресурс с сервера.</span><span class="sxs-lookup"><span data-stu-id="d1b18-112">When you refresh the webpage, the browser does not load the resource from the server.</span></span>  <span data-ttu-id="d1b18-113">Вместо этого браузер заменяет его локальной копией ресурса.</span><span class="sxs-lookup"><span data-stu-id="d1b18-113">Instead the browser replaces it with your local copy of the resource.</span></span>  

## <span data-ttu-id="d1b18-114">Настройка локальной папки для хранения переопределений</span><span class="sxs-lookup"><span data-stu-id="d1b18-114">Setting up your local folder to store Overrides</span></span>  

1.  <span data-ttu-id="d1b18-115">В инструменте **источники** найдите несколько разделов в левой части экрана.</span><span class="sxs-lookup"><span data-stu-id="d1b18-115">In the **Sources** tool, find several sections on the left-hand side.</span></span>  <span data-ttu-id="d1b18-116">Если параметр **Переопределение** не отображается, нажмите кнопку</span><span class="sxs-lookup"><span data-stu-id="d1b18-116">If the **Overrides** option is not displayed, choose the</span></span> <code>&#x0226B;</code><!--`≫`--> <span data-ttu-id="d1b18-117">значок, чтобы получить его.</span><span class="sxs-lookup"><span data-stu-id="d1b18-117">icon to get there.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/javascript-overrides-overflow-menu.msft.png" alt-text="Инструмент «источники» с недостаточным объемом свободного места для отображения параметра «Overrides»" lightbox="../media/javascript-overrides-overflow-menu.msft.png":::
             <span data-ttu-id="d1b18-119">Инструмент « **источники** » с недостаточным объемом свободного места для отображения параметра «Overrides»</span><span class="sxs-lookup"><span data-stu-id="d1b18-119">**Sources** tool with not enough space to show the overrides option</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/javascript-overrides-menu.msft.png" alt-text="Выбор параметра "изменения"" lightbox="../media/javascript-overrides-menu.msft.png":::
             <span data-ttu-id="d1b18-121">Выбор параметра "изменения"</span><span class="sxs-lookup"><span data-stu-id="d1b18-121">Choose the overrides option</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  <span data-ttu-id="d1b18-122">После выбора параметра " **изменения** " необходимо выбрать папку на локальном компьютере, чтобы сохранить файлы ресурсов, которые вы хотите заменить.</span><span class="sxs-lookup"><span data-stu-id="d1b18-122">After you choose the **Overrides** option, you must choose a folder on your local computer to store the resource files that you want to replace.</span></span>  <span data-ttu-id="d1b18-123">Нажмите кнопку **+ выбрать для поиска переопределенных** папок.</span><span class="sxs-lookup"><span data-stu-id="d1b18-123">Choose the **+ Select folder for overrides** to search for a folder.</span></span>  
    
    :::image type="complex" source="../media/javascript-overrides-select-folder.msft.png" alt-text="Выбор папки для использования при переопределении" lightbox="../media/javascript-overrides-select-folder.msft.png":::
       <span data-ttu-id="d1b18-125">Выбор папки для использования при переопределении</span><span class="sxs-lookup"><span data-stu-id="d1b18-125">Choose a folder to use for overrides</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d1b18-126">DevTools предупреждает вас о том, что у вас должен быть полный доступ к папке, и не следует отображать конфиденциальную информацию.</span><span class="sxs-lookup"><span data-stu-id="d1b18-126">DevTools warns you that must have full access to the folder and that you should not reveal any sensitive information.</span></span>  <span data-ttu-id="d1b18-127">На панели с предупреждением выберите **разрешение** для предоставления доступа.</span><span class="sxs-lookup"><span data-stu-id="d1b18-127">On the warning bar, choose **Allow** to grant access.</span></span>  
    
    :::image type="complex" source="../media/javascript-overrides-give-access-to-folder.msft.png" alt-text="предоставление DevTools доступа к папке" lightbox="../media/javascript-overrides-give-access-to-folder.msft.png":::
       <span data-ttu-id="d1b18-129">Предоставление DevTools доступа к папке</span><span class="sxs-lookup"><span data-stu-id="d1b18-129">Grant DevTools access to folder</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d1b18-130">В области **Overrides** должен отображаться флажок рядом с `Enable Local Overrides` папкой Overrides.</span><span class="sxs-lookup"><span data-stu-id="d1b18-130">In the **Overrides** pane, a checkbox should be displayed next to `Enable Local Overrides` and your overrides folder.</span></span>  <span data-ttu-id="d1b18-131">Рядом с ним появится значок, с помощью которого вы можете удалить локальные параметры переопределения.</span><span class="sxs-lookup"><span data-stu-id="d1b18-131">An icon is displayed next to it that allows you to delete your local overrides settings.</span></span>  <span data-ttu-id="d1b18-132">Теперь вы закончите настройку папки и будете готовы заменить динамические ресурсы локальными.</span><span class="sxs-lookup"><span data-stu-id="d1b18-132">You are now done setting up your folder and ready to replace live resources with local ones.</span></span>
    
    :::image type="complex" source="../media/javascript-overrides-folder-setup-complete.msft.png" alt-text="Настройка папки "переопределения" успешно завершена" lightbox="../media/javascript-overrides-folder-setup-complete.msft.png":::
       <span data-ttu-id="d1b18-134">Настройка папки "переопределения" успешно завершена</span><span class="sxs-lookup"><span data-stu-id="d1b18-134">Successful set up of an overrides folder</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="d1b18-135">Добавление файлов в папку Overrides</span><span class="sxs-lookup"><span data-stu-id="d1b18-135">Adding files to your Overrides folder</span></span>  
  
<span data-ttu-id="d1b18-136">Чтобы добавить файлы в папку Overrides, откройте инструмент **элементы** и просмотрите веб-страницу.</span><span class="sxs-lookup"><span data-stu-id="d1b18-136">To add files to your overrides folder, open the **Elements** tool and inspect the webpage.</span></span>  <span data-ttu-id="d1b18-137">Чтобы изменить стиль CSS, выберите его имя в инспекторе **стилей** .</span><span class="sxs-lookup"><span data-stu-id="d1b18-137">To edit, choose the name of the CSS file in the **Styles** inspector.</span></span>  

:::image type="complex" source="../media/javascript-overrides-select-css-file.msft.png" alt-text="Выбор файла в инспекторе стилей" lightbox="../media/javascript-overrides-select-css-file.msft.png":::
   <span data-ttu-id="d1b18-139">Выбор файла в инспекторе **стилей**</span><span class="sxs-lookup"><span data-stu-id="d1b18-139">Choose a file in the **Styles** inspector</span></span>  
:::image-end:::  

<span data-ttu-id="d1b18-140">В редакторе **источников** наведите указатель мыши на имя файла выбранного файла, откройте контекстное меню (щелкните правой кнопкой мыши \) и выберите команду **сохранить для переопределений**.</span><span class="sxs-lookup"><span data-stu-id="d1b18-140">On the **Sources** editor, hover on the file name of your chosen file, open the contextual menu \(right-click\), and choose **Save for overrides**.</span></span>  

:::image type="complex" source="../media/javascript-overrides-file-name.msft.png" alt-text="В редакторе источников введите имя файла для переопределения." lightbox="../media/javascript-overrides-file-name.msft.png":::
   <span data-ttu-id="d1b18-142">В редакторе **источников** введите имя файла для переопределения.</span><span class="sxs-lookup"><span data-stu-id="d1b18-142">In the **Sources** editor, add the name of the file to overrides</span></span>  
:::image-end:::  

:::image type="complex" source="../media/javascript-overrides-save-for-overrides.msft.png" alt-text="В контекстном меню выберите команду Сохранить для переопределения." lightbox="../media/javascript-overrides-save-for-overrides.msft.png":::
   <span data-ttu-id="d1b18-144">В контекстном меню выберите команду **сохранить для переопределения** .</span><span class="sxs-lookup"><span data-stu-id="d1b18-144">On the context menu, choose **Save for overrides**</span></span>  
:::image-end:::  

<span data-ttu-id="d1b18-145">Файл сохраняется в папке Overrides.</span><span class="sxs-lookup"><span data-stu-id="d1b18-145">The file is stored in your overrides folder.</span></span>  <span data-ttu-id="d1b18-146">Убедитесь, что DevTools создает папку с именем, использующую URL-адрес файла с правильной структурой каталогов.</span><span class="sxs-lookup"><span data-stu-id="d1b18-146">Verify that DevTools create a folder that is named using the URL of the file with the correct directory structure.</span></span>  <span data-ttu-id="d1b18-147">Файл хранится внутри.</span><span class="sxs-lookup"><span data-stu-id="d1b18-147">The file is stored inside.</span></span>  <span data-ttu-id="d1b18-148">В редакторе теперь отображается фиолетовая точка, указывающая на то, что файл является локальным и не является динамическим.</span><span class="sxs-lookup"><span data-stu-id="d1b18-148">The file name in the editor now also shows a purple dot that indicates that the file is local and not a live one.</span></span>  

:::image type="complex" source="../media/javascript-overrides-file-stored.msft.png" alt-text="Файл успешно сохранен в папке Overrides" lightbox="../media/javascript-overrides-file-stored.msft.png":::
   <span data-ttu-id="d1b18-150">Файл успешно сохранен в папке Overrides</span><span class="sxs-lookup"><span data-stu-id="d1b18-150">Successfully stored the file in your overrides folder</span></span>  
:::image-end:::  

:::row:::
   :::column span="":::
      <span data-ttu-id="d1b18-151">В следующем примере теперь можно изменить стили веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="d1b18-151">In the following example, you may now change the styles of the webpage.</span></span>  <span data-ttu-id="d1b18-152">Чтобы добавить красную рамку вокруг файла, в редакторе **стилей** Скопируйте приведенный ниже стиль и добавьте его в элемент Body.</span><span class="sxs-lookup"><span data-stu-id="d1b18-152">To add a red border around the file, on the **Styles** editor, copy the following style, and add it to the body element.</span></span>  
      
      ```css
      border: 10px solid firebrick
      ```  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="d1b18-153">Файл будет автоматически сохранен на вашем компьютере.</span><span class="sxs-lookup"><span data-stu-id="d1b18-153">The file is automatically saved on your computer.</span></span>  <span data-ttu-id="d1b18-154">Если вы обновите файл, отобразится граница, и все ваши данные не будут потеряны.</span><span class="sxs-lookup"><span data-stu-id="d1b18-154">If you refresh the file, the border is displayed and none of your work is lost.</span></span>  
      
      :::image type="complex" source="../media/javascript-overrides-changing-styles.msft.png" alt-text="Изменение стилей веб-страниц с помощью редактирования файлов в папке Overrides" lightbox="../media/javascript-overrides-changing-styles.msft.png":::
         <span data-ttu-id="d1b18-156">Изменение стилей веб-страниц с помощью редактирования файлов в папке Overrides</span><span class="sxs-lookup"><span data-stu-id="d1b18-156">Change webpage styles persistently by editing a file in your overrides folder</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

:::row:::
   :::column span="":::
      <span data-ttu-id="d1b18-157">В инструменте **источники** в разделе **страница** наведите указатель мыши на любой файл, откройте контекстное меню (щелкните правой кнопкой мыши \) и добавьте его в переопределение.</span><span class="sxs-lookup"><span data-stu-id="d1b18-157">On the **Sources** tool, in the **Page** section, hover on any file, open the contextual menu \(right-click\), and add it to overrides.</span></span>  <span data-ttu-id="d1b18-158">Файлы, которые уже находятся в папке Overrides, имеют фиолетовые точки на значке.</span><span class="sxs-lookup"><span data-stu-id="d1b18-158">Again, files that are already in your overrides folder have a purple dot on the icon.</span></span>  
      
      :::image type="complex" source="../media/javascript-overrides-safe-from-sources.msft.png" alt-text="Выбор файла в инструменте «источники» для переопределений" lightbox="../media/javascript-overrides-safe-from-sources.msft.png":::
         <span data-ttu-id="d1b18-160">Выбор файла в инструменте « **источники** » для переопределений</span><span class="sxs-lookup"><span data-stu-id="d1b18-160">Choose a file from the **Sources** tool for overrides</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="d1b18-161">Кроме того, в инструменте **Network (сеть** ) наведите указатель мыши на любой файл, откройте контекстное меню (щелкните правой кнопкой мыши \) и добавьте его в переопределение.</span><span class="sxs-lookup"><span data-stu-id="d1b18-161">Alternatively, on the **Network** tool, hover on any file, open the contextual menu \(right-click\), and add it to overrides.</span></span>  <span data-ttu-id="d1b18-162">Переопределение в силе — файлы, которые находятся на компьютере, а не на веб-странице Live.</span><span class="sxs-lookup"><span data-stu-id="d1b18-162">When overrides are in effect, files that are located on your computer and not from the live webpage.</span></span>  <span data-ttu-id="d1b18-163">Когда действует переопределение, в инструменте **Network (сеть** ) найдите значок предупреждения рядом с именем файла.</span><span class="sxs-lookup"><span data-stu-id="d1b18-163">When overrides are in effect, on the **Network** tool, locate a warning icon next to the file name.</span></span>  
      
      :::image type="complex" source="../media/javascript-overrides-network.msft.png" alt-text="Выбор файла в средстве "сеть" для переопределения" lightbox="../media/javascript-overrides-network.msft.png":::
         <span data-ttu-id="d1b18-165">Выбор файла в средстве " **сеть** " для переопределения</span><span class="sxs-lookup"><span data-stu-id="d1b18-165">Choose a file from the **Network** tool for overrides</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="d1b18-166">Двухстороннее взаимодействие с переопределенными методами</span><span class="sxs-lookup"><span data-stu-id="d1b18-166">Two-way interaction of overrides</span></span>  

<span data-ttu-id="d1b18-167">Используйте редактор, предоставленный с помощью инструмента " **источники** " DevTools, или любой другой редактор, для которого вы хотите изменить файлы.</span><span class="sxs-lookup"><span data-stu-id="d1b18-167">Use the editor provided with the **Sources** tool of DevTools or any editor you want to change the files.</span></span>  <span data-ttu-id="d1b18-168">Изменения синхронизируются для всех продуктов, которые обращаются к файлам в папке Overrides.</span><span class="sxs-lookup"><span data-stu-id="d1b18-168">Changes are synced across all the products that access the files in the overrides folder.</span></span>  

## <span data-ttu-id="d1b18-169">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="d1b18-169">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsSourcesTool]: ../sources.md "Общие сведения о средстве «источники» | Документы Microsoft"  
