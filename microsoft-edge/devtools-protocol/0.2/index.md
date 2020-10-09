---
description: Заметки о выпуске Microsoft Edge DevTools Protocol версии 0,2
title: Заметки о выпуске протокола Microsoft Edge DevTools версии 0,2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: c4959d2905f95c2bcf98cb78ad67bb88ecfec959
ms.sourcegitcommit: 845a0d53a86bee3678f421adee26b3372cefce57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/08/2020
ms.locfileid: "11104744"
---
# Протокол DevTools версии 0,2 заметки о выпуске

> [!NOTE]
> Версия 0,2 протокола Microsoft Edge DevTools работает только на [обновлениях для Windows 10 октября 2018](/windows/uwp/whats-new/windows-10-build-17763) и более поздних сборок для [предварительной оценки Windows](https://insider.windows.com/getting-started/) .

Версия 0,2 **протокола Microsoft Edge DevTools** обеспечивает предварительный просмотр для проверки инструментальных средств EdgeHTML и Basic Remote Debugging в новом отдельном приложении [Microsoft Edge DevTools Preview](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) . Для этого требуется, чтобы на компьютере была установлена версия [Windows 10 октябрь 2018](/windows/uwp/whats-new/windows-10-build-17763) или более поздняя сборка предварительной [оценки для Windows](https://insider.windows.com/getting-started/) .

Цели протокола DevTools — это три части:

 - Предоставьте общедоступный API для нашего приложения DevTools, чтобы присоединиться к Microsoft Edge
 - Расширение доступа к функциональным возможностям DevTools с помощью внешних клиентов
 - Разрешите удаленную отладку в диапазоне устройств с Windows 10, работающих под управлением Microsoft Edge. 

Версия 0,2 протокола DevTools включает новые домены для стиля и макета (только для чтения) и API консоли в дополнение к основным функциям отладки сценария, представленным в версии 0,1. В пользовательском интерфейсе DevTools это преобразуется в функциональные возможности, доступные на панелях [**элементы**](../../devtools-guide/elements.md), [**консоль**](../../devtools-guide/console.md) и [**отладчик**](../../devtools-guide/debugger.md)  .
