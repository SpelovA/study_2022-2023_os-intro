---
## Front matter
title: "Лабораторная работа №8"
subtitle: "Адресация IPv4 и IPv6. Настройка маршрутизации"
author: "Спелов Андрей Николаевич"

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

Целью данной работы является изучение принципов маршрутизации в IPv4- и IPv6-сетях и принципы настройки сетевого оборудования.

# Выполнение лабораторной работы

Запустим GNS3 VM и GNS3 и создадим новый проект (рис. [-@fig:001]):

![Создание нового проекта в GNS3.](image/1.png){#fig:001 width=70%}

В рабочем пространстве разместим и соединим устройства в соответствии с топологией, приведённой в лабораторной работе. Будем использовать маршрутизаторы FRR. Далее изменим отображаемые названия устройств. Коммутаторам присвоим названия msk-anspelov-sw-0x, маршрутизаторам — msk-anspelov-gw-0x, VPCS — PCx-anspelov, где вместо x — порядковый номер устройства (рис. [-@fig:002]):

![Размещение устройств в соответствии с топологией в лабораторной работе. Изменение названий устройств.](image/2.png){#fig:002 width=70%}

Включим захват трафика на соединении между коммутатором sw-01 и маршрутизатором gw-01, а также между коммутатором sw-02 и маршрутизатором gw-03 (рис. [-@fig:003]):

![Включение захвата трафика.](image/3.png){#fig:003 width=70%}

Присвоим IPv4-адреса оконечным устройствам PC1 и PC2 в соответствии с данными в таблице (рис. [-@fig:004]):

![Присвоение IPv4-адреса конечному устройству PC1-anspelov.](image/4.png){#fig:004 width=70%}

![Присвоение IPv4-адреса конечному устройству PC2-anspelov.](image/5.png){#fig:005 width=70%}

Настроим IPv4-адреса на интерфейсах маршрутизаторов (рис. [-@fig:006]):

![Настройка IPv4-адреса на интерфейсе маршрутизатора msk-anspelov-gw-01.](image/6.png){#fig:006 width=70%}

![Настройка IPv4-адреса на интерфейсе маршрутизатора msk-anspelov-gw-02.](image/7.png){#fig:007 width=70%}

![Настройка IPv4-адреса на интерфейсе маршрутизатора msk-anspelov-gw-03.](image/8.png){#fig:008 width=70%}

![Настройка IPv4-адреса на интерфейсе маршрутизатора msk-anspelov-gw-04.](image/9.png){#fig:009 width=70%}

Присвоим IPv6-адреса оконечным устройствам PC1 и PC2 в соответствии с данными в таблице (рис. [-@fig:010]):

![Присвоение IPv6-адреса конечному устройству PC1-anspelov.](image/10.png){#fig:010 width=70%}

![Присвоение IPv6-адреса конечному устройству PC2-anspelov.](image/11.png){#fig:011 width=70%}

Настроим IPv6-адреса на интерфейсах маршрутизаторов (рис. [-@fig:012]):

![Настройка IPv6-адреса на интерфейсе маршрутизатора msk-anspelov-gw-01.](image/12.png){#fig:012 width=70%}

![Настройка IPv6-адреса на интерфейсе маршрутизатора msk-anspelov-gw-02.](image/13.png){#fig:013 width=70%}

![Настройка IPv6-адреса на интерфейсе маршрутизатора msk-anspelov-gw-03.](image/14.png){#fig:014 width=70%}

![Настройка IPv6-адреса на интерфейсе маршрутизатора msk-anspelov-gw-04.](image/15.png){#fig:015 width=70%}

На маршрутизаторах настроим RIP в качестве протокола динамической маршрутизации (рис. [-@fig:016]):

![Настройка RIP в качестве протокола динамической маршрутизации на маршрутизаторе msk-anspelov-gw-01.](image/16.png){#fig:016 width=70%}

![Настройка RIP в качестве протокола динамической маршрутизации на маршрутизаторе msk-anspelov-gw-02.](image/17.png){#fig:017 width=70%}

![Настройка RIP в качестве протокола динамической маршрутизации на маршрутизаторе msk-anspelov-gw-03.](image/18.png){#fig:018 width=70%}

![Настройка RIP в качестве протокола динамической маршрутизации на маршрутизатора msk-anspelov-gw-04.](image/19.png){#fig:019 width=70%}

Убедимся, что маршрутизация по RIP настроена (рис. [-@fig:020]):

![Проверка настройки маршрутизации RIP на маршрутизаторе msk-anspelov-gw-01.](image/20.png){#fig:020 width=70%}

![Проверка настройки маршрутизации RIP на маршрутизаторе msk-anspelov-gw-02.](image/21.png){#fig:021 width=70%}

![Проверка настройки маршрутизации RIP на маршрутизаторе msk-anspelov-gw-03.](image/22.png){#fig:022 width=70%}

![Проверка настройки маршрутизации RIP на маршрутизаторе msk-anspelov-gw-04.](image/23.png){#fig:023 width=70%}

Проверим метрики протокола RIP (рис. [-@fig:024]).

![Проверка метрики протокола RIP.](image/24.png){#fig:024 width=70%}

Предположим, что пакет проходит через маршрутизатор msk-anspelov-gw-02. Для этого отключим на маршрутизаторе msk-anspelov-gw-02 интерфейс (рис. [-@fig:025]):

![Отключение на маршрутизаторе msk-anspelov-gw-02 интерфейса.](image/25.png){#fig:025 width=70%}

Проверим метрики протокола RIP (рис. [-@fig:026]):

![Проверка метрики протокола RIP.](image/26.png){#fig:026 width=70%}

Включим на маршрутизаторе msk-anspelov-gw-02 интерфейс (рис. [-@fig:027]):

![Включение на маршрутизаторе msk-anspelov-gw-02 интерфейса.](image/27.png){#fig:027 width=70%}

На маршрутизаторах настроим RIPng для сетей IPv6 (рис. [-@fig:028]):

![Настройка RIPng для сетей IPv6 на маршрутизаторе msk-anspelov-gw-01.](image/28.png){#fig:028 width=70%}

![Настройка RIPng для сетей IPv6 на маршрутизаторе msk-anspelov-gw-02.](image/29.png){#fig:029 width=70%}

![Настройка RIPng для сетей IPv6 на маршрутизаторе msk-anspelov-gw-03.](image/30.png){#fig:030 width=70%}

![Настройка RIPng для сетей IPv6 на маршрутизаторе msk-anspelov-gw-04.](image/31.png){#fig:031 width=70%}

Проверим метрики протокола RIPng (рис. [-@fig:032]).

![Проверка метрики протокола RIPng.](image/32.png){#fig:032 width=70%}

Предположим, что пакет проходит через маршрутизатор msk-anspelov-gw-02. Для этого отключим на маршрутизаторе msk-anspelov-gw-02 интерфейс (рис. [-@fig:033]):

![Отключение на маршрутизаторе msk-anspelov-gw-02 интерфейса.](image/33.png){#fig:033 width=70%}

Проверим метрики протокола RIPng (рис. [-@fig:034]):

![Проверка метрики протокола RIPng.](image/34.png){#fig:034 width=70%}

Включим на маршрутизаторе msk-anspelov-gw-02 интерфейс (рис. [-@fig:035]):

![Включение на маршрутизаторе msk-anspelov-gw-02 интерфейса.](image/35.png){#fig:035 width=70%}

На маршрутизаторах настроим OSPFv2 для сетей IPv4 (рис. [-@fig:036]):

![Настройка OSPFv2 для сетей IPv4 на маршрутизаторе msk-anspelov-gw-01.](image/36.png){#fig:036 width=70%}

![Настройка OSPFv2 для сетей IPv4 на маршрутизаторе msk-anspelov-gw-02.](image/37.png){#fig:037 width=70%}

![Настройка OSPFv2 для сетей IPv4 на маршрутизаторе msk-anspelov-gw-03.](image/38.png){#fig:038 width=70%}

![Настройка OSPFv2 для сетей IPv4 на маршрутизаторе msk-anspelov-gw-04.](image/39.png){#fig:039 width=70%}

Проверим таблицу маршрутизации протокола OSPFv2 (рис. [-@fig:040]):

![Проверка таблицы маршрутизации протокола OSPFv2.](image/40.png){#fig:040 width=70%}

Предположим, что пакет проходит через маршрутизатор msk-anspelov-gw-02. Для этого отключим на маршрутизаторе msk-anspelov-gw-02 интерфейс (рис. [-@fig:041]):

![Отключение на маршрутизаторе msk-anspelov-gw-02 интерфейса.](image/41.png){#fig:041 width=70%}

Проверим таблицу маршрутизации протокола OSPFv2 (рис. [-@fig:042]):

![Проверка таблицы маршрутизации протокола OSPFv2.](image/42.png){#fig:042 width=70%}

Включим на маршрутизаторе msk-anspelov-gw-02 интерфейс (рис. [-@fig:043]):

![Включение на маршрутизаторе msk-anspelov-gw-02 интерфейса.](image/43.png){#fig:043 width=70%}

На маршрутизаторах настроим OSPFv3 для сетей IPv6 (рис. [-@fig:044]):

![Настройка OSPFv3 для сетей IPv6 на маршрутизаторе msk-anspelov-gw-01.](image/44.png){#fig:044 width=70%}

![Настройка OSPFv3 для сетей IPv6 на маршрутизаторе msk-anspelov-gw-02.](image/45.png){#fig:045 width=70%}

![Настройка OSPFv3 для сетей IPv6 на маршрутизаторе msk-anspelov-gw-03.](image/46.png){#fig:046 width=70%}

![Настройка OSPFv3 для сетей IPv6 на маршрутизаторе msk-anspelov-gw-04.](image/47.png){#fig:047 width=70%}

Проверим таблицу маршрутизации протокола OSPFv3 (рис. [-@fig:048]):

![Проверка таблицы маршрутизации протокола OSPFv3.](image/48.png){#fig:048 width=70%}

Предположим, что пакет проходит через маршрутизатор msk-anspelov-gw-02. Для этого отключим на маршрутизаторе msk-anspelov-gw-02 интерфейс (рис. [-@fig:049]):

![Отключение на маршрутизаторе msk-anspelov-gw-02 интерфейса.](image/49.png){#fig:049 width=70%}

Проверим таблицу маршрутизации протокола OSPFv3 (рис. [-@fig:050]):

![Проверка таблицы маршрутизации протокола OSPFv3.](image/50.png){#fig:050 width=70%}

Включим на маршрутизаторе msk-anspelov-gw-02 интерфейс (рис. [-@fig:051]):

![Включение на маршрутизаторе msk-anspelov-gw-02 интерфейса.](image/51.png){#fig:051 width=70%}

Создадим новый проект в GNS3 (рис. [-@fig:052]):

![Создание нового проекта в GNS3.](image/52.png){#fig:052 width=70%}

В рабочем пространстве разместим и соединим устройства в соответствии с топологией, приведённой в лабораторной работе. Для этого будем использовать маршрутизаторы VyOS. Изменим отображаемые названия устройств. Коммутаторам присвоим названия msk-anspelov-sw-0x, маршрутизаторам — msk-anspelov-gw-0x, VPCS — PCx-anspelov, где вместо x — порядковый номер устройства (рис. [-@fig:053]):

![Размещение устройств в соответствии с топологией в лабораторной работе. Изменение названий устройств.](image/53.png){#fig:053 width=70%}

На соединении между первым и третьим маршрутизаторами подключим анализатор трафика (рис. [-@fig:054]):

![Включение захвата трафика.](image/54.png){#fig:054 width=70%}

Присвоим адреса оконечным устройствам PC1 и PC2 в соответствии с данными в таблице (рис. [-@fig:055]):

![Присвоение адреса конечному устройству PC1-anspelov.](image/55.png){#fig:055 width=70%}

![Присвоение адреса конечному устройству PC2-anspelov.](image/56.png){#fig:056 width=70%}

На маршрутизаторах перейдём в режим конфигурирования, изменим имя устройства (рис. [-@fig:058]):

![Изменение имени маршрутизатора msk-anspelov-gw-01.](image/58.png){#fig:058 width=70%}

![Изменение имени маршрутизатора msk-anspelov-gw-02.](image/59.png){#fig:059 width=70%}

![Изменение имени маршрутизатора msk-anspelov-gw-03.](image/60.png){#fig:060 width=70%}

Настроим адреса на интерфейсах маршрутизаторов (рис. [-@fig:061]):

![Настройка адреса на интерфейсе маршрутизатора msk-anspelov-gw-01.](image/61.png){#fig:061 width=70%}

![Настройка адреса на интерфейсе маршрутизатора msk-anspelov-gw-02.](image/62.png){#fig:062 width=70%}

![Настройка адреса на интерфейсе маршрутизатора msk-anspelov-gw-03.](image/63.png){#fig:063 width=70%}

Проверим маршруты с маршрутизатора R1 (рис. [-@fig:064]):

![Проверка маршрутов с маршрутизатора msk-anspelov-gw-01.](image/64.png){#fig:064 width=70%}

Настроим маршрутизацию IPv4 (рис. [-@fig:065]):

![Настройка маршрутизации IPv4 на маршрутизаторе msk-anspelov-gw-01.](image/65.png){#fig:065 width=70%}

![Настройка маршрутизации IPv4 на маршрутизаторе msk-anspelov-gw-02.](image/66.png){#fig:066 width=70%}

![Настройка маршрутизации IPv4 на маршрутизаторе msk-anspelov-gw-03.](image/67.png){#fig:067 width=70%}

Проверим маршруты (рис. [-@fig:068]):

![Проверка маршрутов.](image/68.png){#fig:068 width=70%}

Создадим туннель IPv6 через сеть IPv4 (рис. [-@fig:069]):

![Создание туннеля IPv6 через сеть IPv4 на маршрутизаторе msk-anspelov-gw-01.](image/69.png){#fig:069 width=70%}

![Создание туннеля IPv6 через сеть IPv4 на маршрутизаторе msk-anspelov-gw-02.](image/70.png){#fig:070 width=70%}

Настроим статическую маршрутизацию IPv6 (рис. [-@fig:071]):

![Настройка статической маршрутизации на маршрутизаторе msk-anspelov-gw-01.](image/71.png){#fig:071 width=70%}

![Настройка статической маршрутизации на маршрутизаторе msk-anspelov-gw-02.](image/72.png){#fig:072 width=70%}

# Выводы

В ходе выполнения лабораторной работы мы изучили принципы маршрутизации в IPv4- и IPv6-сетях и принципы настройки сетевого оборудования.

# Список литературы{.unnumbered}

::: {#refs}
:::
