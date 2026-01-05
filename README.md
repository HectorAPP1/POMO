# Pomodoro 25/5 — Focus & Wake

Aplicación de pomodoro enfocada en combatir la somnolencia en jornadas de oficina. Incluye temporizador 25/5, micro-acciones activas, registro de cafeína y notificaciones para mantenerte despierto y productivo.

## Tabla de contenidos

1. [Características](#características)
2. [Requisitos y ejecución](#requisitos-y-ejecución)
3. [Controles y atajos](#controles-y-atajos)
4. [Datos que persisten](#datos-que-persisten)
5. [Personalización](#personalización)
6. [Tecnologías utilizadas](#tecnologías-utilizadas)
7. [Licencia](#licencia)

## Características

- **Timer Pomodoro 25/5** con alternancia entre enfoque y descansos activos.
- **Autocambio opcional** entre fases al finalizar cada bloque.
- **Micro-acciones anti-sueño** con logs diarios/total, temporizador independiente y edición completa.
- **Panel de estado** con tips rápidos y accesos directos.
- **Gestión de sonidos** (start, pause, fin de bloque, avisos) usando Web Audio API.
- **Notificaciones de escritorio** al terminar cada fase (requieren permiso del navegador).
- **Contador de ciclos** y registro del último café para cuidar el sueño.
- **Persistencia local** con `localStorage` para no perder configuraciones ni historiales.
- **Interfaz responsive** y diseño con gradientes, cartas translúcidas y modo oscuro.

## Requisitos y ejecución

1. Clona o descarga este repositorio.
2. Abre `index.html` en tu navegador preferido (se recomienda Chrome/Edge/Firefox).
3. Acepta los permisos de sonido/notificaciones cuando el navegador los solicite para aprovechar todas las funciones.

> No se requiere un servidor ni instalación adicional: la app funciona como un archivo único con React 18 desde CDN y Babel Standalone para JSX.

## Controles y atajos

- **Botón principal** ▶️ / ⏸️ para iniciar o pausar el ciclo actual.
- **Botones rápidos** para cambiar a modo Foco o Descanso y reiniciar el temporizador.
- **Atajos de teclado**:
  - `Space`: Play/Pause.
  - `R`: Reinicia el bloque actual.
  - `S`: Activa/desactiva sonidos.
  - `N`: Activa/desactiva notificaciones.
  - `Esc`: Cierra cualquier modal abierto.

## Datos que persisten

La aplicación guarda información en `localStorage` para mantener tu contexto entre sesiones:

- Duración configurada de foco y descanso.
- Contador de ciclos completados.
- Última hora registrada de cafeína.
- Listado de micro-acciones personalizadas y su historial (hoy, total, última vez).

Puedes limpiar estos datos desde las opciones internas (por ejemplo, reiniciar ciclos o borrar historial de una acción) o eliminando el almacenamiento local del sitio desde tu navegador.

## Personalización

- Ajusta duraciones con los controles deslizables del modal **“Ajustes rápidos”** (15–60 min foco, 3–15 min descanso).
- Usa los presets 25/5 o 20/5 anti-sueño para configurar rápidamente.
- Agrega, edita o elimina micro-acciones (emoji, descripción, duración) según tus necesidades.
- Modifica colores o comportamientos avanzados editando directamente `index.html` (el JSX de React está embebido bajo el tag `<script type="text/babel">`).

## Tecnologías utilizadas

- **React 18** y **ReactDOM** (CDN UMD) para la interfaz y estado.
- **Babel Standalone** para transpilar JSX en tiempo de ejecución.
- **Web Audio API** para tonos y feedback auditivo.
- **Web Notifications API** para avisos de cambio de fase.
- **localStorage** para persistencia ligera del usuario.

## Licencia

Este proyecto no declara una licencia explícita. Si planeas reutilizar el código, revisa con el autor la licencia deseada o agrega una en este repositorio.
