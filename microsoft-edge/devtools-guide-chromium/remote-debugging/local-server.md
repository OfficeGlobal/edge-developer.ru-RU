---
description: Разведите сайт на веб-сервере разработчика, а затем получите доступ к содержимому с устройства Android.
title: Доступ к локальным серверам
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: f994092460f090743119d7304bfe12aa28556b19
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125414"
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

# Доступ к локальным серверам  

Размещение сайта на веб-сервере разработчика, а затем доступ к содержимому с устройства Android.  

С помощью USB-кабеля и Microsoft Edge DevTools, запустите сайт с компьютера для разработки и просмотрите сайт на устройстве с Android.  

### Краткий обзор  

*   Переадресация портов позволяет просматривать контент, размещенный на вашем компьютере, на котором работает веб-сервер, на устройстве с Android.  
*   Если веб-сервер использует настраиваемый домен, настройте на устройстве с Android доступ к контенту в этом домене с помощью собственного сопоставления доменов.  

## Настройка переадресации портов  

Переадресация портов позволяет устройству Android получать доступ к содержимому, размещенному на веб-сервере, работающем на компьютере разработчика.  Переадресация порта работает путем создания прослушивающего порта TCP на устройстве с Android, которое сопоставляется с портом TCP на компьютере разработчика.  Трафик между портами проходит через USB-соединение между устройством с Android и компьютером для разработки, поэтому подключение не зависит от конфигурации сети.  

Чтобы включить перенаправление портов, выполните указанные ниже действия.  

1.  Настройка [удаленной отладки][RemoteDebuggingGettingStarted] между компьютером разработчика и устройством с Android.  Когда вы закончите работу, вы увидите устройство с Android в левом меню диалогового окна **Проверка устройств** и индикатор состояния **подключен** .  
1.  В диалоговом окне **Проверка устройств** в DevTools включите **переадресацию порта**.  
1.  Нажмите кнопку **Добавить правило**.  
    
    :::image type="complex" source="../media/remote-debugging-remote-devices-devices-port-forwarding-add-rule.msft.png" alt-text="Добавление правила переадресации портов" lightbox="../media/remote-debugging-remote-devices-devices-port-forwarding-add-rule.msft.png":::
       Добавление правила переадресации портов  
    :::image-end:::  
    
1.  В поле " **порт устройства** " слева введите `localhost` номер порта, с которого вы хотите получить доступ к сайту на устройстве с Android.  Например, если вы хотите получить доступ к сайту из `localhost:5000` ввода `5000` .  
1.  В текстовом поле " **локальный адрес** " щелкните правой кнопкой мыши IP-адрес или имя узла, на котором расположен сайт, который находится на компьютере разработчика, а затем укажите номер порта.  Например, если ваш веб-сайт запущен на `localhost:7331` входе `localhost:7331` .  
1.  Нажмите кнопку **Добавить**.  
    
Переадресация порта теперь настроена.  Просмотрите индикатор состояния для порта на вкладке на вашем устройстве в диалоговом окне **Проверка устройств** .  

:::image type="complex" source="../media/remote-debugging-remote-devices-devices-port-forwarding-5000-edge-user-agent.msft.png" alt-text="Добавление правила переадресации портов" lightbox="../media/remote-debugging-remote-devices-devices-port-forwarding-5000-edge-user-agent.msft.png":::
   Состояние переадресации порта  
:::image-end:::  

Чтобы просмотреть содержимое, откройте приложение Microsoft EDGE на устройстве с Android и перейдите к `localhost` порту, который вы указали в поле " **порт устройства** ".  Например, если вы ввели `5000` поле, перейдите на страницу `localhost:5000` .  

## Сопоставление с пользовательскими локальными доменами  

С помощью настраиваемого сопоставления доменов вы можете просматривать содержимое на устройстве с Android с веб-сервера на компьютере разработчика, использующем настраиваемый домен.  

Например, предположим, что ваш сайт использует библиотеку JavaScript стороннего поставщика, которая работает только в домене `microsoft-edge.devtools` .  Таким образом, вы создаете запись в `hosts` файле на компьютере разработчика, чтобы сопоставить этот домен с доменом `localhost` (например, `127.0.0.1 microsoft-edge.devtools` \).  После настройки сопоставления домена и переадресации порта просмотрите сайт на своем устройстве с Android по URL-адресу `microsoft-edge.devtools` .  

### Настройка пересылки порта на прокси-сервер  

Для сопоставления собственного домена необходимо запустить прокси-сервер на компьютере разработчика.  Ниже приведены примеры прокси-серверов: [Чарльз][CharlesWebDebuggingProxy], [Squid][SquidOptimisingWebDelivery]и [Fiddler][FiddlerWebDebuggingProxy].  

Чтобы настроить перенаправление порта на прокси-сервер, выполните указанные ниже действия.  

1.  Запустите прокси-сервер и запишите порт, который он использует.  
    
    > [!NOTE]
    > Прокси-сервер и веб-сервер должны работать на разных портах.  
    
1.  Настройка [пересылки порта](#set-up-port-forwarding) на устройство с Android.  В поле **Local Address (локальный адрес** ) введите `localhost:` за ним порт, на котором работает прокси-сервер.  Например, если он запущен на порте `8000` , перейдите к `localhost:8000` .  В поле **порт устройства** введите номер, который будет прослушивать ваше устройство с Android, например `3333` .  
    
### Настройка параметров прокси-сервера на устройстве  

Затем необходимо настроить устройство Android для взаимодействия с прокси-сервером.  

1.  На устройстве с Android перейдите в раздел **Параметры**  >  **Wi-Fi**.  
1.  Long-нажимайте имя сети, к которой вы подключены в данный момент.  
    
    > [!NOTE]
    > Параметры прокси-сервера применяются к каждой сети.  
    
1.  Выберите команду **изменить сеть**.  
1.  Нажмите кнопку **Дополнительные параметры**.  Отображение параметров прокси-сервера.  
1.  Откройте меню **прокси** и выберите пункт **вручную**.  
1.  В поле **имя HostName прокси-сервера** введите `localhost` .  
1.  В поле порт **прокси-сервера** введите номер порта, который вы ввели для **порта устройства** в предыдущем разделе.  
1.  Нажмите кнопку **сохранить**.  
    
С помощью этих параметров устройство перенаправляет все свои запросы на прокси-сервер на компьютере разработчика.  Прокси-сервер создает запросы от имени вашего устройства, поэтому запросы к своему пользовательскому домену разрешаются надлежащим образом.  

Теперь вы можете получать доступ к настраиваемым доменам на устройстве с Android так же, как и на компьютере разработчика.  

Если веб-сервер не работает с нестандартным портом, не забудьте указать порт при запросе содержимого с устройства с Android.  Например, если ваш веб-сервер использует собственный домен `microsoft-edge.devtools` для порта, то `7331` при просмотре сайта с устройства Android вы должны использовать URL-адрес `microsoft-edge.devtools:7331` .  

> [!TIP]
> Чтобы возобновить обычный просмотр, не забудьте вернуть параметры прокси-сервера на устройстве с Android после отключения от компьютера для разработки.  

## Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[RemoteDebuggingGettingStarted]: ./index.md "Начало работы с удаленными отладочными устройствами Android | Документы Microsoft"  

[CharlesWebDebuggingProxy]: https://www.charlesproxy.com "Прокси-сервер отладчика Чарльз"  

[SquidOptimisingWebDelivery]: https://www.squid-cache.org "Squid: оптимизация веб-доставки"  

[FiddlerWebDebuggingProxy]: https://www.telerik.com/fiddler "Прокси-сервер для Fiddler без поддержки бесплатной отладки"  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/local-server) и [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \) и [Meggin Kearney][MegginKearney] \ (технический редактор \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
