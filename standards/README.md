# Standards

## Objetivo

Esta carpeta define el conjunto de estándares técnicos que guiarán el desarrollo dentro de AI-STARTUP-KIT. Su función es transformar buenas intenciones en reglas reutilizables, verificables y mantenibles para equipos reales.

## Alcance

Los estándares están organizados por dominio técnico y se apoyan en los principios definidos en [company/engineering-principles.md](../company/engineering-principles.md), [company/workflow.md](../company/workflow.md) y [company/release-policy.md](../company/release-policy.md).

## Estructura

- [react.md](react.md): arquitectura, estado, routing, rendering y acceso.
- [node.md](node.md): arquitectura de servicios, servicios, repositorios y capa de transporte.
- [typescript.md](typescript.md): tipado, patrones y seguridad en tipado.
- [javascript.md](javascript.md): estilo y cuidado de runtime cuando no se usa TypeScript.
- [database.md](database.md): normalización, migraciones, índices, auditoría y integridad.
- [api.md](api.md): contratos HTTP, REST, OpenAPI, versionado y seguridad.
- [security.md](security.md): controles, amenazas, secretos, autorización y revisiones.
- [testing.md](testing.md): unit, integration, E2E, cobertura, QA y validación real.
- [git.md](git.md): commits, branches, PRs, merge, rebase y versionado.
- [documentation.md](documentation.md): documentación de sistema, decisiones y mantenimiento de conocimiento.
- [performance.md](performance.md): tiempos, recursos, observabilidad y optimización.
- [naming.md](naming.md): convenciones de nomenclatura.
- [clean-code.md](clean-code.md): legibilidad, responsabilidad única y refactorización.
- [clean-architecture.md](clean-architecture.md): capas, dependencias y casos de uso.
- [logging.md](logging.md): trazabilidad, estructura y niveles de log.
- [error-handling.md](error-handling.md): clasificación, manejo y respuesta estándar.
- [dependencies.md](dependencies.md): gestión segura y sostenible de dependencias.
- [code-style.md](code-style.md): estilo de formato, estilo de importación y mantenimiento de archivos.

## Principios de operación

- No duplicar reglas entre documentos.
- Referenciar primero el documento base cuando exista un principio general.
- Espere trazabilidad de decisiones, no solo de código.
- Mantener ejemplos realistas y reutilizables.

## Definition of Ready

Un estándar nuevo o un cambio de estándar está listo cuando:

- el problema de ingeniería está claramente descrito,
- el principio operativo que lo justifica está documentado,
- los ejemplos son verificables,
- y el impacto en el flujo de trabajo y la seguridad queda explicitado.

## Definition of Done

Un estándar se considera adoptado cuando:

- se ha escrito de forma consistente,
- se expresa con ejemplos y anti-patrones,
- y queda vinculado al flujo de calidad, review y despliegue del framework.

## KPIs

- proporción de documentos estándar con ejemplos completos,
- porcentaje de cambios alineados con una política de revisión,
- reducción de inconsistencias entre departamentos,
- tiempo de comprensión de un módulo por parte de un nuevo integrante.

## Referencias internas

- [company/engineering-principles.md](../company/engineering-principles.md)
- [company/workflow.md](../company/workflow.md)
- [company/release-policy.md](../company/release-policy.md)
- [company/communication.md](../company/communication.md)
