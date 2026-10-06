# Contrato de arquitectura y distribución del repositorio

**Identificador:** `RAC-001`  
**Estado:** `ACTIVE`  
**Alcance:** todo el repositorio `RobertMX23/google-cloud-engineering-lab`  
**Versión:** `1.0.0`

El registro normativo de recursos y vínculos es [`RESOURCE_REGISTRY_v0.1.yaml`](RESOURCE_REGISTRY_v0.1.yaml).

## 1. Propósito

Este documento es la fuente de verdad para la arquitectura, distribución y clasificación de los recursos del repositorio. Toda incorporación, reorganización o automatización debe respetar este contrato.

## 2. Arquitectura principal

El repositorio sigue una progresión pedagógica de tres niveles:

```text
01 Cloud Digital Leader
        ↓ fundamentos y negocio
02 Associate Cloud Engineer
        ↓ implementación y operación
03 Professional Cloud Architect
        ↓ arquitectura y decisiones
```

La clasificación primaria de un recurso es:

```text
Certificación → Área del examen → Producto o capability → Lab → Evidence
```

Los productos nunca sustituyen a la certificación ni al área del examen como nivel principal de organización.

## 3. Distribución autorizada

### 3.1 Cloud Digital Leader

Ruta: `01-cloud-digital-leader/`

- `01-digital-transformation/`
- `02-data-transformation/`
- `03-artificial-intelligence/`
- `04-modernize-infrastructure-applications/`
- `05-trust-security/`
- `06-scaling-cloud-operations/`

Uso: fundamentos conceptuales, capacidades de Google Cloud, casos de negocio y transformación empresarial.

### 3.2 Associate Cloud Engineer

Ruta: `02-associate-cloud-engineer/`

- `01-setting-up-cloud-solution-environment/`
- `02-planning-implementing-cloud-solution/`
  - `compute/`
    - `cloud-run/`
    - `compute-engine/`
    - `gke/`
    - `agent-runtime/`
  - `storage-and-data/`
    - `cloud-storage/`
    - `cloud-sql/`
    - `bigquery/`
  - `networking/`
  - `tooling/`
    - `terraform/`
    - `gemini-cli/`
    - `antigravity/`
- `03-ensuring-successful-operation/`
  - `compute/`
  - `storage-and-data/`
  - `networking/`
  - `monitoring-and-logging/`
- `04-configuring-access-security/`
  - `iam/`
  - `service-accounts/`

Uso: configuración, despliegue, operación, observabilidad y seguridad de soluciones.

### 3.3 Professional Cloud Architect

Ruta: `03-professional-cloud-architect/`

- `01-designing-planning-architecture/`
- `02-managing-provisioning-infrastructure/`
  - `01-network-topologies/`
  - `02-storage-systems/`
  - `03-compute-systems/`
  - `04-agent-platform-ml-workflows/`
  - `05-agent-platform-apis-prebuilt-solutions/`
- `03-security-compliance/`
- `04-technical-business-processes/`
- `05-managing-implementation/`
- `06-solution-operations-excellence/`

Uso: diseño, trade-offs, seguridad, cumplimiento, implementación y excelencia operativa.

### 3.4 Recursos compartidos

Ruta: `shared/`

- `codelabs/`
- `colab/`
- `github-reference-projects/`
- `google-skills/`
- `coursera/`
- `architecture-patterns/`
- `evidence/`

Solo se permite colocar aquí material transversal o referencias comunes a más de una certificación. Un recurso específico debe permanecer en su clasificación primaria.

## 4. Reglas de clasificación

1. Todo recurso debe tener una clasificación primaria única.
2. Un lab se ubica dentro del área del examen que evalúa principalmente.
3. Si un recurso cubre varias áreas, se coloca donde tenga su objetivo principal y se documentan las referencias cruzadas en su README.
4. Las fuentes externas no se duplican innecesariamente; se registra su origen y URL.
5. Cada lab debe incluir objetivo, prerrequisitos, pasos, validación, evidencia, costos y limpieza.
6. No crear una carpeta raíz genérica `labs/` desconectada de la taxonomía.

## 5. PDFs y documentos de certificación

Las guías de examen se colocan en la raíz de su certificación:

- CDL: `01-cloud-digital-leader/`
- ACE: `02-associate-cloud-engineer/`
- PCA: `03-professional-cloud-architect/`

Los documentos que no correspondan a estas tres certificaciones no se mueven automáticamente. Deben conservarse en su ubicación actual hasta que exista una decisión explícita y una sección aprobada para ellos.

Actualmente quedan fuera de la progresión principal:

- Generative AI Leader
- Professional Agentic Architect

## 6. Contrato operativo para cambios

Antes de cualquier cambio estructural se debe:

1. inspeccionar el estado local;
2. comparar el commit local con `origin/main`;
3. aplicar el cambio sin mover recursos fuera de alcance;
4. verificar la estructura resultante;
5. crear un commit descriptivo;
6. publicar en `main` cuando el cambio esté autorizado;
7. comparar nuevamente los hashes local y remoto;
8. reportar cualquier archivo local no versionado.

No se considera completado un cambio publicado hasta que el hash local y el remoto coincidan.

## 7. Evolución del contrato

Los cambios a la arquitectura requieren actualizar este documento, el README del área afectada y, cuando aplique, `AGENTS.md`. Las nuevas certificaciones deben incorporarse como una decisión explícita; no deben mezclarse silenciosamente en CDL, ACE o PCA.

## 8. Registro de vínculos y recursos

`RESOURCE_REGISTRY_v0.1.yaml` es el registro canónico de los vínculos de aprendizaje, documentación, codelabs, repositorios, notebooks y programas formativos asociados al proyecto.

Cada registro debe contener como mínimo:

- `certification` — `CDL`, `ACE` o `PCA`;
- `exam_section` — área primaria del blueprint;
- `priority` — `P0`, `P1` o `P2`;
- `resource_type` — tipo de recurso;
- `name` y `url` — identidad y vínculo externo;
- `repo_path` — ubicación prevista en el repositorio;
- `resource_status` — vigencia o necesidad de revisión;
- `execution_status` — avance práctico del recurso.

La prioridad se interpreta así:

- `P0`: recurso canónico y de ejecución prioritaria;
- `P1`: recurso importante de apoyo o profundización;
- `P2`: recurso complementario, opcional o de terceros.

El registro distingue entre el estado del vínculo (`resource_status`) y el avance de estudio o ejecución (`execution_status`). No se debe marcar un recurso como completado solo por haber guardado su URL.

Antes de incorporar o descargar un recurso se debe verificar su URL, título, propietario y señales de vigencia. Si el vínculo no puede verificarse, debe marcarse como `LINK_REVIEW_REQUIRED` y no se debe inventar una URL alternativa.

## 9. Plan de ejecución

El plan operativo de estudio y práctica está definido en [`STUDY_EXECUTION_PLAN.md`](STUDY_EXECUTION_PLAN.md). Ese documento convierte la matriz de recursos en una secuencia de 42 semanas con carga diaria, objetivos semanales, evidencias y controles de costo para Google Skills, GCP Pay Per Use y workstation local.

El plan no cambia la clasificación del repositorio: solo define cuándo y cómo se ejecuta cada recurso. Los estados de avance deben mantenerse en sincronía con `RESOURCE_REGISTRY_v0.1.yaml`.

## 10. Proyecto transversal Digital Twin

El proyecto integral B2E + B2B + B2C está definido en [`shared/digital-twin-platform/PROJECT_CHARTER.md`](shared/digital-twin-platform/PROJECT_CHARTER.md). Es un proyecto aplicado transversal, no una cuarta certificación.

Su arquitectura combina:

- Google ADK para agentes, herramientas, workflows, evaluación y orquestación;
- NVIDIA Nemotron/NIM para inferencia acelerada y modelos especializados;
- Google Cloud para datos, eventos, APIs, seguridad, observabilidad y operación;
- GCP GPU/GKE únicamente cuando el benchmark justifique el costo y la capacidad requerida.

El charter debe mantenerse alineado con este contrato, el registro de recursos y el plan de ejecución. La selección exacta del modelo Nemotron queda abierta hasta completar benchmark de calidad, latencia, costo, memoria, seguridad y licencia.
