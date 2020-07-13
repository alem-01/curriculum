# Тип данных Массив

Массивы это индексированный список из элементов к которым можно обратиться через индекс.
В нем мы можем хранить любые типы данных.

Индексация начинается с 0.

<iframe width="100%" height="315" src="https://www.youtube.com/embed/oigfaZ5ApsM" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

Создание массива
```js
let arr = [1, 2];

console.log(arr[0]); // 1
```

`length` - для получения длины массива.

Получить последний элемент
```js
let arr = [1, 2, 3, 4, 5, 6];

console.log(arr[arr.length - 1]); // 6
```

Методы перебора по массиву.

```js
let fruits = ['Apple', 'Banana'];

fruits.forEach(function(item, index, array) {
  console.log(item, index);
});
// Apple 0
// Banana 1
```

Для добавления, удаления, создания новых массивов существует встроенные методы для типа Массив.

Добавление нового элемента.
```js
let newLength = fruits.push('Orange');
// ["Apple", "Banana", "Orange"]
```

Удаление последнего элемента массива.

```js
var last = fruits.pop(); // remove Orange (from the end)
// ["Apple", "Banana"];
```

Удаление первого элемента массива.

```js
var first = fruits.shift(); // remove Apple from the front
// ["Banana"];
```

Добавление в начало массива.
```js
var newLength = fruits.unshift('Strawberry') // add to the front
// ["Strawberry", "Banana"];
```

Поиск элемента в массиве, возвращает индекс.

```js
var pos = fruits.indexOf('Banana');
// 1
```

Для удаления больше одного элемента есть методы:

splice
<iframe width="100%" height="315" src="https://www.youtube.com/embed/pNJDbE-d77w" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

slice
<iframe width="100%" height="315" src="https://www.youtube.com/embed/QdwLGI1yNrk" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

Для перебора есть метода `map`, `reduce`, `filter`

<iframe width="100%" height="315" src="https://www.youtube.com/embed/G3BS3sh3D8Q" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
<iframe width="100%" height="315" src="https://www.youtube.com/embed/4_iT6EGkQfk" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
<iframe width="100%" height="315" src="https://www.youtube.com/embed/g1C40tDP0Bk" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

[js array](https://devdocs.io/javascript/global_objects/array)