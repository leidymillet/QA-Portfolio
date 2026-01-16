# SauceDemo – Proyecto Web QA

Este proyecto corresponde a pruebas funcionales y automatizadas sobre la aplicación de e-commerce **SauceDemo**.  
El objetivo es validar los flujos críticos de un sitio de compras en línea: login, catálogo de productos, carrito y checkout.

## 📌 Alcance
- Pruebas funcionales: login, carrito, checkout, logout.
- Pruebas de API: validación de endpoints con Postman.
- Automatización: scripts básicos con Cypress para flujos críticos.
- Usabilidad: mensajes de error claros y persistencia de sesión.
- Regresión: ejecución tras cambios en el sitio.

## 📂 Estructura del proyecto
- **Test_Plan.md** → Estrategia de pruebas, alcance, cronograma y riesgos.
- **Test_Cases/** → Casos de prueba organizados por módulos:
  - Login.md
  - Cart.md
  - Checkout.md
  - API.md
- **Bug_Reports/** → Registro de defectos encontrados durante la ejecución.
- **Automation/Cypress/** → Scripts de automatización para login, carrito y checkout.

## 🛠️ Herramientas utilizadas
- **Cypress** → Automatización end-to-end.
- **Postman** → Validación de APIs REST.
- **GitHub** → Documentación y gestión de defectos.

## 🎯 Objetivo
Asegurar que los flujos principales de SauceDemo funcionen correctamente, con cobertura en pruebas manuales y automatizadas, mostrando buenas prácticas de QA en proyectos web.
