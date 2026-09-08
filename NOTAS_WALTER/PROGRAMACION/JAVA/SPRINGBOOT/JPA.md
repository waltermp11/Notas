# Spring DATA JPA
vamos a tener como conectar nuestro proyecto a la base de datos.

actualmente no tenemos persistencia -- o sea los datos se nos pierden. Cuando reiniciamos la aplicacion pues no vemos datos.


# ORM (Object Relational Mapping)
objetos de java los convierte en tablas ( entidades), tambien:

<mark style="background:#b1ffff">NOTA --> Casi todos los lenguajes de backend que tienen datos persistentes, tienen un ORM en bases de datos relacionales.</mark>

- **traduccion, soloamente hace traduccion** de clases a las tablas!
	- Clase  -- entidad
	- atributos -- columnas


**El ORM se encarga de hacerlo automaticamente, nosotros no lo hacemos manualmente**



# JPA AND HIBERNATE

- **jpa** -- nos da especificacion, reglas, instrucciones en como se tienen que hacer las cosas.
- **Hibernate** --> cumple las reglas y genera las tablas en SQL ( *lo hace real*)




**Donde creamos las tablas?**
las creamos normalmente de JAVA

## Cambios desarrollador

- repository es una interface. 




## LOMBOK 

- Eliminia el codigo mecanico
- Libreria que nos ayuda en vez de crear tanto codigo sino a desarrollar anotaciones! 
- Hace como tal **codigo limpio y ahorramos lineas ya por su funcion por debajo.**
	

![[Pasted image 20260828111050.png]]