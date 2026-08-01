# Code Style

## Objetivo

Asegurar que el código escrito en el framework sea consistente, legible y fácil de revisar.

## Alcance

Aplica a todos los lenguajes, módulos y archivos de código fuente que se mantengan en la base del proyecto.

## Cuándo aplica

En todo archivo que sea leído, revisado, extendido o mantenido por más de una persona.

## Principios

- estilo consistente,
- formato automatizado,
- legibilidad y previsibilidad,
- import order claro,
- menos ruido y más intención.

## Buenas prácticas

- Usar Prettier o equivalent formatter.
- Indentación consistente por lenguaje y configuración.
- Mantener archivos y funciones de tamaño razonable.
- Ordenar imports por dominio y tipo.
- Evitar comentarios redundantes.

## Anti-patrones

- formato inconsistente por editor,
- imports desordenados,
- líneas demasiado largas,
- archivos sin una guía clara de estilo.

## Convenciones

- un formato consistente para todo el repositorio,
- comentarios solo cuando clarifican un motivo o decisión no obvia,
- separación clara entre imports, constantes y lógica.

## Ejemplos correctos

```ts
import { createUser } from './user';

export function saveUser() {
  return createUser();
}
```

## Ejemplos incorrectos

```ts
import './user';
import {createUser} from './user'
```

## Checklist

- ¿El archivo está formateado?
- ¿Los imports están ordenados?
- ¿Las funciones son pequeñas?
- ¿El código mantiene una estructura clara?

## Definition of Ready

Un estilo está listo cuando la forma de escribir, revisar y formatear el código se mantiene uniforme en el equipo.

## Definition of Done

El estilo se considera adoptado cuando el código puede revisarse y mantenerse con mínimo fricción por la anormalidad del formato.

## KPIs

- tasa de reformatting en review,
- inconsistencias de estilo por PR,
- número de comentarios por formato.

## Métricas

- median time to review,
- cantidad de archivos con formato no uniforme,
- cantidad de comentarios por estilo en review.

## Herramientas recomendadas

- Prettier
- ESLint
- editorconfig

## Librerías recomendadas

- dependencias de formateo y linting según runtime.

## Errores comunes

- depender del estilo de cada desarrollador,
- mezclar un estilo con otro sin aplicar configuración común,
- comentar cada línea en lugar de explicar decisiones.

## Preguntas frecuentes

- ¿Qué pasa si el estilo no se aplica? Se vuelve una fuente de fricción constante y reducción de productividad.
- ¿Debe usarse siempre un formatter? Sí, la base operativa del repositorio debe ser predecible.

## Referencias internas

- [clean-code.md](clean-code.md)
- [documentation.md](documentation.md)
- [naming.md](naming.md)
