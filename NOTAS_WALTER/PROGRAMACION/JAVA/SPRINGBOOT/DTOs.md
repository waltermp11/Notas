# DATA TRANSFER OBJECT

Relaciones entre entidades y  DTO --> tenemos que aprenderlas a hacer ( *relaciones en las bases de datos*)\

**Que tenemos que tener en cuenta**?
- RequestDTO
- ResponseDTO

Con estos dos, nosotros lo que hacemos es elegir que hacemos para cada uno. 
- **DTO entrada** --  los datos de entrada como tal, que si necesitm
- **DTO Salida** --  los datos que solamente queremos mostrar regun las reglas de negocio! ✅



****

## RECORD

- <mark class="verde">No todos los DTO seran tipo record</mark>
- construir una vez y leer siempre.

**Pero que es un Record?**
clase desde java 16, diseñana para almacenar datos *inmutables!*









****

# RELACIONES 

Donde una tabla se relaciona con tora, gracias a una columna. Aplicando las anotaciones, tenemos las siguientes:

1. ManyToOne
2. OneToMany
3. OneToOne
4. ManyToMany --> *Al poner esta relacion, solo crea una tabla intermedia como siempre, pero solo dejar poner el id ✅, solo enlazar*


*Ejemplo --> Tenemos un dueño tiene varias mascotas. OneToMany?*


### NOTA --> tenemos que tener cuidado en donde nosotros ponemos el @ManyToOne y la otra entidad con @OneToMany



****
## Configuracion de relaciones y sus cargas

![[Pasted image 20260831112724.png|556]]

- lazy --> carga lenta en la entidad, evita traer datos.
- Eager --> por defecto, siempre va a traer todos los datos.


**Nosotros no siempre necesitamos los datos del dueno de la mascota como tal, no se necesitan muchas veces todos los datos que se necesitan del dueno ✅
**


## MappedBy

Necesario para hibernate **diga quien es el padre o quien es el hijo como tal**

![[Pasted image 20260831112558.png|720]]

en la Clase Dueno, tenemos en cuenta que :

1. relacion de 1:n, 1 dueno tiene muchas mascotas
2. Establecemos nuestra etiqueta **@OneToMany**
3. MappedBy( "dueno") --> <mark class="verde">tenemos de bajo de el un atributo privado que serian todas las mascotas en formato de un array list.</mark>


![[Pasted image 20260831113821.png|488]]


![[Pasted image 20260831113917.png|751]]





# Transaccion