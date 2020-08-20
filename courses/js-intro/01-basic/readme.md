## Basic

> Variables, Types, If/Else, Functions

To successfully submit the exercise push your code to your repo.

## Exercise

1. **Variables and Types**

Create constant variables with different types:
- `number` contains `Number` value
- `float` contains `float` value
- `str` contains `String` value
- `bool` contains `Boolean` value
- `undef` contains `undefined` value
- `nullVar` contains `null` value
___

2. **Square Function**

Create function `square` that returns square value of passed `Number`.

```js
const square = (n) => {
    // your code here
}

square(3) // 9
```
___

3. **Hello, ${name}**

Create function `hello` with parameter `name`.

```js
const hello = (name) => {
    // your code here
}

hello('world') // `Hello, world!`
hello('Martin') // `Hello, Martin!`
```

> [interpolation](https://flaviocopes.com/javascript-template-literals/#interpolation)
___

4. **Concat Strings**

Create function `concat`.

Parameters: Array of String

Return: concatenated string

```js
const concat = (strings) => {
    // your code here
}

concat(['Hello ', 'World!']) // 'Hello World!'
```
___

5. **What Type?**

Create function `getType` that returns type of passed value.

```js
const getType = (value) => {
    // your code here
}

getType(1) // 'number'
getType(['Hello ', 'World!']) // 'array'
getType('hello') // 'string'
getType({a: 1, b: 2}) // 'object'
```

> [typeof](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Operators/typeof)
___

6. **Max**

Create function `max` that takes 2 arguments and returns maximum of them.

```js
const max = (a, b) => {
    // your code here
}

max(3, 100) // 100
```

> [if...else](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Statements/if...else)
___

7. **Max of 3**

Create function `max3` that takes 3 arguments and returns maximum of them.

```js
const max3 = (a, b, c) => {
    // your code here
}

max(300, 100, 5) // 300
```
___

8. **Change**

An item costs `N` dollars and `C` cents. You bought it for `K` dollars and `L` cents.

Create function `change` that takes 4 arguments and returns a string - the money you get.

```js
const change = (N, C, K, L) => {
    // your code here
}

change(5, 5, 6, 5) // '$1.0'
change(2, 17, 2, 18) // '$0.1'
change(2, 17, 2, 16) // 'not enough'
```
___

9. **Triangle**

Create a function `triangle` that returns the following triangle as string with height 7:
```
#
##
###
####
#####
######
#######
```

> Last line must have a new line.

```js
const triangle = (height) => {
    // your code here
}
```

> [Loops](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Loops_and_iteration)
___

10. **FizzBuzz**

Create a function `fizzbuzz` that returns an array.
It should push the numbers from 1 to `N`, with two exceptions. 
- For numbers divisible by 3, push `Fizz` instead of the number
- For numbers divisible by 5 (and not 3), push `Buzz` instead.

```js
const fizzbuzz = (N) => {
    // your code here
}
```

> use `===` for strict comparison.
___

11. **Count char**

Create a function `countChar` that counts `char` in `str`. If second argument is not given 
then count for `C`.

```js
const countChar = (str, char) => {
    // your code here
}

countChar('Im gonna go, go, go', 'o') // 4
countChar('Crown for King') // 1
```

> [default value](https://stackoverflow.com/a/894877)
___

### Ссылки

- [Values](https://eloquentjavascript.net/01_values.html)
- [Functions](https://eloquentjavascript.net/03_functions.html)