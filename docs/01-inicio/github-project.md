# GitHub Projects del equipo

El equipo ya tiene un Project y no debe crear otro. El tablero existente **SymptoLeaf-AI - Proceso del equipo** es el Project #1 de `GuamanJordan` y está vinculado a `GuamanJordan/symptoleaf-ai-lab2`.

- Project: <https://github.com/users/GuamanJordan/projects/1>
- Repositorio: <https://github.com/GuamanJordan/symptoleaf-ai-lab2>
- Issues incluidos al validar: #1 Archivos de colaboración, #2 Inicio y requisitos, #3 Modelado y proceso, #4 Retrospectiva del Sprint 1.

## Campos existentes

El tablero ya cuenta con los campos necesarios, así que no se deben duplicar:

- `Status`: Backlog, Por hacer, En progreso, En revisión y Hecho.
- `Prioridad`: Must, Should, Could y Won't.
- `Talla`: XS, S, M, L y XL.
- `Sprint`: campo de iteración de 14 días, con el Sprint 1 ya creado.

## Consultar y mantener el Project por CLI

Usa una versión reciente de GitHub CLI y una sesión de `DeniseRea` con acceso al repo y al Project:

```powershell
gh auth status
gh project list --owner GuamanJordan --limit 100 --format json
gh project view 1 --owner GuamanJordan --format json
gh project field-list 1 --owner GuamanJordan --limit 100 --format json
gh project item-list 1 --owner GuamanJordan --limit 100 --format json
```

Para comprobar el vínculo formal del Project al repositorio:

```powershell
gh api graphql -f query='query { user(login: "GuamanJordan") { projectV2(number: 1) { repositories(first: 100) { nodes { nameWithOwner } } } } }'
```

Al abrir un PR, pasar el issue correspondiente a `En revisión`:

```powershell
gh project item-edit 1 --owner GuamanJordan --url https://github.com/GuamanJordan/symptoleaf-ai-lab2/issues/2 --field Status --value "En revisión"
```

## Crear las historias HU-01 a HU-08

Las ocho fichas con criterios están en `docs/02-requisitos/issues/`. Jordan crea y asigna los Issues definitivos según el acuerdo del equipo. GitHub asigna los números de issue; no reutilizar los IDs HU como números de issue.

Ejemplo para crear una historia y añadirla al Project existente en el mismo paso:

```powershell
gh issue create --repo GuamanJordan/symptoleaf-ai-lab2 --title "HU-01 Gestionar cuenta" --body-file docs/02-requisitos/issues/HU-01.md --project "SymptoLeaf-AI - Proceso del equipo"
```

Repetir para HU-02 a HU-08. Luego completar en el Project responsable, prioridad, talla y Sprint acordados. Las prioridades e iteraciones de `historias.md` son referencias del plan; el equipo debe conciliarlas antes de asignarlas.
