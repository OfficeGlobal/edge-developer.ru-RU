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

# Сопоставление предварительно обработанного кода с исходным кодом  

Код на стороне клиента будет читаемым и отлаженным даже после того, как вы объедините, minify или компилируете его.  С помощью карт исходного кода сопоставьте исходный код с скомпилированным кодом.  

### Краткий обзор  

*   С помощью карт исходного кода сопоставьте minified код с исходным кодом. После этого вы сможете прочитать и отладить скомпилированный код в исходном источнике.  
*   Используйте только предварительные процессоры с возможностью создания карт исходного кода.  
*   Убедитесь в том, что веб-сервер может служить исходными картами.  
    
<!--todo: add link to preprocessors capable of producing Source Maps when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors?#supported_preprocessors ""  -->  

## Приступая к работе с препроцессорами  

В этой статье объясняется, как взаимодействовать с исходными картами JavaScript на панели "DevTools источники".  <!--For a first overview of what preprocessors are, how each may help, and how Source Maps work; see Set Up CSS & JS Preprocessors.  -->  

<!--todo: add link to Set Up CSS & JS Preprocessors when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors#debugging-and-editing-preprocessed-content ""  -->  

## Использование поддерживаемой предварительной обработки  

Вам необходимо использовать Minifier, который способен создавать карты исходного кода.  <!--For the most popular options, navigate to preprocessor support section.  -->  Для расширенного представления перейдите к [исходным картам: языки, инструменты и другие информационные][GitHubWikiSourceMapsLanguagesTools] вики-страницы.  

<!--todo: add link to see the preprocessor support section when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors?#supported_preprocessors ""  -->  

В сочетании с исходными картами обычно используются следующие типы предварительной обработки:  

*   Transpilers \ ([Babel][BabelJS], [Traceur][GitHubWikiGoogleTraceurCompiler]\)  
*   Компиляторы \ ([компилятор замыканий][GitHubGoogleClosureCompiler], [TypeScript][|::ref1::|Main], [CoffeeScript][|::ref2::|Main], [DART][DartMain]\)  
*   Minifiers \ ([UglifyJS][GitHubMishooUglifyJS]\)  
    
## Карты исходного кода на панели «источники DevTools»  

Карты исходного кода из предварительной обработки заставляют DevTools загрузить исходные файлы в дополнение к minified.  Затем вы можете использовать оригиналы для задания точек останова и пошагового кода.  В то же время Microsoft EDGE на самом деле выполняет minified код. Это дает вам иллюзию запуска сайта разработки в рабочей среде.  

При запуске карт исходного кода в DevTools следует обратить внимание на то, что JavaScript не скомпилирован и вы можете просматривать все отдельные файлы JavaScript, на которые он ссылается.  Используется сопоставление источника, но в фоновом режиме фактически запускается скомпилированный код.  Любые ошибки, журналы и точки останова сопоставлены с кодом разработки для Awesome Debugging!  Таким образом, это дает впечатление, что вы используете сайт разработчика в производстве.  

### Включение карт исходного кода в параметрах  

Исходные карты включены по умолчанию. <!--\(as of Microsoft Edge 39\)-->, но если вы хотите дважды проверить или включить их; Сначала откройте DevTools, нажмите кнопку **Настройка и управление DevTools** \ ( `...` \) и выберите пункт **Параметры**.  В области **Параметры** в разделе **источники**установите флажок **включить сопоставления источников JavaScript**.  Вы также можете установить флажок **включить сопоставления источников CSS**.  

:::image type="complex" source="../media/javascript-settings-preferences-sources-enable-javascript-source-maps.msft.png" alt-text="Включение карт исходного кода" lightbox="../media/javascript-settings-preferences-sources-enable-javascript-source-maps.msft.png":::
   **Включение карт исходного кода JavaScript**  
:::image-end:::  

### Отладка с помощью карт исходного кода  

При включении отладки кода и сопоставления источников отображаются два места.  

1.  На консоли \ (ссылка на источник — это исходный файл, а не созданный).  
1.  При пошаговом выполнении кода \ (ссылки в стеке вызовов должны открыть исходный исходный файл)  
    
<!--todo: add link to debugging your code when section is available -->  
<!--[DebugBreakpointsStepCode]: ../debug/breakpoints/step-code.md ""  -->  

## @sourceURL и displayName  

Несмотря на то, что она не входит в спецификацию карты источника, она `@sourceURL` позволяет упростить разработку при работе с evalами.  Этот вспомогательный элемент выглядит очень похож на `//# sourceMappingURL` свойство и на самом деле упоминается в спецификации исходной карты v3.  

Включив в код следующее специальное примечание, которое будет вычислено, вы можете присвоить именам и встроенным сценариям и стилям, чтобы они отображались в DevTools с более логичными именами.  

```javascript
//# sourceURL=source.coffee
```  

Перейдите на следующую страницу.  

*   [ролик][CssNinjaDemoSourceMapping]

Выполните указанные ниже действия.  

1.  Откройте DevTools и перейдите на панель " **источники** ".  
1.  Введите имя файла в поле **код:** input.  
1.  Нажмите кнопку **Compile (компилировать** ).  
1.  Появится предупреждение с вычисленной суммой из источника CoffeeScript.  
    
Если развернуть раздел **источники** , вы увидите новый файл с пользовательским именем, введенным ранее.  Если дважды щелкнуть для просмотра этого файла, он будет содержать скомпилированный код JavaScript для первоначального источника.  Однако в последней строке есть `// @sourceURL` Примечание, указывающее исходный исходный файл.  Это может помочь при отладке при работе с языковыми абстракциями.  

:::image type="complex" source="../media/javascript-sources-page-coffeeeeeeee.msft.png" alt-text="Включение карт исходного кода" lightbox="../media/javascript-sources-page-coffeeeeeeee.msft.png":::
   Работа с `sourceURL`  
:::image-end:::  

## Взаимодействие с командой средств разработчика Microsoft Edge

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
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница размещается [здесь](https://developers.google.com/web/tools/chrome-devtools/javascript/source-maps) и разрабатывается с помощью [Meggin Kearney][MegginKearney] \ (технический писатель \) и [пола Bakaus][PaulBakaus] \ (Open Web Developer, Google: Tools, Performance, Animation и UX).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
[PaulBakaus]: https://developers.google.com/web/resources/contributors/pbakaus  
