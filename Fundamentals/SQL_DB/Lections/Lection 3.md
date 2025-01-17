24.09.2024

![[Снимок экрана 2024-09-24 в 19.04.19.png]]
![[Снимок экрана 2024-09-24 в 19.04.32.png]]
![[Pasted image 20241001020623.png]]
```sql
SELECT [константы, агрегатные_функции, поля_группировки]
FROM имя_таблицы
WHERE условия_на_ограничения_строк
GROUP BY поля_группировки
HAVING условие_на_ограничение_строк_после_группировки
ORDER BY условие_сортировки
```
![[Снимок экрана 2024-09-24 в 19.05.14.png]]
![[Снимок экрана 2024-09-24 в 19.05.27.png]]

# Подзапросы

Подзапрос — это запрос, использующийся в другом SQL запросе. Подзапрос всегда заключён в круглые скобки и обычно выполняется перед основным запросом

Возможности подзапросов:
- позволяют использовать результаты одного запроса для фильтрации данных во внешнем запросе;
- используются для получения агрегированных значений (COUNT, SUM, AVG) и включения их во внешний запрос;
- позволяют сравнивать данные из разных таблиц или таблицы с самой собой.

## Некоррелированные подзапросы
Независимые
### Скалярные подзапросы
- Возвращают одно значение, которое используется во внешнем запросе.
- Часто используются для сравнения или фильтрации данных

```sql
SELECT CustomerName 
FROM Customers 
WHERE CustomerID = (SELECT CustomerID FROM Orders WHERE OrderID = 12345);
```

### Многострочные подзапросы
- Возвращают несколько строк данных, которые используются во внешнем запросе.
- Часто используются с операторами IN для проверки членства или наличия данных.
```sql
SELECT OrderID, ProductName
FROM Orders WHERE ProductID IN (
	SELECT ProductID
	FROM Products
	WHERE CategoryID = 'Electronics'
);
```

### Многостолбцовые подзапросы
```sql
SELECT * FROM Reservations
    WHERE (room_id, price) IN (SELECT id, price FROM Rooms);
```
## Коррелированные подзапросы
- Используют значения из внешнего запроса для фильтрации данных во внутреннем подзапросе.
- Позволяют выполнять более сложные операции с данными из разных таблиц.

``` sql
SELECT ProductName 
FROM Products 
WHERE Price > (SELECT AVG(Price) 
			   FROM Products 
			   WHERE CategoryID = Products.CategoryID);
```

```sql
SELECT FamilyMembers.member_name, (
    SELECT SUM(Payments.unit_price * Payments.amount)
    FROM Payments
    WHERE Payments.family_member = FamilyMembers.member_id
) AS total_spent
FROM FamilyMembers;
```
## Подзапросы в FROM
- Возвращают несколько строк данных, которые используются во внешнем запросе.
```sql
SELECT OrderID, ProductName
FROM (
	SELECT ProductID 
	FROM Products 
	WHERE CategoryID = 'Electronics' 
) t1;
```

