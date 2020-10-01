---
description: Упорядочивайте ресурсы по кадрам, доменам, типам и другим критериям.
title: Просмотр ресурсов страницы с помощью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 4f90927cc4044c722d9a62ab4b0427aa2753e4c5
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993592"
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





# Просмотр ресурсов страницы с помощью Microsoft Edge DevTools   

  

В этом руководстве рассказывается, как использовать Microsoft Edge DevTools для просмотра ресурсов веб-страницы.  Ресурсы — это файлы, необходимые для правильного отображения страницы.  Примеры ресурсов включают CSS, JavaScript и HTML-файлы, а также изображения.  

В этом руководстве предполагается, что вы знакомы с основами [веб-разработки][MDNLearnWebDevelopment] и [Microsoft Edge DevTools][MicrosoftEdgeDevTools].  

## Открытие ресурсов   

Если вы знаете имя ресурса, который вы хотите проверить, **меню команд** предоставляет быстрый способ открытия ресурса.  

1.  Нажмите клавиши `Control` + `P` \ (Windows \) или `Command` + `P` \ (macOS \).  Откроется диалоговое окно **Открытие файла** .  
    
    :::image type="complex" source="../media/resources-command-menu-empty.msft.png" alt-text="Диалоговое окно «Открытие файла»" lightbox="../media/resources-command-menu-empty.msft.png":::
       Диалоговое окно « **Открытие файла** »  
    :::image-end:::  
    
1.  Выберите файл из раскрывающегося списка или введите имя файла и нажмите `Enter` один раз, чтобы выделить его в поле "Автозаполнение".  
    
    :::image type="complex" source="../media/resources-command-menu-file-search.msft.png" alt-text="Диалоговое окно «Открытие файла»" lightbox="../media/resources-command-menu-file-search.msft.png":::
       Введите имя файла в диалоговом окне " **Открытие файла** "  
    :::image-end:::  
    
### Открытие ресурсов на панели "сеть"   

Ознакомьтесь [с подробными сведениями о ресурсе][DevtoolsNetworkInspectDetailsResource].  

:::image type="complex" source="../media/resources-network-response.msft.png" alt-text="Диалоговое окно «Открытие файла»" lightbox="../media/resources-network-response.msft.png":::
   Проверка ресурса на панели " **сеть** "  
:::image-end:::  

### Показать ресурсы на панели "сеть" с других панелей   

В разделе [Обзор ресурсов](#browse-resources) ниже показано, как просматривать ресурсы из различных частей пользовательского интерфейса DevTools.  Если вы когда-нибудь хотите просмотреть ресурс на панели **сеть** , щелкните ресурс правой кнопкой мыши и выберите пункт **Показать на панели "сеть**".  

:::image type="complex" source="../media/resources-sources-page-reveal-in-network-panel.msft.png" alt-text="Диалоговое окно «Открытие файла»" lightbox="../media/resources-sources-page-reveal-in-network-panel.msft.png":::
   **Панель "Показать в сети"**  
:::image-end:::  

## Просмотр ресурсов   

### Просмотр ресурсов на панели «Сеть»   

Просмотр [журнала активности сети][DevtoolsNetworkLogActivity].  

:::image type="complex" source="../media/resources-network-resources.msft.png" alt-text="Диалоговое окно «Открытие файла»" lightbox="../media/resources-network-resources.msft.png":::
   Ресурсы страницы в журнале **сети**  
:::image-end:::  

### Просмотр по каталогу   

Чтобы просмотреть ресурсы на странице, упорядоченные по каталогу, выполните указанные ниже действия.  

1.  Перейдите на вкладку **источники** , чтобы открыть панель " **источники** ".  
1.  Щелкните вкладку **страницы** , чтобы показать ресурсы страницы.  Откроется область **страница** .  
    
    :::image type="complex" source="../media/resources-sources-page-empty.msft.png" alt-text="Диалоговое окно «Открытие файла»" lightbox="../media/resources-sources-page-empty.msft.png":::
       Область **страницы**  
    :::image-end:::  
    
    Ниже приведено разделение неочевидных элементов на предыдущем рисунке.  
    
    | Элемент страницы | Описание |  
    |:--- |:--- |  
    | `top` | Основной [контекст обзора][MDNInlineFrame]документов. |  
    | `airhorner.com` | Домен.  Все ресурсы, вложенные в него, поступают из этого домена.  Например, может быть задан полный URL-адрес `comlink.global.j` файла `https://airhorner.com/scripts/comlink.global.js` . |  
    | `scripts` | Каталог. |  
    | `(index)` | Основной HTML-документ. |  
    | `sw.js` | Контекст среды выполнения рабочего процесса службы. |  
    
1.  Щелкните ресурс, чтобы просмотреть его в **редакторе**.  
    
    :::image type="complex" source="../media/resources-sources-page-resource.msft.png" alt-text="Диалоговое окно «Открытие файла»" lightbox="../media/resources-sources-page-resource.msft.png":::
       Просмотр файла в **редакторе**  
    :::image-end:::  
    
### Просмотр по имени файла   

По умолчанию в области **страницы** ресурсы группируются по каталогам.  Чтобы отключить эту группировку и просмотреть ресурсы для каждого домена в виде плоского списка, выполните указанные ниже действия.  

1.  Открытие области **страницы** .  Просмотр [по каталогу](#browse-by-directory).  
1.  Нажмите кнопку **Дополнительные параметры** `...` и отключите функцию **Группировка по папкам**.  
    
    :::image type="complex" source="../media/resources-sources-page-resource-group-by-folder.msft.png" alt-text="Диалоговое окно «Открытие файла»" lightbox="../media/resources-sources-page-resource-group-by-folder.msft.png":::
       Параметр **Группировка по папке**  
    :::image-end:::  
    
    Ресурсы упорядочены по типам файлов.  В каждом типе файла ресурсы упорядочены по алфавиту.  
    
    :::image type="complex" source="../media/resources-sources-page-resources-empty-not-grouped-by-folder.msft.png" alt-text="Диалоговое окно «Открытие файла»" lightbox="../media/resources-sources-page-resources-empty-not-grouped-by-folder.msft.png":::
       Область **страницы** после отключения **группировки по папке**  
    :::image-end:::  
    
### Просмотр по типу файла   

Чтобы сгруппировать ресурсы в зависимости от типа файла:  

1.  Откройте вкладку **приложение** .  Откроется панель **приложения** .  По умолчанию область **манифеста** обычно открывается в первую очередь.  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner.msft.png" alt-text="Диалоговое окно «Открытие файла»" lightbox="../media/resources-application-mainfest-airhorner.msft.png":::
       Панель **приложения**  
    :::image-end:::  
    
1.  Прокрутите страницу вниз до области **рамок** .  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner-frames-expanded.msft.png" alt-text="Диалоговое окно «Открытие файла»" lightbox="../media/resources-application-mainfest-airhorner-frames-expanded.msft.png":::
       Область **рамок**  
    :::image-end:::  
    
1.  Разверните разделы, в которых вы заинтересованы.  
1.  Щелкните ресурс, чтобы просмотреть его.  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner-expanded-resources.msft.png" alt-text="Диалоговое окно «Открытие файла»" lightbox="../media/resources-application-mainfest-airhorner-expanded-resources.msft.png":::
       Просмотр ресурса на панели « **приложение** »  
    :::image-end:::  
    
#### Просмотр файлов по типу на панели «Сеть»   

Просмотреть [Фильтр по типу ресурсов][DevtoolsNetworkFilterByResourceType].  

:::image type="complex" source="../media/resources-network-resources-filter-css.msft.png" alt-text="Диалоговое окно «Открытие файла»" lightbox="../media/resources-network-resources-filter-css.msft.png":::
   Фильтр для CSS в **сетевом** журнале  
:::image-end:::  

<!--  
  


-->  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Инструменты разработчика Microsoft EDGE (Chromium) | Документы Microsoft"  
[DevtoolsNetworkFilterByResourceType]: ../network/index.md#filter-by-resource-type "Фильтрация по типу ресурсов: Проверка активности сети в Microsoft Edge DevTools | Документы Microsoft"  
[DevtoolsNetworkInspectDetailsResource]: ../network/index.md#inspect-the-details-of-the-resource "Просмотрите сведения об активности в сети для проверки ресурсов в Microsoft Edge DevTools | Документы Microsoft"  
[DevtoolsNetworkLogActivity]: ../network/index.md#log-network-activity "Регистрация активности сети — проверка активности сети в Microsoft Edge DevTools | Документы Microsoft"  

[MDNInlineFrame]: https://developer.mozilla.org/docs/Web/HTML/Element/iframe "<> IFRAME: элемент встроенной рамки | MDN"  
[MDNLearnWebDevelopment]: https://developer.mozilla.org/docs/Learn "Знакомство с веб-разработкой | MDN"  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/resources/index) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
