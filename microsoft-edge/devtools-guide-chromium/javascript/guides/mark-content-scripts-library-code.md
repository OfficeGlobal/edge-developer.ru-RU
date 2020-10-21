---
description: Включите параметр "помечать сценарии содержимого как код библиотеки" в настройках > код библиотеки Framework.
title: Пометка сценария содержимого как кода библиотеки
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 2a9bca703004b6232bef857d7b9e2f45458db52d
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "11124700"
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

# Помечайте сценарии содержимого как код библиотеки  

При использовании панели **Sources (источники** данных) Microsoft Edge DevTools для [перехода по коду][DevToolsJavascriptStepThroughCode], иногда наведите указатель мыши на код, который вы не знаете.  Возможно, вы приостановили код для одного из установленных расширений Microsoft Edge.  Выполните указанные ниже действия, чтобы не приостанавливаться на коде расширения.  

1.  Откройте DevTools, нажмите кнопку **Настройка DevTools и** `...` выберите пункт **Параметры**.  Вы также можете открыть **Параметры** , выбрав `F1` .  

1.  Откройте вкладку **код библиотеки** , которая открывает раздел **код библиотеки Framework** **параметров**.  
1.  Установите флажок **помечать сценарии содержимого как библиотечный код** .  
    
    :::image type="complex" source="../../media/javascript-settings-library-code-mark-content-scripts-library-code.msft.png" alt-text="Флажок &quot;помечать сценарии содержимого как библиотеку кода&quot;" lightbox="../../media/javascript-settings-library-code-mark-content-scripts-library-code.msft.png":::
       Флажок " **помечать сценарии содержимого как библиотеку кода** "  
    :::image-end:::  
    
## Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsJavascriptStepThroughCode]: ../index.md#step-4-step-through-the-code "Шаг 4: пошаговое руководство по написанию кода — начало работы с отладкой JavaScript в Microsoft Edge DevTools | Документы Microsoft"  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/javascript/guides/blackbox-chrome-extension-scripts) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
