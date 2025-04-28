amos a acomodar una imagen corrupta
intentamos usar xxd 
xxd -l 100 mystery 

pero nos da datos que aun no nos sirve

asi que preguntandole a chatgpt nos da unos bytes con los que siempre empieza una imagen para poder recuperarla

vamos a intentar repararla
hacemos una copia
cp mystery flag.png
luisquinte

vamos a usar el hexeditor para poder agregar lo que nos dio chatgpt

89 50 4E 47 0D 0A 1A 0A

pero aun no lo podemos abrir, asiq ue instalamos un programa 

sudo apt install pngchceck

despues la vamos a modificar aun más, vamos a ir arreglando la imagen por chunks 
, vamos a reparar esa parte
+


BANDERA
==picoCTF{c0rrupt10n_1847995}==


notas adicionales

que son los magic byte, con los chunks 

despues vamos a seguir reparando la imagen paso a paso

