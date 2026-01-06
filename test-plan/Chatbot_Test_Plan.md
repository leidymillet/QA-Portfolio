# Test Plan – Drift Chatbot Demo

## 1. Objetivo de las pruebas
- Validar la interacción del chatbot en el sitio demo de Drift.
- Evaluar precisión, relevancia y tiempo de respuesta de las respuestas automáticas.
- Asegurar que el chatbot mejora la experiencia del usuario sin interrumpir la navegación.
- Detectar defectos en intents, respuestas y manejo de entradas inválidas.

## 2. Alcance
- **Incluye:** preguntas simples, preguntas predefinidas de soporte/ventas, manejo de entradas inválidas, relevancia de respuestas.
- **Excluye:** entrenamiento del modelo IA, pruebas de seguridad avanzada, integración con CRM externo.

## 3. Estrategia
- **Funcionales:** validar que el chatbot responde correctamente a preguntas esperadas.
- **Negativas:** probar entradas fuera de contexto o inválidas.
- **Usabilidad:** verificar que el chat no interrumpe la navegación del sitio.
- **Automatizadas:** usar Botium para simular conversaciones y medir métricas.
- **Ambientes:** navegador Chrome y Firefox en desktop.
- **Herramientas:** Botium, GitHub (documentación).

## 4. Criterios de entrada y salida
- **Entrada:** chatbot habilitado en el sitio demo, intents configurados.
- **Salida:** 100% de casos ejecutados, defectos críticos documentados, reporte final con métricas de precisión y cobertura.

## 5. Casos de prueba (ejemplos)
| ID   | Caso de prueba                  | Entrada                        | Resultado esperado                          |
|------|---------------------------------|--------------------------------|---------------------------------------------|
| CB01 | Pregunta simple                 | "¿Cómo contacto soporte?"      | Chatbot muestra información de contacto      |
| CB02 | Pregunta inválida               | "¿Cuál es tu color favorito?"  | Chatbot responde con mensaje de error o redirección |
| CB03 | Pregunta de ventas              | "¿Qué productos ofrecen?"      | Chatbot lista productos o redirige a ventas |
| CB04 | Tiempo de respuesta             | "Necesito ayuda con mi cuenta" | Respuesta en menos de 3 segundos             |

## 6. Gestión de defectos
- Reporte en `/bug-reports` con: título, pasos, resultado esperado/obtenido, severidad, prioridad.
- Clasificación de defectos de chatbot: precisión, relevancia, tiempo de respuesta.

## 7. Recursos y responsabilidades
- **Responsable QA:** Leidy.
- **Herramientas:** Botium, GitHub.
- **Tiempo estimado:** 1 semana de ejecución.

## 8. Cronograma
- Día 1–2: pruebas funcionales del chatbot.
- Día 3: pruebas negativas y de usabilidad.
- Día 4: pruebas automatizadas con Botium.
- Día 5: reporte de métricas y defectos.

## 9. Riesgos y mitigaciones
- **Respuestas poco relevantes:** riesgo de baja satisfacción → mitigación: documentar defectos y sugerir mejoras en intents.
- **Tiempo de respuesta alto:** riesgo de frustración → mitigación: reportar métricas y optimizar configuración.
- **Entradas no reconocidas:** riesgo de errores frecuentes → mitigación: ampliar cobertura de intents.

## 10. Métricas de cumplimiento
| Métrica                  | Fórmula                                   | Ejemplo |
|--------------------------|-------------------------------------------|---------|
| Precisión de respuestas  | (Respuestas correctas / Total) × 100      | 85%     |
| Tiempo de respuesta      | Promedio en segundos                      | 2.5s    |
| Cobertura de preguntas   | (Preguntas respondidas / Total predefinidas) × 100 | 90% |
| Relevancia alta          | Clasificación automática                  | 70%     |
