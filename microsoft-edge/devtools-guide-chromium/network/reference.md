---
description: Полный справочник по функциям панели DevTools сети Microsoft Edge.
title: Справочник по анализу сети
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 38570e6d196314aa6315a34f0b8b1b0b0d740c91
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993620"
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

# Справочник по анализу сети  

Ознакомьтесь с новыми способами для анализа того, как страница загружается в этой полной версии справочника по функциям сетевого анализа Microsoft Edge DevTools.  

<!--
> [!NOTE]
> This reference is based on Microsoft Edge 58.  If you use another version of Microsoft Edge, the UI, and features of DevTools may be different.  Check `edge://help` to see what version of Microsoft Edge you are running.  
-->

## Запись сетевых запросов  

По умолчанию DevTools записывает все сетевые запросы на панели "сеть", пока не откроете DevTools.  

:::image type="complex" source="../media/network-network-panel.msft.png" alt-text="Панель сеть" lightbox="../media/network-network-panel.msft.png":::
   Рисунок 1: панель " **сеть** "  
:::image-end:::  

### Прекращение записи сетевых запросов  

Чтобы остановить запись запросов, выполните указанные ниже действия.  

1.  Выберите **остановить запись** остановка записи сетевого журнала ![ ][ImageRecordOnIcon] на панели **сеть** .  Оно превращается в серый, чтобы показать, что DevTools больше не записывает запросы.  
1.  Нажимайте клавиши `Control` + `E` \ (Windows \) или `Command` + `E` \ (macOS \), пока фокус находится на панели " **сеть** ".  

### Очистка запросов  

**Clear** ![ ][ImageClearIcon] Чтобы очистить все запросы из таблицы "запросы", на панели "сеть" нажмите кнопку Clear Clear.  

:::image type="complex" source="../media/network-network-clear-button.msft.png" alt-text="Кнопка очистить" lightbox="../media/network-network-clear-button.msft.png":::
   Рисунок 2: кнопка " **очистить** "  
:::image-end:::  

### Сохранение запросов на загрузку страниц  

Для сохранения запросов на страницах загрузок на панели "сеть" установите флажок **сохранить журнал** .  DevTools сохраняет все запросы, пока не отключайте параметр **сохранить журнал**.  

:::image type="complex" source="../media/network-network-preserve-log.msft.png" alt-text="Флажок сохранить журнал" lightbox="../media/network-network-preserve-log.msft.png":::
   Рисунок 3: флажок " **сохранить журнал** "  
:::image-end:::  

### Захват снимков экрана при загрузке страницы  

Выведите снимки экрана, чтобы проанализировать, какие пользователи видят при ожидании загрузки страницы.  

Чтобы включить снимки экрана, нажмите кнопку **Параметры сети** и выберите команду **захватить снимки экрана** на панели " **сеть** ".  

Обновите страницу, когда фокус находится на панели " **сеть** ", чтобы захватить снимки экрана.  

После захвата снимка экрана вы взаимодействуете с ним следующими способами.  

*   Наведите указатель мыши на снимок экрана, чтобы просмотреть точку, в которой был записан снимок экрана.  На панели **обзора** появится желтая линия.  
*   Щелкните эскиз экрана, чтобы отфильтровать все запросы, произошедшие после захвата снимка экрана.  
*   Дважды щелкните эскиз, чтобы увеличить его.  

:::image type="complex" source="../media/network-network-screenshot-hover.msft.png" alt-text="Наведение указателя на снимок экрана" lightbox="../media/network-network-screenshot-hover.msft.png":::
   Рисунок 4: наведение указателя на снимок экрана  
:::image-end:::  

<!--  ### Replay XHR request  -->

<!--  To replay an XHR request, hover on the request in the Requests table, open the contextual menu \(right-click\), and select **Replay XHR**.  -->

<!--  
:::image type="complex" source="../media/network-replay-xhr.msft.png" alt-text="Selecting Replay XHR" lightbox="../media/network-replay-xhr.msft.png":::
   Old Figure 5:  Selecting Replay XHR  
:::image-end:::  
-->  

## Изменение поведения при загрузке  

### Эмуляция первого времени посетителя с помощью отключения кэша браузера  

Чтобы эмулировать, как пользователь попытается получить доступ к сайту, установите флажок **отключить кэш** .  DevTools отключает кэш браузера.  Это более точно эмулирует взаимодействие с пользователем при первом запуске, так как запросы размещаются из кэша браузера на повторных посещениях.  

:::image type="complex" source="../media/network-network-disable-cache-checkbox.msft.png" alt-text="Флажок отключить кэш" lightbox="../media/network-network-disable-cache-checkbox.msft.png":::
   Рисунок 5: флажок **отключения кэша**  
:::image-end:::  

#### Отключение кэша браузера из денежных ящиков условий сети  

Если вы хотите отключить кэш при работе с другими панелями DevTools, используйте денежные ящики условия сети.  

1.  Откройте денежный ящик **условий сети** .  
1.  Установите или снимите флажок **отключить кэш** .  

<!--todo: add network condition section when available -->  

### Очистка кэша браузера вручную  

Чтобы вручную очистить кэш браузера в любое время, откройте контекстное меню (щелкните правой кнопкой мыши в любом месте таблицы запросов и выберите пункт **очистить кэш браузера**).  

:::image type="complex" source="../media/network-network-clear-browser-cache.msft.png" alt-text="Выбор очистки кэша браузера" lightbox="../media/network-network-clear-browser-cache.msft.png":::
   Рисунок 6: выбор **очистки кэша браузера**  
:::image-end:::  

### Эмуляция в автономном режиме  

Новый класс веб-приложений, именуемых [прогрессивными веб-приложениями][DevtoolsProgressiveWebApps], не будет работать в автономном режиме с помощью **обслуживания сотрудников**.  Возможно, вам будет удобно быстро смоделировать устройство, которое не имеет подключения к данным, при построении такого типа приложения.  

<!--[ServiceWorkers]: /web/fundamentals/getting-started/primers/service-workers  -->

Щелкните раскрывающееся меню **онлайн** , выполните поиск в разделе " **стили**", а затем выберите пункт в **автономном режиме** , чтобы имитировать полностью автономный режим работы сети.  

:::image type="complex" source="../media/network-network-offline-dropdown.msft.png" alt-text="Раскрывающееся меню автономный режим" lightbox="../media/network-network-offline-dropdown.msft.png":::
   Рисунок 7: раскрывающийся список в **автономном режиме**  
:::image-end:::  

### Эмуляция медленных сетевых подключений  

Эмуляция медленной сети 3G, Fast 3G и других скоростей соединения из раскрывающегося меню **Online** .  

:::image type="complex" source="../media/network-network-throttling-menu.msft.png" alt-text="Раскрывающееся меню регулирования" lightbox="../media/network-network-throttling-menu.msft.png":::
   Рисунок 8: раскрывающееся меню **регулирования**  
:::image-end:::  

Вы можете выбрать один из самых разнообразных наборов параметров, например медленной или скорости 3G.  Вы также можете добавить собственные пользовательские стили, открыв меню регулирования и выбрав пункт **настраиваемое**  >  **Добавление**.  

DevTools отображает значок предупреждения рядом с вкладкой **сеть** , чтобы напомнить вам, что регулирование разрешено.  

#### Эмуляция медленных сетевых подключений из денежных ящиков условий сети  

Если вы хотите регулировать сетевое соединение при работе с другими панелями DevTools, используйте денежные ящики условий сети.  

1.  Откройте денежный ящик **условий сети** .  
1.  Выберите нужную скорость соединения в меню **регулирования** .  

<!--todo: add network condition section when available -->  

### Очистка файлов cookie браузера вручную  

Чтобы вручную удалить cookie-файлы браузера в любое время, откройте контекстное меню (щелкните правой кнопкой мыши, где угодно в таблице запросов и выберите команду **Очистить cookie-файлы браузера**).  

:::image type="complex" source="../media/network-network-clear-browser-cookies.msft.png" alt-text="Выбор очистки cookie-файлов браузера" lightbox="../media/network-network-clear-browser-cookies.msft.png":::
   Рисунок 9: выбор пункта **"Удалить cookie-файлы браузера"**  
:::image-end:::  

### Переопределение агента пользователя  

Чтобы вручную переопределить агент пользователя, выполните указанные ниже действия.  

1.  Откройте денежный ящик **условий сети** .  
1.  Снимите флажок **автоматически**.  
1.  Выберите в меню пункт агента пользователя или введите его в текстовом поле.  

<!--todo: add network condition section when available -->  

## Фильтрация запросов  

### Фильтрация запросов по свойствам  

С помощью текстового поля **Фильтр** можно отфильтровать запросы по свойствам, таким как домен или размер запроса.  

Если надпись не отображается, возможно, область Фильтры скрыта.  
Посмотрите [скрыть область фильтров](#hide-the-filters-pane).  

:::image type="complex" source="../media/network-network-filters-textbox.msft.png" alt-text="Текстовое поле фильтр" lightbox="../media/network-network-filters-textbox.msft.png":::
   Рисунок 10: текстовое поле " **Фильтр** "  
:::image-end:::  

Вы можете использовать несколько свойств одновременно, разделяя каждое свойство пробелами.  Например, `mime-type:image/png larger-than:1K` отображает все PNGs, размер которых больше 1 Кбайт.  Эти фильтры с несколькими свойствами эквивалентны `AND` операциям.  `OR` операции в настоящее время не поддерживаются.  

Полный список поддерживаемых свойств.  

| Свойство | Сведения |  
|:--- | :--- |  
| `domain` | Отображать только ресурсы из указанного домена.  Вы можете использовать подстановочный знак "\ `*` ", чтобы включить несколько доменов.  Например, `*.com` отображаются ресурсы из всех доменных имен, которые заканчиваются на `.com` .  DevTools заполняет раскрывающееся меню автозаполнения всеми найденными доменами. |  
| `has-response-header` | Показать ресурсы, содержащие указанный заголовок HTTP-ответа.  DevTools заполняет раскрывающийся список автозавершения всеми найденными заголовками ответов. |  
| `is` | Используется `is:running` для поиска `WebSocket` ресурсов. |  
| `larger-than` | Показать ресурсы, размер которых больше указанного (в байтах).  Установка значения эквивалентно значению свойства `1000` `1k` . |  
| `method` | Показать ресурсы, полученные с помощью указанного типа метода HTTP.  DevTools заполнит раскрывающийся список всех обнаруженных методов HTTP. |  
| `mime-type` | Показать ресурсы указанного типа MIME.  DevTools наполняет в раскрывающемся списке все обнаруженные типы MIME. |  
| `mixed-content` | Показать все смешанные ресурсы контента \ ( `mixed-content:all` \) или только те из них, которые в данный момент отображаются \ ( `mixed-content:displayed` \). |  
| `scheme` | Показать ресурсы, полученные через незащищенные HTTP \ ( `scheme:http` \) или защищенные HTTPS \ ( `scheme:https` \). |  
| `set-cookie-domain` | Показать ресурсы с `Set-Cookie` заголовком с `Domain` атрибутом, соответствующим указанному значению.  DevTools заполняет Автозаполнение всеми обнаруженными ими доменами cookie. |  
| `set-cookie-name` | Показать ресурсы с `Set-Cookie` заголовком с именем, которое соответствует указанному значению.  DevTools заполняет Автозаполнение всеми именами cookie-файлов, которые были обнаружены. |  
| `set-cookie-value` | Показать ресурсы с `Set-Cookie` заголовком со значением, соответствующим указанному значению.  DevTools заполняет Автозаполнение всеми обнаруженными значениями cookie-файлов. |  
| `status-code` | Показать только ресурсы, для которых код состояния HTTP соответствует указанному коду.  DevTools заполнит раскрывающееся меню автозаполнения, содержащее все найденные коды состояния. |  

### Фильтрация запросов по типу  

Чтобы отфильтровать запросы по типу запроса, выберите один из указанных ниже кнопок: **XHR**, **JS**, **CSS**, **img**, **Media**, **Font**, **doc**, **WS** \ (WebSocket \), **Манифест**или **другой** \ (любой другой тип, не указанный здесь) на панели "сеть".  

Если эти кнопки не отображаются, возможно, область фильтров скрыта.  
Посмотрите [скрыть область фильтров](#hide-the-filters-pane).  

Чтобы включить множественные фильтры типов одновременно, удерживайте клавишу `Control` \ (Windows \) или `Command` \ (macOS \) и выберите.  

:::image type="complex" source="../media/network-network-type-filters.msft.png" alt-text="Использование фильтров типов для отображения ресурсов JS, CSS и документов" lightbox="../media/network-network-type-filters.msft.png":::
   На рисунке 11: использование фильтров типов для отображения ресурсов JS, CSS и документов  
:::image-end:::  

### Фильтрация запросов по времени  

Чтобы отобразить только те запросы, которые были активны в течение этого времени, выберите и перетащите его влево или вправо в области "Обзор".  Фильтр является инклюзивным.  Отображается любой запрос, который был активен в течение выбранного периода времени.  

:::image type="complex" source="../media/network-network-overview-filter.msft.png" alt-text="Фильтрация запросов, которые неактивны вокруг 300ms" lightbox="../media/network-network-overview-filter.msft.png":::
   Рис. 12: Фильтрация запросов, которые неактивны вокруг 300ms  
:::image-end:::  

### Скрыть URL-адреса данных  

[URL-адреса данных][MDNHTTPDataURIs] — это небольшие файлы, внедренные в другие документы.  Любой запрос, который начинается с адреса в таблице запросов, `data:` — это URL-адрес данных.  

Установите флажок **скрыть URL-адреса данных** , чтобы скрыть запросы.  

:::image type="complex" source="../media/network-network-hide-data-urls.msft.png" alt-text="Флажок скрыть URL-адреса данных" lightbox="../media/network-network-hide-data-urls.msft.png":::
   Рисунок 13: флажок **скрыть URL-адреса данных**  
:::image-end:::  

## Запросы сортировки  

По умолчанию запросы в таблице запросов сортируются по времени запуска, но вы можете отсортировать таблицу с помощью других условий.  

### Сортировка по столбцам  

Выберите верхний колонтитул любого столбца в списке запросы для сортировки запросов по этому столбцу.  

### Этап сортировки по действию  

Чтобы изменить способ сортировки запросов, наведите указатель мыши на заголовок таблицы запросы, откройте контекстное меню, наведите указатель мыши на пункт **Каскад**и выберите один из следующих вариантов.  

*   **Время начала**.  Первый инициированный запрос находится наверху.  
*   **Время отклика**.  Первый запрос, загруженный в верхней части экрана.  
*   **Время окончания**.  Первый завершенный запрос вверху.  
*   **Общая длительность**.  Запрос с наиболее короткой установкой подключения и запросом и ответом в начале.  
*   **Задержка**.  Запрос, который ожидает наиболее короткий момент ответа, находится наверху.  

В этих описаниях предполагается, что каждый из вариантов имеет приоритет от кратчайшего к наиболее продолжительному.  Если выбрать верхний колонтитул столбца **каскадом** , порядок будет изменен на противоположный.  

:::image type="complex" source="../media/network-network-waterfall-total-duration.msft.png" alt-text="Сортировка каскадом по общей длительности" lightbox="../media/network-network-waterfall-total-duration.msft.png":::
   Рисунок 14: Сортировка каскадом по общей длительности \ (светлая часть каждого элемента обходуется временем ожидания, а темная часть — это время, затраченное на загрузку байтов)  
:::image-end:::  

## Анализ запросов  

Пока открыто окно DevTools, все запросы будут регистрироваться на панели "сеть".  
Проанализируйте запросы с помощью панели "сеть".  

### Просмотр журнала запросов  

С помощью таблицы запросы можно просмотреть журнал всех запросов, выполненных, когда DevTools открыт.  При выборе или наведении указателя мыши на запросы открывается больше сведений о каждом элементе.  

:::image type="complex" source="../media/network-network-requests-table.msft.png" alt-text="Таблица запросов" lightbox="../media/network-network-requests-table.msft.png":::
   Рис. 15: таблица запросы  
:::image-end:::  

По умолчанию в таблице запросов отображаются следующие столбцы.  

*   **Имя**.  Имя или идентификатор ресурса.  
*   **Состояние**.  Код состояния HTTP.  
*   **Тип**.  Тип MIME запрашиваемого ресурса.  
*   **Инициатор**.  Следующие объекты или процессы инициируют запросы:  
    *   **Средство синтаксического анализа**.  Средство синтаксического анализа HTML для Microsoft Edge.  
    *   **Redirect (перенаправление**).  Переадресация HTTP.  
    *   **Сценарий**.  Функция JavaScript.  
    *   **Другие**.  Другие процессы или действия, например переход на страницу с помощью ссылки или ввод URL-адреса в адресную строку.  
*   **Размер**.  Объединенный размер заголовков ответа и текст ответа, доставленный сервером.  
*   **Time (время**).  Общая продолжительность от начала запроса до получения последнего байта в ответе.  
*   [**Каскадом**](#view-the-timing-of-requests-in-relation-to-one-another).  Визуальная декомпозиция мероприятия для каждого запроса.  

#### Добавление и удаление столбцов  

Наведите указатель мыши на заголовок таблицы запросы, откройте контекстное меню (щелкните правой кнопкой мыши \) и выберите один из вариантов, чтобы скрыть или отобразить его.  Параметры, отображаемые в данный момент, отмечены флажками рядом с каждым элементом.  

:::image type="complex" source="../media/network-network-requests-add-column.msft.png" alt-text="Добавление столбца в таблицу запросы" lightbox="../media/network-network-requests-add-column.msft.png":::
   Рисунок 16: Добавление столбца в таблицу "запросы"  
:::image-end:::  

#### Добавление настраиваемых столбцов  

Чтобы добавить настраиваемый столбец в таблицу запросы, наведите указатель мыши на заголовок таблицы запросы, откройте контекстное меню (щелкните правой кнопкой мыши \) и выберите **заголовки ответов**  >  .**Управление столбцами заголовков**.  

:::image type="complex" source="../media/network-network-requests-add-custom.msft.png" alt-text="Добавление настраиваемого столбца в таблицу запросы" lightbox="../media/network-network-requests-add-custom.msft.png":::
   Рисунок 17: Добавление настраиваемого столбца в таблицу "запросы"  
:::image-end:::  

### Просмотр времени связи между запросами друг на друга  

Используйте Каскад, чтобы просмотреть время связи между запросами друг с другом.  
По умолчанию каскадом упорядочиваются по времени начала запросов.  
Таким образом, запросы, которые раньше приступили к началу, чем те, которые находятся дальше по правому краю.  

Чтобы увидеть различные способы сортировки каскадов, просмотрите [фазу сортировки по действию](#sort-by-activity-phase) .  

:::image type="complex" source="../media/network-network-requests-waterfall.msft.png" alt-text="Столбец Каскад на панели запросы" lightbox="../media/network-network-requests-waterfall.msft.png":::
   Рисунок 18: столбец "Каскад" на панели " **запросы** "  
:::image-end:::  

<!-- ### Analyze the frames of a WebSocket Connection  -->

<!--To view the frames of a WebSocket connection:  

1.  Select the URL of the WebSocket connection, under the **Name** column of the Requests table.  
1.  Select the **Frames** tab.  The table shows the last 100 frames.  

To refresh the table, re-select the name of the WebSocket connection under the **Name** column of the Requests table.  -->

<!--
:::image type="complex" source="../media/network-frames.msft.png" alt-text="The Frames tab" lightbox="../media/network-frames.msft.png":::
   Old Figure 20:  The **Frames** tab  
:::image-end:::  
-->

<!--The table contains three columns:  

*   **Data**.  The message payload.  If the message is plain text, it is displayed here.  For binary opcodes, this column displays the name and code of the opcode.  The following opcodes are supported: Continuation Frame, Binary Frame, Connection Close Frame, Ping Frame, and Pong Frame.  
*   **Length**.  The length of the message payload, in bytes.  
*   **Time**.  The time when the message was received or sent.  -->

<!--Messages are color-coded according to their type:  

*   Outgoing text messages are light-green.  
*   Incoming text messages are white.  
*   WebSocket opcodes are light-yellow.  
*   Errors are light-red.  -->

### Предварительный просмотр тела ответа  

Чтобы предварительно просмотреть текст ответа, выполните указанные ниже действия.  

1.  Выберите URL-адрес запроса в столбце " **имя** " таблицы "запросы".  
1.  Откройте вкладку **Предварительный просмотр** .  

Эта вкладка особенно полезна для просмотра изображений.  

:::image type="complex" source="../media/network-network-resources-preview.msft.png" alt-text="Вкладка "предварительный просмотр"" lightbox="../media/network-network-resources-preview.msft.png":::
   На рисунке 19: вкладка " **Предварительный просмотр** "  
:::image-end:::  

### Просмотр текста ответа  

Чтобы просмотреть текст ответа на запрос, выполните указанные ниже действия.  

1.  Выберите URL-адрес запроса в столбце " **имя** " таблицы "запросы".  
1.  Откройте вкладку **ответ** .  

:::image type="complex" source="../media/network-network-resources-response.msft.png" alt-text="Вкладка "ответ"" lightbox="../media/network-network-resources-response.msft.png":::
   Рисунок 20. Вкладка " **ответ** "  
:::image-end:::  

### Просмотр заголовков HTTP  

Чтобы просмотреть данные заголовка HTTP для запроса, выполните указанные ниже действия.  

1.  Выберите URL-адрес запроса в столбце " **имя** " таблицы "запросы".  
1.  Откройте вкладку **заголовки** .  

:::image type="complex" source="../media/network-resources-headers.msft.png" alt-text="Вкладка "заголовки"" lightbox="../media/network-resources-headers.msft.png":::
   Рисунок 21: вкладка " **заголовки** "  
:::image-end:::  

#### Просмотр источника заголовков HTTP  

По умолчанию на вкладке заголовки отображаются имена заголовков в алфавитном порядке.  Чтобы просмотреть имена HTTP-заголовков в том порядке, в котором они были получены:  

1.  Открытие вкладки " **заголовки** " для запроса, который вас интересует.  См.: [Просмотр заголовков HTTP](#view-http-headers).  
1.  Нажмите кнопку **источник**, рядом с разделом **заголовок запроса** или **заголовок ответа** .  

### Просмотр параметров строки запроса  

Чтобы просмотреть параметры строки запроса URL-адреса в удобочитаемом формате, выполните указанные ниже действия.  

1.  Открытие вкладки " **заголовки** " для запроса, который вас интересует.  См.: [Просмотр заголовков HTTP](#view-http-headers).  
1.  Перейдите к разделу **Параметры строки запроса** .  

:::image type="complex" source="../media/network-network-resources-headers-query-string-parameters.msft.png" alt-text="Раздел "параметры строки запроса"" lightbox="../media/network-network-resources-headers-query-string-parameters.msft.png":::
   Рис. 22: раздел " **Параметры строки запроса** "  
:::image-end:::  

#### Просмотр источника параметров строки запроса  

Чтобы просмотреть источник параметра строки запроса для запроса:  

1.  Перейдите к разделу Параметры строки запроса.  Просмотрите [Параметры строки запроса на просмотр](#view-query-string-parameters).  
1.  Нажмите кнопку **Просмотр источника**.  

#### Просмотр строковых параметров запроса в кодировке URL  

Чтобы просмотреть параметры строки запроса в удобочитаемом формате, но с сохранением кодировки, выполните указанные ниже действия.  

1.  Перейдите к разделу Параметры строки запроса.  Просмотрите [Параметры строки запроса на просмотр](#view-query-string-parameters).  
1.  Выберите команду **Просмотреть закодированный URL-адрес**.  

### Просмотр файлов cookie  

Чтобы просмотреть cookie-файлы, отправленные в заголовке HTTP запроса, выполните указанные ниже действия.  

1.  Выберите URL-адрес запроса в столбце " **имя** " таблицы "запросы".  
1.  Перейдите на вкладку " **cookie** ".  

<!--See [Fields][ManageDataCookiesFields] for a description of each of the columns.  -->

<!--[ManageDataCookiesFields]: manage-data/cookies#fields  -->
<!--TODO: add link when section is available -->

:::image type="complex" source="../media/network-network-resources-cookies.msft.png" alt-text="Вкладка "cookie"" lightbox="../media/network-network-resources-cookies.msft.png":::
   Рис. 23: вкладка "cookie"  
:::image-end:::  

### Просмотр разбиения по времени для запроса  

Чтобы просмотреть межвременную разбивку запроса, выполните указанные ниже действия.  

1.  Выберите URL-адрес запроса в столбце " **имя** " таблицы "запросы".  
1.  Откройте вкладку **время** .  

Дополнительные сведения можно найти в разделе [Предварительный просмотр разбивки времени](#preview-a-timing-breakdown) для доступа к данным.  

Дополнительные сведения о каждой из фаз, которые можно увидеть на вкладке время, приведены в разделе [этапы разбиения по времени](#timing-breakdown-phases-explained) .  

:::image type="complex" source="../media/network-network-resources-timing.msft.png" alt-text="Вкладка время" lightbox="../media/network-network-resources-timing.msft.png":::
   Рисунок 24: вкладка **время**  
:::image-end:::  

Дополнительные сведения о каждой из фаз.  

Другие способы доступа к этому представлению можно найти в разделе [Просмотр временных интервалов](#view-the-timing-breakdown-of-a-request) .  

#### Предварительный просмотр разбивки по времени  

Чтобы просмотреть сведения о разбиении по времени для запроса, наведите указатель мыши на запись запроса в столбце **Каскад** таблицы запросы.  

Ознакомьтесь [со](#view-the-timing-breakdown-of-a-request) сведениями о том, как получить доступ к данным, которые не требуют наведения мыши, в запросе.  

:::image type="complex" source="../media/network-network-resources-waterfall-hover.msft.png" alt-text="> предварительный просмотр разбиения по времени для запроса" lightbox="../media/network-network-resources-waterfall-hover.msft.png":::
   Рис. 25: предварительный просмотр разбиения по времени для запроса  
:::image-end:::  

#### Описание этапов разделения времени  

Дополнительные сведения о каждой из фаз, которые можно увидеть на вкладке **время** .  

*   **Очереди**.  Браузер помещает запросы в очередь в следующих случаях:  
    *   Существуют запросы с более высокими приоритетами.  
    *   Для этого происхождения уже открыто шесть подключений TCP, что является ограничением.  Применимо только к HTTP/1.0 и HTTP/1.1.  
    *   Браузер временно выделяет место в кэше на диске.  
*   **Ожидание**.  Запрос может быть остановлен в любой из причин, описанных в разделе **очереди**.  
*   **Поиск DNS**.  Браузер разрешает IP-адрес запроса.  
*   **Начальное соединение**.  Браузер устанавливает подключение, в том числе подтверждения TCP, повторы TCP и согласование SSL.
*   **Согласование прокси-сервера**.  Браузер согласовывает запрос с [прокси-сервером][WikiProxyServer].  
*   **Запрос отправлен**.  Запрос отправляется.  
*   **Подготовка ServiceWorker**.  Браузер запускает сервисный рабочий процесс.  
*   **Запросите ServiceWorker**.  Запрос отправляется сотруднику службы.  
*   **Ожидание \ (TTFB \)**.  Браузер ожидает первый байт ответа.  TTFB означает время для первого байта.  Это время включает 1 круговый путь задержки и время, затраченное сервером на подготовку ответа.  
*   **Загрузка содержимого**.  Браузер получает ответ.  
*   **Получение push-уведомлений**.  Браузер получает данные для этого ответа через HTTP/2 серверную извещающую передачу.  
*   **Чтение push-уведомлений**.  Браузер читает локальные данные, полученные ранее.  

### Просмотр инициаторов и зависимостей  

Чтобы просмотреть инициаторы и зависимости запроса, удерживайте `Shift` и наведите указатель мыши на запрос в таблице запросы.  DevTools цвета: инициаторы отображаются зеленым цветом, а зависимости — красным.  

:::image type="complex" source="../media/network-network-resources-initiators-dependencies.msft.png" alt-text="Просмотр инициаторов и зависимостей запроса" lightbox="../media/network-network-resources-initiators-dependencies.msft.png":::
   Рис. 26: Просмотр инициаторов и зависимостей запроса  
:::image-end:::  

Когда таблица запросов упорядочивается в хронологическом порядке, первым зеленым запросом над ним, который вы наводите, является инициатор зависимости.  Если над ним появится еще один зеленый запрос, этот более высокий запрос является инициатором инициатора.  И так далее.  

### Просмотр событий загрузки  

DevTools отображает время показа `DOMContentLoaded` `load` событий в нескольких местах на панели "сеть".  `DOMContentLoaded`Событие окрашивается синим цветом, а `load` событие — красным.  

:::image type="complex" source="../media/network-network-requests-load-events.msft.png" alt-text="Расположение событий DOMContentLoaded и Load на панели "сеть"" lightbox="../media/network-network-requests-load-events.msft.png":::
   На рисунке 27 показано расположение событий " `DOMContentLoaded` и" `load` на панели "сеть".  
:::image-end:::  

### Просмотр общего числа запросов  

Общее количество запросов можно найти в области сводки в нижней части панели "сеть".  

> [!CAUTION]
> Этот номер отслеживает только те запросы, которые были зарегистрированы с момента открытия DevTools.  Если при открытии DevTools возникли другие запросы, эти запросы не учитываются.  

:::image type="complex" source="../media/network-network-total-requests.msft.png" alt-text="Общее количество запросов с момента открытия DevTools" lightbox="../media/network-network-total-requests.msft.png":::
   Рис. 28: общее количество запросов с момента открытия DevTools  
:::image-end:::  

### Просмотр общего объема загружаемого файла  

Общий объем загруженных запросов отображается в области Сводка в нижней части панели "сеть".  

> [!CAUTION]
> Этот номер отслеживает только те запросы, которые были зарегистрированы с момента открытия DevTools.  Если при открытии DevTools возникли другие запросы, предыдущие запросы не учитываются.  

:::image type="complex" source="../media/network-network-total-download-size.msft.png" alt-text="Общий объем загруженных запросов" lightbox="../media/network-network-total-download-size.msft.png":::
   Рис. 29: общий размер загружаемого запроса.  
:::image-end:::  

[Просмотр несжатого размера ресурса](#view-the-uncompressed-size-of-a-resource) для просмотра больших ресурсов после того, как браузер распаковывает каждый элемент.  

### Просмотр трассировки стека, которая привела к запросу  

После того, как инструкция JavaScript запрашивает ресурс, наведите указатель мыши на столбец **инициатора** , чтобы просмотреть трассировку стека, выступающей в запрос.  

<!-- [codepen.io/contoso/pen/yLBrOWa?editors=0010#0](https://codepen.io/contoso/pen/yLBrOWa?editors=0010#0) -->  

<!--
```javascript
function init() {
  getData();
}

function getData() {
  fetch('https:/httpbin.org/get?message=hi');
}

init();
```  
-->  

:::image type="complex" source="../media/network-network-requests-initiator-stack.msft.png" alt-text="Трассировка стека, ведущая к запросу ресурсов" lightbox="../media/network-network-requests-initiator-stack.msft.png":::
   На рисунке 30 показана трассировка стека, ведущая к запросу ресурсов  
:::image-end:::  

### Просмотр несжатого размера ресурса  

Установите флажок **использовать строки большого запроса** , а затем посмотрите на нижнее значение столбца **Размер** .  

:::image type="complex" source="../media/network-network-requests-uncompressed-compare.msft.png" alt-text="Пример несжатых ресурсов" lightbox="../media/network-network-requests-uncompressed-compare.msft.png":::
   Рисунок 31: пример несжатых ресурсов \ (сжатый размер `jquery-3.3.1.min.js` файла, отправленного по сети `29.9 KB` , в то время как несжатый размер `84.9 KB` )  
:::image-end:::  

## Данные запросов на экспорт  

### Сохранение всех сетевых запросов в файле HAR  

Чтобы сохранить все сетевые запросы в файле HAR, выполните указанные ниже действия.  

1.  Наведите указатель мыши на любой запрос в таблице запросов и откройте контекстное меню (щелкните правой кнопкой мыши \).  
1.  Выберите команду **Сохранить как HAR с содержимым**.  DevTools сохраняет все запросы, произошедшие после того, как вы открыли DevTools в файл HAR.  Невозможно отфильтровать запросы или сохранить только один запрос.  

После того как вы сохраните файл HAR, вы можете импортировать его обратно в DevTools для анализа.  Просто перетащите файл HAR в таблицу запросы.  
<!--See also [HAR Analyzer][HARAnalyzer].  -->  

<!--[HARAnalyzer]: https://toolbox.alphabetapps.com/apps/har_analyzer  -->  
<!--Todo: add section link when content is available  -->  

:::image type="complex" source="../media/network-network-requests-save-har-content.msft.png" alt-text="Выбор команды "Сохранить как HAR с контентом"" lightbox="../media/network-network-requests-save-har-content.msft.png":::
   Рисунок 32: выбор команды " **Сохранить как HAR с контентом** "  
:::image-end:::  

### Копирование одного или нескольких запросов в буфер обмена  

В столбце **имя** таблицы запросы наведите указатель мыши на запрос, откройте контекстное меню (щелкните правой кнопкой мыши \), наведите указатель на пункт **Копировать**и выберите один из следующих вариантов.  

*   **Копировать адрес ссылки**.  Скопируйте URL-адрес запроса в буфер обмена.  
*   **Копирование ответа**.  Скопировать текст ответа в буфер обмена.  
*   **Копировать как выборку**.  
*   **Копировать как фигуру**.  Копирование запроса в виде текстовой команды.  
*   **Копировать все как выборку**.  
*   **Скопировать все как фигуру**.  Копирование всех запросов в виде последовательности команд с фигурой.  
*   **Копировать все как HAR**.  Скопируйте все запросы как данные HAR.  

:::image type="complex" source="../media/network-network-requests-copy-response.msft.png" alt-text="Выбор пункта "Копировать ответ"" lightbox="../media/network-network-requests-copy-response.msft.png":::
   Рисунок 33: выбор пункта " **Копировать ответ** "  
:::image-end:::  

## Изменение макета панели "сеть"  

Вы можете развернуть или свернуть разделы пользовательского интерфейса панели "сеть", чтобы сосредоточиться на важных сведениях.  

### Скрытие области фильтров  

По умолчанию в DevTools отображается **область фильтров**.  
Щелкните фильтр **фильтра** ![ ][ImageFilterIcon] , чтобы скрыть его.  

:::image type="complex" source="../media/network-network-resources-hide-filters-button.msft.png" alt-text="Кнопка "скрыть фильтры"" lightbox="../media/network-network-resources-hide-filters-button.msft.png":::
   Рисунок 34: кнопка "скрыть фильтры"  
:::image-end:::  

### Использование строк большого запроса  

Используйте большие строки, если вы хотите, чтобы в таблице сетевых запросов больше пробелов.  Некоторые столбцы также содержат дополнительные сведения при использовании больших строк.  Например, минимальное значение столбца « **Размер** » — это несжатый размер запроса.  

:::image type="complex" source="../media/network-network-requests-large-request-rows.msft.png" alt-text="Пример строк большого запроса в области "запросы"" lightbox="../media/network-network-requests-large-request-rows.msft.png":::
   Рисунок 35: пример строк большого запроса в области " **запросы** "  
:::image-end:::  

Установите флажок **использовать строки большого запроса** , чтобы включить большие строки.  

:::image type="complex" source="../media/network-network-requests-use-large-request-rows-on.msft.png" alt-text="Флажок "использовать строки большого запроса"" lightbox="../media/network-network-requests-use-large-request-rows-on.msft.png":::
   Рисунок 36: флажок " **использовать строки большого запроса** "  
:::image-end:::  

### Скрытие области обзора  

По умолчанию в DevTools отображается **область "Общие сведения**".  Снимите флажок **Показать общие сведения** , чтобы скрыть его.  

:::image type="complex" source="../media/network-network-requests-show-overview-off.msft.png" alt-text="Флажок "Показать общие сведения"" lightbox="../media/network-network-requests-show-overview-off.msft.png":::
   Рисунок 37: флажок **Показать общие сведения**  
:::image-end:::  

<!-- image links -->  

[ImageCaptureScreenshotsIcon]: ../media/capture-screenshots-icon.msft.png  
[ImageClearIcon]: ../media/clear-requests-icon.msft.png  
[ImageFilterIcon]: ../media/filter-icon.msft.png  
[ImageHideIcon]: ../media/hide-overview-icon.msft.png  
[ImageLargeResourceRowsIcon]: ../media/large-resource-rows-button-icon.msft.png  
[ImageRecordOnIcon]: ../media/record-on-icon.msft.png  

<!-- links -->  

[DevtoolsProgressiveWebApps]: /microsoft-edge/devtools-guide-chromium/network/progressive-web-apps "Отладка последовательного веб-приложения"  

<!--[NetworkConditions]: /microsoft-edge/devtools-guide-chromium/network/network-conditions "Optimize Performance Under Varying Network Conditions"  -->  

[MDNHTTPDataURIs]: https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/Data_URIs "URL-адреса данных | MDN"  

[WikiProxyServer]: https://en.wikipedia.org/wiki/Proxy_server "Прокси-сервер — Википедии"  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/network/reference) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
