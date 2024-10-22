# Тема 7. Работа с файлами ввод, вывод
Отчет по Теме #7 выполнил:
- Тачеев Пётр Алексеевич
- ПИЭ-21-1

| Задание    | Лаб_раб | Сам_раб |
|------------|---------|---|
| Задание 1  | +       | + |
| Задание 2  | +       | + |
| Задание 3  | +       | + |
| Задание 4  | +       | + |
| Задание 5  | +       | + |
| Задание 6  | +       |  |
| Задание 7  | +       |  |
| Задание 8  | +       |  |
| Задание 9  | +       |  |
| Задание 10 | +       |   |


знак "+" - задание выполнено; знак "-" - задание не выполнено;

Работу проверили:
- к.э.н., доцент Панов М.А.

## Лабораторная работа №1
### Составьте текстовый файл и положите его в одну директорию с программой на Python. Текстовый файл должен состоять минимум из двух строк

### Результат.
https://github.com/ptacheev/-/blob/1cfd360110f602e9a602c30171570662344c46f0/images/tema7/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-10-22%20203258.png

## Лабораторная работа №2
## Напишите программу, которая выведет только первую строку из вашего файла, при этом используйте конструкцию open()/close().
```python
f = open('input.txt', 'r')
print(f.readline())
f.close()
```
### Результат.
https://github.com/ptacheev/-/blob/1cfd360110f602e9a602c30171570662344c46f0/images/tema7/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-10-22%20203603.png

## Выводы
f = open('input.txt', 'r')
print(f.readline())
f.close()

## Лабораторная работа №3
### Напишите программу, которая выведет все строки из вашего файла в  массиве, при этом используйте конструкцию open()/close(). 

```python
f = open('input.txt', 'r')
print(f.readlines())
f.close()

```
### Результат.

https://github.com/ptacheev/-/blob/1cfd360110f602e9a602c30171570662344c46f0/images/tema7/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-10-22%20203641.png  

## Выводы

f = open('input.txt', 'r')
print(f.readlines())
f.close()
## Лабораторная работа №4
### Напишите программу, которая выведет все строки из вашего файла в массиве, при этом используйте конструкцию with open().

```python
with open('input.txt') as f:
    print(f.readlines())
```
### Результат.
https://github.com/ptacheev/-/blob/1cfd360110f602e9a602c30171570662344c46f0/images/tema7/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-10-22%20203800.png

## Выводы

with open('input.txt') as f:
    print(f.readlines())
## Лабораторная работа №5
### Напишите программу, которая выведет каждую строку из вашего файла отдельно, при этом используйте конструкцию with open().
```python
with open('input.txt') as f:
    for line in f:
        print(line)

```
### Результат.
https://github.com/ptacheev/-/blob/1cfd360110f602e9a602c30171570662344c46f0/images/tema7/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-10-22%20203905.png

## Выводы

with open('input.txt') as f:
    for line in f:
        print(line)
## Лабораторная работа №6
### Напишите программу, которая будет добавлять новую строку в ваш файл, а потом выведет полученный файл в консоль. Вывод можно осуществлять любым способом. Обязательно проверьте сам файл, чтобы изменения в нем тоже отображались.

```python
with open('input.txt', 'a+') as f:
    f.write('\nIm addtirional line')
with open('input.txt', 'r') as f:
    result = f.readlines()
    print(result)


```
### Результат.
https://github.com/ptacheev/-/blob/1cfd360110f602e9a602c30171570662344c46f0/images/tema7/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-10-22%20204203.png

## Выводы

with open('input.txt', 'a+') as f:
    f.write('\nIm addtirional line')
with open('input.txt', 'r') as f:
    result = f.readlines()
    print(result)

## Лабораторная работа №7
### Напишите программу, которая перепишет всю информацию, которая была у вас в файле до этого, например напишет любые данные из произвольно вами составленного списка. Также не забудьте проверить что измененная вами информация сохранилась в файле.
```python
lines = ['one', 'two', 'three']
with open('input.txt', 'w') as f:
    for line in lines:
        f.write('\nCycle run' + line)
print('done!')


```
### Результат.
https://github.com/ptacheev/-/blob/1cfd360110f602e9a602c30171570662344c46f0/images/tema7/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-10-22%20204441.png

## Выводы
lines = ['one', 'two', 'three']
with open('input.txt', 'w') as f:
    for line in lines:
        f.write('\nCycle run' + line)
print('done!')

## Лабораторная работа №8
### Выберите любую папку на своем компьютере, имеющую вложенные директории. Выведите на печать в терминал ее содержимое, как и всехподкаталогов при помощи функции print_docs(directory).

```python 
import os

def print_docs(directory):
    all_files = os.walk(directory)
    for catalog in all_files:
        print(f'Папка {catalog[0]} содержит')
    print(f'Директории: {", ".join([folder for folder in catalog[1]])}')
    print(f'Файлы: {", ".join([file for file in catalog[2]])}')
    print('-' * 40)

print_docs('C:/')

```
### Результат.
https://github.com/ptacheev/-/blob/1cfd360110f602e9a602c30171570662344c46f0/images/tema7/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-10-22%20205527.png

## Выводы

import os

def print_docs(directory):
    all_files = os.walk(directory)
    for catalog in all_files:
        print(f'Папка {catalog[0]} содержит')
    print(f'Директории: {", ".join([folder for folder in catalog[1]])}')
    print(f'Файлы: {", ".join([file for file in catalog[2]])}')
    print('-' * 40)

print_docs('C:/')

## Лабораторная работа №9
### Документ «input.txt» содержит следующий текст: Приветствие Спасибо Извините Пожалуйста До свидания Ты готов? Как дела? С днем рождения! Удача! Я тебя люблю. Требуется реализовать функцию, которая выводит слово, имеющее максимальную длину (или список слов, если таковых несколько). Проверьте работоспособность программы на своем наборе данных

```python
def longest_words(file):
    with open(file,encoding= 'utf - 8') as f:
        words = f.read().split()
        max_length = len(max(words, key = len))
        for word in words:
            if len(word) == max_length:
                sought_words = word
        if len(sought_words) == 1:
            return sought_words[0]
        return sought_words
print(longest_words('input.txt'))

```
### Результат.
https://github.com/ptacheev/-/blob/1cfd360110f602e9a602c30171570662344c46f0/images/tema7/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-10-22%20205929.png


## Выводы
def longest_words(file):
    with open(file,encoding= 'utf - 8') as f:
        words = f.read().split()
        max_length = len(max(words, key = len))
        for word in words:
            if len(word) == max_length:
                sought_words = word
        if len(sought_words) == 1:
            return sought_words[0]
        return sought_words
print(longest_words('input.txt'))

## Лабораторная работа №10
### Требуется создать csv-файл «rows_300.csv» со следующими столбцами: • № - номер по порядку (от 1 до 300); • Секунда – текущая секунда на вашем ПК; • Микросекунда – текущая миллисекунда на часах. Для наглядности на каждой итерации цикла искусственно приостанавливайте скрипт на 0,01 секунды.
```python
import csv
import datetime
import time
with open('rows_300.csv','w', encoding = 'utf - 8', newline = '') as f:
    writer = csv.writer(f)
    writer.writerow(['№', 'Секунда', 'Микросекунда'])
    for line in range(1, 301):
        writer.writerow([line, datetime.datetime.now().second, datetime.datetime.now().microsecond])
        time.sleep(0.01)



```
### Результат.
https://github.com/ptacheev/-/blob/1cfd360110f602e9a602c30171570662344c46f0/images/tema7/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-10-22%20210532.png

## Выводы

import csv
import datetime
import time
with open('rows_300.csv','w', encoding = 'utf - 8', newline = '') as f:
    writer = csv.writer(f)
    writer.writerow(['№', 'Секунда', 'Микросекунда'])
    for line in range(1, 301):
        writer.writerow([line, datetime.datetime.now().second, datetime.datetime.now().microsecond])
        time.sleep(0.01)



## Самостоятельная работа №1
### Найдите в интернете любую статью (объем статьи не менее 200 слов), скопируйте ее содержимое в файл и напишите программу, которая считает количество слов в текстовом файле и определит самое часто встречающееся слово. Результатом выполнения задачи будет: скриншот файла со статьей, листинг кода, и вывод в консоль, в котором будет указана вся необходимая информация

```python
with open('input.txt','r', encoding = 'utf - 8') as f:
    words = f.read().split()
    clr_words =[]
    index = ['!', ',', '.', '(', ')', ';', ':', '?', '1', '2', '3', '4', '5', '6', '7', '8', '9', '0']
    for i in range(len(words)):
        if i not in index:
            clr_words.append(words[i])
    print(len(clr_words))
    mx = -1;
    for i in clr_words:
        if clr_words.count(i) > mx:
            mx = clr_words.index(i)

    print(clr_words[mx])

```
## Выводы
with open('input.txt','r', encoding = 'utf - 8') as f:
    words = f.read().split()
    clr_words =[]
    index = ['!', ',', '.', '(', ')', ';', ':', '?', '1', '2', '3', '4', '5', '6', '7', '8', '9', '0']
    for i in range(len(words)):
        if i not in index:
            clr_words.append(words[i])
    print(len(clr_words))
    mx = -1;
    for i in clr_words:
        if clr_words.count(i) > mx:
            mx = clr_words.index(i)

    print(clr_words[mx])



### Результат.
https://github.com/ptacheev/-/blob/1cfd360110f602e9a602c30171570662344c46f0/images/tema7/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-10-22%20210532.png
https://github.com/ptacheev/-/blob/1cfd360110f602e9a602c30171570662344c46f0/images/tema7/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-10-22%20211812.png


## Самостоятельная работа №2
###  У вас появилась потребность в ведении книги расходов, посмотрев все существующие варианты вы пришли к выводу что вас ничего не устраивает и нужно все делать самому. Напишите программу для учета расходов. Программа должна позволять вводить информацию о расходах, сохранять ее в файл и выводить существующие данные в консоль. Ввод информации происходит через консоль. Результатом выполнения задачи будет: скриншот файла с учетом расходов, листинг кода, и вывод в консоль, с демонстрацией работоспособности программы.

```python

with open('uchet.txt','w', encoding = 'utf - 8') as f:
    n = int (input('Введите  кол-во записей '))
    x =[]
    for i in range(1, n+1):
        x. append(input(f'Расход № {i} ')+'\n')
    f.writelines(x)
    f.close()


```
### Результат.
https://github.com/ptacheev/-/blob/1cfd360110f602e9a602c30171570662344c46f0/images/tema7/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-10-22%20213524.png
https://github.com/ptacheev/-/blob/1cfd360110f602e9a602c30171570662344c46f0/images/tema7/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-10-22%20213530.png
## Выводы

with open('uchet.txt','w', encoding = 'utf - 8') as f:
    n = int (input('Введите  кол-во записей '))
    x =[]
    for i in range(1, n+1):
        x. append(input(f'Расход № {i} ')+'\n')
    f.writelines(x)
    f.close()

## Самостоятельная работа №3
###  Имеется файл input.txt с текстом на латинице. Напишите программу, которая выводит следующую статистику по тексту: количество букв латинского алфавита; число слов; число строк. • Текст в файле: Beautiful is better than ugly. Explicit is better than implicit. Simple is better than complex. Complex is better than complicated. • Ожидаемый результат: Input file contains: 108 letters 20 words 4 lines

```python
f = open('input.txt', 'r')
arr = []
wrds = ''
while True:
    line = f.readline()
    if not line:
        break
    arr.append(line)
lines = len(arr)
for i in range(len(arr)):
    wrds += arr[i][:-2]+' ';
arr2 = wrds.split()
words = len(arr2)
sum = 0
for i in arr2:
    sum += len(i)
print(arr2)
print(f'Input file contains: \n {sum+1} letters \n {words} words \n {lines} lines')
f.close()


```
### Результат.
https://github.com/ptacheev/-/blob/1cfd360110f602e9a602c30171570662344c46f0/images/tema7/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-10-22%20213530.png

## Выводы
f = open('input.txt', 'r')
arr = []
wrds = ''
while True:
    line = f.readline()
    if not line:
        break
    arr.append(line)
lines = len(arr)
for i in range(len(arr)):
    wrds += arr[i][:-2]+' ';
arr2 = wrds.split()
words = len(arr2)
sum = 0
for i in arr2:
    sum += len(i)
print(arr2)
print(f'Input file contains: \n {sum+1} letters \n {words} words \n {lines} lines')
f.close()


## Самостоятельная работа №4
### Напишите программу, которая получает на вход предложение, выводит его в терминал, заменяя все запрещенные слова звездочками * (количество звездочек равно количеству букв в слове). Запрещенные слова, разделенные символом пробела, хранятся в текстовом файле input.txt. Все слова в этом файле записаны в нижнем регистре. Программа должна заменить запрещенные слова, где бы они ни встречались, даже в середине другого слова. Замена производится независимо от регистра: если


```python

sent = 'Hello, world! Python IS the programming language of thE future. My EMAIL is.... PYTHON is awesome!!!!'
with open('input.txt','r', encoding = 'utf - 8') as f:
    ban = f.read().split()
    clr_words = ''
    index = ['!', ',', '.', '(', ')', ';', ':', '?', '1', '2', '3', '4', '5', '6', '7', '8', '9', '0']
    for i in range(len(sent)):
        if sent[i] not in index:
            clr_words += sent[i]
    arr = clr_words.split()
    for i in range(len(arr)):
        for j in range(len(ban)):
            if  ban[j] in arr[i].casefold():
                arr[i] = '*'*len(arr[i])

    print(*arr)

    f.close()

```
### Результат.
https://github.com/ptacheev/-/blob/1cfd360110f602e9a602c30171570662344c46f0/images/tema7/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-10-22%20223453.png

## Выводы

sent = 'Hello, world! Python IS the programming language of thE future. My EMAIL is.... PYTHON is awesome!!!!'
with open('input.txt','r', encoding = 'utf - 8') as f:
    ban = f.read().split()
    clr_words = ''
    index = ['!', ',', '.', '(', ')', ';', ':', '?', '1', '2', '3', '4', '5', '6', '7', '8', '9', '0']
    for i in range(len(sent)):
        if sent[i] not in index:
            clr_words += sent[i]
    arr = clr_words.split()
    for i in range(len(arr)):
        for j in range(len(ban)):
            if  ban[j] in arr[i].casefold():
                arr[i] = '*'*len(arr[i])

    print(*arr)

    f.close()

## Самостоятельная работа №5
### Самостоятельно придумайте и решите задачу, которая будет заимодействовать с текстовым файлом: считать из файла числа и записать в него эти числа буквами

```python
def zadach(name, weekd, days):
    print(f"Месяц {name}, в нем {weekd} недели и {days} дней")
semt = ('Сентябрь', 4, 31)
zadach(*semt)
oct = ('Октябрь', 4, 31)
zadach(*oct)
nov = ('Ноябрь', 4, 30)
zadach(*nov)
```
### Результат.
https://github.com/ptacheev/-/blob/1cfd360110f602e9a602c30171570662344c46f0/images/tema7/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-10-22%20224809.png

```python
from num2words import num2words
with open('input.txt','r', encoding = 'utf - 8') as f:
    nums = f.read().split('\n')
    print(*nums)
    f.close()
with open('input.txt','w', encoding = 'utf - 8') as f:
    for i in nums:
        f.write(num2words(int(i),lang = 'ru') + '\n')
```

## Общие выводы по теме
- Развернутый вывод
- Рассмотренны файлы ввод и вывод и сделаны лабораторные и самостаятельные работы