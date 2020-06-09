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
ms.openlocfilehash: 1e316c0315a8852574ea8b44cc98b11126155492
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699147"
---
# <span data-ttu-id="24333-104">Класс Microsoft. Web. WebView2. Core. CoreWebView2Controller</span><span class="sxs-lookup"><span data-stu-id="24333-104">Microsoft.Web.WebView2.Core.CoreWebView2Controller class</span></span> 

<span data-ttu-id="24333-105">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="24333-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="24333-106">Сборка: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="24333-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="24333-107">Этот класс является владельцем объекта CoreWebView2 и предоставляет поддержку для изменения размеров, отображения и скрытия, фокусировки и других функциональных возможностей, связанных с окнами и композицией.</span><span class="sxs-lookup"><span data-stu-id="24333-107">This class is the owner of the CoreWebView2 object, and provides support for resizing, showing and hiding, focusing, and other functionality related to windowing and composition.</span></span>

## <span data-ttu-id="24333-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="24333-108">Summary</span></span>

 <span data-ttu-id="24333-109">Участников</span><span class="sxs-lookup"><span data-stu-id="24333-109">Members</span></span>                        | <span data-ttu-id="24333-110">Описания</span><span class="sxs-lookup"><span data-stu-id="24333-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="24333-111">AcceleratorKeyPressed</span><span class="sxs-lookup"><span data-stu-id="24333-111">AcceleratorKeyPressed</span></span>](#acceleratorkeypressed) | <span data-ttu-id="24333-112">AcceleratorKeyPressed активируется при нажатии или отпускании клавиши сочетания клавиш в том случае, если WebView имеет фокус.</span><span class="sxs-lookup"><span data-stu-id="24333-112">AcceleratorKeyPressed fires when an accelerator key or key combo is pressed or released while the WebView is focused.</span></span>
[<span data-ttu-id="24333-113">Границ</span><span class="sxs-lookup"><span data-stu-id="24333-113">Bounds</span></span>](#bounds) | <span data-ttu-id="24333-114">Границы WebView.</span><span class="sxs-lookup"><span data-stu-id="24333-114">The webview bounds.</span></span>
[<span data-ttu-id="24333-115">CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="24333-115">CoreWebView2</span></span>](#corewebview2) | <span data-ttu-id="24333-116">Возвращает CoreWebView2, связанный с этим CoreWebView2Controller.</span><span class="sxs-lookup"><span data-stu-id="24333-116">Gets the CoreWebView2 associated with this CoreWebView2Controller.</span></span>
[<span data-ttu-id="24333-117">GotFocus</span><span class="sxs-lookup"><span data-stu-id="24333-117">GotFocus</span></span>](#gotfocus) | <span data-ttu-id="24333-118">Получение фокуса срабатывает, когда WebView получил фокусировку.</span><span class="sxs-lookup"><span data-stu-id="24333-118">GotFocus fires when WebView got focus.</span></span>
[<span data-ttu-id="24333-119">IsVisible</span><span class="sxs-lookup"><span data-stu-id="24333-119">IsVisible</span></span>](#isvisible) | <span data-ttu-id="24333-120">Свойство Visible определяет, нужно ли отображать или скрывать WebView.</span><span class="sxs-lookup"><span data-stu-id="24333-120">The IsVisible property determines whether to show or hide the webview.</span></span>
[<span data-ttu-id="24333-121">LostFocus</span><span class="sxs-lookup"><span data-stu-id="24333-121">LostFocus</span></span>](#lostfocus) | <span data-ttu-id="24333-122">LostFocus вызывается, когда WebView теряет фокус.</span><span class="sxs-lookup"><span data-stu-id="24333-122">LostFocus fires when WebView lost focus.</span></span>
[<span data-ttu-id="24333-123">MoveFocusRequested</span><span class="sxs-lookup"><span data-stu-id="24333-123">MoveFocusRequested</span></span>](#movefocusrequested) | <span data-ttu-id="24333-124">MoveFocusRequested активируется, когда пользователь пытается выполнить переход из WebView.</span><span class="sxs-lookup"><span data-stu-id="24333-124">MoveFocusRequested fires when user tries to tab out of the WebView.</span></span>
[<span data-ttu-id="24333-125">ParentWindow</span><span class="sxs-lookup"><span data-stu-id="24333-125">ParentWindow</span></span>](#parentwindow) | <span data-ttu-id="24333-126">Родительское окно, предоставленное приложением, используемое этим WebView, для отрисовки содержимого.</span><span class="sxs-lookup"><span data-stu-id="24333-126">The parent window provided by the app that this WebView is using to render content.</span></span>
[<span data-ttu-id="24333-127">ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="24333-127">ZoomFactor</span></span>](#zoomfactor) | <span data-ttu-id="24333-128">Коэффициент масштабирования для WebView.</span><span class="sxs-lookup"><span data-stu-id="24333-128">The zoom factor for the WebView.</span></span>
[<span data-ttu-id="24333-129">ZoomFactorChanged</span><span class="sxs-lookup"><span data-stu-id="24333-129">ZoomFactorChanged</span></span>](#zoomfactorchanged) | <span data-ttu-id="24333-130">Событие срабатывает, когда изменяется свойство ZoomFactor объекта WebView.</span><span class="sxs-lookup"><span data-stu-id="24333-130">The event fires when the ZoomFactor property of the WebView changes.</span></span>
[<span data-ttu-id="24333-131">Close (закрыть)</span><span class="sxs-lookup"><span data-stu-id="24333-131">Close</span></span>](#close) | <span data-ttu-id="24333-132">Закрывает WebView и очищает основной экземпляр браузера.</span><span class="sxs-lookup"><span data-stu-id="24333-132">Closes the WebView and cleans up the underlying browser instance.</span></span>
[<span data-ttu-id="24333-133">MoveFocus</span><span class="sxs-lookup"><span data-stu-id="24333-133">MoveFocus</span></span>](#movefocus) | <span data-ttu-id="24333-134">Перемещение фокуса в WebView.</span><span class="sxs-lookup"><span data-stu-id="24333-134">Move focus into WebView.</span></span>
[<span data-ttu-id="24333-135">NotifyParentWindowPositionChanged</span><span class="sxs-lookup"><span data-stu-id="24333-135">NotifyParentWindowPositionChanged</span></span>](#notifyparentwindowpositionchanged) | <span data-ttu-id="24333-136">Это уведомление отделено от границ, которые сообщают WebView, что родительский HWND (или любой предк) переместился.</span><span class="sxs-lookup"><span data-stu-id="24333-136">This is a notification separate from Bounds that tells WebView its parent (or any ancestor) HWND moved.</span></span>
[<span data-ttu-id="24333-137">SetBoundsAndZoomFactor</span><span class="sxs-lookup"><span data-stu-id="24333-137">SetBoundsAndZoomFactor</span></span>](#setboundsandzoomfactor) | <span data-ttu-id="24333-138">Одновременное обновление границ и свойств ZoomFactor.</span><span class="sxs-lookup"><span data-stu-id="24333-138">Update Bounds and ZoomFactor properties at the same time.</span></span>

<span data-ttu-id="24333-139">CoreWebView2Controller владеет CoreWebView2 и, если все ссылки на CoreWebView2Controller выходит из него, WebView будет закрыт.</span><span class="sxs-lookup"><span data-stu-id="24333-139">The CoreWebView2Controller owns the CoreWebView2, and if all references to the CoreWebView2Controller go away, the WebView will be closed.</span></span>

## <span data-ttu-id="24333-140">Участников</span><span class="sxs-lookup"><span data-stu-id="24333-140">Members</span></span>

#### <span data-ttu-id="24333-141">AcceleratorKeyPressed</span><span class="sxs-lookup"><span data-stu-id="24333-141">AcceleratorKeyPressed</span></span> 

<span data-ttu-id="24333-142">AcceleratorKeyPressed активируется при нажатии или отпускании клавиши сочетания клавиш в том случае, если WebView имеет фокус.</span><span class="sxs-lookup"><span data-stu-id="24333-142">AcceleratorKeyPressed fires when an accelerator key or key combo is pressed or released while the WebView is focused.</span></span>

> <span data-ttu-id="24333-143">событие EventHandler< [CoreWebView2AcceleratorKeyPressedEventArgs](microsoft-web-webview2-core-corewebview2acceleratorkeypressedeventargs.md)  >  [AcceleratorKeyPressed](#acceleratorkeypressed)</span><span class="sxs-lookup"><span data-stu-id="24333-143">public event EventHandler< [CoreWebView2AcceleratorKeyPressedEventArgs](microsoft-web-webview2-core-corewebview2acceleratorkeypressedeventargs.md) > [AcceleratorKeyPressed](#acceleratorkeypressed)</span></span>

<span data-ttu-id="24333-144">AcceleratorKeyPressed активируется при нажатии или отпускании клавиши сочетания клавиш в том случае, если WebView имеет фокус.</span><span class="sxs-lookup"><span data-stu-id="24333-144">AcceleratorKeyPressed fires when an accelerator key or key combo is pressed or released while the WebView is focused.</span></span> <span data-ttu-id="24333-145">Клавиша считается ускорителем по одной из следующих способов:</span><span class="sxs-lookup"><span data-stu-id="24333-145">A key is considered an accelerator if either:</span></span>

1. <span data-ttu-id="24333-146">В данный момент удерживается клавиша CTRL или ALT;</span><span class="sxs-lookup"><span data-stu-id="24333-146">Ctrl or Alt is currently being held, or</span></span>

1. <span data-ttu-id="24333-147">Нажатая клавиша не сопоставляется с символом.</span><span class="sxs-lookup"><span data-stu-id="24333-147">the pressed key does not map to a character.</span></span> <span data-ttu-id="24333-148">Некоторые неопределенные клавиши никогда не рассматриваются как ускорители, например Shift.</span><span class="sxs-lookup"><span data-stu-id="24333-148">A few specific keys are never considered accelerators, such as Shift.</span></span> <span data-ttu-id="24333-149">Клавиша ESC всегда считается ускорителем.</span><span class="sxs-lookup"><span data-stu-id="24333-149">The Escape key is always considered an accelerator.</span></span>

<span data-ttu-id="24333-150">Событие с автоматическим нажатием клавиши, вызванное удерживанием нажатой клавиши, также срабатывает.</span><span class="sxs-lookup"><span data-stu-id="24333-150">Autorepeated key events caused by holding the key down will also fire this event.</span></span> <span data-ttu-id="24333-151">Чтобы отфильтровать эти данные, Проверьте аргументы события "KeyEventLParam" или "PhysicalKeyStatus".</span><span class="sxs-lookup"><span data-stu-id="24333-151">You can filter these out by checking the event args' KeyEventLParam or PhysicalKeyStatus.</span></span>

<span data-ttu-id="24333-152">В оконном режиме этот обработчик событий вызывается синхронно.</span><span class="sxs-lookup"><span data-stu-id="24333-152">In windowed mode, this event handler is called synchronously.</span></span> <span data-ttu-id="24333-153">До тех пор пока вы не вызываете Handle () для аргументов события или не будет возвращен обработчик событий, процесс браузера будет заблокирован и исходящие межпроцессные вызовы COM не будут работать с RPC_E_CANTCALLOUT_ININPUTSYNCCALL.</span><span class="sxs-lookup"><span data-stu-id="24333-153">Until you call Handle() on the event args or the event handler returns, the browser process will be blocked and outgoing cross-process COM calls will fail with RPC_E_CANTCALLOUT_ININPUTSYNCCALL.</span></span> <span data-ttu-id="24333-154">Однако все методы API CoreWebView2 будут работать.</span><span class="sxs-lookup"><span data-stu-id="24333-154">All CoreWebView2 API methods will work, however.</span></span>

<span data-ttu-id="24333-155">В режиме безоконный обработчик событий вызывается асинхронно.</span><span class="sxs-lookup"><span data-stu-id="24333-155">In windowless mode, the event handler is called asynchronously.</span></span> <span data-ttu-id="24333-156">Дальнейшие входные данные не доходят до браузера, пока обработчик событий не возвратит или не завершит вызов (), но сам процесс браузера не будет заблокирован, а исходящие вызовы COM будут работать нормально.</span><span class="sxs-lookup"><span data-stu-id="24333-156">Further input will not reach the browser until the event handler returns or Handle() is called, but the browser process itself will not be blocked, and outgoing COM calls will work normally.</span></span>

<span data-ttu-id="24333-157">Рекомендуется, чтобы вы могли узнать, что вы хотите обрабатывать клавишу быстрого вызова (TRUE), как и раньше.</span><span class="sxs-lookup"><span data-stu-id="24333-157">It is recommended to call Handle(TRUE) as early as you can know that you want to handle the accelerator key.</span></span>

#### <span data-ttu-id="24333-158">Границ</span><span class="sxs-lookup"><span data-stu-id="24333-158">Bounds</span></span> 

<span data-ttu-id="24333-159">Границы WebView.</span><span class="sxs-lookup"><span data-stu-id="24333-159">The webview bounds.</span></span>

> <span data-ttu-id="24333-160">[границы](#bounds) открытых Rect</span><span class="sxs-lookup"><span data-stu-id="24333-160">public Rect [Bounds](#bounds)</span></span>

<span data-ttu-id="24333-161">Границы задаются относительно родительского дескриптора HWND.</span><span class="sxs-lookup"><span data-stu-id="24333-161">Bounds are relative to the parent HWND.</span></span> <span data-ttu-id="24333-162">Приложение может располагать WebView двумя способами:</span><span class="sxs-lookup"><span data-stu-id="24333-162">The app has two ways it can position a WebView:</span></span>

1. <span data-ttu-id="24333-163">Создание дочернего HWND, который является родительским дескриптором HWND WebView.</span><span class="sxs-lookup"><span data-stu-id="24333-163">Create a child HWND that is the WebView parent HWND.</span></span> <span data-ttu-id="24333-164">Расположите это окно в том месте, где должен быть WebView.</span><span class="sxs-lookup"><span data-stu-id="24333-164">Position this window where the WebView should be.</span></span> <span data-ttu-id="24333-165">В этом случае используйте (0, 0) для левого верхнего угла WebView Bound's (сдвиг).</span><span class="sxs-lookup"><span data-stu-id="24333-165">In this case, use (0, 0) for the WebView's Bound's top left corner (the offset).</span></span>

1. <span data-ttu-id="24333-166">Используйте окно самого высокого приложения в качестве родительского HWND WebView.</span><span class="sxs-lookup"><span data-stu-id="24333-166">Use the app's top most window as the WebView parent HWND.</span></span> <span data-ttu-id="24333-167">Задайте Bound's левый верхний угол WebView, чтобы WebView правильно расположиться в приложении.</span><span class="sxs-lookup"><span data-stu-id="24333-167">Set the WebView's Bound's top left corner so that the WebView is positioned correctly in the app.</span></span> <span data-ttu-id="24333-168">Значения границ находятся в пространстве координат основного приложения.</span><span class="sxs-lookup"><span data-stu-id="24333-168">The Bound's values are in the host's coordinate space.</span></span>

#### <span data-ttu-id="24333-169">CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="24333-169">CoreWebView2</span></span> 

<span data-ttu-id="24333-170">Возвращает CoreWebView2, связанный с этим CoreWebView2Controller.</span><span class="sxs-lookup"><span data-stu-id="24333-170">Gets the CoreWebView2 associated with this CoreWebView2Controller.</span></span>

> <span data-ttu-id="24333-171">общедоступная [CoreWebView2](microsoft-web-webview2-core-corewebview2.md) [CoreWebView2](#corewebview2)</span><span class="sxs-lookup"><span data-stu-id="24333-171">public [CoreWebView2](microsoft-web-webview2-core-corewebview2.md) [CoreWebView2](#corewebview2)</span></span>

#### <span data-ttu-id="24333-172">GotFocus</span><span class="sxs-lookup"><span data-stu-id="24333-172">GotFocus</span></span> 

<span data-ttu-id="24333-173">Получение фокуса срабатывает, когда WebView получил фокусировку.</span><span class="sxs-lookup"><span data-stu-id="24333-173">GotFocus fires when WebView got focus.</span></span>

> <span data-ttu-id="24333-174">событие EventHandler<, > [Получение фокуса](#gotfocus) на объект</span><span class="sxs-lookup"><span data-stu-id="24333-174">public event EventHandler< object > [GotFocus](#gotfocus)</span></span>

#### <span data-ttu-id="24333-175">IsVisible</span><span class="sxs-lookup"><span data-stu-id="24333-175">IsVisible</span></span> 

<span data-ttu-id="24333-176">Свойство Visible определяет, нужно ли отображать или скрывать WebView.</span><span class="sxs-lookup"><span data-stu-id="24333-176">The IsVisible property determines whether to show or hide the webview.</span></span>

> <span data-ttu-id="24333-177">Открытый bool [Visible](#isvisible)</span><span class="sxs-lookup"><span data-stu-id="24333-177">public bool [IsVisible](#isvisible)</span></span>

<span data-ttu-id="24333-178">Если для свойства Visible задано значение false, WebView будет прозрачным и не будет обрабатываться.</span><span class="sxs-lookup"><span data-stu-id="24333-178">If IsVisible is set to false, the webview will be transparent and will not be rendered.</span></span> <span data-ttu-id="24333-179">Однако это не повлияет на окно, содержащее WebView (параметр HWND, переданный в CreateCoreWebView2Controller).</span><span class="sxs-lookup"><span data-stu-id="24333-179">However, this will not affect the window containing the webview (the HWND parameter that was passed to CreateCoreWebView2Controller).</span></span> <span data-ttu-id="24333-180">Если вы хотите, чтобы окно не исчезало, вызовите для него функцию ShowWindow прямо в дополнение к изменению свойства Visible.</span><span class="sxs-lookup"><span data-stu-id="24333-180">If you want that window to disappear too, call ShowWindow on it directly in addition to modifying the IsVisible property.</span></span> <span data-ttu-id="24333-181">WebView — это дочернее окно не получает оконные сообщения, когда окно свертывания или восстановления находится в верхней части окна.</span><span class="sxs-lookup"><span data-stu-id="24333-181">WebView as a child window won't get window messages when the top window is minimized or restored.</span></span> <span data-ttu-id="24333-182">Для повышения производительности разработчик должен установить для свойства WebView значение false, если окно приложения свернуто, и вернуть значение true при восстановлении окна приложения.</span><span class="sxs-lookup"><span data-stu-id="24333-182">For performance reason, developer should set IsVisible property of the WebView to false when the app window is minimized and back to true when app window is restored.</span></span> <span data-ttu-id="24333-183">Это можно сделать, обрабатывая команды SC_MINIMIZE и SC_RESTORE при получении WM_SYSCOMMAND сообщения.</span><span class="sxs-lookup"><span data-stu-id="24333-183">App window can do this by handling SC_MINIMIZE and SC_RESTORE command upon receiving WM_SYSCOMMAND message.</span></span>

#### <span data-ttu-id="24333-184">LostFocus</span><span class="sxs-lookup"><span data-stu-id="24333-184">LostFocus</span></span> 

<span data-ttu-id="24333-185">LostFocus вызывается, когда WebView теряет фокус.</span><span class="sxs-lookup"><span data-stu-id="24333-185">LostFocus fires when WebView lost focus.</span></span>

> <span data-ttu-id="24333-186">событие EventHandler,<, объект > [LostFocus](#lostfocus)</span><span class="sxs-lookup"><span data-stu-id="24333-186">public event EventHandler< object > [LostFocus](#lostfocus)</span></span>

<span data-ttu-id="24333-187">В случае, если возникает событие MoveFocusRequested, фокус по-прежнему находится в WebView при срабатывании события MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="24333-187">In the case where MoveFocusRequested event is fired, the focus is still on WebView when MoveFocusRequested event fires.</span></span> <span data-ttu-id="24333-188">Потерянный фокус срабатывает только в том случае, если код приложения или действие по умолчанию, заданное MoveFocusRequested события, задали фокус от WebView.</span><span class="sxs-lookup"><span data-stu-id="24333-188">Lost focus only fires afterwards when app's code or default action of MoveFocusRequested event set focus away from WebView.</span></span>

#### <span data-ttu-id="24333-189">MoveFocusRequested</span><span class="sxs-lookup"><span data-stu-id="24333-189">MoveFocusRequested</span></span> 

<span data-ttu-id="24333-190">MoveFocusRequested активируется, когда пользователь пытается выполнить переход из WebView.</span><span class="sxs-lookup"><span data-stu-id="24333-190">MoveFocusRequested fires when user tries to tab out of the WebView.</span></span>

> <span data-ttu-id="24333-191">событие EventHandler< [CoreWebView2MoveFocusRequestedEventArgs](microsoft-web-webview2-core-corewebview2movefocusrequestedeventargs.md)  >  [MoveFocusRequested](#movefocusrequested)</span><span class="sxs-lookup"><span data-stu-id="24333-191">public event EventHandler< [CoreWebView2MoveFocusRequestedEventArgs](microsoft-web-webview2-core-corewebview2movefocusrequestedeventargs.md) > [MoveFocusRequested](#movefocusrequested)</span></span>

<span data-ttu-id="24333-192">При срабатывании этого события фокус WebView не изменился.</span><span class="sxs-lookup"><span data-stu-id="24333-192">The WebView's focus has not changed when this event is fired.</span></span>

#### <span data-ttu-id="24333-193">ParentWindow</span><span class="sxs-lookup"><span data-stu-id="24333-193">ParentWindow</span></span> 

<span data-ttu-id="24333-194">Родительское окно, предоставленное приложением, используемое этим WebView, для отрисовки содержимого.</span><span class="sxs-lookup"><span data-stu-id="24333-194">The parent window provided by the app that this WebView is using to render content.</span></span>

> <span data-ttu-id="24333-195">Public IntPtr [ParentWindow](#parentwindow)</span><span class="sxs-lookup"><span data-stu-id="24333-195">public IntPtr [ParentWindow](#parentwindow)</span></span>

<span data-ttu-id="24333-196">Если задать значение свойства, WebView будет перестать родительским окном в новом окне.</span><span class="sxs-lookup"><span data-stu-id="24333-196">Setting the property will cause the WebView to reparent its window to the newly provided window.</span></span>

#### <span data-ttu-id="24333-197">ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="24333-197">ZoomFactor</span></span> 

<span data-ttu-id="24333-198">Коэффициент масштабирования для WebView.</span><span class="sxs-lookup"><span data-stu-id="24333-198">The zoom factor for the WebView.</span></span>

> <span data-ttu-id="24333-199">общедоступная двойная [ZoomFactor](#zoomfactor)</span><span class="sxs-lookup"><span data-stu-id="24333-199">public double [ZoomFactor](#zoomfactor)</span></span>

<span data-ttu-id="24333-200">Обратите внимание, что изменение коэффициента масштабирования может привести к `window.innerWidth/innerHeight` изменению масштаба страницы.</span><span class="sxs-lookup"><span data-stu-id="24333-200">Note that changing zoom factor could cause `window.innerWidth/innerHeight` and page layout to change.</span></span> <span data-ttu-id="24333-201">Коэффициент масштабирования, примененный ведущим приложением путем вызова ZoomFactor, становится новым масштабом по умолчанию для WebView.</span><span class="sxs-lookup"><span data-stu-id="24333-201">A zoom factor that is applied by the host by calling ZoomFactor becomes the new default zoom for the WebView.</span></span> <span data-ttu-id="24333-202">Этот коэффициент масштабирования применяется для всех переходов и — коэффициент масштабирования WebView возвращается, когда пользователь нажимает клавиши CTRL + 0.</span><span class="sxs-lookup"><span data-stu-id="24333-202">This zoom factor applies across navigations and is the zoom factor WebView is returned to when the user presses ctrl+0.</span></span> <span data-ttu-id="24333-203">При изменении коэффициента масштабирования пользователем (в результате использования приложения, получающего ZoomFactorChanged) это масштабирование применяется только к текущей странице.</span><span class="sxs-lookup"><span data-stu-id="24333-203">When the zoom factor is changed by the user (resulting in the app receiving ZoomFactorChanged), that zoom applies only for the current page.</span></span> <span data-ttu-id="24333-204">Любой пользователь, который применяет масштабирование, используется только для текущей страницы и сбрасывается на панели навигации.</span><span class="sxs-lookup"><span data-stu-id="24333-204">Any user applied zoom is only for the current page and is reset on a navigation.</span></span> <span data-ttu-id="24333-205">Указывать zoomFactor меньше или равно 0 не разрешается.</span><span class="sxs-lookup"><span data-stu-id="24333-205">Specifying a zoomFactor less than or equal to 0 is not allowed.</span></span> <span data-ttu-id="24333-206">WebView также имеет внутренний поддерживаемый диапазон коэффициента масштабирования.</span><span class="sxs-lookup"><span data-stu-id="24333-206">WebView also has an internal supported zoom factor range.</span></span> <span data-ttu-id="24333-207">Если указанный коэффициент масштаба выходит за пределы этого диапазона, он будет нормализован в пределах диапазона, а событие ZoomFactorChanged будет инициировано для фактического коэффициента масштабирования.</span><span class="sxs-lookup"><span data-stu-id="24333-207">When a specified zoom factor is out of that range, it will be normalized to be within the range, and a ZoomFactorChanged event will be fired for the real applied zoom factor.</span></span> <span data-ttu-id="24333-208">При выполнении этой нормализации диапазона свойство ZoomFactor будет указывать коэффициент масштабирования, указанный в предыдущем изменении свойства ZoomFactor, пока событие ZoomFactorChanged не будет получено после WebView применяет нормализованный коэффициент масштабирования.</span><span class="sxs-lookup"><span data-stu-id="24333-208">When this range normalization happens, the ZoomFactor property will report the zoom factor specified during the previous modification of the ZoomFactor property until the ZoomFactorChanged event is received after webview applies the normalized zoom factor.</span></span>

#### <span data-ttu-id="24333-209">ZoomFactorChanged</span><span class="sxs-lookup"><span data-stu-id="24333-209">ZoomFactorChanged</span></span> 

<span data-ttu-id="24333-210">Событие срабатывает, когда изменяется свойство ZoomFactor объекта WebView.</span><span class="sxs-lookup"><span data-stu-id="24333-210">The event fires when the ZoomFactor property of the WebView changes.</span></span>

> <span data-ttu-id="24333-211">событие EventHandler< объект > [ZoomFactorChanged](#zoomfactorchanged)</span><span class="sxs-lookup"><span data-stu-id="24333-211">public event EventHandler< object > [ZoomFactorChanged](#zoomfactorchanged)</span></span>

<span data-ttu-id="24333-212">Событие может срабатывать из-за того, что вызывающий объект изменил свойство ZoomFactor или пользователь вручную изменял масштаб.</span><span class="sxs-lookup"><span data-stu-id="24333-212">The event could fire because the caller modified the ZoomFactor property, or due to the user manually modifying the zoom.</span></span> <span data-ttu-id="24333-213">При изменении вызывающим абонентом с помощью свойства ZoomFactor внутренний коэффициент масштабирования немедленно обновляется, и событие ZoomFactorChanged не выводится.</span><span class="sxs-lookup"><span data-stu-id="24333-213">When it is modified by the caller via the ZoomFactor property, the internal zoom factor is updated immediately and there will be no ZoomFactorChanged event.</span></span> <span data-ttu-id="24333-214">WebView связывает последний использованный коэффициент масштабирования для каждого сайта.</span><span class="sxs-lookup"><span data-stu-id="24333-214">WebView associates the last used zoom factor for each site.</span></span> <span data-ttu-id="24333-215">Поэтому коэффициент масштабирования может изменяться при переходе на другую страницу.</span><span class="sxs-lookup"><span data-stu-id="24333-215">Therefore, it is possible for the zoom factor to change when navigating to a different page.</span></span> <span data-ttu-id="24333-216">При изменении коэффициента масштабирования из-за этого событие ZoomFactorChanged срабатывает сразу после события ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="24333-216">When the zoom factor changes due to this, the ZoomFactorChanged event fires right after the ContentLoading event.</span></span>

#### <span data-ttu-id="24333-217">Close (закрыть)</span><span class="sxs-lookup"><span data-stu-id="24333-217">Close</span></span> 

<span data-ttu-id="24333-218">Закрывает WebView и очищает основной экземпляр браузера.</span><span class="sxs-lookup"><span data-stu-id="24333-218">Closes the WebView and cleans up the underlying browser instance.</span></span>

> <span data-ttu-id="24333-219">общедоступное [закрытие](#close)void ()</span><span class="sxs-lookup"><span data-stu-id="24333-219">public void [Close](#close)()</span></span>

<span data-ttu-id="24333-220">Очистка экземпляра браузера приведет к освобождению ресурсов, WebView в сети.</span><span class="sxs-lookup"><span data-stu-id="24333-220">Cleaning up the browser instance will release the resources powering the WebView.</span></span> <span data-ttu-id="24333-221">Экземпляр браузера будет закрыт, если он не используется другими веб – представлениями.</span><span class="sxs-lookup"><span data-stu-id="24333-221">The browser instance will be shut down if there are no other WebViews using it.</span></span>

<span data-ttu-id="24333-222">После вызова метода Close все вызовы методов завершатся сбоем, и обработчики событий прекратятся.</span><span class="sxs-lookup"><span data-stu-id="24333-222">After calling Close, all method calls will fail and event handlers will stop firing.</span></span> <span data-ttu-id="24333-223">В частности, WebView будет освобождать ссылки на обработчики событий при вызове Close.</span><span class="sxs-lookup"><span data-stu-id="24333-223">Specifically, the WebView will release its references to its event handlers when Close is called.</span></span>

<span data-ttu-id="24333-224">Метод Close вызывается неявно, когда CoreWebView2Controller теряет свою конечную ссылку и является независимым.</span><span class="sxs-lookup"><span data-stu-id="24333-224">Close is implicitly called when the CoreWebView2Controller loses its final reference and is destructed.</span></span> <span data-ttu-id="24333-225">Но рекомендуется явным образом вызывать метод Close, чтобы избежать случайного цикла ссылок между WebView и кодом приложения.</span><span class="sxs-lookup"><span data-stu-id="24333-225">But it is best practice to explicitly call Close to avoid any accidental cycle of references between the WebView and the app code.</span></span> <span data-ttu-id="24333-226">В частности, если вы захватываете ссылку на WebView в обработчике событий, вы создадите цикл ссылки между WebView и обработчиком событий.</span><span class="sxs-lookup"><span data-stu-id="24333-226">Specifically, if you capture a reference to the WebView in an event handler you will create a reference cycle between the WebView and the event handler.</span></span> <span data-ttu-id="24333-227">Вызов Close приведет к прерыванию этого цикла, освобождая все обработчики событий.</span><span class="sxs-lookup"><span data-stu-id="24333-227">Calling Close will break this cycle by releasing all event handlers.</span></span> <span data-ttu-id="24333-228">Но чтобы избежать такой ситуации, рекомендуется как явным образом вызвать метод Close для WebView и не захватить ссылку на WebView, чтобы убедиться, что WebView может быть корректно очищено.</span><span class="sxs-lookup"><span data-stu-id="24333-228">But to avoid this situation it is best practice both to explicitly call Close on the WebView and to not capture a reference to the WebView to ensure the WebView can be cleaned up correctly.</span></span>

#### <span data-ttu-id="24333-229">MoveFocus</span><span class="sxs-lookup"><span data-stu-id="24333-229">MoveFocus</span></span> 

<span data-ttu-id="24333-230">Перемещение фокуса в WebView.</span><span class="sxs-lookup"><span data-stu-id="24333-230">Move focus into WebView.</span></span>

> <span data-ttu-id="24333-231">общедоступная void [MoveFocus](#movefocus)(причина[CoreWebView2MoveFocusReason](./namespace-microsoft-web-webview2-core.md) )</span><span class="sxs-lookup"><span data-stu-id="24333-231">public void [MoveFocus](#movefocus)([CoreWebView2MoveFocusReason](./namespace-microsoft-web-webview2-core.md) reason)</span></span>

<span data-ttu-id="24333-232">WebView получит фокус, и фокус будет установлен на элемент корреспондента на странице, которая размещена в WebView.</span><span class="sxs-lookup"><span data-stu-id="24333-232">WebView will get focus and focus will be set to correspondent element in the page hosted in the WebView.</span></span> <span data-ttu-id="24333-233">В целях программной причины фокус установлен на ранее сфокусированный элемент или элемент по умолчанию, если нет ранее фокусируемого элемента.</span><span class="sxs-lookup"><span data-stu-id="24333-233">For Programmatic reason, focus is set to previously focused element or the default element if there is no previously focused element.</span></span> <span data-ttu-id="24333-234">В следующей причине фокус задается для первого элемента.</span><span class="sxs-lookup"><span data-stu-id="24333-234">For Next reason, focus is set to the first element.</span></span> <span data-ttu-id="24333-235">По этой причине фокус установлен на последний элемент.</span><span class="sxs-lookup"><span data-stu-id="24333-235">For Previous reason, focus is set to the last element.</span></span> <span data-ttu-id="24333-236">WebView также может сосредоточиться на взаимодействии с пользователем, например, щелкнув на WebView или TAB.</span><span class="sxs-lookup"><span data-stu-id="24333-236">WebView can also got focus through user interaction like clicking into WebView or Tab into it.</span></span> <span data-ttu-id="24333-237">Для табуляции приложение может вызвать MoveFocus с помощью кнопки Далее или назад, чтобы выровнять элементы Tab и SHIFT + TAB, если это необходимо, если WebView является следующим элементом с вкладками.</span><span class="sxs-lookup"><span data-stu-id="24333-237">For tabbing, the app can call MoveFocus with Next or Previous to align with tab and shift+tab respectively when it decides the WebView is the next tabbable element.</span></span> <span data-ttu-id="24333-238">Кроме того, приложение может вызвать IsDialogMessage как часть цикла обработки сообщений, чтобы платформа автоматически обрабатывала табуляцию.</span><span class="sxs-lookup"><span data-stu-id="24333-238">Or, the app can call IsDialogMessage as part of its message loop to allow the platform to auto handle tabbing.</span></span> <span data-ttu-id="24333-239">Платформа будет повернута на все окна с помощью WS_TABSTOP.</span><span class="sxs-lookup"><span data-stu-id="24333-239">The platform will rotate through all windows with WS_TABSTOP.</span></span> <span data-ttu-id="24333-240">Когда WebView получает фокус из IsDialogMessage, он будет внутренне размещать фокус на первом или последнем элементе Tab и Shift + Tab соответственно.</span><span class="sxs-lookup"><span data-stu-id="24333-240">When the WebView gets focus from IsDialogMessage, it will internally put the focus on the first or last element for tab and shift+tab respectively.</span></span>

#### <span data-ttu-id="24333-241">NotifyParentWindowPositionChanged</span><span class="sxs-lookup"><span data-stu-id="24333-241">NotifyParentWindowPositionChanged</span></span> 

<span data-ttu-id="24333-242">Это уведомление отделено от границ, которые сообщают WebView, что родительский HWND (или любой предк) переместился.</span><span class="sxs-lookup"><span data-stu-id="24333-242">This is a notification separate from Bounds that tells WebView its parent (or any ancestor) HWND moved.</span></span>

> <span data-ttu-id="24333-243">общедоступная void [NotifyParentWindowPositionChanged](#notifyparentwindowpositionchanged)()</span><span class="sxs-lookup"><span data-stu-id="24333-243">public void [NotifyParentWindowPositionChanged](#notifyparentwindowpositionchanged)()</span></span>

<span data-ttu-id="24333-244">Это необходимо для правильной работы специальных возможностей и некоторых диалоговых окон в WebView.</span><span class="sxs-lookup"><span data-stu-id="24333-244">This is needed for accessibility and certain dialogs in WebView to work correctly.</span></span>

#### <span data-ttu-id="24333-245">SetBoundsAndZoomFactor</span><span class="sxs-lookup"><span data-stu-id="24333-245">SetBoundsAndZoomFactor</span></span> 

<span data-ttu-id="24333-246">Одновременное обновление границ и свойств ZoomFactor.</span><span class="sxs-lookup"><span data-stu-id="24333-246">Update Bounds and ZoomFactor properties at the same time.</span></span>

> <span data-ttu-id="24333-247">Public void [SetBoundsAndZoomFactor](#setboundsandzoomfactor)(границы Rect, Double ZoomFactor)</span><span class="sxs-lookup"><span data-stu-id="24333-247">public void [SetBoundsAndZoomFactor](#setboundsandzoomfactor)(Rect Bounds, double ZoomFactor)</span></span>

<span data-ttu-id="24333-248">Эта операция является атомарной с точки зрения хоста.</span><span class="sxs-lookup"><span data-stu-id="24333-248">This operation is atomic from the host's perspective.</span></span> <span data-ttu-id="24333-249">После того как вы вернете эту функцию, свойства Bounds и ZoomFactor будут обновлены при успешном выполнении функции, или ни один из них не будет обновляться при сбое функции.</span><span class="sxs-lookup"><span data-stu-id="24333-249">After returning from this function, the Bounds and ZoomFactor properties will have both been updated if the function is successful, or neither will be updated if the function fails.</span></span> <span data-ttu-id="24333-250">Если границы и ZoomFactor обновляются одним масштабом (то есть границы и ZoomFactor оба двойных), то страница не будет видеть изменение в Window. innerWidth/innerHeight, а WebView будет отображать содержимое на новом размере и масштабе без промежуточных преобразований.</span><span class="sxs-lookup"><span data-stu-id="24333-250">If Bounds and ZoomFactor are both updated by the same scale (i.e. Bounds and ZoomFactor are both doubled), then the page will not see a change in window.innerWidth/innerHeight and the WebView will render the content at the new size and zoom without intermediate renderings.</span></span> <span data-ttu-id="24333-251">Эта функция также может использоваться для обновления только одного из ZoomFactor или границ путем передачи нового значения для одного и текущего значения другого.</span><span class="sxs-lookup"><span data-stu-id="24333-251">This function can also be used to update just one of ZoomFactor or Bounds by passing in the new value for one and the current value for the other.</span></span>
