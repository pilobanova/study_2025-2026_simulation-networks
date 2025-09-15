---
## Front matter
lang: ru-RU
title: "Презентация по лабораторной работе №4"
subtitle: "Дисциплина: Моделирование сетей передачи данных"
author:
  - Лобанова П.И.
institute:
  - Российский университет дружбы народов, Москва, Россия
date: 15 сентября 2025

## i18n babel
babel-lang: russian
babel-otherlangs: english

## Formatting pdf
toc: false
toc-title: Содержание
slide_level: 2
aspectratio: 169
section-titles: true
theme: metropolis
header-includes:
 - \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}
 - '\makeatletter'
 - '\beamer@ignorenonframefalse'
 - '\makeatother'
---

# Информация

## Докладчик


  * Лобанова Полина Иннокентьевна
  * Учащаяся на направлении "Фундаментальная информатика и информационные технологии"
  * Студентка группы НФИбд-02-22
  * [polla-2004@mail.ru](polla-2004@mail.ru)
  

# Цель

Основной целью работы является знакомство с NETEM — инструментом для тестирования производительности приложений в виртуальной сети, а также получение навыков проведения интерактивного и воспроизводимого экспериментов по измерению задержки и её дрожания (jitter) в моделируемой сети в среде Mininet.

# Задание

1. Задайте простейшую топологию, состоящую из двух хостов и коммутатора с назначенной по умолчанию mininet сетью 10.0.0.0/8.

2. Проведите интерактивные эксперименты по добавлению/изменению задержки, джиттера, значения корреляции для джиттера и задержки, распределения времени задержки в эмулируемой глобальной сети.

3. Реализуйте воспроизводимый эксперимент по заданию значения задержки в эмулируемой глобальной сети. Постройте график. 

4. Самостоятельно реализуйте воспроизводимые эксперименты по изменению задержки, джиттера, значения корреляции для джиттера и задержки, распределения времени задержки в эмулируемой глобальной сети. Постройте графики.

# Выполнение

![*Исправление права запуска X-соединения*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/1.png){#fig:001 width=70%}

## 

![*Создание простейшей топологии*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/2.png){#fig:002 width=70%}

## 

![*Команда ifconfig на хосте h1*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/3.png){#fig:003 width=70%}

## 

![*Команда ifconfig на хосте h2*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/4.png){#fig:004 width=70%}

## 

![*Команда ping*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/5.png){#fig:005 width=70%}

## 

![*Добавление задержки на хосте h1*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/7.png){#fig:007 width=70%}

## 

![*Команда ping*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/8.png){#fig:008 width=70%}

## 

![*Добавление задержки на хосте h2*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/9.png){#fig:009 width=70%}

## 

![*Команда ping*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/10.png){#fig:010 width=70%}

## 

![*Изменение задержки*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/11.png){#fig:011 width=70%}

## 

![*Команда ping*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/12.png){#fig:012 width=70%}

## 

![*Удаление правил*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/13.png){#fig:013 width=70%}

## 

![*Команда ping*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/14.png){#fig:014 width=70%}

## 

![*Добавление задержки со случайным отклонением*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/15.png){#fig:015 width=70%}

## 

![*Команда ping*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/16.png){#fig:016 width=70%}

## 

![*Удаление правил*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/17.png){#fig:017 width=70%}

## 

![*Добавление задержки со случайным отклонением и корреляцией*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/18.png){#fig:018 width=70%}

## 

![*Команда ping*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/19.png){#fig:019 width=70%}

## 

![*Добавление нормального распределения*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/20.png){#fig:020 width=70%}

## 

![*Команда ping*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/21.png){#fig:021 width=70%}

##

![*Обновление репозиториев программного обеспечения*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/22.png){#fig:022 width=70%}

##

![*Установка пакета geeqie*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/23.png){#fig:023 width=70%}

##

![*Создание каталога*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/24.png){#fig:024 width=70%}

##

![*Создание подкаталога*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/25.png){#fig:025 width=70%}

##

![*Создание скрипта lab_netem_i.py*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/26.png){#fig:026 width=70%}

##

![*Создание скрипта ping_plot*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/27.png){#fig:027 width=70%}

##

![*Изменение прав доступа*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/28.png){#fig:028 width=70%}

##

![*Создание Makefile*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/29.png){#fig:029 width=70%}

##

![*Выполнение эксперемента*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/30.png){#fig:030 width=70%}

##

![*График 1.1*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/31.png){#fig:031 width=70%}

##

![*Удаление строки*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/32.png){#fig:032 width=70%}

##

![*График 1.2*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/33.png){#fig:033 width=70%}

##

![*Скрипт для вычисления данных*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/34.png){#fig:034 width=70%}

##

![*Изменение Makefile*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/35.png){#fig:035 width=70%}

##

![*Результат работы скрипта*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/36.png){#fig:036 width=70%}

##

![*Изменение файла lab_netem_i.py*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/37.png){#fig:037 width=70%}

##

![*График 2*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/38.png){#fig:038 width=70%}

##

![*Вычисленные значения*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/39.png){#fig:039 width=70%}

##

![*Изменение файла lab_netem_i.py*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/40.png){#fig:040 width=70%}

##

![*График 3*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/41.png){#fig:041 width=70%}

##

![*Вычисленные значения*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/42.png){#fig:042 width=70%}

##

![*Изменение файла lab_netem_i.py*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/43.png){#fig:043 width=70%}

##

![*График 4*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/44.png){#fig:044 width=70%}

##

![*Вычисленные значения*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/45.png){#fig:045 width=70%}

##

![*Изменение файла lab_netem_i.py*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/46.png){#fig:046 width=70%}

##

![*График 5*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/47.png){#fig:047 width=70%}

##

![*Вычисленные значения*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab04/report/image/лаб4/48.png){#fig:048 width=70%}

# Вывод

Я ознакомилась с NETEM и получила навыки проведения интерактивного и воспроизводимого экспериментов по измерению задержки и её дрожания в моделируемой сети в среде Mininet.




