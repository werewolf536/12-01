# Домашнее задание к занятию «Базы данных» - Стрельцов Владимир

Легенда
Заказчик передал вам файл в формате Excel, в котором сформирован отчёт.

На основе этого отчёта нужно выполнить следующие задания.

Задание 1
Опишите не менее семи таблиц, из которых состоит база данных:

какие данные хранятся в этих таблицах;
какой тип данных у столбцов в этих таблицах, если данные хранятся в PostgreSQL.
Приведите решение к следующему виду:

Сотрудники (

идентификатор, первичный ключ, serial,
фамилия varchar(50),
...
идентификатор структурного подразделения, внешний ключ, integer).


## Таблица  1 – Сотрудники

```
сотрудник_id, primary key, smallserial
ФИО, varchar(50);
Дата_найма, mediumint
оклад_id, foreign key, tinyint
структурное_подразделение_id, foreign key, tinyint
проект_id, foreign key, tinyint
```

## Таблица 2 – Оклады

```
Оклад_id, primary key, tinyint
Оклад, salary DECIMAL(8,2)
```

## Таблица 3 – Должность

```
Должность_id, primary key, tinyint
Должность, varchar(40)
```

## Таблица  4 - Тип подразделения

```
тип_подразделения_id, primary key, tinyint
тип_подразделения, varchar(15)
```

## Таблица 5 - Структурное подразделение

```
структурное_подразделение_id, primary key, tinyint
тип_подразделения, varchar(50)
адрес_филиала_id, foreign key, tinyint 
тип_подразделения_id, foreign key, tinyint
```

## Таблица 6 - Адрес филиала

```
адрес_филиала_id, primary key, tinyint
адрес_филиала, varchar(100)
```

## Таблица 7 – Проект

```
проект_id, primary key, tinyint
проект, varchar(70)
```


