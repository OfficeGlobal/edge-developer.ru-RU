---
description: Полный справочник по всем функциям и поведениям, связанным с ИНТЕРФЕЙСом консоли в Microsoft Edge DevTools.
title: Справочник по консоли
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 27d521a4af528e95d06f58ac240f620a9c745044
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125260"
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

# <span data-ttu-id="07992-104">Справочник по консоли</span><span class="sxs-lookup"><span data-stu-id="07992-104">Console Reference</span></span>  

<span data-ttu-id="07992-105">Эта страница содержит ссылки на возможности, связанные с консолью Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="07992-105">This page is a reference of features related to the Microsoft Edge DevTools Console.</span></span>  <span data-ttu-id="07992-106">Предполагается, что вы уже знакомы с использованием консоли для просмотра сообщений в журнале и запуска JavaScript.</span><span class="sxs-lookup"><span data-stu-id="07992-106">It assumes that you are already familiar with using the Console to view logged messages and run JavaScript.</span></span>  <span data-ttu-id="07992-107">В противном случае перейдите в раздел Начало работы [с JavaScript на консоли][DevToolsConsoleJavascript] и приступайте к [регистрации сообщений на консоли][DevToolsConsoleLog].</span><span class="sxs-lookup"><span data-stu-id="07992-107">If not, navigate to [Get Started With Running JavaScript In The Console][DevToolsConsoleJavascript] and [Get Started With Logging Messages In The Console][DevToolsConsoleLog].</span></span>  

<span data-ttu-id="07992-108">Если вы ищете ссылку API на функции, такие как `console.log()` , [Справочник по API консоли][DevToolsConsoleApi].</span><span class="sxs-lookup"><span data-stu-id="07992-108">If you are looking for the API reference on functions like `console.log()` see [Console API Reference][DevToolsConsoleApi].</span></span>  <span data-ttu-id="07992-109">Для справки по функциям `monitorEvents()` , например, перейдите на [ссылку API служебных программ для консоли][DevToolsConsoleUtilities].</span><span class="sxs-lookup"><span data-stu-id="07992-109">For the reference on functions like `monitorEvents()`, navigate to [Console Utilities API Reference][DevToolsConsoleUtilities].</span></span>  

## <span data-ttu-id="07992-110">Открытие консоли</span><span class="sxs-lookup"><span data-stu-id="07992-110">Open the Console</span></span>  

<span data-ttu-id="07992-111">Вы можете открыть консоль как [панель](#open-the-console-panel) или как [вкладку в ящике](#open-the-console-tab-in-the-drawer).</span><span class="sxs-lookup"><span data-stu-id="07992-111">You may open the Console as a [panel](#open-the-console-panel) or as a [tab in the Drawer](#open-the-console-tab-in-the-drawer).</span></span>  

### <span data-ttu-id="07992-112">Открытие панели консоли</span><span class="sxs-lookup"><span data-stu-id="07992-112">Open the Console panel</span></span>  

<span data-ttu-id="07992-113">Выберите `Control` + `Shift` + `J` \ (Windows, Linux \) или `Command` + `Option` + `J` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="07992-113">Select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\).</span></span>  

:::image type="complex" source="../media/console-hello-console.msft.png" alt-text="Панель консоли" lightbox="../media/console-hello-console.msft.png":::
   <span data-ttu-id="07992-115">Панель **консоли**</span><span class="sxs-lookup"><span data-stu-id="07992-115">The **Console** panel</span></span>  
:::image-end:::  

<span data-ttu-id="07992-116">Чтобы открыть панель консоли из [меню команд][DevToolsCommandMenu], начните вводить текст, `Console` а затем запустите команду **Показать консоль** с индикатором **панели** рядом с ним.</span><span class="sxs-lookup"><span data-stu-id="07992-116">To open the Console panel from the [Command Menu][DevToolsCommandMenu], start typing `Console` and then run the **Show Console** command that has the **Panel** badge next to it.</span></span>  

:::image type="complex" source="../media/console-command-menu-show-console.msft.png" alt-text="Панель консоли" lightbox="../media/console-command-menu-show-console.msft.png":::
   <span data-ttu-id="07992-118">Команда для отображения панели **консоли**</span><span class="sxs-lookup"><span data-stu-id="07992-118">The command to show the **Console** panel</span></span>  
:::image-end:::  

### <span data-ttu-id="07992-119">Открытие вкладки "консоль" в ящике</span><span class="sxs-lookup"><span data-stu-id="07992-119">Open the Console tab in the Drawer</span></span>  

<span data-ttu-id="07992-120">Выберите пункт `Escape` **Настройка DevTools** \ ( `...` \) и нажмите кнопку **Показать входной ящик консоли**.</span><span class="sxs-lookup"><span data-stu-id="07992-120">Select `Escape` or choose **Customize And Control DevTools** \(`...`\) and then choose **Show console drawer**.</span></span>  

:::image type="complex" source="../media/console-elements-customize-control-devtools-show-console-drawer.msft.png" alt-text="Панель консоли" lightbox="../media/console-elements-customize-control-devtools-show-console-drawer.msft.png":::
   **<span data-ttu-id="07992-122">Показать консольный ящик</span><span class="sxs-lookup"><span data-stu-id="07992-122">Show console drawer</span></span>**  
:::image-end:::  

<span data-ttu-id="07992-123">Ящик появляется в нижней части окна DevTools и открывается вкладка **консоли** .</span><span class="sxs-lookup"><span data-stu-id="07992-123">The Drawer pops up at the bottom of your DevTools window, with the **Console** tab open.</span></span>  

:::image type="complex" source="../media/console-elements-console-drawer-hello-world.msft.png" alt-text="Панель консоли" lightbox="../media/console-elements-console-drawer-hello-world.msft.png":::
   <span data-ttu-id="07992-125">Вкладка « **консоль** » в **ящике**</span><span class="sxs-lookup"><span data-stu-id="07992-125">The **Console** tab in the **Drawer**</span></span>  
:::image-end:::  

<span data-ttu-id="07992-126">Чтобы открыть вкладку консоль в [меню команд][DevToolsCommandMenu], начните вводить текст, `Console` а затем запустите команду **Показать консоль** с индикатором **ящика** рядом с ним.</span><span class="sxs-lookup"><span data-stu-id="07992-126">To open the Console tab from the [Command Menu][DevToolsCommandMenu], start typing `Console` and then run the **Show Console** command that has the **Drawer** badge next to it.</span></span>  

:::image type="complex" source="../media/console-command-menu-show-console.msft.png" alt-text="Панель консоли" lightbox="../media/console-command-menu-show-console.msft.png":::
   <span data-ttu-id="07992-128">Команда для отображения вкладки " **консоль** " в **ящике**</span><span class="sxs-lookup"><span data-stu-id="07992-128">The command to show the **Console** tab in the **Drawer**</span></span>  
:::image-end:::  

### <span data-ttu-id="07992-129">Открытие параметров консоли</span><span class="sxs-lookup"><span data-stu-id="07992-129">Open Console Settings</span></span>  

<span data-ttu-id="07992-130">На панели " **Параметры консоли** ![ " нажмите значок ][ImageSettingsButtonIcon] "Параметры консоли".</span><span class="sxs-lookup"><span data-stu-id="07992-130">Choose **Console Settings** \(![Console Settings icon][ImageSettingsButtonIcon]\).</span></span>  

:::image type="complex" source="../media/console-settings-group-similar-empty.msft.png" alt-text="Панель консоли" lightbox="../media/console-settings-group-similar-empty.msft.png":::
   **<span data-ttu-id="07992-132">Параметры консоли</span><span class="sxs-lookup"><span data-stu-id="07992-132">Console Settings</span></span>**  
:::image-end:::  

<span data-ttu-id="07992-133">Ниже описаны ссылки для каждого параметра.</span><span class="sxs-lookup"><span data-stu-id="07992-133">The links below explain each setting:</span></span>  

*   [**<span data-ttu-id="07992-134">Скрыть сеть</span><span class="sxs-lookup"><span data-stu-id="07992-134">Hide Network</span></span>**](#hide-network-messages)  
*   [**<span data-ttu-id="07992-135">Сохранить журнал</span><span class="sxs-lookup"><span data-stu-id="07992-135">Preserve Log</span></span>**](#persist-messages-across-page-loads)  
*   [**<span data-ttu-id="07992-136">Только выделенный контекст</span><span class="sxs-lookup"><span data-stu-id="07992-136">Selected Context Only</span></span>**](#filter-out-messages-from-different-contexts)  
*   [**<span data-ttu-id="07992-137">Одинаковая группа</span><span class="sxs-lookup"><span data-stu-id="07992-137">Group Similar</span></span>**](#disable-message-grouping)  
*   [**<span data-ttu-id="07992-138">Запись в журнал XmlHttpRequest</span><span class="sxs-lookup"><span data-stu-id="07992-138">Log XmlHttpRequests</span></span>**](#log-xhr-and-fetch-requests)  
*   [**<span data-ttu-id="07992-139">Упреждающая Оценка</span><span class="sxs-lookup"><span data-stu-id="07992-139">Eager Evaluation</span></span>**](#disable-eager-evaluation)  
*   [**<span data-ttu-id="07992-140">Автозаполнение из истории</span><span class="sxs-lookup"><span data-stu-id="07992-140">Autocomplete From History</span></span>**](#disable-autocomplete-from-history)  
    
### <span data-ttu-id="07992-141">Открытие боковой панели консоли</span><span class="sxs-lookup"><span data-stu-id="07992-141">Open the Console Sidebar</span></span>  

<span data-ttu-id="07992-142">Нажмите кнопку **Показать боковую панель консоли** \ ( ![ Показать боковую панель консоли ][ImageShowConsoleSidebarIcon] ), чтобы отобразить боковую панель, которая удобна для фильтрации.</span><span class="sxs-lookup"><span data-stu-id="07992-142">Choose **Show Console Sidebar** \(![Show Console Sidebar][ImageShowConsoleSidebarIcon]\) to show the Sidebar, which is useful for filtering.</span></span>  

:::image type="complex" source="../media/console-sidebar-drawer-empty.msft.png" alt-text="Панель консоли" lightbox="../media/console-sidebar-drawer-empty.msft.png":::
   <span data-ttu-id="07992-144">**Console (консоль** ) Врезка</span><span class="sxs-lookup"><span data-stu-id="07992-144">**Console** Sidebar</span></span>  
:::image-end:::  

## <span data-ttu-id="07992-145">Просмотр сообщений</span><span class="sxs-lookup"><span data-stu-id="07992-145">View messages</span></span>  

<span data-ttu-id="07992-146">В этом разделе описаны возможности, которые позволят изменить способ представления сообщений на консоли.</span><span class="sxs-lookup"><span data-stu-id="07992-146">This section contains features that change how messages are presented in the Console.</span></span>  <span data-ttu-id="07992-147">В этом пошаговом руководстве показано, как [Просмотреть сообщения][DevToolsConsoleViewMessages] .</span><span class="sxs-lookup"><span data-stu-id="07992-147">See [View messages][DevToolsConsoleViewMessages] for a hands-on walkthrough.</span></span>  

### <span data-ttu-id="07992-148">Отключение группировки сообщений</span><span class="sxs-lookup"><span data-stu-id="07992-148">Disable message grouping</span></span>  

<span data-ttu-id="07992-149">[Откройте параметры консоли](#open-console-settings) и отключите **группу, как** отключить поведение группировки сообщений по умолчанию для консоли.</span><span class="sxs-lookup"><span data-stu-id="07992-149">[Open Console Settings](#open-console-settings) and disable **Group similar** to disable the default message grouping behavior of the Console.</span></span>  <span data-ttu-id="07992-150">Посмотрите, как [XHR журнал и](#log-xhr-and-fetch-requests) выводит запросы на получение примера.</span><span class="sxs-lookup"><span data-stu-id="07992-150">See [Log XHR and Fetch requests](#log-xhr-and-fetch-requests) for an example.</span></span>  

### <span data-ttu-id="07992-151">Регистрация запросов XHR и FETCH</span><span class="sxs-lookup"><span data-stu-id="07992-151">Log XHR and Fetch requests</span></span>  

<span data-ttu-id="07992-152">[Откройте параметры консоли](#open-console-settings) и включите в **журнал записи XMLHttpRequest** , чтобы регистрировать все `XMLHttpRequest` и `Fetch` запросы на консоли по мере их появления.</span><span class="sxs-lookup"><span data-stu-id="07992-152">[Open Console Settings](#open-console-settings) and enable **Log XMLHttpRequests** to log all `XMLHttpRequest` and `Fetch` requests to the Console as they happen.</span></span>  

:::image type="complex" source="../media/console-xhr-fetch.msft.png" alt-text="Панель консоли" lightbox="../media/console-xhr-fetch.msft.png":::
   <span data-ttu-id="07992-154">Журналы `XMLHttpRequest` и `Fetch` запросы</span><span class="sxs-lookup"><span data-stu-id="07992-154">Log `XMLHttpRequest` and `Fetch` requests</span></span>  
:::image-end:::  
<span data-ttu-id="07992-155">Верхнее сообщение на предыдущем рисунке показывает поведение группировки по умолчанию для **консоли**.</span><span class="sxs-lookup"><span data-stu-id="07992-155">The top message in previous figure displays the default grouping behavior of the **Console**.</span></span>  <!--  In the following figure, the same log is displayed after [disabling message grouping](#disable-message-grouping).  -->  

<!--  
> ##### Old Figure 9  
> How the logged `XMLHttpRequest` and `Fetch` requests look after ungrouping  
> :::image type="complex" source="../media/console-xhr-fetch-all.msft.png" alt-text="Панель консоли" lightbox="../media/console-xhr-fetch-all.msft.png":::
>    How the logged XMLHttpRequest and Fetch requests look after ungrouping  
> :::image-end:::  
-->  

<!--todo: add example for ungrouping console items  -->  

### <span data-ttu-id="07992-156">Сохранение сообщений на загрузок страниц</span><span class="sxs-lookup"><span data-stu-id="07992-156">Persist messages across page loads</span></span>  

<span data-ttu-id="07992-157">По умолчанию консоль очищается каждый раз, когда вы загружаете новую страницу.</span><span class="sxs-lookup"><span data-stu-id="07992-157">By default the Console clears whenever you load a new page.</span></span>  <span data-ttu-id="07992-158">Чтобы сохранить сообщения на нескольких страницах, [откройте параметры консоли](#open-console-settings) и установите флажок **сохранить журнал** .</span><span class="sxs-lookup"><span data-stu-id="07992-158">To persist messages across page loads, [Open Console Settings](#open-console-settings) and then enable the **Preserve Log** checkbox.</span></span>  

### <span data-ttu-id="07992-159">Скрыть сетевые сообщения</span><span class="sxs-lookup"><span data-stu-id="07992-159">Hide network messages</span></span>  

<span data-ttu-id="07992-160">По умолчанию браузер записывает сетевые сообщения на **консоль**.</span><span class="sxs-lookup"><span data-stu-id="07992-160">By default the browser logs network messages to the **Console**.</span></span>  <span data-ttu-id="07992-161">На приведенном ниже рисунке выбранное сообщение представляет код состояния HTTP `429` .</span><span class="sxs-lookup"><span data-stu-id="07992-161">In the following figure, the selected message represents an HTTP status code of `429`.</span></span>  

:::image type="complex" source="../media/console-show-network.msft.png" alt-text="Панель консоли" lightbox="../media/console-show-network.msft.png":::
   <span data-ttu-id="07992-163">`429`Сообщение на **консоли**</span><span class="sxs-lookup"><span data-stu-id="07992-163">A `429` message in the **Console**</span></span>  
:::image-end:::  
<span data-ttu-id="07992-164">Чтобы скрыть сетевые сообщения, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="07992-164">To hide network messages:</span></span>  

1.  <span data-ttu-id="07992-165">[Откройте параметры консоли](#open-console-settings).</span><span class="sxs-lookup"><span data-stu-id="07992-165">[Open Console Settings](#open-console-settings).</span></span>  
1.  <span data-ttu-id="07992-166">Включите флажок **Скрыть сеть** .</span><span class="sxs-lookup"><span data-stu-id="07992-166">Enable the **Hide Network** checkbox.</span></span>  
    
## <span data-ttu-id="07992-167">Фильтрация сообщений</span><span class="sxs-lookup"><span data-stu-id="07992-167">Filter messages</span></span>  

<span data-ttu-id="07992-168">Есть несколько способов отфильтровать сообщения на консоли.</span><span class="sxs-lookup"><span data-stu-id="07992-168">There are many ways to filter out messages in the Console.</span></span>  

### <span data-ttu-id="07992-169">Фильтрация сообщений браузера</span><span class="sxs-lookup"><span data-stu-id="07992-169">Filter out browser messages</span></span>  

<span data-ttu-id="07992-170">[Откройте панель консоли](#open-the-console-sidebar) и выберите пункт **сообщения пользователя** , чтобы отображались только те сообщения, которые поставляются из JavaScript страницы.</span><span class="sxs-lookup"><span data-stu-id="07992-170">[Open the Console Sidebar](#open-the-console-sidebar) and choose **User Messages** to only show messages that came from the JavaScript of the page.</span></span>  

:::image type="complex" source="../media/console-sidebar-drawer-user-messages.msft.png" alt-text="Панель консоли" lightbox="../media/console-sidebar-drawer-user-messages.msft.png":::
   <span data-ttu-id="07992-172">Просмотр сообщений пользователя</span><span class="sxs-lookup"><span data-stu-id="07992-172">View user messages</span></span>  
:::image-end:::  

### <span data-ttu-id="07992-173">Фильтрация по уровню ведения журнала</span><span class="sxs-lookup"><span data-stu-id="07992-173">Filter by log level</span></span>  

<span data-ttu-id="07992-174">DevTools назначает каждому `console.*` методу уровень серьезности.</span><span class="sxs-lookup"><span data-stu-id="07992-174">DevTools assigns each `console.*` method a severity level.</span></span>  <span data-ttu-id="07992-175">Существует 4 уровня: `Verbose` ,, `Info` `Warning` , и `Error` .</span><span class="sxs-lookup"><span data-stu-id="07992-175">There are 4 levels: `Verbose`, `Info`, `Warning`, and `Error`.</span></span>  <span data-ttu-id="07992-176">Например, `console.log()` входит в `Info` группу, в то время как `console.error()` она находится в `Error` группе.</span><span class="sxs-lookup"><span data-stu-id="07992-176">For example, `console.log()` is in the `Info` group, whereas `console.error()` is in the `Error` group.</span></span>  <span data-ttu-id="07992-177">[Справочник по API консоли][DevToolsConsoleApi] описывает уровень важности каждого применимого метода.</span><span class="sxs-lookup"><span data-stu-id="07992-177">The [Console API Reference][DevToolsConsoleApi] describes the severity level of each applicable method.</span></span>  <span data-ttu-id="07992-178">Каждое сообщение, которое браузер записывает на консоль, также имеет уровень серьезности.</span><span class="sxs-lookup"><span data-stu-id="07992-178">Every message that the browser logs to the Console has a severity level too.</span></span>  <span data-ttu-id="07992-179">Вы можете скрыть любые ненужные сообщения.</span><span class="sxs-lookup"><span data-stu-id="07992-179">You may hide any level of messages that you are not interested in.</span></span>  <span data-ttu-id="07992-180">Например, если вы заинтересованы в `Error` сообщениях, вы можете скрыть другие три группы.</span><span class="sxs-lookup"><span data-stu-id="07992-180">For example, if you are only interested in `Error` messages, you may hide the other 3 groups.</span></span>  

<span data-ttu-id="07992-181">Щелкните раскрывающийся список **уровни журнала** , чтобы включить или отключить `Verbose` , `Info` `Warning` или `Error` сообщения.</span><span class="sxs-lookup"><span data-stu-id="07992-181">Click the **Log Levels** dropdown to enable or disable `Verbose`, `Info`, `Warning` or `Error` messages.</span></span>  

:::image type="complex" source="../media/console-log-level-default-levels.msft.png" alt-text="Панель консоли" lightbox="../media/console-log-level-default-levels.msft.png":::
   <span data-ttu-id="07992-183">Раскрывающийся список **уровней журнала**</span><span class="sxs-lookup"><span data-stu-id="07992-183">The **Log Levels** dropdown</span></span>  
:::image-end:::  

<span data-ttu-id="07992-184">Вы также можете отфильтровать по уровню журнала, [открыв боковую панель консоли](#open-the-console-sidebar) и выбрав пункт **ошибки**, **предупреждения**, **сведения**или **подробный**.</span><span class="sxs-lookup"><span data-stu-id="07992-184">You may also filter by log level by [opening the Console Sidebar](#open-the-console-sidebar) and then clicking **Errors**, **Warnings**, **Info**, or **Verbose**.</span></span>  

:::image type="complex" source="../media/console-sidebar-warnings.msft.png" alt-text="Панель консоли" lightbox="../media/console-sidebar-warnings.msft.png":::
   <span data-ttu-id="07992-186">Использование боковой панели для просмотра предупреждений</span><span class="sxs-lookup"><span data-stu-id="07992-186">Use the Sidebar to view warnings</span></span>  
:::image-end:::  

### <span data-ttu-id="07992-187">Фильтрация сообщений по URL-адресу</span><span class="sxs-lookup"><span data-stu-id="07992-187">Filter messages by URL</span></span>  

<span data-ttu-id="07992-188">Введите и `url:` URL-адрес, чтобы просматривать только те сообщения, которые были отправлены из этого URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="07992-188">Type `url:` followed by a URL to only view messages that came from that URL.</span></span>  <span data-ttu-id="07992-189">После ввода `url:` DevTools появятся все нужные URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="07992-189">After you type `url:` DevTools shows all relevant URLs.</span></span>  <span data-ttu-id="07992-190">Домены также работают.</span><span class="sxs-lookup"><span data-stu-id="07992-190">Domains also work.</span></span>  <span data-ttu-id="07992-191">Например, если `https://example.com/a.js` `https://example.com/b.js` сообщения записываются в журнал, `url:https://example.com` вы можете сосредоточиться на сообщениях из этих 2 сценариев.</span><span class="sxs-lookup"><span data-stu-id="07992-191">For example, if `https://example.com/a.js` and `https://example.com/b.js` are logging messages, `url:https://example.com` enables you to focus on the messages from these 2 scripts.</span></span>  

:::image type="complex" source="../media/console-filter-text.msft.png" alt-text="Панель консоли" lightbox="../media/console-filter-text.msft.png":::
   <span data-ttu-id="07992-193">Фильтр URL-адреса</span><span class="sxs-lookup"><span data-stu-id="07992-193">A URL filter</span></span>  
:::image-end:::  

<span data-ttu-id="07992-194">Введите текст `-url:` , чтобы скрыть сообщения от этого URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="07992-194">Type `-url:` to hide messages from that URL.</span></span>  <span data-ttu-id="07992-195">Это называется фильтром отрицательных URL-адресов.</span><span class="sxs-lookup"><span data-stu-id="07992-195">This is called a negative URL filter.</span></span>  

:::image type="complex" source="../media/console-negative-filter-text.msft.png" alt-text="Панель консоли" lightbox="../media/console-negative-filter-text.msft.png":::
   <span data-ttu-id="07992-197">Фильтр отрицательных URL-адресов, в котором скрываются все сообщения, соответствующие `https://b.wal.co` URL-адресу.</span><span class="sxs-lookup"><span data-stu-id="07992-197">A negative URL filter that hides all messages that match the `https://b.wal.co` URL</span></span>
:::image-end:::  

<span data-ttu-id="07992-198">Вы также можете показывать сообщения с одного URL-адреса, [открыв боковую панель консоли](#open-the-console-sidebar), развернув раздел " **пользовательские сообщения** ", а затем щелкнув URL-адрес сценария, содержащего сообщения, на которые нужно обратить внимание.</span><span class="sxs-lookup"><span data-stu-id="07992-198">You may also show messages from a single URL by [opening the Console Sidebar](#open-the-console-sidebar), expanding the **User Messages** section, and then clicking the URL of the script containing the messages on which you want to focus.</span></span>  

:::image type="complex" source="../media/console-filter-text-specified.msft.png" alt-text="Панель консоли" lightbox="../media/console-filter-text-specified.msft.png":::
   <span data-ttu-id="07992-200">Просмотр сообщений, которые были получены</span><span class="sxs-lookup"><span data-stu-id="07992-200">View the messages that came from</span></span> `wp-ad.min.js`  
:::image-end:::  

### <span data-ttu-id="07992-201">Фильтрация сообщений в разных контекстах</span><span class="sxs-lookup"><span data-stu-id="07992-201">Filter out messages from different contexts</span></span>  

<span data-ttu-id="07992-202">Предположим, что у вас есть реклама \ (AD) на вашей странице.</span><span class="sxs-lookup"><span data-stu-id="07992-202">Suppose that you have an advertisement \(ad\) on your page.</span></span>  <span data-ttu-id="07992-203">Рекламное объявление встраивается в приложение `<iframe>` и создает большое количество сообщений на консоли.</span><span class="sxs-lookup"><span data-stu-id="07992-203">The ad is embedded in an `<iframe>` and is generating a lot of messages in your Console.</span></span>  <span data-ttu-id="07992-204">Так как объявление запущено в другом [контексте JavaScript](#select-javascript-context), один из способов скрыть сообщения — [открыть параметры консоли](#open-console-settings) и установить флажок **только выбранный контекст** .</span><span class="sxs-lookup"><span data-stu-id="07992-204">Because the ad is running in a different [JavaScript context](#select-javascript-context), one way to hide the messages is to [open Console Settings](#open-console-settings) and enable the **Selected Context Only** checkbox.</span></span>  

### <span data-ttu-id="07992-205">Фильтрация сообщений, не соответствующих шаблону регулярного выражения</span><span class="sxs-lookup"><span data-stu-id="07992-205">Filter out messages that do not match a regular expression pattern</span></span>  

<span data-ttu-id="07992-206">Введите регулярное выражение, например `/[gm][ta][mi]/` в текстовое поле **Фильтр** , чтобы отфильтровать сообщения, которые не соответствуют этому шаблону.</span><span class="sxs-lookup"><span data-stu-id="07992-206">Type a regular expression such as `/[gm][ta][mi]/` in the **Filter** text box to filter out any messages that do not match that pattern.</span></span>  <span data-ttu-id="07992-207">DevTools проверяет, найден ли шаблон в тексте сообщения или сценарий, который привел к занесению в журнал сообщения.</span><span class="sxs-lookup"><span data-stu-id="07992-207">DevTools checks if the pattern is found in the message text or the script that caused the message to be logged.</span></span>  

:::image type="complex" source="../media/console-filter-regex.msft.png" alt-text="Панель консоли" lightbox="../media/console-filter-regex.msft.png":::
   <span data-ttu-id="07992-209">Фильтрация сообщений, не соответствующих `/[gm][ta][mi]/` выражению регулярного выражения</span><span class="sxs-lookup"><span data-stu-id="07992-209">Filter out any messages that do not match the `/[gm][ta][mi]/` regex expression</span></span>  
:::image-end:::  

## <span data-ttu-id="07992-210">Запуск JavaScript</span><span class="sxs-lookup"><span data-stu-id="07992-210">Run JavaScript</span></span>  

<span data-ttu-id="07992-211">В этом разделе описаны возможности, связанные с выполнением JavaScript на консоли.</span><span class="sxs-lookup"><span data-stu-id="07992-211">This section contains features related to running JavaScript in the Console.</span></span>  <span data-ttu-id="07992-212">В этом пошаговом руководстве показано, как [запускать JavaScript][DevToolsConsoleOverviewJavascript] .</span><span class="sxs-lookup"><span data-stu-id="07992-212">See [Run JavaScript][DevToolsConsoleOverviewJavascript] for a hands-on walkthrough.</span></span>  

### <span data-ttu-id="07992-213">Повторное выполнение выражений из истории</span><span class="sxs-lookup"><span data-stu-id="07992-213">Re-run expressions from history</span></span>  

<span data-ttu-id="07992-214">Нажмите клавишу `Up Arrow` для циклического просмотра истории выражений JavaScript, которые выполнялись на консоли раньше.</span><span class="sxs-lookup"><span data-stu-id="07992-214">Press the `Up Arrow` key to cycle through the history of JavaScript expressions that you ran earlier in the Console.</span></span>  <span data-ttu-id="07992-215">Выберите `Enter` , чтобы выполнить это выражение еще раз.</span><span class="sxs-lookup"><span data-stu-id="07992-215">Select `Enter` to run that expression again.</span></span>  

### <span data-ttu-id="07992-216">Просмотр значения выражения в режиме реального времени с помощью выражений с реальными данными</span><span class="sxs-lookup"><span data-stu-id="07992-216">Watch the value of an expression in real-time with Live Expressions</span></span>  

<span data-ttu-id="07992-217">Если вы обнаружите, что один и тот же выражение JavaScript будет вводиться повторно в консоль, возможно, вам будет проще создать **выражение в реальном времени**.</span><span class="sxs-lookup"><span data-stu-id="07992-217">If you find yourself typing the same JavaScript expression in the Console repeatedly, you may find it easier to create a **Live Expression**.</span></span>  <span data-ttu-id="07992-218">С помощью **выражений в реальном времени** вы вводите выражение один раз, а затем закрепите его в верхней части консоли.</span><span class="sxs-lookup"><span data-stu-id="07992-218">With **Live Expressions** you type an expression once and then pin it to the top of your Console.</span></span>  <span data-ttu-id="07992-219">Значение выражения обновляется почти в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="07992-219">The value of the expression updates in near real-time.</span></span>  <span data-ttu-id="07992-220">Просмотрите [значения выражений JavaScript в Real-Time с помощью выражений в реальном времени][DevToolsConsoleLiveExpressions].</span><span class="sxs-lookup"><span data-stu-id="07992-220">See [Watch JavaScript Expression Values In Real-Time With Live Expressions][DevToolsConsoleLiveExpressions].</span></span>  

### <span data-ttu-id="07992-221">Отключение безотлагательной оценки</span><span class="sxs-lookup"><span data-stu-id="07992-221">Disable Eager Evaluation</span></span>  

<span data-ttu-id="07992-222">По мере ввода выражений JavaScript в консоли **упреждающая Оценка** показывает предварительный просмотр возвращаемого значения для этого выражения.</span><span class="sxs-lookup"><span data-stu-id="07992-222">As you type JavaScript expressions in the Console, **Eager Evaluation** shows a preview of the return value for that expression.</span></span>  <span data-ttu-id="07992-223">[Откройте параметры консоли](#open-console-settings) и отключите флажок **упреждающая Оценка** , чтобы отключить предварительный просмотр возвращаемых значений.</span><span class="sxs-lookup"><span data-stu-id="07992-223">[Open Console Settings](#open-console-settings) and disable the **Eager Evaluation** checkbox to turn off the return value previews.</span></span>  

### <span data-ttu-id="07992-224">Отключение автозаполнения из истории</span><span class="sxs-lookup"><span data-stu-id="07992-224">Disable autocomplete from history</span></span>  

<span data-ttu-id="07992-225">По мере ввода выражения в всплывающем окне для консоли отображаются выражения, которые были выполнены раньше.</span><span class="sxs-lookup"><span data-stu-id="07992-225">As you type out an expression, the autocomplete popup window for the Console shows expressions that you ran earlier.</span></span>  <span data-ttu-id="07992-226">Эти выражения добавляются в начале `>` символа.</span><span class="sxs-lookup"><span data-stu-id="07992-226">These expressions are prepended with the `>` character.</span></span>  <span data-ttu-id="07992-227">[Откройте меню Параметры консоли](#open-console-settings) и отключите флажок **Автозаполнение из журнала** , чтобы отключить отображение выражений из истории.</span><span class="sxs-lookup"><span data-stu-id="07992-227">[Open Console Settings](#open-console-settings) and disable the **Autocomplete From History** checkbox to stop showing expressions from your history.</span></span>  

> [!NOTE]
> <span data-ttu-id="07992-228">На приведенном ниже рисунке, `document.querySelector('a')` а `document.querySelector('img')` также выражения, которые были оценены ранее.</span><span class="sxs-lookup"><span data-stu-id="07992-228">In the following figure, `document.querySelector('a')` and `document.querySelector('img')` are expressions that were evaluated earlier.</span></span>  

:::image type="complex" source="../media/console-filter-text-autofilter-history.msft.png" alt-text="Панель консоли" lightbox="../media/console-filter-text-autofilter-history.msft.png":::
   <span data-ttu-id="07992-230">В всплывающем окне "Автозаполнение" отображаются выражения из истории</span><span class="sxs-lookup"><span data-stu-id="07992-230">The autocomplete popup displays expressions from history</span></span>  
:::image-end:::  

### <span data-ttu-id="07992-231">Выбор контекста JavaScript</span><span class="sxs-lookup"><span data-stu-id="07992-231">Select JavaScript context</span></span>  

<span data-ttu-id="07992-232">По умолчанию раскрывающийся список **контекстов JavaScript** имеет значение **Top**, которое представляет [контекст просмотра][MDNBrowsingContext] основного документа.</span><span class="sxs-lookup"><span data-stu-id="07992-232">By default the **JavaScript Context** dropdown is set to **top**, which represents the [browsing context][MDNBrowsingContext] of the main document.</span></span>  

:::image type="complex" source="../media/console-dom-level-top.msft.png" alt-text="Панель консоли" lightbox="../media/console-dom-level-top.msft.png":::
   <span data-ttu-id="07992-234">Раскрывающийся список **контекстов JavaScript**</span><span class="sxs-lookup"><span data-stu-id="07992-234">The **JavaScript Context** dropdown</span></span>  
:::image-end:::  

<span data-ttu-id="07992-235">Предположим, что у вас есть реклама на странице, внедренная в `<iframe>` .</span><span class="sxs-lookup"><span data-stu-id="07992-235">Suppose you have an ad on your page embedded in an `<iframe>`.</span></span>  <span data-ttu-id="07992-236">Вы хотите запустить JavaScript, чтобы настроить модель DOM рекламы.</span><span class="sxs-lookup"><span data-stu-id="07992-236">You want to run JavaScript in order to tweak the DOM of the ad.</span></span>  <span data-ttu-id="07992-237">Сначала необходимо выбрать контекст обзора рекламы из раскрывающегося списка **контекстов JavaScript** .</span><span class="sxs-lookup"><span data-stu-id="07992-237">You should first select the browsing context of the ad from the **JavaScript Context** dropdown.</span></span>  

:::image type="complex" source="../media/console-dom-level-multiple.msft.png" alt-text="Панель консоли" lightbox="../media/console-dom-level-multiple.msft.png":::
   <span data-ttu-id="07992-239">Выбор другого контекста JavaScript</span><span class="sxs-lookup"><span data-stu-id="07992-239">Select a different JavaScript context</span></span>  
:::image-end:::  

## <span data-ttu-id="07992-240">Очистка консоли</span><span class="sxs-lookup"><span data-stu-id="07992-240">Clear the Console</span></span>  

<span data-ttu-id="07992-241">Чтобы очистить консоль, вы можете использовать любой из следующих рабочих процессов:</span><span class="sxs-lookup"><span data-stu-id="07992-241">You may use any of the following workflows to clear the Console:</span></span>  

*   <span data-ttu-id="07992-242">Выберите **Очистить консоль** \ ( ![ Очистить консоль ][ImageClearConsoleIcon] ).</span><span class="sxs-lookup"><span data-stu-id="07992-242">Choose **Clear Console** \(![Clear Console][ImageClearConsoleIcon]\).</span></span>  
*   <span data-ttu-id="07992-243">Щелкните сообщение правой кнопкой мыши и выберите команду **Очистить консоль**.</span><span class="sxs-lookup"><span data-stu-id="07992-243">Right-click a message and then choose **Clear Console**.</span></span>  
*   <span data-ttu-id="07992-244">Введите `clear()` значение в поле консоль и нажмите кнопку `Enter` .</span><span class="sxs-lookup"><span data-stu-id="07992-244">Enter `clear()` in the Console and then select `Enter`.</span></span>  
*   <span data-ttu-id="07992-245">Выполните на `console.clear()` веб-странице сценарий JavaScript.</span><span class="sxs-lookup"><span data-stu-id="07992-245">Run `console.clear()` from the JavaScript for your webpage.</span></span>  
*   <span data-ttu-id="07992-246">Выберите, `Control` + `L` пока консоль находится в фокусе.</span><span class="sxs-lookup"><span data-stu-id="07992-246">Select `Control`+`L` while the Console is in focus.</span></span>  
    
## <span data-ttu-id="07992-247">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="07992-247">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageClearConsoleIcon]: ../media/clear-console-button-icon.msft.png  
[ImageSettingsButtonIcon]: ../media/settings-button-icon.msft.png  
[ImageShowConsoleSidebarIcon]: ../media/show-console-sidebar-icon.msft.png  

<!-- links -->  

[DevToolsCommandMenu]: ../command-menu/index.md "Выполнение команд с помощью командного меню Microsoft Edge DevTools | Документы Microsoft"  
[DevToolsConsoleViewMessages]: ./index.md#viewing-logged-messages "Просмотр сообщений с запротоколированием — обзор консоли | Документы Microsoft"  
[DevToolsConsoleApi]: ./api.md "Справочник по API консоли | Документы Microsoft"  
[DevToolsConsoleOverviewJavascript]: ./index.md#running-javascript "Выполнение JavaScript: обзор консоли | Документы Microsoft"  
[DevToolsConsoleJavascript]: ./javascript.md "Начало работы с JavaScript на консоли | Документы Microsoft"  
[DevToolsConsoleLiveExpressions]: ./live-expressions.md "Просмотр значений выражений JavaScript в режиме реального времени с помощью выражений в реальном масштабе | Документы Microsoft"  
[DevToolsConsoleLog]: ./log.md "Начало работы с сообщениями в журнале на консоли | Документы Microsoft"  
[DevToolsConsoleUtilities]: ./utilities.md "Справочник по API служебных программ для консоли | Документы Microsoft"  

[MDNBrowsingContext]: https://developer.mozilla.org/docs/Glossary/Browsing_context "Контекст просмотра | MDN"  

> [!NOTE]
> <span data-ttu-id="07992-257">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="07992-257">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="07992-258">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/console/reference) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="07992-258">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="07992-260">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="07992-260">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
