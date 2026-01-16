# Casos de Prueba – Carrito (SauceDemo)

| ID   | Caso de Prueba              | Pasos                                                                 | Resultado Esperado                          | Severidad | Automatable con Cypress |
|------|-----------------------------|----------------------------------------------------------------------|---------------------------------------------|-----------|-------------------------|
| TC04 | Agregar producto al carrito | 1. Seleccionar producto<br>2. Click en “Add to cart”<br>3. Ir al carrito | Producto aparece listado en carrito         | Alta      | ✅ |
| TC05 | Carrito vacío en checkout   | 1. Ir al carrito vacío<br>2. Click en Checkout                         | Sistema impide continuar, mensaje de error  | Media     | ✅ |
| TC07 | Persistencia de sesión      | 1. Login válido<br>2. Refrescar página                                | Usuario sigue logueado, sesión activa       | Media     | ✅ |
