# Guion para explicar la vista motivacional (CE0142)

**Versión del diagrama:** v6
**Duración aproximada:** 5 minutos
**Cómo leerla:** de arriba hacia abajo. Arriba está el **por qué** (quién necesita el cambio, qué lo impulsa y qué problemas hay), en el medio el **para qué** (objetivos, metas, resultados y medidas) y abajo el **cómo** (principios, requerimientos, restricciones y procesos).

---

## 1. Introducción (20 s)

> "Esta es la vista motivacional de Franco's ERP, construida en la Fase A de TOGAF. Sirve para mostrar por qué hacemos el sistema y cómo cada requerimiento responde a un objetivo de la organización. Se lee de arriba hacia abajo: primero quién necesita el cambio y qué problemas tiene, luego qué queremos lograr y cómo lo vamos a medir, y al final cómo lo vamos a construir. Cada color representa un tipo de elemento, como se ve en la leyenda."

## 2. Interesados (30 s)

*[Señalar el grupo azul de arriba.]*

> "Arriba están los ocho interesados, que son los actores del sistema. Siete son internos: el Operador de Ventas, de Inventarios, de Insumos, de Producción y de Despacho, el Analista Estratégico y el Administrador. El octavo es el Cliente, el único actor externo, que compra en la tienda en línea.
>
> Cada interesado está encima de la meta que le interesa, y una línea lo une con ella: los cinco operadores con MT-01, el Analista con MT-02, el Administrador con MT-03 y el Cliente con MT-05."

## 3. Impulsores del cambio (25 s)

*[Señalar el grupo naranja de la izquierda.]*

> "A la izquierda están los cinco impulsores, las fuerzas que obligan a Franco's a cambiar: la digitalización de su gestión, la integración de la información entre áreas, la continuidad de la operación, la protección de datos personales que exige la Ley 29733 y la trazabilidad de lotes y conservación de registros. Todos influyen en el objetivo organizacional, por eso sus flechas llegan a la barra verde."

## 4. Objetivos estratégicos y plazo (30 s)

*[Señalar la barra verde grande, la caja verde de la derecha y la caja marrón RS-03.]*

> "La barra verde es el objetivo organizacional OEN-03: optimizar la gestión operativa y estratégica mediante el uso de tecnologías digitales e información. A su derecha está el objetivo de TI que lo soporta, OET-03: implementar soluciones empresariales integradas para digitalizar los procesos operativos y comerciales. Ambos vienen de los mapas estratégicos del Entregable 1.
>
> La caja marrón es la restricción RS-03: las iniciativas TI-002, el ERP, y TI-003, la infraestructura, deben ejecutarse entre el 6 de abril y el 30 de noviembre de 2026."

## 5. Evaluaciones: los problemas actuales (40 s)

*[Señalar la fila amarilla.]*

> "En amarillo están las nueve evaluaciones, que son los problemas encontrados en el diagnóstico del CE0141. Por ejemplo:
> - EV-01: las ventas, el inventario y la distribución se anotan en papel y en Excel, y no pasan a ningún sistema.
> - EV-04: no hay una base de datos donde se junte la información de las áreas.
> - EV-07 y EV-08: no hay servidor ni nube, y la red no tiene redundancia ni detecta fallas.
> - EV-09: no existe un canal de venta en línea.
>
> Cada evaluación apunta a la meta que la resuelve."

## 6. Metas (40 s)

*[Señalar la fila verde claro y los rombos debajo de la barra verde.]*

> "Los objetivos estratégicos son amplios, así que los descomponemos en cinco metas concretas:
> - MT-01: registrar las ventas, los despachos, el inventario y las solicitudes de producción en el ERP.
> - MT-02: dar seguimiento a la estrategia de negocio y de TI en el ERP.
> - MT-03: reunir los datos operativos en una sola base, con copia restaurable y acceso por rol.
> - MT-04: sostener el ERP en una infraestructura propia y en la nube, redundante, segmentada y monitoreada.
> - MT-05: abrir un canal de venta en línea para el cliente.
>
> Las cuatro primeras forman parte de OEN-03 y la quinta de OET-03. Por eso se unen con una relación de agregación, que se reconoce por el rombo del lado del objetivo: el objetivo se compone de sus metas."

## 7. Resultados y medidas (40 s)

*[Señalar la fila turquesa y la fila lila.]*

> "Debajo de cada meta están los resultados esperados, en turquesa, que describen cómo se verá la empresa cuando la meta se cumpla. Por ejemplo, RE-02: el inventario de insumos y de producto terminado llevado en el ERP, con cada producto rastreable hasta su lote.
>
> En lila están las diez medidas con las que comprobamos cada resultado, como MD-03, productos terminados rastreables hasta su lote, o MD-08, disponibilidad del ERP. Cada medida tiene su indicador en el CE0145, con fórmula, línea base, meta y frecuencia. Por ejemplo, la disponibilidad tiene una meta de 95 % o más en horario de trabajo."

## 8. Principios de arquitectura (30 s)

*[Señalar el grupo rosado.]*

> "En rosado están los trece principios de arquitectura: las reglas que guían todas las decisiones de diseño. Por ejemplo, P1 Registro único: cada dato se registra una sola vez. P9 Acceso por rol: cada usuario ve solo lo que le corresponde. P11 Sin punto único de falla. Y P13 Detección y aviso: toda falla se detecta y se avisa a un responsable."

## 9. Requerimientos, restricciones y procesos (50 s)

*[Señalar la fila ocre, las cajas marrones y la fila amarilla de abajo.]*

> "En ocre están los trece requerimientos, que es lo que el sistema debe cumplir. Cada uno realiza uno o más principios. Por ejemplo, RQ-07, respaldo diario fuera de la sede con restauración probada, cumple P2, copia restaurable; y RQ-12, red y conexión a internet redundantes y segmentadas, cumple P11 y P12.
>
> Las cajas marrones son restricciones que condicionan a esos requerimientos:
> - RS-01: SICO ERP sigue como emisor oficial de comprobantes hasta la integración con SUNAT.
> - RS-02: los datos históricos en papel, Excel y Word no se migran.
> - RS-04: los datos se procesan fuera del país, en AWS us-east-1, por eso la demostración usa datos ficticios.
>
> Abajo están los ocho procesos de negocio rediseñados en el Entregable 3, como la validación y formalización de la venta o la recepción de la solicitud de insumos. Estos procesos son los que hacen realidad los requerimientos en la operación diaria."

## 10. Recorrido de ejemplo (40 s)

*[Recorrer con el dedo una columna completa, de arriba hacia abajo.]*

> "Para ver cómo se conecta todo, sigamos una columna. El Operador de Inventarios tiene el problema EV-01: el inventario se lleva en papel y en Excel. Eso motiva la meta MT-01, registrar el inventario en el ERP, que forma parte del objetivo OEN-03. Su resultado es RE-02, cada producto rastreable hasta su lote, y se comprueba con la medida MD-03, cuya meta en el CE0145 es el 100 %. Para lograrlo, el requerimiento RQ-03, registro de lotes y movimientos de inventario rastreables, cumple los principios P1 Registro único y P5 Trazabilidad de lotes, y lo hacen realidad procesos como la actualización y gestión de inventario."

## 11. Cierre (20 s)

> "En resumen, la vista asegura que nada en el sistema esté de más: cada requerimiento cumple un principio, cada meta resuelve un problema real del diagnóstico y se comprueba con una medida, y todo apunta a los objetivos estratégicos OEN-03 y OET-03 de Franco's."

---

## Preguntas que podría hacer el jurado

**¿Por qué las metas se unen a los objetivos con un rombo?**
> "Porque es una relación de agregación: el objetivo se compone de sus metas. MT-01 no es un tipo de OEN-03, sino una parte de él."

**¿Por qué los requerimientos no tienen flechas hacia las metas?**
> "Esas relaciones están en el modelo, pero no se dibujan para que la vista se pueda leer. En el diagrama se muestra la relación de cada requerimiento con sus principios."

**¿Dónde están las metas numéricas de las medidas?**
> "En el CE0145. Cada medida de la vista tiene allí su indicador, con fórmula, línea base, meta y frecuencia. Por ejemplo, MD-08 Disponibilidad tiene una meta de 95 % o más."

**¿Por qué no aparece la gerencia como interesado?**
> "Porque la vista muestra a los actores que usan el sistema, y el ERP no tiene un rol de gerencia: la información estratégica la registra y le da seguimiento el Analista Estratégico."

**¿Qué diferencia hay entre un impulsor y una evaluación?**
> "El impulsor es una fuerza general que empuja el cambio, como la necesidad de digitalizarse. La evaluación es un problema concreto encontrado en el diagnóstico, como que el inventario se lleve en papel."

**¿Qué diferencia hay entre una meta, un resultado y una medida?**
> "La meta es lo que nos proponemos hacer, como registrar el inventario en el ERP. El resultado es el estado final que esperamos, como que cada producto sea rastreable hasta su lote. La medida es cómo comprobamos que ese resultado se logró."

**¿Qué diferencia hay entre un principio y un requerimiento?**
> "El principio es una regla general de diseño, como 'cada dato se registra una sola vez'. El requerimiento es algo concreto que el sistema debe cumplir para respetar esa regla, como 'una base de datos central con un esquema por dominio'."
