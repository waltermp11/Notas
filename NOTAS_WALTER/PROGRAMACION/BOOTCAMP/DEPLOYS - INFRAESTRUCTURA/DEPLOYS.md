# Deploys
Que todo no quede a nivel local, sino que quede disponible para todo el mundo.


<strong class="rosa-encendido">deploy en JAVA</strong>
- no es facil
- todo es de cobro.
- tiene mas condiciones.


<strong class="rosa-encendido">DONDE PODEMOS HACER DEPLOYS?</strong>
- supabase
- render



****
## Recomendaciones


![[Pasted image 20260914095309.png|587]]


## RENDER
- Toca pagar, la BD solo dura 7 dias.
- No permanece la BD.
-


## SUPABASE
es un programa donde podemos crear aplicacion  ( *deploys*).

- permite a los desarrolladores crear aplicaciones completas sin tener que **programar o configurar un servidor desde cero**




****
# DOCKER
Empaquetar todo el codigo, para que sea llevado de un lugar a otro.

- <mark class="naranja">si funciona en una maquina --> funciona en todas
</mark>


<strong class="rosa-encendido">
QUE HACE DOCKER?</strong>
Empaquetar todo nuestro proyecto como tal

- <mark class="verde">versiones</mark>
- <mark class="verde">dependencias</mark>
- <mark class="verde">librerias</mark>



## Dockerfile
Tiene las instrucciones de que va a ejecutar, copia, revisa y hace lo correspondiende, como ultimo ejecuta 🏃



- <mark class="naranja">Vamos a tener nuestro backend en render</mark>.





***

## CONFIGURACION DE CORS
(*Cross- Origin Resource Sharing*)

- mencanismo de seguridad del navegador que bloquea como tal las solicitudes entre origenes distintos! ✅


<mark class="verde">ejemplo</mark>
- *Hacer POST desde cualquier parte como tal*.



![[Pasted image 20260914095652.png]]





****
## El orden importa
Casa paso depende del anterior, si se hace en otro orden, habran <mark class="naranja">dependencias</mark> <mark class="naranja">faltantes</mark>

1. **SUPABASE**
2. **RENDER**
3. **GITHUBPAGES**


Primero en supabase
- creacion de cuenta
- credenciales y conectar al servicio en linea
- le damos click en connect
-



![[Pasted image 20260914101729.png]]


![[Pasted image 20260914101801.png]]

- <mark class="verde">copiamos la URL que esta abajo</mark> : postgresql://postgres.jxdmculcyeavxzywerxb:[YOUR-PASSWORD]@aws-0-ca-central-1.pooler.supabase.com:5432/postgres



### CONFIGURACION DE APPLICATION.PROPERTIES


![[Pasted image 20260914102156.png]]



### PARA DAR PERMISO DESDE PARA EL REPOSITORIO 

![[Pasted image 20260914103500.png]]



## RENDER
Tenemos que crear un repositorio solo para el backend como tal, continuando con el render: 


![[Pasted image 20260914105343.png]]





****
## EJEMPLO DE APPLICATION PROPERTIES


![[Pasted image 20260914110730.png]]



### VARIABLES DE ENTORNO
- SPRING_DATASOURCE_URL
- SPRING_DATASOURCE_USERNAME
- SPRING_DATASOURCE_PASSWORD
- JWT_SECRET
	- JWT_EXPIRATION

![[Pasted image 20260914111259.png]]