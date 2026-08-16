## Casos de Prueba Manuales - Diseñados

**Fecha**: Agosto 2026  | **Autor**: Jhon Churivanti Alva  | **Web para prueba**: [Playground CSH](https://playground.calidadsinhumo.com/registro)

---
## Resumen

| **Técnica** / prueba | **Casos** |
|--------|------|
| Partición de equivalencia   | 3  |
| Funcional + PE  | 1  |

Total de pruebas diseñadas: 4

**☑️ Visualizar por completo las pruebas diseñadas, gracias 👉** [ test-cases](https://docs.google.com/spreadsheets/d/12yJfJr4lzlcJjpkx3QFfJPffLmTajegcwKSF42BHdbk/edit?usp=sharing)

---
## Módulo 2 — Inicio de sesión

### CPL01 · Inicio de sesión de estudiante con 3 intentos fallidos

| **Campo** | **Detalle** |
|--------|------|
| **IDs Riesgo** | R-01 |
| **Precondición**   | <ul><li>Conexión a internet estable</li> <li> Se accede al formulario del sistema: https://playground.calidadsinhumo.com/login </li> <li> El usuario tenga una cuenta registrada </li></ul>  |
| **Pasos**  | <ol><li> Llenar el formulario con email válido y contraseña incorrecta -> (Email = ana.garcia@ejemplo.com, Contraseña incorrecta = 12345678)</li> <li>Hacer clic en "Iniciar sesión"</li> <li>Repetir los pasos 1-2 (2 veces más)</li> </ol>  |
| **Resultado esperado** | <ul> <li>Se espera que el sistema en el intento 3 no bloquee la cuenta del usuario</li> <li>Muestre el mensaje de error adecuado de  “Email o contraseña incorrectos"</li> <li>El usuario permanece en el formulario de "Iniciar sesión"</li> </ul>  |

---
### CPL04 · Inicio de sesión de estudiante y foco en la habilitación de botón (segundo 5 restante)

| **Campo** | **Detalle** |
|--------|------|
| **IDs Riesgo** | R-02 |
| **Precondición**   | <ul><li>Conexión a internet estable</li> <li> Se accede al formulario del sistema: https://playground.calidadsinhumo.com/login </li> <li> El usuario tenga una cuenta registrada </li></ul>  |
| **Pasos**  | <ol><li> Llenar el formulario con email válido y contraseña incorrecta -> (Email = ana.garcia@ejemplo.com, Contraseña incorrecta = 12345678)</li> <li>Hacer clic en "Iniciar sesión"</li> <li>Repetir los pasos 1-2 (3 veces más)</li> <li>Después del  intento 4, esperar hasta que el timer visual marque 5 segundo restantes</li> <li>Intentar volver hacer clic en "Iniciar sesión"</li>  </ol>  |
| **Resultado esperado** | <ul> <li>Se espera que el sistema cuando el timer llega a 5 segundos restantes, no habilite el botón de "Iniciar sesión"</li> <li>El usuario no pueda hacer clic en "Iniciar sesión"</li> <li>El usuario permanece en el formulario de "Iniciar sesión"</li> </ul>  |

---
QA Portfolio — Jhon Churivanti