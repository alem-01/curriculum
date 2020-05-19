#bash scripting

### Преимущества bash скриптов
- Автоматизация задач, уменьшив риск на ошибки
- Комбинация несколько программ в одно
- Не нужно компилировать

Давайте создадим простой bash скрипт.

создайте файл hello.sh

```shell script
#!/bin/bash
echo "Hello alem!"
```

запустим скрипт

```shell script
bash hello.sh
```
> Hello alem!

для того, что бы запускать файл без использования команды bash
достаточно поменять права файлу

```shell script
chmod +x hello.sh
./hello.sh
```

Для интерактивной программы мы можем использовать команду `read`

Создадим еще один файл welcome.sh
```shell script
#!/bin/bash
echo "ENTER YOUR NAME"
read name
echo WELCOME $name
# comment
```

Мы можем обращаться к переменным, которые создаем через символ `$`
Для комментариев, используется символ `#` - он не выполняется

[Продолжение](http://www.pepedocs.com/notes?tid=linux&nid=lfs101x#ch15_16)

[Основы работы в bash](https://www.youtube.com/watch?v=HwhMyGUGxZ0&list=PLLyG9JTjVd9VTEKisukGLJhl8H2YeIN09)

[Цикл уроков по написанию bash скриптов](https://www.youtube.com/watch?v=PpmyVXCdiDY)