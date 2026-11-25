---
name: auto-declara-falta-competencia-territorial-tras-civ-2971
description: "Auto que declara la falta de competencia territorial tras la demanda por existir fueros electivos. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Auto que declara la falta de competencia territorial tras la demanda por existir fueros electivos

> Formulario **CIV-2971** del plugin **Resoluciones judiciales civiles: autos, sentencias y actas** (`formularios-resoluciones-judiciales-civiles`) · Civil › Resoluciones judiciales (autos, decretos, providencias, diligencias) · normativa revisada el 25-11-2026.

## Qué es

Auto, no recurrible, por el que el órgano jurisdiccional establece su falta de competencia territorial para el conocimiento del proceso de separación, nulidad o divorcio, inhibiéndose del mismo. Ambos cónyuges, residen actualmente en localidades pertenecientes a municipios distintos al de su demarcación. Al ser fueros electivos, la parte actora tendrá un plazo de cinco días para manifestar a qué órgano han de remitirse las actuaciones.

Es un modelo de tipo **resoluciones judiciales (autos, decretos, providencias, diligencias)**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Auto que declara la falta de competencia territorial tras la demanda por existir fueros electivos» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Auto que declara la falta de competencia territorial tras la demanda por existir fueros electivos” para mi caso». También puedes invocarla directamente con `/formularios-resoluciones-judiciales-civiles:auto-declara-falta-competencia-territorial-tras-civ-2971`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-resoluciones-judiciales-civiles:indice`.

## Qué contiene esta skill

- `SKILL.md` (este fichero): qué es el formulario, para qué sirve, cómo se usa, los datos que pide, las normas que cita, los avisos de actualización y las instrucciones para Claude.
- `assets/formulario.md`: el formulario seco, tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…]. Es el texto que se rellena; no lleva explicaciones.
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Resoluciones judiciales civiles: autos, sentencias y actas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (4 veces)
- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] COMPLETAR (3 veces)
- [ ] FECHA (2 veces)
- [ ] SEDE

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

- Junto a «…S], que lo es de la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. «De los de» es residuo de los varios juzgados de una plaza. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Notas al pie del formulario original:
(1) Siguiendo la línea marcada por la Disposición Adicional Tercera de la Ley 30/1981, la competencia territorial se atribuye en los procesos de separación, nulidad o divorcio al órgano jurisdiccional en que radique el domicilio del matrimonio; para el caso de que los cónyuges residan en distintos partidos judiciales la norma prevé dos fueros concurrentes en régimen rigurosamente alternativo: el del último domicilio conyugal y el de la residencia del demandado, --STS Sala Primera, de 20 de noviembre de 1990--, pudiendo, los que carezcan de domicilio o residencia fijos ser demandados, a elección del cónyuge actor, ante los Tribunales del lugar en que aquéllos se encuentren o del en que radicase su última residencia, estableciéndose como fuero subsidiario final el del domicilio del demandante. Sorprende, sin embargo, que la LEC 1/2000 no subvenga a la carencia, largamente sentida, de establecer un fuero para el caso de que los Tribunales españoles ostenten jurisdicción y ni el matrimonio ni ninguno de los cónyuges haya tenido nunca fijado su domicilio o residencia en territorio español (artículo 22.3 de la Ley Orgánica del Poder Judicial)

En los procesos de separación o divorcio promovidos de mutuo acuerdo se establece como fuero territorial, en régimen concurrente alternativo, el último lugar del domicilio conyugal o el del domicilio de cualquiera de los solicitantes.

El apartado tercero del mismo artículo 769 de la LEC disciplina los fueros aplicables a los procesos en que se controvierta sobre la guarda y custodia de los hijos menores o sobre alimentos que reclame uno de los progenitores, actuando en nombre y representación de los hijos menores, frente al otro. La regulación resulta, en este particular, innecesariamente compleja. Así, la dicción literal parece distinguir formalmente el caso de que los progenitores hayan tenido en algún momento un domicilio común, --pues a eso hace referencia el término "último"--, de aquél otro en que los progenitores residan en distintos partidos judiciales, hipótesis ambas que en modo alguno resultan incompatibles entre sí. Estamos persuadidos de que el precepto realmente quiere diferenciar los casos en que al tiempo de promoverse el proceso los progenitores residan o no en un mismo partido judicial.

Finalmente, se impone al Juez en este precepto el deber de analizar ex officio e inicialmente su propia competencia territorial, resultando ineficaz cualquier determinación convencional de esta clase de competencia. Téngase en cuenta que el artículo 58 de la LEC establece también que cuando la competencia territorial venga fijada por reglas imperativas, el LAJ examinará la competencia territorial inmediatamente después de presentada la demanda y, previa audiencia del Ministerio Fiscal y de las partes personadas, si entiende que el Tribunal carece de competencia territorial para conocer del asunto, dará cuenta al Juez para que resuelva lo que proceda. La resolución que declara la incompetencia territorial del órgano jurisdiccional deberá adoptar la forma de auto y en el mismo se acordará remitir las actuaciones al Tribunal que se considere territorialmente competente, aunque, si fueran de aplicación fueros electivos, el Tribunal estará a lo que manifieste el demandante, tras el requerimiento que se le dirigirá a tales efectos.

Parece que no puede haber obstáculo en que el órgano jurisdiccional aprecie su propia incompetencia territorial en un momento posterior a la admisión de la demanda, toda vez que, tratándose de normas de orden público, otra tesis conduciría a la posibilidad de que se fallara un pleito por un órgano que se sabe territorialmente incompetente. Además, la necesidad contemplada en el precepto de dar audiencia a "las partes personadas" parece militar también en este sentido, pues, en otro caso, habría bastado con referirse a la parte actora.

Conviene, por último, destacar, conforme ya hiciera el C.G.P.J. en su informe al anteproyecto de LEC, el distinto tratamiento que el texto legal dispensa a los supuestos de apreciación de falta de competencia objetiva (en los que el auto que la declara se limita a indicar la clase de órgano jurisdiccional al que corresponde el conocimiento del asunto) y los supuestos de apreciación de falta de competencia territorial, en los que deben ser remitidas las actuaciones al órgano que se considera competente, no por la parte sino por el órgano jurisdiccional mismo.


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
