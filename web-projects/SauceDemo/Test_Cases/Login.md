# Casos de Prueba – Login (SauceDemo)

| ID   | Caso de Prueba        | Pasos                                                                 | Resultado Esperado                          | Severidad | Automatable con Cypress |
|------|-----------------------|----------------------------------------------------------------------|---------------------------------------------|-----------|-------------------------|
| TC01 | Login válido          | 1. Ir a login<br>2. Ingresar *standard_user* y password válido<br>3. Click en Login | Acceso exitoso, redirección al catálogo     | Alta      | ✅ |
| TC02 | Login inválido        | 1. Ir a login<br>2. Ingresar credenciales incorrectas<br>3. Click en Login | Mensaje de error claro, sin acceso          | Alta      | ✅ |
| TC03 | Login usuario bloqueado | 1. Ir a login<br>2. Ingresar *locked_out_user* y password válido<br>3. Click en Login | Mensaje de error específico de bloqueo      | Alta      | ✅ |
