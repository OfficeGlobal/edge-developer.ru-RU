---
description: Фрагменты — это небольшие сценарии, которые можно создавать и использовать в инструменте "источники" Microsoft Edge DevTools.  Вы можете открывать и запускать ресурсы на любой веб-странице.  При запуске фрагмента кода запускается из контекста открытой на данный момент веб-страницы.
title: Выполнение фрагментов кода JavaScript на любой странице с Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 3542243f7fa886865ced47d47991cd9b11001e2e
ms.sourcegitcommit: 9dcaf598f3930bcfab9f93ff63463beb98274de0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/30/2020
ms.locfileid: "11145122"
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

# <span data-ttu-id="c87a3-106">Выполнение фрагментов кода JavaScript на любой веб-странице с помощью Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="c87a3-106">Run snippets of JavaScript on any webpage with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="c87a3-107">Если вы используете один и тот же код на [консоли][DevtoolsConsoleIndex] несколько раз, вместо этого рекомендуется сохранить его в виде фрагмента кода.</span><span class="sxs-lookup"><span data-stu-id="c87a3-107">If you are running the same code in the [Console][DevtoolsConsoleIndex] repeatedly, consider saving the code as a Snippet instead.</span></span>  <span data-ttu-id="c87a3-108">Фрагменты — это сценарии, созданные в инструменте « [источники][DevToolsSourcesTool] ».</span><span class="sxs-lookup"><span data-stu-id="c87a3-108">Snippets are scripts that you author in the [Sources][DevToolsSourcesTool] tool.</span></span>  <span data-ttu-id="c87a3-109">Фрагменты имеют доступ к контексту JavaScript на веб-странице, и вы можете запускать фрагменты на любой веб-странице.</span><span class="sxs-lookup"><span data-stu-id="c87a3-109">Snippets have access to the JavaScript context of the webpage, and you may run snippets on any webpage.</span></span>  <span data-ttu-id="c87a3-110">Параметры безопасности большинства веб-страниц заключаются в том, что они не загружают другие сценарии во фрагментах.</span><span class="sxs-lookup"><span data-stu-id="c87a3-110">The security settings of most webpages block from loading other scripts in Snippets.</span></span>  <span data-ttu-id="c87a3-111">По этой причине вы должны добавить весь код в один файл.</span><span class="sxs-lookup"><span data-stu-id="c87a3-111">For that reason, you must include all your code in one file.</span></span>  

<span data-ttu-id="c87a3-112">Фрагменты — это альтернатива [для использования в качестве][WikiBookmarklet] задвижей с разницей, которую фрагменты работают только в DevTools и не ограничиваются допустимой длиной URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="c87a3-112">Snippets are an alternative to [bookmarklets][WikiBookmarklet] with the difference that Snippets only run in DevTools and are not limited to the allowed length of a URL.</span></span>  

<span data-ttu-id="c87a3-113">Использование сниппетов — это отличный способ изменить некоторые элементы на веб-странице стороннего поставщика.</span><span class="sxs-lookup"><span data-stu-id="c87a3-113">Using Snippets is an excellent way to change a few things in a third-party webpage.</span></span>  <span data-ttu-id="c87a3-114">Изменения кода во фрагментах добавляются на текущую веб-страницу и выполняются в том же контексте.</span><span class="sxs-lookup"><span data-stu-id="c87a3-114">Code changes in Snippets are added to the current webpage and run in the same context.</span></span>  <span data-ttu-id="c87a3-115">Дополнительные сведения об изменении существующего кода веб-страницы можно найти в разделе [Overrides][DevtoolsJavascriptOverrides].</span><span class="sxs-lookup"><span data-stu-id="c87a3-115">For more information about changing the existing code of a webpage, navigate to [Overrides][DevtoolsJavascriptOverrides].</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="c87a3-116">Например, на приведенном ниже рисунке показана домашняя страница DevTools слева и фрагмент исходного кода справа.</span><span class="sxs-lookup"><span data-stu-id="c87a3-116">For example, in the following figure shows the DevTools homepage on the left and some Snippet source code on the right.</span></span>  
      
      :::image type="complex" source="../media/javascript-sources-snippets-split-screen.msft.png" alt-text="Перед запуском сниппета" lightbox="../media/javascript-sources-snippets-split-screen.msft.png":::
         <span data-ttu-id="c87a3-118">Веб-страница перед выполнением фрагмента</span><span class="sxs-lookup"><span data-stu-id="c87a3-118">The webpage before running the Snippet</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="c87a3-119">Исходный код фрагмента на веб-странице перед выполнением фрагмента.</span><span class="sxs-lookup"><span data-stu-id="c87a3-119">The Snippet source code from the webpage before running the Snippet.</span></span>  
      
      ```javascript
      console.log('Hello, Snippets!');
      document.body.innerHTML = '';
      var p = document.createElement('p');
      p.textContent = 'Hello, Snippets!';
      document.body.appendChild(p);
      ```
   :::column-end:::
:::row-end:::  

<span data-ttu-id="c87a3-120">На рисунке ниже показана веб-страница после выполнения фрагмента.</span><span class="sxs-lookup"><span data-stu-id="c87a3-120">In the following figure, the webpage appears after running the Snippet.</span></span>  <span data-ttu-id="c87a3-121">Во всплывающем **ящике консоли** выводится `Hello, Snippets!` сообщение о том, что журналы фрагментов, и содержимое веб-страницы полностью меняются.</span><span class="sxs-lookup"><span data-stu-id="c87a3-121">The **Console Drawer** pops up to display the `Hello, Snippets!` message that the Snippet logs, and the content of the webpage changes completely.</span></span>  

:::image type="complex" source="../media/javascript-sources-snippets-split-screen-after.msft.png" alt-text="Веб-страница после выполнения фрагмента" lightbox="../media/javascript-sources-snippets-split-screen-after.msft.png":::
   <span data-ttu-id="c87a3-123">Веб-страница после выполнения фрагмента</span><span class="sxs-lookup"><span data-stu-id="c87a3-123">The webpage after running the Snippet</span></span>  
:::image-end:::  

## <span data-ttu-id="c87a3-124">Открытие области "фрагменты кода"</span><span class="sxs-lookup"><span data-stu-id="c87a3-124">Open the Snippets pane</span></span>  

<span data-ttu-id="c87a3-125">На панели **фрагментов** перечислены ваши фрагменты.</span><span class="sxs-lookup"><span data-stu-id="c87a3-125">The **Snippets** pane lists your Snippets.</span></span>  <span data-ttu-id="c87a3-126">Если вы хотите изменить фрагмент, необходимо открыть его из области **фрагментов** .</span><span class="sxs-lookup"><span data-stu-id="c87a3-126">When you want to edit a Snippet, you need to open it from the **Snippets** pane.</span></span>  

:::image type="complex" source="../media/javascript-sources-snippets-pane.msft.png" alt-text="Область фрагментов" lightbox="../media/javascript-sources-snippets-pane.msft.png":::
   <span data-ttu-id="c87a3-128">Область **фрагментов**</span><span class="sxs-lookup"><span data-stu-id="c87a3-128">The **Snippets** pane</span></span>  
:::image-end:::  

### <span data-ttu-id="c87a3-129">Открытие области фрагментов с помощью мыши</span><span class="sxs-lookup"><span data-stu-id="c87a3-129">Open the Snippets pane with a mouse</span></span>  

1.  <span data-ttu-id="c87a3-130">Перейдите на вкладку **источники** , чтобы открыть средство " **источники** ".</span><span class="sxs-lookup"><span data-stu-id="c87a3-130">Choose the **Sources** tab to open the **Sources** tool.</span></span>  <span data-ttu-id="c87a3-131">Обычно область **страницы** открывается по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c87a3-131">The **Page** pane usually opens by default.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-pane.msft.png" alt-text="Инструмент «источники» с открытой областью страницы в левой части экрана" lightbox="../media/javascript-sources-page-pane.msft.png":::
       <span data-ttu-id="c87a3-133">Инструмент « **источники** » с открытой областью **страницы** в левой части экрана</span><span class="sxs-lookup"><span data-stu-id="c87a3-133">The **Sources** tool with the **Page** pane open on the left</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c87a3-134">Перейдите на вкладку **фрагменты кода** , чтобы открыть область **фрагменты** .</span><span class="sxs-lookup"><span data-stu-id="c87a3-134">Choose the **Snippets** tab to open the **Snippets** pane.</span></span>  <span data-ttu-id="c87a3-135">**More Tabs** ![ ][ImageMoreTabsIcon] Для доступа к параметру **фрагментов** может потребоваться выбрать дополнительные вкладки \ (дополнительные вкладки \).</span><span class="sxs-lookup"><span data-stu-id="c87a3-135">You may need to choose **More Tabs** \(![More Tabs][ImageMoreTabsIcon]\) to access the **Snippets** option.</span></span>  
    
### <span data-ttu-id="c87a3-136">Открытие области фрагментов с помощью меню команд</span><span class="sxs-lookup"><span data-stu-id="c87a3-136">Open the Snippets pane with the Command Menu</span></span>  

1.  <span data-ttu-id="c87a3-137">Сфокусировать указатель на своем месте в DevTools.</span><span class="sxs-lookup"><span data-stu-id="c87a3-137">Focus your cursor somewhere in DevTools.</span></span>  
1.  <span data-ttu-id="c87a3-138">Выберите `Control` + `Shift` + `P` \ (Windows, Linux \) или `Command` + `Shift` + `P` \ (macOS \), чтобы открыть меню команд.</span><span class="sxs-lookup"><span data-stu-id="c87a3-138">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="c87a3-139">Введите `Snippets` команду **Показать фрагменты**, а затем нажмите кнопку, `Enter` чтобы выполнить команду.</span><span class="sxs-lookup"><span data-stu-id="c87a3-139">Type `Snippets`, choose **Show Snippets**, and then select `Enter` to run the command.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-show-snippets.msft.png" alt-text="Команда «Показать фрагменты»" lightbox="../media/javascript-search-show-snippets.msft.png":::
       <span data-ttu-id="c87a3-141">Команда « **Показать фрагменты** »</span><span class="sxs-lookup"><span data-stu-id="c87a3-141">The **Show Snippets** command</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="c87a3-142">Создание фрагментов кода</span><span class="sxs-lookup"><span data-stu-id="c87a3-142">Create Snippets</span></span>  

### <span data-ttu-id="c87a3-143">Создание фрагмента с помощью панели «источники»</span><span class="sxs-lookup"><span data-stu-id="c87a3-143">Create a Snippet through the Sources panel</span></span>  

1.  <span data-ttu-id="c87a3-144">[Открытие области **фрагментов** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="c87a3-144">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="c87a3-145">Выберите команду **создать фрагмент**.</span><span class="sxs-lookup"><span data-stu-id="c87a3-145">Choose **New snippet**.</span></span>  
1.  <span data-ttu-id="c87a3-146">Введите имя для фрагмента, а затем выберите `Enter` для сохранения.</span><span class="sxs-lookup"><span data-stu-id="c87a3-146">Enter a name for your Snippet then select `Enter` to save.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-naming.msft.png" alt-text="Присвоение имени фрагменту" lightbox="../media/javascript-sources-snippets-naming.msft.png":::
       <span data-ttu-id="c87a3-148">Присвоение имени фрагменту</span><span class="sxs-lookup"><span data-stu-id="c87a3-148">Name a Snippet</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="c87a3-149">Создание фрагмента с помощью меню команд</span><span class="sxs-lookup"><span data-stu-id="c87a3-149">Create a Snippet through the Command Menu</span></span>  

1.  <span data-ttu-id="c87a3-150">Сфокусировать указатель на своем месте в DevTools.</span><span class="sxs-lookup"><span data-stu-id="c87a3-150">Focus your cursor somewhere in DevTools.</span></span>  
1.  <span data-ttu-id="c87a3-151">Выберите `Control` + `Shift` + `P` \ (Windows, Linux \) или `Command` + `Shift` + `P` \ (macOS \), чтобы открыть меню команд.</span><span class="sxs-lookup"><span data-stu-id="c87a3-151">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="c87a3-152">Введите `Snippet` команду **создать фрагмент**, а затем нажмите кнопку, `Enter` чтобы выполнить команду.</span><span class="sxs-lookup"><span data-stu-id="c87a3-152">Type `Snippet`, choose **Create new snippet**, then select `Enter` to run the command.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-create-new-snippet.msft.png" alt-text="Команда для создания нового фрагмента." lightbox="../media/javascript-search-create-new-snippet.msft.png":::
       <span data-ttu-id="c87a3-154">Команда для создания нового фрагмента.</span><span class="sxs-lookup"><span data-stu-id="c87a3-154">The command for creating a new Snippet</span></span>  
    :::image-end:::  
    
<span data-ttu-id="c87a3-155">Чтобы переименовать новый фрагмент с помощью настраиваемого имени, перейдите в раздел [Переименование фрагментов](#rename-snippets).</span><span class="sxs-lookup"><span data-stu-id="c87a3-155">To rename your new Snippet with a custom name, navigate to [Rename Snippets](#rename-snippets).</span></span>  

## <span data-ttu-id="c87a3-156">Редактирование фрагментов</span><span class="sxs-lookup"><span data-stu-id="c87a3-156">Edit Snippets</span></span>  

1.  <span data-ttu-id="c87a3-157">[Открытие области **фрагментов** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="c87a3-157">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="c87a3-158">В области **фрагменты** выберите имя фрагмента, который вы хотите изменить.</span><span class="sxs-lookup"><span data-stu-id="c87a3-158">In the **Snippets** pane, choose the name of the Snippet that you want to edit.</span></span>  <span data-ttu-id="c87a3-159">Откроется **Редактор кода**.</span><span class="sxs-lookup"><span data-stu-id="c87a3-159">It opens in the **Code Editor**.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-saved.msft.png" alt-text="Редактор кода" lightbox="../media/javascript-sources-snippets-editor-saved.msft.png":::
       <span data-ttu-id="c87a3-161">**Редактор кода**</span><span class="sxs-lookup"><span data-stu-id="c87a3-161">The **Code Editor**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c87a3-162">С помощью **редактора кода** добавьте JavaScript в сниппет.</span><span class="sxs-lookup"><span data-stu-id="c87a3-162">Use the **Code Editor** to add JavaScript to your Snippet.</span></span>  
1.  <span data-ttu-id="c87a3-163">Если рядом с именем фрагмента появится звездочка, это означает, что у вас есть несохраненный код.</span><span class="sxs-lookup"><span data-stu-id="c87a3-163">When an asterisk appears next to the name of your Snippet, it means you have unsaved code.</span></span>  <span data-ttu-id="c87a3-164">Выберите `Control` + `S` \ (Windows, Linux \) или `Command` + `S` \ (macOS \), чтобы сохранить его.</span><span class="sxs-lookup"><span data-stu-id="c87a3-164">Select `Control`+`S` \(Windows, Linux\) or `Command`+`S` \(macOS\) to save.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-unsaved.msft.png" alt-text="Звездочка рядом с именем фрагмента указывает на несохраненный код." lightbox="../media/javascript-sources-snippets-editor-unsaved.msft.png":::
       <span data-ttu-id="c87a3-166">Звездочка рядом с именем фрагмента указывает на несохраненный код.</span><span class="sxs-lookup"><span data-stu-id="c87a3-166">An asterisk next to the Snippet name indicates unsaved code</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="c87a3-167">Выполнение фрагментов кода</span><span class="sxs-lookup"><span data-stu-id="c87a3-167">Run Snippets</span></span>  

### <span data-ttu-id="c87a3-168">Выполнение фрагмента на панели «источники»</span><span class="sxs-lookup"><span data-stu-id="c87a3-168">Run a Snippet from the Sources panel</span></span>  

1.  <span data-ttu-id="c87a3-169">[Открытие области **фрагментов** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="c87a3-169">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="c87a3-170">Выберите имя фрагмента, который вы хотите выполнить.</span><span class="sxs-lookup"><span data-stu-id="c87a3-170">Choose the name of the Snippet that you want to run.</span></span>  <span data-ttu-id="c87a3-171">Фрагмент откроется в **редакторе кода**.</span><span class="sxs-lookup"><span data-stu-id="c87a3-171">The Snippet opens in the **Code Editor**.</span></span>  
1.  <span data-ttu-id="c87a3-172">Выберите команду **выполнить фрагмент** \ ( ![ выполнить фрагмент ][ImageRunSnippetIcon] \) или выберите `Control` + `Enter` \ (Windows, Linux \) или `Command` + `Enter` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="c87a3-172">Choose **Run Snippet** \(![Run Snippet][ImageRunSnippetIcon]\), or select `Control`+`Enter` \(Windows, Linux\) or `Command`+`Enter` \(macOS\).</span></span>  
    
### <span data-ttu-id="c87a3-173">Выполнение фрагмента с помощью меню команд</span><span class="sxs-lookup"><span data-stu-id="c87a3-173">Run a Snippet with the Command Menu</span></span>  

1.  <span data-ttu-id="c87a3-174">Сфокусировать указатель на своем месте в DevTools.</span><span class="sxs-lookup"><span data-stu-id="c87a3-174">Focus your cursor somewhere in DevTools.</span></span>  
1.  <span data-ttu-id="c87a3-175">Выберите `Control` + `Shift` + `P` \ (Windows, Linux \) или `Command` + `Shift` + `P` \ (macOS \), чтобы открыть меню команд.</span><span class="sxs-lookup"><span data-stu-id="c87a3-175">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="c87a3-176">Удалите `>` символ и введите символ, а `!` затем имя фрагмента, который вы хотите выполнить.</span><span class="sxs-lookup"><span data-stu-id="c87a3-176">Delete the `>` character and type the `!` character followed by the name of the Snippet that you want to run.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-run-command.msft.png" alt-text="Выполнение фрагмента из меню команд" lightbox="../media/javascript-search-run-command.msft.png":::
       <span data-ttu-id="c87a3-178">Выполнение фрагмента из **меню команд**</span><span class="sxs-lookup"><span data-stu-id="c87a3-178">Running a Snippet from the **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c87a3-179">Выберите `Enter` , чтобы запустить фрагмент.</span><span class="sxs-lookup"><span data-stu-id="c87a3-179">Select `Enter` to run the Snippet.</span></span>  

## <span data-ttu-id="c87a3-180">Переименование фрагментов</span><span class="sxs-lookup"><span data-stu-id="c87a3-180">Rename Snippets</span></span>  

1.  <span data-ttu-id="c87a3-181">[Открытие области **фрагментов** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="c87a3-181">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="c87a3-182">Наведите указатель мыши на имя фрагмента, откройте контекстное меню (щелкните правой кнопкой мыши \) и выберите команду **Переименовать**.</span><span class="sxs-lookup"><span data-stu-id="c87a3-182">Hover on the Snippet name, open the contextual menu \(right-click\), and choose **Rename**.</span></span>  
    
## <span data-ttu-id="c87a3-183">Удаление фрагментов</span><span class="sxs-lookup"><span data-stu-id="c87a3-183">Delete Snippets</span></span>  

1.  <span data-ttu-id="c87a3-184">[Открытие области **фрагментов** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="c87a3-184">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="c87a3-185">Наведите указатель мыши на имя фрагмента, откройте контекстное меню (щелкните правой кнопкой мыши и выберите команду **Удалить**).</span><span class="sxs-lookup"><span data-stu-id="c87a3-185">Hover on the Snippet name, open the contextual menu \(right-click\), and choose **Remove**.</span></span>  
    
## <span data-ttu-id="c87a3-186">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="c87a3-186">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageMoreTabsIcon]: ../media/more-tabs-icon.msft.png  
[ImageRunSnippetIcon]: ../media/run-snippet-icon.msft.png  

<!-- links -->  

[DevtoolsConsoleIndex]: ../console/index.md "Обзор консоли | Документы Microsoft"  
[DevToolsSourcesTool]: ../sources.md "Общие сведения о средстве «источники» | Документы Microsoft"  
[DevtoolsJavascriptOverrides]: ./overrides.md "Переопределение | Документы Microsoft"  

[MDNScratchpad]: https://developer.mozilla.org/docs/Tools/Scratchpad "Пометок | MDN"  
[WikiBookmarklet]: https://en.wikipedia.org/wiki/Bookmarklet "Кнопка с закладкой | Википедии"  

> [!NOTE]
> <span data-ttu-id="c87a3-192">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c87a3-192">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="c87a3-193">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="c87a3-193">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="c87a3-195">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c87a3-195">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
