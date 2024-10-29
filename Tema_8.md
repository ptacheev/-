# Тема 8. Концепции и принципы ООП
Отчет по Теме #8 выполнил:
- Тачеев Пётр Алексеевич
- ПИЭ-21-1

| Задание    | Лаб_раб | Сам_раб |
|------------|---------|---|
| Задание 1  | +       | + |
| Задание 2  | +       | + |
| Задание 3  | +       | + |
| Задание 4  | +       | + |
| Задание 5  | +       | + |



знак "+" - задание выполнено; знак "-" - задание не выполнено;

Работу проверили:
- к.э.н., доцент Панов М.А.

## Лабораторная работа №1
### Создайте класс “Car” с атрибутами производитель и модель. Создайте объект этого класса. Напишите комментарии для кода, объясняющие его работу. Результатом выполнения задания будет листинг кода с комментариями.
```python
class Car:
    def __init__(self, make, model):
        self.make = make
        self.model = model

my_car = Car("Toyota", "Corolla")
```
### Результат.
https://github.com/ptacheev/-/blob/8447203b6edd7b49a8b2e1601ccb54d888dfdf97/images/tema%208/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-10-29%20224404.png

## Лабораторная работа №2
## Дополните код из первого задания, добавив в него атрибуты и методы класса, заставьте машину “поехать”. Напишите комментарии для кода, объясняющие его работу. Результатом выполнения задания будет листинг кода с комментариями и получившийся вывод в консоль.
```python
class Car:
    def __init__(self, make, model):
        self.make = make
        self.model = model

    def drive(self):
        print(f"Driving the {self.make} {self.model}")

my_car = Car("Toyota", "Corolla")
my_car.drive()
```
### Результат.
https://github.com/ptacheev/-/blob/8447203b6edd7b49a8b2e1601ccb54d888dfdf97/images/tema%208/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-10-29%20224417.png

## Лабораторная работа №3
### Создайте новый класс “ElectricCar” с методом “charge” и атрибутом емкость батареи. Реализуйте его наследование от класса, созданного в первом задании. Заставьте машину поехать, а потом заряжаться. Результатом выполнения задания будет листинг кода с комментариями и получившийся вывод в консоль. 

```python
class Car:
    def __init__(self, make, model):
        self.make = make
        self.model = model

    def drive(self):
        print(f"Driving the {self.make} {self.model}")
my_car = Car("Toyota", "Corolla")
my_car.drive()
class ElectricCar(Car):
    def __init__(self, make, model, battery_capacity):
        super().__init__(make, model)
        self.battery_capacity = battery_capacity

    def charge(self):
        print(f"Charging the {self.make} {self.model} with {self.battery_capacity} kWh")

my_electric_car = ElectricCar("Tesla", "Model S", 75)
my_electric_car.drive()
my_electric_car.charge()

```
### Результат.
https://github.com/ptacheev/-/blob/8447203b6edd7b49a8b2e1601ccb54d888dfdf97/images/tema%208/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-10-29%20224427.png

## Лабораторная работа №4
### Реализуйте инкапсуляцию для класса, созданного в первом задании. Создайте защищенный атрибут производителя и приватный атрибут модели. Вызовите защищенный атрибут и заставьте машину поехать. Напишите комментарии для кода, объясняющие его работу. Результатом выполнения задания будет листинг кода с комментариями и получившийся вывод в консоль.

```python
class Car:
    def __init__(self, make, model):
        self._make = make
        self.__model = model

    def drive(self):
        print(f"Driving the {self._make} {self.__model}")

my_car = Car("Toyota", "Corolla")

print(my_car._make)
my_car.drive()
```
### Результат.
https://github.com/ptacheev/-/blob/8447203b6edd7b49a8b2e1601ccb54d888dfdf97/images/tema%208/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-10-29%20224440.png

## Лабораторная работа №5
### Реализуйте полиморфизм создав основной (общий) класс “Shape”, а также еще два класса “Rectangle” и “Circle”. Внутри последних двух классов реализуйте методы для подсчета площади фигуры. После этого создайте массив с фигурами, поместите туда круг и прямоугольник, затем при помощи цикла выведите их площади. Напишите комментарии для кода, объясняющие его работу. Результатом выполнения задания будет листинг кода с комментариями и получившийся вывод в консоль.

```python
class Shape:
    def area(self):
        pass

class Rectangle(Shape):
    def __init__(self, width, height):
        self.width = width
        self.height = height

    def area(self):
        return self.width * self.height

class Circle(Shape):
    def __init__(self, radius):
        self.radius = radius

    def area(self):
        return 3.14 * self.radius * self.radius

my_rectangle = Rectangle(3, 4)
my_circle = Circle(3)

print(my_rectangle.area())
print(my_circle.area())

```
### Результат.
https://github.com/ptacheev/-/blob/8447203b6edd7b49a8b2e1601ccb54d888dfdf97/images/tema%208/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-10-29%20224452.png

## Самостоятельная работа №1
### Самостоятельно создайте класс и его объект. Они должны отличаться, от тех, что указаны в теоретическом материале (методичке) и лабораторных заданиях. Результатом выполнения задания будет листинг кода и получившийся вывод консоли.

```python
class Hp:
    def __init__(self, dmg):
        self.dmg = dmg

    def Damage(self):
        return self.dmg

hp = Hp(500)
print(hp.Damage())

```



### Результат.
https://github.com/ptacheev/-/blob/8447203b6edd7b49a8b2e1601ccb54d888dfdf97/images/tema%208/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-10-29%20222956.png

## Самостоятельная работа №2
### Самостоятельно создайте атрибуты и методы для ранее созданного класса. Они должны отличаться, от тех, что указаны в теоретическом материале (методичке) и лабораторных заданиях. Результатом выполнения задания будет листинг кода и получившийся вывод консоли 

```python

class Hp:
    def __init__(self, dmg, nd):
        self.dmg = dmg
        self.nd = nd

    def Damage(self):
        return self.dmg

    def Nd(self):
        return self.nd

hp = Hp(100, "Need healing")
print(hp.Damage())
print(hp.Nd())

```
### Результат.
https://github.com/ptacheev/-/blob/8447203b6edd7b49a8b2e1601ccb54d888dfdf97/images/tema%208/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-10-29%20223232.png


## Самостоятельная работа №3
### Самостоятельно реализуйте наследование, продолжая работать с ранее созданным классом. Оно должно отличаться, от того, что указано в теоретическом материале (методичке) и лабораторных заданиях. Результатом выполнения задания будет листинг кода и получившийся вывод консоли.
    
```python
class Hp:
    def __init__(self, dmg):
        self.dmg = dmg
        self.nd = "Need healing"

    def Damage(self):
        return self.dmg

    def Nd(self):
        return self.nd
class Tanky(Hp):
    def __init__(self, dmg):
        super().__init__(dmg)
        self.nd = "Im fine"
hp = Hp(100, )
tanky = Tanky(1000)
print(tanky.Nd())
print(hp.Nd())


```
### Результат.
https://github.com/ptacheev/-/blob/8447203b6edd7b49a8b2e1601ccb54d888dfdf97/images/tema%208/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-10-29%20223621.png


## Самостоятельная работа №4
### 

```python
class Hp:
    def __init__(self, dmg):
        self.dmg = dmg
        self.nd = "Need healing"

    def Damage(self):
        return self.dmg

    def Nd(self):
        return self.nd

    def set_damage(self, new_dmg):
        if new_dmg >= 50:
            self.__dmg = new_dmg
        else:
            print("Not enough!")
class Tanky(Hp):
    def __init__(self, dmg):
        super().__init__(dmg)
        self.nd = "Im fine"
hp = Hp(100, )
tanky = Tanky(1000)
print(tanky.Nd())
print(hp.Nd())
hp.set_damage(1)
print(hp.Damage())
hp.set_damage(442)
print(hp.Damage())

```
### Результат.
https://github.com/ptacheev/-/blob/8447203b6edd7b49a8b2e1601ccb54d888dfdf97/images/tema%208/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-10-29%20223914.png

## Самостоятельная работа №5
### Самостоятельно реализуйте инкапсуляцию, продолжая работать с ранее созданным классом. Она должна отличаться, от того, что указана в теоретическом материале (методичке) и лабораторных заданиях. Результатом выполнения задания будет листинг кода и получившийся вывод консоли

```python
class Hp:
    def __init__(self, dmg):
        self.dmg = dmg

    def Damage(self):
        return self.dmg

    def Nd(self):
        return "Need healing"

    def set_damage(self, new_dmg):
        if new_dmg >= 50:
            self.__dmg = new_dmg
        else:
            print("Not enough!")
class Tanky(Hp):
    def __init__(self, dmg):
        super().__init__(dmg)
    def Nd(self):
        return "Im fine"
class squishy(Hp):
    def __init__(self, dmg):
        super().__init__(dmg)
    def Nd(self):
        return "So painful.."

hpbars = [Hp(100),Tanky(1000), squishy(10)]

for hps in hpbars:
    print(hps.Nd())
```
### Результат.
https://github.com/ptacheev/-/blob/8447203b6edd7b49a8b2e1601ccb54d888dfdf97/images/tema%208/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-10-29%20224301.png

## Общие выводы по теме
- Развернутый вывод
- Рассмотренны введение в ООП лабораторные и самостаятельные работы