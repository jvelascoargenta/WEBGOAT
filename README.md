# WEBGOAT

DevSecOps

La aplicación web-app elegida por nuestro grupo de trabajo es la llamada Webgoat, esta aplicación es un honeypot, es básicamente una maquina totalmente vulnerable en la que se puedan realizar ataques como Metasploitable.

¿Cómo podemos implementar o usar esta aplicación para hacer honor a la filosofía DevSecOps? Una de las claves para promover este modo de desarrollo seguro de nuestras aplicaciones futuras, es fomentar una cultura en la que todos nuestros miembros de nuestro equipo tomen conciencia sobre los riegos que trae un diseño débil y las consecuencias que traería si esta es atacada con éxito.

Que mejor manera de inducir al desarrollo seguro de nuestro proyectos, es creando una aplicación totalmente vulnerable para que los miembros de nuestro equipo puedan ver, lo fácil que es atacar con éxito una máquina. Un ejemplo de esta filosofía es HackTheBox, esta página web en la que se alojan una gran variedad de máquinas vulnerables de todos los niveles, te enseña a tomar conciencia de lo fácil que es vulnerar páginas web . Existen muchas páginas web en la actualidad que no han sido desarrolladas con el pensamiento de un potencial ataque de un persona ajena a la empresa con la malas intenciones.

Una de las primeras máquinas que ataque y que vulnere con facilidad fue, iniciando cesión en dicha maquina con usuario ‘admin‘y contraseña ‘admin’. Conseguí tomar el control de esa página web, aunque parezca absurdo, compañías como Orange, han sufrido un ataques similares, hace poco un administrador de Orange, este administrador tenía una contraseña bastante débil, esta ataque afecto a muchos clientes y se podría haber evitado, si este empleado hubiera tomado las medidas y hubiera seguido la filosofía DevSecOps.
En nuestra opinión es el punto más fuerte de esta filosofa y que hay hincapié, es la conciencia de la Ciberseguridad en todos sus aspectos, organizaciones europeas como ENISA y en España INCIBE , están constantemente impulsando la culturar de la Ciberseguridad a todos los niveles como expertos en la materia y menos experimentados .

Aunque en la actividad se pide que demostremos como podríamos implementar DevSecOps en esta aplicación, podríamos tomarnos esta aplicación como un paso previo en la creación de nuestros siguientes proyectos, ayudaría mucho a la identificación de riesgos y nuestros desarrolladores los tendrían en cuenta el momento de desarrollo de los futuros proyectos. Como hemos comentado el login de una web-app es uno de los primeros potenciales ataques que se tendrían que tener en cuenta, también inyecciones SQL, subida de archivos, tener un cifrado de extremo a extremo, comentarios que se dejan en el parte de HTML. Todos estos errores que hemos encontrado, nos ayudara a familiarizarnos con los 10 principales riesgos de seguridad de las aplicaciones web. Todo este proceso ayudaría a los desarrolladores a empezar tener una pequeña experiencia
en las prácticas de seguridad pero también durante el desarrollo de nuestra aplicación debemos contar con herramientas como Jenkins, usando este software estaríamos incorporando la estrategia integración continua/entrega (CI/CD) parte fundamental en la filosofía DevSecOps.

Otro momento importante, es el después de realizar el lanzamiento de nuestro proyecto, en esta etapa tenemos que monitorizar el comportamiento de nuestra web-app, como por ejemplo las veces que un usuario intenta entrar a una cuenta (fuerza bruta) o el flujo de peticiones (cantidad de peticiones) .Para analizar el comportamiento de nuestra web-app podemos usar Google Analytics o New Relic. También podríamos hacer pruebas de penetración cada cierto tiempo, usando Nmap, Burpsuite, Metasploit….Cuantas más herramientas usemos aunque tengan la misma función como por ejemplo Dirbuster y Gobuster, estas herramientas de seguridad cumplen la misma función pero hay veces que dan un resultado distinto.

**En el caso del diagrama las etapas de concienciación y formación se quedan fueran, no les he encontrado sito en alguna etapa de S-SDLC. 

La primera etapa es la más temprana y es la fase en la que se intenta recabar y crear un diseño seguro teniendo en cuenta todos los potenciales vulnerabilidades que pueda tener nuestra aplicación.

La segunda etapa es la de corregir el código tanto de forma manual y uso de software externos que analicen el código.

La tercera etapa es la de monitorizar nuestro proyecto, corregir todos los errores que encontremos y por ultimo actualizar nuestra web-app en todos los sentidos para que sea más segura , cuanto más tiempo sin actualizar este la página es más probable que existan y se hayan descubierto vulnerabilidades (librerías , Framework) .


S-SDLC

Paso 1: Requisitos
Objetivo: Definir qué aspectos de la seguridad informática quieres enseñar.

 Identificar Necesidades: Decidir que vulnerabilidades y ataques se quieren incluir (por ejemplo, inyección SQL, XSS, CSRF).
 Especificación de Requisitos: Documentar cada requisito de seguridad y funcionamiento.

Paso 2: Diseño
Objetivo: Diseñar la arquitectura de la aplicación y cómo cada módulo interactuará.

 Diseño de Arquitectura: Crear diagramas que muestren los componentes de laaplicación y sus interacciones.
 Revisión de Seguridad: Realizar una revisión de seguridad del diseño para asegurar quese introduzcan controles adecuados para las áreas vulnerables.

Paso 3: Desarrollo
Objetivo: Codificar la aplicación siguiendo buenas prácticas de programación segura.

 Entorno de Desarrollo Seguro: Configurar un entorno de desarrollo que minimice riesgos de seguridad en el código.
 Codificación: Desarrollar módulos según las especificaciones. Utilizar comentarios y seguir las guías de estilo de codificación para mantener el código legible y mantenible.

Paso 4: Pruebas
Objetivo: Verificar tanto la funcionalidad como la seguridad de la aplicación.

 Pruebas Unitarias y de Integración: Escribir y ejecutar pruebas para cada módulo y sus interacciones.
 Pruebas de Penetración: Simular ataques contra la aplicación para verificar la efectividad de las medidas de seguridad.
 Revisión de Código: Organizar revisiones de código entre pares para buscar vulnerabilidades de seguridad en el código.

Paso 5: Implementación
Objetivo: Lanzar la aplicación en un entorno controlado.

 Despliegue Seguro: Asegurar que el entorno de producción esté configurado correctamente para minimizar los riesgos.
 Capacitación de Usuarios: Preparar documentación y tutoriales para que los usuarios entiendan cómo usar la aplicación y explorar las vulnerabilidades.

Paso 6: Mantenimiento
Objetivo: Mantener la aplicación actualizada y segura frente a nuevas vulnerabilidades.

 Monitoreo: Vigilar la aparición de nuevos ataques o vulnerabilidades que podrían afectar a la aplicación.
 Parches y Actualizaciones: Implementar mejoras y correcciones de forma regular para mantener la seguridad de la aplicación.

Paso 7: Retirada
Objetivo: Finalizar el uso de la aplicación de manera segura cuando ya no sea necesaria.

 Plan de Retirada: Definir un proceso para descontinuar la aplicación de forma segura, asegurando que todos los datos y recursos sean adecuadamente eliminados o archivados.

Documentación y Retroalimentación
A lo largo de todo el S-SDLC, es crucial documentar cada paso, decisión y cambio. Además, recoger feedback tanto de usuarios como de expertos en seguridad puede proporcionar insights valiosos para mejorar la aplicación.

DEVSECOPS

Paso 1: Planificación y Diseño
Objetivo: Incorporar la seguridad como un componente fundamental desde el principio.

 Evaluación de Riesgos: Realizar una evaluación de riesgos temprana para identificar posibles amenazas y vulnerabilidades.
 Requisitos de Seguridad: Definir los requisitos de seguridad que deben integrarse en la aplicación.
 Diseño de Infraestructura: Planear una infraestructura que soporte prácticas de seguridad, como la segmentación de la red y el cifrado.

Paso 2: Integración y Desarrollo Continuo
Objetivo: Integrar la seguridad en el desarrollo diario y la integración continua.

 Entorno de Desarrollo Seguro: Utilizar contenedores y otras tecnologías de aislamiento para crear entornos de desarrollo seguros y reproducibles.
 Codificación Segura: Fomentar prácticas de codificación segura mediante la formación y el uso de herramientas de análisis estático de código fuente (SAST) que se ejecutan en cada commit.
 Integración Continua (CI): Configurar pipelines de CI para automatizar las pruebas de seguridad, como análisis de dependencias y pruebas dinámicas (DAST).

Paso 3: Despliegue y Entrega Continuos
Objetivo: Automatizar el despliegue seguro de aplicaciones.

 Infraestructura como Código (IaC): Utilizar IaC para gestionar la infraestructura de manera consistente y segura.
 Entrega Continua (CD): Implementar pipelines de CD que incorporen pasos de aprobación automática y manual para garantizar la seguridad antes del despliegue.
 Pruebas de Seguridad en el Despliegue: Automatizar las pruebas de penetración y las evaluaciones de configuración como parte del proceso de despliegue.

Paso 4: Operación y Monitoreo
Objetivo: Operar y monitorear la aplicación para detectar y responder a incidentes de seguridad.

 Monitoreo Continuo: Implementar herramientas de monitoreo en tiempo real para detectar actividades sospechosas y vulnerabilidades.
 Respuesta a Incidentes: Desarrollar un plan de respuesta a incidentes que pueda ejecutarse automáticamente en ciertos escenarios y que sea fácilmente accesible para el equipo de operaciones.
 Retroalimentación y Aprendizaje: Utilizar los datos recopilados durante el monitoreo para mejorar continuamente las prácticas de seguridad.

Paso 5: Retroalimentación y Mejora Continua
Objetivo: Utilizar la retroalimentación para mejorar continuamente las prácticas de seguridad.
 Revisión Continua: Realizar auditorías de seguridad regulares y revisa las prácticas y herramientas actuales.
 Integración de Nuevas Tecnologías: Evaluar y adoptar nuevas tecnologías y métodos para mejorar la seguridad y la eficiencia del desarrollo.
 Capacitación y Concienciación: Fomentar una cultura de seguridad mediante la formación continua y la sensibilización sobre las mejores prácticas de seguridad.

DISCUSIÓN DEL PROGRAMA WEBGOAT
WebGoat es una aplicación desarrollada por OWASP diseñada para enseñar a desarrolladores y profesionales de seguridad sobre vulnerabilidades en aplicaciones web mediante un entorno educativo interactivo y práctico. Esta herramienta, que incluye una amplia gama de lecciones sobre fallos de seguridad comunes como inyección SQL y XSS, es ideal para formación corporativa y educación superior, ofreciendo un recurso gratuito y abierto para mejorar la conciencia de seguridad y la habilidad en programación segura. Sin embargo, WebGoat debe usarse exclusivamente en entornos de prueba, ya que está intencionadamente llena de fallos de seguridad y requiere actualizaciones constantes para mantenerse relevante ante nuevas técnicas de explotación.


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


