Descripción
Bueno, ya basta de usar mi propio cifrado. ¡Las cookies de sesión de Flask deberían ser muy seguras! server.py http://mercury.picoctf.net:53700/


Vamos a descargar nuestro archivo con wget 
vamos a usar una herramienta llamada flask unsign

abrimos la pagina con snickerdoodles para que nos de las cookies

usamos este codigo 
eyJ2ZXJ5X2F1dGgiOiJzbmlja2VyZG9vZGxlIn0.Z-3Esw.1e0Wt1iMQu1czb3_RVM33mvZs2Y

luego lo atacamos silenciosamente con un -s y agregamos un grep para filtar la bandera

BANDERA
==picoCTF{pwn_4ll_th3_cook1E5_3646b931}==

Referencias

https://www.youtube.com/watch?v=ufs1xqSQCUM&pp=ygUeTW9zdCBjb29raWVzIHBpY28gY3RmIGVzcGHDsW9s