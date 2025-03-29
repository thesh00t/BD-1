BD-1
1. Выберите из таблицы orders все заказы

```   
SELECT * FROM orders
```

![image](https://github.com/user-attachments/assets/7d8c4305-9a3d-4db1-8591-9b41eb5ff3a2)
--------------------------------------------------------------------------------------------------------------------------------------------------
2. Выберите из таблицы orders все заказы кроме новых. У новых заказов status равен "new". Использовать in
   
SELECT * FROM orders WHERE STATUS IN ('cancelled','in_progress','delivery')
![image](https://github.com/user-attachments/assets/e326c33e-8a01-4048-9d4a-6bd78032f846)
--------------------------------------------------------------------------------------------------------------------------------------------------
3. Выберите из таблицы orders все новые и отмененные заказы. У отмененных заказов status равен "cancelled". У новых заказов status равен "new".
   
SELECT * FROM orders WHERE STATUS IN ('cancelled','new')
![image](https://github.com/user-attachments/assets/7e01271a-2291-4a96-946c-9d1e3e0d30b2)
--------------------------------------------------------------------------------------------------------------------------------------------------
4. Выберите из таблицы orders все заказы содержащие более 3 товаров (products_count). Вывести нужно только номер (id) и сумму (sum) заказа.
   
SELECT id, sum FROM orders WHERE products_count > 3
![image](https://github.com/user-attachments/assets/73c7bcaa-3ed3-4070-ad40-88672abcc02e)
--------------------------------------------------------------------------------------------------------------------------------------------------
BD-2
1 файл

1) Выберите из таблицы orders 3 самых дешевых заказа за всё время.
Данные нужно отсортировать в порядке убывания цены.
Отмененные заказы не учитывайте.
![image](https://github.com/user-attachments/assets/1af19dab-cfbb-4b75-9f61-813b974bff42)

2) Выберите из таблицы orders 2 самых дорогих заказов за всё время.
Данные нужно отсортировать в порядке убывания цены.
Отмененные заказы не учитывайте.
![image](https://github.com/user-attachments/assets/ce083f5c-3ed1-4b4d-b228-949e6c67281f)
--------------------------------------------------------------------------------------------------------------------------------------------------
2 файл

Добавьте в таблицу orders данные о новом заказе стоимостью 8000 рублей. В заказе 4 товара (products).

INSERT INTO orders (id, products, sum) VALUES (6, 4, 8000);
![image](https://github.com/user-attachments/assets/b3aa098e-c039-49ef-b0be-51cfd9a485ae)
--------------------------------------------------------------------------------------------------------------------------------------------------
3 файл

Добавьте в таблицу products новый товар — «VR-очки», стоимостью 70000 рублей в количестве (count) 2 штук

INSERT INTO products (id, name, price, count) VALUES (7, 'VR-очки', 70000, 2);
![image](https://github.com/user-attachments/assets/2cd55a50-0e8c-417d-8ad2-6d0307d7d85a)
--------------------------------------------------------------------------------------------------------------------------------------------------
4 файл

В таблицу products внесли данные с ошибкой, вместо "PS5" в наименовании написали IMAC. Исправьте ошибку.

UPDATE products SET name = 'PS5' WHERE name = 'IMAC';
![image](https://github.com/user-attachments/assets/6e1c717f-503c-4246-9611-933962924dbf)
--------------------------------------------------------------------------------------------------------------------------------------------------
Лр 3 
-
1.Создайте таблицу users с полем id типа INT и двумя текстовыми полями, которые будут хранить имя (first_name) и фамилию (last_name). Длина имени и фамилии не превышает 50 символов.
-
Добавьте в таблицу трех пользователей: Дмитрия Иванова, Анатолия Белого и Дениса Давыдова.

![image](https://github.com/user-attachments/assets/d729b1c5-e31a-4e60-88c1-ad851c497f26)

![image](https://github.com/user-attachments/assets/4096d56a-3ebb-4e19-a839-ecc0fd60b75a)

Лр 4
-
1.Создайте таблицу users для хранения информации о пользователях сайта. В таблице должны быть следующие поля: id – идентификатор, целое положительное; email – адрес электронной почты, строка не более 100 символов; date_joined – дата регистрации 
(достаточно хранить дату, без времени) last_activity – дата и время последней активности (с точностью до секунд).
-
![image](https://github.com/user-attachments/assets/b7acc72a-7fa5-4fdd-91ff-c59c92db939c)

Неверное решение:

CREATE TABLE users( id INT UNSIGNED, email VARCHAR(100), date_joined DATE, last_activity DATETIME );
INSERT INTO users (id, email, date_joined, last_activity) VALUES (1, "user1@domain.com", "2014-12-12", "2016-04-08 12:34:54") INSERT INTO users (id, email, date_joined, last_activity) VALUES (2, "user2@domain.com", "2014-12-12", "2017-02-13 11:46:53") INSERT INTO users (id, email, date_joined, last_activity) VALUES (3, "user3@domain.com", "2014-12-13", "2017-04-04 05:12:07")

Верное решение: 

create table users ( id int(10) unsigned, email varchar (100), date_joined date, last_activity datetime ); insert into users (id, email, date_joined,last_activity) values (1,'user1@domain.com', '2014-12-12','2016-04-08 12:34:54'), (2,'user2@domain.com', '2014-12-12','2017-02-13 11:46:53'), (3,'user3@domain.com', '2014-12-13','2017-04-04 05:12:07');

![image](https://github.com/user-attachments/assets/d1e72b07-f656-41cf-aa8d-06c4cd585b0c)

2.Создайте таблицу calendar для хранения календаря посетителей. В таблице должны быть следующие поля: id – идентификатор записи в календаре, целое положительное; user_id – идентификатор пользователя, целое положительное; doctor_id – идентификатор доктора, целое положительное; visit_date – дата и время визита (точность до секунд).
-
![image](https://github.com/user-attachments/assets/9fdfbd4f-2646-49d5-a954-94c48b90baf7)

Неверное решение:

Create table calendar ( id int unsigned, user_id int unsigned, doctor_id int unsigned, visit_date datetime); Insert into calendar (id, user_id, doctor_id, visit_date) Values (1, 1914 , 1, '2017-04-08 12:00:00'), (2, 12, 1, '2017-04-08 12:30:00'), (3, 4641, 2, '2017-04-09 09:00:00'), (4, 4641, 2,'2017-04-09 09:00:00'), (5, 15, 2,'2017-04-09 10:00:00')

Верное решение:

Create table calendar ( id int unsigned, user_id int unsigned, doctor_id int unsigned, visit_date datetime); Insert into calendar (id, user_id, doctor_id, visit_date) Values (1, 1914 , 1, '2017-04-08 12:00:00'), (2, 12, 1, '2017-04-08 12:30:00'), (3, 4641, 2, '2017-04-09 09:00:00'), (4, 784, 1,'2017-04-08 13:00:00'), (5, 15, 2,'2017-04-09 10:00:00') 

![image](https://github.com/user-attachments/assets/b3af42ac-b570-424f-bb73-dadf7cf39b34)

3.Создайте таблицу users , в которой будут следующие поля: id — идентификатор, целые положительные числа. first_name— имя, строки до 50 символов. last_name — фамилия, строки до 60 символов. bio — биография, текст до 65000 символов.
-
![image](https://github.com/user-attachments/assets/0c30eb1c-25bc-42f3-8731-fb064ed04f5d)

Неверное решение:

create table users ( id int (10) unsigned, first_name varchar (50) unsigned, last_name varchar (60) unsigned, bio text ); INSERT INTO users (id, first_name, last_name, bio) VALUES (1,'Антон','Кулик','С отличием окончил 39 лицей.'), (2,'Сергей','Давыдов',''), (3,'Дмитрий','Соколов','Профессиональный программист.')

Верное решение:

create table users ( id int (10) unsigned, first_name varchar (50), last_name varchar (60), bio text ); INSERT INTO users (id, first_name, last_name, bio) VALUES (1,'Антон','Кулик','С отличием окончил 39 лицей.'), (2,'Сергей','Давыдов',''), (3,'Дмитрий','Соколов','Профессиональный программист.')

![image](https://github.com/user-attachments/assets/2713ba61-ab0d-4490-8b05-c56a7af914be)
