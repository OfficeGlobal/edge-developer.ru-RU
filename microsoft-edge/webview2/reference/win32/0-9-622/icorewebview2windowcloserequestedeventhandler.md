---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2WindowCloseRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2WindowCloseRequestedEventHandler
ms.openlocfilehash: f5c1799225df5460029b3ad0c40db63a2e16113c
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012393"
---
# <span data-ttu-id="ec78b-104">интерфейс ICoreWebView2WindowCloseRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="ec78b-104">interface ICoreWebView2WindowCloseRequestedEventHandler</span></span> 

```
interface ICoreWebView2WindowCloseRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="ec78b-105">Вызывающий объект реализует этот интерфейс, чтобы получать события NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="ec78b-105">The caller implements this interface to receive NewWindowRequested events.</span></span>

## <span data-ttu-id="ec78b-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="ec78b-106">Summary</span></span>

 <span data-ttu-id="ec78b-107">Участников</span><span class="sxs-lookup"><span data-stu-id="ec78b-107">Members</span></span>                        | <span data-ttu-id="ec78b-108">Описания</span><span class="sxs-lookup"><span data-stu-id="ec78b-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ec78b-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="ec78b-109">Invoke</span></span>](#invoke) | <span data-ttu-id="ec78b-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="ec78b-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="ec78b-111">Участников</span><span class="sxs-lookup"><span data-stu-id="ec78b-111">Members</span></span>

#### <span data-ttu-id="ec78b-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="ec78b-112">Invoke</span></span> 

<span data-ttu-id="ec78b-113">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="ec78b-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="ec78b-114">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="ec78b-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="ec78b-115">Аргументы события отсутствуют, а параметр args — null.</span><span class="sxs-lookup"><span data-stu-id="ec78b-115">There are no event args and the args parameter will be null.</span></span>
