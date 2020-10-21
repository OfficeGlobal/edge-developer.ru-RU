---
description: Начало работы с HTML и моделью DOM
title: 'DevTools для начинающих: Приступая к работе с HTML и моделью DOM'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: f17b68845ef746fa2612cdf4d02cc7e1003baabb
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125302"
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

# DevTools для начинающих: Приступая к работе с HTML и моделью DOM  

Это первый из ряда учебников, в котором изучаются основы разработки веб-приложений.  Кроме того, вы узнаете о наборе средств для веб-разработчиков, именуемых Microsoft Edge DevTools, которые могут повысить производительность.  

В этом конкретном учебнике вы узнаете о HTML и модели DOM.  HTML — это одна из основных методик разработки веб-приложений.  Это язык, управляющий структурой и содержимым веб-страниц.  Модель DOM также связана со структурой и контентом веб-страниц, но вы узнаете об этом позже.  

## Цели  

Вы собираетесь познакомиться с веб-разработкой, завершив создание собственного веб-сайта.  По мере того, как вы закончите все учебные курсы в серии *DevTools для начинающих* , ваш готовый сайт будет выглядеть так, как показано на следующем рисунке.  

:::image type="complex" source="../media/beginners-html-finished.msft.png" alt-text="Готовый сайт" lightbox="../media/beginners-html-finished.msft.png":::
   Готовый сайт  
:::image-end:::  

В конце этого учебника вы узнаете:  

*   Как HTML и DOM создают содержимое, которое отображается на веб-страницах.  
*   Как Microsoft Edge DevTools помогает экспериментировать с изменениями HTML и DOM.  
*   Разница между HTML и DOM.  

У тебя также есть реальный веб-сайт!  Вы можете использовать этот сайт для размещения резюме или блога.  

## Предварительные условия  

Прежде чем приступить к работе с учебником, выполните следующие требования:  

*   Если вы не знакомы с форматом HTML, ознакомьтесь с разделом начало [работы с HTML][MDNGettingStartedHtml].  
*   Скачайте веб-браузер [Microsoft Edge][MicrosoftEdgeInsider] .  В этом учебнике используется набор средств разработки веб-приложений, которые называются Microsoft Edge DevTools, которые встроены в Microsoft Edge.  

## Настройка кода  

Вы собираетесь создать сайт в редакторе кода на веб-сайте с именем "сбой".  

1.  Откройте [Исходный код][GlitchAlluringShockIndex].  Эта вкладка будет называться **вкладкой "редактор"** в рамках этого учебника.  
    
    :::image type="complex" source="../media/beginners-html-setup1.msft.png" alt-text="Готовый сайт" lightbox="../media/beginners-html-setup1.msft.png":::
       Вкладка "редактор"  
    :::image-end:::  
    
1.  Выберите **alluring-удар**.  В левом верхнем углу откроется меню "Параметры проекта".  
    
    :::image type="complex" source="../media/beginners-html-setup2.msft.png" alt-text="Готовый сайт" lightbox="../media/beginners-html-setup2.msft.png":::
       Меню "Параметры проекта"  
    :::image-end:::  
    
1.  Выберите **Remix проект**.  При возникновении недостаточной версии создается копия проекта, которую можно редактировать и случайным образом создает новое имя для проекта.  Содержимое будет таким же, как и раньше.  
    
    :::image type="complex" source="../media/beginners-html-setup3.msft.png" alt-text="Готовый сайт" lightbox="../media/beginners-html-setup3.msft.png":::
       Смешанный проект  
    :::image-end:::  
    
1.  Если вы планируете завершить работу следующего учебника в этой серии, выберите **Вход** и войдите в систему с помощью учетной записи GitHub или Facebook.  Если вы не входите в свою учетную запись, то после закрытия вкладки Правка вы потеряли возможность изменить этот проект.  
1.  Нажмите кнопку **Показать** и выберите **в новом окне**.  Откроется новая вкладка, на которой отображается активная страница.  Эта вкладка будет называться на **вкладке динамический** в рамках этого учебника.  
    
    :::image type="complex" source="../media/beginners-html-setup4.msft.png" alt-text="Готовый сайт" lightbox="../media/beginners-html-setup4.msft.png":::
       Вкладка "динамический"  
    :::image-end:::  
    
## Добавление содержимого  

Ваш сайт совершенно пуст.  Чтобы добавить содержимое, выполните указанные ниже действия.  

1.  На **вкладке "редактор"** замените `<!-- You're "About Me" will go here.  -->` на `<h1>About Me</h1>` .  
    
    :::row:::
       :::column span="":::
          ```html
          ...
              ...
              <body>
                  <p> Your site!</p>
                  <main>
                      <h1>About Me</h1>
                  </main>
                  ...
              ...
          ...
          ```  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/beginners-html-add1.msft.png" alt-text="Готовый сайт" lightbox="../media/beginners-html-add1.msft.png":::
             На вкладке "редактор" выделена новая программа  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
1.  Просмотрите изменения на **вкладке "живые"**.  Текст `About Me` будет отображаться на странице.  Он больше, чем оставшаяся часть текста, так как `<h1>` элемент представляет заголовок раздела.  В веб-браузере стили заголовков автоматически заменяются на более крупные размеры шрифта.  
    
    :::image type="complex" source="../media/beginners-html-add2.msft.png" alt-text="Готовый сайт" lightbox="../media/beginners-html-add2.msft.png":::
       Новый заголовок отображается на вкладке "живые"  
    :::image-end:::  
    
1.  Вернувшись на **вкладку Редактор**, вставьте `<p>I am learning HTML.  Recent accomplishments:</p>` строку под тем местом, где они просто размещены `<h1>About Me</h1>` .  
    
    :::row:::
       :::column span="":::
          ```html
          ...
              ...
              <body>
                  <p> Your site!</p>
                  <main>
                      <h1>About Me</h1>
                      <p>I am learning web development.  Recent accomplishments:</p>
                  </main>
                  ...
              ...
          ...
          ```  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/beginners-html-add3.msft.png" alt-text="Готовый сайт" lightbox="../media/beginners-html-add3.msft.png":::
             Обновленный код выделен на вкладке "редактор"  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
1.  Просмотрите изменения на **вкладке "живые"**.  
1.  Вернитесь на **вкладку Редактор**и добавьте список ваших достижений.  
    
    :::row:::
       :::column span="":::
          ```html
          ...
              ...
                  ...
                  <p>I am learning web development.  Recent accomplishments:</p>
                  <ul>
                      <li>Learned how to set up my code in Glitch.</li>
                      <li>Added content to my HTML.</li>
                      <li>TODO: Learn how to use Microsoft Edge DevTools to experiment with content changes.</li>
                      <li>TODO: Learn the difference between HTML and the DOM.</li>
                  </ul>
                  ...
              ...
          ...
          ```  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/beginners-html-add4.msft.png" alt-text="Готовый сайт" lightbox="../media/beginners-html-add4.msft.png":::
             Обновленный код также выделена на вкладке "редактор"  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  Опять же, вернитесь на **вкладку динамический** , чтобы убедиться, что новое содержимое отображается правильно.  
    
    :::image type="complex" source="../media/beginners-html-add5.msft.png" alt-text="Готовый сайт" lightbox="../media/beginners-html-add5.msft.png":::
       Новый список отображается на вкладке "живые"  
    :::image-end:::  
    
## Поэкспериментировать с изменениями содержимого в Microsoft Edge DevTools  

Если вы разрабатываете большую страницу с большим количеством HTML-файлов, вы можете представить, что она может быть довольно утомительной, чтобы просматривать изменения, особенно если вы не уверены, что нужно сделать, чтобы они были размещены на странице.  Microsoft Edge DevTools поможет вам поэкспериментировать с изменениями содержимого, не выходя из вкладки Live.  

### Сведения о различиях между HTML и DOM  

Перед тем как приступить к редактированию содержимого в Microsoft Edge DevTools, полезно понять разницу между HTML и DOM.  Лучший способ освоить это можно, например:  

1.  Перейдите на **вкладку динамический**.  В нижней части страницы отображается текст `A new element!?!` .  
    
    :::image type="complex" source="../media/beginners-html-dom1.msft.png" alt-text="Готовый сайт" lightbox="../media/beginners-html-dom1.msft.png":::
       В нижней части страницы текст — это новый элемент!?! может отображаться  
    :::image-end:::  
    
1.  Вернитесь на **вкладку Редактор** и попробуйте найти этот текст в `index.html` .  Это не так!  
    
    :::image type="complex" source="../media/beginners-html-dom2.msft.png" alt-text="Готовый сайт" lightbox="../media/beginners-html-dom2.msft.png":::
       Текст загадкы `A new element!?!` не удается найти в `index.html`  
    :::image-end:::  
    
1.  Вернитесь на **вкладку динамический**, щелкните правой кнопкой мыши `A new element!?!` и выберите команду **проверить**.  
    
    :::image type="complex" source="../media/beginners-html-dom3.msft.png" alt-text="Готовый сайт" lightbox="../media/beginners-html-dom3.msft.png":::
       Проверка текста  
    :::image-end:::  
    
    DevTools открывается вместе со страницей.  `<div>A new element!?!</div>` выделяется синим цветом.  Несмотря на то, что структура в DevTools выглядит так же, как и у вашего HTML-кода, она действительно является **деревом DOM**.  
    
    :::image type="complex" source="../media/beginners-html-dom4.msft.png" alt-text="Готовый сайт" lightbox="../media/beginners-html-dom4.msft.png":::
       DevTools открывается вместе со страницей  
    :::image-end:::  
    
При загрузке страницы браузер использует HTML для создания *начального* содержимого страницы.  Модель DOM представляет *Текущее* содержимое страницы, которое может изменяться с течением времени.  Содержимое Mysterious `<div>A new element!?!</div>` будет добавлено на страницу из `<script src="new.js"></script>` -за тега в нижней части HTML.  Этот тег вызывает выполнение кода JavaScript.  Более подробно о JavaScript можно узнать в более подробном учебнике, но теперь его можно рассматривать как язык программирования, который может изменить содержимое страницы.  В этом конкретном случае код JavaScript добавляется `<div>A new element!?!</div>` на страницу.  Причина в том, что этот загадкный текст отображается на живой странице, но не в HTML.  

### Редактирование модели DOM  

Если вы хотите быстро поэкспериментировать с изменениями содержимого, не выходя из вкладки Live, попробуйте DevTools.  

1.  В DevTools щелкните правой кнопкой мыши `Your site!` и выберите команду **изменить в виде HTML**.  
    
    :::image type="complex" source="../media/beginners-html-edit1.msft.png" alt-text="Готовый сайт" lightbox="../media/beginners-html-edit1.msft.png":::
       Редактирование узла в формате HTML  
    :::image-end:::  
    
1.  Замените `<p>Your site!</p>` на код ниже.  
    
    :::row:::
       :::column span="":::
          ```html
          ...
              ...
                  ...
                  <header>
                      <p><b>Welcome to my site!</b></p>
                      <button>Download my resume</button>
                  </header>
                  ...
              ...
          ...
          ```  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/beginners-html-edit2.msft.png" alt-text="Готовый сайт" lightbox="../media/beginners-html-edit2.msft.png":::
             Обновление узла в формате HTML  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  Выберите `Control` + `Enter` \ (Windows, Linux \) или `Command` + `Enter` \ (macOS \), чтобы сохранить изменения, или щелкните любое место за пределами поля.  Изменения автоматически отображаются в режиме реального времени на странице.  Текст `Your site!` заменен новым содержимым.  
    
    :::image type="complex" source="../media/beginners-html-edit3.msft.png" alt-text="Готовый сайт" lightbox="../media/beginners-html-edit3.msft.png":::
       Новое содержимое немедленно появляется на странице  
    :::image-end:::  
    
Этот рабочий процесс хорошо подходит только для экспериментов с изменениями контента.  Если вы перезагрузите страницу или закроете ее, ваши изменения будут потеряны.  Если вы используете этот рабочий процесс и хотите сохранить изменения, вам потребуется вручную скопировать эти изменения на HTML-код.  В следующей паре разделов показаны другие способы изменения контента из дерева DOM.  

## Изменение порядка узлов  

Вы также можете изменить порядок узлов DOM.  Например, на веб-странице в нижней части окна находится меню навигации.  Чтобы переместить элемент в начало страницы, выполните указанные ниже действия.  

1.  Найдите `<nav>` узел в **дереве DOM** DevTools.  
    
    :::image type="complex" source="../media/beginners-html-reorder1.msft.png" alt-text="Готовый сайт" lightbox="../media/beginners-html-reorder1.msft.png":::
       Узел навигации выделяется синим цветом в DevTools  
    :::image-end:::  
    
1.  Перетащите `<nav>` узел в верхнюю части экрана, чтобы он был первым дочерним `<body>` узлом узла.  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/beginners-html-reorder2.msft.png" alt-text="Готовый сайт" lightbox="../media/beginners-html-reorder2.msft.png":::
             Перетаскивание узла навигации в начало  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          `<nav>`Теперь узел отображается в верхней части страницы.  
          
          :::image type="complex" source="../media/beginners-html-reorder3.msft.png" alt-text="Готовый сайт" lightbox="../media/beginners-html-reorder3.msft.png":::
             Узел навигации находится в верхней части страницы  
          :::image-end:::  
       :::column-end:::
   :::row-end:::  
    
### Удаление узла  

Вы также можете удалить узлы из дерева DOM.  

1.  В **дереве DOM**щелкните `<div>A new element!?!</div>` .  DevTools выделяет узел синим цветом.  
    
    :::image type="complex" source="../media/beginners-html-delete1.msft.png" alt-text="Готовый сайт" lightbox="../media/beginners-html-delete1.msft.png":::
       Выбор узла для удаления  
    :::image-end:::  
    
1.  Нажмите клавишу `Delete` на клавиатуре.  `<div>A new element!?!</div>`Узел удаляется из дерева DOM.  
    
    :::image type="complex" source="../media/beginners-html-delete2.msft.png" alt-text="Готовый сайт" lightbox="../media/beginners-html-delete2.msft.png":::
       Узел удален  
    :::image-end:::  
    
## Копирование изменений  

Почти все готово.  Вы внесли несколько изменений на странице в DevTools, но они еще не сохранились в исходном коде.  

1.  Обновите **вкладку Live**.  Изменения, внесенные в дереве DOM, исчезнут.  В частности, текст `Your site!` возвращается в верхней части страницы, а текст `A new element!?!` возвращается в нижнюю часть.  
    
    :::image type="complex" source="../media/beginners-html-copy1.msft.png" alt-text="Готовый сайт" lightbox="../media/beginners-html-copy1.msft.png":::
       Внесенные вами изменения исчезли  
    :::image-end:::  
    
1.  Скопируйте приведенный ниже код.  
    
    ```html
    <!DOCTYPE html>
    <html lang="en">
        <head>
            <meta charset="utf-8">
            <meta http-equiv="X-UA-Compatible" content="IE=edge">
            <meta name="viewport" content="width=device-width, initial-scale=1">
        </head>
        <body>
            <header>
                <p>Welcome to my site!</p>
            </header>
            <nav>
                <ul>
                    <li><a href="/">Home</a></li>
                    <li><a href="/contact.html">Contact</a></li>
                </ul>
            </nav>
            <main>
                <h1>About Me</h1>
                <p>I am learning web development.  Recent accomplishments:</p>
                <ul>
                    <li>Learned how to set up my code in Glitch.</li>
                    <li>Added content to my HTML.</li>
                    <li>Learned how to use Microsoft Edge DevTools to experiment with content changes.</li>
                    <li>Learned the difference between HTML and the DOM.</li>
                </ul>
            </main>
        </body>
    </html>
    ```  
    
1.  Вернитесь на **вкладку Редактор** и замените содержимое `index.html` файла кодом, который вы только что скопировали.  
    
    :::image type="complex" source="../media/beginners-html-copy2.msft.png" alt-text="Готовый сайт" lightbox="../media/beginners-html-copy2.msft.png":::
       Как `index.html` должен выглядеть файл  
    :::image-end:::  
    
## Дальнейшие действия  

*   Чтобы узнать, как изменить стиль страницы и поэкспериментировать с изменениями стиля в Microsoft Edge DevTools, выполните следующие шаги в этой серии. Приступая к [работе с CSS][DevToolsBeginnersCss].  
*   Ознакомьтесь [с введением в DOM][MDNIntroductionDom] , чтобы узнать больше об DOM.  
*   Ознакомьтесь с курсом, например [Знакомство с веб-разработкой][CourseraIntroductionToWebDevelopment] , чтобы получить больше возможностей для веб-разработки.  

## Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!--- links --->  

[DevToolsBeginnersCss]: ./css.md "DevTools для начинающих: Приступая к работе с CSS | Документы Microsoft"  

[MicrosoftEdgeInsider]: https://www.microsoftedgeinsider.com "Предварительная оценка Microsoft Edge"  

[CourseraIntroductionToWebDevelopment]: https://www.coursera.org/learn/web-development "Общие сведения о веб-разработке | Coursera"  

[GlitchAlluringShockIndex]: https://glitch.com/edit/#!/alluring-shock?path=index.html "index.html-alluring-удар | Цепь"  

[MDNGettingStartedHtml]: https://developer.mozilla.org/docs/Learn/HTML/Introduction_to_HTML/Getting_started "Начало работы с HTML | MDN"  
[MDNIntroductionDom]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Общие сведения об DOM | MDN"  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/beginners/html) и [Katherine Джексон][KatherineJackson] \ (помощник службы технической поддержки, Chrome DevTools \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[KatherineJackson]: https://developers.google.com/web/resources/contributors/katjackson  
