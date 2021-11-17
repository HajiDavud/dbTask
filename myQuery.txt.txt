CREATE TABLE products 
(
 id int PRIMARY KEY,
 name VARCHAR(255),
 price int,
 brandID int
)

CREATE TABLE brands
(
 id int PRIMARY KEY,
 name VARCHAR(255)
)

ALTER TABLE products
ADD FOREIGN KEY (brandID) REFERENCES brands(id);

INSERT INTO brands
VALUES(1,'Milla')

INSERT INTO brands
VALUES(2,'Sirab')

INSERT INTO brands
VALUES(3,'Kola')

INSERT INTO brands
VALUES(4,'KolaFantaUzunluqBOuyukdurON')


INSERT INTO products
VALUES(1,'Milk',5,1)

INSERT INTO products
VALUES(2,'Milk 2',3,1)

INSERT INTO products
VALUES(3,'Sirab1',1,2)


INSERT INTO products
VALUES(4,'Sirab2',12,2)

INSERT INTO products
VALUES(5,'Boyuk Kola',25,3)


INSERT INTO products
VALUES(6,'Boyuk Kola ZERO',215,3)

SELECT * FROM products WHERE price>10;


SELECT name FROM brands WHERE LEN(name) > 10;
