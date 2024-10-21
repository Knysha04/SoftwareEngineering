# Тема 7. Работа с файлами (ввод, вывод)
### Отчет по Теме #7 выполнила:
- Кныш Анна Анатольевна
- ПИЭ-22-2

| Задание | Лаб. раб. | Сам. раб. |
| ------ | ------ | ------ |
| Задание 1 | + | + |
| Задание 2 | + | + |
| Задание 3 | + | + |
| Задание 4 | + | + |
| Задание 5 | + | + |
| Задание 6 | + | - |
| Задание 7 | + | - |
| Задание 8 | + | - |
| Задание 9 | + | - |
| Задание 10 | + | - |

Работу проверили:
- к.э.н., доцент Панов М.А.

## Лабораторная работа №7
## Задание №1
### Составьте текстовый файл и положите его в одну директорию с программой на Python. Текстовый файл должен состоять минимум из двух строк.
#### Выполнение:
```python
Hello, World!
A text document for laboratory work.
```
#### Результат:
![Меню](https://github.com/Knysha04/SoftwareEngineering/blob/main/pic/Tema7.1.png)

#### Вывод: Я создала текстовый файл в одной дирктории с программой Python, созстоящий из 2 строк.
 
## Задание №2
### Напишите программу, которая выведет только первую строку из вашего файла, при этом используйте конструкцию open()/close().
#### Выполнение:
```python
f = open('input.txt', 'r')
print(f.readline())
f.close()
```
#### Результат:
![Меню](https://github.com/Knysha04/SoftwareEngineering/blob/main/pic/Tema7.2.png)

#### Вывод: С помощью конструкции open()/close(), я написала программу, которая выводит первую строку.

## Задание №3
### Напишите программу, которая выведет все строки из вашего файла в массиве, при этом используйте конструкцию open()/close().
#### Выполнение:
```python
f = open('input.txt', 'r')
print(f.readlines())
f.close()
```
#### Результат:
![Меню](https://github.com/Knysha04/SoftwareEngineering/blob/main/pic/Tema7.3.png)

#### Вывод: Чтобы вывести текст, а не первую строку, можно использовать f.readlines в конструкции open()/close().

## Задание №4
### Напишите программу, которая выведет все строки из вашего файла в массиве, при этом используйте конструкцию with open().
#### Выполнение:
```python
with open('input.txt') as f:
print(f.readlines())
```
#### Результат: 
![Меню](https://github.com/Knysha04/SoftwareEngineering/blob/main/pic/Tema7.3.png)

#### Вывод: Я использовала конструкцию with open(), чтобы вывести все строки из моего файла.

## Задание №5
### Напишите программу, которая выведет каждую строку из вашего файла отдельно, при этом используйте конструкцию with open().
#### Выполнение:
```python
with open('input.txt') as f:
for line f:print(line)
```
#### Результат:
![Меню](https://github.com/Knysha04/SoftwareEngineering/blob/main/pic/Tema7.4.png)

#### Вывод: С помощью конструктора  with open(), я вывела каждую строку из моего файла.

## Задание №6
### Напишите программу, которая будет добавлять новую строку в ваш файл, а потом выведет полученный файл в консоль. Вывод можно осуществлять любым способом.
#### Выполнение:
```python
with open('input,txt', 'a+') as f:
f.write('\nIm aditional line')
with open('input.txt', 'r') as f:
result = f.readlines()
print(result)
```
#### Результат:
![Меню](https://github.com/Knysha04/SoftwareEngineering/blob/main/pic/Tema7.5.png)

#### Вывод: Программа выводит добавленную строку в консоль.

## Задание №7
### Напишите программу, которая перепишет всю информацию, которая была у вас в файле до этого, например напишет любые данные из произвольно вами составленного списка.
#### Выполнение:
```python
lines = ['one', 'two', 'three']
with open ('input.txt')
for line in lines:
f.write('\nCycle run'+ line)
print('Done!')
```
#### Результат:
![Меню](https://github.com/Knysha04/SoftwareEngineering/blob/main/pic/Tema7.7(1).png)
![Меню](https://github.com/Knysha04/SoftwareEngineering/blob/main/pic/Tema7.7(2).png)

#### Вывод: Программа выводит добавленную строку в консоль.

## Задание №8
### Выберите любую папку на своем компьютере, имеющую вложенные директории. Выведите на печать в терминал ее содержимое, как и всех подкаталогов при помощи функции print_docs(directory).
#### Выполнение:
```python
import os
def print_docks(directoty):
    all_files = os.walk(directoty)
    for catalog in all_files:
        print(f'Папка{catalog[0]} содержит:')
        print(f'Файлы: {",".join([file for file in catalog])}')
        print('-' * 40)
print_docks('/Anna/PycharmProjects/pythonProject/main.py"')
```
#### Результат:
![Меню](https://github.com/Knysha04/SoftwareEngineering/blob/main/pic/Tema7.8.png)

#### Вывод: Функция print_docs(directory) выводит содержимое папки.

## Задание №9
### Напишите программу, которая перепишет всю информацию, которая была у вас в файле до этого, например напишет любые данные из произвольно вами составленного списка.
#### Выполнение:
```python
def longest_world(file):
    with open(file, encoding='utf-8') as f:
        words = f.read().split()
        max_lenght = len(max(words, key = len))
        for word in words:
            if len(word) == max_lenght:
                sought_words = word
        if len(sought_words) == 1:
            return sought_words[0]
        return sought_words
print(longest_world('input.txt'))
```
#### Результат:
![Меню](https://github.com/Knysha04/SoftwareEngineering/blob/main/pic/Tema7.9.png)

#### Вывод: Программа выбрала случайным образом выбрало слово "Привествие" из списка слов.

## Задание №10
### Требуется создать csv-файл «rows_300.csv» со следующими столбцами:1. № - номер по порядку (от 1 до 300); 2. Секунда – текущая секунда на вашем ПК; 3. Микросекунда – текущая миллисекунда на часах.
#### Выполнение:
```python
import csv
import datetime
import time

with open('rows_300.csv', 'w', encoding='utf-8', newline='') as f:
  writer = csv.writer(f)
  writer.writerow(['№', 'Секунда', 'Микросекунда'])
  for line in range(1, 301):
    writer.writerow([line, datetime.datetime.now().second,
             datetime.datetime.now().microsecond])
    time.sleep(0.01)
```
#### Результат:
![Меню](https://github.com/Knysha04/SoftwareEngineering/blob/main/pic/Tema7.10(1).png)
![Меню](https://github.com/Knysha04/SoftwareEngineering/blob/main/pic/Tema7.10(2).png)

#### Вывод:  Программа создала список с номерами, секундами и миллисекундами.

## Самостоятельная работа №1
## Задание №1
### Ресторан на предприятии ведет учет посещений за неделю при помощи кода работника. У них есть список со всеми посещениями за неделю. Ваша задача почитать: 1) Сколько было выдано чеков, 2) Сколько разных людей посетило ресторан, 3) Какой работник посетил ресторан больше всех раз.
#### Выполнение:
```python
