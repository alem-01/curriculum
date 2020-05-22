# bash scripting

Преимущества bash скриптов
- Автоматизация задач, уменьшив риск на ошибки
- Комбинация нескольких программ в одно
- Не нужно компилировать

Давайте создадим простой bash скрипт.

Cоздайте файл hello.sh со следующим содержимым.

```sh
#!/bin/bash
echo "Hello alem!"
```

запустим скрипт

```sh
bash hello.sh
```

```sh
$> Hello alem!
```

для того, что бы запускать файл без использования команды bash
достаточно поменять права файлу.

```sh
chmod +x hello.sh # меняем права
./hello.sh        # запускаем скрипт
```
____

Для чтения ввода мы можем использовать команду `read`

Создадим еще один файл welcome.sh
```sh
#!/bin/bash
echo "ENTER YOUR NAME"
read name # читаем ввод
echo "Welcome, $name"
```

Мы можем обращаться к переменным, которые создаем через символ `$`

Для комментариев, используется символ `#` — он не выполняется

___

### Практическое занятие

Создайте скрипт которые считывает имя, возраст и страну и выведет:
```
Hello, <имя>! You are age of <возраст> and you are from <страна>.
```

<iframe height="400px" width="100%" src="https://repl.it/@atlekbai/script?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>

___

### Полезные ссылки

[Продолжение](http://www.pepedocs.com/notes?tid=linux&nid=lfs101x#ch15_16)

[Основы работы в bash](https://www.youtube.com/watch?v=HwhMyGUGxZ0&list=PLLyG9JTjVd9VTEKisukGLJhl8H2YeIN09)

[Цикл уроков по написанию bash скриптов](https://www.youtube.com/watch?v=PpmyVXCdiDY)