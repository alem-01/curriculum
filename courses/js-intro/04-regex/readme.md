# Regex

Regular expressions are a way to describe patterns in string data. They form a small, separate language that is part of JavaScript and many other languages and systems.

There are two ways to declare `RegExp` in JS.

```js
const re1 = new RegExp("abc");
const re2 = /abc/;
```

Both represent the same pattern.
___

## Testing for mathes

```js
/abc/.test("abcde") // → true
/abc/.test("abxde") // → false
```
___

## Matches

```js
const match = /\d+/.exec("one two 100");

match // → ["100"]
match.index // → 8
```
___

## Replace

```js
"papa".replace("p", "m") // → mapa (only first match is replaced)
"Borobudur".replace(/[ou]/, "a") // → Barobudur

"Borobudur".replace(/[ou]/g, "a") // → Barabadar (all matches were replaced because of 'g' flag)

"Borobudur".replace(/[ou]/g, str => str.toUpperCase()) // → BOrObUdUr (all matches were replaced by function result)

```

## Exercises

1. **Warming up**

For each of the following conditions - write a `RegExp`.

1. _car_ and _cat_
2. _pop_ and _prop_
3. _ferret_, _ferry_, and _ferrari_
4. Any word ending in _ious_
5. A whitespace character followed by a dot(`.`), comma(`,`), colon(`:`), or semicolon(`;`)
6. A word longer than six letters
7. A word without the letter e (or E)

```js
const CarCat = // your code here
const PopProp = // your code here
const Ferrs = // your code here
const Ious = // your code here
const WhiteSpace = // your code here
const LongerThanSix = // your code here
const NoE = // your code here

CarCat.test('black cat') // true
CarCat.test('Camping') // false
```

## Links

- [Regular Expressions](https://eloquentjavascript.net/09_regexp.html)
- [Regular Expressions for Humans](https://refrf.shreyasminocha.me)
- [Online Regex Tester](https://regex101.com/)