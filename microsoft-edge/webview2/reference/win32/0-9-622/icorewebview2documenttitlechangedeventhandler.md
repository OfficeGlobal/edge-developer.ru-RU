---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2DocumentTitleChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2DocumentTitleChangedEventHandler
ms.openlocfilehash: 9332786935ba79adfd6ef215c9e11afa24c5ceb2
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012395"
---
# <span data-ttu-id="80493-104">интерфейс ICoreWebView2DocumentTitleChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="80493-104">interface ICoreWebView2DocumentTitleChangedEventHandler</span></span> 

```
interface ICoreWebView2DocumentTitleChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="80493-105">Вызывающий объект реализует этот интерфейс, чтобы получать события DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="80493-105">The caller implements this interface to receive DocumentTitleChanged events.</span></span>

## <span data-ttu-id="80493-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="80493-106">Summary</span></span>

 <span data-ttu-id="80493-107">Участников</span><span class="sxs-lookup"><span data-stu-id="80493-107">Members</span></span>                        | <span data-ttu-id="80493-108">Описания</span><span class="sxs-lookup"><span data-stu-id="80493-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="80493-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="80493-109">Invoke</span></span>](#invoke) | <span data-ttu-id="80493-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="80493-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="80493-111">Используйте свойство DocumentTitle, чтобы получить измененный заголовок.</span><span class="sxs-lookup"><span data-stu-id="80493-111">Use the DocumentTitle property to get the modified title.</span></span>

## <span data-ttu-id="80493-112">Участников</span><span class="sxs-lookup"><span data-stu-id="80493-112">Members</span></span>

#### <span data-ttu-id="80493-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="80493-113">Invoke</span></span> 

<span data-ttu-id="80493-114">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="80493-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="80493-115">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="80493-115">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="80493-116">Аргументы события отсутствуют, а параметр args — null.</span><span class="sxs-lookup"><span data-stu-id="80493-116">There are no event args and the args parameter will be null.</span></span>
