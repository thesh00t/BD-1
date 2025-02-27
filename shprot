delete from cars where country = "JP" and (power <= 80 or power >= 130)
delete from cars where country = 'KR' or power<80

#Удалить из таблицы products все товары, которых нет на складе.
delete from products where count<1;

#Удалить из таблицы cars все автомобили начиная с 2010 года и старше
delete from cars where year<=2010

#Измените статус (status) заказа под номером (id) 5 с delivery на success.
update orders set status='success' where id=5

#Увеличьте цену 5 самых дешевых товаров на 5%
update products set price=price*1.05 order by price limit 5

теперь самых дорогих:
update products set price=price*1.05 order by price desc limit 5
