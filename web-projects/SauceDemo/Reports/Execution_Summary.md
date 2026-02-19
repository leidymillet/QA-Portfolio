# 📊 Execution Summary – SauceDemo

## 1. Resumen general
- Total de casos de prueba: 15  
- Casos ejecutados: 15  
- Casos pasados: 13  
- Casos fallidos: 2  
- Defectos críticos abiertos: 1  
- Estado: **Pendiente de corrección antes de release**

---

## 2. Resultados por módulo
| Módulo   | Casos ejecutados | Pasados | Fallidos | Defectos reportados |
|----------|------------------|---------|----------|---------------------|
| Login    | 3                | 2       | 1        | 1 (usuario bloqueado) |
| Carrito  | 2                | 2       | 0        | - |
| Checkout | 3                | 2       | 1        | 1 (mensaje de error inconsistente) |
| Logout   | 1                | 1       | 0        | - |
| API      | 3                | 3       | 0        | - |
| UI/UX    | 3                | 3       | 0        | - |

---

## 3. Defectos críticos
- **Bug ID 001:** Al pagar con tarjeta inválida, el sistema muestra “Compra exitosa” en lugar de error.  
  - Severidad: Crítica  
  - Estado: Abierto  
  - Reportado en: `/Bug_Reports/Defects.md`

---

## 4. Métricas de ejecución
- Cobertura de requisitos: 100% (según `Traceability_Matrix.md`)  
- Riesgos críticos mitigados: 80% (según `Risk_Matrix.md`)  
- Tiempo total de ejecución: 5 días  
- Herramientas utilizadas: Cypress, Postman, GitHub  

---

## 5. Conclusiones
- Los flujos principales (login, carrito, checkout) funcionan en su mayoría correctamente.  
- Se requiere corrección en el módulo de **checkout** antes de liberar.  
- La automatización con Cypress cubre los flujos críticos y smoke tests.  
- La validación de APIs con Postman fue exitosa.  

---

## 6. Próximos pasos
- Corregir defectos críticos en checkout.  
- Reejecutar pruebas de regresión tras correcciones.  
- Actualizar `Risk_Matrix.md` y `Execution_Summary.md` con nuevos resultados.  
