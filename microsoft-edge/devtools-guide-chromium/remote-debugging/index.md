---
description: Удаленная отладка динамического содержимого на устройстве Android с компьютера с Windows или macOS.
title: Начало работы с удаленными отладкой устройств с Android
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: c6bdb48460fb8f6ff26cbb02872e33cb50dd6e12
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125365"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  

# <span data-ttu-id="f7031-104">Начало работы с удаленными отладкой устройств с Android</span><span class="sxs-lookup"><span data-stu-id="f7031-104">Get started with remote debugging Android devices</span></span>  

<span data-ttu-id="f7031-105">Удаленная отладка динамического содержимого на устройстве Android с компьютера Windows или macOS.</span><span class="sxs-lookup"><span data-stu-id="f7031-105">Remote debug live content on an Android device from your Windows or macOS computer.</span></span>  <span data-ttu-id="f7031-106">На следующей странице учебника вы узнаете, как выполнять указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="f7031-106">The following tutorial page teaches you how to complete the following actions.</span></span>  

*   <span data-ttu-id="f7031-107">Настройте устройство Android для удаленной отладки и найдите его на компьютере разработчика.</span><span class="sxs-lookup"><span data-stu-id="f7031-107">Set up your Android device for remote debugging, and discover it from your development machine.</span></span>  
*   <span data-ttu-id="f7031-108">Изучите и отлаживать динамический контент на устройстве с Android с компьютера для разработки.</span><span class="sxs-lookup"><span data-stu-id="f7031-108">Inspect and debug live content on your Android device from your development machine.</span></span>  
*   <span data-ttu-id="f7031-109">Содержимое ролика с устройства Android на экземпляр DevTools на компьютере разработчика.</span><span class="sxs-lookup"><span data-stu-id="f7031-109">Screencast content from your Android device onto a DevTools instance on your development machine.</span></span>  

<!--  
:::image type="complex" source="../media/remote-debugging--remote-debugging.msft.png" alt-text="Remote Debugging lets you inspect a page running on an Android device from your development machine" lightbox="../media/remote-debugging--remote-debugging.msft.png":::
   old Figure 1.  Remote Debugging lets you inspect a page running on an Android device from your development machine  
:::image-end:::  
-->  

> [!NOTE]
> <span data-ttu-id="f7031-110">Удаленная отладка приложения Microsoft EDGE на устройствах с iOS в настоящее время не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f7031-110">Remote debugging the Microsoft Edge app on iOS devices is not currently supported.</span></span>  <span data-ttu-id="f7031-111">Следующее руководство специально ориентировано на удаленную отладку Microsoft EDGE на устройствах с Android.</span><span class="sxs-lookup"><span data-stu-id="f7031-111">The following guide is specifically focused on remote debugging Microsoft Edge on Android devices.</span></span>
> <span data-ttu-id="f7031-112">Если у вас есть устройство macOS, следуйте инструкциям [по отладке Brightcove][BrightcoveSupportDebuggingMobileDevices] для удаленной отладки Microsoft EDGE на устройстве с iOS с помощью Safari.</span><span class="sxs-lookup"><span data-stu-id="f7031-112">If you have a macOS device, follow the [Brightcove Debugging guide][BrightcoveSupportDebuggingMobileDevices] to remotely debug Microsoft Edge on an iOS device using Safari.</span></span>  <span data-ttu-id="f7031-113">Для получения дополнительных сведений о средстве веб-инспектора в Safari перейдите на [страницу веб-разработки Safari][AppleDeveloperSafariTools].</span><span class="sxs-lookup"><span data-stu-id="f7031-113">For more information about the Web Inspector tool in Safari, navigate to [Safari Web Development Tools][AppleDeveloperSafariTools].</span></span>  

## <span data-ttu-id="f7031-114">Шаг 1: обнаружение устройства с Android</span><span class="sxs-lookup"><span data-stu-id="f7031-114">Step 1: Discover your Android device</span></span>  

<span data-ttu-id="f7031-115">Рабочий процесс, описанный ниже, подходит для большинства пользователей.</span><span class="sxs-lookup"><span data-stu-id="f7031-115">The workflow below works for most users.</span></span>  <span data-ttu-id="f7031-116">Дополнительные сведения можно найти в разделе [Устранение неполадок: DevTools не удается найти раздел устройства Android](#troubleshooting-devtools-is-not-detecting-the-android-device) .</span><span class="sxs-lookup"><span data-stu-id="f7031-116">For more help, navigate to [Troubleshooting: DevTools is not detecting the Android device](#troubleshooting-devtools-is-not-detecting-the-android-device) section.</span></span>  

1.  <span data-ttu-id="f7031-117">Откройте экран **Параметры разработчика** на устройстве с Android.</span><span class="sxs-lookup"><span data-stu-id="f7031-117">Open the **Developer Options** screen on your Android.</span></span>  <span data-ttu-id="f7031-118">Дополнительные сведения можно найти в разделе [Настройка параметров разработчика на устройстве][AndroidDeveloperStudioDevOptions].</span><span class="sxs-lookup"><span data-stu-id="f7031-118">For more information, navigate to [Configure On-Device Developer Options][AndroidDeveloperStudioDevOptions].</span></span>  
1.  <span data-ttu-id="f7031-119">Выберите **включить отладку USB**.</span><span class="sxs-lookup"><span data-stu-id="f7031-119">Choose **Enable USB Debugging**.</span></span>  
1.  <span data-ttu-id="f7031-120">На своем компьютере для разработки откройте Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="f7031-120">On your development machine, open Microsoft Edge.</span></span>  
1.  <span data-ttu-id="f7031-121">Перейдите на `edge://inspect` страницу в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="f7031-121">Navigate to the `edge://inspect` page in Microsoft Edge.</span></span>  
    
    :::image type="complex" source="../media/remote-debugging-edge-inspect-no-targets.msft.png" alt-text="Remote Debugging lets you inspect a page running on an Android device from your development machine" lightbox="../media/remote-debugging-edge-inspect-no-targets.msft.png":::
       <span data-ttu-id="f7031-123">Рисунок 1.</span><span class="sxs-lookup"><span data-stu-id="f7031-123">Figure 1.</span></span>  <span data-ttu-id="f7031-124">`edge://inspect`Страница в Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="f7031-124">The `edge://inspect` page in Microsoft Edge</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f7031-125">Подключите устройство Android непосредственно к компьютеру разработчика с помощью USB-кабеля.</span><span class="sxs-lookup"><span data-stu-id="f7031-125">Connect your Android device directly to your development machine using a USB cable.</span></span>  <span data-ttu-id="f7031-126">При первой попытке подключения на экран будет выведено сообщение о том, что DevTools обнаруживает неизвестное устройство.</span><span class="sxs-lookup"><span data-stu-id="f7031-126">The first time you try to connect, a prompt should be displayed about DevTools detecting an unknown device.</span></span>  <span data-ttu-id="f7031-127">Подтвердите запрос разрешения на **отладку USB** на устройстве с Android.</span><span class="sxs-lookup"><span data-stu-id="f7031-127">Accept the **Allow USB Debugging** permission prompt on your Android device.</span></span>  
    
    :::image type="complex" source="../media/remote-debugging-android-permissions-prompt.msft.png" alt-text="Remote Debugging lets you inspect a page running on an Android device from your development machine" lightbox="../media/remote-debugging-android-permissions-prompt.msft.png":::
       <span data-ttu-id="f7031-129">Рисунок 2.</span><span class="sxs-lookup"><span data-stu-id="f7031-129">Figure 2.</span></span>  <span data-ttu-id="f7031-130">Предупреждение о разрешении разрешения на **отладку USB** на устройстве с Android</span><span class="sxs-lookup"><span data-stu-id="f7031-130">The **Allow USB Debugging** permission prompt on an Android device</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f7031-131">Если вы видите название модели устройства с Android, Microsoft Edge успешно установил подключение к устройству.</span><span class="sxs-lookup"><span data-stu-id="f7031-131">If the model name of your Android device is displayed, then Microsoft Edge has successfully established the connection to your device.</span></span>  <span data-ttu-id="f7031-132">Перейдите к разделу [этап 2](#step-2-debug-content-on-your-android-device-from-your-development-machine) .</span><span class="sxs-lookup"><span data-stu-id="f7031-132">Continue to the [Step 2](#step-2-debug-content-on-your-android-device-from-your-development-machine) section.</span></span>  
    
    <!--  
    :::image type="complex" source="../media/remote-debugging--unknown-device.msft.png" alt-text="Remote Debugging lets you inspect a page running on an Android device from your development machine" lightbox="../media/remote-debugging--unknown-device.msft.png":::
       old Figure 4.  The **Remote Devices** tab has successfully detected an unknown device that is pending authorization  
    :::image-end:::
    -->  
    
### <span data-ttu-id="f7031-133">Устранение неполадок: DevTools не может обнаружить устройство с Android</span><span class="sxs-lookup"><span data-stu-id="f7031-133">Troubleshooting: DevTools is not detecting the Android device</span></span>  

<span data-ttu-id="f7031-134">Ниже приведены советы по устранению неполадок, связанных с правильными параметрами оборудования.</span><span class="sxs-lookup"><span data-stu-id="f7031-134">Use the following tips to help you troubleshoot the correct settings for your hardware.</span></span>  

*   <span data-ttu-id="f7031-135">Если вы используете USB-концентратор, попробуйте подключить устройство Android прямо к компьютеру разработчика.</span><span class="sxs-lookup"><span data-stu-id="f7031-135">If you are using a USB hub, try connecting your Android device directly to your development machine.</span></span>  
*   <span data-ttu-id="f7031-136">Попробуйте отключить кабель USB между устройством Android и компьютером разработчика, а затем снова подключить USB-кабель.</span><span class="sxs-lookup"><span data-stu-id="f7031-136">Try unplugging the USB cable between your Android device and development machine, and then re-plugging your USB cable.</span></span>  <span data-ttu-id="f7031-137">Выполнение задачи во время разблокировки экранов компьютера Android и разработки.</span><span class="sxs-lookup"><span data-stu-id="f7031-137">Complete the task while your Android and development machine screens are unlocked.</span></span>  
*   <span data-ttu-id="f7031-138">Убедитесь, что USB-кабель работает.</span><span class="sxs-lookup"><span data-stu-id="f7031-138">Make sure that your USB cable works.</span></span>  <span data-ttu-id="f7031-139">Вы должны иметь возможность проверять файлы на устройстве с Android с компьютера, на котором ведется разработка.</span><span class="sxs-lookup"><span data-stu-id="f7031-139">You should be able to inspect files on your Android device from your development machine.</span></span>  

<span data-ttu-id="f7031-140">Чтобы убедиться, что программное обеспечение правильно настроено, воспользуйтесь приведенными ниже советами.</span><span class="sxs-lookup"><span data-stu-id="f7031-140">Use the following tips to help you verify that your software is set up correctly.</span></span>  

*   <span data-ttu-id="f7031-141">Если на вашем компьютере разработчика установлена операционная система Windows, попробуйте установить драйверы USB для устройства с Android вручную.</span><span class="sxs-lookup"><span data-stu-id="f7031-141">If your development machine is running Windows, try manually installing the USB drivers for your Android device.</span></span>  <span data-ttu-id="f7031-142">Для получения дополнительных сведений перейдите к разделу [Установка драйверов USB для OEM][AndroidDeveloperToolsOemUsb].</span><span class="sxs-lookup"><span data-stu-id="f7031-142">For more information, navigate to [Install OEM USB Drivers][AndroidDeveloperToolsOemUsb].</span></span>  
*   <span data-ttu-id="f7031-143">Некоторые комбинации устройств Windows и Android (особенно Samsung) требуют дополнительных настроек.</span><span class="sxs-lookup"><span data-stu-id="f7031-143">Some combinations of Windows and Android devices \(especially Samsung\) require additional settings.</span></span>  <span data-ttu-id="f7031-144">Дополнительные сведения можно найти в [разделе устройства DevTools, когда устройство подключено к сети][Stackoverflow21925992].</span><span class="sxs-lookup"><span data-stu-id="f7031-144">For more information, navigate to [DevTools Devices does not detect device when plugged in][Stackoverflow21925992].</span></span>  

<span data-ttu-id="f7031-145">Воспользуйтесь приведенными ниже советами, чтобы устранить проблему с отображением запроса на **отладку USB** на устройстве с Android.</span><span class="sxs-lookup"><span data-stu-id="f7031-145">Use the following tips to help you troubleshoot if the **Allow USB Debugging** prompt is not displayed on your Android device.</span></span>  

*   <span data-ttu-id="f7031-146">Отключение кабеля USB и повторное подключение к нему, когда DevTools на компьютере разработки и отображается начальный экран на устройстве с Android.</span><span class="sxs-lookup"><span data-stu-id="f7031-146">Disconnecting and then re-connecting the USB cable while DevTools is in focus on your development machine and your Android homescreen is showing.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="f7031-147">Это сообщение появляется, если ваши экраны вашего компьютера Android или разработчика заблокированы.</span><span class="sxs-lookup"><span data-stu-id="f7031-147">The prompt is displayed if your Android or development machine screens are locked.</span></span>  

*   <span data-ttu-id="f7031-148">Обновление параметров отображения для устройства Android и компьютера для разработки таким образом, чтобы все они никогда не переходили в спящий режим.</span><span class="sxs-lookup"><span data-stu-id="f7031-148">Updating the display settings for your Android device and development machine so that each never goes to sleep.</span></span>  
*   <span data-ttu-id="f7031-149">Установка режима USB для устройства с Android на PTP.</span><span class="sxs-lookup"><span data-stu-id="f7031-149">Setting the USB mode for Android to PTP.</span></span>  <span data-ttu-id="f7031-150">Для получения дополнительных сведений перейдите в [Galaxy S4 не показывает диалоговое окно "авторизация USB"][StackexchangeAndroid101933].</span><span class="sxs-lookup"><span data-stu-id="f7031-150">For more information, navigate to [Galaxy S4 does not show Authorize USB debugging dialog box][StackexchangeAndroid101933].</span></span>  
*   <span data-ttu-id="f7031-151">Выберите **отозвать разрешения на отладку USB** на экране **Параметры разработчика** на устройстве с Android, чтобы сбросить его в новое состояние.</span><span class="sxs-lookup"><span data-stu-id="f7031-151">Choose **Revoke USB Debugging Authorizations** from the **Developer Options** screen on your Android device to reset it to a fresh state.</span></span>  

<span data-ttu-id="f7031-152">Если вы нашли решение, которое не было упомянуто на этой странице, или на [DevTools устройствах не обнаружите устройства при подключении][Stackoverflow21925992] к переполнению стека, добавьте свое решение на вопрос о переполнении стека.</span><span class="sxs-lookup"><span data-stu-id="f7031-152">If you find a solution that is not mentioned on this page or in [DevTools Devices does not detect device when plugged in][Stackoverflow21925992] on Stack Overflow, please add your solution to the Stack Overflow question</span></span><!--, or [open an issue in the webfundamentals repository][GitHubWebFundamentalsNewIssue]--><span data-ttu-id="f7031-153">!</span><span class="sxs-lookup"><span data-stu-id="f7031-153">!</span></span>  

## <span data-ttu-id="f7031-154">Шаг 2: Отладка содержимого на устройстве с Android с компьютера для разработки</span><span class="sxs-lookup"><span data-stu-id="f7031-154">Step 2: Debug content on your Android device from your development machine</span></span>  

1.  <span data-ttu-id="f7031-155">Откройте Microsoft EDGE на устройстве с Android.</span><span class="sxs-lookup"><span data-stu-id="f7031-155">Open Microsoft Edge on your Android device.</span></span>  
1.  <span data-ttu-id="f7031-156">Перейдите к нужному `edge://inspect` названию модели устройства с Android, а затем выберите серийный номер устройства.</span><span class="sxs-lookup"><span data-stu-id="f7031-156">Navigate to `edge://inspect`, the model name of your Android device is displayed, followed by the device serial number.</span></span>  <span data-ttu-id="f7031-157">Ниже показано, как будет отображаться версия Microsoft EDGE, установленная на устройстве, с номером версии в круглых скобках.</span><span class="sxs-lookup"><span data-stu-id="f7031-157">Below that, the version of Microsoft Edge running on the device should be displayed, with the version number in parentheses.</span></span>  <span data-ttu-id="f7031-158">Каждая открытая вкладка Microsoft Edge получает уникальный раздел.</span><span class="sxs-lookup"><span data-stu-id="f7031-158">Each open Microsoft Edge tab gets a unique section.</span></span>  <span data-ttu-id="f7031-159">Вы можете работать с этой вкладкой в разделе.</span><span class="sxs-lookup"><span data-stu-id="f7031-159">You may interact with that tab from a section.</span></span>  <!--If there are any apps using WebView, a section for each of those apps should be displayed, too.  --><!--In [**Figure 5**](#figure-5) there are no tabs or WebViews open.  -->  
    
    :::image type="complex" source="../media/remote-debugging-edge-inspect-with-targets.msft.png" alt-text="Remote Debugging lets you inspect a page running on an Android device from your development machine" lightbox="../media/remote-debugging-edge-inspect-with-targets.msft.png":::
       <span data-ttu-id="f7031-161">Рисунок 3.</span><span class="sxs-lookup"><span data-stu-id="f7031-161">Figure 3.</span></span>  <span data-ttu-id="f7031-162">Подключенное удаленное устройство</span><span class="sxs-lookup"><span data-stu-id="f7031-162">A connected remote device</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f7031-163">В текстовом поле **открыть вкладку с URL-адресом** введите URL-адрес и нажмите кнопку **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="f7031-163">In the **Open tab with url** text box, enter a URL and then choose **Open**.</span></span>  <span data-ttu-id="f7031-164">Страница откроется на новой вкладке на устройстве с Android.</span><span class="sxs-lookup"><span data-stu-id="f7031-164">The page opens in a new tab on your Android device.</span></span>  
1.  <span data-ttu-id="f7031-165">Нажмите кнопку " **проверить** " рядом с URL-адресом, который вы только что открыли.</span><span class="sxs-lookup"><span data-stu-id="f7031-165">Choose **inspect** next to the URL that you just opened.</span></span>  <span data-ttu-id="f7031-166">Откроется новый экземпляр DevTools.</span><span class="sxs-lookup"><span data-stu-id="f7031-166">A new DevTools instance opens.</span></span>  

<!-- The version of Microsoft Edge running on your Android device determines the version of DevTools that opens on your development machine.  
    So, if your Android device is running a very old version of Microsoft Edge, the DevTools instance may look very different than what you are used to.   -->

### <span data-ttu-id="f7031-167">Дополнительные действия: перемещение фокуса, перезагрузка или закрытие вкладки</span><span class="sxs-lookup"><span data-stu-id="f7031-167">More actions: focus, reload, or close a tab</span></span>  

<span data-ttu-id="f7031-168">Выберите **вкладку фокус**, **Перезагрузка**или **Закрыть** рядом с вкладкой, на которую вы хотите установить фокус, перезагрузить или закрыть.</span><span class="sxs-lookup"><span data-stu-id="f7031-168">Choose **focus tab**, **reload**, or **close** next to the tab that you want to focus, reload, or close.</span></span>  

:::image type="complex" source="../media/remote-debugging-edge-inspect-with-targets-buttons.msft.png" alt-text="Remote Debugging lets you inspect a page running on an Android device from your development machine" lightbox="../media/remote-debugging-edge-inspect-with-targets-buttons.msft.png":::
   <span data-ttu-id="f7031-170">Рисунок 4.</span><span class="sxs-lookup"><span data-stu-id="f7031-170">Figure 4.</span></span>  <span data-ttu-id="f7031-171">Кнопки для фокусировки, повторной загрузки и закрытия вкладки</span><span class="sxs-lookup"><span data-stu-id="f7031-171">The buttons for focusing, reloading, or closing a tab</span></span>  
:::image-end:::  

### <span data-ttu-id="f7031-172">Проверка элементов</span><span class="sxs-lookup"><span data-stu-id="f7031-172">Inspect elements</span></span>  

<span data-ttu-id="f7031-173">Перейдите на панель **элементы** экземпляра DevTools и наведите указатель мыши на элемент, чтобы выделить его в окне просмотра на устройстве с Android.</span><span class="sxs-lookup"><span data-stu-id="f7031-173">Go to the **Elements** panel of your DevTools instance, and hover over an element to highlight it in the viewport of your Android device.</span></span>  

<span data-ttu-id="f7031-174">Вы также можете выбрать элемент на экране устройства с Android, чтобы выбрать его на панели " **элементы** ".</span><span class="sxs-lookup"><span data-stu-id="f7031-174">You may also select an element on your Android device screen to select it in the **Elements** panel.</span></span>  <span data-ttu-id="f7031-175">В экземпляре DevTools нажмите кнопку **выбрать элемент** ![ , выберите элемент ][ImageSelectElementIcon] , а затем выберите элемент на экране устройства с Android.</span><span class="sxs-lookup"><span data-stu-id="f7031-175">Choose **Select Element** \(![Select Element][ImageSelectElementIcon]\) icon on your DevTools instance, and then select the element on your Android device screen.</span></span>  

> [!NOTE]
> <span data-ttu-id="f7031-176">**Элемент "выбрать** " отключается после первого выбора, поэтому для использования этой функции необходимо повторно включить его.</span><span class="sxs-lookup"><span data-stu-id="f7031-176">**Select Element** is disabled after the first selection, so you must re-enable it every time you want to use the feature.</span></span>  

### <span data-ttu-id="f7031-177">Демонстрация экрана Android на компьютере разработчика</span><span class="sxs-lookup"><span data-stu-id="f7031-177">Screencast your Android screen to your development machine</span></span>  

<span data-ttu-id="f7031-178">Нажмите кнопку **вкл** ![ ][ImageToggleScreencastIcon] ., чтобы просмотреть содержимое устройства с Android в экземпляре DevTools, щелкнув значок Показать презентацию.</span><span class="sxs-lookup"><span data-stu-id="f7031-178">Choose **Toggle Screencast** \(![Toggle Screencast][ImageToggleScreencastIcon]\) icon to view the content of your Android device in your DevTools instance.</span></span>  

<span data-ttu-id="f7031-179">Вы можете взаимодействовать с презентацией следующими способами.</span><span class="sxs-lookup"><span data-stu-id="f7031-179">You are able to interact with the screencast in the following ways.</span></span>  

*   <span data-ttu-id="f7031-180">Нажатия клавиш переводятся в касания, и на устройстве обрабатывались соответствующие события сенсорного ввода.</span><span class="sxs-lookup"><span data-stu-id="f7031-180">Clicks are translated into taps, firing proper touch events on the device.</span></span>  
*   <span data-ttu-id="f7031-181">Нажатия клавиш на компьютере отправляются на устройство.</span><span class="sxs-lookup"><span data-stu-id="f7031-181">Keystrokes on your computer are sent to the device.</span></span>  
*   <span data-ttu-id="f7031-182">Чтобы смоделировать жест сжатия, удерживайте `Shift` при перетаскивании.</span><span class="sxs-lookup"><span data-stu-id="f7031-182">To simulate a pinch gesture, hold `Shift` while dragging.</span></span>  
*   <span data-ttu-id="f7031-183">Для прокрутки используйте сенсорной панели, колесико мыши или смахивание с помощью указателя мыши.</span><span class="sxs-lookup"><span data-stu-id="f7031-183">To scroll, use your trackpad or mouse wheel, or fling with your mouse pointer.</span></span>

> [!NOTE]
> <span data-ttu-id="f7031-184">Чтобы сделать презентацию более подсказками, воспользуйтесь приведенными ниже советами.</span><span class="sxs-lookup"><span data-stu-id="f7031-184">Use the following tips to help you screencast.</span></span>  
> 
> *   <span data-ttu-id="f7031-185">В ролики отображается только содержимое страницы.</span><span class="sxs-lookup"><span data-stu-id="f7031-185">Screencasts only display page content.</span></span>  <span data-ttu-id="f7031-186">Прозрачные части презентации представляют интерфейсы устройства, такие как адресная строка Microsoft EDGE, строка состояния Android или клавиатура Android.</span><span class="sxs-lookup"><span data-stu-id="f7031-186">Transparent portions of the screencast represent device interfaces, such as the Microsoft Edge address bar, the Android status bar, or the Android keyboard.</span></span>  
> *   <span data-ttu-id="f7031-187">Ролики негативно влияют на частоту кадров.</span><span class="sxs-lookup"><span data-stu-id="f7031-187">Screencasts negatively affect frame rates.</span></span>  <span data-ttu-id="f7031-188">Отключите экранную анимацию, изменяя прокрутки или анимации, чтобы получить более точную картину производительности страницы.</span><span class="sxs-lookup"><span data-stu-id="f7031-188">Disable screencasting while measuring scrolls or animations to get a more accurate picture of the performance of your page.</span></span>  
> *   <span data-ttu-id="f7031-189">Если экран вашего устройства с Android блокируется, содержимое презентации исчезнет.</span><span class="sxs-lookup"><span data-stu-id="f7031-189">If your Android device screen locks, the content of your screencast disappears.</span></span>  <span data-ttu-id="f7031-190">Разблокируйте экран устройства с Android для автоматического возобновления ролика.</span><span class="sxs-lookup"><span data-stu-id="f7031-190">Unlock your Android device screen to automatically resume the screencast.</span></span>  

## <span data-ttu-id="f7031-191">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="f7031-191">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageSelectElementIcon]: /microsoft-edge/devtools-guide-chromium/media/select-element-icon.msft.png  
[ImageToggleScreencastIcon]: /microsoft-edge/devtools-guide-chromium/media/toggle-screencast-icon.msft.png  

<!-- links -->  

[AndroidDeveloperStudioDevOptions]: https://developer.android.com/studio/debug/dev-options "Настройка параметров разработчика на устройстве | Разработчик Android"  
[AndroidDeveloperToolsOemUsb]: https://developer.android.com/tools/extras/oem-usb.html "Установка драйверов USB для OEM | Разработчики Android"  

[AppleDeveloperSafariTools]: https://developer.apple.com/safari/tools "Средства разработки веб-браузера Safari | Разработчик Apple"  

[BrightcoveSupportDebuggingMobileDevices]: https://support.brightcove.com/debugging-mobile-devices "Отладка на мобильных устройствах | Поддержка Brightcove"  

<!-- [GitHubWebFundamentalsNewIssue]: https://github.com/Alphabet/webfundamentals/issues/new?title=[Remote%20Debugging] "GitHub - Web Fundamentals - New Issue"  -->  

[StackexchangeAndroid101933]: https://android.stackexchange.com/questions/101933 "ADB — обмен данными в стеке для энтузиастов Android"  

[Stackoverflow21925992]: https://stackoverflow.com/questions/21925992 "Устройства DevTools не обнаруживают устройства при подключении к стеку с переполнением"  

> [!NOTE]
> <span data-ttu-id="f7031-198">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f7031-198">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="f7031-199">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/index) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="f7031-199">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="f7031-201">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f7031-201">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
