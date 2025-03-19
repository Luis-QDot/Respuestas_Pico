nos vamos a login con las credencaiales que nos proporcionaron
Use ssh to connect to this server:

```
Server: saturn.picoctf.net
Port: 53223
Username: picoplayer 
Password: ENAFb6zfzn
``` 
usando ssh picoplayer@saturn... -p (puer

Luiscat02-picoctf@webshell:~$ ssh picoplayer@saturn.picoctf.net -p 53223
The authenticity of host '[saturn.picoctf.net]:53223 ([13.59.203.175]:53223)' can't be established.
ED25519 key fingerprint is SHA256:dMTscRrUiURy7uMu5eGWwEKdd2FzqLzx6LfWhssWnNQ.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[saturn.picoctf.net]:53223' (ED25519) to the list of known hosts.
picoplayer@saturn.picoctf.net's password: 
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

picoplayer@challenge:~$  


luego vamos a usar el comando 
picoplayer@challenge:~$ cat /etc/crontab

el cual nos dara la bandera
picoplayer@challenge:~$ cat /etc/crontab
# picoCTF{Sch3DUL7NG_T45K3_L1NUX_1d781160}
picoplayer@challenge:~$ 




