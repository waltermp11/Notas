

# MVC - Modelo vista controlador

- Estandar mas usado para construir aplicaciones WEB.
- Separa responsabilidades del software en --> **capas**

**por que capas?**
*Es por capas, para que sea modular (<mark class="verde">dividido en partes independientes, especializadas para tareas especificas</mark>), mantenible y escalable*



**Como aplicamos este patron de diseño y que es este?** 

- Tenemos la siguiente distribucion referente al Patro de diseño.
- Entender que es una arquitectura como tal --> seleccionada
- **Tambien** --> <mark class="verde">Springboot conoce mas este framework como tal, trabaja mejor</mark>. ✅

<mark style="background:#fdbfff">**NOTA --> BUSCAR QUE ARQUITECTURAS NOSOTROS TENEMOS DISPONIBLES PARA DESARROLLAR**</mark>



- **DELEGACIONES** -- **CAPAS** --> pensamos en ahora den adelante quie son las carpetas comot al



![[Pasted image 20260901162614.png|590]]


![[Pasted image 20260829153045.png|886]]





## EJEMPLO DE COMO SE VEE LA ESTRUCTURA

com.nombreaplicacion.vetCare

- **Controller** --> gestiona las peticiones ( recibe y manda)
- **Service** --> tenemos la logica y reglas del negocio 🗿
- **repository** --> Es la que interactua con la base de datos 📊
- **model** --> Aca tenemos las entidades 🪪 
<mark class="verde">
Recordando que en model a futuro es donde se vana  desarrollar las columnas de nuestra base de datos</mark>

- **dto** --> Data transfer Object ( DTO de salida y DTO de entrada, como entra y sale y con sus respectivas validaciones JSON)




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


*Ejemplo de reglas de negocio --> <mark class="verde">si pasa x entonces que sucede y</mark>*

![[Pasted image 20260829152454.png|651]]



### **LOGICA DE NEGOCIO**

procedimiento o flujo de pasos, aca si tenemos codigo.

*ejemplos:*

![[Pasted image 20260829152837.png|436]]




## 3. Repository

Es la que trabaja o interactua unicamente con la base de datos!!!!!!


**nota -->**
Repository al interactuar directamente con la base de datos, cuenta ya con **metodos desarrollados ya anterioemente**


- <mark class="verde">Buscar por Id</mark>
- <mark class="verde"> Listar todos</mark>
- <mark class="verde">eliminar para ID</mark>




****

## COMO SERIA UN LOGIN?
Nosotros tenemos que tener en cuenta que :

1. Tenemos una entidad llamada **usuario** 👤
2. Tenemos DTOs, que nos ayudan a ver como recibimos y como damos salida a ese dato.
3. Nunca retornamos la password en un dto. --> seguridad obviamente 🔐



**DTO --> DATA TRANSFER OBJECT**
- cada entidad tiene una salida y entrada de datos. ✅
- En los DTOs encontramos validaciones de campos, si como si fuera un *FRONT, donde validamos cantidad de caracteres, que no sea null y entre otras.*


