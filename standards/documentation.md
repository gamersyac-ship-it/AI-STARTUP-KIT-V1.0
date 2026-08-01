# Documentation

## Objetivo

Establecer una práctica de documentación profesional, mantenible y reutilizable dentro del framework.

## Alcance

Aplica a README, ADRs, guías de arquitectura, API docs, procesos, estándares y cualquier artefacto de conocimiento de ingeniería.

## Cuándo aplica

Cuando una decisión, proceso, patrón o entrega necesita quedar reutilizable y no solo en la memoria de un individuo.

## Principios

- la documentación es parte del producto,
- las decisiones deben ser trazables,
- los documentos deben ser mantenibles,
- la información debe estar resumida y conectada con el contexto.

## Buenas prácticas

- Mantener estructura consistente de títulos y secciones.
- Referenciar documentos relacionados en vez de repetir información.
- Usar ejemplos y decisiones con contexto.
- Estimar el ciclo de vida y ownership del documento.

## Anti-patrones

- documentación obsoleta,
- documentación sin dueño,
- duplicados de reglas del mismo tema,
- descripciones vagas que no ayudan a ejecutar.

## Convenciones

- headings con estilo consistente,
- enlaces internos a documentos de referencia,
- mantener ejemplos actuales,
- versionar documentos cuando el contexto o comportamiento cambie.

## Ejemplos correctos

```md
# API

## Objetivo

Describir el contrato y la intención del endpoint.
```

## Ejemplos incorrectos

```md
# docs

TODO
```

## Checklist

- ¿El documento responde a una necesidad real?
- ¿Está conectado con el sistema de trabajo?
- ¿La información es precisa y actual?
- ¿Tiene ejemplos o referencias adecuadas?

## Definition of Ready

Un documento está listo cuando el tema, el propietario y la intención de mantenimiento están claros.

## Definition of Done

Un documento se considera completo cuando puede ser usado por otra persona del equipo sin requerir conocimiento oculto.

## KPIs

- porcentaje de documentos con enlaces cruzados,
- frecuencia de actualización de ADRs y procesos,
- tiempo de incorporación de nuevos integrantes.

## Métricas

- número de documentos obsoletos,
- número de duplicados funcionales,
- tasa de cambios documentados después de release.

## Herramientas recomendadas

- Markdown con estructura clara
- MkDocs o Docsify si se desea navegación estática
- GitHub/GitLab docs

## Librerías recomendadas

- sin requerir librerías específicas para standard base.

## Errores comunes

- dejar todos los conocimientos en el README,
- no documentar decisiones técnicas que impactan evolución,
- escribir con lenguaje decorativo y poco operativo.

## Preguntas frecuentes

- ¿Qué debe documentarse? Todo lo que influye en mantenimiento, operación, calidad o despliegue.
- ¿Qué no necesita documentación? No existe regla general; casi todo necesita una referencia cuando afecta a múltiples personas.

## Referencias internas

- [company/communication.md](../company/communication.md)
- [company/workflow.md](../company/workflow.md)
- [company/engineering-principles.md](../company/engineering-principles.md)
