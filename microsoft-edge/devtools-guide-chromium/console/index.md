---
description: В основном используются консоль Microsoft Edge DevTools для ведения журнала сообщений и выполнения JavaScript.
title: Обзор консоли
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 32272c3f76f715566ced66d11346985dc95dd290
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125267"
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

# <span data-ttu-id="d0c04-104">Обзор консоли</span><span class="sxs-lookup"><span data-stu-id="d0c04-104">Console Overview</span></span>  

  

<span data-ttu-id="d0c04-105">На этой странице объясняется, как консоль Microsoft Edge DevTools упрощает разработку веб-страниц.</span><span class="sxs-lookup"><span data-stu-id="d0c04-105">This page explains how the Microsoft Edge DevTools Console makes it easier to develop web pages.</span></span>  <span data-ttu-id="d0c04-106">У консоли есть 2 основного использования: [Просмотр сообщений, записанных в журнал](#viewing-logged-messages) , и [запуск JavaScript](#running-javascript).</span><span class="sxs-lookup"><span data-stu-id="d0c04-106">The Console has 2 main uses: [viewing logged messages](#viewing-logged-messages) and [running JavaScript](#running-javascript).</span></span>  

## <span data-ttu-id="d0c04-107">Просмотр записанных сообщений</span><span class="sxs-lookup"><span data-stu-id="d0c04-107">Viewing logged messages</span></span>  

<span data-ttu-id="d0c04-108">Веб-разработчики часто записывает сообщения на консоль, чтобы убедиться в том, что их JavaScript работает должным образом.</span><span class="sxs-lookup"><span data-stu-id="d0c04-108">Web developers often log messages to the Console to make sure that their JavaScript is working as expected.</span></span>  <span data-ttu-id="d0c04-109">Чтобы записать сообщение в журнал, вставьте выражение, например, `console.log('Hello, Console!')` в сценарий JavaScript.</span><span class="sxs-lookup"><span data-stu-id="d0c04-109">To log a message, you insert an expression like `console.log('Hello, Console!')` into your JavaScript.</span></span>  <span data-ttu-id="d0c04-110">Когда браузер запускает JavaScript и видит такое выражение, оно заносит сообщение в консоль.</span><span class="sxs-lookup"><span data-stu-id="d0c04-110">When the browser runs your JavaScript and sees an expression like that, it logs the message to the Console.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="d0c04-111">HTML и JavaScript для страницы.</span><span class="sxs-lookup"><span data-stu-id="d0c04-111">The HTML and JavaScript for the page.</span></span>  
      
      ```html
      <!doctype html>
      <html>
          <head>
              <title>Console Demo</title>
          </head>
          <body>
              <h1>Hello, World!</h1>
              <script>
                  console.log('Loading!');
                  const h1 = document.querySelector('h1');
                  console.log(h1.textContent);
                  console.assert(document.querySelector('h2'), 'h2 not found!');
                  const artists = [
                      { first: 'René', last: 'Magritte' },
                      { first: 'Chaim', last: 'Soutine' },
                        
                  ];
                  console.table(artists);
                  setTimeout(() => {
                      h1.textContent = 'Hello, Console!';
                      console.log(h1.textContent);
                  }, 3000);
              </script>
          </body>
      </html>
      ```  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="d0c04-112">На приведенном ниже рисунке показана **консоль** , на которой выводятся результаты загрузки страницы и ожидания 3 секунды.</span><span class="sxs-lookup"><span data-stu-id="d0c04-112">In the following figure, the **Console** displays the results of loading the page and waiting 3 seconds.</span></span>  
      
      :::image type="complex" source="../media/console-console-demo.msft.png" alt-text="Панель консоли" lightbox="../media/console-console-demo.msft.png":::
         <span data-ttu-id="d0c04-114">Панель **консоли**</span><span class="sxs-lookup"><span data-stu-id="d0c04-114">The **Console** panel</span></span>  
      :::image-end:::  
      
      <span data-ttu-id="d0c04-115">Попробуйте определить, какие строки кода привели к тому, что браузер зарегистрирует сообщения.</span><span class="sxs-lookup"><span data-stu-id="d0c04-115">Try to determine which lines of code caused the browser to log the messages.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="d0c04-116">Веб-разработчики могут регистрировать сообщения по следующим двум основным причинам.</span><span class="sxs-lookup"><span data-stu-id="d0c04-116">Web developers log messages for the following 2 general reasons.</span></span>  

*   <span data-ttu-id="d0c04-117">Убедитесь в том, что код выполняется в нужном порядке.</span><span class="sxs-lookup"><span data-stu-id="d0c04-117">Making sure that code is running in the right order.</span></span>  
*   <span data-ttu-id="d0c04-118">Проверка значений переменных в определенный момент времени.</span><span class="sxs-lookup"><span data-stu-id="d0c04-118">Inspecting the values of variables at a certain moment in time.</span></span>  

<span data-ttu-id="d0c04-119">В разделе Начало работы [с сообщениями для ведения журнала][DevtoolsConsoleLoggingMessages] вы можете получить практический опыт по ведению журнала.</span><span class="sxs-lookup"><span data-stu-id="d0c04-119">See [Get Started With Logging Messages][DevtoolsConsoleLoggingMessages] to get hands-on experience with logging.</span></span>  <span data-ttu-id="d0c04-120">Полный список методов можно найти в [справочнике по API консоли][DevToolsConsoleAPI] `console` .</span><span class="sxs-lookup"><span data-stu-id="d0c04-120">See the [Console API Reference][DevToolsConsoleAPI] to browse the full list of `console` methods.</span></span>  <span data-ttu-id="d0c04-121">Основным различием между методами является способ отображения данных в журнале.</span><span class="sxs-lookup"><span data-stu-id="d0c04-121">The main difference between the methods is how the data being logged is displayed.</span></span>  

## <span data-ttu-id="d0c04-122">Выполнение JavaScript</span><span class="sxs-lookup"><span data-stu-id="d0c04-122">Running JavaScript</span></span>  

<span data-ttu-id="d0c04-123">**Консоль** также является [REPL][WikiREPLoop].</span><span class="sxs-lookup"><span data-stu-id="d0c04-123">The **Console** is also a [REPL][WikiREPLoop].</span></span>  <span data-ttu-id="d0c04-124">Вы можете запустить JavaScript на **консоли** для взаимодействия с проверяемой страницей.</span><span class="sxs-lookup"><span data-stu-id="d0c04-124">You may run JavaScript in the **Console** to interact with the page being inspected.</span></span>   

:::row:::
   :::column span="":::
      <span data-ttu-id="d0c04-125">На приведенном ниже рисунке **консоль** показана рядом с домашней страницей DevTools.</span><span class="sxs-lookup"><span data-stu-id="d0c04-125">In the following figure, the **Console** is shown next to the DevTools homepage.</span></span>  
      
      :::image type="complex" source="../media/devtools-console-empty.msft.png" alt-text="Панель консоли" lightbox="../media/devtools-console-empty.msft.png":::
         <span data-ttu-id="d0c04-127">Панель **консоли** рядом с домашней страницей DevTools</span><span class="sxs-lookup"><span data-stu-id="d0c04-127">The **Console** panel next to the DevTools homepage</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="d0c04-128">На приведенном ниже рисунке эта же страница отображается после использования **консоли** для изменения верхнего заголовка страницы.</span><span class="sxs-lookup"><span data-stu-id="d0c04-128">In the following figure, the same page is shown after using the **Console** to change the top heading of the page.</span></span>
      
      :::image type="complex" source="../media/devtools-console-h1-changed.msft.png" alt-text="Панель консоли" lightbox="../media/devtools-console-h1-changed.msft.png":::
         <span data-ttu-id="d0c04-130">Использование **консоли** для изменения верхнего заголовка страницы</span><span class="sxs-lookup"><span data-stu-id="d0c04-130">Use the **Console** to change the top heading of the page</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

<span data-ttu-id="d0c04-131">Изменение страницы на **консоли** возможно из-за того, что **консоль** имеет полный доступ к [окну][MDNWindow] страницы.</span><span class="sxs-lookup"><span data-stu-id="d0c04-131">Modifying the page from the **Console** is possible because the **Console** has full access to the [window][MDNWindow] of the page.</span></span>  <span data-ttu-id="d0c04-132">В DevTools есть несколько удобных функций, которые облегчают изучение страницы.</span><span class="sxs-lookup"><span data-stu-id="d0c04-132">DevTools has a few convenience functions that make it easier to inspect a page.</span></span>  <span data-ttu-id="d0c04-133">Например, предположим, что ваш сценарий JavaScript содержит функцию с именем `hideModal` .</span><span class="sxs-lookup"><span data-stu-id="d0c04-133">For example, suppose that your JavaScript contains a function called `hideModal`.</span></span>  <span data-ttu-id="d0c04-134">Выполнение `debug(hideModal)` программы приостанавливает код на первой строке при `hideModal` следующем запуске.</span><span class="sxs-lookup"><span data-stu-id="d0c04-134">Running `debug(hideModal)` pauses your code on the first line of `hideModal` the next time that you run it.</span></span>  <span data-ttu-id="d0c04-135">Дополнительные сведения о всех служебных функциях можно найти в [справочнике по API служебных программ для консоли][DevtoolsConsoleUtilitiesDebug].</span><span class="sxs-lookup"><span data-stu-id="d0c04-135">For more information about the full list of utility functions, navigate to [Console Utilities API Reference][DevtoolsConsoleUtilitiesDebug].</span></span>  

<span data-ttu-id="d0c04-136">При запуске JavaScript вам не нужно взаимодействовать со страницей.</span><span class="sxs-lookup"><span data-stu-id="d0c04-136">When you run JavaScript you do not have to interact with the page.</span></span>  <span data-ttu-id="d0c04-137">Вы можете использовать **консоль** , чтобы попробовать новый код, не связанный со страницей.</span><span class="sxs-lookup"><span data-stu-id="d0c04-137">You may use the **Console** to try out new code unrelated to the page.</span></span>  <span data-ttu-id="d0c04-138">Например, предположим, что вы только что узнали о встроенном методе [Map ()][MDNMap] для массивов JavaScript () и хотите поэкспериментировать с ним.</span><span class="sxs-lookup"><span data-stu-id="d0c04-138">For example, suppose you just learned about the built-in JavaScript Array [map()][MDNMap] method, and you want to experiment with it.</span></span>  
<span data-ttu-id="d0c04-139">**Консоль** — это хорошее место для повторения функции.</span><span class="sxs-lookup"><span data-stu-id="d0c04-139">The **Console** is a good place to try out the function.</span></span>  

<span data-ttu-id="d0c04-140">Чтобы узнать больше о том, как запускать JavaScript на **консоли**, перейдите в раздел Начало работы [с JavaScript][DevtoolsConsoleRunningJavascript].</span><span class="sxs-lookup"><span data-stu-id="d0c04-140">For more hands-on experience with running JavaScript in the **Console**, navigate to [Get Started With Running JavaScript][DevtoolsConsoleRunningJavascript].</span></span>  

## <span data-ttu-id="d0c04-141">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="d0c04-141">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsConsoleAPI]: ./api.md "Справочник по API консоли | Документы Microsoft"  
[DevtoolsConsoleLoggingMessages]: ./log.md "Начало работы с сообщениями в журнале на консоли | Документы Microsoft"  
[DevtoolsConsoleRunningJavascript]: ./javascript.md "Начало работы с JavaScript на консоли | Документы Microsoft"  
[DevtoolsConsoleUtilitiesDebug]: ./utilities.md#debug "Справочник по API для служебных программ консоли | Документы Microsoft"  

[MDNMap]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/map "Array. prototype. Map () | MDN"  
[MDNWindow]: https://developer.mozilla.org/docs/Web/API/Window "Окно | MDN"  

[WikiREPLoop]: https://en.wikipedia.org/wiki/Read%E2%80%93eval%E2%80%93print_loop "Read – eval — цикл печати — Википедии"  

> [!NOTE]
> <span data-ttu-id="d0c04-149">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="d0c04-149">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="d0c04-150">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/console/index) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="d0c04-150">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="d0c04-152">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="d0c04-152">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
