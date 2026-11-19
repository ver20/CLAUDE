# Guion de exposición: Organigrama funcional y Mapa de la defensa

*Defensa de Infraestructura TI · láminas 9 y 10 · duración aproximada: 3 minutos y medio. El texto en cursiva entre corchetes indica qué señalar; todo lo demás es lo que se dice. Entre paréntesis va cómo se pronuncia cada sigla.*

*La lámina 9 viene después de «¿Por qué Franco's necesita esta solución?». Después de la lámina 10 empieza la sección A, Infraestructura implementada, con la vista global de Rubén Salazar.*

---

## Lámina 9 · «Organigrama funcional y roles»

*Aproximadamente 2 minutos.*

**Apertura**
Ya vimos por qué Franco's necesita esta solución. Ahora mostramos quién la gobierna y quién la ejecuta. Este organigrama no es el de la empresa, sino el del SGSI (ese ge ese i), el sistema de gestión de seguridad de la información: muestra cómo se reparten las responsabilidades entre los diez integrantes del equipo.

**Nivel de dirección**
*[Señalar las tres cajas de arriba.]*
Arriba está la Alta Dirección, que es el patrocinador del proyecto, a cargo de Jorge Chavarri. Rinde cuentas ante ella el Comité de Seguridad, que es el órgano que toma las decisiones del SGSI. En el comité votan Chavarri, Lanche, Sauñe y yo, y Rubén Salazar participa como secretario sin voto. A la derecha está la Auditoría de controles y marco normativo, a cargo de Roxwell Ramos, que asiste como invitado sin voto: así la auditoría puede evaluar al comité sin ser parte de sus decisiones.

Debajo del comité está la Dirección del SGSI, el CISO (ciso), que es Rubén Salazar. Su papel es coordinar todas las funciones del equipo.

**Funciones de gestión del SGSI**
*[Señalar la fila de cajas moradas.]*
Las cajas moradas son las funciones que gestionan la seguridad:
- **Contexto y alcance**, a mi cargo: defino las partes interesadas y hasta dónde llega el SGSI.
- **Riesgos y respuesta**, a cargo de Uziel Sauñe: la matriz de riesgos, las pruebas de seguridad y la respuesta a incidentes.
- **Activos y servicios**, a cargo de Pamela Vallejos: el inventario de activos y la mesa de ayuda en GLPI (ge ele pe i).
- **Continuidad y recuperación**, a cargo de Piero Lanche: cómo se recupera la operación ante una falla grave.
- **Infraestructura y arquitectura**, a cargo de Rubén Salazar, que articula la parte técnica.

**Funciones de ejecución técnica**
*[Señalar la fila de cajas verdes.]*
Las cajas verdes son las funciones que construyen y operan la infraestructura:
- **Red, perímetro y monitoreo**, con Rubén Salazar;
- **Nube, infraestructura como código e identidad federada**, con Piero Lanche;
- **Virtualización y gestión de cambios**, con Evans Chacón;
- **Bases de datos**, con la PostgreSQL (postgres cu ele) del ERP, a cargo de Joel Rivera;
- y **Cableado y planta física**, con Joshua Pedraza.

**Cierre**
*[Señalar la nota de abajo.]*
Cada función tiene su número en la matriz RACI (rasi) vigente al 16 de noviembre de 2026, donde se indica quién ejecuta, quién aprueba, a quién se consulta y a quién se informa. Las líneas del organigrama muestran coordinación, no jerarquía: así cada control del SGSI tiene un responsable claro.

---

## Lámina 10 · «Mapa de la defensa»

*Aproximadamente 1 minuto y medio.*

**Apertura**
Con los roles claros, este es el recorrido de nuestra defensa. Sigue la misma lógica con la que se construye un SGSI.

**La cadena**
*[Recorrer las siete cajas de izquierda a derecha.]*
Partimos de la **empresa** y sus **procesos**, que es lo que acabamos de presentar en la apertura: por qué y para qué. De los procesos identificamos los **activos** que los sostienen; de los activos, los **riesgos** que los amenazan; y para esos riesgos definimos **controles**. Esos controles se materializan en la **implementación** de la infraestructura, y todo se comprueba con **evidencia**.

**Las secciones**
*[Señalar las barras de abajo.]*
Estas etapas se reparten en las secciones de la defensa:
- la **apertura**, que ya presentamos, explica el porqué;
- la **sección B, SGSI aplicado**, cubre los activos, los riesgos, la declaración de aplicabilidad y la operación;
- la **sección A, Infraestructura**, muestra lo construido, de abajo hacia arriba;
- y la **auditoría** mide los resultados y cierra el ciclo.

**La regla de la defensa**
*[Señalar el texto de abajo.]*
Aunque en la lógica del SGSI los riesgos van antes que la implementación, en la exposición presentamos primero lo que funciona, la sección A, y después cómo lo gobernamos, la sección B. Así cada control del que hablemos ya lo habrán visto funcionando. Y seguimos una regla: lo que solo está diseñado lo presentamos como diseño, no como algo hecho.

**Pase**
Empezamos entonces por la infraestructura implementada, con la vista global que presenta Rubén Salazar.

---

## Respuestas preparadas para el jurado

**¿Por qué el auditor no vota en el comité?**
Para mantener su independencia: si votara las decisiones, después estaría auditando sus propias decisiones.

**¿Por qué Rubén Salazar es CISO y además ejecuta funciones técnicas?**
Porque el equipo es pequeño. Para equilibrarlo, Rubén participa en el comité como secretario sin voto: coordina y ejecuta, pero las decisiones las toma el comité.

**¿Por qué presentan la infraestructura antes que el SGSI, si los riesgos van primero?**
Porque queremos que el jurado vea los controles funcionando antes de explicar cómo los gobernamos. La lógica del SGSI se mantiene en el mapa; solo cambia el orden de la exposición.

**¿Qué significa que algo «solo está diseñado»?**
Que está definido en los documentos pero todavía no está implementado. Lo decimos así para no presentar como hecho algo que aún no funciona.

**¿Qué es la matriz RACI?**
Es la tabla que indica, para cada función, quién la ejecuta (R), quién la aprueba (A), a quién se consulta (C) y a quién se informa (I).
