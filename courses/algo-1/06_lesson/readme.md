# Рекурсия  

Рекурсия это процесс вызова функции самой себя, с другими параметрами. Звучит довольно абстракно, попробую привести пример для понимания.  
В математике есть понятие факториал числа, которое подразумевает переумножение всех чисел от 1 до искомого чилса, т.е.
1! = 1 = 1  
2! = 1 * 2 = 2  
3! = 1 * 2 * 3 = 6  и так далее.  Также, можно сказать что факториал числа **n**, это факториал числа **n - 1** умноженный на число **n**, т.е. 
3! = 2! * 3, что в приниципе правильно, но нужно учесть неколько вещей.  
- Факториала негативного числа нет.  
- 0! = 1.  


``` python
num = 5
def factorial(num):
    # Нужно написать рекурсивную функцию для нахождения факториала
    # return ans 

print(factorial(num)

```




``` python
num = 5
def factorial(num):
if (num == 1 or num == 0):
    return 1
else :
    return num * factorial(num - 1) 

print(factorial(num))

```

Схожую аналогию можно сделать для выведения степени числа, например 3^4, три в четвертой степени.  
3^4 = 3^3 * 3  
3^3 = 3^2 * 3  
3^2 = 3^1 * 3  
3^1 = 3^0 * 3  
3^0 = 1  

``` python  
num = 7
pwr = 2
def power(num, pwr):
    # верни num в степени pwr
    # return ans
print(power(num, pwr))
```

``` python  
num = 7
pwr = 2
def power(num, pwr):
    if (pwr == 1):
        return num
    elif (pwr == 0):
        return 1
    else:
        return num * power(num, pwr - 1) 

print(power(num, pwr))
```


Также, прочитай про числа фибоначи, и попробуй сделать функцию для вывода числа фибоначи.

``` python
num = 10

def fib(n):
    # верни n'ное число фибоначчи
    # return ans

for i in range (0, num):
    print(fib(i))


```


``` python 

num = 10
def fib(num):
    if (num == 1):
        return 1
    if (num == 0):
        return 0
    return (fib(num - 1) + fib(num - 2))

for i in range (0, num):
    print(fib(i))

```

