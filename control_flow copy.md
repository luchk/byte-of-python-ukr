# Control Flow {#control-flow}
# Потік управління (потік команд){#control-flow}


In the programs we have seen till now, there has always been a series of statements faithfully executed by Python in exact top-down order. What if you wanted to change the flow of how it works? For example, you want the program to take some decisions and do different things depending on different situations, such as printing 'Good Morning' or 'Good Evening' depending on the time of the day?

У програмах, які ми бачили до цих пір, завжди була серія тверджень, сумлінно виконуваних Python в точному порядку зверху вниз. Що якщо ви хочете змінити потік, як це працює? Наприклад, ви хочете, щоб програма приймала певні рішення і робила різні речі в залежності від різних ситуацій, наприклад, друкувала "Доброго ранку" або "Добрий вечір" в залежності від часу доби?

As you might have guessed, this is achieved using control flow statements. There are three control flow statements in Python - `if`, `for` and `while`.

Як ви могли здогадатися, це досягається за допомогою операторів управління потоком. У Python є три оператори управління потоком - `if`, `for` і `while`.

## The `if` statement
## Оператор `if`

The `if` statement is used to check a condition: *if* the condition is true, we run a block of statements (called the _if-block_), *else* we process another block of statements (called the _else-block_). The *else* clause is optional.

В `if` використовується, щоб перевірити стан: ** якщо умова істинна, то виконати блок операторів (так званий _if-block_), *ще* ми обробляємо інший блок операторів (так званий _else-block_). Пропозиція * else * є необов'язковою.

Example (save as `if.py`):

Приклад (зберегти як `if.py`):

<pre><code class="lang-python">{% include "./programs/if.py" %}</code></pre>

```python
number = 23
guess = int(input('Enter an integer : '))

if guess == number:
    # New block starts here
    print('Congratulations, you guessed it.')
    print('(but you do not win any prizes!)')
    # New block ends here
elif guess < number:
    # Another block
    print('No, it is a little higher than that')
    # You can do whatever you want in a block ...
else:
    print('No, it is a little lower than that')
    # you must have guessed > number to reach here

print('Done')
# This last statement is always executed,
# after the if statement is executed.

```

Output:

Вивід:

<pre><code>{% include "./programs/if.txt" %}</code></pre>

```python
$ python if.py
Enter an integer : 50
No, it is a little lower than that
Done

$ python if.py
Enter an integer : 22
No, it is a little higher than that
Done

$ python if.py
Enter an integer : 23
Congratulations, you guessed it.
(but you do not win any prizes!)
Done

```

**How It Works**
** Як Це Працює**

In this program, we take guesses from the user and check if it is the number that we have. We set the variable `number` to any integer we want, say `23`. Then, we take the user's guess using the `input()` function. Functions are just reusable pieces of programs. We'll read more about them in the [next chapter](./functions.md#functions).

У цій програмі, ми беремо здогади від користувача і перевірити, якщо це номер, який у нас є. Ми встановлюємо змінну у `number` будь-яке ціле число, скажімо `23`. Потім ми приймаємо припущення користувача за допомогою функції `input ()`. Функції - це просто багаторазові частини програм. Детальніше про них ми прочитаємо в [наступному розділі](./functions.md#functions).

We supply a string to the built-in `input` function which prints it to the screen and waits for input from the user. Once we enter something and press kbd:[enter] key, the `input()` function returns what we entered, as a string. We then convert this string to an integer using `int` and then store it in the variable `guess`. Actually, the `int` is a class but all you need to know right now is that you can use it to convert a string to an integer (assuming the string contains a valid integer in the text).

Ми поставляємо рядок вбудованої функції вводу, яка виводить її на екран і чекає введення від користувача. Як тільки ми вводимо щось і натискаємо клавішу kbd:[enter], функція `input()` повертає те, що ми ввели, у вигляді рядка. Потім ми перетворимо цей рядок у ціле число, використовуючи `int`, а потім зберігаємо його в змінній `guess`. Насправді, `int` - це клас, але все, що вам потрібно знати прямо зараз, це те, що ви можете використовувати його для перетворення рядка в ціле число (за умови, що рядок містить припустиме ціле число в тексті).

Next, we compare the guess of the user with the number we have chosen. If they are equal, we print a success message. Notice that we use indentation levels to tell Python which statements belong to which block. This is why indentation is so important in Python. I hope you are sticking to the "consistent indentation" rule. Are you?

Потім ми порівнюємо припущення користувача з номером, який ми обрали. Якщо вони рівні, ми друкуємо повідомлення про успіх. Зверніть увагу, що ми використовуємо рівні відступи, щоб повідомити Python, які оператори належать якому блоку. Ось чому відступи настільки важливі в Python. Сподіваюся, ви дотримуєтеся правила "послідовного відступу". А ти?

Notice how the `if` statement contains a colon at the end - we are indicating to Python that a block of statements follows.

Зверніть увагу, як оператор `if` містить двокрапку в кінці-ми вказуємо Python, що слідуєь блок операторів.


Then, we check if the guess is less than the number, and if so, we inform the user that they must guess a little higher than that. What we have used here is the `elif` clause which actually combines two related `if else-if else` statements into one combined `if-elif-else` statement. This makes the program easier and reduces the amount of indentation required.

Потім ми перевіряємо, чи менше припущення, і якщо так, ми повідомляємо користувачеві, що вони повинні вгадати трохи вище цього. Те, що ми скористалися тут `Еліф` пункт, який фактично поєднує в собі два суміжних, якщо ще-якщо заяви ще один комбінований `якщо-Еліф-небудь заяву. Це робить програму простіше і зменшує кількість відступів, необхідних.

The `elif` and `else` statements must also have a colon at the end of the logical line followed by their corresponding block of statements (with proper indentation, of course)

Оператори `elif` і `else` також повинні мати двокрапку в кінці логічного рядки, за яким йде відповідний блок операторів (з відповідним відступом, звичайно)

You can have another `if` statement inside the if-block of an `if` statement and so on - this is called a nested `if` statement.

Ви можете мати інший оператор  `if` всередині if-блоку оператора `if `і т. д. - Це називається вкладеним оператором `if`.

Remember that the `elif` and `else` parts are optional. A minimal valid `if` statement is:
Пам'ятайте, що частини `elif` і `else` є необов'язковими. Мінімальний допустимий оператор `if`:

```python
if True:
    print('Yes, it is true')
```

```python
if True:
    print(' так, це правда')
```

After Python has finished executing the complete `if` statement along with the associated `elif` and `else` clauses, it moves on to the next statement in the block containing the `if` statement. In this case, it is the main block (where execution of the program starts), and the next statement is the `print('Done')` statement. After this, Python sees the ends of the program and simply finishes up.

Після того, як Python завершив виконання повного оператора `if` разом з відповідними пропозиціями `elif` і `else`, він переходить до наступного оператору в блоці, що містить оператор `if`. У цьому випадку це основний блок (де починається виконання програми), а наступний оператор-оператор `print('Done')`. Після цього Python бачить кінці програми і просто закінчує роботу.

Even though this is a very simple program, I have been pointing out a lot of things that you should notice. All these are pretty straightforward (and surprisingly simple for those of you from C/C++ backgrounds). You will need to become aware of all these things initially, but after some practice you will become comfortable with them, and it will all feel 'natural' to you.

Незважаючи на те, що це дуже проста програма, я вказував на багато речей, які ви повинні помітити. Все це досить просто (і дивно просто для тих з вас, хто моє знання C/C++). Спочатку вам потрібно буде усвідомити всі ці речі, але після деякої практики ви відчуєте себе комфортно з ними, і все це буде здаватися вам "природним".


> **Note for C/C++ Programmers**
> 
> There is no `switch` statement in Python. You can use an `if..elif..else` statement to do the same thing (and in some cases, use a [dictionary](./data_structures.md#dictionary) to do it quickly)

> * * Примітка для програмістів C / C++ **
> 
> В Python немає оператора `switch`. Ви можете використовувати `if..elif..else`, щоб зробити те ж саме (і в деяких випадках, використовувати [словник] ./data_structures.md#dictionary)), щоб зробити це швидко)



## The while Statement
## Оператор while

The `while` statement allows you to repeatedly execute a block of statements as long as a condition is true. A `while` statement is an example of what is called a *looping* statement. A `while` statement can have an optional `else` clause.

Оператор `while` дозволяє повторно виконувати блок операторів до тих пір, поки умова істинна. while - приклад того, що називається *зациклення* . Оператор while може мати необов'язкову пропозицію else.

Example (save as `while.py`):
Приклад (зберегти як `while.py`):

<pre><code class="lang-python">{% include "./programs/while.py" %}</code></pre>

```python
number = 23
running = True

while running:
    guess = int(input('Enter an integer : '))

    if guess == number:
        print('Congratulations, you guessed it.')
        # this causes the while loop to stop
        running = False
    elif guess < number:
        print('No, it is a little higher than that.')
    else:
        print('No, it is a little lower than that.')
else:
    print('The while loop is over.')
    # Do anything else you want to do here

print('Done')
```

Output:
Вивід:

<pre><code>{% include "./programs/while.txt" %}</code></pre>


'''
$ python while.py
Enter an integer : 50
No, it is a little lower than that.
Enter an integer : 22
No, it is a little higher than that.
Enter an integer : 23
Congratulations, you guessed it.
The while loop is over.
Done

'''

**How It Works**
** Як Це Працює**

In this program, we are still playing the guessing game, but the advantage is that the user is allowed to keep guessing until he guesses correctly - there is no need to repeatedly run the program for each guess, as we have done in the previous section. This aptly demonstrates the use of the `while` statement.

У цій програмі ми все ще граємо в Угадайку, але перевага в тому, що користувачеві дозволено продовжувати вгадувати, поки він не вгадає правильно - немає необхідності повторно запускати програму для кожної здогади, як ми робили в попередньому розділі. Це наочно демонструє використання оператора while.

We move the `input` and `if` statements to inside the `while` loop and set the variable `running` to `True` before the while loop. First, we check if the variable `running` is `True` and then proceed to execute the corresponding *while-block*. After this block is executed, the condition is again checked which in this case is the `running` variable. If it is true, we execute the while-block again, else we continue to execute the optional else-block and then continue to the next statement.

Ми переходимо на `вхід` і `якщо`, що всередині циклу "while" та встановлюємо змінну `running` на `True`, перед  циклом while. Спочатку ми перевіряємо, чи є змінна `running ``True`, а потім приступаємо до виконання відповідного *while-block*. Після виконання цього блоку знову перевіряється умова, яка в даному випадку є змінною `running`. Якщо це правда, ми знову виконуємо while-блок, інакше ми продовжуємо виконувати необов'язковий else-block, а потім переходимо до наступного оператору.

The `else` block is executed when the `while` loop condition becomes `False` - this may even be the first time that the condition is checked. If there is an `else` clause for a `while` loop, it is always executed unless you break out of the loop with a `break` statement.

Блок `else` виконується, коли умова циклу `while` стає `False` - це може бути навіть перший раз, коли умова перевіряється. Якщо є пропозиція `else` для циклу `while`, вони завжди виконується, якщо ви не виходите з циклу за допомогою оператора `break`.


The `True` and `False` are called Boolean types and you can consider them to be equivalent to the value `1` and `0` respectively.

`True` і `False` називаються булевими типами, і їх можна вважати еквівалентними значенням `1` і `0` відповідно.


> **Note for C/C++ Programmers**
> 
> Remember that you can have an `else` clause for the `while` loop.

> * * Примітка для програмістів C / C++ **
> 
> Пам'ятайте, що ви можете мати `else` для циклу `while`.

## The `for` loop

The `for..in` statement is another looping statement which *iterates* over a sequence of objects i.e. go through each item in a sequence. We will see more about [sequences](./data_structures.md#sequence) in detail in later chapters. What you need to know right now is that a sequence is just an ordered collection of items.

## Цикл `for`

Оператор `for..in` - це ще один оператор циклу, який *повторює* дії над послідовністю об'єктів, тобто проходить через кожний елемент послідовності. Ми побачимо більше про [послідовності]](./data_structures.md#sequence) докладно в наступних главах. Що вам потрібно знати прямо зараз, що послідовність-це просто упорядкований набір елементів.

Example (save as `for.py`):
Приклад (зберегти як `for.py`):

<pre><code class="lang-python">{% include "./programs/for.py" %}</code></pre>


```python
for i in range(1, 5):
    print(i)
else:
    print('The for loop is over')

```

Output:
Вивід:

<pre><code>{% include "./programs/for.txt" %}</code></pre>

```python
$ python for.py
1
2
3
4
The for loop is over

```

**How It Works**

In this program, we are printing a *sequence* of numbers. We generate this sequence of numbers using the built-in `range` function.

У цій програмі ми друкуємо * послідовність * чисел. Ми генеруємо цю послідовність чисел за допомогою вбудованої функції `range`.

What we do here is supply it two numbers and `range` returns a sequence of numbers starting from the first number and up to the second number. For example, `range(1,5)` gives the sequence `[1, 2, 3, 4]`. By default, `range` takes a step count of 1. If we supply a third number to `range`, then that becomes the step count. For example, `range(1,5,2)` gives `[1,3]`. Remember that the range extends *up to* the second number i.e. it does *not* include the second number.

Те, що ми робимо тут, це надаємо йому два числа і `range` повертає послідовність чисел, починаючи з першого числа і до другого числа. Наприклад, `range (1,5)` дає послідовність`[1, 2, 3, 4]`. За замовчуванням `range ' приймає число кроків 1. Якщо ми поставимо третє число в `range`, то це стане лічильником кроків. Наприклад, `діапазон(1,5,2)` дає `[1,3]`. Пам'ятайте, що діапазон розширюється *до * другого числа, тобто він *не* включає друге число.

Note that `range()` generates only one number at a time, if you want the full list of numbers, call `list()` on the `range()`, for example, `list(range(5))` will result in `[0, 1, 2, 3, 4]`. Lists are explained in the [data structures chapter](./data_structures.md#data-structures).

Зверніть увагу що `range ()` генерує тільки один номер за раз, якщо ви хочете повний список номерів, виклик `list ()` на `range ()`, наприклад, `list(range(5))` призведе до`[0, 1, 2, 3, 4]`. Списки пояснюються в розділі [структури даних](./data_structures.md#data-structures)


The `for` loop then iterates over this range - `for i in range(1,5)` is equivalent to `for i in [1, 2, 3, 4]` which is like assigning each number (or object) in the sequence to i, one at a time, and then executing the block of statements for each value of `i`.  In this case, we just print the value in the block of statements.

Цикл `for` потім повторюється в цьому діапазоні - `for i in range(1,5)` еквівалентний `for i in [1, 2, 3, 4]` це схоже на присвоєння кожного числа (або об'єкта) в послідовності i, по одному за раз, а потім виконання блоку операторів для кожного значення `i`.  В цьому випадку ми просто друкуємо значення в блоці операторів.

Remember that the `else` part is optional. When included, it is always executed once after the `for` loop is over unless a [break](#break-statement) statement is encountered.

Пам'ятайте, що  частина `else`  не є обов'язковою. При включенні він завжди виконується один раз після завершення циклу `for`, якщо не зустрічається оператор [break](#break-statement).

Remember that the `for..in` loop works for any sequence. Here, we have a list of numbers generated by the built-in `range` function, but in general we can use any kind of sequence of any kind of objects! We will explore this idea in detail in later chapters.

Пам'ятайте, що цикл `for..in` працює для будь-якої послідовності. Тут у нас є список чисел, що генеруються вбудованою функцією `range`, але в цілому ми можемо використовувати будь-яку послідовність будь-яких об'єктів! Ми детально розглянемо цю ідею в наступних главах.


> **Note for C/C++/Java/C# Programmers**
> 
> The Python `for` loop is radically different from the C/C++ `for` loop. C# programmers will note that the `for` loop in Python is similar to the `foreach` loop in C#. Java programmers will note that the same is similar to `for (int i : IntArray)` in Java 1.5.
> 
> In C/C++, if you want to write `for (int i = 0; i < 5; i++)`, then in Python you write just `for i in range(0,5)`. As you can see, the `for` loop is simpler, more expressive and less error prone in Python.


> * * Примітка для програмістів C/C++/Java/C# **
> 
> Цикл Python `for `радикально відрізняється від циклу ` for` y C/C++. Програмісти C# помітять, що цикл "for в Python схожий на цикл foreach" в C#. Java-програмісти помітять, що те ж саме схоже на "for (int i : Int Array)" в Java 1.5.
> 
> В C / C++, якщо ви хочете написати `for (int i = 0; i < 5; i++)`, то в Python ви пишете тільки " for i in range(0,5)". Як ви можете бачити, цикл `for` простіше, виразніше і менш схильний до помилок в Python.
>Примітка від перекладача на Українську мову. У С++ також є цикл `fore-each` так званий `range-based` цикл і виглядає він наступним чином for(auto a : b) 

## The break Statement {#break-statement}

## Оператор break {#break-statement}

The `break` statement is used to *break* out of a loop statement i.e. stop the execution of a looping statement, even if the loop condition has not become `False` or the sequence of items has not been completely iterated over.

Оператор `break` використовується для *виходу* з оператора циклу, тобто зупинення виконання оператора циклу, навіть якщо умова циклу не стало "хибною" або послідовність елементів не була повністю пройденою

An important note is that if you *break* out of a `for` or `while` loop, any corresponding loop `else` block is **not** executed.

Важливо відзначити, що якщо ви * виходите* з циклу `for` або `while` , будь-який відповідний блок циклу `else` * * не виконується **.

Example (save as `break.py`):

Приклад (зберегти як `break.py`):.

<pre><code class="lang-python">{% include "./programs/break.py" %}</code></pre>

```python

while True:
    s = input('Enter something : ')
    if s == 'quit':
        break
    print('Length of the string is', len(s))
print('Done')

```

Output:
Вивід:

<pre><code>{% include "./programs/break.txt" %}</code></pre>

```python

$ python break.py
Enter something : Programming is fun
Length of the string is 18
Enter something : When the work is done
Length of the string is 21
Enter something : if you wanna make your work also fun:
Length of the string is 37
Enter something : use Python!
Length of the string is 11
Enter something : quit
Done

```

**How It Works**
** Як Це Працює**


In this program, we repeatedly take the user's input and print the length of each input each
time. We are providing a special condition to stop the program by checking if the user input is
`'quit'`. We stop the program by *breaking* out of the loop and reach the end of the program.

У цій програмі, ми повторно приймаємо вхідний данні користувача і друкуємо довжину кожного взідних данних кожен
раз. Ми надаємо спеціальну умову для зупинки програми, перевіряючи, чи є користувальницький ввід
`'quit'`. Ми зупиняємо програму, * виходячи* з циклу і досягаємо кінця програми.

The length of the input string can be found out using the built-in `len` function.

Довжину вхідного рядка можна дізнатися за допомогою вбудованої функції len.

Remember that the `break` statement can be used with the `for` loop as well.

Пам'ятайте, що оператор break також може використовуватися з циклом for.

**Swaroop's Poetic Python**
** Поетика Swaroop про Python**

The input I have used here is a mini poem I have written:

Вхід, який я використовував тут, - це міні-вірш, який я написав:

```
Programming is fun
When the work is done
if you wanna make your work also fun:
    use Python!
```

```
Програмування веселе
Коли роботу виконано
Якщо ти хочеш зробити свою роботу веселою:
    Використовук Python!
```


## The `continue` Statement {#continue-statement}

## Оператор 'continue' {#continue-statement}

The `continue` statement is used to tell Python to skip the rest of the statements in the current loop block and to *continue* to the next iteration of the loop.

Оператор `continue` використовується для вказівки Python пропустити інші оператори в поточному блоці циклу і* продовжити * до наступної ітерації циклу.

Example (save as `continue.py`):

Приклад (зберегти як `continue.py`):

<pre><code class="lang-python">{% include "./programs/continue.py" %}</code></pre>

```python
while True:
    s = input('Enter something : ')
    if s == 'quit':
        break
    if len(s) < 3:
        print('Too small')
        continue
    print('Input is of sufficient length')
    # Do other kinds of processing here...
```

Output:

Вихід:

<pre><code>{% include "./programs/continue.txt" %}</code></pre>

```python
$ python continue.py
Enter something : a
Too small
Enter something : 12
Too small
Enter something : abc
Input is of sufficient length
Enter something : quit
```

**How It Works**
** Як Це Працює**

In this program, we accept input from the user, but we process the input string only if it is at least 3 characters long. So, we use the built-in `len` function to get the length and if the length is less than 3, we skip the rest of the statements in the block by using the `continue` statement. Otherwise, the rest of the statements in the loop are executed, doing any kind of processing we want to do here.

У цій програмі ми приймаємо вхідні дані від користувача, але обробляємо вхідний рядок, тільки якщо він має довжину не менше 3 символів. Таким чином, ми використовуємо вбудовану функцію len для отримання довжини, і якщо довжина менше 3, ми пропускаємо інші оператори в блоці з допомогою оператора continue. В іншому випадку інші оператори в циклі виконуються, виконуючи будь-яку обробку, яку ми хочемо зробити тут.

Note that the `continue` statement works with the `for` loop as well.

Зверніть увагу, що оператор` continue `також працює з циклом` for'.


## Summary

## Резюме

We have seen how to use the three control flow statements - `if`, `while` and `for` along with their associated `break` and `continue` statements. These are some of the most commonly used parts of Python and hence, becoming comfortable with them is essential.

Ми бачили, як використовувати три оператори управління потоком - `if`, `while` І `for`, а також пов'язані з ними оператори `break` і `continue`. Ось деякі з найбільш часто використовуваних частин Python і, ознайомитися з ними є надзвичайно важливим.

Next, we will see how to create and use functions.

Далі ми побачимо, як створювати і використовувати функції.
