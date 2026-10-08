# 001 — Separar estudio privado y evidencia pública

Estado: adoptada. Fecha: 2026-10-08.

## Contexto

El proyecto combina aprendizaje personal y publicaciones técnicas. El estudio necesita borradores, un backlog amplio y continuidad; una publicación necesita un alcance claro y evidencia que otra persona pueda examinar.

## Alternativas consideradas

1. Publicar todo el espacio de estudio junto al código.
2. Mantener un repositorio exclusivamente de código y demos.
3. Separar el estudio privado de un laboratorio público con conocimiento destilado, decisiones y experimentos.

## Decisión

Adoptar la tercera opción.

El temario, los apuntes sin estructurar, las fuentes de trabajo y la memoria permanecen en el espacio privado. El repositorio público contiene notas consolidadas, decisiones reales, diseños seleccionados y resultados verificables.

El autor decide qué experimento iniciar. La infraestructura y las propuestas del asistente no equivalen a una decisión del autor ni a evidencia de aprendizaje.

## Consecuencias

- La publicación exige revisión y una razón concreta para compartir el material.
- El repositorio puede crecer sin replicar el backlog completo.
- No hay sincronización automática del espacio privado hacia GitHub.
- La portada refleja el estado real; una base documental no se presenta como un laboratorio con resultados.
- Los estudios se incorporan cuando el autor haya elegido la pregunta y el alcance.
- El primer código activará el entorno, los tests y la CI que necesite.

## Revisión

Revisar si la separación dificulta localizar evidencia o mantener enlaces. Resolverlo mediante índices y referencias estables antes de introducir una sincronización automática.
