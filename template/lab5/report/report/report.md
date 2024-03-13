---
## Front matter
title: "Отчёт по лабораторной работе №5"
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

Получить навыки правильной настройки рабочей среды.

# Выполнение лабораторной работы

Устанавливаем pass (рис. [-@fig:001]).

![Устанавливаем pass](image/1.png){#fig:001 width=70%}

Устанавливаем gopass (рис. [-@fig:002]).

![Устанавливаем gopass](image/2.png){#fig:002 width=70%}

Инициализируем хранилище по gpg ключу (рис. [-@fig:003]).

![Инициализируем хранилище](image/3.png){#fig:003 width=70%}

Задаем адрес репозитория и создаем структуру (рис. [-@fig:004]).

![Задаем адрес репозитория и создаем структуру](image/4.png){#fig:004 width=70%}

Синхронизируем (рис. [-@fig:005]).

![Синхронизируем](image/5.png){#fig:005 width=70%}

Вручную закоммитим и выложим изменения (рис. [-@fig:006]).

![Вручную закоммитим и выложим изменения](image/6.png){#fig:006 width=70%}

Проверим статус синхронизации (рис. [-@fig:007]).

![Проверим статус синхронизации](image/7.png){#fig:007 width=70%}

Настройка интерфейса с браузером (рис. [-@fig:008]).

![Настройка интерфейса с браузером](image/8.png){#fig:008 width=70%}

![Настройка интерфейса с браузером](image/9.png){#fig:009 width=70%}

Добавим новый пароль (рис. [-@fig:010]).

![Добавим новый пароль](image/10.png){#fig:010 width=70%}

Проверим пароль и зададим новый (рис. [-@fig:011]).

![Проверим пароль и зададим новый](image/11.png){#fig:011 width=70%}

Установим дополнительное программное обеспечение (рис. [-@fig:012]).

![Установим дополнительное программное обеспечение](image/12.png){#fig:012 width=70%}

Установим шрифты (рис. [-@fig:013]).

![Установим шрифты](image/13.png){#fig:013 width=70%}

Установим бинарный файл  (рис. [-@fig:014]).

![Установим бинарный файл](image/14.png){#fig:014 width=70%}

# Выводы

Мы получили навыки правильной настройки рабочей среды.

# Список литературы{.unnumbered}

::: {#refs}
:::
