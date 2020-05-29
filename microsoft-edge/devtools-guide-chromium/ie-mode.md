---
description: Режим IE и Microsoft EDGE (Chromium) DevTools
title: Режим Internet Explorer и DevTools
author: robpaveza
ms.author: ropaveza
ms.date: 01/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools, ie11, Internet Explorer 11, режим IE
ms.openlocfilehash: 18e5f029d277e446857ec48b9cf129149f219256
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572430"
---
# Режим Internet Explorer и DevTools

В этом документе описывается интеграция режима Internet Explorer (режим IE) с Microsoft EDGE (Chromium) DevTools.

## Общие сведения о режиме IE

Режим IE — это механизм, с помощью которого компании могут определять набор веб-сайтов, которые, до этого момента, будут работать только в Internet Explorer 11. Когда эти веб-сайты просматриваются в Microsoft EDGE (Chromium), на вкладке выполняется полный экземпляр браузера Internet Explorer 11 и отображаются на нем. Это позволяет предприятиям управлять совместимостью в режимах документов IE, элементов ActiveX и других устаревших компонентах, которые в настоящее время не совместимы с любыми современными веб-браузерами.

В режиме IE процесс рендеринга полностью основан на Internet Explorer 11. Процесс диспетчера Microsoft EDGE (Chromium) управляет жизненным циклом процесса отрисовки, но ограничивается временем существования вкладки на данном сайте или приложении. При отображении вкладки в режиме IE в адресной строке для указанной вкладки появляется индикатор.

![Значок режима IE в адресной строке](./media/ie-mode-badge.png)

В настоящее время режим Internet Explorer доступен в Windows 10 версии 1903 (обновление может 2019), но вскоре на все поддерживаемые платформы Windows.

## Запуск DevTools на вкладке в режиме IE

Если вы пытаетесь просмотреть режим документов на веб-сайте в режиме IE, вы можете щелкнуть значок в адресной строке.

![Просмотр режима документов с помощью эмблемы в режиме IE](./media/ie-mode-badge-doc-mode.png)

На вкладке в режиме IE DevTools работать не будет. `F12` `Ctrl` + `Shift` + `I` Вы можете запустить пустой экземпляр Microsoft EDGE (Chromium) только в том случае, если у вас есть сообщение, которое Прочитано: "средства разработчика недоступны в режиме Internet Explorer. Чтобы выполнить отладку страницы, откройте ее в Internet Explorer 11. " **Представление "источник** " запускает приложение "Блокнот", а **элемент проверки** не будет отображаться в контекстном меню в режиме Internet Explorer.

Это связано с тем, что при переходе с Chromium на Internet Explorer 11 в режиме IE некоторые компоненты в DevTools (например, сети и средства для работы с производительностью) будут разорваны. Чтобы отправить нам отзыв, щелкните `:)` значок.

![DevTools запущен в режиме IE](./media/ie-mode-devtools.png)

Если вы разрабатываете или сохраняете веб-сайт или приложение на базе Internet Explorer 11, рекомендуем перейти на одну и ту же страницу в Internet Explorer 11. В Windows 10 вы можете найти ярлык для Internet Explorer 11 в меню "Пуск" в разделе "Аксессуары" для Windows. В Windows 7 вы можете найти Internet Explorer 11 в главном меню "Пуск". Затем вы можете запустить Internet Explorer DevTools, нажав `F12` или нажав кнопку **проверить элемент** в контекстном меню. Чтобы узнать больше о том, как использовать эти инструменты, щелкните [здесь](/previous-versions/windows/internet-explorer/ie-developer/samples/bg182326(v%3dvs.85)).

## Удаленная отладка и режим IE

Вы можете запустить Microsoft EDGE (Chromium) с включенной удаленной отладкой, которая обычно описывает такие инструменты, как Visual Studio или VS Code EDGE, из командной строки.

`start msedge --remote-debugging-port=9222`

При запуске Microsoft EDGE (Chromium) с помощью этого аргумента командной строки режим IE будет недоступен. Вы по-прежнему можете переходить к веб-сайтам или приложениям, которые в противном случае находятся в режиме IE, но содержимое будет отображено через Chromium, а не Internet Explorer 11. Вы можете ожидать, что части страниц, которые используют IE11, такие как элементы ActiveX, будут отображаться неправильно. Значок "режим IE" больше не будет отображаться в адресной строке.

Режим IE останется недоступным, пока не будет полностью закрыт Microsoft EDGE (Chromium).