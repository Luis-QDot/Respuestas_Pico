#### Descripción

Descargue esta imagen de disco y busque la bandera.Nota: si está usando el shell web, descargue y extraiga la imagen del disco en un `/tmp`directorio que no sea su directorio de inicio.

- [Descargar imagen de disco comprimida](https://artifacts.picoctf.net/c/214/disk.flag.img.gz)
vamos a descargar con wget
luisquintero@DESKTOP-P53ABHB:~/forence4/orquidea$ ls
disk.flag.img.gz
luisquintero@DESKTOP-P53ABHB:~/forence4/orquidea$ gzip -d disk.flag.img.gz
luisquintero@DESKTOP-P53ABHB:~/forence4/orquidea$ openssl aes256 -d -salt -in flag.txt.enc -out flag.txt -k unbreakablepassword1234567
Can't open "flag.txt.enc" for reading, No such file or directory
40077496C37F0000:error:80000002:system library:BIO_new_file:No such file or directory:../crypto/bio/bss_file.c:67:calling fopen(flag.txt.enc, rb)
40077496C37F0000:error:10000080:BIO routines:BIO_new_file:no such file:../crypto/bio/bss_file.c:75:
luisquintero@DESKTOP-P53ABHB:~/forence4/orquidea$ ls
disk.flag.img
luisquintero@DESKTOP-P53ABHB:~/forence4/orquidea$ ls
disk.flag.img
luisquintero@DESKTOP-P53ABHB:~/forence4/orquidea$ mmls disk.flag.img
DOS Partition Table
Offset Sector: 0
Units are in 512-byte sectors

      Slot      Start        End          Length       Description
000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
001:  -------   0000000000   0000002047   0000002048   Unallocated
002:  000:000   0000002048   0000206847   0000204800   Linux (0x83)
003:  000:001   0000206848   0000411647   0000204800   Linux Swap / Solaris x86 (0x82)
004:  000:002   0000411648   0000819199   0000407552   Linux (0x83)
luisquintero@DESKTOP-P53ABHB:~/forence4/orquidea$ fls disk.flag.img -o 411648
d/d 460:        home
d/d 11: lost+found
d/d 12: boot
d/d 13: etc
d/d 81: proc
d/d 82: dev
d/d 83: tmp
d/d 84: lib
d/d 87: var
d/d 96: usr
d/d 106:        bin
d/d 120:        sbin
d/d 466:        media
d/d 470:        mnt
d/d 471:        opt
d/d 472:        root
d/d 473:        run
d/d 475:        srv
d/d 476:        sys
d/d 2041:       swap
V/V 51001:      $OrphanFiles
luisquintero@DESKTOP-P53ABHB:~/forence4/orquidea$ openssl aes256 -d -salt -in flag.txt.enc -out flag.txt -k unbreakablepassword1234567
Can't open "flag.txt.enc" for reading, No such file or directory
4007CC8B1F7F0000:error:80000002:system library:BIO_new_file:No such file or directory:../crypto/bio/bss_file.c:67:calling fopen(flag.txt.enc, rb)
4007CC8B1F7F0000:error:10000080:BIO routines:BIO_new_file:no such file:../crypto/bio/bss_file.c:75:
luisquintero@DESKTOP-P53ABHB:~/forence4/orquidea$ fls disk.flag.img -o 411648 472
r/r 1875:       .ash_history
r/r * 1876(realloc):    flag.txt
r/r 1782:       flag.txt.enc
luisquintero@DESKTOP-P53ABHB:~/forence4/orquidea$ icat disk.flag.img -o 411648 472
   .       ..  S  $ .ash_historyT  flag.txt  flag.txt.enc                                               ,洞luisquintero@DESKTOP-P53ABHB:~/forence4/orquidea$ file flag.txt.enc
flag.txt.enc: cannot open `flag.txt.enc' (No such file or directory)
luisquintero@DESKTOP-P53ABHB:~/forence4/orquidea$ file flag.txt.enc
flag.txt.enc: cannot open `flag.txt.enc' (No such file or directory)
luisquintero@DESKTOP-P53ABHB:~/forence4/orquidea$ icat disk.flag.img -o 411648 472 > flag.txt.enc
luisquintero@DESKTOP-P53ABHB:~/forence4/orquidea$ file flag.txt.enc
flag.txt.enc: data
luisquintero@DESKTOP-P53ABHB:~/forence4/orquidea$ icat disk.flag.img -o 411648 1875
touch flag.txt
nano flag.txt
apk get nano
apk --help
apk add nano
nano flag.txt
openssl
openssl aes256 -salt -in flag.txt -out flag.txt.enc -k unbreakablepassword1234567
shred -u flag.txt
ls -al
halt
luisquintero@DESKTOP-P53ABHB:~/forence4/orquidea$ touch flag.txt
luisquintero@DESKTOP-P53ABHB:~/forence4/orquidea$ nano flag.txt
luisquintero@DESKTOP-P53ABHB:~/forence4/orquidea$ apk get nano
Command 'apk' not found, did you mean:
  command 'apg' from deb apg (2.2.3.dfsg.1-5build2)
  command 'apt' from deb apt (2.7.6)
  command 'ack' from deb ack (3.7.0-1)
  command 'ark' from deb ark (4:23.08.4-0ubuntu1)
  command 'awk' from deb gawk (1:5.2.1-2)
  command 'awk' from deb mawk (1.3.4.20231126-1)
  command 'awk' from deb original-awk (2023-11-27-1)
Try: sudo apt install <deb name>
luisquintero@DESKTOP-P53ABHB:~/forence4/orquidea$ apk add nano
Command 'apk' not found, did you mean:
  command 'apg' from deb apg (2.2.3.dfsg.1-5build2)
  command 'ark' from deb ark (4:23.08.4-0ubuntu1)
  command 'ack' from deb ack (3.7.0-1)
  command 'apt' from deb apt (2.7.6)
  command 'awk' from deb gawk (1:5.2.1-2)
  command 'awk' from deb mawk (1.3.4.20231126-1)
  command 'awk' from deb original-awk (2023-11-27-1)
Try: sudo apt install <deb name>
luisquintero@DESKTOP-P53ABHB:~/forence4/orquidea$ nano flag.txt
luisquintero@DESKTOP-P53ABHB:~/forence4/orquidea$ openssl
help:

Standard commands
asn1parse         ca                ciphers           cmp
cms               crl               crl2pkcs7         dgst
dhparam           dsa               dsaparam          ec
ecparam           enc               engine            errstr
fipsinstall       gendsa            genpkey           genrsa
help              info              kdf               list
mac               nseq              ocsp              passwd
pkcs12            pkcs7             pkcs8             pkey
pkeyparam         pkeyutl           prime             rand
rehash            req               rsa               rsautl
s_client          s_server          s_time            sess_id
smime             speed             spkac             srp
storeutl          ts                verify            version
x509

Message Digest commands (see the `dgst' command for more details)
blake2b512        blake2s256        md4               md5
rmd160            sha1              sha224            sha256
sha3-224          sha3-256          sha3-384          sha3-512
sha384            sha512            sha512-224        sha512-256
shake128          shake256          sm3

Cipher commands (see the `enc' command for more details)
aes-128-cbc       aes-128-ecb       aes-192-cbc       aes-192-ecb
aes-256-cbc       aes-256-ecb       aria-128-cbc      aria-128-cfb
aria-128-cfb1     aria-128-cfb8     aria-128-ctr      aria-128-ecb
aria-128-ofb      aria-192-cbc      aria-192-cfb      aria-192-cfb1
aria-192-cfb8     aria-192-ctr      aria-192-ecb      aria-192-ofb
aria-256-cbc      aria-256-cfb      aria-256-cfb1     aria-256-cfb8
aria-256-ctr      aria-256-ecb      aria-256-ofb      base64
bf                bf-cbc            bf-cfb            bf-ecb
bf-ofb            camellia-128-cbc  camellia-128-ecb  camellia-192-cbc
camellia-192-ecb  camellia-256-cbc  camellia-256-ecb  cast
cast-cbc          cast5-cbc         cast5-cfb         cast5-ecb
cast5-ofb         des               des-cbc           des-cfb
des-ecb           des-ede           des-ede-cbc       des-ede-cfb
des-ede-ofb       des-ede3          des-ede3-cbc      des-ede3-cfb
des-ede3-ofb      des-ofb           des3              desx
rc2               rc2-40-cbc        rc2-64-cbc        rc2-cbc
rc2-cfb           rc2-ecb           rc2-ofb           rc4
rc4-40            seed              seed-cbc          seed-cfb
seed-ecb          seed-ofb          sm4-cbc           sm4-cfb
sm4-ctr           sm4-ecb           sm4-ofb

luisquintero@DESKTOP-P53ABHB:~/forence4/orquidea$ openssl aes256 -salt -in flag.txt -out flag.txt.enc -k unbreakablepassword1234567
*** WARNING : deprecated key derivation used.
Using -iter or -pbkdf2 would be better.
luisquintero@DESKTOP-P53ABHB:~/forence4/orquidea$ shred -u flag.txt
luisquintero@DESKTOP-P53ABHB:~/forence4/orquidea$ halt
System has not been booted with systemd as init system (PID 1). Can't operate.
Failed to connect to bus: Host is down
luisquintero@DESKTOP-P53ABHB:~/forence4/orquidea$ openssl aes256 -salt -d -in flag.txt.enc -out flag.txt -k unbreakablepassword1234567
*** WARNING : deprecated key derivation used.
Using -iter or -pbkdf2 would be better.
luisquintero@DESKTOP-P53ABHB:~/forence4/orquidea$ cat flag.txt.enc
Salted__        :`:ӀHQO{3luisquintero@DESKTOP-P53ABHB:~/forence4/orquidea$ enssl aes256 -salt -d -in flag.txt.enc -out flag.txt -k unbreakablepassword123456
enssl: command not found
luisquintero@DESKTOP-P53ABHB:~/forence4/orquidea$ openssl aes256 -salt -d -in
aes256: Option -in needs a value
aes256: Use -help for summary.
luisquintero@DESKTOP-P53ABHB:~/forence4/orquidea$ flag.txt.enc -out flag.txt -k unbreakablepassword123456
flag.txt.enc: command not found
luisquintero@DESKTOP-P53ABHB:~/forence4/orquidea$ icat disk.flag.img -o 411648 1875
touch flag.txt
nano flag.txt
apk get nano
apk --help
apk add nano
nano flag.txt
openssl
openssl aes256 -salt -in flag.txt -out flag.txt.enc -k unbreakablepassword1234567
shred -u flag.txt
ls -al
halt
luisquintero@DESKTOP-P53ABHB:~/forence4/orquidea$ touch flag.txt
luisquintero@DESKTOP-P53ABHB:~/forence4/orquidea$ nano flag.txt
luisquintero@DESKTOP-P53ABHB:~/forence4/orquidea$ openssl aes256 -salt -in flag.txt -out flag.txt.enc -k unbreakablepassword1234567
*** WARNING : deprecated key derivation used.
Using -iter or -pbkdf2 would be better.
luisquintero@DESKTOP-P53ABHB:~/forence4/orquidea$ shred -u flag.txt
luisquintero@DESKTOP-P53ABHB:~/forence4/orquidea$ icat disk.flag.img -o 411648 1782
Salted__S+%+Okђ(Ac@]ԣ
ޢȤ7 ؎$'%luisquintero@DESKTOP-P53ABHB:~/forence4/orquidea$ openssl aes256 -salt -d -in flag.txt.enc -out flag.txt -k unbreakablepassword1234567
*** WARNING : deprecated key derivation used.
Using -iter or -pbkdf2 would be better.
luisquintero@DESKTOP-P53ABHB:~/forence4/orquidea$ cat flag.txt
apk get nano

luisquintero@DESKTOP-P53ABHB:~/forence4/orquidea$ icat disk.flag.img -o 411648
Missing image name and/or address
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
luisquintero@DESKTOP-P53ABHB:~/forence4/orquidea$ 1782
1782: command not found
luisquintero@DESKTOP-P53ABHB:~/forence4/orquidea$ icat disk.flag.img -o 411648 1782  > flag2.txt.enc
luisquintero@DESKTOP-P53ABHB:~/forence4/orquidea$ openssl aes256 -salt -d -in flag2.txt.enc -out flag.txt -k unbreakablepassword1234567
*** WARNING : deprecated key derivation used.
Using -iter or -pbkdf2 would be better.
bad decrypt
4007C43E497F0000:error:1C800064:Provider routines:ossl_cipher_unpadblock:bad decrypt:../providers/implementations/ciphers/ciphercommon_block.c:124:
luisquintero@DESKTOP-P53ABHB:~/forence4/orquidea$ cat flag.txt
picoCTF{h4un71ng_p457_1d02081e}luisquintero@DESKTOP-P53ABHB:~/forence4/orquidea$



BANDERa
==picoCTF{h4un71ng_p457_1d02081e}==

