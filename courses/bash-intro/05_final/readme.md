# Финальный проект

### Описание задачи
У вас есть набор данных, в котором хранится информация о пользователях.
Каждая линия разделена символом переноса строки `\n`, каждый столбец разделен `,`


```sh
?> cat data.txt
Gender,FirstName,LastName,UserName,Email,Age,City,Device,Coffee Quantity,OrderAt
Male,Carl,Wilderman,carl,yahoo.com,21->40,Seattle,Safari iPhone,2,afternoon
```

| Gender | FirstName | LastName | UserName | Email | Age | City | Device | Coffee Quantity | OrderAt |
|--------|-----------|----------|----------|-------|-----|------|--------|-----------------|---------|
|1|2|3|4|5|6|7|8|9|10|
|Male|Carl|Wilderman|carl|yahoo.com|21->40|Seattle|Safari iPhone|2|afternoon|


Вам необходимо создать для каждого ряда файл `FirstName_LastName.txt` в котором будут храниться \
ячейки `Gender, Email, Age, City, Device, Coffee`

### Пример

```sh
?> cat data.txt
Gender,FirstName,LastName,UserName,Email,Age,City,Device,Coffee Quantity,Order At,
Male,Carl,Wilderman,carl,yahoo.com,21->40,Seattle,Safari iPhone,2,afternoon,
?> bash my_script.sh
?> ls -l
Carl_Wilderman.txt
?> cat Carl_Wilderman.txt
Male,yahoo.com,21->40,Seattle,Safari iPhone,2,afternoon,
```

### Задача

- Создайте файл data.txt
```sh
?> cat data.txt
Gender,FirstName,LastName,UserName,Email,Age,City,Device,Coffee Quantity,Order At
Male,Carl,Wilderman,carl,yahoo.com,21->40,Seattle,Safari iPhone,2,afternoon
Male,Marvin,Lind,marvin,hotmail.com,66->99,Detroit,Chrome Android,2,afternoon
Female,Shanelle,Marquardt,shanelle,hotmail.com,21->40,Las Vegas,Chrome,1,afternoon
Female,Lavonne,Romaguera,lavonne,yahoo.com,66->99,Seattle,Chrome,2,morning
Male,Derick,McLaughlin,derick,hotmail.com,41->65,Chicago,Chrome Android,1,afternoon
```
- Напишите скрипт

<iframe height="400px" width="100%" src="https://repl.it/@atlekbai/script?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>