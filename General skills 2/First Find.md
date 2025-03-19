#### Description

Unzip this archive and find the file named 'uber-secret.txt'

- [Download zip file](https://artifacts.picoctf.net/c/501/files.zip)

Primero descargamos nuestro archivo con wget
ahora vamos a hacer un ls paa ver nuestro archivo 
README.txt  big-zip-files  big-zip-files.zip  challenge.zip  drop-in  file  files.zip  flag  flagout.txt  ll
Luiscat02-picoctf@webshell:~$ 

una vez este ahi, vamos a usar unzip para descomprimirlo
y nos da 
Luiscat02-picoctf@webshell:~$ unzip files.zip 
Archive:  files.zip
   creating: files/
   creating: files/satisfactory_books/
   creating: files/satisfactory_books/more_books/
  inflating: files/satisfactory_books/more_books/37121.txt.utf-8  
  inflating: files/satisfactory_books/23765.txt.utf-8  
  inflating: files/satisfactory_books/16021.txt.utf-8  
  inflating: files/13771.txt.utf-8   
   creating: files/adequate_books/
   creating: files/adequate_books/more_books/
   creating: files/adequate_books/more_books/.secret/
   creating: files/adequate_books/more_books/.secret/deeper_secrets/
   creating: files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/
 extracting: files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/uber-secret.txt  
  inflating: files/adequate_books/more_books/1023.txt.utf-8  
  inflating: files/adequate_books/46804-0.txt  
  inflating: files/adequate_books/44578.txt.utf-8  
   creating: files/acceptable_books/
   creating: files/acceptable_books/more_books/
  inflating: files/acceptable_books/more_books/40723.txt.utf-8  
  inflating: files/acceptable_books/17880.txt.utf-8  
  inflating: files/acceptable_books/17879.txt.utf-8  
  inflating: files/14789.txt.utf-8   
Luiscat02-picoctf@webshell:~$ 

ahora vamos a buscar el archivo "uber secret.txt" que nos dice en la descripcion

vamos a usar el comando find files para que nos muestre nuestros archivos y seguido de eso vamos a filtarrlos usando el comando grep seguido del nombre de nuestro archivo secreto o uber-secret

Luiscat02-picoctf@webshell:~$ find files |grep uber-secret.txt
files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/uber-secret.txt
Luiscat02-picoctf@webshell:~$ 

una vez nos muestra su localizacion vamos a usar el cat para ver que tiene ese archivo 
Y ahi nos muestra nuestra bandera 
Luiscat02-picoctf@webshell:~$ cat files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/uber-secret.txt
picoCTF{f1nd_15_f457_ab443fd1}
Luiscat02-picoctf@webshell:~$ 


### NOTAS ADICIONALES
- **`wget [URL]`** – Descarga un archivo desde la URL especificada.
- **`unzip [archivo.zip]`** – Descomprime un archivo `.zip`.
- **`find [directorio]`** – Busca archivos y directorios dentro del directorio especificado.
- **`grep [expresión]`** – Filtra las líneas que coinciden con una expresión regular.
- **`cat [archivo]`** – Muestra el contenido de un archivo


### BANDERA


==`picoCTF{f1nd_15_f457_ab443fd1}`==
