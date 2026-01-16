# Test Plan – DemoBankApp

## Objetivo
Validar la funcionalidad principal de la aplicación bancaria móvil: login, transacciones y notificaciones.

## Alcance
- **Incluye:** login, transferencias, historial de transacciones, notificaciones push, APIs de backend.
- **Excluye:** pruebas de performance avanzada, pruebas en dispositivos legacy.

## Estrategia
- Funcionales: login, transferencias, notificaciones.
- Exploratorias: gestos móviles (tap, swipe, scroll).
- Automatizadas: Appium para login y transferencias.
- APIs: Postman para login y cuentas.
- Usabilidad: mensajes de error claros, accesibilidad básica.

## Criterios de entrada/salida
- Entrada: app instalada en emulador/dispositivo, credenciales de prueba.
- Salida: 100% de casos ejecutados, defectos críticos corregidos.

## Cronograma
- Día 1–2: pruebas de login.
- Día 3–4: pruebas de transacciones.
- Día 5: pruebas de notificaciones y reporte final.

## Riesgos
- Inestabilidad del emulador → mitigación: pruebas en dispositivos reales.
- Cambios en APIs → mitigación: actualización de casos.
