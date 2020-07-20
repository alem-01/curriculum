# Файловая система

При открытии терминала, мы находимся в $HOME.

Для того, что бы вывести файлы, находящиеся в текущей директории \
можно использовать команду `ls`

```sh
ls
```

`ls` — это [программа](https://www.opennet.ru/man.shtml?topic=ls&category=1), которая отображает файлы и их информацию. 

Для просмотра базовой информации о функционале программы можно получить, вызвав команду `man <программа>`.
```sh
man ls
```

Для перехода в папки, мы можем использовать команду `cd`.

Есть два универсальных аргумента, это `.` и `..`

`.` — это текущая директория. \
`..` — это указатель назад.

Мы можем переместиться назад используя

```sh
cd ..
```

Переменная `$PWD` хранит в себе информацию о текущем местоположении

```sh
echo $PWD
```

Стоит отметить, что есть несколько типов файлов в Linux
- Директория (папка)
- Регулярный файл
- Ссылка (ярлык)
- Socket и т.д.


<iframe width="100%" height="315" src="https://www.youtube.com/embed/1WV-OsaCzbo?start=112" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

____

### Перенаправления

Для создания файла с текстом

```sh
echo "Hello World" > file.txt
```

`>` выполняет роль проводника данных. Т.е. вывод команды перенаправился в file.txt

Для просмотра содержимого регулярных файлов есть команда `cat`
```sh
cat file.txt
```

```sh
> Hello World
```

Есть более изощренные методы создания файла.

```sh
cat <<EOF> file.txt
Hello World
EOF
```

Для удаления файла используется команда `rm`

```sh
rm file
```

Для создания папки

```sh
mkdir dir
```

Для удаления папки

```sh
rm -rf dir
```

___

### Практическое задание

Ваня Пупкин подключился к удаленному серверу по ssh. Но он не умеет пользоваться терминалом.
В домашней директории пользователя необходимо создать директорию _project_ с файлом _.env_. В файле _.env_ должно быть следующее содержимое:
```
export WELCOME="hello cruel world"
```
Помогите Ване. Решите задачу в этом окне.

<iframe height="400px" width="100%" src="https://repl.it/repls/ScentedInfiniteSpellchecker?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>

___

### Полезные ссылки

[Развернутая статья про файловую систему UNIX](https://cs.petrsu.ru/~vadim/shell-html/s_u_2_ru.htm)

[Команда ls](https://www.opennet.ru/man.shtml?topic=ls&category=1)

[Команды ls, rm, mkdir, pwd, cd, echo](https://www.youtube.com/watch?v=XAfDrMeqoHY)

[Статья про перенаправление вывода команды](https://www.guru99.com/linux-redirection.html)

[Еще круче статья про перенаправления](https://ryanstutorials.net/linuxtutorial/piping.php)

[Что такое EOF?](https://ru.wikipedia.org/wiki/EOF)
