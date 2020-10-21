---
description: Узнайте о том, как в Microsoft Edge DevTools вы можете приостановить выполнение кода.
title: Приостановка кода с точки останова в Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 98c0e42657d9b0900d3eaca8af69f1c17abfcf06
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "11124812"
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

# Приостановка кода с точки останова в Microsoft Edge DevTools  

Используйте точки останова для приостановки кода JavaScript.  В этом руководстве описаны все типы точек останова, доступные в DevTools, а также способы их использования и настройки каждого типа.  Для получения практических учебников, посвященных отладке, перейдите к [разделу Начало отладки JavaScript в Microsoft Edge DevTools][DevtoolsJavascriptIndex].  

## Общие сведения о том, когда использовать каждый тип точки останова  

Наиболее известный тип точки останова — это строка кода.  Однако точки останова для кода могут быть неэффективными для установки, особенно в том случае, если вы точно не знаете, где искать, или если вы работаете с большой базой кода.  Вы можете экономить время при отладке, зная, как и когда использовать другие типы точек останова.  

| Тип точки останова | Используйте этот параметр, если вы хотите приостановить...  |  
|:--- |:--- |  
| [Строка кода](#line-of-code-breakpoints) | В определенном регионе кода.  |  
| [Условный текст](#conditional-line-of-code-breakpoints) | В определенном регионе кода, но только в том случае, если истинно какое – либо другое условие.  |  
| [DOM](#dom-change-breakpoints) | В коде, который изменяет или удаляет определенный узел DOM или дочерние элементы.  |  
| [XHR](#xhrfetch-breakpoints) | Если URL-адрес XHR имеет строковый шаблон.  |  
| [Прослушиватель событий](#event-listener-breakpoints) | В коде, который выполняется после события, например `click` , выполняется.  |  
| [Ошибка](#exception-breakpoints) | В строке кода, которая вызывает перехваченное или неперехваченное исключение.  |  
| [Функция](#function-breakpoints) | Каждый раз, когда выполняется определенная команда, функция или метод.  |  

## Точки останова в коде строки  

Если вы знаете точную область кода, которую нужно исследовать, используйте точку останова из строки кода.  DevTools всегда задерживается перед выполнением этой строки кода.  

Установка точки останова в коде строки в DevTools:  

1.  Откройте вкладку **источники** .  
1.  Откройте файл с той строкой, в которой вы хотите прервать ее.  
1.  Перейдите к строке кода.  
1.  Слева от строки кода находится столбец номер строки.  Щелкните по нему.  Рядом со столбцом номер строки появится красный значок.  
    
    :::image type="complex" source="../media/javascript-sources-page-js-breakpoint-30.msft.png" alt-text="Точка останова строки кода" lightbox="../media/javascript-sources-page-js-breakpoint-30.msft.png":::
       Точка останова строки кода  
    :::image-end:::  
    
### Точки останова в коде для строк кода  

Выполняйте `debugger` метод из вашего кода, чтобы приостановить его на этой линии.  Это эквивалентно [точке останова строки кода](#line-of-code-breakpoints), за исключением того, что точка останова задается в коде, а не в пользовательском интерфейсе DevTools.  

```javascript
console.log('a');
console.log('b');
debugger;
console.log('c');
```  

### Зависимые точки останова для строк кода  

Если вы знаете точную область кода, которую нужно исследовать, но вы хотите приостанавливать только в том случае, если какое-либо другое условие имеет значение true, используйте для нее точку останова в условном коде.  

Установка условной точки останова для строки кода:  

1.  Откройте вкладку **источники** .  
1.  Откройте файл с той строкой, в которой вы хотите прервать ее.  
1.  Перейдите к строке кода.  
1.  Слева от строки кода находится столбец номер строки.  Щелкните правой кнопкой мыши номер строки.  
1.  Нажмите кнопку **добавить условную точку останова**.  Под строкой кода появится диалоговое окно.  
1.  Введите условие в диалоговом окне.  
1.  Выберите `Enter` , чтобы активировать точку останова.  Значок рядом со столбцом "номер строки".  
    
    :::image type="complex" source="../media/javascript-sources-page-js-conditional-breakpoint.msft.png" alt-text="Точка останова строки кода" lightbox="../media/javascript-sources-page-js-conditional-breakpoint.msft.png":::
       Условная точка останова для строки кода  
    :::image-end:::  
    
### Управление точками останова для строк кода  

С помощью области " **точки останова** " можно отключить или удалить точки останова для строк кода из одного места.  

:::image type="complex" source="../media/javascript-sources-page-js-breakpoints-16-33.msft.png" alt-text="Точка останова строки кода" lightbox="../media/javascript-sources-page-js-breakpoints-16-33.msft.png":::
   Панель « **точки останова** »  
:::image-end:::  

*   Установите флажок рядом с записью, чтобы отключить эту точку останова.  
*   Щелкните правой кнопкой мыши запись для удаления точки останова.  
*   Щелкните правой кнопкой мыши в любом месте области **точки останова** , чтобы отключить все точки останова, отключить все точки останова или удалить все точки останова.  Отключение всех точек останова эквивалентно депроверке каждого из них.  Отключение всех точек останова дает указание DevTools игнорировать все точки останова для строк кода, а также поддерживать состояние включения, чтобы каждый из них нав одном и том же состоянии до повторной активации каждой из них.  
    
    :::image type="complex" source="../media/javascript-sources-page-js-breakpoints-deactivate-breakpoints.msft.png" alt-text="Точка останова строки кода" lightbox="../media/javascript-sources-page-js-breakpoints-deactivate-breakpoints.msft.png":::
       Деактивированные точки останова на панели " **точки останова** "  
    :::image-end:::  
    
## Точки останова по изменению модели DOM  

Чтобы приостановить выполнение кода, который изменяет узел DOM или дочерние элементы, используйте точку останова изменения модели DOM.  

Настройка точки останова для изменения модели DOM.  

1.  Откройте вкладку **элементы** .  
1.  Перейдите к элементу, для которого вы хотите установить точку останова.  
1.  Щелкните элемент правой кнопкой мыши.  
1.  Наведите указатель мыши **на пункт разрыв**, а затем выберите **изменения поддерева**, **изменения атрибутов**или **Удаление узла**.  
    
    :::image type="complex" source="../media/javascript-elements-break-on-subtree-modifications.msft.png" alt-text="Точка останова строки кода" lightbox="../media/javascript-elements-break-on-subtree-modifications.msft.png":::
       Контекстное меню для создания точки останова по изменению модели DOM  
    :::image-end:::  
    
### Типы точек останова для изменения модели DOM  

*   **Изменения поддерева**.  Вызывается при удалении или добавлении дочернего узла, выбранного в данный момент, или изменении содержимого дочернего элемента.  Не инициируется для изменений атрибутов дочернего узла или при любых изменениях в выбранном в данный момент узле.  
*   **Изменения атрибутов**: активируется при добавлении или удалении атрибута на текущем выбранном узле или изменении значения атрибута.  
*   **Удаление узла**: активируется при удалении текущего выбранного узла.  
    
## Точки останова XHR и FETCH  

Используйте точку останова XHR, когда нужно прервать, когда URL-адрес запроса XHR содержат указанную строку.  DevTools приостанавливается на строке кода, где XHR запускает `send()` метод.  

> [!NOTE]
> Эта функция также работает для запросов [API FETCH][MDNFetchApi] .  

Это может быть полезно, если вы видите, что ваша страница запрашивает неверный URL-адрес, и вам нужно быстро найти исходный код AJAX или FETCH, вызывающий неверный запрос.  

Чтобы установить точку останова XHR, выполните указанные ниже действия.  

1.  Откройте вкладку **источники** .  
1.  Разверните область **точки останова XHR** .  
1.  Нажмите кнопку **Добавить точку останова**.  
1.  Введите строку, на которой вы хотите приостановить.  DevTools приостанавливает работу, когда эта строка отображается в любом месте URL-адреса запроса XHR.  
1.  Выберите `Enter` для подтверждения.  
    
    :::image type="complex" source="../media/javascript-sources-page-js-xhr-fetch-breakpoints-org.msft.png" alt-text="Точка останова строки кода" lightbox="../media/javascript-sources-page-js-xhr-fetch-breakpoints-org.msft.png":::
       Создание точки останова XHR  
    :::image-end:::  
    
## Точки останова прослушивателя событий   

Используйте точки останова прослушивателя событий, когда необходимо приостановить выполнение кода прослушивателя событий, который выполняется после срабатывания события.  Вы можете выбрать определенные события, такие как `click` или категории событий, например все события мыши.  

1.  Откройте вкладку **источники** .  
1.  Разверните область **точки останова для прослушивателя событий** .  DevTools отображает список категорий событий, например **анимацию**.  
1.  Отметьте одну из этих категорий, чтобы приостановить любое событие из этой категории, или развернуть категорию и проверить определенное событие.  
    
    :::image type="complex" source="../media/javascript-sources-page-js-event-listener-breakpoints-device-deviceorientation.msft.png" alt-text="Точка останова строки кода" lightbox="../media/javascript-sources-page-js-event-listener-breakpoints-device-deviceorientation.msft.png":::
       Создание точки останова для прослушивателя событий  
    :::image-end:::  
    
## Точки останова для исключений  

Используйте точки останова, когда нужно приостановить выполнение в строке кода, которая вызывает перехваченное или неперехваченное исключение.  

1.  Откройте вкладку **источники** .  
1.  Выберите **Pause on Exceptions** \ ( ![ Pause on Exceptions ][ImagePauseOnExceptionsIcon] \).  При включении значок становится синей.  
    
    :::image type="complex" source="../media/javascript-sources-page-js-pause-on-exceptions.msft.png" alt-text="Точка останова строки кода" lightbox="../media/javascript-sources-page-js-pause-on-exceptions.msft.png":::
       Кнопка " **Пауза при исключениях** "  
    :::image-end:::  
    
1.  **Необязательный**.  Установите флажок **приостановить на перехваченных исключениях** , если вы также хотите приостанавливать на перехваченных исключениях помимо неперехваченных.  
    
    :::image type="complex" source="../media/javascript-sources-page-js-paused-on-exception.msft.png" alt-text="Точка останова строки кода" lightbox="../media/javascript-sources-page-js-paused-on-exception.msft.png":::
       Приостановлено при неперехваченном исключении  
    :::image-end:::  
    
## Точки останова по функциям  

Выполняйте `debug(method)` метод, где `method` — команда, функция или метод, для которого нужно выполнить отладку, когда вы хотите приостановить каждый раз при запуске определенной функции.  Вы можете вставить `debug()` в код (например, `console.log()` инструкцию) или запустить метод из консоли DevTools.  `debug()` эквивалентно установке [точки останова строки кода](#line-of-code-breakpoints) в первой строке функции.  

```javascript
function sum(a, b) {
    let result = a + b; // DevTools pauses on this line.
    return result;
}
debug(sum); // Pass the function object, not a string.
sum();
```  

### Проверка того, что Целевая функция находится в области  

DevTools создает исключение, `ReferenceError` Если функция, которую вы хотите отладить, не находится в области действия.  

```javascript
(function () {
    function hey() {
        console.log('hey');
    }
    function yo() {
        console.log('yo');
    }
    debug(yo); // This works.
    yo();
})();
debug(hey); // This does not work.  hey() is out of scope.
```  

Убедитесь в том, что Целевая функция находится в области действия, если вы запускаете `debug()` метод из консоли DevTools.  Ниже описана одна из стратегий.  

1.  Установите [точку останова для строки кода](#line-of-code-breakpoints) , где находится функция в области.
1.  Активация точки останова.  
1.  Выполняйте `debug()` метод на консоли DevTools, когда код по-прежнему придерживается в точке останова кода.  
    
## Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImagePauseOnExceptionsIcon]: ../media/pause-on-exceptions-icon.msft.png  

<!-- links -->  

[DevtoolsJavascriptIndex]: index.md "Начало работы с отладкой JavaScript в Microsoft Edge DevTools | Документы Microsoft"  

[MDNFetchApi]: https://developer.mozilla.org/docs/Web/API/Fetch_API "Получить API | MDN"  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/javascript/breakpoints) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
