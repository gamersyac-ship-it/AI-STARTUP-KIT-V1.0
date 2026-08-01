# Naming

## Objetivo

Establecer convenciones de nomenclatura que hagan el sistema claro, consistente y fácil de mantener.

## Alcance

Aplica a archivos, APIs, variables, componentes, ramas, DTOs, entidades, servicios y cualquier artefacto que deba ser entendido por equipo.

## Cuándo aplica

Siempre que un nombre se use para describir una responsabilidad, dominio o flujo de trabajo.

## Principios

- nombres expresivos,
- consistencia entre capas,
- evitar abreviaturas ambiguas,
- reflejar intención y dominio.

## Buenas prácticas

- Usar `camelCase` para variables y funciones en JS/TS.
- Usar `PascalCase` para componentes.
- Usar `kebab-case` para nombres de rutas o archivos donde sea natural.
- Preferir nombres basados en dominio y no en la tecnología.

## Anti-patrones

- `data`, `stuff`, `misc`, `thing`, `handler` sin contexto,
- abreviaturas no estandarizadas,
- nombres que describen cómo se implementa en lugar de qué representa.

## Convenciones

- `feature/*` para trabajo de producto,
- `useX` para hooks,
- `UserRepository` para repositorios,
- `createUser` para operaciones explícitas.

## Ejemplos correctos

```ts
const userSession = getUserSession();
```

## Ejemplos incorrectos

```ts
const data = getThing();
```

## Checklist

- ¿El nombre comunica intención?
- ¿Es consistente con el resto del sistema?
- ¿Evita ambigüedad?
- ¿Se puede comprender sin contexto extra?

## Definition of Ready

Una convención de naming está lista cuando el nombre del artefacto no permite otra interpretación probable.

## Definition of Done

El naming queda consistente cuando un nuevo integrante puede inferir el propósito del artefacto con mínima ayuda.

## KPIs

- tiempo de lectura y entendimiento de módulos,
- porcentaje de nombres ambiguos detectados en review,
- tasa de re-nombrado por ausencia de convenios.

## Métricas

- cantidad de archivos con nombres vagos,
- número de PRs con cambios de nomenclatura,
- número de comentarios sobre ambigüedad de names.

## Herramientas recomendadas

- ESLint naming rules
- code review checklist
- linting de import paths y naming

## Librerías recomendadas

- reglas de eslint y tsconfig donde aplique.

## Errores comunes

- usar acrónimos sin definirlos,
- mantener nombres técnicos por comodidad,
- no documentar la convención para nuevos integrantes.

## Preguntas frecuentes

- ¿Qué pasa si el nombre es demasiado largo? Es mejor un nombre claro que uno corto pero confuso.
- ¿Debo renombrar un símbolo ya en uso? Sí, si el nombre está creando ambigüedad o contradice el dominio.

## Referencias internas

- [clean-code.md](clean-code.md)
- [documentation.md](documentation.md)
- [code-style.md](code-style.md)
