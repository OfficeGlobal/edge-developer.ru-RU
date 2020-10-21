---
description: Фрагменты — это небольшие сценарии, которые можно создавать и запускать на панели «источники» в Microsoft Edge DevTools.  Вы можете получать доступ к ним и запускать их на любой странице.  При запуске фрагмента кода выполняется из контекста открытой на данный момент страницы.
title: Выполнение фрагментов кода JavaScript на любой странице с Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: e353da76a5c354d834b69708c8a8c9e8dbdf9934
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "11124742"
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

# <span data-ttu-id="96791-106">Выполнение фрагментов кода JavaScript на любой странице с Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="96791-106">Run snippets of JavaScript on any page with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="96791-107">Если вы обнаружите, что один и тот же код запускается повторно на [консоли][DevtoolsConsoleIndex] , попробуйте сохранить его как фрагмент кода.</span><span class="sxs-lookup"><span data-stu-id="96791-107">If you find yourself running the same code in the [Console][DevtoolsConsoleIndex] repeatedly, consider saving the code as a Snippet instead.</span></span>  <span data-ttu-id="96791-108">Фрагменты — это сценарии, созданные вами на панели « [источники][DevToolsSourcesPanel] ».</span><span class="sxs-lookup"><span data-stu-id="96791-108">Snippets are scripts that you author in the [Sources][DevToolsSourcesPanel] panel.</span></span>  <span data-ttu-id="96791-109">У них есть доступ к контексту JavaScript на странице, и вы можете запускать их на любой странице.</span><span class="sxs-lookup"><span data-stu-id="96791-109">They have access to the JavaScript context of the page, and you can run them on any page.</span></span>  <span data-ttu-id="96791-110">Фрагменты — это альтернатива для [Закладка][WikiBookmarklet].</span><span class="sxs-lookup"><span data-stu-id="96791-110">Snippets are an alternative to [bookmarklets][WikiBookmarklet].</span></span>  
<span data-ttu-id="96791-111">В Firefox DevTools есть функция, похожая на фрагменты, которые называются [блокнотом][MDNScratchpad].</span><span class="sxs-lookup"><span data-stu-id="96791-111">Firefox DevTools has a feature similar to Snippets called [Scratchpad][MDNScratchpad].</span></span>  

<span data-ttu-id="96791-112">Например, на приведенном ниже рисунке показана домашняя страница DevTools слева и фрагмент исходного кода справа.</span><span class="sxs-lookup"><span data-stu-id="96791-112">For example, in the following figure shows the DevTools homepage on the left and some Snippet source code on the right.</span></span>  

:::image type="complex" source="../media/javascript-sources-snippets-split-screen.msft.png" alt-text="Вид страницы перед выполнением фрагмента" lightbox="../media/javascript-sources-snippets-split-screen.msft.png":::
   <span data-ttu-id="96791-114">Вид страницы перед выполнением фрагмента</span><span class="sxs-lookup"><span data-stu-id="96791-114">How the page looks before running the Snippet</span></span>  
:::image-end:::  

<span data-ttu-id="96791-115">Исходный код фрагмента на предыдущем рисунке.</span><span class="sxs-lookup"><span data-stu-id="96791-115">The Snippet source code from the previous figure.</span></span>  

```javascript
console.log('Hello, Snippets!');
document.body.innerHTML = '';
var p = document.createElement('p');
p.textContent = 'Hello, Snippets!';
document.body.appendChild(p);
```  

<span data-ttu-id="96791-116">На рисунке ниже показана страница после выполнения фрагмента.</span><span class="sxs-lookup"><span data-stu-id="96791-116">In the following figure, the page appears after running the Snippet.</span></span>  <span data-ttu-id="96791-117">Во всплывающем **ящике консоли** выводится `Hello, Snippets!` сообщение о том, что журналы фрагментов, и содержимое страницы полностью меняются.</span><span class="sxs-lookup"><span data-stu-id="96791-117">The **Console Drawer** pops up to display the `Hello, Snippets!` message that the Snippet logs, and the content of the page changes completely.</span></span>  

:::image type="complex" source="../media/javascript-sources-snippets-split-screen-after.msft.png" alt-text="Вид страницы перед выполнением фрагмента" lightbox="../media/javascript-sources-snippets-split-screen-after.msft.png":::
   <span data-ttu-id="96791-119">Вид страницы после выполнения фрагмента</span><span class="sxs-lookup"><span data-stu-id="96791-119">How the page looks after running the Snippet</span></span>  
:::image-end:::  

## <span data-ttu-id="96791-120">Открытие области "фрагменты кода"</span><span class="sxs-lookup"><span data-stu-id="96791-120">Open the Snippets pane</span></span>  

<span data-ttu-id="96791-121">На панели **фрагментов** перечислены ваши фрагменты.</span><span class="sxs-lookup"><span data-stu-id="96791-121">The **Snippets** pane lists your Snippets.</span></span>  <span data-ttu-id="96791-122">Если вы хотите изменить фрагмент, необходимо открыть его из области **фрагментов** .</span><span class="sxs-lookup"><span data-stu-id="96791-122">When you want to edit a Snippet, you need to open it from the **Snippets** pane.</span></span>  

:::image type="complex" source="../media/javascript-sources-snippets-pane.msft.png" alt-text="Вид страницы перед выполнением фрагмента" lightbox="../media/javascript-sources-snippets-pane.msft.png":::
   <span data-ttu-id="96791-124">Область **фрагментов**</span><span class="sxs-lookup"><span data-stu-id="96791-124">The **Snippets** pane</span></span>  
:::image-end:::  

### <span data-ttu-id="96791-125">Открытие области фрагментов с помощью мыши</span><span class="sxs-lookup"><span data-stu-id="96791-125">Open the Snippets pane with a mouse</span></span>  

1.  <span data-ttu-id="96791-126">Перейдите на вкладку **источники** , чтобы открыть панель " **источники** ".</span><span class="sxs-lookup"><span data-stu-id="96791-126">Click the **Sources** tab to open the **Sources** panel.</span></span>  <span data-ttu-id="96791-127">Обычно область **страницы** открывается по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="96791-127">The **Page** pane usually opens by default.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-pane.msft.png" alt-text="Вид страницы перед выполнением фрагмента" lightbox="../media/javascript-sources-page-pane.msft.png":::
       <span data-ttu-id="96791-129">Панель « **источники** » с открытой областью **страницы** в левой части экрана</span><span class="sxs-lookup"><span data-stu-id="96791-129">The **Sources** panel with the **Page** pane open on the left</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="96791-130">Перейдите на вкладку **фрагменты кода** , чтобы открыть область **фрагменты** .</span><span class="sxs-lookup"><span data-stu-id="96791-130">Click the **Snippets** tab to open the **Snippets** pane.</span></span>  <span data-ttu-id="96791-131">**More Tabs** ![ ][ImageMoreTabsIcon] Для доступа к параметру **фрагментов** может потребоваться выбрать дополнительные вкладки \ (дополнительные вкладки \).</span><span class="sxs-lookup"><span data-stu-id="96791-131">You might need to choose **More Tabs** \(![More Tabs][ImageMoreTabsIcon]\) in order to access the **Snippets** option.</span></span>  
    
### <span data-ttu-id="96791-132">Открытие области фрагментов с помощью меню команд</span><span class="sxs-lookup"><span data-stu-id="96791-132">Open the Snippets pane with the Command Menu</span></span>  

1.  <span data-ttu-id="96791-133">Сфокусировать указатель мыши в DevTools.</span><span class="sxs-lookup"><span data-stu-id="96791-133">Focus your cursor somewhere inside of DevTools.</span></span>  
1.  <span data-ttu-id="96791-134">Выберите `Control` + `Shift` + `P` \ (Windows, Linux \) или `Command` + `Shift` + `P` \ (macOS \), чтобы открыть меню команд.</span><span class="sxs-lookup"><span data-stu-id="96791-134">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="96791-135">Начните вводить текст `Snippets` , нажмите кнопку **Показать фрагменты**, а затем выберите `Enter` для запуска команды.</span><span class="sxs-lookup"><span data-stu-id="96791-135">Start typing `Snippets`, choose **Show Snippets**, and then select `Enter` to run the command.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-show-snippets.msft.png" alt-text="Вид страницы перед выполнением фрагмента" lightbox="../media/javascript-search-show-snippets.msft.png":::
       <span data-ttu-id="96791-137">Команда « **Показать фрагменты** »</span><span class="sxs-lookup"><span data-stu-id="96791-137">The **Show Snippets** command</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="96791-138">Создание фрагментов кода</span><span class="sxs-lookup"><span data-stu-id="96791-138">Create Snippets</span></span>  

### <span data-ttu-id="96791-139">Создание фрагмента с помощью панели «источники»</span><span class="sxs-lookup"><span data-stu-id="96791-139">Create a Snippet through the Sources panel</span></span>  

1.  <span data-ttu-id="96791-140">[Открытие области **фрагментов** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="96791-140">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="96791-141">Выберите команду **создать фрагмент**.</span><span class="sxs-lookup"><span data-stu-id="96791-141">Choose **New snippet**.</span></span>  
1.  <span data-ttu-id="96791-142">Введите имя для фрагмента, а затем выберите `Enter` для сохранения.</span><span class="sxs-lookup"><span data-stu-id="96791-142">Enter a name for your Snippet then select `Enter` to save.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-naming.msft.png" alt-text="Вид страницы перед выполнением фрагмента" lightbox="../media/javascript-sources-snippets-naming.msft.png":::
       <span data-ttu-id="96791-144">Присвоение имени фрагменту</span><span class="sxs-lookup"><span data-stu-id="96791-144">Name a Snippet</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="96791-145">Создание фрагмента с помощью меню команд</span><span class="sxs-lookup"><span data-stu-id="96791-145">Create a Snippet through the Command Menu</span></span>  

1.  <span data-ttu-id="96791-146">Сфокусировать указатель мыши в DevTools.</span><span class="sxs-lookup"><span data-stu-id="96791-146">Focus your cursor somewhere inside of DevTools.</span></span>  
1.  <span data-ttu-id="96791-147">Выберите `Control` + `Shift` + `P` \ (Windows, Linux \) или `Command` + `Shift` + `P` \ (macOS \), чтобы открыть меню команд.</span><span class="sxs-lookup"><span data-stu-id="96791-147">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="96791-148">Начните вводить текст `Snippet` , выберите команду **создать фрагмент**, а затем нажмите кнопку, `Enter` чтобы выполнить команду.</span><span class="sxs-lookup"><span data-stu-id="96791-148">Start typing `Snippet`, choose **Create new snippet**, then select `Enter` to run the command.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-create-new-snippet.msft.png" alt-text="Вид страницы перед выполнением фрагмента" lightbox="../media/javascript-search-create-new-snippet.msft.png":::
       <span data-ttu-id="96791-150">Команда для создания нового фрагмента.</span><span class="sxs-lookup"><span data-stu-id="96791-150">The command for creating a new Snippet</span></span>  
    :::image-end:::  
    
<span data-ttu-id="96791-151">Если вы хотите присвоить новому фрагменту настраиваемое имя, просмотрите [фрагменты Rename](#rename-snippets) .</span><span class="sxs-lookup"><span data-stu-id="96791-151">See [Rename Snippets](#rename-snippets) if you'd like to give your new Snippet a custom name.</span></span>  

## <span data-ttu-id="96791-152">Редактирование фрагментов</span><span class="sxs-lookup"><span data-stu-id="96791-152">Edit Snippets</span></span>  

1.  <span data-ttu-id="96791-153">[Открытие области **фрагментов** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="96791-153">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="96791-154">В области **фрагменты** щелкните имя фрагмента, который вы хотите изменить, чтобы открыть его в **редакторе кода**.</span><span class="sxs-lookup"><span data-stu-id="96791-154">In the **Snippets** pane click the name of the Snippet that you want to edit in order to open it in the **Code Editor**.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-saved.msft.png" alt-text="Вид страницы перед выполнением фрагмента" lightbox="../media/javascript-sources-snippets-editor-saved.msft.png":::
       <span data-ttu-id="96791-156">**Редактор кода**</span><span class="sxs-lookup"><span data-stu-id="96791-156">The **Code Editor**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="96791-157">С помощью **редактора кода** добавьте JavaScript в сниппет.</span><span class="sxs-lookup"><span data-stu-id="96791-157">Use the **Code Editor** to add JavaScript to your Snippet.</span></span>  
1.  <span data-ttu-id="96791-158">Если рядом с именем фрагмента появится звездочка, это означает, что у вас есть несохраненный код.</span><span class="sxs-lookup"><span data-stu-id="96791-158">When an asterisk appears next to the name of your Snippet it means you have unsaved code.</span></span> <span data-ttu-id="96791-159">Выберите `Control` + `S` \ (Windows, Linux \) или `Command` + `S` \ (macOS \), чтобы сохранить его.</span><span class="sxs-lookup"><span data-stu-id="96791-159">Select `Control`+`S` \(Windows, Linux\) or `Command`+`S` \(macOS\) to save.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-unsaved.msft.png" alt-text="Вид страницы перед выполнением фрагмента" lightbox="../media/javascript-sources-snippets-editor-unsaved.msft.png":::
       <span data-ttu-id="96791-161">Звездочка рядом с именем фрагмента, обозначающее несохраненный код.</span><span class="sxs-lookup"><span data-stu-id="96791-161">An asterisk next to the Snippet name, which indicates unsaved code</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="96791-162">Выполнение фрагментов кода</span><span class="sxs-lookup"><span data-stu-id="96791-162">Run Snippets</span></span>  

### <span data-ttu-id="96791-163">Выполнение фрагмента на панели «источники»</span><span class="sxs-lookup"><span data-stu-id="96791-163">Run a Snippet from the Sources panel</span></span>  

1.  <span data-ttu-id="96791-164">[Открытие области **фрагментов** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="96791-164">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="96791-165">Щелкните имя фрагмента, который вы хотите выполнить.</span><span class="sxs-lookup"><span data-stu-id="96791-165">Click the name of the Snippet that you want to run.</span></span>  <span data-ttu-id="96791-166">Фрагмент откроется в **редакторе кода**.</span><span class="sxs-lookup"><span data-stu-id="96791-166">The Snippet opens in the **Code Editor**.</span></span>  
1.  <span data-ttu-id="96791-167">Выберите команду **выполнить фрагмент** \ ( ![ выполнить фрагмент ][ImageRunSnippetIcon] \) или выберите `Control` + `Enter` \ (Windows, Linux \) или `Command` + `Enter` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="96791-167">Choose **Run Snippet** \(![Run Snippet][ImageRunSnippetIcon]\), or select `Control`+`Enter` \(Windows, Linux\) or `Command`+`Enter` \(macOS\).</span></span>  
    
### <span data-ttu-id="96791-168">Выполнение фрагмента с помощью меню команд</span><span class="sxs-lookup"><span data-stu-id="96791-168">Run a Snippet with the Command Menu</span></span>  

1.  <span data-ttu-id="96791-169">Сфокусировать указатель мыши в DevTools.</span><span class="sxs-lookup"><span data-stu-id="96791-169">Focus your cursor somewhere inside of DevTools.</span></span>  
1.  <span data-ttu-id="96791-170">Выберите `Control` + `Shift` + `P` \ (Windows, Linux \) или `Command` + `Shift` + `P` \ (macOS \), чтобы открыть меню команд.</span><span class="sxs-lookup"><span data-stu-id="96791-170">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="96791-171">Удалите `>` символ и введите символ, а `!` затем имя фрагмента, который вы хотите выполнить.</span><span class="sxs-lookup"><span data-stu-id="96791-171">Delete the `>` character and type the `!` character followed by the name of the Snippet that you want to run.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-run-command.msft.png" alt-text="Вид страницы перед выполнением фрагмента" lightbox="../media/javascript-search-run-command.msft.png":::
       <span data-ttu-id="96791-173">Выполнение фрагмента из **меню команд**</span><span class="sxs-lookup"><span data-stu-id="96791-173">Running a Snippet from the **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="96791-174">Выберите `Enter` , чтобы запустить фрагмент.</span><span class="sxs-lookup"><span data-stu-id="96791-174">Select `Enter` to run the Snippet.</span></span>  

## <span data-ttu-id="96791-175">Переименование фрагментов</span><span class="sxs-lookup"><span data-stu-id="96791-175">Rename Snippets</span></span>  

1.  <span data-ttu-id="96791-176">[Открытие области **фрагментов** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="96791-176">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="96791-177">Щелкните имя фрагмента правой кнопкой мыши и выберите команду **Переименовать**.</span><span class="sxs-lookup"><span data-stu-id="96791-177">Right-click the Snippet name and choose **Rename**.</span></span>  
    
## <span data-ttu-id="96791-178">Удаление фрагментов</span><span class="sxs-lookup"><span data-stu-id="96791-178">Delete Snippets</span></span>  

1.  <span data-ttu-id="96791-179">[Открытие области **фрагментов** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="96791-179">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="96791-180">Щелкните имя фрагмента правой кнопкой мыши и выберите команду **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="96791-180">Right-click the Snippet name and choose **Remove**.</span></span>  
    
## <span data-ttu-id="96791-181">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="96791-181">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageMoreTabsIcon]: ../media/more-tabs-icon.msft.png  
[ImageRunSnippetIcon]: ../media/run-snippet-icon.msft.png  

<!-- links -->  

[DevtoolsConsoleIndex]: ../console/index.md "Обзор консоли | Документы Microsoft"  
[DevToolsSourcesPanel]: ../sources.md "Обзор панели «источники» | Документы Microsoft"  

[MDNScratchpad]: https://developer.mozilla.org/docs/Tools/Scratchpad "Пометок | MDN"  
[WikiBookmarklet]: https://en.wikipedia.org/wiki/Bookmarklet "Кнопка-«Википедии»"  

> [!NOTE]
> <span data-ttu-id="96791-186">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="96791-186">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="96791-187">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="96791-187">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="96791-189">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="96791-189">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
