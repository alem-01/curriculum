#Файловая система и навигация

[Видео о файловой системе](https://cs.petrsu.ru/~vadim/shell-html/s_u_2_ru.htm)

При открытии терминала, мы находимся в $HOME.

Для того, что бы вывести файлы, находящиеся в текущей директории \
можно использовать команду `ls`

```sh
ls
```

`ls` - это [программа](https://www.opennet.ru/man.shtml?topic=ls&category=1), которая отображает файлы и их информацию. 

Для навигации, мы можем использовать команду `cd`.

Есть два универсальных аргумента, это `.` и `..`. \
`.` - это текущая директория. \
`..` - это указатель назад.

Мы можем переместиться назад используя

```sh
cd ..
```

[Команды ls, rm, mkdir, pwd, cd, echo](https://www.youtube.com/watch?v=XAfDrMeqoHY)

Переменная `$PWD` хранит в себе информацию о текущем местоположении

```sh
echo $PWD
```

Стоит отметить, что есть несколько типов файлов в Linux
- Директория (папка)
- Регулярный файл
- Ссылка (ярлык)
- Socket и т.д.

[Файлы и папки](https://www.youtube.com/watch?v=1WV-OsaCzbo)

Для создания файла с текстом

```sh
echo "Hello World" > file.txt
```

`>` выполняет роль проводника данных. Т.е. вывод одной команды перенаправился в file.txt
[более подробно](https://www.guru99.com/linux-redirection.html)
[i/o redirection](https://ryanstutorials.net/linuxtutorial/piping.php)

Для просмотра содержимого регулярных файлов есть команда `cat`
```text
cat file.txt
```
> Hello World


Есть более изощренные методы создания файла.
```text
cat <<EOF> filename
Hello World
EOF
```

[EOF](https://ru.wikipedia.org/wiki/EOF)

