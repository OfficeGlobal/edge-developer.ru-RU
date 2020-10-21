---
description: С помощью панели безопасности убедитесь, что страница полностью защищена HTTPS.
title: Общие сведения о проблемах с безопасностью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 09f7e641ddd8da74c361980b9ce61b212a8477fe
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125386"
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
1.  Перейдите на вкладку " **Безопасность** ", чтобы открыть панель " **Безопасность** ".  
    
    :::image type="complex" source="../media/security-security-overview-secure.msft.png" alt-text="Панель &quot;безопасность&quot;" lightbox="../media/security-security-overview-secure.msft.png":::
       Панель " **Безопасность** "  
    :::image-end:::  
    
## Распространенные проблемы  

### Небезопасные основные источники  

Если основной источник страницы небезопасен, в **обзоре безопасности** указано, что **Эта страница не является безопасной**.  

:::image type="complex" source="../media/security-security-overview-non-secure.msft.png" alt-text="Панель &quot;безопасность&quot;" lightbox="../media/security-security-overview-non-secure.msft.png":::
   Небезопасная страница  
:::image-end:::  

Эта проблема возникает, когда ваш URL-адрес, который вы посещали, запрашивался по протоколу HTTP.  Для обеспечения безопасности необходимо запросить его по протоколу HTTPS.  Например, если вы посмотрите на URL-адрес в адресной строке, скорее всего, он выглядит примерно так `http://example.com` .  Чтобы защитить этот URL-адрес, сделайте это `https://example.com` .  

Если вы уже настроили HTTPS на сервере, все, что нужно сделать, чтобы устранить эту проблему, — настроить сервер для перенаправления всех HTTP-запросов на HTTPS.  

Если вы не настроили HTTPS на сервере, [давайте шифрованием][LetsEncrypt] обеспечивается бесплатный и достаточно простой способ запуска процесса.  Вы также можете размещать сайт в сети CDN.  По умолчанию в настоящее время используются наиболее важные сайты узлов сети CDN на HTTPS.  

> [!TIP]
> Использование подсказки по [протоколу HTTPS][WebhintUseHttps] в этой [подсказке][Webhint] может помочь автоматизировать процесс, чтобы все HTTP-запросы направлялись на HTTPS.  

### Смешанное содержимое  

**Смешанное содержимое** указывает на то, что основной источник страницы является безопасным, но страница запрашивает ресурсы из незащищенных источников.  Смешанные страницы содержимого защищены только частично, так как содержимое HTTP доступно для прослушивания и уязвимо для атак "злоумышленник в середине".  

:::image type="complex" source="../media/security-security-overview-mixed-secure.msft.png" alt-text="Панель &quot;безопасность&quot;" lightbox="../media/security-security-overview-mixed-secure.msft.png":::
   Смешанное содержимое  
:::image-end:::  

На предыдущем рисунке на панели " **сеть" выберите Просмотр 1 запрос** , чтобы открыть панель **Network (сеть** ) и применить `mixed-content:displayed` фильтр, чтобы в **сетевом журнале** отображались не безопасные ресурсы.  

:::image type="complex" source="../media/security-network-filter.msft.png" alt-text="Панель &quot;безопасность&quot;" lightbox="../media/security-network-filter.msft.png":::
   Смешанные ресурсы в **сетевом журнале**  
:::image-end:::  

## Просмотреть подробные сведения  

### Просмотр сертификата основного источника  

В разделе **Общие сведения о безопасности**выберите **Просмотр сертификата** для быстрого проверки сертификата для основного источника.  

:::image type="complex" source="../media/security-security-overview-secure-view-certificate.msft.png" alt-text="Панель &quot;безопасность&quot;" lightbox="../media/security-security-overview-secure-view-certificate.msft.png":::
   Основной сертификат источника  
:::image-end:::  

### Просмотр сведений об источнике  

Щелкните одну из записей на левой панели навигации, чтобы просмотреть подробные сведения об источнике.  На странице сведения вы можете просмотреть сведения о подключении и сертификате.  Информация о прозрачности сертификата также отображается, если она доступна.  

:::image type="complex" source="../media/security-security-overview-mixed-secure-main-origin.msft.png" alt-text="Панель &quot;безопасность&quot;" lightbox="../media/security-security-overview-mixed-secure-main-origin.msft.png":::
   Сведения о главном источнике  
:::image-end:::  

## Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Инструменты разработчика Microsoft EDGE (Chromium) | Документы Microsoft"  
[DevToolsOpen]: ../open.md "Открыть Microsoft Edge DevTools | Документы Microsoft"  
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
