#### Description

There is some interesting information hidden around this site [http://mercury.picoctf.net:5080/](http://mercury.picoctf.net:5080/). Can you find it?


Una pista que nos dan es
You should have enough hints to find the files, don't run a brute forcer.


abrimos la pagina y nos dice que tiene html css

inspeccionamos nuestro codigo fuente
Vemos que aparece la primera parte de la bandera
<!-- Here's the first part of the flag: picoCTF{t -->

luego vamos a la hoja de estilos y hasta abajo viene la segunda parte de la bandera
  
/* CSS makes the page look nice, and yes, it also has part of the flag. Here's part 2: h4ts_4_l0 */

Vamos al java y nos da esta pista 
/* How can I keep Google from indexing my website? */
 dicho esto usamos robots en e link que nos da
 http://mercury.picoctf.net:5080/robots.txt
 y nos da la otra bandera
 Agente de usuario: *
No permitir: /index.html
# Parte 3: t_0f_pl4c
# Creo que este es un servidor Apache... ¿puedes acceder a la siguiente bandera?
y con la misma pista que nos da buscamos usando apache agregando .htaccess
http://mercury.picoctf.net:5080/.htaccess
 y nos da la siguiente bandera
 # Parte 4: 3s_2_lO0k
# Me encanta crear sitios web en mi Mac, puedo almacenar mucha información allí.


y nos da la siguiente pista
y en el cotexto de las mac hay un archivo .ds_store por lo cual hayinformacion en esa carpeta, por l cual cambiamosn el link
http://mercury.picoctf.net:5080/.DS_Store
y nos da toda la bandera
¡Felicidades! Completaste la búsqueda del tesoro. Parte 5: _35844447}

BANDERA
picoCTF{th4ts_4_l0t_0f_pl4c3s_2_lO0k_35844447}
