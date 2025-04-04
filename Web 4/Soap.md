Descripción
El proyecto web se realizó con prisas y no se realizó ninguna evaluación de seguridad. ¿Puedes leer el archivo /etc/passwd?
Portal web

vamos a inspreccionar elcodigo fuente
y vemos este codigo 
<div class="col-md-4">
          <div class="card mb-4 shadow-sm">
              <img src="/static/image2.png" class="bd-placeholder-img
              card-img-top" width="100%" height="225">
            <div class="card-body">
                <p class="card-text"><b>Carnegie Mellon  University Africa</b> Offers 3 masters degree programs.</p>
              <div class="d-flex justify-content-between align-items-center">
                <div class="btn-group">
                    <form class="detailForm" action="/data" method="POST">
                        <input required type="hidden" name="ID" value="1">
                  <button type="submit" class="btn btn-sm
                      btn-outline-secondary">Details</button>
                    </form>
                </div>
              </div>
            </div>
          </div>
        </div>


vamos a usar Burp y nos da 3 peticiones de post
y con chatgpt vamos a hacer unos pailoads para hacer parcer 


Bandera
==picoCTF{XML_3xtern@l_3nt1t1ty_e5f02dbf}==
Referencias

https://www.youtube.com/watch?v=b1pGlutUL34&pp=ygUWU29hcCBwaWNvIGN0ZiBlc3Bhw7FvbA%3D%3D