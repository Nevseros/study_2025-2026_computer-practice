---
## Front matter
title: "Отчёт по лабораторной работе №2"
subtitle: "Компьютерный практикум по статистическому анализу данных"
author: "Канева Екатерина, НФИбд-02-22"

## Generic otions
lang: ru-RU
toc-title: "Содержание"

## Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

## Pdf output format
toc: true # Table of contents
toc-depth: 2
lof: true # List of figures
lot: true # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4
documentclass: scrreprt
## I18n polyglossia
polyglossia-lang:
  name: russian
  options:
  - spelling=modern
  - babelshorthands=true
polyglossia-otherlangs:
  name: english
## I18n babel
babel-lang: russian
babel-otherlangs: english
## Fonts
mainfont: IBM Plex Serif
romanfont: IBM Plex Serif
sansfont: IBM Plex Sans
monofont: IBM Plex Mono
mathfont: STIX Two Math
mainfontoptions: Ligatures=Common,Ligatures=TeX,Scale=0.94
romanfontoptions: Ligatures=Common,Ligatures=TeX,Scale=0.94
sansfontoptions: Ligatures=Common,Ligatures=TeX,Scale=MatchLowercase,Scale=0.94
monofontoptions: Scale=MatchLowercase,Scale=0.94,FakeStretch=0.9
mathfontoptions:
## Biblatex
biblatex: true
biblio-style: "gost-numeric"
biblatexoptions:
  - parentracker=true
  - backend=biber
  - hyperref=auto
  - language=auto
  - autolang=other*
  - citestyle=gost-numeric
## Pandoc-crossref LaTeX customization
figureTitle: "Рис."
tableTitle: "Таблица"
listingTitle: "Листинг"
lofTitle: "Список иллюстраций"
lotTitle: "Список таблиц"
lolTitle: "Листинги"
## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Основная цель работы — изучить несколько структур данных, реализованных в Julia, научиться применять их и операции над ними для решения задач

# Задание

* Используя Jupyter Lab, повторить примеры.
* Выполнить задания для самостоятельной работы.

# Теоретическая часть

Julia - высокоуровневый свободный язык программирования с динамической типизацией, созданный для математических вычислений. Эффективен также и для написания программ общего назначения. Синтаксис языка схож с синтаксисом других математических языков, однако имеет некоторые существенные отличия.

Для выполнения заданий была использована официальная документация Julia.

Рассмотрим несколько структур данных, реализованных в Julia. Несколько функций (методов), общих для всех структур данных:

- isempty() — проверяет, пуста ли структура данных,
- length() — возвращает длину структуры данных,
- in() — проверяет принадлежность элемента к структуре,
- unique() — возвращает коллекцию уникальных элементов структуры,
- reduce() — свёртывает структуру данных в соответствии с заданным бинарным оператором,
- maximum() (или minimum()) — возвращает наибольший (или наименьший) результат вызова функции для каждого элемента структуры данных.

# Выполнение лабораторной работы

Сначала я выполнила примеры с кортежами (рис. [-@fig:1]):

![Примеры с кортежами.](image/1.png){#fig:1 width=70%}

Потом я выполнила примеры со словарями (рис. [-@fig:2]):

![Примеры со словарями.](image/2.png){#fig:2 width=70%}

Потом я выполнила примеры со множествами (рис. [-@fig:3]):

![Примеры со множествами.](image/3.png){#fig:3 width=70%}

Потом я выполнила примеры с массивами (рис. [-@fig:4]-[-@fig:9]):

![Примеры с массивами 1.](image/4.png){#fig:4 width=70%}

![Примеры с массивами 2.](image/5.png){#fig:5 width=70%}

![Примеры с массивами 3.](image/6.png){#fig:6 width=70%}

![Примеры с массивами 4.](image/7.png){#fig:7 width=70%}

![Примеры с массивами 5.](image/8.png){#fig:8 width=70%}

![Примеры с массивами 6.](image/9.png){#fig:9 width=70%}

Далее я приступила к выполнению заданий для самостоятельной работы.

1. Даны множества: $A = {0, 3, 4, 9}, B = {1, 3, 4, 7}, C = {0, 1, 2, 4, 7, 8, 9}$. Найдём $P = A \cap B \cup A \cap B \cup A \cap C \cup B \cap C$ (рис. [-@fig:10]):

![Задание 1.](image/10.png){#fig:10 width=70%}

2. Приведём примеры с выполнением операций над множествами элементов разных типов (рис. [-@fig:11]):

![Задание 2.](image/11.png){#fig:11 width=70%}

3. Создадим массивы разными способами (рис. [-@fig:12]-[-@fig:17]):

![Задание 3 (1-8).](image/12.png){#fig:12 width=70%}

![Задание 3 (9-13).](image/13.png){#fig:13 width=70%}

![Задание 3 (14.1-2).](image/14.png){#fig:14 width=70%}

![Задание 3 (14.3-5).](image/15.png){#fig:15 width=70%}

![Задание 3 (14.6-8).](image/16.png){#fig:16 width=70%}

![Задание 3 (14.9-13).](image/17.png){#fig:17 width=70%}

4. Создадим массив squares, в котором будут храниться квадраты всех целых чисел от 1 до 100 (рис. [-@fig:18]).

![Задание 4](image/18.png){#fig:18 width=70%}

5. Подключим пакет Primes (функции для вычисления простых чисел). Сгенерируем массив myprimes, в котором будут храниться первые 168 простых чисел. Определим 89-е наименьшее простое число. Получии срез массива с 89-го до 99-го элемента включительно, содержащий наименьшие простые числа (рис. [-@fig:19]).

![Задание 5](image/19.png){#fig:19 width=70%}

6. Вычислим выражения (рис. [-@fig:20]).

![Задание 6](image/20.png){#fig:20 width=70%}

# Выводы

Изучила несколько структур данных, реализованных в Julia, научилась применять их и операции над ними для решения задач.