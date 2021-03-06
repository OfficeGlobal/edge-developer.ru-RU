---
ms.assetid: f3560505-e01f-47e5-9ad6-7a419f060fc2
description: Узнайте о том, как использовать встроенные системы обмена сообщениями, чтобы ваше расширение могло взаимодействовать с сопутствующим приложением UWP.
title: Расширения — упаковка
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: EDGE, веб-разработка, HTML, CSS, JavaScript, разработчик
ms.openlocfilehash: 23c97f366db527cae2672d6ad46fa666583f6398
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571526"
---
# Упаковка расширений Microsoft Edge  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Наконец, вы закончите свое расширение и готовы упаковать его. Возможно, вам будет интересно узнать, что происходит в ходе выполнения следующих действий в руки потенциальных пользователей. Это руководство предназначено для изучения того, как это сделать.

Руководство по упаковке расширений является исчерпывающим в том, что оно охватывает все, что нужно знать о упаковках, даже более детально nitty gritty. Если вы не хотите изучать все, что нужно знать о том, как упаковать расширение, вы будете в курсе. Добавлена поддержка расширений для ManifoldJS — средства Open source node. js, которые занимают большую часть упаковки woes.

> [!NOTE]
> Отправка расширения Microsoft EDGE в Microsoft Store в настоящее время ограничена возможностями. [Поделитесь с нами](https://aka.ms/extension-request) с помощью ваших запросов на участие в Microsoft Store, и мы поможем вам ознакомиться с будущими обновлениями.


Воспользуйтесь приведенной ниже структурой "процесс" для подключения к упаковке Adventure!


## [Расширения в центре разработки для Windows](./packaging/extensions-in-the-windows-dev-center.md)

Независимо от того, какой маршрут создания пакетов вы выбрали, вручную или ManifoldJS, первым этапом является регистрация учетной записи разработчика Windows и резервирование имен ваших расширений.

После этого вы можете перейти в раздел [Создание и тестирование пакетов расширений](./packaging/creating-and-testing-extension-packages.md) , чтобы выяснить, как создаются appx-пакеты и вы вручную упаковывает свое расширение, либо просто перейдете на него и переходите к [использованию ManifoldJS в расширениях пакетов](./packaging/using-ManifoldJS-to-package-extensions.md).

> [!NOTE]
> После того как вы зайдете в США и хотите, чтобы ваше расширение было утверждено в магазине Microsoft Store, ознакомьтесь со [списком для отправки приложения](https://docs.microsoft.com/windows/uwp/publish/app-submissions).


## [Создание и тестирование пакетов расширений](./packaging/creating-and-testing-extension-packages.md)

Этот раздел руководства проходит через создание пакета расширения вручную, как только [вы настроили свою учетную запись разработчика Windows и заменили имена расширений (-ов)](./packaging/extensions-in-the-windows-Dev-Center.md). Если вы хотите больше узнать о том, как упаковать расширение, дайте это чтение.

Кроме того, в этой статье приведены сведения о том, как [тестировать и распаковать упакованное расширение](./packaging/creating-and-testing-extension-packages.md#testing-an-appx-package). Эта информация важна даже в том случае, если вы проходили маршрут на упаковке ManifoldJS.

## [Локализация пакетов расширений](./packaging/localizing-extension-packages.md)
Этап локализации пакета находится между созданием файла appxmanifest. XML и выполнением финальной команды для упаковки расширения.
Это позволяет указать, какие языки поддерживаются в вашем описании в магазине Microsoft Store, а также выбрать язык, на котором будет отображаться имя расширения в Windows.

Вы можете перейти к [локализованному имени и описанию в Microsoft Store](./packaging/localizing-extension-packages.md#localizing-name-and-description-in-the-microsoft-store) в этом разделе руководства, если ваше расширение не поддерживает несколько языков.

## [Использование ManifoldJS для расширения пакетов](./packaging/using-ManifoldJS-to-package-extensions.md)

На маршруте инструмента для упаковки вашего расширения ManifoldJS будет упаковываться расширение в привязке с минимальными усилиями на вашем конечном итоге. Предоставляя доступ к некоторым ресурсам Windows/Microsoft Store после того, как вы заполните некоторые свойства AppXManifest, и ваше расширение будет упаковано без времени.

После упаковки расширения вы можете ознакомиться с разделом [тестирование](./packaging/creating-and-testing-extension-packages.md#testing-an-appx-package) создания и тестирования расширения Microsoft EDGE, чтобы узнать, как неопубликованного или распаковать его.


## [Запуск комплекта сертификации приложений для Windows](./packaging/running-the-windows-app-certification-kit.md)

После того как у вас есть упакованное расширение, вы можете запустить его с помощью комплекта сертификации приложений для Windows. Это приведет к тому, что в пакете расширения будет выполняться ряд тестов, чтобы убедиться, что он готов для Microsoft Store.
