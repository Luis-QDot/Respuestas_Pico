Description
I found a web app that can help process images: PNG images only!
Try it here!

vamos a ir al link y darnos cuenta que solo nos edja sunir imagenes png
agregamos robots.txt y nos da un sitio donde sabemos que se suben nuestras imagenes
luego hay un apartado de instrucciones 
Agente de usuario: *
No permitir: /instructions.txt
No permitir: /subidas/


y aqui esta como podemos solucionar
Creemos una aplicación web para el procesamiento de imágenes PNG.
Es necesario:
Permitir a los usuarios cargar imágenes PNG
	Busque la extensión ".png" en los archivos enviados
	Asegúrese de que los bytes mágicos coincidan (no estoy seguro de qué es esto exactamente, pero Wikipedia dice que los primeros bytes contienen "PNG" en hexadecimal: "50 4E 47")
Después de la validación, almacene los archivos cargados para que el administrador pueda recuperarlos más tarde y realizar el procesamiento necesario.




Bandera
==picoCTF{c3rt!fi3d_Xp3rt_tr1ckst3r_48785c0e}==

Referencias 
https://www.youtube.com/watch?v=co8MZmviC1U&pp=ygUbVHJpY2tzdGVyIHBpY28gY3RmIGVzcGHDsW9s