# Registro de experimentos

[Portada](../README.md) · [Método](../docs/project-guide.md) · [Plantilla](../docs/templates/experiment.md)

## Estado

**No hay experimentos seleccionados ni resultados publicados.** El primer estudio lo elegirá el autor.

## Iniciar un estudio

1. Elegir la pregunta y el alcance.
2. Definir baseline, variantes, dataset y métricas.
3. Crear NNN-slug/ con un README basado en la plantilla.
4. Añadir código y datos únicamente si el diseño los necesita.
5. Registrar medidas en results.md después de ejecutar.

La numeración identifica estudios elegidos. Una propuesta en una issue no reserva un número ni se presenta como experimento activo.

## Estructura de un experimento

```text
NNN-slug/
├── README.md       # Diseño, configuración y cómo reproducir
├── run.py          # Cuando haga falta código
├── cases.jsonl     # Cuando haya datos pequeños versionables
└── results.md      # Cuando existan medidas
```

Cada estudio debe poder entenderse desde su README. El formato de los datos depende del problema; JSONL es una opción, no una obligación.

## Añadir al registro

Cuando exista un diseño elegido, enlázalo aquí con su estado. Al publicar resultados, resume también la conclusión y su límite en la portada.
