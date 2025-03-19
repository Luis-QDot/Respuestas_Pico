#### Description

Run the Python script `code.py` in the same directory as `codebook.txt`.

- [Download code.py](https://artifacts.picoctf.net/c/3/code.py)
- [Download codebook.txt](https://artifacts.picoctf.net/c/3/codebook.txt)
nos da como pistas
On the webshell, use `ls` to see if both files are in the directory you are in


Asi que primero descarguemos nuestros archivos con wget
una ves descargado lo vamos a ejecutar con python todos nuestros archivos junto y nos da la bandera

Luiscat02-picoctf@webshell:~$ python3 code.py codebook.txt 
picoCTF{c0d3b00k_455157_197a982c}
Luiscat02-picoctf@webshell:~$ 


Bandera
picoCTF{c0d3b00k_455157_197a982c}

**NOTAS ADICIONALES:**

- El comando `python3` se utiliza para ejecutar scripts escritos en Python 3.
- Asegúrate de que el archivo `codebook.txt` esté en el formato adecuado para ser procesado por el script `code.py`.

**BANDERA:**  
==picoCTF{c0d3b00k_455157_197a982c}==