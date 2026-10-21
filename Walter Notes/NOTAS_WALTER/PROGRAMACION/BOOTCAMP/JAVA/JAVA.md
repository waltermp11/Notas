****


# Tabla de Contenido



1. [[#Variables y tipos de datos]] 
	1. [[#Datos primitivos]]
	2. [[#Conversiones]]
	3. [[#Truncar]]
	
****

# JAVA  - Lenguaje orientado a la programacion de Objetos

Lenguaje que la idea es escribir una vez y ejecutar en cualquier lugar. --> Java nace de esta premisa.

<mark class="verde"> Premisa - WORA</mark>



# Mas informacion

- Lenguaje orientado al desarrollo de OBJETOS.
- Es un lenguaje que se transforma en **byteCode**, entonces
	- Primero lee el codigo
	- segundo, ejecuta todo el codigo!


![[Pasted image 20260730113646.png]]


****
# Como funciona JAVA?

1. Codigo
2. Compilacion
3. ByteCode
4. JVM
5. Multiplataforma


![[Pasted image 20260730114442.png|413]]



Tenemos que entender que en Js y JAVA, no van por el mismo camino, Js, es con lenguaje interpretado. 




****
# Buenas Practicas

Van con UpperCammelCase, osea:

<mark class="verde">class name = UsuarioSpotify</mark>

- Clase
- interfaces



## Comandos 

- sout --> System.out.println( "Mensaje de texto)
- psvm --> ejecuta el metodo **public static void main**



**** 
# Asignacion de Variables en JAVA

Nosotros tenemos delimitaciones en java a la hora de crear variables:

## ejemplos

- int x = valor;
- String nombreUsuario = Walter;
- 



****

# Variables y tipos de datos

[[#Tabla de Contenido]]

Claramente necesitamos diferentes tipos de datos a la hora de almacenar ciertas variables.

- nombre -- string
- edad -- int
- saldo --decimal
- activa -- boolean


<mark class="verde">
Variable</mark>
espacio con nombre en memoria que guarda un tipo determinado.



## Datos primitivos

[[#Tabla de Contenido]]
Son llamados asi, porque son <mark class="verde">**predeterminados o ya llamados por le lenguaje**</mark>

![[Pasted image 20260805092026.png|940]]

![[Pasted image 20260805092916.png|812]]

- **byte**
- **short**
- **int** -- 32 bits
- **long** -- 64 bits, permite demasiados numeros
	- Al final del long siempre ponemos una L al final
- **float**
- **double** --> mas preciso
- **char**
- **boolean**



#Nota-Java <mark class="verde">no es un dato primitivo, es una clase! ✅</mark>


## Formas de Impresion

- utilizamos el comando **sout** Esto, nos tabula el metodo println()

	![[Pasted image 20260805094548.png|412]]


	![[Pasted image 20260805102723.png|853]]


## Conversiones
[[#Tabla de Contenido]]
Nosotros podemos decidir o hacemos que JAVA deecida por nosotros 

1. Entero --> decimal.
		![[Pasted image 20260805102911.png|529]]


2. double --> entero

	![[Pasted image 20260805103004.png|570]]


### Truncar 

Eliminar la parte decimal de mi valor, ejemplo:

- (int) 789 --> 7 truncar
-  Math.round(7.89) -->8

![[Pasted image 20260805103249.png|929]]

#Nota-Java truncar es diferente de redondear




****



![[Pasted image 20260805103830.png|1174]]


****

# Arrays en JAVA

Pendiente a organizar tema.







# Debugging

Ir probando mientras vamos ejecutando, donde paso a paso o bloque a bloque, verificamos como funciona las cosas.


![[Pasted image 20260806114132.png|473]]

- en **Scanner**, nosotros tenemos un problema al tener el nextInt();
	- cuando tenemos un <mark class="verde">nextInt()</mark> para que no haya salto  con los otros datos, lo que hacemos es agregar :
		- <mark class="verde">scanner.nextLine()</mark>




## Compilar no significa estar correcto ✅

- Solo es revision de codigo como tal.
- Tenemos los errores en JAVA


1. <mark class="verde">Error de Compilacion: </mark>
	no va a dejar a ejecutar como tal el programa.
	
	![[Pasted image 20260806114530.png|503]]

2. <mark class="verde">Error en Ejecucion - compilo bien ✅</mark>

	- Muestra el mensaje abajo despues de hacer la compilacion.
	- Seria mas error de **logica** que un error, casi siempre nos menciona la **ubicacion**
	
![[Pasted image 20260806114901.png]]


****

# Programacion Orientada a Objetos ( Clases, objetos y encapsulamiento)


- La POO, nos ayuda a evitar la <mark class="verde">**redundancia** de **creacion de datos innecesarios!**</mark> o sea, no mas variables casi que iguales.

	- <mark class="verde">Siempre debemos tener validaciones!</mark>
- POO -->Una forma de programar, aplicar la realidad en la programacion.
- Representacion.
- Junta sus caracteristicas ( atributos) y tambien sus funciones (metodos unicos o compartidos)



## Encapsulamiento
Una propiedad fundamental en la 

[[#Tabla de Contenido]]


- utilizamos private para que no todo el mundo acceda, solo a traves del metodo.
	- **private String nombre;**
	- **private double precioObjeto;**


## Metodos
Nosotros tenemos que tener en cuenta si es **HACE o DA**

- <mark class="verde">Hace</mark>
	- Hace operaciones, muestra resultados donde no necesitamos el valor posteriormente.
- <mark class="verde">Da:</mark>
	- Hace operaciones, pero lo que retorna normalmente lo necesitamos.




### Por que main lleva Static?




