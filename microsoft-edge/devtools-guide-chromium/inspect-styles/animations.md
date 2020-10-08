---
description: Просмотрите и измените анимацию с помощью инспектора анимации Microsoft Edge DevTools.
title: Проверка эффектов анимации
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: e867cc373286666f73bee3b8fb886f60fa1b94f6
ms.sourcegitcommit: d360e419b5f96f4f691cf7330b0d8dff9126f82e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/15/2020
ms.locfileid: "11015774"
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

# Проверка эффектов анимации  

Просмотрите и измените анимацию с помощью инспектора анимации Microsoft Edge DevTools.  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations-completed.msft.png" alt-text="Инспектор анимации" lightbox="../media/inspect-styles-elements-styles-drawer-animations-completed.msft.png":::
   Инспектор анимации  
:::image-end:::  

### Краткий обзор  

*   Запишите анимацию, открыв инспектор анимации.  Инспектор анимации автоматически определяет и сортирует анимации в группах.  
*   Изучите анимацию, заменив каждую из них, воспроизводить каждую из них или просматривая исходный код.  
*   Изменяйте анимацию, изменяя время, задержку, продолжительность или смещение опорных кадров.  

## Обзор  

Инспектор анимации Microsoft Edge DevTools имеет два основных назначения.  

*   Проверка анимации.  Вы хотите замедлить, воспроизвести или проверить исходный код для группы анимации.  
*   Изменение анимаций.  Вы хотите изменить время, задержку, длительность или смещение кадров в группе анимации.  Редактирование Безье и изменение опорных кадров в настоящее время не поддерживается.  

Инспектор анимации поддерживает анимацию CSS, переходы CSS и веб-анимации.  `requestAnimationFrame` анимации в настоящее время не поддерживаются.  

### Что такое группа анимации?  

Группа анимации — это группа анимаций, которые могут быть связаны друг с другом.  В настоящее время в веб-браузере отсутствует фактическая Концепция групповых анимаций, поэтому разработчики движений и разработчиков должны создавать и обрабатывать отдельные анимации, чтобы анимация отображалась как один и тот же визуальный эффект.  Инспектор анимации прогнозирует, какие анимации связаны с учетом времени начала, (за исключением задержек и т. д.).  Инспектор анимации также группирует анимацию рядом друг с другом.  
Другими словами, набор анимаций, которые вызываются в одном блоке сценария, группируются вместе.  Если анимация является асинхронной, она помещается в отдельную группу.  

## Get started  

Открыть инспектор анимации можно двумя способами:  

*   Открытие меню " **Настройка и управление DevTools** "  
    1.  Перейдите к вложенному меню **другие инструменты** .  
    1.  Выберите **анимации**:  
        
        :::image type="complex" source="../media/inspect-styles-elements-styles-more-tools-animations.msft.png" alt-text="Инспектор анимации" lightbox="../media/inspect-styles-elements-styles-more-tools-animations.msft.png":::
           **Анимация** с помощью главного меню  
    :::image-end:::  
        
*   Открытие **меню команд**  
    1.  Введите `Drawer: Show Animations`.  

Инспектор анимации открывается в виде вкладки рядом с лотком консоли.  Поскольку инспектор анимаций является вкладкой ящика, вы можете использовать инспектор анимации на любой DevTools панели.  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations.msft.png" alt-text="Инспектор анимации" lightbox="../media/inspect-styles-elements-styles-drawer-animations.msft.png":::
   Пустой инспектор анимации  
:::image-end:::  

Инспектор анимации сгруппирован в четыре основных раздела \ (или области).  Это руководство относится к каждой области, как описано ниже.  

| Индекс | Панель | Описание |  
|:--- |:--- |:--- |  
| 1,1 | **Элементы управления** | Здесь вы можете очистить все текущие группы анимации или изменить скорость выбранной в данный момент группы анимации. |  
| 2 | **Обзор** | Выберите группу анимации, чтобы проверить ее и изменить ее в области **сведений** . |  
| Трехконтактный | **Информация о сроках** | Задержите и начните анимацию отсюда или переходите к определенной точке анимации. |  
| четырехпроцессорном | **Сведения** | Проверка и изменение выбранной в данный момент группы эффектов анимации. |  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations-selected-paused.msft.png" alt-text="Инспектор анимации" lightbox="../media/inspect-styles-elements-styles-drawer-animations-selected-paused.msft.png":::
   Инспектор анимации с заметками  
:::image-end:::  

Чтобы зафиксировать анимацию, просто выполните взаимодействие, которое запускает анимацию, когда открыт Инспектор анимации.  Если анимация запускается при загрузке страницы, перезагрузите страницу с помощью инспектора анимации, чтобы определить анимацию.  

<!--  old link: <video src="animations/capture-animations.mp4" autoplay loop muted controls></video>  -->  

<!--  import the video to ACOM using https://review.docs.microsoft.com/en-us/help/contribute/contribute-video-publish?branch=master  -->  

<!--  > [!VIDEO animations/capture-animations.mp4]  -->  

## Проверка эффектов анимации  

После захвата анимации есть несколько способов воспроизведения.  

*   Наведите указатель мыши на эскиз в области " **Обзор** ", чтобы просмотреть его в предварительной версии.  
*   В области " **Обзор** " выберите группу анимации \ (чтобы она отображалась в области **сведений** ) и нажмите значок " **воспроизвести** " ( ![ значок воспроизведения ][ImageReplayButtonIcon] \).  Анимация воспроизводится в окне просмотра.  Щелкните значок **скорость анимации** \ ( ![ значки скорости анимации ][ImageAnimationSpeedButtonsIcon] \), чтобы изменить скорость просмотра выбранной группы анимации.  Вы можете изменить текущее расположение с помощью красной вертикальной черты.  
*   Щелкните и перетащите красную вертикальную полосу, чтобы проочистки анимации просмотра.  
    
### Просмотр подробных сведений о анимации  

После захвата группы анимации щелкните ее в области " **Обзор** ", чтобы просмотреть подробные сведения.  В области **сведений** каждая из анимаций назначается отдельной строке.  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations-selected-completed.msft.png" alt-text="Инспектор анимации" lightbox="../media/inspect-styles-elements-styles-drawer-animations-selected-completed.msft.png":::
   Сведения о группе эффектов анимации  
:::image-end:::  

Наведите указатель мыши на анимацию, чтобы выделить ее в окне просмотра.  Щелкните анимацию, чтобы выделить ее на панели " **элементы** ".  

:::image type="complex" source="../media/inspect-styles-split-elements-styles-drawer-animations-selected-completed.msft.png" alt-text="Инспектор анимации" lightbox="../media/inspect-styles-split-elements-styles-drawer-animations-selected-completed.msft.png":::
   Наведите указатель мыши на анимацию, чтобы выделить ее в окне просмотра  
:::image-end:::  

Самым левым и темным разделом анимации является определение.  Справа, более размытые части представляют собой итерации.  Например, на приведенном ниже рисунке две и три части представляют собой итерации раздела One.  

:::image type="complex" source="../media/inspect-styles-glitch-display-animations-highlight.msft.png" alt-text="Инспектор анимации" lightbox="../media/inspect-styles-glitch-display-animations-highlight.msft.png":::
   Схема итераций анимации  
:::image-end:::  

Если к двум элементам применена одинаковая анимация, инспектор анимации назначает элементам один и тот же цвет.  Цвет является произвольным и не имеет значимости.  Например, на приведенном ниже рисунке показаны два элемента `div.cwccw.earlier` и `div.cwccw.later` применена одинаковая анимация \ ( `spinrightleft` \), как `div.ccwcw.earlier` и `div.ccwcw.later` элементы.  

:::image type="complex" source="../media/inspect-styles-glitch-display-animations.msft.png" alt-text="Инспектор анимации" lightbox="../media/inspect-styles-glitch-display-animations.msft.png":::
   Анимация с цветовым кодированием  
:::image-end:::  

## Изменение анимации  

Вы можете изменить анимацию с помощью инспектора анимации тремя способами.  

*   Длительность анимации.  
*   Временные интервалы для ключевых кадров.  
*   Время начала задержки.  
    
На приведенном ниже рисунке представлена исходная анимация.  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations.msft.png" alt-text="Инспектор анимации" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations.msft.png":::
   Исходная анимация перед изменением  
:::image-end:::  

Чтобы изменить длительность анимации, щелкните и перетащите первый или последний круг.  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations-shorter.msft.png" alt-text="Инспектор анимации" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations-shorter.msft.png":::
   Измененная длительность  
:::image-end:::  

Если анимация определяет любые правила для ключевого кадра, они будут представлены как белые внутренние круги.  Щелкните и перетащите один из них, чтобы изменить временные показатели для ключевого кадра.  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations-keyframe-modification.msft.png" alt-text="Инспектор анимации" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations-keyframe-modification.msft.png":::
   Измененный ключевой кадр  
:::image-end:::  

Чтобы добавить задержку для анимации, щелкните и перетащите ее в любое место за исключением кругов.  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations-delay.msft.png" alt-text="Инспектор анимации" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations-delay.msft.png":::
   Измененная задержка  
:::image-end:::  

## Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageAnimationSpeedButtonsIcon]: ../media/animation-speed-buttons-icon.msft.png  
[ImageReplayButtonIcon]: ../media/replay-button-icon.msft.png  

<!-- links -->  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/inspect-styles/animations) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
