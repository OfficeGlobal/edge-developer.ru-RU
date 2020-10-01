---
description: Узнайте, как API запроса payment обрабатывает Microsoft Edge в качестве промежуточного средства между методами, потребителями и способами оплаты потребителей, которые хранятся в облаке.
title: API запросов о платежах — руководство по разработке
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/20/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: windows-integration
keywords: Edge, разработчики, html, css, javascript, разработчики
ms.openlocfilehash: 338940ab6f7e6bb04c6d5a8cc6ff0a198e7afbcc
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "10941850"
---
# API запросов платежей (набазу спектра HTML)  

> [!NOTE]
> В этой статье описан рабочий процесс, поддерживаемый в [предыдущей версии Microsoft Edge.][MicrosoftSupport44533505]  Microsoft Edge \(Chromium\) поддерживает API запросов о платеже с другими внедрением, используя другое внедрение в соответствии с проектом Chromium.  

Продажи электронной торговли продаж электронной почты продолжают увеличиваться на слухом птицах.  Согласно [eMarketer,](https://www.emarketer.com)2018 г. прогнозируются на 23 % от уровней, меры, мере которых в 2013 г.  Хотя потребители и предприятия мало отличаются от продаж электронного коммерческого выплат, проблемы остаются неизменными.  Сегодня каждый владелец веб-сайта электронной платеж должен тщательно разрабатывать потоки оплаты высокого качества оплаты и правила проверки.  Потребители должны перемещаться по различным потокам оформления оплаты и повторно ввести одинаковые сведения о доставке и выставлении на каждом сайте, где они происходят покупки.  Это может занимать много времени и недостатки для потребителей, приведущего к высоте корзины и уменьшенные продажи для медалей.  Оценок на [estimate](http://baymard.com/lists/cart-abandonment-rate) 60 % до 70 % корпоративных покупок отличаются.  

[API запроса оплаты стандартный API](https://w3.org/TR/payment-request) распроизвождается при оформлении оплаты.  Для этого интерфейс API требует менее настройки веб-разработчиков и более гибкий, четко и потребительский интерфейс для потребителей.  Поскольку потребители могут выбрать платежные и адреса для доставки из учетной записи Майкрософт, им необходимо ввести данные меньше, чтобы завершить покупки, чтобы завершить оплату.  

[API запросов платежей](https://w3.org/TR/payment-request) — это открытый aPI-браузера, который позволяет браузерам работать в качестве промежуточного материала, потребителей и методов оплаты \(например, кредитных карт\).  
  
В сводке при использовании [API запросов о платежах](https://w3.org/TR/payment-request)клиенты совершаются обычными веб-сайтами (как обычный).  Когда будет ее оплатить, aPI-сайта **Payment Request** вызывает API запроса оплаты и проверяет в браузере реквизиты платежа \(например поддерживаемые методы оплаты, сумма покупки, сумма, денежные единицы и т. д.) в браузере. **Payment Request**  

:::image type="complex" source="../media/payment_request_construct.png" alt-text="Конструктивная оплата запроса на оплату" lightbox="../media/payment_request_construct.png":::
   Конструктивная оплата запроса на оплату  
:::image-end:::  

Браузер проводит проверку подлинности пользователя, позволяет пользователю выбрать поддерживаемый способ оплаты для файла и обрабатывать платежные данные.  После этого браузер отправляет сведения об оплате на веб-сайт из готового платежа, чтобы производитель мог завершить платеж.  Кроме принятия сведений об оплате, профиль также может получить в запросе платежа, а также получать информацию о **доставке.**  

:::image type="complex" source="../media/payment_response_construct.png" alt-text="Конструктивная оплата запроса на оплату" lightbox="../media/payment_response_construct.png":::
   Построение ответа платежа  
:::image-end:::  

Чтобы просмотреть API запроса о платеже, а также получить обзор его использования, посмотрите видео.  

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Using-the-Payments-Request-API/player]  

> [!NOTE]
> API запросов платежей поддерживается в сборке Microsoft Edge 14992 или более поздней версии.  

## Создание запроса оплаты  

На веб-страницах создается запрос **платежа,** когда пользователь инициирует процесс оплаты, нажимая кнопку "купить".  **Конструктор запроса payment** [включает](/previous-versions/mt790440(v=vs.85)) в себя методы метода данных, подробности и параметры.  

```javascript
var payment = new PaymentRequest ( 
    methodData,  // required payment method data including payment method identifiers 
    details,     // required transaction information 
    options      // optional information like shipping or contact info to be returned 
); 
```  

Параметр [метода DataData](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) содержит список методов оплаты и сетей, принятых веб-сайтом, и любыми связанным методом оплаты.  В Microsoft Edge этот список соответствует поддерживаемым методам оплаты, которые сохранялись в учетной записи Майкрософт, и в результате он будет указан в пользовательском интерфейсе оплаты.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/pay_with.png" alt-text="Конструктивная оплата запроса на оплату" lightbox="../media/pay_with.png":::
         **Оплата со списком** в пользовательском интерфейсе "Бульты(Майкрософт)"  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      ```javascript
      var supportedInstruments = [{
          supportedMethods: ['basic-card'],
          data: {
              supportedNetworks: ['visa', 'mastercard', 'amex'],
              supportedTypes: ['credit'] 
          }         
      }]; 
      ```  
   :::column-end:::
:::row-end:::  

Параметр ["Сведения" содержит сведения](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) о том, что производитель предполагает клиенту о транзакции.  К ним относятся итоговые элементы заказа, такие как сумма, сумма поставки и другие сводные элементы уровня, влияют на сумму платежа.  Они не предназначены для заказа элементов строк.  
  
Параметр [сведений также](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) используется для определения параметров доставки, доступных клиенту при необходимости.  Дополнительные сведения можно получить в разделе **"Запрос** оплаты" ниже.  

Каждая [строка](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) подробных данных содержит название валюты и сумму.  

> [!NOTE]
> Запрос **оплаты не** вычисляет сумму или общий итог этих значений.  Это отвечает за веб-сайт издателя, чтобы правильно ее общее искомое портивное порядковый номер.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/show_details.png" alt-text="Конструктивная оплата запроса на оплату" lightbox="../media/show_details.png":::
         Промежуточный итог, отправка, налоги и общие сведения об итогах  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      ```javascript
      var details = {
          total: {
              label: 'Total (USD)',
              amount: {currency: 'USD', value: '193.98'}
          },
          displayItems: [{
                  label: 'Subtotal',
                  amount: {currency: 'USD', value: '174.99'}
              }, {
                  label: 'Taxes',
                  amount: {currency: "USD", value: '18.99'}
          }],
      };  
      ```  
   :::column-end:::
:::row-end:::  

[PaymentRequest](/previous-versions/mt790440(v=vs.85)) не поддерживает возврат средств, поэтому суммы должны всегда быть положительными. Элементы списка могут быть отрицательными, например скидки.  

В браузере метки отображаются по мере их определения и автоматически отображают правильное форматирование в виде денежных единиц с учетом языкового стандарта клиента.  Обратите внимание, что подписи должны обрабатываться на том же языке, что и в содержимом.  

Параметр [параметров](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) определяет данные, которые должны возвращаться из запроса **оплаты.**  Это также определяет данные, которые необходимо собрать, в том числе об отправке, адресе электронной почты, номер телефона или все необходимые данные.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/email_snippet.png" alt-text="Конструктивная оплата запроса на оплату" lightbox="../media/email_snippet.png":::
         Раскрывающееся меню "Адрес электронной почты"  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      ```javascript
      var options =
          {
              requestPayerEmail: true
          }; 
      ```  
   :::column-end:::
:::row-end:::  

## Отображение запроса оплаты  

[Метод отображения()](/previous-versions/mt790448(v=vs.85)) называется веб-страницей, чтобы пользователь мог взаимодействовать с пользовательским интерфейсом **"Запрос** платежа".  [Метод показать()](/previous-versions/mt790448(v=vs.85)) возвращает значение производительности, который будет решено, когда пользователь авторизует запрос платежа.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/pay_screen_default.png" alt-text="Конструктивная оплата запроса на оплату" lightbox="../media/pay_screen_default.png":::
         Подтвердите и оплатите сведения об оплате  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      ```javascript
      paymentRequest.show().then(paymentInstrumentResponse => {
          paymentInstrumentResponse.complete('success').then().catch(error => {
              handlePaymentRequestError(error); 
      });
      ```  
   :::column-end:::
:::row-end:::  

## Прибавление запроса о платежа  
 
[Метод абонента()](/previous-versions/mt790437(v=vs.85)) может вызываться веб-страницей в любой момент вызываемого методом [показать,](/previous-versions/mt790448(v=vs.85)) пока не сопоставить точку, в которой решается решение производительности.  [Метод отказа браузера приведет](/previous-versions/mt790437(v=vs.85)) к **Payment Request** извлечению запроса оплаты и закрытия пользовательского интерфейса **"Запрос** оплаты".  Например, веб-страница может быть абонентской, если пользователь не завершил транзакцию в течение нужного времени.  

```javascript
payment.abort();
```  

## Ответ на оплату  
Когда клиент утверждает запрос о **Payment Response** **платежа,** на веб-сайте возвращается ответ о платежном.  Ответ **платежа** включает следующие элементы:  

 Свойство      | Описание | Обязательный | Дополнительные сведения
|---------------|-----------------|-------|-----------------|
[methodName](/previous-versions/mt790656(v=vs.85)) | Идентификатор метода оплаты, выбранный пользователем | Y | |   
[details](/previous-versions/mt790655(v=vs.85)) | Объект JSON, включающий все данные, требующий обработки транзакции с помощью выбранного метода оплаты или маркера платежа | Y | [Basic Card](https://w3c.github.io/payment-method-basic-card) Словарь: cardHolderName; cardNumber; expiryMonth; expiryYear; cardSecurityCode; billingAddress; |   
[shippingAddress](/previous-versions/mt790445(v=vs.85)) | Адрес доставки, выбранный пользователем  |  Необязательно.  Требуется, если [запросShipping на звучит](/previous-versions/mt790440(v=vs.85)#PaymentOptions) `True`  | Словарь адреса: страна/регион; addressLine; регион; город; dependentLocality; postalCode; sortingCode; languageCode; организация; получатель; телефон |  
[shippingOption](/previous-versions/mt790446(v=vs.85)) | Идентификатор выбранной отправки | Необязательно.  Требуется, если [запросShipping на звучит](/previous-versions/mt790440(v=vs.85)#PaymentOptions) `True`  | |   
[payerName](/previous-versions/mt790440(v=vs.85)#PaymentOptions) | Имя, предоставленное пользователем  | Необязательно.  Требуется, если [запросpayerName:](/previous-versions/mt790440(v=vs.85)#PaymentOptions) `True` | |  
[payerEmail](/previous-versions/mt790440(v=vs.85)#PaymentOptions) | Адрес электронной почты, выбранный пользователем | Необязательно.  Требуется, если [запросPayerEmail](/previous-versions/mt790440(v=vs.85)#PaymentOptions) находится `True`  | |  
[PayerPhone](/previous-versions/mt790440(v=vs.85)#PaymentOptions) | Номер телефона, выбранный пользователем | Необязательно.  Требуется, если [запросPayerPhone является](/previous-versions/mt790440(v=vs.85)#PaymentOptions) `True` | |  

Объект [Details](/previous-versions/mt790655(v=vs.85)#PaymentRequest_params) JSON в **ответе на оплату** будет содержать данные об оплате, необходимые для обработки платежа.  Самый простой способ ответом представляет [Basic Card](https://w3c.github.io/payment-method-basic-card) собой базовую плату с четырьмя картой.  Если мероприятия маршруты упорядочивают свой обход процессоров с дополнительными партнерами шлюза или процессорами для предоставления поддержки платежей, возможно, ему потребуется пиграфическая загрузка процессора.  Они могут принимать форму маркера процессора или шлюза или зашифрованного платежного средства.  Эти методы оплаты выходят за рамки данного документа и перечисляются в документации по конкретному процессору.  Кроме того, для получения [базового](https://w3c.github.io/payment-method-basic-card) ответа на карточку в корпорацию Майкрософт не требуется дополнительная адаптация в корпорацию Майкрософт, в отличие от других способов оплаты или шлюза, которые могут потребовать ся шифрование ключей шифрования или запросить авторизацию \(oAuth\).  

После поступления ответа **на оплату веб-сайт**отправляет платежную информацию об оплате его процессором.  Во время обработки платежа в браузере отобразится страница счетчика.  

:::image type="complex" source="../media/loading_screen.png" alt-text="Конструктивная оплата запроса на оплату" lightbox="../media/loading_screen.png":::
   Страница, которая отображается при обработке платежа  
:::image-end:::  

После завершения оплаты веб-страница вызывает метод [полного ()](/previous-versions/mt790642(v=vs.85)) и отправляет значение успешного **или** **отработки.**  [Метод полного()](/previous-versions/mt790642(v=vs.85)) сообщает браузеромо о том, что покупка завершена, а также соответствующий экран завершения, который должен отображаться в зависимости от значения успешного **или** **сбоя.**  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/response_payment-request_complete.png" alt-text="Конструктивная оплата запроса на оплату" lightbox="../media/response_payment-request_complete.png":::
         Интерфейс, отображаемый при успешном приобретении  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/response_payment-request_failure.png" alt-text="Конструктивная оплата запроса на оплату" lightbox="../media/response_payment-request_failure.png":::
         Интерфейс, отображаемый при сбое покупки  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## Запрос о платежа с помощью отправки  

### Адрес доставки  

Для продаж, для которых требуется доставка физических товаров, требуется адрес доставки.  Чтобы включить адрес доставки, укажите `requestShipping = True` [параметры](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) запроса.  

Когда пользователь выбирает или обновляет адрес доставки, событие на экране запускается событие [onshippingaddresschange.](/previous-versions/mt790442(v=vs.85))  Веб-сайт, используя список событий, учитывайте об изменении, а затем сможет проверить адрес, пересчитывать затраты доставки и налоги по доставке, а также обновление [доставки,](/previous-versions/mt790440(v=vs.85)) чтобы отразить измененные затраты и доставки для выбранного адреса \(если применимо\).  

### Параметры отправки  

Параметры отправки клиенту можно представить, добавив к [параметру сведений параметр](/previous-versions/mt790440(v=vs.85)) доставки параметрдовать [доставку](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) параметра доставки.  Для этого можно задать один из вариантов `selected = True` отправки.  
 
Когда пользователь выбирает или обновляет параметры доставки, [событие onshippingoptionchangechange будет](/previous-versions/mt790436(v=vs.85)) выполняться.  Веб-сайт, использующий список событий, учитывается об изменении и смогут обновлять сведения о параметре доставки. [details](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params)  

```javascript
var details = {
    total: {
        label: 'Total (USD)',
        amount: {currency: 'USD', value: '193.98'}
    },
    displayItems: [{
         label: 'Subtotal',
         amount: {currency: 'USD', value: '174.99'}
        }, {
            label: 'Shipping',
            amount: {currency: 'USD', value: '0.00'}
        }, {
            label: 'Taxes',
            amount: {currency: "USD", '18.99'}
    }],
    shippingOptions: [{
        id: 'STANDARD',
        label: 'Standard – FREE (5-6 Business days)',
        amount: {currency: 'USD', value: '0.00'},
        selected: true
    }, {
        id: 'EXPEDITED',
        label: 'Two-Day Shipping',
        amount: {currency: 'USD', value: '7.00'}
    }]
};
        
var options = {
    requestShipping: true,
    requestPayerEmail: true
}; 
```  

## Справочник по API  

[API запроса оплаты](/previous-versions/mt790447(v=vs.85))  

## Спецификаци
[API запроса оплаты](https://w3.org/TR/payment-request)

<!-- links -->  

[DevtoolsGuideChromium]: /microsoft-edge/devtools-guide-chromium "Средства разработчика Microsoft Edge (на базе Chromium) | Документы Майкрософт"  

[MicrosoftSupport44533505]: https://support.microsoft.com/help/4533505 "Что такое устаревшая версия Microsoft Edge?"  
