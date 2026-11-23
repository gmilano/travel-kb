---
industry: travel
region: Global
updated: 2026-11-23
---

# 📡 Tendencias — Travel & Hospitality

> Estado del vertical al 2026-11-23. Cada tendencia lleva la evidencia que la sostiene y,
> cuando la evidencia es débil, lo dice. Las tendencias 1–10 se establecieron el 2026-11-21;
> las 11–13 se agregaron el 2026-11-23 al abrir el **plano de frontera e identidad**.

## 1. El agente planifica; el humano todavía paga

La cifra que define el año: **52% de los viajeros de EE.UU. usan AI para planificar y 2%
reserva con ella** (Phocuswright 2026; ~8% contando Google AI Mode). Solo **8% confía en que
la AI complete una reserva**. No es un problema de modelo — es de confianza y de quién responde
si la compra sale mal. Las aerolíneas lo institucionalizaron: United apoya AI para investigación
e inspiración y **mantiene intervención humana en la compra**.

Corolario de ingeniería: el human-in-the-loop en el pago no es una concesión de producto, es el
estado del arte. El agente open source más honesto del ecosistema
([`Prism-Shadow/travel-agent`](https://github.com/Prism-Shadow/travel-agent), Apache-2.0)
navega sitios reales y **se detiene en la página de pago**.

## 2. El merchant of record se volvió la decisión de arquitectura

**12-nov-2026: Travelport y Booked AI completaron una compra de vuelo end-to-end conducida por
AI**, vía NDC sobre Travelport TripServices, **con la aerolínea como merchant of record**. Eso
es exactamente lo que Travelport quería demostrar: que se puede vender por agentes sin que la
aerolínea pierda el control del cobro. Google, en la otra punta, declaró que **no tiene
intención de convertirse en OTA** y que **no es merchant of record**.

Quien diseñe asumiendo que el agente cobra está diseñando contra la postura de todos los
proveedores de inventario a la vez.

## 3. MCP se volvió infraestructura, no experimento

Anthropic **donó MCP a la Agentic AI Foundation (Linux Foundation) en dic-2025**. Lo adoptaron
Sabre, Travelport, Amadeus, Booking.com, Expedia y Turkish Airlines. El **MCP server de Sabre
está en piloto o producción en ~80 empresas de travel** (Virgin Australia, Flight Centre,
Internova), y algunas de esas herramientas corren dentro de ChatGPT y Claude *(fuente
secundaria, sept-2026 — vale confirmarlo contra el press release de Sabre)*.

Travelport lo formuló mejor que nadie en jul-2026: el objetivo es **que la reserva sea
determinística** en lugar de que el modelo infiera el inventario.

## 4. IATA no emitió un estándar agentic — y eso importa

NDC (XML, framework EASD: oferta, orden, pago, servicing, cancelación, reembolso) y ONE Order
son la base. **La capa agentic la construyen proveedores: MCP y UCP, sin aval de IATA.**
TPConnects integró MCP en su plataforma NDC Astra; Amadeus integra NDC y ONE Order para
comercio agentic. Son claims de proveedor, no estándares de la industria.

**Corrección a ciclos previos de esta KB:** se registró "NDC 24.2 obligatorio" y repos
"certificados NDC 24.2". **NDC no es obligatorio.** Su adopción es desigual: Lufthansa Group
reporta >50% de ventas de agencia vía NDC, pero solo de su propio negocio de agencia.

## 5. La demanda agentic llegó antes que la capacidad transaccional

En marzo-2026, en APAC, **ChatGPT superó a Google por 13 puntos porcentuales** en visitas a
páginas de reserva de travel (Criteo). **En el mismo mes, OpenAI retiró la capacidad de reserva
directa de ChatGPT.** El tráfico migró a un asistente que, en ese momento, dejó de poder
cerrar. Ese hueco —intención agentic sin riel transaccional— es el mercado.

## 6. El crecimiento está en plataformas verticales con MCP incorporado

No en frameworks de agentes nuevos. Lo que creció medido en estrellas este año:
[`liketrek/TREK`](https://github.com/liketrek/TREK) (15.842★, AGPL-3.0, creado en marzo-2026 —
15.8k en ocho meses, con MCP server propio), [`Kamra-PMS/kamra-pms`](https://github.com/Kamra-PMS/kamra-pms)
("primer PMS open source agentic-AI-ready"), [`TelivityAI/haip`](https://github.com/TelivityAI/haip),
[`TelivityAI/otaip`](https://github.com/TelivityAI/otaip). El patrón es sistema operativo real +
servidor MCP propio.

Para un engagement esto es buena noticia: la capa agentic se enchufa en lugar de construirse.

## 7. El inventario empieza a distribuirse como *skill*, no como API

[`tourmind-com/Tourmind-Booking-Skills`](https://github.com/tourmind-com/Tourmind-Booking-Skills)
(MIT, 2.414★) es un proveedor B2B publicando sus propias agent skills de booking bajo licencia
permisiva. Los MCP de RollingGo hacen lo mismo con 2M+ hoteles a tarifa mayorista y
compatibilidad con 40+ LLMs. El canal de distribución ya no es "integrá nuestra API": es
"instalá nuestro skill".

## 8. El copyleft domina la plataforma; lo permisivo, la infraestructura

Los tres repos de travel con más tracción son copyleft: TREK (AGPL-3.0, 15.8k★), QloApps
(OSL-3.0 core / AFL-3.0 módulos, 14.5k★), Kamra (AGPL-3.0). Lo permisivo son las piezas de
abajo: graphhopper (Apache-2.0), valhalla (MIT), photon (Apache-2.0), motis (MIT), fli (MIT).

Y hay trampas medidas: [`MikkoParkkola/trvl`](https://github.com/MikkoParkkola/trvl) (95★)
aparece junto a los MIT en toda búsqueda y es **PolyForm Noncommercial 1.0.0** — inutilizable
en un engagement comercial. [`LetsFG/LetsFG`](https://github.com/LetsFG/LetsFG) (2.295★) es MIT
real **más un addendum que pide 1% del valor de la reserva**. QloApps es OSL-3.0 en el core y
AFL-3.0 en los módulos: **la extensión propietaria va en un módulo**.
Ver `agents/top.md` → "Verificar antes de usar".

## 9. Asia tiene el código; Europa tiene la regulación; LATAM tiene al Estado comprando

- **APAC** concentra el open source real de travel (449★, 415★, 179★ y los MCP hoteleros) y la
  adopción más alta medida: **79% de las empresas de travel de APAC ya usan AI, 97% planea**
  (Expedia Group 2026). Singapur publicó en ene-2026 el **marco de gobernanza de AI agentic de
  IMDA**, que cubre cadenas de delegación y coordinación multiagente — el documento regulatorio
  más útil para trabajo con agentes de cualquier región.
- **EMEA** tiene el entorno normativo más denso (Digital Omnibus, Reg. (EU) 2026/1744; alto
  riesgo Annex III corrido a 2-dic-2027 y Annex I embebido a 2-ago-2028) y, a la vez, la
  lectura tranquilizadora de que la mayoría de las herramientas de cara al huésped
  probablemente no son de alto riesgo. En Medio Oriente la única norma vinculante y específica
  sobre sistemas autónomos es la **Regulation 10 del DIFC** de Dubái.
- **LATAM**: Perú (abr-2026), Chile (sep-2026) y Argentina desplegaron asistentes AI de turismo
  nacional en el mismo año. El comprador es el Estado. Y **el open source de travel no habla
  español**: la búsqueda en español devuelve 1 repo con 0 estrellas.

## 10. Lo que no existe, medido

Siete consultas con cero resultados útiles el 2026-11-21: revenue management hotelero,
implementaciones NDC, ERP de agencia / tour operador, predicción de demoras de vuelo, gestión
de alquiler vacacional, reservas de restaurante y SDKs de GDS con comunidad. El detalle está en
`repos/foundations.md` → "Brechas medidas".

**La escasez nunca es el agente: es el acceso tipado y transaccional al dominio.** Es el cuarto
vertical consecutivo de esta red de KBs donde la medición da ese mismo resultado.

Ampliado el 2026-11-23 con seis consultas más, todas del plano de frontera: APIS, PNR, ETIAS,
biometría de embarque, chequeo de documento tipo Timatic y API de requisitos de visado.
**Cero útiles en las seis.**

## 11. El plano de frontera es la excepción permisiva de todo el vertical

En travel, la regla medida durante cuatro ciclos es que **la plataforma es copyleft y la
infraestructura es permisiva** (TREK AGPL-3.0, QloApps OSL-3.0 frente a graphhopper, photon,
motis). El documento de viaje rompe la regla: **todo el segmento es permisivo y está vivo.**

[`AndyQ/NFCPassportReader`](https://github.com/AndyQ/NFCPassportReader) (MIT, 867★, push
2026-11-16) lee el chip ICAO 9303; [`konstantint/PassportEye`](https://github.com/konstantint/PassportEye)
(MIT, 471★) y [`sivakumar-mahalingam/fastmrz`](https://github.com/sivakumar-mahalingam/fastmrz)
(Apache-2.0, 174★, push el 2026-11-23) parsean la MRZ;
[`zkpassport/circuits`](https://github.com/zkpassport/circuits) (Apache-2.0) y
[`rarimo/passport-zk-circuits`](https://github.com/rarimo/passport-zk-circuits) (MIT) prueban
atributos sin revelar el documento; y el verificador del **EU Digital Identity Wallet** es
Apache-2.0, mantenido por la Comisión Europea. **Hay dos implementaciones independientes de
cada problema**, que es la señal de un segmento sano y no de un proyecto solitario.

**Por qué pasa esto y no en otros planos:** la identidad documental es un estándar público
(ICAO 9303) y no un contrato comercial. Donde la especificación es pública, el open source
crece. Donde la especificación es contractual (NDC, Timatic, PNR), no hay nada. **Esa es la
regla predictiva del vertical: el piso open source existe exactamente donde el estándar es
público, y en ningún otro lado.**

## 12. El open source de frontera lee el documento pero no conoce la regla

El complemento exacto de la tendencia 1. Allá, el agente planifica y no paga. Acá, **el
software identifica y no decide.** Entre "sé quién sos" y "podés entrar" hay un dato —la regla
de admisión por par pasaporte×destino con su fecha de vigencia— que no existe en abierto.

La única fuente abierta es una cadena de dos repos: [`ilyankou/passport-index-dataset`](https://github.com/ilyankou/passport-index-dataset)
(MIT, 310★) **archivado desde enero-2025**, que apunta como sucesor a
[`imorte/passport-index-data`](https://github.com/imorte/passport-index-data) (MIT, 88★), que
se declara *"updated regularly"* y cuyo dato lleva **nueve meses sin actualizar** (README:
"Last updated: 17 February 2026"; último push 2026-03-01). Su taxonomía es excelente; sus
valores no sirven para decirle a nadie si puede volar.

El dato vigente vive en **Timatic (IATA)**, de acceso contractual. Es el monopolio de datos
más limpio que esta red de KBs midió en cualquier industria: `timatic travel document check
stars:>=20` devuelve **0**.

## 13. Un estándar de identidad en el que el regulador escribe el código

Nuevo y específico de EMEA: la Comisión Europea no publica solo la norma, **publica la
implementación**, y la estratifica por licencia a propósito — especificación **CC BY 4.0**,
apps de referencia **EUPL-1.2**, librerías y servicios **Apache-2.0**.

Esto invierte el hallazgo que la KB de retail registró el mismo mes sobre beckn/ONDC, donde la
especificación era la pieza *restrictiva* (CC BY-NC-SA, NonCommercial) y las implementaciones
eran permisivas. **La licencia de una especificación y la de su implementación son variables
independientes: hay que leer las dos y no se puede predecir una desde la otra.** La regla ya
se verificó en las dos direcciones, en dos industrias, en el mismo mes.

**Corolario de método, el más caro de este ciclo:** [`Kamra-PMS/kamra-pms`](https://github.com/Kamra-PMS/kamra-pms)
pasó de AGPL-3.0 a Apache-2.0 el **2026-11-21** (commit `ce8dec8`), el mismo día en que el
ciclo anterior leyó el archivo y registró AGPL-3.0 correctamente. **Una licencia verificada no
es un hecho permanente: es una medición con fecha.** Desde este ciclo, toda licencia citada en
esta KB lleva la fecha de lectura del archivo.

---
## 14. Dos planos adyacentes, licencias invertidas: la licencia se distribuye por capa

El 2026-11-23 esta KB midió, con siete horas de diferencia y el mismo método, dos planos
vecinos del mismo vertical. El resultado se invierte:

| | Plano de frontera e identidad | Plano operativo de vuelo |
|---|---|---|
| Piezas más grandes | `NFCPassportReader` **MIT** 867★, `PassportEye` **MIT** 471★, `fastmrz` **Apache-2.0** 174★ | `tar1090` **GPL-2.0+** 1979★, `openflights` **AGPL-3.0** 1686★, `readsb` **GPL-3.0+** 707★, `pyModeS` **GPL-3.0** 674★ |
| Dónde está lo permisivo | **En el núcleo**: leer el chip y la MRZ | **En la periferia**: datasets de referencia (`ourairports-data` Unlicense, `airportsdata` MIT) y una caja de herramientas (`traffic` MIT) |
| Dónde está el copyleft | En los accesorios (`Arg0s1080/mrz` GPL-3.0) | **En todo el músculo mantenido** |
| Lo mejor mantenido | Permisivo | Copyleft |

No es casualidad, y la explicación es quién escribe cada capa. El plano de identidad lo
escriben **fabricantes de app y reguladores** que necesitan que otros integren: la licencia
permisiva es el vehículo de adopción, y la Comisión Europea publicando sus librerías bajo
Apache-2.0 es el caso extremo. El plano de vuelo lo escribe una **comunidad de
radioaficionados y académicos** cuyo valor es la red de receptores, no el binario: la GPL
protege el bien común que construyeron con su propio hardware.

**La consecuencia operativa para un engagement:** no existe una respuesta de licencia "para
travel". `intel/market.md` ya dice que *la licencia es arquitectura*; este ciclo agrega la
precisión que faltaba: **la licencia es arquitectura por capa, y hay que medirla capa por
capa, en el ciclo en que se va a usar.** Un arquitecto que generalice desde el plano que miró
primero se equivocará en el segundo, en la dirección que sea.

## 15. La licencia del código deja de alcanzar cuando el repo es cliente de una red

Es el hallazgo metodológico de la segunda pasada del 2026-11-23, y corrige por arriba el
propio método de esta KB.

Durante noviembre esta KB construyó una disciplina que funciona: no confiar en el badge SPDX
de GitHub, abrir el archivo de licencia, anotar su tamaño y la fecha de lectura. Encontró así
que `valhalla` y `airportsdata` eran MIT pese a figurar como `NOASSERTION`, que `readsb` y
`tar1090` eran GPL por la misma marca, que `Ctrip-Style` y `JourniOne-Planning-Skills` no
tienen licencia, y que Kamra PMS cambió de AGPL-3.0 a Apache-2.0 en 48 horas.

`openskynetwork/opensky-api` **pasa esa prueba y sigue sin ser utilizable comercialmente.** Su
`LICENSE.txt` es GPL-3.0 íntegro y correcto. Pero el repo es un **cliente** de la red OpenSky,
una asociación suiza sin fines de lucro, y las fuentes consultadas coinciden en que sus
términos **de dato** licencian investigación y educación sin fines de lucro, evaluación
interna no comercial y fines gubernamentales — no el uso comercial. El archivo de licencia no
lo menciona porque no es su función.

**La regla, generalizable a toda la red de KBs de industria:** hay que clasificar cada repo en
**librería autocontenida** o **cliente de un servicio**. Para la primera, la licencia del
código es la historia completa. Para la segunda hay **dos** documentos, y el segundo no está
en GitHub, no tiene SPDX y no se puede verificar con `raw.githubusercontent.com`. En este
plano, `readsb`, `pyModeS`, `adsb_deku` y `tar1090` son del primer tipo —procesan señal que
uno mismo recibe—, mientras que `opensky-api` y `FlightRadarAPI` son del segundo.

El corolario comercial es incómodo y conviene decirlo entero: **el camino barato a datos de
vuelo (OpenSky, clientes no oficiales de FR24) es el que no se puede facturar, y el camino
facturable (receptor propio con el stack GPL, o contrato de datos) cuesta hardware o dinero.**
Un presupuesto que suponga lo contrario está mal hecho desde la primera línea.

## 16. El regulador europeo trazó la misma línea que esta KB, y la puso en el texto

La pasada de la mañana del 2026-11-23 cerró con una frase sobre el plano de frontera: el open
source **lee el documento pero no conoce la regla**, y entre "sé quién sos" y "podés entrar"
hay un dato que no existe en abierto (tendencia 12). La pasada de la tarde encontró que **el
Anexo III del AI Act divide el mundo exactamente por esa línea** — y que la divide a favor del
camino que esta KB venía recomendando.

El punto 7 del Anexo III (migración, asilo y control de fronteras) **excluye expresamente la
verificación de documentos de viaje** de su literal (d). La lectura concordante de las fuentes
consultadas:

- **Verificación 1:1 — fuera del literal (d).** El viajero confirma su identidad contra el
  chip de su propio pasaporte. Es exactamente lo que hacen `NFCPassportReader` (MIT) y
  `fastmrz` (Apache-2.0), y exactamente lo que proponen las Recetas 7 y 8.
- **Identificación 1:N — dentro, y de alto riesgo.** Reconocer a una persona contra una lista
  de vigilancia.
- **Literal (c) — puede alcanzar igualmente** a un escáner de autenticidad documental usado
  *dentro de una solicitud de visado*, aunque el mismo escáner quede fuera en un mostrador de
  check-in.

Y el calendario se movió: el **Reglamento (UE) 2026/1744** (*Digital Omnibus*, DOUE
2026-07-24, en vigor 2026-07-27) difiere las obligaciones de alto riesgo del Anexo III
autónomo **del 2026-08-02 al 2026-12-02**, y las del Anexo I al **2028-08-02**. Las
obligaciones de transparencia del **Artículo 50 no se aplazaron**: siguen aplicando desde el
2026-08-02.

**Lo que cambia en la conversación con un cliente europeo:** el check-in biométrico de hotel y
el embarque 1:1 **no son el caso regulado**; el matching contra listas **sí**. Son dos
productos distintos, con dos presupuestos de cumplimiento distintos, y conviene no venderlos
en el mismo enunciado. La prórroga a diciembre de 2027 **no es una derogación** —es tiempo, no
permiso— y decirlo así es parte del trabajo.

⚠️ **Límite de verificación declarado.** `ai-act-service-desk.ec.europa.eu`,
`opensky-network.org` y `zenodo.org` **no resuelven DNS desde el entorno de ingesta de esta
KB**. Lo anterior proviene de fuentes secundarias concordantes —incluido el texto citado del
propio Service Desk de la Comisión— y **no fue leído en EUR-Lex**. Antes de comprometerlo en
una propuesta hay que abrir el Anexo III del Reglamento (UE) 2024/1689 y el Reglamento (UE)
2026/1744 en la fuente oficial. Se registra como hallazgo **con su límite pegado**, porque un
hallazgo sin su límite es exactamente como se fabrican los datos que esta KB pasó noviembre
corrigiendo.

## 17. El plano de pago agentic es el primero del vertical donde la licencia no es el problema

Medido el 2026-11-23 (tercera pasada). Durante cuatro ciclos la regla de esta KB fue
**plataforma copyleft, infraestructura permisiva** (→ 8), y el plano de frontera se registró
como *la excepción permisiva* (→ 11). El plano de pago no es una excepción más: es una
**inversión completa**. Las cinco especificaciones con tracción son **Apache-2.0 o MIT**, sin
una sola pieza copyleft, y las cuatro herramientas utilizables también.

La causa no es cultural, es estructural: **es una guerra de estándares entre consorcios**
—Google (AP2, a2a-x402), OpenAI + Stripe (ACP), la fundación x402, Shopify y UCP—, y en una
guerra de estándares la licencia restrictiva es una desventaja competitiva. Nadie cobra por el
protocolo; se cobra por el riel.

**Qué cambia para un engagement.** En todos los demás planos de travel la primera pregunta es
"¿podemos construir sobre esto?". Acá esa pregunta ya está contestada que sí, y la primera
pregunta pasa a ser **"¿cuál de estos sobrevive a 2027?"** — que es una apuesta de arquitectura,
no un problema legal. La respuesta defensiva es la de siempre en esta KB: **neutralidad de
protocolo**, con la capa de autorización como adaptador propio.

## 18. La especificación se congeló; los rieles se mueven

El dato que ordena el plano de pago, medido sobre `pushed_at` el 2026-11-23:

| Capa | Repo | Stars | Último push |
|------|------|-------|-------------|
| Rieles (mover dinero) | `x402-foundation/x402` | 6822 | 2026-11-20 |
| Comercio (merchant of record) | `Universal-Commerce-Protocol/ucp` | 3517 | 2026-11-21 |
| **Autorización (¿el usuario consintió?)** | `google-agentic-commerce/AP2` | 3283 | **2026-06-17** |
| **Interacción comprador-agente-comercio** | `agentic-commerce-protocol/...` | 1609 | **2026-07-18** |

Las dos capas que la prensa trata como el corazón del pago agentic —**autorización e
interacción**— llevan **cuatro y cinco meses sin un commit**, mientras las de rieles y comercio
empujaron **esta semana**. Y `AP2 mandate implementation stars:>=20` devuelve **0**: el
protocolo más citado no tiene implementación con tracción.

**La lectura, que es incómoda y por eso se registra:** la prensa del sector —y los ciclos
anteriores de esta KB, que hablaban del "corte en el pago" como si hubiera infraestructura
detrás— está adelantada respecto del código. **El mandato firmado, que es la primitiva de la
que depende todo el discurso de "el agente compra por vos", es hoy una especificación quieta.**
Para travel eso no es malo: confirma que el entregable honesto sigue terminando en el merchant
of record, y que **la capa de autorización es un lugar donde construir IP, no una dependencia
que se adopta.**

⚠️ **Cautela explícita:** un repo quieto no es un estándar muerto. AP2 puede haberse movido a
otra gobernanza —varias fuentes secundarias mencionan la FIDO Alliance en abril de 2026, y
**no se pudo corroborar desde este entorno**—. Lo que está medido es el `pushed_at` del repo
canónico, no el destino del estándar. Antes de descartarlo en una propuesta, verificar dónde
vive hoy.

## 19. El plano de visibilidad es el primero que está completo y es todo horizontal

Medido el 2026-11-23 (cuarta pasada). Los tres planos anteriores de esta KB tenían el mismo
defecto de forma: **faltaba la pieza**. Frontera: se lee el documento, no se conoce la regla.
Vuelo: se sabe dónde está el avión, no qué se le debe al pasajero. Pago: la especificación está
quieta. El plano de visibilidad **rompe el patrón**: la herramienta está, es permisiva, está
activa y es buena.

| Capa | ¿Existe? | Mejor pieza | Licencia | Stars |
|------|----------|-------------|----------|-------|
| Vocabulario | **sí** | `schemaorg/schemaorg` | Apache-2.0 | 6316 |
| Tipado / emisión | **sí** | `google/schema-dts` | Apache-2.0 | 1262 |
| Auditoría de lo emitido | **sí** | `scrapinghub/extruct` | BSD-3-Clause | 985 |
| Medición de citas | **sí** | `elmohq/elmo` | MIT | 713 |
| Analítica de crawlers AI | **sí** | `yaojingang/GEOInflow` | MIT | 866 |
| **Cualquiera de las anteriores sabiendo qué es un hotel** | **no** | — | — | **0** |

**Qué significa comercialmente, que es lo contrario de lo que parece.** Un plano completo y
permisivo **no es una mala noticia para un integrador: es la mejor de las cuatro.** En
frontera, vuelo y pago, la respuesta honesta a un cliente incluye "esta pieza hay que
construirla y es riesgo". Acá la respuesta es **"la máquina ya está; lo que no existe es el
adaptador al dominio"** — y el adaptador de dominio es exactamente lo que un studio vertical
hace mejor y más rápido que un proveedor horizontal. **El trabajo es ensamblar y domeñar, no
inventar.**

## 20. El estándar que todas las guías recomiendan no tiene evidencia de uso

`llms.txt` es, en 2026, la recomendación número uno de las guías de "hotel AI-friendly". Lo
medido *[fuentes secundarias; los sitios de los estudios no son alcanzables desde este entorno
de ingesta]*:

| Qué | Medición | Fuente |
|-----|----------|--------|
| Adopción, top-1000 dominios | **9,3%** | Rankability, scan sep-2026 |
| Adopción, 300.000 dominios | 10,13% | SE Ranking |
| Dominios con `llms.txt` válido que **no recibieron ni una petición** en mayo-2026 | **97%** | Ahrefs (~38.000 dominios) |
| De las peticiones que sí hubo, cuántas eran de bots | 96% | Ahrefs |
| Proveedores grandes que confirman usarlo para decidir citas | **ninguno** | — |

**La asimetría que importa:** la adopción (~10%) se cita todo el tiempo; **el uso (~0%) no se
cita nunca.** Y la adopción sin uso es, exactamente, una métrica de vanidad.

**La regla que queda:** publicar `llms.txt` —cuesta minutos, no hace daño, y si mañana un
proveedor empieza a leerlo ya está puesto— **y no venderlo jamás como la palanca.** La palanca
con evidencia de consumo es el JSON-LD del tipo correcto. Esta distinción es defendible frente
a un cliente que haya leído las mismas guías, y es la clase de cosa por la que un cliente
decide que le decimos la verdad.

## 21. El organismo de estándares del vertical no tiene licencia

`OpenTravel` —el cuerpo que define la distribución de travel, miembro de la Linux Foundation,
que se sumó a Overture Maps en agosto de 2025 bajo el título *"AI-ready travel infrastructure"*
y que anuncia que pasará a llamarse Open Travel Foundation— tiene en GitHub: **12 repos, máximo
22 estrellas, 8 sin licencia declarada, ningún push desde enero de 2025.** La especificación
OTA 1.0 se distribuye además bajo el *OpenTravel License Agreement*, que **no es open source**.

Enfrente, el vocabulario que los motores efectivamente consumen —`schema.org`— es Apache-2.0,
6316 estrellas y tuvo push esta semana.

**La conclusión de arquitectura, y es directa:** para descubrimiento agentic, **modelar en
Schema.org**; tratar OTA/OTM como **formato de integración con GDS heredado**, que es donde
sigue siendo imprescindible. No son competidores: son capas distintas que la prensa del sector
mezcla. Seguir la alineación con Overture (GERS IDs) porque es real y puede cambiar esto —pero
a hoy el anuncio tiene un año y tres meses **y no hay código que lo acompañe.**

⚠️ **Cautela, la misma que en el punto 18:** un repo sin push no implica un organismo inactivo.
OpenTravel publica especificaciones fuera de GitHub y su trabajo de comités no es visible ahí.
Lo medido es **el estado de su código público y de sus licencias**, que es lo que determina si
podemos construir encima — no la salud del organismo.

## 22. El piso open source sabe **informar** sobre un tren y no sabe **venderlo**

Medido el 2026-11-23. Es la tendencia estructural del plano terrestre y la más transferible a
otras industrias de la red.

Un itinerario tiene dos mitades y el open source solo cubre una:

| Capacidad | ¿Existe en open source? | Evidencia |
|-----------|-------------------------|-----------|
| Horario, andén, trayecto, retraso | **Sí, y sobra** | `hafas-client` ISC 372★, `public-transport-enabler` GPL-3.0 456★, `OpendataCH/Transport` MIT 269★, `navitia` AGPL-3.0 456★, 8 servidores MCP |
| Precio **mostrado** | Parcial | los mismos clientes lo exponen cuando el operador lo publica |
| **Oferta** (qué puedo venderte, bajo qué condición) | **No** | `osdm client implementation` → **0** |
| **Tarificación** | **No** | `fare engine open source` → **0** |
| **Reserva de plaza** | **No** | `train booking api stars:>=20` → **0** |
| **Emisión** | **No** | `ticket vending machine open source` → **0** |
| **Derechos y reembolso** | **No** | `passenger rights compensation rail` → **0** |

Es la misma frontera que el KB de retail encontró en fulfilment —*"el piso open source cubre la
matemática y se detiene en el comercio"*— pero un paso antes: aquí se detiene en **la
información**. La explicación es la misma y vale generalizarla: **consultar es una operación
sin contraparte; ofrecer es un compromiso.** Una oferta liga inventario, tarifa, condición de
reembolso y responsabilidad frente al pasajero. Nadie publica un compromiso bajo licencia MIT.

**Consecuencia para un engagement:** el prototipo que impresiona —"el agente te arma el viaje
en tren por Europa"— se construye en días con código permisivo. **El 100% del riesgo y del
presupuesto está del otro lado de la línea**, y la línea es exactamente el momento de decir
*"esta plaza, a este precio, con esta condición"*. Presupuestar como si el prototipo fuera el
80% es el error estructural de este plano.

## 23. El estándar abierto llegó, el regulador lo respaldó, y nadie escribió el cliente

**OSDM** (Open Sales and Distribution Model, UIC IRS 90918-10) está en GitHub bajo
**Apache-2.0**, con 95 estrellas y push del 2026-11-20. Cubre oferta, tarifa, reserva y emisión
— es decir, **exactamente las cuatro capacidades que la tendencia 22 acaba de registrar como
inexistentes**. Suecia lo adoptó como estándar nacional de distribución en 2025. La TSI de
telemática de la UE lo reconoce. Y:

```
search/repositories  q="osdm client implementation"   →  TOTAL = 0
```

Lo único que existe es `mainmatter/reStations` (Apache-2.0, 8★): implementa **solo la Places
API** —el catálogo de estaciones— y no tiene push desde **2025-04-02**.

Esto rompe el supuesto que esta KB venía usando para explicar el vacío del vertical. En
distribución aérea el argumento era sólido: *no hay NDC open source porque el esquema está
licenciado por IATA y el acceso es contractual* — **la barrera era legal**. En ferrocarril esa
explicación no está disponible: **la especificación es Apache-2.0, pública, con concesión de
patente, respaldada por el regulador y con un calendario de implementación 2027–2028.** No hay
barrera legal alguna, y aun así no hay código.

Queda una hipótesis, y conviene escribirla como hipótesis: **lo que falta no es permiso sino
contraparte.** Un cliente OSDM sin un operador que exponga un servidor OSDM no sirve para nada,
así que nadie lo escribe primero. Es un problema de arranque en dos lados, no de licencia.

**Predicción falsable, para que la próxima pasada la verifique:** si la implementación de la
TSI 2027–2028 avanza, **aparece al menos un cliente OSDM open source con ≥25 estrellas antes de
que termine 2027**. Si en esa fecha `osdm client implementation` sigue devolviendo 0, la
hipótesis del arranque en dos lados es insuficiente y hay que buscar otra causa. *Medir esta
consulta exacta en cada pasada de travel.*

## 24. La licencia de una especificación se decide por organismo, no por categoría

El KB de retail cerró su ciclo 9 con una regla propuesta para las 12 industrias: *la licencia
de una especificación es una licencia de documentación y arrastra restricciones que las
licencias de código no tienen*. La evidencia era buena — beckn bajo **CC BY-NC-SA**
(no comercial) y ONDC bajo **CC BY-ND** (sin derivados), frente a UCP/ACP/AP2/x402 todas
Apache-2.0.

**El plano terrestre de travel la contradice dentro de un solo plano**, con los archivos
leídos:

| Especificación | Organismo | Licencia (archivo leído) | Qué permite |
|----------------|-----------|--------------------------|-------------|
| **OSDM** | UIC (ferrocarriles) | **Apache-2.0**, 11374B | Vendorizar el esquema, con concesión de patente |
| **GBFS** | MobilityData | **CC BY 3.0**, 19467B | Atribuir y derivar; **sin concesión de patente** |
| **Transitland Atlas** | Interline | **CC BY 4.0**, 18657B | Es un dataset, no código |
| **awesome-transit** | MobilityData | **CC0-1.0**, 6974B | Dominio público, sin condiciones |

Cuatro artefactos del mismo ecosistema, **cuatro familias de licencia distintas**, y la más
permisiva de todas es la del estándar comercialmente más sensible. La regla corregida:

> **La licencia de una especificación no se infiere de que sea una especificación. Se lee, una
> por una, y puede ser de código.** Lo que sí generaliza del hallazgo de retail es la parte
> operativa: **el repo de la especificación se verifica por separado del repo de la
> implementación**, porque no hay ninguna razón para que coincidan.

Vale como corrección entre KBs, no como refutación: la observación de retail era correcta
**sobre los artefactos que midió**. Lo que no sobrevive es la generalización a las 12
industrias.


---
*Fuentes: Phocuswright 2026, IATA Global Passenger Survey 2026, Expedia Group APAC 2026,
Criteo, Visa 2026, Agoda, prensa especializada de travel, textos regulatorios de UE/APAC/LATAM,
Skift Data + AI Summit Europe (oct-2026), ICAO FALP14 (abr-2026),
Reglamento (UE) 2026/1744 (*Digital Omnibus*, DOUE 2026-07-24) y Anexo III del Reglamento (UE)
2024/1689 vía AI Act Service Desk de la Comisión, regla de reembolso automático del US DOT
(vigente 2024-10-28), Ley Marco de AI de Corea del Sur (2026-01-22), Ley de AI de Vietnam
(2026-03-01), consulta pública de gobernanza de AI de Malasia (2026-07-10),
Plano de Dados Abertos da ANAC 2026-2028,
y medición directa sobre la API de GitHub y sobre los archivos de licencia en
`raw.githubusercontent.com`. Las cifras de proveedor sin informe primario
localizable están marcadas como tales en `intel/market.md`.
Los puntos que no pudieron leerse en su fuente primaria por restricción de red del entorno de
ingesta (`ai-act-service-desk.ec.europa.eu`, `opensky-network.org`, `zenodo.org`, y en esta
quinta pasada `era.europa.eu` y `transport.ec.europa.eu`, que afectan al Reglamento de
Ejecución (UE) 2026/253 y a COM(2026) 232 final) llevan la
advertencia pegada al hallazgo, no en una nota al pie.*

## 25. La emisión dejó de ser reporte anual y pasó a ser atributo de compra

Sexta pasada, 2026-11-23. Hasta ahora la huella de carbono de un viaje se
calculaba **después**, una vez por año, para un informe de sostenibilidad. Dos
hechos medidos este ciclo muestran el desplazamiento:

- `andreacappelletti97/google-flights-mcp` (ISC, commit del 2026-11-01)
  devuelve **CO₂ por leg junto al precio**, en la misma respuesta de búsqueda.
- `abahgat/timcp` (Apache-2.0) expone Scope 3 categoría 6 como **tool
  invocable**, no como exportación de planilla.

Cuando la emisión viaja en la misma estructura que la tarifa, deja de ser
contabilidad y pasa a ser **criterio de ranking**. Eso cambia el requisito del
producto: ya no alcanza con poder calcular la huella del viaje cerrado, hay que
poder calcularla **para cada opción que se muestra**, con la latencia de una
búsqueda.

## 26. El modelo de referencia del vertical no tiene licencia de software, y nadie lo nota

`google/travel-impact-model` es el modelo que usa la coalición Travalyst y la
referencia de hecho del cálculo de emisiones aéreas. Medido este ciclo
clonando el repo:

- No contiene implementación. Es `README.md` + `contributing.md` + `images/` +
  `projects/`.
- Su archivo `LICENSE` dice **CC BY 4.0**; su `README.md`, línea 694, dice
  **CC BY-SA 4.0**. El repo se contradice.
- **No es Apache-2.0.** El único Apache-2.0 del repo está en las notas al pie
  2 y 4 y cubre **los íconos de las figuras**.

Las tres cosas sobreviven porque casi nadie abre el `LICENSE` de un repo de
Google. La tendencia real: **en el plano de emisiones, la pieza central del
vertical se distribuye bajo licencia de contenido, no de software** — sin
concesión de patente y, en una de las dos lecturas, con ShareAlike vírico sobre
el dato derivado.

## 27. Lo mejor mantenido del cálculo de emisiones es deliberadamente no comercial

Las dos calculadoras alineadas a GLEC / ISO 14083 más activas del espacio
—`majidkabir/Sootcase` y `majidkabir/Carbonara`, ambas con commits del
**2026-11-23**, el día de esta pasada— son **PolyForm Noncommercial 1.0.0**.
Están vivas, cubren carretera, ferrocarril, mar, aire y vía navegable con ruteo
mundial, y **una consultora no puede usarlas en un engagement**.

Es el segundo plano de esta KB donde lo mejor mantenido es lo que no se puede
vender (el primero fue `MikkoParkkola/trvl`, también PolyForm, registrado en el
ciclo 9). El patrón emergente: **en travel, el autor individual que mantiene
bien elige licencia no comercial precisamente para que las consultoras no lo
usen gratis.** Buscar "open source" sin leer el `LICENSE` produce un plan de
proyecto que no se puede ejecutar.

## 28. La regulación de emisiones es el único eje del vertical donde EMEA va claramente adelante

Comparadas las cuatro regiones este ciclo, el stack obligatorio sólo existe
completo en una:

| Región | Obligación de reporte de emisiones de viaje |
|---|---|
| **EMEA** | CSRD/ESRS (Scope 3 cat. 6) + ReFuelEU (2% hoy, 6% en 2030) + EU ETS |
| **North America** | **Ninguna específica de viajes encontrada.** CORSIA vía ICAO alcanza a aerolíneas, no a programas corporativos |
| **APAC** | Calendarios de SAF por país (Singapur 1% movido a 2027, Japón 10% a 2030), sin régimen de reporte homogéneo |
| **LATAM** | Mandato brasileño de SAF **esperado para enero de 2027**, sin detalles publicados |

En los otros planos de esta KB (pago, visibilidad, tierra) la ventaja regional
rota. En emisiones no rota: **el producto se diseña contra requisitos europeos
y se degrada hacia las otras tres regiones**, no al revés. Eso invierte el
orden de diseño habitual de un engagement norteamericano.

## 29. El agente sabe auditar la página para un usuario ciego y no sabe prometerle la habitación a uno en silla de ruedas

Séptima pasada. El plano de accesibilidad se parte en dos con madurez opuesta:

| | Digital (¿se puede completar la reserva?) | Físico (¿se puede entrar?) |
|---|---|---|
| Regulación | EAA vigente (EMEA), ACAA web (NA), LBI art. 63 (Brasil) | Wheelchair Rule (NA), LBI art. 45 10% (Brasil), ajuste razonable (Japón) |
| Open source | Lighthouse y `equal-access` **Apache**, `axe-core` MPL | Dos routers **LGPL**, esquema de veredas **CC BY-ND** |
| Agentes / MCP | 3 servidores MCP con licencia OSI | **0** |
| Vocabulario estándar | WCAG / EN 301 549 | **schema.org: ninguno** para lugares; OpenTravel: rico y **sin licencia** |

La consecuencia práctica: **un agente de viaje de 2026 puede ser accesible y
seguir sin servir a la persona.** Es el mismo patrón que la quinta pasada
encontró en tierra (informa pero no vende), un plano más abajo.

## 30. En este plano el badge de licencia no alcanza

De 7 repos centrales del plano, **en 4 la licencia que muestra GitHub o la
wiki de OSM no coincide con el archivo**: 2 están **equivocadas**
(`openrouteservice`, y `wheelmap-frontend` en la wiki) y 2 aparecen como
`NOASSERTION` (`sa11y`, `TaskarCenterAtUW/AccessMap`). El caso de manual es `openrouteservice`:
la wiki dice Apache (cierto hasta 2018), GitHub dice GPL-3.0 (lee sólo el
texto GPL que acompaña por convención a LGPL), y el repo es LGPL-3.0. Los
errores son **sistemáticos**, no anecdóticos:

- **Cualquier repo con `LICENSE.LESSER`/`COPYING.LESSER` aparece como GPL** en
  GitHub. Un escáner de licencias que confía en la API bloquea usos legítimos.
- **Las wikis y directorios congelan la licencia del momento en que se
  escribió la entrada**: `openrouteservice` (Apache→LGPL), `sa11y` (MIT→GPL-2.0).
  Un relicenciamiento no actualiza a quien lo citó.

Para Globant: el control de licencia de un SOW se hace **leyendo el archivo en
el commit que se va a usar**, y el commit se fija.

## 31. Es el primer eje donde las cuatro regiones tienen ley vigente — y ninguna dicta el formato del dato

North America (ACAA, Wheelchair Rule), EMEA (EAA), APAC (Japón, 2024) y LATAM
(Brasil, LBI) tienen obligación **vigente** de accesibilidad que toca viaje.
En los demás planos de esta KB siempre había una región sin ley. Pero **ninguna
de las cuatro fija un formato de dato** para describir una habitación o una
entrada: obligan al resultado, no a la representación. El formato lo tiene que
elegir el integrador — y la elección permisiva medida es `a11yjson` (MIT),
alimentado desde los códigos de OpenTravel que el hotel ya emite.

## 32. La obligación sobre reseñas llegó a tres regiones y la capa open source que la cumpliría está vacía

Es la asimetría más limpia que esta KB midió, porque las dos mitades se midieron
el mismo día con el mismo método.

**La obligación, fechada.** La regla de la FTC (16 CFR Part 465) alcanza a quien
**difunde** reseñas falsas, no solo a quien las escribe, y la FTC nombró
expresamente las generadas por AI. Italia puso en vigor la Ley 34/2026 el
**7-abr-2026**, con prohibición de compraventa de reseñas y **prueba de estadía**
exigible. China publicó en **jun-2026** reglas de divulgación: enlace comercial
etiquetado como publicidad, base de la reseña declarada. La Comisión Europea
abrió **procedimiento formal DSA contra Booking.com el 21-oct-2026** por listados
fraudulentos, phishing y publicidad no identificada. Y la AGCM italiana ya multó
a **Trustpilot con 4 M€** por no verificar reseñas **marcadas como "verificadas"**.

**La herramienta, medida.** `fake review detection stars:>=20` devuelve **8 repos
en todo GitHub**, y uno de los ocho es de robótica escolar y entra por la sigla
`FTC`. El más estrellado (109★) no tiene licencia. El único MIT real está
**archivado**. `review moderation trust safety stars:>=200` y
`review authenticity provenance stars:>=50` devuelven **0**.

**Por qué no es un hueco de madurez.** En los demás planos de esta KB el vacío se
explicaba por juventud: el estándar acababa de salir, nadie había escrito el
cliente. Acá no: la detección de reseñas falsas tiene veinte años de literatura.
Lo que no hay es **razón para publicarla**. Quien tiene un detector bueno lo tiene
cerrado, porque publicarlo es publicar el manual de evasión. **Es el primer plano
del vertical donde el vacío open source es estructural y no transitorio** — y por
eso es el que no se resuelve esperando otro ciclo.

## 33. Las tres capas de un mismo plano envejecieron a velocidades distintas, y las estrellas apuntan al revés

La cohorte que **lee** reseñas (ABSA) suma **4535★ en seis repos** y tiene **un
solo push en 2026**. La cohorte que prueba **procedencia** de contenido (C2PA)
suma **1045★ en siete repos** y tuvo **dos push el día de este ciclo**. Menos de
una cuarta parte de las estrellas, y toda la vida.

La lectura operativa: **las estrellas miden el pasado de un plano y `pushed_at`
mide si se puede construir sobre él mañana**, y en este plano las dos métricas
apuntan en direcciones opuestas. Elegir por la métrica visible lleva directo a
`songyouwei/ABSA-PyTorch`: 2112★, el más recomendado del tema en listados y
blogs, **archivado desde 2023, sin archivo de licencia y con 516 forks**. Es la
tercera vez que esta KB mide que el repo más estrellado de un plano es el menos
tomable (tras `plane-notify` en vuelo y `axuse` en accesibilidad). **Ya no es
anécdota: es el comportamiento esperable de un vertical donde el prestigio
académico y el mantenimiento comercial no coinciden.**

## 34. El error de licencia tiene dos direcciones, y la segunda es la cara

Esta KB registró tres casos de **`NOASSERTION` escondiendo una licencia permisiva
real** (`valhalla`, `odoo`, `airportsdata`): GitHub no reconocía el archivo, y
leerlo revelaba que el repo **sí** era usable. El costo de ese error es una
oportunidad perdida.

Esta pasada midió el error inverso. `songyouwei/ABSA-PyTorch` **no tiene archivo
de licencia en ninguna ruta estándar de su rama default** —comprobado una por
una—, su único rastro es un badge de `shields.io` cuya URL apunta a
`packagist/l/doctrine/orm.svg`, es decir **la licencia de un ORM de PHP sin
relación con el proyecto**, y la API de GitHub devuelve `MIT`. El costo de este
error no es perder una oportunidad: es **construir sobre un permiso que nadie
otorgó**, y con 516 forks la afirmación ya se replicó 516 veces.

Y en el mismo plano apareció una tercera forma: **dual licensing invisible**.
`c2pa-rs`, `c2pa-swift` y `c2pa-cpp` traen `LICENSE-MIT` **y** `LICENSE-APACHE`;
la API muestra `NOASSERTION` para el primero y solo `Apache-2.0` para los otros
dos. Acá la API **esconde una opción que el proyecto concede** — y si el contrato
de un cliente excluye Apache-2.0 por su cláusula de patentes, leer el badge
habría descartado un stack tomable bajo MIT.

**La regla, en su forma final tras ocho pasadas:** no se lee el archivo *porque
GitHub diga `NOASSERTION`*. Se lee **siempre**, incluso —sobre todo— cuando la
API afirma una licencia limpia.

## 35. El resumen AI de reseñas creó un modo de falla nuevo: no miente, omite

El hallazgo de *Which?* del **3-jul-2026** sobre los resúmenes AI de Tripadvisor
no es un caso de alucinación: es de **supresión de la cola**. Los resúmenes
omitían intoxicaciones alimentarias —102 menciones en una propiedad en
marzo-2026, con 32 reseñas de 1-2 estrellas entre dic-2025 y abr-2026— y
denuncias de acoso sexual, describiendo lo más cercano como "algunas carencias
señaladas por unos pocos", mientras los resúmenes de Google **sí** advertían
"posibilidad de enfermedad" sobre la misma propiedad. Tripadvisor discrepa y
sostiene que suprime el resumen en fichas con incidentes graves.

**Por qué es tendencia y no incidente.** Un resumen es, por construcción, una
media; y la información que un viajero más necesita vive en la cola. Es el mismo
error de forma que esta KB registró en accesibilidad —colapsar
`sí / no / desconocido` en `sí`— aplicado al texto: **el promedio de las reseñas
borra exactamente lo que había que leer**. Dos competidores corrieron sobre el
mismo corpus y uno advirtió: no es un límite del método, es una decisión de
diseño. Y para quien construye, es la regla operativa más clara del plano:
**la minoría grave no se promedia, se eleva** — con volumen y ventana temporal
declarados. Receta 23.

## El equipaje — la tendencia que mejora mientras su software no existe (2026-11-23)

Noveno plano de esta KB. La tendencia tiene una forma que no se repite en ningún otro plano del
vertical: **el indicador mejora con fuerza, el costo unitario está publicado, la obligación está
vigente en tres continentes, y la capa de software abierta es un repo de 17 estrellas.**

**Lo que mejora.** SITA mide la tasa global de equipaje mal manejado en **4,9 por 1.000 pasajeros**
en 2025, **una baja del 23%** interanual, con el volumen total cayendo 19% a **24 millones de
piezas** — las dos cifras **por debajo de prepandemia**, y sobre un récord de ~5.000 millones de
pasajeros. Es la mejora operativa más grande que esta KB registró en cualquier plano de cualquier
industria, y se atribuye a digitalización y rastreo. (⚠️ Primario no leído: el PDF del informe no
resuelve desde esta red. Hay una cifra discrepante de 3,4 con alza del 9%, probablemente la de
APAC leída como global; **se registran las dos**.)

**Lo que no cambia.** Siguen siendo **USD 6.300 millones al año** y **USD 260 por pieza** — y SITA
lo traduce a la frase que vende el plano: **cinco piezas mal manejadas borran la ganancia de un
vuelo entero**. El riesgo no está distribuido: pasa de **1,65 por mil en doméstico a 9,12 en
internacional**, un factor de 5,5 que se concentra en **la transferencia**, que es exactamente el
tercero de los cuatro puntos de custodia de la Resolución 753.

**La tendencia regulatoria va en tres direcciones a la vez, y es la primera vez que esta KB mide
eso.** En los ocho planos anteriores la regulación empujaba hacia el mismo artefacto en las tres
regiones (un registro replayable de por qué un sistema automatizado decidió algo). Acá no:

| Región | Hacia dónde empuja | Artefacto que exige |
|--------|-------------------|---------------------|
| North America | **Un reloj.** Reembolso de la tasa si la pieza no llega en 12 h (doméstico) | Dos sellos de tiempo y un MBR |
| EMEA | **Un límite por pasajero.** 1.519 DEG vigentes desde dic-2024, que prevalecen sobre las condiciones de transporte | Un motor de liquidación que agregue por **pasajero**, no por reserva |
| APAC | **Una tecnología.** Mandato RFID de la CAAC, *whole-process tracking* | Infraestructura física de lectura |
| LATAM | **Un número.** Franquía mínima de 10 kg del art. 14 de la Resolución 400 | Verificación de tarifa contra norma |

**Cuatro obligaciones, cuatro artefactos distintos, ninguna convergencia.** Para una práctica
global eso significa lo contrario de lo que significaba en los planos anteriores: no hay un solo
build que sirva en las cuatro jurisdicciones. Hay **un modelo de datos común** — la pieza, la
etiqueta, el evento con hora — y **cuatro consumidores distintos** de ese modelo. Es un argumento
de arquitectura, no de cumplimiento: modelar el evento de custodia una vez y derivar las cuatro
obligaciones, en lugar de construir cuatro integraciones.

**La tendencia de software, medida y contraintuitiva.** La capa existe y **apareció este año**:
[`adamf/jetway`](https://github.com/adamf/jetway) fue creado el **29-ago-2026**, tiene 72.163
líneas de Go bajo MIT, y tuvo push **el día de esta medición**. Tres meses de existencia para la
primera implementación abierta de BSM/BPM/BUM y de los expedientes AHL/OHD/FWD. **Es demasiado
nuevo para llamarlo tendencia y demasiado grande para ignorarlo**: 5 forks, un mantenedor,
pre-1.0 por declaración propia. La lectura honesta es que el plano pasó de *imposible* a
*posible con riesgo de proveedor único* en un trimestre.

**Y la tendencia que no se movió.** `airline operations agent stars:>=10` devuelve **0 repos en
todo GitHub**. Mientras la planificación de viaje tiene adopción de consumidor del 25% al 67%
según la región, **la operación aérea no tiene un solo agente con diez estrellas**. Toda la ola
agentic de 2026 que esta KB viene registrando está del lado de **buscar y reservar**; ninguna del
lado de **operar y responder**. Es la brecha más grande y más estable del vertical, y es donde un
estudio con acceso a sistemas de operador tiene ventaja sobre un laboratorio de IA.
