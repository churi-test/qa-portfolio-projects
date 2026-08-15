## Casos de Prueba Manuales - Ejecutados

**Fecha de ejecución**: 3 Agosto 2026 | **Autor**: Jhon Churivanti Alva |  **Web para prueba**: [Playground CSH](https://playground.calidadsinhumo.com/registro)

---
## Resumen

| Módulo | Casos | Pasaron | Fallaron | Observado | Estado|
|--------|------|------|------|------|------|
| Registro de estudiante  | 13 | 9 | 3 | 1 | 3 Bugs encontrados + hallazgo  | 

Total de pruebas ejecutados manualmente: 13

**☑️ Visualizar por completo los casos ejecutados, gracias 👉** [test-execution](https://docs.google.com/spreadsheets/d/1GYnL0E37I-48pPcjotzRRlTaj2ImuuZL33p2o-ze9UA/edit?usp=sharing)

---
## Módulo 1 — Registro de estudiante

### CPR01 · Registro de nuevo estudiante con formato de email válido

| **Campo** | **Detalle** |
|--------|------|
| **IDs Riesgo** | R-02 |
| **Precondición**   | <ul><li>Conexión a internet estable</li> <li> Se accede al formulario del sistema: https://playground.calidadsinhumo.com/registro </li> <li> El usuario no tenga una cuenta registrada </li></ul>  |
| **Pasos**  | <ol><li>Llenar cada campo del formulario con los datos de la prueba. <li>Presionar el botón "Crear cuenta".</li></ol>  |
| **Resultado esperado** | Se espera que el sistema registre el nuevo estudiante de forma exitosa, muestre el mensaje de “¡Registro exitoso! Tu cuenta ha sido creada."  |
| **Datos de prueba** | <ul><li>Nombre: Juan</li> <li>Email: user@gmail.com</li> <li>Contraseña: 12345678 </li> <li>Edad: 16</li></ol>  |
| **Prioridad**  | Alta  |
| **Resultado obtenido**  | El sistema registra el nuevo estudiante y muestra el mensaje de "¡Registro exitoso! Tu cuenta ha sido creada."  |
| **Estado**  | Aprobado ☑️  |

---
### CPR13 · Verificar que tras un registro exitoso, se limpie cada campo del formulario

| **Campo** | **Detalle** |
|--------|------|
| **IDs Riesgo** | R-03 |
| **Precondición**   | <ul><li>Conexión a internet estable</li> <li> Se accede al formulario del sistema: https://playground.calidadsinhumo.com/registro </li> <li> El usuario no tenga una cuenta registrada </li></ul> |
| **Pasos**  | <ol><li>Llenar cada campo del formulario con los datos de la prueba.</li> <li>Presionar el botón "Crear cuenta".</li></ol>  |
| **Resultado esperado** | Se espera que el sistema tras el mensaje de registro exitoso, limpie cada campo del formulario: nombre completo, email, contraseña, edad.  |
| **Datos de prueba** | <ul><li>Nombre: Pedro</li> <li>Email: pedro@gmail.com</li> <li>Contraseña: 123456789 </li> <li>Edad: 16</li></ol>   |
| **Prioridad**  | Alta  |
| **Resultado obtenido**  | El sistema tras el mensaje de registro exitoso, no llegó a limpiar cada campo del formulario:, nombre completo, email, contraseña, edad  |
| **Estado**  | Fallido ❌  |
| **Evidencia**  | [Link(captura de pantalla)](https://drive.google.com/file/d/1koDuLDoG288_7xH2rEOtdcOhnvuAGRv6/view?usp=sharing)  |
| **IDs defecto**  | DEF-R03  |

---
QA Portfolio — Jhon Churivanti