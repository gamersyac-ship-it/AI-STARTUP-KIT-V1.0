# Database

## Objetivo

Definir reglas para modelar, evolucionar y operar bases de datos con integridad, rendimiento y trazabilidad.

## Alcance

Aplica a persistencia relacional y no relacional cuando el proyecto requiera integración de bases de datos con un modelo estable.

## Cuándo aplica

Cuando se define el modelo de negocio, una migración, índice o operación de consulta.

## Principios

- normalización y consistencia,
- integridad referencial,
- trazabilidad de cambios,
- auditoría y seguridad,
- rendimiento medido y controlado.

## Buenas prácticas

- Normalizar para reducir redundancia.
- Usar relaciones explícitas y claves consistentes.
- Crear índices solo cuando el patrón de consulta lo justificue.
- Usar migraciones versionadas y reversibles.
- Implementar soft delete y auditoría cuando sea necesario.

## Anti-patrones

- duplicar información en varias tablas,
- usar texto libre donde debería haber relación,
- crear índices sin evidencia de consulta,
- hacer cambios directos en BD sin migración.

## Convenciones

- nombres legibles y consistentes,
- columnas de auditoría y timestamps explícitas,
- constraints declarativas donde el modelo lo permita,
- versionado de migraciones asociado al release.

## Ejemplos correctos

```sql
CREATE TABLE users (
  id UUID PRIMARY KEY,
  email TEXT NOT NULL UNIQUE,
  created_at TIMESTAMPTZ NOT NULL DEFAULT NOW()
);
```

## Ejemplos incorrectos

```sql
ALTER TABLE users ADD COLUMN role TEXT;
```

## Checklist

- ¿La base de datos refleja el dominio del negocio?
- ¿Las relaciones son claras y verificables?
- ¿La migración es versionada y segura?
- ¿Hay una estrategia de auditoría y borrado lógico?

## Definition of Ready

Una migración o modelo de datos está listo cuando el dominio, restricción y el patrón de acceso están suficientemente definidos.

## Definition of Done

La base de datos queda lista para entrega cuando su modelado, integridad y estrategia de revisión están documentados y validados.

## KPIs

- tiempo de diagnóstico de consultas lentas,
- tasa de errores por integridad de datos,
- cobertura de migraciones versionadas.

## Métricas

- tiempo medio de consulta,
- tasa de uso de índices,
- número de migraciones sin rollback plan.

## Herramientas recomendadas

- PostgreSQL
- Prisma
- Flyway o Liquibase
- pgAdmin o DBeaver

## Librerías recomendadas

- `prisma`
- `drizzle`
- `sequelize` (solo en contextos ya definidos)

## Errores comunes

- no documentar el modelo de datos,
- tratar migración como tarea de despliegue sin validación,
- relaciones sin constraints claras,
- dependencias de la base de datos no soportadas en tests.

## Preguntas frecuentes

- ¿Cuándo usar soft delete? Cuando el dato necesita trazabilidad y recuperación controlada.
- ¿Cuándo elegir PostgreSQL? Cuando se necesita robustez transaccional, consultas complejas y soporte serio de integridad.

## Referencias internas

- [company/engineering-principles.md](../company/engineering-principles.md)
- [api.md](api.md)
- [security.md](security.md)
- [testing.md](testing.md)
