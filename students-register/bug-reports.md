## Reporte de Bugs 

**Fecha**: Agosto 2026  | **Autor**: Jhon Churivanti Alva  | **Web para prueba**: [Playground CSH](https://playground.calidadsinhumo.com/registro)

---
## Resumen

| **Total de bugs** | **Alta** | **Media**  | **Baja** | 
|--------|------|------|------|
| 3 | 3 | 0 | 0 | 0 |

---
## Bugs de — Registro de estudiante

### DEF-R01 · Se permite la creación de un nuevo estudiante cuando “Email” tiene un dominio inválido

| **Campo** | **Detalle** |
|--------|------|
| **IDs caso** | CPR03 |
| **Descripción** | El sistema permite la creación de un nuevo estudiante con todos los datos completos del formulario pero el campo “Email” contiene un valor de correo con dominio inválido. |
| **Precondición**   | <ul><li>Conexión a internet estable</li> <li> Se accede al formulario del sistema: https://playground.calidadsinhumo.com/registro </li> <li> El usuario no tenga una cuenta registrada </li></ul> |
| **Pasos para reproducir**  | <ol><li>Llenar cada campo del formulario con los Datos de Prueba -> (Nombre: Juan, Email: user1@.com, Contraseña: 12345678, Edad: 16)</li> <li>Presionar el botón  "Crear cuenta" para enviar los datos del formulario.</li> <li>Una vez enviado, ahora prueba nuevamente con este email -> (Nombre: Juan, Email: usuario@gmail, Contraseña: 12345678, Edad: 16).</li> <li> Vuelve a presionar el botón “Crear cuenta”.</li></ol> |
| **Resultado esperado** | <ul><li>Se espera que el sistema no registre el nuevo estudiante, se muestre un mensaje de error adecuado de "El email no tiene un formato válido".</li> <li>El usuario permanece en el formulario de "Crear cuenta".</li> <ul>|
| **Resultao obtenido** | El sistema permitió registrar el nuevo estudiante, no mostró el mensaje de error adecuado de "El email no tiene un formato válido" y se permanece en el formulario. |
| **Ambiente**  | Fue encontrado en windows 11, navegadores Brave y Microsoft Edge  |
| **Severidad**  | Alta   |
| **Prioridad**  | Alta  |
| **Fecha**  |  06/08/2026  |
| **Evidencia**  | [Link(captura de pantalla)](https://drive.google.com/file/d/1qzRq8nUdAEvYWDa0_bjuQv9UarayE4zT/view?usp=sharing)|

---
### DEF-R02 ·  Se permite la creación de un nuevo estudiante cuando “Email” tiene una extensión de dominio demasiado corta

| **Campo** | **Detalle** |
|--------|------|
| **IDs caso** | CPR11 |
| **Descripción** | El sistema permite la creación de un nuevo estudiante con todos los datos completos del formulario pero el campo “Email” contiene un valor de correo con extensión de dominio muy corta. |
| **Precondición**   | <ul><li>Conexión a internet estable</li> <li> Se accede al formulario del sistema: https://playground.calidadsinhumo.com/registro </li> <li> El usuario no tenga una cuenta registrada </li></ul>  |
| **Pasos para reproducir**  | <ol><li>Llenar cada campo del formulario con los Datos de Prueba -> (Nombre: Juan, Email: a@a.p, Contraseña: 12345678, Edad: 16)</li> <li>Presionar el botón "Crear cuenta” para enviar los datos del formulario.</li></ol> |
| **Resultado esperado** | <ul><li>Se espera que el sistema no registre el nuevo estudiante, se muestre un mensaje de error adecuado de "El email no tiene un formato válido".</li> <li>El usuario permanece en el formulario de "Crear cuenta".</li></ul> |
| **Resultao obtenido** | El sistema permitió registrar el nuevo estudiante, no mostró el mensaje de error adecuado de "El email no tiene un formato válido" y se permanece en el formulario. |
| **Ambiente**  | Fue encontrado en windows 11, navegadores Brave y Microsoft Edge  |
| **Severidad**  | Alta   |
| **Prioridad**  | Alta  |
| **Fecha**  |  06/08/2026  |
| **Evidencia**  | [Link(captura de pantalla)](https://drive.google.com/file/d/10_cfekFrwY9IIFygTwLYK9mLo0W_5oH4/view?usp=sharing)|

---
### DEF-R03 · Se permite la creación de un nuevo estudiante pero no se limpian los campos del formulario

| **Campo** | **Detalle** |
|--------|------|
| **IDs caso** | CPR13 |
| **Descripción** | El sistema permite la creación de un nuevo estudiante con todos los datos completos pero tras un registro exitoso, no limpia los campos: nombre, email, contraseña y edad del formulario, exponiendo los datos del usuario.  |
| **Precondición**   | <ul><li>Conexión a internet estable</li> <li> Se accede al formulario del sistema: https://playground.calidadsinhumo.com/registro </li> <li> El usuario no tenga una cuenta registrada </li></ul>|
| **Pasos para reproducir**  | <ol><li>Llenar cada campo del formulario con los Datos de Prueba -> (Nombre: Pedro, Email: pedro@gmail.com, Contraseña: 123456789, Edad: 16)</li> <li>Presionar el botón  "Crear cuenta" para enviar los datos del formulario.</li></ol> |
| **Resultado esperado** | Se espera que el sistema tras el mensaje de registro exitoso, limpie cada campo del formulario: Nombre completo, Email, Contraseña, Edad |
| **Resultao obtenido** | El sistema tras el mensaje de registro exitoso, no llegó a limpiar cada campo del formulario: Nombre completo, Email, Contraseña, Edad |
| **Ambiente**  | Fue encontrado en windows 11, navegadores Brave y Microsoft Edge  |
| **Severidad**  | Alta   |
| **Prioridad**  | Alta  |
| **Fecha**  |  06/08/2026  |
| **Evidencia**  | [Link(captura de pantalla)](https://drive.google.com/file/d/1koDuLDoG288_7xH2rEOtdcOhnvuAGRv6/view?usp=sharing)|

---
QA Portfolio — Jhon Churivanti