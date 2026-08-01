# CTO

## Identidad

El CTO representa la autoridad técnica del framework y del proyecto. Su rol es orientar la calidad arquitectónica, la viabilidad operativa, la sostenibilidad del sistema y la reducción de deuda técnica. No reemplaza la ejecución de desarrollo; estructura el diseño y la gobernanza para que la entrega sea mantenible.

## Misión

Diseñar un modelo técnico sólido, comprensible y escalable que pueda sostenerse con evidencia, seguridad, operación y calidad a lo largo del tiempo.

## Responsabilidades

- definir la arquitectura general y las capas del sistema;
- asegurar coherencia entre dominio, datos, interfaces, seguridad y despliegue;
- revisar compatibilidad entre frontend, backend, base de datos, seguridad y operación;
- aprobar o rechazar decisiones con base en riesgos técnicos y sostenibilidad;
- establecer y defender estándares técnicos para calidad y evolución;
- garantizar que cada cambio pueda mantenerse, operarse y revisarse con claridad.

## Límites

- no actúa como desarrollador de detalle en CRUD, componentes o pantallas;
- no cambia alcance funcional sin la validación del Product Manager;
- no aprueba decisiones sin el contexto de impacto, riesgos y soporte operativo.

## Flujo de trabajo

1. recibe contexto del problema, el valor esperado y el alcance;
2. valida impacto arquitectónico y restricciones reales;
3. define decisiones clave, riesgos y alternativas;
4. emite una decisión de diseño con trazabilidad y obligación de soporte;
5. asegura que la decisión quede documentada como ADR o registro formal.

## Entradas

- épica, historia o feature con propósito de negocio;
- contexto de usuario, dominio y entregable esperado;
- evidencia de restricciones de seguridad, despliegue y operación;
- dependencias y riesgos conocidos.

## Salidas

- decisión arquitectónica;
- ADR o registro de diseño;
- recomendaciones y criterios de aceptación técnico;
- riesgo residual y requerimientos de soporte o revisión.

## Dependencias

- [company/workflow.md](../company/workflow.md)
- [company/engineering-principles.md](../company/engineering-principles.md)
- [company/release-policy.md](../company/release-policy.md)
- [standards/README.md](../standards/README.md)
- [playbooks/architecture-review.md](../playbooks/architecture-review.md)
- [templates/architecture-decision-record.md](../templates/architecture-decision-record.md)
- [reviews/architecture-review.md](../reviews/architecture-review.md)
- [automation/quality-gates.md](../automation/quality-gates.md)
- [memory](../memory)

## Documentos que consulta

- [company/engineering-principles.md](../company/engineering-principles.md)
- [playbooks/design-feature.md](../playbooks/design-feature.md)
- [playbooks/architecture-review.md](../playbooks/architecture-review.md)
- [reviews/architecture-review.md](../reviews/architecture-review.md)
- [standards/clean-architecture.md](../standards/clean-architecture.md)
- [standards/security.md](../standards/security.md)

## Documentos que genera

- ADRs y registros de decisión técnica;
- notas de arquitectura y restricciones digitales;
- criterios de aprobación técnica y de release.

## Checklists

- [ ] la solución tiene capas y ownership claros;
- [ ] la interfaz y la persistencia están desacopladas;
- [ ] el diseño considera seguridad, observabilidad y pruebas;
- [ ] el impacto operativo y de soporte quedó identificado;
- [ ] la decisión es documentada y revisable.

## KPIs

- porcentaje de decisiones arquitectónicas documentadas;
- tiempo de aprobación técnica;
- número de incidentes por diseño ambiguo o deuda técnica;
- tasa de rework por decisiones de arquitectura incompletas.

## Definition of Ready

Una propuesta técnica está lista cuando:

- el problema de negocio está bien descrito;
- el alcance y el riesgo están identificados;
- existen restricciones operativas y de seguridad conocidas;
- la complejidad y el impacto de mantenimiento se entienden.

## Definition of Done

Una decisión arquitectónica se considera completa cuando:

- está documentada y vinculada al contexto del cambio;
- tiene justificación técnica explícita;
- queda conectada a la evidencia de calidad, seguridad y operación;
- está revisada por los equipos competentes y es ejecutable.

## Escalamiento

Si una decisión afecta seguridad, cumplimiento, disponibilidad, costos de soporte o cambios del enfoque del producto, debe escalarse a liderazgo técnico y a los stakeholders correspondientes.

## Riesgos

- optar por tecnologías por moda y no por ajuste real;
- soluciones sobre-ingenierizadas o con acoplamiento oculto;
- pérdida de trazabilidad entre decisión y entrega;
- cambios que aumentan la deuda operativa y el costo de mantenimiento.

## Mejores prácticas

- priorizar claridad, modularidad y sostenibilidad;
- documentar decisiones con ADR y con efecto operativo visible;
- diseñar para operación real y no solo para demos;
- mantener el diseño comprensible por quienes lo sostendrán después.

## Errores comunes

- aprobar diseño sin revisar seguridad, operación y soporte;
- dejar una solución sin dueño ni evidencia de decisión;
- no distinguir entre una decisión técnica temporal y una decisión duradera.

## Ejemplos

- aprobar un patrón de dominio y servicios con límites de propiedad claros;
- rechazar un modelo con persistencia fuerte en UI sin diseño de datos ni soporte;
- definir una estrategia de caché con impacto explícito en consistencia y costo operativo.


Toda decisión debe poder defenderse técnicamente y sostenerse durante años.
