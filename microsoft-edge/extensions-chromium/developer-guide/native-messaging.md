---
description: Собственная документация для обмена сообщениями
title: Встроенные сообщения
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-Chromium, Разработка расширений, расширения браузера, надстройки, центр партнера, разработчик
ms.openlocfilehash: 9d33fc4e8c9449d539b6ea82cca87c3aad4d564e
ms.sourcegitcommit: 39636248d0266730089aa2e57b9cf04d9feb363d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/29/2020
ms.locfileid: "11088557"
---
# <span data-ttu-id="1e7cb-104">Встроенные сообщения</span><span class="sxs-lookup"><span data-stu-id="1e7cb-104">Native messaging</span></span>  

<span data-ttu-id="1e7cb-105">Расширения могут взаимодействовать с собственными приложениями Win32, установленными на устройстве пользователя с помощью API передачи сообщений.</span><span class="sxs-lookup"><span data-stu-id="1e7cb-105">Extensions can communicate with a native Win32 application installed on a user’s device using message passing APIs.</span></span> <span data-ttu-id="1e7cb-106">Собственный хост приложений может отправлять и получать сообщения с расширениями с помощью стандартных входных и стандартных выходных данных.</span><span class="sxs-lookup"><span data-stu-id="1e7cb-106">The native application host can send and receive messages with extensions using standard input and standard output.</span></span> <span data-ttu-id="1e7cb-107">Расширения с использованием встроенных сообщений устанавливаются в Microsoft EDGE, аналогично любому другому добавочному номеру.</span><span class="sxs-lookup"><span data-stu-id="1e7cb-107">Extensions using native messaging are installed in Microsoft Edge similar to any other extension.</span></span> <span data-ttu-id="1e7cb-108">Однако встроенные приложения не устанавливаются и не управляются Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="1e7cb-108">However, native applications are not installed or managed by Microsoft Edge.</span></span>

<span data-ttu-id="1e7cb-109">Чтобы получить расширение и собственный хост приложений, вы можете:</span><span class="sxs-lookup"><span data-stu-id="1e7cb-109">To acquire the extension and native application host, you can:</span></span>

1. <span data-ttu-id="1e7cb-110">Упакуйте расширение вместе с узлом.</span><span class="sxs-lookup"><span data-stu-id="1e7cb-110">Package the extension and the host together.</span></span> <span data-ttu-id="1e7cb-111">При установке пакета пользователи устанавливаются и расширение, и узел.</span><span class="sxs-lookup"><span data-stu-id="1e7cb-111">When users install the package, both the extension and the host are installed.</span></span>
1. <span data-ttu-id="1e7cb-112">Установите расширение из магазина для [надстроек Microsoft Edge][EdgeAddons]и запросите у пользователей свое расширение, чтобы установить узел.</span><span class="sxs-lookup"><span data-stu-id="1e7cb-112">Install the extension from the [Microsoft Edge Add-ons store][EdgeAddons], and have your extension prompt users to install the host.</span></span> 

<span data-ttu-id="1e7cb-113">Ознакомьтесь с приведенными ниже инструкциями, чтобы настроить расширение для отправки и получения сообщений с собственными хостами приложений.</span><span class="sxs-lookup"><span data-stu-id="1e7cb-113">Refer to the steps below to setup your extension to send and receive messages with native application hosts.</span></span>

### <span data-ttu-id="1e7cb-114">Действие 1: Добавление разрешений в манифест расширения</span><span class="sxs-lookup"><span data-stu-id="1e7cb-114">Step 1: Add permissions to the extension manifest</span></span>

<span data-ttu-id="1e7cb-115">Добавьте разрешение nativeMessaging к **manifest.jsу** расширения для файла.</span><span class="sxs-lookup"><span data-stu-id="1e7cb-115">Add the nativeMessaging permission to the extension’s **manifest.json** file.</span></span> <span data-ttu-id="1e7cb-116">Ниже приведен пример manifest.js:</span><span class="sxs-lookup"><span data-stu-id="1e7cb-116">Below is an example of manifest.json:</span></span>

```json
    {
          "name": "Native Messaging Example",
          "version": "1.0",
          "manifest_version": 2, 
          "description": "Send a message to a native application.",
          "app": { 
              "launch": { 
                  "local_path": "main.html" } 
                 }, 
          "icons": { 
              "128": "icon-128.png"}, 
          "permissions": ["nativeMessaging"] 
    }
```

### <span data-ttu-id="1e7cb-117">Действие 2: создание собственного файла манифеста узла сообщений</span><span class="sxs-lookup"><span data-stu-id="1e7cb-117">Step 2: Create your native messaging host manifest file</span></span>
    
<span data-ttu-id="1e7cb-118">Собственные приложения должны предоставлять собственный файл манифеста узла сообщений.</span><span class="sxs-lookup"><span data-stu-id="1e7cb-118">Native applications must provide a native messaging host manifest file.</span></span> <span data-ttu-id="1e7cb-119">Этот файл манифеста содержит путь к исполняемому объекту хоста сообщений, методу связи с расширением и списку допустимых расширений, с которыми он может взаимодействовать.</span><span class="sxs-lookup"><span data-stu-id="1e7cb-119">This manifest file contains the path to the native messaging host executable, the method of communication with the extension, and a list of allowed extensions it can communicate with.</span></span> <span data-ttu-id="1e7cb-120">Браузеры читают и проверяют собственный манифест узла сообщений, но не устанавливаются и не управляются браузером.</span><span class="sxs-lookup"><span data-stu-id="1e7cb-120">Browsers read and validate the native messaging host manifest, but it’s never installed or managed by the browser.</span></span> <span data-ttu-id="1e7cb-121">Файл манифеста узла должен представлять собой допустимый JSON-файл, содержащий указанные ниже поля.</span><span class="sxs-lookup"><span data-stu-id="1e7cb-121">The host manifest file must be a valid json file containing the following fields.</span></span>

    
```json
    {
        "name": "com.my_company.my_application",
        "description": "My Application",
        "path": "C:\\Program Files\\My Application\\chrome_native_messaging_host.exe",
        "type": "stdio",
        "allowed_origins": [
            "chrome-extension://knldjmfmopnpolahpmmgbagdohdnhkik/"
        ]
    }
```  




| <span data-ttu-id="1e7cb-122">Имя</span><span class="sxs-lookup"><span data-stu-id="1e7cb-122">Name</span></span> | <span data-ttu-id="1e7cb-123">Описание</span><span class="sxs-lookup"><span data-stu-id="1e7cb-123">Description</span></span> |  
|:--- |:--- |  
| `name` | <span data-ttu-id="1e7cb-124">Имя собственного узла сообщений.</span><span class="sxs-lookup"><span data-stu-id="1e7cb-124">Name of the native messaging host.</span></span> <span data-ttu-id="1e7cb-125">Клиенты передают эту строку `runtime.connectNative` или `runtime.sendNativeMessage` .</span><span class="sxs-lookup"><span data-stu-id="1e7cb-125">Clients pass this string to `runtime.connectNative` or `runtime.sendNativeMessage`.</span></span>  <span data-ttu-id="1e7cb-126">Это имя должно содержать только строчные буквы, цифры, знаки подчеркивания и точки.</span><span class="sxs-lookup"><span data-stu-id="1e7cb-126">This name must only contain lowercase alphanumeric characters, underscores, and dots.</span></span>  <span data-ttu-id="1e7cb-127">Имя не должно начинаться или заканчиваться точкой, а точка после нее не должна быть другой точкой.</span><span class="sxs-lookup"><span data-stu-id="1e7cb-127">The name must not start or end with a dot, and a dot must not be followed by another dot.</span></span> |  
| `description` | <span data-ttu-id="1e7cb-128">Краткое описание приложения.</span><span class="sxs-lookup"><span data-stu-id="1e7cb-128">Brief description of the application.</span></span> |  
| `path` | <span data-ttu-id="1e7cb-129">Путь к двоичному файлу хоста сообщений в машинном коде.</span><span class="sxs-lookup"><span data-stu-id="1e7cb-129">Path to the native messaging host binary.</span></span> <span data-ttu-id="1e7cb-130">На устройствах с Windows вы можете использовать относительные пути к каталогу, содержащему файл манифеста.</span><span class="sxs-lookup"><span data-stu-id="1e7cb-130">On Windows devices, you may use relative paths to the directory that contains the manifest file.</span></span> <span data-ttu-id="1e7cb-131">В macOS и Linux путь должен быть абсолютным.</span><span class="sxs-lookup"><span data-stu-id="1e7cb-131">On macOS and Linux, the path must be absolute.</span></span> <span data-ttu-id="1e7cb-132">Процесс хоста запустится с текущим набором каталогов и каталогом, содержащим двоичный файл узла.</span><span class="sxs-lookup"><span data-stu-id="1e7cb-132">The host process is started with the current directory set to the directory that contains the host binary.</span></span> <span data-ttu-id="1e7cb-133">Например, если для этого параметра задано значение `C:\Application\nm_host.exe` , двоичный код запускается с текущим каталогом `C:\Application\` .</span><span class="sxs-lookup"><span data-stu-id="1e7cb-133">For example, if this parameter is set to `C:\Application\nm_host.exe`, the binary is started using the current directory `C:\Application\`.</span></span> |  
| `type` | <span data-ttu-id="1e7cb-134">Тип интерфейса, используемого для связи с собственным узлом сообщений.</span><span class="sxs-lookup"><span data-stu-id="1e7cb-134">Type of the interface used to communicate with the native messaging host.</span></span>  <span data-ttu-id="1e7cb-135">В настоящее время для этого параметра существует только одно возможное значение: `stdio` .</span><span class="sxs-lookup"><span data-stu-id="1e7cb-135">Currently there's only one possible value for this parameter: `stdio`.</span></span>  <span data-ttu-id="1e7cb-136">Это значение указывает на то, что Microsoft Edge должен использовать `stdin` и `stdout` взаимодействовать с узлом.</span><span class="sxs-lookup"><span data-stu-id="1e7cb-136">This value indicates that Microsoft Edge should use `stdin` and `stdout` to communicate with the host.</span></span> |  
| `allowed_origins` |  <span data-ttu-id="1e7cb-137">Список расширений, которые могут иметь доступ к собственному узлу сообщений.</span><span class="sxs-lookup"><span data-stu-id="1e7cb-137">List of extensions that may have access to the native messaging host.</span></span>  <span data-ttu-id="1e7cb-138">Чтобы позволить приложению идентифицировать расширение и взаимодействовать с ним, установите `allowed_origins` для него значение `chrome-extension://[Microsoft-Catalog-extensionID]` в исходном файле манифеста узла сообщений.</span><span class="sxs-lookup"><span data-stu-id="1e7cb-138">To enable your application to identify and communicate with an extension, set `allowed_origins` to `chrome-extension://[Microsoft-Catalog-extensionID]` in your native messaging host manifest file.</span></span> |  


<span data-ttu-id="1e7cb-139">В процессе разработки вы можете неопубликованного расширение для проверки собственного обмена сообщениями с узлом, выполнив следующие действия:</span><span class="sxs-lookup"><span data-stu-id="1e7cb-139">While developing, you can sideload your extension to test native messaging with the host by:</span></span>
1. <span data-ttu-id="1e7cb-140">Перейдите к `edge://extensions` элементу, а затем включите выключатель режима разработчика.</span><span class="sxs-lookup"><span data-stu-id="1e7cb-140">Navigating to `edge://extensions`, and then turning on the Developer mode toggle button.</span></span> 
1. <span data-ttu-id="1e7cb-141">Выберите пункт Загрузить распакованные, а затем выберите пакет расширения в неопубликованного.</span><span class="sxs-lookup"><span data-stu-id="1e7cb-141">Choose Load unpacked, and then select your extension package to sideload.</span></span>  
1. <span data-ttu-id="1e7cb-142">Нажмите кнопку ОК.</span><span class="sxs-lookup"><span data-stu-id="1e7cb-142">Choose OK.</span></span>
1. <span data-ttu-id="1e7cb-143">Убедитесь, что `edge://extensions` теперь на странице указано расширение.</span><span class="sxs-lookup"><span data-stu-id="1e7cb-143">Verify the `edge://extensions` page now lists your extension.</span></span> 
1. <span data-ttu-id="1e7cb-144">Скопируйте ключ из идентификатора из списка расширений на странице.</span><span class="sxs-lookup"><span data-stu-id="1e7cb-144">Copy the key from ID from the extension listing on the page.</span></span>

<span data-ttu-id="1e7cb-145">Когда вы будете готовы распространить расширение для пользователей, опубликуйте расширение в магазине надстроек Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="1e7cb-145">When you're ready to distribute your extension to users, publish your extension to the Microsoft Edge add-ons store.</span></span> <span data-ttu-id="1e7cb-146">КОД расширения опубликованного расширения может отличаться от идентификатора, используемого при проведении неопубликованного расширения.</span><span class="sxs-lookup"><span data-stu-id="1e7cb-146">The extension ID of the published extension may be different to the ID used while sideloading your extension.</span></span> <span data-ttu-id="1e7cb-147">Если идентификатор изменился, обновите `allowed_origins` его в файле манифеста узла, УКАЗАВ идентификатор опубликованного расширения.</span><span class="sxs-lookup"><span data-stu-id="1e7cb-147">If the ID changed, update `allowed_origins` in the host manifest file with the ID of your published extension.</span></span> 



### <span data-ttu-id="1e7cb-148">Шаг 3: копирование собственного файла манифеста узла сообщений в систему</span><span class="sxs-lookup"><span data-stu-id="1e7cb-148">Step 3: Copy the native messaging host manifest file to your system</span></span>

<span data-ttu-id="1e7cb-149">На заключительном этапе выполняется копирование файла манифеста собственного узла сообщений на компьютер и проверка правильности его настройки.</span><span class="sxs-lookup"><span data-stu-id="1e7cb-149">The final step involves copying the native messaging host manifest file to your computer, and ensuring it’s configured correctly.</span></span> <span data-ttu-id="1e7cb-150">Выполните указанные ниже действия, чтобы убедиться в том, что собственный файл узла сообщений размещен в нужном расположении, так как он зависит от платформы.</span><span class="sxs-lookup"><span data-stu-id="1e7cb-150">Follow the steps below to ensure the native messaging host file is placed in the expected location because it varies by platform.</span></span>
    
<span data-ttu-id="1e7cb-151">**Windows**.</span><span class="sxs-lookup"><span data-stu-id="1e7cb-151">**Windows**.</span></span> <span data-ttu-id="1e7cb-152">Файл манифеста может находиться в любом месте файловой системы.</span><span class="sxs-lookup"><span data-stu-id="1e7cb-152">The manifest file may be located anywhere in the file system.</span></span> <span data-ttu-id="1e7cb-153">Установщик приложения должен создать раздел реестра и задать в качестве значения по умолчанию для него полный путь к файлу манифеста.</span><span class="sxs-lookup"><span data-stu-id="1e7cb-153">The application installer must create a registry key and set the default value of that key to the full path of the manifest file.</span></span> <span data-ttu-id="1e7cb-154">Ниже приведены примеры разделов реестра.</span><span class="sxs-lookup"><span data-stu-id="1e7cb-154">The following commands are examples of registry keys.</span></span>
    
`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application`  
    <span data-ttu-id="1e7cb-155">или</span><span class="sxs-lookup"><span data-stu-id="1e7cb-155">or</span></span>  
`HKEY_CURRENT_USER\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application`<span data-ttu-id="1e7cb-156">,</span><span class="sxs-lookup"><span data-stu-id="1e7cb-156">,</span></span>  
    
<span data-ttu-id="1e7cb-157">Выполните в командной строке следующую команду, чтобы добавить раздел реестра в папку с файлом манифеста.</span><span class="sxs-lookup"><span data-stu-id="1e7cb-157">Run the following command at a command prompt to add a registry key to the folder with the manifest file.</span></span>
    
```shell
REG ADD "HKCU\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application" /ve /t REG_SZ /d "C:\path\to\nmh-manifest.json" /f
```  
    
<span data-ttu-id="1e7cb-158">Кроме того, можно скопировать указанную ниже команду в REG-файл и выполнить его, чтобы добавить раздел реестра.</span><span class="sxs-lookup"><span data-stu-id="1e7cb-158">Alternatively, copy the following command to a .reg file and run it to add the registry key.</span></span> 
    
```shell
Windows Registry Editor Version 5.00
[HKEY_CURRENT_USER\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application]
@="C:\\path\\to\\nmh-manifest.json"
``` 

  <span data-ttu-id="1e7cb-159">Microsoft Edge сначала отправляет 32-разрядный реестр, а затем 64-разрядный реестр для идентификации машинных приложений для обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="1e7cb-159">Microsoft Edge queries the 32-bit registry first, and then the 64-bit registry to identify native messaging hosts.</span></span> <span data-ttu-id="1e7cb-160">Если вы запустите вышеприведенный reg-файл как часть пакетного сценария, убедитесь, что он запущен с помощью командной строки администратора.</span><span class="sxs-lookup"><span data-stu-id="1e7cb-160">If you run the above .reg file as part of a batch script, ensure you run it using an administrator command prompt.</span></span>


<span data-ttu-id="1e7cb-161">**macOS**.</span><span class="sxs-lookup"><span data-stu-id="1e7cb-161">**macOS**.</span></span> <span data-ttu-id="1e7cb-162">Файл манифеста должен храниться следующим образом:</span><span class="sxs-lookup"><span data-stu-id="1e7cb-162">The manifest file must be stored as follows:</span></span>

1. <span data-ttu-id="1e7cb-163">Встроенные системные приложения для обмена сообщениями, доступные всем пользователям, хранятся в определенном месте.</span><span class="sxs-lookup"><span data-stu-id="1e7cb-163">System-wide native messaging hosts, which are available to all users, are stored in a fixed location.</span></span> <span data-ttu-id="1e7cb-164">Например, файл манифеста должен храниться в</span><span class="sxs-lookup"><span data-stu-id="1e7cb-164">For example, the manifest file must be stored in</span></span> `/Library/Microsoft/Edge/NativeMessagingHosts/com.my_company.my_application.json`

1. <span data-ttu-id="1e7cb-165">Пользовательские машинные образы для обмена сообщениями, доступные только для текущего пользователя, находятся в подкаталоге NativeMessagingHosts в каталоге профиля пользователя.</span><span class="sxs-lookup"><span data-stu-id="1e7cb-165">User-specific native messaging hosts, which are available to the current user only, are located in the NativeMessagingHosts  subdirectory in the user profile directory.</span></span> <span data-ttu-id="1e7cb-166">Например, файл манифеста должен храниться в</span><span class="sxs-lookup"><span data-stu-id="1e7cb-166">For example, the manifest file must be stored in</span></span>  
    `~/Library/Application Support/Microsoft Edge <ChannelName>/NativeMessagingHosts/com.my_company.my_application.json`

    <span data-ttu-id="1e7cb-167">где `ChannelName` может быть Канарские, dev или Beta.</span><span class="sxs-lookup"><span data-stu-id="1e7cb-167">where `ChannelName` may be Canary, Dev, or Beta.</span></span> <span data-ttu-id="1e7cb-168">При использовании стабильного канала `ChannelName` не требуется.</span><span class="sxs-lookup"><span data-stu-id="1e7cb-168">When using the Stable channel, `ChannelName` isn't required.</span></span>


<span data-ttu-id="1e7cb-169">**Linux** Файл манифеста должен храниться следующим образом:</span><span class="sxs-lookup"><span data-stu-id="1e7cb-169">**Linux** The manifest file must be stored as follows:</span></span>

1. <span data-ttu-id="1e7cb-170">Встроенные системные узлы сообщений на уровне системы:  `~/.config/microsoft-edge/NativeMessagingHosts`</span><span class="sxs-lookup"><span data-stu-id="1e7cb-170">System-wide native messaging hosts:  `~/.config/microsoft-edge/NativeMessagingHosts`</span></span>

1. <span data-ttu-id="1e7cb-171">Специфические для пользователя машинные узлы сообщений:  `/etc/opt/edge/native-messaging-hosts`</span><span class="sxs-lookup"><span data-stu-id="1e7cb-171">User-specific native messaging hosts:  `/etc/opt/edge/native-messaging-hosts`</span></span>


> [!NOTE]
> <span data-ttu-id="1e7cb-172">Убедитесь в том, что у вас есть разрешения на чтение для файла манифеста и выполняются разрешения на исполняемый объект узла.</span><span class="sxs-lookup"><span data-stu-id="1e7cb-172">Ensure that you provide read permissions on the manifest file, and execute permissions on the host executable.</span></span>


> [!NOTE]
> <span data-ttu-id="1e7cb-173">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="1e7cb-173">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="1e7cb-174">[Здесь](https://developer.chrome.com/extensions/nativeMessaging)будет найдена исходная страница.</span><span class="sxs-lookup"><span data-stu-id="1e7cb-174">The original page is found [here](https://developer.chrome.com/extensions/nativeMessaging).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="1e7cb-176">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="1e7cb-176">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  


<!-- image links -->  

<!-- links -->  

[EdgeAddons]: https://microsoftedge.microsoft.com/addons/Microsoft-Edge-Extensions-Home "Надстройки Microsoft Edge"
[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
