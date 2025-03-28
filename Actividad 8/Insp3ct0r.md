#### Descripción

Kishor Balan nos avisó que el siguiente código podría necesitar inspección: `https://jupiter.challenges.picoctf.org/problem/9670/`( [enlace](https://jupiter.challenges.picoctf.org/problem/9670/) ) o http://jupiter.challenges.picoctf.org:9670

Vamos a entrar al enlace e inspeccionar el codigo
luego nos fijamos que hasta abajo esta la primera parte de la bandera
Html is neat. Anyways have 1/3 of the flag: picoCTF{tru3_d3 -->

luego entramos a este herf href="[mycss.css](https://jupiter.challenges.picoctf.org/problem/9670/mycss.css)">
y al abrirlo nos aparece la parte 2 
/* You need CSS to make pretty pages. Here's part 2/3 of the flag: t3ct1ve_0r_ju5t */
y por ultimo entramos a 
src="[myjs.js](https://jupiter.challenges.picoctf.org/problem/9670/myjs.js)"></script>
y ahi hasta abajo va a estra la parte 3 de la bandera
/* Javascript sure is neat. Anyways part 3/3 of the flag: _lucky?2e7b23e3} */

BANDERA
==picoCTF{tru3_d3t3ct1ve_0r_ju5t_lucky?2e7b23e3}==