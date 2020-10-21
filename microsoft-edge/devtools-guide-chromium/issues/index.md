---
description: Используйте средство "проблемы" для поиска и устранения проблем с веб-сайтом.
title: Поиск и устранение проблем с помощью средства Microsoft Edge DevTools "вопросы"
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 4691db9542ecff93d1b59e243844109e0c730d23
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "11124728"
---
<!-- Copyright Sam Dutton 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  

# Поиск и устранение проблем с помощью средства Microsoft Edge DevTools "вопросы"  

Инструмент " **вопросы** " в Microsoft Edge DevTools сокращает усталость уведомлений и бессрочные элементы **консоли**.  Используйте его для поиска решений проблем, обнаруженных браузером, например проблем с файлами cookie и смешанного содержимого.  

> [!NOTE]
> В Microsoft Edge 84 средство " **проблемы** " поддерживает три типа проблемы:  
> *   [Проблемы с cookie-файлами][MDNSameSiteCookies]  
> *   [Смешанное содержимое][MDNMixedContent]  
> *   [Проблемы с COEP][W3CCOEPSpec]
> 
> Планы Microsoft Edge DevTools Teams, чтобы поддерживать дополнительные типы проблем в будущих версиях Microsoft Edge.  

## Открытие инструмента "проблемы" в ящике DevTools  

1.  Посетите страницу, например [SameSite-Sandbox.glitch.Me][GlitchSamesiteSandbox], которая включает проблемы, которые необходимо устранить.  
1.  [Откройте DevTools][DevtoolsOpen].  
1.  :::row:::
       :::column span="":::
          Нажмите кнопку **Перейти к разделу "проблемы** " на желтой панели предупреждения.  
          
          :::image type="complex" source="../media/issues-open-issues-tab.msft.png" alt-text="Нажатие кнопки &quot;проблемы&quot; на желтой полосе предупреждения при обнаружении проблем" lightbox="../media/issues-open-issues-tab.msft.png":::
             Кнопка **Перейти к проблемам** на желтой полосе предупреждения при обнаружении проблем.  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          Кроме того, можно выбрать пункт " **проблемы** " в меню " **другие инструменты** ".  
          
          :::image type="complex" source="../media//issues-more-tools-menu.msft.png" alt-text="Нажатие кнопки &quot;проблемы&quot; на желтой полосе предупреждения при обнаружении проблем" lightbox="../media//issues-more-tools-menu.msft.png":::
             Средство " **вопросы** " в меню " **другие инструменты** "  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
1.  При необходимости нажмите кнопку **перезагрузить страницу** .  
    
    :::image type="complex" source="../media/issues-tab-before-refresh.msft.png" alt-text="Нажатие кнопки &quot;проблемы&quot; на желтой полосе предупреждения при обнаружении проблем" lightbox="../media/issues-tab-before-refresh.msft.png":::
       Инструмент " **проблемы** " в DevTools ящике с кнопкой " **перезагрузить страницу** "  
    :::image-end:::  

    Проблемы, обнаруженные в **консоли** , довольно сложно понять, например предупреждения о cookie-файлах на рисунке ниже.  На основе обнаруженных проблем может быть не ясно, что необходимо сделать.  
    
    :::image type="complex" source="../media/issues-tab-after-refresh.msft.png" alt-text="Нажатие кнопки &quot;проблемы&quot; на желтой полосе предупреждения при обнаружении проблем" lightbox="../media/issues-tab-after-refresh.msft.png":::
       Инструмент " **проблемы** " в денежном ящике DevTools с тремя неполадками с файлами cookie  
    :::image-end:::  
    
## Просмотр элементов в инструменте "проблемы"  

Инструмент " **проблемы** " в ящике DevTools представляет предупреждения в структурированных, агрегатных и возможных действиях.  

1.  Выберите элемент в инструменте " **вопросы** ", чтобы получить инструкции по устранению проблемы и поиску затронутых ресурсов.  
    
    :::image type="complex" source="../media/issues-tab-issue-open.msft.png" alt-text="Нажатие кнопки &quot;проблемы&quot; на желтой полосе предупреждения при обнаружении проблем" lightbox="../media/issues-tab-issue-open.msft.png":::
       **Пометка cookie-файлов другого сайта как безопасной проблемы при** открытии в инструменте " **вопросы** "  
    :::image-end:::  
    
    Каждый элемент состоит из четырех компонентов:  
    
    *   Заголовок, описывающий эту ошибку.  
    *   Описание, предоставляющее контекст и решение.  
    *   Раздел " **уязвимые ресурсы** ", который содержит ссылки на ресурсы в соответствующем DevTools контексте, например на панели "сеть".  
    *   Ссылки на другие инструкции.  
    
1.  Чтобы просмотреть подробные сведения, выберите элементы в **затронутых ресурсах** .  В следующем примере **cookie-файлы межсайтового сайта как безопасные** вопросы влияют на один файл cookie и два запроса.  
    
    :::image type="complex" source="../media/issues-tab-affected-resources.msft.png" alt-text="Нажатие кнопки &quot;проблемы&quot; на желтой полосе предупреждения при обнаружении проблем" lightbox="../media/issues-tab-affected-resources.msft.png":::
       Затронутые ресурсы, открытые в инструменте " **вопросы** " в ящике DevTools  
    :::image-end:::  
    
## Просмотр проблем в контексте  

1.  Выберите ссылку на ресурс, чтобы просмотреть элемент в соответствующем контексте в DevTools.  В следующем примере выберите `samesite-sandbox.glitch.me` в разделе **запросы** для отображения файлов cookie, вложенных в запрос.  
    
    :::image type="complex" source="../media/issues-tab-view-request.msft.png" alt-text="Нажатие кнопки &quot;проблемы&quot; на желтой полосе предупреждения при обнаружении проблем" lightbox="../media/issues-tab-view-request.msft.png":::
       Просмотр затрагиваемого cookie-файла на панели DevTools **Network**  
    :::image-end:::  

1.  Прокрутите экран, чтобы просмотреть элемент с проблемой: в следующем примере показан `ck02` объект cookie.  Наведите указатель мыши на столбец **SameSite** , чтобы увидеть `None` значение, которое обнаружено проблемой.  
    
    :::image type="complex" source="../media/issues-tab-view-issue.msft.png" alt-text="Нажатие кнопки &quot;проблемы&quot; на желтой полосе предупреждения при обнаружении проблем" lightbox="../media/issues-tab-view-issue.msft.png":::
       `None` значение в столбце " **SameSite** " для `ck02` файла cookie на панели DevTools **Network (сеть** )  
    :::image-end:::  

## Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsOpen]: ../open.md "Открыть Microsoft Edge DevTools | Документы Microsoft"  

[GlitchSamesiteSandbox]: https://samesite-sandbox.glitch.me "Проверка файлов cookie SameSite | Цепь"  

[MDNSameSiteCookies]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie/SameSite "SameSite cookie-файлы | MDN"  
[MDNMixedContent]: https://developer.mozilla.org/docs/Web/Security/Mixed_content "Смешанное содержимое | MDN"  

[W3CCOEPSpec]: https://wicg.github.io/cross-origin-embedder-policy "Политика внедрения для разных источников | Группа сообщества веб-Incubator"  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница [будет найдена, и](https://developers.google.com/web/tools/chrome-devtools/issues/index) ее можно создать с помощью [SAM Dutton][SamDutton] \ (разработчик отвечает \).  
[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[SamDutton]: https://developers.google.com/web/resources/contributors/samdutton  
