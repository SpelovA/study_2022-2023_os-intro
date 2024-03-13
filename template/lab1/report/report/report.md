---
## Front matter
title: "Отчёт по лабораторной работе №1"
subtitle: "Установка операционной системы Linux, дистрибутив Fedora Sway на виртуальную машину"
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

Приобрести практические навыки установки операционной системы на виртуальную машину, настройки минимально необходимых для дальнейшей работы сервисов.

# Выполнение лабораторной работы

На заранее установленный Virtual Box начинаем процесс установки виртуальной машины(называем машину, ставим тип системы) (рис. [-@fig:001]).

![Начало создания виртуальной машины](image/1.png){#fig:001 width=70%}

Ставим необходимое для работы количество памяти и ядер процессора (рис. [-@fig:002]).

![Первоначальная настройка виртуальной машины](image/2.png){#fig:002 width=70%}

Ставим необходимое количество памяти жесткого диска на виртуальную машину(80+ Гб) (рис. [-@fig:003]).

![Создаем виртуальный жесткий диск](image/3.png){#fig:003 width=70%}

Закончив настройку виртуальной машины в меню Virtual Box выбираем заранее установленную систему Fedora Sway (рис. [-@fig:004]).

![Выбираем систему в качестве оптического привода для дальнейшей установки](image/4.png){#fig:004 width=70%}

Заходим на виртуальную машину (рис. [-@fig:005]).

![Заходим на машину и вводим необходимые команды для начала установки системы](image/5.png){#fig:005 width=70%}

Заходим в меню установки системы (рис. [-@fig:006]).

![Начинаем выбирать нужную конфигурацию будущей системы](image/6.png){#fig:006 width=70%}

Выбираем все необходимые параметры(раскладку клавиатуры, супер пользователя root) и начинаем установку (рис. [-@fig:007]).

![Выбираем нужную конфигурацию](image/7.png){#fig:007 width=70%}

После установки системы закрываем машину и убираем загрузочный диск (рис. [-@fig:008]).

![Удаляем загрузочный диск](image/8.png){#fig:008 width=70%}

Запускаем виртуальную машину (рис. [-@fig:009]).

![Снова заходим в систему](image/9.png){#fig:009 width=70%}

Заходим в терминал и скачиваем все необходимые обновления системы (рис. [-@fig:010]).

![Используем команду sudo dnf -y update](image/10.png){#fig:010 width=70%}

Устанавливаем tmux командой dnf -y install tmux mc, устанавливаем пакет DKMS (рис. [-@fig:011]).

![Устанавливаем необходимый софт](image/11.png){#fig:011 width=70%}

Так же устанавливаем pandoc командой dnf -y install pandoc и TexLive командой dnf -y install texlive-scheme-full (рис. [-@fig:012]).

![Устанавливаем язык разметки Markdown](image/12.png){#fig:012 width=70%}

# Домашнее задание

Узнаем Версию ядра Linux  (рис. [-@fig:013]).

![Используем команду dmesg | grep -i "linux version"](image/13.png){#fig:013 width=70%}

Узнаем Частоту процессора  (рис. [-@fig:014]).

![Используем команду dmesg | grep -i "MHz"](image/14.png){#fig:014 width=70%}

Узнаем Модель процессора  (рис. [-@fig:015]).

![Используем команду dmesg | grep -i "CPU0"](image/16.png){#fig:015 width=70%}

Узнаем Объём доступной оперативной памяти  (рис. [-@fig:016]).

![Используем команду free -m](image/17.png){#fig:016 width=70%}

Узнаем Тип обнаруженного гипервизора  (рис. [-@fig:017]).

![Используем команду dmesg | grep -i "hypervisor detected"](image/18.png){#fig:017 width=70%}

Узнаем Тип файловой системы корневого раздела  (рис. [-@fig:018]).

![Используем команду dfindmnt](image/19.png){#fig:018 width=70%}

Узнаем Последовательность монтирования файловых систем  (рис. [-@fig:019]).

![Используем команду dmesg | grep -i "mount"](image/20.png){#fig:019 width=70%}


# Выводы

Мы приобрели практические навыки установки операционной системы на виртуальную машину, настройки минимально необходимых для дальнейшей работы сервисов.

# Список литературы{.unnumbered}

::: {#refs}
:::
