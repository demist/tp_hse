![year][0] ![status][1] ![progress][2]

**1 модуль, 2022/2023 учебный год, ВШЭ ВШБ ДБИ**

## [Канал курса в telegram](https://t.me/tp_hse_2022)

## [Рабочая ведомость по курсу](https://docs.google.com/spreadsheets/d/1Uq64G57-YaH_k5zItIrmAuB3o0W-kDZ0NvCaGfApURk/edit?usp=sharing)

## [Перейти к плану](https://github.com/demist/tp_hse_2022#%D0%BF%D0%BE%D0%BD%D0%B5%D0%B4%D0%B5%D0%BB%D1%8C%D0%BD%D1%8B%D0%B9-%D0%BF%D0%BB%D0%B0%D0%BD)

# Аннотация

*Курс про все, что связано с созданием ПО, кроме непосредственно написания программного кода*

Курс состоит из лекций и семинарских занятий.

Лекционный материал включает краткий обзор важных с точки зрения процесса разработки понятий: методы отладки и этапы исправления дефектов ПО, критерии хорошей и неудачной архитектуры, этапы проектирования и разработки, методологии разработки.
Семинарский материал состоит из рассказа о важных инструментах программиста: системы контроля версий, системы сборки, gdb, valgrind, развертывание и настройка систем непрерывной интеграции.

Цель курса — дать слушателям, которые параллельно изучают языки программирования, алгоритмы и т. п., информацию и дополнительные знания, какими инструментами можно пользоваться и на что обращать внимание при создании рыночного программного продукта.

# Объявления

## Подготовка к Семинару №2

Для успешного выполнения практики на **Семинаре №2** вам понадобятся некоторые инструменты, для разных операционных систем на вашем ПК действия разные: 

- Если у вас *Windows*, варианты:
	- (`в.1`) Поставить себе **Linux** - наиболее удобный способ
		- Рекомендуем использовать дистрибутив *Ubuntu 22.04.1 LTS* (скачать можно [тут](https://ubuntu.com/download/desktop))
		- Вы можете либо поставить *Ubuntu* второй системой, либо же развернуть в виртуальной машине
			- [Одна из множества инструкций, как поставить второй системой](https://www.tecmint.com/install-ubuntu-alongside-with-windows-dual-boot/)
			- [Одна из множества инструкций, как развернуть в виртуальной машине](https://ubuntu.com/tutorials/how-to-run-ubuntu-desktop-on-a-virtual-machine-using-virtualbox#1-overview)
	- (`в.2`) Установить себе WSL (*Windows Subsystem for Linux*)
		- [Одна из инструкций, как это сделать](https://docs.microsoft.com/ru-ru/windows/wsl/install)
	- (`в.3`) Использовать online-консоль (*наименее приоритетный вариант, использовать только если другое не получилось*)
		- Например, [вот эту](https://www.onlinegdb.com/online_bash_shell)
		- Или [вот эту](https://replit.com/languages/bash)
		- Или [вот эту](https://rextester.com/l/bash_online_compiler)
	- Если вы остановились на `в.2` или `в.3`, то вам еще необходимо установить `Git`
		- Скачать его можно [тут](https://git-scm.com/download/win)
- Если у вас *MacOS* - у вас есть уже приложение [*Terminal*](https://ru.wikipedia.org/wiki/Terminal_(macOS))
	- *Очень желательно, кроме того*, установить `brew`
		- Инструкция [тут](https://brew.sh/)
			- Достаточно в *Terminal* вставить команду `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`
	- После установки `brew` - установить `Git`
		- Инструкция [тут](https://git-scm.com/download/mac)
			- Достаточно в *Terminal* вставить команду `brew install git`
- Если у вас *Linux* (любой дистрибутив) - у вас уже есть приложение *Терминал* / *Эмулятор терминала* / "что-то подобное" - точно есть во всех дистрибутивах, просто поищите
	- Нужно установить `Git`
		- Достаточно в *Терминале* набрать команду `sudo apt-get install git` (если выпадает ошибка - стоит погуглить, какой менеджер пакетов используется в вашем дистрибутиве)


# План лекций

## Лекция 0 

*Неделя 1*

**Организационное**

-  План курса
-  Правила оценивания
-  Информация о заданиях
-  Контрольные мероприятия

## Лекция 1

*Неделя 1*

**Этапы развития проекта**

-  Основные этапы жизненного цикла проектирования, реализации и внедрения ПО
-  Формирование требований
-  Разработка концепции
-  Техническое задание
-  Эскизный проект
    - Понятие о MVP и примеры MVP
-  Технический проект
-  Рабочая документация
-  Поставка / ввод в действие
-  Сопровождение 
-  Вывод из эксплуатации

> Почитать подробнее про MVP можно [тут](https://www.productplan.com/glossary/minimum-viable-product/), [тут](https://vc.ru/marketing/139040-sekret-uspeshnyh-startapov-minimum-viable-product-chto-eto-i-kak-ego-sozdayut), [тут](https://habr.com/ru/company/productstar/blog/508892/) и [тут](https://trends.rbc.ru/trends/innovation/60dc23419a7947caa5598064)

> [Хороший пост про "Техническое задание на разработку ПО"](https://habr.com/ru/post/328822/)

## Лекция 2

*Неделя 1*

**Базовые понятия о языках программирования**

-  Парадигмы программирования
	- Императивное программирование
		- Описание
		- Примеры
		- "Вложенные парадигмы"
			- Процедурное программирование
			- Структурное программирование
			- Аспектно-ориентированное программирование
			- Объектно-ориентированное программирование
			- Обобщенное программирование
	- Декларативное программирование
		- Пример-объяснение
		- "Вложенные парадигмы"
			- Логическое программирование 
			- Функциональное программирование
	- Общая схема парадигм
	- Метапрограммирование
	- Реализация парадигм в языках программирования
-  Компилируемые и интерпретируемые языка
	- Определения
	- Примеры
-  Типизация
	- Сильная / слабая типизация
	- Статическая / динамическая типизация
	- Явная / неявная типизация


## Лекция 3

*Неделя 2*

**Основные диаграммы UML**

-  Что такое UML? 
	- Базовое понятие о нотации UML
-  Диаграмма вариантов использования
	- Понятие о вариантах использования
	- Понятие об акторах
	- Нотация диаграммы вариантов использования
-  Диаграмма классов
	- Понятие о классах
	- Нотация диаграммы классов
	- Выделение сущностей
		- Карточки CRC
		- Метод Аббота
-  Диаграмма последовательности
	- Нотация диаграммы последовательности
-  Диаграмма состояний
	- Нотация диаграммы состояний
-  Диаграмма деятельности
	- Нотация диаграммы деятельности

> [UML Cheat Sheet](https://www.guru99.com/uml-cheatsheet-reference-guide.html)

## Лекция 4

*Неделя 2*

**CI/CD/CD**

-  CI/CD/CD
-  Понятие о Continuous Integration
-  Понятие о Continuous Delivery
-  Понятие о Continuous Deployment
-  Пример организации процесса разработка из индустрии
	- Этап проектирования
	- Этап реализации
	- Этап сдачи задачи
	- Подготовка к выпуску версии

> [TravisCI](https://www.travis-ci.com/), [TeamCity](https://www.jetbrains.com/teamcity/), [GitHub Actions](https://github.com/features/actions), [Jenkins](https://www.jenkins.io/)

## Лекция 5

*Неделя 3*

**Отладка ПО, ч.1: работа с ошибками ПО**

-  Основные этапы отладки ПО
-  Воспроизведение дефекта
	- Необходимая информация для воспроизведения
-  Анализ дефекта
	- Понятие root-cause
	- Условия возникновения
	- Область повреждения
	- Необходимые выводы
-  Дизайн исправления 
	- Технический
	- Архитектурный
	- Технологический
-  Исправление дефекта
-  Валидация исправления
-  Интеграция исправления в код или целевую систему
-  Дополнительные валидации после интеграции

## Лекция 6

*Неделя 3*

**Отладка ПО, ч.2: техники отладки**

-  Запуск программ в отладчике (трассировка)
	- Софтверный дебаггер
	- "Железный" дебаггер
	- Удаленный дебаггер
-  Логирование
	- Работы системы
	- Программного кода
-  Анализ программного кода без исполнения программы
	- "Метод пристального взгляда"
	- Статические анализаторы
-  Анализ поведения системы
	- Упрощение сценария
	- Ограничение объема данных
	- Упрощение данных / запроса
-  UNIT-тестирование
-  Прототипирование
-  Отладка с помощью дампов
-  Отладка с помощью перехватов
-  Профилирование кода
-  Выполнение кода в другой среде
-  Отладка методом RPC (*Remote procedure call*)
-  Отладка путем анализа документации
-  Отладка трансляцией кода 
	- Трансляция "вниз"
	- Трансляция "вверх"
-  Отладка разработкой интерпретатора
-  Метод индукции
-  Метод дедукции
-  Обратное движение по алгоритму

## Лекция 7

*Неделя 4*

**Управление качеством ПО, ч.1**

-  Понятие о качестве ПО
-  Характеристики и атрибуты качества ПО
-  Основые аспекты качества ПО
-  Парадокс тестировщика
-  Соответствие ожиданиям stakeholder'ов
-  Качество и деньги
	- Десятичное правило качества
	- Важные аспекты

## Лекция 8

*Неделя 4*

**Управление качеством ПО, ч.2**

-  Ручное тестирования
	- Класс эквивалентности
	- Граничные значения
-  7 ключевых инструментов качества
	- Причинно-следственная диаграмма Исикавы
	- Блок-схема
	- Контрольный листок
	- Контрольная карта (карта Шухарта)
		- Примеры
	- Гистограмма
	- Диаграмма Парето
	- Диаграмма разбрасывания
-  Ручное тестирование. Практические советы
-  Автоматизированное тестирование 
	- Основные аспекты
	- Жизненный цикл автотеста
	- Практические советы
	- Как на практике?

## Лекция 9

*Неделя 5*

**Принципы проектирования ПО, часть 1**

-  Что такое программа, как она устроена, как она работает (*вопросы к аудитории, если есть понимание - быстро двигаемся дальше*)
-  Что такое архитектура ПО
-  Что такое "Проектирование ПО"?
-  По каким критериям можно оценить архитектуру? 
	- Критерии хорошей архитектуры
		- Эффективность
		- Гибкость
		- Расширяемость
		- Масштабируемость, тестируемость, возможность повторного использования, сопровождаемость
	- Критерии неудачной архитектуры
		- Жесткость
		- Хрупкость
		- Неподвижность
-  Принцип *High Cohesion / Low Coupling*

> [Отличный ресурс про паттерны проектирования](https://refactoring.guru/ru/design-patterns/catalog)

## Лекция 10

*Неделя 5*

**Принципы проектирования ПО, часть 2**

-  Принципы SOLID
	- **S**ingle responsibility principle
	- **O**pen-closed principle
	- **L**iskov substitutional principle
	- **I**nterface segregation principle
	- **D**ependency inversion principle
-  Закон Деметры
-  YAGNI
-  DRY / DIE
-  KISS

> [Лекция Роберта *Uncle Bob* Мартина  про SOLID](https://www.youtube.com/watch?v=zHiWqnTWsn4)

## Лекция 11

*Неделя 6*

**Архитектурные паттерны**

-  Классификация архитектуры ПО
	- Локальные
	- Распределенные
		- Файл-серверные
		- Клиент-серверные
			- Двухзвенные
			- Трехзвенные
			- Многозвенные
-  Локальные приложения 
	- MVC (*Model-View-Controller*)
-  Клиент-серверная архитектура 
	- Тонкий и толстый клиент
	- Трехзвенная архитектура
-  Оценка нагрузки на систему
-  Тим проекта и влияние на нагрузку
-  Ресурсы для обеспечения производительности 
-  Масштабирование
	- Горизонтальное
	- Вертикальное
	- Функциональное разбиение
	- Шардинг
-  Типичная архитектура веб-сервиса
-  Типичная архитектура нагруженной информационной системы

## Лекция 12

*Неделя 6*

**Методологии разработки ПО**

-  Основные понятия
-  Факторы, оказывающие влияние на процесс разработки
	- Внешние факторы
	- Внутренние факторы
-  Каскадная модель
-  V-модель
-  Инкрементная модель
-  Итерационная модель
-  Спиральная модель
-  RAD-модель 
-  Семейство гибких методологий
	- Agile-манифест
	- Scrum
	- Kanban

> [Статья про методологии разработки](https://acodez.in/12-best-software-development-methodologies-pros-cons/)


# План семинаров 

##  Семинар 1 *(неделя 1)*

**Основы Python**

- понятие о python и интерпретаторе
- запускаем интерпретатор и считаем парочку арифметических выражений
- показываем переменные
- пишем скрипт на сложение чисел
- пишем скрипт "Hello world"
- показываем условные переходы и циклы
- пишем простую функцию расчета факториала

> [Хороший курс по Python](https://stepik.org/course/58852/promo)

> [Python First Steps](https://realpython.com/python-first-steps/)

> [Python for Beginners](https://www.python.org/about/gettingstarted/)

> [Еще разные туториалы](https://www.tutorialspoint.com/python/python_quick_guide.htm)

> [Консоль Python прямо на сайте](https://trinket.io/console)

> [Документация по Python](https://www.python.org/doc/)

##  Семинар 2 *(неделя 2)*

**Базовые инструменты разработки ПО**

Системы контроля версий, git, git-flow (*опционально*). 

Bash и основные команды.

**План семинара:** 
- показываем bash (*на лекции предупрежу, что надо иметь Linux / macOS или WSL*)
- базовые команды bash: touch, rm, cd, mkdir, rmdir, ls, cp, mv, cat, echo, ...
- пишем простой скрипт на bash (*Например, считаем количество файлов в директории*)
- рассказываем про системы контроля версий в целом (зачем нужно, какие есть)
- рассказываем основы git: что такое репозиторий, что такое ветки, что такое коммиты, pull-request'ы
- показываем: создание репозитория на github, клонирование локально, создание файла, коммит, push origin

> [bash commands cheatsheet](https://www.educative.io/blog/bash-shell-command-cheat-sheet)

> [bash script cheatsheet](https://devhints.io/bash)

##  Семинар 3 *(неделя 3)*

**Инструменты отладки**

*Показываем дебаггер в IDE, точки останова, как с этим работать*.
*(опционально) показываем gdb & valgrind*

**План семинара:**
- запускаем любимую IDE 
- пишем простую программу (лучше на питоне), запускаем дебагер
- показываем точки останова, шаг вперед / шаг с заходом / шаг с обходом
- показываем значения переменных
- *опционально* показываем профилировщик
- *опционально* показываем gdb - как работать из консоли (опять же, на простом примере)
- *опционально* показываем valgrind в простейших сценариях (память не освобождена, переменная не инициализирована, используется неинициализированная переменная в условном переходе)

##  Семинар 4 *(неделя 4)*

**Тестирование ПО**

*Отработка на семинаре простейших примеров написания тестов на python, демонстрация разных видов тестов*

**План семинара:**
- пишем на питоне пару простых функций (например, сложение и умножение чисел)
- показываем юнит-тесты (каждую функцию)
- показываем нагрузочное тестирование (запускаем много итераций теста, смотрим производительность)
- показываем сценарное тестирование (на уровне "посчитаем значения выражения")

##  Семинар 5 *(неделя 5)*

**Диаграммы UML**

*Отработка на семинаре навыков построения диаграмм, решение небольших задач. Диаграммы классов пока не рассматриваем.*

**План семинара:**
- решаем задачку на диаграмму вариантов использования (например, "варианты использования сайта аэропорта")
- решаем задачку на диаграмму последовательности (например, "снимаем деньги в банкомате")
- решаем задачку на диаграмму деятельности (например, "поступаем в университет")
- решаем задачку на диаграмму состояний ("рассматриваем сдачу курса: изучается-сдан-пересдача-не сдан")

##  Семинар 6 *(неделя 6)*

**Практика проектирования**

*Отрабатываем практические навыки проектирования (без погружения в программный код) понятных предметных задач: заказ такси через приложение, покупка в интернет-магазине...Рисуем диаграммы классов UML*

**План семинара:**
- решаем простую задачу на проектирование локального приложения (мобильного или десктопного), без взаимодействия с сервером. *Например, проектируем простейшее приложение для создания и хранения заметок. Жетально проектировать на уровне классов. Если идет сложно - сначала пытаемся выделить варианты использования и придумать, как их реализовать. Даже если получится по итогу криво, главное, чтобы получилось хоть что-то.*.
- решаем задачу посложнее на проектирование клиент-серверного приложения. *Например, приложение для заказа такси. Обязательно надо подстветить проблему, что запрос от клиента до сервера может не дойти (или от сервера до клиента), как это можно решать (спойлер - таймлимитом)*

# Контрольные мероприятия

##  Контрольная работа (КР)

:exclamation: **Контрольная работа пройдет на лекции 28 сентября, в формате онлайн.**

*Подробности будут опубликованы после лекций №5 и №6 (21.09)*

##  Техническое задание №1 (ТЗ1)

**Пишем простую программу на Python**

### Легенда задания 

Вам нужно написать простую программу на *Python*, которая поможет разобраться с вашей базой контактов. Графический интерфейс делать не нужно, достаточно просто консольной программы.

Контакты хранятся в виде текстового файла, в каждой строке которого - *ФИО* (первое слово - *фамилия*, второе при наличии - *имя*, третье при наличии - *отчество*), 
*номер телефона* (формата `+Х`, где *X* - от 9 до 11 цифр), *адрес электронной почты* (формата `X@Y.Z`, состоящий из букв латинского алфавита, знака `@` и точки).

Обратите внимание, что *ФИО* может быть неполное (например, только *ФИ*, или только *Фамилия*), *номер телефона* и/или *адрес электронной почты* может быть не заполнен.

*ФИО*, *номер телефона*, *адрес электронной почты* отделены друг от друга запятыми, если не заполнено - запятые все равно расставлены.

Пример файла с базой контактов:

`Иванов Иван Иванович, +79999999995, ivanov@ma.il`

`Петров Коля,, kolya@gmail.com`

`Вася, +79966969669,`

`Пушкин Александр Сергеевич,,`


### Требования и критерии оценки

За задание вы можете получить максимум **10 баллов**.

Семинарист при проверке может выставить за какой-либо пункт частичный балл, если требования пункта выполнены не полностью.

- `1 балл` Создан класс *Contact* с необходимыми полями
- `1 балл` Реализовано чтение базы контактов из файла (*имя файла вводится в консоль*) в коллекцию объектов типа *Contact*. Если *телефон* или *адрес электронной почты* не указан, нужно корректно это учесть в программе. *NB: прямо это на семинаре могли не показывать, но это действительно очень просто (не просто так это первые пункты задания). Если будут сложности - задайте вопросы на семинаре №3, объясним :)*
- `1 балл` Реализован поиск по *номеру телефона*
- `1 балл` Реализован поиск по *адресу электронной почты*
- `2 балла` Реализован поиск по *Фамилии*, *Имени*, *Отчеству* как в отдельности, так и вместе (т.е. можно искать *Иван*, а можно искать *Иван Иванов*, например)
- `2 балла` Реализован поиск и вывод на экран всех контактов, у которых не заполнен *номер телефона* и/или *адрес электронной почты*
- `2 балла` Реализована возможность редактирования любого контакта (*подумайте, как это сделать удобно*)

### Дедлайн

Есть два дедлайна - `мягкий` и `жесткий`. 

- Если вы присылаете ваше решение до `мягкого дедлайна` - то ваш семинарист проверяет работу, дает замечения, и далее у вас есть **3 дня** на то, чтобы внести исправления (и получить балл выше). 
Вы можете не вносить исправления и согласиться на тот балл, который получили по итогам первой проверки.
- Если вы присылаете ваше решение после `мягкого дедлайна`, но до `жесткого дедлайна` - семинарист проверяет вашу работу и выставляет балл. Исправления не допускаются.
- Если вы присылаете ваше решение после `жесткого дедлайна`, то задание не проверяется, и вы получаете **0 баллов**

#### Сроки 

**Вариант 1 - если у вас уже прошел семинар №2**

- `Мягкий дедлайн` **25.09**
- `Жесткий дедлайн` **02.10**

**Вариант 2 - если у вас еще не было семинара №2** 

- `Мягкий дедлайн` **дата семинара №2 + 1 неделя**
- `Жесткий дедлайн` **дата семинара №2 + 2 недели**

### Формат сдачи

Задание вы сдаете своему семинаристу. Результаты выполнения задания должны быть загружены в репозиторий на *GitHub*.
Канал отправки ссылки на репозиторий семинаристу - на усмотрение семинариста.


##  Техническое задание №2 (ТЗ2)

**Добавляем тесты и разворачиваем простейший CI/CD**

*tbd*

##  Техническое задание №3 (ТЗ3)

**Проектируем небольшое приложение по требованиям**

*tbd*

##  Письменный экзамен (ЭКЗ)

*tbd*

# Понедельный план

| Неделя | Лекции | Семинары | Выдача заданий | Сдача заданий | 
| :---: | :---: | :---: | :---: | :---: |
| :white_check_mark: 1 | [Организационное](https://github.com/demist/tp_hse_2022/blob/main/slides/intro.pdf) + [Этапы развития проекта](https://github.com/demist/tp_hse_2022/blob/main/slides/lec1.pdf) + [Базовые понятия о языках программирования](https://github.com/demist/tp_hse_2022/blob/main/slides/lec2.pdf) | Основы Python | *Установить необходимое ПО для курса на свои машины* | |
| :white_check_mark: 2 | [Основные диаграммы UML](https://github.com/demist/tp_hse_2022/blob/main/slides/lec3.pdf) + [CI/CD/CD](https://github.com/demist/tp_hse_2022/blob/main/slides/lec4.pdf) | Базовые инструменты разработки ПО | **ТЗ1**: Пишем простую программу на Python | |
| :fire: 3 | [Отладка ПО, ч.1: работа с ошибками ПО](https://github.com/demist/tp_hse_2022/blob/main/slides/lec5.pdf) + [Отладка ПО, ч.2: техники отладки](https://github.com/demist/tp_hse_2022/blob/main/slides/lec6.pdf) | Инструменты отладки | | |
| 4 | **КР** + [Управление качеством ПО, ч.1](https://github.com/demist/tp_hse_2022/blob/main/slides/lec7.pdf) + [Управление качеством ПО, ч.2](https://github.com/demist/tp_hse_2022/blob/main/slides/lec8.pdf) | Тестирование ПО | **ТЗ2**: Добавляем тесты и разворачиваем простейший CI/CD | **ТЗ1**: Пишем простую программу на Python |
| 5 | [Принципы проектирования ПО, часть 1](https://github.com/demist/tp_hse_2022/blob/main/slides/lec9.pdf) + [Принципы проектирования ПО, часть 2](https://github.com/demist/tp_hse_2022/blob/main/slides/lec10.pdf) | Диаграммы UML | **ТЗ3**: Проектируем небольшое приложение по требованиям | |
| 6 | [Архитектурные паттерны](https://github.com/demist/tp_hse_2022/blob/main/slides/lec11.pdf) + [Методологии разработки ПО](https://github.com/demist/tp_hse_2022/blob/main/slides/lec12.pdf) | Практика проектирования | | **ТЗ2**: Добавляем тесты и разворачиваем простейший CI/CD |
| 7 | **ЭКЗ** | | | **ТЗ3**: Проектируем небольшое приложение по требованиям |

# Правила оценивания

**Финальная оценка** = *Математическое округление* (0.2\*`КР` + 0.15\*`ТЗ1` + 0.15\*`ТЗ2` + 0.15\*`ТЗ3` + 0.35\*`ЭКЗ`)

[0]:https://img.shields.io/badge/year-2022%2F2023-yellow
[1]:https://img.shields.io/badge/status-ongoing-green
[2]:https://progress-bar.dev/33/
