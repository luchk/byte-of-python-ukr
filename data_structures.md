# Структури даних {#data-structures}

Структури даних в основному такі-це* структури*, які можуть містити деякі* дані * разом. Іншими словами, вони використовуються для зберігання колекції пов'язаних даних.

В Python є чотири вбудовані структури даних-_list, tuple dictionary і set_. Ми побачимо, як використовувати кожен з них і як вони полегшують нам життя.

## Список - List

Список-це структура даних, яка містить впорядкований набір елементів, тобто ви можете зберігати *послідовності* елементів у списку. Це легко уявити, якщо ви можете придумати список покупок, в якому у вас є список предметів для покупки, за винятком того, що у вас, ймовірно є; кожен елемент розшатовується в окремому рядку в списку для покупок, тоді як в Python ви ставите коми між ними.

Список елементів повинен бути поміщений в квадратні дужки, щоб Python зрозумів, що ви вказуєте список. Після створення списку можна додавати, видаляти або шукати елементи в списку. Оскільки ми можемо додавати і видаляти елементи, ми говоримо, що список-це *змінні* тип даних, тобто цей тип може бути змінений.

## Короткий Вступ До Об'єктів Та Класів

Хоча я  відкладав обговорення об'єктів та класів до цих пір, невелике пояснення необхідно прямо зараз, щоб ви могли краще зрозуміти списки. Ми детально розглянемо цю тему в [наступному розділі](./oop.md#oop)..

Список є прикладом використання об'єктів і класів. Коли ми використовуємо змінну `i` і присвоюємо їй значення, скажімо, ціле число `5`, Ви можете думати про це як про створення *об'єкта* (тобто примірника) `i` *класу* (тобто типу) `int`. Фактично, ви можете прочитати `help(int)`, щоб краще зрозуміти це.

Клас також може мати * методи*, тобто функції, визначені для використання тільки по відношенню до цього класу. Ці функціональні можливості можна використовувати тільки при наявності об'єкта цього класу. Наприклад, Python надає метод "append" для класу "list", який дозволяє додавати елемент в кінець списку. Наприклад, `mylist.append('an item')`   додасть цей рядок в список `mylist`. Зверніть увагу на використання точкової нотації (dotted notation ) для доступу до методів об'єкта.

Клас також може мати* поля*, які є не чим іншим, як змінними, визначеними для використання тільки щодо цього класу. Ви можете використовувати ці змінні/імена лише тоді, коли у вас є об'єкт цього класу. Поля також доступні за допомогою точкової нотації, наприклад, мій список.поле.`

Приклад (зберегти як `ds_using_list.py`):

<pre><code class="lang-python">{% include "./programs/ds_using_list.py" %}</code></pre>

Вивід:

<pre><code>{% include "./programs/ds_using_list.txt" %}</code></pre>

**Як це працює**

Змінна `shoplist` є списоком покупок для тих, хто збирається на ринок. У `списку покупок` ми зберігаємо тільки рядки імен товарів, які потрібно купити, але ви можете додати _ будь який тип обєктів_ в список, включаючи номери і навіть інші списки.

Ми також використовували цикл `for..in ' для перебору елементів списку. До цього часу ви, мабуть, зрозуміли, що список-це також послідовність. Спеціальність послідовностей буде обговорюватися в [більш пізньому розділі](#sequence).

Зверніть увагу на параметр `end` у виклику функції `print`, який використовується щоб вказати, що ми хочемо закінчити рядок прогалиною замість звичайного розриву рядка.

Потім ми додаємо елемент до списку за допомогою методу `append` об'єкта `list`, як вже обговорювалося раніше. Потім ми перевіряємо, що елемент дійсно доданий в список, друкуючи вміст списку, просто передаючи список функції `print` , яка акуратно друкує його.

Потім ми сортуємо список за допомогою методу `sort`. Важливо розуміти, що цей метод впливає на сам список, а не повертає змінений список - це відрізняється від того, як працюють рядки. Ось що ми маємо на увазі, кажучи, що списки _змінні_ і що рядки _незмінні_.

Потім, коли ми закінчимо купувати товар на ринку, ми хочемо видалити його зі списку. Ми досягаємо цього за допомогою оператора `del`. Тут ми згадуємо, який елемент списку ми хочемо видалити, і оператор `del` видаляє його зі списку для нас.  Ми вказуємо, що ми хочемо видалити перший елемент зі списку, і тому ми використовуємо `del shoplist[0]` (пам'ятайте, що Python починає відлік від 0).

Якщо ви хочете знати всі методи, визначені об'єктом list, див. `help(list)` для отримання додаткової інформації.


## Кортеж

Кортежі використовуються для зберігання декількох об'єктів. Думайте про них як про схожі на списки, але без великої функціональності, яку дає вам клас list. Однією з основних особливостей кортежів є те, що вони *незмінні* як рядки, тобто ви не можете змінювати кортежі.

Кортежі визначаються шляхом вказівки елементів, розділених комами в необов'язковій парі дужок.

Кортежі зазвичай використовуються в тих випадках, коли оператор або користувацька функція можуть з упевненістю припустити, що колекція значень (тобто Використовується кортеж значень) не зміниться.

Приклад (зберегти як `ds_using_tuple.py`):

<pre><code class="lang-python">{% include "./programs/ds_using_tuple.py" %}</code></pre>

Вивід:

<pre><code>{% include "./programs/ds_using_tuple.txt" %}</code></pre>

**Як це працює**

Змінна `zoo`  відноситься до кортежу елементів. Ми бачимо, що функція `len` може бути використаний для отримання довжини кортежу. Це також вказує на те, що кортеж також є і  [послідовністю](#sequence).

Зараз ми переводимо цих тварин в новий зоопарк, так як старий зоопарк закривається. Тому кортеж `new_zoo` містить деяких тварин, які вже знаходяться там разом з тваринами, привезеними з старого зоопарку. Повертаючись до реальності, зверніть увагу, що кортеж всередині кортежу не втрачає своєї ідентичності.

Ми можемо отримати доступ до елементів кортежу, вказавши позицію елемента в квадратних дужках, як і для списків. Це називається оператором _indexing_. Ми отримуємо доступ до третього елемента `new_zoo`, вказавши `new_zoo[2]`, і ми отримуємо доступ до третього елементу в третьому елементі кортежу `new_zoo`, вказавши ` new_zoo[2][2]`. Це дуже просто, як тільки ви зрозуміли ідіому.

> **Кортеж з 0 або 1 елементів**
> 
 Порожній кортеж створюється порожньою парою дужок, таких як `myempty = ()`. Однак кортеж з одним елементом не такий простий. Ви повинні вказати його з допомогою коми після першого (і тільки) елемента, щоб Python міг розрізняти кортеж і пару дужок, що оточують об'єкт у виразі, тобто ви повинні вказати ` singleton = (2,)`, Якщо ви хочете, щоб кортеж містив елемент `2`.

<!-- -->

> * * Примітка для програмістів Perl**
> 
> Список у списку не втрачає своєї ідентичності, тобто списки не згладжуються, як в Perl. Те ж саме стосується кортежу всередині кортежу, або кортежу всередині списку, або списку всередині кортежу і т. д. що стосується Python, вони просто об'єкти, що зберігаються з використанням іншого об'єкта, ось і все.

## Словник

Словник схожий на адресну книгу, де ви можете знайти адресу або контактну інформацію людину, знаючи тільки його ім'я, тобто ми пов'язуємо *ключі* (імена) з *значеннями* (деталями). Зверніть увагу, що ключ повинен бути унікальним так само, як ви не можете дізнатися правильну інформацію, якщо у вас є дві людини з однаковим ім'ям.

Зверніть увагу, що ви можете використовувати тільки незмінні об'єкти (наприклад, рядки) для ключів словника, але ви можете використовувати фіксовані чи змінювані об'єкти для значень словника.  Це в основному означає, що ви повинні використовувати тільки прості об'єкти для ключів.

Пари ключів і значень задаються в словнику за допомогою позначення ` d = {ключ1: значення1, ключ2: значення2, ключ3: значення3 }`. Зверніть увагу, що пари ключ-значення розділені двокрапкою, а самі пари розділені комами, і все це укладена в пару фігурних дужок`{}`.;

Пам'ятайте, що пари ключ-значення в словнику жодним чином не впорядковані. Якщо ви хочете конкретний порядок, то вам доведеться сортувати їх самостійно, перш ніж використовувати їх.

Словники, які ви будете використовувати, є екземплярами / об'єктами класу 'dict'.

Приклад (зберегти як `ds_using_dict.py`):

<pre><code class="lang-python">{% include "./programs/ds_using_dict.py" %}</code></pre>

Вивід:

<pre><code>{% include "./programs/ds_using_dict.txt" %}</code></pre>

** Як Це Працює**

Ми створюємо словник 'ab', використовуючи вже обговорену нотацію. Потім ми отримуємо доступ до пар ключ-значення, вказуючи ключ з допомогою оператора індексування, як описано в контексті списків і кортежів. Дотримуйтесь простий синтаксис.

Ми можемо видалити пари ключ-значення за допомогою нашого старого друга - оператора `del`. Ми просто вказуємо словник і оператор індексації для ключа, який буде видалений, і передаємо його оператору `del`. Немає необхідності знати значення, відповідне ключу для цієї операції.

Потім ми звертаємося до кожної пари ключ-значення словника, використовуючи метод `items` словника, який повертає список кортежів, де кожен кортеж містить пару елементів - ключ, за яким йде значення. Ми отримуємо цю пару і присвоюємо її змінним `name` і `address` відповідно для кожної пари, використовуючи цикл `for..in`, а потім друкуємо ці значення в блоці `for`.

Ми можемо додати нові пари ключ - значення, просто використовуючи оператор індексації для доступу до ключа і присвоєння цього значення, як ми зробили для Guido у наведеному вище випадку.

Ми можемо перевірити, чи існує пара ключ-значення за допомогою `in` оператора.

Список методів класу `dict` див. у розділі `help (dict)`.

> **Аргументи ключових слів і словники**
> 
> Якщо ви використовували аргументи ключових слів у своїх функціях, ви вже використовували словники! Просто подумайте про це - пари ключ-значення вказується вами у списку параметрів визначення функції, і коли ви звертаєтеся до змінних усередині своєї функції, це просто доступ до ключа словника (який називається _symbol table_ в термінології проектування компілятора).

## Послідовність

Списки, кортежі і рядки є прикладами послідовностей, але що таке послідовності і що в них такого особливого?

Основними функціями є *тести членства* (тобто вирази `in` і `not in`) і * операції індексування*, які дозволяють нам безпосередньо витягувати конкретний елемент в послідовності.

Три типи послідовностей, згаданих вище - списки, кортежі і рядки, також мають операцію *розрізання*, яка дозволяє нам отримати фрагмент послідовності, тобто частину послідовності.

Приклад (зберегти як `ds_seq.py`):

<pre><code class="lang-python">{% include "./programs/ds_seq.py" %}</code></pre>

Вивід:

<pre><code>{% include "./programs/ds_seq.txt" %}</code></pre>

** Як Це Працює**

По-перше, ми бачимо, як використовувати індекси для отримання окремих елементів послідовності. Це також називається _subscription operation_(_операції по підписці _). Всякий раз, коли ви вказуєте число в послідовності у квадратних дужках, як показано вище, Python отримає вам елемент, відповідний цій позиції в послідовності. Пам'ятайте, що Python починає відлік чисел від 0. Отже ` shoplist[0]` вибирає перший елемент , `shoplist[3]` вибирає четвертий пункт в  послідовності `shoplist`.

Індекс також може бути негативним числом, в цьому випадку, позиція відраховується від кінця послідовності. Тому `shoplist[-1]` відноситься до останнього елементу в послідовності, а `shoplist[-2]` вибирає другий останній (передостаній) елемент в послідовності.

Операція нарізки (`_slicing operation_`) використовується шляхом вказівки імені послідовності, за якою слідує необов'язкова пара чисел, розділених двокрапкою в квадратних дужках. Зверніть увагу, що це дуже схоже на операцію індексування, яку ви використовували до сих пір. Пам'ятайте, що числа необов'язковими, але двокрапка - ні (але двокрапка обовязковою).

Перше число (перед двокрапкою) в операції зрізу відноситься до позиції, з якої починається зріз, а друге число (після двокрапки) вказує, де зріз зупиниться. Якщо перше число не вказано, Python запуститься на початку послідовності. Якщо друге число опущено, Python зупиниться в кінці послідовності. Зверніть увагу, що зріз повертає _starts_ в початкову позицію і закінчується безпосередньо перед позицією _end_, тобто початкова позиція включена, але кінцева позиція виключена зі зрізу послідовності.

Таким чином,`shoplist[1:3]` повертає фрагмент послідовності, що починається з позиції 1, включає в себе позицію 2, але зупиняється в позиції 3, і тому повертається *фрагмент* двох елементів.  Аналогічно, `shoplist[:]` повертає копію всієї послідовності.

Ви також можете зробити нарізку з негативними позиціями. Негативні числа використовуються для позицій з кінця послідовності. Наприклад, `shoplist [: -1]` поверне фрагмент послідовності, що виключає останній елемент послідовності, але містить все інше.

Ви також можете надати третій аргумент для зрізу, який є _кроком_ для зрізу (за замовчуванням розмір кроку дорівнює 1):

```python
>>> shoplist = ['apple', 'mango', 'carrot', 'banana']
>>> shoplist[::1]
['apple', 'mango', 'carrot', 'banana']
>>> shoplist[::2]
['apple', 'carrot']
>>> shoplist[::3]
['apple', 'banana']
>>> shoplist[::-1]
['banana', 'carrot', 'mango', 'apple']
```

Зверніть увагу, що коли крок дорівнює 2, ми отримуємо елементи з позиції 0, 2,... Коли розмір кроку 3, ми отримуємо деталі з положенням 0, 3, і так далі.

Спробуйте різні комбінації таких специфікацій зрізу, використовуючи інтерпретатор Python в інтерактивному режимі щоб ви могли відразу побачити результати. Саме чудове в послідовностях те, що ви можете отримати доступ до кортежів, списків і рядків однаково!

## Набір

Набори - це _невпорядкованих_ колекції простих об'єктів. Вони використовуються, коли існування об'єкта в колекції більш важливо, ніж порядок, або скільки раз це відбувається.

За допомогою наборів можна перевірити, чи є він підмножиною іншого набору, знайти перетин між двома наборами і т. д.

```python
>>> bri = set(['brazil', 'russia', 'india'])
>>> 'india' in bri
True
>>> 'usa' in bri
False
>>> bric = bri.copy()
>>> bric.add('china')
>>> bric.issuperset(bri)
True
>>> bri.remove('russia')
>>> bri & bric # OR bri.intersection(bric)
{'brazil', 'india'}
```
** Як Це Працює**

Якщо ви пам'ятаєте базову математику теорії множин зі школи, то цей приклад досить очевидинй.  Але якщо ні, ви можете "прогуглити" : "теорія множин" і "діаграма Венна", щоб краще зрозуміти наше використання наборів в Python.

## Відносини

Коли ви створюєте об'єкт і призначаєте його змінній, змінна тільки _відноситься_ (_refers_) до об'єкта і не представляє сам об'єкт!  Тобто ім'я змінної вказує на ту частину пам'яті комп'ютера, де зберігається об'єкт. Це називається *прив'язка* імені до об'єкта.


Як правило, вам не потрібно турбуватися про це, але є тонкий ефект посилання, які вам потрібно знати:

Приклад (зберегти як `ds_reference.py`):

<pre><code class="lang-python">{% include "./programs/ds_reference.py" %}</code></pre>

Вивід:

<pre><code>{% include "./programs/ds_reference.txt" %}</code></pre>
** Як Це Працює**

Велика частина пояснень доступна в коментарях.

Пам'ятайте, що якщо ви хочете зробити копію списку або таких послідовностей або складних об'єктів (а не простих _обєктів_, таких як цілі числа), то ви повинні використовувати операцію зрізу, щоб зробити копію. Якщо ви просто призначите ім'я змінної іншому імені, обидва вони будуть `посилатися` на той самий об'єкт, і це може бути проблемою, якщо ви не будете обережні.

> ** Примітка для програмістів Perl**
> 
> Пам'ятайте,що оператор присвоювання для списків не створює копію. Ви повинні використовувати операцію нарізки, щоб зробити копію послідовності.

## Детальніше про Strings {#more-strings}

Ми вже детально обговорювали рядки раніше. Що ще може там бути, щоб знати?  Ну, чи знаєте ви, що рядки також є об'єктами і мають методи, які роблять все від перевірки частини рядка до видалення пробілів?  Фактично, Ви вже використовували строковий метод... метод `format`!

Рядки, що використовуються в програмах, є об'єктами класу `str`.  Деякі корисні методи цього класу продемонстровані в наступному прикладі. Повний список таких методів див. У розділі `help(str)`.

Приклад (зберегти як `ds_str_methods.py`):

<pre><code class="lang-python">{% include "./programs/ds_str_methods.py" %}</code></pre>

Вихід:

<pre><code>{% include "./programs/ds_str_methods.txt" %}</code></pre>

** Як Це Працює**

Тут ми бачимо багато рядкових методів у дії. Метод `startswith` використовується, щоб дізнатися, чи починається рядок з даного рядка. Оператор `in` використовується для перевірки, чи є цей рядок частиною рядка.

Метод `find` використовується для визначення положення даного підрядка в рядку; `find` повертає -1, якщо не вдається знайти підрядок. Клас `str` також має метод `join`, який склеює послідовність у рядок з акащаним розділювачем.

## Резюме

Ми детально вивчили різні вбудовані структури даних Python. Ці структури даних будуть необхідні для написання програм розумного розміру.

Тепер, коли у нас є хороша основа Python, ми побачимо, як проектувати і писати реальну програму Python.