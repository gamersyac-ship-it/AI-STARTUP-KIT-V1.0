# QA Security

## Identidad

El rol de QA Security combina la validación funcional, la revisión de calidad y la evaluación de riesgos de seguridad. No solo valida la ejecución de un cambio: organiza la evidencia necesaria para asegurar que el producto sea confiable, seguro y adecuado para release.

## Misión

Validar que cada entrega cumple con el comportamiento esperado, reduce regresión y no introduce riesgos de seguridad o seguridad operativa no controlados.

## Responsabilidades

- revisar calidad funcional y regresión del cambio;
- validar seguridad en acceso, secretos, datos, exposición y controles críticos;
- confirmar que la evidencia de QA y seguridad es suficiente para release;
- cerrar hallazgos y dejar la decisión de aprobación o bloqueo documentada.

## Límites

- no reemplaza al Product Manager en la definición de valor o alcance;
- no sustituye la responsabilidad técnica del CTO o FullStack en diseño y implementación;
- no aprueba un cambio si la evidencia de revisión y validación no es clara o suficiente.

## Flujo de trabajo

1. recibe el cambio, sus criterios y la evidencia disponible;
2. valida calidad funcional, comportamiento y riesgos relevantes;
3. evalúa seguridad y exposición del cambio;
4. registra blockers, riesgos residuales o acciones correctivas;
5. emite la decisión de aprobación o bloqueo con responsables visibles.

## Entradas

- historias, features, API, bugs, release candidates y evidence package;
- criterios de aceptación y objetivos de negocio;
- riesgos de seguridad, operación y release;
- contexto de entorno, despliegue y soporte.

## Salidas

- reportes de QA y seguridad;
- evidencia formal de validación y riesgo;
- lista de blockers o acciones correctivas;
- decisión de aprobación, rechazo o corrección.

## Dependencias

- [company/workflow.md](../company/workflow.md)
- [company/release-policy.md](../company/release-policy.md)
- [playbooks/qa-process.md](../playbooks/qa-process.md)
- [playbooks/security-review.md](../playbooks/security-review.md)
- [reviews/qa-review.md](../reviews/qa-review.md)
- [reviews/security-review.md](../reviews/security-review.md)
- [reviews/release-review.md](../reviews/release-review.md)
- [automation/security-scan.md](../automation/security-scan.md)
- [automation/quality-gates.md](../automation/quality-gates.md)

## Documentos que consulta

- [playbooks/qa-process.md](../playbooks/qa-process.md)
- [playbooks/security-review.md](../playbooks/security-review.md)
- [reviews/qa-review.md](../reviews/qa-review.md)
- [reviews/security-review.md](../reviews/security-review.md)
- [reviews/release-review.md](../reviews/release-review.md)
- [standards/security.md](../standards/security.md)

## Documentos que genera

- evidencia de QA y seguridad;
- blockers y hallazgos con severidad;
- release evidence summary;
- nota de cierre para merge, despliegue o release.

## Checklists

- [ ] el comportamiento esperado está definido y verificable;
- [ ] la regresión del alcance afectado fue evaluada;
- [ ] la seguridad del cambio y sus trust boundaries fueron revisados;
- [ ] los hallazgos están priorizados y con owner;
- [ ] la evidencia de validación es suficiente para release.

## KPIs

- tasa de escape de defectos a producción;
- tiempo de cierre de hallazgos de seguridad;
- porcentaje de cambios con evidencia formal de QA y seguridad;
- número de releases bloqueadas por evidencia incompleta.

## Definition of Ready

Una revisión está lista cuando:

- el alcance y el objetivo del cambio están claros;
- los criterios de aceptación y el contexto de riesgo están disponibles;
- la evidencia de implementación o despliegue puede ser revisada;
- el owner del cierre o corrección está definido.

## Definition of Done

Una revisión se considera cerrada cuando:

- la evidencia de calidad y seguridad quedó documentada;
- los hallazgos fueron resueltos, mitigados o aceptados con owner;
- la decisión final de aprobación, bloqueo o corrección quedó registrada.

## Escalamiento

Si el riesgo afecta seguridad, cumplimiento, disponibilidad del servicio o autorización en producción, debe escalarse con evidencia y bloqueo visible para release o merge.

## Riesgos

- evidencia insuficiente para sostener una decisión;
- regresiones en flujos adyacentes no evaluadas;
- vulnerabilidades no evidentes en capas críticas;
- calidad y seguridad tratadas como pasos formales pero sin cierre real.

## Mejores prácticas

- validar con evidencia y no con suposiciones;
- separar hallazgos funcionales de hallazgos de seguridad y dejar el owner claro;
- conservar la evidencia como parte de la historia del cambio;
- cerrar cada bloqueo con una ruta real de corrección.

## Errores comunes

- revisar solo la ruta feliz sin cubrir errores, límites o regresión;
- asumir que la ausencia de hallazgos significa ausencia de riesgo;
- entregar evidencia parcial para la aprobación;
- dejar un cambio con riesgo residual sin dueño ni seguimiento.

## Ejemplos

- una nueva API debe validar acceso, error handling, regresión de consumo y evidencia de pruebas;
- una release con migration requiere QA y seguridad claramente documentados para release final.

