---
description: Просмотр и редактирование файлов, создание фрагментов, Отладка JavaScript и Настройка рабочих областей на панели «источники» в Microsoft Edge DevTools.
title: Обзор панели источников
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 971ee6e112daaba828a8b754b63eee73ea51e99e
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125330"
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

# Обзор панели источников  

С помощью панели DevTools **источники** Microsoft Edge выполните указанные ниже действия.  

*   [Просмотр файлов](#view-files).  
*   [Редактирование CSS и JavaScript](#edit-css-and-javascript).  
*   [Создавайте и сохраняйте **фрагменты кода** JavaScript](#create-save-and-run-snippets), которые можно запускать на любой странице.  **Фрагменты** аналогичны кнопкам для закладок.  
*   [Отладка JavaScript](#debug-javascript).  
*   [Настройте рабочую область](#set-up-a-workspace), чтобы изменения, внесенные в DevTools, сохранялись в коде в файловой системе.  
    
## Просмотр файлов  

Используйте область **страниц** для просмотра всех ресурсов, загруженных страницей.

:::image type="complex" source="./media/sources-page-pane.msft.png" alt-text="Область страницы" lightbox="./media/sources-page-pane.msft.png":::
   Область **страницы**  
:::image-end:::  

Упорядочение области **страницы** .  
*   Верхний уровень (например, `top` на предыдущем рисунке) представляет [рамку HTML][W3CHtml4Frames].  Найдите `top` на каждой странице, которую вы посещаете.  `top` представляет рамку основного документа.  
*   Второй уровень (например, `docs.microsoft.com` на предыдущем рисунке) представляет [источник][HtmlstandardOrigin].  
*   Третий уровень, четвертый уровень и т. д. — каталоги и ресурсы, загруженные из этого источника.  Например, в приведенном выше рисунке полный путь `devtools-guide-chromium` к ресурсу `docs.microsoft.com/en-us/microsoft-edge/devtools-guide-chromium`  
    
Щелкните файл в области **страницы** , чтобы просмотреть содержимое в области " **Редактор** ".  Вы можете просматривать файлы любого типа.  Для изображений на экран выводится предварительный просмотр изображения.  

:::image type="complex" source="./media/sources-editor-pane.msft.png" alt-text="Область страницы" lightbox="./media/sources-editor-pane.msft.png":::
   Просмотр содержимого `a4d10f71.index-docs.js` в области " **Редактор** "  
:::image-end:::  

## Редактирование CSS и JavaScript  

Для изменения CSS и JavaScript используйте область " **Редактор** ".  DevTools обновляет страницу, чтобы выполнить новый код.  Например, если вы изменяете CSS-файл, добавив правило стиля ниже:

```css
.metadata.page-metadata {
    color: red;
}
```

Изменения вступают в силу немедленно.

:::image type="complex" source="./media/edit-css.msft.png" alt-text="Область страницы" lightbox="./media/edit-css.msft.png":::
   Редактирование CSS на панели « **Редактор** » для изменения цвета текста подзаголовка на красный  
:::image-end:::  

Изменения в CSS вступают в силу немедленно, сохранение не требуется.  Чтобы изменения в JavaScript вступили в силу, выберите `Control` + `S` \ (Windows, Linux \) или `Command` + `S` \ (macOS \).  DevTools не выполняет повторно сценарий, поэтому изменения, которые вступают в силу, выполняются только в рамках функций.  Например, на приведенном ниже рисунке обратите внимание на `console.log('A')` то, что не выполняется, в то время как `console.log('B')` оно делает.  Если после внесения изменений DevTools повторно запускает весь сценарий, он `A` будет записан в журнал на **консоли**.  

:::image type="complex" source="./media/edit-js.msft.png" alt-text="Область страницы" lightbox="./media/edit-js.msft.png":::
   Редактирование JavaScript в области " **Редактор** "  
:::image-end:::  

DevTools удаляет изменения стилей CSS и JavaScript при повторной загрузке страницы.  Перейдите к разделу [Настройка рабочей области](#set-up-a-workspace) , чтобы получить сведения о том, как сохранить изменения в файловой системе.  

## Создание, сохранение и запуск фрагментов  

Фрагменты — это сценарии, которые можно запускать на любой странице.  Предположим, что вы повторно вводите на **консоли**следующий код, чтобы вставить библиотеку jQuery на страницу, чтобы можно было запускать команды jQuery из **консоли**:  

```javascript
let script = document.createElement('script');
script.src = 'https://code.jquery.com/jquery-3.2.1.min.js';
script.crossOrigin = 'anonymous';
script.integrity = 'sha256-hwg4gsxgFZhOsEEamdOYGBf13FyQuiTwlAQgxVSNgt4=';
document.head.appendChild(script);
```  

Вместо этого вы можете сохранить этот код во **фрагменте** и выполнить его с помощью нескольких нажатий кнопки, когда вам понадобится.  DevTools сохранит **фрагмент** в файловой системе.  

:::image type="complex" source="./media/snippet.msft.png" alt-text="Область страницы" lightbox="./media/snippet.msft.png":::
   **Фрагмент кода** , который вставляет библиотеку jQuery на страницу  
:::image-end:::  

Чтобы выполнить **фрагмент кода**, выполните указанные ниже действия.

*   Откройте файл с помощью области **фрагментов** и выберите команду **выполнить** \ ( ![ кнопка выполнить \ ][ImageRunIcon] ).  
*   Откройте **[меню команд][DevtoolsGuideChromiumCommandMenuIndex]**, удалите `>` символ, введите `!` имя, введите его **и**нажмите кнопку `Enter` .  
    
Перейдите к разделу [выполнение фрагментов кода на любой странице][DevtoolsGuideChromiumJavascriptSnippets] , чтобы узнать больше.

## Отладка JavaScript  

Вместо того `console.log()` , чтобы использовать для определения того, где произошел сбой JavaScript, рекомендуется использовать инструменты отладки Microsoft Edge DevTools.  Общая идея состоит в том, чтобы установить точку останова, которая является умышленно остановленным местом в вашем коде, и пошаговое руководство по коду — по одной строке за раз.  По мере выполнения кода вы можете просматривать и изменять значения всех текущих заданных свойств и переменных, запускать JavaScript на **консоли**и т. д.

Перейдите к разделу [Начало отладки JavaScript][DevtoolsGuideChromiumJavascriptIndex] , чтобы ознакомиться с основами отладки в DevTools.

:::image type="complex" source="./media/debugging.msft.png" alt-text="Область страницы" lightbox="./media/debugging.msft.png":::
   Отладка JavaScript  
:::image-end:::  

## Настройка рабочей области  

По умолчанию при редактировании файла на панели « **источники** » эти изменения теряются при повторной загрузке страницы.  **Рабочие области** позволяют сохранить изменения, внесенные в DevTools, в файловую систему.  По сути, DevTools можно использовать в качестве редактора кода.

Перейдите к разделу [изменение файлов с помощью рабочих областей][DevtoolsGuideChromiumWorkspacesIndex] , чтобы приступить к работе.

## Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](./includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageRunIcon]: ./media/run-snippet-icon.msft.png  

<!-- links -->  

[DevtoolsGuideChromiumCommandMenuIndex]: ./command-menu/index.md "Выполнение команд с помощью командного меню Microsoft Edge DevTools"  
[DevtoolsGuideChromiumJavascriptIndex]: ./javascript/index.md "Начало работы с отладкой JavaScript в Microsoft Edge DevTools"  
[DevtoolsGuideChromiumJavascriptSnippets]: ./javascript/snippets.md "Выполнение фрагментов кода JavaScript на любой странице с Microsoft Edge DevTools"  
[DevtoolsGuideChromiumWorkspacesIndex]: ./workspaces/index.md "Редактирование файлов с помощью рабочих областей"  

[HtmlstandardOrigin]: https://html.spec.whatwg.org/multipage/origin.html#origin "Современный: HTML Standard"  

[W3CHtml4Frames]: https://w3.org/TR/html401/present/frames.html "Кадры | PNG"  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/sources) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
