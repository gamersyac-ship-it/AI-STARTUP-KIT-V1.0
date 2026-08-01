# API Review

## Objetivo

Validar que un contrato de API es coherente, seguro, versionable, comprensible y suficientemente documentado para su uso por clientes internos o externos.

## Cuándo ejecutarlo

- en cambios de endpoints, payloads, headers, errores o esquema de respuesta;
- al introducir nuevas rutas internas o públicas;
- antes de release para cambios que alteran compatibilidad o contrato.

## Responsable

- Principal Architect: valida integridad del diseño y compatibilidad.
- FullStack o API owner: define y entrega el cambio.
- Security Lead: revisa autorización, secretos, exposición y protección.
- QA Lead: valida comportamiento, errores y regresión en cliente o servidor.

## Checklist completo

- [ ] el propósito del endpoint está claro y trazable
- [ ] el contrato documentado coincide con la implementación
- [ ] los request y response tienen esquema claro
- [ ] los errores son consistentes y měliconsecuentes para clientes
- [ ] los headers, autenticación y autorización están definidos
- [ ] la compatibilidad con versiones anteriores es evaluada
- [ ] el endpoint tiene estrategia de versionado o deprecation
- [ ] hay límites de payload, rate, paginación y tiempo de respuesta definidos
- [ ] los cambios en errores o respuestas están comunicados a consumidores
- [ ] la revisión incluye riesgo de seguridad y desacoplamiento

## Criterios de aprobación

- el API contract es claro, documentado y consistente;
- el cambio mantiene seguridad y compatibilidad aceptable;
- los consumidores o dependencias reconocen la evolución del contrato.

## Criterios de rechazo

- se introducen cambios con ruptura silenciosa o no declarada;
- la seguridad o límites de acceso no están definidos;
- el endpoint no tiene evidencia de contrato ni versionado.

## Riesgos

- incompatibilidades entre clientes y servidor;
- fuga de información en errores o respuestas;
- cambios de contrato no escalables en mantenimiento.

## Acciones correctivas

- versionar el cambio o mantener compatibilidad explícita;
- documentar el contrato y la estrategia de error;
- reforzar validación y pruebas de no regresión;
- cerrar la revisión con approval owner y evidencia de release.

## Ejemplos

Ejemplo: un endpoint de creación cambia el esquema de respuesta y añade un campo de auditoría. La API review exige que el cambio sea versionado o que el cliente tenga un plan de adaptación, además de revisar seguridad, errores y compatibilidad.

## KPIs

- tiempo medio de aprobación de contratos API;
- número de incidentes por ruptura de contrato;
- tasa de cambios con deprecation y versión documentada;
- tasa de revisar compatibilidad antes del release.

## Métricas

- número de endpoints por servicio;
- cantidad de cambios de contrato en release;
- tiempo de evolución de versiones;
- porcentaje de endpoints con documentados headers, errores y autenticación.

## Definition of Done

La API review queda cerrada cuando el contrato, compatibilidad, seguridad, versionado y evidencia de validación están explícitos y respaldan una decisión de aprobación o bloqueo con propietario visible.
