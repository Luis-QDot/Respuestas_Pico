Primero vamos a obtener nuestro reto con wget y el link 

vamos a entrar al drop-in 
y al hacer ls vemos un mensaje 
le intentamos hacer un cat y nos sale 
uiscat02-picoctf@webshell:~/drop-in$ cat message.txt 
This is what I was working on, but I'd need to look at my commit history to know why...Luiscat02-picoctf@webshell:~/drop-in$ 
Luiscat02-picoctf@webshell:~/drop-in$ 

Por lo que usaremos el comando git log y nos mostrara 

commit 712314f105348e295f8cadd7d7dc4e9fa871e9a2 (HEAD -> master)
Author: picoCTF <ops@picoctf.com>
Date:   Tue Mar 12 00:07:26 2024 +0000

    picoCTF{t1m3m@ch1n3_e8c98b3a}
(END)
Y asi nos dara nuestra bandera 

Referencias
https://www.youtube.com/watch?v=ijt0mQzFT0o&t=70s&pp=ygUUVGltZSBNYWNoaW5lIHBpY29jdGY%3D

