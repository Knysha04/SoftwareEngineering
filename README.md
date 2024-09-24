# Тема 3. Операторы, условия, циклы
### Отчет по Теме #3 выполнила:
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

## Лабораторная работа №1
## Задание №1
### Создайте две переменные, значение которых будете вводить через консоль. Также составьте условие, в котором созданные ранее переменные будут сравниваться, если условие выполняется, то выведете в консоль «Выполняется», если нет, то «Не выполняется».
#### Выполнение:
```python
one = int(input('Введите значение первой переменной: '))
two = int(input('Введите значение второй переменной: '))
if one >= two:
    print('Выполняется')
else:
    print('Не выполняется')
```
#### Результат:

![Меню](https://github.com/Knysha04/SoftwareEngineering/blob/main/pic/1.1.png)
#### Вывод: В данной программе используется консоль для ввода занчений, а также конструкция if-else для сравнения двух переменных и вывода сооттвествующего ответа.

## Задание №2
### Напишите программу, которая будет определять значения переменной меньше 0, больше 0 и меньше 10 или больше 10. это нужно реализовать при помощи одной переменной, значение которой будет вводится через консоль, а также при помощи конструкций if, elif, else.
#### Выполнение:
```python
one = int(input('Введите значение переменной: '))
if one < 0:
    print('Переменная меньше 0')
elif 0 < one < 10:
    print('Переменная больше 0 и меньше 10')
else:
    print('Переменная больше 10')
```

#### Результат:

![Меню](https://github.com/Knysha04/SoftwareEngineering/blob/main/pic/2.1.png)
#### Вывод: В данной программе используется консоль для ввода занчений, а также конструкция if-elif-else для сравнения трех переменных и вывода сооттвествующего ответа.

## Задание №3
### Напишите программу, в которой будет проверяться есть ли переменная в указанном массиве используя логический оператор in. Самостоятельно посмотрите, как работает программа со значениями которых нет в массиве numbers.
#### Выполнение
```python
numbers = [1, 3, 4, 6, 8, 9]
value = int(input('Введите значение переменной: '))
if value in numbers:
    print('Переменная есть в данном массиве')
else:
    print('Переменной нет в этом массиве')
```
#### Результат:

![Меню](https://github.com/Knysha04/SoftwareEngineering/blob/main/pic/3.1.png)
#### Вывод: С помощью логичского оператора in проверяется есть ли введеная нами переменная в созданном массиве. Результат обозначается соответсвующим выражением.

## Задание №4
### Напишите программу, которая будет определять находится ли переменная в указанном массиве и если да, то проверьте четная она или нет. Самостоятельно протестируйте данную программу с разными значениями переменной value.
#### Выполнение:
```python
numbers = [1, 3, 4, 6, 8, 9, 15, 16, 73, 321, 322]
value = int(input('Введите значение переменной: '))
if value in numbers:
    if value % 2 == 0:
        print('Переменная четная и есть в массиве numbers')
    else:
        print('Переменная нечетная и есть в массиве numbers')
else:
    print(f'Переменной нет в массиве number и она равна {value}')
```
#### Результат:

![Меню](https://github.com/Knysha04/SoftwareEngineering/blob/main/pic/4.1.png)
#### Вывод: Программа проверяет одновременно два условия с помощью конструкции if-else.

## Задание №5
### Напишите программу, в которой циклом for значения переменной i будут меняться от 0 до 10 и посмотрите, как разные виды сравнений и операций работают в цикле.
#### Выполнение:
```python
for i in range(10):
    print('i=', i)
    if i == 0:
        i += 2
    if i == 1:
        continue
    if i == 2 or i == 3:
        print('Переменная равна 2 или 3')
    elif i in [4, 5, 6]:
        print('Переменная равна 4,5 или 6')
    else:
        break
```
#### Результат:
![Меню](https://github.com/Knysha04/SoftwareEngineering/blob/main/pic/5.1.png)
#### Вывод: В этом задании мы продемонстрировали использование цикла for для перебора значений i. Внтури цикла были использованы различные виды сравнений и операция.

## Задание №6
### Напишите программу, в которой при помощи цикла for определяется есть ли переменная value в строке string и посмотрите, как работает оператор else для циклов. Самостоятельно посмотрите, что выведет программа, если значение переменной value оказалось в строке string. 
#### Выполнение:
```python
string = 'Привет всем изучающим Python!'
value = input()
for i in string:
    if i == value:
        index = string.find(value)
        print(f"Буква '{value}' есть в строке под {index} индексом")
        break
else:
    print(f"Буквы '{value}' нет в указанной строке")
```
#### Результат:
![Меню](https://github.com/Knysha04/SoftwareEngineering/blob/main/pic/6.1.png)
#### Вывод: В этом задании мы продемонстрировали использование оператора for для определения, есть ли в строке string введенная переменная или нет.

## Задание №7
### Напишите программу, в которой вы наглядно посмотрите, как работает цикл for проходя в обратном порядке, то есть, к примеру не от 0 до 10, а от 10 до 0. В уже готовой программе показано вычитание из 100, а вам во время реализации программы будет необходимо придумать свой вариант применения обратного цикла
#### Выполнение:
```python
value = 100
for i in range(10, -1, -1):
    value -= i
    print(i, value)
```
#### Результат:
![Меню](https://github.com/Knysha04/SoftwareEngineering/blob/main/pic/7.1.png)
#### Вывод: Данная программа яляется примером того, как работает цикл for.

## Задание №8
### Напишите программу используя цикл while, внутри которого есть какие-либо проверки, но быть осторожным, поскольку циклы while при неправильно написанных условиях могут становится бесконечными, как указано в примере далее.
#### Выполнение:
```python
value = 0
while value < 100:
    if value == 0:
        value += 10
    elif value // 5 > 1:
        value *= 5
    else:
        value -= 5
    print(value)
```
#### Результат:
Бесконечный цикл:
![Меню](https://github.com/Knysha04/SoftwareEngineering/blob/main/pic/8.1.(2).png)
Конечный цикл:
![Меню](https://github.com/Knysha04/SoftwareEngineering/blob/main/pic/8.1.png)
#### Вывод: В данном коде мы использовали цикл while для изменения значения переменной value на основе различных условий. 

## Задание №9
### Напишите программу с использованием вложенных циклов и одной проверкой внутри них. Самое главное, не забудьте, что нельзя использовать одинаковые имена итерируемых переменных, когда вы используете вложенные циклы
#### Выполнение:
```python
value = 0
for i in range(10):
        for j in range(10):
            if i != j:
                value += j
            else:
                pass #оператор-заглушка
print(value)
```
#### Результат:
![Меню](https://github.com/Knysha04/SoftwareEngineering/blob/main/pic/9.1.png)
#### Вывод: В данном коде мы использовали внешний цикл for, внутри каждой итерации внешнего цикла, внутренний цикл for  выполняется , меняя значение j от 0 до 9. Внутри вложенного цикла, условие с if проверяется для каждой пары.

## Задание №10
### Напишите программу с использованием flag, которое будет определять есть ли нечетное число в массиве. В данной задаче flag выступает в роли индикатора встречи нечетного числа в исходном массиве, четных чисел.
#### Выполнение:
```python
even_array =  [2, 4, 6, 8, 9]
flag = False
for value in even_array:
    if value % 2 == 1:
        flag = True

if flag is True:
    print('В массиве есть нечетное число')
else:
    print('В массиве все числа четные')
```
#### Результат:
![Меню](https://github.com/Knysha04/SoftwareEngineering/blob/main/pic/10.1.png)
#### Вывод: В этой программе flag используется как индикатор, чтобы определить, есть ли нечетные числа в исходном массиве even_array. Если хотя бы одно нечетное число найдено, то flag устанавливается в True, и это значение проверяется в конце программы.
## Задание №10
### Напишите программу с использованием flag, которое будет определять есть ли нечетное число в массиве. В данной задаче flag выступает в роли индикатора встречи нечетного числа в исходном массиве, четных чисел.
#### Выполнение:
```python
even_array =  [2, 4, 6, 8, 9]
flag = False
for value in even_array:
    if value % 2 == 1:
        flag = True

if flag is True:
    print('В массиве есть нечетное число')
else:
    print('В массиве все числа четные')
```
#### Результат:
![image](https://github.com/legendarykk/Programmnaya_Inzheneriya/assets/146570109/1c37a60a-0f10-42ce-8772-c17af9cca912)

## Самостоятельная работа №1
## Задание №1
### Напишите программу, которая преобразует 1 в 31. Для выполнения поставленной задачи необходимо обязательно и только один раз использовать: Цикл for, *= 5, += 1. Никаких других действий или циклов использовать нельзя.
#### Выполнение:
```python
value = 1
for i in range(2):
    value *= 5
    value += 1
print(value)
```
#### Результат:
![image](https://github.com/legendarykk/Programmnaya_Inzheneriya/assets/146570109/069b5880-bed0-49c5-b462-c7e11891057b)

#### Вывод: В данном коде цикл 'for' дважды прогоняет число 1 через две математические операции, *5 и +1, после чего подает результат, равный 31, на вывод.

## Задание №2
### Напишите программу, которая фразу «Hello World» выводит в обратном порядке, и каждая буква находится в одной строке консоли. При этом необходимо обязательно использовать любой цикл, а также программа должна занимать не более 3 строк в редакторе кода.
#### Выполнение:
```python
sentence = "Hello World"
for i in range(len(sentence)-1, -1, -1):
    print(sentence[i])
```
#### Результат:
![image](https://github.com/legendarykk/Programmnaya_Inzheneriya/assets/146570109/20c685ec-4291-44af-a01b-23847335f834)

#### Вывод: В данном коде, с помощью отрицательного щшага, по одной выводим буквы из заданного предложения в обратном направлении.

## Задание №3
### Напишите программу, на вход которой поступает значение из консоли, оно должно быть числовым и в диапазоне от 0 до 10 включительно (это необходимо учесть в программе). Если вводимое число не подходит по требованиям, то необходимо вывести оповещение об этом в консоль и остановить программу. Код должен вычислять в каком диапазоне находится полученное число. Нужно учитывать три диапазона: от 0 до 3 включительно, от 3 до 6, от 6 до 10 включительно. Результатом работы программы будет выведенный в консоль диапазон. Программа должна занимать не более 10 строчек в редакторе кода.
#### Выполнение:
```python
number = int(input("Введите число от 0 до 10: "))
if number < 0 or number > 10:
    print("Данное число не подходит по условиям, пожалуйста введите число от 0 до 10")
elif 0 <= number <= 3:
    print("Данное число входит в диапазон от 0 до 3 (включительно)")
elif 3 < number < 6:
    print("Данное число входит в диапазон от 3 до 6")
elif 6 <= number <= 10:
    print("Данное число входит в диапазон от 6 до 10 (включительно)")
```
#### Результат:
Вариант 1:
![image](https://github.com/legendarykk/Programmnaya_Inzheneriya/assets/146570109/c9299d40-aa87-45dd-be2b-c93b4de801d8)
Вариант 2:
![image](https://github.com/legendarykk/Programmnaya_Inzheneriya/assets/146570109/24cd70ec-97c5-4f4f-b101-e864abe38aee)
Вариант 3:
![image](https://github.com/legendarykk/Programmnaya_Inzheneriya/assets/146570109/9471101a-7c61-4182-b2d3-7f29ab779ffd)
Вариант 4:
![image](https://github.com/legendarykk/Programmnaya_Inzheneriya/assets/146570109/754e486c-4949-4813-8785-6eebcdb21b93)

#### Вывод: После получения введенного числа, код проверяет выполнения первого условия (число должно входить в диапазон от 0 до 10), после этого, код сверяет введенное число с тремя диапазонами по очереди и выводит итоговый результат в виде текста.

## Задание №4
### Манипулирование строками. Напишите программу на Python, которая принимает предложение (на английском) в качестве входных данных от пользователя. Выполните следующие операции и отобразите результаты: Выведите длину предложения, Переведите предложение в нижний регистр, Подсчитайте количество гласных (a, e, i, o, u) в предложении, Замените все слова "ugly" на "beauty", Проверьте, начинается ли предложение с "The" и заканчивается ли на "end". Проверьте работу программы минимум на 3 предложениях, чтобы охватить проверку всех поставленных условий.
#### Выполнение:
```python
sentence1 = input("Введите предложение на английском: ")
print("Длина введенного предложения: ", len(sentence1))
sentence2 = sentence1.lower()
print("Ваше предложение в нижнем регистре: ", sentence2)
print("Кол-во гласных в введенном предложении: ", sentence2.count('a') + sentence2.count('e') + sentence2.count('i') + sentence2.count('o') + sentence2.count('u'))
sentence3 = sentence2.replace('ugly', 'beauty')
print("Измененое предложение: ", sentence3)

if sentence3.startswith('the') == True:
    print("Предложение начинается с The")
else: print("Предложение не начинается с The")

if sentence3.endswith('end') == True:
    print("Предложение заканчивается на End")
else: print("Предложение не заканчивается на End")
```
#### Результат:
![image](https://github.com/legendarykk/Programmnaya_Inzheneriya/assets/146570109/835dcf0e-d643-4437-a207-9971b80bfaf4)

#### Вывод: Код, после получения введенного предложения, сначала находит его длину с помощью метода 'len'. Затем переводит его в нижний регистр посредством метода 'lower' и выводит его в консоль. Далее считает количество каждой гласной с помощью метода 'count', складывает каждое полученное число и выводит итог в консоль. На следующем шаге с помощью метода 'replace' заменяет каждое слово 'ugly' на слово 'beauty' и выводит в консоль измененное предложение. После этого запускает проверку наличия в начале предложения слова 'The' и в конце слова 'End'. В результате выводит два итога своей проверки.
## Задание №5
### Составьте программу, результатом которой будет данный вывод в консоль.
![image](https://github.com/legendarykk/Programmnaya_Inzheneriya/assets/146570109/b49f6215-3d15-4bcd-860d-85ebd98aad49)
### Программу нужно составить из данных строк кода:
![image](https://github.com/legendarykk/Programmnaya_Inzheneriya/assets/146570109/a9356c2b-06a1-4654-97f6-4f48c0f8308a)
### Строки кода можно использовать только один раз. Не обязательно использовать все строки кода.
#### Выполнение:
```python
string = "hello"
values = [0, 2, 4, 6, 8, 10]
counter = 0
while ' world' not in string:
    memory = string
    if counter in values:
        string = string + ' world'
    print(string)
    if counter < 10:
        string = memory
    counter += 1
```
#### Результат:
![image](https://github.com/legendarykk/Programmnaya_Inzheneriya/assets/146570109/e94f769b-f0e7-412d-8cfc-8fd2a9840f41)

#### Вывод: Мы объявляем строковую переменную с именем "string", массив чисел под названием "values" и устанавливаем счетчик "counter" равным 0. Затем, в рамках цикла "while", выполняется следующий процесс: пока строка "string" не содержит слово "world" и значение счетчика "counter" меньше 10, программа выводит сначала "hello world" на одной строке, а затем "hello" на следующей строке. Когда значение счетчика достигнет 10, будет выведена фраза "hello world", а "hello" больше не будет выводиться, после чего цикл завершит свою работу.
