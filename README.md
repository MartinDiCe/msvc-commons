
# Microservicio de Utilidades Comunes (msvc-commons)

`msvc-commons` es un microservicio que agrupa y centraliza funcionalidades comunes y utilitarias que son compartidas entre varios microservicios en la arquitectura. Este servicio permite evitar la duplicación de código y facilita el mantenimiento y la consistencia en los diferentes microservicios que lo utilizan.

## Funcionalidades Principales

- **Modelos Compartidos:** Definición de entidades comunes que son utilizadas por múltiples microservicios.
- **Utilidades:** Funciones y clases utilitarias como conversores, validadores, y mappers que pueden ser reutilizados.
- **Configuración Común:** Configuración compartida y valores predeterminados para diferentes microservicios.
- **Manejo de Excepciones:** Clases base para la gestión de excepciones que pueden ser extendidas y utilizadas en otros servicios.

## Tecnologías Utilizadas

- **Java** - Spring Boot
- **Spring WebFlux** - Para desarrollar aplicaciones reactivas.
- **Spring Security** - Para manejar seguridad y roles en aplicaciones Spring.
- **MongoDB** - Base de datos NoSQL usada en algunos modelos compartidos.
- **Lombok** - Para reducir el código boilerplate.
- **SpringDoc** - Para la documentación de la API, si es necesario exponer algún endpoint utilitario.

## Estructura del Proyecto

- **`src/main/java/com/diceprojects/msvccommons`**: Código fuente del microservicio.
    - **`models`**: Modelos compartidos y entidades comunes utilizadas por otros microservicios.
    - **`utils`**: Clases utilitarias, como validadores y funciones comunes.
    - **`mappers`**: Clases para mapear entidades a DTOs y viceversa.
    - **`exceptions`**: Clases para el manejo centralizado de excepciones.
    - **`config`**: Clases de configuración común para los microservicios que utilizan `msvc-commons`.
- **`src/test`**: Pruebas unitarias y de integración para las funcionalidades compartidas.

## Configuración

Este proyecto no tiene una configuración propia, ya que está destinado a ser utilizado como una dependencia por otros microservicios. Sin embargo, asegúrate de configurar adecuadamente los microservicios que utilicen `msvc-commons`.

## Uso

1. **Compilación y Publicación:**
    - Utiliza Maven o tu herramienta de construcción preferida para compilar y publicar este proyecto en tu repositorio local o remoto.
   ```bash
   mvn clean install
   mvn deploy
   ```
    - Los microservicios que dependen de `msvc-commons` deben incluirlo como una dependencia en su propio `pom.xml`.

## Contribuir

¡Contribuciones son bienvenidas! Si encuentras errores o tienes sugerencias para mejorar las utilidades y configuraciones comunes, abre un problema o envía una solicitud de extracción.

## Licencia

Este proyecto está bajo la Licencia MIT. Consulta el archivo `LICENSE.md` para más detalles.

## Dependencias

Este proyecto utiliza las siguientes dependencias principales:

- **Spring Boot Starter Data MongoDB Reactive** - Para las operaciones con MongoDB en modo reactivo.
- **Spring Boot Starter Security** - Para manejar seguridad y roles en aplicaciones Spring.
- **Spring Boot Starter WebFlux** - Para soporte de aplicaciones reactivas.
- **Lombok** - Para la reducción del código boilerplate.
- **SpringDoc OpenAPI WebFlux UI** - Para la documentación de API.

Las dependencias están definidas en el archivo `pom.xml` del proyecto.
