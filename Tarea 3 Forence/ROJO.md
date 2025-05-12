ROJO
Brandon Omar Cardenas Gonzales
Luis Jesus Quintero Bañuelos
Descripción
ROJO, ROJO, ROJO, ROJO
Descargar la imagen: red.png

vamos a descargar la imagen con wget https://challenge-files.picoctf.net/c_verbal_sleep/831307718b34193b288dde31e557484876fb84978b5818e2627e453a54aa9ba6/red.png
le damos un exftool
y nos da este texto
Poem                            : Crimson heart, vibrant and bold,.Hearts flutter at your sight..Evenings glow softly red,.Cherries burst with sweet life..Kisses linger with your warmth..Love deep as merlot..Scarlet leaves falling softly,.Bold in every stroke.
Image Size                      : 128x128
Megapixels                      : 0.016

asi que vamos a usar un comando llamado zsteg
y nos rara un texto el cual cortando palabras sabremos que esta en BASE64 asi que vamos a cyberchef y le decimos que nos convierta el texto
y sino ponemos el comando para que nos lo de ahi mismno
luisquintero@DESKTOP-P53ABHB:~/Forencee/rojo$ zsteg --lsb --channel rgba red.png
b1,rgba,lsb,xy      .. text: "cGljb0NURntyM2RfMXNfdGgzX3VsdDFtNHQzX2N1cjNfZjByXzU0ZG4zNTVffQ==cGljb0NURntyM2RfMXNfdGgzX3VsdDFtNHQzX2N1cjNfZjByXzU0ZG4zNTVffQ==cGljb0NURntyM2RfMXNfdGgzX3VsdDFtNHQzX2N1cjNfZjByXzU0ZG4zNTVffQ==cGljb0NURntyM2RfMXNfdGgzX3VsdDFtNHQzX2N1cjNfZjByXzU0ZG4zNTVffQ=="
b2,rgba,lsb,xy      .. file: OpenPGP Secret Key
luisquintero@DESKTOP-P53ABHB:~/Forencee/rojo$ echo cGljb0NURntyM2RfMXNfdGgzX3VsdDFtNHQzX2N1cjNfZjByXzU0ZG4zNTVffQ== | base64 -d
picoCTF{r3d_1s_th3_ult1m4t3_cur3_f0r_54dn355_}luisquintero@DESKTOP-P53ABHB:~/Forencee/rojo$

Y nos da la bandera

BANDERA
==picoCTF{r3d_1s_th3_ult1m4t3_cur3_f0r_54dn355_}==


Notas adicionales

Usampos el zsteg para ver el texto oculto en la imagen 

Referencias

https://www.youtube.com/watch?v=tbJwWVW6wk8 

