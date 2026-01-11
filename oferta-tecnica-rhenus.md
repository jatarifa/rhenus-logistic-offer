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

Rhenus Logistics actualmente dispone de un sistema TMS que no cubre adecuadamente la optimización del uso de contenedores vacíos, generando:
- Costes innecesarios de reposicionamiento
- Retornos a terminal de contenedores que podrían utilizarse directamente
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
   - Identificar automáticamente oportunidades de conectar contenedores de importación con órdenes de exportación
   - Evitar retornos a terminal cuando exista demanda cercana

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
  - PDFs con información de llegadas de contenedores vía tren a terminales ferroviarias (para gestión de stock en depots)
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
- **Contenedores en depots:** Vista del inventario de contenedores disponibles en:
  - Terminal marítima: Barcelona
  - Terminales ferroviarias: Noain, Agoncillo y Miranda
- **Contenedores en uso:** Tracking del estado de contenedores actualmente asignados a rutas
- **Distribución geográfica:** Mapa de la zona norte mostrando:
  - Ubicaciones de terminales y stock de contenedores (Barcelona, Noain, Agoncillo, Miranda)
  - Centro de gestión en Bilbao (sin stock físico de contenedores)
  - Contenedores vacíos vs. necesidades de exportación
- **Estados y tipos:** Clasificación por tipo de contenedor, condición, y disponibilidad

#### 3.6.2. Métricas de Efectividad del Sistema
El sistema proporcionará indicadores clave (KPIs) para que el negocio pueda evaluar el retorno de la inversión:

- **Métricas de optimización:**
  - % de contenedores de importación reutilizados directamente para exportación (sin retorno a depot)
  - Reducción estimada de kilómetros en vacío
  - Tiempo promedio de inactividad de contenedores
  - Tasa de utilización de contenedores

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
     - Procesamiento de llegadas de contenedores vía tren a terminales ferroviarias (Noain, Agoncillo, Miranda)
   - Procesamiento en tiempo real o near-real-time
   - Sistema de validación para detección de inconsistencias y alucinaciones del modelo
   - Alertas en caso de errores o baja confianza en la extracción
   - Actualización automática de stock en depots con base en información de llegadas validada

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
- **Ingesta automática:** Monitorización continua del inbox configurado
- **Extracción de datos mediante LLM multimodal:**
  - Tipo de operación (import/export)
  - Cliente/naviera
  - Origen y destino (terminales: Barcelona, Noain, Agoncillo, Miranda)
  - Tipo y cantidad de contenedores
  - Fechas de operación
  - Requisitos especiales
- **Salida:** Datos estructurados en formato JSON
- **Validación:** Detección de inconsistencias y alucinaciones
- **Notificaciones:** Alertas a usuarios cuando se requiere intervención manual o validación humana

**B) PDFs de Llegadas de Contenedores Ferroviarios**
- **Ingesta automática:** Monitorización de PDFs con información de llegadas de contenedores vía tren
- **Extracción de datos mediante LLM multimodal:**
  - Terminal ferroviaria de destino (Noain, Agoncillo o Miranda)
  - Identificación de contenedores
  - Tipo y características de contenedores
  - Fecha y hora de llegada
  - Estado del contenedor (vacío/lleno)
- **Salida:** Datos estructurados en formato JSON
- **Validación:** Verificación de consistencia de datos extraídos
- **Actualización de stock:** Actualización automática del inventario en el depot correspondiente tras validación exitosa
- **Notificaciones:** Alertas sobre nuevas llegadas y disponibilidad de contenedores

#### 4.4.2. Motor de Recomendaciones de Optimización

El sistema generará recomendaciones que incluirán:

- **Matching específico:** Identificación concreta de contenedor de importación → orden de exportación
- **Ruta propuesta:** Secuencia detallada de movimientos y modos de transporte sugeridos:
  - **TRAIN:** Transporte ferroviario entre terminales (Barcelona ↔ Noain/Agoncillo/Miranda)
  - **TRUCK:** Transporte por carretera para primero/último tramo o trayectos completos
  - Combinaciones multimodales óptimas TRAIN + TRUCK
- **Impacto estimado:**
  - Ahorro económico estimado
  - Kilómetros evitados
  - Reducción de emisiones de CO2
  - Tiempo de operación
- **Nivel de confianza:** Score que indica la fiabilidad de la recomendación

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

- **Vista de depots:** Inventario de contenedores disponibles por ubicación:
  - **Barcelona:** Terminal marítima
  - **Noain, Agoncillo, Miranda:** Terminales ferroviarias
  - Stock actualizado automáticamente con PDFs de llegadas de tren
- **Contenedores en uso:** Estado de contenedores asignados a rutas activas (TRAIN/TRUCK)
- **Mapa de distribución:** Visualización geográfica de la zona norte con ubicaciones de contenedores vacíos vs. necesidades de exportación
- **Filtros y búsquedas:** Por tipo de contenedor, ubicación (Barcelona/Noain/Agoncillo/Miranda), estado, disponibilidad, propietario

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
   - Tipos (20', 40', High Cube, Reefer, etc.)
   - Capacidades y características
   - Propietarios (Rhenus, navieras, terceros)
   - Estado actual (disponible, en uso, en mantenimiento)
   - Ubicación actual

2. **Depots/Terminales**
   - **Barcelona:** Terminal marítima (puerto)
   - **Noain, Agoncillo, Miranda:** Terminales ferroviarias
   - Capacidades de almacenamiento por ubicación
   - Tipos de contenedores soportados en cada terminal
   - Costes de almacenamiento
   - Operadores y horarios de operación

3. **Rutas y Tarifas**
   - Costes de transporte entre terminales (Barcelona ↔ Noain/Agoncillo/Miranda)
   - Tiempos estimados de tránsito por modo:
     - **TRAIN:** Rutas ferroviarias entre Barcelona y terminales ferroviarias
     - **TRUCK:** Rutas por carretera entre terminales
   - Restricciones de capacidad por modo de transporte
   - Frecuencias de servicio ferroviario

4. **Clientes y Navieras**
   - Información de clientes
   - Navieras colaboradoras
   - Acuerdos comerciales relevantes
   - Prioridades o restricciones específicas

5. **Parámetros de Optimización**
   - Pesos para los diferentes criterios (coste, tiempo, CO2)
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
