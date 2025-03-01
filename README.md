BD-1
1. Выберите из таблицы orders все заказы
   
SELECT * FROM orders
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


