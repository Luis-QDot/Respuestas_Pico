#### Description

Can you look at the data in this binary: [static](https://mercury.picoctf.net/static/0f6ea599582dcce7b4f1ba94e3617baf/static)? This [BASH script](https://mercury.picoctf.net/static/0f6ea599582dcce7b4f1ba94e3617baf/ltdis.sh) might help!

Primero vamos a obtener los archivos de los links con wget 

Solucion

Luiscat02-picoctf@webshell:~$ chmod +x ltdis.sh 
Luiscat02-picoctf@webshell:~$ ./ltdis.sh static
Attempting disassembly of static ...
Disassembly successful! Available at: static.ltdis.x86_64.txt
Ripping strings from binary with file offsets...
Any strings found in static have been written to static.ltdis.strings.txt with file offset
Luiscat02-picoctf@webshell:~$ ls
README.txt  big-zip-files  drop-in  files  ltdis.sh  static  static.ltdis.strings.txt  static.ltdis.x86_64.txt
Luiscat02-picoctf@webshell:~$ gedit static.ltdis.x86_64.txt 


Luiscat02-picoctf@webshell:~$ chmod +x static
Luiscat02-picoctf@webshell:~$ ./static 
Oh hai! Wait what? A flag? Yes, it's around here somewhere!
Luiscat02-picoctf@webshell:~$ 

Como nos dice que por ahi esta la bandera, lo que vamos a hacer es filtrar la bandera con un grep
Luiscat02-picoctf@webshell:~$  strings static |grep picoCTF
picoCTF{d15a5m_t34s3r_6f8c8200}
Luiscat02-picoctf@webshell:~$ 

y ahi tenemos la bandera
BANDERA
==picoCTF{d15a5m_t34s3r_6f8c8200}==


Referencias
https://www.youtube.com/watch?v=cVpei_-wGMQ&pp=ygUiU3RhdGljIGFpbid0IGFsd2F5cyBub2lzZSAgcGljb2N0Zg%3D%3D