# Casos de Prueba – Login (DemoBankApp)

| ID   | Caso de Prueba        | Pasos                                                                 | Resultado Esperado                          | Severidad | Automatable con Appium |
|------|-----------------------|----------------------------------------------------------------------|---------------------------------------------|-----------|-------------------------|
| TC01 | Login válido          | Ingresar usuario válido y contraseña → Tap en Login | Acceso exitoso, redirección al dashboard    | Alta      | ✅ |
| TC02 | Login inválido        | Ingresar credenciales incorrectas → Tap en Login | Mensaje de error claro, sin acceso          | Alta      | ✅ |
| TC03 | Login usuario bloqueado | Ingresar usuario bloqueado → Tap en Login | Mensaje de error específico de bloqueo      | Alta      | ✅ |
