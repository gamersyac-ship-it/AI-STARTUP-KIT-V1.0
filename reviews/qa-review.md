# QA Review

## Objetivo

Validar que un cambio cumple con el comportamiento esperado, no introduce regresiones y está respaldado por evidencia de prueba verificable.

## Cuándo ejecutarlo

- al completar una funcionalidad o corrección;
- antes del merge cuando hay riesgos de regresión;
- en cambios de flujo, permisos, formularios, APIs o despliegues;
- cuando una revisión de seguridad o arquitectura identifica riesgo funcional.

## Responsable

- QA Lead: lidera la revisión funcional y validación.
- FullStack o author: entrega evidencia y contexto.
- Product Manager: valida que el comportamiento entregado coincide con el objetivo de negocio.
- Security o DevOps: participan cuando el riesgo cruza seguridad o despliegue.

## Checklist completo

- [ ] el alcance del cambio está claro y delimitado
- [ ] la historia, requisito o caso de uso está documentado
- [ ] existen casos de prueba para el flujo principal y los flujos alternativos
- [ ] hay cobertura para casos de borde, errores esperados y mensajes de usuario
- [ ] el resultado esperado es observable y verificable
- [ ] las pruebas están configuradas para entorno relevante
- [ ] se verifican regresiones relacionadas con el mismo módulo o dependencia
- [ ] la evidencia de prueba es legible y trazable
- [ ] el cambio no requiere pasos manuales ambiguos para validación
- [ ] la revisión recoge riesgos de uso no cubiertos por la suite actual

## Criterios de aprobación

- el comportamiento cumple el objetivo del cambio;
- la evidencia de prueba es clara y reproducible;
- no hay regresiones abiertas en los flujos afectados;
- la validación quedó documentada para merge o release.

## Criterios de rechazo

- el comportamiento no puede ser verificado con evidencia;
- hay regresiones detectadas en el alcance afectado;
- faltan pruebas para flujos críticos;
- la validación depende de conocimiento tácito no documentado.

## Riesgos

- regresiones ocultas en componentes adyacentes;
- validaciones incompletas por falta de entorno realista;
- evidencia insuficiente para soportar aprobación.

## Acciones correctivas

- ampliar casos de prueba y escenarios de borde;
- documentar un plan de regresión específico;
- bloquear el merge hasta que la evidencia sea consistente;
- separar cambios de alcance para reducir riesgo de regresión.

## Ejemplos

Ejemplo: una nueva pantalla de onboarding se valida con casos de flujo exitoso, error de validación y navegación posterior. La QA review solo aprueba si cada caso tiene evidencia de ejecución y la regresión del flujo antiguo queda descartada.

## KPIs

- tasa de escape de defectos a producción;
- porcentaje de cambios con evidencia de QA formal;
- tiempo medio de validación por cambio;
- tasa de rework post-release.

## Métricas

- número de casos de prueba ejecutados;
- número de fallas encontradas;
- tiempo de ejecución de validación por entorno;
- porcentaje de cobertura de regresión para módulos críticos.

## Definition of Done

La revisión QA queda cerrada cuando el cambio ha sido validado con evidencia, se confirma su comportamiento esperado y queda registrada la decisión de aprobación, bloqueo o corrección.
