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
![[Pasted image 20260722101945.png|1062]]

****
# Otras formas de seleccionar

- getElementsByClassName ("ClaseName")
- recomendacion querySelector, querySelectorAll() y usamos el del getElementById(), en los proyectos modernos! ✅

![[Pasted image 20260722102236.png]]
****

## Propiedades que nosotros tenemos en JS 

tenemos las siguientes dos propiedades donde tenemos:

1. textContent 
2. innerHTML

ahora definiendo como tal:

### textContent

- Solo agrega un texto, literalmente solo es texto


### innerHTML

- Agregar etiquetas en HTML.
- agrega lo que nosotros queramos a nuestor HTML
![[Pasted image 20260722102517.png|762]]


**Explicacion de como se comporta**
- 

![[Pasted image 20260722102740.png]]




****
# ClassList y Atributos

## Classlist 
- al pasar un activo como tal.

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

| ***Cliente Servidor***         | 1. El cliente envia una peticion que se llama **<mark class="verde">request</mark>**<br>2. El servidor procesa la *<mark class="verde">*<mark class="verde">request</mark>**</mark><br>3. Devuelve una respuesta **<mark class="verde">response</mark><br><br><br><br>                                                                                                                                                                                                                                               |
| :----------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| ***EndPoint***                 | Es la **url especifica** a la cual nosotros realizamos la peticion, tenemos los siguientes <mark class="verde">ejemplos:</mark><br><br>1. https://api.nasa.gov/planetary/apod<br>                                                                                                                                                                                                                                                                                                                                    |
| ***Protocolo HTTP y Metodos*** | **Traduccion de  --> hypertext Transfer Protocol**<br><br><br>- Nos ayuda a realizar peticiones de <mark class="verde">datos y recursos</mark><br><br>**METODOS**<br><br>1. <mark class="verde">GET</mark> -- solicitar / leer datos<br>2. <mark class="verde">POST</mark> -- Es cuando nosotros enviamos datos.<br>3. <mark class="verde">PUT / PATCH</mark> --Actualizacion de datos, que ya existian.<br>4. <mark class="verde">DELETE</mark> -- Aca es donde **borramos!** apartir de una solicitud.<br><br><br> |












