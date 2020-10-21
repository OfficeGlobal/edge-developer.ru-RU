---
description: Ссылки на все способы записи и анализа производительности в Microsoft Edge DevTools.
title: Справочные материалы по анализу производительности
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: d135f83273842a1e128df0bb346f0f126e2fbe8d
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125141"
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

# Справочные материалы по анализу производительности  

На этой странице представлен полный справочник по функциям Microsoft Edge DevTools, относящимися к анализу производительности.  

Перейдите в раздел [Приступая к анализу производительности среды выполнения][DevtoolsEvaluatePerformanceGettingStarted] для учебного руководства по анализу производительности страницы с помощью [Microsoft Edge DevTools][MicrosoftEdgeDevTools].  

## Запись производительности  

### Запись производительности среды выполнения  

Записывайте производительность во время выполнения, когда необходимо проанализировать производительность страницы по мере ее выполнения, а не загрузку.  

1.  Перейдите на страницу, которую вы хотите проанализировать.  
1.  Откройте вкладку **производительность** в DevTools.  
1.  Выберите **запись** \ ( ![ значок записи ][ImageRecordIcon] \).  
    
    :::image type="complex" source="../media/evaluate-performance-performance-record-highlight.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-record-highlight.msft.png":::
       **Record**  
    :::image-end:::  
    
1.  Взаимодействие со страницей.  DevTools записывает все действия страниц, которые выполняются в результате взаимодействия.  
1.  Нажмите кнопку " **запись** " еще раз или кнопку " **остановить** ", чтобы остановить запись.  
    
### Скорость загрузки записей  

Запишите производительность загрузки, когда необходимо проанализировать производительность страницы при ее загрузке, а не на выполнение.  

1.  Перейдите на страницу, которую вы хотите проанализировать.  
1.  Откройте панель " **производительность** " DevTools.  
1.  Нажмите кнопку **обновить страницу** \ ( ![ обновить страницу ][ImageRefreshPageIcon] \).  DevTools записывает метрики производительности во время обновления страницы, а затем автоматически останавливает запись спустя пару секунд после завершения загрузки.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-refresh-button.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-refresh-button.msft.png":::
       **Обновить страницу**  
    :::image-end:::  
    
DevTools автоматически масштабирует часть записи, в которой возникло большинство действий.  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-refreshed.msft.png":::
   Запись загрузки страницы  
:::image-end:::  

### Снимки экрана при записи  

Установите флажок **снимки экрана** , чтобы зафиксировать снимок экрана для каждого кадра во время записи.  

:::image type="complex" source="../media/evaluate-performance-performance-capture-screenshots-checkbox.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-capture-screenshots-checkbox.msft.png":::
   Флажок " **снимки экрана** "  
:::image-end:::  

Перейдите к разделу [Просмотр снимка экрана](#view-a-screenshot) , чтобы узнать, как работать с экранными снимками.  

### Принудительная сборка мусора во время записи  

Во время записи страницы выберите команду **собрать мусора** \ ( ![ собрать значок мусора ][ImageCollectGarbageIcon] \), чтобы принудительно инициировать сбор мусора.  

:::image type="complex" source="../media/evaluate-performance-performance-collect-garbage-button.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-collect-garbage-button.msft.png":::
   Сбор мусора  
:::image-end:::  

### Показать параметры записи  

Выберите **Параметры захвата** \ ( ![ Параметры захвата ][ImageCaptureSettingsIcon] ), чтобы предоставить доступ к дополнительным параметрам, связанным с тем, как DevTools захватывает записи производительности.  

:::image type="complex" source="../media/evaluate-performance-performance-capture-settings-button-open-drawer.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-capture-settings-button-open-drawer.msft.png":::
   Раздел " **Параметры захвата** "  
:::image-end:::  

### Отключение примеров JavaScript  

По умолчанию **основной** раздел записи содержит подробные стеки вызовов функций JavaScript, которые были вызваны во время записи.  Чтобы отключить эти стеки звонков, выполните указанные ниже действия.  

1.  Открытие меню " **Параметры захвата** ".  Перейдите к разделу [Отображение параметров записи](#show-recording-settings).  
1.  Установите флажок **Отключить образцы JavaScript** .  
1.  Запишите страницу.  
    
На следующих двух рисунках показана разница между отключением и включением образцов JavaScript.  **Основной** раздел записи становится более коротким, так как выборка отключена, так как при этом не будут выпускаться все стеки вызовов JavaScript.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-on.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-on.msft.png":::
         Пример записи при отключенных примерах JS  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off.msft.png":::
         Пример записи при включенных примерах JS  
      :::image-end:::  
   :::column-end:::
:::row-end:::

### Регулирование сети во время записи  

Чтобы перерегулировать сеть при записи, выполните указанные ниже действия.  

1.  Открытие меню " **Параметры захвата** ".  Перейдите к разделу [Отображение параметров записи](#show-recording-settings).  
1.  Настройте **сеть** для нужного уровня регулирования.  
    
### Регулирование ЦП во время записи  

Чтобы перерегулировать ЦП во время записи, выполните указанные ниже действия.  

1.  Открытие меню " **Параметры захвата** ".  Перейдите к разделу [Отображение параметров записи](#show-recording-settings).  
1.  Установите для **ЦП** требуемый уровень регулирования.  
    
Регулирование производится относительно возможностей компьютера.  Например, параметр "интервал по **промедлению** " обеспечивает работу ЦП 2 раза ниже обычного.  DevTools не имитируют процессоры мобильных устройств, так как архитектура мобильных устройств значительно отличается от настольных компьютеров и ноутбуков.  

### Включение расширенного инструментария рисования  

Чтобы просмотреть подробные инструменты для рисования, выполните указанные ниже действия.  

1.  Открытие меню " **Параметры захвата** ".  Перейдите к разделу [Отображение параметров записи](#show-recording-settings).  
1.  Установите флажок **включить дополнительные возможности инструментирования краски (медленно)** .  

Чтобы узнать, как взаимодействовать с данными краски, перейдите к разделу [Просмотр слоев](#view-layers-information) и [профилировщика Paint](#view-paint-profiler).  

## Сохранение записи  

Чтобы сохранить запись, щелкните ее правой кнопкой мыши и выберите команду **Сохранить профиль**.  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-save-profile.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-save-profile.msft.png":::
   **Сохранить профиль**  
:::image-end:::  

## Загрузка записи  

Чтобы загрузить запись, щелкните ее правой кнопкой мыши и выберите команду " **загрузить профиль**".  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-load-profile.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-load-profile.msft.png":::
   **Загрузить профиль**  
:::image-end:::  

## Удаление предыдущей записи  

После внесения записи нажмите **Очистить запись** \ ( ![ снимите значок записи ][ImageClearRecordingIcon] \), чтобы очистить эту запись на панели " **производительность** ".  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-clear-button.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-clear-button.msft.png":::
   **Очистка записи**  
:::image-end:::  

## Анализ записи производительности  

После того как вы [зарегистрируете производительность во время выполнения](#record-runtime-performance) или [скорость загрузки записи](#record-load-performance), на панели **производительности** можно получить большое количество данных для анализа производительности.  

### Выбор части записи  

Чтобы выделить часть записи, перетащите указатель мыши по левому или правому краю **обзора** .  **Обзор** — это раздел, содержащий диаграммы в **кадрах**, **ЦП**и **сети** .  

:::image type="complex" source="../media/evaluate-performance-performance-zoom-highlighted.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-zoom-highlighted.msft.png":::
   Перетащите указатель мыши по **обзору** , чтобы увеличить масштаб  
:::image-end:::  

Чтобы выбрать часть с помощью клавиатуры, выполните указанные ниже действия.  

1.  Щелкните фон **основного** раздела или любой раздел рядом с ним, например **взаимодействия**, **сеть**или **графический процессор**.  Этот рабочий процесс клавиатуры работает только в том случае, если в фокусе находится один из этих разделов.  
1.  С помощью `W` клавиш,, `A` `S` ,, `D` клавиши для увеличения, перемещения влево, уменьшения и перемещения вправо соответственно.  

Чтобы выбрать часть с помощью сенсорной панели, выполните указанные ниже действия.  

1.  Наведите указатель мыши на раздел **Общие сведения** или на раздел **сведения** .  Раздел **Обзор** — это область, содержащая диаграммы в **кадрах**, **ЦП**и **сети** .  Раздел " **сведения** " — это область, содержащая **основной** раздел, раздел " **взаимодействия** " и т. д.  
1.  С помощью двух пальцев проведите пальцем вверх, проведите пальцем влево, чтобы переместить влево, проведите пальцем вниз, чтобы увеличить масштаб, и проведите пальцем вправо, чтобы перейти вправо.  

Для прокрутки длинной Flame диаграммы в **главном** разделе или любом из соседей щелкните и удерживайте клавишу во время перетаскивания вверх и вниз.  Чтобы переместить выделенную часть записи, перетащите левую и правую клавишу.  

### Поиск действий  

Выберите `Control` + `F` \ (Windows, Linux \) или `Command` + `F` \ (macOS \), чтобы открыть поле поиска в нижней части панели " **производительность** ".  

:::image type="complex" source="../media/evaluate-performance-performance-search-regex.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-search-regex.msft.png":::
   Поле поиска  
:::image-end:::  

Чтобы перейти к действиям, которые соответствуют запросу, выполните указанные ниже действия.  

*   Используйте кнопки **назад** ( ![ предыдущее ][ImagePreviousIcon] ) и **Далее** \ ( ![ Далее ][ImageNextIcon] \).  
*   Выбор `Shift` + `Enter` предыдущего или `Enter` для выбора следующего.  

Чтобы изменить параметры запроса, выполните указанные ниже действия.  

*   Нажмите клавишу **с учетом регистра** \ (с ![ учетом регистра ][ImageSearchCaseIcon] ), чтобы сделать запрос чувствительным к регистру.  
*   Нажмите **регулярные** выражения \ ( ![ Regex ][ImageSearchRegexIcon] \), чтобы использовать регулярное выражение в запросе.  

Чтобы скрыть поле поиска, нажмите кнопку **Отмена**.  

### Просмотр основного действия потока  

Используйте **главный** раздел для просмотра действий, которые произошли в основном потоке страницы.  

:::image type="complex" source="../media/evaluate-performance-performance-main-zoomed.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-main-zoomed.msft.png":::
   **Основной** раздел  
:::image-end:::  

Щелкните событие, чтобы просмотреть дополнительные сведения о нем на вкладке **Сводка** .  DevTools выделеет выбранное событие.  

:::image type="complex" source="../media/evaluate-performance-performance-summary-me.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-summary-me.msft.png":::
   Дополнительные сведения о `anonymous` функции на вкладке " **Сводка** "  
:::image-end:::  

DevTools представляет главную активность потока с Flame диаграммой.  Ось x обозначает запись с течением времени.  Ось y представляет стек вызова.  Событие Top приводит к возникновению событий, указанных ниже.  

:::image type="complex" source="../media/evaluate-performance-performance-main-flame-chart.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-main-flame-chart.msft.png":::
   Flame диаграмма  
:::image-end:::  

На предыдущем рисунке `click` событие вызвало `Function Call` в `activitytabs.js` строке 53.  Ниже `Function Call` показано, что была вызвана анонимная функция.  Анонимная функция, вызываемая, которая вызывается `a` `wait` `Minor GC` .  

DevTools назначает сценарии случайные цвета.  На предыдущем рисунке вызовы функций из одного сценария окрашены в зеленый цвет.  Вызов из другого сценария имеет цветный бежевый.  Темным желтым обозначенными действиями в сценариях, а фиолетовые — действия отрисовки.  Эти темные желтые и фиолетовые события будут согласованы во всех записях.  

Перейдите к разделу [Отключение примеров JavaScript](#disable-javascript-samples) , если вы хотите скрыть подробную flameную диаграмму вызовов JavaScript.  При отключенных примерах JS отображаются только события высокого уровня, такие как `Event: click` и на `Function Call` предыдущем рисунке.  

### Просмотр действий в таблице  

После записи страницы, чтобы проанализировать действия, не нужно полагаться только на **основной** раздел.  DevTools также предоставляет три табличных представления для анализа действий.  Каждое представление предлагает различные варианты действий:  

*   Если вы хотите просмотреть корневые действия, которые приводят к большинству работ, используйте [вкладку "дерево вызовов"](#the-call-tree-tab).  
*   Если вы хотите просмотреть действия, в которых больше всего затрачено время, используйте [вкладку "Bottom-Up"](#the-bottom-up-tab).  
*   Если вы хотите просмотреть действия в том порядке, в котором они были обнаружены во время записи, используйте [вкладку Журнал событий](#the-event-log-tab).  
    
> [!NOTE]
> Следующие три раздела относятся к одной и той же демонстрации.  Запустите демонстрацию самостоятельно на [вкладке "действия" демонстрации][ActivityTabsDemo].  

#### Корневые действия  

Ниже приведено описание концепции **корневых действий** , упомянутой на вкладке " **дерево вызовов** ", вкладке " **снизу вверх** " и в разделе " **журнал событий** ".  

Корневые действия — это те, которые приводят к тому, что браузер выполняет определенную работу.  Например, при щелчке страницы браузер запускает `Event` действие в качестве корневого действия.  Это `Event` может привести к запуску обработчика и т. д.  

В диаграмме Flame **основного** раздела корневые действия находятся в верхней части диаграммы.  В **дереве вызовов** и на вкладках **журнал событий** корневые действия — это элементы верхнего уровня.  

Перейдите на [вкладку "дерево вызовов"](#the-call-tree-tab) для примера корневых действий.  

#### Вкладка "дерево вызовов"  

С помощью вкладки " **дерево вызовов** " можно просмотреть, какие [корневые действия](#root-activities) приводят к наибольшему работоспособности.  

На вкладке " **дерево вызовов** " отображаются только действия в выбранной части записи.  Перейдите к [разделу](#select-a-portion-of-a-recording) , в котором вы можете выбрать части записи.  

:::image type="complex" source="../media/evaluate-performance-performance-call-tree.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-call-tree.msft.png":::
   Вкладка " **дерево вызовов** "  
:::image-end:::  

На приведенном выше рисунке сверху находятся элементы в столбце " **действия** ", `Evaluate Script` а также `Parse HTML` корневые действия.  Вложенный объект представляет стек вызова.  Например, на предыдущем рисунке, `Parse HTML` вызвавшем `Evaluate Script` причины `Compile Script` и `(anonymous)` .  

**Собственное время** — это время, которое прямо затрачено на это действие.  **Общее время** представляет время, затраченное на выполнение этого мероприятия или любого из дочерних элементов.  

Выберите **свое время**, **Общее время**или **активность** , чтобы отсортировать таблицу по этому столбцу.  

Используйте текстовое поле " **Фильтр** " для фильтрации событий по имени действия.  

По умолчанию для меню **Группировка** выбрано значение **Нет группировки**.  Используйте меню **Группировка** для сортировки таблицы действий на основе различных условий.  

Выберите пункт **Показать наиболее тяжелую стопку** ![ ][ImageShowHeaviestStackIcon] , чтобы отобразить другую таблицу справа от таблицы " **действия** ".  Щелкните действие, чтобы заполнить таблицу с самым **максимальным** .  В таблице наиболее **плотного стека** показано, какие дочерние элементы выбранного действия занимали наибольшее время.  

#### Вкладка "Bottom-Up"  

С помощью вкладки " **снизу вверх** " можно просмотреть, какие действия немедленно потратили на общее время в агрегате.  

На вкладке " **снизу вверх** " отображаются только действия в выбранной части записи.  Перейдите к [разделу](#select-a-portion-of-a-recording) , в котором вы можете выбрать части записи.  

:::image type="complex" source="../media/evaluate-performance-performance-bottoms-up.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-bottoms-up.msft.png":::
   Вкладка " **снизу вверх** "  
:::image-end:::  

В разделе **основной** Flame диаграмма предыдущего рисунка перейдите к нему практически практически все время, затраченное на выполнение `Parse HTML` .  Верхнее действие на вкладке " **снизу вверх** " на предыдущем рисунке `Parse HTML` .  <!--In the flame chart of the previous figure, the yellow below the calls to `wait` are actually thousands of `Minor GC` calls.  -->  Перейдите на вкладку **снизу вверх** , и вы можете выполнить следующее очень дорогостоящее действие `Layout` .  

Столбец " **собственное время** " представляет агрегированное время, проведенное непосредственно в этом действии, для всех вхождений.  

Столбец " **Общее время** " представляет объединенное время, затраченное на это действие или любые дочерние элементы.  

#### Вкладка "журнал событий"  

Используйте вкладку **журнал событий** , чтобы просмотреть действия в том порядке, в котором они были обнаружены во время записи.  

На вкладке **журнал событий** отображаются только действия в выбранной части записи.  Перейдите к [разделу](#select-a-portion-of-a-recording) , в котором вы можете выбрать части записи.  

:::image type="complex" source="../media/evaluate-performance-performance-event-log.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-event-log.msft.png":::
   Вкладка " **журнал событий** "  
:::image-end:::  

Столбец " **время начала** " представляет точку, в которой началось действие, относительно начала записи.  Например, время начала `175.7 ms` для выделенного элемента на предыдущем рисунке означает, что действие началось 175,7 MS после начала записи.  

Столбец " **собственное время** " представляет время, затраченное непосредственно на это действие.  

Столбцы « **Общее время** » обозначают время, затраченное непосредственно на это действие или в любой из дочерних элементов.  

Выберите **время начала**, **собственное время**или **Общее время** для сортировки таблицы по этому столбцу.

Используйте текстовое поле **Фильтр** , чтобы отфильтровать действия по имени.  

С помощью меню " **Длительность** " можно отфильтровать все действия, которые заняли менее 1 мс или 15 мс.  По умолчанию для меню **Duration** задано значение **все**, что означает, что отображаются все действия.  

Отключите флажки " **Загрузка**", " **Создание сценариев**", " **Подготовка**" и " **раскраска** ", чтобы отфильтровать все действия из этих категорий.  

### Просмотр действий GPU  

Просматривайте активность GPU в разделе **GPU** .  

:::image type="complex" source="../media/evaluate-performance-performance-gpu-zoomed.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-gpu-zoomed.msft.png":::
   Раздел **GPU**  
:::image-end:::  

### Просмотр растровых операций  

Просматривайте растровые действия в разделе " **растр** ".  

:::image type="complex" source="../media/evaluate-performance-performance-raster.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-raster.msft.png":::
   **Разточечный** раздел  
:::image-end:::  

### Просмотр взаимодействия  

В разделе " **взаимодействия** " можно найти и проанализировать взаимодействие с пользователями, произошедшие во время записи.  

:::image type="complex" source="../media/evaluate-performance-performance-interactions-animation.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-interactions-animation.msft.png":::
   Раздел " **взаимодействия** "  
:::image-end:::  

Красная линия в нижней части взаимодействия представляет время, затраченное на ожидание основного потока.  

Щелкните взаимодействие, чтобы просмотреть дополнительные сведения о нем на вкладке **Сводка** .  

### Анализ кадров в секунду (кадр/с)  

DevTools предлагает многочисленные способы анализа кадров в секунду.  

*   Используйте [диаграмму в кадре](#the-fps-chart) , чтобы получить обзор кадров в кадре в течение не более чем на продолжительность записи.  
*   С помощью [раздела кадры](#the-frames-section) вы можете узнать, сколько времени занимает определенный кадр.  
*   Используйте **индикатор кадров между кадрами** для оценки в режиме реального времени при выполнении страницы.  Переход к [просмотру кадров в секунду в режиме реального времени с индикатором кадров](#view-frames-per-second-in-realtime-with-the-fps-meter).  
    
#### Диаграмма кадр/с  

Диаграмма **кадр/** с — это обзор частоты кадров во время записи.  Как правило, чем больше зеленая полоса, тем выше частота кадров.  

Красная черта над диаграммой с индикатором **кадров** — это предупреждение о том, что частота кадров отброшена настолько, что она может повредить взаимодействие с пользователем.  

:::image type="complex" source="../media/evaluate-performance-performance-fps-highlight.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-fps-highlight.msft.png":::
   Диаграмма **кадр/** с  
:::image-end:::  

#### Раздел "кадры"  

Раздел **кадры** содержит сведения о том, сколько времени занимает определенный кадр.  

Наведите указатель мыши на кадр, чтобы просмотреть всплывающую подсказку с дополнительными сведениями.  

:::image type="complex" source="../media/evaluate-performance-performance-frames-hover.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-frames-hover.msft.png":::
   Наведение указателя мыши на рамку  
:::image-end:::  

Щелкните рамку, чтобы просмотреть дополнительные сведения о кадре на вкладке " **Сводка** ".  DevTools выделеет выделенный кадр синим цветом.  

:::image type="complex" source="../media/evaluate-performance-performance-frames-summary.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-frames-summary.msft.png":::
   Просмотр кадра на вкладке " **Сводка** "  
:::image-end:::  

### Просмотр сетевых запросов  

Разверните раздел **сеть** , чтобы просмотреть каскадные сетевые запросы, которые произошли во время записи.  

:::image type="complex" source="../media/evaluate-performance-performance-network.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-network.msft.png":::
   Раздел " **сеть** "  
:::image-end:::  

Запросы записываются цветом следующим образом:  

*   HTML: синий  
*   CSS: фиолетовый  
*   JS: желтый  
*   Изображения: зеленые  
    
Щелкните запрос, чтобы просмотреть дополнительные сведения о нем на вкладке " **Сводка** ".  Например, на предыдущем рисунке на вкладке " **Сводка** " отображаются дополнительные сведения о синем запросе, выбранном в разделе " **сеть** ".  

Темно-синий квадрат в верхней левой части запроса означает, что это запрос более высокого приоритета.  Более светлый квадрат — более низкий приоритет.  Например, на предыдущем рисунке синий, выбранный запрос имеет более высокий приоритет, а зеленый — более низкий приоритет.  

На первой из приведенных ниже рисунков запрос `www.bing.com` будет представлен линией слева, полосой в середине, темной частью и светлой частью и линией справа.  На втором рисунке показаны соответствующие представления одного и того же запроса на вкладке **время** на панели **сеть** .  Ниже показано, как эти два представления соотносятся друг с другом.

*   Левая строка — это все, что нужно для `Connection Start` группы событий (включительно).  Другими словами, это все, что раньше `Request Sent` , исключительно.  
*   Светлая часть панели — `Request Sent` и `Waiting (TTFB)` .  
*   Темная часть панели `Content Download` .  
*   В настоящее время в течение всего времени, затраченного на ожидание основного потока, в правой строке.  Этот параметр не отображается на вкладке **время** .  
    
:::row:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-bing-performance-network.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-bing-performance-network.msft.png":::
         Представление запроса в виде строки на строке `www.bing.com`  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-bing-network-timing.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-bing-network-timing.msft.png":::
         Инструмент " **сеть** "  
::: Image-End:::  
   :::column-end:::
:::row-end:::

### Просмотр метрик памяти  

Включите флажок **память** , чтобы просмотреть метрики памяти от последней записи.  

:::image type="complex" source="../media/evaluate-performance-performance-memory-highlight.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-memory-highlight.msft.png":::
   Флажок " **память** "  
:::image-end:::  

DevTools выводит новую диаграмму с **памятью** над вкладкой **Сводка** .  Кроме того, вы также можете создать новую диаграмму под **чистой** диаграммой, называемой **кучей**.  Диаграмма **кучи** предоставляет те же данные, что и в линии **кучи JS** в диаграмме с **памятью** .  

:::image type="complex" source="../media/evaluate-performance-performance-memory-chart.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-memory-chart.msft.png":::
   Метрики памяти  
:::image-end:::  

Цветные линии на диаграмме сопоставляются с цветными флажками над диаграммой.  
Отключите флажок, чтобы скрыть эту категорию на диаграмме.  

На диаграмме отображается только область текущей записи.  Например, на предыдущем рисунке диаграмма **памяти** показывает использование памяти только вокруг 400 MS, помечая его на 1750 MS.  

### Просмотр длительности части записи  

При анализе раздела, например " **сеть** " или " **основной**", иногда требуется более точная оценка продолжительности определенных событий.  `Shift`Чтобы выделить часть записи, перетащите указатель влево или вправо, удерживая нажатой клавишу CTRL.  В нижней части выделенного фрагмента DevTools показывает, сколько времени заняло эта часть.  

:::image type="complex" source="../media/evaluate-performance-performance-main-duration.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-main-duration.msft.png":::
   Просмотр длительности части записи  
:::image-end:::  

### Просмотр снимка экрана  

Перейдите к разделу [захват снимков экрана во время записи](#capture-screenshots-while-recording) , чтобы научиться включать снимки экрана.  

Наведите указатель мыши на **Обзор** , чтобы просмотреть снимок экрана, на котором размещается страница в этот момент записи.  **Обзор** — это раздел, содержащий диаграммы **ЦП**, **кадров между кадрами**и **сети** .  

:::image type="complex" source="../media/evaluate-performance-performance-screenshots-hover.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-screenshots-hover.msft.png":::
   Просмотр снимка экрана  
:::image-end:::  

Вы также можете просмотреть снимки экрана, щелкнув кадр в разделе **кадры** .  DevTools отображает маленькую версию снимка экрана на вкладке " **Сводка** ".  

:::image type="complex" source="../media/evaluate-performance-performance-summary-preview.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-summary-preview.msft.png":::
   Просмотр снимка экрана на вкладке " **Сводка** "  
:::image-end:::  

Щелкните эскиз на вкладке " **Сводка** ", чтобы увеличить масштаб на снимке экрана.  

:::image type="complex" source="../media/evaluate-performance-performance-summary-preview-select.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-summary-preview-select.msft.png":::
   Изменение масштаба экрана на вкладке " **Сводка** "  
:::image-end:::  

### Просмотр сведений о слоях  

Чтобы просмотреть дополнительные сведения о кадре, выполните указанные ниже действия.  

1.  [Включите дополнительные инструменты рисования](#enable-advanced-paint-instrumentation).  
1.  Выберите кадр в разделе **кадры** .  DevTools отображает сведения о слоях на вкладке Создание **слоев** рядом с вкладкой **журнал событий** .  
    
    :::image type="complex" source="../media/evaluate-performance-layers-all.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-layers-all.msft.png":::
       Область **слоев**  
    :::image-end:::  
    
Наведите указатель мыши на слой, чтобы выделить его на схеме.  

:::image type="complex" source="../media/evaluate-performance-performance-frames-document-nav-bar-highlighted.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-frames-document-nav-bar-highlighted.msft.png":::
   Выделение слоя  
:::image-end:::  

Чтобы переместить схему, выполните указанные ниже действия.  

*   Выберите **режим панорамирования** \ ( ![ режим панорамирования ][ImagePanModeIcon] ), чтобы перемещаться вдоль осей X и Y.  
*   Выберите **режим поворота** \ ( ![ режим поворота ][ImageRotateModeIcon] \) для поворота вдоль оси Z.  
*   Выберите **Сброс преобразования** \ ( ![ Сброс преобразования ][ImageResetTransformIcon] ), чтобы восстановить исходное расположение схемы.  
    
### Просмотр профилировщика Paint  

Чтобы просмотреть дополнительные сведения о событии Paint, выполните указанные ниже действия.  

1.  [Включите дополнительные инструменты рисования](#enable-advanced-paint-instrumentation).  
1.  Выберите событие **Paint** в **главном** разделе.  
    
    :::image type="complex" source="../media/evaluate-performance-paint-profiler.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-paint-profiler.msft.png":::
       Вкладка " **профилировщик Paint** "  
    :::image-end:::  
    
## Анализ производительности отрисовки с помощью вкладки "рендеринг"  

С помощью функций вкладки " **отрисовка** " можно визуализировать эффективность отрисовки страницы.  

Чтобы открыть вкладку **рендеринга** , выполните указанные ниже действия.  

1.  [Открытие меню команд][DevToolsCommandMenu].  
1.  Начните вводить текст `Rendering` и выберите его `Show Rendering` .  DevTools отображает вкладку **рендеринг** в нижней части окна DevTools.  
    
    :::image type="complex" source="../media/evaluate-performance-console-drawer-rendering.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-console-drawer-rendering.msft.png":::
       Вкладка « **рендеринг** »  
    :::image-end:::  
    
### Просмотр кадров в секунду в режиме реального времени с индикатором кадров  

**Индикатор кадров в кадрах** — это наложение, которое отображается в правом верхнем углу окна просмотра.  Она предоставляет оценку кадров в реальном времени при выполнении страницы.  Чтобы открыть **индикатор кадров**, выполните указанные ниже действия.  

1.  Открытие вкладки " **рендеринг** ".  НД [Анализ производительности обработки с помощью вкладки рендеринг](#analyze-rendering-performance-with-the-rendering-tab).  
1.  Включите флажок **индикатор кадров в кадре** .  
    
    :::image type="complex" source="../media/evaluate-performance-jank-console-rendering-frame-rate.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-jank-console-rendering-frame-rate.msft.png":::
       **Индикатор кадров в кадре**  
    :::image-end:::  
    
### Просмотр событий рисования в реальном времени с помощью помигания Paint  

Чтобы получить представление о всех событиях рисования на странице в реальном времени, используйте Paint.  Каждый раз, когда часть страницы зарисуется повторно, DevTools разменяет его зеленым цветом.  

Чтобы включить мигание краски, сделайте следующее:  

1.  Открытие вкладки " **рендеринг** ".  Перейдите к разделу [Анализ производительности отрисовки с помощью вкладки рендеринг](#analyze-rendering-performance-with-the-rendering-tab).  
1.  Установите флажок **закрасить мигающий** .  
    
    :::image type="complex" source="../media/evaluate-performance-jank-console-rendering-paint-flashing.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-jank-console-rendering-paint-flashing.msft.png":::
       **Мигание краски**  
    :::image-end:::  
    
### Просмотр наложения слоев с границами слоев  

Используйте **границы слоев** для просмотра наложенных границ слоев и плиток в верхней части страницы.  

Чтобы включить границы слоев, выполните указанные ниже действия.  

1.  Открытие вкладки " **рендеринг** ".  Перейдите к разделу [Анализ производительности отрисовки с помощью вкладки рендеринг](#analyze-rendering-performance-with-the-rendering-tab).  
1.  Установите флажок **границы слоя** .  
    
    :::image type="complex" source="../media/evaluate-performance-devtools-console-rendering-layer-borders.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-devtools-console-rendering-layer-borders.msft.png":::
       **Границы слоев**  
    :::image-end:::  
    
Перейдите к примечаниям в [debug_colors. CC][ChromiumDebugColors] , чтобы получить пояснения к цветовой кодировке.  

### Поиск проблем с производительностью прокрутки в реальном времени  

Используйте проблемы с производительностью прокрутки, чтобы идентифицировать элементы страницы, которые содержат прослушиватели событий, связанные с прокруткой, которые могут повредить производительность страницы.  
DevTools поменяет потенциально проблематичные элементы в синем тексте.  

Для просмотра проблем с производительностью прокрутки:  

1.  Открытие вкладки " **рендеринг** ".  Перейдите к разделу [Анализ производительности отрисовки с помощью вкладки рендеринг](#analyze-rendering-performance-with-the-rendering-tab).  
1.  Включите флажок **проблемы с прокруткой** .  
    
    :::image type="complex" source="../media/evaluate-performance-bing-console-drawer-rendering-scrolling-performance-issues.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-bing-console-drawer-rendering-scrolling-performance-issues.msft.png":::
       **Прокрутка проблем с производительностью** указывает на то, что объекты просмотра, не связанные с разслойю, могут повредить производительность при прокрутке.  
    :::image-end:::  
    
## Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageCaptureSettingsIcon]: ../media/capture-settings-icon.msft.png  
[ImageClearRecordingIcon]: ../media/clear-recording-icon.msft.png  
[ImageCollectGarbageIcon]: ../media/collect-garbage-icon.msft.png  
[ImageNextIcon]: ../media/next-icon.msft.png  
[ImagePanModeIcon]: ../media/pan-mode-icon.msft.png  
[ImagePreviousIcon]: ../media/previous-icon.msft.png  
[ImageRecordIcon]: ../media/record-icon.msft.png
[ImageRefreshPageIcon]: ../media/refresh-page-icon.msft.png  
[ImageResetTransformIcon]: ../media/reset-transform-icon.msft.png  
[ImageRotateModeIcon]: ../media/rotate-mode-icon.msft.png  
[ImageSearchCaseIcon]: ../media/search-case-icon.msft.png  
[ImageSearchRegexIcon]: ../media/search-regex-icon.msft.png  
[ImageShowHeaviestStackIcon]: ../media/show-heaviest-stack-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Инструменты разработчика Microsoft EDGE (Chromium) | Документы Microsoft"  
[DevToolsCommandMenu]: ../command-menu/index.md#open-the-command-menu "Открытие меню команд — команды "выполнить" с помощью меню "команда" Microsoft Edge DevTools | Документы Microsoft"  
[DevtoolsEvaluatePerformanceGettingStarted]: ./index.md "Приступая к анализу производительности среды выполнения | Документы Microsoft"  

[ActivityTabsDemo]: https://microsoft-edge-chromium-devtools.glitch.me/perf/activitytabs.html "Пример вкладки "действия" | цепь"  

[ChromiumDebugColors]: https://cs.chromium.org/chromium/src/cc/debug/debug_colors.cc "debug_colors поиска CC-Code"  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/reference) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
