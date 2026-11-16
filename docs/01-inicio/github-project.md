# Configurar GitHub Projects desde CLI

El repositorio ya acuerda usar GitHub Projects. GitHub CLI es la opción más reproducible para crear el tablero y sus campos; Issues seguirá siendo la fuente de cada historia y Project su vista de planificación.

## Requisitos

1. Instalar GitHub CLI (`gh`) en el equipo.
2. Autenticarse con una cuenta que tenga acceso de escritura al repositorio y al Project:

```powershell
gh auth login
gh auth status
gh auth refresh -s project
```

## Crear y vincular el Project

Ejecutar desde la raíz del repositorio. Si el Project ya existe, listar primero con `gh project list --owner GuamanJordan` y omitir su creación para evitar duplicados.

```powershell
$projectNumber = gh project create --owner GuamanJordan --title "SymptoLeaf-AI · Grupo 3" --format json --jq .number
gh project link $projectNumber --owner GuamanJordan --repo symptoleaf-ai-lab2
```

Guardar el número devuelto para los siguientes comandos. GitHub CLI incluye el campo Status; crear los campos acordados:

```powershell
gh project field-create $projectNumber --owner GuamanJordan --name "Prioridad" --data-type SINGLE_SELECT --single-select-options "Must,Should,Could,Won't"
gh project field-create $projectNumber --owner GuamanJordan --name "Talla" --data-type SINGLE_SELECT --single-select-options "XS,S,M,L,XL"
gh project field-create $projectNumber --owner GuamanJordan --name "Iteración" --data-type SINGLE_SELECT --single-select-options "1,2,3,4,5,6,7,8"
```

## Crear las historias

Los cuerpos listos para cada historia están en `docs/02-requisitos/issues/`. Crear HU-01 a HU-08 como issues del repositorio; `--project` los agrega al Project al momento de crearlos:

```powershell
gh issue create --repo GuamanJordan/symptoleaf-ai-lab2 --title "HU-01 Gestionar cuenta" --body-file docs/02-requisitos/issues/HU-01.md --project "SymptoLeaf-AI · Grupo 3"
```

Repetir por historia, registrar el número real del issue en la matriz y completar responsable e iteración acordada. No crear IDs de issue a mano: GitHub los asigna.

## Comprobación

```powershell
gh project view $projectNumber --owner GuamanJordan
gh project field-list $projectNumber --owner GuamanJordan
gh project item-list $projectNumber --owner GuamanJordan
```

Si la cuenta no tiene alcance `project` o permiso de escritura, detener la creación y solicitar acceso al propietario del repositorio. La cuenta del docente y la fecha de entrega se agregan cuando el equipo las confirme.
