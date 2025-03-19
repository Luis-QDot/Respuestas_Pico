#### Description

If I told you a word started with 0x70 in hexadecimal, what would it start with in ASCII?

vamos a usar el comando de python para adyudarnos en este problema
escribimos
python 

Luiscat02-picoctf@webshell:~$ python
Python 3.10.12 (main, Feb  4 2025, 14:57:36) [GCC 11.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> bytes.fromhex("70")
b'p'
>>> bytes.fromhex("70").decode()
'p'

y nos arroja que la bandera es la letra p, asi que solo le agregamos la bandera picoctf y listo

- **`bytes.fromhex("70")`** – Convierte el valor hexadecimal `70` en su equivalente en bytes (`b'p'`).
- **`.decode()`** – Convierte los bytes resultantes en una cadena de texto.
Bandera
==picoCTF{p}==
