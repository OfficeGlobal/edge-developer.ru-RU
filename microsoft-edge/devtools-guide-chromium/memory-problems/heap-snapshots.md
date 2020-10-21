---
description: Узнайте, как записывать моментальные снимки кучи с помощью профилировщика Microsoft Edge DevTools и поиска утечек памяти.
title: Запись моментальных снимков кучи
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 9762cb1d4932ce1a5d0b1c3944aa0b85d78b1060
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125463"
---
<!-- Copyright Meggin Kearney 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->

# Запись моментальных снимков кучи  

Узнайте, как записывать моментальные снимки кучи с помощью профилировщика Microsoft Edge DevTools и поиска утечек памяти.  

Профилировщик кучи Microsoft Edge DevTools показывает распределение памяти по объектам JavaScript и связанным узлам DOM на странице.  Используйте его для создания моментальных снимков JavaScript \ (JS-файлов, кучи и т. д.), анализа графов памяти, сравнения снимков и поиска утечек памяти.  Смотрите также [объекты][DevtoolsMemoryProblems101ObjectsRetainingTree], которые хранятся в дереве.  

## Создание снимка  

На панели **память** выберите команду **сделать снимок**, а затем нажмите кнопку **начать**.  Вы также можете выбрать `Ctrl` + `E` \ (Windows, Linux \) или `Cmd` + `E` \ (macOS \).  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots.msft.png" alt-text="Выбор типа профилирования" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots.msft.png":::
   Выбор типа профилирования  
:::image-end:::  

**Моментальные снимки** первоначально хранятся в памяти процесса обработчика.  При необходимости снимки переносятся в DevTools по запросу, если щелкнуть значок снимка, чтобы просмотреть его.  

После того как вы загрузили моментальный снимок в DevTools и проанализируете его, появится число под заголовком снимка, в котором будет показан [Общий размер достижимых объектов JavaScript][DevtoolsMemoryProblems101ObjectSizes].  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all.msft.png" alt-text="Выбор типа профилирования" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all.msft.png":::
   Общий размер достижимых объектов  
:::image-end:::  

> [!NOTE]
> В снимки включаются только достижимые объекты.  Кроме того, создание моментального снимка всегда начинается со сборки мусора.  

## Очистка снимков  

Нажмите кнопку **Очистить все профили** , чтобы удалить снимки \ (как из DevTools, так и из памяти, связанной с процессом рендеринга \).  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all-hover-clear-all-profiles.msft.png" alt-text="Выбор типа профилирования" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all-hover-clear-all-profiles.msft.png":::
   Удаление снимков  
:::image-end:::  

Закрытие окна DevTools не приводит к удалению профилей из памяти, связанной с процессом рендеринга.  При повторном открытии DevTools все ранее созданные моментальные снимки снова появляются в списке снимков.  

> [!NOTE]
> Попробуйте этот пример [геоточечных объектов][GlitchDevtoolsMemoryExample03] и пропрофилировать его с помощью профилировщика кучи.  Вы увидите число выделений элементов \ (объект \).  

## Просмотр снимков  

Просмотр снимков с разных точек зрения для разных задач.  

В **представлении "Сводка** " отображаются объекты, сгруппированные по имени конструктора.  Используйте его для поиска объектов \ (и использование памяти \) в зависимости от типа, сгруппированного по имени конструктора.  Это особенно полезно для **отслеживания УТЕЧЕК DOM**.

<!--todo: add profile memory problems memory diagnosis (tracking down DOM leaks) section when available  -->  

**Представление сравнения**.  Показывает разницу между двумя снимками.  Используйте его для сравнения двух (или более) моментальных снимков памяти от до и после выполнения операции.  Проверка дельты в освобожденной памяти и счетчике ссылок позволяет вам подтвердить присутствие и причину утечки памяти.  

**Представление "вложение**".  Позволяет исследовать содержимое кучи.  **Представление "вложение** " обеспечивает более эффективное представление структуры объектов, помогая анализировать объекты, на которые ссылается глобальное пространство имен \ (окно \), чтобы узнать, что такое хранение объектов.  Используйте его для анализа замыканий и пошагового углубления объектов на низком уровне.  

Для переключения между представлениями Используйте селектор в верхней части представления.  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-view-dropdown.msft.png" alt-text="Выбор типа профилирования" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-view-dropdown.msft.png":::
   Переключатель выбора представлений  
:::image-end:::  

> [!NOTE]
> Не все свойства хранятся в куче JavaScript.  Свойства, реализованные с помощью методов доступа, которые выполняют машинный код, не фиксируются.  Кроме того, не записываются значения, не являющиеся строками, например числа.  

### Представление сводки  

Изначально в представлении сводки открывается моментальный снимок, в котором отображаются итоговые объекты, которые могут быть развернуты для отображения экземпляров.  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-retainers.msft.png" alt-text="Выбор типа профилирования" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-retainers.msft.png":::
   Представление **сводки**  
:::image-end:::  

Элементы верхнего уровня — строки "Итого".  

| Элементы верхнего уровня | Описание |  
|:--- |:--- |  
| **Конструктор** | Представляет все объекты, созданные с помощью этого конструктора.  |  
| **Расстояние** | показывает расстояние до корня с минимальным простым путем к узлам.  |  
| **Неглубокий размер** | Отображает сумму мелких размеров всех объектов, созданных с помощью определенной функции конструктора.  Неглубокий размер — это размер памяти, занимаемой объектом, (обычно массивы и строки имеют более мелких размеров).  Смотрите также [размеры объектов][DevtoolsMemoryProblems101ObjectSizes].  |  
| **Сохраненный размер** | Отображение максимального размера в одном наборе объектов.  Объем памяти, который вы можете освобождать после удаления объекта \ (а зависимые элементы становятся недостижимыми \), называется сохраненным размером.  Смотрите также [размеры объектов][DevtoolsMemoryProblems101ObjectSizes].  |  

<!--| **Number of object instances** | Displayed in the # column.  |  -->  

После того как вы разворачиваете итоговую строку в верхнем представлении, отобразятся все экземпляры.  Для каждого экземпляра в соответствующих столбцах отображаются неполные и удержанные размеры.  Число после `@` символа является уникальным идентификатором объекта, что позволяет сравнивать моментальные снимки кучи на отдельных объектах.  

Обратите внимание, что желтые объекты содержат ссылки на JavaScript, а красные объекты — это отсоединенные узлы, на которые ссылается один из них с желтым фоном.  

**Что в профилировщике кучи соотносятся различные элементы конструктора \ (Group \)?**  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-highlight.msft.png" alt-text="Выбор типа профилирования" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-highlight.msft.png":::
   Группы **конструкторов**  
:::image-end:::  

| Элемент Конструктор \ (группировка) | Описание |  
|:--- |:--- |  
| **\ (глобальное свойство)** | Промежуточные объекты между глобальным объектом (например, `window` \) и объектом, на который ссылается этот объект.  Если объект создается с помощью конструктора `Person` и удерживается глобальным объектом, путь сохранения будет выглядеть так, как нужно `[global] > \(global property\) > Person` .  Это отличается от нормы, где объекты непосредственно ссылаются друг на друга.  Промежуточные объекты существуют для повышения производительности.  Глобальные объекты регулярно изменяются, а оптимизации доступа к свойствам являются хорошим заданием для неглобальных объектов, неприменимо для глобальных.  |  
| **\ (корни \)** | Корневые элементы в представлении в виде дерева сохраняются как сущности, которые содержат ссылки на выбранный объект.  Записи могут также содержать ссылки, созданные ядром для целей, специфических для ядра.  Ядро содержит кэш, в котором есть ссылки на объекты, но все такие ссылки являются слабыми и не запрещают сбору объекта с учетом того, что нет действительно строгой ссылки.  |  
| **\ (замыкание)** | Количество ссылок на группу объектов с помощью замыкания функций.  |  
| **\ (массив, строка, число, regexp)** | Список типов объектов со свойствами, которые ссылаются на массив, строку, число или регулярное выражение.  |  
| **\ (скомпилированный код)** | Все, что связано с компилированным кодом.  Сценарий похож на функцию, но соответствует `<script>` телу.  SharedFunctionInfos \ (SFI \) — объекты, зафиксированные между функциями и скомпилированным кодом.  У функций обычно есть контекст, а не SFIs.  |  
| **HTMLDivElement**, **HTMLAnchorElement**, **DocumentFragment**и т. д.  | Ссылки на элементы или объекты документа определенного типа, на которые ссылается ваш код.  |  

<!--todo: add heap profiling summary section when available -->  

### Представление "Сравнение"  

Находить потерянные объекты, сравнивая несколько моментальных снимков друг с другом.  Чтобы убедиться в том, что определенная операция приложения не создает утечки \ (например, при открытии документа, а затем его закрытии), не следует оставлять все сборки мусора, вы можете воспользоваться приведенным ниже сценарием.  

1.  Сделайте снимок кучи, прежде чем выполнять операцию.  
1.  Выполнение операции \ (взаимодействие с страницей в некоторых условиях, когда вы считаете, что она вызывает утечку).  
1.  Выполните обратную операцию, чтобы (выполнить обратное взаимодействие и повторить ее несколько раз).  
1.  Сделайте второй снимок кучи и измените его представление на **Сравнение**, сравнив его с **снимком 1**.  
    
В представлении **Сравнение** отображается разница между двумя снимками.  При развертывании элемента общего типа отображаются добавленные и удаленные экземпляры объекта.  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-comparison-dropdown.msft.png" alt-text="Выбор типа профилирования" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-comparison-dropdown.msft.png":::
   Представление " **Сравнение** "  
:::image-end:::  

<!--todo: add HeapProfilingComparison section when available  -->  

### Представление "вложение"  

Представление " **вложение** " — это по сути представление "глаз с высоты птичьего полета" для структуры объектов приложения.  Это позволяет просматривать замыкания функций внутри функции, чтобы отслеживать внутренние объекты виртуальной машины \ (VM \), которые вместе составляют объекты JavaScript, и понять, какая память используется приложением на очень низком уровне.  

| Точки входа в Просмотр вложений | Описание |  
|:--- |:--- |  
| **Объекты DOMWindow** | Глобальные объекты для кода JavaScript.  |  
| **Корни GC** | Фактические корни GC, используемые сборкой мусора ВМ.  Корни GC состоят из встроенных карт объектов, таблиц символов, стеков потоков виртуальной машины, кэшей компиляций, областей обработки и глобальных дескрипторов.  |  
| **Собственные объекты** | Объекты браузера "отправили" на виртуальной машине JavaScript \ (JavaScript VM \), чтобы разрешить автоматизацию, например узлы DOM, правила CSS.  |  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-containment-dropdown.msft.png" alt-text="Выбор типа профилирования" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-containment-dropdown.msft.png":::
   Представление " **вложение** "  
:::image-end:::  

<!--todo: add heap profiling containment section when available  -->  

> [!TIP]
> Всплывающая подсказка о замыканиях.  Назовите функции таким образом, чтобы можно было легко отличать между собой замыкания в снимке.  Например, в этом примере не используются именованные функции.  
> 
> ```javascript
> function createLargeClosure() {
>     var largeStr = new Array(1000000).join('x');
>     var lC = function() { // this is NOT a named function
>         return largeStr;
>     };
>     return lC;
> }
> ```  
> 
> Во фрагменте followingcode используются именованные функции.  
> 
> ```javascript
> function createLargeClosure() {
>     var largeStr = new Array(1000000).join('x');
>     var lC = function lC() { // this IS a named function
>         return largeStr;
>     };
>     return lC;
> }
> ```  
> 
> <!--  
> :::image type="complex" source="../media/memory-problems-domleaks.msft.png" alt-text="Выбор типа профилирования" lightbox="../media/memory-problems-domleaks.msft.png":::
>    Name functions to distinguish between closures  
> :::image-end:::  
> -->  
> 
> > [!NOTE]
> > Попробуйте этот пример, чтобы [можно `eval` было][GlitchDevtoolsMemoryExample07] проанализировать влияние замыканий на память.  Кроме того, вам может потребоваться подписаться на этот пример, в котором осуществляется запись [ресурсов кучи][GlitchDevtoolsMemoryExample08].  
> 

## Поиск цветового кодирования  

Свойства и значения свойств объектов имеют различные типы и окрашены соответствующим образом.  Каждое свойство имеет один из четырех типов.  

| Тип свойства | Описание |  
|:--- |:--- |  
| **a: свойство** | Обычное свойство с именем, доступ к которому осуществляется с помощью `.` оператора \ (точка) или через `[` `]` \ (квадратные скобки \), например `["foo bar"]` .  |  
| **0: элемент** | Регулярное свойство с числовым индексом, доступ к которому осуществляется через `[` `]` представление \ (скобки).  |  
| **a: VAR (контекст)** |  Переменная в контексте функции, доступная по имени переменной из замыкания функции.  |  
| **a: System Prop** | Свойство, добавленное виртуальной машиной JavaScript, недоступно из кода JavaScript.  |  

Объекты, помеченные как не `System` имеющие соответствующего типа JavaScript.  Каждый из них является частью реализации объектной системы виртуальной машины JavaScript.  V8 выделяет большинство внутренних объектов в той же куче, где находятся объекты JS пользователя.  Итак, это только внутренние V8.  

## Поиск конкретного объекта  

Чтобы найти объект в собранной куче, вы можете найти его с помощью `Ctrl` + `F` и присвоить ему идентификатор объекта.  

## Обнаружение утечек DOM  

Профилировщик кучи может отображать двунаправленные зависимости между собственными объектами браузера \ (узлы DOM, правила CSS \) и объекты JavaScript.
Это помогает выявить невидимые утечки, происходящие из-за плавающего отсоединенного поддерева DOM.  

Утечки DOM могут быть больше, чем вы думаете.  Вот пример.  Когда #tree GC?  

```javascript
var select = document.querySelector;
var treeRef = select("#tree");
var leafRef = select("#leaf");
var body = select("body");
body.removeChild(treeRef);
//#tree in not GC yet due to treeRef
treeRef = null;
//#tree is not GC yet due to indirect
//reference from leafRef
leafRef = null;
//#NOW able to be #tree GC
```  

Функция `#leaf` хранит ссылку на подходящую родительскую структуру \ (ParentNode \) и рекурсивно `#tree` дополнить, так что только в том случае, если leafRef является nullified — это всего лишь дерево с `#tree` кандидатом на сборку мусора.  

:::image type="complex" source="../media/memory-problems-tree-gc.msft.png" alt-text="Выбор типа профилирования" lightbox="../media/memory-problems-tree-gc.msft.png":::
   Поддерево DOM  
:::image-end:::  

> [!NOTE]
> Примеры: попробуйте этот пример [утечки узла DOM][GlitchDevtoolsMemoryExample06] , чтобы понять, где она может быть потеряна и как ее найти.  Кроме того, вы можете просмотреть этот пример [утечек DOM больше, чем ожидалось][GlitchDevtoolsMemoryExample09].  

Для получения дополнительных сведений о утечках DOM и анализе памяти ознакомьтесь с разделом извлечение [и отладка утечек памяти с помощью Microsoft Edge DevTools][GonzaloRuizdeVillaMemory] , Gonzalo Ruiz De Villa.  

<!--  
> [!NOTE]
> Example: Try this **demo** to play with detached DOM trees.  
-->  

<!--todo: add heap profiling dom leaks section when available  -->  

## Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsMemoryProblems101ObjectSizes]: ./memory-101.md#object-sizes "Размеры объектов — терминология с памятью | Документы Microsoft"  
[DevtoolsMemoryProblems101ObjectsRetainingTree]: ./memory-101.md#objects-retaining-tree "Объекты, в которых хранятся терминология в дереве-память | Документы Microsoft"  

<!--[DevToolsHeapProfilingComparison]: https://developer.alphabet.com/devtools/docs/heap-profiling-comparison ""  -->  
<!--[DevToolsHeapProfilingContainment]: https://developer.alphabet.com/devtools/docs/heap-profiling-containment ""  -->  
<!--[DevtoolsHeapProfilingDomLeaks]: https://developer.alphabet.com/devtools/docs/heap-profiling-dom-leaks ""  -->  
<!--[DevToolsHeapProfilingSummary]: https://developer.alphabet.com/devtools/docs/heap-profiling-summary ""  -->  
<!--[DevtoolsProfileMemoryProblemsDiagnosisCausesMemoryLeaks]: ../profile/memory-problems/memory-diagnosis#narrow-down-causes-of-memory-leaks ""  -->  

[GlitchDevtoolsMemoryExample03]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-03.html "example-03.html-Microsoft EDGE (Chromium) DevTools | Цепь"  
[GlitchDevtoolsMemoryExample06]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-06.html "example-06.html-Microsoft EDGE (Chromium) DevTools | Цепь"  
[GlitchDevtoolsMemoryExample07]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-07.html "example-07.html-Microsoft EDGE (Chromium) DevTools | Цепь"  
[GlitchDevtoolsMemoryExample08]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-08.html "example-08.html-Microsoft EDGE (Chromium) DevTools | Цепь"  
[GlitchDevtoolsMemoryExample09]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-09.html "example-09.html-Microsoft EDGE (Chromium) DevTools | Цепь"  
[GlitchDevtoolsMemoryExample10]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-10.html "example-10.html-Microsoft EDGE (Chromium) DevTools | Цепь"  

[GonzaloRuizdeVillaMemory]: https://slid.es/gruizdevilla/memory "память | Закончен"  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/memory-problems/heap-snapshots) и была написана с помощью [Meggin Kearney][MegginKearney] \ (технический редактор \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
