# CAPÍTULO 4 — CE0144 Plan de Implementación y Gestión del Sistema de Información

El plan de implementación define cómo Franco's ERP pasará del diseño conceptual a la operación diaria de Franco's S.A.C. Para ello, organiza el trabajo en fases con hitos verificables, asigna responsables y recursos, define la estrategia de despliegue y reversión y define los mecanismos de gestión del cambio y soporte que acompañarán la adopción del sistema. El plan se construye sobre la línea base aprobada en el Entregable 2 (Project Charter, WBS, cronograma, presupuesto y matriz de riesgos) y sobre la secuencia de iniciativas de mejora priorizadas en el Entregable 3, de modo que lo planificado en la gestión del proyecto coincida con lo que se implementa en el sistema de información.

## 4.1 Fases y cronograma

La implementación corresponde a dos proyectos del Roadmap Tecnológico del Entregable 1 que se ejecutan en paralelo entre el 06/04/2026 y el 30/11/2026: **TI-002**, implementación del sistema ERP para la digitalización de procesos, a cargo del equipo de Desarrollo de Software (SW), y **TI-003**, implementación de la infraestructura tecnológica organizacional, a cargo del equipo de Infraestructura Tecnológica (ITI). Ambos confluyen en el hito H1 del roadmap, previsto para noviembre de 2026: «Base tecnológica operativa: infraestructura organizacional y sistema ERP implementados». Los dos proyectos se relacionan por dependencia: TI-003 provee los ambientes de pruebas y de producción (servidor H3 en la sede y servicios AWS) sobre los cuales se construye y despliega TI-002, por lo que el avance de la infraestructura condiciona las fases de pruebas y despliegue del sistema.

El trabajo se organiza en siete fases comunes a ambos proyectos y una fase transversal de monitoreo y control. En cada fase, TI-002 y TI-003 desarrollan actividades propias que se coordinan bajo la dirección del Líder del proyecto, y la fase solo se cierra cuando se cumple su hito, como se muestra en la Tabla 1. Al término de la implementación, ambos proyectos continúan con ocho meses de soporte, lo que completa el horizonte de dieciséis meses considerado en la evaluación económica.

**Tabla 1.** Fases y cronograma de TI-002 y TI-003

| Fase | Fechas | TI-002 Sistema ERP (equipo SW) | TI-003 Infraestructura (equipo ITI) | Hito / criterio de cierre |
|---|---|---|---|---|
| F-01 Inicio y planificación | 06/04 – 05/05/2026 | Project Charter, plan de gestión y backlog inicial. | Revisión de la infraestructura actual (hallazgos H-12 a H-21) y definición del ambiente dedicado al ERP. | Project Charter y plan de gestión aprobados. |
| F-02 Análisis | 06/05 – 25/06/2026 | Requisitos funcionales y no funcionales (SRS) y priorización del backlog. | Requisitos de infraestructura: disponibilidad, respaldo, segmentación de red, redundancia y monitoreo. | SRS validado con Franco's S.A.C. y backlog priorizado. |
| F-03 Diseño | 25/05 – 25/06/2026 | Arquitectura C4, modelo de base de datos y prototipos. | Diseño del ambiente híbrido (servidor H3 en sede y AWS), de la red segmentada y del esquema de respaldo y recuperación. | Arquitectura, modelo de datos y prototipos aprobados. |
| F-04 Construcción | 06/07 – 23/10/2026 | Ocho sprints que desarrollan los once módulos (detalle en la Tabla 2). | Instalación del servidor H3 con VMware ESXi, configuración de servicios AWS, red y seguridad, y ambiente de pruebas en contenedores Docker. | Once módulos funcionales con pruebas unitarias aprobadas. |
| F-05 Calidad y pruebas | 12/10 – 04/11/2026 | Pruebas unitarias, de integración y de aceptación (UAT). | Pruebas de respaldo y restauración, de conmutación ante fallas y de seguridad; pipeline CI/CD. | ≥ 90 % de casos de prueba aprobados y pipeline CI/CD configurado. |
| F-06 Despliegue | 02/11 – 27/11/2026 | Puesta en producción de los Portales A y B. | Ambiente de producción operativo, con monitoreo y alertas activos. | Sistema en producción con disponibilidad ≥ 95 %. |
| F-07 Cierre | 27/11 – 30/11/2026 | Acta de aceptación, manuales e informe de cierre. | Manual técnico de infraestructura y reporte de disponibilidad. | Acta de aceptación firmada; hito H1 del roadmap alcanzado. |
| F-08 Monitoreo y control | 05/05 – 27/11/2026 | Seguimiento semanal del avance de los sprints. | Seguimiento de consumo, disponibilidad y costos de la infraestructura. | Informes semanales y reporte quincenal al asesor. |
| Soporte | 01/12/2026 – 31/07/2027 | Corrección de incidencias y mejoras menores. | Mantenimiento, monitoreo y respaldos del ambiente. | Disponibilidad ≥ 95 % durante el soporte. |

La fase de construcción se desarrolla bajo Scrum adaptado, en ocho sprints de dos semanas. Cada sprint entrega un incremento funcional vinculado a las iniciativas de mejora del Entregable 3, lo que permite que el sistema crezca en el mismo orden de prioridad con que se rediseñaron los procesos. La Tabla 2 presenta la secuencia.

**Tabla 2.** Secuencia de sprints de la fase de construcción

| Sprint | Fechas | Incremento funcional | Iniciativas (E3) |
|---|---|---|---|
| 1 | 06/07 – 17/07 | Núcleo transaccional del Portal A: autenticación interna, clientes, productos, ciclo de pedidos y pagos, y control de stock de insumos y productos terminados. | IM-02, IM-05 |
| 2 | 20/07 – 31/07 | Gestión estratégica del negocio (BSC): plan y mapa estratégico, KPI e iniciativas con tablero de control. | Gestión estratégica |
| 3 | 03/08 – 14/08 | Gestión estratégica de TI: mapa estratégico, KPI e iniciativas alineados al negocio. | Gestión estratégica TI |
| 4 | 17/08 – 28/08 | Portal B (cliente): autenticación, catálogo, carrito, creación de pedido y pago en línea; configuración base. | IM-01 |
| 5 | 31/08 – 11/09 | Cierre del ciclo de venta con emisión de comprobantes internos y operación de almacén: descuento de inventario y registro de entregas. | IM-01, IM-06 |
| 6 | 14/09 – 25/09 | Trazabilidad entre almacén y producción: solicitudes de insumos y de producción, pedidos en backoffice y notificaciones al cliente. | IM-02, IM-03 |
| 7 | 28/09 – 09/10 | Configuración y backoffice: parámetros del sistema, usuarios internos y flujo pendiente de carrito y pedido del Portal B. | IM-04, IM-05 |
| 8 | 12/10 – 23/10 | Perfil y seguridad de cuenta en ambos portales: datos personales, cambio de contraseña y recuperación de acceso. | Transversal |

La secuencia prioriza primero el núcleo transaccional, porque sobre él se apoyan los demás módulos: no es posible tramitar solicitudes de producción ni medir indicadores sin ventas e inventario registrados en una sola base. Los módulos orientados al cliente se habilitan a partir del sprint 4, cuando el registro interno ya es estable, y los aspectos de seguridad de cuenta se consolidan al final, antes de las pruebas de aceptación.

## 4.2 Responsables y recursos

La implementación involucra a los diez integrantes del equipo del proyecto y a dos actores de Franco's S.A.C.: la Gerencia, como patrocinador, y los usuarios clave de ventas e inventario, que validan los requisitos y participan en las pruebas de aceptación. La Tabla 3 asigna las responsabilidades de cada fase mediante una matriz RACI, en la que R identifica a quien ejecuta la actividad, A a quien la aprueba y rinde cuentas, C a quien se consulta e I a quien se informa; cada actividad tiene un único responsable de aprobación.

**Tabla 3.** Matriz RACI de la implementación

| Fase / actividad | Director | Analista | Backend (×2) | DBA y Frontend | Frontend | Diseño y QA | QA y Doc. | Despliegue (×2) | Gerencia | Usuarios clave |
|---|---|---|---|---|---|---|---|---|---|---|
| Inicio y planificación | A/R | C | I | I | I | I | R | I | C | — |
| Análisis | A | R | C | C | I | C | C | I | C | C |
| Diseño | A | C | R | R | C | R | I | C | I | C |
| Construcción | A | C | R | R | R | C | I | C | I | I |
| Calidad y pruebas | A | C | C | C | C | R | R | C | I | C |
| Despliegue | A | I | C | R | C | C | I | R | C | I |
| Capacitación de usuarios | A | R | I | I | I | C | R | C | C | C |
| Cierre | A/R | I | I | I | I | I | R | I | C | — |
| Soporte post-implementación | A | C | C | C | C | I | C | R | I | C |
| Control de cambios (transversal) | A | R | C | C | C | I | R | C | C | — |

En cuanto a los recursos, el proyecto dispone del presupuesto aprobado en el Entregable 2 y de un conjunto de recursos tecnológicos con responsables definidos. Los integrantes del equipo constituyen el recurso humano del desarrollo; los costos de recursos humanos presupuestados corresponden a los especialistas de apoyo (cloud, desarrollo y base de datos). La Tabla 4 resume los recursos y su control.

**Tabla 4.** Recursos de la implementación

| Tipo | Recurso | Responsable | Uso / control | Costo (S/) |
|---|---|---|---|---|
| Infraestructura | Servidor H3 en sede (backend del ERP) | Especialistas de despliegue | Disponibilidad, configuración, respaldos y capacidad. | 6,750.00 |
| Infraestructura | VMware ESXi (servidor H3) y servicios AWS (frontend y recuperación) | Especialistas de despliegue | Consumo, disponibilidad, alertas y costos mensuales. | 20,670.00 |
| Humano | Especialista cloud, desarrollador y DBA de apoyo | Director del proyecto | Asignación por fase y seguimiento en el tablero. | 2,550.00 |
| Servicio | Soporte técnico (8 meses × S/ 2,000) | Especialistas de despliegue | Atención de incidencias y mantenimiento. | 16,000.00 |
| Software | PostgreSQL | DBA | Accesos, integridad, copias de seguridad y recuperación. | — |
| Software | NATS y API Gateway | Backend y despliegue | Configuración, pruebas de integración y monitoreo. | — |
| Gestión | GitHub, Jira y Figma | Desarrolladores, Director y Diseñadora | Control de versiones, backlog y prototipos. | — |
| | **Costo total del proyecto** | | | **45,970.00** |

## 4.3 Despliegue y reversión

## 4.4 Gestión del cambio y soporte

La gestión del cambio comprende tres frentes: el control de los riesgos de la implementación, la gobernanza que asegura que lo construido corresponda a lo aprobado y la adopción del sistema por parte del personal. A ellos se suma el soporte post-implementación, que sostiene la operación una vez cerrado el proyecto.

**Riesgos de la implementación.** De la matriz de riesgos del Entregable 2 se seleccionaron los que afectan directamente al despliegue y la adopción del sistema. La Tabla 5 los presenta con su respuesta.

**Tabla 5.** Riesgos de la implementación y respuesta

| ID | Riesgo | Prob. | Impacto | Respuesta | Responsable |
|---|---|---|---|---|---|
| R-01 | Cambios frecuentes de requisitos | 70 % | Alto | Procedimiento formal de control y aprobación de cambios. | Director del proyecto |
| R-02 | Retrasos en el desarrollo de los sprints | 50 % | Alto | Seguimiento semanal, priorización del backlog y reasignación de recursos. | Director / desarrolladores |
| R-03 | Incremento de ciberamenazas | 50 % | Alto | Control de acceso por rol, actualizaciones, respaldos y monitoreo de incidentes. | Equipo de infraestructura |
| R-04 | Problemas de integración entre Software e Infraestructura | 45 % | Medio | Plan de integración y pruebas técnicas anticipadas. | Director del proyecto |
| R-05 | Resistencia al cambio de los usuarios | 45 % | Medio | Capacitación por rol y acompañamiento durante el despliegue. | QA y Documentadora |
| R-07 | Incumplimiento de la Ley N.° 29733 | 30 % | Alto | Protección de datos desde el diseño y verificación en UAT. | Analista / desarrollador |
| R-08 | Fallas en la infraestructura cloud (AWS) | 25 % | Medio | Respaldos, monitoreo y plan de recuperación. | Especialistas de despliegue |

**Gobernanza de la implementación.** Ningún cambio en el alcance, el cronograma o el presupuesto se incorpora sin seguir el proceso formal del Entregable 2: solicitud, evaluación de impacto, aprobación del Director y del asesor, implementación y cierre con actualización de la línea base. El Director revisa semanalmente el avance de cada rol e informa al asesor académico de forma quincenal.

**Adopción del sistema.** Para reducir la resistencia al cambio (R-05), la capacitación se organiza por rol y se realiza antes de la puesta en producción, de modo que cada usuario aprenda únicamente las funciones que utilizará. La Tabla 6 resume el plan.

**Tabla 6.** Capacitación por rol

| Rol del sistema | Contenido | Momento |
|---|---|---|
| Operador de ventas | Registro de pedidos, clientes, catálogo y estados de venta. | Antes de la puesta en producción (F-06) |
| Operador de inventario | Movimientos de stock, almacenes, alertas de stock mínimo y solicitudes. | Antes de la puesta en producción (F-06) |
| Gerente | Consulta de reportes, pedidos y tablero BSC. | Durante la puesta en producción (F-06) |
| Analista estratégico | Registro de objetivos, KPI e iniciativas del BSC. | Durante la puesta en producción (F-06) |
| Administrador | Usuarios, roles, parámetros y configuración del sistema. | Antes de la puesta en producción (F-06) |
| Cliente | Guía breve en el Portal B para registro, compra y seguimiento de pedidos. | Durante la puesta en producción (F-06) |

Esta capacitación inicial cubre el uso del sistema en el arranque. La formación digital más amplia del personal queda a cargo del programa de transformación y capacitación digital (TI-005) previsto en el Roadmap Tecnológico del Entregable 1 para 2027.

**Soporte post-implementación.** Tras el cierre, el sistema cuenta con ocho meses de soporte técnico a cargo de los especialistas de despliegue, con un costo de S/ 2,000 mensuales. El soporte se organiza según las prácticas de ITIL 4: los usuarios reportan las incidencias por un canal único, estas se registran y clasifican por prioridad, y se atienden en el orden que muestra la Tabla 7. Los tiempos son una propuesta del equipo y se validarán con la Gerencia.

**Tabla 7.** Prioridades de atención en el soporte (propuesta)

| Prioridad | Ejemplo | Atención propuesta |
|---|---|---|
| Crítica | El sistema no permite registrar ventas o inventario. | Inicio inmediato; solución en el mismo día. |
| Alta | Falla en un módulo con alternativa temporal. | Dentro de las 24 horas. |
| Media | Error que no detiene la operación. | Dentro de las 72 horas. |
| Baja | Consulta de uso o mejora menor. | Se programa en el siguiente mantenimiento. |

Durante este periodo se mantienen el monitoreo de disponibilidad y los respaldos periódicos, y se registra la disponibilidad mensual para verificar la meta del 95 %. Las incidencias recurrentes y las mejoras solicitadas se canalizan mediante el proceso de control de cambios, lo que conecta el soporte con el seguimiento de indicadores que se desarrolla en el capítulo 5.
