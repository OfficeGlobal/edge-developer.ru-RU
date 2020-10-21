---
description: Просмотр и редактирование файлов, создание фрагментов, Отладка JavaScript и Настройка рабочих областей на панели «источники» в Microsoft Edge DevTools.
title: Обзор панели источников
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 971ee6e112daaba828a8b754b63eee73ea51e99e
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125330"
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

# <span data-ttu-id="cf4bb-104">Обзор панели источников</span><span class="sxs-lookup"><span data-stu-id="cf4bb-104">Sources panel overview</span></span>  

<span data-ttu-id="cf4bb-105">С помощью панели DevTools **источники** Microsoft Edge выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="cf4bb-105">Use the Microsoft Edge DevTools **Sources** panel to perform the following actions.</span></span>  

*   <span data-ttu-id="cf4bb-106">[Просмотр файлов](#view-files).</span><span class="sxs-lookup"><span data-stu-id="cf4bb-106">[View files](#view-files).</span></span>  
*   <span data-ttu-id="cf4bb-107">[Редактирование CSS и JavaScript](#edit-css-and-javascript).</span><span class="sxs-lookup"><span data-stu-id="cf4bb-107">[Edit CSS and JavaScript](#edit-css-and-javascript).</span></span>  
*   <span data-ttu-id="cf4bb-108">[Создавайте и сохраняйте **фрагменты кода** JavaScript](#create-save-and-run-snippets), которые можно запускать на любой странице.</span><span class="sxs-lookup"><span data-stu-id="cf4bb-108">[Create and save **Snippets** of JavaScript](#create-save-and-run-snippets), which you may run on any page.</span></span>  <span data-ttu-id="cf4bb-109">**Фрагменты** аналогичны кнопкам для закладок.</span><span class="sxs-lookup"><span data-stu-id="cf4bb-109">**Snippets** are similar to bookmarklets.</span></span>  
*   <span data-ttu-id="cf4bb-110">[Отладка JavaScript](#debug-javascript).</span><span class="sxs-lookup"><span data-stu-id="cf4bb-110">[Debug JavaScript](#debug-javascript).</span></span>  
*   <span data-ttu-id="cf4bb-111">[Настройте рабочую область](#set-up-a-workspace), чтобы изменения, внесенные в DevTools, сохранялись в коде в файловой системе.</span><span class="sxs-lookup"><span data-stu-id="cf4bb-111">[Set up a Workspace](#set-up-a-workspace), so that changes you make in DevTools get saved to the code on your file system.</span></span>  
    
## <span data-ttu-id="cf4bb-112">Просмотр файлов</span><span class="sxs-lookup"><span data-stu-id="cf4bb-112">View files</span></span>  

<span data-ttu-id="cf4bb-113">Используйте область **страниц** для просмотра всех ресурсов, загруженных страницей.</span><span class="sxs-lookup"><span data-stu-id="cf4bb-113">Use the **Page** pane to view all of the resources that the page has loaded.</span></span>

:::image type="complex" source="./media/sources-page-pane.msft.png" alt-text="Область страницы" lightbox="./media/sources-page-pane.msft.png":::
   <span data-ttu-id="cf4bb-115">Область **страницы**</span><span class="sxs-lookup"><span data-stu-id="cf4bb-115">The **Page** pane</span></span>  
:::image-end:::  

<span data-ttu-id="cf4bb-116">Упорядочение области **страницы** .</span><span class="sxs-lookup"><span data-stu-id="cf4bb-116">How the **Page** pane is organized:</span></span>  
*   <span data-ttu-id="cf4bb-117">Верхний уровень (например, `top` на предыдущем рисунке) представляет [рамку HTML][W3CHtml4Frames].</span><span class="sxs-lookup"><span data-stu-id="cf4bb-117">The top-level, such as `top` in the previous figure, represents an [HTML frame][W3CHtml4Frames].</span></span>  <span data-ttu-id="cf4bb-118">Найдите `top` на каждой странице, которую вы посещаете.</span><span class="sxs-lookup"><span data-stu-id="cf4bb-118">Find `top` on every page that you visit.</span></span>  `top` <span data-ttu-id="cf4bb-119">представляет рамку основного документа.</span><span class="sxs-lookup"><span data-stu-id="cf4bb-119">represents the main document frame.</span></span>  
*   <span data-ttu-id="cf4bb-120">Второй уровень (например, `docs.microsoft.com` на предыдущем рисунке) представляет [источник][HtmlstandardOrigin].</span><span class="sxs-lookup"><span data-stu-id="cf4bb-120">The second-level, such as `docs.microsoft.com` in the previous figure, represents an [origin][HtmlstandardOrigin].</span></span>  
*   <span data-ttu-id="cf4bb-121">Третий уровень, четвертый уровень и т. д. — каталоги и ресурсы, загруженные из этого источника.</span><span class="sxs-lookup"><span data-stu-id="cf4bb-121">The third-level, fourth-level, and so on, represent directories and resources that were loaded from that origin.</span></span>  <span data-ttu-id="cf4bb-122">Например, в приведенном выше рисунке полный путь `devtools-guide-chromium` к ресурсу</span><span class="sxs-lookup"><span data-stu-id="cf4bb-122">For example, in the previous figure the full path to the resource `devtools-guide-chromium` is</span></span> `docs.microsoft.com/en-us/microsoft-edge/devtools-guide-chromium`  
    
<span data-ttu-id="cf4bb-123">Щелкните файл в области **страницы** , чтобы просмотреть содержимое в области " **Редактор** ".</span><span class="sxs-lookup"><span data-stu-id="cf4bb-123">Click a file in the **Page** pane to view the contents in the **Editor** pane.</span></span>  <span data-ttu-id="cf4bb-124">Вы можете просматривать файлы любого типа.</span><span class="sxs-lookup"><span data-stu-id="cf4bb-124">You may view any type of file.</span></span>  <span data-ttu-id="cf4bb-125">Для изображений на экран выводится предварительный просмотр изображения.</span><span class="sxs-lookup"><span data-stu-id="cf4bb-125">For images, a preview of the image is displayed.</span></span>  

:::image type="complex" source="./media/sources-editor-pane.msft.png" alt-text="Область страницы" lightbox="./media/sources-editor-pane.msft.png":::
   <span data-ttu-id="cf4bb-127">Просмотр содержимого `a4d10f71.index-docs.js` в области " **Редактор** "</span><span class="sxs-lookup"><span data-stu-id="cf4bb-127">View the contents of `a4d10f71.index-docs.js` in the **Editor** pane</span></span>  
:::image-end:::  

## <span data-ttu-id="cf4bb-128">Редактирование CSS и JavaScript</span><span class="sxs-lookup"><span data-stu-id="cf4bb-128">Edit CSS and JavaScript</span></span>  

<span data-ttu-id="cf4bb-129">Для изменения CSS и JavaScript используйте область " **Редактор** ".</span><span class="sxs-lookup"><span data-stu-id="cf4bb-129">Use the **Editor** pane to edit CSS and JavaScript.</span></span>  <span data-ttu-id="cf4bb-130">DevTools обновляет страницу, чтобы выполнить новый код.</span><span class="sxs-lookup"><span data-stu-id="cf4bb-130">DevTools updates the page to run your new code.</span></span>  <span data-ttu-id="cf4bb-131">Например, если вы изменяете CSS-файл, добавив правило стиля ниже:</span><span class="sxs-lookup"><span data-stu-id="cf4bb-131">For example, if you edit a CSS file by adding the style rule below:</span></span>

```css
.metadata.page-metadata {
    color: red;
}
```

<span data-ttu-id="cf4bb-132">Изменения вступают в силу немедленно.</span><span class="sxs-lookup"><span data-stu-id="cf4bb-132">That change should take effect immediately.</span></span>

:::image type="complex" source="./media/edit-css.msft.png" alt-text="Область страницы" lightbox="./media/edit-css.msft.png":::
   <span data-ttu-id="cf4bb-134">Редактирование CSS на панели « **Редактор** » для изменения цвета текста подзаголовка на красный</span><span class="sxs-lookup"><span data-stu-id="cf4bb-134">Edit CSS in the **Editor** pane to change the text color of the subtitle to red</span></span>  
:::image-end:::  

<span data-ttu-id="cf4bb-135">Изменения в CSS вступают в силу немедленно, сохранение не требуется.</span><span class="sxs-lookup"><span data-stu-id="cf4bb-135">CSS changes take effect immediately, no save needed.</span></span>  <span data-ttu-id="cf4bb-136">Чтобы изменения в JavaScript вступили в силу, выберите `Control` + `S` \ (Windows, Linux \) или `Command` + `S` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="cf4bb-136">For JavaScript changes to take effect, select `Control`+`S` \(Windows, Linux\) or `Command`+`S` \(macOS\).</span></span>  <span data-ttu-id="cf4bb-137">DevTools не выполняет повторно сценарий, поэтому изменения, которые вступают в силу, выполняются только в рамках функций.</span><span class="sxs-lookup"><span data-stu-id="cf4bb-137">DevTools does not re-run a script, so the only JavaScript changes that take effect are those that you make inside of functions.</span></span>  <span data-ttu-id="cf4bb-138">Например, на приведенном ниже рисунке обратите внимание на `console.log('A')` то, что не выполняется, в то время как `console.log('B')` оно делает.</span><span class="sxs-lookup"><span data-stu-id="cf4bb-138">For example, in the following figure, notice how `console.log('A')` does not run, whereas `console.log('B')` does.</span></span>  <span data-ttu-id="cf4bb-139">Если после внесения изменений DevTools повторно запускает весь сценарий, он `A` будет записан в журнал на **консоли**.</span><span class="sxs-lookup"><span data-stu-id="cf4bb-139">If DevTools re-runs the entire script after making the change, then the text `A` would have been logged to the **Console**.</span></span>  

:::image type="complex" source="./media/edit-js.msft.png" alt-text="Область страницы" lightbox="./media/edit-js.msft.png":::
   <span data-ttu-id="cf4bb-141">Редактирование JavaScript в области " **Редактор** "</span><span class="sxs-lookup"><span data-stu-id="cf4bb-141">Editing JavaScript in the **Editor** pane</span></span>  
:::image-end:::  

<span data-ttu-id="cf4bb-142">DevTools удаляет изменения стилей CSS и JavaScript при повторной загрузке страницы.</span><span class="sxs-lookup"><span data-stu-id="cf4bb-142">DevTools erases your CSS and JavaScript changes when you reload the page.</span></span>  <span data-ttu-id="cf4bb-143">Перейдите к разделу [Настройка рабочей области](#set-up-a-workspace) , чтобы получить сведения о том, как сохранить изменения в файловой системе.</span><span class="sxs-lookup"><span data-stu-id="cf4bb-143">Navigate to [Set up a Workspace](#set-up-a-workspace) to learn how to save the changes to your file system.</span></span>  

## <span data-ttu-id="cf4bb-144">Создание, сохранение и запуск фрагментов</span><span class="sxs-lookup"><span data-stu-id="cf4bb-144">Create, save, and run Snippets</span></span>  

<span data-ttu-id="cf4bb-145">Фрагменты — это сценарии, которые можно запускать на любой странице.</span><span class="sxs-lookup"><span data-stu-id="cf4bb-145">Snippets are scripts which you may run on any page.</span></span>  <span data-ttu-id="cf4bb-146">Предположим, что вы повторно вводите на **консоли**следующий код, чтобы вставить библиотеку jQuery на страницу, чтобы можно было запускать команды jQuery из **консоли**:</span><span class="sxs-lookup"><span data-stu-id="cf4bb-146">Imagine that you repeatedly type out the following code in the **Console**, in order to insert the jQuery library into a page, so that you may run jQuery commands from the **Console**:</span></span>  

```javascript
let script = document.createElement('script');
script.src = 'https://code.jquery.com/jquery-3.2.1.min.js';
script.crossOrigin = 'anonymous';
script.integrity = 'sha256-hwg4gsxgFZhOsEEamdOYGBf13FyQuiTwlAQgxVSNgt4=';
document.head.appendChild(script);
```  

<span data-ttu-id="cf4bb-147">Вместо этого вы можете сохранить этот код во **фрагменте** и выполнить его с помощью нескольких нажатий кнопки, когда вам понадобится.</span><span class="sxs-lookup"><span data-stu-id="cf4bb-147">Instead, you may save this code in a **Snippet** and run it with a couple of button clicks, any time you need it.</span></span>  <span data-ttu-id="cf4bb-148">DevTools сохранит **фрагмент** в файловой системе.</span><span class="sxs-lookup"><span data-stu-id="cf4bb-148">DevTools saves the **Snippet** to your file system.</span></span>  

:::image type="complex" source="./media/snippet.msft.png" alt-text="Область страницы" lightbox="./media/snippet.msft.png":::
   <span data-ttu-id="cf4bb-150">**Фрагмент кода** , который вставляет библиотеку jQuery на страницу</span><span class="sxs-lookup"><span data-stu-id="cf4bb-150">A **Snippet** that inserts the jQuery library into a page</span></span>  
:::image-end:::  

<span data-ttu-id="cf4bb-151">Чтобы выполнить **фрагмент кода**, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="cf4bb-151">To run a **Snippet**:</span></span>

*   <span data-ttu-id="cf4bb-152">Откройте файл с помощью области **фрагментов** и выберите команду **выполнить** \ ( ![ кнопка выполнить \ ][ImageRunIcon] ).</span><span class="sxs-lookup"><span data-stu-id="cf4bb-152">Open the file using the **Snippets** pane, and choose **Run** \(![The Run button][ImageRunIcon]\).</span></span>  
*   <span data-ttu-id="cf4bb-153">Откройте **[меню команд][DevtoolsGuideChromiumCommandMenuIndex]**, удалите `>` символ, введите `!` имя, введите его **и**нажмите кнопку `Enter` .</span><span class="sxs-lookup"><span data-stu-id="cf4bb-153">Open the **[Command Menu][DevtoolsGuideChromiumCommandMenuIndex]**, delete the `>` character, type `!`, type the name of your **Snippet**, then select `Enter`.</span></span>  
    
<span data-ttu-id="cf4bb-154">Перейдите к разделу [выполнение фрагментов кода на любой странице][DevtoolsGuideChromiumJavascriptSnippets] , чтобы узнать больше.</span><span class="sxs-lookup"><span data-stu-id="cf4bb-154">Navigate to [Run Snippets Of Code From Any Page][DevtoolsGuideChromiumJavascriptSnippets] to learn more.</span></span>

## <span data-ttu-id="cf4bb-155">Отладка JavaScript</span><span class="sxs-lookup"><span data-stu-id="cf4bb-155">Debug JavaScript</span></span>  

<span data-ttu-id="cf4bb-156">Вместо того `console.log()` , чтобы использовать для определения того, где произошел сбой JavaScript, рекомендуется использовать инструменты отладки Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="cf4bb-156">Rather than using `console.log()` to infer where your JavaScript is going wrong, consider using the Microsoft Edge DevTools debugging tools, instead.</span></span>  <span data-ttu-id="cf4bb-157">Общая идея состоит в том, чтобы установить точку останова, которая является умышленно остановленным местом в вашем коде, и пошаговое руководство по коду — по одной строке за раз.</span><span class="sxs-lookup"><span data-stu-id="cf4bb-157">The general idea is to set a breakpoint, which is an intentional stopping place in your code, and then step through the runtime of your code, one line at a time.</span></span>  <span data-ttu-id="cf4bb-158">По мере выполнения кода вы можете просматривать и изменять значения всех текущих заданных свойств и переменных, запускать JavaScript на **консоли**и т. д.</span><span class="sxs-lookup"><span data-stu-id="cf4bb-158">As you step through the code, you may view and change the values of all currently-defined properties and variables, run JavaScript in the **Console**, and more.</span></span>

<span data-ttu-id="cf4bb-159">Перейдите к разделу [Начало отладки JavaScript][DevtoolsGuideChromiumJavascriptIndex] , чтобы ознакомиться с основами отладки в DevTools.</span><span class="sxs-lookup"><span data-stu-id="cf4bb-159">Navigate to [Get Started With Debugging JavaScript][DevtoolsGuideChromiumJavascriptIndex] to learn the basics of debugging in DevTools.</span></span>

:::image type="complex" source="./media/debugging.msft.png" alt-text="Область страницы" lightbox="./media/debugging.msft.png":::
   <span data-ttu-id="cf4bb-161">Отладка JavaScript</span><span class="sxs-lookup"><span data-stu-id="cf4bb-161">Debug JavaScript</span></span>  
:::image-end:::  

## <span data-ttu-id="cf4bb-162">Настройка рабочей области</span><span class="sxs-lookup"><span data-stu-id="cf4bb-162">Set up a Workspace</span></span>  

<span data-ttu-id="cf4bb-163">По умолчанию при редактировании файла на панели « **источники** » эти изменения теряются при повторной загрузке страницы.</span><span class="sxs-lookup"><span data-stu-id="cf4bb-163">By default, when you edit a file in the **Sources** panel, those changes are lost when you reload the page.</span></span>  <span data-ttu-id="cf4bb-164">**Рабочие области** позволяют сохранить изменения, внесенные в DevTools, в файловую систему.</span><span class="sxs-lookup"><span data-stu-id="cf4bb-164">**Workspaces** enable you to save the changes that you make in DevTools to your file system.</span></span>  <span data-ttu-id="cf4bb-165">По сути, DevTools можно использовать в качестве редактора кода.</span><span class="sxs-lookup"><span data-stu-id="cf4bb-165">Essentially, DevTools is able to be used as your code editor.</span></span>

<span data-ttu-id="cf4bb-166">Перейдите к разделу [изменение файлов с помощью рабочих областей][DevtoolsGuideChromiumWorkspacesIndex] , чтобы приступить к работе.</span><span class="sxs-lookup"><span data-stu-id="cf4bb-166">Navigate to [Edit Files With Workspaces][DevtoolsGuideChromiumWorkspacesIndex] to get started.</span></span>

## <span data-ttu-id="cf4bb-167">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="cf4bb-167">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](./includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageRunIcon]: ./media/run-snippet-icon.msft.png  

<!-- links -->  

[DevtoolsGuideChromiumCommandMenuIndex]: ./command-menu/index.md "Выполнение команд с помощью командного меню Microsoft Edge DevTools"  
[DevtoolsGuideChromiumJavascriptIndex]: ./javascript/index.md "Начало работы с отладкой JavaScript в Microsoft Edge DevTools"  
[DevtoolsGuideChromiumJavascriptSnippets]: ./javascript/snippets.md "Выполнение фрагментов кода JavaScript на любой странице с Microsoft Edge DevTools"  
[DevtoolsGuideChromiumWorkspacesIndex]: ./workspaces/index.md "Редактирование файлов с помощью рабочих областей"  

[HtmlstandardOrigin]: https://html.spec.whatwg.org/multipage/origin.html#origin "Современный: HTML Standard"  

[W3CHtml4Frames]: https://w3.org/TR/html401/present/frames.html "Кадры | PNG"  

> [!NOTE]
> <span data-ttu-id="cf4bb-174">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="cf4bb-174">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="cf4bb-175">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/sources) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="cf4bb-175">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/sources) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="cf4bb-177">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="cf4bb-177">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
