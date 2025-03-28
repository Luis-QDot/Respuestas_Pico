#### Descripción

¿Puedes descifrar la contraseña para obtener la bandera?Descargue el verificador de contraseñas [aquí](https://artifacts.picoctf.net/c/12/level1.py) y también necesitará la [bandera](https://artifacts.picoctf.net/c/12/level1.flag.txt.enc) cifrada en el mismo directorio.

Primero vamos a descargar los links que vienen ahi con wget

Solucion


Primero vamos a inspeccionar el codigo con el comando nano 
 y justo aqui viene la contraseña para la bandera
 def level_1_pw_check():
    user_pw = input("Please enter correct password for flag: ")
    if( user_pw == "8713"):
        print("Welcome back... your flag, user:")
        decryption = str_xor(flag_enc.decode(), user_pw)
        print(decryption)
        return
    print("That password is incorrect")
    y al correr nuestro archivo ponemos la contraseña y nos da la bandera
    Luiscat02-picoctf@webshell:~$ python level1.py 
Please enter correct password for flag: 8713
Welcome back... your flag, user:
picoCTF{545h_r1ng1ng_1b2fd683}


**NOTAS ADICIONALES:**

- El código compara la contraseña proporcionada por el usuario con la correcta (`8713`).
- La función `str_xor` se usa para descifrar la bandera utilizando la contraseña.
**BANDERA:**  
==picoCTF{545h_r1ng1ng_1b2fd683}==


Referencias
https://www.youtube.com/watch?v=9vm_Uj60a7o&pp=ygUSUFcgQ3JhY2sgMSBwaWNvY3Rm