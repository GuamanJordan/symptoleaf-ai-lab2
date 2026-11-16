# Contribuir a SymptoLeaf-AI

1. Toma un issue asignado por Jordan y pásalo a En progreso. Mantén un máximo de dos issues simultáneos en ese estado.
2. Actualiza main con git pull --ff-only origin main. Crea una rama tipo/número-descripción, por ejemplo docs/12-inicio-y-requisitos.
3. Haz commits con el formato tipo: descripción en presente (#issue). Sube la rama con git push -u origin HEAD.
4. Abre el PR con gh pr create, base main y Closes #N. Pasa el issue a En revisión.
5. Solicita revisión a otro integrante. Jordan acepta y fusiona los PR de Denise y Mesias. Para el PR de colaboración de Jordan, Mesias aprueba y Denise fusiona.
6. Responde observaciones en el PR y sube nuevos commits. Repite la revisión si cambió el diff. Integra por squash y confirma el estado Hecho.
7. Cambia los documentos del curso mediante PR revisado. Desde la semana 5, registra las pruebas aplicables en el PR.

## Definición de terminado

- [ ] El PR enlaza un issue con Closes #N y cumple sus criterios de aceptación.
- [ ] La rama, los commits y el título del PR siguen las convenciones.
- [ ] La documentación afectada está actualizada, cuando aplica.
- [ ] Desde la semana 5, se ejecutaron y pasaron las pruebas aplicables.
- [ ] Otro integrante dejó un comentario y el responsable de aceptación aprobó el PR después de resolver los hilos.
- [ ] El cambio entró por squash y el issue vinculado quedó en Hecho.
