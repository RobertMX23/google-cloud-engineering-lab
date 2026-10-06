# Guía para contribuir

La arquitectura y distribución obligatorias están definidas en [`REPOSITORY_ARCHITECTURE_CONTRACT.md`](REPOSITORY_ARCHITECTURE_CONTRACT.md). Ese contrato es la fuente de verdad para clasificar recursos, organizar PDFs y publicar cambios.

## Organización

- Clasifica cada recurso por certificación y área del examen antes de añadirlo.
- Usa `shared/` únicamente para material transversal o referencias originales.
- Mantén un README junto a cada lab con objetivo, prerrequisitos, pasos, limpieza y evidencia esperada.
- No dupliques repositorios externos; registra la fuente y su enlace en el recurso correspondiente.

## Convenciones de labs

Cada lab debe documentar:

1. objetivo y relación con el blueprint;
2. costo estimado y recursos creados;
3. prerrequisitos y variables de configuración;
4. procedimiento reproducible;
5. validaciones y evidencia;
6. limpieza y riesgos.

## Cambios

Prefiere cambios pequeños y verificables. Actualiza el README del área cuando cambie la taxonomía.

Antes de publicar cambios estructurales, compara siempre el estado local con `origin/main`, verifica la estructura resultante y confirma que los hashes local y remoto coincidan después del push.
