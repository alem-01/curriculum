## Arrays and Objects

Arrays

```js
const listOfNumbers = [99, 12, 34, 100, 7];

console.log(
    listOfNumbers[0], // → 99
    listOfNumbers[2], // → 34
    listOfNumbers[listOfNumbers.length - 1], // → 7 - last element
    listOfNumbers.length, // → 5 - length of array
)

// append element to array
listOfNumbers.push(8)

// pop last element
const popped = listOfNumbers.pop() // → pop() returns removed element
```

Object - represents a `map` key-value data-structure.

```js
const programmer = {
    age: 23,
    married: false,
    plan: ['coffee', 'code', 'sleep']
}

console.log(
    programmer.age, // → 23
    programmer.plan, // → ['coffee', 'code', 'sleep'],
    programmer.girlfriend // → undefined
)

programmer.girlfriend = 'Natalia Portman'

console.log(
    programmer.girlfriend // → 'Natalia Portman'
)

delete programmer.plan // → delete key-value pair `plan

console.log(
    'plan' in programmer // → false
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

deleteA(myObj) // → {name: 'John', deleted: false}
```
___

2. **Keys**

Implement a function _Object.keys_.

```js
const keys = (obj) => {
    // your code here
}

keys({x: 0, y: 0, z: 2}) // → ['x', 'y', 'z']
```

> [Object.keys](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/Object/keys)
___

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
    myObj, // → {y: 0, z: 2}
    copied // → {x: 0, y: 0, z: 2}
)
```

> [Object.assign](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/Object/assign)

Hint: Object mutability

```js
let object1 = {value: 10}
let object2 = object1
let object3 = {value: 10}

console.log(object1 == object2) // → true
console.log(object1 == object3) // → false

object1.value = 15

console.log(object2.value) // → 15
console.log(object3.value) // → 10
```
___

4. **Advanced max**

Implement a function `advancedMax` that accepts any number of parameters and returns the biggest value.

```js
const advancedMax = (...numbers) => {
    // your code here
}

advancedMax(1) // → 1
advancedMax(5, 3, 10) // → 10
```

> [Rest Parameters](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Functions/Rest_parameters)
___

5. **Reverse Array**

Create a function `reverseArray` that reverses an array.

```js
const reverseArray = (arr) => {
    // your code here
}

reverseArray([1, 2, 3]) // → [3, 2, 1]
```
___

6. **Array to List**

Create a function `arrayToList` that returns list of array values.

```js
const list = {
    value: 1,
    next: {
        value: 2,
        next: {
            value: 3,
            next: {}
        }
    }
}

__________   __________   __________
|value: 1|   |value: 2|   |value: 3|
|next:------>|next:------>|next:-------> {}
|________|   |________|   |________|
```

```js
const arrayToList = (arr) => {
    // your code here
}

arrayToList([1, 2, 3])
```
___

7. **List to Array**

Create a function `listToArray` that returns array of list values.

```js
const listToArray = (list) => {
    // your code here
}

const list = {
    value: 1,
    next: {
        value: 2,
        next: {
            value: 3,
            next: {}
        }
    }
}

arrayToList(list) // → [1, 2, 3]
```

8. **Deep Equal**

Create a function `deepEqual` that takes two values and returns `true` 
if they are the same value or are objects with the same properties, where the 
values of the properties are equal when compared with a recursive call to `deepEqual`.

```js
const deepEqual = (obj1, obj2) => {
    // your code here
}
```

> use _Object.keys_
___

## Links

- [Arrays and Objects](https://eloquentjavascript.net/04_data.html)