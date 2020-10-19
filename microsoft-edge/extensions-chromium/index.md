---
description: Обзор расширений Microsoft EDGE (Chromium), а также создание и публикация расширений браузера в целом.
title: Расширения Microsoft EDGE (Chromium)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/28/2020
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: EDGE, Разработка расширений, расширения браузера, надстройки, центр партнера, разработчик, расширения Chromium
ms.openlocfilehash: 85858fc7e1159db3175c3a67c3cfd5f6dfbb448f
ms.sourcegitcommit: 845a0d53a86bee3678f421adee26b3372cefce57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/08/2020
ms.locfileid: "11104702"
---
# Расширения Microsoft EDGE (Chromium) 

Расширение — это небольшая программа, которую вы (разработчик) может использовать для добавления новых функций в Microsoft Edge \ (Chromium \) или изменения существующих функциональных возможностей.  Расширение предназначено для повышения ежедневного обзора пользователей, предоставляя функции специализированные, важные для целевой аудитории.  

Вы можете создавать расширения, если ваша идея или продукт зависит от доступности определенного веб-браузера или дополнению браузера, в котором нужно предоставить вам функциональные возможности, которые расширяют существующие веб-сайты.  Примеры сопутствующих возможностей включают adblockers и диспетчеры паролей.  

Расширение структурировано так же, как обычное веб-приложение.  Как минимум, он содержит JSON-файл манифеста приложения, который содержит основные сведения о платформе, файл JavaScript для определения функциональных возможностей, а также HTML и CSS-файл, чтобы определить внешний вид пользовательского интерфейса \ (как требуется).  Для работы непосредственно с веб-браузером, например окном или вкладкой, необходимо отправить запросы API и часто ссылаться на веб-браузер по имени.  

:::image type="complex" source="./media/example-extension-screenshot.png" alt-text="Расширение Microsoft EDGE (Chromium)":::
  Расширение Microsoft Edge \ (Chromium \)  
:::image-end:::  

## Основные рекомендации  

Среди самых популярных браузеров, которые нужно собрать для включения Safari, Firefox, Chrome, Opera, Brave и Microsoft Edge.  Большие места для начала работы с руководствами по разработке расширений и исследованием документации — сайты, размещенные в организациях браузера.  Приведенная ниже таблица является неопределенной, пожалуйста, используйте ее в качестве полезной начальной точки.  

| веб-браузер | На основе Chromium? | Домашняя страница разработки расширения |  
|:--- |:--- |:--- |  
| Safari | Нет | [developer.apple.com/documentation/safariservices/safari_app_extensions][AppleDeveloperSafariservicesAppExtensions] |  
| Firefox | Нет | [developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions][MDNWebextensions] |  
| Хром | Да | [developer.chrome.com/extensions][ChromeDeveloperExtensions] |  
| Opera | Да | [dev.opera.com/extensions][OperaDevExtensions] |  
| Brave | Да | Использование [веб-магазина Chrome][GoogleChromeWebstoreCategoryExtensions] |  
| Новый Microsoft Edge | Да | [developer.microsoft.com/microsoft-edge/extensions][MicrosoftDeveloperEdgeExtensions] |  

> [!IMPORTANT]
> Многие учебники по сайтам используют API, зависящие от браузера, которые могут не совпадать с браузером, для которого вы разрабатываете.  В большинстве случаев расширение Chromium работает так же, как в разных браузерах Chromium, и API работают должным образом.  Только некоторые менее распространенные API могут быть строго специфичными для браузера.  Ссылки на учебники можно найти в [разделе Дополнительные сведения](#see-also).  

## Зачем Chromium?

Если вы хотите опубликовать расширение в максимально возможном количестве хранилищ расширений браузера, оно должно быть изменено для нескольких версий, чтобы обеспечить целевую работу и работать в каждой из различных сред браузера.  [Расширения Safari][AppleDeveloperSafariservicesAppExtensions], в отличие от других типов расширений, могут использовать как веб-, так и машинный код для связи с собственными машинными приложениями.  [Расширения Firefox][MDNWebextensions] совместно используются вместе с другими типами расширений, но есть и другие [отличия][ExtensionworkshopPorting] , которые следует учитывать.  Однако есть и другие хорошие новости; последние четыре браузера, описанные выше, позволяют использовать один и тот же пакет кода и свести к минимуму необходимость изменения и поддержки параллельных версий.  Это связано с тем, что браузеры основаны на [проекте с открытым исходным кодом Chromium][|::ref1::|Home].  

Создание расширения Chromium позволяет написать минимальный объем кода для максимального увеличения количества хранилищ расширений и, в конечном итоге, числа пользователей, которые смогут найти и получить расширение.  

В основном основное внимание уделяется Chromium расширениям.  

## Совместимость с браузерами и тестирование расширений  

Иногда четность API между браузерами Chromium не существует.  Например, в API идентификации и оплаты есть различия.  Чтобы обеспечить соответствие расширениям ожиданиям клиентов, просмотрите состояние API в официальной документации браузера, например [API Chrome][ChromeDeveloperExtensionsApiIndex], [API расширения, поддерживаемые в Opera][OperaDevExtensionsApis], и [расширение Chrome для порта в Microsoft (Chromium) Edge][ExtensionsChromiumDeveloperGuidePortChrome].  

В зависимости от необходимых API-интерфейсов эти отличия могут означать, что вы должны создать немного разные пакеты кода с небольшим отличием в коде для каждого магазина.  

Если вы разрабатываете расширение, вы можете неопубликованного его в браузере, чтобы протестировать его в разных средах перед отправкой расширения в магазины веб-браузера.  

## Публикация расширения в магазинах веб – браузеров  

Вы можете отправлять и искать расширения браузера в указанных ниже магазинах браузеров.  

*   [Надстройки браузера Firefox][MozillaAddonsFirefoxExtensions]  
*   [Веб-магазин Chrome][GoogleChromeWebstoreCategoryExtensions]  
*   [Надстройки для Opera][OperaAddonsExtensions]  
*   [Надстройки Microsoft Edge][MicrosoftEdgeAddonsCategoryExtensions]  

В некоторых магазинах вы можете загружать перечисленные расширения из других браузеров.  Загрузка из другого браузера может сэкономить время (разработчик) и удалить требование для отправки в другие магазины, если пользователи смогут переходить к существующим описаниям магазина в разных браузерах.  Тем не менее, доступ к веб-браузерам не обеспечивается с помощью разных хранилищ браузеров.  Чтобы убедиться в том, что пользователи смогут находить свое расширение в разных браузерах, вы должны сохранить вхождение в каждом из них в каждом хранилище расширений браузера.  

Расширение может иметь наложение аудиторий, часто использующих несколько браузеров, или может быть обнаружено, что оно должно быть нацелено на аудиторию.  Чтобы это произошло, существующие расширения Chromium могут быть перенесены из одного браузера в другой.  

### Перенос существующего расширения в Microsoft Edge  

Если вы уже разработали расширение для другого браузера Chromium и хотите предоставить его для работы в Microsoft EDGE, вам не придется переписывать расширение.  Миграция существующих расширений Chromium в другие браузеры Chromium очень проста, если используемые API доступны в разных браузерах или есть другие API, которые обеспечивают требуемую функциональность.  

Дополнительные сведения о переносе расширения Chrome можно найти в разделе [расширения Chrome для порта Microsoft (Chromium) Edge][ExtensionsChromiumDeveloperGuidePortChrome].  После того как вы наносите расширение для целевого браузера, следующий шаг — опубликовать.  

### Публикация на веб-сайте надстроек Microsoft Edge  

Чтобы приступить к публикации расширения в Microsoft EDGE, вы должны [зарегистрироваться для получения учетной записи для разработчика][MicrosoftDeveloperRegistration] с учетной записью электронной почты MSA \ (@outlook. com, @live. com и т. д.) для отправки списка расширений в магазине.  Если вы выберете адрес электронной почты, который нужно зарегистрировать, продумайте, нужно ли передавать или предоставлять доступ к этому расширению другим пользователям в вашей организации.  После завершения регистрации вы можете создать новую отправку расширения в магазине.  

Чтобы отправить свое расширение в магазин, необходимо соблюдать указанные ниже требования.  

*   Архив \ (ZIP-файл), содержащий файлы кода.  
*   Все необходимые визуальные ресурсы, в том числе логотип и мелкая рекламная плитка.  
*   Необязательные рекламные видеоматериалы, например снимки экрана, большие рекламные плитки, URL-адрес или любое сочетание с видеороликами вашего расширения.  
*   Сведения, описывающие расширение, например имя, краткое описание, полное описание и ссылка на политику конфиденциальности.  

> [!NOTE]
> В разных магазинах могут быть разные требования к отправке.  В приведенном выше списке перечислены [требования][ExtensionsChromiumPublish] для публикации расширения в Microsoft Edge.  

После того как вы завершите процесс отправки, вы просматриваете свое расширение и пройдете или завершите процесс сертификации.  Владельцы получают уведомление от результата, и при необходимости выполняются следующие действия.  Если вы отправили в магазин обновленное расширение, в том числе обновления сведений о расширении, запускается новый процесс проверки.  

## См. также  

*   [Перенос расширения Google Chrome][ExtensionworkshopPorting]  
*   [Создание расширения приложения Safari][AppleDeveloperSafariservicesAppExtensionsBuilding]  
*   [Свое первое расширение (Firefox)][MDNWebextensionsYourFirst]  
*   [Учебник &quot;Приступая к работе&quot; (Chrome)][ChromeDeveloperExtensionsGetstarted]  
*   [Приступая к работе (Opera)][OperaDevExtensionsGettingStarted]  
*   [Начало работы с расширениями Microsoft EDGE (Chromium)][ExtensionsChromiumGettingStartedIndex]  

<!-- image links -->  

<!-- links -->  

[ExtensionsChromiumDeveloperGuidePortChrome]: ./developer-guide/port-chrome-extension.md &quot;Расширение Chrome для порта в Microsoft (Chromium) Edge | Документы Microsoft&quot;  
[ExtensionsChromiumGettingStartedIndex]: ./getting-started/index.md &quot;Начало работы с расширениями Microsoft EDGE (Chromium) | Документы Microsoft&quot;  
[ExtensionsChromiumPublish]: ./publish/publish-extension.md &quot;Опубликовать расширение | Документы Microsoft&quot;  

[MicrosoftDeveloperEdgeExtensions]: https://developer.microsoft.com/microsoft-edge/extensions &quot;Разработка расширений для Microsoft Edge | Разработчик Майкрософт&quot;  
[MicrosoftDeveloperRegistration]: https://developer.microsoft.com/registration &quot;Центр партнеров | Разработчик Майкрософт&quot;  

[MicrosoftEdgeAddonsCategoryExtensions]: https://microsoftedge.microsoft.com/addons/category/Edge-Extensions &quot;Расширения Microsoft Edge | Microsoft Edge&quot;  

[AppleDeveloperSafariservicesAppExtensions]: https://developer.apple.com/documentation/safariservices/safari_app_extensions &quot;Расширения приложения Safari | Разработчик Apple&quot;  
[AppleDeveloperSafariservicesAppExtensionsBuilding]: https://developer.apple.com/documentation/safariservices/safari_app_extensions/building_a_safari_app_extension &quot;Создание расширения приложения Safari | Разработчик Apple&quot;  

[ChromeDeveloperExtensions]: https://developer.chrome.com/extensions &quot;Что такое расширения? | Разработчик Chrome&quot;  
[ChromeDeveloperExtensionsApiIndex]: https://developer.chrome.com/extensions/api_index &quot;Интерфейсы API Chrome | Разработчик Chrome&quot;  
[ChromeDeveloperExtensionsGetstarted]: https://developer.chrome.com/extensions/getstarted &quot;Учебник &quot;Приступая к работе&quot; | Разработчик Chrome&quot;  

[ChromiumHome]: https://www.chromium.org/Home &quot;Chromium&quot;  

[ExtensionworkshopPorting]: https://extensionworkshop.com/documentation/develop/porting-a-google-chrome-extension &quot;Перенос расширения Google Chrome | Семинар по добавочному номеру&quot;  

[GoogleChromeWebstoreCategoryExtensions]: https://chrome.google.com/webstore/category/extensions &quot;Расширения | Веб-магазин Chrome&quot;  

[MDNWebextensions]: https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions &quot;Расширения браузера | MDN&quot;  
[MDNWebextensionsYourFirst]: https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/Your_first_WebExtension &quot;Первое расширение | MDN&quot;  

[MozillaAddonsFirefoxExtensions]: https://addons.mozilla.org/firefox/extensions &quot;Расширения | Надстройки для Firefox&quot;  

[OperaAddonsExtensions]: https://addons.opera.com/extensions &quot;Расширения | Надстройки для Opera&quot;  

[OperaDevExtensions]: https://dev.opera.com/extensions &quot;Документация по расширениям | Dev. Opera&quot;  
[OperaDevExtensionsApis]: https://dev.opera.com/extensions/apis &quot;API расширения, поддерживаемые в Opera | Dev. Opera&quot;  
[OperaDevExtensionsGettingStarted]: https://dev.opera.com/extensions/getting-started &quot;Приступая к работе | Dev. Opera"  
