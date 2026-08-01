# Performance Review

## Objetivo

Evaluar si un cambio cumple con los límites de latencia, consumo de memoria, capacidad y estabilidad esperados por el sistema operativo y el usuario.

## Cuándo ejecutarlo

- en cambios de rutas críticas, APIs, queries, UI render y caché;
- en refactors de alto impacto o migrations de infraestructura;
- antes de release cuando la carga o la latencia son factores de riesgo.

## Responsable

- Performance Engineer: lidera la revisión de comportamiento en carga y consumo.
- FullStack o DevOps: entrega evidencia de implementación y entorno.
- CTO o Engineering Manager: aprueba el impacto operativa sobre la entrega.

## Checklist completo

- [ ] se ha identificado la ruta o caso de carga relevante
- [ ] se han definido límites aceptables de tiempo, memoria y uso de recursos
- [ ] el acceso a datos y dependencias es medible y observable
- [ ] se evaluaron serialización, consultas, render, conexión y timeouts
- [ ] la revisión contempla escenarios de picos y saturación
- [ ] se han definido métricas base y meta del comportamiento
- [ ] el impacto en costos de infraestructura está identificado
- [ ] hay evidencia de comparación antes y después del cambio
- [ ] se han documentado riesgos y mitigaciones

## Criterios de aprobación

- el cambio mantiene los límites definidos para la ruta crítica;
- no introduce degradación material en latencia o consumo;
- existe evidencia comparativa o benchmarking suficiente.

## Criterios de rechazo

- la ruta crítica excede umbrales aceptables;
- el cambio aumenta consumo de forma sostenida sin justificación;
- no hay evidencia del impacto real sobre la carga o usuario.

## Riesgos

- degradación silenciosa en producción;
- comportamiento inestable bajo picos de tráfico;
- cambios de performance ocultos en dependencias externas.

## Acciones correctivas

- reducir complejidad de consultas o render;
- introducir caché o batching controlado;
- limitar el número de llamadas, reintentos y consultas innecesarias;
- requerir benchmark y aprobación en release.

## Ejemplos

Ejemplo: una API nueva se revisa bajo carga de 100 usuarios concurrentes. La revisión exige que la latencia p95 se mantenga bajo el umbral establecido y que el consumo de memoria no aumente de forma sostenida en el entorno de pruebas.

## KPIs

- p95 y p99 de latencia en rutas críticas;
- tasa de errores por timeout;
- uso de memoria y CPU por servicio;
- tiempo de respuesta en flujo crítico.

## Métricas

- latencia promedio, p95, p99;
- CPU y memoria máxima;
- throughput por endpoint o flujo;
- número de consultas por request;
- tasa de errores por saturación.

## Definition of Done

La performance review queda cerrada cuando los resultados y umbrales del cambio están medidos, comparados con la línea base y registrados como aprobación, bloqueo o requisito de corrección.
