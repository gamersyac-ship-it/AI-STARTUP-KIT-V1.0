# Deployment Review

## Objetivo

Verificar que el despliegue de un cambio es seguro, reversible, observable y compatible con el plan de lanzamiento y soporte operativo.

## Cuándo ejecutarlo

- antes de cualquier release o despliegue planificado;
- cuando cambia infraestructura, dependencias, secretos, entorno o capacidad;
- para hotfix, migration y cambios con alta dependencia operativa.

## Responsable

- DevOps: lidera la revisión del despliegue y rollback.
- QA Lead: valida evidencias de validación previa al rollout.
- Security Lead: revisa secretos, exposure y control de acceso.
- CTO o Engineering Manager: aprueba el riesgo de operación.

## Checklist completo

- [ ] el entorno objetivo está definido y es verificable
- [ ] la release candidate pasó validaciones requeridas
- [ ] la estrategia de despliegue es conocida: rolling, canary, full, blue-green
- [ ] rollback o revert está definido y probado
- [ ] la observabilidad del servicio es suficiente antes y después del deployment
- [ ] las variables de entorno, secretos y configs están alineadas con el target
- [ ] las dependencias externas y su comportamiento están controlados
- [ ] el cambio considera impacto sobre usuarios, capacidad y SLA
- [ ] el proceso de comunicación de release y contingencias está documentado
- [ ] la evidencia de operación queda registrada para cierre

## Criterios de aprobación

- el despliegue no introduce riesgos no mitigados;
- el rollback queda definido y es comprensible;
- la observabilidad y validación post-deploy están disponibles.

## Criterios de rechazo

- faltan evidencias de validación previa o post-deploy;
- el rollback o recuperación no es práctico;
- la operación depende de pasos manuales no documentados.

## Riesgos

- downtime o degradación silenciosa;
- errores de configuración o variables no sincronizadas;
- pérdida de trazabilidad en release o rollback.

## Acciones correctivas

- separar despliegues por fases y activar validación en cada etapa;
- preparar rollback con evidencia y owner;
- bloquear release hasta completar validación de entorno y seguridad;
- documentar la operación y los criterios de fallo.

## Ejemplos

Ejemplo: una migration de schema se despliega con control de versión, validación previa en staging, observabilidad de consultas y plan de rollback por script reversible. La deployment review aprueba solo si el proceso queda explícito y con owner de operación.

## KPIs

- tasa de rollback por release;
- tiempo de despliegue por cambio;
- tiempo de resolución de incidentes post-release;
- tasa de despliegues con validación post-deploy completa.

## Métricas

- número de despliegues por release;
- tiempo de espera entre etapas de release;
- tasa de errores observados tras rollout;
- porcentaje de deployments con rollback verificado.

## Definition of Done

La deployment review se considera cerrada cuando el plan de despliegue, validación de pre y post-release, rollback y observabilidad están en evidencia y el cambio tiene decisión explícita de aprobación o bloqueo.
