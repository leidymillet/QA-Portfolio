# Casos de Prueba - Módulo Login

## TC01 - Login válido
- **Escenario:** Autenticación exitosa
- **Pasos de ejecución:** Ingresar credenciales correctas
- **Datos de prueba:** Usuario: `standard_user`, Password: `secret_sauce`
- **Precondiciones:** Acceso al sitio disponible
- **Prioridad:** Alta
- **Severidad:** Alta
- **Status:** ✅ Ejecutado
- **Resultado esperado:** Acceso exitoso al catálogo
- **Resultado obtenido:** Acceso permitido
- **Evidencia:** ![Captura Login válido](evidencias/login_valido.png)

---

## TC02 - Login inválido
- **Escenario:** Autenticación fallida
- **Pasos de ejecución:** Ingresar credenciales incorrectas
- **Datos de prueba:** Usuario: `fake_user`, Password: `12345`
- **Precondiciones:** Acceso al sitio disponible
- **Prioridad:** Alta
- **Severidad:** Alta
- **Status:** ✅ Ejecutado
- **Resultado esperado:** Mensaje de error claro
- **Resultado obtenido:** Mensaje “Username and password do not match”
- **Evidencia:** ![Captura Login inválido](evidencias/login_invalido.png)

---

## TC03 - Login usuario bloqueado
- **Escenario:** Usuario bloqueado
- **Pasos de ejecución:** Ingresar usuario bloqueado
- **Datos de prueba:** Usuario: `locked_out_user`, Password: `secret_sauce`
- **Precondiciones:** Acceso al sitio disponible
- **Prioridad:** Alta
- **Severidad:** Alta
- **Status:** ✅ Ejecutado
- **Resultado esperado:** Mensaje de error específico
- **Resultado obtenido:** “Sorry, this user has been locked out”
- **Evidencia:** ![Captura Login bloqueado](evidencias/login_bloqueado.png)

---

## TC07 - Persistencia de sesión
- **Escenario:** Sesión activa tras refrescar
- **Pasos de ejecución:** Login → refrescar página
- **Datos de prueba:** Usuario: `standard_user`, Password: `secret_sauce`
- **Precondiciones:** Usuario logueado
- **Prioridad:** Media
- **Severidad:** Media
- **Status:** ✅ Ejecutado
- **Resultado esperado:** Sesión activa
- **Resultado obtenido:** Usuario permanece en catálogo
- **Evidencia:** ![Captura Persistencia](evidencias/sesion_activa.png)

---

## TC08 - Logout
- **Escenario:** Cierre de sesión
- **Pasos de ejecución:** Login → Logout
- **Datos de prueba:** Usuario: `standard_user`, Password: `secret_sauce`
- **Precondiciones:** Usuario logueado
- **Prioridad:** Media
- **Severidad:** Baja
- **Status:** ✅ Ejecutado
- **Resultado esperado:** Redirección a pantalla de login
- **Resultado obtenido:** Usuario vuelve al login
- **Evidencia:** ![Captura Logout](evidencias/logout.png)
