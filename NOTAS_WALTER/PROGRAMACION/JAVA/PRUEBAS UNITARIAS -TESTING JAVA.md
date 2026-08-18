
# PRUEBAS UNITARIAS CON JUNIT 5


## Tabla de contenido
1. Pruebas unitarias




# Pruebas Unitarias - JUnit 5

<mark class="verde">Evaluacion de una parte del codigo</mark>, como una funcion o metodo, clase, se verificar los casos posibles que tiene que arrojar

- **rojo --> test no pasa**
- **verde --> el test pasa**

en caso, yo puedo re factorizar el codigo




## Pasos
- **<mark class="verde">Paso 1</mark>** -- fallo, la idea es verificar donde tiro error o el por que no paso
- **<mark class="verde">Paso 1</mark>** -- paso
- **<mark class="verde">Paso 1</mark>** -- refactorizamos, corrige y limpia codigo, hacerlo mas simple o mas claro.

****

## Mocks
- Los necesitamos para hacer pruebas.
- versiones falsas para realizar sistemas.


1. **Inicio con confianza**
2. **Falla confusa**
	- Falla de forma inesperada, no e sla logica es algo externo
3. **Base de datos -- dormida**
	- La BD estaba fuera de linea.
	- El sistema no estaba disponible no habia nada malo en el codigo.
	
4. **aparece un ayudante amigable.**
	- Usamos mock, **versiones falsas de sistemas reales.**

****
# MOCKS

**ejemplo: darle una caja de mock al rescate!**

1. <mark class="verde">Darle al chef una caja de mock </mark>: ingredientes falsos para que este mismo practique con ellos.
	1. sin demoras, sin fallas y solo practica.



### por que no siempre usamos ingredientes reales al hacer pruebas?

- El codigo como chef, las dependencias como ingredientes.

## Que es Maven?

- <mark class="verde">Maven es el gestor de dependencias de un proyecto en JAVA! </mark> --> Crear un proyecto entero o mejor dicho algo mas real.
- Tambien tenemos Graddle.

## Ejemplo para desarrollar en "mock" - MAVEN

1. Creamos el proyecto en intellij, pero seleccionamos **maven**.

	![[Pasted image 20260818094619.png|563]] 
2. Seleccionamos la siguiente opcion : 
	1. ![[Pasted image 20260818094710.png]]
3. Ahora nos genera un POM.xml, aca es donde nosotros vamos agregando las dependencias o las librerias necesarias de nuestro proyecto!!!
	1. ![[Pasted image 20260818095053.png]] 


4. en la parte de dependencias, agregamos las que nosotros necesitamos en nuestro proyecto :
	1. ![[Pasted image 20260818095224.png]]  


5. Vamos a descargar como tal **mockito** nuestra dependencia, la agregamos dentro de <mark class="verde">**dependencies**</mark>

	```
			<dependency>  
	    <groupId>org.mockito</groupId>  
	    <artifactId>mockito-core</artifactId>  
	    <version>5.11.0</version>  
	    <scope>test</scope>  
	</dependency>
	```
	
	![[Pasted image 20260818095538.png|987]]
	


6. Nosotros tenemos que tener los archivos organizados y las carpetas, con su adecuado enrutamiento (Path)
	- ![[Pasted image 20260818104719.png]]
		-
		 ![[Pasted image 20260818104634.png]]



![[Pasted image 20260818104811.png|767]]