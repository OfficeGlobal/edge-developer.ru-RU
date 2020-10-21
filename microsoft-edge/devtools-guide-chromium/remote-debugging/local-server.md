---
description: Разведите сайт на веб-сервере разработчика, а затем получите доступ к содержимому с устройства Android.
title: Доступ к локальным серверам
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: f994092460f090743119d7304bfe12aa28556b19
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125414"
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

# <span data-ttu-id="25987-104">Доступ к локальным серверам</span><span class="sxs-lookup"><span data-stu-id="25987-104">Access local servers</span></span>  

<span data-ttu-id="25987-105">Размещение сайта на веб-сервере разработчика, а затем доступ к содержимому с устройства Android.</span><span class="sxs-lookup"><span data-stu-id="25987-105">Host a site on a development machine web server, then access the content from an Android device.</span></span>  

<span data-ttu-id="25987-106">С помощью USB-кабеля и Microsoft Edge DevTools, запустите сайт с компьютера для разработки и просмотрите сайт на устройстве с Android.</span><span class="sxs-lookup"><span data-stu-id="25987-106">With a USB cable and Microsoft Edge DevTools, run a site from a development machine and then view the site on an Android device.</span></span>  

### <span data-ttu-id="25987-107">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="25987-107">Summary</span></span>  

*   <span data-ttu-id="25987-108">Переадресация портов позволяет просматривать контент, размещенный на вашем компьютере, на котором работает веб-сервер, на устройстве с Android.</span><span class="sxs-lookup"><span data-stu-id="25987-108">Port forwarding enables you to view content hosted by the web server running in your development machine on your Android device.</span></span>  
*   <span data-ttu-id="25987-109">Если веб-сервер использует настраиваемый домен, настройте на устройстве с Android доступ к контенту в этом домене с помощью собственного сопоставления доменов.</span><span class="sxs-lookup"><span data-stu-id="25987-109">If your web server is using a custom domain, set up your Android device to access the content at that domain with custom domain mapping.</span></span>  

## <span data-ttu-id="25987-110">Настройка переадресации портов</span><span class="sxs-lookup"><span data-stu-id="25987-110">Set up port forwarding</span></span>  

<span data-ttu-id="25987-111">Переадресация портов позволяет устройству Android получать доступ к содержимому, размещенному на веб-сервере, работающем на компьютере разработчика.</span><span class="sxs-lookup"><span data-stu-id="25987-111">Port forwarding enables your Android device to access content that is being hosted on the web server running in your development machine.</span></span>  <span data-ttu-id="25987-112">Переадресация порта работает путем создания прослушивающего порта TCP на устройстве с Android, которое сопоставляется с портом TCP на компьютере разработчика.</span><span class="sxs-lookup"><span data-stu-id="25987-112">Port forwarding works by creating a listening TCP port on your Android device that maps to a TCP port on your development machine.</span></span>  <span data-ttu-id="25987-113">Трафик между портами проходит через USB-соединение между устройством с Android и компьютером для разработки, поэтому подключение не зависит от конфигурации сети.</span><span class="sxs-lookup"><span data-stu-id="25987-113">Traffic between the ports travel through the USB connection between your Android device and development machine, so the connection does not depend on your network configuration.</span></span>  

<span data-ttu-id="25987-114">Чтобы включить перенаправление портов, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="25987-114">To enable port forwarding:</span></span>  

1.  <span data-ttu-id="25987-115">Настройка [удаленной отладки][RemoteDebuggingGettingStarted] между компьютером разработчика и устройством с Android.</span><span class="sxs-lookup"><span data-stu-id="25987-115">Set up [remote debugging][RemoteDebuggingGettingStarted] between your development machine and your Android device.</span></span>  <span data-ttu-id="25987-116">Когда вы закончите работу, вы увидите устройство с Android в левом меню диалогового окна **Проверка устройств** и индикатор состояния **подключен** .</span><span class="sxs-lookup"><span data-stu-id="25987-116">When you are finished, you should see your Android device in the left-hand menu of the **Inspect Devices** dialog and a **Connected** status indicator.</span></span>  
1.  <span data-ttu-id="25987-117">В диалоговом окне **Проверка устройств** в DevTools включите **переадресацию порта**.</span><span class="sxs-lookup"><span data-stu-id="25987-117">In the **Inspect Devices** dialog in DevTools, enable **Port forwarding**.</span></span>  
1.  <span data-ttu-id="25987-118">Нажмите кнопку **Добавить правило**.</span><span class="sxs-lookup"><span data-stu-id="25987-118">Choose **Add rule**.</span></span>  
    
    :::image type="complex" source="../media/remote-debugging-remote-devices-devices-port-forwarding-add-rule.msft.png" alt-text="Добавление правила переадресации портов" lightbox="../media/remote-debugging-remote-devices-devices-port-forwarding-add-rule.msft.png":::
       <span data-ttu-id="25987-120">Добавление правила переадресации портов</span><span class="sxs-lookup"><span data-stu-id="25987-120">Adding a port forwarding rule</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="25987-121">В поле " **порт устройства** " слева введите `localhost` номер порта, с которого вы хотите получить доступ к сайту на устройстве с Android.</span><span class="sxs-lookup"><span data-stu-id="25987-121">In the **Device port** textbox on the left, enter the `localhost` port number from which you want to be able to access the site on your Android device.</span></span>  <span data-ttu-id="25987-122">Например, если вы хотите получить доступ к сайту из `localhost:5000` ввода `5000` .</span><span class="sxs-lookup"><span data-stu-id="25987-122">For example, if you wanted to access the site from `localhost:5000` enter `5000`.</span></span>  
1.  <span data-ttu-id="25987-123">В текстовом поле " **локальный адрес** " щелкните правой кнопкой мыши IP-адрес или имя узла, на котором расположен сайт, который находится на компьютере разработчика, а затем укажите номер порта.</span><span class="sxs-lookup"><span data-stu-id="25987-123">In the **Local address** textbox on the right, enter the IP address or hostname on which your site is hosted on the web server running in your development machine, followed by the port number.</span></span>  <span data-ttu-id="25987-124">Например, если ваш веб-сайт запущен на `localhost:7331` входе `localhost:7331` .</span><span class="sxs-lookup"><span data-stu-id="25987-124">For example, if your site is running on `localhost:7331` enter `localhost:7331`.</span></span>  
1.  <span data-ttu-id="25987-125">Нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="25987-125">Choose **Add**.</span></span>  
    
<span data-ttu-id="25987-126">Переадресация порта теперь настроена.</span><span class="sxs-lookup"><span data-stu-id="25987-126">Port forwarding is now set up.</span></span>  <span data-ttu-id="25987-127">Просмотрите индикатор состояния для порта на вкладке на вашем устройстве в диалоговом окне **Проверка устройств** .</span><span class="sxs-lookup"><span data-stu-id="25987-127">See the status indicator for the port forward on the tab on your device within the **Inspect Devices** dialog.</span></span>  

:::image type="complex" source="../media/remote-debugging-remote-devices-devices-port-forwarding-5000-edge-user-agent.msft.png" alt-text="Добавление правила переадресации портов" lightbox="../media/remote-debugging-remote-devices-devices-port-forwarding-5000-edge-user-agent.msft.png":::
   <span data-ttu-id="25987-129">Состояние переадресации порта</span><span class="sxs-lookup"><span data-stu-id="25987-129">Port forwarding status</span></span>  
:::image-end:::  

<span data-ttu-id="25987-130">Чтобы просмотреть содержимое, откройте приложение Microsoft EDGE на устройстве с Android и перейдите к `localhost` порту, который вы указали в поле " **порт устройства** ".</span><span class="sxs-lookup"><span data-stu-id="25987-130">To view the content, open up Microsoft Edge on your Android device and go to the `localhost` port that you specified in the **Device port** field.</span></span>  <span data-ttu-id="25987-131">Например, если вы ввели `5000` поле, перейдите на страницу `localhost:5000` .</span><span class="sxs-lookup"><span data-stu-id="25987-131">For example, if you entered `5000` in the field, visit `localhost:5000`.</span></span>  

## <span data-ttu-id="25987-132">Сопоставление с пользовательскими локальными доменами</span><span class="sxs-lookup"><span data-stu-id="25987-132">Map to custom local domains</span></span>  

<span data-ttu-id="25987-133">С помощью настраиваемого сопоставления доменов вы можете просматривать содержимое на устройстве с Android с веб-сервера на компьютере разработчика, использующем настраиваемый домен.</span><span class="sxs-lookup"><span data-stu-id="25987-133">Custom domain mapping enables you to view content on an Android device from a web server on your development machine that is using a custom domain.</span></span>  

<span data-ttu-id="25987-134">Например, предположим, что ваш сайт использует библиотеку JavaScript стороннего поставщика, которая работает только в домене `microsoft-edge.devtools` .</span><span class="sxs-lookup"><span data-stu-id="25987-134">For example, suppose that your site uses a third-party JavaScript library that only works on the domain `microsoft-edge.devtools`.</span></span>  <span data-ttu-id="25987-135">Таким образом, вы создаете запись в `hosts` файле на компьютере разработчика, чтобы сопоставить этот домен с доменом `localhost` (например, `127.0.0.1 microsoft-edge.devtools` \).</span><span class="sxs-lookup"><span data-stu-id="25987-135">So, you create an entry in your `hosts` file on your development machine to map this domain to `localhost` \(for example, `127.0.0.1 microsoft-edge.devtools`\).</span></span>  <span data-ttu-id="25987-136">После настройки сопоставления домена и переадресации порта просмотрите сайт на своем устройстве с Android по URL-адресу `microsoft-edge.devtools` .</span><span class="sxs-lookup"><span data-stu-id="25987-136">After setting up custom domain mapping and port forwarding, view the site on your Android device at the URL `microsoft-edge.devtools`.</span></span>  

### <span data-ttu-id="25987-137">Настройка пересылки порта на прокси-сервер</span><span class="sxs-lookup"><span data-stu-id="25987-137">Set up port forwarding to proxy server</span></span>  

<span data-ttu-id="25987-138">Для сопоставления собственного домена необходимо запустить прокси-сервер на компьютере разработчика.</span><span class="sxs-lookup"><span data-stu-id="25987-138">To map a custom domain you must run a proxy server on your development machine.</span></span>  <span data-ttu-id="25987-139">Ниже приведены примеры прокси-серверов: [Чарльз][CharlesWebDebuggingProxy], [Squid][SquidOptimisingWebDelivery]и [Fiddler][FiddlerWebDebuggingProxy].</span><span class="sxs-lookup"><span data-stu-id="25987-139">Examples of proxy servers are [Charles][CharlesWebDebuggingProxy], [Squid][SquidOptimisingWebDelivery], and [Fiddler][FiddlerWebDebuggingProxy].</span></span>  

<span data-ttu-id="25987-140">Чтобы настроить перенаправление порта на прокси-сервер, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="25987-140">To set up port forwarding to a proxy:</span></span>  

1.  <span data-ttu-id="25987-141">Запустите прокси-сервер и запишите порт, который он использует.</span><span class="sxs-lookup"><span data-stu-id="25987-141">Run the proxy server and record the port that it is using.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="25987-142">Прокси-сервер и веб-сервер должны работать на разных портах.</span><span class="sxs-lookup"><span data-stu-id="25987-142">The proxy server and your web server must run on different ports.</span></span>  
    
1.  <span data-ttu-id="25987-143">Настройка [пересылки порта](#set-up-port-forwarding) на устройство с Android.</span><span class="sxs-lookup"><span data-stu-id="25987-143">Set up [port forwarding](#set-up-port-forwarding) to your Android device.</span></span>  <span data-ttu-id="25987-144">В поле **Local Address (локальный адрес** ) введите `localhost:` за ним порт, на котором работает прокси-сервер.</span><span class="sxs-lookup"><span data-stu-id="25987-144">For the **local address** field, enter `localhost:` followed by the port that your proxy server is running on.</span></span>  <span data-ttu-id="25987-145">Например, если он запущен на порте `8000` , перейдите к `localhost:8000` .</span><span class="sxs-lookup"><span data-stu-id="25987-145">For example, if it is running on port `8000`, navigate to `localhost:8000`.</span></span>  <span data-ttu-id="25987-146">В поле **порт устройства** введите номер, который будет прослушивать ваше устройство с Android, например `3333` .</span><span class="sxs-lookup"><span data-stu-id="25987-146">In the **device port** field enter the number that you want your Android device to listen on, such as `3333`.</span></span>  
    
### <span data-ttu-id="25987-147">Настройка параметров прокси-сервера на устройстве</span><span class="sxs-lookup"><span data-stu-id="25987-147">Configure proxy settings on your device</span></span>  

<span data-ttu-id="25987-148">Затем необходимо настроить устройство Android для взаимодействия с прокси-сервером.</span><span class="sxs-lookup"><span data-stu-id="25987-148">Next, you need to configure your Android device to communicate with the proxy server.</span></span>  

1.  <span data-ttu-id="25987-149">На устройстве с Android перейдите в раздел **Параметры**  >  **Wi-Fi**.</span><span class="sxs-lookup"><span data-stu-id="25987-149">On your Android device go to **Settings** > **Wi-Fi**.</span></span>  
1.  <span data-ttu-id="25987-150">Long-нажимайте имя сети, к которой вы подключены в данный момент.</span><span class="sxs-lookup"><span data-stu-id="25987-150">Long-press the name of the network to which you are currently connected.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="25987-151">Параметры прокси-сервера применяются к каждой сети.</span><span class="sxs-lookup"><span data-stu-id="25987-151">Proxy settings apply per network.</span></span>  
    
1.  <span data-ttu-id="25987-152">Выберите команду **изменить сеть**.</span><span class="sxs-lookup"><span data-stu-id="25987-152">Choose **Modify network**.</span></span>  
1.  <span data-ttu-id="25987-153">Нажмите кнопку **Дополнительные параметры**.</span><span class="sxs-lookup"><span data-stu-id="25987-153">Choose **Advanced options**.</span></span>  <span data-ttu-id="25987-154">Отображение параметров прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="25987-154">The proxy settings display.</span></span>  
1.  <span data-ttu-id="25987-155">Откройте меню **прокси** и выберите пункт **вручную**.</span><span class="sxs-lookup"><span data-stu-id="25987-155">Select the **Proxy** menu and choose **Manual**.</span></span>  
1.  <span data-ttu-id="25987-156">В поле **имя HostName прокси-сервера** введите `localhost` .</span><span class="sxs-lookup"><span data-stu-id="25987-156">For the **Proxy hostname** field, enter `localhost`.</span></span>  
1.  <span data-ttu-id="25987-157">В поле порт **прокси-сервера** введите номер порта, который вы ввели для **порта устройства** в предыдущем разделе.</span><span class="sxs-lookup"><span data-stu-id="25987-157">For the **Proxy port** field, enter the port number that you entered for **device port** in the previous section.</span></span>  
1.  <span data-ttu-id="25987-158">Нажмите кнопку **сохранить**.</span><span class="sxs-lookup"><span data-stu-id="25987-158">Choose **Save**.</span></span>  
    
<span data-ttu-id="25987-159">С помощью этих параметров устройство перенаправляет все свои запросы на прокси-сервер на компьютере разработчика.</span><span class="sxs-lookup"><span data-stu-id="25987-159">With these settings, your device forwards all of its requests to the proxy on your development machine.</span></span>  <span data-ttu-id="25987-160">Прокси-сервер создает запросы от имени вашего устройства, поэтому запросы к своему пользовательскому домену разрешаются надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="25987-160">The proxy makes requests on behalf of your device, so requests to your customized local domain are properly resolved.</span></span>  

<span data-ttu-id="25987-161">Теперь вы можете получать доступ к настраиваемым доменам на устройстве с Android так же, как и на компьютере разработчика.</span><span class="sxs-lookup"><span data-stu-id="25987-161">Now access custom domains on your Android device just like on the development machine.</span></span>  

<span data-ttu-id="25987-162">Если веб-сервер не работает с нестандартным портом, не забудьте указать порт при запросе содержимого с устройства с Android.</span><span class="sxs-lookup"><span data-stu-id="25987-162">If your web server is running off of a non-standard port, remember to specify the port when requesting the content from your Android device.</span></span>  <span data-ttu-id="25987-163">Например, если ваш веб-сервер использует собственный домен `microsoft-edge.devtools` для порта, то `7331` при просмотре сайта с устройства Android вы должны использовать URL-адрес `microsoft-edge.devtools:7331` .</span><span class="sxs-lookup"><span data-stu-id="25987-163">For example, if your web server is using the custom domain `microsoft-edge.devtools` on port `7331`, when you view the site from your Android device you should be using the URL `microsoft-edge.devtools:7331`.</span></span>  

> [!TIP]
> <span data-ttu-id="25987-164">Чтобы возобновить обычный просмотр, не забудьте вернуть параметры прокси-сервера на устройстве с Android после отключения от компьютера для разработки.</span><span class="sxs-lookup"><span data-stu-id="25987-164">To resume normal browsing, remember to revert the proxy settings on your Android device after you disconnect from the development machine.</span></span>  

## <span data-ttu-id="25987-165">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="25987-165">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[RemoteDebuggingGettingStarted]: ./index.md "Начало работы с удаленными отладочными устройствами Android | Документы Microsoft"  

[CharlesWebDebuggingProxy]: https://www.charlesproxy.com "Прокси-сервер отладчика Чарльз"  

[SquidOptimisingWebDelivery]: https://www.squid-cache.org "Squid: оптимизация веб-доставки"  

[FiddlerWebDebuggingProxy]: https://www.telerik.com/fiddler "Прокси-сервер для Fiddler без поддержки бесплатной отладки"  

> [!NOTE]
> <span data-ttu-id="25987-170">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="25987-170">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="25987-171">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/local-server) и [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \) и [Meggin Kearney][MegginKearney] \ (технический редактор \).</span><span class="sxs-lookup"><span data-stu-id="25987-171">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/local-server) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) and [Meggin Kearney][MegginKearney] \(Tech Writer\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="25987-173">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="25987-173">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
