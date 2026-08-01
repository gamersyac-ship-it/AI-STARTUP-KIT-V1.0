# Documentation Review

## Objetivo

Confirmar que la documentación asociada al cambio es clara, consistente, útil y suficientemente trazable para mantenimiento, operación, revisión y onboarding.

## Cuándo ejecutarlo

- en toda entrega con impacto en funcionamiento, uso o mantenimiento;
- cuando cambian contratos, API, arquitectura, despliegue o procedimientos internos;
- antes de cerrar una pull request o release con documentación asociada.

## Responsable

- Technical Writer o Documentation Owner: valida claridad narrativa y estructura.
- Product Manager: revisa intención y contexto de uso.
- CTO o Engineering Manager: valida trazabilidad con decisiones y estándares.
- QA Lead: evalúa si la documentación soporta validación y operación real.

## Checklist completo

- [ ] el documento describe el propósito del cambio con contexto suficiente
- [ ] la referencia a requisitos, playbooks o estándares es correcta
- [ ] la estructura es legible y consistente con el sistema de documentación
- [ ] el lenguaje es claro, objetivo y no ambiguo
- [ ] los pasos operativos son reales y verificables
- [ ] la documentación refleja el estado actual y no un estado antiguo
- [ ] los riesgos, límites y dependencias están explícitos
- [ ] la evidencia de revisión o aprobación está enlazada cuando aplica
- [ ] el documento se puede usar para onboarding y operación sin conocimiento tácito
- [ ] la actualización queda asociada al cambio de forma trazable

## Criterios de aprobación

- la documentación es útil para ejecutar, mantener y validar el cambio;
- se elimina ambigüedad y se conserva trazabilidad con el flujo del framework;
- la información es consistente con el sistema de trabajo vigente.

## Criterios de rechazo

- la documentación omite pasos críticos o decisiones de diseño;
- el documento contradice el comportamiento, release o estándares actuales;
- el contenido es demasiado teórico o no accionable.

## Riesgos

- mala adopción por falta de contexto;
- ejecución defectuosa por pasos incompletos;
- inconsistencias entre diseño, operación y evidencia documental.

## Acciones correctivas

- completar secciones faltantes con información operativa;
- controlar versiones y referencias a decisiones o releases;
- actualizar el documento en el mismo ciclo del cambio; 
- pedir revisión del owner técnico o de documentación cuando el documento afecte release.

## Ejemplos

Ejemplo: un release documentado sin el paso de rollback o sin la evidencia de validación posterior no pasa la documentación review, porque el documento no es útil para operación real y soporte.

## KPIs

- porcentaje de cambios con documentación actualizada;
- tiempo de actualización de documentación asociada al release;
- tasas de rework por documentación incompleta;
- uso de documentación en onboarding y soporte.

## Métricas

- número de documentos no actualizados;
- número de hallazgos de documentación por release;
- tiempo de corrección de documentación por cambio;
- porcentaje de tickets de soporte resueltos por documentación clara.

## Definition of Done

La documentation review queda cerrada cuando la documentación del cambio es útil, consistente con el estado actual y sirve como evidencia de ejecución, soporte o operación.
