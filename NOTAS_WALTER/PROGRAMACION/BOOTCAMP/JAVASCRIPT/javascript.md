****
hoy vamos a ver el DOM




# TABLA DE CONTENIDO

1. [[#Document]]
2. [[#APIS - CONSUMO DE APIS]]
# Document
*el objeto como tal donde esta todo mi HTML! ✅*

- document.getElementById("*Aca iria el id de mi etiqueta*")
	- *Recordar que a traves de la dot notation ingresamos a todas las cosas*

****


# QuerySelector

- *selecciona el primer elemento con clase "demo-item"*
- querySelectorAll() --> Selecciona a todos los de esa clase.
-
![[Pasted image 20260722101945.png|800]]

****
# Otras formas de seleccionar

- getElementsByClassName ("ClaseName")
- recomendacion querySelector, querySelectorAll() y usamos el del getElementById(), en los proyectos modernos! ✅

![[Pasted image 20260722102236.png]]
****

## Propiedades que nosotros tenemos en JS 

tenemos las siguientes dos propiedades donde tenemos:

1. **textContent** 
2. **innerHTML**
## textContent

- Solo agrega texto en el HTML, invalida aun las etiquetas que aun estan ahi.
## innerHTML

- Agregar etiquetas en HTML.
- agrega lo que nosotros queramos a nuestro HTML
- lo usamos para renderizar paginas
-
![[Pasted image 20260722102517.png|717]]

![[Pasted image 20260722102740.png|704]]




****
# ClassList y Atributos

## Classlist 
- Tengo que entender que con ClassList podemos:
	- <mark class="naranja">Agregar</mark>
	- Quitar
	- Alternar

Pero todo orientado a las clases

## SetAttribute
Modifica un atributo personalizado


![[Pasted image 20260722103125.png|933]]


![[Pasted image 20260722103539.png|931]]

![[Pasted image 20260722104647.png]]

![[Pasted image 20260722105503.png|762]]


****

# APIS - CONSUMO DE APIS

una API es una aplicacion que interactua con **cliente y servidor**.

[[#TABLA DE CONTENIDO]]



## Conceptos Claves

- **Cliente servidor**
- **Endpoint**
- **Protocolo HTTP y Metodos**

| ***<mark style="background:#fdbfff">Cliente Servidor**</mark>*                 | 1. El cliente envia una peticion que se llama **<mark class="verde">request</mark>**<br>2. El servidor procesa la *<mark class="verde">*<mark class="verde">request</mark>**</mark><br>3. Devuelve una respuesta **<mark class="verde">response</mark><br><br><br><br>                                                                                                                                                                                                                                                      |
| :----------------------------------------------------------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <mark style="background:rgba(74, 82, 199, 0.2)">***EndPoint***</mark>          | Es la **url especifica** a la cual nosotros realizamos la peticion, tenemos los siguientes <mark class="verde">ejemplos:</mark><br><br>1. https://api.nasa.gov/planetary/apod<br>                                                                                                                                                                                                                                                                                                                                           |
| <mark style="background:rgba(74, 82, 199, 0.2)">***Protocolo HTTP y Metodos*** | **Traduccion de  --> hypertext Transf</mark>er Protocol**<br><br><br>- Nos ayuda a realizar peticiones de <mark class="verde">datos y recursos</mark><br><br>**METODOS**<br><br>1. <mark class="verde">GET</mark> -- solicitar / leer datos<br>2. <mark class="verde">POST</mark> -- Es cuando nosotros enviamos datos.<br>3. <mark class="verde">PUT / PATCH</mark> --Actualizacion de datos, que ya existian.<br>4. <mark class="verde">DELETE</mark> -- Aca es donde **borramos!** apartir de una solicitud.<br><br><br> |

**** 

# API - CONSUMO DE ESTAS

- Entendemos que es una API.


## API ( Application Programming Interface)
- Lo entendemos como  (*Interfaz de Programacion de Aplicaciones*)

Conceptos claves para el entendemiento  de consumo de APIs

- <mark class="azul-encendido">FETCH</mark>
- <mark class="azul-encendido">ASYNC</mark>
- <mark class="azul-encendido">AWAIT</mark>

****

## <mark class="naranja">FETCH</mark>

- <strong class="rosa-encendido">funcion integrada de JavaScript</strong>, ojo este nos sirve para solicitar las tipicas situaciones:
	- <mark class="verde">GET, POST, DELETE, PUT</mark>
	- Esta función integrada --><mark class="verde"> SIEMPRE RETOMA UNA PROMESA</mark>


<mark class="azul-encendido">
EJEMPLO</mark>
- Aca estamos consumiendo el LINK de la API, nosotros podemos tener vario consumos de APIs
```
fetch(`https://jsonplaceholder.typicode.com/users/${id}`);
```


**** 
## <mark class="naranja"> ASYNCRONO --> ASYNC ()</mark>

Bueno, esto es un tipo de funcion, tenemos que entender que JavaScript es:

- <mark class="naranja">JavaScript</mark> --> solo puede hacer una cosa a la vez.
- también tenemos que tener en cuenta que **PEDIR DATOS A UN SERVIDOR ES UNA TAREA PESADA**

	- *Pedir información a una API*
	- *Leer un archivo pesado*
	- *Pedir información a un servidor*
 


### <mark class="verde">ASINCRONIA --> ASYNC</mark> 
- Se delega la tarea en segundo plano.
- Continua ejecutando el resto de codigos

Entonces cuando la informacion llega --> se renderiza la informacion! ✅


****

## AWAIT
Tenemos que entender que es una palabra reservada que solo sea usa en la <mark class="naranja">funcion asincrona</mark>

- --> AWAIT para la funcion hasta que se resuelva o se tenga una promesa.

