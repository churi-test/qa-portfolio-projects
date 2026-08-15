## Base Plan — Students-register
**Version**: 1.0  | **Fecha**: Agosto 2026 | **Autor**: Jhon Churivanti Alva  | **Web para prueba**: [Playground CSH](https://playground.calidadsinhumo.com/registro)

---
## 1. Requisitos
A continuación se proporciona el  requisito funcional junto a sus criterios de aceptación

|ID|RF-01|
|---|---|
|Nombre|Registro de estudiantes|
|Descripción|El sistema debe permitir a los usuarios registrarse en la plataforma, completando sus datos, nombre completo, email, contraseña, edad.|
|Criterios de aceptación| <ul><li>El sistema debe validar que todos los campos son obligatorios.</li></ul> <ul><li>El sistema debe validar que el nombre debe tener entre 2 y 50 caracteres.</li></ul> <ul><li>El sistema debe validar que el email debe tener un formato válido.</li></ul> <ul><li>El sistema debe aceptar contraseña entre 8 y 64 caracteres.</li></ul> <ul><li>El sistema debe aceptar la edad entre 16 y 99.</li></ul> <ul><li>Tras un registro exitoso, el sistema limpiará completamente todos los campos del formulario.</li></ul> <ul><li>El sistema debe validar que no se registre nuevamente un email usado.</li></ul> |

## 2. Análisis de riesgo

|#|Riesgo|Impacto|Probabi lidad|Priorid ad|Justificación|
|------|------|------|------|------|------|
|R-01|Caracteres especiales corrompen el campo nombre|Media|Media|Media|El sistema confunde textos por caracteres como *, #. Esto ocasiona que no se sepa diferenciar entre un nombre de una persona real para temas de estudio.|
|R-02|Formato de email sin dominio es aceptado|Alta|Media|Alta|Puede escribir sin @ y confundir m por n. Al colocar un dominio sin punto usuario@gmailcom. Cuando se aceptan, puede que para otros módulos como el inicio de sesión que son válidos, no permita la autenticación.|
|R-03|Los datos no se limpian después del registro exitoso|Alta|Media|Media|El sistema retiene datos tras el envío exitoso. Genera exposición de datos, si no se cumple afecta al usuario mismo de hacer un reenvío de datos y registrar datos duplicados.|
|R-04|Se acepta una contraseña de 65 caracteres|Baja|Baja|Baja|Pueden usar generadores de contraseña y al copiar y pegar se acepte dicha longitud. Entonces, tiene un bajo impacto por que la contraseña se guarda, y al usar en el módulo login no genera inconsistencia.|

## 3. Estrategia de prueba

- 3.1 Casos a probar
    
    
|ID|Riesgo|Tipo de prueba / técnica|
|------|------|------|
|R-02|Formato de email sin dominio es aceptado|Tabla de decisión, partición de equivalencia, valores límite|
|R-03|Los datos no se limpian después del registro exitoso|Prueba funcional|

- 3.2 Casos no probados

|ID|Riesgo|Tipo de prueba / técnica|
|------|------|------|
|R-01|Caracteres especiales corrompen el campo nombre|Partición de equivalencia|
|R-04|Se acepta una contraseña de 65 caracteres|Valores límite|

---
QA Portfolio — Jhon Churivanti