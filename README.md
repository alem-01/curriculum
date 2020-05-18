# Curriculum

## Создание курса

Для добавления курса необходимо создать директорию в папке ./courses.
```
|__ courses
    `__ course_name [0]
        |-- .config [1]
        |-- readme.md [2]
        `__ 1_lesson [3]
            |__ readme.md
            |__ .config
```

### [0] course_name
Название курса на английском, хранит в себе директории с уроком и файлы .config, readme.md

### [1] .config
Файл содержит информацию о курсе
```text
name: shell-intro
title: Основы shell
prev: none
```
> name: должен иметь значение имени директории \
> title: название на русском, которое будет выводится на платформе \
> prev: name пререквизита \

### [2] readme.md
Файл содержит описание курса

### [3] n_lesson
Название директории урока начинается с **n_**, где n - это номер урока. \
Директория содержит файл .config [4] c названием урока на русском и файлом readme.md \
содержащий контент урока.

> пример 1_lesson/.config
```text
name: Алгоритмы реализации очереди CPU
``` 

> пример 1_lesson/readme.md
```text
# Алгоритмы реализации очереди CPU

https://www.guru99.com/cpu-scheduling-algorithms.html
```