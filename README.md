# Тема 7. Работа с файлами (ввод, вывод)
### Отчет по Теме #7 выполнила:
- Кныш Анна Анатольевна
- ПИЭ-22-1

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

## Самостоятельная работа №7
## Задание №1
### Ресторан на предприятии ведет учет посещений за неделю при помощи кода работника. У них есть список со всеми посещениями за неделю. Ваша задача почитать: 1) Сколько было выдано чеков, 2) Сколько разных людей посетило ресторан, 3) Какой работник посетил ресторан больше всех раз.
#### Выполнение:
```python
from collections import Counter
import re

def count_words(text):
    # Используем регулярное выражение для разделения текста на слова
    words = re.findall(r'\b\w+\b', text.lower())

    # Считаем количество использований каждого слова
    word_counts = Counter(words)

    # Находим самое популярное слово и количество его использований
    most_common_word, count = word_counts.most_common(1)[0]

    return most_common_word, count

if __name__ == "__main__":
    # Задайте абсолютный путь к вашему файлу
    file_path = "C:/Users/Anna/PycharmProjects/pythonProject/input.txt"

    try:
        # Читаем текст из файла
        with open(file_path, 'r', encoding='utf-8') as file:
            text = file.read()

        most_common_word, count = count_words(text)

        # Вывод результатов
        print(f"Самое популярное слово: {most_common_word}")
        print(f"Количество использований: {count}")

    except FileNotFoundError:
        print(f"Файл по пути '{file_path}' не найден.")
    except Exception as e:
        print(f"Произошла ошибка: {e}")
```
#### Результат:
![Меню](https://github.com/Knysha04/SoftwareEngineering/blob/main/pic/Tema7.11(1).png)
![Меню](https://github.com/Knysha04/SoftwareEngineering/blob/main/pic/Tema7.11(2).png)

#### Вывод: Программа успешно считывает текст из указанного файла, а затем подсчитывает количество слов и определяет самое популярное слово с его количеством использований. Убедитесь, что указанный путь к файлу верен и файл существует. В случае ошибки при чтении файла программа предоставит соответствующее уведомление.
 
## Задание №2
### У вас появилась потребность в ведении книги расходов, посмотрев все существующие варианты вы пришли к выводу что вас ничего не устраивает и нужно все делать самому. Напишите программу для учета расходов. Программа должна позволять вводить информацию о расходах, сохранять ее в файл и выводить существующие данные в консоль. Ввод информации происходит через консоль. Результатом выполнения задачи будет: скриншот файла с учетом расходов, листинг кода, и вывод в консоль, с демонстрацией работоспособности программы.
#### Выполнение:
```python
import csv
import os
import datetime

def create_expenses_file(file_name):
    with open(file_name, 'w', encoding='utf-8', newline='') as f:
        writer = csv.writer(f)
        writer.writerow(['Дата', 'Сумма', 'Трата'])

def add_expense(file_name, amount, expense):
    date = datetime.datetime.now().strftime('%Y-%m-%d %H:%M:%S')
    with open(file_name, 'a', encoding='utf-8', newline='') as f:
        writer = csv.writer(f)
        writer.writerow([date, amount, expense])

def display_expenses(file_name):
    with open(file_name, 'r', encoding='cp1251', errors='replace') as f:
        reader = csv.reader(f)
        for row in reader:
            print(row)

def main():
    expenses_file = "expenses.csv"

    if not os.path.isfile(expenses_file):
        create_expenses_file(expenses_file)

    while True:
        print("\nВыберите действие:")
        print("1. Добавить расход")
        print("2. Просмотреть расходы")
        print("3. Выйти")

        choice = input("Введите номер действия: ")

        if choice == "1":
            amount = input("Введите сумму расхода: ")
            expense = input("Введите трать: ")
            add_expense(expenses_file, amount, expense)
            print("Расход успешно добавлен!")

        elif choice == "2":
            display_expenses(expenses_file)

        elif choice == "3":
            print("Программа завершена.")
            break

        else:
            print("Некорректный ввод. Пожалуйста, выберите существующий вариант.")

if __name__ == "__main__":
    main()
```
#### Результат:
![Меню](https://github.com/Knysha04/SoftwareEngineering/blob/main/pic/Tema7.12.png)

#### Вывод: Эта программа на Python предоставляет простой механизм учета расходов через консоль. Пользователь может вводить информацию о расходах, которая сохраняется в файле `expenses.json`, и просматривать текущие расходы. Программа обеспечивает удобный способ отслеживания финансов и может быть легко расширена для добавления дополнительных функциональностей по необходимости.

## Задание №3
### Имеется файл input.txt с текстом на латинице. Напишите программу, которая выводит следующую статистику по тексту: количество букв латинского алфавита; число слов; число строк.
#### Выполнение:
```python
def get_statistics(file_path):
    try:
        with open(file_path, 'r', encoding='utf-8') as file:
            text = file.read()

            # Подсчет количества букв латинского алфавита
            alphabet_letters_count = sum(c.isalpha() and c.isascii() for c in text)

            # Подсчет количества слов
            word_count = len(text.split())

            # Подсчет количества строк
            line_count = text.count('\n') + 1

            return alphabet_letters_count, word_count, line_count
    except FileNotFoundError:
        return None

if __name__ == "__main__":
    file_path = 'input.txt'

    statistics = get_statistics(file_path)

    if statistics is not None:
        alphabet_letters_count, word_count, line_count = statistics
        print(f"Количество букв латинского алфавита: {alphabet_letters_count}")
        print(f"Количество слов: {word_count}")
        print(f"Количество строк: {line_count}")
    else:
        print(f"Файл '{file_path}' не найден.")
```
#### Результат:
![Меню](https://github.com/Knysha04/SoftwareEngineering/blob/main/pic/Tema7.13.png)

#### Вывод: Данная программа на Python выполняет анализ текстового файла `input.txt`, выводя статистику, включающую количество букв латинского алфавита, число слов и количество строк. Простота использования и понятность вывода делают этот инструмент удобным для быстрого анализа текстовых данных на латинице. Убедитесь, что файл `input.txt` существует в том же каталоге, что и скрипт, и запустите программу для получения статистики.

## Задание №4
### Напишите программу, которая получает на вход предложение, выводит его в терминал, заменяя все запрещенные слова звездочками * (количество звездочек равно количеству букв в слове). Запрещенные слова, разделенные символом пробела, хранятся в текстовом файле input.txt. Все слова в этом файле записаны в нижнем регистре. Программа должна заменить запрещенные слова, где бы они ни встречались, даже в середине другого слова. Замена производится независимо от регистра: если файл input.txt содержит запрещенное слово exam, то слова exam, Exam, ExaM, EXAM и exAm должны быть заменены на ****.
#### Выполнение:
```python
def censor_text(sentence, forbidden_words):
    for word in forbidden_words:
        # Заменяем каждое вхождение слова независимо от регистра
        sentence = sentence.replace(word, '*' * len(word), -1)
    return sentence


def load_forbidden_words(file_path):
    try:
        with open(file_path, 'r', encoding='utf-8') as file:
            forbidden_words = [word.strip().lower() for word in file.read().split()]
        return forbidden_words
    except FileNotFoundError:
        return None


if __name__ == "__main__":
    sentence = input("Введите предложение: ")

    forbidden_words = load_forbidden_words('input.txt')

    if forbidden_words is not None:
        censored_sentence = censor_text(sentence.lower(), forbidden_words)
        print("Цензурированное предложение:")
        print(censored_sentence)
    else:
        print("Файл 'input.txt' не найден.")
```
#### Результат: 
![Меню](https://github.com/Knysha04/SoftwareEngineering/blob/main/pic/Tema7.14.png)

#### Вывод: Программа успешно реализует цензуру текста, заменяя запрещенные слова звездочками. Замена слов происходит независимо от регистра, что делает ее более универсальной. 

## Задание №5
### Самостоятельно придумайте и решите задачу, которая будет взаимодействовать с текстовым файлом.
#### Выполнение:
```python
def calculate_average_grade(file_path):
    try:
        with open(file_path, 'r', encoding='utf-8') as file:
            lines = file.readlines()

            total_students = len(lines)
            total_grades = sum(int(line.split(':')[1].strip()) for line in lines)

            if total_students > 0:
                average_grade = total_grades / total_students
                return average_grade
            else:
                return None
    except FileNotFoundError:
        return None

if __name__ == "__main__":
    file_path = 'input.txt'

    average_grade = calculate_average_grade(file_path)

    if average_grade is not None:
        print(f"Средний балл всех студентов: {average_grade:.2f}")
    else:
        print(f"Файл '{file_path}' не найден или не содержит данных.")
```
#### Результат:
![Меню](https://github.com/Knysha04/SoftwareEngineering/blob/main/pic/Tema7.15(1).png)
![Меню](https://github.com/Knysha04/SoftwareEngineering/blob/main/pic/Tema7.15(2).png)

#### Вывод: Программа успешно вычисляет средний балл студентов, используя данные из файла `input.txt`, где указаны их имена и оценки. Для этого предоставлены случайные имена и оценки в диапазоне до 5. Пользователь может легко адаптировать эти данные или добавить свои собственные для дополнительного тестирования программы.

## Общий вывод: Данная работа помогла углубиться в тему работы с файлами в Python, а так же научить нескольким новым способам работы с ними, что неслмненно поомжет в дальнейшей разработке.
