#### Descripción

En RSA, un `e`valor pequeño puede ser problemático, pero ¿qué ocurre con [los valores](https://mercury.picoctf.net/static/b9ddda080c56fb421bf30409bec3460d/values)`N` ? ¿Se puede descifrar?

Vamos a descargar el arhivo

Le damos cat para ver que contiene el archivo
luisquintero@DESKTOP-P53ABHB:~/crippto3/pq$ cat values
Decrypt my super sick RSA:
c: 964354128913912393938480857590969826308054462950561875638492039363373779803642185
n: 1584586296183412107468474423529992275940096154074798537916936609523894209759157543
e: 65537luisquintero@DESKTOP-P53ABHB:~/crippto3/pq$

luego vamos a esta pagina para cambiar los valores
https://www.dcode.fr/rsa-cipher


ponemos los valores de C y N y nos da la bandera

BANDERA
picoCTF{sma11_N_n0_g0od_73918962}


Referencias


https://www.youtube.com/watch?v=pdAHWr5cxRc&ab_channel=COZT 
