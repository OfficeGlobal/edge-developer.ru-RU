---
description: Функции отладки сетки CSS, запросы на изменение и воспроизведение с помощью консоли сети и многое другое.
title: Новые возможности DevTools (Microsoft Edge 85)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 01651bdf0f36f7c175f843655c275695a680b6c1
ms.sourcegitcommit: b337717957529239434b4e8e1e167aebf0543518
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/15/2020
ms.locfileid: "11015463"
---
# Новые возможности DevTools (Microsoft Edge 85)  

## Объявления из группы Microsoft Edge DevTools  

В следующих разделах представлен список извещений, которые могут быть пропущены командой Microsoft Edge DevTools.  Просмотрите объявления, чтобы ознакомиться с новыми возможностями в DevTools, расширениях кода Visual Studio и многое другое.  Чтобы всегда оставаться на связи с самыми последними и более свежими возможностями, скачайте на веб – [каналы предварительного просмотра Microsoft Edge][MicrosoftEdgePreviewChannels] и [следуйте указаниям Microsoft Edge DevTools Team для Twitter][EdgeDevToolsTwitterAccount].  

### Функции отладки сетки каскадных стилей  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Экспериментальная функция":::
   Экспериментальная функция  
:::image-end:::  

Группа Microsoft Edge DevTools — совместная работа с группой Chrome DevTools и Chromium, чтобы добавить в DevTools новые функции отладки сетки каскадных стилей.  Теперь вы можете отображать номера линий сетки, зазоры сетки и дополнительные линии сетки в качестве наложений на страницы.  Кроме того, в скором времени становятся более улучшены инструменты сетки.  

:::image type="complex" source="../../media/2020/06/experiments-grid.msft.png" alt-text="Экспериментальная функция" lightbox="../../media/2020/06/experiments-grid.msft.png":::
   Функции отладки сетки каскадных стилей
:::image-end:::  

> [!NOTE]
> Чтобы включить эксперимент, ознакомьтесь со следующей страницей [Включение экспериментальных функций][DevtoolsExperimentalFeaturesTurnOn] и установите флажок **включить новые возможности отладки сетки каскадных стилей**.  
> 
> Чтобы опробовать эксперимент с образцом, ознакомьтесь со статьей [Пример планировщика сетки каскадных стилей][CodepenRachelweilYzwBzKM].  

[#1047356][CR1047356] проблем с Chromium  

### Изменение и повторное воспроизведение запросов с помощью сетевой консоли  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Экспериментальная функция на запросах в [сетевом журнале][DevtoolsNetworkIndexLogActivity] с помощью **сетевой консоли**." ::: 

:::image type="complex" source="../../media/2020/06/experiments-network-console-edit-and-replay.msft.png" alt-text="Экспериментальная функция" lightbox="../../media/2020/06/experiments-network-console-edit-and-replay.msft.png":::
   Изменение и повторное воспроизведение запроса в [NetworkLog][DevtoolsNetworkIndexLogActivity] с помощью **сетевой консоли**  
:::image-end:::  

Новая панель, **Сетевая консоль** открывается в [ящике DevTools][DevtoolsCustomizeIndexDrawer] и автоматически заполняется данными для HTTP-запроса.  Чтобы просмотреть ответ, возвращенный сервером, измените запрос и нажмите кнопку **Отправить**.  

Вы также можете использовать **консоль сети** для создания и отправки HTTP-запросов непосредственно из DevTools.  

:::image type="complex" source="../../media/2020/06/experiments-network-console.msft.png" alt-text="Экспериментальная функция" lightbox="../../media/2020/06/experiments-network-console.msft.png":::
   Панель " **Сетевая консоль** "  
:::image-end:::  

> [!TIP]
> Чтобы увидеть **сетевую консоль** в главной панели \ (Top \), а не в [DevTools][DevtoolsCustomizeIndexDrawer], ознакомьтесь с разделами [Перемещение инструментов между панелями](#move-tools-between-panels).  

> [!NOTE]
> Чтобы включить эксперимент, ознакомьтесь со следующей командой [Включение экспериментальных функций][DevtoolsExperimentalFeaturesTurnOn] и установите флажок **включить сетевую консоль**.  
> 
> Откройте [Журнал сети][DevtoolsNetworkIndexLogActivity], откройте контекстное меню (щелкните правой кнопкой мыши и выберите команду **изменить и воспроизвести**).  

[#1093687][CR1093687] проблем с Chromium  

### События respondWith рабочего процесса на вкладке время  

Вкладка **время** на панели " **сеть** " теперь включает `respondWith` события рабочих процессов служб.  `respondWith`Событие "сотрудник службы" показывает продолжительность, начиная с момента, `fetch` когда обработчик событий сотрудника службы начнет выполняться до того момента, когда `respondWith` `fetch` будет сопоставлено обещание обработчика.  

:::image type="complex" source="../../media/2020/06/timing-tab.msft.png" alt-text="Экспериментальная функция" lightbox="../../media/2020/06/timing-tab.msft.png":::
   `respondWith`Событие "сотрудник службы" на вкладке " **время** " на панели " **сеть** "  
:::image-end:::  

Развернутый **ответ получен** , чтобы просмотреть дополнительные сведения из `fetch` ответа, например, `CacheStorageCacheName` `serviceWorkerResponseSource` и `ResponseTime` .  

:::image type="complex" source="../../media/2020/06/timing-tab2.msft.png" alt-text="Экспериментальная функция" lightbox="../../media/2020/06/timing-tab2.msft.png":::
   **Получен ответ на запрос** Expand для просмотра дополнительных сведений из `fetch` ответа  
:::image-end:::  

[#1066579][CR1066579] проблем с Chromium  

### Обратная связь по этой подсказке на панели "вопросы"  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Экспериментальная функция [вопросы][DevtoolsIssues] ".:::

:::image type="complex" source="../../media/2020/06/experiments-webhint.msft.png" alt-text="Экспериментальная функция" lightbox="../../media/2020/06/experiments-webhint.msft.png":::
   Обратная связь по этой подсказке на панели "вопросы"  
:::image-end:::  

> [!NOTE]
> Чтобы включить эксперимент, ознакомьтесь со следующей страницей [Включение экспериментальных функций][DevtoolsExperimentalFeaturesTurnOn] и установите флажок **включить подсказку**.  
> 
> Откройте панель " [проблемы][DevtoolsIssues] ", чтобы увидеть отзыв из подсказки.  

[#1070378][CR1070378] проблем с Chromium  

### Перемещение инструментов между панелями  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Экспериментальная функция":::
   Экспериментальная функция  
:::image-end:::  

Обычно такие инструменты, как **элементы** и **сеть** , можно открывать только на главной панели \ (Top \) DevTools.  Аналогичным образом такие инструменты, как **трехмерный вид** и **проблемы** , можно открывать только на панели ящик \ (Нижняя \) DevTools.  Теперь вы можете настраивать макет DevTools, перемещая инструменты между верхней и нижней панелями.  

:::image type="complex" source="../../media/2020/06/experiments-move-panels.msft.png" alt-text="Экспериментальная функция" lightbox="../../media/2020/06/experiments-move-panels.msft.png":::
   Перемещение вкладок между панелями  
:::image-end:::  

> [!NOTE]
> Чтобы включить эксперимент, ознакомьтесь со следующей страницей [Включение экспериментальных функций][DevtoolsExperimentalFeaturesTurnOn] и установите флажок **включить функцию поддержки для перемещения вкладок между панелями**.  

[#897944][CR897944] проблем с Chromium  

### Улучшенная всплывающая подсказка инициатора на панели "сеть"  

В Microsoft Edge 83 и 84 с помощью всплывающих подсказок для столбца инициаторов, в котором отображается причина запроса ресурсов, в [сетевом журнале][DevtoolsNetworkIndexLogActivity] отображается горизонтальная полоса прокрутки.  Вы можете видеть стек вызовов, который инициировал запрос, прокручивать по горизонтали в подсказке.  

:::image type="complex" source="../../media/2020/06/initiator-tooltip-84.msft.png" alt-text="Экспериментальная функция" lightbox="../../media/2020/06/initiator-tooltip-84.msft.png":::
   Всплывающая подсказка инициатора в Microsoft Edge 84  
:::image-end:::  

Начиная с Microsoft Edge 85, теперь вы можете видеть стек вызовов инициаторов в подсказке без горизонтальной прокрутки.  

:::image type="complex" source="../../media/2020/06/initiator-tooltip-85.msft.png" alt-text="Экспериментальная функция" lightbox="../../media/2020/06/initiator-tooltip-85.msft.png":::
   Всплывающая подсказка инициатора в Microsoft Edge 85
:::image-end:::  

[#1069404][CR1069404] проблем с Chromium  

## Объявления из проекта Chromium  

В следующих разделах описаны дополнительные возможности, доступные в Microsoft Edge 85, которые были задействованы в проекте Open Source Chromium.  

### Редактирование стилей для платформ CSS в JS  

Панель " **стили** " теперь обеспечивает улучшенную поддержку редактирования стилей, созданных с помощью API [объектной модели CSS (CSSOM)][CsswgDraftsCssom] .  Во многих платформах и библиотеках, использующих CSS из JS, для конструирования стилей используются API CSSOM в разделе "внутри".  

Теперь вы можете изменять стили, добавленные в JavaScript с помощью [построенных таблиц стилей][WicgConstructStylesheet].  Создаваемые таблицы стилей — это новый способ создания и распространения многократно используемых стилей при использовании [теневой модели DOM][MdnShadowDom].  

Например, стили, `h1` добавленные с помощью `CSSStyleSheet` \ (CSSOM API \), не были изменены ранее.  Теперь стили доступны для редактирования в области **стили** .  

:::image type="complex" source="../../media/2020/06/css-in-js.msft.png" alt-text="Экспериментальная функция" lightbox="../../media/2020/06/css-in-js.msft.png":::
   Изменение `background` свойства `h1` стиля, добавленного в значение `CSSStyleSheet` FROM `pink` `lightblue` .
:::image-end:::  

Придайте этой функции [пример с использованием CSS-in-JS][CodepenZoherghadyaliAbdgrpz].

[#946975][CR946975] проблем с Chromium  

### Lighthouse 6 на панели Lighthouse  

Панель **Lighthouse** теперь работает под управлением Lighthouse 6.  Полный список всех изменений можно найти в разделе [заметки о выпуске 6.0.0][GithubGoogleChromeLighthouse600].  

Lighthouse 6,0 предлагает три новые метрики для отчета: самую крупную краску \ (LCP \), интегральная схема сдвига \ (CLS \) и общее время блокировки \ (TBT \).  

Формула оценки производительности также была изменена в соответствии с тем, чтобы лучше понять процесс загрузки пользователя.  

[#772558][CR772558] проблем с Chromium  

#### Устаревшее изображение для первого осмысленного изображения  

Первый значащий графический редактор (FMP \ "\" \ "\") устарел в Lighthouse 6,0.  FMP также был удален из панели **Performance** .  **Самая крупная краска с содержимым** — Рекомендуемая замена для fmp.  <!--See [First Meaningful Paint][WebDevFirstMeaningfulPaint] for an explanation of why it was deprecated.  -->  

<!--todo: add Largest Contentful Paint when section available  -->  
<!--todo: add First Meaningful Paint link and note when available  -->  

[#1096008][CR1096008] проблем с Chromium  

### Поддержка новых функций JavaScript  

В DevTools теперь улучшена поддержка некоторых последних языковых функций JavaScript.  

:::row:::
   :::column span="1":::
      [Необязательное автозавершение цепочки цепочек][V8DevOptionalChaining]  
   :::column-end:::
   :::column span="2":::
      Автоматическое завершение свойств в **консоли** теперь поддерживает дополнительный синтаксис цепочек, например  `name?.` теперь он работает и в дополнение к нему `name.` `name[` .  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      Подсветка синтаксиса для [закрытых полей][V8DevClassFieldsPrivate]  
   :::column-end:::
   :::column span="2":::
      закрытые поля класса теперь правильно выделены синтаксисом и печатаются на панели « **источники** ».  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      Выделение синтаксиса для [непустого оператора слияния][V8DevNullishCoalescing]
   :::column-end:::
   :::column span="2":::
      DevTools правильно — печатает на панели « **источники** » оператор объединения без значений NULL.  
   :::column-end:::
:::row-end:::  

Проблемы с Chromium [#1073903][CR1073903], [#1083214][CR1083214] [#1083797][CR1083797]  

### Новые предупреждения о сочетаниях клавиш для приложения в области манифеста  

**Сочетания клавиш** для работы с приложениями помогают пользователям быстро запускать наиболее распространенные или Рекомендуемые задачи в веб-приложении.  

<!--todo: add App shortcuts when section is live  -->  

В области **манифеста** отображаются предупреждения для указанных ниже условий.  

* Значки сочетаний клавиш приложения меньше 96x96 пикселей  
* Значки сочетаний клавиш приложения и манифеста не квадратны \ (так как значки игнорируются)  

:::image type="complex" source="../../media/2020/06/app-shortcut-warnings.msft.png" alt-text="Экспериментальная функция" lightbox="../../media/2020/06/app-shortcut-warnings.msft.png":::
   Предупреждения о сочетаниях клавиш для приложения  
:::image-end:::  

[#955497][CR955497] проблем с Chromium  

### Последовательная отображение вычисляемой области  

**Вычисляемая** область на панели " **элементы** " теперь отображается единообразно в виде области на всех размерах окна просмотра.  Ранее **Вычисляемая** область была объединена в области " **стили** ", когда ширина окна просмотра DevTools была узкой.  

:::image type="complex" source="../../media/2020/06/computed-pane.msft.png" alt-text="Экспериментальная функция" lightbox="../../media/2020/06/computed-pane.msft.png":::
   **Вычисляемая** область последовательно отображается как отдельная область, даже если DevTools узким.
:::image-end:::  

[#1073899][CR1073899] проблем с Chromium  

### Смещения байт-кода для файлов сборки  

DevTools теперь использует смещения байт-кода для отображения номеров строк Wasm дизассемблированного кода.  
Номера строк упрощают просмотр двоичных данных и более последовательную работу, так как среда выполнения Wasm ссылается на расположение.  

[#1071432][CR1071432] проблем с Chromium  

### Построчное копирование и вырезание на панели «источники»  

При копировании или вырезании без выделения в [редакторе палитры «источники][DevtoolsSourcesEditCssJavascript]» DevTools копирует или вырезает текущую строку содержимого.  

:::image type="complex" source="../../media/2020/06/line-wise-cut.msft.png" alt-text="Экспериментальная функция" lightbox="../../media/2020/06/line-wise-cut.msft.png":::
   С курсором в конце строки 5 копируется вся строка из **pen.js** в DevTools и вставляется в [код Visual Studio][VSCode].
:::image-end:::  

[#800028][CR800028] проблем с Chromium

### Обновления параметров консоли  

#### Разгруппирование одинаковых сообщений консоли  

Для повторяющихся сообщений **Группа одинаковый** переключатель в разделе Параметры консоли будет применена.  Ранее она была применена к аналогичным сообщениям.  

Например, ранее DevTools не разгруппирование сообщений, несмотря на то, что `hello` флажок **Group похоже** не установлен.  Теперь `hello` сообщения разгруппированы.  

:::image type="complex" source="../../media/2020/06/ungroup-similar.msft.png" alt-text="Экспериментальная функция" lightbox="../../media/2020/06/ungroup-similar.msft.png":::
   Если флажок " **Группировать как** " не установлен, `hello` сообщения разносятся в разгруппирование
:::image-end:::  

Придайте этой функции [пример, который отправляет на консоль повторяющиеся сообщения][CodepenZoherghadyaliZyrjgdJ].  

[#1082963][CR1082963] проблем с Chromium  

### Сохранение только выбранных контекстных параметров  

**Выбранный контекст** теперь сохраняется только в параметрах консоли.  Ранее параметры были сброшены каждый раз при закрытии и повторном открытии DevTools.  Изменение приводит к поведению параметров с другими параметрами консоли.  

:::image type="complex" source="../../media/2020/06/selected-context.msft.png" alt-text="Экспериментальная функция" lightbox="../../media/2020/06/selected-context.msft.png":::
   Параметр " **только выбранный контекст** "  
:::image-end:::  

[#1055875][CR1055875] проблем с Chromium  

### Обновления панели "производительность"  

#### Информация кэша компиляции для JavaScript на панели "производительность"  

[Данные кэша компиляции для JavaScript][V8DevCodeCaching] теперь всегда отображаются на вкладке "Сводка" на панели "производительность".  Ранее DevTools не показывает ничего, связанного с кэшированием кода, если кэширование кода не произошло.  

:::image type="complex" source="../../media/2020/06/js-compilation-cache.msft.png" alt-text="Экспериментальная функция" lightbox="../../media/2020/06/js-compilation-cache.msft.png":::
   Данные кэша компиляции для JavaScript  
:::image-end:::  

[#912581][CR912581] проблем с Chromium  

#### Выравнивание времени навигации на панели «производительность»  

Панель **производительности** , используемая для отображения времени на линейках на основе начала записи.  Время ожидания изменилось для записей, в которых пользователь осуществляет переход, где DevTools теперь показывает время линейки относительно навигации.  

:::image type="complex" source="../../media/2020/06/nav-timing.msft.png" alt-text="Экспериментальная функция" lightbox="../../media/2020/06/nav-timing.msft.png":::
   Выравнивание времени навигации на панели « **производительность** »  
:::image-end:::  

Время, для которого `DOMContentLoaded` Первая краска, первая краска и наибольшее количество событий, связанных с содержимым, обновляется в соответствии с началом навигации, а это значит, что время соответствует значению времени, указанное в `PerformanceObserver` .  

[#974550][CR974550] проблем с Chromium  

### Новые значки для точек останова, условных точек останова и logpoints  

На панели « **источники** » есть новые дизайны для точек останова, условных точек останова и logpoints.  Точки останова представлены на красном круге, точно так же, как и в [Visual Studio][VSCode] , и в [Visual Studio][VS].  Значки добавляются для различения условных точек останова и logpoints.  

:::image type="complex" source="../../media/2020/06/breakpoints.msft.png" alt-text="Экспериментальная функция" lightbox="../../media/2020/06/breakpoints.msft.png":::
   Точки останова  
:::image-end:::  

[#1041830][CR1041830] проблем с Chromium  

## Загрузка каналов предварительной версии Microsoft Edge  

Если вы используете Windows или macOS, рассматривайте в качестве браузера по умолчанию использование [каналов предварительного просмотра Microsoft Edge][MicrosoftEdgePreviewChannels] .  Каналы предварительного просмотра предоставляют доступ к последним функциям DevTools.  

## Знакомство с Microsoft Edge DevTools Team  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DevtoolsMain]: /microsoft-edge/devtools-guide-chromium "Инструменты разработчика Microsoft EDGE (Chromium) | Документы Microsoft"  
[DevtoolsCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu "Выполнение команд с помощью командного меню Microsoft Edge DevTools | Документы Microsoft"
[DevtoolsCustomizeIndexDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Ящик — настройка Microsoft Edge DevTools | Документы Microsoft"
[DevtoolsExperimentalFeaturesTurnOn]: /microsoft-edge/devtools-guide-chromium/experimental-features#turn-on-experimental-features "Включите экспериментальные функции — экспериментальные функции | Документы Microsoft"  
[DevtoolsIssues]: /microsoft-edge/devtools-guide-chromium/issues "Поиск и устранение проблем с помощью средства Microsoft Edge DevTools "вопросы" | Документы Microsoft"
[DevtoolsSourcesEditCssJavascript]: /microsoft-edge/devtools-guide-chromium/sources#edit-css-and-javascript "Общие сведения об панели редактирования CSS и JavaScript-sources | Документы Microsoft"  
[DevtoolsNetworkIndexLogActivity]: /microsoft-edge/devtools-guide-chromium/network/index#log-network-activity "Регистрация активности сети — проверка активности сети в Microsoft Edge DevTools | Документы Microsoft"

[CodepenZoherghadyaliAbdgrpz]: https://codepen.io/zoherghadyali/full/abdGrPZ "Редактирование стилей для платформ CSS-JS | CodePen"
[CodepenZoherghadyaliZyrjgdJ]: https://codepen.io/zoherghadyali/full/zYrjgdJ "Отправлять повторяющиеся сообщения на консоль | CodePen"
[CodepenRachelweilYzwBzKM]: https://codepen.io/hxlnt/full/YzwBzKM "Пример планировщика сетки CSS | CodePen"

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Ошибки Chromium"  

[CR772558]: https://crbug.com/772558 "DevTools: обновление до последней версии Lighthouse | Ошибки Chromium"  
[CR800028]: https://crbug.com/800028 "Повторяющийся ярлык строки в редакторе средств разработчика не работает после обновления Chrome | Ошибки Chromium"  
[CR912581]: https://crbug.com/912581 "Предоставление сценариев, которые были бы кэшированы в коде с помощью V8 в DevTools/about: Tracing | Ошибки Chromium"  
[CR946975]: https://crbug.com/946975 "Боковая панель "стили DevTools" не работает с сконструированными таблицами стилей | Ошибки Chromium"  
[CR955497]: https://crbug.com/955497 "Контекстное меню значка приложения для PWAs | Ошибки Chromium"  
[CR974550]: https://crbug.com/974550 "Несоответствие метрик между панелью производительности и performanceObserver | Ошибки Chromium"  
[CR1041830]: https://crbug.com/1041830 "Улучшение цветопередачи для точек останова | Ошибки Chromium"  
[CR1055875]: https://crbug.com/1055875 "Значение выбранного контекста параметр консоли не сохраняется после закрытия и повторного открытия средств разработчика | Ошибки Chromium"  
[CR1066579]: https://crbug.com/1066579 "DevTools: Показать ServiceWorkers выбор временной шкалы для запроса на панели "сеть" | Ошибки Chromium"  
[CR1071432]: https://crbug.com/1071432 "Базовые возможности для разработчиков Wasm | Ошибки Chromium"  
[CR1073899]: https://crbug.com/1073899 "Вкладка "вычисляемый стиль" исчезает в режиме отклика | Ошибки Chromium"  
[CR1073903]: https://crbug.com/1073903 "DevTools: выделение синтаксических конструкций не работает с закрытыми полями | Ошибки Chromium"  
[CR1082963]: https://crbug.com/1082963 "Не удается отключить поведение группировки аналогичных сообщений в консоли | Ошибки Chromium"  
[CR1083214]: https://crbug.com/1083214 "Acorn не поддерживает дополнительное объединение | Ошибки Chromium"  
[CR1083797]: https://crbug.com/1083797 "Неправильное распечатка для ненулевого объединения | Ошибки Chromium"  
[CR1096008]: https://crbug.com/1096008 "Удалить FMP | Ошибки Chromium"  
[CR1047356]: https://crbug.com/1047356 "Сетка CSS/гибкая таблица/подсказка для таблиц | Ошибки Chromium"  
[CR1093687]: https://crbug.com/1093687 "Инструмент "создать" для создания и воспроизведения запросов виртуальных сетей | Ошибки Chromium"  
[CR1070378]: https://crbug.com/1070378 "Интегрировать подсказку в DevTools | Ошибки Chromium"  
[CR1069404]: https://crbug.com/1069404 "[Средства разработки] всплывающие элементы мини-приложения слишком узкие | Ошибки Chromium"  
[CR897944]: https://crbug.com/897944 "Перетаскиваемые панели DevTool | Ошибки Chromium"

[GithubGoogleChromeLighthouse600]: https://github.com/GoogleChrome/lighthouse/releases/tag/v6.0.0 "v 6.0.0-GoogleChrome/Lighthouse | GitHub"  

[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=[DevTools%20Docs%20Feedback] "Новая ошибка — MicrosoftDocs/Edge-разработчик"  

[MdnShadowDom]: https://developer.mozilla.org/docs/Web/Web_Components/Using_shadow_DOM "Использование теневой модели DOM | MDN"

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download/ "Каналы предварительной версии Microsoft Edge"  

[VS]: https://visualstudio.microsoft.com/ "Visual Studio"
[VSCode]: https://code.visualstudio.com/ "Код Visual Studio"  

[CsswgDraftsCssom]: https://drafts.csswg.org/cssom "Объектная модель CSS (CSSOM) | Черновики редакторов рабочих групп W3C CSS"  

[PostTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Публикация твита"  
[EdgeDevToolsTwitterAccount]: https://twitter.com/EdgeDevTools "@EdgeDevTools учетной записи Twitter"  

[V8DevClassFieldsPrivate]: https://v8.dev/features/class-fields#private-class-fields "Закрытые поля класса — открытые и закрытые поля класса | V8. Разработки"  
[V8DevCodeCaching]: https://v8.dev/blog/code-caching-for-devs "Кэширование кода для разработчиков JavaScript | V8. Разработки"  
[V8DevNullishCoalescing]: https://v8.dev/features/nullish-coalescing "Ненулевое объединение | V8. Разработки"  
[V8DevOptionalChaining]: https://v8.dev/features/optional-chaining "Дополнительные сцепления | V8. Разработки"  

[WebhintMain]: https://webhint.io "Подсказка"  

[WicgConstructStylesheet]: https://wicg.github.io/construct-stylesheets/ "Объекты стилей, которые вы создаете? Веб-Incubator CG"

<!--[WebDevLighthouseWhatsNew60]: https://web.dev/lighthouse-whats-new-6.0 "What's New in Lighthouse 6.0 | Web.Dev"  -->  
<!--[WebDevVitalsCoreWeb]: https://web.dev/vitals#core-web-vitals "Core Web Vitals - Web Vitals | Web.Dev"  -->  
<!--[WebdevAppShortcuts]: https://alphabet-dev/app-shortcuts "Get things done quickly with app shortcuts | alphabet-dev"  -->  
<!--[WebdevCls]: https://alphabet-dev/cls "Cumulative Layout Shift (CLS) | alphabet-dev"  -->  
<!--[WebdevControlFocus]: https://alphabet-dev/control-focus-with-tabindex "Control focus with tabindex | alphabet-dev"  -->  
<!--[WebdevMeasureSpeedLabField]: https://alphabet-dev/how-to-measure-speed#lab-data-vs-field-data "Lab data vs Field data - How to measure speed? | alphabet-dev"  -->  
<!--[WebdevLabelsText]: https://alphabet-dev/labels-and-text-alternatives "Labels and text alternatives | alphabet-dev"  -->  
<!--[WebdevTbt]: https://alphabet-dev/tbt "Total Blocking Time (TBT) | alphabet-dev"  -->  
<!--[WebFundamentalComponentsShadowdom]: /web/fundamentals/web-components/shadowdom  -->  
<!--[WebDevLcp]: https://web.dev/lcp "Largest Contentful Paint (LCP) | Web.Dev"  -->  
<!--[WebDevFirstMeaningfulPaint]: https://web.dev/first-meaningful-paint "First Meaningful Paint | Web.Dev"  -->  
<!--[WhatsNew201902ConstructableStylesheets]: ../../2019/02/constructable-stylesheets.md "Constructable Stylesheets: seamless reusable styles | Microsoft Docs"  -->  

[TheWebWeWant]: https://webwewant.fyi/ "Требуемый веб-сайт"  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница [будет найдена, и](https://developers.google.com/web/updates/2020/06/devtools/index) ее можно создать с помощью [Jecelyn Yeen][JecelynYeen] \ (разработчик отвечает, Chrome DevTools \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
