---
description: Функция Overrides — это функция, которая находится в инструменте источники Microsoft Edge DevTools, позволяющей копировать ресурсы веб-страниц на жесткий диск.  Когда вы обновите веб-страницу, DevTools не загружайте ресурс, а вместо этого замените его локальной копией.
title: Переопределение ресурсов веб-страниц с помощью локальных копий в Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 579ebe92dc50571837e7e3caf8fb7c1a9989bc59
ms.sourcegitcommit: 9dcaf598f3930bcfab9f93ff63463beb98274de0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/30/2020
ms.locfileid: "11145197"
---
# Переопределение ресурсов веб-страниц с помощью локальных копий в Microsoft Edge DevTools  

Иногда вам нужно исправить проблему на веб-странице, в которой нет доступа к данным или исправлениям, которые используют процесс создания медленной и сложной сборки.  Вы можете выполнять отладку и устранять неполадки всех типов в DevTools. Но проблема в том, что изменения не сохраняются.  После обновления файла вся работа будет пропала.  

Функция Overrides в инструменте " [источники][DevToolsSourcesTool] " помогает решить эту проблему.  

Теперь вы можете сделать ресурс текущей веб-страницей и сохранить ее локально.  Когда вы обновите веб-страницу, браузер не загрузит ресурс с сервера.  Вместо этого браузер заменяет его локальной копией ресурса.  

## Настройка локальной папки для хранения переопределений  

1.  В инструменте **источники** найдите несколько разделов в левой части экрана.  Если параметр **Переопределение** не отображается, нажмите кнопку <code>&#x0226B;</code><!--`≫`--> значок, чтобы получить его.  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/javascript-overrides-overflow-menu.msft.png" alt-text="Инструмент «источники» с недостаточным объемом свободного места для отображения параметра «Overrides»" lightbox="../media/javascript-overrides-overflow-menu.msft.png":::
             Инструмент « **источники** » с недостаточным объемом свободного места для отображения параметра «Overrides»  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/javascript-overrides-menu.msft.png" alt-text="Инструмент «источники» с недостаточным объемом свободного места для отображения параметра «Overrides»" lightbox="../media/javascript-overrides-menu.msft.png":::
             Выбор параметра "изменения"  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  После выбора параметра " **изменения** " необходимо выбрать папку на локальном компьютере, чтобы сохранить файлы ресурсов, которые вы хотите заменить.  Нажмите кнопку **+ выбрать для поиска переопределенных** папок.  
    
    :::image type="complex" source="../media/javascript-overrides-select-folder.msft.png" alt-text="Инструмент «источники» с недостаточным объемом свободного места для отображения параметра «Overrides»" lightbox="../media/javascript-overrides-select-folder.msft.png":::
       Выбор папки для использования при переопределении  
    :::image-end:::  
    
1.  DevTools предупреждает вас о том, что у вас должен быть полный доступ к папке, и не следует отображать конфиденциальную информацию.  На панели с предупреждением выберите **разрешение** для предоставления доступа.  
    
    :::image type="complex" source="../media/javascript-overrides-give-access-to-folder.msft.png" alt-text="Инструмент «источники» с недостаточным объемом свободного места для отображения параметра «Overrides»" lightbox="../media/javascript-overrides-give-access-to-folder.msft.png":::
       Предоставление DevTools доступа к папке  
    :::image-end:::  
    
1.  В области **Overrides** должен отображаться флажок рядом с `Enable Local Overrides` папкой Overrides.  Рядом с ним появится значок, с помощью которого вы можете удалить локальные параметры переопределения.  Теперь вы закончите настройку папки и будете готовы заменить динамические ресурсы локальными.
    
    :::image type="complex" source="../media/javascript-overrides-folder-setup-complete.msft.png" alt-text="Инструмент «источники» с недостаточным объемом свободного места для отображения параметра «Overrides»" lightbox="../media/javascript-overrides-folder-setup-complete.msft.png":::
       Настройка папки "переопределения" успешно завершена  
    :::image-end:::  
    
## Добавление файлов в папку Overrides  
  
Чтобы добавить файлы в папку Overrides, откройте инструмент **элементы** и просмотрите веб-страницу.  Чтобы изменить стиль CSS, выберите его имя в инспекторе **стилей** .  

:::image type="complex" source="../media/javascript-overrides-select-css-file.msft.png" alt-text="Инструмент «источники» с недостаточным объемом свободного места для отображения параметра «Overrides»" lightbox="../media/javascript-overrides-select-css-file.msft.png":::
   Выбор файла в инспекторе **стилей**  
:::image-end:::  

В редакторе **источников** наведите указатель мыши на имя файла выбранного файла, откройте контекстное меню (щелкните правой кнопкой мыши \) и выберите команду **сохранить для переопределений**.  

:::image type="complex" source="../media/javascript-overrides-file-name.msft.png" alt-text="Инструмент «источники» с недостаточным объемом свободного места для отображения параметра «Overrides»" lightbox="../media/javascript-overrides-file-name.msft.png":::
   В редакторе **источников** введите имя файла для переопределения.  
:::image-end:::  

:::image type="complex" source="../media/javascript-overrides-save-for-overrides.msft.png" alt-text="Инструмент «источники» с недостаточным объемом свободного места для отображения параметра «Overrides»" lightbox="../media/javascript-overrides-save-for-overrides.msft.png":::
   В контекстном меню выберите команду **сохранить для переопределения** .  
:::image-end:::  

Файл сохраняется в папке Overrides.  Убедитесь, что DevTools создает папку с именем, использующую URL-адрес файла с правильной структурой каталогов.  Файл хранится внутри.  В редакторе теперь отображается фиолетовая точка, указывающая на то, что файл является локальным и не является динамическим.  

:::image type="complex" source="../media/javascript-overrides-file-stored.msft.png" alt-text="Инструмент «источники» с недостаточным объемом свободного места для отображения параметра «Overrides»" lightbox="../media/javascript-overrides-file-stored.msft.png":::
   Файл успешно сохранен в папке Overrides  
:::image-end:::  

:::row:::
   :::column span="":::
      В следующем примере теперь можно изменить стили веб-страницы.  Чтобы добавить красную рамку вокруг файла, в редакторе **стилей** Скопируйте приведенный ниже стиль и добавьте его в элемент Body.  
      
      ```css
      border: 10px solid firebrick
      ```  
   :::column-end:::
   :::column span="":::
      Файл будет автоматически сохранен на вашем компьютере.  Если вы обновите файл, отобразится граница, и все ваши данные не будут потеряны.  
      
      :::image type="complex" source="../media/javascript-overrides-changing-styles.msft.png" alt-text="Инструмент «источники» с недостаточным объемом свободного места для отображения параметра «Overrides»" lightbox="../media/javascript-overrides-changing-styles.msft.png":::
         Изменение стилей веб-страниц с помощью редактирования файлов в папке Overrides  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

:::row:::
   :::column span="":::
      В инструменте **источники** в разделе **страница** наведите указатель мыши на любой файл, откройте контекстное меню (щелкните правой кнопкой мыши \) и добавьте его в переопределение.  Файлы, которые уже находятся в папке Overrides, имеют фиолетовые точки на значке.  
      
      :::image type="complex" source="../media/javascript-overrides-safe-from-sources.msft.png" alt-text="Инструмент «источники» с недостаточным объемом свободного места для отображения параметра «Overrides»" lightbox="../media/javascript-overrides-safe-from-sources.msft.png":::
         Выбор файла в инструменте « **источники** » для переопределений  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      Кроме того, в инструменте **Network (сеть** ) наведите указатель мыши на любой файл, откройте контекстное меню (щелкните правой кнопкой мыши \) и добавьте его в переопределение.  Переопределение в силе — файлы, которые находятся на компьютере, а не на веб-странице Live.  Когда действует переопределение, в инструменте **Network (сеть** ) найдите значок предупреждения рядом с именем файла.  
      
      :::image type="complex" source="../media/javascript-overrides-network.msft.png" alt-text="Инструмент «источники» с недостаточным объемом свободного места для отображения параметра «Overrides»" lightbox="../media/javascript-overrides-network.msft.png":::
         Выбор файла в средстве " **сеть** " для переопределения  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## Двухстороннее взаимодействие с переопределенными методами  

Используйте редактор, предоставленный с помощью инструмента " **источники** " DevTools, или любой другой редактор, для которого вы хотите изменить файлы.  Изменения синхронизируются для всех продуктов, которые обращаются к файлам в папке Overrides.  

## Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsSourcesTool]: ../sources.md "Общие сведения о средстве «источники» | Документы Microsoft"  
