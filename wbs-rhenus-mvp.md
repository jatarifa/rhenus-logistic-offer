# Work Breakdown Structure (WBS) - Rhenus Logistics MVP

## Tabla de Contenidos

1. [Información del Proyecto](#información-del-proyecto)
2. [Objetivos del MVP](#objetivos-del-mvp)
3. [Principios del WBS](#principios-del-wbs)
4. [Estructura del WBS](#estructura-del-wbs)
   - 4.0. [Resumen en Formato Tabla](#resumen-en-formato-tabla)
   - 4.1. [FASE 0: Discovery & Setup](#10-fase-0-discovery--setup)
     - 4.1.1. [Discovery y análisis de procesos actuales](#11-discovery-y-análisis-de-procesos-actuales)
     - 4.1.2. [Arquitectura y setup de proyecto](#12-arquitectura-y-setup-de-proyecto)
   - 4.2. [FASE 1: Core Infrastructure](#20-fase-1-core-infrastructure)
     - 4.2.1. [Backend core y APIs base](#21-backend-core-y-apis-base)
     - 4.2.2. [Frontend base y sistema de componentes](#22-frontend-base-y-sistema-de-componentes)
   - 4.3. [FASE 2: PDF Ingestion & LLM Processing](#30-fase-2-pdf-ingestion--llm-processing)
     - 4.3.1. [Motor de ingesta de PDFs](#31-motor-de-ingesta-de-pdfs)
     - 4.3.2. [UI de gestión de ingesta](#32-ui-de-gestión-de-ingesta)
   - 4.4. [FASE 3: Optimization Engine](#40-fase-3-optimization-engine)
     - 4.4.1. [Motor de optimización con Timefold](#41-motor-de-optimización-con-timefold)
     - 4.4.2. [API de orquestación de optimización](#42-api-de-orquestación-de-optimización)
   - 4.5. [FASE 4: UI & Integration](#50-fase-4-ui--integration)
     - 4.5.1. [Pantallas de recomendaciones](#51-pantallas-de-recomendaciones)
     - 4.5.2. [Visualización de stock y contenedores](#52-visualización-de-stock-y-contenedores)
   - 4.6. [FASE 5: Testing, Dashboard Analytics & Launch](#60-fase-5-testing-dashboard-analytics--launch)
     - 4.6.1. [Dashboard analítico simplificado](#61-dashboard-analítico-simplificado)
     - 4.6.2. [Testing y QA](#62-testing-y-qa)
     - 4.6.3. [Documentación y training](#63-documentación-y-training)
     - 4.6.4. [Beta privada y launch](#64-beta-privada-y-launch)
5. [Resumen de Esfuerzo por Fase](#resumen-de-esfuerzo-por-fase)
6. [Resumen de Esfuerzo por Rol](#resumen-de-esfuerzo-por-rol)
7. [Resumen de Entregables por Sprint](#resumen-de-entregables-por-sprint)
8. [Dependencias Críticas](#dependencias-críticas)
9. [Riesgos y Buffers](#riesgos-y-buffers)
   - 9.1. [Riesgos Principales](#riesgos-principales)
   - 9.2. [Gestión de Riesgos sin Buffer](#gestión-de-riesgos-sin-buffer)
10. [Exclusiones del MVP (Out of Scope)](#exclusiones-del-mvp-out-of-scope)
11. [Criterios de Aceptación del MVP](#criterios-de-aceptación-del-mvp)
    - 11.1. [Funcionales](#funcionales)
    - 11.2. [No Funcionales](#no-funcionales)
    - 11.3. [Validación de Negocio](#validación-de-negocio)
12. [Próximos Pasos Post-MVP](#próximos-pasos-post-mvp)

---

## Información del Proyecto

| Atributo | Valor |
|----------|-------|
| **Proyecto** | Sistema TMS con IA para optimización de contenedores |
| **Cliente** | Rhenus Logistics |
| **Duración** | 12 semanas (6 sprints de 2 semanas) |
| **Equipo** | 1 Arquitecto/Tech Lead (flexible) + 1 Senior Dev Full-Stack (40h/sem) + 1 Developer Full-Stack (40h/sem) + 1 PO Rhenus |
| **Enfoque** | MVP - Minimum Viable Product |
| **Recursos** | 3 personas, 25% buffer, developers 40h/sem dedicación completa |

---

## Objetivos del MVP

1. ✅ **Motor de optimización** con matching inteligente import-export (Timefold)
2. ✅ **Ingesta automática de PDFs** mediante LLM multimodal (Gemini)
3. ✅ **UI básica** para visualización de recomendaciones y gestión de feedback
4. ⚠️ **Dashboard analítico** simplificado con KPIs esenciales
5. ⚠️ **Gestión de datos maestros** mínima viable

**Nota:** ✅ = Prioridad CRÍTICA | ⚠️ = Alcance reducido por recursos limitados

---

## Principios del WBS

Este WBS sigue las mejores prácticas del PMI (Project Management Institute):

- **Regla del 100%**: Todas las tareas cubren el 100% del trabajo necesario
- **Orientado a entregables**: Cada elemento representa un entregable, no actividades
- **Regla 8/80**: Work packages entre 8-80 horas de esfuerzo
- **Niveles jerárquicos**: 4 niveles (Proyecto → Fase → Entregable → Work Package)

---

## Estructura del WBS

### Resumen en Formato Tabla

| WBS ID | Entregable / Work Package | Esfuerzo (h) | Responsable | Sprint |
|--------|---------------------------|--------------|-------------|---------|
| **1.0** | **FASE 0: Discovery & Setup** | **160h** | | **Sprint 0** |
| 1.1 | Discovery y análisis de procesos actuales | 64h | | Sprint 0 |
| 1.1.1 | Sesiones de discovery con stakeholders de Rhenus | 24h | Arquitecto + PO | Sprint 0 |
| 1.1.2 | Análisis de PDFs de ejemplo | 16h | Arquitecto | Sprint 0 |
| 1.1.3 | Validación de datos maestros | 16h | Developer | Sprint 0 |
| 1.1.4 | Definición de reglas de negocio específicas | 8h | Arquitecto + PO | Sprint 0 |
| 1.2 | Arquitectura y setup de proyecto | 96h | | Sprint 0 |
| 1.2.1 | Arquitectura técnica detallada | 24h | Arquitecto | Sprint 0 |
| 1.2.2 | Setup de Google Cloud Platform | 16h | Arquitecto | Sprint 0 |
| 1.2.3 | Setup de repositorios y CI/CD | 16h | Senior Dev | Sprint 0 |
| 1.2.4 | Ambiente de desarrollo local | 8h | Senior Dev | Sprint 0 |
| 1.2.5 | Modelo de datos inicial | 24h | Developer | Sprint 0 |
| 1.2.6 | Prototipo de UI/UX básico | 8h | Senior Dev | Sprint 0 |
| **2.0** | **FASE 1: Core Infrastructure** | **160h** | | **Sprint 1** |
| 2.1 | Backend core y APIs base | 84h | | Sprint 1 |
| 2.1.1 | API Gateway y autenticación | 16h | Arquitecto | Sprint 1 |
| 2.1.2 | Code review y Tech Lead | 8h | Arquitecto | Sprint 1 |
| 2.1.3 | APIs de datos maestros | 30h | Developer | Sprint 1 |
| 2.1.4 | APIs de órdenes | 30h | Developer | Sprint 1 |
| 2.2 | Frontend base y sistema de componentes | 76h | | Sprint 1 |
| 2.2.1 | Setup de proyecto frontend | 14h | Senior Dev | Sprint 1 |
| 2.2.2 | Sistema de componentes base | 24h | Senior Dev | Sprint 1 |
| 2.2.3 | Pantallas de gestión de datos maestros | 30h | Senior Dev | Sprint 1 |
| 2.2.4 | Integración con APIs backend | 8h | Developer | Sprint 1 |
| **3.0** | **FASE 2: PDF Ingestion & LLM Processing** | **160h** | | **Sprint 2** |
| 3.1 | Motor de ingesta de PDFs | 96h | | Sprint 2 |
| 3.1.1 | Sistema de recepción de emails | 24h | Developer | Sprint 2 |
| 3.1.2 | Integración con Google Gemini (Vertex AI) | 32h | Arquitecto | Sprint 2 |
| 3.1.3 | Sistema de validación anti-alucinaciones | 16h | Arquitecto | Sprint 2 |
| 3.1.4 | Almacenamiento y notificaciones | 24h | Developer | Sprint 2 |
| 3.2 | UI de gestión de ingesta | 64h | | Sprint 2 |
| 3.2.1 | Pantalla de órdenes procesadas | 24h | Senior Dev | Sprint 2 |
| 3.2.2 | Pantalla de revisión manual de PDFs | 24h | Senior Dev | Sprint 2 |
| 3.2.3 | Dashboard de ingesta | 16h | Senior Dev | Sprint 2 |
| **4.0** | **FASE 3: Optimization Engine** | **160h** | | **Sprint 3** |
| 4.1 | Motor de optimización con Timefold + Tech Lead | 80h | | Sprint 3 |
| 4.1.1 | Setup de proyecto Java + Timefold | 8h | Arquitecto | Sprint 3 |
| 4.1.2 | Modelado del problema de optimización | 20h | Arquitecto | Sprint 3 |
| 4.1.3 | Algoritmo de matching import-export | 20h | Arquitecto | Sprint 3 |
| 4.1.4 | Cálculo de rutas multimodales (TRUCK) | 14h | Arquitecto | Sprint 3 |
| 4.1.5 | Generación de recomendaciones con scoring | 8h | Arquitecto | Sprint 3 |
| 4.1.6 | Containerización y deployment a Cloud Run | 6h | Arquitecto | Sprint 3 |
| 4.1.7 | Code review y Tech Lead QA | 4h | Arquitecto | Sprint 3 |
| 4.2 | API de orquestación de optimización | 80h | | Sprint 3 |
| 4.2.1 | Cloud Function de orquestación | 36h | Developer | Sprint 3 |
| 4.2.2 | APIs de gestión de recomendaciones | 28h | Developer | Sprint 3 |
| 4.2.3 | Sistema de notificaciones | 8h | Developer | Sprint 3 |
| 4.2.4 | Soporte UI básico de recomendaciones | 8h | Senior Dev | Sprint 3 |
| **5.0** | **FASE 4: UI & Integration** | **160h** | | **Sprint 4** |
| 5.1 | Pantallas de recomendaciones | 68h | | Sprint 4 |
| 5.1.1 | Dashboard principal de recomendaciones | 20h | Senior Dev | Sprint 4 |
| 5.1.2 | Vista detalle de recomendación | 28h | Senior Dev | Sprint 4 |
| 5.1.3 | Interface de aceptación/rechazo | 14h | Senior Dev | Sprint 4 |
| 5.1.4 | Botón de trigger manual de optimización | 6h | Developer | Sprint 4 |
| 5.2 | Visualización de stock y contenedores | 68h | | Sprint 4 |
| 5.2.1 | Vista de stock en terminales | 20h | Developer | Sprint 4 |
| 5.2.2 | Vista de contenedores post-import | 14h | Developer | Sprint 4 |
| 5.2.3 | Mapa geográfico interactivo | 28h | Developer | Sprint 4 |
| 5.2.4 | Filtros y búsqueda | 6h | Senior Dev | Sprint 4 |
| 5.3 | Tech Lead review crítico + QA integración | 24h | | Sprint 4 |
| 5.3.1 | Code review de frontend completo | 12h | Arquitecto | Sprint 4 |
| 5.3.2 | QA de integración UI-backend | 8h | Arquitecto | Sprint 4 |
| 5.3.3 | Validación de arquitectura y performance | 4h | Arquitecto | Sprint 4 |
| **6.0** | **FASE 5: Testing, Dashboard Analytics & Launch** | **160h** | | **Sprint 5** |
| 6.1 | Dashboard analítico simplificado | 48h | | Sprint 5 |
| 6.1.1 | KPIs de optimización | 24h | Senior Dev | Sprint 5 |
| 6.1.2 | KPIs de adopción | 16h | Senior Dev | Sprint 5 |
| 6.1.3 | Métricas de impacto | 8h | Senior Dev | Sprint 5 |
| 6.2 | Testing y QA | 80h | | Sprint 5 |
| 6.2.1 | Testing del motor de optimización | 24h | Arquitecto | Sprint 5 |
| 6.2.2 | Testing de APIs backend | 24h | Developer | Sprint 5 |
| 6.2.3 | Testing de ingesta de PDFs | 16h | Developer | Sprint 5 |
| 6.2.4 | Testing E2E de frontend | 16h | Senior Dev | Sprint 5 |
| 6.3 | Documentación y training | 24h | | Sprint 5 |
| 6.3.1 | Documentación técnica | 12h | Developer | Sprint 5 |
| 6.3.2 | Documentación de usuario | 4h | Senior Dev | Sprint 5 |
| 6.3.3 | Training a usuarios de Rhenus | 8h | Arquitecto + PO | Sprint 5 |
| 6.4 | Beta privada y launch | 8h | | Sprint 5 |
| 6.4.1 | Beta privada con usuarios piloto | 4h | Todo el equipo | Sprint 5 |
| 6.4.2 | Lanzamiento oficial | 4h | Todo el equipo | Sprint 5 |
| | **TOTAL PROYECTO** | **960h** | | **12 semanas** |

---

### Resumen de Carga de Trabajo por Sprint

| Sprint | Semanas | Arquitecto/Tech Lead | Senior Dev (Full-Stack) | Developer (Full-Stack) | Total | Principales Entregables |
|--------|---------|---------------------|------------------------|------------------------|-------|------------------------|
| **Sprint 0** | 1-2 | 64h (32h/sem) | 48h (24h/sem) | 48h (24h/sem) | 160h | Discovery, Arquitectura, Setup GCP, Modelo datos |
| **Sprint 1** | 3-4 | 24h (12h/sem) | 68h (34h/sem) | 68h (34h/sem) | 160h | APIs backend, Frontend base, UI maestros + Tech Lead review |
| **Sprint 2** | 5-6 | 48h (24h/sem) | 56h (28h/sem) | 56h (28h/sem) | 160h | Gemini LLM, Ingesta PDFs, UI ingesta + Tech Lead |
| **Sprint 3** | 7-8 | 80h (40h/sem) | 40h (20h/sem) | 40h (20h/sem) | 160h | Motor Timefold crítico + Tech Lead/QA |
| **Sprint 4** | 9-10 | 24h (12h/sem) | 68h (34h/sem) | 68h (34h/sem) | 160h | UI recomendaciones, Mapa + Tech Lead review crítico |
| **Sprint 5** | 11-12 | 24h (12h/sem) | 68h (34h/sem) | 68h (34h/sem) | 160h | Dashboard KPIs, Testing, Docs, Launch + QA |
| **TOTAL** | **12 sem** | **264h** | **348h** | **348h** | **960h** | **MVP Completo** |

**Disponibilidad y buffer:**
- **Arquitecto/Tech Lead**: 264h asignadas, dedicación flexible con presencia en TODOS los sprints para code review y QA
- **Senior Dev**: 348h usadas de 480h disponibles (40h/sem × 12 sem) = **+132h buffer (27.5%)**
- **Developer**: 348h usadas de 480h disponibles (40h/sem × 12 sem) = **+132h buffer (27.5%)**
- **Buffer total: 264h (27.5% del proyecto)**

---

### Detalle por Fase

### 1.0 FASE 0: Discovery & Setup
**Sprint 0 | Semanas 1-2 | Esfuerzo: 160 horas-persona**

#### 1.1 Discovery y análisis de procesos actuales
**Esfuerzo: 64 horas-persona**

##### 1.1.1 Sesiones de discovery con stakeholders de Rhenus
- Mapeo de flujos operativos actuales (import, export, tren)
- Identificación de roles y perfiles de usuario
- Validación de supuestos de la oferta técnica
- **Esfuerzo**: 24 horas-persona
- **Responsable**: Arquitecto + PO

##### 1.1.2 Análisis de PDFs de ejemplo
- Recopilación de PDFs de órdenes import/export reales
- Recopilación de PDFs de llegadas ferroviarias
- Análisis de estructura y variabilidad de formatos
- Documentación de campos críticos a extraer
- **Esfuerzo**: 16 horas-persona
- **Responsable**: Arquitecto

##### 1.1.3 Validación de datos maestros
- Obtención de inventario de contenedores
- Catálogo de terminales (Barcelona, Noain, Agoncillo, Miranda)
- Lista de clientes con ubicaciones GPS
- Información de navieras y restricciones
- Matriz de distancias y costes de transporte
- **Esfuerzo**: 16 horas-persona
- **Responsable**: Developer

##### 1.1.4 Definición de reglas de negocio específicas
- Restricciones de navieras sobre reutilización de contenedores
- Políticas de free time y devolución
- Prioridades de clientes
- Criterios de matching (radio máximo, ventana temporal)
- **Esfuerzo**: 8 horas-persona
- **Responsable**: Arquitecto + Rhenus stakeholders

#### 1.2 Arquitectura y setup de proyecto
**Esfuerzo: 96 horas-persona**

##### 1.2.1 Arquitectura técnica detallada
- Refinamiento del diagrama C4 de contenedores
- Definición de contratos de APIs (REST)
- Diseño de esquema de base de datos PostgreSQL
- Arquitectura de seguridad (RBAC, autenticación)
- **Esfuerzo**: 24 horas-persona
- **Responsable**: Arquitecto

##### 1.2.2 Setup de Google Cloud Platform
- Creación de proyecto GCP
- Configuración de Firebase (Hosting, Auth, Firestore)
- Setup de Vertex AI para Gemini
- Configuración de Cloud Storage buckets
- Setup de PostgreSQL (Firebase Data Connect)
- Configuración de IAM y permisos
- **Esfuerzo**: 16 horas-persona
- **Responsable**: Arquitecto

##### 1.2.3 Setup de repositorios y CI/CD
- Repositorio Git (monorepo o multi-repo)
- Estructura de carpetas y convenciones
- GitHub Actions para CI/CD
- Pipelines de build/test/deploy
- Configuración de linters (ESLint, Prettier)
- **Esfuerzo**: 16 horas-persona
- **Responsable**: Senior Dev

##### 1.2.4 Ambiente de desarrollo local
- Docker Compose para desarrollo local
- PostgreSQL local para desarrollo
- Configuración de variables de entorno
- Documentación de setup para nuevos developers
- **Esfuerzo**: 8 horas-persona
- **Responsable**: Senior Dev

##### 1.2.5 Modelo de datos inicial
- Diseño del esquema de PostgreSQL
- Entidades: Containers, Orders, Terminals, Clients, Shipping Lines
- Tablas para Recommendations, Feedback
- Migraciones de base de datos (schema versioning)
- Scripts de seed data para desarrollo
- **Esfuerzo**: 24 horas-persona
- **Responsable**: Developer

##### 1.2.6 Prototipo de UI/UX básico
- Wireframes de pantallas principales
- Flujos de navegación
- Sistema de diseño básico (colores, tipografía, componentes)
- Aprobación de diseño con Rhenus
- **Esfuerzo**: 8 horas-persona
- **Responsable**: Senior Dev

---

### 2.0 FASE 1: Core Infrastructure
**Sprint 1 | Semanas 3-4 | Esfuerzo: 160 horas-persona**

#### 2.1 Backend core y APIs base
**Esfuerzo: 84 horas-persona**

##### 2.1.1 API Gateway y autenticación
- Setup de Cloud Functions con Express.js
- Integración de Firebase Authentication
- Middleware de autenticación (JWT validation)
- RBAC implementation (roles: Operator, Viewer, Admin)
- **Esfuerzo**: 16 horas-persona
- **Responsable**: Arquitecto

##### 2.1.2 Code review y Tech Lead
- Code review del backend core
- Validación de arquitectura de APIs
- Control de calidad del código
- **Esfuerzo**: 8 horas-persona
- **Responsable**: Arquitecto

##### 2.1.3 APIs de datos maestros
- CRUD para Contenedores
- CRUD para Terminales
- CRUD para Clientes (con ubicaciones GPS)
- CRUD para Navieras
- Validaciones de negocio
- **Esfuerzo**: 30 horas-persona
- **Responsable**: Developer

##### 2.1.4 APIs de órdenes
- Endpoint para crear órdenes de import
- Endpoint para crear órdenes de export
- Endpoint para crear llegadas ferroviarias
- Query endpoints (filtros, búsquedas)
- Actualización automática de stock de contenedores
- **Esfuerzo**: 30 horas-persona
- **Responsable**: Developer

#### 2.2 Frontend base y sistema de componentes
**Esfuerzo: 76 horas-persona**

##### 2.2.1 Setup de proyecto frontend
- Vite + React + TypeScript setup
- Routing (React Router)
- State management (Context API + Hooks)
- Configuración de build y deployment a Firebase Hosting
- **Esfuerzo**: 14 horas-persona
- **Responsable**: Senior Dev

##### 2.2.2 Sistema de componentes base
- Layout principal (navbar, sidebar, content area)
- Componentes reutilizables (Button, Input, Table, Modal, etc.)
- Librería de componentes UI (integración)
- Theme y estilos globales
- **Esfuerzo**: 24 horas-persona
- **Responsable**: Senior Dev

##### 2.2.3 Pantallas de gestión de datos maestros
- Pantalla de gestión de Contenedores
- Pantalla de gestión de Clientes
- Pantalla de gestión de Terminales
- Formularios de creación/edición
- Validaciones en frontend
- **Esfuerzo**: 30 horas-persona
- **Responsable**: Senior Dev

##### 2.2.4 Integración con APIs backend
- HTTP client setup (Axios o Fetch)
- Manejo de autenticación (tokens)
- Error handling y feedback al usuario
- Loading states
- **Esfuerzo**: 8 horas-persona
- **Responsable**: Developer

---

### 3.0 FASE 2: PDF Ingestion & LLM Processing
**Sprint 2 | Semanas 5-6 | Esfuerzo: 160 horas-persona**

#### 3.1 Motor de ingesta de PDFs
**Esfuerzo: 96 horas-persona**

##### 3.1.1 Sistema de recepción de emails
- Configuración de inbox de Rhenus
- Setup de Cloud Pub/Sub para eventos de email
- Cloud Function trigger para procesar emails entrantes
- Descarga de attachments (PDFs)
- Almacenamiento en Cloud Storage
- **Esfuerzo**: 24 horas-persona
- **Responsable**: Developer

##### 3.1.2 Integración con Google Gemini (Vertex AI)
- Setup de Vertex AI API
- Prompting para extracción de órdenes import
- Prompting para extracción de órdenes export
- Prompting para extracción de llegadas ferroviarias
- Parsing de respuestas JSON del LLM
- **Esfuerzo**: 32 horas-persona
- **Responsable**: Arquitecto

##### 3.1.3 Sistema de validación anti-alucinaciones
- Validación de campos obligatorios
- Validación de tipos de datos (fechas, números, códigos ISO)
- Detección de valores fuera de rango
- Validación de referencias (clientes, terminales, navieras existen)
- Score de confianza por campo extraído
- Detección de inconsistencias
- **Esfuerzo**: 16 horas-persona
- **Responsable**: Arquitecto

##### 3.1.4 Almacenamiento y notificaciones
- Persistencia de órdenes extraídas en PostgreSQL
- Actualización automática de stock de contenedores
- Sistema de notificaciones para validación fallida
- Queue para revisión manual de PDFs problemáticos
- Logging completo del proceso de ingesta
- **Esfuerzo**: 24 horas-persona
- **Responsable**: Developer

#### 3.2 UI de gestión de ingesta
**Esfuerzo: 64 horas-persona**

##### 3.2.1 Pantalla de órdenes procesadas
- Lista de órdenes import/export
- Filtros (tipo, fecha, estado, cliente)
- Vista detalle de orden individual
- Indicador de confianza de extracción
- **Esfuerzo**: 24 horas-persona
- **Responsable**: Senior Dev

##### 3.2.2 Pantalla de revisión manual de PDFs
- Queue de PDFs con validación fallida
- Visualización de PDF original
- Comparación lado a lado: PDF vs datos extraídos
- Interface para corrección manual
- Aprobación/rechazo de datos extraídos
- **Esfuerzo**: 24 horas-persona
- **Responsable**: Senior Dev

##### 3.2.3 Dashboard de ingesta
- Métricas de procesamiento (PDFs/día, tasa de éxito)
- Gráfico de evolución temporal
- Alertas de errores de procesamiento
- **Esfuerzo**: 16 horas-persona
- **Responsable**: Senior Dev

---

### 4.0 FASE 3: Optimization Engine
**Sprint 3 | Semanas 7-8 | Esfuerzo: 160 horas-persona**

#### 4.1 Motor de optimización con Timefold
**Esfuerzo: 80 horas-persona**

##### 4.1.1 Setup de proyecto Java + Timefold
- Proyecto Maven/Gradle
- Integración de Timefold dependency
- Configuración de solver
- Setup de testing con JUnit
- **Esfuerzo**: 8 horas-persona
- **Responsable**: Arquitecto

##### 4.1.2 Modelado del problema de optimización
- Clases de dominio (Order, Container, Terminal, Client, Route)
- Definición de Planning Entity (orden de export)
- Definición de Planning Variable (contenedor asignado)
- Constraints hard (compatibilidad de contenedores, disponibilidad)
- Constraints soft (coste, tiempo, CO2, distancia)
- **Esfuerzo**: 20 horas-persona
- **Responsable**: Arquitecto

##### 4.1.3 Algoritmo de matching import-export
- Lógica de detección de oportunidades de matching
- Cálculo de proximidad geográfica (radio máximo)
- Validación de ventana temporal
- Validación de compatibilidad de tipos de contenedores
- Validación de restricciones de navieras
- **Esfuerzo**: 20 horas-persona
- **Responsable**: Arquitecto

##### 4.1.4 Cálculo de rutas multimodales (TRUCK)
- Matriz de distancias entre ubicaciones
- Cálculo de costes de transporte
- Cálculo de tiempos de tránsito
- Cálculo de emisiones de CO2
- Comparación ruta tradicional vs. optimizada
- **Esfuerzo**: 14 horas-persona
- **Responsable**: Arquitecto

##### 4.1.5 Generación de recomendaciones con scoring
- Score de confianza de cada recomendación (0-100%)
- Cálculo de ahorro estimado (coste, km, CO2)
- Justificación de la recomendación
- Detalles de ruta propuesta paso a paso
- **Esfuerzo**: 8 horas-persona
- **Responsable**: Arquitecto

##### 4.1.6 Containerización y deployment a Cloud Run
- Dockerfile para aplicación Java
- Build de imagen Docker
- Push a Artifact Registry
- Deployment a Cloud Run
- Configuración de auto-scaling
- **Esfuerzo**: 6 horas-persona
- **Responsable**: Arquitecto

##### 4.1.7 Code review y Tech Lead QA
- Code review del motor de optimización
- Validación de constraints y algoritmos
- Testing de performance del solver
- Control de calidad del código Java
- **Esfuerzo**: 4 horas-persona
- **Responsable**: Arquitecto

#### 4.2 API de orquestación de optimización
**Esfuerzo: 80 horas-persona**

##### 4.2.1 Cloud Function de orquestación
- Endpoint para trigger manual de optimización
- Endpoint para trigger automático (post-ingesta)
- Recopilación de contexto (órdenes, stock, parámetros)
- Invocación del motor Timefold (Cloud Run)
- Almacenamiento de recomendaciones en PostgreSQL
- **Esfuerzo**: 36 horas-persona
- **Responsable**: Developer

##### 4.2.2 APIs de gestión de recomendaciones
- Endpoint para listar recomendaciones (filtros, paginación)
- Endpoint para aceptar recomendación
- Endpoint para rechazar recomendación (con motivo)
- Endpoint para obtener detalle de recomendación
- Actualización de estado de órdenes según feedback
- **Esfuerzo**: 28 horas-persona
- **Responsable**: Developer

##### 4.2.3 Sistema de notificaciones
- Notificación a usuarios conectados sobre nuevas recomendaciones
- Notificación de finalización de proceso de optimización
- **Esfuerzo**: 8 horas-persona
- **Responsable**: Developer

##### 4.2.4 Soporte UI básico de recomendaciones
- Componente React básico para listado de recomendaciones
- Integración con APIs de 4.2.2
- Manejo de estados de carga y errores
- **Esfuerzo**: 8 horas-persona
- **Responsable**: Senior Dev

---

### 5.0 FASE 4: UI & Integration
**Sprint 4 | Semanas 9-10 | Esfuerzo: 160 horas-persona**

#### 5.1 Pantallas de recomendaciones
**Esfuerzo: 68 horas-persona**

##### 5.1.1 Dashboard principal de recomendaciones
- Lista de recomendaciones pendientes
- Score de confianza visual
- Ahorro estimado (coste, km, CO2)
- Filtros (tipo de matching, fecha, cliente, score)
- Ordenamiento (por score, por ahorro, por fecha)
- **Esfuerzo**: 20 horas-persona
- **Responsable**: Senior Dev

##### 5.1.2 Vista detalle de recomendación
- Información completa del matching import-export
- Comparación lado a lado: ruta tradicional vs. optimizada
- Mapa con visualización de ruta propuesta
- Detalles de contenedores involucrados
- Justificación del algoritmo
- **Esfuerzo**: 28 horas-persona
- **Responsable**: Senior Dev

##### 5.1.3 Interface de aceptación/rechazo
- Modal de confirmación de aceptación
- Modal de rechazo con selección de motivo
- Motivos predefinidos (cliente no disponible, timing incompatible, etc.)
- Campo de comentario adicional
- Actualización inmediata de estado en UI
- **Esfuerzo**: 14 horas-persona
- **Responsable**: Senior Dev

##### 5.1.4 Botón de trigger manual de optimización
- Botón para solicitar nueva optimización
- Loading state durante procesamiento
- Feedback de finalización
- **Esfuerzo**: 6 horas-persona
- **Responsable**: Developer

#### 5.2 Visualización de stock y contenedores
**Esfuerzo: 68 horas-persona**

##### 5.2.1 Vista de stock en terminales
- Stock de contenedores en Barcelona (vacíos, llenos)
- Stock en terminales ferroviarias (Noain, Agoncillo, Miranda)
- Clasificación por tipo de contenedor (22G1, 42G1, 45G1)
- Clasificación por estado (vacío disponible, lleno pendiente)
- Filtros por terminal, tipo, naviera
- **Esfuerzo**: 20 horas-persona
- **Responsable**: Developer

##### 5.2.2 Vista de contenedores post-import
- Lista de contenedores vacíos en ubicaciones de clientes
- Tiempo desde que quedaron vacíos
- Indicador de proximidad a órdenes export
- Destacado de oportunidades de matching potenciales
- **Esfuerzo**: 14 horas-persona
- **Responsable**: Developer

##### 5.2.3 Mapa geográfico interactivo
- Integración de Google Maps API
- Pins de terminales con stock (Barcelona, Noain, Agoncillo, Miranda)
- Pins de clientes con contenedores vacíos post-import
- Pins de clientes con órdenes export pendientes
- Líneas conectando oportunidades de matching
- Rutas activas en tiempo real (opcional, nice-to-have)
- **Esfuerzo**: 28 horas-persona
- **Responsable**: Developer

##### 5.2.4 Filtros y búsqueda
- Buscador de contenedores por ID
- Filtros por tipo, estado, ubicación, naviera
- Filtros por edad (tiempo inactivo)
- **Esfuerzo**: 6 horas-persona
- **Responsable**: Senior Dev

#### 5.3 Tech Lead review crítico + QA integración
**Esfuerzo: 24 horas-persona**

##### 5.3.1 Code review de frontend completo
- Revisión exhaustiva del código React/TypeScript
- Validación de componentes y arquitectura frontend
- Verificación de mejores prácticas y patrones
- Control de calidad del código
- **Esfuerzo**: 12 horas-persona
- **Responsable**: Arquitecto

##### 5.3.2 QA de integración UI-backend
- Testing de integración completa frontend-backend
- Validación de flujos end-to-end
- Verificación de manejo de errores
- Testing de rendimiento de la aplicación
- **Esfuerzo**: 8 horas-persona
- **Responsable**: Arquitecto

##### 5.3.3 Validación de arquitectura y performance
- Revisión de arquitectura general del sistema
- Análisis de performance y optimizaciones necesarias
- Validación de escalabilidad
- Recomendaciones de mejora
- **Esfuerzo**: 4 horas-persona
- **Responsable**: Arquitecto

---

### 6.0 FASE 5: Testing, Dashboard Analytics & Launch
**Sprint 5 | Semanas 11-12 | Esfuerzo: 160 horas-persona**

#### 6.1 Dashboard analítico simplificado
**Esfuerzo: 48 horas-persona**

##### 6.1.1 KPIs de optimización
- % de matching import-export exitoso
- Viajes evitados (total)
- Reducción de kilómetros totales
- Reducción de km en vacío
- Gráficos de tendencias temporales
- **Esfuerzo**: 24 horas-persona
- **Responsable**: Senior Dev

##### 6.1.2 KPIs de adopción
- % de aceptación de sugerencias
- % de rechazo de sugerencias
- Distribución de motivos de rechazo
- Tiempo medio de respuesta a recomendaciones
- **Esfuerzo**: 16 horas-persona
- **Responsable**: Senior Dev

##### 6.1.3 Métricas de impacto
- Ahorro de costes estimado (acumulado)
- Reducción de CO2 estimada (acumulado)
- Gráficos de evolución mensual
- **Esfuerzo**: 8 horas-persona
- **Responsable**: Senior Dev

#### 6.2 Testing y QA
**Esfuerzo: 80 horas-persona**

##### 6.2.1 Testing del motor de optimización
- Unit tests de constraints
- Tests de algoritmo de matching
- Tests de cálculo de rutas
- Tests de scoring
- Validación con datos reales de Rhenus
- **Esfuerzo**: 24 horas-persona
- **Responsable**: Arquitecto

##### 6.2.2 Testing de APIs backend
- Unit tests de endpoints críticos
- Integration tests de flujo completo
- Tests de autenticación y autorización
- Tests de validaciones de negocio
- **Esfuerzo**: 24 horas-persona
- **Responsable**: Developer

##### 6.2.3 Testing de ingesta de PDFs
- Tests con PDFs reales de Rhenus
- Tests de validación anti-alucinaciones
- Tests de casos edge (PDFs malformados)
- Tests de actualización de stock
- **Esfuerzo**: 16 horas-persona
- **Responsable**: Developer

##### 6.2.4 Testing E2E de frontend
- Tests de flujos críticos (login, ver recomendaciones, aceptar/rechazar)
- Tests de responsiveness (desktop, tablet)
- Tests de accesibilidad básica
- Cross-browser testing
- **Esfuerzo**: 16 horas-persona
- **Responsable**: Senior Dev

#### 6.3 Documentación y training
**Esfuerzo: 24 horas-persona**

##### 6.3.1 Documentación técnica
- README de setup de proyecto
- Documentación de APIs (Swagger/OpenAPI)
- Guía de deployment
- Guía de troubleshooting
- **Esfuerzo**: 12 horas-persona
- **Responsable**: Developer

##### 6.3.2 Documentación de usuario
- Manual de usuario del sistema
- Guías de uso de cada funcionalidad
- FAQs
- **Esfuerzo**: 4 horas-persona
- **Responsable**: Senior Dev

##### 6.3.3 Training a usuarios de Rhenus
- Sesión de training a operadores
- Sesión de training a administradores
- Q&A y feedback inicial
- **Esfuerzo**: 8 horas-persona
- **Responsable**: Arquitecto + PO

#### 6.4 Beta privada y launch
**Esfuerzo: 8 horas-persona**

##### 6.4.1 Beta privada con usuarios piloto
- Selección de 2-3 operadores para beta
- Monitoring intensivo durante primera semana
- Recopilación de feedback
- Fixing de bugs críticos
- **Esfuerzo**: 4 horas-persona (soporte continuo)
- **Responsable**: Todo el equipo

##### 6.4.2 Lanzamiento oficial
- Comunicación de lanzamiento a todos los usuarios
- Monitoring post-launch
- Soporte on-call durante primera semana
- **Esfuerzo**: 4 horas-persona (soporte continuo)
- **Responsable**: Todo el equipo

---

## Resumen de Esfuerzo por Fase

| Fase | Duración | Arq/Tech Lead | Senior Dev | Developer | Total | % del Proyecto |
|------|----------|--------------|-----------|-----------|-------|----------------|
| **Fase 0: Discovery & Setup** | Sprint 0 (2 sem) | 64h | 48h | 48h | 160h | 16.7% |
| **Fase 1: Core Infrastructure** | Sprint 1 (2 sem) | 24h | 68h | 68h | 160h | 16.7% |
| **Fase 2: PDF Ingestion & LLM** | Sprint 2 (2 sem) | 48h | 56h | 56h | 160h | 16.7% |
| **Fase 3: Optimization Engine** | Sprint 3 (2 sem) | 80h | 40h | 40h | 160h | 16.7% |
| **Fase 4: UI & Integration** | Sprint 4 (2 sem) | 24h | 68h | 68h | 160h | 16.7% |
| **Fase 5: Testing & Launch** | Sprint 5 (2 sem) | 24h | 68h | 68h | 160h | 16.7% |
| **TOTAL** | **12 semanas** | **264h** | **348h** | **348h** | **960h** | **100%** |

---

## Resumen de Esfuerzo por Rol

**Composición del equipo:**
- **1 Arquitecto/Tech Lead** - Rol técnico principal (arquitectura, infraestructura GCP, Gemini/LLM, motor Timefold) + Tech Lead (code review, QA, control de calidad, gestión técnica) - Dedicación flexible
- **1 Senior Developer Full-Stack** - Desarrollo full-stack senior (frontend React/TypeScript, backend Node.js, UI/UX, liderazgo técnico) - **40h/semana dedicación completa**
- **1 Developer Full-Stack** - Desarrollo full-stack mid-level (APIs backend, frontend, integraciones, testing) - **40h/semana dedicación completa**
- **1 Product Owner de Rhenus** - Responsable de producto (sin asignación de horas de desarrollo)
- **1 Data Scientist** - OPCIONAL, solo para forecasting/ML si se requiere (NO asignado en este MVP)

**Equipo técnico de 3 personas:**

| Rol | Esfuerzo Estimado | % del Total | Disponibilidad (12 semanas) | h/semana promedio | h/sem máxima | Buffer |
|-----|-------------------|-------------|----------------------------|-------------------|--------------|--------|
| **Arquitecto/Tech Lead** | 264 horas-persona | 27.5% | Flexible | 22h/sem | 40h/sem (Sprint 3) | ✅ Flexible |
| **Senior Developer Full-Stack** | 348 horas-persona | 36.25% | 480h (40h/sem × 12) | 29h/sem | 34h/sem | ✅ +132h (27.5%) |
| **Developer Full-Stack** | 348 horas-persona | 36.25% | 480h (40h/sem × 12) | 29h/sem | 34h/sem | ✅ +132h (27.5%) |
| **TOTAL** | **960 horas-persona** | **100%** | **960h + buffers** | - | - | **+264h (27.5%)** |

**Distribución de responsabilidades:**

**Arquitecto/Tech Lead (264h - flexible, pico 40h/semana en Sprint 3):**
- **Liderazgo técnico en TODOS los sprints**: Code review continuo, control de calidad, gestión técnica del proyecto
- Arquitectura técnica y diseño del sistema (Sprint 0: 24h)
- Setup de infraestructura GCP (Firebase, Vertex AI, Cloud Run - Sprint 0: 16h)
- API Gateway y autenticación (Sprint 1: 16h)
- Integración con Google Gemini (Vertex AI) para extracción de PDFs (Sprint 2: 32h)
- Sistema de validación anti-alucinaciones (Sprint 2: 16h)
- **Motor de optimización Timefold (Java) - algoritmo core crítico (Sprint 3: 76h técnico + 4h Tech Lead)**
- Algoritmo de matching import-export y cálculo de rutas
- Testing del motor de optimización (Sprint 5: 24h)
- Training a usuarios de Rhenus (Sprint 5)
- **Code review y QA en TODOS los sprints**:
  - Sprint 0: 64h (setup + arquitectura)
  - Sprint 1: 24h (16h API Gateway + 8h Tech Lead)
  - Sprint 2: 48h (Gemini + validación)
  - Sprint 3: 80h (Motor Timefold + Tech Lead)
  - Sprint 4: 24h (Code review frontend + QA integración + validación performance)
  - Sprint 5: 24h (Testing + QA final)

**Senior Developer Full-Stack (348h - dedicación completa 40h/semana):**
- **Liderazgo técnico del equipo de desarrollo frontend**
- Setup de repositorios y CI/CD (Sprint 0: 16h)
- Prototipo UI/UX básico (Sprint 0: 8h)
- **Setup completo de proyecto frontend** (Sprint 1: 14h)
- **Sistema de componentes base React/TypeScript** (Sprint 1: 24h)
- Frontend principal: React + TypeScript + Vite, sistema de componentes, UI/UX
- Pantallas de gestión de datos maestros (Sprint 1: 30h)
- UI completa de ingesta de PDFs (Sprint 2: 56h - órdenes, revisión manual, dashboard)
- UI de recomendaciones completa (Sprint 4: 62h - dashboard, detalle, aceptación/rechazo)
- Dashboard analítico con KPIs (Sprint 5: 48h - optimización, adopción, impacto)
- Testing E2E de frontend (Sprint 5: 16h)
- Documentación de usuario (Sprint 5: 4h)
- **Code reviews y pair programming con Developer**
- Soporte backend cuando necesario (full-stack)

**Developer Full-Stack (348h - dedicación completa 40h/semana):**
- Validación de datos maestros y modelo de datos
- **APIs de datos maestros** (CRUD contenedores, terminales, clientes, navieras)
- **APIs de órdenes** (import, export, ferrocarril)
- Sistema de recepción de emails y procesamiento de PDFs
- Almacenamiento y notificaciones
- **APIs de orquestación de optimización**
- APIs de gestión de recomendaciones
- Visualización de stock y contenedores
- Mapa geográfico interactivo (Google Maps) compartido
- Testing de APIs backend e ingesta de PDFs
- Documentación técnica
- Soporte frontend cuando necesario (full-stack)

**Data Scientist (OPCIONAL - NO en MVP):**
- Solo se involucraría en funcionalidades de forecasting/ML
- Predicción de demanda con ML (funcionalidad post-MVP)
- NO asignado a tareas actuales del MVP

**Conclusión**: Con un equipo técnico de **3 personas** (1 Arquitecto/Tech Lead flexible + 2 developers full-stack a dedicación completa):
- **Arquitecto/Tech Lead**: 264h, pico de 40h/semana en Sprint 3 (motor Timefold crítico + Tech Lead)
- **Senior Developer**: 348h necesarias vs 480h disponibles (**+132h buffer, 27.5%**)
- **Developer**: 348h necesarias vs 480h disponibles (**+132h buffer, 27.5%**)
- **Ambos developers con dedicación completa 40h/semana** (disponibles para el proyecto)
- **Arquitecto presente en TODOS los sprints** para code review, QA y liderazgo técnico
- **Arquitecto máximo 40h/semana** en Sprint 3 (NO excede - Timefold + Tech Lead)
- **Buffer total**: 264 horas (27.5% del proyecto)

**DIMENSIONAMIENTO DE PROYECTO:**

1. **Dedicación completa garantizada**: Developers disponibles 40h/semana todo el proyecto
2. **Flexibilidad full-stack**: Ambos developers pueden hacer frontend y backend
3. **Absorber imprevistos**: Buffer del 27.5% permite manejar complejidad inesperada
4. **Calidad asegurada**: Arquitecto/Tech Lead con code review y QA en TODOS los sprints
5. **Tech Lead continuo**: Sprint 1 (24h), Sprint 4 (24h), Sprint 5 (24h) dedicados a revisión
6. **Balance sano**: Promedio 29h/sem para devs, picos hasta 34h/sem cuando necesario
7. **Arquitecto enfocado**: Puede dedicarse intensamente al motor Timefold en Sprint 3 (40h/sem)
8. **Ningún rol excede 40h/semana**: Distribución sostenible y balanceada

---

## Resumen de Entregables por Sprint

| Sprint | Semanas | Entregables Principales |
|--------|---------|------------------------|
| **Sprint 0** | 1-2 | • Discovery completo<br>• Arquitectura definida<br>• Infraestructura GCP setup<br>• Repositorio y CI/CD<br>• Modelo de datos inicial |
| **Sprint 1** | 3-4 | • APIs de autenticación y maestros<br>• APIs de órdenes<br>• Frontend base con componentes<br>• Pantallas de gestión de maestros |
| **Sprint 2** | 5-6 | • Sistema de ingesta de PDFs funcional<br>• Integración con Gemini<br>• Validación anti-alucinaciones<br>• UI de órdenes y revisión manual |
| **Sprint 3** | 7-8 | • Motor Timefold funcionando<br>• Algoritmo de matching import-export<br>• Generación de recomendaciones<br>• Deployment a Cloud Run |
| **Sprint 4** | 9-10 | • Pantallas de recomendaciones completas<br>• Mapa geográfico con stock<br>• Interface de aceptación/rechazo<br>• Visualización de contenedores |
| **Sprint 5** | 11-12 | • Dashboard analítico con KPIs<br>• Testing completo (E2E, integración, unit)<br>• Documentación y training<br>• Beta privada y lanzamiento |

---

## Dependencias Críticas

| Dependencia | Impacto | Mitigación |
|-------------|---------|------------|
| **Acceso a PDFs reales de Rhenus** | Crítico para Sprint 2 | Solicitar desde Sprint 0. Usar PDFs sintéticos si hay retraso. |
| **Datos maestros completos** | Crítico para Sprint 3 | Obtener en Sprint 0. Usar datos mock si faltan. |
| **Validación de reglas de negocio** | Alto para algoritmo de optimización | Discovery detallado en Sprint 0. Iteraciones posteriores. |
| **Disponibilidad de stakeholders** | Alto para validaciones | Agenda semanal fija. Comunicación asíncrona documentada. |
| **Aprobación de diseño UI** | Medio para Sprint 1 | Wireframes en Sprint 0. Feedback rápido. |

---

## Riesgos y Buffers

### Riesgos Principales

1. **Complejidad subestimada del motor Timefold**: Algoritmo de optimización puede requerir más iteraciones
   - **Mitigación**: ⚠️ SIN BUFFER - Priorizar versión básica funcional, optimizaciones post-MVP

2. **Calidad de extracción de PDFs con Gemini**: LLM puede requerir mucho tuning de prompts
   - **Mitigación**: Validación anti-alucinaciones + revisión manual como fallback

3. **Disponibilidad de stakeholders de Rhenus**: Retrasos en validaciones y feedback
   - **Mitigación**: Decisiones documentadas, supuestos validados post-facto si necesario

4. **Scope creep**: Solicitudes de funcionalidades adicionales
   - **Mitigación**: Backlog de post-MVP. Change requests formales.

### Gestión de Riesgos con Buffer del 25%

Con 240 horas de buffer (25% del proyecto), el equipo puede absorber imprevistos comunes:

**Estrategias de mitigación:**

1. **Priorización MoSCoW clara**:
   - **Must Have**: Motor de optimización + Ingesta PDFs con LLM + UI recomendaciones
   - **Should Have**: Dashboard analítico + Visualización stock con mapa
   - **Could Have**: Mejoras UI/UX, validaciones avanzadas
   - **Won't Have (en MVP)**: Integración TMS existente, tracking GPS, app móvil

2. **Buffer por rol estratégicamente distribuido**:
   - Senior Dev: 168h buffer (35%) - Puede absorber complejidad en APIs o integraciones
   - Mid Dev: 72h buffer (15%) - Margen para refinamiento UI/UX y testing
   - Arquitecto: 0h buffer pero medio tiempo - Puede aumentar a 30-40h/semana puntualmente si crítico

3. **Identificación temprana de bloqueos**:
   - Daily standups para detectar problemas inmediatamente
   - Escalación rápida a PO de Rhenus si falta información/decisiones
   - Revisión semanal de consumo de horas vs. planificado

4. **Alcance completo viable**:
   - El buffer permite implementar todas las funcionalidades planificadas
   - Testing completo (unit, integration, E2E) está contemplado
   - Documentación técnica y de usuario incluida

5. **Flexibilidad del equipo**:
   - Senior Dev puede apoyar en tareas de deployment o Cloud Functions si necesario
   - Mid Dev con 34h/semana promedio puede aumentar puntualmente a 40h
   - Arquitecto en 20h/semana puede escalar si Sprint 3 (Timefold) requiere más tiempo

---

## Exclusiones del MVP (Out of Scope)

Las siguientes funcionalidades quedan **fuera del alcance** de este MVP de 12 semanas:

| Categoría | Funcionalidades Excluidas |
|-----------|---------------------------|
| **Integraciones** | • Integración con TMS existente de Rhenus<br>• APIs públicas para terceros<br>• Integración con sistemas de navieras |
| **Aplicaciones móviles** | • App nativa iOS/Android |
| **Tracking GPS** | • Tracking en tiempo real de contenedores<br>• Integración con IoT/sensores |
| **Funcionalidades avanzadas** | • Predicción de demanda con ML<br>• Rutas multimodales con TREN (solo TRUCK en MVP) |
| **Analytics avanzados** | • Reportes personalizables<br>• Exportación de datos<br>• BI integrado |

**Nota**: Estas funcionalidades se pueden incorporar en fases post-MVP según validación y ROI del sistema inicial.

---

## Criterios de Aceptación del MVP

Para considerar el MVP completo y listo para lanzamiento:

### Funcionales

- ✅ Sistema procesa PDFs de órdenes import/export con tasa de éxito ≥ 90%
- ✅ Sistema procesa PDFs de llegadas ferroviarias con tasa de éxito ≥ 90%
- ✅ Motor de optimización genera recomendaciones de matching válidas
- ✅ Operadores pueden aceptar/rechazar recomendaciones y proporcionar feedback
- ✅ Dashboard muestra KPIs básicos de optimización y adopción
- ✅ Mapa geográfico visualiza stock y oportunidades de matching
- ✅ Sistema de autenticación y autorización RBAC funcional

### No Funcionales

- ✅ Procesamiento de PDFs en < 2 minutos desde recepción
- ✅ Generación de recomendaciones en < 2 minutos
- ✅ UI responsive en desktop y tablet
- ✅ Disponibilidad ≥ 99% durante horario laboral
- ✅ Tests unitarios y de integración con coverage ≥ 80%
- ✅ Documentación técnica y de usuario completa
- ✅ Training realizado a usuarios piloto

### Validación de Negocio

- ✅ Al menos 3 operadores de Rhenus han usado el sistema en beta
- ✅ Al menos 1 recomendación de matching ha sido aceptada y ejecutada
- ✅ Feedback positivo de stakeholders de Rhenus sobre usabilidad

---

## Próximos Pasos Post-MVP

Funcionalidades candidatas para iteraciones posteriores (priorizadas):

1. **Rutas multimodales TRUCK + TREN**: Optimización considerando transporte ferroviario
2. **Predicción de demanda con ML**: Anticipar necesidades futuras de contenedores
3. **Dashboard analítico avanzado**: Reportes personalizables, exportación de datos
4. **Integración con TMS existente**: Generación automática de órdenes de transporte
5. **Tracking GPS**: Visibilidad en tiempo real de contenedores
6. **Aplicación móvil**: App nativa para operadores en campo
7. **Expansión geográfica**: Otras zonas de Rhenus (más allá del norte de España)
