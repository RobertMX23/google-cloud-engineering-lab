# Cloud Digital Leader: matriz de preguntas y conocimientos

**Propósito:** convertir la guía de CDL en preguntas básicas de estudio y conectarlas con las fases V0–V5 de CareOps Cloud.

La guía local cubre seis dominios. La página oficial de certificación confirma la misma estructura, un examen de 50–60 preguntas de opción múltiple y selección múltiple, 90 minutos y sin prerrequisitos técnicos. Estas no son preguntas filtradas del examen; son preguntas representativas para comprobar dominio conceptual. [Información oficial CDL](https://cloud.google.com/learn/certification/cloud-digital-leader)

## 1. Qué debe dominarse

| Dominio | Peso guía | Conocimiento esperado |
|---|---:|---|
| Transformación digital | ~18% | Valor cloud, arquitecturas, red global, regiones, zonas, IaaS/PaaS/SaaS y trade-offs |
| Datos | ~18% | Valor del dato, database/warehouse/lake, tipos de datos, gobierno, BigQuery, Cloud Storage y pipelines |
| IA | ~18% | AI/ML/gen AI, calidad de datos, IA responsable, Gemini, agentes, APIs y AI Hypercomputer |
| Modernización | ~18% | Migración, VM, contenedores, microservicios, Kubernetes, serverless, APIs y multicloud |
| Confianza y seguridad | ~18% | Amenazas, responsabilidad compartida, IAM, cifrado, zero trust, resiliencia y servicios de seguridad |
| Operaciones | ~10% | CapEx/OpEx, TCO, jerarquía de recursos, presupuestos, observabilidad, SLI/SLO/SLA y resiliencia |

## 2. Preguntas básicas y conocimiento requerido

### CDL-01 — Transformación digital

| ID | Pregunta representativa | Debo poder explicar | Evidencia CareOps |
|---|---|---|---|
| CDL-01 | ¿Qué problema empresarial resuelve migrar a cloud? | Escalabilidad, agilidad, velocidad, alcance global, seguridad, datos y foco estratégico | V0: business case y problema manual |
| CDL-02 | ¿Cuál es la diferencia entre cloud pública, privada, híbrida y multicloud? | Cuándo usar cada arquitectura y qué trade-offs introduce | V0/V4: matriz de arquitectura |
| CDL-03 | ¿Qué diferencia hay entre IaaS, PaaS y SaaS? | Qué administra el cliente y qué administra el proveedor | V0/V1: Cloud Run frente a VM |
| CDL-04 | ¿Qué diferencia hay entre región, zona y edge location? | Disponibilidad, latencia, residencia y costo | V1/V4: decisión de región y DR |
| CDL-05 | ¿Qué son IP, DNS, latencia y ancho de banda? | Cómo afectan conectividad y experiencia de usuario | V1/V4: API y topología de red |

### CDL-02 — Data Transformation

| ID | Pregunta representativa | Debo poder explicar | Evidencia CareOps |
|---|---|---|---|
| CDL-06 | ¿Por qué los datos crean valor empresarial? | Insights, tendencias, decisiones, automatización y combustible para IA | V0: KPIs y modelo de valor |
| CDL-07 | ¿Cuál es la diferencia entre database, data warehouse y data lake? | Operación transaccional, analítica estructurada y datos crudos | V1/V2/V4: Cloud SQL, BigQuery y Storage |
| CDL-08 | ¿Qué diferencia hay entre datos estructurados, semiestructurados y no estructurados? | Cómo cambia almacenamiento, procesamiento y análisis | V0/V2/V5: visitas, eventos y documentos |
| CDL-09 | ¿Qué es gobierno de datos y por qué importa? | Propiedad, calidad, acceso, retención, lineage y cumplimiento | V0/V4: clasificación y lineage |
| CDL-10 | ¿Cuándo usar Cloud Storage, Cloud SQL, BigQuery, Spanner, Bigtable o Firestore? | Patrón de acceso, escala, consistencia, costo y estructura | V1/V4: ADR de datos |

### CDL-03 — Artificial Intelligence

| ID | Pregunta representativa | Debo poder explicar | Evidencia CareOps |
|---|---|---|---|
| CDL-11 | ¿Cuál es la diferencia entre AI, ML, generative AI y business intelligence? | Automatización, aprendizaje, generación y análisis descriptivo | V0: alcance sin IA |
| CDL-12 | ¿Qué problema resuelve ML frente a una regla determinística? | Patrones complejos y escala; no usar ML si una regla es suficiente | V2/V5: Rules vs Agent vs Hybrid |
| CDL-13 | ¿Por qué la calidad de datos importa para IA? | Completeness, uniqueness, timeliness, validity, accuracy y consistency | V0/V2/V5: calidad de eventos |
| CDL-14 | ¿Qué significa IA responsable y explicable? | Seguridad, sesgo, privacidad, transparencia, supervisión y límites | V0/V5: no diagnóstico y aprobación humana |
| CDL-15 | ¿Cuándo usar una API preentrenada, un modelo fundacional o un modelo custom? | Velocidad, esfuerzo, diferenciación, costo, control y expertise | V5: adapter y benchmark de modelos |

### CDL-04 — Modernize Infrastructure and Applications

| ID | Pregunta representativa | Debo poder explicar | Evidencia CareOps |
|---|---|---|---|
| CDL-16 | ¿Qué significan rehost, replatform, refactor, retire y retain? | Estrategias de migración y sus costos/riesgos | V0/V4: migración de CareOps |
| CDL-17 | ¿Qué es una VM y cuándo conviene? | Control, compatibilidad, operación y costo | V1/V4: Cloud Run vs Compute Engine |
| CDL-18 | ¿Qué es un contenedor y qué aporta Kubernetes? | Portabilidad, empaquetado, orquestación y complejidad operativa | V1/V4: GKE como referencia |
| CDL-19 | ¿Qué es serverless y cuál es el valor de Cloud Run? | Escala bajo demanda, menor operación y límites del modelo | V1: CareOps serverless |
| CDL-20 | ¿Qué valor aporta una API y qué hace Apigee? | Exponer, controlar, monetizar y gobernar capacidades | V1/V4/V5: APIs y tools |

### CDL-05 — Trust and Security

| ID | Pregunta representativa | Debo poder explicar | Evidencia CareOps |
|---|---|---|---|
| CDL-21 | ¿Qué amenazas afectan una solución cloud? | Phishing, ransomware, DDoS, malware, cryptomining, misconfiguración y ataques LLM | V0/V3/V5: threat scenarios |
| CDL-22 | ¿Cuál es la diferencia entre autenticación, autorización y auditoría? | Identidad, permisos y trazabilidad | V1/V4/V5: IAM y audit trail |
| CDL-23 | ¿Qué significa least privilege y zero trust? | Acceso mínimo, verificación continua y ausencia de confianza implícita | V1/V4: roles y tenants |
| CDL-24 | ¿Cómo protege el cifrado los datos en reposo, tránsito y uso? | Objetivo de cada estado y manejo de llaves | V1/V4: Secret Manager, KMS y datos |
| CDL-25 | ¿Qué es la responsabilidad compartida? | Qué protege Google y qué debe proteger el cliente | V0/V4: límites de seguridad |

### CDL-06 — Scaling with Cloud Operations

| ID | Pregunta representativa | Debo poder explicar | Evidencia CareOps |
|---|---|---|---|
| CDL-26 | ¿Qué cambia de CapEx a OpEx al ir a cloud? | TCO, elasticidad, consumo y gobierno financiero | V0/V4: caso de costo |
| CDL-27 | ¿Qué es la jerarquía organization/folder/project/resource? | Herencia, acceso, visibilidad, auditoría y políticas | V1/V4: landing zone |
| CDL-28 | ¿Cómo se controla el consumo cloud? | Presupuestos, cuotas, alertas, reportes, Spot VMs y apagado | V1/V4: FinOps |
| CDL-29 | ¿Qué son Monitoring, Logging, Trace y Profiler? | Métricas, eventos, trazas, rendimiento y diagnóstico | V3: observabilidad |
| CDL-30 | ¿Qué significan SLI, SLO, SLA, alta disponibilidad y resiliencia? | Medición, objetivo, compromiso, redundancia, backups y recuperación | V3/V4: SLO y DR |

## 3. Tabla cruzada CDL → CareOps V0–V5

| Competencia CDL | V0 Business case | V1 Serverless MVP | V2 Event-driven | V3 Observability | V4 PCA redesign | V5 Agentic |
|---|---|---|---|---|---|---|
| Valor cloud | Problema manual, impacto y KPI | Justifica Cloud Run | Justifica automatización | Mide mejora | Justifica evolución | Justifica asistencia segura |
| Arquitecturas y modelos | Selección conceptual | Cloud Run y Cloud SQL | Pub/Sub/Eventarc | Dependencias | Cloud Run vs GKE, regional/HA | Runtime de agentes |
| Datos | Entidades y calidad | Modelo operacional | Eventos y alertas | Métricas históricas | BigQuery, Storage, SQL/NoSQL | RAG, grounding y evidencia |
| IA | Alcance y límites | Se evita IA prematura | Regla determinística | Señales de calidad | Selección de plataforma | ADK, MCP, Nemotron/NIM |
| Modernización | Proceso actual | MVP serverless | Desacoplamiento por eventos | Operación | Rediseño y migración | Agentic workflow |
| Seguridad | Datos excluidos y consentimiento | IAM y secretos | Seguridad de eventos | Auditoría y redacción | Tenants, KMS, WIF, DR | Tool security y aprobación |
| Operaciones | KPI y costo esperado | Billing y cleanup | Backlog y retries | SLI/SLO/logs/traces | FinOps, HA, DR | Costo por interacción y fallback |
| Producto | Caso B2B2C | Registro de visita | Alerta operativa | Dashboard | Plataforma escalable | Coordinación asistida |

## 4. Orden de dominio recomendado

1. CDL-01 a CDL-05: explicar el problema y la tecnología sin entrar todavía en comandos.
2. CDL-06 a CDL-10: elegir datos y servicios por patrón de uso.
3. CDL-11 a CDL-15: justificar IA y sus límites.
4. CDL-16 a CDL-20: conectar modernización con CareOps V1.
5. CDL-21 a CDL-25: explicar controles y responsabilidad.
6. CDL-26 a CDL-30: defender costo, operación y resiliencia.

## 5. Criterio de preparación

Antes de presentar CDL debo poder responder las 30 preguntas sin memorizar definiciones aisladas y, para cada respuesta, dar un ejemplo de CareOps.

Meta práctica:

- 30/30 respuestas claras;
- 6 decisiones de servicio correctamente justificadas;
- 6 riesgos de seguridad identificados;
- 5 trade-offs de arquitectura explicados;
- pitch de CareOps de 5 minutos;
- al menos 80% en preguntas de práctica;
- ninguna confusión entre AI, ML, gen AI, analytics y BI.

La certificación CDL evalúa comprensión amplia de conceptos, productos, beneficios y casos de uso; no exige construir toda la plataforma ni operar GKE o GPUs. El proyecto CareOps se utiliza como contexto para demostrar comprensión y preparar la transición a ACE y PCA.

