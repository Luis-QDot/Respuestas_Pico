#### Description

Can you find the flag in [file](https://jupiter.challenges.picoctf.org/static/fae9ac5267cd6e44124e559b901df177/strings) without running it?

Primero obtenemos nuestro archivo del link con wget
hacemos un strings a nuestro strings y nos da muchisimo texto, a lo cual vamos a filtrar todo el texto usando grep y vamos a buscar la bandera
Luiscat02-picoctf@webshell:~$ strings strings |grep pico
picoCTF{5tRIng5_1T_7f766a23}
Luiscat02-picoctf@webshell:~$ 

Y ahi esta nuestra bandera
	**NOTAS ADICIONALES:**

- Comando `strings`: Muestra todas las secuencias de caracteres legibles dentro de un archivo binario.
- Comando `grep`: Filtra el texto y muestra las líneas que contienen el patrón de búsqueda.

**BANDERA:**  
==picoCTF{5tRIng5_1T_7f766a23}==
