# Guía de contenido – Entregable 4

**Diseño e Integración de Sistemas de Información – Franco's S.A.C.**
Evalúa: CE014 – Gestión de Sistemas de Información · Etapa CDIO: Operate
Rol: Arquitecto de Soluciones / Analista de SI
Estándares dominantes: TOGAF – ISO 27001 – ITIL 4 – ISO/IEC 25010

Notas de apoyo para llenar cada sección de `indice_entregable4.tex`.
- **Insumo:** de qué sección del *Informe de Arquitectura Empresarial* (AE), fase TOGAF o entregable previo sale el contenido.
- **Rúbrica:** qué exige el nivel Excelente (18–20 pts.).
- **PENDIENTE:** contenido que aún falta definir.

## Hilo conductor del entregable

Todo el E4 gira en torno a un solo problema y una sola solución, ya fijados en el informe AE:

- **Problema (AE 4.5):** ausencia de mecanismos de monitoreo y control en el procedimiento de *Operación y Control de Cocción* (S5-P02), lo que genera variación de calidad entre lotes por falta de estándares e instrumentos para medir tiempo y temperatura.
- **Alcance (AE 5.1.1):** subproceso de Procesamiento Térmico, ocho familias de producto. Fuera: Procesamiento Inicial y Procesamiento Final (envasado).
- **Visión (AE 5.2.1):** monitorear y controlar las variables críticas de cocción para reducir la variabilidad entre lotes y fortalecer la trazabilidad.
- **Solución (AE 5.4 aplicación TO-BE):** seis componentes:
  1. Módulo de Fichas Técnicas de Cocción (parámetros estándar por familia)
  2. Servicio de Integración IoT (sensores y actuador de la freidora)
  3. Módulo de Monitoreo (compara lecturas en tiempo real, ordena cancelación ante anomalía)
  4. Módulo de Alertas (notifica a operario y jefe de producción)
  5. Módulo de Visión Artificial (conformidad del producto y descarte automático)
  6. Plataforma BI (indicadores y desviaciones por lote, turno y familia)

Cada capítulo del E4 debe usar estos mismos nombres para que el documento guarde coherencia con el informe AE.

---

## Introducción

- Resumir el contexto ya fijado en E1–E3 y en el informe AE sin repetirlo: Franco's S.A.C. (MYPE de snacks naturales, ~40 productos en 8 familias), problema, alcance, visión y la solución de seis componentes.
- Cerrar con un párrafo que anuncie los cinco capítulos (CE0141 a CE0145).

---

## 1. CE0141 – Mapa del Ecosistema de Sistemas de Información de la Organización

**Rúbrica:** mapa completo con todos los sistemas existentes, sus relaciones, interdependencias y roles organizacionales claramente identificados.

| Sección | Insumo / nota |
|---|---|
| 1.1.1 Procedimiento S5-P02 | AE 5.1.1 (alcance) y AE 5.3.1 (diagrama AS-IS de Fase B). Referenciar procesos de E3, no copiarlos. |
| 1.1.2 Actores y áreas | AE 5.1.3: Producción, Calidad, Infraestructura/Software, Gestión de TI, Gerencia General, Cliente. |
| 1.2.1 SICO ERP/Móvil | AE 4.3: solo emite comprobantes; no tiene módulo de control de proceso. |
| 1.2.2 Formato físico de inspección | AE 4.3: lo usa Control de Calidad para evaluar el producto terminado (sabor, textura, apariencia). |
| 1.2.3 Registros manuales | Papel y Excel usados en otros procesos (inventario, pedidos: AE 3.5.1). En cocción no existe ningún registro. |
| 1.2.4 Roles organizacionales | Propietario y usuarios de cada sistema según el organigrama (AE 4.1). Exigido por la rúbrica. |
| 1.2.5 Matriz sistema – proceso | Cruce de sistemas con los procesos del mapa (Obtención de insumos, Producción, Almacenaje, Despacho). |
| 1.3.1 a 1.3.3 Diagramas AS-IS | AE 5.4.1.1 (datos), AE 5.4 aplicación AS-IS y AE 5.5.1 (tecnología). **PENDIENTE en el informe AE:** datos AS-IS y tecnología AS-IS están vacíos. |
| 1.3.4 Relaciones e interdependencias | Exigido por la rúbrica: mostrar que hoy no hay integración entre SICO, el formato de calidad y producción. |
| 1.4 Hallazgos | Brechas de aplicación (AE 5.4 GAP: 7 prácticas manuales → 6 módulos), datos (AE 4.2) y tecnología (AE 4.4). |

---

## 2. CE0142 – Arquitectura Conceptual del Sistema de Información Propuesto

**Rúbrica:** arquitectura completa, justificada y alineada a los objetivos organizacionales, con componentes, capas y tecnologías claramente definidos.

| Sección | Insumo / nota |
|---|---|
| 2.1.1 Visión y vista motivacional | AE 5.2.1 y 5.2.2 (Fase A). |
| 2.1.2 Alineación con objetivos estratégicos | AE 3.5: sobre todo E3 (optimizar gestión operativa con tecnologías digitales) y E8 (certificaciones de calidad); también CE0112 del E1. |
| 2.1.3 Principios de arquitectura | AE 5.1.2: proceso estandarizado, trazabilidad del lote, dato único, registro de variables críticas, retención, interoperabilidad, monitoreo, captura instrumentada, disponibilidad. |
| 2.1.4 Requisitos de calidad y seguridad | ISO/IEC 25010 (disponibilidad, fiabilidad, rendimiento) e ISO 27001 (acceso a datos del lote). |
| 2.2.1 Componentes | Los seis componentes del hilo conductor. |
| 2.2.2 a 2.2.4 Capas TO-BE | AE 5.4 aplicación TO-BE, AE 5.4.1.2 datos TO-BE, AE 5.5.2 tecnología TO-BE. **PENDIENTE en el informe AE:** datos TO-BE y tecnología TO-BE. |
| 2.2.5 Matriz de transición | Formato de la clase Fase C (Baseline vs Target): SICO se mantiene; formato físico y aviso verbal se eliminan; los seis módulos son nuevos. |
| 2.3 Tecnologías y su justificación | Fase E, paso 3: soluciones candidatas (sensores, microcontrolador, broker MQTT, cámara, BD, Power BI), criterios de selección acordes a una MYPE (bajo costo). |

---

## 3. CE0143 – Modelo de Integración de Sistemas y Flujos de Información

**Rúbrica:** modelo completo con flujos de información documentados, interfaces definidas y coherencia técnica entre sistemas.

| Sección | Insumo / nota |
|---|---|
| 3.1 Diagrama de comunicación | Conexiones entre los seis componentes (Fase C). |
| 3.2 Tabla de interfaces | Por construir. Columnas sugeridas: ID, origen, destino, dato, protocolo, formato, frecuencia, seguridad. |
| 3.2.1 Freidora – IoT | Lecturas de temperatura y tiempo; orden al actuador. |
| 3.2.2 IoT – monitoreo y alertas | Comparación con ficha técnica y notificación de desviación. |
| 3.2.3 Visión artificial – lote | Resultado de conformidad y descarte. |
| 3.2.4 Base de datos – BI | Indicadores por lote, turno y familia. |
| 3.3 Flujo del proceso principal | AE 5.3.2 (TO-BE de Fase B): 11 actividades, 6 modificadas y 1 nueva ("Notificar desviación de proceso térmico"). |
| 3.4 Coherencia técnica y seguridad | Validación cruzada: cada interfaz ↔ componente ↔ actividad del proceso TO-BE. |

---

## 4. CE0144 – Plan de Implementación y Gestión del Sistema de Información

**Rúbrica:** plan detallado con fases, recursos, tiempos, responsables, estrategia de despliegue y gestión del cambio claramente definidos.

| Sección | Insumo / nota |
|---|---|
| 4.1.1 Paquetes de trabajo | Fase E (AE 5.6). |
| 4.1.2 Hoja de ruta | Fase E y CE0114 Roadmap Tecnológico (E1). |
| 4.1.3 Cronograma de 14 meses | Fase F (AE 5.7). Debe coincidir con CE0123 (E2). |
| 4.1.4 Matriz RACI | Actores de AE 5.1.3. Exigido por la rúbrica. |
| 4.1.5 Recursos y presupuesto | CE0122 y CE0124 (E2). |
| 4.2 Despliegue y reversión | Fase F: transiciones A y B, piloto (sugerido: una familia de producto antes de las ocho). **PENDIENTE:** plan de reversión. |
| 4.3.1 Riesgos R-01 a R-20 | Fase F y CE0125 (E2). **PENDIENTE:** R-20. |
| 4.3.2 Gobernanza | Fase G (AE 5.8). |
| 4.3.3 Gestión del cambio | Fase H. |
| 4.3.4 Capacitación y adopción | Operarios por turno; vincular con objetivo estratégico E1 (capacitación en monitoreo). |
| 4.3.5 Soporte y operación | ITIL 4: mesa de ayuda, gestión de incidentes de sensores y del sistema. |

---

## 5. CE0145 – Indicadores de Uso, Valor y Mejora del Sistema de Información

**Rúbrica:** indicadores de uso, valor generado y mejora continua del SI definidos con métricas, línea base, metas y mecanismos de seguimiento.

| Sección | Insumo / nota |
|---|---|
| 5.1 Tabla de indicadores | Fase A (visión) y Fase E (IOS5-P02, criterios de éxito). |
| 5.1.1 Uso | Ej.: % de lotes con parámetros registrados automáticamente; disponibilidad del sistema en turnos. |
| 5.1.2 Valor | Ej.: variabilidad de temperatura/tiempo entre lotes; % de lotes no conformes; descartes. |
| 5.1.3 Mejora | Ej.: tiempo de respuesta ante alertas; fichas técnicas actualizadas por familia. |
| 5.2 Fórmula, línea base, meta y frecuencia | Línea base desde CE0135 (E3). **PENDIENTE:** metas sin validar. |
| 5.3 Seguimiento | Plataforma BI del propio sistema como tablero; Fase G y Fase H. |

---

## Secciones finales

- **Conclusiones y recomendaciones.**
- **Referencias:** formato IEEE o APA 7.ª edición.
- **Anexos:** actas, evidencias, dashboards y reportes complementarios.

## Observaciones

### Sobre la plantilla de Prism
1. El capítulo 1 tiene contenido de CE0131 (mapa de procesos, SIPOC, jerarquización), no de CE0141.
2. En el E3, los códigos CE0133 (TO-BE) y CE0134 (Propuesta de automatización) están intercambiados respecto al documento maestro.
3. La portada dice "CE011 · Entregable 3": cambiar a "CE014 · Entregable 4: Diseño e Integración de Sistemas de Información" y actualizar la fecha.

### Sobre el informe de Arquitectura Empresarial (insumos que faltan)
1. Fase C – Datos (AS-IS, TO-BE, GAP) está vacía: se necesita para 1.3.1 y 2.2.3.
2. Fase D – Tecnología está vacía: se necesita para 1.3.3, 2.2.4 y 2.3.
3. Fases E, F y G tienen solo la plantilla copiada (subtítulos 5.5.x repetidos).
4. El punto 5.8 dice "Fase F – Gobernabilidad"; debe ser **Fase G**.
5. Arquitectura de aplicación repite la numeración 5.4.1 de datos; debería ser 5.4.2.
6. La introducción del informe AE anuncia capítulos (AMOFHIT, PESTEL, caso de negocio) que no coinciden con su propio índice.
