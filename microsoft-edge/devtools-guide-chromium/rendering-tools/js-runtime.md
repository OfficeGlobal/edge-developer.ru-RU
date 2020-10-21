---
description: Нахождение ресурсоемких функций с помощью панели DevTools Memory (Microsoft EDGE).
title: Ускорение среды выполнения JavaScript
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: f3cf0440579865495f4afc8b1ae4e3940af7b04f
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125358"
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
   limitations under the License. -->

# Ускорение среды выполнения JavaScript  

Нахождение ресурсоемких функций с помощью панели **памяти** .  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png" alt-text="Образцы профилей" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png":::
   Образцы профилей  
:::image-end:::  

### Краткий обзор  

*   Записывайте именно те функции, которые были вызваны, и объем памяти, необходимый для выделения ресурсов, на панели **памяти** .  
*   Визуализируйте свои профили как flameную диаграмму.  
    
## Запись профиля выборки  

Если вы заметили, что Jank в коде JavaScript, соберите профиль выборки.  Профили выборки показывают, где на странице потратило время выполнения.  

1.  Откройте панель **память** в DevTools.  
1.  Установите переключатель **выборка распределения** .  
1.  Нажмите кнопку **начать**.  
1.  В зависимости от того, что вы пытаетесь проанализировать, вы можете либо повторно загрузить страницу, взаимодействовать со страницей, либо просто разрешить выполнение страницы.  
1.  Когда все будет готово, нажмите кнопку **остановить** .  
    
> [!NOTE]
> Вы также можете использовать [API консольных утилит][DevtoolsConsoleUtilities] для записи и группировки профилей из командной строки.  

## Просмотр профиля выборки  

Когда вы закончите запись, DevTools автоматически заполнит панель **памяти** в разделе **Профили выборки** с данными из записи.  

Представление по умолчанию имеет **большой вид \ (снизу вверх)**.  Это представление позволяет узнать, какие функции приводили к снижению производительности и как проанализировать пути вызова для этих функций.  

### Изменение порядка сортировки  

Чтобы изменить порядок сортировки, щелкните раскрывающееся меню рядом с **выделенной функцией фокуса** , ![ ][ImageFocusIcon] а затем выберите один из указанных ниже вариантов.

**Диаграмма**.  Диаграмма, на которой показана Хронология записи.  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png" alt-text="Образцы профилей" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png":::
   Flame диаграмма  
:::image-end:::  

**Тяжелая – (снизу вверх)**.  Перечисление функций, влияющих на производительность, и позволяет исследовать пути вызова функций.  Это представление по умолчанию.  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png" alt-text="Образцы профилей" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png":::
   Тяжелая диаграмма  
:::image-end:::  

**Дерево \ (сверху вниз)**.  Показывает общую картину структуры вызова, начиная с верхней части стека вызова.  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-tree-top-down.msft.png" alt-text="Образцы профилей" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-tree-top-down.msft.png":::
   Древовидная диаграмма  
:::image-end:::  

### Исключить функции  

Чтобы исключить функцию из профиля выборочной выборки, выберите ее и нажмите кнопку **исключить выбранную функцию** \ (исключить выбранную функцию \ ![ ][ImageExcludeIcon] ).  Функция запроса \ (родительский элемент) исключенной функции \ (дочерней) оценивается выделенной памятью, назначенной исключенной функции \ (дочерняя).  

Нажмите кнопку **восстановить все функции** \ ( ![ восстановить все функции ][ImageRestoreIcon] \), чтобы восстановить все исключенные функции, возвращенные в запись.  

## Просмотр профиля выборки как диаграммы  

Представление Диаграмма обеспечивает визуальное представление профиля выборки с течением времени.  

После [записи профиля выборочной](#record-a-sampling-profile)настройки просмотрите запись в виде Flame диаграммы, [изменив порядок сортировки](#change-sort-order) на **Chart**.  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png" alt-text="Образцы профилей" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png":::
   Flame представления диаграммы  
:::image-end:::  

Flame диаграмма делится на две части.  

| индекса | Составляющая | Описание |  
| --- |:--- |:--- |  
| 1,1 | Обзор | Представление всей записи в Birds взгляда.  Высота отрезков соответствует глубине стека вызова.  Таким образом, чем выше отрезок, тем глубже стека вызовов.  |  
| 2 | Стеки вызовов | Это подробное представление функций, которые были вызваны во время записи.  Горизонтальная ось — это время и вертикальная ось — стек вызовов.  Стеки организованы сверху вниз.  Таким образом, функция сверху вызывается под ней и т. д.  |  

Функции окрашены в случайном порядке.  Нет связи с цветами, используемыми в других панелях.  Однако функции всегда выделяются одинаково во всех вызовах, чтобы можно было видеть закономерности в каждой среде выполнения.  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-highlighted.msft.png" alt-text="Образцы профилей" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-highlighted.msft.png":::
   Диаграмма с аннотированными Flame  
:::image-end:::  

Высокий стек вызовов не обязательно важен, это означает, что было вызвано много функций.  Но широкий отрезок означает, что выполнение функции заняло много времени.  Они являются кандидатами для оптимизации.  

### Масштабирование отдельных частей записи  

Выберите, удерживайте и перетащите указатель мыши по левому краю обзора и проведите по экрану, чтобы увеличить масштаб отдельных частей стека вызова.  После масштабирования стек вызовов автоматически отображает выбранную часть записи.  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-zoomed.msft.png" alt-text="Образцы профилей" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-zoomed.msft.png":::
   Диаграмма с увеличенным масштабом  
:::image-end:::  

### Просмотр сведений о функции  

Выберите функцию, чтобы просмотреть ее определение на панели « **источники** ».  

Наведите указатель мыши на функцию, чтобы отобразить имя и данные о времени.  Ниже приведены сведения.  

| Подробнее | Описание |  
|:--- |:--- |  
| **Name** | Имя функции.  |  
| **Сам размер** | Размер текущего вызова функции, включая только инструкции в функции.  |  
| **Общий размер** | Размер текущего вызова функции и всех ее вызываемых функций.  |  
| **URL-адрес** | Расположение определения функции в форме `base.js:261` Where `base.js` — имя файла, в котором определена функция, и `261` является номером строки определения.  |  
<!--*   **Aggregated self time**.  Aggregate time for all invocations of the function across the recording, not including functions called by this function.  -->  
<!--*   **Aggregated total time**.  Aggregate total time for all invocations of the function, including functions called by this function.  -->  
<!--*   **Not optimized**.  If the profiler has detected a potential optimization for the function it lists it here.  -->  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-hover.msft.png" alt-text="Образцы профилей" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-hover.msft.png":::
   Просмотр сведений о функциях на диаграмме  
:::image-end:::  

## Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageExcludeIcon]: ../media/exclude-icon.msft.png  
[ImageFocusIcon]: ../media/focus-icon.msft.png  
[ImageRestoreIcon]: ../media/restore-icon.msft.png  

<!-- links -->  

[DevtoolsConsoleUtilities]: ../console/utilities.md "Справочник по API служебных программ для консоли | Документы Microsoft"  
[DevtoolsConsoleUtilitiesProfile]: ../console/utilities.md#profile "Profile — Справочник по API для служебных программ консоли | Документы Microsoft"  
[DevtoolsConsoleUtilitiesProfileEnd]: ../console/utilities.md#profileend "Справочник по API для служебных программ на консоли profileEnd | Документы Microsoft"  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/js-execution) и [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \) и [Meggin Kearney][MegginKearney] \ (технический редактор \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
