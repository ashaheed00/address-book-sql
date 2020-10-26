# address-book-sql
## UC1_Create_AddressBookServiceDB
```
CREATE DATABASE address_book_service;
SHOW DATABASES;
USE address_book_service;
```
## UC2_Create_AddressBookTable
```
CREATE TABLE address_book (
id              INT unsigned NOT NULL AUTO_INCREMENT,
first_name      VARCHAR(20) NOT NULL,
last_name       VARCHAR(20),
address         VARCHAR(200) NOT NULL,
city            VARCHAR(20) NOT NULL,
state           VARCHAR(20) NOT NULL,
zip             VARCHAR(6) NOT NULL,
phone_number    VARCHAR(10) NOT NULL,
email           VARCHAR(20) NOT NULL,
PRIMARY KEY (id)
);
```