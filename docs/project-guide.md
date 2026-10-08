# Método de trabajo

[Portada](../README.md) · [Índice](index.md) · [Experimentos](../experiments/README.md)

## Dos espacios con funciones distintas

| Espacio | Función | Contenido |
|---|---|---|
| Estudio privado | Aprender, explorar y recordar | Temario, backlog, fuentes, apuntes sin estructurar y continuidad |
| Repositorio público | Explicar decisiones y compartir evidencia | Notas maduras, ADRs, diseños elegidos, código, datos publicables y resultados |

El repositorio no copia automáticamente el espacio de estudio. Una nota se publica porque aporta una comprensión reusable y tiene suficiente respaldo.

## Elegir una pregunta

El autor elige la pregunta. Un asistente puede proponer alternativas y ayudar a concretarlas, pero no inicia un estudio como si la propuesta ya estuviera aceptada.

Una pregunta útil delimita una decisión: qué alternativas se comparan, bajo qué condiciones y qué observación haría cambiar de opinión.

## Preparar una nota

Usa la [plantilla de concepto](templates/concept.md). Distingue definición, modelo mental, interpretación propia, fuente y evidencia. Incluye alternativas, trade-offs y contraejemplos.

Publica una nota cuando ayude a comprender o decidir. Haber leído una fuente o reformateado apuntes no acredita dominio.

## Diseñar un experimento

Usa la [plantilla de experimento](templates/experiment.md) después de que el autor elija el alcance.

Define antes de ejecutar:

- La pregunta, una hipótesis falsable y la decisión que podría cambiar.
- Un baseline y variantes comparables.
- La unidad de evaluación, los datos, las etiquetas y sus límites.
- Las métricas y el criterio de mejora.
- La configuración, el presupuesto y las condiciones de parada.
- Los fallos que conviene observar y cómo reproducir la ejecución.

Crea experiments/NNN-slug/ cuando exista un diseño elegido. Cada estudio tiene su README, datos pequeños cuando apliquen, script reproducible cuando sea necesario y results.md cuando haya medidas.

## Implementar

Empieza con código local al experimento. Extrae componentes a src/agent_lab/ cuando varios estudios los reutilicen.

Con el primer código elegido, configura Python, uv, pyproject.toml, uv.lock, Ruff y Pytest. La CI ejecutará los checks documentados, sin secretos ni llamadas a servicios de pago.

Las versiones y los comandos concretos se fijarán en ese cambio. En este esqueleto todavía no hay entorno de aplicación ni checks de código configurados.

## Medir e interpretar

Usa la [plantilla de resultados](templates/results.md). Explica tamaños muestrales, denominadores, segmentos, costes y latencias cuando apliquen. Separa el efecto observado de la interpretación.

Los resultados negativos y la ausencia de mejora también se publican. No extrapoles un resultado pequeño o sintético a rendimiento de producción.

Si el experimento no usa un LLM, no inventes tokens ni consumo de API. Si lo usa, registra modelo, versión o identificador, parámetros, fecha, número de llamadas y coste observado.

## Tests y evaluaciones

Tests: lógica determinista, parsing, contratos, permisos y fallos de tools simulados.

Evaluaciones: calidad de resultados, trayectorias y comportamiento estocástico sobre un dataset identificado.

No conviertas una evaluación variable en un test unitario supuestamente determinista. La [guía de tests](../tests/README.md) define el punto de partida.

## Publicar

Antes de enlazar una entrega desde la portada, comprueba que otra persona pueda entenderla y, cuando haya código, ejecutarla.

Mantén trazabilidad entre datos, código, configuración y resultados. Comprueba enlaces, comandos y procedencia de datasets. Cada entrada declara su estado real: propuesta, diseño elegido, ejecutado o revisado.

La licencia se elegirá explícitamente. Las memorias personales, datos de clientes, credenciales y propiedad intelectual del trabajo permanecen fuera del repositorio.

## Mantener el aprendizaje

La continuidad y el progreso del temario se registran en privado. Un tema se cierra con evidencia de comprensión del autor, no por la existencia de una nota o de código generado.

Actualiza índices y enlaces cuando cambie una publicación. Usa ADRs solo cuando exista una decisión significativa con alternativas y consecuencias.
