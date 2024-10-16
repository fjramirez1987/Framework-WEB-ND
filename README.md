# Changelog

## v1.3 - 2024-10-12
### Nuevas características:
- Añadido soporte para **middleware personalizados**, permitiendo a los desarrolladores agregar lógica antes y después del manejo de las solicitudes.
- Implementada **carga automática de clases con PSR-4**, simplificando la estructura de directorios y mejorando la autocompletar en IDEs.
- Nuevo **sistema de enrutamiento dinámico** con soporte para expresiones regulares en las rutas.
- Soporte nativo para **APIs REST** con métodos simplificados para la creación de endpoints.
- Añadido un **comando de consola** para generar controladores, modelos y middleware automáticamente.

### Mejoras:
- Se optimizó el sistema de caché para mejorar el rendimiento general de la aplicación.
- Refactorización del núcleo del framework para reducir la cantidad de dependencias externas.
- Mejorada la documentación con ejemplos más claros y completos sobre la autenticación y autorización.

### Corrección de errores:
- Corregido un bug que causaba un mal manejo de las variables globales en solicitudes concurrentes.
- Solucionado un problema donde algunas excepciones no se registraban en el log correctamente.
- Corregidos errores menores en la validación de formularios y la sanitización de entradas.
- Corrección de **error grave de seguridad**. El proceso de backups genera el archivo temporal /tmp.zip en un directorio público.

---

## v1.2 - 2024-08-15
### Nuevas características:
- Añadido soporte para **sistema de plantillas basado en Blade**, permitiendo un uso más eficiente de layouts y secciones reutilizables.
- Introducción de **controladores REST** para simplificar la creación de APIs.
- Sistema de **validación de formularios** más robusto con reglas personalizadas y mensajes de error configurables.

### Mejoras:
- Mejora en la **gestión de sesiones**, añadiendo soporte para sesiones distribuidas y almacenamiento en Redis.
- Optimización de la carga de archivos estáticos con mejor manejo de cabeceras `Cache-Control`.
- Documentación ampliada con ejemplos para la integración con bases de datos no relacionales.

### Corrección de errores:
- Corregido un error en el sistema de rutas que fallaba al manejar rutas anidadas con parámetros opcionales.
- Solucionado un problema con el manejador de excepciones que no capturaba correctamente las excepciones personalizadas.

---

## v1.1 - 2023-06-10
### Nuevas características:
- Añadida funcionalidad de **enrutamiento por grupos** con prefijos, permitiendo una organización más clara de rutas similares.
- Introducción de un **sistema de migraciones de base de datos**, facilitando las actualizaciones del esquema de forma segura.
- Implementación de **controladores de recursos** con métodos predeterminados (index, show, create, update, delete).

### Mejoras:
- Optimización en el manejo de **errores y excepciones**, añadiendo un sistema de logs mejorado.
- Mejorado el rendimiento del **sistema de plantillas** al reducir el tiempo de compilación de vistas.
- Refactorización del manejo de configuraciones para soportar **entornos múltiples** (producción, desarrollo, etc.).

### Corrección de errores:
- Corregido un bug en la conexión a bases de datos que causaba problemas intermitentes en configuraciones con múltiples conexiones.
- Arreglado un problema que causaba que las rutas definidas sin método explícito fallaran en solicitudes `POST`.

---

## v1.0 - 2022-04-01
### Lanzamiento inicial del framework:
- Sistema de **enrutamiento sencillo** basado en controladores y funciones de callback.
- Soporte para **MVC (Modelo-Vista-Controlador)**.
- Integración con **PDO** para manejo seguro de bases de datos.
- Soporte básico para **sesiones** y **autenticación**.
- Motor de vistas simple con soporte para plantillas básicas.
- Soporte para **controladores** y **modelos** con generación automática de CRUD.
