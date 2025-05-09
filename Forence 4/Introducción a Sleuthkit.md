#### Descripción

Descargue la imagen de disco y úsela `mmls`para determinar el tamaño de la partición de Linux. Conéctese al servicio de verificación remota para comprobar su respuesta y obtener la bandera.Nota: si está usando el shell web, descargue y extraiga la imagen del disco en un `/tmp`directorio que no sea su directorio de inicio.[Descargar imagen de disco](https://artifacts.picoctf.net/c/164/disk.img.gz)Programa de verificación de acceso:`nc saturn.picoctf.net 53773`


vamos a hacerle una carpeta y luego descargamos con  wget
vamos a revisr el disco
luisquintero@DESKTOP-P53ABHB:~/forence4/sleut$ mv disk.flag.img disk.img
luisquintero@DESKTOP-P53ABHB:~/forence4/sleut$ mmls disk.img
DOS Partition Table
Offset Sector: 0
Units are in 512-byte sectors

      Slot      Start        End          Length       Description
000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
001:  -------   0000000000   0000002047   0000002048   Unallocated
002:  000:000   0000002048   0000204799   0000202752   Linux (0x83)
luisquintero@DESKTOP-P53ABHB:~/forence4/sleut$ nc saturn.picoctf.net 53773
What is the size of the Linux partition in the given disk image?
Length in sectors: 202752
202752
Great work!
picoCTF{mm15_f7w!}


BANDERA

==picoCTF{mm15_f7w!}==

