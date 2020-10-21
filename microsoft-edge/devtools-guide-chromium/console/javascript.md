---
description: Сведения о том, как запускать JavaScript на консоли.
title: Начало работы с JavaScript на консоли
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 6537cb07b52ef6b8be4b1ea7d9420bf2307d3fd5
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125246"
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

# Начало работы с JavaScript на консоли  

В этом интерактивном учебнике показано, как запустить JavaScript на **консоли**Microsoft Edge DevTools.  Дополнительные сведения о том, как записывать сообщения на **консоль**, можно найти в разделе Начало [работы с сообщениями журнала][DevToolsConsoleLoggingMessages].  Дополнительные сведения о том, как приостановить код JavaScript и прокручивать по одной строке за один раз, можно найти в статье [Начало работы с отладкой JavaScript][DevToolsJavascriptIndex].  

:::image type="complex" source="../media/console-javascript-example-console-playground.msft.png" alt-text="На консоли" lightbox="../media/console-javascript-example-console-playground.msft.png":::
   На **консоли**  
:::image-end:::  

## Обзор  

**Консоль** — это [REPL][WikiReadEvalPrintLoop], который означает чтение, оценку, печать и зацикливание.  Она считывает JavaScript, который вы вводите в него, оценивает код, выводит результат [выражения][2alityExpressionsVersusStatements]и осуществляет переход к первому шагу.  

## Настройка DevTools  

Этот учебник предназначен для того, чтобы открыть демонстрацию и попробовать все рабочие процессы самостоятельно.  После того как вы будете физически подписаться на нее, вы, наверное, захотите запомнить рабочие процессы позже.

1.  `Control` + `Shift` + `J` Чтобы открыть консоль, выберите \ (Windows, Linux \) или `Command` + `Option` + `J` \ (macOS \ **Console**).  
1.  Удерживайте клавишу `Control` \ (Windows, Linux \) или `Command` \ (macOS \) и выберите **пример кода JavaScript на консоли** , чтобы открыть его в новом окне.  
    
    *   [Пример сценария на консоли][GlitchConsoleJavascriptExample]  
    
    :::image type="complex" source="../media/console-javascript-example-console-empty.msft.png" alt-text="На консоли" lightbox="../media/console-javascript-example-console-empty.msft.png":::
       Страница примера JavaScript на консоли в левой части экрана и DevTools справа  
    :::image-end:::  
    
## Просмотр и изменение JavaScript или DOM страницы  

При сборке или отладке страницы часто бывает полезно запускать инструкции на **консоли** , чтобы изменить внешний вид или выполнение страницы.  
    
1.  Обратите внимание на текст на кнопке.  
1.  Введите текст `document.getElementById('hello').textContent = 'Hello, Console!'` на **консоли** и выберите `Enter` , чтобы вычислить выражение.  Обратите внимание на то, как изменится текст внутри кнопки.  
    
    :::image type="complex" source="../media/console-javascript-example-console-change-button-text.msft.png" alt-text="На консоли" lightbox="../media/console-javascript-example-console-change-button-text.msft.png":::
       Внешний вид **консоли** после вычисления выражения  
    :::image-end:::  
    
    Под кодом, который вы проверили `"Hello, Console!"` .  Отзывайте 4 шага REPL: чтение, оценка, печать, цикл.  После оценки кода программа REPL выводит результат выражения.  Это `"Hello, Console!"` должно быть результатом вычисления `document.getElementById('hello').textContent = 'Hello, Console!'` .  
    
## Запуск произвольного кода JavaScript, не связанного со страницей  

Иногда требуется, чтобы код Песочница в том месте, где вы можете протестировать какой-либо код, или опробуйте новые возможности JavaScript, с которыми вы не знакомы.  Консоль — это идеальное место для экспериментов такого рода.  

1.  Введите текст `5 + 15` в окне консоли и выберите `Enter` этот вариант, чтобы вычислить выражение. Консоль печатает результат выражения под кодом.  На приведенном ниже рисунке на **консоли** должны отобразиться результаты после вычисления выражения.  

1.  На **консоли**введите следующий код.  Попробуйте ввести его, а затем построчно, а не скопировав.  
    
    ```javascript
    function add(a, b=20)
    ```  
    
    Если вы не знакомы с `b=20` синтаксисом, перейдите в раздел [Определение значений по умолчанию для аргументов функций][Esma6DefaultParameterValues].  
    
1.  Теперь запустите определенную функцию.  
    
    :::row:::
       :::column span="":::
          ```javascript
          add(25);
          ```  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/console-javascript-example-console-playground.msft.png" alt-text="На консоли" lightbox="../media/console-javascript-example-console-playground.msft.png":::
             **Консоль** отображается после оценки выражений в фрагменте кода.  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
    `add(25)` вычисляется `45` , так как при `add` вызове функции без второго аргумента `b` равным ему присваивается значение по умолчанию `20` .  

## Дальнейшие действия  

<!--See [Run JavaScript][DevToolsConsoleReference] to explore more features related to running JavaScript in the Console.  -->  

<!--todo: add console reference (run javascript) section when available  -->  

DevTools позволяет приостановить выполнение сценария в центре выполнения.  Во время приостановки вы можете использовать **консоль** для просмотра и изменения `window` `DOM` страницы в данный момент времени.  Рабочий процесс обеспечивает мощный процесс отладки.  Для интерактивного учебника перейдите к разделу [Начало работы с отладкой JavaScript][DevToolsJavascriptIndex].  

Кроме того, **консоль** имеет набор удобных функций, которые облегчают взаимодействие с страницей.  Например:  

*   Вместо того `document.querySelector()` чтобы выделять элемент, введите `$()` .  Этот синтаксис имеет тот факт, что jQuery, но он не является jQuery.  Это просто псевдоним `document.querySelector()` .  
*   `debug(function)` фактически задает точку останова в первой строке этой функции.  
*   `keys(object)` Возвращает массив с ключами указанного объекта.  

Дополнительные сведения о специальных возможностях можно найти в [справочнике по API служебных программ для консоли][DevToolsConsoleUtilities].  

## Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsConsoleLoggingMessages]: ./log.md "Начало работы с сообщениями в журнале на консоли | Документы Microsoft"  
[DevToolsConsoleReference]: ./reference.md#run-javascript "Справочник по консоли | Документы Microsoft"  
[DevToolsConsoleUtilities]: ./utilities.md "Справочник по API служебных программ для консоли | Документы Microsoft"  
[DevToolsJavascriptIndex]: ../javascript/index.md "Начало работы с отладкой JavaScript в Microsoft Edge DevTools"  

[2alityExpressionsVersusStatements]: https://2ality.com/2012/09/expressions-vs-statements.html "Выражения и операторы в JavaScript"  

[Esma6DefaultParameterValues]: https://es6-features.org/index#DefaultParameterValues "Значения параметров по умолчанию — обработка расширенных параметров-ECMAScript 6 — новые возможности: Общие сведения о сравнении &"  

[GlitchConsoleJavascriptExample]: https://microsoft-edge-chromium-devtools.glitch.me/static/console/javascript/index.html "Пример кода JavaScript на консоли | Цепь"  

[WikiReadEvalPrintLoop]: https://en.wikipedia.org/wiki/Read–eval–print_loop "Read – eval — цикл печати — Википедии"  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/console/javascript) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
