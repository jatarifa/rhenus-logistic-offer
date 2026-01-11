# Oferta Técnica - Rhenus Logistics

**Cliente:** Rhenus Logistics
**Fecha:** 11 de Enero de 2026
**Preparado por:** José - Arquitecto de Sistemas y Software

---

## 1. Información del Cliente

Rhenus Logistics es una empresa de logística global con:
- Presencia en España desde 1964
- 37 delegaciones en Península, Canarias y Baleares
- Parte del Rhenus Group (8.6 billones € facturación anual, 39.000 empleados, 1.120 ubicaciones)
- Servicios: Transporte (aéreo, marítimo, carretera, ferroviario), almacenamiento, logística portuaria, soluciones digitales

---

## 2. Resumen Ejecutivo

[Por definir]

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

[Por definir]

---

## 6. Tecnologías y Herramientas

[Por definir]

---

## 7. Cronograma y Fases

[Por definir]

---

## 8. Equipo y Recursos

[Por definir]

---

## 9. Presupuesto

[Por definir]

---

## 10. Riesgos y Mitigación

[Por definir]

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
