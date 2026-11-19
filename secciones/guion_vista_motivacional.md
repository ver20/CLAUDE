# Guion de exposición: Vista motivacional, planificación, riesgos y metas

*Láminas 9, 24, 25 y 26 de la presentación «Franco's ERP: del papel a un sistema integrado». Duración aproximada: 6 minutos. El texto en cursiva entre corchetes indica qué señalar; todo lo demás es lo que se dice. Entre paréntesis va cómo se pronuncia cada código.*

*La lámina 9 viene después de «El diseño responde a OEN-03 y brechas». Las láminas 24 a 26 vienen después de «Los datos viven en islas, a mano y sin respaldo», y después de ellas sigue «Ocho actores que usan el ERP».*

---

## Lámina 9 · «Vista motivacional»

*Aproximadamente 1 minuto y medio.*

**Apertura**
Como acabamos de ver, el diseño responde al objetivo OEN-03 (o e ene cero tres). La vista motivacional explica, en una sola imagen, por qué hacemos el sistema y cómo eso se convierte en lo que vamos a construir. Se lee de arriba hacia abajo, en tres partes.

**El porqué**
*[Señalar la parte de arriba: interesados, impulsores y objetivos.]*
Arriba está el porqué: las personas que usarán el ERP, las razones que obligan a Franco's a cambiar, como digitalizar su gestión y proteger sus datos, y los objetivos estratégicos de negocio y de TI que definimos en el Entregable 1.

**El para qué**
*[Señalar la parte del medio: evaluaciones, metas, resultados y medidas.]*
En el medio está el para qué. Partimos de los problemas que encontramos en el diagnóstico, como que la información está en papel y en Excel, sin respaldo y sin una base común. Para resolverlos definimos cinco metas, cada una con resultados concretos y una forma de medirlos.

**El cómo**
*[Señalar la parte de abajo: principios, requerimientos y procesos.]*
Abajo está el cómo: los principios de arquitectura que guían el diseño, los requerimientos que el sistema debe cumplir y los procesos de negocio donde esos requerimientos se aplican en el día a día.

**Cierre**
En resumen, la vista nos asegura que todo lo que construimos responde a un problema real y a un objetivo de la empresa. Las cinco metas las detallaremos más adelante, en la sección de oportunidades y soluciones.
---

## Lámina 24 · «Planificación» (E. Oportunidades y soluciones)

*Aproximadamente 1 minuto y medio.*

Para cerrar las brechas que acabamos de ver, en la fase de oportunidades y soluciones planificamos la implementación. Se ejecutan dos iniciativas en paralelo: TI-002 (te i cero cero dos), que es el ERP, y TI-003 (te i cero cero tres), que es la infraestructura. El proyecto va del 6 de abril al 30 de noviembre de 2026, y luego tiene ocho meses de soporte hasta el 31 de julio de 2027.

*[Señalar las barras azules.]*
Las primeras fases son de planificación, análisis y diseño. La fase F-01 (efe cero uno) cerró con el charter y el plan aprobados; el análisis continuó con el refinamiento y la planificación de los sprints; y el diseño cerró con la arquitectura y los prototipos aprobados.

*[Señalar las barras verdes de los sprints.]*
La construcción, F-04 (efe cero cuatro), se organizó en seis sprints registrados en Jira, del 14 de septiembre al 6 de noviembre. Empieza por el núcleo del Portal A y la estrategia, sigue con el Portal B, el comprobante y la entrega, luego almacén y producción, la configuración y el carrito, y termina con el perfil, la seguridad y las pruebas de extremo a extremo.

*[Señalar las barras de pruebas y despliegue.]*
Las pruebas, F-05 (efe cero cinco), empiezan el 12 de octubre, en paralelo con la construcción, e incluyen la integración y el despliegue continuos. Por eso los sprints 3 a 6 duran una semana: así se mantiene la fecha de despliegue y de cierre que comprometimos en el Entregable 2.

El despliegue, F-06 (efe cero seis), se hace en tres etapas: primero la infraestructura; luego la operación interna, en paralelo con el registro actual; y al final la estrategia y la tienda en línea. Su hito es una disponibilidad de 95 % o más.

*[Señalar el último rombo.]*
El proyecto cierra el 30 de noviembre con el acta de aceptación, que es también el hito H1 (hache uno) del roadmap: la base tecnológica de Franco's operativa.

---

## Lámina 25 · «Riesgos de la implementación»

*Aproximadamente 1 minuto y medio.*

Para cumplir este cronograma identificamos los riesgos que pueden afectar la implementación, con su probabilidad, su impacto y la respuesta que aplicamos.

*[Señalar R-10 y R-01.]*
Los dos riesgos más probables son estos. El R-10 (erre diez), con 80 %: que falle la PC que ejecuta SICO ERP, porque SICO sigue emitiendo los comprobantes oficiales y no tiene respaldo. Lo atendemos con un respaldo periódico de SICO y un procedimiento alterno de emisión. Y el R-01 (erre cero uno), con 70 %: los cambios frecuentes de requerimientos, que controlamos con un proceso formal de cambios aprobado por el Director.

*[Señalar R-02, R-03 y R-07.]*
Con impacto alto también están los retrasos en los sprints, que seguimos semanalmente priorizando el backlog; las ciberamenazas, que mitigamos con acceso por rol, el WAF, secretos fuera del código y registro de actividad; y el incumplimiento de la Ley de Protección de Datos, que prevenimos con protección desde el diseño y cifrado en tránsito.

*[Señalar R-04, R-05, R-08 y R-09.]*
Con impacto medio o bajo están la integración entre Software e Infraestructura, que probamos de forma anticipada; la resistencia al cambio, que atendemos con capacitación por rol; las fallas de la nube o de la sede, cubiertas con el volcado diario, una base temporal restaurable y monitoreo; y el aumento de costos, controlado con un presupuesto de 80 dólares al mes y avisos al 50, 80 y 100 %.

Así, cada riesgo tiene una respuesta concreta y se revisa dentro del control del proyecto.

---

## Lámina 26 · «Cinco metas llevan OEN-03 a la práctica»

*Aproximadamente 1 minuto y medio.*

Con el plan y sus riesgos definidos, volvemos al objetivo que guía todo el proyecto. OEN-03 (o e ene cero tres) es amplio, así que lo bajamos a cinco metas concretas, que son las que vimos en la vista motivacional. Debajo de cada una indicamos qué brecha del diagnóstico cierra o, si no viene de una brecha, a qué mejora responde.

*[Señalar MT-01.]*
La primera, MT-01 (eme te cero uno), es registrar las ventas, los despachos, el inventario y las solicitudes de producción en el ERP. Cierra las brechas B-01 (be cero uno), porque hoy esa información no se registra en ningún sistema; B-03 (be cero tres), porque Excel y Word se usan sin integración; y B-14 (be catorce), porque Producción e Insumos también registran en papel.

*[Señalar MT-02.]*
La segunda, MT-02 (eme te cero dos), es dar seguimiento a la estrategia de negocio y de TI en el ERP. No nace de una brecha, porque hoy no existe ningún registro de la estrategia: es una mejora que responde a la parte estratégica de OEN-03.

*[Señalar MT-03.]*
La tercera, MT-03 (eme te cero tres), es reunir los datos en una sola base, con copia restaurable y acceso por rol. Cierra la B-05 (be cero cinco), porque no hay una base de datos central, y la B-09 (be cero nueve), porque la información no tiene respaldo.

*[Señalar MT-04.]*
La cuarta, MT-04 (eme te cero cuatro), es sostener el ERP en la sede y en la nube, con una infraestructura redundante, segmentada y monitoreada. Cierra las brechas tecnológicas B-08 (be cero ocho), B-10 (be diez), B-11 (be once) y B-12 (be doce): red sin redundancia, red sin segmentar, sin servidor ni nube, y sin monitoreo.

*[Señalar MT-05.]*
La quinta, MT-05 (eme te cero cinco), es abrir un canal de venta en línea para el cliente. Tampoco nace de una brecha, porque hoy ese canal no existe: es una mejora que responde al objetivo de TI OET-03 (o e te cero tres), que soporta a OEN-03 en la digitalización de los procesos comerciales.

En resumen, las cinco metas cubren las dos caras del objetivo: la gestión operativa, con MT-01, MT-03 y MT-04, y la gestión estratégica y comercial, con MT-02 y MT-05. A continuación, se presentan los ocho actores que usarán el ERP para cumplirlas.

---

## Respuestas preparadas para el jurado

**¿Por qué las metas se relacionan con los objetivos mediante agregación?**
Porque cada meta es una parte del objetivo, no un tipo de objetivo. OEN-03 se compone de las cuatro primeras metas, y OET-03 de la quinta.

**¿Por qué no aparece la gerencia como actor?**
Porque la vista representa a los actores que usan el sistema, y el ERP no tiene un rol de gerencia. La información estratégica la registra y le da seguimiento el Analista Estratégico.

**¿Por qué los sprints 3 a 6 duran una semana?**
Porque la construcción empezó más tarde de lo previsto y, para no mover el despliegue del 27 de noviembre ni el cierre del 30 de noviembre comprometidos en el Entregable 2, acortamos esos sprints y adelantamos las pruebas en paralelo.

**¿Por qué el riesgo de SICO tiene la mayor probabilidad?**
Porque SICO ERP sigue siendo el emisor oficial de comprobantes hasta la integración con SUNAT, corre en una sola PC y no tiene respaldo. Una falla de esa PC detendría la facturación, por eso le damos respaldo periódico y un procedimiento alterno.

**¿Por qué el despliegue es por etapas?**
Para no detener la operación: primero se prepara la infraestructura, luego el personal trabaja en el ERP en paralelo con el registro actual, y solo al final se abren la estrategia y la tienda en línea.
