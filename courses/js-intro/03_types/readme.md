# Типы данных в JavaScript

<iframe width="100%" height="315" src="https://www.youtube.com/embed/808eYu9B9Yw" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Number

Можно использовать все математические операции.
Имеется встроенная библиотека `Math`.

```js
2 + 2 // сложение
3 - 3 // вычитание
10 / 2 // деление
42 * 1 // умножение
10 % 2 // остаток от деления

2.3 + 2.7 // операции с числа с плавающей точкой

console.log(Math.PI) //  вывод числа Пи
```

## String

<iframe width="100%" height="315" src="https://www.youtube.com/embed/irX5I4FaSQE" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<iframe width="100%" height="315" src="https://www.youtube.com/embed/nQ5Ms1WqNa4" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

При обращении к строке с использованием `.` мы обращаемся к методам объекта строка. т.е. наша строка становится объектом.
```js
let i = "hello world";

i.toUpperCase(); // HELLO WORLD
console.log(i) // hello world
```
Большинство методов создают копию строку и выполняют инструкции, не изменяя оригинал.

## Boolean

Примитивный тип данных, имеется только два значения.

```js
let t = true;
let f = false;

if (t)
    console.log("true");
else
    console.log("false");

// true
```

<iframe width="100%" height="315" src="https://www.youtube.com/embed/B4ZCFdrBmbE" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Null/undefined

<iframe width="100%" height="315" src="https://www.youtube.com/embed/VwaqJy_clnc" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<iframe height="400px" width="100%" src="https://repl.it/repls/DoubleHighlevelBootstrapping?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>


[js типы данных (en)](https://javascript.info/types)

[js типы данных (ru)](https://learn.javascript.ru/types)