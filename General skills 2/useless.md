#### Description

There's an interesting script in the user's home directory

Additional details will be available after launching your challenge instance.


The work computer is running SSH. We've been given a script which performs some basic calculations, explore the script and find a flag.

```
Hostname: saturn.picoctf.net
Port:     57493
Username: picoplayer
Password: password
```
estas son las credenciales con las que vamos a iniciar
**Solucion**


luego al hacer ls vemos un programa asi que lo ejecutamos
luego entramos a ver como es el programa y como esta escrito y ahi en ese programa esta nuestra bandera

picoplayer@challenge:~$ ls
useless
picoplayer@challenge:~$ ./useless -h
Read the code first
picoplayer@challenge:~$ ./useless add 2 5
The Sum is: 7
picoplayer@challenge:~$ ./uselessmul 5 6     
-bash: ./uselessmul: No such file or directory
picoplayer@challenge:~$ ./useless mul 5 6
The product is: 30
picoplayer@challenge:~$ man useless 

useless
     useless, -- This is a simple calculator script

SYNOPSIS
     useless, [add sub mul div] number1 number2

DESCRIPTION
     Use the useless, macro to make simple calulations like addition,subtraction, multiplication and division.

Examples
     ./useless add 1 2
       This will add 1 and 2 and return 3

     ./useless mul 2 3
       This will return 6 as a product of 2 and 3

     ./useless div 6 3
       This will return 2 as a quotient of 6 and 3

     ./useless sub 6 5
       This will return 1 as a remainder of substraction of 5 from 6

Authors
     This script was designed and developed by Cylab Africa

     picoCTF{us3l3ss_ch4ll3ng3_3xpl0it3d_6194}

picoplayer@challenge:~$ 


**NOTAS ADICIONALES:**

- El script `useless` permite realizar operaciones matemáticas como suma, resta, multiplicación y división.
- El comando `man` muestra el manual de cualquier comando en el sistema, y en este caso, fue útil para encontrar la bandera.

**BANDERA:**  
==picoCTF{us3l3ss_ch4ll3ng3_3xpl0it3d_6194}==

Referencias
https://www.youtube.com/watch?v=Pb-wTPsqr4M&pp=ygUQdXNlbGVzcyAgcGljb2N0Zg%3D%3D