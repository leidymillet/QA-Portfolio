# Test Plan – SauceDemo

## 1. Objetivo de las pruebas
- Validar la funcionalidad principal del sitio de e-commerce SauceDemo: login, navegación de productos, carrito y checkout.
- Evaluar rendimiento básico en carga de páginas.
- Verificar seguridad mínima (login con credenciales inválidas).
- Asegurar usabilidad en flujos críticos (compra completa).

## 2. Alcance de las pruebas
- **Incluye:** login, catálogo de productos, carrito de compras, checkout.
- **Excluye:** pruebas de performance avanzada, pruebas en dispositivos móviles legacy, pruebas de seguridad profunda.

## 3. Estrategia de pruebas
- **Funcionales:** casos positivos y negativos de login, agregar productos al carrito, checkout.
- **Regresión:** repetir pruebas tras cambios en el sitio.
- **Automatizadas:** scripts básicos en Cypress para login y checkout.
- **Carga ligera:** verificar respuesta con múltiples usuarios concurrentes.
- **Ambientes:** navegador Chrome y Firefox en desktop.
- **Herramientas:** Postman (API), Cypress (automatización), GitHub (documentación).

## 4. Criterios de entrada y salida
- **Entrada:** ambiente disponible, credenciales de prueba, datos preparados.
- **Salida:** 100% de casos ejecutados, defectos críticos corregidos, reporte final con métricas.

## 5. Casos de prueba
- **Login válido:** usuario estándar accede correctamente.
- **Login inválido:** credenciales incorrectas muestran mensaje de error.
- **Agregar producto al carrito:** producto aparece en carrito.
- **Checkout completo:** compra finalizada con confirmación.
- **Logout:** usuario sale correctamente.

## 6. Gestión de defectos
- Reporte en `/bug-reports` con: título, pasos, resultado esperado/obtenido, severidad, prioridad.
- Seguimiento en GitHub Issues o documento compartido.

## 7. Recursos y responsabilidades
- **Responsable QA:** Leidy.
- **Herramientas:** Postman, Cypress, GitHub.
- **Tiempo estimado:** 1 semana de ejecución.

## 8. Cronograma de pruebas
- Día 1–2: pruebas de login y carrito.
- Día 3–4: pruebas de checkout y regresión.
- Día 5: reporte de métricas y defectos.

## 9. Riesgos y mitigaciones
- **Cambios en el sitio demo:** riesgo de que se actualice y rompa pruebas → mitigación: actualizar casos.
- **Datos de prueba limitados:** riesgo de inconsistencias → mitigación: usar credenciales estándar provistas por SauceDemo.
