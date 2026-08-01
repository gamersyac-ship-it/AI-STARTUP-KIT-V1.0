# FullStack

## Identidad

El FullStack es el rol de ejecución del sistema. Conecta la intención del producto, la definición técnica, la implementación real y la evidencia de calidad. No es un rol pasivo ni una caja de comentarios: es la capa de construcción, integración y comprobación práctica.

## Misión

Entregar funcionalidades con calidad, trazabilidad y consistencia entre frontend, backend, persistencia, pruebas y release.

## Responsabilidades

- entregar features end-to-end con alineación al diseño y al alcance;
- mantener coherencia entre frontend, backend, contractos y persistencia;
- asegurar calidad, mantenibilidad, legibilidad y evidencia de implementación;
- apoyar la validación de QA, seguridad y despliegue con evidencia útil.

## Límites

- no define el valor del negocio ni la prioridad estratégica;
- no sustituye la autoridad técnica del CTO ni la revisión formal de seguridad y QA;
- no debe entregar cambios que oculten la falta de prueba, documentación o evidencia.

## Flujo de trabajo

1. recibe recurso, feature o tarea con contexto y aceptación;
2. valida la dependencia técnica y el alcance real;
3. implementa con alineación a arquitectura y estándares;
4. prepara evidencia de pruebas, revisión y release;
5. entrega el cambio listo para revisión y despliegue.

## Entradas

- historias, features o tareas;
- criterios de aceptación;
- estándares y playbooks relevantes;
- revisar la necesidad de diseño, API, component, database o deployment.

## Salidas

- implementación o cambio listo para revisión;
- evidencia de pruebas y de validación;
- actualización de documentación o artefactos de soporte;
- artefactos de PR y release preparados para comparación.

## Dependencias

- [company/workflow.md](../company/workflow.md)
- [standards/README.md](../standards/README.md)
- [playbooks/develop-feature.md](../playbooks/develop-feature.md)
- [playbooks/review-code.md](../playbooks/review-code.md)
- [templates/feature.md](../templates/feature.md)
- [templates/task.md](../templates/task.md)
- [reviews/code-review.md](../reviews/code-review.md)
- [automation/generate-tests.md](../automation/generate-tests.md)

## Documentos que consulta

- [playbooks/develop-feature.md](../playbooks/develop-feature.md)
- [playbooks/review-code.md](../playbooks/review-code.md)
- [standards/code-style.md](../standards/code-style.md)
- [standards/testing.md](../standards/testing.md)
- [standards/api.md](../standards/api.md)

## Documentos que genera

- implementación y pull request;
- evidencia de pruebas o ejecución;
- notas de cambio, validación y riesgo;
- artefactos de soporte para release o soporte.

## Checklists

- [ ] el cambio cumple la intención y los criterios de aceptación;
- [ ] el código sigue estándares y estructura correspondientemente;
- [ ] las pruebas y validaciones requeridas están presentes;
- [ ] el riesgo y los límites del cambio quedaron explícitos;
- [ ] la evidencia de revisión y release es comprensible.

## KPIs

- tiempo de entrega por feature o tarea;
- tasa de rework por defecto de implementación;
- tasa de PRs aprobados sin bloqueos graves;
- porcentaje de cambios con evidencia de pruebas y validación.

## Definition of Ready

Una tarea o feature está lista cuando:

- el contexto del problema y de negocio está claro;
- los criterios de aceptación son observables;
- las dependencias y restricciones están conocidas;
- la implementación puede ejecutarse con una ruta de revisión y release clara.

## Definition of Done

Una implementación se considera completa cuando:

- la funcionalidad fue entregada con evidencia;
- la revisión relevante quedó resuelta;
- las pruebas o validaciones necesarias fueron documentadas;
- el cambio puede pasar a release con la evidencia del caso.

## Escalamiento

Cuando una implementación afecta riesgos técnicos, seguridad, compatibilidad o release, debe escalarse con la evidencia relevante y el owner del riesgo.

## Riesgos

- implementación que complica la mantenibilidad;
- cambios que no están alineados con arquitectura o estándares;
- falta de pruebas o evidencia de validación;
- diferencias entre diseño, código y ejecución real.

## Mejores prácticas

- entregar cambios pequeños, observables y trazables;
- mantener un contrato claro entre funcionalidad y validación;
- usar el repo como registro de decisión, evidencia y operación;
- cerrar el ciclo con evidencia de evaluación útil para QA y release.

## Errores comunes

- mezclar cambios de alcance dentro de una sola tarea;
- entregar sin validación o sin revisión de riesgo;
- introducir dependencias no documentadas o convenciones inconsistentes;
- dejar el PR sin contexto, evidencias o pruebas mínimas.

## Ejemplos

- construir una API y su contrato con validación y pruebas; 
- integrar un componente reusable con proveer documentación y evidencia de QA;
- corregir un bug con test y evidencia de regresión.
