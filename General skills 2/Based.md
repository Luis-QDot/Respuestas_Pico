#### Description

To get truly 1337, you must understand different data encodings, such as hexadecimal or binary. Can you get the flag from this program to prove you are on the way to becoming 1337? Connect with `nc jupiter.challenges.picoctf.org 29221`.


Solucion

Esto va a ser una carrera de  velocidad al decifrar las palabras clabes, por lo cual vamos a usar cyberchef para decifrar todo


primero nos logueamos donde nos dice  y luego
Let us see how data is stored
colorado
Please give the 01100011 01101111 01101100 01101111 01110010 01100001 01100100 01101111 as a word.
...
you have 45 seconds.....

Input:
colorado
Please give me the  155 141 160 as a word.
Input:
Too slow!

primer intento
 ya en el segundo intento es más rapido
 Luiscat02-picoctf@webshell:~$ nc jupiter.challenges.picoctf.org 29221
Let us see how data is stored
falcon
Please give the 01100110 01100001 01101100 01100011 01101111 01101110 as a word.
...
you have 45 seconds.....

Input:
falcon 
Please give me the  164 145 163 164 as a word.
Input:
test
Please give me the 6c696d65 as a word.
Input:
lime
You've beaten the challenge
Flag: picoCTF{learning_about_converting_values_00a975ff}
 y nos da nuestra bandera


BANDERA
==picoCTF{learning_about_converting_values_00a975ff}==

Referencias
https://www.youtube.com/watch?v=EVomRoUHD-M&pp=ygUNQmFzZWQgcGljb2N0ZtIHCQlPCQGHKiGM7w%3D%3D