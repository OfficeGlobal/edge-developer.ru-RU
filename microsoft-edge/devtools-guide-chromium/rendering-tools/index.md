---
description: Пользователи ожидают интерактивные и плавные страницы.  Каждый этап конвейера на пиксельах представляет возможность введения Jank.  Узнайте о средствах и стратегиях, позволяющих выявить и устранить распространенные проблемы, которые замедляют производительность во время выполнения.
title: Анализ производительности среды выполнения
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: f7ca848712268110700fac2c5fb75fe1751812bf
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/02/2020
ms.locfileid: "10992709"
---
<!-- Copyright Kayce Basques and Meggin Kearney

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->

# Анализ производительности среды выполнения 

Пользователи ожидают интерактивные и плавные страницы.  Каждый этап конвейера на пиксельах представляет возможность введения Jank.  Узнайте о средствах и стратегиях, позволяющих выявить и устранить распространенные проблемы, которые замедляют производительность во время выполнения.  

### Краткий обзор  

*   Не записывайте JavaScript, который заставляет браузер обновить макет.  Разделяйте функции чтения и записи, а затем выполняйте операции чтения первыми.  
*   Не переусложняйте CSS.  Используйте меньший CSS, чтобы сделать селекторы CSS простыми.  
*   Старайтесь не использовать разметку максимально возможной.  Выберите CSS, для которого не запущен макет.  
*   Рисование может занимать больше времени, чем любые другие действия рендеринга.  Посмотрите, как узкие места закрашивания закраски.  
    
## JavaScript  

Вычисления JavaScript, особенно те, которые вызывают сложные визуальные изменения, могут привести к снижению производительности приложения.  Не разрешать неправильное или долгое выполнение JavaScript, мешая взаимодействию с пользователем.  

### JavaScript: инструменты  

Сделайте запись на панели " **производительность** " и найдите подозрительные `Evaluate Script` события.  <!--If you find any, you are able to enable the **JS Profiler** and re-do your recording to get more detailed information about exactly which JavaScript functions were used and how long each took.  -->  

<!--todo: add Recording section when available  -->  
<!--todo: add Profile JavaScript (JS Profiler) section when available  -->  

е, что вы проjankе в JavaScript, вам может потребоваться выполнить анализ следующего уровня и собрать профиль ЦП JavaScript.  В профилях ЦП показано, где в функциях страницы потратила среда выполнения.  В этой статье объясняется, как создавать профили ЦП с использованием [ускорения выполнения JavaScript][DevtoolsRenderingToolsJavascriptRuntime].

### JavaScript: проблемы  

В приведенной ниже таблице описаны некоторые распространенные проблемы JavaScript и возможные решения.  

| Проблема | Пример. | Решение |  
|:--- |:--- |:--- |  
| Ресурсоемкие обработчики входных данных, влияющие на отклик или анимацию.  | Сенсор, параллакс прокрутку.  | Разрешите браузеру управлять сенсорными и прокруткой или привяжите прослушиватель как можно позже.  Просмотр [ресурсоемких обработчиков ввода в контрольном списке производительности в пол Lewis and "][WebPerformanceCalendarRuntimeChecklist].  |  
| Некорректное применение JavaScript, которое влияет на отклик, анимацию, загрузку.  | Пользователь выполняет прокрутку сразу после загрузки страницы, setTimeout/setInterval.  | Оптимизация среды выполнения JavaScript: использование `requestAnimationFrame` , распространение управления DOM на кадры и использование [веб-рабочих процессов][MDNUsingWebWorkers].  |  
| Длительное выполнение ответа на JavaScript.  | [Событие DOMContentLoaded][MDNUsingWebWorkers] останавливается, так как оно вашего удобства с помощью JS.  | Перевод чистых вычислительных трудозатрат на [веб-рабочие процессы][MDNUsingWebWorkers].  Если вам нужен доступ DOM, используйте `requestAnimationFrame` .  <!--See also [Optimize JavaScript Execution][WebFundamentalsPerformanceRenderingOptimizeJavascriptRuntime].  -->  |  
| Сценарии сборки мусора, влияющие на ответ или анимацию.  | Сбор мусора может происходить везде, где бы вы ни находились  | Создавать менее сценарии сборки мусора.  Ознакомьтесь со [сборкой мусора в анимации в контрольном списке производительности в пол Lewis and "][WebPerformanceCalendarRuntimeChecklist].  |  

<!--todo: add Optimize JavaScript runtime section when available  -->  

## Стиль  

Изменение стиля — это дорогостоящие особенности, особенно если эти изменения влияют на более чем один элемент в DOM.  Каждый раз, когда к элементу применяются стили, браузер отражает влияние на все связанные элементы, пересчитывать макет и перекрашивать.  

<!--Related Guides:  

*   [Reduce the Scope and Complexity of Styles Calculations][WebFundamentalsPerformanceRenderingReduceScope]  
-->  

<!--todo: add Reduce the Scope and Complexity of Styles Calculations section when available -->  

### Стиль: инструменты  

Сделайте запись на панели " **производительность** ".  Проверка записи для больших `Recalculate Style` событий (отображается фиолетовым).  

<!--todo: add Recording section when available  -->  

Щелкните событие, `Recalculate Style` чтобы просмотреть дополнительные сведения о нем в области **сведений** .  Если изменение стиля занимает много времени, это снижение производительности.  Если вычисления стиля влияют на большое количество элементов, это еще одна область с комнатой для улучшения.  

:::image type="complex" source="../media/rendering-tools-performance-recalculate-style-summary.msft.png" alt-text="Длинный стиль пересчета" lightbox="../media/rendering-tools-performance-recalculate-style-summary.msft.png":::
   Длинный стиль пересчета  
:::image-end:::  

Чтобы уменьшить влияние событий, `Recalculate Style` сделайте следующее:  

*   Используйте [триггеры CSS][CssTriggers] , чтобы выяснить, какие свойства CSS активируют макет, Paint и Composite.  Эти свойства имеют наихудшее влияние на производительность отрисовки.  
*   Переключиться на свойства с меньшим влиянием.  <!--See [Stick to compositor-only properties and manage layer count][WebFundamentalsPerformanceRenderingCompositorOnlyProperties] for more guidance.  -->  
    
<!--todo: add Stick to compositor-only properties and manage layer count section when available -->  

### Стиль: проблемы  

В таблице ниже описаны некоторые распространенные проблемы стиля и возможные решения.  

| Проблема | Пример. | Решение |  
|:--- |:--- |:--- |  
| Дорогостоящие расчеты стиля, влияющие на отклик или анимацию.  | Любое свойство CSS, которое изменяет геометрию элемента, например ширину, высоту или расположение; Браузер проверяет все другие элементы и пересчитывает макет.  | Старайтесь не использовать CSS, которые инициируют макеты |  
| Сложные селекторы, влияющие на отклик или анимацию.  | Вложенные элементы выбора заставляют браузер знать все о всех остальных элементах, включая родительские и дочерние элементы.  | Сослаться на элемент в таблице CSS только с помощью класса.  |  

<!--todo: add Avoid CSS that triggers layouts section when available -->  
<!--todo: add Reduce the Scope and Complexity of Styles Calculations (Reference an element in your CSS with just a class) section when available -->  

<!--Related Guides:  

*   [Reduce the Scope and Complexity of Styles Calculations][WebFundamentalsPerformanceRenderingReduceScope]  -->  

<!--todo: add Reduce the Scope and Complexity of Styles Calculations section when available -->  

## Макет  

Макет (или перекомпоновка в Firefox) — это процесс, с помощью которого браузер вычисляет позиции и размеры всех элементов на странице.  Модель макета веба означает, что один элемент может повлиять на других пользователей; Например, ширина `<body>` элемента обычно влияет на ширину дочерних элементов и т. д., так же, как и вниз по дереву.  Процесс может быть довольно вовлеченным в браузер.  

Как правило, если вы запрашиваете значение геометрического значения из DOM перед завершением кадра, вы собираетесь найти себя с помощью принудительно синхронных макетов, что может привести к значительному снижению производительности, если часто приходится создавать большое дерево DOM.  

<!--Related Guides:  

*   [Avoid Layout Thrashing][WebFundamentalsPerformanceRenderingAvoidLargeComplexLayouts]  
*   [Diagnose Forced Synchronous Layouts][DevtoolsRenderingToolsForcedSynchronousLayouts]  -->  

<!--todo: add Avoid CSS that triggers layouts (Avoid Layout Thrashing) section when available -->  
<!--todo: add Diagnose Forced Synchronous Layouts section when available  -->  

### Макет: инструменты  

Область **производительности** определяет, когда страница вызывает принудительно синхронные макеты.  Эти `Layout` события помечены красными отрезками.  

:::image type="complex" source="../media/rendering-tools-jank-performance-recalculate-style-summary.msft.png" alt-text="Длинный стиль пересчета" lightbox="../media/rendering-tools-jank-performance-recalculate-style-summary.msft.png":::
   Принудительно синхронный макет  
:::image-end:::  

"Макет Thrashing" — это повторение принудительно синхронно заданных условий макета.  Это происходит, когда JavaScript пишет и считывает из DOM многократно, что приводит к пересчету макета в браузере.  Чтобы определить макет Thrashing, найдите шаблон с несколькими принудительно синхронными предупреждениями макета.  Просмотреть предыдущий рисунок.  

### Макет: проблемы  

В таблице ниже описаны некоторые типичные проблемы с макетами и возможные решения.  

| Проблема | Пример. | Решение |  
|:--- |:--- |:--- |  
| Принудительно синхронный макет, влияющий на ответ или анимацию.  | Принудительное выполнение браузером более ранней версии в конвейере пикселей, что приводит к повторяющимся действиям в процессе отрисовки.  | Предварительно заполните свой стиль, а затем выполните все операции записи.  <!--See also [Avoid large, complex layouts and layout thrashing][WebFundamentalsPerformanceRenderingAvoidLargeComplexLayouts].  -->  |  
| Макет Thrashing влияет на отклик или анимацию.  | Цикл, покрывающий браузер, в цикле чтения и записи-чтения, который принудительно пересчитывает макет, переключаясь в браузер.  | Автоматическая обработка пакетных операций чтения и записи с помощью [библиотеки FastDom][GitHubWilsonpageFastdom].  |  

<!--todo: add Avoid CSS that triggers layouts (Avoid large, complex layouts and layout thrashing) section when available -->  

## Рисование и совмещение цветов  

Заливка — это процесс заполнения пикселов.  Это часто является наиболее дорогостоящей частью процесса отрисовки.  Если вы заметили, что ваша страница janky, возможно, у вас возникли проблемы с окрашиванием.  

Композиция — это область, в которой окрашенные части страницы размещаются вместе для отображения на экране.  В большинстве случаев, если вы перейдете на свойства, предназначенные только для компоновщика, и не можете вообще обрисовываться, вы увидите значительную улучшенность в производительности, но вам нужно пронаблюдать за избыточными счетчиками слоев.  <!--See also [Stick to compositor-only properties and manage layer count][WebFundamentalsPerformanceRenderingCompositorOnlyProperties].  -->  

<!--todo: add Stick to compositor-only properties and manage layer count section when available  -->  

### Рисование и совмещение: инструменты  

Хотите узнать, как долго рисуются и как часто происходит рисование?  Установите флажок [включить дополнительные возможности инструментирования Paint][DevtoolsChromiumEvaluatePerformanceReferenceEnableadvancedpaintinstrumentation] на панели **производительности** и сделайте запись.  Если большая часть времени отрисовки потратила на рисование, у вас возникли проблемы с рисованием.  

<!--
:::image type="complex" source="../media/rendering-tools-jank-performance-advanced-paint-instrumentation-summary.msft.png" alt-text="Длинный стиль пересчета" lightbox="../media/rendering-tools-jank-performance-advanced-paint-instrumentation-summary.msft.png":::
   Long paint times in timeline recording  
:::image-end:::  
-->  

<!--
Check out the **Rendering** panel for further configurations that are able to help you diagnose paint problems.  -->  

<!--todo: link Rendering panel in ../evaluate-performance/timeline-tool  sub-section when live  -->  

### Раскрашивание и совмещение: проблемы  

В таблице ниже описаны некоторые распространенные проблемы, возникающие при работе с закрасками и комплексными решениями.  

| Проблема | Пример. | Решение |  
|:--- |:--- |:--- |  
| Эффекты рисования влияют на реакцию или анимацию.  | Большие области или дорогостоящие краски влияют на реакцию или анимацию.  | Избегайте рисования, продвижение элементов, которые перемещаются в собственный слой, использование преобразований и непрозрачности.  <!--See [Simplify paint complexity and reduce paint areas][WebFundamentalsPerformanceRenderingSimplifyPaintComplexity].  -->  |  
| Развертывание слоев влияет на анимацию.  | Превышение избыточного продвижения слишком большого количества элементов `translateZ(0)` заметно влияет на производительность анимации.  | Придвигайте к слоям экономно и только в том случае, если вы знаете, что она содержит существенные улучшения.  <!--See [Stick to composite-only properties and manage layer count][WebFundamentalsPerformanceRenderingCompositorOnlyProperties].  -->  |  

<!--todo: add Simplify paint complexity and reduce paint areas section when available  -->  
<!--todo: add Stick to compositor-only properties and manage layer count section when available  -->  

## Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsRenderingToolsJavascriptRuntime]: ./js-runtime.md "Ускорение выполнения JavaScript | Документы Microsoft"  
[DevtoolsChromiumEvaluatePerformanceReferenceEnableadvancedpaintinstrumentation]: ../evaluate-performance/reference.md#enable-advanced-paint-instrumentation "Включение расширенного инструментария рисования — Справка по анализу производительности | Документы Microsoft"

<!--[DevtoolsRenderingToolsForcedSynchronousLayouts]: ./rendering-tools/forced-synchronous-layouts.md "Diagnose Forced Synchronous Layouts | Microsoft Docs"  -->  

<!-- The Timeline Tool page is deprecated  -->  
<!--[DevtoolsEvaluatePerformanceTimelineToolProfileJavascript]: ../evaluate-performance/timeline-tool#profile-javascript "Profile JavaScript - How to Use the Timeline Tool | Microsoft Docs"  -->  
<!--[DevtoolsEvaluatePerformanceTimelineToolProfilePainting]: ../evaluate-performance/timeline-tool#profile-painting "Profile painting - How to Use the Timeline Tool | Microsoft Docs"  -->  
<!--[DevtoolsEvaluatePerformanceTimelineToolRecording]: ../evaluate-performance/timeline-tool#make-a-recording "Make a recording - How to Use the Timeline Tool | Microsoft Docs"  -->  
<!--[DevtoolsEvaluatePerformanceTimelineToolRenderingSettings]: ../evaluate-performance/timeline-tool#rendering-settings "Rendering settings - How to Use the Timeline Tool | Microsoft Docs"  -->  

<!--[WebFundamentalsPerformanceRenderingAvoidLargeComplexLayouts]: /web/fundamentals/performance/rendering/avoid-large-complex-layouts-and-layout-thrashing "Avoid Large, Complex Layouts, and Layout Thrashing"  -->  
<!--[WebFundamentalsPerformanceRenderingOptimizeJavascriptRuntime]: /web/fundamentals/performance/rendering/optimize-javascript-execution "Optimize JavaScript Runtime"  -->  
<!--[WebFundamentalsPerformanceRenderingReduceScope]: /web/fundamentals/performance/rendering/reduce-the-scope-and-complexity-of-style-calculations "Reduce the Scope and Complexity of Style Calculations"  -->  
<!--[WebFundamentalsPerformanceRenderingSimplifyPaintComplexity]: /web/fundamentals/performance/rendering/simplify-paint-complexity-and-reduce-paint-areas "Simplify Paint Complexity and Reduce Paint Areas"  -->  
<!--[WebFundamentalsPerformanceRenderingCompositorOnlyProperties]: /web/fundamentals/performance/rendering/stick-to-compositor-only-properties-and-manage-layer-count "Stick to Compositor-Only Properties and Manage Layer Count"  -->  

[CssTriggers]: https://csstriggers.com "Триггеры CSS"  

[MDNUsingWebWorkers]: https://developer.mozilla.org/docs/Web/API/Web_Workers_API/Using_web_workers "Использование веб-сотрудников | MDN"  

[WebPerformanceCalendarRuntimeChecklist]: https://calendar.perfplanet.com/2013/the-runtime-performance-checklist/ "Контрольный список производительности во время выполнения — Календарь веб-производительности"  

[GitHubWilsonpageFastdom]: https://github.com/wilsonpage/fastdom "wilsonpage/fastdom | GitHub"  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/index) и [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \) и [Meggin Kearney][MegginKearney] \ (технический редактор \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
