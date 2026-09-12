# JWT ( Json Web Token ✅🔐)
- <strong class="rosa-encendido">JSON Web Token</strong>
	- Estandan de formato compato donde esencialmente **TRANSMITIMOS***
			<mark class="verde">informacion de una forma segura</mark>!!! 🔐
	- Claramente la tranmision segura <strong class="rosa-encendido">Cliente y Servidor ( Objeto JSON enctriptado o sea un JWT)</strong>
- RFC --> 7519, es como donde establecen los estandare en la web. ✅



<strong class="rosa-encendido">COMO SE COMPONE EL TOKEN?</strong>
- <mark class="verde">Encabezado ( HEADER)</mark>
- <mark class="naranja">Carga util (PAYLOAD)</mark>
- <mark class="verde">Firma ( SIGNATURE)</mark>


# ENCABEZADO
- Tambien conocido como header
- Contiene dos propiedades fundamentales:

	- *Tipo de Token a utilizar*
	- *Firma de algoritmo al utilizar*

**Ejemplo**
![[Pasted image 20260910123321.png|483]]



# CARGA UTIL
Contiene la informacion --> codificados en JSON ( claims)

 - <mark class="verde">Tenemos la informacion que nosotros queremos transmitir.</mark>

*Ejemplo* --> *EL JSON Merito*

![[Pasted image 20260910124348.png]]

****

## Informacion plana
Tenemos la informacion clara en la URL

-
	