---
## Front matter
lang: ru-RU
title: Отчёт по лабораторной работе 5
subtitle: Простые сети в GNS3. Анализ трафика
author:
  - Абрикосов Артём
institute:
  - Российский университет дружбы народов, Москва, Россия
date: 13 января 2025

## i18n babel
babel-lang: russian
babel-otherlangs: english

## Formatting pdf
toc: false
slide_level: 2
aspectratio: 169
section-titles: true
theme: metropolis
header-includes:
 - \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}
---

# Цели и задачи работы

## Цель лабораторной работы

Построение простейших моделей сети на базе коммутатора и маршрутизаторов FRR и VyOS в GNS3, анализ трафика посредством Wireshark.

# Выполнение лабораторной работы

## Справка по командам VPCS

![Просмотр списка команд VPCS](Screenshot_1.png){ #fig:001 width=80% }

## Справка по настройке IP

![Просмотр синтаксиса команды ip](Screenshot_2.png){ #fig:002 width=80% }

## Настройка IP-адреса PC1

![Настройка IP-адреса PC1 и проверка параметров](Screenshot_3.png){ #fig:003 width=80% }

## Проверка связности PC1 ↔ PC2

![Проверка связи между PC1 и PC2](Screenshot_4.png){ #fig:004 width=80% }

## ARP-сообщения (gratuitous ARP)

![Анализ ARP-сообщений в Wireshark](Screenshot_5.png){ #fig:005 width=80% }

## Опции ping в VPCS

![Просмотр параметров команды ping](Screenshot_6.png){ #fig:006 width=80% }

## Выполнение ping с PC2

![Выполнение ping](Screenshot_7.png){ #fig:007 width=80% }

## ICMP Echo Request/Reply

![Анализ ICMP Echo-запроса и ответа](Screenshot_8.png){ #fig:008 width=80% }

## UDP mode (Echo over UDP)

![Анализ UDP Echo-пакета](Screenshot_9.png){ #fig:009 width=80% }

## TCP mode (Echo over TCP)

![Анализ TCP-соединения и передачи данных](Screenshot_10.png){ #fig:010 width=80% }

## Топология: VPCS — Switch — FRR

![Топология сети с маршрутизатором FRR](Screenshot_11.png){ #fig:011 width=80% }

## Настройка IP на PC1 (192.168.1.10/24)

![Настройка IP-адреса PC1 и проверка параметров](Screenshot_12.png){ #fig:012 width=80% }

## Настройка eth0 на FRR (192.168.1.1/24)

![Настройка интерфейса eth0 маршрутизатора FRR](Screenshot_13.png){ #fig:013 width=80% }

## Проверка конфигурации FRR

![Проверка конфигурации и состояния интерфейсов маршрутизатора](Screenshot_14.png){ #fig:014 width=80% }

## Проверка связности PC1 → FRR (192.168.1.1)

![Проверка связи между PC1 и маршрутизатором](Screenshot_15.png){ #fig:015 width=80% }

## ICMP/ARP в Wireshark (PC1 ↔ FRR)

![Анализ ICMP-трафика между PC1 и маршрутизатором](Screenshot_16.png){ #fig:016 width=80% }

# Моделирование сети на базе VyOS

## Топология: VPCS — Switch — VyOS

![Топология сети с маршрутизатором VyOS](Screenshot_17.png){ #fig:017 width=80% }

## Настройка интерфейса eth0 на VyOS (192.168.1.1/24)

![Настройка интерфейса eth0 маршрутизатора VyOS](Screenshot_18.png){ #fig:018 width=80% }

## Проверка связности PC1 → VyOS (192.168.1.1)

![Проверка связи между PC1 и маршрутизатором VyOS](Screenshot_19.png){ #fig:019 width=80% }

## ICMP/ARP в Wireshark (PC1 ↔ VyOS)

![Анализ ICMP-трафика между PC1 и маршрутизатором](Screenshot_20.png){ #fig:020 width=80% }

# Выводы по работе

## Вывод

В ходе выполнения лабораторной работы были смоделированы простейшие сети в GNS3 на базе коммутатора Ethernet и маршрутизаторов FRR и VyOS. Выполнена статическая настройка IP-адресации в подсети 192.168.1.0/24 и проверена связность между узлами с использованием ICMP эхо-запросов.

С помощью Wireshark были захвачены и проанализированы ARP- и ICMP-сообщения, а также особенности формирования трафика при выполнении ping в режимах ICMP/UDP/TCP. Поставленные задачи выполнены в полном объёме.
