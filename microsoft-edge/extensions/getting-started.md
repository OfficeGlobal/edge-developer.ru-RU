---
description: Узнайте о том, как начать разработку, чтобы обойтись на упаковке расширений Microsoft Edge.
title: Расширения — начало работы
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: EDGE, веб-разработка, HTML, CSS, JavaScript, разработчик, расширения
ms.openlocfilehash: 5d2bf0ea2236e36b9e6205e13291ffee4118d9d7
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571584"
---
# <span data-ttu-id="df18a-104">Начало работы с расширениями</span><span class="sxs-lookup"><span data-stu-id="df18a-104">Getting started with extensions</span></span>  

[!INCLUDE [deprecation-note](includes/deprecation-note.md)]  

<span data-ttu-id="df18a-105">Это руководство содержит все сведения, необходимые для разработки, тестирования, упаковки и публикации расширений для Microsoft EDGE, если разработчик хочет ознакомиться с расширениями или сезонными ветеранами с расширением Chrome, которое вы хотели бы перенести.</span><span class="sxs-lookup"><span data-stu-id="df18a-105">Whether you're a new developer wanting to familiarize yourself with extensions or a seasoned veteran with a Chrome extension you'd like to port, this guide contains all the information you need to develop, test, package, and publish an extension for Microsoft Edge.</span></span> 

## <span data-ttu-id="df18a-106">Разработка расширения</span><span class="sxs-lookup"><span data-stu-id="df18a-106">Developing an extension</span></span>

<span data-ttu-id="df18a-107">Первый этап этого путешествия — Создание расширения Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="df18a-107">The first step of this journey is to create a Microsoft Edge extension:</span></span> 
- <span data-ttu-id="df18a-108">Новое в расширениях?</span><span class="sxs-lookup"><span data-stu-id="df18a-108">New to extensions?</span></span> <span data-ttu-id="df18a-109">Ознакомьтесь с [руководством по созданию расширений](./guides/creating-an-extension.md) для получения сведений о том, как создать первое расширение браузера.</span><span class="sxs-lookup"><span data-stu-id="df18a-109">Check out our [guide on how to create extensions](./guides/creating-an-extension.md) for information on how to build your first browser extension!</span></span> 
- <span data-ttu-id="df18a-110">Уже знакомы с API расширения?</span><span class="sxs-lookup"><span data-stu-id="df18a-110">Already familiar with extension APIs?</span></span> <span data-ttu-id="df18a-111">Ознакомьтесь с [документацией по поддержке API](./api-support.md) , чтобы получить последние сведения о поддерживаемых и разрабатываемых API-интерфейсах.</span><span class="sxs-lookup"><span data-stu-id="df18a-111">Check out our [API support documentation](./api-support.md) for the latest info on which APIs are supported/in development.</span></span> 
- <span data-ttu-id="df18a-112">У вас есть расширение Chrome, которое вы хотите перенести в Microsoft Edge?</span><span class="sxs-lookup"><span data-stu-id="df18a-112">Have a Chrome extension that you want to port to Microsoft Edge?</span></span> <span data-ttu-id="df18a-113">Попробуйте [набор средств расширения Microsoft Edge](./guides/porting-chrome-extensions.md)!</span><span class="sxs-lookup"><span data-stu-id="df18a-113">Try the [Microsoft Edge Extension Toolkit](./guides/porting-chrome-extensions.md)!</span></span>

## <span data-ttu-id="df18a-114">Загрузка и отладка</span><span class="sxs-lookup"><span data-stu-id="df18a-114">Loading and debugging</span></span>

<span data-ttu-id="df18a-115">Если у вас есть расширение, работающее в Microsoft EDGE, вы захотите загрузить его, чтобы он отображался в действии.</span><span class="sxs-lookup"><span data-stu-id="df18a-115">Once you have an extension that works in Microsoft Edge, you'll want to side load it to see it in action.</span></span> <span data-ttu-id="df18a-116">Для этого сначала необходимо убедиться в том, что у вас есть [функции разработчика расширений](./guides/adding-and-removing-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="df18a-116">The first step to do this is to ensure that you have [extension developer features enabled](./guides/adding-and-removing-extensions.md).</span></span> <span data-ttu-id="df18a-117">Это позволит вам загрузить файлы расширения в Microsoft EDGE, чтобы можно было протестировать расширение при разработке.</span><span class="sxs-lookup"><span data-stu-id="df18a-117">This will allow you to side load extension files in Microsoft Edge so that you can test your extension while developing it.</span></span> <span data-ttu-id="df18a-118">Если вы столкнулись с проблемами, средства разработчика F12 разрешают [отладку различных контекстов расширения](./guides/debugging-extensions.md) , чтобы точно определить, что происходит.</span><span class="sxs-lookup"><span data-stu-id="df18a-118">Should you run into any issues, the F12 developer tools allow you to [debug the various contexts of your extension](./guides/debugging-extensions.md) to determine exactly what's going on.</span></span> <span data-ttu-id="df18a-119">Все еще используете проблемы?</span><span class="sxs-lookup"><span data-stu-id="df18a-119">Still running into issues?</span></span> <span data-ttu-id="df18a-120">В [руководстве по устранению неполадок описаны](./troubleshooting.md) некоторые распространенные проблемы.</span><span class="sxs-lookup"><span data-stu-id="df18a-120">Our [troubleshooting guide](./troubleshooting.md) has solutions to several common gotchas.</span></span> 

## <span data-ttu-id="df18a-121">Сообщения об ошибках и Справка</span><span class="sxs-lookup"><span data-stu-id="df18a-121">Reporting bugs and getting help</span></span>

<span data-ttu-id="df18a-122">Считаете, что в нашей платформе расширений обнаружена ошибка?</span><span class="sxs-lookup"><span data-stu-id="df18a-122">Think you've found a bug in our extensions platform?</span></span> <span data-ttu-id="df18a-123">Если эта неполадка связана с Microsoft EDGE, выполните поиск по ее вопросу в [Microsoft Edge Tracker](https://developer.microsoft.com/microsoft-edge/platform/issues/) , чтобы узнать, не было ли оно отправлено.</span><span class="sxs-lookup"><span data-stu-id="df18a-123">If the issue is specific to Microsoft Edge, please search for it on our [Microsoft Edge Issue Tracker](https://developer.microsoft.com/microsoft-edge/platform/issues/) to see if it's already been reported.</span></span> <span data-ttu-id="df18a-124">Если это так, очень удобно!</span><span class="sxs-lookup"><span data-stu-id="df18a-124">If it has, great!</span></span> <span data-ttu-id="df18a-125">Вы можете нажать кнопку "+ я не слишком много", чтобы отследить ошибку и нажать кнопку "наблюдать за обновлениям", чтобы получать уведомления об изменениях, внесенных в вопрос.</span><span class="sxs-lookup"><span data-stu-id="df18a-125">You can press the "+ Me too" button to upvote the bug and the "Watch this issue for updates" button to be alerted to any changes on the issue.</span></span> <span data-ttu-id="df18a-126">Если вы не можете найти проблем, с которыми вы столкнулись, вы можете открыть новую ошибку и получить как можно более подробную информацию, чтобы наши разработчики могли найти его.</span><span class="sxs-lookup"><span data-stu-id="df18a-126">If you can't find the issue you're running into, feel free to open a new issue and provide as much information as possible so our developers can look into it.</span></span> 

<span data-ttu-id="df18a-127">У нас нет API-интерфейса, который требуется для правильной работы вашего расширения?</span><span class="sxs-lookup"><span data-stu-id="df18a-127">Are we missing an API that your extension needs to work properly?</span></span> <span data-ttu-id="df18a-128">Если да, [мы всегда отслеживаемся UserVoice](https://wpdev.uservoice.com/forums/257854-microsoft-edge-developer/category/87962-extensions).</span><span class="sxs-lookup"><span data-stu-id="df18a-128">If so, [we're always listening on UserVoice](https://wpdev.uservoice.com/forums/257854-microsoft-edge-developer/category/87962-extensions).</span></span> <span data-ttu-id="df18a-129">Вы можете спокойно проголосовать за ваш API, если он уже существует, или создать новый элемент отзыва, чтобы другие разработчики могли его проголосовать!</span><span class="sxs-lookup"><span data-stu-id="df18a-129">Feel free to upvote your API if it already exists, or to create a new feedback item so that other developers can upvote it too!</span></span> 

<span data-ttu-id="df18a-130">У вас есть вопрос о том, что вы не можете найти ответ в документации?</span><span class="sxs-lookup"><span data-stu-id="df18a-130">Do you have a question that you can't find an answer to in the documentation?</span></span> <span data-ttu-id="df18a-131">Мы настоятельно рекомендуем присоединиться к [сообществу расширений Microsoft Edge](https://stackoverflow.com/questions/tagged/microsoft-edge-extension) в области переполнения стека и попросить его!</span><span class="sxs-lookup"><span data-stu-id="df18a-131">We strongly recommend you join the [Microsoft Edge Extensions community](https://stackoverflow.com/questions/tagged/microsoft-edge-extension) on Stack Overflow and ask it there!</span></span>

## <span data-ttu-id="df18a-132">Проверка расширения</span><span class="sxs-lookup"><span data-stu-id="df18a-132">Testing your extension</span></span>

<span data-ttu-id="df18a-133">По мере обновления годовщины Windows [веб – дисковод Microsoft](../dev-guide/tools/webdriver.md) поддерживает автоматическую загрузку расширений в сеансах Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="df18a-133">As of the Windows Anniversary Update, [Microsoft WebDriver](../dev-guide/tools/webdriver.md) supports the automated side loading of extensions in Microsoft Edge sessions.</span></span> <span data-ttu-id="df18a-134">Это позволит вам создавать простые тесты, чтобы гарантировать, что любое расширение, предназначенное для изменения страницы, выполняется так, как ожидалось.</span><span class="sxs-lookup"><span data-stu-id="df18a-134">This will allow you to write simple tests to ensure that any extension that is meant to modify a page does so in the expected manner.</span></span> <span data-ttu-id="df18a-135">Дополнительные сведения о том, как это сделать, можно найти в [руководстве по тестированию](./guides/packaging/creating-and-testing-extension-packages.md#automated-testing-with-webdriver).</span><span class="sxs-lookup"><span data-stu-id="df18a-135">You can find more info on how to do this in our [testing guide](./guides/packaging/creating-and-testing-extension-packages.md#automated-testing-with-webdriver).</span></span> <span data-ttu-id="df18a-136">Кроме того, вы можете настроить обновления так, как мы планируем добавить в будущем дополнительные функции расширения для Microsoft.</span><span class="sxs-lookup"><span data-stu-id="df18a-136">Also, stay tuned for updates as we plan to add more extension-specific features to Microsoft WebDriver in the future.</span></span>

## <span data-ttu-id="df18a-137">Добавление заключительных касаний</span><span class="sxs-lookup"><span data-stu-id="df18a-137">Adding the final touches</span></span>

<span data-ttu-id="df18a-138">Так что ваше расширение работает в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="df18a-138">So your extension works in Microsoft Edge.</span></span> <span data-ttu-id="df18a-139">Что дальше?</span><span class="sxs-lookup"><span data-stu-id="df18a-139">What happens next?</span></span> <span data-ttu-id="df18a-140">Перед тем как продолжить упаковку расширения, мы настоятельно рекомендуем ознакомиться с приведенными ниже рекомендациями, чтобы убедиться в том, что расширение задается на наилучших практических политиках.</span><span class="sxs-lookup"><span data-stu-id="df18a-140">Before you continue packaging your extension, we strongly recommend you to check out these guides to ensure that your extension is following our best-practice policies:</span></span> 
- <span data-ttu-id="df18a-141">Убедитесь, что значки расширений [правильно](./guides/design.md) изменяются и [доступны](./guides/accessibility.md) (это означает, что они видны как светлые, так и темные темы Microsoft EDGE, а также в режиме высокой контрастности).</span><span class="sxs-lookup"><span data-stu-id="df18a-141">Make sure your extension icons are [correctly sized](./guides/design.md) and [accessible](./guides/accessibility.md) (meaning they're visible in both light and dark themes of Microsoft Edge as well as in high contrast mode).</span></span> 
- <span data-ttu-id="df18a-142">Если ваше расширение должно поддерживать несколько языков, убедитесь в том, что вы просмотрии [руководство по интернационализации](./guides/internationalization.md).</span><span class="sxs-lookup"><span data-stu-id="df18a-142">If your extension needs to support multiple languages, please make sure you've taken a look over our [internationalization guide](./guides/internationalization.md).</span></span> 

## <span data-ttu-id="df18a-143">Упаковка расширения</span><span class="sxs-lookup"><span data-stu-id="df18a-143">Packaging an extension</span></span>

<span data-ttu-id="df18a-144">Теперь ваше расширение, наконец, будет готово к упаковке.</span><span class="sxs-lookup"><span data-stu-id="df18a-144">Now your extension is finally polished up and ready to be packaged.</span></span> <span data-ttu-id="df18a-145">Если вы собираетесь упаковать ее для подготовки к отправке в Microsoft Store или для упрощения ее распространения в рамках групп разработки и тестирования, существует множество ресурсов, с помощью которых можно сделать следующее:</span><span class="sxs-lookup"><span data-stu-id="df18a-145">Whether you wish to package it to prepare for submission to the Microsoft Store, or to make it easier to distribute within your development/testing teams, there are plenty of resources available to help you:</span></span> 

- <span data-ttu-id="df18a-146">Рекомендуемое решение для создания пакета расширения — подписаться на наше руководство по комплекту [ManifoldJS](./guides/packaging/using-manifoldjs-to-package-extensions.md) , которое поможет вам пройти шаги по использованию средства на основе файла Node. js для быстрого создания расширения независимо от того, на какой платформе вы разрабатываете.</span><span class="sxs-lookup"><span data-stu-id="df18a-146">Our recommended solution for creating an extension package is to follow our [ManifoldJS packaging guide](./guides/packaging/using-manifoldjs-to-package-extensions.md) which will walk you through the steps of using a Node.js based tool to easily package your extension no matter what platform you develop on.</span></span> <span data-ttu-id="df18a-147">Если вам нужна более подробная информация о том, как ознакомиться с нашим форматом добавочных упаковок, ознакомьтесь с [руководством по созданию пакета Appx](./guides/packaging/creating-and-testing-extension-packages.md#preparing-the-submission-folder).</span><span class="sxs-lookup"><span data-stu-id="df18a-147">If you want a more manual and in-depth look into our extension packaging format, please refer to our [AppX package creation guide](./guides/packaging/creating-and-testing-extension-packages.md#preparing-the-submission-folder).</span></span> 
- <span data-ttu-id="df18a-148">Если ваше расширение поддерживает несколько языков, вам также потребуется выполнить наше руководство по [локализации пакетов расширений](./guides/packaging/localizing-extension-packages.md) таким образом, чтобы языки, которые вы используете в расширении, правильно регистрировались после упаковки.</span><span class="sxs-lookup"><span data-stu-id="df18a-148">If your extension supports multiple languages, you'll also need to follow our guide on [localizing extension packages](./guides/packaging/localizing-extension-packages.md) so that the languages you have in your extension are correctly registered after packaging.</span></span> 

<span data-ttu-id="df18a-149">Если вы являетесь корпоративным клиентом, которым требуется распространить Упакованные расширения по внутренним каналам, ознакомьтесь с разрешениями [для руководства по расширениям для предприятий](./extensions-for-enterprise.md) , чтобы узнать, как это сделать.</span><span class="sxs-lookup"><span data-stu-id="df18a-149">If you're an enterprise customer looking to distribute your packaged extensions via internal channels, please see our [extensions for enterprise guide](./extensions-for-enterprise.md) to see how to do this.</span></span>  

## <span data-ttu-id="df18a-150">Публикация в Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="df18a-150">Publishing to the Microsoft Store</span></span>

<span data-ttu-id="df18a-151">Так как наша платформа расширений по-прежнему остается на своем деле, мы решили управлять отправкой расширений в Microsoft Store, чтобы мы могли сосредоточиться на предоставлении качества для наших пользователей и разработчиков.</span><span class="sxs-lookup"><span data-stu-id="df18a-151">Since our extensions platform is still in its infancy, we're purposely managing extension submissions to the Microsoft Store so that we can focus on delivering a quality experience for our users and developers.</span></span> <span data-ttu-id="df18a-152">С другой стороны, мы хотели бы сделать так, чтобы разработчикам было проще публиковать свои расширения.</span><span class="sxs-lookup"><span data-stu-id="df18a-152">That being said, we want to make it as easy as possible for developers to publish their extensions.</span></span> <span data-ttu-id="df18a-153">В результате мы недавно запустили новую [форму отправки расширений](https://aka.ms/extension-request) , в которой разработчики могут запросить разрешение на отправку расширения appx в Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="df18a-153">As a result, we have recently launched a new [extension submission form](https://aka.ms/extension-request) where developers can request permission to submit their extension AppX to the Microsoft Store.</span></span>
 

<span data-ttu-id="df18a-154">Первый шаг процесса публикации — убедиться, что расширение соответствует [политике расширения браузера](./microsoft-browser-extension-policy.md) , а также [разделу "расширения Microsoft Edge" политик Microsoft Store](https://msdn.microsoft.com/library/windows/apps/dn764944.aspx#pol_10_12).</span><span class="sxs-lookup"><span data-stu-id="df18a-154">The first step of the publishing process is to make sure your extension conforms to our [browser extension policy](./microsoft-browser-extension-policy.md) as well as the [Microsoft Edge extensions section of the Microsoft Store Policies](https://msdn.microsoft.com/library/windows/apps/dn764944.aspx#pol_10_12).</span></span> 

<span data-ttu-id="df18a-155">После подтверждения того, что расширение следует за политиками, вам нужно будет зарегистрироваться для получения [учетной записи разработчика в центре партнера и зарезервировать имя расширения](./guides/packaging/extensions-in-the-windows-dev-center.md).</span><span class="sxs-lookup"><span data-stu-id="df18a-155">Once you've confirmed that your extension follows the policies, you will need to register for a [developer account in Partner Center and reserve the name of your extension](./guides/packaging/extensions-in-the-windows-dev-center.md).</span></span> <span data-ttu-id="df18a-156">Затем, чтобы запросить разрешение на публикацию в Microsoft Store, вам потребуется отправить запрос через [форму отправки расширения](https://aka.ms/extension-request) .</span><span class="sxs-lookup"><span data-stu-id="df18a-156">Then, you'll need to submit a request via our [extension submission form](https://aka.ms/extension-request) in order to request permission to publish to the Microsoft Store.</span></span> <span data-ttu-id="df18a-157">При попытке отправить расширение AppX без предварительного получения разрешения появляется следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="df18a-157">If you try to submit your extension AppX without first obtaining permission, you'll receive the following error:</span></span>

`Package acceptance validation error: com.microsoft.edge.extension is a reserved extension type. Your app does not have permission to use this extension type.`

<span data-ttu-id="df18a-158">После того как вы отправили запрос, мы получим уведомление и попытаемся получить отправку, как только это станет возможным.</span><span class="sxs-lookup"><span data-stu-id="df18a-158">Once you've submitted a request, we'll receive a notification and will try to get to your submission as soon as possible.</span></span> <span data-ttu-id="df18a-159">Это может занять некоторое время из-за того, что вы получили большое количество отправленных данных, но мы свяжемся с вами по электронной почте.</span><span class="sxs-lookup"><span data-stu-id="df18a-159">This may take a bit due to the high volume of submissions we've received, but we'll notify you via email the moment you're approved!</span></span> <span data-ttu-id="df18a-160">После получения почты вы сможете отправить расширение AppX в Microsoft Store через центр партнеров.</span><span class="sxs-lookup"><span data-stu-id="df18a-160">Once you've received the mail, you'll be able to submit your extension AppX to the Microsoft Store via Partner Center.</span></span> <span data-ttu-id="df18a-161">Обратите внимание на то, что вы не должны подписыватье AppX, прежде чем отправлять его; процесс приема данных в магазине Майкрософт поможет вам сделать это.</span><span class="sxs-lookup"><span data-stu-id="df18a-161">Please note that you do not have to sign your AppX before submitting it; the Microsoft Store ingestion process will take care of that for you!</span></span>
 
> [!NOTE]
> <span data-ttu-id="df18a-162">Процесс публикации расширения в магазине Microsoft Store (это новое расширение или обновление уже существующей) может занять до 72 часов.</span><span class="sxs-lookup"><span data-stu-id="df18a-162">The process for publishing an extension to the Microsoft Store (whether it's a brand new extension or an update to an existing one) can take up to 72 hours to complete.</span></span> <span data-ttu-id="df18a-163">Чтобы ускорить этот процесс, убедитесь, что вы проверили эти распространенные проблемы перед отправкой, чтобы избежать необходимости повторной отправки.</span><span class="sxs-lookup"><span data-stu-id="df18a-163">In order to expedite this process, please ensure you have verified these common gotchas before submitting to avoid having to resubmit later:</span></span> 
> - <span data-ttu-id="df18a-164">Ваши снимки экрана имеют правильный размер и имеют расширение, работающее в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="df18a-164">Your screenshots are correctly sized and are of your extension running in Microsoft Edge</span></span> 
> - <span data-ttu-id="df18a-165">Описание расширения ссылается на "Microsoft Edge", а не на "Edge" (это легальное требование)</span><span class="sxs-lookup"><span data-stu-id="df18a-165">Your extension description references "Microsoft Edge" instead of "Edge" (this is a legal requirement)</span></span> 
> - <span data-ttu-id="df18a-166">У значка 150x150 в пакете расширения нет [прозрачного фона](./guides/design.md#microsoft-store-icon) (в клиенте Microsoft Store неправильно отображаются изображения с прозрачными фоновыми рисунками).</span><span class="sxs-lookup"><span data-stu-id="df18a-166">Your 150x150 icon in your extension package [does not have a transparent background](./guides/design.md#microsoft-store-icon) (The Microsoft Store client does not correctly render images with transparent backgrounds)</span></span> 

<span data-ttu-id="df18a-167">Помимо описанных выше, и, если это применимо, убедитесь в том, что на вашем веб-сайте сведения о доступности вашей платформы правильно упоминаются о доступности расширения в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="df18a-167">In addition to the above, and if applicable, please ensure that any platform availability information on your website correctly mentions your extension's availability on Microsoft Edge.</span></span> <span data-ttu-id="df18a-168">Несмотря на то, что в Microsoft Store не разрешается использовать одновременную установку встроенного расширения, вы можете добавить [глубокую ссылку на расширение в Microsoft Store](./tips-and-tricks.md#get-a-direct-link-to-your-extension-in-the-microsoft-store) , чтобы пользователи могли легко получить его.</span><span class="sxs-lookup"><span data-stu-id="df18a-168">While the Microsoft Store does not allow for one-click inline extension installs, you can [deep-link to your extension in the Microsoft Store](./tips-and-tricks.md#get-a-direct-link-to-your-extension-in-the-microsoft-store) to make it easy for users to acquire it.</span></span> 

<span data-ttu-id="df18a-169">Кроме того, Microsoft Store позволяет [управлять отображением расширения](https://blogs.windows.com/buildingapps/2015/09/10/managing-hidden-apps-beta-apps-and-visibility-of-in-app-purchases-in-dev-center/) в каталоге Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="df18a-169">The Microsoft Store also allows you to [control the visibility of your extension](https://blogs.windows.com/buildingapps/2015/09/10/managing-hidden-apps-beta-apps-and-visibility-of-in-app-purchases-in-dev-center/) in the Microsoft Store catalog.</span></span> <span data-ttu-id="df18a-170">Некоторые из наших партнеров пользовались следующими возможностями для достижения следующих целей:</span><span class="sxs-lookup"><span data-stu-id="df18a-170">Some of our partners have taken advantage of this functionality to achieve the following:</span></span> 
- <span data-ttu-id="df18a-171">Публикация второй бета-версии расширения в формате, скрытом в Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="df18a-171">Publishing a second beta version of their extension as hidden in the Microsoft Store.</span></span>
- <span data-ttu-id="df18a-172">Первоначально публикуют свое расширение как скрытое для отслеживания первоначальной телеметрии перед изменением состояния на Visible, пока не будет достигнут определенный уровень достоверности.</span><span class="sxs-lookup"><span data-stu-id="df18a-172">Initially publishing their extension as hidden to monitor initial telemetry before eventually changing its status to visible once a certain level of confidence is reached.</span></span>

## <span data-ttu-id="df18a-173">Вот и все!</span><span class="sxs-lookup"><span data-stu-id="df18a-173">That's it!</span></span>

<span data-ttu-id="df18a-174">Если вы достигли нижней части этого руководства, вы завершили процесс разработки расширения для Microsoft Edge!</span><span class="sxs-lookup"><span data-stu-id="df18a-174">If you've reached the bottom of this guide, you've completed the process of developing an extension for Microsoft Edge!</span></span> <span data-ttu-id="df18a-175">Не забудьте ознакомиться с [советами и рекомендациями](./tips-and-tricks.md) о том, как рекламировать свое расширение и взаимодействовать с пользователями.</span><span class="sxs-lookup"><span data-stu-id="df18a-175">Be sure to check out our [tips and tricks](./tips-and-tricks.md) page for ideas on how to market your extension and interact with your users.</span></span>