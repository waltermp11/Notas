# NO RELACIONALES
Datos flexibles.

## Tabla de Contenido

[[#TIPOS DE BASES DE DATOS NO RELACIONALES]]
- [[#DOCUMENTO]]
- [[#CLAVE / VALOR]]
- 

<strong class="rosa-encendido">nota 
En las no relacionales el ID es tipo String</strong> ✅

<mark class="verde">Ejemplo</mark>
- Desarrollo de un blog, donde un desarrollador quiere mostrar sus proyectos.


<mark class="verde">
CARACTERISTICAS DE LAS NO-RELACIONALES</mark>
la informacion entra de muchas maneras.

- Hay una base de datos, donde no interactua con todos los datos como tal! --> estas son las *NoSQL o no relacionales*
-  Tengo que pensar que se usa mas o necesita desarrollar.



****

## TIPOS DE BASES DE DATOS NO RELACIONALES

1. **Documento** --> formato Json
2. **Clave - valor**
3. **columna anacha** 
4. **Grafo**



## <strong class="rosa-encendido">EXPLICACION</strong> TIPOS DE NO RELACIONALES

### DOCUMENTO
Json, listas y objetos anidados. Se comporta a medida que lo voy usando. 

<strong class="rosa-encendido">**usado para:**</strong>
- perfiles
- catalogos
- contenido de forma variable

Ejemplo --> MondoDB - couchbase


****

### CLAVE / VALOR

usado para :
- sesiones
- cache
- carritos temporales.

### COLUMNA ANCHA
Son conjuntos de distinas columnas.

<mark class="naranja">
Para entender columna ancha:</mark>
- Tenemos nombre, apellido, direccion y correo
- puedo llamar estos (4 datos y ponerle "*Informacion Personal " *)
- Entonces


### GRAFO
tiene varias variantes como tal.

Lo usamos para:
- redes sociales
- Recomendaciones.

<mark class="verde">ejemplo</mark> :
"*Tenemos varias consistencias, donde seria, una persona le gusta varias cosas y muchas personas tambien comparten esos gustos como tal.*"

- una red social, a una persona le gusta bateria y tambien le gusta la comida, pero tambien el GYM

 
![[Pasted image 20260914045317.png|700]]




****
## NOTA
#no_relacionales
NINGUNA ES MEJOR QUE OTRA, SOLO DEPENDE DE NOSOTROS QUE NECESITAMOS PARA QUE TODO FUNCIONE CORRECTAMENTE.

****
## QUE DATOS VIVEN JUNTOS?
Tenemos como relaciones propias en cuanto a las **bases de datos no relacionales**.


- <mark class="naranja">Como vamos a entender el comportamiento?</mark> --> de que un usuario le pertenecen las cosas.


<mark class="verde">
Ejemplo</mark>
*Una publicacion con comentarios, tenemos un JSON el ID no es long, sino que es String en las bases de datos no relacionales.*
****


## RELACION DE CONCEPTOS 
Aclaracion de bases de datos
![[Pasted image 20260914073015.png]]



****

## MONGO DB
Entendemos que se tiene que conectar a la nube, <mark class="naranja">pregunta, se puede desarrollar a nivel local?</mark>

- creamos la cuenta
- configuracion pertinente de la pagina




![[Pasted image 20260914074729.png]]

### NOTA 
*Verificar como se puede ejecutar mongo a nivel local*