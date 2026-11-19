# Guion de exposición: Vista motivacional de Franco's ERP

*Diapositivas 24, 25 y 26 · duración aproximada: 5 minutos. El texto en cursiva entre corchetes indica qué señalar; todo lo demás es lo que se dice. Entre paréntesis va cómo se pronuncia cada código.*

---

## Diapositiva 24 · «Ocho actores que usan el ERP»

*Aproximadamente 1 minuto.*

Para explicar por qué construimos Franco's ERP, empezamos por quiénes lo van a usar. Son ocho actores.

*[Señalar las cinco primeras tarjetas.]*
Cinco son operadores de las áreas que hoy registran su información en papel y en Excel:
- el **Operador de Ventas**, que gestiona clientes, catálogo, pedidos y reembolsos;
- el **Operador de Inventario**, que lleva el producto terminado, sus lotes y sus movimientos;
- el **Operador de Insumos**, que maneja los insumos y atiende las solicitudes de insumos;
- el **Operador de Producción**, que recibe las solicitudes de producción y registra los lotes;
- y el **Operador de Despacho**, que prepara y entrega los pedidos.

*[Señalar A6 y A7.]*
A ellos se suman el **Analista Estratégico**, que lleva el cuadro de mando integral y pertenece a una nueva jefatura de Gestión Estratégica, y el **Administrador**, que gestiona los usuarios, los roles y la configuración del sistema.

*[Señalar la tarjeta naranja.]*
Finalmente está el **Cliente**, el único actor externo, que se registra, consulta el catálogo y gestiona su cuenta en la tienda en línea.

Estos ocho actores son los interesados de la vista motivacional que presentamos a continuación.

---

## Diapositiva 25 · «Vista motivacional»

*Aproximadamente 2 minutos y medio.*

**Apertura**
En la vista motivacional mostramos por qué Franco's necesita este sistema, qué objetivos persigue y cómo esos objetivos se convierten en los requerimientos que guían el diseño del ERP y de su infraestructura.

**Interesados e impulsores**
*[Señalar la fila azul y el grupo naranja de la izquierda.]*
Arriba están los ocho actores que acabamos de ver. A la izquierda, los cinco impulsores del cambio: la digitalización de la gestión operativa, estratégica y comercial; la integración de la información entre las áreas; la continuidad de la operación; la protección de datos personales que exige la Ley 29733 (veintinueve mil setecientos treinta y tres); y la trazabilidad de lotes y conservación de registros.

**Objetivos**
*[Señalar la barra verde, la caja verde de la derecha y la caja marrón.]*
Estos impulsores influyen en el objetivo de negocio OEN-03 (o e ene cero tres): optimizar la gestión operativa y estratégica mediante tecnologías digitales e información. Lo soporta el objetivo de TI OET-03 (o e te cero tres): implementar soluciones empresariales integradas para digitalizar los procesos operativos y comerciales. Ambos vienen de los mapas estratégicos del Entregable 1. Y tenemos una restricción de plazo: el ERP y su infraestructura deben implementarse entre el 6 de abril y el 30 de noviembre de 2026.

**Evaluaciones**
*[Señalar la fila amarilla.]*
En la fila amarilla están las nueve evaluaciones, que son los problemas que encontramos en el diagnóstico: las ventas, el inventario y la distribución se anotan en papel y en Excel; no hay una base de datos donde se junte la información ni copia de respaldo; no hay servidor ni nube; la red no tiene redundancia ni detecta fallas; y no existe un canal de venta en línea.

**Metas, resultados y medidas**
*[Señalar la fila verde claro, la turquesa y la lila.]*
Para resolverlos, el objetivo se descompone en cinco metas, que explicaremos en la siguiente diapositiva. Cada meta se cumple mediante resultados concretos, en turquesa, y cada resultado se comprueba con una medida, en lila. Por ejemplo, el resultado de que el ERP siga en servicio aunque falle un equipo se comprueba con la disponibilidad del sistema, cuya meta es de 95 % o más en horario de trabajo.

**Principios, requerimientos y procesos**
*[Señalar el grupo rosado, la fila ocre y la fila amarilla de abajo.]*
El diseño se rige por trece principios de arquitectura, como el registro único, la trazabilidad de lotes, el acceso por rol y que no exista un punto único de falla. Estos principios se cumplen mediante trece requerimientos, que se hacen realidad en los ocho procesos de negocio que rediseñamos en el Entregable 3. Las cajas marrones son las restricciones del alcance: SICO ERP sigue emitiendo los comprobantes oficiales, los datos históricos no se migran y los datos se procesan en la nube de AWS.

**Ejemplo**
*[Recorrer con el dedo la columna del Operador de Inventario.]*
Por ejemplo: el Operador de Inventario lleva hoy su inventario en papel y en Excel. Eso se atiende con la meta de registrar el inventario en el ERP; el resultado es que cada producto sea rastreable hasta su lote; y se cumple con el requerimiento de registro de lotes y movimientos, que respeta los principios de registro único y de trazabilidad.

**Cierre**
Así, cada elemento del sistema tiene una razón de ser: cada requerimiento cumple un principio, cada meta resuelve un problema real y se verifica con una medida, y todo apunta a los objetivos estratégicos de Franco's.

---

## Diapositiva 26 · «Cinco metas llevan OEN-03 a la práctica»

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

En resumen, las cinco metas cubren las dos caras del objetivo: la gestión operativa, con MT-01, MT-03 y MT-04, y la gestión estratégica y comercial, con MT-02 y MT-05. Cada una tiene sus resultados e indicadores, que se miden con el plan de indicadores del entregable.

---

## Respuestas preparadas para el jurado

**¿Por qué las metas se relacionan con los objetivos mediante agregación?**
Porque cada meta es una parte del objetivo, no un tipo de objetivo. OEN-03 se compone de las cuatro primeras metas, y OET-03 de la quinta.

**¿Dónde están las metas numéricas de las medidas?**
En el plan de indicadores del entregable. Cada una de las diez medidas de la vista tiene allí su fórmula, línea base, meta y frecuencia.

**¿Por qué no aparece la gerencia como actor?**
Porque la vista representa a los actores que usan el sistema, y el ERP no tiene un rol de gerencia. La información estratégica la registra y le da seguimiento el Analista Estratégico.

**¿Por qué SICO ERP sigue en operación?**
Porque esta versión del ERP no emite comprobantes electrónicos válidos ante SUNAT. Mientras no se integre, SICO ERP sigue como emisor oficial, y lo registramos como restricción y como riesgo del plan de implementación.

**¿Qué normas sustentan la trazabilidad y la conservación de registros?**
El Decreto Legislativo 1062, Ley de Inocuidad de los Alimentos, que exige rastrear cada producto hasta su lote, y el Código Tributario, que obliga a conservar los registros y comprobantes mientras el tributo no prescriba.
