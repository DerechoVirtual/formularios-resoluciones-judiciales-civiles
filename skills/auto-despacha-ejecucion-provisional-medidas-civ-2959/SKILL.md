---
name: auto-despacha-ejecucion-provisional-medidas-civ-2959
description: "Auto que despacha ejecución provisional de medidas patrimoniales antes de remitir la apelación. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Auto que despacha ejecución provisional de medidas patrimoniales antes de remitir la apelación

> Formulario **CIV-2959** del plugin **Resoluciones judiciales civiles: autos, sentencias y actas** (`formularios-resoluciones-judiciales-civiles`) · Civil › Resoluciones judiciales (autos, decretos, providencias, diligencias) · normativa revisada el 25-11-2026.

## Qué es

Es un modelo de tipo **resoluciones judiciales (autos, decretos, providencias, diligencias)**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Auto que despacha ejecución provisional de medidas patrimoniales antes de remitir la apelación» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Auto que despacha ejecución provisional de medidas patrimoniales antes de remitir la apelación” para mi caso». También puedes invocarla directamente con `/formularios-resoluciones-judiciales-civiles:auto-despacha-ejecucion-provisional-medidas-civ-2959`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-resoluciones-judiciales-civiles:indice`.

## Qué contiene esta skill

- `SKILL.md` (este fichero): qué es el formulario, para qué sirve, cómo se usa, los datos que pide, las normas que cita, los avisos de actualización y las instrucciones para Claude.
- `assets/formulario.md`: el formulario seco, tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…]. Es el texto que se rellena; no lleva explicaciones.
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Resoluciones judiciales civiles: autos, sentencias y actas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] COMPLETAR (14 veces)
- [ ] NOMBRE Y APELLIDOS (14 veces)
- [ ] LOCALIDAD (7 veces)
- [ ] NÚMERO (5 veces)
- [ ] FECHA (4 veces)
- [ ] IMPORTE (3 veces)
- [ ] AÑO (2 veces)
- [ ] CALLE
- [ ] CORREO ELECTRÓNICO
- [ ] LUGAR
- [ ] Nº
- [ ] SEDE
- [ ] TELÉFONO

## Normas que cita el formulario

- art. 524.2 LEC
- art. 550 LEC
- art. 525 LEC
- art. 524 LEC
- art. 106 CC
- art. 551.3.1.º LEC
- art. 98 Código Civil

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

### Avisos de actualización (3) — se aplican en el texto, nunca se copian en el documento

- Junto a «…DE FAMILIA, INFANCIA Y CAPACIDAD DEL TRIBUNAL DE INSTANCIA NÚMERO DE [LOCALIDAD]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: Denominación legal: Sección de Familia, Infancia y Capacidad. Si no existe en el partido, conoce la Sección Civil o la Única (art. 86.3-4 LOPJ). Fuente: LOPJ arts. 84.2.a) y 86 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…S], que lo es de la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. «De los de» es residuo de los varios juzgados de una plaza. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Notas al pie del formulario original:
(1) EJECUCIÓN PROVISIONAL DE SENTENCIAS MATRIMONIALES.

Son inejecutables provisionalmente las sentencias dictadas en procesos sobre nulidad de matrimonio, separación y divorcio, salvo los pronunciamientos que regulen las obligaciones y relaciones patrimoniales relacionadas con lo que sea objeto principal del proceso (art. 525.1.1ªLEC).

Este apartado tiene su precedente en el art. 385.3 LEC de 1881, siendo sus diferencias más relevantes las relativas a que: 1. Se ha incluido la referencia a las sentencias dictadas en los procesos de nulidad y separación matrimonial (no expresamente contenida en la normativa anterior) y, 2. por otro, la relativa a que los pronunciamientos de contenido patrimonial incluidos en este tipo de sentencias si son ejecutables provisionalmente (nótese que la norma utiliza un concepto el concepto de patrimonialidad distinto al concepto de "medidas económicas"), lo que sin duda va a evitar interpretaciones confusas, pese a que parecía generalizada la opinión de que podían ser ejecutados provisionalmente los pronunciamientos de contenido patrimonial, incluso, sin prestación de fianza, salvo el pronunciamiento relativo a la pensión compensatoria que precisaba de caución (SAT Barcelona 21 Septiembre 1988; SAP Barcelona (Sec. 14) 3 Octubre 1991), aunque no faltaban opiniones contrarias [SAP Barcelona (Sec. 11) 30 Junio 1993 y SAP Barcelona (Sec. 12) 2 Enero 1996] y otras que diferenciaban entre los diversos pronunciamientos [SAP Vizcaya, Sec. 1, de 25 Marzo 1996].

No obstante, ante la aparente simplicidad de la norma, es preciso armonizar tal previsión sobre la ejecución provisional con lo dispuesto en sede de procesos matrimoniales en relación con las medidas provisionales y definitivas en la nueva Ley de Enjuiciamiento Civil, en especial, con los artículos 774.5 y 806 y siguientes LEC y lo dispuesto en el Código Civil.

En este sentido, ha de resaltarse que las medidas adoptadas en los procesos matrimoniales como provisionales, tienen ejecutividad inmediata y no son objeto de ejecución provisional (el auto de medidas previas, igual que el de coetáneas, no admite recurso alguno conforme a los artículos 771.4 y 773.3 LEC), y no pierden eficacia si no es porque no se presente la demanda dentro de los treinta días siguientes a su adopción, en el caso de medidas previas (artículo 771.5 LEC), o hasta que se ponga fin al procedimiento o sean sustituidas y se transformen en definitivas por una sentencia, en el caso de las medidas provisionales (art. 773.5 LEC en concordancia con el art. 106 Código Civil).

Pero, además, tales medidas definitivas, tampoco pierden su eficacia por el hecho de haber sido recurridas de manera independiente o junto con la sentencia que decida sobre la relación matrimonial, acogiéndose en el ámbito de la ejecución de sentencias matrimoniales, en consonancia con las normas generales, la idea de la eficacia de las medidas acordadas en primera instancia en el caso de impugnación (Art. 774.5 LEC: "Los recursos que, conforme a la ley, se interpongan contra la sentencia no suspenderán la eficacia de las medidas que se hubieren acordado en ésta); así como la idea de ejecución de la última medida acordada, pues parte de la idea de que el juez, en cada fase ulterior, está mejor informado y en mejores condiciones de adaptar las medidas a la realidad cambiante.

Igualmente, es de destacar que los pronunciamientos contenidos en la sentencia o el auto cuando se hayan adoptado de mutuo acuerdo y sean aprobados por el Juez (art. 90 CC), son directamente ejecutables, ya que el art. 777.8 LEC señala que: "El recurso contra el auto que decida sobre las medidas no suspenderá la eficacia de éstas, ni afectará a la firmeza de la sentencia relativa a la separación o al divorcio". Se trata de una ejecución cualitativamente diferente de la dispuesta en la ejecución provisional.

Por otra parte, se plantea el problema sobre cuál ha de ser la interpretación del término patrimoniales que utiliza el artículo 525.1. 1ª de la LEC, ya que no es igual al término "económico" utilizado en otros lugares, sobre todo si se tiene en cuenta que los artículos 771 y 773 LEC permiten la adopción de medidas previas y provisionales con un contenido que supera la esfera patrimonial, y que el art. 774.4. LEC se refiere a los hijos, la vivienda, las cargas, el régimen económico y las cautelas o garantías respectivas (enumeración que entendemos no exhaustiva, debiendo comprenderse la pensión compensatoria y otras indemnizaciones, tales como la correspondiente a la nulidad, o la compensación del trabajo en la casa existente en Cataluña, etc.).

Todo ello nos lleva a concluir que la normativa sobre ejecución provisional en el ámbito de los procesos matrimoniales tiene una aplicación limitada a los pronunciamientos sobre medidas definitivas de contenido patrimonial, apreciándose que en esta materia la nueva ley adopta una posición cambiante, pues se reconoce la eficacia de las medidas y la posibilidad de ejecución provisional respecto de condenas patrimoniales. De no entenderse de esta manera dejaríamos sin aplicación el artículo 774.5 LEC por el artículo 525.1.1ª LEC.

Así, los autores proponen la siguiente interpretación:

- El pronunciamiento relativo al vínculo matrimonial (acción principal sobre estado civil) no es ejecutable provisionalmente, a tenor de lo dispuesto en el art. 521 LEC, al tener naturaleza constitutiva o declarativa. No obstante, si es posible su ejecución si se declara la firmeza parcial de la sentencia en ese punto, siendo lo único discutido en apelación las medidas (art. 774.5 LEC).
- Los pronunciamientos que regulen aspectos de carácter personal y económicos, salvo las estrictamente patrimoniales (realizando una interpretación restrictiva del término patrimoniales distinto al concepto de "medidas económicas"), tienen aparejada ejecución inmediata, sin que quepa oposición, según el artículo 774.5 LEC.
- Los pronunciamientos que regulan las obligaciones y relaciones patrimoniales no son inmediatamente ejecutivos, por lo que su ejecución habrá de pedirse a través de la ejecución provisional, según las normas generales, de acuerdo con el artículo 525.1.1ªLEC [COMPLETAR], por lo que contra el acuerdo despachando ejecución provisional cabe oposición. Aquí habrán de incluirse las prestaciones no periódicas, es decir las indemnizaciones de los artículos 98 y 1438 del Código Civil y 232-5 del Código Civil de Cataluña y la división de bienes comunes del artículo 232-12 de ese mismo código.

No obstante, también podría entenderse que la pensión compensatoria o las indemnizaciones ya citadas, que no aparecen entre las medidas definitivas relacionadas en el artículo 774.4 de la LEC no son ejecutivas al igual que las incluidas específicamente y han de ser objeto de ejecución provisional.

- Los pronunciamientos relativos a la liquidación del régimen económico matrimonial contenidos en la sentencia o la declaración de separación, divorcio o nulidad que conlleva la disolución del régimen económico matrimonial (art. 95 Código Civil), no son ejecutables provisionalmente, pese a que se encuentre mencionada expresamente de forma errónea entre las medidas que han de sustituir las dictadas anteriormente, pues no es una medida que haya podido ser acordada anteriormente como provisional, y, además, requieren para su ejecución la previa firmeza de la sentencia matrimonial según los artículos 810.1 y 811.1 de la LEC. Así, no es posible la ejecución de la disolución del régimen económico matrimonial si se declara la firmeza parcial de la sentencia en cuanto a las medidas, siendo lo único discutido en apelación el pronunciamiento principal (art. 774.5 LEC), ya que la medida se encuentra inexorablemente unida a la nulidad, separación o divorcio, sin que se pueda dar lugar a la disolución del régimen económico mientras que aquel pronunciamiento no sea firme, pese a las dudas que inicialmente pudiera suscitar el texto legal. Por otra parte, si se hubiera adoptado antes la declaración de disolución del régimen económico matrimonial, tendría que haberlo sido en un proceso de separación anterior respecto de uno de divorcio o en uno de nulidad respecto de un precedente de separación o divorcio, pero, incluso en estos casos ya no cabría acordarse de nuevo la disolución.

Ahora bien, los pronunciamientos relativos a la liquidación que se contengan en la sentencia que termina el procedimiento de división del régimen económico matrimonial, cuando no existe acuerdo, que carece de eficacia de cosa juzgada (art. 787.5 segundo párrafo LEC, por remisión del art. 810.5 LEC) tiene aparejada ejecución inmediata (art. 788 LEC), aunque quepa un proceso ordinario posterior.

Igualmente, ha de hacerse notar que no hay una previsión especial sobre las consecuencias de una eventual revocación de las medidas ejecutadas en el ámbito matrimonial por lo que habrá de acudirse a la normativa general (artículos 533 y 534 LEC), lo que no está exento de problemas, por ejemplo, en relación al devengo periódico de prestaciones económicas de naturaleza alimenticia (máxime si se acepta que la voluntad del legislador es la de establecer una ejecución inmediata de las medidas económicas) o pronunciamientos no económicos, como los relativos a las relaciones paterno-filiales y de uso del domicilio familiar, en tanto tales efectos se encuentran consumidos y no son recuperables.


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
