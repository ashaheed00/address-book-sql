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
## UC4_EditData_UsingName
```
UPDATE address_book set email = 'akram007@gmai.com'
   WHERE first_name = 'Akram' AND last_name = 'Shaheed';
```
## UC5_DeletePerson_UsingName
#### Adding a dummy person and later deleting it using name
```
INSERT INTO address_book (first_name, last_name, address, city, state, zip, phone_number, email) VALUES
   ('Dummy','Person','Berhampore','Kolkata','West Bengal','742100','9999900000','dummy@person.com');
```
```DELETE FROM ADDRESS_BOOK WHERE FIRST_NAME = 'Dummy' AND LAST_NAME = 'Person';```
## UC6_RetrievePerson_FromCityState
```
SELECT * FROM address_book WHERE city = 'Aluva';
```
```
SELECT * FROM address_book WHERE state = 'West Bengal';
```
## UC7_SizeBy_CityOrState
```
SELECT city, COUNT(city) FROM address_book GROUP BY city;
SELECT state, COUNT(state) FROM address_book GROUP BY state;
```