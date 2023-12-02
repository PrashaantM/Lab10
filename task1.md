Make a query that returns all the names (only the names) of customers from the United Kingdom:

SELECT CustomerName FROM Customers WHERE Country = 'UK';

Make a query that returns product names, the units they are sold in, and their prices, listing only the rows where products have a price of $55 or more:

SELECT productName, Unit, Price FROM Products WHERE Price >= 55;

Make a query that lists the product names, prices, and category names from the beverage category. Have it sorted by lowest price to highest price.:

SELECT ProductName, Price, CategoryName FROM Products INNER JOIN Categories ON Products.CategoryID = Categories.CategoryID WHERE Categories.CategoryID = 1 ORDER BY Price ASC;

Make a query that returns the first name of the employee, the last name of the employee, and order numbers of all of their orders placed by the employees that have employee numbers from 1-5. Have it sorted in alphabetical order based on the last name of the employees:
SELECT FirstName, LastName, Orders.OrderID FROM Employees INNER JOIN Orders ON Employees.EmployeeID = Orders.EmployeeID WHERE Employees.EmployeeID Between 1 AND 5 ORDER BY LastName ASC;

Make a query that returns the customer's names, the order id, the product name, and the quantity of each product. Have it returned in alphabetical order based on customer names. (Note: For this query you will need 4 relations and 3 joins. ):

SELECT CustomerName, Orders.OrderID, ProductName, Quantity FROM ((Customers INNER JOIN Orders ON Customers.CustomerID = Orders.CustomerID) INNER JOIN OrderDetails ON OrderDetails.OrderID=Orders.OrderID) INNER JOIN Products ON Products.ProductID=OrderDetails.ProductID ORDER BY CustomerName ASC;
