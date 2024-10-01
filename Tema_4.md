# Тема 4. Функции и модули
Отчет по Теме #3 выполнил:
- Тачеев Пётр Алексеевич
- ПИЭ-21-1

| Задание | Лаб_раб | Сам_раб |
| ------ |---------|------|
| Задание 1 | +       | +    |
| Задание 2 | +       | +    |
| Задание 3 | +       | +    |
| Задание 4 | +       | +    |
| Задание 5 | +       | +    |
| Задание 6 | +       |     |
| Задание 7 | +       |     |
| Задание 8 | +       |     |
| Задание 9 | +       |      |
| Задание 10 | +       |      |

знак "+" - задание выполнено; знак "-" - задание не выполнено;

Работу проверили:
- к.э.н., доцент Панов М.А.

## Лабораторная работа №1
### Напишите функцию, которая выполняет любые арифметические действия и выводит результат в консоль. Вызовите функцию используя “точку входа”

```python
def main():
    print(2 + 2)
if __name__ == '__main__':
    main()
```
### Результат.
https://github.com/ptacheev/-/blob/a2aa9e65028eb8a18de8db6fed7e5979f0448a83/images/tema4/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-10-01%20211153.png

## Выводы

def main():
    print(2 + 2)
if __name__ == '__main__':
    main()

## Лабораторная работа №2
## Напишите функцию, которая выполняет любые арифметические действия, возвращает при помощи return значение в место, откуда вызывали функцию. Выведите результат в консоль. Вызовите функцию используя “точку входа”.
```python
def main():
    result = 2 + 2
    return result
if __name__ == '__main__':
    answer = main()
    print(answer)
```
### Результат.
https://github.com/ptacheev/-/blob/a2aa9e65028eb8a18de8db6fed7e5979f0448a83/images/tema4/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-10-01%20211247.png

## Выводы

def main():
    result = 2 + 2
    return result
if __name__ == '__main__':
    answer = main()
    print(answer)


## Лабораторная работа №3
### Напишите функцию, в которую передаются два аргумента, над ними производится арифметическое действие, результат возвращается туда, откуда эту функцию вызывали. Выведите результат в консоль. Вызовите функцию в любом небольшом цикле.
```python
def main(one, two):
    result = one + two
    return result
for i in range(5):
    x = 1
    y = 10
    answer = main(x, y)
    print(answer)

```
### Результат.
https://github.com/ptacheev/-/blob/a2aa9e65028eb8a18de8db6fed7e5979f0448a83/images/tema4/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-10-01%20211559.png
## Выводы

def main(one, two):
    result = one + two
    return result
for i in range(5):
    x = 1
    y = 10
    answer = main(x, y)
    print(answer)
## Лабораторная работа №4
### Напишите функцию, на вход которой подается какое-то изначальное неизвестное количество аргументов, над которыми будет производится арифметические действия. Для выполнения задания необходимо использовать кортеж “*args”.

```python
def main(x, *args):
    one = x
    two = sum(args)
    three = float(len(args))
    print(f"one={one}\ntwo={two}\nthree={three}")
if __name__ == '__main__':
    result = main(10, 0 ,1, 2,-1,0, -1, 1, 2)
```
### Результат.
https://github.com/ptacheev/-/blob/a2aa9e65028eb8a18de8db6fed7e5979f0448a83/images/tema4/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-10-01%20211936.png

## Выводы

def main(x, *args):
    one = x
    two = sum(args)
    three = float(len(args))
    print(f"one={one}\ntwo={two}\nthree={three}")
if __name__ == '__main__':
    result = main(10, 0 ,1, 2,-1,0, -1, 1, 2)
## Лабораторная работа №5
### Напишите функцию, которая на вход получает кортеж “**kwargs” и при помощи цикла выводит значения, поступившие в функцию. На скриншоте ниже указаны два варианта вызова функции с “**kwargs” и два варианта работы с данными, поступившими в эту функцию. 

```python
def main(**kwargs):
    for i in kwargs.items():
        print(i[0],i[1])
    print()
    for key in kwargs:
        print(f"{key} = {kwargs[key]}")
if __name__ == '__main__':
            main(x = [1, 2, 3], y =[3, 3, 0], z =[2, 3, 0], q=[3, 3, 0], w=[3, 3, 0])
            print()
            main(**{'x':[1,2,3],'y':[3, 3, 0]})

```
### Результат.
https://github.com/ptacheev/-/blob/a2aa9e65028eb8a18de8db6fed7e5979f0448a83/images/tema4/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-10-01%20212405.png


## Выводы

def main(**kwargs):
    for i in kwargs.items():
        print(i[0],i[1])
    print()
    for key in kwargs:
        print(f"{key} = {kwargs[key]}")
if __name__ == '__main__':
            main(x = [1, 2, 3], y =[3, 3, 0], z =[2, 3, 0], q=[3, 3, 0], w=[3, 3, 0])
            print()
            main(**{'x':[1,2,3],'y':[3, 3, 0]})
## Лабораторная работа №6
### Напишите две функции. Первая – получает в виде параметра “**kwargs”. Вторая считает среднее арифметическое из значений первой функции. Вызовите первую функцию используя “точку входа” и минимум 4 аргумента

```python
def main(**kwargs):
    for i,j in kwargs.items():
        print(f"{i}.Mean = {mean(j)}")
def mean(data):
    return sum(data) / float(len(data))
if __name__ == '__main__':
    main(x=[1, 2, 3], y=[3, 3, 0])

```
### Результат.
https://github.com/ptacheev/-/blob/a2aa9e65028eb8a18de8db6fed7e5979f0448a83/images/tema4/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-10-01%20212700.png

## Выводы
def main(**kwargs):
    for i,j in kwargs.items():
        print(f"{i}.Mean = {mean(j)}")
def mean(data):
    return sum(data) / float(len(data))
if __name__ == '__main__':
    main(x=[1, 2, 3], y=[3, 3, 0])
## Лабораторная работа №7
### Создайте дополнительный файл .py. Напишите в нем любую функцию, которая будет что угодно выводить в консоль, но не вызывайте ее в нем. Откройте файл main.py, импортируйте в него функцию из нового файла и при помощи “точки входа” вызовите эту функцию

```python
from for_imp import say_hello
if __name__ == '__main__':
    say_hello()
```
### Результат.
https://github.com/ptacheev/-/blob/a2aa9e65028eb8a18de8db6fed7e5979f0448a83/images/tema4/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-10-01%20212913.png

## Выводы

from for_imp import say_hello
if __name__ == '__main__':
    say_hello()
## Лабораторная работа №8
### Напишите программу, которая будет выводить корень, синус, косинус полученного от пользователя числа

```python
import math
def main():
    value = int(input('Введите значение: '))
    print(math.sqrt(value))
    print(math.sin(value))
    print(math.cos(value))
if __name__ == '__main__':
    main()

```
### Результат.
https://github.com/ptacheev/-/blob/a2aa9e65028eb8a18de8db6fed7e5979f0448a83/images/tema4/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-10-01%20212913.png
## Выводы
import math
def main():
    value = int(input('Введите значение: '))
    print(math.sqrt(value))
    print(math.sin(value))
    print(math.cos(value))
if __name__ == '__main__':
    main()

## Лабораторная работа №9
### Напишите программу, которая будет рассчитывать какой день недели будет через n-нное количество дней, которые укажет пользователь.

```python
from datetime import datetime as dt
from datetime import timedelta as td
def main():
    print(
        f"Сегодня {dt.today().date()}."
        f"День недели - {dt.today().isoweekday()}."
    )
    n = int(input("Введите кол-во дней: "))
    today = dt.today()
    result = today + td(days = n)
    print(
        f" Через {n} дней будет{result.date()}."
        f"День недели - {result.isoweekday()}."
    )
if __name__ == '__main__':
    main()

```
### Результат.
https://github.com/ptacheev/-/blob/a2aa9e65028eb8a18de8db6fed7e5979f0448a83/images/tema4/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-10-01%20212913.png
## Выводы

from datetime import datetime as dt
from datetime import timedelta as td
def main():
    print(
        f"Сегодня {dt.today().date()}."
        f"День недели - {dt.today().isoweekday()}."
    )
    n = int(input("Введите кол-во дней: "))
    today = dt.today()
    result = today + td(days = n)
    print(
        f" Через {n} дней будет{result.date()}."
        f"День недели - {result.isoweekday()}."
    )
if __name__ == '__main__':
    main()

## Лабораторная работа №10
### Напишите программу с использованием глобальных переменных, которая будет считать площадь треугольника или прямоугольника в зависимости от того, что выберет пользователь. Получение всей необходимой информации реализовать через input(), а подсчет площадей выполнить при помощи функций. Результатом программы будет число, равное площади, необходимой фигуры.

```python
global result
def rectangle():
    a = float(input("Ширина: "))
    b = float(input("Высота: "))
    global result
    result = a + b
def triangle():
    a = float(input("Основание: "))
    h = float(input("Высота: "))
    global result
    result = 0.5 * a * h
figure = input("1 - прямоугольникб 2- треугольник: ")
if figure == '1':
    rectangle()
elif figure == '2':
    triangle()
print(f"Площадь {result}")


```
### Результат.
https://github.com/ptacheev/-/blob/a2aa9e65028eb8a18de8db6fed7e5979f0448a83/images/tema4/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-10-01%20214438.png
## Выводы
global result
def rectangle():
    a = float(input("Ширина: "))
    b = float(input("Высота: "))
    global result
    result = a + b
def triangle():
    a = float(input("Основание: "))
    h = float(input("Высота: "))
    global result
    result = 0.5 * a * h
figure = input("1 - прямоугольникб 2- треугольник: ")
if figure == '1':
    rectangle()
elif figure == '2':
    triangle()
print(f"Площадь {result}")

## Самостоятельная работа №1
###  Дайте подробный комментарий для кода, написанного ниже.
Комментарий нужен для каждой строчки кода, нужно описать что она
делает. Не забудьте, что функции комментируются по-особенному

```python
from datetime import datetime # импорт класа datetime и функции sqrt из соответствующих библиотек
from math import sqrt
def main(**kwargs):
    for key in kwargs.items():#цикл будет проходить через все эелементы кортежа
        result = sqrt(key[1][0]**2 +key[1][1]**2) #корень суммы квадратов элементов одного из под кортежа
        print(result)
if __name__ == '__main__':# точка входа
    start_time = datetime.now() #время начала выполнения программы
    main(#функция принимает двумерный кортеж
        one =[10, 3], 
        two=[5, 4],
        three=[15, 13],
        four=[93, 53],
        five=[133, 15],
    )
time_costs = datetime.now()-start_time #из нынешнего вычитается время старта программы и выводиться
print(f"Время выполнения команды - {time_costs}")


```
### Результат.
https://github.com/ptacheev/-/blob/a2aa9e65028eb8a18de8db6fed7e5979f0448a83/images/tema4/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-10-01%20222635.png


## Самостоятельная работа №2
### 2) Напишите программу, которая будет заменять игральную кость с 6 гранями. Если значение равно 5 или 6, то в консоль выводится «Вы победили», если значения 3 или 4, то вы рекурсивно должны вызвать эту же функцию, если значение 1 или 2, то в консоль выводится «Вы проиграли». При этом каждый вызов функции необходимо выводить в консоль значение “кубика”. Для выполнения задания необходимо использовать стандартную библиотеку random. Программу нужно написать, используя одну функцию и “точку входа”

```python
from random import randint
def die():
    x = randint(1,6)
    print(x)
    if x == 1 or x == 2:
        return 'Вы Проиграли!'
    elif (x == 3 or x == 4):
        print('Переброс')
        return(die())
    else:
        return 'Вы Выйграли!'
if __name__ == '__main__':
    print(die())

```
### Результат.
https://github.com/ptacheev/-/blob/a2aa9e65028eb8a18de8db6fed7e5979f0448a83/images/tema4/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-10-01%20215004.png

## Выводы

from random import randint
def die():
    x = randint(1,6)
    print(x)
    if x == 1 or x == 2:
        return 'Вы Проиграли!'
    elif (x == 3 or x == 4):
        print('Переброс')
        return(die())
    else:
        return 'Вы Выйграли!'
if __name__ == '__main__':
    print(die())
## Самостоятельная работа №3
### 3) Напишите программу, которая будет выводить текущее время, с точностью до секунд на протяжении 5 секунд. Программу нужно написать с использованием цикла. Подсказка: необходимо использовать модуль datetime и time, а также вам необходимо как-то “усыплять” программу на 1 секунду
```python
import datetime
import time
for i in range(5):
    print(datetime.datetime.now().time())
    time.sleep(1)

```
### Результат.
https://github.com/ptacheev/-/blob/a2aa9e65028eb8a18de8db6fed7e5979f0448a83/images/tema4/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-10-01%20220106.png
    
## Выводы
import datetime
import time
for i in range(5):
    print(datetime.datetime.now().time())
    time.sleep(1)

## Самостоятельная работа №4
### Напишите программу, которая считает среднее арифметическое от аргументов вызываемое функции, с условием того, что изначальное количество этих аргументов неизвестно. Программу необходимо реализовать используя одну функцию и “точку входа”.

```python
def main(*args):
    return(sum(args)/len(args))
if __name__ == "__main__":
    print(main(10, 40, 43, 22, 93))


```
### Результат.
https://github.com/ptacheev/-/blob/a2aa9e65028eb8a18de8db6fed7e5979f0448a83/images/tema4/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-10-01%20220303.png

## Выводы
def main(*args):
    return(sum(args)/len(args))
if __name__ == "__main__":
    print(main(10, 40, 43, 22, 93))

## Самостоятельная работа №5
### 5) Создайте два Python файла, в одном будет выполняться вычисление площади треугольника при помощи формулы Герона (необходимо реализовать через функцию), а во втором будет происходить взаимодействие с пользователем (получение всей необходимой информации и вывод результатов). Напишите эту программу и выведите в консоль полученную площадь.


```python
from triangle import square
a = int(input("Введите первую сторону треугольника "))
b = int(input("Введите вторую сторону треугольника "))
c = int(input("Введите третьую сторону треугольника "))
print(f"Площадь треугольника равна {square(a,b,c)}")

```
### Результат.
https://github.com/ptacheev/-/blob/a2aa9e65028eb8a18de8db6fed7e5979f0448a83/images/tema4/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-10-01%20220915.png
## triangle
```python
import math
def square(a, b, c):
    p = (a + b + c)/2
    return (math.sqrt(p*(p-a)*(p-b)*(p-c)))
```

## Общие выводы по теме
- Развернутый вывод
- Рассмотренны Функции и модули и сделаны лабораторные и самостаятельные работы