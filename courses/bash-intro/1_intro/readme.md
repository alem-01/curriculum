# Среда shell
<iframe width="100%" height="315" src="https://www.youtube.com/embed/npZYUkXFqd4" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


<iframe height="400px" width="100%" src="https://repl.it/repls/DapperRaggedCodeview?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>

[Bash](https://ru.wikipedia.org/wiki/Bash) - (комaндная оболочка Linux, часто просто «шелл» или «sh») — 
**командный интерпретатор**, используемый в **операционных системах** семейства
**Unix**. В нем пользователь может либо давать команды операционной системе по 
отдельности, либо запускать **скрипты**, состоящие из списка команд. В MacOS и
Linux стандартной командой оболочкой является bash (одна из разновидностей оригинального shell).



[Командный интерпретатор](https://ru.wikipedia.org/wiki/%D0%9E%D0%B1%D0%BE%D0%BB%D0%BE%D1%87%D0%BA%D0%B0_%D0%BE%D0%BF%D0%B5%D1%80%D0%B0%D1%86%D0%B8%D0%BE%D0%BD%D0%BD%D0%BE%D0%B9_%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC%D1%8B) - это программа, которая взаимодействует с пользователей путем принятия
и выполнения команд.

[Операционная система](https://ru.wikipedia.org/wiki/%D0%9E%D0%BF%D0%B5%D1%80%D0%B0%D1%86%D0%B8%D0%BE%D0%BD%D0%BD%D0%B0%D1%8F_%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC%D0%B0) - это большая программа, которая является проводником между пользователем, пользовательскими
приложениями и железом любого вычислительного устройства (компьютер, телефон).

[UNIX](https://ru.wikipedia.org/wiki/Unix) - это семейство операционных систем.

Скрипт - это программа, написанная на любом языке программирования.

Почему стоит научиться работать в командной оболочке bash?
- весь функционал, который есть в проводнике имеется в bash, но в bash он гораздо быстрее
- можно выстраивать взаимодействие нескольких программ
- отличный инструмент для системного/сетевого администрирования

При запуске bash, нас встречает пустой экран со строкой приглашения
```sh
user@group:~/ThistleNonstopList$
```

Мы можем вводить команды, которые терминал будет обрабатывать и выполнять.
Начнем с самого простого, воспользуемся командой `echo` [man echo](https://www.opennet.ru/man.shtml?topic=echo&category=1).

```
echo "Hello world!"
```

нажав enter, bash выполняет нашу инструкцию и в терминале мы увидим.
> Hello world!

давайте запустим команду
```
echo $PWD
```

мы получили полный путь того, где мы находимся в [файловой системе](http://linux.yaroslavl.ru/docs/book/burk/Part4.html)
> /home/runner/ThistleNonstopList

Символ `$` уникальный символ, который устанавливается при обращении к [переменной окружения](https://wiki.archlinux.org/index.php/Environment_variables_(%D0%A0%D1%83%D1%81%D1%81%D0%BA%D0%B8%D0%B9))

Окружение это набор переменных, который используется программами при работе.

Мы можем воспользоваться командой `env` что бы вывести всю таблицу переменных.

```
env
```

И мы получим большой список =)

```
LC_ALL=en_US.UTF-8
LD_LIBRARY_PATH=/home/runner/.apt/usr/lib/x86_64-linux-gnu:/home/runner/.apt/usr/lib/i386-linux-gnu:/home/runner/.apt/usr/lib:
XDG_CONFIG_HOME=/config
LANG=en_US.UTF-8
DISPLAY=MAGIC
HOSTNAME=3b6634655cc9
VIRTUAL_ENV=/opt/virtualenvs/python3
PWD=/home/runner/ThistleNonstopList
HOME=/home/runner
CPATH=
LIBRARY_PATH=/home/runner/.apt/usr/lib/x86_64-linux-gnu:/home/runner/.apt/usr/lib/i386-linux-gnu:/home/runner/.apt/usr/lib:
APT_OPTIONS=-o debug::nolocking=true -o dir::cache=/tmp/apt/cache -o dir::state=/tmp/apt/state -o dir::etc::sourcelist=/tmp/apt/sources/sources.list
TERM=xterm-256color
SHLVL=1
PYTHONPATH=/opt/virtualenvs/python3/lib/python3.8/site-packages
CPPPATH=
PATH=/home/runner/.apt/usr/bin:/opt/virtualenvs/python3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
PS1=${debian_chroot:+($debian_chroot)}\u@\h:\w\$ 
PKG_CONFIG_PATH=/.apt/usr/lib/x86_64-linux-gnu/pkgconfig:/.apt/usr/lib/i386-linux-gnu/pkgconfig:/.apt/usr/lib/pkgconfig:
LD_PRELOAD=/usr/local/lib/repl.so
INCLUDE_PATH=/home/runner/.apt/usr/include:/.apt/usr/include/x86_64-linux-gnu:
_=/usr/bin/env
```

Как пользователи, мы можем спокойно [изменять, удалять, добавлять переменные окружения](https://www.tecmint.com/set-unset-environment-variables-in-linux/),
но эти изменения не будут сохранены после закрытия терминала. Для того, что бы увековечить переменную
у нас есть файл `.bashrc`, данный файл представляет собой один большой скрипт.
Он выполняется при запуске терминала.

