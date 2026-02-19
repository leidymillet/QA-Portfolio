# ⚠️ Risk Matrix – SauceDemo

Este documento identifica los riesgos principales en el sitio de e-commerce SauceDemo, evaluando impacto y probabilidad para priorizar las pruebas.

---

## 1. Escala de evaluación
- **Impacto:** Bajo, Medio, Alto  
- **Probabilidad:** Baja, Media, Alta  
- **Nivel de riesgo:** calculado combinando impacto y probabilidad (Crítico, Alto, Medio, Bajo)

---

## 2. Matriz de riesgos

| ID  | Riesgo                                    | Impacto | Probabilidad | Nivel   | Mitigación |
|-----|-------------------------------------------|---------|--------------|---------|------------|
| R01 | Fallo en pasarela de pago                 | Alto    | Alta         | Crítico | Pruebas exhaustivas de checkout y validación de respuestas de API |
| R02 | Stock incorrecto en carrito/checkout      | Alto    | Media        | Alto    | Validar inventario en cada compra y pruebas de regresión tras cambios |
| R03 | Acceso sin login (bypass de seguridad)    | Alto    | Baja         | Medio   | Pruebas de seguridad y roles, validación de sesiones |
| R04 | Mensajes de error poco claros             | Medio   | Alta         | Alto    | Pruebas de usabilidad, verificación de mensajes en login y checkout |
| R05 | Pérdida de sesión al refrescar página     | Medio   | Media        | Medio   | Validar persistencia de sesión en múltiples navegadores |
| R06 | API devuelve datos incompletos o erróneos | Alto    | Media        | Alto    | Validación con Postman de endpoints críticos (login, catálogo, checkout) |
| R07 | Inestabilidad del entorno demo            | Medio   | Alta         | Alto    | Reejecutar pruebas críticas, documentar fallos intermitentes |

---

## 3. Conclusiones
- Los riesgos **críticos** se concentran en el **checkout/pago** y en la **integridad del stock**.  
- Los riesgos **altos** incluyen problemas de mensajes de error y estabilidad del entorno demo.  
- La mitigación se centra en pruebas funcionales exhaustivas, validación de APIs y pruebas de seguridad básicas.  

---

## 4. Relación con otros artefactos
- Los riesgos críticos están priorizados en el **Test Plan**.  
- La cobertura de mitigación se refleja en la **Traceability_Matrix.md** (requisitos ↔ casos de prueba).  
- Los resultados de ejecución y defectos relacionados se documentan en **Reports/Execution_Summary.md** y **Bug_Reports/**.  
