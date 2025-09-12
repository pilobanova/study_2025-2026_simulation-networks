---
## Front matter
title: "Отчет по лабораторной работе №3"
subtitle: "Дисциплина: Моделирование сетей передачи данных"
author: "Лобанова Полина Иннокентьевна"

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

Основной целью работы является знакомство с инструментом для измерения пропускной способности сети в режиме реального времени — iPerf3, а также получение навыков проведения воспроизводимого эксперимента по измерению пропускной способности моделируемой сети в среде Mininet.

# Задание

1. Воспроизвести посредством API Mininet эксперименты по измерению пропускной способности с помощью iPerf3.
2. Построить графики по проведённому эксперименту.

# Выполнение лабораторной работы

1. С помощью API Mininet создала простейшую топологию сети, состоящую из двух хостов и коммутатора с назначенной по умолчанию mininet сетью 10.0.0.0/8. Для этого в каталоге /work/lab_iperf3 для работы над проектом создала подкаталог lab_iperf3_topo и скопировала в него файл с примером скрипта mininet/examples/emptynet.py, описывающего стандартную простую топологию сети mininet.

![*Создание каталога и копирование файла*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab03/report/image/лаб3/1.png){#fig:001 width=70%}

2. Изучила содержание скрипта lab_iperf3_topo.py.

![*Скрипт lab_iperf3_topo.py*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab03/report/image/лаб3/2.png){#fig:002 width=70%}

3. Запустила скрипт создания топологии lab_iperf3_topo.py.

![*Запуск скрипта*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab03/report/image/лаб3/3.png){#fig:003 width=70%}

4. После отработки скрипта посмотрела элементы топологии и завершила работу mininet.

![*Элементы топологии*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab03/report/image/лаб3/4.png){#fig:004 width=70%}

5. Внесла в скрипт lab_iperf3_topo.py изменение, позволяющее вывести на экран информацию о хосте h1, а именно имя хоста, его IP-адрес, MACадрес. 

![*Внесение изменений в скрипт*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab03/report/image/лаб3/5.png){#fig:005 width=70%}

6. Проверила корректность отработки изменённого скрипта.

![*Запуск скрипта*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab03/report/image/лаб3/6.png){#fig:006 width=70%}

7. Изменила скрипт lab_iperf3_topo.py так, чтобы на экран выводилась информация об имени, IP-адресе и MAC-адресе обоих хостов сети. Проверила корректность отработки изменённого скрипта.

![*Внесение изменений в скрипт*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab03/report/image/лаб3/7.png){#fig:007 width=70%}

![*Запуск скрипта*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab03/report/image/лаб3/8.png){#fig:008 width=70%}

8. Добавила в скрипт настройки параметров производительности. Для этого сделала копию скрипта lab_iperf3_topo.py.

![*Внесение изменений в скрипт*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab03/report/image/лаб3/9.png){#fig:009 width=70%}

9. В начале скрипта lab_iperf3_topo2.py добавила записи об импорте классов CPULimitedHost и TCLink.

![*Внесение изменений в скрипт*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab03/report/image/лаб3/10.png){#fig:010 width=70%}

10. В скрипте lab_iperf3_topo2.py изменила строку описания сети, указав на использование ограничения производительности и изоляции.

![*Внесение изменений в скрипт*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab03/report/image/лаб3/11.png){#fig:011 width=70%}

11. В скрипте lab_iperf3_topo2.py изменила функцию задания параметров виртуального хоста h1, указав, что ему будет выделено 50% от общих ресурсов процессора системы.

![*Внесение изменений в скрипт*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab03/report/image/лаб3/12.png){#fig:012 width=70%}

12. Аналогичным образом для хоста h2 задала долю выделения ресурсов процессора в 45%.

![*Внесение изменений в скрипт*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab03/report/image/лаб3/13.png){#fig:013 width=70%}

13. В скрипте lab_iperf3_topo2.py изменила функцию параметров соединения между хостом h1 и коммутатором s3.

![*Внесение изменений в скрипт*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab03/report/image/лаб3/14.png){#fig:014 width=70%}

14. Запустила на отработку сначала скрипт lab_iperf3_topo2.py, затем lab_iperf3_topo.py и сравнила результат.

![*Запуск скрипта*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab03/report/image/лаб3/15.png){#fig:015 width=70%}

15. Построила графики по проводимому эксперименту. Для этого сделала копию скрипта lab_iperf3_topo2.py и поместила его в подкаталог iperf.

![*Создание подкаталога и копирование скрипта*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab03/report/image/лаб3/16.png){#fig:016 width=70%}

16. В начале скрипта lab_iperf3.py добавила запись import time.

![*Внесение изменений в скрипт*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab03/report/image/лаб3/17.png){#fig:017 width=70%}

17. Изменила код в скрипте lab_iperf3.py так, чтобы:

– на хостах не было ограничения по использованию ресурсов процессора;

– каналы между хостами и коммутатором были по 100 Мбит/с с задержкой 75 мс, без потерь, без использования ограничителей пропускной способности и максимального размера очереди.

![*Внесение изменений в скрипт*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab03/report/image/лаб3/18.png){#fig:018 width=70%}

18. После функции старта сети описала запуск на хосте h2 сервера iPerf3, а на хосте h1 запуск с задержкой в 10 секунд клиента iPerf3 с экспортом результатов в JSON-файл, закомментировала строки, отвечающие за запуск
CLI-интерфейса.

![*Внесение изменений в скрипт*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab03/report/image/лаб3/19.png){#fig:019 width=70%}

19. Запустила на отработку скрипт lab_iperf3.py.

![*Запуск скрипта*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab03/report/image/лаб3/20.png){#fig:020 width=70%}

20. Построила графики из получившегося JSON-файла.

![*Построение графиков*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab03/report/image/лаб3/21.png){#fig:021 width=70%}

21. Создала Makefile для проведения всего эксперимента. В Makefile прописала запуск скрипта эксперимента, построение графиков и очистку каталога от результатов.

![*Написание скрипта Makefile*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab03/report/image/лаб3/22.png){#fig:022 width=70%}

22. Проверила корректность отработки Makefile.

![*Запуск скрипта Makefile*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab03/report/image/лаб3/23.png){#fig:023 width=70%}

23. Завершила соединение с виртуальной машиной mininet и выключила её.

# Выводы

Я ознакомилась с инструментом для измерения пропускной способности сети в режиме реального времени — iPerf3, а также
получила навыки проведения воспроизводимого эксперимента по измерению пропускной способности моделируемой сети в среде Mininet.

# Список литературы{.unnumbered}

::: {#refs}
:::
