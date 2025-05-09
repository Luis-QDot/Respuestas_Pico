#### Descripción

Descargue esta imagen de disco, busque la clave e inicie sesión en la máquina remota.Nota: si está usando el shell web, descargue y extraiga la imagen del disco en un `/tmp`directorio que no sea su directorio de inicio.

- [Descargar imagen de disco](https://artifacts.picoctf.net/c/69/disk.img.gz)
- Máquina remota:`ssh -i key_file -p 53941 ctf-player@saturn.picoctf.net`

Vamos a descargar el archivo con wget 


luisquintero@DESKTOP-P53ABHB:~/forence4/oni$ gzip -d disk.img.gz
luisquintero@DESKTOP-P53ABHB:~/forence4/oni$ man mmls
luisquintero@DESKTOP-P53ABHB:~/forence4/oni$ fls -o 206848 disk.img
d/d 458:        home
d/d 11: lost+found
d/d 12: boot
d/d 13: etc
d/d 79: proc
d/d 80: dev
d/d 81: tmp
d/d 82: lib
d/d 85: var
d/d 94: usr
d/d 104:        bin
d/d 118:        sbin
d/d 464:        media
d/d 468:        mnt
d/d 469:        opt
d/d 470:        root
d/d 471:        run
d/d 473:        srv
d/d 474:        sys
V/V 33049:      $OrphanFiles
luisquintero@DESKTOP-P53ABHB:~/forence4/oni$ fls -o 206848 disk.img 470
r/r 2344:       .ash_history
d/d 3916:       .ssh
luisquintero@DESKTOP-P53ABHB:~/forence4/oni$ fls -o 206848 disk.img 3919
luisquintero@DESKTOP-P53ABHB:~/forence4/oni$ fls -o 206848 disk.img 3919
luisquintero@DESKTOP-P53ABHB:~/forence4/oni$ icat -o 206848 disk.img 2345
-----BEGIN OPENSSH PRIVATE KEY-----
b3BlbnNzaC1rZXktdjEAAAAABG5vbmUAAAAEbm9uZQAAAAAAAAABAAAAMwAAAAtzc2gtZW
QyNTUxOQAAACBgrXe4bKNhOzkCLWOmk4zDMimW9RVZngX51Y8h3BmKLAAAAJgxpYKDMaWC
gwAAAAtzc2gtZWQyNTUxOQAAACBgrXe4bKNhOzkCLWOmk4zDMimW9RVZngX51Y8h3BmKLA
AAAECItu0F8DIjWxTp+KeMDvX1lQwYtUvP2SfSVOfMOChxYGCtd7hso2E7OQItY6aTjMMy
KZb1FVmeBfnVjyHcGYosAAAADnJvb3RAbG9jYWxob3N0AQIDBAUGBw==
-----END OPENSSH PRIVATE KEY-----
luisquintero@DESKTOP-P53ABHB:~/forence4/oni$ icat -o 206848 disk.img 2345 > key_file
luisquintero@DESKTOP-P53ABHB:~/forence4/oni$ cat Key_file
cat: Key_file: No such file or directory
luisquintero@DESKTOP-P53ABHB:~/forence4/oni$ icat -o 206848 disk.img 2345 > key_file
luisquintero@DESKTOP-P53ABHB:~/forence4/oni$ cat key_file
-----BEGIN OPENSSH PRIVATE KEY-----
b3BlbnNzaC1rZXktdjEAAAAABG5vbmUAAAAEbm9uZQAAAAAAAAABAAAAMwAAAAtzc2gtZW
QyNTUxOQAAACBgrXe4bKNhOzkCLWOmk4zDMimW9RVZngX51Y8h3BmKLAAAAJgxpYKDMaWC
gwAAAAtzc2gtZWQyNTUxOQAAACBgrXe4bKNhOzkCLWOmk4zDMimW9RVZngX51Y8h3BmKLA
AAAECItu0F8DIjWxTp+KeMDvX1lQwYtUvP2SfSVOfMOChxYGCtd7hso2E7OQItY6aTjMMy
KZb1FVmeBfnVjyHcGYosAAAADnJvb3RAbG9jYWxob3N0AQIDBAUGBw==
-----END OPENSSH PRIVATE KEY-----
luisquintero@DESKTOP-P53ABHB:~/forence4/oni$ chmod 400 Key_file
chmod: cannot access 'Key_file': No such file or directory
luisquintero@DESKTOP-P53ABHB:~/forence4/oni$ cat key_file
-----BEGIN OPENSSH PRIVATE KEY-----
b3BlbnNzaC1rZXktdjEAAAAABG5vbmUAAAAEbm9uZQAAAAAAAAABAAAAMwAAAAtzc2gtZW
QyNTUxOQAAACBgrXe4bKNhOzkCLWOmk4zDMimW9RVZngX51Y8h3BmKLAAAAJgxpYKDMaWC
gwAAAAtzc2gtZWQyNTUxOQAAACBgrXe4bKNhOzkCLWOmk4zDMimW9RVZngX51Y8h3BmKLA
AAAECItu0F8DIjWxTp+KeMDvX1lQwYtUvP2SfSVOfMOChxYGCtd7hso2E7OQItY6aTjMMy
KZb1FVmeBfnVjyHcGYosAAAADnJvb3RAbG9jYWxob3N0AQIDBAUGBw==
-----END OPENSSH PRIVATE KEY-----
luisquintero@DESKTOP-P53ABHB:~/forence4/oni$ chmod 400 Key_file
chmod: cannot access 'Key_file': No such file or directory
luisquintero@DESKTOP-P53ABHB:~/forence4/oni$ chmod 400 Key_file
chmod: cannot access 'Key_file': No such file or directory
luisquintero@DESKTOP-P53ABHB:~/forence4/oni$ ssh -i key_file -p 58491 ctf-player@saturn.picoctf.net
ssh: connect to host saturn.picoctf.net port 58491: Connection refused
luisquintero@DESKTOP-P53ABHB:~/forence4/oni$ ssh -i key_file -p 53941 ctf-player@saturn.picoctf.net
The authenticity of host '[saturn.picoctf.net]:53941 ([13.59.203.175]:53941)' can't be established.
ED25519 key fingerprint is SHA256:XBSvB1lk28EctsAVdKJtsl0A7C5bonqPrvHCYH8aEy4.
This key is not known by any other names.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[saturn.picoctf.net]:53941' (ED25519) to the list of known hosts.
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
@         WARNING: UNPROTECTED PRIVATE KEY FILE!          @
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
Permissions 0644 for 'key_file' are too open.
It is required that your private key files are NOT accessible by others.

solo nos falto un chmood y ahora cambiandolo es
luisquintero@DESKTOP-P53ABHB:~/forence4/oni$ ssh -i key_file -p 53941 ctf-player@saturn.picoctf.net
Welcome to Ubuntu 20.04.5 LTS (GNU/Linux 6.5.0-1023-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

This system has been minimized by removing packages and content that are
not required on a system that users do not log into.

To restore this content, you can run the 'unminimize' command.

The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

ctf-player@challenge:~$ cat flag.txt
picoCTF{k3y_5l3u7h_339601ed}ctf-player@challenge:~$

BANDERA

==picoCTF{k3y_5l3u7h_339601ed}==
