# Тема 6. Базовые коллекции: словари и кортежи
Отчет по Теме #6 выполнил:
- Тачеев Пётр Алексеевич
- ПИЭ-21-1

| Задание | Лаб_раб | Сам_раб |
| ------ |---------|------|
| Задание 1 | +       | +    |
| Задание 2 | +       | +    |
| Задание 3 | +       | +    |
| Задание 4 | +       | +    |
| Задание 5 | +       | +    |


знак "+" - задание выполнено; знак "-" - задание не выполнено;

Работу проверили:
- к.э.н., доцент Панов М.А.

## Лабораторная работа №1
### В школе, где вы учились, узнали, что вы крутой программист и попросили написать программу для учителей, которая будет при вводе кабинета писать для него ключ доступа и статус, занят кабинет или нет. При написании программы необходимо использовать словарь (dict), который на вход получает номер кабинета, а выводит необходимую информацию. Если кабинета, который вы ввели нет в словаре, то в консоль в виде значения ключа нужно вывести “None” и виде статуса вывести “False”. По большому счету написав данную программу мы с вами научились заменять иногда громоздкую конструкцию if/elif/else. Поскольку здесь функционал словаря полностью повторяет функционал условия, но при этом у использования словарей в более сложных программах есть намного больше возможностей реализации.

```python
request = int(input('Введите номер кабинета: '))
dictionary = {
    101:{'key': 1234, 'access': True},
    102:{'key': 1337, 'access': True},
    103:{'key': 8943, 'access': False},
    104:{'key': 5555, 'access': False},
    None: {'key': None, 'access':False},
}
response = dictionary.get(request)
if not response:
    response = dictionary[None];
key = response.get('key')
access = response.get('access')
print(key, access)
```
### Результат.
https://github.com/ptacheev/-/blob/eff0a737a67d6f51eac44b70c2dc3dde9a859704/images/tema6/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-10-15%20221530.png

## Выводы

request = int(input('Введите номер кабинета: '))
dictionary = {
    101:{'key': 1234, 'access': True},
    102:{'key': 1337, 'access': True},
    103:{'key': 8943, 'access': False},
    104:{'key': 5555, 'access': False},
    None: {'key': None, 'access':False},
}
response = dictionary.get(request)
if not response:
    response = dictionary[None];
key = response.get('key')
access = response.get('access')
print(key, access)

## Лабораторная работа №2
## Алексей решил создать самый большой словарь в мире. Для этого он придумал функцию dict_maker (**kwargs), которая принимает неограниченное количество параметров «ключ: значение» и обновляет созданный им словарь my_dict, состоящий всего из одного элемента «first» со значением «so easy». Помогите Алексею создать данную функцию.

```python
from pprint import pprint
my_dict = {'first':'so easy'}
def dict_maker(**kwargs):
    my_dict.update(**kwargs)
dict_maker(a1 = 1, a2=20, a3=54, a4= 13)
dict_maker(name='Пётр',age = 20, weigth = 95, eyes_color ='brown')
pprint(my_dict)
```
### Результат.
https://github.com/ptacheev/-/blob/eff0a737a67d6f51eac44b70c2dc3dde9a859704/images/tema6/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-10-15%20221858.png

## Выводы
from pprint import pprint
my_dict = {'first':'so easy'}
def dict_maker(**kwargs):
    my_dict.update(**kwargs)
dict_maker(a1 = 1, a2=20, a3=54, a4= 13)
dict_maker(name='Пётр',age = 20, weigth = 95, eyes_color ='brown')
pprint(my_dict)

## Лабораторная работа №3
### Для решения некоторых задач бывает необходимо разложить строку на отдельные символы. Мы знаем что это можно сделать при помощи split(), у которого более гибкая настройка для разделения для этого, но если нам нужно посимвольно разделить строку без всяких условий, то для этого мы можем использовать кортежи (tuple). Для этого напишем любую строку, которую будем делить и “обвернем” ее в tuple и дальше мы можем как нам угодно с ней работать, например, сделать ее списком (тогда получится полный аналог split()) или же работать с ним дальше, как с кортежем.

```python
input_string = 'HelloWorld'
result = tuple(input_string)
print(result)
print(list(result))

```
### Результат.

https://github.com/ptacheev/-/blob/eff0a737a67d6f51eac44b70c2dc3dde9a859704/images/tema6/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-10-15%20222018.png

## Выводы

input_string = 'HelloWorld'
result = tuple(input_string)
print(result)
print(list(result))

## Лабораторная работа №4
### Вовочка решил написать крутую функцию, которая будет писать имя, возраст и место работы, но при этом на вход этой функции будет поступать кортеж. Помогите Вовочке написать эту программу.

```python
def personal_info(name, age, company= 'unnamed'):
    print(f"Имя: {name} Возраст: {age} Компания: {company} ")
tom = ("Григорий", 22)
personal_info(*tom)
bob = ("Георгий", 41, "Yandex")
personal_info(*bob)
```
### Результат.
https://github.com/ptacheev/-/blob/eff0a737a67d6f51eac44b70c2dc3dde9a859704/images/tema6/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-10-15%20222249.png

## Выводы

def personal_info(name, age, company= 'unnamed'):
    print(f"Имя: {name} Возраст: {age} Компания: {company} ")
tom = ("Григорий", 22)
personal_info(*tom)
bob = ("Георгий", 41, "Yandex")
personal_info(*bob)
## Лабораторная работа №5
### Для сопровождения первых лиц государства X нужен кортеж, но никто не может определиться с порядком машин, поэтому вам нужно написать функцию, которая будет сортировать кортеж, состоящий из целых чисел по возрастанию, и возвращает его. Если хотя бы один элемент не является целым числом, то функция возвращает исходный кортеж.

```python
def useless(lst):
    return max(lst)/len(lst)
print(useless([3, 5, 7, 3, 33]))
print(useless([-12.5, 54, 77.3, 0, -36, 98.2, -63, 21.7, 47, -89.6]))
print(useless([-25.8, 86, 12.5, -56, 73.2, 0, 43, -91.5, 65.9, -7]))


```
### Результат.
https://github.com/ptacheev/-/blob/eff0a737a67d6f51eac44b70c2dc3dde9a859704/images/tema6/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-10-15%20222541.png


## Выводы

def useless(lst):
    return max(lst)/len(lst)
print(useless([3, 5, 7, 3, 33]))
print(useless([-12.5, 54, 77.3, 0, -36, 98.2, -63, 21.7, 47, -89.6]))
print(useless([-25.8, 86, 12.5, -56, 73.2, 0, 43, -91.5, 65.9, -7]))


## Самостоятельная работа №1
### При создании сайта у вас возникла потребность обрабатывать данные пользователя в странной форме, а потом переводить их в нужные вам форматы. Вы хотите принимать от пользователя последовательность чисел, разделенных пробелом, а после переформатировать эти данные в список и кортеж. Реализуйте вашу задумку. Для получения начальных данных используйте input(). Результатом программы будет выведенный список и кортеж из начальных данных.

```python
strt = input()
print(tuple(strt))
print(list(strt))

```
## Выводы
strt = input()
print(tuple(strt))
print(list(strt))



### Результат.
https://github.com/ptacheev/-/blob/eff0a737a67d6f51eac44b70c2dc3dde9a859704/images/tema6/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-10-15%20222909.png



## Самостоятельная работа №2
### Николай знает, что кортежи являются неизменяемыми, но он очень упрямый и всегда хочет доказать, что он прав. Студент решил создать функцию, которая будет удалять первое появление определенного элемента из кортежа по значению и возвращать кортеж без него. Попробуйте повторить шедевр не признающего авторитеты начинающего программиста. Но учтите, что Николай не всегда уверен в наличии элемента в кортеже (в этом случае кортеж вернется функцией в исходном виде)
```python
def func(tpl, elem):
    lst = list(tpl)
    c = -1
    for i in range(1,len(lst)+1):
        if lst[i-1] == elem:
            c = i-1;
            break
    if c == -1:
        return tpl
    lst.pop(c)
    tpl = tuple(lst)
    return tpl


if __name__ == '__main__':
    print(func((1,2,3),1))
    print(func((1, 2, 3, 1, 2, 3 ,4, 5, 2 , 3 , 4 , 2, 4, 2), 3))
    print(func((2, 4, 6, 6, 4, 2), 9))


```
### Результат.
https://github.com/ptacheev/-/blob/eff0a737a67d6f51eac44b70c2dc3dde9a859704/images/tema6/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-10-15%20224150.png

## Выводы
def func(tpl, elem):
    lst = list(tpl)
    c = -1
    for i in range(1,len(lst)+1):
        if lst[i-1] == elem:
            c = i-1;
            break
    if c == -1:
        return tpl
    lst.pop(c)
    tpl = tuple(lst)
    return tpl


if __name__ == '__main__':
    print(func((1,2,3),1))
    print(func((1, 2, 3, 1, 2, 3 ,4, 5, 2 , 3 , 4 , 2, 4, 2), 3))
    print(func((2, 4, 6, 6, 4, 2), 9))

## Самостоятельная работа №3
### Ребята поспорили кто из них одним нажатием на numpad наберет больше повторяющихся цифр, но не понимают, как узнать победителя. Вам им нужно в этом помочь. Дана строка в виде случайной последовательности чисел от 0 до 9 (длина строки минимум 15 символов). Требуется создать словарь, который в качестве ключей будет принимать данные числа (т. е. ключи будут типом int), а в качестве значений – количество этих чисел в имеющейся последовательности. Для построения словаря создайте функцию, принимающую строку из цифр. Функция должна возвратить словарь из 3-х самых часто встречаемых чисел, также эти значения нужно вывести в порядке возрастания ключа.

```python
from collections import Counter


def top_three_digits(num_str):
    counts = Counter(map(int, num_str))
    most_common = counts.most_common(3)
    sorted_common = sorted(most_common, key=lambda x: x[0])
    result_dict = {k: v for k, v in sorted_common}

    return result_dict



num_str = '2422525253330356362624462'
top_three = top_three_digits(num_str)
print( top_three)

```
### Результат.
https://github.com/ptacheev/-/blob/eff0a737a67d6f51eac44b70c2dc3dde9a859704/images/tema6/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-10-15%20225928.png

## Выводы
from collections import Counter


def top_three_digits(num_str):
    counts = Counter(map(int, num_str))
    most_common = counts.most_common(3)
    sorted_common = sorted(most_common, key=lambda x: x[0])
    result_dict = {k: v for k, v in sorted_common}

    return result_dict



num_str = '2422525253330356362624462'
top_three = top_three_digits(num_str)
print( top_three)

## Самостоятельная работа №4
### Ваш хороший друг владеет офисом со входом по электронным картам, ему нужно чтобы вы написали программу, которая показывала в каком порядке сотрудники входили и выходили из офиса. Определение сотрудника происходит по id. Напишите функцию, которая на вход принимает кортеж и случайный элемент (id), его можно придумать самостоятельно. Требуется вернуть новый кортеж, начинающийся с первого появления элемента в нем и заканчивающийся вторым его появлением включительно. Если элемента нет вовсе – вернуть пустой кортеж. Если элемент встречается только один раз, то вернуть кортеж, который начинается с него и идет до конца исходного.

```python
def sotr(a, id):
    if id not in a:
        return ()
    fi = a.index(id)

    if a.count(id) > 1:

        si = a.index(id, fi + 1)
        return a[fi:si + 1]
    else:
        return a[fi:]



print(sotr((1, 2, 3), 8))
print(sotr((1, 8, 3, 4, 8, 8, 9, 2), 8))
print(sotr((1, 2, 8, 5, 1, 2, 9), 8))

```
### Результат.
https://github.com/ptacheev/-/blob/eff0a737a67d6f51eac44b70c2dc3dde9a859704/images/tema6/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-10-15%20230318.png


## Выводы
def sotr(a, id):
    if id not in a:
        return ()
    fi = a.index(id)

    if a.count(id) > 1:

        si = a.index(id, fi + 1)
        return a[fi:si + 1]
    else:
        return a[fi:]



print(sotr((1, 2, 3), 8))
print(sotr((1, 8, 3, 4, 8, 8, 9, 2), 8))
print(sotr((1, 2, 8, 5, 1, 2, 9), 8))

## Самостоятельная работа №5
### Самостоятельно придумайте и решите задачу, в которой будут обязательно использоваться кортеж или список. Проведите минимум три теста для проверки работоспособности вашей задачи

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
https://github.com/ptacheev/-/blob/eff0a737a67d6f51eac44b70c2dc3dde9a859704/images/tema6/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-10-15%20230901.png

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

## Общие выводы по теме
- Развернутый вывод
- Рассмотренны Базовые коллекции: кортежи и сделаны лабораторные и самостаятельные работы