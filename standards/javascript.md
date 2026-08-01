# JavaScript

## Objetivo

Mantener un estándar de calidad para aplicaciones JavaScript donde el uso de TypeScript no sea obligatorio o donde se necesite compatibilidad de runtime.

## Alcance

Este estándar aplica a scripts, utilidades, módulos frontend o backend en JavaScript puro.

## Cuándo aplica

Cuando una base de código usa JavaScript sin tipado fuerte o necesita ser compatible con runtimes específicos.

## Principios

- legibilidad por encima de cleverness,
- comportamiento explícito,
- manejo seguro de edge cases,
- consistencia de estilo y convención.

## Buenas prácticas

- Usar sintaxis moderna cuando el runtime lo permita.
- Evitar coerción implícita.
- Sacar utilidad repetida a funciones pequeñas y reutilizables.
- Mantener efectos laterales mínimos y claros.

## Anti-patrones

- `==` para comparaciones,
- mutations silenciosas,
- expresiones demasiado compactas,
- lógica profundamente anidada.

## Convenciones

- nombrar funciones con intención clara,
- mantener archivos cortos y con una responsabilidad identificable,
- evitar funciones demasiado largas.

## Ejemplos correctos

```js
function normalizeEmail(email) {
  return email.trim().toLowerCase();
}
```

## Ejemplos incorrectos

```js
if (user.role == 1) {
  // implicit coercion
}
```

## Checklist

- ¿La función es estable y predecible?
- ¿La lógica es legible?
- ¿Se evitó coerción implícita?
- ¿Se documenta el caso de borde necesario?

## Definition of Ready

Un módulo JavaScript está listo si el comportamiento previsto está claro y la dependencias de runtime son conocidas.

## Definition of Done

Un módulo JavaScript se considera completado si puede mantenerse, revisarse y probarse sin ambigüedad.

## KPIs

- tasa de errores por coerción o interpretación implícita,
- cantidad de funciones con complejidad innecesaria,
- tiempo de revisión y comprensión del archivo.

## Métricas

- número de archivos con más de una responsabilidad,
- número de funciones largas,
- tasa de bugs por comportamiento ambiguo.

## Herramientas recomendadas

- ESLint
- Prettier
- Node.js runtime aware linting

## Librerías recomendadas

- dependencias de validación o utilidades con buena reputación y mantenimiento activo.

## Errores comunes

- escribir código con demasiada magia,
- depender de inferencia de runtime poco clara,
- no revisar compatibilidad del runtime elegido.

## Preguntas frecuentes

- ¿Cuándo usar JavaScript en vez de TypeScript? Cuando el proyecto o runtime no necesitan el tipado fuerte y se prioriza compatibilidad simple.
- ¿Se puede usar JS en producción? Sí, pero con disciplina de estilo y más pruebas de validación.

## Referencias internas

- [typescript.md](typescript.md)
- [clean-code.md](clean-code.md)
- [code-style.md](code-style.md)
