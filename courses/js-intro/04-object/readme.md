# Тип данных - Объект

Объект это еще один тип данных. Представляет собой список ключ/значение.

```js
let obj = {
    name: "Abylaikhan",
    birthYear: 1997
}
// мы можем обращаться по ключу
console.log(obj["name"]) 
console.log(obj.name)
console.log({name} = obj)
```

Мы создали переменную `obj` типа `объект`. В нем `name` и `birthYear` это ключи, а `"Abylaikhan"` и `1997` это значения.

Для добавления элемента можно обратить по новому ключу и присвоить значение.

```js
let o = {} // создаем пустой объект

o.one = 1; // создадим ключ `one` со значением 1

console.log(o)
// OUTPUT
// { "one": 1 }
```

Для удаления используется инструкция `delete key`

```js
let o = {
    one: 1
}

delete o.one
```

Для перебора по объекту используется операция `for (let key in object)`

```js

let o = {
    one: 1,
    two: 2
};

for (let key in o) {
    console.log(key, o[key]);
}
// Output
// one 1
// two 2
```

Для того, чтобы узнать есть ли ключ в объекте, используется инструкция `"key" in obj`, которая возвращает `true` или `false`

```js
let o = {
    one: 1
};

if ("one" in o) {
    console.log("One exist");
}

if ("two" in o) {
    console.log("Two exsit");
} else {
    consol.log("Two does not exist");
}

// OUTPUT
// One exist
// Two does not exist
```

Есть и другие способы, можно прочитать в этой [статье](https://gomakethings.com/looping-through-objects-with-es6/)

<iframe width="100%" height="315" src="https://www.youtube.com/embed/X0ipw1k7ygU" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<iframe height="400px" width="100%" src="https://repl.it/repls/DoubleHighlevelBootstrapping?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>

[JS object basic](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Objects/Basics)
[js object methods](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Working_with_Objects)