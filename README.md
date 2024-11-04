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

#### Вывод:  Создан класс Ivan, который принимает имя и проверяет его на совпадение с заданным именем "Иван". В результате, если имя совпадает, программа сообщает, что это искомое имя, в противном случае — выдает, что это не то имя. Это демонстрирует базовые возможности работы с классами и инициализацией атрибутов.

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

#### Вывод: Реализован класс Icecream, который управляет состоянием добавления топпинга в мороженое. Программа корректно обрабатывает входные данные, проверяя, является ли добавка строкой, а также демонстрирует использование методов для вывода состояния объекта. Это иллюстрирует работу с методами и условными проверками в классах.

## Задание №3
### Петя – начинающий программист и на занятиях ему сказали реализовать икапсу…что-то. А вы хороший друг Пети и ко всему прочему прекрасно знаете, что икапсу…что-то – это инкапсуляция, поэтому решаете помочь вашему другу с написанием класса с инкапсуляцией. Ваш класс будет не просто инкапсуляцией, а классом с сеттером, геттером и деструктором. После написания класса вам необходимо продемонстрировать что все написанные вами функции работают.
#### Выполнение
```python
class MyClass:
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

#### Вывод: Создан класс MyClass, демонстрирующий инкапсуляцию с использованием приватных атрибутов и соответствующих методов-сеттеров и геттеров. Деструктор реализован через метод del_value, удаляющий атрибут. Работает на примере манипуляции атрибутом, показывая, как можно безопасно управлять внутренним состоянием объекта.

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

#### Вывод: Разработаны классы Mamal, Dog и Cat, демонстрирующие наследование. Классы собак и кошек наследуют от класса млекопитающих, что демонстрирует иерархию классов. Каждый из подчиненных классов имеет свои уникальные атрибуты, иллюстрируя полиморфизм и различия между разными типами объектов, созданных на основе одного родительского класса.

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

#### Вывод: В этом задании реализован полиморфизм через создание классов Russian и English, каждый из которых имеет статический метод greeting, возвращающий приветствие на соответствующем языке. Функция greet принимает объект языка и вызывает его метод greeting, демонстрируя, как один и тот же интерфейс может использоваться для различных реализаций. Это подчеркивает принцип полиморфизма, позволяя легко добавлять новые языки с аналогичной функциональностью.

## Самостоятельная работа №1
## Задание №1
### Вызовите справку по садоводству
Классовая структура:
Есть Помидор со следующими характеристиками:
• Индекс 
• Стадия созревания (стадии: отсутствует, цветение, зеленый, красный)
Помидор может:
• Расти (переходить на следующую стадию созревания) 
• Предоставлять информацию о своей зрелости
Есть Куст с помидорами, который:
• Содержит список томатов, которые на нем растут 
А также может:
• Расти вместе с томатами 
• Предоставлять информацию о зрелости всех томатов 
• Предоставлять урожай
И также есть Садовник, который имеет:
• Имя 
• Растение, за которым он ухаживает
Он может:
• Ухаживать за растением
• Собирать с него урожай

Класс Tomato:
1. Создайте класс Tomato
2. Создайте статическое свойство states, которое будет содержать все стадии созревания помидора
3. Создайте метод init(), внутри которого будут определены два динамических свойства: _index (передается параметром) и _state
#### Выполнение:
```python
class Tomato:
    def __init__(self, index):
        self. index = index
        self. ripeness = "отсутствует"
    def grow(self):
        if self. ripeness == "отсутствует":
            self. ripeness = "цветение"
        elif self. ripeness == "цветение":
            self. ripeness = "зеленый"
        elif self. ripeness == "зеленый":
            self. ripeness = "красный"
def is_ripe(self):
    return self. ripeness == "красный"
```
![Меню](https://github.com/Knysha04/SoftwareEngineering/blob/main/pic/Tema9.6.png)

Класс TomatoBush:
1. Создайте класс TomatoBush
2. Определите метод init(), который будет принимать в качестве параметра количество томатов и на его основе будет создавать список объектов класса Tomato. Данный список будет храниться внутри динамического свойства tomatoes
3. Создайте метод grow_all(), который будет переводить все объекты из списка томатов на следующий этап созревания
4. Создайте метод all_are_ripe(), который будет возвращать True, если все томаты из списка стали спелыми.
5. Создайте метод give_away_all(), который будет чистить список томатов после сбора урожая Класс Gardener
#### Выполнение:
```python
class TomatoBush:
    def __init__(self, num_tomatoes):
        self.tomatoes = [Tomato(index) for index in range(1, num_tomatoes + 1)]

    def grow_all(self):
        for tomato in self.tomatoes:
            tomato.grow()

    def all_are_ripe(self):
        return all(tomato.is_ripe() for tomato in self.tomatoes)

    def give_away_all(self):
        self.tomatoes = []
```
#### Результат:
![Меню](https://github.com/Knysha04/SoftwareEngineering/blob/main/pic/Tema9.7.png)

Класс Gardener:
1. Создайте класс Gardener
2. Создайте метод init (), внутри которого будут определены два динамических свойства: name (передается параметром, является публичным) и _plant (принимает объект класса TomatoBush). После написания этого блока кода в комментарии к нему укажите какими являются эти два свойства
3. Создайте метод work(), который заставляет садовника работать, что позволяет растению становиться более зрелым
4. Создайте метод harvest(), который проверяет, все ли плоды созрели. Если все, то садовник собирает урожай. Если нет, то метод печатает предупреждение
5. Создайте статический метод knowledge_base(), который выведет в консоль справку по садоводству
#### Выполнение:
```python
class Gardener:
    def __init__(self, name, plant):
        self.name = name
        self._plant = plant

    def work(self):
        self._plant.grow_all()

    def harvest(self):
        if self._plant.all_are_ripe():
            print("Сбор урожая...")
            self._plant.give_away_all()
        else:
            print("Помидоры не созрели. Продолжай выращивать.")
```
#### Результат:
![Меню](https://github.com/Knysha04/SoftwareEngineering/blob/main/pic/Tema9.8.png)

Вызовите справку по садоводству
#### Выполнение:
```python
    @staticmethod
    def knowledge_base():
        print("База знаний садовода:")
        print("- Поливай растения регулярно.")
        print("- Нужно больше солнечнного света.")
        print("- ИСпользуй удобрение для улучшение почвы.")

Gardener.knowledge_base()
```
#### Результат:
![Меню](https://github.com/Knysha04/SoftwareEngineering/blob/main/pic/Tema9.9.png)
#### Вывод:

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
