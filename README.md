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

Класс TomatoBush:
1. Создайте класс TomatoBush
2. Определите метод init(), который будет принимать в качестве параметра количество томатов и на его основе будет создавать список объектов класса Tomato. Данный список будет храниться внутри динамического свойства tomatoes
3. Создайте метод grow_all(), который будет переводить все объекты из списка томатов на следующий этап созревания
4. Создайте метод all_are_ripe(), который будет возвращать True, если все томаты из списка стали спелыми.
5. Создайте метод give_away_all(), который будет чистить список томатов после сбора урожая Класс Gardener
   
Класс Gardener:
1. Создайте класс Gardener
2. Создайте метод init (), внутри которого будут определены два динамических свойства: name (передается параметром, является публичным) и _plant (принимает объект класса TomatoBush). После написания этого блока кода в комментарии к нему укажите какими являются эти два свойства
3. Создайте метод work(), который заставляет садовника работать, что позволяет растению становиться более зрелым
4. Создайте метод harvest(), который проверяет, все ли плоды созрели. Если все, то садовник собирает урожай. Если нет, то метод печатает предупреждение
5. Создайте статический метод knowledge_base(), который выведет в консоль справку по садоводству
#### Выполнение:
```python
class Tomato: # Словарь, описывающий состояния помидора
    states = {
        0: "отсутствует",
        1: "цветение",
        2: "зеленый",
        3: "красный"
    }

    def __init__(self, index): # Инициализация экземпляра помидора с индексом и начальным состоянием
        self._index = index
        self._state = 0

    def grow(self): # Увеличивает состояние помидора на один, если оно меньше трех
        if self._state < 3:
            self._state += 1

    def is_ripe(self):
        return self._state == 3


class TomatoBush:
    def __init__(self, num_tomatoes): # Инициализация куста помидоров с заданным количеством помидоров
        self.tomatoes = [Tomato(index) for index in range(1, num_tomatoes + 1)]

    def grow_all(self): # Выращивает все помидоры на кусте
        for tomato in self.tomatoes:
            tomato.grow()

    def all_are_ripe(self):  # Проверяет, все ли помидоры созрели
        return all(tomato.is_ripe() for tomato in self.tomatoes)

    def give_away_all(self):  # Удаляет все помидоры с куста (симулирует сбор урожая)
        self.tomatoes = []


class Gardener:
    def __init__(self, name, plant): # Инициализация садовода с именем и растением
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

    @staticmethod
    def knowledge_base():
        print("База знаний садовода:")
        print("- Поливай растения регулярно.")
        print("- Нужно больше солнечнного света.")
        print("- ИСпользуй удобрение для улучшение почвы.")

Gardener.knowledge_base() # Вывод базы знаний садовода
```
#### Результат:
![Меню](https://github.com/Knysha04/SoftwareEngineering/blob/main/pic/Tema9.6.png)
![Меню](https://github.com/Knysha04/SoftwareEngineering/blob/main/pic/Tema9.7.png)
![Меню](https://github.com/Knysha04/SoftwareEngineering/blob/main/pic/Tema9.8.png)
![Меню](https://github.com/Knysha04/SoftwareEngineering/blob/main/pic/Tema9.9.png)
#### Вывод: В данном коде реализована система для моделирования процесса выращивания помидоров с использованием классов Tomato, TomatoBush и Gardener. Класс Tomato описывает состояние помидора, включая его стадии роста. Класс TomatoBush управляет коллекцией помидоров и предоставляет методы для их роста и проверки зрелости. Класс Gardener представляет садовода, который может ухаживать за растениями и собирать урожай, если помидоры созрели. Метод knowledge_base в классе Gardener выводит полезные советы по садоводству, что делает программу не только функциональной, но и образовательной. Вызов Gardener.knowledge_base() демонстрирует, как можно предоставить пользователю информацию о правильном уходе за растениями, что является важной частью садоводства.

## Задание №2
### Создайте объекты классов TomatoBush и Gardener
#### Выполнение:
```python
class Tomato: # Словарь, описывающий состояния помидора
    states = {
        0: "отсутствует",
        1: "цветение",
        2: "зеленый",
        3: "красный"
    }

    def __init__(self, index): # Инициализация экземпляра помидора с индексом и начальным состоянием
        self._index = index
        self._state = 0

    def grow(self): # Увеличивает состояние помидора на один, если оно меньше трех
        if self._state < 3:
            self._state += 1

    def is_ripe(self):
        return self._state == 3


class TomatoBush:
    def __init__(self, num_tomatoes): # Инициализация куста помидоров с заданным количеством помидоров
        self.tomatoes = [Tomato(index) for index in range(1, num_tomatoes + 1)]

    def grow_all(self): # Выращивает все помидоры на кусте
        for tomato in self.tomatoes:
            tomato.grow()

    def all_are_ripe(self):  # Проверяет, все ли помидоры созрели
        return all(tomato.is_ripe() for tomato in self.tomatoes)

    def give_away_all(self):  # Удаляет все помидоры с куста (симулирует сбор урожая)
        self.tomatoes = []


class Gardener:
    def __init__(self, name, plant): # Инициализация садовода с именем и растением
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

    @staticmethod
    def knowledge_base():
        print("База знаний садовода:")
        print("- Поливай растения регулярно.")
        print("- Нужно больше солнечнного света.")
        print("- ИСпользуй удобрение для улучшение почвы.")

# Создаем объекты классов TomatoBush и Gardener
tomato_bush = TomatoBush(num_tomatoes=5)
gardener = Gardener(name="John", plant=tomato_bush)
```
#### Результат:
![Меню](https://github.com/Knysha04/SoftwareEngineering/blob/main/pic/Tema9.10.png)

### Вывод: В данном задании созданы объекты классов TomatoBush и Gardener, что позволяет моделировать процесс ухода за кустом помидоров. Класс TomatoBush управляет состоянием помидоров, включая их рост и сбор урожая, в то время как класс Gardener представляет садовода, который ухаживает за растениями и принимает решения о сборе урожая. Эта реализация демонстрирует основные принципы ООП, такие как инкапсуляция и взаимодействие объектов, а также разделяет ответственность между разными классами для упрощения логики программы.

## Задание №3
### Используя объект класса Gardener, поухаживайте за кустом с помидорами
#### Выполнение:
```python
class Tomato: # Словарь, описывающий состояния помидора
    states = {
        0: "отсутствует",
        1: "цветение",
        2: "зеленый",
        3: "красный"
    }

    def __init__(self, index): # Инициализация экземпляра помидора с индексом и начальным состоянием
        self._index = index
        self._state = 0

    def grow(self): # Увеличивает состояние помидора на один, если оно меньше трех
        if self._state < 3:
            self._state += 1

    def is_ripe(self):
        return self._state == 3


class TomatoBush:
    def __init__(self, num_tomatoes): # Инициализация куста помидоров с заданным количеством помидоров
        self.tomatoes = [Tomato(index) for index in range(1, num_tomatoes + 1)]

    def grow_all(self): # Выращивает все помидоры на кусте
        for tomato in self.tomatoes:
            tomato.grow()

    def all_are_ripe(self):  # Проверяет, все ли помидоры созрели
        return all(tomato.is_ripe() for tomato in self.tomatoes)

    def give_away_all(self):  # Удаляет все помидоры с куста (симулирует сбор урожая)
        self.tomatoes = []


class Gardener:
    def __init__(self, name, plant): # Инициализация садовода с именем и растением
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

    @staticmethod
    def knowledge_base():
        print("База знаний садовода:")
        print("- Поливай растения регулярно.")
        print("- Нужно больше солнечнного света.")
        print("- ИСпользуй удобрение для улучшение почвы.")

# Создаем объекты классов TomatoBush и Gardener
tomato_bush = TomatoBush(num_tomatoes=5)
gardener = Gardener(name="John", plant=tomato_bush)
# Ухаживаем за кустом с помидорами
gardener.work()
gardener.work()
gardener.work()
```
#### Результат:
![Меню](https://github.com/Knysha04/SoftwareEngineering/blob/main/pic/Tema9.11.png)

### Вывод: В процессе выполнения кода создаются объекты TomatoBush и Gardener, после чего садовод "John" ухаживает за кустом три раза, что позволяет помидорам расти. Это демонстрирует взаимодействие между объектами и использование методов для управления состоянием растений. В результате, программа иллюстрирует основные принципы объектно-ориентированного программирования, такие как инкапсуляция и взаимодействие объектов.

## Задание №4
### Попробуйте собрать урожай, когда томаты еще не дозрели. Продолжайте ухаживать за ними
#### Выполнение:
```python
class Tomato: # Словарь, описывающий состояния помидора
    states = {
        0: "отсутствует",
        1: "цветение",
        2: "зеленый",
        3: "красный"
    }

    def __init__(self, index): # Инициализация экземпляра помидора с индексом и начальным состоянием
        self._index = index
        self._state = 0

    def grow(self): # Увеличивает состояние помидора на один, если оно меньше трех
        if self._state < 3:
            self._state += 1

    def is_ripe(self):
        return self._state == 3


class TomatoBush:
    def __init__(self, num_tomatoes): # Инициализация куста помидоров с заданным количеством помидоров
        self.tomatoes = [Tomato(index) for index in range(1, num_tomatoes + 1)]

    def grow_all(self): # Выращивает все помидоры на кусте
        for tomato in self.tomatoes:
            tomato.grow()

    def all_are_ripe(self):  # Проверяет, все ли помидоры созрели
        return all(tomato.is_ripe() for tomato in self.tomatoes)

    def give_away_all(self):  # Удаляет все помидоры с куста (симулирует сбор урожая)
        self.tomatoes = []


class Gardener:
    def __init__(self, name, plant): # Инициализация садовода с именем и растением
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

    @staticmethod
    def knowledge_base():
        print("База знаний садовода:")
        print("- Поливай растения регулярно.")
        print("- Нужно больше солнечнного света.")
        print("- ИСпользуй удобрение для улучшение почвы.")

# Создаем объекты классов TomatoBush и Gardener
tomato_bush = TomatoBush(num_tomatoes=5)
gardener = Gardener(name="John", plant=tomato_bush)
# Попробуем собрать урожай, когда томаты еще не дозрели
gardener.harvest()

# Ухаживаем за кустом с помидорами
gardener.work()
gardener.work()
gardener.work()

# Собираем урожай
gardener.harvest()
```
#### Результат:
![Меню](https://github.com/Knysha04/SoftwareEngineering/blob/main/pic/Tema9.11.png)

#### Вывод: В данном коде реализована система для моделирования ухода за кустом помидоров с использованием классов Tomato, TomatoBush и Gardener. Садовод по имени "John" сначала пытается собрать урожай до того, как помидоры полностью созреют, и получает сообщение о том, что сбор урожая невозможен. Затем он ухаживает за кустом три раза, что способствует росту помидоров. После этого садовод снова пытается собрать урожай

## Задание №5
### Соберите урожай
#### Выполнение:
```python
class Tomato: # Словарь, описывающий состояния помидора
    states = {
        0: "отсутствует",
        1: "цветение",
        2: "зеленый",
        3: "красный"
    }

    def __init__(self, index): # Инициализация экземпляра помидора с индексом и начальным состоянием
        self._index = index
        self._state = 0

    def grow(self): # Увеличивает состояние помидора на один, если оно меньше трех
        if self._state < 3:
            self._state += 1

    def is_ripe(self):
        return self._state == 3


class TomatoBush:
    def __init__(self, num_tomatoes): # Инициализация куста помидоров с заданным количеством помидоров
        self.tomatoes = [Tomato(index) for index in range(1, num_tomatoes + 1)]

    def grow_all(self): # Выращивает все помидоры на кусте
        for tomato in self.tomatoes:
            tomato.grow()

    def all_are_ripe(self):  # Проверяет, все ли помидоры созрели
        return all(tomato.is_ripe() for tomato in self.tomatoes)

    def give_away_all(self):  # Удаляет все помидоры с куста (симулирует сбор урожая)
        self.tomatoes = []


class Gardener:
    def __init__(self, name, plant): # Инициализация садовода с именем и растением
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

    @staticmethod
    def knowledge_base():
        print("База знаний садовода:")
        print("- Поливай растения регулярно.")
        print("- Нужно больше солнечнного света.")
        print("- ИСпользуй удобрение для улучшение почвы.")

# Создаем объекты классов TomatoBush и Gardener
tomato_bush = TomatoBush(num_tomatoes=5)
gardener = Gardener(name="John", plant=tomato_bush)
# Попробуем собрать урожай, когда томаты еще не дозрели
gardener.harvest()

# Ухаживаем за кустом с помидорами
gardener.work()
gardener.work()
gardener.work()

# Собираем урожай
gardener.harvest()
# Собираем урожай
gardener.harvest()

# Выводим информацию о зрелости томатов в кусте после сбора урожая
print("\nAre all tomatoes ripe?", gardener._plant.all_are_ripe())

# Проверяем состояние каждого томата после сбора урожая
for i, tomato in enumerate(gardener._plant.tomatoes, 1):
    print(f"Tomato {i}: State - {Tomato.states[tomato._state]}, Ripe - {tomato.is_ripe()}")
```
#### Результат:
![Меню](https://github.com/Knysha04/SoftwareEngineering/blob/main/pic/Tema9.12.png)
![Меню](https://github.com/Knysha04/SoftwareEngineering/blob/main/pic/Tema9.13.png)

#### Вывод: В конце программы выводится информация о состоянии каждого помидора, что позволяет увидеть, как изменилось их состояние в процессе работы. Этот код не только демонстрирует принципы ООП, такие как инкапсуляция и взаимодействие объектов, но и учит важным жизненным урокам о терпении, внимании к деталям и необходимости заботы о том, что мы хотим вырастить.
## Вывод: Объектно-ориентированное программирование (ООП) в Python, как и в других языках программирования, предоставляет ряд преимуществ и инструментов для более удобной и эффективной разработки программ.
