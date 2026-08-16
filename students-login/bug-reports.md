## Reporte de Bugs 

**Fecha**: Agosto 2026  | **Autor**: Jhon Churivanti Alva  | **Web para prueba**: [Playground CSH](https://playground.calidadsinhumo.com/registro)

---
## Resumen

| **Total de bugs** | **Alta** | **Media**  |**Baja** | 
|--------|------|------|------|
| 2 | 1 | 0 | 1 | 

---
## Bugs de — Inicio de sesión

### DEF-L01 · Se bloquea la cuenta del usuario en el inicio de sesión con 4 intentos fallidos

| **Campo** | **Detalle** |
|--------|------|
| **IDs caso** | CPL02, CPL03 |
| **Descripción** | El sistema permite el bloqueo de la cuenta de usuario, cuando este llega a tener 4 intentos fallidos consecutivos. Y no le permite realizar un intento más, lo cual debería cumplir según la spec (en el intento 5 se bloquea). |
| **Precondición**   | <ul><li>Conexión a internet estable</li> <li> Se accede al formulario del sistema: https://playground.calidadsinhumo.com/login </li> <li> El usuario tenga una cuenta registrada </li></ul> |
| **Pasos para reproducir**  | <ol><li>Llenar cada campo del formulario con los Datos de Prueba -> (Email: ana.garcia@ejemplo.com, Contraseña: 12345678)</li> <li>Hacer clic en “Iniciar sesión”</li> <li>Repetir los pasos 1-2 (3 veces más)</li> <li> Sin esperar el desbloqueo, intenta hacer clic en “Iniciar sesión” una vez más (observar que el sistema ya está bloqueado y botón deshabilitado, no permite alcanzar el intento 5) </li></ol> |
| **Resultado esperado** | <ul><li>Se espera que el sistema  en el intento 4 no bloquee la cuenta del usuario.</li> <li>Muestre el mensaje de error adecuado de “Email o contraseña incorrectos”</li> <li>El usuario permanece en el formulario de “Iniciar sesión” </li> <ul> |
| **Resultado obtenido** | <ul><li>El sistema en el intento 4 bloquea la cuenta del usuario</li> <li>No muestra el mensaje de error adecuado "Email o contraseña incorrectos" porque el sistema pasa directamente al estado de bloqueo</li> <li>Se permanece en el formulario de inicio de sesión</li> </ul> |
| **Ambiente**  | Fue encontrado en windows 11, navegadores Brave y Microsoft Edge  |
| **Severidad**  | Alta   |
| **Prioridad**  | Alta  |
| **Fecha**  |  14/08/2026  |
| **Evidencia**  | [Link(captura de pantalla)](https://drive.google.com/file/d/1-xsJOUnGymKGZ2KHqc8FUB28HsOQcHgx/view?usp=sharing) |

---
### DEF-L02 · Se habilita el botón de “Iniciar sesión” antes de tiempo, en el segundo 5 restante

| **Campo** | **Detalle** |
|--------|------|
| **IDs caso** | CPL04 |
| **Descripción** | El sistema permite de manera visual la habilitación del botón 5 segundos antes de lo que indica la spec, donde solo debería de habilitar cuando el timer visual llega a 0. Permitiendo hacer clic y el botón solo responda, nada de login exitoso.  |
| **Precondición**   | <ul><li>Conexión a internet estable</li> <li> Se accede al formulario del sistema: https://playground.calidadsinhumo.com/login </li> <li> El usuario tenga una cuenta registrada </li></ul> |
| **Pasos para reproducir**  | <ol><li>Llenar cada campo del formulario con los Datos de Prueba -> (Email: ana.garcia@ejemplo.com, Contraseña: 12345678)</li> <li>Hacer clic en “Iniciar sesión”</li> <li>Repetir los pasos 1-2 (3 veces más)</li> <li>Después del intento 4, esperar hasta que el timer marque 5 segundos restantes</li> <li>Intentar volver hacer clic en “Iniciar sesión”</li> </ol> |
| **Resultado esperado** | <ul><li>Se espera que el sistema cuando el timer llega a 5 segundos restantes, no habilite el botón de "Iniciar sesión"</li> <li>El usuario no pueda hacer clic en "Iniciar sesión"</li> <li>El usuario permanece en el formulario de "Iniciar sesión". </li> </ul> |
| **Resultado obtenido** | <ul><li>El sistema cuando el timer llega  a 5 segundos restantes, habilita el botón de "Iniciar sesión"</li> <li>El botón se habilita visualmente y permite hacer clic  5 segundos antes de tiempo, no resulta en un login exitoso, el botón solo responde</li> <li>Se permanece en el formulario de "Iniciar sesión"</li> <ul> |
| **Ambiente**  | Fue encontrado en Windows 11, navegadores Brave y Microsoft Edge  |
| **Severidad**  | Baja   |
| **Prioridad**  | Media  |
| **Fecha**  |  14/08/2026  |
| **Evidencia**  | [Link(captura de pantalla)](https://drive.google.com/file/d/1tSH1HSk7V3jkDp4Ubif5GFRU2DWdSqoJ/view?usp=sharing) |

---
QA Portfolio — Jhon Churivanti