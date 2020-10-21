---
description: Открыть консоль, создать выражение в реальном времени и задать для него выражение Document. activeElement.
title: Отслеживание, какой элемент имеет фокус
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: a0d0861494db87e546443c0f3a1d4f531412300c
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125309"
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

# Отслеживание, какой элемент имеет фокус  

Предположим, что вы тестируете специальные возможности навигации с помощью клавиатуры для страницы.  При переходе по странице с помощью `Tab` клавиши иногда теряется фокус, так как элемент, на который установлен фокус, скрыт.  

Чтобы отследить фокусируемый элемент в DevTools, выполните указанные ниже действия.  

1.  Открытие **консоли**.  
1.  Выберите **создать выражение в реальном времени** \ ( ![ создать выражение в реальном времени ][ImageCreateIcon] ).  
    
    :::image type="complex" source="../media/accessibility-console-create-live-expression-empty.msft.png" alt-text="Создание выражения в реальном времени" lightbox="../media/accessibility-console-create-live-expression-empty.msft.png":::
       Создание выражения в реальном времени  
    :::image-end:::  
    
1.  Введите `document.activeElement`.  
1.  Щелкните за пределами пользовательского интерфейса **Live Expression** , чтобы сохранить его.  
    
Значение, которое вы видите ниже, `document.activeElement` является результатом выражения.  

Так как это выражение всегда представляет фокусируемый элемент, вы можете всегда следить за тем, какой элемент находится в фокусе.  

*   Наведите указатель мыши на результат, чтобы выделиь фокусируемый элемент в окне просмотра.  
*   Щелкните результат правой кнопкой мыши и выберите пункт **Показать на панели элементов** , чтобы отобразить элемент в дереве DOM на панели **элементы** .  
*   Щелкните результат правой кнопкой мыши и выберите **Сохранить как глобальную переменную** , чтобы создать ссылку на переменную на узел, который вы можете использовать на **консоли**.  

## Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageCreateIcon]: ../media/create-live-expression-icon.msft.png  

<!-- links -->  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/accessibility/focus) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
