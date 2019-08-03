# Оператори та вирази {#op-exp}

Більшість операторів (логічних рядків), які ви пишете, будуть містити _вирази_. Простий приклад виразу `2 + 3`. Вираз можна розділити на оператори і операнди.

_Оператори_-це функціональність, яка щось робить і може бути представлена символами, такими як `+` або спеціальними ключовими словами. Операторам потрібні деякі дані для роботи, і такі дані називаються _операндами_. У цьому випадку `2` і `3` операнди.

## Оператор

Ми коротко розглянемо оператори та їх застосування.

Зверніть увагу, що вирази в прикладах, можна обчислити за допомогою інтерпретатора в інтерактивному режимі. Наприклад, щоб перевірити вираз `2 + 3`, використовуйте інтерактивний інтерпретатора Python:

```python
>>> 2 + 3
5
>>> 3 * 5
15
>>>
```

Ось короткий огляд доступних операторів:


- `+` (плюс)
    - Додає два об'єкти
    - `3 + 5` дає `8`. `'a' + 'b'` дає `'ab'`.

- `-` (мінус)
    - Забезпечує віднімання одного числа з іншого; якщо перший операнд відсутній, він вважається рівним нулю.
    `-5.2` дає негативне число і `50-24` дає `26`.

- `*` (множачи)
    - Дає множення двох чисел або повертає рядок, повторену багато разів.
    - `2 * 3` дає `6`. `'la' * 3` дає `"lalala"`.

- `**` (степінь)
    - Повертає x до степені y
    - `3 ** 4` дає `81` (тобто `3 * 3 * 3 * 3`)

- `/` (ділення)
    - Розділяє x на y
    - `13 / 3` дає `4.333333333333333`

- '//'(розділити і заукруглити)
    - Розділити x на y і округлити відповідь до найближчого _мнешого_ цілого значення. Зверніть увагу, що якщо одне з значень є типу float, Ви отримаєте назад float.
    - `13 // 3` дає `4`
    - `-13 // 3` дає `-5`
    - `9//1.81` дає `4.0`

- `%` (ділення по модулю)
    - Повертає залишок від ділення
    - `13 % 3` дає `1`. `-25.5 % 2.25` дає `1.5`.

- '<<'(зсув вліво)
    - Зсуває біти числа вліво на вказану кількість біт. (Кожне число представлено в пам'яті бітами або двійковими цифрами, тобто 0 і 1)
    - `2 << 2` дає `8`. `2` представлено `10` в бітах.
    - Зсування вліво на 2 біта дає `1000`, що являє собою `8` у десятковій системі.

- `>>`(зсув вправо)
    - Зсуває біти числа вправо на вказану кількість розрядів.
    - `11 >> 1` дає `5`.
    - `11' представлений в бітах `1011`, зсув вправо на 1 біт дає `101`, що є десятковим '5'.

- `&` (побітове І (AND))
    - Побітове і двох чисел
    - `5 & 3` дасть `1`.

- `|` (побітове або)
    - Побітове або чисел
    - `5 | 3` дає `7`

- `^` (побітове виключає АБО)
    - Побітове XOR чисел
    - `5 ^ 3` дає `6`

- `~` (побітова інверсія)
    - Бітова інверсія x це -(x+1)
    - `~5` дає `-6`. Більш детальну інформацію по http://stackoverflow.com/a/11810203


- `<`(менш)
    - Повертає, чи x менше y. Всі оператори порівняння повертають значення True або False. Зверніть увагу на великі літери цих імен.
    `5 < 3` дає `False` a `3 < 5` `true`.
    - Порівняння можуть бути складними  `3 < 5 < 7` дає `true` .

- `>` (більше, ніж)
    - Повертає, чи x більше ніж y
    - `5 > 3` повертає `True`. Якщо обидва операнди є числами, вони спочатку перетворюються на загальний тип. В іншому випадку він завжди повертає False.

- `<=` (менше або дорівнює)
    - Повертає значення x менше або дорівнює y
    - х = 3; у = 6; повертає X <= р `True`

- `>=` (більше або дорівнює)
    - Повертає значення x більше або дорівнює y
    - х = 4; у = 3; повертає x >= 3 `True`

- `==` (дорівнює)
    - Порівнює,  qo об'єкти рівні
    - х = 2; У = 2; х == р повертає `True`
    - `x = 'str'; y = 'stR'; x == y` повертає `False`
    - `x = 'str'; y = 'str'; x == y` повертає `True`

- `!=` (не дорівнює)
    - Порівнює, чи об'єкти не рівні
    - 'x = 2; y = 3; x != y` повертає `True`

- `not` (логічне не)
    - Якщо Х дорівнює `true`, вона повертає `False`. Якщо X має значення `False`, то він повертає `True`.
    - `x = True; not x` повертає `False`.

- `and` (логічне і)
    - `x and y` повертає `False`, якщо X має значення false
    - `x = False; y = True; x and y` повертає `False`, так як x є False. У цьому випадку Python не буде оцінювати y, оскільки він знає, що ліва частина виразу `and` є `False`, що означає, що вираз `False` незалежно від інших значень. Це називається оцінкою короткого замикання.

- `or` (логічне або)
    - Якщо x або y `True` то певератється `True`
    - `x = True; y = False; x or y` повертає `True`. Оцінка короткого замикання застосовується і тут.

## Скорочення для математичної операції і призначення

Зазвичай виконується математична операція над змінною, а потім присвоюється результат операції назад змінної, тому для таких виразів існує скорочення:

```python
a = 2
a = a * 3
```

можна записати як:

```python
a = 2
a *= 3
```

Зауважимо, що `var = var операція вираз ` стає `var операція= вираз`.

## Порядок виконання

Яущо ви маєте такий вислів `2 + 3 * 4` - то що буде першим, спочатку додавання або множення? В нашій школі математика говорить нам, що множення повинно бути зроблено в першу чергу. Це означає, що оператор множення має більш високий пріоритет, ніж оператор додавання.

В наступній таблиці наведена таблиця пріоритетів для Python, від найнижчого пріоритету (найменша прив'язка) до найвищого пріоритету (велика прив'язка). Це означає, що в даному виразі Python спочатку оцінить оператори і вирази нижче в таблиці перед тими, які перераховані вище в таблиці.

Наступна таблиця, взята з [Python reference manual](http://docs.python.org/3/reference/expressions.html#operator-precedence), надається для повноти картини. Набагато краще використовувати круглі дужки для групування операторів і операндів відповідним чином, щоб явно вказати пріоритет. Це робить програму більш читаємою. Див. [зміна порядку оцінки](#changing-order-of-evaluation) нижче для отримання додаткової інформації.

- `lambda`: лямбда-вирази
- `if-else`: умовний вираз
- `or` : логічне або
- `and`: булево і
- `not x` : логічне не
- `in, not in, is, not, <, <=, >, >=, != , == `: Порівняння, включаючи тести членства та тести ідентифікації
- `|`: Побітове або
- `^`: Побітове XOR
- `&`: Побітове і
- ` << , >>`: Зрушення
- `+, -` : Додавання і віднімання
- `*, /, //, %` : Множення, ділення, ділення статі і залишок
- `+x, -x, ~x`: позитивний, негативний, побітовий не
- `**` : Зведення в ступінь
- `х[індекс], Х[Index:індекс], Х(аргументу...), х.атрибут`: підписка, нарізка, виклик, посилання на атрибут
- `(вираз....), [вираз...], {ключ:значення...}, {вираз...}`: Відображення прив'язки або кортежу, відображення списку, відображення словника, відображення набору

Оператори, з якими ми ще не стикалися, будуть пояснені в наступних главах.

Оператори з _таким самим пріоритетом_ перераховані в одному тому ж рядку в таблиці вище. Наприклад, `+` і `-` мають однаковий пріоритет.

## Зміна порядку виконання {#changing-order-of-evaluation}

Щоб зробити вирази більш читабельними, ми можемо використовувати круглі дужки. Наприклад, `2 + (3 * 4)` це, безумовно, легше зрозуміти, ніж `2 + 3 * 4` - що вимагає знання пріоритету оператора. Як і в усьому іншому, дужки повинні використовуватися розумно (не перестарайтеся) і не повинні бути надлишковими, як в`(2 + (3 * 4))`.

Є додаткова перевага використання дужок - це допомагає нам змінити порядок виконання дій. Наприклад, якщо ви хочете, щоб додавання обчислювалося перед множенням у виразі, то ви можете написати щось на зразок`(2 + 3) * 4`.

## Асоціативність

Оператори, як правило, асоціюються зліва направо. Це означає, що оператори з однаковим пріоритетом обчислюються зліва направо. Наприклад, `2 + 3 + 4` оцінюється як`(2 + 3) + 4`.

## Expressions
## Вирази?

Приклад (зберегти як `expression.py`):

```python
length = 5
breadth = 2

area = length * breadth
print('Area is', area)
print('Perimeter is', 2 * (length + breadth))
```
Вивід:

```
$ python expression.py
Area is 10
Perimeter is 14
```

** Як Це Працює**

Довжина і ширина прямокутника зберігаються в змінних. Ми використовуємо їх для обчислення площі і периметра прямокутника за допомогою виразів. Ми зберігаємо результат виразу `length * width` у змінній `area`, а потім друкуємо його за допомогою функції `print`. У другому випадку, ми безпосередньо використовувати значення вираження `2 * (length + breadth)` у функції `print`.

Крім того, зверніть увагу, як Python красиво друкує. Незважаючи на те, що ми не вказали пробір між `Area is` і змінної `area`, Python ставить його для нас, щоб ми отримали чистий приємний вивід, і програма була набагато більш читаємою таким чином (так як нам не потрібно турбуватися про інтервали в рядках, які ми використовуємо для виведення). Це приклад того, як Python полегшує життя програмісту.

## Резюме

Ми бачили, як використовувати оператори, операнди і вирази - це основні будівельні блоки програми. Далі ми побачимо, як використовувати їх в наших програмах за допомогою операторів.