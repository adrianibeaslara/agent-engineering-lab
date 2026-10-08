# Tests y evaluaciones

[Portada](../README.md) · [Método](../docs/project-guide.md)

Todavía no hay código de aplicación ni tests ejecutables. Esta carpeta documenta el criterio de verificación para el primer experimento elegido.

## Tests deterministas

Probar lógica, parsing, contratos, permisos, condiciones de parada y fallos de tools simulados cuando existan esos componentes.

Usar casos pequeños cuyo resultado esperado pueda justificarse independientemente de la implementación.

## Evaluaciones

La calidad de outputs y trayectorias se evalúa con datasets identificados, criterios explícitos y análisis de varianza cuando corresponda.

Las ejecuciones con modelos reales permanecerán fuera de la CI ordinaria y tendrán presupuesto documentado.

## Activación

Añadir Pytest, Ruff y CI junto al primer código. La CI no requerirá claves ni servicios de pago. Documentar comandos reales en la portada antes de afirmar que los checks están disponibles.
