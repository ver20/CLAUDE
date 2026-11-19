# CAPÍTULO 5 — CE0145 Indicadores de Uso, Valor y Mejora del Sistema de Información

Los indicadores permiten comprobar si Franco's ERP cumple el propósito para el que fue diseñado: que la información operativa deje el papel y las hojas de cálculo, que esa información genere valor para la organización y que el sistema se mantenga disponible, seguro y en mejora continua. Para ello, este capítulo define un conjunto de indicadores organizados en tres tipos, establece para cada uno su fórmula, línea base, meta y frecuencia de medición, y describe el mecanismo con el que se les dará seguimiento. Los indicadores parten de las medidas definidas en la vista motivacional del CE0142 (MD-01 a MD-10) y se complementan con los criterios de éxito del Entregable 2 y con el indicador del objetivo OET-03 en el tablero de control del Entregable 1.

## 5.1 Tabla de indicadores

Los indicadores se agrupan en tres tipos. Los indicadores de **uso** miden si el personal y los clientes efectivamente registran su información en el ERP, en lugar de hacerlo en papel o en Excel. Los indicadores de **valor** miden el beneficio que el sistema genera para el negocio. Los indicadores de **mejora** miden la calidad con que el sistema opera y se sostiene en el tiempo, y son la base para detectar oportunidades de mejora continua. La Tabla 1 presenta el conjunto completo y su relación con las metas y objetivos de la vista motivacional.

**Tabla 1.** Indicadores de uso, valor y mejora de Franco's ERP

| Código | Indicador | Tipo | Medida (CE0142) | Meta u objetivo al que responde |
|---|---|---|---|---|
| U-01 | Pedidos registrados en el ERP | Uso | MD-01 | MT-01 |
| U-02 | Pedidos con despacho cerrado en el ERP | Uso | MD-02 | MT-01 |
| U-03 | Solicitudes de insumos tramitadas en el ERP | Uso | MD-04 | MT-01 |
| U-04 | Objetivos del BSC con seguimiento | Uso | MD-05 | MT-02 |
| U-05 | Clientes con cuenta verificada | Uso | MD-10 | MT-05 |
| V-01 | Productos terminados rastreables hasta su lote | Valor | MD-03 | MT-01 |
| V-02 | Procesos digitalizados | Valor | — | OET-03 |
| V-03 | Reducción de quiebres de stock | Valor | — | OEN-03 |
| V-04 | Satisfacción de los usuarios | Valor | — | OEN-03 |
| V-05 | Retorno sobre la inversión (ROI) | Valor | — | OEN-03 |
| M-01 | Disponibilidad del ERP | Mejora | MD-08 | MT-04 |
| M-02 | Tiempo de respuesta del sistema | Mejora | — | MT-04 |
| M-03 | Respaldo verificado | Mejora | MD-06 | MT-03 |
| M-04 | Fallas avisadas a un responsable | Mejora | MD-09 | MT-04 |
| M-05 | Cuentas con permisos solo por rol | Mejora | MD-07 | MT-03 |
| M-06 | Incidencias atendidas a tiempo | Mejora | — | MT-04 |

Los indicadores de uso son los primeros en mostrar resultados, porque reflejan la adopción del sistema desde la puesta en producción. Los de valor requieren un periodo de operación más largo, ya que dependen de que el registro en el ERP se haya consolidado. Los de mejora se miden de forma continua desde el primer día y alertan sobre cualquier condición que ponga en riesgo la operación.

## 5.2 Fórmula, línea base, meta y frecuencia

Cada indicador se define con su fórmula de cálculo, la línea base que corresponde a la situación actual (AS-IS) descrita en el CE0141, la meta que se espera alcanzar, la frecuencia con que se mide y la fuente de la que se obtiene el dato. Dado que hoy la información de ventas, inventario e insumos no se registra en ningún sistema, la línea base de la mayoría de los indicadores de uso es 0 %. La columna «Origen de la meta» distingue las metas que ya fueron aprobadas en entregables anteriores de las que propone el equipo en este capítulo, que deberán validarse con los usuarios clave de Franco's S.A.C. La Tabla 2 presenta los indicadores de uso.

**Tabla 2.** Ficha de los indicadores de uso

| Código | Fórmula | Línea base (AS-IS) | Meta | Origen de la meta | Frecuencia | Fuente del dato |
|---|---|---|---|---|---|---|
| U-01 | (Ventas registradas en el ERP ÷ comprobantes emitidos en SICO ERP en el periodo) × 100 | 0 %: las ventas se anotan en papel y Excel | ≥ 95 % | Propuesta | Mensual | Módulo de ventas; SICO ERP |
| U-02 | (Pedidos en estado «entregado» ÷ pedidos despachados en el periodo) × 100 | 0 %: la distribución se anota en papel | ≥ 95 % | Propuesta | Mensual | Módulo de despacho |
| U-03 | (Solicitudes de insumos registradas en el ERP ÷ solicitudes de insumos del periodo) × 100 | 0 %: las solicitudes se hacen en papel | ≥ 90 % | Propuesta | Mensual | Módulo de producción e inventario de insumos |
| U-04 | (Objetivos de negocio y de TI con al menos un KPI medido ÷ objetivos registrados) × 100 | 0 %: no existe seguimiento de la estrategia | 100 % | Propuesta | Trimestral | Módulo de estrategia (BSC) |
| U-05 | (Clientes con correo verificado ÷ clientes registrados en el Portal B) × 100 | No existe canal de venta en línea | ≥ 90 % | Propuesta | Mensual | Módulo de autenticación y personas |

Los indicadores de valor se presentan en la Tabla 3. En este grupo, las metas de V-02 a V-05 provienen del tablero de control del Entregable 1 y de los criterios de éxito del Entregable 2, por lo que mantienen la coherencia con la evaluación económica y estratégica del proyecto.

**Tabla 3.** Ficha de los indicadores de valor

| Código | Fórmula | Línea base (AS-IS) | Meta | Origen de la meta | Frecuencia | Fuente del dato |
|---|---|---|---|---|---|---|
| V-01 | (Productos terminados con lote registrado ÷ productos terminados en stock) × 100 | 0 %: los lotes envasados se llevan en un archivo de Excel aparte | 100 % | Propuesta | Mensual | Módulo de inventario |
| V-02 | (Procesos digitalizados ÷ procesos identificados) × 100 | Ningún proceso operativo digitalizado | ≥ 80 % | E1, tablero BSC (OET-03) | Mensual | Mapa de procesos y módulos del ERP |
| V-03 | ((Quiebres de stock antes − quiebres de stock después) ÷ quiebres de stock antes) × 100 | Quiebres registrados de forma manual en el mes previo a la puesta en producción | Reducción ≥ 50 % en los primeros 3 meses de uso | E2, criterio IE-05 | Mensual | Alertas de stock mínimo del módulo de inventario |
| V-04 | (Usuarios satisfechos ÷ usuarios encuestados) × 100 | Sin medición | ≥ 80 % | E2, criterio IE-04 | Al cierre de la UAT y semestral | Encuesta de satisfacción |
| V-05 | ((Beneficios acumulados − inversión) ÷ inversión) × 100 | Inversión total de S/ 45,970 | ROI ≥ 60 % y recuperación de la inversión en el mes 14 | E2, criterios IE-06 e IE-07 | Trimestral, con cierre en el mes 16 | Flujo de caja del proyecto |

Por último, la Tabla 4 presenta los indicadores de mejora, que miden la calidad del servicio del sistema. Sus fuentes de datos corresponden a los mecanismos de monitoreo y respaldo definidos en la arquitectura del CE0142.

**Tabla 4.** Ficha de los indicadores de mejora

| Código | Fórmula | Línea base (AS-IS) | Meta | Origen de la meta | Frecuencia | Fuente del dato |
|---|---|---|---|---|---|---|
| M-01 | (Tiempo en servicio ÷ tiempo del periodo en horario operativo) × 100 | No se puede medir: no hay redundancia ni monitoreo | ≥ 95 % | E2, criterio IE-01 | Mensual | Sonda de conexión y alarmas de CloudWatch; monitoreo de la sede |
| M-02 | (Peticiones respondidas en 2 s o menos ÷ peticiones totales) × 100 | No aplica: no existe sistema | ≥ 95 % | E2, criterio IE-02 | Mensual | Métricas del balanceador y del backend |
| M-03 | (Respaldos diarios completados ÷ días del periodo) × 100, más una prueba de restauración exitosa | Sin respaldo de la información | 100 % de respaldos y una restauración exitosa por mes | Propuesta | Diaria (respaldo) y mensual (restauración) | Bucket de respaldos en S3 y base en espera de la sede |
| M-04 | (Fallas con alerta recibida por un responsable ÷ fallas registradas) × 100 | 0 %: las fallas no se detectan | 100 % | Propuesta | Mensual | Monitoreo y registro central de eventos (CloudWatch, SNS y Wazuh) |
| M-05 | (Cuentas activas cuyos permisos provienen solo de su rol ÷ cuentas activas) × 100 | No existe control de acceso | 100 % | E2, objetivo OPR-07 | Mensual | Módulo de usuarios y roles |
| M-06 | (Incidencias atendidas dentro del tiempo de su prioridad ÷ incidencias registradas) × 100 | No existe registro de incidencias | ≥ 90 % | Propuesta | Mensual | Registro de incidencias del soporte |

## 5.3 Seguimiento

El seguimiento de los indicadores aprovecha el propio sistema: el módulo de estrategia de Franco's ERP, que implementa el cuadro de mando integral, se utiliza como tablero de control para registrar los valores de cada indicador y compararlos con su meta. De esta manera, la organización mide el sistema con el mismo sistema, y el indicador U-04 refleja a la vez el uso del módulo de estrategia. Cada indicador tiene un responsable de medirlo y un rol que lo revisa, como se muestra en la Tabla 5.

**Tabla 5.** Responsables y mecanismo de seguimiento

| Indicadores | Responsable de la medición | Herramienta | Revisión |
|---|---|---|---|
| U-01, U-02 | A1 Operador de Ventas y A5 Operador de Despacho | Reportes del módulo de ventas y despacho | Mensual, por el A6 Analista Estratégico |
| U-03, V-01, V-03 | A2 Operador de Inventarios y A3 Operador de Insumos | Reportes del módulo de inventario y alertas de stock mínimo | Mensual, por el A6 Analista Estratégico |
| U-04, V-02 | A6 Analista Estratégico | Módulo de estrategia (BSC) | Trimestral, con el Director del proyecto |
| U-05 | A7 Administrador | Módulo de autenticación y personas | Mensual, por el A6 Analista Estratégico |
| V-04, V-05 | Director del proyecto | Encuesta de satisfacción y flujo de caja | Al cierre de la UAT y trimestral |
| M-01 a M-04 | Equipo de infraestructura | CloudWatch, sonda de conexión, SNS, Wazuh y respaldos en S3 | Mensual, en el informe de disponibilidad |
| M-05 | A7 Administrador | Módulo de usuarios y roles | Mensual |
| M-06 | Equipo de infraestructura | Registro de incidencias del soporte | Mensual, en el informe de soporte |

Para facilitar la lectura del tablero, cada indicador se clasifica con un semáforo, siguiendo el mismo criterio del tablero de control del Entregable 1. La Tabla 6 define los rangos y la acción que corresponde a cada estado.

**Tabla 6.** Semáforo de los indicadores

| Estado | Condición | Acción |
|---|---|---|
| Verde | El valor alcanza o supera la meta. | Se mantiene la operación y se registra el resultado en el tablero. |
| Ámbar | El valor está por debajo de la meta en hasta 10 puntos porcentuales. | El responsable analiza la causa y propone una acción correctiva antes de la siguiente medición. |
| Rojo | El valor está por debajo de la meta en más de 10 puntos porcentuales, o la tendencia baja en dos mediciones seguidas. | Se registra una incidencia o una solicitud de cambio y se trata en el proceso de control de cambios del capítulo 4. |

El seguimiento se organiza como un ciclo de mejora continua, alineado con la práctica de mejora continua de ITIL 4. En cada periodo se **mide** el valor de los indicadores desde sus fuentes; se **analiza** su estado en el semáforo y la tendencia respecto de las mediciones anteriores; se **actúa** sobre los indicadores en ámbar o rojo mediante acciones correctivas, incidencias o solicitudes de cambio; y se **verifica** en la siguiente medición si la acción tuvo efecto. Durante los ocho meses de soporte post-implementación, este ciclo se revisa en una reunión mensual entre el Director del proyecto, el equipo de infraestructura y el Analista Estratégico. Al término del soporte, el seguimiento continúa a cargo de la Jefatura de Gestión Estratégica, y los resultados alimentan las siguientes iniciativas del Roadmap Tecnológico, como la estandarización de procesos con BPM (TI-004) y el programa de capacitación digital (TI-005).
