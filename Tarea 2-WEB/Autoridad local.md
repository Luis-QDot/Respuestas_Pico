Descripción
¿Puedes conseguir la bandera?
Vaya a este sitio web y vea lo que puede descubrir.

vamos a abrir el codigo fuente y vamos a hacer la acccion que nos dice, agregamdo un /login.php a la pagina 
 estando ahi vamos a abrir el script
 <script src="secure.js"></script>
y nos salen las credenciales para acceder 
function checkPassword(username, password)
{
  if( username === 'admin' && password === 'strongPassword098765' )
  {
    return true;
  }
  else
  {
    return false;
  }
}

accedemos y nos da las banderas
==picoCTF{j5_15_7r4n5p4r3n7_a8788e61}==

Referencia
https://www.youtube.com/watch?v=PgYT8FX4Jm8