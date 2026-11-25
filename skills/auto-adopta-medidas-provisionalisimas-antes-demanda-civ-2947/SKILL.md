---
name: auto-adopta-medidas-provisionalisimas-antes-demanda-civ-2947
description: "Auto que adopta medidas provisionalísimas antes de la demanda de nulidad, separación o divorcio. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Auto que adopta medidas provisionalísimas antes de la demanda de nulidad, separación o divorcio

> Formulario **CIV-2947** del plugin **Resoluciones judiciales civiles: autos, sentencias y actas** (`formularios-resoluciones-judiciales-civiles`) · Civil › Resoluciones judiciales (autos, decretos, providencias, diligencias) · normativa revisada el 25-11-2026.

## Qué es

Auto, no recurrible, por el que se acuerda la adopción inmediata de las medidas provisionalísimas solicitadas previamente a la interposición de la demanda de separación.

Es un modelo de tipo **resoluciones judiciales (autos, decretos, providencias, diligencias)**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Auto que adopta medidas provisionalísimas antes de la demanda de nulidad, separación o divorcio» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Auto que adopta medidas provisionalísimas antes de la demanda de nulidad, separación o divorcio” para mi caso». También puedes invocarla directamente con `/formularios-resoluciones-judiciales-civiles:auto-adopta-medidas-provisionalisimas-antes-demanda-civ-2947`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-resoluciones-judiciales-civiles:indice`.

## Qué contiene esta skill

- `SKILL.md` (este fichero): qué es el formulario, para qué sirve, cómo se usa, los datos que pide, las normas que cita, los avisos de actualización y las instrucciones para Claude.
- `assets/formulario.md`: el formulario seco, tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…]. Es el texto que se rellena; no lleva explicaciones.
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Resoluciones judiciales civiles: autos, sentencias y actas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (11 veces)
- [ ] Nº (3 veces)
- [ ] FECHA (2 veces)
- [ ] AÑO
- [ ] COMPLETAR
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] SEDE

## Normas que cita el formulario

- art. 771.1 Ley 1/2000
- art. 102 Código Civil
- art. 771.1 LEC
- art. 771 LEC
- art. 771.2 LEC
- art. 92 Código Civil

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

- Junto a «…E JUSTICIA. M/ SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Notas al pie del formulario original:
(1) El apdo. 1 del art. 771 de la LEC, reproduciendo la norma contenida en el art. 104 CC permite interesar con anterioridad a la presentación de la demanda la adopción de medidas cautelares --S.A.P. de Barcelona, de 15 de septiembre de 1992 y A.A.P. de Barcelona, Secc. 12ª, de 7 de julio de 1995-- con el designio de armonizar temporal y provisoriamente, en principio --arts. 91 y 106 CC; A.A.T. Valencia, de 19 de enero de 1988 y S.A.P. de Granada, de 8 de septiembre de 1993--, los aspectos patrimoniales y extrapatrimoniales de una unión conyugal en crisis --Cfr., S.A.P. de Badajoz, de 28 de mayo de 1991--.

Pese a las omisiones de la norma, ha de entenderse que la solicitud tanto puede revestir forma escrita como realizarse mediante comparecencia; no ha de sujetarse a solemnidad o fórmula alguna, bastando con que exprese los datos de identificación de los cónyuges interesados, sus domicilios o los lugares en que puedan ser habidos, si existen o no hijos del matrimonio, y en caso afirmativo su identidad y circunstancias, así como las medidas cuya adopción se interesa de acuerdo con lo dispuesto en los arts. 102 y 103 CC.

Se autoriza la presentación de la solicitud ante los órganos jurisdiccionales del lugar en que radique el domicilio del cónyuge instante, que únicamente es fuero subsidiario al de la residencia actual o última de los demandados «que no tuvieren domicilio o residencia fijos» respecto de los procesos principales contenciosos (art. 769.1 párr. segundo LEC), o alternativo en los consensuales (art. 769.2 LEC).

En materia de postulación se modaliza el régimen común de estos procesos (art. 750 LEC 1/2000) al relevarse la necesidad de representación causídica y de dirección letrada para formular la solicitud --lo que coincide, empero, con la regla general de los arts. 23.2, 3º y 31.2, 2º LEC 1/2000--, imponiéndose como preceptiva, en cambio, para las actuaciones subsiguientes.

La norma contempla dos posibles situaciones: a) las que podemos llamar «ordinarias»; y b) las de «urgencia».

a) El procedimiento ordinario, de obligada observancia en cualquier caso, impone que admitida la solicitud se convoque a los cónyuges y, si hubiere hijos menores o personas con discapacidad con medidas de apoyo [NOTA DE REVISIÓN: Desde la Ley 8/2021, de 2 de junio, no existe la incapacitación judicial ni la tutela de mayores de edad: donde el texto dice «incapacitado» debe entenderse persona con discapacidad que cuenta con medidas de apoyo (en su caso, curatela representativa). Fuente: Ley 8/2021.], al Ministerio Fiscal, a una comparecencia --orientada a salvaguardar los derechos prestacionales a la contradicción, a la audiencia bilateral y a la defensa (art. 24.1 C.E.), a celebrar, en principio, dentro de los diez días siguientes --este plazo se dilatará, v. gr., si el cónyuge solicitado interesa la designación de Abogado y Procurador de oficio--. Al acto deberá acudir cada uno de los cónyuges con su propia representación causídica y dirigidos por Letrado.

No dice la norma qué habrá de resolverse si no compareciere ninguno de los cónyuges, limitándose a prever que la sola inasistencia de alguno de ellos únicamente «podrá determinar que se consideren admitidos los hechos alegados por el cónyuge presente para fundamentar sus peticiones sobre medidas provisionales de carácter patrimonial».

En el acto de la comparecencia, pueden darse, a su vez, las siguientes situaciones:

a1) Supuesta la asistencia de ambos cónyuges y la inexistencia de hijos, que medie acuerdo respecto de las medidas a adoptar. En este supuesto, salvo que el Tribunal tenga razones fundadas para rechazar en todo o en parte el contenido de la propuesta presentada, finalizada la comparecencia dictará Auto dentro de tercero día aprobando el convenio. En otro caso, se procederá como en a3).
a2) Supuesta la asistencia de ambos cónyuges y la existencia de hijos del matrimonio menores o personas con discapacidad con medidas de apoyo, que medie acuerdo respecto de las medidas a adoptar. En esta situación, si el Ministerio Fiscal no opusiere objeción alguna en relación con las relativas a los hijos y el Tribunal reputa admisible el contenido de la propuesta presentada, finalizada la comparecencia dictará Auto dentro de tercero día aprobando el convenio. En otro caso, se procederá como en a3).
a3) Si no asistieren ambos cónyuges, o, concurriendo, no mediase acuerdo de los mismos en cuanto a las medidas a adoptar, lo mismo que cuando en alguno de los casos anteriores, el órgano jurisdiccional considere rechazable en todo o en parte la propuesta presentada. En estos casos, oídas las alegaciones de los cónyuges o del que de ellos concurra y, en su caso, el Ministerio Fiscal, se abrirá un trámite para practicar las pruebas conducentes que aquéllos propongan y las que el propio Tribunal estime oportuno acordar de oficio, permitiendo que, si no fuere posible realizarlas todas en el acto, se señale una única audiencia dentro de los diez días siguientes para practicar todas las que falten. La locución «unidad de acto» empleada por la norma parece argüir la imposibilidad de señalar más de una audiencia para prueba, ni aun dentro del plazo legal.

Finalizado uno u otros actos, el Tribunal dictará Auto dentro de tercero día acordando lo procedente, contra el cual no cabe interponer recurso alguno.

b) En los casos de «urgencia», al tiempo que se admite a trámite la solicitud, podrá el Juez acordar mediante Auto «los efectos a que se refiere el art. 102 del Código Civil y lo que considere procedente en relación con la custodia de los hijos y uso de la vivienda y ajuar familiares».

En nuestro criterio, no debería resultar suficiente con el empleo de fórmulas más o menos estereotipadas que reproduzcan la dicción legal o con la mera afirmación de que la urgencia existe, sino que habrán de proporcionarse al órgano jurisdiccional, precisa y circunstanciadamente, los elementos fácticos de los que inducir objetiva y razonablemente la realidad de aquellos asertos.

Contra la resolución del Juez acordando medidas urgentes no cabe interponer recurso alguno (apdo. 2, párr. segundo, in fine). Se acoge así por la norma el criterio mayoritariamente seguido por la jurisprudencia menor --Vid. AA.A.P. de Barcelona, de 15 de septiembre de 1989, 14 de diciembre de 1990; A.A.P. de Barcelona, Secc. 12ª, de 7 de julio de 1995; A.A.P. de Madrid, Secc. 22ª, de 22 de mayo de 1992--.

La subsistencia de las medidas acordadas se subordina a la presentación de la demanda de separación, divorcio o nulidad dentro de los treinta días siguientes a aquel en que se notifique la resolución a los interesados (así, también, LÓPEZ-MUÑIZ GOÑI).

(2) Como decíamos supra, el párrafo 2º del apartado 2 del artículo 771 de la Ley de Enjuiciamiento Civil contempla la posibilidad de que, en los casos de urgencia, el Juez, a la par que cita a la comparecencia a los cónyuges y, en su caso, al Ministerio Fiscal, acuerde de inmediato las medidas a que se refiere el artículo 102 del Código Civil y en relación a la custodia de los hijos y el uso de la vivienda y ajuar familiares, tal y como se preveía en el artículo 1881 de la Ley de Enjuiciamiento Civil 1881 precedente. Las medidas se adoptarán sin dar traslado al otro cónyuge y sin oír al Ministerio Fiscal en el caso de que existan hijos menores de edad.

Esta posibilidad de acordar las medidas mencionadas inaudita parte, ha llevado a algunos autores, como es el caso de LÓPEZ-MUÑIZ GOÑI, a cuestionar su constitucionalidad, por incidir en el derecho a la tutela judicial efectiva, y el perjuicio que se ocasiona a una persona obligándole a salir de su domicilio sin haber sido oído, colocándole en una situación de indefensión. En cualquier caso, tal posibilidad es excepcional pero común a cualquier medida cautelar (vid. artículo 733.2 LEC); y el órgano jurisdiccional deberá examinar con atención los hechos en los que se funde tal petición y concluir acerca de la verosimilitud de los hechos y de la concurrencia de la nota de urgencia en el caso sometido a su consideración, razonando en el Auto su decisión y el porqué de no haber sido oído el otro cónyuge. Si tales circunstancias se apuntasen, parece oportuno adoptar las medidas sin dar traslado, ante la situación de riesgo que pudiera plantearse, pues en cualquier caso, seguirá el trámite de las medidas provisionales previas, teniendo lugar la comparecencia en un lapso de tiempo corto, en la que serán examinadas contradictoriamente las circunstancias que motivaron su adopción y podrían ser modificadas las medidas adoptadas a que se refiere el artículo 102 del Código Civil y en relación a la custodia de los hijos y el uso de la vivienda y ajuar familiares.


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
