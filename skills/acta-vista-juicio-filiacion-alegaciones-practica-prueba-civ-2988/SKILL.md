---
name: acta-vista-juicio-filiacion-alegaciones-practica-prueba-civ-2988
description: "Acta de la vista en juicio de filiación con alegaciones y práctica de prueba. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Acta de la vista en juicio de filiación con alegaciones y práctica de prueba

> Formulario **CIV-2988** del plugin **Resoluciones judiciales civiles: autos, sentencias y actas** (`formularios-resoluciones-judiciales-civiles`) · Civil › Resoluciones judiciales (autos, decretos, providencias, diligencias) · normativa revisada el 25-11-2026.

## Qué es

Acta de vista ante el Juez, seguida en juicio sobre filiación, en el que se recogen las alegaciones de las partes y la práctica de las pruebas solicitadas por éstas.

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Acta de la vista en juicio de filiación con alegaciones y práctica de prueba» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Acta de la vista en juicio de filiación con alegaciones y práctica de prueba” para mi caso». También puedes invocarla directamente con `/formularios-resoluciones-judiciales-civiles:acta-vista-juicio-filiacion-alegaciones-practica-prueba-civ-2988`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-resoluciones-judiciales-civiles:indice`.

## Qué contiene esta skill

- `SKILL.md` (este fichero): qué es el formulario, para qué sirve, cómo se usa, los datos que pide, las normas que cita, los avisos de actualización y las instrucciones para Claude.
- `assets/formulario.md`: el formulario seco, tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…]. Es el texto que se rellena; no lleva explicaciones.
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Resoluciones judiciales civiles: autos, sentencias y actas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (13 veces)
- [ ] CALLE (4 veces)
- [ ] COMPLETAR (4 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] NÚMERO (4 veces)
- [ ] PROFESIÓN (4 veces)
- [ ] ACTO O RESOLUCIÓN
- [ ] AÑO
- [ ] FECHA
- [ ] LUGAR
- [ ] NOMBRE DEL SOLICITANTE
- [ ] Nº

## Normas que cita el formulario

- art. 301 LEC
- art. 440 LEC

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

Acta de vista ante el Juez, seguida en juicio sobre filiación, en el que se recogen las alegaciones de las partes y la práctica de las pruebas solicitadas por éstas.

Notas al pie del formulario original:
(1) Téngase en cuenta que el acta pormenorizada del acto de la audiencia previa sólo se redactará en el supuesto de imposibilidad de registro en medios audiovisuales, tal como previene el art. 187.2. LEC

(2) El artículo 752 expresa la abolición de los principios de aportación de parte, dispositivo y de preclusión en materia probatoria, aunque sin detrimento de la debida contradicción, salvedad hecha de los elementos o componentes pretensionales de índole complementaria que, en su caso, puedan yuxtaponerse a aquélla, y que por su naturaleza "de ordinario, estrictamente patrimonial", no les alcanza la naturaleza de interés público.

El órgano judicial que conozca del proceso en cualquiera de las dos instancias ordinarias, no ha de atender únicamente a los hechos introducidos por las partes, ni de ellos sólo a los que lo hayan sido en el período alegatorio que resulte oportuno conforme a las reglas generales (Vid. arts. 286.4). A su vez, y sobre ser ésta una de las ocasiones en que, de acuerdo con la previsión del art. 282 in fine LEC 1/2000, la Ley autoriza al órgano judicial a practicar pruebas de oficio, no rige la fijación de hechos por admisión tácita o expresa, de acuerdo con lo dispuesto en los arts. 281.3. Repárese en que un proceder diverso podría valer tanto como una transacción, prohibida por el art. 751.1 de la Ley.

Si bien no se impide medio alguno de prueba, se modula asimismo su régimen: la incomparecencia de la parte cuyo interrogatorio se hubiese acordado no permitirá, por sí sola y automáticamente, «considerar reconocidos como ciertos los hechos» a que se refiera (Vid. art. 307.1 LEC 1/2000); la negativa a declarar, aunque no concurra obligación legal de guardar secreto, o las respuestas evasivas o inconcluyentes tampoco aparejarán aquella consecuencia (Vid. art. 307.2 LEC 1/2000). Los documentos públicos no harán, necesariamente, prueba plena de los hechos, actos o estados de cosas que documenten y demás circunstancias a que se refiere el art. 319.1 LEC 1/2000; lo mismo es predicable respecto de los documentos privados, aunque su autenticidad no se impugnase por la parte perjudicada ex art. 326.1 LEC 1/2000.

Tampoco rige una estricta preclusión en punto a su práctica ni de su realización intempestiva puede derivarse, en rigor, sanción alguna para las partes proponentes de las mismas (ex art. 288 LEC 1/2000), de forma que cualquiera que sea el tiempo en que se realicen su virtualidad y eficacia no se verá afectada.

(3) El acto de la vista, cuya finalidad principal es la práctica de prueba, se desarrolla según lo establecido en el artículo 443 de la Ley para el juicio verbal (art. 753 LEC).

En principio resultan aplicables a la actividad probatoria las normas generales establecidas en los artículos 281 y siguientes de la Ley, si bien debemos tener en cuenta el legislador pretende que todas las pruebas se realicen en el acto de la vista, lo que, siendo difícil en el ejercicio de otras acciones, posiblemente lo sea más en el ejercicio de las acciones de filiación. A fin de salvar este escollo no debemos olvidar lo dispuesto en los artículos 290 y 193 de la Ley.

La Ley 1/2000 establece como característica relevante de esta clase de procesos ciertas especialidades en materia de prueba. En el apartado 2. del artículo 767 se recoge la norma que enunciase el art. 127.1 C.C., que desarrollara la previsión del art. 39 C.E., permitiendo la investigación de la filiación auténtica por toda clase de pruebas, siempre, claro está, que se cuestione la realidad de la filiación. El precepto se completa ahora con la previsión expresa del criterio dimanante del criterio mantenido por la doctrina emanada del Tribunal Constitucional y de la Sala Primera del Tribunal Supremo, a propósito de que la sola resistencia a colaborar en la determinación de la filiación mediante el sometimiento a las pruebas biológicas no conduce inexorablemente al acogimiento de la pretensión deducida, como si de una confesión se tratase, a menos que existan indicios suficientemente reveladores, de suyo, de la filiación controvertida "atinentes, v. gr., al desarrollo del feto y duración conocida del embarazo; y a las presunciones del apartado 3. de este mismo precepto", o la prueba directa de aquélla no haya podido obtenerse razonablemente por medios distintos "v. gr., por secreto profesional".

El apartado 3. complementando el número precedente incorpora, en lo sustancial, la disposición del art. 135 C.C. (también derogado por la Disposición Derogatoria 2.1º. de la Ley). Habida cuenta de las dificultades que comúnmente presenta la posibilidad de contar con pruebas directas, especialmente cuando mayor sea el tiempo transcurrido, se facilita la determinación de un estado civil básico autorizando el recurso a elementos que, en atención a las circunstancias concurrentes, el Juez puede valorar libremente y, en su caso, concurriendo los requisitos precisos "plena certidumbre del hecho indiciario; enlace lógico entre aquéllos y el que se quiere colegir, de forma que la conclusión no resulte absurda o inverosímil, aunque no se excluye en absoluto el error; señaladamente", fundar en ellos la filiación presunta.

En la relación del precepto, meramente enunciativa, se contemplan:

a) El reconocimiento expreso o tácito, o admisión unilateral de la propia maternidad o paternidad a la que, por faltarle alguno de los requisitos necesarios, no resulte eficaz, por sí sola, como título de determinación legal, incluso aunque posteriormente se hubiere revocado. Ni siquiera el efectuado en prueba de confesión "pese a que difícilmente será mendaz al tratarse de un hecho «perjudicial»" dentro del propio proceso libera al favorecido por ella de cualquier otra actividad probatoria, ni vincula al Juez, al tratarse de litigios cuyo objeto se encuentra sustraído al poder de disposición de las partes (vid. art. 751). La amplitud de la norma permite otorgar validez al reconocimiento, directo o incidental, que conste en cualquier forma, incluso por actos concluyentes (vid. Ley 11 de Toro).
b) La posesión de estado, o goce de hecho, de modo público y dotado de cierta continuidad o permanencia y evidenciado por actos directos y propios del progenitor o de su familia, del estado de hijo en las relaciones familiares y sociales, le corresponda o no efectivamente (PEÑA BERNALDO DE QUIRÓS). Se da, en tanto subsista, cuando concurren los tres requisitos clásicos: nomen (ser designado como «hijo»; utilización del apellido en los casos de filiación matrimonial); tractatus (ejercicio de la autoridad parental, prestación de alimentos, etc.); y fama, o reputación social y, especialmente, familiar, como tal hijo.

Al igual que en el caso del reconocimiento, constituye mero hecho indiciario cuando le falta algún requisito "ordinariamente, haber dejado de ser actual" para ser, por sí, título de legitimación, aun cuando no sea formalmente impugnada, siempre que no resulte notoriamente o como consecuencia de otras circunstancias acreditadas, contraria a la realidad.

c) La convivencia con la madre en la época de la concepción, esto es, la unión de hecho, estable "no meramente ocasional" de los progenitores. A diferencia de los precedentes, no es, por sí sola, título de determinación legal de la filiación. Como regla, aunque en algún caso singular pueda admitir excepciones, requiere acreditar que la convivencia se inició al menos ciento ochenta días antes del nacimiento o que entre éste y el cese de aquélla no transcurrieron más de trescientos días (arts. 116 y 117 C.C.).
d) Los «otros hechos de los que se infiera la filiación, de modo análogo», requieren que los mismos permitan colegir o presumir la filiación pretendida, de forma tan vehemente como las circunstancias expresamente mencionadas. Entre otras, sugiere la doctrina más autorizada las relaciones maritales notorias con mujer no pública aunque no exista convivencia; la fecundación artificial; y la aceptación de esponsales o la convivencia conociendo el embarazo.

Recordemos que la Ley 1/2000 regula la prueba de presunciones en los artículos 385 y 386.


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
