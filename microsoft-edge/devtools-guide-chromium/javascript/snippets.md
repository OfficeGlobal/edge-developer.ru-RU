---
description: Фрагменты — это небольшие сценарии, которые можно создавать и запускать на панели «источники» в Microsoft Edge DevTools.  Вы можете получать доступ к ним и запускать их на любой странице.  При запуске фрагмента кода выполняется из контекста открытой на данный момент страницы.
title: Выполнение фрагментов кода JavaScript на любой странице с Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: e353da76a5c354d834b69708c8a8c9e8dbdf9934
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "11124742"
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

# Выполнение фрагментов кода JavaScript на любой странице с Microsoft Edge DevTools  

Если вы обнаружите, что один и тот же код запускается повторно на [консоли][DevtoolsConsoleIndex] , попробуйте сохранить его как фрагмент кода.  Фрагменты — это сценарии, созданные вами на панели « [источники][DevToolsSourcesPanel] ».  У них есть доступ к контексту JavaScript на странице, и вы можете запускать их на любой странице.  Фрагменты — это альтернатива для [Закладка][WikiBookmarklet].  
В Firefox DevTools есть функция, похожая на фрагменты, которые называются [блокнотом][MDNScratchpad].  

Например, на приведенном ниже рисунке показана домашняя страница DevTools слева и фрагмент исходного кода справа.  

:::image type="complex" source="../media/javascript-sources-snippets-split-screen.msft.png" alt-text="Вид страницы перед выполнением фрагмента" lightbox="../media/javascript-sources-snippets-split-screen.msft.png":::
   Вид страницы перед выполнением фрагмента  
:::image-end:::  

Исходный код фрагмента на предыдущем рисунке.  

```javascript
console.log('Hello, Snippets!');
document.body.innerHTML = '';
var p = document.createElement('p');
p.textContent = 'Hello, Snippets!';
document.body.appendChild(p);
```  

На рисунке ниже показана страница после выполнения фрагмента.  Во всплывающем **ящике консоли** выводится `Hello, Snippets!` сообщение о том, что журналы фрагментов, и содержимое страницы полностью меняются.  

:::image type="complex" source="../media/javascript-sources-snippets-split-screen-after.msft.png" alt-text="Вид страницы перед выполнением фрагмента" lightbox="../media/javascript-sources-snippets-split-screen-after.msft.png":::
   Вид страницы после выполнения фрагмента  
:::image-end:::  

## Открытие области "фрагменты кода"  

На панели **фрагментов** перечислены ваши фрагменты.  Если вы хотите изменить фрагмент, необходимо открыть его из области **фрагментов** .  

:::image type="complex" source="../media/javascript-sources-snippets-pane.msft.png" alt-text="Вид страницы перед выполнением фрагмента" lightbox="../media/javascript-sources-snippets-pane.msft.png":::
   Область **фрагментов**  
:::image-end:::  

### Открытие области фрагментов с помощью мыши  

1.  Перейдите на вкладку **источники** , чтобы открыть панель " **источники** ".  Обычно область **страницы** открывается по умолчанию.  
    
    :::image type="complex" source="../media/javascript-sources-page-pane.msft.png" alt-text="Вид страницы перед выполнением фрагмента" lightbox="../media/javascript-sources-page-pane.msft.png":::
       Панель « **источники** » с открытой областью **страницы** в левой части экрана  
    :::image-end:::  
    
1.  Перейдите на вкладку **фрагменты кода** , чтобы открыть область **фрагменты** .  **More Tabs** ![ ][ImageMoreTabsIcon] Для доступа к параметру **фрагментов** может потребоваться выбрать дополнительные вкладки \ (дополнительные вкладки \).  
    
### Открытие области фрагментов с помощью меню команд  

1.  Сфокусировать указатель мыши в DevTools.  
1.  Выберите `Control` + `Shift` + `P` \ (Windows, Linux \) или `Command` + `Shift` + `P` \ (macOS \), чтобы открыть меню команд.  
1.  Начните вводить текст `Snippets` , нажмите кнопку **Показать фрагменты**, а затем выберите `Enter` для запуска команды.  
    
    :::image type="complex" source="../media/javascript-search-show-snippets.msft.png" alt-text="Вид страницы перед выполнением фрагмента" lightbox="../media/javascript-search-show-snippets.msft.png":::
       Команда « **Показать фрагменты** »  
    :::image-end:::  
    
## Создание фрагментов кода  

### Создание фрагмента с помощью панели «источники»  

1.  [Открытие области **фрагментов** ](#open-the-snippets-pane).  
1.  Выберите команду **создать фрагмент**.  
1.  Введите имя для фрагмента, а затем выберите `Enter` для сохранения.  
    
    :::image type="complex" source="../media/javascript-sources-snippets-naming.msft.png" alt-text="Вид страницы перед выполнением фрагмента" lightbox="../media/javascript-sources-snippets-naming.msft.png":::
       Присвоение имени фрагменту  
    :::image-end:::  
    
### Создание фрагмента с помощью меню команд  

1.  Сфокусировать указатель мыши в DevTools.  
1.  Выберите `Control` + `Shift` + `P` \ (Windows, Linux \) или `Command` + `Shift` + `P` \ (macOS \), чтобы открыть меню команд.  
1.  Начните вводить текст `Snippet` , выберите команду **создать фрагмент**, а затем нажмите кнопку, `Enter` чтобы выполнить команду.  
    
    :::image type="complex" source="../media/javascript-search-create-new-snippet.msft.png" alt-text="Вид страницы перед выполнением фрагмента" lightbox="../media/javascript-search-create-new-snippet.msft.png":::
       Команда для создания нового фрагмента.  
    :::image-end:::  
    
Если вы хотите присвоить новому фрагменту настраиваемое имя, просмотрите [фрагменты Rename](#rename-snippets) .  

## Редактирование фрагментов  

1.  [Открытие области **фрагментов** ](#open-the-snippets-pane).  
1.  В области **фрагменты** щелкните имя фрагмента, который вы хотите изменить, чтобы открыть его в **редакторе кода**.  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-saved.msft.png" alt-text="Вид страницы перед выполнением фрагмента" lightbox="../media/javascript-sources-snippets-editor-saved.msft.png":::
       **Редактор кода**  
    :::image-end:::  
    
1.  С помощью **редактора кода** добавьте JavaScript в сниппет.  
1.  Если рядом с именем фрагмента появится звездочка, это означает, что у вас есть несохраненный код. Выберите `Control` + `S` \ (Windows, Linux \) или `Command` + `S` \ (macOS \), чтобы сохранить его.  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-unsaved.msft.png" alt-text="Вид страницы перед выполнением фрагмента" lightbox="../media/javascript-sources-snippets-editor-unsaved.msft.png":::
       Звездочка рядом с именем фрагмента, обозначающее несохраненный код.  
    :::image-end:::  
    
## Выполнение фрагментов кода  

### Выполнение фрагмента на панели «источники»  

1.  [Открытие области **фрагментов** ](#open-the-snippets-pane).  
1.  Щелкните имя фрагмента, который вы хотите выполнить.  Фрагмент откроется в **редакторе кода**.  
1.  Выберите команду **выполнить фрагмент** \ ( ![ выполнить фрагмент ][ImageRunSnippetIcon] \) или выберите `Control` + `Enter` \ (Windows, Linux \) или `Command` + `Enter` \ (macOS \).  
    
### Выполнение фрагмента с помощью меню команд  

1.  Сфокусировать указатель мыши в DevTools.  
1.  Выберите `Control` + `Shift` + `P` \ (Windows, Linux \) или `Command` + `Shift` + `P` \ (macOS \), чтобы открыть меню команд.  
1.  Удалите `>` символ и введите символ, а `!` затем имя фрагмента, который вы хотите выполнить.  
    
    :::image type="complex" source="../media/javascript-search-run-command.msft.png" alt-text="Вид страницы перед выполнением фрагмента" lightbox="../media/javascript-search-run-command.msft.png":::
       Выполнение фрагмента из **меню команд**  
    :::image-end:::  
    
1.  Выберите `Enter` , чтобы запустить фрагмент.  

## Переименование фрагментов  

1.  [Открытие области **фрагментов** ](#open-the-snippets-pane).  
1.  Щелкните имя фрагмента правой кнопкой мыши и выберите команду **Переименовать**.  
    
## Удаление фрагментов  

1.  [Открытие области **фрагментов** ](#open-the-snippets-pane).  
1.  Щелкните имя фрагмента правой кнопкой мыши и выберите команду **Удалить**.  
    
## Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageMoreTabsIcon]: ../media/more-tabs-icon.msft.png  
[ImageRunSnippetIcon]: ../media/run-snippet-icon.msft.png  

<!-- links -->  

[DevtoolsConsoleIndex]: ../console/index.md "Обзор консоли | Документы Microsoft"  
[DevToolsSourcesPanel]: ../sources.md "Обзор панели «источники» | Документы Microsoft"  

[MDNScratchpad]: https://developer.mozilla.org/docs/Tools/Scratchpad "Пометок | MDN"  
[WikiBookmarklet]: https://en.wikipedia.org/wiki/Bookmarklet "Кнопка-«Википедии»"  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
