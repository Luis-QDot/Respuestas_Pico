Description
Use `srch_strings` from the sleuthkit and some terminal-fu to find a flag in this disk image: dds1-alpine.flag.img.gz


Vamos a descargar el archivo con wget 

una ves descargada la vamos a descompimir
luisquintero@DESKTOP-P53ABHB:~/forence4/Disk$ gunzip dds1-alpine.flag.img.gz

le damos un srch como nos da idea las pistas

luisquintero@DESKTOP-P53ABHB:~/forence4/Disk$ srch_strings dds1-alpine.flag.img

y nos da muchisimo texto, para lo cual vamos a filtar con un gep para ver si aparece

luisquintero@DESKTOP-P53ABHB:~/forence4/Disk$ srch_strings dds1-alpine.flag.img | grep pico
ffffffff81399ccf t pirq_pico_get
ffffffff81399cee t pirq_pico_set
ffffffff820adb46 t pico_router_probe
  SAY picoCTF{f0r3ns1c4t0r_n30phyt3_267e38f6}
luisquintero@DESKTOP-P53ABHB:~/forence4/Disk$


Y ahi nos da la bandera

BANderA

==picoCTF{f0r3ns1c4t0r_n30phyt3_267e38f6}==



Notas adicionales