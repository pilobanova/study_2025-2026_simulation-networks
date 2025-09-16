---
## Front matter
lang: ru-RU
title: "Презентация по лабораторной работе №5"
subtitle: "Дисциплина: Моделирование сетей передачи данных"
author:
  - Лобанова П.И.
institute:
  - Российский университет дружбы народов, Москва, Россия
date: 16 сентября 2025

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

Основной целью работы является получение навыков проведения интерактивных экспериментов в среде Mininet по исследованию параметров сети, связанных с потерей, дублированием, изменением порядка и повреждением пакетов при передаче данных. Эти параметры влияют на производительность протоколов и сетей.

# Задание

1. Задайте простейшую топологию, состоящую из двух хостов и коммутатора с назначенной по умолчанию mininet сетью 10.0.0.0/8.

2. Проведите интерактивные эксперименты по по исследованию параметров сети, связанных с потерей, дублированием, изменением порядка и повреждением пакетов при передаче данных.

3. Реализуйте воспроизводимый эксперимент по добавлению правила отбрасывания пакетов в эмулируемой глобальной сети. На экран выведите сводную информацию о потерянных пакетах. 

4. Самостоятельно реализуйте воспроизводимые эксперименты по исследованию параметров сети, связанных с потерей, изменением порядка и повреждением пакетов при передаче данных. На экран выведите сводную информацию о потерянных пакетах.

# Выполнение

![*Изменение прав запуска X-соединения. *](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab05/report/image/лаб5/1.png){#fig:001 width=70%}

## 

![*Создание топологии*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab05/report/image/лаб5/2.png){#fig:002 width=70%}

## 

![*Команда ifconfig на хосте h1*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab05/report/image/лаб5/3.png){#fig:003 width=70%}

## 

![*Команда ifconfig на хосте h2*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab05/report/image/лаб5/4.png){#fig:004 width=70%}

## 

![*Пингование*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab05/report/image/лаб5/5.png){#fig:005 width=70%}

## 

![*Добавление процента потерь*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab05/report/image/лаб5/6.png){#fig:006 width=70%}

## 

![*Пингование*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab05/report/image/лаб5/8.png){#fig:008 width=70%}

## 

![*Добавление процента потерь*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab05/report/image/лаб5/9.png){#fig:009 width=70%}

## 

![*Пингование*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab05/report/image/лаб5/11.png){#fig:011 width=70%}

## 

![*Восстановление конфигурации*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab05/report/image/лаб5/12.png){#fig:012 width=70%}

## 

![*Пингование*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab05/report/image/лаб5/13.png){#fig:013 width=70%}

## 

![*Добавление коэффициента потерь с корреляцией*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab05/report/image/лаб5/14.png){#fig:014 width=70%}

## 

![*Пингование*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab05/report/image/лаб5/15.png){#fig:015 width=70%}

## 

![*Добавление повреждения*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab05/report/image/лаб5/16.png){#fig:016 width=70%}

## 

![*Запуск сервера*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab05/report/image/лаб5/17.png){#fig:017 width=70%}

## 

![*Запуск клента*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab05/report/image/лаб5/18.png){#fig:018 width=70%}

## 

![*Добавление переупорядочивания пакетов*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab05/report/image/лаб5/19.png){#fig:019 width=70%}

## 

![*Пингование*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab05/report/image/лаб5/20.png){#fig:020 width=70%}

## 

![*Добавление дублирования*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab05/report/image/лаб5/21.png){#fig:021 width=70%}

##

![*Пингование*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab05/report/image/лаб5/22.png){#fig:022 width=70%}

##

![*Создание каталога*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab05/report/image/лаб5/23.png){#fig:023 width=70%}

##

![*Создание подкаталога*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab05/report/image/лаб5/24.png){#fig:024 width=70%}

##

![*Скрипт lab_netem_ii.py*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab05/report/image/лаб5/25.png){#fig:025 width=70%}

##

![*Изменение в скрипте lab_netem_ii.py*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab05/report/image/лаб5/26.png){#fig:026 width=70%}

##

![*Создание Makefile*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab05/report/image/лаб5/27.png){#fig:027 width=70%}

##

![*Выполнение эксперимента*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab05/report/image/лаб5/28.png){#fig:028 width=70%}

##

![*Добавление коэффициента потерь с корреляцией*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab05/report/image/лаб5/29.png){#fig:029 width=70%}

##

![*Выполнение эксперимента*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab05/report/image/лаб5/30.png){#fig:030 width=70%}

##

![*Добавление повреждения*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab05/report/image/лаб5/31.png){#fig:031 width=70%}

##

![*Выполнение эксперимента*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab05/report/image/лаб5/32.png){#fig:032 width=70%}

##

![*Добавление переупорядочивания пакетов*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab05/report/image/лаб5/33.png){#fig:033 width=70%}

##

![*Выполнение эксперимента*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab05/report/image/лаб5/34.png){#fig:034 width=70%}

##

![*Добавление дублирования*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab05/report/image/лаб5/35.png){#fig:035 width=70%}

##

![*Выполнение эксперимента*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab05/report/image/лаб5/36.png){#fig:036 width=70%}

# Вывод

Я получила навыки проведения интерактивных экспериментов в среде Mininet по исследованию параметров сети, связанных с потерей, дублированием, изменением порядка и повреждением пакетов при передаче данных. 


