---
description: Трехмерное представление, интеграция Visual Studio с Microsoft EDGE и многое другое.
title: Новые возможности DevTools (Microsoft Edge 81)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 3081ebb256a9ede637aaaddc3c3cdf7a70a201bb
ms.sourcegitcommit: b337717957529239434b4e8e1e167aebf0543518
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/15/2020
ms.locfileid: "11015477"
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

# Новые возможности DevTools (Microsoft Edge 81)  

## Объявления из группы Microsoft Edge DevTools  

В следующих разделах представлен список извещений, которые вы могли не получить в Microsoft Edge DevTools Teams! Узнайте, как использовать новые функции в DevTools, расширения кода Visual Studio и многое другое.  Чтобы оставаться на связи с самыми последними и более свежими возможностями, скачайте на веб – [каналы предварительной версии Microsoft Edge][MicrosoftEdgePreviewChannels] и [следуйте указаниям Twitter][EdgeDevToolsTwitterAccount].  

### Улучшение специальных возможностей в DevTools  

Группа DevTools изменила 170 в Chromium для устранения проблем с высокой контрастностью цвета, клавиатуры и средства чтения с экрана в DevTools.  Каждый разработчик, создающий веб-сайт, должен иметь возможность использовать DevTools.  

:::image type="complex" source="../../images/2020/01/a11y-performance-tool.msft.gif" alt-text="Средство &quot;производительность&quot; в DevTools с улучшенной навигацией с помощью клавиатуры и средства чтения с экрана" lightbox="../../images/2020/01/a11y-performance-tool.msft.gif":::
   Средство " **производительность** " в DevTools с улучшенной навигацией с помощью клавиатуры и средства чтения с экрана  
:::image-end:::  

Сведения о том, как сделать веб-страницу доступной для всех пользователей?  Скачайте [расширения для][WebhintBrowserExtension] Microsoft Edge " [Специальные возможности][AccessibilityInsights] ", чтобы приступить к работе.  

Если вы используете средства чтения с экрана или клавиатуру для навигации по DevTools, отправьте нам свой отзыв, выполнив [твит][PostTweetEdgeDevTools] в США или щелкнув значок [Отправить отзыв](#getting-in-touch-with-microsoft-edge-devtools-team) !  

[#963183][CR963183] проблем с Chromium  

### Использование DevTools на других языках  

Многие разработчики используют другие инструменты разработчика, такие как StackOverflow и код Visual Studio, на родном языке, а не только на английском языке.  Мы рады объявить локализацию для DevTools, который теперь вы можете использовать на одном из 10 языков, кроме английского.  

:::row:::
   :::column span="":::
      Китайский (упрощенное письмо) —  &#20013;&#25991;&#65288;&#31616;&#20307;&#65289;
   :::column-end:::
   :::column span="":::
      Китайский (традиционное письмо) —  &#20013;&#25991;&#65288;&#32321;&#39636;&#65289;
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      Французский — Fran&#231;AIS
   :::column-end:::
   :::column span="":::
      Немецкий — Deutsch
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      Итальянский — Italiano
   :::column-end:::
   :::column span="":::
      Японская  &#26085;&#26412;&#35486;
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      Корейский —  &#54620;&#44397;&#50612;
   :::column-end:::
   :::column span="":::
      Португальский (portugu&#234;s)
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      Русский —  &#1088;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081;
   :::column-end:::
   :::column span="":::
      Испанская — ESPA&#241;OL
   :::column-end:::
:::row-end:::

<!--  
|  |  |  
|:--- |:--- |  
| Chinese (Simplified) - 中文(简体)（简体）| Chinese (Traditional) - 中文(繁體)（繁體）|  
| French – français | German - deutsch |  
| Italian - italiano | Portuguese - português |  
| Korean - 한국어 | Japanese - 日本語 |  
| Russian – русский | Spanish - español |  
-->  

DevTools автоматически соответствует языку, который вы используете для Microsoft Edge in `edge://settings/languages` .  

Если вы хотите, чтобы Microsoft Edge выоставался на одном языке, а DevTools на русском языке, нажмите кнопку `F1` DevTools, чтобы открыть вкладку [Параметры][Settings] и отключить **язык браузера**.  

:::image type="complex" source="../../images/2020/01/localized-devtools.msft.png" alt-text="Средство &quot;производительность&quot; в DevTools с улучшенной навигацией с помощью клавиатуры и средства чтения с экрана" lightbox="../../images/2020/01/localized-devtools.msft.png":::
   DevTools на немецком языке  
:::image-end:::  

Сообщения **консоли** не локализуются.  На языке, используемом для Microsoft EDGE, отображаются только строки, используемые в пользовательском интерфейсе DevTools.  

Если вы хотите использовать DevTools на языке, отличном от того, на котором они доступны, [твит][PostTweetEdgeDevTools] в США или щелкните значок [Отправить отзыв](#getting-in-touch-with-microsoft-edge-devtools-team) .  

[#941561][CR941561] проблем с Chromium  

### Веб – подсказка с расширением Microsoft Edge  

Расширение веб-подсказки Microsoft EDGE позволяет легко находить и получать отзывы о специальных возможностях, совместимости с браузерами, безопасности, производительности и других средствах в DevTools.  Узнайте больше о [https://webhint.io][Webhint] .  

:::image type="complex" source="../../images/2020/01/webhint-browser-extension.msft.png" alt-text="Средство &quot;производительность&quot; в DevTools с улучшенной навигацией с помощью клавиатуры и средства чтения с экрана" lightbox="../../images/2020/01/webhint-browser-extension.msft.png":::
   Вкладка **"Подсказка** " в DevTools, если установлено расширение браузера веб.  
:::image-end:::  

[Попробуйте расширение браузера веб для подсказки в Microsoft Edge][MicrosoftEdgeInsiderAddons].  После установки расширения откройте DevTools и перейдите на вкладку подсказки.  В этой статье запустите настраиваемое сканирование сайта.  Чтобы получить дополнительные сведения, [заwebhint.IO][WebhintBrowserExtension] в голову.  

### Трехмерное представление  

С помощью **трехмерного представления** вы можете выполнять отладку своего веб-приложения, перемещаясь по [объектной модели документов \ (DOM)][MDNDocumentObjectModel] или контексту стека [z-индексов][MDNZIndex] .  

:::image type="complex" source="../../images/2020/01/3dview.msft.png" alt-text="Средство &quot;производительность&quot; в DevTools с улучшенной навигацией с помощью клавиатуры и средства чтения с экрана" lightbox="../../images/2020/01/3dview.msft.png":::
   Трехмерное представление в DevTools  
:::image-end:::  

Для доступа к трехмерному представлению нажмите клавишу `Ctrl`  +  `Shift`  +  `P` Ввод в **режиме 3D-представления** и выберите **Показать 3D-представление**.  

Мы работаем над ИНТЕРФЕЙСом и добавляем дополнительные функции в 3D-представление, поэтому отправьте нам свой [отзыв](#getting-in-touch-with-microsoft-edge-devtools-team).  

[#987787][CR987787] проблем с Chromium  

### Расширения кода Visual Studio  

Кроме того, в команде DevTools были выпущены некоторые расширения для [кода Visual Studio][VisualStudioCode] , позволяющие использовать возможности DevTools прямо из текстового редактора. Ознакомьтесь с приведенными ниже расширениями.  

#### Элементы Microsoft Edge  

Используйте инструмент "элементы" в коде Visual Studio, добавив [элементы для расширения кода Microsoft Edge \ (Chromium \)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] Visual Studio.  

:::image type="complex" source="../../images/2020/01/elements-for-edge.msft.png" alt-text="Средство &quot;производительность&quot; в DevTools с улучшенной навигацией с помощью клавиатуры и средства чтения с экрана" lightbox="../../images/2020/01/elements-for-edge.msft.png":::
   Инструмент " **элементы** " в коде Visual Studio с использованием элементов для расширения Microsoft Edge  
:::image-end:::  

Для получения дополнительных сведений изучите [элементы для расширения кода Microsoft Edge Visual Studio][VisualStudioCodeElementEdgeExtension].  

#### Отладчик для Microsoft Edge  

С помощью [отладчика для расширения кода Microsoft Edge][VisualStudioMarketplaceDebuggerEdge] Visual Studio выполните отладку JavaScript, который выполняется в Microsoft EDGE, прямо из кода Visual Studio.  

:::image type="complex" source="../../images/2020/01/vscode-debugger.msft.png" alt-text="Средство &quot;производительность&quot; в DevTools с улучшенной навигацией с помощью клавиатуры и средства чтения с экрана" lightbox="../../images/2020/01/vscode-debugger.msft.png":::
   Отладчик для расширения Microsoft EDGE в Visual Studio  
:::image-end:::  

Дополнительные сведения [об отладке Microsoft Edge из кода Visual Studio можно найти в этой процедуре][VisualStudioCodeDebuggerEdgeExtension].  

#### webhint  

Расширение [кода Visual Studio, которое используется][VisualStudioMarketplaceWebhintExtension] `webhint` для усовершенствования веб-страницы во время их написания! Это расширение запускает и сообщает диагностику файлов рабочей области на основе `webhint` анализа.  

:::image type="complex" source="../../images/2020/01/webhint-vscode-extension.msft.png" alt-text="Средство &quot;производительность&quot; в DevTools с улучшенной навигацией с помощью клавиатуры и средства чтения с экрана" lightbox="../../images/2020/01/webhint-vscode-extension.msft.png":::
   Расширение кода Visual Studio «веб-подсказка» для анализа `.tsx` файла в коде Visual Studio  
:::image-end:::  

[Узнайте больше о расширении подсказки кода Visual Studio][WebhintVisualStudioCodeExtension].  

### Интеграция с Visual Studio  

В Visual Studio 2019 версии 16,2 или более поздней Используйте отладчик Visual Studio для отладки JavaScript, который выполняется в Microsoft Edge.  [Загрузите Visual Studio 2019][MicrosoftVisualStudioDownloads] , чтобы попробовать эту функцию!  

:::image type="complex" source="../../images/2020/01/vs.msft.png" alt-text="Средство &quot;производительность&quot; в DevTools с улучшенной навигацией с помощью клавиатуры и средства чтения с экрана" lightbox="../../images/2020/01/vs.msft.png":::
   Visual Studio с возможностью запуска веб-приложения в Microsoft Edge Канарские, dev или Beta  
:::image-end:::  

Дополнительные [сведения об отладке Microsoft Edge из Visual Studio][MicrosoftVisualStudio].  

### Сообщения консоли предотвращения отслеживания  

Защита от слежения — это уникальная функция в Microsoft EDGE, которая защищает вас от отслеживания веб-сайтов, которые вы еще не посещаете.  Параметр предотвращения отслеживания по умолчанию — это режим балансировки, который блокирует средства отслеживания и известных злоумышленников, чтобы обеспечить баланс конфиденциальности и веб-совместимости.  Чтобы получить более подробную информацию о совместимости веб-страницы, если некоторые средства отслеживания заблокированы, мы также добавили предупреждающие сообщения на консоли, когда средство отслеживания заблокировано.  

:::image type="complex" source="../../images/2020/01/tracking-prevention.msft.png" alt-text="Средство &quot;производительность&quot; в DevTools с улучшенной навигацией с помощью клавиатуры и средства чтения с экрана" lightbox="../../images/2020/01/tracking-prevention.msft.png":::
   Сообщения на консоли, когда предотвращение отслеживания блокирует доступ к хранилищу для средства отслеживания  
:::image-end:::  

[Узнайте больше о предотвращении отслеживания и балансе между конфиденциальностью и веб-совместимостью][TrackingPrevention].  

## Объявления из проекта Chromium  

В следующих разделах описаны дополнительные возможности, доступные в Microsoft Edge 81, которые были задействованы в проекте Open Source Chromium.  

### Поддержка Moto G4 в режиме устройства  

После [включения панели инструментов устройства][DeviceToolbar]имитируйте размеры окна просмотра Moto G4 в списке **устройств** .  

:::image type="complex" source="../../images/2020/01/motog4.msft.png" alt-text="Средство &quot;производительность&quot; в DevTools с улучшенной навигацией с помощью клавиатуры и средства чтения с экрана" lightbox="../../images/2020/01/motog4.msft.png":::
   Имитация окна просмотра Moto G4  
:::image-end:::  

Щелкните [Показать рамку устройства][DeviceFrame] , чтобы показать аппаратуру Moto G4 в окне просмотра.  

:::image type="complex" source="../../images/2020/01/motog4frame.msft.png" alt-text="Средство &quot;производительность&quot; в DevTools с улучшенной навигацией с помощью клавиатуры и средства чтения с экрана" lightbox="../../images/2020/01/motog4frame.msft.png":::
   Аппаратное обеспечение Moto G4  
:::image-end:::  

Дополнительные возможности:  

*   Откройте [меню команд][CommandMenu] и выполните команду, `Capture screenshot` чтобы сделать снимок экрана просмотра, включающий оборудование Moto G4 (после включения команды **Показать рамку устройства**).  
*   [Регулирование сети и ЦП][ThrottleNetworkAndCpu] для более точной имитации условий просмотра веб-страниц пользователя на мобильном устройстве.  

[#924693][CR924693] проблем с Chromium  

### Обновления, связанные с файлами cookie  

#### Заблокированные cookie-файлы в области "cookie"  

В области "файлы cookie" на панели приложения теперь отображаются заблокированные файлы cookie с желтым фоном.  

:::image type="complex" source="../../images/2020/01/blockedcookies.msft.png" alt-text="Средство &quot;производительность&quot; в DevTools с улучшенной навигацией с помощью клавиатуры и средства чтения с экрана" lightbox="../../images/2020/01/blockedcookies.msft.png":::
   Заблокированные cookie-файлы в области "cookie" на панели приложения  
:::image-end:::  

[#1030258][CR1030258] проблем с Chromium  <!-- inaccessible  -->  

#### Приоритет cookie-файлов в области "cookie"  

Таблицы cookie на панелях сеть и приложения теперь включают столбец **приоритета** .  

> [!CAUTION]
> Chromiumные браузеры, такие как Microsoft EDGE, — это единственные браузеры, поддерживающие приоритет cookie-файлов.  

[#1026879][CR1026879] проблем с Chromium  

#### Изменение всех значений cookie-файлов  

Все ячейки в таблицах cookie теперь доступны для редактирования, кроме ячеек в столбце **Размер** , так как этот столбец представляет размер файла cookie в байтах.  Просмотрите [поля][CookiesFields] , поясняющие каждый столбец.  

:::image type="complex" source="../../images/2020/01/editcookie.msft.png" alt-text="Средство &quot;производительность&quot; в DevTools с улучшенной навигацией с помощью клавиатуры и средства чтения с экрана" lightbox="../../images/2020/01/editcookie.msft.png":::
   Изменение значения cookie-файла  
:::image-end:::  

#### Копирование как Node.js выбор для включения данных cookie  

Щелкните правой кнопкой мыши по сетевому запросу и выберите команду **Копировать**  >  **копию как Node.js извлечь** , чтобы получить `fetch` выражение, включающее данные cookie.  

:::image type="complex" source="../../images/2020/01/fetchcookies.msft.png" alt-text="Средство &quot;производительность&quot; в DevTools с улучшенной навигацией с помощью клавиатуры и средства чтения с экрана" lightbox="../../images/2020/01/fetchcookies.msft.png":::
   Копирование как Node.js выборка  
:::image-end:::  

[#1029826][CR1029826] проблем с Chromium  

### Более точные значки манифеста веб-приложения  

Ранее область манифеста на панели приложения отправляет свои собственные запросы для отображения значков манифеста веб-приложения.  DevTools теперь показывает тот же значок манифеста, который использует Microsoft Edge.  

:::image type="complex" source="../../images/2020/01/manifesticons.msft.png" alt-text="Средство &quot;производительность&quot; в DevTools с улучшенной навигацией с помощью клавиатуры и средства чтения с экрана" lightbox="../../images/2020/01/manifesticons.msft.png":::
   Значки в области «манифест»  
:::image-end:::  

[#985402][CR985402] проблем с Chromium  

### Наведите указатель мыши на свойства содержимого CSS, чтобы увидеть неэкранированные значения  

Наведите указатель мыши на значение `content` свойства, чтобы увидеть неэкранированную версию значения.  

Например, в этой статье вы узнаете [о том,][CSSContentDemo] что на `p::after` панели Стили отображается строка с escape-символами.  

:::image type="complex" source="../../images/2020/01/escapedstring.msft.png" alt-text="Средство &quot;производительность&quot; в DevTools с улучшенной навигацией с помощью клавиатуры и средства чтения с экрана" lightbox="../../images/2020/01/escapedstring.msft.png":::
   Строка с escape-символом  
:::image-end:::  

При наведении указателя мыши на значение, которое `content` отображается в неэкранированном значении:  

:::image type="complex" source="../../images/2020/01/unescapedstring.msft.png" alt-text="Средство &quot;производительность&quot; в DevTools с улучшенной навигацией с помощью клавиатуры и средства чтения с экрана" lightbox="../../images/2020/01/unescapedstring.msft.png":::
   Неэкранированное значение  
:::image-end:::  

### Дополнительные сведения об ошибках на карте исходного кода на консоли  

Теперь консоль содержит более подробные сведения о том, почему не удалось загрузить или проанализировать исходную карту.  Ранее она только что предоставила ошибку, не объясняющую, что пошло не так.  

:::image type="complex" source="../../images/2020/01/sourcemap.msft.png" alt-text="Средство &quot;производительность&quot; в DevTools с улучшенной навигацией с помощью клавиатуры и средства чтения с экрана" lightbox="../../images/2020/01/sourcemap.msft.png":::
   Ошибка при загрузке карты исходного кода на консоли  
:::image-end:::  

### Настройка отключения прокрутки за пределами файла  

Откройте [Параметры][Settings] и выберите Отключить **Preferences**  >  **исходные**настройки.  >  **разрешите прокрутку за** пределами файла, чтобы отключить поведение пользовательского интерфейса по умолчанию, позволяющее прокручивать прокрутку за пределами файла на панели « **источники** ».  

:::image type="complex" source="../../images/2020/01/settings.msft.png" alt-text="Средство &quot;производительность&quot; в DevTools с улучшенной навигацией с помощью клавиатуры и средства чтения с экрана" lightbox="../../images/2020/01/settings.msft.png":::
   Отключение **разрешения на прокрутку за** пределами файла в параметрах  
:::image-end:::  

:::image type="complex" source="../../images/2020/01/scrollingsources.msft.png" alt-text="Средство &quot;производительность&quot; в DevTools с улучшенной навигацией с помощью клавиатуры и средства чтения с экрана" lightbox="../../images/2020/01/scrollingsources.msft.png":::
   Прокрутка за пределами файла теперь отключена на панели «источники»  
:::image-end:::  

## Загрузка каналов предварительной версии Microsoft Edge  

Если вы используете Windows или macOS, рассматривайте в качестве браузера по умолчанию использование [каналов предварительного просмотра Microsoft Edge][MicrosoftEdgePreviewChannels] .  Каналы предварительного просмотра предоставляют доступ к последним функциям DevTools.  

## Знакомство с Microsoft Edge DevTools Team  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DeviceToolbar]: /microsoft-edge/devtools-guide-chromium/device-mode/index#simulate-a-mobile-viewport "Имитировать окно просмотра для мобильных устройств: Эмуляция мобильных устройств с помощью режима устройства в Microsoft Edge DevTools | Документы Microsoft"
[DeviceFrame]: /microsoft-edge/devtools-guide-chromium/device-mode/index#show-device-frame "Показать рамку устройства — имитировать мобильные устройства с помощью режима устройства в Microsoft Edge DevTools | Документы Microsoft"
[CommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Выполнение команд с помощью командного меню Microsoft Edge DevTools | Документы Microsoft"  
[ThrottleNetworkAndCpu]: /microsoft-edge/devtools-guide-chromium/device-mode/index#throttle-the-network-and-cpu "Регулирование сети и ЦП — Эмуляция мобильных устройств с помощью режима устройства в Microsoft Edge DevTools | Документы Microsoft"
[Settings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Параметры: Настройка Microsoft Edge DevTools | Документы Microsoft"
[MicrosoftVisualStudio]: /microsoft-edge/visual-studio/index "Visual Studio | Документы Microsoft"  
[CookiesFields]: /microsoft-edge/devtools-guide-chromium/storage/cookies#fields "Поля — просмотр, изменение и удаление cookie-файлов в Microsoft Edge DevTools | Документы Microsoft"  

[VisualStudioCodeDebuggerEdgeExtension]: /microsoft-edge/visual-studio-code/debugger-for-edge "Отладчик для расширения кода Microsoft Edge Visual Studio"  
[VisualStudioCodeElementEdgeExtension]: /microsoft-edge/visual-studio-code/elements-for-edge "Элементы расширения кода Microsoft Edge Visual Studio"  

[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Каналы предварительной версии Microsoft Edge"  

[VisualStudioCode]: https://aka.ms/vscode "Код Visual Studio"  
[VisualStudioMarketplaceDebuggerEdge]: https://aka.ms/debugger4code "Отладчик для Microsoft Edge-Visual Studio Marketplace"  
[VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension]: https://aka.ms/elements4code "Элементы для Microsoft Edge \ (Chromium \) — Visual Studio Marketplace"  
[VisualStudioMarketplaceWebhintExtension]: https://aka.ms/webhint4code ""Подсказка" — Visual Studio Marketplace"

[TrackingPrevention]: https://aka.ms/microsoftedge/tracking-prevention-blog "Улучшение защиты от слежения в блоге Microsoft Edge"

[MicrosoftEdgeInsiderAddons]: https://aka.ms/webhint/edge-extension "Надстройки Microsoft Edge для участников программы предварительной оценки"  
[MicrosoftVisualStudioDownloads]: https://aka.ms/vs/download "Скачайте Visual Studio 2019 для Windows & Mac"  

[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Публикация твита"  

[CR924693]: https://crbug.com/924693 "Запрос функции: Добавление Moto G4 в список режимов устройства | Ошибки Chromium"  
[CR1030258]: https://crbug.com/1030258 "CR 1030258 | Ошибки Chromium"  
[CR1026879]: https://crbug.com/1026879 "На вкладке cookie на консоли разработки больше не отображается приоритет | Ошибки Chromium"  
[CR1029826]: https://crbug.com/1029826 "Вкладка "сеть" — > щелкнуть правой кнопкой мыши, чтобы запрашивать > копирование > копирование в качестве выборке не копирует файлы cookie | Ошибки Chromium"  
[CR985402]: https://crbug.com/985402 "строки ошибки значка манифеста веб-приложения — это запутанная | Ошибки Chromium"  
[CR963183]: https://crbug.com/963183 "DevTools не соответствуют требованиям WCAG | Ошибки Chromium"  
[CR941561]: https://crbug.com/941561 "Локализуемость DevTools | Ошибки Chromium"  
[CR987787]: https://crbug.com/987787 "3D-представление DOM | Ошибки Chromium"  

[CSSContentDemo]: https://mathiasbynens.github.io/css-dbg-stories/css-escapes.html "Демонстрация для без последовательного содержимого CSS"  

[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Новая ошибка — MicrosoftDocs/Edge-разработчик"  

[TheWebWeWant]: https://aka.ms/webwewant "Требуемый веб-сайт"  
[AccessibilityInsights]: https://aka.ms/a11yinsights "Аналитические сведения о специальных возможностях"  
[MDNDocumentObjectModel]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model "Объектная модель документов (DOM) | MDN"  
[MDNZIndex]: https://developer.mozilla.org/docs/Web/CSS/z-index "z-индекс | MDN"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools учетной записи Twitter"  

[Webhint]: https://aka.ms/webhint "Подсказка"  

[WebhintBrowserExtension]: https://aka.ms/webhint/browser-extension "Расширение браузеров веб – подсказок | Документация по подсказкам"  
[WebhintVisualStudioCodeExtension]: https://aka.ms/webhint/code-extension "Расширение кода Visual Studio "Подсказка" | Документация по подсказкам"  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/updates/2020/01/devtools/index) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  