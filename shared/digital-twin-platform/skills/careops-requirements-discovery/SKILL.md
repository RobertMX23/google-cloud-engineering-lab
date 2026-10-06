---
name: careops-requirements-discovery
description: Levanta funciones, requisitos técnicos y especificaciones verificables para las fases V0-V5 de CareOps Cloud, usando entrevistas estructuradas y criterios de salida para transformar respuestas en backlog, contratos, ADRs y criterios de aceptación.
metadata:
  short-description: Levantar funciones y specs de CareOps V0-V5
---

# CareOps Requirements Discovery

Usa este skill cuando se necesite descubrir, aclarar o documentar funciones y especificaciones de CareOps Cloud para cualquiera de sus fases V0, V1, V2, V3, V4 o V5.

## Resultado esperado

Producir, para la fase solicitada:

- alcance incluido y excluido;
- actores, roles y permisos;
- capacidades y funciones;
- flujos principales y excepciones;
- datos, eventos y contratos;
- requisitos no funcionales;
- riesgos y decisiones abiertas;
- criterios de aceptación verificables;
- backlog priorizado;
- evidencia requerida;
- preguntas pendientes con responsable y fecha.

## Fuente de verdad

Usa como contexto mínimo:

- el charter de CareOps Cloud;
- el plan de ejecución;
- RESOURCE_REGISTRY_v0.1.yaml;
- los blueprints de CDL, ACE y PCA;
- la referencia de preguntas en references/question-bank.md.

No inventes integraciones, datos clínicos, obligaciones regulatorias, modelos NVIDIA, límites de costo o SLOs. Marca esos elementos como OPEN_DECISION y formula la pregunta necesaria.

## Método

1. Identifica la fase V y su objetivo de salida.
2. Carga únicamente las preguntas de esa fase en references/question-bank.md.
3. Pregunta primero las preguntas MUST; usa las SHOULD cuando la respuesta cambie arquitectura, costo, seguridad o aceptación.
4. Evita repetir preguntas ya respondidas en artefactos existentes.
5. Convierte cada respuesta en una afirmación verificable:
   - REQ-F-### para requisito funcional;
   - REQ-NF-### para requisito no funcional;
   - DATA-### para entidad o dato;
   - EVENT-### para evento o contrato;
   - SEC-### para control de seguridad;
   - ADR-### para decisión arquitectónica;
   - ACC-### para criterio de aceptación.
6. Señala contradicciones entre respuestas y detén la especificación afectada hasta resolverlas.
7. Separa decisión confirmada, supuesto provisional, pregunta abierta y evidencia pendiente.
8. Cierra la fase solo cuando se cumplan sus criterios de salida y las preguntas MUST estén contestadas o aceptadas como riesgo.

## Reglas técnicas

- El primer flujo de CareOps debe funcionar sin IA: registro de visita, evento, regla de retraso y alerta.
- No conviertas al agente en autoridad médica; el alcance agentic es coordinación, priorización, resumen y preparación de escalación.
- Cada función debe declarar actor, entrada, salida, permisos, errores, auditoría y criterio de aceptación.
- Cada API debe declarar autenticación, autorización, idempotencia, timeouts, retries, errores y observabilidad.
- Cada evento debe declarar productor, consumidor, esquema, versionado, orden, deduplicación, retención y replay.
- Cada dato debe declarar origen, propietario, clasificación, retención, calidad y lineage.
- Cada componente GCP debe declarar propósito, región, costo, escala, backup, cleanup y alternativa.
- Nemotron/NIM debe permanecer detrás de una interfaz de modelo hasta completar benchmark de calidad, latencia, costo, memoria, seguridad y licencia.
- Las acciones L2 o superiores requieren revisión o aprobación humana según el charter.
- No despliegues GKE con GPU, Cloud SQL, balanceadores o recursos costosos para responder preguntas de diseño; primero usa workstation, datos sintéticos y pruebas locales.

## Formato de salida

Entrega un paquete con:

1. Resumen de fase.
2. Decisiones confirmadas.
3. Supuestos y preguntas abiertas.
4. Actores y permisos.
5. Funciones priorizadas.
6. Flujos y estados.
7. Modelo de datos y eventos.
8. APIs y herramientas.
9. Requisitos no funcionales.
10. Seguridad, privacidad y aprobación humana.
11. Observabilidad y FinOps.
12. Criterios de aceptación.
13. ADRs requeridos.
14. Backlog y próximos pasos.

Para cada pregunta registra ID, pregunta, categoría, prioridad, respuesta, impacto si queda abierta, artefacto actualizado, responsable y estado.

## Criterio de finalización

No declares una fase lista solo porque se respondió el cuestionario. Declárala lista únicamente cuando:

- el conteo mínimo de preguntas esté cubierto;
- no existan contradicciones críticas;
- cada función P0 tenga criterio de aceptación;
- los datos y eventos críticos tengan contrato;
- los riesgos de seguridad y costo tengan tratamiento;
- exista una demostración o evidencia prevista;
- el backlog restante tenga dueño y fecha.


