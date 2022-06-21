# 1. CREAR UNA NUEVA BASE DE DATOS DONDE ADENTRO TENDREMOS NUESTRAS TABLAS

CREATE DATABASE 'nombre';

//Example:

CREATE DATABASE myfirstdatabase;

# 2. PARA PODER PODER VER EL REGISTRO DE TODAS LAS BASES DE DATOS QUE EXISTEN Y QUE MYSQL ESTA GESTIONANDO

SHOW DATABASES;

# 3. PARA PODER INDICAR A QUE BASE DE DATOS VAMOS A ENTRAR O QUE BASE DE DATOS VAMOS A UTILIZAR

USE 'nombre';

//Example:

USE myfirstdatabase;

# 4. TIPOS DE DATOS MYSQL

int(integer) -> 1, 3, 10, 1000
float -> 1.5, 16.9, 100.5
varchar(string) -> 'chanchito', 'hola mundo'

# 5. PARA CREAR UNA NUEVA TABLA

CREATE TABLE 'nombre';

//Example:

CREATE TABLE animales;

# 6. PARA CREAR UNA TABLA Y COLUMNAS

CREATE TABLE 'nombre'('valores');   Example:

CREATE TABLE animales(
  id int; (le indicamos que id es entero)
  tipo varchar(255); (le indicamos que tipo sera un string ya que queremos indicar que tipo de animal es) | varchar('le indicamos que tan largo queremos que sea la cadena de caracteres)
  estado varchar(255);
  CREATE PRIMARY KEY(id); (con esto le indicamos que esta es una llave primaria y que funcione como identificador unico)
);

# 7. PARA PODER INSERTAR DATOS A NUESTRA TABLA

INSERT INTO 'nameTable' ('los campos a los cuales queremos insertar datos') VALUES ('indicamos cuales son los valores que le vamos a pasar');

//Example:

INSERT INTO animales (tipo, estado) VALUES ('chanchito', 'feliz');

# 8. AL EJECUTAR TODO LO DE ARRIBA NOS SALDRA ERROR YA QUE NO LE INDICAMOS LA PROPIEDAD DE AUTOINCREMENTAR SU VALOR

# 9. MODIFICAR UNA TABLA QUE YA HA SIDO CREADA

ALTER TABLE 'nameTable' MODIFY COLUMN 'la columna que queremos modificar' 'tipo de valor' 'lo que queremos modificar de la columna';

//Example:

ALTER TABLE animales MODIFY COLUMN id int auto_increment;
