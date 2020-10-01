---
description: Инструкции по просмотру данных из кэша на панели приложения Microsoft Edge DevTools.
title: Просмотр данных кэша с помощью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: c920a171ec89925cc79ab741eed01e11d749bf1b
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993298"
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





# Просмотр данных кэша с помощью Microsoft Edge DevTools   



В этом руководстве описано, как использовать [Microsoft Edge DevTools][MicrosoftEdgeDevTools] для проверки данных [кэша][MDNCache] .  

Если вы пытаетесь проверить данные [кэша HTTP][MDNHTTPCaching] , это не значит, что вам нужно.  Найдите данные в столбце " **Размер** " в **сетевом журнале**.  Просмотр [журнала активности сети][DevtoolsNetworkLogActivity].  

## Просмотр данных кэша   

1.  Перейдите на вкладку **приложение** , чтобы открыть панель **приложения** .  Обычно область **манифеста** открывается по умолчанию.  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-manifest.msft.png":::
       Область « **Манифест** »  
    :::image-end:::  
    
1.  Разверните раздел **хранилище кэша** , чтобы просмотреть доступные кэши.  
    
    :::image type="complex" source="../media/storage-application-cache-storage.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-cache-storage.msft.png":::
       Доступные кэши  
    :::image-end:::  
    
1.  Выберите кэш, чтобы просмотреть его содержимое.  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-root-headers.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-cache-storage-domain-root-headers.msft.png":::
       Просмотр содержимого кэша  
    :::image-end:::  
    
1.  Выберите ресурс для просмотра заголовков HTTP в разделе под таблицей.  
    
    :::image type="complex" source="../media/storage-application-cache-storage-index-headers.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-cache-storage-index-headers.msft.png":::
       Просмотр заголовков HTTP для ресурса  
    :::image-end:::  
    
1.  Нажмите кнопку **Предварительный просмотр** , чтобы просмотреть содержимое ресурса.  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-js-preview.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-cache-storage-domain-js-preview.msft.png":::
       Просмотр содержимого ресурса  
    :::image-end:::  
    
## Обновление ресурса   

1.  [Просмотр данных для кэша](#view-cache-data).  
1.  Выберите ресурс, который вы хотите обновить.  DevTools выделит ее, чтобы показать, что она выбрана.  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-refresh.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-cache-storage-domain-refresh.msft.png":::
       Выберите ресурс  
    :::image-end:::  
    
1.  Нажмите кнопку **Обновить** \ ( ![ обновить ][ImageRefreshIcon] \).  
    
## Фильтрация ресурсов   

1.  [Просмотр данных для кэша](#view-cache-data).  
1.  С помощью текстового поля **Фильтр по пути** можно отфильтровать ресурсы, которые не соответствуют указанному вами пути.  
    
    :::image type="complex" source="../media/storage-application-cache-storage-filter.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-cache-storage-filter.msft.png":::
       Фильтрация ресурсов, не соответствующих указанному пути  
    :::image-end:::  
    
## Удаление ресурса   

1.  [Просмотр данных для кэша](#view-cache-data).  
1.  Выберите ресурс, который вы хотите удалить.  DevTools выделит ее, чтобы показать, что она выбрана.  
    
    :::image type="complex" source="../media/storage-application-cache-storage-delete-selected.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-cache-storage-delete-selected.msft.png":::
       Выберите ресурс  
    :::image-end:::  
    
1.  Нажмите кнопку " **Удалить** " ![ , а затем "удалить выбрано ][ImageDeleteIcon] ".  
    
## Удаление всех данных из кэша   

1.  Откройте **приложение**  >  , чтобы**Очистить хранилище**.  
1.  Убедитесь, что флажок **хранилище кэша** включен.  
    
    :::image type="complex" source="../media/storage-application-clear-storage-cache-storage-checkbox.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-clear-storage-cache-storage-checkbox.msft.png":::
       Флажок " **хранилище кэша** "  
    :::image-end:::  
    
1.  Нажмите кнопку **Очистить данные сайта**.  
    
    :::image type="complex" source="../media/storage-application-clear-storage-cache-storage-checkbox-clear-site-data-button.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-clear-storage-cache-storage-checkbox-clear-site-data-button.msft.png":::
       Кнопка " **Очистить данные сайта** "  
    :::image-end:::  
    
<!--  
  


-->  

<!-- image links -->  

[ImageDeleteIcon]: ../media/delete-icon.msft.png  
[ImageRefreshIcon]: ../media/refresh-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Инструменты разработчика Microsoft EDGE (Chromium) | Документы Microsoft"  
[DevtoolsNetworkLogActivity]: ../network/index.md#log-network-activity  "Регистрация активности в сети | Документы Microsoft"  

[MDNCache]: https://developer.mozilla.org/docs/Web/API/Cache "Кэш | MDN"  
[MDNHTTPCaching]: https://developer.mozilla.org/docs/Web/HTTP/Caching "Кэширование HTTP | MDN"  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/storage/cache) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
