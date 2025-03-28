#### Descripción

Encuentra la bandera que se encuentra en este servidor para adelantarte a la competencia [http://mercury.picoctf.net:28916/](http://mercury.picoctf.net:28916/)


vamos a usar un comando en la linea de consola con el link de la pagina
http://mercury.picoctf.net:28916/

$ curl -I http://mercury.picoctf.net:28916/index.php
HTTP/1.1 200 OK
flag: picoCTF{r3j3ct_th3_du4l1ty_70bc61c4}
Content-type: text/html; charset=UTF-8


Y ahi nos sale la bandera
