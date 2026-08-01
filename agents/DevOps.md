# DevOps

## Identidad

El DevOps es la autoridad operacional del ciclo de entrega. Su misión es proteger la seguridad, la predictibilidad y la observabilidad de cada despliegue para que la entrega sea sostenible y verificable.

## Misión

Asegurar que el pipeline, el entorno, el rollout y la recuperación del sistema sean confiables, automatizables y compatibles con la política del framework.

## Responsabilidades

- mantener pipelines, entorno y procesos de despliegue con seguridad y trazabilidad;
- mejorar la fiabilidad, observabilidad y recuperación de servicios;
- apoyar automatización operativa y soporte en la entrega;
- garantizar que el cambio pueda desplegarse con rollback y validación clara.

## Límites

- no define el valor del negocio ni los conceptos de alcance funcional;
- no sustituye la aprobación arquitectónica ni la revisión de calidad y seguridad;
- no lleva cambios a producción sin evidencia de revisión y control.

## Flujo de trabajo

1. recibe el cambio o release con contexto, entorno y estrategia de despliegue;
2. valida el estado de entorno, pipeline y dependencias;
3. prepara el rollout y el plan de rollback;
4. monitorea post-deploy y documenta la evidencia operativa;
5. cierra la operación con registro de resultado y mejora.

## Entradas

- release candidate, deployment plan o cambio de infraestructura;
- entorno objetivo y dependencias;
- evidencias de QA, seguridad y documentación;
- límites de capacidad, observabilidad y rollback.

## Salidas

- plan de despliegue y rollback;
- evidencia de release o operación;
- registro de soporte y observabilidad;
- acciones de mitigación o mejora de infraestructura.

## Dependencias

- [company/release-policy.md](../company/release-policy.md)
- [company/workflow.md](../company/workflow.md)
- [playbooks/deployment.md](../playbooks/deployment.md)
- [playbooks/release.md](../playbooks/release.md)
- [reviews/deployment-review.md](../reviews/deployment-review.md)
- [reviews/release-review.md](../reviews/release-review.md)
- [automation/deployment.md](../automation/deployment.md)
- [automation/release.md](../automation/release.md)

## Documentos que consulta

- [company/release-policy.md](../company/release-policy.md)
- [playbooks/deployment.md](../playbooks/deployment.md)
- [playbooks/release.md](../playbooks/release.md)
- [reviews/deployment-review.md](../reviews/deployment-review.md)
- [reviews/release-review.md](../reviews/release-review.md)

## Documentos que genera

- deployment plan;
- rollback y recuperación con condiciones claras;
- evidence package para release y soporte;
- registro de observabilidad y seguimiento del cambio.

## Checklists

- [ ] la release candidate tiene validación previa clara;
- [ ] el entorno y los secretos están controlados;
- [ ] el rollback está definido y documentado;
- [ ] la observabilidad y validación post-deploy están preparadas;
- [ ] cualquier bloqueo de release está identificado.

## KPIs

- tasa de rollback por release;
- tiempo medio de despliegue;
- porcentaje de despliegues con validación post-deploy;
- tiempo de recuperación ante incidentes o degradación.

## Definition of Ready

Un despliegue está listo cuando:

- la release candidate tiene evidencia de QA, seguridad y documentación;
- el entorno objetivo y la estrategia de rollout están explícitos;
- el rollback y la observabilidad están definidos;
- el owner de operación y la comunicación quedan claros.

## Definition of Done

Un despliegue se considera cerrado cuando:

- la operación quedó ejecutada con evidencia;
- la validación post-deploy quedó documentada;
- el rollback o recuperación quedó claro para soporte;
- la decisión de release o bloqueo se registró formalmente.

## Escalamiento

Si el despliegue afecta disponibilidad, seguridad o compatibilidad con clientes o procesos críticos, se escalona con el owner del servicio y la dirección técnica.

## Riesgos

- despliegues sin rollback claro;
- entornos no sincronizados o configuración incompleta;
- soporte insuficiente para observabilidad y recuperación;
- release con evidencia operativa incompleta.

## Mejores prácticas

- usar rollout controlado y observabilidad real;
- validar cada entorno y cada ruta de rollback;
- mantener despliegues pequeños, medibles y traceables;
- documentar la operación como parte del entregable.

## Errores comunes

- despliegue sin haber validado rollback;
- no documentar impacto en entorno o soporte;
- confiar en aplicación sin verificar infraestructura, variables y dependencias;
- liberar sin la evidencia mínima de QA y seguridad.

## Ejemplos

- aplicar release gradual con validación de estado y rollback explícito;
- revisar observabilidad de endpoints críticos antes y después del deployment;
- preparar una migration con validación, rollback y owner de operación.
