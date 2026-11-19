# CAPÍTULO 4 — CE0144 Plan de Implementación y Gestión del Sistema de Información

El plan de implementación define cómo Franco's ERP pasará del diseño conceptual a la operación diaria de Franco's S.A.C. Para ello, organiza el trabajo en fases con hitos verificables, asigna responsables y recursos, define la estrategia de despliegue y reversión, y establece los mecanismos de gestión del cambio y soporte que acompañarán la adopción del sistema. El plan se construye sobre la línea base aprobada en el Entregable 2 (Project Charter, WBS, cronograma, presupuesto y matriz de riesgos), sobre la secuencia de iniciativas de mejora priorizadas en el Entregable 3 y sobre la arquitectura definida en el CE0142, de modo que lo planificado en la gestión del proyecto coincida con lo que se construye en el software y en la infraestructura.

## 4.1 Fases y cronograma

La implementación corresponde a dos proyectos del Roadmap Tecnológico del Entregable 1 que se ejecutan en paralelo entre el 06/04/2026 y el 30/11/2026 y que atienden el objetivo de TI OET-03 y, a través de él, el objetivo organizacional OEN-03. **TI-002**, implementación del ERP para la digitalización de procesos, está a cargo del equipo de Desarrollo de Software (SW) y comprende el backend, los dos portales y la base de datos. **TI-003**, implementación de la infraestructura tecnológica, está a cargo del equipo de Infraestructura Tecnológica (ITI) y comprende la nube, la red de la sede, el respaldo, la continuidad y el monitoreo. Ambos confluyen en el hito H1 del roadmap, previsto para noviembre de 2026: «Base tecnológica operativa: infraestructura organizacional y sistema ERP implementados».

Los dos proyectos dependen entre sí. TI-003 provee el ambiente en el que corre TI-002: la base de datos de producción se aloja en la sede, en dos máquinas virtuales (primaria y en espera), mientras que el backend y los portales se ejecutan en AWS y se comunican con la sede mediante una VPN. Por ello, la red de la sede y el enlace con la nube deben estar operativos antes de las pruebas integrales y de la puesta en producción del sistema.

El trabajo se organiza en siete fases comunes a ambos proyectos y una fase transversal de monitoreo y control. En cada fase, TI-002 y TI-003 desarrollan actividades propias que se coordinan bajo la dirección del Líder del proyecto, y la fase solo se cierra cuando se cumple su hito, como se muestra en la Tabla 1. Al término de la implementación, ambos proyectos continúan con ocho meses de soporte, lo que completa el horizonte de dieciséis meses considerado en la evaluación económica.

**Tabla 1.** Fases y cronograma de TI-002 y TI-003

| Fase | Fechas | TI-002 Sistema ERP (equipo SW) | TI-003 Infraestructura (equipo ITI) | Hito / criterio de cierre |
|---|---|---|---|---|
| F-01 Inicio y planificación | 06/04 – 05/05/2026 | Project Charter, plan de gestión y backlog inicial. | Revisión de la infraestructura actual y de las brechas tecnológicas B-08 a B-12. | Project Charter y plan de gestión aprobados. |
| F-02 Análisis | 06/05 – 25/06/2026 | Requisitos funcionales y no funcionales (SRS), actores del sistema y priorización del backlog. | Requisitos de infraestructura: alojamiento, redundancia, segmentación, respaldo y monitoreo. | SRS validado con Franco's S.A.C. y backlog priorizado. |
| F-03 Diseño | 25/05 – 25/06/2026 | Arquitectura del monolito modular con Clean Architecture, modelo de datos en PostgreSQL con esquemas por dominio y prototipos de los Portales A y B. | Diseño del esquema sede–nube: datos en la sede, cómputo en AWS, red en VLAN, VPN IPsec, respaldo diario y recuperación con base temporal en la nube. | Arquitectura, modelo de datos y prototipos aprobados. |
| F-04 Construcción | 06/07 – 23/10/2026 | Ocho sprints que desarrollan los módulos del sistema (detalle en la Tabla 2). | Sede: firewalls pfSense en par, switches en stack con VLAN, dos proveedores de internet y base de datos primaria y en espera sobre VMware. Nube: VPC, VPN, ECS Fargate, CloudFront y S3, WAF, ALB y Secrets Manager. | Módulos funcionales con pruebas unitarias aprobadas. |
| F-05 Calidad y pruebas | 12/10 – 04/11/2026 | Pruebas unitarias, de extremo a extremo y de aceptación (UAT); integración continua que bloquea cada cambio si fallan la compilación, el lint o las pruebas. | Pruebas de restauración desde el respaldo, de conmutación a la base en espera, de recuperación con la base temporal en la nube y de seguridad del WAF. | ≥ 90 % de casos de prueba aprobados y pipeline CI/CD configurado. |
| F-06 Despliegue | 02/11 – 27/11/2026 | Puesta en producción de los Portales A y B y del backend. | Ambiente de producción operativo, con monitoreo y alertas activos. | Sistema en producción con disponibilidad ≥ 95 %. |
| F-07 Cierre | 27/11 – 30/11/2026 | Acta de aceptación, manuales e informe de cierre. | Manual técnico de infraestructura y reporte de disponibilidad. | Acta de aceptación firmada; hito H1 del roadmap alcanzado. |
| F-08 Monitoreo y control | 05/05 – 27/11/2026 | Seguimiento semanal del avance de los sprints. | Seguimiento de disponibilidad y del gasto en AWS frente al presupuesto mensual. | Informes semanales y reporte quincenal al asesor. |
| Soporte | 01/12/2026 – 31/07/2027 | Corrección de incidencias y mejoras menores. | Mantenimiento, monitoreo, respaldos y control de costos del ambiente. | Disponibilidad ≥ 95 % durante el soporte. |

La fase de construcción se desarrolla bajo Scrum adaptado, en ocho sprints de dos semanas. Cada sprint entrega un incremento funcional vinculado a las iniciativas de mejora del Entregable 3, lo que permite que el sistema crezca en el mismo orden de prioridad con que se rediseñaron los procesos. La Tabla 2 presenta la secuencia.

**Tabla 2.** Secuencia de sprints de la fase de construcción

| Sprint | Fechas | Incremento funcional | Iniciativas (E3) |
|---|---|---|---|
| 1 | 06/07 – 17/07 | Núcleo transaccional del Portal A: autenticación interna, clientes, productos, ciclo de pedidos y pagos, y control de stock de insumos y productos terminados. | IM-02, IM-05 |
| 2 | 20/07 – 31/07 | Gestión estratégica del negocio: plan y mapa estratégico, KPI e iniciativas con tablero de control. | Gestión estratégica |
| 3 | 03/08 – 14/08 | Gestión estratégica de TI: mapa estratégico, KPI e iniciativas alineados al negocio. | Gestión estratégica TI |
| 4 | 17/08 – 28/08 | Portal B (tienda en línea): registro y verificación del cliente, catálogo, carrito y creación de pedido; configuración base. | IM-01 |
| 5 | 31/08 – 11/09 | Cierre del ciclo de venta y operación de almacén: descuento de inventario y registro de entregas. | IM-01, IM-06 |
| 6 | 14/09 – 25/09 | Trazabilidad entre almacén y producción: solicitudes de insumos y de producción, pedidos en backoffice y notificaciones al cliente. | IM-02, IM-03 |
| 7 | 28/09 – 09/10 | Configuración y backoffice: parámetros del sistema, usuarios internos y flujo pendiente de carrito y pedido del Portal B. | IM-04, IM-05 |
| 8 | 12/10 – 23/10 | Perfil y seguridad de cuenta en ambos portales: datos personales, cambio de contraseña y recuperación de acceso. | Transversal |

La secuencia prioriza primero el núcleo transaccional, porque sobre él se apoyan los demás módulos: no es posible tramitar solicitudes de producción ni medir indicadores sin ventas e inventario registrados en una sola base. Los módulos orientados al cliente se habilitan a partir del sprint 4, cuando el registro interno ya es estable, y los aspectos de seguridad de cuenta se consolidan al final, antes de las pruebas de aceptación.

## 4.2 Responsables y recursos

La implementación involucra a los integrantes de los equipos de Software e Infraestructura y a los usuarios clave de Franco's S.A.C. de las áreas de ventas, inventarios, insumos, producción y despacho, que validan los requisitos y participan en las pruebas de aceptación. La Tabla 3 asigna las responsabilidades de cada fase mediante una matriz RACI, en la que R identifica a quien ejecuta la actividad, A a quien la aprueba y rinde cuentas, C a quien se consulta e I a quien se informa; cada actividad tiene un único responsable de aprobación.

**Tabla 3.** Matriz RACI de la implementación

| Fase / actividad | Director | Analista | Backend (×2) | DBA y Frontend | Frontend | Diseño y QA | QA y Doc. | Infraestructura (×2) | Usuarios clave |
|---|---|---|---|---|---|---|---|---|---|
| Inicio y planificación | A/R | C | I | I | I | I | R | I | — |
| Análisis | A | R | C | C | I | C | C | C | C |
| Diseño | A | C | R | R | C | R | I | R | C |
| Construcción | A | C | R | R | R | C | I | R | I |
| Calidad y pruebas | A | C | C | C | C | R | R | R | C |
| Despliegue | A | I | C | R | C | C | I | R | I |
| Capacitación de usuarios | A | R | I | I | I | C | R | I | C |
| Cierre | A/R | I | I | I | I | I | R | C | C |
| Soporte post-implementación | A | C | C | C | C | I | C | R | C |
| Control de cambios (transversal) | A | R | C | C | C | I | R | C | — |

En cuanto a los recursos, el proyecto dispone del presupuesto aprobado en el Entregable 2 y de los componentes tecnológicos definidos en el CE0142, cada uno con un responsable. Los componentes de la sede aprovechan los equipos disponibles en el laboratorio de la universidad, y los servicios de AWS se controlan con un presupuesto mensual de 80 USD, con avisos al 50, 80 y 100 % del gasto. La Tabla 4 resume los recursos y su control.

**Tabla 4.** Recursos de la implementación

| Tipo | Recurso | Responsable | Uso / control | Costo (S/) |
|---|---|---|---|---|
| Infraestructura (sede) | Servidor con hipervisor VMware para las máquinas virtuales de la base de datos (primaria y en espera) | Equipo de infraestructura | Disponibilidad, réplica y capacidad. | 6,750.00 |
| Infraestructura (sede y nube) | Licenciamiento VMware y servicios AWS: CloudFront, S3, WAF, ALB, ECS Fargate, ECR, Secrets Manager, VPC y VPN | Equipo de infraestructura | Consumo, disponibilidad y alertas de presupuesto (AWS Budgets). | 20,670.00 |
| Humano | Especialista cloud, desarrollador y DBA de apoyo | Director del proyecto | Asignación por fase y seguimiento en el tablero. | 2,550.00 |
| Servicio | Soporte técnico (8 meses × S/ 2,000) | Equipo de infraestructura | Atención de incidencias y mantenimiento. | 16,000.00 |
| Red (sede) | Firewalls pfSense en par, switches Cisco C9300L en stack y dos proveedores de internet (Claro y Movistar) | Equipo de infraestructura | Segmentación en VLAN, redundancia de enlace y túneles IPsec hacia AWS. | — |
| Datos | PostgreSQL 17 con Prisma; volcado diario a S3 y base temporal en RDS ante desastre | DBA | Accesos, integridad, respaldo fuera de la sede y recuperación. | — |
| Monitoreo | CloudWatch, SNS, Lambda, Step Functions, CloudTrail y Wazuh | Equipo de infraestructura | Detección de la caída de la base, aviso al equipo y registro de actividad. | — |
| Desarrollo | NestJS, Angular, GitHub y GitHub Actions | Equipo de software | Control de versiones, integración continua y despliegue con credenciales temporales. | — |
| Gestión | Jira y Figma | Director y Diseñadora | Backlog, avance y prototipos. | — |
| | **Costo total del proyecto** | | | **45,970.00** |

## 4.3 Despliegue y reversión

## 4.4 Gestión del cambio y soporte

La gestión del cambio comprende tres frentes: el control de los riesgos de la implementación, la gobernanza que asegura que lo construido corresponda a lo aprobado y la adopción del sistema por parte del personal. A ellos se suma el soporte post-implementación, que sostiene la operación una vez cerrado el proyecto.

### 4.4.1 Riesgos de la implementación

De la matriz de riesgos del Entregable 2 se seleccionaron los que afectan directamente al despliegue y la adopción del sistema, y se incorporaron dos riesgos que surgen del diseño del CE0142: la dependencia de SICO ERP, que se mantiene como emisor de comprobantes, y el procesamiento de datos en una región de AWS fuera del país. La Tabla 5 los presenta con su respuesta.

**Tabla 5.** Riesgos de la implementación y respuesta

| ID | Riesgo | Prob. | Impacto | Respuesta | Responsable |
|---|---|---|---|---|---|
| R-01 | Cambios frecuentes de requisitos | 70 % | Alto | Procedimiento formal de control y aprobación de cambios. | Director del proyecto |
| R-02 | Retrasos en el desarrollo de los sprints | 50 % | Alto | Seguimiento semanal, priorización del backlog y reasignación de recursos. | Director / desarrolladores |
| R-03 | Incremento de ciberamenazas | 50 % | Alto | Acceso por rol denegado por defecto, WAF delante de los portales y la API, secretos fuera del código y registro de actividad. | Equipo de infraestructura |
| R-04 | Problemas de integración entre Software e Infraestructura | 45 % | Medio | Plan de integración y pruebas anticipadas de la conexión entre el backend en AWS y la base de la sede. | Director del proyecto |
| R-05 | Resistencia al cambio de los usuarios | 45 % | Medio | Capacitación por rol y acompañamiento durante el despliegue. | QA y Documentadora |
| R-07 | Incumplimiento de la Ley N.° 29733 | 30 % | Alto | Protección de datos desde el diseño, cifrado en tránsito y verificación en UAT; consideración del procesamiento en us-east-1. | Analista / desarrollador |
| R-08 | Fallas en la infraestructura cloud o en la conexión con la sede | 25 % | Medio | Volcado diario a S3, base temporal en RDS restaurable de forma automática y monitoreo con aviso al equipo. | Equipo de infraestructura |
| R-09 | Incremento de costos tecnológicos | 25 % | Bajo | Presupuesto mensual de 80 USD con avisos al 50, 80 y 100 % y revisión mensual del consumo. | Jefatura de Finanzas / Director |
| R-10 | Falla de la PC que ejecuta SICO ERP, que no tiene respaldo y sigue emitiendo los comprobantes | — | Alto | Respaldo periódico de la base de SICO ERP y procedimiento alterno de emisión hasta la integración del ERP con SUNAT. | Equipo de infraestructura / Jefatura de Finanzas |

### 4.4.2 Alcance que queda pendiente

Algunas brechas del CE0141 se atienden solo en parte en esta versión. La Tabla 6 registra lo que queda fuera, para que se gestione en las siguientes versiones del sistema.

**Tabla 6.** Pendientes de las brechas atendidas en parte

| Brecha | Qué cubre esta versión | Qué queda pendiente |
|---|---|---|
| B-03 | Las ventas, el inventario y los lotes envasados pasan del Excel al ERP. | Los documentos de Word no se integran y los archivos históricos no se migran. |
| B-04 | El ERP envía por correo las verificaciones, credenciales y recuperación de contraseña. | WhatsApp no se integra. |
| B-09 | Los datos registrados desde la puesta en marcha tienen respaldo fuera de la sede. | Los datos anteriores en papel, Excel y Word no se respaldan con el ERP. |
| B-14 | Insumos y Producción pasan al ERP. | Compras, Calidad y RR. HH. siguen registrando fuera del sistema. |
| B-02, B-06, B-07 y B-13 | SICO ERP sigue como emisor oficial de comprobantes. | Integración del ERP con SUNAT y retiro de SICO ERP. |

### 4.4.3 Gobernanza de la implementación

Ningún cambio en el alcance, el cronograma o el presupuesto se incorpora sin seguir el proceso formal del Entregable 2: solicitud, evaluación de impacto, aprobación del Director y del asesor, implementación y cierre con actualización de la línea base. El Director revisa semanalmente el avance de cada rol e informa al asesor académico de forma quincenal. En el plano técnico, la integración continua impide incorporar cambios al código si fallan la compilación, el lint o las pruebas, y el despliegue hacia AWS se realiza con credenciales temporales, sin claves permanentes en el repositorio.

### 4.4.4 Adopción del sistema

Para reducir la resistencia al cambio (R-05), la capacitación se organiza por actor del sistema y se realiza en torno a la puesta en producción, de modo que cada usuario aprenda únicamente las funciones que utilizará. La Tabla 7 resume el plan.

**Tabla 7.** Capacitación por actor

| Actor | Contenido | Momento |
|---|---|---|
| A1 Operador de Ventas | Clientes, catálogo, registro de pedidos y reembolsos. | Antes de la puesta en producción (F-06) |
| A2 Operador de Inventarios | Stock de producto terminado, lotes, movimientos y solicitudes de producción. | Antes de la puesta en producción (F-06) |
| A3 Operador de Insumos | Insumos, sus lotes y movimientos, y atención de solicitudes de insumos. | Antes de la puesta en producción (F-06) |
| A4 Operador de Producción | Recepción de solicitudes de producción, registro de lotes y envío de solicitudes de insumos. | Antes de la puesta en producción (F-06) |
| A5 Operador de Despacho | Preparación y entrega de pedidos con sus estados. | Antes de la puesta en producción (F-06) |
| A6 Analista Estratégico | Objetivos, KPI, iniciativas y tablero del cuadro de mando integral. | Durante la puesta en producción (F-06) |
| A7 Administrador | Usuarios, roles, empresa emisora y configuración del sistema. | Antes de la puesta en producción (F-06) |
| A8 Cliente | Registro, verificación de correo, catálogo y cuenta en el Portal B. | Durante la puesta en producción (F-06) |

Esta capacitación inicial cubre el uso del sistema en el arranque. La formación digital más amplia del personal queda a cargo del programa de transformación y capacitación digital (TI-005) previsto en el Roadmap Tecnológico del Entregable 1 para 2027.

### 4.4.5 Soporte post-implementación

Tras el cierre, el sistema cuenta con ocho meses de soporte técnico a cargo del equipo de infraestructura, con un costo de S/ 2,000 mensuales. El soporte se organiza según las prácticas de ITIL 4: los usuarios reportan las incidencias por un canal único, estas se registran y clasifican por prioridad, y se atienden en el orden que muestra la Tabla 8. Los tiempos son una propuesta del equipo y se validarán con los usuarios clave de Franco's S.A.C.

**Tabla 8.** Prioridades de atención en el soporte (propuesta)

| Prioridad | Ejemplo | Atención propuesta |
|---|---|---|
| Crítica | El sistema no permite registrar ventas o inventario. | Inicio inmediato; solución en el mismo día. |
| Alta | Falla en un módulo con alternativa temporal. | Dentro de las 24 horas. |
| Media | Error que no detiene la operación. | Dentro de las 72 horas. |
| Baja | Consulta de uso o mejora menor. | Se programa en el siguiente mantenimiento. |

Durante este periodo se mantienen activos los mecanismos de operación definidos en el CE0142: una sonda prueba cada minuto la conexión con la base de datos y, si detecta una caída, avisa al equipo y activa la recuperación con la base temporal en la nube; el volcado diario de la base se conserva en S3 fuera de la sede; y el registro de actividad de la cuenta de AWS se revisa desde Wazuh. La disponibilidad se registra cada mes para verificar la meta del 95 %, y las incidencias recurrentes y las mejoras solicitadas se canalizan mediante el proceso de control de cambios, lo que conecta el soporte con el seguimiento de indicadores que se desarrolla en el capítulo 5.
