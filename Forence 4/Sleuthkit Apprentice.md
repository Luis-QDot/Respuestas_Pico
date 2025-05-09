#### Descripción

Descargue esta imagen de disco y busque la bandera.Nota: si está usando el shell web, descargue y extraiga la imagen del disco en un `/tmp`directorio que no sea su directorio de inicio.

- [Descargar imagen de disco comprimida](https://artifacts.picoctf.net/c/136/disk.flag.img.gz)
luisquintero@DESKTOP-P53ABHB:~/forence4/ulti$ fls disk.flag.img -o 0000360448 -r | grep flag
++ r/r * 2082(realloc): flag.txt
++ r/r 2371:    flag.uni.txt
luisquintero@DESKTOP-P53ABHB:~/forence4/ulti$ icat disk.flag.img -0 0000360448 2082
icat: invalid option -- '0'
Invalid argument: 0000360448
usage: icat [-hrRsvV] [-f fstype] [-i imgtype] [-b dev_sector_size] [-o imgoffset] image [images] inum[-typ[-id]]
        -h: Do not display holes in sparse files
        -r: Recover deleted file
        -R: Recover deleted file and suppress recovery errors
        -s: Display slack space at end of file
        -i imgtype: The format of the image file (use '-i list' for supported types)
        -b dev_sector_size: The size (in bytes) of the device sectors
        -f fstype: File system type (use '-f list' for supported types)
        -o imgoffset: The offset of the file system in the image (in sectors)
        -P pooltype: Pool container type (use '-P list' for supported types)
        -B pool_volume_block: Starting block (for pool volumes only)
        -S snap_id: Snapshot ID (for APFS only)
        -v: verbose to stderr
        -V: Print version
        -k password: Decryption password for encrypted volumes
luisquintero@DESKTOP-P53ABHB:~/forence4/ulti$ icat disk.flag.img -o 0000360448 2082
            3.449677            13.056403
luisquintero@DESKTOP-P53ABHB:~/forence4/ulti$ icat disk.flag.img -o 0000360448 2371
 p i c o C T F { b y 7 3 _ 5 u r f 3 r _ 3 4 9 7 a e 6 b }
luisquintero@DESKTOP-P53ABHB:~/forence4/ulti$                                                                                                                                                                                                                                                                                                                                                                                  

BANDERA
==picoCTF{by73_5urf3r_3497ae6b}==