# Тема 2. Базовые операции языка Python
Отчет по Теме #2 выполнил(а):
- Тачеев Пётр Алексеевич
- ПИЭ-21-1

| Задание | Лаб_раб | Сам_раб |
| ------ |---------|---------|
| Задание 1 | +       | +       |
| Задание 2 | +       | +       |
| Задание 3 | +       | +       |
| Задание 4 | +       | +       |
| Задание 5 | +       | +       |
| Задание 6 | +       | +       |
| Задание 7 | +       | +       |
| Задание 8 | +       | +       |
| Задание 9 | +       | +       |
| Задание 10 | +       | +       |

знак "+" - задание выполнено; знак "-" - задание не выполнено;

Работу проверили:
- к.э.н., доцент Панов М.А.

## Лабораторная работа №1
### Выведите в консоль три строки. Первая – любое число. Вторая – любое число в виде строки. Третья – любое число с плавающей точкой.

```python
print(123)
print('123')
print(1.23)
```
### Результат.
https://github.com/ptacheev/-/blob/87bcb3fe603311dbf55d2a51e3d05a64e4a67bfc/images/1.png

## Выводы

В данном коде выводятся три строки с использованием функции `print()`. Каждая строка содержит разные значения:

1. `print(123)`: Выводится целое число 123. Это число не взаимодействует со строковыми операциями и выводится как есть.

2. `print('123')`: Выводится строка '123', так как она заключена в одинарные кавычки. В этом случае это текстовая строка, а не число.

3. `print(1.23)`: Выводится число с плавающей точкой 1.23. Так же, как и в первом случае, оно выводится как числовое значение.

## Лабораторная работа №2
### https://github.com/ptacheev/-/blob/87bcb3fe603311dbf55d2a51e3d05a64e4a67bfc/images/21.png

```python
print(1823 - 486)
print(5.1 + 8.27)
print(3 + 7.04 + 1 + 2.33)

```
### Результат.
https://github.com/ptacheev/-/blob/87bcb3fe603311dbf55d2a51e3d05a64e4a67bfc/images/2.png

## Выводы

1 - print(1823 - 486)    выводиться целый ответ между целым и целым
2 - print(5.1 + 8.27)    смешанное число между смешанным и смешанным
3 - print(3 + 7.04 + 1 + 2.33) смешанное между множеством смешанных и целых


## Лабораторная работа №3
### https://github.com/ptacheev/-/blob/87bcb3fe603311dbf55d2a51e3d05a64e4a67bfc/images/22.png
```python
print('Привет, Мир!')
world = 'Мир'
print (f"Привет, {world}!")
one = 'Привет, '
two = 'Мир!'
print(one + two)

```
### Результат.
https://github.com/ptacheev/-/blob/87bcb3fe603311dbf55d2a51e3d05a64e4a67bfc/images/3.png

## Выводы

print('Привет, Мир!')  выводиться нормально
world = 'Мир'
print (f"Привет, {world}!") благодаря ф строке выводиться нормально , учитывая переменную
one = 'Привет, '
two = 'Мир!'
print(one + two) выводит несколько переменных как одну строку

## Лабораторная работа №4
### https://github.com/ptacheev/-/blob/87bcb3fe603311dbf55d2a51e3d05a64e4a67bfc/images/23.png

```python
one ='Hello'
print(bool(one))
two = 142
print(float(two))
three = None
print(str(three))
```
### Результат.
https://github.com/ptacheev/-/blob/87bcb3fe603311dbf55d2a51e3d05a64e4a67bfc/images/4.png

## Выводы

one ='Hello'
print(bool(one)) строка превращается в булевую переменную
two = 142
print(float(two)) из целого в число с плаващиющей точкой
three = None
print(str(three)) 

## Лабораторная работа №5
### https://github.com/ptacheev/-/blob/87bcb3fe603311dbf55d2a51e3d05a64e4a67bfc/images/24.png

```python
one = input('one:')
two = input('two:')
three = input('three:')
print(one,two,three)

```
### Результат.
https://github.com/ptacheev/-/blob/87bcb3fe603311dbf55d2a51e3d05a64e4a67bfc/images/5.png

## Выводы

one = input('one:') ввод производиться с помощью input()
two = input('two:')
three = input('three:')
print(one,two,three)

## Лабораторная работа №6
### https://github.com/ptacheev/-/blob/87bcb3fe603311dbf55d2a51e3d05a64e4a67bfc/images/25.png

```python
a = 12
b = 5
print( a**b)
print( a/b)
print(a//b)
print(a%b)

```
### Результат.
https://github.com/ptacheev/-/blob/87bcb3fe603311dbf55d2a51e3d05a64e4a67bfc/images/6.png

## Выводы

a = 12
b = 5
print( a**b)операция возведения в степень
print( a/b) цделения
print(a//b) елочисленного деления
print(a%b) остаток от деления
## Лабораторная работа №7
### https://github.com/ptacheev/-/blob/87bcb3fe603311dbf55d2a51e3d05a64e4a67bfc/images/26.png

```python
line = 'EEEEl'
print(line*553) 
```
### Результат.
https://github.com/ptacheev/-/blob/87bcb3fe603311dbf55d2a51e3d05a64e4a67bfc/images/7.png

## Выводы

line = 'EEEEl'
print(line*553)умножение строки на число дает много таких строк подряд
## Лабораторная работа №8
### https://github.com/ptacheev/-/blob/87bcb3fe603311dbf55d2a51e3d05a64e4a67bfc/images/27.png

```python
sentence = 'Hello World'
print(sentence.count('o'))

```
### Результат.
https://github.com/ptacheev/-/blob/87bcb3fe603311dbf55d2a51e3d05a64e4a67bfc/images/8.png

## Выводы

sentence = 'Hello World'
print(sentence.count('o')) с помощью count() можно подсчитать количество символов в строке

## Лабораторная работа №9
### https://github.com/ptacheev/-/blob/87bcb3fe603311dbf55d2a51e3d05a64e4a67bfc/images/28.png

```python
print('Hello\nWorld')

```
### Результат.
https://github.com/ptacheev/-/blob/87bcb3fe603311dbf55d2a51e3d05a64e4a67bfc/images/9.png

## Выводы

print('Hello\nWorld') \n переносит строку

## Лабораторная работа №10
### https://github.com/ptacheev/-/blob/87bcb3fe603311dbf55d2a51e3d05a64e4a67bfc/images/29.png

```python
sentence = 'Hello World'
print(sentence[1])
print(sentence[:5])

```
### Результат.

https://github.com/ptacheev/-/blob/87bcb3fe603311dbf55d2a51e3d05a64e4a67bfc/images/10.png
## Выводы
sentence = 'Hello World' с помощью индексов можно разделить строку
print(sentence[1])
print(sentence[:5])

## Самостоятельная работа №1
### https://github.com/ptacheev/-/blob/87bcb3fe603311dbf55d2a51e3d05a64e4a67bfc/images/11.png

```python
print(bool(0))

```
### Результат.
https://github.com/ptacheev/-/blob/87bcb3fe603311dbf55d2a51e3d05a64e4a67bfc/images/30.png

## Выводы

print(bool(0)) при переходе 0 в булевую переменную будет False

## Самостоятельная работа №2
### https://github.com/ptacheev/-/blob/87bcb3fe603311dbf55d2a51e3d05a64e4a67bfc/images/31.png

```python
a,b,c = 1,1,1;
print(a,' ',b,' ',c)

```
### Результат.
https://github.com/ptacheev/-/blob/87bcb3fe603311dbf55d2a51e3d05a64e4a67bfc/images/12.png

## Выводы

a,b,c = 1,1,1; Переменные можно обьявлять все в одной строке
print(a,' ',b,' ',c)

## Самостоятельная работа №3
### https://github.com/ptacheev/-/blob/87bcb3fe603311dbf55d2a51e3d05a64e4a67bfc/images/32.png

```python
a = int(input())
if (isinstance(a,int)): print(a)

```
### Результат.
https://github.com/ptacheev/-/blob/87bcb3fe603311dbf55d2a51e3d05a64e4a67bfc/images/13.png   

## Выводы

a = int(input()) преобразование из строки в число
if (isinstance(a,int)): print(a)

## Самостоятельная работа №4
### https://github.com/ptacheev/-/blob/87bcb3fe603311dbf55d2a51e3d05a64e4a67bfc/images/34.png

```python
s = 'r323r'
print(s*43532)

```
### Результат.
https://github.com/ptacheev/-/blob/87bcb3fe603311dbf55d2a51e3d05a64e4a67bfc/images/14.png

## Выводы

s = 'r323r' изначально 5 символов
print(s*43532)теперь символов больше 16

## Самостоятельная работа №5
### https://github.com/ptacheev/-/blob/87bcb3fe603311dbf55d2a51e3d05a64e4a67bfc/images/35.png

```python
day, month, year = 1,'may',23
print(f"Сегодня {day} {month} {year}.Всего Хорошего!")


```
### Результат.
https://github.com/ptacheev/-/blob/87bcb3fe603311dbf55d2a51e3d05a64e4a67bfc/images/15.png

## Выводы

day, month, year = 1,'may',23
print(f"Сегодня {day} {month} {year}.Всего Хорошего!") через f строку можно выводить переменные прямо среди текста

## Самостоятельная работа №6
### https://github.com/ptacheev/-/blob/87bcb3fe603311dbf55d2a51e3d05a64e4a67bfc/images/36.png

```python
a ='Hello World'
print(a[:5]+' my '+a[6:])
```
### Результат.
https://github.com/ptacheev/-/blob/87bcb3fe603311dbf55d2a51e3d05a64e4a67bfc/images/16.png

## Выводы

a ='Hello World'
print(a[:5]+' my '+a[6:]) индексы у строки позволяют вставить еще строку внутрь
## Самостоятельная работа №7
### https://github.com/ptacheev/-/blob/87bcb3fe603311dbf55d2a51e3d05a64e4a67bfc/images/37.png

```python
print(len('Hello World'))

```
### Результат.
https://github.com/ptacheev/-/blob/87bcb3fe603311dbf55d2a51e3d05a64e4a67bfc/images/17.png

## Выводы

print(len('Hello World')) len  определяет длинну строки

## Самостоятельная работа №8
### https://github.com/ptacheev/-/blob/87bcb3fe603311dbf55d2a51e3d05a64e4a67bfc/images/38.png

```python
a = 'HELLO WORLD'
print(a.lower())

```
### Результат.
https://github.com/ptacheev/-/blob/87bcb3fe603311dbf55d2a51e3d05a64e4a67bfc/images/18.png

## Выводы

a = 'HELLO WORLD'
print(a.lower())  lower() делает весь регистр строки нижним

## Самостоятельная работа №9
### Вывести строку 'Hello World' заменить первове слово верхним а второе нижним регистром

```python
a = 'Hello World'.split() 
print(a[0].upper() +' '+ a[1].lower())


```
### Результат.
https://github.com/ptacheev/-/blob/87bcb3fe603311dbf55d2a51e3d05a64e4a67bfc/images/19.png

## Выводы

a = 'Hello World'.split() переделывает строку в массив разделяя пробелом
print(a[0].upper() +' '+ a[1].lower()) первый элемент в верхний а второй элемент в нижний регистр

## Самостоятельная работа №10
### Вывести предложение, случайно определить регистр каждого слова в нем

```python
import random
a ='Hello my beatiful World'.split()
i = 0
for i in range(1, len(a)):
    if (random.randint(1,2) == 1):
        a[i] = a[i].lower();
    else:
        a[i] = a[i].upper();
print(a[0]+' '+a[1]+' '+a[2]+' '+a[3] )

```
### Результат.
https://github.com/ptacheev/-/blob/87bcb3fe603311dbf55d2a51e3d05a64e4a67bfc/images/20.png

## Выводы

import random
a ='Hello my beatiful World'.split()
i = 0
for i in range(1, len(a)): случайный регистр в каждом слове
    if (random.randint(1,2) == 1):
        a[i] = a[i].lower();
    else:
        a[i] = a[i].upper();
print(a[0]+' '+a[1]+' '+a[2]+' '+a[3] )

## Общие выводы по теме
- Развернутый вывод
- Рассмотренны базовые операции python и сделаны лабораторные и самостаятельные работы