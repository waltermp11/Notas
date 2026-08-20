
Tenemos dos bases de datos, relacionales y no relacionales, 2 universos completamente diferentes, para almacenar informacion.



# Bases de datos Relacionales

tienen relaciones, donde una tabla de datos se puede relacionar con otras.
- Datos conectados
- uniones.


**que factores se necesitan para que se den esas relaciones? o situaciones?**


## Las tablas
Nosotros tenemos esto para guardar los datos como tal.

## PRIMARY KEY
- id -- lo usamos siempre para un identificador propio. Clave primaria, es con la que se relaciona con la otra.
	- normalmente es auto- incremental!!!


**Pero vamos a tener un cambio llamaremos PRIMARY KEY --  SERA EL VALOR UNICO,  ya que es un valor que sera (Auto incrementar)**

-

## CLAVE FORANEA
- no nació de mi, esta en otro lado, no es de acá.
- esta me ayuda a la conexión de dos tablas!!!!!
- Relaciones para conectar las tablas.


## Ejemplo de las bases datos y sus relaciones 
### Tabla de Mascotas

- decidimos agregar una columna <mark class="verde">dueño_id</mark>, si lo pongo, se que de quien es dueño
- Resulta que un dueño puede tener varias mascotas entonces lo anterior se lee:
	- <mark class="verde">el dueño 1 es dueño de las mascotas con id 1 y 2</mark>				
	
		- **Foreign KEY** -- dueño_id, tenemos la siguiente teoría, toda clave primaria en otra tabla es clave foranea.


- en ste caso MASCOTAS dependen de DUEÑO, porque sin DUEÑO no hay mascotas que evaluar en la veterinaria.

| id  | Nombre   | Peso | especie                | dueño_id |
| :-- | :------- | :--- | ---------------------- | -------- |
| 1   | Estrella | 5kg  | French Poodle mini Toy | 1        |
| 2   | Celeste  | 11kg | Gato                   | 1        |

### Tabla de Dueños

| Id  | nombre | apellido   |
| :-- | :----- | :--------- |
| 1   | Pepito | mendieta   |
| 2   | pepita | picapiedra |


## RELACIONES DE TABLAS
Tenemos 3 tipos de relaciones principales

1. Uno a uno -- 1:1
2. Uno a muchos -- 1:n
3. Muchos a muchos -- n:n








