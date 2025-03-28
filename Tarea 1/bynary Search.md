Sorry, you've exceeded the maximum number of guesses.
Connection to atlas.picoctf.net closed.
Luiscat02-picoctf@webshell:~$ ssh -p 59161 ctf-player@atlas.picoctf.net
ctf-player@atlas.picoctf.net's password: 
Welcome to the Binary Search Game!
I'm thinking of a number between 1 and 1000.
Enter your guess: 500
Lower! Try again.
Enter your guess: 250
Higher! Try again.
Enter your guess: 375
Lower! Try again.
Enter your guess: 312
Lower! Try again.
Enter your guess: 281
Lower! Try again.
Enter your guess: 265
Lower! Try again.
Enter your guess: 257
Higher! Try again.
Enter your guess: 261
Higher! Try again.
Enter your guess: 263
Lower! Try again.
Enter your guess: 262
Congratulations! You guessed the correct number: 262
Here's your flag: picoCTF{g00d_gu355_6dcfb67c}
Connection to atlas.picoctf.net closed.
Luiscat02-picoctf@webshell:~$ 

se resolvio usando la busqueda binaria que como lo eh visto en clase es agarrar un numero a la mitad del arreglo ordenado y luego si es mas alto pues 1/4 del problema original se le suma, si da mas, se suman los dos numeros entre los cuales esta y se divide entre dos y asi susesivamente hasta llegar al numero que buscamos 
Referencias

https://www.youtube.com/watch?v=0qzEqPWw6Oc&pp=ygUSYnluYXJ5IFNlYXJjaCBwaWNv