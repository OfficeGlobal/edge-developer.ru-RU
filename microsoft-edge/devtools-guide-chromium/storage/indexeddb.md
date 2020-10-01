---
description: Просмотр и изменение данных IndexedDB с помощью панели приложения и фрагментов.
title: Просмотр и изменение IndexedDBных данных с помощью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 6b1209ddcbfac305535d9d61e001441dbf61b6ec
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993564"
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





# <span data-ttu-id="43fdf-104">Просмотр и изменение IndexedDBных данных с помощью Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="43fdf-104">View and change IndexedDB data with Microsoft Edge DevTools</span></span>   

  

<span data-ttu-id="43fdf-105">В этом руководстве описано, как использовать [Microsoft Edge DevTools][MicrosoftEdgeDevTools] для просмотра и изменения [IndexedDB][MDNIndexedDBAPI] данных.</span><span class="sxs-lookup"><span data-stu-id="43fdf-105">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to view and change [IndexedDB][MDNIndexedDBAPI] data.</span></span>  <span data-ttu-id="43fdf-106">Предполагается, что вы знакомы с DevTools.</span><span class="sxs-lookup"><span data-stu-id="43fdf-106">It assumes you are familiar with DevTools.</span></span>  <span data-ttu-id="43fdf-107">Кроме того, предполагается, что вы знакомы с IndexedDB.</span><span class="sxs-lookup"><span data-stu-id="43fdf-107">It also assumes you are familiar with IndexedDB.</span></span>  <span data-ttu-id="43fdf-108">В противном случае ознакомьтесь [с разIndexedDB][MDNUsingIndexedDB].</span><span class="sxs-lookup"><span data-stu-id="43fdf-108">If not, see [Using IndexedDB][MDNUsingIndexedDB].</span></span>  

## <span data-ttu-id="43fdf-109">Просмотр данных IndexedDB</span><span class="sxs-lookup"><span data-stu-id="43fdf-109">View IndexedDB data</span></span>   

1.  <span data-ttu-id="43fdf-110">Перейдите на вкладку **приложение** , чтобы открыть панель **приложения** .</span><span class="sxs-lookup"><span data-stu-id="43fdf-110">Select the **Application** tab to open the **Application** panel.</span></span>  <span data-ttu-id="43fdf-111">Обычно область **манифеста** открывается по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="43fdf-111">The **Manifest** pane usually opens by default.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest-empty.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-manifest-empty.msft.png":::
       <span data-ttu-id="43fdf-113">Область « **Манифест** »</span><span class="sxs-lookup"><span data-stu-id="43fdf-113">The **Manifest** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="43fdf-114">Разверните меню **IndexedDB** , чтобы узнать, какие базы данных доступны.</span><span class="sxs-lookup"><span data-stu-id="43fdf-114">Expand the **IndexedDB** menu to see which databases are available.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-storage-indexeddb.msft.png":::
       <span data-ttu-id="43fdf-116">Меню **IndexedDB**</span><span class="sxs-lookup"><span data-stu-id="43fdf-116">The **IndexedDB** menu</span></span>  
    :::image-end:::  
    
    *   <span data-ttu-id="43fdf-117">\ ( ![ Значок базы данных ][ImageDatabaseIcon] \) `notes - https://mdn.github.io` представляет базу данных, где `notes` — это имя базы данных, а `https://mdn.github.io` также источник, который получает доступ к базе данных.</span><span class="sxs-lookup"><span data-stu-id="43fdf-117">\(![Database icon][ImageDatabaseIcon]\) `notes - https://mdn.github.io` represents a database, where `notes` is the name of the database and `https://mdn.github.io` is the origin that accesses the database.</span></span>  
    *   <span data-ttu-id="43fdf-118">\ ( ![ Значок хранилища объектов ][ImageObjectStoreIcon] \) `notes` — это хранилище объектов.</span><span class="sxs-lookup"><span data-stu-id="43fdf-118">\(![Object Store icon][ImageObjectStoreIcon]\) `notes` is an object store.</span></span>  
    *   <span data-ttu-id="43fdf-119">**заголовок** и **текст** — это [индексы][MDNUsingIndexedDBUsingIndex].</span><span class="sxs-lookup"><span data-stu-id="43fdf-119">**title** and **body** are [indexes][MDNUsingIndexedDBUsingIndex].</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="43fdf-120">**Известное ограничение**  Сторонние базы данных не видны.</span><span class="sxs-lookup"><span data-stu-id="43fdf-120">**Known Limitation**  Third-party databases are not visible.</span></span>  <span data-ttu-id="43fdf-121">Например, если вы используете `<iframe>` для внедрения баннера на странице, а в вашей рекламной сети используется IndexedDB, данные IndexedDB для вашей рекламной сети не будут видны.</span><span class="sxs-lookup"><span data-stu-id="43fdf-121">For example, if you use an `<iframe>` to embed an ad on your page, and your ad network uses IndexedDB, the IndexedDB data for your ad network is not be visible.</span></span>  <span data-ttu-id="43fdf-122">Просмотреть [#943770 вопросов][ChromiumIssue943770].</span><span class="sxs-lookup"><span data-stu-id="43fdf-122">See [issue #943770][ChromiumIssue943770].</span></span>  
    
1.  <span data-ttu-id="43fdf-123">Выберите базу данных, чтобы увидеть источник и номер версии.</span><span class="sxs-lookup"><span data-stu-id="43fdf-123">Select a database to see the origin and version number.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-storage-indexeddb-notes_db.msft.png":::
       <span data-ttu-id="43fdf-125">База данных **Notes**</span><span class="sxs-lookup"><span data-stu-id="43fdf-125">The **notes** database</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="43fdf-126">Выберите хранилище объектов для просмотра пар "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="43fdf-126">Select an object store to see the key-value pairs.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="43fdf-127">Данные IndexedDB не обновляются в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="43fdf-127">IndexedDB data does not update in real-time.</span></span>  <span data-ttu-id="43fdf-128">Смотрите раздел [Обновление данных IndexedDB](#refresh-indexeddb-data).</span><span class="sxs-lookup"><span data-stu-id="43fdf-128">See [Refresh IndexedDB data](#refresh-indexeddb-data).</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os.msft.png":::
       <span data-ttu-id="43fdf-130">Хранилище объектов " **заметки** "</span><span class="sxs-lookup"><span data-stu-id="43fdf-130">The **notes** object store</span></span>  
    :::image-end:::  
    
    *   <span data-ttu-id="43fdf-131">**Всего элементов** — общее количество пар "ключ-значение" в хранилище объектов.</span><span class="sxs-lookup"><span data-stu-id="43fdf-131">**Total entries** is the total number of key-value pairs in the object store.</span></span>  
    *   <span data-ttu-id="43fdf-132">**Значение ключевого генератора** — это следующий доступный ключ.</span><span class="sxs-lookup"><span data-stu-id="43fdf-132">**Key generator value** is the next available key.</span></span>  <span data-ttu-id="43fdf-133">Это поле отображается только при использовании [генераторов ключей][MDNBasicConceptsKeyGenerator].</span><span class="sxs-lookup"><span data-stu-id="43fdf-133">This field is only shown when using [key generators][MDNBasicConceptsKeyGenerator].</span></span>  
    
1.  <span data-ttu-id="43fdf-134">Выберите ячейку в столбце **значение** , чтобы развернуть это значение.</span><span class="sxs-lookup"><span data-stu-id="43fdf-134">Select a cell in the **Value** column to expand that value.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-edge-chromium.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-edge-chromium.msft.png":::
       <span data-ttu-id="43fdf-136">Просмотр значения **IndexedDB**</span><span class="sxs-lookup"><span data-stu-id="43fdf-136">View an **IndexedDB** value</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="43fdf-137">Выберите индекс (например, **заголовок** или **текст** ) на приведенном ниже рисунке, чтобы отсортировать хранилище объектов согласно значениям этого индекса.</span><span class="sxs-lookup"><span data-stu-id="43fdf-137">Select an index, such as **title** or **body** in the following figure, to sort the object store according to the values of that index.</span></span>  
   
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-title.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-title.msft.png":::
       <span data-ttu-id="43fdf-139">Сортировка хранилища объектов по индексу</span><span class="sxs-lookup"><span data-stu-id="43fdf-139">Sort an object store by an index</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="43fdf-140">Обновление данных IndexedDB</span><span class="sxs-lookup"><span data-stu-id="43fdf-140">Refresh IndexedDB data</span></span>   

<span data-ttu-id="43fdf-141">Значения IndexedDB на панели **приложения** не обновляются в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="43fdf-141">IndexedDB values in the **Application** panel do not update in real-time.</span></span>  <span data-ttu-id="43fdf-142">Выберите команду **Обновить** \ ( ![ обновить ][ImageReloadIcon] \) при просмотре хранилища объектов, чтобы обновить данные, или просмотрите базу данных и нажмите **обновить базу данных** , чтобы обновить все данные.</span><span class="sxs-lookup"><span data-stu-id="43fdf-142">Select **Refresh** \(![Refresh][ImageReloadIcon]\) when viewing an object store to refresh the data, or view a database and click **Refresh database** to refresh all data.</span></span>  

:::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-refresh-database.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-refresh-database.msft.png":::
   <span data-ttu-id="43fdf-144">Просмотр базы данных</span><span class="sxs-lookup"><span data-stu-id="43fdf-144">View a database</span></span>  
:::image-end:::  

## <span data-ttu-id="43fdf-145">Изменить данные IndexedDB</span><span class="sxs-lookup"><span data-stu-id="43fdf-145">Edit IndexedDB data</span></span>   

<span data-ttu-id="43fdf-146">IndexedDB ключи и значения не подлежат редактированию на панели **приложения** .</span><span class="sxs-lookup"><span data-stu-id="43fdf-146">IndexedDB keys and values are not editable from the **Application** panel.</span></span>  <span data-ttu-id="43fdf-147">Так как DevTools имеет доступ к контексту страницы, вы можете выполнить код JavaScript в DevTools для редактирования IndexedDB данных.</span><span class="sxs-lookup"><span data-stu-id="43fdf-147">Since DevTools has access to page context, however, you may run JavaScript code within DevTools to edit IndexedDB data.</span></span>  

### <span data-ttu-id="43fdf-148">Редактирование данных IndexedDB с помощью фрагментов</span><span class="sxs-lookup"><span data-stu-id="43fdf-148">Edit IndexedDB data with Snippets</span></span>   

<span data-ttu-id="43fdf-149">[Фрагменты][DevtoolsJavascriptSnippets] — это способ хранения и выполнения блоков кода JavaScript в DevTools.</span><span class="sxs-lookup"><span data-stu-id="43fdf-149">[Snippets][DevtoolsJavascriptSnippets] are a way to store and run blocks of JavaScript code within DevTools.</span></span>  <span data-ttu-id="43fdf-150">При выполнении фрагмента на **консоль**выписывается результат.</span><span class="sxs-lookup"><span data-stu-id="43fdf-150">When you run a Snippet, the result is logged to the **Console**.</span></span>  <span data-ttu-id="43fdf-151">Вы можете использовать сниппет для выполнения кода JavaScript, чтобы изменить базу данных IndexedDB.</span><span class="sxs-lookup"><span data-stu-id="43fdf-151">You may use a Snippet to run JavaScript code to edit an IndexedDB database.</span></span>  

:::image type="complex" source="../media/storage-sources-snippets-indexeddb-output.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-sources-snippets-indexeddb-output.msft.png":::
   <span data-ttu-id="43fdf-153">Использование фрагмента для взаимодействия с IndexedDB</span><span class="sxs-lookup"><span data-stu-id="43fdf-153">Use a Snippet to interact with IndexedDB</span></span>  
:::image-end:::  

## <span data-ttu-id="43fdf-154">Удаление данных IndexedDB</span><span class="sxs-lookup"><span data-stu-id="43fdf-154">Delete IndexedDB data</span></span>   

### <span data-ttu-id="43fdf-155">Удаление пары ключ-значение IndexedDB</span><span class="sxs-lookup"><span data-stu-id="43fdf-155">Delete an IndexedDB key-value pair</span></span>   

1.  <span data-ttu-id="43fdf-156">[Просмотр хранилища объектов IndexedDB](#view-indexeddb-data).</span><span class="sxs-lookup"><span data-stu-id="43fdf-156">[View an IndexedDB object store](#view-indexeddb-data).</span></span>  
1.  <span data-ttu-id="43fdf-157">Выберите пару "ключ-значение", которую вы хотите удалить.</span><span class="sxs-lookup"><span data-stu-id="43fdf-157">Select the key-value pair that you want to delete.</span></span>  <span data-ttu-id="43fdf-158">DevTools выделит ее, чтобы показать, что она выбрана.</span><span class="sxs-lookup"><span data-stu-id="43fdf-158">DevTools highlights it to indicate that it is selected.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os2.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os2.msft.png":::
       <span data-ttu-id="43fdf-160">Выберите пару "ключ-значение", чтобы удалить ее</span><span class="sxs-lookup"><span data-stu-id="43fdf-160">Select a key-value pair in order to delete it</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="43fdf-161">Нажмите клавишу `Delete` или нажмите кнопку **Удалить выделенные** \ ( ![ Удалить выбранные \ ][ImageDeleteIcon] ).</span><span class="sxs-lookup"><span data-stu-id="43fdf-161">Press the `Delete` key or click **Delete Selected** \(![Delete Selected][ImageDeleteIcon]\).</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-delete-selected.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-delete-selected.msft.png":::
       <span data-ttu-id="43fdf-163">Как выглядит хранилище объектов после удаления пары "ключ-значение"</span><span class="sxs-lookup"><span data-stu-id="43fdf-163">How the object store looks after the key-value pair has been deleted</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="43fdf-164">Удаление всех пар "ключ-значение" в хранилище объектов</span><span class="sxs-lookup"><span data-stu-id="43fdf-164">Delete all key-value pairs in an object store</span></span>   

1.  <span data-ttu-id="43fdf-165">[Просмотр хранилища объектов IndexedDB](#view-indexeddb-data).</span><span class="sxs-lookup"><span data-stu-id="43fdf-165">[View an IndexedDB object store](#view-indexeddb-data).</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-clear-object-store.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-clear-object-store.msft.png":::
       <span data-ttu-id="43fdf-167">Просмотр хранилища объектов</span><span class="sxs-lookup"><span data-stu-id="43fdf-167">View an object store</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="43fdf-168">Выберите **Очистить хранилище объектов** \ ( ![ Очистить хранилище объектов ][ImageClearIcon] ).</span><span class="sxs-lookup"><span data-stu-id="43fdf-168">Select **Clear object store** \(![Clear object store][ImageClearIcon]\).</span></span>  
    
### <span data-ttu-id="43fdf-169">Удаление базы данных IndexedDB</span><span class="sxs-lookup"><span data-stu-id="43fdf-169">Delete an IndexedDB database</span></span>   

1.  <span data-ttu-id="43fdf-170">[Просмотрите базу данных IndexedDB](#view-indexeddb-data) , которую вы хотите удалить.</span><span class="sxs-lookup"><span data-stu-id="43fdf-170">[View the IndexedDB database](#view-indexeddb-data) that you want to delete.</span></span>  
1.  <span data-ttu-id="43fdf-171">Выберите команду **Удалить базу данных**.</span><span class="sxs-lookup"><span data-stu-id="43fdf-171">Select **Delete database**.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-delete-database.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-storage-indexeddb-notes_db-delete-database.msft.png":::
       <span data-ttu-id="43fdf-173">Кнопка " **Удалить базу данных** "</span><span class="sxs-lookup"><span data-stu-id="43fdf-173">The **Delete database** button</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="43fdf-174">Удаление всех IndexedDB хранилища</span><span class="sxs-lookup"><span data-stu-id="43fdf-174">Delete all IndexedDB storage</span></span>   

1.  <span data-ttu-id="43fdf-175">Открытие области **очистки хранилища** .</span><span class="sxs-lookup"><span data-stu-id="43fdf-175">Open the **Clear storage** pane.</span></span>  
1.  <span data-ttu-id="43fdf-176">Убедитесь, что флажок **IndexedDB** установлен.</span><span class="sxs-lookup"><span data-stu-id="43fdf-176">Make sure that the **IndexedDB** checkbox is enabled.</span></span>  
1.  <span data-ttu-id="43fdf-177">Нажмите кнопку **Очистить данные сайта**.</span><span class="sxs-lookup"><span data-stu-id="43fdf-177">Select **Clear site data**.</span></span>  
    
    :::image type="complex" source="../media/storage-application-clear-storage-indexeddb-clear-site-data.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-clear-storage-indexeddb-clear-site-data.msft.png":::
       <span data-ttu-id="43fdf-179">Область " **Очистка хранилища** "</span><span class="sxs-lookup"><span data-stu-id="43fdf-179">The **Clear storage** pane</span></span>  
    :::image-end:::  
    
<!--  
 


-->  

<!-- image links -->  

[ImageClearIcon]: ../media/clear-icon.msft.png  
[ImageDatabaseIcon]: ../media/database-icon.msft.png  
[ImageDeleteIcon]: ../media/delete-icon.msft.png  
[ImageObjectStoreIcon]: ../media/object-store-icon.msft.png  
[ImageReloadIcon]: ../media/reload-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Инструменты разработчика Microsoft EDGE (Chromium) | Документы Microsoft"  
[DevtoolsJavascriptSnippets]: ../javascript/snippets.md "Выполнение фрагментов кода JavaScript на любой странице с Microsoft Edge DevTools | Документы Microsoft"  

[ChromiumIssue943770]: https://crbug.com/943770 "943770-DevTools: Show IFRAME IndexedDB databases-Chromium-Monorail"  

[MDNBasicConceptsKeyGenerator]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Basic_Concepts_Behind_IndexedDB#gloss_keygenerator "Ключевой генератор — основные принципы | MDN"  
[MDNIndexedDBAPI]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API "API IndexedDB | MDN"  
[MDNUsingIndexedDB]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB "Использование IndexedDB | MDN"  
[MDNUsingIndexedDBUsingIndex]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB#Using_an_index "Использование индекса с помощью IndexedDB | MDN"  

> [!NOTE]
> <span data-ttu-id="43fdf-187">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="43fdf-187">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="43fdf-188">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/storage/indexeddb) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="43fdf-188">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/indexeddb) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="43fdf-190">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="43fdf-190">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
