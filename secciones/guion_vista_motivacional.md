# Guion de exposición: Vista motivacional, planificación, riesgos y metas

*Láminas 9, 24, 25 y 26 de la presentación «Franco's ERP: del papel a un sistema integrado». Duración aproximada: 4 minutos y medio. El texto en cursiva entre corchetes indica qué señalar; todo lo demás es lo que se dice. Entre paréntesis va cómo se pronuncia cada código.*

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

*Aproximadamente 1 minuto.*

Para cerrar las brechas que acabamos de ver, planificamos la implementación del ERP y de su infraestructura, que se ejecutan en paralelo entre abril y noviembre de 2026.

*[Señalar las barras de arriba.]*
Primero vienen la planificación, el análisis y el diseño, donde definimos qué construir y cómo.

*[Señalar las barras verdes y las de pruebas.]*
Luego viene la construcción, organizada en seis sprints, y en paralelo las pruebas, para no mover las fechas comprometidas.

*[Señalar las barras moradas y el último rombo.]*
Después, el despliegue se hace por etapas, para no detener la operación de la empresa. El proyecto cierra el 30 de noviembre con el acta de aceptación, y continúa con ocho meses de soporte.

---

## Lámina 25 · «Riesgos de la implementación»

*Aproximadamente 1 minuto.*

Para cumplir este plan, identificamos los riesgos que podrían afectarlo, cada uno con su probabilidad, su impacto y una respuesta.

*[Señalar R-10 y R-01.]*
Los más probables son dos: que falle la computadora donde corre el sistema actual de facturación, que no tiene respaldo, y que los requerimientos cambien con frecuencia. Para el primero tenemos respaldos y un procedimiento alterno; para el segundo, un control formal de cambios.

*[Señalar el resto de la tabla.]*
Los demás riesgos son de tiempo, de seguridad, de integración, de adopción por parte de los usuarios y de costos. Cada uno tiene una respuesta concreta, como el seguimiento semanal, la capacitación por rol o un presupuesto con alertas.

---

## Lámina 26 · «Cinco metas llevan OEN-03 a la práctica»

*Aproximadamente 1 minuto.*

Con el plan y sus riesgos definidos, volvemos al objetivo que guía todo el proyecto. OEN-03 (o e ene cero tres) lo bajamos a cinco metas concretas, que son las que vimos en la vista motivacional.

*[Recorrer las cinco tarjetas de izquierda a derecha.]*
Las metas son: registrar la operación diaria en el ERP; dar seguimiento a la estrategia; reunir los datos en una sola base con respaldo; sostener el sistema sobre una infraestructura segura y redundante; y abrir un canal de venta en línea.

*[Señalar los textos grises de abajo.]*
Debajo de cada meta indicamos qué brechas del diagnóstico cierra. Las metas de estrategia y de venta en línea no vienen de un problema actual, sino que son mejoras que la empresa incorpora.

En resumen, las cinco metas cubren la gestión operativa, la estratégica y la comercial. A continuación, se presentan los ocho actores que usarán el ERP para cumplirlas.

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
