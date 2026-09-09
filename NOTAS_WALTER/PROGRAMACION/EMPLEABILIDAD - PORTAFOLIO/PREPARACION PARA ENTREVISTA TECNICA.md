# PREPARACION ENTREVISTA TECNICA - PREGUNTAS

1. **<strong class="rosa-encendido">Que es la programacion orientada a Objetos y diga cuales son los 4 pilares principales**</strong>

	La programacion orientada a objetos es un *paradigma de la programacion --> es una forma de estructurar  y resolver problemas mediante codigo.*

	ENTONCES, POO es un paradigma de codigo que estructura el codigo usando **objetos!!, combinando datos y Comportamientos**

**4 Pilares de la Programacion Orientada a Objetos**

- <mark class="verde">Encapsulamiento</mark>
- <mark class="verde">Herencia</mark>
- <mark class="verde">Polimorfismo</mark>
- <mark class="verde">Abstraccion</mark>

## Encapsulamiento
*Entendemos de que los datos solo se acceden por metodos como (getters and Setters) --> **Gracias a los modificadores PRIVATE en las variables de la clase***

## Herencia
La herencia es entenderlo como la vida real, hay un Padre donde tiene hijos, no es Padre si no tiene hijos.

- Lo traemos a la programacion tenemos **una clase Padre y tenemos clases Hijas**. (*una clase en programacion es una identidad, croquis, plantilla o molde donde nos basamos para tener los objetos*)

**Que se puede heredar?**
- <mark class="verde">Metodos</mark>
- <mark class="verde">Atributos</mark> ( *recordamos que es por modificadores --> **protected, private y public.***)

## Polimorfismo
Es fundamental en la harencia, es donde otras clases o moldes, tienen o heredan el mismo metodo **pero el metodo se comporta diferente en cada clase.**

- <mark style="background:#d2cbff">**ejemplo - cocinarPapas() -->**</mark> puede que en una misma franquicia como tal cocinar las papas, sea igual para todas, pero en otros locales, hacen tambien papas, pero las hacen de diferentes formas
## Abstraccion
Es un proceso donde ocultamos el proceso interno y <mark class="verde">solo importa lo que hace no como lo hace</mark>.



****
2. **<strong class="rosa-encendido">Cual es la diferencia entre == y el metodo .equals() en java</strong>?**

- <mark class="verde">el operador == --> </mark>
	- compara referencias de *memoria en objetos*. Apunta hacia el mismo espacio de memoria.
	- La idea es usar este solo cuando se trabaje con tipos primitivos.
		- (**int, boolean, double, char**, null)

<strong class="rosa-encendido">
**Pregunta condicional referente a esta, entonces porque si aplica usarlo en operaciones?</strong>**




- <mark class="verde">El metodo .equals () --></mark>
	- Compara el contenido o el valor logico de 2 objetos, ejemplo, 2 cadenas de texto aunque esten en distinas posiciones de memoria.
	- usar **.equals ()**, cuando quiera comparar contendio o el valor de un objecto ( *String, Integer, List o un objeto creado por mi*)




****

3. <strong class="rosa-encendido">**Que es springboot? y por que se utiliza en el desarrollo con java?**</strong>

<mark class="naranja">Springboot</mark> es una herramiente del framework spring, springboot es una herramienta ya configurada para que haya un despligue mas rapido.

**CON QUE FIN?**
con le fin de que solo nos importe la <mark class="verde">*logica de negocio, donde nosotros aplicamos el codigo como tal ( Procedimiento o el flujo de pasos).</mark>


****

4. <strong class="rosa-encendido">**Como funciona una API rest y que metodos HTTP principales conoces?**</strong>

- Tenemos el concepto de API claro, que es una aplicacion mediadora, que se comunica entre dos programas. 
- Manejando reglas **REST**


*REST --> son un conjunto de reclas y principiso de arquitectura para el  diseño de servicios web.*


**R** -- recursos que son entidades de mi programa, cada recurso tiene una url unica.

**E** --> Estandarizar los metodos o que sean generales. (**CRUD**)


**S** --> Stateless ( sin estado), que toda la informacions e pase en la solicitud (*que se entienda*), <mark class="verde">NO SE MANEJA UN RECUERDO</mark>`

**T** --> Transferencia apartir de formato JSON


Las peticiones HTTP que me se:

1. GET --> *Trae informacion*
2. POST --> *Sube informacion, registra, manda informacion desde el usuario*
3. DELETE --> *Borramos, nada mas ❌*
4. UPDATE --> *Actualizamos como tal ✅*



