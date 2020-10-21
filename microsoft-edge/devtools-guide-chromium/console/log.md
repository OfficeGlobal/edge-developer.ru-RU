---
description: Сведения о том, как записывать сообщения на консоль.
title: Начало работы с сообщениями журнала на консоли
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 96e3ad76fb86e32cf58abe6187fa0d6e75a2c00a
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125274"
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

# Начало работы с сообщениями журнала на консоли  

В этом интерактивном учебнике показано, как записывать и фильтровать сообщения на консоли [Microsoft Edge DevTools][MicrosoftEdgeDevTools] .  

:::image type="complex" source="../media/console-ars-technica-console-onload.msft.png" alt-text="Сообщения на консоли" lightbox="../media/console-ars-technica-console-onload.msft.png":::
   Сообщения на **консоли**  
:::image-end:::  

Этот учебник предназначен для выполнения в нужном порядке.  Предполагается, что вы знакомы с основами веб-разработки, например с помощью JavaScript для добавления интерактивности на страницу.  

## Настройка ролика и DevTools  

Этот учебник разработан таким образом, чтобы вы могли открыть демонстрацию и попробовать все рабочие процессы самостоятельно.  После того как вы будете физически подписаться на нее, вы, наверное, захотите запомнить рабочие процессы позже.  

1.  Удерживайте клавишу `Control` \ (Windows, Linux \) или `Command` \ (macOS \) и выберите **примеры журнала консоли** , которые нужно открыть на новой вкладке.  
    
    [Примеры журнала консоли][GlitchDevToolsConsoleLogExamples]
    
    <!--
    > [!TIP]
    > Move the demo to a separate window.  
    > 
    > :::image type="complex" source="../media/log-set-up-1.msft.png" alt-text="Сообщения на консоли" lightbox="../media/log-set-up-1.msft.png":::
    >    The tutorial on the left, and the demo on the right  
    > :::image-end:::  
    -->
    
1.  Чтобы открыть DevTools, сосредоточьте демонстрацию и выберите `Control` + `Shift` + `J` \ (Windows, Linux \) или `Command` + `Option` + `J` \ (macOS \).  По умолчанию DevTools открывается справа от демонстрации.  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/console-example-devtools-right-console.msft.png" alt-text="Сообщения на консоли" lightbox="../media/console-example-devtools-right-console.msft.png":::
             DevTools открывается справа от демонстрации  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          > [!TIP]
          > [Закрепите DevTools в нижней части окна][DevToolsCustomizePlacement].  
          
          :::image type="complex" source="../media/console-example-devtools-bottom-console.msft.png" alt-text="Сообщения на консоли" lightbox="../media/console-example-devtools-bottom-console.msft.png":::
             DevTools закреплено в нижней части демонстрации  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    :::row:::
       :::column span="":::
          > [!TIP]
          > [Открепите DevTools в отдельном окне][DevToolsCustomizePlacement].  
          
          :::image type="complex" source="../media/console-example-devtools-separate-console-browse.msft.png" alt-text="Сообщения на консоли" lightbox="../media/console-example-devtools-separate-console-browse.msft.png":::
             Браузер в отдельном окне  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          > [!TIP]
          > [Открепите DevTools в отдельном окне][DevToolsCustomizePlacement].  
          
          :::image type="complex" source="../media/console-example-devtools-separate-console-devtools.msft.png" alt-text="Сообщения на консоли" lightbox="../media/console-example-devtools-separate-console-devtools.msft.png":::
             DevTools отсоединяется в отдельном окне  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
## Просмотр сообщений, записанных из JavaScript  

Большинство сообщений, которые вы видите на консоли, поступают от веб-разработчиков, которые написали JavaScript страницы.  Цель этого раздела — рассказать вам о различных типах сообщений, которые вы, вероятно, видите на консоли, и объясните, как можно вести журнал для каждого типа сообщений.  

1.  Нажмите кнопку " **сведения о журнале** " в демонстрационной версии.  `Hello, Console!` Получает запись в журнал консоли.
    
    :::image type="complex" source="../media/console-log-info.msft.png" alt-text="Сообщения на консоли" lightbox="../media/console-log-info.msft.png":::
       **Консоль** после нажатия кнопки " **сведения о журнале** "  
    :::image-end:::  
    
1.  Рядом с `Hello, Console!` сообщением на консоли выберите **log.js:2**.  Откроется панель источники, в которой выделена строка кода, которая привела к тому, что сообщение будет записано на консоль.  Сообщение было занесено в журнал при выполнении кода JavaScript на странице `console.log('Hello, Console!')` .
    
    :::image type="complex" source="../media/console-sources-logjs.msft.png" alt-text="Сообщения на консоли" lightbox="../media/console-sources-logjs.msft.png":::
       DevTools открывает панель « **источники** » после нажатия кнопки `log.js:2`  
    :::image-end:::  
    
1.  Вернитесь на **консоль** с помощью одного из следующих рабочих процессов:  
    
    *   Откройте вкладку **консоль** .  
    *   Выберите `Control` + `[` \ (Windows, Linux \) или `Command` + `[` \ (macOS \), пока панель консоли не станет фокусом.  
    *   [Откройте меню команд][DevToolsCommandMenu], начните вводить текст `Console` , выберите команду **Показать панель консоли** , а затем нажмите кнопку `Enter` .  
    
1.  Нажмите кнопку **предупреждение журнала** в демонстрационной версии.  `Abandon Hope All Ye Who Enter` Получает запись в журнал консоли.  Сообщения, которые форматируются таким образом, представляют собой предупреждения.  
    
    :::image type="complex" source="../media/console-log-warning.msft.png" alt-text="Сообщения на консоли" lightbox="../media/console-log-warning.msft.png":::
       **Консоль** после выбора команды " **log Warning** "  
    :::image-end:::  
    
    > [!TIP]
    > Если вы хотите просмотреть код, который привел к тому, что сообщение записалось определенным образом, нажмите на сценарий \ (например, `log.js:12` \), чтобы просмотреть код, который привел к форматированию сообщения.  

1.  Щелкните значок **expand** ( ![ Развернуть ][ImageExpandIcon] ) перед `Abandon Hope All Ye Who Enter` .  DevTools показывает [трассировку стека][WikiStackTrace] , ведущая к вызову.  
    
    :::image type="complex" source="../media/console-log-warning-expanded.msft.png" alt-text="Сообщения на консоли" lightbox="../media/console-log-warning-expanded.msft.png":::
       Трассировка стека  
    :::image-end:::  
    
    Трассировка стека указывает на то, что вызвана функция с именем `logWarning` , которая, в свою очередь, вызывает функцию с именем `quoteDante` .  Другими словами, вызов, который произошел первым, находится в нижней части трассировки стека.  Вы можете регистрировать трассировку стека в любое время, вызывая `console.trace()` .  

1.  Выберите пункт **Ошибка журнала**.  Регистрируется следующее сообщение об ошибке: `I'm sorry, Dave.  I'm afraid I can't do that.`  
    
    :::image type="complex" source="../media/console-log-error.msft.png" alt-text="Сообщения на консоли" lightbox="../media/console-log-error.msft.png":::
       Сообщение об ошибке  
    :::image-end:::  
    
1.  Выберите пункт **таблица журнала**.  Таблица, посвященная знаменитым исполнителям, записывается на консоль.  
    
    > [!NOTE]
    > `birthday`Столбец заполняется только для одной строки.  Проверьте код, чтобы определить причину.
    
    :::image type="complex" source="../media/console-log-table.msft.png" alt-text="Сообщения на консоли" lightbox="../media/console-log-table.msft.png":::
       Таблица в **консоли**  
    :::image-end:::  
    
1.  Выберите команду **Группа журналов**.  Названия четырех знаменитых turtlesных, преступных, группируются под `Adolescent Irradiated Espionage Tortoises` меткой.  
    
    :::image type="complex" source="../media/console-log-group.msft.png" alt-text="Сообщения на консоли" lightbox="../media/console-log-group.msft.png":::
       Группа сообщений на **консоли**  
    :::image-end:::  
    
1.  Выберите пункт **Журнал настраиваемого**.  Сообщение с красной рамкой и синим фоном записываются в консоль.  
    
    :::image type="complex" source="../media/console-log-custom.msft.png" alt-text="Сообщения на консоли" lightbox="../media/console-log-custom.msft.png":::
       Сообщение с настраиваемым форматированием в **консоли**  
    :::image-end:::  
    
Основная идея здесь заключается в том, что если вы хотите записывать сообщения на консоль из JavaScript, используйте один из этих `console` методов.  Каждый метод форматирует сообщения по-разному.  

В этом разделе есть еще больше методов, чем было показано ниже.  В этом учебнике показано, как ознакомиться с другими методами.  

## Просмотр сообщений, записанных браузером  

Браузер также регистрирует сообщения на консоли.  Обычно это происходит при возникновении проблемы со страницей.  

1.  Выберите **причина 404**.  Браузер регистрирует код состояния HTTP `404` ошибки сети, так как сценарий JavaScript пытается получить несуществующий файл.  
    
    :::image type="complex" source="../media/console-cause-404.msft.png" alt-text="Сообщения на консоли" lightbox="../media/console-cause-404.msft.png":::
       `404`Ошибка в **консоли**  
    :::image-end:::  
    
1.  Выберите " **Причина ошибки**".  Браузер регистрирует неперехваченные записи, `TypeError` так как JavaScript пытается обновить несуществующий узел DOM.  
    
    :::image type="complex" source="../media/console-cause-error.msft.png" alt-text="Сообщения на консоли" lightbox="../media/console-cause-error.msft.png":::
       А на `TypeError` **консоли**  
    :::image-end:::  
    
1.  Щелкните раскрывающийся список **уровни журнала** и включите параметр **подробный** , если он отключен.  Подробнее о фильтрации можно узнать в следующем разделе.  Это необходимо сделать, чтобы убедиться в том, что следующее сообщение отображается в журнале.  
    
    > [!NOTE]
    > Если раскрывающийся список уровни по умолчанию отключен, может потребоваться закрыть панель **консоли** .  Отфильтровать по источнику сообщения, чтобы получить дополнительные сведения о боковой панели **консоли** .
    
    :::image type="complex" source="../media/console-cause-error-log-levels.msft.png" alt-text="Сообщения на консоли" lightbox="../media/console-cause-error-log-levels.msft.png":::
       Включение подробного уровня ведения журнала  
    :::image-end:::  
    
1.  Выберите команду **вызвать нарушение**.  Страница перестает отвечать на запросы в течение нескольких секунд, а затем браузер заносит сообщение `[Violation] 'click' handler took 3000ms` на консоль.  Точная длительность может отличаться.  
    
    :::image type="complex" source="../media/console-cause-violation.msft.png" alt-text="Сообщения на консоли" lightbox="../media/console-cause-violation.msft.png":::
       Нарушение в **консоли**  
    :::image-end:::  
    
## Фильтрация сообщений  

На некоторых страницах вы видите консоль с сообщениями.  DevTools предоставляет множество различных способов фильтрации сообщений, которые не связаны с задачей.  

### Фильтрация по уровню ведения журнала  

Каждому `console` методу назначается уровень серьезности: `Verbose` , `Info` , `Warning` или `Error` .  Например, `console.log()` `Info` сообщение на уровне, в то время как `console.error()` сообщение на `Error` уровне.  

1.  Щелкните раскрывающийся список **уровни журнала** и отключите **ошибки**.  Уровень отключается, если рядом с ним больше нет метки.  `Error`Сообщения на уровне пропадают.  
    
    :::image type="complex" source="../media/console-cause-violation-log-levels.msft.png" alt-text="Сообщения на консоли" lightbox="../media/console-cause-violation-log-levels.msft.png":::
       Отключение сообщений уровня ошибки на **консоли**  
    :::image-end:::  
    
1.  Снова щелкните в раскрывающемся списке **уровни журнала** и повторно включите **ошибки**.  `Error`Снова появятся сообщения уровня.  

### Фильтрация по тексту  

Если вы хотите только просматривать сообщения, содержащие точную строку, введите эту строку в текстовом поле **Фильтр** .  

1.  Введите `Dave` текст в текстовое поле **Фильтр** .  Все сообщения, в которых не указана строка `Dave` , скрыты.  Кроме того, вы можете увидеть `Adolescent Irradiated Espionage Tortoises` метку.  Это ошибка.  
    
    :::image type="complex" source="../media/console-all-messages-text-filter.msft.png" alt-text="Сообщения на консоли" lightbox="../media/console-all-messages-text-filter.msft.png":::
       Фильтрация сообщений, которые не включают `Dave`  
    :::image-end:::  
    
1.  `Dave`"Удалить" из текстового поля " **Фильтр** ".  Все сообщения снова появятся.  

### Фильтрация по регулярному выражению  

Если вы хотите отобразить все сообщения, которые содержат шаблон текста, а не определенную строку, используйте [регулярное выражение][MDNRegularExpressions].  

1.  Введите `/^[AH]/` текст в текстовое поле **Фильтр** .  Введите этот шаблон в [Regex][|::ref1::|Main] , чтобы узнать, что он делает.  
    
    :::image type="complex" source="../media/console-all-messages-regex-filter.msft.png" alt-text="Сообщения на консоли" lightbox="../media/console-all-messages-regex-filter.msft.png":::
       Фильтрация сообщений, не соответствующих шаблону `/^[AH]/`  
    :::image-end:::  
    
1.  `/^[AH]/`"Удалить" из текстового поля " **Фильтр** ".  Все сообщения будут снова видны.  

### Фильтрация по источнику сообщения  

Если вы хотите только просматривать сообщения, поступившие с определенного URL-адреса, используйте **боковую панель**.  

1.  Нажмите кнопку **Показать боковую панель консоли** \ ( ![ Показать боковую панель консоли ][ImageShowConsoleSidebarIcon] ).  
    
    :::image type="complex" source="../media/console-sidebar-all-messages.msft.png" alt-text="Сообщения на консоли" lightbox="../media/console-sidebar-all-messages.msft.png":::
       Боковая панель  
    :::image-end:::  
    
1.  Щелкните значок " **развернуть** " и " ![ Развернуть" ][ImageExpandIcon] рядом с количеством сообщений.  На приведенном ниже рисунке количество сообщений обозначено **13 сообщениями**.  На **боковой панели** отображается список URL-адресов, которые привели к тому, что сообщения записываются в журнал.  Например, это `log.js` связано с 11 сообщениями.  
    
    :::image type="complex" source="../media/console-sidebar-expanded-all-messages.msft.png" alt-text="Сообщения на консоли" lightbox="../media/console-sidebar-expanded-all-messages.msft.png":::
       Просмотр источника сообщений на боковой панели  
    :::image-end:::  
    
### Фильтрация по пользовательским сообщениям  

Более того, после того, как вы щелкните **сведения журнала**, сценарий вызывается `console.log('Hello, Console!')` для записи сообщения на консоль.  Сообщения, которые регистрируются из сценария JavaScript вроде этого, называются **сообщениями пользователей**.  В отличие от того, когда вы щелкните **Причина ошибки 404**, браузер записал `Error` сообщение о том, что запрошенный ресурс не найден.  Такие сообщения считаются **сообщениями браузера**.  Используйте **боковую панель** , чтобы отфильтровать сообщения браузера и показать только сообщения пользователей.  

1.  Выберите **9 пользовательских сообщений**.  Сообщения браузера скрыты.  
    
    :::image type="complex" source="../media/console-sidebar-user-messages.msft.png" alt-text="Сообщения на консоли" lightbox="../media/console-sidebar-user-messages.msft.png":::
       Фильтрация сообщений браузера  
    :::image-end:::  
    
1.  Выберите **13 сообщений** , чтобы снова Показать все сообщения.  

## Использование консоли рядом с любой другой панелью  

Что делать, если стили редактируются, но вам нужно быстро проверить журнал консоли на что-то?  Используйте денежный ящик.  

1.  Откройте вкладку **элементы** .  
1.  Выберите `Escape` .  Откроется вкладка " **консоль** " для **ящика** .  У него есть все функции панели консоли, которые использовались в этом учебнике.  
    
    :::image type="complex" source="../media/console-elements-drawer-console-sidebar-all-messages.msft.png" alt-text="Сообщения на консоли" lightbox="../media/console-elements-drawer-console-sidebar-all-messages.msft.png":::
         Вкладка « **консоль** » в **ящике**  
    :::image-end:::  
    
<!--## Next steps  -->

<!--
*   See [Console Reference][DevToolsConsoleApi] to explore more features and workflows related to the Console UI.
*   See [Console API Reference][DevToolsConsoleReference] to learn more about all of the `console` methods that were demonstrated in [View messages logged from JavaScript(#view-messages-logged-from-javascript) and explore the other `console` methods that were not covered in this tutorial.  
*   See [Get Started](/microsoft-edge/devtools-guide-chromium/#start) to explore what else you are able to do with DevTools.  -->  

## Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageExpandIcon]: ../media/expand-icon.msft.png  
[ImageShowConsoleSidebarIcon]: ../media/show-console-sidebar-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Microsoft Edge \ (Chromium \) Инструменты разработчика | Документы Microsoft"  
[DevToolsCommandMenu]: ../command-menu/index.md "Выполнение команд с помощью командного меню Microsoft Edge DevTools | Документы Microsoft"  
[DevToolsCustomizePlacement]: ../customize/placement.md "Изменение положения Microsoft Edge DevTools | Документы Microsoft"  
[DevToolsConsoleApi]: ./api.md "Справочник по API консоли | Документы Microsoft"  
[DevToolsConsoleReference]: ./reference.md "Справочник по консоли | Документы Microsoft"  

[GlitchDevToolsConsoleLogExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/console/log.html "Начало работы с сообщениями в журнале | Цепь"  

[MDNRegularExpressions]: https://developer.mozilla.org/docs/Web/JavaScript/Guide/Regular_Expressions "Регулярные выражения | MDN"  

[RegExrMain]: https://regexr.com "Регулярное выражение"  

[WikiStackTrace]: https://en.wikipedia.org/wiki/Stack_trace "Трассировка стека — Википедии"  
> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/console/log) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
