---
description: Откройте вкладку датчики и выберите координаты в списке географическое положение.
title: Переопределение географического положения с помощью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 269e7ca4bf259aa168c06ac0fd915604731463c4
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/02/2020
ms.locfileid: "10992990"
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

# Переопределение географического положения с помощью Microsoft Edge DevTools  

Многие веб-сайты имеют преимущество для предоставления пользователям более подходящих возможностей.  Например, на веб-сайте Weather может отображаться локальный прогноз в области пользователя, после того как пользователь выдает разрешение веб-сайту на доступ к текущему расположению пользователя.  

<!--todo: add link to user location section when available -->  

Если вы создаете пользовательский интерфейс, который изменяется в зависимости от того, где находится пользователь, возможно, вы захотите убедиться в том, что сайт правильно работает в разных местах по всему миру.  Чтобы переопределить географическое положение в Microsoft Edge DevTools, выполните указанные ниже действия.  

1.  `Control` + `Shift` + `P` Чтобы открыть меню команд, нажмите клавиши \ (Windows \) или `Command` + `Shift` + `P` \ ( **Command Menu**macOS \).  
    
    :::image type="complex" source="../media/device-mode-console-command-menu.msft.png" alt-text="Меню команд" lightbox="../media/device-mode-console-command-menu.msft.png":::
       **Меню команд**  
    :::image-end:::  
    
1.  Введите текст `sensors` , установите флажок **Показать датчики**и нажмите клавишу `Enter` .  Вкладка **датчики** откроется в нижней части окна DevTools.  
1.  В списке **географическое положение** выберите один из готовых городов `Tokyo` или выберите **другое расположение** , чтобы указать пользовательские координаты долготы и широты, или выберите пункт **расположение недоступно** , чтобы увидеть, как работает сайт, когда его расположение недоступно.  
    
    :::image type="complex" source="../media/device-mode-console-sensors-geolocation-tokyo.msft.png" alt-text="Меню команд" lightbox="../media/device-mode-console-sensors-geolocation-tokyo.msft.png":::
       Выберите в `Tokyo` списке " **географическое положение** "  
    :::image-end:::  
    
## Взаимодействие с командой средств разработчика Microsoft Edge

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

<!--[WebFundamentalsNativeHardwareUserLocationIndex]: /web/fundamentals/native-hardware/user-location/index "User Location"  -->  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/device-mode/geolocation) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
