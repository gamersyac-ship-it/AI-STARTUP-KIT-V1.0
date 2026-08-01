# Release Review

## Objetivo

Confirmar que un cambio, en conjunto con su evidencia y su operación asociada, está listo para ser entregado a producción o a una audiencia de release controlado.

## Cuándo ejecutarlo

- antes del cierre final de release;
- cuando una entrega reúne cambios de código, seguridad, QA, deployment o documentación;
- cuando el riesgo del cambio requiere evidencia formal para aprobación de salida.

## Responsable

- CTO o Engineering Manager: coordinación de aprobación final.
- QA Lead: valida la evidencia de funcionamiento.
- Security Lead: confirma riesgos críticos y cierre de hallazgos.
- DevOps: valida_release y rollback.
- Product Manager: confirma alineación de valor y prioridad.

## Checklist completo

- [ ] el alcance del release está definido y reseñado
- [ ] las revisiones obligatorias asociadas al cambio fueron ejecutadas
- [ ] las evidencias de QA, security, deployment y documentación están disponibles
- [ ] los riesgos de release quedaron identificados y manejados
- [ ] el rollback o contingency plan está documentado y permitido
- [ ] no existen blockers abiertos de impacto de seguridad, funcionamiento o operación
- [ ] la coordinación de comunicación y soporte está lista
- [ ] la evidencia para aprobación es trazable y legible para la organización

## Criterios de aprobación

- las revisiones obligatorias tienen evidencia clara;
- la entrega cumple con el criterio de salida del proyecto;
- la operación asociada está validada y el release se puede sostener.

## Criterios de rechazo

- cualquier blocker funcional, de seguridad, de despliegue o documentario queda abierto sin owner;
- no hay evidencia suficiente del riesgo y su manejo;
- el release se presenta sin validación de pre o post condiciones requeridas.

## Riesgos

- liberar cambios con evidencias insuficientes;
- ocultar dependencias o riesgos en la ventana de salida;
- producir incidentes por falta de coordinación de rollback o soporte.

## Acciones correctivas

- bloquear la salida hasta completar revisiones faltantes;
- separar el release en fases o volver una parte del cambio;
- exigir evidencia de cada gate antes del cierre;
- mantener una comunicación de riesgo y compensación con owner.

## Ejemplos

Ejemplo: un release incluye nuevas políticas de acceso y una migration de esquema. La release review exige evidencia de security review, QA validation, deployment review y documentación del rollback antes de autorizar salida a producción.

## KPIs

- porcentaje de releases aprobados sin incidentes;
- tiempo de cierre de release;
- tasa de rollback por release;
- número de blockers detectados antes de salida.

## Métricas

- número de revisiones ejecutadas por release;
- número de blockers abiertos al cierre;
- tiempo entre aprobación y despliegue final;
- tasa de rework por release no preparado.

## Definition of Done

La release review termina cuando el cambio quedó validado por todas las revisiones obligatorias, la evidencia está completa y la salida queda autorizada o rechazada con decisión explícita y responsable visible.
