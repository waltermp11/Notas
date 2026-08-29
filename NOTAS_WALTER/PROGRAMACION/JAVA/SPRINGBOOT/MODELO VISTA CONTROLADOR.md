

# MVC - Modelo vista controlador

**Como aplicamos este patron de diseño y que es este?** 

- Tenemos la siguiente distribucion referente al Patro de diseño.
- Entender que es una arquitectura como tal --> seleccionada, 

<mark style="background:#fdbfff">**NOTA --> BUSCAR QUE ARQUITECTURAS NOSOTROS TENEMOS DISPONIBLES PARA DESARROLLAR**</mark>




- **DELEGACIONES** -- **CAPAS** --> pensamos en ahora den adelante quie son las carpetas comot al


![[Pasted image 20260829153045.png|886]]


****
# Recomendaciones

En modo de informacion, nosotros tambien podemos ver un backend en **Python** --> gracias al framework **FASTAPI**




****
# Que sucede en springboot?

1. Tenemos que entender que springboot es una herramienta de spring
	1. Springboot se desarrollo porque antes se demoraba mucho desplegar java + spring --> springboot nos ayuda a evitar demorandonos con configuraciones.


# Manejo de responsabilidades

Nosotros tenemos capas, cada capa tiene una responsabilidad en mi programa!!!
Estas seriasn las 3 capas que normalmente trabajamos en el proyecto

1. **Controller**
2. **Service**
3. **Repository**



##  1. Controller

**funciones importantes**

- Recibe la peticiones (usuario) y devuelve la respuesta (parte del servidor).
- La solicitud viene desde el front y la respuesta es alojaba en el backend, despues es renderizada para el front.



## 2. Service

**principales funciones**

- Aca tenemos la logica del negocio y las reglas de negocio

### Pregunta
- **que es la logica y las reglas de negocio?**

### **REGLAS DE NEGOCIO**

Aca respondemos varias cosas, 
- *como opera la empresa, un ejemplo de reglas de negocio seria
- *Tambien una definicion seria las validaciones que nosotros desarrollamos para que todo pueda funcionar correctamente, descuentos y entre otras.*


*Ejemplod e reglas de negocio --> <mark class="verde">si pasa x entonces que sucede y</mark>*

![[Pasted image 20260829152454.png|651]]



### **LOGICA DE NEGOCIO**

procedimiento o flujo de pasos, aca si tenemos codigo.

*ejemplos:*

![[Pasted image 20260829152837.png|436]]




## 3. Repository

Es la que trabaja o interactua unicamente con la base de datos!!!!!!



