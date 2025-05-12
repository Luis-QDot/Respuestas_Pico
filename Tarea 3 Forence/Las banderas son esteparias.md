Las banderas son esteparias
Brandon Omar Cardenas Gonzales
Luis Jesus Quintero Bañuelos
Un grupo de hackers clandestinos podría estar usando este sitio legítimo para comunicarse. Usa tus técnicas forenses para descubrir su mensaje.
Pruébalo aquí !
asi que vamos a entrar al sitio
http://standard-pizzas.picoctf.net:52747/

leyendo la pista nos dice que busquemos en el pais que no existe
y pues la bandera que no encaja es la que tiene escrito texto en lugar de bandera
asi que copiamos la imagen y la guardamos en la carpeta del reto

si intentamos abrir la imagen, vemos que es muy grande y con un editor de igamenes tampoco nos ayuda
y con el titulo de la imagen nos damos cuenta que stepic es una herramienta que nos va a ayudar 
porque es una herramienta para decodificar
asi que usamos el comando stepic -i archivo -d para que nos de el archivo y nos da la bandera

luisquintero@DESKTOP-P53ABHB:~/Forencee/banderas$ stepic -i upz.png -d
/usr/lib/python3/dist-packages/PIL/Image.py:3186: DecompressionBombWarning: Image size (150658990 pixels) exceeds limit of 89478485 pixels, could be decompression bomb DOS attack.
  warnings.warn(
picoCTF{fl4g_h45_fl4g51d83cb1}luisquintero@DESKTOP-P53ABHB:~/Forencee/banderas$


BANDERA
==picoCTF{fl4g_h45_fl4g51d83cb1}==


Notas adicionales

descubrimos como funciona e instalamos el stepic

Referencias
https://www.youtube.com/watch?v=EXuKrStFsQo
