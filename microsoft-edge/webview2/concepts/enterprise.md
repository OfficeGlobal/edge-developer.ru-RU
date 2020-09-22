---
description: Общие сведения об управлении WebView2 приложениями
title: Управление WebView2 приложениями
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/21/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, управление браузером, EDGE HTML, предприятие, групповая политика, управляемость
ms.openlocfilehash: 1eb8b9dc1637daa8d10004ab8c340fe9ae33e38b
ms.sourcegitcommit: 24151cc65bad92d751a8e7a868c102e1121456e3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/22/2020
ms.locfileid: "11057866"
---
# Управление WebView2 приложениями  

[WebView2][WebView2Landing] — это компонент, который используются разработчиками для создания приложений, и разработчики могут развернуть [Самообновляемую среду выполнения WebView2 Evergreen][Webview2ConceptsDistributionUnderstandRuntimeInstallerPreview] на устройстве пользователя, чтобы поработать с ними приложения.  В этом документе описано, как ИТ администраторы могут управлять приложениями WebView2 и средой выполнения.  Отзывы и предложения от ИТ – администраторов и разработчиков находятся в [репозитории обратной связи WebView2][GithubMicrosoftedgeWebviewfeddback].  

## Групповые политики для WebView2  

ИТ-администраторы могут использовать объекты групповой политики \ (GPO) для настройки параметров политики для WebView2.  Следующий набор политик неприменим к WebView2,  

*   [Политики обновления Microsoft Edge][EdgeUpdatePolicies] доступны для ИТ-администраторов, чтобы управлять аспектами установки и обновления среды выполнения WebView2.  Браузер Microsoft EDGE и среда выполнения WebView2 обновляются с помощью одного и того же механизма обновления.  За исключением случаев, когда ни один из политик (например `Update` , для определенного канала) применяется как в браузере, так и в среде выполнения WebView2.  Например, `UpdateSuppressed` ИТ-администраторы могут настроить время в каждый день, чтобы отключить автоматическое обновление как для браузера, так и для среды выполнения WebView2.  Это позволяет ИТ-администраторам настраивать параметры и прокси-серверы, как в браузере, так и в среде выполнения WebView2 для управления пропускной способностью сети и трафиком или для других целей.  ИТ-администраторы могут выполнять [инструкции Microsoft][ConfigureMicrosoftEdge] Edge для настройки политик обновления Microsoft Edge.  
*   [Microsoft Edge — политики браузера][EdgeBrowserPolicies] не применяются к WebView2 приложениям.  Это обусловлено тем, что приложения и браузеры имеют разные варианты использования, и ИТ-администраторы могут не знать о том, какие приложения используют WebView2.  Применение политик браузера в WebView2 может привести к нежелательным последствиям.  Например, администраторы могут заблокировать JavaScript в браузере, и все приложения WebView2 с использованием JavaScript будут разорваны.  
*   \ (Вскоре) политики WebView2 – WebView2 предоставит небольшой дополнительный набор групповых политик в тех случаях, когда управление WebView2 напрямую имеет смысл.  Мы рекомендуем разработчикам приложений реализовывать собственные групповые политики для управления использованием WebView2, так как они более просты для ИТ – администраторов для управления приложением, а не WebView2 напрямую.  

<!-- Links -->  

[Webview2ConceptsDistributionUnderstandRuntimeInstallerPreview]: ./distribution.md#understanding-the-webview2-runtime "Общие сведения о среде выполнения WebView2 и установщике (Предварительная версия) — распространение приложений с помощью WebView2 | Документы Microsoft"  

[WebView2Landing]: ../index.md "Введение в Microsoft Edge WebView2 (Предварительная версия) | Документы Microsoft"  

[EdgeUpdatePolicies]: /deployedge/microsoft-edge-update-policies "Microsoft Edge: политики обновления | Документы Microsoft"  
[EdgeBrowserPolicies]: /deployedge/microsoft-edge-policies "Microsoft Edge: политики браузера | Документы Microsoft"  
[ConfigureMicrosoftEdge]: /deployedge/configure-microsoft-edge "Настройка параметров политики Microsoft EDGE в Windows | Документы Microsoft"  


[GithubMicrosoftedgeWebviewfeddback]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView Feedback-MicrosoftEdge/WebViewFeedback | GitHub"  
