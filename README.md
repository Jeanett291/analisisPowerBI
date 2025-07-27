# analisisPowerBI
En este proyecto se analizará una base de datos mediante el uso de Power BI

# Conexión a los datos
1.	Obten los datos desde la Fuente de OData utilizando el siguiente enlace:
https://services.odata.org/V4/Northwind/Northwind.svc/
2.	Selecciona las siguientes tablas:
a.	Categories
b.	Products
c.	Orders_Details
d.	Orders
e.	Employees
f.	Customers
# Transformación de datos con Power Query
1.	Da click en Transformar datos.
2.	En el Editor de Power Query realiza las siguientes transformaciones:
1.	Para la tabla Categories deja únicamente las columnas:
“CategoryID”, “CategoryName”, “Description”
2.	Para la tabla Products deja únicamente las columnas:
“ProductID”, “ProductName”, “CategoryID”.
3.	Para la tabla Order_Details, agrega una columna personalizada llamada
“TotalPrice” con la siguiente fórmula: (UnitPrice*Quantity) * (1-Discount)
4.	Para la tabla Order_Details deja únicamente las columnas:
“OrderID”, “ProductID”, “Quantity”, “Discount”, “TotalPrice”.
5.	Para la tabla Orders deja únicamente las columnas:
“OrderID”, “CustomerID”, “EmployeeID”, “OrderDate”, “RequiredDate”,
“ShippedDate”, “ShipCity”, “ShipCountry”.
6.	Para la tabla Employees, agrega una columna llamada “Name” que resulte
de combinar “FirstName” y “LastName”, separado por un separador Espacio.
Como ejemplo, debería quedar así: Davolio Nancy.
7.	Para la tabla Employees deja únicamente las columnas:
“EmployeeID”, “Name”.
8.	Para la tabla Customers deja únicamente las columnas:
“CustomerID”, “CompanyName”, “ContactName”, “ContactTitle”, “Phone”.
# Formato y DAX
1.	Ve a la Vista de Tabla.
2.	Explora las tablas, trata de comprender los datos y asigna el formato/categoría que consideres adecuada para tus datos. Por ejemplo, formato de moneda, porcentajes, número de decimales, categoría de datos, etcétera.
3.	Selecciona la tabla Orders. Ahí encuentras dos columnas: “RequiredDate” y
•	“ShippedDate”. Crea una nueva columna llamada “ShipResult” con la siguiente
•	lógica:
•	Si el “ShippedDate“ es mayor que el “RequiredDate”, entonces la columna es igual a “Late”, de lo contrario será “On time”.
4.	Utilizando la columna recientemente generada “ShipResult” , crea una nueva columna llamada “DaysLate” con la siguiente lógica:

<img width="1788" height="767" alt="Power BI" src="https://github.com/user-attachments/assets/92a8de5c-456c-4986-afa0-c8267e3a87c2" />





Durante el proyecto aprendí a conectar datos usando OData y a transformar tablas con Power Query también desarrollé columnas calculadas con DAX como ShipResult y DaysLate además entendí cómo modelar datos y establecer relaciones entre tablas para lograr una interacción fluida entre visualizaciones finalmente diseñé un dashboard dinámico y lo publiqué en Power BI Service aplicando roles de seguridad para controlar el acceso a la información según el país de envío

