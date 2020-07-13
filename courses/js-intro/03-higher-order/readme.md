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

3. **Flattening**


___

## Links

- [Higher-Order Functions](https://eloquentjavascript.net/05_higher_order.html)