# Contrato del banco de preguntas CDL 2026

**ID:** CDL-QB-2026-001  
**Versión:** 2026.1  
**Fuente canónica:** `CDL_QUESTION_BANK_2026.yaml`

## Propósito

Este banco permite generar sesiones de práctica aleatorias para Cloud Digital Leader. Las preguntas son representativas y educativas; no son preguntas filtradas ni predicen el resultado del examen.

## Estructura obligatoria

Cada pregunta debe tener:

- `id` estable e irrepetible;
- dominio del blueprint;
- nivel de dificultad;
- tipo de pregunta;
- opciones y respuesta esperada;
- conceptos evaluados;
- relación con CareOps V0–V5.

## Reglas de sorteo

1. No repetir una pregunta dentro de la misma sesión.
2. Una sesión estándar tendrá 10 preguntas: al menos una por dominio y cuatro distribuidas proporcionalmente.
3. Una sesión completa tendrá 30 preguntas: cinco por dominio.
4. Una sesión de IA tendrá 12 preguntas: al menos ocho de `artificial-intelligence` y `trust-security`.
5. Alternar preguntas `single_choice` y `multi_select` cuando el tamaño de la sesión lo permita.
6. No revelar `answer` antes de que el usuario responda.
7. Después de cada respuesta, mostrar: resultado, explicación breve, concepto, dominio y vínculo con CareOps.
8. Registrar intentos, aciertos, errores y preguntas pendientes, sin modificar el texto canónico.

## Criterio de preparación

Se considera dominio alcanzado cuando el usuario obtiene:

- mínimo 80% en dos sesiones completas consecutivas;
- mínimo 80% en una sesión específica de IA;
- explicación correcta de al menos seis decisiones de servicio;
- identificación de riesgos de seguridad y trade-offs;
- capacidad de relacionar la respuesta con un caso CareOps.

## Mantenimiento

La guía oficial de certificación y el Learning Path de Google Skills son la autoridad. Coursera, codelabs y repositorios sirven como material complementario. Si cambia el blueprint, se incrementa la versión del banco y no se borran preguntas antiguas: se marcan como `legacy` o se reemplazan mediante un registro de cambio.

## Política de uso

El banco se utilizará exclusivamente dentro del repositorio `RobertMX23/google-cloud-engineering-lab`. No se copiarán preguntas protegidas, dumps de examen ni contenido confidencial de proveedores.
