## Base Plan — Students-login
**Version**: 1.0  | **Fecha**: Agosto 2026 | **Autor**: Jhon Churivanti Alva  | **Web para prueba**: [Playground CSH](https://playground.calidadsinhumo.com/registro)

---
## 1. Requisitos
A continuación se proporciona el requisito funcional junto a sus criterios de aceptación

| ID | RF-01 |
|---|---|
| Nombre | Inicio de sesión |
| Descripción | El sistema debe permitir a los usuarios registrados iniciar sesión en la plataforma, usando sus credenciales de email y contraseña.|
|Criterios de aceptación| <ul><li>El sistema debe validar que el email y contraseña  son obligatorios.</li></ul> <ul><li>El sistema debe mostrar un mensaje de error cuando el email no está registrado o la contraseña  es incorrecta.</li></ul> <ul><li>El sistema debe bloquear la cuenta por 30 segundos, después de 5 intentos fallidos consecutivos.</li></ul> <ul><li>El sistema durante el bloqueo debe deshabilitar el botón de login, mostrar un timer visual de segundos restantes y habilitar el botón cuando el timer llega a 0.</li></ul> <ul><li>Tras un login exitoso, el sistema debe mostrar un mensaje de bienvenida con el nombre de usuario.</li></ul> |

## 2. Análisis de riesgo

| # | Riesgo | Impacto | Probabilidad | Prioridad |Justificación |
|------|------|------|------|------|------|
| R-01 | Bloqueo de cuenta en el cuarto intento fallido consecutivo | Alta | Media | Alta | <ul><li>Probabilidad: Media,  porque el bloqueo de la cuenta es en el intento 4, puede que el usuario no digite o copie sus credenciales de manera incorrecta.</li> <li>Impacto: Alta, esto ocasiona que los usuarios no puedan completar para ingresar al sistema. No pueden inscribirse o actualizar sus cursos.</li></ul> |
| R-02 | Habilitación de botón en el timer de 5 segundos restantes | Baja | Media | Media | <ul> <li>Probabilidad: Media, el sistema por error habilita el botón en el segundo 5 restante.</li> <li>Impacto: Baja, solo confusión visual y permite hacer clic en el botón, pero sin login exitoso, solo el botón responde a la acción.</li> </ul>|

## 3. Estrategia de prueba

- 3.1 Casos a probar
    
    
| ID | Riesgo | Tipo de prueba / técnica |
|------|------|------|
| R-01 | Bloqueo de cuenta en el cuarto intento fallido consecutivo | Valores límite |
| R-02 | Habilitación de botón en el timer de 5 segundos restantes | Prueba funcional + valores límite |

---
QA Portfolio — Jhon Churivanti