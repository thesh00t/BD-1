
Выберите из таблицы orders все заказы
1.SELECT * FROM orders
![image](https://github.com/user-attachments/assets/7d8c4305-9a3d-4db1-8591-9b41eb5ff3a2)

2.Выберите из таблицы orders все заказы кроме новых. У новых заказов status равен "new". Использовать in
SELECT * FROM orders WHERE STATUS IN ('cancelled','in_progress','delivery')
![image](https://github.com/user-attachments/assets/e326c33e-8a01-4048-9d4a-6bd78032f846)

3.Выберите из таблицы orders все новые и отмененные заказы. У отмененных заказов status равен "cancelled". У новых заказов status равен "new".
SELECT * FROM orders WHERE STATUS IN ('cancelled','new')
![image](https://github.com/user-attachments/assets/7e01271a-2291-4a96-946c-9d1e3e0d30b2)

Выберите из таблицы orders все заказы содержащие более 3 товаров (products_count). Вывести нужно только номер (id) и сумму (sum) заказа.
SELECT id, sum FROM orders WHERE products_count > 3
![image](https://github.com/user-attachments/assets/73c7bcaa-3ed3-4070-ad40-88672abcc02e)

