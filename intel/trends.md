---
industry: travel
region: Global
updated: 2026-11-28
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

## 36. El precio es el primer plano donde lo que falta no es una pieza, es una categoría

En los nueve planos anteriores, «lo que no existe» siempre fue una pieza concreta dentro de una
categoría poblada: faltaba el cliente de OSDM, faltaba el agente de equipaje del lado del operador,
faltaba el detector de reseña falsa. En el plano del precio falta **la categoría entera**:

| Consulta (`search/repositories`, 2026-11-23) | `total_count` |
| --- | --- |
| `price explanation transparency algorithm` | **0** |
| `algorithmic pricing disclosure` | 1 (ajeno al tema: `Rastaman4e/-1`, sin licencia, 2021) |
| `personalized pricing audit` | 1, **y es de retail** (`mizcausevic-dev/retail-decision-record-audit-str`, MIT, 0★) |

Cero no es «pocos». Significa que nadie nombró el problema todavía en código, mientras tres regiones
ya lo nombraron en ley. La única pista existente viene **del vertical de al lado**: el repo de
auditoría de decisiones es de retail, el mismo vertical cuyo plano de *fulfilment* esta rotación
procesó en la pasada anterior.

## 37. La brecha horizontal-vertical del precio es la mayor medida en este KB

La tendencia 8 de este archivo dice que el copyleft domina la plataforma y lo permisivo la
infraestructura. El plano del precio no la contradice: **la lleva al extremo**. Todo es permisivo
—Apache-2.0 y MIT de punta a punta, sin una sola licencia copyleft en el plano— y la asimetría se
corrió de la licencia a la **masa**:

| Capa | Suma de estrellas | Licencias | Mantenimiento |
| --- | --- | --- | --- |
| Horizontal: `or-tools` + `statsforecast` + `pymc-marketing` | **20.731** | Apache-2.0 ×3 | Push en los últimos 5 días |
| Vertical: `revmng` | **2** | MIT | Un solo día de pushes, hace 5 meses |

Un factor de **10.000×**. Y no es que el vertical sea malo: `revmng` implementa Littlewood, EMSR-a/b,
el DP exacto, overbooking, bid prices de red y las métricas del campo, sin dependencias y con
procedencia por resultado. **Es que el vertical es una persona.** Creado el 2026-06-16 por un autor
individual, con CI, PyPI y validación contra ejemplos publicados — y dos estrellas.

La consecuencia para una propuesta es directa y poco cómoda: en este plano Globant **no se apoya en
una comunidad**, se apoya en una biblioteca de un autor. Se fija versión, se lee el código (es
chico y sin dependencias, se puede) y se presupuesta mantenerla.

## 38. La procedencia llegó al precio antes que la obligación de divulgar, y por accidente

`revmng` emite en cada resultado la versión de la biblioteca, el *hash* de las entradas y el
*timestamp*, serializables con `to_dict()`. Su README presenta eso como buena práctica de
reproducibilidad —no menciona ni a Nueva York, ni a la CRD, ni a SAMR—. Pero **es exactamente el
artefacto que las cuatro jurisdicciones de este plano necesitan**, y es la única pieza del vertical
que lo emite de fábrica.

Es el movimiento inverso al de la tendencia 26 (el modelo de referencia del vertical sin licencia de
software, que nadie nota): acá la pieza correcta existe **por motivos técnicos** y todavía nadie la
conectó al motivo regulatorio. El trabajo que queda no es inventar la procedencia: es **traducirla a
la obligación local**, que es la mitad que no existe.

Y hay un corolario de arquitectura que es la parte más valiosa del plano entero. El § 349-a de Nueva
York se dispara cuando un algoritmo fija el precio **usando el dato personal del consumidor**.
`revmng` toma tarifas, demanda, capacidad, no-shows y costos; **no toma ni un atributo de la
persona**. Por lo tanto: *elegir revenue management por capacidad en lugar de precio personalizado
es una postura de cumplimiento, no sólo una decisión de modelado*. Es la única respuesta
**estructural** —en lugar de documental— que apareció en diez planos de este KB.

## 39. Es el primer eje donde una región tiene el despliegue y no la norma, y es LATAM

Nueve planos construyeron el mismo retrato de LATAM: **la norma existe y el código no**. El art. 14
de la Resolución 400/2016 con sus 10 kg, el 10% de habitaciones accesibles, el Estado comprando
turismo nacional. La conclusión repetida era que en LATAM se vende cumplimiento sobre un piso
técnico ausente.

El precio lo da vuelta:

| Región | ¿Norma vigente sobre precio algorítmico? | ¿Motor de AI desplegado en operadores locales? |
| --- | --- | --- |
| North America | **Sí** (NY § 349-a, 2025-11-10) — y una prohibición pendiente de firma | Sí (Delta/Fetcherr, negado como personalizado) |
| EMEA | **Sí** (CRD, deber de informar personalización) | Sí (Accor/IDeaS) |
| APAC | **Sí**, y con multa ya aplicada (SAMR/Trip.com) | Sí (Trip.com, Fliggy) |
| LATAM | **No.** Tres proyectos en trámite (PL 1309/2026, PL 1635/2024, PL 5441/2025) | **Sí**: Azul (Brasil, primer cliente en vivo de Fetcherr), Viva Aerobus (México, desde mayo 2024) |

Lo que cambia en la propuesta comercial es el verbo. En NA, EMEA y APAC el cliente **cumple**: hay
fecha y texto, y el trabajo es satisfacerlos. En LATAM el cliente **se anticipa**: el motor ya cobra
precios hoy y la norma llega después, con tres proyectos apuntando todos a transparencia algorítmica
y fiscalización por ANPD/Senacon/CADE. Quien registre la decisión desde ahora no reconstruye nada;
quien no, va a tener que explicar retroactivamente precios ya cobrados.

## 40. Las cuatro regiones piden el mismo dato y ninguna pide el mismo artefacto — y una exige una frase literal

Es la cuarta vez que este KB mide esta forma (equipaje fue la tercera), pero es la primera en que una
jurisdicción no pide un formato ni un umbral sino **texto exacto en pantalla**:

| Región | Disparador | Artefacto exigido |
| --- | --- | --- |
| North America (NY) | Algoritmo + **dato personal del consumidor** | La frase literal **«THIS PRICE WAS SET BY AN ALGORITHM USING YOUR PERSONAL DATA»**, clara y visible |
| EMEA | Precio **personalizado por decisión automatizada** (sin requerir dato personal identificable) | Aviso de que el precio fue personalizado. **Sin obligación de revelar parámetros** |
| APAC (China) | Discriminación de precio **basada en dato, no divulgada**; y paridad impuesta por algoritmo | Ausencia de la conducta, demostrable; no hay texto obligatorio |
| LATAM | — (sin norma) | — (proyectos: transparencia algorítmica y tipificación de colusión por algoritmo) |

Los disparadores **no son intercambiables**, y ahí está el error de diseño que hay que evitar: una
OTA europea que personaliza por segmento de dispositivo sin tocar dato identificable dispara la CRD
y **no** dispara Nueva York; una cadena que personaliza por historial de estadías dispara las dos,
con dos textos distintos; un operador en China puede no deber ningún aviso y deber, en cambio,
**probar que no discriminó por frecuencia de cliente**. Un *flag* booleano global de «mostrar aviso
de precio» es incorrecto en las cuatro. Receta 30.

Y hay una quinta dimensión que ninguna de las cuatro regiones comparte, que es **la línea de
producto**: la Airline Deregulation Act (49 U.S.C. § 41713) impide a los estados de EE. UU. legislar
sobre precios de aerolíneas, *Morales* anuló el uso de estatutos estatales de consumo sobre
publicidad de tarifas, y el propio DOT afirmó en julio de 2026 que los estados ya están *preempted*
en ese terreno. **Ninguna fuente que alcancé aplica eso a § 349-a en particular** —la inferencia va
marcada como tal en el mapa de mercado—, pero la consecuencia de arquitectura no depende de quién
gane el litigio: **el interruptor de divulgación es por producto, no por estado.** Receta 29.

## 41. El primer plano donde la pieza cara ya está resuelta y lo que falta es un campo

En los diez planos anteriores de esta KB la conclusión fue siempre alguna variante de *falta el
motor*: no hay calculadora de emisiones usable comercialmente, no hay detector de reseña falsa, no
hay biblioteca de revenue management más allá de 2 estrellas, no hay cliente del estándar abierto.
**El plano del comprobante rompe la serie.** El motor existe, es grande, es permisivo y está vivo:
`wmixvideo/nfe` (770★, Apache-2.0, push 2026-11-23), `ZUGFeRD/mustangproject` (497★, Apache-2.0,
push 2026-11-23), `phax/phive-rules` (55★, Apache-2.0, push 2026-11-23).

Lo que falta es **un campo**: la identidad fiscal del comprador —VAT ID, RFC, CUIT, GSTIN, NIF—
pasada **en el momento de la reserva**. La regla operativa, coincidente en toda la cobertura de
viaje corporativo de 2026: si ese dato no llega al hotel con la reserva, el hotel emite recibo de
consumidor y el IVA de esa estadía **no se recupera nunca**.

Es el modo de falla más barato de arreglar y el más caro de ignorar de los once planos, y es
**estructuralmente agentic**: el daño no lo causa una alucinación ni un error de ejecución. Lo causa
**una reserva correcta a la que le falta un campo**. Es el primer plano donde el agente rompe algo
ejecutando bien.

## 42. En este plano el error de licencia de la API tiene una sola dirección, y es la inversa de la octava pasada

La tendencia 34 de esta KB registró que *«el error de licencia tiene dos direcciones»*, con el caso
del badge que **afirma** una licencia inexistente. En el plano del comprobante la dirección fue
**una sola y fue la contraria, cinco veces de cinco**:

| Repo | Campo `license` de la API | Archivo leído | Causa medida |
| --- | --- | --- | --- |
| `phax/phive-rules` (55★) | `NOASSERTION` | Apache-2.0 | Encabezado `====` + copyright antes del nombre |
| `Quittio/quittio` (47★) | `NOASSERTION` | MIT | Está en `master`; **404 en `main`** |
| `TadaSoftware/PyNFe` (599★) | `NOASSERTION` | LGPL-3.0 | Texto sin encabezado SPDX |
| `BrasilNFe/brasilnfe-mcp` | `NOASSERTION` | MIT | Está en `master` |
| `DoubleH10/zatca-mcp` (5★) | `NOASSERTION` | Apache-2.0 | Texto sin encabezado SPDX |

**Sobredeclaraciones: cero.** Filtrar por el campo de la API en este plano habría descartado cinco
repos usables, cuatro de ellos permisivos, uno con 599 estrellas. La causa raíz es mecánica y vale
como regla para cualquier curaduría de este KB: **el detector de licencias de GitHub falla cuando
el archivo vive en `master` en lugar de `main`, o cuando el texto arranca con una línea de
encabezado antes del nombre de la licencia.** La licencia se lee del archivo, en las dos ramas,
siempre.

## 43. Un archivo de licencia puede contener tres licencias, y la restrictiva es la de la dependencia

`InvoicePlane/InvoicePlane` tiene **3.289 estrellas** y es la plataforma de facturación open source
más estrellada que devuelve cualquier búsqueda. Su `LICENSE.txt` contiene, en este orden:

1. una **restricción de marca** que prohíbe redistribuir la aplicación bajo el nombre y el logo;
2. **MIT**, para el código de InvoicePlane;
3. **la licencia propietaria de CodeIgniter de EllisLab Inc.**, redactada como *«legal agreement
   between you and EllisLab Inc.»*, para el framework que viene empaquetado en el repo.

**Decir «InvoicePlane es MIT» es media verdad**, y la media que falta es la del framework que el
repo distribuye. Es un cuarto modo de trampa de licencia, distinto de los tres que esta KB ya tenía
catalogados —badge que miente (octava pasada), archivo ausente (décima), API que subdeclara
(tendencia 42)—: **un archivo de licencia correcto que incluye la licencia restrictiva de una
dependencia empaquetada.** La regla que se deduce: en un repo que empaqueta su framework, leer el
`LICENSE` **completo**, no las primeras líneas.

## 44. LATAM tiene el código por primera vez en once planos, y la causa es que obliga desde 2008

La tendencia 9 de esta KB dice *«Asia tiene el código; Europa tiene la regulación; LATAM tiene al
Estado comprando»*. **El plano del comprobante la invierte.** El repo horizontal fiscal más
estrellado del plano es brasileño y Apache-2.0 (`wmixvideo/nfe`, 770★), y la capa NF-e de Brasil
—770 + 599 + 376 + 330 estrellas entre `nfe`, `PyNFe`, `OCA/l10n-brazil` y `nfewizard-io`— **supera
a la capa fiscal europea de este plano, incluidos los artefactos oficiales de la Comisión (271★)**.

La causa no es talento ni inversión: es **antigüedad del mandato**. Brasil obliga a emitir NF-e
desde 2008; Europa empezó a obligar en 2024–2026. LATAM tuvo dieciocho años para construir lo que
EMEA está construyendo ahora. Y eso produce el único argumento comercial de esta KB que va **de
LATAM hacia afuera**: un equipo que ya resolvió *clearance* en tiempo real contra una autoridad
fiscal brasileña es el que mejor implementa KSeF polaco, Verifactu español o InvoiceNow
singapurense. **Los esquemas cambian; el problema es el mismo que Brasil resuelve desde 2008.**

⚠️ **La brecha interna de la región, medida:** Brasil 376★ en Odoo contra México 20★, y
`cfdi sat facturacion` devuelve **33 repos en total**, cuatro de los ocho primeros por estrellas
**sin archivo de licencia**. Brasil tiene ecosistema; México tiene piezas.

## 45. Un solo viaje de negocios produce dos regímenes documentales, y ninguna herramienta abierta lo modela

Según guía de un proveedor de viaje corporativo (⚠️ secundaria, no del BMF): en Alemania **la
factura de hotel entra plenamente al mandato de e-invoicing y el pasaje de avión y de tren están
exentos**. Un viaje de tres días a Múnich genera, entonces, un documento estructurado obligatorio
por el alojamiento y un documento exento por el transporte — dos regímenes, un mismo viaje, un mismo
centro de costo.

El equivalente en India va por el comprador y no por el tipo de servicio: la reserva corporativa
B2B y la factura de banquetes a una empresa llevan e-invoice con IRN, y **la cuenta B2C del huésped
particular no**. El mismo hotel, el mismo día, emite dos tipos de documento según quién compra — y
**el agente que reserva es quien decide cuál sale**, porque es quien pasa o no pasa el GSTIN.

Ninguna de las piezas open source catalogadas en este plano modela la asimetría. Los doce MCP de
`cmendezs` emiten **por jurisdicción**; ninguno razona sobre **qué línea del itinerario entra al
mandato y cuál no**. Es la misma forma del hallazgo de la Receta 27 (un evento de custodia, cuatro
obligaciones regionales) aplicada al comprobante, y está sin construir.

## 46. La licencia viaja peor cuando el formato de distribución es un *skill*

`causa-prima-ai` publica tres repos que se describen como *«free, AI-native EN 16931-compliant
e-invoicing»*. Los tres archivos `LICENSE` —leídos el 2026-11-23— dicen **«All rights reserved…
proprietary and confidential. No license is granted to use, copy, modify, or distribute»**.

El tercero es [`scribo-skill`](https://github.com/causa-prima-ai/scribo-skill) (7★): **un skill de
Claude/Codex**. Y ahí está la tendencia, que ya había asomado en la séptima pasada de esta KB
—*«el inventario empieza a distribuirse como skill, no como API»*— y que acá muestra su costado
sucio: **un skill es el formato que se copia a un agente sin que nadie abra el archivo de
licencia.** Un repo de biblioteca pasa por un gestor de dependencias y por una revisión de SBOM; un
skill se arrastra a una carpeta. El vector de distribución nuevo del vertical **no tiene el control
de licencia que el viejo sí tenía**.

**Regla para esta KB y para cualquier engagement:** un skill se audita como una dependencia —
licencia leída del archivo, no de la descripción — **antes** de copiarlo.

## 47. El primer plano donde el acto regulado es *hablar*, no *ejecutar*

Once planos midieron fallas por omisión: un campo que no se pasó (comprobante), una categoría que
no existe (precio), un vocabulario sin licencia (accesibilidad). El seguro invierte el eje: **el
agente falla cuando contesta bien.**

- **EE. UU.:** describir una cobertura, **recomendar** un límite y **comparar o interpretar
  coberturas** figuran entre las actividades de *solicitation* que exigen licencia según el
  estatuto de Florida *(fuente secundaria: blog de proveedor citando el estatuto — **[sin
  verificar]**)*. La licencia **se adhiere al acto, no a la herramienta**.
- **UE:** EIOPA preguntó en septiembre de 2026 (artículo vinculado a Eurofi) si un chatbot que
  recolecta datos, **filtra productos o da recomendaciones** realiza **distribución de seguros**
  bajo la IDD. Pregunta abierta de la autoridad, **no norma**.

Consecuencia que cambia el alcance de todo concierge ya desplegado: el asistente hotelero que
responde «¿esto me lo cubre el seguro?» cruzó un límite regulatorio **sin cobrar, sin bindear y sin
tocar un pago**. En los planos de pago y comprobante el corte estaba en la transacción. Acá **el
corte está en la frase**.

## 48. La capa agentic del vertical nació en catorce semanas, y ya trae la baranda puesta

Los seis repos agentic de seguro de viaje que existen en GitHub fueron **creados entre el
2026-08-22 y el 2026-11-08**; ninguno pasa de **2★** (el de 4★ es un DApp). Es la capa vertical más
joven que esta KB midió en doce planos.

Y **cuatro de los seis traen el límite escrito en el propio README**, sin norma que los obligue:

- `voyara` (MIT): «a reference build showing how an insurer can let AI agents **quote a policy
  without letting them buy one**».
- `10life`: «**Premiums and scores are indicative. The product page is the authority**», prohíbe PII
  en el parámetro de razón de llamada, máximo 5 planes por respuesta.
- `tourclaim` (MIT): «the card's benefit administrator, **who decides coverage**», y declara que en
  *review mode* crea reclamos **sintéticos**.
- `HelloSafe`: un solo tool, `get_quote`. **No existe tool de compra.**

**La inversión temporal es el hallazgo.** En el plano de la reseña la obligación llegó y la
herramienta no. En el del comprobante la obligación llegó y faltaba un campo. Acá **la herramienta
llegó primero y se autolimitó antes de que el regulador terminara la frase**. Es la primera
evidencia en esta KB de una industria que escribe su propio corte sin que se lo pidan — y la razón
es económica, no ética: quien cruza el límite pierde la licencia, no una multa.

## 49. Es el primer plano donde lo vertical está mejor licenciado que lo horizontal

La ley estructural de esta KB —«lo permisivo es la infraestructura, el copyleft es la plataforma»—
se da vuelta:

| Capa | Licencias medidas | Estado |
|---|---|---|
| **Vertical de viaje** | **MIT** los cuatro usables (`voyara`, `tourclaim`, `Overdoo`, `byteball`) | 4★ **en total entre los cuatro**; uno dormido desde 2022 |
| **Horizontal cercana al problema** | **LGPL-3.0** (`openl-tablets`, 215★) y **AGPL v3** (`openimis`, 86 forks) | Las dos con push de esta semana |
| **Horizontal permisiva y viva** | **BSD-3-Clause** (`OasisLMF`, `OasisPlatform`, push 2026-11-28) | Permisiva de verdad — **y es modelado de catástrofes: no sabe qué es un vuelo demorado** |
| **Horizontal permisiva y cercana** | MIT (`aspire`), Apache-2.0 (`CalculusPrime`) | **Push de 2021 y 2019.** Muertas |

El precio de la inversión es la madurez: **lo permisivo y vivo está lejos del problema; lo cercano
al problema está copyleft o dormido.** La decisión de licencia en este plano hay que tomarla
*antes* de elegir arquitectura, porque AGPL obliga a correr `openimis` como servicio separado y eso
es una decisión de topología, no de legal.

## 50. `NOASSERTION` va para los dos lados — corrección a la tendencia 42

La undécima pasada midió cinco casos de `NOASSERTION` en los que el archivo tenía una licencia
**real y permisiva**, cero casos inversos, y concluyó que la API **sub**declara. Esta pasada
encontró el inverso: `sepehr071/iran-insurance-mcp` devuelve `NOASSERTION` y su archivo dice
**«Free for personal and non-commercial use… Commercial use…»** — no es open source, y la API no lo
advierte en ninguna dirección.

**La tendencia 42 queda corregida, no borrada:** el campo de licencia de la API no tiene un sesgo
estable. `NOASSERTION` significa **«abrí el archivo»**, y nada más. Y un `MIT` correcto en la API
tampoco cierra el tema: `luciano-coelho/opin-doctor-ppgcc-ufsc` es MIT de verdad y su línea de
copyright nombra a **«Open Insurance Brasil»**, una entidad que no es quien publica el repo —
**cuarto modo de trampa de licencia** de esta KB, después del badge que miente, el archivo ausente
y las tres licencias en un archivo.

## 51. El mismo vuelo demorado dispara dos derechos, y ninguna pieza abierta impide cobrarlo dos veces

Un vuelo que aterriza tarde activa simultáneamente:

1. **La compensación del transportista** (EU261 en la UE, UK261 en el Reino Unido): suma **fija por
   distancia**, obligación legal, independiente del gasto real.
2. **El pago del seguro**: **indemnizatorio**, reembolsa gasto real acreditado.

El principio que los separa es el **indemnizatorio**: no se recupera dos veces la misma pérdida. En
la práctica, el asegurado debe **declarar lo ya recibido** y algunas pólizas traen cláusulas de
coordinación de beneficios *(fuentes secundarias: guías y foros del sector — **[sin verificar]**
contra condicionados; no se leyó ningún condicionado completo)*.

**Lo medido en código:** los seis repos de los dos tramos —`hermes-plugin-delayclaim` (MIT, 7★,
creado hace 18 días), `eu261-claim` (AGPL-3.0), `airtruth` (sin licencia), `Overdoo`, `tourclaim`,
`voyara`— **no implementan ninguno el principio indemnizatorio.** Un agente que reclame las dos vías
por el mismo gasto **expone al viajero a una declaración falsa**, y lo hace ejecutando
correctamente las dos tareas por separado. Es el mismo modo de falla que la identidad fiscal del
plano anterior: **el agente destruye el derecho cumpliendo bien su instrucción.** Receta 36.

## 52. Las cuatro regiones regulan el mismo acto y ninguna regula el mismo tramo del acto

Primer eje de esta KB donde las cuatro regiones tienen norma **viva y aplicable a un agente**, y
donde cada una la puso en un lugar distinto de la conversación:

| Región | Dónde pusieron la norma | Artefacto fechado |
|---|---|---|
| **North America** | En **quién puede hablar**: licencia de productor, con la figura del *limited lines travel insurance producer* y el minorista de viaje exento si sólo «ofrece y disemina» | NAIC Travel Insurance Model Act #632 (adoptado 12-2018), **38 estados con la ley promulgada a abril de 2026** (NAIC) |
| **EMEA** | En **qué cuenta como distribuir**, y en **a quién derivar cuando se dice no** | Opinion de EIOPA sobre gobernanza de AI **EIOPA-BoS-25-360, 6-8-2025** (no vinculante, sin requisitos nuevos, revisión prevista ~8-2027); encuesta de GenAI de EIOPA del **2-2-2026** (347 entidades, 25 países); regla de *signposting* de la FCA desde **4-2021**, con cambios de CP24/26 **vigentes 1-1-2026** |
| **APAC** | En **la mecánica de la venta**, con el detalle más agresivo del mundo para un flujo agentic | Circular de IRDAI vigente desde el **1-10-2019**: **prohibida la preselección** de la cobertura en portales y apps, obligatorio el *opt-out* **antes de concluir la transacción**, y nombre de aseguradora + prima + impuesto visibles. Para domésticos, prima no cobrable con más de **90 días** de anticipación |
| **LATAM** | En **el contrato**, con la primera ley integral de contrato de seguro de la región | **Lei 15.040/2024** de Brasil (Marco Legal dos Seguros): acceso del asegurado a los documentos usados en la regulación del siniestro y plazos objetivos. **Vigencia en conflicto entre fuentes: 11-12-2025 (jurídicas, art. 134) vs 10-12-2024 (Agência Câmara, aparente error)** |

**Lo que esto significa para un diseño único.** Un mismo agente de viaje no puede tener una sola
política de seguro: en India el obstáculo es **la UI** (no tildar nada por defecto, mostrar tres
datos), en EE. UU. es **el verbo** (no recomendar ni comparar), en el Reino Unido es **la salida**
(derivar al directorio), y en Brasil es **la prueba** (qué documentos tiene derecho a ver el
asegurado). Las cuatro son satisfacibles a la vez, y ninguna se satisface sola. Receta 35.

## 53. El esquema le pasó por encima al conector: el campo existe y el validador no

**La tendencia que define el decimotercer plano, y es nueva en las trece pasadas.** En los doce
planos anteriores el patrón era *la obligación existe y no hay ni modelo ni código*. Acá el modelo
**sí existe, y es bueno**: el número de registro de una unidad de alojamiento tiene campo tipado en
los dos protocolos abiertos de STR. OpenSTR define `local_registration_number` y pone en el **emisor
de la credencial** el deber de verificar vigencia y validez antes de emitirla, nombrando Chicago,
Edimburgo, Barcelona, Ámsterdam, París y Nueva York. VRP lo tipifica como atestación de primera
clase `VRPRegulatoryRegistration`, con `evidence` ∈ {`self_declared`, `registry_verified`,
`state_attested`}, **`disclaimer` obligatorio si es autodeclarado** y **`verifiedAt` obligatorio si
es verificado contra registro**.

Y **cero** conectores abiertos a cualquier registro, en ocho búsquedas distintas. Consecuencia
directa y verificable: **toda implementación abierta que existe hoy sólo puede emitir honestamente
`self_declared` + `disclaimer`**. El nivel que el regulador exige está especificado por el protocolo
y **no implementado por nadie en ninguna región**.

## 54. Un plazo legal coordina voluntarios de estándares, no voluntarios de integración

**Corrección y refinamiento de la ley estructural que propuso la pasada de retail del 2026-11-28**
(«un plazo legal cercano produce herramientas open source más rápido que una oportunidad de
margen»). Este plano es el caso de control que esa ley necesitaba: acá **los plazos ya pasaron** —UE
aplicable desde el **2026-05-20**, CIN italiano plenamente obligatorio desde el **2025-01-01**,
Nueva York bloqueando pagos de listados no registrados desde el **2023-09-05**, entre seis meses y
más de tres años de plazo transcurrido— y la capa de cumplimiento **sigue en ocho ceros**. Lo que
los plazos produjeron fue **el esquema**: los dos protocolos son de 2026.

**La razón, y es la parte generalizable a las once industrias restantes:** un esquema se escribe una
vez y vale en toda jurisdicción; **un conector a un registro es por jurisdicción**, exige
credenciales que un voluntario no tiene, **no se puede probar sin una propiedad realmente
registrada**, y no da prestigio. El plazo mueve la capa que un voluntario puede terminar solo.

**PREDICCIÓN FALSABLE, para que la verifique la próxima pasada de travel:** el enum `evidence` de
VRP **seguirá sin implementación abierta de `registry_verified`**, y si aparece una, **vendrá de una
autoridad nacional o municipal publicando una API, no de un voluntario**. **Si antes de la próxima
pasada aparece un conector a cualquiera de los registros de UE / Italia / Nueva York / NSW / CDMX
construido por un voluntario, esta tendencia está mal y hay que tacharla.**

## 55. El registro es la pieza frágil y el caño de transmisión es la pieza durable

**La lección de arquitectura del plano, y salió de un hecho judicial.** El Tribunal Supremo español
**anuló el Registro Único de Arrendamientos** creado por el RD 1312/2024 (Sentencia 620/2026; ⚠️ la
fecha se cita como 19, 21 o 22 de mayo de 2026 según la fuente, y **no se resuelve**). Pero **lo que
sobrevivió** fue la **Ventanilla Única Digital**, el **deber de transmisión de datos de las
plataformas** y el intercambio con fines estadísticos. Sólo cayó el registro.

Y el propio Reglamento (UE) 2024/1028 está construido igual: es un **marco de intercambio de
datos**, con el registro **condicionado** a que el Estado miembro monte el procedimiento.

**Regla de diseño que se desprende, y aplica a cualquier plano regulatorio de cualquier industria:**
**anclar la hoja de ruta en la obligación de transmisión, no en la integración del registro.** Una
propuesta que decía «integramos el registro nacional español» quedó sin objeto en mayo de 2026; una
que decía «emitimos la transmisión mensual de actividad» siguió siendo válida el mismo día. El caño
sobrevive a la base de datos.

## 56. Una licencia puede tener el nombre correcto y el cuerpo dañado — segunda corrección a la tendencia 42

**Y obliga a corregir la regla que esta red de KBs viene afinando desde el ciclo 8.** La regla era:
*la licencia se lee del archivo, nunca del badge ni de la API*, y la pasada de retail la cuantificó
(`NOASSERTION` resultó equivocado en 4 de 5 casos). **Este plano encontró el caso donde leer el
archivo produce un falso positivo.**

El `LICENSE` de [`openstr-protocol/protocol`](https://github.com/openstr-protocol/protocol) tiene
9.761 B, abre con «Apache License, Version 2.0» y el README luce un badge de Apache-2.0. Pero
**difiere del texto canónico en 12 bloques**, **le falta el APPENDIX completo**, y la definición de
`"Contribution"` **perdió su sujeto**: dice *«“Contribution” shall mean, as submitted to the
Licensor for inclusion in the Work…»*, sin el *«any work of authorship, including the original
version of the Work and any modifications or additions to that Work or Derivative Works thereof»*
del original. No es una edición legal deliberada: es un texto **parafraseado con pérdida**.

**La consecuencia es real:** el **§5 de Apache-2.0** —la concesión entrante del contribuyente, que
es una de las razones por las que una empresa elige Apache-2.0— **se apoya en esa definición**, que
acá no define nada. Quien contribuya aguas arriba no tiene concesión clara.

**Y el giro:** la API de GitHub reporta `NOASSERTION` para este repo, y **probablemente acierta** —
su detector rechazó el texto porque el texto no coincide. **Primer caso en esta red de KBs donde
`NOASSERTION` es la lectura correcta.**

**La regla queda así, para las doce industrias:** leer la licencia del archivo **y además
compararla contra el texto canónico**. Un archivo puede tener el nombre bien y el cuerpo mal. Y
cuando el diff no es trivial, **es revisión legal, no una celda de tabla**.

## 57. La frontera entre la capa sana y la capa inexistente es la línea donde empieza la obligación legal

**El corte más nítido medido en esta KB.** La misma unidad de alojamiento, dos capas:

- **Operarla**: `Qloapps/QloApps` 14.525★ OSL-3.0, `open-condo-software/condo` 437★ **MIT con commit
  de hoy**, `senatroxx/OpenKos` 130★ Apache-2.0, `Kamra-PMS/kamra-pms` 116★ **Apache-2.0 con commit
  de hoy**, `Gribadan/RentTools.io` 34★ **MIT con commit de hoy**. **Tres repos con commit del día
  en la rama default, dos de ellos permisivos.**
- **Cumplir con su registro**: **ocho búsquedas en cero.**

No es una diferencia de madurez ni de dinero ni de dificultad técnica —validar un número contra una
API es más fácil que escribir un PMS—. **Es que la primera capa le sirve a quien escribe el código y
la segunda le sirve a un regulador.** Esto generaliza la regla de la pasada de retail («donde hay un
dataset abierto de referencia esperá una capa agentic usable, y donde no, presupuestá construir la
capa de datos primero») con un caso donde **ni el dataset ni la capa existen porque el beneficiario
no es el autor**.

## 58. En LATAM la autorización que decide la legalidad no es estatal, y ningún protocolo la modela

**El hallazgo regional que rompe el modelo de datos de los dos protocolos.** En EMEA y APAC el
artefacto que vuelve lícita una unidad es **un número emitido por el Estado**. En LATAM, en dos de
las tres jurisdicciones medidas, es **una autorización privada**: en Brasil el STJ decidió el
**2026-05-07** (5-4, **REsp 2.121.055**) que el alquiler de corta temporada en condominio
residencial **requiere asamblea con dos tercios** de los condóminos; en CABA el **reglamento de
copropiedad puede prohibirlo** y vincula a todos los propietarios.

**Eso no está en ningún registro público.** Un listado de CABA puede estar **registrado ante el Ente
de Turismo y ser igualmente ilícito**. De modo que `evidence: registry_verified` —el nivel más alto
que un implementador puede aspirar a emitir— **es insuficiente en LATAM por diseño**, no por falta
de datos. Es la misma clase de defecto semántico que la pasada undécima halló en el comprobante
fiscal: **el agente ejecuta correctamente y destruye el resultado**.

**Oportunidad concreta:** el campo que falta es una atestación de **autorización del consorcio o
condominio**, que no existe en VRP ni en OpenSTR. VRP es **CC0-1.0** y declara su `jurisdiction`
explícitamente *«jurisdiction-neutral: never constrained to any specific country»* — es decir,
**está diseñado para recibir esa extensión y no hay que pedir permiso para proponerla**.
