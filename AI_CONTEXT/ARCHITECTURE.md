# Architecture: Planificador de eventos Omega

## 1. Estructura física

La aplicación principal está concentrada en:

pp-planificador.html

Dentro del archivo existe principalmente:

1. HTML de la interfaz
2. CSS de la aplicación
3. JavaScript de la lógica
4. Importaciones de Firebase
5. Integraciones externas

El bloque principal de JavaScript comienza aproximadamente en la línea 10352.

---

## 2. Servicios externos

### Firebase

Importaciones identificadas:

- irebase-app.js
- irebase-auth.js
- irebase-firestore.js

Firebase se inicializa aproximadamente en las líneas 10353-10365.

Funciones relacionadas con autenticación:

- signInWithEmailAndPassword
- signOut
- onAuthStateChanged

Funciones relacionadas con Firestore:

- collection
- ddDoc
- updateDoc
- deleteDoc
- doc
- onSnapshot
- serverTimestamp
- query
- setDoc

---

## 3. Navegación principal

La interfaz contiene áreas identificadas para:

- Dashboard
- Board
- Daily
- Calendar
- Gantt
- Clients
- Reports

Cuando una tarea solicite modificar una sección concreta, localizar primero los elementos HTML y funciones asociados a esa sección.

---

## 4. Eventos

Funciones identificadas relacionadas con eventos:

- stageOf
- llStages
- stageLabel
- stageCalClass
- stageBarClass
- confirmClass
- opClass
- header
- dateTime
- overlap
- conflicts
- hasConflict
- eventHasConflict
- iltered
- stageText
- cleanForFirestore
- seedExcelIfEmpty
- startRealtime
- ender

Estas funciones deben revisarse antes de modificar comportamiento general de eventos, filtros, conflictos, sincronización o renderizado.

---

## 5. Dashboard

Funciones identificadas:

- enderDashboard
- enderWeeklySummary
- dashboardWeekBounds
- eventTouchesWeek
- setHomeListMode
- setReportsConflictScope
- eventFirstRelevantDate
- eventTouchesMonth
- enderHomeEventList
- eventRow
- miniCalendarHtml

Si una modificación afecta al dashboard, localizar primero estas funciones y sus elementos HTML relacionados.

---

## 6. Calendario y Gantt

Funciones identificadas:

- miniCalendarHtml
- ssignGanttLanes
- miniGanttHtml
- enderDailyMiniGantt
- enderDailyWorkspaceGantt

También existen clases y funciones relacionadas con estados visuales de eventos:

- stageCalClass
- stageBarClass
- confirmClass
- opClass

No modificar estas funciones de forma aislada sin comprobar si son utilizadas por más de una vista.

---

## 7. Actividades / tareas diarias

Esta es una de las áreas con mayor cantidad de lógica actualmente identificada.

Funciones principales:

### Creación y edición

- ddInlineDailyTask
- updateDailyTaskFromPage
- updateDailyTaskFromPageField
- deleteDailyTaskFromPage
- ddDailyTaskFromPageQuick

### Workspace diario

- openDailyTasksEvent
- closeDailyWorkspace
- setDailyWorkspaceTab
- updateDailyWorkspaceField
- updateDailyWorkspaceStatus
- deleteDailyWorkspaceTask
- ddDailyWorkspaceTask
- updateDailyWorkspaceEventField
- updateDailyWorkspaceStageField
- saveDailyWorkspace
- updateDailyWorkspaceState
- enderDailyWorkspaceGantt
- enderDailyWorkspace

### Editor rápido

- openDailyQuickEditor
- closeDailyQuickEditor
- updateDailyQuickField
- updateDailyQuickStatus
- deleteDailyQuickTask
- ddDailyQuickTask
- saveDailyQuickEditor
- updateDailyQuickSaveState
- enderDailyQuickEditorBody

### Eventos y borradores diarios

- enderDailyEventCards
- updateDailyDraftField
- updateDailyDraftStatus
- deleteDailyDraftTask
- ddDailyDraftTask
- saveDailyDraft
- cancelDailyDraft
- updateDailyDraftSaveState
- enderDailySelectedEvent

### Conflictos y tiempo

- 	askTimeLabel
- 	asksOverlap
- dailyActivityConflicts
- dailyTaskConflictIds
- llDailyTasks
- dailyHourBucket
- dailyHourLabel
- eventDailyStats
- dailyEventMatchesFilter

Cuando una tarea mencione "tareas diarias", "Daily", "actividad diaria", "workspace diario" o conflictos entre actividades, comenzar la investigación en esta sección.

---

## 8. Outlook

Funciones identificadas:

- outlookStageDateTime
- sendToOutlookFlow
- syncEventToOutlook
- deleteEventFromOutlook

Una modificación relacionada con Outlook debe revisar estas funciones y los puntos donde son invocadas.

---

## 9. Fechas y tiempo

Funciones identificadas:

- dateStr
- 	oday
- parseDate
- shortDate
- ullDate
- dateTime

Los cambios relacionados con fechas deben revisar estas funciones antes de introducir nuevas conversiones o formatos.

---

## 10. Exportación

Existe lógica relacionada con exportación a Excel.

Antes de modificar la exportación, localizar las funciones exactas responsables y sus puntos de llamada.

No asumir que una función relacionada con Excel solamente afecta a la exportación; comprobar dependencias antes de modificar.

---

## 11. Eventos de interfaz

La aplicación utiliza numerosos handlers asociados a controles HTML, incluyendo:

- onclick
- onchange

También existen controles relacionados con:

- Login
- Logout
- Navegación
- Tareas diarias
- Calendario
- Gantt
- Exportación
- Edición de eventos

Cuando una funcionalidad deje de responder después de un cambio, revisar tanto la función modificada como el handler HTML/JavaScript que la invoca.

---

## 12. Estrategia de navegación para IA

Ante una solicitud de modificación:

### Paso 1

Identificar la funcionalidad afectada.

### Paso 2

Buscar primero el nombre de la función, elemento o evento relacionado.

### Paso 3

Leer únicamente el bloque de código necesario.

### Paso 4

Identificar dependencias directas.

### Paso 5

Comprobar si la función es utilizada por otras vistas.

### Paso 6

Realizar el cambio mínimo necesario.

### Paso 7

Revisar el diff:

git diff

### Paso 8

Probar la funcionalidad afectada.

### Paso 9

Actualizar AI_CONTEXT si cambió la arquitectura, una decisión importante o el estado del proyecto.

---

## 13. Regla de lectura del código

pp-planificador.html tiene aproximadamente 15.289 líneas y alrededor de 448 KB.

No cargar el archivo completo en el contexto de IA salvo que exista una razón técnica concreta.

Preferir:

- búsquedas por función
- búsquedas por identificador HTML
- búsquedas por evento
- lectura de rangos de líneas
- revisión de dependencias
- lectura de funciones relacionadas

El objetivo es proporcionar al agente únicamente el contexto necesario para resolver la tarea.

---

## 14. Estado de este mapa

Este documento es una primera versión del mapa arquitectónico.

Las relaciones entre funciones y dependencias deben verificarse progresivamente a medida que se trabaje en cada módulo.

No asumir que la lista actual representa todas las funciones existentes.
