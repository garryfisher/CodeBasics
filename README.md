# Курс по языку Python на CodeBasics
Ссылка на курс: https://code-basics.com/ru/languages/python  

### Задания
[Задание №69. Возврат из циклов](#№69)   
[Задание №70. Цикл for](#№70)   




<a id="№69"></a>
#### №69. Возврат из циклов.

*Реализуйте функцию is_contains_char(), которая проверяет с учётом регистра, содержит ли строка указанную букву. Функция принимает два параметра:*   
- Строка   
- Буква для поиска

```
print(is_contains_char('Hexlet', 'H'))  # => True
print(is_contains_char('Hexlet', 'h'))  # => False
print(is_contains_char('Awesomeness', 'm'))  # => True
print(is_contains_char('Awesomeness', 'd'))  # => False
```
Ответ 1:
```
def is_contains_char(item, char):
    result = False
    for x in item:
        if x == char:
            result = True
    return result
```
Ответ 2:
```
def is_contains_char(item, char):
    return char in item
```
Ответ 3
```
def is_contains_char(item, char):
    return True if char in item else False
```



<a id="№70"></a>
#### №70. Цикл for.

*В одном из предыдущих уроков мы уже написали функцию filter_string(). Напомним, она принимает на вход строку и символ и возвращает новую строку, в которой удалён переданный символ во всех его позициях. На этот раз реализуйте эту функцию с помощью цикла for. Дополнительное условие: регистр исключаемого символа не имеет значения.  
Пример вызова:*   
```
text = 'If I look forward I win'   
filter_string(text, 'i')  # 'f  look forward  wn'   
filter_string(text, 'O')  # 'If I lk frward I win'
```
Ответ:  

```
def filter_string(item, char):   
    result = ''   
    for x in item:   
        if x.lower() != char.lower():   
            result += x   
    return result
```
