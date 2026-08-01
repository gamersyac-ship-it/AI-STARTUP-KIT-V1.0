# Dependencies

## Objetivo

Definir una política profesional para agregar, mantener y eliminar dependencias sin introducir deuda técnica o riesgo de seguridad innecesario.

## Alcance

Aplica a librerías, paquetes, runtimes, plugins, SDKs y servicios de terceros usados por el código.

## Cuándo aplica

Antes de agregar una dependencia y durante su actualización, revisión o retiro.

## Principios

- dependencia por necesidad,
- mantenimiento y seguridad verificables,
- mínimo imprescindible,
- trazabilidad de adopción y retiro.

## Buenas prácticas

- Usar dependencias con mantenimiento activo y comunidad sólida.
- Revisar vulnerabilidades, licencias y compatibilidad antes de instalar.
- Preferir pequeñas dependencias bien mantenidas a stacks gigantes.
- Mantener lockfiles y un registro claro de versiones.

## Anti-patrones

- packages por moda,
- instalar sin revisar licencia,
- acumular utilidades duplicadas,
- no retirar bibliotecas obsoletas.

## Convenciones

- todo paquete añadido requiere explicación de por qué se necesita,
- cambios grandes de dependencias deben pasar por revisión técnica,
- upgrades deben estar acompañados de validación de compatibilidad y releases.

## Ejemplos correctos

- añadir una librería de validación porque la validación de contratos es un requisito real y reutilizable.

## Ejemplos incorrectos

- instalar una librería de rutas simplemente porque “más tarde podrá servir”.

## Checklist

- ¿La dependencia resuelve una necesidad clara?
- ¿Tiene soporte y mantenimiento actual?
- ¿La licencia del paquete es compatible con el proyecto?
- ¿El riesgo de seguridad y compatibilidad se evaluó?

## Definition of Ready

Una dependencia está lista para ser incorporada cuando la necesidad y el reemplazo posible están claros.

## Definition of Done

Una dependencia queda integrada cuando su adopción está validada, documentada y compatible con la política de seguridad y mantenimiento.

## KPIs

- número de dependencias no mantenidas,
- tasa de dependencias con vulnerabilidades conocidas,
- reducción de paquetes redundantes.

## Métricas

- paquetes por proyecto,
- dependencias sin propietario,
- número de actualizaciones pendientes por riesgo o seguridad.

## Herramientas recomendadas

- Dependabot
- Snyk
- npm audit / pnpm audit
- Renovate

## Librerías recomendadas

- herramientas de seguridad y actualización automatizada.

## Errores comunes

- mantener paquetes sin revisar actualización,
- usar pequeñas utilidades que se vuelven redundantes,
- no revisar compatibilidad tras un upgrade.

## Preguntas frecuentes

- ¿Cuándo eliminar una dependencia? Cuando su valor ya no es necesario o se ha reemplazado por una solución más segura o simple.
- ¿Qué es más importante: reducción de dependencias o velocidad? La reducción de riesgo y mantenimiento suele priorizarse.

## Referencias internas

- [security.md](security.md)
- [performance.md](performance.md)
- [company/release-policy.md](../company/release-policy.md)
