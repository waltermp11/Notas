
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
	
		- **Foreign KEY** -- dueño_id, tenemos la siguiente teoría, toda clave primaria en otra tabla es clave <font color="#92d050">foranea.</font>


- en este caso MASCOTAS dependen de DUEÑO, porque sin DUEÑO no hay mascotas que evaluar en la veterinaria.

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
2. Uno a muchos -- 1:n --> *normalmente la clave foranea va en la tabla de muchos a uno.*
3. Muchos a muchos -- n:n





## FOREIGN KEY


Recordemos que hace referencia donde esta la <mark class="verde">clave primaria que haremos clave foranea</mark>

- Tenemos un alter table -- para anunciar que haremos un cambio en la tabla mascotas.
- Add constraint -- agregamos una restriccion que sera la **FOREIGN KEY** -- recordando que yo mismo le pongo nombre a la restriccion
- FOREIGN KEY -- aca tenemos la clave primaria de otra tabla.
	- Nosotrs siempre verificamos y nos hacemos una pregunta : **QUIEN DEPENDE DE QUIEN, O SEA QUE TABLA DE DEPENDE DE LA OTRA**



![[Pasted image 20260820120930.png|500x]]




## En la relacion de muchos a muchos

- tenemos la siguiente representacion en N;M o n:m
- Para la relacion de muchos a muchos tenemos siempre que crear una tabla <mark class="verde">PIVOTE O INTERMEDIA</mark>
- En la tabla intermedia o pivote tenemos:
	- Clave foranea de cada una de las tablas, normalmente son las PK de las otras dos tablas.


```
CREATE TABLE estudiantes (
id SERIAL PRIMARY KEY --> recordando que serial, seria tambien como el AUTOINCREMENT!✅
nombre VARCHAR (150) NOT NULL,  --> la idea es que no sea not null que nunca sea null este valor en la tabla. ✅
email VARCHAR (150) UNIQUE NOT NULL --> **unique: que este dato sea unico como tal, tambien como el numero de pasaporte✅, claramente en este caso es para que nosotros tengamos unicamente solo un email por estudiante asociado.**
)

```




## Subconsultas
Select completo dentro de otro select.

- un select interno seria la condicion del otro select.

**Ejemplo:**
**Bancolombia busca las cuentas con sueldo mayor o igual a 5000000 y despues quiere ver las transacciones de estas cuentas.**


### QUERY

SELECT nombre, especie FROM mascotas  
WHERE id IN (  
    SELECT DISTINCT mascota_id FROM citas  
);

- **DISTINCT** --> hace que no muestre  cosas repetidas, en esta consulta los ID 
- **TRUNCATE**  --> 


## Joins

Trae informacion de tablas relacionadas. Combinacion de tablas relacionadas, tenemos 4 tipos:

1. **INNER JOIN**
2. **LEFT JOIN
3. **RIGHT JOIN**
4. **FULL OUTER JOIN**



### INNER JOIN
Solo nos devuelve las **las filas que coinciden en ambas tablas!**

```
SELECT m.nombre, c.nombre AS clase
FROM miembros AS m
INNER JOIN inscripciones_clases AS ic ON m.id = ic.miembro_id
	INNER JOIN clases AS c ON ic.clase_id = c.id
```


### LEFT JOIN
Devuelve todas las filas de la izquierda!!! la de la izquierda seria cuando colocamos <mark class="verde">FROM ( nombre de la tabla)</mark>

- En caso de no haber coincidencias las columnas de la derecha quedan **null**.
- **nota --> lo usamos mucho para encontrar registros hurfanos ❌**

<mark style="background:#9254de">EJEMPLO</mark>

```
SELECT m.nombre, mem.fecha_inicio
FROM miembros AS m
LEFT JOIN membresias AS mem ON m.id = mem.miembro_id
```

