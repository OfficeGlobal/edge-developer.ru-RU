---
description: Эмуляция средств проверки подлинности и отладки WebAuthn в Microsoft Edge DevTools.
title: Эмуляция средств проверки подлинности и отладки WebAuthn в Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/22/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 6727e9aeea1a51689a80570a2f1c9df880a8c9db
ms.sourcegitcommit: 6e2b26d41a0aa56ac34e6edc7dddd852ddb415b1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/23/2020
ms.locfileid: "11134187"
---
# <span data-ttu-id="b92bf-104">Эмуляция средств проверки подлинности и отладки WebAuthn в Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="b92bf-104">Emulate authenticators and debug WebAuthn in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="b92bf-105">Вместо того чтобы выполнять отладку веб-проверки подлинности на веб-сайте или в приложении с помощью физических средств проверки подлинности, используйте средство **WebAuthn** в Microsoft Edge DevTools, чтобы создавать и взаимодействовать с программными средствами проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="b92bf-105">Instead of debugging Web Authentication in your website or app with physical authenticators, use the **WebAuthn** tool in Microsoft Edge DevTools to create and interact with software-based virtual authenticators.</span></span>  

## <span data-ttu-id="b92bf-106">Перед началом работы</span><span class="sxs-lookup"><span data-stu-id="b92bf-106">Before you begin</span></span>  

<span data-ttu-id="b92bf-107">Чтобы приступить к работе с веб-аутентификацией, нужно использовать [спецификацию API для веб-проверки подлинности][GithubW3cWebauthn].</span><span class="sxs-lookup"><span data-stu-id="b92bf-107">A great place to get started with Web Authentication is the [Web Authentication API specification][GithubW3cWebauthn].</span></span>  

## <span data-ttu-id="b92bf-108">Настройка средства WebAuthn</span><span class="sxs-lookup"><span data-stu-id="b92bf-108">Set up the WebAuthn tool</span></span>  

1.  <span data-ttu-id="b92bf-109">Перейдите на веб-страницу, использующую WebAuthn (например, на следующий демонстрационный сайт).</span><span class="sxs-lookup"><span data-stu-id="b92bf-109">Navigate to a webpage that uses WebAuthn, such as the following demo website.</span></span>  
    
    [<span data-ttu-id="b92bf-110">webauthndemo.appspot.com</span><span class="sxs-lookup"><span data-stu-id="b92bf-110">webauthndemo.appspot.com</span></span>][AppspotWebauthndemo]  
    
1.  <span data-ttu-id="b92bf-111">Войдите на веб-сайт.</span><span class="sxs-lookup"><span data-stu-id="b92bf-111">Sign into the website.</span></span>  
1.  <span data-ttu-id="b92bf-112">[Откройте DevTools][DevtoolsGuideChromiumOpen].</span><span class="sxs-lookup"><span data-stu-id="b92bf-112">[Open DevTools][DevtoolsGuideChromiumOpen].</span></span>  
1.  <span data-ttu-id="b92bf-113">Чтобы открыть средство **WebAuthn** , щелкните значок **Настройка и управление DevTools** \ ( `...` \) > **более средствам**  >  **webauthn**.</span><span class="sxs-lookup"><span data-stu-id="b92bf-113">To open the **WebAuthn** tool, choose the **Customize and control DevTools** \(`...`\) icon > **More tools** > **WebAuthn**.</span></span>  
    
    :::image type="complex" source="../media/webauthn-webauthn-tab.msft.png" alt-text="Средство WebAuthn" lightbox="../media/webauthn-webauthn-tab.msft.png":::
       <span data-ttu-id="b92bf-115">Средство **WebAuthn**</span><span class="sxs-lookup"><span data-stu-id="b92bf-115">**WebAuthn** tool</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b92bf-116">В средстве **WebAuthn** установите флажок **включить виртуальную среду проверки подлинности**.</span><span class="sxs-lookup"><span data-stu-id="b92bf-116">In the **WebAuthn** tool, choose the checkbox next to **Enable virtual authenticator environment**.</span></span>  
1.  <span data-ttu-id="b92bf-117">После включения нового средства **проверки подлинности** появится новый раздел с именем "Новая учетная запись".</span><span class="sxs-lookup"><span data-stu-id="b92bf-117">After it is enabled, a new section named **New authenticator** is displayed.</span></span>  
    
    :::image type="complex" source="../media/webauthn-enable-virtual-auth.msft.png" alt-text="Средство WebAuthn" lightbox="../media/webauthn-enable-virtual-auth.msft.png":::
        **<span data-ttu-id="b92bf-119">Включить виртуальную среду проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="b92bf-119">Enable virtual authenticator environment</span></span>**  
    :::image-end:::  
    
1.  <span data-ttu-id="b92bf-120">В разделе **новый элемент проверки подлинности** настройте следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="b92bf-120">In the **New authenticator** section, configure the following options.</span></span>  
    
    | <span data-ttu-id="b92bf-121">Параметр</span><span class="sxs-lookup"><span data-stu-id="b92bf-121">Option</span></span> | <span data-ttu-id="b92bf-122">Значение</span><span class="sxs-lookup"><span data-stu-id="b92bf-122">Value</span></span> | <span data-ttu-id="b92bf-123">Сведения</span><span class="sxs-lookup"><span data-stu-id="b92bf-123">Details</span></span> |  
    |:--- |:--- |:--- |  
    | `Protocol` | <span data-ttu-id="b92bf-124">[ctap2][FidoallianceSpecsV20Id20180227ClientToAuthenticatorProtocolHtml] или [u2f][FidoallianceSpecsU2fV12Ps20170411OverviewHtml]</span><span class="sxs-lookup"><span data-stu-id="b92bf-124">[ctap2][FidoallianceSpecsV20Id20180227ClientToAuthenticatorProtocolHtml] or [u2f][FidoallianceSpecsU2fV12Ps20170411OverviewHtml]</span></span> | <span data-ttu-id="b92bf-125">Протокол, используемый виртуальным средством проверки подлинности для кодирования и декодирования.</span><span class="sxs-lookup"><span data-stu-id="b92bf-125">The protocol the virtual authenticator uses for encoding and decoding</span></span> |  
    | `Transport` |   `usb`<span data-ttu-id="b92bf-126">, `nfc` , `ble` или</span><span class="sxs-lookup"><span data-stu-id="b92bf-126">, `nfc`, `ble`, or</span></span> `internal` | <span data-ttu-id="b92bf-127">Виртуальная аутентификация имитирует выбранный транспорт для связи с клиентами, чтобы получить утверждение для определенных учетных данных.</span><span class="sxs-lookup"><span data-stu-id="b92bf-127">The virtual authenticator simulates the selected transport for communicating with clients in order to obtain an assertion for a specific credential.</span></span>  <span data-ttu-id="b92bf-128">Дополнительные сведения можно найти в разделе " [перечисление транспорта для проверки подлинности][GithubW3cWebauthnEnumTransport] "</span><span class="sxs-lookup"><span data-stu-id="b92bf-128">For more information, navigate to [Authenticator Transport Enumeration][GithubW3cWebauthnEnumTransport]</span></span> |  
    |  `Supports resident keys` | <span data-ttu-id="b92bf-129">Включить \ (или выключить) с помощью флажка</span><span class="sxs-lookup"><span data-stu-id="b92bf-129">Turn on \(or off\) using the checkbox</span></span> | <span data-ttu-id="b92bf-130">Включите этот параметр, если веб-приложение основывается на резидентных ключах \ (также называемых учетными данными, обнаруживаемыми на стороне клиента).</span><span class="sxs-lookup"><span data-stu-id="b92bf-130">Turn on if your web app relies on resident keys \(also known as client-side discoverable credentials\).</span></span>  <span data-ttu-id="b92bf-131">Для получения дополнительных сведений перейдите к [перечислению требований к резидентному ключу][GithubW3cWebauthnEnumResidentkeyrequirement].</span><span class="sxs-lookup"><span data-stu-id="b92bf-131">For more information, navigate to [Resident Key Requirement Enumeration][GithubW3cWebauthnEnumResidentkeyrequirement].</span></span> |  
    | `Supports user verification` | <span data-ttu-id="b92bf-132">Включить \ (или выключить) с помощью флажка</span><span class="sxs-lookup"><span data-stu-id="b92bf-132">Turn on \(or off\) using the checkbox</span></span> | <span data-ttu-id="b92bf-133">Включите этот параметр, если веб-приложение опирается на локальную авторизацию с помощью жестов модальностей, таких как PIN-коды сенсорного ввода, ввод пароля или биометрическое распознавание.</span><span class="sxs-lookup"><span data-stu-id="b92bf-133">Turn on if your web app relies on local authorization using gesture modalities like touch plus pin code, password entry, or biometric recognition.</span></span>  <span data-ttu-id="b92bf-134">Дополнительные сведения можно найти в разделе [Проверка пользователей][GithubW3cWebauthnEnumUserverification]</span><span class="sxs-lookup"><span data-stu-id="b92bf-134">For more information, navigate to [User Verification][GithubW3cWebauthnEnumUserverification]</span></span> |  
    
1.  <span data-ttu-id="b92bf-135">Нажмите кнопку **Добавить** .</span><span class="sxs-lookup"><span data-stu-id="b92bf-135">Choose the **Add** button.</span></span>  
1.  <span data-ttu-id="b92bf-136">Откроется новый раздел созданного средства проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="b92bf-136">A new section of your newly created authenticator is displayed.</span></span>  
    
    :::image type="complex" source="../media/webauthn-authenticator.msft.png" alt-text="Средство WebAuthn" lightbox="../media/webauthn-authenticator.msft.png":::
       <span data-ttu-id="b92bf-138">Authenticator</span><span class="sxs-lookup"><span data-stu-id="b92bf-138">Authenticator</span></span>  
    :::image-end:::  
    
<span data-ttu-id="b92bf-139">Раздел **Authenticator** содержит таблицу **учетных данных** .</span><span class="sxs-lookup"><span data-stu-id="b92bf-139">The **Authenticator** section includes a **Credentials** table.</span></span>  <span data-ttu-id="b92bf-140">Таблица будет пустой, пока учетные данные не будут зарегистрированы для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="b92bf-140">The table is empty until a credential is registered to the authenticator.</span></span>  

:::image type="complex" source="../media/webauthn-no-cred.msft.png" alt-text="Средство WebAuthn" lightbox="../media/webauthn-no-cred.msft.png":::
   <span data-ttu-id="b92bf-142">Нет учетных данных</span><span class="sxs-lookup"><span data-stu-id="b92bf-142">No credentials</span></span>  
:::image-end:::  

## <span data-ttu-id="b92bf-143">Регистрация новых учетных данных</span><span class="sxs-lookup"><span data-stu-id="b92bf-143">Register a new credential</span></span>  

<span data-ttu-id="b92bf-144">Чтобы зарегистрировать новые учетные данные, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="b92bf-144">To register a new credential, complete the following steps.</span></span>  <span data-ttu-id="b92bf-145">Для получения дополнительных сведений о том, что делает [API для проверки подлинности][GithubW3cWebauthn] при регистрации новых учетных данных, перейдите на страницу [Создание новых учетных данных][GithubW3cWebauthnSctnCreatecredential].</span><span class="sxs-lookup"><span data-stu-id="b92bf-145">For more information about what the [Web Authentication API][GithubW3cWebauthn] is doing when registering a new credential, navigate to [Create a New Credential][GithubW3cWebauthnSctnCreatecredential].</span></span>  

1.  <span data-ttu-id="b92bf-146">На веб-сайте Demo выберите **зарегистрировать новые учетные данные**.</span><span class="sxs-lookup"><span data-stu-id="b92bf-146">On the demo website, choose **Register new credential**.</span></span>  
1.  <span data-ttu-id="b92bf-147">Новые учетные данные теперь добавляются в таблицу **учетных данных** в средстве WebAuthn.</span><span class="sxs-lookup"><span data-stu-id="b92bf-147">A new credential is now added to the **Credentials** table in the WebAuthn tool.</span></span>  
    
    :::image type="complex" source="../media/webauthn-view-cred.msft.png" alt-text="Средство WebAuthn" lightbox="../media/webauthn-view-cred.msft.png":::
       <span data-ttu-id="b92bf-149">Просмотр учетных данных</span><span class="sxs-lookup"><span data-stu-id="b92bf-149">View credentials</span></span>  
    :::image-end:::  
    
<span data-ttu-id="b92bf-150">На веб-сайте Demo нажмите кнопку **Проверка подлинности** .</span><span class="sxs-lookup"><span data-stu-id="b92bf-150">On the demo website, choose the **Authenticate** button.</span></span>  <span data-ttu-id="b92bf-151">Убедитесь, что [число знаков][GithubW3cWebauthnSctnSignCounter] в таблице **учетных** данных увеличено на 1, что помечает успешно выполненную операцию [authenticatorGetAssertion][GithubW3cWebauthnAuthenticatorgetassertion] .</span><span class="sxs-lookup"><span data-stu-id="b92bf-151">Verify that the [Sign Count][GithubW3cWebauthnSctnSignCounter] of the credential in the **Credentials** table increased by 1, which marks a successful [authenticatorGetAssertion][GithubW3cWebauthnAuthenticatorgetassertion] operation.</span></span>  

## <span data-ttu-id="b92bf-152">Экспорт и удаление учетных данных</span><span class="sxs-lookup"><span data-stu-id="b92bf-152">Export and remove credentials</span></span>  

<span data-ttu-id="b92bf-153">Чтобы экспортировать или удалить учетные данные, нажмите кнопку " **Экспорт** " или " **Удалить** ".</span><span class="sxs-lookup"><span data-stu-id="b92bf-153">To export or remove a credential, choose the **Export** or **Remove** button.</span></span>  

:::image type="complex" source="../media/webauthn-export-remove.msft.png" alt-text="Средство WebAuthn" lightbox="../media/webauthn-export-remove.msft.png":::
   <span data-ttu-id="b92bf-155">Экспорт и удаление учетных данных</span><span class="sxs-lookup"><span data-stu-id="b92bf-155">Export or remove a credential</span></span>  
:::image-end:::  

## <span data-ttu-id="b92bf-156">Переименование средства проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="b92bf-156">Rename an authenticator</span></span>  

<span data-ttu-id="b92bf-157">Чтобы переименовать средство проверки подлинности, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="b92bf-157">To rename an authenticator, complete the following steps.</span></span>  

1.  <span data-ttu-id="b92bf-158">Рядом с именем средства проверки подлинности нажмите кнопку " **изменить** ".</span><span class="sxs-lookup"><span data-stu-id="b92bf-158">Next to the authenticator name, choose the **Edit** button.</span></span>  
1.  <span data-ttu-id="b92bf-159">Измените имя и нажмите клавишу **Ввод** , чтобы сохранить изменения.</span><span class="sxs-lookup"><span data-stu-id="b92bf-159">Edit the name, then choose **Enter** to save the changes.</span></span>  

:::image type="complex" source="../media/webauthn-rename.msft.png" alt-text="Средство WebAuthn" lightbox="../media/webauthn-rename.msft.png":::
   <span data-ttu-id="b92bf-161">Переименование средства проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="b92bf-161">Rename an authenticator</span></span>  
:::image-end:::  

## <span data-ttu-id="b92bf-162">Установка активного средства проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="b92bf-162">Set the active authenticator</span></span>  

<span data-ttu-id="b92bf-163">Вновь созданный средство проверки подлинности активируется автоматически.</span><span class="sxs-lookup"><span data-stu-id="b92bf-163">A newly created authenticator is automatically activated.</span></span>  <span data-ttu-id="b92bf-164">Чтобы использовать другой виртуальный способ проверки подлинности, нажмите кнопку **активного** переключателя рядом с удостоверением средства проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="b92bf-164">To use another virtual authenticator, choose the **Active** radio button next to the authenticator.</span></span>  

> [!NOTE]
> <span data-ttu-id="b92bf-165">DevTools поддерживает только один активный виртуальный проверяющий элемент проверки подлинности в любой момент.</span><span class="sxs-lookup"><span data-stu-id="b92bf-165">DevTools supports only one active virtual authenticator at any point of time.</span></span>  <span data-ttu-id="b92bf-166">При удалении активного средства проверки подлинности не будет автоматически включена другая служба проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="b92bf-166">If you remove the active authenticator, another authenticator is not automatically activated.</span></span>  

:::image type="complex" source="../media/webauthn-set-active.msft.png" alt-text="Средство WebAuthn" lightbox="../media/webauthn-set-active.msft.png":::
   <span data-ttu-id="b92bf-168">Установка активного средства проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="b92bf-168">Set active authenticator</span></span>  
:::image-end:::  

## <span data-ttu-id="b92bf-169">Удаление виртуального средства проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="b92bf-169">Remove a virtual authenticator</span></span>  

<span data-ttu-id="b92bf-170">Чтобы удалить виртуальную проверку подлинности, рядом с пунктом проверки подлинности нажмите кнопку " **Удалить** ".</span><span class="sxs-lookup"><span data-stu-id="b92bf-170">To remove a virtual authenticator, next to the authenticator, choose the **Remove** button.</span></span>  

:::image type="complex" source="../media/webauthn-remove-authenticator.msft.png" alt-text="Средство WebAuthn" lightbox="../media/webauthn-remove-authenticator.msft.png":::
   <span data-ttu-id="b92bf-172">Удаление средства проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="b92bf-172">Remove authenticator</span></span>  
:::image-end:::  

## <span data-ttu-id="b92bf-173">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="b92bf-173">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumOpen]: ../open.md "Открыть Microsoft Edge DevTools | Документы Microsoft"  

[AppspotWebauthndemo]: https://webauthndemo.appspot.com "Демонстрация по Webauthn | Appspot"  

[FidoallianceSpecsV20Id20180227ClientToAuthenticatorProtocolHtml]: https://fidoalliance.org/specs/fido-v2.0-id-20180227/fido-client-to-authenticator-protocol-v2.0-id-20180227.html "Клиент для протокола проверки подлинности (CTAP) | Fido Alliance"  
[FidoallianceSpecsU2fV12Ps20170411OverviewHtml]: https://fidoalliance.org/specs/fido-u2f-v1.2-ps-20170411/fido-u2f-overview-v1.2-ps-20170411.html "Общие сведения о универсальном втором коэффициенте (U2F) | Fido Alliance"  

[GithubW3cWebauthn]: https://w3c.github.io/webauthn "Веб-проверка подлинности: API для доступа к учетным данным открытого ключа, уровень 2 | GitHub"  
[GithubW3cWebauthnAuthenticatorgetassertion]: https://w3c.github.io/webauthn#authenticatorgetassertion "Операция authenticatorGetAssertion — веб-проверка подлинности: API для доступа к учетным данным открытого ключа на уровне 2 | GitHub"  
[GithubW3cWebauthnEnumTransport]: https://w3c.github.io/webauthn#enum-transport "Перечисление транспорта для проверки подлинности (перечисление AuthenticatorTransport) — веб-проверка подлинности: API для доступа к учетным данным открытых ключей PNG"  
[GithubW3cWebauthnEnumResidentkeyrequirement]: https://w3c.github.io/webauthn#enum-residentKeyRequirement "Перечисление потребностей резидентного ключа (перечисление ResidentKeyRequirement) — веб-проверка подлинности: API для доступа к учетным данным открытого ключа уровня 2 | PNG"  
[GithubW3cWebauthnEnumUserverification]: https://w3c.github.io/webauthn#user-verification "Проверка пользователей — веб-проверка подлинности: API для доступа к учетным данным открытого ключа на уровне 2 | PNG"  
[GithubW3cWebauthnSctnCreatecredential]: https://w3c.github.io/webauthn#sctn-createCredential "Создание новых учетных данных-PublicKeyCredential [[создание]] (источник, параметры, sameOriginWithAncestors) — веб-проверка подлинности: API для доступа к учетным данным открытого ключа, уровень 2 | GitHub"  
[GithubW3cWebauthnSctnSignCounter]: https://w3c.github.io/webauthn/#sctn-sign-counter "Вопросы о счетчиках подписей — веб-аутентификация: API для доступа к учетным данным открытого ключа на уровне 2 | GitHub"  

> [!NOTE]
> <span data-ttu-id="b92bf-185">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b92bf-185">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="b92bf-186">Исходная страница [будет найдена, и](https://developers.google.com/web/tools/chrome-devtools/webauthn/index) ее можно создать с помощью [Jecelyn Yeen][JecelynYeen] \ (разработчик отвечает, Chrome DevTools \).</span><span class="sxs-lookup"><span data-stu-id="b92bf-186">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/webauthn/index) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="b92bf-188">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b92bf-188">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
