# TypeScript

## Objetivo

Establecer un uso seguro, consistente y expresivo de TypeScript para construir sistemas mantenibles y verificables.

## Alcance

Aplica a toda base de código TypeScript, especialmente a servicios, librerías, routers, entidades de dominio y componentes compartidos.

## Cuándo aplica

Cuando se define un contrato, un DTO, una interfaz, una entidad de negocio o una API pública.

## Principios

- tipado explícito en interfaces públicas,
- unión de tipos y discriminación donde aporten claridad,
- evitar `any` salvo en casos muy justificados,
- preferir inferencia segura y composición de tipos.

## Buenas prácticas

- Definir tipos para DTOs, responses y dominios.
- Usar `unknown` cuando antes no se sabe el formato exacto.
- Documentar tipos complejos y utilidades compartidas.
- Usar `readonly` cuando el valor no debería mutarse.

## Anti-patrones

- `any` por defecto,
- repetir tipos en múltiples clases,
- usar `as` sin necesidad,
- depender de inferencias impredecibles.

## Convenciones

- interfaces para contratos,
- `type` para uniones y alias,
- nombres significativos y consistentes,
- evitar tipos demasiado genéricos sin aportar valor.

## Ejemplos correctos

```ts
export type UserRole = 'admin' | 'member';

export interface UserContext {
  id: string;
  role: UserRole;
}
```

## Ejemplos incorrectos

```ts
function createUser(input: any) {
  return input;
}
```

## Checklist

- ¿El tipo expone intención clara?
- ¿El contrato es específico sin ser rígido?
- ¿Se evitó `any` innecesario?
- ¿El dominio está representado correctamente?

## Definition of Ready

Un tipo o interfaz está listo cuando su intención de uso es clara y el alcance del contrato se conoce.

## Definition of Done

Un tipo se considera completo cuando refuerza la seguridad estática y al mismo tiempo mejora legibilidad del sistema.

## KPIs

- porcentaje de interfaces con tipado explícito,
- número de usos de `any` por componente,
- reducción de errores de runtime por contratos no confiables.

## Métricas

- cantidad de tipos no reutilizados,
- número de inferencias ambiguas,
- tasa de errores difíciles de rastrear por ausencia de typings.

## Herramientas recomendadas

- TypeScript strict mode
- ESLint con reglas estrictas
- TSC en CI

## Librerías recomendadas

- `zod`
- `class-validator`
- `ts-pattern`

## Errores comunes

- usar `any` para acelerar,
- no activar strict mode,
- usar tipos demasiado amplios para evitar trabajo.

## Preguntas frecuentes

- ¿Cuándo usar `unknown`? Cuando el dato viene de un contexto externo y no se sabe su forma exacta.
- ¿Cuándo usar `type` vs `interface`? Usar `interface` para contratos de objetos y `type` para uniones o alias complejos.

## Referencias internas

- [company/engineering-principles.md](../company/engineering-principles.md)
- [react.md](react.md)
- [node.md](node.md)
- [api.md](api.md)
