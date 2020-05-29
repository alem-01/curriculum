## Основы JavaScript

Если вы никогда до этого не пробовали программировать, 
то для начала необходимо разобраться в синтаксисе языка, 
а также, что из себя представляет алгоритм.

<iframe width="100%" height="315" src="https://www.youtube.com/embed/_J-3nt9bhbI" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

Любая задачка, требующая решения состоит из `алгоритмов`. \
`Алгортим`, представляет собой набор инструкций.\
`Инструкция` это набор операций и переменных.\
Давайте решим простую задачку.\
Нам необходимо напечатать квадрат nxn из `#`, где `n` - это значение, введенное пользователем.
```
####
####
####
####
```

for (let i = 0; i < n; i++)
    for (let z = 0; z < n; z++)

Наше решение псевдокодом будет выглядеть так:
```
прочитать n в переменную size
создать переменную x = 0
цикл от x до size
    создать переменную line
    цикл от y до size
        добавить в переменную line `#`
        увеличить y
    вывести line
    увеличить x
```

Для создания переменных есть два ключевых слова
```js
let variable = 0; // переменная, которую можно изменить
const constant = 0; // константа, нельзя изменить
```

> Очень важно писать чистый код.
> [про стиль кода](https://learn.javascript.ru/coding-style)

[let](https://devdocs.io/javascript/statements/let)

[const](https://devdocs.io/javascript/statements/const)

Для считывания информации от пользователя существует функция `prompt`

[functions](https://devdocs.io/javascript/operators/function)
<iframe width="100%" height="315" src="https://www.youtube.com/embed/RfW4MwkT0hw" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

Нам необходимо узнать, как создать цикл в JS.

<iframe width="100%" height="315" src="https://www.youtube.com/embed/TREWm2urXtk" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

Теперь мы можем написать код, использовав новые знания из видео.

```js
const size = parseInt(prompt());        // сохраняем числовое значение от пользователя в переменную size

for (let x = 0; i < size; i++) {        // цикл от 0 до `n`
    let line = "";                      // создаем переменную line в которую будут добавляться `#`
    for (let y = 0; y < size; y++) {    // цикл от 0 до `n`
        line = line + "#";              // добавить `#` в строку
    }
    console.log(line);                  // вывести строку
}
```

<iframe height="400px" width="100%" src="https://repl.it/repls/DoubleHighlevelBootstrapping?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>
