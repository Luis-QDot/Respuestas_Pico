

Solucion



Primero obtenemos nuestro challenge con wget y la direccion del zip https://artifacts.picoctf.net/c_titan/75/challenge.zip


luego hacemos unzip para descmprimir 
entramos a drop-in con cd y buscamos con ls
vemos que hay un txt con mensaje, 

luego al intentar hacer un cat al mensaje nos aparecera como TOP SECRET  asi que lo que vamos a hacer es un git show y nos aparece 


commit 3899edb7f3110d613c72ad40083fd8feeef703d0 (HEAD, master)
Author: picoCTF <ops@picoctf.com>
Date:   Sat Mar 9 21:09:58 2024 +0000

    remove sensitive info

diff --git a/message.txt b/message.txt
index ed59373..d552d1e 100644
--- a/message.txt
+++ b/message.txt
@@ -1 +1 @@
-picoCTF{s@n1t1z3_9539be6b}
+TOP SECRET
(END)


Teniendo ahi la bandera 

Referencias
https://www.youtube.com/watch?v=_CH5IQewkzw&pp=ygUhQ29sbGFib3JhdGl2ZSBEZXZlbG9wbWVudCBwaWNvY3Rm
