---
description: Использование DevTools в режиме высокой контрастности Windows, соответствие сочетаний клавиш в коде DevTools и в Visual Studio, а также многое другое.
title: Новые возможности DevTools (Microsoft Edge 84)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 2752dec8bc7c4eec34ddde05a7dedff7bebef05f
ms.sourcegitcommit: b337717957529239434b4e8e1e167aebf0543518
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/15/2020
ms.locfileid: "11015491"
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

# Новые возможности DevTools (Microsoft Edge 84)  

## Объявления из группы Microsoft Edge DevTools  

В следующих разделах представлен список извещений, которые вы могли не получить в Microsoft Edge DevTools Teams! Узнайте, как использовать новые функции в DevTools, расширения кода Visual Studio и многое другое.  Чтобы оставаться на связи с самыми последними и более свежими возможностями, скачайте на веб – [каналы предварительной версии Microsoft Edge][MicrosoftEdgePreviewChannels] и [следуйте указаниям Twitter][EdgeDevToolsTwitterAccount].  

### Использование DevTools в режиме высокой контрастности Windows

Microsoft Edge DevTools теперь отображается в режиме высокой контрастности, когда Windows находится в режиме высокой контрастности.  

:::image type="complex" source="../../media/2020/05/high-contrast.msft.png" alt-text="Microsoft Edge DevTools в режиме высокой контрастности" lightbox="../../media/2020/05/high-contrast.msft.png":::
   Microsoft Edge DevTools в режиме высокой контрастности  
:::image-end:::  

[Следуйте инструкциям, чтобы включить режим высокой контрастности в Windows][MicrosoftSupportWindows10HighContrastMode].  Откройте DevTools в Microsoft EDGE, нажав `F12` или `Ctrl` + `Shift` + `I` .  DevTools отображаются в режиме высокой контрастности.  

> [!NOTE]
> Microsoft Edge DevTools в настоящее время поддерживает режим высокой контрастности в Windows, но не на macOS. 

[#1048378][CR1048378] проблем с Chromium  

### Соответствие сочетаний клавиш в DevTools с кодом Visual Studio  

Из вашего [отзыва](#getting-in-touch-with-microsoft-edge-devtools-team) и средства [отслеживания общедоступных проблем Chromium][CRIssuesList]в Microsoft Edge DevTools была рассказано о том, что вы решили настроить сочетания клавиш в DevTools.  В Microsoft Edge 84 теперь вы можете сопоставить сочетания клавиш в DevTools с [кодом Visual Studio][VSCode], который является только одной из функций, над которыми работает команда для настройки ярлыков.  

:::image type="complex" source="../../media/2020/05/keyboard-shortcut.msft.png" alt-text="Microsoft Edge DevTools в режиме высокой контрастности" lightbox="../../media/2020/05/keyboard-shortcut.msft.png":::
   Microsoft Edge DevTools в режиме высокой контрастности  
:::image-end:::  

Чтобы попробовать эксперимент, откройте параметры DevTools, нажав `?` или выделив значок ![ параметров DevTools ][ImageSettingsIcon] в правом верхнем углу DevTools.  Перейдите к разделу " **эксперименты** " и установите флажок **включить пользовательские сочетания клавиш (требуется повторная загрузка)**.  Теперь повторно Загрузи DevTools, снова откройте параметры и перейдите к разделу **сочетания клавиш** .  

Выберите **DevTools (по умолчанию)** в раскрывающемся списке **искать сочетания клавиш из предварительной настройки** и выберите **код Visual Studio**.  Сочетания клавиш в DevTools теперь соответствуют сочетаниям клавиш для эквивалентных действий в коде Visual Studio.  

Например, с помощью сочетания клавиш можно приостановить или продолжить выполнение сценария в [Visual Studio][VSCodeShortcuts] `F5` .  В стиле **DevTools (Default)** это же сочетание клавиш в DevTools имеет тот же самый ярлык `F8` , что и в **Visual Studio** , но теперь этот ярлык также доступен `F5` .  

В настоящее время эта функция доступна в Microsoft Edge 84 в качестве эксперимента, поэтому Поделитесь своим [мнением](#getting-in-touch-with-microsoft-edge-devtools-team) с командой!  

[#174309][CR174309] проблем с Chromium  

### Эмуляторы Surface Duo удаленной отладки  

Теперь вы можете выполнять удаленную отладку веб-содержимого, работающего в [эмуляторе Duo Surface][DualScreensAndroidEmulator] , используя полную мощь [Microsoft Edge DevTools][DevToolsChromiumGuide].  

С помощью [эмулятора Surface Duo][DualScreensAndroidEmulator]вы можете протестировать отображение веб-содержимого в новом классе складная и на устройствах с двумя экранами.  Эмулятор запускает операционную систему Android и предоставляет [приложение Microsoft Edge Android][AndroidEdge].  Загрузи веб-содержимое в [приложении Microsoft Edge][AndroidEdge] и отлаживать его с помощью [Microsoft Edge DevTools][DevToolsChromiumGuide].  

:::image type="complex" source="../../media/2020/05/surface-duo-emulator.msft.png" alt-text="Microsoft Edge DevTools в режиме высокой контрастности" lightbox="../../media/2020/05/surface-duo-emulator.msft.png":::
   Приложение Microsoft EDGE на эмуляторе Duo Surface  
:::image-end:::  

`edge://inspect`Страница в экземпляре [Microsoft Edge][DesktopEdge] на рабочем столе показывает **SurfaceDuoEmulator** со списком открытых вкладок или [PWAs][PwaIndex] , которые выполняются в [эмуляторе Duo Surface][DualScreensAndroidEmulator].  

:::image type="complex" source="../../media/2020/05/edge-inspect.msft.png" alt-text="Microsoft Edge DevTools в режиме высокой контрастности" lightbox="../../media/2020/05/edge-inspect.msft.png":::
   На `edge://inspect` странице отображается список вкладок в приложении Microsoft EDGE, работающем в эмуляторе.
:::image-end:::  

Если выбрать пункт **Проверка** для ВКЛАДКИ или PWA, для которых нужно выполнить отладку, откроется [Microsoft Edge DevTools][DevToolsChromiumGuide].  Следуйте пошаговым инструкциям, [чтобы выполнить удаленную отладку веб-содержимого в эмуляторе Surface Duo][DevToolsRemoteDebugDuoEmulator].  

### Упрощенное изменение размера DevToolsого ящика  

В Microsoft Edge 83 или более ранней версии вы смогли изменить размер [DevToolsого ящика][DevToolsDrawer] , наведя указатель мыши на панель инструментов ящика.  Денежный ящик ведет себя иначе, чем другие элементы управления изменением размера для областей в DevTools, где вы наводите указатель мыши на границу области, чтобы изменить ее размер.  Чтобы узнать, как изменить размер ящика, который работал в версии 83 или более ранней версии Microsoft EDGE, выберите приведенный ниже рисунок.  

:::image type="complex" source="../../media/2020/05/drawer-83.msft.png" alt-text="Microsoft Edge DevTools в режиме высокой контрастности" lightbox="../../media/2020/05/drawer-83.msft.gif":::
   Изменение размера DevTools денежных средств в Microsoft Edge 83
:::image-end:::  

<!--todo:  create png that represents the gif information  -->  

Начиная с Microsoft Edge 84, вы можете изменить размер денежного ящика, наведя указатель мыши на границу денежного ящика.  Это изменение выровнять поведение, изменяя размер DevToolsого ящика с учетом того, как вы измените размеры других областей в DevTools.  Чтобы изменить размер в действии в Microsoft Edge 84, выберите приведенный ниже рисунок.  

:::image type="complex" source="../../media/2020/05/drawer-84.msft.png" alt-text="Microsoft Edge DevTools в режиме высокой контрастности" lightbox="../../media/2020/05/drawer-84.msft.gif":::
   Изменение размера DevTools денежных средств в Microsoft Edge 84
:::image-end:::  

<!--todo:  create png that represents the gif information  -->  

[#1076112][CR1076112] проблем с Chromium  

### Отображение фокуса на кнопках навигации для презентаций  

При удаленной отладке [устройства с Android][DevToolsRemoteDebugAndroid], [устройства с Windows 10][DevToolsRemoteDebugWindows]или [эмулятора Surface Duo][DevToolsRemoteDebugDuoEmulator]вы можете переключаться между экранной презентацией с помощью ![ значка "Показать презентацию" ][ImageScreencastingIcon] в левом верхнем углу окна DevTools.  При включенной презентации вы можете перемещаться по вкладке в Microsoft EDGE на удаленном устройстве из окна DevTools.  В Microsoft Edge 84 эти кнопки навигации теперь также доступны для клавиатуры.  

:::image type="complex" source="../../media/2020/05/screencasting-nav.msft.png" alt-text="Microsoft Edge DevTools в режиме высокой контрастности" lightbox="../../media/2020/05/screencasting-nav.msft.png":::
   При нажатии на `Shift` + `Tab` отрезке экранного URL-адреса появляется фокус на кнопке " **Обновить** "
:::image-end:::  

[#1081486][CR1081486] проблем с Chromium  

### Область сведений на панели "сеть" теперь доступна  

В Microsoft Edge 84 [область сведений][DevToolsNetworkDetails] на панели " **сеть** " теперь получает фокус при открытии ресурса в [сетевом журнале][DevToolsNetworkLog].  Это изменение позволяет средствам чтения с экрана читать и взаимодействовать с содержимым области **сведений** .  

:::image type="complex" source="../../media/2020/05/network-details.msft.png" alt-text="Microsoft Edge DevTools в режиме высокой контрастности" lightbox="../../media/2020/05/network-details.msft.png":::
   При открытии области **сведений** на панели " **сеть** " выводится фокус
:::image-end:::  

[#963183][CR963183] проблем с Chromium  

## Объявления из проекта Chromium  

В следующих разделах описаны дополнительные возможности, доступные в Microsoft Edge 84, которые были задействованы в проекте Open Source Chromium.  

### Устранение проблем с сайтом с помощью средства "новые проблемы" в DevToolsном ящике

В DevToolsном лотке была создана функция новых **проблем** , позволяющая уменьшить усталость уведомлений и бессрочные элементы **консоли**.  В настоящее время **консоль** — это центральное место для разработчиков веб-сайтов, библиотек, платформ и Microsoft Edge для записи сообщений, предупреждений и ошибок.  Средство " **проблемы** " объединяет предупреждения из браузера в структурированном, статистическом и определенном виде, а также ссылки на уязвимые ресурсы в Microsoft Edge DevTools и инструкции по устранению проблем.  С течением времени вы должны видеть больше и больше предупреждений в Microsoft Edge использование в инструменте " **проблемы** ", а не на **консоли**, что поможет вам уменьшить ненужные элементы на **консоли**.  

Чтобы приступить к работе, ознакомьтесь со статьей [Поиск и устранение проблем с помощью средства Microsoft Edge DevToolss][DevtoolsIssuesIndex].  

:::image type="complex" source="../../media/2020/05/issues.msft.png" alt-text="Microsoft Edge DevTools в режиме высокой контрастности" lightbox="../../media/2020/05/issues.msft.png":::
   Инструмент " **проблемы** " в DevTools ящике  
:::image-end:::  

[#1068116][CR1068116] проблем с Chromium  

### Просмотр сведений о специальных возможностях в подсказке режима проверки  

Всплывающая подсказка **режима проверки** теперь указывает, имеет ли элемент доступное [имя и роль][WebhintHintsAxeNameRoleValue] , и это может быть [фокус клавиатуры][WebhintHintsAxeKeyboard].  

<!--todo:  add link inspect mode tooltip (WebdevCls) when section is live  -->  
<!--todo:  add link name and role (WebdevLabelsText) when section is live  -->  
<!--todo:  add link keyboard-focusable (WebdevControlFocus) when section is live  -->  

:::image type="complex" source="../../media/2020/05/a11y.msft.png" alt-text="Microsoft Edge DevTools в режиме высокой контрастности" lightbox="../../media/2020/05/a11y.msft.png":::
  Всплывающая подсказка **режима проверки** с информацией о специальных возможностях  
:::image-end:::  

[#1040025][CR1040025] проблем с Chromium  

### Обновления панели "производительность"  

#### Просмотр общих сведений о времени блокировки в нижнем колонтитуле  

После того как вы запустите производительность загрузки, на панели **производительности** теперь выводятся общие сведения о времени блокировки (TBT \) в нижнем колонтитуле.  TBT — это метрика производительности нагрузки, которая помогает количественно оценить время, затрачиваемое на использование страницы.  Он по сути определяет, как долго страница может быть использована для работы, а не в том случае, если содержимое отображается на экране. но фактически не годен для использования, так как JavaScript блокирует основной поток, поэтому страница не отвечает на ввод данных пользователем.  TBT — это основная метрика для приближения первой задержки ввода.  

<!--todo:  add link Total Blocking Time (TBT) (WebdevTbt) when section is live  -->  
<!--todo:  add link lab metric (WebdevMeasureSpeedLabField) when section is live  -->  
<!--todo:  add link Core Web Vitals (WebdevCoreWebVitals) when section is live  -->  

Чтобы получить общую информацию о времени блокировки, не используйте рабочий процесс обновления **страницы** ![ ][ImageRefreshPageIcon] для записи загрузки страниц с помощью значка страницы обновить.  

Вместо этого нажмите значок **записи записи** ![ ][ImageRecordIcon] , вручную перезагрузить страницу, дождитесь загрузки страницы и остановите запись.  

Если вы видите `Total Blocking Time: Unavailable` , Microsoft Edge DevTools не получил нужные сведения из внутренних данных профилирования в Microsoft Edge.  

:::image type="complex" source="../../media/2020/05/tbt.msft.png" alt-text="Microsoft Edge DevTools в режиме высокой контрастности" lightbox="../../media/2020/05/tbt.msft.png":::
   Общие сведения о времени блокировки в нижнем колонтитуле записи панели " **производительность** "  
:::image-end:::  

[#1054381][CR1054381] проблем с Chromium  

#### События смещения макета в разделе "новый интерфейс"  

С помощью раздела "новый **интерфейс** " на панели " **производительность** " можно определять смену макета.  Интегральная схема сдвига \ (CLS \) — это метрика, которая помогает оценить нежелательные визуальные нестабильность.

<!--todo:  add link Core Web Vitals (WebdevCoreWebVitals) when section is live  -->  
<!--todo:  add link layout shifts (WebdevCls) when section is live  -->  

Выберите событие **сдвиг макета** , чтобы просмотреть сведения о смене макета в области **Сводка** .  Наведите указатель мыши на поле **переместить из** и **переместили в** поля, чтобы увидеть, где произошел сдвиг макета.  

:::image type="complex" source="../../media/2020/05/cls.msft.png" alt-text="Microsoft Edge DevTools в режиме высокой контрастности" lightbox="../../media/2020/05/cls.msft.png":::
   Сведения о смене макета  
:::image-end:::  

### Более точная терминология по обещанию на консоли  

При входе в систему `Promise` **консоль** неправильно предоставила `PromiseStatus` значение, равное `resolved` .  

:::image type="complex" source="../../media/2020/05/resolved.msft.png" alt-text="Microsoft Edge DevTools в режиме высокой контрастности" lightbox="../../media/2020/05/resolved.msft.png":::
   Пример **консоли** с помощью старой `resolved` терминологии  
:::image-end:::  

Теперь **консоль** использует термин, который выводится `fulfilled` в соответствии со `Promise` спецификацией.  Дополнительные сведения о `Promise` спецификации можно найти в статьях [состояния и Fates на GitHub](https://github.com/domenic/promises-unwrapping/blob/master/docs/states-and-fates.md).  

:::image type="complex" source="../../media/2020/05/fulfilled.msft.png" alt-text="Microsoft Edge DevTools в режиме высокой контрастности" lightbox="../../media/2020/05/fulfilled.msft.png":::
  Пример **консоли** , в которой используется новая `fulfilled` терминология  
:::image-end:::  

[#6751][CRV86751] проблем с V8  

### Обновления области "стили"  

#### Поддержка ключевого слова "вернуть"  

Пользовательский интерфейс "Автозаполнение" области " **стили** " теперь определяет ключевое слово " [вернуть][MDNRevert] CSS", которое возвращает каскадное значение свойства к предыдущему значению, примененному к стилю элемента.  

:::image type="complex" source="../../media/2020/05/revert.msft.png" alt-text="Microsoft Edge DevTools в режиме высокой контрастности" lightbox="../../media/2020/05/revert.msft.png":::
  Установка значения свойства "вернуть"  
:::image-end:::  

[#1075437][CR1075437] проблем с Chromium  

#### Предварительный просмотр изображений  

Наведите указатель мыши на `background-image` значение в области **стили** , чтобы просмотреть изображение во всплывающей подсказке.  

:::image type="complex" source="../../media/2020/05/image-preview.msft.png" alt-text="Microsoft Edge DevTools в режиме высокой контрастности" lightbox="../../media/2020/05/image-preview.msft.png":::
  Наведение указателя мыши на `background-image` значение  
:::image-end:::  

[#1040019][CR1040019] проблем с Chromium  

#### Средство выбора цвета теперь использует нотацию функционального цвета, отделенную от пробелов  

[Модуль цветов CSS Level 4][CSSWGDraftsColor4Changes3] указывает, что функции цвета, такие как `rgb()` , должны поддерживать аргументы, разделенные пробелами.  Например, команда `rgb(0, 0, 0)` эквивалентна `rbg(0 0 0)`.  

При выборе цветов с помощью [палитры][DevtoolsCssReferenceColorPicker] цветов или переключения между цветовыми представлениями в области **стили** при нажатии `Shift` и выделении `background-color` значения должен отобразиться синтаксис аргументов, разделенных пробелами.  

:::image type="complex" source="../../media/2020/05/color.msft.png" alt-text="Microsoft Edge DevTools в режиме высокой контрастности" lightbox="../../media/2020/05/color.msft.png":::
  Использование аргументов, разделенных пробелами, в области " **стили** "  
:::image-end:::  

Также следует ознакомиться с синтаксисом в области **вычисляемый** раздел и подсказкой **режима проверки** .  

Microsoft Edge DevTools использует новый синтаксис, так как предстоящие функции CSS, например [Color ()][CSSWGDraftsColor4Property] , не поддерживают устаревший синтаксис аргументов, разделенных запятыми.  

В большинстве браузеров поддерживается синтаксис аргументов, разделенных пробелами.  Более подробную информацию можно найти в [статье возможность использования: нотация функциональных цветов, разделенных с помощью пробелов][CaniuseMDNSpaceSeparatedFunctionalColorNotations]  

[#1072952][CR1072952] проблем с Chromium  

### Устаревшее окно "Свойства" на панели "элементы"  

Область " **Свойства** " на панели " **элементы** " устарела.  Запустите `console.dir($0)` на **консоли** .  

:::image type="complex" source="../../media/2020/05/properties.msft.png" alt-text="Microsoft Edge DevTools в режиме высокой контрастности" lightbox="../../media/2020/05/properties.msft.png":::
   Область "устаревшие **Свойства** "  
:::image-end:::  

#### Ссылок  

*   [Console. dir ()][DevtoolsConsoleApiDir]  
*   [$0][DevtoolsConsoleUtilitiesDom]  

### Поддержка клавиш со встроенными приложениями в области манифеста  

Сочетания клавиш для работы с приложениями помогают пользователям быстро запускать наиболее распространенные или Рекомендуемые задачи в веб-приложении.  Меню "ярлыки приложения" отображается только для [последовательного веб-приложений][PwaIndex] , установленных на настольном компьютере или мобильном устройстве пользователя.  

<!--For more information, see [Get things done quickly with app shortcuts][WebdevAppShortcuts].  -->  

<!--todo:  add link Get things done quickly with app shortcuts (WebdevAppShortcuts) when section is live -->  

:::image type="complex" source="../../media/2020/05/app-shortcuts.msft.png" alt-text="Microsoft Edge DevTools в режиме высокой контрастности" lightbox="../../media/2020/05/app-shortcuts.msft.png":::
  Ярлыки приложений в области **манифеста**  
:::image-end:::  

## Загрузка каналов предварительной версии Microsoft Edge  

Если вы используете Windows или macOS, рассматривайте в качестве браузера по умолчанию использование [каналов предварительного просмотра Microsoft Edge][MicrosoftEdgePreviewChannels] .  Каналы предварительного просмотра предоставляют доступ к последним функциям DevTools.  

## Знакомство с Microsoft Edge Devtools Team  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- image links -->  

[ImageSettingsIcon]: /microsoft-edge/devtools-guide-chromium/remote-debugging/media/settings-icon.msft.png  
[ImageScreencastingIcon]: /microsoft-edge/devtools-guide-chromium/remote-debugging/media/toggle-screencast-icon.msft.png  
[ImageRefreshPageIcon]: /microsoft-edge/devtools-guide-chromium/remote-debugging/media/refresh-page-icon.msft.png  
[ImageRecordIcon]: /microsoft-edge/devtools-guide-chromium/remote-debugging/media/record-icon.msft.png  

<!-- links -->  

[DualScreensAndroidEmulator]: /dual-screen/android/use-emulator "Использование эмулятора Surface Duo | Документы Microsoft"

[DevtoolsConsoleApiDir]: /microsoft-edge/devtools-guide-chromium/console/api#dir "Справочник по API dir-Console | Документы Microsoft"  
[DevtoolsConsoleUtilitiesDom]: /microsoft-edge/devtools-guide-chromium/console/utilities#recently-selected-element-or-javascript-object "Недавно выбранный элемент или объект JavaScript: Справочник по API служебных программ для консоли | Документы Microsoft"  
[DevtoolsCssReferenceColorPicker]: /microsoft-edge/devtools-guide-chromium/css/reference#change-colors-with-the-color-picker "Изменение цвета с помощью палитры цветов — Справка по CSS | Документы Microsoft"  
[DevToolsDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Ящик: Настройка обзора | Документы Microsoft"  
[DevToolsChromiumGuide]: /microsoft-edge/devtools-guide-chromium "Инструменты разработчика Microsoft EDGE (Chromium) | Документы Microsoft"  
[DevtoolsIssuesIndex]: /microsoft-edge/devtools-guide-chromium/issues/index "Поиск и устранение проблем с вкладкой Microsoft Edge DevTools "вопросы" | Документы Microsoft"  
[DevToolsRemoteDebugAndroid]: /microsoft-edge/devtools-guide-chromium/remote-debugging/index "Начало работы с удаленными отладочными устройствами Android | Документы Microsoft"  
[DevToolsRemoteDebugDuoEmulator]: /microsoft-edge/devtools-guide-chromium/remote-debugging/surface-duo-emulator "Начало работы с эмуляторами Surface Duo удаленной отладки | Документы Microsoft"  
[DevToolsRemoteDebugWindows]: /microsoft-edge/devtools-guide-chromium/remote-debugging/windows "Начало работы с удаленной отладкой на устройствах с Windows 10 | Документы Microsoft"  
[DevToolsNetworkDetails]: /microsoft-edge/devtools-guide-chromium/network/index#inspect-the-details-of-the-resource "Проверка сведений о ресурсе | Документы Microsoft"  
[DevToolsNetworkLog]: /microsoft-edge/devtools-guide-chromium/network/index#log-network-activity "Регистрация активности в сети | Документы Microsoft"  
[PwaIndex]: /microsoft-edge/progressive-web-apps-chromium/index "Прогрессивные веб-приложения в Windows | Документы Microsoft"  
<!--[DevtoolsWhatsNew201901Inspect]: /microsoft-edge/devtools-guide-chromium/whats-new/2019/01/devtools#inspect "Detailed tooltips in Inspect Mode - What's New In DevTools (Edge 73) | Microsoft Docs"  -->  

[AndroidEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Приложение Microsoft Edge для Android"

[CaniuseMDNSpaceSeparatedFunctionalColorNotations]: https://caniuse.com/#feat=mdn-css_types_color_space_separated_functional_notation "Представления функциональных цветов, разделенные пробелами — MDN | Можно ли использовать"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Ошибки Chromium"

[CR174309]: https://crbug.com/174309 "DevTools: разрешение на настройку сочетаний клавиш и привязок клавиш | Ошибки Chromium"  
[CR963183]: https://crbug.com/963183 "DevTools не соответствуют требованиям WCAG | Ошибки Chromium"  
[CR1040019]: https://crbug.com/1040019 "DevTools: простое предварительное Просмотр изображений и фоновых изображений в области "стили" | Ошибки Chromium"  
[CR1040025]: https://crbug.com/1040025 "DevTools: Показывать основные сведения о a11y в элементе popover | Ошибки Chromium"  
[CR1048378]: https://crbug.com/1048378 "Поддержка пользовательского интерфейса DevTools для режима высокой контрастности | Ошибки Chromium"  
[CR1054381]: https://crbug.com/1054381 "CR 1054381 | Ошибки Chromium"  
[CR1068116]: https://crbug.com/1068116 "Панель отправки вопросов | Ошибки Chromium"  
[CR1072952]: https://crbug.com/1072952 "DevTools: средство выбора цвета должно создавать современный синтаксис цвета CSS | Ошибки Chromium"  
[CR1075437]: https://crbug.com/1075437 "DevTools: добавьте поддержку для ключевого слова "вернуть" и значений для CSS | Ошибки Chromium"  
[CR1076112]: https://crbug.com/1076112 "Devtools Персонализация — изменение размера лотка"  
[CR1081486]: https://crbug.com/1081486 "Фокус клавиатуры не отображается для кнопок навигации в режиме презентации | Ошибки Chromium"  
[CRV86751]: https://bugs.chromium.org/p/v8/issues/detail?id=6751 "PromiseStatus должен быть "выполнены", а не "разрешено" | Ошибки V8"  

[CSSWGDraftsColor4Changes3]: https://drafts.csswg.org/css-color#changes-from-3 "Изменения цвета 3 — цветовой модуль CSS уровня 4 | Черновики редакторов рабочих групп W3C CSS"  
[CSSWGDraftsColor4Property]: https://drafts.csswg.org/css-color#the-color-property "3. цвет переднего плана: "цветная" — уровень модуля цветовой поддержки CSS 4 | Черновики редакторов рабочих групп W3C CSS"  

[DesktopEdge]: https://www.microsoft.com/edge/ "Знакомство с новым Microsoft Edge"  

[GithubDomenicPromiseUnwrappingStatesFates]: https://github.com/domenic/promises-unwrapping/blob/master/docs/states-and-fates.md "Состояния и Fates-Domenic/обещания — разтекание | GitHub"  

[MDNRevert]: https://developer.mozilla.org/docs/Web/CSS/revert "вернуть | MDN"  
[MDNRevertBrowserCompatibility]: https://developer.mozilla.org/docs/Web/CSS/revert#Browser_compatibility "Совместимость с браузерами | MDN"  

[VSCode]: https://code.visualstudio.com/ "Код Visual Studio"  
[VSCodeShortcuts]: https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf "Сочетания клавиш в Visual Studio Code для Windows"  

[WebhintHintsAxeKeyboard]: https://webhint.io/docs/user-guide/hints/hint-axe/keyboard/ "Axe: клавиатура | Подсказка"  
[WebhintHintsAxeNameRoleValue]: https://webhint.io/docs/user-guide/hints/hint-axe/name-role-value/ "Axe: Name значение роли | Подсказка"  

[MicrosoftSupportWindows10HighContrastMode]: https://support.microsoft.com/help/4026951/windows-10-turn-high-contrast-mode-on-or-off "Включение и отключение режима высокой контрастности в Windows | Поддержка Windows"  

[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Публикация твита"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools учетной записи Twitter"  
[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Новая ошибка — MicrosoftDocs/Edge-разработчик"  
[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Каналы предварительной версии Microsoft Edge"  
[TheWebWeWant]: https://aka.ms/webwewant "Требуемый веб-сайт"  

<!--[WebdevAppShortcuts]: https://alphabet-dev/app-shortcuts "Get things done quickly with app shortcuts | alphabet-dev"  -->  
<!--[WebdevCls]: https://alphabet-dev/cls "Cumulative Layout Shift (CLS) | alphabet-dev"  -->  
<!--[WebdevControlFocus]: https://alphabet-dev/control-focus-with-tabindex "Control focus with tabindex | alphabet-dev"  -->  
<!--[WebdevMeasureSpeedLabField]: https://alphabet-dev/how-to-measure-speed#lab-data-vs-field-data "Lab data vs Field data - How to measure speed? | alphabet-dev"  -->  
<!--[WebdevLabelsText]: https://alphabet-dev/labels-and-text-alternatives "Labels and text alternatives | alphabet-dev"  -->  
<!--[WebdevTbt]: https://alphabet-dev/tbt "Total Blocking Time (TBT) | alphabet-dev"  -->  
<!--[WebdevCoreWebVitals]: https://alphabet-dev/vitals#core-web-vitals "Core Web Vitals | alphabet-dev"  -->  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/updates/2020/05/devtools/index) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
