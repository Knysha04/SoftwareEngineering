# Тема 2. Базовые операции языка Python
### Отчет по Теме #2 выполнила:
- Кныш Анна Анатольевна
- ПИЭ-22-1

| Задание | Лаб. раб. | Сам. раб. |
| ------ | ------ | ------ |
| Задание 1 | + | + |
| Задание 2 | + | + |
| Задание 3 | + | + |
| Задание 4 | + | + |
| Задание 5 | + | + |
| Задание 6 | + | + |
| Задание 7 | + | + |
| Задание 8 | + | + |
| Задание 9 | + | + |
| Задание 10 | + | + |

Работу проверили:
- к.э.н., доцент Панов М.А.

## Лабораторная работа №1
## Задание №1
### Выведите в консоль три строки. Первая – любое число. Вторая – любое число в виде строки. Третья – любое число с плавающей точкой.
#### Выполнение:
```python
print(123)
print('123')
print(1.23)
```
#### Результат:
![Lab1](https://github.com/Knysha04/SoftwareEngineering/blob/main/pic/Tema2.1.png)

## Задание №2
### Выведите в консоль три строки. Первая – результат сложения или вычитания минимум двух переменных типа int. Вторая – результат сложения или вычитания минимум двух переменных типа float. Третья – результат сложения или вычитания минимум двух переменных типа int и float.
#### Выполнение:
```python
print(1823-486)
print(5.1 + 8.27)
print(3 + 7.04 + 1 + 2.33)
```
#### Результат:
![Lab2](https://github.com/Knysha04/SoftwareEngineering/blob/main/pic/Tema2.2.png)

## Задание №3
### Выведите в консоль три строки. Первая – обычная строка. Вторая – F строка с использованием заранее объявленной переменной. Третья – сложите две или более строк в одну.
#### Выполнение
```python
print('Привет, Мир!')

world = 'Мир'
print (f"Привет, {world}!")

one ='Привет, '
two ='Мир!'
print(one + two)
```
#### Результат:
![Lab3](https://github.com/Knysha04/SoftwareEngineering/blob/main/pic/Tema2.3.png)

## Задание №4
### Выведите в консоль три строки. Первая – трансформация любого типа переменной в bool. Вторая – трансформация любого типа переменной в float или int. Третья – трансформация любого типа переменной в str.
#### Выполнение:
```python
one = 'Hello'
print(bool(one))

two = 142
print(float(two))

three = None
print(str(three))
```
#### Результат:
![image](https://github.com/Knysha04/SoftwareEngineering/blob/main/pic/Tema2.4.png)

## Задание №5
### Присвойте трем переменным различные значения, воспользовавшись функцией input().
#### Выполнение:
```python
one = input('one:')
two = input('two:')
three = input('three:')
print(one, two, three)
```
#### Результат:
![image](https://github.com/Knysha04/SoftwareEngineering/blob/main/pic/Tema2.5.png)

## Задание №6
### Создайте две любые числовые переменные и выполните над ними несколько математических операций: возведение в степень, обычное деление, целочисленное деление, нахождение остатка от деления. При желании вы можете проверить как работают эти вычисления с разными типами данных, например, сначала создать две переменные int, затем создать две переменные float и наконец создать переменные типа int и float и провести над ними операции, прописанные выше.
#### Выполнение:
```python
a = 12
b = 5
print("Возведение в степень:", a**b)
print("Обычное деление:", a/b)
print("Целочисленное деление:", a//b)
print("Нахождение остатка от деления:", a%b)
```
#### Результат:
![image](https://github.com/Knysha04/SoftwareEngineering/blob/main/pic/Tema2.6.png)

## Задание №7
### Создайте любую строковую переменную и произведите над ней математическое действие умножение на любое число.
#### Выполнение:
```python
line = 'Hello!'
print(line * 6)
```
#### Результат:
![image](https://github.com/Knysha04/SoftwareEngineering/blob/main/pic/Tema2.7.png)

## Задание №8
### Посчитайте сколько раз символ ‘o’ встречается в строке ‘Hello World’.
#### Выполнение:
```python
sentence = "Hello World"
print(sentence.count('o'))
```
#### Результат:
![image](https://github.com/Knysha04/SoftwareEngineering/blob/main/pic/Tema2.8.png)

## Задание №9
### Напишите предложение ‘Hello World’ в две строки. Написанная программа должна занимать одну строку в редакторе кода.
#### Выполнение:
```python
print("Hello\nWorld")
```
#### Результат:
![image](https://github.com/Knysha04/SoftwareEngineering/blob/main/pic/Tema2.9.png)

## Задание №10
### Из предложения ‘Hello World’ выведите в консоль только 2 символ, а затем выведите слово ‘Hello’.
#### Выполнение:
```python
sentence = "Hello World"
print(sentence[1])
print(sentence[:5])
```
#### Результат:
![image](https://github.com/Knysha04/SoftwareEngineering/blob/main/pic/Tema2.10.png)

## Самостоятельная работа №1
