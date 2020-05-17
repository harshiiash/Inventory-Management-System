User Id: admin
Password : password
SQL commands required before program execution
create database IMS;
use IMS;
create table product(productid int NOT NULL AUTO_INCREMENT,productName varchar(30),purchasePrice int,salePrice decimal(8,2),productQty int,PRIMARY KEY (productId));
create table sale(saleID int NOT NULL AUTO_INCREMENT,productID int, price decimal(8,2),date date,saleQty int,PRIMARY KEY(saleId),FOREIGN KEY (productID) REFERENCES product(productID) ON DELETE CASCADE ON UPDATE CASCADE );