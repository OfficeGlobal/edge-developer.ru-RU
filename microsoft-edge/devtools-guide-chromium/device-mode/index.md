---
description: Используйте виртуальные устройства в Microsoft Edge для создания веб-сайтов для мобильных устройств.
title: Эмуляция мобильных устройств в Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools, Эмуляция, устройство, Эмуляция, мобильный
ms.openlocfilehash: 8b636a20fcb1c55630009031ec8bf300624d03d7
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125106"
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

# Эмуляция мобильных устройств в Microsoft Edge DevTools  

Использование **эмуляции устройства** для оценки того, как страница выглядит и отвечает на мобильном устройстве.  Microsoft Edge DevTools предоставляет набор функций, которые помогут вам эмулировать мобильные устройства.  Коллекция включает следующие функции.  

*   [Имитация окна просмотра для мобильных устройств](#simulate-a-mobile-viewport)  
*   [Регулирование сети](#throttle-the-network-only)  
*   [Регулирование ЦП](#throttle-the-cpu-only)  
*   [Имитация географического положения](#override-geolocation)  
*   [Настройка ориентации](#set-orientation)  
*   [Установка строки агента пользователя](#set-user-agent-string)  

## Ограничения  

**Эмуляция устройства** — это [приближенная аппроксимация][WikiApproximation] внешнего вида и функций страницы на мобильном устройстве.  **Эмуляция устройства** фактически не запускает ваш код на мобильном устройстве.  Вместо этого вы имитируете взаимодействие с пользователем на мобильном устройстве или компьютере.  

Некоторые аспекты мобильных устройств не имитируются в DevTools.  Например, архитектура мобильных процессоров отличается от архитектуры компьютеров или процессоров для настольных ПК.  Если вы сомневаетесь, лучше использовать страницу на мобильном устройстве.  Используйте [удаленную отладку] [DevToolsRemoteDebugging], чтобы взаимодействовать с кодом страницы с компьютера, когда страница фактически выполняется на мобильном устройстве.  Вы можете просматривать, изменять, выполнять отладку или все четыре сеанса, пока вы не будете взаимодействовать с этим кодом.  Ваш компьютер может представлять собой записную книжку или настольный компьютер.  

## Имитация окна просмотра для мобильных устройств  

Нажмите кнопку **Переключить эмуляцию устройства**  \ ( ![ Переключить панель инструментов устройства ][ImageDeviceToolbarIcon] ) или щелкните **настроить DevTools** \ ( `...` \) > **эмуляцию устройства** , чтобы открыть пользовательский интерфейс, позволяющий имитировать окно просмотра для мобильных устройств.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="Панель инструментов &quot;устройства&quot;" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
    Панель инструментов "устройства"  
:::image-end:::  

По умолчанию панель инструментов устройства открывается в режиме отклика окна просмотра.  

### Режим окна просмотра с откликом  

Чтобы быстро проверить внешний вид страницы на нескольких размерах экрана, перетащите маркеры, чтобы изменить размер окна просмотра до нужных размеров.  Вы также можете ввести определенные значения в полях Ширина и высота.  На приведенном ниже рисунке задана ширина `626` и высота задана `516` .  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-handles-highlighted.msft.png" alt-text="Панель инструментов &quot;устройства&quot;" lightbox="../media/device-mode-toggle-device-toolbar-handles-highlighted.msft.png":::
    Дескрипторы для изменения размеров окна просмотра в отклике режима просмотра  
:::image-end:::  

#### Показать мультимедийные запросы  

Если вы определили на странице запросы мультимедиа, переходите к измерениям просмотра, в которых эти запросы мультимедиа вступают в силу, отображая точки останова в запросах мультимедиа над окном просмотра.  Нажмите кнопку **Дополнительные параметры**  >  , чтобы**отобразить запросы мультимедиа**.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-options-show-media-queries.msft.png" alt-text="Панель инструментов &quot;устройства&quot;" lightbox="../media/device-mode-toggle-device-toolbar-more-options-show-media-queries.msft.png":::
   **Показать мультимедийные запросы**  
:::image-end:::  

Выберите точку останова, чтобы изменить ширину окна просмотра таким образом, чтобы был запущен запрос мультимедиа.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-click-breakpoint.msft.png" alt-text="Панель инструментов &quot;устройства&quot;" lightbox="../media/device-mode-toggle-device-toolbar-click-breakpoint.msft.png":::
   Выбор точки останова для изменения ширины окна просмотра  
:::image-end:::  

#### Настройка типа устройства  

Используйте список **типов устройств** для имитации мобильного устройства или настольного устройства.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-type-list.msft.png" alt-text="Панель инструментов &quot;устройства&quot;" lightbox="../media/device-mode-toggle-device-toolbar-device-type-list.msft.png":::
   Список **типов устройств**  
:::image-end:::  

В приведенной ниже таблице описаны различия между доступными параметрами типа устройства.  Столбец «метод рендеринга» указывает, будет ли Microsoft Edge обрабатывать страницу в качестве окна просмотра на мобильном или рабочем столе.  Столбец значка курсора указывает на тип курсора, который отображается при наведении указателя на страницу.  Столбец, в котором запущены события, указывает на то, следует ли выполнять триггеры страницы `touch` или `click` события при взаимодействии со страницей.  

| Параметр | Метод отрисовки | Значок курсора | Инициированные события |  
|:--- |:--- |:--- |:--- |  
| Мобильные устройства | Мобильные устройства | Круг | Сенсорный ввод |  
| Мобильный – (без сенсорных устройств) | Мобильные устройства | Обычный |  нажмите  |  
| Desktop | Desktop | Обычный |  нажмите  |  
| Классическое приложение (касание) | Desktop | Круг | Сенсорный ввод |  

> [!NOTE]
> Если список **тип устройства** не отображается, выберите пункт **Дополнительные параметры**  >  **Добавить тип устройства**.  

### Режим просмотра на мобильном устройстве  

Чтобы смоделировать размеры определенного мобильного устройства, выберите нужное устройство из списка **устройств** .  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-list.msft.png" alt-text="Панель инструментов &quot;устройства&quot;" lightbox="../media/device-mode-toggle-device-toolbar-device-list.msft.png":::
   Список **устройств**  
:::image-end:::  

#### Поворот окна просмотра на альбомную ориентацию  

Протестируйте веб-страницу в альбомной ориентации.  

*   Чтобы повернуть окно просмотра на альбомную ориентацию, нажмите кнопку **повернуть** \ ( ![ повернуть ][ImageRotateIcon] \).  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-landscape.msft.png" alt-text="Панель инструментов &quot;устройства&quot;" lightbox="../media/device-mode-toggle-device-toolbar-landscape.msft.png":::
       Страница отображается в альбомной ориентации  
    :::image-end:::  
    
> [!NOTE]
> Кнопка **повернуть** исчезнет, если **панель инструментов на устройстве** является узкой.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="Панель инструментов &quot;устройства&quot;" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
   **Панель инструментов "устройства** "  
:::image-end:::  

Дополнительные сведения можно найти на странице [Настройка ориентации](#set-orientation).  

#### Показать рамку устройства  

Показывать рамку физического устройства вокруг окна просмотра, когда вы моделируете размеры определенного мобильного устройства, например iPhone 6.  

1.  Откройте **диалоговое окно Дополнительные параметры**.  
1.  Выберите пункт **Показать рамку устройства**.  

> [!NOTE]
> Если вы не видите рамку устройства для определенного устройства, это означает, что DevTools не имеет рисунка для этого параметра.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-option-show-device-frame.msft.png" alt-text="Панель инструментов &quot;устройства&quot;" lightbox="../media/device-mode-toggle-device-toolbar-option-show-device-frame.msft.png":::
         Показать рамку устройства  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-options-device-frame-iphone-6.msft.png" alt-text="Панель инструментов &quot;устройства&quot;" lightbox="../media/device-mode-toggle-device-toolbar-options-device-frame-iphone-6.msft.png":::
         Рамка устройства для iPhone 6  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

#### Добавление настраиваемого мобильного устройства  

Если необходимый параметр мобильного устройства отсутствует в списке по умолчанию, вы можете добавить настраиваемое устройство.  Чтобы добавить настраиваемое устройство, выполните указанные ниже действия.  

1.  Выберите список **устройств** > **изменить**.  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-list-edit.msft.png" alt-text="Панель инструментов &quot;устройства&quot;" lightbox="../media/device-mode-toggle-device-toolbar-device-list-edit.msft.png":::
       Нажмите кнопку **изменить** .  
    :::image-end:::  
    
1.  Выберите **Добавить настраиваемое устройство**.  
1.  На **эмулированных устройствах**введите имя устройства, ширину экрана и высоту экрана для настраиваемого устройства.  Поля « [отношение к пикселям][MDNWindowDevicePixelRatio]», « [строка агента пользователя][MDNUserAgent]» и « [тип устройства](#set-the-device-type) » являются необязательными.  Поле «Тип устройства» по умолчанию имеет значение **мобильный**.  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-settings-emulated-devices-add.msft.png" alt-text="Панель инструментов &quot;устройства&quot;" lightbox="../media/device-mode-toggle-device-toolbar-settings-emulated-devices-add.msft.png":::
       Создание настраиваемого устройства  
    :::image-end:::  
    
### Отображение линеек  

Если требуется измерение размеров экрана, вы можете использовать линейки для измерения размера экрана в пикселях.  Нажмите кнопку **Дополнительные параметры**  >  , чтобы отобразить**линейки** сверху и слева от окна просмотра.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-options-show-rulers.msft.png" alt-text="Панель инструментов &quot;устройства&quot;" lightbox="../media/device-mode-toggle-device-toolbar-options-show-rulers.msft.png":::
         Элемент меню для отображения линеек  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-rulers.msft.png" alt-text="Панель инструментов &quot;устройства&quot;" lightbox="../media/device-mode-toggle-device-toolbar-rulers.msft.png":::
         Линейки сверху и слева от окна просмотра  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### Изменение масштаба просмотра  

Для проверки внешнего вида страницы на нескольких уровнях масштабирования используйте в списке **масштаб** , чтобы увеличить или уменьшить масштаб.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-zoom.msft.png" alt-text="Панель инструментов &quot;устройства&quot;" lightbox="../media/device-mode-toggle-device-toolbar-zoom.msft.png":::
   **Масштаб**  
:::image-end:::  

## Регулирование сети и ЦП  

Для мобильных устройств часто используются ограничения сети и ЦП.  Убедитесь, что вы протестируете, как быстро загружается страница и как она реагирует на разные скорости в Интернете и ЦП.  

Регулирование сети и ЦП.  

1.  Выберите пункт **перерегулировать** список и измените стиль на " **средний" Мобильный** или **низкий уровень мобильного**.  
    *   **Мобильные видеосвязи** моделируются и заменяют `fast 3G` ЦП.  Это происходит четыре часа ниже, чем обычно.  
    *   С помощью низкоуровневых эмуляций на **мобильном устройстве** осуществляется `slow 3G` регулирование центрального процессора.  Оно не менее шести, чем обычно.  
    
Все регулировки зависят от нормальной работы ноутбука или настольного компьютера.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-throttle.msft.png" alt-text="Панель инструментов &quot;устройства&quot;" lightbox="../media/device-mode-toggle-device-toolbar-throttle.msft.png":::
   Список **регулирования** на панели инструментов устройства  
:::image-end:::  

> [!NOTE]
> Если **список регулирования** скрыт, **панель инструментов устройства** слишком мала.  Чтобы получить доступ к **списку регулирования**, увеличите ширину **панели инструментов устройства**.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="Панель инструментов &quot;устройства&quot;" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
   **Панель инструментов "устройства** "  
:::image-end:::  

### Регулирование только ЦП  

Чтобы перерегулировать только ЦП, а не сеть, выполните указанные ниже действия.

1.  Выберите панель " **производительность** " и нажмите кнопку " **Параметры** захвата ![ " (параметры записи ][ImageCaptureIcon] ).
1.  Выберите **ЦП**  >  **4X** или **6X замедление**.
    
    :::image type="complex" source="../media/device-mode-performance-cpu-throttle.msft.png" alt-text="Панель инструментов &quot;устройства&quot;" lightbox="../media/device-mode-performance-cpu-throttle.msft.png":::
       Список **ЦП** на панели " **производительность** "  
    :::image-end:::  
    
### Регулирование сети только  

Чтобы перерегулировать сеть, выполните указанные ниже действия.

1.  Выберите панель **Network (сеть** ).
1.  Выберите **онлайновый режим**  >  **3G** или **медленное 3G**.
    
    :::image type="complex" source="../media/device-mode-network-throttle.msft.png" alt-text="Панель инструментов &quot;устройства&quot;" lightbox="../media/device-mode-network-throttle.msft.png":::
       Список **регулирования** на панели "сеть"  
    :::image-end:::  
    
    Или выберите `Control` + `Shift` + `P` \ (Windows, Linux \) или `Command` + `Shift` + `P` \ (macOS \), чтобы открыть **меню команд**, введите `3G` и выберите **включить быстрое регулирование сети 3G** или **включить медленное регулирование сети 3G**.  
    
    :::image type="complex" source="../media/device-mode-command-menu-throttle.msft.png" alt-text="Панель инструментов &quot;устройства&quot;" lightbox="../media/device-mode-command-menu-throttle.msft.png":::
       **Меню команд**  
    :::image-end:::  
    
Вы также можете настроить регулирование сети на панели **Performance** .  

1.  Выберите **Параметры захвата** \ ( ![ Параметры захвата ][ImageCaptureIcon] ) и щелкните список **сетей** и измените стиль на " **Быстрый 3G** " или " **медленный 3G**".  
    
    :::image type="complex" source="../media/device-mode-performance-network-throttle.msft.png" alt-text="Панель инструментов &quot;устройства&quot;" lightbox="../media/device-mode-performance-network-throttle.msft.png":::
       Настройка регулирования сети с помощью панели " **производительность** "  
    :::image-end:::  
    
## Переопределение геолокации  

:::row:::
   :::column span="":::
      Если страница зависит от данных географического расположения на мобильном устройстве, для правильного отображения укажите различные географическое положение с помощью пользовательского интерфейса переопределения географического расположения.  

      1.  Нажмите кнопку **Настройка и** выберите пункт DevTools \ ( `...` \) > **другие инструменты**  >  **датчики**.  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png" alt-text="Панель инструментов &quot;устройства&quot;" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png":::
         **Датчики** для географического местоположения  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      1.  Открытие меню команд.  
          *   Выберите `Control` + `Shift` + `P` \ (Windows, Linux \) или `Command` + `Shift` + `P` \ (macOS \).  
      1. Введите текст `Sensors` и выберите пункт **Показать датчики**.  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png" alt-text="Панель инструментов &quot;устройства&quot;" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png":::
         **Показать датчики** для географического положения  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

На панели **Sensors (датчики** ) вы можете выбрать одно из расположений, указанных в DevTools, с помощью раскрывающегося меню **Расположение** .  Чтобы ввести другое расположение, выберите пункт **другие...** и введите координаты вашего собственного местоположения.  Чтобы протестировать страницу в состоянии ошибки, если сведения о расположении недоступны, выберите пункт **расположение недоступно**.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-sensors-tokyo.msft.png" alt-text="Панель инструментов &quot;устройства&quot;" lightbox="../media/device-mode-toggle-device-toolbar-sensors-tokyo.msft.png":::
    Панель « **датчики** » с выбранным расположением.  
:::image-end:::

## Настройка ориентации  

:::row:::
   :::column span="":::
      Если страница зависит от сведений о ориентации на мобильном устройстве для правильной обработки, откройте пользовательский интерфейс ориентации.  

      1.  Нажмите кнопку **Настройка и** выберите пункт DevTools \ ( `...` \) > **другие инструменты**  >  **датчики**.  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png" alt-text="Панель инструментов &quot;устройства&quot;" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png":::
         **Датчики** для ориентации  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      1.  Открытие меню команд.  
          *   Выберите `Control` + `Shift` + `P` \ (Windows, Linux \) или `Command` + `Shift` + `P` \ (macOS \).  
      1. Введите текст `Sensors` и выберите пункт **Показать датчики**.  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png" alt-text="Панель инструментов &quot;устройства&quot;" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png":::
         **Отображение датчиков** для ориентации  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

На панели **Sensors (датчики** ) можно выбрать стандартную ориентацию в раскрывающемся меню **ориентация** .  Чтобы задать собственную ориентацию, выберите пункт **Настраиваемая ориентация**и введите значения [альфа][MDNDeviceOrientaitonAlpha], [бета][MDNDeviceOrientaitonBeta]и [гамма][MDNDeviceOrientaitonGamma] .  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-sensors-tokyo-portrait-upside-down.msft.png" alt-text="Панель инструментов &quot;устройства&quot;" lightbox="../media/device-mode-toggle-device-toolbar-sensors-tokyo-portrait-upside-down.msft.png":::
    Параметры **ориентации** на панели **датчиков**  
:::image-end:::  

## Установка строки агента пользователя  

:::row:::
   :::column span="":::
      Если страница зависит от строки агента пользователя на мобильном устройстве для правильного отображения, используйте панель " **условия сети** " для предоставления разных строк пользовательского агента.  
      
      1.  Нажмите кнопку **Настройка и** выберите пункт DevTools \ ( `...` \), > **Дополнительные инструменты**,  >  **сетевые условия**.  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-network-conditions.msft.png" alt-text="Панель инструментов &quot;устройства&quot;" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-network-conditions.msft.png":::
         Элемент " **условия сети** " в меню " **другие инструменты** "  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      1.  Открытие меню команд.  
          *   Выберите `Control` + `Shift` + `P` \ (Windows, Linux \) или `Command` + `Shift` + `P` \ (macOS \).  
      1. Введите текст `Network conditions` и выберите пункт **Показать условия сети**.  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-network-conditions.msft.png" alt-text="Панель инструментов &quot;устройства&quot;" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-network-conditions.msft.png":::
         **Показывать условия сети**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Рядом с **агентом пользователя**снимите флажок **выбрать автоматически** .  Затем выберите **Custom...** , чтобы выбрать из списка предварительно заданных строк агента пользователя.  Чтобы ввести собственную строку агента пользователя, введите ее в поле **введите настраиваемый агент пользователя**.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-network-conditions-macos.msft.png" alt-text="Панель инструментов &quot;устройства&quot;" lightbox="../media/device-mode-toggle-device-toolbar-network-conditions-macos.msft.png":::
    Установка строки агента пользователя в Microsoft EDGE на macOS  
:::image-end:::  

## Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageCaptureIcon]: ../media/capture-settings-icon.msft.png  
[ImageDeviceToolbarIcon]: ../media/toggle-device-toolbar-dark-icon.msft.png  
[ImageRotateIcon]: ../media/rotate-dark-icon.msft.png  

<!-- links -->  

<!--[DevToolsCommunity]: ../index.md#community "Join the DevTools community | Microsoft Docs"  -->
[DevToolsRemoteDebugging]: .. /Remote-Debugging/index.md "Начало работы с удаленными отладочными устройствами Android | Microsoft Docs»  

[MDNWindowDevicePixelRatio]: https://developer.mozilla.org/docs/Web/API/Window/devicePixelRatio "Window. devicePixelRatio | MDN"  
[MDNUserAgent]: https://developer.mozilla.org/docs/Glossary/User_agent "Агент пользователя | MDN"  
[MDNDeviceOrientaitonAlpha]: https://developer.mozilla.org/en-US/docs/Web/API/DeviceOrientationEvent/alpha "DeviceOrientationEvent. Alpha | MDN"  
[MDNDeviceOrientaitonBeta]: https://developer.mozilla.org/en-US/docs/Web/API/DeviceOrientationEvent/beta "DeviceOrientationEvent. бета | MDN"  
[MDNDeviceOrientaitonGamma]: https://developer.mozilla.org/en-US/docs/Web/API/DeviceOrientationEvent/gamma "DeviceOrientationEvent. гамма | MDN"  

[WikiApproximation]: https://en.wikipedia.org/wiki/Order_of_approximation#First-order "Порядок приближения — первый-заказ — Википедии"  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/device-mode/index) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
