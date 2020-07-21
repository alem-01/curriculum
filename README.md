# Curriculum

## Полезные материалы для чтения

[markdown guide](https://www.markdownguide.org/basic-syntax/)

Стиль названия файлов и директорий - [kebab-case](https://techrocks.ru/2018/08/09/most-common-programming-case-types/)

## Создание курса

Для добавления курса необходимо создать директорию в папке ./courses.
```
|__ courses
    |__ course-name [0]
        |-- .config.json [1]
        |-- readme.md [2]
        |__ 1-lesson [3]
            |__ readme.md
            |__ .config.json
```

### [0] course-name
Название курса на английском, хранит в себе директории с уроками и файлы .config.json, readme.md

### [1] .config.json
Файл содержит информацию о курсе
```json
{
    "name": "sign-up",
    "title": "Регистрация",
    "prev": ["none"],
    "x": 0,
    "y": 0,
    "achievement": {
        "name": "sign-up",
        "title": "let`s go",
        "description": "description",
        "key": "6",
        "icon": "https://cdn3.iconfinder.com/data/icons/halloween-128-colored-outline/128/Devil_Hell_Satan_evil_Demon-512.png"
    }
}
```
> *name*: должен иметь значение имени директории <br>
> *title*: название на русском, которое будет выводится на платформе <br>
> *prev*: name пререквизита <br>
> *x, y*: координаты на графе <br>
> *achievement*: будет получено пользователем после завершения курса <br>
>> *name*: название достижения на английском <br>
>> *title*: название на руссоком, которое будет отображаться на платформе <br>
>> *description*: описание достижение <br>
>> *key*: уникально значение <br>
>> *icon*: ссылка на иконку

*Код для генерации ключа*
```bash
python  -c 'import uuid; print(uuid.uuid1())'
```

### [2] readme.md
Файл содержит описание курса. Конвенция по написанию описания курса:
```markdown
# Название Курса

Длинное или короткое описание. Файл должен начинаться с "# Название файла", далее пустая новая линия и на след линии следует описание курса. После описания курса может следовать что угодно.
```

### [3] n-lesson
Название директории урока начинается с **n_**, где n - это номер урока. <br>
Директория содержит файл .config.json c названием урока на русском и файлом readme.md <br>
содержащий контент урока.

> пример 1-lesson/.config.json
```json
{
    "title": "Списки и кортежи",
    "type": "project"
}
``` 

> name: название урока <br>
> type: может иметь два значения (article, project)

> пример 1-lesson/readme.md
```text
# Алгоритмы реализации очереди CPU

https://www.guru99.com/cpu-scheduling-algorithms.html
```

> Можно интегрировать <iframe>

