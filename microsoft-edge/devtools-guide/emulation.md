---
description: Использование панели эмуляции для проверки различных профилей браузера, размеров экрана и разрешения и координат местоположения GPS
title: DevTools — Эмуляция
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/04/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools, эмуляция устройств, разработка с откликом, географическое расположение, разрешение
ms.custom: seodec18
ms.openlocfilehash: 6eaa8d79cfd64473dcc52beff5659b39054e2a48
ms.sourcegitcommit: 912609aa49864e3363aaa3b245ff2aa4bec3fc3e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/08/2020
ms.locfileid: "11104849"
---
# <span data-ttu-id="bb6cd-104">Эмуляция</span><span class="sxs-lookup"><span data-stu-id="bb6cd-104">Emulation</span></span>  

> [!NOTE]
> <span data-ttu-id="bb6cd-105">Новый Microsoft Edge строится с помощью Chromium и начинается в версии 75.</span><span class="sxs-lookup"><span data-stu-id="bb6cd-105">The new Microsoft Edge is built using Chromium, and starts at version 75.</span></span>  <span data-ttu-id="bb6cd-106">Чтобы получить дополнительные сведения, [Скачайте новый Microsoft Edge][MicrosoftNewEdge]и ознакомьтесь с новыми [средствами разработчика Microsoft EDGE (Chromium)][DevtoolsGuideChromium].</span><span class="sxs-lookup"><span data-stu-id="bb6cd-106">For more information, [download the new Microsoft Edge][MicrosoftNewEdge], and try out the new [Microsoft Edge (Chromium) Developer Tools][DevtoolsGuideChromium].</span></span>  
> 
> <span data-ttu-id="bb6cd-107">Чтобы эмулировать различные устройства, браузеры, размеры экрана и разрешения в новом DevTools, перейдите в [раздел Эмуляция мобильных устройств в Microsoft Edge \ (Chromium \) DevTools][DevtoolsGuideChromiumDeviceMode].</span><span class="sxs-lookup"><span data-stu-id="bb6cd-107">To emulate different devices, browsers, screen sizes, and resolutions in the new DevTools, navigate to [Emulate Mobile Devices in Microsoft Edge \(Chromium\) DevTools][DevtoolsGuideChromiumDeviceMode].</span></span>  

<span data-ttu-id="bb6cd-108">Панель **эмуляции** помогает выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="bb6cd-108">The **Emulation** panel helps with the following activities.</span></span>    

*   <span data-ttu-id="bb6cd-109">Имитация различных [профилей устройств](#device), [браузеров](#browser-profile)и [размеров экрана и их разрешений](#display)</span><span class="sxs-lookup"><span data-stu-id="bb6cd-109">Simulate various [device profiles](#device), [browsers](#browser-profile), and [screen sizes and resolutions](#display)</span></span>  
*   <span data-ttu-id="bb6cd-110">Проверка различных [параметров и координат географического положения](#geolocation)</span><span class="sxs-lookup"><span data-stu-id="bb6cd-110">Test different [geolocation settings and coordinates](#geolocation)</span></span>  

:::image type="complex" source="./media/emulation.png" alt-text="Панель эмуляции DevTools Microsoft Edge" lightbox="./media/emulation.png":::
   <span data-ttu-id="bb6cd-112">Панель **эмуляции** DevTools Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="bb6cd-112">The Microsoft Edge DevTools **Emulation** panel</span></span>  
:::image-end:::  

1.  <span data-ttu-id="bb6cd-113">При нажатии кнопки **сохранить параметры эмуляции** все изменения, внесенные в параметры эмуляции рабочего стола по умолчанию, сохраняются, даже когда вы закрываете и снова открываете DevTools.</span><span class="sxs-lookup"><span data-stu-id="bb6cd-113">The **Persist Emulation settings** button saves any changes you made from the default desktop emulation settings, even when you close and reopen the DevTools.</span></span>  

1.  <span data-ttu-id="bb6cd-114">Кнопка **сброса параметров эмуляции** сбрасывает параметры эмуляции в профиль рабочего стола по умолчанию и строку агента пользователя Microsoft Edge с отключенным параметром GPS.</span><span class="sxs-lookup"><span data-stu-id="bb6cd-114">The **Reset Emulation settings** button resets your emulation settings back to the default Desktop browser profile and Microsoft Edge user agent string with GPS turned off.</span></span>  

1.  <span data-ttu-id="bb6cd-115">Когда какие – либо из этих параметров будут изменены по умолчанию, на вкладке **Эмуляция** отображается информационное оповещение о том, что некоторые аспекты поведения браузера эмулируется.</span><span class="sxs-lookup"><span data-stu-id="bb6cd-115">When any of these options are changed from the default, the **Emulation** tab displays an informational alert to indicate that some aspect of the behavior of your browser is being emulated.</span></span>  

## <span data-ttu-id="bb6cd-116">Устройство</span><span class="sxs-lookup"><span data-stu-id="bb6cd-116">Device</span></span>  

<span data-ttu-id="bb6cd-117">Выберите один из готовых списков профилей устройств Windows, которые автоматически настраивают другие параметры эмуляции или определяют свои собственные **пользовательские** настройки.</span><span class="sxs-lookup"><span data-stu-id="bb6cd-117">Pick from a preset list of Windows device profiles that automatically configure the other emulation options or specify your own **Custom** configuration.</span></span>  <span data-ttu-id="bb6cd-118">Чтобы сбросить все средства эмуляции, вернитесь к параметру **Default** .</span><span class="sxs-lookup"><span data-stu-id="bb6cd-118">Switch back to **Default** to reset all the emulation tools.</span></span>  

## <span data-ttu-id="bb6cd-119">Режим</span><span class="sxs-lookup"><span data-stu-id="bb6cd-119">Mode</span></span>  

### <span data-ttu-id="bb6cd-120">Профиль браузера</span><span class="sxs-lookup"><span data-stu-id="bb6cd-120">Browser profile</span></span>  

<span data-ttu-id="bb6cd-121">Для имитации страницы, работающей на устройстве с Windows Phone, можно быстро изменить параметр **профиля браузера** на **Windows Phone**.</span><span class="sxs-lookup"><span data-stu-id="bb6cd-121">A quick way to simulate your page running on a Windows Phone device is to change the **Browser profile** setting to **Windows Phone**.</span></span>  

#### <span data-ttu-id="bb6cd-122">Строка агента пользователя</span><span class="sxs-lookup"><span data-stu-id="bb6cd-122">User agent string</span></span>  

<span data-ttu-id="bb6cd-123">Изменение строки агента пользователя для имитации другого браузера — это хороший первый шаг в ошибках отладки, происходящих только в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="bb6cd-123">Modifying your user agent string to mimic another browser is a good first step in debugging errors that are only happening in Microsoft Edge.</span></span>  

<span data-ttu-id="bb6cd-124">В сценариях для определения используемого браузера используется строка агента пользователя.</span><span class="sxs-lookup"><span data-stu-id="bb6cd-124">Scripts use the user agent string to detect which browser is used.</span></span>  <span data-ttu-id="bb6cd-125">Сценарий может быть внешним, внутренним, внешним и внутренним.</span><span class="sxs-lookup"><span data-stu-id="bb6cd-125">Script may be front-end, back-end, or front-end and back-end.</span></span>  <span data-ttu-id="bb6cd-126">Несмотря на то, что ваш код не использует обнаружение браузеров, ваш код может наследовать его от библиотеки JavaScript стороннего поставщика или серверного сценария.</span><span class="sxs-lookup"><span data-stu-id="bb6cd-126">Although your code does not use browser detection, your code may inherit it from a third-party JavaScript library or server-side script.</span></span>  

<span data-ttu-id="bb6cd-127">Проблема с обнаружением браузера заключается в том, что вы можете масштабировать и повторно использовать возможности на веб-странице, используя допущения о возможностях браузера.</span><span class="sxs-lookup"><span data-stu-id="bb6cd-127">The problem with browser detection is that you may scale-back \(or change\) features in your webpage using assumptions about browser capabilities.</span></span> <span data-ttu-id="bb6cd-128">Вместо этого следует использовать обнаружение компонентов для определения возможностей браузера.</span><span class="sxs-lookup"><span data-stu-id="bb6cd-128">Instead, you should consider using feature detection to detect the capabilities of your browser.</span></span>  <span data-ttu-id="bb6cd-129">Непредвиденное поведение может возникать из-за одной из указанных ниже ситуаций.</span><span class="sxs-lookup"><span data-stu-id="bb6cd-129">Unexpected behavior may occur because of one of the following situations.</span></span>  

*   <span data-ttu-id="bb6cd-130">Код, предназначенный для Windows Internet Explorer 8, может работать иначе в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="bb6cd-130">Code targeted at Windows Internet Explorer 8 may run differently in Microsoft Edge.</span></span>  
*   <span data-ttu-id="bb6cd-131">Функция, которую должен поддерживать ваш браузер, отключена из-за предположения, сделанного разработчиком.</span><span class="sxs-lookup"><span data-stu-id="bb6cd-131">A feature that your browser should support is disabled, because of an assumption made by the developer.</span></span>  

<span data-ttu-id="bb6cd-132">Если при изменении строки агента пользователя происходит удаление проблемы, обнаружение браузера, возможно, будет заблокировано.</span><span class="sxs-lookup"><span data-stu-id="bb6cd-132">If changing your user agent string clears up the problem, browser detection is likely culprit.</span></span>  

## <span data-ttu-id="bb6cd-133">Монитор</span><span class="sxs-lookup"><span data-stu-id="bb6cd-133">Display</span></span>  

<span data-ttu-id="bb6cd-134">Эмуляция экрана для предварительного просмотра сайта на различных размерах и разрешениях экрана.</span><span class="sxs-lookup"><span data-stu-id="bb6cd-134">Display emulation to preview your site on different screen sizes and resolutions.</span></span>  

*   <span data-ttu-id="bb6cd-135">обычные мониторы для настольных ПК</span><span class="sxs-lookup"><span data-stu-id="bb6cd-135">conventional desktop monitors</span></span>  
*   <span data-ttu-id="bb6cd-136">небольшие экраны для мобильных устройств</span><span class="sxs-lookup"><span data-stu-id="bb6cd-136">smaller mobile screens</span></span>  
*   <span data-ttu-id="bb6cd-137">более новые дисплеи с высоким разрешением</span><span class="sxs-lookup"><span data-stu-id="bb6cd-137">newer high-resolution displays</span></span>  

<span data-ttu-id="bb6cd-138">Эмуляции приспособлены для поиска соответствия физических размеров экранов с имитацией.</span><span class="sxs-lookup"><span data-stu-id="bb6cd-138">Emulations are adapted to try to match the physical dimensions of the screens being emulated.</span></span>  <span data-ttu-id="bb6cd-139">Эмулированные Пиксели могут выглядеть как сжатые или развернутые.</span><span class="sxs-lookup"><span data-stu-id="bb6cd-139">Emulated pixels may appear compressed or expanded.</span></span> <span data-ttu-id="bb6cd-140">Эмуляция не рекомендуется, если нужно протестировать точечное расположение элементов HTML.</span><span class="sxs-lookup"><span data-stu-id="bb6cd-140">Emulation is not recommended if you need to test pixel-perfect positioning of HTML elements.</span></span>  <span data-ttu-id="bb6cd-141">Однако Эмуляция, тем не менее, хорошо подходит для тестирования и выявления более крупных проблем, связанных с размещением элементов.</span><span class="sxs-lookup"><span data-stu-id="bb6cd-141">Emulation is, however, good for testing responsive designs and identifying larger element positioning issues.</span></span>  

### <span data-ttu-id="bb6cd-142">Ориентация</span><span class="sxs-lookup"><span data-stu-id="bb6cd-142">Orientation</span></span>  

<span data-ttu-id="bb6cd-143">Выберите режим **Альбомная** или **Книжная** .</span><span class="sxs-lookup"><span data-stu-id="bb6cd-143">Choose from **Landscape** or **Portrait** mode.</span></span>  

### <span data-ttu-id="bb6cd-144">Разрешение</span><span class="sxs-lookup"><span data-stu-id="bb6cd-144">Resolution</span></span>  

<span data-ttu-id="bb6cd-145">Выберите готовый набор разрешений для устройства или укажите собственный **Настраиваемый** файл конфигурации.  Поддерживаются разрешения до 80 дюйма и 3820 x 2160.</span><span class="sxs-lookup"><span data-stu-id="bb6cd-145">Choose from a preset list of popular device resolutions, or specify your own **Custom** config.  Resolutions of up to 80 inches and 3820 x 2160 are supported.</span></span>  

## <span data-ttu-id="bb6cd-146">Геолокация</span><span class="sxs-lookup"><span data-stu-id="bb6cd-146">Geolocation</span></span>  

<span data-ttu-id="bb6cd-147">Если ваш веб-сайт использует [API географического расположения][MdnGeolocationUsing] для предоставления услуг на основе местоположения, вы можете воспользоваться следующими действиями для удобства работы на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="bb6cd-147">If your website uses the [Geolocation API][MdnGeolocationUsing] to provide location-based services, the following activities are available from the convenience of your desktop.</span></span>  

*   <span data-ttu-id="bb6cd-148">простое тестирование разных координат GPS</span><span class="sxs-lookup"><span data-stu-id="bb6cd-148">easily test different GPS coordinates</span></span>  
*   <span data-ttu-id="bb6cd-149">легко тестировать различные состояния датчиков</span><span class="sxs-lookup"><span data-stu-id="bb6cd-149">easily test different sensor states</span></span>  

<span data-ttu-id="bb6cd-150">Эти параметры переопределяют любые фактические координаты GPS и состояние датчика на устройствах, которые поддерживают географическое расположение.</span><span class="sxs-lookup"><span data-stu-id="bb6cd-150">The settings override any actual GPS coordinates and the sensor state on devices that support geolocation.</span></span>  

<span data-ttu-id="bb6cd-151">Прежде чем использовать расположение устройства, ваш веб-сайт должен запросить и получить разрешение у пользователя.</span><span class="sxs-lookup"><span data-stu-id="bb6cd-151">Your website must request and be granted permission from a user before using the device location.</span></span>  <span data-ttu-id="bb6cd-152">Проверьте работу сайта с разрешениями расположения и без него на панели " **Параметры** Microsoft Edge".</span><span class="sxs-lookup"><span data-stu-id="bb6cd-152">Test how your site behaves with and without location permissions from the Microsoft Edge **Settings** panel.</span></span>  

<span data-ttu-id="bb6cd-153">**...** >  **Параметры**  >  **Просмотр дополнительных параметров**  >  Разрешения для веб **-сайта**  >  **Управление**</span><span class="sxs-lookup"><span data-stu-id="bb6cd-153">**...** > **Settings** > **View advanced settings** > **Website permissions** > **Manage**</span></span>  

:::image type="complex" source="./media/settings_manage_permissions.png" alt-text="Панель эмуляции DevTools Microsoft Edge" lightbox="./media/settings_manage_permissions.png":::
   <span data-ttu-id="bb6cd-155">Управление разрешениями веб-сайта с помощью панели " **Параметры** Microsoft Edge"</span><span class="sxs-lookup"><span data-stu-id="bb6cd-155">Manage website permissions from the Microsoft Edge **Settings** panel</span></span>  
:::image-end:::  

## <span data-ttu-id="bb6cd-156">Ярлыки</span><span class="sxs-lookup"><span data-stu-id="bb6cd-156">Shortcuts</span></span>

| <span data-ttu-id="bb6cd-157">Действие</span><span class="sxs-lookup"><span data-stu-id="bb6cd-157">Action</span></span>  | <span data-ttu-id="bb6cd-158">Установленное напрямую доверие</span><span class="sxs-lookup"><span data-stu-id="bb6cd-158">Shortcut</span></span>  |  
|:--- |:--- |  
| <span data-ttu-id="bb6cd-159">Сброс параметров эмуляции</span><span class="sxs-lookup"><span data-stu-id="bb6cd-159">Reset Emulation settings</span></span> | `Ctrl`+`Shift`+`L` |  

<!-- links -->  


[DevtoolsGuideChromium]: /microsoft-edge/devtools-guide-chromium "Инструменты разработчика Microsoft EDGE (Chromium) | Документы Microsoft"  
[DevtoolsGuideChromiumDeviceMode]: /microsoft-edge/devtools-guide-chromium/device-mode "Эмуляция мобильных устройств в Microsoft Edge DevTools | Документы Microsoft"  

[MicrosoftNewEdge]: https://www.microsoft.com/edge "Скачать новый браузер Microsoft Edge"  

[MdnGeolocationUsing]: https://developer.mozilla.org/docs/Web/API/Geolocation/Using_geolocation "API географического положения | MDN"  