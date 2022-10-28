<h1>Despliegue de aplicación Pokedex en Heroku</h1>

<h2>Crear App Heroku</h2>

Dado que el despliegue se realizará a través de la plataforma Heroku, lo primero que se debe realizar es crear una aplicación para el componente de frontend.

iniciar el proceso de creación de una nueva aplicación:
![image](https://user-images.githubusercontent.com/111609882/198682561-4997c009-2ac0-490d-8d02-05269d528980.png)

<br>

Ahora se debe ingresar un nombre descriptivo para la aplicación y luego crear la aplicación:
![image](https://user-images.githubusercontent.com/111609882/198683008-62475d9f-c7aa-409d-8b88-10435696f5c5.png)

<br>

Con los pasos anteriores se ha creado una aplicación, la cual servirá para realizar el proceso de despliegue del componente de front-end.

<h2>Editar Código</h2>
Para llevar a cabo el despliegue del componente pokedex-fe con Heroku, es necesario realizar algunos cambios sobre el código, estos cambios permitirán crear el servidor sobre el cual Heroku realizará el despliegue del componente.

<h3>Instalar Paquetes</h3>

Para poder crear el servidor que usará Heroku para llevar a cabo el despliegue, es necesario instalar algunos paquetes de NodeJs en el proyecto. Estos paquetes son express y server-stactic, y se instalan ejecutando el siguiente comando en una consola ubicada en la raíz del proyecto.

npm install express serve-static --save

<h3>Crear Server</h3>

El servidor se creará a través de un script, por cual se debe crear un archivo llamado server.js el cual estará en la raíz del proyecto.
![image](https://user-images.githubusercontent.com/111609882/198724140-52e88afa-3fca-412e-8f9f-bd13115b09b9.png)
<br>

El archivo server.js contendra lo siguiente:
![image](https://user-images.githubusercontent.com/111609882/198689797-02227444-00d7-489f-9992-8dc707ca9c98.png)

Básicamente con ayuda de los paquetes instalados se crea un servidor a partir de algunos parámetros, como el puerto y la raíz del proyecto.

<br>

<h3>Ejecutar Script</h3>

Ahora que se tiene el script para poder crear el servidor, se debe indicar al proyecto que al iniciarse ejecute el script, esto se logra modificando la sección de scripts del archivo package.json del proyecto. Allí, se debe añadir la instrucción “start”: “node server.js”, de la siguiente forma:
![image](https://user-images.githubusercontent.com/111609882/198691446-162d5968-129b-41ca-bfb0-1c676c7ca7e5.png)

<br>

Al momento de realizar el despliegue Heroku ejecutará este comando y se creará el servidor.

<h2>Despliegue</h2>

Una vez se ha modificado el código se puede realizar el proceso de despliegue con Heroku, esto se realiza ejecutando algunos comandos desde una consola en la raíz del proyecto, estos comandos básicamente permiten conectarse con Heroku a través de su CLI anteriores) y con ayuda de git, indicar cual es la versión del proyecto que se desea desplegar.

<h3>Conectarse a Heroku</h3>

Para poder establecer contacto con Heroku se debe loguear con ayuda de su CLI, esto se logra ejecutando el siguiente comando en un cmd, bash o terminal y presionando la tecla espacio:

heroku login
![image](https://user-images.githubusercontent.com/111609882/198691789-88493f80-9e7e-43f0-b3c8-9ca3e5aee7a9.png)

<br>

Esto abrirá una ventana en el navegador que permitirá loguearse:
![image](https://user-images.githubusercontent.com/111609882/198691748-e197fa04-eaff-4cd1-8d7b-db910a95b4d2.png)
<br>

Una vez logueado, debe salir el siguiente mensaje en el navegador y la terminal se debe actualizar:

![image](https://user-images.githubusercontent.com/111609882/198691951-0250ac3c-d199-4bfa-b0f4-0fbb20724ef3.png)
<br>

<h3>Inicializar Repositorio</h3>
Dado que Heroku maneja el código de despliegue utilizando un repositorio de git, se debe tener uno en el componente.
<img src="https://user-images.githubusercontent.com/111609882/198707210-b2e7bac7-db9b-4b7b-92e4-40a3c81500e1.png">

<h3>Agregar Remoto al Repositorio</h3>
<p>El código fuente del componente será subido a un repositorio remoto administrado por Heroku, desde el cual se realizará el despliegue, para agregar este repositorio remoto al repositorio local se debe ejecutar el siguiente comando:</p>
<img src="https://user-images.githubusercontent.com/111609882/198695446-cfd9e6d6-5452-4424-a80b-6673e04701e5.png">

<h3>Realizar Commit</h3>
<p>Se debe crear un commit que incluya todos los archivos referentes al estado actual del proyecto, incluidos los últimos cambios realizados. Esto se logra con los siguientes comandos:</p>
<img src="https://user-images.githubusercontent.com/111609882/198695853-2f88d9f9-d922-48da-a711-804c761637b6.png">

<h3>Realizar Despliegue</h3>
En este punto se puede completar el despliegue del componente, para esto únicamente bastará con subir el último commit al repositorio remoto de heroku. Esto se logra con el siguiente comando:
<img src="https://user-images.githubusercontent.com/111609882/198693017-b188a5a9-b91d-4644-8ff5-7d65fb725c4f.png">
<br>

<h2>Acceder a la Aplicación</h2>
Una vez se ha realizado el despliegue de la aplicación se puede acceder a esta a través de su respectiva URL. Para ello, se debe dar click en el botón Open app, en el dashboard de Heroku:
<img src="https://user-images.githubusercontent.com/111609882/198693415-acd93a3c-9acc-4dc1-a292-b99c4f5d3c22.png">

Esto abrirá la página principal del componente de front-end de pokedex:



