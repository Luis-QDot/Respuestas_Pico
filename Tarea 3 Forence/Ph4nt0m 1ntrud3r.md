Ph4nt0m 1ntrud3r
Brandon Omar Cardenas Gonzales
Luis Jesus Quintero Bañuelos
Descripción
¡Un fantasma digital ha traspasado mis defensas y me han robado mis datos confidenciales! 😱💻 Tu misión es descubrir cómo este intruso fantasma se infiltró en mi sistema y recuperar la bandera oculta.
Para resolver este desafío, deberá analizar el archivo PCAP proporcionado y rastrear el método de ataque. El atacante ha ocultado sus movimientos con astucia y a tiempo. ¡Explore el tráfico de red, aplique los filtros adecuados, demuestre su pericia forense y desenmascare al intruso digital!
Encuentre el archivo PCAP aquí Archivo PCAP de tráfico de red e intente obtener la bandera.

vamos a descargar el archivo y vamos a abrirlo con wiresharky vemos que tiene los paquetes tCP
usamos el comando
tshark -r myNetworkTraffic.pcap -Y "tcp. len==12 || tcp.len==4" 
para que nos de los datos de los TCP de los paquetes
Luego descubrí que, al ordenar el "Tiempo" en orden ascendente y revisar los últimos paquetes, podemos reconstruir la bandera.
asi que usamos los siguientes comandos
tshark -r myNetworkTraffic.pcap -Y "tcp. len==12 || tcp.len==4" -T fields -e frame.time
y nos sale asi 
 tshark -r myNetworkTraffic.pcap -Y "tcp.len==12 || tcp.len==4" -T fields -
e frame.time
Mar  5, 2025 21:32:10.523508000 CST
Mar  5, 2025 21:32:10.522049000 CST
Mar  5, 2025 21:32:10.523288000 CST
Mar  5, 2025 21:32:10.522825000 CST
Mar  5, 2025 21:32:10.522508000 CST
Mar  5, 2025 21:32:10.523062000 CST
Mar  5, 2025 21:32:10.522277000 CST
luisquintero@DESKTOP-P53ABHB:~/Forencee/insp$
y ahora con 
luisquintero@DESKTOP-P53ABHB:~/Forencee/insp$ tshark -r myNetworkTraffic.pcap -Y "tcp.len==12 || tcp.len==4" -T fields -e frame.time -e tcp.segment_data | sort -k4
Mar  5, 2025 21:32:10.522049000 CST     63476c6a62304e5552673d3d
Mar  5, 2025 21:32:10.522277000 CST     657a46305833633063773d3d
Mar  5, 2025 21:32:10.522508000 CST     626e52666447673064413d3d
Mar  5, 2025 21:32:10.522825000 CST     587a4d3063336c6664413d3d
Mar  5, 2025 21:32:10.523062000 CST     596d68664e484a664f413d3d
Mar  5, 2025 21:32:10.523288000 CST     5a5445775a54677a4f513d3d
Mar  5, 2025 21:32:10.523508000 CST     66513d3d
luisquintero@DESKTOP-P53ABHB:~/Forencee/insp$

y al final para filtar con todos los valores de 64 vamos a poner el siguiente codigo
luisquintero@DESKTOP-P53ABHB:~/Forencee/insp$ tshark -r myNetworkTraffic.pcap -Y "tcp.len==12 || tcp.len==4" -T fields -e frame.time -e tcp.segment_data | sort -k4 | awk '{print $6}' | xxd -p -r | base64 -d
picoCTF{1t_w4snt_th4t_34sy_tbh_4r_8e10e839}luisquintero@DESKTOP-P53ABHB:~/Forencee/insp$
luisquintero@DESKTOP-P53ABHB:~/Forencee/insp$

Y nos la nuestra bandera

==picoCTF{1t_w4snt_th4t_34sy_tbh_4r_8e10e839}==

BANDERA

==picoCTF{1t_w4snt_th4t_34sy_tbh_4r_8e10e839}==


Refrencias
https://www.youtube.com/watch?v=_YKC5Smffeg
