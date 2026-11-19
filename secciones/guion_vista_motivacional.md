# Guion para explicar la vista motivacional (CE0142)

**Duración aproximada:** 4 a 5 minutos.
**Cómo leerla:** de arriba hacia abajo. Arriba está el *por qué* (quién necesita el cambio y qué problema hay), en el medio el *para qué* (objetivos, metas y resultados) y abajo el *cómo* (principios, requerimientos y procesos).

---

## 1. Introducción (20 s)

> "Esta es la vista motivacional de Franco's ERP, construida con la Fase A de TOGAF. Su propósito es mostrar por qué hacemos el sistema y cómo cada requerimiento responde a un objetivo de la organización. Se lee de arriba hacia abajo: primero quién necesita el cambio y qué problemas tiene, luego qué queremos lograr, y al final cómo lo vamos a lograr."

## 2. Interesados e impulsores (40 s)

*[Señalar el grupo superior "Interesados" y el grupo de la izquierda "Impulsores del cambio".]*

> "Arriba están los nueve interesados del sistema. Siete son operativos: el Operador de Ventas, de Inventarios, de Insumos, de Producción y de Despacho, el Analista Estratégico y el Administrador. También están el Gerente General, que consulta reportes e indicadores, y el Cliente, que es el único actor externo y compra en la tienda en línea.
>
> A la izquierda están los cinco impulsores del cambio, es decir, las fuerzas que obligan a la empresa a transformarse: la digitalización de su gestión, la integración de la información entre áreas, la continuidad de la operación, la protección de datos personales que exige la Ley 29733 y la trazabilidad de lotes."

## 3. Objetivos estratégicos y restricción de plazo (30 s)

*[Señalar la barra verde grande, la caja verde de la derecha y la caja beige RS-03.]*

> "Estos impulsores influyen en el objetivo organizacional OEN-03: optimizar la gestión operativa y estratégica mediante tecnologías digitales e información. Lo soporta el objetivo de TI OET-03: implementar soluciones empresariales integradas para digitalizar los procesos operativos y comerciales. Ambos vienen de los mapas estratégicos que hicimos en entregables anteriores.
>
> A la derecha está la restricción RS-03: las iniciativas TI-002, que es el ERP, y TI-003, que es la infraestructura, deben ejecutarse entre el 6 de abril y el 30 de noviembre de 2026."

## 4. Evaluaciones: los problemas actuales (40 s)

*[Señalar la fila amarilla.]*

> "En amarillo están las nueve evaluaciones, que son los problemas que encontramos en el diagnóstico del CE0141. Por ejemplo:
> - EV-01: ventas, inventario y distribución se anotan en papel y en Excel y no pasan a ningún sistema.
> - EV-04: no hay una base de datos donde se junte la información de las áreas.
> - EV-07 y EV-08: no hay servidor ni nube, y la red no tiene redundancia ni detecta fallas.
> - EV-09: no existe un canal de venta en línea.
>
> Cada evaluación apunta a la meta que la resuelve."

## 5. Metas: el desglose de los objetivos (40 s)

*[Señalar la fila verde claro.]*

> "Los objetivos estratégicos son amplios, así que los desglosamos en cinco metas concretas:
> - MT-01: registrar las ventas, los despachos, el inventario y las solicitudes de producción en el ERP.
> - MT-02: dar seguimiento a la estrategia de negocio y de TI en el ERP.
> - MT-03: reunir los datos operativos en una sola base, con copia restaurable y acceso por rol.
> - MT-04: sostener el ERP en una infraestructura propia y en la nube, redundante, segmentada y monitoreada.
> - MT-05: abrir un canal de venta en línea para el cliente.
>
> Las cuatro primeras se especializan de OEN-03 y la quinta de OET-03. Cada interesado se conecta con la meta que le interesa: por ejemplo, los operadores con MT-01, el Analista con MT-02 y el Cliente con MT-05."

## 6. Resultados y medidas (40 s)

*[Señalar la fila turquesa y la fila lila.]*

> "Debajo de cada meta están los resultados esperados, en turquesa, que describen cómo se verá la empresa cuando la meta se cumpla. Por ejemplo, RE-02: el inventario de insumos y de producto terminado llevado en el ERP, con cada producto rastreable hasta su lote.
>
> En lila están las medidas con las que vamos a comprobar cada resultado, como MD-03, productos terminados rastreables hasta su lote, o MD-08, disponibilidad del ERP. Sus metas numéricas, la línea base y la frecuencia de medición se definen en el CE0145."

## 7. Principios de arquitectura (30 s)

*[Señalar el grupo rosado.]*

> "En rosado están los trece principios de arquitectura, que son las reglas que guían todas las decisiones de diseño. Por ejemplo, P1 Registro único: cada dato se registra una sola vez. P9 Acceso por rol: cada usuario ve solo lo que le corresponde. P11 Sin punto único de falla. Y P13 Detección y aviso: toda falla se detecta y se avisa a un responsable."

## 8. Requerimientos, restricciones y procesos (50 s)

*[Señalar la fila ocre, las cajas beige de la izquierda y la fila amarilla de abajo.]*

> "En ocre están los trece requerimientos, que es lo que el sistema debe cumplir. Cada requerimiento realiza uno o más principios. Por ejemplo, RQ-07, respaldo diario fuera de la sede con restauración probada, cumple el principio P2, copia restaurable. Y RQ-12, red y conexión a internet redundantes y segmentadas, cumple P11 y P12.
>
> A la izquierda están las restricciones que condicionan esos requerimientos:
> - RS-01: SICO ERP sigue como emisor oficial de comprobantes hasta la integración con SUNAT.
> - RS-02: los datos históricos en papel, Excel y Word no se migran.
> - RS-04: los datos se procesan fuera del país, en AWS us-east-1, por eso la demostración usa datos ficticios.
>
> Abajo están los ocho procesos de negocio que rediseñamos en el E3, como la validación y formalización de la venta o la recepción de la solicitud de insumos. Estos procesos son los que realizan los requerimientos en la operación diaria."

## 9. Recorrido de ejemplo (40 s)

*[Recorrer con el dedo una columna completa, de arriba hacia abajo: la de MT-01.]*

> "Para ver cómo se conecta todo, sigamos una columna. El Operador de Inventarios sufre el problema EV-01: el inventario se lleva en papel y Excel. Eso motiva la meta MT-01, registrar el inventario en el ERP, que forma parte del objetivo OEN-03. Su resultado es RE-02, con cada producto rastreable hasta su lote, y se mide con MD-03. Para lograrlo, el requerimiento RQ-03, registro de lotes y movimientos de inventario rastreables, cumple los principios P1 Registro único y P5 Trazabilidad de lotes, y lo realizan procesos como la actualización y gestión de inventario."

## 10. Cierre (20 s)

> "En resumen, la vista asegura que nada en el sistema esté de más: cada requerimiento responde a un principio y a una meta, cada meta resuelve un problema real del diagnóstico, y todo apunta a los objetivos estratégicos OEN-03 y OET-03 de Franco's."

---

## Preguntas que podría hacer el jurado

**¿Por qué el Gerente General está en la vista si no registra información?**
> "Porque es el patrocinador del proyecto y el principal usuario de la información: necesita consultar en un solo lugar los reportes e indicadores de las áreas, que hoy están en papel y en archivos sueltos. Eso es lo que expresa el resultado RE-10."

**¿Por qué los requerimientos no tienen flechas hacia las metas?**
> "Esas relaciones están en el modelo, pero no se dibujan en la vista para que se pueda leer. En la vista se muestra la relación de cada requerimiento con sus principios."

**¿Por qué las medidas no tienen cifras?**
> "Porque las metas numéricas, la línea base y la frecuencia se definen en el CE0145, que es el capítulo de indicadores."

**¿Qué diferencia hay entre una evaluación y un impulsor?**
> "El impulsor es una fuerza general que empuja el cambio, como la necesidad de digitalizarse. La evaluación es un problema concreto que encontramos en el diagnóstico, como que el inventario se lleve en papel."

**¿Qué diferencia hay entre una meta y un resultado?**
> "La meta es lo que nos proponemos hacer, como registrar el inventario en el ERP. El resultado es el estado final que se espera, como que cada producto sea rastreable hasta su lote. La medida es cómo comprobamos que ese resultado se logró."
