---
description: Перемещение пользователей в Microsoft Edge из Internet Explorer
title: Перемещение пользователей в Microsoft Edge из Internet Explorer
author: MSEdgeTeam
ms.date: 11/04/2020
ms.author: msedgedevrel
ms.prod: microsoft-edge
keywords: Microsoft EDGE, совместимость, веб-платформа, Internet Explorer
ms.openlocfilehash: 48f0f4121fb444d80603dcbb408397679c64753d
ms.sourcegitcommit: 7b4441b7656c8317139650f904b70cc87797d37e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "11154336"
---
# <span data-ttu-id="386f3-104">Перемещение пользователей в Microsoft Edge из Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="386f3-104">Moving users to Microsoft Edge from Internet Explorer</span></span> 

<span data-ttu-id="386f3-105">У многих современных веб-сайтов есть макеты, несовместимые с Internet Explorer \ (IE).</span><span class="sxs-lookup"><span data-stu-id="386f3-105">Many modern websites have designs that are incompatible with Internet Explorer \(IE\).</span></span>  <span data-ttu-id="386f3-106">Если пользователь IE посещает неподдерживаемый общедоступный веб-сайт, пользователь может получить сообщение.</span><span class="sxs-lookup"><span data-stu-id="386f3-106">When an IE user visits an incompatible public website, the user may get a message.</span></span>  <span data-ttu-id="386f3-107">В сообщении говорится о том, что веб-сайт несовместим с браузером.</span><span class="sxs-lookup"><span data-stu-id="386f3-107">The message states that the website is incompatible with the browser.</span></span>  <span data-ttu-id="386f3-108">После того как сообщение будет выводиться, ожидается, что пользователь вручную переключается на современный браузер.</span><span class="sxs-lookup"><span data-stu-id="386f3-108">After the message is displayed, the user is expected to manually switch to a modern browser.</span></span>  <span data-ttu-id="386f3-109">Чтобы свести к минимуму перерывы, начиная с версии 84, Microsoft EDGE поддерживает новую возможность, которая автоматически перенаправляет пользователей.</span><span class="sxs-lookup"><span data-stu-id="386f3-109">To minimize disruptions, starting with version 84, Microsoft Edge supports a new capability that automatically redirects users.</span></span>  <span data-ttu-id="386f3-110">Если пользователь IE переходит на веб-сайт, несовместимый с IE, Windows автоматически перенаправляет пользователя в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="386f3-110">When an IE user navigates to a website that is incompatible with IE, Windows automatically redirects the user to Microsoft Edge.</span></span>  <span data-ttu-id="386f3-111">Чтобы просмотреть веб-сайты в списке, перейдите к [списку необходим Microsoft Edge][MicrosoftEdgeNeededgeV1].</span><span class="sxs-lookup"><span data-stu-id="386f3-111">To review the websites on the list, navigate to [Need Microsoft Edge list][MicrosoftEdgeNeededgeV1].</span></span>

<span data-ttu-id="386f3-112">В этой статье описаны указанные ниже принципы.</span><span class="sxs-lookup"><span data-stu-id="386f3-112">This article describes the following concepts.</span></span>  

*   <span data-ttu-id="386f3-113">Взаимодействие с пользователем для перенаправления</span><span class="sxs-lookup"><span data-stu-id="386f3-113">The user experience for redirection</span></span>  
*   <span data-ttu-id="386f3-114">Добавление веб-сайта в список совместимости с IE</span><span class="sxs-lookup"><span data-stu-id="386f3-114">How to add your website to the IE compatibility list</span></span>  
*   <span data-ttu-id="386f3-115">Удаление веб-сайта из списка совместимости с IE</span><span class="sxs-lookup"><span data-stu-id="386f3-115">How to remove your website from the IE compatibility list</span></span>  
    
## <span data-ttu-id="386f3-116">Почему веб-сайт добавлен в список совместимости IE?</span><span class="sxs-lookup"><span data-stu-id="386f3-116">Why is a website added to the IE compatibility list?</span></span>  

<span data-ttu-id="386f3-117">Список совместимости IE добавляет веб-сайт только в том случае, если выполняются описанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="386f3-117">The IE compatibility List only adds a website when the following actions occur.</span></span>  

*   <span data-ttu-id="386f3-118">Показывает пользователю IE сообщение, предлагающее пользователю использовать другой браузер для обеспечения совместимости.</span><span class="sxs-lookup"><span data-stu-id="386f3-118">Shows an IE user a message suggesting the user should use a different browser for compatibility reasons.</span></span>  
*   <span data-ttu-id="386f3-119">Владелец запрашивает добавление веб-сайта в список совместимости с IE.</span><span class="sxs-lookup"><span data-stu-id="386f3-119">Owner requests to add the website to the IE compatibility list.</span></span>  
    
## <span data-ttu-id="386f3-120">Обновление списка совместимости с IE</span><span class="sxs-lookup"><span data-stu-id="386f3-120">Update the IE compatibility list</span></span>  

<span data-ttu-id="386f3-121">Список совместимости IE — это XML-файл на [Microsoft.com][MicrosoftOfficialHome].</span><span class="sxs-lookup"><span data-stu-id="386f3-121">The IE compatibility list is an XML file on [microsoft.com][MicrosoftOfficialHome].</span></span>  <span data-ttu-id="386f3-122">Этот список регулярно обновляется в ответ на запросы разработчиков веб-сайтов и пользователей, которым требуется добавить или удалить веб-сайт.</span><span class="sxs-lookup"><span data-stu-id="386f3-122">The list is regularly updated in response to user's and website developers requests to have websites added or removed.</span></span>  <span data-ttu-id="386f3-123">Обновления списка автоматически загружаются на компьютеры пользователей.</span><span class="sxs-lookup"><span data-stu-id="386f3-123">Updates to the list are automatically downloaded to user machines.</span></span>  

<span data-ttu-id="386f3-124">Напишите на веб-сайте [ietoedge@microsoft.com][MailtoMicrosoftIetoedge] , который нужно добавить или удалить из списка СОВМЕСТИМОСТИ с IE, и попросите на него следующую информацию.</span><span class="sxs-lookup"><span data-stu-id="386f3-124">Email the following information to [ietoedge@microsoft.com][MailtoMicrosoftIetoedge] for your website to be added or removed from the IE compatibility list.</span></span>    

*   <span data-ttu-id="386f3-125">Имя владельца</span><span class="sxs-lookup"><span data-stu-id="386f3-125">Owner name</span></span>  
*   <span data-ttu-id="386f3-126">Название организации</span><span class="sxs-lookup"><span data-stu-id="386f3-126">Corporate title</span></span>  
*   <span data-ttu-id="386f3-127">Адрес электронной почты</span><span class="sxs-lookup"><span data-stu-id="386f3-127">Email address</span></span>  
*   <span data-ttu-id="386f3-128">Название организации</span><span class="sxs-lookup"><span data-stu-id="386f3-128">Company name</span></span>  
*   <span data-ttu-id="386f3-129">Улица</span><span class="sxs-lookup"><span data-stu-id="386f3-129">Street address</span></span>  
*   <span data-ttu-id="386f3-130">Адрес веб-сайта</span><span class="sxs-lookup"><span data-stu-id="386f3-130">Website address</span></span>  
<!--  *   Telephone number  -->  
<!--  *   Target platform \(desktop, phone, Xbox\)  -->  
    
<!-- links -->  

[MailtoMicrosoftIetoedge]: mailto:ietoedge@microsoft.com "Отправка сообщения электронной почты в ietoedge@microsoft.com"  

[MicrosoftOfficialHome]: https://www.microsoft.com "Официальная домашняя страница Microsoft"  

[MicrosoftEdgeNeededgeV1]:  https://edge.microsoft.com/neededge/v1 "Нужен список Microsoft Edge с кодом версии v1 | Microsoft Edge"  
