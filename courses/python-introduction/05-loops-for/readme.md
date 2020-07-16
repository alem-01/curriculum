# Цикл for
Во многих языках программирования есть циклы в том или ином виде. Циклы очень полезная и эффективная вещь, она и делает управление программами столь эффективными. Представь что Марку Цукербергу нужно отправить письмо с новогодними поздравления всем работникам facebook, и сколько бы у него времени заняло вручную отправлять эти письма, но с помощью циклов, это можно сделать за несколько строчек кода, и нескольких минут времени.  
Все что циклы делают это повторяют одну и ту же операцию, но с модифицированными данными очень много раз, в случае с Цукербергом, он каждый раз изменяет имя, и почту сотрудника.
Давай представим что перед тобой стоит не очень умная но трудоемкая работа - выписать квадраты первых 10 натуральных чисел. Наивным решением было бы:

<iframe height="400px" width="100%" src="https://repl.it/@SakenMukanov/ActualForestgreenPixel?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>

и так далее до 100, но что будет если тебе нужно выписать 100 или 1000 чисел? К счастью циклы отлично помогают с этой задачей.


Попробуй запустить данный кусок кода в своем интерпретаторе:   


<iframe height="400px" width="100%" src="https://repl.it/@SakenMukanov/ExpensiveProbableWireframes?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>


В данном коде мы используем цикл - for, и задаем ему изначальное значение - 1, и значение остановки цикла 11, т.е. когда переменная **i** достигнет значения 11 цикл остановится.    
Внутри цикла он выполняет ```print(i * i)```, так как **i** итерируется от 1 до 11, мы выписываем квадраты натуральных чисел. Для того, чтобы увеличить чилсо с 10 до 100, достаточно поменть range цикла.


Есть и другой вид итерации циклом for. Выглядит он следующим образом:   

<iframe height="400px" width="100%" src="https://repl.it/@SakenMukanov/VapidAlienatedIdentifier?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>



Данный цикл итерирует по словарю с помощью переменной pair, которая изначально равна первому элементу словаря, и итерирует до последнего элемента словаря.
Данный метод работает не только на словарь, но и на листы, tuples, strings, подробнее можете <a href="https://www.tutorialsteacher.com/python/python-for-loop" target="_blank">посмотреть здесь.</a>



**Для успешной сдачи данного урока, напиши код:**

- <a href="https://github.com/alem-classroom/student-python-introduction-${GITHUB_LOGIN}/blob/master/loops-for" class="repo-button">Цикл в списке</a>   


- <a href="https://github.com/alem-classroom/student-python-introduction-${GITHUB_LOGIN}/blob/master/loops-for" class="repo-button">Цикл в словаре</a>   

Если Github возвращает 404 ошибку, тебе нужно зарегистрироваться в <a href="https://classroom.github.com/a/c9J3nA9U">Github classroom</a>   

