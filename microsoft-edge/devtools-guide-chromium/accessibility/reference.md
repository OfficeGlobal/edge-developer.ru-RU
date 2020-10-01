---
description: Исчерпывающая Справка по специальным возможностям в Microsoft Edge DevTools.
title: Справка по специальным возможностям
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 39b0b8c36cea017b9976ea4e80e92ea93896a671
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993270"
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

# Справка по специальным возможностям  

Эта страница является исчерпывающей ссылкой на специальные возможности в Microsoft Edge DevTools.  Оно предназначено для веб-разработчиков, которые:  

*   Разработайте основные принципы DevTools, например, как открыть ее.  
*   Знакомы с [принципами специальных возможностей и][MDNAccessibility]рекомендациями.  
    
Цель этой ссылки — помочь вам найти все средства, доступные в DevTools, которые помогут вам изучить специальные возможности на странице.  

Если вы ищете справку по переходу на DevTools с помощью специальных возможностей, таких как средство чтения с экрана, вы узнаете о том, что нужно сделать для навигации по [Microsoft Edge DevTools с технологией специальных возможностей][DevtoolsAccessibilityNavigation] .  

## Общие сведения о специальных возможностях в Microsoft Edge DevTools  

В этом разделе объясняется, как DevTools в общий набор средств для специальных возможностей.  

Если вы решите, что страница доступна, вам нужно будет 2 общих вопросов.  

1.  Вы можете перемещаться по странице с помощью клавиатуры или [средства чтения с экрана][MDNScreenReader]?  
1.  Правильно ли помечены элементы страницы для средств чтения с экрана?  
    
Как правило, DevTools поможет устранить ошибки, связанные с вопросами #2, так как эти ошибки легко выявить автоматически.  Вопрос #1 так же важен, но, к сожалению, DevTools не поможет вам.  Единственный способ найти ошибки, связанные с вопросом #1, — попытаться использовать страницу с помощью клавиатуры или средства чтения с экрана самостоятельно.  <!--See [How To Do An Accessibility Review][AccessibilityReview] to learn more.  -->  

<!--[AccessibilityReview]: /web/fundamentals/accessibility/how-to-review  -->  

## Аудит специальных возможностей страницы  

> [!NOTE]
> Панель **Аудит** содержит ссылки на содержимое, размещенное на сторонних веб-сайтах.  Корпорация Майкрософт не несет ответственности за контент этих сайтов и любые данные, которые могут быть собраны, и не может контролировать их.  

Как правило, с помощью панели аудит вы можете определить, есть ли в следующих случаях:  

*   Страница правильно помечена для средств чтения с экрана.  
*   Элементы текста на странице имеют достаточные коэффициенты контрастности.  Посмотрите [Просмотр коэффициента контрастности текстового элемента в средстве выбора цвета](#view-the-contrast-ratio-of-a-text-element-in-the-color-picker).  

Чтобы выполнить аудит страницы, выполните указанные ниже действия.  

1.  Перейдите к URL-адресу, на который вы хотите подвестись.  
1.  В DevTools откройте вкладку **аудитория** .  DevTools показывает различные параметры конфигурации.  
    
    :::image type="complex" source="../media/accessibility-audits-pane.msft.png" alt-text="Настройка аудита" lightbox="../media/accessibility-audits-pane.msft.png":::
       Настройка аудита  
    :::image-end:::  
    
    > [!NOTE]
    > Снимки экрана в этом разделе собраны в версии 79 Microsoft Edge.  Вы можете проверить, на какой версии вы работаете `edge://version` .  В более ранних версиях Microsoft Edge пользовательский интерфейс панели **аудита** выглядит иначе, но общий рабочий процесс одинаков.  
    
1.  Для **устройства**выберите **мобильные** устройства, если вы хотите имитировать мобильное устройство.  Этот параметр позволяет изменить строку вашего агента пользователя и изменить размер окна просмотра.  Если Мобильная версия страницы отображается не так, как для классической версии, этот параметр может существенно повлиять на результаты аудита.  
1.  Убедитесь, что в разделе " **Аудит** " включен параметр " **Специальные возможности** ".  Отключите другие категории, если вы хотите исключить их из отчета.  Если вы хотите найти другие способы улучшить качество страницы, оставьте это поле пустым.  
1.  Раздел **регулирования** позволяет регулировать сеть и ЦП, что бывает полезно при анализе производительности нагрузки.  Этот параметр должен быть неважен для оценки доступности, поэтому вы можете использовать любой из них.  
1.  Флажок **clear Storage (очистить хранилище** ) позволяет очистить все хранилище перед загрузкой страницы или сохранением хранилища между загрузкой страниц.  Этот параметр также может быть неважен для оценки доступности, поэтому вы можете использовать любой из них.  
1.  Нажмите кнопку **запустить аудиты**. После 10 – 30 секунд DevTools предоставляет отчет.  В отчете приводятся различные советы по улучшению доступности страницы.  
    
    :::image type="complex" source="../media/accessibility-audits-run-audits-result.msft.png" alt-text="Настройка аудита" lightbox="../media/accessibility-audits-run-audits-result.msft.png":::
       Отчет  
    :::image-end:::  
    
1.  Щелкните аудиторию, чтобы получить дополнительные сведения о нем.  
    
    :::image type="complex" source="../media/accessibility-audits-run-audits-result-issues-expanded.msft.png" alt-text="Настройка аудита" lightbox="../media/accessibility-audits-run-audits-result-issues-expanded.msft.png":::
       Дополнительные сведения об аудите  
    :::image-end:::  
    
1.  Щелкните ссылку **Дополнительные сведения** , чтобы просмотреть документацию по аудиту.  
    
    :::image type="complex" source="../media/accessibility-web-dev-accessibility-audits-learn-more.msft.png" alt-text="Настройка аудита" lightbox="../media/accessibility-web-dev-accessibility-audits-learn-more.msft.png":::
       Просмотр документации по аудиту  
    :::image-end:::  
    
### Дополнительные сведения: расширение aXe  

Вы можете использовать [расширение aXe][ChromeWebStoreAxe] , а не панель **аудита** .  
Расширение aXe обычно предоставляет те же сведения, так как это базовый обработчик, который включает в себя панель аудита.  Расширение aXe имеет другой пользовательский интерфейс и описывает аудит слегка разными способами.  
Одно из преимуществ, которое имеет расширение aXe на панели **аудитов** , состоит в том, что она позволяет проверять и вымечать узлы, в которых произошел сбой.  

:::image type="complex" source="../media/accessibility-devtools-extension-axe-panel.msft.png" alt-text="Настройка аудита" lightbox="../media/accessibility-devtools-extension-axe-panel.msft.png":::
   Расширение aXe  
:::image-end:::  

## Область "Специальные возможности"  

В области " **Специальные возможности** " можно просмотреть дерево специальных возможностей, атрибуты ARIA и вычисляемые свойства специальных возможностей узлов DOM.  

Чтобы открыть область " **Специальные возможности** ", выполните указанные ниже действия.  

1.  Откройте вкладку **элементы** .  
1.  В **дереве DOM**выберите элемент, который нужно проверить.  
1.  Откройте вкладку **Специальные возможности** .  Эта вкладка может быть скрыта за кнопкой **другие вкладки** \ ( ![ другие вкладки ][ImageMoreTabsIcon] \).  

:::image type="complex" source="../media/accessibility-elements-accessibility.msft.png" alt-text="Настройка аудита" lightbox="../media/accessibility-elements-accessibility.msft.png":::
   Проверка `h1` элемента домашней страницы DevTools в области " **Специальные возможности** "  
:::image-end:::  

### Просмотр положения элемента в дереве специальных возможностей  

[Дерево специальных возможностей][MDNAccessibilityTree] — это подмножество дерева DOM.  Она включает только элементы из дерева DOM, которые являются важными и полезны для отображения содержимого страницы в средстве чтения с экрана.  

Проверьте расположение элемента в дереве специальных возможностей в [области "Специальные возможности](#the-accessibility-pane)".  

:::image type="complex" source="../media/accessibility-elements-accessibility-tree.msft.png" alt-text="Настройка аудита" lightbox="../media/accessibility-elements-accessibility-tree.msft.png":::
   Раздел **дерева специальных возможностей**  
:::image-end:::  

### Просмотр атрибутов ARIA элемента  

Атрибуты ARIA гарантируют, что средства чтения с экрана имеют всю необходимую информацию для правильного представления содержимого страницы.  

Просмотрите атрибуты ARIA элемента в [области "Специальные возможности](#the-accessibility-pane)".  

:::image type="complex" source="../media/accessibility-elements-accessibility-aria-attributes.msft.png" alt-text="Настройка аудита" lightbox="../media/accessibility-elements-accessibility-aria-attributes.msft.png":::
   Раздел **атрибутов ARIA**  
:::image-end:::  

### Просмотр вычисляемых свойств специальных возможностей для элемента  

> [!NOTE]
> Если вы ищете вычисляемые свойства CSS, ознакомьтесь с [Разсчитанной вкладкой][DevtoolsCssReferenceViewActuallyAppliedElements].  

Некоторые свойства специальных возможностей динамически рассчитываются браузером.  Эти свойства отображаются в разделе " **вычисляемые свойства** " области " **Специальные возможности** ".  

Просмотр вычисляемых свойств специальных возможностей для элемента в [области специальных возможностей](#the-accessibility-pane).  

:::image type="complex" source="../media/accessibility-elements-accessibility-computed-properties.msft.png" alt-text="Настройка аудита" lightbox="../media/accessibility-elements-accessibility-computed-properties.msft.png":::
   Раздел " **вычисляемые свойства** " области " **Специальные возможности** "  
:::image-end:::  

## Просмотр коэффициента контрастности текстового элемента в палитре цветов  

Некоторые люди со слабым зрением не видят области как очень яркие или очень темные.  Все обычно выводятся примерно одинаковая яркость, что делает ее более четкими и контурами.  

Коэффициент контрастности измеряет разницу яркости между передним и фоном текста.  Если текст имеет низкую степень контрастности, пользователи с низким зрением могут в буквальном смысле работать с вашим сайтом в качестве пустого экрана.  

С помощью средства выбора цвета вы можете убедиться, что текст соответствует рекомендуемым уровням контрастности:  

1.  Откройте вкладку **элементы** .  
1.  В **дереве DOM**выделите текстовый элемент, который нужно проверить.  
    
    :::image type="complex" source="../media/accessibility-elements-paragraph-highlight.msft.png" alt-text="Настройка аудита" lightbox="../media/accessibility-elements-paragraph-highlight.msft.png":::
       Проверка абзаца в **дереве DOM**  
    :::image-end:::  
    
1.  В области **стили** щелкните квадратик цвета рядом со `color` значением элемента.  
    
    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color.msft.png" alt-text="Настройка аудита" lightbox="../media/accessibility-elements-styles-paragraph-highlight-color.msft.png":::
       `color`Свойство элемента  
    :::image-end:::  
    
1.  Проверьте раздел **коэффициент контрастности** в палитре цветов.  Один флажок означает, что элемент соответствует [минимальным рекомендациям][W3CContrastMinimum].  Два флажка означают, что они соответствуют [улучшенным рекомендациям][W3CContrastEnhanced].  
    
    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color-picker.msft.png" alt-text="Настройка аудита" lightbox="../media/accessibility-elements-styles-paragraph-highlight-color-picker.msft.png":::
       В разделе " **степень контрастности** " в окне выбора цвета показаны 2 метки и значение `13.97`  
    :::image-end:::  
    
1.  Щелкните раздел **коэффициент контрастности** , чтобы просмотреть дополнительные сведения.  В визуальном элементе выбора в верхней части окна выбора цвета появится линия.  Если текущий цвет соответствует рекомендациям, то все элементы на одной и той же стороне линии также соответствуют рекомендациям.  Если текущий цвет не соответствует рекомендациям, то на одном и том же стороне не будут выводится соответствие рекомендациям.  
    
    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color-picker-contrast-ratio-details.msft.png" alt-text="Настройка аудита" lightbox="../media/accessibility-elements-styles-paragraph-highlight-color-picker-contrast-ratio-details.msft.png":::
       Линия **коэффициента контрастности** в средстве выбора визуальных элементов  
    :::image-end:::  
    
<!--## Feedback   -->  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageMoreTabsIcon]: ../media/more-tabs-icon.msft.png  

<!-- links -->  

[DevtoolsAccessibilityNavigation]: ./navigation.md "Навигация в Microsoft Edge DevTools с технологией специальных возможностей | Документы Microsoft"  
[DevtoolsCssReferenceViewActuallyAppliedElements]: ../css/reference.md#view-only-the-css-that-is-actually-applied-to-an-element "Просмотр только CSS, которая фактически применяется к ссылке element-CSS | Документы Microsoft"  

[ChromeWebStoreAxe]: https://chrome.google.com/webstore/detail/axe/lhdoppojpmngadmnindnejefpokejbdd?hl=en-US "Axe — тестирование специальных возможностей в Интернете-веб-магазин Chrome"  

[MDNAccessibilityTree]: https://developer.mozilla.org/docs/Glossary/AOM "Дерево специальных возможностей (AOM) | MDN"  
[MDNAccessibility]: https://developer.mozilla.org/docs/Web/Accessibility "Специальные возможности | MDN"  
[MDNScreenReader]: https://developer.mozilla.org/docs/Glossary/Screen_reader "Средство чтения с экрана | MDN"  

[W3CContrastEnhanced]: https://www.w3.org/WAI/WCAG21/quickref/#contrast-enhanced "Контрастность (улучшенная) уровень AAA | PNG"  
[W3CContrastMinimum]: https://www.w3.org/WAI/WCAG21/quickref/#contrast-minimum "Контрастность (минимум) уровень AA | PNG"  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
