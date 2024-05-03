# WEBGOAT
ENUNCIADO DE MI PARTE.
2. 

a. Definición de la aplicación y cómo ejecutarla. – Por favor, incluir un apartado en donde se especifiquen los miembros del grupo junto al enlace del repositorio usado en la actividad anterior.
b. Consideraciones de seguridad hechas durante el diseño de la aplicación.

Documentación de la Aplicación WebGoat.


1. Definición de la Aplicación.
WebGoat es una aplicación web de código abierto diseñada para enseñar a los desarrolladores de software sobre las vulnerabilidades comunes de seguridad en las aplicaciones web. Proporciona una plataforma segura para que los desarrolladores practiquen y aprendan sobre técnicas de explotación, al mismo tiempo que ofrece consejos sobre cómo mitigar estos riesgos en aplicaciones reales.

2. ¿Cómo ejecutaríamos la Aplicación?
Requisitos Previos:
Tener instalado Java Development Kit (JDK) en nuestro sistema.
Descargar el archivo WAR de la última versión de WebGoat desde el sitio oficial.

Pasos para la ejecución de la Aplicación:
Después de descargar el archivo WAR, navegamos hasta el directorio donde lo hayamos guardado.
Abrimos una terminal o línea de comandos en ese directorio.
Ejecutamos el siguiente comando para iniciar WebGoat:
php
Copy code
java -jar webgoat-server-<version>.war
Sustituímos <version> por la versión específica del archivo WAR que descargamos.
Una vez que WebGoat se haya iniciado correctamente, abrimos un navegador web y visitamos la dirección: http://localhost:8080/WebGoat.

Cómo en nuestro caso está hecha.

Ejecutaamos usando Docker:

Ya tenemos un navegador y ZAP y/o Burp instalados en nuestra máquina, en este caso podemos ejecutar la imagen de WebGoat directamente usando Docker.

Cada versión también se publica en DockerHub.

docker run -it -p 127.0.0.1:8080:8080 -p 127.0.0.1:9090:9090 webgoat/webgoat
Si queremos reutilizar el contenedor, le damos un nombre:

docker run --name webgoat -it -p 127.0.0.1:8080:8080 -p 127.0.0.1:9090:9090 webgoat/webgoat
Mientras no eliminemos el contenedor podemos usar

docker start webgoat

De esta forma, podemos empezar donde lo dejamos. Si eliminamos el contenedor, necesitamos usar docker run de nuevo.


docker run -p 127.0.0.1:3000:3000 webgoat/webgoat-desktop


4. Miembros del Grupo
José Luis Díaz Heredia
Carlos Jhasmany Sayago Torrico
Jorge Velasco Argenta


5. Consideraciones de Seguridad
Durante el diseño de WebGoat, se han tenido en cuenta diversas consideraciones de seguridad para garantizar que la aplicación sea utilizada de manera segura y responsable. Algunas de estas consideraciones incluyen:

Aislamiento del Entorno: WebGoat se ejecuta en un entorno controlado y aislado, lo que significa que las prácticas de hacking y los ataques lanzados dentro de la aplicación no afectarán a otros sistemas externos. Esto ayuda a prevenir posibles daños colaterales y garantiza que los usuarios puedan practicar de manera segura sin riesgo para otros sistemas.

Autenticación Segura: La aplicación utiliza un sistema de autenticación robusto para proteger el acceso a las lecciones y funcionalidades administrativas. Los usuarios deben autenticarse con credenciales válidas antes de poder acceder al contenido protegido, lo que ayuda a prevenir el acceso no autorizado.

Control de Acceso: Se implementan controles de acceso granulares para garantizar que los usuarios solo puedan acceder a las lecciones y contenido para los que están autorizados. Esto ayuda a proteger la confidencialidad y la integridad de los datos sensibles, evitando que los usuarios accedan a información a la que no deberían tener acceso.

Sanitización de Entradas: Se aplican medidas de sanitización de datos en toda la aplicación para prevenir ataques de inyección de código y otros vectores de ataque comunes. Esto incluye la validación de entradas de usuario, la utilización de parámetros seguros en consultas de bases de datos y la prevención de la ejecución de scripts maliciosos en páginas web.

Registro y Monitoreo: Se registran y monitorean las actividades de los usuarios dentro de la aplicación para detectar comportamientos sospechosos y posibles intentos de explotación. Esto ayuda a identificar y responder rápidamente a posibles amenazas de seguridad, así como a mejorar continuamente las medidas de seguridad de la aplicación.

Actualizaciones y Parches: Se realizan actualizaciones regulares y se aplican parches de seguridad para corregir vulnerabilidades conocidas y mejorar la resistencia de la aplicación frente a posibles ataques. Es importante mantener la aplicación actualizada para garantizar que se beneficie de las últimas correcciones de seguridad disponibles.
Estas consideraciones de seguridad son fundamentales para asegurar que WebGoat proporcione un entorno de aprendizaje seguro y efectivo para los desarrolladores que deseen aprender sobre vulnerabilidades comunes en aplicaciones web y cómo mitigar estos riesgos en aplicaciones reales.


