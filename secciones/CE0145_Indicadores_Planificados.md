# CE0145 – Indicadores de Uso, Valor y Mejora del SI

**Organización:** Franco's S.A.C.
**Sistema:** Franco's ERP (TI-002) y su infraestructura (TI-003)
**Tipo de indicadores:** planificados

---

## 1. Qué son estos indicadores

El ERP todavía no está en operación. Por eso estos indicadores son **planificados**: aquí se define qué se va a medir, cómo y qué meta se espera. Se empiezan a medir cuando el ERP entre en funcionamiento.

- **Línea base:** el punto de partida. Si hoy se conoce, se pone; si no, dice "se mide al inicio".
- **Meta:** lo que se espera lograr. Cuando viene de E1 o E2, se indica la fuente; las demás las define el equipo del proyecto.
- **Medida (vista):** la medida de la vista motivacional del CE0142 (MD-01 a MD-10) que el indicador desarrolla. Las diez medidas de la vista tienen aquí su fórmula, línea base, meta y frecuencia.

## 2. Indicadores

### 2.1 Uso: ¿se usa el sistema?

| ID | Indicador | Medida (vista) | Fórmula | Línea base | Meta | Frecuencia | Fuente del dato | Responsable |
|---|---|---|---|---|---|---|---|---|
| U-01 | Procesos digitalizados | — | (Procesos que se registran en el ERP ÷ total de procesos identificados) × 100 | 0 % (hoy todo es papel y Excel, CE0141) | 65 % en 2026 y 80 % a largo plazo (E1, tablero BSC) | Mensual | Módulos del ERP en uso | Área de Gestión de TI |
| U-02 | Pedidos registrados en el ERP | MD-01 | (Ventas registradas en el ERP ÷ comprobantes emitidos en SICO) × 100 | 0 % (las ventas se anotan en papel, CE0141 H-02) | 100 % a los 3 meses del inicio | Mensual | ERP y SICO | Área de Ventas |
| U-03 | Pedidos con despacho cerrado en el ERP | MD-02 | (Pedidos en estado «entregado» ÷ pedidos despachados en el mes) × 100 | 0 % (la distribución se anota en papel, CE0141 H-04) | 100 % a los 3 meses del inicio | Mensual | Módulo de despacho | Área de Logística |
| U-04 | Solicitudes de insumos tramitadas en el ERP | MD-04 | (Solicitudes de insumos registradas en el ERP ÷ solicitudes de insumos del mes) × 100 | 0 % (las solicitudes van en papel, CE0141 H-21) | 100 % a los 3 meses del inicio | Mensual | Módulo de producción e inventario de insumos | Área de Insumos |
| U-05 | Objetivos del BSC con seguimiento | MD-05 | (Objetivos del cuadro de mando con medición del mes ÷ total de objetivos) × 100 | 0 % (no hay seguimiento de la estrategia) | 100 % | Mensual | Módulo de estrategia | Jefatura de Gestión Estratégica |
| U-06 | Clientes con cuenta verificada | MD-10 | (Clientes con correo verificado ÷ clientes registrados en la tienda en línea) × 100 | 0 % (no hay tienda en línea) | 90 % o más | Mensual | Módulo de autenticación y personas | Área de Ventas |
| U-07 | Usuarios activos | — | (Usuarios que entraron al ERP al menos una vez en el mes ÷ usuarios con cuenta) × 100 | 0 % (no hay sistema) | 90 % o más | Mensual | Registro de accesos del ERP | Área de Gestión de TI |
| U-08 | Pedidos por la tienda en línea | — | (Pedidos del Portal B ÷ total de pedidos) × 100 | 0 % (no hay tienda en línea) | 10 % el primer año | Mensual | Módulo de pedidos | Área de Ventas |

### 2.2 Valor: ¿el sistema ayuda al negocio?

| ID | Indicador | Medida (vista) | Fórmula | Línea base | Meta | Frecuencia | Fuente del dato | Responsable |
|---|---|---|---|---|---|---|---|---|
| V-01 | Productos terminados rastreables hasta su lote | MD-03 | (Productos terminados con lote registrado ÷ productos terminados en stock) × 100 | 0 % (los lotes envasados se llevan en un Excel aparte, CE0141 H-05) | 100 % | Mensual | Módulo de inventario | Área de Control e Inventariado |
| V-02 | Tiempo de atención del pedido | — | Promedio de horas desde que se registra el pedido hasta que se entrega | Se mide antes del inicio con una muestra de pedidos en papel | Reducir 30 % | Mensual | Estados del pedido en el ERP | Jefatura de Almacén y Logística |
| V-03 | Quiebres de stock | — | Número de veces en el mes que un producto se agotó | Se cuenta con los registros de los 3 meses anteriores al inicio | Reducir 50 % en los primeros 3 meses (E2, criterio IE-05) | Mensual | Alertas de stock del ERP | Jefatura de Almacén y Logística |
| V-04 | Horas administrativas ahorradas | — | Horas al mes en registrar y ordenar papel y Excel antes, menos las horas de ahora | Se mide antes del inicio con una encuesta a las áreas | 75 horas menos al mes (E2, beneficios) | Mensual | Encuesta a las áreas | Área de Gestión de TI |
| V-05 | Beneficio logrado | — | (Beneficio real del mes ÷ beneficio planificado del mes) × 100 | No aplica: empieza con el sistema | 100 % de lo planificado; S/ 12,350 al mes en plena operación (E2, beneficios) | Mensual | Reportes del ERP y Finanzas | Jefatura de Finanzas |

### 2.3 Mejora: ¿el sistema mejora con el tiempo?

| ID | Indicador | Medida (vista) | Fórmula | Línea base | Meta | Frecuencia | Fuente del dato | Responsable |
|---|---|---|---|---|---|---|---|---|
| M-01 | Incidencias reportadas | — | Número de problemas reportados por los usuarios en el mes | Se mide el primer mes | 10 % menos que el mes anterior | Mensual | Registro de incidencias | Área de Gestión de TI |
| M-02 | Tiempo de solución | — | Promedio de horas para resolver una incidencia | Se mide el primer mes | 8 horas hábiles o menos | Mensual | Registro de incidencias | Área de Gestión de TI |
| M-03 | Satisfacción de los usuarios | — | (Usuarios satisfechos ÷ usuarios encuestados) × 100 | Se mide en las pruebas con usuarios | 80 % o más (E2, criterio IE-04) | Semestral | Encuesta | Área de Gestión de TI |

### 2.4 Calidad del sistema (ISO/IEC 25010): ¿el sistema funciona bien?

| ID | Indicador | Medida (vista) | Fórmula | Línea base | Meta | Frecuencia | Fuente del dato | Responsable |
|---|---|---|---|---|---|---|---|---|
| C-01 | Disponibilidad del ERP | MD-08 | (Horas que el sistema funcionó ÷ horas de trabajo) × 100 | Se mide el primer mes | 95 % o más, de lunes a sábado de 8:00 a 20:00 (E2, criterio IE-01) | Mensual | Monitoreo (CloudWatch) | Área de Infraestructura Tecnológica |
| C-02 | Tiempo de respuesta | — | Segundos que tarda el sistema en responder | Se mide el primer mes | 2 segundos o menos en el 95 % de las operaciones (E2, criterio IE-02) | Mensual | Monitoreo (CloudWatch) | Área de Software |
| C-03 | Respaldo verificado | MD-06 | (Copias diarias hechas ÷ días del mes) × 100, más una prueba de restauración exitosa al mes | 0 (hoy no hay respaldo, CE0141 H-14 y H-16) | 100 % de copias y una restauración exitosa al mes | Mensual | Bucket de respaldos (S3) | Área de Infraestructura Tecnológica |
| C-04 | Tiempo de recuperación | — | Horas para volver a operar después de una caída grave | Prueba del 17/11/2026 (CE0143) | Igual o menor que en la prueba | Semestral (simulacro) | Registro del simulacro | Área de Infraestructura Tecnológica |
| C-05 | Seguridad | — | (Alertas de seguridad atendidas en 24 horas ÷ total de alertas) × 100 | Se mide el primer mes | 100 % | Mensual | Wazuh y AWS WAF | Área de Infraestructura Tecnológica |
| C-06 | Cuentas con permisos solo por rol | MD-07 | (Cuentas activas cuyos permisos vienen solo de su rol ÷ cuentas activas) × 100 | No hay control de acceso que administrar | 100 % (E2, objetivo OPR-07) | Mensual | Módulo de usuarios y roles | Área de Gestión de TI |
| C-07 | Fallas avisadas a un responsable | MD-09 | (Fallas con alerta recibida por un responsable ÷ fallas registradas) × 100 | 0 % (las fallas no se detectan, CE0141 H-20) | 100 % | Mensual | Monitoreo y registro de eventos (CloudWatch, SNS y Wazuh) | Área de Infraestructura Tecnológica |

### 2.5 Relación con la vista motivacional

Cada medida de la vista motivacional del CE0142 tiene su indicador en este documento. La tabla también muestra el resultado (RE) y la meta (MT) de la vista a los que corresponde cada medida.

| Medida (vista) | Indicador | Resultado (vista) | Meta (vista) |
|---|---|---|---|
| MD-01 Pedidos registrados en el ERP | U-02 | RE-01 | MT-01 |
| MD-02 Pedidos con despacho cerrado en el ERP | U-03 | RE-01 | MT-01 |
| MD-03 Productos terminados rastreables hasta su lote | V-01 | RE-02 | MT-01 |
| MD-04 Solicitudes de insumos tramitadas en el ERP | U-04 | RE-03 | MT-01 |
| MD-05 Objetivos del BSC con seguimiento | U-05 | RE-04 | MT-02 |
| MD-06 Respaldo verificado | C-03 | RE-05 | MT-03 |
| MD-07 Cuentas con permisos solo por rol | C-06 | RE-06 | MT-03 |
| MD-08 Disponibilidad del ERP | C-01 | RE-07 | MT-04 |
| MD-09 Fallas avisadas a un responsable | C-07 | RE-08 | MT-04 |
| MD-10 Clientes con cuenta verificada | U-06 | RE-09 | MT-05 |

## 3. Seguimiento

| Pregunta | Respuesta |
|---|---|
| ¿Quién revisa? | Cada mes, el Jefe de TI con las jefaturas de Ventas, Almacén y Logística y Gestión Estratégica. Cada 3 meses, la Jefatura de Gestión Estratégica consolida los resultados en el cuadro de mando del ERP. |
| ¿Cada cuánto? | Mensual, como propone el E1 (estrategia FO E6). Los indicadores semestrales se revisan cuando toca su medición. |
| ¿Cómo se ve si va bien? | Con un semáforo: **verde** cumple la meta, **amarillo** está cerca, **rojo** está lejos de la meta. |
| ¿Qué se hace si no se cumple? | Se busca la causa, se define una acción con un responsable y una fecha, y se revisa en la siguiente reunión. Si el problema es del sistema, se registra como incidencia o como cambio. |
