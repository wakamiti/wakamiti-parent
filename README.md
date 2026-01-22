
# wakamiti-parent

Este POM está diseñado para ser utilizado por todos los componentes de Wakamiti, proporcionando una configuración 
centralizada del proceso de construcción y propiedades globales como la organización, licencias y versiones. 
Su objetivo es garantizar consistencia y facilitar la gestión del proyecto.

## Propósito

- **Centralización de versiones**: Administra versiones de dependencias y plugins comunes para todos los módulos.
- **Configuraciones estándar**: Define estándares para compilación, pruebas (unitarias con Surefire e integración 
  con Failsafe), y generación de reportes de cobertura (JaCoCo).
- **Soporte para despliegues**: Incluye perfiles para publicar artefactos en repositorios como Sonatype y GitHub 
  Packages.

## Uso
Para heredar este POM parent en un módulo, agrega lo siguiente a tu pom.xml:
```xml
<parent>
    <groupId>es.wakamiti</groupId>
    <artifactId>wakamiti-parent</artifactId>
    <version>1.0.0-SNAPSHOT</version>
</parent>
```

## Perfiles
- `check-updates`: Ejecuta `mvnw -Pcheck-updates` para mostrar actualizaciones disponibles de dependencias, plugins, 
  propiedades y parent POM.
- `sonatype`: Ejecuta `mvnw deploy -Psonatype` para preparar artefactos para despliegue en Sonatype.
- `jlink`: Ejecuta `mvnw initialize -Pjlink` para crear una imagen JRI personalizada.

## Contribuciones
Para proponer cambios o añadir configuraciones comunes, contacta al equipo de desarrollo o sigue el proceso de 
revisión en el repositorio de GitHub (https://github.com/wakamiti/wakamiti-parent).
