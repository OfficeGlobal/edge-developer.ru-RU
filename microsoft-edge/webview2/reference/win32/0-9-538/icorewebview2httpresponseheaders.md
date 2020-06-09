---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 508ecacc867330c73132ae7e446b7483ea002f83
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699256"
---
# <span data-ttu-id="661e2-104">интерфейс ICoreWebView2HttpResponseHeaders</span><span class="sxs-lookup"><span data-stu-id="661e2-104">interface ICoreWebView2HttpResponseHeaders</span></span> 

```
interface ICoreWebView2HttpResponseHeaders
  : public IUnknown
```

<span data-ttu-id="661e2-105">Заголовки ответа HTTP.</span><span class="sxs-lookup"><span data-stu-id="661e2-105">HTTP response headers.</span></span>

## <span data-ttu-id="661e2-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="661e2-106">Summary</span></span>

 <span data-ttu-id="661e2-107">Участников</span><span class="sxs-lookup"><span data-stu-id="661e2-107">Members</span></span>                        | <span data-ttu-id="661e2-108">Описания</span><span class="sxs-lookup"><span data-stu-id="661e2-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="661e2-109">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="661e2-109">AppendHeader</span></span>](#appendheader) | <span data-ttu-id="661e2-110">Добавляет строку заголовка с именем и значением.</span><span class="sxs-lookup"><span data-stu-id="661e2-110">Appends header line with name and value.</span></span>
[<span data-ttu-id="661e2-111">Contains</span><span class="sxs-lookup"><span data-stu-id="661e2-111">Contains</span></span>](#contains) | <span data-ttu-id="661e2-112">Проверяет, содержат ли заголовки записи, соответствующие имени заголовка.</span><span class="sxs-lookup"><span data-stu-id="661e2-112">Checks whether the headers contain entries matching the header name.</span></span>
[<span data-ttu-id="661e2-113">"Голова"</span><span class="sxs-lookup"><span data-stu-id="661e2-113">GetHeader</span></span>](#getheader) | <span data-ttu-id="661e2-114">Возвращает значение первого заголовка в коллекции, соответствующее имени.</span><span class="sxs-lookup"><span data-stu-id="661e2-114">Gets the first header value in the collection matching the name.</span></span>
[<span data-ttu-id="661e2-115">"Голова"</span><span class="sxs-lookup"><span data-stu-id="661e2-115">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="661e2-116">Возвращает значения заголовков, соответствующие имени.</span><span class="sxs-lookup"><span data-stu-id="661e2-116">Gets the header values matching the name.</span></span>
[<span data-ttu-id="661e2-117">Реверсивный итератор</span><span class="sxs-lookup"><span data-stu-id="661e2-117">GetIterator</span></span>](#getiterator) | <span data-ttu-id="661e2-118">Получает итератор на коллекцию всех заголовков ответа.</span><span class="sxs-lookup"><span data-stu-id="661e2-118">Gets an iterator over the collection of entire response headers.</span></span>

<span data-ttu-id="661e2-119">Используется для создания WebResourceResponse для события WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="661e2-119">Used to construct a WebResourceResponse for the WebResourceRequested event.</span></span>

## <span data-ttu-id="661e2-120">Участников</span><span class="sxs-lookup"><span data-stu-id="661e2-120">Members</span></span>

#### <span data-ttu-id="661e2-121">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="661e2-121">AppendHeader</span></span> 

<span data-ttu-id="661e2-122">Добавляет строку заголовка с именем и значением.</span><span class="sxs-lookup"><span data-stu-id="661e2-122">Appends header line with name and value.</span></span>

> <span data-ttu-id="661e2-123">общедоступные значения HRESULT [AppendHeader](#appendheader)(имя LPCWSTR, значение LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="661e2-123">public HRESULT [AppendHeader](#appendheader)(LPCWSTR name, LPCWSTR value)</span></span>

#### <span data-ttu-id="661e2-124">Contains</span><span class="sxs-lookup"><span data-stu-id="661e2-124">Contains</span></span> 

<span data-ttu-id="661e2-125">Проверяет, содержат ли заголовки записи, соответствующие имени заголовка.</span><span class="sxs-lookup"><span data-stu-id="661e2-125">Checks whether the headers contain entries matching the header name.</span></span>

> <span data-ttu-id="661e2-126">общедоступное значение HRESULT [Contains](#contains)(имя LPCWSTR, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="661e2-126">public HRESULT [Contains](#contains)(LPCWSTR name, BOOL \* contains)</span></span>

#### <span data-ttu-id="661e2-127">"Голова"</span><span class="sxs-lookup"><span data-stu-id="661e2-127">GetHeader</span></span> 

<span data-ttu-id="661e2-128">Возвращает значение первого заголовка в коллекции, соответствующее имени.</span><span class="sxs-lookup"><span data-stu-id="661e2-128">Gets the first header value in the collection matching the name.</span></span>

> <span data-ttu-id="661e2-129">общедоступный [заголовок](#getheader)HRESULT (имя LPCWSTR, LPWSTR \* Value)</span><span class="sxs-lookup"><span data-stu-id="661e2-129">public HRESULT [GetHeader](#getheader)(LPCWSTR name, LPWSTR \* value)</span></span>

#### <span data-ttu-id="661e2-130">"Голова"</span><span class="sxs-lookup"><span data-stu-id="661e2-130">GetHeaders</span></span> 

<span data-ttu-id="661e2-131">Возвращает значения заголовков, соответствующие имени.</span><span class="sxs-lookup"><span data-stu-id="661e2-131">Gets the header values matching the name.</span></span>

> <span data-ttu-id="661e2-132">общедоступные [Выголовки](#getheaders)HRESULT (имя LPCWSTR, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \* итератор)</span><span class="sxs-lookup"><span data-stu-id="661e2-132">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="661e2-133">Реверсивный итератор</span><span class="sxs-lookup"><span data-stu-id="661e2-133">GetIterator</span></span> 

<span data-ttu-id="661e2-134">Получает итератор на коллекцию всех заголовков ответа.</span><span class="sxs-lookup"><span data-stu-id="661e2-134">Gets an iterator over the collection of entire response headers.</span></span>

> <span data-ttu-id="661e2-135">общедоступный HRESULT- [итератор](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \*)</span><span class="sxs-lookup"><span data-stu-id="661e2-135">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>
