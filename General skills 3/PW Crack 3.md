
#### Descripción

¿Puedes descifrar la contraseña para obtener la bandera?Descargue el verificador de contraseñas [aquí](https://artifacts.picoctf.net/c/17/level3.py) y también necesitará la [bandera](https://artifacts.picoctf.net/c/17/level3.flag.txt.enc) cifrada y el [hash](https://artifacts.picoctf.net/c/17/level3.hash.bin) en el mismo directorio.Hay 7 contraseñas posibles, de las cuales una es correcta. Puedes encontrarlas examinando el script del verificador de contraseñas.

primero vamos a descargar los 3 enlaces con wget
primero vamos a hacer un cat para  ver que nos sale y nos arroja esto 
level_3_pw_check()


# The strings below are 7 possibilities for the correct password. 
#   (Only 1 is correct)
pos_pw_list = ["f09e", "4dcf", "87ab", "dba8", "752e", "3961", "f159"]
asi que ejecutemos nuestro progrma e intentemos adivinar la contraseña

y no puede ser le atine a la primera 
Luiscat02-picoctf@webshell:~$ python level3.py 
Please enter correct password for flag: 87ab
Welcome back... your flag, user:
picoCTF{m45h_fl1ng1ng_cd6ed2eb}
Luiscat02-picoctf@webshell:~$ 
jajaja y asi nos da nuestra bandera

picoCTF{m45h_fl1ng1ng_cd6ed2eb}