# Clean Architecture

## Objetivo

Definir una estructura de software donde las reglas del negocio permanezcan independientes del framework, UI, base de datos y transporte.

## Alcance

Este estándar aplica a sistemas con cambios frecuentes, equipos múltiples y necesidad de crecimiento sostenido.

## Cuándo aplica

Cuando se diseña un nuevo dominio, un servicio, un producto o un módulo con potencial de evolución.

## Principios

- separación de responsabilidades,
- dependencias dirigidas hacia el núcleo,
- entidades estables y casos de uso claros,
- interfaces y adaptadores bien definidos,
- desacoplamiento del transporte e infraestructura.

## Buenas prácticas

- Definir el dominio central antes de la infraestructura.
- Hacer que los casos de uso dependan de interfaces y no de implementaciones concretas.
- Mantener el flujo del negocio explícito y verificable.

## Anti-patrones

- lógica de dominio dentro de controladores,
- acoplamiento fuerte a framework,
- repositorios u orquestadores con demasiadas responsabilidades.

## Convenciones

- las entidades representan la realidad del negocio,
- los casos de uso describen la intención del sistema,
- los adaptadores permiten la integración con infraestructuras.

## Ejemplos correctos

```ts
interface UserRepository {
  save(user: User): Promise<void>;
}

class RegisterUser {
  constructor(private readonly repository: UserRepository) {}

  async execute(user: User): Promise<void> {
    await this.repository.save(user);
  }
}
```

## Ejemplos incorrectos

```ts
class UserController {
  async create(req: Request) {
    await prisma.user.create({ data: req.body });
  }
}
```

## Checklist

- ¿Las dependencias fluyen hacia el núcleo?
- ¿El dominio es independiente del framework?
- ¿Los casos de uso son claros y reutilizables?
- ¿Las interfaces están definidas por intención y no por implementación?

## Definition of Ready

Una arquitectura está lista cuando el contexto del problema, los casos de uso y los límites tecnológicos están definidos.

## Definition of Done

La arquitectura queda aprobada cuando la separación de capas y dependencias pueden sostener el crecimiento sin acoplamiento excesivo.

## KPIs

- reducción de acoplamiento entre capas,
- tasa de cambios de infraestructura que afectan el dominio,
- tiempo para agregar un nuevo adaptador o caso de uso.

## Métricas

- número de dependencias directas de framework en dominio,
- tasa de cambios en capas de infraestructura,
- complejidad de integración entre módulos.

## Herramientas recomendadas

- diagramas de arquitectura,
- ADRs,
- revisión de dependencias,
- pruebas de integración.

## Librerías recomendadas

- patrones de ports/adapters,
- inyección de dependencias,
- validación de contratos.

## Errores comunes

- empezar con infraestructura antes que modelo de negocio,
- introducir frameworks como núcleo del diseño,
- mezclar casos de uso y transporte.

## Preguntas frecuentes

- ¿Cuándo se usa Clean Architecture? Cuando el sistema necesita evolución y colaboración entre múltiples equipos.
- ¿Qué pasa si el proyecto es pequeño? Sigue siendo útil, pero se puede simplificar sin romper el principio.

## Referencias internas

- [company/engineering-principles.md](../company/engineering-principles.md)
- [node.md](node.md)
- [api.md](api.md)
