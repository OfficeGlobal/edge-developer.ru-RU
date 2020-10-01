---
description: Руководство по открытию меню команд, выполнению команд, просмотрев другие действия и многое другое.
title: Выполнение команд с помощью командного меню Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 54dead492e7d58053efab77c82a10e7e3c912460
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993200"
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





# Выполнение команд с помощью командного меню Microsoft Edge DevTools   

  

Меню команд предоставляет быстрый способ навигации по пользовательскому интерфейсу Microsoft Edge DevTools и выполнения стандартных задач, таких как [Отключение JavaScript][JavascriptDisable].  Возможно, вы знакомы с аналогичной функцией в коде Visual Studio, которая называется [палитрой команд][VisualStudioCodeUICommandPalette], которая была первоначальной для меню команд.  

:::image type="complex" source="../media/command-menu-run-command-java.msft.png" alt-text="Отключение JavaScript с помощью меню команд" lightbox="../media/command-menu-run-command-java.msft.png":::
   Отключение JavaScript с помощью меню команд  
:::image-end:::  

## Открытие меню команд   

Нажмите клавиши `Control` + `Shift` + `P` \ (Windows \) или `Command` + `Shift` + `P` \ (macOS \). Или нажмите кнопку **Настройка DevTools** `...` и выберите **команду выполнить**.  

:::image type="complex" source="../media/command-menu-options-run-command.msft.png" alt-text="Отключение JavaScript с помощью меню команд" lightbox="../media/command-menu-options-run-command.msft.png":::
   Команда "выполнить"  
:::image-end:::  

## Просмотр других доступных действий   

Если вы используете рабочий процесс, описанный в разделе [Открыть меню команд](#open-the-command-menu), откроется меню команд с `>` символом, предварительно заданным в текстовом поле меню команды.  

:::image type="complex" source="../media/command-menu-run-command.msft.png" alt-text="Отключение JavaScript с помощью меню команд" lightbox="../media/command-menu-run-command.msft.png":::
   Символ команды  
:::image-end:::  

Удалите `>` символ и введите текст `?` , чтобы просмотреть другие действия, доступные в меню команд.  

:::image type="complex" source="../media/command-menu-help.msft.png" alt-text="Отключение JavaScript с помощью меню команд" lightbox="../media/command-menu-help.msft.png":::
   Другие доступные действия  
:::image-end:::  

 



<!-- links -->  

[JavascriptDisable]: ../javascript/disable.md "Отключение JavaScript в Microsoft Edge DevTools | Документы Microsoft"  

[VisualStudioCodeUICommandPalette]: https://code.visualstudio.com/docs/getstarted/userinterface#_command-palette "Палитра команд — пользовательский интерфейс кода Visual Studio"  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/command-menu/index) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
