---
description: Начало работы с CSS
title: 'DevTools для начинающих: Приступая к работе с CSS'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: fe87b4f840c6d9dde3cdf6455700161ea8d8d31e
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993305"
---
<!-- Copyright Katherine Jackson 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->

# DevTools для начинающих: Приступая к работе с CSS  

В этом учебнике вы узнаете, как использовать CSS для стиля веб-страницы.  Кроме того, вы узнаете, как использовать Microsoft Edge DevTools для экспериментов с изменениями CSS.  

В следующей статье приведен второй учебник из серии руководств, в которых рассматриваются основы разработки веб-приложений и Microsoft Edge DevTools.  Вы получаете практический опыт, завершив создание собственного веб-сайта.  Перед вторым учебником вам не нужно выполнять первый из них.  [Настройка кода](#set-up-your-code) показывает, как это сделать.  

> [!NOTE]
> Этот учебник предназначен для абсолютных новичков и специализируется на **основах разработки веб-приложений** и основах использования DevTools для экспериментов с CSS.  Если вам нужен учебник, который фокусируется только на DevTools, ознакомьтесь [со статьей Приступая к просмотру и изменению CSS][DevtoolsCssIndex].  

В начале учебника ваш сайт должен выглядеть так, как показано на следующем рисунке.  

:::image type="complex" source="../media/beginners-css-intro1.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-intro1.msft.png":::
   Как выглядит ваш веб-сайт  
:::image-end:::  

После того как вы закончите обучение, сайт должен выглядеть так, как показано на рисунке ниже.  

:::image type="complex" source="../media/beginners-css-intro2.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-intro2.msft.png":::
   Сведения о том, как должен выглядеть сайт в конце учебника  
:::image-end:::  

## Цели  

Следуйте этим рекомендациям, чтобы лучше разобраться в описанных ниже концепциях и задачах.  

*   Использование CSS для стиля веб-страницы.  
*   Использование Microsoft Edge DevTools для экспериментов с CSS.  
*   Разница между платформами CSS и CSS.  

Вы собираетесь создать реальный веб-сайт.  

## Предварительные условия  

Перед началом работы с учебником заполните следующие предварительные требования.  

*   Закончите [работу с HTML и моделью DOM][DevtoolsBeginnersHtml] или убедитесь в том, что вы знаете HTML и модель DOM, похожую на то, что научились в этом учебнике.  
*   Скачайте веб-браузер [Microsoft Edge][MicrosoftEdgeInsider] .  В следующем учебнике используется набор средств разработки веб-приложений, которые называются Microsoft Edge DevTools, которые встроены в Microsoft Edge.  

## Настройка кода  

Чтобы создать сайт, необходимо выполнить описанные ниже действия, чтобы настроить код.  

> [!NOTE]
> Если вы уже завершили первый учебник в ряду, перейдите к следующему разделу.  Продолжайте использовать код из последнего учебника, Приступая к [работе с HTML и DOM][DevtoolsBeginnersHtml].  

1.  Откройте [Исходный код][GlitchCookedAmphibianIndex].  Ссылка на вкладку "на фокус" в браузере указана как **вкладка "Редактирование"**.  
    
    :::image type="complex" source="../media/beginners-css-setup1.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-setup1.msft.png":::
       Вкладка " **Редактирование** "  
    :::image-end:::  
    
1.  Выберите **готовил-amphibian**.  Всплывающее меню.  
    
    :::image type="complex" source="../media/beginners-css-setup2.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-setup2.msft.png":::
       Меню "Параметры проекта"  
    :::image-end:::  

1.  Выберите **Remix проект**.  Сбой создает копию проекта, которую вы можете редактировать.  
    
    > [!NOTE]
    > Сбой генерирует случайное имя для нового проекта.  
    
1.  Нажмите кнопку **Показать** и выберите **в новом окне**.  Откроется другая вкладка с активным представлением сайта.  На вкладку, которая находится в фокусе браузера, указывается **вкладка Динамический**.  
    
    :::image type="complex" source="../media/beginners-css-setup3.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-setup3.msft.png":::
       **Вкладка "динамический"**  
    :::image-end:::  

## Общие сведения о CSS  

**CSS** — это язык компьютера, который определяет макет и стиль веб-страниц.  На приведенном ниже рисунке показан абзац с границей.  

:::image type="complex" source="../media/beginners-css-red_paragraph.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-red_paragraph.msft.png":::
   Текст был добавлен в таблицу каскадных стилей (CSS)  
:::image-end:::  

Следующий фрагмент кода — это код HTML и CSS, который используется для создания абзаца на предыдущем рисунке.  

```html
<p style="border: 1px dashed red; padding: 5px;">
    This has been styled with CSS.
</p>
```  

`style="border: 1px dashed red; padding: 5px;"` возможно, вам покажется, что у вас новый.  Остальные должны выглядеть знакомым.  Если это не так, сначала приступайте [к работе с HTML и моделью DOM,][DevtoolsBeginnersHtml] прежде чем выполнять следующие разделы.  

## Добавление встроенных стилей  

Выполните указанные ниже действия, чтобы применить стили к одному элементу с помощью **встроенных стилей** .  

1.  Вернитесь на вкладку Правка и откройте окно `index.html` .  
    
    :::image type="complex" source="../media/beginners-css-inline1.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-inline1.msft.png":::
       Открытие `index.html` на вкладке "Редактирование"  
    :::image-end:::  
    
1.  Добавить `style="background-color: aliceblue;"` в `<nav>` .  В блоке кода, приведенном ниже, четвертая строка кода имеет тот же адрес, который нужно изменить.  Остальное – это просто, так что вы можете сделать так, чтобы новый код замещается в нужном расположении.  
    
    ```html
    <header>
        <p>Welcome to my site!</p>
    </header>
    <nav style="background-color: aliceblue;">
        <ul>
            <li><a href="/">Home</a></li>
            ...
        ...
    ...
    ```  
    
1.  Перейдите на **вкладку динамический** , чтобы увидеть изменения.  `<nav>`Теперь фон раздела синего цвета.  
    
    :::image type="complex" source="../media/beginners-css-inline2.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-inline2.msft.png":::
       Цвет фона, который находится за **домашней страницей** и ссылками на **Контакты** , стал синей  
    :::image-end:::  
    
## Повторное использование стилей на одной странице с внутренними таблицами стилей  

В предыдущем фрагменте кода встроенный стиль применяет стиль для одного `<p>` тега.  

```html
<p style="border: 1px dashed red; padding: 5px;">
    This has been styled with CSS.
</p>
```  

Что делать, если вы хотите `<p>` , чтобы все элементы на веб-странице были применены таким же образом?  Код необходимо скопировать и вставить в каждый один `<p>` тег на вашем сайте.  Это немало времени и сил.  Если вы хотите внести изменения, вам придется заново изменить все теги.  Выполните указанные ниже действия, чтобы использовать **внутреннюю таблицу стилей** для создания CSS, чтобы она применялась к нескольким элементам.  

1.  На вкладке "динамический" нажмите " **контакт** ", чтобы перейти на страницу контакта.  Обратите внимание на шрифт **домашних** и **контактных**данных.  
    
    :::image type="complex" source="../media/beginners-css-internal1.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-internal1.msft.png":::
       Страница "контакт"  
    :::image-end:::  
    
1.  На **вкладке "редактор**" перейдите в раздел `contact.html` .  
1.  Добавьте следующий код `contact.html` .  Помните, что вам нужно добавить строки, начинающиеся с `<style>` и заканчивая данными `</style>` .  Другой код — это только то, что вы знаете, где разместить новый код.  
    
    ```html
    ...
        <head>
            ...
            <meta name="viewport" content="width=device-width, initial-scale=1">
            <style>
                li a {
                  font-family: 'Courier New', Courier, Serif;
                }
            </style>
            ...
        </head>
        ...
    ...
    ```  
    
1.  Вернитесь на **вкладку динамический**.  
1.  Нажмите кнопку " **контакт** ", чтобы вернуться на страницу контакта.  Изменился шрифт " **Главная** " и " **контакт** ".  
    
    :::image type="complex" source="../media/beginners-css-internal2.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-internal2.msft.png":::
       Изменен шрифт ссылок на **домашнюю страницу** и **контакт контакта**  
    :::image-end:::  
    
### Общие сведения о внутренних таблицах стилей  

Внутренние таблицы стилей. Примените стили с помощью **селекторов**.  Селекторы — это шаблоны, которые могут применяться к одному или нескольким элементам HTML.  Предыдущий фрагмент кода добавил следующий стиль.  

```html
<style>
    li a {
      font-family: 'Courier New', Courier, Serif;
    }
</style>
```  

`li a` — Это селектор, который преобразуется в "любой `<li>` элемент, содержащий `<a>` элемент".  Браузер изменит шрифт **домашних** и **контактных** ссылок, так как каждая из групп тегов соответствует шаблону.  

```html
<li><a href="/">Home</a></li>
<li><a href="/contact.html">Contact</a></li>
```  

`font-family: 'Courier New', Courier, serif` является **объявлением**.  Объявление состоит из двух частей:  

:::row:::
   :::column span="1":::
      **Property**  
   :::column-end:::
   :::column span="1":::
      `font-family`  
   :::column-end:::
   :::column span="2":::
      Это свойство описывает общий способ изменения стиля элемента.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **value**  
   :::column-end:::
   :::column span="1":::
      `'Courier New', Courier, serif`  
   :::column-end:::
   :::column span="2":::
      Значение точно описывает способ изменения стиля элемента.  
   :::column-end:::
:::row-end:::  

Например, `font-family: 'Courier New', Courier, serif` предоставляет браузеру следующую инструкцию: "Установка шрифта для элементов, которые соответствуют шаблону `li a` `'Courier New'` .  Если этот шрифт недоступен, используйте `Courier` .  Если это недоступно, используйте `serif` ".  

### Добавление нескольких селекторов в набор правил  

Блок кода CSS вроде того, что вы видите ниже, называется набором **правил**.  

```css
li a {
  font-family: 'Courier New', Courier, monospace;
}
```  

Выполните следующие действия, чтобы добавить несколько селекторов в RuleSet с помощью запятых.  

1.  На **вкладке Редактор**откройте `contact.html` .  
1.  После `li a` ввода `, h1` .  
    
    ```html
    <style>
        li a, h1 {
          font-family: 'Courier New', Courier, Serif;
        }
    </style>
    ```  
    
    Предыдущий фрагмент кода указывает браузеру на элементы стиля `<h1>` таким же образом, как и элементы, которые соответствуют шаблону `li a` .  
    
1.  Перейдите на **вкладку динамический**.  
1.  Щелкните ссылку **контакт** , чтобы вернуться на страницу контакта.  Теперь **свяжитесь со мной!** имеет тот же шрифт, что и ссылки для навигации.  
    
    :::image type="complex" source="../media/beginners-css-multiple1.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-multiple1.msft.png":::
       Текстовые **Контакты!** Теперь тот же шрифт, что и ссылки на **домашнюю** и **контактный**  
    :::image-end:::  
    
## Поэкспериментировать с DevTools  

По мере того как вы продолжите свое путешествие, чтобы стать экспертом при разработке веб-приложений, возможно, вы обнаружите, что CSS очень сложны.  Вы можете написать каскадную таблицу стилей, чтобы она отображалась одним способом, но браузер делает что-то совершенно другое.  Microsoft Edge DevTools упрощает эксперименты с изменениями и немедленно показывает, как изменения повлияют на страницу.  

### Добавление объявления к существующему правилу в DevTools  

Выполните указанные ниже действия, чтобы выполнить итерацию по стилю существующего элемента, добавив объявление к существующему набору правил.  

1.  Наведите указатель мыши на **домашнюю** ссылку, откройте контекстное меню, а затем выберите команду **проверить**.  
    
    :::image type="complex" source="../media/beginners-css-add1.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-add1.msft.png":::
       Проверка ссылки на домашнюю страницу  
    :::image-end:::  
    
    DevTools открывается вместе со страницей.  Код, представляющий ссылку на домашнюю страницу, `<a href="/">Home</a>` выделяется синим цветом в дереве DOM.  Фрагмент кода и предварительный просмотр должны быть знакомы с тем, как начать [работу с HTML и моделью DOM][DevtoolsBeginnersHtml].  
    
    :::row:::
       :::column span="":::
          На приведенном ниже рисунке `font-family: 'Courier New', Courier, serif` объявление, добавленное ранее, отображается `contact.html` на вкладке **стили** под деревом DOM.  
          
          :::image type="complex" source="../media/beginners-css-add2.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-add2.msft.png":::
             Вкладка " **стили** " находится под ДЕРЕВОм DOM  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          Если окно DevTools является широкой страницей, вкладка стили находится справа от дерева DOM.  
          
          :::image type="complex" source="../media/beginners-css-add3.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-add3.msft.png":::
             Вкладка " **стили** " справа от дерева DOM  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  Чтобы добавить новое объявление, выберите пустую строку ниже `font-family: 'Courier New', Courier, Serif` .  
    
    :::image type="complex" source="../media/beginners-css-add4.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-add4.msft.png":::
       Добавление нового объявления  
    :::image-end:::  
    
1.  Введите текст `color` и выберите его `Enter` .  Пользовательский интерфейс автозаполнения предлагает параметры по мере ввода.  
    
    :::image type="complex" source="../media/beginners-css-add5.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-add5.msft.png":::
       Тип `color`  
    :::image-end:::  
    
1.  Введите текст `magenta` и выберите его `Enter` .  Весь текст на странице контакта стал пурпурным.  
    
    :::image type="complex" source="../media/beginners-css-add6.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-add6.msft.png":::
       Тип `magenta`  
    :::image-end:::  
    
### Изменение объявления в DevTools  

Чтобы изменить существующие объявления в DevTools, выполните указанные ниже действия.  

1.  Выберите пурпурный квадрат рядом с `magenta` .  Появится палитра выбора цвета.  
    
    :::image type="complex" source="../media/beginners-css-edit1.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-edit1.msft.png":::
       Выбор цвета  
    :::image-end:::  
    
1.  С помощью средства выбора цвета измените текст шрифта на нужный цвет.  
    
    :::image type="complex" source="../media/beginners-css-edit2.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-edit2.msft.png":::
       Изменение цвета шрифта на фиолетовый с помощью средства выбора цвета  
    :::image-end:::  
    
### Добавление нового набора правил в DevTools  

Чтобы добавить новые наборы правил в DevTools, выполните указанные ниже действия.  

1.  Выберите **новое правило стиля** \ ( ![ новое правило стиля ][ImageNewStyleRuleIcon] \), которое находится рядом с **. CLS**.  В качестве Selector появится пустой набор правил `a` .  
    
    :::image type="complex" source="../media/beginners-css-rule1.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-rule1.msft.png":::
       Добавление нового правила  
    :::image-end:::  
    
1.  Заменить `a` на `a:hover` .  
    
    :::image type="complex" source="../media/beginners-css-rule2.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-rule2.msft.png":::
       Заменить `a` на `a:hover`  
    :::image-end:::  
    
    `:hover` является **псевдо-классом**.  Используйте псевдо-классы для элементов стиля, которые могут вводить особые состояния.  Например, `a:hover` стиль вступает в силу только при наведении указателя мыши на `<a>` элемент.  
    
1.  Выберите между скобками, чтобы добавить новое объявление.  
1.  Введите `background-color` имя объявления и нажмите кнопку `Enter` .  
    
    :::image type="complex" source="../media/beginners-css-rule3.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-rule3.msft.png":::
       Тип `background-color`  
    :::image-end:::  
    
1.  Введите `green` значение объявления и нажмите кнопку `Enter` .  
    
    :::image type="complex" source="../media/beginners-css-rule4.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-rule4.msft.png":::
       Тип `green`  
    :::image-end:::  
    
1.  Наведите указатель мыши на ссылку " **Домашняя страница** ".  Фон ссылки становится зеленым.  
    
    :::image type="complex" source="../media/beginners-css-rule5.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-rule5.msft.png":::
       Наведите указатель мыши на домашнюю ссылку, чтобы отобразить зеленый фон  
    :::image-end:::  
    
## Повторное использование стилей на разных страницах с внешними таблицами стилей  

На предыдущем этапе вы добавили следующий фрагмент кода в качестве внутренней таблицы стилей `contact.html` .  

```html
...
    ...
        ...
        <style>
            li a, h1 {
              font-family: 'Courier New', Courier, Serif;
            }
        </style>
        ...
    ...
...
```  

Что делать, если вы захотите стиль `index.html` одинаково?  Что делать, если вы хотите применить стили к большому количеству страниц?  Необходимо скопировать и вставить внутреннюю таблицу стилей в каждую веб-страницу на сайте.  Выполните указанные ниже действия, чтобы добавить **внешнюю таблицу стилей** , которая позволит вам создавать CSS один раз и применять ее к нескольким страницам.  

1.  Сначала перезагрузите вкладку Live, чтобы удалить изменения, внесенные в DevTools.  
    
    :::image type="complex" source="../media/beginners-css-external1.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-external1.msft.png":::
        После обновления страницы изменения, внесенные в DevTools, исчезают  
    :::image-end:::  
    
1.  Вернитесь на **вкладку Редактор** и откройте ее `contact.html` .  
    
    :::image type="complex" source="../media/beginners-css-external2.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-external2.msft.png":::
       contact.html  
    :::image-end:::  
    
1.  Удалить все между `<style>` и `</style>` , включая `<style>` и `</style>` .  
    
    :::image type="complex" source="../media/beginners-css-external3.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-external3.msft.png":::
       Тег Style был удален  
    :::image-end:::  
    
1.  Перейдите к `index.html` тегу и удалите `style="background-color: aliceblue;"` его `<nav>` .  Теперь вы удалили все CSS-таблицы, которые вы ранее добавили на сайт.  
    
    :::image type="complex" source="../media/beginners-css-external4.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-external4.msft.png":::
       Встроенный стиль удален из элемента навигации  
    :::image-end:::  
    
1.  Выберите команду **создать файл**.  
    
    :::image type="complex" source="../media/beginners-css-external5.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-external5.msft.png":::
       Диалоговое окно "Создание файла"  
    :::image-end:::  
    
1.  Замените `cool-file.js` на `style.css` и выберите команду **Добавить файл**.  
    
    :::image type="complex" source="../media/beginners-css-external6.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-external6.msft.png":::
       Тип `style.css`  
    :::image-end:::  
    
1.  Добавьте в файл следующий фрагмент кода `style.css` .  
    
    ```css
    li a, h1 {
      font-family: 'Courier New', Courier, Serif;
    }
    a:hover {
      background-color: green;
    }
    nav {
      background-color: aliceblue;
    }
    ```  
    
    :::image type="complex" source="../media/beginners-css-external7.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-external7.msft.png":::
       Добавление кода в `style.css`  
    :::image-end:::  
    
    Убедитесь, что создана внешняя таблица стилей. Ваш HTML-код не знает, что он существует.  
    
1.  Open (открыть) `index.html` .  
1.  Добавьте `<link rel="stylesheet" href="style.css">` в свой HTML-код.  
    
    ```html
    <head>
        ...
        <meta name="viewport" content="width=device-width, initial-scale=1">
        <link rel="stylesheet" href="style.css">
    </head>
    ```  
    
    :::image type="complex" source="../media/beginners-css-external8.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-external8.msft.png":::
       Ссылка на `style.css`  
    :::image-end:::  
    
1.  Откройте `contact.html` файл и добавьте ссылку на него.  
    
    :::image type="complex" source="../media/beginners-css-external9.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-external9.msft.png":::
       Ссылка `style.css` в `contact.html`  
    :::image-end:::  
    
1.  Перейдите на **вкладку динамический**.  Домашняя страница теперь имеет тот же шрифт, что и в последнем разделе, и в синем разделе навигации.  
    
    :::image type="complex" source="../media/beginners-css-external10.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-external10.msft.png":::
       Домашняя страница  
    :::image-end:::  
    
1.  Щелкните ссылку **контакт** , чтобы перейти на страницу контакта.  Страница контакта имеет тот же формат, что и домашняя страница.  
    
    :::image type="complex" source="../media/beginners-css-external11.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-external11.msft.png":::
       Страница "контакт"  
    :::image-end:::  
    
## Использование платформы CSS  

**Платформы CSS** — это коллекции стилей, разработанных другими разработчиками, которые упрощают создание привлекательных веб-сайтов.  Вместо того чтобы определять стили самостоятельно, платформа предоставляет коллекцию стилей, которые вы можете использовать в элементах страницы.  

1.  Скопируйте приведенный ниже код.  
    
    ```html
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.1/css/bootstrap.min.css">
    ```  
    
1.  Перейдите на вкладку Правка и вставьте код в `contact.html` .  
    
    :::image type="complex" source="../media/beginners-css-framework1.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-framework1.msft.png":::
       Ссылка на платформу в `contact.html`  
    :::image-end:::  
    
1.  Откройте `index.html` файл и добавьте в него код.  
    
    :::image type="complex" source="../media/beginners-css-framework2.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-framework2.msft.png":::
       Ссылка на платформу в `index.html`  
    :::image-end:::  
    
1.  Вернитесь на вкладку динамический, чтобы просмотреть изменения.  Несмотря на то, что цвет фона `<nav>` элемента и шрифта `<li>` `<a>` элементов and одинаков, изменился шрифт остальных элементов.  
    
    :::image type="complex" source="../media/beginners-css-framework3.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-framework3.msft.png":::
       Некоторые шрифты на домашней странице изменились из-за платформы  
    :::image-end:::  
    
### Использование класса  

В последнем разделе вы добавили начальную загрузку на веб-страницы, которая изменила шрифты для некоторых элементов на вашем сайте.  Структуры CSS помогают вносить существенные изменения на странице с помощью очень небольшого количества кода.  Чтобы изменить верхний колонтитул, выполните указанные ниже действия.  

1.  Скопируйте следующий фрагмент кода.  
    
    ```html
    class="jumbotron jumbotron-fluid"  
    ```  
    
1.  Добавьте предыдущий фрагмент кода в `<header>` тег `index.html` .  
    
    :::image type="complex" source="../media/beginners-css-jumbotron1.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-jumbotron1.msft.png":::
       Добавление классов в `index.html`  
    :::image-end:::  
    
1.  Добавьте код в `<header>` тег `contact.html` .  
    
    :::image type="complex" source="../media/beginners-css-jumbotron2.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-jumbotron2.msft.png":::
       Добавление классов в `contact.html`  
    :::image-end:::  
    
1.  Просмотрите изменения на вкладке "живые".  Вокруг заголовка есть большое затененное поле.  
    
    :::image type="complex" source="../media/beginners-css-jumbotron3.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-jumbotron3.msft.png":::
       Теперь верхний колонтитул имеет большой серый прямоугольник вокруг него.  
    :::image-end:::  
    
### Общие сведения о классах  

Классы позволяют назначать коллекции стилей произвольным элементам.  Используйте следующий фрагмент кода, чтобы применить к `<header>` элементу несколько стилей после присвоения `class` атрибуту значения `jumbotron` .  

```css
.jumbotron {
  padding: 2rem 1rem;
  margin-bottom: 2rem;
  background-color: #e9ecef;
  border-radius: .3rem;
}
```  

Одно из преимуществ класса состоит в том, что он позволяет применять стили к любым нужным элементам.  Например, предположим, что вам нужно установить для некоторых элементов цвет фона `<p>` , который будет фиолетовым, но не все `<p>` элементы.  Используйте следующий фрагмент кода, чтобы определить стиль в классе.  

```css
.custom-background {
  background-color: purple;
}
```  

Затем примените класс только к тем `<p>` элементам, для которых вы хотите применить стиль.  

```html
<p>The text is not purple.</p>
<p class="custom-background">The text is purple.</p>
<p>The text is not purple.</p>
<p class="custom-background">The text is purple.</p>
```  

### Выравнивание элементов  

Выполните указанные ниже действия, чтобы выполнить загрузку и предоставить классы для выравнивания элементов.  

1.  Вернитесь на вкладку Редактор и откройте ее `index.html` .  
1.  Добавьте `class="container-fluid"` в свой `<body>` тег.  
    
    :::image type="complex" source="../media/beginners-css-align1.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-align1.msft.png":::
       Добавьте `container-fluid` класс  
    :::image-end:::  
    
1.  Обтекание `<nav>` `<main>` элементов `<div class="row">` .  `</div>`Чтобы правильно закрыть новый тег, убедитесь в том, что вы хотите сделать `</main>` это.  
    
    :::image type="complex" source="../media/beginners-css-align2.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-align2.msft.png":::
       Добавление строки  
    :::image-end:::  
    
1.  Добавьте `class="col-3"` теги в тег `<nav>` и `class="col-9"` в `<main>` тег.  
    
    :::image type="complex" source="../media/beginners-css-align3.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-align3.msft.png":::
       Добавление `col-3` классов и `col-9`  
    :::image-end:::  
    
1.  Просмотрите изменения на вкладке "живые".  
    
    :::image type="complex" source="../media/beginners-css-align4.msft.png" alt-text="Как выглядит ваш веб-сайт" lightbox="../media/beginners-css-align4.msft.png":::
       Содержимое элемента навигации теперь находится слева от основного содержимого.  
    :::image-end:::  
    
## Дальнейшие действия  

Поздравляем, вы закончите.  

*   Лучший способ улучшить качество веб-приложений — создать дополнительные сайты.  Не беспокойтесь о нарушениях.  Просто восприятие и обучение очень удобно.  
*   Чтобы узнать больше о стилях веб-страниц, ознакомьтесь со статьей общие сведения о [CSS][MDNCssFirstSteps].  
*   Дополнительные сведения о том, как использовать DevTools для экспериментов с CSS-страницей, можно найти в статье Начало [работы с помощью просмотра и изменения CSS][DevtoolsCssIndex].  

<!--- image links --->  

[ImageNewStyleRuleIcon]: ../media/new-style-rule-icon.msft.png  

<!--- links  --->  

[DevtoolsBeginnersHtml]: ./html.md "DevTools для начинающих: Приступая к работе с HTML и моделью DOM | Документы Microsoft"  
[DevtoolsCssIndex]: ../css/index.md "Начало просмотра и изменения CSS | Документы Microsoft"  

[MicrosoftEdgeInsider]: https://www.microsoftedgeinsider.com "Предварительная оценка Microsoft Edge"  

[GlitchCookedAmphibianIndex]: https://glitch.com/edit/#!/cooked-amphibian?path=index.html "index.html-готовил-amphibian | Цепь"  

[MDNCssFirstSteps]: https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS "Первые шаги CSS | MDN"  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/beginners/css) и [Katherine Джексон][KatherineJackson] \ (помощник службы технической поддержки, Chrome DevTools \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[KatherineJackson]: https://developers.google.com/web/resources/contributors/katjackson  
