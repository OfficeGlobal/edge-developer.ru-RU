---
description: Использование элементов для Microsoft EDGE (Chromium) из кода Visual Studio
title: Элементы для Microsoft EDGE (Chromium) из кода Visual Studio
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/26/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools, код VS, код Visual Studio, элементы
ms.openlocfilehash: 81488c08a76a16b80a415cbd17cd0617df916f54
ms.sourcegitcommit: 1cfcf2c8970a6c2221cfbf09a23d36b08bd60690
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "11135502"
---
# Расширение кода Microsoft Edge DevTools для Visual Studio  

Использование <!--the [Microsoft Edge DevTools for Visual Studio Code][VisualstudioMarketplaceElementsMicrosoftEdgeChromium] -->Это расширение для Access в Microsoft Edge DevTools в [коде Visual Studio][VisualstudioCode].  У вас есть доступ к **элементам** и **сетевым** инструментам в Microsoft Edge DevTools.  Вы можете запустить или присоединиться к экземпляру Microsoft Edge.  После подключения вы можете отобразить структуру HTML среды выполнения, изменить макет, устранить проблемы со стилизацией и проанализировать сетевой трафик.  

## Инструмент "элементы"  

По умолчанию расширение запускает экземпляр браузера в уникальном окне и предоставляет вам функциональные возможности **элементов** Microsoft Edge DevTools.  

:::image type="complex" source="./media/edge-devtools-for-vscode-windowed.png" alt-text="Microsoft Edge DevTools для кода Visual Studio, работающего в полном окне браузера" lightbox="./media/edge-devtools-for-vscode-windowed.png":::
   Microsoft Edge DevTools для кода Visual Studio, работающего в полном окне браузера  
:::image-end:::  

В параметрах расширения вы можете включить дополнительные функции, такие как **режим Бездисплейной** **сети и сеть**.  

:::image type="complex" source="./media/edge-devtools-for-vscode-settings.png" alt-text="Microsoft Edge DevTools для кода Visual Studio, работающего в полном окне браузера" lightbox="./media/edge-devtools-for-vscode-settings.png":::
   Включение и отключение режима без монитора и проверки сети в параметрах расширения  
:::image-end:::  

## Режим без монитора  

В режиме бездисплейного режима это расширение не запускает полный экземпляр браузера для отладки.  Он запускает экземпляр в фоновом режиме.  Возможно, вам придется оставаться внутри редактора и взаимодействовать с внедренным браузером.  На панели задач не отображается дополнительный значок браузера.  

:::image type="complex" source="./media/edge-devtools-for-vscode-headless.png" alt-text="Microsoft Edge DevTools для кода Visual Studio, работающего в полном окне браузера" lightbox="./media/edge-devtools-for-vscode-headless.png":::
   Microsoft Edge DevTools для кода Visual Studio, работающего в автономном браузере  
:::image-end:::  

> [!NOTE]
> В macOS следует включить режим без монитора в качестве предпочтительного режима.  При использовании режима без монитора необходимо решить проблему, в которой окно браузера выводится, если окно не отображается `Not Active` .  

## Инструмент "сеть"  

Если вы также хотите проверить сетевой трафик вашего приложения, откройте параметры и включите вкладку **сеть** .  

:::image type="complex" source="./media/edge-devtools-for-vscode-network.png" alt-text="Microsoft Edge DevTools для кода Visual Studio, работающего в полном окне браузера" lightbox="./media/edge-devtools-for-vscode-network.png":::
    Проверка сети в Microsoft Edge DevTools для кода Visual Studio  
:::image-end:::  

## Запуск Microsoft Edge из расширения  

На **панели действий**перейдите в раздел "Инструменты Microsoft Edge".  Рядом с надписью **Microsoft Edge Tools: targets ("цели")** есть знак "плюс", который открывает браузер для вашего приложения.  Если вы выбрали параметр **about: Blank** , то для его отображения на панели **элементы** в коде Visual Studio необходимо перейти в браузере для этого веб-приложения.  

## Запуск Microsoft Edge из представления отладки  

Если вы привыкли использовать представление отладку в коде Visual Studio, вы можете получить доступ к Microsoft Edge DevTools.  

1.  В коде Visual Studio перейдите в представление Отладка 
    *   Выберите `Ctrl` + `Shift` + `D` в Windows или Linux \ ( `Command` + `Shift` + `D` на macOS \).  

<!--TODO:  Is this section intended to be optional  -->  
> [!NOTE]
> 1.  Если у вас нет каких – либо конфигураций в коде Visual Studio, выполните одно из указанных ниже действий.  
>     *   Выберите `F5` .  
>     *   Нажмите кнопку **воспроизвести** \ (зеленый \).  
> 1.  В раскрывающемся списке выберите пункт **край** в раскрывающемся списке.  
> 1.  `launch.json`Должен отобразиться файл, содержащий указанную ниже конфигурацию.  
>     
>     ```json
>     {
>       "version": "0.2.0",
>       "configurations": [
>         {
>           "name": "Launch Microsoft Edge and open the Edge DevTools",
>           "request": "launch",
>           "type": "vscode-edge-devtools.debug",
>           "url": "http://localhost:8080"
>         }
>       ]
>     }
>     ```  
>     
> После загрузки правильной конфигурации выполните указанные ниже действия.  

1.  Чтобы запустить инструмент **элементы** из кода Visual Studio, выполните одно из указанных ниже действий. 
    *   Выберите `F5` .  
    *   Нажмите кнопку **воспроизвести** \ (зеленый \).  
         
Теперь вы можете выполнить указанные ниже действия.  

*   Открыть презентацию в браузере.  
*   Проверьте модель DOM и стиль компонентов на странице.  

## Присоединение к Microsoft Edge  

Чтобы открыть браузер и присоединить экземпляр к коду Visual Studio, выполните указанные ниже действия. 

1.  Чтобы открыть экземпляр Microsoft Edge \ (Chromium \), скопируйте и выполните следующую команду:  
    
    ```shell
    start msedge --remote-debugging-port=9222
    ```  
    
1.  После того как экземпляр запустится, скопируйте и вставьте следующий фрагмент кода в `launch.json` файл.  
    
    ```json
    {
        "type": "vscode-edge-devtools.debug",
        "request": "attach",
        "name": "Attach to Microsoft Edge and open the developer tools",
        "url": "http://localhost:3000/",
        "webRoot": "${workspaceFolder}/out",
        "port": 9222
    }
    ```  
    
1.  В коде Visual Studio откройте раскрывающееся меню **отладчик** и выберите команду **присоединиться к Microsoft EDGE и откройте Инструменты разработчика**.  
1.  Чтобы запустить инструмент **элементы** из кода Visual Studio, выполните одно из указанных ниже действий. 
    *   Выберите `F5` .  
    *   Нажмите кнопку **воспроизвести** \ (зеленый \).  
         
Теперь вы можете выполнить указанные ниже действия.  

*   Открыть презентацию в браузере.  
*   Проверьте модель DOM и стиль компонентов на странице.  
    
## Знакомство с командой Microsoft Edge DevTools для расширения кода Visual Studio  

Отправьте отзыв, выполнив [архивацию][GithubMicrosoftVscodeEdgeDevtoolsNewIssue] в [репозитории GitHub][GithubMicrosoftVscodeEdgeDevtools] в расширении.  

Сведения о том, что нужно сделать <!--the Microsoft Edge DevTools for Visual Studio Code -->Это расширение лучше, ваши публикации — Добро пожаловать.  Найдите все, что нужно, чтобы начать работу в [репозитории GitHub][GithubMicrosoftVscodeEdgeDevtools] на расширение.  

<!--links -->  

[VisualstudioCode]: https://code.visualstudio.com "Код Visual Studio"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Документация | Код Visual Studio"   

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/Microsoft/vscode-edge-devtools "Microsoft/vscode-Edge-Devtools | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsNewIssue]: https://github.com/Microsoft/vscode-edge-devtools/issues/new "Новая ошибка — Microsoft/vscode-Edge-Devtools | GitHub"

[VisualstudioMarketplaceElementsMicrosoftEdgeChromium]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Инструменты Microsoft Edge для кода VS"  
