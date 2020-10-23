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
# Эмуляция средств проверки подлинности и отладки WebAuthn в Microsoft Edge DevTools  

Вместо того чтобы выполнять отладку веб-проверки подлинности на веб-сайте или в приложении с помощью физических средств проверки подлинности, используйте средство **WebAuthn** в Microsoft Edge DevTools, чтобы создавать и взаимодействовать с программными средствами проверки подлинности.  

## Перед началом работы  

Чтобы приступить к работе с веб-аутентификацией, нужно использовать [спецификацию API для веб-проверки подлинности][GithubW3cWebauthn].  

## Настройка средства WebAuthn  

1.  Перейдите на веб-страницу, использующую WebAuthn (например, на следующий демонстрационный сайт).  
    
    [webauthndemo.appspot.com][AppspotWebauthndemo]  
    
1.  Войдите на веб-сайт.  
1.  [Откройте DevTools][DevtoolsGuideChromiumOpen].  
1.  Чтобы открыть средство **WebAuthn** , щелкните значок **Настройка и управление DevTools** \ ( `...` \) > **более средствам**  >  **webauthn**.  
    
    :::image type="complex" source="../media/webauthn-webauthn-tab.msft.png" alt-text="Средство WebAuthn" lightbox="../media/webauthn-webauthn-tab.msft.png":::
       Средство **WebAuthn**  
    :::image-end:::  
    
1.  В средстве **WebAuthn** установите флажок **включить виртуальную среду проверки подлинности**.  
1.  После включения нового средства **проверки подлинности** появится новый раздел с именем "Новая учетная запись".  
    
    :::image type="complex" source="../media/webauthn-enable-virtual-auth.msft.png" alt-text="Средство WebAuthn" lightbox="../media/webauthn-enable-virtual-auth.msft.png":::
        **Включить виртуальную среду проверки подлинности**  
    :::image-end:::  
    
1.  В разделе **новый элемент проверки подлинности** настройте следующие параметры.  
    
    | Параметр | Значение | Сведения |  
    |:--- |:--- |:--- |  
    | `Protocol` | [ctap2][FidoallianceSpecsV20Id20180227ClientToAuthenticatorProtocolHtml] или [u2f][FidoallianceSpecsU2fV12Ps20170411OverviewHtml] | Протокол, используемый виртуальным средством проверки подлинности для кодирования и декодирования. |  
    | `Transport` |   `usb`, `nfc` , `ble` или `internal` | Виртуальная аутентификация имитирует выбранный транспорт для связи с клиентами, чтобы получить утверждение для определенных учетных данных.  Дополнительные сведения можно найти в разделе " [перечисление транспорта для проверки подлинности][GithubW3cWebauthnEnumTransport] " |  
    |  `Supports resident keys` | Включить \ (или выключить) с помощью флажка | Включите этот параметр, если веб-приложение основывается на резидентных ключах \ (также называемых учетными данными, обнаруживаемыми на стороне клиента).  Для получения дополнительных сведений перейдите к [перечислению требований к резидентному ключу][GithubW3cWebauthnEnumResidentkeyrequirement]. |  
    | `Supports user verification` | Включить \ (или выключить) с помощью флажка | Включите этот параметр, если веб-приложение опирается на локальную авторизацию с помощью жестов модальностей, таких как PIN-коды сенсорного ввода, ввод пароля или биометрическое распознавание.  Дополнительные сведения можно найти в разделе [Проверка пользователей][GithubW3cWebauthnEnumUserverification] |  
    
1.  Нажмите кнопку **Добавить** .  
1.  Откроется новый раздел созданного средства проверки подлинности.  
    
    :::image type="complex" source="../media/webauthn-authenticator.msft.png" alt-text="Средство WebAuthn" lightbox="../media/webauthn-authenticator.msft.png":::
       Authenticator  
    :::image-end:::  
    
Раздел **Authenticator** содержит таблицу **учетных данных** .  Таблица будет пустой, пока учетные данные не будут зарегистрированы для проверки подлинности.  

:::image type="complex" source="../media/webauthn-no-cred.msft.png" alt-text="Средство WebAuthn" lightbox="../media/webauthn-no-cred.msft.png":::
   Нет учетных данных  
:::image-end:::  

## Регистрация новых учетных данных  

Чтобы зарегистрировать новые учетные данные, выполните указанные ниже действия.  Для получения дополнительных сведений о том, что делает [API для проверки подлинности][GithubW3cWebauthn] при регистрации новых учетных данных, перейдите на страницу [Создание новых учетных данных][GithubW3cWebauthnSctnCreatecredential].  

1.  На веб-сайте Demo выберите **зарегистрировать новые учетные данные**.  
1.  Новые учетные данные теперь добавляются в таблицу **учетных данных** в средстве WebAuthn.  
    
    :::image type="complex" source="../media/webauthn-view-cred.msft.png" alt-text="Средство WebAuthn" lightbox="../media/webauthn-view-cred.msft.png":::
       Просмотр учетных данных  
    :::image-end:::  
    
На веб-сайте Demo нажмите кнопку **Проверка подлинности** .  Убедитесь, что [число знаков][GithubW3cWebauthnSctnSignCounter] в таблице **учетных** данных увеличено на 1, что помечает успешно выполненную операцию [authenticatorGetAssertion][GithubW3cWebauthnAuthenticatorgetassertion] .  

## Экспорт и удаление учетных данных  

Чтобы экспортировать или удалить учетные данные, нажмите кнопку " **Экспорт** " или " **Удалить** ".  

:::image type="complex" source="../media/webauthn-export-remove.msft.png" alt-text="Средство WebAuthn" lightbox="../media/webauthn-export-remove.msft.png":::
   Экспорт и удаление учетных данных  
:::image-end:::  

## Переименование средства проверки подлинности  

Чтобы переименовать средство проверки подлинности, выполните указанные ниже действия.  

1.  Рядом с именем средства проверки подлинности нажмите кнопку " **изменить** ".  
1.  Измените имя и нажмите клавишу **Ввод** , чтобы сохранить изменения.  

:::image type="complex" source="../media/webauthn-rename.msft.png" alt-text="Средство WebAuthn" lightbox="../media/webauthn-rename.msft.png":::
   Переименование средства проверки подлинности  
:::image-end:::  

## Установка активного средства проверки подлинности  

Вновь созданный средство проверки подлинности активируется автоматически.  Чтобы использовать другой виртуальный способ проверки подлинности, нажмите кнопку **активного** переключателя рядом с удостоверением средства проверки подлинности.  

> [!NOTE]
> DevTools поддерживает только один активный виртуальный проверяющий элемент проверки подлинности в любой момент.  При удалении активного средства проверки подлинности не будет автоматически включена другая служба проверки подлинности.  

:::image type="complex" source="../media/webauthn-set-active.msft.png" alt-text="Средство WebAuthn" lightbox="../media/webauthn-set-active.msft.png":::
   Установка активного средства проверки подлинности  
:::image-end:::  

## Удаление виртуального средства проверки подлинности  

Чтобы удалить виртуальную проверку подлинности, рядом с пунктом проверки подлинности нажмите кнопку " **Удалить** ".  

:::image type="complex" source="../media/webauthn-remove-authenticator.msft.png" alt-text="Средство WebAuthn" lightbox="../media/webauthn-remove-authenticator.msft.png":::
   Удаление средства проверки подлинности  
:::image-end:::  

## Взаимодействие с командой средств разработчика Microsoft Edge  

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
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница [будет найдена, и](https://developers.google.com/web/tools/chrome-devtools/webauthn/index) ее можно создать с помощью [Jecelyn Yeen][JecelynYeen] \ (разработчик отвечает, Chrome DevTools \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
