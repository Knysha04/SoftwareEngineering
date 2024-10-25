# Тема 8. Введение в объектно-ориентированное программирование
### Отчет по Теме #8 выполнила:
- Кныш Анна Анатольевна
- ПИЭ-22-1

| Задание | Лаб. раб. | Сам. раб. |
| ------ | ------ | ------ |
| Задание 1 | + | + |
| Задание 2 | + | + |
| Задание 3 | + | + |
| Задание 4 | + | + |
| Задание 5 | + | + |

Работу проверили:
- к.э.н., доцент Панов М.А.

## Лабораторная работа №1
## Задание №1
### Создайте класс “Car” с атрибутами производитель и модель. Создайте объект этого класса. Напишите комментарии для кода, объясняющие его работу. Результатом выполнения задания будет листинг кода с комментариями.
#### Выполнение:
```python
class Car:
    def __init__(self, make, model):
        self.make = make
        self.model = model

myCar = Car("Toyota", "Mazda")
```
#### Результат:
![Меню](https://github.com/Knysha04/SoftwareEngineering/blob/main/pic/Tema8.1.png)

#### Вывод:  Создан класс `Car` с атрибутами `make` (производитель) и `model` (модель). Объект этого класса был успешно создан, что позволяет хранить информацию о конкретной машине.

## Задание №2
### Дополните код из первого задания, добавив в него атрибуты и методы класса, заставьте машину “поехать”. Напишите комментарии для кода, объясняющие его работу. Результатом выполнения задания будет листинг кода с комментариями и получившийся вывод в консоль
#### Выполнение:
```python
class Car:
    def __init__(self, make, model):
        self.make = make
        self.model = model
    def drive(self):
        print(f"Driving the {self.make} {self.model}")

myCar = Car("Toyota", "Mazda")
myCar.drive()
```
#### Результат:
![Меню](https://github.com/Knysha04/SoftwareEngineering/blob/main/pic/Tema8.2.png)

#### Вывод: Код был дополнен методом `drive`, который позволяет "заставить" машину поехать. Это демонстрирует, как можно добавлять функциональность в классы, а также использовать методы для взаимодействия с объектами.

## Задание №3
### Создайте новый класс “ElectricCar” с методом “charge” и атрибутом емкость батареи. Реализуйте его наследование от класса, созданного в первом задании. Заставьте машину поехать, а потом заряжаться. Напишите комментарии для кода, объясняющие его работу. Результатом выполнения задания будет листинг кода с комментариями и получившийся вывод в консоль.
#### Выполнение
```python
class Car:
    def __init__(self, make, model):
        self.make = make
        self.model = model

    def drive(self):
        print(f"Driving the {self.make} {self.model}")

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
#### Результат:
![Меню](https://github.com/Knysha04/SoftwareEngineering/blob/main/pic/Tema8.3.png)

#### Вывод: Создан новый класс `ElectricCar`, который наследует от класса `Car`. В этом классе добавлен метод `charge` и атрибут `battery_capacity`. Это показывает, как можно расширять функциональность базового класса и добавлять специфические для подкласса методы.

## Задание №4
### Реализуйте инкапсуляцию для класса, созданного в первом задании. Создайте защищенный атрибут производителя и приватный атрибут модели. Вызовите защищенный атрибут и заставьте машину поехать. Напишите комментарии для кода, объясняющие его работу. Результатом выполнения задания будет листинг кода с комментариями и получившийся вывод в консоль.
#### Выполнение:
```python
class Car:
    def __init__(self, make, model):
        self.make = make
        self.model = model

    def drive(self):
        print(f"Driving the {self.make} {self.model}")

myCar = Car("Toyota", "Corolla")
print(myCar.make)
myCar.drive()
```
#### Результат:
![Меню](https://github.com/Knysha04/SoftwareEngineering/blob/main/pic/Tema8.4.png)

#### Вывод: Реализована инкапсуляция в классе `Car` с использованием защищенного и приватного атрибутов. Это демонстрирует, как можно скрывать данные и управлять доступом к ним, что является важным аспектом объектно-ориентированного программирования.

## Задание №5
### Реализуйте полиморфизм создав основной (общий) класс “Shape”, а также еще два класса “Rectangle” и “Circle”. Внутри последних двух классов реализуйте методы для подсчета площади фигуры. После этого создайте массив с фигурами, поместите туда круг и прямоугольник, затем при помощи цикла выведите их площади. Напишите комментарии для кода, объясняющие его работу. Результатом выполнения задания будет листинг кода с комментариями и получившийся вывод в консоль
#### Выполнение:
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

myRectangle = Rectangle(20, 30)

result1 = myRectangle.area()

myCircle = Circle(20)
result2 = myCircle.area()

print(result1)
print(result2)
```
#### Результат:
![Меню](https://github.com/Knysha04/SoftwareEngineering/blob/main/pic/Tema8.5.png)

#### Вывод: Создан общий класс `Shape` и два его подкласса `Rectangle` и `Circle`, каждый из которых реализует метод для подсчета площади. Это демонстрирует полиморфизм, позволяя использовать один и тот же интерфейс для различных типов объектов, что упрощает работу с ними и делает код более гибким.

## Самостоятельная работа №1
## Задание №1
### Самостоятельно создайте класс и его объект. Они должны отличаться, от тех, что указаны в теоретическом материале (методичке) и лабораторных заданиях. Результатом выполнения задания будет листинг кода и получившийся вывод консоли.
#### Выполнение:
```python
class Book:
    def __init__(self, title, author):
        self.title = title
        self.author = author
```
#### Результат:
![Меню](https://github.com/Knysha04/SoftwareEngineering/blob/main/pic/Tema8.6.png)

#### Вывод: класс, представляющий книгу, и объект этого класса.

## Задание №2
### Самостоятельно создайте атрибуты и методы для ранее созданного класса. Они должны отличаться, от тех, что указаны в теоретическом материале (методичке) и лабораторных заданиях. Результатом выполнения задания будет листинг кода и получившийся вывод консоли.
#### Выполнение:
```python
class Book:
    def __init__(self, title, author):
        self.title = title
        self.author = author

    def info(self):
        print(f"Book Title: {self.title}")
        print(f"Author: {self.author}")

my_book = Book("Anna Carenina", "Tolstoi")

my_book.info()
```
#### Результат:
![Меню](https://github.com/Knysha04/SoftwareEngineering/blob/main/pic/Tema8.7.png)

### Вывод:класс, представляющий книгу, и объект этого класса. В этом примере книга будет иметь атрибуты title (название) и author (автор), а также метод display_info(), который выводит информацию о книге.

## Задание №3
### Самостоятельно реализуйте наследование, продолжая работать с ранее созданным классом. Оно должно отличаться, от того, что указано в теоретическом материале (методичке) и лабораторных заданиях. Результатом выполнения задания будет листинг кода и получившийся вывод консоли
#### Выполнение:
```python
class Book:
    def __init__(self, title, author):
        self.title = title
        self.author = author

    def info(self):
        print(f"Book Title: {self.title}")
        print(f"Author: {self.author}")

my_book = Book("Anna Carenina", "Tolstoi")



class EBook(Book):
    def __init__(self, title, author, format):
        super().__init__(title, author)
        self.format = format

    def info(self):
        super().info()
        print(f"Format: {self.format}")

my_ebook = EBook("Anna Carenina", "Tolstoi", "PDF")

my_ebook.info()
```
#### Результат:
![Меню](https://github.com/Knysha04/SoftwareEngineering/blob/main/pic/Tema8.8.png)

### Вывод: Использовано наследование для создания нового класса EBook, который расширяет функциональность базового класса Book и добавляет новый атрибут format. Метод info в EBook был переопределен для учета нового атрибута и одновременно использования функциональности родительского класса.

## Задание №4
### Самостоятельно реализуйте инкапсуляцию, продолжая работать с ранее созданным классом. Она должна отличаться, от того, что указана в теоретическом материале (методичке) и лабораторных заданиях. Результатом выполнения задания будет листинг кода и получившийся вывод консоли.
#### Выполнение:
```python
class Book:
    def __init__(self, title, author):
        self._title = title
        self._author = author

    def get_title(self):
        return self._title

    def set_title(self, title):
        self._title = title

    def get_author(self):
        return self._author

    def set_author(self, author):
        self._author = author

    def info(self):
        print(f"Book Title: {self._title}")
        print(f"Author: {self._author}")

class EBook(Book):
    def __init__(self, title, author, format):
        super().__init__(title, author)
        self._format = format

    def get_format(self):
        return self._format

    def set_format(self, format):
        self._format = format

    def info(self):
        super().info()
        print(f"Format: {self.get_format()}")

my_ebook = EBook("Anna Carenina", "Tolstoi", "PDF")

my_ebook.set_title("New Title")

my_ebook.info()
```
#### Результат:
![Меню](https://github.com/Knysha04/SoftwareEngineering/blob/main/pic/Tema8.9.png)

#### Вывод: Атрибуты title, author и format закрытыми (приватными) и предоставим методы для получения и установки этих значений. Таким образом, мы скрываем прямой доступ к атрибутам и обеспечиваем контролируемый доступ к данным.

## Задание №5
### Самостоятельно реализуйте полиморфизм. Он должен отличаться, от того, что указан в теоретическом материале (методичке) и лабораторных заданиях. Результатом выполнения задания будет листинг кода и получившийся вывод консоли.
#### Выполнение:
```python
class Book:
    def __init__(self, title, author):
        self._title = title
        self._author = author

    def get_title(self):
        return self._title

    def set_title(self, title):
        self._title = title

    def get_author(self):
        return self._author

    def set_author(self, author):
        self._author = author

    def info(self):
        print(f"Book Title: {self._title}")
        print(f"Author: {self._author}")

    def read(self):
        print("Reading a physical book.")

class EBook(Book):
    def __init__(self, title, author, format):
        super().__init__(title, author)
        self._format = format

    def get_format(self):
        return self._format

    def set_format(self, format):
        self._format = format

    def info(self):
        super().info()
        print(f"Format: {self.get_format()}")

    def read(self):
        print("Reading an ebook.")

my_book = Book("Anna Carenina", "Tolstoi")
my_ebook = EBook("Padenie", "Kamu", "PDF")

my_book.read()
my_ebook.read()
```
#### Результат:
![Меню](https://github.com/Knysha04/SoftwareEngineering/blob/main/pic/Tema8.10.png)

#### Вывод: Использованн полиморфизм, где метод read представляет общий интерфейс для чтения книг, но каждый подкласс (Book и EBook) предоставляет свою уникальную реализацию этого метода.
## Общий вывод: Объектно-ориентированное программирование (ООП) в Python, как и в других языках, предлагает множество преимуществ и инструментов, которые делают процесс разработки программ более удобным и эффективным.
