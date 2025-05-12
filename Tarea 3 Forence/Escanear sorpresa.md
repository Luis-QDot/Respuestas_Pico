Escanear sorpresa

Brandon Omar Cardenas Gonzales
Luis Jesus Quintero Bañuelos
Descripción
Me aburrí de repartir banderas como texto. ¿No sería genial si fueran una imagen?
Puedes descargar los archivos del desafío aquí:
desafío.zip

The same files are accessible via SSH here:
ssh -p 62609 ctf-player@atlas.picoctf.net
Using the password 6dd28e9b. Accept the fingerprint with yes, and ls once connected to begin. Remember, in a shell, passwords are hidden!


asi que vamos a descargar el archivo
lo vamos a descomprimir con unzip
vemos que nos creo una carpeta y le damos cd y vemos con ls que hay otra y asi seguimos
hasta llegar a una imagen 
asi que le hacemos cat
pero sino tambien nos podemos conectar con lo que nos dice
ssh -p 62609 ctf-player@atlas.picoctf.net

Using the password 6dd28e9b. Accept the fingerprint with yes, and ls once connect
y nos manda el mismo QR pero si le aplicamos un comando, nos puede dar la informacion

ctf-player@challenge:~/drop-in$ zbarimg flag.png
Connection Error (Failed to connect to socket /var/run/dbus/system_bus_socket: No such file or directory)
Connection Null
QR-Code:picoCTF{p33k_@_b00_a81f0a35}
scanned 1 barcode symbols from 1 images in 0 seconds

ctf-player@challenge:~/drop-in$


y nos da la bandera

==BANDERA==
==picoCTF{p33k_@_b00_a81f0a35}==


NOtas adicionales
Usamos el comando zbarimg para que nos diera informacion que contenia la imagen


Referencias
https://www.youtube.com/watch?v=ubnU0Han6eg
