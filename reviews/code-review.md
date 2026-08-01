# Code Review

## Objetivo

Establecer una revisión formal de calidad, mantenibilidad y seguridad del código entregado, con evidencia verificable y decisión explícita de aprobación o rechazo.

## Cuándo ejecutarlo

- en cada pull request o merge request de cambios de código;
- cuando una funcionalidad, corrección o refactor afecta comportamiento o riesgo de producción;
- antes del merge o release si el cambio es de alcance significativo.

## Responsable

- QA Lead: valida calidad funcional y evidencia del comportamiento observado.
- Security Lead: revisa riesgos derivados de seguridad, secretos y exposición.
- Principal Architect: confirma diseño, dependencia y sostenibilidad.
- FullStack o reviewer: revisa corrección, legibilidad y mantenimiento.
- Author: aporta contexto, pruebas y evidencia para revisión.

## Checklist completo

- [ ] el propósito del cambio es comprensible y acotado
- [ ] el cambio se alinea con el objetivo del ticket o historia
- [ ] las pruebas o evidencias funcionales están disponibles
- [ ] la lógica revisada maneja casos de borde y errores esperados
- [ ] el estilo y la estructura del código son consistentes con los estándares vigentes
- [ ] el código no introduce acoplamiento oculto o lógica duplicada innecesaria
- [ ] los cambios de seguridad, permisos, logging o datos sensibles fueron evaluados
- [ ] el impacto en rendimiento y despliegue es observable
- [ ] el autor documenta riesgos o limitaciones conocidos
- [ ] la decisión final del review queda registrada con owner y cierre claro

## Criterios de aprobación

- el código cumple su intención y es verificable con evidencia;
- el cambio es legible, mantenible y consistente con el sistema de estándares;
- no hay bloqueadores de seguridad, regresión o operación sin owner y plan de corrección.

## Criterios de rechazo

- el cambio es ambiguo, no está respaldado por evidencia, o mezcla varios objetivos sin control;
- el código introduce fallos, riesgos de seguridad o dependencia oculta sin mitigación;
- el review no puede sostener la aprobación porque el cambio no es reproducible, trazable o seguro.

## Riesgos

- regresión funcional oculta;
- deuda técnica y baja mantenibilidad;
- seguridad o observabilidad insuficientes;
- revisión superficial basada en apariencia o estilo sin evidencia.

## Acciones correctivas

- requerir pruebas adicionales o evidencia de validación;
- dividir cambios mezclados en unidades más pequeñas;
- corregir lógica insegura, logging, permisos o validaciones faltantes;
- bloquear merge y volver al author hasta completar revisión pertinente.

## Ejemplos

Ejemplo: un PR de cambios en un servicio de autenticación se revisa para confirmar que la lógica de validación ocurre en la capa correcta, no se expone información sensible, y la evidencia de pruebas verifica rechazo a accesos no autorizados.

## KPIs

- tiempo medio de revisión por PR;
- tasa de rework por código entregado;
- porcentaje de cambios aprobados con evidencia completa;
- tasa de defectos escapados a producción luego de merge.

## Métricas

- número de comentarios de revisión por PR;
- tasa de re-changes requests por PR;
- número de hallazgos críticos, altos y medios;
- porcentaje de cambios con evidencia de pruebas asociada al merge.

## Definition of Done

La code review se considera cerrada cuando el cambio fue evaluado contra intención, diseño, seguridad, calidad y evidencia, y la decisión de aprobación, rechazo o solicitud de cambios quedó registrada de forma explícita y reutilizable.
