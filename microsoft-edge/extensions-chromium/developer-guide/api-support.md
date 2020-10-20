---
description: Список поддерживаемых API-интерфейсов, которые следует использовать при сборке расширений Microsoft Edge.
title: Поддерживаемые API для расширений Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/14/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-Chromium, Разработка расширений, расширения браузера, надстройки, API расширения, разработчик, веб-разработка
ms.openlocfilehash: 868473393da6cefbf146fb7acd6c9816903bd253
ms.sourcegitcommit: af91bfc3e6d8afc51f0fbbc0fe392262f424225c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/19/2020
ms.locfileid: "11120396"
---
# Поддерживаемые API для расширений Microsoft Edge

В таблице ниже приведен список API-интерфейсов, которые можно использовать при создании расширений для браузера Microsoft Edge \ (Chromium \).

| API                                   | Описание                                            
|---------------------------------------|----------------------------------------------------------|
| [будильники](https://developer.chrome.com/extensions/alarms) | Код расписания, который будет периодически выполняться или заданный период в будущем. |
| [закладки](https://developer.chrome.com/extensions/bookmarks) | Создавать и упорядочивать закладки, а можно управлять ими. |
| [browserAction](https://developer.chrome.com/extensions/browserAction) | Использование действий браузера для размещения значков на панели инструментов в Microsoft Edge. Вы также можете использовать действия браузера для добавления всплывающих подсказок, значков или всплывающих окон. |
| [browsingData](https://developer.chrome.com/extensions/browsingData) | Удаление данных обзора из локального профиля пользователя. |
| [команды](https://developer.chrome.com/extensions/commands) | Добавление сочетаний клавиш, вызывающих действия в расширении. Например, действие для открытия браузера или отправки команды на расширение. |
| [contentSettings](https://developer.chrome.com/extensions/contentSettings) | Как правило, параметры содержимого позволяют настраивать поведение Microsoft EDGE на каждом сайте, а не глобально. Измените параметры, определяющие, могут ли веб-сайты использовать такие функции, как cookie, JavaScript и подключаемые модули. |
| [contextMenu](https://developer.chrome.com/extensions/contextMenus) | Добавить элементы в контекстное меню Microsoft Edge. Элементы меню могут применяться к различным объектам, таким как изображения, гиперссылки и страницы. |
| [файлах](https://developer.chrome.com/extensions/cookies) | Запрашивать и изменять файлы cookie и получать уведомления при их изменении. |
| [отладчика](https://developer.chrome.com/extensions/debugger) | Присоединение к одной или нескольким вкладкам для взаимодействия с сетью, отладки JavaScript, изменения модели DOM, изменения CSS и т. д. Используйте отладчик tabId для назначения вкладок с sendCommand и маршрутизации событий tabId из функций обратного вызова oneven. |
| [declarativeContent](https://developer.chrome.com/extensions/declarativeContent) | Выполнение действий в зависимости от содержимого страницы без необходимости разрешения на чтение содержимого страницы. |
| [declarativeNetRequest](https://developer.chrome.com/extensions/declarativeNetRequest) | Обеспечивает более подробную конфиденциальность, блокируя или изменяя сетевые запросы, задавая декларативные правила. Разрешите расширения изменить сетевые запросы, не перехватывая запрос и просматривая содержимое. |
| [desktopCapture](https://developer.chrome.com/extensions/desktopCapture) | Захват содержимого экрана, отдельных окон или вкладок. |
| [devtools.inspectedWindow](https://developer.chrome.com/extensions/devtools_inspectedWindow) | Общайтесь с проверенным окном. Например, можно получить идентификатор вкладки страниц, оценить код, повторно загрузить страницы или получить ресурсы на странице. |
| [devtools. Network](https://developer.chrome.com/extensions/devtools_network) | Получение сведений о сетевых запросах, отображаемых средствами разработчика на панели "сеть". |
| [devtools. Panels](https://developer.chrome.com/extensions/devtools.panels) | Интегрировать расширение в пользовательский интерфейс окна средств разработчика можно с помощью создания собственных панелей, доступа к существующим панелям или добавления боковых панелей. |
| [загрузки](https://developer.chrome.com/extensions/downloads) | Программный запуск, мониторинг, управление и поиск загрузок. |
| [Enterprise. hardwarePlatform](https://developer.chrome.com/extensions/enterprise.hardwarePlatform) | Получите изготовитель и модель аппаратной платформы, в которой работает браузер. Этот API доступен только для расширений, установленных корпоративной политикой. |
| [событиях](https://developer.chrome.com/extensions/events) | Распространенные типы, используемые API, которые инициируют события для уведомления о возникновении интересных событий. |
| [добавоч](https://developer.chrome.com/extensions/extension) | Любая страница расширения может использовать служебные программы этого API. Она включает в себя поддержку обмена сообщениями между расширениями и сценариями содержимого, описанными в разделе Передача сообщений. |
| [extensionTypes](https://developer.chrome.com/extensions/extensionTypes) | Содержат объявления типов для расширений Microsoft Edge. |
| [fontSettings](https://developer.chrome.com/extensions/fontSettings) | Управление параметрами шрифта в Microsoft Edge. |
| [журнал](https://developer.chrome.com/extensions/history) | Взаимодействие с записью просмотренных страниц в браузере. Вы можете добавлять, удалять или запрашивать URL-адреса в истории браузера. Сведения о том, как переопределить страницу журнала с помощью собственной версии, можно найти в разделе "переопределение страниц". |
| [i18n](https://developer.chrome.com/extensions/i18n) | Реализуйте международные приложения во всех приложениях и расширениях. |
| [С3](https://developer.chrome.com/extensions/idle) | Определение факта изменения состояния бездействия компьютера. |
| [оснастк](https://developer.chrome.com/extensions/management) | Управление списком установленных или запущенных расширений. Это полезно для расширений, которые переопределяют встроенную страницу новой вкладки. |
| [уведомления](https://developer.chrome.com/extensions/notifications) | Создание форматированных уведомлений с помощью шаблонов и их отображение в области уведомлений. |
| [omnibox](https://developer.chrome.com/extensions/omnibox) | Зарегистрируйте ключевые слова в адресной строке Microsoft EDGE, также называемой Omnibox. |
| [pageAction](https://developer.chrome.com/extensions/pageAction) | Добавьте значки на панель инструментов Microsoft Edge справа от адресной строки. Действия на странице — это действия, которые можно выполнить на текущей странице и которые не применимы ко всем страницам. При неактивном выполнении действия страницы отображаются серым цветом. |
| [pageCapture](https://developer.chrome.com/extensions/pageCapture) | Сохранение вкладок в виде файлов MHTML.|
| [правами](https://developer.chrome.com/extensions/permissions) | Извлеките объявленные, необязательные разрешения во время выполнения, а не на этапе установки. Этот API можно использовать для отображения необходимых и утвержденных разрешений для пользователей. |
| [выключение](https://developer.chrome.com/extensions/power) | Переопределение функций управления электропитанием системы. |
| [printerProvider](https://developer.chrome.com/extensions/printerProvider) | Используйте события, чтобы запрашивать принтеры, их возможности и отправлять задания печати. |
| [конфиденциальность](https://developer.chrome.com/extensions/privacy) | Элементы управления в Microsoft EDGE, которые влияют на конфиденциальность пользователя. Этот API зависит от `EdgeSetting` прототипа `types` для получения и задания конфигурации Microsoft Edge. |
| [посредник](https://developer.chrome.com/extensions/proxy) | Управление параметрами прокси-сервера в Microsoft Edge. Этот API зависит от `EdgeSetting` прототипа `types` API для получения и задания конфигурации прокси-сервера Microsoft Edge. |
| [язык](https://developer.chrome.com/extensions/runtime) | Получение фоновой страницы, возврат сведений о манифесте и прослушивание событий и реагирование на события в жизненном цикле приложения или расширения. Кроме того, можно преобразовать относительный путь URL-адреса в полный URL-адрес. |
| [упражнени](https://developer.chrome.com/extensions/sessions) | Запрашивать и восстанавливать вкладки и окна из сеанса просмотра. |
| [хранилище](https://developer.chrome.com/extensions/storage) | Храните, изменяйте и отслеживайте изменения, внесенные в пользовательские данные. |
| [System. Memory](https://developer.chrome.com/extensions/system_memory) | `system.memory`API. |
| [System. Storage](https://developer.chrome.com/extensions/system_storage) | Запрос сведений об устройствах хранения. Вы также можете получать уведомления о присоединении и отсоединении запоминающих устройств. |
| [tabCapture](https://developer.chrome.com/extensions/tabCapture) | Взаимодействие с потоками вкладок. |
| [закладок](https://developer.chrome.com/extensions/tabs) | Взаимодействие с системой вкладок браузера для создания, изменения и переупорядочивания вкладок. |
| [topSites](https://developer.chrome.com/extensions/topSites) | Получайте доступ к самым распространенным сайтам, которые также называют большинством посещенных сайтов, которые отображаются на странице Создать вкладку. Эти сайты не содержат сочетаний клавиш, настроенных пользователем. |
| [речь](https://developer.chrome.com/extensions/tts) | Воспроизводить синтезированный текст в речь (TTS). |
| [ttsEngine](https://developer.chrome.com/extensions/ttsEngine) | Реализация обработчика преобразования текста в речь (TTS) с помощью расширения. Расширения, регистрируемые для использования этого API, получают события, которые содержат utterances для обработки и другие параметры. Затем расширения могут использовать любые доступные веб-технологии для создания и вывода речевого ввода, а также отправлять события назад в вызывающую функцию для отчета о состоянии. |
| [лично](https://developer.chrome.com/extensions/types) | Объявления типов для Microsoft Edge. |
| [Навигация](https://developer.chrome.com/extensions/webNavigation) | Получать уведомления о состоянии запросов на переходы. |
| [WebRequest (запрос)](https://developer.chrome.com/extensions/webRequest) | Просмотрите и проанализируйте трафик. Перехват, блокирование и изменение запросов. |
| [windows](https://developer.chrome.com/extensions/windows) | Взаимодействие с окнами браузера для создания, изменения и упорядочения окон в браузере. |



## Неподдерживаемые API расширения

Microsoft EDGE не поддерживает следующие API расширений:

* `chrome.gcm`.
* `chrome.identity.getAccounts`.
* `chrome.identity.getAuthToken` -В качестве альтернативы вы можете использовать `launchWebAuthFlow` для получения маркера OAuth2 для проверки подлинности пользователей.
* `chrome.instanceID`.


## Дополнительные рекомендации для поддерживаемых API

* Пользователь должен войти в Microsoft EDGE, используя учетную запись MSA или Azure Active Directory для использования `chrome.identity.getProfileUserInfo` . Если пользователь вошел в Microsoft Edge с помощью локальной учетной записи Active Directory, API-интерфейс возвращает `null` для значений электронной почты и идентификаторов.

* Microsoft EDGE не поддерживает расширения, использующие платежи в Интернет-магазине Chrome, так как они используются `identity.getAuthtoken` для запроса маркеров для пользователей, которые вошли в систему. Эти маркеры отправляются в интерфейс API лицензирования на основе RESTFUL. 


<!-- links -->  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> [Здесь](https://developer.chrome.com/apps/external_extensions)будет найдена исходная страница.  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
