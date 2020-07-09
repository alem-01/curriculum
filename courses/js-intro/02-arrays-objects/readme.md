## Arrays and Objects

Arrays

```js
const listOfNumbers = [99, 12, 34, 100, 7];

console.log(
    listOfNumbers[0], // 99
    listOfNumbers[2], // 34
    listOfNumbers[listOfNumbers.length - 1], // 7 - last element
    listOfNumbers.length, // 5 - length of array
)

// append element to array
listOfNumbers.push(8)

// pop last element
const popped = listOfNumbers.pop() // pop() returns removed element
```

Object - represents a `map` key-value data-structure.

```js
const programmer = {
    age: 23,
    married: false,
    plan: ['coffee', 'code', 'sleep']
}

console.log(
    programmer.age, // 23
    programmer.plan, // ['coffee', 'code', 'sleep'],
    programmer.girlfriend // undefined
)

programmer.girlfriend = 'Natalia Portman'

console.log(
    programmer.girlfriend // 'Natalia Portman'
)

delete programmer.plan // delete key-value pair `plan

console.log(
    'plan' in programmer // false
)
```

> Arrays, Objects

## Задания

1. **Delete a**

Create a function `deleteA` that takes an object and returns it with deleted 
keys which start from `a and A`.

```js
const deleteA = (obj) => {
    // your code here
}

const myObj = {
    age: 23,
    name: 'John',
    'a human': true,
    deleted: false
}

deleteA(myObj) // {name: 'John', deleted: false}
```

2. **Keys**

Implement a function _Object.keys_.

```js
const keys = (obj) => {
    // your code here
}

keys({x: 0, y: 0, z: 2}) // ['x', 'y', 'z']
```

> [Object.keys](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/Object/keys)

3. **Assign**

Create a function that returns a copy of passed object.

```js
const copyObj = (obj) => {
    // your code here
}

const myObj = {x: 0, y: 0, z: 2}
const copied = copyObj(myObj)

delete myObj.x
console.log(
    myObj, // {y: 0, z: 2}
    copied // {x: 0, y: 0, z: 2}
)
```

> [Object.assign](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/Object/assign)


### Ссылки

- [о JS](https://learn.javascript.ru/intro)
- [node](https://nodejs.dev/)
