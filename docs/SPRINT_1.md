# SPRINT 1 — Base SuriOS-COROS / COROSLINK

**Fecha de cierre:** 2026-10-19
**Reloj objetivo:** COROS PACE 3
**Entorno:** COROSLINK, trabajando con previsualización y sin reloj físico disponible
**Proyecto COROSLINK:** `SuriOS-COROS PACE 3 V0`

## Objetivo

Preparar una primera adaptación visual de la Watchface Ultra v1.7 para COROS, conservando la identidad de SuriOS y dejando fuera todo lo relacionado con RADAR.

## Trabajo realizado

- Creación y configuración inicial del proyecto para PACE 3.
- Ajuste de escala y encaje de la armadura.
- Eliminación del texto residual `S 28`/similar.
- Incorporación del emblema de la Hermandad como fondo con baja opacidad.
- Ampliación del indicador de batería al 200 % respecto a su tamaño inicial.
- Conservación de la composición principal de hora, fecha, clima, batería y armadura.
- Mantenimiento de las etiquetas `CAPS`, `TRAINING` y `STATUS` como elementos independientes.
- Evaluación de la conversión de la armadura en indicador de pasos.
- Evaluación del reemplazo de `RADIO` por control multimedia.

## Decisiones y limitaciones

- La armadura queda como sprite estático en COROSLINK. El editor no permite aplicar sobre ella una máscara u opacidad vinculada directamente a pasos/objetivo diario.
- El componente `Steps chart` disponible en COROSLINK es experimental, usa datos de muestra en la previsualización y no permite controlar la armadura.
- `CAPS`, `TRAINING`, `STATUS` y `RADIO` siguen siendo textos estáticos; no son botones funcionales en esta versión del proyecto.
- COROSLINK no ofrece una capa de control multimedia para este template/firmware. Tampoco aparece un control `media/music` en su configuración raw.
- RADAR queda explícitamente fuera del alcance de este proyecto.
- No se ha enviado nada al reloj ni a COROS; el proyecto se ha validado únicamente en previsualización.

## Estado final

- **Versión:** V0
- **Estado en COROSLINK:** guardado
- **Template:** `260526`
- **Firmware type:** `COROS W331`
- **Capas:** 21
- **Reloj:** sin conexión / no disponible durante el sprint

El proyecto COROSLINK se conserva localmente en su almacenamiento de aplicación, bajo:

`%APPDATA%\coroslink\watchface-projects\3e29d799-acf3-4a9e-bbc5-3ad3962dabe7\`

No se versionan la caché, la base de datos ni las carpetas de AppData de COROSLINK, conforme al flujo definido en `COROSLINK_HANDOFF.md`.

## Próximo sprint

Validar la esfera en la previsualización de 240×240 y, cuando haya un PACE 3 disponible, comprobar la renderización real, la interacción del reloj y la compatibilidad de los datos dinámicos.
