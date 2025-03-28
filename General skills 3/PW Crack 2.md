#### Descripción

¿Puedes descifrar la contraseña para obtener la bandera?Descargue el verificador de contraseñas [aquí](https://artifacts.picoctf.net/c/13/level2.py) y también necesitará la [bandera](https://artifacts.picoctf.net/c/13/level2.flag.txt.enc) cifrada en el mismo directorio.

Nos da algunas pistas
- ¿Te resulta familiar esta codificación?
- `str_xor`No es necesario realizar ingeniería inversa a la función para este desafío.
-

Soluciones


asi que procedemosa  descargar nuestro archivo con wget 

usamos nano para inspeccionar el codigo y nos arroja el siguiente texto 
def level_2_pw_check():
    user_pw = input("Please enter correct password for flag: ")
    if( user_pw == chr(0x64) + chr(0x65) + chr(0x37) + chr(0x36) ):
        print("Welcome back... your flag, user:")
        decryption = str_xor(flag_enc.decode(), user_pw)
        print(decryption)
        return
    print("That password is incorrect")
    por lo cual para decifrar la contraseña hay que encontra las letras de los strings 
siendo esta pagina a la que entraremos 
https://onlinestringtools.com/convert-ascii-to-string

y nuestra contraseña es 
0x64 0x65 0x37 0x36 = de76
asi que ejecutamos nuestro programa
y poniendo la contraseña nos da la bandera 
Luiscat02-picoctf@webshell:~$ nano level2.py
Luiscat02-picoctf@webshell:~$ python level2.py
Please enter correct password for flag: de76
Welcome back... your flag, user:
picoCTF{tr45h_51ng1ng_489dea9a}
Luiscat02-picoctf@webshell:~$ 


**NOTAS ADICIONALES:**
La contraseña está codificada usando valores hexadecimales, que se convierten a caracteres ASCII.
 La función `str_xor` se usa para descifrar la bandera.

**BANDERA:**  
==picoCTF{tr45h_51ng1ng_489dea9a}==


Referencias
https://www.youtube.com/watch?v=ykhTVuWEpIU&pp=ygUSUFcgQ3JhY2sgMiBwaWNvY3Rm
