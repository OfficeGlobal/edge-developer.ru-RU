---
description: Ссылка на удобные команды, доступные в консоли Microsoft Edge DevTools.
title: Справочник по API для консольных программ
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 2882d980e6da45072cab4b028ceb1838a9078064
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993109"
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

# Справочник по API для консольных программ  

API консоли содержат набор удобных команд для выполнения распространенных задач: выбор и анализ элементов DOM, отображение данных в удобочитаемом формате, остановка и запуск профилировщика, а также наблюдение за событиями DOM.  

> [!WARNING]
> Следующие команды работают только на консоли Microsoft Edge DevTools.  Команды не работают при запуске из ваших сценариев.  

Ищете `console.log()` `console.error()` и другие `console.*` методы?  См.: [Справочник по API для консольных интерфейсов][DevToolsConsoleApi].  

## Последнее вычисленное выражение  

```console
$_
```  

Возвращает значение последнего вычисленного выражения.  

На приведенном ниже рисунке вычисляется простое выражение \ ( `2 + 2` \).  `$_`Затем вычисляется свойство, которое содержит одно и то же значение.  

:::image type="complex" source="../media/console-arithmatic.msft.png" alt-text="$ _ — это последнее вычисленное выражение" lightbox="../media/console-arithmatic.msft.png":::
   Рисунок 1:  `$_` это последнее вычисленное выражение.  
:::image-end:::  

На приведенном ниже рисунке вычисленное выражение изначально включает массив имен.  Вычисление `$_.length` для определения длины массива, значение, хранящееся в `$_` изменениях, становится последним вычисленным выражением `4` .  

:::image type="complex" source="../media/console-array-length.msft.png" alt-text="$ _ — это последнее вычисленное выражение" lightbox="../media/console-array-length.msft.png":::
   Рисунок 2:  `$_` изменения при вычислении новых команд  
:::image-end:::  

## Недавно выбранный элемент или объект JavaScript  

```console
$0
```  

Возвращает последний выбранный элемент или объект JavaScript.  `$1` Возвращает второй, последний выбранный элемент и т. д.  Команды,,, и, Кроме того, `$0` `$1` работают в `$2` `$3` `$4` виде исторических ссылок на последние пять элементов DOM, проверенных на панели **элементов** , или последние пять объектов кучи JavaScript, выбранных на панели " **память** ".  

:::row:::
   :::column span="1":::
      ```console
      $0
      ```  
   :::column-end:::
   :::column span="1":::
      ```console
      $1
      ```  
   :::column-end:::
   :::column span="1":::
      ```console
      $2
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      ```console
      $3
      ```  
   :::column-end:::
   :::column span="1":::
      ```console
      $4
      ```  
   :::column-end:::
   :::column span="1":::
   :::column-end:::
:::row-end:::  

На рисунке ниже показан элемент, `img` выбранный на панели **элементы** .  В ящике **консоли** `$0` вычисляется и отображается один и тот же элемент.  

:::image type="complex" source="../media/console-image-highlighted-$0.msft.png" alt-text="$ _ — это последнее вычисленное выражение" lightbox="../media/console-image-highlighted-$0.msft.png":::
   Рис. 3: `$0`  
:::image-end:::  

На приведенном ниже рисунке показано, как на изображении показан другой элемент, выбранный на той же странице.  `$0`Теперь он ссылается на только что выбранный элемент, то `$1` есть возвращает ранее выбранное.  

:::image type="complex" source="../media/console-image-highlighted-$1.msft.png" alt-text="$ _ — это последнее вычисленное выражение" lightbox="../media/console-image-highlighted-$1.msft.png":::
   На рисунке 4: `$1`  
:::image-end:::  

## Область выбора запроса  

```console
$(selector, [startNode])
```  

Возвращает ссылку на первый элемент DOM с указанным селектором CSS.  Этот метод является псевдонимом метода [Document. querySelector ()][MDNDocumentQuerySelector] .  

На приведенном ниже рисунке возвращается ссылка на первый `<img>` элемент в документе.  

:::image type="complex" source="../media/console-element-selector-image.msft.png" alt-text="$ _ — это последнее вычисленное выражение" lightbox="../media/console-element-selector-image.msft.png":::
   На рисунке 5: `$('img')`  
:::image-end:::  

Наведите указатель мыши на полученный результат, откройте контекстное меню, а затем выберите пункт **Показать на панели элементов** , чтобы найти его в модели DOM, или **прокрутите** страницу, чтобы отобразить ее на странице.  

На приведенном ниже рисунке возвращается ссылка на элемент, выбранный в данный момент, и отображается свойство src.  

:::image type="complex" source="../media/console-element-selector-image-source.msft.png" alt-text="$ _ — это последнее вычисленное выражение" lightbox="../media/console-element-selector-image-source.msft.png":::
   На рисунке 6: `$('img').src`  
:::image-end:::  

Этот метод также поддерживает второй параметр, startNode, задающий "элемент" или узел, из которого следует искать элементы.  Значением по умолчанию для параметра является `document` .  

На приведенном ниже рисунке первый `img` элемент найден после элемента `title--image` и отображается `src` правильно.  

:::image type="complex" source="../media/console-element-selector-image-filter-source.msft.png" alt-text="$ _ — это последнее вычисленное выражение" lightbox="../media/console-element-selector-image-filter-source.msft.png":::
   На рисунке 7: `$('img', document.querySelector('title--image')).src`  
:::image-end:::  

> [!NOTE]
> Если вы используете библиотеку (например, jQuery, которая использует `$` , эта функция перезаписывается и `$` соответствует реализации из этой библиотеки).  

## Выбор запроса  

```console
$$(selector, [startNode])
```  

Возвращает массив элементов, которые соответствуют указанному селектору CSS.  Этот метод эквивалентен вызову метода [Document. querySelectorAll ()][MDNDocumentQuerySelectorAll] .  

В приведенном ниже примере кода и рисунке используется `$$()` для создания массива всех `<img>` элементов в текущем документе и отображения значения `src` свойства для каждого элемента.  

```console
var images = $$('img');
for (each in images) {
    console.log(images[each].src);
}
```  

:::image type="complex" source="../media/console-element-selector-image-all.msft.png" alt-text="$ _ — это последнее вычисленное выражение" lightbox="../media/console-element-selector-image-all.msft.png":::
   Рисунок 8: использование `$$()` для выделения всех изображений в документе и отображения источников  
:::image-end:::  

Этот метод также поддерживает второй параметр, startNode, указывающий элемент или узел, из которого нужно выполнить поиск элементов.  Значением по умолчанию для параметра является `document` .  

В следующем примере кода и рисунке измененная версия предыдущего примера кода и на рисунке используются `$$()` для создания массива всех `<img>` элементов, которые отображаются в текущем документе после выбранного узла.  

```console
var images = $$('img', document.querySelector(`title--image`));
for (each in images) {
   console.log(images[each].src);
}
```  

:::image type="complex" source="../media/console-element-selector-image-filter-all.msft.png" alt-text="$ _ — это последнее вычисленное выражение" lightbox="../media/console-element-selector-image-filter-all.msft.png":::
   Рисунок 9: использование `$$()` для выбора всех изображений, которые отображаются после указанного `<div>` элемента в документе, и отображения источников  
:::image-end:::  

> [!NOTE]
> Нажмите клавишу `Shift` + `Enter` консоль, чтобы начать новую строку, не выполняя сценарий.  

## Выражения  

```console
$x(path, [startNode])
```  

Возвращает массив элементов DOM, соответствующих указанному выражению XPath.  

В приведенном ниже примере кода `<p>` возвращаются все элементы на странице.  

```console
$x("//p")
```  

:::image type="complex" source="../media/console-array-xpath.msft.png" alt-text="$ _ — это последнее вычисленное выражение" lightbox="../media/console-array-xpath.msft.png":::
   Рисунок 10: использование селектора XPath  
:::image-end:::  

В приведенном ниже примере кода и рисунке `<p>` возвращаются все элементы, содержащие `<a>` элементы.  

```console
$x("//p[a]")
```  

:::image type="complex" source="../media/console-array-xpath-sub-element.msft.png" alt-text="$ _ — это последнее вычисленное выражение" lightbox="../media/console-array-xpath-sub-element.msft.png":::
   Рисунок 11: использование более сложного селектора XPath  
:::image-end:::  

Как и другие команды Selector, `$x(path)` имеет дополнительный второй параметр, `startNode` указывающий на элемент или узел, из которого нужно выполнить поиск элементов.  

:::image type="complex" source="../media/console-array-xpath-startnode.msft.png" alt-text="$ _ — это последнее вычисленное выражение" lightbox="../media/console-array-xpath-startnode.msft.png":::
   Рисунок 12: использование селектора XPath с `startNode`  
:::image-end:::  

## Сброс  

```console
clear()
```  

Очищает консоль журнала.  

```console
clear()
```  

## copy  

```console
copy(object)
```  

`copy(object)`Метод копирует строковое представление указанного объекта в буфер обмена.  

```console
copy($0)
```  

## отладка  

```console
debug(method)
```  

>[!NOTE]
> [#1050237 проблема с Chromium][MonorailIssue1050237] отслеживает ошибку с `debug()` функцией.  Если вы столкнулись с проблемой, попробуйте использовать вместо нее [точки останова][DevtoolsJavascriptBreakpoints] .  

Когда вы запрашиваете указанный метод, отладчик вызывается и останавливается внутри метода на панели « **источники** », что позволяет пошагово пройти этот код и выполнить его отладку.  

```console
debug("debug");
```  

:::image type="complex" source="../media/console-debug-text.msft.png" alt-text="$ _ — это последнее вычисленное выражение" lightbox="../media/console-debug-text.msft.png":::
   Рисунок 13: прерывание внутри метода с `debug()`  
:::image-end:::  

Используйте `undebug(method)` для прекращения прерывания на методе или с помощью пользовательского интерфейса, чтобы отключить все точки останова.  

Дополнительные сведения о точках останова можно найти в разделе [приостановка кода с точки останова][DevToolsJavascriptBreakpoints].  

## dir  

```console
dir(object)
```  

Отображает список всех свойств указанного объекта в стиле объекта.  Этот метод является псевдонимом для метода [Console. dir ()][MDNConsoleDir] .  

Вычислите `document.head` текст на консоли, чтобы отобразить HTML `<head>` между `</head>` тегами и.  В приведенном ниже примере кода и рисунке после использования на консоли отображается вхождение стиля объекта `console.dir()` .  

```console
document.head;
dir(document.head);
```  

:::image type="complex" source="../media/console-dir-document-head-expanded.msft.png" alt-text="$ _ — это последнее вычисленное выражение" lightbox="../media/console-dir-document-head-expanded.msft.png":::
   Рисунок 14: ведение журнала `document.head` с помощью `dir()` метода  
:::image-end:::  

Дополнительные сведения можно найти в описании [`console.dir()`][DevToolsConsoleApiConsoleDirObject] записи в API-интерфейсе консоли.  

## dirxml  

```console
dirxml(object)
```  

Печатает XML-представление указанного объекта, как показано на вкладке **элементы** .  Этот метод эквивалентен методу [Console. DirXML ()][MDNConsoleDirxml] .  

## Проверка  

```console
inspect(object/method)
```  

Открывает и выбирает определенный элемент или объект на соответствующей панели: либо панель **элементов** для элементов DOM, либо панель **памяти** для объектов кучи JavaScript.  

В приведенном ниже примере и рисунке кода `document.body` откроется панель " **элементы** ".  

```console
inspect(document.body);
```  

:::image type="complex" source="../media/console-inspect-document-body.msft.png" alt-text="$ _ — это последнее вычисленное выражение" lightbox="../media/console-inspect-document-body.msft.png":::
   Рис. 15: Проверка элемента с помощью `inspect()`  
:::image-end:::  

При передаче метода для проверки этот метод открывает документ на панели « **источники** » для проверки.  

## getEventListeners  

```console
getEventListeners(object)
```  

Возвращает прослушиватели событий, зарегистрированные для указанного объекта.  Возвращаемое значение — это объект, который содержит массив для всех зарегистрированных типов событий \ (например, `click` или `keydown` \).  Каждый из этих массивов — это объекты, которые описывают прослушиватель, зарегистрированный для каждого типа.  В следующем примере кода показано, как перечисляются все прослушиватели событий, зарегистрированные в объекте Document.  

```console
getEventListeners(document);
```  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document.msft.png" alt-text="$ _ — это последнее вычисленное выражение" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document.msft.png":::
   Рисунок 16: результат использования `getEventListeners(document)`  
:::image-end:::  

Если в указанном объекте зарегистрировано более одного прослушивателя, то массив содержит элемент для каждого прослушивателя.  На рисунке ниже показано, как в элементе Document для события зарегистрированы два прослушивателя событий `click` .  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document-expanded-1.msft.png" alt-text="$ _ — это последнее вычисленное выражение" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document-expanded-1.msft.png":::
   Рисунок 17: несколько прослушивателей  
:::image-end:::  

Вы можете расширить каждый из указанных ниже объектов, чтобы просмотреть свойства.  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document-2.msft.png" alt-text="$ _ — это последнее вычисленное выражение" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document-2.msft.png":::
   Рисунок 18: развернутое представление объекта прослушивателя  
:::image-end:::  

## клавиши  

```console
keys(object)
```  

Возвращает массив, содержащий имена свойств, принадлежащих указанному объекту.  Чтобы получить связанные значения одинаковых свойств, используйте `values()` .  

Например, предположим, что приложение определило следующий объект.  

```console
var player1 = { "name":  "Ted", "level": 42 }
```  

В приведенных ниже примерах кода предполагается, что результат `player1` определен в глобальном пространстве имен \ (для простоты) перед вводом `keys(player1)` и `values(player1)` на консоли.  

```console
keys(player1)

values(player1)
```  

:::image type="complex" source="../media/console-keys-values.msft.png" alt-text="$ _ — это последнее вычисленное выражение" lightbox="../media/console-keys-values.msft.png":::
   На рисунке 19: `keys()` `values()` команды и  
:::image-end:::  

## монитор  

```console
monitor(method)
```  

Заносит в консоль сообщение, которое указывает имя метода вместе с аргументами, передаваемыми методу при его вызове.  

```console
function sum(x, y) {
    return x + y;
}
monitor(sum);
```  

:::image type="complex" source="../media/console-function-monitor-sum.msft.png" alt-text="$ _ — это последнее вычисленное выражение" lightbox="../media/console-function-monitor-sum.msft.png":::
   Рис. 20: `monitor()` метод  
:::image-end:::  

Используется `unmonitor(method)` для прекращения наблюдения.  

## monitorEvents  

```console
monitorEvents(object[, events])
```  

Когда в указанном объекте происходит одно из указанных событий, объект события регистрируется в консоли.  Вы можете указать одно событие для отслеживания, массив событий или один из типов универсальных событий, сопоставленных с предопределенной коллекцией событий.  Ниже приведен пример кода и рисунок.  

Ниже приведено наблюдение за всеми событиями изменения размера объекта Window.  

```console
monitorEvents(window, "resize");
```  

:::image type="complex" source="../media/console-monitor-events-resize-window.msft.png" alt-text="$ _ — это последнее вычисленное выражение" lightbox="../media/console-monitor-events-resize-window.msft.png":::
   Рисунок 21: наблюдение за событиями изменения размера окна  
:::image-end:::  

В следующем примере определяется массив для мониторинга обоих `resize` и `scroll` событий в объекте Window.  

```console
monitorEvents(window, ["resize", "scroll"]);
```  

Вы также можете указать один из доступных типов событий — строки, которые сопоставляются с предопределенными наборами событий.  В приведенной ниже таблице показаны типы доступных событий и сопоставлений связанных событий.  

| Тип события | Соответствующие сопоставленные события |  
|:--- |:--- |  
| `mouse` | "Click", "DblClick", "MouseDown", "MouseMove", "указатель мыши", "onmouseover", "MouseUp", "MouseWheel" |  
| `key` | "KeyDown", "нажатие клавиши", "KeyUp", "textInput" |  
| `touch` | "touchcancel", "touchend", "touchmove", "touchstart" |  
| `control` | "Размытие", "Изменить", "фокусировку", "прокрутка", "выделить", "Отправить", "выбрать", "Отправить", "с масштабом" |  

В следующем примере кода `key` Тип события, соответствующий `key` событиям текстового поля ввода, в данный момент выделены на панели **элементы** .  

```console
monitorEvents($0, "key");
```  

На приведенном ниже рисунке показан пример выходных данных после ввода символа в текстовом поле.  

:::image type="complex" source="../media/console-monitor-events-type-t-y.msft.png" alt-text="$ _ — это последнее вычисленное выражение" lightbox="../media/console-monitor-events-type-t-y.msft.png":::
   Рис. 22: Отслеживание ключевых событий  
:::image-end:::  

## профиль  

```console
profile([name])
```  

Запускает сеанс профилирования ЦП JavaScript с необязательным именем.  Метод [profileEnd ()](#profileend) завершает профиль и отображает результаты на панели **памяти** .  <!--See also [Speed Up JavaScript Runtime][DevToolsRenderingToolsJSRuntime].  -->  

1.  Запустите `profile()` метод, чтобы начать профилирование.  
    
    ```console
    profile("My profile")
    ```  
    
1.  Запустите метод [profileEnd ()](#profileend) , чтобы остановить профилирование и отобразить результаты на панели **памяти** .  

Профили также могут быть вложенными.  В приведенных ниже примерах кода результат одинаков вне зависимости от порядка.  

```console
profile('A');
profile('B');
profileEnd('A');
profileEnd('B');
```  

> [!NOTE]
> Несколько профилей ЦП могут работать одновременно, и вы не обязаны закрывать каждый из них в заказе на создание.  

## profileEnd  

```console
profileEnd([name])
```  

Завершает сеанс профилирования ЦП JavaScript и отображает результаты на панели **памяти** .  Необходимо запустить метод [Profile ()](#profile) .  <!--See also [Speed Up JavaScript Runtime][DevToolsRenderingToolsJSRuntime].  -->  

1.  Запустите метод [Profile ()](#profile) , чтобы начать профилирование.  
1.  Запустите `profileEnd()` метод, чтобы остановить профилирование и отобразить результаты на панели **памяти** .  
    
    ```console
    profileEnd("My profile")
    ```  

Профили также могут быть вложенными.  В приведенном ниже примере кода результат одинаков вне зависимости от порядка.  

```console
profile('A');
profile('B');
profileEnd('A');
profileEnd('B');
```  

Результат появится в виде снимка кучи на панели " **память** ".  

:::image type="complex" source="../media/console-memory-multiple-cpu-profiles.msft.png" alt-text="$ _ — это последнее вычисленное выражение" lightbox="../media/console-memory-multiple-cpu-profiles.msft.png":::
   Рисунок 23: сгруппированные профили  
:::image-end:::  

> [!NOTE]
> Несколько профилей ЦП могут работать одновременно, и вы не обязаны закрывать каждый из них в заказе на создание.  

## queryObjects  

```console
queryObjects(Constructor)
```  

Возвращают массив объектов, созданных с помощью указанного конструктора.  Область `queryObjects()` — это выбранный в данный момент контекст среды выполнения на консоли.

:::row:::
   :::column span="1":::
      ```console
      queryObjects(promise)
      ```  
      
      Возвращает все `Promises` .  
   :::column-end:::
   :::column span="1":::
      ```console
      queryObjects(HTMLElement)
      ```  
      
      Возвращает все элементы HTML.  
   :::column-end:::
   :::column span="1":::
      ```console
      queryObjects(functionName)
      ```  
      
      Возвращает все объекты, экземпляры которых были созданы с помощью `new functionName()` .  
   :::column-end:::
:::row-end:::  

---  

## таблич  

```console
table(data[, columns])
```  

Заносит в журнал объектные данные с форматированием таблицы, основанным на объекте данных, с помощью необязательных заголовков столбцов.  В приведенном ниже примере кода и рисунке показано, как отображается список имен, использующих таблицу на консоли.  

```console
var names = {
    0:  {
        firstName:  "John",
        lastName:  "Smith"
    },
    1:  {
        firstName:  "Jane",
        lastName:  "Doe"
    }
};
table(names);
```  

:::image type="complex" source="../media/console-table-display.msft.png" alt-text="$ _ — это последнее вычисленное выражение" lightbox="../media/console-table-display.msft.png":::
   Рисунок 24: результат выполнения `table()` метода  
:::image-end:::  

## Отладка  

```console
undebug(method)
```  

Прекращает отладку указанного метода, поэтому при вызове метода отладчик больше не вызывается.  

```console
undebug(getData);
```  

## отследить  

```console
unmonitor(method)
```  

Останавливает мониторинг указанного метода.  Этот метод используется совместно с методом [Monitor ()](#monitor) .  

```console
unmonitor(getData);
```  

## unmonitorEvents  

```console
unmonitorEvents(object[, events])
```  

Прекращает наблюдение за событиями для указанного объекта и событий.  Например, в приведенном ниже примере останавливается отслеживание всех событий в объекте Window.  

```console
unmonitorEvents(window);
```  

Вы также можете отключить наблюдение за определенными событиями для объекта.  Например, следующий код начинает наблюдать за всеми `mouse` событиями выбранного в данный момент элемента, а затем останавливает наблюдение за `mousemove` событиями (возможно, чтобы уменьшить шум в выходных данных консоли \).  

```console
monitorEvents($0, "mouse");
unmonitorEvents($0, "mousemove");
```  

## данные  

```console
values(object)
```  

Возвращает массив, содержащий значения всех свойств, принадлежащих указанному объекту.  

```console
values(object);
```  

<!-- links -->  

[DevToolsConsoleApi]: /microsoft-edge/devtools-guide-chromium/console/api "Справочник по API консоли"  
[DevToolsConsoleApiConsoleDirObject]: /microsoft-edge/devtools-guide-chromium/console/api#dir "Справочник по API dir-Console"  
[DevToolsJavascriptBreakpoints]: /microsoft-edge/devtools-guide-chromium/javascript/breakpoints "Приостановка кода с точки останова в Microsoft Edge DevTools"  
[DevToolsRenderingToolsJSRuntime]: /microsoft-edge/devtools-guide-chromium/rendering-tools/js-runtime "Ускорение выполнения JavaScript"  

[MDNConsoleDir]: https://developer.mozilla.org/docs/Web/API/Console/dir "Console. dir () | MDN"  
[MDNConsoleDirxml]: https://developer.mozilla.org/docs/Web/API/Console/dirxml "Console. DirXML () | MDN"  
[MDNDocumentQuerySelector]: https://developer.mozilla.org/docs/Web/API/Document/querySelector "Document. querySelector () | MDN"  
[MDNDocumentQuerySelectorAll]: https://developer.mozilla.org/docs/Web/API/Document/querySelectorAll "Document. querySelectorAll () | MDN"  

[MonorailIssue1050237]: https://bugs.chromium.org/p/chromium/issues/detail?id=1050237 "Ошибка 1050237: Отладка (функция) не работает | Monorail"  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/console/utilities) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
