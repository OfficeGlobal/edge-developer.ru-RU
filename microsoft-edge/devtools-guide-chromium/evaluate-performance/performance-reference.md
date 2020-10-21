---
description: В режиме событий временной шкалы отображаются все события, инициированные во время создания записи.  Чтобы узнать больше о каждом типе событий временной шкалы, воспользуйтесь ссылкой на событие временной шкалы.
title: Справочные материалы по событию временной шкалы
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 989d4d84345fedc1c5aef2cb8d893db3c0e1634b
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "11124903"
---
<!-- Copyright Meggin Kearney and Flavio Copes

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->

# <span data-ttu-id="b687f-105">Справочные материалы по событию временной шкалы</span><span class="sxs-lookup"><span data-stu-id="b687f-105">Timeline Event Reference</span></span>  

<span data-ttu-id="b687f-106">В режиме событий временной шкалы отображаются все события, инициированные во время создания записи.</span><span class="sxs-lookup"><span data-stu-id="b687f-106">The timeline events mode displays all events triggered while making a recording.</span></span>  <span data-ttu-id="b687f-107">Чтобы узнать больше о каждом типе событий временной шкалы, воспользуйтесь ссылкой на событие временной шкалы.</span><span class="sxs-lookup"><span data-stu-id="b687f-107">Use the timeline event reference to learn more about each timeline event type.</span></span>  

## <span data-ttu-id="b687f-108">Общие свойства событий временной шкалы</span><span class="sxs-lookup"><span data-stu-id="b687f-108">Common timeline event properties</span></span>  

<span data-ttu-id="b687f-109">Некоторые сведения представлены в событиях всех типов, в то время как некоторые применимы только к определенным типам событий.</span><span class="sxs-lookup"><span data-stu-id="b687f-109">Certain details are present in events of all types, while some only apply to certain event types.</span></span>  <span data-ttu-id="b687f-110">В этом разделе перечислены свойства, которые являются общими для различных типов событий.</span><span class="sxs-lookup"><span data-stu-id="b687f-110">This section lists properties common to different event types.</span></span>  <span data-ttu-id="b687f-111">Свойства, специфичные для определенных типов событий, перечислены в ссылках на следующие типы событий.</span><span class="sxs-lookup"><span data-stu-id="b687f-111">Properties specific to certain event types are listed in the references for those event types that follow.</span></span>  

| <span data-ttu-id="b687f-112">Свойство</span><span class="sxs-lookup"><span data-stu-id="b687f-112">Property</span></span> | <span data-ttu-id="b687f-113">Когда оно отображается</span><span class="sxs-lookup"><span data-stu-id="b687f-113">When is it shown</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="b687f-114">Агрегированное время</span><span class="sxs-lookup"><span data-stu-id="b687f-114">Aggregated time</span></span> | <span data-ttu-id="b687f-115">Для событий с **вложенными событиями**— время, затраченное на каждую категорию событий.</span><span class="sxs-lookup"><span data-stu-id="b687f-115">For events with **nested events**, the time taken by each category of events.</span></span> |  
| <span data-ttu-id="b687f-116">Стек вызовов</span><span class="sxs-lookup"><span data-stu-id="b687f-116">Call Stack</span></span> | <span data-ttu-id="b687f-117">Для событий с **дочерними событиями**— время, затраченное на каждую категорию событий.</span><span class="sxs-lookup"><span data-stu-id="b687f-117">For events with **child events**, the time taken by each category of events.</span></span> |  
| <span data-ttu-id="b687f-118">Время ЦП</span><span class="sxs-lookup"><span data-stu-id="b687f-118">CPU time</span></span> | <span data-ttu-id="b687f-119">Сколько времени ЦП потратило на записанное событие.</span><span class="sxs-lookup"><span data-stu-id="b687f-119">How much CPU time the recorded event took.</span></span> |  
| <span data-ttu-id="b687f-120">Сведения</span><span class="sxs-lookup"><span data-stu-id="b687f-120">Details</span></span> | <span data-ttu-id="b687f-121">Другие сведения о событии.</span><span class="sxs-lookup"><span data-stu-id="b687f-121">Other details about the event.</span></span> |  
| <span data-ttu-id="b687f-122">Duration \ (в заметках времени \)</span><span class="sxs-lookup"><span data-stu-id="b687f-122">Duration \(at time-stamp\)</span></span> | <span data-ttu-id="b687f-123">Сколько времени занимает событие со всеми дочерними элементами; timestamp — время возникновения события, относительно момента начала записи.</span><span class="sxs-lookup"><span data-stu-id="b687f-123">How long it took the event with all of its children to complete; timestamp is the time at which the event occurred, relative to when the recording started.</span></span> |  
| <span data-ttu-id="b687f-124">Собственное время</span><span class="sxs-lookup"><span data-stu-id="b687f-124">Self time</span></span> | <span data-ttu-id="b687f-125">Время, в течение которого событие не дочернего объекта.</span><span class="sxs-lookup"><span data-stu-id="b687f-125">How long the event took without any of its children.</span></span> |  
| <span data-ttu-id="b687f-126">Размер использованной кучи</span><span class="sxs-lookup"><span data-stu-id="b687f-126">Used Heap Size</span></span> | <span data-ttu-id="b687f-127">Объем памяти, используемой приложением, когда событие было записано, а дельта \ (+/-) изменяется в используемом размере кучи с момента последнего выборки.</span><span class="sxs-lookup"><span data-stu-id="b687f-127">Amount of memory being used by the application when the event was recorded, and the delta \(+/-\) change in used heap size since the last sampling.</span></span> |  

<!--todo: add nested and child events (timelinetool) section when available -->  

## <span data-ttu-id="b687f-128">Загрузка событий</span><span class="sxs-lookup"><span data-stu-id="b687f-128">Loading events</span></span>  

<span data-ttu-id="b687f-129">В этом разделе перечислены события, которые относятся к загрузке категории и их свойствам.</span><span class="sxs-lookup"><span data-stu-id="b687f-129">This section lists events that belong to Loading category and their properties.</span></span>  

| <span data-ttu-id="b687f-130">Событие</span><span class="sxs-lookup"><span data-stu-id="b687f-130">Event</span></span> | <span data-ttu-id="b687f-131">Описание</span><span class="sxs-lookup"><span data-stu-id="b687f-131">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="b687f-132">Анализ HTML-кода</span><span class="sxs-lookup"><span data-stu-id="b687f-132">Parse HTML</span></span> |  <span data-ttu-id="b687f-133">Microsoft Edge запустил алгоритм синтаксического анализа HTML.</span><span class="sxs-lookup"><span data-stu-id="b687f-133">Microsoft Edge ran the HTML parsing algorithm.</span></span> |  
| <span data-ttu-id="b687f-134">Завершить загрузку</span><span class="sxs-lookup"><span data-stu-id="b687f-134">Finish Loading</span></span> |  <span data-ttu-id="b687f-135">Сетевой запрос выполнен.</span><span class="sxs-lookup"><span data-stu-id="b687f-135">A network request completed.</span></span> |  
| <span data-ttu-id="b687f-136">Получение данных</span><span class="sxs-lookup"><span data-stu-id="b687f-136">Receive Data</span></span> |  <span data-ttu-id="b687f-137">Получены данные для запроса.</span><span class="sxs-lookup"><span data-stu-id="b687f-137">Data for a request was received.</span></span>  <span data-ttu-id="b687f-138">Одно или несколько событий приема данных.</span><span class="sxs-lookup"><span data-stu-id="b687f-138">There are one or more Receive Data events.</span></span> |  
| <span data-ttu-id="b687f-139">Получение ответа</span><span class="sxs-lookup"><span data-stu-id="b687f-139">Receive Response</span></span> |  <span data-ttu-id="b687f-140">Первоначальный ответ HTTP из запроса.</span><span class="sxs-lookup"><span data-stu-id="b687f-140">The initial HTTP response from a request.</span></span> |  
| <span data-ttu-id="b687f-141">Отправить запрос</span><span class="sxs-lookup"><span data-stu-id="b687f-141">Send Request</span></span> |  <span data-ttu-id="b687f-142">Сетевой запрос отправлен.</span><span class="sxs-lookup"><span data-stu-id="b687f-142">A network request has been sent.</span></span> |  

### <span data-ttu-id="b687f-143">Загрузка свойств событий</span><span class="sxs-lookup"><span data-stu-id="b687f-143">Loading event properties</span></span>  

| <span data-ttu-id="b687f-144">Свойство</span><span class="sxs-lookup"><span data-stu-id="b687f-144">Property</span></span> | <span data-ttu-id="b687f-145">Описание</span><span class="sxs-lookup"><span data-stu-id="b687f-145">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="b687f-146">Ресурс</span><span class="sxs-lookup"><span data-stu-id="b687f-146">Resource</span></span> | <span data-ttu-id="b687f-147">URL-адрес запрашиваемого ресурса.</span><span class="sxs-lookup"><span data-stu-id="b687f-147">The URL of the requested resource.</span></span> |  
| <span data-ttu-id="b687f-148">Preview</span><span class="sxs-lookup"><span data-stu-id="b687f-148">Preview</span></span> | <span data-ttu-id="b687f-149">Предварительный просмотр запрашиваемого ресурса \ (только изображения \).</span><span class="sxs-lookup"><span data-stu-id="b687f-149">Preview of the requested resource \(images only\).</span></span> |  
| <span data-ttu-id="b687f-150">Метод запроса</span><span class="sxs-lookup"><span data-stu-id="b687f-150">Request Method</span></span> | <span data-ttu-id="b687f-151">Метод HTTP, используемый для запроса ( `GET` `POST` например, "\").</span><span class="sxs-lookup"><span data-stu-id="b687f-151">HTTP method used for the request \(`GET` or `POST`, for example\).</span></span> |  
| <span data-ttu-id="b687f-152">Код состояния</span><span class="sxs-lookup"><span data-stu-id="b687f-152">Status Code</span></span> | <span data-ttu-id="b687f-153">Код ответа HTTP.</span><span class="sxs-lookup"><span data-stu-id="b687f-153">HTTP response code.</span></span> |  
| <span data-ttu-id="b687f-154">Тип MIME</span><span class="sxs-lookup"><span data-stu-id="b687f-154">MIME Type</span></span> | <span data-ttu-id="b687f-155">Тип MIME запрашиваемого ресурса.</span><span class="sxs-lookup"><span data-stu-id="b687f-155">MIME type of the requested resource.</span></span> |  
| <span data-ttu-id="b687f-156">Длина закодированных данных</span><span class="sxs-lookup"><span data-stu-id="b687f-156">Encoded Data Length</span></span> | <span data-ttu-id="b687f-157">Длина запрашиваемого ресурса в байтах.</span><span class="sxs-lookup"><span data-stu-id="b687f-157">Length of requested resource in bytes.</span></span> |  

## <span data-ttu-id="b687f-158">События сценария</span><span class="sxs-lookup"><span data-stu-id="b687f-158">Scripting events</span></span>  

<span data-ttu-id="b687f-159">В этом разделе перечислены события, которые относятся к категории сценариев и их свойствам.</span><span class="sxs-lookup"><span data-stu-id="b687f-159">This section lists events that belong to the Scripting category and their properties.</span></span>  

| <span data-ttu-id="b687f-160">Событие</span><span class="sxs-lookup"><span data-stu-id="b687f-160">Event</span></span> | <span data-ttu-id="b687f-161">Описание</span><span class="sxs-lookup"><span data-stu-id="b687f-161">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="b687f-162">Кадр анимации, срабатывающий</span><span class="sxs-lookup"><span data-stu-id="b687f-162">Animation Frame Fired</span></span> | <span data-ttu-id="b687f-163">Назначенный кадр анимации, а также его обработчик обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="b687f-163">A scheduled animation frame fired, and its callback handler invoked.</span></span> |  
| <span data-ttu-id="b687f-164">Отмена анимации кадра</span><span class="sxs-lookup"><span data-stu-id="b687f-164">Cancel Animation Frame</span></span> |  <span data-ttu-id="b687f-165">Запланированный кадр анимации был отменен.</span><span class="sxs-lookup"><span data-stu-id="b687f-165">A scheduled animation frame was canceled.</span></span> |  
| <span data-ttu-id="b687f-166">Событие GC</span><span class="sxs-lookup"><span data-stu-id="b687f-166">GC Event</span></span> |  <span data-ttu-id="b687f-167">Произошел сбор мусора.</span><span class="sxs-lookup"><span data-stu-id="b687f-167">Garbage collection occurred.</span></span> |  
| <span data-ttu-id="b687f-168">DOMContentLoaded</span><span class="sxs-lookup"><span data-stu-id="b687f-168">DOMContentLoaded</span></span> |  <span data-ttu-id="b687f-169">[Событие DOMContentLoaded][MDNWindowDOMContentLoadedEvent] было инициировано браузером.</span><span class="sxs-lookup"><span data-stu-id="b687f-169">The [DOMContentLoaded event][MDNWindowDOMContentLoadedEvent] was fired by the browser.</span></span>  <span data-ttu-id="b687f-170">Это событие возникает, когда все содержимое модели DOM страницы загружено и проанализировано.</span><span class="sxs-lookup"><span data-stu-id="b687f-170">This event is fired when all of the page's DOM content has been loaded and parsed.</span></span> |  
| <span data-ttu-id="b687f-171">Оценка сценария</span><span class="sxs-lookup"><span data-stu-id="b687f-171">Evaluate Script</span></span> | <span data-ttu-id="b687f-172">Вычислен сценарий.</span><span class="sxs-lookup"><span data-stu-id="b687f-172">A script was evaluated.</span></span> |  
| <span data-ttu-id="b687f-173">Событие</span><span class="sxs-lookup"><span data-stu-id="b687f-173">Event</span></span> | <span data-ttu-id="b687f-174">Событие JavaScript \ (например, `mousedown` или `key` \).</span><span class="sxs-lookup"><span data-stu-id="b687f-174">A JavaScript event \(for example, `mousedown`, or `key`\).</span></span> |  
| <span data-ttu-id="b687f-175">Вызов функции</span><span class="sxs-lookup"><span data-stu-id="b687f-175">Function Call</span></span> | <span data-ttu-id="b687f-176">Сделан вызов функции JavaScript верхнего уровня (появляется только в том случае, если браузер входит в ядро JavaScript).</span><span class="sxs-lookup"><span data-stu-id="b687f-176">A top-level JavaScript function call was made \(only appears when browser enters JavaScript engine\).</span></span> |  
| <span data-ttu-id="b687f-177">Установка таймера</span><span class="sxs-lookup"><span data-stu-id="b687f-177">Install Timer</span></span> | <span data-ttu-id="b687f-178">Таймер создан с помощью [setInterval ()][MDNWindowOrWorkerGlobalScopeSetInterval] или [setTimeout ()][MDNWindowOrWorkerGlobalScopeSetTimeout].</span><span class="sxs-lookup"><span data-stu-id="b687f-178">A timer was created with [setInterval()][MDNWindowOrWorkerGlobalScopeSetInterval] or [setTimeout()][MDNWindowOrWorkerGlobalScopeSetTimeout].</span></span> |  
| <span data-ttu-id="b687f-179">Кадр анимации запроса</span><span class="sxs-lookup"><span data-stu-id="b687f-179">Request Animation Frame</span></span> | <span data-ttu-id="b687f-180">`requestAnimationFrame()`Звонок, запланированный новым кадром.</span><span class="sxs-lookup"><span data-stu-id="b687f-180">A `requestAnimationFrame()` call scheduled a new frame.</span></span> |  
| <span data-ttu-id="b687f-181">Удалить таймер</span><span class="sxs-lookup"><span data-stu-id="b687f-181">Remove Timer</span></span> | <span data-ttu-id="b687f-182">Ранее созданный таймер был очищен.</span><span class="sxs-lookup"><span data-stu-id="b687f-182">A previously created timer was cleared.</span></span> |  
| <span data-ttu-id="b687f-183">Время</span><span class="sxs-lookup"><span data-stu-id="b687f-183">Time</span></span> |  <span data-ttu-id="b687f-184">Сценарий, именуемый [Console. Time ()][ConsoleApiTime].</span><span class="sxs-lookup"><span data-stu-id="b687f-184">A script called [console.time()][ConsoleApiTime].</span></span> |  
| <span data-ttu-id="b687f-185">Время окончания</span><span class="sxs-lookup"><span data-stu-id="b687f-185">Time End</span></span> | <span data-ttu-id="b687f-186">Сценарий, именуемый [Console. timeEnd ()][ConsoleApiTimeEnd].</span><span class="sxs-lookup"><span data-stu-id="b687f-186">A script called [console.timeEnd()][ConsoleApiTimeEnd].</span></span> |  
| <span data-ttu-id="b687f-187">Таймер запущен</span><span class="sxs-lookup"><span data-stu-id="b687f-187">Timer Fired</span></span> | <span data-ttu-id="b687f-188">Таймер, который был запланирован с помощью `setInterval()` или `setTimeout()` .</span><span class="sxs-lookup"><span data-stu-id="b687f-188">A timer fired that was scheduled with `setInterval()` or `setTimeout()`.</span></span> |  
| <span data-ttu-id="b687f-189">Изменение состояния XHR Ready</span><span class="sxs-lookup"><span data-stu-id="b687f-189">XHR Ready State Change</span></span> | <span data-ttu-id="b687f-190">Состояние готовности XMLHTTPRequest изменилось.</span><span class="sxs-lookup"><span data-stu-id="b687f-190">The ready state of an XMLHTTPRequest changed.</span></span> |  
| <span data-ttu-id="b687f-191">Загрузка XHR</span><span class="sxs-lookup"><span data-stu-id="b687f-191">XHR Load</span></span> | <span data-ttu-id="b687f-192">`XMLHTTPRequest`Загрузка завершена.</span><span class="sxs-lookup"><span data-stu-id="b687f-192">An `XMLHTTPRequest` finished loading.</span></span> |  

### <span data-ttu-id="b687f-193">Свойства событий в сценариях</span><span class="sxs-lookup"><span data-stu-id="b687f-193">Scripting event properties</span></span>  

| <span data-ttu-id="b687f-194">Свойство</span><span class="sxs-lookup"><span data-stu-id="b687f-194">Property</span></span> | <span data-ttu-id="b687f-195">Описание</span><span class="sxs-lookup"><span data-stu-id="b687f-195">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="b687f-196">КОД таймера</span><span class="sxs-lookup"><span data-stu-id="b687f-196">Timer ID</span></span> | <span data-ttu-id="b687f-197">Идентификатор таймера.</span><span class="sxs-lookup"><span data-stu-id="b687f-197">The timer ID.</span></span> |  
| <span data-ttu-id="b687f-198">Превышено время ожидания</span><span class="sxs-lookup"><span data-stu-id="b687f-198">Timeout</span></span> | <span data-ttu-id="b687f-199">Время ожидания, указанное в таймере.</span><span class="sxs-lookup"><span data-stu-id="b687f-199">The timeout specified by the timer.</span></span> |  
| <span data-ttu-id="b687f-200">Повторяет</span><span class="sxs-lookup"><span data-stu-id="b687f-200">Repeats</span></span> | <span data-ttu-id="b687f-201">Логическое значение, определяющее, повторяется ли таймер.</span><span class="sxs-lookup"><span data-stu-id="b687f-201">Boolean that specifies if the timer repeats.</span></span> |  
| <span data-ttu-id="b687f-202">Вызов функции</span><span class="sxs-lookup"><span data-stu-id="b687f-202">Function Call</span></span> | <span data-ttu-id="b687f-203">Вызываемая функция.</span><span class="sxs-lookup"><span data-stu-id="b687f-203">A function that was invoked.</span></span> |  

## <span data-ttu-id="b687f-204">Обработка событий</span><span class="sxs-lookup"><span data-stu-id="b687f-204">Rendering events</span></span>  

<span data-ttu-id="b687f-205">В этом разделе перечислены события, которые относятся к категории отрисовки и их свойствам.</span><span class="sxs-lookup"><span data-stu-id="b687f-205">This section lists events that belong to Rendering category and their properties.</span></span>  

| <span data-ttu-id="b687f-206">Событие</span><span class="sxs-lookup"><span data-stu-id="b687f-206">Event</span></span> | <span data-ttu-id="b687f-207">Описание</span><span class="sxs-lookup"><span data-stu-id="b687f-207">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="b687f-208">Недействительный макет</span><span class="sxs-lookup"><span data-stu-id="b687f-208">Invalidate layout</span></span> | <span data-ttu-id="b687f-209">Макет страницы был аннулирован при изменении модели DOM.</span><span class="sxs-lookup"><span data-stu-id="b687f-209">The page layout was invalidated by a DOM change.</span></span> |  
| <span data-ttu-id="b687f-210">Макет</span><span class="sxs-lookup"><span data-stu-id="b687f-210">Layout</span></span> | <span data-ttu-id="b687f-211">Макет страницы завершен.</span><span class="sxs-lookup"><span data-stu-id="b687f-211">A page layout was completed.</span></span> |  
| <span data-ttu-id="b687f-212">Пересчитать стиль</span><span class="sxs-lookup"><span data-stu-id="b687f-212">Recalculate style</span></span> | <span data-ttu-id="b687f-213">Стили элементов, пересчитанные Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="b687f-213">Microsoft Edge recalculated element styles.</span></span> |  
| <span data-ttu-id="b687f-214">Scroll</span><span class="sxs-lookup"><span data-stu-id="b687f-214">Scroll</span></span> | <span data-ttu-id="b687f-215">Содержимое вложенного представления было прокручено.</span><span class="sxs-lookup"><span data-stu-id="b687f-215">The content of nested view was scrolled.</span></span> |  

### <span data-ttu-id="b687f-216">Свойства событий отрисовки</span><span class="sxs-lookup"><span data-stu-id="b687f-216">Rendering event properties</span></span>  

| <span data-ttu-id="b687f-217">Свойство</span><span class="sxs-lookup"><span data-stu-id="b687f-217">Property</span></span> | <span data-ttu-id="b687f-218">Описание</span><span class="sxs-lookup"><span data-stu-id="b687f-218">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="b687f-219">Макет "недействителен"</span><span class="sxs-lookup"><span data-stu-id="b687f-219">Layout invalidated</span></span> | <span data-ttu-id="b687f-220">Для записей макета трассировка стека кода, который привел к недействительности макета.</span><span class="sxs-lookup"><span data-stu-id="b687f-220">For Layout records, the stack trace of the code that caused the layout to be invalidated.</span></span> |  
| <span data-ttu-id="b687f-221">Узлы, для которых нужен макет</span><span class="sxs-lookup"><span data-stu-id="b687f-221">Nodes that need layout</span></span> | <span data-ttu-id="b687f-222">Для записей макета — количество узлов, которые были помечены как нужные макеты до начала перекомпоновки.</span><span class="sxs-lookup"><span data-stu-id="b687f-222">For Layout records, the number of nodes that were marked as needing layout before the relayout started.</span></span>  <span data-ttu-id="b687f-223">Обычно это узлы, которые были аннулированы кодом разработчика, и путь вверх, чтобы переадресовать корневой макет.</span><span class="sxs-lookup"><span data-stu-id="b687f-223">These are normally those nodes that were invalidated by developer code, plus a path upward to relayout root.</span></span> |  
| <span data-ttu-id="b687f-224">Размер дерева макета</span><span class="sxs-lookup"><span data-stu-id="b687f-224">Layout tree size</span></span> | <span data-ttu-id="b687f-225">Для записей макета — общее количество узлов в корне перемакета (узел, на котором Microsoft Edge запускает перекомпоновку).</span><span class="sxs-lookup"><span data-stu-id="b687f-225">For Layout records, the total number of nodes under the relayout root \(the node that Microsoft Edge starts the relayout\).</span></span> |  
| <span data-ttu-id="b687f-226">Область макета</span><span class="sxs-lookup"><span data-stu-id="b687f-226">Layout scope</span></span> | <span data-ttu-id="b687f-227">Возможные значения: `Partial` \ (граница макета — часть DOM \) или `Whole document` .</span><span class="sxs-lookup"><span data-stu-id="b687f-227">Possible values are `Partial` \(the re-layout boundary is a portion of the DOM\) or `Whole document`.</span></span> |  
| <span data-ttu-id="b687f-228">Затронутые элементы</span><span class="sxs-lookup"><span data-stu-id="b687f-228">Elements affected</span></span> | <span data-ttu-id="b687f-229">Для пересчета записей стилей — количество элементов, затронутых с помощью пересчета стилей.</span><span class="sxs-lookup"><span data-stu-id="b687f-229">For Recalculate style records, the number of elements affected by a style recalculation.</span></span> |  
| <span data-ttu-id="b687f-230">Недействительные стили</span><span class="sxs-lookup"><span data-stu-id="b687f-230">Styles invalidated</span></span> | <span data-ttu-id="b687f-231">Для пересчета записей стилей — трассировка стека кода, который вызвал недействительность стиля.</span><span class="sxs-lookup"><span data-stu-id="b687f-231">For Recalculate style records, provides the stack trace of the code that caused the style invalidation.</span></span> |  

## <span data-ttu-id="b687f-232">События рисования</span><span class="sxs-lookup"><span data-stu-id="b687f-232">Painting events</span></span>  

<span data-ttu-id="b687f-233">В этом разделе перечислены события, которые относятся к категории "раскрасить" и их свойствам.</span><span class="sxs-lookup"><span data-stu-id="b687f-233">This section lists events that belong to Painting category and their properties.</span></span>  

| <span data-ttu-id="b687f-234">Событие</span><span class="sxs-lookup"><span data-stu-id="b687f-234">Event</span></span> | <span data-ttu-id="b687f-235">Описание</span><span class="sxs-lookup"><span data-stu-id="b687f-235">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="b687f-236">Составные слои</span><span class="sxs-lookup"><span data-stu-id="b687f-236">Composite Layers</span></span> | <span data-ttu-id="b687f-237">Составные слои изображений для модуля отрисовки Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="b687f-237">The composited image layers for the Microsoft Edge rendering engine.</span></span> |  
| <span data-ttu-id="b687f-238">Декодирование изображений</span><span class="sxs-lookup"><span data-stu-id="b687f-238">Image Decode</span></span> | <span data-ttu-id="b687f-239">Перекодировано ресурс изображения.</span><span class="sxs-lookup"><span data-stu-id="b687f-239">An image resource was decoded.</span></span> |  
| <span data-ttu-id="b687f-240">Изменение размера изображения</span><span class="sxs-lookup"><span data-stu-id="b687f-240">Image Resize</span></span> | <span data-ttu-id="b687f-241">Размер изображения был изменен с помощью собственных размеров.</span><span class="sxs-lookup"><span data-stu-id="b687f-241">An image was resized from its native dimensions.</span></span> |  
| <span data-ttu-id="b687f-242">Paint</span><span class="sxs-lookup"><span data-stu-id="b687f-242">Paint</span></span> | <span data-ttu-id="b687f-243">Составные слои были окрашены в область экрана.</span><span class="sxs-lookup"><span data-stu-id="b687f-243">Composited layers were painted to a region of the display.</span></span>  <span data-ttu-id="b687f-244">При наведении указателя мыши на запись Paint выделена область экрана, которая была обновлена.</span><span class="sxs-lookup"><span data-stu-id="b687f-244">Hovering over a Paint record highlights the region of the display that was updated.</span></span> |  

### <span data-ttu-id="b687f-245">Свойства событий рисования</span><span class="sxs-lookup"><span data-stu-id="b687f-245">Painting event properties</span></span>  

| <span data-ttu-id="b687f-246">Свойство</span><span class="sxs-lookup"><span data-stu-id="b687f-246">Property</span></span> | <span data-ttu-id="b687f-247">Описание</span><span class="sxs-lookup"><span data-stu-id="b687f-247">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="b687f-248">Location</span><span class="sxs-lookup"><span data-stu-id="b687f-248">Location</span></span> | <span data-ttu-id="b687f-249">Для событий Paint координаты x и y прямоугольника рисования.</span><span class="sxs-lookup"><span data-stu-id="b687f-249">For Paint events, the x and y coordinates of the paint rectangle.</span></span> |  
| <span data-ttu-id="b687f-250">Кодов</span><span class="sxs-lookup"><span data-stu-id="b687f-250">Dimensions</span></span> | <span data-ttu-id="b687f-251">Для событий рисования — высота и Ширина закрашиваемой области.</span><span class="sxs-lookup"><span data-stu-id="b687f-251">For Paint events, the height and width of the painted region.</span></span> |  

## <span data-ttu-id="b687f-252">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="b687f-252">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->

[ConsoleApiTime]: /microsoft-edge/devtools-guide-chromium/console/api#time "Справочник по API для консоли времени"  
[ConsoleApiTimeEnd]: /microsoft-edge/devtools-guide-chromium/console/api#timeend "Справочник по API для timeEnd-Console"  
<!--[EvaluatePerformanceTimelineTool]: timeline-tool "How to Use the Timeline Tool"  -->

[MDNWindowDOMContentLoadedEvent]: https://developer.mozilla.org/docs/Web/Events/DOMContentLoaded "Окно: DOMContentLoaded событие | MDN"  
[MDNWindowOrWorkerGlobalScopeSetInterval]: https://developer.mozilla.org/docs/Web/API/WindowTimers/setInterval "WindowOrWorkerGlobalScope. setInterval () | MDN"  
[MDNWindowOrWorkerGlobalScopeSetTimeout]: https://developer.mozilla.org/docs/Web/API/WindowTimers/setTimeout "WindowOrWorkerGlobalScope. setTimeout () | MDN"  

> [!NOTE]
> <span data-ttu-id="b687f-258">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b687f-258">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="b687f-259">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/performance-reference) и [Meggin Kearney][MegginKearney] \ (технический редактор \) и [Flavioной][FlavioCopes] — для разработчиков с полным комплектом.</span><span class="sxs-lookup"><span data-stu-id="b687f-259">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/performance-reference) and is authored by [Meggin Kearney][MegginKearney] \(Tech Writer\) and [Flavio Copes][FlavioCopes] \(Full Stack Developer\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="b687f-261">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b687f-261">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
[FlavioCopes]: https://developers.google.com/web/resources/contributors/flaviocopes  
