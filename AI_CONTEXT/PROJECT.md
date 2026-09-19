# Project: Planificador de eventos Omega

## Descripción

Aplicación web para planificación y gestión de eventos.

Actualmente está implementada principalmente en un único archivo HTML:

pp-planificador.html

El archivo contiene la interfaz, estilos CSS y lógica JavaScript de la aplicación.

## Firebase

La aplicación utiliza Firebase como backend y servicios de autenticación.

Firebase utilizado actualmente:

- Firebase Authentication
- Cloud Firestore
- Firebase Web SDK mediante módulos ES

Proyecto Firebase:

- Project ID: planificador-de-eventos-omega

## Funcionalidades identificadas

La aplicación contiene funcionalidades relacionadas con:

- Autenticación de usuarios
- Dashboard
- Gestión de eventos
- Gestión de actividades/tareas diarias
- Calendario
- Gantt
- Clientes
- Reportes
- Exportación a Excel
- Integración con Outlook

## Archivo principal

pp-planificador.html

Tamaño aproximado actual: 448 KB.

El código JavaScript comienza alrededor de la línea 10352 y contiene gran parte de la lógica de la aplicación.

## Arquitectura actual

La aplicación utiliza una arquitectura monolítica de cliente:

HTML + CSS + JavaScript dentro de pp-planificador.html.

No existe actualmente una estructura tradicional de múltiples archivos JavaScript, componentes o módulos locales.

## Control de versiones

Repositorio Git:

- Rama principal: main
- Repositorio remoto: GitHub
- Primer commit: 7164f1
- Mensaje: chore: initial project setup

## Regla para agentes de IA

Este archivo proporciona contexto general.

Para realizar cambios específicos, el agente debe consultar primero ARCHITECTURE.md y localizar las partes relevantes del código antes de leer o modificar grandes secciones de pp-planificador.html.
