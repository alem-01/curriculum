# Higher-Order Functions

This is the program to find sum between 1 and 10. It takes 6 lines long.

```js
let total = 0, count = 1;
while (count <= 10) {
    total += count;
    count += 1;
}
console.log(total);
```

To make programs more readable, there are ready built-in functions that allow you 
to shorten your code and make them more elegant - **higher order functions**.

The program above can be written:

```js
console.log(sum(range(1, 10)));
```

- `range` returns an array of numbers from 1 to 10
- `sum` returns sum of array elements

At the end of the page you will find useful links to finish the exercises. 


## Exercises

1. **Map**

Create a function `map`. It should return array of function call results on each 
element of `array`.

```js
const map = (array, func) => {
    // your code here
}

map([1, 2, 3, 4], (elem) => elem * 2) // [2, 4, 6, 8]
map(['John', 'Martin'], (name) => `Hello, ${name}`) // ['Hello, John', 'Hello, Martin']
```
___

2. **Greater Than**

Create function `greaterThan` that returns a function which returns `true` or `false` 
whether value is greater than `N`.

```js
const greaterThan = N => {
    // your code here
}

const greater = greaterThan(10)

greater(5) // false
greater(12) // true
```
___

3. **Flattening**

Write function `flatten` that uses `reduce` method in combination with the `concat` method 
to _flatten_ an array of arrays into a single array that has all the elements of the original arrays.

```js
const flatten = (array) => {
    // your code here with .reduce
}

const arrays = [[1, 2, 3], [4, 5], [6]]
flatten(arrays) // [1, 2, 3, 4, 5, 6]
```

> Use [.reduce](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/Array/Reduce)
___

4. **Loop**

Create a function `loop` that implements `for` loop statement.

It takes:
- an initial value,
- a test function,
- an update function, 
- a body function.

Each iteration, it first runs the `test` function on the current loop `value` and stops if that returns `false`.
Then it calls the `body` function, passing the current value. Finally, it calls the `update` function to create a new value and starts from the beginning.

```js
const loop = (init, testFunc, updateFunc, bodyFunc) => {
    // your code here
}

loop(3, n => n > 0, n => n - 1, console.log);
// → 3
// → 2
// → 1
```
___

5. **Every**

Create a function `every` which returns `true` if every element in the array returns `true`, otherwise `false`.

```js
const every = (array, testFunc) => {
    // your code here
}

every([1, 3, 5], n => n < 10) // → true
every([2, 4, 16], n => n < 10) // → false
every([], n => n < 10) // → true
```
___

6. **Filter**

Write a `filter` function that implements [Array.prototype.filter](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/Array/filter).

```js
const filter = (array, callback) => {
    // your code here
}

filter(['spray', 'limit', 'elite', 'exuberant', 'destruction', 'present'], word => word.length > 6) // ['`exuberant', 'destruction', 'present']
```

7. **Reduce**

Write `reduce` function that implements [Array.prototype.reduce](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/Array/Reduce).

```js
const reduce = (array, callback, initialValue) => {
    // your code here 
}

// 1 + 2 + 3 + 4
reduce([1, 2, 3, 4], (accumulator, currentValue) => accumulator + currentValue) // 10

// 5 + 1 + 2 + 3 + 4
reduce([1, 2, 3, 4], (accumulator, currentValue) => accumulator + currentValue, 5) // 15
```

## Links

- [Higher-Order Functions](https://eloquentjavascript.net/05_higher_order.html)