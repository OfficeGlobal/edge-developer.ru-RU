---
description: Инструкции по просмотру узлов, поиску узлов, изменению узлов, узлам ссылок в консоли, прерыванию изменений узла и т. д.
title: Приступая к просмотру и изменению модели DOM
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 8c0b544f2c4717a01d09c287f1167c81456a97f3
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125029"
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

# Приступая к просмотру и изменению модели DOM  

Заполните эти интерактивные учебники, чтобы ознакомиться с основными принципами просмотра и изменения модели DOM на странице с помощью Microsoft Edge DevTools.  

В этом руководстве предполагается, что вы знаете разницу между DOM и HTML.  Ознакомьтесь с приложением [: HTML и модель DOM](#appendix-html-versus-the-dom) для объяснения.  

## Примеры открытых DOM  

1.  Удерживайте клавишу `Control` \ (Windows, Linux \) или `Command` \ (macOS \) и выберите **примеры DOM** , которые нужно открыть на новой вкладке.  
    
    [Примеры DOM][GlitchDomExamples]  
    
## Просмотр узлов DOM  

На панели "элементы" в дереве DOM можно выполнить все действия, связанные с DOM, в DevTools.  

### Проверка узла  

Если вы заинтересованы в определенном узле DOM, **Проверьте** , как быстро открыть DevTools и проанализировать этот узел.  

1.  [Откройте примеры DOM](#open-dom-examples).  
1.  В разделе **Проверка узла**щелкните правой кнопкой мыши пункт **Michelangelo** и выберите команду **проверить**.  
    
    :::image type="complex" source="../media/dom-glitch-dom-examples-michelangelo-inspect.msft.png" alt-text="Проверка узла" lightbox="../media/dom-glitch-dom-examples-michelangelo-inspect.msft.png":::
       Проверка узла  
    :::image-end:::  
    
    1.  Откроется панель " **элементы** " DevTools.  `<li>Michelangelo</li>` в **дереве DOM**выделено.  
        
        :::image type="complex" source="../media/dom-glitch-dom-examples-michelangelo-elements-highlighted.msft.png" alt-text="Проверка узла" lightbox="../media/dom-glitch-dom-examples-michelangelo-elements-highlighted.msft.png":::
           Выделение `Michelangelo` узла  
        :::image-end:::  
        
        1.  Щелкните значок **проверить** \ ( ![ проверить ][ImageInspectIcon] \) в левом верхнем углу DevTools.  
            
            :::image type="complex" source="../media/dom-elements-highlighted-select-element-page-inspect.msft.png" alt-text="Проверка узла" lightbox="../media/dom-elements-highlighted-select-element-page-inspect.msft.png":::
               Значок **проверки**  
            :::image-end:::  
            
1.  В разделе **Проверка узла**щелкните текст в **Токио** .  Теперь `<li>Tokyo</li>` выделена в дереве DOM.  

Проверка узла также является первым шагом в направлении просмотра и изменения стилей узла.  Ознакомьтесь [со статьей начало работы с помощью просмотра и изменения CSS][DevToolsCssGetStarted].  

### Навигация по дереву DOM с помощью клавиатуры  

После того как вы выбрали узел в дереве DOM, вы можете перемещаться по дереву DOM с помощью клавиатуры.  

1.  [Откройте примеры DOM](#open-dom-examples).  
1.  В разделе **Навигация по дереву DOM с помощью клавиатуры**щелкните правой кнопкой мыши **Ringo** и выберите команду **проверить**.  `<li>Ringo</li>` выбрано в дереве DOM.  
    
    :::image type="complex" source="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ringo.msft.png" alt-text="Проверка узла" lightbox="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ringo.msft.png":::
       Проверка `Ringo` узла  
    :::image-end:::  
    
    1.  Нажимайте клавишу `Up` стрелка 2.  `<ul>` .  
        
        :::image type="complex" source="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ul.msft.png" alt-text="Проверка узла" lightbox="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ul.msft.png":::
           Проверка `ul` узла  
        :::image-end:::  
        
    1.  Нажмите клавишу `Left` со стрелкой.  `<ul>`Список сворачивается.  
    1.  Снова нажмите клавишу `Left` со стрелкой.  Выбран родительский элемент `<ul>` узла.  В этом случае это `<div>` идентификатор `navigate-the-dom-tree-with-a-keyboard-1` .  
    1.  Нажимайте клавишу `Down` стрелка 2, чтобы повторно выбрать `<ul>` только что свернутый список.  Это должно выглядеть следующим образом. `<ul>... </ul>`  
    1.  Нажмите клавишу `Right` со стрелкой.  Список будет развернут.  

### Прокрутка представления  

При просмотре дерева DOM может возникнуть интерес к узлу DOM, который в данный момент не находится в окне просмотра.  Например, предположим, что вы прокручивается в нижней части страницы, и вы заинтересованы в `<h1>` узле в верхней части страницы.  **Прокрутка представления** позволяет быстро изменить расположение окна просмотра, чтобы вы могли видеть этот узел.  

1.  [Откройте примеры DOM](#open-dom-examples).  
1.  В разделе **прокрутка представления**щелкните правой кнопкой мыши **Magritte** и выберите команду **проверить**.  
1.  Прокрутите страницу "примеры DOM" до конца.  
1.  Этот `<li>Magritte</li>` узел по-прежнему должен быть выбран в дереве DOM.  В противном случае вернитесь на [страницу Просмотр](#scroll-into-view) и начните заново.  
1.  Щелкните правой кнопкой мыши `<li>Magritte</li>` узел и выберите **прокрутка в представлении**.  Ваше окно просмотра будет прокручено, чтобы вы могли видеть узел **Magritte** .  Если вы не видите параметр **прокрутить в представлении** , вы можете просмотреть [Приложение: отсутствующие параметры](#appendix-missing-options) .
    
    :::image type="complex" source="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png" alt-text="Проверка узла" lightbox="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png":::
       **Прокрутка представления**  
    :::image-end:::  

### Поиск узлов  

Вы можете выполнить поиск по дереву DOM по строке, селектору CSS или селектору XPath.  

1.  Сосредоточьте указатель мыши на панели " **элементы** ".  
1.  Выберите `Control` + `F` \ (Windows, Linux \) или `Command` + `F` \ (macOS \).  Строка поиска откроется в нижней части дерева DOM.  
1.  Введите `The Moon is a Harsh Mistress`.  Последнее предложение выделено в дереве DOM.  
    
    :::image type="complex" source="../media/dom-elements-highlighted-search-nodes-highlight.msft.png" alt-text="Проверка узла" lightbox="../media/dom-elements-highlighted-search-nodes-highlight.msft.png":::
       Выделение запроса в строке поиска  
    :::image-end:::  
    
Как упоминалось выше, строка поиска также поддерживает селекторы CSS и XPath.  

## Редактирование модели DOM  

Вы можете изменить модель DOM на лету и посмотреть, как эти изменения влияют на страницу.  

### Редактирование контента  

Чтобы изменить содержимое узла, дважды щелкните его содержимое в дереве DOM.  

1.  [Откройте примеры DOM](#open-dom-examples).  
1.  В разделе **изменить содержимое**щелкните правой кнопкой мыши **Мишель** и выберите команду **проверить**.  
    1.  В дереве DOM дважды щелкните `Michelle` .  Другими словами, дважды щелкните текст между `<li>` and `</li>` .  Текст будет выделено, чтобы показать, что он выделен.  
        
        :::image type="complex" source="../media/dom-elements-highlighted-edit-content.msft.png" alt-text="Проверка узла" lightbox="../media/dom-elements-highlighted-edit-content.msft.png":::
           Редактирование текста  
        :::image-end:::  
        
    1.  Удалить `Michelle` , введите `Leela` и выберите `Enter` для подтверждения изменения.  Текст в DOM изменится с **Мишель** на **Leela**.  

### Изменение атрибутов  

Чтобы изменить атрибуты, дважды щелкните имя или значение атрибута.  Следуйте инструкциям, чтобы научиться добавлять атрибуты на узел.  

1.  [Откройте примеры DOM](#open-dom-examples).  
1.  В разделе **изменить атрибуты**щелкните правой кнопкой мыши **Говард** и выберите команду **проверить**.  
1.  Дважды щелкните `<li>` .  Текст будет выделено, чтобы показать, что выбран узел.  
    
    :::image type="complex" source="../media/dom-elements-highlighted-edit-attributes-highlighted.msft.png" alt-text="Проверка узла" lightbox="../media/dom-elements-highlighted-edit-attributes-highlighted.msft.png":::
       Изменение узла  
    :::image-end:::  
    
1.  Нажимайте клавишу `Right` со стрелкой, добавьте пробел, введите текст `style="background-color:gold"` и нажмите кнопку `Enter` .  Цвет фона узла изменится на Золотой.  
    
    :::image type="complex" source="../media/dom-elements-highlighted-edit-attributes-inline-css.msft.png" alt-text="Проверка узла" lightbox="../media/dom-elements-highlighted-edit-attributes-inline-css.msft.png":::
       Добавление `style` атрибута на узел  
    :::image-end:::  
    
### Изменить тип узла  

Чтобы изменить тип узла, дважды щелкните его, а затем введите новый тип.  

1.  [Откройте примеры DOM](#open-dom-examples).  
1.  В разделе **изменить тип узла**щелкните правой кнопкой мыши пункт **Hank** и выберите команду **проверить**.  
    1.  Дважды щелкните `<li>` .  Текст `li` будет выделен.  
    1.  "Удалить" `li` , введите текст `button` и нажмите кнопку `Enter` .  `<li>`Узел изменится на `<button>` узел.  
        
        :::image type="complex" source="../media/dom-elements-highlighted-edit-node-type-button.msft.png" alt-text="Проверка узла" lightbox="../media/dom-elements-highlighted-edit-node-type-button.msft.png":::
           Измените тип узла на `button`  
        :::image-end:::  
        
### Изменение порядка узлов DOM  

Перетащите узлы, чтобы изменить их порядок.  

1.  [Откройте примеры DOM](#open-dom-examples).  
1.  В разделе **изменение порядка узлов DOM**щелкните **Elvis Presley** правой кнопкой мыши и выберите команду **проверить**.  
    
    > [!NOTE]
    > Это последний элемент в списке.  
    
    1.  В дереве DOM перетащите указатель `<li>Elvis Presley</li>` в верхнюю часть списка.  
        
        :::image type="complex" source="../media/dom-elements-reorder-dom-nodes.msft.png" alt-text="Проверка узла" lightbox="../media/dom-elements-reorder-dom-nodes.msft.png":::
           Перетащите узел в верхнюю часть списка.  
        :::image-end:::  
        
### Принудительное состояние  

Вы можете принудительно оставлять узлы в состоянии, в том числе,,, `:active` `:hover` `:focus` `:visited` и `:focus-within` .  

1.  [Откройте примеры DOM](#open-dom-examples).  
1.  В разделе **принудительное состояние**наведите указатель мыши на **Lord летит**.  Цвет фона становится оранжевым.  
    1.  Щелкните правой кнопкой мыши **Lord в полете** и выберите команду **проверить**.  
    1.  Щелкните правой кнопкой мыши `<li class="demo--hover">The Lord of the Flies</li>` и выберите **принудительное состояние**  >  **: наведение**.  Если вы не видите этот параметр, просмотрите [Приложение: отсутствующие параметры](#appendix-missing-options) .  Цвет фона остается оранжевым, несмотря на то что вы не наводите указатель мыши на узел.  

### Скрытие узла  

Выберите `H` , чтобы скрыть узел.  

1.  [Откройте примеры DOM](#open-dom-examples).  
1.  В разделе **скрыть узел**щелкните правой кнопкой мыши **звезду** и выберите команду **проверить**.  
    1.  Нажмите клавишу `H` .  Узел скрыт.  
        
        :::image type="complex" source="../media/dom-elements-highlighted-hide-a-node.msft.png" alt-text="Проверка узла" lightbox="../media/dom-elements-highlighted-hide-a-node.msft.png":::
           Как выглядит узел в дереве DOM после его скрытия  
        :::image-end:::  
        
    1.  Снова нажмите клавишу `H` .  Узел снова появится.  

### Удаление узла  

Выберите `Delete` , чтобы удалить узел.  

1.  [Откройте примеры DOM](#open-dom-examples).  
1.  В разделе **Удаление узла**щелкните правой кнопкой мыши пункт **Foundation** и выберите команду **проверить**.  
    1.  Нажмите клавишу `Delete` .  Узел удален.  
    1.  Выберите `Control` + `Z` \ (Windows, Linux \) или `Command` + `Z` \ (macOS \).  Последнее действие отменено, и узел появится снова.  

## Узлы Access на консоли  

DevTools предоставляет несколько сочетаний клавиш для доступа к узлам DOM из консоли или получения ссылок JavaScript на каждую из них.  

### Ссылка на узел, выбранный в настоящее время с помощью $0  

Когда вы просматриваете узел, `== $0` текст рядом с узлом означает, что вы можете добавить ссылку на этот узел в консоль с переменной `$0` .  

1.  [Откройте примеры DOM](#open-dom-examples).  
1.  В разделе **ссылка на выбранный узел в $0**щелкните правой кнопкой мыши **в левой части экрана затемнения** и выберите команду **проверить**.  
    1.  Нажмите клавишу, `Escape` чтобы открыть консольный ящик.  
    1.  Введите текст и нажмите клавишу ВВОД `$0` `Enter` .  Результат выражения показывает, что выражение `$0` имеет значение `<li>The Left Hand of Darkness</li>` .  
        
        :::image type="complex" source="../media/dom-elements-highlighted-reference-currently-selected-node-console-1.msft.png" alt-text="Проверка узла" lightbox="../media/dom-elements-highlighted-reference-currently-selected-node-console-1.msft.png":::
            Результат первого `$0` выражения в **консоли**  
        :::image-end:::  
        
    1.  Наведите указатель мыши на результат.  Узел выделится в окне просмотра.  
    1.  Щелкните `<li>Dune</li>` дерево DOM, введите `$0` консоль еще раз, а затем нажмите `Enter` еще раз.  Теперь `$0` оценивается `<li>Dune</li>` .  
        
        :::image type="complex" source="../media/dom-elements-highlighted-reference-currently-selected-node-console-2.msft.png" alt-text="Проверка узла" lightbox="../media/dom-elements-highlighted-reference-currently-selected-node-console-2.msft.png":::
           Результат второго `$0` выражения в **консоли**  
        :::image-end:::  
        
### Сохранить как глобальную переменную  

Если необходимо повторно сослаться на узел, сохраните его как глобальную переменную.  

1.  [Откройте примеры DOM](#open-dom-examples).  
1.  В разделе **Сохранить как глобальную переменную**щелкните правой кнопкой мыши **большую** временную подменю и выберите команду **проверить**.  
    1.  Щелкните правой кнопкой мыши `<li>The Big Sleep</li>` дерево DOM и выберите **Сохранить как глобальную переменную**.  Если вы не видите этот параметр, просмотрите [Приложение: отсутствующие параметры](#appendix-missing-options) .  
    1.  Введите текст `temp1` в окне консоли и нажмите кнопку `Enter` .  Результат выражения показывает, что переменная является узлом.  
        
        :::image type="complex" source="../media/dom-elements-highlighted-store-global-variable-console-temp1.msft.png" alt-text="Проверка узла" lightbox="../media/dom-elements-highlighted-store-global-variable-console-temp1.msft.png":::
           Результат `temp1` выражения  
        :::image-end:::  
        
### Скопировать путь к JS  

Скопируйте путь JavaScript на узел, если вам нужно сослаться на него в автоматическом тесте.  

1.  [Откройте примеры DOM](#open-dom-examples).  
1.  В разделе **скопировать путь к каталогу**щелкните правой кнопкой мыши **братьев Karamazov** и выберите команду **проверить**.  
    1.  Щелкните правой кнопкой мыши `<li>The Brothers Karamazov</li>` дерево DOM и выберите команду **Копировать**  >  **путь к каталогу**.  `document.querySelector()`Выражение, которое разрешается в узел, копируется в буфер обмена.  
    1.  Выберите `Control` + `V` \ (Windows, Linux \) или `Command` + `V` \ (macOS \), чтобы вставить выражение в консоль.  
    1.  Выберите `Enter` , чтобы вычислить выражение.
        
        :::image type="complex" source="../media/dom-elements-highlighted-copy-js-path-console-query-selector.msft.png" alt-text="Проверка узла" lightbox="../media/dom-elements-highlighted-copy-js-path-console-query-selector.msft.png":::
           Результат выражения **Copy JS Path**  
        :::image-end:::  
        
## Прерывание изменений DOM  

DevTools позволяет приостановить JavaScript на странице, когда JavaScript изменит модель DOM.  

### Прерывание изменений атрибутов  

Используйте точки останова по изменению атрибутов, если требуется приостановить JavaScript, который приводит к изменению любого атрибута узла.  

1.  [Откройте примеры DOM](#open-dom-examples).  
1.  В разделе **прервать при изменении атрибутов**щелкните правой кнопкой мыши **Sauerkraut** и выберите команду **проверить**.  
    1.  В дереве DOM щелкните правой кнопкой мыши `<li id="target">Sauerkraut</li>` и выберите команду **прервать при**  >  **изменении атрибутов**.  Если вы не видите этот параметр, ознакомьтесь со статьей [Приложение: отсутствующие параметры](#appendix-missing-options) .
        
        :::image type="complex" source="../media/dom-elements-highlighted-break-attribute-modifications-break-on-attribute-modifications.msft.png" alt-text="Проверка узла" lightbox="../media/dom-elements-highlighted-break-attribute-modifications-break-on-attribute-modifications.msft.png":::
           **Прерывание изменений атрибутов**  
        :::image-end:::  
        
    1.  На следующем этапе вы будете получать инструкции по нажатию кнопки, которая приостанавливает код страницы.  После того как страница приостановлена, прокрутка страницы больше недоступна.  **Resume Script** ![ ][ImageResumeScriptIcon] Чтобы снова выполнить прокрутку страницы, необходимо выбрать сценарий возобновления \ (возобновить сценарий \).
        
        :::image type="complex" source="../media/dom-break-attribute-modifications-sources-paused-on.msft.png" alt-text="Проверка узла" lightbox="../media/dom-break-attribute-modifications-sources-paused-on.msft.png":::
           Как возобновить выполнение сценария  
        :::image-end:::  
        
    1.  Нажмите кнопку " **настроить фон** ".  Таким образом, `style` для атрибута узла будет задано значение `background-color:thistle` .  DevTools приостанавливает страницу и выделяет код, который привел к изменению атрибута.  
    1.  Выберите команду **возобновить сценарий** \ ( ![ возобновить сценарий ][ImageResumeScriptIcon] \), как упоминалось ранее.  
    
### Прерывание при удалении узла  

Если вы хотите приостановить работу при удалении определенного узла, используйте точки останова удаления узла.  

1.  [Откройте примеры DOM](#open-dom-examples).  
1.  В разделе **прервать удаление узла**щелкните правой кнопкой мыши **Neuromancer** и выберите команду **проверить**.  
    1.  В дереве DOM щелкните правой кнопкой мыши `<li id="target">Neuromancer</li>` и выберите команду **прервать при**  >  **удалении узла**.  Если вы не видите этот параметр, ознакомьтесь со статьей [Приложение: отсутствующие параметры](#appendix-missing-options) .  
    1.  Нажмите кнопку " **Удалить** ".  DevTools приостанавливает страницу и выделяет код, вызвавший удаление узла.  
    1.  Выберите команду **возобновить сценарий** \ ( ![ возобновить сценарий ][ImageResumeScriptIcon] \).  
    
### Прерывание при изменении поддерева  

После того как вы добавите на узел точку останова изменения поддерева, DevTools приостанавливает страницу при добавлении или удалении любого потомка узла.  

1.  [Откройте примеры DOM](#open-dom-examples).  
1.  В разделе **прервать при изменении поддерева**щелкните правой кнопкой **мыши и выберите команду** **проверить**.  
    1.  В дереве DOM щелкните правой кнопкой мыши расположенный `<ul id="target">` выше узел `<li>A Fire Upon the Deep</li>` и выберите команду **прервать при**  >  **изменении поддерева**.  Если вы не видите этот параметр, ознакомьтесь со статьей [Приложение: отсутствующие параметры](#appendix-missing-options) .  
    1.  Нажмите кнопку **Добавить дочерний элемент**.  Код приостанавливается, так как `<li>` узел был добавлен в список.  
    1.  Выберите команду **возобновить сценарий** \ ( ![ возобновить сценарий ][ImageResumeScriptIcon] \).  
    
## Дальнейшие действия  

, Которая охватывает большую часть функций, связанных с DOM, в DevTools.  Вы можете найти остальные элементы, щелкнув правой кнопкой мыши узлы в дереве DOM и экспериментируя с другими параметрами, которые не были рассмотрены в этом учебнике.  Вы также можете просмотреть [сочетания клавиш для панели элементов][DevToolsShortcutsElements].  

Ознакомьтесь с [домашней страницей Microsoft Edge DevTools][MicrosoftEdgeDevTools] , чтобы найти все, что вы можете делать с DevTools.  

<!--See [Community](../index#community) if you want to contact the DevTools team or get help from the DevTools community.  -->  

## Приложение: HTML и модель DOM  

В следующем разделе показано, как быстро рассказано о различиях между HTML и DOM.  

:::row:::
   :::column span="":::
      При использовании веб-браузера для запроса страницы сервер возвращает HTML-код, как в следующем фрагменте кода.  

      ```html
      <!doctype html>
      <html>
          <head>
              <title>Hello, world!</title>
          </head>
          <body>
              <h1>Hello, world!</h1>
              <p>This is a hypertext document on the World Wide Web.</p>
              <script src="/script.js" async></script>
          </body>
      </html>
      ```  
   :::column-end:::
   :::column span="":::
      Браузер анализирует HTML и создает дерево объектов, как в приведенном ниже списке.  
      
      ```dom
      html
          head
              title
          body
              h1
              p
              script
      ```  
   :::column-end:::
:::row-end:::  

Это дерево объектов или узлов, представляющее содержимое страницы, называется DOM.  

:::row:::
   :::column span="":::
      Теперь оно выглядит так же, как HTML, но предположим, что сценарий, указанный в нижней части HTML, выполняет следующий фрагмент кода.  
      
      ```javascript
      const h1 = document.querySelector('h1');
      h1.parentElement.removeChild(h1);
      const p = document.createElement('p');
      p.textContent = 'Wildcard!';
      document.body.appendChild(p);
      ```  
   :::column-end:::
   :::column span="":::
      Этот код удаляет `h1` узел и добавляет еще один `p` узел в модель DOM.  Теперь в качестве полного DOM появится следующий список.  
      
      ```dom
      html
          head
              title
          body
              p
              script
              p
      ```  
   :::column-end:::
:::row-end:::  

HTML-код страницы теперь отличается от модели DOM.  Другими словами, HTML представляет начальное содержимое страницы, а модель DOM — текущее содержимое страницы.  Когда JavaScript добавляет, удаляет или редактирует узлы, модель DOM становится отличной от HTML.  

Дополнительные сведения можно найти в разделе [Введение в модель DOM][MDNIntroductionToDOM] .  

<!--
## Appendix: Scroll into view  

This is a continuation of the [Scroll into view](#scroll-into-view) section.  Follow the instructions below to complete the section.  

1.  The `<li>Magritte</li>` node should still be selected in your DOM Tree.  If not, go back to [Scroll into view](#scroll-into-view) and start over.  
1.  Right-click the `<li>Magritte</li>` node and choose **Scroll into view**.  Your viewport scrolls back up so that you may see the **Magritte** node.  See [Appendix: Missing options](#appendix-missing-options) if you are not able to see the **Scroll into view** option.
    
    :::image type="complex" source="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png" alt-text="Проверка узла" lightbox="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png":::
       Scroll into view  
    :::image-end:::  
    -->  

## Приложение: отсутствующие параметры  

Многие инструкции, описанные в этом руководстве, помогут вам щелкнуть правой кнопкой мыши узел в дереве DOM и выбрать нужный вариант в контекстном меню.  Если указанный параметр не отображается в контекстном меню, попробуйте щелкнуть правой кнопкой мыши за пределами текста узла.  

:::image type="complex" source="../media/dom-elements-highlighted-right-click-right-side.msft.png" alt-text="Проверка узла" lightbox="../media/dom-elements-highlighted-right-click-right-side.msft.png":::
   Выбор варианта, если вы не видите все параметры  
:::image-end:::  

## Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageInspectIcon]: ../media/inspect-icon.msft.png  
[ImageResumeScriptIcon]: ../media/resume-script-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Microsoft Edge \ (Chromium \) Инструменты разработчика | Документы Microsoft"  
[DevToolsCssGetStarted]: ../css/index.md "Начало просмотра и изменения CSS | Документы Microsoft"  
[DevToolsShortcutsElements]: ../shortcuts.md#elements-panel-keyboard-shortcuts "Сочетания клавиш для панели элементов — сочетания клавиш в Microsoft Edge DevTools | Документы Microsoft"  

[GlitchDomExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/dom "Пример Microsoft EDGE (Chromium) DevTools DOM | Цепь"

[MDNIntroductionToDOM]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Общие сведения об DOM | MDN"  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/dom/index) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
