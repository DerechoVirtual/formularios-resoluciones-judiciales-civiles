---
name: indice
description: "Índice de los 236 formularios de Resoluciones judiciales civiles: autos, sentencias y actas. Úsala cuando el usuario pida un documento de esta materia y no esté claro qué formulario usar: propone el adecuado y lo abre. Requiere Jurisprudenciator."
---

# Resoluciones judiciales civiles: autos, sentencias y actas: índice de formularios

> Plugin `formularios-resoluciones-judiciales-civiles` · 236 formularios · normativa revisada el 25-11-2026.

## Qué es

Modelos de los autos y sentencias que dicta el juez en el proceso civil (despacho de ejecución, medidas cautelares, competencia, homologación de acuerdos…) y de las actas, oficios, mandamientos, edictos y cédulas del tribunal. Los decretos, providencias y diligencias tienen sus propios plugins.

## Cómo se usa

Cuéntale a Claude qué documento necesitas y para qué caso. Esta skill busca en la lista de abajo el formulario que mejor encaja (por tipo de documento y por su nombre) y lo abre. Si hay dos o tres que encajan, te los propone para que elijas.

Ejemplos de petición:

- «Auto que despacha ejecución por título judicial»
- «Auto que acuerda una medida cautelar»
- «Acta de la vista del juicio verbal»

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

### Cómo elegir

Busca por tipo de documento y por nombre. Cada formulario es una skill de este plugin (`/formularios-resoluciones-judiciales-civiles:<skill>`). Si dudas entre dos, elige el que mejor encaje con los hechos y dilo; si la petición es ambigua, propón al usuario los dos o tres formularios que mejor encajan y pregúntale cuál quiere. Las reglas del tema están en `marco.md`.

### Cómo usar el formulario elegido

Invoca su skill. Si esa skill no aparece en tu lista de skills disponibles (puede pasar cuando hay muchas skills instaladas), lee directamente su fichero `SKILL.md`: está en la carpeta hermana de esta (`../<skill>/SKILL.md`). Síguelo igual que si la hubieras invocado: el formulario que se rellena está en `../<skill>/assets/formulario.md` y la guía del tema es el `marco.md` de esta carpeta.

### Resoluciones judiciales (autos, decretos, providencias, diligencias) (179)

| Código | Formulario | Skill |
|---|---|---|
| CIV-1797 | Auto que acuerda una medida cautelar sin oír antes al demandado | `auto-acuerda-medida-cautelar-sin-oir-antes-demandado-civ-1797` |
| CIV-1799 | Auto que suspende la ejecución por oposición basada solo en motivos de fondo | `auto-suspende-ejecucion-oposicion-basada-solo-motivos-civ-1799` |
| CIV-1800 | Auto que acuerda suspender la ejecución por admitirse la revisión o rescisión de una sentencia firme | `auto-acuerda-suspender-ejecucion-admitirse-revision-civ-1800` |
| CIV-1802 | Auto de medidas inmediatas sobre custodia de los hijos y uso de la vivienda familiar | `auto-medidas-inmediatas-sobre-custodia-hijos-uso-civ-1802` |
| CIV-1803 | Auto que admite a trámite la solicitud de divorcio de mutuo acuerdo | `auto-admite-tramite-solicitud-divorcio-mutuo-acuerdo-civ-1803` |
| CIV-1807 | Auto que admite la demanda contenciosa de separación con medidas provisionales simultáneas | `auto-admite-demanda-contenciosa-separacion-medidas-civ-1807` |
| CIV-1808 | Auto que admite demanda de separación contenciosa con medidas provisionales previas de otro órgano | `auto-admite-demanda-separacion-contenciosa-medidas-civ-1808` |
| CIV-1809 | Auto que admite a trámite la petición de designación judicial de un árbitro único | `auto-admite-tramite-peticion-designacion-judicial-civ-1809` |
| CIV-1810 | Auto que admite a trámite la demanda de determinación de la filiación de un menor | `auto-admite-tramite-demanda-determinacion-filiacion-civ-1810` |
| CIV-1813 | Auto que desestima la excepción de inmunidad de jurisdicción alegada por una parte | `auto-desestima-excepcion-inmunidad-jurisdiccion-civ-1813` |
| CIV-1843 | Auto de inhibición del juez civil a favor del Juzgado de Violencia sobre la Mujer | `auto-inhibicion-juez-civil-favor-juzgado-violencia-civ-1843` |
| CIV-1844 | Auto de la Sección de Violencia sobre la Mujer que requiere de inhibición a la Sección de Familia | `auto-seccion-violencia-sobre-mujer-requiere-inhibicion-civ-1844` |
| CIV-1846 | Auto de requerimiento de inhibición de Violencia sobre la Mujer a Familia tras denuncia del Fiscal | `auto-requerimiento-inhibicion-violencia-sobre-mujer-civ-1846` |
| CIV-1848 | Sentencia de separación contenciosa con reconvención, medidas previas de otro tribunal y Fiscal | `sentencia-separacion-contenciosa-reconvencion-medidas-civ-1848` |
| CIV-1850 | Auto que acuerda cambiar el procedimiento contencioso por uno de mutuo acuerdo | `auto-acuerda-cambiar-procedimiento-contencioso-uno-civ-1850` |
| CIV-1852 | Auto que declara caducadas las medidas provisionales previas a la demanda | `auto-declara-caducadas-medidas-provisionales-previas-civ-1852` |
| CIV-1861 | Sentencia que estima el divorcio de mutuo acuerdo | `sentencia-estima-divorcio-mutuo-acuerdo-civ-1861` |
| CIV-1865 | Auto que despacha ejecución para entregar cosas genéricas o indeterminadas | `auto-despacha-ejecucion-entregar-cosas-genericas-civ-1865` |
| CIV-1869 | Auto en ejecutoria penal que fija lo debido por pensiones impagadas fijadas en proceso civil | `auto-ejecutoria-penal-fija-lo-debido-pensiones-civ-1869` |
| CIV-1871 | Auto que despacha ejecución de las medidas de separación matrimonial | `auto-despacha-ejecucion-medidas-separacion-matrimonial-civ-1871` |
| CIV-1873 | Auto que estima la eficacia civil de sentencia canónica de nulidad matrimonial | `auto-estima-eficacia-civil-sentencia-canonica-nulidad-civ-1873` |
| CIV-1878 | Auto que suspende la ejecución del laudo arbitral previa prestación de caución | `auto-suspende-ejecucion-laudo-arbitral-previa-civ-1878` |
| CIV-1880 | Auto que designa árbitros conforme a los criterios legales | `auto-designa-arbitros-conforme-criterios-legales-civ-1880` |
| CIV-1881 | Auto que despacha ejecución de laudo arbitral y decreta el embargo de bienes | `auto-despacha-ejecucion-laudo-arbitral-decreta-embargo-civ-1881` |
| CIV-1882 | Auto de medidas provisionales previas a la separación sin hijos y sin acuerdo entre las partes | `auto-medidas-provisionales-previas-separacion-sin-civ-1882` |
| CIV-1883 | Auto que aprueba el nuevo convenio regulador de divorcio con la estipulación modificada | `auto-aprueba-nuevo-convenio-regulador-divorcio-civ-1883` |
| CIV-1886 | Sentencia de divorcio de mutuo acuerdo tras transformar el contencioso, sin aprobar una cláusula | `sentencia-divorcio-mutuo-acuerdo-tras-transformar-civ-1886` |
| CIV-1887 | Sentencia que estima la separación de mutuo acuerdo y aprueba el convenio regulador | `sentencia-estima-separacion-mutuo-acuerdo-aprueba-civ-1887` |
| CIV-1893 | Oficio que recaba informe sobre las cláusulas del convenio regulador relativas a los hijos menores | `oficio-recaba-informe-sobre-clausulas-convenio-civ-1893` |
| CIV-1896 | Auto de archivo por acumulación objetiva de acciones indebida no subsanada | `auto-archivo-acumulacion-objetiva-acciones-indebida-no-civ-1896` |
| CIV-1900 | Auto de sobreseimiento del proceso por repudiación de la herencia por los sucesores del demandado | `auto-sobreseimiento-proceso-repudiacion-herencia-civ-1900` |
| CIV-1902 | Auto que rectifica un error material en el fallo de la sentencia | `auto-rectifica-error-material-fallo-sentencia-civ-1902` |
| CIV-1904 | Oficio que remite por duplicado comisión rogatoria para emplazar a demandado en el extranjero | `oficio-remite-duplicado-comision-rogatoria-emplazar-civ-1904` |
| CIV-1905 | Auto que declara reservadas las actuaciones | `auto-declara-reservadas-actuaciones-civ-1905` |
| CIV-1906 | Auto que aparta definitivamente al juez del asunto por interés indirecto | `auto-aparta-definitivamente-juez-asunto-interes-civ-1906` |
| CIV-1907 | Auto del juez civil que se abstiene por enemistad manifiesta | `auto-juez-civil-abstiene-enemistad-manifiesta-civ-1907` |
| CIV-1912 | Auto que acuerda la sucesión procesal por subrogación o cesión del crédito ejecutivo | `auto-acuerda-sucesion-procesal-subrogacion-cesion-civ-1912` |
| CIV-1918 | Auto que continúa el proceso pese a la incomparecencia de los sucesores | `auto-continua-proceso-pese-incomparecencia-sucesores-civ-1918` |
| CIV-1919 | Sentencia que tiene por renunciada la acción por incomparecencia de los sucesores del actor | `sentencia-tiene-renunciada-accion-incomparecencia-civ-1919` |
| CIV-1924 | Auto que declara improcedente la pretensión acumulada y sigue el proceso respecto de la otra | `auto-declara-improcedente-pretension-acumulada-sigue-civ-1924` |
| CIV-1931 | Auto de sobreseimiento y archivo tras requerir a la parte para que nombre nuevo procurador | `auto-sobreseimiento-archivo-tras-requerir-parte-nombre-civ-1931` |
| CIV-1934 | Auto que acuerda celebrar la vista a puerta cerrada | `auto-acuerda-celebrar-vista-puerta-cerrada-civ-1934` |
| CIV-1937 | Cédula de citación a las partes para la vista del juicio verbal | `cedula-citacion-partes-vista-juicio-verbal-civ-1937` |
| CIV-1946 | Auto que inadmite la impugnación de la tasación de costas | `auto-inadmite-impugnacion-tasacion-costas-civ-1946` |
| CIV-1949 | Auto que suspende el juicio cambiario por prejudicialidad penal | `auto-suspende-juicio-cambiario-prejudicialidad-penal-civ-1949` |
| CIV-1963 | Auto que resuelve sobre la liquidación de daños y perjuicios | `auto-resuelve-sobre-liquidacion-danos-perjuicios-civ-1963` |
| CIV-1966 | Auto que deniega despachar ejecución de un hacer no personalísimo | `auto-deniega-despachar-ejecucion-hacer-no-personalisimo-civ-1966` |
| CIV-1967 | Auto que deniega despachar ejecución para la entrega de bienes inmuebles | `auto-deniega-despachar-ejecucion-entrega-bienes-civ-1967` |
| CIV-1968 | Auto que deniega despachar ejecución para la entrega de cosa mueble cierta y determinada | `auto-deniega-despachar-ejecucion-entrega-cosa-mueble-civ-1968` |
| CIV-1969 | Auto que declara personalísimo el hacer y sigue la ejecución por su equivalente con multa única | `auto-declara-personalisimo-hacer-sigue-ejecucion-civ-1969` |
| CIV-1970 | Auto que deniega despachar ejecución de una condena de no hacer | `auto-deniega-despachar-ejecucion-condena-no-hacer-civ-1970` |
| CIV-1971 | Auto que declara no personalísimo el hacer de la sentencia | `auto-declara-no-personalisimo-hacer-sentencia-civ-1971` |
| CIV-1972 | Auto que apremia con multas al ejecutado tras declarar personalísimo el hacer | `auto-apremia-multas-ejecutado-tras-declarar-civ-1972` |
| CIV-1974 | Auto que deniega despachar ejecución de un hacer personalísimo | `auto-deniega-despachar-ejecucion-hacer-personalisimo-civ-1974` |
| CIV-1975 | Auto que tiene por emitida la declaración de voluntad y fija los elementos no esenciales del negocio | `auto-tiene-emitida-declaracion-voluntad-fija-elementos-civ-1975` |
| CIV-1977 | Auto que tiene por emitida la declaración de voluntad a la que fue condenado el ejecutado | `auto-tiene-emitida-declaracion-voluntad-fue-condenado-civ-1977` |
| CIV-1980 | Auto que manda seguir la ejecución por allanamiento del ejecutante a la tercería de mejor derecho | `auto-manda-seguir-ejecucion-allanamiento-ejecutante-civ-1980` |
| CIV-1981 | Sentencia que desestima la tercería de mejor derecho | `sentencia-desestima-terceria-mejor-derecho-civ-1981` |
| CIV-1982 | Auto que declara que el ocupante no tiene derecho a permanecer en el inmueble enajenado | `auto-declara-ocupante-no-tiene-derecho-permanecer-civ-1982` |
| CIV-1999 | Sentencia que estima la tercería de mejor derecho | `sentencia-estima-terceria-mejor-derecho-civ-1999` |
| CIV-2002 | Auto que tiene por allanado al ejecutante en la tercería y la sigue contra el ejecutado | `auto-tiene-allanado-ejecutante-terceria-sigue-contra-civ-2002` |
| CIV-2011 | Auto que inadmite la demanda de tercería de dominio | `auto-inadmite-demanda-terceria-dominio-civ-2011` |
| CIV-2012 | Auto que estima la tercería de dominio | `auto-estima-terceria-dominio-civ-2012` |
| CIV-2014 | Auto que inadmite la demanda de tercería de mejor derecho | `auto-inadmite-demanda-terceria-mejor-derecho-civ-2014` |
| CIV-2015 | Auto que desestima la tercería de dominio | `auto-desestima-terceria-dominio-civ-2015` |
| CIV-2020 | Auto que rechaza la oposición de un tercero al embargo y decreta la traba | `auto-rechaza-oposicion-tercero-embargo-decreta-traba-civ-2020` |
| CIV-2021 | Auto que deniega el embargo de bienes por pertenecer a un tercero | `auto-deniega-embargo-bienes-pertenecer-tercero-civ-2021` |
| CIV-2023 | Auto que admite el allanamiento del ejecutante si el crédito del tercerista no consta en título | `auto-admite-allanamiento-ejecutante-si-credito-civ-2023` |
| CIV-2024 | Auto que deniega abonar el valor de las cosas no separables | `auto-deniega-abonar-valor-cosas-no-separables-civ-2024` |
| CIV-2027 | Auto que despacha ejecución para la entrega de bienes inmuebles | `auto-despacha-ejecucion-entrega-bienes-inmuebles-civ-2027` |
| CIV-2037 | Auto que autoriza la entrada en lugar cerrado para entregar la cosa al ejecutante | `auto-autoriza-entrada-lugar-cerrado-entregar-cosa-civ-2037` |
| CIV-2039 | Auto que deniega despachar ejecución para la entrega de cosas genéricas o indeterminadas | `auto-deniega-despachar-ejecucion-entrega-cosas-civ-2039` |
| CIV-2048 | Auto que desestima la oposición a la ejecución por motivos de fondo | `auto-desestima-oposicion-ejecucion-motivos-fondo-civ-2048` |
| CIV-2050 | Auto que estima la oposición a la ejecución por motivos de fondo | `auto-estima-oposicion-ejecucion-motivos-fondo-civ-2050` |
| CIV-2051 | Auto que alza la suspensión de la ejecución tras desestimarse la revisión o rescisión de sentencia | `auto-alza-suspension-ejecucion-tras-desestimarse-civ-2051` |
| CIV-2059 | Mandamiento al Registro de la Propiedad para que expida certificación de cargas | `mandamiento-registro-propiedad-expida-certificacion-civ-2059` |
| CIV-2085 | Auto que despacha provisionalmente la vía de apremio solicitada por el ejecutante | `auto-despacha-provisionalmente-via-apremio-solicitada-civ-2085` |
| CIV-2086 | Auto de sobreseimiento de la ejecución provisional cuando es imposible devolver el bien | `auto-sobreseimiento-ejecucion-provisional-cuando-es-civ-2086` |
| CIV-2087 | Auto que despacha ejecución fundada en auto de cuantía máxima del seguro obligatorio de automóviles | `auto-despacha-ejecucion-fundada-auto-cuantia-maxima-civ-2087` |
| CIV-2088 | Auto que estima la oposición por defectos procesales insubsanables | `auto-estima-oposicion-defectos-procesales-insubsanables-civ-2088` |
| CIV-2089 | Auto que deniega despachar ejecución de póliza de contrato mercantil por falta de firma del corredor | `auto-deniega-despachar-ejecucion-poliza-contrato-civ-2089` |
| CIV-2090 | Auto que deniega despachar ejecución de una sentencia de condena que no es firme | `auto-deniega-despachar-ejecucion-sentencia-condena-no-civ-2090` |
| CIV-2091 | Auto que despacha ejecución fundada en póliza de contrato mercantil | `auto-despacha-ejecucion-fundada-poliza-contrato-civ-2091` |
| CIV-2092 | Auto que despacha ejecución de sentencia firme de condena al pago de cantidad | `auto-despacha-ejecucion-sentencia-firme-condena-pago-civ-2092` |
| CIV-2094 | Auto que rechaza la medida cautelar anterior al juicio por no concurrir urgencia ni necesidad | `auto-rechaza-medida-cautelar-anterior-juicio-no-civ-2094` |
| CIV-2097 | Auto que adopta medida cautelar sustitutoria pese a sentencia íntegramente desestimatoria apelada | `auto-adopta-medida-cautelar-sustitutoria-pese-civ-2097` |
| CIV-2099 | Auto que resuelve la oposición a una medida cautelar acordada sin audiencia previa | `auto-resuelve-oposicion-medida-cautelar-acordada-sin-civ-2099` |
| CIV-2102 | Auto que adopta una medida cautelar solicitada junto con la demanda | `auto-adopta-medida-cautelar-solicitada-junto-demanda-civ-2102` |
| CIV-2104 | Auto que despacha ejecución en un juicio cambiario | `auto-despacha-ejecucion-juicio-cambiario-civ-2104` |
| CIV-2105 | Auto que da por terminado el juicio cambiario y despacha ejecución con embargo ya practicado | `auto-da-terminado-juicio-cambiario-despacha-ejecucion-civ-2105` |
| CIV-2106 | Auto de desistimiento en proceso monitorio con oposición del demandado | `auto-desistimiento-proceso-monitorio-oposicion-civ-2106` |
| CIV-2107 | Auto de allanamiento parcial y ejecución por lo reconocido en monitorio de más de 2.000 euros | `auto-allanamiento-parcial-ejecucion-lo-reconocido-civ-2107` |
| CIV-2109 | Auto que despacha ejecución en monitorio de más de 2.000 euros por incomparecencia del deudor | `auto-despacha-ejecucion-monitorio-mas-2-000-euros-civ-2109` |
| CIV-2110 | Auto de ejecución con embargo de bienes concretos en monitorio de más de 2.000 euros | `auto-ejecucion-embargo-bienes-concretos-monitorio-mas-civ-2110` |
| CIV-2111 | Auto que deniega el monitorio de una comunidad contra varios deudores por acumulación indebida | `auto-deniega-monitorio-comunidad-contra-varios-civ-2111` |
| CIV-2112 | Auto que despacha ejecución provisional con bienes para la traba designados por el ejecutante | `auto-despacha-ejecucion-provisional-bienes-traba-civ-2112` |
| CIV-2113 | Auto que deniega la ejecución provisional por no ser la sentencia provisionalmente ejecutable | `auto-deniega-ejecucion-provisional-no-ser-sentencia-civ-2113` |
| CIV-2114 | Auto que despacha ejecución provisional sin que el ejecutante haya designado bienes para la traba | `auto-despacha-ejecucion-provisional-sin-ejecutante-civ-2114` |
| CIV-2115 | Auto que desestima la oposición a la ejecución provisional por infracción de requisitos procesales | `auto-desestima-oposicion-ejecucion-provisional-civ-2115` |
| CIV-2116 | Auto que estima la oposición a la ejecución provisional si fuera muy difícil restaurar la situación | `auto-estima-oposicion-ejecucion-provisional-si-fuera-civ-2116` |
| CIV-2117 | Auto que desestima la oposición a la ejecución provisional basada en la imposible restauración | `auto-desestima-oposicion-ejecucion-provisional-basada-civ-2117` |
| CIV-2118 | Auto que rechaza plantear la cuestión incidental | `auto-rechaza-plantear-cuestion-incidental-civ-2118` |
| CIV-2119 | Auto que acuerda una diligencia final extraordinaria de ampliación del dictamen pericial económico | `auto-acuerda-diligencia-final-extraordinaria-civ-2119` |
| CIV-2124 | Auto que ratifica el embargo de gananciales por deuda no privativa derivada de accidente de tráfico | `auto-ratifica-embargo-gananciales-deuda-no-privativa-civ-2124` |
| CIV-2127 | Auto que declara privativa la deuda y da al cónyuge no deudor la opción de disolver los gananciales | `auto-declara-privativa-deuda-da-conyuge-no-deudor-civ-2127` |
| CIV-2139 | Auto que concede alimentos provisionales como medida cautelar en un proceso de filiación | `auto-concede-alimentos-provisionales-como-medida-civ-2139` |
| CIV-2145 | Auto que acuerda de oficio intervenir el caudal hereditario | `auto-acuerda-oficio-intervenir-caudal-hereditario-civ-2145` |
| CIV-2147 | Auto que resuelve sobre la administración, custodia y conservación del caudal hereditario | `auto-resuelve-sobre-administracion-custodia-civ-2147` |
| CIV-2148 | Auto que admite el juicio de división de herencia y la intervención del caudal hereditario | `auto-admite-juicio-division-herencia-intervencion-civ-2148` |
| CIV-2152 | Auto que acepta el requerimiento de otro tribunal para acumular los autos | `auto-acepta-requerimiento-otro-tribunal-acumular-autos-civ-2152` |
| CIV-2154 | Auto que declara procedente acumular autos de otro tribunal tras la impugnación de la contraparte | `auto-declara-procedente-acumular-autos-otro-tribunal-civ-2154` |
| CIV-2155 | Auto del tribunal requerido que deniega la acumulación y remite los autos al tribunal superior | `auto-tribunal-requerido-deniega-acumulacion-remite-civ-2155` |
| CIV-2156 | Auto que deniega inicialmente la acumulación de autos de otro tribunal (art. 78 LEC) | `auto-deniega-inicialmente-acumulacion-autos-otro-civ-2156` |
| CIV-2157 | Auto que acumula el juicio de divorcio al de modificación de medidas de separación | `auto-acumula-juicio-divorcio-modificacion-medidas-civ-2157` |
| CIV-2161 | Auto que deniega suspender el procedimiento por prejudicialidad civil | `auto-deniega-suspender-procedimiento-prejudicialidad-civ-2161` |
| CIV-2165 | Auto que deniega el requerimiento por edictos en monitorios ajenos a cuotas de propiedad horizontal | `auto-deniega-requerimiento-edictos-monitorios-ajenos-civ-2165` |
| CIV-2169 | Auto que despacha ejecución en monitorio de menos de 2.000 euros por incomparecencia del deudor | `auto-despacha-ejecucion-monitorio-menos-2-000-euros-civ-2169` |
| CIV-2170 | Auto que sobresee la ejecución provisional de condena dineraria por revocación total de la sentencia | `auto-sobresee-ejecucion-provisional-condena-dineraria-civ-2170` |
| CIV-2171 | Auto de sobreseimiento de ejecución provisional tras revocación total de condena de hacer | `auto-sobreseimiento-ejecucion-provisional-tras-civ-2171` |
| CIV-2172 | Auto que acuerda continuar la ejecución provisional | `auto-acuerda-continuar-ejecucion-provisional-civ-2172` |
| CIV-2173 | Auto que sobresee la ejecución provisional al revocarse la entrega de un bien determinado | `auto-sobresee-ejecucion-provisional-revocarse-entrega-civ-2173` |
| CIV-2175 | Auto que ordena devolver parte de lo cobrado cuando la condena dineraria se revoca en parte | `auto-ordena-devolver-parte-lo-cobrado-cuando-condena-civ-2175` |
| CIV-2177 | Auto que estima la oposición por defectos procesales no subsanados por el ejecutante | `auto-estima-oposicion-defectos-procesales-no-civ-2177` |
| CIV-2184 | Auto que archiva la ejecución provisional al poner el ejecutado la suma a disposición del tribunal | `auto-archiva-ejecucion-provisional-poner-ejecutado-civ-2184` |
| CIV-2185 | Auto que estima la oposición a una actuación concreta de la ejecución provisional dineraria | `auto-estima-oposicion-actuacion-concreta-ejecucion-civ-2185` |
| CIV-2186 | Auto que suspende la ejecución provisional por consignación de la condena | `auto-suspende-ejecucion-provisional-consignacion-civ-2186` |
| CIV-2187 | Auto que estima la oposición a la ejecución provisional por infracción de requisitos procesales | `auto-estima-oposicion-ejecucion-provisional-infraccion-civ-2187` |
| CIV-2189 | Auto que desestima la oposición a una actuación concreta de la ejecución provisional dineraria | `auto-desestima-oposicion-actuacion-concreta-ejecucion-civ-2189` |
| CIV-2191 | Auto que desestima la oposición por defectos procesales y sigue por motivos de fondo | `auto-desestima-oposicion-defectos-procesales-sigue-civ-2191` |
| CIV-2193 | Auto que desestima la oposición fundada solo en defectos procesales | `auto-desestima-oposicion-fundada-solo-defectos-civ-2193` |
| CIV-2894 | Edicto que anuncia la subasta de los bienes inmuebles del ejecutado | `edicto-anuncia-subasta-bienes-inmuebles-ejecutado-civ-2894` |
| CIV-2895 | Edicto abreviado para el BOE que publica la subasta de bienes muebles embargados | `edicto-abreviado-boe-publica-subasta-bienes-muebles-civ-2895` |
| CIV-2897 | Oficio a los acreedores preferentes anteriores para que informen si su crédito subsiste | `oficio-acreedores-preferentes-anteriores-informen-si-civ-2897` |
| CIV-2898 | Mandamiento al Registro de la Propiedad para anotar preventivamente el embargo de inmuebles | `mandamiento-registro-propiedad-anotar-preventivamente-civ-2898` |
| CIV-2899 | Auto que reconoce a los ocupantes el derecho a seguir en el inmueble embargado tras su venta | `auto-reconoce-ocupantes-derecho-seguir-inmueble-civ-2899` |
| CIV-2903 | Auto del tribunal superior que resuelve la discrepancia y deniega la acumulación de procesos | `auto-tribunal-superior-resuelve-discrepancia-deniega-civ-2903` |
| CIV-2904 | Auto que deniega lanzar al ocupante con título suficiente del inmueble ejecutado | `auto-deniega-lanzar-ocupante-titulo-suficiente-civ-2904` |
| CIV-2905 | Auto que ordena el lanzamiento de los ocupantes del inmueble subastado | `auto-ordena-lanzamiento-ocupantes-inmueble-subastado-civ-2905` |
| CIV-2906 | Auto que despacha ejecución de una obligación de hacer no personalísimo | `auto-despacha-ejecucion-obligacion-hacer-no-civ-2906` |
| CIV-2907 | Auto que despacha ejecución para que se publique o difunda la sentencia | `auto-despacha-ejecucion-publique-difunda-sentencia-civ-2907` |
| CIV-2908 | Auto que despacha ejecución de una obligación de hacer personalísimo | `auto-despacha-ejecucion-obligacion-hacer-personalisimo-civ-2908` |
| CIV-2909 | Auto que despacha ejecución de una condena de no hacer | `auto-despacha-ejecucion-condena-no-hacer-civ-2909` |
| CIV-2910 | Auto que despacha ejecución para la entrega de una cosa mueble determinada | `auto-despacha-ejecucion-entrega-cosa-mueble-determinada-civ-2910` |
| CIV-2913 | Auto que estima la declinatoria y declara la falta de competencia territorial | `auto-estima-declinatoria-declara-falta-competencia-civ-2913` |
| CIV-2921 | Oficio al pagador del ejecutado para que retenga parte del sueldo y lo consigne en el tribunal | `oficio-pagador-ejecutado-retenga-parte-sueldo-lo-civ-2921` |
| CIV-2922 | Oficio al Registro Civil para anotar al margen el fallo de la sentencia matrimonial firme | `oficio-registro-civil-anotar-margen-fallo-sentencia-civ-2922` |
| CIV-2925 | Auto que admite la demanda y une las medidas provisionales previas tramitadas en otro tribunal | `auto-admite-demanda-une-medidas-provisionales-previas-civ-2925` |
| CIV-2927 | Mandamiento al Registro de la Propiedad para inscribir la atribución judicial del uso de la vivienda | `mandamiento-registro-propiedad-inscribir-atribucion-civ-2927` |
| CIV-2928 | Auto que admite a trámite la demanda de alimentos en juicio verbal | `auto-admite-tramite-demanda-alimentos-juicio-verbal-civ-2928` |
| CIV-2931 | Auto que estima la falta de litisconsorcio en el verbal de alimentos y ordena subsanar | `auto-estima-falta-litisconsorcio-verbal-alimentos-civ-2931` |
| CIV-2932 | Cédula de citación al demandado para la vista del juicio verbal de alimentos | `cedula-citacion-demandado-vista-juicio-verbal-alimentos-civ-2932` |
| CIV-2933 | Auto que rechaza la falta de litisconsorcio en el verbal de alimentos y convoca a la vista | `auto-rechaza-falta-litisconsorcio-verbal-alimentos-civ-2933` |
| CIV-2937 | Auto que admite la demanda de eficacia civil de una sentencia eclesiástica de nulidad | `auto-admite-demanda-eficacia-civil-sentencia-civ-2937` |
| CIV-2947 | Auto que adopta medidas provisionalísimas antes de la demanda de nulidad, separación o divorcio | `auto-adopta-medidas-provisionalisimas-antes-demanda-civ-2947` |
| CIV-2952 | Auto que rechaza las medidas del nuevo convenio propuesto y decide lo procedente | `auto-rechaza-medidas-nuevo-convenio-propuesto-decide-civ-2952` |
| CIV-2956 | Auto que adopta medidas provisionales previas a la demanda matrimonial con hijos menores | `auto-adopta-medidas-provisionales-previas-demanda-civ-2956` |
| CIV-2959 | Auto que despacha ejecución provisional de medidas patrimoniales antes de remitir la apelación | `auto-despacha-ejecucion-provisional-medidas-civ-2959` |
| CIV-2963 | Auto que inadmite la reconvención y cita a las partes a la vista con los apercibimientos legales | `auto-inadmite-reconvencion-cita-partes-vista-civ-2963` |
| CIV-2964 | Auto que admite la reconvención y da diez días para contestarla | `auto-admite-reconvencion-da-diez-dias-contestarla-civ-2964` |
| CIV-2966 | Auto que da por subsanado el defecto procesal previo y admite a trámite la demanda matrimonial | `auto-da-subsanado-defecto-procesal-previo-admite-civ-2966` |
| CIV-2967 | Auto que admite la demanda matrimonial y emplaza al demandado y al Ministerio Fiscal | `auto-admite-demanda-matrimonial-emplaza-demandado-civ-2967` |
| CIV-2971 | Auto que declara la falta de competencia territorial tras la demanda por existir fueros electivos | `auto-declara-falta-competencia-territorial-tras-civ-2971` |
| CIV-2973 | Auto que declara la falta de competencia territorial una vez presentada la demanda matrimonial | `auto-declara-falta-competencia-territorial-vez-civ-2973` |
| CIV-2979 | Auto que desestima la reposición contra la admisión de la reconvención en proceso matrimonial | `auto-desestima-reposicion-contra-admision-reconvencion-civ-2979` |
| CIV-2995 | Auto que estima la reposición contra la inadmisión de la reconvención en proceso matrimonial | `auto-estima-reposicion-contra-inadmision-reconvencion-civ-2995` |
| CIV-2996 | Auto que deniega medidas provisionalísimas previas a la demanda de nulidad, separación o divorcio | `auto-deniega-medidas-provisionalisimas-previas-demanda-civ-2996` |
| CIV-3008 | Auto que adopta medidas provisionales previas a la demanda de nulidad, separación o divorcio | `auto-adopta-medidas-provisionales-previas-demanda-civ-3008` |
| CIV-3009 | Auto que adopta medidas provisionales sobre los hijos menores pedidas en la demanda matrimonial | `auto-adopta-medidas-provisionales-sobre-hijos-menores-civ-3009` |
| CIV-3011 | Auto que aprueba las medidas del nuevo convenio en la separación o divorcio de mutuo acuerdo | `auto-aprueba-medidas-nuevo-convenio-separacion-civ-3011` |
| CIV-3012 | Auto que acuerda seguir por mutuo acuerdo el proceso contencioso de separación o divorcio | `auto-acuerda-seguir-mutuo-acuerdo-proceso-contencioso-civ-3012` |
| CIV-3013 | Cédula que cita al demandado a la comparecencia de medidas provisionales previas a la demanda | `cedula-cita-demandado-comparecencia-medidas-civ-3013` |
| CIV-3015 | Auto que reconoce eficacia civil a la nulidad canónica por ajustarse al Derecho del Estado | `auto-reconoce-eficacia-civil-nulidad-canonica-civ-3015` |
| CIV-3016 | Auto que niega eficacia civil a la nulidad canónica por no ajustarse al Derecho del Estado | `auto-niega-eficacia-civil-nulidad-canonica-no-civ-3016` |
| CIV-3017 | Oficio al Registro Civil para anotar el auto que da eficacia civil a la nulidad canónica | `oficio-registro-civil-anotar-auto-da-eficacia-civil-civ-3017` |
| CIV-3027 | Auto que despacha ejecución contra la aseguradora en el juicio ejecutivo del automóvil | `auto-despacha-ejecucion-contra-aseguradora-juicio-civ-3027` |
| CIV-3028 | Auto que acuerda la diligencia preliminar contra el otro implicado en el accidente y su aseguradora | `auto-acuerda-diligencia-preliminar-contra-otro-civ-3028` |
| CIV-3031 | Auto que declara de oficio la falta de jurisdicción por inmunidad de jurisdicción | `auto-declara-oficio-falta-jurisdiccion-inmunidad-civ-3031` |
| CIV-3032 | Auto que estima la declinatoria y declara la falta de jurisdicción por inmunidad de jurisdicción | `auto-estima-declinatoria-declara-falta-jurisdiccion-civ-3032` |
| CIV-3033 | Auto que descarta la inmunidad de jurisdicción examinada de oficio | `auto-descarta-inmunidad-jurisdiccion-examinada-oficio-civ-3033` |

### Estatutos, actas, certificaciones y escrituras (52)

| Código | Formulario | Skill |
|---|---|---|
| CIV-1888 | Acta de la vista principal en juicio de separación matrimonial | `acta-vista-principal-juicio-separacion-matrimonial-civ-1888` |
| CIV-1890 | Acta de audiencia del menor sobre el régimen de visitas | `acta-audiencia-menor-sobre-regimen-visitas-civ-1890` |
| CIV-1894 | Acta de ratificación de la petición de divorcio y del convenio regulador | `acta-ratificacion-peticion-divorcio-convenio-regulador-civ-1894` |
| CIV-1933 | Acta de la vista de apelación con recusación oral de un magistrado | `acta-vista-apelacion-recusacion-oral-magistrado-civ-1933` |
| CIV-2151 | Acta de la vista sobre medidas de protección y alimentos provisionales en reclamación de filiación | `acta-vista-sobre-medidas-proteccion-alimentos-civ-2151` |
| CIV-2896 | Acta de aceptación del cargo por el perito tasador designado en la ejecución | `acta-aceptacion-cargo-perito-tasador-designado-civ-2896` |
| CIV-2914 | Acta de la junta de interesados en la herencia para nombrar contador y peritos | `acta-junta-interesados-herencia-nombrar-contador-civ-2914` |
| CIV-2918 | Acta de la audiencia a los abuelos sobre el régimen de visitas propuesto por los padres | `acta-audiencia-abuelos-sobre-regimen-visitas-propuesto-civ-2918` |
| CIV-2919 | Acta de la vista sobre los bienes del inventario y la fecha de disolución de los gananciales | `acta-vista-sobre-bienes-inventario-fecha-disolucion-civ-2919` |
| CIV-2920 | Acta de la vista sobre la exclusión del inventario de regalos de boda no gananciales | `acta-vista-sobre-exclusion-inventario-regalos-boda-no-civ-2920` |
| CIV-2926 | Acta de la vista para liquidar la sociedad de gananciales | `acta-vista-liquidar-sociedad-gananciales-civ-2926` |
| CIV-2929 | Acta de vista del verbal de alimentos con oposición del demandado y práctica de prueba | `acta-vista-verbal-alimentos-oposicion-demandado-civ-2929` |
| CIV-2930 | Acta de vista del verbal de alimentos con el demandado incomparecido declarado en rebeldía | `acta-vista-verbal-alimentos-demandado-incomparecido-civ-2930` |
| CIV-2934 | Acta de vista del verbal de alimentos con conformidad del demandado sobre los hechos | `acta-vista-verbal-alimentos-conformidad-demandado-civ-2934` |
| CIV-2935 | Acta del juicio de filiación celebrado sin asistencia del Fiscal citado | `acta-juicio-filiacion-celebrado-sin-asistencia-fiscal-civ-2935` |
| CIV-2936 | Acta de vista del verbal de alimentos reclamados por un hijo mayor de edad | `acta-vista-verbal-alimentos-reclamados-hijo-mayor-edad-civ-2936` |
| CIV-2938 | Acta de la vista matrimonial con incomparecencia del demandado | `acta-vista-matrimonial-incomparecencia-demandado-civ-2938` |
| CIV-2939 | Acta de vista que tiene por desistido al actor incomparecido, con petición de indemnización | `acta-vista-tiene-desistido-actor-incomparecido-civ-2939` |
| CIV-2940 | Acta de vista que tiene por desistido al actor incomparecido sin interés del demandado en seguir | `acta-vista-tiene-desistido-actor-incomparecido-sin-civ-2940` |
| CIV-2941 | Acta de vista con desistimiento por incomparecencia de ambas partes | `acta-vista-desistimiento-incomparecencia-ambas-partes-civ-2941` |
| CIV-2957 | Acta de la vista sobre medidas cautelares en un proceso de filiación | `acta-vista-sobre-medidas-cautelares-proceso-filiacion-civ-2957` |
| CIV-2981 | Acta de la vista sobre la inclusión de bienes en el inventario matrimonial | `acta-vista-sobre-inclusion-bienes-inventario-civ-2981` |
| CIV-2986 | Acta de la prueba testifical en la vista del juicio de reclamación de paternidad extramatrimonial | `acta-prueba-testifical-vista-juicio-reclamacion-civ-2986` |
| CIV-2987 | Acta de vista de juicio verbal en la que el demandado niega la existencia de la pareja de hecho | `acta-vista-juicio-verbal-demandado-niega-existencia-civ-2987` |
| CIV-2988 | Acta de la vista en juicio de filiación con alegaciones y práctica de prueba | `acta-vista-juicio-filiacion-alegaciones-practica-prueba-civ-2988` |
| CIV-2989 | Acta de la vista en juicio de filiación con petición de diligencias finales | `acta-vista-juicio-filiacion-peticion-diligencias-civ-2989` |
| CIV-2990 | Acta de vista con la petición del testigo de que se le abonen los gastos de desplazamiento | `acta-vista-peticion-testigo-le-abonen-gastos-civ-2990` |
| CIV-2991 | Acta de la junta de herederos para nombrar contador y peritos sin conformidad en los nombramientos | `acta-junta-herederos-nombrar-contador-peritos-sin-civ-2991` |
| CIV-2992 | Acta de la junta para nombrar varios peritos en la división de herencia sin acuerdo de las partes | `acta-junta-nombrar-varios-peritos-division-herencia-civ-2992` |
| CIV-2993 | Acta de la comparecencia de medidas previas a la separación con acuerdo parcial y prueba | `acta-comparecencia-medidas-previas-separacion-acuerdo-civ-2993` |
| CIV-2994 | Acta de la comparecencia de medidas previas a la separación sin asistencia del demandado | `acta-comparecencia-medidas-previas-separacion-sin-civ-2994` |
| CIV-2997 | Acta de comparecencia para liquidar la participación en ganancias sin acuerdo de los cónyuges | `acta-comparecencia-liquidar-participacion-ganancias-civ-2997` |
| CIV-2998 | Acta para liquidar gananciales sin acuerdo, con contador y perito nombrados por el tribunal | `acta-liquidar-gananciales-sin-acuerdo-contador-perito-civ-2998` |
| CIV-2999 | Acta de comparecencia sobre la oposición a las operaciones divisorias sin acuerdo de las partes | `acta-comparecencia-sobre-oposicion-operaciones-civ-2999` |
| CIV-3000 | Acta de comparecencia sobre la oposición a las operaciones divisorias con acuerdo de las partes | `acta-comparecencia-sobre-oposicion-operaciones-civ-3000` |
| CIV-3001 | Acta de comparecencia para liquidar los gananciales sin asistencia de uno de los cónyuges | `acta-comparecencia-liquidar-gananciales-sin-asistencia-civ-3001` |
| CIV-3002 | Acta de comparecencia para liquidar los gananciales sin acuerdo, con contador y perito pactados | `acta-comparecencia-liquidar-gananciales-sin-acuerdo-civ-3002` |
| CIV-3003 | Acta de comparecencia para liquidar los gananciales con acuerdo de los cónyuges | `acta-comparecencia-liquidar-gananciales-acuerdo-civ-3003` |
| CIV-3004 | Acta de la junta de herederos para nombrar contador y peritos con conformidad en los nombramientos | `acta-junta-herederos-nombrar-contador-peritos-civ-3004` |
| CIV-3006 | Acta de la vista del proceso matrimonial contencioso con admisión y práctica de prueba | `acta-vista-proceso-matrimonial-contencioso-admision-civ-3006` |
| CIV-3007 | Acta de la vista matrimonial con práctica de prueba y nuevo señalamiento por ausencia de un testigo | `acta-vista-matrimonial-practica-prueba-nuevo-civ-3007` |
| CIV-3010 | Acta de comparecencia del cónyuge conforme con la eficacia civil de la nulidad canónica | `acta-comparecencia-conyuge-conforme-eficacia-civil-civ-3010` |
| CIV-3014 | Acta de comparecencia del testigo que no puede acudir a la vista y pide su aplazamiento | `acta-comparecencia-testigo-no-puede-acudir-vista-pide-civ-3014` |
| CIV-3020 | Acta en la que cada cónyuge ratifica por separado la petición de separación o divorcio consensual | `acta-cada-conyuge-ratifica-separado-peticion-civ-3020` |
| CIV-3021 | Acta de la práctica de la prueba testifical acordada de oficio en el proceso matrimonial | `acta-practica-prueba-testifical-acordada-oficio-civ-3021` |
| CIV-3022 | Acta de la audiencia a los hijos menores ante el juez en el proceso matrimonial | `acta-audiencia-hijos-menores-ante-juez-proceso-civ-3022` |
| CIV-3023 | Acta de la comparecencia de medidas previas a la separación en la que las partes llegan a un acuerdo | `acta-comparecencia-medidas-previas-separacion-partes-civ-3023` |
| CIV-3024 | Acta de la vista matrimonial sin el demandante que continúa por interés legítimo del demandado | `acta-vista-matrimonial-sin-demandante-continua-interes-civ-3024` |
| CIV-3025 | Acta de la vista matrimonial que estima la excepción de poder insuficiente alegada por la demandada | `acta-vista-matrimonial-estima-excepcion-poder-civ-3025` |
| CIV-3026 | Acta de la continuación de la vista matrimonial para practicar la prueba pendiente | `acta-continuacion-vista-matrimonial-practicar-prueba-civ-3026` |
| CIV-3029 | Acta de comparecencia en la que se practica la diligencia preliminar acordada | `acta-comparecencia-practica-diligencia-preliminar-civ-3029` |
| CIV-3030 | Acta de audiencia previa que examina la falta de representación del administrador de la herencia | `acta-audiencia-previa-examina-falta-representacion-civ-3030` |

### Escritos de trámite y otros (5)

| Código | Formulario | Skill |
|---|---|---|
| CIV-1798 | Pronunciamientos de la sentencia definitiva sobre las medidas cautelares | `pronunciamientos-sentencia-definitiva-sobre-medidas-civ-1798` |
| CIV-1815 | Resolución que admite la declinatoria por inmunidad de jurisdicción alegada por el demandado | `resolucion-admite-declinatoria-inmunidad-jurisdiccion-civ-1815` |
| CIV-1816 | Resolución que declara la falta de jurisdicción por inmunidad apreciada de oficio | `resolucion-declara-falta-jurisdiccion-inmunidad-civ-1816` |
| CIV-1923 | Acuerda la sucesión procesal por causa de muerte (decreto) | `acuerda-sucesion-procesal-causa-muerte-decreto-civ-1923` |
| CIV-1935 | Escrito del juez de primera instancia que se abstiene por ser cónyuge del procurador de una parte | `escrito-juez-primera-instancia-abstiene-ser-conyuge-civ-1935` |
