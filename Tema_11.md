# Тема 11. Итераторы и генераторы
Отчет по Теме #11 выполнил:
- Тачеев Пётр Алексеевич
- ПИЭ-21-1

| Задание    | Лаб_раб | Сам_раб |
|------------|---------|--|
| Задание 1  | +       | + |
| Задание 2  | +       | + |
| Задание 3  | +       |  |
| Задание 4  | +       |  |
| Задание 5  | +       |  |



знак "+" - задание выполнено; знак "-" - задание не выполнено;

Работу проверили:
- к.э.н., доцент Панов М.А.

## Лабораторная работа №1
### Простой итератор, но у него нет гибкой настройки, например его нельзя развернуть. Он работает просто как next(), но нет prev()
```python
numbers = [0, 1, 2, 3, 4, 5]
for item in numbers:
    print(item)
  
```

### Результат.
https://github.com/ptacheev/-/blob/a396cd8c4e6dc388ca8a0beb5026bafb3559ec30/images/tema%2011/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-11-24%20194433.png

## Лабораторная работа №2
### класс итератор с гибкой настройкой и удобными применением 

```python
class CountDown:
    def __init__(self,start):
        self.count = start + 1
    def __iter__(self):
        return self
    def __next__(self):
        self.count -= 1
        if self.count < 0:
            raise StopIteration
        return self.count
if __name__ == '__main__':
    counter = CountDown(5)
    for i in counter:
        print(i)
```
### Результат.
https://github.com/ptacheev/-/blob/a396cd8c4e6dc388ca8a0beb5026bafb3559ec30/images/tema%2011/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-11-24%20194721.png
## Лабораторная работа №3
### Генератор списка

```python
a = [i ** 2 for i in range(1, 5)]
print('a - ', a)
for i in a:
    print(i)
print('iter(a) - ', iter(a))
for i in a:
    print(i)


```
### Результат.
https://github.com/ptacheev/-/blob/a396cd8c4e6dc388ca8a0beb5026bafb3559ec30/images/tema%2011/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-11-24%20194851.png

## Лабораторная работа №4
### Выражения генераторы

```python
b = (i ** 2 for i in range(1, 5))
print(b)
print('first')
for i in b:
    print(i)
print('second')
for i in b:
    print(i)

```
### Результат.
https://github.com/ptacheev/-/blob/a396cd8c4e6dc388ca8a0beb5026bafb3559ec30/images/tema%2011/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-11-24%20195202.png


## Лабораторная работа №5
### Такой же счетчик, как и в первом задании, только это генератор и использует yield
```python
def countdown(count):
    while count >= 0:
        yield count
        count -= 1

if __name__ == '__main__':
    counter = countdown(5)
    for i in counter:
        print(i)

```
### Результат.
https://github.com/ptacheev/-/blob/a396cd8c4e6dc388ca8a0beb5026bafb3559ec30/images/tema%2011/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-11-24%20195346.png


## Самостоятельная работа №1
### Вас никак не могут оставить числа Фибоначчи, очень уж они вас заинтересовали. Изучив новые возможности Python вы решили реализовать программу, которая считает числа Фибоначчи при помощи итераторов. Расчет начинается с чисел 1 и 1. Создайте функцию fib(n), генерирующую n чисел Фибоначчи с минимальными затратами ресурсов. Для реализации этой функции потребуется обратиться к инструкции yield (Она не сохраняет в оперативной памяти огромную последовательность, а дает возможность “доставать” промежуточные результаты по одному). Результатом решения задачи будет листинг кода и вывод в консоль с числом Фибоначчи от 200.

```python
def fibonacci(n):
    fib1,fib2 = 0, 1
    for __ in range(n):
        yield fib1
        fib1,fib2 = fib2,fib1 + fib2


if __name__ == '__main__':
   print(*list(fibonacci(200)))


```


### Результат.
https://github.com/ptacheev/-/blob/a396cd8c4e6dc388ca8a0beb5026bafb3559ec30/images/tema%2011/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-11-24%20200152.png
## Самостоятельная работа №2
### К коду предыдущей задачи добавьте запоминание каждого числа Фибоначчи в файл “fib.txt”, при этом каждое число должно находиться на отдельной строчке. Результатом выполнения задачи будет листинг кода и скриншот получившегося файла

```python

def fibonacci(n):
    fib1,fib2 = 0, 1
    for __ in range(n):
        yield fib1
        fib1,fib2 = fib2,fib1 + fib2


if __name__ == '__main__':
   a = list(fibonacci(200))
   f = open('uchet.txt','w')
   for i in range(len(a)):
       f.write(str(a[i]) + '\n')
   f.close()
   print(*a)



```


### Результат.
https://github.com/ptacheev/-/blob/74cffc7d0d9f896c4c49a30afad806b395d83f58/images/tema%2011/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-11-24%20200744.png
## Общие выводы по теме
- Развернутый вывод:
- Рассмотренны итераторы и генераторы сделаны лабораторные и самостоятельные работы