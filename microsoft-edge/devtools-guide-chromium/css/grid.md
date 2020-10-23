---
description: Сведения о том, как использовать Microsoft Edge DevTools для просмотра и изменения CSS для страниц CSS.
title: Проверка сетки CSS в Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/22/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 150aea57aa676580b554cc74292671ed567a0a2c
ms.sourcegitcommit: 6e2b26d41a0aa56ac34e6edc7dddd852ddb415b1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/23/2020
ms.locfileid: "11134152"
---
# Проверка сетки CSS  

В этой статье описано, как определить сетки CSS на веб-сайте и выявить проблемы макета сетки с помощью настраиваемых наложений сетки.  

Примеры, используемые на рисунках в этой статье, взяты из следующих веб-страниц.  

*   [Поле "фруктов"][JecFyiDemoCssGridFruit]  
*   [Поле питанию][JecFyiDemoCssGridSnack]  

## Перед началом работы  

Сетка CSS — это мощная парадигма макета для веб-сайта.  Это удобное место для изучения сетки каскадных стилей, а многие функции — руководство по [макету сетки CSS][MdnCssGridLayout] на MDN.  

## Знакомство с таблицами CSS  

Если на странице применен HTML-элемент `display: grid` , на `display: inline-grid` `grid` панели " [элементы][DevtoolsGuideChromiumOpen] " рядом с ним отображается индикатор.  

:::image type="complex" source="../media/grid-discover-grid.msft.png" alt-text="Сетка &quot;Поиск&quot;" lightbox="../media/grid-discover-grid.msft.png":::
   Сетка "Поиск"  
:::image-end:::  

Щелкните значок, чтобы включить или отключить наложение сетки на странице.  Для отображения положения линий сетки и дорожек на элементе появляется наложенный указатель на элемент в виде сетки.  

:::image type="complex" source="../media/grid-highlight-grid.msft.png" alt-text="Сетка &quot;Поиск&quot;" lightbox="../media/grid-highlight-grid.msft.png":::
   Отображение значка сетки  
:::image-end:::  

Открытие области " **Макет** ".  Если на странице включены сетки, в области **макетов** имеется раздел **Grid** , содержащий ряд параметров для просмотра сетки.  

:::image type="complex" source="../media/grid-layout-pane.msft.png" alt-text="Сетка &quot;Поиск&quot;" lightbox="../media/grid-layout-pane.msft.png":::
   Область " **Макет** "  
:::image-end:::  

Раздел **Grid** в области " **Макет** " включает следующие 2 подраздела.  

*   Параметры отображения наложения  
*   Наложения сетки  

<!--todo: @zoher verify the details for each of the sub-sections.  -->  

## Параметры отображения наложения  

**Параметры отображения наложения** состоят из следующих двух частей.  

*   В раскрывающемся меню выберите один из следующих параметров.  
    
    | Параметр линии | Сведения |  
    |:--- |:--- |  
    | **Скрытие меток линий** | Скрыть метки линий для каждой наложения сетки. |  
    | **Показывать номера строк** | Отображение номеров строк для каждого перекрытия сетки \ (выбрано по умолчанию \). |  
    | **Показывать названия строк** | Отображение названий строк для каждого перекрытия сетки при указании имен. |  
    
*  Установите флажок рядом с приведенными ниже параметрами.  
    
    | Параметр | Сведения |  
    |:--- |:--- |  
    | **Показать размеры дорожек**  | Отображение и скрытие размера дорожек. |  
    | **Показать имена областей** | Выводится название области (или скрыть ее), когда указаны имена. |  
    | **Увеличение линий сетки** | Отображает (или скрывает) расширения размеров сетки вдоль каждой оси.  По умолчанию линии сетки отображаются только в элементе с `display: grid` `display: inline-grid` установленным для него или CSS. |  
    
В следующих разделах приведены подробные сведения о каждом из **параметров отображения наложения**.  

### Показывать номера строк  

По умолчанию в наложение сетки отображаются положительные и отрицательные номера строк.  

Для получения дополнительных сведений об отрицательных числах в наложение сетки перейдите в раздел [расположение на строке с таблицей каскадных стилей][MdnLineBasedPlacementCssGrid].  

:::image type="complex" source="../media/grid-show-line-numbers.msft.png" alt-text="Сетка &quot;Поиск&quot;" lightbox="../media/grid-show-line-numbers.msft.png":::
   Отображение номеров строк  
:::image-end:::  

### Скрытие меток линий  

Выберите команду **Скрыть метки линии** , чтобы скрыть номера строк.  

:::image type="complex" source="../media/grid-hide-line-labels.msft.png" alt-text="Сетка &quot;Поиск&quot;" lightbox="../media/grid-hide-line-labels.msft.png":::
   Скрытие меток линий  
:::image-end:::  

### Показывать названия строк  

<!--todo: @rachel verify the link and text for line name -->  
Чтобы получить дополнительные сведения о названиях линий в наложения сетки, перейдите в раздел [макет с помощью именованных линий сетки][MdnLayoutUsingNamedGridLines].  

Выберите **Показывать названия строк** , чтобы просмотреть названия строк вместо чисел.  В примере 4 строки имеют имена: `left` , `middle1` , `middle2` и `right` .  

<!--In the demo, **orange** element spans from left to right, with `grid-column: left` and `grid-column: right` CSS.  Showing line names makes it easier to visualize the start and end position of the element.  -->  

:::image type="complex" source="../media/grid-show-line-names.msft.png" alt-text="Сетка &quot;Поиск&quot;" lightbox="../media/grid-show-line-names.msft.png":::
   **Показывать названия строк**  
:::image-end:::  

### Показать размеры дорожек  

Установите флажок **Показывать размеры дорожек** для просмотра размеров сетки.  

DevTools отображает `[authored size]` и `[computed size]` в каждой метке строки.  

| Size | Сведения |  
|:--- |:--- |  
| **Авторский размер** | Размер, определенный в таблице стилей \ (опущено, если не определено). |  
| **вычисляемый размер** | Реальный размер на экране. |  

В роликах `snack-box` размеры столбцов определяются в `grid-template-columns:1fr 2fr;` CSS.  Таким образом, Метки строк столбцов выводят как созданные, так и вычисляемые размеры.  

| Размер дорожки | Авторский размер | Вычисляемый размер |  
|:--- |:--- |:--- |  
| **1fr** &#x2022; **96.66 px** | 1fr | 96.66 px |  
| **2fr** &#x2022; **193.32 px** | 2fr | 193.32 px |  

В названиях строк строки отображаются только вычисляемые размеры, так как в таблице стилей не определена ни одна из размеров строк.  

| Размер дорожки | Авторский размер | Вычисляемый размер |  
|:--- |:--- |:--- |  
| **80px** | &nbsp;| 80px |  
| **80px** | &nbsp;| 80px |  

:::image type="complex" source="../media/grid-show-track-sizes.msft.png" alt-text="Сетка &quot;Поиск&quot;" lightbox="../media/grid-show-track-sizes.msft.png":::
   **Показать размеры дорожек**  
:::image-end:::  

### Показать имена областей  

Чтобы просмотреть названия областей, установите флажок **Показывать имена областей** .  В примере таблица Grid имеет три области: **Top**, **bottom1** и **bottom2**.  

:::image type="complex" source="../media/grid-show-area-names.msft.png" alt-text="Сетка &quot;Поиск&quot;" lightbox="../media/grid-show-area-names.msft.png":::
   **Показать имена областей**  
:::image-end:::  

### Увеличение линий сетки  

Установите флажок **удлинить линии сетки** , чтобы распространить линии сетки по краям окна просмотра на каждой оси.  

:::image type="complex" source="../media/grid-extend-grid-lines.msft.png" alt-text="Сетка &quot;Поиск&quot;" lightbox="../media/grid-extend-grid-lines.msft.png":::
   **Увеличение линий сетки**  
:::image-end:::  

## Наложения сетки  

Раздел ' ' **наложенные сетки** ' ' включает список сеток, присутствующих на странице, каждый с флажком, а также различные параметры.  

### Включение многоналоженных представлений нескольких сеток  

<!--todo: @zoher verify and provide updates -->  

Чтобы отобразить наложение сетки для нескольких сеток, установите флажок рядом с именем сетки.  В примере используются два наложенных перекрытия сетки, каждый из которых представлен различными цветами.  

*   `main`  
*   `div.snack-box`  
    
:::image type="complex" source="../media/grid-grid-overlays.msft.png" alt-text="Сетка &quot;Поиск&quot;" lightbox="../media/grid-grid-overlays.msft.png":::
   Включение многоналоженных представлений нескольких сеток  
:::image-end:::  

### Настройка цвета наложения сетки  

Чтобы открыть окно выбора цвета и настроить цвет наложения сетки, установите флажок рядом с именем наложения сетки.  

:::image type="complex" source="../media/grid-grid-overlays-color.msft.png" alt-text="Сетка &quot;Поиск&quot;" lightbox="../media/grid-grid-overlays-color.msft.png":::
   Настройка цвета наложения сетки  
:::image-end:::  

### Выделение сетки  

Чтобы выделиь элемент HTML на панели **элементы** и прокрутить его на веб-странице, выберите **элемент Показать на панели элементы** \ ( ![ Показать элемент на значке панели элементов \ ][ImageShowElementInElementsPanelIcon] ).  

:::image type="complex" source="../media/grid-grid-overlays-highlight.msft.png" alt-text="Сетка &quot;Поиск&quot;" lightbox="../media/grid-grid-overlays-highlight.msft.png":::
   Выделение сетки  
:::image-end:::  

## Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageShowElementInElementsPanelIcon]: ../media/show-element-in-element-panel-icon.msft.png  

<!-- links -->  

[DevtoolsGuideChromiumOpen]: ../open.md "Открыть Microsoft Edge DevTools | Документы Microsoft"  

[JecFyiDemoCssGridFruit]: https://jec.fyi/demo/css-grid-fruit "Сетка CSS | JEC к сведению"  
[JecFyiDemoCssGridSnack]: https://jec.fyi/demo/css-grid-snack "Сетка CSS | JEC к сведению"  

[MdnCssGridLayout]: https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout "Макет сетки CSS | MDN"  
[MdnLayoutUsingNamedGridLines]: https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout/Layout_using_Named_Grid_Lines "Макет с помощью именованных линий сетки | MDN"  
[MdnLineBasedPlacementCssGrid]: https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout/Line-based_Placement_with_CSS_Grid "Размещение на основе строк с сеткой CSS | MDN"  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница [будет найдена, и](https://developers.google.com/web/tools/chrome-devtools/css/grid) ее можно создать с помощью [Jecelyn Yeen][JecelynYeen] \ (разработчик отвечает, Chrome DevTools \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
