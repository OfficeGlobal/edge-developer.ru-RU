---
description: Сведения о том, как найти сетевые проблемы на панели "сеть" в Microsoft Edge DevTools.
title: Справочные материалы по неполадкам в сети
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: ccd78c34a50bf235416df58aad28df9253b1b24e
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993375"
---
<!-- Copyright Kayce Basques and Jonathan Garbee

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->





# Руководство по сетевым проблемам   




В этом руководстве показано, как определить сетевые проблемы или возможности оптимизации на панели "сеть" Microsoft Edge DevTools.  

Ознакомьтесь со [статьей][NetworkPerformance] "Начало работы", чтобы ознакомиться с основными понятиями панели " **сеть** ".  

## Запросы, поставленные в очередь или остановленные   

**Симптомы**  

Шесть запросов загружаются одновременно.  После этого серии запросов будут помещены в очередь или остановлены.  После завершения одного из шести первых запросов запускается один из запросов в очереди.  

На **каскаде** на приведенном ниже рисунке первые шесть запросов `edge-iconx1024.msft.png` актива запускаются одновременно.  Последующие запросы загружаются до тех пор, пока не завершится один из этих шести первоначальных элементов.  

:::image type="complex" source="../media/network-network-disabled-cache-resources-queue.msft.png" alt-text="Пример списка в очереди или остановленного ряда на панели &quot;сеть&quot;" lightbox="../media/network-network-disabled-cache-resources-queue.msft.png":::
   Пример списка в очереди или остановленного ряда на панели " **сеть** "  
:::image-end:::  

**Причины**  

Слишком много запросов выполняется в одном домене.  Для подключений HTTP/1.0 или HTTP/1.1 Microsoft Edge допускает не более шести одновременных подключений TCP на одном узле.  

**Исправления**  

*   Реализуйте сегментирование доменов, если необходимо использовать HTTP/1.0 или HTTP/1.1.  
*   Используйте HTTP/2.  Не используйте сегментирование доменов с протоколом HTTP/2.  
*   Удалите или отложите ненужные запросы, чтобы загрузить критические запросы.  
    
## Медленное время до первого байта (TTFB)   

**Симптомы**  

Запрос тратит много времени на ожидание получения первого байта с сервера.  

На рисунке ниже показана длинная зеленая полоса в **каскаде** , указывающая на то, что запрос был выполнен в течение длительного времени.  Это было смоделировано с помощью профиля, ограничивающего скорость сети и добавляя задержку.  

:::image type="complex" source="../media/network-network-resources-using-dial-up-profile.msft.png" alt-text="Пример списка в очереди или остановленного ряда на панели &quot;сеть&quot;" lightbox="../media/network-network-resources-using-dial-up-profile.msft.png":::
   Пример запроса с медленным временем до получения первого байта  
:::image-end:::  

**Причины**  

*   Соединение между клиентом и сервером происходит медленно.  
*   Скорость ответа сервера не отвечает.  Разведите сервер на локальный компьютер, чтобы определить, является ли это подключение или медленный сервер.  Если вы по-прежнему получаете очень много времени на первый байт \ (TTFB \) при доступе к локальному серверу, сервер работает медленно.  
    
**Исправления**  

*   Если соединение медленное, разрешите размещение содержимого в сети CDN или изменение поставщиков услуг размещения.  
*   Если сервер работает медленно, рассматривайте запросы к базе данных, реализуйте кэш или изменяйте конфигурацию сервера.  
    
## Медленная загрузка содержимого   

**Симптомы**  

Загрузка запроса занимает много времени.  

На приведенном ниже рисунке показана длинная синяя полоса в **каскаде** рядом с форматом PNG, поэтому загрузка занимает много времени.  

:::image type="complex" source="../media/network-network-resources-edge-devtools.msft.png" alt-text="Пример списка в очереди или остановленного ряда на панели &quot;сеть&quot;" lightbox="../media/network-network-resources-edge-devtools.msft.png":::
   Пример запроса, загрузка которого занимает много времени  
:::image-end:::  

**Причины**  

*   Соединение между клиентом и сервером происходит медленно.  
*   Загружается много контента.  
    
**Исправления**  

*   Возможно, вы размещаете содержимое в сети CDN или меняете поставщиков услуг размещения.  
*   Уменьшите количество байтов, оптимизируя запросы.  
    
## Сведения о Contribute  

Есть ли у вас сетевая проблема, которая должна быть добавлена в это руководство?  

*   Отправить твит на [@EdgeDevTools][MicrosoftEdgeTweet].  
*   Выберите **Отправить отзыв** \ ( ![ Отправить отзыв ][ImageSendFeedbackIcon] \) в DevTools или нажмите клавиши `Alt` + `Shift` + `I` \ (Windows \) или `Option` + `Shift` + `I` \ (macOS \), чтобы предоставить отзыв или запрос функций.  
*   [Открыть вопрос][WebFundamentalsIssue] в репозитории документов.  
    
<!--  
  


-->  

<!-- image links -->  

[ImageSendFeedbackIcon]: ../media/smile-icon.msft.png  

<!-- links -->  

[NetworkPerformance]: ./index.md "Проверка активности сети в Microsoft Edge DevTools | Документы Microsoft"  

[MicrosoftEdgeTweet]: https://twitter.com/intent/tweet?text=@EdgeDevTools%20[Network%20Issues%20Guide%20Suggestion]  

[WebFundamentalsIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=%5BDevTools%20Network%20Issues%20Guide%20Suggestion%5D "Новая ошибка — MicrosoftDocs/Edge-разработчик"  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница размещается [здесь](https://developers.google.com/web/tools/chrome-devtools/network/issues) и разрабатывается с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \) и [Джонатан-искаженного][JonathanGarbee] (эксперта Google Developer, для Web Technology).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[JonathanGarbee]: https://developers.google.com/web/resources/contributors/jonathangarbee
