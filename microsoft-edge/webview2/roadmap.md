---
description: Узнайте о том, что дальше в WebView2
title: План для Microsoft Edge WebView 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/19/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 4b64509e63acb966a95c32c4560c3ddcefebd5e4
ms.sourcegitcommit: 5bdffe91a6594f77eeffa4e864fda90a02784771
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/19/2020
ms.locfileid: "10659715"
---
# WebView2ная схема Microsoft Edge

##### Последнее обновление: Май 2020

Элемент управления WebView2 позволяет разработчикам внедрять веб-технологии в собственные приложения. В этом документе представлен перспективный план для WebView2. 

> [!NOTE]
> WebView2 находится в активном состоянии, и план продолжит развиваться в соответствии с изменениями рынка и отзывами пользователей, поэтому обратите внимание на то, что описанные здесь планы не являются исчерпывающими и могут быть изменены. 

Если у вас возникли проблемы или вопросы о планах, оставьте отзыв в [репозитории обратной связи](https://github.com/MicrosoftEdge/WebViewFeedback).

У группы WebView2 есть несколько основных усилий.

1.  Установщик среды выполнения WebView2 (Q4 2020)
2.  Фиксированная версия (Q4 2020)
3.  Общая доступность 
    *   Win32 C/C++ (Q4 2020)
    *   .NET (Q4 2020)
    *   WinUI 3,0 (Q2 2021)

## Установщик & среды выполнения WebView2

Модель распространения WebView2 [Evergreen](./concepts/distribution.md#microsoft-edge-webview2-runtime) позволит вам назначать или устанавливать среду выполнения WebView2 на компьютер пользователя. Предварительная версия среды выполнения WebView2 и установщика должна быть доступна Q3 2020 и Дж в Q4 2020.

## Фиксированная версия

С помощью [фиксированной](./concepts/distribution.md#roadmap) модели распределения WebView2 можно упаковать двоичные файлы Microsoft EDGE в собственное приложение. Инженерные задачи в настоящее время в предварительной версии не запланировались до конца Q3 2020 и Дж 4 квартала 2020.

## Общая доступность 

### Win32 C/C++

Пакет SDK для Win32 C/C++ должен быть в 4 квартале 2020 вскоре после среды выполнения WebView2 и установщика GA.

### .NET

.NET SDK упаковывает пакет SDK C/C++ для Win32. Предполагается, что пакет .NET SDK вскоре скоро будет после того, как Win32 C/C++ GA в 4 квартале 2020.

### WinUI 3,0

Вы можете перенести WebView2 в приложения UWP с помощью [Win UI 3,0](/uwp/toolkits/winui3/), в настоящее время в Alpha. Извлеките [схему библиотеки пользовательского интерфейса Windows](https://github.com/microsoft/microsoft-ui-xaml/blob/master/docs/roadmap.md) , чтобы поддерживать актуальность.  