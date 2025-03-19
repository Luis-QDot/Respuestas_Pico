Empezamos descargando nuestro archivo con 
wget https://artifacts.picoctf.net/c_titan/177/challenge.zip

Al descomprimir usamos un 
Luiscat02-picoctf@webshell:~/drop-in$ git  branch -a 


------------------------
Luego de mostrarnos las tres partes hacemos un Luiscat02-picoctf@webshell:~/drop-in$ git checkout feature/part-1 
para cada parte, en este caso son 3

luego de hacer el checkout, hacemos un Ls y nos muestra un archivo flag. py 
le hacemos cat y nos muestra una parte de la bandera, lo hacemos con las otras 2 y juntamos toda la bandera 


Luiscat02-picoctf@webshell:~/drop-in$ git  branch -a 

[4]+  Stopped                 git branch -a
Luiscat02-picoctf@webshell:~/drop-in$ git checkout feature/part-1
Warning: you are leaving 1 commit behind, not connected to
any of your branches:

  6921b0e metged

If you want to keep it by creating a new branch, this may be a good time
to do so with:

 git branch <new-branch-name> 6921b0e

Switched to branch 'feature/part-1'
Luiscat02-picoctf@webshell:~/drop-in$ flag.py
-bash: flag.py: command not found
Luiscat02-picoctf@webshell:~/drop-in$ ls
flag.py
Luiscat02-picoctf@webshell:~/drop-in$ cat falg.py
cat: falg.py: No such file or directory
Luiscat02-picoctf@webshell:~/drop-in$ cat flag.py
print("Printing the flag...")
print("picoCTF{t3@mw0rk_", end='')Luiscat02-picoctf@webshell:~/drop-in$ 
Luiscat02-picoctf@webshell:~/drop-in$ 
Luiscat02-picoctf@webshell:~/drop-in$ git checkout feature/part-2
Switched to branch 'feature/part-2'
Luiscat02-picoctf@webshell:~/drop-in$ cat flag.py
print("Printing the flag...")

print("m@k3s_th3_dr3@m_", end='')Luiscat02-picoctf@webshell:~/drop-in$ 
Luiscat02-picoctf@webshell:~/drop-in$ git checkout feature/part-3
Switched to branch 'feature/part-3'
Luiscat02-picoctf@webshell:~/drop-in$ cat flag.py
print("Printing the flag...")

print("w0rk_7ae8dd33}")
Luiscat02-picoctf@webshell:~/drop-in$ 


picoCTF{t3@mw0rk_
m@k3s_th3_dr3@m_
w0rk_7ae8dd33

picoCTF{t3@mw0rk_m@k3s_th3_dr3@m_w0rk_7ae8dd33}

