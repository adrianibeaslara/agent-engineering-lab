# Agent Engineering Lab — reglas operativas

## Objetivo

Construir un laboratorio público de conocimiento destilado, decisiones técnicas y evidencia reproducible. Responde en español, explica qué cambió y cómo se comprobó.

Entrada: README.md. Método: docs/project-guide.md. Consulta solo las notas y experimentos relevantes para la petición.

## Decisiones del autor

- El autor elige qué pregunta y qué experimento se inicia. Una propuesta del asistente no es una decisión.
- No crear un experimento, un dataset, una demo o un resultado por iniciativa propia para rellenar la estructura.
- No presentar código generado, notas redactadas o tests ejecutados como aprendizaje acreditado del autor.
- No afirmar que existen resultados, tests o CI cuando todavía no están implementados y verificados.

## Dónde va cada contenido

| Contenido | Destino |
|---|---|
| Conocimiento consolidado | docs/concepts/ |
| Decisión significativa | docs/decisions/ |
| Estudio seleccionado y su evidencia | experiments/NNN-slug/ |
| Código reutilizado entre experimentos | src/agent_lab/, cuando exista esa necesidad |
| Tests deterministas y contratos | tests/ |
| Plantillas de trabajo | docs/templates/ |
| Temario, borradores y memoria personal | Espacio privado de estudio, fuera de este repositorio |

No copiar ni sincronizar automáticamente el vault privado. No modificarlo desde este repositorio salvo instrucción explícita. Career, candidaturas y CV permanecen fuera.

## Antes de implementar

1. Confirmar que la pregunta y el alcance han sido elegidos por el autor.
2. Leer el diseño del experimento.
3. Identificar el baseline, las variantes, los datos y los criterios de evaluación.
4. Proponer estructura antes de cambios extensos y justificar dependencias nuevas.
5. Implementar solo lo necesario. No extraer librerías genéricas sin reutilización real.

## Calidad y reproducibilidad

- Cada experimento documenta configuración, baseline, dataset, métricas, comandos y límites.
- Separar hipótesis de medidas; no elegir solo resultados favorables.
- Los datasets serán sintéticos o públicos y con procedencia conocida. Nunca usar datos de clientes, secretos ni material del empleador.
- Separar tests deterministas de evaluaciones estocásticas.
- Versionar datasets pequeños y resultados ligeros; ignorar credenciales, trazas sensibles y outputs pesados.
- Si cambia código asociado a un resultado, conservar su procedencia o ejecutar y documentar una nueva versión.

## Checks según el estado del proyecto

Ahora: revisar enlaces locales, coherencia de índices, placeholders y ausencia de información privada. No hay tests de aplicación ni CI de código.

Con el primer código seleccionado: configurar pyproject.toml, uv.lock, Ruff, Pytest y GitHub Actions; documentar los comandos reales en README.md. La CI no usará claves ni llamará a LLMs de pago.

Comandos previstos una vez configurados: uv sync --locked --group dev; uv run ruff check .; uv run ruff format --check .; uv run pytest.

## Git

Respetar cambios existentes. Mantener commits descriptivos y cambios acotados. No hacer pull, rebase, reset ni push forzado como efecto colateral. Commit, push y publicación cuando la petición los autorice.
