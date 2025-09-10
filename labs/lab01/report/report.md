---
## Front matter
title: "Отчет по лабораторной работе №1"
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

Основной целью работы является развёртывание в системе виртуализации (например, в VirtualBox) mininet, знакомство с основными командами для работы с Mininet через командную строку через графический интерфейс.

# Задание

1. Выполнить настройку стенда виртуальной машины Mininet.

2. Выполнить работу с Mininet с помощью командной строки.

3. Выполнить построение и эмуляции сети в Mininet с использованием графического интерфейса.

# Выполнение лабораторной работы

1. Скачала актуальный релиз ovf-образа виртуальной машины. Переместила скачанный образ в каталог для работы,
затем распаковала его. Запустила систему виртуализации и импортировала файл .ovf.

![*Импортирование файла*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/1.png){#fig:001 width=70%}

2. Перешла в настройки системы виртуализации и уточнила параметры настройки виртуальной машины. Изменила тип графического контроллера на рекомендуемый. В настройках сети первый адаптер имеет подключение типа NAT. Для второго адаптера указала тип подключения host-only network adapter (виртуальный адаптер хоста).

![*Изменение графического контроллера*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/2.png){#fig:002 width=70%}

![*Изменение первого адаптера*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/3.png){#fig:003 width=70%}

![*Изменение второго адаптера*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/4.png){#fig:004 width=70%}

3. Запустила виртуальную машину с Mininet.

![*Запуск виртуальной машины*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/5.png){#fig:005 width=70%}

4. Залогинилась в виртуальной машине.

![*Вход в виртуальную машину*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/6.png){#fig:006 width=70%}

5. Посмотрела адрес машины.

![*Адрес машины*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/7.png){#fig:007 width=70%}

6. Подключилась к виртуальной машине.

![*Подключение к виртуальной машине*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/8.png){#fig:008 width=70%}

7. Настроила ssh-подсоединение по ключу к виртуальной машине. Вновь подключилась к виртуальной машине и убедилась, что подсоединение происходит успешно и без ввода пароля.

![*Настройка ssh-подсоединения по ключу*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/9.png){#fig:009 width=70%}

8. После подключения к виртуальной машине mininet посмотрела IP-адреса машины.

![*IP-адреса машины*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/10.png){#fig:010 width=70%}

9. Для доступа к сети Интернет должен быть активен адрес NAT: 10.0.0.x. У меня был активен только внутренний адрес машины вида 192.168.x.y, поэтому я активировала второй интерфейс.

![*Активация второго интерфейса*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/11.png){#fig:011 width=70%}

10. Для удобства дальнейшей работы установила mc.

![*Установка mc*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/12.png){#fig:012 width=70%}

11. Для удобства дальнейшей работы добавила для mininet указание на использование двух адаптеров при запуске. Для этого перешла в режим суперпользователя и внесла изменения в файл /etc/netplan/01-netcfg.yaml.

![*Открытие файла*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/13.png){#fig:013 width=70%}

![*Изменения в файле /etc/netplan/01-netcfg.yaml*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/14.png){#fig:014 width=70%}

12. В виртуальной машине mininet переименовала предыдущую установку Mininet.

![*Переименовывание предыдущей установки Mininet*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/15.png){#fig:015 width=70%}

13. Скачала новую версию Mininet.

![*Скачивание новой версии Mininet*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/16.png){#fig:016 width=70%}

14. Обновила исполняемые файлы.

![*Обновление исполняемых файлов*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/17.png){#fig:017 width=70%}

15. Проверила номер установленной версии mininet.

![*Версия Mininet*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/18.png){#fig:018 width=70%}

16. Для увеличения размера шрифта и применения векторных шрифтов вместо растровых внесла изменения в файл /etc/X11/app-defaults/XTerm.

![*Открытие файла*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/19.png){#fig:019 width=70%}

![*Изменения в файле /etc/X11/app-defaults/XTerm*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/20.png){#fig:020 width=70%}

17. Скопировала значение куки пользователя mininet в файл для пользователя root. После выполнения этих действий графические приложения должны запускаться под пользователем mininet.

![*Копирование значения куки пользователя mininet в файл для пользователя root*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/21.png){#fig:021 width=70%}

18. Запустила минимальную топологию.

![*Запуск минимальной топологии*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/22.png){#fig:022 width=70%}

19. Отобразила список команд интерфейса командной строки Mininet и примеров их использования.

![*Команда help*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/23.png){#fig:023 width=70%}

20. Отобразила доступные узлы и линки.

![*Доступные узлы и линки*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/24.png){#fig:024 width=70%}

21. Посмотрела интерфейсы хоста h1 — хост h1 имеет интерфейс h1-eth0, настроенный с IP-адресом 10.0.0.1, и другой интерфейс lo, настроенный с IP-адресом 127.0.0.1.

![*Интерфейсы хоста h1*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/25.png){#fig:025 width=70%}

22. Посмотрела интерфейсы хоста h2 — хост h2 имеет интерфейс h2-eth0, настроенный с IP-адресом 10.0.0.2, и другой интерфейс lo, настроенный с IP-адресом 127.0.0.1.

![*Интерфейсы хоста h2 *](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/26.png){#fig:026 width=70%}

23. Посмотрела интерфейсы хоста s1 — хост s1 имеет интерфейс s1-eth0, настроенный с IP-адресом 192.168.56.103, интерфейс s1-eth1, настроенный с IP-адресом 10.0.2.15, и другой интерфейс lo, настроенный с IP-адресом 127.0.0.1.

![*Интерфейсы хоста s1*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/27.png){#fig:027 width=70%}

24. Чтобы проверить связь между узлами, использовала команду ping.

![*Пингование*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/28.png){#fig:028 width=70%}

25. Остановила эмуляцию.

26. В терминале виртуальной машины mininet запустила MiniEdit.

![*Запуск MiniEdit*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/29.png){#fig:029 width=70%}

27. Добавила два хоста и один коммутатор, соединила хосты с коммутатором.

![*Схема сети*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/30.png){#fig:030 width=70%}

28. Настроила IP-адреса на хостах h1 и h2. Для хоста h1 указала IP-адрес 10.0.0.1/8, а для хоста h2 — 10.0.0.2/8.

![*IP-адрес на хосте h1*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/31.png){#fig:031 width=70%}

![*IP-адрес на хосте h2*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/32.png){#fig:032 width=70%}

29. Запустила эмуляцию. Открыла терминал на хосте h1 и ввела команду ifconfig, чтобы отобразить назначенные ему IP-адреса.

![*IP-адреса на хосте h1*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/35.png){#fig:033 width=70%}

30. Повторила эти действия на хосте h2.

![*IP-адреса на хосте h2*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/36.png){#fig:034 width=70%}

31. Проверила соединение между хостами.

![*Пингование*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/37.png){#fig:035 width=70%}

32. Остановила эмуляцию.

33. Удалила назначенный вручную IP-адрес с хостов h1 и h2.

34. В MiniEdit нажала Edit > Preferences. По умолчанию в поле базовые значения IP-адресов (IP Base) установлено 10.0.0.0/8. Изменила это значение на 15.0.0.0/8.

![*Изменение базового значения IP-адресов*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/38.png){#fig:036 width=70%}

35. Запустила эмуляцию. Открыла терминал на хосте h1 и отобразила IP-адреса, назначенные хосту h1.

![*IP-адреса на хосте h1*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/39.png){#fig:037 width=70%}

36. Остановила эмуляцию. В домашнем каталоге виртуальной машины mininet создала каталог для работы с проектами mininet.

![*Создание каталога*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/40.png){#fig:038 width=70%}

37. Для сохранения топологии сети в файл нажала в MiniEdit File > Save. Указала имя для топологии и сохранила на своём компьютере. 

![*Сохранение топологии*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/41.png){#fig:039 width=70%}

38. После сохранения проекта поменяла права доступа к файлам в каталоге проекта.

![*Изменение прав доступа*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/42.png){#fig:040 width=70%}

39. Завершила соединение с виртуальной машиной mininet и выключила её.




# Выводы

Я выполнила развёртывание в системе виртуализации mininet и ознакомилась с основными командами для работы с Mininet через командную строку через графический интерфейс.

# Список литературы{.unnumbered}

::: {#refs}
:::
