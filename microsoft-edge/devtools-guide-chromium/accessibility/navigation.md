---
description: Руководство по навигации по Microsoft Edge DevTools с использованием специальных возможностей, таких как средства чтения с экрана.
title: Навигация в Microsoft Edge DevTools с помощью специальных возможностей
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: f4ec63a0d432925b7db99ce695db66dd61f8bcf1
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125295"
---
<!-- Copyright Rob Dodson 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->

# Навигация в Microsoft Edge DevTools с помощью специальных возможностей  

Следующая статья предназначена для того, чтобы помочь пользователям, которые в основном полагаются на специальные возможности, такие как средства чтения с экрана, доступ и использование [Microsoft Edge DevTools][MicrosoftEdgeDevtoolsMain].  [Microsoft Edge DevTools][MicrosoftEdgeDevtoolsMain] — это набор средств для веб-разработчиков, встроенных в браузер Microsoft Edge.  Если вы ищете функции DevTools, связанные с улучшением специальных возможностей веб-страницы, ознакомьтесь [со справочными материалами о специальных возможностях][DevtoolsAccessibilityReference].  

Доступность DevTools — это незавершенная работа.  На некоторых панелях и вкладках удобнее использовать специальные возможности, чем другие.  Это руководство поможет вам просмотреть все доступные и важные проблемы, которые могут возникнуть в ходе работы.  

## Обзор  

Перед началом работы он может использовать оценку DevTools пользовательского интерфейса.  DevTools делится на ряд панелей, упорядоченных в [ARIA TabList][W3CWaiAriaTablist].  

Например:  

*   С помощью панели **элементы** вы можете [просмотреть и изменить узлы DOM] [DevtoolsDomIndexNavigateDomTreeKeyboard] или [CSS][DevtoolsCssIndex].  
*   [Панель консоли][DevtoolsConsoleIndex] позволяет читать журналы JavaScript и объекты Live Edit.  

В области содержимого каждой панели находятся различные инструменты, часто называемые вкладками и областями в документации.  
Например, на панели **элементы** содержатся дополнительные вкладки для проверки прослушивателей событий, дерева специальных возможностей и многого другого.  Различие между вкладками и областями является несколько произвольным.  Единственная причина, по которой вы можете увидеть один термин, или другую — для обеспечения единообразия с помощью оставшейся части официального DevToolsной документации.  

## Сочетания клавиш  

[DevTools сочетаний клавиш] [DevtoolsShortcuts] является полезным cheatsheet.  Запусти закладку и обратись к ней по мере того, как вы изучите различные панели.  

## Открыть средства разработчика  

Чтобы приступить к работе, перейдите на [открыть Microsoft Edge DevTools] [DevtoolsOpen].  Открыть DevTools можно несколькими способами с помощью сочетаний клавиш или элементов меню.  

## Переход между панелями  

### Навигация с помощью клавиатуры  

*   После открытия DevTools выберите `Control` + `]` \ (Windows, Linux \) или `Command` + `]` \ (macOS \), чтобы сосредоточиться на следующей панели.  
*   Выберите `Control` + `[` \ (Windows, Linux \) или `Command` + `[` \ (macOS \), чтобы сосредоточиться на предыдущей панели.  
*   Кроме того, с помощью `Shift` + `Tab` клавиш со стрелками вы можете переместить фокус на [TabList в Aria][W3CWaiAriaTablist] на панели и использовать для изменения палитры.  

**Известные проблемы**  

*   Некоторые панели, например Console ( **консоль** ) и панели **производительности** , могут перемещать фокус в область содержимого Panel сразу после того, как каждая панель будет активирована.  Это может усложнить навигацию по клавишам со стрелками.  
*   Имя выбранной панели будет объявлено, но только после того, как оно прочитало содержимое, на которое ориентирован элемент, на панели.  Это может привести к простому пропуску.  

### Меню команд навигации  

Чтобы сфокусироваться на определенной панели, используйте [меню команд][DevtoolsCommandMenuIndex].  

1.  После открытия DevTools выберите `Control` + `Shift` + `P` \ (Windows, Linux \) или `Command` + `Shift` + `P` \ (macOS \), чтобы открыть **меню команд**.  
    **Меню команд** — поле со списком автозаполнения для поиска.  
1.  Введите имя панели, которую вы хотите открыть, а затем выберите `Down Arrow` нужный параметр с помощью клавиши на клавиатуре.  
1.  Выберите `Enter` , чтобы выполнить команду.  

Чтобы открыть панель " **элементы** ", выполните указанные ниже действия.  

1.  Открытие **меню команд**.  
1.  Введите `E` затем `L` .  Выбран параметр **> Показать элементы панели** .  
1.  Выберите `Enter` , чтобы запустить команду, которая открывает панель.  

Открытие панели таким образом направляет фокус на содержимое панели.  В случае панели **элементов** фокус переместится в **дерево DOM**.  

## Панель "элементы"  

### Проверка элемента на странице  

1.  Перейдите к элементу, который вы хотите проанализировать с помощью курсора в средстве чтения с экрана.  
1.  Имитировать щелчок правой кнопкой мыши на элементе с помощью мыши, чтобы открыть контекстное меню.  
1.  Выберите параметр **проверки** .  [Открывает панель элементы и фокусируется на элементе дерева DOM] [DevtoolsDomIndexViewDomNodes].  

**Дерево DOM** расрасполагается как [дерево ARIA][W3CWaiAriaTree].  Например, перейдите к разделу [Навигация по **дереву DOM** с помощью клавиатуры] [DevtoolsDomIndexNavigateDomTreeKeyboard].  

### Копирование кода для элемента в дереве DOM  

1.  При наведении фокуса на узел в **дереве DOM**наведите указатель мыши на узел и откройте контекстное меню (щелкните правой кнопкой мыши \).  
1.  Разверните элемент " **Копировать** ".  
1.  Нажмите кнопку **Копировать OuterHtml**.  

**Известные проблемы**  

*   **Копирование OuterHtml** часто не выделяет текущий узел, а вместо этого выделяет родительский узел.  Однако содержимое элемента по-прежнему должно находиться в копируемом outerHTML.  

### Изменение атрибутов элемента в дереве DOM  

*   С фокусом на узле в **дереве DOM**выберите, `Enter` чтобы сделать его редактируемым.  
*   Выберите `Tab` для перемещения между значениями атрибутов.  Когда вы услышите "место", в пустом текстовом вводе вы можете ввести новое значение атрибута.  
*   Выберите `Control` + `Enter` \ (Windows, Linux \) или `Command` + `Enter` \ (macOS \), чтобы сохранить изменения и прослушать все содержимое элемента.  

**Известные проблемы**  

*   При вводе текста в тексте не получается никаких отзывов.  Если вы производите опечатку и используете клавиши со стрелками для обзора ваших данных, вы также не получаете обратной связи.  Самый простой способ проверить работу — это внести изменения, а затем прослушивать весь элемент, который будет объявлен.  

### Редактирование HTML-кода элемента в дереве DOM  

*   С фокусом на узле в **дереве DOM**выберите, `Enter` чтобы сделать его редактируемым.  
*   Выберите `Tab` для перемещения между значениями атрибутов.  Например, когда вы услышите имя элемента, `h2` вы будете внутри текстового ввода и может изменить тип элемента.  
*   Выберите `Control` + `Enter` \ (Windows, Linux \) или `Command` + `Enter` \ (macOS \), чтобы сохранить изменения.  

Например, при вводе `h3` и выборе `Control` + `Enter` \ (Windows, Linux \) или `Command` + `Enter` \ (macOS \) можно изменить начальный и конечный теги `h3` элемента.  

## Вкладки панели элементов  

Панель " **элементы** " включает дополнительные вкладки для проверки элементов, таких как CSS, примененные к элементу или соответствующему месту в дереве специальных возможностей.  

*   Установив фокус на узел в **дереве DOM**, выберите пункт `Tab` пока не услышите, что выбрана область **стили** .  
*   Используйте `Right Arrow` для исследования другие доступные вкладки.  

**Дерево DOM** превращает элементы с `href` атрибутами в ссылки, поэтому для перехода в `Tab` область " **стили** " может потребоваться выбрать более одного раза.  

**Известные проблемы**  

Вкладки " **точки останова** " и " **свойства** " DOM не поддерживают специальные возможности клавиатуры.  

### Область "стили"  

В области " **стили** " найдите элементы управления для фильтрации стилей, переключения состояний элементов \ (например, [Active][MDNActive] и [: Focus][MDNFocus]), переключение классов и добавление новых классов.  Кроме того, существует мощное средство проверки стиля для изучения и изменения стилей, которые в данный момент применены к элементу, который находится в фокусе в **дереве DOM**.  

Ключевая концепция, указывающая на область **стилей** , заключается в том, что она показывает только стили для выбранного в данный момент узла в **дереве DOM**.  Например, предположим, что вы проверили стили `<header>` узла, и теперь вам нужно просмотреть стили `<footer>` узла.  Для этого сначала нужно выбрать `<footer>` узел в **дереве DOM**.  Возможно, вам будет удобнее использовать рабочий процесс [проверки](#inspect-an-element-on-the-page) для проверки узла, находящейся в общей области `footer` (например, ссылки в нижнем колонтитуле \), который специализируется на **дереве DOM**, а затем используйте клавиатуру для перехода на точный узел, в котором он заинтересован.  

#### Навигация в области "стили"  

Так как все инструменты стиля подключаются друг к другу, а не в область **стилей** , в этом случае имеет смысл стать экспертом в этом инструменте.  

*   В области **стили** выберите `Tab` переместить фокус внутрь и просмотрите содержимое.  
*   Выберите `Tab` , пока первый стиль не станет активным.  При использовании средства чтения с экрана первый стиль объявляется как `element.style {}` .  
*   Выберите `Down Arrow` для перемещения по списку стилей в определенном порядке.  Средство чтения с экрана уведомляет каждый стиль, начиная с имени CSS-файла, номер строки, в которой отображается стиль, и название стиля.  Например, `main.css:233 .card__img {}`.  
*   Выберите этот пункт `Enter` , чтобы подробно изучить стиль.  Фокус начинается с редактируемой версии имени стиля.  
*   Выберите `Tab` для перемещения между редактируемыми версиями каждого свойства CSS и соответствующими значениями.  В конце каждого блока Style — пустое Редактируемое текстовое поле, которое можно использовать для добавления дополнительных свойств CSS.  
*   Вы можете продолжить переход по `Tab` списку стилей или выбрать `Escape` выход из режима и вернуться к переходу с помощью клавиш со стрелками.  

Для дополнительных сочетаний клавиш перейдите в раздел [Справка: клавиатура в области стилей] [DevtoolsShortcutsStylesPaneKeyboard].  

**Известные проблемы**  

*   Если вы используете Редактируемое текстовое поле **Фильтр** , вы больше не сможете перемещаться по списку стилей.  

#### Переключить состояние элемента  

Чтобы переключить состояние элемента (например, или), `:active` `:focus` выполните указанные ниже действия.  

1.  Перейдите к области **стили** и выберите `Tab` , пока фокус не установлен на кнопке **Состояние переключаемого элемента** .  
1.  Выберите `Enter` , чтобы развернуть коллекцию состояний элементов.  Состояния элементов представляются в виде группы флажков.  
1.  Выбери, пока не будет выбрано `Tab` первое состояние, `:active` будет установлен фокус.  
1.  Выберите `Space` , чтобы включить его.  Если элемент, выбранный в дереве DOM `:active` , имеет стиль, он теперь применяется.  
1.  Удерживайте `Tab` , чтобы ознакомиться со всеми доступными состояниями.  

#### Добавление существующего класса  

Рядом с кнопкой " **включить состояние элемента** " находится кнопка " **классы элементов** ".  Чтобы переместить фокус на этот элемент, выберите его `Tab` и нажмите кнопку `Enter` .  Фокус перемещается в поле редактирования текста, помеченное **Добавить новый класс**.  

Кнопка « **классы элементов** » используется преимущественно для добавления в элемент существующих классов.  Например, если ваша таблица стилей содержала вспомогательный класс `.clearfix` , вы можете выбрать `.` внутри поля изменить текст, чтобы просмотреть список предложений и `Down Arrow` найти нужный `.clearfix` вариант.  Или введите имя класса, а затем нажмите кнопку `Enter` , чтобы применить его.  

#### Добавление нового правила стиля  

Рядом с кнопкой " **классы элементов** " находится **Новая кнопка "новое правило стиля** ".  Чтобы переместить фокус на этот элемент, выберите его `Tab` и нажмите кнопку `Enter` .  Фокус переместится в редактируемое текстовое поле в инспекторе стилей.  Начальным текстовым содержимым поля является имя тега элемента, выбранного в **дереве DOM**.  
Вы можете ввести имя нужного класса в это поле, а затем выбрать `Tab` для него назначение свойств CSS.  

### Вычисляемая вкладка  

В разделе **Вычисляемая** вкладка выберите `Tab` Перемещение фокуса внутрь и изучение содержимого.  В **вычисляемой** вкладке есть элементы управления для изучения того, какие свойства CSS фактически применяются к элементу в порядке их следования.  

<!--todo: add computed tab section when available  -->  

#### Ознакомьтесь со всеми вычисляемыми стилями  

Выберите, `Tab` пока не дойдете до коллекции вычисляемых стилей.  Они представлены в виде [дерева ARIA][W3CWaiAriaTree].  Разворачивание списка ListBox указывает, какие селекторы CSS применяют вычисляемый стиль.  Эти селекторы упорядочены по определенному принципу.  Средство чтения с экрана объявляет вычисленное значение, которое в настоящее время определяет элемент выбора CSS, имя файла таблицы стилей, содержащей селектор, и номер строки для элемента Selector.  

**Известные проблемы**  

*   Если вы используете текстовое поле " **Фильтр** ", вы больше не сможете проверять стили.  

### Вкладка "прослушиватели событий"  

На панели **элементы** можно проверить прослушиватели событий, примененные к элементу, с помощью вкладки **прослушиватели событий** .  В области **стили** щелкните элемент, `Right Arrow` чтобы перейти на вкладку **прослушиватели событий** .  

#### Анализ прослушивателей событий  

Прослушиватели событий представлены в виде [дерева ARIA][W3CWaiAriaTree].  Вы можете перемещаться с помощью клавиш со стрелками.  Средство чтения с экрана объявляет имя объекта DOM, к которому прикреплен прослушиватель событий, а также имя файла, в котором определен прослушиватель событий, и номер строки.  

### Область специальных возможностей  

В области **специальных возможностей** выберите `Tab` Перемещение фокуса внутрь и изучение содержимого.  В [области специальных возможностей][DevtoolsAccessibilityReference] есть элементы управления для изучения дерева специальных возможностей, атрибуты ARIA, примененные к элементу, и вычисляемые свойства специальных возможностей.  

#### Дерево специальных возможностей  

**Дерево специальных возможностей** представлено в виде [дерева ARIA][W3CWaiAriaTree] , где каждый `treeitem` из них соответствует элементу в DOM.  Дерево объявляет вычисляемую роль для выбранного узла.  Универсальные элементы, такие как `div` и `span` , объявляются как "GenericContainer" в дереве.  Используйте клавиши со стрелками для перемещения по дереву и просмотра связей между родительскими и дочерними таблицами.  

**Известные проблемы**  

*   Тип [дерева ARIA][W3CWaiAriaTree] , используемого областью **специальных возможностей** , может быть неправильно представлено в Microsoft Edge для средств чтения с экрана MacOS, таких как VoiceOver.  Подпишитесь на [вопрос Chromium #868480][ChromiumIssues868480] , чтобы получить информацию о ходе выполнения этой ошибки.  
*   Каждый раздел с **атрибутами ARIA** и **вычисляемые свойства** помечается как [дерево ARIA][W3CWaiAriaTree], но в настоящее время у каждого из них отсутствует управление фокусом, и это не повлияет на клавиатуру.  

## Панель «аудит»  

Для проверки распространенных проблем, связанных с производительностью, читаемостью, SEO и другими категориями, необходимо выполнить серию тестов на сайте с помощью панели **аудита** .  

### Настройка и запуск аудита  

1.  При первом открытии панели « **аудиты** » фокус помещается на кнопку « **запустить аудит** » в конце формы.  По умолчанию форма настроена для выполнения аудита для каждой категории с помощью эмуляции мобильного устройства в имитируемом соединении 3G.  
1.  Используйте `Shift` + `Tab` или вернитесь в режим просмотра, чтобы изменить параметры аудита.  
1.  Когда вы будете готовы запустить аудит, вернитесь к кнопке **запустить аудит** и выберите `Enter` .  
1.  Фокус перемещается в модальное окно с помощью кнопки **"Отмена"** , которая позволяет выйти из аудита.  Вы можете прослушать серию earconsов в процессе аудита, а также обновить страницу несколько появлений.  

**Известные проблемы**  

*   В настоящее время разные разделы формы конфигурации не помечаются `fieldset` элементом.  Чтобы узнать, какие элементы управления связаны с каждым разделом, удобнее перейти в режим просмотра.  
*   При завершении работы аудита отсутствует объявление earcon или Live Region.  Как правило, это займет около 30 секунд, после чего вы сможете перейти к результатам.  Использование режима обзора может быть самым простым способом достичь результатов.  

### Навигация по отчету аудита  

Отчет аудита организован в разделы, соответствующие каждой из категорий аудита.  Откроется отчет со списком оценок для каждой категории.  Эти баллы также являются ссылками, которые можно использовать для перехода к соответствующим разделам.  В каждом разделе находятся `details` элементы с расширениями, которые содержат сведения, связанные с прошедших аудитом или сбоем.  По умолчанию отображаются только ошибки аудита.  Каждый раздел завершается с помощью последнего `details` элемента, содержащего все переданные аудиты.  

Чтобы запустить новый аудит, используйте `Shift` + `Tab` для выхода из него отчет и поиска кнопки **выполнить аудит** .  

## Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsAccessibilityReference]: ./reference.md "Справка по специальным возможностям | Документы Microsoft"  
[DevtoolsAccessibilityReferencePane]: reference.md#the-accessibility-pane "Область "Специальные возможности": Справочник по специальным возможностям | Документы Microsoft"  
[MicrosoftEdgeDevtoolsMain]: ../../devtools-guide-chromium.md "Инструменты разработчика Microsoft EDGE (Chromium) | Документы Microsoft"  
[DevtoolsCommandMenuIndex]: ../command-menu/index.md "Выполнение команд с помощью командного меню Microsoft Edge DevTools | Документы Microsoft"  
[DevtoolsConsoleIndex]: ../console/index.md "Обзор консоли | Документы Microsoft"  
[DevtoolsCssIndex]: ../css/index.md "Начало просмотра и изменения CSS | Документы Microsoft"  
<!--[DevtoolsCssReferenceViewAppliedElement]: ../css/reference.md#view-only-the-css-that-is-actually-applied-to-an-element "CSS Reference - View only the CSS that is actually applied to an element | Microsoft Docs"  -->  
<!--[DevtoolsDomIndex]: ../dom/index.md "Get started with viewing and changing the DOM | Microsoft Docs"  -->  
[DevtoolsDomIndexViewDomNodes]: .. /DOM/index.md # View-DOM-Nodes: Просмотр узлов DOM — начало работы с просмотром и изменением модели DOM | Microsoft Docs»  
[DevtoolsDomIndexNavigateDomTreeKeyboard]: .. /DOM/index.md # Навигация--DOM-"Навигация по дереву DOM с помощью клавиатуры, начало работы с просмотром и изменением модели DOM | Microsoft Docs»  
[DevtoolsOpen]: .. /open.md "открыть Microsoft Edge DevTools | Microsoft Docs»  
[DevtoolsShortcuts]: .. /shortcuts.md "Microsoft Edge DevTools сочетания клавиш | Microsoft Docs»  
[DevtoolsShortcutsStylesPaneKeyboard]: .. /Shortcuts.md # Styles (стили) — область — сочетания клавиш в области стилей — Microsoft Edge DevTools сочетания клавиш | Microsoft Docs»  

[ChromiumIssues868480]: https://bugs.chromium.org/p/chromium/issues/detail?id=868480 "Вопрос 868480 – предоставление деревьев ARIA в виде таблиц в специальных возможностях Mac"  

[GithubEdgeDeveloperNewIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=%5BDevTools%20Docs%20Feedback%5D "Новая ошибка — MicrosoftDocs/Edge-разработчик | GitHub"  

[MDNActive]: https://developer.mozilla.org/docs/Web/CSS/:active ": активный | MDN"  
[MDNFocus]: https://developer.mozilla.org/docs/Web/CSS/:focus ": фокус | MDN"  

[MonorailChromiumIssues]: https://crbug.com "Проблемы — Chromium-Monorail"  

[W3CWaiAriaTablist]: https://www.w3.org/TR/wai-aria-1.1/#tablist "TabList (роль) — доступные богатые Интернет-приложения (помощью ОРИЕНТИРОВ WAI-ARIA) 1,1 | PNG"  
[W3CWaiAriaTree]: https://www.w3.org/TR/wai-aria-1.1/#tree "Tree (роль) — доступные богатые Интернет-приложения (помощью ОРИЕНТИРОВ WAI-ARIA) 1,1 | PNG"  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> [Здесь вы найдете](https://developers.google.com/web/tools/chrome-devtools/accessibility/navigation) исходную страницу и она была написана [Вадимом Dodson][RobDodson] \ (участники, Google веб-основы.).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[RobDodson]: https://developers.google.com/web/resources/contributors/robdodson  
