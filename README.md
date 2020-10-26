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
## UC3_InsertDataInto_AddressBookTable
```
INSERT INTO address_book (first_name, last_name, address, city, state, zip, phone_number, email) VALUES
   ('Akram','Shaheed','Berhampore','Kolkata','West Bengal','742100','9999900000','first@person.com'),
   ('Aditi','Sharma','4/11 Vati Nagar','Thane','Maharashtra','625058','8888888888', 'sec@person.com'),
   ('John','Smith','8/22 Kalyani','Kalyani','West Bengal','729558','8123400000','third@person.com'),
   ('Krishna','Pauly','8/11 Podula Road','Aluva','Kerala','826123','7894652222','fourth@person.com');
```