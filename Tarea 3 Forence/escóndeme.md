escóndeme
Brandon Omar Cardenas Gonzales
Luis Jesus Quintero Bañuelos
Descripción
Cada archivo recibe una bandera.
El analista del SOC vio que dos personas intercambiaban una misma imagen. Decidieron investigar y descubrieron que había algo más de lo que se ve a simple vista .
primero descargamos el archivo con wget https://artifacts.picoctf.net/c/259/flag.png
 y le hacemos un string y vemos una palabra clave que es 
secret/flag.png
le hacemos un binwalk para ver que tiene
luego le damos un binwalk -e flag.png
 binwalk -e flag.png

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 512 x 504, 8-bit/color RGBA, non-interlaced
41            0x29            Zlib compressed data, compressed
39739         0x9B3B          Zip archive data, at least v1.0 to extract, name: secret/
39804         0x9B7C          Zip archive data, at least v2.0 to extract, compressed size: 2869, uncompressed size: 3024, name: secret/flag.png
42908         0xA79C          End of Zip archive, footer length: 22

Luiscat02-picoctf@webshell:~$ ls
y nos da unos archivos de flag asi que entramos con cd 
luego le damos un sz a flag.png y nos da una imagen, donde se encuentra la bandera

Luiscat02-picoctf@webshell:~/enc$ binwalk -e flag.png 

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 512 x 504, 8-bit/color RGBA, non-interlaced
41            0x29            Zlib compressed data, compressed
39739         0x9B3B          Zip archive data, at least v1.0 to extract, name: secret/
39804         0x9B7C          Zip archive data, at least v2.0 to extract, compressed size: 2869, uncompressed size: 3024, name: secret/flag.png
42908         0xA79C          End of Zip archive, footer length: 22

Luiscat02-picoctf@webshell:~/enc$ ls
_flag.png.extracted  flag.png
Luiscat02-picoctf@webshell:~/enc$ 

 ls
_flag.png.extracted  flag.png
Luiscat02-picoctf@webshell:~/enc$ ^C
Luiscat02-picoctf@webshell:~/enc$ cd _flag.png.extracted/
Luiscat02-picoctf@webshell:~/enc/_flag.png.extracted$ ls
29  29.zlib  9B3B.zip  secret
Luiscat02-picoctf@webshell:~/enc/_flag.png.extracted$ cd secret/
Luiscat02-picoctf@webshell:~/enc/_flag.png.extracted/secret$ ls
flag.png
Luiscat02-picoctf@webshell:~/enc/_flag.png.extracted/secret$ sz flag.png 
PNGg.png 100.00% 2.95 KB/2.95 KB


BANDERA
==picoCTF{Hiddinng_An_imag3_within_@n_ima9e_cda72af0}==