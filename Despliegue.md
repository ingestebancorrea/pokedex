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
![image](https://user-images.githubusercontent.com/111609882/198686168-e38616cc-bcb4-40c8-b57c-9c53e0e1bc92.png)
<br>

El archivo server.js contendra lo siguiente:
![image](https://user-images.githubusercontent.com/111609882/198686730-8c54549e-e46f-4b77-ac69-9dc5c503ee79.png)

Básicamente con ayuda de los paquetes instalados se crea un servidor a partir de algunos parámetros, como el puerto y la raíz del proyecto.

<h3>Ejecutar Script</h3>

Ahora que se tiene el script para poder crear el servidor, se debe indicar al proyecto que al iniciarse ejecute el script, esto se logra modificando la sección de scripts del archivo package.json del proyecto. Allí, se debe añadir la instrucción “start”: “node server.js”, de la siguiente forma:


Al momento de realizar el despliegue Heroku ejecutará este comando y se creará el servidor.

<h2>Despliegue</h2>

Una vez se ha modificado el código se puede realizar el proceso de despliegue con Heroku, esto se realiza ejecutando algunos comandos desde una consola en la raíz del proyecto, estos comandos básicamente permiten conectarse con Heroku a través de su CLI anteriores) y con ayuda de git, indicar cual es la versión del proyecto que se desea desplegar.

<h3>Conectarse a Heroku</h3>

Para poder establecer contacto con Heroku se debe loguear con ayuda de su CLI, esto se logra ejecutando el siguiente comando en un cmd, bash o terminal y presionando la tecla espacio:

heroku login

Esto abrirá una ventana en el navegador que permitirá loguearse:



