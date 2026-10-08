# Plantilla — resultados

Crear results.md dentro del experimento cuando existan medidas. Una tabla sin ejecutar no es un resultado.

# Resultados — [experimento]

Estado: [ejecutado / revisado]. Fecha: [YYYY-MM-DD].

## Procedencia de la ejecución

[Código o commit, dataset, configuración, modelo si aplica, comando y reporte.]

## Medidas

| Variante | Métrica | Valor observado | Casos evaluados |
|---|---|---|---|
| [Método] | [Métrica con denominador definido] | [Medida] | [N] |

[Coste y latencia cuando apliquen. No usar cero para información desconocida.]

## Análisis de errores

| Caso | Esperado | Observado | Causa candidata | Próxima comprobación |
|---|---|---|---|---|
| [ID] | [Referencia] | [Resultado] | [Hipótesis] | [Acción] |

## Incertidumbre y límites

[Tamaño muestral, varianza, sesgos, cobertura y condiciones que faltan.]

## Interpretación

[Qué se observó. Distinguir medida de explicación causal.]

## Decisión

[Qué decisión cambia, para qué condiciones y por qué.]

## Siguiente pregunta

[Qué incertidumbre merece otro estudio. No iniciar automáticamente un nuevo experimento.]
