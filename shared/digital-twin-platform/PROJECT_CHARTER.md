# CareOps Cloud: Digital Twin B2E + B2B + B2C

**Estado:** SELECTED-PROJECT  
**Tipo:** proyecto transversal aplicado  
**Ubicación arquitectónica:** shared/digital-twin-platform/  
**Stack estratégico:** Google Cloud + Google ADK + NVIDIA Nemotron/NIM  
**Versión:** 0.2.0

**Tesis del producto:** plataforma B2B2C de coordinación y alertas para el cuidado de adultos mayores. Los cuidadores o familiares registran visitas y eventos; Google Cloud procesa los eventos, genera alertas operativas, conserva trazabilidad y produce analítica. La IA ayuda a coordinar, priorizar y resumir, pero no diagnostica.

## 1. Visión

Construir CareOps Cloud como un digital twin operativo y evolutivo que represente adultos mayores, cuidadores, familiares, coordinadores, proveedores, visitas, alertas, políticas, eventos y relaciones del ecosistema de cuidado. El twin servirá como una capa común de conocimiento, simulación y decisión para tres experiencias:

- B2E — Business to Employee: copilotos para empleados, operaciones, aprendizaje y productividad.
- B2B — Business to Business: colaboración con clientes empresariales, proveedores, partners y cuentas.
- B2C — Business to Consumer: experiencias personalizadas, soporte, recomendaciones y autoservicio.

No será únicamente un chatbot. Será una plataforma con estado, identidad, eventos, memoria, simulación, evidencia y controles de autorización.

## 2. Objetivo de negocio

Permitir que una organización de cuidados entienda el estado de sus operaciones, detecte retrasos e incidencias, simule escenarios, coordine agentes y personas y convierta decisiones en acciones auditables, sin convertir el sistema en una herramienta de diagnóstico médico.

## 3. Principios de diseño

1. Un twin, múltiples vistas: B2E, B2B y B2C consultan el mismo modelo gobernado, pero no comparten datos sin autorización.
2. Event-driven: el estado se actualiza por eventos trazables, no por documentos aislados.
3. Human-in-the-loop: decisiones sensibles requieren aprobación humana.
4. Evidence-first: cada recomendación debe explicar datos, reglas, modelo y herramientas.
5. Model-agnostic: ADK no queda acoplado a un único modelo; Nemotron se integra mediante una interfaz sustituible.
6. Cloud-native y GPU-aware: GCP administra datos, seguridad y operación; NVIDIA aporta aceleración GPU, NIM y modelos Nemotron.
7. Least privilege: cada actor, agente y herramienta opera con permisos mínimos.
8. FinOps by design: todo recurso tiene dueño, propósito, expiración y costo observable.
9. Reversible decisions: simulación y aprobación antes de acciones con impacto financiero, laboral, legal o de cliente.

## 4. Arquitectura lógica

~~~text
B2E apps       B2B portal/API       B2C web/mobile
    \                |                  /
     \--------------- API / Identity --/
                      |
                 Apigee / API Gateway
                      |
             ADK Twin Orchestrator
       /          |           |          \
  Employee     B2B Agent   B2C Agent   Simulation Agent
       \          |           |          /
        -------- Tool / Policy Layer ----
          MCP tools, APIs, approvals, audit
                      |
       Agent Runtime / Cloud Run / GKE
                      |
        Model Gateway / Inference Adapter
                      |
       NVIDIA NIM + Nemotron on GKE GPU
                      |
       BigQuery / Spanner or AlloyDB / GCS
                      |
 Pub/Sub → Dataflow → normalized twin events
                      |
 HR / ERP / CRM / commerce / IoT / partner systems
~~~

## 5. Responsabilidad tecnológica

### Google ADK

ADK será la capa de agentes y orquestación: agentes especializados y multiagente, workflows predecibles, routing dinámico, herramientas MCP y APIs, evaluación de trayectorias, sesiones, memoria y despliegue local, en Cloud Run, GKE o Agent Runtime.

Referencia oficial: https://docs.cloud.google.com/gemini-enterprise-agent-platform/build/adk?hl=en

### NVIDIA Nemotron y NIM

Nemotron será la capa de inferencia especializada y privada para razonamiento, planificación, comprensión documental, clasificación, ranking y generación. NIM será la interfaz operativa para servir el modelo en GPUs NVIDIA.

La selección exacta de modelo no queda fijada en este contrato. Se elegirá después de medir calidad, latencia, costo, memoria, seguridad, licencia y capacidad de tool calling.

Referencia oficial: https://www.nvidia.com/en-us/ai-data-science/foundation-models/nemotron/

### Google Cloud

- Pub/Sub: eventos del ecosistema.
- Dataflow: ingestión, normalización y enriquecimiento.
- BigQuery: analítica, métricas, histórico y datasets.
- Cloud Storage: documentos, objetos y evidencias.
- Spanner o AlloyDB: estado operacional, entidades y relaciones.
- Cloud Run: APIs, workers y agentes de bajo costo.
- GKE: servicios stateful y NIM con GPU.
- Apigee/API Gateway: exposición gobernada para B2B y B2C.
- IAM, Secret Manager, KMS y VPC Service Controls: identidad y protección.
- Monitoring, Logging y Trace: observabilidad.
- Terraform: infraestructura reproducible.

## 6. Modelo conceptual del twin

Entidades iniciales de CareOps:

Person, OlderAdult, Caregiver, FamilyMember, Coordinator, Organization, Provider, Visit, CarePlan, Alert, Location, Process, Interaction, Event, Policy, Risk, Scenario, Decision y Evidence.

Cada entidad debe tener identificador estable, origen, propietario, clasificación de datos, timestamp de vigencia, versión, confianza, permisos, lineage y estado actual/histórico cuando aplique.

## 7. Agentes iniciales

- Twin Orchestrator: coordina intención, contexto, agentes y políticas.
- B2E Care Coordinator Copilot: políticas, turnos, priorización, seguimiento y soporte operativo.
- B2B Account and Operations Agent: cuentas, contratos, SLA, partners y forecast.
- B2C Experience Agent: soporte, recomendaciones y autoservicio con consentimiento.
- Simulation and What-if Agent: precios, capacidad, interrupciones, demanda y migraciones.
- Governance and Evidence Agent: permisos, datos sensibles, políticas y auditoría.

## 8. Límites de autonomía

| Nivel | Acción | Requisito |
|---|---|---|
| L0 | Leer y resumir | Automático |
| L1 | Recomendar | Fuentes, confianza y alternativas |
| L2 | Preparar cambio | Revisión humana |
| L3 | Ejecutar cambio reversible | Aprobación y rollback |
| L4 | Ejecutar cambio sensible | Aprobación explícita y doble control |
| L5 | Cambio irreversible o legal/financiero | No autónomo en MVP |

Nunca se permite modificar nómina, crédito, contratos, precios críticos, derechos de empleados, datos personales sensibles o infraestructura productiva sin política, aprobación y auditoría.

## 9. MVP

### MVP-1: CareOps twin foundation

Modelo de entidades de cuidado, datos sintéticos, Pub/Sub, Dataflow, BigQuery, documentos, API, lineage y dashboard.

### MVP-2: ADK control plane

Twin Orchestrator, Employee Copilot, MCP tools, sesiones, memoria, evaluación y despliegue inicial en Cloud Run.

### MVP-3: NVIDIA inference plane

Interfaz de modelo, Nemotron seleccionado mediante NIM, GKE con GPU durante pruebas, benchmark de calidad/latencia/costo y fallback controlado.

### MVP-4: B2B y B2C

API multi-tenant, portal B2B, experiencia B2C, consentimiento, aislamiento por tenant, cuotas y observabilidad.

### MVP-5: Simulation and production readiness

What-if, aprobaciones, rollback, SLO, incident response, DR, seguridad, evaluación de sesgo, fuga de datos y prompt injection.

## 10. Métricas de éxito

- Producto: usuarios activos, sesiones resueltas, tiempo hasta respuesta útil, adopción y satisfacción.
- Agentes: task success rate, groundedness, tool-call accuracy, hallucination rate, escalamiento humano, costo y p95.
- Plataforma: disponibilidad, freshness del twin, propagación de eventos, costo por tenant, utilización GPU y recuperación.
- Negocio: tiempo operativo, incidentes, conversión, retención, costo de atención y cumplimiento de SLA.

## 11. Fases

1. Descubrimiento y gobierno.
2. Twin mínimo.
3. Agentes internos B2E.
4. Inferencia NVIDIA.
5. B2B controlado.
6. B2C controlado.
7. Simulación.
8. Industrialización.

## 12. Riesgos

- Acoplamiento a un modelo: usar adapter y fallback.
- Costo GPU: usar ventanas de prueba y no dejar GKE GPU permanente.
- Mezcla de tenants: autorización, clasificación y pruebas negativas.
- Alucinaciones: grounding, herramientas verificables, evaluación y evidencia.
- Autonomía excesiva: niveles de autonomía y human-in-the-loop.
- Licenciamiento: revisar el acuerdo del Nemotron y NIM seleccionado antes de uso comercial.
- Twin desactualizado: freshness SLO, timestamps, lineage e incertidumbre.
- Complejidad prematura: iniciar con el journey de visita retrasada y un segmento controlado.

## 13. Relación con la arquitectura del repositorio

Este proyecto es transversal, no una cuarta certificación:

- CDL: valor de negocio, datos, IA, confianza y operaciones.
- ACE: APIs, Pub/Sub, Dataflow, Cloud Run, GKE, IAM, Terraform y monitoring.
- PCA: arquitectura, multi-tenancy, seguridad, resiliencia, costos y trade-offs.
- Professional Agentic Architect: especialización posterior para agentes, NIM, MCP, A2A y autonomía.

Ubicación:

~~~text
shared/
└── digital-twin-platform/
    ├── PROJECT_CHARTER.md
    ├── architecture/
    ├── data-model/
    ├── agents/
    ├── infrastructure/
    ├── applications/
    ├── evaluation/
    ├── security/
    └── evidence/
~~~
