---
## Front matter
lang: ru-RU
title: "Презентация по лабораторной работе №1"
subtitle: "Дисциплина: Моделирование сетей передачи данных"
author:
  - Лобанова П.И.
institute:
  - Российский университет дружбы народов, Москва, Россия
date: 10 сентября 2025

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

Основной целью работы является развёртывание в системе виртуализации (например, в VirtualBox) mininet, знакомство с основными командами для работы с Mininet через командную строку через графический интерфейс.

# Задание

1. Выполнить настройку стенда виртуальной машины Mininet.

2. Выполнить работу с Mininet с помощью командной строки.

3. Выполнить построение и эмуляции сети в Mininet с использованием графического интерфейса.

# Выполнение

![*Импортирование файла*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/1.png){#fig:001 width=70%}

## 

![*Изменение графического контроллера*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/2.png){#fig:002 width=70%}

## 

![*Изменение первого адаптера*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/3.png){#fig:003 width=50%}

 

![*Изменение второго адаптера*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/4.png){#fig:004 width=50%}

## 

![*Запуск виртуальной машины*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/5.png){#fig:005 width=70%}

## 

![*Вход в виртуальную машину*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/6.png){#fig:006 width=70%}

## 

![*Адрес машины*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/7.png){#fig:007 width=70%}

## 

![*Подключение к виртуальной машине*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/8.png){#fig:008 width=70%}

## 

![*Настройка ssh-подсоединения по ключу*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/9.png){#fig:009 width=70%}

## 

![*IP-адреса машины*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/10.png){#fig:010 width=70%}

## 

![*Активация второго интерфейса*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/11.png){#fig:011 width=70%}

## 

![*Установка mc*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/12.png){#fig:012 width=70%}

## 

![*Открытие файла*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/13.png){#fig:013 width=70%}



![*Изменения в файле /etc/netplan/01-netcfg.yaml*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/14.png){#fig:014 width=50%}


## 

![*Переименовывание предыдущей установки Mininet*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/15.png){#fig:015 width=70%}

## 

![*Скачивание новой версии Mininet*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/16.png){#fig:016 width=70%}

## 

![*Обновление исполняемых файлов*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/17.png){#fig:017 width=70%}

## 

![*Версия Mininet*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/18.png){#fig:018 width=70%}

## 

![*Открытие файла*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/19.png){#fig:019 width=70%}



![*Изменения в файле /etc/X11/app-defaults/XTerm*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/20.png){#fig:020 width=50%}

##

![*Копирование значения куки пользователя mininet в файл для пользователя root*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/21.png){#fig:021 width=70%}

##

![*Запуск минимальной топологии*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/22.png){#fig:022 width=70%}

##

![*Команда help*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/23.png){#fig:023 width=70%}

##

![*Доступные узлы и линки*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/24.png){#fig:024 width=70%}

##

![*Интерфейсы хоста h1*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/25.png){#fig:025 width=70%}

##

![*Интерфейсы хоста h2 *](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/26.png){#fig:026 width=70%}

##

![*Интерфейсы хоста s1*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/27.png){#fig:027 width=70%}

##

![*Пингование*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/28.png){#fig:028 width=70%}

##

![*Запуск MiniEdit*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/29.png){#fig:029 width=70%}

##

![*Схема сети*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/30.png){#fig:030 width=70%}

##

![*IP-адрес на хосте h1*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/31.png){#fig:031 width=70%}

##

![*IP-адрес на хосте h2*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/32.png){#fig:032 width=70%}

##

![*IP-адреса на хосте h1*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/35.png){#fig:033 width=70%}

##

![*IP-адреса на хосте h2*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/36.png){#fig:034 width=70%}

##

![*Пингование*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/37.png){#fig:035 width=70%}

##

![*Изменение базового значения IP-адресов*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/38.png){#fig:036 width=70%}

##

![*IP-адреса на хосте h1*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/39.png){#fig:037 width=70%}

##

![*Создание каталога*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/40.png){#fig:038 width=70%}

##

![*Сохранение топологии*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/41.png){#fig:039 width=70%}

##

![*Изменение прав доступа*](/home/pilobanova/work/study/2025-2026/Моделирование сетей передачи данных/simulation-networks/labs/lab01/report/image/лаб1/42.png){#fig:040 width=70%}

# Выводы

Я выполнила развёртывание в системе виртуализации mininet и ознакомилась с основными командами для работы с Mininet через командную строку через графический интерфейс.





