# Guía de contenido – Entregable 4

Qué debe contener cada sección de `indice_entregable4.tex` y de dónde sale.

## 1. CE0141 – Mapa del Ecosistema de SI
*Rúbrica: todos los sistemas, sus relaciones, interdependencias y roles organizacionales.*

| Sección | Qué debe contener | Insumo |
|---|---|---|
| 1.1 Inventario de sistemas | Tabla: sistema / herramienta, tipo (software, papel, Excel), función, proceso que soporta, estado. | Informe AE 4.3 (SICO ERP/Móvil, formato físico de inspección, papel y Excel). |
| 1.2 Roles organizacionales | Tabla: sistema, área propietaria, responsable, usuarios y tipo de uso (registra, consulta, aprueba). | Informe AE 4.1 (organigrama) y 5.1.3 (actores). |
| 1.3 Diagrama del ecosistema actual | Diagrama de los sistemas actuales con las áreas que los usan y la infraestructura donde corren. Párrafo breve que lo explique. | Fase C y D: AS-IS de aplicación y tecnología. |
| 1.4 Relaciones e interdependencias | Matriz sistema × sistema (qué información intercambian y cómo: manual o automática). Señalar los sistemas aislados. | Diagrama de 1.3. |
| 1.5 Hallazgos | Tabla: código, tipo de brecha (aplicación, datos, tecnología), descripción, impacto. Cerrar con un párrafo de síntesis. | Brechas GAP-A, GAP-D y GAP-T. |

## 2. CE0142 – Arquitectura Conceptual del SI Propuesto
*Rúbrica: completa, justificada, alineada a objetivos, con componentes, capas y tecnologías.*

| Sección | Qué debe contener | Insumo |
|---|---|---|
| 2.1 Objetivos que guían el diseño | Visión de arquitectura, objetivos estratégicos que atiende el sistema y principios de arquitectura (tabla: principio, declaración, implicancia). | Fase A (visión, vista motivacional) y Fase Preliminar (principios). |
| 2.2 Componentes del sistema propuesto | Tabla: componente, función, usuario principal, brecha que cierra. | Informe AE 5.4 (seis módulos del TO-BE). |
| 2.3 Diagrama por capas | Diagrama con capas de presentación, aplicación, datos e infraestructura, y un párrafo por capa. | Fase C y D: software, modelo de datos e infraestructura TO-BE. |
| 2.4 Tecnologías y su justificación | Tabla: componente, tecnología elegida, alternativas evaluadas, criterio de selección (costo, compatibilidad, soporte). | Fase E, paso 3: soluciones candidatas y decisiones transversales. |

## 3. CE0143 – Modelo de Integración y Flujos de Información
*Rúbrica: flujos documentados, interfaces definidas y coherencia técnica.*

| Sección | Qué debe contener | Insumo |
|---|---|---|
| 3.1 Diagrama de comunicación | Diagrama de los componentes y sus conexiones, con flechas que indiquen qué dato viaja en cada una. | Fase C: conexiones del diagrama de software. |
| 3.2 Tabla de interfaces | Tabla: ID, origen, destino, dato, protocolo, formato, frecuencia. | Flujos IoT → backend → base de datos (por construir). |
| 3.3 Flujo del proceso principal | Diagrama BPMN del proceso TO-BE indicando en qué actividad interviene cada sistema. | Fase B: proceso TO-BE de cocción. |

## 4. CE0144 – Plan de Implementación y Gestión del SI
*Rúbrica: fases, recursos, tiempos, responsables, despliegue y gestión del cambio.*

| Sección | Qué debe contener | Insumo |
|---|---|---|
| 4.1 Fases y cronograma | Paquetes de trabajo por fase y un diagrama de Gantt con hitos. | Fase E (paquetes, roadmap) y Fase F (cronograma de 14 meses; debe coincidir con E2). |
| 4.2 Responsables y recursos | Matriz RACI (actividad × rol) y tabla de recursos (humanos, hardware, software, presupuesto). | Actores del Informe AE 5.1.3 y presupuesto del E2. |
| 4.3 Despliegue y reversión | Estrategia de despliegue (piloto, etapas de transición) y plan de reversión: qué condición lo activa y qué pasos sigue. | Fase F: transiciones A y B, piloto. **Pendiente:** reversión. |
| 4.4 Gestión del cambio y soporte | Tabla de riesgos (riesgo, probabilidad, impacto, mitigación), plan de capacitación, comunicación y soporte post-implementación. | Riesgos R-01 a R-20 (**pendiente R-20**), Fase G (gobernanza) y Fase H (gestión del cambio). |

## 5. CE0145 – Indicadores de Uso, Valor y Mejora del SI
*Rúbrica: métricas, línea base, metas y mecanismos de seguimiento.*

| Sección | Qué debe contener | Insumo |
|---|---|---|
| 5.1 Tabla de indicadores | Tabla: código, indicador, tipo (uso, valor, mejora), objetivo al que responde. Al menos uno de cada tipo. | Fase A (objetivo) y Fase E (IOS5-P02, criterios de éxito). |
| 5.2 Fórmula, línea base, meta y frecuencia | Ficha por indicador: fórmula, unidad, línea base, meta, frecuencia de medición, fuente del dato. | **Pendiente:** metas sin validar. |
| 5.3 Seguimiento | Quién mide, cada cuánto, dónde se reporta (tablero) y qué se hace si no se cumple la meta. | Fase G (gobernanza) y Fase H. |
