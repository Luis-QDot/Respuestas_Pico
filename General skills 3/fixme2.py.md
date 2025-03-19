#### Descripción

Corrija el error de sintaxis en el script de Python para imprimir la bandera.[Descargar script de Python](https://artifacts.picoctf.net/c/4/fixme2.py)


algunas pistas son
-Para ver el archivo en el webshell, haga lo siguiente:`$ nano fixme2.py`
`str_xor`No es necesario realizar ingeniería inversa a la función para este desafío.

asi que empezamos descargando nuestro archivo con wget
lo empezamos ejecutando y nos da este error 
Luiscat02-picoctf@webshell:~$ python3 fixme2.py 
  File "/home/Luiscat02-picoctf/fixme2.py", line 22
    if flag = "":
       ^^^^^^^^^
SyntaxError: invalid syntax. Maybe you meant '==' or ':=' instead of '='?
Luiscat02-picoctf@webshell:~$ 
asi que toca hacerle un nano para inspeccionar el codigo

asi que inspeccionando el codigo modificamos esta linea del codigo 
if flag == "":
  print('String XOR encountered a problem, quitting.')
else:
  print('That is correct! Here\'s your flag: ' + flag)
  en el if == para que al ejecutarlo nos aparesca la bandera
  Y al correrlo ya nos da nuestra bandera
  Luiscat02-picoctf@webshell:~$ python3 fixme2.pyes
That is correct! Here's your flag: picoCTF{3qu4l1ty_n0t_4551gnm3nt_e8814d03}
Luiscat02-picoctf@webshell:~$ 
(Tiene otro nombre porque cuando lo cambien y lo guarde le di que Y a guardar con diferente nombre)


Bandera
==picoCTF{3qu4l1ty_n0t_4551gnm3nt_e8814d03}==