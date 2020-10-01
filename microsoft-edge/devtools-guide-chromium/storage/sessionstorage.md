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





# Просмотр и изменение хранилища сеанса с помощью Microsoft Edge DevTools   

  

В этом руководстве описано, как использовать [Microsoft Edge DevTools][MicrosoftEdgeDevTools] для просмотра, изменения и удаления [`sessionStorage`][MDNSessionStorage] пар "ключ-значение".  

## Просмотр ключей и значений sessionStorage   

1.  Перейдите на вкладку **приложение** , чтобы открыть панель **приложения** .  Область **манифеста** отображается по умолчанию.  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-manifest.msft.png":::
       Область « **Манифест** »  
    :::image-end:::  
    
1.  Разверните меню **хранилище сеанса** .  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-storage-session-storage.msft.png":::
       Меню « **хранилище сеанса** »  
    :::image-end:::  
    
1.  Выберите домен, чтобы просмотреть пары "ключ-значение".  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-storage-session-storage-domain.msft.png":::
       `sessionStorage`Пары "ключ-значение"  
    :::image-end:::  
    
1.  Выделите строку таблицы, чтобы просмотреть ее значение в представлении под таблицей.  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain-key-value-selected.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-storage-session-storage-domain-key-value-selected.msft.png":::
       Просмотр значения `x-sid` ключа  
    :::image-end:::  
    
## Создание новой пары "ключ-значение" для sessionStorage   

1.  [Просмотр `sessionStorage` пар "ключ-значение" домена](#view-sessionstorage-keys-and-values).  
1.  Дважды щелкните пустую часть таблицы.  DevTools создает новую строку и нафокусирует указатель мыши на **ключевом** столбце.  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain-key-value-new.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-storage-session-storage-domain-key-value-new.msft.png":::
       Пустая часть таблицы для двойного щелчка, чтобы создать новую пару ключ-значение.  
    :::image-end:::  
    
## Изменение ключей и значений sessionStorage   

1.  [Просмотр `sessionStorage` пар "ключ-значение" домена](#view-sessionstorage-keys-and-values).  
1.  Дважды щелкните ячейку в столбце " **раздел** " или " **значение** ", чтобы изменить этот раздел или значение.  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain-key-value-edit.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-storage-session-storage-domain-key-value-edit.msft.png":::
       Изменение `sessionStorage` ключа  
    :::image-end:::  
    
## Удаление пар ключ-значение sessionStorage   

1.  [Просмотр `sessionStorage` пар "ключ-значение" домена](#view-sessionstorage-keys-and-values).  
1.  Выберите пару "ключ-значение", которую вы хотите удалить.  DevTools выделит ее синей, чтобы показать, что она выбрана.  
1.  Нажмите клавишу `Delete` или нажмите кнопку **Удалить выделенные** \ ( ![ Удалить выбранные \ ][ImageDeleteIcon] ).  
    
## Удаление всех пар ключ-значение sessionStorage для домена   

1.  [Просмотр `sessionStorage` пар "ключ-значение" домена](#view-sessionstorage-keys-and-values).  
1.  Нажмите **Очистить все** \ ( ![ Очистить все ][ImageClearIcon] \).  
    
## Взаимодействие с sessionStorage с помощью консоли   

Так как вы можете запустить JavaScript на **консоли**, и так как **консоль** имеет доступ к контекстам JavaScript на странице, можно взаимодействовать с `sessionStorage` ней из **консоли**.  

1.  Используйте меню "контексты **JavaScript** " для изменения контекста JavaScript на **консоли** , если вы хотите получить доступ к `sessionStorage` парам "ключ-значение" домена, отличного от страницы, на которой вы являетесь.  
    
    :::image type="complex" source="../media/storage-console-domain-selection.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-console-domain-selection.msft.png":::
       Изменение контекста JavaScript консоли  
    :::image-end:::  
    
1.  Выполняйте `sessionStorage` выражения на консоли так же, как и в JavaScript.  
    
    :::image type="complex" source="../media/storage-console-session-storage-keys.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-console-session-storage-keys.msft.png":::
       Взаимодействие с `sessionStorage` **консолью**  
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
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/storage/sessionstorage) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
