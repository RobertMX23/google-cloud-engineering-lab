# Plan diario de estudio y trabajo: CareOps Cloud + CDL → ACE → PCA

**Versión:** \`1.2.0\`
**Inicio recomendado:** Semana 1  
**Duración total:** 42 semanas  
**Carga estimada:** 679 horas  
**Días de estudio:** 6 por semana  
**Día de descanso:** domingo, salvo simulacros o examen

Este plan convierte el contrato \`RAC-001\`, el registro [\`RESOURCE_REGISTRY_v0.1.yaml\`](RESOURCE_REGISTRY_v0.1.yaml) y el charter de [CareOps Cloud](shared/digital-twin-platform/PROJECT_CHARTER.md) en una secuencia diaria ejecutable. La ruta \`CDL → ACE → PCA\` es una progresión pedagógica del repositorio; no es un requisito oficial de Google.

CareOps Cloud será el proyecto transversal principal. Online Boutique, \`microservices-demo\`, Cloud Run Samples, Cloud Foundation Fabric y los codelabs se utilizarán como referencias técnicas, no como el producto principal.

## 1. Recursos disponibles y función

| Recurso | Uso principal | Regla operativa |
|---|---|---|
| Google Skills | Cursos, quests, skill badges y laboratorios guiados | Ejecutar primero los recursos P0 del registro |
| GCP Pay Per Use | Validar despliegues reales, operación, IAM, networking y arquitectura | Crear presupuesto, alertas y borrar recursos al terminar cada sesión |
| Laptop workstation | gcloud, Terraform, Docker, Git, documentación, notebooks, diagramas y pruebas locales | Preparar y validar localmente antes de consumir GCP |
| Repositorio | Notas, código, evidencia, decisiones y estado de ejecución | Registrar cada lab con objetivo, costo, validación y limpieza |
| CareOps Cloud | Hilo conductor de negocio, implementación y arquitectura | Cada fase debe producir una demo, decisión o evidencia reutilizable |
| Banco CDL 2026 | 96 preguntas, taxonomía y sesiones aleatorias | Usar `01-cloud-digital-leader/CDL_QUESTION_BANK_2026.yaml`; no revelar respuestas antes del intento |

## 2. Jornada semanal estándar

### CDL — 10.5 horas por semana

- Lunes a jueves: \`1.5 h/día\` — teoría, guía de examen y Google Skills.
- Viernes: \`1.5 h\` — preguntas por dominio, revisión de errores y tarjetas de conceptos.
- Sábado: \`3 h\` — laboratorio corto, simulacro o sesión de preguntas calificadas.
- Domingo: descanso.

### ACE — 16 horas por semana

- Lunes a viernes: \`2 h/día\` — curso, consola, CLI y documentación.
- Sábado: \`6 h\` — laboratorio completo, troubleshooting y evidencia.
- Domingo: descanso.

### PCA — 18 horas por semana

- Lunes a viernes: \`2.5 h/día\` — arquitectura, casos, trade-offs y lectura técnica.
- Sábado: \`5.5 h\` — diseño, Terraform, capstone o simulacro.
- Domingo: descanso.

## 3. Fase 1 — Cloud Digital Leader

**Duración:** semanas 1–6  
**Carga:** 63 horas  
**Objetivo:** comprender las seis áreas del blueprint y explicar el valor de Google Cloud en términos técnicos y de negocio.

| Semana | Tema | Lunes–viernes | Sábado | Evidencia mínima |
|---:|---|---|---|---|
| 1 | CareOps business case | 6 h de guía y Google Skills + 1.5 h CDL-001–016 | 3 h: sesión de 10 preguntas | Caso B2B2C, problema, KPIs, riesgos y alcance V0 |
| 2 | Datos del cuidado | 6 h de BigQuery, Looker y datos + 1.5 h CDL-017–032 | 3 h: sesión de 10 preguntas | Modelo de caregiver, adulto mayor, visita, evento y alerta |
| 3 | IA responsable y agentes | 6 h de IA, Gemini y agentic AI + 1.5 h CDL-033–048 | 3 h: sesión de IA de 12 preguntas | Límites: coordinación, no diagnóstico; riesgos y consentimiento |
| 4 | Modernización | 6 h de compute, contenedores y serverless + 1.5 h CDL-049–064 | 3 h: sesión de 10 preguntas | Matriz IaaS/PaaS/CaaS/serverless |
| 5 | Confianza y seguridad | 6 h de IAM, seguridad, privacidad y cumplimiento + 1.5 h CDL-065–080 | 3 h: sesión de seguridad de 12 preguntas | Decisión de seguridad para un caso empresarial |
| 6 | Operaciones y examen | 6 h de repaso y preguntas + 1.5 h CDL-081–096 | 3 h: simulacro de 50–60 preguntas y análisis | Checklist CDL + pitch de CareOps de 5 minutos |

**Salida de fase:** completar el Learning Path CDL, revisar las seis áreas, resolver preguntas de práctica y programar el examen cuando el simulacro sea consistente.

### Protocolo de práctica CDL

Cada sesión debe sortear preguntas del banco canónico respetando la taxonomía definida en `CDL_QUESTION_TAXONOMY_2026.md`.

| Sesión | Cuándo | Tamaño | Resultado mínimo |
|---|---|---:|---:|
| Diagnóstico | Inicio de semana 1 | 10 | Registrar línea base, sin criterio de aprobación |
| Dominio | Viernes de cada semana | 10–16 | 80% por dominio antes de cerrar la semana |
| IA y agentes | Semana 3 y repaso final | 12 | 80% y explicación de riesgos, tools y aprobación humana |
| Completa | Sábado de semana 6 | 50–60 | 80% global y ningún dominio por debajo de 70% |
| Recuperación | Cuando un dominio falle | 10 | Repetir solo errores y conceptos relacionados |

Para cada intento se registra fecha, tamaño, IDs sorteados, aciertos, porcentaje, dominios débiles y siguiente acción. El resultado no se considera evidencia de aprobación oficial; es un control interno de preparación.

## 4. Fase 2 — Associate Cloud Engineer

**Duración:** semanas 7–22  
**Carga:** 256 horas  
**Objetivo:** desplegar, operar y proteger soluciones reales, acumulando experiencia práctica con GCP Pay Per Use.

| Semana | Tema | Trabajo principal | Evidencia mínima |
|---:|---|---|---|
| 7 | Entorno cloud | Organización conceptual, proyectos, APIs, regiones y billing | Checklist de proyecto, APIs, cuotas y presupuesto |
| 8 | IAM y cuentas | Roles, políticas, service accounts y Workforce Identity | Matriz de permisos y prueba de mínimo privilegio |
| 9 | Compute Engine | VM, discos, imágenes, snapshots y grupos administrados | Lab reproducible y limpieza verificada |
| 10 | CareOps V1 serverless | Cloud Run, API, autenticación y registro de visitas | Visit ID, caregiver, horario, llegada y estado |
| 11 | Referencia GKE | Cluster, nodes, workloads, Service y Artifact Registry | Comparación Cloud Run vs GKE; GKE no es aún el runtime principal |
| 12 | GKE operación | Réplicas, rollout, subnet, DNS, NAT y escalamiento | Cambio sin downtime y evidencia de operación |
| 13 | Storage y bases de datos | Cloud Storage, Cloud SQL, BigQuery y elección de producto | Matriz de decisión y consultas ejecutadas |
| 14 | Networking | VPC, subnets, firewall, balanceo, rutas y conectividad | Diagrama de red y prueba de conectividad |
| 15 | IaC | Terraform, variables, módulos, state y plan/apply | Infraestructura reproducible desde workstation |
| 16 | CareOps V1 completo | Cloud Run + Cloud SQL + Secret Manager | Registro de visitas, roles, alertas básicas y cleanup |
| 17 | Monitoring | Métricas, dashboards, alertas, uptime checks y SLO básico | Alerta funcional con prueba controlada |
| 18 | Logging y diagnóstico | Log Router, buckets, Logs Explorer, Ops Agent y auditoría | Investigación documentada de un incidente |
| 19 | CareOps V2 event-driven | Pub/Sub, Eventarc, reglas de retraso y notificaciones | Evento visit.registered → ALERT_CREATED |
| 20 | Failure engineering | Usar Online Boutique/GKE outage como referencia; inyectar fallos en CareOps | Postmortem de backlog, timeout, IAM o Cloud SQL |
| 21 | Repaso ACE | Repetir laboratorios débiles y preguntas por dominio | Matriz de brechas y segunda ejecución |
| 22 | Readiness y examen | Simulacros, revisión de comandos y examen | Checklist ACE y evidencia de preparación |

**Regla de experiencia:** Google recomienda seis meses o más de experiencia práctica con Google Cloud antes del ACE. Este plan crea práctica intensiva, pero no sustituye experiencia laboral sostenida; si el resultado de los labs todavía es frágil, extender las semanas 17–21 antes de presentar el examen. [Recomendación oficial para ACE](https://cloud.google.com/learn/certification/cloud-engineer)

## 5. Fase 3 — Professional Cloud Architect

**Duración:** semanas 23–42  
**Carga:** 360 horas  
**Objetivo:** diseñar soluciones completas, defender trade-offs y convertir arquitectura en infraestructura y operación verificables.

| Semana | Tema | Trabajo principal | Evidencia mínima |
|---:|---|---|---|
| 23 | Blueprint PCA | Exam guide, dominios, casos y Well-Architected | Mapa de objetivos y brechas |
| 24 | Well-Architected | Excelencia operativa, seguridad, confiabilidad, costo, rendimiento y sostenibilidad | Checklist aplicado a una solución |
| 25 | Requisitos | Requisitos funcionales/no funcionales, KPIs, restricciones y riesgos | Documento de requisitos |
| 26 | Diseño de datos y compute | Selección de productos, rendimiento, disponibilidad y costo | ADR de datos y compute |
| 27 | Integración y migración | APIs, eventos, híbrido, multicloud, dependencias y migración | Diagrama de contexto y plan de migración |
| 28 | Deployment Archetypes | Zonal, regional, multirregional, global, híbrido y multicloud | Matriz de trade-offs |
| 29 | Networking arquitectónico | VPC, Shared VPC, conectividad híbrida, seguridad y topologías | Diseño de red empresarial |
| 30 | Storage arquitectónico | Retención, ciclo de vida, cifrado, latencia y crecimiento | Decisión de almacenamiento |
| 31 | Compute arquitectónico | GCE, GKE, serverless, contenedores y workloads especializados | Decisión de plataforma |
| 32 | Landing zone | Foundation Fabric/FAST, jerarquía, billing, proyectos y guardrails | Diseño de landing zone |
| 33 | Seguridad y compliance | IAM, SoD, KMS, secretos, VPC Service Controls, auditoría y privacidad | Threat model y controles |
| 34 | Terraform Foundation | Bootstrap, módulos, CI/CD, state y separación de funciones | Repositorio IaC reproducible |
| 35 | Procesos técnicos y negocio | SDLC, CI/CD, costos, stakeholders, cambio y operación | RACI, proceso y KPIs |
| 36 | Gestión de implementación | Plan de releases, testing, migración, riesgos y adopción | Plan de implementación |
| 37 | Operations Excellence | SLO, SLI, observabilidad, DR, incidentes y mejora continua | Runbook y plan DR |
| 38 | Agent Platform | Agent Runtime, sesiones, memoria, MCP, A2A y seguridad | Diagrama de plataforma agentic |
| 39 | GenAI y RAG | Grounding, embeddings, Vector Search, evaluación y costo | ADR de RAG/grounding |
| 40 | CareOps V5 capstone | ADK + modelo + BigQuery MCP + Cloud Run/GKE | Agente de coordinación, herramientas, aprobación y evidencia |
| 41 | Casos y simulacros | Casos PCA, decisiones bajo restricciones y defensa oral | 2 simulacros revisados |
| 42 | Readiness y examen | Repaso final, revisión de brechas y examen | Checklist PCA y paquete final |

Google recomienda para PCA más de tres años de experiencia profesional, incluyendo al menos un año diseñando y administrando soluciones en Google Cloud. El plan puede preparar el examen, pero no debe presentarse como sustituto de esa experiencia recomendada. [Recomendación oficial para PCA](https://cloud.google.com/learn/certification/cloud-architect/)

## 6. Uso controlado de GCP Pay Per Use

Antes de iniciar la semana 7:

1. Crear un proyecto de laboratorio separado de cualquier entorno productivo.
2. Configurar billing budget y alertas al 50%, 80% y 100% del límite mensual elegido.
3. Activar solo las APIs de la sesión.
4. Usar workstation para lint, \`terraform validate\`, \`terraform plan\`, Docker y pruebas locales antes de \`apply\`.
5. Etiquetar recursos con \`owner\`, \`phase\`, \`week\` y \`expires_on\`.
6. Destruir recursos temporales al final de cada sesión.
7. Mantener GKE, Cloud SQL, balanceadores y cualquier GPU/TPU solo durante ventanas de laboratorio planificadas.
8. No usar GPUs/TPUs ni despliegues multirregión como configuración predeterminada.
9. Registrar costo observado y cleanup en la evidencia de cada lab.

## 7. Rutina diaria de workstation

Cada sesión debe seguir este ciclo:

~~~text
10 min  Revisar objetivo y estado del recurso en RESOURCE_REGISTRY
20 min  Leer blueprint/documentación oficial
60-120 min  Ejecutar curso, lab o diseño
20 min  Validar, capturar evidencia y anotar errores
10 min  Cleanup, actualizar estado y planear la siguiente sesión
~~~

Para sesiones ACE/PCA con GCP, el cleanup no es opcional. Para sesiones CDL, se prioriza comprensión, explicación y decisiones sobre cantidad de código.

## 8. Criterio de terminación por recurso

Un recurso pasa por estos estados:

~~~text
NOT_STARTED → IN_PROGRESS → COMPLETED → EVIDENCE_CAPTURED
~~~

\`COMPLETED\` exige haber ejecutado o estudiado el recurso. \`EVIDENCE_CAPTURED\` exige además un README o registro con:

- objetivo y área del examen;
- fecha y duración;
- recursos GCP creados;
- costo o estimación;
- comandos, configuración o decisiones;
- validación;
- evidencia;
- cleanup;
- lecciones y siguiente acción.

## 9. Revisión semanal y control de ritmo

Cada sábado se debe responder:

1. ¿Qué objetivos del blueprint cubrí?
2. ¿Qué puedo explicar sin consultar notas?
3. ¿Qué pude desplegar y operar realmente?
4. ¿Qué evidencia quedó en el repositorio?
5. ¿Qué recurso debe pasar a \`LINK_REVIEW_REQUIRED\`?
6. ¿Qué debo repetir antes de avanzar?

Si una semana queda por debajo del 80% de sus objetivos, se repite o se extiende; no se acumulan temas nuevos para compensar superficialmente.

## 10. Resumen ejecutivo

| Certificación | Semanas | Horas/semana | Horas totales | Resultado esperado |
|---|---:|---:|---:|---|
| CDL | 6 | 10.5 | 63 | Fundamentos y examen de nivel foundational |
| ACE | 16 | 16 | 256 | Capacidad práctica de desplegar y operar |
| PCA | 20 | 18 | 360 | Diseño, trade-offs y capstone arquitectónico |
| **Total** | **42** | — | **679** | Ruta completa CDL → ACE → PCA |

## 11. Ruta de trabajo CareOps Cloud

Esta es la secuencia de construcción que debe acompañar el estudio. Cada versión tiene que quedar demostrable antes de abrir la siguiente.

| Versión | Semanas | Construcción | Competencia principal |
|---|---:|---|---|
| V0 | 1–6 | Business case, actores, proceso manual, KPIs, datos sintéticos y límites médicos | CDL |
| V1 | 7–16 | Web/API en Cloud Run, Cloud SQL, IAM, Secret Manager y registro de visitas | ACE |
| V2 | 17–20 | Pub/Sub, Eventarc, reglas determinísticas, alertas y notificaciones | ACE |
| V3 | 17–22 | Logging, Monitoring, Trace, métricas custom, dashboards y troubleshooting | ACE |
| V4 | 23–37 | Rediseño PCA: HA, DR, costos, multi-tenant, seguridad, IaC y SLO | PCA |
| V5 | 38–42 | ADK, MCP, agente de coordinación, evaluación, aprobación humana y benchmark | PCA / Agentic |

### MVP funcional de CareOps

El primer flujo debe ser deliberadamente simple y sin IA:

~~~text
Caregiver registra visita
        ↓
Cloud Run API
        ↓
Cloud SQL
        ↓
Pub/Sub / Eventarc
        ↓
Regla: retraso > 30 minutos
        ↓
ALERT_CREATED
        ↓
Notificación al coordinador
~~~

Después se compara:

~~~text
Rules Engine vs Agent vs Hybrid
~~~

Las métricas mínimas son precisión, latencia, costo, explicabilidad, falsos positivos y confiabilidad. El agente solo podrá sugerir o preparar una escalación; la acción sensible requiere aprobación humana.

### Failure engineering

Los escenarios mínimos son:

- Cloud SQL no disponible;
- backlog de Pub/Sub;
- timeout de una herramienta del agente;
- permiso IAM inválido;
- aumento de latencia en Cloud Run;
- cuota de BigQuery;
- recomendación agentic incorrecta.

Cada escenario debe seguir el ciclo: inject → detect → observe → diagnose → recover → postmortem.

### Evidencia de portfolio

Cada release de CareOps debe incluir:

- diagrama de arquitectura;
- README ejecutable;
- código o Terraform relevante;
- decisión arquitectónica y trade-offs;
- métricas y costo;
- pruebas y fallos inyectados;
- evidencia de cleanup;
- postmortem cuando aplique;
- relación con objetivos CDL, ACE o PCA.
