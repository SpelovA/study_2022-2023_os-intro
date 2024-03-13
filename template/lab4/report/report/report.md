---
## Front matter
title: "Отчёт по лабораторной работе №4"
subtitle: "Работа с репозиториями Git"
author: "Спелов Андрей Николаевич НПИбд-02-23"

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
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase,Scale=0.9
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

Получить навыки правильной работы с репозиториями git.

# Выполнение лабораторной работы

Подключаем corp репозиторий. (рис. [-@fig:001]).

![Подключаем corp репозиторий](image/1.png){#fig:001 width=70%}

Скачиваем пакет gitflow (рис. [-@fig:002]).

![Скачиваем пакет gitflow](image/2.png){#fig:002 width=70%}

Скачиваем пакет nodejs (рис. [-@fig:003]).

![Скачиваем пакет nodejs](image/3.png){#fig:003 width=70%}

Скачиваем пакет pnpm (рис. [-@fig:004]).

![Скачиваем пакет pnpm](image/4.png){#fig:004 width=70%}

Запускаем pnpm (рис. [-@fig:005]).

![Запускаем pnpm](image/5.png){#fig:005 width=70%}

Перелогиниваемся и делаем общепринятый коммит (рис. [-@fig:006]).

![Перелогиниваемся и делаем общепринятый коммит](image/6.png){#fig:006 width=70%}

Вводим комманду для помощи создании логов (рис. [-@fig:007]).

![Вводим комманду для помощи создании логов](image/7.png){#fig:007 width=70%}

Создаем новый репозиторий git-extended (рис. [-@fig:008]).

![Создаем новый репозиторий](image/8.png){#fig:008 width=70%}

Клонируем репозиторий в папку work (рис. [-@fig:009]).

![Клонируем репозиторий](image/9.png){#fig:009 width=70%}

Делаем первый коммит и выкладываем на github (рис. [-@fig:010]).

![Делаем первый коммит и выкладываем на github](image/10.png){#fig:010 width=70%}

Конфигурация для пакетов Node.js (рис. [-@fig:011]).

![Конфигурация для пакетов Node.js](image/11.png){#fig:011 width=70%}

Меняем package.json в mc (рис. [-@fig:012]).

![Меняем package.json в mc](image/12.png){#fig:012 width=70%}

Добавляем новые файлы и отправляем на github (рис. [-@fig:013]).

![Добавляем новые файлы и отправляем на github](image/13.png){#fig:013 width=70%}

Инициализируем git-flow  (рис. [-@fig:014]).

![Инициализируем git-flow](image/14.png){#fig:014 width=70%}

Проверяем, что мы на ветке develop  (рис. [-@fig:015]).

![Проверяем, что мы на ветке develop](image/15.png){#fig:015 width=70%}

Проверяем, что мы на ветке develop (рис. [-@fig:016]).

![Загружаем весь репозиторий в хранилище](image/16.png){#fig:016 width=70%}

Установите внешнюю ветку как вышестоящую для этой ветки (рис. [-@fig:017]).

![Установите внешнюю ветку как вышестоящую для этой ветки](image/17.png){#fig:017 width=70%}

Создадим релиз с версией 1.0.0 (рис. [-@fig:018]).

![Создадим релиз с версией 1.0.0](image/18.png){#fig:018 width=70%}

Создадим журнал изменений (рис. [-@fig:019]).

![Создадим журнал изменений](image/19.png){#fig:019 width=70%}

Добавим журнал изменений в индекс (рис. [-@fig:020]).

![Добавим журнал изменений в индекс](image/20.png){#fig:020 width=70%}

Зальём релизную ветку в основную ветку (рис. [-@fig:021]).

![Зальём релизную ветку в основную ветку](image/21.png){#fig:021 width=70%}

Отправим данные на github (рис. [-@fig:022]).

![Отправим данные на github](image/22.png){#fig:022 width=70%}

Создадим релиз на github (рис. [-@fig:023]).

![Создадим релиз на github](image/23.png){#fig:023 width=70%}

Создадим ветку для новой функциональности (рис. [-@fig:024]).

![Создадим ветку для новой функциональности](image/24.png){#fig:024 width=70%}

Объединяем ветки (рис. [-@fig:025]).

![Объединяем ветки](image/25.png){#fig:025 width=70%}

Создадим релиз с версией 1.2.3 (рис. [-@fig:026]).

![Создадим релиз с версией 1.2.3](image/26.png){#fig:026 width=70%}

Меняем package.json в mc (рис. [-@fig:027]).

![Меняем package.json в mc](image/27.png){#fig:027 width=70%}

Cоздадим журнал изменений (рис. [-@fig:028]).

![оздадим журнал изменений](image/28.png){#fig:028 width=70%}

Добавим журнал изменений в индекс (рис. [-@fig:029]).

![Добавим журнал изменений в индекс](image/29.png){#fig:029 width=70%}

Зальём релизную ветку в основную ветку (рис. [-@fig:030]).

![Зальём релизную ветку в основную ветку](image/30.png){#fig:030 width=70%}

Отправим данные на github (рис. [-@fig:031]).

![Отправим данные на github](image/31.png){#fig:031 width=70%}

Создадим релиз на github с комментарием из журнала изменений (рис. [-@fig:032]).

![Создадим релиз на github с комментарием из журнала изменений](image/32.png){#fig:032 width=70%}

# Выводы

Мы получили навыки правильной работы с репозиториями git.

# Список литературы{.unnumbered}

::: {#refs}
:::
