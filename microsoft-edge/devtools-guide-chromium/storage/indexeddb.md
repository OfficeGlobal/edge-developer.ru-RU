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





# Просмотр и изменение IndexedDBных данных с помощью Microsoft Edge DevTools   

  

В этом руководстве описано, как использовать [Microsoft Edge DevTools][MicrosoftEdgeDevTools] для просмотра и изменения [IndexedDB][MDNIndexedDBAPI] данных.  Предполагается, что вы знакомы с DevTools.  Кроме того, предполагается, что вы знакомы с IndexedDB.  В противном случае ознакомьтесь [с разIndexedDB][MDNUsingIndexedDB].  

## Просмотр данных IndexedDB   

1.  Перейдите на вкладку **приложение** , чтобы открыть панель **приложения** .  Обычно область **манифеста** открывается по умолчанию.  
    
    :::image type="complex" source="../media/storage-application-manifest-empty.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-manifest-empty.msft.png":::
       Область « **Манифест** »  
    :::image-end:::  
    
1.  Разверните меню **IndexedDB** , чтобы узнать, какие базы данных доступны.  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-storage-indexeddb.msft.png":::
       Меню **IndexedDB**  
    :::image-end:::  
    
    *   \ ( ![ Значок базы данных ][ImageDatabaseIcon] \) `notes - https://mdn.github.io` представляет базу данных, где `notes` — это имя базы данных, а `https://mdn.github.io` также источник, который получает доступ к базе данных.  
    *   \ ( ![ Значок хранилища объектов ][ImageObjectStoreIcon] \) `notes` — это хранилище объектов.  
    *   **заголовок** и **текст** — это [индексы][MDNUsingIndexedDBUsingIndex].  
    
    > [!NOTE]
    > **Известное ограничение**  Сторонние базы данных не видны.  Например, если вы используете `<iframe>` для внедрения баннера на странице, а в вашей рекламной сети используется IndexedDB, данные IndexedDB для вашей рекламной сети не будут видны.  Просмотреть [#943770 вопросов][ChromiumIssue943770].  
    
1.  Выберите базу данных, чтобы увидеть источник и номер версии.  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-storage-indexeddb-notes_db.msft.png":::
       База данных **Notes**  
    :::image-end:::  
    
1.  Выберите хранилище объектов для просмотра пар "ключ-значение".  
    
    > [!NOTE]
    > Данные IndexedDB не обновляются в режиме реального времени.  Смотрите раздел [Обновление данных IndexedDB](#refresh-indexeddb-data).  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os.msft.png":::
       Хранилище объектов " **заметки** "  
    :::image-end:::  
    
    *   **Всего элементов** — общее количество пар "ключ-значение" в хранилище объектов.  
    *   **Значение ключевого генератора** — это следующий доступный ключ.  Это поле отображается только при использовании [генераторов ключей][MDNBasicConceptsKeyGenerator].  
    
1.  Выберите ячейку в столбце **значение** , чтобы развернуть это значение.  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-edge-chromium.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-edge-chromium.msft.png":::
       Просмотр значения **IndexedDB**  
    :::image-end:::  
    
1.  Выберите индекс (например, **заголовок** или **текст** ) на приведенном ниже рисунке, чтобы отсортировать хранилище объектов согласно значениям этого индекса.  
   
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-title.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-title.msft.png":::
       Сортировка хранилища объектов по индексу  
    :::image-end:::  
    
## Обновление данных IndexedDB   

Значения IndexedDB на панели **приложения** не обновляются в режиме реального времени.  Выберите команду **Обновить** \ ( ![ обновить ][ImageReloadIcon] \) при просмотре хранилища объектов, чтобы обновить данные, или просмотрите базу данных и нажмите **обновить базу данных** , чтобы обновить все данные.  

:::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-refresh-database.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-refresh-database.msft.png":::
   Просмотр базы данных  
:::image-end:::  

## Изменить данные IndexedDB   

IndexedDB ключи и значения не подлежат редактированию на панели **приложения** .  Так как DevTools имеет доступ к контексту страницы, вы можете выполнить код JavaScript в DevTools для редактирования IndexedDB данных.  

### Редактирование данных IndexedDB с помощью фрагментов   

[Фрагменты][DevtoolsJavascriptSnippets] — это способ хранения и выполнения блоков кода JavaScript в DevTools.  При выполнении фрагмента на **консоль**выписывается результат.  Вы можете использовать сниппет для выполнения кода JavaScript, чтобы изменить базу данных IndexedDB.  

:::image type="complex" source="../media/storage-sources-snippets-indexeddb-output.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-sources-snippets-indexeddb-output.msft.png":::
   Использование фрагмента для взаимодействия с IndexedDB  
:::image-end:::  

## Удаление данных IndexedDB   

### Удаление пары ключ-значение IndexedDB   

1.  [Просмотр хранилища объектов IndexedDB](#view-indexeddb-data).  
1.  Выберите пару "ключ-значение", которую вы хотите удалить.  DevTools выделит ее, чтобы показать, что она выбрана.  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os2.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os2.msft.png":::
       Выберите пару "ключ-значение", чтобы удалить ее  
    :::image-end:::  
    
1.  Нажмите клавишу `Delete` или нажмите кнопку **Удалить выделенные** \ ( ![ Удалить выбранные \ ][ImageDeleteIcon] ).  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-delete-selected.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-delete-selected.msft.png":::
       Как выглядит хранилище объектов после удаления пары "ключ-значение"  
    :::image-end:::  
    
### Удаление всех пар "ключ-значение" в хранилище объектов   

1.  [Просмотр хранилища объектов IndexedDB](#view-indexeddb-data).  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-clear-object-store.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-clear-object-store.msft.png":::
       Просмотр хранилища объектов  
    :::image-end:::  
    
1.  Выберите **Очистить хранилище объектов** \ ( ![ Очистить хранилище объектов ][ImageClearIcon] ).  
    
### Удаление базы данных IndexedDB   

1.  [Просмотрите базу данных IndexedDB](#view-indexeddb-data) , которую вы хотите удалить.  
1.  Выберите команду **Удалить базу данных**.  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-delete-database.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-storage-indexeddb-notes_db-delete-database.msft.png":::
       Кнопка " **Удалить базу данных** "  
    :::image-end:::  
    
### Удаление всех IndexedDB хранилища   

1.  Открытие области **очистки хранилища** .  
1.  Убедитесь, что флажок **IndexedDB** установлен.  
1.  Нажмите кнопку **Очистить данные сайта**.  
    
    :::image type="complex" source="../media/storage-application-clear-storage-indexeddb-clear-site-data.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-clear-storage-indexeddb-clear-site-data.msft.png":::
       Область " **Очистка хранилища** "  
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
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/storage/indexeddb) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
