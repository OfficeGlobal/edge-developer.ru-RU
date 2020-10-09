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
# <span data-ttu-id="afd63-103">Протокол DevTools версии 0,1 заметки о выпуске</span><span class="sxs-lookup"><span data-stu-id="afd63-103">DevTools Protocol Version 0.1 Release Notes</span></span>

> [!NOTE]
> <span data-ttu-id="afd63-104">Протокол Microsoft Edge DevTools работает только на [Windows 10 2018 апрельского обновления](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) и более поздних сборок для предварительной [оценки Windows](https://insider.windows.com/en-us/getting-started/) .</span><span class="sxs-lookup"><span data-stu-id="afd63-104">The Microsoft Edge DevTools Protocol works only on [Windows 10 April 2018 Update](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) and later [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) builds.</span></span>

<span data-ttu-id="afd63-105">Версия 0,1 **протокола Microsoft Edge DevTools** обеспечивает более раннее предварительный просмотр для проверки оснащения EdgeHTML и базовой удаленной отладки в новом отдельном приложении [Microsoft Edge DevTools Preview](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) .</span><span class="sxs-lookup"><span data-stu-id="afd63-105">Version 0.1 of the Microsoft **Edge DevTools Protocol** provides an early preview for testing EdgeHTML instrumentation and basic remote debugging in the new standalone [Microsoft Edge DevTools Preview](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) app.</span></span> <span data-ttu-id="afd63-106">Для этого требуется, чтобы на компьютере под управлением [Windows 10 эйприл 2018](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) или более поздней сборки [предварительной оценки Windows](https://insider.windows.com/en-us/getting-started/) .</span><span class="sxs-lookup"><span data-stu-id="afd63-106">As such, it requires you to be running [Windows 10 April 2018 Update](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) or a later [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) build.</span></span>

<span data-ttu-id="afd63-107">Цели протокола DevTools — это три части:</span><span class="sxs-lookup"><span data-stu-id="afd63-107">The goals behind the DevTools Protocol are three-fold:</span></span>

 - <span data-ttu-id="afd63-108">Предоставьте общедоступный API для нашего приложения DevTools, чтобы присоединиться к Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="afd63-108">Provide a public API for our DevTools app to attach to Microsoft Edge</span></span>
 - <span data-ttu-id="afd63-109">Расширение доступа к функциональным возможностям DevTools с помощью внешних клиентов</span><span class="sxs-lookup"><span data-stu-id="afd63-109">Expand access of DevTools functionality to external tooling clients</span></span>
 - <span data-ttu-id="afd63-110">Разрешите удаленную отладку в диапазоне устройств с Windows 10, работающих под управлением Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="afd63-110">Enable remote debugging across the range of Windows 10 devices running Microsoft Edge</span></span> 

<span data-ttu-id="afd63-111">В этом предварительном выпуске доступны основные функциональные возможности отладки, такие как установка точек останова, пошаговое выполнение кода и изучение трассировок стека.</span><span class="sxs-lookup"><span data-stu-id="afd63-111">This preliminary release provides core debugging functionality, such as setting breakpoints, stepping through code, and exploring stack traces.</span></span> <span data-ttu-id="afd63-112">В пользовательском интерфейсе DevTools это преобразуется в функциональные возможности, доступные на панели [**отладчика**](../../devtools-guide/debugger.md) , за вычетом проверки кэша (для веб-хранилища, рабочего процесса службы, кэша API и IndexedDB).</span><span class="sxs-lookup"><span data-stu-id="afd63-112">In the Edge DevTools UI, this translates to functionality available in the [**Debugger**](../../devtools-guide/debugger.md) panel, minus cache inspection (for Web storage, Service worker, Cache API, and IndexedDB).</span></span> 

<span data-ttu-id="afd63-113">Дополнительные функции отладчика будут добавлены в предстоящие выпуски, а также с помощью инструментария, в котором другие панели [DevTools](../../devtools-guide.md) .</span><span class="sxs-lookup"><span data-stu-id="afd63-113">Further debugger functionality will be added in upcoming releases, followed by the instrumentation powering other [DevTools](../../devtools-guide.md) panels.</span></span>
