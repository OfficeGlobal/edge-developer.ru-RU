---
description: Ваше задание не заканчивается, и вы не гарантируете, что ваш сайт будет работать в Microsoft EDGE и Android.  Несмотря на то, что режим устройства может имитировать ряд других устройств, таких как iPhone, мы рекомендуем вам извлечь решения для эмуляции, предоставляемой другими браузерами.
title: Эмуляция и тестирование других браузеров
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 1a7cc1c7e0a49760f30afdc16921824372b3a1aa
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "11124945"
---
<!-- Copyright Meggin Kearney and Paul Bakaus

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->

# <span data-ttu-id="965a3-105">Эмуляция и тестирование других браузеров</span><span class="sxs-lookup"><span data-stu-id="965a3-105">Emulate and test other browsers</span></span>  

<span data-ttu-id="965a3-106">Ваше задание не заканчивается, и вы не гарантируете, что ваш сайт будет работать в Microsoft EDGE и Android.</span><span class="sxs-lookup"><span data-stu-id="965a3-106">Your job does not end with ensuring your site runs great across Microsoft Edge and Android.</span></span>  <span data-ttu-id="965a3-107">Несмотря на то, что режим устройства может имитировать ряд других устройств, таких как iPhone, мы рекомендуем вам извлечь решения для эмуляции, предоставляемой другими браузерами.</span><span class="sxs-lookup"><span data-stu-id="965a3-107">Even though Device Mode is able to simulate a range of other devices like iPhones, we encourage you to check out solutions for emulation provided by other browsers.</span></span>  

### <span data-ttu-id="965a3-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="965a3-108">Summary</span></span>  

*   <span data-ttu-id="965a3-109">Если вы не имеете определенного устройства или хотите проверит что-либо, лучше использовать эмуляцию устройства прямо в браузере.</span><span class="sxs-lookup"><span data-stu-id="965a3-109">When you do not have a particular device, or want to do a spot check on something, the best option is to emulate the device right inside your browser.</span></span>  
*   <span data-ttu-id="965a3-110">Эмуляторы устройств и симуляторы позволяют имитировать сайт разработки на различных устройствах с рабочей станции.</span><span class="sxs-lookup"><span data-stu-id="965a3-110">Device emulators and simulators enable you to mimic your development site on a range of devices from your workstation.</span></span>  
*   <span data-ttu-id="965a3-111">Облачные Эмуляторы позволяют автоматизировать модульные тесты для сайта на разных платформах.</span><span class="sxs-lookup"><span data-stu-id="965a3-111">Cloud-based emulators enable you to automate unit tests for your site across different platforms.</span></span>  

## <span data-ttu-id="965a3-112">Эмуляторы браузеров</span><span class="sxs-lookup"><span data-stu-id="965a3-112">Browser emulators</span></span>  

<span data-ttu-id="965a3-113">Эмуляторы браузеров очень удобны для проверки скорости реагирования на сайт, но каждый из них не эмулирует различия в API, поддержку CSS и некоторые поведения, которые вы видите в браузере для мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="965a3-113">Browser emulators are great for testing the responsiveness of a site, but each does not emulate differences in API, CSS support, and certain behaviors that you see on a mobile browser.</span></span>  <span data-ttu-id="965a3-114">Протестируйте сайт в браузерах, работающих на реальных устройствах, чтобы убедиться в том, что все работает должным образом.</span><span class="sxs-lookup"><span data-stu-id="965a3-114">Test your site on browsers running on real devices to be certain everything behaves as expected.</span></span>  

### <span data-ttu-id="965a3-115">Режим разработки с откликом Firefox</span><span class="sxs-lookup"><span data-stu-id="965a3-115">Firefox Responsive Design View</span></span>  

<span data-ttu-id="965a3-116">У Firefox есть [реагирующий на запросы режим разработки][MDNResponsiveDesignMode] , с помощью которого вы сможете остановиться на определенных устройствах, а вместо этого Изучите изменения структуры на распространенных размерах экрана или собственного размера, перетаскивая края.</span><span class="sxs-lookup"><span data-stu-id="965a3-116">Firefox has a [responsive design view][MDNResponsiveDesignMode] that encourages you to stop thinking in terms of specific devices and instead explore how your design changes at common screen sizes or your own size by dragging the edges.</span></span>  

### <span data-ttu-id="965a3-117">Эмуляция EdgeHTML</span><span class="sxs-lookup"><span data-stu-id="965a3-117">EdgeHTML emulation</span></span>  

<span data-ttu-id="965a3-118">Для эмуляции телефонной системы Windows используйте [встроенную эмуляцию][DevToolsEdgeHtmlEmulation]Microsoft Edge \ (EdgeHTML \).</span><span class="sxs-lookup"><span data-stu-id="965a3-118">To emulate Windows Phones, use the Microsoft Edge \(EdgeHTML\) [built-in emulation][DevToolsEdgeHtmlEmulation].</span></span>  

<span data-ttu-id="965a3-119">[Эмуляция IE 11][Ie11DevToolsEmulation] используется для моделирования того, как страница может выглядеть в более ранних версиях Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="965a3-119">Use [IE 11 Emulation][Ie11DevToolsEmulation] to simulate how your page may look in older versions of Internet Explorer.</span></span>  

## <span data-ttu-id="965a3-120">Эмуляторы устройств и симуляторы</span><span class="sxs-lookup"><span data-stu-id="965a3-120">Device emulators and simulators</span></span>  

<span data-ttu-id="965a3-121">Симуляторы устройств и Эмуляторы моделируют не только среду браузера, но и все устройство.</span><span class="sxs-lookup"><span data-stu-id="965a3-121">Device simulators and emulators simulate not just the browser environment but the entire device.</span></span>  <span data-ttu-id="965a3-122">Каждый из них полезен для тестирования возможностей, требующих интеграции с ОС, например входных данных формы с виртуальными клавиатурами.</span><span class="sxs-lookup"><span data-stu-id="965a3-122">Each are useful to test things that require OS integration, for example form input with virtual keyboards.</span></span>  

### <span data-ttu-id="965a3-123">Эмулятор Android</span><span class="sxs-lookup"><span data-stu-id="965a3-123">Android emulator</span></span>  

<!--  
:::image type="complex" source="../media/device-mode-android-emulator-stock-browser.msft.png" alt-text="Stock Browser in Android Emulator" lightbox="../media/device-mode-android-emulator-stock-browser.msft.png":::
   Stock Browser in Android Emulator  
:::image-end:::  
-->  

<span data-ttu-id="965a3-124">В настоящее время невозможно установить Microsoft EDGE на эмуляторе Android.</span><span class="sxs-lookup"><span data-stu-id="965a3-124">At the moment, there is no way to install Microsoft Edge on an Android emulator.</span></span>  <span data-ttu-id="965a3-125">Однако вы можете использовать браузер Android, оболочку содержимого Chromium и Firefox для Android, который мы рассмотрим позже в этом руководстве.</span><span class="sxs-lookup"><span data-stu-id="965a3-125">However, you may use the Android Browser, the Chromium Content Shell, and Firefox for Android which we review later in this guide.</span></span>  <span data-ttu-id="965a3-126">Chromium Content Shell запускает тот же механизм отрисовки Chromium, что и Microsoft EDGE, но не имеет каких бы то ни было специальных возможностей браузера.</span><span class="sxs-lookup"><span data-stu-id="965a3-126">Chromium Content Shell runs the same Chromium rendering engine as Microsoft Edge, but comes without any of the browser specific features.</span></span>  

<span data-ttu-id="965a3-127">Эмулятор Android поставляется с пакетом SDK для Android, который необходимо загрузить в составе [Android Studio][AndroidStudioDownload].</span><span class="sxs-lookup"><span data-stu-id="965a3-127">The Android emulator comes with the Android SDK which you need to download as part of [Android Studio][AndroidStudioDownload].</span></span>  <span data-ttu-id="965a3-128">Затем следуйте инструкциям по [настройке виртуального устройства][AndroidStudioCreateManageVirtualDevices] и [запуску эмулятора][AndroidStudioRunAppsAndroidEmulator].</span><span class="sxs-lookup"><span data-stu-id="965a3-128">Then follow the instructions to [set up a virtual device][AndroidStudioCreateManageVirtualDevices] and [start the emulator][AndroidStudioRunAppsAndroidEmulator].</span></span>  
<span data-ttu-id="965a3-129">После загрузки эмулятора щелкните значок браузера и проверьте свой сайт в старом браузере акций для Android.</span><span class="sxs-lookup"><span data-stu-id="965a3-129">Once your emulator is booted, click on the Browser icon, and test your site on the old Stock Browser for Android.</span></span>  

#### <span data-ttu-id="965a3-130">Оболочка содержимого Chromium на Android</span><span class="sxs-lookup"><span data-stu-id="965a3-130">Chromium content shell on Android</span></span>  

<!--  
:::image type="complex" source="../media/device-mode-android-avd-contentshell.msft.png" alt-text="Stock Browser in Android Emulator" lightbox="../media/device-mode-android-avd-contentshell.msft.png":::
   Android Emulator Content Shell  
:::image-end:::  
-->  

<span data-ttu-id="965a3-131">Чтобы установить оболочку содержимого Chromium для Android, оставьте симулятор запущенным и выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="965a3-131">To install the Chromium Content Shell for Android, leave your emulator running and run the following command.</span></span>  

```shell
git clone https://github.com/PaulKinlan/chromium-android-installer.git
chmod u+x ./chromium-android-installer/*.sh
./chromium-android-installer/install-chromeandroid.sh
```  

<span data-ttu-id="965a3-132">Теперь вы можете протестировать сайт с помощью оболочки содержимого Chromium.</span><span class="sxs-lookup"><span data-stu-id="965a3-132">Now you are able to test your site with the Chromium Content Shell.</span></span>  

#### <span data-ttu-id="965a3-133">Firefox для Android</span><span class="sxs-lookup"><span data-stu-id="965a3-133">Firefox on Android</span></span>  

<!--  
:::image type="complex" source="../media/device-mode-ff-on-android-emulator.msft.png" alt-text="Stock Browser in Android Emulator" lightbox="../media/device-mode-ff-on-android-emulator.msft.png":::
   Firefox Icon on Android Emulator  
:::image-end:::  
-->  

<span data-ttu-id="965a3-134">Как и в оболочке содержимого Chromium, вы можете получить APK для установки Firefox на эмулятор.</span><span class="sxs-lookup"><span data-stu-id="965a3-134">Similar to the Chromium Content Shell, you are able to get an APK to install Firefox onto the emulator.</span></span>  

<span data-ttu-id="965a3-135">[Скачайте правильный файл. apk][MozillaFirefoxDownload].</span><span class="sxs-lookup"><span data-stu-id="965a3-135">[Download the correct .apk file][MozillaFirefoxDownload].</span></span>  

<span data-ttu-id="965a3-136">Чтобы установить файл на открытый эмулятор или подключенное устройство с Android, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="965a3-136">To install the file onto an open emulator or connected Android device, run the following command.</span></span>  

```shell
adb install <path_to_APK>/fennec-XX.X.XX.android-arm.apk
```  

### <span data-ttu-id="965a3-137">Имитатор iOS</span><span class="sxs-lookup"><span data-stu-id="965a3-137">iOS simulator</span></span>  

<span data-ttu-id="965a3-138">Имитатор iOS для Mac OS X поставляется с Xcode, который [устанавливается из App Store][MacAppStoreXcode].</span><span class="sxs-lookup"><span data-stu-id="965a3-138">The iOS simulator for Mac OS X comes with Xcode, which you [install from the App Store][MacAppStoreXcode].</span></span>  

<span data-ttu-id="965a3-139">Когда вы закончите работу, научитесь работать с имитатором с помощью [документации разработчика Apple][AppleSimulatorHelp].</span><span class="sxs-lookup"><span data-stu-id="965a3-139">When you are done, learn how to work with the simulator through [Apple Developer documentation][AppleSimulatorHelp].</span></span>  

> [!NOTE]
> <span data-ttu-id="965a3-140">Чтобы не открывать Xcode каждый раз, когда вы хотите использовать имитатор iOS, откройте его, а затем щелкните правой кнопкой мыши значок имитатора iOS в Dock и выберите пункт **сохранить в Закреплениях**.</span><span class="sxs-lookup"><span data-stu-id="965a3-140">To avoid having to open Xcode every time you want to use the iOS Simulator, open it, then right-click the iOS Simulator icon in your dock and choose **Keep in Dock**.</span></span>  <span data-ttu-id="965a3-141">Теперь просто щелкаю этот значок, когда он вам нужен.</span><span class="sxs-lookup"><span data-stu-id="965a3-141">Now just click this icon whenever you need it.</span></span>  

###  <span data-ttu-id="965a3-142">Microsoft EDGE (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="965a3-142">Microsoft Edge (EdgeHTML)</span></span>  

:::image type="complex" source="../media/device-mode-modern-ie-vm.msft.png" alt-text="Stock Browser in Android Emulator" lightbox="../media/device-mode-modern-ie-vm.msft.png":::
   <span data-ttu-id="965a3-144">Современная виртуальная машина IE</span><span class="sxs-lookup"><span data-stu-id="965a3-144">Modern IE VM</span></span>  
:::image-end:::  

<span data-ttu-id="965a3-145">Microsoft Edge \ (EdgeHTML \) виртуальные машины \ (VMS \) предоставляют доступ к разным версиям EdgeHTML и IE на компьютере с помощью VirtualBox \ (или VMWare).</span><span class="sxs-lookup"><span data-stu-id="965a3-145">Microsoft Edge \(EdgeHTML\) Virtual Machines \(VMs\) enable you to access different versions of EdgeHTML and IE on your computer via VirtualBox \(or VMWare\).</span></span>  <span data-ttu-id="965a3-146">Выберите [виртуальную машину на странице загрузки][MicrosoftDeveloperEdgeVms].</span><span class="sxs-lookup"><span data-stu-id="965a3-146">Choose a [virtual machine on the download page][MicrosoftDeveloperEdgeVms].</span></span>  

## <span data-ttu-id="965a3-147">Эмуляторы и симуляторы на основе облака</span><span class="sxs-lookup"><span data-stu-id="965a3-147">Cloud-based emulators and simulators</span></span>  

<span data-ttu-id="965a3-148">Если вы не можете использовать Эмуляторы и у вас нет доступа к реальным устройствам, Эмуляторы на основе облака являются следующим лучшим делом.</span><span class="sxs-lookup"><span data-stu-id="965a3-148">If you are not able to use the emulators and do not have access to real devices, then cloud-based emulators are the next best thing.</span></span>  <span data-ttu-id="965a3-149">Большое преимущество облачных эмуляторов на реальных устройствах и местных эмуляторах состоит в том, что вы можете автоматизировать тестирование модулей для сайта на разных платформах.</span><span class="sxs-lookup"><span data-stu-id="965a3-149">A big advantage of cloud-based emulators over real devices and local emulators is that you are able to automate unit tests for your site across different platforms.</span></span>  

*   <span data-ttu-id="965a3-150">[BrowserStack (коммерческая версия)][|::ref1::|] — это самый простой способ использовать ручное тестирование.</span><span class="sxs-lookup"><span data-stu-id="965a3-150">[BrowserStack (commercial)][|::ref1::|] is the easiest to use for manual testing.</span></span>  <span data-ttu-id="965a3-151">Вы выбираете операционную систему, выбираете версию браузера и тип устройства, выбираете URL-адрес, который будет просматривать размещенную виртуальную машину, с которой вы можете взаимодействовать.</span><span class="sxs-lookup"><span data-stu-id="965a3-151">You select an operating system, select your browser version and device type, select a URL to browse, and it spins up a hosted virtual machine with which you may interact.</span></span>  <span data-ttu-id="965a3-152">Вы также можете запускать несколько эмуляторов на одном экране, что позволяет тестировать внешний вид и функции приложения на нескольких устройствах одновременно.</span><span class="sxs-lookup"><span data-stu-id="965a3-152">You are able to also run multiple emulators in the same screen, enabling you to test the look and feel of your app across multiple devices at the same time.</span></span>  
*   <span data-ttu-id="965a3-153">[SauceLabs (коммерческая версия)][SauceLabs] позволяет выполнять модульные тесты внутри эмулятора, который может быть весьма полезен для создания сценариев на сайте и просмотра видеозаписи после этого на различных устройствах.</span><span class="sxs-lookup"><span data-stu-id="965a3-153">[SauceLabs (commercial)][SauceLabs] enables you to run unit tests inside of an emulator, which may be really useful for scripting a flow through your site and watching the video recording of this afterwards on various devices.</span></span>  <span data-ttu-id="965a3-154">Вы также можете выполнять тестирование на сайте вручную.</span><span class="sxs-lookup"><span data-stu-id="965a3-154">You are also able to do manual testing with your site.</span></span>  
*   <span data-ttu-id="965a3-155">[Устройства в любом месте (в коммерческой версии)][AppExperience] не используют Эмуляторы, но реальные устройства, которыми вы можете управлять удаленно.</span><span class="sxs-lookup"><span data-stu-id="965a3-155">[Device Anywhere (commercial)][AppExperience] does not use emulators but real devices which you are able to control remotely.</span></span>  <span data-ttu-id="965a3-156">Это очень полезно в том случае, если вам нужно воспроизвести проблему на конкретном устройстве и не удается просмотреть ошибку с помощью любого из параметров предыдущих руководств.</span><span class="sxs-lookup"><span data-stu-id="965a3-156">This is very useful in the event where you need to reproduce a problem on a specific device and are not able to see the bug using any of the options in the previous guides.</span></span>  

## <span data-ttu-id="965a3-157">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="965a3-157">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsEdgeHtmlEmulation]: /microsoft-edge/devtools-guide/emulation "DevTools (EdgeHTML) — эмуляция | Документы Microsoft"  

[Ie11DevToolsEmulation]: /previous-versions/windows/internet-explorer/ie-developer/samples/dn255001(v=vs.85) "Эмуляция браузеров, размеров экрана и точек доступа к GPS | Документы Microsoft"  

[MicrosoftDeveloperEdgeVms]: https://developer.microsoft.com/microsoft-edge/tools/vms "Скачать виртуальные машины"  

[AndroidStudioCreateManageVirtualDevices]: https://developer.android.com/tools/devices/managing-avds.html "Создание виртуальных устройств и управление ими | Разработчики Android"  
[AndroidStudioDownload]:  https://developer.android.com/sdk/installing/studio.html "Скачайте инструменты для Android Studio и SDK | Разработчики Android"  
[AndroidStudioRunAppsAndroidEmulator]: https://developer.android.com/tools/devices/emulator.html "Запуск приложений в эмуляторе Android | Разработчики Android"  

[AppExperience]: https://www.sigos.com/app-experience/ "Взаимодействие с приложениями"  
[AppleSimulatorHelp]: https://help.apple.com/simulator/mac/current "Справка по имитатору — текущая | Изображение"  
[BrowserStack]: https://www.browserstack.com/automate "BrowserStack"  
[MacAppStoreXcode]: https://itunes.apple.com/app/xcode/id497799835 "Xcode в магазине Mac App Store"  
[MDNResponsiveDesignMode]: https://developer.mozilla.org/docs/Tools/Responsive_Design_View "Режим конструктора | MDN"  
[MozillaFirefoxDownload]: https://www.mozilla.org/firefox/all/#product-android-beta "Скачивание браузера Firefox"  
[SauceLabs]: https://saucelabs.com "Работа со семинарами"  

> [!NOTE]
> <span data-ttu-id="965a3-171">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="965a3-171">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="965a3-172">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/device-mode/testing-other-browsers) и [Meggin Kearney][MegginKearney] \ (технический редактор \) и [Пол Bakaus][PaulBakaus] \ (веб-разработчик отвечает на Google | Инструменты, производительность, анимация, UX и т. д.</span><span class="sxs-lookup"><span data-stu-id="965a3-172">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/device-mode/testing-other-browsers) and is authored by [Meggin Kearney][MegginKearney] \(Tech Writer\) and [Paul Bakaus][PaulBakaus] \(Open Web Developer Advocate at Google | Tools, Performance, Animation, UX\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="965a3-174">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="965a3-174">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
[PaulBakaus]: https://developers.google.com/web/resources/contributors/pbakaus  
