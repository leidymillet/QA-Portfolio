# Casos de Prueba – Transacciones (DemoBankApp)

| ID   | Caso de Prueba              | Pasos                                                                 | Resultado Esperado                          | Severidad | Automatable con Appium |
|------|-----------------------------|----------------------------------------------------------------------|---------------------------------------------|-----------|-------------------------|
| TC04 | Transferencia válida        | Login → Seleccionar cuenta origen → Ingresar monto → Confirmar | Transferencia exitosa, saldo actualizado    | Alta      | ✅ |
| TC05 | Transferencia inválida      | Login → Seleccionar cuenta origen → Ingresar monto > saldo → Confirmar | Mensaje de error, sin ejecución             | Alta      | ✅ |
| TC06 | Historial de transacciones  | Login → Ir a historial | Lista de transacciones visible y ordenada | Media     | ✅ |
