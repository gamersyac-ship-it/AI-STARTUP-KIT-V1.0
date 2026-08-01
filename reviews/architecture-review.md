# Architecture Review

## Objetivo

Evaluar si la solución propuesta es coherente con el modelo de dominio, la mantenibilidad del sistema y los límites operativos del framework.

## Cuándo ejecutarlo

- en nuevas funcionalidades que cambian la arquitectura de un módulo;
- en cambios de integración, dependencias o tecnologías;
- cuando una mejora introduce nueva tensión de diseño o de ownership.

## Responsable

- Principal Architect: lidera la revisión de diseño y decisiones principales.
- CTO: aprueba el direccionamiento estratégico y de riesgo.
- Security Lead: revisa compatibilidad con límites de seguridad y exposición.
- DevOps: valida sostenibilidad operativa y despliegue.
- Product Manager: valida alineación con el objetivo de negocio.

## Checklist completo

- [ ] la intención del cambio y el problema a resolver están claros
- [ ] la solución mantiene separación adecuada entre dominio, acceso y transporte
- [ ] el diseño es sostenible a largo plazo y testable en operación real
- [ ] la arquitectura no introduce dependencia oculta o deuda técnica innecesaria
- [ ] el impacto en rendimiento, operación y seguridad es conocido
- [ ] se identifican responsables y decisiones de propiedad
- [ ] la solución se alinea con el flujo de release y mantenimiento del framework
- [ ] existen alternativas documentadas y se evalúa la elección recomendada
- [ ] la revisión produce un registro ejecutivo con decisiones y riesgos
- [ ] el resultado puede entregarse como ADR o decisión formal de aprobación

## Criterios de aprobación

- la solución es clara, mantenible, operable y documentada;
- las decisiones quedan registradas con impacto y ownership;
- no hay dependencia estructural ocultamente peligrosa.

## Criterios de rechazo

- la solución crea acoplamiento excesivo, duplicación o dependencias no visibles;
- la decisión no ofrece capacidad de operación o sostenibilidad;
- la arquitectura cambia los límites de dominio sin evidencia ni dueño.

## Riesgos

- deuda técnica acumulada por decisiones rápidas;
- mantenimiento difícil por acoplamiento indiscriminado;
- operación y seguridad no contempladas en un cambio abundante.

## Acciones correctivas

- refinar el diseño antes de aprobación;
- priorizar modularidad y propiedad explícita;
- registrar decisiones con ADR o decisión formal;
- devolver la propuesta con un plan de mitigación y seguimiento.

## Ejemplos

Ejemplo: una nueva integración de eventos entre servicios se revisa con arquitectura, seguridad y operación. La aprobación requiere que el ownership, la recuperación ante fallos y el flujo de interdependencia estén explícitos y con responsable claro.

## KPIs

- tasa de decisiones arquitectónicas documentadas;
- rework arquitectónico por release;
- reducción de incidentes por acoplamiento o diseño ambiguo;
- tiempo de toma de decisiones de arquitectura.

## Métricas

- número de ADRs aprobados por periodo;
- tiempo promedio de revisión arquitectónica;
- número de incidentes explicables por diseño ambiguo;
- cantidad de cambios con decisión arquitectónica reflexionada antes de desarrollo.

## Definition of Done

La architecture review queda cerrada cuando la decisión técnica tiene contexto, evidencias, limitaciones, riesgos y aprobación explícita con owner responsable.
