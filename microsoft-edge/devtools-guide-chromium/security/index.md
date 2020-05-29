---
title: Общие сведения о проблемах с безопасностью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: 05112d5270f41ce83daa935b8137c4a773ad25a0
ms.sourcegitcommit: 4c24edbd1c591914cb4109511534851570a614cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611912"
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





# Общие сведения о проблемах с безопасностью Microsoft Edge DevTools   

  

<!--Use the **Security** Panel in [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to make sure HTTPS is properly implemented on a page.  See **Why HTTPS Matters** to learn why every website should be protected with HTTPS, even sites that do not handle sensitive user data.  -->  

<!--todo: add section when why-https is available -->  

## Открытие панели безопасности   

Панель **безопасности** — это основное место в DevTools для проверки безопасности страницы.  

1.  [Откройте DevTools][DevToolsOpen].  

1.  Щелкните вкладку " **Безопасность** ", чтобы открыть панель " **Безопасность** ".  
    
    > ##### Рис. 1  
    > Панель "безопасность"  
    > ![Панель "безопасность"][ImageSecurityPanel]  
    
## Распространенные проблемы   

### Небезопасные основные источники   

Если основной источник страницы небезопасен, в **обзоре безопасности** указано, что **Эта страница не является безопасной**.  

> ##### Рисунок 2  
> Небезопасная страница  
> ![Небезопасная страница][ImageNonSecurePage]  

Эта проблема возникает, когда ваш URL-адрес, который вы посещали, запрашивался по протоколу HTTP.  Для обеспечения безопасности необходимо запросить его по протоколу HTTPS.  Например, если вы посмотрите на URL-адрес в адресной строке, скорее всего, он выглядит примерно так `http://example.com` .  Чтобы защитить этот URL-адрес, сделайте это `https://example.com` .  

Если вы уже настроили HTTPS на сервере, все, что нужно сделать, чтобы устранить эту проблему, — настроить сервер для перенаправления всех HTTP-запросов на HTTPS.  

Если вы не настроили HTTPS на сервере, [давайте шифрованием][LetsEncrypt] обеспечивается бесплатный и достаточно простой способ запуска процесса.  Вы также можете размещать сайт в сети CDN.  По умолчанию в настоящее время используются наиболее важные сайты узлов сети CDN на HTTPS.  

> [!TIP]
> Использование подсказки по [протоколу HTTPS][WebhintUseHttps] в этой [подсказке][Webhint] может помочь автоматизировать процесс, чтобы все HTTP-запросы направлялись на HTTPS.  

### Смешанное содержимое   

**Смешанное содержимое** указывает на то, что основной источник страницы является безопасным, но страница запрашивает ресурсы из незащищенных источников.  Смешанные страницы содержимого защищены только частично, так как содержимое HTTP доступно для прослушивания и уязвимо для атак "злоумышленник в середине".  

> ##### Рисунок3  
> Смешанное содержимое  
> ![Смешанное содержимое][ImageMixedContent]  

На [рис. 3](#figure-3)щелкните **Просмотреть 1 запрос на панели "сеть** ", чтобы открыть панель " **сеть** " и применить `mixed-content:displayed` фильтр, чтобы в **журнале сети** отображались только небезопасные ресурсы.  

> ##### Рисунок4  
> Смешанные ресурсы в сетевом журнале  
> ![Смешанные ресурсы в сетевом журнале][ImageMixedResourcesNetworkLog]  

## Просмотреть подробные сведения   

### Просмотр сертификата основного источника   

В разделе " **Общие сведения о безопасности**" щелкните ссылку **Просмотр сертификата** для быстрого проверки сертификата для основного источника.  

> ##### Рисунок 5  
> Основной сертификат источника  
> ![Основной сертификат источника][ImageCertificate]  

### Просмотр сведений об источнике   

Щелкните одну из записей на левой панели навигации, чтобы просмотреть подробные сведения об источнике.  На странице сведения вы можете просмотреть сведения о подключении и сертификате.  Информация о прозрачности сертификата также отображается, если она доступна.  

> ##### Рисунок6  
> Сведения о главном источнике  
> ![Сведения о главном источнике][ImageOriginDetails]  

 



<!-- image links -->  

[ImageSecurityPanel]: /microsoft-edge/devtools-guide-chromium/media/security-security-overview-secure.msft.png "Рисунок 1: панель "безопасность""  
[ImageNonSecurePage]: /microsoft-edge/devtools-guide-chromium/media/security-security-overview-non-secure.msft.png "Рисунок 2: небезопасная страница"  
[ImageMixedContent]: /microsoft-edge/devtools-guide-chromium/media/security-security-overview-mixed-secure.msft.png "Рисунок 3: смешанное содержимое"  
[ImageMixedResourcesNetworkLog]: /microsoft-edge/devtools-guide-chromium/media/security-network-filter.msft.png "Рисунок 4: смешанные ресурсы в сетевом журнале"  
[ImageCertificate]: /microsoft-edge/devtools-guide-chromium/media/security-security-overview-secure-view-certificate.msft.png "Рисунок 5: сертификат основного источника"  
[ImageOriginDetails]: /microsoft-edge/devtools-guide-chromium/media/security-security-overview-mixed-secure-main-origin.msft.png "Рисунок 6: сведения о главном источнике"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Инструменты разработчика Microsoft EDGE (Chromium)"  
[DevToolsOpen]: /microsoft-edge/devtools-guide-chromium/open "Открыть Microsoft Edge DevTools"  


[LetsEncrypt]: https://letsencrypt.org "Шифрование-бесплатные сертификаты SSL/TLS"  

[Webhint]: https://webhint.io "Подсказка"  
[WebhintUseHttps]: https://webhint.io/docs/user-guide/hints/hint-https-only "Использование HTTPS | Документация по подсказкам"  

<!--[mixed]: /web/fundamentals/security/prevent-mixed-content/what-is-mixed-content ""  -->

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/security/index) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  