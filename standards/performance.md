# Performance

## Objetivo

Definir un enfoque sostenible para construir software con tiempos de respuesta, uso de recursos y experiencia de usuario adecuados a la necesidad del negocio.

## Alcance

Aplica a frontend, API, queries, infraestructura, middleware, bases de datos y cualquier flujo con impacto en latencia o consumo.

## Cuándo aplica

Cuando existe riesgo de latencia, carga excesiva, consultas lentas, problemas de render o de uso de memoria.

## Principios

- medir para mejorar,
- optimizar en los puntos correctos,
- evitar optimizaciones prematuras,
- priorizar experiencia del usuario y confiabilidad del servicio.

## Buenas prácticas

- Prefieren arquitectura eficiente por diseño a micro-optimizaciones.
- Reducir llamadas innecesarias y payloads excesivos.
- Usar lazy loading, cache y batching donde aplique.
- Medir consultas, render y bottlenecks en producción y no solo en desarrollo.

## Anti-patrones

- cargar demasiado al inicio,
- hacer consultas sin filtro ni paginación,
- optimizar sin medir,
- usar caché sin estrategia clara.

## Convenciones

- cada flujo crítico debe tener un criterio de rendimiento verificable,
- las decisiones de performance deben quedar documentadas cuando afectan a la experiencia,
- se deben definir alertas y observabilidad relevantes.

## Ejemplos correctos

```ts
const query = await db.user.findMany({
  take: 20,
  orderBy: { createdAt: 'desc' },
});
```

## Ejemplos incorrectos

```ts
const users = await db.user.findMany();
```

## Checklist

- ¿Hay medición del flujo crítico?
- ¿Se usa caché o lazy loading cuando aplica?
- ¿Existen límites de paginación y filtros?
- ¿La carga de la UI o endpoint está alineada con el SLA necesario?

## Definition of Ready

La optimización está lista cuando se conoce el hotspot, la métrica objetivo y el impacto esperado.

## Definition of Done

Un cambio de performance se considera terminado cuando la mejora queda validada con evidencia y no compromete mantenibilidad ni seguridad.

## KPIs

- latencia p95,
- tasa de consultas lentas,
- tiempo de interacción en UI,
- uso de CPU y memoria por servicio.

## Métricas

- tiempo de carga inicial,
- rate de requests por endpoint,
- tamaño de bundle,
- número de consultas N+1.

## Herramientas recomendadas

- Lighthouse
- Postman/Newman
- profiling tools del runtime
- observabilidad con dashboarding

## Librerías recomendadas

- React Query / TanStack Query
- profiling y monitoring tools de runtime

## Errores comunes

- optimizar sin basar la decisión en datos,
- sacrificar claridad por rendimiento sin planificación,
- no medir el costo real del cambio.

## Preguntas frecuentes

- ¿Cuándo optimizar? Cuando el problema ya es medible y real.
- ¿Cuándo no optimizar? Cuando la mejora habría sido prematura o no aporta valor medible.

## Referencias internas

- [react.md](react.md)
- [api.md](api.md)
- [database.md](database.md)
- [testing.md](testing.md)
