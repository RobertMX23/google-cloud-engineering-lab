# Plan diario de ejecución: CDL → ACE → PCA

**Versión:** \`1.0.0\`  
**Inicio recomendado:** Semana 1  
**Duración total:** 42 semanas  
**Carga estimada:** 679 horas  
**Días de estudio:** 6 por semana  
**Día de descanso:** domingo, salvo simulacros o examen

Este plan convierte el contrato \`RAC-001\` y el registro [\`RESOURCE_REGISTRY_v0.1.yaml\`](RESOURCE_REGISTRY_v0.1.yaml) en una secuencia diaria ejecutable. La ruta \`CDL → ACE → PCA\` es una progresión pedagógica del repositorio; no es un requisito oficial de Google.

## 1. Recursos disponibles y función

| Recurso | Uso principal | Regla operativa |
|---|---|---|
| Google Skills | Cursos, quests, skill badges y laboratorios guiados | Ejecutar primero los recursos P0 del registro |
| GCP Pay Per Use | Validar despliegues reales, operación, IAM, networking y arquitectura | Crear presupuesto, alertas y borrar recursos al terminar cada sesión |
| Laptop workstation | gcloud, Terraform, Docker, Git, documentación, notebooks, diagramas y pruebas locales | Preparar y validar localmente antes de consumir GCP |
| Repositorio | Notas, código, evidencia, decisiones y estado de ejecución | Registrar cada lab con objetivo, costo, validación y limpieza |

## 2. Jornada semanal estándar

### CDL — 10.5 horas por semana

- Lunes a viernes: \`1.5 h/día\` — teoría, guía de examen y Google Skills.
- Sábado: \`3 h\` — laboratorio corto, resumen y preguntas de práctica.
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
| 1 | Transformación digital | 7.5 h de guía y Google Skills | 3 h de mapa de conceptos | Resumen de cloud, modelos, valor y diferenciadores |
| 2 | Datos | 7.5 h de BigQuery, Looker y datos | 3 h de BigQuery con Python | Notebook o captura de consulta y explicación de valor |
| 3 | IA | 7.5 h de IA, Gemini y agentic AI | 3 h de un notebook Gemini | Comparación de IA generativa, agentes, RAG y usos |
| 4 | Modernización | 7.5 h de compute, contenedores y serverless | 3 h de arquitectura de modernización | Matriz IaaS/PaaS/CaaS/serverless |
| 5 | Confianza y seguridad | 7.5 h de IAM, seguridad, privacidad y cumplimiento | 3 h de caso de responsabilidad compartida | Decisión de seguridad para un caso empresarial |
| 6 | Operaciones y examen | 7.5 h de repaso y preguntas | 3 h de simulacro y brechas | Checklist de preparación y decisión de examen |

**Salida de fase:** completar el Learning Path CDL, revisar las seis áreas, resolver preguntas de práctica y programar el examen cuando el simulacro sea consistente.

## 4. Fase 2 — Associate Cloud Engineer

**Duración:** semanas 7–22  
**Carga:** 256 horas  
**Objetivo:** desplegar, operar y proteger soluciones reales, acumulando experiencia práctica con GCP Pay Per Use.

| Semana | Tema | Trabajo principal | Evidencia mínima |
|---:|---|---|---|
| 7 | Entorno cloud | Organización conceptual, proyectos, APIs, regiones y billing | Checklist de proyecto, APIs, cuotas y presupuesto |
| 8 | IAM y cuentas | Roles, políticas, service accounts y Workforce Identity | Matriz de permisos y prueba de mínimo privilegio |
| 9 | Compute Engine | VM, discos, imágenes, snapshots y grupos administrados | Lab reproducible y limpieza verificada |
| 10 | Cloud Run | Imagen, despliegue, revisiones, variables y autenticación | Servicio desplegado y rollback documentado |
| 11 | GKE fundamentos | Cluster, nodes, workloads, Service y Artifact Registry | Aplicación desplegada en GKE |
| 12 | GKE operación | Réplicas, rollout, subnet, DNS, NAT y escalamiento | Cambio sin downtime y evidencia de operación |
| 13 | Storage y bases de datos | Cloud Storage, Cloud SQL, BigQuery y elección de producto | Matriz de decisión y consultas ejecutadas |
| 14 | Networking | VPC, subnets, firewall, balanceo, rutas y conectividad | Diagrama de red y prueba de conectividad |
| 15 | IaC | Terraform, variables, módulos, state y plan/apply | Infraestructura reproducible desde workstation |
| 16 | Cloud Run + Cloud SQL | Proyecto full-stack completo | Aplicación, base de datos, secretos y cleanup |
| 17 | Monitoring | Métricas, dashboards, alertas, uptime checks y SLO básico | Alerta funcional con prueba controlada |
| 18 | Logging y diagnóstico | Log Router, buckets, Logs Explorer, Ops Agent y auditoría | Investigación documentada de un incidente |
| 19 | Online Boutique | Despliegue del sistema de microservicios | Inventario de servicios y dependencias |
| 20 | GKE outage/SRE | Romper, investigar, reparar y redactar postmortem | Postmortem con causa raíz y acciones |
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
| 40 | Capstone | ADK + Gemini + BigQuery MCP + Cloud Run o solución equivalente | Arquitectura, IaC, demo y evidencia |
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

