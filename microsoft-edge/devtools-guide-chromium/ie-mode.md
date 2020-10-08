---
description: Режим IE и Microsoft EDGE (Chromium) DevTools
title: Режим Internet Explorer и DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/08/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools, ie11, Internet Explorer 11, режим IE
ms.openlocfilehash: b059cae3ff48a45fe92cbf69e37ad692e329b200
ms.sourcegitcommit: 6b577cb118f34f3ff2c65eab2908b65f155dc151
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/09/2020
ms.locfileid: "11003975"
---
# Режим Internet Explorer и DevTools  

В этой статье описывается интеграция режима Internet Explorer \ (режим IE) с Microsoft Edge \ (Chromium \) DevTools.  

## Общие сведения о режиме IE  

Режим IE позволяет компаниям указывать список веб-сайтов, которые работают только в Internet Explorer 11.  При переходе на такие веб-сайты в Microsoft Edge \ (Chromium \) экземпляр браузера Internet Explorer 11 запускается и отображает сайт на вкладке.  Эта функция позволяет предприятиям управлять совместимостью с технологиями, которые в настоящее время не совместимы с современными веб-браузерами.  Поддержка следующих технологий включена в режим IE.  

*   Режимы работы с документами в IE  
*   элементы ActiveX;  
*   другие устаревшие компоненты  

В режиме IE процесс отрисовки основан на Internet Explorer 11.  Диспетчер обработки Microsoft Edge \ (Chromium \) обрабатывает жизненный цикл процесса отрисовки.  Оно ограничено временем существования вкладки для определенного сайта \ (или приложения \).  При отображении вкладки в режиме IE в адресной строке на вкладке появляется индикатор.  

:::image type="complex" source="./media/ie-mode-badge.msft.png" alt-text="Значок режима IE в адресной строке" lightbox="./media/ie-mode-badge.msft.png":::
   Значок режима IE в адресной строке  
:::image-end:::  

В настоящее время режим Internet Explorer доступен в Windows 10 версии 1903 \ (обновление Май 2019), но скоро задействуется на все поддерживаемые платформы Windows.  

## Запуск DevTools на вкладке в режиме IE  

Если вы пытаетесь просмотреть режим документов на веб-сайте в режиме IE, выберите индикатор в адресной строке.  

:::image type="complex" source="./media/ie-mode-badge-doc-mode.msft.png" alt-text="Значок режима IE в адресной строке" lightbox="./media/ie-mode-badge-doc-mode.msft.png":::
   Просмотр режима документов с помощью эмблемы в режиме IE  
:::image-end:::  

Если вкладка используется в режиме IE, DevTools не работает и выполняются следующие условия.

*   Если вы выберете `F12` или выберете `Ctrl` + `Shift` + `I` пустой экземпляр Microsoft Edge \ (Chromium \) DevTools, появится следующее сообщение.  
    
    ```text
    Developer Tools are not available in Internet Explorer mode.  To debug the page, open it in Internet Explorer 11.
    ```  
    
*   Если вы открыли контекстное меню \ (щелкните правой кнопкой мыши \) и выберите команду **Просмотреть источник**, запускается блокнот.  
*   Если открыть контекстное меню \ (щелкните правой кнопкой мыши \), элемент " **проверить** " не будет виден.  

Причина, по которой не работают некоторые инструменты в DevTools \ (например, **сеть** и **производительность** ), — средство визуализации переключается с Chromium на Internet Explorer 11 в режиме IE.  Чтобы отправить отзыв, перейдите к [разделу знакомство с командой Microsoft Edge DevTools](#getting-in-touch-with-the-microsoft-edge-devtools-team).  

:::image type="complex" source="./media/ie-mode-devtools.msft.png" alt-text="Значок режима IE в адресной строке" lightbox="./media/ie-mode-devtools.msft.png":::
   DevTools запущен в режиме IE  
:::image-end:::  

Чтобы протестировать веб-сайт на базе Internet Explorer 11 (или приложение \) в Internet Explorer 11 и IE, выполните указанные ниже действия.  

1.  Откройте Internet Explorer 11.  
    *   В Windows 10 найдите ярлык для Internet Explorer 11.
        1.  Меню "Пуск" **Start Menu**  >  **Аксессуары**  >  для Windows **Internet Explorer 11**.  
    *   В Windows 7 найдите Internet Explorer 11.
        1.  Меню "Пуск" **Start Menu**  >  **Internet Explorer 11**.  
1.  В Internet Explorer 11 откройте ту же веб-страницу.  
1.  Запустите Internet Explorer DevTools.  
    *   Выберите `F12` .  
    *   Наведите указатель мыши на любое место, откройте контекстное меню, а затем нажмите кнопку **проверить элемент**.  Дополнительные сведения об использовании этих средств можно найти в разделе [использование средств разработчика F12][PreviousVersionsWindowsInternetExplorerDeveloperSamplesbg182326].  

## Удаленная отладка и режим IE  

Запустите Microsoft Edge \ (Chromium \) с включенной удаленной отладкой с помощью интерфейса командной строки.  Visual Studio, Visual Studio и другие средства разработки обычно выполняют команду для запуска Microsoft Edge.  Следующая команда запускает Microsoft Edge с установленным портом удаленной отладки `9222` .  

```shell
start msedge --remote-debugging-port=9222
```  

После запуска Microsoft Edge \ (Chromium \) с помощью аргумента командной строки режим IE будет недоступен.  Вы по-прежнему можете переходить к веб-сайтам, которые в противном случае отображались бы в режиме IE. Контент веб-сайта \ (или приложения \) будет обрабатываться с помощью Chromium, а не Internet Explorer 11.  Ожидается, что части страниц, зависящие от IE11, такие как элементы ActiveX, не отображаются должным образом.  Значок "режим IE" не отображается в адресной строке.  

Режим IE останется недоступным, пока вы не закроете и не перезапустите Microsoft Edge \ (Chromium \).  

## Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](./includes/contact-devtools-team-note.md)]  

<!-- links -->  

[PreviousVersionsWindowsInternetExplorerDeveloperSamplesbg182326]: /previous-versions/windows/internet-explorer/ie-developer/samples/bg182326(v%3dvs.85) "Использование средств разработчика F12 | Документы Microsoft"  