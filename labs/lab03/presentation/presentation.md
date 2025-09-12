---
## Front matter
lang: ru-RU
title: "Презентация по лабораторной работе №3"
subtitle: "Дисциплина: Моделирование сетей передачи данных"
author:
  - Лобанова П.И.
institute:
  - Российский университет дружбы народов, Москва, Россия
date: 12 сентября 2025

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

Основной целью работы является знакомство с инструментом для измерения пропускной способности сети в режиме реального времени — iPerf3, а также получение навыков проведения воспроизводимого эксперимента по измерению пропускной способности моделируемой сети в среде Mininet.

# Задание

1. Воспроизвести посредством API Mininet эксперименты по измерению пропускной способности с помощью iPerf3.

2. Построить графики по проведённому эксперименту.

# Выполнение

![*Создание каталога и копирование файла*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab03/report/image/лаб3/1.png){#fig:001 width=70%}

## 

![*Скрипт lab_iperf3_topo.py*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab03/report/image/лаб3/2.png){#fig:002 width=70%}

## 

![*Запуск скрипта*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab03/report/image/лаб3/3.png){#fig:003 width=70%}

## 

![*Элементы топологии*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab03/report/image/лаб3/4.png){#fig:004 width=70%}

## 

![*Внесение изменений в скрипт*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab03/report/image/лаб3/5.png){#fig:005 width=70%}

## 

![*Запуск скрипта*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab03/report/image/лаб3/6.png){#fig:006 width=70%}

## 

![*Внесение изменений в скрипт*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab03/report/image/лаб3/7.png){#fig:007 width=70%}

## 

![*Запуск скрипта*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab03/report/image/лаб3/8.png){#fig:008 width=70%}

## 

![*Внесение изменений в скрипт*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab03/report/image/лаб3/9.png){#fig:009 width=70%}

## 

![*Внесение изменений в скрипт*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab03/report/image/лаб3/10.png){#fig:010 width=70%}

## 

![*Внесение изменений в скрипт*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab03/report/image/лаб3/11.png){#fig:011 width=70%}

## 

![*Внесение изменений в скрипт*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab03/report/image/лаб3/12.png){#fig:012 width=70%}

## 

![*Внесение изменений в скрипт*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab03/report/image/лаб3/13.png){#fig:013 width=70%}

## 

![*Внесение изменений в скрипт*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab03/report/image/лаб3/14.png){#fig:014 width=70%}

## 

![*Запуск скрипта*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab03/report/image/лаб3/15.png){#fig:015 width=70%}

## 

![*Создание подкаталога и копирование скрипта*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab03/report/image/лаб3/16.png){#fig:016 width=70%}

## 

![*Внесение изменений в скрипт*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab03/report/image/лаб3/17.png){#fig:017 width=70%}

## 

![*Внесение изменений в скрипт*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab03/report/image/лаб3/18.png){#fig:018 width=70%}

## 

![*Внесение изменений в скрипт*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab03/report/image/лаб3/19.png){#fig:019 width=70%}

## 

![*Запуск скрипта*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab03/report/image/лаб3/20.png){#fig:020 width=50%}

##

![*Построение графиков*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab03/report/image/лаб3/21.png){#fig:021 width=70%}

##

![*Написание скрипта Makefile*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab03/report/image/лаб3/22.png){#fig:022 width=70%}

##

![*Запуск скрипта Makefile*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab03/report/image/лаб3/23.png){#fig:023 width=60%}

# Вывод

Я ознакомилась с инструментом для измерения пропускной способности сети в режиме реального времени — iPerf3, а также
получила навыки проведения воспроизводимого эксперимента по измерению пропускной способности моделируемой сети в среде Mininet.
