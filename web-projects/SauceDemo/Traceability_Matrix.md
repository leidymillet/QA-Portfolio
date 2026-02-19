# 🔗 Traceability Matrix – SauceDemo

Este documento relaciona los **requisitos funcionales y no funcionales** del sitio SauceDemo con los **casos de prueba** definidos en el Test Plan.  
El objetivo es garantizar cobertura completa y detectar requisitos sin pruebas asociadas.

---

## 1. Requisitos ↔ Casos de prueba

| ID Requisito | Descripción del requisito | Casos de prueba asociados | Estado de cobertura |
|--------------|---------------------------|---------------------------|---------------------|
| R01 | El sistema debe permitir login con credenciales válidas | TC01 | Cubierto |
| R02 | El sistema debe mostrar error con credenciales inválidas | TC02 | Cubierto |
| R03 | El sistema debe impedir acceso a usuarios bloqueados | TC03 | Cubierto |
| R04 | El usuario debe poder agregar productos al carrito | TC04 | Cubierto |
| R05 | El sistema debe impedir checkout con carrito vacío | TC05 | Cubierto |
| R06 | El sistema debe permitir checkout con múltiples productos | TC06 | Cubierto |
| R07 | La sesión debe persistir tras refrescar la página | TC07 | Cubierto |
| R08 | El sistema debe permitir logout correctamente | TC08 | Cubierto |
| R09 | API debe validar login y devolver token | TC09 | Cubierto |
| R10 | API debe devolver catálogo de productos | TC10 | Cubierto |
| R11 | API debe procesar checkout con carrito válido | TC11 | Cubierto |
| R12 | Cada producto en catálogo debe mostrar nombre, precio y botón | TC12 | Cubierto |
| R13 | El sistema debe permitir ordenar productos por precio | TC13 | Cubierto |
| R14 | El sistema debe mostrar mensajes de error claros en checkout | TC14 | Cubierto |
| R15 | El flujo crítico (login → carrito → checkout) debe ejecutarse sin errores | TC15 | Cubierto |

---

## 2. Observaciones
- Todos los requisitos funcionales principales tienen al menos un caso de prueba asociado.  
- Los requisitos críticos (login, checkout, API) están cubiertos por múltiples casos de prueba y automatización.  
- La trazabilidad asegura que no hay requisitos sin validación.  

---

## 3. Relación con otros artefactos
- Los riesgos críticos identificados en `Risk_Matrix.md` se reflejan en los casos de prueba asociados.  
- Los resultados de ejecución se documentan en `Reports/Execution_Summary.md`.  
- Los defectos encontrados se registran en `Bug_Reports/Defects.md`.  
