information
Brandon Omar Cardenas Gonzales
Luis Jesus Quintero Bañuelos
Description
Files can always be changed in a secret way. Can you find the flag? cat.jpg


descargamos el archivo con wget https://mercury.picoctf.net/static/e5825f58ef798fdd1af3f6013592a971/cat.jpg
y nos da una imagen 
vamos a darle un exiftool a la imagen a ver que nos aparece 
y con la informacion, vemos que en la parte de la license hay un codigo que nos interesa
License                         : cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9
vamos a cyberchef a ver que nos dice 
que es nuestra bandera

picoCTF{the_m3tadata_1s_modified}

BANDERA
==picoCTF{the_m3tadata_1s_modified}==

notas adicionales
usamos elexiftool para ver la informacion de la imagen

Referencias
https://www.youtube.com/watch?v=uG42AMp0XHU