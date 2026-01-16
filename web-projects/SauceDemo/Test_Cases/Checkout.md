# Casos de Prueba – Checkout (SauceDemo)

| ID   | Caso de Prueba                        | Pasos                                                                 | Resultado Esperado                          | Severidad | Automatable con Cypress |
|------|----------------------------------------|----------------------------------------------------------------------|---------------------------------------------|-----------|-------------------------|
| TC06 | Checkout con múltiples productos       | 1. Agregar 2+ productos<br>2. Ir al carrito<br>3. Click en Checkout<br>4. Completar datos | Total calculado correctamente, orden confirmada | Alta      | ✅ |
| TC14 | Validar mensajes de error en checkout  | 1. Login válido<br>2. Ir al carrito<br>3. Click en Checkout sin completar datos obligatorios | Mensaje de error claro indicando campos faltantes | Alta      | ✅ |
| TC15 | Smoke Test automatizado (suite básica) | 1. Login válido<br>2. Agregar producto<br>3. Checkout completo         | Flujo crítico ejecutado sin errores         | Alta      | ✅ |
