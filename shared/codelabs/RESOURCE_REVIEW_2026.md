# Revisión de codelabs y repositorio técnico — 2026

**Fecha de revisión:** 2026-10-06  
**Propósito:** registrar, validar y evaluar los ocho recursos enviados para el proyecto CareOps Cloud y las certificaciones CDL → ACE → PCA.

## Resultado

Los ocho vínculos fueron revisados contra sus páginas públicas. Tres ya estaban registrados en `RESOURCE_REGISTRY_v0.1.yaml`; cuatro recursos de ADK/MCP fueron agregados; el repositorio `microservices-demo` ya estaba registrado.

La revisión de contenido no equivale a ejecución. Todos quedan inicialmente en `execution_status: NOT_STARTED` hasta que se realicen los laboratorios y se capture evidencia.

## Matriz de evaluación

| Recurso | Registro | Qué aporta | Certificación | CareOps | Evaluación |
|---|---|---|---|---|---|
| [Cloud Run + Cloud SQL + Next.js](https://codelabs.developers.google.com/codelabs/deploy-application-with-database/cloud-sql-nextjs?hl=es-419) | Ya existente: `ace-cloud-run-cloud-sql` | Aplicación web, PostgreSQL, identidad de servicio, conexión privada y despliegue | ACE | V1 | Prioridad alta; base del MVP serverless |
| [Investigate GKE outage with Antigravity CLI and SRE](https://codelabs.developers.google.com/codelabs/investigate-gke-cluster-breakage-scenarios-with-postmortem) | Ya existente: `ace-gke-outage-sre`, `pca-gke-outage-sre` | Diagnóstico, postmortem, señales operativas y resiliencia | ACE/PCA | V3/V4 | Prioridad alta; evidencia de operación y SRE |
| [microservices-demo](https://github.com/GoogleCloudPlatform/microservices-demo) | Ya existente: `ace-online-boutique` | Microservicios, Kubernetes, Istio y gRPC | ACE | V1/V4 | Prioridad alta; referencia de arquitectura, no producto final |
| [Building AI Agents with ADK: The Foundation](https://codelabs.developers.google.com/devsite/codelabs/build-agents-with-adk-foundation) | Agregado: `pca-adk-foundation` | Fundamentos de agentes, ADK, instrucciones, herramientas y ejecución | PCA/Agentic | V5 | Prioridad alta; prerrequisito para agentes |
| [Building a Simple Travel Agent with ADK and Gemini CLI](https://codelabs.developers.google.com/codelabs/build-a-simple-travel-agent-with-adk-and-gemini-cli) | Agregado: `pca-adk-travel-agent-gemini-cli` | Agente práctico, Gemini CLI, herramientas y flujo de conversación | PCA/Agentic | V5 | Prioridad media-alta; patrón de referencia, no dominio CareOps |
| [Tools to make an agent with ADK](https://codelabs.developers.google.com/codelabs/cloud-run/tools-make-an-agent?hl=es-419) | Agregado: `pca-adk-tools-agent-cloud-run` | Diseño de tools, integración de capacidades y despliegue en Cloud Run | PCA/Agentic | V5 | Prioridad alta; conecta agente con backend operativo |
| [Use an MCP Server on Cloud Run with an ADK Agent](https://codelabs.developers.google.com/codelabs/cloud-run/use-mcp-server-on-cloud-run-with-an-adk-agent?hl=es) | Agregado: `pca-mcp-server-cloud-run-adk-agent` | Servidor MCP, herramientas remotas, ADK y Cloud Run | PCA/Agentic | V5 | Prioridad crítica; patrón directo para CareOps |
| [ADK + Gemini + BigQuery MCP + Cloud Run](https://codelabs.developers.google.com/codelabs/cloud-run/cloud-run-adk-gemini-bq-mcp?hl=es-419) | Ya existente: `pca-adk-gemini-bigquery-mcp-cloud-run` | Agente con MCP sobre datos analíticos y despliegue Cloud Run | PCA/Agentic | V2/V5 | Prioridad crítica; integración analítica del twin |

## Orden de ejecución recomendado

1. Cloud Run + Cloud SQL.
2. `microservices-demo`.
3. GKE outage y postmortem.
4. ADK Foundation.
5. ADK Tools + Cloud Run.
6. MCP Server + Cloud Run + ADK Agent.
7. ADK + Gemini + BigQuery MCP + Cloud Run.
8. Travel Agent como práctica adicional de agente.

## Criterio de aceptación

Cada recurso pasará de `NOT_STARTED` a `EVIDENCE_CAPTURED` únicamente cuando exista:

- resumen técnico propio;
- comandos o pasos reproducibles;
- diagrama o decisión arquitectónica aplicable;
- evidencia de ejecución, cuando el recurso sea práctico;
- relación explícita con V0–V5;
- nota de costos y limpieza de recursos.

## Riesgos identificados

- Los codelabs pueden cambiar de URL, idioma o nomenclatura.
- Cloud SQL puede generar cargos; el codelab indica limpiar recursos al finalizar.
- Los agentes y MCP no deben recibir permisos amplios por defecto.
- Las prácticas de ADK deben adaptarse a CareOps; no se deben copiar sin validar seguridad, datos y aprobación humana.
