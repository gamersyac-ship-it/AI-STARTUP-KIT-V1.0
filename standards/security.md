# Security

## Objetivo

Asegurar que el software sea resistente a amenazas comunes, siga principios de seguridad por diseño y conserve la integridad, confidencialidad y disponibilidad del sistema.

## Alcance

Aplica a todos los productos, APIs, integraciones, flujos de autenticación, secretos, manejo de datos sensibles y entornos de despliegue.

## Cuándo aplica

Cuando se define una entrada, flujo de autenticación, acceso a recursos, integración externa o release que exponga datos o permisos.

## Principios

- seguridad desde el diseño,
- mínimo privilegio,
- validación en cada frontera de confianza,
- secretos protegidos,
- observabilidad para incidentes y auditoría.

## Buenas prácticas

- Usar JWT o OAuth según el modelo de acceso requerido.
- Definir RBAC con permisos explícitos por recurso y acción.
- Usar variables de entorno para secrets y configuración.
- Aplicar Helmet, CORS y rate limiting en servicios expuestos.
- Asegurar que SQL injection, XSS, CSRF, SSRF y clickjacking estén cubiertos por diseño y validación.

## Anti-patrones

- aceptar input sin validar,
- guardar secrets en codigo fuente,
- exponer tokens en logs,
- permitir accesos globales sin justificación.

## Convenciones

- toda autenticación debe ser explícita,
- toda autorización debe estar basada en permisos definidos,
- toda secret debe estar externalizado y rotado,
- todos los logging de seguridad deben ser estandarizados.

## Ejemplos correctos

```ts
const token = req.headers.authorization?.replace('Bearer ', '');
```

## Ejemplos incorrectos

```ts
const query = `SELECT * FROM users WHERE email = '${email}'`;
```

## Checklist

- ¿El flujo usa autenticación y autorización real?
- ¿Hay secretos en repositorio?
- ¿Se valida request/response según el contexto?
- ¿Las políticas de CORS, rate limit y headers están configuradas?

## Definition of Ready

Una funcionalidad con impacto de seguridad está lista cuando el riesgo, el alcance de acceso y la estrategia de validación han sido definidos.

## Definition of Done

Una solución se considera segura cuando sus controles de autenticación, autorización, secretos y validación están alineados con el riesgo esperado y la revisión no reporta bloqueantes críticos.

## KPIs

- número de vulnerabilidades críticas abiertas,
- tiempo de resolución de incidentes de seguridad,
- tasa de releases sin hallazgos severos.

## Métricas

- número de secretos expuestos,
- porcentaje de endpoints con rate limit,
- cantidad de endpoints sin revisión de permisos.

## Herramientas recomendadas

- Helmet
- bcrypt / argon2
- JWT libraries
- OWASP ZAP
- Snyk o Dependabot
- CI security scanning

## Librerías recomendadas

- `jsonwebtoken`
- `argon2`
- `helmet`
- `cors`
- `express-rate-limit`

## Errores comunes

- tratar seguridad como una capa final,
- validar solo en frontend,
- usar secretos en archivos de configuración versionados,
- no auditorar endpoints de subida o integración.

## Preguntas frecuentes

- ¿Qué pasa con JWT? Debe manejarse con expiración, revocación o rotación apropiada según la arquitectura.
- ¿Qué es RBAC? Un control de acceso basado en roles y permisos explícitos.

## Referencias internas

- [company/engineering-principles.md](../company/engineering-principles.md)
- [api.md](api.md)
- [logging.md](logging.md)
- [error-handling.md](error-handling.md)
