**ПРЗ 6.2 Контроль целостности**

Выполнил
Студент 1 курса

Группы ББМО-01-23 

Белов Владимир Станиславович

Шифр 23Б1716


Задание 1
1. Настройка протокола GRE в Packet Tracer согласно предоставленным
исходным и заданию.
2. Подготовка собственных исходных данных и настройка протокола GRE.

Исходные данные:

![image](https://github.com/V0vochka/Praktika-6/assets/70959108/14375ae4-1c38-4b2b-ac36-69e9a6faa87f)

![image](https://github.com/V0vochka/Praktika-6/assets/70959108/4532cf46-0a66-431f-94a9-0f387aa12f72)

**Задача 1: Проверка связи между маршрутизаторами**
1) Определим IP-адреса порта S0/0/0 на маршрутизаторе RA используя команду show ip interface brief

![image](https://github.com/V0vochka/Praktika-6/assets/70959108/848dbc1b-02ed-4606-992d-3b56a07fa03b)

2)Отправим с маршрутизатора RB эхо-запрос на IP-адрес интерфейса S0/0/0 маршрутизатора RA.

![image](https://github.com/V0vochka/Praktika-6/assets/70959108/c761dfde-0552-40ba-a5e5-7ad759268346)

3) Отправим эхо с ПК B на ПК A
   Узнаем IP адрес ПК A

![image](https://github.com/V0vochka/Praktika-6/assets/70959108/6e7b15be-177d-4fc3-8c06-dab16384fc1d)

Отправляем эхо-запрос с ПК B на ПК A.

![image](https://github.com/V0vochka/Praktika-6/assets/70959108/cc4b6943-9add-4142-b596-f2d866adadc7)

**Задача 2: Настройка туннелей GRE**

1) Настроим интерфейс туннеля 0 на маршрутизаторе RA
   
![image](https://github.com/V0vochka/Praktika-6/assets/70959108/6e27cd98-2ad1-4417-9080-a403335cdb95)

2) Настроим интерфейс туннеля 0 на маршрутизаторе RB

![image](https://github.com/V0vochka/Praktika-6/assets/70959108/ca62e506-4bab-49ae-8eb0-23abac350fa2)

3) Настроим маршрут для частного трафика IP. Создадим маршрут между сетями 192.168.X.X, используя в качестве назначения сеть 10.10.10.0/30.
   RA(config)# ip route 192.168.2.0 255.255.255.0 10.10.10.2
   
   ![image](https://github.com/V0vochka/Praktika-6/assets/70959108/a7de26b8-b598-4444-955b-7549c379449e)

   RB(config)# ip route 192.168.1.0 255.255.255.0 10.10.10.1

   ![image](https://github.com/V0vochka/Praktika-6/assets/70959108/9da21828-96d6-4f91-9536-f7c534fd132c)

   **Задача 3: Проверка связи между маршрутизаторами**

   1)Отправим эхо-запрос с ПК B на IP-адрес компьютера ПК A.

   ![image](https://github.com/V0vochka/Praktika-6/assets/70959108/a4ea8b8c-6e0c-4fba-9fe9-53ada26d79f0)

   Сделаем трассировку от ПК A до ПК B.

   ![image](https://github.com/V0vochka/Praktika-6/assets/70959108/7fd71b8b-df23-4f38-b7ef-cb736c6044c6)

   Обратите внимание на отсутствие в результатах публичных IP-адресов.

   Задание выполнено:
   
   ![image](https://github.com/V0vochka/Praktika-6/assets/70959108/e1f531ad-16d6-4555-9f14-27519a58dd7c)





