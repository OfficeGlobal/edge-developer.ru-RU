---
description: Учебник по наиболее распространенным функциям, связанным с сетью, в Microsoft Edge DevTools.
title: Проверка активности сети в Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: a55ff05e29817c483cbf13b8713ef37cf96424d5
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125428"
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

# Проверка активности сети в Microsoft Edge DevTools  

В этом практическом занятии описаны некоторые из наиболее часто используемых функций DevTools, связанных с проанализом активности сети для страницы.  

Для просмотра функциональных возможностей используйте [ссылку сетевая ссылка][DevtoolsNetworkReference] .  

<!--TODO: This entire section needs a Microsoft Edge DevTools re-write  -->

<!-- Read on, or watch the video version of this tutorial:  -->  

<!--
> [!VIDEO embed/e1gAyQuIFQo]  
-->

## Когда следует использовать панель "сеть"  

В общем случае следует использовать панель "сеть", чтобы убедиться в том, что ресурсы загружаются или загружаются должным образом.  Наиболее распространенными вариантами использования панели "сеть" являются:  

*   Убедитесь в том, что ресурсы действительно отправляются или загружаются вообще.  
*   Проверка свойств отдельного ресурса, например HTTP-заголовков, содержимого, размера и т. д.  
    
Если вы ищете способы повышения быстродействия загрузки страниц, **не** начинайте с панели "сеть".  Существует множество типов проблем с производительностью нагрузки, не связанных с работой сети.  Начните работу с панели аудита, так как она содержит рекомендации по улучшению страницы.  Ознакомьтесь со [скоростью оптимизации веб-сайта][DevtoolsSpeedGetStarted].  

## Открытие панели "сеть"  

Чтобы максимально эффективно пользоваться этим учебником, откройте демонстрацию и ознакомьтесь с функциями на странице Demo.  

1.  Откройте [демонстрацию Приступая к работе][GlitchNetworkGetStarted].  
    
    :::image type="complex" source="../media/network-glitch-inspect-network-activity-demo.msft.png" alt-text="Демонстрация" lightbox="../media/network-glitch-inspect-network-activity-demo.msft.png":::
       Демонстрация  
    :::image-end:::  
    
    <!--You may prefer to move the demo to a separate window.  -->  
    
    <!--
    :::image type="complex" source="../media/network-tutorial/windows.msft.png" alt-text="Демонстрация" lightbox="../media/network-tutorial/windows.msft.png":::
       The demo in one window and this tutorial in a different window  
    :::image-end:::  
    -->
    
1.  [Откройте DevTools][DevToolsOpen] , нажав клавиши `Control` + `Shift` + `J` \ (Windows, Linux \) или `Command` + `Option` + `J` \ (macOS \).  Откроется панель **консоли** .  
    
    :::image type="complex" source="../media/network-glitch-console.msft.png" alt-text="Демонстрация" lightbox="../media/network-glitch-console.msft.png":::
       На **консоли**  
    :::image-end:::  
    
    Вы можете [закрепить DevTools в нижней части окна][DevToolsCustomizePlacement].  
    
    :::image type="complex" source="../media/network-glitch-console-bottom.msft.png" alt-text="Демонстрация" lightbox="../media/network-glitch-console-bottom.msft.png":::
       DevTools закреплено в нижней части окна  
    :::image-end:::  
    
1.  Откройте вкладку **сеть** .  Откроется панель **Network (сеть** ).  
    
    :::image type="complex" source="../media/network-glitch-network-bottom.msft.png" alt-text="Демонстрация" lightbox="../media/network-glitch-network-bottom.msft.png":::
       Инструмент **консоли** в DevTools закрепленной в нижней части окна  
    :::image-end:::  
    
Прямо сейчас панель Network (сеть) пуста.  DevTools только записывает сетевые активности после того, как вы откроете ее и не произошел никаких сетевых операций после того, как вы открыли DevTools.  

## Регистрация активности в сети  

Чтобы просмотреть сетевую активность, которая вызывается страницей, выполните указанные ниже действия.  

1.  Перезагрузите страницу.  На панели Network (сеть) регистрируются все сетевые активности в **журнале сети**.  
    
    :::image type="complex" source="../media/network-glitch-network.msft.png" alt-text="Демонстрация" lightbox="../media/network-glitch-network.msft.png":::
       **Журнал сети**  
    :::image-end:::  
    
    Каждая строка **журнала сети** представляет ресурс.  По умолчанию ресурсы указаны в хронологическом порядке.  Самый верхний ресурс обычно является основным HTML-документом.  Самый нижний ресурс — это тот, который запрашивался последним.  
    
    Каждый столбец представляет сведения о ресурсе.  На приведенном выше рисунке отображаются столбцы по умолчанию.  

    *   **Состояние**.  Код состояния HTTP для ответа.  
    *   **Тип**.  Тип ресурса.  
    *   **Инициатор**.  Причина запроса ресурса.  При выборе ссылки в столбце инициатора осуществляется переход к исходному коду, вызвавшему запрос.  
    *   **Time (время**).  Продолжительность запроса.  
    *   **Каскадом**.  Графическое представление различных стадий запроса.  Наведите указатель мыши на Каскад, чтобы увидеть разбивку.  
    
    > [!NOTE]
    > Диаграмма, расположенная над сетевым журналом, называется обзором.  Вы не будете использовать граф обзора в этом учебнике, поэтому вы можете скрыть его.  Ознакомьтесь [со статьей скрыть область "Общие сведения"][DevtoolsReferenceHideOverview].
    
1.  После открытия DevTools записывает в журнал сети активность сети.  
    Чтобы продемонстрировать это, сначала ознакомьтесь с нижней частью **журнала сети** и запомните о том, что последнее действие будет заглянуть в эту оценку.  
1.  Теперь нажмите кнопку " **получить данные** " в демонстрационной версии.  
1.  Снова посмотрите на нижнюю часть **сетевого журнала** .  Вы должны увидеть новый ресурс под названием "" `getstarted.json` .  Нажатие кнопки " **получить данные** " привела к тому, что страница запрашивает этот файл.  
    
    :::image type="complex" source="../media/network-glitch-network-new-resource.msft.png" alt-text="Демонстрация" lightbox="../media/network-glitch-network-new-resource.msft.png":::
       Новый ресурс в **сетевом журнале**  
    :::image-end:::  
    
## Показать дополнительные сведения  

Столбцы сетевого журнала можно настраивать.  Столбцы, которые вы не используете, могут быть скрыты.  
Кроме того, существует множество столбцов, которые по умолчанию скрыты, что может оказаться полезным.  

1.  Щелкните правой кнопкой мыши заголовок таблицы журнала сети и выберите команду **Domain (домен**).  Теперь отображается домен каждого ресурса.  
    
    :::image type="complex" source="../media/network-glitch-network-edit-column.msft.png" alt-text="Демонстрация" lightbox="../media/network-glitch-network-edit-column.msft.png":::
       Включение столбца Domain (домен)  
    :::image-end:::  
    
    > [!TIP]
    > Просмотр полного URL-адреса ресурса при наведении указателя мыши на ячейку в столбце **имя** .  
    
## Имитация медленных подключений к сети  

Сетевое подключение компьютера, используемого для создания сайтов, скорее всего быстрее, чем сетевые подключения мобильных устройств ваших пользователей.  Перетаскивая страницу, вы получите более общее представление о том, как долго страница будет загружаться на мобильном устройстве.  

1.  Выберите раскрывающийся список **регулирования** , для которого по умолчанию установлено значение в **сети** .  
    
    :::image type="complex" source="../media/network-glitch-network-throttling.msft.png" alt-text="Демонстрация" lightbox="../media/network-glitch-network-throttling.msft.png":::
       Включение регулирования  
    :::image-end:::  
    
1.  Выберите **медленное 3G**.  
    
    :::image type="complex" source="../media/network-glitch-network-throttling-slow-3g.msft.png" alt-text="Демонстрация" lightbox="../media/network-glitch-network-throttling-slow-3g.msft.png":::
       Выбор медленной сети 3G  
    :::image-end:::  
    
1.  Нажмите кнопку **перезагрузить** ![ ][ImageRefreshIcon] , а затем выберите **пустой кэш и принудительную перезагрузку**.  
    
    :::image type="complex" source="../media/network-glitch-empty-cache-and-hard-reset.msft.png" alt-text="Демонстрация" lightbox="../media/network-glitch-empty-cache-and-hard-reset.msft.png":::
       **Пустой кэш и окончательная перезагрузка**  
    :::image-end:::  
    
    При повторном посещении браузер обычно обслуживает некоторые файлы из [кэша][MDNHTTPCache], что ускоряет загрузку страницы.  **Пустой кэш, и при принудительной перезагрузке** браузер перейдет в сеть для всех ресурсов.  Это полезно, если вы хотите узнать, как в первый раз происходит загрузка страницы посетителем.  
    
    > [!NOTE]
    > **Пустой кэш и рабочий процесс повторной загрузки** доступны только в том случае, если открыт DevTools.  
    
## Захват снимков экрана  

С помощью снимков экрана можно увидеть, как страница была найдена во время загрузки.  

1.  Выберите \ ( ![ Параметры сети ][ImageSettingsIcon] \) и установите флажок **захватить снимки экрана** .
1.  Снова загрузите страницу с помощью **пустого кэша и окончательной повторной загрузки** .  Если вам нужно напоминание о том, как это сделать, ознакомьтесь [с](#simulate-a-slower-network-connection) разрешениями.  
    В области снимков экрана представлены эскизы того, как страница рассмотрелась на разных этапах процесса загрузки.  
    
    :::image type="complex" source="../media/network-glitch-network-screenshots.msft.png" alt-text="Демонстрация" lightbox="../media/network-glitch-network-screenshots.msft.png":::
       Снимки экрана загрузки страницы  
    :::image-end:::  
    
1.  Выберите первый эскиз.  DevTools показывает, какая сетевая активность происходила в данный момент времени.  
    
    :::image type="complex" source="../media/network-glitch-network-screenshots-first.msft.png" alt-text="Демонстрация" lightbox="../media/network-glitch-network-screenshots-first.msft.png":::
       Сетевая активность, происходящий на первом снимке экрана  
    :::image-end:::  
    
1.  Нажмите кнопку \ ( ![ Параметры сети ][ImageSettingsIcon] \) еще раз и снимите флажок **захватить снимки экрана** , чтобы закрыть область снимки экрана.
1.  Повторно загрузите страницу.  
    
## Проверка сведений о ресурсе  

Выберите ресурс, чтобы получить дополнительные сведения о нем.  Попробуйте вот так:  

1.  Выберите `getstarted.html` .  Показана вкладка " **заголовки** ".  Используйте эту вкладку для проверки заголовков HTTP.  
    
    :::image type="complex" source="../media/network-glitch-network-resources-headers.msft.png" alt-text="Демонстрация" lightbox="../media/network-glitch-network-resources-headers.msft.png":::
       Вкладка " **заголовки** "  
    :::image-end:::  
    
1.  Откройте вкладку **Предварительный просмотр** .  Отобразится основной рендеринг HTML-кода.  
    
    :::image type="complex" source="../media/network-glitch-network-resources-preview.msft.png" alt-text="Демонстрация" lightbox="../media/network-glitch-network-resources-preview.msft.png":::
       Вкладка " **Предварительный просмотр** "  
    :::image-end:::  
    
    Эта вкладка полезна, если API возвращает код ошибки в HTML.  Возможно, вам будет проще прочитать обработанный HTML, чем исходный HTML-код или просматривает изображения.  

1.  Откройте вкладку **ответ** .  Отобразится исходный код HTML.  
    
    :::image type="complex" source="../media/network-glitch-network-resources-response.msft.png" alt-text="Демонстрация" lightbox="../media/network-glitch-network-resources-response.msft.png":::
       Вкладка " **ответ** "  
    :::image-end:::  
    
    > [!TIP]
    > Когда файл minified, при нажатии кнопки **Формат** \ ( ![ Формат ][ImageFormatIcon] \) в нижней части вкладки **ответа** повторно форматирует содержимое файла для чтения.  
    
1.  Откройте вкладку **время** .  Показана сетевая подразделение активности для этого ресурса.  
    
    :::image type="complex" source="../media/network-glitch-network-resources-timing.msft.png" alt-text="Демонстрация" lightbox="../media/network-glitch-network-resources-timing.msft.png":::
       Вкладка **время**  
    :::image-end:::  
    
1.  **Close** ![ ][ImageCloseIcon] Чтобы снова просмотреть журнал сети, нажмите Закрыть (закрыть).  
    
    :::image type="complex" source="../media/network-glitch-network-resources-close-tabs.msft.png" alt-text="Демонстрация" lightbox="../media/network-glitch-network-resources-close-tabs.msft.png":::
       Кнопка " **Закрыть** "  
    :::image-end:::  
    
## Поиск заголовков и ответов в сети  

Используйте область **поиска** , если вам нужно найти заголовки HTTP и ответы по всем ресурсам для определенной строки или регулярного выражения.  

Например, предположим, что вы хотите убедиться, что ваши ресурсы используют разумные **политики кэширования**.  

<!--TODO: add cache policies section when available  -->

1.  Нажмите **Поиск** \ ( ![ Поиск ][ImageSearchIcon] \).  Область поиска откроется слева от сетевого журнала.  
    
    :::image type="complex" source="../media/network-glitch-network-search-empty.msft.png" alt-text="Демонстрация" lightbox="../media/network-glitch-network-search-empty.msft.png":::
       Область " **Поиск** "  
    :::image-end:::  
    
1.  Введите текст `Cache-Control` и выберите его `Enter` .  В области поиска перечислены все вхождения `Cache-Control` , найденные в заголовках или содержимом ресурсов.  
    
    :::image type="complex" source="../media/network-glitch-network-search-cache-control.msft.png" alt-text="Демонстрация" lightbox="../media/network-glitch-network-search-cache-control.msft.png":::
       Результаты поиска по запросу  `Cache-Control`  
    :::image-end:::  
    
1.  Выберите результат, чтобы просмотреть ресурс, в котором был найден результат.  Если вы видите сведения о ресурсе, выберите результат, чтобы перейти непосредственно к нему.  Например, если запрос был найден в заголовке, откроется вкладка Заголовки.   Если запрос найден в содержимом, откроется вкладка **ответ** .  
    
    :::image type="complex" source="../media/network-glitch-network-search-cache-control-headers-response-headers.msft.png" alt-text="Демонстрация" lightbox="../media/network-glitch-network-search-cache-control-headers-response-headers.msft.png":::
       Результат поиска, выделенный на вкладке " **заголовки** "  
    :::image-end:::  
    
1.  Закройте область поиска и вкладку заголовки.  
    
    :::image type="complex" source="../media/network-glitch-network-search-close.msft.png" alt-text="Демонстрация" lightbox="../media/network-glitch-network-search-close.msft.png":::
       Кнопки " **Закрыть** "  
    :::image-end:::  
    
## Фильтрация ресурсов  

DevTools предоставляет множество рабочих процессов для фильтрации ресурсов, не относящихся к поставленной задаче.  

:::image type="complex" source="../media/network-glitch-network-filter-empty.msft.png" alt-text="Демонстрация" lightbox="../media/network-glitch-network-filter-empty.msft.png":::
   Панель инструментов " **фильтры** "  
:::image-end:::  

Панель инструментов " **фильтры** " должна быть включена по умолчанию.  Если не так:  

1.  Щелкните **Фильтр** \ ( ![ фильтр ][ImageFilterIcon] \), чтобы отобразить его.  
    
### Фильтрация по строке, регулярному выражению или свойству  

Текстовое поле « **Фильтр** » поддерживает различные типы фильтрации.  

1.  Введите `png` текст в текстовое поле **Фильтр** .  Отображаются только файлы, содержащие текст `png` .  В этом случае только файлы, соответствующие фильтру, являются изображениями в формате PNG.  
    
    :::image type="complex" source="../media/network-glitch-network-filter-png.msft.png" alt-text="Демонстрация" lightbox="../media/network-glitch-network-filter-png.msft.png":::
       Строковый фильтр  
    :::image-end:::  
    
1.  Введите `/.*\.[cj]s+$/`.  DevTools отфильтровать все ресурсы с именем файла, которое не оканчивается на a, а `j` `c` затем с 1 или более `s` символами.  
    
    :::image type="complex" source="../media/network-glitch-network-filter-regex.msft.png" alt-text="Демонстрация" lightbox="../media/network-glitch-network-filter-regex.msft.png":::
       Фильтр регулярных выражений  
    :::image-end:::  
    
1.  Введите `-main.css`.  DevTools отфильтровать `main.css` .  Если какой – либо другой файл соответствует шаблону, он также будет исключен.  
    
    :::image type="complex" source="../media/network-glitch-network-filter-negative-statement.msft.png" alt-text="Демонстрация" lightbox="../media/network-glitch-network-filter-negative-statement.msft.png":::
       Отрицательный фильтр  
    :::image-end:::  
    
1.  Введите `domain:cdn.glitch.com` текст в текстовое поле **Фильтр** .  DevTools отфильтровать все ресурсы с URL-адресом, который не соответствует этому домену.  
    
    :::image type="complex" source="../media/network-glitch-network-filter-property-value.msft.png" alt-text="Демонстрация" lightbox="../media/network-glitch-network-filter-property-value.msft.png":::
       Фильтр свойств  
    :::image-end:::  
    
    Просмотрите [запросы фильтрации по свойствам][DevtoolsReferenceProperty] для полного списка фильтруемых свойств.  
    
1.  Очистите текстовое поле " **Фильтр** " в любом тексте.  
    
### Фильтрация по типу ресурсов  

Чтобы сосредоточиться на файле определенного типа, например в таблицах стилей, выполните указанные ниже действия.  

1.  Выберите **CSS**.  Все остальные типы файлов будут отфильтрованы.  
    
    :::image type="complex" source="../media/network-glitch-network-filter-file-type-css.msft.png" alt-text="Демонстрация" lightbox="../media/network-glitch-network-filter-file-type-css.msft.png":::
       Показывать только CSS – файлы  
    :::image-end:::  
    
1.  Чтобы также просмотреть сценарии, удерживайте клавишу `Control` \ (Windows, Linux \) или `Command` \ (macOS \), а затем выберите **JS**.  
    
    :::image type="complex" source="../media/network-glitch-network-filter-file-type-css-js.msft.png" alt-text="Демонстрация" lightbox="../media/network-glitch-network-filter-file-type-css-js.msft.png":::
       Показывать только файлы CSS и JS  
    :::image-end:::  
    
1.  Нажмите кнопку **все** , чтобы удалить фильтры и снова просмотреть все ресурсы.  
    
Просмотр [запросов фильтрации][DevtoolsNetworkReferenceFilter] для других рабочих процессов фильтрации.  

## Блокировать запросы  

Как выглядит и работает страница при недоступности некоторых ресурсов страницы?  Не удается полностью завершить его или он по-прежнему работает?  Блокировка запросов на определение:  

1.  Выберите `Control` + `Shift` + `P` \ (Windows, Linux \) или `Command` + `Shift` + `P` \ (macOS \), чтобы открыть **меню команд**.  
    
    :::image type="complex" source="../media/network-glitch-network-cli-empty.msft.png" alt-text="Демонстрация" lightbox="../media/network-glitch-network-cli-empty.msft.png":::
       **Меню команд**  
    :::image-end:::  
    
1.  Введите `block` команду **Показать блокировку запросов**и нажмите кнопку `Enter` .  
    
    :::image type="complex" source="../media/network-glitch-network-cli-block.msft.png" alt-text="Демонстрация" lightbox="../media/network-glitch-network-cli-block.msft.png":::
       **Показать блокировку запросов**  
    :::image-end:::  
    
1.  Нажмите кнопку **Добавить узор** \ ( ![ Добавить шаблон ][ImageAddIcon] \).  
1.  Введите `main.css`.  
    
    :::image type="complex" source="../media/network-glitch-network-cli-block-add-pattern.msft.png" alt-text="Демонстрация" lightbox="../media/network-glitch-network-cli-block-add-pattern.msft.png":::
       Снижающи `main.css`  
    :::image-end:::  
    
1.  Нажмите кнопку **Добавить**.  
1.  Перезагрузите страницу.  Как и предполагалось, стиль страницы немного изменился, так как основная таблица стилей заблокирована.  
    
    > [!NOTE]
    > `main.css`Строка в сетевом журнале.  Красный текст означает, что ресурс заблокирован.
    
    :::image type="complex" source="../media/network-glitch-network-cli-block-main-css.msft.png" alt-text="Демонстрация" lightbox="../media/network-glitch-network-cli-block-main-css.msft.png":::
       `main.css` заблокирован  
    :::image-end:::  
    
1.  Снимите флажок **включить блокировку запросов** .  

## Заключение  

Поздравляем, вы завершили обучение.  Теперь вы знаете, как использовать панель " **сеть** " в Microsoft Edge DevTools!

Перейдите по [ссылке Network (сеть][DevtoolsNetworkReference] ), чтобы найти другие функции DevTools, связанные с проанализом активности сети.  

## Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageAddIcon]: ../media/add-icon.msft.png  
[ImageCloseIcon]: ../media/close-icon.msft.png  
[ImageFilterIcon]: ../media/filter-icon.msft.png  
[ImageFormatIcon]: ../media/format-icon.msft.png  
[ImageRefreshIcon]: ../media/refresh-icon.msft.png  
[ImageScreenshotsIcon]: ../media/screenshots-icon.msft.png  
[ImageSearchIcon]: ../media/search-icon.msft.png  
[ImageSettingsIcon]: ../media/settings-icon.msft.png

<!-- links -->  

<!--[CachePolicies]: ../../../web/tools/lighthouse/audits/cache-policy ""  -->  

[DevToolsCustomizePlacement]: ../customize/placement.md "Изменение положения Microsoft Edge DevTools | Документы Microsoft"  
[DevtoolsNetworkReference]: ./reference.md "Справка по анализу сети | Документы Microsoft"
[DevtoolsNetworkReferenceFilter]: ./reference.md#filter-requests "Запросы фильтрации — Справочник по анализу сети | Документы Microsoft"  
[DevtoolsReferenceHideOverview]: ./reference.md#hide-the-overview-pane "Скрыть область обзора — Справка по анализу сети | Документы Microsoft"
[DevtoolsReferenceProperty]: ./reference.md#filter-requests-by-properties "Фильтрация запросов по свойствам-Справка по анализу сети | Документы Microsoft"
[DevToolsOpen]: ../open.md "Открыть Microsoft Edge DevTools | Документы Microsoft"  
[DevtoolsSpeedGetStarted]: ../speed/get-started.md "Оптимизация скорости веб-сайта с помощью Microsoft Edge DevTools | Документы Microsoft"  

[GlitchNetworkGetStarted]: https://microsoft-edge-chromium-devtools.glitch.me/static/network/getstarted.html "Пример проверки активности сети | Цепь"  

[MDNHTTPCache]: https://developer.mozilla.org/docs/Web/HTTP/Caching "Кэширование HTTP | MDN"  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/network/index) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
