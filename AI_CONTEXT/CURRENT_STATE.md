# Current State

## Fecha de referencia

19 de septiembre de 2026.

---

## Estado general

El proyecto se encuentra actualmente en funcionamiento como una aplicación web monolítica.

La aplicación principal está contenida en:

pp-planificador.html

No se ha realizado todavía una separación del HTML, CSS y JavaScript en múltiples archivos.

---

## Código

Archivo principal:

pp-planificador.html

Características identificadas:

- HTML
- CSS
- JavaScript
- Firebase Web SDK
- lógica de autenticación
- lógica de Firestore
- lógica de eventos
- dashboard
- tareas diarias
- calendario
- Gantt
- clientes
- reportes
- exportación
- integración con Outlook

El archivo contiene aproximadamente 15.289 líneas y 448 KB.

---

## Firebase

Firebase CLI instalada y funcionando.

Versión comprobada:

15.30.0

Proyecto Firebase:

planificador-de-eventos-omega

La CLI tiene acceso al proyecto.

Servicios Firebase identificados en el código:

- Authentication
- Cloud Firestore

---

## Git

Git está instalado y funcionando.

Rama principal:

main

Repositorio local inicializado correctamente.

Primer commit:

7164f1

Mensaje:

chore: initial project setup

El repositorio remoto de GitHub está configurado y la rama local main está sincronizada con origin/main.

Estado conocido al crear este documento:

working tree clean

---

## GitHub

El proyecto ya tiene un repositorio privado en GitHub.

GitHub CLI está instalada y autenticada.

La conexión local utiliza el remoto:

origin

---

## Control de archivos

.gitignore está configurado para excluir:

- irebase-debug.log
- .firebase/
- .env
- .env.*
- 
ode_modules/
- .vscode/
- archivos temporales del sistema

No se ha incluido irebase-debug.log en el repositorio.

---

## Sistema de contexto para IA

Ya se han creado:

- AGENTS.md
- AI_CONTEXT/PROJECT.md
- AI_CONTEXT/ARCHITECTURE.md
- AI_CONTEXT/CURRENT_STATE.md
- AI_CONTEXT/DECISIONS.md
- AI_CONTEXT/TASKS.md

El objetivo es que los agentes de IA puedan consultar primero el contexto relevante y después localizar únicamente las partes necesarias del código.

---

## Indexación y recuperación de código

Todavía no se ha implementado un sistema adicional de indexación semántica o búsqueda especializada del código.

Actualmente la estrategia consiste en:

1. consultar AGENTS.md
2. consultar AI_CONTEXT/
3. buscar funciones, identificadores o eventos
4. leer únicamente los rangos relevantes de pp-planificador.html
5. modificar el mínimo código necesario
6. revisar el diff
7. probar el cambio

---

## Refactorización

No se ha realizado todavía una refactorización estructural del archivo principal.

La aplicación continúa utilizando una arquitectura monolítica.

Cualquier futura separación en módulos debe realizarse de forma controlada y verificando las dependencias existentes.

---

## Dependencias Node

Existe:

package-lock.json

Actualmente no existe un package.json funcional asociado a un proyecto Node.

No se debe asumir que el proyecto utiliza un entorno Node para ejecutar la aplicación.

---

## Pendientes conocidos

El sistema de documentación todavía debe completarse con:

- decisiones arquitectónicas
- tareas pendientes
- cambios futuros
- relaciones más precisas entre módulos
- posibles mejoras del sistema de recuperación de código para IA

---

## Regla de mantenimiento

Este archivo debe actualizarse cuando cambie de manera significativa el estado técnico del proyecto.

No actualizarlo por cada pequeño cambio visual o corrección menor.

Los cambios importantes de arquitectura, infraestructura, herramientas o flujo de trabajo deben quedar registrados aquí o en el archivo de contexto correspondiente.
