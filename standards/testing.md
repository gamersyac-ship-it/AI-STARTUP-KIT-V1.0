# Testing

## Objetivo

Asegurar que el software se valide con evidencia real, no con suposiciones, y que las entregas principales se puedan probar con confianza.

## Alcance

Aplica a unit tests, integration tests, E2E, pruebas de seguridad, pruebas de performance y validación de calidad de release.

## Cuándo aplica

Cuando se valida lógica de negocio, API, UI, integraiones, seguridad, regresiones o flujos críticos.

## Principios

- testear comportamiento real,
- usar mocks con criterio y no por defecto,
- validar casos de borde,
- proteger la regresión,
- mantener pruebas mantenibles y comprensibles.

## Buenas prácticas

- Unit Testing para lógica aislada.
- Integration Testing para contratos y dependencias.
- E2E para escenarios reales de usuario.
- Usar fixtures, test data y setup reproducible.
- Mantener cobertura en paths críticos de negocio.

## Anti-patrones

- testear mocks en lugar del comportamiento,
- cubrir solo el happy path,
- duplicar lógica de setup en múltiples suites,
- usar fixtures muy frágiles.

## Convenciones

- pruebas con nombres descriptivos,
- asserts de comportamiento y no de implementación,
- separar test data por escenario,
- evolucionar la suite junto al código.

## Ejemplos correctos

```ts
it('returns 401 when token is missing', async () => {
  const res = await request(app).get('/v1/profile');
  expect(res.status).toBe(401);
});
```

## Ejemplos incorrectos

```ts
it('calls mocked method once', () => {
  expect(mockFn).toHaveBeenCalledTimes(1);
});
```

## Checklist

- ¿La prueba valida comportamiento real?
- ¿Hay evidencia de regresión?
- ¿Hay tests en flujos críticos?
- ¿Se valida el error-case además del happy-path?

## Definition of Ready

Una prueba está lista cuando el comportamiento, el escenario y el criterio de validación son claros.

## Definition of Done

La prueba se considera completa cuando el flujo está validado con evidencia y queda como protección para futuras entregas.

## KPIs

- cobertura en rutas críticas,
- número de defectos detectados antes de release,
- reducción de regresiones por release.

## Métricas

- cobertura de unit/integration/E2E,
- tiempo de ejecución de suite,
- tasa de flakiness de pruebas.

## Herramientas recomendadas

- Jest/Vitest
- Playwright/Cypress
- Testing Library
- Pact o similar para contratos

## Librerías recomendadas

- `@testing-library/react`
- `supertest`
- `vitest`
- `playwright`

## Errores comunes

- validar mocks en vez del comportamiento,
- no cubrir escenarios de error,
- tener suites de pruebas demasiado lentas o frágiles.

## Preguntas frecuentes

- ¿Cuántas pruebas son suficientes? Aquellas que cubran la lógica crítica y la regresión del flujo más sensible.
- ¿Qué hacer con un bug reportado? Añadir prueba que reproduzca el fallo antes de corregirlo.

## Referencias internas

- [company/workflow.md](../company/workflow.md)
- [company/release-policy.md](../company/release-policy.md)
- [react.md](react.md)
- [api.md](api.md)
