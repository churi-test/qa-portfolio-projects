## Casos de Prueba Manuales - Ejecutados

**Fecha de ejecución**: 13 Agosto 2026 | **Autor**: Jhon Churivanti Alva |  **Web para prueba**: [Playground CSH](https://playground.calidadsinhumo.com/registro)

---
## Resumen

| Módulo | Casos | Pasaron | Fallaron | Estado|
|--------|------|------|------|------|
| Inicio de sesión  | 4 | 1 | 3 | 2 Bugs encontrados|

Total de pruebas ejecutadas manualmente: 4

**☑️ Visualizar por completo los casos ejecutados, gracias 👉** [test-execution](https://docs.google.com/spreadsheets/d/1Kk-nx1Oa2DB0iBgylFv_7-u60fS7p4t0OOamF6AD9cM/edit?usp=sharing)

---
## Módulo 2 — Inicio de sesión

### CPL01 · Inicio de sesión de estudiante  con 3 intentos fallidos

| **Campo** | **Detalle** |
|--------|------|
| **IDs Riesgo** | R-01 |
| **Precondición**   | <ul><li>Conexión a internet estable</li> <li> Se accede al formulario del sistema: https://playground.calidadsinhumo.com/login </li> <li> El usuario tenga una cuenta registrada </li></ul>  |
| **Pasos**  | <ol><li> Llenar el formulario con email válido y contraseña incorrecta</li> <li>Hacer clic en "Iniciar sesión"</li> <li>Repetir los pasos 1-2 (2 veces más)</li> </ol> |
| **Resultado esperado** | <ul> <li>Se espera que el sistema en el intento 3 no bloquee la cuenta del usuario</li> <li>Muestre el mensaje de error adecuado de  “Email o contraseña incorrectos"</li> <li>El usuario permanece en el formulario de "Iniciar sesión"</li> </ul>   |
| **Datos de prueba** | <ul><li>Email: ana.garcia@ejemplo.com</li> <li>Contraseña: 12345678 </li> |
| **Prioridad**  | Alta  |
| **Resultado obtenido**  | <ul> <li>El sistema en el intento 3 no bloquea la cuenta del usuario</li> <li>Mostró el mensaje de error "Email o contraseña incorrectos"</li> <li>Se permanece en el formulario de "Inicio de sesión"</li> </ul>  |
| **Estado**  | Aprobado ☑️  |

---
### CPL04 · Inicio de sesión de estudiante y foco en la habilitación de botón (segundo 5 restante)

| **Campo** | **Detalle** |
|--------|------|
| **IDs Riesgo** | R-02 |
| **Precondición**   | <ul><li>Conexión a internet estable</li> <li> Se accede al formulario del sistema: https://playground.calidadsinhumo.com/login </li> <li> El usuario tenga una cuenta registrada </li></ul>  |
| **Pasos**  | <ol><li> Llenar el formulario con email válido y contraseña incorrecta</li> <li>Hacer clic en "Iniciar sesión"</li> <li>Repetir los pasos 1-2 (3 veces más)</li> <li>Después del  intento 4, esperar hasta que el timer visual marque 5 segundos restantes</li> <li>Intentar volver hacer clic en "Iniciar sesión"</li>  </ol>  |
| **Resultado esperado** | <ul> <li>Se espera que el sistema cuando el timer llega a 5 segundos restantes, no habilite el botón de "Iniciar sesión"</li> <li>El usuario no pueda hacer clic en "Iniciar sesión"</li> <li>El usuario permanece en el formulario de "Iniciar sesión"</li> </ul>  |
| **Datos de prueba** | <ul><li>Email: ana.garcia@ejemplo.com</li> <li>Contraseña: 12345678 </li> |
| **Prioridad**  | Media  |
| **Resultado obtenido**  | <ul> <li>El sistema cuando el timer llega  a 5 segundos restantes, habilita el botón de "Iniciar sesión"</li> <li>El botón se habilita visualmente y permite hacer clic  5 segundos antes de tiempo, no resulta en un login exitoso, el botón solo responde</li> <li>Se permanece en el formulario de "Iniciar sesión"</li> </ul>  |
| **Estado**  | Fallido ❌   |
| **Evidencia**  | [Link(captura de pantalla)](https://drive.google.com/file/d/1tSH1HSk7V3jkDp4Ubif5GFRU2DWdSqoJ/view?usp=sharing)  |
| **IDs defecto**  | DEF-L02  |

---
QA Portfolio — Jhon Churivanti