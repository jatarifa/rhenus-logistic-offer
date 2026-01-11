# Rhenus Logistics - Sistema TMS con IA

## 📋 Descripción del Proyecto

Este repositorio contiene la documentación técnica y de planificación para el **MVP del Sistema TMS (Transport Management System) con Inteligencia Artificial** desarrollado para **Rhenus Logistics**.

El sistema está diseñado para optimizar la gestión de contenedores mediante matching inteligente import-export, reduciendo costes operativos, kilómetros en vacío y emisiones de CO2.

### 🎯 Objetivos Principales

1. **Motor de optimización** con matching inteligente import-export (Timefold)
2. **Ingesta automática de PDFs** mediante LLM multimodal (Google Gemini)
3. **UI básica** para visualización de recomendaciones y gestión de feedback
4. **Dashboard analítico** simplificado con KPIs esenciales
5. **Gestión de datos maestros** mínima viable

---

## 📚 Documentación del Proyecto

### Documentos Principales

| Documento | Descripción | Enlace |
|-----------|-------------|--------|
| **Oferta Técnica** | Propuesta técnica completa con alcance, arquitectura, tecnologías y estimaciones | [oferta-tecnica-rhenus.md](./oferta-tecnica-rhenus.md) |
| **WBS (Work Breakdown Structure)** | Desglose detallado del trabajo por fases, sprints y responsables | [wbs-rhenus-mvp.md](./wbs-rhenus-mvp.md) |

### 🏗️ Diagramas de Arquitectura

Todos los diagramas están disponibles en formato PlantUML (`.puml`) y SVG renderizado (`.svg`):

| Diagrama | Descripción | PlantUML | SVG |
|----------|-------------|----------|-----|
| **C4 - Containers** | Arquitectura del sistema (nivel contenedores C4) | [c4-containers.puml](./diagrams/c4-containers.puml) | [📊 Ver SVG](./diagrams/c4-containers.svg) |
| **Flujo de Ingesta** | Secuencia de ingesta automática de PDFs con LLM | [sequence-ingestion-flow.puml](./diagrams/sequence-ingestion-flow.puml) | [📊 Ver SVG](./diagrams/sequence-ingestion-flow.svg) |
| **Flujo del Operador** | Interacción del operador con recomendaciones | [sequence-operator-flow.puml](./diagrams/sequence-operator-flow.puml) | [📊 Ver SVG](./diagrams/sequence-operator-flow.svg) |
| **Flujo de Optimización** | Proceso completo del motor de optimización | [sequence-optimization-flow.puml](./diagrams/sequence-optimization-flow.puml) | [📊 Ver SVG](./diagrams/sequence-optimization-flow.svg) |

---

## 🚀 Stack Tecnológico

### Backend
- **Node.js** + TypeScript + Express.js
- **PostgreSQL** (Firebase Data Connect)
- **Google Cloud Functions** (serverless)
- **Timefold** (Java) para optimización

### Frontend
- **React** + TypeScript + Vite
- **Firebase Hosting**
- **Google Maps API**

### IA/ML
- **Google Gemini** (Vertex AI) para extracción de PDFs
- Sistema de validación anti-alucinaciones

### Infraestructura
- **Google Cloud Platform**
- **Firebase** (Auth, Hosting, Firestore)
- **Cloud Run** (motor Timefold)
- **GitHub Actions** (CI/CD)

---

## 👥 Equipo del Proyecto

### Equipo Técnico (3 personas)

| Rol | Dedicación | Esfuerzo Total | Responsabilidades |
|-----|------------|----------------|-------------------|
| **Arquitecto/Tech Lead** | Flexible (pico 40h/sem) | 264h | Arquitectura, GCP, Gemini/LLM, Motor Timefold, Code Review continuo, QA |
| **Senior Developer Full-Stack** | 40h/sem | 348h | Frontend React/TypeScript, Backend Node.js, UI/UX, Testing E2E |
| **Developer Full-Stack** | 40h/sem | 348h | APIs backend, Integraciones, Visualización, Testing |
| **Product Owner (Rhenus)** | Cliente | - | Validación de negocio, priorización |

**Total Proyecto:** 960 horas-persona | **Buffer:** 264h (27.5%)

---

## 📅 Planificación

### Duración
- **12 semanas** (6 sprints de 2 semanas)
- Enero - Marzo 2026

### Fases del Proyecto

| Sprint | Fase | Entregables Principales |
|--------|------|------------------------|
| **Sprint 0** (Sem 1-2) | Discovery & Setup | Arquitectura, Setup GCP, Modelo de datos |
| **Sprint 1** (Sem 3-4) | Core Infrastructure | APIs backend, Frontend base, UI maestros |
| **Sprint 2** (Sem 5-6) | PDF Ingestion & LLM | Gemini LLM, Ingesta PDFs, UI ingesta |
| **Sprint 3** (Sem 7-8) | Optimization Engine | Motor Timefold, Matching import-export |
| **Sprint 4** (Sem 9-10) | UI & Integration | UI recomendaciones, Mapa, Visualización |
| **Sprint 5** (Sem 11-12) | Testing & Launch | Dashboard KPIs, Testing E2E, Launch |

---

## 📊 Métricas de Éxito

### KPIs de Optimización
- % de matching import-export exitoso
- Reducción de kilómetros en vacío
- Reducción de emisiones de CO2
- Viajes evitados

### KPIs de Adopción
- % de aceptación de sugerencias
- % de rechazo de sugerencias
- Tiempo medio de respuesta a recomendaciones

### KPIs de Impacto
- Ahorro de costes estimado (acumulado)
- Reducción de CO2 estimada (acumulado)

---

## 🔒 Criterios de Aceptación del MVP

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

---

## 🚫 Exclusiones del MVP (Out of Scope)

- Integración con TMS existente de Rhenus
- Aplicaciones móviles nativas (iOS/Android)
- Tracking GPS en tiempo real
- Rutas multimodales con TREN (solo TRUCK en MVP)
- Predicción de demanda con ML
- APIs públicas para terceros

---

## 📝 Notas Adicionales

- Este proyecto utiliza metodología **Agile/Scrum** con sprints de 2 semanas
- El WBS sigue las mejores prácticas del **PMI (Project Management Institute)**
- Todos los diagramas están creados con **PlantUML** para facilitar versionado y mantenimiento
- El código y la documentación técnica se mantendrán en repositorios separados

---

**🔗 Enlaces Rápidos:**
- [📄 Oferta Técnica](./oferta-tecnica-rhenus.md)
- [📋 WBS Detallado](./wbs-rhenus-mvp.md)
- [🏗️ Diagrama de Arquitectura](./diagrams/c4-containers.svg)
- [🔄 Flujos del Sistema](./diagrams/)
