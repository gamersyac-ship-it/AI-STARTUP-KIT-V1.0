# Reviews

## Objetivo

Este módulo define los procesos oficiales de revisión de calidad para cambios de software, documentación, entrega, operaciones y experiencia del usuario dentro del framework.

## Principios

- Toda revisión debe estar basada en evidencia observable.
- La aprobación debe ser explícita, con responsable y fecha.
- Las revisiones obligatorias dependen del tipo de cambio.
- Si una revisión bloquea una entrega, la razón debe quedar registrada.

## Mapa de revisiones

- [code-review.md](code-review.md): revisión de implementación y mantenibilidad.
- [qa-review.md](qa-review.md): validación funcional, regresión y evidencias de prueba.
- [security-review.md](security-review.md): revisión de autorización, secretos, ingreso, salida y exposición.
- [architecture-review.md](architecture-review.md): evaluación del diseño y su sostenibilidad.
- [performance-review.md](performance-review.md): evaluación de latencia, carga y consumo de recursos.
- [accessibility-review.md](accessibility-review.md): revisión de uso por personas con diversidad funcional.
- [database-review.md](database-review.md): revisión de esquema, migraciones, integridad y consultas.
- [api-review.md](api-review.md): revisión de contrato, compatibilidad y evolución del API.
- [deployment-review.md](deployment-review.md): revisión de riesgos de despliegue y recuperación.
- [documentation-review.md](documentation-review.md): revisión de claridad, consistencia y trazabilidad documental.
- [ux-review.md](ux-review.md): revisión de usabilidad, flujo y coherencia de experiencia.
- [release-review.md](release-review.md): revisión final de aprobación para entrega o lanzamiento.

## Matriz de revisiones obligatorias

| Tipo de cambio | Revisiones obligatorias |
| --- | --- |
| API | code-review, api-review, security-review, qa-review, release-review |
| UI / UX | code-review, qa-review, accessibility-review, ux-review, performance-review, release-review |
| Base de Datos | code-review, database-review, security-review, qa-review, deployment-review, release-review |
| Infraestructura | architecture-review, security-review, deployment-review, performance-review, release-review |
| Refactor técnico grande | architecture-review, code-review, qa-review, performance-review, release-review |
| Cambio de seguridad crítico | security-review, architecture-review, qa-review, release-review |
| Cambio de documentación | documentation-review, release-review |
| Cambio de despliegue | deployment-review, release-review, qa-review |
| Cambio de experiencia / onboarding | ux-review, documentation-review, qa-review |

## Definition of Done del módulo reviews

El módulo se considera completo cuando:

- cada revisión tiene objetivo, responsable, checklist, criterios de aprobación y rechazo, riesgos, acciones correctivas, ejemplo, KPIs, métricas y Definition of Done;
- la matriz de obligatoriedad de revisiones está documentada y es reutilizable;
- cada revisión se alinea con el flujo de trabajo y la política de release del framework.
