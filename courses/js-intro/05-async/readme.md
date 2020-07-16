# Async

Async allows to run multiple procedures in multiple threads. 

JS allows to run these `procedures` and wait for the results. For example you make 
2 fetch requests each takes 2 secs.

Synchoriniously waiting for first fetch to resolve and then running second fetch will take 4 seconds overall.

Therefore, you can make these `fetches` asynchroniously waiting for both to resolve - 
that would take 2 seconds overall.
___

## Resolve: then

A `promise` is an asynchronous action that may complete at some point and produce a value. It is able to notify anyone who is interested when its value is available.

One of the ways to create a `promise` is by calling `new Promise`.

```js
const fifteen = new Promise((resolve, reject) => {
	resolve(15)
})

fifteen.then(value => {
	console.log(value) // → Got 15
})
```

To get the result of a promise, use its `then` method.

Promise should take callback function with arguments: `(resolve, reject)`.
- `resolve` is a function that takes only one argument and passes it to `.then` method
___

## Reject: catch

Regular JavaScript computations can fail by throwing an `exception`. Asynchronous computations often need something like that.

Promises can be either `resolved` (the action finished successfully) or `rejected` (it failed).

```js
const fifteen = new Promise((resolve, reject) => {
	reject(new Error('Fail'))
})

fifteen.catch(error => {
	console.log(error) // → Fail
})
```

To catch the error, simply call `.catch` method.
___

## Ignored

```js
let fifteen = new Promise(function(resolve, reject) {
	resolve(15);

	reject(new Error('Fail')); // ignored
	resolve('...') // ignored
});
```

Promise function can't call multiple times `resolve` and `reject`. Only first function call is executed, any further are ignored.

## Exercises

1. **Delay**

Create a function `delay` that returns a promise that resolves after `N` seconds.

```js
const delay = (N) => {
	// your code here
}

delay(5).then(() => console.log('Resolved after 5 seconds!'))
```

> use [setTimeout](https://developer.mozilla.org/ru/docs/Web/API/WindowTimers/setTimeout)
___

2. **All**

Create a function `all` that implements `Promise.all`.

```js
const all = (promises) => {
	// your code here
}
```

> [Promise.all](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/Promise/all)

___

3. **Race**

Create a function `race` that implements `Promise.race`.

```js
const race = (promises) => {
	// your code here
}
```

> [Promise.race](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/Promise/race)

## Links

1. [Async](https://eloquentjavascript.net/11_async.html)
2. [Promise Chaining](https://javascript.info/promise-chaining)
