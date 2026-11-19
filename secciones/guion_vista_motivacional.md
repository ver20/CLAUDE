# Guion de exposición: Vista motivacional de Franco's ERP (CE0142)

*Duración aproximada: 4 minutos. El texto en cursiva entre corchetes indica qué señalar en el diagrama; todo lo demás es lo que se dice.*

---

## 1. Apertura

Presentamos la vista motivacional de Franco's ERP. En ella mostramos por qué la organización necesita este sistema, qué objetivos persigue y cómo esos objetivos se traducen en los requerimientos que guían el diseño de las iniciativas TI-002 (te i cero cero dos), el ERP, y TI-003 (te i cero cero tres), la infraestructura.

## 2. Interesados e impulsores

*[Señalar el grupo de interesados y el de impulsores.]*

El sistema tiene ocho interesados. Siete son internos: los operadores de Ventas, Inventarios, Insumos, Producción y Despacho, el Analista Estratégico y el Administrador. El octavo es el Cliente, que se incorpora como actor externo a través de la tienda en línea.

El cambio responde a cinco impulsores: la digitalización de la gestión operativa, estratégica y comercial; la integración de la información entre las áreas; la continuidad de la operación; la protección de datos personales que exige la Ley 29733 (veintinueve mil setecientos treinta y tres); y la trazabilidad de lotes y conservación de registros que exigen el D.L. 1062 (decreto legislativo mil sesenta y dos) y el Código Tributario.

## 3. Objetivos estratégicos

*[Señalar OEN-03, OET-03 y RS-03.]*

Estos impulsores influyen en el objetivo organizacional OEN-03 (o e ene cero tres), optimizar la gestión operativa y estratégica mediante el uso de tecnologías digitales e información, que está soportado por el objetivo de TI OET-03 (o e te cero tres), implementar soluciones empresariales integradas para la digitalización de procesos operativos y comerciales. Ambos objetivos provienen de los mapas estratégicos que definimos en el Entregable 1.

Para cumplirlos tenemos una restricción de plazo: TI-002 (te i cero cero dos) y TI-003 (te i cero cero tres) deben ejecutarse entre el 6 de abril y el 30 de noviembre de 2026.

## 4. Evaluaciones

*[Señalar la fila de evaluaciones.]*

Las nueve evaluaciones resumen los problemas que encontramos en el diagnóstico del CE0141 (ce e cero uno cuatro uno). Hoy las ventas, el inventario y la distribución se anotan en papel y en Excel; Producción e Insumos manejan sus solicitudes en papel; no existe una base de datos donde se junte la información de las áreas ni copia de respaldo; el correo no se conecta con ningún sistema; no hay servidor ni nube; la red no tiene redundancia ni detecta fallas; la organización no da seguimiento a su estrategia; y no existe un canal de venta en línea.

## 5. Metas

*[Señalar las cinco metas y la agregación con los objetivos.]*

Para resolver estos problemas, descompusimos los objetivos en cinco metas. Las cuatro primeras forman parte de OEN-03 (o e ene cero tres):

- **MT-01 (eme te cero uno)**, registrar las ventas, los despachos, el inventario y las solicitudes de producción en el ERP;
- **MT-02 (eme te cero dos)**, dar seguimiento a la estrategia de negocio y de TI en el ERP;
- **MT-03 (eme te cero tres)**, reunir los datos operativos en una sola base, con copia restaurable y acceso por rol;
- **MT-04 (eme te cero cuatro)**, sostener el ERP en una infraestructura propia y en la nube, redundante, segmentada y monitoreada.

La quinta, **MT-05 (eme te cero cinco)**, abrir un canal de venta en línea para el cliente, forma parte de OET-03 (o e te cero tres), porque responde a la digitalización de los procesos comerciales. Cada interesado está asociado a la meta que le corresponde: los cinco operadores a MT-01 (eme te cero uno), el Analista Estratégico a MT-02 (eme te cero dos), el Administrador a MT-03 (eme te cero tres) y el Cliente a MT-05 (eme te cero cinco).

## 6. Resultados y medidas

*[Señalar las filas de resultados y medidas.]*

Cada meta se realiza mediante resultados concretos, y cada resultado se comprueba con una medida. Definimos nueve resultados y diez medidas. Por ejemplo, la meta MT-04 (eme te cero cuatro) se realiza cuando el ERP sigue en servicio aunque falle un equipo, un enlace o un proveedor, y eso se comprueba con la disponibilidad del ERP, cuya meta es de 95 % o más en horario de trabajo. Todas las medidas de esta vista tienen su indicador en el CE0145 (ce e cero uno cuatro cinco), con su fórmula, línea base, meta y frecuencia.

## 7. Principios y requerimientos

*[Señalar los principios y los requerimientos.]*

El diseño se rige por trece principios de arquitectura. Los más importantes para este sistema son el registro único, que cada dato se registre una sola vez; la trazabilidad de lotes; el acceso por rol; la nube para lo expuesto y la sede para los datos; y que no exista un punto único de falla.

Estos principios se cumplen mediante trece requerimientos. Por ejemplo, el respaldo diario fuera de la sede con restauración probada cumple el principio de copia restaurable, y la red y la conexión a internet redundantes y segmentadas cumplen los principios de no tener un punto único de falla y de separar la red por función.

## 8. Restricciones y procesos

*[Señalar las restricciones y la fila de procesos.]*

Los requerimientos están condicionados por tres restricciones de alcance: SICO ERP sigue como emisor oficial de comprobantes hasta la integración con SUNAT; los datos históricos en papel, Excel y Word no se migran; y los datos se procesan fuera del país, en AWS us-east-1 (us east uno), por lo que la demostración utiliza datos ficticios.

Finalmente, los requerimientos se hacen realidad en los ocho procesos de negocio que rediseñamos en el Entregable 3, desde la validación y formalización de la venta hasta la recepción de la solicitud de insumos.

## 9. Recorrido de ejemplo

*[Recorrer la columna de MT-01 de arriba hacia abajo.]*

Para mostrar la trazabilidad completa, tomemos el caso del Operador de Inventarios. Su problema es que el inventario se lleva en papel y en Excel. Esto se atiende con la meta MT-01 (eme te cero uno), que forma parte de OEN-03 (o e ene cero tres). El resultado esperado es que cada producto terminado sea rastreable hasta su lote, y lo comprobamos con la medida de productos terminados rastreables, cuya meta es el 100 %. Para lograrlo, el requerimiento de registro de lotes y movimientos de inventario cumple los principios de registro único y de trazabilidad de lotes, y se ejecuta en procesos como la actualización y gestión de inventario.

## 10. Cierre

En conclusión, la vista motivacional garantiza que cada elemento del sistema tenga una razón de ser: cada requerimiento cumple un principio, cada meta resuelve un problema real del diagnóstico y se verifica con una medida, y todo el diseño apunta a los objetivos estratégicos OEN-03 (o e ene cero tres) y OET-03 (o e te cero tres) de Franco's S.A.C.

---

## Respuestas preparadas para el jurado

**¿Por qué las metas se relacionan con los objetivos mediante agregación?**
Porque cada meta es una parte del objetivo, no un tipo de objetivo. OEN-03 (o e ene cero tres) se compone de MT-01 (eme te cero uno) a MT-04 (eme te cero cuatro), y OET-03 (o e te cero tres) de MT-05 (eme te cero cinco).

**¿Por qué no se dibujan las relaciones de los requerimientos con las metas?**
Están registradas en el modelo, pero no las mostramos en la vista para mantenerla legible. En el diagrama se muestra la relación de cada requerimiento con los principios que cumple.

**¿Dónde están las metas numéricas de las medidas?**
En el CE0145 (ce e cero uno cuatro cinco). Cada una de las diez medidas tiene allí su indicador, con fórmula, línea base, meta y frecuencia.

**¿Por qué no aparece la gerencia como interesado?**
Porque la vista representa a los actores que usan el sistema, y el ERP no tiene un rol de gerencia. La información estratégica la registra y le da seguimiento el Analista Estratégico.

**¿Por qué SICO ERP sigue en operación?**
Porque esta versión del ERP no emite comprobantes electrónicos válidos ante SUNAT. Mientras no se integre, SICO ERP sigue como emisor oficial, y lo registramos como restricción y como riesgo en el CE0144 (ce e cero uno cuatro cuatro).

**¿Por qué los datos están en la sede y no en la nube?**
Por el principio de nube para lo expuesto y sede para los datos: los portales y el backend corren en AWS, mientras la base de datos de producción se mantiene en la sede, con una base en espera y un respaldo diario en la nube.

---

## Diapositiva: «Cinco metas llevan OEN-03 a la práctica»

*Duración aproximada: 1 minuto y medio.*

En la vista motivacional vimos que el objetivo OEN-03 (o e ene cero tres) es amplio. En esta diapositiva mostramos cómo lo bajamos a cinco metas concretas, y debajo de cada una indicamos qué brecha del diagnóstico cierra o, si no viene de una brecha, a qué mejora responde.

*[Señalar MT-01.]*
La primera meta, MT-01 (eme te cero uno), es registrar las ventas, los despachos, el inventario y las solicitudes de producción en el ERP. Cierra tres brechas: la B-01 (be cero uno), porque hoy las ventas, el inventario y la distribución no se registran en ningún sistema; la B-03 (be cero tres), porque Excel y Word se usan sin integración; y la B-14 (be catorce), porque Producción e Insumos también registran en papel.

*[Señalar MT-02.]*
La segunda, MT-02 (eme te cero dos), es dar seguimiento a la estrategia de negocio y de TI en el ERP. No nace de una brecha, porque hoy no existe ningún registro de la estrategia que reemplazar: es una mejora que responde directamente a la parte estratégica de OEN-03 (o e ene cero tres).

*[Señalar MT-03.]*
La tercera, MT-03 (eme te cero tres), es reunir los datos en una sola base, con copia restaurable y acceso por rol. Cierra la B-05 (be cero cinco), porque no existe una base de datos central, y la B-09 (be cero nueve), porque la información no tiene copia de respaldo.

*[Señalar MT-04.]*
La cuarta, MT-04 (eme te cero cuatro), es sostener el ERP en la sede y en la nube, con una infraestructura redundante, segmentada y monitoreada. Es la meta de la iniciativa TI-003 (te i cero cero tres) y cierra cuatro brechas tecnológicas: la B-08 (be cero ocho), red e internet sin redundancia; la B-10 (be diez), red sin segmentar; la B-11 (be once), sin servidor ni nube; y la B-12 (be doce), sin monitoreo.

*[Señalar MT-05.]*
La quinta, MT-05 (eme te cero cinco), es abrir un canal de venta en línea para el cliente. Tampoco nace de una brecha, porque hoy ese canal no existe: es una mejora que responde al objetivo de TI OET-03 (o e te cero tres), que soporta a OEN-03 (o e ene cero tres) en la digitalización de los procesos comerciales.

En resumen, las cinco metas cubren las dos caras del objetivo: la gestión operativa, con MT-01 (eme te cero uno), MT-03 (eme te cero tres) y MT-04 (eme te cero cuatro), y la gestión estratégica y comercial, con MT-02 (eme te cero dos) y MT-05 (eme te cero cinco). Cada una tiene sus resultados y sus indicadores, que presentamos en el CE0145 (ce e cero uno cuatro cinco).
