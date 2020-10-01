---
description: С помощью панели приложения можно просматривать, изменять и отлаживать манифесты веб-приложения, рабочие процессы служб и служебные кэши служб.
title: Отладка последовательного веб-приложения
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 7eb71d0d57d8a9227a54b921f15dfe434ad6e65b
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993606"
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





# Отладка последовательного веб-приложения   



С помощью панели **приложения** можно просматривать, изменять и отлаживать манифесты веб-приложения, рабочие процессы служб и служебные кэши служб.  

<!--Related Guides:  

*   [Progressive Web Apps](/web/progressive-web-apps)  -->

<!--TODO:  Link web "Progressive Web Apps" section when available. -->

В этом руководстве рассматриваются только прогрессивные возможности веб-приложений на панели **приложения** .  <!--If you're looking for help on the other panes, check out the last section of this guide, [Other Application panel guides](#other-application-panel-guides).  -->

<!--TODO:  Link to sections when available. -->

### Краткий обзор  

*   Используйте область **манифеста** для проверки манифеста веб-приложения и триггера Add to начальный экран Events.  
*   Область " **сотрудники службы** " используется для целого ряда задач, связанных с рабочими процессами, например для отмены регистрации или обновления службы, эмуляции извещающих событий, перехода в автономный режим или остановки рабочего процесса.  
*   Просмотр кэша рабочих процессов службы из области **хранилища кэша** .  
*   Отмена регистрации сотрудника службы и удаление всех хранилищ и кэшей с одним нажатием кнопки из области **очистки хранилища** .  
    
## Манифест веб-приложения   

Если вы хотите, чтобы пользователи смогли добавить ваше приложение на свой мобильный homescreens, вам понадобится манифест веб-приложения.  Манифест определяет, как приложение появляется на начальный экран, где можно направить пользователя при запуске из начальный экран и что приложение будет выглядеть при запуске.  

<!--Related Guides:  

*   [Improve user experiences with a Web App Manifest](/web/fundamentals/web-app-manifest)  
*   [Using App Install Banners](/web/fundamentals/app-install-banners)  -->

<!--TODO:  Link to sections when available. -->

После настройки манифеста вы можете проверить ее с помощью панели " **Манифест** " на панели " **приложение** ".  

:::image type="complex" source="./media/manifest-pane.msft.png" alt-text="Область «манифест»" lightbox="./media/manifest-pane.msft.png":::
   Область « **Манифест** »  
:::image-end:::  

*   Чтобы просмотреть источник манифеста, щелкните ссылку под меткой **манифест приложения** \ ( `https://airhorner.com/manifest.json` на предыдущем рисунке).  
<!-- *   Press the **Add to homescreen** button to simulate an Add to Homescreen event.  Check out the next section for more information.  -->  
*   В разделах " **удостоверение** " и " **Презентация** " отображаются только поля из источника манифеста в более удобном для пользователя дисплее.  
*   В разделе **значков** появится каждый заданный вами значок.  
    
<!--### Simulate Add to Homescreen events   -->

<!--A web app can only be added to a homescreen when the site is visited at least twice, with at least five minutes between visits.  While developing or debugging your Add to Homescreen workflow, this criteria can be inconvenient.  
The **Add to homescreen** button on the **App Manifest** pane lets you simulate Add to Homescreen events whenever you want.  -->

<!--You can test out this feature with the [Microsoft I/O 2016 progressive web app](https://events.alpahabet.com/io2016/), which has proper support for Add to Homescreen.  Clicking on **Add to Homescreen** while the app is open prompts Microsoft Edge to display the "add this site to your shelf" banner, which is the desktop equivalent of the "add to homescreen" banner for mobile devices.  -->

<!--  
:::image type="complex" source="./media/io.msft.png" alt-text="Область «манифест»" lightbox="./media/io.msft.png":::
   Add to desktop shelf  
:::image-end:::
-->  

<!--
> [!Tip]
> Keep the **Console** drawer open while simulating Add to Homescreen events.  The Console tells you if your manifest has any issues and logs other information about the Add to Homescreen lifecycle.  -->

<!--The **Add to Homescreen** feature cannot yet simulate the workflow for mobile devices.  Notice how the "add to shelf" prompt was triggered in the screenshot above, even though DevTools is in Device Mode.  However, if you can successfully add your app to your desktop shelf, then it'll work for mobile, too.  -->

<!-- TODO: Rework content after sample app is created. -->

<!--If you want to test out the genuine mobile experience, you can connect a real mobile device to DevTools via **remote debugging**, and then click the **Add to Homescreen** button \(on DevTools\) to trigger the "add to homescreen" prompt on the connected mobile device.  -->

<!--TODO:  Link Debug "remote debugging" sections when available. -->

## Обслуживание сотрудников   

ИТ-специалисты — это фундаментальная технология в будущем.  Они представляют собой сценарии, которые браузер работает в фоновом режиме, отделенные от веб-страницы.  Эти сценарии позволяют получить доступ к функциям, для которых не требуется взаимодействие с веб-страницей или пользователем, например извещающих уведомлений, фоновой синхронизации и автономным режимом работы.  

<!--Related Guides:  

*   [Intro to Service Workers](/web/fundamentals/primers/service-worker)  
*   [Push Notifications: Timely, Relevant, and Precise](/web/fundamentals/push-notifications)  -->  
    
<!--TODO:  Link to sections when available. -->  

Область " **сотрудники службы** " на панели **приложения** — это основное место в DevTools для проверки и отладки рабочих сотрудников.  

:::image type="complex" source="./media/service-workers-pane.msft.png" alt-text="Область «манифест»" lightbox="./media/service-workers-pane.msft.png":::
   Область " **сотрудники службы** "  
:::image-end:::  

*   Если сервисный сотрудник установлен на текущую открытую страницу, вы увидите ее в списке на этой панели.  Например, на предыдущем рисунке имеется сотрудник службы, установленный для области `https://weather-pwa-sample.firebaseapp.com` .  
*   Флажок **offline** перевод DevTools в автономный режим.  Это эквивалентно автономному режиму, доступному на панели " **сеть** ", или `Go offline` параметром в [меню "команды][DevtoolsCommandMenuIndex]".  
*   Флажок **обновить при повторной загрузке** вызывает принудительное обновление сотрудника службы при каждой загрузке страницы.  
*   Флажок **пропускать из сети** обходит сотрудника службы и заставляет браузер перейти к сети для запрашиваемых ресурсов.  
*   Кнопка " **Обновить** " выполняет разовое обновление указанного сотрудника службы.  
*   Кнопка " **Отправить** " эмулирует push-уведомление без полезной нагрузки \ (также называемой **Tickle**).  
*   Кнопка " **синхронизировать** " эмулирует событие синхронизации в фоновом режиме.  
*   Кнопка Отмена **регистрации** отменяет регистрацию указанного сотрудника службы.  Снимите флажок [Очистить хранилище](#clear-storage) , чтобы отменить регистрацию сотрудника службы и очистить хранение и кэширование при нажатии одной кнопки.  
*   **Исходная** строка, указывающая на то, что текущий запущенный сервисный рабочий процесс был установлен.  Ссылка — это имя исходного файла сотрудника службы.  Если щелкнуть ссылку, вы отправляете вам источник сотрудника службы.  
*   Строка **состояния** показывает состояние сотрудника службы.  ИДЕНТИФИКАЦИОНный номер рядом с зеленым индикатором состояния \ ( `#36` на предыдущем рисунке \) — для текущего активного сотрудника службы.  Рядом с состоянием отображается кнопка " **Пуск** ", а также кнопка " **остановить** " (если сотрудник службы остановлен)  Сотрудники служб должны быть остановлены и запущены браузером в любое время.  Явная остановка сотрудника службы с помощью кнопки " **остановить** " может смоделировать ее.  Остановка рабочего процесса — это отличный способ проверить работу вашего кода при запуске сотрудника службы.  Она часто обнаруживает ошибки из-за неправильного предположения о постоянном глобальном состоянии.  
*   Строка " **Клиенты** " указывает источник, на область которого выдается сотрудник службы.  Кнопка " **фокус** " особенно полезна, если вы включили флажок **Показать все** .  Если этот флажок установлен, в списке будут перечислены все зарегистрированные работники службы.  При нажатии кнопки **фокуса** рядом с сервисным сотрудником, работающим на другой вкладке, Microsoft Edge фокусируется на этой вкладке.  
    
Если сервисный рабочий процесс вызывает ошибки, появляется новая метка **ошибки** .  

<!--  
:::image type="complex" source="./media/sw-error.msft.png" alt-text="Область «манифест»" lightbox="./media/sw-error.msft.png":::
   Service worker with errors  
:::image-end:::
-->  

<!--TODO:  Capture Service Worker Errors sample when available. -->
<!--TODO:  Link Web "How tickle works" sections when available. -->

## Кэши рабочих процессов служб 

Область **кэширования кэша** предоставляет доступный только для чтения список ресурсов, которые были кэшированы с помощью [API кэша][MDNWebCacheAPI]\ (рабочий процесс-служба).  

:::image type="complex" source="./media/cache-pane-cache-storage-resources.msft.png" alt-text="Область «манифест»" lightbox="./media/cache-pane-cache-storage-resources.msft.png":::
   Область " **хранение кэша** "  
:::image-end:::  

> [!NOTE]
> При первом открытии кэша и добавлении в него ресурсов DevTools может не обнаружить изменения.  Перезагрузите страницу, и вы увидите кэш.  

Если открыто два или более кэша, вы увидите их в списке под раскрывающимся списком для **хранения кэша** .  

:::image type="complex" source="./media/cache-pane-cache-storage.msft.png" alt-text="Область «манифест»" lightbox="./media/cache-pane-cache-storage.msft.png":::
   Раскрывающийся список **хранилища кэша**  
:::image-end:::  

## Использование квоты 

Некоторые ответы в области **хранилища кэша** можно пометить как "непрозрачный".  Это относится к ответу, извлекаемому из другого источника, например из сети **CDN** или удаленного API, когда функция [CORS][FetchHttpCorsProtocol] не включена.  

<!--TODO:  Link Web "CDN" section when available. -->  
<!--TODO:  Link Web "opaque" section when available. -->

Чтобы не допустить утечек междоменных данных, нужно добавить дополнительное дополнение к размеру непрозрачного ответа, используемого для вычисления предельных квот хранилища \ (например, `QuotaExceeded` вызывается ли исключение \) и сообщается `navigator.storage` API.  

<!--TODO:  Link Estimating "`navigator.storage` API" sections when available. -->

Сведения об этом заполнении отличаются в зависимости от браузера, но для Microsoft Edge это означает, что **Минимальный размер** любого отдельного кэшированного непрозрачного ответа составляет [примерно 7 мегабайт][ChromiumIssues796060#c17].  Это необходимо учитывать при определении количества непрозрачных ответов, которые вы хотите кэшировать, так как вы можете легко превысить ограничения квоты хранилища, так как в противном случае вы ожидаете фактический размер непрозрачных ресурсов.  

Связанные направляющие:  

*   [Переполнение стека: какие ограничения применяются к непрозрачным откликам?][StackOverflowLimitationsForOpaqueResponses]  
<!--*   [Alphabet work container: Understanding Storage Quota](/web/tools/Alphabet-work-container/guides/storage-quota#beware_of_opaque_responses)  -->
    
<!--TODO:  Link Work container storage quota for opaque responses section when available. -->

## Очистка хранилища 

При разработке последовательного веб-приложения удобнее использовать область **очистки хранилища** .  В этой области можно отменить регистрацию сотрудников службы и очистить все кэши и хранилище с помощью одного нажатия кнопки.  <!--Check out the section below to learn more.  -->

<!--Related Guides:  

*   [Clear Storage](/iterate/manage-data/local-storage#clear-storage)  -->
    
<!--TODO:  Link to sections when available. -->

<!--## Other Application panel guides 

Check out the guides below for more help on the other panes of the **Application** panel.  

Related Guides:  

*   [Inspect page resources](/iterate/manage-data/page-resources)  
*   [Inspect and manage local storage and caches](/iterate/manage-data/local-storage)  -->
    
<!--TODO  -->

<!--  
 


-->  

<!-- links -->  

[DevtoolsCommandMenuIndex]: ./command-menu/index.md "Выполнение команд с помощью командного меню Microsoft Edge DevTools | Документы Microsoft"  

[ChromiumIssues796060#c17]: https://bugs.chromium.org/p/chromium/issues/detail?id=796060#c17 "Chromium дата_выпуска 796060: значение хранилища кэша выводится при каждом обновлении, когда код аналитики находится в HTML"  

[FetchHttpCorsProtocol]: https://fetch.spec.whatwg.org/#http-cors-protocol  

[MDNWebCacheAPI]: https://developer.mozilla.org/docs/Web/API/Cache "Cache-API | MDN"  

[StackOverflowLimitationsForOpaqueResponses]: https://stackoverflow.com/q/39109789/385997 "Переполнение стека: какие ограничения применяются к непрозрачным откликам?"  

<!--[WebEstimatingAvailableStorageSpace]: whats-new/2017/08/estimating-available-storage-space  -->
<!--[RemoteDebugging]: /debug/remote-debugging/remote-debugging  -->

<!--[WebHowPushWorks]: /web/fundamentals/push-notifications/how-push-works  -->  
<!--[WebGlossaryCDN]: /web/fundamentals/glossary#CDN  -->
<!--[WebGlossaryOpaque]: /web/fundamentals/glossary#opaque-response  -->

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/progressive-web-apps) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
