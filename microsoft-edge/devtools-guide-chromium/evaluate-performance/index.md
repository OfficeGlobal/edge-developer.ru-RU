---
description: Сведения о том, как оценивать производительность среды выполнения в Microsoft Edge DevTools.
title: Приступая к анализу производительности среды выполнения
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 65351f3846ed76ef8a27dbff2cfb08c497282d15
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/02/2020
ms.locfileid: "10992948"
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

# Приступая к анализу производительности среды выполнения  

> [!NOTE]
> Сведения о том, как повысить скорость загрузки страниц, можно найти в статье [Оптимизация веб-сайта][DevtoolsSpeedGetStarted].  

Производительность во время выполнения — это то, как страница выполняется при ее запуске, а не в виде загрузки.  В следующей статье учебника объясняется, как использовать панель производительности Microsoft Edge DevTools для анализа производительности среды выполнения.  В плане модели **салазок** уровни опыта, описанные в этом учебнике, полезны для анализа отклика, анимации и этапов простоя страницы.  

<!--todo: add rail link when section is ready -->  

## Get started  

В следующем учебнике вы откроете DevTools на реальной странице и с помощью панели " **производительность** " найдите узкое место на странице.  

1.  Откройте Microsoft EDGE в **режиме InPrivate**.  Режим InPrivate обеспечивает выполнение Microsoft EDGE в чистом состоянии.  Например, если на вашем компьютере установлено большое количество расширений, эти расширения могут создать шум в измерениях производительности.  
    
    <!--TODO: replace section when updated for new Edge  -->
    
1.  Загрузите следующую страницу в окне InPrivate.  Страница — это демонстрационный ролик, который вы собираетесь профилировать.  На странице показан ряд маленьких значков, перемещаясь вверх и вниз.  
    
    ```https
    https://microsoft-edge-chromium-devtools.glitch.me/sluggish/
    ```  
    
1.  Выберите `Control` + `Shift` + `I` \ (Windows \) или `Command` + `Option` + `I` \ (macOS \), чтобы открыть DevTools.  
    
    :::image type="complex" source="../media/evaluate-performance-get-started-side-by-side.msft.png" alt-text="Демонстрация слева и DevTools справа" lightbox="../media/evaluate-performance-get-started-side-by-side.msft.png":::
       Демонстрация слева и DevTools справа  
    :::image-end:::  
    
    > [!NOTE]
    > В остальных рисунках DevTools [отсоединяется в отдельном окне][DevtoolsCustomizePlacement] , чтобы лучше сосредоточиться на содержимом.  
    
### Имитация мобильного ЦП  

На мобильных устройствах больше энергии ЦП, чем на настольных компьютерах и ноутбуках.  Каждый раз, когда вы профилем страницы, используйте метод регулирования ЦП для моделирования того, как страница работает на мобильных устройствах.  

1.  В DevTools выберите вкладку **Performance (производительность** ).  
1.  Убедитесь, что флажок **снимки экрана** включен.  
1.  Выберите **Параметры захвата** \ (! [ Параметры захвата] [ImageCaptureSettingsIcon] \).  DevTools показывает параметры, связанные с тем, как они захватывают метрики производительности.  
1.  На вкладке **ЦП**выберите пункт **замедление 4X**.  DevTools загружает ЦП так, чтобы он был 4 медленнее, чем обычно.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-capture-settings.msft.png" alt-text="Демонстрация слева и DevTools справа" lightbox="../media/evaluate-performance-performance-capture-settings.msft.png":::
       Интервал регулирования ЦП  
    :::image-end:::  
    
    > [!NOTE]
    > При тестировании других страниц; Если вы хотите, чтобы каждая страница хорошо работала на мобильных устройствах с низким интерфейсом, установите для ускорения ЦП **6X**скорость.  Демонстрационный ролик не работает с 6xем замедления, поэтому он просто использует 4X для целей.  
    
### Настройка ролика  

Очень сложно создать демонстрацию производительности во время выполнения, который постоянно подходит для всех читателей веб-сайта.  В следующем разделе описано, как настроить демонстрацию, чтобы убедиться в том, что взаимодействие между снимками экрана и описаниями не зависит от конкретной настройки.

1.  Нажмите кнопку " **Добавить 10** ", чтобы синий значок не перемещался заметно медленнее.  На высоком уровне компьютера вы можете выбрать его в течение 20 появлений.  
1.  Нажмите кнопку **оптимизировать**.  Синие значки должны двигаться быстрее и более гладко.  
    
    > [!NOTE]
    > Для лучшего отображения различий между оптимизированными и неоптимизированными версиями нажмите кнопку " **вычесть 10** " несколько раз, а затем повторите попытку.  
    > Если вы добавите слишком много синих значков, вы можете получить максимум ресурсов ЦП, и вы можете не заметить существенных различий в результатах двух версий.  
    
1.  Нажмите **Отмена оптимизации**.  Синие значки перемещаются медленнее и с более низкой скоростью.  
    
### Запись производительности среды выполнения  

Когда вы запустили оптимизированную версию страницы, синие значки перемещаются быстрее.  Почему так?  Обе версии предназначены для того, чтобы переместить значки в одинаковые промежутки времени.  Чтобы выяснить, как выявить узкие места производительности в неоптимизированной версии, сделайте запись на панели производительности.  

1.  В DevTools выберите **запись** \ (! [ Record] [ImageRecordIcon] \).  DevTools захватывает метрики производительности по мере выполнения страницы.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-profiling.msft.png" alt-text="Демонстрация слева и DevTools справа" lightbox="../media/evaluate-performance-performance-profiling.msft.png":::
       Профилирование страницы  
    :::image-end:::  
    
1.  Подождите несколько секунд.  
1.  Нажмите кнопку **остановить**.  DevTools останавливает запись, обрабатывает данные, а затем отображает результаты на панели Performance.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-capture-results.msft.png" alt-text="Демонстрация слева и DevTools справа" lightbox="../media/evaluate-performance-performance-capture-results.msft.png":::
       Результаты профиля  
    :::image-end:::  
    
Wow, это является большим объемом данных.  не беспокойтесь, в скором времени процесс становится более понятным.  

## Анализ результатов  

После того как вы зарегистрируете производительность страницы, измерьте качество ее функционирования и получите все причины.  

### Анализ кадров в секунду  

Основная метрика для измерения производительности любой анимации — число кадров в секунду с повтором (кадр/с).  Пользователи будут рады, что анимации работают в 60 кадр/с.  

1.  Посмотрите на диаграмму в **кадре** .  Если вы видите красную полосу над **кадром кадров**, это означает, что частота кадров, отброшенных таким образом, что она может повредить взаимодействие с пользователем.  Как правило, чем больше зеленая полоса, тем выше кадр кадров.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-fps-chart.msft.png" alt-text="Демонстрация слева и DevTools справа" lightbox="../media/evaluate-performance-performance-fps-chart.msft.png":::
       Диаграмма **кадр/** с  
    :::image-end:::  
    
1.  Под диаграммой с **кадром кадров** вы видите диаграмму **ЦП** .  Цвета на диаграмме **ЦП** соответствуют цветам на вкладке " **Сводка** " в нижней части панели "производительность".  Тот факт, что диаграмма **ЦП** заполнена цветом, означает, что ЦП был maxed во время записи.  Всякий раз, когда вы видите maxed ЦП в течение длительного времени, это подсказка для поиска способов уменьшения объема работы.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-cpu-chart.msft.png" alt-text="Демонстрация слева и DevTools справа" lightbox="../media/evaluate-performance-performance-cpu-chart.msft.png":::
       Вкладка "Диаграмма **ЦП** " и " **Сводка** "  
    :::image-end:::  
    
1.  Наведите указатель мыши на диаграммы **кадров**, **ЦП**или **нетто** .  В DevTools показан снимок страницы на данный момент времени.  Чтобы воспроизвести запись, передвиньте указатель влево и вправо.  Действие, на которое указывает ссылка, используется как элемент очистки, и его можно использовать для анализа хода анимации вручную.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-screenshot-hover.msft.png" alt-text="Демонстрация слева и DevTools справа" lightbox="../media/evaluate-performance-performance-screenshot-hover.msft.png":::
       Просмотр снимка страницы в 2500ms отметке записи  
    :::image-end:::  
    
1.  В разделе **кадры** наведите указатель мыши на один из зеленых квадратиков.  DevTools показывает, что этот конкретный кадр находится в кадре/сек.  Скорее всего, каждый кадр расположен ниже целевого числа 60 кадр/с.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-frame-hover.msft.png" alt-text="Демонстрация слева и DevTools справа" lightbox="../media/evaluate-performance-performance-frame-hover.msft.png":::
       Наведение указателя мыши на рамку  
    :::image-end:::  
    
Разумеется, вы увидите, что страница не работает должным образом.  Но в реальных сценариях это может быть не так понятно, так что все средства, позволяющие делать измерения, будут полезны.  

#### Премия: открытие индикатора кадров  

Еще одним удобным инструментом является индикатор между КАДРами, который обеспечивает оценки в реальном времени при выполнении страницы.  

1.  Выберите `Control` + `Shift` + `P` \ (Windows \) или `Command` + `Shift` + `P` \ (macOS \), чтобы открыть **меню команд**.  
1.  Начните вводить текст `Rendering` в **меню команд** и выберите пункт **Показать отрисовку**.  
1.  На вкладке " **рендеринг** " Включите **индикатор кадров**.  В правом верхнем углу окна просмотра появится новая наложение.  
    
    :::image type="complex" source="../media/evaluate-performance-fps-meter-overlay.msft.png" alt-text="Демонстрация слева и DevTools справа" lightbox="../media/evaluate-performance-fps-meter-overlay.msft.png":::
       **Индикатор кадров в кадре**  
        :::image-end:::  
    
1.  Отключите **индикатор кадров** и щелкните `Escape` , чтобы закрыть вкладку **Отображение** .  В этом учебнике не используется **индикатор в кадре** .  
    
### Определение узкого места  

После того как вы зайдете и проверите, что анимация не работает, следующий шаг — ответить на вопрос "Зачем?".  

1.  Если не выбрано ни одного события, на вкладке **Сводка** показана разбивка действий.  Страница потратила большую часть времени на отрисовку.  Так как производительность — это изображение, которое уменьшает трудозатраты, цель состоит в том, чтобы уменьшить время, затраченное на обработку результатов.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-summary-tab.msft.png" alt-text="Демонстрация слева и DevTools справа" lightbox="../media/evaluate-performance-performance-summary-tab.msft.png":::
       Вкладка " **Сводка** "  
    :::image-end:::  
    
1.  Разверните раздел **основной** .  DevTools показывает flameную диаграмму активности в главном потоке с течением времени.  С течением времени ось x представляет запись.  Каждая строка представляет событие.  Более широкий отрезок означает, что событие занимает больше времени.  Ось y представляет стек вызова.  Если вы видите события, наложенные друг на друга, это означает, что события верхнего уровня приводили к появлению младших событий.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-main.msft.png" alt-text="Демонстрация слева и DevTools справа" lightbox="../media/evaluate-performance-performance-main.msft.png":::
       **Основной** раздел  
    :::image-end:::  
    
1.  В записи много данных.  Изменение масштаба одного события; Выберите, удерживайте и наведите указатель мыши на **Обзор**, который включает в себя раздел с диаграммами в **кадрах**, **ЦП**и **сети** .  В **главном** разделе и на вкладке " **Сводка** " отображаются только сведения о выбранной части записи.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-main-zoomed.msft.png" alt-text="Демонстрация слева и DevTools справа" lightbox="../media/evaluate-performance-performance-main-zoomed.msft.png":::
       Изменение размера события  
    :::image-end:::  
    
    > [!NOTE]
    > Кроме того, можно изменить масштаб, сосредоточиться на **главном** разделе, выбрать фоновый рисунок или событие, а затем выбрать `W` , `A` , `S` или `D` .  
    
    1.  Сосредоточьтесь на красном треугольнике в правой верхней части события **анимации Frame, которое активировалось** .  Если вы видите красный треугольник, это предупреждение может быть связано с проблемой, связанной с событием.  
    
    > [!NOTE]
    > Событие **анимации Frame срабатывает** при каждом запуске [ `requestAnimationFrame()` обратного вызова][MDNWebRequestAnimationFrame] .  
    
1.  Выберите событие **кадр анимации, которое активировалось** .  На вкладке **Сводка** теперь отображаются сведения об этом событии.  Обратите внимание на ссылку " **Показать** ".  После того как вы выберете его, DevTools выделит событие, которое инициировало событие **кадра анимации** .  Кроме того, обратите внимание на ссылку **app.js:95** .  После того как вы выберете его, отобразится соответствующая строка исходного кода.
    
    :::image type="complex" source="../media/evaluate-performance-performance-animation-frame-fired.msft.png" alt-text="Демонстрация слева и DevTools справа" lightbox="../media/evaluate-performance-performance-animation-frame-fired.msft.png":::
       Дополнительные сведения о событии **анимации запускаемого кадра**  
    :::image-end:::  
    
    > [!NOTE]
    > После выбора события с помощью клавиш со стрелками выберите события рядом с ним.  
    
1.  В рамках события **app. Update** существует множество фиолетовых событий.  Если каждое фиолетовое событие было расширено, оно выглядит так, как будто каждый из них может иметь красный треугольник.  
1.  Выберите одно из фиолетовых событий **макета** .  DevTools предоставляет дополнительные сведения о событии на вкладке " **Сводка** ".  В действительности есть предупреждение о принудительном передвижении \ (другое слово для макета \).  
    
1.  На вкладке **Сводка** щелкните ссылку **app.js:71** в разделе **Макет принудительно**.  DevTools перенесет вас в строку кода, которая замещает макет.  
    
    :::image type="complex" source="../media/evaluate-performance-sources-app-update.msft.png" alt-text="Демонстрация слева и DevTools справа" lightbox="../media/evaluate-performance-sources-app-update.msft.png":::
       Строка кода, вызвавшая принудительный макет.  
    :::image-end:::  
    
    > [!NOTE]
    > Проблема с кодом состоит в том, что в каждом кадре анимации каждый из них изменяет стиль каждого значка, а затем запрашивает расположение каждого значка на странице.  Поскольку стили изменились, браузер не может определить, изменилось ли положение каждого значка, поэтому для вычисления нового положения необходимо изменить макет значка.  <!--  > See [Avoid forced synchronous layouts][RenderingAvoidSynchronousLayouts] to learn more.  -->
    
<!-- todo: add layouts section when available -->

Это было очень мало для обучения.  Теперь у вас есть надежная основа базового рабочего процесса для анализа производительности среды выполнения.  Молодец.  

### Премия: анализ оптимизированной версии  

Используй рабочие процессы и инструменты, которые вы только что узнали, нажмите кнопку **оптимизировать** на демонстрационной версии, чтобы включить оптимизированный код, а затем выберите другую запись и проанализируйте результаты.  С улучшенной частотой кадров, направленной на сокращение событий в диаграмме Flame в **главном** разделе, вы можете видеть, что оптимизированная версия приложения работает гораздо меньше усилий, что повышает производительность.  

> [!NOTE]
> Даже оптимизированная версия не имеет ничего удобного, так как она управляет `top` свойством каждого значка.  Лучший подход — придерживаться свойств, которые влияют только на композицию.  <!--  > See [Use transform and opacity changes for animations][RenderingCompositor] for more information.  -->  

<!--todo: add rendering section when available -->

## Дальнейшие действия

<!--The foundation for understanding performance is the RAIL model.  The RAIL model teaches you the performance metrics that are most important to your users.  
See [Measure Performance With The RAIL Model][RAIL] to learn more.  -->  

Для более удобного функционирования с помощью панели "производительность" лучше всего сделать это.  Попробуйте выполнить профилирование страниц и проанализировать результаты.  Если у вас возникли вопросы по поводу ваших результатов, используйте значок **Отправить отзыв** , выберите `Alt` + `Shift` + `I` \ (Windows \), выберите `Option` + `Shift` + `I` \ (macOS \) или [твит в группу DevTools][TwitterEdgeDevtools].  Включите снимки экрана или ссылки на воспроизводимые страницы, если это возможно.  

:::image type="complex" source="../media/evaluate-performance-feedback-icon.msft.png" alt-text="Демонстрация слева и DevTools справа" lightbox="../media/evaluate-performance-feedback-icon.msft.png":::
   Значок " **Отправить отзыв** " в Microsoft Edge DevTools  
:::image-end:::  

<!-- To really become an expert in runtime performance, you must learn how the browser translates HTML, CSS, and JS into pixels on a screen.  The best place to start is the [Rendering Performance Overview][RenderingPerformance].  [The Anatomy Of A Frame][FrameAnatomy] dives into even more detail.  -->  

Наконец, существует множество способов улучшить производительность во время выполнения.  В этой статье рассказывается о узком узким местах анимации, чтобы дать вам сфокусированный обзор на панели производительности, но это лишь один из многих узких мест.  <!--  The rest of the Rendering Performance series has a lot of good tips for improving various aspects of runtime performance, such as:  -->

<!--
*   [Optimizing JS Execution][RenderingOptimizeJS]  
*   [Reduce The Scope And Complexity Of Style Calculations][RenderingReduceScope]  
*   [Avoid Large, Complex Layouts And Layout Thrashing][RenderingAvoidThrashing]  
*   [Simplify Paint Complexity And Reduce Paint Areas][RenderingSimplifyPaint]  
*   [Stick To Compositor-Only Properties And Manage Layer Count][RenderingManageLayers]  
*   [Debounce Your Input Handlers][RenderingDebounceInputs]  
-->

<!-- links -->

[DevtoolsCustomizePlacement]: ../customize/placement.md "Изменение положения DevTools Microsoft EDGE (Отстыковка, закрепить в нижней части, закрепить слева)"  
[DevtoolsSpeedGetStarted]: ../speed/get-started.md "Оптимизация скорости веб-сайта с помощью Microsoft Edge DevTools"  

[TwitterEdgeDevtools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "EdgeDevTools-опубликовать твит | Контента"  

[MDNWebRequestAnimationFrame]: https://developer.mozilla.org/docs/Web/API/window/requestAnimationFrame "Window. requestAnimationFrame \ (\) | MDN"  

<!--[InPrivate]: https://support.microsoft.com/help/4026200/microsoft-edge-browse-inprivate "Browse InPrivate in Microsoft Edge"  -->

<!--[FrameAnatomy]: https://aerotwist.com/blog/the-anatomy-of-a-frame  -->  

<!--[RAIL]: /web/fundamentals/performance/rail  -->  
<!--[RenderingAvoidSynchronousLayouts]: /web/fundamentals/performance/rendering/avoid-large-complex-layouts-and-layout-thrashing#avoid_forced_synchronous_layouts  -->  
<!--[RenderingAvoidThrashing]: /web/fundamentals/performance/rendering/avoid-large-complex-layouts-and-layout-thrashing  -->  
<!--[RenderingCompositor]: /web/fundamentals/performance/rendering/stick-to-compositor-only-properties-and-manage-layer-count#use_transform_and_opacity_changes_for_animations  -->  
<!--[RenderingDebounceInputs]: /web/fundamentals/performance/rendering/debounce-your-input-handlers  -->
<!--[RenderingManageLayers]: /web/fundamentals/performance/rendering/stick-to-compositor-only-properties-and-manage-layer-count  -->  
<!--[RenderingOptimizeJS]: /web/fundamentals/performance/rendering/optimize-javascript-execution  -->  
<!--[RenderingPerformance]: /web/fundamentals/performance/rendering  -->  
<!--[RenderingReduceScope]: /web/fundamentals/performance/rendering/reduce-the-scope-and-complexity-of-style-calculations  -->  
<!--[RenderingSimplifyPaint]: /web/fundamentals/performance/rendering/simplify-paint-complexity-and-reduce-paint-areas  -->  

<!--[StackOverflowAlphabetBrowserDevtools]: https://stackoverflow.com/questions/ask?tags=alphabet-browser-devtools "Alphabet Browser - Stack Overflow"  -->  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/index) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
