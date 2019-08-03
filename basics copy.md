# Basics
# Основа

Just printing `hello world` is not enough, is it? You want to do more than that - you want to take some input, manipulate it and get something out of it. We can achieve this in Python using constants and variables, and we'll learn some other concepts as well in this chapter.

Просто друкувати "hello world" недостатньо, чи не так? Ви хочете зробити більше, ніж це ви хочете ввести щось, маніпулювати ним і що-небудь зробити. Ми можемо досягти цього в Python, використовуючи константи і змінні, і ми дізнаємося деякі інші поняття, а також в цій главі.

## Comments
## Коментарі
_Comments_ are any text to the right of the `#` symbol and is mainly useful as notes for the reader of the program.

_Comments_-це будь-який текст праворуч від символу ' # ' і в основному корисний в якості заміток для читача програми.

For example:
Для прикладу:

```python
print('hello world') # Нотатка про те що друкує ця функція
```

or:
або:

```python
print('hello world') #Нотатка про те що друкує ця функція
```

Use as many useful comments as you can in your program to:
Використовуйте якомога більше корисних коментарів в програмі, щоб:


- explain assumptions
- explain important decisions
- explain important details
- explain problems you're trying to solve
- explain problems you're trying to overcome in your program, etc.

- пояснити припущення
- пояснити важливі рішення
- пояснити важливі деталі
- пояснити проблеми, які ви намагаєтеся вирішити
- пояснити проблеми, які ви намагаєтеся подолати в своїй програмі і т. д.


[*Code tells you how, comments should tell you why*](http://www.codinghorror.com/blog/2006/12/code-tells-you-how-comments-tell-you-why.html).

[*Код говорить вам, як, коментарі повинні сказати вам, чому*][*Code tells you how, comments should tell you why*](http://www.codinghorror.com/blog/2006/12/code-tells-you-how-comments-tell-you-why.html).

This is useful for readers of your program so that they can easily understand what the program is doing. Remember, that person can be yourself after six months!

Це корисно для читачів вашої програми, щоб вони могли легко зрозуміти, що робить програма. Пам'ятайте, що цією людиною можете бути Ви самі через півроку!

## Literal Constants

## Литеральные Константи

An example of a literal constant is a number like `5`, `1.23`, or a string like `'This is a string'` or `"It's a string!"`.

Прикладом літеральной константи є числa типу "5", " 1.23" або рядок типу "це рядок" або " це рядок!".

It is called a literal because it is _literal_ - you use its value literally. The number `2` always represents itself and nothing else - it is a _constant_ because its value cannot be changed. Hence, all these are referred to as literal constants.

Він називається літералом, тому що це _literal_ - ви використовуєте його значення буквально. Число " 2 " завжди представляє себе і нічого більше - це _constant_, тому що його значення не може бути змінено. Отже, всі вони називаються константами.


## Numbers
## Числа

Numbers are mainly of two types - integers and floats.
Числа в основному бувають двох типів-цілі і з плаваючою комою (не цілі, "3.14").

An example of an integer is `2` which is just a whole number.
Прикладом цілого числа є "2", яке є просто цілим числом.

Examples of floating point numbers (or _floats_ for short) are `3.23` and `52.3E-4`. The `E` notation indicates powers of 10. In this case, `52.3E-4` means `52.3 * 10^-4^`.

Прикладами чисел з плаваючою комою (або _floats_ для стислості) є `3.23` і `52.3 E-4`. Позначення " E " вказує на ступені 10. В цьому випадку `52.3 E-4` означає `52.3 * 10^-4^`.


> **Note for Experienced Programmers**
> 
> There is no separate `long` type. The `int` type can be an integer of any size.

> * * Примітка Для досвідчених програмістів**

> Немає окремого "long" типу. Тип ' int ' може бути цілим числом будь-якого розміру.

## Strings
## Стрічки

A string is a _sequence_ of _characters_. Strings are basically just a bunch of words.
Рядок (string) - це _sequence_ of _characters_ (набір букв). Рядки в основному просто купа слів.

You will be using strings in almost every Python program that you write, so pay attention to the following part.

Ви будете використовувати рядки майже в кожній програмі Python, яку ви пишете, тому зверніть увагу на наступну частину.

### Single Quote
### одинарні лапка

You can specify strings using single quotes such as `'Quote me on this'`.

Ви можете вказати рядки, використовуючи одинарні лапки 'такі як Quote me on this'.

All white space i.e. spaces and tabs, within the quotes, are preserved as-is.

Всі прогалини (пробіли), тобто прогалини і таби, в лапках, зберігаються як є.

### Double Quotes
### подвійні лапки

Strings in double quotes work exactly the same way as strings in single quotes. An example is `"What's your name?"`.

Рядки в подвійних лапках працюють точно так само, як рядки в одинарних лапках. Наприклад `"як тебе звуть?"`.

### Triple Quotes {#triple-quotes}
### Потрійні лапки {#triple-quotes}

You can specify multi-line strings using triple quotes - (`"""` or `'''`). You can use single quotes and double quotes freely within the triple quotes. An example is:

Ви можете вказати багаторядкові рядки, використовуючи потрійні лапки-(`"""`або`'''`). Ви можете використовувати одинарні лапки і подвійні лапки вільно в потрійних лапках. Приклад:

```python
'''This is a multi-line string. This is the first line.
This is the second line.
"What's your name?," I asked.
He said "Bond, James Bond."
'''
```


```python
'''Це багаторядковий рядок. Це перший рядок.
Це другий.
"Як тебе звати?" - Запитав я.
Він сказав: "Бонд, Джеймс Бонд."
'''
```


### Strings Are Immutable
### Рядки Незмінні

This means that once you have created a string, you cannot change it. Although this might seem like
a bad thing, it really isn't. We will see why this is not a limitation in the various programs that
we see later on.

Це означає, що після того, як ви створили рядок, ви не можете змінити його. Хоча це може здатися
поганим, але це не так. Ми побачимо, чому це не є обмеженням в різних програмах, які
побачимо пізніше.

> **Note for C/C++ Programmers**
> 
> There is no separate `char` data type in Python. There is no real need for it and I am sure you won't miss it.

> * * Примітка для програмістів C / C++ **
> 
> В Python немає окремого типу даних "char". У цьому немає необхідності, і я впевнений, що ви не сумуватимете за ним.

<!-- -->

> **Note for Perl/PHP Programmers**
> 
> Remember that single-quoted strings and double-quoted strings are the same - they do not differ in any way.

> * * Примітка для програмістів Perl / PHP**
> 
> Пам'ятайте, що рядки в одинарних і подвійних лапках однакові-вони нічим не відрізняються.

### The format method
### Метод format

Sometimes we may want to construct strings from other information. This is where the `format()` method is useful.

Іноді ми можемо захотіти побудувати рядки з іншої інформації. Тут корисний метод format ().

Save the following lines as a file `str_format.py`:

Збережіть наступні рядки у вигляді файлу str_format.py`:

```python
age = 20
name = 'Swaroop'

print('{0} was {1} years old when he wrote this book'.format(name, age))
print('Why is {0} playing with that python?'.format(name))
```

```python
age = 20
name = 'Swaroop'

print('{0} було {1} років  коли він написав цю книгу'.format(name, age))
print('Чому {0} грається з тим Python?'.format(name))
```


Output:
Вихід:

```
$ python str_format.py
Swaroop was 20 years old when he wrote this book
Why is Swaroop playing with that python?
```

```
$ python str_format.py
Swaroop було 20 років коли він написав цю книгу
Чому Swaroop грається з тим  Python?
```

**How It Works**
** Як Це Працює**

A string can use certain specifications and subsequently, the `format` method can be called to substitute those specifications with corresponding arguments to the `format` method.

Рядок може використовувати певні специфікації, а потім метод "format" може бути викликаний для заміни цих специфікацій відповідними аргументами методу "format".

Observe the first usage where we use `{0}` and this corresponds to the variable `name` which is the first argument to the format method. Similarly, the second specification is `{1}` corresponding to `age` which is the second argument to the format method. Note that Python starts counting from 0 which means that first position is at index 0, second position is at index 1, and so on.

Зверніть увагу на перше використання, де ми використовуємо " {0}", і це відповідає змінної "name", яка є першим аргументом методу format. Аналогічно, друга Специфікація '{1}' відповідає 'віку', який є другим аргументом методу format. Зверніть увагу, що Python починає відлік з 0, що означає, що перша позиція має індекс 0, друга позиція має індекс 1, і так далі.

Notice that we could have achieved the same using string concatenation:

Зверніть увагу, що ми могли б досягти того ж за допомогою конкатенації рядків:

```python
name + ' is ' + str(age) + ' years old'
```

```python
name + ' має ' + str(age) + ' років'
```


but that is much uglier and error-prone. Second, the conversion to string would be done automatically by the `format` method instead of the explicit conversion to strings needed in this case. Third, when using the `format` method, we can change the message without having to deal with the variables used and vice-versa.


але це набагато потворніше і більше щансів отримати помилку. По-друге, перетворення в рядок буде виконуватися автоматично методом "format" замість явного перетворення рядка, необхідного в цьому випадку. По-третє, при використанні методу "format" ми можемо змінити повідомлення без необхідності мати справу з використовуваними змінними і навпаки.


Also note that the numbers are optional, so you could have also written as:
Також зверніть увагу, що числа є необов'язковими, тому ви могли б також написати:

```python
age = 20
name = 'Swaroop'

print('{} was {} years old when he wrote this book'.format(name, age))
print('Why is {} playing with that python?'.format(name))
```

```python
age = 20
name = 'Swaroop'

print('{} було {} років  коли він написав цю книгу'.format(name, age))
print('Чому {} грається з тим Python?'.format(name))
```

which will give the same exact output as the previous program.
що дасть той самий результат, що і попередня програма.

We can also name the parameters:
Ми також можемо назвати параметри:

```python
age = 20
name = 'Swaroop'

print('{name} was {age} years old when he wrote this book'.format(name=name, age=age))
print('Why is {name} playing with that python?'.format(name=name))
```
```python
age = 20
name = 'Swaroop'

print('{name} було {age} років  коли він написав цю книгу'.format(name=name, age=age))
print('Чому {name} грається з тим Python?'.format(name=name))
```

which will give the same exact output as the previous program.

що дасть той самий точний результат, що і попередня програма.

Python 3.6 introduced a shorter way to do named parameters, called "f-strings":
Python 3.6 представив коротший спосіб виконання іменованих параметрів, званих " F-рядками"("f-strings"):

```python
age = 20
name = 'Swaroop'

print(f'{name} was {age} years old when he wrote this book')  # notice the 'f' before the string
print(f'Why is {name} playing with that python?')  # notice the 'f' before the string
```

```python
age = 20
name = 'Swaroop'

print(f'{name} було {age} років  коли він написав цю книгу'.format(name, age)) # зверніть увагу на 'f' перед рядком
print(f'Чому {name} грається з тим Python?'.format(name)) # зверніть увагу на 'f' перед рядком
```



which will give the same exact output as the previous program.
що дасть той самий точний результат, що і попередня програма.

What Python does in the `format` method is that it substitutes each argument value into the place of the specification. There can be more detailed specifications such as:

Те, що Python робить у методі "format", полягає в тому, що він замінює кожне значення аргументу на місце специфікації. Можуть бути більш детальні специфікації такі як:

```python
# decimal (.) precision of 3 for float '0.333'
print('{0:.3f}'.format(1.0/3))
# fill with underscores (_) with the text centered
# (^) to 11 width '___hello___'
print('{0:_^11}'.format('hello'))
# keyword-based 'Swaroop wrote A Byte of Python'
print('{name} wrote {book}'.format(name='Swaroop', book='A Byte of Python'))
```


```python
# десяткове число (.) точність 3 для float '0.333'
print ('{0:.3f}'.farmat(1.0/3))
# заповнити підкресленнями (_) з текстом по центру
# ( ^ ) до 11 width'___hello___'
frint('{0:_^11}'.format('hello'))
# на основі ключових слів "Swaroop написав A Byte of Python"
print('{name} написав {book}'.format(ім'я= 'Swaroop', книга= 'A Byte of Python'))
```

Output:
Вивід:

```
0.333
___hello___
Swaroop написав A Byte of Python
```

Since we are discussing formatting, note that `print` always ends with an invisible "new line" character (`\n`) so that repeated calls to `print` will all print on a separate line each. To prevent this newline character from being printed, you can specify that it should `end` with a blank:

Оскільки ми обговорюємо форматування, зверніть увагу, що "print" завжди закінчується невидимим символом "нового рядка" ("\n"), так що повторні виклики "друку" будуть друкуватися на окремому рядку кожен. Щоб цей символ нового рядка не друкувався, можна вказати, що він повинен закінчуватись пробілом:

```python
print('a', end='')
print('b', end='')
```

Output is:

Вивід:

```
ab
```

Or you can `end` with a space:
Або ви можете "закінчити" пробілом:

```python
print('a', end=' ')
print('b', end=' ')
print('c')
```

Output is:
Виведеться ось це:

```
a b c
```

### Escape Sequences
### escape-послідовність

Suppose, you want to have a string which contains a single quote (`'`), how will you specify this string? For example, the string is `"What's your name?"`. You cannot specify `'What's your name?'` because Python will be confused as to where the string starts and ends. So, you will have to specify that this single quote does not indicate the end of the string. This can be done with the help of what is called an _escape sequence_. You specify the single quote as `\'` : notice the backslash. Now, you can specify the string as `'What\'s your name?'`.

Припустимо, ви хочете мати рядок, що містить одну лапку ( ' ), як ви вкажете цей рядок? Наприклад, рядок `"як тебе звуть?"`. Ви не можете вказати 'What's your name?' тому що Python буде плутати, де починається і закінчується рядок. Таким чином, вам треба буде вказати, що ця одинарна лапка не вказує на кінець рядка. Це можна зробити за допомогою того, що називається _escape sequence_. Вказати одинарну лапку як "\'" : зверніть увагу на зворотну косу риску. Тепер ви можете вказати рядок як 'What\'s your name?'.

Another way of specifying this specific string would be `"What's your name?"` i.e. using double quotes. Similarly, you have to use an escape sequence for using a double quote itself in a double quoted string. Also, you have to indicate the backslash itself using the escape sequence `\\`.

Інший спосіб вказати цей конкретний рядок `"What's your name?"`тобто використовуючи подвійні лапки. Аналогічно, ви повинні використовувати escape-послідовність для використання подвійної лапки в рядку з подвійними лапками. Крім того, ви повинні вказати зворотну косу риску перед зворотньою косою рискою, використовуючи escape-послідовність `\\`.

What if you wanted to specify a two-line string? One way is to use a triple-quoted string as shown [previously](#triple-quotes) or you can use an escape sequence for the newline character - `\n` to indicate the start of a new line. An example is:

Що робити, якщо ви хочете вказати дворядковий рядок? Один із способів-використовувати рядок у потрійних лапках, як показано [раніше] (#triple-quotes), або ви можете використовувати escape - послідовність для символу нового рядка `\n`, щоб вказати початок нового рядка. Приклад:


```python
'This is the first line\nThis is the second line'
```

```python
'Це перший рядок\nЦе другий рядок'
```

Another useful escape sequence to know is the tab: `\t`. There are many more escape sequences but I have mentioned only the most useful ones here.

Іншою корисною Escape-послідовністю є Таб: '\ t'. Є ще багато escape-послідовностей, але я згадав тільки самі корисні.


One thing to note is that in a string, a single backslash at the end of the line indicates that the string is continued in the next line, but no newline is added. For example:

Слід зазначити, що в рядку одна зворотна коса риса в кінці рядка вказує, що рядок триває в наступному рядку, але новий рядок не додається. Наприклад:

```python
"This is the first sentence. \
This is the second sentence."
```

```python
"Це перше речення. \
Це друге речення."
```


is equivalent to

```python
"This is the first sentence. This is the second sentence."
```

```python
"Це перше речення.Це друге речення."
```

### Raw String
### Необроблений Рядок

If you need to specify some strings where no special processing such as escape sequences are handled, then what you need is to specify a _raw_ string by prefixing `r` or `R` to the string. An example is:

Якщо вам потрібно вказати деякі рядки, де не обробляються спеціальні обробки, такі як escape-послідовності, то вам потрібно вказати рядок _raw_, додавши префікс " r " або " R " до рядка. Приклад:

```python
r"Newlines are indicated by \n"
```

```python
r" нові рядки позначаються \n
```

> **Note for Regular Expression Users**
> 
> Always use raw strings when dealing with regular expressions. Otherwise, a lot of backwhacking may be required. For example, backreferences can be referred to as `'\\1'` or `r'\1'`.

> * * Примітка Для користувачів регулярних виразів**
> 
> Завжди використовуйте необроблені рядки при роботі з регулярними виразами. В іншому випадку може знадобитися багато "backwhacking". Наприклад, зворотні посилання можуть називатися `'\\1'` або `r'\1'`.



## Variable
## Змінні

Using just literal constants can soon become boring - we need some way of storing any information and manipulate them as well. This is where _variables_ come into the picture. Variables are exactly what the name implies - their value can vary, i.e., you can store anything using a variable. Variables are just parts of your computer's memory where you store some information. Unlike literal constants, you need some method of accessing these variables and hence you give them names.

Використання тільки літеральних констант скоро може стати нудним - нам потрібен якийсь спосіб зберігання будь-якої інформації і маніпулювання нею. Ось тут-то і з'являються змінні. Змінні - це саме те, про що говорить їх назва - їх значення може змінюватися, тобто ви можете зберігати що завгодно, використовуючи змінну. Змінні - це просто частини пам'яті вашого комп'юте ра, де ви зберігаєте деяку інформацію. На відміну від літеральних констант, вам потрібен якийсь метод доступу до цих змінних і, отже, ви даєте їм імена.

## Identifier Naming
## Identifier Naming## Іменування Ідентифікаторів


Variables are examples of identifiers. _Identifiers_ are names given to identify _something_. There are some rules you have to follow for naming identifiers:

Змінні є прикладами ідентифікаторів. _Identifiers_-імена, дані для ідентифікації чогось. Є кілька правил, яким ви повинні слідувати для іменування ідентифікаторів:

- The first character of the identifier must be a letter of the alphabet (uppercase ASCII or lowercase ASCII or Unicode character) or an underscore (`_`).
- The rest of the identifier name can consist of letters (uppercase ASCII or lowercase ASCII or Unicode character), underscores (`_`) or digits (0-9).
- Identifier names are case-sensitive. For example, `myname` and `myName` are _not_ the same. Note the lowercase `n` in the former and the uppercase `N` in the latter.
- Examples of _valid_ identifier names are `i`, `name_2_3`. Examples of _invalid_ identifier names are `2things`, `this is spaced out`, `my-name` and `>a1b2_c3`.

- Першим символом ідентифікатора повинна бути буква алфавіту (верхній або нижній регістр ASCII або символ Юнікоду) або символ підкреслення (`_`).
- Інша частина імені ідентифікатора може складатися з букв (верхній регістр ASCII або нижній регістр ASCII або символ Юнікоду), підкреслення ( ` _ ' ) або цифр (0-9).
- Імена ідентифікаторів чутливі до регістру. Наприклад, "myname" і "myName" - це не одне й те саме. Зверніть увагу на нижній регістр " n "в першому і верхній регістр" N " у другому.
- Приклади _дійсних, валідних_ імен ідентифікаторів `i`, `name_2_3`. Приклади _невалідних, недійсних_ імен ідентифікаторів - `2things`, `this is spaced out`, `my-name` and `>a1b2_c3`.

## Data Types

Variables can hold values of different types called _data types_. The basic types are numbers and strings, which we have already discussed. In later chapters, we will see how to create our own types using [classes](./oop.md#classes).

## Тип даних

Змінні можуть містити значення різних типів, званих _data types_(_типи данних_). Основними типами є числа і рядки, про які ми вже говорили. У наступних розділах ми побачимо, як створювати власні типи за допомогою [класів] (./oop.md#classes).

## Object
## Об'єкт

Remember, Python refers to anything used in a program as an _object_.  This is meant in the generic sense. Instead of saying "the _something_"', we say "the _object_".

Пам'ятайте, Python відноситься до всього, що використовується в програмі як до _обєктів_.  Це мається на увазі в загальному сенсі. Замість того щоб говорити "щось", ми говоримо "об'єкт".

> **Note for Object Oriented Programming users**:
>
> Python is strongly object-oriented in the sense that everything is an object including numbers, strings and functions.

> **Примітка для користувачів об'єктно-орієнтованого програмування **:
>
> Python строго об'єктно-орієнтований в тому сенсі, що все є об'єктом, включаючи числа, рядки і функції.

We will now see how to use variables along with literal constants. Save the following example and run the program.

Зараз ми побачимо, як використовувати змінні з константами. Збережіть такий приклад і запустіть програму.

## How to write Python programs
## Як писати програми на Python

Henceforth, the standard procedure to save and run a Python program is as follows:

Далі стандартна процедура, щоб зберегти і запустити програму на мові Python наступним чином:

### For PyCharm
### Для PyCharm

1. Open [PyCharm](./first_steps.md#pycharm).
2. Create new file with the filename mentioned.
3. Type the program code given in the example.
4. Right-click and run the current file.

1. Відкрити [PyCharm] (./first_steps.md#pycharm).
2. Створіть новий файл із зазначеним ім'ям файлу.
3. Введіть код програми, наведений у Прикладі.
4. Клацніть правою кнопкою миші та запустіть поточний файл.


NOTE: Whenever you have to provide [command line arguments](./modules.md#modules), click on `Run` -> `Edit Configurations` and type the arguments in the `Script parameters:` section and click the `OK` button:

Примітка: всякий раз, коли ви повинні надати [аргументи командного рядка](./modules.md#modules), натисніть `Виконати` - > `змінити конфігурації` (`Run` -> `Edit Configurations`) і введіть аргументи в розділі "Параметри скрипта:" (`Script parameters:`) та натисніть кнопку `ОК`:



![PyCharm command line arguments](./img/pycharm_command_line_arguments.png)

![аргументи командного рядка PyCharm](./img/pycharm_command_line_arguments.png)


### For other editors
### Для інших редакторів

1. Open your editor of choice.
2. Type the program code given in the example.
3. Save it as a file with the filename mentioned.
4. Run the interpreter with the command `python program.py` to run the program.

1. Відкрийте редактор за вашим вибором.
2. Введіть код програми, наведений у Прикладі.
3. Збережіть його у вигляді файлу з вказаним ім'ям файлу.
4. Запустіть інтерпретатор за допомогою команди `python program.py` щоб запустити програму.

### Example: Using Variables And Literal Constants
### Приклад: Використання Змінних І Констант

Type and run the following program:
Введіть і запустіть наступну програму:

```python
# Filename : var.py
i = 5
print(i)
i = i + 1
print(i)

s = '''This is a multi-line string.
This is the second line.'''
print(s)
```


```python
# імя файлу : var.py
i = 5
print(i)
i = i + 1
print(i)

s = '''Це багато рядкова стрічка.
Це другий рядок.'''
print(s)
```


Output:
Вивід:

```
5
6
This is a multi-line string.
This is the second line.
```

```
5
6
Це багато рядкова стрічка.
Це другий рядок.
```

**How It Works**
** Як Це Працює**

Here's how this program works. First, we assign the literal constant value `5` to the variable `i` using the assignment operator (`=`). This line is called a statement because it states that something should be done and in this case, we connect the variable name `i` to the value `5`. Next, we print the value of `i` using the `print` statement which, unsurprisingly, just prints the value of the variable to the screen.

Ось як працює ця програма. По-перше, ми присвоюємо літеральне постійне значення `5` змінної `i` за допомогою оператора присвоювання (`=`). Цей рядок називається оператором, тому що він стверджує, що щось має бути зроблено, і в цьому випадку ми пов'язуємо ім'я змінної `i` зі значенням `5`. Потім ми друкуємо значення `i`, використовуючи оператор `print`, який, як не дивно, просто виводить значення змінної на екран.

Then we add `1` to the value stored in `i` and store it back. We then print it and expectedly, we get the value `6`.

Потім ми додаємо `1` до значення, що зберігається в `i`, і зберігаємо його назад. Потім ми друкуємо його і очікувано отримуємо значення `6`.

Similarly, we assign the literal string to the variable `s` and then print it.

Аналогічним чином, ми присвоюємо Рядкове значення змінної `S` і потім роздруковуємо його.



> **Note for static language programmers**
> 
> Variables are used by just assigning them a value. No declaration or data type definition is needed/used.

> ** Примітка для програмістів на статичних мовах**
> 
> Змінні використовуються, просто присвоївши їм значення. Оголошення або визначення типу даних не потрібно / не використовується.


## Logical And Physical Line
## Логічна І Фізична Лінія

A physical line is what you _see_ when you write the program. A logical line is what _Python sees_ as a single statement. Python implicitly assumes that each _physical line_ corresponds to a _logical line_.

Фізичний рядок-це те, що ви бачите, коли пишете програму. Логічний рядок - це те, що бачить _python_ як одне твердження. Python неявно припускає, що кожен _фізичний рядок_ відповідає _логічному рядку_.

An example of a logical line is a statement like `print 'hello world'` - if this was on a line by itself (as you see it in an editor), then this also corresponds to a physical line.

Прикладом логічного рядка є оператор типу `print ('hello world')` - якщо це в рядку саме по собі (як ви бачите в редакторі), то це також відповідає фізичної рядку.

Implicitly, Python encourages the use of a single statement per line which makes code more readable.

Неявно Python заохочує використання одного оператора на рядок, що робить код більш читаним.

If you want to specify more than one logical line on a single physical line, then you have to explicitly specify this using a semicolon (`;`) which indicates the end of a logical line/statement. For example:

Якщо ви хочете вказати кілька логічних рядків в одному фізичному рядку, ви повинні явно вказати це за допомогою точки з комою (`;`), яка вказує на кінець логічного рядка / оператора. Наприклад:


```python
i = 5
print(i)
```

```python
i = 5
print(i)
```

is effectively same as
одним і тим самим що і

```python
i = 5;
print(i);
```

```python
i = 5;
print(i);
```

which is also same as
що у свою чергу ж тим самим що і

```python
i = 5; print(i);
```
```python
i = 5; print(i);
```

and same as
і тим самим що

```python
i = 5; print(i)
```

```python
i = 5; print(i)
```

However, I *strongly recommend* that you stick to *writing a maximum of a single logical line on each single physical line*. The idea is that you should never use the semicolon. In fact, I have _never_ used or even seen a semicolon in a Python program.

Проте, я * наполеглево рекомендую * дотримуватися * запис максимум одного логічного рядка на кожному окремому фізичному рядку*. Ідея полягає в тому, що ви ніколи не повинні використовувати крапку з комою. Насправді, я ніколи не використовував цього знку або навіть не бачив крапки з комою в програмі Python.

There is one kind of situation where this concept is really useful: if you have a long line of code, you can break it into multiple physical lines by using the backslash. This is referred to as _explicit line joining_:

Існує одна ситуація, коли ця концепція дійсно корисна: якщо у вас є довгий рядок коду, Ви можете розбити його на кілька фізичних рядків за допомогою риски. Це називається _explicit line joining_:

```python
s = 'This is a string. \
This continues the string.'
print(s)
```

```python
s = 'Це стрічка. \
Це продовження стрічки.'
print(s)
```

Output:
Вивід:

```
This is a string. This continues the string.
```

```
Це стрічка. Це продовження стрічки.
```


Similarly,
Подібно

```python
i = \
5
```

```python
i = \
5
```

is the same as
є тим самим що і

```python
i = 5
```

```python
i = 5
```

Sometimes, there is an implicit assumption where you don't need to use a backslash. This is the case where the logical line has a starting parentheses, starting square brackets or a starting curly braces but not an ending one. This is called *implicit line joining*. You can see this in action when we write programs using [list](./data_structures.md#lists) in later chapters.

Іноді існує неявне припущення, що вам не потрібно використовувати зворотну косу риску. Це той випадок, коли в логічному рядку є дужки, квадратні дужки або фігурні дужки. Це називається *неявне з'єднання рядків*. Ви можете побачити це в дії, коли ми пишемо програми за допомогою [списку](./data_structures.md#lists) в наступних розділах.

## Indentation
## Поглиблення


Whitespace is important in Python. Actually, *whitespace at the beginning of the line is important*. This is called _indentation_. Leading whitespace (spaces and tabs) at the beginning of the logical line is used to determine the indentation level of the logical line, which in turn is used to determine the grouping of statements.

Пробіли важливі в Python. Насправді, * пробіли на початку рядка важливі*. Це називається _indentation_. Початкові пробіли (пробіли і табуляція) на початку логічного рядка використовуються для визначення рівня відступу логічного рядка, який в свою чергу використовується для визначення угруповання операторів.

This means that statements which go together _must_ have the same indentation. Each such set of statements is called a *block*. We will see examples of how blocks are important in later chapters.

Це означає, що заяви, які йдуть разом _повинні_ мати однаковий відступ. Кожен такий набір операторів називається блоком. Приклади того, як важливі блоки, ми побачимо в наступних главах.

One thing you should remember is that wrong indentation can give rise to errors. For example:

Одна річ, яку Ви повинні пам'ятати, що неправильний відступ може призвести до помилок. Наприклад:


```python
i = 5
# Error below! Notice a single space at the start of the line
 print('Value is', i)
print('I repeat, the value is', i)
```

```python
i = 5
# Помилка нижче! Зверніть увагу на пробіл на початку рядка
 print('Value is', i)
print('Я повторюю, значення ', i)
```

When you run this, you get the following error:

При запуску цього з'являється таке повідомлення про помилку:

```
  File "whitespace.py", line 3
    print('Value is', i)
    ^
IndentationError: unexpected indent
```


```
  File "whitespace.py", line 3
    print('Value is', i)
    ^
IndentationError: unexpected indent
```


Notice that there is a single space at the beginning of the second line. The error indicated by Python tells us that the syntax of the program is invalid i.e. the program was not properly written. What this means to you is that _you cannot arbitrarily start new blocks of statements_ (except for the default main block which you have been using all along, of course). Cases where you can use new blocks will be detailed in later chapters such as the [control flow](./control_flow.md#control_flow).

Зверніть увагу, що на початку другого рядка є один пробіл. Помилка, зазначена Python говорить нам, що синтаксис програми є неприпустимим, тобто програма не була правильно написана. Це означає, що ви не можете довільно запускати нові блоки тверджень (за винятком основного блоку за замовчуванням, який ви використовували весь час, звичайно). Випадки, коли ви можете використовувати нові блоки, будуть детально описані в наступних розділах, таких як [потік управління](./control_flow.md#control_flow).

> **How to indent**
> 
> Use four spaces for indentation. This is the official Python language recommendation. Good editors will automatically do this for you. Make sure you use a consistent number of spaces for indentation, otherwise your program will not run or will have unexpected behavior.

> * * Як відступати**
> 
> Використовуйте чотири пробіли для відступу. Це офіційна рекомендація мови Python. Хороші редактори автоматично зроблять це за вас. Переконайтеся, що ви використовуєте однакову кількість пробілів для відступів, інакше програма не буде запущена або матиме несподівану поведінку.


<!-- -->

> **Note to static language programmers**
> 
> Python will always use indentation for blocks and will never use braces. Run `from __future__ import braces` to learn more.


> * * Примітка для програмістів які використовують статичної мови**
> 
> Python завжди буде використовувати відступи для блоків і ніколи не буде використовувати дужки. Запустіть 
> Python will always use indentation for blocks and will never use braces. Run `from __future__ import braces`, щоб дізнатися більше.

## Summary
## Резюме

Now that we have gone through many nitty-gritty details, we can move on to more interesting stuff such as control flow statements. Be sure to become comfortable with what you have read in this chapter.


Тепер, коли ми пройшли через безліч дрібних деталей, ми можемо перейти до більш цікавих речей, таких як оператори потоку управління. Переконайтеся, що ви освоїлися з тим, що прочитали в цьому розділі.