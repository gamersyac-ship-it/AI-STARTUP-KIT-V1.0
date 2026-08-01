# Security Review

## Objetivo

Establecer el proceso oficial de revisión de seguridad para cambios que afecten acceso, secretos, datos, salidas, autenticación o exponencia del sistema.

## Cuándo ejecutarlo

- en cambios de API, autenticación, autorización o manejo de fortalezas legales;
- cuando se altera la superficie de exposición del sistema;
- en cambios con manejo de datos sensibles o secretos;
- antes del release si el cambio toca políticas de seguridad.

## Responsable

- Security Lead: lidera la revisión;
- CTO o Principal Architect: evalúa impacto estructural y excepción;
- FullStack: entrega evidencia de implementación;
- QA Lead: valida riesgos funcionales y regresiones de seguridad;
- DevOps: valida entorno, secretos y despliegue.

## Checklist completo

- [ ] se identifican los trust boundaries del cambio
- [ ] la autenticación y autorización están definidas y verificables
- [ ] las rutas de acceso cumplen principio de menor privilegio
- [ ] no se exponen secretos, tokens o credenciales en código, logs o respuestas
- [ ] las entradas y salidas están validadas y saneadas de forma apropiada
- [ ] los headers, CORS y políticas de transporte están definidos
- [ ] existen límites de rate, throttling o control de abuso cuando corresponde
- [ ] se revisa el manejo de logs y auditoría de acciones sensibles
- [ ] la evidencia de aprobación o mitigación queda registrada
- [ ] el riesgo residual es explícito y conocido por el owner del release

## Criterios de aprobación

- el cambio no introduce vulnerabilidad material o exposición no mitigada;
- los privilegios, secretos y salidas quedan controlados y verificables;
- la evidencia de seguridad está documentada para release.

## Criterios de rechazo

- existen tokens, secretos o permisos demasiado amplios;
- la revisión no logra demostrar control de trust boundaries;
- el cambio puede producir exposición o autorización insegura.

## Riesgos

- bypass de autorización;
- fuga de secretos;
- abuso de exposición por headers, CORS o rate limit;
- logging y auditoría insegura.

## Acciones correctivas

- mover validación de permisos al backend o capa segura;
- externalizar secretos y revisar rotación;
- corregir políticas de headers, logs y CORS;
- bloquear release con evidencia de seguridad insuficiente.

## Ejemplos

Ejemplo: una nueva API con permisos por roles se revisa para confirmar que la validación ocurre en la capa del servidor, que el JWT se valida de forma correcta y que las respuestas no muestran información interna o sensible.

## KPIs

- tiempo medio de cierre de hallazgos de seguridad;
- número de bloqueos de release por seguridad;
- porcentaje de cambios con evidencia de seguridad formal;
- tasa de vulnerabilidades críticas remediadas a tiempo.

## Métricas

- número de hallazgos críticos, altos y medios;
- tiempo entre detección y corrección;
- porcentaje de endpoints con validación autorizativa explícita;
- número de releases con evidencia de seguridad completa.

## Definition of Done

La security review concluye cuando la autenticación, autorización, exposición, manejo de secretos, límites de transporte y evidencia de salida son evaluados y la decisión de aprobación o bloqueo queda registrada con responsable.
