---
## Front matter
title: "Отчет по лабораторной работе №4"
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

Основной целью работы является знакомство с NETEM — инструментом для тестирования производительности приложений в виртуальной сети, а также получение навыков проведения интерактивного и воспроизводимого экспериментов по измерению задержки и её дрожания (jitter) в моделируемой сети в среде Mininet.

# Задание

1. Задайте простейшую топологию, состоящую из двух хостов и коммутатора с назначенной по умолчанию mininet сетью 10.0.0.0/8.

2. Проведите интерактивные эксперименты по добавлению/изменению задержки, джиттера, значения корреляции для джиттера и задержки, распределения времени задержки в эмулируемой глобальной сети.

3. Реализуйте воспроизводимый эксперимент по заданию значения задержки в эмулируемой глобальной сети. Постройте график. 

4. Самостоятельно реализуйте воспроизводимые эксперименты по изменению задержки, джиттера, значения корреляции для джиттера и задержки, распределения времени задержки в эмулируемой глобальной сети. Постройте графики.

# Выполнение лабораторной работы

1. Запустила виртуальную среду с mininet и из основной ОС подключилась к виртуальной машине.

2. В виртуальной машине mininet исправила права запуска X-соединения. Скопировала значение куки своего пользователя mininet в файл для пользователя root.

![*Исправление права запуска X-соединения*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/1.png){#fig:001 width=70%}

3. Задала простейшую топологию, состоящую из двух хостов и коммутатора с назначенной по умолчанию mininet сетью 10.0.0.0/8.

![*Создание простейшей топологии*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/2.png){#fig:002 width=70%}

4. На хостах h1 и h2 ввела команду ifconfig, чтобы отобразить информацию, относящуюся к их сетевым интерфейсам и назначенным им IP-адресам.

![*Команда ifconfig на хосте h1*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/3.png){#fig:003 width=70%}

![*Команда ifconfig на хосте h2*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/4.png){#fig:004 width=70%}

5. Проверила подключение между хостами h1 и h2 с помощью команды ping с параметром -c 6.
Минимальное RTT: 0,03; Среднее RTT: 0,548; Максимальное RTT: 1,3; Стандартное отклонение: 0,464.

![*Команда ping*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/5.png){#fig:005 width=70%}

![*Команда ping*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/6.png){#fig:006 width=70%}

6. На хосте h1 добавила задержку в 100 мс к выходному интерфейсу.

![*Добавление задержки на хосте h1*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/7.png){#fig:007 width=70%}

7. Проверила, что соединение от хоста h1 к хосту h2 имеет задержку 100 мс, используя команду ping с параметром -c 6 с хоста h1. Минимальное RTT: 100; Среднее RTT: 100,8; Максимальное RTT: 101; Стандартное отклонение: 0,374.

![*Команда ping*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/8.png){#fig:008 width=70%}

8. Для эмуляции глобальной сети с двунаправленной задержкой к соответствующему интерфейсу на хосте h2 также добавила задержку в 100 миллисекунд.

![*Добавление задержки на хосте h2*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/9.png){#fig:009 width=70%}

9. Проверила, что соединение между хостом h1 и хостом h2 имеет RTT в 200 мс (100 мс от хоста h1 к хосту h2 и 100 мс от хоста h2 к хосту h1), повторив команду ping с параметром -c 6 на терминале хоста h1. Минимальное RTT: 201; Среднее RTT: 201; Максимальное RTT: 201; Стандартное отклонение: 0.

![*Команда ping*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/10.png){#fig:010 width=70%}

10. Изменила задержку со 100 мс до 50 мс для отправителя h1 и для получателя h2.

![*Изменение задержки*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/11.png){#fig:011 width=70%}

11. Проверила, что соединение от хоста h1 к хосту h2 имеет задержку 100 мс, используя команду ping с параметром -c 6 с терминала хоста h1. Минимальное RTT: 100; Среднее RTT: 101; Максимальное RTT: 102; Стандартное отклонение: 1.

![*Команда ping*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/12.png){#fig:012 width=70%}

12. Восстановила конфигурацию по умолчанию, удалив все правила, применённые к сетевому планировщику соответствующего интерфейса. Для отправителя h1 и для получателя h2.

![*Удаление правил*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/13.png){#fig:013 width=70%}

13. Проверила, что соединение между хостом h1 и хостом h2 не имеет явно установленной задержки, используя команду ping с параметром -c 6 с терминала хоста h1. Минимальное RTT: 0,033; Среднее RTT: 0,5118; Максимальное RTT: 1,11; Стандартное отклонение: 0,487.

![*Команда ping*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/14.png){#fig:014 width=70%}

14. Добавила на узле h1 задержку в 100 мс со случайным отклонением 10 мс.

![*Добавление задержки со случайным отклонением*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/15.png){#fig:015 width=70%}

15. Проверьте, что соединение от хоста h1 к хосту h2 имеет задержку 100 мс со случайным отклонением ±10 мс, используя в терминале хоста h1 команду ping с параметром -c 6. Минимальное RTT: 94; Среднее RTT: 102.46; Максимальное RTT: 111; Стандартное отклонение: 6.6.

![*Команда ping*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/16.png){#fig:016 width=70%}

16. Восстановила конфигурацию интерфейса по умолчанию на узле h1.

![*Удаление правил*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/17.png){#fig:017 width=70%}

17. Добавила на интерфейсе хоста h1 задержку в 100 мс с вариацией ±10 мс и значением корреляции 25%.

![*Добавление задержки со случайным отклонением и корреляцией*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/18.png){#fig:018 width=70%}

18. Убедилась, что все пакеты, покидающие устройство h1 на интерфейсе h1-eth0, будут иметь время задержки 100 мс со случайным отклонением ±10 мс, при этом время передачи следующего пакета зависит от предыдущего значения на 25%. Использовала для этого в терминале хоста h1 команду ping с параметром -c 6. Минимальное RTT: 91,5; Среднее RTT: 97,3; Максимальное RTT: 109; Стандартное отклонение: 6,43. Восстановила конфигурацию интерфейса по умолчанию на узле h1.

![*Команда ping*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/19.png){#fig:019 width=70%}

19. Задала нормальное распределение задержки на узле h1 в эмулируемой сети.

![*Добавление нормального распределения*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/20.png){#fig:020 width=70%}

20. Убедилась, что все пакеты, покидающие хост h1 на интерфейсе h1-eth0, будут иметь время задержки, которое распределено в диапазоне 100 мс ±20 мс. Использовала для этого команду ping на терминале хоста h1 с параметром
-c 6. Минимальное RTT: 75,8; Среднее RTT: 106,3; Максимальное RTT: 135; Стандартное отклонение: 24,36. Завершила работу mininet в интерактивном режиме.

![*Команда ping*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/21.png){#fig:021 width=70%}

21. Обновила репозитории программного обеспечения на виртуальной машине.

![*Обновление репозиториев программного обеспечения*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/22.png){#fig:022 width=70%}

22. Установила пакет geeqie — понадобится для просмотра файлов png.

![*Установка пакета geeqie*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/23.png){#fig:023 width=70%}

23. Для каждого воспроизводимого эксперимента expname создала свой каталог, в котором будут размещаться файлы эксперимента.

![*Создание каталога*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/24.png){#fig:024 width=70%}

24. В виртуальной среде mininet в своём рабочем каталоге с проектами создала каталог simple-delay и перешла в него.

![*Создание подкаталога*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/25.png){#fig:025 width=70%}

25. Создала скрипт для эксперимента lab_netem_i.py.

![*Создание скрипта lab_netem_i.py*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/26.png){#fig:026 width=70%}

26. Создала скрипт для визуализации ping_plot результатов эксперимента.

![*Создание скрипта ping_plot*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/27.png){#fig:027 width=70%}

27. Задала права доступа к файлу скрипта.

![*Изменение прав доступа*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/28.png){#fig:028 width=70%}

28. Создала Makefile для управления процессом проведения эксперимента.

![*Создание Makefile*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/29.png){#fig:029 width=70%}

29. Выполнила эксперимент.

![*Выполнение эксперемента*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/30.png){#fig:030 width=70%}

30. Продемонстрировала построенный в результате выполнения скриптов график.

![*График 1.1*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/31.png){#fig:031 width=70%}

31. Из файла ping.dat удалила первую строку и заново постройте график.

![*Удаление строки*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/32.png){#fig:032 width=70%}

32. Продемонстрировала построенный в результате график.

![*График 1.2*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/33.png){#fig:033 width=70%}

33. Разработала скрипт для вычисления на основе данных файла ping.dat минимального, среднего, максимального и стандартного отклонения времени приёма-передачи. Добавила правило запуска скрипта в Makefile. Продемонстрировала работу скрипта с выводом значений на экран. Очистила каталог от результатов проведения экспериментов.

![*Скрипт для вычисления данных*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/34.png){#fig:034 width=70%}

![*Изменение Makefile*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/35.png){#fig:035 width=70%}

![*Результат работы скрипта*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/36.png){#fig:036 width=70%}

34. Самостоятельно реализовала воспроизводимые эксперименты по изменению задержки в эмулируемой глобальной сети. Построила графики. Вычислила минимальное, среднее, максимальное и стандартное отклонение времени приёма-передачи для каждого случая.

![*Изменение файла lab_netem_i.py*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/37.png){#fig:037 width=70%}

![*График 2*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/38.png){#fig:038 width=70%}

![*Вычисленные значения*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/39.png){#fig:039 width=70%}

35. Самостоятельно реализовала воспроизводимые эксперименты по изменению джиттера в эмулируемой глобальной сети. Построила графики. Вычислила минимальное, среднее, максимальное и стандартное отклонение времени приёма-передачи для каждого случая.

![*Изменение файла lab_netem_i.py*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/40.png){#fig:040 width=70%}

![*График 3*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/41.png){#fig:041 width=70%}

![*Вычисленные значения*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/42.png){#fig:042 width=70%}

36. Самостоятельно реализовала воспроизводимые эксперименты по изменению значения корреляции для джиттера и задержки в эмулируемой глобальной сети. Построила графики. Вычислила минимальное, среднее, максимальное и стандартное отклонение времени приёма-передачи для каждого случая.

![*Изменение файла lab_netem_i.py*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/43.png){#fig:043 width=70%}

![*График 4*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/44.png){#fig:044 width=70%}

![*Вычисленные значения*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/45.png){#fig:045 width=70%}

37. Самостоятельно реализовала воспроизводимые эксперименты по изменению распределения времени задержки в эмулируемой глобальной сети. Построила графики. Вычислила минимальное, среднее, максимальное и стандартное отклонение времени приёма-передачи для каждого случая.

![*Изменение файла lab_netem_i.py*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/46.png){#fig:046 width=70%}

![*График 5*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/47.png){#fig:047 width=70%}

![*Вычисленные значения*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/48.png){#fig:048 width=70%}


# Выводы

Я ознакомилась с NETEM и получила навыки проведения интерактивного и воспроизводимого экспериментов по измерению задержки и её дрожания в моделируемой сети в среде Mininet.

# Список литературы{.unnumbered}

::: {#refs}
:::
