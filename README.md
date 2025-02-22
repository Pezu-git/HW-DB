# Базы данных, их типы

## Задание №1. СУБД

### 1.1

Для бюджетирования проектов, формирования финансовых аналитических отчётов и прогнозирования рисков, когда важна целостность и чёткая структура данных, подойдёт реляционная модель СУБД: PostgeSQL, MySQL, Microsoft SQL Server.
Она позволяет обеспечивать безопасное и надёжное управление элементами данных «проект-заказчик-финансирование» на основе правил целостности.

### 1.2

Для лендингов и CRM лучше всего использовать реляционные СУБД, такие как MySQL или PostgreSQL. Они обеспечивают гибкость и скорость работы с данными, а также имеют широкий спектр функций для управления и анализа информации.

### 1.3

Для создания базы данных, которая будет соответствовать всем предъявленным выше требованиям, можно выбрать реляционные системы управления базами данных, такие как MySQL или PostgreSQL. Оба эти решения имеют простой и понятный интерфейс, позволяющий легко создавать базы данных с нужной структурой. Кроме того, они обладают высокой производительностью и надежностью, что важно для хранения корпоративных данных. Также можно реализовать на NoSQL СУБД, если хранить данные не ввиде таблиц, а в виде документов либо коллекций.

### 1.4

Для решения этих задач можно использовать СУБД, такую как PostgreSQL или Oracle. Эти СУБД позволяют быстро работать со сложными связями между объектами и эффективно распределять ресурсы. Можно подключить отдел закупок к СУБД PostgreSQL или Oracle. Обе эти СУБД предоставляют широкие возможности для создания и управления базами данных, которые могут быть использованы в разных отделах компании, включая отдел закупок.

## Задание №2. Транзакции

### 2.1

1. Пользователь вводит номер своего телефона и сумму пополнения на сайте оператора или в мобильном приложении.
2. Данные отправляются на сервер оператора, проверка доступности суммы для пополнения на счете пользователя.
3. В случае успеха, отправляется запрос на подтверждение транзакции на телефон пользователя.
4. Подтвержддение транзакции пользователем - ввод секретного кода, отправленного оператором.
5. Списание суммы пополнения со счета пользователя. Пополнение баланса.
6. Баланс телефона обновляется, транзакция окончена.

## Задание №3. SQL vs NoSQL

### 3.1

1. Поддержка ACID, что гарантирует сохранность и целостность данных.
2. Строгая типизация: SQL системы имеют строгую типизацию данных, что помогает предотвратить ошибки и улучшает производительность. В отличие от этого, NoSQL системы могут иметь более слабую типизацию или не иметь ее вообще.
3. Более широкий выбор инструментов и библиотек: Существует огромное количество инструментов и библиотек для работы с SQL системами, что упрощает разработку и поддержку приложений. NoSQL системы, хотя и набирают популярность, пока еще не имеют такого широкого выбора инструментов.
4. Лучшее соответствие для классических реляционных данных: SQL системы изначально были разработаны для работы с классическими реляционными данными, такими как таблицы. Некоторые NoSQL системы лучше подходят для работы с “неклассическими” данными, но SQL системы все еще остаются наиболее подходящим выбором для большинства случаев.
5. Более высокий уровень безопасности: SQL системы, как правило, имеют более высокий уровень безопасности, поскольку они были разработаны с учетом требований безопасности.

## Задание №4. Кластеры

### 4.1

При выборе типа СУБД для обработки большого количества данных и производства большого количества вычислений, основными критериями могут быть следующие:

1. Производительность: СУБД должна обеспечивать высокую производительность обработки запросов и операций с данными.
2. Масштабируемость: СУБД должна позволять масштабировать вычислительные ресурсы в горизонтальном (добавление новых серверов) и вертикальном (увеличение мощности существующих серверов) направлении.
3. Отказоустойчивость: СУБД должна иметь механизмы обеспечения безопасности данных и восстановления после сбоев.
4. Распределенность: СУБД должна позволять распределять данные и запросы на выполнение между несколькими серверами для увеличения пропускной способности и ускорения обработки.

При выборе модели распределенных вычислений для работы с огромным количеством данных можно рассмотреть два варианта:

1. Модель "массовой обработки данных" (MapReduce): данная модель подходит для обработки больших объемов данных, разбивая их на части и распределяя для параллельной обработки на несколько серверов. Она эффективна в случаях, когда требуется обработать данные в пакетном режиме, без требования по мгновенному ответу. Примерами распределенных СУБД, основанных на модели MapReduce, являются Apache Hadoop (свободно распространяемый набор утилит, библиотек и фреймворк для разработки и выполнения распределённых программ, работающих на кластерах более сотен узлов) и Apache Spark.

2. Модель "управляемых транзакций" (ACID): данная модель подходит для обработки данных, где требуется ACID-консистентность (атомарность, согласованность, изолированность, долговечность) транзакций. Она обеспечивает возможность выполнения сложных операций с данными и соблюдение целостности данных при распределении на несколько серверов. Примеры распределенных СУБД, основанных на модели управляемых транзакций, включают MySQL Cluster, Oracle RAC и PostgreSQL.
