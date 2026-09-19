# AGENTS.md

## Proyecto

Planificador de eventos web desarrollado como una aplicación HTML monolítica.

## Estructura actual

- pp-planificador.html: aplicación principal. Contiene HTML, CSS y JavaScript.
- package-lock.json: archivo de bloqueo existente; actualmente no existe un package.json funcional.
- .gitignore: archivos excluidos del control de versiones.
- irebase-debug.log: generado por Firebase CLI y excluido de Git.

## Backend y servicios

La aplicación utiliza Firebase:
- Firebase Authentication
- Cloud Firestore
- Firebase Web SDK mediante módulos ES desde gstatic.com

Proyecto Firebase:
- Project ID: planificador-de-eventos-omega

## Regla principal para trabajar con el código

No leer ni modificar pp-planificador.html completo si la tarea puede resolverse trabajando únicamente con una sección, función o bloque relevante.

Antes de modificar código:

1. Identificar qué funcionalidad está involucrada.
2. Localizar las funciones, eventos, elementos HTML o estilos relacionados.
3. Leer únicamente el contexto necesario.
4. Revisar dependencias directas antes de modificar.
5. Mantener intactas las funcionalidades no relacionadas.
6. Verificar el resultado antes de realizar un commit.

## Arquitectura actual

La aplicación es monolítica: HTML, CSS y JavaScript están contenidos principalmente en pp-planificador.html.

No realizar una refactorización estructural únicamente por motivos de organización sin evaluar primero el impacto sobre las funcionalidades existentes.

## Firebase

No eliminar ni ocultar arbitrariamente la configuración pública de Firebase del cliente.

Las modificaciones relacionadas con autenticación, Firestore o reglas de seguridad deben tratarse con especial cuidado.

## Git

La rama principal es main.

Antes de cada commit:

- revisar git diff
- comprobar que no existan cambios no relacionados
- verificar que no se hayan incluido archivos sensibles o temporales

Los commits deben describir claramente el cambio realizado.

## Regla de seguridad

Nunca introducir en el repositorio:

- claves privadas
- service account keys
- contraseñas
- tokens
- credenciales
- archivos .env con secretos
