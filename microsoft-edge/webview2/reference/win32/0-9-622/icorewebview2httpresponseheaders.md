---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2HttpResponseHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2HttpResponseHeaders
ms.openlocfilehash: 1622d2c19159bca76e036408810e2ca145d30e85
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012466"
---
# <span data-ttu-id="87ffe-104">интерфейс ICoreWebView2HttpResponseHeaders</span><span class="sxs-lookup"><span data-stu-id="87ffe-104">interface ICoreWebView2HttpResponseHeaders</span></span> 

```
interface ICoreWebView2HttpResponseHeaders
  : public IUnknown
```

<span data-ttu-id="87ffe-105">Заголовки ответа HTTP.</span><span class="sxs-lookup"><span data-stu-id="87ffe-105">HTTP response headers.</span></span>

## <span data-ttu-id="87ffe-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="87ffe-106">Summary</span></span>

 <span data-ttu-id="87ffe-107">Участников</span><span class="sxs-lookup"><span data-stu-id="87ffe-107">Members</span></span>                        | <span data-ttu-id="87ffe-108">Описания</span><span class="sxs-lookup"><span data-stu-id="87ffe-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="87ffe-109">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="87ffe-109">AppendHeader</span></span>](#appendheader) | <span data-ttu-id="87ffe-110">Добавляет строку заголовка с именем и значением.</span><span class="sxs-lookup"><span data-stu-id="87ffe-110">Appends header line with name and value.</span></span>
[<span data-ttu-id="87ffe-111">Contains</span><span class="sxs-lookup"><span data-stu-id="87ffe-111">Contains</span></span>](#contains) | <span data-ttu-id="87ffe-112">Проверяет, содержат ли заголовки записи, соответствующие имени заголовка.</span><span class="sxs-lookup"><span data-stu-id="87ffe-112">Checks whether the headers contain entries matching the header name.</span></span>
[<span data-ttu-id="87ffe-113">"Голова"</span><span class="sxs-lookup"><span data-stu-id="87ffe-113">GetHeader</span></span>](#getheader) | <span data-ttu-id="87ffe-114">Возвращает значение первого заголовка в коллекции, соответствующее имени.</span><span class="sxs-lookup"><span data-stu-id="87ffe-114">Gets the first header value in the collection matching the name.</span></span>
[<span data-ttu-id="87ffe-115">"Голова"</span><span class="sxs-lookup"><span data-stu-id="87ffe-115">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="87ffe-116">Возвращает значения заголовков, соответствующие имени.</span><span class="sxs-lookup"><span data-stu-id="87ffe-116">Gets the header values matching the name.</span></span>
[<span data-ttu-id="87ffe-117">Реверсивный итератор</span><span class="sxs-lookup"><span data-stu-id="87ffe-117">GetIterator</span></span>](#getiterator) | <span data-ttu-id="87ffe-118">Получает итератор на коллекцию всех заголовков ответа.</span><span class="sxs-lookup"><span data-stu-id="87ffe-118">Gets an iterator over the collection of entire response headers.</span></span>

<span data-ttu-id="87ffe-119">Используется для создания WebResourceResponse для события WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="87ffe-119">Used to construct a WebResourceResponse for the WebResourceRequested event.</span></span>

## <span data-ttu-id="87ffe-120">Участников</span><span class="sxs-lookup"><span data-stu-id="87ffe-120">Members</span></span>

#### <span data-ttu-id="87ffe-121">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="87ffe-121">AppendHeader</span></span> 

<span data-ttu-id="87ffe-122">Добавляет строку заголовка с именем и значением.</span><span class="sxs-lookup"><span data-stu-id="87ffe-122">Appends header line with name and value.</span></span>

> <span data-ttu-id="87ffe-123">общедоступные значения HRESULT [AppendHeader](#appendheader)(имя LPCWSTR, значение LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="87ffe-123">public HRESULT [AppendHeader](#appendheader)(LPCWSTR name, LPCWSTR value)</span></span>

#### <span data-ttu-id="87ffe-124">Contains</span><span class="sxs-lookup"><span data-stu-id="87ffe-124">Contains</span></span> 

<span data-ttu-id="87ffe-125">Проверяет, содержат ли заголовки записи, соответствующие имени заголовка.</span><span class="sxs-lookup"><span data-stu-id="87ffe-125">Checks whether the headers contain entries matching the header name.</span></span>

> <span data-ttu-id="87ffe-126">общедоступное значение HRESULT [Contains](#contains)(имя LPCWSTR, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="87ffe-126">public HRESULT [Contains](#contains)(LPCWSTR name, BOOL \* contains)</span></span>

#### <span data-ttu-id="87ffe-127">"Голова"</span><span class="sxs-lookup"><span data-stu-id="87ffe-127">GetHeader</span></span> 

<span data-ttu-id="87ffe-128">Возвращает значение первого заголовка в коллекции, соответствующее имени.</span><span class="sxs-lookup"><span data-stu-id="87ffe-128">Gets the first header value in the collection matching the name.</span></span>

> <span data-ttu-id="87ffe-129">общедоступный [заголовок](#getheader)HRESULT (имя LPCWSTR, LPWSTR \* Value)</span><span class="sxs-lookup"><span data-stu-id="87ffe-129">public HRESULT [GetHeader](#getheader)(LPCWSTR name, LPWSTR \* value)</span></span>

#### <span data-ttu-id="87ffe-130">"Голова"</span><span class="sxs-lookup"><span data-stu-id="87ffe-130">GetHeaders</span></span> 

<span data-ttu-id="87ffe-131">Возвращает значения заголовков, соответствующие имени.</span><span class="sxs-lookup"><span data-stu-id="87ffe-131">Gets the header values matching the name.</span></span>

> <span data-ttu-id="87ffe-132">общедоступные [Выголовки](#getheaders)HRESULT (имя LPCWSTR, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \* итератор)</span><span class="sxs-lookup"><span data-stu-id="87ffe-132">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="87ffe-133">Реверсивный итератор</span><span class="sxs-lookup"><span data-stu-id="87ffe-133">GetIterator</span></span> 

<span data-ttu-id="87ffe-134">Получает итератор на коллекцию всех заголовков ответа.</span><span class="sxs-lookup"><span data-stu-id="87ffe-134">Gets an iterator over the collection of entire response headers.</span></span>

> <span data-ttu-id="87ffe-135">общедоступный HRESULT- [итератор](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \*)</span><span class="sxs-lookup"><span data-stu-id="87ffe-135">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>
