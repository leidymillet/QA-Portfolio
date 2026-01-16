# 🧪 Test Plan – SauceDemo

## 1. Objetivo de las pruebas
- Validar la funcionalidad principal del sitio de e-commerce SauceDemo: login, navegación de productos, carrito y checkout.  
- Evaluar rendimiento básico en carga de páginas.  
- Verificar seguridad mínima (login inválido, usuarios bloqueados).  
- Asegurar usabilidad en flujos críticos (mensajes de error claros, persistencia de sesión).  
- Validar APIs REST con Postman (login, catálogo, carrito, checkout).  
- Demostrar experiencia en automatización con Cypress en flujos críticos.  

---

## 2. Alcance
- **Incluye:** login, catálogo de productos, carrito de compras, checkout, logout, validación de APIs, automatización con Cypress.  
- **Excluye:** pruebas de performance avanzada, pruebas en dispositivos móviles legacy, pruebas de seguridad profunda.  

---

## 3. Estrategia de pruebas
- **Funcionales:** casos positivos y negativos de login, agregar productos al carrito, checkout.  
- **Regresión:** repetir pruebas tras cambios en el sitio.  
- **Exploratorias:** detectar comportamientos inesperados en flujos no documentados.  
- **Automatizadas (Cypress):** login, carrito, checkout, validaciones de UI y smoke tests.  
- **Carga ligera:** verificar respuesta con múltiples usuarios concurrentes.  
- **Usabilidad:** mensajes de error claros, consistencia visual, accesibilidad básica.  
- **Ambientes:** navegador Chrome y Firefox en desktop.  
- **Herramientas:** Postman (API), Cypress (automatización), GitHub (documentación).  

---

## 4. Criterios de entrada y salida
- **Entrada:** ambiente disponible, credenciales de prueba (ej. *standard_user*, *locked_out_user*), datos preparados.  
- **Salida:** 100% de casos ejecutados, defectos críticos corregidos, reporte final con métricas, sin defectos de severidad alta abiertos.  

---

## 5. Casos de prueba detallados

| ID   | Caso de Prueba                        | Pasos                                                                 | Resultado Esperado                                      | Severidad | Automatable con Cypress |
|------|----------------------------------------|----------------------------------------------------------------------|---------------------------------------------------------|-----------|-------------------------|
| TC01 | Login válido                           | 1. Ir a login<br>2. Ingresar *standard_user* y password válido<br>3. Click en Login | Acceso exitoso, redirección al catálogo                 | Alta      | ✅ |
| TC02 | Login inválido                         | 1. Ir a login<br>2. Ingresar credenciales incorrectas<br>3. Click en Login | Mensaje de error claro, sin acceso                      | Alta      | ✅ |
| TC03 | Login usuario bloqueado                | 1. Ir a login<br>2. Ingresar *locked_out_user* y password válido<br>3. Click en Login | Mensaje de error específico de bloqueo                  | Alta      | ✅ |
| TC04 | Agregar producto al carrito            | 1. Seleccionar producto<br>2. Click en “Add to cart”<br>3. Ir al carrito | Producto aparece listado en carrito                     | Alta      | ✅ |
| TC05 | Carrito vacío en checkout              | 1. Ir al carrito vacío<br>2. Click en Checkout                         | Sistema impide continuar, mensaje de error              | Media     | ✅ |
| TC06 | Checkout con múltiples productos       | 1. Agregar 2+ productos<br>2. Ir al carrito<br>3. Click en Checkout<br>4. Completar datos | Total calculado correctamente, orden confirmada         | Alta      | ✅ |
| TC07 | Persistencia de sesión                 | 1. Login válido<br>2. Refrescar página                                | Usuario sigue logueado, sesión activa                   | Media     | ✅ |
| TC08 | Logout                                 | 1. Login válido<br>2. Click en Logout                                 | Usuario sale correctamente, redirección a login         | Media     | ✅ |
| TC09 | API – Login                            | 1. Enviar request POST con credenciales válidas<br>2. Revisar respuesta | Código 200, token válido en payload                     | Alta      | ❌ (Postman) |
| TC10 | API – Catálogo                         | 1. Enviar request GET catálogo<br>2. Revisar respuesta                 | Código 200, lista de productos con campos correctos     | Alta      | ❌ (Postman) |
| TC11 | API – Checkout                         | 1. Enviar request POST con carrito válido<br>2. Revisar respuesta      | Código 200, confirmación de orden                       | Alta      | ❌ (Postman) |
| TC12 | Validar elementos de UI en catálogo    | 1. Login válido<br>2. Revisar que cada producto tenga nombre, precio y botón | Todos los elementos visibles y consistentes             | Media     | ✅ |
| TC13 | Ordenar productos por precio           | 1. Login válido<br>2. Usar menú de ordenación “Price (low to high)”    | Productos listados en orden ascendente de precio        | Media     | ✅ |
| TC14 | Validar mensajes de error en checkout  | 1. Login válido<br>2. Ir al carrito<br>3. Click en Checkout sin completar datos obligatorios | Mensaje de error claro indicando campos faltantes       | Alta      | ✅ |
| TC15 | Smoke Test automatizado (suite básica) | 1. Login válido<br>2. Agregar producto<br>3. Checkout completo         | Flujo crítico ejecutado sin errores                     | Alta      | ✅ |

---

## 6. Gestión de defectos
- Reporte en `/bug-reports` con: título, pasos, resultado esperado/obtenido, severidad, prioridad.  
- Seguimiento en GitHub Issues o documento compartido.  

---

## 7. Recursos y responsabilidades
- **Responsable QA:** Leidy.  
- **Herramientas:** Postman, Cypress, GitHub.  
- **Tiempo estimado:** 1 semana de ejecución.  

---

## 8. Cronograma
- **Día 1–2:** pruebas de login y carrito.  
- **Día 3–4:** pruebas de checkout, logout y regresión.  
- **Día 5:** reporte de métricas y defectos.  

---

## 9. Riesgos y mitigaciones
- **Cambios en el sitio demo:** riesgo de que se actualice y rompa pruebas → mitigación: actualizar casos.  
- **Datos de prueba limitados:** riesgo de inconsistencias → mitigación: usar credenciales estándar provistas por SauceDemo.  
- **Inestabilidad del entorno demo:** riesgo de fallos intermitentes → mitigación: reejecutar pruebas críticas y documentar.  
