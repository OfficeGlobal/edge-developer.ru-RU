---
description: Эмуляция концепции deficiencies, закрепление слева в меню команд и т. д.
title: Новые возможности DevTools (Microsoft Edge 83)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: f9eb306ab7b30495c91ff4a70797898459d7e722
ms.sourcegitcommit: b337717957529239434b4e8e1e167aebf0543518
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/15/2020
ms.locfileid: "11015484"
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

# Новые возможности DevTools (Microsoft Edge 83)  

Согласно обновленному календарному плану Chromium мы настраивая наше расписание для предстоящих выпусков Microsoft EDGE и отменив выпуск Microsoft Edge 82. Дополнительные сведения находятся в записи [блога][WindowsBlogStableRelease] .  

Ниже описаны новые возможности, доступные в DevTools в Microsoft Edge 83.  

## Объявления из группы Microsoft Edge DevTools  

В следующих разделах представлен список извещений, которые вы могли не получить в Microsoft Edge DevTools Teams! Узнайте, как использовать новые функции в DevTools, расширения кода Visual Studio и многое другое.  Чтобы оставаться на связи с самыми последними и более свежими возможностями, скачайте на веб – [каналы предварительной версии Microsoft Edge][MicrosoftEdgePreviewChannels] и [следуйте указаниям Twitter][EdgeDevToolsTwitterAccount].  

### Удаленная отладка Microsoft EDGE на устройствах с Windows 10  

Приложение [Remote Tools для Microsoft Edge \ (бета-версия)][RemoteTools] теперь доступно в [магазине Microsoft Store][MicrosoftStore].  С помощью этого приложения, которое расширяет [портал устройств Windows][WindowsUwpDebugTestPerfDevicePortal], вы можете подключаться из экземпляра Microsoft EDGE, запущенного на компьютере разработки, на удаленное устройство с Windows 10, просмотреть список конечных объектов \ (все вкладки в Microsoft EDGE и [PWAs][PprgressiveWebAppsChromiumIndex] открыть на устройстве с Windows 10 \) и использовать DevTools на своем компьютере для разработки по отношению к целевому объекту на удаленном устройстве с Windows 10.  

:::image type="complex" source="../../media/2020/03/remote-tools.msft.png" alt-text="Приложение Remote Tools для Microsoft EDGE (бета-версия), доступное в Microsoft Store" lightbox="../../media/2020/03/remote-tools.msft.png":::
   Приложение [Remote Tools для Microsoft EDGE (бета-версия)][RemoteTools] , доступное в [Microsoft Store][MicrosoftStore]  
:::image-end:::  

[Ознакомьтесь с руководством по настройке устройства с Windows 10 и компьютера для разработки удаленной отладки][DevtoolsRemoteDebuggingWindows].  Сообщите нам об удаленной отладке, выполнив [твит][PostTweetEdgeDevTools] или щелкнув значок " [Отправить отзыв](#getting-in-touch-with-microsoft-edge-devtools-team) "!  

### Новые способы доступа к параметрам  

Существует множество параметров для DevTools, которые можно настроить таким образом, чтобы DevTools внешний вид, оформление и работу. В Microsoft Edge 83 доступ к [параметрам][DevtoolsCustomizeIndexSettings] в DevTools теперь стал более простым. Откройте параметры с помощью значка шестеренки рядом с пунктом оповещения консоли и главное меню.  

:::image type="complex" source="../../media/2020/03/settings.msft.png" alt-text="Приложение Remote Tools для Microsoft EDGE (бета-версия), доступное в Microsoft Store" lightbox="../../media/2020/03/settings.msft.png":::
   Значок шестеренки, чтобы открыть **Параметры** в DevTools  
:::image-end:::  

Вы также можете открыть [Параметры][DevtoolsCustomizeIndexSettings] из **главного меню** в разделе **Дополнительные инструменты**.

:::image type="complex" source="../../media/2020/03/settings2.msft.png" alt-text="Приложение Remote Tools для Microsoft EDGE (бета-версия), доступное в Microsoft Store" lightbox="../../media/2020/03/settings2.msft.png":::
   **Главное меню**  >  **Дополнительные инструменты**  >  **Параметры**  
:::image-end:::  

[#1050855][CR1050855] проблем с Chromium

### Новые и улучшенные infobars

В DevTools теперь есть улучшенные возможности, которые появятся на панелях уведомлений \ (infobars \) на информационной панели. В Microsoft Edge 83 infobars более удобны для чтения и предоставляют кнопки, чтобы можно было принять нужное действие прямо сейчас.  

:::image type="complex" source="../../media/2020/03/infobar.msft.png" alt-text="Приложение Remote Tools для Microsoft EDGE (бета-версия), доступное в Microsoft Store" lightbox="../../media/2020/03/infobar.msft.png":::
   Информационная панель для печати файла minified в Microsoft Edge версии 83  
:::image-end:::  

[#1056348][CR1056348] проблем с Chromium

### Навигация в окне выбора цвета с помощью клавиатуры  

[Палитра цветов][DevtoolsCssReferenceColorPicker] — это графический интерфейс пользователя на [панели «элементы»][DevtoolsCssIndex] для изменения `color` и `background-color` объявлений.  В предыдущих версиях Microsoft Edge вы не смогли перемещаться по разделу " **тени** " в [палитре цветов][DevtoolsCssReferenceColorPicker] с помощью клавиатуры.  

:::image type="complex" source="../../media/2020/03/color-picker.msft.png" alt-text="Приложение Remote Tools для Microsoft EDGE (бета-версия), доступное в Microsoft Store" lightbox="../../media/2020/03/color-picker.msft.png":::
   Теперь вы можете использовать клавиатуру для перемещения селектора в разделе " **тени** " [палитры цветов][DevtoolsCssReferenceColorPicker]  
:::image-end:::  

В Microsoft Edge 83 теперь можно использовать клавиатуру для перемещения селектора в разделе **тени** окна выбора цвета.  

[#963183][CR963183] проблем с Chromium  

### Вкладка "Свойства" теперь заполняется после обновления страницы  

В Microsoft Edge 81 и более ранних версий **вкладка Свойства** на [панели элементы][DevtoolsCssIndex] была разорвана обновлениями страницы.  После обновления страницы на **вкладке Свойства** не заполнятся свойства элемента, выбранного в данный момент.  

:::image type="complex" source="../../media/2020/03/properties-in-81.msft.png" alt-text="Приложение Remote Tools для Microsoft EDGE (бета-версия), доступное в Microsoft Store" lightbox="../../media/2020/03/properties-in-81.msft.png":::
   В Microsoft Edge 81 и более ранних версий **вкладка Свойства** была пуста после обновления страницы  
:::image-end:::  

В Microsoft Edge 83 теперь вы можете видеть свойства элемента, выбранного в данный момент, после обновления страницы на **вкладке Свойства**.  

:::image type="complex" source="../../media/2020/03/properties-in-82.msft.png" alt-text="Приложение Remote Tools для Microsoft EDGE (бета-версия), доступное в Microsoft Store" lightbox="../../media/2020/03/properties-in-82.msft.png":::
   В Microsoft Edge 83 на **вкладке Свойства** отображаются свойства элемента, выбранного в данный момент, после обновления страницы.  
:::image-end:::  

[#1050999][CR1050999] проблем с Chromium  

### Используйте клавиши со стрелками для прокрутки в инструменте "изменения"  

**Средство "изменения** " отслеживает все изменения, внесенные в CSS или JavaScript, в DevTools.  Вы можете использовать **средство "изменения** ", чтобы быстро просмотреть все изменения и вернуть их в редактор или интегрированную среду разработки.  

Откройте **инструмент "изменения** ", нажав `Ctrl` + `Shift` + `P` в DevTools, чтобы открыть [меню команд][DevToolsCommandMenuIndex] и ввести текст `changes` .  Выберите и запустите команду **Показать изменения** , чтобы открыть **средство "изменения** " в DevToolsном ящике.  

После внесения изменений в файл minified **инструмент "изменения** " позволяет выполнить горизонтальную прокрутку для просмотра всего кода minified.  Начиная с Microsoft Edge 83, теперь можно прокручивать по горизонтали с помощью клавиш со стрелками на клавиатуре.  

:::image type="complex" source="../../media/2020/03/changes.msft.png" alt-text="Приложение Remote Tools для Microsoft EDGE (бета-версия), доступное в Microsoft Store" lightbox="../../media/2020/03/changes.msft.png":::
   В Microsoft Edge 83 вы можете выполнить горизонтальную прокрутку с помощью клавиш со стрелками, чтобы просмотреть изменения, внесенные в код minified в **инструменте "изменения** ".  
:::image-end:::  

Если вы используете средства чтения с экрана или клавиатуру для навигации по DevTools, отправьте нам свой отзыв, выполнив [твит][PostTweetEdgeDevTools] в США или щелкнув значок [Отправить отзыв](#getting-in-touch-with-microsoft-edge-devtools-team) !  

[#963183][CR963183] проблем с Chromium  

## Объявления из проекта Chromium  

В следующих разделах описаны дополнительные возможности, доступные в Microsoft Edge 83, которые были задействованы в проекте Open Source Chromium.  

### Эмуляция видения deficiencies  

Откройте [вкладку рендеринг][DevtoolsEvaluatePreformanceReferenceAnalyzeRenderingTab] и воспользуйтесь новой функцией **эмуляции deficiencies** , чтобы лучше понять, как люди с разными типами концепций deficienciesют свой сайт.  

:::image type="complex" source="../../media/2020/03/vision.msft.png" alt-text="Приложение Remote Tools для Microsoft EDGE (бета-версия), доступное в Microsoft Store" lightbox="../../media/2020/03/vision.msft.png":::
   Имитация размытого видения  
:::image-end:::  

DevTools может эмулировать размытое видение и следующие [типы концепций цветопередачи deficiencies][ColorBlindnessTypes].  

| Некоторая концепция цвета | Сведения |  
|:--- |:--- |  
| Protanopia | Невозможность воспринимать красный индикатор. |  
| Deuteranopia | Невозможность воспринимать зеленый свет. |  
| Tritanopia | Невозможность воспринимать любой синий индикатор. |  
| Achromatopsia | Невозможность воспринимать любой цвет, за исключением оттенков серого \ (очень редких). |  

Ниже указаны менее экстремальные версии deficiencies, и в действительности они являются более распространенными.  
Например, Protanomaly — это уменьшенная чувствительность к красному свету (в отличие от Protanopia, что является полноценным невозможностью воспринимать красный свет). Тем не менее, omaly концепция deficiencies не так четко: каждый человек, имеющий такой интерес, отличается от того, кто имеет такой же интерес, и может по-разному видеть различные варианты (которые могут выпустить больше или меньше подходящих цветов).  

Благодаря разработке для более экстремальных эмуляций в DevTools веб-приложения будут гарантированно доступны людям с protanomaly, Deuteranomaly, Tritanomaly и achromatomaly.  

Отправьте отзыв, выполнив [твит][PostTweetEdgeDevTools] или щелкнув значок " [Отправить отзыв](#getting-in-touch-with-microsoft-edge-devtools-team) "!  

[#1003700][CR1003700] проблем с Chromium  

### Эмуляция языков  

Эмуляция региональных стандартов путем задания местоположения в **Sensors**  >  **расположениях**датчиков. [Открыть **меню команд** ][DevToolsCommandMenuIndex] и ввести текст `Sensors` для доступа к вкладке **Sensors (датчики** ).  После выполнения этих действий DevTools изменяет текущий языковой стандарт по умолчанию, влияя на приведенный ниже код.  

*   `Intl.*` API, например: `new Intl.NumberFormat().resolvedOptions().locale`  
*   Другие API JavaScript, поддерживающие национальные настройки `String.prototype.localeCompare` , такие как и `*.prototype.toLocaleString` , например: `123_456..toLocaleString()`  
*   API DOM, например `navigator.language` и `navigator.languages`  
*   Заголовок HTTP-запроса для [приема на языке][MDNAcceptLanguage]  

> [!NOTE]
> Обновляются `navigator.language` и `navigator.languages` не отображаются немедленно, но только после следующей навигации или обновления страницы.  Изменения в `Accept-Language` заголовке HTTP отражаются только для последующих запросов.  

:::image type="complex" source="../../media/2020/03/locale.msft.png" alt-text="Приложение Remote Tools для Microsoft EDGE (бета-версия), доступное в Microsoft Store" lightbox="../../media/2020/03/locale.msft.png":::
   Эмуляция языкового стандарта  
:::image-end:::  

Чтобы попробовать посмотреть демонстрацию, ознакомьтесь с [примером кода, зависящим от языкового стандарта][MathiasByensLocaleDemo].

[#1051822][CR1051822] проблем с Chromium

### Отладка политики встраивания по началу (COEP)  

На панели Network (сеть) теперь представлена отладочная информация о [политике встраивания][COEP] .  

Столбец **Status** теперь содержит краткое описание причины блокировки запроса, а также ссылку на просмотр заголовков этого запроса для дальнейшей отладки.  

:::image type="complex" source="../../media/2020/03/status.msft.png" alt-text="Приложение Remote Tools для Microsoft EDGE (бета-версия), доступное в Microsoft Store" lightbox="../../media/2020/03/status.msft.png":::
   Заблокированные запросы в столбце " **состояние** "  
:::image-end:::  

В разделе **заголовки ответа** вкладки **заголовки** содержатся дополнительные инструкции по устранению проблем.  

:::image type="complex" source="../../media/2020/03/guidance.msft.png" alt-text="Приложение Remote Tools для Microsoft EDGE (бета-версия), доступное в Microsoft Store" lightbox="../../media/2020/03/guidance.msft.png":::
   Другие рекомендации в разделе " **заголовки ответа** "  
:::image-end:::  

Отправьте отзыв, выполнив [твит][PostTweetEdgeDevTools] или щелкнув значок " [Отправить отзыв](#getting-in-touch-with-microsoft-edge-devtools-team) "!  

[#1051466][CR1051466] проблем с Chromium  

### Новые значки для точек останова, условных точек останова и logpoints  

На панели «источники» есть новые значки для точек останова, условных точек останова и logpoints:  

*   Точки останова \ (![Точкой](../../media/2020/03/breakpoint.msft.png)\) представлены красными кружками.  
*   Условные точки останова \ (![Условная точка останова](../../media/2020/03/conditional.msft.png)\) представлены в виде кружков из половины белых.  
*   Logpoints \(![Logpoint](../../media/2020/03/logpoint.msft.png)\) представлены красными кружками с помощью значков консоли.  

Мотивация для новых значков — сделать пользовательский интерфейс более подродным с помощью других средств отладки графического интерфейса (обычно это цветовые точки останова), чтобы облегчить различение трех функций.  

[#1041830][CR1041830] проблем с Chromium  

### Просмотр сетевых запросов, заданных для определенного пути к файлу cookie  

С помощью нового `cookie-path` ключевого слова фильтра на панели **Network (сеть** ) можно сосредоточиться на запросах в сети, которые задают определенный [путь к файлу cookie][MDNCookiePath].  

Изучите [запросы фильтра по свойствам][DevtoolsNetworkReferenceFilterRequestsProperties] , чтобы найти другие ключевые слова, такие как `cookie-path` .

### Закрепить слева от меню команд  

Откройте [меню команд][DevToolsCommandMenuIndex] и выполните команду, `Dock to left` чтобы переместить DevTools в левой части окна просмотра.  

:::image type="complex" source="../../media/2020/03/dock-to-left.msft.png" alt-text="Приложение Remote Tools для Microsoft EDGE (бета-версия), доступное в Microsoft Store" lightbox="../../media/2020/03/dock-to-left.msft.png":::
   DevTools закреплен в левой части окна просмотра  
:::image-end:::  

> [!NOTE]
> Функция " **прикрепить к левому краю** " была доступна после выпуска Microsoft Edge 75, но ранее она была доступна только в [главном меню][DevtoolsCustomizePlacementsChangeMainMenu].  Новая функция в Microsoft Edge 83 — теперь вы можете получить доступ к этой функции в меню команд.  

Отправьте отзыв, выполнив [твит][PostTweetEdgeDevTools] или щелкнув значок " [Отправить отзыв](#getting-in-touch-with-microsoft-edge-devtools-team) "!  

[#1011679][CR1011679] проблем с Chromium  

### Панель "Аудит" теперь является панелью Lighthouse  

Группа DevTools часто получила отзыв от веб-разработчиков, которые могли бы запустить [Lighthouse][GithubGoogleChromeLighthouse] из DevTools, когда они могли бы не найти панель "Lighthouse", и панель **аудиторий** стала на панели " **Lighthouse** ".  

:::image type="complex" source="../../media/2020/03/lighthouse.msft.png" alt-text="Приложение Remote Tools для Microsoft EDGE (бета-версия), доступное в Microsoft Store" lightbox="../../media/2020/03/lighthouse.msft.png":::
   Панель Lighthouse  
:::image-end:::  

> [!NOTE]
> Панель **Lighthouse** содержит ссылки на содержимое, размещенное на сторонних веб-сайтах.  Корпорация Майкрософт не несет ответственности за содержимое этих сайтов и любые данные, которые могут быть собраны, и не может управлять ими.  

### Удаление всех локальных переопределений в папке  

После настройки **локальных переопределений** вы можете щелкнуть папку правой кнопкой мыши и выбрать команду создать **все переопределение** для удаления всех локальных переопределений в этой папке.  

:::image type="complex" source="../../media/2020/03/overrides.msft.png" alt-text="Приложение Remote Tools для Microsoft EDGE (бета-версия), доступное в Microsoft Store" lightbox="../../media/2020/03/overrides.msft.png":::
   Удаление всех переопределений  
:::image-end:::  

Отправьте отзыв, выполнив [твит][PostTweetEdgeDevTools] или щелкнув значок " [Отправить отзыв](#getting-in-touch-with-microsoft-edge-devtools-team) "!  

[#1016501][CR1016501] проблем с Chromium  

### Обновленный пользовательский интерфейс длительных задач  

**Длинная задача** — это код JavaScript, который занимает много времени, что приводит к закреплениям веб-страницы.  

На панели производительности вы можете [визуализировать длинные задачи][DevtoolsEvaluatePerformanceReferenceViewMainThreadActivity] , но в Microsoft Edge 83 пользовательский интерфейс визуализации задач на панели производительности обновлен.  Область задач "Долгая задача" теперь окрашена на красный фон с чередованием.  

:::image type="complex" source="../../media/2020/03/long-task.msft.png" alt-text="Приложение Remote Tools для Microsoft EDGE (бета-версия), доступное в Microsoft Store" lightbox="../../media/2020/03/long-task.msft.png":::
   Новый пользовательский интерфейс длительной задачи  
:::image-end:::  

Отправьте отзыв, выполнив [твит][PostTweetEdgeDevTools] или щелкнув значок " [Отправить отзыв](#getting-in-touch-with-microsoft-edge-devtools-team) "!  

[#1054447][CR1054447] проблем с Chromium  

### Поддержка маскированных значков в области манифеста  

В Oreo Android появились адаптивные значки, которые отображают значки приложений в различных моделях устройств.  **Маскированные значки** — это новый формат значков, поддерживающий адаптивные значки, которые позволяют убедиться, что на устройствах, поддерживающих стандарт маскированных значков, будет хорошо выглядеть значок [PWA][PprgressiveWebAppsChromiumIndex] .  

Установите флажок **Показывать только минимальную безопасную область для маскированных значков** в области **манифеста** , чтобы убедиться в том, что маскирующий значок хорошо подходит для устройств с Android Oreo.  

<!-- Check out [Are my current icons ready?] to learn more.  -->  

:::image type="complex" source="../../media/2020/03/maskable-icons.msft.png" alt-text="Приложение Remote Tools для Microsoft EDGE (бета-версия), доступное в Microsoft Store" lightbox="../../media/2020/03/maskable-icons.msft.png":::
   Флажок **Показать только минимальную безопасную область для маскированных значков**  
:::image-end:::  

> [!NOTE]
> Этот компонент запущен в Microsoft Edge 81.  Обновления, описанные здесь в Microsoft Edge 83, не были освещены в статье [новые возможности DevTools (Microsoft Edge 81)][WhatsNew81].  

## Загрузка каналов предварительной версии Microsoft Edge  

Если вы используете Windows или macOS, рассматривайте в качестве браузера по умолчанию использование [каналов предварительного просмотра Microsoft Edge][MicrosoftEdgePreviewChannels] .  Каналы предварительного просмотра предоставляют доступ к последним функциям DevTools.  

## Знакомство с Microsoft Edge DevTools Team  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[WhatsNew81]: ../01/devtools.md "Новые возможности DevTools (Microsoft Edge 81) | Документы Microsoft"  

[DevToolsCommandMenuIndex]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Выполнение команд с помощью командного меню Microsoft Edge DevTools | Документы Microsoft"  
[DevtoolsCssReferenceColorPicker]: /microsoft-edge/devtools-guide-chromium/css/reference#change-colors-with-the-color-picker "Изменение цвета с помощью средства выбора цвета | Документы Microsoft"  
[DevtoolsCssIndex]: /microsoft-edge/devtools-guide-chromium/css/index "Начало просмотра и изменения CSS | Документы Microsoft"  
[DevtoolsCustomizePlacementsChangeMainMenu]: /microsoft-edge/devtools-guide-chromium/customize/placement#change-placement-from-the-main-menu "Изменение положения в главном меню | Документы Microsoft"  
[DevtoolsEvaluatePerformanceReferenceViewMainThreadActivity]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#view-main-thread-activity "Просмотр основного действия потока | Документы Microsoft"  
[DevtoolsEvaluatePreformanceReferenceAnalyzeRenderingTab]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#analyze-rendering-performance-with-the-rendering-tab "Анализ производительности отрисовки с помощью вкладки "рендеринг" | Документы Microsoft"  
[PprgressiveWebAppsChromiumIndex]: /microsoft-edge/progressive-web-apps-chromium/index "Прогрессивные веб-приложения в Windows | Документы Microsoft"  
[DevtoolsRemoteDebuggingWindows]: /microsoft-edge/devtools-guide-chromium/remote-debugging/windows "Начало работы с удаленной отладкой на устройствах с Windows 10 | Документы Microsoft"  
[DevtoolsJavascriptBreakpointsLineCode]: /microsoft-edge/devtools-guide-chromium/javascript/breakpoints#line-of-code-breakpoints "Точки останова по строке кода: как приостановить выполнение кода с точки останова в Microsoft Edge DevTools | Документы Microsoft"
[DevtoolsNetworkReferenceFilterRequestsProperties]: /microsoft-edge/devtools-guide-chromium/network/reference#filter-requests-by-properties "Фильтрация запросов по свойствам-Справка по анализу сети | Документы Microsoft"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Параметры: Настройка Microsoft Edge DevTools | Документы Microsoft"  

[WindowsUwpDebugTestPerfDevicePortal]: /windows/uwp/debug-test-perf/device-portal "Общие сведения о портале устройств Windows"  

[RemoteTools]: https://www.microsoft.com/store/apps/9P6CMFV44ZLT "Удаленные инструменты для Microsoft EDGE (бета-версия)"  
[MicrosoftStore]: https://www.microsoft.com/store/apps/windows "Microsoft Store"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Каналы предварительной версии Microsoft Edge"  

[WindowsBlogStableRelease]: https://blogs.windows.com/msedgedev/2020/03/20 "Обновление в стабильных выпусках канала для Microsoft Edge"  

[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=[DevTools%20Docs%20Feedback] "Новая ошибка — MicrosoftDocs/Edge-разработчик-GitHub"  

[MicrosoftVisualstudio]: https://visualstudio.microsoft.com "Visual Studio"  

[VisualstudioCode]: https://code.visualstudio.com "Код Visual Studio"  

[PostTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Публикация твита"  
[EdgeDevToolsTwitterAccount]: https://twitter.com/EdgeDevTools "@EdgeDevTools учетной записи Twitter"  
[TheWebWeWant]: https://webwewant.fyi "Требуемый веб-сайт"  

[ColorBlindnessTypes]: http://www.colourblindawareness.org/colour-blindness/types-of-colour-blindness "Типы цветовой жалюзи"  

[MDNAcceptLanguage]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Accept-Language "Одобрение-язык | MDN"  
[MDNCookiePath]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie#Directives "Set-cookie | MDN"  

[MathiasByensLocaleDemo]: https://mathiasbynens.be/demo/locale "Пример кода, зависящий от языкового стандарта"  

[CR963183]: https://crbug.com/963183 "Ошибка 963183: DevTools не соответствует требованиям WCAG"  
[CR1003700]: https://crbug.com/1003700 "Вопрос 1003700: Добавление поддержки DevTools в целях моделирования недостатков для представления цвета"  
[CR1011679]: https://crbug.com/1011679 "Ошибка 1011679: ввод "закрепить влево" с помощью меню команд"  
[CR1016501]: https://crbug.com/1016501 "Ошибка 1016501: запрос компонента: кнопка для удаления всех локальных переопределений"  
[CR1050999]: https://crbug.com/1050999 "Ошибка 1050999: вкладка "Свойства""  
[CR1051466]: https://crbug.com/1051466 "Ошибка 1051466: поддержка отладки COOP/COEP в DevTools"  
[CR1054447]: https://crbug.com/1054447 "Ошибка 1054447: обновление метрик производительности на временной шкале DevTools"  
[CR1051822]: https://crbug.com/1051822 "Ошибка 1051822: DevTools: Добавление пользовательского интерфейса для эмуляции национальной настройки"
[CR1041830]: https://crbug.com/1041830 "Ошибка 1041830: улучшение цветопередачи для точек останова"
[CR1050855]: https://crbug.com/1050855 "Неполадка 1050855: Просмотр параметров затрудняет обнаружение"
[CR1056348]: https://crbug.com/1056348 "Ошибка 1056348: обновление компонента на информационной панели"

[COOP]: https://docs.google.com/document/d/1zDlfvfTJ_9e8Jdc8ehuV4zMEu9ySMCiTGMS9y0GU92k/edit#bookmark=id.tu4hyy6v12wn "Описание COOP и COEP — политика opener для разных источников"  
[COEP]: https://docs.google.com/document/d/1zDlfvfTJ_9e8Jdc8ehuV4zMEu9ySMCiTGMS9y0GU92k/edit#bookmark=id.uo6kivyh0ge2 "Объяснение COOP и COEP — политика для внедрения разных источников"  

[GithubGoogleChromeLighthouse]: https://github.com/GoogleChrome/lighthouse "Lighthouse | GitHub"  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/updates/2020/03/devtools/index) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
