# Guion de exposición: Vista motivacional, metas, planificación y riesgos

*Duración aproximada: 7 minutos. El texto en cursiva entre corchetes indica qué señalar; todo lo demás es lo que se dice. Entre paréntesis va cómo se pronuncia cada código.*

---

## 1. Vista motivacional

*Aproximadamente 2 minutos y medio.*

**Apertura**
En la vista motivacional mostramos por qué Franco's necesita este sistema, qué objetivos persigue y cómo esos objetivos se convierten en los requerimientos que guían el diseño del ERP y de su infraestructura.

**Interesados e impulsores**
*[Señalar la fila azul y el grupo naranja de la izquierda.]*
Arriba están los ocho actores que usan el ERP: los operadores de Ventas, Inventario, Insumos, Producción y Despacho, el Analista Estratégico, el Administrador y el Cliente. A la izquierda, los cinco impulsores del cambio: la digitalización de la gestión operativa, estratégica y comercial; la integración de la información entre las áreas; la continuidad de la operación; la protección de datos personales que exige la Ley 29733 (veintinueve mil setecientos treinta y tres); y la trazabilidad de lotes y conservación de registros.

**Objetivos**
*[Señalar la barra verde, la caja verde de la derecha y la caja marrón.]*
Estos impulsores influyen en el objetivo de negocio OEN-03 (o e ene cero tres): optimizar la gestión operativa y estratégica mediante tecnologías digitales e información. Lo soporta el objetivo de TI OET-03 (o e te cero tres): implementar soluciones empresariales integradas para digitalizar los procesos operativos y comerciales. Ambos vienen de los mapas estratégicos del Entregable 1. Y tenemos una restricción de plazo: el ERP y su infraestructura deben implementarse entre el 6 de abril y el 30 de noviembre de 2026.

**Evaluaciones**
*[Señalar la fila amarilla.]*
En la fila amarilla están las nueve evaluaciones, que son los problemas que encontramos en el diagnóstico: las ventas, el inventario y la distribución se anotan en papel y en Excel; no hay una base de datos donde se junte la información ni copia de respaldo; no hay servidor ni nube; la red no tiene redundancia ni detecta fallas; y no existe un canal de venta en línea.

**Metas, resultados y medidas**
*[Señalar la fila verde claro, la turquesa y la lila.]*
Para resolverlos, el objetivo se descompone en cinco metas, que veremos en la siguiente lámina. Cada meta se cumple mediante resultados concretos, en turquesa, y cada resultado se comprueba con una medida, en lila. Por ejemplo, el resultado de que el ERP siga en servicio aunque falle un equipo se comprueba con la disponibilidad del sistema, cuya meta es de 95 % o más en horario de trabajo.

**Principios, requerimientos y procesos**
*[Señalar el grupo rosado, la fila ocre y la fila amarilla de abajo.]*
El diseño se rige por trece principios de arquitectura, como el registro único, la trazabilidad de lotes, el acceso por rol y que no exista un punto único de falla. Estos principios se cumplen mediante trece requerimientos, que se hacen realidad en los ocho procesos de negocio que rediseñamos en el Entregable 3. Las cajas marrones son las restricciones del alcance: SICO ERP sigue emitiendo los comprobantes oficiales, los datos históricos no se migran y los datos se procesan en la nube de AWS.

**Ejemplo y cierre**
*[Recorrer con el dedo la columna del Operador de Inventario.]*
Por ejemplo: el Operador de Inventario lleva hoy su inventario en papel y en Excel. Eso se atiende con la meta de registrar el inventario en el ERP; el resultado es que cada producto sea rastreable hasta su lote; y se cumple con el requerimiento de registro de lotes y movimientos, que respeta los principios de registro único y de trazabilidad. Así, cada elemento del sistema tiene una razón de ser y todo apunta a los objetivos estratégicos de Franco's.

---

## 2. «Cinco metas llevan OEN-03 a la práctica»

*Aproximadamente 1 minuto y medio.*

El objetivo OEN-03 (o e ene cero tres) es amplio, así que lo bajamos a cinco metas concretas. Debajo de cada una indicamos qué brecha del diagnóstico cierra o, si no viene de una brecha, a qué mejora responde.

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

En resumen, las cinco metas cubren las dos caras del objetivo: la gestión operativa, con MT-01, MT-03 y MT-04, y la gestión estratégica y comercial, con MT-02 y MT-05.

---

## 3. «Planificación» · Cronograma de implementación

*Aproximadamente 1 minuto y medio.*

Estas metas se cumplen con dos iniciativas que se ejecutan en paralelo: TI-002 (te i cero cero dos), que es el ERP, y TI-003 (te i cero cero tres), que es la infraestructura. El proyecto va del 6 de abril al 30 de noviembre de 2026, y luego tiene ocho meses de soporte hasta el 31 de julio de 2027.

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

## 4. «Riesgos de la implementación»

*Aproximadamente 1 minuto y medio.*

Para cumplir este cronograma identificamos los riesgos que pueden afectar la implementación, con su probabilidad, su impacto y la respuesta que aplicamos.

*[Señalar R-10 y R-01.]*
Los dos riesgos más probables son estos. El R-10 (erre diez), con 80 %: que falle la PC que ejecuta SICO ERP, porque SICO sigue emitiendo los comprobantes oficiales y no tiene respaldo. Lo atendemos con un respaldo periódico de SICO y un procedimiento alterno de emisión. Y el R-01 (erre cero uno), con 70 %: los cambios frecuentes de requerimientos, que controlamos con un proceso formal de cambios aprobado por el Director.

*[Señalar R-02, R-03 y R-07.]*
Con impacto alto también están los retrasos en los sprints, que seguimos semanalmente priorizando el backlog; las ciberamenazas, que mitigamos con acceso por rol, el WAF, secretos fuera del código y registro de actividad; y el incumplimiento de la Ley de Protección de Datos, que prevenimos con protección desde el diseño y cifrado en tránsito.

*[Señalar R-04, R-05, R-08 y R-09.]*
Con impacto medio o bajo están la integración entre Software e Infraestructura, que probamos de forma anticipada; la resistencia al cambio, que atendemos con capacitación por rol; las fallas de la nube o de la sede, cubiertas con el volcado diario, una base temporal restaurable y monitoreo; y el aumento de costos, controlado con un presupuesto de 80 dólares al mes y avisos al 50, 80 y 100 %.

Así, cada riesgo tiene una respuesta concreta y un responsable, y se revisa dentro del control del proyecto.

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
