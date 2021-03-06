---
title: Представление типов среды выполнения Windows в JavaScript
ms.custom: ''
ms.date: 07/29/2020
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.technology: windows-integration
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- Windows Runtime types [JavaScript]
- JavaScript, Windows Runtime types
ms.assetid: f4851802-8b40-4afa-ba6c-8a162a9a43cc
caps.latest.revision: 9
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 0ee55b5dd5071b0f0b31656ae164e9801e98d6ac
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "10942050"
---
# Представление типов среды выполнения Windows в JavaScript  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

В приведенной ниже таблице описано, как JavaScript представляет типы выполнения Windows Runtime.  

> [!IMPORTANT]
> Функции выполнения Windows недоступны для приложений, работающих в Internet Explorer.  

## Типы выполнения Windows в JavaScript  

| Тип Windows Runtime | Представление JavaScript | Описание |  
|:--- |:--- |:--- |  
| `UInt8` | `Number` | Windows Runtime — `Uint8` это 8-разрядное целое число без знака с неподписанным целым числом, представленным как JavaScript number.  Значение JavaScript сначала преобразуется в номер JavaScript, после чего `ToUint32` выполняется процесс.  Если значение номера JavaScript находится за пределами диапазона Uint8, в результате будет применен модуль 2^8.  |  
| `Int32` | `Number` | Во время выполнения Windows `Int32` служит 32-разрядное целое число со знаком с номером JavaScript.  Значение JavaScript сначала преобразуется в номер JavaScript, после чего `ToInt32` выполняется процесс.  Если значение номера JavaScript находится за пределами `Int32` диапазона, будет применен модуль 2^16.  |  
| `Int64` | `Number` | `Int64`64-разрядное целое число с знаком "64-разрядная", представляемое как стандартное число, если он попадется в диапазон \[-2^53\].  Если она выходит за этот диапазон, оно представляется как числовое значение, которое в котором сохраняется полный хранилище для шести целых чисел.  Все математические операции с этими числовыми номерами Int64 приводит к преобразованию его в стандартное число в диапазоне \[-2^53, 2^53\].  Если значение находится за пределами этого диапазона, возникает ошибка типа.  Исключения из этого процесса `==` преобразования: `===` " ", `SameValue` ", `RelationalComparison` " и операции, которые сравнивают аргументы с учетом полных 64-битов при переносе двух битов, представленных в 64-разрядной.  Если значение какого-либо из аргументов является стандартным номером JavaScript, эти операции также преобразуются в номер JavaScript перед сравнением.  Значение JavaScript назначается непосредственно, если это Int64 само значение. В противном итоге применение преобразования значения `ToInteger` в среду среды выполнения Windows.  Если возникнет сбой согласия типов, возвращается исключение.  |  
| `Uint64` | `Number` | `Uint64`64-разрядное целое число без знака и представляет собой стандартное число, если оно попадет в диапазон \[0, 2^53\].  Если она выходит за этот диапазон, он будет иметь число с настраиваемым магазином для обратной связи, в котором будут храниться полные 64 биты неподписанных целых чисел без знака.  Все математические операции на этих пользовательских значениях Uint64 приводит к преобразованию его в стандартное число в диапазоне \[0, 2^53\].  Если значение находится за пределами этого диапазона, возникает ошибка типа.  Исключения из этого процесса `==` преобразования: `===` , , , `SameValue` и `RelationalComparison` операции, которые сравнивают аргументы с учетом полных 64-разрядных значений при переносе два-разрядных значения.  Если значение какого-либо из аргументов является стандартным номером JavaScript, эти операции также преобразуются в номер JavaScript перед сравнением.  Значение JavaScript назначается непосредственно, если оно является само значением Uint64. В противном случае результат применения преобразования значения, за которым `ToInteger` путаница 2^52, пройдет проверка windows в среду выполнения Windows.  Если преобразование типа не произойдет, возвращается исключение.  |  
| `Single` | `Number` | Windows Runtime `Single` — это 32-разрядное число с плавающей запятой, которое представлено как номер JavaScript, выбрав ближайшее значение точности для одной точности.  Значение JavaScript преобразуется в номер JavaScript, а затем — установленный флажок, чтобы значение было представлено в 32-разрядной версии IEEE 754 с плавающей запятой.  Если проверка или диапазон не пройдена, возвращается ошибка поля.  |  
| `Double` | `Number` | Во время выполнения Windows `Double` выбирается 64-разрядное число с плавающей запятой.  `ToNumber` используется для преобразования кода Выполнения Windows Runtime `Double` в номер JavaScript.  Если преобразование завершится сбоем, возвращается ошибка маршрутизации.  |  
| `Boolean` | `Boolean` | Выполнение Windows — это 8-битное значение, где нулевым совпадает и любое значение, отличный `Boolean` `false` от нуля, представлено в виде `true` JavaScript. `Boolean`  Значение JavaScript сначала преобразуется в JavaScript. `Boolean` `ToBoolean`  Это означает, что функция среды выполнения Windows обрасплевена так, как можно записывать `void func(BOOL);` в JavaScript `obj.func("test");` как.  Функция Windows Runtime называется `BOOL` параметром, который был переведен как параметр, который был переведен `TRUE` как параметр.  Если преобразование завершится сбоем, возвращается ошибка маршрутизации.  |  
| `Char16` | `String` | Среда выполнения Windows — `Char16` это 16-битный символ Юникода, содержащий один символ.  Значение JavaScript преобразуется в строку JavaScript, проверяя, надоличить у достижения длиной `ToString` единого символа.  После этого в качестве значения будет добавлен один `Char16` символ.  Если проверка или длина проверки завершится сбоем, возвращается ошибка "Разное поле".  |  
| `String` | `String` | Windows Runtime представляет собой немного важную последовательность `String` `Char16` объектов.  Строки представлены как объекты JavaScript. `String`  Для строк среды выполнения Windows не требуются разные значения для и пустой `null` строки \("\).  `null` пустые строковые значения преобразуются в пустую строку JavaScript пустой строки JavaScript.  **ПРИМЕЧАНИЕ.** Когда JavaScript присутствует `null` значение JavaScript, ожидающее строку, возвращается строковое значение "Null", а не `null` пустая строка \("\).  Строки, которые были переданныы в среду выполнения Windows Runtime, всегда должны быть перечислены в пустую строку.  |  
| `Enumeration` | `Object` | Среда выполнения Windows — `Enumeration` это 32-битное целое число \(подписанная или неподписанная\), которое имеет связанный набор именованных констант.  В JavaScript перечисление представлены в виде объекта, содержащего поле с доступом только для чтения для чтения.  Значения перечисления преобразуются в номера JavaScript, определенные ранее для `Int32` и сохранения. `UInt32`  При преобразовании значения JavaScript в перечисления среды выполнения это значение преобразуется, усечено и диапазоном, как описано выше.  Однако полученное значение не проверяется на заданные именованные значения, указанные в перечислении.  |  
| `Structure` | `Object` | Windows Runtime — `Structure` это шестеренку именованных полей данных.  В JavaScript структура представлена как объект JavaScript, содержащий именованное свойство каждого поля в структуре.  В случае сбоя структуры любого значения возвращается ошибка при ошибке изменения.  Поля объекта JavaScript, у которых нет эквивалентных данных в структуре выполнения Windows, игнорируются.  **ПРИМЕЧАНИЕ.** Структуру выполнения Windows Runtime невозможно справиться с ключевым `new` словом JavaScript.  |  
| `Array` | `Array` | Во время выполнения Windows `Array` выполняется преобразование в массив JavaScript.  Однако размер массивов Windows Runtime невозможно изменить, поэтому некоторые операции массива JavaScript недоступны.  Внутреннее `[[Class]]` свойство преобразованного массива не равно "массиву", поскольку это действие не допустило спецификацию ECMAScript 5.  Это означает, что `Array.isArray(v)` возвращается `false` значение.  Значение JavaScript преобразуется в массив выполнения Windows следующим образом: если значение имеет значение или оно преобразуется в `null` `undefined` собственный. `null`  Если его внутреннее свойство скопировано в массив, то оно копируется в массив, а ссылка на `[[Class]]` этот массив пройдет.  Если это преобразованный массив, как описано выше, в качестве встроенного массива производится собственный массив.  **ПРИМЕЧАНИЕ.** При принципе к методу выполнения Windows Runtime приводит к полной копии массива.  |  
| Delegate \(функция callback\) | `Function` | Делегат выполнения Windows — это ссылка на один метод.  Делегат выполнения Windows Runtime представленва в виде JavaScript, который гарантированно вызывается в `Function` нужной цепочке.  При `Function` вызове аргументы преобразуются в аналогичные типы параметров Windows.  Если аргументов JavaScript меньше, чем параметры `in` делегирования, делегирование не работает.  Если представителю были исключены другие аргументы JavaScript, чем для представителя, `in` аргументы дополнительных аргументов JavaScript игнорируются.  После вызова представителя параметры преобразуются `out` в типы JavaScript и вернутся.  При преобразовании объекта функции JavaScript в делегат среды выполнения Windows переносится в делегат на Windows Runtime соответствующего типа.  При вызове представителя параметры преобразуются `in` в типы JavaScript.  После вызова представителя возвращаемое значение преобразуется в `out` параметры делегата.  |  
| Интерфейс | `Object` | Группы интерфейсов и интерфейсов не представлены непосредственно в JavaScript как объекты.  Однако интерфейсы представлены в виде параметра и возвращаемых методов Windows Runtime.  Экземпляр интерфейса Windows преобразуется в следующий синтаксис:<br /> <br /> 1. Если имеется допустимое занятие выполнения, представьте его как экземпляр этого класса.<br /> 2. Если нет допустимого класса среды выполнения, представьте объект в качестве экземпляра неименованного занятия среды выполнения, который реализует интерфейс того, что экземпляр известен для реализации и необходимых интерфейсов.<br /> <br /> Значение JavaScript проверяется, чтобы определить, является ли он экземпляром класса среды выполнения или интерфейса выполнения.  Если это так, и исходное значение среды выполнения Windows реализовано в интерфейсе, он переносится в среду выполнения Windows Runtime.  |  
| Классы выполнения | `Object` | Объекты в среде среды выполнения Windows могут быть экземплярами классов среды выполнения, которые реализуют один или несколько интерфейсов.  Объекты PowerPoint представлены в виде объектов JavaScript.  Объединение методов, свойств и событий, определенных во всех реализованных интерфейсах класса, обозначает имена свойств объекта JavaScript.  Потребители JavaScript могут получить доступ непосредственно к любым участникам класса.  Объекты Windows имеет прототип, содержащий все хотя бы одного из внедренных интерфейсов класса среды выполнения.  |  
  
## См. также  

[Использование среды выполнения Windows в JavaScript][WindowsRuntimeJavascript]  

<!-- links -->  

[WindowsRuntimeJavascript]: ./using-the-windows-runtime-in-javascript.md "Использование Windows Runtime в JavaScript | Документы Майкрософт"  
