# Backlog inicial de historias

Se adoptan los identificadores estables HU-01 a HU-08 porque coinciden con el backlog del Taller 2 y cubren las ocho funciones F1-F8 del acta. Estos son IDs del producto; los números de issue serán los que asigne GitHub.

| ID | Historia | F | Prioridad inicial | Iteración de referencia | RF / CU |
|---|---|---|---|---|---|
| HU-01 | Como usuario, quiero crear cuenta, iniciar o cerrar sesión y consultar mi perfil para acceder de forma protegida. | F1 | Must | 2; integrar en 6 | RF1; CU01-CU03, CU12 |
| HU-02 | Como usuario, quiero tomar una fotografía con la cámara para analizar una hoja. | F2 | Must | 2 | RF2; CU14-CU15 |
| HU-03 | Como usuario, quiero seleccionar una fotografía existente para analizar una hoja. | F3 | Must | 2 | RF3; CU14, CU16 |
| HU-04 | Como usuario, quiero validar y clasificar una hoja localmente para obtener una orientación aun sin conexión. | F4 | Must | 3 | RF4-RF5; CU04, CU13 |
| HU-05 | Como usuario, quiero comprender el resultado y su confianza para interpretar los límites de la clasificación. | F5 | Must | 3 | RF6; CU04-CU05 |
| HU-06 | Como usuario, quiero recibir orientación de cuidados para el resultado seleccionado. | F6 | Should | 5 | RF7; CU05-CU06 |
| HU-07 | Como usuario, quiero conversar con el asistente sobre mi planta y diagnóstico. | F7 | Should | 5 | RF8; CU06 |
| HU-08 | Como usuario, quiero guardar, consultar y eliminar mis casos, y consultar conversaciones propias. | F8 | Must | 4-5 | RF9-RF10; CU07-CU11 |

Las prioridades e iteraciones son la planificación de referencia del Taller 2, no issues creados ni un compromiso actualizado de Sprint. El equipo debe confirmarlas en GitHub Projects antes de asignarlas. Tallas y responsables se dejan por estimar con el equipo.

## Criterios de aceptación base

### HU-01 Gestionar cuenta

- **Dado** un usuario con credenciales válidas, **cuando** inicia sesión, **entonces** accede a su cuenta y a su perfil.
- **Dado** un registro o inicio de sesión con datos inválidos, **cuando** lo envía, **entonces** recibe un error claro y no se concede acceso.
- **Dado** un usuario autenticado, **cuando** cierra sesión, **entonces** la sesión deja de estar disponible en la aplicación.

### HU-02 Tomar fotografía

- **Dado** que la cámara está disponible y el permiso fue concedido, **cuando** el usuario captura una imagen, **entonces** la aplicación obtiene una fotografía para analizar.
- **Dado** que el permiso fue denegado o la captura se cancela, **cuando** finaliza la acción, **entonces** la aplicación informa el estado y permite reintentar.

### HU-03 Seleccionar fotografía

- **Dado** que hay imágenes disponibles en el dispositivo, **cuando** el usuario selecciona una imagen admitida, **entonces** la aplicación la entrega al flujo de análisis.
- **Dado** que el usuario cancela la selección, **cuando** vuelve a la aplicación, **entonces** no se crea un diagnóstico.

### HU-04 Validar y clasificar

- **Dado** una imagen legible de una hoja dentro del catálogo admitido, **cuando** el usuario solicita el análisis, **entonces** la clasificación local devuelve una categoría estimada.
- **Dado** una imagen ilegible, incompatible o sin una hoja reconocible, **cuando** se valida, **entonces** se rechaza sin generar diagnóstico.
- **Dado** que el modelo local no está disponible, **cuando** se solicita el análisis, **entonces** se informa el fallo sin inventar una predicción.

### HU-05 Comprender resultado

- **Dado** un análisis completado, **cuando** el usuario consulta el resultado, **entonces** ve categoría, confianza y explicación en español como orientación, no diagnóstico definitivo.
- **Dado** un resultado incierto o fuera del catálogo, **cuando** se presenta, **entonces** se muestra la limitación o un resultado no concluyente.

### HU-06 Solicitar cuidados

- **Dado** un resultado y conexión disponible, **cuando** el usuario solicita cuidados, **entonces** recibe orientación asociada a ese resultado.
- **Dado** que el servicio remoto no responde o no hay conexión, **cuando** se solicita orientación, **entonces** se informa la indisponibilidad y se conserva el resultado local.

### HU-07 Conversar con asistente

- **Dado** un diagnóstico seleccionado y conexión disponible, **cuando** el usuario envía una pregunta, **entonces** recibe una respuesta contextual asociada al caso.
- **Dado** que el servicio de conversación falla, **cuando** se envía el mensaje, **entonces** la aplicación comunica el error y permite reintentar sin duplicar el mensaje.

### HU-08 Gestionar historial propio

- **Dado** un resultado y un usuario autenticado, **cuando** decide guardarlo, **entonces** queda asociado a su cuenta.
- **Dado** que existen registros propios, **cuando** el usuario consulta el historial, **entonces** solo ve sus diagnósticos y conversaciones guardados.
- **Dado** un registro propio seleccionado, **cuando** confirma su eliminación, **entonces** deja de aparecer en su historial.
- **Dado** otro usuario autenticado, **cuando** intenta consultar o eliminar ese registro, **entonces** la operación se deniega.

Los criterios son una normalización inicial basada en los requisitos y casos de uso suministrados. Jordan y Mesias deben revisar la trazabilidad exacta y el alcance técnico antes de crear los issues definitivos.
