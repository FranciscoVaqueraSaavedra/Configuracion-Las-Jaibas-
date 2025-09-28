# Configuración de la aplicación

Este directorio contiene los archivos de configuración para los distintos entornos del proyecto (`development`, `staging` y `production`).  
El objetivo es centralizar parámetros clave y que cualquier desarrollador nuevo entienda rápidamente qué cambia entre entornos.

---

## 1. Formato elegido y sintaxis

- **Formato**: **JSON (JavaScript Object Notation)**
- **Sintaxis**:
  - Pares clave–valor rodeados por llaves `{ }`.
  - Las claves y valores de tipo cadena se escriben entre comillas dobles `""`.
  - No se permiten comentarios en línea.
  - Arrays se definen con corchetes `[ ]`.
  - Tipos válidos: `string`, `number`, `boolean`, `array`, `object`, `null`.

**Ejemplo mínimo:**

```json
{
  "ENV": "development",
  "API_BASE_URL": "http://localhost:3000/api",
  "DB_PORT": 5432,
  "FEATURE_FLAGS": {
    "new_ui": true
  }
}
```

## 2. Descripción de cada parámetro

## 2. Descripción de cada parámetro

| **Parámetro**   | **Tipo** | **Descripción**                                                              |
| --------------- | -------- | ---------------------------------------------------------------------------- |
| `ENV`           | string   | Identifica el entorno de ejecución (`development`, `staging`, `production`). |
| `API_BASE_URL`  | string   | URL base para las peticiones de la API.                                      |
| `DB.HOST`       | string   | Dirección del servidor de base de datos.                                     |
| `DB.PORT`       | number   | Puerto de conexión a la base de datos.                                       |
| `DB.NAME`       | string   | Nombre de la base de datos a utilizar.                                       |
| `DB.USER`       | string   | Usuario de la base de datos _(ejemplo, no real)_.                            |
| `DB.PASSWORD`   | string   | Contraseña de la base de datos _(ejemplo, nunca subir secretos reales)_.     |
| `FEATURE_FLAGS` | object   | Conjunto de llaves booleanas para activar/desactivar funcionalidades.        |
| `new_ui`        | boolean  | Habilita la interfaz de usuario nueva.                                       |
| `beta_feature`  | boolean  | Activa una funcionalidad experimental en prueba.                             |

---

## 3. Convenciones de nomenclatura

- **Archivos**: un archivo por entorno (`development.json`, `staging.json`, `production.json`), en **kebab-case**.  
- **Claves principales**: **MAYÚSCULAS con snake_case** (`ENV`, `DB_HOST`, `API_BASE_URL`).  
- **Estructura anidada**: usar objetos por dominio (`DB.HOST`, `DB.PORT`) en lugar de nombres largos.  
- **Booleanos / feature flags**: nombre afirmativo con sufijo `*_enabled` o prefijo `enable_*` (`enable_new_ui`).  
- **Listas (arrays)**: siempre en plural (`allowed_origins`).  
- **Unidades y tiempos**: incluir sufijo claro (`*_MS`, `*_SECONDS`, `*_MB`).  
- **Valores sensibles**: nunca reales, usar marcadores (`replace_in_ci`).  
