## Введение
Добро пожаловать в экспресс курс по JS!


JS динамично развивающийся язык программирования. С помощью него разрабатывают 
веб и мобильные приложений.

## Синтаксис

Синтаксис языка программирования достаточно интуитивен, в нашем арсенале есть 
основные типы и множество встроенных функций для работы с ними. Имеется множество 
отладчиков, программ, которые позволяют найти ошибки.

## Разработка

Для разработки мы будем использовать редактор `repl.it`. 

JS встроен в браузер и можно легко запустить код открыв `Developer Tools` (можете загуглить)
Также, существует движок [node](https://nodejs.org) который умеет выполнять код JS.


Напишем простую программу, которая поприветствует человека, запустившего его.

```js
console.log("Hello World!");
```

Про консоль

<iframe width="100%" height="315" src="https://www.youtube.com/embed/L8CDt1J3DAw" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
____

Песочница

<iframe height="400px" width="100%" src="https://repl.it/repls/DoubleHighlevelBootstrapping?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>

## Задания

1. Variables and Types

Create constant variables with different types:
- `number` contains `Number` value
- `float` contains `float` value
- `str` contains `String` value
- `bool` contains `Boolean` value
- `undef` contains `undefined` value
- `null` contains `null` value

2. Square Function

Create function `square` that returns square value of passed `Number`.

```js
const square = (n) => {
    // your code here
}

square(3) // 9
```

3. Hello, ${name}

Create function `hello` with parameter `name`.

```js
const hello = (name) => {
    // your code here
}

hello('world') // `Hello, world!`
hello('Martin') // `Hello, Martin!`
```

4. Concat Strings

Create function `concat`.

Parameters: Array of String

Return: concatenated string

```js
const concat = (strings) => {
    // your code here
}

concat(['Hello ', 'World!']) // 'Hello World!'
```

5. What Type?

Create function `getType` that returns type of passed value.

```js
const getType = (value) => {
    // your code here
}

getType(1) // number
getType(['Hello ', 'World!']) // array
getType('hello') // string
getType({a: 1, b: 2}) // object
```

6. Max

Create function `max` that takes 2 arguments and returns maximum of them.

```js
const max = (a, b) => {
    // your code here
}

max(3, 100) // 100
```
___

### Ссылки

- [о JS](https://learn.javascript.ru/intro)
- [node](https://nodejs.dev/)

