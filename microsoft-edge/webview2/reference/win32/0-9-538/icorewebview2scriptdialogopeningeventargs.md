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
ms.openlocfilehash: 94a008af5a66109add56cec7fd0969d4e20d8ca8
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699280"
---
# <span data-ttu-id="3cdc8-104">интерфейс ICoreWebView2ScriptDialogOpeningEventArgs</span><span class="sxs-lookup"><span data-stu-id="3cdc8-104">interface ICoreWebView2ScriptDialogOpeningEventArgs</span></span> 

```
interface ICoreWebView2ScriptDialogOpeningEventArgs
  : public IUnknown
```

<span data-ttu-id="3cdc8-105">Аргументы события для события ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="3cdc8-105">Event args for the ScriptDialogOpening event.</span></span>

## <span data-ttu-id="3cdc8-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="3cdc8-106">Summary</span></span>

 <span data-ttu-id="3cdc8-107">Участников</span><span class="sxs-lookup"><span data-stu-id="3cdc8-107">Members</span></span>                        | <span data-ttu-id="3cdc8-108">Описания</span><span class="sxs-lookup"><span data-stu-id="3cdc8-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3cdc8-109">Принять</span><span class="sxs-lookup"><span data-stu-id="3cdc8-109">Accept</span></span>](#accept) | <span data-ttu-id="3cdc8-110">Основное приложение может вызвать этот метод, чтобы ответить с помощью команды "ОК" для подтверждения, запроса и beforeunload диалоговых окон или вызова этого метода для указания отмены.</span><span class="sxs-lookup"><span data-stu-id="3cdc8-110">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>
[<span data-ttu-id="3cdc8-111">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="3cdc8-111">get_DefaultText</span></span>](#get_defaulttext) | <span data-ttu-id="3cdc8-112">Второй параметр, передаваемый диалоговому окну запроса JavaScript.</span><span class="sxs-lookup"><span data-stu-id="3cdc8-112">The second parameter passed to the JavaScript prompt dialog.</span></span>
[<span data-ttu-id="3cdc8-113">get_Kind</span><span class="sxs-lookup"><span data-stu-id="3cdc8-113">get_Kind</span></span>](#get_kind) | <span data-ttu-id="3cdc8-114">Диалоговое окно "вида JavaScript".</span><span class="sxs-lookup"><span data-stu-id="3cdc8-114">The kind of JavaScript dialog box.</span></span>
[<span data-ttu-id="3cdc8-115">get_Message</span><span class="sxs-lookup"><span data-stu-id="3cdc8-115">get_Message</span></span>](#get_message) | <span data-ttu-id="3cdc8-116">Сообщение в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="3cdc8-116">The message of the dialog box.</span></span>
[<span data-ttu-id="3cdc8-117">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="3cdc8-117">get_ResultText</span></span>](#get_resulttext) | <span data-ttu-id="3cdc8-118">Возвращаемое значение функции Prompt для JavaScript при вызове метода "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="3cdc8-118">The return value from the JavaScript prompt function if Accept is called.</span></span>
[<span data-ttu-id="3cdc8-119">get_Uri</span><span class="sxs-lookup"><span data-stu-id="3cdc8-119">get_Uri</span></span>](#get_uri) | <span data-ttu-id="3cdc8-120">URI страницы, запросившего диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="3cdc8-120">The URI of the page that requested the dialog box.</span></span>
[<span data-ttu-id="3cdc8-121">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="3cdc8-121">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="3cdc8-122">Для возврата объекта [ICoreWebView2Deferral](icorewebview2deferral.md) можно вызвать методического РБП.</span><span class="sxs-lookup"><span data-stu-id="3cdc8-122">GetDeferral can be called to return an [ICoreWebView2Deferral](icorewebview2deferral.md) object.</span></span>
[<span data-ttu-id="3cdc8-123">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="3cdc8-123">put_ResultText</span></span>](#put_resulttext) | <span data-ttu-id="3cdc8-124">Задайте свойство ResultText.</span><span class="sxs-lookup"><span data-stu-id="3cdc8-124">Set the ResultText property.</span></span>

## <span data-ttu-id="3cdc8-125">Участников</span><span class="sxs-lookup"><span data-stu-id="3cdc8-125">Members</span></span>

#### <span data-ttu-id="3cdc8-126">Принять</span><span class="sxs-lookup"><span data-stu-id="3cdc8-126">Accept</span></span> 

<span data-ttu-id="3cdc8-127">Основное приложение может вызвать этот метод, чтобы ответить с помощью команды "ОК" для подтверждения, запроса и beforeunload диалоговых окон или вызова этого метода для указания отмены.</span><span class="sxs-lookup"><span data-stu-id="3cdc8-127">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>

> <span data-ttu-id="3cdc8-128">общедоступное значение HRESULT [принято](#accept)()</span><span class="sxs-lookup"><span data-stu-id="3cdc8-128">public HRESULT [Accept](#accept)()</span></span>

<span data-ttu-id="3cdc8-129">Из JavaScript это означает, что функция Confirm и beforeunload возвращает значение истина, если вызывается метод принятии.</span><span class="sxs-lookup"><span data-stu-id="3cdc8-129">From JavaScript, this means that the confirm and beforeunload function returns true if Accept is called.</span></span> <span data-ttu-id="3cdc8-130">И для функции Prompt она возвращает значение ResultText, если вызывается метод допуска, и возвращает значение false в противном случае.</span><span class="sxs-lookup"><span data-stu-id="3cdc8-130">And for the prompt function it returns the value of ResultText if Accept is called and returns false otherwise.</span></span>

#### <span data-ttu-id="3cdc8-131">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="3cdc8-131">get_DefaultText</span></span> 

<span data-ttu-id="3cdc8-132">Второй параметр, передаваемый диалоговому окну запроса JavaScript.</span><span class="sxs-lookup"><span data-stu-id="3cdc8-132">The second parameter passed to the JavaScript prompt dialog.</span></span>

> <span data-ttu-id="3cdc8-133">общедоступные значения HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR \* DefaultText)</span><span class="sxs-lookup"><span data-stu-id="3cdc8-133">public HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR \* defaultText)</span></span>

<span data-ttu-id="3cdc8-134">Это значение по умолчанию, используемое в качестве результата функции JavaScript "prompt".</span><span class="sxs-lookup"><span data-stu-id="3cdc8-134">This is the default value to use for the result of the prompt JavaScript function.</span></span>

#### <span data-ttu-id="3cdc8-135">get_Kind</span><span class="sxs-lookup"><span data-stu-id="3cdc8-135">get_Kind</span></span> 

<span data-ttu-id="3cdc8-136">Диалоговое окно "вида JavaScript".</span><span class="sxs-lookup"><span data-stu-id="3cdc8-136">The kind of JavaScript dialog box.</span></span>

> <span data-ttu-id="3cdc8-137">общедоступные значения HRESULT [get_Kind](#get_kind)(COREWEBVIEW2_SCRIPT_DIALOG_KIND \* видам)</span><span class="sxs-lookup"><span data-stu-id="3cdc8-137">public HRESULT [get_Kind](#get_kind)(COREWEBVIEW2_SCRIPT_DIALOG_KIND \* kind)</span></span>

<span data-ttu-id="3cdc8-138">Приняв, подтвердите, запросите или beforeunload.</span><span class="sxs-lookup"><span data-stu-id="3cdc8-138">Accept, confirm, prompt, or beforeunload.</span></span>

#### <span data-ttu-id="3cdc8-139">get_Message</span><span class="sxs-lookup"><span data-stu-id="3cdc8-139">get_Message</span></span> 

<span data-ttu-id="3cdc8-140">Сообщение в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="3cdc8-140">The message of the dialog box.</span></span>

> <span data-ttu-id="3cdc8-141">общедоступное значение HRESULT [get_Message](#get_message)(LPWSTR \* сообщение)</span><span class="sxs-lookup"><span data-stu-id="3cdc8-141">public HRESULT [get_Message](#get_message)(LPWSTR \* message)</span></span>

<span data-ttu-id="3cdc8-142">Из JavaScript это первый параметр, передаваемый в Alert, Confirm и Prompt, и он пуст для beforeunload.</span><span class="sxs-lookup"><span data-stu-id="3cdc8-142">From JavaScript this is the first parameter passed to alert, confirm, and prompt and is empty for beforeunload.</span></span>

#### <span data-ttu-id="3cdc8-143">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="3cdc8-143">get_ResultText</span></span> 

<span data-ttu-id="3cdc8-144">Возвращаемое значение функции Prompt для JavaScript при вызове метода "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="3cdc8-144">The return value from the JavaScript prompt function if Accept is called.</span></span>

> <span data-ttu-id="3cdc8-145">общедоступные значения HRESULT [get_ResultText](#get_resulttext)(LPWSTR \* ResultText)</span><span class="sxs-lookup"><span data-stu-id="3cdc8-145">public HRESULT [get_ResultText](#get_resulttext)(LPWSTR \* resultText)</span></span>

<span data-ttu-id="3cdc8-146">Этот тип игнорируется, если диалоговое окно не является запросом.</span><span class="sxs-lookup"><span data-stu-id="3cdc8-146">This is ignored for dialog kinds other than prompt.</span></span> <span data-ttu-id="3cdc8-147">Если параметр "принято" не вызывается, это значение игнорируется, и в командной строке возвращается значение "ложь".</span><span class="sxs-lookup"><span data-stu-id="3cdc8-147">If Accept is not called this value is ignored and false is returned from prompt.</span></span>

#### <span data-ttu-id="3cdc8-148">get_Uri</span><span class="sxs-lookup"><span data-stu-id="3cdc8-148">get_Uri</span></span> 

<span data-ttu-id="3cdc8-149">URI страницы, запросившего диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="3cdc8-149">The URI of the page that requested the dialog box.</span></span>

> <span data-ttu-id="3cdc8-150">общедоступные значения HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="3cdc8-150">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="3cdc8-151">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="3cdc8-151">GetDeferral</span></span> 

<span data-ttu-id="3cdc8-152">Для возврата объекта [ICoreWebView2Deferral](icorewebview2deferral.md) можно вызвать методического РБП.</span><span class="sxs-lookup"><span data-stu-id="3cdc8-152">GetDeferral can be called to return an [ICoreWebView2Deferral](icorewebview2deferral.md) object.</span></span>

> <span data-ttu-id="3cdc8-153">общедоступный HRESULT- [РБП](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* РБП)</span><span class="sxs-lookup"><span data-stu-id="3cdc8-153">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="3cdc8-154">Вы можете использовать этот параметр, чтобы выполнить событие позже.</span><span class="sxs-lookup"><span data-stu-id="3cdc8-154">You can use this to complete the event at a later time.</span></span>

#### <span data-ttu-id="3cdc8-155">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="3cdc8-155">put_ResultText</span></span> 

<span data-ttu-id="3cdc8-156">Задайте свойство ResultText.</span><span class="sxs-lookup"><span data-stu-id="3cdc8-156">Set the ResultText property.</span></span>

> <span data-ttu-id="3cdc8-157">общедоступные значения HRESULT [put_ResultText](#put_resulttext)(LPCWSTR ResultText)</span><span class="sxs-lookup"><span data-stu-id="3cdc8-157">public HRESULT [put_ResultText](#put_resulttext)(LPCWSTR resultText)</span></span>
