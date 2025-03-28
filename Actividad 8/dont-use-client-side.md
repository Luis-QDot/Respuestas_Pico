#### Descripción

¿Puedes entrar en este portal súper seguro? `https://jupiter.challenges.picoctf.org/problem/17682/`( [enlace](https://jupiter.challenges.picoctf.org/problem/17682/) ) o http://jupiter.challenges.picoctf.org:17682




le damos click al link y luego inspeccionamos el codigo
y nos fijamos en estro 
|   |
|---|
|if (checkpass.substring(0, split) == 'pico') {|
||if (checkpass.substring(split*6, split*7) == '706c') {|
||if (checkpass.substring(split, split*2) == 'CTF{') {|
||if (checkpass.substring(split*4, split*5) == 'ts_p') {|
||if (checkpass.substring(split*3, split*4) == 'lien') {|
||if (checkpass.substring(split*5, split*6) == 'lz_b') {|
||if (checkpass.substring(split*2, split*3) == 'no_c') {|
||if (checkpass.substring(split*7, split*8) == '5}') {|
||alert("Password Verified")|
asi que siguiendo la logica,ahi va a aparecer la bandera, asi que vamos a armar la bandera
siguiendo la logica de substric para substraer todo lo que nos interesa

BANDERA
picoCTF{not_a_r3a1ly_l_5ab1e}
