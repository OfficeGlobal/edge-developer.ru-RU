---
description: Просмотр и редактирование localStorage с помощью панели "Локальные хранилище" и консоли.
title: Просмотр и изменение локального хранилища с помощью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 25404e454187db941dc12d356dfe5ae7437d833b
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125421"
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

# Просмотр и изменение локального хранилища с помощью Microsoft Edge DevTools  

В этом руководстве описано, как использовать [Microsoft Edge DevTools][MicrosoftEdgeDevTools] для просмотра, изменения и удаления пар ключ-значение [localStorage][MDNWindowsLocalStorage] .  

## Просмотр ключей и значений localStorage  

1.  Перейдите на вкладку **приложение** , чтобы открыть панель **приложения** .  Область **манифеста** отображается по умолчанию.  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-manifest.msft.png":::
       Область « **Манифест** »  
    :::image-end:::  
    
1.  Разверните меню **Локальное хранилище** .  
    
    :::image type="complex" source="../media/storage-application-local-storage.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-local-storage.msft.png":::
       Меню « **Локальное хранилище** »  
    :::image-end:::  
    
1.  Выберите домен, чтобы просмотреть пары "ключ-значение".  
    
    :::image type="complex" source="../media/storage-application-local-storage-view-key-value.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-local-storage-view-key-value.msft.png":::
       `localStorage`Пары "ключ-значение" для `https://www.bing.com` домена  
    :::image-end:::  
    
1.  Выделите строку таблицы, чтобы просмотреть ее значение в представлении под таблицей.  
    
    :::image type="complex" source="../media/storage-application-local-storage-view-key-value-selected.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-local-storage-view-key-value-selected.msft.png":::
       Просмотр значения `eventLogQueue_Online` ключа  
    :::image-end:::  
    
## Создание новой пары "ключ-значение" для localStorage  

1.  [Просмотр `localStorage` пар "ключ-значение" домена](#view-localstorage-keys-and-values).  
1.  Дважды щелкните пустую часть таблицы.  DevTools создает новую строку и нафокусирует указатель мыши на **ключевом** столбце.  
    
    :::image type="complex" source="../media/storage-application-local-storage-new-key-value.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-local-storage-new-key-value.msft.png":::
       Пустая часть таблицы для двойного щелчка, чтобы создать новую пару ключ-значение.  
    :::image-end:::  
    
## Изменение ключей и значений localStorage  

1.  [Просмотр `localStorage` пар "ключ-значение" домена](#view-localstorage-keys-and-values).  
1.  Дважды щелкните ячейку в столбце " **раздел** " или " **значение** ", чтобы изменить этот раздел или значение.  
    
    :::image type="complex" source="../media/storage-application-local-storage-edit-key-value.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-local-storage-edit-key-value.msft.png":::
       Изменение `localStorage` ключа  
    :::image-end:::  
    
## Удаление пар ключ-значение localStorage  

1.  [Просмотр `localStorage` пар "ключ-значение" домена](#view-localstorage-keys-and-values).  
1.  Выберите пару "ключ-значение", которую вы хотите удалить.  DevTools выделит ее синей, чтобы показать, что она выбрана.  
1.  Нажмите клавишу `Delete` или выберите команду **Удалить выделенные** \ ( ![ Удалить выбранные ][ImageDeleteIcon] \).  
    
## Удаление всех `localStorage` пар "ключ-значение" для домена  

1.  [Просмотр `localStorage` пар "ключ-значение" домена](#view-localstorage-keys-and-values).  
1.  Выберите **Очистить все** \ ( ![ Очистить все ][ImageClearIcon] \).  
    
## Взаимодействие с localStorage с помощью консоли  

Так как вы можете запускать JavaScript на **консоли**, а так как у **консоли** есть доступ к контекстам JavaScript страницы, взаимодействие с `localStorage` **консолью**возможно.  

1.  Используйте меню "контексты **JavaScript** " для изменения контекста JavaScript на **консоли** , если требуется получить доступ к `localStorage` парам "ключ-значение" домена, отличного от отображаемой страницы.  
    
    :::image type="complex" source="../media/storage-console-local-storage.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-console-local-storage.msft.png":::
       Изменение контекста JavaScript консоли  
    :::image-end:::  
    
1.  Выполняйте `localStorage` выражения на консоли так же, как и в JavaScript.  
    
    :::image type="complex" source="../media/storage-console-local-storage-interaction.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-console-local-storage-interaction.msft.png":::
       Взаимодействие с `localStorage` **консолью**  
    :::image-end:::  
    
## Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageClearIcon]: ../media/clear-icon.msft.png  
[ImageDeleteIcon]: ../media/delete-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Инструменты разработчика Microsoft EDGE (Chromium) | Документы Microsoft"  

[MDNWindowsLocalStorage]: https://developer.mozilla.org/docs/Web/API/Window/localStorage "Window. localStorage | MDN"  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/storage/localstorage) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
