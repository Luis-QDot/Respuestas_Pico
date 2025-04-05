Descripción
Tenemos varias páginas ocultas. ¿Puedes encontrar la de la bandera?
El sitio web se está ejecutando aquí .

vamos a abrir la pagina y la vamos a inspeccionar
luego agregamos esto aesto
http://saturn.picoctf.net:58719/secret/
y llendo a esta pagina, vamos a inspeccionar la nueva pagina
y ahora agregamos esto 
view-source:http://saturn.picoctf.net:58719/secret/hidden/
y inspeccionamos el codigo
luego agregamos eso al url 
view-source:http://saturn.picoctf.net:58719/secret/hidden/superhidden/

y volviendo a inspeccionar la pagina, nos da la bandera
<body>
    <h1>Finally. You found me. But can you see me</h1>
    <h3 class="flag">picoCTF{succ3ss_@h3n1c@10n_39849bcf}</h3>
  </body>
</html>


Bandera
==picoCTF{succ3ss_@h3n1c@10n_39849bcf}==

Referencias
https://www.youtube.com/watch?v=40DYCMInk5E