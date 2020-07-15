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

Create a function `delay` that returns a promises that resolves after N seconds.

```js
const delay = (N) => {
	// your code here
}

delay(5).then(() => console.log('Resolved after 5 seconds!'))
```

> use [setTimeout](https://developer.mozilla.org/ru/docs/Web/API/WindowTimers/setTimeout)

2. **Fetch Data**

Create function `fetchData` that returns `.text` method result from `fetch`. If error is caught, return `error`.

```js
const fetchData = (url) => {
	// your code here
}

fetchData('http://there-is-no-such-site-should-be-error.lol') // error
fetchData('https://google.com') // (Google body)...
```

> use [fetch](https://developer.mozilla.org/ru/docs/Web/API/Fetch_API/Using_Fetch)