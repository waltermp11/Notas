# Actividades desarrolladas junto a la IA

- Lectura, analisis de texto y tambien la clasificacion. Tambien tenemos reumen y revision de codigo.
- Descripcion de procesos y analisis de codigo.
- <mark class="naranja">Casos de uso para cada tarea?</mark>



<mark class="verde">NOTA</mark> --> *Explicacion detallada y precisa a la hora de revisar correos con informacion, con el fin de automatizar las tareas.*



****
## NLP (*Procesamiento de Lenguaje Natural*) --> Podemos manejar tareas de lectura.


<strong class="rosa-encendido">Que tenemos que entender del NLP?</strong>
- Descompone el texto en partes.
- Identificacion de informacion importante.
Se hace para el gran flujo de informacion. (**volumenes altos de informacion**)




 <strong class="rosa-encendido">Como me puede ayudar precisamente?</strong>
- Clasificacion de texto
- analisis de Sentimientos ?
- Extraccion de palabras clave.
- Resumen de Texto
- Revision de Codigo.


## 1. Clasificacion de Texto
La idea es definir *grupos predefinidos,* con el fin de :

- <mark class="naranja">Priorizar tareas.</mark>
- Ahorrar tiempo (**Ordenar Correos**)
- Organizacion de archivos e informes.
- Automatizar los procesos.



## 2. Analisis de Sentimientos
Evaluacion del <mark class="verde">tono emocional en las plataformas de comunicacion o la retroalimentacion.</mark>

- Estado de animo del equipo
- Medicion de satisfaccion del cliente.
- <mark class="naranja">ANALISIS DE COMUNICACION?</mark>




## 3. Extraccion de Palabras Clave
- Identificar entidades especificas ( *Nombres, ubicaciones, fechas, u organizacion*)
- <mark class="verde">NOTA</mark> --> recolecion de datos en informes o contratos.





## 4. Resumen de Texto
- Condesacion de informacion
- resumen de documentacion (*con alguna tecnica?*)
- Resumen de Tickets grandes! ✅
- Resumenes detallado ( *Tenemos que ser especificos, donde depronto queremos hacer un enfasis.*)




## 5. Revision de Codigo

Lo usamos la la revision del codigo desarrollado, pero en:

- posibles problemas
- ineficiencias
- ERROREs
- Identificacion de Patrones en mi codigo.
- <mark class="verde">FEEDBACK</mark> --> la idea es pedirlo en nuestro codigo, para mejorar las habilidades de codificacion.


****
# PREPARACION DE MATERIAL 
La IA puede leer varios formatos a la hora de desarrollar tareas de lectura, resumir y mas cosas.


<mark class="verde"> CHATGPT</mark> 
- en la version gratis solo procesa **texto**
- Pago, entradas multimodales como texto, imagenes y audio. PDFs
	- DALL-E  --> la usamos para la creacion de imagenes.

<mark class="naranja">
PERPLEXITY AI</mark>
- gratis --> tenemos limitaciones en cuando a PDFs y multimedia sencilla ( *Solo 3 documentos por dia*)
- Pro --> archivos ilimitados, PDFs, CSV, imagenes y documentos de texto.
	- Analisis mejorados.




## MANEJO DE DOCUMENTOS COMPLEJOS

- Verificacion de encabezados claros 
- Verificacion de nombres, etiquetas, columnas con nombres especificos.
- Asegurar la consistencia de datos ( **Manejar los mismos formatos y tipos de datos en la columna**)
- <mark class="verde">Limpia los datos</mark> --> eliminar lo irrelevante de la base de datos.
- <mark class="naranja">Añade anotaciones o metados</mark>--> 
	- Esto es en caso de requerir<mark class="naranja"> Contexto adicional</mark>



# PREPARACION DE CODIGO PARA REVISION
- Codigo formateado --> <mark class="naranja">identado</mark>
- Manejar las convencionalidades de las variables y funciones.
- Evitar <mark class="verde">COMENTARIOS INNECESARIOS EN EL CODIGO</mark>






****
# formatos aceptados (legiblementes por la IA)


- PDFs --> menos vulnerables a los <mark class="naranja">malwares</mark>
- Markdown
- txt --> texto plano


 <strong class="rosa-encendido">al tener estos formatos, hagamos esta filtracion o acciones:</strong>
 
1. Eliminar contenido innecesario.
2. Podemos agregar definiciones -->
	- Como objetivo, que la IA me entienda mas facil (*dentro de los mismos parentesis del texto.*)
3. Anotaciones para explicacion y evitar malos entendidos de informacion.





****
# CLASIFICACION DE TEXTO
1. Categorias definidas --> 
2. <mark class="naranja">Modelado de temas </mark>

- Metodos de aprendizaje automatico no supervisado.
- Tenemos de pronto bastante contenido, donde no podemos identificar los temas o las categorias definidas.


![[Pasted image 20260911101650.png]]


****
# ANALISIS DE SENTIMINETOS
Tono emocional de un texto.
- usado para la evaluacion de comentarios de clientes.
- Entender el estado de la audiencia.


- ![[Pasted image 20260911102025.png]]


<mark class="verde">NOTA</mark>
- siempre revisar como es la salida.


****



## DESARROLLO DE ACTIVIDAD
- Implementar lo aprendido de lecturas html



# Revision de codigo

<mark class="verde">PROMPT</mark> 
hazme una revision de codigo, teniendo en cuenta

1. Estructura de codigo

2. Funcionalidad y detecta ambiguedades.

3. Verifica los errores mas visibles.

4. En caso de tener comentarios, revisalos cuales son pertinentes de que se queden en el codigo:


<mark class="verde">RESULTADO</mark>

**1. Estructura de código**

- **Errores de sangría (_IndentationError_):** En `send_email_reminder`, las líneas de `smtp_server` y `logging.info` tienen espacios adicionales desalineados respecto al bloque `try`. De igual forma, el `logging.warning` dentro del bloque `else` de `process_rsvps_and_reminders` está mal alineado respecto a su declaración `else:`.
    
- **Falta de modularidad y acoplamiento:** `process_rsvps_and_reminders` depende directamente de una variable global mutable (`guest_list`). Es mejor pasar la lista como parámetro.
    
- **Configuración del Logger:** Se utiliza el módulo `logging`, pero no está configurado explícitamente (`logging.basicConfig(...)`), por lo que los logs usarán el formato por defecto.
    

**2. Funcionalidad y ambigüedades**

- **Manejo de claves opcionales en Diccionarios:** Acceder con `guest['phone']` o `guest['rsvp']` lanza un `KeyError` si la clave no existe en alguno de los elementos de la lista. Conviene usar `.get('key')`.
    
- **Credenciales hardcodeadas:** Hay un usuario y contraseña en texto plano en la conexión SMTP. Deben extraerse hacia variables de entorno.
    
- **Manejo de conexión SMTP poco seguro:** Si `sendmail()` o la autenticación fallan, la conexión nunca se cierra con `quit()` o `close()` porque no se utiliza un context manager (`with`).
    
- **Lógica de envío síncrono:** Procesar la lista de forma puramente secuencial (mismo hilo/proceso) bloqueará la ejecución por cada latencia de red en las llamadas SMTP o API de SMS.
    

**3. Errores más visibles y corregibles**

- **`IndentationError`:** Bloqueará la ejecución en Python antes de correr cualquier línea de código.
    
- **Ausencia de `Context Manager` (`with`):** Podría dejar conexiones colgadas en el servidor SMTP en caso de excepciones durante el envío.
    
- **Falta de cifrado TLS desde el inicio:** Abrir el puerto 587 requiere iniciar con TLS antes de autenticarse, pero `SMTP_SSL` o un bloque `with smtplib.SMTP(...)` con `starttls()` asegura la liberación correcta de recursos.
    

**4. Revisión de comentarios**

- `# Sample guest list` $\rightarrow$ **Innecesario.** Es evidente por el nombre de la variable.
    
- `# Send an email reminder` $\rightarrow$ **Innecesario.** El nombre de la función `send_email_reminder` ya lo expresa claramente.
    
- `# Replace with actual password` $\rightarrow$ **Innecesario/Riesgoso.** Se debe eliminar y reemplazar la práctica por variables de entorno.
    
- `# Send an SMS reminder (simulation)` $\rightarrow$ **Pertinente si se modifica.** Es útil para indicar de manera explícita que es un _mock_ o implementación de simulación temporal.
    
- `# Process RSVPs and send reminders` $\rightarrow$ **Innecesario.** Redundante con la firma de la función.


 ****
 
 # VIDEO
 - aplicacion de software.
 - Recopilacion de datos usuarios y metricas de rendimiento del backend
 - analisis claro de los datos
	 - gustar saber como se sientes los usuarios, herramientas, resaltar temas( satisfechos o frustrados)
	 - comparacion de rendimiento backend y los comentarios orientados al software.
	 - Proponer cambios para el analisis, enfocarnos para los problemas principales.
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 Cuando le pedimos a la Ia que encuentre hallazgos en ( *comentarios, opiniones*), de algun texto, lo que hacemos es siempre **es que destaque los hallazgos mas importantes.**


- <mark class="verde">Mencionar a la audiencia que voy a presentarle los hallazos, IMPORTANTES ✅</mark>

- Si la idea es mejorar --> hacer foco a <mark class="naranja">Los problemas clave y las soluciones propuestas.</mark>
- <mark class="verde">Generacion de preguntas</mark>
	- Preguntarme  si impulsa cambios inmediatos
	- influira en la toma de decisiones a un nivel superior?



<mark class="verde">NOTA</mark> --> Revision siempre del texto que mandamos a organizar






****

# APLICACIONES PARA DETECCION DE DOCUMENTOS DE IA



- Lumo AI --> verificacion de IA en un documento.
- claude code --> mejor para la generacion de codigo y seguir instrucciones.
- 





