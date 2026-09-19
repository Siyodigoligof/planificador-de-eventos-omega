# Technical Decisions

Registro de decisiones técnicas y de arquitectura del proyecto.

---

## DEC-001 — Mantener temporalmente la aplicación como archivo monolítico

**Estado:** Activa

**Fecha:** 19 de septiembre de 2026

### Decisión

Mantener la aplicación principal concentrada en pp-planificador.html.

### Motivo

La aplicación ya contiene múltiples funcionalidades relacionadas y actualmente funciona como una aplicación monolítica.

Separar inmediatamente HTML, CSS y JavaScript podría introducir cambios innecesarios y riesgos sobre funcionalidades existentes.

### Consecuencia

Los cambios deben realizarse de forma localizada dentro del archivo siempre que sea posible.

La refactorización modular podrá evaluarse posteriormente si existe una necesidad técnica concreta.

---

## DEC-002 — Utilizar Git como sistema de control de versiones

**Estado:** Activa

**Fecha:** 19 de septiembre de 2026

### Decisión

Utilizar Git para controlar los cambios del proyecto y GitHub como repositorio remoto privado.

### Motivo

Permite:

- conservar historial de cambios
- comparar modificaciones
- recuperar versiones anteriores
- trabajar con ramas
- facilitar el trabajo con herramientas de IA
- mantener un respaldo remoto del código

### Consecuencia

Los cambios relevantes deben quedar registrados mediante commits.

---

## DEC-003 — Utilizar main como rama principal

**Estado:** Activa

**Fecha:** 19 de septiembre de 2026

### Decisión

La rama principal del proyecto será main.

### Motivo

Mantener una convención moderna y consistente con el repositorio remoto.

---

## DEC-004 — Mantener Firebase Web SDK en el cliente

**Estado:** Activa

**Fecha:** 19 de septiembre de 2026

### Decisión

Mantener la configuración necesaria del Firebase Web SDK dentro de la aplicación cliente.

### Motivo

La aplicación utiliza directamente Firebase Authentication y Cloud Firestore desde el navegador.

La configuración pública del SDK no debe tratarse automáticamente como una contraseña o clave privada.

### Regla de seguridad

No introducir en el cliente:

- claves privadas
- service account keys
- contraseñas
- tokens secretos
- credenciales administrativas

La seguridad debe gestionarse mediante los mecanismos apropiados de Firebase, especialmente autenticación y reglas de seguridad.

---

## DEC-005 — Utilizar documentación específica para agentes de IA

**Estado:** Activa

**Fecha:** 19 de septiembre de 2026

### Decisión

Mantener documentación específica para agentes mediante:

- AGENTS.md
- AI_CONTEXT/PROJECT.md
- AI_CONTEXT/ARCHITECTURE.md
- AI_CONTEXT/CURRENT_STATE.md
- AI_CONTEXT/DECISIONS.md
- AI_CONTEXT/TASKS.md

### Motivo

El archivo principal contiene aproximadamente 15.289 líneas.

Proporcionar siempre el archivo completo a una IA genera consumo de contexto innecesario cuando una tarea solamente requiere una pequeña parte del código.

### Consecuencia

Los agentes deben utilizar primero la documentación y posteriormente realizar búsquedas específicas sobre el código.

---

## DEC-006 — Preferir recuperación selectiva de código

**Estado:** Activa

**Fecha:** 19 de septiembre de 2026

### Decisión

Para modificaciones específicas, localizar primero funciones, identificadores, eventos y dependencias relacionadas antes de leer grandes cantidades del archivo principal.

### Motivo

Reducir contexto innecesario y disminuir el riesgo de modificar código no relacionado.

### Consecuencia

La lectura completa de pp-planificador.html debe reservarse para casos donde sea técnicamente necesaria.

---

## DEC-007 — No introducir dependencias Node sin necesidad

**Estado:** Activa

**Fecha:** 19 de septiembre de 2026

### Decisión

No convertir automáticamente el proyecto en una aplicación Node únicamente porque exista package-lock.json.

### Motivo

Actualmente la aplicación funciona principalmente como una aplicación HTML del lado del cliente.

No existe un package.json funcional asociado a un flujo Node.

### Consecuencia

Cualquier incorporación de Node, npm o herramientas de build debe justificarse por una necesidad concreta.

---

## DEC-008 — Actualizar el contexto cuando cambie la arquitectura

**Estado:** Activa

**Fecha:** 19 de septiembre de 2026

### Decisión

Las modificaciones importantes de arquitectura deben reflejarse en los archivos correspondientes de AI_CONTEXT.

### Motivo

La documentación debe representar el estado real del proyecto para evitar que los agentes trabajen con información obsoleta.

### Consecuencia

Cuando una modificación cambie:

- estructura
- arquitectura
- servicios
- dependencias importantes
- flujo de datos
- decisiones técnicas

se debe actualizar la documentación correspondiente.

---

## DEC-009 — No refactorizar sin una razón técnica concreta

**Estado:** Activa

**Fecha:** 19 de septiembre de 2026

### Decisión

No realizar refactorizaciones estructurales solamente por razones estéticas u organizativas.

### Motivo

La prioridad actual es mantener la funcionalidad existente y establecer un flujo seguro de mantenimiento asistido por IA.

### Consecuencia

Las mejoras estructurales deben justificarse por beneficios concretos y evaluarse antes de ejecutarse.

---

## Registro futuro

Las nuevas decisiones importantes deben añadirse siguiendo este formato:

DEC-XXX — Título

Incluyendo:

- Estado
- Fecha
- Decisión
- Motivo
- Consecuencia

No registrar aquí cambios menores de código que no representen una decisión técnica.
