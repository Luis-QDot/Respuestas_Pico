Para este ejercicio vamos a abrir la consola 
#### Description

Can you find the flag in [file](https://jupiter.challenges.picoctf.org/static/315d3325dc668ab7f1af9194f2de7e7a/file)? This would be really tedious to look through manually, something tells me there is a better way.


Solucion

Copiamos el lnk del archivo y damos wget para descargarlo 
Luiscat02-picoctf@webshell:~$ wget https://jupiter.challenges.picoctf.org/static/315d3325dc668ab7f1af9194f2de7e7a/file
--2025-03-14 17:15:52--  https://jupiter.challenges.picoctf.org/static/315d3325dc668ab7f1af9194f2de7e7a/file
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 14551 (14K) [application/octet-stream]
Saving to: 'file'

file                                            100%[======================================================================================================>]  14.21K  --.-KB/s    in 0s      


vamos a hacerle un cat a nuestro documento usando el grep por lo cual vamos a ecribir

cat file | grep pico
y nos da la bandera
Luiscat02-picoctf@webshell:~$ cat file | grep pico 
picoCTF{grep_is_good_to_find_things_f77e0797}
Luiscat02-picoctf@webshell:~$ 

Notas Adicionales 
- **`cat file`** – Muestra el contenido del archivo llamado `file`.
- **`grep pico`** – Busca la palabra `pico` dentro del contenido mostrado por `cat`.
    - `pico` → Palabra clave que indica el formato de la bandera (`picoCTF{}`).


BANDERA
==picoCTF{grep_is_good_to_find_things_f77e0797}==