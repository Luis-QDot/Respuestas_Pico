#### Descripción

Corrija el error de sintaxis en este script de Python para imprimir la bandera.[Descargar script de Python](https://artifacts.picoctf.net/c/27/fixme1.py)

-Pistas La sangría es muy significativa en Python
-Para ver el archivo en el webshell, haga lo siguiente:`$ nano fixme1.py`

Soluciones



vamos a decargar nuestro archivo con wget
luego le hacemos nano a nuestro documento para inspreccionar y nos sale la frase
return "".join([chr(ord(secret_c) ^ ord(new_key_c)) for (secret_c,new_key_c) in zip(secret,new_key)])


flag_enc = chr(0x15) + chr(0x07) + chr(0x08) + chr(0x06) + chr(0x27) + chr(0x21) + chr(0x23) + chr(0x15) + chr(0x5a) + chr(0x07) + chr(0x00) + chr(0x46) + chr(0x0b) + chr(0x1a) + chr(0x5a) +>

  
flag = str_xor(flag_enc, 'enkidu')
  print('That is correct! Here\'s your flag: ' + flag)
asi que corremos nuestro archivo y nos da la bandera
Luiscat02-picoctf@webshell:~$ python3 fixme1.py 
That is correct! Here's your flag: picoCTF{1nd3nt1ty_cr1515_182342f7}
Luiscat02-picoctf@webshell:~$ 

==Bandera==
==picoCTF{1nd3nt1ty_cr1515_182342f7}==


Referencias
https://www.youtube.com/watch?v=yLS55NGo81k&pp=ygUSZml4bWUxLnB5ICBwaWNvY3Rm
