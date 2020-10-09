---
description: С помощью панели мультимедиа вы можете просматривать сведения и отлаживать проигрыватели мультимедиа на вкладке "браузер".
title: Просмотр и отладка сведений о проигрывателях мультимедиа
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/08/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: dfcf17861c0296e347007bc3a1a02a2b80661e6f
ms.sourcegitcommit: 912609aa49864e3363aaa3b245ff2aa4bec3fc3e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/08/2020
ms.locfileid: "11105213"
---
# Просмотр и отладка сведений о проигрывателях мультимедиа  

С помощью панели **медиа** в Microsoft Edge DevTools можно просматривать сведения и отлаживать проигрыватели мультимедиа на вкладке "браузер".  

## Открытие панели мультимедиа  

Панель " **мультимедиа** " — это основное место в DevTools для проверки проигрывателя мультимедиа на веб-странице.

1.  [Откройте DevTools][DevtoolsGuideChromiumOpen].  
1.  Чтобы открыть панель " **мультимедиа** ", нажмите кнопку **Настройка и управление DevTools** `...`  >  **дополнительных средств**  >  **мультимедиа**.  
    
    :::image type="complex" source="../media/media-panel-empty.msft.png" alt-text="Панель мультимедиа" lightbox="../media/media-panel-empty.msft.png":::
       Панель **мультимедиа**  
    :::image-end:::  
    
## Просмотр сведений о проигрывателях мультимедиа  

1.  Перейдите на веб-страницу с помощью универсального проигрывателя, например следующей веб-страницы.  
    
    [Максимизация производительности с помощью средств разработчика Edge][BingVideosSearchViewDetailMidE0BA14EC0E0D18C06C8DE0BA14EC0E0D18C06C8]  
    
1.  В меню **игрока** отображается проигрыватель мультимедиа.  
1.  Выберите игрока.  На вкладке **Свойства** отображаются свойства универсального проигрывателя.  
    
    :::image type="complex" source="../media/media-panel-view.msft.png" alt-text="Панель мультимедиа" lightbox="../media/media-panel-view.msft.png":::
       Свойства мультимедиа  
    :::image-end:::  
    
1.  Чтобы просмотреть все события проигрывателя мультимедиа, перейдите на вкладку **события** .  
    
    :::image type="complex" source="../media/media-panel-events.msft.png" alt-text="Панель мультимедиа" lightbox="../media/media-panel-events.msft.png":::
       События мультимедиа  
    :::image-end:::  
    
1.  Чтобы просмотреть журналы сообщений проигрывателя мультимедиа, выберите вкладку **сообщения** .  Вы можете отфильтровать сообщения по уровню или строке журнала.  
    
    :::image type="complex" source="../media/media-panel-messages.msft.png" alt-text="Панель мультимедиа" lightbox="../media/media-panel-messages.msft.png":::
       Мультимедийные сообщения  
    :::image-end:::  
    
1.  На вкладке **временная шкала** воспроизведение мультимедиа и состояние буфера отображаются в режиме реального времени.  
    
    :::image type="complex" source="../media/media-panel-timeline.msft.png" alt-text="Панель мультимедиа" lightbox="../media/media-panel-timeline.msft.png":::
       Временная шкала мультимедиа  
    :::image-end:::  
    
### Удаленная отладка  

Просмотр сведений о проигрывателях мультимедиа на устройстве с ОС Windows или macOS с компьютера Android.  

1.  Чтобы настроить удаленную отладку, перейдите в раздел Начало [работы с удаленно удаленной отладкой устройств с Android][DevtoolsGuideChromiumRemoteDebuggingIndex].  
1.  Удаленное Просмотр сведений о проигрывателях мультимедиа.  
    
    <!-- TODO: recreate image using an Android device -->  
    <!--  
    :::image type="complex" source="../media/media-panel-remote-debug.msft.png" alt-text="Панель мультимедиа" lightbox="../media/media-panel-remote-debug.msft.png":::
       Remote debugging  
    :::image-end:::  
    -->  
    
## Скрытие и отображение проигрывателей мультимедиа  

Иногда вы запускаете несколько проигрывателей мультимедиа на веб-странице или с помощью одной вкладки браузера для просмотра различных веб-страниц с помощью мультимедийных проигрывателей.

Вы можете скрыть \ (или показать) каждый проигрыватель мультимедиа для более удобного процесса отладки.  

1.  Переход на несколько различных веб-страниц видео с помощью одной вкладки браузера.  
1.  Чтобы скрыть проигрыватели мультимедиа, выполните одно из указанных ниже действий.  
    *   Чтобы скрыть один проигрыватель мультимедиа, наведите на него указатель мыши, откройте контекстное меню, а затем выберите команду **Скрыть проигрыватель**.  
    *   Чтобы скрыть все другие проигрыватели мультимедиа, наведите указатель мыши на проигрыватель мультимедиа, откройте контекстное меню, а затем выберите команду **Скрыть все другие**.  
    
    :::image type="complex" source="../media/media-panel-hide-show.msft.png" alt-text="Панель мультимедиа" lightbox="../media/media-panel-hide-show.msft.png":::
       Скрытие проигрывателей мультимедиа  
    :::image-end:::  
    
## Экспорт сведений о проигрывателе мультимедиа  

1.  Чтобы загрузить сведения о проигрывателе мультимедиа в формате JSON, наведите указатель мыши на проигрыватель мультимедиа, откройте контекстное меню (щелкните правой кнопкой мыши и выберите команду **сохранить сведения о проигрывателе**).  
    
    :::image type="complex" source="../media/media-panel-save.msft.png" alt-text="Панель мультимедиа" lightbox="../media/media-panel-save.msft.png":::
       Экспорт мультимедийных данных  
    :::image-end:::  
    
## Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumOpen]: ../open.md "Открыть Microsoft Edge DevTools"  

[DevtoolsGuideChromiumRemoteDebuggingIndex]: ../remote-debugging/index.md "Начало работы с удаленными отладочными устройствами Android | Документы Microsoft"  

[BingVideosSearchViewDetailMidE0BA14EC0E0D18C06C8DE0BA14EC0E0D18C06C8]: https://www.bing.com/videos/search?view=detail&mid=DE0BA14EC0E0D18C06C8DE0BA14EC0E0D18C06C8 "Максимально подвысьте производительность с помощью средств разработчика Edge | Видеоролик Bing"  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница [будет найдена, и](https://developers.google.com/web/tools/chrome-devtools/media-panel/index) ее можно создать с помощью [Jecelyn Yeen][JecelynYeen] \ (разработчик отвечает, Chrome DevTools \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  

