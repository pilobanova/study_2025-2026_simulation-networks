---
## Front matter
lang: ru-RU
title: "Презентация по лабораторной работе №2"
subtitle: "Дисциплина: Моделирование сетей передачи данных"
author:
  - Лобанова П.И.
institute:
  - Российский университет дружбы народов, Москва, Россия
date: 11 сентября 2025

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

Основной целью работы является знакомство с инструментом для измерения пропускной способности сети в режиме реального времени — iPerf3, а также получение навыков проведения интерактивного эксперимента по измерению пропускной способности моделируемой сети в среде Mininet.

# Задание

1. Установить на виртуальную машину mininet iPerf3 и дополнительное программное обеспечения для визуализации и обработки данных.

2. Провести ряд интерактивных экспериментов по измерению пропускной способности с помощью iPerf3 с построением графиков.

# Выполнение

![*Подключение к виртуальной машине*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab02/report/image/лаб2/1.png){#fig:001 width=70%}

## 

![*IP-адреса машины*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab02/report/image/лаб2/2.png){#fig:002 width=70%}

## 

![*Обновление репозитории программного обеспечения*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab02/report/image/лаб2/3.png){#fig:003 width=70%}

## 

![*Установка iperf3*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab02/report/image/лаб2/4.png){#fig:004 width=70%}

## 

![*Установка необходимого дополнительного программного обеспечения*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab02/report/image/лаб2/5.png){#fig:005 width=70%}

## 

![*Скачивание репозитория*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab02/report/image/лаб2/6.png){#fig:006 width=70%}

## 

![*Установка iperf3_plotter*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab02/report/image/лаб2/7.png){#fig:007 width=70%}

## 

![*Простейшая топология*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab02/report/image/лаб2/8.png){#fig:008 width=70%}

## 

![*Параметры запущенной топологии*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab02/report/image/лаб2/9.png){#fig:009 width=70%}

## 

![*Запуск сервера iPerf3*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab02/report/image/лаб2/10.png){#fig:010 width=70%}

## 

![*Запуск клиента iPerf3*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab02/report/image/лаб2/11.png){#fig:011 width=70%}

## 

![*Запуск клиента iPerf3*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab02/report/image/лаб2/13.png){#fig:013 width=70%}

## 

![*Остановка серверного процесса*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab02/report/image/лаб2/14.png){#fig:014 width=70%}

## 

![*Запуск сервера iPerf3*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab02/report/image/лаб2/15.png){#fig:015 width=70%}


## 

![*Запуск клиента iPerf3*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab02/report/image/лаб2/16.png){#fig:016 width=70%}

## 

![*Запуск сервера iPerf3*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab02/report/image/лаб2/17.png){#fig:017 width=70%}

## 

![*Запуск клиента iPerf3*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab02/report/image/лаб2/18.png){#fig:018 width=70%}

## 

![*Запуск клиента iPerf3*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab02/report/image/лаб2/19.png){#fig:019 width=70%}

## 

![*Запуск клиента iPerf3*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab02/report/image/лаб2/20.png){#fig:020 width=70%}

## 

![*Запуск сервера iPerf3*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab02/report/image/лаб2/21.png){#fig:021 width=70%}

## 

![*Запуск клиента iPerf3*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab02/report/image/лаб2/22.png){#fig:022 width=70%}

## 

![*Запуск сервера iPerf3*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab02/report/image/лаб2/23.png){#fig:023 width=70%}

## 

![*Запуск клиента iPerf3*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab02/report/image/лаб2/24.png){#fig:024 width=70%}

## 

![*Создание каталога*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab02/report/image/лаб2/25.png){#fig:025 width=70%}

##

![*Запуск клиента iPerf3*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab02/report/image/лаб2/26.png){#fig:026 width=70%}

##

![*Запуск клиента iPerf3*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab02/report/image/лаб2/27.png){#fig:027 width=70%}

##

![*Просмотр каталога*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab02/report/image/лаб2/28.png){#fig:028 width=70%}

##

![*Исправление прав*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab02/report/image/лаб2/29.png){#fig:029 width=70%}

##

![*Корректировка прав*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab02/report/image/лаб2/30.png){#fig:030 width=70%}

##

![*Генерация выходных файлов*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab02/report/image/лаб2/31.png){#fig:031 width=70%}

##

![*Просмотр каталога*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab02/report/image/лаб2/32.png){#fig:032 width=70%}

# Вывод

Я ознакомилась с инструментом для измерения пропускной способности сети в режиме реального времени — iPerf3, а также получила навыков проведения интерактивного эксперимента по измерению пропускной способности моделируемой сети в среде Mininet.


