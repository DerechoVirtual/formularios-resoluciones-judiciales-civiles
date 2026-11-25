---
name: acta-vista-sobre-medidas-cautelares-proceso-filiacion-civ-2957
description: "Acta de la vista sobre medidas cautelares en un proceso de filiación. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Acta de la vista sobre medidas cautelares en un proceso de filiación

> Formulario **CIV-2957** del plugin **Resoluciones judiciales civiles: autos, sentencias y actas** (`formularios-resoluciones-judiciales-civiles`) · Civil › Resoluciones judiciales (autos, decretos, providencias, diligencias) · normativa revisada el 25-11-2026.

## Qué es

Acta de vista realizada para determinar la adopción de medidas cautelares en el proceso sobre filiación.

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Acta de la vista sobre medidas cautelares en un proceso de filiación» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Acta de la vista sobre medidas cautelares en un proceso de filiación” para mi caso». También puedes invocarla directamente con `/formularios-resoluciones-judiciales-civiles:acta-vista-sobre-medidas-cautelares-proceso-filiacion-civ-2957`.
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
- [ ] COMPLETAR (6 veces)
- [ ] CALLE (4 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] NÚMERO (4 veces)
- [ ] PROFESIÓN (4 veces)
- [ ] AÑO
- [ ] FECHA
- [ ] LUGAR
- [ ] Nº DE PROCEDIMIENTO

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

Acta de vista realizada para determinar la adopción de medidas cautelares en el proceso sobre filiación.

Notas al pie del formulario original:
(1) Los dos primeros apartados del art. 768 incorporan a la LEC 1/2000 los dos párrafos del art. 128 C.C., que expresamente deroga "vid. D. Derogatoria 2, 1.º".

En aras a una mayor protección de los menores o incapaces sobre quienes las personas que ejercen potestades de guarda o administración patrimonial ostentan dicha calidad por razón de la filiación que se impugna, se reclame o no, al propio tiempo otra contradictoria con aquélla, es razonable presumir el peligro en que los primeros se encuentran. Aunque el precepto no se refiere explícitamente a ellas, el mismo riesgo concurre en las acciones de reclamación si la sentencia eventualmente estimatoria apareja la crisis de la titularidad actual de las potestades tuitivas, sean o no las del progenitor las cuestionadas (tutela, curatela, defensor judicial, defensor o representante legal del ausente.

Con anterioridad a la presentación de la demanda, momento al que se retrotrae la litispendencia luego de su admisión, y tras la extinción del litigio, no proceden las medidas protectoras previstas en este precepto sino en otras normas (vid. v. gr., arts. 158 y 167 C.C.). En todo caso, ha de tratarse de medidas idóneas para salvaguardar la situación de peligro que pueda deparar el proceso a la persona o bienes del menor o incapaz, según apreciación discrecional del Juez, atendidas las circunstancias: v. gr., acordar que la patria potestad sea ejercida total o parcialmente por uno de los progenitores o distribuir entre ambos sus funciones (art. 156.V C.C.); determinar la forma en que el progenitor cuya filiación se cuestiona pueda velar por el hijo, comunicar con él y tenerlo en su compañía (arg. exart. 103.1.ª.I C.C.); encomendar el hijo a otra persona o a una institución idónea (arg. exart. 103.1.ª.II C.C.); medidas de aseguramiento de la prestación de alimentos (art. 158, 1.º C.C.); disposiciones para evitar a los hijos las perturbaciones dañosas que pueda aparejar el cambio de titularidad de la potestad de guarda (art. 158.2.º C.C.), apartarle de cualquier peligro o evitarle perjuicios (art. 158.3.º C.C.); o para procurar la seguridad y recaudo de los bienes, exigir cauciones o fianzas para la continuación de la administración o nombrar un administrador (art. 167 C.C.).

A su vez, y con el fin de atender las necesidades de cualquier necesitado de alimentos, aunque sea mayor y capaz "también del nasciturus (art. 29 C.C.), a través de la alimentación de la madre (arg. ex art. 964 C.C. y art. 142.III C.C.)", se autoriza a fijar anticipadamente la prestación de alimentos provisionales sobre el demandado en razón de la filiación reclamada, pese a que no esté aún legalmente determinada. La prestación es provisional tanto por extinguirse si finaliza anormalmente el procedimiento (arg. exart. 106 C.C.) o si se absuelve al demandado, sin perjuicio del derecho que le asiste a repetir lo indebidamente pagado (art. 1894 C.C.); cuanto por la posibilidad de controvertir ulteriormente el derecho mismo a la prestación y su alcance.

Al igual que en relación con las restantes medidas, las potestades del Juez son discrecionales, sin atención rigurosa a los mismos criterios rectores de la prestación en relación con parientes distintos de los hijos. Parece pacífico el criterio de excluir en estos casos la facultad del alimentante conforme al art. 149 C.C. atendida la situación de conflicto derivada del proceso [S.T.S. 15 de febrero de 1983]. Se pueden adoptar, además, las medidas de seguridad que aconseje la prudencia para garantizar la prestación acordada (arg. exarts. 103.3.º, 148.III y 158.1.º C.C.).

Es competente el mismo Juez que conozca del proceso, a quien pueden serle solicitadas por el actor, sin perjuicio de acordarse ex officio. En lo menester resulta aplicable el procedimiento cautelar común, y en materia de audiencia de los afectados "especialmente de los hijos que tuvieren suficiente juicio (arg. exart. 92.II y 154 penúltimo párrafo C.C.)" ahora, por expresa dicción normativa, de los arts. 734 a 736 LEC. No obstante, constatada la urgencia se autoriza a establecer las medidas procedentes de plano, sin perjuicio de diferir la audiencia de los interesados, y con ella, la modificación o alzamiento de las acordadas, a una comparecencia que habrá de celebrarse dentro de los diez días siguientes.

Asimismo y como excepción al régimen común se ha incorporado a la LEC 1/2000 a su paso por el Congreso la posibilidad de relevar de la prestación de fianza al solicitante de las medidas.

COMENTARIOS DE JURISPRUDENCIA:

‐ En tanto no se decida por el juez competente cuál debe ser el correspondiente domicilio conyugal, conforme a la normativa existente en el actual tiempo social de aplicación, y se niegue a integrarse en él la esposa una vez fijado, no puede eximirse el marido de la prestación de alimentos que le viene impuesta por los núms. 1 y 2 art. 143 CC, dado que la facultad de elección que autoriza el art. 149 CC, de pagar la pensión que se fije, o recibir y mantener en la propia casa del obligado al que tenga derecho a los alimentos, únicamente es posible cuando no existe motivo justificativo de la incorporación a la casa del obligado, lo que no puede evidenciarse en tanto el correspondiente juez competente no decida cuál debe ser el domicilio conyugal y, determinado, se niegue a incorporarse a él.

[TS 1.ª S 15 Feb. 1983.- Ponente: Sr. Fernández Rodríguez].

(2) Téngase en cuenta que el acta pormenorizada del acto de la audiencia previa sólo se redactará en el supuesto de imposibilidad de registro en medios audiovisuales, tal como previene el art. 187.2. LEC


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
