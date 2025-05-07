Descripción
He escondido una bandera en este archivo. ¿Puedes encontrarla? La ciencia forense es divertida.pptm

vamos a descargar el archivo con wget de la pagina 
vamos a hacerle unzip al archivo 

vamos a acceder a macro luego al ppt, despues a slide masters 
debemos estar aqui 
~/Forence3/Macro/macro/ppt/slideMasters$ l
vamos a usar cat para entrar al hide y nos aparece esto
luisquintero@DESKTOP-P53ABHB:~/Forence3/Macro/macro/ppt/slideMasters$ cat hidden
Z m x h Z z o g c G l j b 0 N U R n t E M W R f d V 9 r b j B 3 X 3 B w d H N f c l 9 6 M X A 1 f Qluisquintero@DESKTOP-P53ABHB:~/Forence3/Macro/macro/ppt/slideMasters$

luego hacemos esto y nos da la bandera

luisquintero@DESKTOP-P53ABHB:~/Forence3/Macro/macro/ppt/slideMasters$ cat hidden
Z m x h Z z o g c G l j b 0 N U R n t E M W R f d V 9 r b j B 3 X 3 B w d H N f c l 9 6 M X A 1 f Qluisquintero@DESKTOP-P53ABHB:~/Forence3/Macro/macro/ppt/slideMasters$ cat hidden | sed's/ //'
-bash: seds/ //: No such file or directory
luisquintero@DESKTOP-P53ABHB:~/Forence3/Macro/macro/ppt/slideMasters$ cat hidden | sed 's/ //'
Zm x h Z z o g c G l j b 0 N U R n t E M W R f d V 9 r b j B 3 X 3 B w d H N f c l 9 6 M X A 1 f Qluisquintero@DESKTOP-P53ABHB:~/Forence3/Macro/macro/ppt/slideMasters$ cat hidden | sed 's/ //g' | base64 -d
flag: picoCTF{D1d_u_kn0w_ppts_r_z1p5}base64: invalid input
luisquintero@DESKTOP-P53ABHB:~/Forence3/Macro/macro/ppt/slideMasters$

BANDErA
==flag: picoCTF{D1d_u_kn0w_ppts_r_z1p5}==


Notas adicionales:


entramos usando cat y usamos la consola para traducir un texto de base 64

