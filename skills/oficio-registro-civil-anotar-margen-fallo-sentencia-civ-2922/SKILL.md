---
name: oficio-registro-civil-anotar-margen-fallo-sentencia-civ-2922
description: "Oficio al Registro Civil para anotar al margen el fallo de la sentencia matrimonial firme. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Oficio al Registro Civil para anotar al margen el fallo de la sentencia matrimonial firme

> Formulario **CIV-2922** del plugin **Resoluciones judiciales civiles: autos, sentencias y actas** (`formularios-resoluciones-judiciales-civiles`) · Civil › Resoluciones judiciales (autos, decretos, providencias, diligencias) · normativa revisada el 25-11-2026.

## Qué es

Oficio librado al Registro Civil para que proceda a la anotación marginal del pronunciamiento principal de la sentencia ya firme de nulidad, separación o divorcio.

Es un modelo de tipo **resoluciones judiciales (autos, decretos, providencias, diligencias)**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Oficio al Registro Civil para anotar al margen el fallo de la sentencia matrimonial firme» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Oficio al Registro Civil para anotar al margen el fallo de la sentencia matrimonial firme” para mi caso». También puedes invocarla directamente con `/formularios-resoluciones-judiciales-civiles:oficio-registro-civil-anotar-margen-fallo-sentencia-civ-2922`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-resoluciones-judiciales-civiles:indice`.

## Qué contiene esta skill

- `SKILL.md` (este fichero): qué es el formulario, para qué sirve, cómo se usa, los datos que pide, las normas que cita, los avisos de actualización y las instrucciones para Claude.
- `assets/formulario.md`: el formulario seco, tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…]. Es el texto que se rellena; no lleva explicaciones.
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Resoluciones judiciales civiles: autos, sentencias y actas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] DESCRIBIR (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] Nº DE PROCEDIMIENTO (2 veces)
- [ ] AÑO
- [ ] COMPLETAR
- [ ] FECHA
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] PÁGINA
- [ ] TOMO

## Normas que cita el formulario

- No cita artículos concretos; Claude localizará las normas aplicables con Jurisprudenciator si el documento las necesita.

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

- Junto a «… DE INSTANCIA SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD DEL TRIBUNAL DE INSTANCIA»: Denominación legal: Sección de Familia, Infancia y Capacidad. Si no existe en el partido, conoce la Sección Civil o la Única (art. 86.3-4 LOPJ). Fuente: LOPJ arts. 84.2.a) y 86 (redacc. LO 1/2025, BOE-A-2025-76).

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Notas al pie del formulario original:
(1) EJECUCIÓN DE SENTENCIAS MATRIMONIALES. PRONUNCIAMIENTO PRINCIPAL. EJECUCIÓN IMPROPIA. INSCRIPCIÓN EN REGISTROS.

Las sentencias matrimoniales, en lo que se refiere a su pronunciamiento principal relativo al vínculo matrimonial, pueden ser objeto de ejecución impropia al participar de la consideración de sentencias mero declarativas y constitutivas, al precisar de algunas actuaciones complementarias destinadas a completar su efectividad, tal como se recoge en el artículo 755 LEC (que, con menores precisiones técnicas, incorpora el contenido de la DA Novena de la Ley 30/1981 y del art. 214 CC), que concreta la regulación general contenida en los artículos 521 y 522 de la LEC.

A diferencia de otras ejecuciones impropias que se practican a instancia de parte, en el ámbito matrimonial se establece la preceptiva actuación de oficio de los Tribunales para la inscripción en el Registro Civil del pronunciamiento de la sentencia relativa al vínculo, mediante el correspondiente mandamiento judicial oportuno (artículo 755 LEC).

Las resoluciones susceptibles de inscripción a que se refiere la norma son las sentencias definitivas, recaídas de forma originaria como las que puedan dictarse en uno posterior, como los autos que decidan acerca de medidas cautelares o sus eventuales modificaciones, adoptadas ex officio o a instancia de parte (arts. 77 LRC 2011 y arts. 261, 263 y 264 RRC 1958).

Los autos de medidas previas o provisionales no tienen acceso al Registro, por no tener el carácter de definitivos.

La norma alcanza a cualesquiera asientos, a los cuales incluso se abstiene de designar. De acuerdo con lo dispuesto en el art. 38 de la Ley del Registro Civil, se anotará, en virtud de mandamiento judicial librado de oficio o a instancia de parte, al margen de la correspondiente inscripción de nacimiento (art. 46 LRC 2011 y art. 150 y ss. RRC 1958), con un valor simplemente informativo "no declarativo", la pendencia del procedimiento cuyo resultado pueda afectar al contenido del Registro. La anotación caduca a los cuatro años de su fecha, "salvo que se prorrogue sucesivamente por igual plazo y con idénticos requisitos", o en el momento en que se extinga el procedimiento (art. 150 RRC 1958), o si se inscribe el hecho concernido (art. 146.2 RRC 1958).

La sentencia firme que modifique el estado civil actual de las personas se inscribirá "obligatoriamente" en el Registro (art. 1.º LRC 2011; art. 82 RRC 1958), al margen de la correspondiente inscripción de nacimiento (art. 46 LRC 2011) o de matrimonio, en su caso (arts. 76 LRC 2011; art. 260.2.º RRC 1958). Si el hecho afecta a la patria potestad sobre los hijos, también se inscribirá al margen de la inscripción de nacimiento de éstos (art. 46.2.º LRC 2011), salvo que sea consecuencia de un hecho inscribible separadamente, en cuyo caso, simplemente se extenderá al margen de la inscripción de nacimiento de los hijos, nota de referencia (art. 180 RRC 1958).

A tal efecto el Tribunal que la dictase "único competente para la ejecución aunque sea «impropia» (art. 61 y 545.1 LEC 1/2000)", de oficio (art. 25 LRC 2011), tan pronto como la sentencia sea firme, librará testimonio bastante de aquélla y lo remitirá al Juez Encargado del Registro Civil. Su eficacia se producirá ex nunc. En tanto ésta no se produzca, la falta de inscripción favorece al tercero a quien no resultarán oponibles ni pararán perjuicio los hechos no inscritos (art. 223 LEC y art. 89 del Código Civil).

Los Tribunales utilizan como medio de comunicación un oficio y en otras ocasiones el exhorto, sin necesidad de esperar a que lo solicite la parte a la que interese ejecutar la sentencia. No obstante, para vencer el posible retraso u olvido del órgano jurisdiccional nada impide la realización de un escrito recordando el cumplimiento del mandato legal.

Muchas veces los Procuradores solicitan la entrega del oficio o del exhorto para llevarlo en mano. No obstante, al tratarse de una actividad de oficio, obligación del Tribunal y sin intervención de parte, parece más adecuado que sea el propio Órgano Judicial el que proceda a la remisión directa (arts. 167 y 172 LEC). No obstante, entendemos que no existe ningún problema en la entrega al Procurador para su cumplimentación, si bien este podrá incurrir en responsabilidad (arts. 168, 172 y 176 LEC).

Pese a lo establecido a lo que pudiera desprenderse del artículo 755 de la LEC (en consonancia con la anterior regulación) la sentencia habrá de comunicarse necesariamente al Registro Civil donde está inscrito el matrimonio y donde figure inscrito el nacimiento de los hijos, si existe algún pronunciamiento que afecte a la patria potestad sobre los hijos.

Junto a dicha comunicación de oficio, también se prevé la anotación de las sentencias, a instancia de parte, en cualquier Registro Público (art. 521 y 755 LEC), principalmente, en los Registros de la Propiedad y Mercantil (para evitar la disposición indebida de algún bien ...), en cuanto pudiera afectar a bienes o actividades mercantiles de ambos cónyuges y su oposición frente a terceros (arts. 89 CC). Así, cuando afecten a la titularidad sobre bienes inmuebles o a derechos reales (arts. 1 y 2 LH 1946), o se refieran a comerciantes individuales podrán anotarse o inscribirse, según los casos, en el Registro de la Propiedad -arts. 2, 26, 42 y 43 LH 1946; arts. 10, 55, 91 y 166 RH 1947- o en el Registro Mercantil -arts. 2, 3, 18, 69, 70, 74, 82 y 83 RRM 1996-.

También podrá solicitarse en otros Registros públicos como el Registro de bienes Muebles, Propiedad Industrial o Intelectual.

Téngase en cuenta, por ejemplo, que ya en fase de medidas previas o coetáneas existen unas necesarias que pueden instarse por alguno de los cónyuges en orden a la revocación de poderes y consentimientos inscribibles en los Registros públicos citados.

En estos casos, y siempre a instancia de parte (sin perjuicio de lo dispuesto en el artículo 162 LEC), se remitirá también testimonio de la sentencia conteniendo los particulares del fallo y se ha de hacer referencia al asunto concreto por el cual se acuerde la anotación o inscripción en el Registro que proceda. En estos supuestos, a diferencia de la anotación en el Registro Civil, parece claro que el procurador de la parte que haya solicitado la ejecución impropia podrá solicitar y el Tribunal deberá entregar el testimonio y oficio, bajo su responsabilidad, con el fin de que sea él quien lo presente ante el Registro correspondiente. En caso contrario, se deberá proceder a la remisión directa.


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
