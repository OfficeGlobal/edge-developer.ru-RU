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

# <span data-ttu-id="2ea63-104">Использование инструментирования выделения на временной шкале</span><span class="sxs-lookup"><span data-stu-id="2ea63-104">How to use Allocation instrumentation on Timeline</span></span>  

<span data-ttu-id="2ea63-105">Используйте **Инструментирование выделения на временной шкале** , чтобы найти объекты, которые не будут собираться сборщиком мусора, и продолжайте удерживать память.</span><span class="sxs-lookup"><span data-stu-id="2ea63-105">Use **Allocation instrumentation on timeline** to find objects that are not being properly garbage collected, and continue to retain memory.</span></span>  

## <span data-ttu-id="2ea63-106">Как работает Инструментарий выделения на временной шкале</span><span class="sxs-lookup"><span data-stu-id="2ea63-106">How Allocation instrumentation on timeline works</span></span>  

<span data-ttu-id="2ea63-107">**Инструмент выделения на временной шкале** объединяет подробные сведения о снимке **профилировщика кучи** с помощью добавочного обновления и отслеживания на панели **производительности** .</span><span class="sxs-lookup"><span data-stu-id="2ea63-107">**Allocation instrumentation on timeline** combines the detailed snapshot information of the **heap profiler** with the incremental updating and tracking of the **Performance** panel.</span></span>  <span data-ttu-id="2ea63-108">Аналогичным образом отслеживание выделения кучи для объектов включает в себя запуск записи, выполнение последовательности действий и остановку записи для анализа.</span><span class="sxs-lookup"><span data-stu-id="2ea63-108">Similarly, tracking heap allocation for objects involves starting a recording, performing a sequence of actions, and stopping the recording for analysis.</span></span>  

<!--todo: add profile memory problems (heap profiler) section when available  -->  
<!--todo: add profile evaluate performance (Performance panel) section when available  -->  

<span data-ttu-id="2ea63-109">**Инструментарий выделения на временной шкале** периодически берет моментальные снимки кучи во время записи \ (как обычно каждые 50 MS \) и один конечный снимок в конце записи.</span><span class="sxs-lookup"><span data-stu-id="2ea63-109">**Allocation instrumentation on timeline** takes heap snapshots periodically throughout the recording \(as frequently as every 50 ms\) and one final snapshot at the end of the recording.</span></span>  

:::image type="complex" source="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted.msft.png" alt-text="Инструментирование выделения на временной шкале" lightbox="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted.msft.png":::
   **<span data-ttu-id="2ea63-111">Инструментирование выделения на временной шкале</span><span class="sxs-lookup"><span data-stu-id="2ea63-111">Allocation instrumentation on timeline</span></span>**  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="2ea63-112">Число после a `@` — это идентификатор объекта, который сохраняется во многих снимках, сделанных в ходе сеанса записи.</span><span class="sxs-lookup"><span data-stu-id="2ea63-112">The number after the `@` is an object ID that persists across the multiple snapshots taken during the recording session.</span></span>  <span data-ttu-id="2ea63-113">Постоянный идентификатор объекта обеспечивает точное сравнение состояний кучи.</span><span class="sxs-lookup"><span data-stu-id="2ea63-113">The persistent object ID enables precise comparison between heap states.</span></span>  <span data-ttu-id="2ea63-114">Объекты перемещаются во время сборки мусора, поэтому отображение адреса объекта не имеет смысла.</span><span class="sxs-lookup"><span data-stu-id="2ea63-114">Objects are moved during garbage collections, so displaying the address of an object makes no sense.</span></span>  

## <span data-ttu-id="2ea63-115">Включение инструментирования выделения на временной шкале</span><span class="sxs-lookup"><span data-stu-id="2ea63-115">Enable Allocation Instrumentation on Timeline</span></span>  

<span data-ttu-id="2ea63-116">Выполните указанные ниже действия, чтобы приступить к работе с **инструментированием выделения на временной шкале**.</span><span class="sxs-lookup"><span data-stu-id="2ea63-116">Complete the following actions to begin using **Allocation instrumentation on timeline**.</span></span>  

1.  <span data-ttu-id="2ea63-117">[Откройте DevTools][DevtoolsOpenIndex].</span><span class="sxs-lookup"><span data-stu-id="2ea63-117">[Open the DevTools][DevtoolsOpenIndex].</span></span>  
1.  <span data-ttu-id="2ea63-118">Откройте панель **память** и выберите переключатель **Инструментирование выделения на временной шкале** .</span><span class="sxs-lookup"><span data-stu-id="2ea63-118">Open the **Memory** panel, select the **Allocation instrumentation on timeline** radio button.</span></span>  
1.  <span data-ttu-id="2ea63-119">Start recording.</span><span class="sxs-lookup"><span data-stu-id="2ea63-119">Start recording.</span></span>  
    
    :::image type="complex" source="../media/memory-problems-memory-allocation-instrumentation-on-timeline-selected.msft.png" alt-text="Инструментирование выделения на временной шкале" lightbox="../media/memory-problems-memory-allocation-instrumentation-on-timeline-selected.msft.png":::
       <span data-ttu-id="2ea63-121">Профилировщик записи для выделения кучи</span><span class="sxs-lookup"><span data-stu-id="2ea63-121">Record heap allocations profiler</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="2ea63-122">Чтение временной шкалы выделения кучи</span><span class="sxs-lookup"><span data-stu-id="2ea63-122">Read a heap allocation timeline</span></span>  

<span data-ttu-id="2ea63-123">Временная шкала выделения кучи показывает, где создаются объекты и определяет путь сохранения.</span><span class="sxs-lookup"><span data-stu-id="2ea63-123">The heap allocation timeline shows where objects are being created and identifies the retaining path.</span></span>  <span data-ttu-id="2ea63-124">На приведенном ниже рисунке в верхней части экрана указываются новые объекты, найденные в куче.</span><span class="sxs-lookup"><span data-stu-id="2ea63-124">In the following figure, the bars at the top indicate when new objects are found in the heap.</span></span>  

<span data-ttu-id="2ea63-125">Высота каждой линии соответствует размеру недавно выделенных объектов, а цвет отрезков показывает, будут ли эти объекты по-прежнему находиться в последнем снимке кучи.</span><span class="sxs-lookup"><span data-stu-id="2ea63-125">The height of each bar corresponds to the size of the recently allocated objects, and the color of the bars indicate whether or not those objects are still live in the final heap snapshot.</span></span>  <span data-ttu-id="2ea63-126">Синие отрезки указывают на объекты, которые по-прежнему находятся в конце временной шкалы, а серые — на объекты, которые были выделены на временной шкале, но с момента сбора мусора.</span><span class="sxs-lookup"><span data-stu-id="2ea63-126">Blue bars indicate objects that are still live at the end of the timeline, Gray bars indicate objects that were allocated during the timeline, but have since been garbage collected.</span></span>  

:::image type="complex" source="../media/memory-problems-memory-allocation-timelines-snapshot.msft.png" alt-text="Инструментирование выделения на временной шкале" lightbox="../media/memory-problems-memory-allocation-timelines-snapshot.msft.png":::
   <span data-ttu-id="2ea63-128">**Инструментирование выделения для снимка временной шкалы**</span><span class="sxs-lookup"><span data-stu-id="2ea63-128">**Allocation instrumentation on timeline** snapshot</span></span>  
:::image-end:::  

<!--In the following figure, an action was performed 3 times.  The sample program caches five objects, so the last five blue bars are expected.  But the left-most blue bar indicates a potential problem.  -->  
<!--todo: redo figure 4 with multiple click actions  -->  

<span data-ttu-id="2ea63-129">Вы можете использовать ползунки на временной шкале выше, чтобы увеличить этот конкретный снимок и просмотреть объекты, которые были недавно выделены в данный момент.</span><span class="sxs-lookup"><span data-stu-id="2ea63-129">You are able to use the sliders in the timeline above to zoom into that particular snapshot and see the objects that were recently allocated at that point:</span></span>  

:::image type="complex" source="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted-annotated.msft.png" alt-text="Инструментирование выделения на временной шкале" lightbox="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted-annotated.msft.png":::
   <span data-ttu-id="2ea63-131">Изменение размера снимка</span><span class="sxs-lookup"><span data-stu-id="2ea63-131">Zoom into snapshot</span></span>  
:::image-end:::  

<span data-ttu-id="2ea63-132">Если щелкнуть конкретный объект в куче, появится дерево сохранения в нижней части снимка кучи.</span><span class="sxs-lookup"><span data-stu-id="2ea63-132">Clicking on a specific object in the heap shows the retaining tree in the bottom portion of the heap snapshot.</span></span>  <span data-ttu-id="2ea63-133">Проверка пути сохранения для объекта позволяет понять, почему объект не был собран, и необходимо внести необходимые изменения в код, чтобы удалить ненужную ссылку.</span><span class="sxs-lookup"><span data-stu-id="2ea63-133">Examining the retaining path to the object should give you enough information to understand why the object was not collected, and you should make the necessary code changes to remove the unnecessary reference.</span></span>  

## <span data-ttu-id="2ea63-134">Просмотр выделения памяти по функциям</span><span class="sxs-lookup"><span data-stu-id="2ea63-134">View memory allocation by function</span></span>  

<span data-ttu-id="2ea63-135">Вы можете просматривать выделение памяти функцией JavaScript.</span><span class="sxs-lookup"><span data-stu-id="2ea63-135">You are able to view memory allocation by JavaScript function.</span></span>  <span data-ttu-id="2ea63-136">Дополнительные сведения можно найти [в разделе изучение выделения памяти по функциям][DevtoolsMemoryProblemsIndexInvestigateMemoryAllocationFunction].</span><span class="sxs-lookup"><span data-stu-id="2ea63-136">For more information, see [Investigate memory allocation by function][DevtoolsMemoryProblemsIndexInvestigateMemoryAllocationFunction].</span></span>  

## <span data-ttu-id="2ea63-137">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2ea63-137">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsOpenIndex]: ../open.md "Открыть Microsoft EDGE (Chromium) DevTools | Документы Microsoft"
[DevtoolsMemoryProblemsIndexInvestigateMemoryAllocationFunction]: ./index.md#investigate-memory-allocation-by-function "Исследование выделения памяти функцией — устранение проблем с памятью | Документы Microsoft"  

<!--[HeapProfiler]: ./heap-snapshots.md "How to Record Heap Snapshots"  -->  
<!--[PerformancePanel]: ../profile/evaluate-performance/timeline-tool ""  -->  

[MicrosoftEdgeChannel]: https://www.microsoftedgeinsider.com/download "Скачайте канал Microsoft Edge"  

> [!NOTE]
> <span data-ttu-id="2ea63-141">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="2ea63-141">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="2ea63-142">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/memory-problems/allocation-profiler) и была написана с помощью [Meggin Kearney][MegginKearney] \ (технический редактор \).</span><span class="sxs-lookup"><span data-stu-id="2ea63-142">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/memory-problems/allocation-profiler) and is authored by [Meggin Kearney][MegginKearney] \(Technical Writer\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="2ea63-144">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="2ea63-144">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
