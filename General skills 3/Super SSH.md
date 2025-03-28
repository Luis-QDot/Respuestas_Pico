#### Descripción

El uso de un Secure Shell (SSH) será bastante importante.¿ Puedes `ssh`ir al puerto para conseguir la bandera?`ctf-player``titan.picoctf.net``49221`También necesitarás la contraseña `83dcefb7`. Si se te solicita, acepta la huella digital con `yes`.Si su dispositivo no tiene un shell, puede usar: [https://webshell.picoctf.org](https://webshell.picoctf.org/)Si no está seguro de qué es un shell, consulte nuestro manual: [https://primer.picoctf.com/#_the_shell](https://primer.picoctf.com/#_the_shell)

Solucion


asi que como la descripcion nos dice, vamos a usar ssh para loguearnos 
Luiscat02-picoctf@webshell:~$ ssh ctf-player@titan.picoctf.net -p 49221    
The authenticity of host '[titan.picoctf.net]:49221 ([3.139.174.234]:49221)' can't be established.
ED25519 key fingerprint is SHA256:4S9EbTSSRZm32I+cdM5TyzthpQryv5kudRP9PIKT7XQ.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[titan.picoctf.net]:49221' (ED25519) to the list of known hosts.
ctf-player@titan.picoctf.net's password: 
Welcome ctf-player, here's your flag: picoCTF{s3cur3_c0nn3ct10n_8969f7d3}
Connection to titan.picoctf.net closed.
Luiscat02-picoctf@webshell:~$ 
despues de hacer loggin pues nos pide la contraseña que nos dice y nos da la bandera


**BANDERA:**  
==**picoCTF{s3cur3_c0nn3ct10n_8969f7d3}**==


Referencias
https://www.youtube.com/watch?v=9vO0tDaCySA&pp=ygURU3VwZXIgU1NIIHBpY29jdGY%3D