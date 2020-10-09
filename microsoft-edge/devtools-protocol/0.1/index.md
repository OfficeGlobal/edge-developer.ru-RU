---
description: Заметки о выпуске Microsoft Edge DevTools Protocol версии 0,1
title: Протокол DevTools версии 0,1 заметки о выпуске
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: 3c0648467c20572a525fe257788068966efd193c
ms.sourcegitcommit: 845a0d53a86bee3678f421adee26b3372cefce57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/08/2020
ms.locfileid: "11104737"
---
# Протокол DevTools версии 0,1 заметки о выпуске

> [!NOTE]
> Протокол Microsoft Edge DevTools работает только на [Windows 10 2018 апрельского обновления](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) и более поздних сборок для предварительной [оценки Windows](https://insider.windows.com/en-us/getting-started/) .

Версия 0,1 **протокола Microsoft Edge DevTools** обеспечивает более раннее предварительный просмотр для проверки оснащения EdgeHTML и базовой удаленной отладки в новом отдельном приложении [Microsoft Edge DevTools Preview](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) . Для этого требуется, чтобы на компьютере под управлением [Windows 10 эйприл 2018](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) или более поздней сборки [предварительной оценки Windows](https://insider.windows.com/en-us/getting-started/) .

Цели протокола DevTools — это три части:

 - Предоставьте общедоступный API для нашего приложения DevTools, чтобы присоединиться к Microsoft Edge
 - Расширение доступа к функциональным возможностям DevTools с помощью внешних клиентов
 - Разрешите удаленную отладку в диапазоне устройств с Windows 10, работающих под управлением Microsoft Edge. 

В этом предварительном выпуске доступны основные функциональные возможности отладки, такие как установка точек останова, пошаговое выполнение кода и изучение трассировок стека. В пользовательском интерфейсе DevTools это преобразуется в функциональные возможности, доступные на панели [**отладчика**](../../devtools-guide/debugger.md) , за вычетом проверки кэша (для веб-хранилища, рабочего процесса службы, кэша API и IndexedDB). 

Дополнительные функции отладчика будут добавлены в предстоящие выпуски, а также с помощью инструментария, в котором другие панели [DevTools](../../devtools-guide.md) .
