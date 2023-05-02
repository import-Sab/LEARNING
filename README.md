Configure CPI JDBC Driver and Data Source then Create iFlow Select Records From Database Table


Configure JDBC Driver, Download from:
https://help.sap.com/viewer/368c481cd6954bdfa5d0435479fd4eaf/Cloud/en-US/88be64412f1b46d684dfba11f2767c5b.html
https://help.sap.com/viewer/368c481cd6954bdfa5d0435479fd4eaf/Cloud/en-US/77c7d9550e12494eb600ec82496ef215.html


Create Data Source
Name = MSQL_NORTHWIND

DB user = user01
DB password = 12345abc
Url = jdbc:sqlserver://sql-server-virtual-host:1433;databaseName=Northwind
Virtual host = sql-server-virtual-host
Virtual port = 1433
Location ID = POC
Tick "Cloud Connector"


Create iFlow connect to SQL Server using JDBC Adapter and Data Soure MSQL_NORTHWIND
SELECT * FROM Customers
