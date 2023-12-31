# Servidores de Aplicaciones - CheatSheet

## Introducción
Un servidor de aplicaciones es una plataforma de software diseñada para crear y servir aplicaciones web, actuando como intermediario entre el servidor web y la base de datos.

## Características Principales
- **Intermediario**: Entre el servidor web y la base de datos.
- **Multifuncional**: Admite aplicaciones en la nube y basadas en la web.
- **Versátil**: Puede contener su propio servidor web.
- **Tareas Adicionales**: Incluye procesamiento de transacciones, mensajería, administración de recursos, conexiones y seguridad.

## Servidor de Aplicaciones
- **Función**: Soporta múltiples aplicaciones web y en la nube.
- **Ubicación**: Entre servidores de bases de datos y servidores web.
- **Capacidades Especiales**: Procesamiento de solicitudes de servlets (Java), seguridad avanzada, transacciones, servicios, clustering, diagnósticos.

## Terminología Clave
| Término        | Descripción                                                  |
|----------------|--------------------------------------------------------------|
| Servidor web   | Almacena, procesa y entrega datos de páginas web.            |
| Cliente web    | Usuario final que accede a recursos web o de aplicación.     |
| HTTPS          | Protocolo de comunicación seguro.                            |
| JSON           | Lenguaje de intercambio de datos entre servidores.           |
| Lógica de negocio | Reglas para almacenamiento y transferencia de datos.      |
| Aplicación     | Programa o sitio web conectado a una base de datos.          |

## Papel en la Arquitectura de Servicios
- **Procesamiento Backend**: Maneja solicitudes dinámicas de aplicaciones.
- **Optimización de Tráfico y Seguridad**: Añade una capa adicional de seguridad y eficiencia.

## Comparación: Servidor de Aplicaciones vs. Servidor Web
| Servidor de Aplicaciones | Servidor Web                     |
|--------------------------|----------------------------------|
| Sirve peticiones HTTP y de lógica de negocio | Sirve peticiones HTTP de contenido web estático |
| Almacena y proporciona lógica de negocio | Gestiona contenido web estático |
| Uso de recursos más intensivo | Uso de recursos más ligero |
| Soporta transacciones distribuidas y EJB | Soporta Servlets, JSP y JSON |

## Tendencias 2020-2026
- **Crecimiento**: Se espera un CAGR del 13.2%, de 17 mil millones a 41 mil millones de dólares.
- **Impulsores**: Migración a la nube, IoT, políticas BYOD, fuerza laboral remota.

## Despliegue de Aplicaciones Web
### ¿Qué es?
El despliegue implica pasar cambios o actualizaciones de un entorno a otro, como de desarrollo a producción.

### Proceso de Despliegue
1. **Planificación**
2. **Desarrollo**
3. **Pruebas**
4. **Despliegue**
5. **Supervisión**

### Tipos de Despliegue
- **Metadatos**: Cambios en código, plantillas, hojas de estilo.
- **Contenidos**: Texto, imágenes, vídeos.

### Mejores Prácticas
- Utilizar Git y trabajar en ramas.
- Revisar diferencias antes del despliegue en producción.
- Considerar permisos de usuario diferenciados.
- Planificar el momento del despliegue.

## Ventajas del Despliegue en Múltiples Entornos
- **Reducción de Riesgos**: Menor probabilidad de romper el sitio en producción.
- **Ahorro de Tiempo**: Optimización del flujo de trabajo.
- **Gestión de Contenido Sensible al Tiempo**: Facilita campañas y lanzamientos programados.

## Aplicaciones Java en Servidores

### Introducción
En los apartados anteriores, hemos explorado qué es un servidor de aplicaciones y un despliegue de aplicaciones web en términos generales. Ahora, nos enfocaremos en un caso específico: las aplicaciones Java.

En el lado del servidor, necesitamos que nuestro servidor HTTP sea capaz de ejecutar programas de aplicación que recojan parámetros de peticiones del cliente, los procesen y devuelvan al servidor un documento que, a su vez, será pasado al cliente.

### Funcionamiento
Para el cliente, el servidor no habrá hecho nada distinto a lo estipulado en el protocolo HTTP. Sin embargo, el servidor puede utilizar herramientas externas para procesar y servir la petición solicitada, permitiendo no solo servir páginas estáticas sino también documentos con contenido dinámico a través de otras aplicaciones como servlets y JSP.

Los programas de aplicación suelen realizar tareas como consultas a bases de datos, procesamiento de la información resultante y devolución de la salida al servidor.

### Enfoque en JavaEE
Nos centraremos en las aplicaciones web JavaEE, donde los componentes dinámicos que recibirán las peticiones HTTP en el servidor serán los servlets y JSPs. Estos componentes pueden analizar la petición y utilizar otros componentes Java para realizar las acciones necesarias (beans, EJBs, etc).

## Estructura de una Aplicación Java

### Organización de Archivos
- **Directorio Raíz**: Contiene páginas HTML o JSP. Puede subdividirse en directorios.
- **Directorio WEB-INF**: Ubicado dentro del directorio inicial, contiene información Web relevante para la aplicación.
- **Otros Elementos**: Como imágenes, se pueden estructurar según convenga.

### Despliegue
Esta estructura se coloca dentro de un directorio correspondiente a la aplicación Web en el servidor. Cualquier servidor Web JavaEE soporta esta estructura, permitiendo su fácil copia y despliegue.

### Contexto de la Aplicación
Cada aplicación web JavaEE es un contexto, una unidad que comprende un conjunto de recursos y clases Java junto con su configuración.

## Empaquetamiento y Despliegue

### Empaquetamiento en WAR
Las aplicaciones Web pueden empaquetarse en un archivo WAR, similar a un TAR o JAR, utilizando la herramienta JAR. Estos archivos WAR son un estándar en JavaEE y pueden utilizarse en diferentes servidores de aplicaciones JavaEE.

### Despliegue de Archivos WAR
Los archivos WAR se utilizan para distribuir los contenidos de las aplicaciones Web en tecnología JEE. El proceso de despliegue puede variar según el servidor, pero generalmente se realiza a través de una consola de administración o colocando el archivo en un directorio específico.

## Maven: Herramienta de Automatización

### Introducción a Maven
Maven es una herramienta open-source creada en 2001 para simplificar los procesos de build. Facilita la compilación y generación de ejecutables a partir del código fuente, gestionando dependencias y automatizando tareas.

### Funcionalidades de Maven
- **Build Automatizado**: Ejecutando `mvn install`.
- **Gestión de Dependencias**: A través del archivo POM (Project Object Module).
- **Ciclos de Build**: Incluye etapas como validación, compilación, pruebas, empaquetado, entre otras.

### Estructura de Proyectos
Maven establece una estructura común de directorios para todos los proyectos, facilitando la organización y el desarrollo.

## Despliegue de Aplicaciones Node.js con Express

### ¿Qué es Node.js?
Node.js es un entorno de ejecución de JavaScript para construir aplicaciones del lado del servidor. No es un lenguaje de programación ni un framework, sino un entorno para ellos.

### Express JS
Express JS es un framework de Node.js diseñado para construir aplicaciones web y API's de forma rápida, facilitando la gestión de archivos y peticiones HTTP.

### npm: Gestor de Paquetes
NPM es el gestor de paquetes por defecto para JavaScript, facilitando la compartición, instalación y gestión de paquetes y librerías.

### Archivo `package.json`
Define la información y configuración del proyecto, incluyendo dependencias, scripts y metadatos.

## CI/CD: Integración y Despliegue Continuos

### Introducción
CI/CD es un método para distribuir aplicaciones mediante la automatización en las etapas de desarrollo. Incluye prácticas como integración continua (CI), distribución continua (CD) y, en algunos casos, implementación continua.

### Procesos CI/CD
- **Integración Continua (CI)**: Incorporación y validación automáticas de cambios en el código.
- **Distribución Continua (CD)**: Automatización del traslado del código validado a un repositorio.
- **Implementación Continua**: Automatización del lanzamiento de aplicaciones a la producción.

# Instalación de Tomcat

## Introducción
Instalación del servidor de aplicaciones Apache Tomcat en su última versión disponible, considerando las diferencias entre versiones de Java y la importancia de la consistencia en las versiones de desarrollo y despliegue.

## Instalación de Java
1. Comprobar si Java está instalado:
   `java --version`
2. Si no está instalado, actualizar e instalar Java:
`sudo apt-get update && sudo apt-get upgrade`
`sudo apt-get install default-jdk`
`sudo apt-get install default-jre`

3. Volver a comprobar la versión de Java.

## Instalación de Apache Tomcat
1. Instalar Tomcat usando apt:
`sudo apt-get install -y tomcat10 tomcat10-admin`
2. Comprobar el estado de Tomcat:
`systemctl status tomcat10`
(Presionar `q` para volver al prompt.)
3. Verificar el acceso al servidor Tomcat a través de `http://IP_SERVIDOR:8080`.

## Gestión Gráfica de Tomcat y Creación de Usuario
1. Para gestionar Tomcat gráficamente, acceder a `http://IP_SERVIDOR:8080/manager`.
2. Crear un usuario de Tomcat modificando /etc/tomcat10/tomcat-users.xml:
`sudo vi /etc/tomcat10/tomcat-users.xml`

## Añadir las siguientes líneas antes del cierre </tomcat-users>:
   `<role rolename="manager-gui"/>
   <role rolename="admin-gui"/>
   <user username="admin" password="ieselcaminas" roles="admin-gui,manager-gui"/>`

3. Reiniciar Tomcat:
   `sudo systemctl restart tomcat10`
4. Comprobar el estado de Tomcat:
   `sudo systemctl status tomcat10`
5. Acceder a `http://IP_SERVIDOR:8080/manager` y `http://IP_SERVIDOR:8080/host-manager` con el usuario y contraseña creados.


### Despliegue Manual en Tomcat
1. **Acceso al Gestor de Aplicaciones Web**: 
   - Acceder a la interfaz web de Tomcat usando `http://IP_SERVIDOR:8080/manager/html`.
   - Autenticarse con las credenciales configuradas.

2. **Despliegue de la Aplicación**:
   - En la sección "WAR file to deploy", seleccionar el archivo `.war` de la aplicación.
   - Hacer clic en "Deploy" para iniciar el despliegue.

3. **Verificación**:
   - La aplicación desplegada aparecerá en la lista de aplicaciones en el gestor de Tomcat.
   - Acceder a la aplicación mediante `http://IP_SERVIDOR:8080/nombreAplicacion`.

### Comandos Útiles en Tomcat
- **Replegar**: Para desinstalar una aplicación.
- **Reiniciar**: Para reiniciar una aplicación y reflejar cambios.

## Uso de Maven para Gestión de Proyectos Java

### Instalación de Maven
`sudo apt-get update`
`sudo apt-get install maven`

## Verificación de la instalación
`mvn -v`

## Configuración de Usuario en Tomcat:
Añadir un usuario con el rol manager-script en tomcat-users.xml.
`xml <role rolename="admin-gui"/> <role rolename="manager-gui"/> <role rolename="manager-script"/> <user username="admin" password="ieselcaminas" roles="admin-gui,manager-gui"/> <user username="despliegues" password="ieselcaminas" roles="manager-script"/>`

## Configuración de Maven:
Editar settings.xml de Maven para añadir el servidor Tomcat.
Especificar el ID del servidor, usuario y contraseña.

## Clonar o Crear un Proyecto:
Para proyectos existentes, clonar el repositorio.
Para nuevos proyectos, usar `mvn archetype:generate`.

## Despliegue del Proyecto:
Ejecutar `mvn tomcat7:deploy` para desplegar el proyecto en Tomcat.
Comandos Maven para Gestión de Proyectos
Compilar Proyecto: `mvn compile`.
Empaquetar Proyecto: `mvn package`.
Ejecutar Tests: `mvn test`.
Limpiar Proyecto: `mvn clean`.
Instalar Proyecto en Repositorio Local: `mvn install`.

## Instalación de Node JS
# Actualizar e instalar dependencias necesarias
`sudo apt-get update`
`sudo apt-get install -y ca-certificates curl gnupg`

# Descargar e importar la clave GPG de Nodesource
`curl -fsSL https://deb.nodesource.com/gpgkey/nodesource-repo.gpg.key | sudo gpg --dearmor -o /etc/apt/keyrings/nodesource.gpg`

# Crear el repositorio deb para Node.js
NODE_MAJOR=20  # O cambiar por la versión deseada
echo "deb [signed-by=/etc/apt/keyrings/nodesource.gpg] https://deb.nodesource.com/node_$NODE_MAJOR.x nodistro main" | sudo tee /etc/apt/sources.list.d/nodesource.list

# Ejecutar la actualización e instalar Node.js
`sudo apt-get update`
`sudo apt-get install nodejs -y`

# Verificar la instalación de Node.js y npm
`node --version`
`npm --version`

# Instalar Express globalmente
`sudo npm install -g express`

# Actualizar npm si es necesario
`sudo npm install -g npm@<version>`

# Despliegue de una aplicación de terceros
`git clone <url_del_repositorio>`

# Acceder al directorio del proyecto clonado
`cd <nombre_del_directorio>`

# Instalar las dependencias del proyecto
`npm install`

# Iniciar la aplicación
`npm run start:dev`

# Despliegue de una Aplicación "Clusterizada" con Node Express

## Introducción
Optimización del rendimiento de aplicaciones Node.js mediante el uso de clusters para aprovechar múltiples núcleos de CPU.

## Instalación de Node.js y Express
`sudo apt-get update`
`sudo apt-get install -y nodejs npm`
`sudo npm install -g express`

## Uso de PM2 para Administrar Clusters
Instalar PM2 globalmente.
`sudo npm install pm2 -g`

## Iniciar la aplicación con PM2 en modo cluster.
`pm2 start pruebacluster.js -i 0`

## Comprobar el estado de los procesos.
`pm2 ls`

## Comandos Adicionales de PM2
Reiniciar, recargar, detener y eliminar aplicaciones.
`pm2 restart pruebacluster`
`pm2 reload pruebacluster`
`pm2 stop pruebacluster`
`pm2 delete pruebacluster`

## Monitorear logs y métricas.
`pm2 logs`
`pm2 monit`

## ¿Qué es Netlify?
Netlify es un proveedor de alojamiento en la nube para sitios web estáticos, ofreciendo servicios de backend sin servidor. Facilita el despliegue rápido de aplicaciones, conectándose a un repositorio de GitHub y pre-renderizando las páginas en archivos estáticos.

## Preparación del Entorno
Regístrate en Netlify con tu email y no enlaces tu cuenta de GitHub todavía.
Crea una instancia EC2 Debian en AWS Academy y conéctate vía SSH.
Instala GIT y Node.js.

## Opciones de Despliegue en Netlify
Despliegue Manual desde el CLI de Netlify:
Instala el CLI de Netlify: `sudo npm install netlify-cli -g`.
Autentícate con netlify login, generando un token de acceso.

## Despliegue desde un Repositorio de GitHub:
Clona el repositorio de ejemplo: `git clone https://github.com/StackAbuse/color-shades-generator`.
Instala dependencias con `npm install` y crea un build de producción con `npm run build`.
Despliega usando `netlify deploy` y luego `netlify deploy --prod`.

## Despliegue mediante Conexión con GitHub
Elimina el sitio previamente desplegado en Netlify.
Descarga y descomprime el código fuente del proyecto.
Crea un nuevo repositorio en GitHub y sube tu código.
Enlaza Netlify con tu repositorio de GitHub y despliega la aplicación.

## Despliegue de Aplicaciones Desarrolladas en Angular
Para aplicaciones Angular, la carpeta de build es `./dist/nombreaplicacion`. Para servir la aplicación desde tu servidor antes del despliegue en Netlify, usa `ng serve -o --host=IPPRIVADA` y accede a través de `http://IPPUBLICA:4200`.

## Despliegue de una Aplicación Flask en EC2 (Debian)

## Actualizar e Instalar pip
`sudo apt-get update && sudo apt-get upgrade`
`sudo apt-get install python3-pip`

## Instalar pipenv (Gestión de entornos virtuales)
`sudo apt-get install pipenv`
`pipenv --version`

## Configuración del Proyecto
`sudo mkdir /var/www/practica_flask`
`sudo chown -R $USER:www-data /var/www/practica_flask`
`chmod -R 775 /var/www/practica_flask/`

## Crear y Configurar Archivo .env
`cd /var/www/practica_flask`
`touch .env`
# Añadir en .env:
# FLASK_APP=wsgi.py
# FLASK_ENV=production

## Activar Entorno Virtual y Dependencias
`cd /var/www/practica_flask`
`pipenv shell`
`pipenv install flask gunicorn`

## Dentro del entorno virtual
`flask run --host=0.0.0.0`

## Probar Aplicación con Gunicorn
`gunicorn --workers 2 --bind 0.0.0.0:5000 wsgi:app`

## Configurar Gunicorn como Servicio
Crear `/etc/systemd/system/flaskapp.service`
Configurar el servicio con los detalles del proyecto
## Habilitar y Iniciar el Servicio de Gunicorn
`systemctl enable flask_app`
`systemctl start flask_app`

## Instalar y Configurar Nginx
`sudo apt-get install nginx`
`sudo systemctl start nginx`
`sudo systemctl status nginx`

## Configurar Sitio en Nginx
Crear `/etc/nginx/sites-available/practica_flask`
Configurar el archivo para el proxy a Gunicorn
Crear enlace simbólico en /etc/nginx/sites-enabled/

## Verificar y Reiniciar Nginx
`sudo nginx -t`
`sudo systemctl restart nginx`
