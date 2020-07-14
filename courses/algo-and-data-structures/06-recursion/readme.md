# Рекурсия  

Рекурсия это процесс вызова функции самой себя, с другими параметрами. Звучит довольно абстракно, попробую привести пример для понимания.  
В математике есть понятие факториал числа, которое подразумевает переумножение всех чисел от 1 до искомого чилса, т.е.
1! = 1 = 1  
2! = 1 * 2 = 2  
3! = 1 * 2 * 3 = 6  и так далее.  Также, можно сказать что факториал числа **n**, это факториал числа **n - 1** умноженный на число **n**, т.е. 
3! = 2! * 3, что в приниципе правильно, но нужно учесть неколько вещей.  
- Факториала негативного числа нет.  
- 0! = 1.  

Схожую аналогию можно сделать для выведения степени числа, например 3^4, три в четвертой степени.  
3^4 = 3^3 * 3  
3^3 = 3^2 * 3  
3^2 = 3^1 * 3  
3^1 = 3^0 * 3  
3^0 = 1  


Также, прочитай про числа Фибоначчи, и попробуй сделать функцию для вывода числа фибоначи.

<iframe height="400px" width="100%" src="https://repl.it/@SakenMukanov/RectangularSupportiveMuse?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>

**Для успешной сдачи данного урока, напиши код:**

- <a href="https://github.com/alem-classroom/student-algo-1-${GITHUB_LOGIN}/tree/master/recursion" class="repo-button">Чисел Фибоначчи рекурсией</a>   


Если Github возвращает 404 ошибку, тебе нужно зарегистрироваться в <a href="https://classroom.github.com/a/QaSKclaO">Github classroom</a>   
