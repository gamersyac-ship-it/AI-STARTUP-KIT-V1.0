# Accessibility Review

## Objetivo

Confirmar que una interfaz o flujo de usuario es usable, comprensible y operable para personas con diversas capacidades, sin introducir barreras evitables en el acceso, entendimiento o interacción.

## Cuándo ejecutarlo

- en toda interfaz nueva o modificada;
- cuando cambian flujos principales de navegación o formularios;
- antes del release de UX o UI con impacto de usuario;
- cuando una revisión de diseño o QA identifica riesgo de uso.

## Responsable

- UX Lead o Product Designer: evalúa flujo, claridad y navegación.
- QA Lead: valida comportamiento observable en pruebas.
- FullStack o Frontend owner: corrige accesibilidad técnica y semántica.
- Security o Product Manager: participan cuando hay riesgos de exclusión o cumplimiento.

## Checklist completo

- [ ] los componentes tienen etiquetas semánticas apropiadas
- [ ] el foco y el orden de navegación son lógicos
- [ ] los controles son operables con teclado y soporte de lector
- [ ] los contrastes cumplen con el estándar aceptable
- [ ] la información importante no depende solo del color
- [ ] los mensajes de error son claros y asociados al control correcto
- [ ] los formularios tienen instrucciones y validación comprensibles
- [ ] las animaciones y cambios de estado no producen confusión o pérdida de contexto
- [ ] las imágenes y iconos aportan texto o alternativa accesible
- [ ] las pantallas se pueden usar con tamaño de fuente ampliado o zoom razonable

## Criterios de aprobación

- el flujo de uso es operable sin barreras evitables;
- los controles y mensajes se comprenden por usuarios con diversidad funcional;
- la evidencia de validación y corrección queda registrada.

## Criterios de rechazo

- la interfaz requiere interacción no accesible con teclado o lector;
- la información crítica se entrega solo visualmente;
- los errores, navegación o foco confunden al usuario.

## Riesgos

- exclusión funcional de usuarios y pérdida de adopción;
- errores de uso replicados en producción;
- cumplimiento y reputación afectados por experiencia poco usable.

## Acciones correctivas

- corregir etiquetas, foco y orden de navegación;
- reescribir mensajes y validaciones;
- ajustar contrastes, semántica y soporte de lectura;
- someter el flujo a verificación manual y automatizada.

## Ejemplos

Ejemplo: un modal de “confirmación” requiere que el foco se mueva al texto principal y que el botón de cierre sea operable por teclado. La revisión de accesibilidad bloquea el cambio si el flujo no permite la navegación completa sin ratón.

## KPIs

- tasa de errores de accesibilidad en componentes críticos;
- porcentaje de pantallas con validación accesible;
- tiempo de corrección por hallazgo de accesibilidad;
- tasa de rechazo o rework por UX accesible.

## Métricas

- número de hallazgos críticos o mayores;
- cantidad de flujos con contraste o foco defectuoso;
- porcentaje de validación por componente;
- tasa de disminución de incidencias por assistive tech.

## Definition of Done

La accessibility review termina cuando las barreras de uso evitables han sido eliminadas, la evidencia de validación está documentada y la aprobación o bloqueo queda registrado con responsable.
