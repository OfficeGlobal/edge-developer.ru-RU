---
description: Сведения о том, как использовать Microsoft Edge DevTools для просмотра и изменения CSS-страниц.
title: Начало работы с просмотром и редактированием CSS
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 3cd833c97cb2e7b746943f18526d09481b4e3cc5
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125211"
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

# Начало работы с просмотром и редактированием CSS  

Эти интерактивные учебники помогут вам ознакомиться с основными принципами просмотра и изменения CSS для страниц с помощью Microsoft Edge DevTools.  

## Открытие примеров CSS  

1.  Удерживайте клавишу `Control` \ (Windows, Linux \) или `Command` \ (macOS \) и выберите **CSS-примеры** , которые нужно открыть в новом окне.  
    
    [Примеры CSS][GlitchDevToolsCssExamples]  
    
    > [!NOTE]
    > Если вы хотите [закрепить окно DevTools][DevToolsCustomizePlacement] справа от окна просмотра \ (на рисунке ниже), выберите **Настройка и управление DevTools** `...` .  В раскрывающемся меню **Настройка и управление DevTools** в разделе **закрепляемая на стороне** нажмите кнопку **закрепить вправо**.  
    
## Просмотр CSS для элемента  

1.  [Откройте примеры CSS](#open-css-examples).  
1.  Наведите указатель мыши на `Inspect Me!` текст, откройте контекстное меню, а затем выберите команду **проверить**.  
    1.  В DevTools на панели " **элементы** " на вкладке " **дерево DOM** " `Inspect Me!` выделена кнопка "элемент".  
        
        :::image type="complex" source="../media/css-elements-inspect-me.msft.png" alt-text="Проверяемый элемент выделен в дереве DOM" lightbox="../media/css-elements-inspect-me.msft.png":::
           Рисунок 1: в **дереве DOM** выделено проверенный элемент  
        :::image-end:::  
        
    1.  `Inspect Me!`Найдите значение атрибута в элементе `data-message` и скопируйте его.  
1.  На странице в поле **значение `data-message` :** введите значение.  
1.  Наведите указатель мыши на `Inspect Me!` текст, откройте контекстное меню, а затем выберите команду **проверить**.  
    1.  В DevTools на панели **элементы** откройте вкладку **стили** .  
    1.  На вкладке **стили** `Inspect Me!` элемент выделен.  
    1.  В `Inspect Me!` элементе найдите `aloha` правило класса.  
        
        > [!NOTE]
        > Вы видите это правило, так как оно применяется к `Inspect Me!` элементу.  
        
    1.  В `aloha` классе найдите значение для `padding` стиля и скопируйте его.  
        
        :::image type="complex" source="../media/css-elements-inspect-me-styles.msft.png" alt-text="Проверяемый элемент выделен в дереве DOM" lightbox="../media/css-elements-inspect-me-styles.msft.png":::
           Рисунок 2: классы CSS, примененные к выбранному элементу, такие как `aloha` , отображаются на вкладке **стили**  
        :::image-end:::  
        
1.  На странице в поле **значение `padding` :** введите значение.  

## Добавление объявления CSS в элемент  

Используйте вкладку **стили** , если вы хотите изменить или добавить объявления CSS к элементу.  

> [!NOTE]
> Завершите [Просмотр CSS для](#view-the-css-for-an-element) учебника по элементу, прежде чем сделать это.  

1.  [Откройте примеры CSS](#open-css-examples).  
1.  Наведите указатель мыши на `Add A Background Color To Me!` текст, откройте контекстное меню, а затем выберите команду **проверить**.  
1.  Нажмите кнопку в `element.style` верхней части вкладки **стили** .  
1.  Введите текст `background-color` и выберите его `Enter` .  
1.  Введите текст `honeydew` и выберите его `Enter` .  В **дереве DOM** вы увидите, что к элементу применено объявление встроенного стиля.  
    
    :::image type="complex" source="../media/css-elements-add-background-color-to-me-styles-p.msft.png" alt-text="Проверяемый элемент выделен в дереве DOM" lightbox="../media/css-elements-add-background-color-to-me-styles-p.msft.png":::
       Рисунок 3: `background-color:honeydew` объявление применено к элементу с помощью `element.style` раздела вкладки " **стили** "  
    :::image-end:::  
    
## Добавление класса CSS в элемент  

С помощью вкладки " **стили** " можно увидеть, как выглядит элемент, когда класс CSS применяется к элементу или удаляется из него.  

> [!NOTE]
> Завершите [Просмотр CSS для](#view-the-css-for-an-element) учебника по элементу, прежде чем сделать это.  

1.  [Откройте примеры CSS](#open-css-examples).  
1.  Наведите указатель мыши на `Add A Class To Me!` текст, откройте контекстное меню, а затем выберите команду **проверить**.  
1.  Выберите **. CLS**.  DevTools открывает текстовое поле, в котором можно добавлять классы к выбранному элементу.  
1.  Введите `color_me` текст в текстовом поле **Добавить новый класс** и нажмите кнопку `Enter` .  Флажок отображается под текстовым полем " **Добавить новый класс** ", в котором можно включить или отключить класс.  Если `Add A Class To Me!` к элементу применены другие классы, вы также можете переключаться между ними.  
    
    :::image type="complex" source="../media/css-elements-add-a-class-to-me-styles-cls.msft.png" alt-text="Проверяемый элемент выделен в дереве DOM" lightbox="../media/css-elements-add-a-class-to-me-styles-cls.msft.png":::
       Рисунок 4: `color_me` класс применен к элементу с помощью раздела **. CLS** на вкладке " **стили** ".  
    :::image-end:::  
    
## Добавление PseudoState в класс  

С помощью вкладки **стили** вы можете навсегда применить CSS-PseudoState к элементу.  DevTools поддерживает `:active` , `:focus` , `:hover` , и `:visited` .  

> [!NOTE]
> Завершите [Просмотр CSS для](#view-the-css-for-an-element) учебника по элементу, прежде чем сделать это.  

1.  [Откройте примеры CSS](#open-css-examples).  
1.  Наведите указатель мыши на `Hover Over Me!` текст.  Цвет фона изменится.  
1.  Наведите указатель мыши на `Hover Over Me!` текст, откройте контекстное меню, а затем выберите команду **проверить**.  
1.  На вкладке **стили** выберите **: Hov**.  
1.  Установите флажок **: наведение указателя мыши** .  Цвет фона изменится так же, как и раньше, несмотря на то, что вы не наводите указатель мыши на элемент.  
    
    :::image type="complex" source="../media/css-elements-hover-over-me-styles-hov-hover.msft.png" alt-text="Проверяемый элемент выделен в дереве DOM" lightbox="../media/css-elements-hover-over-me-styles-hov-hover.msft.png":::
       Рисунок 5: Переключение `:hover` PseudoState на элементе  
    :::image-end:::  
    
## Изменение размеров элемента  

С помощью интерактивной схемы **"модель Box** " на вкладке " **стили** " можно изменить ширину, высоту, заполнение, границу или длину границы элемента.  

> [!NOTE]
> Завершите [Просмотр CSS для](#view-the-css-for-an-element) учебника по элементу, прежде чем сделать это.  

1.  [Откройте примеры CSS](#open-css-examples).  
1.  Наведите указатель мыши на `Change My Margin!` текст, откройте контекстное меню, а затем выберите команду **проверить**.  
1.  На схеме **модель Box** на вкладке **стили** наведите указатель мыши на **Заполнение**.  Заполнение элемента выделено в окне просмотра.  

    > [!NOTE]
    > В зависимости от размера окна DevTools, возможно, потребуется прокрутить в нижнюю часть вкладки **стили** , чтобы увидеть **модель Box**.  

1.  Дважды щелкните левое поле в **модели Box**, которое в настоящее время имеет значение `-` , означающее, что у элемента нет левого поля.  
1.  Введите текст `100px` и выберите его `Enter` .  **Модель Box** по умолчанию имеет значения пикселей, но также принимает другие значения, например `25%` или `10vw` .  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/css-elements-change-my-margin-styles-padding.msft.png" alt-text="Проверяемый элемент выделен в дереве DOM" lightbox="../media/css-elements-change-my-margin-styles-padding.msft.png":::
             Рисунок 6: наведение указателя мыши на заполнение элемента  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/css-elements-change-my-margin-styles-margin-edit.msft.png" alt-text="Проверяемый элемент выделен в дереве DOM" lightbox="../media/css-elements-change-my-margin-styles-margin-edit.msft.png":::
             Рисунок 7: изменение левого поля элемента  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
## Отладка запросов мультимедиа  

С помощью [запросов мультимедиа][MDNUsingMediaGueries] можно сделать так, чтобы ваш веб-продукт реагировал на изменения параметров конфигурации для каждого пользователя.  Наиболее важным вариантом использования является предоставление для продукта другого макета CSS в зависимости от размеров окна просмотра.  Использование раздельных макетов позволяет создавать макеты с одним столбцом для мобильных устройств и многостолбцовый макет, если доступно больше свободного пространства на экране.  

Чтобы выполнить отладку или тестирование запросов мультимедиа, определенных в таблице CSS, выполните указанные ниже действия.  

1.  Откройте Инструменты разработчика и щелкните значок " **Переключить панель инструментов устройства** " в верхней части экрана или выберите `Ctrl` + `Shift` + `M` \ ( `Cmd` + `Shift` + `M` в macOS \).  
    
    :::image type="complex" source="../media/css-elements-media-queries-open-device-toolbar.msft.png" alt-text="Проверяемый элемент выделен в дереве DOM" lightbox="../media/css-elements-media-queries-open-device-toolbar.msft.png":::
       Рисунок 8: Открытие панели инструментов устройства  
    :::image-end:::  
    
1.  На панели инструментов устройства откройте `...` меню в верхнем правом углу и выберите **просмотреть запросы мультимедиа**.  На экран выводится цветная полоса, представляющая различные запросы мультимедиа.  
    
    :::image type="complex" source="../media/css-elements-media-queries-showing-mq.msft.png" alt-text="Проверяемый элемент выделен в дереве DOM" lightbox="../media/css-elements-media-queries-showing-mq.msft.png":::
       Рис. 9: отображение запросов мультимедиа на панели инструментов устройства  
    :::image-end:::  
    
1.  Наведите указатель мыши на границу линии, чтобы просмотреть значения различных запросов мультимедиа. Выберите каждый из них, чтобы изменить размер веб-страницы.  
    
    :::image type="complex" source="../media/css-elements-media-queries-select-bar.msft.png" alt-text="Проверяемый элемент выделен в дереве DOM" lightbox="../media/css-elements-media-queries-select-bar.msft.png":::
       Рисунок 10: выбор запроса мультимедиа из панели предварительного просмотра  
    :::image-end:::  
    
1.  Чтобы выполнить отладку запросов мультимедиа и открыть CSS-файл в `Sources` редакторе, наведите указатель мыши на любой из сегментов отрезков, откройте контекстное меню, а затем выберите команду `reveal in source code` .  
    
    :::image type="complex" source="../media/css-elements-media-queries-reveal-in-sources.msft.png" alt-text="Проверяемый элемент выделен в дереве DOM" lightbox="../media/css-elements-media-queries-reveal-in-sources.msft.png":::
       Рисунок 11: отображение запросов мультимедиа в редакторе источников  
    :::image-end:::  
    
## Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsCustomizePlacement]: /microsoft-edge/devtools-guide-chromium/customize/placement "Изменение положения DevTools Microsoft EDGE (Отстыковка, закрепить в нижней части, закрепить слева)"  

[GlitchDevToolsCssExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/css/examples/ecma.html "Примеры CSS — Microsoft EDGE (Chromium) DevTools | Цепь"  

[MDNUsingMediaGueries]: https://developer.mozilla.org/docs/Web/CSS/Media_Queries/Using_media_queries "Использование мультимедийных запросов | MDN"  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/css/index) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
