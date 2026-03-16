---
## Front matter
lang: ru-RU
title: Отчёт по лабораторной работе 8
subtitle: Адресация IPv4 и IPv6. Настройка маршрутизации
author:
  - Абрикосов Артём
institute:
  - Российский университет дружбы народов, Москва, Россия

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

Изучение принципов маршрутизации в IPv4- и IPv6-сетях и принципов настройки сетевого оборудования в среде GNS3.

# Выполнение лабораторной работы

## Топология в GNS3

![Топология сети в GNS3](Screenshot_1.png){ #fig:001 width=85% }

## Настройка IPv6 на PC1

![Настройка IPv6 на PC1](Screenshot_2.png){ #fig:002 width=85% }

## Настройка IPv6 на PC2

![Настройка IPv6 на PC2](Screenshot_3.png){ #fig:003 width=85% }

## Подготовка gw-01

![Подготовка gw-01](Screenshot_4.png){ #fig:004 width=85% }

## Адресация gw-01

![Настройка интерфейсов gw-01](Screenshot_5.png){ #fig:005 width=85% }

## Подготовка gw-02

![Подготовка gw-02](Screenshot_6.png){ #fig:006 width=85% }

## Адресация gw-02

![Настройка интерфейсов gw-02](Screenshot_7.png){ #fig:007 width=85% }

## Подготовка и адресация gw-03

![Подготовка gw-03](Screenshot_8.png){ #fig:008 width=85% }

## Подготовка и адресация gw-03

![Настройка интерфейсов gw-03](Screenshot_9.png){ #fig:009 width=85% }

## Проверка RA на оконечных устройствах

![Проверка IPv6 на PC1](Screenshot_10.png){ #fig:010 width=85% }

## Проверка RA на оконечных устройствах

![Проверка IPv6 на PC2](Screenshot_11.png){ #fig:011 width=85% }

## Ping с gw-01 до настройки маршрутизации

![Проверка связности с gw-01](Screenshot_12.png){ #fig:012 width=85% }

## Анализ трафика до RIP (gw-01 ↔ gw-03)

![Анализ трафика до RIP](Screenshot_13.png){ #fig:013 width=85% }

## Настройка RIP на gw-01

![RIP на gw-01](Screenshot_14.png){ #fig:014 width=85% }

## Настройка RIP на gw-02

![RIP на gw-02](Screenshot_15.png){ #fig:015 width=85% }

## Настройка RIP на gw-03

![RIP на gw-03](Screenshot_16.png){ #fig:016 width=85% }

## Проверка связности после включения RIP

![Проверка после RIP](Screenshot_17.png){ #fig:017 width=85% }

## Анализ трафика после RIP

![Трафик ICMP и RIP](Screenshot_18.png){ #fig:018 width=85% }

## Туннель SIT на gw-01

![Туннель SIT на gw-01](Screenshot_19.png){ #fig:019 width=85% }

## Туннель SIT на gw-02

![Туннель SIT на gw-02](Screenshot_20.png){ #fig:020 width=85% }

## Статическая маршрутизация IPv6

![Статический IPv6-маршрут на gw-01](Screenshot_21.png){ #fig:021 width=85% }

## Статическая маршрутизация IPv6

![Статический IPv6-маршрут на gw-02](Screenshot_22.png){ #fig:022 width=85% }

## Проверка с PC1: ping и trace до PC2

![PC1 → PC2: ping/trace](Screenshot_23.png){ #fig:023 width=85% }

## Проверка с PC2: ping и trace до PC1

![PC2 → PC1: ping/trace](Screenshot_24.png){ #fig:024 width=85% }

## Трафик IPv6 при передаче через IPv4

![Трафик при работе туннеля](Screenshot_25.png){ #fig:025 width=85% }

## Где видна информация о прохождении через туннель

![Инкапсуляция IPv6 в IPv4](Screenshot_26.png){ #fig:026 width=85% }

# Выводы по работе

## Вывод

В GNS3 настроена сеть с VyOS и VPCS, выполнена адресация IPv4/IPv6 и проведена проверка связности. Динамическая маршрутизация IPv4 (RIP) обеспечила доступность удалённых IPv4-сетей. Туннель SIT и статические маршруты IPv6 обеспечили обмен трафиком между удалёнными IPv6-сегментами. Анализ Wireshark подтвердил обмен ARP/ICMP/RIP и наличие инкапсуляции IPv6-пакетов внутри IPv4 при передаче через туннель.
