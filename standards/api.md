# API

## Objetivo

Definir un estándar de diseño y entrega para APIs seguras, versionables, documentadas y fáciles de mantener.

## Alcance

Aplica a servicios HTTP/REST, endpoints de dominio, contratos de integración y uso de OpenAPI/Swagger.

## Cuándo aplica

Cuando se diseña una API para frontend, terceros, servicios internos o integraciones externas.

## Principios

- REST claro y consistente,
- versionado explícito,
- respuestas seguras y consistentes,
- autenticación y autorización en el borde,
- idempotencia cuando el flujo lo exige.

## Buenas prácticas

- Usar endpoints semánticos y HTTP status apropiados.
- Definir paginación, filtros y ordenamiento de forma consistente.
- Documentar errores y contratos en OpenAPI.
- Definir rate limiting y límites de uso en APIs expuestas.
- Preservar idempotencia para operations sensibles o reintentos.

## Anti-patrones

- mezclar responsabilidades de API y negocio,
- usar verbos en el endpoint,
- no documentar errores,
- exponer metadata interna en respuestas.

## Convenciones

- los errores siguen un contrato estándar,
- los paths son estables y versionados,
- parámetros de consulta formateados de forma uniforme,
- respuestas con payloads claros y previsibles.

## Ejemplos correctos

```http
GET /v1/users?page=1&limit=20&sort=name
```

## Ejemplos incorrectos

```http
GET /api/getUsersData
```

## Checklist

- ¿La API está versionada?
- ¿Los errores son predecibles?
- ¿Los endpoints son consistentes con el dominio?
- ¿Hay documentación de OpenAPI o Swagger?

## Definition of Ready

Una API está lista cuando el contrato, los métodos, las respuestas y los permisos están definidos con claridad.

## Definition of Done

Una API queda lista cuando cumple contrato, seguridad, trazabilidad y documentación suficiente para consumo y mantenimiento.

## KPIs

- tiempo de integración por parte de consumidores,
- reducción de errores de contrato,
- tasa de errores 4xx/5xx por uso incorrecto.

## Métricas

- latencia por endpoint,
- número de endpoints no versionados,
- tasa de reintentos por idempotencia no tratada.

## Herramientas recomendadas

- OpenAPI/Swagger
- Postman/Newman
- Redocly
- rate limiters y API gateways

## Librerías recomendadas

- `zod`
- `class-validator`
- `swagger-ui-express`
- `openapi-typescript`

## Errores comunes

- no versionar cambios importantes,
- usar GET con side effects,
- falta de paginación y filtros,
- controlar autenticación y autorización solo en frontend.

## Preguntas frecuentes

- ¿Cuándo versionar? Cuando un cambio rompe compatibilidad o cambia el contrato del endpoint.
- ¿Qué es idempotencia? La capacidad de ejecutar una operación varias veces sin cambiar el resultado más allá del efecto esperado.

## Referencias internas

- [company/engineering-principles.md](../company/engineering-principles.md)
- [security.md](security.md)
- [database.md](database.md)
- [testing.md](testing.md)
