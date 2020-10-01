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
# <span data-ttu-id="140c1-104">API запросов платежей (набазу спектра HTML)</span><span class="sxs-lookup"><span data-stu-id="140c1-104">Payment Request API (EdgeHTML)</span></span>  

> [!NOTE]
> <span data-ttu-id="140c1-105">В этой статье описан рабочий процесс, поддерживаемый в [предыдущей версии Microsoft Edge.][MicrosoftSupport44533505]</span><span class="sxs-lookup"><span data-stu-id="140c1-105">This article describes the workflow supported in the [legacy version of Microsoft Edge][MicrosoftSupport44533505].</span></span>  <span data-ttu-id="140c1-106">Microsoft Edge \(Chromium\) поддерживает API запросов о платеже с другими внедрением, используя другое внедрение в соответствии с проектом Chromium.</span><span class="sxs-lookup"><span data-stu-id="140c1-106">Microsoft Edge \(Chromium\) supports the Payment Request API with a different implementation based on the Chromium project.</span></span>  

<span data-ttu-id="140c1-107">Продажи электронной торговли продаж электронной почты продолжают увеличиваться на слухом птицах.</span><span class="sxs-lookup"><span data-stu-id="140c1-107">E-commerce sales continue growing at a rapid pace.</span></span>  <span data-ttu-id="140c1-108">Согласно [eMarketer,](https://www.emarketer.com)2018 г. прогнозируются на 23 % от уровней, меры, мере которых в 2013 г.</span><span class="sxs-lookup"><span data-stu-id="140c1-108">According to [eMarketer](https://www.emarketer.com), by 2018 digital sales are forecasted to increase by 23% from the levels measured in 2013.</span></span>  <span data-ttu-id="140c1-109">Хотя потребители и предприятия мало отличаются от продаж электронного коммерческого выплат, проблемы остаются неизменными.</span><span class="sxs-lookup"><span data-stu-id="140c1-109">While consumers and businesses enjoy the convenience of e-commerce sales, challenges remain.</span></span>  <span data-ttu-id="140c1-110">Сегодня каждый владелец веб-сайта электронной платеж должен тщательно разрабатывать потоки оплаты высокого качества оплаты и правила проверки.</span><span class="sxs-lookup"><span data-stu-id="140c1-110">Today each e-commerce website owner needs to invest time to develop high quality payment checkout flows and validation rules.</span></span>  <span data-ttu-id="140c1-111">Потребители должны перемещаться по различным потокам оформления оплаты и повторно ввести одинаковые сведения о доставке и выставлении на каждом сайте, где они происходят покупки.</span><span class="sxs-lookup"><span data-stu-id="140c1-111">Consumers need to navigate different payment checkout flows and re-enter the same payment and shipping information on every site where they shop.</span></span>  <span data-ttu-id="140c1-112">Это может занимать много времени и недостатки для потребителей, приведущего к высоте корзины и уменьшенные продажи для медалей.</span><span class="sxs-lookup"><span data-stu-id="140c1-112">This can be time consuming and frustrating for consumers, leading to a high rate of shopping cart abandonment and decreased sales for merchants.</span></span>  <span data-ttu-id="140c1-113">Оценок на [estimate](http://baymard.com/lists/cart-abandonment-rate) 60 % до 70 % корпоративных покупок отличаются.</span><span class="sxs-lookup"><span data-stu-id="140c1-113">Merchants [estimate](http://baymard.com/lists/cart-abandonment-rate) between 60% and 70% of shopping carts are abandoned.</span></span>  

<span data-ttu-id="140c1-114">[API запроса оплаты стандартный API](https://w3.org/TR/payment-request) распроизвождается при оформлении оплаты.</span><span class="sxs-lookup"><span data-stu-id="140c1-114">The [Payment Request API](https://w3.org/TR/payment-request) standardizes the payment checkout process.</span></span>  <span data-ttu-id="140c1-115">Для этого интерфейс API требует менее настройки веб-разработчиков и более гибкий, четко и потребительский интерфейс для потребителей.</span><span class="sxs-lookup"><span data-stu-id="140c1-115">This API requires less customization for web developers and provides a faster, more consistent, and therefore, less confusing experience for consumers.</span></span>  <span data-ttu-id="140c1-116">Поскольку потребители могут выбрать платежные и адреса для доставки из учетной записи Майкрософт, им необходимо ввести данные меньше, чтобы завершить покупки, чтобы завершить оплату.</span><span class="sxs-lookup"><span data-stu-id="140c1-116">Because consumers can select payment instruments and shipping addresses from their Microsoft account, they are required to enter less data to complete purchases which reduces the time and data entry required to complete a payment.</span></span>  

<span data-ttu-id="140c1-117">[API запросов платежей](https://w3.org/TR/payment-request) — это открытый aPI-браузера, который позволяет браузерам работать в качестве промежуточного материала, потребителей и методов оплаты \(например, кредитных карт\).</span><span class="sxs-lookup"><span data-stu-id="140c1-117">The [Payment Request API](https://w3.org/TR/payment-request) is an open, cross-browser standard that enables browsers to act as an intermediary between merchants, consumers, and the payment methods \(such as credit cards\) that consumers have stored in the cloud.</span></span>  
  
<span data-ttu-id="140c1-118">В сводке при использовании [API запросов о платежах](https://w3.org/TR/payment-request)клиенты совершаются обычными веб-сайтами (как обычный).</span><span class="sxs-lookup"><span data-stu-id="140c1-118">In summary, when using the [Payment Request API](https://w3.org/TR/payment-request), customers shop on merchant websites as normal.</span></span>  <span data-ttu-id="140c1-119">Когда будет ее оплатить, aPI-сайта **Payment Request** вызывает API запроса оплаты и проверяет в браузере реквизиты платежа \(например поддерживаемые методы оплаты, сумма покупки, сумма, денежные единицы и т. д.) в браузере. **Payment Request**</span><span class="sxs-lookup"><span data-stu-id="140c1-119">When ready to pay, the merchant website calls the **Payment Request** API to create a **Payment Request** and passes the relevant payment information \(such as supported payment methods, purchase amount, currency, and so on\) to the browser.</span></span>  

:::image type="complex" source="../media/payment_request_construct.png" alt-text="Конструктивная оплата запроса на оплату" lightbox="../media/payment_request_construct.png":::
   <span data-ttu-id="140c1-121">Конструктивная оплата запроса на оплату</span><span class="sxs-lookup"><span data-stu-id="140c1-121">Payment request construct</span></span>  
:::image-end:::  

<span data-ttu-id="140c1-122">Браузер проводит проверку подлинности пользователя, позволяет пользователю выбрать поддерживаемый способ оплаты для файла и обрабатывать платежные данные.</span><span class="sxs-lookup"><span data-stu-id="140c1-122">The browser authenticates the user, enables the user to select a supported payment method on file, and processes the payment details.</span></span>  <span data-ttu-id="140c1-123">После этого браузер отправляет сведения об оплате на веб-сайт из готового платежа, чтобы производитель мог завершить платеж.</span><span class="sxs-lookup"><span data-stu-id="140c1-123">The browser then sends the payment information details back to the merchant website, so that the merchant can complete the payment.</span></span>  <span data-ttu-id="140c1-124">Кроме принятия сведений об оплате, профиль также может получить в запросе платежа, а также получать информацию о **доставке.**</span><span class="sxs-lookup"><span data-stu-id="140c1-124">In addition to receiving payment information, the merchant can also elect to receive shipping information as part of the **Payment Request**.</span></span>  

:::image type="complex" source="../media/payment_response_construct.png" alt-text="Конструктивная оплата запроса на оплату" lightbox="../media/payment_response_construct.png":::
   <span data-ttu-id="140c1-126">Построение ответа платежа</span><span class="sxs-lookup"><span data-stu-id="140c1-126">Payment response construct</span></span>  
:::image-end:::  

<span data-ttu-id="140c1-127">Чтобы просмотреть API запроса о платеже, а также получить обзор его использования, посмотрите видео.</span><span class="sxs-lookup"><span data-stu-id="140c1-127">To see the Payment Request API in action, as well as get an overview of how to use it, check out this video.</span></span>  

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Using-the-Payments-Request-API/player]  

> [!NOTE]
> <span data-ttu-id="140c1-128">API запросов платежей поддерживается в сборке Microsoft Edge 14992 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="140c1-128">The Payment Request API is supported in Microsoft Edge build 14992 or newer.</span></span>  

## <span data-ttu-id="140c1-129">Создание запроса оплаты</span><span class="sxs-lookup"><span data-stu-id="140c1-129">Creating a Payment Request</span></span>  

<span data-ttu-id="140c1-130">На веб-страницах создается запрос **платежа,** когда пользователь инициирует процесс оплаты, нажимая кнопку "купить".</span><span class="sxs-lookup"><span data-stu-id="140c1-130">Web pages create a **Payment Request** typically when the user initiates a payment process by clicking a "buy" button.</span></span>  <span data-ttu-id="140c1-131">**Конструктор запроса payment** [включает](/previous-versions/mt790440(v=vs.85)) в себя методы метода данных, подробности и параметры.</span><span class="sxs-lookup"><span data-stu-id="140c1-131">The **Payment Request** [constructor](/previous-versions/mt790440(v=vs.85)) includes methodData, details, and options.</span></span>  

```javascript
var payment = new PaymentRequest ( 
    methodData,  // required payment method data including payment method identifiers 
    details,     // required transaction information 
    options      // optional information like shipping or contact info to be returned 
); 
```  

<span data-ttu-id="140c1-132">Параметр [метода DataData](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) содержит список методов оплаты и сетей, принятых веб-сайтом, и любыми связанным методом оплаты.</span><span class="sxs-lookup"><span data-stu-id="140c1-132">The [methodData](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) parameter contains a list of the payment methods and networks accepted by the website and any associated payment method specific data.</span></span>  <span data-ttu-id="140c1-133">В Microsoft Edge этот список соответствует поддерживаемым методам оплаты, которые сохранялись в учетной записи Майкрософт, и в результате он будет указан в пользовательском интерфейсе оплаты.</span><span class="sxs-lookup"><span data-stu-id="140c1-133">In Microsoft Edge, this list is matched with the supported payment methods that the shopper has saved in their Microsoft account and results in the "pay with" list in the payment user experience.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/pay_with.png" alt-text="Конструктивная оплата запроса на оплату" lightbox="../media/pay_with.png":::
         <span data-ttu-id="140c1-135">**Оплата со списком** в пользовательском интерфейсе "Бульты(Майкрософт)"</span><span class="sxs-lookup"><span data-stu-id="140c1-135">The **pay with** list in the Microsoft Wallet user experience</span></span>  
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

<span data-ttu-id="140c1-136">Параметр ["Сведения" содержит сведения](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) о том, что производитель предполагает клиенту о транзакции.</span><span class="sxs-lookup"><span data-stu-id="140c1-136">The [details](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) parameter contains information that the merchant wishes to convey to the customer about the transaction.</span></span>  <span data-ttu-id="140c1-137">К ним относятся итоговые элементы заказа, такие как сумма, сумма поставки и другие сводные элементы уровня, влияют на сумму платежа.</span><span class="sxs-lookup"><span data-stu-id="140c1-137">These include order summary items like total, tax, shipping amount, and other summary level items impacting the payment amount.</span></span>  <span data-ttu-id="140c1-138">Они не предназначены для заказа элементов строк.</span><span class="sxs-lookup"><span data-stu-id="140c1-138">These are not intended to be order line items.</span></span>  
  
<span data-ttu-id="140c1-139">Параметр [сведений также](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) используется для определения параметров доставки, доступных клиенту при необходимости.</span><span class="sxs-lookup"><span data-stu-id="140c1-139">The [details](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) parameter is also used to define shipping options available to the customer when required.</span></span>  <span data-ttu-id="140c1-140">Дополнительные сведения можно получить в разделе **"Запрос** оплаты" ниже.</span><span class="sxs-lookup"><span data-stu-id="140c1-140">More details are included in the **Payment Request** with Shipping section below.</span></span>  

<span data-ttu-id="140c1-141">Каждая [строка](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) подробных данных содержит название валюты и сумму.</span><span class="sxs-lookup"><span data-stu-id="140c1-141">Each [detail](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) line includes a label for the currency and the amount.</span></span>  

> [!NOTE]
> <span data-ttu-id="140c1-142">Запрос **оплаты не** вычисляет сумму или общий итог этих значений.</span><span class="sxs-lookup"><span data-stu-id="140c1-142">The **Payment Request** does not calculate the sum or total of these amounts.</span></span>  <span data-ttu-id="140c1-143">Это отвечает за веб-сайт издателя, чтобы правильно ее общее искомое портивное порядковый номер.</span><span class="sxs-lookup"><span data-stu-id="140c1-143">It is the responsibility of the merchant's website to ensure that the line items total correctly.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/show_details.png" alt-text="Конструктивная оплата запроса на оплату" lightbox="../media/show_details.png":::
         <span data-ttu-id="140c1-145">Промежуточный итог, отправка, налоги и общие сведения об итогах</span><span class="sxs-lookup"><span data-stu-id="140c1-145">Subtotal, shipping, taxes, and total details</span></span>  
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

<span data-ttu-id="140c1-146">[PaymentRequest](/previous-versions/mt790440(v=vs.85)) не поддерживает возврат средств, поэтому суммы должны всегда быть положительными. Элементы списка могут быть отрицательными, например скидки.</span><span class="sxs-lookup"><span data-stu-id="140c1-146">[PaymentRequest](/previous-versions/mt790440(v=vs.85)) does not support refunds, so the amounts should always be positive; individual list items can be negative, such as discounts.</span></span>  

<span data-ttu-id="140c1-147">В браузере метки отображаются по мере их определения и автоматически отображают правильное форматирование в виде денежных единиц с учетом языкового стандарта клиента.</span><span class="sxs-lookup"><span data-stu-id="140c1-147">The browser will render the labels as you define them and automatically render the correct currency formatting based on the customer's locale.</span></span>  <span data-ttu-id="140c1-148">Обратите внимание, что подписи должны обрабатываться на том же языке, что и в содержимом.</span><span class="sxs-lookup"><span data-stu-id="140c1-148">Note that the labels should be rendered in the same language as your content.</span></span>  

<span data-ttu-id="140c1-149">Параметр [параметров](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) определяет данные, которые должны возвращаться из запроса **оплаты.**</span><span class="sxs-lookup"><span data-stu-id="140c1-149">The [options](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) parameter defines data the web page wants returned from the **Payment Request**.</span></span>  <span data-ttu-id="140c1-150">Это также определяет данные, которые необходимо собрать, в том числе об отправке, адресе электронной почты, номер телефона или все необходимые данные.</span><span class="sxs-lookup"><span data-stu-id="140c1-150">This also defines the data that needs to be collected, including if shipping, email address, phone number or all are required.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/email_snippet.png" alt-text="Конструктивная оплата запроса на оплату" lightbox="../media/email_snippet.png":::
         <span data-ttu-id="140c1-152">Раскрывающееся меню "Адрес электронной почты"</span><span class="sxs-lookup"><span data-stu-id="140c1-152">Email address dropdown</span></span>  
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

## <span data-ttu-id="140c1-153">Отображение запроса оплаты</span><span class="sxs-lookup"><span data-stu-id="140c1-153">Showing the Payment Request</span></span>  

<span data-ttu-id="140c1-154">[Метод отображения()](/previous-versions/mt790448(v=vs.85)) называется веб-страницей, чтобы пользователь мог взаимодействовать с пользовательским интерфейсом **"Запрос** платежа".</span><span class="sxs-lookup"><span data-stu-id="140c1-154">The [show()](/previous-versions/mt790448(v=vs.85)) method is called by the web page to allow the user to interact with the **Payment Request** user interface.</span></span>  <span data-ttu-id="140c1-155">[Метод показать()](/previous-versions/mt790448(v=vs.85)) возвращает значение производительности, который будет решено, когда пользователь авторизует запрос платежа.</span><span class="sxs-lookup"><span data-stu-id="140c1-155">The [show()](/previous-versions/mt790448(v=vs.85)) method returns a Promise that will be resolved when the user authorizes the payment request.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/pay_screen_default.png" alt-text="Конструктивная оплата запроса на оплату" lightbox="../media/pay_screen_default.png":::
         <span data-ttu-id="140c1-157">Подтвердите и оплатите сведения об оплате</span><span class="sxs-lookup"><span data-stu-id="140c1-157">Confirm and pay details</span></span>  
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

## <span data-ttu-id="140c1-158">Прибавление запроса о платежа</span><span class="sxs-lookup"><span data-stu-id="140c1-158">Aborting a Payment Request</span></span>  
 
<span data-ttu-id="140c1-159">[Метод абонента()](/previous-versions/mt790437(v=vs.85)) может вызываться веб-страницей в любой момент вызываемого методом [показать,](/previous-versions/mt790448(v=vs.85)) пока не сопоставить точку, в которой решается решение производительности.</span><span class="sxs-lookup"><span data-stu-id="140c1-159">The [abort()](/previous-versions/mt790437(v=vs.85)) method can be called by the web page any time after the [show()](/previous-versions/mt790448(v=vs.85)) method is called, up until the point where the Promise is resolved.</span></span>  <span data-ttu-id="140c1-160">[Метод отказа браузера приведет](/previous-versions/mt790437(v=vs.85)) к **Payment Request** извлечению запроса оплаты и закрытия пользовательского интерфейса **"Запрос** оплаты".</span><span class="sxs-lookup"><span data-stu-id="140c1-160">The [abort()](/previous-versions/mt790437(v=vs.85)) method will cause the browser to abort the **Payment Request** and close the **Payment Request** user interface.</span></span>  <span data-ttu-id="140c1-161">Например, веб-страница может быть абонентской, если пользователь не завершил транзакцию в течение нужного времени.</span><span class="sxs-lookup"><span data-stu-id="140c1-161">For example, a web page may choose to abort if the user did not complete the transaction in the required amount of time.</span></span>  

```javascript
payment.abort();
```  

## <span data-ttu-id="140c1-162">Ответ на оплату</span><span class="sxs-lookup"><span data-stu-id="140c1-162">Payment Response</span></span>  
<span data-ttu-id="140c1-163">Когда клиент утверждает запрос о **Payment Response** **платежа,** на веб-сайте возвращается ответ о платежном.</span><span class="sxs-lookup"><span data-stu-id="140c1-163">When the customer approves the **Payment Request**, a **Payment Response** is returned to the website.</span></span>  <span data-ttu-id="140c1-164">Ответ **платежа** включает следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="140c1-164">The **Payment Response** includes the following:</span></span>  

 <span data-ttu-id="140c1-165">Свойство</span><span class="sxs-lookup"><span data-stu-id="140c1-165">Property</span></span>      | <span data-ttu-id="140c1-166">Описание</span><span class="sxs-lookup"><span data-stu-id="140c1-166">Description</span></span> | <span data-ttu-id="140c1-167">Обязательный</span><span class="sxs-lookup"><span data-stu-id="140c1-167">Required</span></span> | <span data-ttu-id="140c1-168">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="140c1-168">Additional Info</span></span>
|---------------|-----------------|-------|-----------------|
[<span data-ttu-id="140c1-169">methodName</span><span class="sxs-lookup"><span data-stu-id="140c1-169">methodName</span></span>](/previous-versions/mt790656(v=vs.85)) | <span data-ttu-id="140c1-170">Идентификатор метода оплаты, выбранный пользователем</span><span class="sxs-lookup"><span data-stu-id="140c1-170">The ID for the payment method selected by the user</span></span> | <span data-ttu-id="140c1-171">Y</span><span class="sxs-lookup"><span data-stu-id="140c1-171">Y</span></span> | |   
[<span data-ttu-id="140c1-172">details</span><span class="sxs-lookup"><span data-stu-id="140c1-172">details</span></span>](/previous-versions/mt790655(v=vs.85)) | <span data-ttu-id="140c1-173">Объект JSON, включающий все данные, требующий обработки транзакции с помощью выбранного метода оплаты или маркера платежа</span><span class="sxs-lookup"><span data-stu-id="140c1-173">A JSON object that includes all of the data the merchant requires to process the transaction using the selected payment method or a payment token</span></span> | <span data-ttu-id="140c1-174">Y</span><span class="sxs-lookup"><span data-stu-id="140c1-174">Y</span></span> | <span data-ttu-id="140c1-175">[Basic Card](https://w3c.github.io/payment-method-basic-card) Словарь: cardHolderName; cardNumber; expiryMonth; expiryYear; cardSecurityCode; billingAddress;</span><span class="sxs-lookup"><span data-stu-id="140c1-175">[Basic Card](https://w3c.github.io/payment-method-basic-card) Dictionary:  cardholderName; cardNumber; expiryMonth; expiryYear; cardSecurityCode; billingAddress;</span></span> |   
[<span data-ttu-id="140c1-176">shippingAddress</span><span class="sxs-lookup"><span data-stu-id="140c1-176">shippingAddress</span></span>](/previous-versions/mt790445(v=vs.85)) | <span data-ttu-id="140c1-177">Адрес доставки, выбранный пользователем</span><span class="sxs-lookup"><span data-stu-id="140c1-177">The shipping address selected by the user</span></span>  |  <span data-ttu-id="140c1-178">Необязательно.</span><span class="sxs-lookup"><span data-stu-id="140c1-178">Optional.</span></span>  <span data-ttu-id="140c1-179">Требуется, если [запросShipping на звучит](/previous-versions/mt790440(v=vs.85)#PaymentOptions)</span><span class="sxs-lookup"><span data-stu-id="140c1-179">Required when [requestShipping](/previous-versions/mt790440(v=vs.85)#PaymentOptions) is</span></span> `True`  | <span data-ttu-id="140c1-180">Словарь адреса: страна/регион; addressLine; регион; город; dependentLocality; postalCode; sortingCode; languageCode; организация; получатель; телефон</span><span class="sxs-lookup"><span data-stu-id="140c1-180">Address dictionary:  country; addressLine; region; city; dependentLocality; postalCode; sortingCode; languageCode; organization; recipient; phone</span></span> |  
[<span data-ttu-id="140c1-181">shippingOption</span><span class="sxs-lookup"><span data-stu-id="140c1-181">shippingOption</span></span>](/previous-versions/mt790446(v=vs.85)) | <span data-ttu-id="140c1-182">Идентификатор выбранной отправки</span><span class="sxs-lookup"><span data-stu-id="140c1-182">The ID for the selected shipping option</span></span> | <span data-ttu-id="140c1-183">Необязательно.</span><span class="sxs-lookup"><span data-stu-id="140c1-183">Optional.</span></span>  <span data-ttu-id="140c1-184">Требуется, если [запросShipping на звучит](/previous-versions/mt790440(v=vs.85)#PaymentOptions)</span><span class="sxs-lookup"><span data-stu-id="140c1-184">Required when [requestShipping](/previous-versions/mt790440(v=vs.85)#PaymentOptions) is</span></span> `True`  | |   
[<span data-ttu-id="140c1-185">payerName</span><span class="sxs-lookup"><span data-stu-id="140c1-185">payerName</span></span>](/previous-versions/mt790440(v=vs.85)#PaymentOptions) | <span data-ttu-id="140c1-186">Имя, предоставленное пользователем</span><span class="sxs-lookup"><span data-stu-id="140c1-186">The name provided by the user</span></span>  | <span data-ttu-id="140c1-187">Необязательно.</span><span class="sxs-lookup"><span data-stu-id="140c1-187">Optional.</span></span>  <span data-ttu-id="140c1-188">Требуется, если [запросpayerName:](/previous-versions/mt790440(v=vs.85)#PaymentOptions)</span><span class="sxs-lookup"><span data-stu-id="140c1-188">Required when [requestPayerName](/previous-versions/mt790440(v=vs.85)#PaymentOptions) is</span></span> `True` | |  
[<span data-ttu-id="140c1-189">payerEmail</span><span class="sxs-lookup"><span data-stu-id="140c1-189">payerEmail</span></span>](/previous-versions/mt790440(v=vs.85)#PaymentOptions) | <span data-ttu-id="140c1-190">Адрес электронной почты, выбранный пользователем</span><span class="sxs-lookup"><span data-stu-id="140c1-190">The email address selected by the user</span></span> | <span data-ttu-id="140c1-191">Необязательно.</span><span class="sxs-lookup"><span data-stu-id="140c1-191">Optional.</span></span>  <span data-ttu-id="140c1-192">Требуется, если [запросPayerEmail](/previous-versions/mt790440(v=vs.85)#PaymentOptions) находится</span><span class="sxs-lookup"><span data-stu-id="140c1-192">Required when [requestPayerEmail](/previous-versions/mt790440(v=vs.85)#PaymentOptions) is</span></span> `True`  | |  
[<span data-ttu-id="140c1-193">PayerPhone</span><span class="sxs-lookup"><span data-stu-id="140c1-193">PayerPhone</span></span>](/previous-versions/mt790440(v=vs.85)#PaymentOptions) | <span data-ttu-id="140c1-194">Номер телефона, выбранный пользователем</span><span class="sxs-lookup"><span data-stu-id="140c1-194">The phone number selected by the user</span></span> | <span data-ttu-id="140c1-195">Необязательно.</span><span class="sxs-lookup"><span data-stu-id="140c1-195">Optional.</span></span>  <span data-ttu-id="140c1-196">Требуется, если [запросPayerPhone является](/previous-versions/mt790440(v=vs.85)#PaymentOptions)</span><span class="sxs-lookup"><span data-stu-id="140c1-196">Required when [requestPayerPhone](/previous-versions/mt790440(v=vs.85)#PaymentOptions) is</span></span> `True` | |  

<span data-ttu-id="140c1-197">Объект [Details](/previous-versions/mt790655(v=vs.85)#PaymentRequest_params) JSON в **ответе на оплату** будет содержать данные об оплате, необходимые для обработки платежа.</span><span class="sxs-lookup"><span data-stu-id="140c1-197">The [details](/previous-versions/mt790655(v=vs.85)#PaymentRequest_params) JSON object in the **Payment Response** will contain the payment data required by the merchant to process a payment.</span></span>  <span data-ttu-id="140c1-198">Самый простой способ ответом представляет [Basic Card](https://w3c.github.io/payment-method-basic-card) собой базовую плату с четырьмя картой.</span><span class="sxs-lookup"><span data-stu-id="140c1-198">In its simplest form, the response will be a [Basic Card](https://w3c.github.io/payment-method-basic-card) payload containing cleartext payment card details.</span></span>  <span data-ttu-id="140c1-199">Если мероприятия маршруты упорядочивают свой обход процессоров с дополнительными партнерами шлюза или процессорами для предоставления поддержки платежей, возможно, ему потребуется пиграфическая загрузка процессора.</span><span class="sxs-lookup"><span data-stu-id="140c1-199">Where merchants have arrangements with additional gateway/processor partners for them to provide payments support, the merchant may require a payload the processor can handle.</span></span>  <span data-ttu-id="140c1-200">Они могут принимать форму маркера процессора или шлюза или зашифрованного платежного средства.</span><span class="sxs-lookup"><span data-stu-id="140c1-200">These can take the shape of a processor/gateway token or an encrypted payment instrument.</span></span>  <span data-ttu-id="140c1-201">Эти методы оплаты выходят за рамки данного документа и перечисляются в документации по конкретному процессору.</span><span class="sxs-lookup"><span data-stu-id="140c1-201">These payment methods are outside the scope of this document and will be covered in documentation specific to the processor.</span></span>  <span data-ttu-id="140c1-202">Кроме того, для получения [базового](https://w3c.github.io/payment-method-basic-card) ответа на карточку в корпорацию Майкрософт не требуется дополнительная адаптация в корпорацию Майкрософт, в отличие от других способов оплаты или шлюза, которые могут потребовать ся шифрование ключей шифрования или запросить авторизацию \(oAuth\).</span><span class="sxs-lookup"><span data-stu-id="140c1-202">Additionally, to receive a [Basic Card](https://w3c.github.io/payment-method-basic-card) response, no additional onboarding to Microsoft is required by the developer, unlike other processor/gateway specific payment methods which may require encryption key onboarding or request authorization \(oAuth\).</span></span>  

<span data-ttu-id="140c1-203">После поступления ответа **на оплату веб-сайт**отправляет платежную информацию об оплате его процессором.</span><span class="sxs-lookup"><span data-stu-id="140c1-203">Upon receiving the **Payment Response**, the website submits the payment information to their payment processor.</span></span>  <span data-ttu-id="140c1-204">Во время обработки платежа в браузере отобразится страница счетчика.</span><span class="sxs-lookup"><span data-stu-id="140c1-204">The browser will display a spinner page while the payment is being processed.</span></span>  

:::image type="complex" source="../media/loading_screen.png" alt-text="Конструктивная оплата запроса на оплату" lightbox="../media/loading_screen.png":::
   <span data-ttu-id="140c1-206">Страница, которая отображается при обработке платежа</span><span class="sxs-lookup"><span data-stu-id="140c1-206">The page displayed when the payment is being processed</span></span>  
:::image-end:::  

<span data-ttu-id="140c1-207">После завершения оплаты веб-страница вызывает метод [полного ()](/previous-versions/mt790642(v=vs.85)) и отправляет значение успешного **или** **отработки.**</span><span class="sxs-lookup"><span data-stu-id="140c1-207">Once the payment is complete, the web page calls the [complete()](/previous-versions/mt790642(v=vs.85)) method and passes a value of **success** or **fail**.</span></span>  <span data-ttu-id="140c1-208">[Метод полного()](/previous-versions/mt790642(v=vs.85)) сообщает браузеромо о том, что покупка завершена, а также соответствующий экран завершения, который должен отображаться в зависимости от значения успешного **или** **сбоя.**</span><span class="sxs-lookup"><span data-stu-id="140c1-208">The [complete()](/previous-versions/mt790642(v=vs.85)) method informs the browser that the purchase is finished and the appropriate terminating UI screen should be shown depending on the value of **success** or **fail**.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/response_payment-request_complete.png" alt-text="Конструктивная оплата запроса на оплату" lightbox="../media/response_payment-request_complete.png":::
         <span data-ttu-id="140c1-210">Интерфейс, отображаемый при успешном приобретении</span><span class="sxs-lookup"><span data-stu-id="140c1-210">The UI displayed when the purchase succeeded</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/response_payment-request_failure.png" alt-text="Конструктивная оплата запроса на оплату" lightbox="../media/response_payment-request_failure.png":::
         <span data-ttu-id="140c1-212">Интерфейс, отображаемый при сбое покупки</span><span class="sxs-lookup"><span data-stu-id="140c1-212">The UI displayed when the purchase failed</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="140c1-213">Запрос о платежа с помощью отправки</span><span class="sxs-lookup"><span data-stu-id="140c1-213">Payment Request with Shipping</span></span>  

### <span data-ttu-id="140c1-214">Адрес доставки</span><span class="sxs-lookup"><span data-stu-id="140c1-214">Shipping Address</span></span>  

<span data-ttu-id="140c1-215">Для продаж, для которых требуется доставка физических товаров, требуется адрес доставки.</span><span class="sxs-lookup"><span data-stu-id="140c1-215">For sales that require shipping physical goods, a shipping address is required.</span></span>  <span data-ttu-id="140c1-216">Чтобы включить адрес доставки, укажите `requestShipping = True` [параметры](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) запроса.</span><span class="sxs-lookup"><span data-stu-id="140c1-216">To include a shipping address, set `requestShipping = True` in the [options](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) parameter of the request.</span></span>  

<span data-ttu-id="140c1-217">Когда пользователь выбирает или обновляет адрес доставки, событие на экране запускается событие [onshippingaddresschange.](/previous-versions/mt790442(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="140c1-217">When the user selects or updates the shipping address, the [onshippingaddresschange](/previous-versions/mt790442(v=vs.85)) event will run.</span></span>  <span data-ttu-id="140c1-218">Веб-сайт, используя список событий, учитывайте об изменении, а затем сможет проверить адрес, пересчитывать затраты доставки и налоги по доставке, а также обновление [доставки,](/previous-versions/mt790440(v=vs.85)) чтобы отразить измененные затраты и доставки для выбранного адреса \(если применимо\).</span><span class="sxs-lookup"><span data-stu-id="140c1-218">The website, using an event listener, will be aware of the change and can then validate the address, re-calculate shipping costs and taxes, and update [shippingOptions](/previous-versions/mt790440(v=vs.85)) to reflect the changed costs and shipping options available for the address selected \(if applicable\).</span></span>  

### <span data-ttu-id="140c1-219">Параметры отправки</span><span class="sxs-lookup"><span data-stu-id="140c1-219">Shipping Options</span></span>  

<span data-ttu-id="140c1-220">Параметры отправки клиенту можно представить, добавив к [параметру сведений параметр](/previous-versions/mt790440(v=vs.85)) доставки параметрдовать [доставку](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) параметра доставки.</span><span class="sxs-lookup"><span data-stu-id="140c1-220">Shipping options can be presented to the customer by adding [shippingOptions](/previous-versions/mt790440(v=vs.85)) to the [details](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) parameter.</span></span>  <span data-ttu-id="140c1-221">Для этого можно задать один из вариантов `selected = True` отправки.</span><span class="sxs-lookup"><span data-stu-id="140c1-221">A default can be established by setting `selected = True` for one of the shipping options.</span></span>  
 
<span data-ttu-id="140c1-222">Когда пользователь выбирает или обновляет параметры доставки, [событие onshippingoptionchangechange будет](/previous-versions/mt790436(v=vs.85)) выполняться.</span><span class="sxs-lookup"><span data-stu-id="140c1-222">When the user selects or updates the shippingOptions, the [onshippingoptionchange](/previous-versions/mt790436(v=vs.85)) event will run.</span></span>  <span data-ttu-id="140c1-223">Веб-сайт, использующий список событий, учитывается об изменении и смогут обновлять сведения о параметре доставки. [details](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params)</span><span class="sxs-lookup"><span data-stu-id="140c1-223">The website, using an event listener, will be aware of the change and can update the [details](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) parameter with the correct shipping amount.</span></span>  

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

## <span data-ttu-id="140c1-224">Справочник по API</span><span class="sxs-lookup"><span data-stu-id="140c1-224">API Reference</span></span>  

[<span data-ttu-id="140c1-225">API запроса оплаты</span><span class="sxs-lookup"><span data-stu-id="140c1-225">Payment Request API</span></span>](/previous-versions/mt790447(v=vs.85))  

## <span data-ttu-id="140c1-226">Спецификаци</span><span class="sxs-lookup"><span data-stu-id="140c1-226">Specification</span></span>
[<span data-ttu-id="140c1-227">API запроса оплаты</span><span class="sxs-lookup"><span data-stu-id="140c1-227">Payment Request API</span></span>](https://w3.org/TR/payment-request)

<!-- links -->  

[DevtoolsGuideChromium]: /microsoft-edge/devtools-guide-chromium "Средства разработчика Microsoft Edge (на базе Chromium) | Документы Майкрософт"  

[MicrosoftSupport44533505]: https://support.microsoft.com/help/4533505 "Что такое устаревшая версия Microsoft Edge?"  
