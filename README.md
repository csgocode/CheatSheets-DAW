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
