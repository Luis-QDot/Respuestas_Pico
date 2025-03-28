#### Description

Do you know how to move between directories and read files in the shell? Start the container, `ssh` to it, and then `ls` once connected to begin. Login via `ssh` as `ctf-player` with the password, `a13b7f9d`

Additional details will be available after launching your challenge instance.

Una vez empezamos el reto 
nos va a pedir quenos conectmos aqui |   |   |
|---|---|
|SSH|`ssh ctf-player@venus.picoctf.net -p 56747`|
asi que conectamos


Luiscat02-picoctf@webshell:~$ ssh ctf-player@venus.picoctf.net -p 56747
The authenticity of host '[venus.picoctf.net]:56747 ([3.131.124.143]:56747)' can't be established.
ED25519 key fingerprint is SHA256:P1f6h95BrSVnJbm2AKhphfHHGEyAeThib/rN/AwKs24.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[venus.picoctf.net]:56747' (ED25519) to the list of known hosts.
ctf-player@venus.picoctf.net's password: 
Y nos va a apedir la constraseña que ya nos proporcionaron
a13b7f9d
Una vez dentro hacemos ls y nos aparece 
1of3.flag.txt  instructions-to-2of3.txt
ctf-player@pico-chall$ 
le hacemos cat y nos aparece una parte de la bandera

ctf-player@pico-chall$ cat 1of3.flag.txt 
picoCTF{xxsh_
al intentar hacer cat no nos deja 
ctf-player@pico-chall$ cat instructions-to-2of3.txt 
Next, go to the root of all things, more succinctly `/`
ctf-player@pico-chall$ cd /
al hacer el cd nos aparece 
Next, go to the root of all things, more succinctly `/`
ctf-player@pico-chall$ cd /
ctf-player@pico-chall$ ls
2of3.flag.txt  bin  boot  dev  etc  home  instructions-to-3of3.txt  lib  lib64  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
ctf-player@pico-chall$ cat 2of3.flag.txt 
0ut_0f_\/\/4t3r_
ctf-player@pico-chall$ ls
2of3.flag.txt  bin  boot  dev  etc  home  instructions-to-3of3.txt  lib  lib64  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
ctf-player@pico-chall$ cat instructions-to-3of3.txt 
Lastly, ctf-player, go home... more succinctly `~`
ctf-player@pico-chall$ cd~

Por lo que hicimos un cd más como nos aparece y al hacer otro ls nos aparece
ctf-player@pico-chall$ ls
3of3.flag.txt  drop-in

asi que le hacemos cat y nos aparece la otraparte de la bandera

ctf-player@pico-chall$ cat 3of3.flag.txt 
71be5264}
picoCTF{xxsh_
0ut_0f_\/\/4t3r_
71be5264}
asi que al juntar las tres partes nos sale 
picoCTF{xxsh_0ut_0f_\/\/4t3r_71be5264}


### NOTAS ADICIONALES

- **`ssh [usuario]@[host] -p [puerto]`** – Conectar a una máquina remota mediante SSH en un puerto especificado.
- **`ls`** – Listar los archivos en el directorio actual.
- **`cd [directorio]`** – Cambiar de directorio.
- **`cat [archivo]`** – Mostrar el contenido de un archivo.

### BANDERA

==`picoCTF{xxsh_0ut_0f_\/\/4t3r_71be5264}`==

Referencias
https://www.youtube.com/watch?v=duEwM4xC-dw&pp=ygUgTWFnaWthcnAgR3JvdW5kIE1pc3Npb24gIHBpY29jdGY%3D