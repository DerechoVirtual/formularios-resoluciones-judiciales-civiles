---
name: auto-estima-declinatoria-declara-falta-jurisdiccion-civ-3032
description: "Auto que estima la declinatoria y declara la falta de jurisdicción por inmunidad de jurisdicción. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Auto que estima la declinatoria y declara la falta de jurisdicción por inmunidad de jurisdicción

> Formulario **CIV-3032** del plugin **Resoluciones judiciales civiles: autos, sentencias y actas** (`formularios-resoluciones-judiciales-civiles`) · Civil › Resoluciones judiciales (autos, decretos, providencias, diligencias) · normativa revisada el 25-11-2026.

## Qué es

Modelo de auto judicial que, estimando la declinatoria planteada por la parte demandada, aprecia la falta de jurisdicción de los tribunales españoles por concurrir inmunidad de jurisdicción (Estados extranjeros, agentes diplomáticos, organizaciones internacionales), se abstiene de conocer y sobresee el procedimiento dejando a salvo la acción.

Es un modelo de tipo **resoluciones judiciales (autos, decretos, providencias, diligencias)**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Auto que estima la declinatoria y declara la falta de jurisdicción por inmunidad de jurisdicción» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Auto que estima la declinatoria y declara la falta de jurisdicción por inmunidad de jurisdicción” para mi caso». También puedes invocarla directamente con `/formularios-resoluciones-judiciales-civiles:auto-estima-declinatoria-declara-falta-jurisdiccion-civ-3032`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-resoluciones-judiciales-civiles:indice`.

## Qué contiene esta skill

- `SKILL.md` (este fichero): qué es el formulario, para qué sirve, cómo se usa, los datos que pide, las normas que cita, los avisos de actualización y las instrucciones para Claude.
- `assets/formulario.md`: el formulario seco, tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…]. Es el texto que se rellena; no lleva explicaciones.
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Resoluciones judiciales civiles: autos, sentencias y actas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (4 veces)
- [ ] AÑO
- [ ] DENOMINACIÓN
- [ ] DOCUMENTAL O PRUEBA QUE LO ACREDITA
- [ ] DÍA
- [ ] LOCALIDAD
- [ ] MES
- [ ] NOMBRE Y APELLIDOS
- [ ] Nº DE PROCEDIMIENTO
- [ ] PROVINCIA
- [ ] RAZONAMIENTO SOBRE LA CONCURRENCIA DE LA INMUNIDAD
- [ ] SEDE
- [ ] TIPO DE JUICIO
- [ ] TIPO DE PROCEDIMIENTO

## Normas que cita el formulario

- art. 65 LEC
- art. 64 LEC
- art. 36.2 LEC
- art. 21 LOPJ
- art. 21.2 LOPJ
- art. 66.1 LEC
- art. 458.1 LEC

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

- Al principio del formulario: Se mantiene la nota inicial (orden social: art. 14 LRJS y suplicación, art. 191.3.e y 191.4.a LRJS; LO 16/2015): sus citas son correctas y depende del caso.
- Junto a «…91.3.e y 191.4.a LRJS; LO 16/2015): sus citas son correctas y depende del caso.]»: No se han podido localizar en Jurisprudenciator las SAP Madrid de 20-1-1994 y 8-10-1996, SAP Almería de 15-7-2004, SAP Barcelona de 13-6-1989 ni las sentencias del TPJI (Lotus, Panevezys-Saldutiskis) (sin comprobar).
- Junto a «…1989 ni las sentencias del TPJI (Lotus, Panevezys-Saldutiskis) (sin comprobar).]»: el modelo sigue la tramitación de la declinatoria de la LEC (arts. 63 a 66) y prevé recurso de apelación. Si se dicta en un proceso del orden social, téngase en cuenta que, conforme al art. 14 LRJS, las declinatorias se proponen como excepciones y se resuelven previamente en la sentencia, sin suspender el curso de los autos, y que el régimen de recursos es el de la LRJS (suplicación contra la sentencia que decida sobre la falta de jurisdicción, art. 191.3.e) LRJS; y contra los autos que resuelvan la reposición frente a la resolución que, antes del juicio, declare la falta de jurisdicción, art. 191.4.a) LRJS). Además, la inmunidad de los Estados extranjeros y de las organizaciones internacionales está regulada hoy en la Ley Orgánica 16/2015, de 27 de octubre, sobre privilegios e inmunidades de los Estados extranjeros, las Organizaciones Internacionales con sede u oficina en España y las Conferencias y Reuniones internacionales celebradas en España (en materia de contratos de trabajo, art. 10), y la de los agentes diplomáticos y consulares en las Convenciones de Viena sobre Relaciones Diplomáticas de 1961 y sobre Relaciones Consulares de 1963; el fundamento de derecho tercero debe adaptarse a la norma aplicable al caso.

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

- Ninguna.

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
