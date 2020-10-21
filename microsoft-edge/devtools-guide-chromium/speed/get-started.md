---
description: Узнайте, как использовать Microsoft Edge DevTools для поиска возможностей, позволяющих быстрее загружать веб-сайты.
title: Оптимизация скорости веб-сайта с помощью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: af655941fdc836759651e8d8202e41d8d03331c5
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125491"
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

# Оптимизация скорости веб-сайта с помощью Microsoft Edge DevTools  

## Цель учебника  

В этом учебнике объясняется, как использовать Microsoft Edge DevTools, чтобы найти способы быстрой загрузки веб-сайтов.  

## Предварительные условия  

*   У вас должен быть базовый интерфейс разработки веб-приложений, аналогично тому, что научились в этом [Знакомство с классом веб-разработки][CourseraIntroductionWebDevelopmentClass].  
*   Вам ничего не нужно знать о быстродействии нагрузки.  В этом учебнике вы узнаете об этом.  

## Введение  

Это Илья.  Илья чрезвычайно знаменита в отношении Cat общества.  Он создал веб-сайт, чтобы его вентиляторы могли узнать о своем любимом продуктов.  Его вентиляторы понравятся на сайте, но в Илья сохраняются жалобы, которые медленно загружаются на сайт.  Илья предложит вам помочь ему ускорить работу сайта.  

:::image type="complex" source="../media/speed-tony.msft.png" alt-text="Илья CAT" lightbox="../media/speed-tony.msft.png":::
   Илья CAT  
:::image-end:::  

## Действие 1: аудит сайта  

Всякий раз, когда вы захотите улучшить производительность загрузки сайта, **всегда начинайте с аудита**.  
Аудитория имеет 2 важные функции.  

*   Она создает **базовый план** для измерения последующих изменений.  
*   Здесь вы найдете **Советы** , которые помогут вам изменить наиболее благоприятные изменения.  
    
### Настройка  

Сначала необходимо настроить сайт, чтобы вы могли вносить в него изменения позже.  

1.  [Откройте исходный код для сайта](https://glitch.com/edit/#!/tony).  Эта вкладка называется **вкладкой "редактор"**.  
    
    :::image type="complex" source="../media/speed-glitch-tony-server-js.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-server-js.msft.png":::
       **Вкладка "редактор"**  
    :::image-end:::  
    
1.  Выберите **Илья**.  Откроется меню.  
    
    :::image type="complex" source="../media/speed-glitch-tony-server-js-remix-project.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-server-js-remix-project.msft.png":::
       Меню, которое появляется после нажатия кнопки **Илья**  
    :::image-end:::  
    
1.  Выберите **Remix проект**.  Имя проекта меняется с **Илья** на случайное сгенерированное имя.  Теперь у вас есть Редактируемая копия кода.  Позже вы можете внести изменения в этот код.  
1.  Нажмите кнопку **Показать** и выберите **в новом окне**.  Демонстрационный ролик откроется на новой вкладке.  Эта вкладка упоминается как **вкладка Demo**.  Загрузка сайта может занять некоторое время.  
    
    :::image type="complex" source="../media/speed-glitch-tony-show-live.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-show-live.msft.png":::
       Вкладка "демонстрация"  
    :::image-end:::  
    
1.  Выберите `Control` + `Shift` + `J` \ (Windows, Linux \) или `Command` + `Option` + `J` \ (macOS \).  Рядом с демоном DevTools откроется Microsoft Edge.  
    
    :::image type="complex" source="../media/speed-glitch-tony-show-live-console.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-show-live-console.msft.png":::
       DevTools и демонстрация  
    :::image-end:::  
    
Для остальных снимков экрана в этом учебнике DevTools отображается в отдельном окне.  Выберите `Control` + `Shift` + `P` \ (Windows, Linux \) или `Command` + `Shift` + `P` \ (macOS \), чтобы открыть меню команд, введите его `Undock` и выберите команду **открепить в отдельном окне**.  

:::image type="complex" source="../media/speed-console.msft.png" alt-text="Илья CAT" lightbox="../media/speed-console.msft.png":::
   Незакрепленные DevTools  
:::image-end:::  

### Создание базового плана  

Базовый план — это запись того, как выполняется сайт, прежде чем вы внесли улучшения производительности.  

1.  Перейдите на вкладку **Аудит** .  Она может быть скрыта за кнопкой " **Дополнительные панели** " \ "дополнительные панели ![ ][ImageMorePanelsIcon] \".  На этой панели есть Lighthouse, так как проект, который включает панель «аудиты», называется **Lighthouse**.  
    
    [!INCLUDE [audits-panel-note](../includes/audits-panel-note.md)]  
    
    :::image type="complex" source="../media/speed-audits-performance.msft.png" alt-text="Илья CAT" lightbox="../media/speed-audits-performance.msft.png":::
       Панель « **Аудит** »  
    :::image-end:::  
    
    <!--todo: add link to Lighthouse when section is available  -->  
    <!-- /web/tools/lighthouse  -->  
    
1.  Соответствие параметров конфигурации аудита с параметрами, приведенными на предыдущем рисунке.  Ниже приведено описание различных параметров.  
    
    *   **Устройства**.  При настройке на **мобильном устройстве** изменяется строка агента пользователя и имитируется мобильное окно просмотра.  Настройка для **настольного компьютера** очень просто отключает изменения на **мобильном устройстве** .  
    *   **Аудита**.  Отключение категории не позволяет панели аудита выполнять эти проверки и исключает из отчета эти проверки.  Если вы хотите просмотреть предоставленные типы рекомендаций, оставьте другие доступные категории.  Отключение категорий немного ускоряет процесс аудита.  
    *   **Регулирование**.  Для **эмуляции медленного 4G, скорость процессора 4X** эмулирует типичные условия обзора на мобильном устройстве.  Она называется смоделированной, так как панель "Аудит" не выполняет никаких действий по регулированию в процессе аудита.  Вместо этого оно просто экстраполяция того, сколько времени займет загрузка страницы в условиях мобильных устройств.  Параметр " **применено...** ", в свою очередь, в действительности регулирует производительность процессора и сети с компромиссом более продолжительного процесса аудита.  
    *   **Очистите хранилище**.  При установке этого флажка все хранилище, связанное со страницей, будет очищено перед каждым аудитом.  Оставьте этот параметр, если вы хотите подвергать аудиту, как посетители в первый раз будут работать на вашем сайте.  Отключите этот параметр, если вы хотите использовать функцию повторного посещения.  
    
1.  Выберите команду **запустить аудиты**.  После 10 – 30 секунд на панели «аудиты» отображается отчет о быстродействии сайта.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed.msft.png":::
       Отчет для панели «аудит» для производительности сайта  
    :::image-end:::  
    
#### Обработка ошибок отчета  

Если вы когда-либо получаете сообщение об ошибке в отчете на панели аудиты, попробуйте запустить вкладку Demo из окна **InPrivate** без открытия других вкладок.  Это гарантирует, что вы используете Microsoft Edge из чистого состояния.  Определенные расширения Microsoft Edge часто мешают процессу аудита.  

<!--todo: add screen capture for error in audit -->  
<!--
:::image type="complex" source="../media/speed-.msft.png" alt-text="Илья CAT" lightbox="../media/speed-.msft.png":::
   A report that errored  
:::image-end:::  
-->  

### Понимание отчета  

Число в верхней части отчета является общим показателем эффективности сайта.  После внесения изменений в код вы должны увидеть этот номер.  Более высокие баллы означают более высокую производительность.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-metrics-highlighted.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-metrics-highlighted.msft.png":::
   Общая оценка производительности  
:::image-end:::  

Раздел **метрики** содержит количественные измерения производительности сайта.  Каждая метрика обеспечивает различные аспекты производительности.  Например, при первом обобщении с **содержимым** появляется сообщение о том, что содержимое сначала закрашено на экран, что является важной вехой в восприятии загрузки страницы, в то время как в **интерактивном режиме** отмечается тот момент, когда страница будет готова для обработки взаимодействия с пользователем.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-highlighted.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-highlighted.msft.png":::
   Раздел **метрики**  
:::image-end:::  

Щелкните выделенный выключатель на приведенном ниже рисунке, чтобы просмотреть описание каждой метрики, а затем нажмите **Дополнительные сведения** , чтобы прочитать его документацию.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-expanded.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-expanded.msft.png":::
   Щелкните выделенный выключатель, чтобы развернуть элементы метрик  
:::image-end:::  

Под метриками представлен набор снимков экрана, показывающий, как страница выглядит как загруженная.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png":::
   Снимки экрана, посвященные загрузке страницы  
:::image-end:::  

В разделе " **возможности** " представлены конкретные советы по повышению производительности загрузки данной страницы.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png":::
   Раздел " **возможности** "  
:::image-end:::  

Выберите возможность, чтобы узнать больше о ней.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-opportunities-expanded.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-remix-audits-performance-opportunities-expanded.msft.png":::
   **Исключение ресурсов блокировки рендеринга** возможная сделка  
:::image-end:::  

Выберите дополнительные **сведения** , чтобы просмотреть документацию о важности возможной сделки и конкретные рекомендации по ее устранению.  

:::image type="complex" source="../media/speed-web-dev-performance-audits.msft.png" alt-text="Илья CAT" lightbox="../media/speed-web-dev-performance-audits.msft.png":::
   Документация по **устранению ресурсов с блокировкой рендеринга** возможная сделка  
:::image-end:::  

Раздел **Диагностика** содержит дополнительные сведения о факторах, которые влияют на время загрузки страницы.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-diagnostics.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-remix-audits-performance-diagnostics.msft.png":::
   Раздел " **Диагностика** "  
:::image-end:::  

В разделе **переданные аудиты** показано, что делает сайт правильно.  Выберите этот пункт, чтобы развернуть раздел.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-passed-audits.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-remix-audits-performance-passed-audits.msft.png":::
   Раздел " **пройденные аудиты** "  
:::image-end:::  

## Этап 2: эксперименты  

Раздел "возможности" в отчете об аудите содержит советы по улучшению производительности страницы.  В этом разделе вы реализуете рекомендованные изменения в базе кода, проведя аудит сайта после каждого изменения, чтобы определить, как оно влияет на скорость сайта.  

### Включение сжатия текста  

В отчете говорится, что отсутствие огромных полезных данных сети является одной из самых первых возможностей для повышения производительности страницы.  Включить сжатие текста — это возможность улучшить производительность страницы.  

Сжатие текста — это сокращение размера текстового файла перед отправкой по сети, а также его сжатие.  Например, вы можете почтовые индексы, чтобы уменьшить размер папки.  

Перед включением сжатия вы можете вручную проверить, сжимаются ли текстовые ресурсы.  

1.  Откройте вкладку **сеть** .  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-remix-network.msft.png":::
       Панель " **сеть** "  
    :::image-end:::  
    
1.  Выберите значок **Параметры сети** .  
1.  Установите флажок **использовать строки большого запроса** .  Высота строк в таблице сетевых запросов возрастает.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-use-large-request-rows.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-remix-network-use-large-request-rows.msft.png":::
       Большие строки в таблице "сетевые запросы"  
    :::image-end:::  
    
1.  Если столбец **Размер** не отображается в таблице сетевых запросов, щелкните заголовок таблицы и выберите команду **Размер**.  

В каждой ячейке **размера** отображаются два значения.  Верхнее значение — размер загруженного ресурса.  
Минимальное значение — размер несжатого ресурса.  Если оба значения совпадают, значит, ресурс не сжимается, когда он отправляется по сети.  Например, на предыдущем рисунке значения Top и Bottom для параметров "" `bundle.js` — " `1.2 MB` и" `1.2 MB` ... ".  

Проверка на наличие сжатия с помощью проверки заголовков HTTP ресурса.  

1.  Выберите **bundle.js**.  
1.  Откройте вкладку **заголовки** .  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-use-large-request-rows-bundle-js.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-remix-network-use-large-request-rows-bundle-js.msft.png":::
       Вкладка " **заголовки** "  
    :::image-end:::  
    
1.  Поиск заголовка в разделе **заголовков ответа** `content-encoding` .  Вы не видите один из них, то есть `bundle.js` не был сжат.  Когда ресурс сжимается, этот верхний колонтитул обычно имеет значение `gzip` , `deflate` или `br` .  Описание этих значений показано в разделе [директивы][MDNContentEncodingDirectives] .  

Достаточно с пояснениями.  Время, чтобы внести некоторые изменения!  Включите сжатие текста, добавив несколько строк кода.  

1.  На вкладке "редактор" выберите **server.js**.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-server-js.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-remix-server-js.msft.png":::
       Edit `server.js`  
    :::image-end:::  
    
1.  Добавьте следующий код для **server.js**.  Убедитесь, что он должен быть помещен `app.use(compression())` `app.use(express.static('build'))` .  

    ```javascript
    const express = require('express');
    const app = express();
    const fs = require('fs');
    const compression = require('compression');

    app.use(compression());
    app.use(express.static('build'));
    
    const listener = app.listen(process.env.PORT || 1234, function () {
        console.log(`Listening on port ${listener.address().port}`);
    });
    ```  
    
    > [!NOTE]
    > Как правило, вы должны установить `compression` пакет с помощью какого-либо вида `npm i -S compression` , но это еще не сделано.  
    
1.  Дождитесь, пока не будет развернуто новая сборка сайта.  Неузорная анимация рядом с **инструментами** означает, что сайт перестраивается и повторно развертывается.  Изменение будет готово, когда анимация рядом с пунктом " **инструменты** " исчезает.  Выберите команду **Показать** , а затем еще раз выберите **в новом окне** .  
    
    <!--
    :::image type="complex" source="../media/speed-glitch-tony-remix-server-js-edited.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-remix-server-js-edited.msft.png":::
       The animation that indicates that the site is getting built  
    :::image-end:::  
    -->  
    
Используйте рабочие процессы, которые вы узнали ранее, чтобы вручную проверить, работает ли сжатие.  

1.  Вернитесь на вкладку Demo и повторно загрузите страницу.  Столбец « **Размер** » теперь должен показывать 2 разных значения для текстовых ресурсов `bundle.js` , таких как.  На рисунке после следующего значения аргумента " `256 KB` `bundle.js` равно" — Размер файла, отправленного по сети, а в качестве нижнего значения `1.2 MB` — несжатый размер файла.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-main.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-remix-network-main.msft.png":::
       В столбце " **Размер** " теперь показано 2 разных значения для текстовых ресурсов.  
    :::image-end:::  
    
1.  В разделе **заголовки ответа** `bundle.js` теперь должен быть указан `content-encoding: gzip` верхний колонтитул.
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-bundle-js-headers-response.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-remix-network-bundle-js-headers-response.msft.png":::
       Раздел **заголовки ответа** теперь содержат заголовок Content-Encoding  
    :::image-end:::  
    
Проведите аудит страницы, чтобы оценить, какое влияние сжатие текста влияет на производительность загрузки страницы:  

1.  Перейдите на вкладку **Аудит** .  
1.  Выберите команду **выполнить аудит** \ ( ![ выполнить аудит ][ImagePerformIcon] \).  
1.  Параметры не совпадают.  
1.  Выберите команду **запустить аудит**.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance.msft.png":::
       Отчет "Аудит" после включения сжатия текста  
    :::image-end:::  
    
<!--  Woohoo!  That looks like progress.  -->  Общая оценка производительности должна быть увеличена, а это значит, что сайт быстрее.  

#### Сжатие текста в реальном мире  

На большинстве серверов есть простые решения, подобные этим, чтобы включить сжатие.  Просто выполните поиск, чтобы настроить любой сервер, который вы используете для сжатия текста.  

### Изменение размера изображения  

Отчет о том, что не следует избегать огромных полезных данных сети, является одной из самых первых возможностей для повышения производительности страницы.  Изменение размеров изображений помогает уменьшить размер полезных данных в сети.  Если пользователь просматривает изображения на экране мобильного устройства размером 500 в пикселах, это не значит, что при отправке изображения в масштабе не более 1500 точек.  В идеале вы отправляете изображение в 500 в масштабе по пикселю.  

1.  В отчете выберите **исключить огромные полезные данные сети** , чтобы узнать, какие изображения нужно изменить.  Похоже, что 2 файлов JPG — более 2000 КБ, что больше не требуется.  
    
    <!--
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-opportunities-expanded.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-opportunities-expanded.msft.png":::
       Details about the properly size images opportunity  
    :::image-end:::  
    -->
    
1.  Вернувшись на вкладку Редактор, открыть `src/model.js` .  
1.  Заменить `const dir = 'big'` на `const dir = 'small'` .  Этот каталог содержит копии тех же изображений, размер которых был изменен.  
1.  Вновь проведите аудит страницы, чтобы увидеть, как это изменение влияет на производительность загрузки.  
    
    :::image type="complex" source="../media/speed-glitch-compression-small-images-audits-performance.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-compression-small-images-audits-performance.msft.png":::
       Отчет об аудите после изменения размеров изображений  
    :::image-end:::  
    
Похоже, что изменение имеет незначительный уровень влияния на общую оценку производительности.  Тем не менее, в этом случае баллы не показываются четко, так как данные сети, которые вы сохраняете, не отображаются.  Общий размер старой фотографии — около 5,3 мегабайт, в то время как теперь это не более 0,18 МБ.  

#### Изменение размеров изображений в реальном мире  

В случае с небольшим приложением вы можете использовать один из этих способов, так как это может быть достаточно хорошим.  Но для больших приложений это очевидно не масштабируется.  Ниже приведены некоторые стратегии управления изображениями в крупных приложениях.  

*   Изменение размера изображения во время процесса сборки.  
*   Создавайте несколько размеров изображения во время процесса сборки, а затем используйте `srcset` их в коде.  Во время выполнения браузер берет на себя выбор оптимального размера для устройства.  
    <!--See [Relative-sized images][relative].  -->
    
<!--[relative]: /web/fundamentals/design-and-ux/responsive/images#relative_sized_images  -->  

*   Использование сети CDN изображений, позволяющей динамически изменять размер изображения при запросе.  
*   По крайней мере, оптимизируйте каждое изображение.  Это может создать огромный выигрыш.  
  Оптимизация — это время, когда вы запускаете изображение с помощью специальной программы, которая уменьшает размер файла изображения.  Дополнительные советы приведены в статье основные сведения об [оптимизации изображений][EssentialImageOptimization] .  
    
### Исключение ресурсов блокировки рендеринга  

В последней версии отчета говорится о том, что в настоящее время ресурсы, блокирующие рендеринг, стали самой большой возможностью.  

Ресурс блокировки обработки — это внешний файл JavaScript или CSS, который браузер должен загрузить, проанализировать и выполнить, прежде чем отобразить страницу.  Цель состоит в том, чтобы запустить только основной код CSS и JavaScript, необходимый для правильного отображения страницы.  

Первая задача — это поиск кода, который не нужно выполнять при загрузке страницы.  

1.  Чтобы просмотреть блокируемые ресурсы, нажмите кнопку **удалить ресурсы блокировки рендеринга** .  
    `lodash.js` и `jquery.js` .  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded.msft.png":::
       Дополнительные сведения о **ресурсах блокировки обработки** с возможностью устранения  
    :::image-end:::  
    
1.  Выберите `Control` + `Shift` + `P` \ (Windows, Linux \) или `Command` + `Shift` + `P` \ (macOS \), чтобы открыть меню команд, начните вводить текст `Coverage` , а затем выберите команду **Показать покрытие**.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-command-coverage.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-command-coverage.msft.png":::
       Открытие меню "команд" на панели " **Аудит** "  
    :::image-end:::  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage.msft.png":::
       Вкладка " **покрытие** "  
    :::image-end:::  
    
1.  Нажмите кнопку **Обновить** \ ( ![ обновить ][ImageRefreshIcon] \).  На вкладке " **покрытие** " представлены общие сведения о том, какая часть `bundle.js` кода `jquery.js` и `lodash.js` выполняется при загрузке страницы.  На рисунке ниже показано, что около 76% и 30% файлов jQuery и Lodash не используются соответственно.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage-reloaded.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage-reloaded.msft.png":::
       Отчет о покрытии  
    :::image-end:::  
    
1.  Выделите строку **jquery.js** .  DevTools откроет файл на панели «источники».  Строка кода была выполнена, если рядом с ней есть синяя полоска.  Красная черта означает, что она не была выполнена и определенно не требуется при загрузке страницы.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-sources-drawer-coverage-reloaded-jquery-js.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-remix-updated-sources-drawer-coverage-reloaded-jquery-js.msft.png":::
       Просмотр файла jQuery на панели « **источники** »  
    :::image-end:::  
    
1.  Прокрутите код jQuery на немного.  Некоторые строки, которые получают слово "выполнить", на самом деле представляют собой комментарии.  Выполнение этого кода с помощью Minifier, который содержит примечания, — еще один способ уменьшить размер файла.  

Коротко говоря, при работе с собственным кодом вкладка "покрытие" помогает проанализировать код, построчно и поставлять только код, необходимый для загрузки страницы.  

Нужны ли `jquery.js` `lodash.js` файлы и даже для загрузки страницы?  На вкладке Блокировка запроса показано, что происходит, когда ресурсы недоступны.  

1.  Откройте вкладку **сеть** .  
1.  Выберите `Control` + `Shift` + `P` \ (Windows, Linux \) или `Command` + `Shift` + `P` \ (macOS \), чтобы снова открыть меню команд.  
1.  Начните вводить данные `blocking` и выберите команду **Показать блокировку запросов**.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-empty.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-empty.msft.png":::
       Вкладка " **Блокировка запросов** "  
    :::image-end:::  
    
1.  Нажмите кнопку **Добавить узор** \ ( ![ Добавить шаблон ][ImageAddPatternIcon] \), введите `/libs/*` и выберите `Enter` для подтверждения.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-added.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-added.msft.png":::
       Добавление шаблона для блокирования запросов в `libs` Каталог  
    :::image-end:::  
    
1.  Обновите страницу.  Запросы jQuery и Lodash красного цвета, означающие, что запросы были заблокированы.   Страница по-прежнему загружается и является интерактивной, поэтому она выглядит так, как это не требуется.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-network-reloaded-drawer-request-blocking-added.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-remix-updated-network-reloaded-drawer-request-blocking-added.msft.png":::
       На панели **Network (сеть** ) показано, что запросы заблокированы  
    :::image-end:::  
    
1.  Выберите команду **удалить все шаблоны** \ ( ![ удалить все шаблоны ][ImageRemoveIcon] \), чтобы удалить `/libs/*` шаблон блокировки.  
    
Как правило, вкладка "блокировка запросов" полезна для имитации того, как работает страница, если какой-либо из указанных ресурсов недоступен.  

Теперь удалите ссылки на эти файлы из кода и выполните аудит страницы еще раз:  

1.  Вернувшись на вкладку Редактор, открыть `template.html` .  
1.  Удалите `<script src="/libs/lodash.js">` и `<script src="/libs/jquery.js"></script>`.  
1.  Дождитесь повторного создания и повторного развертывания сайта.  
1.  Снова проведите аудит страницы с помощью панели **аудита** .  Ваши общие баллы должны быть улучшены.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-2-audits-performance.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-remix-updated-2-audits-performance.msft.png":::
       Отчет об **аудите** после удаления ресурсов блокировки рендеринга  
    :::image-end:::  
    
#### Оптимизация критического пути отрисовки в реальном мире  

**Критический путь рендеринга** указывает на код, необходимый для загрузки страницы.  Как правило, скорость загрузки страницы повышается за счет отправки критического кода только при загрузке страницы, а затем — через отложенную загрузку всех остальных.  

<!--[CRP]: /web/fundamentals/performance/critical-rendering-path/  -->  

*   Маловероятно, что вы можете найти сценарии, которые можно удалить прямо, но вы можете найти большое количество сценариев, которые вам не нужно запрашивать во время загрузки страницы, и, возможно, они будут запрашиваться асинхронно.  <!--See [Using async or defer][async].  -->  
*   Если вы используете платформу, убедитесь в том, что у нее есть производственный режим.  Этот режим может использовать такие функции, как [Tree встряхнув][WebpackTreeShaking] , для удаления ненужного кода, блокирующего критический рендеринг.  
    
<!--[async]: /web/fundamentals/performance/optimizing-content-efficiency/loading-third-party-javascript/#use_async_or_defer  -->  

### Работа менее основного потока  

В последней версии отчета представлены некоторые небольшие возможности по экономии средств в разделе "возможности", но если вы просмотрии раздел "Диагностика", это похоже на то, что наибольший узкий участок слишком велик для основного потока.  

Основной поток — это тот случай, когда браузер выполняет большую часть работы, необходимой для отображения страницы, например синтаксического анализа и выполнения HTML, CSS и JavaScript.  

Цель состоит в том, чтобы проанализировать трудозатраты, выполняемые основным потоком при загрузке страницы, и найти способы задержать или удалить ненужные данные.  

1.  Откройте вкладку **производительность** .  
1.  Выберите **Параметры захвата** \ ( ![ Параметры захвата ][ImageCaptureIcon] ).  
1.  Настройте **сеть** на **медленное 3G** и **ЦП** , чтобы **6X замедление**.  На мобильных устройствах обычно используются больше ограничений на оборудование, чем на ноутбуках или настольных компьютерах, поэтому эти параметры позволяют загрузить страницу так, как если бы вы использовали менее мощное устройство.  
1.  Нажмите кнопку **Обновить** \ ( ![ обновить ][ImageRefreshIcon] \).  DevTools обновляет страницу и создает визуализацию всей выполненной работы, чтобы загрузить страницу.  Этот зрительный образ называется **трассировкой**.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu.msft.png":::
       Трассировка загрузки страницы на панели **производительности**  
    :::image-end:::  
    
Трассировка отображает операцию в хронологическом порядке, слева направо.  На диаграммах с частотой кадров, ЦП и нетто в верхней части экрана дается обзор кадров в секунду, активности ЦП и активности сети.  Выделенный блок желтого цвета, показанный на рисунке после следующего, ЦП полностью загружен с действиями в сценарии.  Это говорит о том, что вы можете ускорить загрузку страницы, выполнив меньше действий JavaScript.  

:::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main-highlight.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main-highlight.msft.png":::
   Раздел обзора трассировки  
:::image-end:::  

Изучите трассировку, чтобы найти способы выполнения меньшей работы в JavaScript.  

1.  Щелкните раздел **время показа** , чтобы развернуть его.  В зависимости от того факта, что существует ряд мер [времени][MDNUserTimingApi] , не отклика, может показаться, что приложение Илья использует режим разработки реагируй.  Переключение в режим рабочего режима может привести к снижению производительности WINS.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings.msft.png":::
       Раздел " **временные интервалы** "  
    :::image-end:::  
    
1.  Чтобы свернуть этот раздел, выберите **время показа** еще раз.  
1.  Просмотрите **основной** раздел.  В этом разделе показан хронологический журнал основных операций потока, слева направо.  Ось y (сверху вниз) показывает причины возникновения событий.  Например, в figyre после указанных ниже `Evaluate Script` событий событие привело `(anonymous)` к выполнению функции, которое привело к выполнению `(anonymous)` `__webpack__require__` и т. д.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main.msft.png":::
       **Основной** раздел  
    :::image-end:::  
    
1.  Прокрутите страницу вниз до конца **основного** раздела.  При использовании платформы большая часть верхнего действия вызывается платформой, которая обычно находится в вашем элементе управления.  Действия, вызванные вашим приложением, обычно находятся в нижней части экрана.  В этом приложении это похоже на функцию с именем, которая `App` вызывает большое количество запросов к `mineBitcoin` функции.  Это звучит так, как Илья может использовать устройства своего вентилятора для cryptocurrency...  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-minebitcoin.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-minebitcoin.msft.png":::
       Наведение указателя на `mineBitcoin` мероприятие  
    :::image-end:::  
    
    > [!NOTE]
    > Несмотря на то что запросы вашей платформы обычно прерываются из вашего элемента управления, иногда вы можете структурировать приложение таким образом, чтобы она выполнялась неэффективно.  Реструктуризация приложения для эффективного использования инфраструктуры — это способ выполнения менее основного потока работ.  Тем не менее, для этого необходимо глубокое понимание того, как работает ваша платформа, и какие изменения вносятся в вашем собственном коде для более эффективной работы с платформой.  
    
1.  Разверните раздел **снизу вверх** .  На этой вкладке прерываются действия, которые выполнялись в течение всего времени.  Если вы ничего не видите в разделе Bottom-Up, щелкните надпись для **основного** раздела.  В разделе " **снизу вверх** " отображаются только сведения о каких-либо действиях или группах действий, которые вы уже выбрали.  Например, если вы `mineBitcoin` **настроили** одно из действий, в разделе снизу вверх будет отображаться только информация для этого действия.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-summary-minebitcoin.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-summary-minebitcoin.msft.png":::
       Вкладка " **снизу вверх** "  
    :::image-end:::  
    
В столбце " **собственное время** " показано, сколько времени было затрачено непосредственно на каждое действие.  Например, на приведенном ниже рисунке около 63% времени основного потока было затрачено на выполнение `mineBitcoin` функции.  

Время от времени до того, чтобы узнать, используется ли производственный режим и уменьшается активность JavaScript, может ускорить загрузку страницы.  Начните работу в режиме "в производство":  

1.  На вкладке Редактор откройте `webpack.config.js` .  
1.  Заменить `"mode":"development"` на `"mode":"production"` .  
1.  Дождитесь завершения развертывания новой сборки.  
1.  Вновь проведите аудит страницы.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-3-audits-performance.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-remix-updated-3-audits-performance.msft.png":::
       Отчет по аудиту после настройки пакета для использования режима "в производство"  
    :::image-end:::  
    
Сокращение действий JavaScript путем удаления запроса на `mineBitcoin` :  

1.  На вкладке Редактор откройте `src/App.jsx` .  
1.  Закомментируйте запрос `this.mineBitcoin(1500)` в `constructor` .  
1.  Дождитесь завершения развертывания новой сборки.  
1.  Вновь проведите аудит страницы.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-4-audits-performance.msft.png" alt-text="Илья CAT" lightbox="../media/speed-glitch-tony-remix-updated-4-audits-performance.msft.png":::
       Отчет по аудиту после удаления ненужных действий JavaScript  
    :::image-end:::  
    
Похоже, что Последнее изменение вызвало значительный переход в производительности!  

> [!NOTE]
> Этот раздел предоставил краткое введение в панель производительности.  Дополнительные сведения о том, как анализировать производительность страниц, можно найти в статье [Анализ производительности][DevtoolsEvaluatePerformanceReference] .  

<!--todo: add section when available -->  

#### Выполнение менее основного потока работ в реальном мире  

Как правило, панель **производительности** является наиболее распространенным способом для понимания того, какие действия выполняет загружаемый сайт, и Узнайте о способах удаления ненужных действий.  

Если вы предпочитаете использовать более похожий подход `console.log()` , Пользовательский API для работы с [временными][MDNUserTimingApi] сведениями позволяет вам произвольно помечать определенные этапы жизненного цикла приложения, чтобы отслеживать продолжительность каждого из этих фаз.  

## Краткий обзор  

*   Каждый раз, когда вы задаете оптимальное качество нагрузки для сайта, всегда начинайте с аудита.  Аудит определяет базовые показатели и предоставляет советы по улучшению.  
*   За один раз сделайте одно изменение и проведите аудит страницы после каждого изменения, чтобы увидеть, как это изолированное изменение влияет на производительность.  

<!--
## Next steps  

*   Run audits on your own site!  If you need help interpreting your report, or finding ways to improve your load performance, check out [Feedback](#feedback) for ways to get help from the DevTools community.  Stack Overflow, the mailing list, or Twitter are probably best for these types of questions.  
*   Please leave [feedback](#feedback) on this tutorial.  I really do use the data to make better tutorials for you.  
-->  

## Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageAddPatternIcon]: ../media/add-pattern-icon.msft.png  
[ImageCaptureIcon]: ../media/capture-icon.msft.png  
[ImageLargeResourceRowsButtonIcon]: ../media/large-resource-rows-button-icon.msft.png  
[ImageMorePanelsIcon]: ../media/more-panels-icon.msft.png  
[ImagePerformIcon]: ../media/perform-icon.msft.png  
[ImageRefreshIcon]: ../media/reload-icon.msft.png  
[ImageRemoveIcon]: ../media/remove-icon.msft.png  
<!-- links -->  

[DevtoolsEvaluatePerformanceReference]: ../evaluate-performance/reference.md "Справка по анализу производительности | Документы Microsoft"  

[CourseraIntroductionWebDevelopmentClass]: https://www.coursera.org/learn/web-development#syllabus "Знакомство с классом веб-разработки | Coursera"  

[EssentialImageOptimization]: https://images.guide "Оптимизация изображений"  

[MDNContentEncodingDirectives]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Content-Encoding#Directives "Директивы-кодировка содержимого | MDN"  
[MDNUserTimingApi]: https://developer.mozilla.org/docs/Web/API/User_Timing_API "API времени пользователя | MDN"  

[WebpackTreeShaking]: https://webpack.js.org/guides/tree-shaking "Tree встряхнув | упаковать"  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/speed/get-started) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
