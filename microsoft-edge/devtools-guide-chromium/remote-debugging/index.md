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

# Начало работы с удаленными отладкой устройств с Android  

Удаленная отладка динамического содержимого на устройстве Android с компьютера Windows или macOS.  На следующей странице учебника вы узнаете, как выполнять указанные ниже действия.  

*   Настройте устройство Android для удаленной отладки и найдите его на компьютере разработчика.  
*   Изучите и отлаживать динамический контент на устройстве с Android с компьютера для разработки.  
*   Содержимое ролика с устройства Android на экземпляр DevTools на компьютере разработчика.  

<!--  
:::image type="complex" source="../media/remote-debugging--remote-debugging.msft.png" alt-text="Remote Debugging lets you inspect a page running on an Android device from your development machine" lightbox="../media/remote-debugging--remote-debugging.msft.png":::
   old Figure 1.  Remote Debugging lets you inspect a page running on an Android device from your development machine  
:::image-end:::  
-->  

> [!NOTE]
> Удаленная отладка приложения Microsoft EDGE на устройствах с iOS в настоящее время не поддерживается.  Следующее руководство специально ориентировано на удаленную отладку Microsoft EDGE на устройствах с Android.
> Если у вас есть устройство macOS, следуйте инструкциям [по отладке Brightcove][BrightcoveSupportDebuggingMobileDevices] для удаленной отладки Microsoft EDGE на устройстве с iOS с помощью Safari.  Для получения дополнительных сведений о средстве веб-инспектора в Safari перейдите на [страницу веб-разработки Safari][AppleDeveloperSafariTools].  

## Шаг 1: обнаружение устройства с Android  

Рабочий процесс, описанный ниже, подходит для большинства пользователей.  Дополнительные сведения можно найти в разделе [Устранение неполадок: DevTools не удается найти раздел устройства Android](#troubleshooting-devtools-is-not-detecting-the-android-device) .  

1.  Откройте экран **Параметры разработчика** на устройстве с Android.  Дополнительные сведения можно найти в разделе [Настройка параметров разработчика на устройстве][AndroidDeveloperStudioDevOptions].  
1.  Выберите **включить отладку USB**.  
1.  На своем компьютере для разработки откройте Microsoft Edge.  
1.  Перейдите на `edge://inspect` страницу в Microsoft Edge.  
    
    :::image type="complex" source="../media/remote-debugging-edge-inspect-no-targets.msft.png" alt-text="Remote Debugging lets you inspect a page running on an Android device from your development machine" lightbox="../media/remote-debugging-edge-inspect-no-targets.msft.png":::
       Рисунок 1.  `edge://inspect`Страница в Microsoft Edge  
    :::image-end:::  
    
1.  Подключите устройство Android непосредственно к компьютеру разработчика с помощью USB-кабеля.  При первой попытке подключения на экран будет выведено сообщение о том, что DevTools обнаруживает неизвестное устройство.  Подтвердите запрос разрешения на **отладку USB** на устройстве с Android.  
    
    :::image type="complex" source="../media/remote-debugging-android-permissions-prompt.msft.png" alt-text="Remote Debugging lets you inspect a page running on an Android device from your development machine" lightbox="../media/remote-debugging-android-permissions-prompt.msft.png":::
       Рисунок 2.  Предупреждение о разрешении разрешения на **отладку USB** на устройстве с Android  
    :::image-end:::  
    
1.  Если вы видите название модели устройства с Android, Microsoft Edge успешно установил подключение к устройству.  Перейдите к разделу [этап 2](#step-2-debug-content-on-your-android-device-from-your-development-machine) .  
    
    <!--  
    :::image type="complex" source="../media/remote-debugging--unknown-device.msft.png" alt-text="Remote Debugging lets you inspect a page running on an Android device from your development machine" lightbox="../media/remote-debugging--unknown-device.msft.png":::
       old Figure 4.  The **Remote Devices** tab has successfully detected an unknown device that is pending authorization  
    :::image-end:::
    -->  
    
### Устранение неполадок: DevTools не может обнаружить устройство с Android  

Ниже приведены советы по устранению неполадок, связанных с правильными параметрами оборудования.  

*   Если вы используете USB-концентратор, попробуйте подключить устройство Android прямо к компьютеру разработчика.  
*   Попробуйте отключить кабель USB между устройством Android и компьютером разработчика, а затем снова подключить USB-кабель.  Выполнение задачи во время разблокировки экранов компьютера Android и разработки.  
*   Убедитесь, что USB-кабель работает.  Вы должны иметь возможность проверять файлы на устройстве с Android с компьютера, на котором ведется разработка.  

Чтобы убедиться, что программное обеспечение правильно настроено, воспользуйтесь приведенными ниже советами.  

*   Если на вашем компьютере разработчика установлена операционная система Windows, попробуйте установить драйверы USB для устройства с Android вручную.  Для получения дополнительных сведений перейдите к разделу [Установка драйверов USB для OEM][AndroidDeveloperToolsOemUsb].  
*   Некоторые комбинации устройств Windows и Android (особенно Samsung) требуют дополнительных настроек.  Дополнительные сведения можно найти в [разделе устройства DevTools, когда устройство подключено к сети][Stackoverflow21925992].  

Воспользуйтесь приведенными ниже советами, чтобы устранить проблему с отображением запроса на **отладку USB** на устройстве с Android.  

*   Отключение кабеля USB и повторное подключение к нему, когда DevTools на компьютере разработки и отображается начальный экран на устройстве с Android.  
    
    > [!NOTE]
    > Это сообщение появляется, если ваши экраны вашего компьютера Android или разработчика заблокированы.  

*   Обновление параметров отображения для устройства Android и компьютера для разработки таким образом, чтобы все они никогда не переходили в спящий режим.  
*   Установка режима USB для устройства с Android на PTP.  Для получения дополнительных сведений перейдите в [Galaxy S4 не показывает диалоговое окно "авторизация USB"][StackexchangeAndroid101933].  
*   Выберите **отозвать разрешения на отладку USB** на экране **Параметры разработчика** на устройстве с Android, чтобы сбросить его в новое состояние.  

Если вы нашли решение, которое не было упомянуто на этой странице, или на [DevTools устройствах не обнаружите устройства при подключении][Stackoverflow21925992] к переполнению стека, добавьте свое решение на вопрос о переполнении стека.<!--, or [open an issue in the webfundamentals repository][GitHubWebFundamentalsNewIssue]-->!  

## Шаг 2: Отладка содержимого на устройстве с Android с компьютера для разработки  

1.  Откройте Microsoft EDGE на устройстве с Android.  
1.  Перейдите к нужному `edge://inspect` названию модели устройства с Android, а затем выберите серийный номер устройства.  Ниже показано, как будет отображаться версия Microsoft EDGE, установленная на устройстве, с номером версии в круглых скобках.  Каждая открытая вкладка Microsoft Edge получает уникальный раздел.  Вы можете работать с этой вкладкой в разделе.  <!--If there are any apps using WebView, a section for each of those apps should be displayed, too.  --><!--In [**Figure 5**](#figure-5) there are no tabs or WebViews open.  -->  
    
    :::image type="complex" source="../media/remote-debugging-edge-inspect-with-targets.msft.png" alt-text="Remote Debugging lets you inspect a page running on an Android device from your development machine" lightbox="../media/remote-debugging-edge-inspect-with-targets.msft.png":::
       Рисунок 3.  Подключенное удаленное устройство  
    :::image-end:::  
    
1.  В текстовом поле **открыть вкладку с URL-адресом** введите URL-адрес и нажмите кнопку **Открыть**.  Страница откроется на новой вкладке на устройстве с Android.  
1.  Нажмите кнопку " **проверить** " рядом с URL-адресом, который вы только что открыли.  Откроется новый экземпляр DevTools.  

<!-- The version of Microsoft Edge running on your Android device determines the version of DevTools that opens on your development machine.  
    So, if your Android device is running a very old version of Microsoft Edge, the DevTools instance may look very different than what you are used to.   -->

### Дополнительные действия: перемещение фокуса, перезагрузка или закрытие вкладки  

Выберите **вкладку фокус**, **Перезагрузка**или **Закрыть** рядом с вкладкой, на которую вы хотите установить фокус, перезагрузить или закрыть.  

:::image type="complex" source="../media/remote-debugging-edge-inspect-with-targets-buttons.msft.png" alt-text="Remote Debugging lets you inspect a page running on an Android device from your development machine" lightbox="../media/remote-debugging-edge-inspect-with-targets-buttons.msft.png":::
   Рисунок 4.  Кнопки для фокусировки, повторной загрузки и закрытия вкладки  
:::image-end:::  

### Проверка элементов  

Перейдите на панель **элементы** экземпляра DevTools и наведите указатель мыши на элемент, чтобы выделить его в окне просмотра на устройстве с Android.  

Вы также можете выбрать элемент на экране устройства с Android, чтобы выбрать его на панели " **элементы** ".  В экземпляре DevTools нажмите кнопку **выбрать элемент** ![ , выберите элемент ][ImageSelectElementIcon] , а затем выберите элемент на экране устройства с Android.  

> [!NOTE]
> **Элемент "выбрать** " отключается после первого выбора, поэтому для использования этой функции необходимо повторно включить его.  

### Демонстрация экрана Android на компьютере разработчика  

Нажмите кнопку **вкл** ![ ][ImageToggleScreencastIcon] ., чтобы просмотреть содержимое устройства с Android в экземпляре DevTools, щелкнув значок Показать презентацию.  

Вы можете взаимодействовать с презентацией следующими способами.  

*   Нажатия клавиш переводятся в касания, и на устройстве обрабатывались соответствующие события сенсорного ввода.  
*   Нажатия клавиш на компьютере отправляются на устройство.  
*   Чтобы смоделировать жест сжатия, удерживайте `Shift` при перетаскивании.  
*   Для прокрутки используйте сенсорной панели, колесико мыши или смахивание с помощью указателя мыши.

> [!NOTE]
> Чтобы сделать презентацию более подсказками, воспользуйтесь приведенными ниже советами.  
> 
> *   В ролики отображается только содержимое страницы.  Прозрачные части презентации представляют интерфейсы устройства, такие как адресная строка Microsoft EDGE, строка состояния Android или клавиатура Android.  
> *   Ролики негативно влияют на частоту кадров.  Отключите экранную анимацию, изменяя прокрутки или анимации, чтобы получить более точную картину производительности страницы.  
> *   Если экран вашего устройства с Android блокируется, содержимое презентации исчезнет.  Разблокируйте экран устройства с Android для автоматического возобновления ролика.  

## Взаимодействие с командой средств разработчика Microsoft Edge  

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
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/index) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
