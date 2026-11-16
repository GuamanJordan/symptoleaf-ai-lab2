# Retrospectiva del Sprint 1

**Proyecto:** SymptoLeaf-AI · Grupo 3 · NRC 36848

**Fecha de elaboración:** 16 de noviembre de 2026

**Responsable del acta:** Mesias Mariscal (@AMVMesias)

**Modalidad:** revisión del trabajo registrado en GitHub y validación mediante pull request.

**Revisor solicitado:** Jordan Guaman (@GuamanJordan).

## Resultado del sprint

Se integraron los aportes de los tres integrantes: configuración de colaboración, inicio y requisitos, y modelado y proceso. Los PR #5, #6 y #15 están fusionados y sus issues #1, #2 y #3 están cerrados. El repositorio incluye la Tarea 3, su diagrama editable y `docs/proceso/PROCESO.md` con las partes A, B, C y E.

Este registro recoge observaciones sustentadas en los PR y el seguimiento comunicado por Mesias. Las acciones de mejora de esta acta se presentan a Jordan para revisión y confirmación; su publicación no acredita una reunión ni sustituye la aceptación de la docente.

## Qué funcionó

- **Cada integrante publicó un aporte identificable.** Jordan incorporó los archivos de colaboración en el [PR #5](https://github.com/GuamanJordan/symptoleaf-ai-lab2/pull/5), Denise integró inicio y requisitos en el [PR #6](https://github.com/GuamanJordan/symptoleaf-ai-lab2/pull/6) y Mesias publicó modelado y proceso en el [PR #15](https://github.com/GuamanJordan/symptoleaf-ai-lab2/pull/15). La vinculación con los issues permitió seguir su integración.
- **Las revisiones detectaron diferencias antes de aceptar los aportes.** Denise dejó un comentario de aprobación del PR #5. En el PR #6, Jordan solicitó resolver conflictos y restaurar una condición de la definición de terminado; Denise corrigió y explicó el resultado antes de la aprobación.
- **Las correcciones conservaron trazabilidad.** Denise documentó la resolución de conflictos en `50d6034` y el ajuste de la plantilla en `311dbb4`. En el PR #15, Mesias completó la descripción y agregó la asociación de Cloud Firestore con CU08 «Consultar historial» en `3c1eff8`, dejó un comentario y solicitó otra revisión. Denise aprobó el editable corregido y Jordan aprobó y fusionó el aporte.
- **Se conservaron los aportes al integrar.** El conflicto de requisitos se resolvió manteniendo la información del equipo y los enlaces de la documentación; se aprovechó esa evidencia real para el informe del laboratorio.

## Qué debemos mejorar

- **Revisar la plantilla completa antes de solicitar revisión.** En los PR #6 y #15 fue necesario completar o alinear información de la plantilla. Una comprobación previa reduciría correcciones posteriores por omisiones documentales.
- **Contrastar el editable con las especificaciones.** La asociación de Cloud Firestore con CU08 figuraba en la Tarea 3, pero faltaba en el diagrama editable. Es necesario comprobar actores, asociaciones y referencias CU antes de publicar el modelo.
- **Mantener una referencia única de historias.** `historias.md` agrupa ocho historias, mientras que los issues emplean la numeración original de once historias de la Tarea 2. Se necesita una actualización o tabla de equivalencias que evite confundir HU, RF y CU.
- **Cerrar el acceso de la docente.** Según la actualización comunicada por Mesias, del seguimiento de acceso y configuración del Project resta confirmar el acceso de la docente al repositorio y al tablero. Esa confirmación debe registrarse cuando ocurra.

## Acciones de mejora

Las fechas son objetivos propuestos. Los responsables y plazos se confirman mediante la revisión de este PR; cualquier ajuste se conserva en su conversación y en un nuevo commit del acta.

| Acción | Responsable propuesto | Fecha objetivo | Estado | Evidencia de cierre |
|---|---|---|---|---|
| Aplicar antes de cada solicitud de revisión una lista que compruebe todas las secciones de la plantilla y contraste los actores y asociaciones del editable con la especificación CU correspondiente. | Mesias (@AMVMesias), con aplicación por cada autor | 17/11/2026 | Pendiente de validación en el PR | Lista utilizada en el siguiente PR y observaciones atendidas |
| Conciliar las ocho historias agrupadas con HU1–HU11 mediante actualización de `historias.md` o tabla de equivalencias; verificar RF, CU e issues enlazados. | Denise (@DeniseRea) | 18/11/2026 | Pendiente de validación en el PR | PR revisado con la trazabilidad conciliada |
| Confirmar que la docente puede acceder al repositorio y al Project y registrar la comprobación, usando el acceso autorizado por el equipo. | Jordan (@GuamanJordan) | 18/11/2026 | Pendiente de validación en el PR; acceso docente por confirmar | Confirmación de acceso registrada por Jordan, sin publicar datos privados |

## Continuidad: Sprint 2

El objetivo documentado en el informe es diseñar entidades, navegación y permisos de Android y preparar el primer flujo de cuenta y entrada de imágenes por cámara o galería. Las historias y responsables indicados son:

| Historia de la Tarea 2 | Issue | Responsable registrado |
|---|---|---|
| HU1 · Cuenta e inicio de sesión | [#7](https://github.com/GuamanJordan/symptoleaf-ai-lab2/issues/7) | Jordan |
| HU2 · Tomar fotografía | [#8](https://github.com/GuamanJordan/symptoleaf-ai-lab2/issues/8) | Mesias |
| HU3 · Seleccionar galería | [#9](https://github.com/GuamanJordan/symptoleaf-ai-lab2/issues/9) | Denise |

La docente-cliente conserva la decisión de alcance y aceptación del incremento. El cierre de esta acta requiere la revisión de Jordan y la confirmación de las acciones, sin dar por terminadas las funcionalidades del Sprint 2.

## Evidencias consultadas

- [Revisión de Denise en el PR #5](https://github.com/GuamanJordan/symptoleaf-ai-lab2/pull/5#pullrequestreview-5914533739): comentario sobre README, CONTRIBUTING y plantillas, seguido de aprobación.
- [PR #6: revisiones y correcciones de requisitos](https://github.com/GuamanJordan/symptoleaf-ai-lab2/pull/6).
- [Denise explica la resolución del conflicto](https://github.com/GuamanJordan/symptoleaf-ai-lab2/pull/6#issuecomment-6906183084).
- [Denise explica la corrección de la definición de terminado](https://github.com/GuamanJordan/symptoleaf-ai-lab2/pull/6#issuecomment-6906283469).
- [Mesias explica la corrección del PR #15 y solicita otra revisión](https://github.com/GuamanJordan/symptoleaf-ai-lab2/pull/15#issuecomment-6906847433).
- [PR #15: aprobaciones de Denise y Jordan y fusión](https://github.com/GuamanJordan/symptoleaf-ai-lab2/pull/15).
- [Informe del equipo](https://docs.google.com/document/d/12PHGobasPabb1DHIKRCy9dmgEPLaNXGpOcLCX4HUic8/edit): objetivo de Sprint 2 y captura de sus historias.

**Herramientas de apoyo:** GitHub CLI para consultar revisiones, comentarios, commits e issues; ChatGPT/Codex para organizar y redactar el acta a partir de esa evidencia.
