<h1 align="center"> ⚡ CRUD operations with FastAPI </h1>
<p align="justify"> Aplicación backend construida con FastAPI que permite realizar operaciones CRUD (Create, Read, Update, Delete) sobre una BD PostgreSQL. </p>
<h2 align="left"> ● Pasos: </h2>
<p align="justify">1. En una terminal se ejecuta el comando <code>docker run --name fastapi-postgres -e POSTGRES_PASSWORD=password -d -p 5432:5432 postgres:14.17</code> para crear un contenedor PostgreSQL con Docker.</p>
<p align="justify">2. Se inserta el comando <code>docker exec -it fastapi-postgres psql -U postgres</code> para acceder a la consola interactiva de PostgreSQL dentro del contenedor <code>fastapi-postgres</code>.</p>
<p align="justify">3. Se crea una base de datos mediante el comando <code>create database fastapi_database;</code>.</p>
<p align="justify">4. Se crea un usuario mediante el comando <code>create user myuser with encrypted password 'password';</code>.</p>
<p align="justify">5. Se le añaden permisos al usuario para que pueda realizar operaciones sobre la base de datos mediante el comando <code>grant all privileges on database fastapi_database to myuser;</code>.</p>
<p align="justify">6. Accedemos a <code>fastapi_database</code> mediante el comando <code>\c fastapi_database</code>.</p>
<p align="justify">7. En una nueva terminal, creamos un entorno virtual <code>python3 -m venv venv</code> y lo activamos <code>source venv/bin/activate</code>. Posteriormente, instalamos los recursos necesarios <code>pip3 install "fastapi[all]" SQLAlchemy psycopg2-binary</code>.</p>
<p align="justify">7. Introducimos el comando <code>uvicorn main:app --reload</code> para ejecutar la aplicación FastAPI.</p>
<p align="justify">8. Accedemos a <code>http://127.0.0.1:8000/docs</code> para probar las funcionalidades de la API implementada.</p>
<p align="left">
  <img src="./images/Captura_2.JPG" alt="6" width="1000"/>
</p>
<hr>
<h2 align="left"> ● Post: </h2>
<p align="justify">Ejm: Se añaden 3 contactos a la tabla <i>contacts</i>. Para ello, se sigue el siguiente esquema:</p>
{<br>
  "first_name": "string",<br>
  "last_name": "string",<br>
  "email": "string",<br>
  "phone_number": "string"<br>
}
<br><br>
<p align="left">
  <img src="./images/Captura_3.JPG" alt="6" width="500"/>
</p>
<p align="left">
  <img src="./images/Captura_5.JPG" alt="6" width="500"/>
</p>
<p align="left">
  <img src="./images/Captura_4.JPG" alt="6" width="500"/>
</p>
<p align="justify"></p>
<hr>
<h2 align="left"> ● GET: </h2>
<p align="justify">Se muestran todos los contactos de la tabla <i>contacts</i>.</p>
<p align="left">
  <img src="./images/Captura_6.JPG" alt="6" width="500"/>
</p>
<p align="left">
  <img src="./images/Captura_7.JPG" alt="6" width="500"/>
</p>
<h2 align="left"> ● GET {contact_id}: </h2>
<p align="justify">Ejm: Se quiere mostrar toda la información del contacto con <i>id = 2 (existe)</i> de la tabla <i>contacts</i>.</p>
<p align="left">
  <img src="./images/Captura_8.JPG" alt="6" width="500"/>
</p>
<p align="justify">Ejm: Se quiere mostrar toda la información del contacto con <i>id = 4 (no existe)</i> de la tabla <i>contacts</i>.</p>
<p align="left">
  <img src="./images/Captura_9.JPG" alt="9" width="500"/>
</p>
<p align="left">
  <img src="./images/Captura_10.JPG" alt="6" width="500"/>
</p>
<hr>
<h2 align="left"> ● PUT {contact_id}: </h2>
<p align="justify">Ejm: Se quiere actualizar el contacto con <i>id = 3 (existe)</i> de la tabla <i>contacts</i>. Para ello, se sigue el siguiente esquema:</p>
{<br>
  "first_name": "string",<br>
  "last_name": "string",<br>
  "email": "string",<br>
  "phone_number": "string"<br>
}
<br><br>
<p align="left">
  <img src="./images/Captura_11.JPG" alt="6" width="500"/>
</p>
<p align="left">
  <img src="./images/Captura_12.JPG" alt="6" width="500"/>
</p>
<p align="justify">Ejm: Se quiere actualizar el contacto con <i>id = 4 (no existe)</i> de la tabla <i>contacts</i>.</p>
<p align="left">
  <img src="./images/Captura_13.JPG" alt="6" width="500"/>
</p>
<p align="left">
  <img src="./images/Captura_14.JPG" alt="6" width="500"/>
</p>
