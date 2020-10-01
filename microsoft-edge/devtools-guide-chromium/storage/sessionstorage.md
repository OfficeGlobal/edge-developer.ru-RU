---
description: Просмотр и редактирование sessionStorage с помощью панели хранилища сеанса и консоли.
title: Просмотр и изменение хранилища сеанса с помощью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 24fca3fd3a068f3b2ffbe4ec1c23e6b80b968953
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993550"
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





# <span data-ttu-id="a935a-104">Просмотр и изменение хранилища сеанса с помощью Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="a935a-104">View and edit Session Storage with Microsoft Edge DevTools</span></span>   

  

<span data-ttu-id="a935a-105">В этом руководстве описано, как использовать [Microsoft Edge DevTools][MicrosoftEdgeDevTools] для просмотра, изменения и удаления [`sessionStorage`][MDNSessionStorage] пар "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="a935a-105">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to view, edit, and delete [`sessionStorage`][MDNSessionStorage] key-value pairs.</span></span>  

## <span data-ttu-id="a935a-106">Просмотр ключей и значений sessionStorage</span><span class="sxs-lookup"><span data-stu-id="a935a-106">View sessionStorage keys and values</span></span>   

1.  <span data-ttu-id="a935a-107">Перейдите на вкладку **приложение** , чтобы открыть панель **приложения** .</span><span class="sxs-lookup"><span data-stu-id="a935a-107">Select the **Application** tab to open the **Application** panel.</span></span>  <span data-ttu-id="a935a-108">Область **манифеста** отображается по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a935a-108">The **Manifest** pane is shown by default.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-manifest.msft.png":::
       <span data-ttu-id="a935a-110">Область « **Манифест** »</span><span class="sxs-lookup"><span data-stu-id="a935a-110">The **Manifest** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="a935a-111">Разверните меню **хранилище сеанса** .</span><span class="sxs-lookup"><span data-stu-id="a935a-111">Expand the **Session Storage** menu.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-storage-session-storage.msft.png":::
       <span data-ttu-id="a935a-113">Меню « **хранилище сеанса** »</span><span class="sxs-lookup"><span data-stu-id="a935a-113">The **Session Storage** Menu</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="a935a-114">Выберите домен, чтобы просмотреть пары "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="a935a-114">Select a domain to view the key-value pairs.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-storage-session-storage-domain.msft.png":::
       <span data-ttu-id="a935a-116">`sessionStorage`Пары "ключ-значение"</span><span class="sxs-lookup"><span data-stu-id="a935a-116">The `sessionStorage` key-value pairs</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="a935a-117">Выделите строку таблицы, чтобы просмотреть ее значение в представлении под таблицей.</span><span class="sxs-lookup"><span data-stu-id="a935a-117">Select a row of the table to view the value in the viewer below the table.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain-key-value-selected.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-storage-session-storage-domain-key-value-selected.msft.png":::
       <span data-ttu-id="a935a-119">Просмотр значения `x-sid` ключа</span><span class="sxs-lookup"><span data-stu-id="a935a-119">View the value of the `x-sid` key</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="a935a-120">Создание новой пары "ключ-значение" для sessionStorage</span><span class="sxs-lookup"><span data-stu-id="a935a-120">Create a new sessionStorage key-value pair</span></span>   

1.  <span data-ttu-id="a935a-121">[Просмотр `sessionStorage` пар "ключ-значение" домена](#view-sessionstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="a935a-121">[View the `sessionStorage` key-value pairs of a domain](#view-sessionstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="a935a-122">Дважды щелкните пустую часть таблицы.</span><span class="sxs-lookup"><span data-stu-id="a935a-122">Double-click the empty part of the table.</span></span>  <span data-ttu-id="a935a-123">DevTools создает новую строку и нафокусирует указатель мыши на **ключевом** столбце.</span><span class="sxs-lookup"><span data-stu-id="a935a-123">DevTools creates a new row and focuses your cursor in the **Key** column.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain-key-value-new.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-storage-session-storage-domain-key-value-new.msft.png":::
       <span data-ttu-id="a935a-125">Пустая часть таблицы для двойного щелчка, чтобы создать новую пару ключ-значение.</span><span class="sxs-lookup"><span data-stu-id="a935a-125">The empty part of the table to double-click in order to create a new key-value pair</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="a935a-126">Изменение ключей и значений sessionStorage</span><span class="sxs-lookup"><span data-stu-id="a935a-126">Edit sessionStorage keys or values</span></span>   

1.  <span data-ttu-id="a935a-127">[Просмотр `sessionStorage` пар "ключ-значение" домена](#view-sessionstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="a935a-127">[View the `sessionStorage` key-value pairs of a domain](#view-sessionstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="a935a-128">Дважды щелкните ячейку в столбце " **раздел** " или " **значение** ", чтобы изменить этот раздел или значение.</span><span class="sxs-lookup"><span data-stu-id="a935a-128">Double-click a cell in the **Key** or **Value** column to edit that key or value.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain-key-value-edit.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-storage-session-storage-domain-key-value-edit.msft.png":::
       <span data-ttu-id="a935a-130">Изменение `sessionStorage` ключа</span><span class="sxs-lookup"><span data-stu-id="a935a-130">Edit a `sessionStorage` key</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="a935a-131">Удаление пар ключ-значение sessionStorage</span><span class="sxs-lookup"><span data-stu-id="a935a-131">Delete sessionStorage key-value pairs</span></span>   

1.  <span data-ttu-id="a935a-132">[Просмотр `sessionStorage` пар "ключ-значение" домена](#view-sessionstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="a935a-132">[View the `sessionStorage` key-value pairs of a domain](#view-sessionstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="a935a-133">Выберите пару "ключ-значение", которую вы хотите удалить.</span><span class="sxs-lookup"><span data-stu-id="a935a-133">Select the key-value pair that you want to delete.</span></span>  <span data-ttu-id="a935a-134">DevTools выделит ее синей, чтобы показать, что она выбрана.</span><span class="sxs-lookup"><span data-stu-id="a935a-134">DevTools highlights it blue to indicate that it is selected.</span></span>  
1.  <span data-ttu-id="a935a-135">Нажмите клавишу `Delete` или нажмите кнопку **Удалить выделенные** \ ( ![ Удалить выбранные \ ][ImageDeleteIcon] ).</span><span class="sxs-lookup"><span data-stu-id="a935a-135">Press the `Delete` key or click **Delete Selected** \(![Delete Selected][ImageDeleteIcon]\).</span></span>  
    
## <span data-ttu-id="a935a-136">Удаление всех пар ключ-значение sessionStorage для домена</span><span class="sxs-lookup"><span data-stu-id="a935a-136">Delete all sessionStorage key-value pairs for a domain</span></span>   

1.  <span data-ttu-id="a935a-137">[Просмотр `sessionStorage` пар "ключ-значение" домена](#view-sessionstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="a935a-137">[View the `sessionStorage` key-value pairs of a domain](#view-sessionstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="a935a-138">Нажмите **Очистить все** \ ( ![ Очистить все ][ImageClearIcon] \).</span><span class="sxs-lookup"><span data-stu-id="a935a-138">Select **Clear All** \(![Clear All][ImageClearIcon]\).</span></span>  
    
## <span data-ttu-id="a935a-139">Взаимодействие с sessionStorage с помощью консоли</span><span class="sxs-lookup"><span data-stu-id="a935a-139">Interact with sessionStorage from the Console</span></span>   

<span data-ttu-id="a935a-140">Так как вы можете запустить JavaScript на **консоли**, и так как **консоль** имеет доступ к контекстам JavaScript на странице, можно взаимодействовать с `sessionStorage` ней из **консоли**.</span><span class="sxs-lookup"><span data-stu-id="a935a-140">Since you can run JavaScript in the **Console**, and since the **Console** has access to the JavaScript contexts of the page, it is possible to interact with `sessionStorage` from the **Console**.</span></span>  

1.  <span data-ttu-id="a935a-141">Используйте меню "контексты **JavaScript** " для изменения контекста JavaScript на **консоли** , если вы хотите получить доступ к `sessionStorage` парам "ключ-значение" домена, отличного от страницы, на которой вы являетесь.</span><span class="sxs-lookup"><span data-stu-id="a935a-141">Use the **JavaScript contexts** menu to change the JavaScript context of the **Console** if you want to access the `sessionStorage` key-value pairs of a domain other than the page you are on.</span></span>  
    
    :::image type="complex" source="../media/storage-console-domain-selection.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-console-domain-selection.msft.png":::
       <span data-ttu-id="a935a-143">Изменение контекста JavaScript консоли</span><span class="sxs-lookup"><span data-stu-id="a935a-143">Change the JavaScript context of the Console</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="a935a-144">Выполняйте `sessionStorage` выражения на консоли так же, как и в JavaScript.</span><span class="sxs-lookup"><span data-stu-id="a935a-144">Run your `sessionStorage` expressions in the Console, the same as you would in your JavaScript.</span></span>  
    
    :::image type="complex" source="../media/storage-console-session-storage-keys.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-console-session-storage-keys.msft.png":::
       <span data-ttu-id="a935a-146">Взаимодействие с `sessionStorage` **консолью**</span><span class="sxs-lookup"><span data-stu-id="a935a-146">Interact with `sessionStorage` from the **Console**</span></span>  
    :::image-end:::  
    
<!--  
   

  
-->  

<!-- image links -->  

[ImageClearIcon]: ../media/clear-icon.msft.png  
[ImageDeleteIcon]: ../media/delete-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Инструменты разработчика Microsoft EDGE (Chromium) | Документы Microsoft"  

[MDNSessionStorage]: https://developer.mozilla.org/docs/Web/API/Window/sessionStorage "Window. sessionStorage | MDN"  

> [!NOTE]
> <span data-ttu-id="a935a-149">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="a935a-149">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="a935a-150">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/storage/sessionstorage) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="a935a-150">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/sessionstorage) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="a935a-152">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="a935a-152">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
