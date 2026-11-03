# 2.1 Objetivos que guían el diseño

El diseño de la arquitectura conceptual de Franco's ERP no parte de una elección tecnológica, sino de las necesidades del negocio identificadas en los entregables anteriores. El diagnóstico organizacional evidenció una gestión operativa informal, información dispersa en papel y hojas de cálculo, herramientas subutilizadas y decisiones tomadas sin indicadores. A partir de ello, y siguiendo el método ADM de TOGAF, esta sección define la visión de arquitectura, relaciona los problemas detectados con los objetivos estratégicos que atiende el sistema y establece los principios que orientan las decisiones de diseño de los capítulos siguientes.

**Visión de arquitectura.** Se plantea la siguiente visión, que resume el propósito de la arquitectura propuesta:

> *"Integrar en una plataforma web única la información de ventas, inventario, atención al cliente y gestión estratégica de Franco's S.A.C., reemplazando los registros manuales y aislados por datos centralizados, trazables y disponibles en tiempo real para la operación diaria y la toma de decisiones."*

**Vista motivacional.** La Tabla 1 muestra la relación entre los impulsores del cambio, los objetivos estratégicos definidos en el Entregable 1 y los resultados que se esperan del sistema. Esta relación asegura que cada componente de la arquitectura responda a una necesidad concreta del negocio.

**Tabla 1.** Vista motivacional de la arquitectura propuesta

| Impulsor (problema) | Objetivo estratégico | Resultado esperado |
|---|---|---|
| Operaciones de ventas, inventario y distribución registradas en papel y hojas de cálculo desarticuladas. | Negocio E3 / TI E3: digitalizar procesos operativos y comerciales mediante soluciones integradas. | Registros manuales reemplazados por un sistema web centralizado. |
| Quiebres de stock por falta de control y de alertas oportunas. | TI E3 / TI E9: soluciones integradas y automatización de procesos clave. | Inventario con trazabilidad de movimientos y alertas de stock mínimo. |
| Pedidos atendidos de forma manual y sin visibilidad de su estado. | Negocio E7 / TI E7: optimizar la gestión de pedidos y la experiencia del cliente. | Ciclo de venta digital, con seguimiento de pedidos por parte del cliente. |
| Decisiones gerenciales tomadas sin indicadores ni información confiable. | TI E4 / TI E6: inteligencia de negocios y gobierno de TI alineado al negocio. | Reportes en tiempo real y tablero BSC con KPIs estratégicos. |
| Información sensible sin políticas de seguridad ni control de acceso. | TI E6: gobierno de TI alineado a los objetivos del negocio. | Acceso controlado por roles y comunicaciones cifradas. |

**Objetivos de diseño.** De la vista motivacional se derivan los objetivos que la arquitectura debe cumplir. Cada uno se vincula con las iniciativas de mejora priorizadas en el Entregable 3, lo que garantiza la continuidad entre el rediseño de procesos y el diseño del sistema de información (Tabla 2).

**Tabla 2.** Objetivos de diseño de la arquitectura

| ID | Objetivo de diseño | Iniciativa (E3) |
|---|---|---|
| OD-01 | Centralizar la información operativa en una base de datos única, eliminando la duplicidad entre registros físicos y digitales. | IM-02, IM-05 |
| OD-02 | Integrar los procesos de ventas, inventario y despacho, de modo que cada operación actualice automáticamente la información relacionada. | IM-01, IM-06 |
| OD-03 | Asegurar la trazabilidad de pedidos, lotes y movimientos de inventario desde su registro hasta su cierre. | IM-04, IM-05 |
| OD-04 | Proveer información oportuna para la toma de decisiones mediante reportes e indicadores estratégicos. | Gestión estratégica |
| OD-05 | Garantizar el acceso seguro a la información según el rol de cada usuario. | Transversal |
| OD-06 | Asegurar la disponibilidad del sistema durante el horario operativo y su capacidad de crecer junto con la empresa. | Transversal |

**Principios de arquitectura.** Finalmente, se establecen los principios que rigen las decisiones de diseño en cada dominio de la arquitectura. Estos principios recogen los lineamientos del proyecto definidos en el Entregable 2 y sirven como criterio para evaluar las alternativas tecnológicas descritas más adelante (Tabla 3).

**Tabla 3.** Principios de arquitectura por dominio

| Dominio | Principio | Declaración | Implicancia |
|---|---|---|---|
| Negocio | Alineamiento estratégico | Toda funcionalidad del sistema debe responder a un objetivo estratégico de la organización. | Los módulos se priorizan según su aporte a los objetivos del Entregable 1. |
| Negocio | Procesos soportados por el sistema | Los procesos rediseñados deben ejecutarse dentro del sistema y no fuera de él. | Se eliminan los registros paralelos en papel y hojas de cálculo. |
| Datos | Dato único y compartido | Cada dato se registra una sola vez y es consultado por todas las áreas que lo requieren. | Ventas, inventario y gerencia trabajan sobre la misma información. |
| Datos | Trazabilidad | Toda operación debe quedar registrada con su responsable y fecha. | Es posible reconstruir el historial de cualquier pedido o movimiento. |
| Aplicaciones | Modularidad | El sistema se organiza en módulos independientes por dominio de negocio. | Cada módulo puede desarrollarse, mantenerse y ampliarse sin afectar a los demás. |
| Aplicaciones | Acceso según rol | Cada usuario accede únicamente a las funciones que requiere su rol. | Se definen perfiles diferenciados para el personal interno y los clientes. |
| Tecnología | Disponibilidad y continuidad | La plataforma debe mantenerse operativa durante el horario de trabajo y recuperarse ante fallas. | Se requiere infraestructura con respaldo y mecanismos de recuperación. |
| Tecnología | Seguridad desde el diseño | La protección de la información se incorpora desde la concepción del sistema. | Se aplican autenticación, cifrado de comunicaciones y protección de datos personales. |

En conjunto, la visión, los objetivos de diseño y los principios constituyen el marco de referencia de la arquitectura conceptual: los componentes, capas y tecnologías que se presentan en las secciones siguientes se justifican en función de su contribución a estos objetivos.
