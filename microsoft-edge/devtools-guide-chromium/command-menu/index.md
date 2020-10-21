---
description: Руководство по открытию меню команд, выполнению команд, просмотру других действий и т. д.
title: Выполнение команд с помощью командного меню Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 2f13461fdf04e034b324db63c6ec6d9090f80f50
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125281"
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

# <span data-ttu-id="6c667-104">Выполнение команд с помощью командного меню Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="6c667-104">Run Commands With The Microsoft Edge DevTools Command Menu</span></span>  

  

<span data-ttu-id="6c667-105">Меню команд предоставляет быстрый способ навигации по пользовательскому интерфейсу Microsoft Edge DevTools и выполнения стандартных задач, таких как [Отключение JavaScript][JavascriptDisable].</span><span class="sxs-lookup"><span data-stu-id="6c667-105">The Command Menu provides a fast way to navigate the Microsoft Edge DevTools UI and accomplish common tasks, such as [disabling JavaScript][JavascriptDisable].</span></span>  <span data-ttu-id="6c667-106">Возможно, вы знакомы с аналогичной функцией в коде Visual Studio, которая называется [палитрой команд][VisualStudioCodeUICommandPalette], которая была первоначальной для меню команд.</span><span class="sxs-lookup"><span data-stu-id="6c667-106">You may be familiar with a similar feature in Visual Studio Code called the [Command Palette][VisualStudioCodeUICommandPalette], which was the original inspiration for the Command Menu.</span></span>  

:::image type="complex" source="../media/command-menu-run-command-java.msft.png" alt-text="Отключение JavaScript с помощью меню команд" lightbox="../media/command-menu-run-command-java.msft.png":::
   <span data-ttu-id="6c667-108">Отключение JavaScript с помощью меню команд</span><span class="sxs-lookup"><span data-stu-id="6c667-108">Using the Command Menu to disable JavaScript</span></span>  
:::image-end:::  

## <span data-ttu-id="6c667-109">Открытие меню команд</span><span class="sxs-lookup"><span data-stu-id="6c667-109">Open the Command Menu</span></span>  

<span data-ttu-id="6c667-110">Выберите `Control` + `Shift` + `P` \ (Windows, Linux \) или `Command` + `Shift` + `P` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="6c667-110">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\).</span></span> <span data-ttu-id="6c667-111">Или нажмите кнопку **Настройка DevTools** `...` и выберите **команду выполнить**.</span><span class="sxs-lookup"><span data-stu-id="6c667-111">Or choose **Customize And Control DevTools** `...` and then choose **Run Command**.</span></span>  

:::image type="complex" source="../media/command-menu-options-run-command.msft.png" alt-text="Отключение JavaScript с помощью меню команд" lightbox="../media/command-menu-options-run-command.msft.png":::
   <span data-ttu-id="6c667-113">Команда "выполнить"</span><span class="sxs-lookup"><span data-stu-id="6c667-113">Run Command</span></span>  
:::image-end:::  

## <span data-ttu-id="6c667-114">Просмотр других доступных действий</span><span class="sxs-lookup"><span data-stu-id="6c667-114">See other available actions</span></span>  

<span data-ttu-id="6c667-115">Если вы используете рабочий процесс, описанный в разделе [Открыть меню команд](#open-the-command-menu), откроется меню команд с `>` символом, предварительно заданным в текстовом поле меню команды.</span><span class="sxs-lookup"><span data-stu-id="6c667-115">If you use the workflow outlined in [Open the Command Menu](#open-the-command-menu), the Command Menu opens with a `>` character pre-pended to the Command Menu text box.</span></span>  

:::image type="complex" source="../media/command-menu-run-command.msft.png" alt-text="Отключение JavaScript с помощью меню команд" lightbox="../media/command-menu-run-command.msft.png":::
   <span data-ttu-id="6c667-117">Символ команды</span><span class="sxs-lookup"><span data-stu-id="6c667-117">The command character</span></span>  
:::image-end:::  

<span data-ttu-id="6c667-118">Удалите `>` символ и введите текст `?` , чтобы просмотреть другие действия, доступные в меню команд.</span><span class="sxs-lookup"><span data-stu-id="6c667-118">Delete the `>` character and type `?` to see other actions that are available from the Command Menu.</span></span>  

:::image type="complex" source="../media/command-menu-help.msft.png" alt-text="Отключение JavaScript с помощью меню команд" lightbox="../media/command-menu-help.msft.png":::
   <span data-ttu-id="6c667-120">Другие доступные действия</span><span class="sxs-lookup"><span data-stu-id="6c667-120">Other available actions</span></span>  
:::image-end:::  

## <span data-ttu-id="6c667-121">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="6c667-121">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[JavascriptDisable]: ../javascript/disable.md "Отключение JavaScript в Microsoft Edge DevTools | Документы Microsoft"  

[VisualStudioCodeUICommandPalette]: https://code.visualstudio.com/docs/getstarted/userinterface#_command-palette "Палитра команд — пользовательский интерфейс кода Visual Studio"  

> [!NOTE]
> <span data-ttu-id="6c667-124">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="6c667-124">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="6c667-125">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/command-menu/index) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="6c667-125">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/command-menu/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="6c667-127">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="6c667-127">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
