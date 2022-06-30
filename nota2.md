# CREANDO UNA TABLA DE DATOS DE USUARIOS

## 1. CREAMOS LA TABLA

~~~
CREATE TABLE user (
  id int not null AUTO_INCREMENT,
  name varchar(255) not null,
  edad int not null,
  email varchar(255) not null,
  PRIMARY KEY(id)
);
~~~

## 2. INSERTAMOS DATOS

Data:
~~~
NAME  EDAD  EMAIL
OSCAR 25 oscar@gmail.com
LAYLA 15 layla@gmail.com
NICOLAS 36 nico@gmail.com
CHANCHITO 7 oscar@gmail.com
~~~

Solving:
~~~
INSERT INTO user (name, edad, email) VALUES ('OSCAR', 25, 'oscar@gmail.com');
INSERT INTO user (name, edad, email) VALUES ('LAYLA', 15, 'layla@gmail.com);
INSERT INTO user (name, edad, email) VALUES ('NICOLAS', 36, 'nico@gmail.com');
INSERT INTO user (name, edad, email) VALUES ('CHANCHITO', 7, 'oscar@gmail.com');
~~~

## 3. PROPIEDADES Y CONDICIONES SELECT:

- 3.1 LIMIT: Limitamos el numero de registros que se nos va a mostrar.

~~~
SELECT * FROM user LIMIT 1;
~~~

- 3.2 WHERE: GENERAMOS UNA CONDICION.

~~~
SELECT * FROM user WHERE edad > 15;
SELECT * FROM user WHERE edad >= 15;
SELECT * FROM user WHERE edad > 20 AND email = 'nico@gmail.com'; // EN ESTE CASO SOLO SE IMPRIMIRA EL VALOR SI ES QUE CUMPLE LAS 2 CONDICIONES
SELECT * FROM user WHERE edad > 20 OR email = 'layla@gmail.com'; // EN ESTE CASO SE IMPRIMIRA TODOS LOS VALORES
~~~
