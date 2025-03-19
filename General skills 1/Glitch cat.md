#### Description

Our flag printing service has started glitching!

Additional details will be available after launching your challenge instance.


le damos a empezar y nos dice 
Our flag printing service has started glitching!`$ nc saturn.picoctf.net 52362`
por lo que vamos a copiar y pegar el mensaje en nuestra terminal ya que viene con el comando nc 
y al pegarlo y darle enter nos aparece nuestra bandera de este modo 
'picoCTF{gl17ch_m3_n07_' + chr(0x62) + chr(0x64) + chr(0x61) + chr(0x36) + chr(0x38) + chr(0x66) + chr(0x37) + chr(0x35) + '}'

por lo que vamos a usar el comando "python -c "print()'picoCTF{gl17ch_m3_n07_' + chr(0x62) + chr(0x64) + chr(0x61) + chr(0x36) + chr(0x38) + chr(0x66) + chr(0x37) + chr(0x35) + '}')"

y nos arroja nuestra bandera ya sin glitch 

### NOTAS ADICIONALES

- **`nc [host] [port]`** – Se conecta a un servicio remoto utilizando netcat.
- `saturn.picoctf.net` → Dirección del servidor.
- `52362` → Puerto del servicio.
- **`python -c "[código]"`** – Ejecuta un fragmento de código Python desde la línea de comandos.
- `chr(0x62)` → Convierte el valor hexadecimal `0x62` en su carácter ASCII correspondiente (`b`).
Bandera
==picoCTF{gl17ch_m3_n07_bda68f75}==
