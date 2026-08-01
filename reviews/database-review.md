# Database Review

## Objetivo

Evaluar si el modelo de datos, la migración, las relaciones, las consultas y los límites de integridad cumplen con el diseño de dominio, la seguridad y la sostenibilidad operativa.

## Cuándo ejecutarlo

- en cambios de esquema, integridad, relación entre entidades o migrations;
- antes de release de lógica con persistencia crítica;
- en refactors de queries, índices o plan de acceso.

## Responsable

- CTO o Principal Architect: valida el diseño de dominio y las decisiones de modelado.
- FullStack o DB owner: entrega el cambio de esquema y migración.
- DevOps: valida despliegue de migración y estrategia de rollback.
- Security o QA: apoyan en integridad, acceso y regresión de datos.

## Checklist completo

- [ ] la entidad o tabla está justificada por un dominio claro
- [ ] se documentan relaciones, cardinalidad y clave primaria o alternativa
- [ ] se revisan índices, ordenamiento y consulta más probable
- [ ] la migración es incremental y reversible en caso necesario
- [ ] se valida el riesgo de pérdida de integridad o duplicidad
- [ ] se controla acceso mínimo y permisos por contexto
- [ ] se revisan datos sensibles, auditoría y retención
- [ ] la semilla, datos de prueba o requisitos de contrato se documentan
- [ ] el plan de rollback o rollback parcial está definido
- [ ] la revisión contempla impacto de rendimiento y capacidad

## Criterios de aprobación

- el modelo es trazable a un requisito de negocio o dominio claro;
- la migración es segura y reversible;
- la persistencia mantiene integridad, rendimiento razonable y buen manejo de accesos.

## Criterios de rechazo

- el cambio introduce relaciones ambiguas o integridad no controlada;
- la migración no es reversible o no contempla rollback;
- las consultas o índices generan riesgo funcional o de operación.

## Riesgos

- pérdida o corrupción de datos;
- degradación por consultas no optimizadas;
- cambios de contrato de persistencia que rompen compatibilidad.

## Acciones correctivas

- añadir validaciones de integridad y claves únicas;
- separar migración en pasos guiados por riesgo;
- revisar y reforzar índices o consultas críticas;
- documentar rollout y rollback con evidencia y owner.

## Ejemplos

Ejemplo: una nueva relación entre usuarios y espacios requiere revisión de clave única, índice sobre workspace_id y usuario_id, política de navegación en acceso, y un plan de migration con impacto de compatibilidad hacia atrás.

## KPIs

- tasa de incidentes por integridad o migración;
- tiempo de resolución de errores de esquema;
- porcentaje de migrations con rollback documentado;
- número de regresiones relacionadas con persistencia.

## Métricas

- número de migraciones por release;
- tiempo de ejecución de migraciones;
- tasa de errores de integridad;
- impacto en latencia de consultas críticas.

## Definition of Done

La database review queda cerrada cuando el diseño, la migración, la integridad, el acceso y la recuperación del cambio están validados con evidencia documental y la aprobación o bloqueo está explícito.
