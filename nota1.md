## 1. CREAR UNA NUEVA BASE DE DATOS DONDE ADENTRO TENDREMOS NUESTRAS TABLAS
~~~
CREATE DATABASE 'nombre';
~~~
Example:
~~~
CREATE DATABASE myfirstdatabase;
~~~
## 2. PARA PODER PODER VER EL REGISTRO DE TODAS LAS BASES DE DATOS QUE EXISTEN Y QUE MYSQL ESTA GESTIONANDO
~~~
SHOW DATABASES;
~~~
## 3. PARA PODER INDICAR A QUE BASE DE DATOS VAMOS A ENTRAR O QUE BASE DE DATOS VAMOS A UTILIZAR
~~~
USE 'nombre';
~~~
Example:
~~~
USE myfirstdatabase;
~~~
## 4. TIPOS DE DATOS MYSQL
~~~
int(integer) -> 1, 3, 10, 1000
float -> 1.5, 16.9, 100.5
varchar(string) -> 'chanchito', 'hola mundo'
~~~
## 5. PARA CREAR UNA NUEVA TABLA
~~~
CREATE TABLE 'nombre';
~~~
Example:
~~~
CREATE TABLE animales;
~~~
## 6. PARA CREAR UNA TABLA Y COLUMNAS
~~~
CREATE TABLE 'nombre'('valores');
~~~
Example:
~~~
CREATE TABLE animales(
  id int; (le indicamos que id es entero)
  tipo varchar(255); (le indicamos que tipo sera un string ya que queremos indicar que tipo de animal es) | varchar('le  - indicamos que tan largo queremos que sea la cadena de caracteres)
  estado varchar(255);
  CREATE PRIMARY KEY(id); (con esto le indicamos que esta es una llave primaria y que funcione como identificador unico)
);
~~~

## 7. PARA PODER INSERTAR DATOS A NUESTRA TABLA
~~~
INSERT INTO 'nameTable' ('los campos a los cuales queremos insertar datos') VALUES ('indicamos cuales son los valores que le vamos a pasar');
~~~
Example:
~~~
INSERT INTO animales (tipo, estado) VALUES ('chanchito', 'feliz');
~~~
## 8. AL EJECUTAR TODO LO DE ARRIBA NOS SALDRA ERROR YA QUE NO LE INDICAMOS LA PROPIEDAD DE AUTOINCREMENTAR SU VALOR

## 9. MODIFICAR UNA TABLA QUE YA HA SIDO CREADA
~~~
ALTER TABLE 'nameTable' MODIFY COLUMN 'la columna que queremos modificar' 'tipo de valor' 'lo que queremos modificar de la columna';
~~~
Example:
~~~
ALTER TABLE animales MODIFY COLUMN id int auto_increment;
~~~
## 10. SI QUEREMOS VER EL COMANDO QUE USAMOS PARA CREAR UNA TABLA
~~~
SHOW CREATE TABLE 'nameTable';
~~~
Example:
~~~
SHOW CREATE TABLE animales;
~~~
NOS MUESTRA EL SIGUIENTE COMANDO POR TERMINAL:
~~~
CREATE TABLE `animales` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `tipo` varchar(255) COLLATE utf8mb4_unicode_ci DEFAULT NULL,
  `estado` varchar(255) COLLATE utf8mb4_unicode_ci DEFAULT NULL,
  PRIMARY KEY (`id`)
)
~~~


## 11. PARA PODER LISTAR TODOS LOS REGISTROS O MOSTRAR TODOS LOS REGISTROS DE LAS TABLAS QUE HEMOS CREADO.
TIENE VARIOS METODOS.

- 11.1 MOSTRAR TODOS LAS COLUMNAS Y LAS FILAS
~~~
SELECT * FROM 'nameTable';
~~~
Example:
~~~
SELECT * FROM animales;
~~~
- 11.2 MOSTRAR SOLO UN REGISTRO
~~~
SELECT * FROM 'nameTable' WHERE 'nameColumn' = 'value';
~~~
Example:
~~~
SELECT * FROM animales WHERE id = 1;
SELECT * FROM animales WHERE estado = 'feliz';
~~~

- 11.3 MOSTRAR UN REGISTRO CON DOS CONDICIONES;

'AND' : SE TIENE QUE CUMPLIR LAS 2 CONDICIONES PARA QUE LOGRE MOSTRAR EL REGISTRO
~~~
SELECT * FROM 'nameTable' WHERE 'nameColumn' = 'value' AND 'nameColumn' = 'value';
~~~
Example:
~~~
SELECT * FROM animales WHERE id = 2 AND tipo = 'perrito';
~~~
'OR' : SE MUESTRAN AMBOS VALORES
~~~
SELECT * FROM 'nameTable' WHERE 'nameColumn' = 'value' OR 'nameColumn' = 'value';
~~~
Example:
~~~
SELECT * FROM animales WHERE id = 2 OR tipo = 'chanchito';
~~~

## 12. ACTUALIZAR LOS REGISTROS QUE YA SE ENCUENTRAN EN NUESTRA BASE DE DATOS
~~~
UPDATE 'nameTable' SET 'column' = 'value' WHERE 'colum' = 'value'; // SE RECOMIENDA USAR UN INDENTIFICADOR O ID (AND id = 'value')
~~~
Example:
~~~
UPDATE animales SET estado = 'triste' WHERE id = 1;
~~~

## 13. ELIMINAR UN REGISTRO
~~~
DELETE FROM 'nameTable' WHERE 'nameColumn' = 'Value' // SE RECOMIENDA USAR SU IDENTIFICADOR O ID
~~~
Example:
~~~
DELETE FROM animales WHERE id = 3;
~~~

