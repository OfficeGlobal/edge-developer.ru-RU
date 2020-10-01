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





# Просмотр данных из веб-SQL с помощью Microsoft Edge DevTools   



> [!WARNING]
> Спецификация веб-SQL [не поддерживается][W3CWebSQLStatus].  

В этом руководстве описано, как использовать [Microsoft Edge DevTools][MicrosoftEdgeDevTools] для проверки данных в веб-приложении SQL.  

## Просмотр данных в веб-SQL   

1.  Перейдите на вкладку **источники** , чтобы открыть панель " **источники** ".  Обычно область **манифеста** открывается по умолчанию.  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-manifest.msft.png":::
       Область « **Манифест** »  
    :::image-end:::  
    
1.  Разверните раздел **веб-SQL** , чтобы просмотреть базы данных и таблицы.  На приведенном ниже рисунке под **html5meetup** является база данных, а **комнаты** — таблица.  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-storage-web-sql.msft.png":::
       Область " **веб-SQL** "  
    :::image-end:::  
    
1.  Выберите таблицу, чтобы просмотреть данные для этой таблицы.  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql-html5meetup-rooms-1.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-storage-web-sql-html5meetup-rooms-1.msft.png":::
       Просмотр данных таблицы веб-SQL  
    :::image-end:::  
    
## Изменение данных в веб-SQL   

Вы не можете редактировать данные веб-SQL при просмотре таблицы веб-SQL (например, на **рис. 3** выше).  Но вы можете запускать на веб-сайте SQL инструкции для редактирования и удаления таблиц.  Дополнительные сведения: [запуск запросов Web SQL](#run-web-sql-queries).  

## Выполнение запросов на веб-SQL   

1.  Выберите базу данных, чтобы открыть для нее консоль.  
1.  Введите инструкцию веб-SQL и нажмите `Enter` для ее запуска.  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql-html5meetup-commands.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-storage-web-sql-html5meetup-commands.msft.png":::
       Удаление строки из таблицы с помощью веб-консоли SQL  
    :::image-end:::  
    
## Обновление таблицы веб-SQL   

DevTools не обновляет таблицы в режиме реального времени.  Чтобы обновить данные в таблице, выполните указанные ниже действия.  

1.  [Просмотр данных в таблице веб-SQL](#view-web-sql-data).  
1.  Нажмите кнопку **Обновить** \ ( ![ обновить ][ImageRefreshIcon] \).  
    
## Фильтрация столбцов в таблице веб-SQL   

1.  [Просмотр данных в таблице веб-SQL](#view-web-sql-data).  
1.  С помощью текстового поля **видимые столбцы** можно указать, какие столбцы вы хотите отобразить.  Укажите имена столбцов в виде CSV-списка.  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql-html5meetup-rooms-2.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-storage-web-sql-html5meetup-rooms-2.msft.png":::
       Использование текстового поля " **видимые столбцы** " для уменьшения количества отображаемых столбцов  
    :::image-end:::  
    
## Удаление всех данных из веб-SQL   

1.  Открытие области **очистки хранилища** .  
1.  Убедитесь, что установлен флажок **веб-SQL** .  
    
    :::image type="complex" source="../media/storage-application-clear-storage-web-sql.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-clear-storage-web-sql.msft.png":::
       Флажок " **веб-SQL** "  
    :::image-end:::  
    
1.  Нажмите кнопку **Очистить данные сайта**.  
    
    :::image type="complex" source="../media/storage-application-clear-storage-clear-site-data-button.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-clear-storage-clear-site-data-button.msft.png":::
       Кнопка " **Очистить данные сайта** "  
    :::image-end:::  
    
<!--  
 


-->  

<!-- image links -->  

[ImageRefreshIcon]: ../media/refresh-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Инструменты разработчика Microsoft EDGE (Chromium) | Документы Microsoft"  

[W3CWebSQLStatus]: https://w3.org/TR/webdatabase/#status-of-this-document "База данных веб-SQL | PNG"  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/storage/websql) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
