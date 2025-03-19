#### Description

Unzip this archive and find the flag.

- [Download zip file](https://artifacts.picoctf.net/c/503/big-zip-files.zip)
-
Primero vamos a abrir nustra consola y descargar el archivo con wget
y al hacer un ls para ver los archivos nos damos cuenta que tenemos el zip descargado 
Luiscat02-picoctf@webshell:~$ ls
README.txt  big-zip-files.zip  challenge.zip  drop-in  file  flag  flagout.txt  ll
Luiscat02-picoctf@webshell:~$ 
asi que vamos a descomprimir el archivo con el comando unzip 
Luiscat02-picoctf@webshell:~$ unzip big-zip-files.zip 
 y nos aparece muchisima informacion en la cual se encuentra la bandera, por lo cual vamos a usar elcomando grep -rl para filtrar lasa palabras que queremos encontrar
 a lo cual nos arroja la ubicacion por lo cual le vamos a hacer un cat a aesa ubicacion 
Luiscat02-picoctf@webshell:~$ grep -rl "pico" big-zip-files
big-zip-files/folder_pmbymkjcya/folder_cawigcwvgv/folder_ltdayfmktr/folder_fnpfclfyee/whzxrpivpqld.txt
Luiscat02-picoctf@webshell:~$ 


y al hacer eso arroja la bandera
Luiscat02-picoctf@webshell:~$ cat big-zip-files/folder_pmbymkjcya/folder_cawigcwvgv/folder_ltdayfmktr/folder_fnpfclfyee/whzxrpivpqld.txt
information on the record will last a billion years. Genes and brains and books encode **picoCTF{gr3p_15_m4g1c_ef8790dc}**
Luiscat02-picoctf@webshell:~$ 


### NOTAS ADICIONALES

- **`wget [URL]`** – Descarga un archivo desde la URL especificada.
- **`unzip [archivo.zip]`** – Descomprime un archivo `.zip`.
- **`grep -rl [palabra] [directorio]`** – Busca de forma recursiva (`-r`) archivos que contienen la palabra en un directorio.
- **`cat [archivo]`** – Muestra el contenido de un archivo.

 BANDERA
==`picoCTF{gr3p_15_m4g1c_ef8790dc}`==