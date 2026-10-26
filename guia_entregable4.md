# Guía de contenido – Entregable 4

**Diseño e Integración de Sistemas de Información**
Evalúa: CE014 – Gestión de Sistemas de Información · Etapa CDIO: Operate
Rol: Arquitecto de Soluciones / Analista de SI
Estándares dominantes: TOGAF – ISO 27001 – ITIL 4 – ISO/IEC 25010

Notas de apoyo para llenar cada sección de `indice_entregable4.tex`.
- **Insumo:** de qué fase TOGAF o entregable previo sale el contenido.
- **Rúbrica:** qué exige el nivel Excelente (18–20 pts.).
- **PENDIENTE:** contenido que aún falta definir.

---

## Introducción

- Resumir el contexto ya fijado en E1–E3 sin repetirlo: organización, problema, objetivo del proyecto y procesos rediseñados en el TO-BE.

---

## 1. CE0141 – Mapa del Ecosistema de Sistemas de Información de la Organización

**Rúbrica:** mapa completo con todos los sistemas existentes, sus relaciones, interdependencias y roles organizacionales claramente identificados.

| Sección | Insumo / nota |
|---|---|
| 1.1 Alcance del mapa | Procesos de CE0131 y CE0132 (E3). Solo referenciarlos, no copiarlos. |
| 1.2 Inventario de sistemas | Fase C: AS-IS de aplicación (SICO, papel, hojas sueltas). |
| 1.2.3 Roles organizacionales | Propietario y usuarios de cada sistema (exigido por la rúbrica). |
| 1.2.4 Matriz sistema – proceso | Cruce de sistemas con los procesos del E3. |
| 1.3 Diagrama del ecosistema actual | Fase C y Fase D: AS-IS de aplicación y de tecnología. |
| 1.3.3 Relaciones e interdependencias | Exigido por la rúbrica. |
| 1.4 Hallazgos | Brechas GAP-A, GAP-D y GAP-T. |

---

## 2. CE0142 – Arquitectura Conceptual del Sistema de Información Propuesto

**Rúbrica:** arquitectura completa, justificada y alineada a los objetivos organizacionales, con componentes, capas y tecnologías claramente definidos.

| Sección | Insumo / nota |
|---|---|
| 2.1.1 Alineación con los objetivos organizacionales | Fase A (vista motivacional) y CE0112 Alineamiento Estratégico (E1). |
| 2.1.2 Principios de arquitectura | Fase Preliminar. |
| 2.1.3 Requisitos de calidad y seguridad | ISO/IEC 25010 (atributos de calidad) e ISO 27001 (seguridad). |
| 2.2 Diagrama por capas | Fase C y Fase D: software, modelo de datos e infraestructura TO-BE. |
| 2.3 Tecnologías y su justificación | Fase E, paso 3: soluciones candidatas y decisiones transversales. |

---

## 3. CE0143 – Modelo de Integración de Sistemas y Flujos de Información

**Rúbrica:** modelo completo con flujos de información documentados, interfaces definidas y coherencia técnica entre sistemas.

| Sección | Insumo / nota |
|---|---|
| 3.1 Diagrama de comunicación | Fase C: conexiones del diagrama de software. |
| 3.2 Tabla de interfaces | Fase C y Fase D: flujos IoT → backend → base de datos (por construir). Columnas sugeridas: ID, origen, destino, dato, protocolo, formato, frecuencia, seguridad. |
| 3.3 Flujo del proceso principal | Fase B y CE0133 (E3): proceso TO-BE de cocción. |
| 3.4 Coherencia técnica y seguridad | Validación cruzada: cada interfaz ↔ componente TO-BE ↔ proceso. |

---

## 4. CE0144 – Plan de Implementación y Gestión del Sistema de Información

**Rúbrica:** plan detallado con fases, recursos, tiempos, responsables, estrategia de despliegue y gestión del cambio claramente definidos.

| Sección | Insumo / nota |
|---|---|
| 4.1.1 Paquetes de trabajo | Fase E. |
| 4.1.2 Hoja de ruta | Fase E y CE0114 Roadmap Tecnológico (E1). |
| 4.1.3 Cronograma de 14 meses | Fase F. Debe coincidir con CE0123 (E2). |
| 4.1.4 Matriz RACI | Responsables (exigido por la rúbrica). |
| 4.1.5 Recursos y presupuesto | CE0122 y CE0124 (E2). |
| 4.2 Despliegue y reversión | Fase F: transiciones A y B, y piloto. **PENDIENTE:** plan de reversión. |
| 4.3.1 Riesgos R-01 a R-20 | Fase F y CE0125 (E2). **PENDIENTE:** R-20. |
| 4.3.2 Gobernanza | Fase G. |
| 4.3.3 Gestión del cambio | Fase H. |
| 4.3.5 Soporte y operación | ITIL 4: mesa de ayuda, gestión de incidentes. |

---

## 5. CE0145 – Indicadores de Uso, Valor y Mejora del Sistema de Información

**Rúbrica:** indicadores de uso, valor generado y mejora continua del SI definidos con métricas, línea base, metas y mecanismos de seguimiento.

| Sección | Insumo / nota |
|---|---|
| 5.1 Tabla de indicadores | Fase A (objetivos) y Fase E (IOS5-P02, criterios de éxito). Separar en uso / valor / mejora. |
| 5.2 Fórmula, línea base, meta y frecuencia | Línea base desde CE0135 (E3). **PENDIENTE:** metas sin validar. |
| 5.3 Seguimiento | Fase G y Fase H. Tablero sugerido: Power BI, Tableau o Looker Studio. |

---

## Secciones finales

- **Referencias:** formato IEEE o APA 7.ª edición.
- **Anexos:** actas, evidencias, dashboards y reportes complementarios.

## Observaciones sobre la plantilla actual

1. El capítulo 1 tiene contenido de CE0131 (mapa de procesos, SIPOC, jerarquización), no de CE0141.
2. En el E3, los códigos CE0133 (TO-BE) y CE0134 (Propuesta de automatización) están intercambiados respecto al documento maestro.
3. La portada dice "CE011 · Entregable 3": cambiar a "CE014 · Entregable 4: Diseño e Integración de Sistemas de Información" y actualizar la fecha.
