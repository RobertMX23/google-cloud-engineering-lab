# Matriz de preguntas por fase

## Conteos

- MUST: preguntas obligatorias para cerrar la fase.
- SHOULD: preguntas necesarias cuando afectan diseño, costo, seguridad o aceptación.
- PROBE: preguntas de profundización para respuestas ambiguas o de alto riesgo.

| Fase | MUST | SHOULD | PROBE máximo | Objetivo |
|---|---:|---:|---:|---:|
| V0 Business case | 20 | 8 | 4 | 28 |
| V1 Serverless MVP | 28 | 10 | 6 | 38 |
| V2 Event-driven | 24 | 8 | 6 | 32 |
| V3 Observability | 24 | 10 | 6 | 34 |
| V4 PCA redesign | 32 | 12 | 8 | 44 |
| V5 Agentic extension | 34 | 14 | 10 | 48 |
| TOTAL | 162 | 62 | 40 | 224 |

El promedio esperado es de 37 preguntas por fase. El skill puede cerrar antes si los criterios de salida están satisfechos; puede superar el objetivo si aparecen decisiones críticas derivadas.

## V0 — Business case / CDL — 20 MUST

1. ¿Qué problema de coordinación del cuidado se quiere resolver?
2. ¿Quién es el adulto mayor y qué información mínima se representa?
3. ¿Quién registra una visita y desde qué canal?
4. ¿Quién coordina y quién recibe una alerta?
5. ¿Qué diferencia hay entre B2E, B2B y B2C?
6. ¿Cuál es el flujo manual actual?
7. ¿Cuál es el primer journey con valor demostrable?
8. ¿Qué queda fuera del producto?
9. ¿Qué significa visita retrasada?
10. ¿Qué tipos de alerta existen?
11. ¿Qué KPI demuestra valor?
12. ¿Qué costo o riesgo se quiere reducir?
13. ¿Qué datos son sintéticos en el MVP?
14. ¿Qué datos personales se excluyen?
15. ¿Qué decisiones no puede tomar el sistema?
16. ¿Qué significa IA responsable para CareOps?
17. ¿Qué evidencia debe mostrar el demo?
18. ¿Qué duración tendrá la demostración?
19. ¿Qué criterio permite pasar a V1?
20. ¿Quién aprueba el alcance?

SHOULD: segmento piloto, idioma y accesibilidad, frescura de datos, errores aceptables, integraciones futuras, métricas contra el proceso manual, hipótesis de negocio y riesgos legales.

## V1 — Serverless MVP / ACE — 28 MUST

1. ¿Qué endpoints registran, consultan y actualizan visitas?
2. ¿Qué estados puede tener una visita?
3. ¿Qué campos son obligatorios?
4. ¿Qué formato y zona horaria usan fecha y hora?
5. ¿Cómo se genera el Visit ID?
6. ¿Qué roles existen?
7. ¿Qué puede leer y modificar cada rol?
8. ¿Cómo se autentican usuarios y servicios?
9. ¿Cómo se separan ambientes?
10. ¿Qué APIs se habilitan?
11. ¿Qué región se usa y por qué?
12. ¿Qué esquema tiene Cloud SQL?
13. ¿Qué índices son necesarios?
14. ¿Qué transacciones son atómicas?
15. ¿Qué secretos existen?
16. ¿Cómo se almacenan y rotan?
17. ¿Qué pasa con solicitudes duplicadas?
18. ¿Qué errores devuelve cada endpoint?
19. ¿Qué timeout y retry aplica?
20. ¿Qué logs se generan?
21. ¿Qué métricas iniciales se publican?
22. ¿Qué alerta básica se necesita?
23. ¿Cómo se hace rollback?
24. ¿Cómo se ejecuta cleanup?
25. ¿Qué datos se cargan para demo?
26. ¿Qué prueba confirma el flujo completo?
27. ¿Cuál es el costo máximo mensual?
28. ¿Qué condición permite declarar V1 completa?

SHOULD: paginación, búsqueda, exportación, Cloud Storage, backups, RPO/RTO, versionado API, carga, workstation y condición para cambiar Cloud Run por GKE.

## V2 — Event-driven / ACE — 24 MUST

1. ¿Qué eventos existen?
2. ¿Quién produce cada evento?
3. ¿Quién consume cada evento?
4. ¿Qué esquema tiene cada evento?
5. ¿Cómo se versiona?
6. ¿Qué tópico y suscripción corresponde?
7. ¿Cuánto se retiene?
8. ¿Se requiere ordering?
9. ¿Cómo se deduplican eventos?
10. ¿Qué ocurre ante retry?
11. ¿Qué ocurre ante poison message?
12. ¿Existe dead-letter topic?
13. ¿Qué regla determina retraso?
14. ¿Qué severidad produce cada regla?
15. ¿Qué canal recibe la alerta?
16. ¿Cómo se evita duplicación?
17. ¿Qué estado tiene una alerta?
18. ¿Quién puede reconocerla o cerrarla?
19. ¿Cómo se audita la transición?
20. ¿Qué latencia máxima se acepta?
21. ¿Qué volumen diario se espera?
22. ¿Cómo se prueba backlog?
23. ¿Cómo se hace replay?
24. ¿Qué condición permite declarar V2 completa?

SHOULD: Eventarc, eventos externos, exactly-once o idempotencia, ventanas de silencio, escalación, datos prohibidos, costo por mil eventos y contrato para consumidores.

## V3 — Observability / ACE — 24 MUST

1. ¿Qué SLI mide disponibilidad?
2. ¿Qué SLI mide latencia?
3. ¿Qué SLI mide procesamiento?
4. ¿Qué SLI mide alertas?
5. ¿Qué SLO inicial se compromete?
6. ¿Qué logs estructurados son obligatorios?
7. ¿Qué correlation ID cruza API, evento y alerta?
8. ¿Qué métricas custom se publican?
9. ¿Qué dashboard necesita operaciones?
10. ¿Qué alerta es accionable?
11. ¿Quién recibe cada alerta?
12. ¿Qué severidad tiene cada incidente?
13. ¿Qué runbook corresponde?
14. ¿Cómo se rastrea una solicitud?
15. ¿Cómo se detecta backlog?
16. ¿Cómo se detecta error IAM?
17. ¿Cómo se detecta cuota agotada?
18. ¿Cómo se mide costo por mil eventos?
19. ¿Qué retención tienen logs y trazas?
20. ¿Qué datos se redactan?
21. ¿Qué escenario de fallo se inyecta?
22. ¿Cómo se recupera?
23. ¿Qué postmortem se exige?
24. ¿Qué condición permite declarar V3 completa?

SHOULD: error budget, dependencia externa, synthetic monitoring, alerta de costo, dashboard para instructor, exportación a BigQuery, p95/p99, chaos testing seguro, remediación y señales del agente.

## V4 — PCA redesign — 32 MUST

1. ¿Qué requisitos cambian con escala?
2. ¿Qué requisitos no funcionales son obligatorios?
3. ¿Cloud Run sigue siendo suficiente?
4. ¿Cuándo se justifica GKE?
5. ¿Cloud SQL sigue siendo suficiente?
6. ¿Cuándo se justifica Spanner, AlloyDB o Firestore?
7. ¿Qué patrón regional se elige?
8. ¿Cuál es RTO?
9. ¿Cuál es RPO?
10. ¿Qué backup y restore existen?
11. ¿Cómo se aísla cada tenant?
12. ¿Qué jerarquía de recursos se necesita?
13. ¿Qué roles y separación de funciones aplican?
14. ¿Cómo se gestionan secretos y llaves?
15. ¿Qué datos requieren cifrado adicional?
16. ¿Qué frontera de red existe?
17. ¿Cómo se controla acceso de terceros?
18. ¿Cómo se hace WIF o impersonation?
19. ¿Qué datos alimentan BigQuery?
20. ¿Cuál es retención y lineage?
21. ¿Qué topología de eventos se conserva?
22. ¿Qué CI/CD se usa?
23. ¿Cómo se gestiona Terraform state?
24. ¿Qué módulos son reutilizables?
25. ¿Qué SLO definitivo se propone?
26. ¿Qué costo mensual y por tenant se acepta?
27. ¿Qué crecimiento se modela?
28. ¿Qué migración se documenta?
29. ¿Qué trade-off se registra en cada ADR?
30. ¿Qué riesgos de cumplimiento existen?
31. ¿Qué pruebas de DR y seguridad deben pasar?
32. ¿Qué condición permite declarar V4 completa?

SHOULD: multi-región, private service connectivity, Apigee, analytics, data residency, dependencia NVIDIA, fallback sin GPU, capacidad, canary, soporte, evidencia y límites de portfolio.

## V5 — Agentic extension — 34 MUST

1. ¿Qué problema no resuelve una regla determinística?
2. ¿Cuál es el objetivo exacto del agente?
3. ¿Qué agentes existen?
4. ¿Qué responsabilidad tiene cada agente?
5. ¿Qué acciones son solo lectura?
6. ¿Qué acciones preparan una propuesta?
7. ¿Qué acciones requieren aprobación?
8. ¿Qué acciones están prohibidas?
9. ¿Qué herramientas necesita cada agente?
10. ¿Qué tool es MCP?
11. ¿Qué tool es API directa?
12. ¿Cómo se autentica cada tool?
13. ¿Cómo se valida cada argumento?
14. ¿Cómo se evitan tool-call attacks?
15. ¿Cómo se maneja timeout?
16. ¿Cómo se hace retry seguro?
17. ¿Qué memoria necesita?
18. ¿Qué contexto es de sesión?
19. ¿Qué contexto es persistente?
20. ¿Cómo se hace grounding?
21. ¿Qué fuentes puede consultar?
22. ¿Cómo se citan evidencias?
23. ¿Qué modelo Nemotron se benchmarkea?
24. ¿Qué perfil NIM y GPU requiere?
25. ¿Cuál es el modelo fallback?
26. ¿Qué latencia y costo objetivo existen?
27. ¿Cómo se evalúa task success?
28. ¿Cómo se mide groundedness?
29. ¿Cómo se detecta hallucination?
30. ¿Cómo se prueban prompt injection y fuga?
31. ¿Qué aprobación humana existe?
32. ¿Cómo se audita una decisión?
33. ¿Cómo se revierte una acción?
34. ¿Qué condición permite declarar V5 completa?

SHOULD: A2A, Agent Registry, Agent Identity, embeddings, RAG, retención de conversaciones, enmascaramiento, evaluación offline/online, comparación Rules/Agent/Hybrid, revalidación de modelo, costo por interacción, kill switch y evidencia al instructor.

## Plantilla de cobertura

| Campo | Valor |
|---|---|
| Fase | V0–V5 |
| MUST respondidas | n / total |
| SHOULD respondidas | n / total |
| PROBE usadas | n |
| Requisitos funcionales | REQ-F IDs |
| Requisitos no funcionales | REQ-NF IDs |
| Eventos y datos | DATA/EVENT IDs |
| Decisiones | ADR IDs |
| Criterios de aceptación | ACC IDs |
| Riesgos abiertos | IDs y responsables |
| Estado | NOT_STARTED / IN_PROGRESS / READY / BLOCKED |

