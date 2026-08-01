# Git

## Objetivo

Definir un modelo de control de versiones profesional para coordinación, trazabilidad y prevención de conflictos en equipos reales.

## Alcance

Aplica a ramas, commits, PRs, rebase, merge y tags del repositorio.

## Cuándo aplica

En todo cambio de código o documentación dentro del repositorio.

## Principios

- historial legible,
- cambios atómicos,
- review real,
- branches con intención clara,
- versiones discretas y comprobables.

## Buenas prácticas

- Usar Conventional Commits.
- Hacer commits pequeños y entendibles.
- Mantener branches cortas y enfocadas.
- Usar PRs con revisión y evidencia de validación.
- Versionar releases con tags claros.

## Anti-patrones

- commits gigantes con mezclas no relacionadas,
- ramas largas y sin propósito,
- merge sin revisión,
- mensajes como “update” o “fix bug”.

## Convenciones

- commit message con `type(scope): subject`,
- branch naming descriptivo,
- PR con resumen, cambios y validación,
- tags asociados a versión semántica.

## Ejemplos correctos

```bash
git commit -m "feat(api): add user profile endpoint"
```

## Ejemplos incorrectos

```bash
git commit -m "update"
```

## Checklist

- ¿El commit describe intent?
- ¿La PR tiene evidencia de validación?
- ¿La rama tiene un propósito claro?
- ¿La release o versión se alinea con el tag correcto?

## Definition of Ready

Una rama está lista cuando el propósito, la dependencia y el alcance del cambio están claros.

## Definition of Done

Un cambio queda listo cuando el historial, el PR y la evidencia de validación permiten entender exactamente qué se entregó.

## KPIs

- número de PRs revisados dentro del SLA,
- frecuencia de merge sin revisión,
- tasa de commits con mensajes ambiguos.

## Métricas

- tiempo medio de revisión,
- cantidad de ramas vivas demasiado largas,
- número de conflictos por naming o falta de limpieza.

## Herramientas recomendadas

- GitHub/GitLab/Azure DevOps
- Conventional Commits tooling
- PR review enforcement
- git hooks

## Librerías recomendadas

- Commitlint
- Husky
- semantic-release

## Errores comunes

- no revisar cambios de manera formal,
- usar ramas con nombres muy genéricos,
- hacer rebase sin control de impacto.

## Preguntas frecuentes

- ¿Cuándo usar rebase? Solo cuando el equipo entiende el impacto en el historial y la colaboración.
- ¿Cuándo usar merge? En la mayoría de flujos de equipo, especialmente cuando se quiere preservar un historial claro.

## Referencias internas

- [company/branching-strategy.md](../company/branching-strategy.md)
- [company/release-policy.md](../company/release-policy.md)
- [company/workflow.md](../company/workflow.md)
