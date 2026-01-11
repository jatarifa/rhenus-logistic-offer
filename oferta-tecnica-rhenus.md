# Oferta Técnica - Rhenus Logistics

**Cliente:** Rhenus Logistics
**Fecha:** 11 de Enero de 2026
**Preparado por:** José - Arquitecto de Sistemas y Software

---

## Tabla de Contenidos

1. [Información del Cliente](#1-información-del-cliente)
2. [Resumen Ejecutivo](#2-resumen-ejecutivo)
3. [Objetivos del Proyecto](#3-objetivos-del-proyecto)
   - 3.1. [Contexto del Problema](#31-contexto-del-problema)
   - 3.2. [Objetivos Principales](#32-objetivos-principales)
   - 3.3. [Capacidades Clave del Sistema](#33-capacidades-clave-del-sistema)
   - 3.4. [Alcance del MVP](#34-alcance-del-mvp)
   - 3.5. [Modelo de Operación del MVP](#35-modelo-de-operación-del-mvp)
   - 3.6. [Capacidades de Análisis y Visualización](#36-capacidades-de-análisis-y-visualización)
   - 3.7. [Supuestos e Incógnitas del Proyecto](#37-supuestos-e-incógnitas-del-proyecto)
4. [Alcance de la Solución](#4-alcance-de-la-solución)
   - 4.1. [Visión General del Sistema](#41-visión-general-del-sistema)
   - 4.2. [Componentes Principales](#42-componentes-principales)
   - 4.3. [Perfiles de Usuario](#43-perfiles-de-usuario)
   - 4.4. [Funcionalidades Core](#44-funcionalidades-core)
   - 4.5. [Gestión de Datos Maestros](#45-gestión-de-datos-maestros)
   - 4.6. [Aspectos Técnicos Clave](#46-aspectos-técnicos-clave)
   - 4.7. [Funcionalidades Fuera de Alcance del MVP](#47-funcionalidades-fuera-de-alcance-del-mvp)
5. [Arquitectura Técnica Propuesta](#5-arquitectura-técnica-propuesta)
   - 5.1. [Visión General de la Arquitectura](#51-visión-general-de-la-arquitectura)
   - 5.2. [Stack Tecnológico](#52-stack-tecnológico)
   - 5.3. [Flujos de Datos Principales](#53-flujos-de-datos-principales)
   - 5.4. [Escalabilidad y Rendimiento](#54-escalabilidad-y-rendimiento)
   - 5.5. [Seguridad](#55-seguridad)
   - 5.6. [Consideraciones de Implementación](#56-consideraciones-de-implementación)
6. [Tecnologías y Herramientas](#6-tecnologías-y-herramientas)
   - 6.1. [Plataforma Cloud y Servicios Core](#61-plataforma-cloud-y-servicios-core)
   - 6.2. [Frontend](#62-frontend)
   - 6.3. [Backend y APIs](#63-backend-y-apis)
   - 6.4. [Motor de Optimización](#64-motor-de-optimización)
   - 6.5. [Bases de Datos](#65-bases-de-datos)
   - 6.6. [Almacenamiento y Mensajería](#66-almacenamiento-y-mensajería)
   - 6.7. [Autenticación, Seguridad y Secrets](#67-autenticación-seguridad-y-secrets)
   - 6.8. [Observabilidad y Monitoring](#68-observabilidad-y-monitoring)
   - 6.9. [CI/CD y DevOps](#69-cicd-y-devops)
   - 6.10. [Herramientas de Desarrollo](#610-herramientas-de-desarrollo)
   - 6.11. [Testing y Calidad](#611-testing-y-calidad)
   - 6.12. [Gestión de Proyecto](#612-gestión-de-proyecto)
   - 6.13. [Librerías y Frameworks Adicionales Clave](#613-librerías-y-frameworks-adicionales-clave)
   - 6.14. [Costes Estimados de Infraestructura Cloud (MVP)](#614-costes-estimados-de-infraestructura-cloud-mvp)
7. [Cronograma y Fases](#7-cronograma-y-fases)
   - 7.1. [Metodología de Desarrollo](#71-metodología-de-desarrollo)
   - 7.2. [Fases del Proyecto](#72-fases-del-proyecto)
   - 7.3. [Cronograma Consolidado](#73-cronograma-consolidado)
   - 7.4. [Hitos Clave (Milestones)](#74-hitos-clave-milestones)
   - 7.5. [Estrategia de Despliegue](#75-estrategia-de-despliegue)
   - 7.6. [Dependencias y Riesgos de Cronograma](#76-dependencias-y-riesgos-de-cronograma)
8. [Equipo y Recursos](#8-equipo-y-recursos)
   - 8.1. [Estructura del Equipo de Desarrollo](#81-estructura-del-equipo-de-desarrollo)
   - 8.2. [Dedicación por Fase](#82-dedicación-por-fase)
   - 8.3. [Organización del Equipo](#83-organización-del-equipo)
   - 8.4. [Recursos Técnicos](#84-recursos-técnicos)
   - 8.5. [Requerimientos del Cliente (Rhenus)](#85-requerimientos-del-cliente-rhenus)
   - 8.6. [Modelo de Trabajo](#86-modelo-de-trabajo)
   - 8.7. [Ramp-up y Onboarding](#87-ramp-up-y-onboarding)
   - 8.8. [Consideraciones de Escalabilidad del Equipo](#88-consideraciones-de-escalabilidad-del-equipo)
9. [Presupuesto](#9-presupuesto)
   - 9.1. [Modelo de Presupuesto](#91-modelo-de-presupuesto)
   - 9.2. [Costes de Personal de Desarrollo](#92-costes-de-personal-de-desarrollo)
   - 9.3. [Costes de Infraestructura Cloud](#93-costes-de-infraestructura-cloud)
   - 9.4. [Herramientas y Licencias](#94-herramientas-y-licencias)
   - 9.5. [Otros Costes](#95-otros-costes)
   - 9.6. [Resumen de Presupuesto del MVP](#96-resumen-de-presupuesto-del-mvp)
   - 9.7. [Modelo de Facturación Propuesto](#97-modelo-de-facturación-propuesto)
   - 9.8. [Costes Post-MVP (Primer Año de Operación)](#98-costes-post-mvp-primer-año-de-operación)
   - 9.9. [Retorno de Inversión (ROI) Esperado](#99-retorno-de-inversión-roi-esperado)
   - 9.10. [Opciones de Reducción de Presupuesto](#910-opciones-de-reducción-de-presupuesto)
10. [Riesgos y Mitigación](#10-riesgos-y-mitigación)
    - 10.1. [Metodología de Gestión de Riesgos](#101-metodología-de-gestión-de-riesgos)
    - 10.2. [Riesgos Técnicos](#102-riesgos-técnicos)
    - 10.3. [Riesgos de Proyecto](#103-riesgos-de-proyecto)
    - 10.4. [Riesgos de Negocio](#104-riesgos-de-negocio)
    - 10.5. [Riesgos de Seguridad y Cumplimiento](#105-riesgos-de-seguridad-y-cumplimiento)
    - 10.6. [Matriz de Riesgos (Probabilidad × Impacto)](#106-matriz-de-riesgos-probabilidad--impacto)
    - 10.7. [Plan de Comunicación de Riesgos](#107-plan-de-comunicación-de-riesgos)
    - 10.8. [Lecciones Aprendidas y Mejora Continua](#108-lecciones-aprendidas-y-mejora-continua)
11. [Referencias](#referencias)

---

## 1. Información del Cliente

Rhenus Logistics es una empresa de logística global con:
- Presencia en España desde 1964
- 37 delegaciones en Península, Canarias y Baleares
- Parte del Rhenus Group (8.6 billones € facturación anual, 39.000 empleados, 1.120 ubicaciones)
- Servicios: Transporte (aéreo, marítimo, carretera, ferroviario), almacenamiento, logística portuaria, soluciones digitales

---

## 2. Resumen Ejecutivo

### El Desafío

Rhenus Logistics enfrenta uno de los mayores retos de la industria del transporte de contenedores: el **reposicionamiento de contenedores vacíos**, un problema que genera aproximadamente **$20 billones en costes anuales a nivel global**. El 33% de los contenedores en circulación están vacíos y los contenedores pasan casi el 50% de su vida útil inactivos, generando costes innecesarios de transporte, almacenamiento y emisiones de CO2.

En las operaciones de Rhenus en la zona norte de España, los contenedores de **importación** que quedan vacíos en ubicaciones de clientes son devueltos a terminales (Barcelona o terminales ferroviarias), mientras que las órdenes de **exportación** requieren recoger contenedores vacíos de esas mismas terminales. **Este doble viaje (devolución + recogida) es completamente evitable** si se conecta un contenedor vacío de import con una orden cercana de export.

### La Solución Propuesta

Proponemos desarrollar un **MVP (Minimum Viable Product)** de un sistema TMS avanzado con inteligencia artificial que optimice el uso de contenedores vacíos mediante **matching inteligente import-export**. El sistema funcionará como una **plataforma de apoyo a la decisión** que proporcionará recomendaciones inteligentes a los operadores de Rhenus, manteniendo el control humano en la toma de decisiones finales.

**Alcance del MVP:**
- **Geográfico:** Zona norte de España (Bilbao como centro de operaciones, Barcelona como terminal marítima, Noain/Agoncillo/Miranda como terminales ferroviarias)
- **Modos de transporte:** TRAIN (ferroviario) y TRUCK (carretera)
- **Tipos de contenedores:** 22G1 (20'DV), 42G1 (40'DV), 45G1 (40'HC)
- **Propietarios:** Todos los contenedores son propiedad de navieras (Maersk, Hapag-Lloyd, MSC, CMA CGM, ONE)

### Capacidades Clave del Sistema

1. **Procesamiento Automático de PDFs con LLM Multimodal (Google Gemini)**
   - Extracción automática de datos de órdenes de import/export
   - Procesamiento de PDFs de llegadas ferroviarias (contenedores vacíos y llenos)
   - Validación anti-alucinaciones para garantizar precisión
   - Actualización automática de stock en terminales

2. **Motor de Optimización con Timefold**
   - Matching inteligente entre contenedores vacíos de import y órdenes de export cercanas
   - Cálculo de rutas óptimas multiobjetivo (coste + tiempo + CO2)
   - Generación de recomendaciones con nivel de confianza
   - **Valor tangible:** Eliminación de hasta 2 viajes por cada matching exitoso (33% reducción en el ejemplo de la sección 3.1)

3. **Visualización y Analytics**
   - Dashboard con KPIs de optimización, adopción e impacto
   - Mapa geográfico interactivo mostrando stock, oportunidades de matching y rutas
   - Visualización completa del ciclo de vida de contenedores
   - Reportes de ahorro económico y reducción de emisiones CO2

4. **Sistema de Feedback y Aprendizaje**
   - Captura de aceptación/rechazo de recomendaciones con motivos
   - Métricas de adopción del sistema por operadores
   - Base para mejora continua del algoritmo

### Stack Tecnológico

**Cloud-native en Google Cloud Platform:**
- **Frontend:** Vite + React + TypeScript (Firebase Hosting)
- **Backend:** Node.js Cloud Functions + Cloud Firestore (UI parametric data)
- **Motor de Optimización:** Java + Timefold en Cloud Run
- **LLM:** Google Gemini (Vertex AI) para procesamiento de PDFs
- **Base de Datos:** PostgreSQL (Firebase Data Connect) para datos transaccionales
- **Ingesta:** Cloud Pub/Sub + Cloud Functions (sujeto a configuración de inbox de Rhenus)
- **Arquitectura serverless-first** para minimizar overhead operativo y costes

### Cronograma y Metodología

**Duración total:** 5-6 meses (21-23 semanas)

| Fase | Duración | Entregable Principal |
|------|----------|---------------------|
| **Fase 0: Descubrimiento** | 2-3 semanas | Especificación funcional y diseños aprobados |
| **Fase 1: Infraestructura** | 4 semanas | Infraestructura cloud + Datos maestros operativos |
| **Fase 2: Ingesta LLM** | 4 semanas | Procesamiento automático de PDFs funcional |
| **Fase 3: Optimización** | 5-6 semanas | Motor Timefold + Recomendaciones generadas |
| **Fase 4: Analytics** | 6 semanas | Dashboards + Sistema completo refinado y testeado |

**Metodología ágil:** Sprints de 2 semanas, entregas incrementales, demos al final de cada fase, feedback continuo con Rhenus.

### Equipo de Desarrollo

**Team core:** ~8-9 personas FTE
- Arquitecto/Tech Lead + 2 Frontend + 2 Backend (Node.js) + 1 Java (Timefold) + DevOps/SRE + ML Engineer + QA + Product Owner + UI/UX Designer
- Perfiles senior y mid con experiencia en GCP, optimización algorítmica, React, LLMs

### Presupuesto del MVP

| Componente | Coste Estimado |
|------------|----------------|
| **Personal de Desarrollo** | €443,913 |
| **Consultores (Timefold, Security, Tech Writer)** | €9,500 - €15,000 |
| **Infraestructura Cloud (6 meses desarrollo)** | €1,140 - €3,360 |
| **Herramientas y Licencias** | €3,150 |
| **Otros (viajes, contingencia)** | €8,500 - €12,000 |
| **TOTAL MVP** | **€466,203 - €477,423** |

**Modelo de facturación recomendado:** Híbrido
- Fase 0 (Discovery) a precio fijo: €47,000
- Fases 1-4 en Time & Materials con techo de €430,000
- Revisión mensual de gastos vs. presupuesto

### Retorno de Inversión (ROI) Esperado

**Escenario conservador para zona norte España:**
- Supuesto: 5,000 contenedores/año, 40% imports, 30% tasa de matching
- **Ahorro anual estimado:** €270,000/año (1,200 viajes evitados × €225/viaje)
- **Costes operación año 1:** ~€100,000 (infraestructura + soporte)
- **Ahorro neto año 1:** €170,000
- **Payback period:** ~1.5 años

**Beneficios adicionales:**
- Reducción de emisiones CO2 (contribución a objetivos ESG)
- Mejor utilización de flota de contenedores (reducir inactividad del 50%)
- Visibilidad completa de stock y operaciones
- Mejora en planificación operativa
- Capacidad de expansión a otras regiones tras validación del MVP

### Riesgos Principales y Mitigaciones

**Riesgos críticos identificados:**
1. **Precisión del LLM en PDFs:** Mitigación mediante testing temprano, validación anti-alucinaciones, human-in-the-loop para casos de baja confianza
2. **Integración con inbox de email:** Coordinación temprana con IT de Rhenus, alternativas (IMAP, upload manual) si necesario
3. **Adopción por operadores:** Involucrar usuarios desde Discovery, UX intuitivo, demostrar valor en beta privada
4. **Complejidad operativa real:** Discovery exhaustivo en Fase 0, enfoque iterativo, priorizar casos comunes (80/20)

Enfoque proactivo de gestión de riesgos con revisión semanal, escalación clara y planes de contingencia para todos los riesgos identificados.

### Valor Diferencial de Esta Propuesta

1. **Enfoque de apoyo a la decisión:** El MVP proporciona recomendaciones inteligentes pero mantiene control humano, minimizando riesgos operativos y generando confianza
2. **Stack moderno y coste-efectivo:** Arquitectura serverless en GCP minimiza overhead operativo y costes de infraestructura
3. **IA aplicada con validación:** Uso de LLM multimodal (Gemini) para automatización de ingesta con robustas validaciones anti-alucinaciones
4. **Optimización algorítmica avanzada:** Motor Timefold (evolución de OptaPlanner) para constraint-based optimization de clase mundial
5. **Visibilidad y analytics:** No solo optimización, sino también comprensión profunda del negocio mediante dashboards y métricas
6. **Escalable post-MVP:** Arquitectura preparada para expansión a otras zonas geográficas y modos de transporte
7. **ROI demostrable:** Ahorro estimado de €270K/año con payback de ~1.5 años, sin contar beneficios intangibles (ESG, eficiencia operativa)

### Próximos Pasos

1. **Revisión y validación** de esta oferta técnica con stakeholders de Rhenus
2. **Kick-off del proyecto** y arranque de Fase 0 (Discovery)
3. **Discovery workshops** con operadores y áreas de negocio de Rhenus
4. **Validación de supuestos** técnicos y de negocio durante primeras 2-3 semanas
5. **Inicio de desarrollo** (Fase 1) tras aprobación de especificación funcional detallada

Estamos preparados para iniciar el proyecto tan pronto como Rhenus esté listo, con un equipo experimentado en proyectos de logística, optimización y cloud-native development.

---

## 3. Objetivos del Proyecto

### 3.1. Contexto del Problema

El reposicionamiento de contenedores vacíos representa uno de los mayores desafíos en la industria logística:
- **Coste global:** Aproximadamente $20 billones anuales para la industria del transporte de contenedores
- **Ineficiencia:** ~33% de los contenedores en circulación están vacíos
- **Tiempo inactivo:** El contenedor promedio pasa casi el 50% de su vida útil inactivo
- **Origen:** Desequilibrio en el comercio exterior (mercados orientados a importación vs exportación)

#### Flujos Operativos de Contenedores en Rhenus

**Nota:** Los flujos descritos a continuación están sujetos a confirmación con el cliente durante la fase de descubrimiento.

**Flujo IMPORT tradicional (Contenedor lleno → Cliente → Devolución vacío):**
1. Contenedor **LLENO** llega a terminal marítima de Barcelona
2. Se recibe orden de import en PDF
3. TRUCK recoge contenedor lleno en Barcelona
4. TRUCK transporta contenedor a ubicación del cliente
5. Cliente descarga mercancía (contenedor queda **VACÍO**)
6. TRUCK devuelve contenedor vacío a terminal (puede ser Barcelona o terminal ferroviaria: Noain, Agoncillo, Miranda)

**Flujo EXPORT (Contenedor vacío → Cliente → Puerto):**
1. Se recibe orden de export en PDF
2. TRUCK recoge contenedor **VACÍO** de una terminal (Barcelona o terminales ferroviarias: Noain, Agoncillo, Miranda)
3. TRUCK transporta contenedor vacío a ubicación del cliente
4. Cliente carga mercancía (contenedor queda **LLENO**)
5. TRUCK transporta contenedor lleno a terminal marítima de Barcelona
6. Contenedor se entrega en Barcelona para su envío marítimo

**Ciclo de Distribución de Contenedores vía TREN:**
1. Contenedores llegan a Barcelona vía marítima (import o contenedores vacíos de retorno)
2. Contenedores se envían mediante **TREN** desde Barcelona a terminales ferroviarias (Noain, Agoncillo, Miranda)
3. Se recibe PDF con información de contenedores que llegan a terminales ferroviarias
4. Actualización de stock según estado:
   - **Contenedores VACÍOS:** Disponibles para nuevas órdenes de export
   - **Contenedores LLENOS:** Pendientes de entrega a clientes en la zona (import)

#### El Problema de Ineficiencia Actual y el Valor del Reposicionamiento Inteligente

**Situación SIN optimización (flujo tradicional separado):**

*Para una operación IMPORT + EXPORT de clientes cercanos:*

**Import (Cliente A):**
1. Barcelona → Cliente A con contenedor **lleno** (TRUCK)
2. Cliente A descarga
3. **Cliente A → Terminal con contenedor VACÍO** (TRUCK - viaje de devolución a Barcelona o terminal ferroviaria)

**Export (Cliente B cercano al Cliente A):**
4. **Terminal → Cliente B con contenedor VACÍO** (TRUCK - viaje de recogida desde Barcelona o terminal ferroviaria)
5. Cliente B carga
6. Cliente B → Barcelona con contenedor **lleno** (TRUCK)

**Total: 6 viajes**, de los cuales:
- 2 viajes útiles con carga (1 lleno import, 1 lleno export)
- **4 viajes con contenedores vacíos o retornos**
- **2 viajes completamente EVITABLES** (devolución vacío + recogida vacío)

---

**Situación CON optimización (matching import-export):**

*Misma operación IMPORT + EXPORT con matching inteligente:*

**Import + Export optimizado:**
1. Barcelona → Cliente A con contenedor **lleno** (TRUCK)
2. Cliente A descarga (contenedor queda vacío)
3. **Cliente A → Cliente B con contenedor VACÍO** (TRUCK - reposicionamiento directo)
4. Cliente B carga
5. Cliente B → Barcelona con contenedor **lleno** (TRUCK)

**Total: 5 viajes**, de los cuales:
- 2 viajes útiles con carga (1 lleno import, 1 lleno export)
- **3 viajes necesarios** (solo 1 vacío entre clientes cercanos)

---

**VALOR DEL REPOSICIONAMIENTO INTELIGENTE:**
- **1 viaje ELIMINADO** (33% menos viajes que con matching vs sin matching para este ejemplo)
- **Se elimina:** Viaje vacío Cliente A → Terminal + Viaje vacío Terminal → Cliente B
- **Se añade:** Solo 1 viaje vacío Cliente A → Cliente B (distancia mucho menor)
- **Ahorro real:** Kilómetros, combustible, tiempo, coste operativo, emisiones CO2
- **Mejora utilización:** Contenedor pasa menos tiempo inactivo en terminal

Rhenus Logistics actualmente dispone de un sistema TMS que no cubre adecuadamente esta optimización del uso de contenedores vacíos, generando:
- Costes innecesarios de reposicionamiento de contenedores vacíos
- Retornos a terminal de contenedores que podrían reutilizarse directamente
- Falta de visibilidad sobre oportunidades de matching import-export
- Emisiones evitables de CO2 por transporte de contenedores vacíos

### 3.2. Objetivos Principales

El proyecto tiene como objetivo desarrollar un **MVP (Minimum Viable Product)** de un sistema TMS avanzado con capacidades de IA que permita:

#### 3.2.1. Reducción de Costes Operativos
- Minimizar transportes de contenedores vacíos mediante matching inteligente
- Reducir retornos innecesarios a terminal
- Optimizar el uso de la flota de contenedores disponible

#### 3.2.2. Maximización de Utilización de Contenedores
- Aumentar el tiempo activo de los contenedores (reducir inactividad del 50% actual)
- Conectar directamente contenedores de importación con necesidades de exportación
- Mejorar la rotación y disponibilidad del stock de contenedores

#### 3.2.3. Sostenibilidad Ambiental
- Reducir emisiones de CO2 mediante optimización de rutas
- Minimizar kilómetros en vacío
- Contribuir a objetivos de sostenibilidad corporativa

#### 3.2.4. Optimización Multimodal
- Planificación inteligente de rutas considerando dos modos de transporte:
  - **TRAIN (ferroviario):** Para trayectos entre Barcelona y terminales ferroviarias (Noain, Agoncillo, Miranda)
  - **TRUCK (carretera):** Para primeros/últimos tramos y trayectos completos
- Optimización multiobjetivo: coste, tiempo, emisiones y disponibilidad
- Coordinación eficiente entre ambos medios de transporte

### 3.3. Capacidades Clave del Sistema

El sistema deberá incorporar las siguientes capacidades de optimización e inteligencia artificial:

1. **Matching Inteligente Import-Export**
   - Identificar automáticamente oportunidades de reutilización directa de contenedores:
     - Contenedor de **import** que queda vacío en ubicación del cliente
     - Orden de **export** de un cliente cercano que necesita contenedor vacío
     - Evitar retorno del contenedor vacío a terminal
     - Evitar viaje de recogida de contenedor vacío desde terminal
   - Considerar proximidad geográfica entre clientes
   - Analizar compatibilidad de tipos de contenedores y requisitos
   - Evaluar ventanas temporales de disponibilidad

2. **Predicción de Demanda**
   - Anticipar necesidades futuras de contenedores por ruta, cliente y tipo
   - Facilitar planificación proactiva del stock de contenedores

3. **Optimización de Rutas Multiobjetivo**
   - Algoritmos que consideren simultáneamente: coste, tiempo de tránsito, emisiones de CO2 y disponibilidad de recursos
   - Soporte para rutas multimodales (combinación de TRAIN y TRUCK)
   - Consideración de restricciones geográficas (terminales: Barcelona, Noain, Agoncillo, Miranda)

4. **Alertas y Recomendaciones Proactivas**
   - Notificaciones automáticas de oportunidades de optimización
   - Sugerencias inteligentes para mejorar eficiencia operativa

### 3.4. Alcance del MVP

- **Geográfico:** Operaciones de Rhenus Logistics en la zona norte de España:
  - **Bilbao:** Centro de gestión de órdenes
  - **Barcelona:** Puerto marítimo
  - **Depots/Estaciones ferroviarias:** Noain, Agoncillo y Miranda
- **Modos de transporte:** TRAIN (ferroviario) y TRUCK (carretera)
- **Integración inicial:** Sistema de ingesta vía inbox de correo electrónico para procesar PDFs:
  - PDFs con órdenes de import/export
  - PDFs con información de llegadas de contenedores (vacíos o llenos) vía tren a terminales ferroviarias (para gestión de stock en depots)
- **Datos:** Stock de contenedores y datos maestros precargados en el sistema para validación inicial
- **Enfoque:** Desarrollo iterativo para validar el concepto antes de escalar a otras zonas geográficas y modos de transporte

### 3.5. Modelo de Operación del MVP

**Sistema de Recomendaciones para Operadores**

El MVP funcionará como un **sistema de apoyo a la decisión** que proporciona sugerencias inteligentes a los operadores de Rhenus, manteniendo el control humano en la toma de decisiones:

- **Sugerencias, no automatización:** El sistema analizará las órdenes de import/export y generará recomendaciones sobre movimientos óptimos de contenedores, pero serán los operadores quienes decidan ejecutarlas o no
- **Sin integración con sistemas de ejecución:** El MVP **NO se integrará** con ningún sistema externo que genere automáticamente órdenes de transporte
- **Flujo manual validado:** Los operadores revisarán las sugerencias del sistema y, si las aprueban, procederán a generar las órdenes de transporte a través de sus procesos actuales
- **Aprendizaje iterativo:** El feedback de los operadores sobre las sugerencias aceptadas/rechazadas servirá para mejorar el modelo en futuras iteraciones

Este enfoque permite:
1. Validar la precisión y utilidad de las recomendaciones antes de cualquier automatización
2. Mantener el conocimiento y experiencia de los operadores en el proceso
3. Minimizar riesgos operativos durante la fase de prueba
4. Generar confianza en el sistema antes de escalar

### 3.6. Capacidades de Análisis y Visualización

El MVP incorporará funcionalidades de análisis y visualización que permitan tanto a operadores como a la dirección de negocio evaluar el estado actual y la efectividad del sistema:

#### 3.6.1. Visualización de Stock de Contenedores

El sistema proporcionará visibilidad completa del ciclo de vida de contenedores:

- **Contenedores en terminales:**
  - Stock de contenedores en:
    - **Terminales ferroviarias:** Noain, Agoncillo y Miranda (actualizados con PDFs de llegadas de tren)
      - Contenedores **VACÍOS**: Disponibles para órdenes de export
      - Contenedores **LLENOS**: Pendientes de entrega a clientes (import)
    - **Barcelona:** Terminal marítima
      - Contenedores vacíos devueltos de operaciones import
      - Contenedores llenos de importación marítima
  - Disponibles para ser asignados según estado y operación

- **Contenedores en tránsito (en rutas activas):**
  - **Import en curso:** Contenedores llenos en ruta desde Barcelona hacia clientes
  - **Export en curso:** Contenedores en ruta desde terminales/clientes hacia Barcelona

- **Contenedores post-import (vacíos en ubicaciones de clientes):**
  - Contenedores que han completado entregas de import y están vacíos en ubicación del cliente
  - **Candidatos para matching:** Disponibles para ser reutilizados en órdenes de export cercanas
  - Visualización de tiempo desde que quedaron vacíos
  - Proximidad a órdenes de export pendientes

- **Distribución geográfica:** Mapa de la zona norte mostrando:
  - Terminales ferroviarias con stock de vacíos (Noain, Agoncillo, Miranda)
  - Barcelona (terminal marítima)
  - Ubicaciones de clientes con contenedores vacíos post-import
  - Ubicaciones de clientes con órdenes de export pendientes
  - Oportunidades de matching visualizadas geográficamente
  - Centro de gestión en Bilbao (sin stock físico de contenedores)

- **Estados y tipos:** Clasificación por:
  - Tipo de contenedor (22G1=20'DV, 42G1=40'DV, 45G1=40'HC)
  - Estado (vacío en terminal, vacío en cliente, lleno en tránsito, etc.)
  - Disponibilidad y restricciones

#### 3.6.2. Métricas de Efectividad del Sistema
El sistema proporcionará indicadores clave (KPIs) para que el negocio pueda evaluar el retorno de la inversión:

- **Métricas de optimización:**
  - **% de matching import-export exitoso:** Porcentaje de contenedores de import reutilizados directamente para export (sin retorno a terminal)
  - **Viajes evitados:** Número de viajes de retorno a terminal y recogidas desde terminal eliminados
  - **Reducción de kilómetros:** Kilómetros totales ahorrados por matching directo vs. ruta tradicional
  - **Reducción de kilómetros en vacío:** Kilómetros específicamente evitados de transporte de contenedores vacíos
  - **Tiempo de inactividad:** Tiempo promedio que un contenedor permanece inactivo entre operaciones
  - **Tasa de utilización:** Porcentaje de tiempo que contenedores están en uso activo vs. inactivos

- **Métricas de adopción:**
  - % de sugerencias aceptadas vs. rechazadas por operadores
  - Tiempo medio de respuesta a las recomendaciones
  - Motivos de rechazo de sugerencias (para mejora continua)

- **Métricas de impacto económico y ambiental:**
  - Ahorro estimado en costes de reposicionamiento
  - Reducción estimada de emisiones de CO2
  - ROI proyectado del sistema

#### 3.6.3. Dashboard Analítico
Interface visual que consolide toda la información relevante para la toma de decisiones y evaluación del sistema.

### 3.7. Supuestos e Incógnitas del Proyecto

Es importante reconocer que existen aspectos del proceso actual de Rhenus que aún deben ser definidos y que se resolverán durante la ejecución del proyecto:

#### Incógnitas a Resolver
- **Procedimiento actual de asignación:** Cómo gestiona actualmente Rhenus la asignación de contenedores a rutas (criterios, responsables, herramientas utilizadas)
- **Reglas de negocio específicas:** Restricciones, prioridades de clientes, acuerdos comerciales que puedan afectar la asignación de contenedores
- **Fuentes de datos existentes:** Qué datos están disponibles actualmente, en qué formato, y con qué nivel de calidad
- **Procesos de coordinación:** Cómo se coordinan actualmente las diferentes delegaciones y modos de transporte

#### Enfoque de Resolución
Estas incógnitas se abordarán mediante:
1. **Fase de descubrimiento inicial:** Sesiones de trabajo con operadores y responsables de Rhenus para mapear procesos actuales
2. **Desarrollo iterativo:** El MVP se irá ajustando según el conocimiento adquirido durante el proyecto
3. **Colaboración continua:** Comunicación frecuente con el equipo de Rhenus para validar supuestos y ajustar la solución

---

## 4. Alcance de la Solución

### 4.1. Visión General del Sistema

El MVP consistirá en una **plataforma web de apoyo a la decisión** que permita a los operadores de Rhenus Logistics optimizar el uso de contenedores mediante recomendaciones inteligentes basadas en IA. El sistema incluirá capacidades de análisis, visualización y gestión de datos maestros.

### 4.2. Componentes Principales

El sistema estará compuesto por los siguientes módulos:

1. **Motor de Ingesta de Datos**
   - Monitorización automática de inbox de correo electrónico
   - Extracción automática de datos de PDFs mediante **LLMs multimodales**:
     - Análisis visual de documentos PDF
     - Extracción y estructuración de datos en formato estándar (JSON)
     - Procesamiento de órdenes de import/export
     - Procesamiento de llegadas de contenedores (vacíos o llenos) vía tren a terminales ferroviarias (Noain, Agoncillo, Miranda)
   - Procesamiento en tiempo real o near-real-time
   - Sistema de validación para detección de inconsistencias y alucinaciones del modelo
   - Alertas en caso de errores o baja confianza en la extracción
   - Actualización automática de stock en depots con base en información de llegadas validada (diferenciando entre contenedores vacíos y llenos)

2. **Motor de Optimización y Recomendaciones**
   - Algoritmos de matching inteligente import-export
   - Optimización multiobjetivo (coste, tiempo, emisiones CO2, disponibilidad)
   - Predicción de demanda futura de contenedores
   - Cálculo de rutas multimodales óptimas (TRAIN + TRUCK)
   - Generación de nivel de confianza para cada recomendación

3. **Interface de Usuario Web Responsive**
   - Accesible desde navegadores en desktop y tablets
   - Gestión de recomendaciones (revisión, aceptación/rechazo)
   - Visualización de órdenes activas y planificadas
   - Gestión de datos maestros

4. **Dashboard Analítico**
   - Visualización de KPIs en tiempo real
   - Reportes de efectividad del sistema
   - Análisis de tendencias y patrones

5. **Módulo de Gestión de Datos Maestros**
   - Administración de contenedores, depots, rutas, clientes, navieras
   - Configuración de parámetros de optimización
   - Gestión de usuarios y permisos

### 4.3. Perfiles de Usuario

El sistema contemplará diferentes niveles de acceso y funcionalidades según el rol del usuario:

**Nota:** Los perfiles específicos de usuario se definirán con mayor detalle durante la fase de descubrimiento del proyecto.

1. **Usuarios con Capacidad de Decisión**
   - Visualización de recomendaciones de optimización
   - Aceptación/rechazo de sugerencias con justificación
   - Consulta de estado de contenedores y rutas
   - Generación de órdenes de transporte (fuera del sistema, en sus procesos actuales)

2. **Usuarios de Visualización (Solo Lectura)**
   - Consulta de estado de contenedores
   - Visualización de rutas planificadas y en curso
   - Acceso a reportes y dashboards

3. **Administradores del Sistema**
   - Configuración del inbox de correo
   - Ajuste de pesos y criterios de optimización
   - Gestión de datos maestros (contenedores, depots, navieras, clientes, rutas, tarifas)
   - Administración de usuarios y permisos
   - Configuración de parámetros del sistema

### 4.4. Funcionalidades Core

#### 4.4.1. Procesamiento Automático de Datos

El sistema procesará dos tipos de PDFs recibidos en el inbox utilizando **LLMs multimodales** para la extracción de información:

**Tecnología de Extracción:**
- **LLMs multimodales:** Modelos de lenguaje con capacidad de análisis visual de documentos
- **Análisis visual:** Lectura e interpretación del contenido del PDF sin necesidad de OCR tradicional
- **Estructuración en JSON:** Extracción de datos y conversión automática a formato estándar JSON
- **Validación anti-alucinaciones:** Sistema de validación para detectar:
  - Inconsistencias en los datos extraídos
  - Posibles alucinaciones del modelo LLM
  - Campos extraídos con baja confianza
  - Valores fuera de rangos esperados

**A) PDFs de Órdenes Import/Export**

El sistema procesará dos tipos de órdenes con diferentes flujos:

**Órdenes de IMPORT (Contenedor lleno → Cliente → Devolución vacío):**
- **Extracción de datos mediante LLM multimodal:**
  - Cliente (destinatario de la mercancía)
  - Ubicación del cliente (destino de entrega)
  - Tipo y cantidad de contenedores (22G1, 42G1, 45G1)
  - Fecha/hora de recogida en Barcelona (terminal marítima)
  - Fecha/hora estimada de entrega en cliente
  - Requisitos especiales del contenedor o mercancía
  - Naviera propietaria del contenedor (Maersk, Hapag-Lloyd, MSC, etc.)
  - Terminal de devolución preferida (Barcelona, Noain, Agoncillo o Miranda)
- **Flujo tradicional:** Barcelona (lleno) → TRUCK → Cliente (descarga, vacío) → TRUCK → Terminal (Barcelona o ferroviaria)
- **Flujo optimizado (con matching):** Barcelona (lleno) → TRUCK → Cliente A (descarga, vacío) → TRUCK → Cliente B export (evita devolución a terminal)
- **Estado relevante para matching:** Contenedor vacío disponible en ubicación del cliente después de descarga

**Órdenes de EXPORT (Cliente → Contenedor lleno → Barcelona):**
- **Extracción de datos mediante LLM multimodal:**
  - Cliente (origen de la mercancía)
  - Ubicación del cliente (recogida de contenedor vacío)
  - Tipo y cantidad de contenedores requeridos
  - Fecha/hora de recogida en cliente
  - Fecha/hora límite de entrega en Barcelona
  - Requisitos especiales del contenedor o mercancía
  - Naviera de destino
  - Terminal de recogida preferida para contenedor vacío (Barcelona, Noain, Agoncillo o Miranda)
- **Flujo tradicional:** Terminal (Barcelona o ferroviaria) → TRUCK → Cliente (carga, lleno) → TRUCK → Barcelona
- **Flujo optimizado (con matching):** Usar contenedor vacío de import cercano en lugar de recoger de terminal

**Salida común:**
- Datos estructurados en formato JSON
- **Validación:** Detección de inconsistencias y alucinaciones
- **Notificaciones:** Alertas a usuarios cuando se requiere intervención manual o validación humana

**B) PDFs de Llegadas de Contenedores Ferroviarios**

Estos PDFs contienen información sobre contenedores (tanto **VACÍOS** como **LLENOS**) que llegan mediante TREN desde Barcelona a las terminales ferroviarias.

**Contexto de los flujos:**

*Contenedores VACÍOS:*
1. Contenedores export enviados por mar desde Barcelona
2. Contenedores vacíos regresan a Barcelona (gestionados por navieras)
3. Se envían con TREN desde Barcelona a terminales ferroviarias (Noain/Agoncillo/Miranda)
4. PDF informa de la llegada de contenedores vacíos
5. Quedan disponibles para nuevas órdenes de export

*Contenedores LLENOS:*
1. Contenedores llenos llegan a Barcelona vía marítima (importación)
2. Se envían con TREN desde Barcelona a terminales ferroviarias (Noain/Agoncillo/Miranda)
3. PDF informa de la llegada de contenedores llenos
4. Disponibles para entrega a clientes en la zona

**Extracción de datos mediante LLM multimodal:**
- Terminal ferroviaria de destino (Noain, Agoncillo o Miranda)
- Identificación de contenedores
- Tipo y características de contenedores (22G1, 42G1, 45G1)
- Fecha y hora de llegada
- **Estado del contenedor (VACÍO o LLENO)**
- Naviera propietaria
- Si está lleno: cliente destinatario o referencia de orden de import

**Procesamiento:**
- **Salida:** Datos estructurados en formato JSON
- **Validación:** Verificación de consistencia de datos extraídos
- **Actualización de stock:** Actualización automática del inventario en el depot correspondiente según estado:
  - Contenedores VACÍOS: Disponibles para órdenes de export
  - Contenedores LLENOS: Pendientes de entrega a clientes
- **Notificaciones:** Alertas sobre nuevas llegadas y disponibilidad de contenedores

#### 4.4.2. Motor de Recomendaciones de Optimización

El sistema generará recomendaciones inteligentes de matching import-export para optimizar el uso de contenedores vacíos.

**Tipos de Recomendaciones:**

**1. Matching Directo Import → Export (Optimización principal):**
- **Situación detectada:**
  - Orden de IMPORT: Contenedor lleno entregado al Cliente A, después de descarga quedará vacío
  - Orden de EXPORT: Cliente B en ubicación cercana al Cliente A necesita contenedor vacío
- **Recomendación:**
  - Usar el contenedor vacío del import del Cliente A directamente para el export del Cliente B
  - Evitar devolución del vacío a terminal (Barcelona o terminal ferroviaria)
  - Evitar recogida de vacío desde terminal (Barcelona o terminal ferroviaria)

- **Comparación de rutas:**
  - **SIN optimización (tradicional):**
    1. Barcelona → Cliente A (lleno) - Import
    2. Cliente A → Terminal (vacío) - Devolución
    3. Terminal → Cliente B (vacío) - Recogida export
    4. Cliente B → Barcelona (lleno) - Export
    - **Total:** 4 viajes

  - **CON optimización (matching):**
    1. Barcelona → Cliente A (lleno) - Import
    2. Cliente A → Cliente B (vacío) - Reposicionamiento directo
    3. Cliente B → Barcelona (lleno) - Export
    - **Total:** 3 viajes

  - **Ahorro:** 1 viaje eliminado (25% reducción)
  - **Detalle:** Se eliminan los viajes Cliente A → Terminal + Terminal → Cliente B
  - **Se añade:** Solo el viaje directo Cliente A → Cliente B (típicamente distancia mucho menor)

**2. Recogida de Contenedor Vacío Optimizada:**
- Cuando no hay matching directo import-export disponible
- Seleccionar la terminal óptima para recoger contenedor vacío:
  - Barcelona (terminal marítima)
  - Noain, Agoncillo o Miranda (terminales ferroviarias)
- Considerar proximidad al cliente export, disponibilidad de stock en cada terminal, y costes de transporte

**Información incluida en cada recomendación:**

- **Matching específico:**
  - ID de orden de import (contenedor que quedará vacío)
  - ID de orden de export (que necesita contenedor vacío)
  - Ubicaciones de clientes y distancia entre ellos
  - Compatibilidad de tipos de contenedores

- **Ruta propuesta detallada:**
  - Secuencia de movimientos paso a paso
  - Modo de transporte en cada tramo (**TRUCK**)
  - Puntos de origen, intermedios y destino
  - Tiempos estimados por tramo

- **Impacto estimado vs. ruta tradicional:**
  - Ahorro económico (coste de transporte evitado)
  - Kilómetros evitados
  - Reducción de emisiones de CO2
  - Tiempo total de operación
  - Número de viajes/tramos eliminados

- **Nivel de confianza:**
  - Score (0-100%) que indica la fiabilidad de la recomendación
  - Factores considerados: proximidad geográfica, compatibilidad de contenedores, ventanas temporales, restricciones

**Estrategia de generación de recomendaciones:**

El sistema podrá operar en tiempo real al recibir nuevas órdenes, generando sugerencias inmediatamente.

**Incógnita a resolver durante el proyecto:** La estrategia de replanificación ante nuevas órdenes, modificaciones o cancelaciones aún debe definirse con Rhenus:
- ¿Replanificar todas las órdenes pendientes o solo la nueva?
- ¿Cómo gestionar recomendaciones ya aceptadas pero no ejecutadas cuando llega nueva información?
- ¿Qué ventana temporal considerar para replanificación?

#### 4.4.3. Gestión de Feedback de Recomendaciones

- **Aceptación/Rechazo:** Interface para que usuarios indiquen si aceptan o rechazan cada sugerencia
- **Motivos de rechazo:** Captura de razones para retroalimentar el modelo
- **Tracking de ejecución:** Registro de qué recomendaciones aceptadas fueron realmente ejecutadas
- **Aprendizaje continuo:** Uso del feedback para mejorar futuras recomendaciones

#### 4.4.4. Visualización de Stock y Estado de Contenedores

El sistema proporcionará múltiples vistas para entender el estado completo del inventario de contenedores:

**Vista por Estados del Ciclo de Vida:**

1. **Contenedores en Terminales:**
   - **Terminales ferroviarias:** Noain, Agoncillo, Miranda
     - Stock actualizado automáticamente con PDFs de llegadas de tren
     - **VACÍOS:** Disponibles para órdenes de export
     - **LLENOS:** Pendientes de entrega a clientes (import)
   - **Barcelona:** Terminal marítima
     - Contenedores vacíos devueltos de operaciones import
     - Contenedores llenos de importación marítima
   - Cantidad por tipo de contenedor (22G1, 42G1, 45G1) y estado en cada ubicación
   - Tiempo de permanencia en terminal

2. **Contenedores Post-Import (Vacíos en ubicaciones de clientes):**
   - **Vista crítica para matching:** Contenedores que completaron entregas de import
   - Ubicación del cliente donde quedaron vacíos
   - Tiempo transcurrido desde que quedaron vacíos
   - Indicador de proximidad a órdenes de export pendientes
   - Destacado visual de oportunidades de matching

3. **Contenedores en Tránsito:**
   - **Import activo:** Llenos desde Barcelona hacia clientes
   - **Export activo:** Desde ubicación origen (terminal o cliente) hacia Barcelona
   - Modo de transporte actual (TRUCK)
   - Progreso estimado de la ruta

**Mapa Geográfico Interactivo:**
- **Terminales con stock de vacíos:**
  - Terminales ferroviarias (Noain, Agoncillo, Miranda) con nivel de stock
  - Barcelona (terminal marítima) con nivel de stock de vacíos devueltos
- Clientes con contenedores vacíos post-import (pins en mapa)
- Clientes con órdenes de export pendientes (pins en mapa)
- **Visualización de oportunidades:** Líneas conectando contenedores vacíos en clientes con órdenes de export cercanas
- Rutas activas en tiempo real

**Filtros y Búsquedas:**
- Por tipo de contenedor (22G1=20'DV, 42G1=40'DV, 45G1=40'HC)
- Por ubicación (Barcelona, Noain, Agoncillo, Miranda, ubicaciones de clientes)
- Por estado (vacío en terminal, vacío en cliente, lleno en tránsito, etc.)
- Por disponibilidad temporal
- Por propietario/naviera
- Por edad (tiempo desde última operación)

#### 4.4.5. Dashboard y Métricas

Paneles visuales con los KPIs definidos en la sección 3.6.2:
- Métricas de optimización
- Métricas de adopción del sistema
- Métricas de impacto económico y ambiental
- Gráficos de tendencias temporales
- Comparativas antes/después de usar el sistema

### 4.5. Gestión de Datos Maestros

El sistema permitirá administrar la siguiente información:

**Nota:** Durante el proyecto se definirá qué datos son verdaderamente maestros (editables) y cuáles son paramétricos de solo lectura.

1. **Contenedores**
   - Inventario completo
   - **Tipos de contenedores (códigos ISO):**
     - **22G1:** 20'DV (20 pies Dry Van)
     - **42G1:** 40'DV (40 pies Dry Van)
     - **45G1:** 40'HC (40 pies High Cube)
   - Capacidades y características por tipo
   - Naviera dueña de cada contenedor (campo crítico para todas las operaciones)
   - Estado actual:
     - Vacío en terminal (Barcelona o ferroviarias: Noain/Agoncillo/Miranda) - disponible para export
     - Vacío en ubicación de cliente post-import (candidato para matching)
     - Lleno en tránsito import (Barcelona → Cliente)
     - En tránsito export (Cliente/Terminal → Barcelona)
     - En tránsito devolución (Cliente → Terminal con vacío)
     - En mantenimiento
   - Ubicación actual (terminal o cliente)
   - Historial de operaciones (última import/export)

2. **Depots/Terminales**
   - **Barcelona:** Terminal marítima (puerto)
     - Recepción de contenedores llenos de importación
     - Almacenamiento de contenedores vacíos devueltos de operaciones import
     - Envío de contenedores llenos de exportación
   - **Noain, Agoncillo, Miranda:** Terminales ferroviarias
     - Recepción de contenedores vía TREN desde Barcelona (vacíos o llenos)
     - Almacenamiento de contenedores vacíos disponibles para export
     - Almacenamiento de contenedores llenos pendientes de entrega a clientes (import)
   - Capacidades de almacenamiento por ubicación
   - Tipos de contenedores soportados en cada terminal
   - Costes de almacenamiento
   - Operadores y horarios de operación

3. **Clientes**
   - Información de clientes (nombre, identificación)
   - **Ubicaciones geográficas** (crítico para cálculo de proximidad y matching)
   - Coordenadas GPS o dirección completa
   - Tipos de contenedores que manejan habitualmente
   - Restricciones o requisitos especiales
   - Historial de operaciones import/export

4. **Rutas y Tarifas**
   - Costes de transporte TRUCK:
     - Entre terminales (Barcelona ↔ Noain/Agoncillo/Miranda)
     - Entre terminales y ubicaciones de clientes
     - Entre ubicaciones de clientes (para matching import-export)
   - Tiempos estimados de tránsito por modo:
     - **TRAIN:** Rutas ferroviarias entre Barcelona y terminales ferroviarias
     - **TRUCK:** Rutas por carretera (terminales, clientes)
   - Restricciones de capacidad por modo de transporte
   - Frecuencias de servicio ferroviario
   - Matriz de distancias para cálculo de proximidad

5. **Navieras**
   - Las navieras son las **ÚNICAS propietarias** de los contenedores
   - Principales navieras: Maersk, Hapag-Lloyd, Mediterranean Shipping Company, etc.
   - Acuerdos comerciales con Rhenus
   - Condiciones de uso de contenedores
   - Políticas de reposicionamiento de cada naviera
   - Restricciones específicas por naviera
   - Tarifas por uso de contenedores
   - Tiempos de free time (tiempo gratuito de uso)

6. **Parámetros de Optimización**
   - Pesos para los diferentes criterios (coste, tiempo, CO2)
   - **Radio máximo de matching:** Distancia máxima entre cliente import y cliente export para considerar matching directo
   - **Ventana temporal de matching:** Tiempo máximo entre disponibilidad de contenedor vacío y necesidad de export
   - Restricciones de negocio
   - Umbrales de alertas
   - Configuración del motor de IA

### 4.6. Aspectos Técnicos Clave

- **Arquitectura:** Cloud-native, escalable y modular
- **Disponibilidad:** Alta disponibilidad durante horario laboral
- **Rendimiento:** Procesamiento de órdenes en near-real-time (< 5 minutos desde recepción)
- **Seguridad:** Autenticación, autorización basada en roles, cifrado de datos sensibles
- **Trazabilidad:** Auditoría completa de acciones de usuarios y decisiones del sistema

### 4.7. Funcionalidades Fuera de Alcance del MVP

Para mantener el foco en la validación del concepto, las siguientes funcionalidades quedan **explícitamente fuera del alcance** de este MVP:

- Integración automática con sistemas externos (ERP, TMS existente, sistemas de navieras)
- Generación automática de órdenes de transporte
- Aplicación móvil nativa
- Tracking GPS en tiempo real de contenedores
- Integración con IoT/sensores
- Módulo de facturación
- Portal de clientes externos
- APIs públicas para terceros

---

## 5. Arquitectura Técnica Propuesta

### 5.1. Visión General de la Arquitectura

El MVP se desarrollará utilizando una arquitectura **cloud-native en Google Cloud Platform (GCP)**, combinando servicios de Firebase para desarrollo rápido con componentes especializados desplegados en GCP. El enfoque es **serverless-first** para minimizar overhead operativo y costes en la fase de MVP.

### 5.2. Stack Tecnológico

#### 5.2.1. Cloud Provider
- **Google Cloud Platform (GCP)** como proveedor principal
- Aprovechar el ecosistema integrado de servicios de Google

#### 5.2.2. Frontend
- **Framework:** Vite + React + TypeScript
  - Vite para builds rápidos y desarrollo ágil
  - React para UI componentes
  - TypeScript para type safety y mejor mantenibilidad
- **Hosting:** Firebase Hosting
  - CDN global
  - SSL automático
  - Despliegue simple y rápido

#### 5.2.3. Backend
- **Node.js Cloud Functions** para lógica de negocio ligera:
  - Procesamiento de webhooks/eventos
  - Orquestación de servicios
  - APIs REST para frontend
  - Integraciones con servicios externos
- **Serverless:** Escala automáticamente según demanda

#### 5.2.4. Motor de Optimización
- **Lenguaje:** Java
- **Framework:** Timefold (evolución de OptaPlanner)
  - Constraint-based optimization
  - Ideal para problemas de routing y scheduling
  - Soporte para optimización multiobjetivo
  - Algoritmos avanzados de búsqueda local
- **Deployment:** Cloud Run
  - Contenedor serverless
  - Escala automáticamente
  - Pago por uso (solo cuando se ejecutan optimizaciones)
  - Aislamiento del motor de optimización

#### 5.2.5. Machine Learning / Predicción (Si Necesario)
- **Lenguaje:** Python
- **Despliegue:** Cloud Functions o Cloud Run
- **Uso:** Predicción de demanda de contenedores si se implementa

#### 5.2.6. LLM Multimodal para Extracción de PDFs
- **Modelo:** Google Gemini
- **Plataforma:** Vertex AI
- **Ventajas:**
  - Nativo en GCP, integración perfecta
  - Modelo multimodal (procesa imágenes de PDFs)
  - Coste-efectivo para MVP
  - Baja latencia al estar en mismo cloud provider
- **Uso:** Análisis y extracción de datos de PDFs

#### 5.2.7. Base de Datos Relacional
- **PostgreSQL con Firebase Data Connect**
- **Ventajas:**
  - Modelo relacional para datos estructurados
  - Integridad referencial (foreign keys, constraints)
  - Queries SQL complejas para analytics
  - Integración con ecosistema Firebase
  - ACID compliant
- **Schema principal:**
  - Contenedores, Terminales, Clientes, Navieras
  - Órdenes (import/export)
  - Llegadas ferroviarias
  - Recomendaciones generadas
  - Historial de feedback de usuarios

#### 5.2.8. Base de Datos NoSQL para UI
- **Firebase Firestore**
- **Uso:**
  - Datos paramétricos de UI (configuración de interfaz)
  - Preferencias de usuario
  - Configuraciones de visualización
  - Datos de sesión
  - Cache de datos frecuentes para UI
- **Ventajas:**
  - Sincronización en tiempo real con frontend
  - Flexibilidad de esquema para parámetros de UI
  - Latencia muy baja para consultas de configuración
  - Integración directa con React

#### 5.2.9. Cloud Functions Adicionales para UI
- **Node.js Cloud Functions** adicionales para soporte de interfaz:
  - APIs de configuración de UI
  - Endpoints para gestión de preferencias de usuario
  - Servicios de transformación de datos para visualización
  - Agregación de datos para dashboards
  - Webhooks para notificaciones en tiempo real

#### 5.2.10. Almacenamiento de Archivos
- **Cloud Storage**
- **Uso:**
  - Almacenamiento de PDFs originales
  - Archivos procesados
  - Logs de procesamiento
  - Backups

#### 5.2.11. Autenticación y Autorización
- **Firebase Authentication**
- **Soporte:**
  - Email/password
  - Integración SSO si Rhenus lo requiere
  - Role-based access control (RBAC)
  - Tokens JWT para APIs

### 5.3. Flujos de Datos Principales

#### 5.3.1. Flujo de Ingesta de PDFs
1. **Email llega al inbox** configurado por Rhenus
2. **Trigger:** Pub/Sub (preferentemente, sujeto a configuración de inbox de Rhenus)
3. **Cloud Function** procesa evento:
   - Descarga PDF del email
   - Almacena en Cloud Storage
4. **Cloud Function** invoca **Gemini (Vertex AI)**:
   - Análisis visual del PDF
   - Extracción de datos estructurados
   - Salida: JSON validado
5. **Validación anti-alucinaciones**:
   - Verificación de consistencia
   - Detección de campos con baja confianza
6. **Almacenamiento en PostgreSQL**:
   - Órdenes import/export
   - Llegadas ferroviarias
   - Actualización de stock de contenedores

#### 5.3.2. Flujo de Generación de Recomendaciones
1. **Trigger:** Nueva orden de export o import procesada
2. **Cloud Function** recopila contexto:
   - Órdenes pendientes
   - Stock de contenedores vacíos
   - Contenedores post-import disponibles
   - Ubicaciones de clientes
3. **Invocación del Motor de Optimización (Timefold en Cloud Run)**:
   - Input: Órdenes, stock, parámetros de optimización
   - Proceso: Algoritmo de constraint optimization
   - Output: Recomendaciones de matching con scores
4. **Almacenamiento de recomendaciones** en PostgreSQL
5. **Notificación a frontend** vía API

#### 5.3.3. Flujo de Feedback de Usuario
1. Usuario acepta/rechaza recomendación en frontend
2. API call a Cloud Function
3. Actualización en PostgreSQL:
   - Estado de recomendación
   - Motivo de rechazo (si aplica)
4. (Futuro) Datos de feedback para reentrenamiento del modelo

### 5.4. Escalabilidad y Rendimiento

- **Serverless-first:** Todos los componentes escalan automáticamente
- **Cloud Run para Timefold:** Escala de 0 a N instancias según demanda
- **Cloud Functions:** Concurrencia automática
- **PostgreSQL:** Escalado vertical inicialmente, lectura réplicas si necesario
- **Cloud Storage:** Escalado ilimitado
- **CDN (Firebase Hosting):** Baja latencia global

### 5.5. Seguridad

- **Autenticación:** Firebase Auth con JWT tokens
- **Autorización:** RBAC implementado en backend
- **Datos en tránsito:** HTTPS/TLS obligatorio
- **Datos en reposo:** Cifrado automático en Cloud Storage y PostgreSQL
- **Secrets:** Google Secret Manager para API keys, credentials
- **Auditoría:** Logging de todas las acciones de usuarios

### 5.6. Consideraciones de Implementación

- **Desarrollo iterativo:** Priorizar funcionalidades core del MVP
- **Infraestructura como código:** Terraform o Firebase CLI para despliegues reproducibles
- **CI/CD:** GitHub Actions o Cloud Build para automatizar despliegues
- **Monitoring:** Cloud Monitoring + Cloud Logging para observabilidad
- **Costes:** Modelo pay-per-use minimiza costes en fase MVP

---

## 6. Tecnologías y Herramientas

Esta sección consolida el stack tecnológico completo del proyecto, incluyendo herramientas de desarrollo, testing y gestión de proyecto.

### 6.1. Plataforma Cloud y Servicios Core

| Categoría | Tecnología | Propósito |
|-----------|-----------|-----------|
| Cloud Provider | Google Cloud Platform (GCP) | Infraestructura cloud principal |
| Hosting Frontend | Firebase Hosting | Alojamiento de aplicación web con CDN |
| Backend Serverless | Cloud Functions (Node.js) | APIs REST y orquestación |
| Motor Optimización | Cloud Run (Java + Timefold) | Algoritmos de optimización constraint-based |
| ML/Predicción | Cloud Functions/Run (Python) | Predicción de demanda (si necesario) |
| LLM Multimodal | Vertex AI (Google Gemini) | Extracción de datos de PDFs |

### 6.2. Frontend

| Categoría | Tecnología | Justificación |
|-----------|-----------|---------------|
| Build Tool | Vite | Builds rápidos, HMR optimizado, ideal para desarrollo ágil |
| Framework UI | React 18+ | Ecosistema maduro, componentes reutilizables |
| Lenguaje | TypeScript | Type safety, mejor mantenibilidad, detección temprana de errores |
| Librería de Componentes | Material-UI (MUI) o Ant Design | Componentes profesionales, accesibilidad, diseño responsive |
| Mapas | Google Maps API o Leaflet | Visualización geográfica de contenedores y rutas |
| Gráficos y Dashboards | Recharts o Chart.js | Visualización de KPIs y métricas |
| Estado Global | React Context API + Hooks | Gestión de estado ligera para MVP |
| HTTP Client | Axios o Fetch API | Llamadas a APIs REST |
| Formularios | React Hook Form | Validación y gestión de formularios eficiente |

### 6.3. Backend y APIs

| Categoría | Tecnología | Propósito |
|-----------|-----------|-----------|
| Runtime Backend | Node.js 20 LTS | Cloud Functions runtime |
| Framework API | Express.js (en Cloud Functions) | Routing y middleware para APIs REST |
| Validación | Zod o Joi | Validación de schemas de datos |
| Testing Backend | Jest + Supertest | Unit tests y integration tests |
| Linter/Format | ESLint + Prettier | Código consistente y de calidad |

### 6.4. Motor de Optimización

| Categoría | Tecnología | Justificación |
|-----------|-----------|---------------|
| Lenguaje | Java 17+ | Ecosistema robusto para optimización |
| Framework Optimización | Timefold | Constraint programming, algoritmos avanzados de scheduling |
| Build Tool | Maven o Gradle | Gestión de dependencias y builds |
| Containerización | Docker | Despliegue en Cloud Run |
| Testing | JUnit 5 + Mockito | Unit tests para lógica de optimización |

### 6.5. Bases de Datos

| Categoría | Tecnología | Uso Principal |
|-----------|-----------|---------------|
| BBDD Relacional | PostgreSQL 15+ (Firebase Data Connect) | Datos transaccionales, órdenes, contenedores, maestros |
| BBDD NoSQL | Cloud Firestore | Datos paramétricos de UI, configuraciones, preferencias |
| Cache (Futuro) | Cloud Memorystore (Redis) | Cache de resultados de optimización si necesario |

### 6.6. Almacenamiento y Mensajería

| Categoría | Tecnología | Uso |
|-----------|-----------|-----|
| Object Storage | Cloud Storage | PDFs originales, archivos procesados, backups |
| Pub/Sub | Cloud Pub/Sub | Procesamiento asíncrono de emails con PDFs |
| Email Processing | Pub/Sub + Cloud Functions | Ingesta automática desde inbox de Rhenus |

### 6.7. Autenticación, Seguridad y Secrets

| Categoría | Tecnología | Propósito |
|-----------|-----------|-----------|
| Autenticación | Firebase Authentication | Login, JWT tokens, gestión de sesiones |
| Autorización | RBAC custom en backend | Control de acceso basado en roles |
| Secrets Management | Google Secret Manager | API keys, credenciales, variables sensibles |
| SSL/TLS | Automático (Firebase Hosting + Cloud Run) | Cifrado en tránsito |
| Cifrado en Reposo | Automático (GCP default encryption) | Protección de datos almacenados |

### 6.8. Observabilidad y Monitoring

| Categoría | Tecnología | Uso |
|-----------|-----------|-----|
| Logging | Cloud Logging | Logs centralizados de todos los servicios |
| Monitoring | Cloud Monitoring | Métricas de rendimiento, alertas |
| Tracing | Cloud Trace | Análisis de latencia de requests |
| Error Tracking | Cloud Error Reporting | Detección y alertas de errores |
| Uptime Monitoring | Cloud Monitoring | Verificación de disponibilidad |

### 6.9. CI/CD y DevOps

| Categoría | Tecnología | Justificación |
|-----------|-----------|---------------|
| Control de Versiones | Git + GitHub/GitLab | Repositorios de código |
| CI/CD | GitHub Actions o Cloud Build | Pipelines automatizados de build/test/deploy |
| IaC | Terraform o Firebase CLI | Infraestructura como código, despliegues reproducibles |
| Containerización | Docker | Empaquetado del motor de optimización |
| Container Registry | Artifact Registry | Almacenamiento de imágenes Docker |

### 6.10. Herramientas de Desarrollo

| Categoría | Tecnología | Propósito |
|-----------|-----------|-----------|
| IDE Recomendado | VS Code o IntelliJ IDEA | Desarrollo frontend/backend (VS Code) y Java (IntelliJ) |
| API Testing | Postman o Insomnia | Testing manual de APIs |
| DB Management | DBeaver o pgAdmin | Gestión de PostgreSQL |
| Colaboración | Slack o Microsoft Teams | Comunicación del equipo |

### 6.11. Testing y Calidad

| Categoría | Frontend | Backend | Motor Optimización |
|-----------|----------|---------|-------------------|
| Unit Testing | Vitest o Jest + React Testing Library | Jest + Supertest | JUnit 5 + Mockito |
| E2E Testing | Playwright o Cypress | - | - |
| Linting | ESLint + TypeScript | ESLint | Checkstyle |
| Formatting | Prettier | Prettier | Google Java Format |
| Coverage | Vitest/Jest coverage | Jest coverage | JaCoCo |

### 6.12. Gestión de Proyecto

| Categoría | Herramienta Propuesta | Uso |
|-----------|----------------------|-----|
| Project Management | Jira o Linear | Gestión de tareas, sprints, epics |
| Documentación | Confluence o Notion | Documentación técnica y de producto |
| Diagramas | Miro o Lucidchart | Diagramas de arquitectura, flujos |
| Design (UI/UX) | Figma | Diseño de interfaces y prototipos |

### 6.13. Librerías y Frameworks Adicionales Clave

#### Frontend
- **react-router-dom:** Navegación SPA
- **date-fns o dayjs:** Manipulación de fechas
- **react-query (TanStack Query):** Cache y sincronización de datos server-side
- **react-hot-toast o notistack:** Notificaciones y alertas
- **formik o react-hook-form:** Gestión de formularios complejos

#### Backend (Node.js)
- **@google-cloud/storage:** SDK de Cloud Storage
- **@google-cloud/vertexai:** SDK de Vertex AI para Gemini
- **pdf-parse o pdf-lib:** Procesamiento de PDFs (si necesario)
- **zod:** Validación de schemas TypeScript-first
- **winston o pino:** Logging estructurado

#### Java (Motor Optimización)
- **Timefold Solver:** Core de optimización constraint-based
- **Jackson:** Serialización/deserialización JSON
- **Lombok:** Reducción de boilerplate
- **SLF4J + Logback:** Logging

### 6.14. Costes Estimados de Infraestructura Cloud (MVP)

**Nota:** Los costes exactos dependerán del volumen de uso real. A continuación, estimaciones conservadoras para un MVP con carga moderada:

| Servicio | Estimación Mensual | Notas |
|----------|-------------------|-------|
| Cloud Functions (Node.js) | €20-50 | Pay-per-invocation, ~10K invocations/mes |
| Cloud Run (Timefold) | €30-80 | Pay-per-use, ~100 horas compute/mes |
| PostgreSQL (Data Connect) | €50-150 | Según tamaño de base de datos |
| Cloud Firestore | €10-30 | Lecturas/escrituras parametrizadas |
| Cloud Storage | €10-20 | ~50GB PDFs y archivos |
| Vertex AI (Gemini) | €30-100 | ~1000-3000 requests/mes de PDFs |
| Firebase Hosting | €0-10 | Generoso free tier + CDN |
| Cloud Monitoring/Logging | €20-40 | Logs y métricas |
| **TOTAL ESTIMADO** | **€170-480/mes** | Fase MVP con tráfico moderado |

**Consideraciones:**
- Costes escalables según uso real (modelo pay-per-use)
- Firebase tiene generous free tiers para MVP
- Vertex AI Gemini es coste-efectivo comparado con alternativas
- Costes pueden optimizarse tras identificar patrones de uso
- No incluye costes de personal de desarrollo

---

## 7. Cronograma y Fases

### 7.1. Metodología de Desarrollo

El proyecto seguirá una **metodología ágil iterativa** con:
- **Sprints de 2 semanas** para desarrollo
- **Reuniones semanales** de seguimiento con Rhenus
- **Demos al final de cada fase** para validación temprana
- **Entregas incrementales** de funcionalidad
- **Feedback continuo** para ajustes rápidos

### 7.2. Fases del Proyecto

El MVP se desarrollará en **4 fases principales** más una fase inicial de descubrimiento:

---

#### **FASE 0: Descubrimiento y Diseño**
**Duración estimada:** 2-3 semanas

**Objetivos:**
- Entender en profundidad los procesos actuales de Rhenus
- Validar supuestos técnicos y de negocio
- Definir esquema de datos y modelo de dominio
- Diseñar arquitectura detallada
- Crear prototipos de UI/UX

**Actividades principales:**
1. **Semana 1: Discovery Workshops**
   - Sesiones con operadores de Rhenus (usuarios finales)
   - Mapeo de procesos actuales de asignación de contenedores
   - Validación de flujos import/export
   - Definición de roles de usuario y permisos
   - Recolección de ejemplos reales de PDFs (órdenes y llegadas ferroviarias)
   - Identificación de reglas de negocio y restricciones

2. **Semana 2-3: Diseño y Arquitectura**
   - Diseño de esquema de base de datos (PostgreSQL + Firestore)
   - Definición de APIs REST
   - Arquitectura de componentes frontend
   - Diseño de UI/UX en Figma (wireframes y prototipos)
   - Definición de modelo de datos para Timefold
   - Plan de testing y estrategia de QA

**Entregables:**
- Documento de especificación funcional detallada
- Diagramas de arquitectura (C4 model)
- Esquema de base de datos
- Prototipos de UI aprobados por Rhenus
- Plan detallado de sprints para Fases 1-4

---

#### **FASE 1: Infraestructura y Fundamentos**
**Duración estimada:** 3-4 semanas (2 sprints)

**Objetivos:**
- Configurar toda la infraestructura cloud en GCP
- Implementar autenticación y autorización
- Desarrollar schema de base de datos
- Crear estructura base de frontend
- Implementar gestión de datos maestros

**Sprints:**

**Sprint 1 (Semanas 1-2): Infraestructura Cloud**
- Setup de proyecto en GCP y Firebase
- Configuración de entornos (development, staging, production)
- PostgreSQL con Firebase Data Connect
- Cloud Firestore para UI
- Cloud Storage para PDFs
- Firebase Authentication + RBAC
- CI/CD con GitHub Actions o Cloud Build
- Monitoreo y logging (Cloud Monitoring)
- Estructura base de frontend (Vite + React + TypeScript)
- Estructura base de backend (Cloud Functions con Express)

**Sprint 2 (Semanas 3-4): Datos Maestros y UI Base**
- Módulo de gestión de contenedores (CRUD)
- Módulo de gestión de terminales (Barcelona, Noain, Agoncillo, Miranda)
- Módulo de gestión de clientes y ubicaciones
- Módulo de gestión de navieras
- Módulo de gestión de rutas y tarifas
- Módulo de parámetros de optimización
- UI base: navegación, layout, componentes comunes
- Panel de administración básico
- Gestión de usuarios y permisos

**Entregables Fase 1:**
- Infraestructura cloud completamente operativa
- Aplicación web desplegada (frontend + backend)
- Sistema de login funcional con roles
- Módulos de gestión de maestros operativos
- Datos de prueba precargados (contenedores, terminales, clientes)

---

#### **FASE 2: Ingesta de Datos con LLM**
**Duración estimada:** 3-4 semanas (2 sprints)

**Objetivos:**
- Implementar procesamiento automático de PDFs con Gemini
- Desarrollar validación anti-alucinaciones
- Crear flujo de ingesta completo (email → PDF → datos estructurados)
- Implementar actualización automática de stock

**Sprint 3 (Semanas 5-6): Extracción con LLM**
- Integración con Vertex AI (Google Gemini)
- Procesamiento de PDFs Tipo A (órdenes import/export)
  - Extracción de datos mediante LLM multimodal
  - Parsing y estructuración en JSON
- Procesamiento de PDFs Tipo B (llegadas ferroviarias)
  - Extracción de contenedores (vacíos y llenos)
  - Diferenciación de estados
- Sistema de validación de datos extraídos
- Detección de alucinaciones y campos con baja confianza
- Almacenamiento en PostgreSQL

**Sprint 4 (Semanas 7-8): Flujo Completo de Ingesta**
- Configuración de inbox de email (coordinación con Rhenus)
- Cloud Pub/Sub + Cloud Functions para procesamiento asíncrono
- Almacenamiento de PDFs en Cloud Storage
- Actualización automática de stock en terminales
- Creación de órdenes de import/export en sistema
- Interface de revisión manual para PDFs con baja confianza
- Notificaciones y alertas de procesamiento
- Dashboard de monitoreo de ingesta (% éxito, errores, tiempos)

**Entregables Fase 2:**
- Sistema de ingesta automática de PDFs completamente funcional
- Órdenes import/export creadas automáticamente desde PDFs
- Stock de terminales actualizado con llegadas ferroviarias
- Interface de validación manual para casos de baja confianza
- Métricas de precisión del modelo LLM

---

#### **FASE 3: Motor de Optimización y Recomendaciones**
**Duración estimada:** 4-5 semanas (2-3 sprints)

**Objetivos:**
- Desarrollar motor de optimización con Timefold
- Implementar algoritmos de matching import-export
- Generar recomendaciones inteligentes
- Crear sistema de feedback de usuarios

**Sprint 5 (Semanas 9-10): Motor de Optimización Base**
- Setup de proyecto Java con Timefold
- Modelo de dominio para optimización:
  - Contenedores (tipos, ubicaciones, estados)
  - Órdenes (import/export con ventanas temporales)
  - Rutas (distancias, costes, tiempos)
- Implementación de constraints:
  - Compatibilidad de tipos de contenedores (22G1, 42G1, 45G1)
  - Ventanas temporales de disponibilidad
  - Proximidad geográfica para matching
  - Restricciones de navieras
- Función objetivo multiobjetivo (coste + tiempo + CO2)
- Testing unitario de lógica de optimización
- Containerización con Docker
- Despliegue en Cloud Run

**Sprint 6 (Semanas 11-12): Generación de Recomendaciones**
- API REST para invocación del motor desde Cloud Functions
- Lógica de recopilación de contexto para optimización:
  - Órdenes pendientes de import/export
  - Stock de contenedores vacíos en terminales
  - Contenedores post-import disponibles en clientes
- Generación de recomendaciones de matching import→export
- Cálculo de rutas optimizadas vs. tradicionales
- Cálculo de impacto (ahorro km, coste, CO2, viajes evitados)
- Scoring de confianza de recomendaciones
- Almacenamiento de recomendaciones en PostgreSQL

**Sprint 7 (Semanas 13-14): UI de Recomendaciones y Feedback** *(Opcional según progreso)*
- Interface de visualización de recomendaciones
- Comparativa visual: ruta tradicional vs. optimizada
- Aceptación/rechazo de recomendaciones
- Captura de motivos de rechazo
- Tracking de ejecución de recomendaciones
- Historial de recomendaciones (aceptadas/rechazadas)
- Notificaciones de nuevas recomendaciones

**Entregables Fase 3:**
- Motor de optimización Timefold operativo en Cloud Run
- Generación automática de recomendaciones de matching
- Interface de usuario para gestionar recomendaciones
- Sistema de feedback completamente funcional
- Métricas de calidad de recomendaciones

---

#### **FASE 4: Visualización, Analytics y Refinamiento**
**Duración estimada:** 3-4 semanas (2 sprints)

**Objetivos:**
- Implementar visualización de stock de contenedores
- Desarrollar dashboards analíticos con KPIs
- Crear mapa geográfico interactivo
- Refinamiento y testing end-to-end

**Sprint 8 (Semanas 15-16): Visualización de Stock y Mapa**
- Vista de contenedores por estados del ciclo de vida:
  - En terminales (vacíos/llenos, Barcelona y ferroviarias)
  - Post-import en ubicaciones de clientes (candidatos para matching)
  - En tránsito (import/export activos)
- Mapa geográfico interactivo:
  - Terminales con niveles de stock
  - Ubicaciones de clientes con contenedores vacíos
  - Órdenes de export pendientes
  - Visualización de oportunidades de matching
  - Rutas activas en tiempo real
- Filtros y búsquedas avanzadas:
  - Por tipo de contenedor (22G1, 42G1, 45G1)
  - Por ubicación, estado, naviera
  - Por disponibilidad temporal

**Sprint 9 (Semanas 17-18): Dashboard Analítico y KPIs**
- Dashboard con KPIs principales:
  - **Métricas de optimización:**
    - % de matching import-export exitoso
    - Viajes evitados
    - Reducción de kilómetros (total y en vacío)
    - Tiempo de inactividad de contenedores
    - Tasa de utilización de contenedores
  - **Métricas de adopción:**
    - % sugerencias aceptadas/rechazadas
    - Tiempo medio de respuesta
    - Motivos de rechazo (análisis)
  - **Métricas de impacto:**
    - Ahorro económico estimado
    - Reducción de emisiones CO2
    - ROI proyectado
- Gráficos de tendencias temporales
- Reportes exportables (PDF, Excel)
- Comparativas antes/después del sistema

**Sprint 10 (Semanas 19-20): Testing, Refinamiento y Documentación**
- Testing end-to-end completo
- Testing de integración entre todos los módulos
- Performance testing y optimizaciones
- Security audit y penetration testing
- Corrección de bugs identificados
- Refinamiento de UI/UX basado en feedback
- Documentación técnica completa:
  - Manual de usuario
  - Guía de administración del sistema
  - Documentación de APIs
  - Guía de deployment
  - Runbook de operaciones

**Entregables Fase 4:**
- Visualización completa de stock de contenedores
- Mapa geográfico interactivo operativo
- Dashboard analítico con todos los KPIs
- Sistema completamente testeado y refinado
- Documentación completa entregada

---

### 7.3. Cronograma Consolidado

| Fase | Sprints | Semanas | Entregable Principal |
|------|---------|---------|---------------------|
| **Fase 0: Descubrimiento** | - | 2-3 | Especificación funcional y diseños aprobados |
| **Fase 1: Infraestructura** | 1-2 | 4 | Infraestructura cloud + Datos maestros |
| **Fase 2: Ingesta LLM** | 3-4 | 4 | Procesamiento automático de PDFs |
| **Fase 3: Optimización** | 5-7 | 5-6 | Motor Timefold + Recomendaciones |
| **Fase 4: Analytics** | 8-10 | 6 | Dashboards + Sistema completo refinado |
| **TOTAL** | **10** | **21-23 semanas** | **MVP completo y operativo** |

**Duración total estimada: 5-6 meses** (incluyendo Fase 0)

---

### 7.4. Hitos Clave (Milestones)

| Milestone | Semana | Criterio de Éxito |
|-----------|--------|-------------------|
| **M1: Kickoff y Discovery Completo** | 3 | Especificación funcional aprobada por Rhenus |
| **M2: Infraestructura Operativa** | 7 | Entornos cloud desplegados, login funcional, maestros operativos |
| **M3: Primera Ingesta Exitosa** | 11 | Primer PDF procesado automáticamente con >90% precisión |
| **M4: Primera Recomendación Generada** | 15 | Motor Timefold genera primera recomendación de matching válida |
| **M5: Beta Privada con Usuarios** | 18 | Operadores de Rhenus prueban sistema end-to-end |
| **M6: MVP en Producción** | 22-23 | Sistema completo desplegado en producción, documentación entregada |

---

### 7.5. Estrategia de Despliegue

**Entornos:**
1. **Development:** Desarrollo activo del equipo
2. **Staging:** Testing interno y demos con Rhenus
3. **Production:** Operación real con usuarios finales

**Modelo de despliegue:**
- **Semanas 1-14:** Solo development y staging
- **Semana 15:** Despliegue a producción con datos reales (fase beta cerrada)
- **Semanas 15-20:** Beta privada con grupo reducido de operadores de Rhenus
- **Semana 21:** Despliegue completo a todos los usuarios

**Estrategia de rollout:**
- **Beta cerrada (2-4 usuarios):** Validación con operadores clave
- **Feedback y ajustes:** Iteración rápida basada en uso real
- **Rollout gradual:** Expansión paulatina a más usuarios
- **Soporte dedicado:** Acompañamiento durante primeras semanas de uso

---

### 7.6. Dependencias y Riesgos de Cronograma

**Dependencias Externas:**
- **Rhenus IT:** Configuración de inbox de email para ingesta de PDFs
- **Rhenus Negocio:** Disponibilidad de stakeholders para discovery y validaciones
- **Datos:** Acceso a PDFs reales de ejemplo y datos maestros históricos

**Riesgos que pueden afectar el cronograma:**
- Complejidad inesperada en procesamiento de PDFs (variabilidad de formatos)
- Precisión del LLM inferior a esperada (requiere ajustes adicionales)
- Cambios en requerimientos durante desarrollo
- Problemas de integración con inbox de email de Rhenus
- Disponibilidad limitada de usuarios para testing

**Mitigaciones:**
- Buffer de 1-2 semanas incluido en estimación total
- Sprints flexibles que permiten reordenamiento de prioridades
- Comunicación semanal para detección temprana de blockers
- Enfoque iterativo permite ajustes continuos sin retrasar MVP completo

---

## 8. Equipo y Recursos

### 8.1. Estructura del Equipo de Desarrollo

El proyecto requiere un equipo multidisciplinario con experiencia en desarrollo cloud-native, optimización algorítmica y machine learning.

#### 8.1.1. Equipo Core (Dedicación Completa o Parcial según Fase)

| Rol | Cantidad | Responsabilidades | Skills Requeridos |
|-----|----------|-------------------|-------------------|
| **Arquitecto de Soluciones / Tech Lead** | 1 | - Diseño de arquitectura técnica<br>- Decisiones tecnológicas<br>- Coordinación técnica del equipo<br>- Code reviews<br>- Mentoría técnica | - GCP/Firebase experto<br>- Arquitecturas serverless<br>- Liderazgo técnico<br>- 8+ años experiencia |
| **Desarrollador Frontend Senior** | 1 | - Desarrollo de UI en React + TypeScript<br>- Componentes de visualización y mapas<br>- Dashboards y KPIs<br>- Integración con APIs | - React + TypeScript avanzado<br>- Vite<br>- UI/UX<br>- Mapas (Google Maps/Leaflet)<br>- 5+ años experiencia |
| **Desarrollador Frontend Mid** | 1 | - Desarrollo de componentes UI<br>- Implementación de formularios<br>- Testing frontend<br>- Soporte a senior | - React + TypeScript<br>- Testing (Jest/Vitest)<br>- 3+ años experiencia |
| **Desarrollador Backend Senior (Node.js)** | 1 | - Cloud Functions development<br>- APIs REST<br>- Integración Vertex AI (Gemini)<br>- Procesamiento de PDFs<br>- Orquestación de servicios | - Node.js + TypeScript<br>- Express.js<br>- GCP/Firebase<br>- LLMs/Vertex AI<br>- 5+ años experiencia |
| **Desarrollador Backend Mid (Node.js)** | 1 | - Desarrollo de APIs<br>- Integración con bases de datos<br>- Testing backend<br>- Soporte a senior | - Node.js<br>- PostgreSQL<br>- Cloud Functions<br>- 3+ años experiencia |
| **Desarrollador Java Senior** | 1 | - Motor de optimización con Timefold<br>- Algoritmos constraint-based<br>- Modeling de problema de optimización<br>- Despliegue en Cloud Run | - Java 17+<br>- Timefold/OptaPlanner<br>- Algoritmos de optimización<br>- Docker<br>- 5+ años experiencia |
| **Ingeniero DevOps / SRE** | 0.5 | - Setup de infraestructura GCP<br>- CI/CD pipelines<br>- Monitoring y alerting<br>- IaC (Terraform)<br>- Gestión de entornos | - GCP experto<br>- Terraform<br>- CI/CD (GitHub Actions/Cloud Build)<br>- Seguridad cloud<br>- 4+ años experiencia |
| **Ingeniero de Datos / ML** | 0.5 | - Validación de datos LLM<br>- Anti-hallucination logic<br>- Tuning de prompts para Gemini<br>- Análisis de precisión del modelo<br>- (Futuro) Predicción de demanda | - Python<br>- LLMs (Gemini/Vertex AI)<br>- Data validation<br>- ML Engineering<br>- 4+ años experiencia |
| **QA Engineer / Tester** | 1 | - Testing end-to-end<br>- Automatización de tests<br>- Testing de integración<br>- Performance testing<br>- Bug tracking y reporting | - Playwright/Cypress<br>- Jest/Vitest<br>- Testing manual y automatizado<br>- 3+ años experiencia |
| **Product Owner** | 0.5 | - Definición de requerimientos<br>- Priorización de backlog<br>- Coordinación con Rhenus<br>- UAT y validación<br>- Gestión de stakeholders | - Experiencia en logística (ideal)<br>- Product management<br>- Metodologías ágiles<br>- Comunicación con cliente |
| **UI/UX Designer** | 0.25-0.5 | - Diseño de wireframes y prototipos<br>- Design system<br>- Usability testing<br>- Iteración de diseños | - Figma<br>- UI/UX para aplicaciones B2B<br>- Design thinking<br>- 3+ años experiencia |

**Total FTE (Full-Time Equivalent):** ~8-9 personas

---

#### 8.1.2. Roles de Soporte (Bajo Demanda / Consultivo)

| Rol | Dedicación | Responsabilidades |
|-----|------------|-------------------|
| **Consultor de Optimización** | Consultoría puntual | - Asesoramiento en modelado de problemas Timefold<br>- Review de constraints y función objetivo<br>- Optimización de performance del solver |
| **Security Consultant** | Fase de testing | - Security audit<br>- Penetration testing<br>- Review de configuraciones de seguridad GCP |
| **Technical Writer** | Sprint 10 | - Documentación técnica<br>- Manuales de usuario<br>- Runbooks de operaciones |

---

### 8.2. Dedicación por Fase

La siguiente tabla muestra la dedicación estimada (en % de tiempo completo) de cada rol por fase del proyecto:

| Rol | Fase 0<br>Discovery | Fase 1<br>Infra | Fase 2<br>LLM | Fase 3<br>Optimización | Fase 4<br>Analytics |
|-----|---------------------|-----------------|---------------|------------------------|---------------------|
| Arquitecto / Tech Lead | 100% | 100% | 80% | 80% | 60% |
| Frontend Senior | 25% | 80% | 60% | 80% | 100% |
| Frontend Mid | 0% | 60% | 40% | 60% | 80% |
| Backend Senior (Node.js) | 50% | 100% | 100% | 80% | 60% |
| Backend Mid (Node.js) | 25% | 80% | 80% | 60% | 40% |
| Java Senior | 25% | 40% | 20% | 100% | 40% |
| DevOps/SRE | 50% | 100% | 60% | 40% | 50% |
| ML Engineer | 50% | 20% | 100% | 40% | 20% |
| QA Engineer | 25% | 40% | 60% | 80% | 100% |
| Product Owner | 100% | 60% | 40% | 40% | 40% |
| UI/UX Designer | 80% | 40% | 20% | 40% | 60% |

**Nota:** Los porcentajes son orientativos y pueden ajustarse según necesidades del proyecto.

---

### 8.3. Organización del Equipo

#### 8.3.1. Estructura de Reporting

```
Product Owner
    ├── Arquitecto / Tech Lead
    │   ├── Frontend Team
    │   │   ├── Frontend Senior
    │   │   └── Frontend Mid
    │   ├── Backend Team
    │   │   ├── Backend Senior (Node.js)
    │   │   ├── Backend Mid (Node.js)
    │   │   ├── Java Senior (Optimización)
    │   │   └── ML Engineer
    │   ├── Platform Team
    │   │   └── DevOps/SRE
    │   └── Quality
    │       └── QA Engineer
    └── UI/UX Designer
```

#### 8.3.2. Ceremonias Ágiles

**Internas del equipo:**
- **Daily Standup:** 15 min diarios (todo el equipo)
- **Sprint Planning:** Inicio de cada sprint (2 semanas)
- **Sprint Review:** Final de cada sprint (demo interna)
- **Sprint Retrospective:** Final de cada sprint
- **Refinement:** Mid-sprint (preparación siguiente sprint)

**Con Cliente (Rhenus):**
- **Reunión semanal de seguimiento:** 1 hora (PO + Arquitecto + stakeholders Rhenus)
- **Demo de fase:** Al finalizar cada fase completa
- **Discovery Workshops:** Fase 0 (sesiones intensivas)

---

### 8.4. Recursos Técnicos

#### 8.4.1. Infraestructura de Desarrollo

| Recurso | Cantidad | Propósito | Coste Estimado |
|---------|----------|-----------|----------------|
| **Licencias GitHub/GitLab** | 10 usuarios | Repositorios de código, CI/CD | €0-100/mes (Team plan) |
| **GCP Credits (Development)** | - | Entorno de desarrollo | €50-150/mes |
| **GCP Credits (Staging)** | - | Entorno de staging/QA | €100-300/mes |
| **Figma** | 3 usuarios | Diseño UI/UX | €45/mes (Professional) |
| **Jira/Linear** | 10 usuarios | Project management | €80-150/mes |
| **Confluence/Notion** | 10 usuarios | Documentación | €50-100/mes |
| **Postman Team** | 5 usuarios | API testing | €50/mes |
| **Slack/Teams** | 10 usuarios | Comunicación | €0-80/mes |

**Total herramientas/mes:** ~€375-975

#### 8.4.2. Hardware y Equipamiento

- **Portátiles de desarrollo:** Provistos por el equipo o cliente
- **Monitores adicionales:** Recomendado para desarrolladores
- **Acceso a internet de alta velocidad:** Esencial para equipo remoto

---

### 8.5. Requerimientos del Cliente (Rhenus)

Para el éxito del proyecto, se requiere la participación activa de Rhenus en los siguientes aspectos:

#### 8.5.1. Recursos Humanos de Rhenus

| Rol | Dedicación | Responsabilidades |
|-----|------------|-------------------|
| **Product Owner / Sponsor de Negocio** | 20-40% | - Aprobación de requerimientos<br>- Decisiones de negocio<br>- Coordinación interna Rhenus<br>- Validación de entregables |
| **Operadores de Rhenus (Subject Matter Experts)** | 10-20%<br>(Fase 0: 50%) | - Participación en discovery<br>- Validación de flujos<br>- Testing de usabilidad<br>- Feedback sobre recomendaciones |
| **Administrador IT de Rhenus** | 5-10% | - Configuración de inbox de email<br>- Coordinación de accesos<br>- Soporte en integración |
| **Beta Testers (Operadores)** | Variable<br>(Fase 4) | - Uso del sistema en beta privada<br>- Reporte de bugs<br>- Feedback de usabilidad |

#### 8.5.2. Datos y Accesos Requeridos

- **PDFs de ejemplo reales:**
  - Órdenes de import (mínimo 20 ejemplos)
  - Órdenes de export (mínimo 20 ejemplos)
  - Llegadas ferroviarias (mínimo 10 ejemplos)
- **Datos maestros:**
  - Lista de clientes y ubicaciones GPS
  - Navieras con las que trabaja Rhenus
  - Tarifas de transporte TRUCK (estimaciones)
  - Horarios y tarifas de TRAIN (si disponible)
- **Accesos:**
  - Configuración de inbox de email para Pub/Sub
  - Permisos para crear proyecto en GCP de Rhenus (si aplica)
  - VPN o acceso seguro si se requiere conectividad privada

#### 8.5.3. Disponibilidad para Validaciones

- **Fase 0 (Discovery):** Alta disponibilidad de stakeholders y operadores
- **Demos de fase:** Asistencia de decision-makers
- **UAT (User Acceptance Testing):** Fase 4, dedicación de beta testers
- **Reuniones semanales:** Product Owner o representante autorizado

---

### 8.6. Modelo de Trabajo

#### 8.6.1. Modalidad

- **Remoto-first:** Equipo puede trabajar de forma distribuida
- **Reuniones virtuales:** Todas las ceremonias y coordinaciones online
- **Presencial (opcional):** Kick-off inicial y demos de fase pueden ser presenciales si Rhenus lo requiere

#### 8.6.2. Zona Horaria

- **Equipo principal:** Zona horaria de España (CET/CEST) para alineación con Rhenus
- **Horario de colaboración:** Overlap de al menos 6 horas laborables con Rhenus

#### 8.6.3. Herramientas de Colaboración

- **Comunicación:** Slack o Microsoft Teams
- **Videollamadas:** Google Meet, Zoom o Microsoft Teams
- **Documentación compartida:** Confluence o Notion
- **Gestión de tareas:** Jira o Linear
- **Diseño colaborativo:** Figma (con acceso para stakeholders de Rhenus)

---

### 8.7. Ramp-up y Onboarding

#### Semana 1 (Pre-Discovery):
- Formación del equipo completo
- Setup de herramientas y accesos
- Sesión de kick-off interno
- Preparación de discovery workshops

#### Semana 2-3 (Discovery):
- Onboarding con Rhenus
- Inmersión en procesos de negocio
- Acceso a datos y sistemas (lectura)

---

### 8.8. Consideraciones de Escalabilidad del Equipo

**Post-MVP (Futuro):**

Si el proyecto escala más allá del MVP a otras regiones o funcionalidades:
- **Frontend:** +1 desarrollador por cada módulo complejo adicional
- **Backend:** +1 desarrollador por cada integración externa
- **Optimización:** +1 especialista si se añaden modos de transporte adicionales (marítimo, aéreo)
- **DevOps:** Incremento a 100% FTE para gestión multi-región
- **Soporte:** Equipo de 2-3 personas para soporte L1/L2 de usuarios finales

---

## 9. Presupuesto

### 9.1. Modelo de Presupuesto

Este presupuesto está diseñado para el desarrollo del MVP (Minimum Viable Product) del sistema TMS con optimización de contenedores vacíos para la zona norte de España.

**Componentes principales del presupuesto:**
1. Costes de personal de desarrollo (equipo técnico)
2. Costes de infraestructura cloud (GCP/Firebase)
3. Herramientas y licencias
4. Contingencia

**Nota:** Todos los valores son **estimaciones orientativas** basadas en el alcance definido del MVP y están sujetos a validación final con Rhenus.

---

### 9.2. Costes de Personal de Desarrollo

#### 9.2.1. Cálculo por Rol y Fase

La siguiente tabla muestra el coste estimado de cada rol considerando:
- Duración de cada fase (semanas)
- Dedicación (% FTE) por fase
- Tarifa diaria estimada por rol

**Supuestos de cálculo:**
- 1 mes = 4 semanas
- 1 semana = 5 días laborables
- Tarifas basadas en mercado España para perfiles senior/mid

| Rol | Tarifa Día | Fase 0<br>(3 sem) | Fase 1<br>(4 sem) | Fase 2<br>(4 sem) | Fase 3<br>(6 sem) | Fase 4<br>(6 sem) | **Total** |
|-----|------------|-------------------|-------------------|-------------------|-------------------|-------------------|-----------|
| **Arquitecto / Tech Lead** | €700 | €10,500<br>(100%, 15d) | €14,000<br>(100%, 20d) | €11,200<br>(80%, 16d) | €16,800<br>(80%, 24d) | €12,600<br>(60%, 18d) | **€65,100** |
| **Frontend Senior** | €600 | €2,250<br>(25%, 3.75d) | €9,600<br>(80%, 16d) | €7,200<br>(60%, 12d) | €14,400<br>(80%, 24d) | €18,000<br>(100%, 30d) | **€51,450** |
| **Frontend Mid** | €450 | €0<br>(0%, 0d) | €5,400<br>(60%, 12d) | €3,600<br>(40%, 8d) | €8,100<br>(60%, 18d) | €10,800<br>(80%, 24d) | **€27,900** |
| **Backend Senior (Node.js)** | €650 | €4,875<br>(50%, 7.5d) | €13,000<br>(100%, 20d) | €13,000<br>(100%, 20d) | €15,600<br>(80%, 24d) | €11,700<br>(60%, 18d) | **€58,175** |
| **Backend Mid (Node.js)** | €500 | €1,875<br>(25%, 3.75d) | €8,000<br>(80%, 16d) | €8,000<br>(80%, 16d) | €9,000<br>(60%, 18d) | €6,000<br>(40%, 12d) | **€32,875** |
| **Java Senior** | €650 | €2,438<br>(25%, 3.75d) | €5,200<br>(40%, 8d) | €2,600<br>(20%, 4d) | €19,500<br>(100%, 30d) | €7,800<br>(40%, 12d) | **€37,538** |
| **DevOps/SRE** *(0.5 FTE)* | €600 | €4,500<br>(50%, 7.5d) | €12,000<br>(100%, 20d) | €7,200<br>(60%, 12d) | €7,200<br>(40%, 12d) | €9,000<br>(50%, 15d) | **€39,900** |
| **ML Engineer** *(0.5 FTE)* | €600 | €4,500<br>(50%, 7.5d) | €2,400<br>(20%, 4d) | €12,000<br>(100%, 20d) | €7,200<br>(40%, 12d) | €3,600<br>(20%, 6d) | **€29,700** |
| **QA Engineer** | €500 | €1,875<br>(25%, 3.75d) | €4,000<br>(40%, 8d) | €6,000<br>(60%, 12d) | €12,000<br>(80%, 24d) | €15,000<br>(100%, 30d) | **€38,875** |
| **Product Owner** *(0.5 FTE)* | €600 | €9,000<br>(100%, 15d) | €7,200<br>(60%, 12d) | €4,800<br>(40%, 8d) | €7,200<br>(40%, 12d) | €7,200<br>(40%, 12d) | **€35,400** |
| **UI/UX Designer** *(0.5 FTE)* | €500 | €6,000<br>(80%, 12d) | €4,000<br>(40%, 8d) | €2,000<br>(20%, 4d) | €6,000<br>(40%, 12d) | €9,000<br>(60%, 18d) | **€27,000** |

**Subtotal Personal de Desarrollo:** **€443,913**

#### 9.2.2. Roles de Soporte (Consultoría Puntual)

| Rol | Estimación | Justificación |
|-----|------------|---------------|
| **Consultor de Optimización Timefold** | €3,000 - €5,000 | 1-2 días de consultoría para modelado de constraints y optimización (Fase 3) |
| **Security Consultant** | €4,000 - €6,000 | Security audit y penetration testing (Fase 4) |
| **Technical Writer** | €2,500 - €4,000 | Documentación técnica, manuales de usuario (Sprint 10) |

**Subtotal Roles de Soporte:** **€9,500 - €15,000**

---

### 9.3. Costes de Infraestructura Cloud

#### 9.3.1. Costes de GCP/Firebase Durante Desarrollo (6 meses)

| Entorno | Meses | Coste Mensual Estimado | Total |
|---------|-------|------------------------|-------|
| **Development** | 6 | €50-150 | €300-900 |
| **Staging** | 5 (desde mes 2) | €100-300 | €500-1,500 |
| **Production (Beta)** | 2 (últimos 2 meses) | €170-480 | €340-960 |

**Subtotal Infraestructura (Desarrollo del MVP):** **€1,140 - €3,360**

#### 9.3.2. Costes de Infraestructura Post-Lanzamiento (Estimación Primer Año)

**Producción en operación normal (estimación mensual):**

Basado en la tabla de la sección 6.14, con ajustes para diferentes niveles de tráfico:

| Servicio | Tráfico Bajo | Tráfico Medio | Tráfico Alto |
|----------|--------------|---------------|--------------|
| Cloud Functions (Node.js) | €20 | €35 | €50 |
| Cloud Run (Timefold) | €30 | €55 | €80 |
| PostgreSQL (Data Connect) | €50 | €100 | €150 |
| Cloud Firestore | €10 | €20 | €30 |
| Cloud Storage | €10 | €15 | €20 |
| Vertex AI (Gemini) | €30 | €65 | €100 |
| Firebase Hosting | €5 | €7 | €10 |
| Monitoring/Logging | €20 | €30 | €40 |
| **TOTAL MENSUAL** | **€175** | **€327** | **€480** |
| **TOTAL ANUAL** | **€2,100** | **€3,924** | **€5,760** |

**Notas sobre costes de infraestructura:**
- Modelo pay-per-use: costes escalan según uso real
- Firebase ofrece free tiers generosos que reducen costes iniciales
- Optimizaciones post-MVP pueden reducir costes (caching, batching, etc.)
- Cifras NO incluyen backup/DR adicional ni multi-región

---

### 9.4. Herramientas y Licencias

| Categoría | Duración | Coste Mensual | Total Proyecto |
|-----------|----------|---------------|----------------|
| GitHub/GitLab | 6 meses | €100 | €600 |
| Figma (UI/UX) | 6 meses | €45 | €270 |
| Jira/Linear (PM) | 6 meses | €150 | €900 |
| Confluence/Notion (Docs) | 6 meses | €100 | €600 |
| Postman Team | 6 meses | €50 | €300 |
| Slack/Teams | 6 meses | €80 | €480 |

**Subtotal Herramientas y Licencias:** **€3,150**

---

### 9.5. Otros Costes

| Concepto | Estimación | Justificación |
|----------|------------|---------------|
| **Kick-off presencial (opcional)** | €2,000 - €4,000 | Viajes y reuniones iniciales si Rhenus lo requiere |
| **Demos presenciales (opcional)** | €1,500 - €3,000 | 2-3 demos de fase presenciales (viajes) |
| **Buffer de imprevistos** | €5,000 | Contingencias menores no previstas |

**Subtotal Otros Costes:** **€8,500 - €12,000** (incluye contingencia)

---

### 9.6. Resumen de Presupuesto del MVP

| Categoría | Rango Mínimo | Rango Máximo |
|-----------|--------------|--------------|
| **Personal de Desarrollo** | €443,913 | €443,913 |
| **Roles de Soporte (Consultores)** | €9,500 | €15,000 |
| **Infraestructura Cloud (6 meses desarrollo)** | €1,140 | €3,360 |
| **Herramientas y Licencias** | €3,150 | €3,150 |
| **Otros Costes (viajes + contingencia)** | €8,500 | €12,000 |
| **TOTAL PROYECTO MVP** | **€466,203** | **€477,423** |

---

### 9.7. Modelo de Facturación Propuesto

#### Opción A: Precio Fijo por Fases

Facturación por hitos de fase completados:

| Fase | % del Total | Importe (basado en €470,000) |
|------|-------------|------------------------------|
| **Fase 0: Discovery** | 10% | €47,000 |
| **Fase 1: Infraestructura** | 20% | €94,000 |
| **Fase 2: Ingesta LLM** | 25% | €117,500 |
| **Fase 3: Optimización** | 30% | €141,000 |
| **Fase 4: Analytics** | 15% | €70,500 |

**Ventajas:**
- Predictibilidad de costes para Rhenus
- Pagos ligados a entregables tangibles
- Menor riesgo financiero para el cliente

#### Opción B: Time & Materials (T&M)

Facturación mensual según esfuerzo real dedicado:

- Facturación al final de cada mes
- Basada en horas reales trabajadas por rol
- Tarifas acordadas por rol
- Reporting semanal de horas consumidas

**Ventajas:**
- Flexibilidad para ajustar alcance durante desarrollo
- Cliente paga solo por trabajo realizado
- Facilita cambios de prioridades

#### Opción C: Híbrido (Recomendado)

- **Fase 0 (Discovery):** Precio fijo de €47,000
- **Fases 1-4:** Time & Materials con techo presupuestario de €430,000
- Revisión mensual de gastos vs. presupuesto
- Alertas tempranas si se prevé exceder techo

**Ventajas:**
- Combina predictibilidad con flexibilidad
- Discovery a precio fijo valida alcance
- Desarrollo iterativo con control de costes

---

### 9.8. Costes Post-MVP (Primer Año de Operación)

Para planificación financiera de Rhenus, costes estimados del primer año tras entrega del MVP:

| Concepto | Anual | Mensual | Notas |
|----------|-------|---------|-------|
| **Infraestructura Cloud (Producción)** | €2,100 - €5,760 | €175 - €480 | Según volumen de uso (ver 9.3.2) |
| **Soporte y Mantenimiento** | €40,000 - €60,000 | €3,333 - €5,000 | 1-1.5 desarrolladores equivalentes, soporte L2/L3 |
| **Licencias de Herramientas (reducido)** | €1,800 - €2,400 | €150 - €200 | Solo herramientas productivas necesarias |
| **Evolutivos y Mejoras** | €30,000 - €80,000 | Variable | Nuevas funcionalidades, integraciones adicionales |
| **TOTAL PRIMER AÑO (Solo Operación)** | **€73,900 - €148,160** | **€6,158 - €12,347** | Sin contar nuevos desarrollos |

**Notas:**
- Costes de operación mucho menores que desarrollo inicial
- Soporte puede ser interno de Rhenus si forman equipo técnico
- Evolutivos son opcionales según roadmap de Rhenus

---

### 9.9. Retorno de Inversión (ROI) Esperado

**Análisis de valor generado por el MVP:**

Basado en el contexto del problema (sección 3.1):

- **Coste global de reposicionamiento de vacíos:** ~$20 billones/año (industria completa)
- **Ineficiencia:** 33% de contenedores en circulación están vacíos
- **Ahorro por matching exitoso:** ~33% de viajes eliminados (ejemplo sección 3.1)

**Escenario conservador para Rhenus (zona norte España):**

Supuestos:
- Rhenus gestiona ~5,000 contenedores/año en zona norte (estimación conservadora)
- 40% son contenedores import que quedan vacíos
- 30% de esos vacíos pueden hacer matching con exports (tasa de éxito conservadora)
- Coste promedio de un viaje de retorno vacío: €150-300 (combustible + tiempo + driver)

**Cálculo:**
- Contenedores import/año: 5,000 × 40% = 2,000
- Matchings exitosos/año: 2,000 × 30% = 600 contenedores
- Viajes evitados: 600 × 2 (retorno + recogida) = 1,200 viajes
- **Ahorro anual:** 1,200 viajes × €225 (promedio) = **€270,000/año**

**ROI del MVP:**
- Inversión inicial: ~€470,000
- Ahorro año 1: ~€270,000 (estimación conservadora)
- Costes operación año 1: ~€100,000
- **Ahorro neto año 1:** €170,000
- **Payback period:** ~1.5 años

**Beneficios adicionales no cuantificados:**
- Reducción de emisiones CO2 (contribución a objetivos ESG)
- Mejor utilización de flota de contenedores
- Reducción de tiempos de inactividad
- Mejora en planificación operativa
- Visibilidad completa de stock de contenedores
- Capacidad de expansión a otras regiones tras validación MVP

**Nota:** Estos cálculos son estimaciones conservadoras. El ahorro real puede ser significativamente mayor según:
- Volumen real de operaciones de Rhenus
- Tasa de matching alcanzada (puede ser >30%)
- Expansión del sistema a otras zonas geográficas
- Optimizaciones adicionales descubiertas durante operación

---

### 9.10. Opciones de Reducción de Presupuesto

Si el presupuesto propuesto excede la disponibilidad de Rhenus, se pueden considerar las siguientes alternativas para reducir costes:

#### Opción 1: MVP Más Reducido (€350,000 - €380,000)

**Alcance reducido:**
- Eliminar Fase 4 completa (dashboards analíticos avanzados)
- KPIs básicos solo en tablas simples (sin gráficos interactivos)
- Sin mapa geográfico interactivo
- Solo visualización básica de stock

**Ahorro:** ~€90,000 - €100,000

#### Opción 2: Equipo Reducido (€400,000 - €420,000)

**Ajustes de equipo:**
- Eliminar Frontend Mid (Senior hace todo)
- Eliminar Backend Mid (Senior hace todo)
- QA compartido a medio tiempo

**Ahorro:** ~€50,000 - €70,000
**Riesgo:** Mayor duración del proyecto, carga alta en seniors

#### Opción 3: Simplificar Procesamiento de PDFs (€430,000 - €450,000)

**Alcance ajustado:**
- Carga manual de datos extraídos de PDFs en lugar de LLM automático (Fase 2 simplificada)
- Validación manual en lugar de anti-hallucination automático

**Ahorro:** ~€20,000 - €40,000
**Riesgo:** Mayor carga operativa manual, menor adopción de usuarios

---

## 10. Riesgos y Mitigación

### 10.1. Metodología de Gestión de Riesgos

Durante todo el proyecto se seguirá un enfoque proactivo de gestión de riesgos:

1. **Identificación continua:** Revisión de riesgos en cada sprint retrospective
2. **Evaluación:** Probabilidad (Alta/Media/Baja) × Impacto (Alto/Medio/Bajo)
3. **Mitigación:** Planes de acción preventivos
4. **Monitoring:** Seguimiento en reuniones semanales con Rhenus
5. **Escalación:** Protocolo claro para riesgos críticos

---

### 10.2. Riesgos Técnicos

| # | Riesgo | Probabilidad | Impacto | Mitigación | Plan de Contingencia |
|---|--------|--------------|---------|------------|----------------------|
| **T1** | **Precisión insuficiente del LLM (Gemini) en extracción de PDFs**<br>El modelo no alcanza >90% precisión en extracción de datos de PDFs variados | Media | Alto | - Testing temprano con PDFs reales en Fase 0<br>- Prompts engineering iterativo<br>- Validación anti-alucinaciones robusta<br>- Ajuste de confidence thresholds | - Implementar human-in-the-loop para casos de baja confianza<br>- Considerar fine-tuning del modelo<br>- Fallback a procesamiento manual asistido |
| **T2** | **Variabilidad de formatos de PDFs**<br>PDFs de diferentes fuentes con formatos muy heterogéneos dificultan extracción consistente | Alta | Medio | - Recopilar ejemplos de TODAS las fuentes en Discovery<br>- Diseñar prompts genéricos y robustos<br>- Implementar normalización de datos post-extracción | - Crear templates de extracción por tipo de fuente<br>- Validación manual obligatoria para nuevas fuentes<br>- OCR adicional si PDFs son scaneados |
| **T3** | **Performance del motor de optimización (Timefold)**<br>Tiempos de cálculo excesivos (>30 seg) para generar recomendaciones | Media | Medio | - Benchmarking temprano con datasets realistas<br>- Optimización de constraints<br>- Limitar alcance temporal de optimización (ej: próximas 48h)<br>- Tuning de solver parameters | - Implementar límites de tiempo de ejecución<br>- Generar recomendaciones en batch asíncrono<br>- Cachear resultados de optimización<br>- Simplificar función objetivo si necesario |
| **T4** | **Escalabilidad de PostgreSQL con Firebase Data Connect**<br>Limitaciones de rendimiento con grandes volúmenes de datos | Baja | Medio | - Diseño de schema optimizado desde inicio<br>- Índices apropiados en queries frecuentes<br>- Particionamiento de tablas históricas<br>- Monitoring de performance desde día 1 | - Migrar a PostgreSQL estándar en Cloud SQL<br>- Implementar caching con Memorystore<br>- Optimizar queries más lentas<br>- Archivado de datos históricos |
| **T5** | **Integraciones con inbox de email de Rhenus**<br>Complejidad técnica para conectar Pub/Sub con inbox corporativo | Media | Alto | - Discovery temprana de infraestructura email de Rhenus<br>- Involucrar IT de Rhenus desde Fase 0<br>- Validar permisos y posibilidades técnicas<br>- Considerar alternativas (email forwarding, API si disponible) | - Implementar polling de email vía IMAP/POP3 como alternativa<br>- Upload manual de PDFs vía UI como fallback temporal<br>- Integración via FTP/SFTP si email no viable |
| **T6** | **Complejidad de despliegue y configuración en GCP**<br>Problemas en setup de infraestructura serverless | Baja | Medio | - Equipo DevOps experto en GCP<br>- IaC con Terraform desde inicio<br>- Entornos de staging réplica de producción<br>- Documentación exhaustiva de despliegues | - Soporte de Google Cloud Professional Services<br>- Revisión de arquitectura con GCP Solutions Architect<br>- Rollback plans para cada despliegue |

---

### 10.3. Riesgos de Proyecto

| # | Riesgo | Probabilidad | Impacto | Mitigación | Plan de Contingencia |
|---|--------|--------------|---------|------------|----------------------|
| **P1** | **Disponibilidad limitada de stakeholders de Rhenus**<br>Falta de tiempo de usuarios/negocio para discovery, validaciones y testing | Media | Alto | - Comunicar claramente expectativas de dedicación desde inicio<br>- Acordar calendario de disponibilidad en kick-off<br>- Involucrar a management de Rhenus para priorización<br>- Sesiones cortas y bien preparadas | - Extender Fase 0 de Discovery<br>- Priorizar funcionalidades críticas<br>- Asumir decisiones con aprobación posterior<br>- Documentar supuestos para revisión |
| **P2** | **Cambios de alcance durante desarrollo (scope creep)**<br>Solicitudes de funcionalidades adicionales fuera del MVP | Alta | Medio | - Especificación funcional clara y firmada<br>- Product backlog priorizado<br>- Proceso formal de change requests<br>- Comunicación de impacto (tiempo/coste) de cambios | - Documentar cambios en backlog para post-MVP<br>- Re-negociar timeline/presupuesto si cambios críticos<br>- Enfoque iterativo permite ajustar prioridades |
| **P3** | **Retrasos en acceso a datos maestros y PDFs de ejemplo**<br>Rhenus no proporciona datos necesarios a tiempo | Media | Alto | - Lista clara de datos requeridos desde kick-off<br>- Seguimiento semanal de provisión de datos<br>- Escalación temprana si retrasos<br>- Datos sintéticos para desarrollo inicial | - Trabajar con datos sintéticos/mock<br>- Postponer Fase 2 hasta tener PDFs reales<br>- Ajustar cronograma según disponibilidad<br>- Validación intensiva cuando datos lleguen |
| **P4** | **Rotación de personal en equipo de desarrollo**<br>Desarrolladores clave abandonan el proyecto | Baja | Alto | - Contratos con cláusulas de permanencia<br>- Documentación continua de código y decisiones<br>- Pair programming para knowledge sharing<br>- Code reviews obligatorios | - Onboarding rápido de reemplazos<br>- Redistribución de trabajo entre equipo<br>- Soporte de otros seniors temporalmente<br>- Extensión de timeline si necesario |
| **P5** | **Coordinación con múltiples stakeholders de Rhenus**<br>Decisiones inconsistentes de diferentes áreas de negocio | Media | Medio | - Identificar Product Owner único con poder de decisión<br>- Steering committee si necesario<br>- Matriz RACI clara (Responsible, Accountable, Consulted, Informed)<br>- Documentar y compartir decisiones | - Escalación a management de Rhenus<br>- Product Owner tiene voto final<br>- Decisiones arquitectónicas por equipo técnico |
| **P6** | **Subestimación de esfuerzo de testing**<br>Más bugs de lo esperado, testing toma más tiempo | Media | Medio | - QA Engineer desde Fase 1<br>- Testing continuo, no solo al final<br>- Automated testing desde inicio<br>- Buffer de 2 semanas en Sprint 10 | - Extender Fase 4 si necesario<br>- Priorizar bugs críticos vs. nice-to-have<br>- Beta extendida con fixing iterativo<br>- Lanzamiento en etapas (phased rollout) |

---

### 10.4. Riesgos de Negocio

| # | Riesgo | Probabilidad | Impacto | Mitigación | Plan de Contingencia |
|---|--------|--------------|---------|------------|----------------------|
| **N1** | **Baja adopción del sistema por operadores**<br>Usuarios finales no usan el sistema o rechazan recomendaciones sistemáticamente | Media | Alto | - Involucrar operadores desde Discovery<br>- UX intuitivo y amigable<br>- Training adecuado<br>- Sistema de apoyo, no imposición<br>- Demostrar valor desde beta privada | - Programa de change management<br>- Incentivos para adopción<br>- Mejoras de UX basadas en feedback<br>- Comunicación de wins tempranos |
| **N2** | **Expectativas de ROI no cumplidas**<br>Ahorro real menor al proyectado | Media | Medio | - Estimaciones conservadoras de ROI (30% matching)<br>- Comunicar que MVP es validación, no optimización total<br>- KPIs claros para medir valor<br>- Foco en aprendizaje y validación | - Análisis de causas (datos, algoritmo, adopción)<br>- Iteraciones post-MVP para mejorar matching<br>- Expansión a otras zonas para escala<br>- Valor en visibilidad y analytics también cuenta |
| **N3** | **Complejidad operativa mayor de la esperada**<br>Procesos reales de Rhenus más complejos que lo asumido | Alta | Alto | - Discovery exhaustivo en Fase 0<br>- Validación continua con operadores<br>- Enfoque iterativo permite ajustes<br>- Documentar supuestos y validarlos | - Simplificar alcance de MVP si necesario<br>- Priorizar casos de uso más comunes (80/20)<br>- Dejar casos edge para post-MVP<br>- Ajustar modelo de optimización según realidad |
| **N4** | **Regulaciones o restricciones de navieras**<br>Restricciones contractuales con shipping lines limitan reutilización de contenedores | Baja | Alto | - Validar políticas de navieras en Discovery<br>- Consultar con área legal/comercial de Rhenus<br>- Diseñar constraints por naviera en motor<br>- Flexibilidad para reglas específicas | - Matching solo dentro de misma naviera<br>- Negociación con navieras si MVP demuestra valor<br>- Enfoque en casos permitidos primero |

---

### 10.5. Riesgos de Seguridad y Cumplimiento

| # | Riesgo | Probabilidad | Impacto | Mitigación | Plan de Contingencia |
|---|--------|--------------|---------|------------|----------------------|
| **S1** | **Breach de datos sensibles de clientes**<br>Acceso no autorizado a datos de clientes, rutas, tarifas | Baja | Muy Alto | - Security by design desde arquitectura<br>- RBAC estricto<br>- Cifrado en tránsito y reposo<br>- Auditoría de accesos<br>- Security audit en Fase 4<br>- Penetration testing | - Protocolo de respuesta a incidentes<br>- Notificación inmediata a Rhenus y afectados<br>- Auditoría forense<br>- Revisión y hardening de seguridad |
| **S2** | **Cumplimiento GDPR/LOPD**<br>Datos personales no gestionados correctamente | Baja | Alto | - Revisión legal de datos procesados<br>- Políticas de retención de datos<br>- Anonimización donde posible<br>- Consentimientos si aplica<br>- DPO de Rhenus involucrado | - Auditoría de cumplimiento<br>- Corrección de gaps identificados<br>- Documentación de procesamiento de datos<br>- Data Processing Agreement con Rhenus |
| **S3** | **Dependencia de servicios de Google Cloud**<br>Vendor lock-in, cambios de pricing o disponibilidad | Media | Medio | - Arquitectura modular con abstracciones<br>- Uso de estándares (PostgreSQL, Docker, etc.)<br>- Documentación de servicios usados<br>- Monitoreo de costs y alertas | - Multi-cloud teórico posible (pero costoso)<br>- Negociación de contratos enterprise con Google<br>- Portabilidad a servicios equivalentes si necesario |

---

### 10.6. Matriz de Riesgos (Probabilidad × Impacto)

**Riesgos Críticos (Alta prioridad de atención):**
- **T1:** Precisión LLM insuficiente
- **T5:** Integración inbox email
- **P1:** Disponibilidad stakeholders
- **P3:** Acceso a datos
- **N1:** Baja adopción de usuarios
- **N3:** Complejidad operativa
- **S1:** Breach de datos

**Riesgos Altos (Monitoreo continuo):**
- **T2:** Variabilidad formatos PDFs
- **T3:** Performance Timefold
- **P2:** Scope creep
- **P4:** Rotación personal
- **N2:** ROI no cumplido

**Riesgos Medios (Seguimiento periódico):**
- **T4, T6, P5, P6, N4, S2, S3**

---

### 10.7. Plan de Comunicación de Riesgos

**Frecuencia de revisión:**
- **Semanal:** Revisión rápida de riesgos críticos en reunión con Rhenus
- **Por Sprint:** Evaluación completa en retrospective
- **Por Fase:** Assessment de riesgos antes de iniciar nueva fase

**Escalación:**
1. **Nivel 1 (Verde):** Riesgo bajo control, seguimiento normal
2. **Nivel 2 (Amarillo):** Riesgo materializado parcialmente, requiere acción
3. **Nivel 3 (Rojo):** Riesgo crítico, requiere decisión de management

**Responsabilidades:**
- **Product Owner:** Comunicación a stakeholders de Rhenus
- **Arquitecto/Tech Lead:** Riesgos técnicos y decisiones de arquitectura
- **Todo el equipo:** Identificación proactiva de nuevos riesgos

---

### 10.8. Lecciones Aprendidas y Mejora Continua

Al final de cada fase y del proyecto completo:

1. **Retrospectiva de riesgos:**
   - ¿Qué riesgos se materializaron?
   - ¿Fueron efectivas las mitigaciones?
   - ¿Qué riesgos no identificamos?

2. **Documentación:**
   - Actualizar registro de riesgos
   - Compartir aprendizajes con Rhenus
   - Mejorar estimaciones para futuras fases/proyectos

3. **Ajustes:**
   - Incorporar aprendizajes en planificación de siguientes sprints
   - Actualizar estrategias de mitigación según eficacia

---

## Referencias

### Información del Cliente
- [Rhenus Group US](https://www.rhenus.group/us/en/)
- [Rhenus Logistics LinkedIn](https://es.linkedin.com/company/rhenus-logistics)
- [Rhenus en España](https://www.rhenus.group/es/es/rhenus-group/rhenus-en-espana/)

### Investigación del Problema de Contenedores Vacíos
- [Logística Inversa del Contenedor de Importación y Exportación - Zonalogística](https://www.zonalogistica.com/logistica-inversa-del-contenedor-de-importacion-y-exportacion/)
- [La contenerización y el problema de los contenedores vacíos - EAE](https://retos-operaciones-logistica.eae.es/la-contenerizacion-y-el-problema-de-los-contenedores-vacios/)
- [La cadena de suministro de contenedores vacíos - Crane Worldwide Logistics](https://es.craneww.com/centro-de-Conocimiento/%C3%BAltimas-noticias-e-informaci%C3%B3n/log%C3%ADstica-de-contenedores-vac%C3%ADos/)
- [Tendencias logísticas para 2026 - APR](https://www.apr.es/tendencias-logisticas-2026/)
