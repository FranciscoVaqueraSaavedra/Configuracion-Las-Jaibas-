# Guía para Proponer y Revisar Cambios de Configuración

## 1. Cómo proponer cambios

-   Crear una nueva rama con el formato:

        config/<descripcion>

-   Realizar los cambios necesarios en dicha rama.

-   Abrir un **Pull Request** hacia la rama principal del repositorio.

## 2. Quién revisa

-   Todo Pull Request debe ser revisado por **al menos un compañero
    distinto** al autor de los cambios.
-   El revisor debe verificar tanto la corrección técnica como la
    claridad de la propuesta.

## 3. Comprobaciones automáticas mínimas

Antes de poder aprobar un Pull Request, deben cumplirse al menos las
siguientes validaciones automáticas: - **Validación de sintaxis JSON**
con un linter. - **Validación de sintaxis YAML** con un linter. -
(Opcional) Ejecución de pruebas adicionales definidas en el proyecto.

------------------------------------------------------------------------

✅ Con este flujo se garantiza calidad y consistencia en la
configuración del repositorio.
