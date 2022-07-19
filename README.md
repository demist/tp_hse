![year][0] ![status][1] ![progress][2]

**1 модуль, 2022/2023 учебный год, ВШЭ ВШБ ДБИ**

## [Канал курса в telegram #tbd]()

## [Таблица с результатами по курсу #tbd]()

# Аннотация

*Курс про все, что связано с созданием ПО, кроме непосредственно написания программного кода*

Курс состоит из лекций и семинарских занятий.

Лекционный материал включает краткий обзор важных с точки зрения процесса разработки понятий: методы отладки и этапы исправления дефектов ПО, критерии хорошей и неудачной архитектуры, этапы проектирования и разработки, методологии разработки.
Семинарский материал состоит из рассказа о важных инструментах программиста: системы контроля версий, системы сборки, gdb, valgrind, развертывание и настройка систем непрерывной интеграции.

Цель курса — дать слушателям, которые параллельно изучают языки программирования, алгоритмы и т. п., информацию и дополнительные знания, какими инструментами можно пользоваться и на что обращать внимание при создании рыночного программного продукта.

# План лекций

## Лекция 0 

*Неделя 1*

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

> [TravisCI](https://www.travis-ci.com/)

> [TeamCity](https://www.jetbrains.com/teamcity/)

> [GitHub Actions](https://github.com/features/actions)

> [Jenkins](https://www.jenkins.io/)

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

*tbd*

##  Техническое задание №1 (ТЗ1)

Необходимо разработать bash-скрипт, который:
- рекурсивно обойдет директорию (т.е. папку и все вложенные подпапки любого уровня вложенности) (**4 балла**) (*можно воспользоваться подходящей командой, необязательно писать рекурсивный обход вручную*)
- скопирует все найденные файлы в отдельную папку (**2 балла**) (*обратите внимание - в папку нужно сохранить именно файлы, а не вложенные папки и т.п. Т.е. если у вас папка A, в ней файл 1.txt и подпапка В с файлом 2.txt, то после копирования должна быть просто папка с файлами 1.txt и 2.txt*)
- далее скрипт эту отдельную папку заархивирует (**1 балл**)

Скрипт принимает 3 параметра: директория для поиска файлов, имя папки для сохранения файлов, имя архива. 

Обратите внимание, во вложенных папках могут быть файлы с одинаковым именем. Например основная папка А, в ней файл readme.txt и папка B, внутри папки В - еще один файл readme.txt. Если вы не уделите этому внимание, то в архив попадет лишь один файл (который был скопирован последним), что некорректно. Так что придумайте, как эту ситуацию можно разрешить (**3 балла**)

Для сдачи задания отправьте файл со скриптом на электронную почту вашего семинариста. 

**Обязательно** укажите тему письма в формате "ТП_ТЗ1_ФАМИЛИЯ_ГРУППА" (например, *ТП_ТЗ1_ИВАНОВ_112*)

**:end: Дедлайн: 26/09/2021 23:59**

##  Техническое задание №2 (ТЗ2)

Давайте представим, что данный репозиторий на github'е по нашему курсу и канал по курсу в telegram - не репозиторий и канал вовсе, а некоторая програмная система.
И для этой системы вам необходимо: 
- Выделить акторов. (*Минимум 2 актора*)
- Выделить варианты использования. (*Минимум 5 вариантов использования*)
- Составить диаграмму вариантов использования
- Для сценария "Объявить студентам о новом техническом задании" составить диаграмму последовательности. *Диаграмма должна быть адекватна и позволять восстановить сценарий без дополнительных уточнений в стиле "ну тут понятно" / "голосом объясню". Минимум у вас должно получиться 5 отдельных действий. Учитывайте, что текст задания готовит лектор, согласует его с семинаристами, потом его публикует и делает об этом объявление*

> Составлять диаграммы можно в любом удобном для вас ПО или с помощью любого веб-сервиса. Мы предлагаем варианты: [draw.io](https://app.diagrams.net/), [Miro](https://miro.com/), [plantuml](https://plantuml.com/ru/)

Для сдачи задания отправьте два файла (диаграмма вариантов использования + диаграмма последовательности) в любом из форматов *pdf/jpeg/png* на электронную почту вашего семинариста.

**Обязательно** укажите тему письма в формате "ТП_ТЗ2_ФАМИЛИЯ_ГРУППА" (например, *ТП_ТЗ2_ПЕТРОВ_113*)

**:end: Дедлайн:  03/10/2021 23:59**

##  Техническое задание №3 (ТЗ3)

### Задание 
Реализуйте на Python простейшую программу, которая будет считывать из файла числа, а далее отдельными функциями искать среди этих чисел минимальное число, максимальное число, считать их общую сумму и произведение. 
Для этой программы подготовьте тесты:
- проверяющие корректность работы функций поиска минимума и максимума
- проверяющие корректность работы функций сложения и умножения
- проверяющие скорость работы программы при увеличении размера входного файла

### Пример работы
**В файле**: 1 4 2 3

**Минимальное**: 1

**Максимальное**: 4

**Сумма**: 10 *(1+2+3+4)*

**Произведение**: 24 *(1\*2\*3\*4)*

### Критерии оценки
**Для получения оценки "4"**: реализуйте функции чтения из файла, поиска минимального числа, поиска максимального числа, сложения и умножения *всех* чисел из файла

**Для получения оценки "6"**: реализуйте тесты для проверки корректности функций поиска минимума, максимума, сложения и умножения

**Для получения оценки "8"**: реализуйте тесты для проверки скорости работы программы при увеличении размера входного файла

**Для получения оценки "9"**: реализуйте любой другой тест на ваше усмотрение

**Для получения оценки "10"**: реализуйте программу так, чтобы не возникало аварийного завершения работы программы из-за ошибки переполнения (что может легко случиться, если чисел в файле много, и они все достаточно большие - произведение будет очень быстро расти). 

Для сдачи задания отправьте два файла (*program.py* и *tests.py*) на электронную почту вашего семинариста.

**Обязательно** укажите тему письма в формате "ТП_ТЗ3_ФАМИЛИЯ_ГРУППА" (например, *ТП_ТЗ3_ФЕДОРОВ_114*)

**:end: Дедлайн: 17/10/2021 23:59**

##  Письменный экзамен (ЭКЗ)

:end: **Пройдет онлайн 18 октября в 11:10 - 12:30**

**Ключевые моменты**:
- **Темы для экзамена**: все, что было на лекциях + основные команды *bash* (писать скрипты вас никто просить не будет) и *git*
- Экзамен онлайн на базе Google Forms
- На выполнение у вас целая пара (**1 час 20 минут**)
- 5 тестовых вопросов (максимум по 1 баллу за вопрос - итого 5 баллов)
- 13 вопросов со свободным ответов (баллы за разные вопросы разные, суммарно можно заработать 49 баллов за эти вопросы)
- Общий балл за контрольную: **54**
- В таблицу с расчетом оценки будет вноситься так: *ЭКЗ* = *Балл за контрольную* / 5.4
- Нормировок / усреднений / округлений и т.п. не будет
- Т.к. по итогу вопросов со свободным ответом много - нам предстоит проверить более 3000 ответов, поэтому **ожидаемый срок проверки: 22-23.10**
- Публиковать результаты будем порционно по группам. В стиле *вся группа проверена - опубликовали баллы группы*

# Правила оценивания

*Оценка* = Округление (0,25\*(*ТЗ1* + *ТЗ2* + *ТЗ3*)/3 + 0,25\**КР* + 0,5\**ЭКЗ*)

[0]:https://img.shields.io/badge/year-2021%2F2022-blue
[1]:https://img.shields.io/badge/status-ended-red
[2]:https://progress-bar.dev/100/
