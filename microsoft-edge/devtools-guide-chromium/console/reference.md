---
description: Полный справочник по всем функциям и поведениям, связанным с ИНТЕРФЕЙСом консоли в Microsoft Edge DevTools.
title: Справочник по консоли
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 27d521a4af528e95d06f58ac240f620a9c745044
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125260"
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

# Справочник по консоли  

Эта страница содержит ссылки на возможности, связанные с консолью Microsoft Edge DevTools.  Предполагается, что вы уже знакомы с использованием консоли для просмотра сообщений в журнале и запуска JavaScript.  В противном случае перейдите в раздел Начало работы [с JavaScript на консоли][DevToolsConsoleJavascript] и приступайте к [регистрации сообщений на консоли][DevToolsConsoleLog].  

Если вы ищете ссылку API на функции, такие как `console.log()` , [Справочник по API консоли][DevToolsConsoleApi].  Для справки по функциям `monitorEvents()` , например, перейдите на [ссылку API служебных программ для консоли][DevToolsConsoleUtilities].  

## Открытие консоли  

Вы можете открыть консоль как [панель](#open-the-console-panel) или как [вкладку в ящике](#open-the-console-tab-in-the-drawer).  

### Открытие панели консоли  

Выберите `Control` + `Shift` + `J` \ (Windows, Linux \) или `Command` + `Option` + `J` \ (macOS \).  

:::image type="complex" source="../media/console-hello-console.msft.png" alt-text="Панель консоли" lightbox="../media/console-hello-console.msft.png":::
   Панель **консоли**  
:::image-end:::  

Чтобы открыть панель консоли из [меню команд][DevToolsCommandMenu], начните вводить текст, `Console` а затем запустите команду **Показать консоль** с индикатором **панели** рядом с ним.  

:::image type="complex" source="../media/console-command-menu-show-console.msft.png" alt-text="Панель консоли" lightbox="../media/console-command-menu-show-console.msft.png":::
   Команда для отображения панели **консоли**  
:::image-end:::  

### Открытие вкладки "консоль" в ящике  

Выберите пункт `Escape` **Настройка DevTools** \ ( `...` \) и нажмите кнопку **Показать входной ящик консоли**.  

:::image type="complex" source="../media/console-elements-customize-control-devtools-show-console-drawer.msft.png" alt-text="Панель консоли" lightbox="../media/console-elements-customize-control-devtools-show-console-drawer.msft.png":::
   **Показать консольный ящик**  
:::image-end:::  

Ящик появляется в нижней части окна DevTools и открывается вкладка **консоли** .  

:::image type="complex" source="../media/console-elements-console-drawer-hello-world.msft.png" alt-text="Панель консоли" lightbox="../media/console-elements-console-drawer-hello-world.msft.png":::
   Вкладка « **консоль** » в **ящике**  
:::image-end:::  

Чтобы открыть вкладку консоль в [меню команд][DevToolsCommandMenu], начните вводить текст, `Console` а затем запустите команду **Показать консоль** с индикатором **ящика** рядом с ним.  

:::image type="complex" source="../media/console-command-menu-show-console.msft.png" alt-text="Панель консоли" lightbox="../media/console-command-menu-show-console.msft.png":::
   Команда для отображения вкладки " **консоль** " в **ящике**  
:::image-end:::  

### Открытие параметров консоли  

На панели " **Параметры консоли** ![ " нажмите значок ][ImageSettingsButtonIcon] "Параметры консоли".  

:::image type="complex" source="../media/console-settings-group-similar-empty.msft.png" alt-text="Панель консоли" lightbox="../media/console-settings-group-similar-empty.msft.png":::
   **Параметры консоли**  
:::image-end:::  

Ниже описаны ссылки для каждого параметра.  

*   [**Скрыть сеть**](#hide-network-messages)  
*   [**Сохранить журнал**](#persist-messages-across-page-loads)  
*   [**Только выделенный контекст**](#filter-out-messages-from-different-contexts)  
*   [**Одинаковая группа**](#disable-message-grouping)  
*   [**Запись в журнал XmlHttpRequest**](#log-xhr-and-fetch-requests)  
*   [**Упреждающая Оценка**](#disable-eager-evaluation)  
*   [**Автозаполнение из истории**](#disable-autocomplete-from-history)  
    
### Открытие боковой панели консоли  

Нажмите кнопку **Показать боковую панель консоли** \ ( ![ Показать боковую панель консоли ][ImageShowConsoleSidebarIcon] ), чтобы отобразить боковую панель, которая удобна для фильтрации.  

:::image type="complex" source="../media/console-sidebar-drawer-empty.msft.png" alt-text="Панель консоли" lightbox="../media/console-sidebar-drawer-empty.msft.png":::
   **Console (консоль** ) Врезка  
:::image-end:::  

## Просмотр сообщений  

В этом разделе описаны возможности, которые позволят изменить способ представления сообщений на консоли.  В этом пошаговом руководстве показано, как [Просмотреть сообщения][DevToolsConsoleViewMessages] .  

### Отключение группировки сообщений  

[Откройте параметры консоли](#open-console-settings) и отключите **группу, как** отключить поведение группировки сообщений по умолчанию для консоли.  Посмотрите, как [XHR журнал и](#log-xhr-and-fetch-requests) выводит запросы на получение примера.  

### Регистрация запросов XHR и FETCH  

[Откройте параметры консоли](#open-console-settings) и включите в **журнал записи XMLHttpRequest** , чтобы регистрировать все `XMLHttpRequest` и `Fetch` запросы на консоли по мере их появления.  

:::image type="complex" source="../media/console-xhr-fetch.msft.png" alt-text="Панель консоли" lightbox="../media/console-xhr-fetch.msft.png":::
   Журналы `XMLHttpRequest` и `Fetch` запросы  
:::image-end:::  
Верхнее сообщение на предыдущем рисунке показывает поведение группировки по умолчанию для **консоли**.  <!--  In the following figure, the same log is displayed after [disabling message grouping](#disable-message-grouping).  -->  

<!--  
> ##### Old Figure 9  
> How the logged `XMLHttpRequest` and `Fetch` requests look after ungrouping  
> :::image type="complex" source="../media/console-xhr-fetch-all.msft.png" alt-text="Панель консоли" lightbox="../media/console-xhr-fetch-all.msft.png":::
>    How the logged XMLHttpRequest and Fetch requests look after ungrouping  
> :::image-end:::  
-->  

<!--todo: add example for ungrouping console items  -->  

### Сохранение сообщений на загрузок страниц  

По умолчанию консоль очищается каждый раз, когда вы загружаете новую страницу.  Чтобы сохранить сообщения на нескольких страницах, [откройте параметры консоли](#open-console-settings) и установите флажок **сохранить журнал** .  

### Скрыть сетевые сообщения  

По умолчанию браузер записывает сетевые сообщения на **консоль**.  На приведенном ниже рисунке выбранное сообщение представляет код состояния HTTP `429` .  

:::image type="complex" source="../media/console-show-network.msft.png" alt-text="Панель консоли" lightbox="../media/console-show-network.msft.png":::
   `429`Сообщение на **консоли**  
:::image-end:::  
Чтобы скрыть сетевые сообщения, выполните указанные ниже действия.  

1.  [Откройте параметры консоли](#open-console-settings).  
1.  Включите флажок **Скрыть сеть** .  
    
## Фильтрация сообщений  

Есть несколько способов отфильтровать сообщения на консоли.  

### Фильтрация сообщений браузера  

[Откройте панель консоли](#open-the-console-sidebar) и выберите пункт **сообщения пользователя** , чтобы отображались только те сообщения, которые поставляются из JavaScript страницы.  

:::image type="complex" source="../media/console-sidebar-drawer-user-messages.msft.png" alt-text="Панель консоли" lightbox="../media/console-sidebar-drawer-user-messages.msft.png":::
   Просмотр сообщений пользователя  
:::image-end:::  

### Фильтрация по уровню ведения журнала  

DevTools назначает каждому `console.*` методу уровень серьезности.  Существует 4 уровня: `Verbose` ,, `Info` `Warning` , и `Error` .  Например, `console.log()` входит в `Info` группу, в то время как `console.error()` она находится в `Error` группе.  [Справочник по API консоли][DevToolsConsoleApi] описывает уровень важности каждого применимого метода.  Каждое сообщение, которое браузер записывает на консоль, также имеет уровень серьезности.  Вы можете скрыть любые ненужные сообщения.  Например, если вы заинтересованы в `Error` сообщениях, вы можете скрыть другие три группы.  

Щелкните раскрывающийся список **уровни журнала** , чтобы включить или отключить `Verbose` , `Info` `Warning` или `Error` сообщения.  

:::image type="complex" source="../media/console-log-level-default-levels.msft.png" alt-text="Панель консоли" lightbox="../media/console-log-level-default-levels.msft.png":::
   Раскрывающийся список **уровней журнала**  
:::image-end:::  

Вы также можете отфильтровать по уровню журнала, [открыв боковую панель консоли](#open-the-console-sidebar) и выбрав пункт **ошибки**, **предупреждения**, **сведения**или **подробный**.  

:::image type="complex" source="../media/console-sidebar-warnings.msft.png" alt-text="Панель консоли" lightbox="../media/console-sidebar-warnings.msft.png":::
   Использование боковой панели для просмотра предупреждений  
:::image-end:::  

### Фильтрация сообщений по URL-адресу  

Введите и `url:` URL-адрес, чтобы просматривать только те сообщения, которые были отправлены из этого URL-адреса.  После ввода `url:` DevTools появятся все нужные URL-адреса.  Домены также работают.  Например, если `https://example.com/a.js` `https://example.com/b.js` сообщения записываются в журнал, `url:https://example.com` вы можете сосредоточиться на сообщениях из этих 2 сценариев.  

:::image type="complex" source="../media/console-filter-text.msft.png" alt-text="Панель консоли" lightbox="../media/console-filter-text.msft.png":::
   Фильтр URL-адреса  
:::image-end:::  

Введите текст `-url:` , чтобы скрыть сообщения от этого URL-адреса.  Это называется фильтром отрицательных URL-адресов.  

:::image type="complex" source="../media/console-negative-filter-text.msft.png" alt-text="Панель консоли" lightbox="../media/console-negative-filter-text.msft.png":::
   Фильтр отрицательных URL-адресов, в котором скрываются все сообщения, соответствующие `https://b.wal.co` URL-адресу.
:::image-end:::  

Вы также можете показывать сообщения с одного URL-адреса, [открыв боковую панель консоли](#open-the-console-sidebar), развернув раздел " **пользовательские сообщения** ", а затем щелкнув URL-адрес сценария, содержащего сообщения, на которые нужно обратить внимание.  

:::image type="complex" source="../media/console-filter-text-specified.msft.png" alt-text="Панель консоли" lightbox="../media/console-filter-text-specified.msft.png":::
   Просмотр сообщений, которые были получены `wp-ad.min.js`  
:::image-end:::  

### Фильтрация сообщений в разных контекстах  

Предположим, что у вас есть реклама \ (AD) на вашей странице.  Рекламное объявление встраивается в приложение `<iframe>` и создает большое количество сообщений на консоли.  Так как объявление запущено в другом [контексте JavaScript](#select-javascript-context), один из способов скрыть сообщения — [открыть параметры консоли](#open-console-settings) и установить флажок **только выбранный контекст** .  

### Фильтрация сообщений, не соответствующих шаблону регулярного выражения  

Введите регулярное выражение, например `/[gm][ta][mi]/` в текстовое поле **Фильтр** , чтобы отфильтровать сообщения, которые не соответствуют этому шаблону.  DevTools проверяет, найден ли шаблон в тексте сообщения или сценарий, который привел к занесению в журнал сообщения.  

:::image type="complex" source="../media/console-filter-regex.msft.png" alt-text="Панель консоли" lightbox="../media/console-filter-regex.msft.png":::
   Фильтрация сообщений, не соответствующих `/[gm][ta][mi]/` выражению регулярного выражения  
:::image-end:::  

## Запуск JavaScript  

В этом разделе описаны возможности, связанные с выполнением JavaScript на консоли.  В этом пошаговом руководстве показано, как [запускать JavaScript][DevToolsConsoleOverviewJavascript] .  

### Повторное выполнение выражений из истории  

Нажмите клавишу `Up Arrow` для циклического просмотра истории выражений JavaScript, которые выполнялись на консоли раньше.  Выберите `Enter` , чтобы выполнить это выражение еще раз.  

### Просмотр значения выражения в режиме реального времени с помощью выражений с реальными данными  

Если вы обнаружите, что один и тот же выражение JavaScript будет вводиться повторно в консоль, возможно, вам будет проще создать **выражение в реальном времени**.  С помощью **выражений в реальном времени** вы вводите выражение один раз, а затем закрепите его в верхней части консоли.  Значение выражения обновляется почти в режиме реального времени.  Просмотрите [значения выражений JavaScript в Real-Time с помощью выражений в реальном времени][DevToolsConsoleLiveExpressions].  

### Отключение безотлагательной оценки  

По мере ввода выражений JavaScript в консоли **упреждающая Оценка** показывает предварительный просмотр возвращаемого значения для этого выражения.  [Откройте параметры консоли](#open-console-settings) и отключите флажок **упреждающая Оценка** , чтобы отключить предварительный просмотр возвращаемых значений.  

### Отключение автозаполнения из истории  

По мере ввода выражения в всплывающем окне для консоли отображаются выражения, которые были выполнены раньше.  Эти выражения добавляются в начале `>` символа.  [Откройте меню Параметры консоли](#open-console-settings) и отключите флажок **Автозаполнение из журнала** , чтобы отключить отображение выражений из истории.  

> [!NOTE]
> На приведенном ниже рисунке, `document.querySelector('a')` а `document.querySelector('img')` также выражения, которые были оценены ранее.  

:::image type="complex" source="../media/console-filter-text-autofilter-history.msft.png" alt-text="Панель консоли" lightbox="../media/console-filter-text-autofilter-history.msft.png":::
   В всплывающем окне "Автозаполнение" отображаются выражения из истории  
:::image-end:::  

### Выбор контекста JavaScript  

По умолчанию раскрывающийся список **контекстов JavaScript** имеет значение **Top**, которое представляет [контекст просмотра][MDNBrowsingContext] основного документа.  

:::image type="complex" source="../media/console-dom-level-top.msft.png" alt-text="Панель консоли" lightbox="../media/console-dom-level-top.msft.png":::
   Раскрывающийся список **контекстов JavaScript**  
:::image-end:::  

Предположим, что у вас есть реклама на странице, внедренная в `<iframe>` .  Вы хотите запустить JavaScript, чтобы настроить модель DOM рекламы.  Сначала необходимо выбрать контекст обзора рекламы из раскрывающегося списка **контекстов JavaScript** .  

:::image type="complex" source="../media/console-dom-level-multiple.msft.png" alt-text="Панель консоли" lightbox="../media/console-dom-level-multiple.msft.png":::
   Выбор другого контекста JavaScript  
:::image-end:::  

## Очистка консоли  

Чтобы очистить консоль, вы можете использовать любой из следующих рабочих процессов:  

*   Выберите **Очистить консоль** \ ( ![ Очистить консоль ][ImageClearConsoleIcon] ).  
*   Щелкните сообщение правой кнопкой мыши и выберите команду **Очистить консоль**.  
*   Введите `clear()` значение в поле консоль и нажмите кнопку `Enter` .  
*   Выполните на `console.clear()` веб-странице сценарий JavaScript.  
*   Выберите, `Control` + `L` пока консоль находится в фокусе.  
    
## Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageClearConsoleIcon]: ../media/clear-console-button-icon.msft.png  
[ImageSettingsButtonIcon]: ../media/settings-button-icon.msft.png  
[ImageShowConsoleSidebarIcon]: ../media/show-console-sidebar-icon.msft.png  

<!-- links -->  

[DevToolsCommandMenu]: ../command-menu/index.md "Выполнение команд с помощью командного меню Microsoft Edge DevTools | Документы Microsoft"  
[DevToolsConsoleViewMessages]: ./index.md#viewing-logged-messages "Просмотр сообщений с запротоколированием — обзор консоли | Документы Microsoft"  
[DevToolsConsoleApi]: ./api.md "Справочник по API консоли | Документы Microsoft"  
[DevToolsConsoleOverviewJavascript]: ./index.md#running-javascript "Выполнение JavaScript: обзор консоли | Документы Microsoft"  
[DevToolsConsoleJavascript]: ./javascript.md "Начало работы с JavaScript на консоли | Документы Microsoft"  
[DevToolsConsoleLiveExpressions]: ./live-expressions.md "Просмотр значений выражений JavaScript в режиме реального времени с помощью выражений в реальном масштабе | Документы Microsoft"  
[DevToolsConsoleLog]: ./log.md "Начало работы с сообщениями в журнале на консоли | Документы Microsoft"  
[DevToolsConsoleUtilities]: ./utilities.md "Справочник по API служебных программ для консоли | Документы Microsoft"  

[MDNBrowsingContext]: https://developer.mozilla.org/docs/Glossary/Browsing_context "Контекст просмотра | MDN"  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/console/reference) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
