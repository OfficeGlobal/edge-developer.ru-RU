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

# Обзор консоли  

  

На этой странице объясняется, как консоль Microsoft Edge DevTools упрощает разработку веб-страниц.  У консоли есть 2 основного использования: [Просмотр сообщений, записанных в журнал](#viewing-logged-messages) , и [запуск JavaScript](#running-javascript).  

## Просмотр записанных сообщений  

Веб-разработчики часто записывает сообщения на консоль, чтобы убедиться в том, что их JavaScript работает должным образом.  Чтобы записать сообщение в журнал, вставьте выражение, например, `console.log('Hello, Console!')` в сценарий JavaScript.  Когда браузер запускает JavaScript и видит такое выражение, оно заносит сообщение в консоль.  

:::row:::
   :::column span="":::
      HTML и JavaScript для страницы.  
      
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
      На приведенном ниже рисунке показана **консоль** , на которой выводятся результаты загрузки страницы и ожидания 3 секунды.  
      
      :::image type="complex" source="../media/console-console-demo.msft.png" alt-text="Панель консоли" lightbox="../media/console-console-demo.msft.png":::
         Панель **консоли**  
      :::image-end:::  
      
      Попробуйте определить, какие строки кода привели к тому, что браузер зарегистрирует сообщения.  
   :::column-end:::
:::row-end:::  

Веб-разработчики могут регистрировать сообщения по следующим двум основным причинам.  

*   Убедитесь в том, что код выполняется в нужном порядке.  
*   Проверка значений переменных в определенный момент времени.  

В разделе Начало работы [с сообщениями для ведения журнала][DevtoolsConsoleLoggingMessages] вы можете получить практический опыт по ведению журнала.  Полный список методов можно найти в [справочнике по API консоли][DevToolsConsoleAPI] `console` .  Основным различием между методами является способ отображения данных в журнале.  

## Выполнение JavaScript  

**Консоль** также является [REPL][WikiREPLoop].  Вы можете запустить JavaScript на **консоли** для взаимодействия с проверяемой страницей.   

:::row:::
   :::column span="":::
      На приведенном ниже рисунке **консоль** показана рядом с домашней страницей DevTools.  
      
      :::image type="complex" source="../media/devtools-console-empty.msft.png" alt-text="Панель консоли" lightbox="../media/devtools-console-empty.msft.png":::
         Панель **консоли** рядом с домашней страницей DevTools  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      На приведенном ниже рисунке эта же страница отображается после использования **консоли** для изменения верхнего заголовка страницы.
      
      :::image type="complex" source="../media/devtools-console-h1-changed.msft.png" alt-text="Панель консоли" lightbox="../media/devtools-console-h1-changed.msft.png":::
         Использование **консоли** для изменения верхнего заголовка страницы  
      :::image-end:::  
   :::column-end:::
:::row-end:::

Изменение страницы на **консоли** возможно из-за того, что **консоль** имеет полный доступ к [окну][MDNWindow] страницы.  В DevTools есть несколько удобных функций, которые облегчают изучение страницы.  Например, предположим, что ваш сценарий JavaScript содержит функцию с именем `hideModal` .  Выполнение `debug(hideModal)` программы приостанавливает код на первой строке при `hideModal` следующем запуске.  Дополнительные сведения о всех служебных функциях можно найти в [справочнике по API служебных программ для консоли][DevtoolsConsoleUtilitiesDebug].  

При запуске JavaScript вам не нужно взаимодействовать со страницей.  Вы можете использовать **консоль** , чтобы попробовать новый код, не связанный со страницей.  Например, предположим, что вы только что узнали о встроенном методе [Map ()][MDNMap] для массивов JavaScript () и хотите поэкспериментировать с ним.  
**Консоль** — это хорошее место для повторения функции.  

Чтобы узнать больше о том, как запускать JavaScript на **консоли**, перейдите в раздел Начало работы [с JavaScript][DevtoolsConsoleRunningJavascript].  

## Взаимодействие с командой средств разработчика Microsoft Edge  

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
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/console/index) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
