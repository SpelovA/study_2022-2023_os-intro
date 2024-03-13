---
## Front matter
title: "Отчёт по лабораторной работе №2"
subtitle: "Работа с Git"
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

Изучить идеологию и применение средств контроля версий и освоить умения по работе с git.

# Выполнение лабораторной работы

После установки git и gh переходим к настройке. Зададим имя и email владельца. (рис. [-@fig:001]).

![Задаем имя и email владельца](image/1.png){#fig:001 width=70%}

Настроим utf-8 в выводе сообщений git (рис. [-@fig:002]).

![Настройка utf-8](image/2.png){#fig:002 width=70%}

Зададим имя начальной ветки (будем называть её master) (рис. [-@fig:003]).

![Задаем имя ветки](image/3.png){#fig:003 width=70%}

Задаем параметр autocrlf (рис. [-@fig:004]).

![Задаем параметр autocrlf(input)](image/4.png){#fig:004 width=70%}

Задаем параметр safecrlf (рис. [-@fig:005]).

![Задаем параметр safecrlf(warn)](image/5.png){#fig:005 width=70%}

Создаем SSH ключ по алгоритму rsa (рис. [-@fig:006]).

![Создаем SSH ключ](image/6.png){#fig:006 width=70%}

Создаем SSH ключ по алгоритму ed25519 (рис. [-@fig:007]).

![Создаем SSH ключ](image/7.png){#fig:007 width=70%}

Создаем GPG ключ с нужными параметрами (рис. [-@fig:008]).

![Создаем GPG ключ](image/8.png){#fig:008 width=70%}

Выводим список ключей командой gpg --list-secret-keys --keyid-format LONG (рис. [-@fig:009]).

![Выводим список ключей](image/9.png){#fig:009 width=70%}

Cкопируем наш сгенерированный PGP ключ в буфер обмена (рис. [-@fig:010]).

![Копируем ключ](image/10.png){#fig:010 width=70%}

Заходим в настройки GitHub и вставляем GPG ключ (рис. [-@fig:011]).

![Вставляем ключ в свой аккаунт на GitHub](image/11.png){#fig:011 width=70%}

Настраиваем автоматические подписи коммитов git (рис. [-@fig:012]).

![Используя введёный email, указываем Git применять его при подписи коммитов](image/12.png){#fig:012 width=70%}

Начинаем настройку GH  (рис. [-@fig:013]).

![Настройка gh через браузер](image/13.png){#fig:013 width=70%}

Создаем рабочие папки в системе, переходим в нее и создаем шаблон рабочего пространства  (рис. [-@fig:014]).

![ИСоздаем рабочее пространство](image/14.png){#fig:014 width=70%}

Создаем репозиторий шаблона  (рис. [-@fig:015]).

![Создаем репозиторий](image/15.png){#fig:015 width=70%}

В каталоге курса удаляем лишние файлы и создаем необходимые каталоги  (рис. [-@fig:016]).

![Редкатируем курс](image/16.png){#fig:016 width=70%}

Отправляем файлы на сервер (рис. [-@fig:017]).

![Отправляем файлы на сервер](image/17.png){#fig:017 width=70%}

# Выводы

Мы изучили идеологию и применение средств контроля версий и освоили умения по работе с git.

# Список литературы{.unnumbered}

::: {#refs}
:::
