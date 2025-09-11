---
## Front matter
title: "Отчет по лабораторной работе №2"
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

Основной целью работы является знакомство с инструментом для измерения пропускной способности сети в режиме реального времени — iPerf3, а также получение навыков проведения интерактивного эксперимента по измерению пропускной способности моделируемой сети в среде Mininet.


# Задание

1. Установить на виртуальную машину mininet iPerf3 и дополнительное программное обеспечения для визуализации и обработки данных.

2. Провести ряд интерактивных экспериментов по измерению пропускной способности с помощью iPerf3 с построением графиков.

# Выполнение лабораторной работы

1. Запустила виртуальную среду с mininet.

2. Из основной ОС подключилась к виртуальной машине.

![*Подключение к виртуальной машине*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab02/report/image/лаб2/1.png){#fig:001 width=70%}

3. После подключения к виртуальной машине mininet посмотрела IP-адреса машины.

![*IP-адреса машины*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab02/report/image/лаб2/2.png){#fig:002 width=70%}

4. Обновила репозитории программного обеспечения на виртуальной машине.

![*Обновление репозитории программного обеспечения*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab02/report/image/лаб2/3.png){#fig:003 width=70%}

5. Установила iperf3.

![*Установка iperf3*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab02/report/image/лаб2/4.png){#fig:004 width=70%}

6. Установила необходимое дополнительное программное обеспечение на виртуальную машину.

![*Установка необходимого дополнительного программного обеспечения*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab02/report/image/лаб2/5.png){#fig:005 width=70%}

7. Развернула iperf3_plotter. Для этого перешла во временный каталог и скачала репозиторий.

![*Скачивание репозитория*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab02/report/image/лаб2/6.png){#fig:006 width=70%}

8. Установила iperf3_plotter.

![*Установка iperf3_plotter*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab02/report/image/лаб2/7.png){#fig:007 width=70%}

9. Задала простейшую топологию, состоящую из двух хостов и коммутатора с назначенной по умолчанию mininet сетью 10.0.0.0/8.

![*Простейшая топология*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab02/report/image/лаб2/8.png){#fig:008 width=70%}

10. В терминале виртуальной машины посмотрела параметры запущенной в интерактивном режиме топологии.

![*Параметры запущенной топологии*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab02/report/image/лаб2/9.png){#fig:009 width=70%}

11. Провела простейший интерактивный эксперимент по измерению пропускной способности с помощью iPerf3. Для этого в терминале h2 запустила сервер iPerf3.

![*Запуск сервера iPerf3*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab02/report/image/лаб2/10.png){#fig:010 width=70%}

12. В терминале хоста h1 запустила клиент iPerf3.

![*Запуск клиента iPerf3*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab02/report/image/лаб2/11.png){#fig:011 width=70%}

![*Остановка серверного процесса*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab02/report/image/лаб2/12.png){#fig:012 width=70%}

13. Провела аналогичный эксперимент в интерфейсе mininet. Запустила сервер iPerf3 на хосте h2.

14. Запустила клиент iPerf3 на хосте h1.

![*Запуск клиента iPerf3*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab02/report/image/лаб2/13.png){#fig:013 width=70%}

15. Остановила серверный процесс.

![*Остановка серверного процесса*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab02/report/image/лаб2/14.png){#fig:014 width=70%}

16. Для указания iPerf3 периода времени для передачи использовала ключ -t (или --time) — время в секундах для передачи (по умолчанию 10 секунд). В терминале h2 запустила сервер iPerf3.

![*Запуск сервера iPerf3*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab02/report/image/лаб2/15.png){#fig:015 width=70%}

17. В терминале h1 запустила клиент iPerf3 с параметром -t, за которым следует количество секунд.

![*Запуск клиента iPerf3*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab02/report/image/лаб2/16.png){#fig:016 width=70%}

18. Настроила клиент iPerf3 для выполнения теста пропускной способности с 2-секундным интервалом времени отсчёта как на клиенте, так и на сервере. Использовала опцию -i для установки интервала между отсчётами, измеряемого в секундах. В терминале h2 запустила сервер iPerf3.

![*Запуск сервера iPerf3*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab02/report/image/лаб2/17.png){#fig:017 width=70%}

19. В терминале h1 запустила клиент iPerf3.

![*Запуск клиента iPerf3*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab02/report/image/лаб2/18.png){#fig:018 width=70%}

20. Задала на клиенте iPerf3 отправку определённого объёма данных. Использовала опцию -n для установки количества байт для передачи. В терминале h2 запустила сервер iPerf3 В терминале h1 запустила клиент iPerf3, задав объём данных 16 Гбайт.

![*Запуск клиента iPerf3*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab02/report/image/лаб2/19.png){#fig:019 width=70%}

21. Изменила в тесте измерения пропускной способности iPerf3 протокол передачи данных с TCP (установлен по умолчанию) на UDP. Для изменения протокола использовала опцию -u на стороне клиента iPerf3. В терминале h2 запустила сервер iPerf3. В терминале h1 запустила клиент iPerf3, задав протокол UDP.

![*Запуск клиента iPerf3*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab02/report/image/лаб2/20.png){#fig:020 width=70%}

22. В тесте измерения пропускной способности iPerf3 изменила номер порта для отправки/получения пакетов или датаграмм через указанный порт. Использовала для этого опцию -p. В терминале h2 запустила сервер iPerf3, используя параметр -p, чтобы указать порт прослушивания.

![*Запуск сервера iPerf3*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab02/report/image/лаб2/21.png){#fig:021 width=70%}

23. В терминале h1 запустила клиент iPerf3, указав порт.

![*Запуск клиента iPerf3*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab02/report/image/лаб2/22.png){#fig:022 width=70%}

24. В тесте измерения пропускной способности iPerf3 задала для сервера параметр обработки данных только от одного клиента с остановкой сервера по завершении теста. Для этого использовала опцию -1 на сервере iPerf3. В терминале h2 запустила сервер iPerf3, используя параметр -1, чтобы принять только одного клиента.

![*Запуск сервера iPerf3*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab02/report/image/лаб2/23.png){#fig:023 width=70%}

25. В терминале h1 запустила клиент iPerf3.

![*Запуск клиента iPerf3*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab02/report/image/лаб2/24.png){#fig:024 width=70%}

26. Экспортировала результаты теста измерения пропускной способности iPerf3 в файл JSON. Для этого в виртуальной машине mininet создала каталог для работы над проектом. 

![*Создание каталога*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab02/report/image/лаб2/25.png){#fig:025 width=70%}

27. В терминале h2 запустила сервер iPerf3. В терминале h1 запустила клиент iPerf3, указав параметр -J для отображения вывода результатов в формате JSON.

![*Запуск клиента iPerf3*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab02/report/image/лаб2/26.png){#fig:026 width=70%}

28. Остановила сервер iPerf3, нажав Ctrl+c в терминале хоста h2. Еще раз в терминале h2 запустила сервер iPerf3. Запустила клиента, экспортировав вывод результатов теста в файл, перенаправив стандартный вывод в файл.

![*Запуск клиента iPerf3*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab02/report/image/лаб2/27.png){#fig:027 width=70%}

29. Убедилась, что файл iperf_results.json создан в указанном каталоге.

![*Просмотр каталога*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab02/report/image/лаб2/28.png){#fig:028 width=70%}

30. Остановила сервер iPerf3, нажав Ctrl+c в терминале хоста h2 и завершила работу mininet в интерактивном режиме.

31. В виртуальной машине mininet исправила права запуска X-соединения. Скопировала значение куки своего пользователя
mininet в файл для пользователя root.

![*Исправление прав*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab02/report/image/лаб2/29.png){#fig:029 width=70%}

32. В виртуальной машине mininet перешла в каталог для работы над проектом и скорректировала права доступа
к файлу JSON.

![*Корректировка прав*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab02/report/image/лаб2/30.png){#fig:030 width=70%}

33. Сгенерировала выходные данные для файла JSON iPerf3.

![*Генерация выходных файлов*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab02/report/image/лаб2/31.png){#fig:031 width=70%}

34. Сценарий построения должен создать файл CSV (1.dat), который может использоваться другими приложениями. В подкаталоге results каталога, в котором был выполнен скрипт, сценарий должен создать графики для следующих полей файла JSON:
– окно перегрузки (cwnd.pdf);

– повторная передача (retransmits.pdf);

– время приема-передачи (RTT.pdf);

– отклонение времени приема-передачи (RTT_Var.pdf);

– пропускная способность (throughput.pdf);

– максимальная единица передачи (MTU.pdf);

– количество переданных байтов (bytes.pdf).

Убедилась, что файлы с данными и графиками сформировались.

![*Просмотр каталога*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab02/report/image/лаб2/32.png){#fig:032 width=70%}



# Выводы

Я ознакомилась с инструментом для измерения пропускной способности сети в режиме реального времени — iPerf3, а также получила навыков проведения интерактивного эксперимента по измерению пропускной способности моделируемой сети в среде Mininet.

# Список литературы{.unnumbered}

::: {#refs}
:::
