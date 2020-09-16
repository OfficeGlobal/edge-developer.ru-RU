---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2FocusChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2FocusChangedEventHandler
ms.openlocfilehash: f94e6f8323862d092bf9157061333f5e801db891
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012499"
---
# <span data-ttu-id="4262d-104">интерфейс ICoreWebView2FocusChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="4262d-104">interface ICoreWebView2FocusChangedEventHandler</span></span> 

```
interface ICoreWebView2FocusChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="4262d-105">Вызывающий объект реализует этот метод для получения событий GotFocus и LostFocus.</span><span class="sxs-lookup"><span data-stu-id="4262d-105">The caller implements this method to receive the GotFocus and LostFocus events.</span></span>

## <span data-ttu-id="4262d-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="4262d-106">Summary</span></span>

 <span data-ttu-id="4262d-107">Участников</span><span class="sxs-lookup"><span data-stu-id="4262d-107">Members</span></span>                        | <span data-ttu-id="4262d-108">Описания</span><span class="sxs-lookup"><span data-stu-id="4262d-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="4262d-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="4262d-109">Invoke</span></span>](#invoke) | <span data-ttu-id="4262d-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="4262d-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="4262d-111">Аргументы события для этого события отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="4262d-111">There are no event args for this event.</span></span>

## <span data-ttu-id="4262d-112">Участников</span><span class="sxs-lookup"><span data-stu-id="4262d-112">Members</span></span>

#### <span data-ttu-id="4262d-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="4262d-113">Invoke</span></span> 

<span data-ttu-id="4262d-114">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="4262d-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="4262d-115">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2Controller](icorewebview2controller.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="4262d-115">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="4262d-116">Аргументы события отсутствуют, а параметр args — null.</span><span class="sxs-lookup"><span data-stu-id="4262d-116">There are no event args and the args parameter will be null.</span></span>
