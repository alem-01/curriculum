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


> Curry

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

## Links

- [Higher-Order Functions](https://eloquentjavascript.net/05_higher_order.html)