---
description: Откройте вкладку датчики и перейдите к разделу ориентация.
title: Имитация ориентации устройства с помощью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 01e6d3a24513b504665dbe0c03d9e72cc1f97533
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "11124959"
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

# <span data-ttu-id="5981c-104">Имитация ориентации устройства с помощью Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="5981c-104">Simulate device orientation with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="5981c-105">Выполните указанные ниже действия, чтобы имитировать различные ориентации устройств в Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="5981c-105">Complete the following actions to simulate different device orientations from Microsoft Edge DevTools.</span></span>  

<!--todo: update device orientation section when available -->  

1.  <span data-ttu-id="5981c-106">Выберите `Control` + `Shift` + `P` \ (Windows, Linux \) или `Command` + `Shift` + `P` \ (macOS \), чтобы открыть **меню команд**.</span><span class="sxs-lookup"><span data-stu-id="5981c-106">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-console-command-menu.msft.png" alt-text="Меню команд" lightbox="../media/device-mode-console-command-menu.msft.png":::
       <span data-ttu-id="5981c-108">**Меню команд**</span><span class="sxs-lookup"><span data-stu-id="5981c-108">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="5981c-109">Введите текст `sensors` , нажмите кнопку **Показать датчики**и выберите `Enter` .</span><span class="sxs-lookup"><span data-stu-id="5981c-109">Type `sensors`, choose **Show Sensors**, and select `Enter`.</span></span>  <span data-ttu-id="5981c-110">Вкладка **датчики** откроется в нижней части окна DevTools.</span><span class="sxs-lookup"><span data-stu-id="5981c-110">The **Sensors** tab opens at the bottom of your DevTools window.</span></span>  
1.  <span data-ttu-id="5981c-111">В списке **ориентация** выберите одну из готовых ориентаций (например `Portrait upside down` , или настроить **пользовательскую ориентацию** ), чтобы обеспечить точное расположение.</span><span class="sxs-lookup"><span data-stu-id="5981c-111">From the **Orientation** list, select one of the preset orientations, such as `Portrait upside down`, or choose **Custom orientation** to provide your own exact orientation.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/device-mode-console-sensors-orientation-portrait-upside-down.msft.png" alt-text="Меню команд" lightbox="../media/device-mode-console-sensors-orientation-portrait-upside-down.msft.png":::
             <span data-ttu-id="5981c-113">Выбор `Portrait upside down` из списка **ориентации**</span><span class="sxs-lookup"><span data-stu-id="5981c-113">Select `Portrait upside down` from the **Orientation** list</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          <span data-ttu-id="5981c-114">После выбора варианта **Пользовательская ориентация**будет `alpha` `beta` `gamma` включена.</span><span class="sxs-lookup"><span data-stu-id="5981c-114">After you choose **Custom orientation**, the `alpha`, `beta`, and `gamma` fields are enabled.</span></span>  
          <!--See [Alpha][alpha], [Beta][beta], and [Gamma][gamma] to understand how each axis works.  -->  
          <!--todo: update links to alpha, beta, and gamma section when available -->  
          <span data-ttu-id="5981c-115">Вы также можете настроить пользовательскую ориентацию, перетащив **модель ориентации**.</span><span class="sxs-lookup"><span data-stu-id="5981c-115">You are also able to set a custom orientation by dragging the **Orientation Model**.</span></span>  <span data-ttu-id="5981c-116">Удерживайте `Shift` перед перетаскиванием, чтобы повернуть вдоль `alpha` оси.</span><span class="sxs-lookup"><span data-stu-id="5981c-116">Hold `Shift` before dragging to rotate along the `alpha` axis.</span></span>  
          
          :::image type="complex" source="../media/device-mode-console-sensors-orientation-custom.msft.png" alt-text="Меню команд" lightbox="../media/device-mode-console-sensors-orientation-custom.msft.png":::
             <span data-ttu-id="5981c-118">**Модель ориентации**</span><span class="sxs-lookup"><span data-stu-id="5981c-118">The **Orientation Model**</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
## <span data-ttu-id="5981c-119">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="5981c-119">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

<!--[WebFundamentasNativeHardwareDeviceOrientationIndex]: /web/fundamentals/native-hardware/device-orientation/index "Device Orientation & Motion"  -->  
<!--[WebFundamentasNativeHardwareDeviceOrientationIndexAlpha]: /web/fundamentals/native-hardware/device-orientation/index#alpha "Alpha - Device Orientation & Motion"  -->  
<!--[WebFundamentasNativeHardwareDeviceOrientationIndexBeta]: /web/fundamentals/native-hardware/device-orientation/index#beta "Beta - Device Orientation & Motion"  -->  
<!--[WebFundamentasNativeHardwareDeviceOrientationIndexGamma]: /web/fundamentals/native-hardware/device-orientation/index#gamma "Gamma - Device Orientation & Motion"  -->  

> [!NOTE]
> <span data-ttu-id="5981c-120">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="5981c-120">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="5981c-121">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/device-mode/orientation) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="5981c-121">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/device-mode/orientation) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="5981c-123">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="5981c-123">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
