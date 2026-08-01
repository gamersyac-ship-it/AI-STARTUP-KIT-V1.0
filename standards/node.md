# Node

## Objetivo

Definir una arquitectura de servicios Node.js clara, segura, testable y compatible con crecimiento real de producto.

## Alcance

Aplica a APIs, workers, procesos de backend, servicios de dominio y capas de infraestructura en runtimes Node.js.

## Cuándo aplica

Cuando se construye un servicio HTTP, un worker, una integración o un flujo de operación en Node.js.

## Principios

- controladores delgados,
- servicios con lógica de negocio,
- repositorios para acceso a persistencia,
- middlewares para validación e integración,
- logging y diagnósticos estructurados,
- seguridad por default.

## Buenas prácticas

- Separar controllers de services y repositories.
- Usar DTOs para tipar el ingreso y salida de la capa de transporte.
- Usar inyección de dependencias cuando el servicio lo requiera.
- Centralizar validación y error manejo.
- Tratar configuración como un recurso explícito y seguro.

## Anti-patrones

- lógica en el controlador,
- acceso directo a BD en rutas,
- usar `any` por defecto,
- ocultar configuración con env var no documentada.

## Convenciones

- los controllers solo coordinan,
- los services contienen lógica de negocio,
- los repositories encapsulan persistencia,
- los middlewares son reusable y no acoplan el flujo.

## Ejemplos correctos

```ts
class UserService {
  constructor(private readonly userRepository: UserRepository) {}

  async createUser(input: CreateUserDto) {
    return await this.userRepository.save(input);
  }
}
```

## Ejemplos incorrectos

```ts
app.post('/users', async (req, res) => {
  const user = await prisma.user.create({ data: req.body });
  res.json(user);
});
```

## Checklist

- ¿El flujo está dividido por responsabilidad?
- ¿La validación está en el borde apropiado?
- ¿El servicio expone una interfaz clara?
- ¿La salida puede trazarse en logs y tests?

## Definition of Ready

Un servicio Node está listo cuando el alcance del endpoint o proceso está claro, el contrato está definido y la capa de persistencia está identificada.

## Definition of Done

Un servicio Node queda completo cuando tiene lógica separada, manejo de error consistente, validación y trazabilidad operativa.

## KPIs

- tiempo de incorporación de nuevos desarrolladores,
- tasa de fallos por acoplamiento de rutas a infraestructura,
- tasa de errores por validación no manejada.

## Métricas

- porcentaje de endpoints con DTOs y validación explícita,
- cantidad de rutas con lógica de negocio mezclada,
- tiempo de diagnóstico de incidentes.

## Herramientas recomendadas

- Express/Fastify
- Prisma
- Zod o class-validator
- pino / winston
- OpenTelemetry

## Librerías recomendadas

- `zod`
- `class-validator`
- `reflect-metadata`
- `@nestjs/common` (si se usa arquitectura más formal)

## Errores comunes

- hacer controllers demasiado pesados,
- mezclar repositorio, servicio y transporte,
- no normalizar errores a nivel de la API.

## Preguntas frecuentes

- ¿Cuándo usar DTO? Cuando hay entrada y salida que deben responder a un contrato explícito.
- ¿Cuándo usar inyección de dependencias? Cuando la lógica necesita sustituibilidad y testing más limpio.

## Referencias internas

- [company/engineering-principles.md](../company/engineering-principles.md)
- [api.md](api.md)
- [database.md](database.md)
- [logging.md](logging.md)
