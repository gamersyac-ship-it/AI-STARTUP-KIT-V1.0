# React

## Objetivo

Definir un conjunto de reglas para construir aplicaciones React mantenibles, escalables, accesibles y apropiadas para entornos de producción.

## Alcance

Aplica a interfaces que usan React, TypeScript, routers, estado local y global, renderización condicional o APIs paginadas.

## Cuándo aplica

Cuando se construye una pantalla, un flujo de navegación, un formulario o una vista basada en datos.

## Principios

- componentes pequeños y reutilizables,
- separación entre UI y lógica de negocio,
- estados locales donde corresponda,
- manejo explícito de errores y carga,
- accesibilidad y rendimiento como requisitos, no como opcionales.

## Buenas prácticas

- Usar Feature Based Architecture y componentes de dominio bien delimitados.
- Preferir hooks para lógica reutilizable.
- Usar `Suspense` y lazy loading para cargas diferidas.
- Usar `TanStack Query` para data fetching y cache.
- Usar `Zustand` o similar para estado global mínimo y estable.
- Usar `React Router` para navegación declarativa y mantenible.

## Anti-patrones

- colocar lógica de negocio dentro del JSX,
- usar estado global sin necesidad,
- mezclar queries y componentes demasiado acoplados,
- servir bundles demasiado grandes sin code splitting.

## Convenciones

- nombres de componentes en PascalCase,
- hooks con prefijo `use`,
- carpetas por feature o por dominio,
- evitar render de lado en componentes sin necesidad.

## Ejemplos correctos

```tsx
function UserCard({ user }: { user: User }) {
  return (
    <article aria-label="User card">
      <h2>{user.name}</h2>
      <p>{user.email}</p>
    </article>
  );
}
```

## Ejemplos incorrectos

```tsx
function Page() {
  const [data, setData] = useState<any>(null);
  useEffect(() => {
    fetch('/api/users').then((res) => res.json()).then(setData);
  }, []);

  return <div>{JSON.stringify(data)}</div>;
}
```

## Checklist

- ¿La UI es accesible?
- ¿El estado está bien localizado?
- ¿El render es eficiente?
- ¿La operación de data fetching está desacoplada de la visualización?

## Definition of Ready

Una interfaz está lista para construir cuando las rutas, el estado y los criterios de interacción están claros.

## Definition of Done

Una interfaz está completa cuando se comporta conforme a la historia, se valida con accesibilidad y performance, y no mezcla responsabilidades.

## KPIs

- tiempo medio de render,
- número de re-renders innecesarios,
- porcentaje de componentes reutilizables,
- tasa de errores por accesibilidad.

## Métricas

- bundle size,
- que la UI sea navegable con teclado,
- tiempo de interacción con datos cargados.

## Herramientas recomendadas

- React Router
- TanStack Query
- Zustand
- React DevTools
- Lighthouse
- Axe

## Librerías recomendadas

- `zustand`
- `@tanstack/react-query`
- `react-router-dom`
- `@testing-library/react`

## Errores comunes

- usar context para todo,
- usar `useEffect` como sustituto de un query manager,
- no considerar lazy loading ni code splitting,
- no ver impacto de accesibilidad.

## Preguntas frecuentes

- ¿Cuándo usar Zustand? Cuando se necesita un estado global pequeño y bien definido.
- ¿Cuándo usar TanStack Query? Cuando el estado viene de servidor y necesita cache, refetch y error-state.

## Referencias internas

- [company/engineering-principles.md](../company/engineering-principles.md)
- [typescript.md](typescript.md)
- [testing.md](testing.md)
- [performance.md](performance.md)
