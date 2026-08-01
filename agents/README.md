# Agentes de IA

## Objetivo

Este módulo define la estructura operativa del equipo de IA de AI-STARTUP-KIT como una empresa real de ingeniería de software. Los agentes no son prompts aislados: son roles operativos con lenguaje común, proceso compartido, responsabilidades explícitas, evidencia y gobernanza.

## Principios unificadores

Todos los agentes deben operar con el mismo marco:

- [company](../company): reglas de empresa, flujo, principios y política de release.
- [standards](../standards): estándares técnicos y de calidad.
- [playbooks](../playbooks): procedimientos ejecutables.
- [templates](../templates): artefactos reutilizables.
- [reviews](../reviews): revisiones de calidad, seguridad, QA, arquitectura, performance, UX y release.
- [automation](../automation): arquitectura de automatización futura y comandos conceptuales.
- [memory](../memory): memoria del proyecto, contexto y aprendizaje institucional.

## Lenguaje común de trabajo

Todos los agentes deben responder con estas secciones cuando corresponda:

- Identidad
- Misión
- Responsabilidades
- Límites
- Flujo de trabajo
- Entradas
- Salidas
- Dependencias
- Documentos que consulta
- Documentos que genera
- Checklists
- KPIs
- Definition of Ready
- Definition of Done
- Escalamiento
- Riesgos
- Mejores prácticas
- Errores comunes
- Ejemplos

## Matriz de colaboración

| Fase del proyecto | Product Manager | CTO | FullStack | QA Security | DevOps |
| --- | --- | --- | --- | --- | --- |
| Discovery y definición | Lidera problema, usuario, valor y prioridad | Valida viabilidad técnica y restricciones | Aporta estimación de esfuerzo y complejidad | Define riesgos de calidad y seguridad iniciales | Avisa dependencias de entorno y despliegue |
| Diseño y arquitectura | Define alcance y prioridad | Define arquitectura, decisiones clave y ADR | Traduce el diseño en implementación realista | Revisa seguridad, integración y riesgo funcional | Evalúa compatibilidad operativa y release |
| Implementación | Acompaña alcance y cambios de prioridad | Revisa decisiones y evoluciones arquitectónicas | Entrega código, pruebas y evidencia | Valida calidad y seguridad del cambio | Asegura pipeline, rollout y observabilidad |
| QA y revisión | Valida valor entregado | Revisa impacto arquitectónico y deuda | Corrige con evidencia | Ejecuta la revisión formal y define blockers | Revisa despliegue, rollback y soporte |
| Release y operación | Confirma alineación con valor esperado | Aprueba riesgos técnicos residuales | Cierra implementación y soporte | Cierra evidencias de calidad y seguridad | Ejecuta despliegue y post-release observabilidad |

## Rutas de interacción clave

- Product Manager → CTO: definición de alcance y viabilidad.
- CTO → FullStack: arquitectura y decisiones de diseño asumidas.
- FullStack ↔ QA Security: evidencia de comportamiento, riesgos y validación.
- FullStack ↔ DevOps: release, despliegue, rollback y observabilidad.
- QA Security ↔ CTO: riesgo técnico, seguridad y excepción de diseño.
- Product Manager ↔ DevOps: prioridad de despliegue y entorno.

## Definition of Done del módulo agents

El módulo agents está completo cuando:

- cada agente compartel el mismo idioma, estructura y criterio operativo;
- ninguno actúa como prompt aislado o improvisado;
- todos siguen la misma cadena de contexto, evidencias, revisión y release;
- la colaboración entre agentes queda representada como una empresa de ingeniería real, no como un conjunto de tareas sueltas.
