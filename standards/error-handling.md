# Error Handling

## Objetivo

Establecer un manejo de errores predecible, seguro y consistente para cualquier capa de software.

## Alcance

Aplica a APIs, servicios, workflows, interfaces y procesos de integración.

## Cuándo aplica

Cuando se expone un error al usuario, al sistema o a otra dependencia del sistema.

## Principios

- clasificar el error correctamente,
- no ocultar fallas,
- usar respuestas consistentes,
- mantener trazabilidad,
- preservar seguridad y contexto.

## Buenas prácticas

- Diferenciar error de negocio y error técnico.
- Usar códigos legibles y estables.
- Evitar exponer detalles internos a clientes no autorizados.
- Registrar el error con contexto y correlación.

## Anti-patrones

- devolver errores genéricos que no permiten actuar,
- hacer swallow exceptions,
- exponer stack traces a usuarios,
- mezclar errores de negocio con infraestructura.

## Convenciones

- errors de negocio deben producir mensajes claros y accionables,
- errors técnicos deben dejar evidencia y logging estructurado,
- responses HTTP deben seguir un contrato estándar.

## Ejemplos correctos

```json
{
  "error": {
    "code": "VALIDATION_FAILED",
    "message": "One or more fields are invalid.",
    "details": [
      { "field": "email", "issue": "must be a valid email" }
    ]
  }
}
```

## Ejemplos incorrectos

```json
{
  "message": "Something went wrong"
}
```

## Checklist

- ¿El tipo de error está bien clasificado?
- ¿El mensaje es útil para el consumidor correcto?
- ¿Se registró el contexto suficiente?
- ¿La respuesta sigue el contrato esperado?

## Definition of Ready

Un control de errores está listo cuando el flujo y el tipo de fallo están conocidos y el comportamiento esperado está definido.

## Definition of Done

Un control de errores se considera completo cuando el cliente o consumidor recibe una respuesta útil, segura y consistente.

## KPIs

- tasa de errores no mapeados,
- tasa de incidentes por falta de validación,
- proporción de errores con respuesta consistente.

## Métricas

- distribución de errores por tipo,
- tiempo de mitigación,
- tasa de retries por error recuperable.

## Herramientas recomendadas

- error boundaries en frontend,
- middleware centralizado en backend,
- tracking de error IDs y correlación.

## Librerías recomendadas

- framework-specific exception middlewares,
- error normalization libraries,
- logging adapters.

## Errores comunes

- no distinguir errores esperados y no esperados,
- duplicar mensajes de programación en producción,
- permitir mensajes internos a clientes.

## Preguntas frecuentes

- ¿Qué debe exponerse al cliente? Solo lo necesario para actuar o entender el error.
- ¿Cuándo usar excepciones? Cuando el flujo no puede continuar de forma segura.

## Referencias internas

- [api.md](api.md)
- [logging.md](logging.md)
- [security.md](security.md)
