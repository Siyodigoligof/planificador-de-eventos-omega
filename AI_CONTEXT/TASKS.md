# TASKS.md

## Estado actual

### Completado

- [x] Crear repositorio Git local.
- [x] Configurar rama principal main.
- [x] Crear repositorio privado en GitHub.
- [x] Conectar repositorio local con GitHub.
- [x] Crear .gitignore.
- [x] Crear AGENTS.md.
- [x] Crear carpeta AI_CONTEXT.
- [x] Crear PROJECT.md.
- [x] Crear ARCHITECTURE.md.
- [x] Crear CURRENT_STATE.md.
- [x] Crear DECISIONS.md.

### En progreso

- [ ] Completar la infraestructura de contexto para trabajar con IA.
- [ ] Establecer un sistema de búsqueda y recuperación selectiva del código.
- [ ] Verificar el flujo completo de trabajo Git → modificación → prueba → commit → push.

### Pendiente

- [ ] Evaluar una estrategia de indexación/búsqueda del código.
- [ ] Definir el flujo de trabajo recomendado para solicitar cambios a la IA.
- [ ] Documentar procedimientos habituales de desarrollo.
- [ ] Identificar funcionalidades que convenga separar si la aplicación crece.
- [ ] Revisar progresivamente posibles problemas técnicos del código existente.
- [ ] Mantener actualizados los archivos de contexto cuando cambie la arquitectura.

## Reglas para gestionar tareas

1. No marcar una tarea como completada sin haber verificado el resultado.
2. Las tareas grandes deben dividirse en subtareas concretas.
3. Antes de modificar código, identificar qué tarea se está resolviendo.
4. Evitar mezclar cambios no relacionados dentro de una misma tarea.
5. Después de realizar cambios, revisar git diff y comprobar el funcionamiento.
6. Actualizar este archivo cuando una tarea importante cambie de estado.
7. No utilizar este archivo como historial detallado de cambios; para eso se utiliza Git.

## Formato para tareas futuras

Las tareas nuevas deben utilizar este formato:

- [ ] [Área] Descripción concreta de la tarea.

Ejemplos:

- [ ] [Dashboard] Corregir el cálculo de eventos de la semana.
- [ ] [Calendario] Ajustar visualización de eventos superpuestos.
- [ ] [Firebase] Revisar reglas de seguridad de Firestore.
- [ ] [Daily] Corregir actualización del estado de una actividad.
- [ ] [Outlook] Revisar sincronización de eventos eliminados.

## Prioridades

Cuando sea necesario priorizar tareas:

- **Alta:** afecta funcionamiento, datos, seguridad o bloquea otra tarea.
- **Media:** mejora una funcionalidad existente o corrige un problema no crítico.
- **Baja:** mejoras visuales, organización o funcionalidades secundarias.

## Regla para la IA

Antes de comenzar una modificación:

1. Leer AGENTS.md.
2. Consultar AI_CONTEXT/PROJECT.md.
3. Consultar AI_CONTEXT/ARCHITECTURE.md cuando la tarea involucre varias partes del sistema.
4. Consultar AI_CONTEXT/TASKS.md para conocer el estado actual.
5. Consultar AI_CONTEXT/DECISIONS.md si la modificación puede contradecir una decisión existente.
6. Localizar únicamente el código relacionado con la tarea.
7. Realizar el cambio mínimo necesario.
8. Verificar el resultado.
9. Actualizar TASKS.md si corresponde.

## Mantenimiento

Actualizar este archivo cuando:

- se complete una tarea importante;
- aparezca una tarea nueva relevante;
- una tarea quede bloqueada;
- cambie significativamente el estado del proyecto.

No registrar aquí cada pequeño cambio de código.
