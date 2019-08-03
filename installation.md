# Установка {#installation}

Коли ми посилаємося на "Python3" в цій книзі, ми будемо посилатися на будь-яку версію Python, рівну або більшу, ніж версія [Python {{ book.pythonVersion }}](https://www.python.org/downloads/).

## Установка на Windows

Відвідайте  https://www.python.org/downloads / і завантажити останню версію. На момент написання цієї статті, це був Python 3.5.1 
Установка Python на Windows є точнісінько такою самою, як і установка будь-якого іншого програмного забезпечення для Windows.

Зверніть увагу, що якщо ваша версія Windows є нижчою за Vista, Ви повинні [завантажити тільки Python 3.4] (https://www.python.org/downloads/windows/) оскільки пізніші версії вимагають нових версій Windows.

УВАГА: переконайтеся, що ви поставили прапорець `додати Python 3.5 в шлях` (`Add Python 3.5 to PATH`).

Щоб змінити місце установки, натисніть `налаштувати установку` (`Customize installation`), потім `далі` (`Next`) і введіть `C:\python35` (або інше підходяще місце) в якості місця установки.

Якщо ви раніше не перешлядали опцію `Додати шлях Python 3.5` (`Add Python 3.5 PATH`), встановіть прапорець `додати Python до змінних середовища` (`Add Python to environment variables`). Це робить те ж саме, що `додати Python 3.5 в шлях` (`Add Python 3.5 to PATH`) на першому екрані установки.

Ви можете встановити Launcher для всіх користувачів чи ні, це не має великого значення. Launcher використовується для перемикання між різними версіями встановленого Python.

Якщо ваш шлях був встановлений неправильно (шляхом перевірки параметрів `додати шлях Python 3.5` або `додати Python до змінних середовища`), виконайте дії в наступному розділі ("командний рядок DOS" ("DOS Prompt")), щоб виправити це. В іншому випадку перейдіть до розділу "запуск Python prompt на Windows" (`Running Python prompt on Windows`) у цьому документі.

Примітка: для людей, які вже знають програмування, якщо Ви знайомі з Docker, перевірте [Python в Docker](https://hub.docker.com/_/python/) і [Docker на Windows] (https://docs.docker.com/windows/).

### DOS Prompt {#dos-prompt}

Якщо ви хочете мати можливість використовувати Python з командного рядка Windows, тобто в командному рядку DOS, то вам потрібно встановити змінну PATH відповідним чином.

Для Windows 2000, XP, 2003 натисніть `панель управління` (`Control Panel`) - > `Система` (`System`) - > `розширені` (`Advanced`) - > `змінні середовища` (`Environment Variables`). Натисніть на змінну з ім'ям `PATH` в розділі _system Variables_, потім виберіть `Edit` і додайте `;C:\Python35` (будь ласка, переконайтеся, що ця папка існує, вона буде відрізнятися для нових версій Python). Звичайно, використовуйте відповідне ім'я каталогу.

<!-- The directory should match pythonVersion variable in book.json -->

Для більш старих версій Windows відкрийте файл `C:\AUTOEXEC.BAT` і додайте рядок `PATH= %PATH%;C:\Python35` - і перезавантажте систему. Для Windows NT використовуйте  `AUTOEXEC.NT` файл.


Для Windows Vista:

- Натисніть кнопку Пуск і виберіть `Панель управління` (`Control Panel`)
- Натисніть система (System), праворуч ви побачите `перегляд основної інформації про вашому комп'ютері` ("View basic information about your computer")
- Зліва список завдань, остання з яких - `розширені налаштування системи` (`Advanced system settings`). Натисніть.
- Відображається вкладка `Додатково` (`Advanced`) діалогового вікна `Властивості системи` (`Advanced`) . Натисніть кнопку `змінні середовища` (`Environment Variables`) в правому нижньому кутку.
- У нижньому полі під назвою `системні змінні` (`System Variables`) прокрутіть вниз до шляху і натисніть кнопку `Змінити` (`Edit`).
- Змініть свій шлях, як потрібно.
- Перезавантажте систему. 

Для Windows 7 і 8:

- Клацніть правою кнопкою миші на комп'ютері з робочого столу і виберіть `Властивості` (`Properties`) або натисніть кнопку `Пуск` (`Start`) і виберіть `Панель управління` (`Control Panel`) - > `Система і безпека` (`System and Security`) - > `Система` (`System`). Натисніть на `додаткові параметри системи` (`Advanced system settings`) зліва, а потім натисніть на вкладку `Додатково`(`Advanced`). Внизу натисніть `Змінні середовища` (`System Variables`) і в розділі `системні змінні` (`System Variables`) знайдіть змінну `PATH`, і натисніть `Змінити` (`Edit`).
- Перейдіть в кінець рядка під змінним значенням і додайте `;C:\Python35`(будь ласка, переконайтеся, що ця папка існує, вона буде відрізнятися для нових версій Python) до кінця того, що вже є. Звичайно, використовуйте відповідне ім'я папки.
- Якщо значення `%SystemRoot%\system32;` він тепер стане `%SystemRoot%\system32;C:\Python36` <!-- Каталог повинен відповідати змінній версії python в книзі.формат JSON>-- 
- Натисніть кнопку `ОК`, і ви  завершили. Перезапуск не потрібнн, однак може знадобитися закрити і знову відкрити командний рядок.

Для Windows 10:

`Стартовк меню Windows` (`Windows Start Menu`) > `Налаштування` (`Settings`) > `Про програму` (`About`) > `інформація про систему` (`System info`) (це все справа) > `додаткові параметри системи` (`Advanced System Settings`) > `Змінні середовища` (`Environment Variables`) (це внизу) > (потім виберіть змінну `Path` і натисніть `Змінити` (`Edit`)) > `створити` (`New`) > (введіть незалежно від вашого місця розташування python.  Наприклад, `\C:\Python35`)

### Запуск запрошення Python в Windows

Для користувачів Windows, ви можете запустити інтерпретатор командного рядка, якщо у вас є [змінна `PATH` встановлена відповідним чином](#dos-prompt).

Щоб відкрити термінал у Windows, натисніть кнопку Пуск і натисніть кнопку `Виконати` (`Run`). У діалоговому вікні введіть `cmd` і натисніть клавішу `[enter]`.

Потім введіть `python` і переконайтеся, що немає помилок.

## Установка на Mac OS X

Користувачі Mac OS X використовуйте [Homebrew](http://brew.sh) для встановлення Python, введіть у терміналі: `brew install python3`.

Щоб перевірити, відкрийте термінал, натиснувши клавіші `[Command + Space]`(щоб відкрити Spotlight search), введіть `terminal` і натисніть клавішу `[enter]`. Тепер запустіть python3 і переконайтеся, що помилок немає.

## Установка на GNU / Linux

Користувачів GNU/Linux використовуйте менеджер пакетів вашого дистрибутива для встановлення Python 3, наприклад, на Debian і Ubuntu: `sudo apt-get update && sudo apt-get install python3`.

Для перевірки відкрийте термінал, відкривши додаток "термінал" або натиснувши "Alt + F2" і ввівши "gnome-terminal". Якщо це не працює, зверніться до документації вашого конкретного дистрибутива GNU / Linux. Тепер запустіть python3 і переконайтеся, що помилок немає.

Ви можете побачити версію Python на екрані, запустивши:

<!-- The output should match pythonVersion variable in book.json -->
```
$ python3 -V
Python 3.6.0
```

Примітка: `$` - це запрошення оболонки. Він буде відрізнятися для вас в залежності від налаштувань операційної системи на вашому комп'ютері, тому я квазуватиму привітання системи тільки як символом `$`.

Увага: вихідні дані можуть відрізнятися на вашому комп'ютері, залежно від версії програмного забезпечення Python, встановленого на вашому комп'ютері.

## Резюме

Відтепер ми будемо вважати, що у Вас встановлений Python у вашій системі.

Далі, ми напишемо нашу першу програму на Python.