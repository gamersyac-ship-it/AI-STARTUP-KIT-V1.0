# Clean Code

## Objetivo

Aplicar principios de legibilidad, mantenibilidad y responsabilidad clara para que el código sea comprensible por equipos y por herramientas de revisión automatizada.

## Alcance

Este estándar aplica a cualquier proyecto que use código fuente mantenible, testable y compartible en equipos profesionales.

## Cuándo aplica

Cuando se escribe lógica comercial, servicios, componentes, utilidades, endpoints, validaciones o cualquier flujo nuevo.

## Principios

- SOLID
- DRY
- KISS
- YAGNI
- Boy Scout Rule
- responsabilidad única
- legibilidad por encima de cleverness

## Buenas prácticas

- Dividir funciones por responsabilidad.
- Nombrar variables con intención clara.
- Preferir estructuras pequeñas y predecibles.
- Refactorizar cuando el código empiece a esconder lógica.
- Mantener la complejidad del flujo comprensible.

## Anti-patrones

- funciones gigantes,
- nombres vagos,
- lógica duplicada,
- condicionales anidados excesivos,
- ocultar errores con fallbacks silenciosos.

## Convenciones

- Nombre de función expresa intención.
- El cuerpo de una función debe cumplir una sola tarea clara.
- Usar comentarios solo cuando el comportamiento no se puede expresar en el código.

## Ejemplos correctos

```ts
function createUserProfile(user: User): UserProfile {
  return {
    id: user.id,
    role: user.role,
    isActive: user.isActive,
  };
}
```

## Ejemplos incorrectos

```ts
function doStuff(data: any) {
  // lógica difícil de seguir
  if (data.a) {
    if (data.b) {
      if (data.c) {
        // demasiado complejo
      }
    }
  }
}
```

## Checklist

- ¿La función es pequeña y clara?
- ¿La variable expresa intención?
- ¿Existe lógica duplicada?
- ¿Puede leerse sin contexto adicional?

## Definition of Ready

Un cambio de código está listo cuando la intención del comportamiento está clara y su alcance es verificable.

## Definition of Done

Un cambio de código se considera completo cuando el flujo es legible, sigue el patrón elegido y puede ser revisado sin ambigüedad.

## KPIs

- tasa de PRs con comentarios de legibilidad,
- número de cambios con refactorización innecesaria,
- reducción de tiempo de comprensión del módulo.

## Métricas

- complejidad ciclomatica de funciones clave,
- tiempos de lectura y revisión,
- tasa de rework por mala comprensión.

## Herramientas recomendadas

- ESLint
- Prettier
- SonarQube
- code review con criterios de claridad y mantenibilidad

## Librerías recomendadas

- no aplica directamente; se prioriza el diseño.

## Errores comunes

- escribir para “estar bonito” y no para ser comprendido,
- abstraer demasiado pronto,
- dejar el código sin estructura clara.

## Preguntas frecuentes

- ¿Cuándo refactorizar? Cuando el comportamiento ya está cubierto y se observa que el código está ocultando intención.
- ¿Qué pasa si hay duplicación útil? Debe justificarse con un contexto real y no permanecer sin un patrón de reúso.

## Referencias internas

- [company/engineering-principles.md](../company/engineering-principles.md)
- [clean-architecture.md](clean-architecture.md)
- [code-style.md](code-style.md)
