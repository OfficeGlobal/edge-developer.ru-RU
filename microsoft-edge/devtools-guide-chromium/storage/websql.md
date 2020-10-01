---
description: Инструкции по просмотру данных из веб-SQL на панели приложения Microsoft Edge DevTools.
title: Просмотр данных из веб-SQL с помощью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: cc2f726c80fbf0c943b43ff6c131e9479db75b78
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993536"
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





# <span data-ttu-id="ccd0c-104">Просмотр данных из веб-SQL с помощью Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="ccd0c-104">View Web SQL data with Microsoft Edge DevTools</span></span>   



> [!WARNING]
> <span data-ttu-id="ccd0c-105">Спецификация веб-SQL [не поддерживается][W3CWebSQLStatus].</span><span class="sxs-lookup"><span data-stu-id="ccd0c-105">The Web SQL specification is [not being maintained][W3CWebSQLStatus].</span></span>  

<span data-ttu-id="ccd0c-106">В этом руководстве описано, как использовать [Microsoft Edge DevTools][MicrosoftEdgeDevTools] для проверки данных в веб-приложении SQL.</span><span class="sxs-lookup"><span data-stu-id="ccd0c-106">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to inspect Web SQL data.</span></span>  

## <span data-ttu-id="ccd0c-107">Просмотр данных в веб-SQL</span><span class="sxs-lookup"><span data-stu-id="ccd0c-107">View Web SQL Data</span></span>   

1.  <span data-ttu-id="ccd0c-108">Перейдите на вкладку **источники** , чтобы открыть панель " **источники** ".</span><span class="sxs-lookup"><span data-stu-id="ccd0c-108">Select the **Sources** tab to open the **Sources** panel.</span></span>  <span data-ttu-id="ccd0c-109">Обычно область **манифеста** открывается по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ccd0c-109">The **Manifest** pane usually opens by default.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-manifest.msft.png":::
       <span data-ttu-id="ccd0c-111">Область « **Манифест** »</span><span class="sxs-lookup"><span data-stu-id="ccd0c-111">The **Manifest** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ccd0c-112">Разверните раздел **веб-SQL** , чтобы просмотреть базы данных и таблицы.</span><span class="sxs-lookup"><span data-stu-id="ccd0c-112">Expand the **Web SQL** section to view databases and tables.</span></span>  <span data-ttu-id="ccd0c-113">На приведенном ниже рисунке под **html5meetup** является база данных, а **комнаты** — таблица.</span><span class="sxs-lookup"><span data-stu-id="ccd0c-113">In the following figure, below **html5meetup** is a database and **rooms** is a table.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-storage-web-sql.msft.png":::
       <span data-ttu-id="ccd0c-115">Область " **веб-SQL** "</span><span class="sxs-lookup"><span data-stu-id="ccd0c-115">The **Web SQL** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ccd0c-116">Выберите таблицу, чтобы просмотреть данные для этой таблицы.</span><span class="sxs-lookup"><span data-stu-id="ccd0c-116">Select a table to view the data for that table.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql-html5meetup-rooms-1.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-storage-web-sql-html5meetup-rooms-1.msft.png":::
       <span data-ttu-id="ccd0c-118">Просмотр данных таблицы веб-SQL</span><span class="sxs-lookup"><span data-stu-id="ccd0c-118">View the data of a Web SQL table</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="ccd0c-119">Изменение данных в веб-SQL</span><span class="sxs-lookup"><span data-stu-id="ccd0c-119">Edit Web SQL data</span></span>   

<span data-ttu-id="ccd0c-120">Вы не можете редактировать данные веб-SQL при просмотре таблицы веб-SQL (например, на **рис. 3** выше).</span><span class="sxs-lookup"><span data-stu-id="ccd0c-120">You are not able to edit Web SQL data when viewing a Web SQL table, such as in **Figure 3** above.</span></span>  <span data-ttu-id="ccd0c-121">Но вы можете запускать на веб-сайте SQL инструкции для редактирования и удаления таблиц.</span><span class="sxs-lookup"><span data-stu-id="ccd0c-121">But you may run statements from the Web SQL Console that edit or delete tables.</span></span>  <span data-ttu-id="ccd0c-122">Дополнительные сведения: [запуск запросов Web SQL](#run-web-sql-queries).</span><span class="sxs-lookup"><span data-stu-id="ccd0c-122">See [Run Web SQL queries](#run-web-sql-queries).</span></span>  

## <span data-ttu-id="ccd0c-123">Выполнение запросов на веб-SQL</span><span class="sxs-lookup"><span data-stu-id="ccd0c-123">Run Web SQL queries</span></span>   

1.  <span data-ttu-id="ccd0c-124">Выберите базу данных, чтобы открыть для нее консоль.</span><span class="sxs-lookup"><span data-stu-id="ccd0c-124">Select a database to open a console for that database.</span></span>  
1.  <span data-ttu-id="ccd0c-125">Введите инструкцию веб-SQL и нажмите `Enter` для ее запуска.</span><span class="sxs-lookup"><span data-stu-id="ccd0c-125">Type a Web SQL statement, then press `Enter` to run it.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql-html5meetup-commands.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-storage-web-sql-html5meetup-commands.msft.png":::
       <span data-ttu-id="ccd0c-127">Удаление строки из таблицы с помощью веб-консоли SQL</span><span class="sxs-lookup"><span data-stu-id="ccd0c-127">Use the Web SQL Console to delete a row from a table</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="ccd0c-128">Обновление таблицы веб-SQL</span><span class="sxs-lookup"><span data-stu-id="ccd0c-128">Refresh a Web SQL table</span></span>   

<span data-ttu-id="ccd0c-129">DevTools не обновляет таблицы в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="ccd0c-129">DevTools does not update tables in real-time.</span></span>  <span data-ttu-id="ccd0c-130">Чтобы обновить данные в таблице, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="ccd0c-130">To update the data in a table:</span></span>  

1.  <span data-ttu-id="ccd0c-131">[Просмотр данных в таблице веб-SQL](#view-web-sql-data).</span><span class="sxs-lookup"><span data-stu-id="ccd0c-131">[View the data in a Web SQL table](#view-web-sql-data).</span></span>  
1.  <span data-ttu-id="ccd0c-132">Нажмите кнопку **Обновить** \ ( ![ обновить ][ImageRefreshIcon] \).</span><span class="sxs-lookup"><span data-stu-id="ccd0c-132">Select **Refresh** \(![Refresh][ImageRefreshIcon]\).</span></span>  
    
## <span data-ttu-id="ccd0c-133">Фильтрация столбцов в таблице веб-SQL</span><span class="sxs-lookup"><span data-stu-id="ccd0c-133">Filter out columns in a Web SQL table</span></span>   

1.  <span data-ttu-id="ccd0c-134">[Просмотр данных в таблице веб-SQL](#view-web-sql-data).</span><span class="sxs-lookup"><span data-stu-id="ccd0c-134">[View the data in a Web SQL table](#view-web-sql-data).</span></span>  
1.  <span data-ttu-id="ccd0c-135">С помощью текстового поля **видимые столбцы** можно указать, какие столбцы вы хотите отобразить.</span><span class="sxs-lookup"><span data-stu-id="ccd0c-135">Use the **Visible columns** text box to specify what columns you want to show.</span></span>  <span data-ttu-id="ccd0c-136">Укажите имена столбцов в виде CSV-списка.</span><span class="sxs-lookup"><span data-stu-id="ccd0c-136">Provide the column names as a CSV list.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql-html5meetup-rooms-2.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-storage-web-sql-html5meetup-rooms-2.msft.png":::
       <span data-ttu-id="ccd0c-138">Использование текстового поля " **видимые столбцы** " для уменьшения количества отображаемых столбцов</span><span class="sxs-lookup"><span data-stu-id="ccd0c-138">Use the **Visible Columns** text box to reduce the number of columns shown</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="ccd0c-139">Удаление всех данных из веб-SQL</span><span class="sxs-lookup"><span data-stu-id="ccd0c-139">Delete all Web SQL data</span></span>   

1.  <span data-ttu-id="ccd0c-140">Открытие области **очистки хранилища** .</span><span class="sxs-lookup"><span data-stu-id="ccd0c-140">Open the **Clear Storage** pane.</span></span>  
1.  <span data-ttu-id="ccd0c-141">Убедитесь, что установлен флажок **веб-SQL** .</span><span class="sxs-lookup"><span data-stu-id="ccd0c-141">Make sure that the **Web SQL** checkbox is enabled.</span></span>  
    
    :::image type="complex" source="../media/storage-application-clear-storage-web-sql.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-clear-storage-web-sql.msft.png":::
       <span data-ttu-id="ccd0c-143">Флажок " **веб-SQL** "</span><span class="sxs-lookup"><span data-stu-id="ccd0c-143">The **Web SQL** checkbox</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ccd0c-144">Нажмите кнопку **Очистить данные сайта**.</span><span class="sxs-lookup"><span data-stu-id="ccd0c-144">Select **Clear site data**.</span></span>  
    
    :::image type="complex" source="../media/storage-application-clear-storage-clear-site-data-button.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-clear-storage-clear-site-data-button.msft.png":::
       <span data-ttu-id="ccd0c-146">Кнопка " **Очистить данные сайта** "</span><span class="sxs-lookup"><span data-stu-id="ccd0c-146">The **Clear Site Data** button</span></span>  
    :::image-end:::  
    
<!--  
 


-->  

<!-- image links -->  

[ImageRefreshIcon]: ../media/refresh-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Инструменты разработчика Microsoft EDGE (Chromium) | Документы Microsoft"  

[W3CWebSQLStatus]: https://w3.org/TR/webdatabase/#status-of-this-document "База данных веб-SQL | PNG"  

> [!NOTE]
> <span data-ttu-id="ccd0c-149">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ccd0c-149">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="ccd0c-150">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/storage/websql) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="ccd0c-150">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/websql) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="ccd0c-152">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ccd0c-152">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
