---
name: acta-vista-verbal-alimentos-demandado-incomparecido-civ-2930
description: "Acta de vista del verbal de alimentos con el demandado incomparecido declarado en rebeldía. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Acta de vista del verbal de alimentos con el demandado incomparecido declarado en rebeldía

> Formulario **CIV-2930** del plugin **Resoluciones judiciales civiles: autos, sentencias y actas** (`formularios-resoluciones-judiciales-civiles`) · Civil › Resoluciones judiciales (autos, decretos, providencias, diligencias) · normativa revisada el 25-11-2026.

## Qué es

Acta de vista, en juicio declarativo verbal de reclamación de alimentos, en el que fruto de la inasistencia del demandado, se le declara en rebeldía. La parte actora, solicita el recibimiento a prueba, y propone como medios de prueba, la documental aportada en la demanda y el interrogatorio del demandado.

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Acta de vista del verbal de alimentos con el demandado incomparecido declarado en rebeldía» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Acta de vista del verbal de alimentos con el demandado incomparecido declarado en rebeldía” para mi caso». También puedes invocarla directamente con `/formularios-resoluciones-judiciales-civiles:acta-vista-verbal-alimentos-demandado-incomparecido-civ-2930`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-resoluciones-judiciales-civiles:indice`.

## Qué contiene esta skill

- `SKILL.md` (este fichero): qué es el formulario, para qué sirve, cómo se usa, los datos que pide, las normas que cita, los avisos de actualización y las instrucciones para Claude.
- `assets/formulario.md`: el formulario seco, tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…]. Es el texto que se rellena; no lleva explicaciones.
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Resoluciones judiciales civiles: autos, sentencias y actas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] AÑO
- [ ] FECHA
- [ ] LUGAR
- [ ] NÚMERO

## Normas que cita el formulario

- art. 442 LEC
- art. 440 Ley 1/2000

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

Acta de vista, en juicio declarativo verbal de reclamación de alimentos, en el que fruto de la inasistencia del demandado, se le declara en rebeldía. La parte actora, solicita el recibimiento a prueba, y propone como medios de prueba, la documental aportada en la demanda y el interrogatorio del demandado.

Notas al pie del formulario original:
(1) En primer término conviene destacar que el legislador, al dar contenido al apartado 1 del art. 496, confía en la labor del intérprete conocedor de la rebeldía procesal. La declaración en rebeldía del demandado se produce por su falta de incorporación al proceso al que ha sido llamado, compareciendo en tiempo y forma y constituyéndose formalmente en parte (la desatención de cualquier citación o emplazamiento no significa la declaración en rebeldía. v.gr. la incomparecencia a la prueba de confesión).

La cuestión, no siempre fácil de resolver, es determinar cuándo se da realmente esta ausencia del proceso. La Ley 1/2000, con la escueta norma que se contiene en el apartado 1 del artículo, no soluciona lagunas interpretativas que la aplicación de la dispersa normativa de la LEC de 1881 ha venido poniendo de relieve en la práctica.

Cómo solucionar los supuestos de comparecencia fuera de plazo y anterior a la declaración formal de rebeldía o de comparecencia en plazo pero sin el debido cumplimiento de requisitos de forma, en coordinación con los principios de legalidad procesal (art. 1), Improrrogabilidad de los plazos procesales (art. 134) y la doctrina del Tribunal Constitucional sobre subsanación de defectos formales, será una labor de constante interpretación atendiendo al nuevo sistema procesal que la LEC significa.

Conviene poner de relieve que la declaración en rebeldía del demandado exige la corrección absoluta del acto de comunicación por el que se pone en su conocimiento la existencia del proceso y se le emplaza o cita. Recordemos la reiteradísima doctrina del Tribunal Constitucional sobre los actos de comunicación, especialmente aquellos de los que depende que el demandado tenga conocimiento inicial del proceso. En este punto debemos tener en cuenta lo dispuesto en los arts. 149 y siguientes, a cuyo contenido y comentarios resulta obligada la remisión.

Quede constancia de que la declaración en rebeldía del demandado no siempre supone la inclusión de su identidad en el Registro Central de Rebeldes Civiles (novedad incluida por el legislador en art. 157), que sólo procede cuando resultan infructuosas las averiguaciones practicadas de acuerdo con el apartado 1 de dicho art. 496.

El primero de los efectos que produce la declaración en rebeldía del demandado es el relativo al régimen de los actos de comunicación que deban verificarse en el proceso.

El sistema establecido por esta norma supone una novedad con respecto al régimen que venía estableciendo la LEC de 1881, ya que se abandona el tradicional y formal procedimiento, amén de inútil, de notificación en estrados.

Con quien es declarado rebelde no se practica ningún acto de comunicación salvo las notificaciones de la resolución en que sea declarado en rebeldía y de la resolución -auto o sentencia- que ponga fin al proceso. Ambas resoluciones se notifican en la forma señalada en este precepto, que no ofrece mayor dificultad en su interpretación, aunque conviene dejar constancia de la referencia que hace el legislador a la notificación al demandado, cuando su paradero es conocido, de la resolución por la que se le declara en rebeldía mediante correo. Esta mención es, de un lado, inexacta por insuficiente y de otro, claramente superflua. Da la impresión de que el legislador ingenuamente confía en la buena fe del litigante rebelde, quien aceptará las remisiones por correo. Ha de entenderse que resulta plenamente aplicable lo dispuesto en el art. 152.1.2ª. y 3ª.


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
