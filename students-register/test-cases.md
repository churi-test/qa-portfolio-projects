## Casos de Prueba Manuales - Diseñados

**Fecha**: Agosto 2026  **Autor**: Jhon Churivanti Alva   **Web para prueba**: [Playground CSH](https://playground.calidadsinhumo.com/registro)

---
## Resumen

| **Técnica** / prueba | **Casos** |
|--------|------|
| Partición de equivalencia   | 2  |
| Valores límite  | 3  |
| Tabla de decisión | 7  |
| Funcional  | 1  |

Total de pruebas diseñados: 13
> `Nota: A continuación puede observar algunos ejemplos. Pero, puede visualizar por completo los 13 casos diseñados de manera detallada más las técnicas aplicadas, aquí ->` [ test-cases](https://docs.google.com/spreadsheets/d/1-xA_HidvMXRWbK-z-qoKIwq2oTDCwvIAYQSCSvt1cfk/edit?usp=sharing)

---
## Módulo 1 — Registro de estudiante

### CPR01 · Registro de nuevo estudiante con formato de email válido

| **Campo** | **Detalle** |
|--------|------|
| **IDs Riesgo** | R-02 |
| **Precondición**   | - Conexión a internet estable - Se accede al formulario del sistema: https://playground.calidadsinhumo.com/registro - El usuario no tenga una cuenta registrada  |
| **Pasos**  | 1. Llenar cada campo del formulario con los datos de la prueba. 2. Presionar el botón "Crear cuenta".  |
| **Resultado esperado** | Se espera que el sistema registre el nuevo estudiante de forma exitosa, muestre el mensaje de “¡Registro exitoso! Tu cuenta ha sido creada."  |


---
### CPR13 · Verificar que tras un registro exitoso, se limpie cada campo del formulario

| **Campo** | **Detalle** |
|--------|------|
| **IDs Riesgo** | R-03 |
| **Precondición**   | - Conexión a internet estable - Se accede al formulario del sistema: https://playground.calidadsinhumo.com/registro - El usuario no tenga una cuenta registrada  |
| **Pasos**  | 1. Llenar cada campo del formulario con los datos de la prueba. 2. Presionar el botón "Crear cuenta".  |
| **Resultado esperado** | - Se espera que el sistema tras el mensaje de registro exitoso, limpie cada campo del formulario: nombre completo, email, contraseña, edad.  |

---
QA Portfolio — Jhon Churivanti






