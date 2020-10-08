---
description: Используйте инструментирование выделения на временной шкале, чтобы найти объекты, которые не будут собираться сборщиком мусора, и продолжайте удерживать память.
title: Использование инструментирования выделения на временной шкале
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 58a951c4241ae0fe7dce70f523a701694b8254f9
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993508"
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
   limitations under the License. -->

# Использование инструментирования выделения на временной шкале  

Используйте **Инструментирование выделения на временной шкале** , чтобы найти объекты, которые не будут собираться сборщиком мусора, и продолжайте удерживать память.  

## Как работает Инструментарий выделения на временной шкале  

**Инструмент выделения на временной шкале** объединяет подробные сведения о снимке **профилировщика кучи** с помощью добавочного обновления и отслеживания на панели **производительности** .  Аналогичным образом отслеживание выделения кучи для объектов включает в себя запуск записи, выполнение последовательности действий и остановку записи для анализа.  

<!--todo: add profile memory problems (heap profiler) section when available  -->  
<!--todo: add profile evaluate performance (Performance panel) section when available  -->  

**Инструментарий выделения на временной шкале** периодически берет моментальные снимки кучи во время записи \ (как обычно каждые 50 MS \) и один конечный снимок в конце записи.  

:::image type="complex" source="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted.msft.png" alt-text="Инструментирование выделения на временной шкале" lightbox="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted.msft.png":::
   **Инструментирование выделения на временной шкале**  
:::image-end:::  

> [!NOTE]
> Число после a `@` — это идентификатор объекта, который сохраняется во многих снимках, сделанных в ходе сеанса записи.  Постоянный идентификатор объекта обеспечивает точное сравнение состояний кучи.  Объекты перемещаются во время сборки мусора, поэтому отображение адреса объекта не имеет смысла.  

## Включение инструментирования выделения на временной шкале  

Выполните указанные ниже действия, чтобы приступить к работе с **инструментированием выделения на временной шкале**.  

1.  [Откройте DevTools][DevtoolsOpenIndex].  
1.  Откройте панель **память** и выберите переключатель **Инструментирование выделения на временной шкале** .  
1.  Start recording.  
    
    :::image type="complex" source="../media/memory-problems-memory-allocation-instrumentation-on-timeline-selected.msft.png" alt-text="Инструментирование выделения на временной шкале" lightbox="../media/memory-problems-memory-allocation-instrumentation-on-timeline-selected.msft.png":::
       Профилировщик записи для выделения кучи  
    :::image-end:::  
    
## Чтение временной шкалы выделения кучи  

Временная шкала выделения кучи показывает, где создаются объекты и определяет путь сохранения.  На приведенном ниже рисунке в верхней части экрана указываются новые объекты, найденные в куче.  

Высота каждой линии соответствует размеру недавно выделенных объектов, а цвет отрезков показывает, будут ли эти объекты по-прежнему находиться в последнем снимке кучи.  Синие отрезки указывают на объекты, которые по-прежнему находятся в конце временной шкалы, а серые — на объекты, которые были выделены на временной шкале, но с момента сбора мусора.  

:::image type="complex" source="../media/memory-problems-memory-allocation-timelines-snapshot.msft.png" alt-text="Инструментирование выделения на временной шкале" lightbox="../media/memory-problems-memory-allocation-timelines-snapshot.msft.png":::
   **Инструментирование выделения для снимка временной шкалы**  
:::image-end:::  

<!--In the following figure, an action was performed 3 times.  The sample program caches five objects, so the last five blue bars are expected.  But the left-most blue bar indicates a potential problem.  -->  
<!--todo: redo figure 4 with multiple click actions  -->  

Вы можете использовать ползунки на временной шкале выше, чтобы увеличить этот конкретный снимок и просмотреть объекты, которые были недавно выделены в данный момент.  

:::image type="complex" source="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted-annotated.msft.png" alt-text="Инструментирование выделения на временной шкале" lightbox="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted-annotated.msft.png":::
   Изменение размера снимка  
:::image-end:::  

Если щелкнуть конкретный объект в куче, появится дерево сохранения в нижней части снимка кучи.  Проверка пути сохранения для объекта позволяет понять, почему объект не был собран, и необходимо внести необходимые изменения в код, чтобы удалить ненужную ссылку.  

## Просмотр выделения памяти по функциям  

Вы можете просматривать выделение памяти функцией JavaScript.  Дополнительные сведения можно найти [в разделе изучение выделения памяти по функциям][DevtoolsMemoryProblemsIndexInvestigateMemoryAllocationFunction].  

## Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsOpenIndex]: ../open.md "Открыть Microsoft EDGE (Chromium) DevTools | Документы Microsoft"
[DevtoolsMemoryProblemsIndexInvestigateMemoryAllocationFunction]: ./index.md#investigate-memory-allocation-by-function "Исследование выделения памяти функцией — устранение проблем с памятью | Документы Microsoft"  

<!--[HeapProfiler]: ./heap-snapshots.md "How to Record Heap Snapshots"  -->  
<!--[PerformancePanel]: ../profile/evaluate-performance/timeline-tool ""  -->  

[MicrosoftEdgeChannel]: https://www.microsoftedgeinsider.com/download "Скачайте канал Microsoft Edge"  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/memory-problems/allocation-profiler) и была написана с помощью [Meggin Kearney][MegginKearney] \ (технический редактор \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
