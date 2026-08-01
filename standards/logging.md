# Logging

## Objetivo

Garantizar trazabilidad, observabilidad y diagnóstico de errores sin comprometer seguridad ni legibilidad operativa.

## Alcance

Aplica a aplicaciones backend, APIs, servicios, pipelines y procesos operativos relevantes.

## Cuándo aplica

Cuando se registra actividad de negocio, errores, eventos de integración, cambios de estado, seguridad o diagnósticos operativos.

## Principios

- logs estructurados,
- trazabilidad de operación,
- no loggear secretos,
- evidenciar el contexto y la causa,
- separar logs de negocio y de operación.

## Buenas prácticas

- Usar IDs de correlación y request IDs. 
- Registrar intent, contexto, resultado y entidad afectada.
- Mantener niveles consistentes: debug, info, warn, error.
- Usar JSON o formato estructurado cuando la plataforma lo permita.

## Anti-patrones

- logs libres y sin contexto,
- imprimir secretos o tokens,
- registrar PII o información sensible,
- usar logs como almacenamiento temporal de negocio.

## Convenciones

- Nivel adecuado al evento.
- Mensaje claro, específico y operable.
- Campos estándar para request, usuario, scope y error code.

## Ejemplos correctos

```json
{
  "level": "error",
  "service": "auth-api",
  "requestId": "7e1d4f",
  "userId": "u_123",
  "message": "Failed to validate session token",
  "errorCode": "AUTH_INVALID_TOKEN"
}
```

## Ejemplos incorrectos

```text
ERROR token=abcd1234 user=Sebastian
```

## Checklist

- ¿Se registra el contexto suficiente?
- ¿Se omiten secretos y datos sensibles?
- ¿Se usa un ID de correlación?
- ¿Se mantiene consistencia de niveles?

## Definition of Ready

El registro está listo cuando la operación a documentar y el nivel de importancia están definidos claramente.

## Definition of Done

El registro se considera completo cuando aporta contexto útil para diagnóstico y no compromete seguridad.

## KPIs

- tiempo medio de diagnóstico,
- tasa de logs no estructurados,
- resolución de incidentes con trazabilidad.

## Métricas

- volumen de logs por operación,
- número de eventos sin requestId,
- tasa de errores mal clasificados.

## Herramientas recomendadas

- OpenTelemetry
- Pino
- Winston
- Serilog
- Loki + Grafana

## Librerías recomendadas

- structured loggers para Node, Python, Go o Java según el runtime.

## Errores comunes

- registrar demasiada información irrelevante,
- usar logs de debugging en producción,
- usar texto libre en lugar de esquema estructurado.

## Preguntas frecuentes

- ¿Qué se debe registrar? Lo necesario para diagnosticar el flujo, no todo el contenido del sistema.
- ¿Se deben registrar todos los errores? Sí, pero con una clasificación apropiada y contexto operacional.

## Referencias internas

- [security.md](security.md)
- [error-handling.md](error-handling.md)
- [company/incident-management.md](../company/incident-management.md)
