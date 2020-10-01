---
description: Просмотр и редактирование localStorage с помощью панели "Локальные хранилище" и консоли.
title: Просмотр и изменение локального хранилища с помощью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: aa5365d1764ea0db537ea24464f9c76441f05322
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993557"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  





# <span data-ttu-id="3b701-104">Просмотр и изменение локального хранилища с помощью Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="3b701-104">View and edit local storage with Microsoft Edge DevTools</span></span>   



<span data-ttu-id="3b701-105">В этом руководстве описано, как использовать [Microsoft Edge DevTools][MicrosoftEdgeDevTools] для просмотра, изменения и удаления пар ключ-значение [localStorage][MDNWindowsLocalStorage] .</span><span class="sxs-lookup"><span data-stu-id="3b701-105">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to view, edit, and delete [localStorage][MDNWindowsLocalStorage] key-value pairs.</span></span>  

## <span data-ttu-id="3b701-106">Просмотр ключей и значений localStorage</span><span class="sxs-lookup"><span data-stu-id="3b701-106">View localStorage keys and values</span></span>   

1.  <span data-ttu-id="3b701-107">Перейдите на вкладку **приложение** , чтобы открыть панель **приложения** .</span><span class="sxs-lookup"><span data-stu-id="3b701-107">Select the **Application** tab to open the **Application** panel.</span></span>  <span data-ttu-id="3b701-108">Область **манифеста** отображается по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3b701-108">The **Manifest** pane is shown by default.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-manifest.msft.png":::
       <span data-ttu-id="3b701-110">Область « **Манифест** »</span><span class="sxs-lookup"><span data-stu-id="3b701-110">The **Manifest** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="3b701-111">Разверните меню **Локальное хранилище** .</span><span class="sxs-lookup"><span data-stu-id="3b701-111">Expand the **Local Storage** menu.</span></span>  
    
    :::image type="complex" source="../media/storage-application-local-storage.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-local-storage.msft.png":::
       <span data-ttu-id="3b701-113">Меню « **Локальное хранилище** »</span><span class="sxs-lookup"><span data-stu-id="3b701-113">The **Local Storage** menu</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="3b701-114">Выберите домен, чтобы просмотреть пары "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="3b701-114">Select a domain to view the key-value pairs.</span></span>  
    
    :::image type="complex" source="../media/storage-application-local-storage-view-key-value.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-local-storage-view-key-value.msft.png":::
       <span data-ttu-id="3b701-116">`localStorage`Пары "ключ-значение" для `https://www.bing.com` домена</span><span class="sxs-lookup"><span data-stu-id="3b701-116">The `localStorage` key-value pairs for the `https://www.bing.com` domain</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="3b701-117">Выделите строку таблицы, чтобы просмотреть ее значение в представлении под таблицей.</span><span class="sxs-lookup"><span data-stu-id="3b701-117">Select a row of the table to view the value in the viewer below the table.</span></span>  
    
    :::image type="complex" source="../media/storage-application-local-storage-view-key-value-selected.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-local-storage-view-key-value-selected.msft.png":::
       <span data-ttu-id="3b701-119">Просмотр значения `eventLogQueue_Online` ключа</span><span class="sxs-lookup"><span data-stu-id="3b701-119">View the value of the `eventLogQueue_Online` key</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="3b701-120">Создание новой пары "ключ-значение" для localStorage</span><span class="sxs-lookup"><span data-stu-id="3b701-120">Create a new localStorage key-value pair</span></span>   

1.  <span data-ttu-id="3b701-121">[Просмотр `localStorage` пар "ключ-значение" домена](#view-localstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="3b701-121">[View the `localStorage` key-value pairs of a domain](#view-localstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="3b701-122">Дважды щелкните пустую часть таблицы.</span><span class="sxs-lookup"><span data-stu-id="3b701-122">Double-click the empty part of the table.</span></span>  <span data-ttu-id="3b701-123">DevTools создает новую строку и нафокусирует указатель мыши на **ключевом** столбце.</span><span class="sxs-lookup"><span data-stu-id="3b701-123">DevTools creates a new row and focuses your cursor in the **Key** column.</span></span>  
    
    :::image type="complex" source="../media/storage-application-local-storage-new-key-value.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-local-storage-new-key-value.msft.png":::
       <span data-ttu-id="3b701-125">Пустая часть таблицы для двойного щелчка, чтобы создать новую пару ключ-значение.</span><span class="sxs-lookup"><span data-stu-id="3b701-125">The empty part of the table to double-click in order to create a new key-value pair</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="3b701-126">Изменение ключей и значений localStorage</span><span class="sxs-lookup"><span data-stu-id="3b701-126">Edit localStorage keys or values</span></span>   

1.  <span data-ttu-id="3b701-127">[Просмотр `localStorage` пар "ключ-значение" домена](#view-localstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="3b701-127">[View the `localStorage` key-value pairs of a domain](#view-localstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="3b701-128">Дважды щелкните ячейку в столбце " **раздел** " или " **значение** ", чтобы изменить этот раздел или значение.</span><span class="sxs-lookup"><span data-stu-id="3b701-128">Double-click a cell in the **Key** or **Value** column to edit that key or value.</span></span>  
    
    :::image type="complex" source="../media/storage-application-local-storage-edit-key-value.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-local-storage-edit-key-value.msft.png":::
       <span data-ttu-id="3b701-130">Изменение `localStorage` ключа</span><span class="sxs-lookup"><span data-stu-id="3b701-130">Edit a `localStorage` key</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="3b701-131">Удаление пар ключ-значение localStorage</span><span class="sxs-lookup"><span data-stu-id="3b701-131">Delete localStorage key-value pairs</span></span>   

1.  <span data-ttu-id="3b701-132">[Просмотр `localStorage` пар "ключ-значение" домена](#view-localstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="3b701-132">[View the `localStorage` key-value pairs of a domain](#view-localstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="3b701-133">Выберите пару "ключ-значение", которую вы хотите удалить.</span><span class="sxs-lookup"><span data-stu-id="3b701-133">Select the key-value pair that you want to delete.</span></span>  <span data-ttu-id="3b701-134">DevTools выделит ее синей, чтобы показать, что она выбрана.</span><span class="sxs-lookup"><span data-stu-id="3b701-134">DevTools highlights it blue to indicate that it is selected.</span></span>  
1.  <span data-ttu-id="3b701-135">Нажмите клавишу `Delete` или нажмите кнопку **Удалить выделенные** \ ( ![ Удалить выбранные \ ][ImageDeleteIcon] ).</span><span class="sxs-lookup"><span data-stu-id="3b701-135">Press the `Delete` key or click **Delete Selected** \(![Delete Selected][ImageDeleteIcon]\).</span></span>  
    
## <span data-ttu-id="3b701-136">Удаление всех `localStorage` пар "ключ-значение" для домена</span><span class="sxs-lookup"><span data-stu-id="3b701-136">Delete all `localStorage` key-value pairs for a domain</span></span>   

1.  <span data-ttu-id="3b701-137">[Просмотр `localStorage` пар "ключ-значение" домена](#view-localstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="3b701-137">[View the `localStorage` key-value pairs of a domain](#view-localstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="3b701-138">Нажмите **Очистить все** \ ( ![ Очистить все ][ImageClearIcon] \).</span><span class="sxs-lookup"><span data-stu-id="3b701-138">Select **Clear All** \(![Clear All][ImageClearIcon]\).</span></span>  
    
## <span data-ttu-id="3b701-139">Взаимодействие с localStorage с помощью консоли</span><span class="sxs-lookup"><span data-stu-id="3b701-139">Interact with localStorage from the Console</span></span>   

<span data-ttu-id="3b701-140">Так как вы можете запускать JavaScript на **консоли**, а так как у **консоли** есть доступ к контекстам JavaScript страницы, взаимодействие с `localStorage` **консолью**возможно.</span><span class="sxs-lookup"><span data-stu-id="3b701-140">Since you are able to run JavaScript in the **Console**, and since the **Console** has access to the JavaScript contexts of the page, it is possible to interact with `localStorage` from the **Console**.</span></span>  

1.  <span data-ttu-id="3b701-141">Используйте меню "контексты **JavaScript** " для изменения контекста JavaScript на **консоли** , если требуется получить доступ к `localStorage` парам "ключ-значение" домена, отличного от отображаемой страницы.</span><span class="sxs-lookup"><span data-stu-id="3b701-141">Use the **JavaScript contexts** menu to change the JavaScript context of the **Console** if you want to access the `localStorage` key-value pairs of a domain other than the page that is displayed.</span></span>  
    
    :::image type="complex" source="../media/storage-console-local-storage.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-console-local-storage.msft.png":::
       <span data-ttu-id="3b701-143">Изменение контекста JavaScript консоли</span><span class="sxs-lookup"><span data-stu-id="3b701-143">Change the JavaScript context of the Console</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="3b701-144">Выполняйте `localStorage` выражения на консоли так же, как и в JavaScript.</span><span class="sxs-lookup"><span data-stu-id="3b701-144">Run your `localStorage` expressions in the Console, the same as you do in your JavaScript.</span></span>  
    
    :::image type="complex" source="../media/storage-console-local-storage-interaction.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-console-local-storage-interaction.msft.png":::
       <span data-ttu-id="3b701-146">Взаимодействие с `localStorage` **консолью**</span><span class="sxs-lookup"><span data-stu-id="3b701-146">Interact with `localStorage` from the **Console**</span></span>  
    :::image-end:::  
    
<!--  
 


-->  

<!-- image links -->  

[ImageClearIcon]: ../media/clear-icon.msft.png  
[ImageDeleteIcon]: ../media/delete-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Инструменты разработчика Microsoft EDGE (Chromium) | Документы Microsoft"  

[MDNWindowsLocalStorage]: https://developer.mozilla.org/docs/Web/API/Window/localStorage "Window. localStorage | MDN"  

> [!NOTE]
> <span data-ttu-id="3b701-149">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="3b701-149">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="3b701-150">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/storage/localstorage) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="3b701-150">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/localstorage) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="3b701-152">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="3b701-152">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
