# Casos de Prueba – API (SauceDemo)

| ID   | Caso de Prueba   | Pasos                                                                 | Resultado Esperado                          | Severidad | Herramienta |
|------|------------------|----------------------------------------------------------------------|---------------------------------------------|-----------|-------------|
| TC09 | API – Login      | 1. Enviar request POST con credenciales válidas<br>2. Revisar respuesta | Código 200, token válido en payload         | Alta      | Postman |
| TC10 | API – Catálogo   | 1. Enviar request GET catálogo<br>2. Revisar respuesta                 | Código 200, lista de productos con campos correctos | Alta      | Postman |
| TC11 | API – Checkout   | 1. Enviar request POST con carrito válido<br>2. Revisar respuesta      | Código 200, confirmación de orden           | Alta      | Postman |
