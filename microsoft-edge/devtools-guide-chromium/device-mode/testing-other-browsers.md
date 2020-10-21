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

# Эмуляция и тестирование других браузеров  

Ваше задание не заканчивается, и вы не гарантируете, что ваш сайт будет работать в Microsoft EDGE и Android.  Несмотря на то, что режим устройства может имитировать ряд других устройств, таких как iPhone, мы рекомендуем вам извлечь решения для эмуляции, предоставляемой другими браузерами.  

### Краткий обзор  

*   Если вы не имеете определенного устройства или хотите проверит что-либо, лучше использовать эмуляцию устройства прямо в браузере.  
*   Эмуляторы устройств и симуляторы позволяют имитировать сайт разработки на различных устройствах с рабочей станции.  
*   Облачные Эмуляторы позволяют автоматизировать модульные тесты для сайта на разных платформах.  

## Эмуляторы браузеров  

Эмуляторы браузеров очень удобны для проверки скорости реагирования на сайт, но каждый из них не эмулирует различия в API, поддержку CSS и некоторые поведения, которые вы видите в браузере для мобильных устройств.  Протестируйте сайт в браузерах, работающих на реальных устройствах, чтобы убедиться в том, что все работает должным образом.  

### Режим разработки с откликом Firefox  

У Firefox есть [реагирующий на запросы режим разработки][MDNResponsiveDesignMode] , с помощью которого вы сможете остановиться на определенных устройствах, а вместо этого Изучите изменения структуры на распространенных размерах экрана или собственного размера, перетаскивая края.  

### Эмуляция EdgeHTML  

Для эмуляции телефонной системы Windows используйте [встроенную эмуляцию][DevToolsEdgeHtmlEmulation]Microsoft Edge \ (EdgeHTML \).  

[Эмуляция IE 11][Ie11DevToolsEmulation] используется для моделирования того, как страница может выглядеть в более ранних версиях Internet Explorer.  

## Эмуляторы устройств и симуляторы  

Симуляторы устройств и Эмуляторы моделируют не только среду браузера, но и все устройство.  Каждый из них полезен для тестирования возможностей, требующих интеграции с ОС, например входных данных формы с виртуальными клавиатурами.  

### Эмулятор Android  

<!--  
:::image type="complex" source="../media/device-mode-android-emulator-stock-browser.msft.png" alt-text="Stock Browser in Android Emulator" lightbox="../media/device-mode-android-emulator-stock-browser.msft.png":::
   Stock Browser in Android Emulator  
:::image-end:::  
-->  

В настоящее время невозможно установить Microsoft EDGE на эмуляторе Android.  Однако вы можете использовать браузер Android, оболочку содержимого Chromium и Firefox для Android, который мы рассмотрим позже в этом руководстве.  Chromium Content Shell запускает тот же механизм отрисовки Chromium, что и Microsoft EDGE, но не имеет каких бы то ни было специальных возможностей браузера.  

Эмулятор Android поставляется с пакетом SDK для Android, который необходимо загрузить в составе [Android Studio][AndroidStudioDownload].  Затем следуйте инструкциям по [настройке виртуального устройства][AndroidStudioCreateManageVirtualDevices] и [запуску эмулятора][AndroidStudioRunAppsAndroidEmulator].  
После загрузки эмулятора щелкните значок браузера и проверьте свой сайт в старом браузере акций для Android.  

#### Оболочка содержимого Chromium на Android  

<!--  
:::image type="complex" source="../media/device-mode-android-avd-contentshell.msft.png" alt-text="Stock Browser in Android Emulator" lightbox="../media/device-mode-android-avd-contentshell.msft.png":::
   Android Emulator Content Shell  
:::image-end:::  
-->  

Чтобы установить оболочку содержимого Chromium для Android, оставьте симулятор запущенным и выполните следующую команду:  

```shell
git clone https://github.com/PaulKinlan/chromium-android-installer.git
chmod u+x ./chromium-android-installer/*.sh
./chromium-android-installer/install-chromeandroid.sh
```  

Теперь вы можете протестировать сайт с помощью оболочки содержимого Chromium.  

#### Firefox для Android  

<!--  
:::image type="complex" source="../media/device-mode-ff-on-android-emulator.msft.png" alt-text="Stock Browser in Android Emulator" lightbox="../media/device-mode-ff-on-android-emulator.msft.png":::
   Firefox Icon on Android Emulator  
:::image-end:::  
-->  

Как и в оболочке содержимого Chromium, вы можете получить APK для установки Firefox на эмулятор.  

[Скачайте правильный файл. apk][MozillaFirefoxDownload].  

Чтобы установить файл на открытый эмулятор или подключенное устройство с Android, выполните следующую команду:  

```shell
adb install <path_to_APK>/fennec-XX.X.XX.android-arm.apk
```  

### Имитатор iOS  

Имитатор iOS для Mac OS X поставляется с Xcode, который [устанавливается из App Store][MacAppStoreXcode].  

Когда вы закончите работу, научитесь работать с имитатором с помощью [документации разработчика Apple][AppleSimulatorHelp].  

> [!NOTE]
> Чтобы не открывать Xcode каждый раз, когда вы хотите использовать имитатор iOS, откройте его, а затем щелкните правой кнопкой мыши значок имитатора iOS в Dock и выберите пункт **сохранить в Закреплениях**.  Теперь просто щелкаю этот значок, когда он вам нужен.  

###  Microsoft EDGE (EdgeHTML)  

:::image type="complex" source="../media/device-mode-modern-ie-vm.msft.png" alt-text="Stock Browser in Android Emulator" lightbox="../media/device-mode-modern-ie-vm.msft.png":::
   Современная виртуальная машина IE  
:::image-end:::  

Microsoft Edge \ (EdgeHTML \) виртуальные машины \ (VMS \) предоставляют доступ к разным версиям EdgeHTML и IE на компьютере с помощью VirtualBox \ (или VMWare).  Выберите [виртуальную машину на странице загрузки][MicrosoftDeveloperEdgeVms].  

## Эмуляторы и симуляторы на основе облака  

Если вы не можете использовать Эмуляторы и у вас нет доступа к реальным устройствам, Эмуляторы на основе облака являются следующим лучшим делом.  Большое преимущество облачных эмуляторов на реальных устройствах и местных эмуляторах состоит в том, что вы можете автоматизировать тестирование модулей для сайта на разных платформах.  

*   [BrowserStack (коммерческая версия)][|::ref1::|] — это самый простой способ использовать ручное тестирование.  Вы выбираете операционную систему, выбираете версию браузера и тип устройства, выбираете URL-адрес, который будет просматривать размещенную виртуальную машину, с которой вы можете взаимодействовать.  Вы также можете запускать несколько эмуляторов на одном экране, что позволяет тестировать внешний вид и функции приложения на нескольких устройствах одновременно.  
*   [SauceLabs (коммерческая версия)][SauceLabs] позволяет выполнять модульные тесты внутри эмулятора, который может быть весьма полезен для создания сценариев на сайте и просмотра видеозаписи после этого на различных устройствах.  Вы также можете выполнять тестирование на сайте вручную.  
*   [Устройства в любом месте (в коммерческой версии)][AppExperience] не используют Эмуляторы, но реальные устройства, которыми вы можете управлять удаленно.  Это очень полезно в том случае, если вам нужно воспроизвести проблему на конкретном устройстве и не удается просмотреть ошибку с помощью любого из параметров предыдущих руководств.  

## Взаимодействие с командой средств разработчика Microsoft Edge  

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
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/device-mode/testing-other-browsers) и [Meggin Kearney][MegginKearney] \ (технический редактор \) и [Пол Bakaus][PaulBakaus] \ (веб-разработчик отвечает на Google | Инструменты, производительность, анимация, UX и т. д.  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
[PaulBakaus]: https://developers.google.com/web/resources/contributors/pbakaus  
