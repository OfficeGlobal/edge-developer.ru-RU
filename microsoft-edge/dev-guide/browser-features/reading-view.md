---
ms.assetid: 2bc29371-4f2e-4b59-a588-30b107d751f6
description: Узнайте о том, как Microsoft Edge предлагает представление для чтения веб-страниц, позволяющее бесплатно читать дополнительные возможности чтения.
title: 'Руководство для разработчиков: режим чтения'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: EDGE, веб-разработка, HTML, CSS, JavaScript, разработчик
ms.openlocfilehash: e84edb5cc29b644939895f2996c50f3b4ec23379
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10570900"
---
# Режим чтения

Microsoft Edge предоставляет *представление для чтения* для более удобной работы с веб-страницами, так же как и без отзыва несвязанных или других вспомогательных материалов на странице. Режим чтения можно включить или отключить из **режима чтения** (значка книги) в **адресной строке** (или с помощью **сочетания клавиш CTRL**  +  **+**  +  **R**). В режиме чтения на странице извлекаются следующие метаданные:

* Title
* Созданные
* Дата
* Издатель
* Доминирующее изображение (-ов)
* Заголовки доминирующего изображения (-ов)
* Дополнительные изображения
* Основное текстовое содержимое страницы
* Авторские права

Пользователи могут настроить контрастность страницы и размер шрифта на панели " **Параметры** Microsoft Edge".

## Извлечение метаданных


Ниже приведены подробные сведения о метаданных страницы, отображаемых в режиме чтения.

### Title

Чтобы убедиться в том, что в режиме чтения отображается название статьи, выполните указанные ниже действия.

* Добавление элемента **заголовка** в верхний колонтитул
* Включение тега meta с `name="title"`
* Поиск текста заголовка в тексте статьи с помощью строки содержимого тега meta. Каналы `|` в строке контента не допускают, что представление "читатель" становится активным, попробуйте использовать hypens `-` .

### Созданные

В режиме чтения будет искаться элемент `class = "byline-name"` . Рекомендуется размещать имя автора после названия и перед текстом статьи.

```html
<div class="byline-name">Author name</div>
```

### Дата

В режиме чтения сведения о издателе и дате отображаются в одной строке с дополнительными стилями, чтобы выделить эти сведения. Дата публикации статьи будет отображаться точно так же, как в строке. Режим чтения не преобразуется в определенный формат даты.

Если у вас есть дата в тексте статьи и вы хотите, чтобы режим чтения отображался, назначьте элемент, содержащий дату, на этот класс `'dateline'` :

```html
<div class="dateline"> Wednesday, September 18, 2013 7:38 AM </div>
```

Если у вас нет даты в тексте статьи, но вы хотите, чтобы в режиме чтения отображалась Дата, используйте тег META `name='displaydate'` :

```html
<meta name="displaydate" content=" Wednesday, September 18, 2013 7:38 AM ">
```

### Издатель

Режим чтения будет искать протокол *Open Graph* `"og:site_name"` для отрисовки данных издателя. Он также ищет `source_organization` и `publisher` атрибуты в любом HTML-теге как дополнительный индикатор сведений об издателе на странице. Текст издателя будет гиперссылкой на URL-адрес страницы с помощью стиля "гиперссылка" на странице "режим чтения".

```html
<meta content="Name of organization source" property="og:site_name">
```

### Изображения

В режиме чтения захватывается большинство необработанных изображений с Width >= 400px и пропорции >= 1/3 и =< 3,0. Изображения, которые не соответствуют этим измерениям, могут по-прежнему извлекаться, например изображения, размер которых меньше 400px в ширину, но субтитры. Первое подходящего изображения становится главным изображением статьи. Доминирующее изображение визуализируется как первый фрагмент содержимого и задается полная ширина столбца. Все приведенные ниже изображения отображаются как встроенные изображения в статье.

### Подписи

Лучше размещайте изображения на [рисунках](https://msdn.microsoft.com/library/gg593038(v=vs.85).aspx) с помощью тегов, не имеющих более двух вложенных тегов [figcaption](https://msdn.microsoft.com/library/gg593037(v=vs.85).aspx) .

### Body

Чтобы убедиться в том, что весь основной текст страницы захватывается режимом чтения, это позволяет хранить в большей части текста статьи одинаковый размер шрифта и глубину DOM. Алгоритм представления для чтения допускает некоторое отклонение от этого правила, чтобы издатели могли использовать свободу выделения для линий или слов.

### Авторские права

В режиме чтения извлекаются и отображаются сведения об авторских правах, обозначающие теги META `name = "copyright"` , или если сведения о тегах meta отсутствуют, текстовый узел, содержащий символ авторского права (**©**). В режиме чтения сведения об авторских правах отображаются в конце основного текста статьи, в стиле которого используется меньший размер шрифта, чем у основного основного текста.

```html
<meta name="copyright" content="Your copyright information">
```

## Выход из режима чтения


Если вы считаете, что содержимое не подходит для просмотра в режиме чтения, вы можете использовать следующий тег META для отказа от этой функции:

```html
<meta name="IE_RM_OFF" content="true">
```

При использовании этого тега кнопка " **режим чтения** " не отображается в адресной строке, когда пользователи просматривают страницу.