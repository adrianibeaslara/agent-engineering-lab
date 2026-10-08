# Código reutilizable

[Portada](../README.md) · [Método](../docs/project-guide.md)

Esta carpeta recibirá componentes que varios experimentos necesiten compartir.

## Criterio de extracción

Empieza con código junto al experimento. Extrae un componente cuando exista una reutilización real y un contrato estable que se pueda probar.

El destino previsto es src/agent_lab/. Todavía no existe una librería ni un paquete importable.

## Con el primer código

Configurar pyproject.toml y uv.lock; documentar instalación y comandos reales. Usar funciones pequeñas y type hints en los componentes compartidos.

No añadir frameworks de agentes, adaptadores ni dependencias para anticipar necesidades que todavía no han aparecido.
