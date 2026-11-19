1. Objetivo de la práctica

El objetivo de esta práctica es aprender a utilizar la función include de PHP para insertar el contenido de otros archivos dentro de una página web.

2. Estructura del proyecto

El proyecto está organizado de la siguiente manera:

.vscode/launch.json: configuración de depuración de PHP con Xdebug.

app/index.php: archivo principal de la página web.

app/encabezado.php: contiene la cabecera HTML.

app/pie.html: contiene el pie de página.

docker-compose.yml: configuración del entorno Docker.

README.md: documentación de la práctica.

3. Funcionamiento del código

En el archivo index.php declaramos una variable llamada $titulo con el texto "Página con includes".

Después utilizamos la función include("encabezado.php") para insertar el contenido del archivo de cabecera.

En encabezado.php utilizamos la variable $titulo para mostrar el título de la página.

A continuación, en index.php, mostramos el título mediante:

<?= $titulo ?>

Finalmente utilizamos include("pie.html") para insertar el contenido del pie de página.

4. Configuración de Docker

Hemos utilizado Docker Compose para crear un entorno de desarrollo con PHP 8.3, Nginx y Xdebug.

Para iniciar el servidor ejecutamos:

docker compose up -d

Para acceder a la página web utilizamos:

http://localhost:8080

Para detener el servidor ejecutamos:

docker compose down

5. Resultado de la práctica

La página funciona correctamente y muestra el título "Página con includes" y el texto "Pie de Página".