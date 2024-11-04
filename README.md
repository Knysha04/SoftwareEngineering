# Тема 9. Концепции и принципы ООП.
### Отчет по Теме #9 выполнила:
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
### Допустим, что вы решили оригинально и немного странно познакомится с человеком. Для этого у вас должен быть написан свой класс на Python, который будет проверять угадал ваше имя человек или нет. Для этого создайте класс, указав в свойствах только имя. Дальше создайте функцию init (), а в ней сделайте проверку на то угадал человек ваше имя или нет. Также можете проверить что будет, если в этой функции указав атрибут, который не указан в вашем классе, например, попробуйте вызвать фамилию.
#### Выполнение:
```python
class Ivan:
    __slots__ = ['name']
    def __init__ (self, name) :
        if name == "Иван":
            self.name = f"Да, я {name}"
        else:
            self.name = f"Я не {name}, а Иван"
pers1 = Ivan('Алексей')
pers2 = Ivan('Иван')
print (pers1. name)
print(pers2. name)
```
#### Результат:
![Меню](https://github.com/Knysha04/SoftwareEngineering/blob/main/pic/Tema9.1.png)

#### Вывод:  Создан класс `Car` с атрибутами `make` (производитель) и `model` (модель). Объект этого класса был успешно создан, что позволяет хранить информацию о конкретной машине.

## Задание №2
### Вам дали важное задание, написать продавцу мороженого программу, которая будет писать добавили ли топпинг в мороженое и цену после возможного изменения. Для этого вам нужно написать класс, в котором будет определяться изменили ли состав мороженого или нет. В этом классе реализуйте метод, выводящий на печать «Мороженое с {ТОППИНГ}» в случае наличия добавки, а иначе отобразится следующая фраза: «Обычное мороженое». При этом программа должна воспринимать как топпинг только атрибуты типа string.
#### Выполнение:
```python
class Icecream:
    def __init__(self, ingredient=None):
        if isinstance(ingredient, str):
            self. ingredient = ingredient
        else:
            self. ingredient = None
    def composition(self):
        if self. ingredient:
            print(f"Мороженное с {self.ingredient}")
        else:
            print("Обычное мороженное")
icecream = Icecream()
icecream. composition()
icecream = Icecream('шоколадом')
icecream. composition()
icecream = Icecream(5)
icecream. composition()
```
#### Результат:
![Меню](https://github.com/Knysha04/SoftwareEngineering/blob/main/pic/Tema9.2.png)

#### Вывод: Код был дополнен методом `drive`, который позволяет "заставить" машину поехать. Это демонстрирует, как можно добавлять функциональность в классы, а также использовать методы для взаимодействия с объектами.

## Задание №3
### Петя – начинающий программист и на занятиях ему сказали реализовать икапсу…что-то. А вы хороший друг Пети и ко всему прочему прекрасно знаете, что икапсу…что-то – это инкапсуляция, поэтому решаете помочь вашему другу с написанием класса с инкапсуляцией. Ваш класс будет не просто инкапсуляцией, а классом с сеттером, геттером и деструктором. После написания класса вам необходимо продемонстрировать что все написанные вами функции работают.
#### Выполнение
```python
cclass MyClass:
    def __init__(self,value):
        self. _value = value
    def set_value(self,value):
        self. _value = value
    def get_value(self):
        return self. _value
    def del_value(self):
        del self. _value
    value = property(get_value, set_value, del_value, "Свойство value")

obj = MyClass(42)
print(obj.get_value())
obj. set_value(45)
print(obj.set_value())
obj. set_value(100)
print(obj.set_value())
obj. del_valle()
print(obj.set_value())
```
#### Результат:
![Меню](https://github.com/Knysha04/SoftwareEngineering/blob/main/pic/Tema9.3.png)

#### Вывод: Создан новый класс `ElectricCar`, который наследует от класса `Car`. В этом классе добавлен метод `charge` и атрибут `battery_capacity`. Это показывает, как можно расширять функциональность базового класса и добавлять специфические для подкласса методы.

## Задание №4
### Вам прекрасно известно, что кошки и собаки являются млекопитающими, но компьютер этого не понимает, поэтому вам нужно написать три класса: Кошки, Собаки, Млекопитающие. И при помощи “наследования” объяснить компьютеру что кошки и собаки – это млекопитающие. Также добавьте какой-нибудь свой атрибут для кошек и собак, чтобы показать, что они чем-то отличаются друг от друга.
```python
class Mamal:
    className = "Mamal"
class Dog(Mamal):
    species = 'canine'
    sounds = 'meow'
class Cat(Mamal):
    species = 'feline'
    sounds = 'meow'
dog = Dog()
print(f"Dog is {dog.className}, but they say {dog.sounds}")
cat = Cat()
print(f"Cat is {cat. className}, but they say {cat. sounds}")
```
#### Результат:
![Меню](https://github.com/Knysha04/SoftwareEngineering/blob/main/pic/Tema9.4.png)

#### Вывод: Реализована инкапсуляция в классе `Car` с использованием защищенного и приватного атрибутов. Это демонстрирует, как можно скрывать данные и управлять доступом к ним, что является важным аспектом объектно-ориентированного программирования.

## Задание №5
### На разных языках здороваются по-разному, но суть остается одинаковой, люди друг с другом здороваются. Давайте вместе с вами реализуем программу с полиморфизмом, которая будет описывать всю суть первого предложения задачи. Для этого мы можем выбрать два языка, например, русский и английский и написать для них отдельные классы, в которых будет в виде атрибута слово, которым здороваются на этих языках. А также напишем функцию, которая будет выводить информацию о том, как на этих языках здороваются.
#### Выполнение:
```python
class Russian:
    @staticmethod
    def greeting():
        print("Привет")
class English:
    @staticmethod
    def greeting():
        print("Hello")
def greet(language):
    language. greeting()
ivan = Russian()
greet(ivan)
john = English()
greet(john)
```
#### Результат:
![Меню](https://github.com/Knysha04/SoftwareEngineering/blob/main/pic/Tema9.5.png)

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
