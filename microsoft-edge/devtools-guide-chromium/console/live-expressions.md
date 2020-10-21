---
description: Если вы обнаружите, что одинаковые выражения JavaScript отображаются на консоли несколько раз, попробуйте вместо этого использовать выражения в реальном времени.
title: Контроль значений выражений JavaScript в Real-Time с помощью выражений в реальном времени
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: f6787455863f738d0fa4e014ca8fc318ad83a9cb
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125232"
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

# <span data-ttu-id="a1f07-104">Контроль значений выражений JavaScript в Real-Time с помощью выражений в реальном времени</span><span class="sxs-lookup"><span data-stu-id="a1f07-104">Watch JavaScript Expression Values In Real-Time With Live Expressions</span></span>  

<span data-ttu-id="a1f07-105">Если вы обнаружите, что один и тот же выражение JavaScript будет вводиться повторно в консоль, возможно, вам будет проще создать **выражение в реальном времени**.</span><span class="sxs-lookup"><span data-stu-id="a1f07-105">If you find yourself typing the same JavaScript expression in the Console repeatedly, you might find it easier to create a **Live Expression**.</span></span>  <span data-ttu-id="a1f07-106">С помощью **выражений в реальном времени** вы вводите выражение один раз, а затем закрепите его в верхней части консоли.</span><span class="sxs-lookup"><span data-stu-id="a1f07-106">With **Live Expressions** you type an expression once and then pin it to the top of your Console.</span></span>  <span data-ttu-id="a1f07-107">Значение выражения обновляется почти в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="a1f07-107">The value of the expression updates in near real-time.</span></span>  

## <span data-ttu-id="a1f07-108">Создание выражения в реальном времени</span><span class="sxs-lookup"><span data-stu-id="a1f07-108">Create a Live Expression</span></span>  

1.  <span data-ttu-id="a1f07-109">[Открытие консоли][DevToolsConsoleReferenceOpenConsole].</span><span class="sxs-lookup"><span data-stu-id="a1f07-109">[Open the Console][DevToolsConsoleReferenceOpenConsole].</span></span>  
1.  <span data-ttu-id="a1f07-110">Выберите **создать выражение в реальном времени** \ ( ![ создать выражение в реальном времени ][ImageCreateLiveExpressionIcon] ).</span><span class="sxs-lookup"><span data-stu-id="a1f07-110">Choose **Create Live Expression** \(![Create Live Expression][ImageCreateLiveExpressionIcon]\).</span></span>  <span data-ttu-id="a1f07-111">Появится текстовое поле " **выражение в реальном времени** ".</span><span class="sxs-lookup"><span data-stu-id="a1f07-111">The **Live Expression** text box appears.</span></span>  
    
    :::image type="complex" source="../media/console-create-live-expression.msft.png" alt-text="Ввод данных Document. activeElement в текстовое поле &quot;Интерактивное выражение&quot;" lightbox="../media/console-create-live-expression.msft.png":::
       <span data-ttu-id="a1f07-113">Ввод `document.activeElement` текста в текстовое поле " **интерактивное выражение** "</span><span class="sxs-lookup"><span data-stu-id="a1f07-113">Typing `document.activeElement` into the **Live Expression** text box</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="a1f07-114">Выберите `Control` + `Enter` \ (Windows, Linux \) или `Command` + `Enter` \ (macOS \), чтобы сохранить выражение, или выберите его за пределами текстового поля " **выражение в реальном времени** ".</span><span class="sxs-lookup"><span data-stu-id="a1f07-114">Select `Control`+`Enter` \(Windows, Linux\) or `Command`+`Enter` \(macOS\) to save the expression, or choose outside of the **Live Expression** textbox.</span></span>  

## <span data-ttu-id="a1f07-115">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="a1f07-115">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageCreateLiveExpressionIcon]: ../media/create-live-expression-icon.msft.png  

<!-- links -->  

[DevToolsConsoleReferenceOpenConsole]: ./reference.md#open-the-console "Открытие ссылки на консоль консоли | Документы Microsoft"  

> [!NOTE]
> <span data-ttu-id="a1f07-117">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="a1f07-117">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="a1f07-118">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/console/live-expressions) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="a1f07-118">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/live-expressions) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="a1f07-120">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="a1f07-120">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
