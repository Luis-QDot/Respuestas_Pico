Description
This garden contains more than it seems.

vamos a crear una carpeta en ubuntu para guardar nuestros retos, empezamos abriendo una carpeta y descargando el archivo con wget
una ves descargado vamos a hacerle strings a la imagen y vemos que nos da muchisima informacion a lo cual vamos a filtar con grep para encontrar la bandera
luisquintero@DESKTOP-P53ABHB:~/Forence/Gloryofthegarden$ strings garden.jpg | grep picoCTF
Here is a flag "picoCTF{more_than_m33ts_the_3y33dd2eEF5}"
le damos y nos da nuestra bandera

Bandera
==picoCTF{more_than_m33ts_the_3y33dd2eEF5}==


Notas adicionales
Usamos Strings para ver la informacion de una imagen