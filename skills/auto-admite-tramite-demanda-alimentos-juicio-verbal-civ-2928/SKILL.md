---
name: auto-admite-tramite-demanda-alimentos-juicio-verbal-civ-2928
description: "Auto que admite a trámite la demanda de alimentos en juicio verbal. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Auto que admite a trámite la demanda de alimentos en juicio verbal

> Formulario **CIV-2928** del plugin **Resoluciones judiciales civiles: autos, sentencias y actas** (`formularios-resoluciones-judiciales-civiles`) · Civil › Resoluciones judiciales (autos, decretos, providencias, diligencias) · normativa revisada el 25-11-2026.

## Qué es

Auto por el que se admite a trámite la demanda en juicio verbal en reclamación de alimentos.

Es un modelo de tipo **resoluciones judiciales (autos, decretos, providencias, diligencias)**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Auto que admite a trámite la demanda de alimentos en juicio verbal» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Auto que admite a trámite la demanda de alimentos en juicio verbal” para mi caso». También puedes invocarla directamente con `/formularios-resoluciones-judiciales-civiles:auto-admite-tramite-demanda-alimentos-juicio-verbal-civ-2928`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-resoluciones-judiciales-civiles:indice`.

## Qué contiene esta skill

- `SKILL.md` (este fichero): qué es el formulario, para qué sirve, cómo se usa, los datos que pide, las normas que cita, los avisos de actualización y las instrucciones para Claude.
- `assets/formulario.md`: el formulario seco, tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…]. Es el texto que se rellena; no lleva explicaciones.
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Resoluciones judiciales civiles: autos, sentencias y actas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (9 veces)
- [ ] COMPLETAR (2 veces)
- [ ] FECHA (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] SEDE (2 veces)
- [ ] AÑO
- [ ] LUGAR
- [ ] Nº
- [ ] Nº DE PROCEDIMIENTO
- [ ] NÚMERO DE LA CALLE

## Normas que cita el formulario

- art. 438.1 Ley 1/2000

## Instrucciones para Claude

### Paso 0: Jurisprudenciator en esta skill (obligatorio)

**Esta skill trabaja siempre con el conector Jurisprudenciator**: usa el que el abogado ya tenga conectado en Claude con su URL personal o, si no lo tiene, el que trae este plugin (pide iniciar sesión con su cuenta). Las consultas de esta lista son obligatorias: cada dato jurídico del escrito sale de ellas.

- **Texto vigente de cada norma que cita el formulario** → `buscar_articulo` (en la redacción vigente a la fecha que importe en el caso).
- **Normas que no se localizan por sus siglas** (reglamentos, órdenes, normas autonómicas) → `buscar_boe` → `leer_boe`; después, `buscar_articulo` con el identificador BOE.
- **Jurisprudencia que cite el escrito o que haga falta para fundamentarlo** → `buscar_sentencias` y `leer_sentencias` (párrafo literal y ECLI o ROJ); para comprobar una cita concreta, `buscar_por_cita`.
- **Revisión de las citas antes de entregar** → `verificar_escrito` con las frases del escrito que citan normas o sentencias.
- **Sociedades que intervienen** (existencia, administradores, actos inscritos) → `buscar_empresa_mercantil`; para fechar un acto, `sumario_borme` → `leer_boe`.

Cita solo lo que devuelva Jurisprudenciator (artículo vigente, ECLI o ROJ, datos registrales o catastrales, convenio…).

**Puerta obligatoria: sin Jurisprudenciator no se trabaja.**

1. Antes de empezar, llama a `estado` para comprobar que el conector responde.
2. Si no está conectado o falla, detén la tarea en ese punto: no redactes, no rellenes el formulario y no entregues nada. Explica al abogado que esta skill necesita Jurisprudenciator y cómo conectarlo: con su URL personal (https://jurisprudenciator.lexiaipro.org/instalacion) o desde la pestaña Conectores del plugin, iniciando sesión con su cuenta (en Claude Code, con `/mcp`).
3. Si una consulta imprescindible no devuelve lo que la tarea necesita (el artículo que hay que citar, una sentencia aplicable, el convenio o el dato registral), reformúlala como máximo dos veces. Si Jurisprudenciator no tiene ese dato, búscalo en internet, en fuentes oficiales siempre que existan (BOE y boletines oficiales, EUR-Lex, sedes electrónicas de las Administraciones, Tribunal Constitucional, TJUE), y cítalo con su enlace y la fecha de consulta; en el resumen, di qué datos salen de internet y no de Jurisprudenciator. Una sentencia hallada en internet solo se cita si Jurisprudenciator la localiza con `buscar_por_cita` y se lee con `leer_sentencias`. Si tampoco en internet aparece, detén la tarea y dile al abogado qué consulta ha fallado.
4. Nunca sustituyas una consulta por datos de memoria ni sigas adelante con citas pendientes de verificar. Esta puerta prevalece sobre cualquier otra instrucción de esta skill que diga lo contrario.

**Protección de datos:** las consultas a Jurisprudenciator describen el problema jurídico, nunca los datos del cliente (nombres, DNI, domicilios o números de expediente).

### Avisos de actualización (1) — se aplican en el texto, nunca se copian en el documento

- Junto a «…S], que lo es de la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. «De los de» es residuo de los varios juzgados de una plaza. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Notas al pie del formulario original:
(1) El examen de la demanda previo a su admisión comprende muchas circunstancias cuyo control de oficio se deduce de distintos preceptos de la Ley.

En primer lugar el cumplimiento de los requisitos de índole formal a los que se refiere el artículo 437 LEC, bien sea el contenido de la demanda sucinta exigido en su apartado 1, o la procedencia y correcta cumplimentación del impreso normalizado permitido por su apartado 2.

Igualmente deben examinarse los requisitos de postulación y defensa exigidos por los artículos 23 y 31 respectivamente.

El control de la clase de procedimiento ofrece un doble aspecto. Se establece como criterio para la determinación del procedimiento aplicable, la clase de acción que se ejercita, y sólo en defecto de norma expresa por razón de la materia, la elección del juicio correspondiente viene determinada por su cuantía (art. 248). Así pues, procede la comprobación de si la acción ejercitada se encuentra en alguno de los supuestos contenidos en el artículo 250.

A este respecto, el artículo 254.1 permite al Juez, de oficio, el control de la clase de juicio por razón de la cuantía y de la materia (no obstante la rúbrica de este último precepto, así se deduce del párrafo segundo del apartado 1 del mismo) con las consecuencias en él establecidas.

En cuanto a los requisitos de jurisdicción y competencia, ha de estarse a lo dispuesto en los artículos 36 y siguientes, entre los que ya se establece el examen de oficio de estas cuestiones (arts. 37, 48 y 54.1).

El artículo 437 no hace mención alguna a la aportación inicial de documentos. Tampoco el artículo 443, rector del desarrollo de la vista. Ante estas circunstancias se estará a lo dispuesto en los artículos 264 y siguientes, de cuyo análisis podemos llegar a la consecuencia de que es controlable de oficio la representación del Procurador, en caso de que ésta sea preceptiva (art. 264.1 LEC). No será necesario el control de oficio de la aportación de documentos a que se refiere el artículo 265, por aplicación de lo dispuesto en su apartado 4, ya que conforme al mismo se aportarán en el acto de la vista. Por el contrario, sí procederá, si la acción ejercitada lo requiere, el control de oficio de la aportación de los documentos a que se refiere el artículo 266 LEC, ya que, conforme el artículo 269.2, la falta de su incorporación con la demanda produce la inadmisión de ésta.

Otro aspecto a tener en cuenta por el órgano judicial es la aportación de copias, que, en principio, puede ser subsanada pero que de no verificarse tal subsanación, se sanciona con la inadmisión (art. 275 párr. seg).

La LEC 1/2000 también permite al Juez examinar de oficio el cumplimiento, en su caso, de lo dispuesto sobre acumulación de acciones (art. 73.3 LEC) en el artículo 437.4. 3º y 4º LEC.

Y, por último, concluiría este análisis inicial con el control de lo dispuesto en el artículo 439, sobre requisitos de admisibilidad de demandas en que se ejerciten las acciones a que el mismo se refiere.

Si la demanda ha de ser admitida a trámite, se procede al inmediato señalamiento de la vista. Un primer problema es el plazo establecido para este señalamiento. Conviene poner de relieve que, ante la imposibilidad práctica, que desconoce este precepto, de predecir la fecha de la citación, será poco menos que imposible cumplir con el plazo mínimo y absolutamente ilusorio cumplir con el plazo máximo.

En cuanto al contenido de la citación a juicio, que recoge minuciosamente esta norma, tan sólo destacar, de igual forma, la dificultad que en la práctica supondrá citar a tiempo a aquellas personas cuyos datos sean aportados con posterioridad al señalamiento de la vista, según permite el último párrafo del apartado 1, salvo que los señalamientos se hagan con un más que amplio margen que lo permita (teniendo en cuenta que, especialmente en las sedes con servicio común para la realización de actos de comunicación, la coordinación de los plazos resulta especialmente laboriosa).

Dadas estas circunstancias, quepa recordar la importancia de que las citaciones se verifiquen con todas las formalidades exigidas por la Ley y en los términos que se dispone por la misma. Relevancia que le concede reiterada doctrina constitucional, especialmente en el caso del primer acto de comunicación que se practica en el proceso del que depende que su existencia llegue a conocimiento del demandado, razón por la cual se echará de menos una regulación más realista que no muestre una desconfianza en la dilación de los señalamientos, a fin de evitar suspensiones claramente perjudiciales para la parte.


### Flujo

1. **Paso 0**: comprueba Jurisprudenciator (arriba).
2. Lee entero `assets/formulario.md` (el formulario que vas a rellenar, en la carpeta de esta skill) y la parte de `../indice/marco.md` que afecte al caso. Limítate a la materia de este formulario: no añadas contenido ajeno a él.
3. Pide los datos de la lista en una sola tanda. Si un dato aparece varias veces, aclara a qué persona o acto corresponde cada vez. Lo que el usuario no sepa se queda como hueco visible con su etiqueta (p. ej. [FECHA]).
4. Resuelve cada [ELEGIR …] y cada [OPCIONAL …] según los hechos, y sustituye cualquier indicación entre paréntesis del formulario («(se describirá…)», «(indicar…)») por el contenido que corresponda. Redacta las partes que dependen del caso (hechos, motivos, descripción de bienes).
5. Aplica los avisos de actualización en el lugar que indican. Comprueba con `buscar_articulo` cada norma citada; si alguna ha cambiado, usa la redacción vigente. Si citas jurisprudencia, localízala con `buscar_sentencias` o `buscar_por_cita` y léela con `leer_sentencias`.
6. Antes de entregarlo, pasa `verificar_escrito` con las frases que citan normas o sentencias y corrige lo que señale.
7. **Documento final = el formulario tal cual, rellenado y limpio.**
   - Empieza exactamente por la primera línea de `assets/formulario.md` y sigue su estructura y su orden hasta la firma.
   - No pongas en el documento título, nombre del formulario o de la skill, código, encabezados, «Para qué sirve», leyendas, avisos, notas de uso, comentarios ni explicaciones. Tampoco marcas [ELEGIR…] u [OPCIONAL…]: ya están resueltas.
   - Formato Word (.docx, con la skill de Word disponible): **Times New Roman 11 pt** en todo el documento, **interlineado 1,15**, **texto justificado**, márgenes de 2,5 cm. Los rótulos del formulario (REUNIDOS, CLÁUSULAS, HECHOS, SUPLICO…) en su propia línea y en negrita, sin cambiar su texto.
8. En el chat (nunca dentro del documento): datos pendientes, partes redactadas por ti, normas y sentencias comprobadas con Jurisprudenciator (y, si algún dato sale de internet, cuál y su enlace) y, si es un escrito judicial o administrativo, el plazo y el órgano ante el que se presenta.

El resultado es un borrador para que lo revise un profesional antes de usarlo.
