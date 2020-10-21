---
description: Используйте API консоли для записи сообщений на консоль.
title: Справочник по API консоли
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 38fb3ee2345530775423ac3ec8e53e0d8de76eaf
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125288"
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

# Справочник по API консоли  

Используйте методы API консоли для записи сообщений на консоль из JavaScript.  Для интерактивного знакомства со статьей перейдите в раздел Начало [работы с сообщениями журнала на консоли][DevtoolsConsoleLog].  Для удобства работы с удобными методами, такими как `debug()` или `monitorEvents()` доступные только в области **консоли** , перейдите по [ссылке API для консольных программ][DevtoolConsoleUtilities].  

---  

## затребованного  

```javascript
console.assert(expression, object)
```

[Уровень журнала][DevtoolsConsoleReferencePersist]: `Error`  

<!--todo: add reference level (reference#persist-messages-across-page-loads) when available -->  

При вычислении выводит на консоль [сообщение об ошибке](#error) `expression` `false` .  

```javascript
const x = 5;
const y = 3;
const reason = 'x is expected to be less than y';
console.assert(x < y, {x, y, reason});
```  

:::image type="complex" source="../media/console-demo-assert-button.msft.png" alt-text="Результат примера Console. Assert ()" lightbox="../media/console-demo-assert-button.msft.png":::
   Рисунок 1: результат `console.assert()` примера  
:::image-end:::  

---  

## Сброс  

```javascript
console.clear()
```

Очищает консоль.  

```javascript
console.clear();  
```  

Если включен [протокол Preserve][DevtoolsConsoleReferenceLevel] , метод [clear](#clear) отключен.  

### См. также  

*   [Очистка консоли][DevtoolsConsoleReferenceClear]  

---  

## счет  

```javascript
console.count([label])
```  

[Уровень журнала][DevtoolsConsoleReferencePersist]: `Info`  

Записывает количество вызовов метода [Count](#count) в той же строке и с тем же `label` .  Для сброса счетчика используйте метод [countReset](#countreset) .  

```javascript
console.count();
console.count('coffee');
console.count();
console.count();
```  

:::image type="complex" source="../media/console-demo-count-button.msft.png" alt-text="Результат примера Console. Assert ()" lightbox="../media/console-demo-count-button.msft.png":::
   Рисунок 2: результат `console.count()` примера  
:::image-end:::  

---  

## countReset  

```javascript
console.countReset([label])
```  

Сбрасывает число.  

```javascript
console.countReset();
console.countReset('coffee');
```  

---  

## отладка  

```javascript
console.debug(object [, object, ...])
```  

[Уровень журнала][DevtoolsConsoleReferencePersist]: `Verbose`

Совпадает с [журналом](#log) , кроме разных уровней ведения журнала.  

```javascript
console.debug('debug');  
```  

:::image type="complex" source="../media/console-demo-debug-button.msft.png" alt-text="Результат примера Console. Assert ()" lightbox="../media/console-demo-debug-button.msft.png":::
   Рисунок 3: результат `console.debug()` примера  
:::image-end:::  

---  

## dir  

```javascript
console.dir(object)
```  

[Уровень журнала][DevtoolsConsoleReferencePersist]: `Info`  

Печатает представление JSON указанного объекта.  

```javascript
console.dir(document.head);
```  

:::image type="complex" source="../media/console-demo-dir-button.msft.png" alt-text="Результат примера Console. Assert ()" lightbox="../media/console-demo-dir-button.msft.png":::
   Рисунок 4: результат `console.dir()` примера  
:::image-end:::  

---  

## dirxml  

```javascript
console.dirxml(node)
```  

[Уровень журнала][DevtoolsConsoleReferencePersist]: `Info`  

Печатает XML-представление потомков `node` .  

```javascript
console.dirxml(document);
```  

:::image type="complex" source="../media/console-demo-dirxml-button.msft.png" alt-text="Результат примера Console. Assert ()" lightbox="../media/console-demo-dirxml-button.msft.png":::
   На рисунке 5 показан результат примера. `console.dirxml()`  
:::image-end:::  

---  

## ошибка  

```javascript
console.error(object [, object, ...])
```  

[Уровень журнала][DevtoolsConsoleReferencePersist]: `Error`  

Выводит на `object` консоль сообщение об ошибке, форматирует его как ошибку и включает трассировку стека.  

```javascript
console.error("I'm sorry, Dave.  I'm afraid I can't do that.");
```  

:::image type="complex" source="../media/console-demo-error-button.msft.png" alt-text="Результат примера Console. Assert ()" lightbox="../media/console-demo-error-button.msft.png":::
   Рисунок 6: результат `console.error()` примера  
:::image-end:::  

---  

## группа  

```javascript
console.group(label)
```  

Визуально группирует сообщения, пока не будет использован метод [groupEnd](#groupend) .  Используйте метод [groupCollapsed](#groupcollapsed) , чтобы свернуть группу при первом входе в систему на консоли.  

```javascript
const label = 'Adolescent Irradiated Espionage Tortoises';
console.group(label);
console.info('Leo');
console.info('Mike');
console.info('Don');
console.info('Raph');
console.groupEnd(label);
```  

:::image type="complex" source="../media/console-demo-group-button.msft.png" alt-text="Результат примера Console. Assert ()" lightbox="../media/console-demo-group-button.msft.png":::
   На рисунке 7 показан результат примера. `console.group()`  
:::image-end:::  

---  

## groupCollapsed  

```javascript
console.groupCollapsed(label)
```  

То же, что и в методе [log](#log) , за исключением того, что группа изначально свернута при входе в систему на консоли.  

---  

## groupEnd  

```javascript
console.groupEnd(label)
```  

Прекращение визуальной группировки сообщений.  Просмотрите метод [группировки](#group) .  

---  

## "Сведения"  

```javascript
console.info(object [, object, ...])
```  

[Уровень журнала][DevtoolsConsoleReferencePersist]: `Info`  

Идентичен методу [log](#log) .  

```javascript
console.info('info');
```  

:::image type="complex" source="../media/console-demo-info-button.msft.png" alt-text="Результат примера Console. Assert ()" lightbox="../media/console-demo-info-button.msft.png":::
   Рисунок 8: результат `console.info()` примера  
:::image-end:::  

---  

## выходе  

```javascript
console.log(object [, object, ...])
```  

[Уровень журнала][DevtoolsConsoleReferencePersist]: `Info`  

Вывод на консоль сообщения.  

```javascript
console.log('log');
```  

:::image type="complex" source="../media/console-demo-log-button.msft.png" alt-text="Результат примера Console. Assert ()" lightbox="../media/console-demo-log-button.msft.png":::
   На рисунке 9 показан результат примера. `console.log()`  
:::image-end:::  

---  

## таблич  

```javascript
console.table(array)
```  

[Уровень журнала][DevtoolsConsoleReferencePersist]: `Info`  

Заносит в журнал массив объектов в виде таблицы.  

```javascript
console.table([
    {
        first: 'René',
        last: 'Magritte',
    },
    {
        first: 'Chaim',
        last: 'Soutine',
        birthday: '18930113',
    },
    {
        first: 'Henri',
        last: 'Matisse',
    }
]);
```  

:::image type="complex" source="../media/console-demo-table-button.msft.png" alt-text="Результат примера Console. Assert ()" lightbox="../media/console-demo-table-button.msft.png":::
   Рисунок 10: результат `console.table()` примера  
:::image-end:::  

---  

## time  

```javascript
console.time([label])
```  

Запуск нового таймера.  Используйте метод [timeEnd](#timeend) , чтобы остановить таймер и напечатать время, затраченное на консоль.  

```javascript
console.time();
for (var i = 0; i < 100000; i++) {
    let square = i ** 2;
}
console.timeEnd();
```  

:::image type="complex" source="../media/console-demo-time-button.msft.png" alt-text="Результат примера Console. Assert ()" lightbox="../media/console-demo-time-button.msft.png":::
   На рисунке 11 показан результат примера. `console.time()`  
:::image-end:::  

---  

## timeEnd  

```javascript
console.timeEnd([label])
```  

[Уровень журнала][DevtoolsConsoleReferencePersist]: `Info`  

Останавливает таймер.  Просмотрите метод [time (время](#time) ).  

---  

## событий  

```javascript
console.trace()
```  

[Уровень журнала][DevtoolsConsoleReferencePersist]: `Info`  

Выводит на консоль трассировку стека.  

```javascript
const first = () => { second(); };
const second = () => { third(); };
const third = () => { fourth(); };
const fourth = () => { console.trace(); };
first();
```  

:::image type="complex" source="../media/console-demo-trace-button.msft.png" alt-text="Результат примера Console. Assert ()" lightbox="../media/console-demo-trace-button.msft.png":::
   Рис. 12: результат `console.trace()` примера  
:::image-end:::  

---  

## оповещает  

```javascript
console.warn(object [, object, ...])
```  

[Уровень журнала][DevtoolsConsoleReferencePersist]: `Warning`  

Вывод на консоль предупреждения.  

```javascript
console.warn('warn');
```  

:::image type="complex" source="../media/console-demo-warn-button.msft.png" alt-text="Результат примера Console. Assert ()" lightbox="../media/console-demo-warn-button.msft.png":::
   Рисунок 13: результат `console.warn()` примера  
:::image-end:::  

## Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleLog]: /microsoft-edge/devtools-guide-chromium/console/log "Начало работы с сообщениями журнала на консоли"  
[DevtoolConsoleUtilities]: /microsoft-edge/devtools-guide-chromium/console/utilities "Справочник по API для консольных программ"  
[DevtoolsConsoleReferenceClear]: /microsoft-edge/devtools-guide-chromium/console/reference#clear-the-console "Удаление ссылки на консоль консоли"  
[DevtoolsConsoleReferencePersist]: /microsoft-edge/devtools-guide-chromium/console/reference#persist-messages-across-page-loads "Сохранение сообщений на странице с загрузкой на консоли"  
[DevtoolsConsoleReferenceLevel]: /microsoft-edge/devtools-guide-chromium/console/reference#filter-by-log-level "Фильтрация по уровню журнала — Справочник по консоли"  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Инструменты разработчика Microsoft EDGE (Chromium)"  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/console/api) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
