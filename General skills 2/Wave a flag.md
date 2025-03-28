#### Description

Can you invoke help flags for a tool or binary? [This program](https://mercury.picoctf.net/static/a14be2648c73e3cda5fc8490a2f476af/warm) has extraordinarily helpful information...


Unas de las pistas que nos dan son estas
This program will only work in the webshell or another Linux computer.
-Run this program by entering the following in the Terminal prompt: `$ ./warm`, but you'll first have to make it executable with `$ chmod +x warm`
-Not every program implements help features like -h and --help.

Soluciones


Primero descargamos nuestro archivo con wget
luego usamos el chmod +x para ejecutar el archivo

Luiscat02-picoctf@webshell:~$ chmod +x warm
Luiscat02-picoctf@webshell:~$ ./warm
Hello user! Pass me a -h to learn what I can do!
Luiscat02-picoctf@webshell:~$ 

Luiscat02-picoctf@webshell:~$ ./warm -h
Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_755f3544}
Luiscat02-picoctf@webshell:~$ 
y nos da la bandera


**NOTAS ADICIONALES:**

- El comando `chmod +x` otorga permisos de ejecución a un archivo.
- El programa `warm` ofrece la bandera al ejecutar el flag `-h`.

**BANDERA:**  
==picoCTF{b1scu1ts_4nd_gr4vy_755f3544}==

Referencias
https://www.youtube.com/watch?v=uA_ZSCwEZlg&pp=ygUUV2F2ZSBhIGZsYWcgIHBpY29jdGY%3D
