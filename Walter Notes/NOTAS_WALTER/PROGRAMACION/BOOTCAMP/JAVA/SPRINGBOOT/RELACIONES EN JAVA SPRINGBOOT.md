 # Relaciones entre entidades
esto es fundamental a la hora de crear entidades, tenemos que tener en cuenta que son las mismas relaciones de las **bases de datos**

1. <strong class="rosa-encendido">@ManyToMany</strong>
2. <strong class="rosa-encendido">@OneToOne</strong>
3. <strong class="rosa-encendido">@OneToMany o @ManyToOne</strong>

<mark class="verde">
NOTA --> *Para la relacion de ManyToMany, necesitamos siempore una tabla intermediaria, donde normalmente tenemos los id o las PRIMARY KEY de las otras tablas</mark>*

 ****
 Recordamos que las relaciones entre la entidades en JAVA se hacen con JPA/ Hibernate, pero que son estas?


- <mark class="naranja">JPA --> son las anotaciones para hacer todo posible</mark>
- <mark class="verde">Hibernate --> ejecuta o traduce todo a SQL.</mark> ✅


Tenemos el siguiente esquema para entender
1. **Codigo** 
2. **JPA** ( *anotaciones y las reglas! @Entity, @Table*)
3. **Hibernate** (*Este es donde hace un mapeo, mapeo es relacionar los datos con cosas coherentes. ✅*)

		continuando con hibernate, mapea de **CLASES  --> TABLAS (SQL) **


4. **SQL**


****

## Anotaciones indispensables
anotaciones indispensables para hacer las relaciones entre las tablas!

- <mark class="verde">@Entity / @Table</mark>
Define que es una entidad y quie tambien esata clase es una **tabla** en la base de datos


- <mark class="naranja">@Id / @GeneratedValue</mark>
Se define la clave primaria, recordemos que cada tabla necesita una tabla primaria como tal.













****

# ANOTACIONES (SERVICE)

<mark class="naranja">@Transactional </mark>
Todo lo que este seleccionado o un metodo que tenga esto, se le asigna que solo se ejecutara en una transaccion.

