# Guion de exposición: Vista motivacional de Franco's ERP (CE0142)

*Duración aproximada: 4 minutos. El texto en cursiva entre corchetes indica qué señalar en el diagrama; todo lo demás es lo que se dice.*

---

## 1. Apertura

Presentamos la vista motivacional de Franco's ERP. En ella mostramos por qué la organización necesita este sistema, qué objetivos persigue y cómo esos objetivos se traducen en los requerimientos que guían el diseño de las iniciativas TI-002, el ERP, y TI-003, la infraestructura.

## 2. Interesados e impulsores

*[Señalar el grupo de interesados y el de impulsores.]*

El sistema tiene ocho interesados. Siete son internos: los operadores de Ventas, Inventarios, Insumos, Producción y Despacho, el Analista Estratégico y el Administrador. El octavo es el Cliente, que se incorpora como actor externo a través de la tienda en línea.

El cambio responde a cinco impulsores: la digitalización de la gestión operativa, estratégica y comercial; la integración de la información entre las áreas; la continuidad de la operación; la protección de datos personales que exige la Ley 29733; y la trazabilidad de lotes y conservación de registros que exigen el D.L. 1062 y el Código Tributario.

## 3. Objetivos estratégicos

*[Señalar OEN-03, OET-03 y RS-03.]*

Estos impulsores influyen en el objetivo organizacional OEN-03, optimizar la gestión operativa y estratégica mediante el uso de tecnologías digitales e información, que está soportado por el objetivo de TI OET-03, implementar soluciones empresariales integradas para la digitalización de procesos operativos y comerciales. Ambos objetivos provienen de los mapas estratégicos que definimos en el Entregable 1.

Para cumplirlos tenemos una restricción de plazo: TI-002 y TI-003 deben ejecutarse entre el 6 de abril y el 30 de noviembre de 2026.

## 4. Evaluaciones

*[Señalar la fila de evaluaciones.]*

Las nueve evaluaciones resumen los problemas que encontramos en el diagnóstico del CE0141. Hoy las ventas, el inventario y la distribución se anotan en papel y en Excel; Producción e Insumos manejan sus solicitudes en papel; no existe una base de datos donde se junte la información de las áreas ni copia de respaldo; el correo no se conecta con ningún sistema; no hay servidor ni nube; la red no tiene redundancia ni detecta fallas; la organización no da seguimiento a su estrategia; y no existe un canal de venta en línea.

## 5. Metas

*[Señalar las cinco metas y la agregación con los objetivos.]*

Para resolver estos problemas, descompusimos los objetivos en cinco metas. Las cuatro primeras forman parte de OEN-03:

- **MT-01**, registrar las ventas, los despachos, el inventario y las solicitudes de producción en el ERP;
- **MT-02**, dar seguimiento a la estrategia de negocio y de TI en el ERP;
- **MT-03**, reunir los datos operativos en una sola base, con copia restaurable y acceso por rol;
- **MT-04**, sostener el ERP en una infraestructura propia y en la nube, redundante, segmentada y monitoreada.

La quinta, **MT-05**, abrir un canal de venta en línea para el cliente, forma parte de OET-03, porque responde a la digitalización de los procesos comerciales. Cada interesado está asociado a la meta que le corresponde: los cinco operadores a MT-01, el Analista Estratégico a MT-02, el Administrador a MT-03 y el Cliente a MT-05.

## 6. Resultados y medidas

*[Señalar las filas de resultados y medidas.]*

Cada meta se realiza mediante resultados concretos, y cada resultado se comprueba con una medida. Definimos nueve resultados y diez medidas. Por ejemplo, la meta MT-04 se realiza cuando el ERP sigue en servicio aunque falle un equipo, un enlace o un proveedor, y eso se comprueba con la disponibilidad del ERP, cuya meta es de 95 % o más en horario de trabajo. Todas las medidas de esta vista tienen su indicador en el CE0145, con su fórmula, línea base, meta y frecuencia.

## 7. Principios y requerimientos

*[Señalar los principios y los requerimientos.]*

El diseño se rige por trece principios de arquitectura. Los más importantes para este sistema son el registro único, que cada dato se registre una sola vez; la trazabilidad de lotes; el acceso por rol; la nube para lo expuesto y la sede para los datos; y que no exista un punto único de falla.

Estos principios se cumplen mediante trece requerimientos. Por ejemplo, el respaldo diario fuera de la sede con restauración probada cumple el principio de copia restaurable, y la red y la conexión a internet redundantes y segmentadas cumplen los principios de no tener un punto único de falla y de separar la red por función.

## 8. Restricciones y procesos

*[Señalar las restricciones y la fila de procesos.]*

Los requerimientos están condicionados por tres restricciones de alcance: SICO ERP sigue como emisor oficial de comprobantes hasta la integración con SUNAT; los datos históricos en papel, Excel y Word no se migran; y los datos se procesan fuera del país, en AWS us-east-1, por lo que la demostración utiliza datos ficticios.

Finalmente, los requerimientos se hacen realidad en los ocho procesos de negocio que rediseñamos en el Entregable 3, desde la validación y formalización de la venta hasta la recepción de la solicitud de insumos.

## 9. Recorrido de ejemplo

*[Recorrer la columna de MT-01 de arriba hacia abajo.]*

Para mostrar la trazabilidad completa, tomemos el caso del Operador de Inventarios. Su problema es que el inventario se lleva en papel y en Excel. Esto se atiende con la meta MT-01, que forma parte de OEN-03. El resultado esperado es que cada producto terminado sea rastreable hasta su lote, y lo comprobamos con la medida de productos terminados rastreables, cuya meta es el 100 %. Para lograrlo, el requerimiento de registro de lotes y movimientos de inventario cumple los principios de registro único y de trazabilidad de lotes, y se ejecuta en procesos como la actualización y gestión de inventario.

## 10. Cierre

En conclusión, la vista motivacional garantiza que cada elemento del sistema tenga una razón de ser: cada requerimiento cumple un principio, cada meta resuelve un problema real del diagnóstico y se verifica con una medida, y todo el diseño apunta a los objetivos estratégicos OEN-03 y OET-03 de Franco's S.A.C.

---

## Respuestas preparadas para el jurado

**¿Por qué las metas se relacionan con los objetivos mediante agregación?**
Porque cada meta es una parte del objetivo, no un tipo de objetivo. OEN-03 se compone de MT-01 a MT-04, y OET-03 de MT-05.

**¿Por qué no se dibujan las relaciones de los requerimientos con las metas?**
Están registradas en el modelo, pero no las mostramos en la vista para mantenerla legible. En el diagrama se muestra la relación de cada requerimiento con los principios que cumple.

**¿Dónde están las metas numéricas de las medidas?**
En el CE0145. Cada una de las diez medidas tiene allí su indicador, con fórmula, línea base, meta y frecuencia.

**¿Por qué no aparece la gerencia como interesado?**
Porque la vista representa a los actores que usan el sistema, y el ERP no tiene un rol de gerencia. La información estratégica la registra y le da seguimiento el Analista Estratégico.

**¿Por qué SICO ERP sigue en operación?**
Porque esta versión del ERP no emite comprobantes electrónicos válidos ante SUNAT. Mientras no se integre, SICO ERP sigue como emisor oficial, y lo registramos como restricción y como riesgo en el CE0144.

**¿Por qué los datos están en la sede y no en la nube?**
Por el principio de nube para lo expuesto y sede para los datos: los portales y el backend corren en AWS, mientras la base de datos de producción se mantiene en la sede, con una base en espera y un respaldo diario en la nube.
