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
