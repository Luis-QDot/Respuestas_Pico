Description
How about trying to match a regular expression
The website is running here.

vamos a abrir el link 
y tenemos que hacer coincidir una expresion regular 

vamos a ver el codigo fuente y nos encontramos con un codigo de java
function send_request() {
		let val = document.getElementById("name").value;
		// ^p.....F!?
		fetch(`/flag?input=${val}`)
			.then(res => res.text())
			.then(res => {
				const res_json = JSON.parse(res);
				alert(res_json.flag)
				return false;
			})
		return false;
	}



vamos a buscar una pagina llamadaregexr.com y pondremos nuestro regex ahi y esta es nuestra palabra regular 
^p.....F!?

entonces ponemos p12345F y esa es nuestra expresion, lo ponemos en el login de la pagina y nos da la bandera

BANDERA
==picoCTF{succ3ssfully_matchtheregex_8ad436ed}==

Notas adicionales
expresion regular o regex

Referencias
