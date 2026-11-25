---
name: acta-comparecencia-liquidar-participacion-ganancias-civ-2997
description: "Acta de comparecencia para liquidar la participación en ganancias sin acuerdo de los cónyuges. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Acta de comparecencia para liquidar la participación en ganancias sin acuerdo de los cónyuges

> Formulario **CIV-2997** del plugin **Resoluciones judiciales civiles: autos, sentencias y actas** (`formularios-resoluciones-judiciales-civiles`) · Civil › Resoluciones judiciales (autos, decretos, providencias, diligencias) · normativa revisada el 25-11-2026.

## Qué es

Diligencia realizada por el Letrado de la Administración de Justicia del Tribunal que dictó sentencia en proceso matrimonial, en cuya virtud se solicitó la liquidación del régimen de participación en las ganancias, compareciendo las partes con el objeto de llevar a cabo la mencionada liquidación, y transcurriendo esta sin que las partes lleguen a un acuerdo, se fija fecha para la vista ante el Juez.

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Acta de comparecencia para liquidar la participación en ganancias sin acuerdo de los cónyuges» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Acta de comparecencia para liquidar la participación en ganancias sin acuerdo de los cónyuges” para mi caso». También puedes invocarla directamente con `/formularios-resoluciones-judiciales-civiles:acta-comparecencia-liquidar-participacion-ganancias-civ-2997`.
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
- [ ] COMPLETAR (4 veces)
- [ ] AÑO (2 veces)
- [ ] DNI/NIE (2 veces)
- [ ] NOMBRE DEL REPRESENTADO/A (2 veces)
- [ ] Nº (2 veces)
- [ ] DESCRIBIR
- [ ] FECHA

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
(1) Al igual que sucede en el artículo 810 LEC 1/2000, subordinar indeclinablemente, habida cuenta de la terminante dicción del precepto, la solicitud de liquidación a la firmeza de la resolución judicial «que declare disuelto el régimen», supone adoptar una visión desenfocada del problema y partir del presupuesto a todas luces erróneo, de ser siempre necesario un previo pronunciamiento jurisdiccional, con olvido -harto censurable tanto si ha sido involuntaria cuanto deliberada- de que los cónyuges pueden pactar en cualquier momento un régimen económico distinto, caso en el cual, conforme al ordinario curso de los acontecimientos, no sólo es innecesario, sino que, de suyo, faltará aquél.

En el régimen de participación no hay más «masa común de bienes y derechos» que aquélla que los cónyuges eventualmente hayan decidido constituir para la atención de la potestad doméstica y, en su caso, los que puedan pertenecerles en proindiviso ordinario por haberlos adquirido conjuntamente (art. 1414 C.C.), o por ignorarse quien los adquirió o abonó.

Únicamente existe para uno sólo de los cónyuges -transitoriamente indeterminado al tiempo de la disolución- un derecho de crédito eventual a participar en el hipotético beneficio -meramente contable- obtenido por el otro, subordinado a que se demuestre superior a las propias ganancias.

El precepto no contempla tampoco explícitamente la formación de inventario, pese a que el art. 1415 C.C. se remite también al art. 1394 C.C. Que -como se cuida de precisar la doctrina (LACRUZ BERDEJO, RAMS ALBESA)- aparezca como cuestionable que el inventario deba concernir al íntegro patrimonio de cada uno de los cónyuges, a menos que el beneficio o ganancia se encuentre presente, indiferenciadamente, en el caudal de cada uno, comprendidas las plusvalías de los bienes; o, diversamente, parezca más conveniente limitarlo sólo a los bienes «que hubieran tenido la condición de gananciales si entre los cónyuges hubiera mediado la sociedad legal», no comporta en modo alguno que quepa prescindir del inventario, señaladamente atendida la remisión del último inciso del art. 806 LEC «a las normas civiles que resulten aplicables».

Consecuentemente, resulta aplicable a este procedimiento mutatis mutandis lo dispuesto en los arts. 808 y 809 LEC 1/2000.

Sin embargo, estamos persuadidos, junto con la mejor doctrina civilista, de que no cabe adoptar las demás medidas previstas en el art. 1394 C.C., señaladamente en cuanto atañe a la administración y necesidad de licencia judicial respecto de los patrimonios particulares.

Pese a que, como sostiene MORALES, en el procedimiento de división pueden intervenir los acreedores de acuerdo con lo prevenido en el art. 403 C.C. ya que «el crédito de participación es un crédito singular que puede desplazar de un cónyuge a otro un importante valor patrimonial; de ahí su profunda incidencia en el patrimonio del deudor, no menos significativa para los acreedores anteriores que la que para ellos comporta la división de una cosa o patrimonio común», el precepto objeto de análisis tampoco se refiere a ella ni contiene normas análogas a la de los arts. 782.5 y 783.5 LEC 1/2000.

Como a tenor del art. 1417 C.C. las ganancias de cada cónyuge se determinan por la diferencia entre los patrimonios inicial y final, es extraordinariamente relevante efectuar una escrupulosa y prolija relación de uno y otro, y su aportación junto con la solicitud que se formule y con la propuesta de liquidación.

De forma enunciativa, y a la luz de lo dispuesto en el art. 1418 C.C., únicamente quedan excluidos del patrimonio inicial: a) Los créditos sometidos a condición resolutoria, cuando la condición se hubiera cumplido; b) los créditos inciertos, cuando el deudor haya devenido insolvente; c) las propinas y gratificaciones; d) los bienes adquiridos por suerte, azar, ocupación o hallazgo; e) los ingresos periódicos con causa gratuita; y, f) las expectativas.

Asimismo, habrá de expresarse y justificarse cumplidamente la determinación actual del valor que tuviere el patrimonio inicial al comienzo del régimen, sin considerar las vicisitudes que hubieren podido sobrevenir ulteriormente, ajustado monetariamente conforme al valor del dinero en el instante de cesar el régimen (art. 1421 C.C.). El ideal consiste en la realización de un inventario notarial y la fijación de un valor convencionalmente aceptado en capitulaciones; y aún resulta óptima la práctica de un inventario privado con expresión de valores reales suscrito por ambos cónyuges. En ausencia de alguna de estas cautelas, la sanción a la falta de prueba del patrimonio inicial, se presumirá que éste no existió, y la expresión de valores cuestionables, inexactos o claramente simulados puede originar enojosas impugnaciones.

Del mismo modo, conforme al art. 1419 C.C., se deducirán las deudas satisfechas y las cargas, monetariamente actualizadas a la finalización del régimen.

El patrimonio final se integra por los bienes y derechos cuya titularidad se ostente al tiempo de cesar el sistema, incluidos los créditos que los cónyuges tengan entre sí, con deducción de las obligaciones pendientes de satisfacer (arts. 1422 y 1426 C.C.), valorados conforme al estado que presentaren, y los bienes y derechos dispuestos a título gratuito sin consentimiento del otro cónyuge, o en fraude de los derechos de éste (arts. 1423 y 1424 C.C.), o perdidos por negligencia injustificable, de acuerdo con el valor que tenían al tiempo de la enajenación y por el que hubieran tenido de haberse conservado. Únicamente se excluyen las donaciones de uso, las remuneratorias, el cumplimiento de las obligaciones jurídicamente inexigibles, los actos dispositivos que no deparen ganancias.

Como regla, la propuesta de reparto de la suma de las ganancias obtenidas por uno y otro cónyuge, y en todo caso en que existan descendientes no comunes ha de ser por mitad (arts. 1427 y 1428 C.C.). Fuera de este último supuesto, al inicio del régimen puede convenirse una participación recíproca, distinta (art. 1430 C.C.).

Formulada la solicitud, lo que presupone la falta de acuerdo de los cónyuges -o entre el supérstite y los causahabientes del premuerto-, incluso a propósito del nombramiento de un arbitrador o perito -nunca un contador, al no haber nada que partir ni adjudicar- para la liquidación extrajudicial, la Ley se empeña en efectuar una última tentativa de convenio disponiendo la convocatoria de los contradictores a una comparecencia cuya celebración ordena dentro de los diez días siguientes al de la presentación de aquélla. El acuerdo puede producirse tácita o presuntamente -dejando de asistir a la comparecencia- o de forma expresa, luego de comparecer al acto (apdo. 4).

No mediando acuerdo, el apdo. 5 prevé una nueva citación a una vista, que continuará por los trámites del juicio verbal. En él, se habrá de concretar, incluso pericialmente, el valor de los respectivos patrimonios y las deudas particulares, y el de las relaciones económicas entre los de uno y otro.

Determinado cuál de los cónyuges resulta acreedor y en qué medida, la sentencia impondrá al deudor el pago del crédito con los intereses legales (art. 1431 C.C.).

Junto a las enunciadas, las únicas cuestiones que pueden suscitarse con ocasión del juicio son: a) la atinente a la eventual imposibilidad provisional o transitoria de satisfacer la deuda, la cual, debidamente justificada, autoriza al Juez a conceder un aplazamiento no superior a tres años previa garantía suficiente del principal y los intereses (art. 1431 C.C.); b) la relativa a la inexistencia de numerario con que abonar la deuda con propuesta de satisfacerla mediante entrega de bienes de su elección; debidamente probada, a falta de acuerdo del cónyuge acreedor, podrá el Juez acceder discrecionalmente a la dación en pago (art. 1432 C.C.).

A su vez, demostrada la inexistencia total o parcial de bienes en el patrimonio del deudor para satisfacer la deuda, estimamos que la sentencia se limitará a declarar el crédito del otro cónyuge y a cuantificar su importe, sin posibilidad de ejecución inmediata dentro del propio procedimiento. Por otro lado, las eventuales acciones impugnatorias que potestativamente puede ejercitar el cónyuge acreedor exart. 1433 C.C. no son, pues, incidentes del proceso de liquidación ni han de sustanciarse en su seno. Repárese que su resultado puede no aprovechar exclusivamente al cónyuge acreedor si existen otros acreedores por deudas anteriores a la disolución del régimen, que serían preferentes (ÁLVAREZ SALA).


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
