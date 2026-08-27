
# <font color="#e36c09">Springboot</font>

**Que es un bean?**
- un objeto que es creado por spring, que hace lo siguiente:
	- Guarda 
	- Gestiona este mismo mantiene una **instancia preparada bajo la manga**


**Springboot y spring es lo mismo?**
- <mark class="verde">no</mark>, ya que spring es el framework como tal, pero antes era muy complejo de organizar *( como un promedio de 2dias)*
- *Springboot es una herramiente de spring*, donde ya se viene configuracion para ejecutarlo, antes era con un XML


**Por que manejamos anotaciones en Springboot?** **y que nos permiten hacer las anotaciones?**
- Es propio del framework spring boot las <mark class="verde">anotaciones</mark>
- estas nos pertmiten :


|       **Darle un rol a una clase**        | Algunos ejemplos ede darle un rol a la clase:<br><br>- <font color="#938953">@RestController :</font><br>esta clase es un controlador web, que establece que esa clase va<br><br>           - recibir peticiones web<br>					 - **devuelve datos**<br><br><br>-<font color="#e36c09">@Repository:</font><br>Esta clase conecta a la base de datos.<br><br> |
| :---------------------------------------: | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **mapear rutas - Establecer una funcion** | <font color="#e36c09">**@GetMapping:**</font><br>- cuando alguien entre a una URL, ejecuta este metodo.<br>- En este caso <mark class="verde">@GetMapping</mark> lo que hace es traer informacion, en formato JSON como normalmente es.                                                                                                                    |
|         **Inyectar dependencias**         |                                                                                                                                                                                                                                                                                                                                                            |




## Definiciones

### **Que es un endpoint?**
<mark class="verde">direccion o url</mark>lde nuestro backend, este endpoint responde a una peticion:

**ejemplo**
api/saludo/saludo_1
## Manejo de capas en SpringBoot

**Por que es importante el manejo de Capas en SpringBoot?**


- <mark class="verde">Controller</mark>
- <mark class="verde">Service</mark>
- <mark class="verde">Repository</mark>
- <mark class="verde">Model</mark>

**que hacemos en controller?**



### 
### Inyeccion de independencias


Las independencias nos ayudan a hacer el trabajo mas rapido, no tener que crea todo como nuevo.


### Inyeccion de dependecias por constructor

seria casi que una instancia, en este caso, **tenemos un atributo final tipo Objeto objeto**



### Preparar las capas de las reglas




