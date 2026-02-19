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
- **Entrada:** ambiente disponible, credenciales de prueba (`standard_user`, `locked_out_user`), datos preparados.  
- **Salida:**  
  - 100% de casos ejecutados.  
  - Defectos críticos corregidos.  
  - Reporte final con métricas.  
  - Sin defectos de severidad alta abiertos.  
  - Todos los requisitos críticos cubiertos según la **matriz de trazabilidad**.  
  - Riesgos críticos mitigados según la **matriz de riesgos**.  

---

## 5. Casos de prueba detallados
*(La cobertura de estos casos respecto a los requisitos está documentada en `Traceability_Matrix.md`)*  

| ID   | Caso de Prueba | Pasos | Resultado Esperado | Severidad | Automatable con Cypress |
|------|----------------|-------|--------------------|-----------|-------------------------|
| TC01 | Login válido | Ingresar credenciales correctas | Acceso exitoso | Alta | ✅ |
| TC02 | Login inválido | Ingresar credenciales incorrectas | Error claro | Alta | ✅ |
| TC03 | Login usuario bloqueado | Ingresar usuario bloqueado | Error específico | Alta | ✅ |
| TC04 | Agregar producto al carrito | Seleccionar producto → Add to cart | Producto en carrito | Alta | ✅ |
| TC05 | Carrito vacío en checkout | Checkout sin productos | Mensaje de error | Media | ✅ |
| TC06 | Checkout con múltiples productos | Agregar 2+ productos → Checkout | Total correcto, orden confirmada | Alta | ✅ |
| TC07 | Persistencia de sesión | Login → refrescar página | Sesión activa | Media | ✅ |
| TC08 | Logout | Login → Logout | Redirección a login | Media | ✅ |
| TC09 | API – Login | POST con credenciales válidas | Código 200, token válido | Alta | ❌ |
| TC10 | API – Catálogo | GET catálogo | Código 200, lista correcta | Alta | ❌ |
| TC11 | API – Checkout | POST con carrito válido | Código 200, confirmación | Alta | ❌ |
| TC12 | Validar elementos UI catálogo | Login → revisar productos | Nombre, precio, botón visibles | Media | ✅ |
| TC13 | Ordenar productos por precio | Usar filtro “low to high” | Orden ascendente | Media | ✅ |
| TC14 | Mensajes de error en checkout | Checkout sin datos obligatorios | Error claro | Alta | ✅ |
| TC15 | Smoke Test automatizado | Login → carrito → checkout | Flujo crítico sin errores | Alta | ✅ |

---

## 6. Gestión de defectos
- Reporte en `/Bug_Reports` con: título, pasos, resultado esperado/obtenido, severidad, prioridad.  
- Seguimiento en GitHub Issues o documento compartido.  

---

## 7. Recursos y responsabilidades
- Responsable QA: **Leidy**.  
- Herramientas: Postman, Cypress, GitHub.  
- Tiempo estimado: 1 semana de ejecución.  

---

## 8. Cronograma
- **Día 1–2:** pruebas de login y carrito.  
- **Día 3–4:** pruebas de checkout, logout y regresión.  
- **Día 5:** reporte de métricas y defectos.  

---

## 9. Riesgos y mitigaciones
*(Los riesgos detallados se documentan en `Risk_Matrix.md`)*  

- Cambios en el sitio demo → riesgo de que se actualice y rompa pruebas → mitigación: actualizar casos.  
- Datos de prueba limitados → riesgo de inconsistencias → mitigación: usar credenciales estándar provistas por SauceDemo.  
- Inestabilidad del entorno demo → riesgo de fallos intermitentes → mitigación: reejecutar pruebas críticas y documentar.  

---

## 10. Artefactos complementarios
- **Risk_Matrix.md** → Identificación y priorización de riesgos críticos.  
- **Traceability_Matrix.md** → Relación entre requisitos y casos de prueba.  
- **Reports/Execution_Summary.md** → Informe de resultados y métricas tras ejecución.  
