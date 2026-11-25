---
name: acta-liquidar-gananciales-sin-acuerdo-contador-perito-civ-2998
description: "Acta para liquidar gananciales sin acuerdo, con contador y perito nombrados por el tribunal. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Acta para liquidar gananciales sin acuerdo, con contador y perito nombrados por el tribunal

> Formulario **CIV-2998** del plugin **Resoluciones judiciales civiles: autos, sentencias y actas** (`formularios-resoluciones-judiciales-civiles`) · Civil › Resoluciones judiciales (autos, decretos, providencias, diligencias) · normativa revisada el 25-11-2026.

## Qué es

ACTA DE COMPARECENCIA PARA LA LIQUIDACIÓN DE LA SOCIEDAD DE GANANCIALES Firmas Acta de la comparecencia llevada a cabo por los cónyuges ante el Letrado de la Administración de Justicia del Tribunal que conoce de su proceso de nulidad, separación o divorcio, al objeto de liquidar la sociedad de gananciales. No llegando las partes a un acuerdo ni en la liquidación ni en la determinación de quiénes serán el Contador y el Perito, se procede a su nombramiento por el Tribunal.

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Acta para liquidar gananciales sin acuerdo, con contador y perito nombrados por el tribunal» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Acta para liquidar gananciales sin acuerdo, con contador y perito nombrados por el tribunal” para mi caso». También puedes invocarla directamente con `/formularios-resoluciones-judiciales-civiles:acta-liquidar-gananciales-sin-acuerdo-contador-perito-civ-2998`.
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
- [ ] COMPLETAR (4 veces)
- [ ] AÑO (2 veces)
- [ ] DNI/NIE (2 veces)
- [ ] NOMBRE DEL REPRESENTADO/A (2 veces)
- [ ] Nº (2 veces)
- [ ] DESCRIBIR

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

### Avisos de actualización (0) — se aplican en el texto, nunca se copian en el documento

- Ninguno.

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Notas al pie del formulario original:
(1) Con referencia a los sistemas de comunidad y separación absoluta, la LEC 1/2000 parte, en todo caso, de agotar las posibilidades de que la liquidación se desarrolle a través de un procedimiento convencional, habida cuenta que al igual que sucede en las particiones hereditarias, en los supuestos de liquidación del régimen matrimonial es esencial la cooperación de las partes. En su defecto, éstas no pueden sino limitarse a presentar propuestas de liquidación particulares e individuales, y en caso de revelarse irreconciliables, se impone la designación de un contador-partidor independiente que formule un plan objetivo.

La disciplina rectora de los procedimientos de liquidación sucesoria constituye aquí un referente obligado.

Luego de realizado el inventario, convencionalmente o por sentencia firme, el Letrado de la Administración de Justicia ordenará por diligencia convocar a los interesados -o al cónyuge supérstite y a los causahabientes del premuerto- a una comparecencia que habrá de celebrarse, en puridad, antes de que transcurran diez días desde la solicitud. Hay que suponer, ante el silencio de la norma, que de haber precedido actuaciones judiciales, la citación de los interesados personados se entenderá con el Procurador que ostente su representación. En otro caso, y si tienen domicilio conocido, los actos de comunicación se entenderán en éstos. Si se ignorase su paradero, después de practicadas las diligencias de averiguación mencionadas en el art. 156 LEC 1/2000 se efectuará la citación por edictos fijados sólo en el tablón de anuncios del órgano judicial, a menos que se solicite por el promovente la inserción de los mismos a su cargo, además, en alguno de los Boletines Oficiales o en un diario provincial o nacional (art. 164.2).

De existir, la citación de los menores, personas con discapacidad o declarados ausentes se entenderá con sus representantes legales -arts. 154.2º, 181, 184, 185, 267, 271.4, 290 C.C.-, si los tuvieren. En otro caso, lo mismo que si, teniéndolos, éstos tuvieren intereses incompatibles con los del representados, hasta el momento en que se les provea de defensor judicial -arts. 163 y 299.1 C.C.-, desempeñará la representación de los mismos el Ministerio Fiscal. La misma representación ejercerá respecto de los ausentes de hecho, que no se hallaren en el lugar del juicio, hasta tanto se presenten o puedan ser habidos.

En dicho acto, puede suceder, al igual que veíamos en el caso de la comparecencia de inventario: a) que exista acuerdo presunto, que el precepto anuda a la incomparecencia sin justa causa del otro cónyuge -o de su representante, defensor o sucesores-; b) que exista acuerdo expreso, porque los comparecidos se avengan a la propuesta inicial formulada por el promovente; c) que los comparecientes manifiesten su oposición al proyecto de liquidación deducida por el solicitante.

En los dos primeros casos, se consignará en el acta el acuerdo y luego de protocolizadas las operaciones se entregarán a los interesados los títulos expresivos de su derecho, conforme a lo prevenido en el art. 788, apdos. 1 y 2 LEC 1/2000.

En el último caso, el objeto de la comparecencia se contrae, en lo sucesivo a la designación de un solo contador-partidor, ora de común acuerdo o, a falta de avenencia, por sorteo de entre los que figuren en una lista que habrá de interesarse del Colegio de Abogados respectivo, integrada por los colegiados ejercientes con despacho abierto en el lugar del juicio y que manifiesten poseer especiales conocimientos en la división y liquidación de patrimonios (vid., art. 341 LEC 1/2000). Sobre el que resulte elegido, luego de aceptar el cargo, recae la función de determinar el número y titulación de los peritos que repute necesarios, con el límite de uno por cada clase de bienes que deban ser valorados, los cuales se elegirán por sorteo en la misma forma indicada (art. 341). Tanto el contador como los peritos que fuesen designados por sorteo podrán ser recusados por las partes.

En lo sucesivo, el procedimiento se acomoda mutatis mutandis a lo dispuesto para las operaciones divisorias en los procedimientos sucesorios (art. 786 y ss.).


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
