CanYouSee
Brandon Omar Cardenas Gonzales
Luis Jesus Quintero Bañuelos
Description
How about some hide and seek?
Download this file here.

vamos a descargar el archivo con Wget https://artifacts.picoctf.net/c_titan/5/unknown.zip
Y le vamos a dar unzip 
despues le vamos dar exiftool a nuestro archivo y nos mostrara varia unformacion, copiamos una que es
luisquintero@DESKTOP-P53ABHB:~/Forencee/canyousee$ exiftool ukn_reality.jpg
ExifTool Version Number         : 12.76
File Name                       : ukn_reality.jpg
Directory                       : .
File Size                       : 2.3 MB
File Modification Date/Time     : 2024:02:15 16:40:17-06:00
File Access Date/Time           : 2024:02:15 16:40:17-06:00
File Inode Change Date/Time     : 2025:05:11 15:03:29-06:00
File Permissions                : -rw-r--r--
File Type                       : JPEG
File Type Extension             : jpg
MIME Type                       : image/jpeg
JFIF Version                    : 1.01
Resolution Unit                 : inches
X Resolution                    : 72
Y Resolution                    : 72
XMP Toolkit                     : Image::ExifTool 11.88
Attribution URL                 : cGljb0NURntNRTc0RDQ3QV9ISUREM05fNGRhYmRkY2J9Cg==
Image Width                     : 4308
Image Height                    : 2875
Encoding Process                : Baseline DCT, Huffman coding
Bits Per Sample                 : 8
Color Components                : 3
Y Cb Cr Sub Sampling            : YCbCr4:2:0 (2 2)
Image Size                      : 4308x2875
Megapixels                      : 12.4
luisquintero@DESKTOP-P53ABHB:~/Forencee/canyousee$
y una ves copiado nos vamos a cyberchef y nos pone BASE64 lo cual es nuestra bandera

BANDERa

==picoCTF{ME74D47A_HIDD3N_4dabddcb}==


Notas adicionales
descubrimos y usamos el exiftool en los archivos

Referencias
https://www.youtube.com/watch?v=VTx9DSfEcmM&pp=ygUTY2FueW91c2VlbWUgcGljb2N0Zg%3D%3D