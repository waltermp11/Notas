# Taller 4

Repaso y aplicacion de los Inner join.



## INNER JOIN
1. Query

	![[Pasted image 20260825150230.png|654]]

	```
	SELECT c.nombre AS "Nombre Clase", c.duracion_minutos AS "Duracion", i.nombre_completo FROM clases as c
	INNER JOIN instructores as i ON i.id = c.instructor_id
	WHERE i.estado = true;
	
	```


2. Query

	![[Pasted image 20260825150329.png]]

	```
	SELECT mem.nombre AS "Nombre Miembro", c.nombre AS "Nombre Clase " FROM miembros AS mem
	INNER JOIN inscripciones_clases AS ins ON mem.id = ins.miembro_id
	INNER JOIN clases AS c ON c.id =ins.clase_id; 
	
	```

3. Query


	![[Pasted image 20260825151403.png]]

```
	SELECT m.nombre AS "Nombre Miembro", p.nombre_plan AS "Nombre del Plan",p.precio_mensual AS "Precio" FROM miembros AS m
INNER JOIN membresias as mem ON m.id = mem.miembro_id
INNER JOIN planes as p ON p.id = mem.plan_id;
```


4. Query

![[Pasted image 20260825152457.png]]

```
SELECT m.nombre AS "Nombre Miembro", c.nombre AS "Nombre Clase", i.fecha_registro AS "Fecha inscripcion" FROM miembros AS m
INNER JOIN inscripciones_clases AS i ON m.id = i.miembro_id
INNER JOIN clases AS c ON i.clase_id = c.id
WHERE i.asistencia = true
ORDER BY "Fecha inscripcion" DESC;
```



![[Pasted image 20260825154535.png]]

```
SELECT c.nombre AS "Nombre Clase", COUNT(i.miembro_id) AS "Total inscritos" FROM clases AS c
INNER JOIN inscripciones_clases AS i ON c.id = i.clase_id
GROUP BY c.id, c.nombre
ORDER BY "Total inscritos" DESC;`
```




## LEFT JOIN

![[Pasted image 20260825155538.png]]

```
SELECT m.id, m.nombre
FROM miembros AS m
LEFT JOIN inscripciones_clases AS ins ON m.id = ins.miembro_id
WHERE ins.id IS NULL;
```



![[Pasted image 20260825155751.png]]

```
SELECT i.nombre_completo AS "Nombre completo", i.especialidad
FROM instructores AS i
LEFT JOIN clases AS c ON i.id = c.instructor_id
WHERE c.id IS NULL;

```

![[Pasted image 20260825155902.png]]

```
SELECT m.nombre AS "Nombre Miembro", COUNT(ic.id) AS total_clases
FROM miembros AS m
LEFT JOIN inscripciones_clases AS ic ON m.id = ic.miembro_id
GROUP BY m.id, m.nombre
ORDER BY total_clases DESC;
```


![[Pasted image 20260825160017.png]]

```
SELECT m.nombre AS "Nombre Miembro", mem.plan_id, mem.fecha_inicio, mem.fecha_vencimiento
FROM miembros AS m
LEFT JOIN membresias AS mem ON m.id = mem.miembro_id
WHERE mem.estado_pago = FALSE;
```


## RIGHT JOING

![[Pasted image 20260825160335.png]]

```
SELECT  c.nombre AS "Nombre Clase", c.capacidad_participantes
FROM inscripciones_clases AS ins
RIGHT JOIN clases AS c ON ins.clase_id = c.id
WHERE ins.id IS NULL;
```



![[Pasted image 20260825160523.png]]

```
SELECT c.nombre AS "Nombre Clase", COUNT(ic.id) AS total_inscritos
FROM inscripciones_clases AS ic
RIGHT JOIN clases AS c ON ic.clase_id = c.id
GROUP BY c.id, c.nombre
ORDER BY total_inscritos DESC;
```

## FULL OUTER JOIN

![[Pasted image 20260825160609.png]]

```
SELECT m.nombre AS "Nombre Miembro", mem.fecha_inicio FROM miembros AS m
FULL OUTER JOIN membresias AS mem ON m.id = mem.miembro_id;
```


![[Pasted image 20260825161113.png]]

```
SELECT i.nombre_completo AS "Nombre Instructor", c.nombre AS "Nombre Clase" FROM instructores AS i
FULL OUTER JOIN clases AS c ON i.id = c.instructor_id
WHERE i.id IS NULL OR c.id IS NULL;
```

![[Pasted image 20260825161134.png]]

```
SELECT m.nombre AS "Nombre Miembro", c.nombre AS "Nombre Clase",  ins.nombre_completo AS "Nombre Instructor" FROM inscripciones_clases AS ic
INNER JOIN miembros AS m ON ic.miembro_id = m.id
INNER JOIN clases AS c ON ic.clase_id = c.id
INNER JOIN instructores AS ins ON c.instructor_id = ins.id
ORDER BY m.nombre ASC;
```


![[Pasted image 20260825161647.png]]


```
SELECT i.nombre_completo AS "Nombre Instructor", i.especialidad,  COUNT(ic.id) AS total_inscritos FROM instructores AS i
INNER JOIN clases AS c ON i.id = c.instructor_id
INNER JOIN inscripciones_clases AS ic ON c.id = ic.clase_id
GROUP BY i.id, i.nombre_completo, i.especialidad
ORDER BY total_inscritos DESC
LIMIT 1;
```



![[Pasted image 20260825161957.png]]

```
SELECT m.nombre AS "Nombre Miembro", m.email, mem.fecha_vencimiento
FROM miembros AS m
INNER JOIN membresias AS mem ON m.id = mem.miembro_id
INNER JOIN planes AS p ON mem.plan_id = p.id
WHERE p.nombre_plan = 'Plan VIP' 
AND mem.estado_pago = TRUE;
```


![[Pasted image 20260825162029.png]]

```
SELECT c.nombre AS "Nombre Clase", i.nombre AS "Nombre Instructor", COUNT(ic.id) AS total_asistentesFROM clases AS c
INNER JOIN instructores AS i ON c.instructor_id = i.id
LEFT JOIN inscripciones_clases AS ic 
ON c.id = ic.clase_id AND ic.asistio = TRUE
GROUP BY c.id, c.nombre, i.nombre;
```


![[Pasted image 20260825162238.png]]

```
SELECT  c.nombre AS "Nombre Clase", i.nombre_completo AS "Nombre Instructor", COUNT(ic.id) AS total_asistentesFROM clases AS c
INNER JOIN instructores AS i ON c.instructor_id = i.id
LEFT JOIN inscripciones_clases AS ic 
ON c.id = ic.clase_id AND ic.asistencia = TRUE
GROUP BY c.id, c.nombre, i.nombre_completo;

```

 