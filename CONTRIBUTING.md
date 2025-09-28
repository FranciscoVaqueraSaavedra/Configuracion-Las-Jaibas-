# Contribuciones al directorio config/

Gracias por contribuir a la calidad de la configuración del proyecto.  
Sigue estas reglas para mantener consistencia y evitar errores.

---

## 1. Flujo de trabajo

1. **Crea una rama** a partir de `main` con el prefijo `config/`  
   Ejemplo: `config/feat/enable-new-ui-staging`  
2. **Haz tus cambios** en los archivos de `config/` respetando el formato y las convenciones.  
3. **Ejecuta validación de sintaxis** con un linter (`jsonlint` o `yamllint`).  
4. **Abre un Pull Request (PR)** con:  
   - Título claro: `[config:<entorno>] descripción breve`  
   - Ejemplo: `[config:staging] Enable new UI flag`  

---

## 2. Revisión

- Al menos **un compañero distinto** debe revisar y aprobar el PR.  
- Verifica:  
  - Sintaxis válida (linter pasa sin errores).  
  - Convenciones de nomenclatura respetadas.  
  - No se incluyen credenciales reales.  

---

## 3. Merge

- Solo se hace **merge** tras la aprobación.  
- Usa la opción **Squash and merge** para mantener el historial limpio.  

---

## 4. Notas de calidad

- Nunca subir **secretos reales** (contraseñas, API keys).  
- Documenta cualquier parámetro nuevo en `README.md`.  
- Mantén los nombres y unidades consistentes entre entornos.
