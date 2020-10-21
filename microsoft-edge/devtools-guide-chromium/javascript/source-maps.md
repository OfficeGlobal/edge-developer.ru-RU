---
description: Код на стороне клиента будет читаемым и отлаженным даже после того, как вы объедините, minify или компилируете его.
title: Сопоставление предварительно обработанного кода с исходным кодом
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: c16f59658217ab9dfb905bd814f96af21f95130d
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "11124685"
---
<!-- Copyright Meggin Kearney and Paul Bakaus

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  

# <span data-ttu-id="dde6a-104">Сопоставление предварительно обработанного кода с исходным кодом</span><span class="sxs-lookup"><span data-stu-id="dde6a-104">Map preprocessed code to source code</span></span>  

<span data-ttu-id="dde6a-105">Код на стороне клиента будет читаемым и отлаженным даже после того, как вы объедините, minify или компилируете его.</span><span class="sxs-lookup"><span data-stu-id="dde6a-105">Keep your client-side code readable and debuggable even after you combine, minify, or compile it.</span></span>  <span data-ttu-id="dde6a-106">С помощью карт исходного кода сопоставьте исходный код с скомпилированным кодом.</span><span class="sxs-lookup"><span data-stu-id="dde6a-106">Use source maps to map your source code to your compiled code.</span></span>  

### <span data-ttu-id="dde6a-107">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="dde6a-107">Summary</span></span>  

*   <span data-ttu-id="dde6a-108">С помощью карт исходного кода сопоставьте minified код с исходным кодом.</span><span class="sxs-lookup"><span data-stu-id="dde6a-108">Use Source Maps to map minified code to source code.</span></span> <span data-ttu-id="dde6a-109">После этого вы сможете прочитать и отладить скомпилированный код в исходном источнике.</span><span class="sxs-lookup"><span data-stu-id="dde6a-109">You are then able to read and debug compiled code in the original source.</span></span>  
*   <span data-ttu-id="dde6a-110">Используйте только предварительные процессоры с возможностью создания карт исходного кода.</span><span class="sxs-lookup"><span data-stu-id="dde6a-110">Only use pre-processors capable of producing Source Maps.</span></span>  
*   <span data-ttu-id="dde6a-111">Убедитесь в том, что веб-сервер может служить исходными картами.</span><span class="sxs-lookup"><span data-stu-id="dde6a-111">Verify that your web server is able to serve Source Maps.</span></span>  
    
<!--todo: add link to preprocessors capable of producing Source Maps when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors?#supported_preprocessors ""  -->  

## <span data-ttu-id="dde6a-112">Приступая к работе с препроцессорами</span><span class="sxs-lookup"><span data-stu-id="dde6a-112">Get started with preprocessors</span></span>  

<span data-ttu-id="dde6a-113">В этой статье объясняется, как взаимодействовать с исходными картами JavaScript на панели "DevTools источники".</span><span class="sxs-lookup"><span data-stu-id="dde6a-113">This article explains how to interact with JavaScript Source Maps in the DevTools Sources Panel.</span></span>  <!--For a first overview of what preprocessors are, how each may help, and how Source Maps work; see Set Up CSS & JS Preprocessors.  -->  

<!--todo: add link to Set Up CSS & JS Preprocessors when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors#debugging-and-editing-preprocessed-content ""  -->  

## <span data-ttu-id="dde6a-114">Использование поддерживаемой предварительной обработки</span><span class="sxs-lookup"><span data-stu-id="dde6a-114">Use a supported preprocessor</span></span>  

<span data-ttu-id="dde6a-115">Вам необходимо использовать Minifier, который способен создавать карты исходного кода.</span><span class="sxs-lookup"><span data-stu-id="dde6a-115">You need to use a minifier that is capable of creating source maps.</span></span>  <!--For the most popular options, navigate to preprocessor support section.  -->  <span data-ttu-id="dde6a-116">Для расширенного представления перейдите к [исходным картам: языки, инструменты и другие информационные][GitHubWikiSourceMapsLanguagesTools] вики-страницы.</span><span class="sxs-lookup"><span data-stu-id="dde6a-116">For an extended view, navigate to [Source maps: languages, tools and other info][GitHubWikiSourceMapsLanguagesTools] wiki page.</span></span>  

<!--todo: add link to see the preprocessor support section when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors?#supported_preprocessors ""  -->  

<span data-ttu-id="dde6a-117">В сочетании с исходными картами обычно используются следующие типы предварительной обработки:</span><span class="sxs-lookup"><span data-stu-id="dde6a-117">The following types of preprocessors are commonly used in combination with Source Maps:</span></span>  

*   <span data-ttu-id="dde6a-118">Transpilers \ ([Babel][BabelJS], [Traceur][GitHubWikiGoogleTraceurCompiler]\)</span><span class="sxs-lookup"><span data-stu-id="dde6a-118">Transpilers \([Babel][BabelJS], [Traceur][GitHubWikiGoogleTraceurCompiler]\)</span></span>  
*   <span data-ttu-id="dde6a-119">Компиляторы \ ([компилятор замыканий][GitHubGoogleClosureCompiler], [TypeScript][|::ref1::|Main], [CoffeeScript][|::ref2::|Main], [DART][DartMain]\)</span><span class="sxs-lookup"><span data-stu-id="dde6a-119">Compilers \([Closure Compiler][GitHubGoogleClosureCompiler], [TypeScript][|::ref1::|Main], [CoffeeScript][|::ref2::|Main], [Dart][DartMain]\)</span></span>  
*   <span data-ttu-id="dde6a-120">Minifiers \ ([UglifyJS][GitHubMishooUglifyJS]\)</span><span class="sxs-lookup"><span data-stu-id="dde6a-120">Minifiers \([UglifyJS][GitHubMishooUglifyJS]\)</span></span>  
    
## <span data-ttu-id="dde6a-121">Карты исходного кода на панели «источники DevTools»</span><span class="sxs-lookup"><span data-stu-id="dde6a-121">Source Maps in DevTools Sources panel</span></span>  

<span data-ttu-id="dde6a-122">Карты исходного кода из предварительной обработки заставляют DevTools загрузить исходные файлы в дополнение к minified.</span><span class="sxs-lookup"><span data-stu-id="dde6a-122">Source Maps from preprocessors cause DevTools to load your original files in addition to your minified ones.</span></span>  <span data-ttu-id="dde6a-123">Затем вы можете использовать оригиналы для задания точек останова и пошагового кода.</span><span class="sxs-lookup"><span data-stu-id="dde6a-123">You then use the originals to set breakpoints and step through code.</span></span>  <span data-ttu-id="dde6a-124">В то же время Microsoft EDGE на самом деле выполняет minified код.</span><span class="sxs-lookup"><span data-stu-id="dde6a-124">Meanwhile, Microsoft Edge is actually running your minified code.</span></span> <span data-ttu-id="dde6a-125">Это дает вам иллюзию запуска сайта разработки в рабочей среде.</span><span class="sxs-lookup"><span data-stu-id="dde6a-125">This gives you the illusion of running a development site in production.</span></span>  

<span data-ttu-id="dde6a-126">При запуске карт исходного кода в DevTools следует обратить внимание на то, что JavaScript не скомпилирован и вы можете просматривать все отдельные файлы JavaScript, на которые он ссылается.</span><span class="sxs-lookup"><span data-stu-id="dde6a-126">When running Source Maps in DevTools, you should notice that the JavaScript is not compiled and you are able to see all the individual JavaScript files it references.</span></span>  <span data-ttu-id="dde6a-127">Используется сопоставление источника, но в фоновом режиме фактически запускается скомпилированный код.</span><span class="sxs-lookup"><span data-stu-id="dde6a-127">This is using source mapping, but behind the scenes actually runs the compiled code.</span></span>  <span data-ttu-id="dde6a-128">Любые ошибки, журналы и точки останова сопоставлены с кодом разработки для Awesome Debugging!</span><span class="sxs-lookup"><span data-stu-id="dde6a-128">Any errors, logs, and breakpoints map to the dev code for awesome debugging!</span></span>  <span data-ttu-id="dde6a-129">Таким образом, это дает впечатление, что вы используете сайт разработчика в производстве.</span><span class="sxs-lookup"><span data-stu-id="dde6a-129">So in effect it gives you the illusion that you are running a dev site in production.</span></span>  

### <span data-ttu-id="dde6a-130">Включение карт исходного кода в параметрах</span><span class="sxs-lookup"><span data-stu-id="dde6a-130">Enable Source Maps in settings</span></span>  

<span data-ttu-id="dde6a-131">Исходные карты включены по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="dde6a-131">Source Maps are enabled by default</span></span> <!--\(as of Microsoft Edge 39\)--><span data-ttu-id="dde6a-132">, но если вы хотите дважды проверить или включить их; Сначала откройте DevTools, нажмите кнопку **Настройка и управление DevTools** \ ( `...` \) и выберите пункт **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="dde6a-132">, but if you want to double-check or enable them; first open DevTools, click the **Customize and control DevTools** \(`...`\) button, and choose **Settings**.</span></span>  <span data-ttu-id="dde6a-133">В области **Параметры** в разделе **источники**установите флажок **включить сопоставления источников JavaScript**.</span><span class="sxs-lookup"><span data-stu-id="dde6a-133">On the **Preferences** pane, under **Sources**, check **Enable JavaScript Source Maps**.</span></span>  <span data-ttu-id="dde6a-134">Вы также можете установить флажок **включить сопоставления источников CSS**.</span><span class="sxs-lookup"><span data-stu-id="dde6a-134">You may also check **Enable CSS Source Maps**.</span></span>  

:::image type="complex" source="../media/javascript-settings-preferences-sources-enable-javascript-source-maps.msft.png" alt-text="Включение карт исходного кода" lightbox="../media/javascript-settings-preferences-sources-enable-javascript-source-maps.msft.png":::
   **<span data-ttu-id="dde6a-136">Включение карт исходного кода JavaScript</span><span class="sxs-lookup"><span data-stu-id="dde6a-136">Enable JavaScript Source Maps</span></span>**  
:::image-end:::  

### <span data-ttu-id="dde6a-137">Отладка с помощью карт исходного кода</span><span class="sxs-lookup"><span data-stu-id="dde6a-137">Debugging with Source Maps</span></span>  

<span data-ttu-id="dde6a-138">При включении отладки кода и сопоставления источников отображаются два места.</span><span class="sxs-lookup"><span data-stu-id="dde6a-138">When debugging your code and Source Maps enabled, Source Maps show in two places:</span></span>  

1.  <span data-ttu-id="dde6a-139">На консоли \ (ссылка на источник — это исходный файл, а не созданный).</span><span class="sxs-lookup"><span data-stu-id="dde6a-139">In the console \(the link to source should be the original file, not the generated one\)</span></span>  
1.  <span data-ttu-id="dde6a-140">При пошаговом выполнении кода \ (ссылки в стеке вызовов должны открыть исходный исходный файл)</span><span class="sxs-lookup"><span data-stu-id="dde6a-140">When stepping through code \(the links in the call stack should open the original source file\)</span></span>  
    
<!--todo: add link to debugging your code when section is available -->  
<!--[DebugBreakpointsStepCode]: ../debug/breakpoints/step-code.md ""  -->  

## <span data-ttu-id="dde6a-141">@sourceURL и displayName</span><span class="sxs-lookup"><span data-stu-id="dde6a-141">@sourceURL and displayName</span></span>  

<span data-ttu-id="dde6a-142">Несмотря на то, что она не входит в спецификацию карты источника, она `@sourceURL` позволяет упростить разработку при работе с evalами.</span><span class="sxs-lookup"><span data-stu-id="dde6a-142">While not part of the Source Map spec, the `@sourceURL` allows you to make development much easier when working with evals.</span></span>  <span data-ttu-id="dde6a-143">Этот вспомогательный элемент выглядит очень похож на `//# sourceMappingURL` свойство и на самом деле упоминается в спецификации исходной карты v3.</span><span class="sxs-lookup"><span data-stu-id="dde6a-143">This helper looks very similar to the `//# sourceMappingURL` property and is actually mentioned in the Source Map V3 specifications.</span></span>  

<span data-ttu-id="dde6a-144">Включив в код следующее специальное примечание, которое будет вычислено, вы можете присвоить именам и встроенным сценариям и стилям, чтобы они отображались в DevTools с более логичными именами.</span><span class="sxs-lookup"><span data-stu-id="dde6a-144">By including the following special comment in your code, which is be evaled, you are able to name evals and inline scripts and styles so each appears as more logical names in your DevTools.</span></span>  

```javascript
//# sourceURL=source.coffee
```  

<span data-ttu-id="dde6a-145">Перейдите на следующую страницу.</span><span class="sxs-lookup"><span data-stu-id="dde6a-145">Navigate to the following page.</span></span>  

*   [<span data-ttu-id="dde6a-146">ролик</span><span class="sxs-lookup"><span data-stu-id="dde6a-146">demo</span></span>][CssNinjaDemoSourceMapping]

<span data-ttu-id="dde6a-147">Выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="dde6a-147">Complete the following actions.</span></span>  

1.  <span data-ttu-id="dde6a-148">Откройте DevTools и перейдите на панель " **источники** ".</span><span class="sxs-lookup"><span data-stu-id="dde6a-148">Open the DevTools and go to the **Sources** panel.</span></span>  
1.  <span data-ttu-id="dde6a-149">Введите имя файла в поле **код:** input.</span><span class="sxs-lookup"><span data-stu-id="dde6a-149">Enter in a filename into the **Name your code:** input field.</span></span>  
1.  <span data-ttu-id="dde6a-150">Нажмите кнопку **Compile (компилировать** ).</span><span class="sxs-lookup"><span data-stu-id="dde6a-150">Click on the **compile** button.</span></span>  
1.  <span data-ttu-id="dde6a-151">Появится предупреждение с вычисленной суммой из источника CoffeeScript.</span><span class="sxs-lookup"><span data-stu-id="dde6a-151">An alert appears with the evaluated sum from the CoffeeScript source.</span></span>  
    
<span data-ttu-id="dde6a-152">Если развернуть раздел **источники** , вы увидите новый файл с пользовательским именем, введенным ранее.</span><span class="sxs-lookup"><span data-stu-id="dde6a-152">If you expand the **Sources** sub-panel you now see a new file with the custom filename you entered earlier.</span></span>  <span data-ttu-id="dde6a-153">Если дважды щелкнуть для просмотра этого файла, он будет содержать скомпилированный код JavaScript для первоначального источника.</span><span class="sxs-lookup"><span data-stu-id="dde6a-153">If you double-click to view this file it contains the compiled JavaScript for the original source.</span></span>  <span data-ttu-id="dde6a-154">Однако в последней строке есть `// @sourceURL` Примечание, указывающее исходный исходный файл.</span><span class="sxs-lookup"><span data-stu-id="dde6a-154">On the last line, however, is a `// @sourceURL` comment indicating the original source file.</span></span>  <span data-ttu-id="dde6a-155">Это может помочь при отладке при работе с языковыми абстракциями.</span><span class="sxs-lookup"><span data-stu-id="dde6a-155">This may help you with debugging while working with language abstractions.</span></span>  

:::image type="complex" source="../media/javascript-sources-page-coffeeeeeeee.msft.png" alt-text="Включение карт исходного кода" lightbox="../media/javascript-sources-page-coffeeeeeeee.msft.png":::
   <span data-ttu-id="dde6a-157">Работа с</span><span class="sxs-lookup"><span data-stu-id="dde6a-157">Work with</span></span> `sourceURL`  
:::image-end:::  

## <span data-ttu-id="dde6a-158">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="dde6a-158">Getting in touch with the Microsoft Edge DevTools team</span></span>

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[BabelJS]: https://babeljs.io "Babel является компилятором JavaScript"  

[CoffeeScriptMain]: https://coffeescript.org "CoffeeScript"  

[CssNinjaDemoSourceMapping]: https://www.thecssninja.com/demo/source_mapping/compile.html "Простой пример имени//# sourceURL eval"  

[DartMain]: https://www.dartlang.org "Язык программирования DART"  

[GitHubGoogleClosureCompiler]: https://github.com/google/closure-compiler "Google/замыкание — компилятор | GitHub"  

[GitHubMishooUglifyJS]: https://github.com/mishoo/UglifyJS "mishoo/UglifyJS | GitHub"  

[GitHubWikiSourceMapsLanguagesTools]: https://github.com/ryanseddon/source-map/wiki/Source-maps:-languages,-tools-and-other-info "Карты исходного кода: языки, инструменты и другая информация | Вики-сайт GitHub"  

[GitHubWikiGoogleTraceurCompiler]: https://github.com/google/traceur-compiler/wiki/Getting-Started "Приступая к работе-"Google/traceur-Compiler | Вики-сайт GitHub"  

[TypeScriptMain]: https://www.typescriptlang.org "TypeScript"  

> [!NOTE]
> <span data-ttu-id="dde6a-168">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="dde6a-168">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="dde6a-169">Исходная страница размещается [здесь](https://developers.google.com/web/tools/chrome-devtools/javascript/source-maps) и разрабатывается с помощью [Meggin Kearney][MegginKearney] \ (технический писатель \) и [пола Bakaus][PaulBakaus] \ (Open Web Developer, Google: Tools, Performance, Animation и UX).</span><span class="sxs-lookup"><span data-stu-id="dde6a-169">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/source-maps) and is authored by [Meggin Kearney][MegginKearney] \(Tech Writer\) and [Paul Bakaus][PaulBakaus] \(Open Web Developer Advocate, Google: Tools, Performance, Animation, and UX\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="dde6a-171">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="dde6a-171">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
[PaulBakaus]: https://developers.google.com/web/resources/contributors/pbakaus  
