vamos a abrir el wireshark capture.pcap para rastear los paquetes, vemos la bandera pero todo esta encriptado, o sea que esta bien protejido.
pero tenemos la llave asi que 
vamos a edicion, preferencias, protocolos y escribimos para ir a TLS
Entonces ahi modificamos en edit 
cargamos nuestro otro archivo descargado que es la llave , ahora para buscar la llave debe de aparecer en los verdes, perpo buscamos en el menu de nusqueda con CRT F

picoCTF y que bsuque en los detalles de los paquetes y la encuentra 

y ahi esta nuestra bandera



ssldump -r capture.pcap -k picopico.jey -d | grep pico -A 2

BANDERA
==picoCTF{nongshim.shrimp.crackers}==

