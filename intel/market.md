---
industry: travel
region: Global
updated: 2026-11-28
---

# 🗺️ Mapa de mercado — Travel & Hospitality

> Key players, oportunidades y posicionamiento. Investigado globalmente y luego una vez por
> región el 2026-11-21.
> **Convención de evidencia:** cada cifra lleva su fuente. Lo que solo aparece en blogs de
> proveedor se marca **[sin verificar]** en lugar de presentarse como dato. Ciclos anteriores
> de esta KB citaron cifras de proveedor como hechos establecidos; eso se corrige aquí.
>
> **Límite del entorno de ingesta, declarado (2026-11-23):** los dominios oficiales de la UE
> (`travel-europe.europa.eu`, `home-affairs.ec.europa.eu`) **no son alcanzables desde este
> entorno** por política de red. Todo lo que sigue sobre EES y ETIAS es de **fuente
> secundaria** y está marcado como tal. **Antes de comprometer una fecha de EES o ETIAS con
> un cliente hay que confirmarla contra el sitio oficial.** Se deja escrito en lugar de
> omitirlo: un límite declarado es información; el silencio parece cobertura.

## El hecho que ordena todo el vertical

**El viajero planifica con AI y no compra con AI.** Phocuswright (conferencia 2026) mide que
**52% de los viajeros de EE.UU. usan AI para planificar, y solo 2% reserva a través de ella**
— ~8% si se cuenta Google AI Mode. Un artículo de prensa especializada cita que **solo 8% de
los viajeros confía en que la AI complete una reserva**. La brecha planificación→compra es la
estructura del mercado, no una fase pasajera.

Consecuencia directa para un engagement: el valor vendible hoy está **antes** del pago
(inspiración, armado, verificación, reacomodo) y **después** del pago (servicing, disrupción,
rebooking). El pago mismo es territorio del merchant of record, y las aerolíneas lo están
defendiendo deliberadamente.

## Players globales

| Empresa | Tipo | Fortaleza | Debilidad |
|---------|------|-----------|-----------|
| Booking Holdings / Booking.com | OTA | Escala de inventario; socio de lanzamiento de Google AI Mode y adoptante de MCP | Si el agente se vuelve la puerta de entrada, la OTA pasa a ser un proveedor de inventario sin marca |
| Expedia Group | OTA | Investigación propia de adopción por región; socio de Google AI Mode | Sus propias encuestas son las que documentan la brecha de confianza que la amenaza |
| Airbnb | Alojamiento alternativo | Inventario no hotelero difícil de replicar | Sin historia agentic pública comparable a la de los GDS |
| Sabre | GDS | **MCP server con ~80 clientes travel** (Virgin Australia, Flight Centre, Internova), algunos corriendo dentro de ChatGPT y Claude *(fuente secundaria, sept-2026)* | Modelo de negocio atado a la intermediación que el agente puede saltear |
| Travelport | GDS | **12-nov-2026: compra de vuelo completada por AI end-to-end** con Booked AI vía NDC sobre TripServices, **con la aerolínea como merchant of record**. Plataforma construida sobre MCP (jul-2026) | El tercero de los tres GDS en escala |
| Amadeus | GDS | Integra NDC y ONE Order para comercio agentic; adoptante de MCP | Su SDK Python open source está **archivado** desde 2025 — la vía open source está cerrada |
| Google | Buscador / distribución | AI Mode con reserva de hotel y vuelo; socios Booking.com, Expedia, Marriott, IHG, Wyndham | Declaró "**no intention of becoming an OTA**" y **no es merchant of record**: cede la transacción |
| OpenAI | Asistente | ChatGPT **superó a Google por 13 puntos** en visitas a páginas de reserva de travel en APAC (Criteo, marzo 2026) | **Dio marcha atrás con la reserva directa en ChatGPT en marzo 2026** |
| Aerolíneas (ej. United) | Proveedor | Control del inventario y del cobro | Postura explícita: AI para investigación e inspiración, **intervención humana en la compra** |
| IATA | Organismo de estándares | NDC + ONE Order son la base de oferta y orden | **No ha emitido ningún estándar agentic.** MCP y UCP los construyen proveedores, sin aval de IATA |

#### Dónde está realmente el estándar

- **IATA: NDC (XML, framework EASD) + ONE Order.** Base de oferta/orden, pago, servicing,
  cancelación y reembolso. Es lo que un agente necesita para transaccionar de verdad.
- **MCP:** donado por Anthropic a la **Agentic AI Foundation (Linux Foundation) en dic-2025**.
  Es la capa de acceso que están adoptando Sabre, Travelport, Amadeus, Booking.com, Expedia y
  Turkish Airlines.
- **La lectura práctica:** NDC gobierna la oferta, el agente gobierna cómo el software la
  alcanza. Son complementarios, no competidores. Ciclos anteriores de esta KB registraron
  "NDC 24.2 obligatorio": **eso es falso** — NDC es voluntario y su adopción es desigual
  (Lufthansa Group reporta >50% de ventas de agencia vía NDC, pero solo de su propio negocio
  de agencia).

## Tamaño de mercado — con la cautela que corresponde

| Cifra | Fuente | Confianza |
|-------|--------|-----------|
| GenAI es la **prioridad #1 de inversión tecnológica** a 12-18 meses para empresas de travel | Phocuswright, vía prensa especializada | Alta — encuesta de la industria |
| 52% planifica con AI / 2% reserva con AI (EE.UU.) | Phocuswright 2026 | Alta |
| 49% de los pasajeros usó AI para planificar un viaje | IATA Global Passenger Survey 2026 | Alta — primaria de IATA |
| AI en travel: ~USD 2.1B → ~12.1B a 2034 (CAGR ~22,5%) | reportes de market research | **[sin verificar]** — ningún informe primario localizado; los ciclos 5/6/8 de esta KB la citaron como hecho |
| OTA: USD ~561B (2026) → ~1.3T (2033) | reportes de market research | **[sin verificar]** — las cifras varían entre informes |
| LATAM travel USD 109B → 196,6B | nota de ciclos previos de esta KB | **[sin verificar]** — sin fuente localizable |

**Viaje accesible — séptima pasada.** Las cifras divergen **más de 10×** por
alcance: Mordor Intelligence estima el mercado de viaje accesible y asistido en
**78.740 M USD (2026)**, mientras un panel de ATTA cita **>1 billón USD (2025)**
contando a todos los viajeros mayores. **Para material de cliente usar Open
Doors / Harris (~50.000 M USD/año, sólo EE.UU., sólo viajeros con
discapacidad)** y decir el alcance. La cifra de 17.300 M que todavía circula es
de 2015.


### El costo del equipaje, la cifra que ordena el noveno plano (2026-11-23)

Informe **SITA Baggage IT Insights 2026** (datos de 2025). ⚠️ **El PDF del primario no se pudo
abrir desde esta red** (`media.asianaviation.com` no resuelve): todas estas cifras son
**secundarias coincidentes** entre varias fuentes, no leídas del informe.

| Métrica | Valor 2025 | Nota |
|---------|-----------|------|
| Tasa global de equipaje mal manejado | **4,9 por 1.000 pasajeros** | **Baja del 23%** interanual, por debajo de prepandemia |
| Volumen total | **24 millones de piezas** | Baja del 19%, sobre un récord de ~5.000 millones de pasajeros |
| Costo promedio por pieza | **USD 260** | Nuevo *benchmark* de SITA |
| Costo anual de la industria | **USD 6.300 millones** | SITA: *cinco piezas mal manejadas borran la ganancia de un vuelo entero* |
| Doméstico vs internacional | **1,65** vs **9,12** por mil | El riesgo se multiplica por 5,5 al cruzar una frontera — el tramo con transferencia |
| Perdida vs demorada | Una perdida cuesta **2,6×** una demorada | Pero la demorada es la frecuente |

> ⚠️ **Discrepancia abierta, registrada y no resuelta.** Una fuente describe una tasa de **3,4 por
> mil con un alza del 9%**, que contradice el 4,9 con baja del 23% de todas las demás. Lo más
> probable es que sea **la cifra de APAC (3,41) leída como global**, pero no se pudo confirmar.
> **Se registran las dos y no se afirma ninguna.**

**Por qué esta cifra ordena el plano:** USD 260 por pieza es lo que un operador paga por **no
tener el registro**. Es el único plano de esta KB donde el valor de la custodia está publicado en
dólares por evento, y por eso es el plano donde un caso de negocio no necesita estimarse.
### El precio, la cifra que ordena el décimo plano (2026-11-23)

No hay una «cifra de mercado del precio»: el precio no es un segmento, es la función que decide el
ingreso de todos los segmentos ya listados arriba. Lo que sí se puede medir, y es lo que ordena el
plano, es **la distancia entre lo que la industria despliega y lo que el código abierto ofrece**:

| Medida | Valor | Cómo se midió |
| --- | --- | --- |
| Repos de *revenue management* específicos de viajes encontrados | **8** | `search/repositories` sobre EMSR, yield y revenue management, más el topic de GitHub |
| De esos 8, **sin archivo de licencia** (inusables) | **5** | `curl` de LICENSE/LICENSE.md/LICENSE.txt/COPYING en `main` y `master` |
| Estrellas de la única biblioteca de RM real y permisiva (`revmng`, MIT) | **2** | `search/repositories`, 2026-11-23 |
| Estrellas de la capa horizontal que sí sirve (`or-tools` Apache-2.0) | **14.433** | ídem |
| Repos de *divulgación* de precio algorítmico | **1, y no es del tema** | `algorithmic pricing disclosure` → `total_count: 1` |
| Repos de explicación/transparencia de precio | **0** | `price explanation transparency algorithm` → `total_count: 0` |
| Aerolíneas de EE. UU. con pedido de explicación del Congreso | **8** | Cobertura de prensa, plazo reportado 2026-08-25 |
| Multa travel por algoritmos de precio ya aplicada (China, SAMR) | **RMB 5.200 millones** | Secundario coincidente, decisión no leída |

La proporción es el hallazgo: **la industria tiene motores de precio por AI corriendo en producción
en cuatro continentes, y el código abierto del vertical ofrece una biblioteca de 2 estrellas y cero
herramientas de divulgación.** Es la brecha más grande medida en los diez planos de este KB.


### El comprobante, la cifra que ordena el undécimo plano (2026-11-23)

No hay una «cifra de mercado del comprobante»: la factura no es un segmento, es la condición para
que el gasto del viaje corporativo sea recuperable. Lo que se puede medir —y es lo que ordena el
plano— es **cuántas jurisdicciones ya obligan, y qué tan grande es la capa open source que las
cubre frente a la capa específica de viaje**:

| Medida | Valor | Cómo se midió |
| --- | --- | --- |
| Servidores MCP de facturación electrónica por jurisdicción, Apache-2.0 | **12** (de un solo autor) | `user:cmendezs` + lectura de los 12 `LICENSE` |
| De esos 12, con push en los últimos 7 días | **10** | `search/repositories`, 2026-11-23 |
| Estrellas del más estrellado de los 12 | **3** | ídem. **Sin adopción medible: riesgo de autor único** |
| Estrellas del repo horizontal fiscal más grande (`wmixvideo/nfe`, Apache-2.0, **brasileño**) | **770** | ídem, push 2026-11-23 |
| Repos de facturación **específica de viaje** | **2** | `travel agency invoice billing system` |
| De esos 2, usables (licencia + vivos) | **0** | Uno GPL-3.0 con **0★ y último push en 2017**; el otro sin licencia |
| Repos de folio hotelero fiscal | **5, ninguno software con licencia** | `hotel folio invoice` |
| Repos de la red de EE. UU. (DBNAlliance) | **1, de 2023, sin licencia** | `dbnalliance` |
| Repos de cliente Peppol Access Point | **0** | `peppol access point client library` |
| Repos de cálculo de per diem | **0** | `per diem allowance calculator` |
| Veces que la API de GitHub **subdeclaró** la licencia en este plano | **5** | Lectura del archivo en `main` y `master` |
| Veces que la **sobredeclaró** | **0** | ídem |

**Por qué esta cifra ordena el plano:** es el único plano de los once donde **la pieza cara ya está
resuelta y es permisiva**. En los diez anteriores faltaba el motor; acá el motor existe, tiene 770
estrellas, licencia Apache-2.0 y push de hoy. Lo que falta es **un campo**: la identidad fiscal del
comprador, pasada en el momento de la reserva. Y ese campo no existe en ningún agente de reserva
catalogado por esta KB.

**El hecho travel-específico que hace al plano, y es el más accionable de la pasada:** si el número
de IVA del comprador no llega al hotel **en la reserva**, el hotel emite recibo de consumidor y el
IVA de esa estadía **no se recupera nunca**. El agente de reserva es, por lo tanto, el punto donde
se pierde la recuperación — y la pierde ejecutando correctamente.

### El seguro, la cifra que ordena el duodécimo plano (2026-11-28)

**Y la cifra que lo ordena no es el tamaño de mercado.** Las estimaciones del mercado global de
seguro de viaje para 2026 que devolvió esta pasada **no coinciden entre sí**, y todas son informes
pagos con definiciones distintas:

| Fuente | 2026 | Proyección |
|---|---|---|
| IMARC | USD **25,5** mil millones | USD 56,5 mm a 2034 |
| Mordor Intelligence | USD **30,08** mil millones | USD 62,53 mm a 2031 |
| GII Research | USD **31,25** mil millones | USD 53,66 mm a 2032 (CAGR 9,35%) |
| The Business Research Company | USD **35,97** mil millones | CAGR 16,9% |
| Expert Market Research | — | USD 261 mm a 2035 (CAGR 24,5%) — **atípico, descartar** |

**Rango honesto: USD 25–36 mil millones para 2026.** Esta KB no elige un número: la dispersión es de
**más del 40%** entre la cifra más baja y la más alta para el mismo año, lo que indica que las
definiciones de «mercado de seguro de viaje» de cada proveedor no son comparables.

**Lo que no se encontró:** un **ratio de siniestralidad global**. Lo único disponible es por país y
de un solo proveedor: India, siniestralidad incurrida de viaje al exterior **66,35% (2021) → 41,59%
(2023) → 49,45% (2025)**, y doméstico cerca del **11,62%** *(un único vendor de market research —
**[sin verificar]**, no es un benchmark global)*.

**La cifra que sí ordena el plano es regulatoria, no financiera:**

> **38 estados** de EE. UU. con el NAIC Travel Insurance Model Act #632 promulgado (NAIC, abril de
> 2026) · **4 reguladores** con norma viva aplicable a un agente en las cuatro regiones ·
> **0 repositorios** de asistencia en viaje open source en todo GitHub.

Es el primer plano de los doce donde **el presupuesto del cliente lo mueve la licencia y no el
ahorro**: el riesgo no es pagar de más, es **perder la habilitación para distribuir**.

⚠️ **Un dato que circula y no soporta peso:** «casi la mitad de los profesionales de seguros ve al
seguro de viaje como el ramo más listo para automatización end-to-end con AI» (GlobalData). Es una
**encuesta de opinión de 98 respuestas**. Sirve como color, no como evidencia de mercado.

**Brasil, el único dato de prima de la región que se pudo ubicar:** **R$ 965 millones** de primas de
seguro de viaje en 2024 (HelloSafe citando SUSEP vía CNSEG).

## Opportunities by region

### North America

**Evidencia.** 52% planifica con AI, 2% reserva (Phocuswright 2026). **63% de adopción
biométrica, la más alta del mundo**, junto con la preocupación más fuerte por seguridad de
datos (IATA 2026). Las **reglas de visado disuaden al 43% de los viajeros** (IATA 2026).
*[sin verificar]* 45% de los asesores de viaje de NA usan herramientas AI frente a <15% de las
agencias a nivel global (agregador).

*Agregado el 2026-11-23:*
- **La misma casa publica 52% y 56%.** Phocuswright da 52% en los datos de su conferencia 2026
  y **56%** para viajeros activos de EE.UU. en el 1S-2026 (y 39% en el 2S-2025). No es
  contradicción: son ventanas y definiciones distintas. **Citar el rango y la fecha, nunca un
  número suelto** — un cliente que compare dos presentaciones nuestras con cifras distintas
  deja de creernos las dos.
- *[fuente única]* 54% de los viajeros de EE.UU. usa AI para planificar, pero **solo 22% de
  las organizaciones de destino ofrece planificación con AI**. Si se sostiene, es la brecha
  oferta-demanda más explotable de la región, y es el mismo patrón que LATAM ya resolvió por
  el lado de la compra estatal.

**Regulación.** No hay estatuto federal de AI; la obligación vinculante viene de las
legislaturas estatales: **cinco leyes estatales de AI vinculaban a empresas a agosto-2026**,
entre ellas la ley de modelos frontera de California y **TRAIGA en Texas**. Nada específico de
travel: aplica derecho de consumidor, privacidad y seguridad de datos. **Canadá** no tiene
estatuto de AI, pero su ley federal de privacidad y la **Ley 25 de Quebec** ya alcanzan a
cualquier sistema de AI que trate datos personales — que es exactamente lo que hace un flujo
de identidad del viajero. **México** no tiene ley general de AI; hay proyectos en trámite.
Canadá opera además con un marco de confianza y estándares. El **"AI AGENT Act"
del senador Warner, que cubre agentes de cara al consumidor, es un borrador de discusión, no
ley** — se registra así porque un ciclo anterior lo arrastró sin poder verificarlo.

**Oportunidades.**
1. **Servicing y disrupción, no booking.** Es el único lugar donde la brecha de confianza no
   bloquea: reacomodo por clima, recálculo de conexiones, gestión de interrupción. Receta en
   `compose/patterns.md` → Receta 3.
2. **Biometría + agente, con el dato quedándose en casa.** La adopción biométrica más alta
   del mundo convive con la mayor preocupación por datos: el stack self-hosted
   (`headwaymaps/headway`, `komoot/photon`) es un argumento comercial, no un detalle técnico.
3. **Equipar al asesor humano, no reemplazarlo.** Si NA concentra el uso de AI entre asesores,
   el producto es el copiloto del asesor: `borski/travel-hacking-toolkit` (MIT, 1029★) es el
   único activo open source serio de puntos, millas y award flights.
4. **Merchant of record como requisito de arquitectura.** El hito de Travelport funciona
   porque la aerolínea cobra. Cualquier diseño que asuma que el agente cobra choca con la
   postura de las aerolíneas.
5. **Identidad verificada sin pasivo de datos — la oportunidad que une las dos cifras de NA.**
   La región tiene a la vez la adopción biométrica más alta del mundo y la mayor preocupación
   por brechas de datos. No son públicos distintos: es el mismo viajero. El entregable que
   resuelve ambas es **verificar el documento en el dispositivo y no guardarlo**:
   [`AndyQ/NFCPassportReader`](https://github.com/AndyQ/NFCPassportReader) (MIT) para leer el
   chip, [`zkpassport/circuits`](https://github.com/zkpassport/circuits) (Apache-2.0) o
   [`rarimo/passport-zk-circuits`](https://github.com/rarimo/passport-zk-circuits) (MIT) para
   probar el atributo sin revelarlo. Con la Ley 25 de Quebec y las leyes estatales encima,
   "no almacenamos el documento" es defensa legal, no marketing. Receta en
   `compose/patterns.md` → Receta 7.

6. **La disrupción dejó de ser cortesía y pasó a ser obligación con reloj — y esta es la
   región donde eso ya ocurrió.** La regla de reembolso automático del US DOT (vigente desde
   el 2024-10-28 y en vigor durante 2026) fija umbrales operables por software: **3 h de
   retraso en doméstico, 6 h en internacional**, reembolso en **7 días hábiles** si se pagó
   con tarjeta y **20 días corridos** en otras formas de pago, y trata como cancelación el
   vuelo que cambia de número. En marzo de 2026 el DOT propuso sumar los **retrasos de 120
   minutos en pista** al mismo marco. Eso convierte la Receta 3 (servicing y disrupción) en
   un **motor de derechos con fecha de vencimiento**, no en un chatbot de contención: la
   pregunta del cliente deja de ser "¿qué le digo al pasajero?" y pasa a ser "¿cuánto le debo
   y desde cuándo corre el plazo?". **Dos cautelas medidas, no omitidas:** (a) la pausa de
   fiscalización para el caso "misma ruta, otro número de vuelo" figura con fin el
   2026-06-30 y **no se pudo confirmar desde este entorno** si caducó, se extendió o fue
   reemplazada — hay que verificarlo en el Federal Register antes de prometer cobertura de
   ese supuesto; (b) la regla de transparencia de cargos accesorios **fue anulada por el
   Quinto Circuito en pleno el 2026-02-03** y no forma parte de este marco. El cálculo se
   apoya en datos de referencia sin costo de licencia —
   [`davidmegginson/ourairports-data`](https://github.com/davidmegginson/ourairports-data)
   (Unlicense, dominio público) y
   [`mborsetti/airportsdata`](https://github.com/mborsetti/airportsdata) (MIT, husos
   horarios incluidos, que es lo que hace computable un umbral en horas) — **no** sobre
   OpenSky, cuyos términos de dato son no comerciales (ver `repos/foundations.md`). Receta en
   `compose/patterns.md` → Receta 10.


7. **El pago agentic ya ocurrió acá, y conviene saber exactamente qué ocurrió.** El hito es
   **Sabre + PayPal + Mindtrip**: reserva de vuelo dentro del chat, lanzada en 2026
   (*Mindtrip Flights*; la prensa difiere entre el anuncio de febrero/marzo y el lanzamiento
   del 6 de mayo — **citar "2026" y no un día**). Lo que importa no es que "un agente
   reservó": es **cómo se repartió**. Mindtrip conversa, **Sabre** pone inventario, ticketing
   y servicing, y **PayPal** cobra y verifica identidad. **El agente no es el merchant of
   record en ninguna parte del flujo** — es la confirmación comercial de la tendencia 2, y el
   argumento más fuerte que Globant tiene para decirle a un cliente que el entregable honesto
   no incluye cobrar. Se suma el movimiento de distribución: **Marriott integró Google AI Mode
   para reserva directa**, y Google declaró que **no es merchant of record**. North America es
   hoy la **única región con un flujo agentic de punta a punta en producción**, y la pieza que
   falta para construirlo es la capa de mandato, que no existe en abierto (`AP2 mandate
   implementation stars:>=20` → 0). Receta en `compose/patterns.md` → Receta 12.
**Agregado en la cuarta pasada del 2026-11-23 — visibilidad agentic: la región donde el
problema ya tiene dueño y presupuesto.**

- **Google puso en prueba viva la reserva hotelera agentic en EE.UU. en agosto de 2026**
  *[fuente secundaria, cobertura de conferencia]*. Es la región donde el canal agentic deja de
  ser hipótesis: si el motor reserva, **ser citado por el motor es ingreso, no marketing.**
- **El defecto está medido y es mecánico** *[estudio HotelRank 2026 vía prensa de
  hospitality]*: sobre 121.425 home pages de hotel en 7 países, **36,3% sin dato estructurado**,
  **mediana de score 0/100**, y **41,1% de los que emiten JSON-LD usan el tipo equivocado**
  (`Organization`/`LocalBusiness` en vez de `Hotel`/`LodgingBusiness`).
- **La competencia es de proveedor cerrado.** Las herramientas de "AI visibility" para hoteles
  que circulan en NA son productos comerciales. La capa open source equivalente existe y es
  permisiva (`elmohq/elmo` MIT, `yaojingang/GEORank` Apache-2.0), **pero no sabe de travel.**

**Oportunidad, dicha como entregable:** *remediación de schema a escala de portfolio*. No es un
proyecto de AI: es un pipeline que audita N propiedades con `extruct`, detecta el tipo
equivocado, corrige la plantilla del PMS una vez y **mide la variación de citas** con `elmo`.
Se vende con un número de línea de base el día uno —cosa que casi ningún proveedor hace— y es
defendible porque el 41,1% es un error reproducible, no una opinión.

⚠️ **Lo que no hay que prometer en NA:** que publicar `llms.txt` mueve la aguja. La evidencia
disponible dice lo contrario (ver `repos/foundations.md`), y un cliente de esta región
contrasta.

#### Plano terrestre — medido el 2026-11-23

**Evidencia.** North America es la región que **inventó el formato de datos de transporte que
usa todo el mundo** (GTFS, nacido en Portland con TriMet y Google) y **no tiene un solo
servidor MCP de transporte terrestre**. De los ocho medidos globalmente, siete son EMEA y uno
es APAC. Cero aquí.

- El ecosistema de infraestructura sí es norteamericano y es fuerte: `MobilityData` (Montreal)
  mantiene el validador canónico de GTFS (434★, Apache-2.0) y la Mobility Database (354★,
  Apache-2.0); `OneBusAway` (Seattle) es la suite de información al pasajero de grado operador
  (243★, Apache-2.0 por referencia). **La región exporta el estándar de datos y no consume la
  capa agentic que se podría construir encima.**
- Ferrocarril interurbano: no hay API oficial de Amtrak. Lo que existe son cuatro proyectos de
  reingeniería inversa, el mayor con **26 estrellas y sin licencia** (`mgwalker/amtrak-api`,
  sin push desde 2024-07). Uno de ellos se describe literalmente como *"reverse engineer
  amtrak API"*. **No hay base contractual limpia para un entregable de cliente.**
- `interline-io/transitland-lib`, la librería de procesamiento de datos de transporte más usada
  de la región, es **GPL-3.0 con opción comercial de pago** (ver `repos/foundations.md`). Un
  cliente que la adopte sin leer el archivo compra una obligación o una factura.

**Oportunidad:** *la capa agentic sobre el estándar que la región ya mantiene*. El trabajo
construible aquí no es un cliente ferroviario —no hay con qué— sino **un servidor MCP sobre
GTFS + GTFS-Realtime alimentado por la Mobility Database**, que es Apache-2.0 de punta a punta
y no toca un endpoint no autorizado. **Es el único camino del plano terrestre que es a la vez
permisivo, vivo y contractualmente limpio**, y hoy no lo ocupa nadie en esta región.

⚠️ **Lo que no hay que prometer en NA:** reserva o emisión de tren o bus. No existe open source
que lo haga en ninguna región del mundo, y aquí ni siquiera hay API oficial de la que colgarse.



#### Sexta pasada 2026-11-23 — adopción, regulación y el plano de emisiones

**Adopción.** Deloitte (outlook 2026) registra que el uso de IA generativa en
la planificación de viajes **se triplicó entre 2023 y 2025**, con millennials
al frente, mientras la compra y el contenido siguen sin estar conectados. Un
informe de marzo de 2026 difundido por Skift pone a las plataformas de IA
autónomas como las más usadas, con **64% de adopción entre quienes usan IA**, y
la cohorte boomer **duplicada al 27%**. Del lado de la oferta, Google pasó la
reserva agentic de hotel a **testeo en vivo en EE.UU. en agosto de 2026**.

**El techo, que conviene decirle al cliente.** Una encuesta del Oliver Wyman
Forum encontró que **sólo el 7%** de los consumidores dejaría que un asistente
de IA "se encargue de todo" y le notifique el resultado. La delegación total no
es el producto; la delegación con punto de control humano sí.

**Regulación.** El movimiento principal es federal: en **marzo de 2026** la
Casa Blanca publicó recomendaciones legislativas para un marco nacional de IA,
empujando hacia un estándar único en lugar del mosaico estatal. Para un
despliegue multiestado eso reduce fricción, pero todavía es recomendación, no
ley.

**Emisiones — la brecha regional.** Las búsquedas de esta pasada **no
encontraron un mandato federal estadounidense de reporte de emisiones de viaje
equivalente a CSRD**. La obligación que sí alcanza a las aerolíneas de la
región es **CORSIA**, vía ICAO, no vía Washington. Consecuencia práctica: en
Norteamérica el Scope 3 categoría 6 se reporta **por compromiso corporativo
voluntario o por exigencia de cliente/inversor**, no por ley de viajes — lo que
cambia a quién se le vende (sostenibilidad corporativa y finanzas, no
compliance).

⚠️ **Cifra que esta pasada rechaza:** circula un dato de "40% de los viajes de
placer de EE.UU. asistidos por IA" y un PIB de 43.000 M USD atribuido a WTTC,
publicado por un sitio de baja calidad. **No se pudo verificar contra fuente
primaria. No usar en material de cliente.**

#### Séptima pasada 2026-11-23 — plano de accesibilidad

**Regulación.** El US DOT publicó la *Wheelchair Rule* (Federal Register
2024-29731, 17-12-2024; vigente desde el 16-01-2025). La pausa de
cumplimiento sobre **cuatro** de sus disposiciones —incluida la presunción de
violación de la ACAA si se vende un vuelo que no puede llevar la silla del
pasajero, que es la que dispara reembolso— se **extendió del 31-12-2026 al
30-04-2027** (FR 2026-15835), mientras se tramita una *Wheelchair Rule II*.
A4A y varias aerolíneas litigan la regla. ⚠️ **Fuente secundaria:** el sitio
del DOT no resuelve desde esta sesión; verificar la fecha antes de usarla con
cliente.

Además, la ACAA ya exige desde hace una década que el sitio principal de una
aerolínea que vende a consumidores de EE.UU. cumpla **WCAG 2.0 AA** (14 CFR
382.43). *(Conocido; no re-verificado en esta sesión.)*

**Canadá.** *Accessible Transportation for Persons with Disabilities
Regulations* (SOR/2019-244, bajo la Canada Transportation Act), consolidación
vigente a 2026-03-17. La CTA identifica la **reserva** como punto de fricción;
**esta sesión no pudo confirmar qué exige el reglamento al canal de reserva
online.** Brecha escrita.

**Demanda.** Open Doors Organization / Harris Poll: viajeros con discapacidad
de EE.UU. gastan **~50.000 M USD/año** en viaje, **>100.000 M** con
acompañantes; el gasto en crucero pasó de 10,4 a 18,5 mil M entre 2020 y 2024.
Es la cifra citable de este plano (ver *Tamaño de mercado*).

**Oportunidad.** La pieza que la regla del DOT vuelve contable —"¿este vuelo
puede llevar **esta** silla?"— es un dato de **dimensiones de bodega y de la
silla**, no una casilla. Un agente de reserva que no pregunta y no verifica
vende el billete que la regla presume ilegal cuando la pausa termine. Receta 20
con el dato de aeronave de la segunda pasada.

*Agregado en la octava pasada del 2026-11-23 — plano de la reseña:*

**Regulación.** La **Consumer Review Rule de la FTC (16 CFR Part 465)** es la norma sobre
reseñas más dura de las cuatro regiones y la única de alcance federal en EE.UU. Prohíbe
crear, vender, comprar y **difundir** reseñas falsas "cuando la empresa supiera o debiera
haber sabido" que lo eran, y la FTC citó expresamente las **reseñas generadas por AI** como
caso cubierto, por representar a alguien que no existe. *[fuentes secundarias coincidentes]*
sanción civil de hasta **USD 53.088 por infracción**, y acciones que en 2026 ya invocan la
regla. El punto que importa para el diseño: **"difundir" alcanza a quien muestra la reseña,
no solo a quien la escribe.** Un agente de viaje que resume reseñas de terceros está
difundiendo.

**Oportunidad.** La más vendible de la región en este plano no es un detector: es **el
expediente**. Si la responsabilidad se activa por "debiera haber sabido", el entregable es la
**traza**: qué reseñas entraron al resumen, de qué ventana temporal, con qué volumen, y qué se
dejó afuera y por qué. `ScalaConsultants/ABSA` (Apache-2.0) sirve justamente porque **expone
pesos de atención por aspecto** — es decir, es auditable, no una caja negra. Receta 23.

#### Plano del equipaje — North America (2026-11-23)

**El artefacto que la regulación de esta región vuelve obligatorio: un reloj.** El reglamento de
reembolsos automáticos del DOT exige devolver **la tasa de equipaje facturado** si la pieza no se
entrega dentro de un plazo, contado desde la llegada del vuelo a la puerta, **una vez que el
pasajero presenta un Mishandled Baggage Report (MBR)**.

| Elemento | Valor | Confianza |
|----------|-------|-----------|
| Umbral doméstico | **12 horas** desde la llegada a la puerta | Coincidente en la guía de cumplimiento para pequeñas empresas del DOT y en cuatro fuentes secundarias |
| Umbral internacional | **15 a 30 horas** según la duración del vuelo | Igual |
| Disparador | El pasajero **presenta un MBR**; el reembolso es automático después | El propio DOT describe que el MBR puede presentarse en cualquier momento tras la no llegada |
| Alcance | **La tasa pagada por facturar**, no el contenido de la maleta | Coincidente |
| Cifra en disputa | Una fuente afirma un **umbral único de 6 horas** | **Atípica contra cinco fuentes. Se registra y no se afirma** |

> ⚠️ **`transportation.gov` y `www.federalregister.gov` no resuelven desde esta red.** Para
> confirmar el estado vigente del reglamento hay que habilitar esos dominios en la configuración
> de red de la sesión. Todo lo de arriba es **secundario coincidente**.

**El contexto regulatorio se movió en contra en 2026, y hay que decirlo completo:**

- El **Quinto Circuito anuló** el reglamento de divulgación de tarifas de 2024 el **3-feb-2026**,
  por motivos **procesales** — no porque la divulgación sea ilegal. El DOT volvió al estándar de
  2011 el **2-jul-2026**. Una futura reglamentación puede reabrirlo.
- El DOT **rescindió** la regla de compensación en efectivo por demoras y cancelaciones
  controlables en **sep-2025**. Es una norma **distinta** del reembolso de la tasa de equipaje y
  no parece afectarlo.
- *"Airline Refunds and Other Consumer Protections III"* está en etapa de propuesta y una fuente
  lo describe explícitamente como **reducción de carga regulatoria**. Sin resultado final.
- Un aviso del **5-dic-2025** pausó la aplicación de la regla de reembolso por cancelación para
  **renumeración de vuelo** hasta el **30-jun-2026**. Esa fecha ya pasó y **no se pudo determinar
  si se extendió o caducó**.

**Lectura para un engagement:** el reembolso de la tasa de equipaje es el elemento de esta familia
que **sobrevivió** a un año de desregulación, y es el único que depende de **una hora registrada**
en lugar de un juicio sobre si la demora era controlable. Un reloj es defendible; un juicio no.
Por eso es el que conviene construir.

**Adopción y players (2026):** Deloitte mide **25%** de viajeros estadounidenses usando IA
generativa para planificar, contra 15% en 2025 (encuesta de 4.003 personas). Phocuswright mide
**33%** usando plataformas tipo ChatGPT para investigar un viaje, **quintuplicado desde 2024**, y
**64%** de los usuarios de IA usan herramientas autónomas antes que las del proveedor. En la
conferencia Phocuswright 2026 expusieron United, Hilton, Airbnb, Priceline, Spotnana y Booking
Holdings; Google puso en prueba en vivo la reserva agentic de hotel en EE.UU. en **ago-2026**. La
Casa Blanca publicó en **mar-2026** recomendaciones legislativas para un marco federal único de IA.

**Oportunidad Globant en North America, este plano:** un **motor de reembolso de tasa de equipaje
con reloj auditable** — la Receta 26. Los insumos existen y son MIT: `jetway` emite y parsea el
BSM y abre el expediente AHL con marca temporal, y el reloj del DOT necesita exactamente dos
sellos de tiempo (llegada a puerta, entrega de la pieza) más el MBR. Es el mismo patrón que la
Receta 10 (motor de derechos del pasajero con reloj) aplicado al objeto físico, y se vende solo
con la cifra de SITA: **USD 260 por pieza**.


#### El plano del precio — North America (2026-11-23, décima pasada)

Es la región con la obligación **más literal** de todo este KB: no pide un informe ni un
formato de dato, pide **una frase exacta en la pantalla**.

| Elemento | Dato | Fuente |
| --- | --- | --- |
| Norma | NY General Business Law § 349-a, *Algorithmic Pricing Disclosure Act* | Múltiples firmas (Skadden, Duane Morris, Kelley Drye, WSGR) coincidentes |
| En vigor | 2025-11-10 | Anuncio de la NY AG (Letitia James), citado por Kelley Drye y Legal 500 |
| Qué exige | Divulgación clara y visible: **«THIS PRICE WAS SET BY AN ALGORITHM USING YOUR PERSONAL DATA»** | § 349-a subd. 2, citada textualmente por Kelley Drye y jdsupra |
| Disparador | Precio fijado por algoritmo **usando dato personal del consumidor** | § 349-a |
| Sanción | Hasta **USD 1.000 por violación**, aplica la AG | Skadden, Duane Morris |
| Exentos | Aseguradoras e instituciones financieras reguladas | Mondaq, Skadden |
| Litigio | La National Retail Federation perdió en primera instancia (SDNY); apelación **argumentada el 2026-10-19** en el Segundo Circuito, **sin fallo localizado** | Duane Morris, Lexology |
| Lo que viene | *One Fair Price Act* (S.8623B / A.9349B), aprobada por la legislatura en **junio de 2026**: **prohíbe** el precio personalizado por historial de compra, navegación, ubicación en tiempo real, ingreso o tamaño de hogar inferido. **Pendiente de firma del gobernador, plazo 2026-12-31** | WSGR, nysenate.gov (vía buscador) |

**La pregunta travel que la cobertura general no hace, y su respuesta honesta.** § 349-a es
ley **estatal**. La Airline Deregulation Act (49 U.S.C. § 41713) impide a los estados legislar
sobre «prices, routes or services» de una aerolínea; en *Morales* la Corte Suprema anuló el uso
de estatutos estatales de consumo para vigilar la publicidad de tarifas; y el propio DOT, en su
propuesta de julio de 2026 sobre publicidad de tarifas, afirma que «States are already preempted
from regulating in this area by the Airline Deregulation Act, 49 U.S.C. 41713».

> **Esto es una INFERENCIA de esta sesión, no un fallo.** Ninguna fuente que alcancé aplica la
> preemption de la ADA a § 349-a en particular. Lo que se puede afirmar: hotel, alquiler de auto,
> OTA, tours y actividades caen de lleno en el alcance; **la tarifa aérea es territorio disputado**.
> La consecuencia de arquitectura es la parte sólida, y no depende de quién gane: **el interruptor
> de divulgación es por línea de producto, no por estado.** Un motor único que sirve hotel y vuelo
> necesita las dos ramas y el registro de cuál disparó. Receta 29.

**El vector contrario, en la misma región y el mismo año.** Mientras Nueva York aprieta, el
federal afloja: el DOT propuso en julio de 2026 *Enhancing Flexibility of Air Fare Price
Advertising* y restauró las reglas de divulgación de cargos auxiliares previas a 2024. North
America es la única región donde el eje regulatorio **apunta en dos direcciones a la vez**, y la
dirección depende de si el producto es un vuelo o una habitación.

**La presión no regulatoria, que llegó antes que la norma.** El Congreso envió cartas a **ocho
aerolíneas** pidiendo explicación de sus sistemas de precios (plazo reportado: 2026-08-25); un
subcomité del Senado (Judiciary, Crime and Counterterrorism) hizo su **primera audiencia dedicada
a *surveillance pricing* el 2026-08-04**; los senadores Gallego, Warner y Blumenthal escribieron a
Delta por su acuerdo con Fetcherr. Delta negó formalmente: «no fare product Delta has ever used,
is testing or plans to use that targets customers with individualized prices based on personal
data». **Las fechas de esta secuencia varían entre fuentes** (hay reportes que ubican la carta en
2025) y van marcadas como tales.

**Oportunidad Globant en North America, este plano:** el **interruptor de divulgación por producto
con registro de decisión** (Receta 29). No es un modelo de precios: es la pieza de gobierno que una
cadena hotelera o una OTA con tráfico de Nueva York necesita para responder «por qué este precio»
sin apagar su motor. El diferenciador es que se puede auditar hacia atrás: qué rama disparó, con
qué entradas, con qué versión de biblioteca. Y la variante defensiva —**precio desde capacidad y no
desde la persona** (Receta 28)— es la única que contesta la pregunta del regulador de forma
estructural en lugar de documental.


#### Comprobante fiscal — la región sin mandato, y por eso con la oportunidad invertida (undécima pasada, 2026-11-23)

**Evidencia.** **EE. UU. no tiene mandato federal de facturación electrónica B2B** y, según
cobertura de compliance actualizada a septiembre de 2026, **tampoco hay propuesta en trámite**. La
red **DBNAlliance** es un marco de intercambio **voluntario**, alineado a Peppol, presentado como
la contraparte norteamericana de la red europea; tuvo su primera conferencia en Nueva York en abril
de 2026 (las fuentes discrepan entre el 1 y el 22 de abril). La adopción sigue siendo limitada: la
mayor parte de la facturación B2B de EE. UU. es papel, PDF o EDI. La excepción es la compra
pública: las agencias federales facturan electrónicamente desde 2015, sobre todo por la Invoice
Processing Platform del Tesoro.

**La medición que lo confirma del lado del código:** la familia de doce servidores MCP por
jurisdicción **no tiene uno de EE. UU.**, y `dbnalliance` como búsqueda de repos devuelve **un solo
resultado**, de 2023, sin licencia y sin biblioteca. **No es un hueco de la familia: es la forma
correcta del mercado de EE. UU. en este plano.**

**La oportunidad, y acá está invertida respecto de las otras tres regiones.** En EMEA, APAC y LATAM
el trabajo es *cumplir un mandato*. En North America no hay mandato, así que el argumento no puede
ser compliance. Lo que sí hay es **un cliente norteamericano cuyos empleados viajan a jurisdicciones
que sí obligan**: una empresa de EE. UU. que manda gente a Bélgica, Polonia, Francia, India,
Singapur, Brasil o México **recibe facturas bajo seis regímenes distintos y no tiene mandato propio
que la haya obligado a construir la capacidad de leerlas**. Ése es el engagement: no emitir, sino
**recibir, validar y conciliar comprobantes extranjeros** contra el programa de viaje, con
`mustangproject` y `phive-rules` (los dos Apache-2.0) como motor de validación multi-jurisdicción y
la **Receta 33** como forma — y la Receta 31 como cura, porque toda estadía que llegó
como recibo es una regla de reserva para la próxima vez.

**El segundo ángulo, específico de la región.** El mismo cliente tiene un problema de IVA
extranjero recuperable que hoy no recupera por falta del dato en origen — y la pieza que lo arregla
es el adaptador de identidad fiscal en la reserva (Receta 31), no un motor fiscal.

**Gap declarado de la región:** no se localizó ninguna regulación de EE. UU. ni de Canadá que
obligue a un hotel o a una aerolínea a emitir un comprobante estructurado. **La ausencia está
medida, no asumida.**

**El plano del seguro en North America (2026-11-28, duodécima pasada): la región regula *quién
puede hablar*.**

**La norma, fechada.** El **NAIC Travel Insurance Model Act #632** fue adoptado en diciembre de 2018
y, según la propia NAIC, **38 estados lo tienen promulgado a abril de 2026**. La arquitectura
relevante para un agente es la figura del ***limited lines travel insurance producer***, con el
minorista de viaje **exento de licencia únicamente si se limita a «ofrecer y diseminar»** productos
en nombre de ese productor licenciado. (Las cifras de adopción varían según la fuente y la versión
del modelo que se mida: hay reportes de prensa sectorial de 46 estados para la parte de licencia de
agentes de viaje y de «todos menos 19» sin especificar versión. **La cifra de la NAIC es la que esta
KB usa.**)

**Por qué eso convierte al agente en un problema de alcance y no de producto.** La exención del
minorista se sostiene sobre un verbo estrecho: *ofrecer y diseminar*. Un asistente que **compara**
dos pólizas o **recomienda** un límite deja de estar describiendo un producto y pasa a realizar
*solicitation*. El estatuto de Florida enumera seis actividades que exigen licencia, entre ellas
**recomendar** y **comparar o interpretar coberturas** *(fuente secundaria: blog de un proveedor de
agentes de voz citando el estatuto — **[sin verificar]** contra el texto estatutario, y es la pieza
más citable del plano: confirmarla antes de usarla con un cliente)*. **La licencia se adhiere al
acto, no a la herramienta.**

**Lo que sí se mueve en producto en la región.** **Medavie Blue Cross (Canadá)** incorporó un
beneficio de demora **automático** para miembros de planes grupales, sobre la plataforma de Blink
Parametric, que monitorea el estado del vuelo y dispara el beneficio al cruzar el umbral **sin que
se radique reclamo**.

**La oportunidad, y es la inversa de la del comprobante.** Acá el entregable **es la restricción**.
A un cliente norteamericano no se le vende «un agente que vende seguro»: se le vende el
**gobernador de verbos** más el **registro auditable de la negativa** —la **Receta 34**, con el enum
de verbos restringido a `describir | ninguno` por configuración de tool y no por prompt (**Receta
35**, paso 3)—. Es un entregable chico, defendible ante el área legal del cliente, y es lo único del
plano que **no requiere habilitación para construirlo**: documentar una negativa no es distribuir un
seguro.

**El segundo ángulo de la región.** El viajero corporativo norteamericano ya tiene seguro de viaje
**en la tarjeta de crédito corporativa** y no lo usa. `tourclaim/tourclaim-cli` (MIT, creado
2026-10-04) existe exactamente para eso y deja la adjudicación en el administrador del beneficio de
la tarjeta — ⚠️ en *review mode* desde octubre de 2026 **crea reclamos sintéticos**, así que es base
de arquitectura, no proveedor en producción.

**Gaps declarados de la región:** no se localizó **ninguna norma federal de EE. UU. ni de Canadá
sobre AI en distribución de seguros**; las recomendaciones de marco federal de AI de marzo de 2026
no son específicas de seguros. Tampoco se localizó material sobre seguro de viaje en **México**
desde la óptica del regulador (CNSF) en esta pasada. **Las ausencias están medidas, no asumidas.**

### EMEA

**Evidencia.** *[sin verificar]* 38% de adopción de AI en travel en Europa Occidental y 42% en
Medio Oriente, con la transformación digital liderada por el Estado como motor en Medio Oriente
(contenido de proveedor). Encuesta comisionada por Expedia: 53% se siente cómodo con que la AI
*sugiera* opciones — de nuevo, sugerir sí, comprar no. Lufthansa Group: >50% de ventas de
agencia vía NDC (solo su negocio de agencia).

*Agregado el 2026-11-23 — Skift Data + AI Summit Europe, 13-oct-2026:*
- **Amex GBT evaluó ~139 casos de uso de AI en el último año, contra 13 el año anterior**:
  un orden de magnitud en doce meses. Es el mejor indicador publicado de que el corporate
  travel europeo pasó de pilotos sueltos a cartera.
- **Kayak y Skyscanner nombran los dos frenos y no son los que se suponen:** confianza y
  **verificación de precio**. El segundo es un problema de ingeniería resoluble, no de
  percepción — un agente que muestra un precio que no se sostiene al clic destruye la
  confianza una vez y para siempre.

**Regulación — la región más densa, y con una contradicción sin resolver.**
- El **Digital Omnibus on AI, Regulation (EU) 2026/1744**, refina el AI Act.
- Los requisitos de alto riesgo para sistemas **Annex III stand-alone** se corrieron de
  agosto-2026 a **2 de diciembre de 2027**; los **Annex I embebidos** a **2 de agosto de 2028**.
- ⚠️ **Conflicto documentado:** una nota de ciclo previo (retail) registra un plazo
  transitorio del **Art. 50 el 2026-12-02**. Son provisiones distintas con fechas parecidas y
  años distintos. **No conflacionarlas, y confirmar contra el texto oficial antes de
  comprometer un plazo con un cliente.**
- ⚠️ **Claim que circula y NO se pudo confirmar:** que la revisión del reglamento de derechos
  de los pasajeros aéreos obligue a asistentes de accesibilidad con AI desde enero-2026.
  **Aparece en una sola fuente y no se verificó.** Registrado como trampa, no como dato.
- Lectura específica de travel: la mayoría de las herramientas de cara al huésped
  **probablemente no califican como alto riesgo**, así que la postergación importa menos de lo
  que sugiere el titular. Lo que sí aplica siempre es transparencia y GDPR.
- **Medio Oriente:** a junio-2026, **ningún Estado del Golfo ni Israel tiene un estatuto
  horizontal integral de AI**. La norma vinculante más cercana es la **Regulation 10 de las
  DIFC Data Protection Regulations**, que gobierna datos personales procesados por sistemas
  autónomos y semiautónomos en el DIFC de Dubái. En Arabia Saudita el organismo clave es SDAIA.

**Frontera y entrada — el calendario que ningún ciclo anterior de esta KB registró.**
*Todo este bloque es de fuente secundaria: ver el límite de entorno declarado arriba.*
- **EES (Entry/Exit System):** despliegue progresivo iniciado el **2025-10-12** y con cierre
  previsto el **2026-04-09**. Las fuentes secundarias lo dan por completado.
- **ETIAS: a fines de noviembre de 2026 NO hay fecha oficial anunciada.** Las fuentes más
  recientes indican que el objetivo "4T-2026" fue retirado del sitio oficial en julio-2026 y
  que la expectativa se corrió a 2027. La Comisión se comprometió a anunciar la fecha con
  varios meses de anticipación. **Las fuentes de mediados de 2026 todavía dicen "4T-2026":
  están desactualizadas.** Si un cliente planifica contra el 4T-2026, el dato es viejo.
- **La lectura comercial es la misma en los dos casos:** un requisito de entrada nuevo que
  afecta a cientos de millones de viajeros, con fecha incierta, es exactamente la clase de
  evento que rompe itinerarios ya vendidos. Quien tenga el *servicing* resuelto gana el ciclo.

**Oportunidades.**
1. **NDC es un activo europeo.** Lufthansa es el caso más avanzado de NDC en agencias. Un
   engagement de "agente sobre NDC" tiene aquí el inventario más maduro.
2. **El DIFC es el mejor sandbox regulatorio de la región.** Una regla vinculante y específica
   sobre sistemas autónomos, en una jurisdicción financiera, es un marco para pilotear
   delegación de agentes con respaldo legal — raro en el mundo.
3. **Ferrocarril y multimodal: hueco abierto.** El único MCP ferroviario encontrado en todo el
   mundo es [`r-huijts/ns-mcp-server`](https://github.com/r-huijts/ns-mcp-server) (ferrocarril
   holandés, MIT, 64★) y está **dormido 15 meses**. Europa es el mercado ferroviario más denso
   del planeta y su capa agentic no existe. Con `motis` (MIT) y OTP (LGPL) las piezas están.
4. **Ventaja de procedencia de datos.** Bajo el AI Act, el stack self-hosted deja de ser
   preferencia y pasa a ser facilitador de cumplimiento.
5. **El EU Digital Identity Wallet es infraestructura pública y está lista para integrar.**
   La Comisión mantiene su verificador y sus librerías bajo **Apache-2.0**
   ([`eudi-srv-verifier-endpoint`](https://github.com/eu-digital-identity-wallet/eudi-srv-verifier-endpoint),
   [`eudi-lib-jvm-openid4vci-kt`](https://github.com/eu-digital-identity-wallet/eudi-lib-jvm-openid4vci-kt)),
   mientras las apps de referencia son **EUPL-1.2** y la especificación es **CC BY 4.0**.
   Un check-in de hotel o un flujo de embarque que acepta la credencial del wallet se construye
   sobre la capa permisiva sin tocar la copyleft. **Es la única capa de identidad del viajero,
   en cualquier región del mundo, mantenida por un regulador y publicada bajo licencia
   permisiva.** Detalle de las tres capas en `repos/trending.md`; receta en
   `compose/patterns.md` → Receta 8.
6. **EES/ETIAS como producto de servicing, no de cumplimiento.** El valor no está en "informar
   el requisito" — eso lo hace una página web. Está en reacomodar lo ya vendido cuando el
   requisito cambia de fecha, que es precisamente lo que ETIAS viene haciendo desde 2024.

7. **El regulador europeo acaba de trazar la misma línea que esta KB trazó entre documento y
   admisión — y eso cambia la postura de cumplimiento del plano de identidad.** Dos hechos
   distintos, los dos de 2026:
   - **El calendario se movió.** El *Digital Omnibus* — **Reglamento (UE) 2026/1744**,
     publicado en el DOUE el **2026-07-24** y en vigor desde el **2026-07-27** — difiere las
     obligaciones de alto riesgo de los sistemas autónomos del **Anexo III del 2026-08-02 al
     2026-12-02**, y las de los sistemas embebidos en productos regulados del **Anexo I al
     2028-08-02**. Las obligaciones de transparencia del **Artículo 50 siguen aplicando desde
     el 2026-08-02**: avisar que se habla con una AI y etiquetar el contenido generado no se
     aplazó. **Es una prórroga, no una derogación**, y conviene decirlo así al cliente.
   - **El contenido se precisó, y favorece el camino que esta KB ya recomendaba.** El punto 7
     del Anexo III (migración, asilo y control de fronteras) **excluye expresamente la
     verificación de documentos de viaje** de su literal (d). La lectura concordante de las
     fuentes consultadas: la verificación **1:1** — el viajero confirma su identidad contra el
     chip de su propio pasaporte, que es exactamente lo que hacen
     [`AndyQ/NFCPassportReader`](https://github.com/AndyQ/NFCPassportReader) (MIT) y
     [`fastmrz`](https://github.com/sivakumar-mahalingam/fastmrz) (Apache-2.0) — **queda
     fuera** del literal (d); la identificación **1:N** contra una lista de vigilancia **queda
     dentro** y es de alto riesgo; y el literal (c) puede alcanzar igualmente a un escáner de
     autenticidad documental usado **dentro de una solicitud de visado**. Traducido a
     arquitectura: **el check-in biométrico del hotel y el embarque 1:1 no son el caso
     regulado; el matching contra listas sí.** Son dos productos distintos y conviene no
     venderlos en el mismo enunciado.

   ⚠️ **Límite de verificación declarado.** `ai-act-service-desk.ec.europa.eu` y
   `opensky-network.org` **no resuelven DNS desde el entorno de ingesta** de esta KB (el ciclo
   anterior registró la misma restricción para dominios de la UE). Lo anterior está
   corroborado por varias fuentes secundarias concordantes, **incluido el texto citado del
   propio Service Desk de la Comisión**, pero **no fue leído en EUR-Lex**. Antes de
   comprometerlo en una propuesta hay que abrir el Anexo III del Reglamento (UE) 2024/1689 y
   el Reglamento (UE) 2026/1744 en la fuente oficial. Receta en `compose/patterns.md` →
   Receta 11.


**Agregado en la tercera pasada del 2026-11-23 — el pago agentic es, en EMEA, un problema de
autenticación, no de protocolo.**

Es la diferencia regional más accionable que esta KB midió sobre el plano de pago. **PSD2 no
tiene régimen específico para agentes**: las fuentes consultadas coinciden en que la directiva
es tecnológicamente neutra y por lo tanto **alcanza al agente que inicia un pago**, sin
excepción ni puerta especial. El choque es con la **SCA (autenticación reforzada)**, cuyo
diseño de dos factores —conocimiento, posesión, inherencia— **presupone un pagador humano
presente**. Un agente que paga solo no encaja en esa estructura, y las fuentes señalan que el
**Reglamento de Servicios de Pago (PSR) en trámite tampoco aborda expresamente la ejecución
agentic**.

Dos consecuencias prácticas, dichas como se le dicen a un cliente:

1. **Entregar credenciales al agente traslada el riesgo al consumidor.** Al menos una fuente
   lo ata al artículo 69 de PSD2 y a los términos del banco. Un diseño que guarde credenciales
   del viajero para que el agente pague **es, en EMEA, un pasivo** — y es exactamente el
   diseño que un cliente pide cuando dice "que reserve solo".
2. **El mandato no cubre el error.** Un agente puede comprar lo equivocado **sin salirse** del
   mandato aprobado; esa disputa puede no calificar como fraude, y entonces no hay a quién
   reclamarle. Es el hueco que ningún protocolo del plano resuelve.

**Señal de mercado:** se reportan **Santander y Mastercard** con pagos de punta a punta
ejecutados por un agente en Europa (1-mar-2026), y transacciones agentic autenticadas de
Mastercard en Polonia — descritos como **pilotos con topes de gasto y autenticación por
compra**, no como producto abierto. El patrón coincide con lo que recomienda la Receta 12:
mandato acotado, vencible y auditable.

⚠️ **Límite de verificación.** Todo este bloque proviene de **análisis de estudios jurídicos y
prensa de pagos concordantes entre sí**, no de EUR-Lex: no se leyeron PSD2, sus RTS de SCA ni
el borrador de PSR en la fuente oficial desde este entorno. Las fuentes además **difieren en
fechas** y tratan la posición europea como **no resuelta**. Antes de comprometer un diseño de
pago agentic en una propuesta EMEA, esto lo valida el equipo legal del cliente, no esta KB.

**Nota de corroboración:** la mención de que **AP2 pasó a la FIDO Alliance**, que la tercera
pasada registró como no corroborada en `agents/top.md`, aparece **por segunda vez y en una
fuente independiente** (análisis de pagos), que describe un grupo de trabajo desarrollando
especificaciones de comercio iniciado por agentes. **Sigue sin confirmarse en fuente primaria**,
pero ya son dos fuentes independientes: es la explicación más probable del repo quieto desde
junio (`intel/trends.md` → 18).
**Agregado en la cuarta pasada del 2026-11-23 — visibilidad agentic: la única región donde la
visibilidad es además una obligación legal.**

- **Transparencia exigible desde agosto de 2026.** Las obligaciones de transparencia del AI Act
  europeo pasaron a ser aplicables el **2 de agosto de 2026**: hay que **avisar al usuario que
  habla con una máquina** y **etiquetar el contenido sintético** *[fuente secundaria; los
  dominios oficiales de la UE no son alcanzables desde este entorno — ver límite declarado
  arriba]*. Para travel esto toca de lleno la visibilidad: **la descripción de destino generada
  con AI es contenido sintético etiquetable**, y el concierge del hotel es una máquina que debe
  presentarse como tal.
- **El riesgo de invisibilidad es estructural, no técnico.** La cobertura del sector (Skift,
  sep/oct-2026) describe que **los hoteles independientes europeos corren el riesgo de ser
  invisibles en las respuestas AI antes siquiera de competir por la reserva**, y que Booking
  Holdings —con **más del 70% de cuota OTA en Europa**— es tratado como *gatekeeper*. Un
  independiente que no emite schema propio sólo existe en la respuesta **a través de su OTA**.
- **Financiamiento real:** las startups europeas de travel AI levantaron **158 M USD en los
  primeros tres trimestres de 2026**, más del 20% del venture europeo revelado del año
  *[fuente secundaria]*.
- **Fragmentación como requisito de diseño:** multilingüe, multi-marca, multi-sistema de
  reservas y multi-frontera regulatoria. Un `@graph` JSON-LD **por idioma y por entidad legal**,
  no uno global.

**Oportunidad:** *visibilidad con prueba de cumplimiento*. EMEA es la región donde el mismo
entregable sirve dos veces: el JSON-LD que te hace citable y el registro fechado de
etiquetado/divulgación que te hace auditable. **Vender las dos juntas, no la segunda como
costo.**

#### Plano terrestre — medido el 2026-11-23, y es la región del plano

**Evidencia — la más densa y la mejor fechada de las cuatro.** EMEA concentra **siete de los
ocho servidores MCP de transporte terrestre del mundo**, el estándar de venta, el cuerpo
normativo y el calendario regulatorio.

- **El estándar de venta existe, es abierto y es permisivo.** OSDM (*Open Sales and
  Distribution Model*, UIC IRS 90918-10) está publicado en GitHub bajo **Apache-2.0** (95★,
  push 2026-11-20). Cubre oferta, tarifa, reserva de plaza y emisión, para ferrocarril y
  multimodal. Suecia lo adoptó como estándar nacional de distribución en abril de 2025.
- **El regulador lo respaldó con fecha.** La Comisión adoptó la **TSI de telemática** el
  2026-02-06 como **Reglamento de Ejecución (UE) 2026/253**, en vigor desde el **2026-03-02**:
  obliga a publicar **gratuitamente** los datos de planificación de viaje, información al
  pasajero y *ticketing* a través de los **puntos de acceso nacionales (NAP)**, con
  implementación esperada **2027–2028**. *[fuente: ERA y DG MOVE vía búsqueda — los dominios
  `era.europa.eu` y `transport.ec.europa.eu` **no resuelven DNS desde este entorno de ingesta**,
  así que el número de reglamento y las fechas están tomados de resúmenes de esas páginas y no
  del texto oficial. **Verificar contra el DOUE antes de citarlo a un cliente.**]*
- **Y hay un paquete legislativo encima, del 2026-05-13.** La Comisión publicó
  **COM(2026) 232 final** sobre *rail ticketing*, anunciado en noviembre de 2025 como tres
  instrumentos: un **Reglamento MDMS** (servicios digitales multimodales), un **Reglamento de
  Reserva y Billete Único Digital**, y una **revisión focalizada del Reglamento de Derechos
  del Pasajero ferroviario**. Incluye obligaciones para los *"indispensable railway online
  ticketing service providers"* de **alojar ofertas ferroviarias de terceros**, y se declara
  complementario de la DSA. *[mismo límite de verificación; **estado legislativo posterior al
  2026-05-13 no comprobado en esta pasada**.]*
- **La capa de acceso es permisiva y está viva**: `hafas-client` (ISC, 372★),
  `db-vendo-client` (ISC, 209★), `OpendataCH/Transport` (MIT, 269★, push 2026-11-22). **Pero
  hablan con endpoints no documentados de los operadores** — el permiso para llamarlos en
  producción no viene con el repo (ver `repos/foundations.md`).
- **La capa de estándar europeo trae una licencia nueva y exigente.** Los convertidores
  NeTEx/SIRI de **Entur** (operador estatal noruego, push **hoy**) son **EUPL-1.2**, cuyo
  gatillo incluye *"providing access to its essential functionalities"* — **más amplio que la
  AGPL**. Se usan como proceso batch fuera del producto, nunca enlazados dentro del servicio.

**Oportunidad — y es la más concreta que esta KB ha podido colocar en EMEA:** *el cliente OSDM
que no existe*. El estándar es Apache-2.0 y vendorizable; la consulta `osdm client
implementation` devuelve **0 repositorios**; lo único que lo toca cubre solo estaciones y está
dormido desde abril de 2025. **Hay un estándar respaldado por el regulador, con fecha de
implementación 2027–2028, y nadie publicó la pieza de software que lo consume.** Para un
operador o una agencia europea eso es una ventana de dos años con el riesgo técnico ya
resuelto por el UIC.

⚠️ **Lo que no hay que prometer en EMEA:** una integración OSDM "lista". No hay código del cual
partir; hay una especificación excelente. El presupuesto es de implementación, no de
integración — y la diferencia entre esas dos palabras es todo el proyecto.



#### Sexta pasada 2026-11-23 — adopción, regulación y el plano de emisiones

**Adopción.** El informe EMEA 2026 de Marriott Bonvoy (más de **22.000 adultos
en 11 mercados**) encuentra que **más de la mitad** de los viajeros de EMEA ya
usó IA para planificar o investigar un viaje, y que la franja de **55–64 años
pasó de 18% en 2024 a 29%**. El mismo informe anota que los viajeros **notan
cuando la IA se equivoca** — en un mercado con esa tasa de uso, el error es
visible, no anecdótico.

**Adopción empresarial: ancha y poco profunda.** Phocuswright mide **más del
60%** de las compañías experimentando o escalando IA agentic, pero **sólo el
6%** escalándola a través de múltiples dominios y funciones. El resto es
táctico, montado sobre infraestructura existente. En hotelería, las barreras
declaradas son privacidad y seguridad del dato **46%**, costo **42%** e
integración con sistemas legacy **40%** — ⚠️ esa encuesta **no es específica de
EMEA**, se cita como orden de magnitud.

**Regulación — y por qué EMEA es la región que define este plano.** El **EU AI
Act** entra en plena aplicación, y la Comisión publicó en **julio de 2026** sus
*Guidelines on Transparency Obligations for AI Systems*. Skift describe el
mercado como fragmentado, donde compliance, idioma y soberanía del dato deciden
quién puede operar IA a escala.

Pero lo que vuelve a EMEA el centro del plano de emisiones es el stack
regulatorio climático, que **no tiene equivalente en ninguna otra región**:

| Instrumento | Qué obliga | Estado |
|---|---|---|
| **CSRD / ESRS** | Reporte corporativo de sostenibilidad, incluye Scope 3 categoría 6 (viajes de negocio) | En aplicación |
| **ReFuelEU Aviation** | Mezcla de SAF en aeropuertos de la UE: **2% desde 2025**, **6% en 2030**, 70% en 2050 | En vigor |
| **EU ETS aviación** | Derechos de emisión para vuelos intra-EEE | En vigor |

⚠️ **Corrección de un error que circula:** varias guías presentan "6% en 2026".
El escalón de **6% es 2030**; en 2026 la obligación sigue siendo **2%**.

**Inversión y players.** Las startups europeas de IA en viajes levantaron
**158 M USD en los tres primeros trimestres de 2026**, más del **20%** del
capital de riesgo europeo divulgado del vertical. Despliegues concretos: Accor
con IDeaS (G3 RMS) en su portfolio global; **Finnair**, primera aerolínea del
mundo en crear una Native Order sobre Nevio. Skift advierte que los hoteles
independientes europeos corren el riesgo de ser **invisibles en las respuestas
de IA antes de llegar a competir por la reserva** — eso conecta directo con el
plano de visibilidad de la cuarta pasada.

#### Séptima pasada 2026-11-23 — plano de accesibilidad

**Regulación — la más madura de las cuatro regiones en este plano.** La
**European Accessibility Act** (Directiva (UE) 2019/882) aplica desde el
**28-06-2025** a los servicios de comercio electrónico y a los sitios y apps
de transporte aéreo, ferroviario, por autobús y por agua. Alcanza el sitio y la
app donde se reserva un vuelo, un tren o un hotel. El estándar armonizado es
**EN 301 549**, que remite a **WCAG 2.1 AA**. La aplicación es nacional: en
Irlanda la **Irish Aviation Authority** es la autoridad de cumplimiento para
aerolíneas y verifica la corrección de lo que encuentra.

Matices que cambian el alcance de una propuesta *(texto de la Directiva,
conocido; no re-verificado contra EUR-Lex en esta sesión)*: las
**microempresas que prestan servicios** quedan exentas — muchos hoteles
independientes caen ahí — y los servicios pueden seguir usando hasta el
**28-06-2030** los productos que ya usaban legalmente antes de junio de 2025.

**Cumplimiento real.** Un balance al primer año (junio 2026, proveedor de
herramientas de accesibilidad) concluye que las empresas **todavía no
cumplen** — fuente comercial, leerla como señal, no como medición.

**Demanda.** El reporte TUR4all de España ubica al viajero estadounidense
como el mercado receptivo accesible más rentable: **~273 €/día**.

**Oportunidad.** Es la región donde la **Receta 19** (gate de accesibilidad en
CI del flujo de reserva) se vende sola: hay obligación vigente, autoridad
nombrada y estándar técnico. El diferencial de Globant no es correr un
escáner — es **entregar el informe de conformidad EN 301 549 como artefacto de
cada release**.

*Agregado en la octava pasada del 2026-11-23 — plano de la reseña:*

**Es la región donde este plano dejó de ser teórico, con tres hechos fechados.**

1. **Comisión Europea, 21-oct-2026: procedimiento formal DSA contra Booking.com.** Tres
   frentes: **listados fraudulentos o no conformes**, **phishing que explota datos de reserva
   y de huésped**, y **listados impulsados por pago no identificables como publicidad**.
   *[fuente secundaria, múltiple]* los artículos señalados serían **26, 34 y 35** del DSA. El
   procedimiento habilita medidas provisionales, decisión de incumplimiento o compromisos.
2. **Italia, Ley 34/2026 (Ley Anual de PyMEs), en vigor el 7-abr-2026.** Prohíbe **comprar y
   vender reseñas, valoraciones e interacciones, por cualquier motivo**, incluido entre
   hoteleros e intermediarios, y desconoce las reseñas obtenidas con descuentos o regalos para
   "ajustar" la calificación. Exige **prueba de la estadía** vía recibo o documento fiscal
   —**la ventana aparece como 15 días en el borrador de ene-2025 y como 30 en coberturas
   posteriores; no se pudo leer el texto final, se registran las dos**— y habilita al hotelero
   a pedir la **remoción** de la reseña ilícita al hosting provider por la vía del DSA.
3. **AGCM multó a Trustpilot con 4 M€** por práctica comercial desleal: no verificó
   adecuadamente la autenticidad de las reseñas, **incluidas las marcadas como "verificadas"**.
   Es el precedente más citable del plano: **el sello de verificación, sin mecanismo detrás, es
   el pasivo, no la defensa.**

**Reino Unido, 3-jul-2026.** *Which?* publicó que los **resúmenes AI de reseñas de Tripadvisor**
omitían intoxicaciones alimentarias y denuncias de acoso sexual —102 menciones de intoxicación
en una propiedad en marzo-2026 y 32 reseñas de 1-2 estrellas entre dic-2025 y abr-2026—
mientras los resúmenes de Google sí advertían "posibilidad de enfermedad". Tripadvisor
"discrepa fundamentalmente" y afirma que suprime el resumen AI en fichas con incidentes graves
de seguridad. **No hay sanción: hay un método de auditoría publicado y replicable**, que es
peor para quien vende resúmenes y mejor para quien los audita.

**Oportunidad.** Dos entregables distintos, los dos con comprador identificado:
1. **Prueba de estadía como producto, para el hotelero italiano.** La ley le da el derecho de
   pedir remoción, pero la carga de la prueba. El PMS ya tiene el folio: convertirlo en
   atributo verificable de estadía es la Receta 22, y el mercado es inmediato y obligatorio.
2. **Procedencia del listado, para la plataforma bajo DSA.** El frente de "listados
   fraudulentos" se ataca con la capa que **sí está viva**: firmar la foto del alojamiento en
   origen con C2PA (`c2pa-swift`/`c2pa-js`, MIT *o* Apache-2.0) y verificarla en la ficha.
   Receta 24.

#### Plano del equipaje — EMEA (2026-11-23)

**La región con el equipaje más caro del mundo y con la reforma regulatoria más grande en 20 años.**

**La cifra:** SITA mide en Europa el **costo promedio más alto por pieza mal manejada: USD 295**,
contra USD 260 global y USD 210 en APAC. El mismo problema cuesta **40% más** en Europa que en
Asia-Pacífico.

**El límite de responsabilidad, que es la pieza dura y verificada de este plano:**

| Elemento | Valor | Fuente |
|----------|-------|--------|
| Límite por **pasajero** (no por pieza) | **1.519 DEG** | Revisión quinquenal de la OACI bajo el art. 24 del Convenio de Montreal |
| Vigente desde | **28-dic-2024** | Aviso de la Agencia de Transporte de Canadá; aplica a toda pérdida ocurrida desde esa fecha |
| Límite anterior | 1.288 DEG | Alza de **~18%** |
| Efecto sobre contratos | **Prevalece sobre las condiciones de transporte** del transportista que lo contradigan | Clyde & Co |
| Valor declarado | El pasajero puede declarar un valor mayor en el check-in, que reemplaza el límite para esa pieza, normalmente con cargo | Varias fuentes de reclamos |

**"Por pasajero y no por pieza" es la regla que un sistema implementa mal por defecto.** Dos
viajeros que facturan una maleta cada uno tienen **cada uno** su límite de 1.519 DEG; una familia
de cuatro con una sola maleta perdida no tiene cuatro límites. Un motor de liquidación que agregue
por reserva en lugar de por pasajero paga de más o de menos, y en los dos casos es un hallazgo de
auditoría. (El orden de implementación de la UK fue reportado como vigente el **7-feb-2025** por
**una sola fuente**, sin verificar.)

**La reforma del Reglamento 261/2004 — primera en más de 20 años, y la parte de equipaje de mano
está en disputa entre fuentes:**

- Acuerdo político en **trílogo el 15-jun-2026**. Según una guía, el Parlamento aprobó el texto
  final el **7-jul-2026** y el Consejo el **13-jul-2026**. **No se encontró publicación en el
  Diario Oficial**, y una fuente espera entrada en vigor en el **segundo semestre de 2027**.
- **La disputa, registrada sin resolver:** una fuente afirma que un billete estándar dará derecho
  a **dos piezas de equipaje de mano gratis**. Otra lo niega y sostiene que **lo gratuito es un
  objeto personal** con límite de tamaño, y señala que **BEUC celebró la reforma pero advirtió
  abiertamente que el equipaje de cabina no quedó gratis** como esperaban. **Se registran las dos
  y no se afirma ninguna.**
- Lo que sí coincide: **el precio anunciado debe incluir el equipaje de mano**, con tarifas más
  bajas permitidas para quien viaje sin él; se **eliminan las cláusulas de no-show**; se mantiene
  la compensación por demoras de más de 3 horas, cancelaciones dentro de 14 días y denegación de
  embarque.
- Contexto de las enmiendas: las de segunda lectura del Parlamento son del **21-ene-2026**, y en
  el documento del Consejo **la Comisión rechaza la sugerencia de regular el derecho a llevar
  equipaje de mano** — de ahí que ese punto sea el disputado.

**Lectura:** el equipaje de mano en EMEA pasó de ser **precio** a ser **transparencia de precio**,
que es un problema de *producto y de feed*, no de operación. [`AxelUser/carry-fit`](https://github.com/AxelUser/carry-fit)
(MIT, 58★) verifica medidas por aerolínea y es el único repo permisivo que toca ese borde.

**Lo demás de la región (2026):** las obligaciones de transparencia de la Ley de IA de la UE son
**exigibles desde ago-2026**, con guías de la Comisión de **jul-2026**. Booking Holdings supera el
**70%** de cuota OTA en Europa y está designado *gatekeeper*; **~75% de los hoteles europeos son
independientes** y arriesgan ser invisibles en las respuestas de IA. Las startups europeas de IA
de viajes levantaron **USD 158 M** en los tres primeros trimestres de 2026, **más del 20%** del
venture europeo revelado del año (Crunchbase/HumanX vía Skift). El estudio de Marriott Bonvoy en
EMEA (**22.000+** adultos) mide que **más de la mitad** ya usó IA para planificar, y el tramo de
55-64 años pasó de 18% (2024) a **29%**.

**Oportunidad Globant en EMEA, este plano:** un **motor de liquidación de responsabilidad por
pasajero** que convierta 1.519 DEG a la moneda de la póliza en la fecha del hecho, agregue por
**pasajero** y no por reserva, y deje el rastro para auditoría. Es el plano donde la norma ya está
vigente (desde dic-2024), el costo por evento es el más alto del mundo (USD 295) y el riesgo de
implementación por defecto es **agregar por el objeto equivocado**.


#### El plano del precio — EMEA (2026-11-23, décima pasada)

EMEA es la región donde la obligación **ya existe y es vieja**, y donde lo que se discute es si
se endurece. Es también la única donde el deber de informar **no** depende de que el precio use
dato personal del consumidor: depende de que haya sido *personalizado por decisión automatizada*.

| Elemento | Dato | Fuente |
| --- | --- | --- |
| Norma vigente | Consumer Rights Directive: el comerciante debe informar **que** el precio fue personalizado mediante decisión automatizada | tgndata, Checkmate Experts, CMS |
| El límite de esa norma | **No** obliga a revelar los parámetros ni los criterios de la personalización | tgndata (explícito) |
| Lo que se discute | *Digital Fairness Act* (DFA) | Freshfields (2026-11), A&O Shearman, CMS, Lexology |
| Estado | **En conflicto entre fuentes.** El programa de trabajo de la Comisión para 2026 la lista para **Q4 2026**; briefings de noviembre de 2026 la describen ya presentada y con el procedimiento legislativo iniciado | Legislative Train (vía Parlamento) vs Freshfields/A&O |
| Lo que el DFA **no** hace | **No prohíbe** el precio personalizado como tal; **no** prohíbe el precio dinámico en tickets de evento, pese al pedido de las asociaciones de consumidores | A&O Shearman, CMS |
| Lo que **sí** prohíbe | Precio basado en *profiling* que razonablemente pueda dañar a consumidores que se sabe con certeza razonable que son **menores o vulnerables** | insideprivacy (vía buscador), A&O Shearman |
| Transparencia de precio dinámico | Limitada a **ticketing de eventos** | A&O Shearman |
| Excepciones en los recitales | Descuentos de estudiante y jubilado; tarificación de riesgo asegurador basada en evidencia | A&O Shearman |

> **Límite de verificación declarado.** `www.insideprivacy.com`, `www.slaughterandmay.com`,
> `www.nysenate.gov` y `newyork.public.law` **no resuelven desde esta red de ingesta**. Todo lo de
> arriba viene de resúmenes de firmas legales coincidentes entre sí, no de texto normativo leído.
> El estado del DFA queda **en disputa a propósito**: dos conjuntos de fuentes serias dicen cosas
> distintas y no se elige ninguna.

**Lo travel-específico, y es la diferencia que importa.** La CRD obliga a decir que el precio es
personalizado, pero no por qué. El § 349-a de Nueva York obliga a una frase fija y sólo cuando hay
dato personal. **Son disparadores distintos sobre el mismo evento de precio**: una OTA europea que
personaliza por segmento de dispositivo sin tocar dato identificable dispara la CRD y **no** dispara
Nueva York. Una cadena que personaliza por historial de estadías dispara las dos, con dos textos
distintos. Por eso el artefacto no puede ser un *flag* booleano global.

**El contexto de inversión de la región, medido.** Las startups europeas de AI en viajes levantaron
**USD 158 millones en los primeros tres trimestres de 2026**, más del 20% del venture europeo
divulgado del año en el vertical (Skift, cobertura del Data + AI Summit Europe). Y el obstáculo que
los propios hoteleros declaran no es el modelo: **privacidad y seguridad del dato 46%, costo 42%,
integración con sistemas legacy 40%** (ATM Yearbook 2026). El plano del precio toca el primero de
los tres de frente.

**Adopción del lado del viajero:** más de la mitad de los viajeros de EMEA ya usó AI para planificar
o investigar un viaje, y el tramo de 55–64 años subió a **29% en 2026 desde 18% en 2024** (Marriott
Bonvoy, +22.000 adultos en 11 mercados — **estudio de marca, no independiente**, y va marcado así).

**Oportunidad Globant en EMEA, este plano:** el **aviso de precio personalizado como componente del
flujo de reserva**, no como texto legal pegado al pie. Es la contracara de la Receta 19 (gate de
accesibilidad en CI) aplicada al precio: una pieza que, dado el evento de precio, decide si hay que
avisar, con qué texto y en qué idioma, y deja el registro. Si el DFA sale con la prohibición de
*profiling* sobre menores y vulnerables, esa misma pieza es donde se implementa el corte — y el
cliente que ya la tenga no rehace el motor.


#### Comprobante fiscal — la región donde el mandato ya venció y la factura de hotel entra (undécima pasada, 2026-11-23)

**Evidencia — y es la región con el calendario más denso de los once planos.** Todas las fechas
salen de **cobertura secundaria coincidente** (Sovos, Peppol.nu, guías de compliance y guías de
viaje corporativo), **no de los textos oficiales**:

| Jurisdicción | Estado | Fecha |
| --- | --- | --- |
| **Bélgica** | Vigente | **2026-01-01**, B2B estructurado obligatorio sobre Peppol entre empresas sujetas a IVA establecidas en Bélgica |
| **Polonia (KSeF)** | Vigente, por tramos | **2026-02-01** grandes contribuyentes, **2026-04-01** el resto de los registrados en IVA, **2027-01-01** micro |
| **Francia** | **Vigente desde el 2026-09-01** | Grandes y medianas **emiten**, y **todas las empresas deben poder recibir**. PyMEs y micro: **2027-09-01** |
| **Alemania** | Recepción obligatoria desde 2025 | Emisión por tramos **2027–2028**. ⚠️ fuentes en conflicto sobre el umbral (una dice 2027 sobre EUR 800.000 de facturación) |
| **España** | ⚠️ **fuentes en conflicto** | Verifactu corrido a **enero y julio de 2027** por decreto de diciembre de 2025 según una fuente; B2B el **2027-10-01** o el **2027-10-06** |
| **Italia** | Vigente desde hace años | FatturaPA / SDI |
| **Rumania** | Vigente | RO e-Factura. ⚠️ un recibo **se puede reportar** en 5 días hábiles y **no lleva el IVA del comprador**, así que la recuperación falla igual |
| **EAU** | 2026 | PINT AE / Peppol 5-corner |
| **UE (ViDA)** | Futuro | B2B transfronterizo y reporte digital apuntando al **2030-07-01** |

**El hecho travel-específico, y es el más accionable de toda la pasada.** Según guía de un proveedor
de viaje corporativo (⚠️ no del BMF): en Alemania **la factura de hotel entra plenamente al mandato
y el pasaje de avión y de tren están exentos**. Un solo viaje de negocios produce, entonces, **dos
regímenes documentales distintos** — e-factura obligatoria para el alojamiento, documento exento
para el transporte. Ninguna herramienta open source de este KB modela esa asimetría.

**La sanción, que es lo que mueve el presupuesto del cliente.** Cobertura de la industria reporta
multas de hasta el **3% de la facturación global** por incumplimiento del AI Act para firmas que
operan en la UE; el régimen de e-invoicing tiene su propio esquema sancionatorio por jurisdicción.
Y del lado de la recuperación: **un recibo sirve para deducir el gasto en el impuesto a las
ganancias y no sirve para recuperar el IVA.** La confirmación de pago de un hotel **no es** una
factura fiscal.

**La oportunidad.** La capa de código está, es madura y es permisiva: `mustangproject` (497★,
Apache-2.0, push de hoy) cubre Factur-X/ZUGFeRD/XRechnung/CII; `phive-rules` (55★, Apache-2.0,
push de hoy) trae las reglas de validación de muchas jurisdicciones en un solo motor; los MCP de
`cmendezs` cubren DE, ES, FR, IT, BE, PL y AE con Apache-2.0. Lo que **no** existe es el mapeo
folio→factura con *city tax*, desayuno e IVA por tasa, ni el adaptador de identidad fiscal en la
reserva. Receta 31 y Receta 32.

⚠️ **Dos trampas de licencia específicas de esta región:** los artefactos **oficiales** de
validación de la Comisión (`eInvoicing-EN16931`, 271★) son **EUPL-1.2, copyleft recíproco** — limpio
como gate de CI, contaminante dentro de un entregable cerrado; y `gflohr/e-invoice-eu` (383★, push
de hoy) es **WTFPL**, no aprobada por OSI, que varias áreas legales rechazan por política.

**El plano del seguro en EMEA (2026-11-28, duodécima pasada): la única región donde el regulador
nombró el artefacto de la negativa.**

**Las normas y las fechas, separando lo vinculante de lo que no lo es.**
- **EIOPA, Opinion sobre gobernanza y gestión de riesgo de AI: `EIOPA-BoS-25-360`, del 6-8-2025.**
  Dirigida a supervisores nacionales, **no vinculante**, y explícitamente **sin requisitos nuevos**:
  explica cómo la legislación existente (Solvencia II, IDD) aplica a sistemas de AI, con enfoque
  basado en riesgo. Revisión de prácticas supervisoras prevista **dos años después**, hacia agosto
  de 2027. ⚠️ Varios resúmenes comerciales la describen como «guidelines con seis áreas definidas»;
  **eso no coincide con la descripción de EIOPA**. Usar el documento, no los resúmenes.
- **La pregunta abierta, y es la que define el plano.** En un artículo vinculado a Eurofi de
  **septiembre de 2026**, EIOPA plantea si un chatbot que recolecta datos personales, **filtra
  productos o da recomendaciones** está realizando **actividad de distribución de seguros** bajo la
  IDD. La IDD es tecnológicamente neutral; eso no resuelve el caso, **lo deja abierto**.
- **Encuesta de GenAI de EIOPA del 2-2-2026:** **347 entidades en 25 países**.
- **FCA (Reino Unido), *signposting*:** vigente desde **abril de 2021**, obliga a derivar a un
  **directorio de proveedores especializados** —el de MoneyHelper, del Money and Pensions Service, o
  otro que cumpla los criterios de la FCA y figure en su listado— cuando la cobertura se **rechaza,
  no se ofrece, se cancela a mitad de vigencia o se recarga** por una condición médica preexistente.
  La FCA consultó cambios en **CP24/26** con efecto **1-1-2026**, que afectan el disparador de prima.
  ⚠️ **El umbral vigente no se pudo verificar** (la cifra de £100 es de prensa de la época de la
  consulta original): usar «hay un umbral y cambió en enero de 2026».

**Lo que se mueve en producto, y es la región más activa del mundo en paramétrico de viaje.**
**Cover-More Europe (Irlanda)** lanzó un beneficio paramétrico de demora: 3 horas o más disparan
**pase a sala VIP o €30 en efectivo instantáneo**, en tiempo real. **Aviva (Irlanda)** lanzó un
beneficio paramétrico de demora dentro de su seguro **grupal de viaje de negocios**. **Blink
Parametric** aparece como la plataforma detrás de varios de estos lanzamientos, incluido uno con
Heymondo.

**La oportunidad, y es doble.**
1. **El módulo de derivación (Receta 34, segundo estado).** EMEA es la única región donde la
   obligación de derivar existe **y el artefacto está nombrado**. Y los seis repos agentic de seguro
   de viaje que existen en el mundo **implementan el corte de venta y ninguno implementa la
   derivación**. Es un hueco chico, con norma que lo exige y cero competencia open source.
2. **El libro mayor indemnizatorio (Receta 36).** EMEA es donde EU261 convive con el seguro, así que
   es la región donde el riesgo de **cobrar dos veces el mismo gasto** es real y frecuente. Lo que
   hay de código es todo de los últimos tres meses —`hermes-plugin-delayclaim` (MIT, 7★, creado
   2026-11-10), `eu261-claim` (**AGPL-3.0**), `airtruth` (**sin licencia**, inusable)— y
   **ninguno implementa el principio indemnizatorio**.

⚠️ **La trampa de licencia de la región en este plano:** `eu261-claim` es **AGPL-3.0**. Como la
reclamación se expone por red, el copyleft de red aplica: corre **como servicio separado**, nunca
compilado dentro del entregable del cliente.

**Gaps declarados de la región:** no se leyó **ningún condicionado de póliza completo**, así que las
cláusulas de coordinación de beneficios quedan **[sin verificar]**; no se localizó material sobre
seguro de viaje en Medio Oriente ni África en esta pasada, pese a que la región del campo
`region: EMEA` los incluye. **Escrito como lo que falta medir.**

### APAC

**Evidencia — la región con mayor adopción medida, y la más desigual regulatoriamente.**
- **79% de las empresas de travel de APAC ya usan AI, 97% planea usarla** (investigación
  Expedia Group 2026, APAC).
- **49% de los viajeros de la región usa AI para descubrir destinos** (Visa 2026).
- **33% de los viajeros indios ya usa AI para planificar** (Agoda).
- **ChatGPT superó a Google por 13 puntos porcentuales** en visitas a páginas de reserva de
  travel en marzo-2026 (Criteo) — **y OpenAI retiró la reserva directa de ChatGPT ese mismo
  mes**. Las dos cosas pasaron juntas: la demanda llegó antes que la capacidad transaccional.

**Regulación — no hay un modelo, hay un mosaico.**
- **Corea del Sur: AI Basic Act en vigor desde el 22-ene-2026.**
- **Vietnam:** ley de AI vigente en 2026, pero **las fuentes discrepan**: una indica una *Law
  on Artificial Intelligence* efectiva el 1-mar-2026, otra una *Digital Technology Industry
  Law* con marco basado en riesgo. Verificar antes de asesorar.
- **China:** reglas por capas sobre algoritmos y AI generativa — el extremo más estricto.
- **Japón:** guías nacionales de gobernanza y ética **voluntarias**.
- **Singapur:** sin estatuto vinculante; se apoya en toolkits como **AI Verify**, y la
  **IMDA publicó en ene-2026 un marco de gobernanza de AI agentic que cubre cadenas de
  delegación y coordinación multiagente** — el documento regulatorio más directamente útil
  para trabajo con agentes que esta red de KBs encontró en cualquier región o industria.
  **Leerlo para cualquier engagement agentic, no solo de travel.**
- **Malasia:** el National AI Office publicó el 10-jul-2026 un paper de consulta pública sobre
  un AI Governance Bill.

**Frontera y entrada — APAC ya normalizó la declaración digital, y eso cambia el punto de
entrega del agente.** *(Fuentes secundarias: no se alcanzaron portales oficiales desde este
entorno. Verificar antes de prometer.)*
- **Singapur: la SG Arrival Card es obligatoria** y debe presentarse **dentro de los 3 días
  previos** a la entrada por aire, mar o tierra. Reemplazó la tarjeta de papel.
- **Japón: Visit Japan Web es opcional.** Unifica desembarque y declaración de aduana en un
  QR, y **el formulario de papel sigue siendo válido**. Un ciclo encontró el claim de que hay
  que registrarse 72 horas antes: **no se pudo corroborar**, tratarlo como no verificado.
- **La consecuencia de diseño:** donde la declaración es obligatoria y tiene ventana (Singapur,
  3 días), el itinerario deja de ser un documento y pasa a ser **una secuencia con vencimientos
  propios**. Un agente de viaje en APAC que no modele "esta tarea vence 3 días antes de volar"
  entrega un itinerario incompleto, por bonito que sea el PDF.

**Oportunidades.**
1. **APAC es donde está el open source de travel.** El cluster regional es el más fuerte del
   mundo: [`jianhao-travel-planner`](https://github.com/awangwang123/jianhao-travel-planner)
   (449★), [`travel-plan-viz`](https://github.com/zexuanw958-svg/travel-plan-viz) (415★),
   [`china-travel-kit`](https://github.com/tczyliu/china-travel-kit) (179★) y los MCP de
   RollingGo (2M+ hoteles). Un engagement APAC arranca con código real, no con un framework.
2. **Turismo receptivo a China con fuente citada.** `china-travel-kit` expone datos con
   procedencia — exactamente lo que exige el entorno regulatorio chino.
3. **Corporate travel multi-carrier.** Rutas multi-aerolínea y reserva multilingüe son el caso
   estructural de APAC; los finalistas de Business Travel Show APAC 2026 (FCM, TruTrip,
   Thrust Carbon) marcan dónde está la demanda.
4. **Singapur como sede de gobernanza agentic.** Con el marco de IMDA, es la jurisdicción
   donde un diseño de delegación de agentes se puede defender ante un comité de riesgo.
5. **El itinerario con obligaciones vencibles es un producto APAC.** Tarjeta de llegada
   obligatoria con ventana (Singapur), opcional con QR (Japón), e-visa y permisos según
   mercado: la región tiene la mayor densidad de trámites previos con fecha. Un planificador
   que emite **tareas fechadas además del itinerario** es diferenciación real, y se arma sobre
   la taxonomía de [`imorte/passport-index-data`](https://github.com/imorte/passport-index-data)
   (MIT) — **usando su esquema, no sus valores**, que llevan nueve meses sin actualizar
   (ver `repos/foundations.md`). Receta en `compose/patterns.md` → Receta 9.

6. **Es la primera región fuera de la UE con ley de AI vinculante, y el calendario es de
   2026.** La **Ley Marco de AI de Corea del Sur entró en vigor el 2026-01-22**; la **Ley de
   Inteligencia Artificial de Vietnam rige desde el 2026-03-01**; y la Oficina Nacional de AI
   de **Malasia abrió consulta pública sobre un proyecto de ley de gobernanza de AI el
   2026-07-10**. Al mismo tiempo es la región con mayor despliegue medido — **79% de las
   empresas de travel de APAC ya usan AI y 97% planea usarla** (Expedia Group 2026). La
   combinación es poco común y define el encargo: **aquí el cliente ya tiene el agente en
   producción y lo que necesita es que sobreviva a una ley que llegó después.** Eso es
   trabajo de trazabilidad y de obligaciones fechadas — la Receta 9 — no un piloto nuevo.
   **Brecha medida, no silenciada:** no se encontró ningún repositorio de datos de vuelo
   específico de APAC con tracción; el plano de datos operativos de vuelo de esta KB
   (`repos/foundations.md`) es de origen europeo y norteamericano, y en APAC hay que asumir
   cobertura ADS-B de terceros o acuerdo con el operador local.


**Agregado en la tercera pasada del 2026-11-23 — el plano de pago agentic no mira a APAC, y eso
se registra como brecha, no como silencio.**

Se buscó específicamente cómo aterriza el pago agentic en los rieles domésticos que dominan la
región —el tipo de riel donde realmente se paga un viaje en China o India— y **no se encontró
ninguna fuente que lo trate**. Las cinco especificaciones del plano (`repos/foundations.md` →
*Plano de pago agentic*) son de origen estadounidense y están escritas alrededor de tarjeta y
stablecoin. **Ninguna documenta integración con los rieles de pago domésticos de APAC.**

**Por qué importa más acá que en ninguna otra región:** APAC es, por lejos, la región con mayor
adopción declarada de AI en travel de esta KB (**79% de las empresas de travel ya usan AI y 97%
planea hacerlo**, Expedia 2026). Es decir: **la región que más rápido va a pedir checkout
agentic es la que menos cubierta está por los protocolos que lo definen.** Para un engagement
APAC hay que asumir **integración con el proveedor de pago local como trabajo propio**, no como
algo que el protocolo resuelve — y presupuestarlo.

⚠️ **Esto es una brecha de búsqueda, no un hecho probado.** Significa "no se encontró
documentación", no "no existe". La verificación pendiente de mayor valor para APAC en el
próximo ciclo es ir a la documentación de los proveedores de pago dominantes de la región y
ver si publicaron soporte agentic.
**Agregado en la cuarta pasada del 2026-11-23 — visibilidad agentic: la región que etiqueta por
ley y que además escribe la herramienta.**

- **China etiqueta desde 2025 y fiscaliza en 2026.** Las medidas de etiquetado de contenido
  generado por AI están **vigentes desde el 2025-09-01** y exigen etiqueta **explícita e
  implícita** (la implícita va en los metadatos del archivo); la campaña **"Qinglang" de 2026**
  amplió la fiscalización *[fuentes secundarias de seguimiento regulatorio]*. Para un operador
  de travel que genera descripciones de destino o fotos de propiedad con AI para el mercado
  chino, **el etiquetado no es buena práctica: es requisito de publicación.**
- **Japón: *soft law*** con una ley marco que fija la estructura de política nacional, y
  propuestas legislativas para endurecerla sobre modelos fundacionales. **Singapur: no
  resuelto** — las fuentes se contradicen entre marcos voluntarios y un régimen de etiquetado
  obligatorio de dos niveles. **Se registra el conflicto en lugar de elegir una versión**;
  antes de comprometer alcance regulatorio en Singapur hay que confirmarlo contra la fuente
  oficial.
- **La herramienta del plano la está escribiendo APAC.** `yaojingang/GEOInflow` (MIT, 866★) y
  `GEORank` (Apache-2.0, 542★) —las dos piezas más estrelladas de analítica GEO self-hosted—
  se publican desde China, una de ellas junto al 北京日报社智源GEO. **Es el mismo patrón que la
  KB ya registró en el vertical: Asia tiene el código.**
- **Demanda que lo justifica:** 64% de los viajeros de APAC usa AI para planificar
  (Booking.com, enero 2026, 32.800 encuestados en 34 mercados); otra encuesta de la misma casa
  da 67%. *[cifras de proveedor — citar el rango y la fecha, no un número suelto]*

**Oportunidad:** *visibilidad con etiquetado nativo*. El pipeline de contenido que un cliente
de APAC necesita no es "generar descripciones": es **generar, etiquetar explícita e
implícitamente, y dejar registro**. Construirlo sobre GEOInflow/GEORank aprovecha herramienta
permisiva de la propia región.

#### Plano terrestre — medido el 2026-11-23

**Evidencia — la región con más pasajeros de tren del planeta y el piso de código más pobre.**

- **India:** `irctc api stars:>=20` devuelve **0**. No hay API pública oficial de IRCTC; lo que
  existe son *scrapers* comerciales de terceros que se promocionan explícitamente por saltear
  la cola de aprobación de IRCTC. El único MCP ferroviario de la región,
  `amith-vp/indian-railway-mcp` (28★), **no tiene ningún archivo de licencia** —declara MIT en
  `package.json`, que no es una concesión— y lleva **19 meses sin push**.
- **Japón:** `odpt tokyo transport open data` devuelve **0** repositorios con ese nombre. El
  perfil nacional GTFS-JP sí tiene actividad reciente pero minúscula: cuatro repos, **todos con
  0 estrellas**, el más reciente con push el 2026-11-23. Un repo del grupo mide justamente
  *"how often Japan's open GTFS bus timetables lapse"* — es decir, el problema medible de la
  región es la **caducidad de los feeds**, no su ausencia. Fuentes secundarias señalan además
  que el dataset oficial de JR East **excluye el Shinkansen**, y que el MCP comunitario japonés
  advierte en su propio README que su licencia MIT **no relicencia el dato del operador**.
  *[no verificado contra los portales de ODPT ni de JR East: no se consultaron en esta pasada.]*
- **Taiwán:** el repo mejor licenciado del plano terrestre de APAC es `SeanChangX/THSR-Sniper`
  (Apache-2.0 real, 38★) y **resuelve el captcha del operador por OCR**. Licencia impecable,
  comportamiento inadmisible en un entregable.
- **China y Corea: no examinados en esta pasada.** Se dice en vez de omitirse — 12306 y los
  agregadores locales son el mayor volumen ferroviario del mundo y esta medición no los tocó.

**Oportunidad:** *higiene y vigencia del feed antes que agente*. En Japón el trabajo con
demanda demostrada no es conversacional: es **monitoreo de caducidad y calidad de feeds
GTFS-JP**, construible sobre `MobilityData/gtfs-validator` (Apache-2.0, 434★) y la Mobility
Database (Apache-2.0, 354★). En India la oportunidad es **anterior al software**: no hay dato
oficial al que conectarse, así que el trabajo vendible es el acuerdo de acceso, y recién
después el agente.

⚠️ **Lo que no hay que prometer en APAC:** nada construido sobre `indian-railway-mcp` (sin
licencia) ni sobre THSR-Sniper (elude un control de acceso). Son los dos repos que un buscador
pone primero y los dos que no se pueden entregar.



#### Sexta pasada 2026-11-23 — adopción, regulación y el plano de emisiones

**Adopción: la región que más usa IA en viajes.** Booking.com mide **64% de los
viajeros de APAC** usando herramientas de IA al planificar o durante el viaje.
Del lado empresarial, el informe *Future of APAC Travel 2026* de Expedia
reporta **79% de las empresas de viajes de la región ya usando IA y 97%
planeando hacerlo**. Agoda ubica cerca del **63%** la intención de uso para el
próximo viaje. Son las tasas más altas de las cuatro regiones.

**Players.** Phocuswright describe a las OTA chinas posicionándose para
exportar su modelo mobile-first —contenido, pagos, partnerships y ahora reserva
asistida por IA— **a APAC primero**. Trip.com reporta un crecimiento interanual
de **~400% en volumen de órdenes asistidas por IA**. Fliggy publicó su skill
`flyai` para agentes.

**Regulación — brecha explícita, no silencio.** Las búsquedas de esta pasada
**no encontraron regulación de IA específica para viajes en APAC**. Lo único
cercano es una sanción del regulador de mercado chino (SAMR) a Trip.com Group
por infracción antimonopolio — que es **competencia, no IA**. Quien planifique
un engagement regional debe asumir **diversidad regulatoria por país** (China,
Japón, Singapur, India tienen marcos de gobernanza de IA distintos y en
movimiento) y resolverlo país por país, no con una política regional única.

**Emisiones — el calendario que se movió.** Singapur es el caso más concreto y
el más citado con fecha equivocada:

| Jurisdicción | Medida | Fecha real |
|---|---|---|
| **Singapur** | Objetivo SAF del 1% | **Movido de 2026 a 2027** |
| **Singapur** | Tasa al pasajero que lo financia | Billetes vendidos desde **1 oct 2026** |
| **Singapur** | Primer uplift de SAF | Objetivo **mediados de 2027** |
| **Japón** | 10% de SAF para vuelos de salida | **Objetivo a 2030**, detalles de aplicación aún en desarrollo |

⚠️ La tasa al pasajero de Singapur **empieza antes que el mandato de
combustible**: hay más de medio año en que el billete ya la cobra y el SAF
todavía no vuela. Eso es un problema de **explicabilidad en el punto de venta**
—por qué el billete subió sin que cambie nada visible— y es exactamente el tipo
de cosa que un agente tiene que poder responder con una cita, no con una
estimación.

#### Séptima pasada 2026-11-23 — plano de accesibilidad

**Regulación.** Japón: la reforma de la *Act for Eliminating Discrimination
against Persons with Disabilities* volvió **obligatorio** para empresas
privadas, desde el **1-04-2024**, el ajuste razonable a pedido de la persona —
antes era deber de mejor esfuerzo. Alcanza la relación con clientes, no sólo
con empleados (Libro Blanco de la Oficina del Gabinete). **No se encontró guía
específica para hoteles** en los resultados; el lugar a revisar es MLIT.

**Brecha escrita.** No se encontró, para este plano, regulación de
accesibilidad digital o física específica de viaje en **Australia, Singapur,
India, Corea ni China** con las búsquedas de esta pasada. **No significa que
no exista**: significa que esta sesión no la encontró y no la afirma.

**Oportunidad.** El ajuste razonable japonés es **a pedido y tras diálogo**:
el sistema tiene que poder **recibir** el pedido de accesibilidad del huésped
en la reserva y llevarlo hasta la operación. Eso es exactamente lo que
`AccessibilityRequirement` y `DisabilityServices` de OpenTravel modelan y lo
que un agente conversacional puede capturar bien — siempre que no lo resuma en
texto libre.

*Agregado en la octava pasada del 2026-11-23 — plano de la reseña:*

**Regulación — y es la región que regula la reseña por un eje distinto al europeo.**
- **China, jun-2026:** reglas conjuntas del regulador del ciberespacio y el de mercado sobre
  reseñas engañosas en redes sociales. Dos obligaciones de diseño: la reseña que **incluye
  enlace de compra debe marcarse como publicidad**, y el creador debe **declarar cuándo la
  reseña se apoya solo en experiencia personal**. Además, las afirmaciones de función,
  rendimiento y calidad deben estar **ensayadas por instituciones acreditadas** contra norma
  nacional. *[encuesta CCA 2023, citada en la cobertura]* 55,7% de las cuentas de reseña
  difuminaban la frontera entre reseña y promoción y 35,7% eran sospechadas de fabricar
  contenido.
- **Corea del Sur, jul-2026:** la ley de redes de información y comunicaciones revisada obliga
  a plataformas como **Naver y Kakao** a ofrecer vías de denuncia de información falsa o
  manipulada y a **publicar informes de transparencia cada seis meses**. Sumado al etiquetado
  de AI generativa vigente desde ene-2026.
- **Japón:** **no se encontró norma vinculante sobre reseñas falsas**; las guías de AI siguen
  siendo voluntarias. **Se escribe la ausencia**: es la jurisdicción donde el argumento
  comercial tiene que ser reputacional, no de cumplimiento.

**Oportunidad.** El eje chino —**divulgación**, no detección— es el más barato de implementar y
el que ningún producto occidental trae de fábrica: **etiquetar el origen y la base de cada
reseña y de cada resumen** (experiencia propia / incentivada / con enlace comercial). Es
metadato, no modelo. Y el informe semestral coreano convierte la traza de la Receta 23 en un
**entregable periódico contratable**, no en un proyecto de una vez.

#### Plano del equipaje — APAC (2026-11-23)

**La única región donde el rastreo de equipaje es una obligación regulatoria nacional — y no
existe una sola capa abierta para cumplirla.** Es la contradicción más fuerte que esta KB midió
en nueve planos de este vertical.

| Elemento | Qué dice | Confianza |
|----------|----------|-----------|
| Mandato CAAC (China) | **RFID obligatorio** para aeropuertos con más de **10 millones de pasajeros/año**, implementación originalmente apuntada a 2021 | Fuente secundaria |
| Expansión posterior | La política se amplió a **todas las rutas domésticas** y a aeropuertos regionales **pequeños y medianos** | Misma fuente secundaria |
| Texto regulatorio de la CAAC | Pide *"new technologies on baggage tracking"* y **"establish a whole-process tracking mechanism for checked baggage"** | Citado del propio texto de la CAAC |
| Capa abierta disponible | `rfid asset tracking stars:>=50` → **0 repos en todo GitHub** | Medido |

**Hay mandato y no hay código.** Un operador chino obligado a rastrear por RFID no tiene ninguna
opción open source con tracción: compra a proveedor o construye desde cero. En términos de la ley
estructural de esta KB, es el caso más puro de *el piso open source cubre la matemática y se
detiene en el compromiso* — solo que acá ni la matemática está cubierta.

**Y la región con el equipaje mejor manejado del mundo:** SITA mide en Asia-Pacífico la **tasa más
baja (3,41 por 1.000)** y el **costo más bajo por pieza (USD 210)**. Es el contraejemplo que
conviene tener a mano: la región con el mandato más duro tiene también el mejor desempeño, lo que
sostiene el caso de negocio del rastreo mucho mejor que cualquier proyección de proveedor.
(**Ojo:** esta cifra de 3,41 es la candidata más probable a ser el "3,4 global" discrepante
registrado arriba en *El costo del equipaje*.)

**Adopción de la Resolución 753, con las dos cifras que circulan y que no son comparables:**

- Un resumen basado en SITA dice que el rastreo bajo la Resolución 753 **superó el 50% de la
  industria**, con cumplimiento total apuntado a **2027**.
- Una cifra más antigua de una encuesta de IATA citada por un proveedor dice que **44%** de las
  aerolíneas lo tenían plenamente implementado y **41%** en progreso.
- Adopción de RFID específicamente: **27% general, 54% en mega aeropuertos**.
- **Miden cosas distintas en años distintos. No se restan ni se comparan.**

**India — la brecha, escrita en lugar de omitida:** se buscó una regla de la **DGCA** de 2026
sobre rastreo de equipaje y **no existe en las fuentes consultadas**. Lo que devuelve la búsqueda
de DGCA y equipaje son **baterías de litio** (celdas de 2 a 100 Wh en cabina con aprobación de la
aerolínea; bajo 2 Wh prácticamente sin restricción, consistente con el marco IATA), y de fuente
secundaria. **India tiene el crecimiento de tráfico y no tiene la norma de custodia.**

**Otros datos de la región:** el aeropuerto de Bangkok introdujo **inspecciones manuales de
equipaje desde el 16-oct-2026** (es control de seguridad, **no** rastreo — no mezclarlos).
Booking.com mide entre **60% y 67%** de viajeros APAC usando IA para planificar según el estudio;
Criteo señala a la región con **la mayor adopción de planificación de viaje asistida por IA de
punta a punta**. Las OTA chinas están exportando sus ecosistemas mobile-first con IA al resto de
Asia-Pacífico; Fliggy lanzó su *AI agent travel skill*. El regulador de mercado de China determinó
que **Trip.com Group violó la ley antimonopolio** — no es específico de IA, pero pesa sobre el
poder de plataforma en la región.

**Oportunidad Globant en APAC, este plano:** **la capa de cumplimiento de la Resolución 753 para
un operador con mandato CAAC.** Es el único lugar del vertical donde el comprador tiene una
obligación legal, ningún open source con tracción para cumplirla, y un KPI publicado contra el que
medirse. `jetway` (MIT) aporta el modelo de mensaje y de expediente; el lector RFID y el AODB no
existen abiertos y hay que integrarlos o construirlos — **y eso hay que decirlo en la propuesta,
no después**.


#### El plano del precio — APAC (2026-11-23, décima pasada)

**APAC es la única región del mundo que ya multó a una empresa de viajes por sus algoritmos de
precio.** En los nueve planos anteriores de este KB, APAC aportaba un mandato técnico (RFID de la
CAAC) o un estándar; acá aporta jurisprudencia aplicada con cifra.

| Elemento | Dato | Fuente |
| --- | --- | --- |
| Norma de plataforma | *Internet Platform Pricing Conduct Rules*, emitidas por tres organismos en **diciembre de 2025** | Resúmenes legales (stellagent, lome.legal) |
| En vigor | **2026-04-10**, por un plazo de **cinco años** | ídem |
| Qué prohíbe | Recortes de precio forzados; compromisos obligatorios de «precio más bajo de internet»; igualación automática de precio obligatoria; y **discriminación de precio basada en dato no divulgada** | ídem |
| Medidas de comercio online | SAMR + Administración del Ciberespacio; en vigor a comienzos de **febrero de 2026**; prohíben usar big data para precio discriminatorio **contra clientes frecuentes** | Global Times |
| Base de privacidad | PIPL **art. 24**: prohíbe la diferenciación injustificada en condiciones de transacción | Yucheng IP |
| Enforcement travel | SAMR abre investigación antimonopolio a **Trip.com** en **enero de 2026** | SCMP |
| La decisión | Reportada con fecha **2026-07-25** y multa de **RMB 5.200 millones**: abuso de posición dominante por **imponer exclusividad y paridad de precio a los hoteles mediante algoritmos** y herramientas de ajuste automático | Slaughter and May (título), SCMP |
| Norma sectorial | Un aviso del mercado turístico nombra explícitamente la discriminación de precio por big data, junto con publicidad falsa y regulación de OTA | lexchina |

> `www.slaughterandmay.com` **no resuelve desde esta red**; la cifra de RMB 5.200 millones y la
> fecha del 2026-07-25 vienen del título del artículo tal como lo devolvió el buscador y de la
> cobertura de SCMP, **no de la decisión de SAMR leída**. Se registra como secundario coincidente.

**Lo que esta decisión le hace a una arquitectura, y es concreto.** La conducta sancionada no fue
«cobrar distinto»: fue **imponer paridad de precio a los hoteles por algoritmo**. Es decir, la
cláusula de paridad —que en EMEA ya venía cayendo por vía de competencia— en China quedó sancionada
*como ejecución algorítmica*. Para quien construye una plataforma de distribución, el efecto es que
la paridad deja de ser una regla de negocio configurable y pasa a ser **una conducta que el código
ejecuta y que un regulador puede leer en el código**. El repo que monitorea paridad
(`mtnrabi/travel-agent-skills`, MIT) deja de ser una herramienta comercial inocente y pasa a ser,
en esta jurisdicción, un registro de conducta.

**Lo que la región aporta además, y que no es regulación:** el único *skill* de precio dinámico
permisivo y con tracción real que encontró esta pasada es de una empresa taiwanesa —
`asgard-ai-platform/skills`, MIT, **249★**, categoría interna «WP-39 定價演算法». El precio también
se está distribuyendo como *skill*, igual que el inventario en la tendencia 7 de este KB.

**Adopción, con la cautela de siempre:** 64% de los viajeros de APAC usa AI al planificar o durante
el viaje (Booking.com); del lado empresa, Expedia reporta 79% ya usando y 97% planeando usar
(**ambos estudios de marca**). Trip.com reporta ~+400% interanual en volumen de órdenes asistidas
por AI en TripGenie (dato de la propia compañía).

**Oportunidad Globant en APAC, este plano:** la **aserción de no-paridad y no-discriminación como
salida del motor**, no como política escrita. Un operador que vende en China necesita poder mostrar,
por transacción, que el precio no se fijó por frecuencia del cliente y que no se impuso paridad al
proveedor. Eso es un artefacto de datos derivado del mismo evento de precio que alimenta Nueva York
y la CRD — y es la pata que convierte la Receta 30 en una sola pieza de cuatro salidas.


#### Comprobante fiscal — la región donde no facturar bien cuesta crédito fiscal (undécima pasada, 2026-11-23)

**Evidencia.** Todas las fechas de cobertura secundaria, **no de los textos oficiales de CBIC,
IRAS o LHDN**:

| Jurisdicción | Estado | Detalle |
| --- | --- | --- |
| **India** | Vigente | Facturación con turnover ≥ **INR 5 crore** debe registrar cada factura B2B en el IRP y obtener **IRN + QR**. ⚠️ **Sin IRN válido, India niega el crédito fiscal (ITC)**: la factura mal emitida aumenta el impuesto a pagar, no sólo incumple |
| **Singapur** | En despliegue | **2026-04-01**: todos los nuevos registrados voluntarios de GST envían los datos de factura a IRAS por **InvoiceNow**. Extensión por tramos a **todos** los registrados hasta **abril de 2031** |
| **Malasia** | Vigente, por tramos | **MyInvois** desde agosto de 2024 para los más grandes; **desde enero de 2026** para los de facturación anual sobre **RM 1 millón**. Modelo de reporte **en tiempo real con validación de LHDN** |

**El hecho travel-específico de la región.** Según un blog sectorial indio (⚠️ secundario, conviene
confirmar con CBIC/GSTN): en hoteles, **la reserva corporativa B2B y la factura de banquetes a una
empresa sí llevan e-invoice**, mientras que **la cuenta B2C del huésped particular no**. Es decir:
el mismo hotel, el mismo día, emite dos tipos de documento según quién sea el comprador — y **el
agente que reserva es el que define cuál de los dos va a salir**, porque es quien pasa (o no) el
GSTIN del comprador.

**Lo que hay de código, y es poco para el tamaño del mandato.** Dos MCP de la familia
(`mcp-einvoicing-in`, 1★, y `mcp-invoicenow-sg`, 0★, los dos Apache-2.0, push del 2026-11-21/22) y
`ansh-devs/zoho-books-sdk` (MIT, 1★, 2026-11-06) que incluye GST e IRN. **De Malasia (MyInvois) no
se localizó ninguna biblioteca ni MCP open source**: es el mandato más agresivo de la región —
validación en tiempo real— y **la región no tiene capa open source propia que lo cubra**. Gap
declarado.

**La oportunidad.** El argumento comercial de APAC no es compliance, es **dinero**: en India, una
factura sin IRN válido **no es un incumplimiento formal, es crédito fiscal perdido**. Eso convierte
el adaptador de identidad fiscal en la reserva (Receta 31) en un caso de negocio aritmético, igual
que los USD 260 por pieza del plano del equipaje: el GSTIN que el agente no pasó se paga en ITC
negado. Y el motor de validación en tiempo real que Malasia exige es la variante de la Receta 32
con el estado *«aceptado por la autoridad»* como requisito previo a confirmar la operación.

**Gaps declarados de la región:** no se localizó fuente sobre cómo afecta el mandato a hoteles o
agencias de viaje **de Singapur o de Malasia** en particular, ni material sobre la conciliación
transfronteriza de una factura de viaje india facturada a Singapur o Malasia. No se localizó
biblioteca open source de MyInvois. **Las tres ausencias están escritas, no silenciadas.**

**El plano del seguro en APAC (2026-11-28, duodécima pasada): la región con la regla más dura del
mundo para un flujo agentic — y la única que ya envió código vertical.**

**India: la norma más específica del planeta para un agente que reserva.** La circular de **IRDAI
vigente desde el 1-10-2019** (dictada bajo el art. 34(1) de la Insurance Act, 1938) establece que
los portales y apps de viaje:
- **no pueden traer la cobertura preseleccionada** — el *pre-selection of policy* está prohibido;
- deben ofrecer **opt-out / deselección antes de concluir la transacción**;
- deben mostrar **nombre de la aseguradora y monto de prima** como costo de la cobertura, **y la
  tasa de impuesto aplicable**;
- para viaje **doméstico**, no pueden cobrar prima con más de **90 días** de anticipación al inicio
  del riesgo (para **internacional** esa restricción **no** aplica, y la cobertura al exterior
  puede emitirse en cualquier momento).

Es la única jurisdicción medida en esta KB donde **la regulación dicta la interfaz**, no el
resultado. Un agente que «ayuda» agregando la cobertura por conveniencia **incumple por diseño**.

⚠️ **Y un segundo límite indio que un agente puede violar sin saberlo:** la compra de seguros de
aseguradoras del exterior por residentes en India **está prohibida**, salvo aprobación general o
específica del RBI (guía Chambers 2026). Un agente que derive a un viajero indio a una aseguradora
extranjera puede estar empujando una operación de **control de cambios**, no sólo una venta no
licenciada.

**Siniestralidad medida (la única del plano, y de un solo proveedor):** siniestralidad incurrida de
viaje al exterior en India **66,35% (2021) → 41,59% (2023) → 49,45% (2025)**; doméstico cerca del
**11,62%** *(**[sin verificar]** — un único vendor)*.

**Singapur y Japón, con sus contradicciones declaradas.** El **MAS** publicó sus **Guidelines on
Artificial Intelligence Risk Management el 7-10-2026**, y cubren explícitamente **AI convencional,
generativa y agentes de AI**, con enfoque basado en riesgo y la expectativa de distinguir de forma
documentada la asistencia rutinaria de la decisión de alto impacto. ⚠️ **Las fechas de exigibilidad
se contradicen entre fuentes** (una dice vigencia 7-10-2027; otra, cumplimiento desde octubre de
2027 e implementación plena en octubre de 2028), y **no se pudo determinar** si reemplazan, enmiendan
o conviven con los principios **FEAT de 2018**. La **FSA japonesa** publicó el **AI Discussion Paper
v1.1 el 3-3-2026**; el documento está en japonés y **no se localizó su contenido sobre distribución
de seguros**: se reporta su existencia, **no su contenido**.

**La región que ya envió código vertical, y es el hallazgo de la pasada para APAC.** Tres de los
repos más relevantes del plano son de APAC:
- `10Life/10life-travel-mcp` (Hong Kong, 2026-10-22): comparador single-trip **read-only**, el más
  explícito del mundo en autolimitarse («premiums and scores are indicative, **the product page is
  the authority**»), prohíbe PII en el parámetro de razón de llamada y topea en 5 planes por
  respuesta. ⚠️ **sin archivo de licencia**, y es un manual de conexión a un endpoint remoto.
- `kentaroajisaka/labor-law-mcp` (Japón, **MIT, 67★ 8f**): el MCP de seguros **más estrellado que
  existe**, y **no sirve un producto: sirve la ley** (derecho laboral y de seguridad social, API
  e-Gov y 通達 del MHLW). La forma que gana tracción es *el agente consulta la regla*.
- Dos *Agent Skills* MIT en chino (`Zenine/china-family-insurance` 2026-11-20,
  `xuyue9129-ctrl/medical-insurance-product-research` 2026-10-28), los dos **autolimitados en el
  README** y el segundo con **SHA256 y grado de evidencia A/B/C/D** por documento.

**Lo que se mueve en producto.** **Southern Cross Travel Insurance (Australia/Nueva Zelanda)** paga
un voucher de **NZ$50 por viajero asegurado con demora de 2 horas y sin radicar reclamo**, y reportó
que en sus primeros tres meses **cerca de 200 vuelos** cruzaron el umbral entre julio y septiembre
de 2026.

**La oportunidad.** APAC es donde el entregable es **la interfaz, no el modelo**: el widget de
*ancillary* que cumple la regla india (nada tildado, tres datos visibles, opt-out antes del botón
final) es la **Receta 35, paso 2**, y es replicable a cualquier OTA de la región. Y el pipeline de
investigación de producto con evidencia hasheada —el patrón del skill chino— es la pieza de método
que la región ya probó y que ningún competidor occidental está copiando.

**Gaps declarados de la región:** no se midió el seguro de viaje de **China continental** desde la
óptica de las grandes OTA (Trip.com/Fliggy); no se localizó material sobre **Malasia, Indonesia,
Tailandia ni Corea** en este plano; y de la FSA japonesa se tiene la existencia del documento y no su
contenido. **Las cuatro ausencias están escritas, no silenciadas.**

### LATAM

**Evidencia — y aquí la narrativa ha ido por delante de los datos durante tres industrias
seguidas en esta red de KBs, así que se separa lo medido de lo afirmado.**

Lo que está documentado y es verificable:
- **Perú: 14/15-abr-2026** *(fecha corregida en la octava pasada del 2026-11-23; esta KB
  arrastraba 7-abr-2026)*. MINCETUR y PROMPERÚ integraron un asistente virtual de viaje con AI
  directamente en la plataforma oficial **Peru.travel** — descrito como el primer asistente
  conversacional de viaje oficial en una plataforma nacional de turismo de Sudamérica.
- **Chile: 15-sep-2026** *(⚠️ pendiente de reverificación — las búsquedas de la octava pasada
  no devolvieron fuente)*. Sernatur lanzó la **Chile Travel App** con asistente AI e información
  personalizada.
- **Argentina** *(⚠️ pendiente de reverificación — ídem Chile)*. El gobierno nacional anunció
  un planificador de viaje con AI para **Visit Argentina**, que arma itinerarios según
  intereses y tiempo disponible.
- **Regulación: 716 instrumentos regulatorios de AI en 23 países y territorios**, más del 80%
  iniciados desde 2023 (estudio 2026, Universidad de los Andes, Bogotá). La fragmentación, no
  la ausencia, es el problema.
- Brasil: marco de AI en trámite legislativo, de inspiración europea; **acuerdo Brasil–UE de
  regulación de AI y tecnología (jun-2026)**. Argentina: desregulación bajo Milei. Chile:
  proyecto basado en riesgo, **con su ley de protección de datos y su marco de ciberseguridad
  ya modernizados** — la infraestructura regulatoria previa a la AI es la más sólida de la
  región. Perú: ley de AI de 2023, actualizada en 2025, **y un agravante penal por uso de AI**
  en su código penal. Colombia: **CONPES 4144** (feb-2025) hasta 2030, orientado a capacidades
  y adopción más que a obligaciones horizontales inmediatas. **Uruguay firmó el convenio marco
  del Consejo de Europa sobre AI** — el único país de la región atado a un instrumento
  internacional vinculante, lo que lo vuelve la jurisdicción más predecible para un piloto
  regional.
- **Frontera: no se encontró tarjeta de llegada digital en Brasil.** Las fuentes consultadas
  solo registran e-visa para nacionalidades que antes requerían visa consular. **Se escribe la
  ausencia en lugar de omitirla:** a diferencia de APAC, el trámite previo digital todavía no
  es la norma en la región, así que la receta de "itinerario con tareas vencibles" tiene aquí
  menos superficie — por ahora.

Lo que circula y **no** se pudo verificar:
- *[sin verificar]* 54% de viajeros que ya usó AI para planificar (una sola encuesta citada por
  una fuente peruana).
- *[sin verificar]* Brasil 65,89 / Chile 63,19 / Uruguay 62,21 como únicos latinoamericanos en
  el top 50 global de AI readiness (un solo blog).
- *[sin verificar]* Mercado travel LATAM USD 109B → 196,6B (arrastrado de ciclos previos de
  esta KB sin fuente).

**La brecha medida, explícita.** La consulta `turismo viajes IA agente` sobre
`search/repositories` devuelve **1 repo con 0 estrellas**. No hay cluster open source de travel
en español ni en portugués. Lo más cercano es [`felipebasurto/viajante`](https://github.com/felipebasurto/viajante)
(MIT, 60★) — nombre en español, autor europeo. **El ecosistema open source de travel no habla
español.** Eso no es una carencia de la región: es el hueco más claro del vertical.

**Oportunidades.**
1. **El comprador es el Estado, y está comprando ahora.** Perú, Chile y Argentina desplegaron
   asistentes AI de turismo nacional en 2026, los tres en el mismo ciclo. Es un patrón
   replicable con referencia pública, no un pitch especulativo: el próximo ministerio de
   turismo de la región tiene tres vecinos que ya lo hicieron.
2. **Construir el cluster en español/portugués.** Con cero competencia open source medida, un
   skill o MCP de itinerario en español publicado bajo MIT se convierte en la referencia por
   defecto a coste casi nulo. Es la jugada de posicionamiento más barata de toda la KB.
3. **La fragmentación regulatoria es el servicio.** 716 instrumentos en 23 jurisdicciones hacen
   del cumplimiento multipaís un entregable en sí mismo para cualquier operador regional.
4. **Restricción real a diseñar alrededor:** las herramientas AI con precio en USD son caras
   para pymes con moneda devaluada. Un stack self-hosted (`photon`, `motis`, `headway`,
   modelo local) no es ideología: es la diferencia entre viable e inviable.
5. **La ventana del español se está cerrando, y hay fecha.** El 2026-11-21 esta KB midió que
   el ecosistema open source de travel no habla español. Dos días después,
   [`JourniOne-ai/JourniOne-Planning-Skills`](https://github.com/JourniOne-ai/JourniOne-Planning-Skills)
   llegó a **1189★ desde septiembre** con README en siete idiomas, **español entre los de
   lanzamiento**. Es un proyecto asiático que trata al español como mercado, no como
   traducción tardía. Dos lecturas, las dos accionables: (a) **la ventana sigue abierta** —
   ese repo **no tiene archivo de licencia**, así que nadie puede construir sobre él todavía;
   (b) **la ventana tiene fecha de cierre** — el argumento "no hay competencia en español"
   tenía 24 meses de vida en agosto y hoy tiene menos. Publicar el skill de itinerario en
   español bajo MIT **este trimestre** vale más que hacerlo el próximo.

6. **El plano de datos de vuelo es la entrada más barata de la región, y conviene decir con
   precisión qué se verificó y qué no.** Las dos piezas de referencia aeroportuaria que esta
   KB incorporó este ciclo **cubren LATAM sin costo de licencia y sin negociación**:
   [`davidmegginson/ourairports-data`](https://github.com/davidmegginson/ourairports-data)
   (**Unlicense — dominio público**, push el 2026-11-23) y
   [`mborsetti/airportsdata`](https://github.com/mborsetti/airportsdata) (**MIT**, con husos
   horarios). Para una región donde el costo en USD de las herramientas AI es una restricción
   real y declarada (punto 4), empezar por la capa de dato de dominio público —y no por una
   API medida por consulta— es una decisión de arquitectura con efecto presupuestario
   inmediato.

   **Lo que se buscó y no se pudo cerrar:** el dataset **VRA (Voo Regular Ativo) de la ANAC
   de Brasil**, que sería la fuente abierta de puntualidad y regularidad más relevante de
   LATAM. Se confirmó que el **Plano de Dados Abertos da ANAC 2026–2028 existe** y que el
   canal de publicación es `dados.gov.br`, pero **no se pudo confirmar desde este entorno la
   página del conjunto, su licencia, su periodicidad ni sus campos**. No se lista como
   hallazgo: se lista como **la verificación pendiente de mayor valor para LATAM en el
   próximo ciclo**. Si el VRA resulta estar bajo licencia abierta, LATAM pasaría a ser la
   única región de esta KB con dato de puntualidad abierto **y** reutilizable
   comercialmente — algo que ni North America ni EMEA tienen hoy (ver la advertencia sobre
   OpenSky en `repos/foundations.md`).


**Agregado en la tercera pasada del 2026-11-23 — pago agentic en LATAM: la misma brecha que
APAC, con una asimetría a favor.**

Igual que en APAC, **no se encontró ninguna fuente que trate cómo aterriza el pago agentic en
los rieles domésticos de la región**. Las especificaciones del plano no documentan integración
con rieles locales. Se registra explícitamente como brecha medida.

**La asimetría a favor, y es la única región donde aparece.** LATAM es, en esta KB, la región
donde **el Estado compra** (`intel/trends.md` → 9): Peru.travel, la Chile Travel App de
Sernatur y el planificador de Visit Argentina son asistentes **oficiales de turismo nacional**.
Ese comprador **no necesita el plano de pago en absoluto**: un asistente de turismo estatal
informa, recomienda y deriva — **no cobra**. Es decir que la región cuyo comprador principal
está menos cubierto por los protocolos de pago es también **la que menos los necesita para su
caso de uso dominante** (`compose/patterns.md` → Receta 6).

**La lectura comercial:** no vender pago agentic en LATAM como la punta de lanza. La punta es
el asistente de turismo nacional —que ya tiene tres precedentes de compra estatal— y el pago
entra después, con el operador privado, y con integración local presupuestada como trabajo
propio.
**Agregado en la cuarta pasada del 2026-11-23 — visibilidad agentic: la región donde el que
necesita ser citado es el Estado.**

- **Regulación: no hay regla de AI específica de la región, y se dice explícitamente.** En
  Brasil, el **PL 2338/2023 sigue sin ser ley**: aprobado por el Senado en diciembre de 2024,
  continúa en la Cámara de Diputados y a comienzos de noviembre de 2026 seguía esperando el
  dictamen del relator, sin fecha de votación; el PL 6.237/2025 del Ejecutivo quedó anexado.
  **Lo que sí rige hoy es la LGPD.** Sobre **México no se encontró fuente** de regulación de AI
  o de protección al consumidor aplicable a este plano: **es una brecha de esta pasada, no una
  ausencia confirmada.**
- **El comprador de la región ya está en producción.** `Peru.travel` incorporó un asistente de
  viaje con AI en **abril de 2026**, construido con tecnología de **Mindtrip**, presentado como
  el primer asistente oficial de un portal nacional de turismo en Sudamérica; Chile (Sernatur)
  y Argentina tienen equivalentes. Esta KB ya lo registra como *el Estado compra*
  (`intel/trends.md` → 9).
- **Por qué la visibilidad le pega distinto a ese comprador.** Un asistente estatal **informa y
  deriva, no cobra** — por eso no necesita el plano de pago (ver LATAM en la tercera pasada).
  Pero sí necesita exactamente lo contrario de lo que suele construir: **que los agentes de
  terceros —ChatGPT, Gemini, Perplexity— citen al portal oficial** cuando alguien pregunta qué
  hacer en Cusco. Hoy la inversión pública va al chatbot del portal; **el tráfico lo decide la
  cita en el agente ajeno.**

**Oportunidad, y es la más clara de la región:** *medición de citación para turismo nacional*.
Entregable: línea de base de cuántas veces el portal oficial es citado frente a OTAs y blogs,
por mercado emisor e idioma, con `elmohq/elmo` (MIT, self-hostable — importante para compra
pública) + emisión de `TouristAttraction`/`TouristDestination` sobre el inventario del ente.
**Es barato, es medible, y le da al comprador estatal justo lo que necesita para justificar la
partida: un número que sube.**

⚠️ **Brecha declarada:** no se encontró ninguna herramienta de visibilidad AI en español o
portugués, ni ningún repo del plano con autor LATAM. Las cinco piezas utilizables son de EE.UU.
y China. **El trabajo de localización es nuestro, y hay que presupuestarlo.**

#### Plano terrestre — medido el 2026-11-23, y aquí la región pierde su racha

**Evidencia — y esta vez la conclusión va en contra de la narrativa que esta red de KBs viene
registrando.** En las últimas pasadas LATAM **superó** su propia narrativa repetidamente (el KB
de retail documentó que el paso de transportista que mide cero en el mundo está resuelto para
seis países latinoamericanos en un solo repo MIT). **En el plano terrestre de travel no ocurre:
LATAM es el peor medido de las cuatro regiones, y el modo afectado es justamente el dominante.**

- El autobús interurbano es el medio de transporte intermunicipal principal de la región. Las
  consultas: `onibus passagem` → 53 repos, **los seis primeros con 0–2 estrellas y ninguno con
  licencia**, trabajos de materia; `rodoviaria passagem api` → **1 repo**, 0★, sin licencia,
  2024; `autobus boleto api` → **1 repo**, 0★, sin licencia, 2023; `gtfs latam brasil` → **0**.
- **La brecha no es solo regional: es global.** `bus ticketing system stars:>=100` devuelve
  **0 repositorios en todo el mundo**. Lo que distingue a LATAM no es que le falte código que
  otros tienen — **es que acá le falta al modo que mueve a la mayor parte de la población.**
  En EMEA el hueco de venta cae sobre el tren, que tiene al menos un estándar abierto que lo
  espera; acá cae sobre el bus, que **no tiene ni estándar ni código**.
- Cero servidores MCP de transporte terrestre con autor o cobertura LATAM, de ocho medidos.
- **Lo que sí hay es regulación, y es favorable.** En Brasil, la ANTT ya admite que los
  billetes y tarjetas de embarque se emitan y almacenen **exclusivamente en formato
  electrónico**, y la venta por sistema electrónico no presencial (internet, televenta) está
  permitida con carácter **facultativo** — no obligatorio. Hay una resolución de 2026
  (**Resolución ANTT nº 6.087, del 2026-08-14**) que modifica las condiciones generales de
  venta. *[fuentes: portal `anttlegis` vía búsqueda; **no se leyó el texto completo de la
  6.087/2026 en esta pasada** y su contenido sustantivo queda sin verificar. Verificar en el
  DOU antes de citarla.]* Un fallo del TRF1 de enero de 2026 habría prohibido a las empresas
  de fletamento vender pasajes individuales por aplicación sin autorización de la ANTT
  *[solo titular y resumen vistos]*.

**Oportunidad:** *el hueco más grande y más limpio del plano, y el que mejor encaja con la
posición de Globant en la región*. Hay **permiso regulatorio para el billete 100% electrónico**,
**demanda demostrada** (el crecimiento de venta digital de pasajes de ómnibus aparece en la
prensa sectorial de varios estados brasileños) y **cero software libre que ocupe el espacio**,
en ningún idioma. A diferencia de EMEA, acá no hay estándar que implementar: hay que **definir
el modelo de oferta** —y GTFS-Fares v2 es el único punto de partida abierto que existe, aunque
su validador (`TransitApp/gtfs-fares-v2-validator`, MIT) esté **archivado**.

⚠️ **Brecha declarada sin maquillaje:** no se encontró **ningún** repositorio de transporte
terrestre con autor LATAM, licencia válida y tracción mínima. En las últimas pasadas esta KB
pudo escribir lo contrario para otros planos. **Acá no, y registrarlo así es el punto:** la
narrativa "LATAM está más adelante de lo que se cree" es verdadera por plano, no en general, y
el plano terrestre es donde no se sostiene.



#### Sexta pasada 2026-11-23 — adopción, regulación y el plano de emisiones

**Adopción.** Un estudio patrocinado por Booking.com ubica a Latinoamérica
**liderando globalmente en familiaridad con la IA**, con **89%** de los
encuestados declarando que conocen la IA y cómo funciona. La cobertura de WTM
Latin America describe la adopción acelerada de IA ocurriendo **junto a nuevas
exigencias de seguridad y pagos digitales** — en esta región la preocupación
por el fraude es alta, y va pegada a la adopción, no separada de ella. Skift
argumenta que los hábitos de planificación intensivos en búsqueda preparan el
terreno para una adopción rápida del descubrimiento guiado por IA.

**Tamaño, con la cautela correspondiente.** MarketsandMarkets proyecta el
mercado regional de IA en turismo de **~93,7 M USD (2024) a ~372,6 M USD
(2029), 25,9% CAGR**. ⚠️ Es el nicho "IA en turismo", **no** el gasto total de
IA en viajes: no sirve para dimensionar un pipeline de plataforma.

**Players y movimientos de Estado.** El caso nacional más claro es **Perú**:
MINCETUR y PROMPERÚ integraron un asistente virtual de viaje con IA
directamente en la plataforma oficial **Peru.travel**. En el sector privado,
**Rappi** empujó su vertical de viajes en enero de 2026, con foco en lealtad,
personalización e IA.

**Regulación — brecha explícita.** Las búsquedas de esta pasada **no
encontraron regulación de IA específica para viajes en Latinoamérica**. La
única referencia regulatoria que aparece en la cobertura regional es el **EU AI
Act**, que es extrarregional. Para un engagement LATAM eso significa que el
marco aplicable sale de las leyes nacionales de protección de datos y de
consumidor, no de una norma de IA de viajes: hay que resolverlo país por país.

**Emisiones — lo que viene y todavía no está firme.** Brasil es el movimiento
relevante de la región, y las fuentes son finas e inconsistentes entre sí:

| Qué | Estado según fuentes de esta pasada |
|---|---|
| Mandato brasileño de SAF | Se espera que **entre en vigor en enero de 2027**; detalles aún sin publicar |
| Mecanismo brasileño | Descrito como **metas basadas en emisiones + book & claim** (cumplir comprando atributos de SAF usado en otro lugar) |

⚠️ **No verificado contra fuente primaria de gobierno.** Se registra como señal
direccional, no como fecha de compliance. Si un cliente brasileño planifica
sobre esto, hay que confirmarlo en la norma antes de comprometer alcance.

**Por qué book & claim importa técnicamente.** Si el cumplimiento se satisface
con atributos y no con combustible físico en el tanque, el sistema necesita un
**registro de atributos auditables separado del itinerario**: la emisión del
vuelo y el crédito aplicado son dos hechos distintos que no deben colapsarse en
un solo número. Un modelo de datos que guarde sólo "CO₂ del viaje" no puede
reportar esto.

#### Séptima pasada 2026-11-23 — plano de accesibilidad

**Regulación — Brasil tiene la regla más cuantitativa de las cuatro regiones.**
La *Lei Brasileira de Inclusão* (Lei 13.146/2015), art. 45, reglamentada por
el **Decreto 9.296/2018** (modificado por el Decreto 11.303/2022), exige a los
establecimientos hoteleros existentes **al menos 10% de dormitorios
accesibles, con mínimo de uno**, sobre rutas accesibles. Para los construidos
hasta 29-06-2004 el plazo era **3-12-2024** — **ya vencido**; esta sesión no
verificó prórrogas posteriores. Hay un proyecto (PL 3.835/23) que daría **50%
de descuento** a la persona con discapacidad si el hotel no tiene habitación
adaptada; **estado no confirmado**. El art. 63 de la misma ley obliga a la
accesibilidad de los sitios de empresas con sede o representación en Brasil.
⚠️ **Fuente secundaria:** `planalto.gov.br` no resuelve desde esta sesión.

**Brecha escrita.** México, Argentina, Chile y Colombia: **no se buscó en
detalle** regulación de accesibilidad turística en esta pasada. Queda
explícito para la próxima.

**Oportunidad — la más concreta del plano en cualquier región.** El 10% es
**contable contra el inventario del PMS**: cuántas habitaciones de la
propiedad tienen ficha accesible verificada sobre el total. Es un reporte de
cumplimiento que un grupo hotelero brasileño puede necesitar hoy, y que nadie
vende en open source. Receta 21.

*Agregado en la octava pasada del 2026-11-23 — plano de la reseña:*

**La ausencia, escrita primero.** Las búsquedas de este ciclo **no encontraron ninguna norma
específica sobre reseñas falsas en ningún país de LATAM** —ni equivalente a la Ley 34/2026
italiana, ni a la regla de la FTC, ni a las reglas chinas de divulgación—. Aplica el derecho de
consumidor general. **Es la única de las cuatro regiones sin obligación específica**, y hay que
decirlo así en una propuesta: acá el plano **no se vende por cumplimiento**, se vende por
conversión y por confianza, que es un argumento más difícil y de ciclo más largo.

**Lo verificado de nuevo en esta pasada, con una corrección.** El asistente de **Peru.travel**
(PROMPERÚ) se confirma por múltiples fuentes, con un dato que esta KB no tenía: **la tecnología
es de Mindtrip** —la misma empresa que el historial de esta KB registraba en el hito
Sabre+PayPal+Mindtrip—. **La fecha hay que corregirla**: el comunicado es del **14-15 de
abril de 2026**, no del 7-abr-2026 que esta KB venía arrastrando. El posicionamiento declarado
es "primer asistente conversacional de AI en una plataforma nacional de turismo de Sudamérica",
y su propósito explícito es **distribuir visitantes hacia destinos menos conocidos**.

**Lo que esta pasada NO pudo reconfirmar, dicho en voz alta.** Las búsquedas de este ciclo **no
devolvieron ninguna fuente** sobre la **Chile Travel App de Sernatur (15-sep-2026)** ni sobre el
planificador AI de **Visit Argentina (may-2026)**, los dos registrados en esta misma sección en
una pasada anterior. **No se borran ni se confirman**: quedan marcados como *pendientes de
reverificación*, y la próxima pasada de travel debería ir a los sitios oficiales de Sernatur y
de Visit Argentina antes de usarlos en una propuesta.

**Oportunidad.** El asistente de destino estatal es el patrón propio de la región —Perú
confirmado, Chile y Argentina por reverificar— y **ninguno de los tres puede citar una fuente
de confianza sobre un alojamiento privado**: un estado no puede recomendar un hotel por
reseñas que no controla. Eso vuelve a la **reseña con estadía probada** (Receta 22) la pieza
que un ente de turismo nacional podría exigir a su oferta inscripta para poder recomendarla.
**Es el único lugar del mundo donde este plano tiene un comprador público en lugar de un
regulador**, y es la clase de encargo que esta región ya demostró que compra.

#### Plano del equipaje — LATAM (2026-11-23)

**La región donde la norma de equipaje es la más explícita del mundo en el mínimo gratuito, y
donde el instrumento de 2026 que todos citan no es de equipaje.**

| Instrumento | Estado a 2026-11-23 | Qué cubre |
|-------------|---------------------|-----------|
| **Resolución ANAC 400/2016, art. 14** (Brasil) | **Vigente.** Confirmada como vigente en nov-2026 por varias fuentes | **Franquía mínima de 10 kg de equipaje de mano sin costo adicional.** Las medidas las fija cada compañía (lo más citado: 55×35×25 cm) |
| **Resolución ANAC 813/2026** | **En vigor desde el 26-oct-2026** (registro oficial de la ANAC) | **NO es equipaje.** Información, asistencia material y reembolso en demora y cancelación. Migalhas la llama *"retrocesso na proteção do passageiro aéreo"* |
| **Resolución ANAC 819/2026** | Nueva redacción del art. 20 vigente desde el **25-nov-2026** según **una sola fuente de terceros** | Sin confirmar en fuente oficial. **Se registra como no verificado** |
| **PL 5.041/2025** (Congreso) | **En tramitación.** Mientras no se apruebe y sancione, rige la Resolución 400 | Garantizaría expresamente **10 kg de mano + un objeto personal gratis** en vuelos domésticos e internacionales operados en Brasil |

> ⚠️ **La trampa de precisión de esta región, y es fácil de pisar.** La Resolución 813/2026 es el
> instrumento brasileño de 2026 del que habla toda la prensa de derechos del pasajero, entró en
> vigor hace cuatro semanas, y **no toca el equipaje**. Un informe que la cite como la norma de
> equipaje vigente está mal, aunque la fecha y el número sean correctos. **La norma de equipaje
> sigue siendo el art. 14 de la 400/2016.** (Una fuente menciona 12 kg en lugar de los 10 kg del
> PL 5.041/2025: divergencia registrada, no resuelta.)

**Y el dato que da el caso de negocio:** el **equipaje está entre los temas más reclamados** en la
plataforma Anac Passageiro en 2026, sobre un total reportado de **98.000 quejas** contra las
aéreas. Es demanda medida, no proyectada.

**Regulación de IA aplicada a viajes: ninguna, en ningún país de la región.** Se buscó
explícitamente y **no se encontró norma específica** — la única referencia regulatoria que
devuelven las búsquedas regionales es global (la Ley de IA de la UE). Es el mismo resultado que el
plano de la reseña registró en la octava pasada, **medido de nuevo con consultas distintas y con
el mismo resultado**. La ausencia queda escrita; no omitida.

**Adopción y players (2026):** un estudio patrocinado por Booking.com mide que **LATAM lidera
globalmente en familiaridad con IA**, con **89%** afirmando que sabe cómo funciona. Phocuswright
advierte que **cerca de la mitad** del crecimiento récord de reservas de 2025 vino del **tipo de
cambio, no de viajeros** — la cautela que esta KB ya tiene escrita y que se reafirma. En el sector
público, Peru.travel opera su asistente oficial (MINCETUR + PROMPERÚ, tecnología Mindtrip, fecha
ya corregida en la octava pasada a 14/15-abr-2026) y Chile tiene app con asistente, geolocalización
e información personalizada. Rappi empuja su vertical de viajes combinando lealtad,
personalización e IA (PhocusWire, ene-2026). MarketsandMarkets estima el mercado regional de IA en
turismo en **USD 93,7 M (2024) → ~372,6 M (2029)**: **estimación de proveedor**, etiquetada.

**El contraste que conviene tener a mano:** SITA mide en **África** la tasa más alta del mundo,
**12,1 por 1.000**, contra 4,9 global. No es LATAM, pero es la referencia que ordena cualquier
conversación sobre mercados emergentes y custodia de equipaje.

**Oportunidad Globant en LATAM, este plano:** un **verificador de franquía mínima contra el
sistema de la aerolínea** — el equivalente de equipaje a la Receta 21 (reporte del 10% de
habitaciones accesibles contra el PMS). La 400/2016 fija un piso de 10 kg **en la norma**, cada
compañía fija las medidas **en su tarifa**, y la brecha entre las dos es exactamente lo que se
reclama en Anac Passageiro. Con `carry-fit` (MIT) como base de medidas y el `pkg/dcs` de `jetway`
(MIT) como lado del operador, es construible con licencias limpias — y es el único plano de esta
región donde la obligación es **numérica y verificable** en lugar de interpretable.


#### El plano del precio — LATAM (2026-11-23, décima pasada)

**Este es el primer plano de los diez en que LATAM está dada vuelta respecto de sí misma.** En
frontera, equipaje, accesibilidad y derechos del pasajero, el hallazgo de este KB fue siempre el
mismo: *LATAM tiene la norma y no tiene el código* (art. 14 de la Res. 400/2016, los 10 kg; el 10%
de habitaciones accesibles; el Estado comprando). Acá es exactamente al revés: **el motor de precio
por AI ya está corriendo en aerolíneas de la región, y la norma que lo gobernaría no existe
todavía.**

**El despliegue, que ya ocurrió:**

| Operador | País | Qué desplegó | Fecha | Fuente |
| --- | --- | --- | --- | --- |
| Azul | Brasil | Motor de precio generativo de Fetcherr; **primer cliente en vivo** de Fetcherr. Un post de Fetcherr de **diciembre de 2025** afirma que fue la primera aerolínea en desplegarlo **a escala completa de red** | Piloto anunciado en 2024 (PR Newswire); escala declarada dic-2025 | Fetcherr (parte interesada) |
| Viva Aerobus | México | *Generative Pricing Engine* y *Large Market Model* de Fetcherr, para precio en tiempo real y publicación directa de tarifas | Alianza anunciada **mayo de 2024** | PhocusWire, accessnewswire |

> Las dos son **declaraciones del proveedor y del cliente**, sin cifras auditadas de resultado. Lo
> verificable es que el despliegue fue anunciado y que la región aparece en la lista de clientes de
> Fetcherr junto con Delta, WestJet y Virgin Atlantic. `fetcherr.io` **no resuelve desde esta red**,
> así que la lista de clientes no fue leída del sitio del proveedor.

**La norma, que todavía no existe.** No localicé **ninguna ley sancionada** sobre precificación
algorítmica en Brasil. Lo que hay son proyectos en trámite y una señal de fiscalización:

| Instrumento | Qué propone | Estado localizado |
| --- | --- | --- |
| PL 1309/2026 (Jadyel Alencar) | Límites a la precificación algorítmica en **bienes esenciales**; altera el CDC | Apensado al PL 385/2026; **devuelto al relator** en la Comisión de Defensa del Consumidor el **2026-05-15** |
| PL 1635/2024 | Incluir en el **art. 39 del CDC** la práctica abusiva de *colusión artificial por algoritmos de precificación* | En trámite |
| PL 5441/2025 | «Lei de Equidade Digital e Transparência Algorítmica»; fiscalización por **Senacon, ANPD y CADE**. Un texto para discusión del Senado lo llama **el más ambicioso** de los analizados | En trámite |
| ANPD | *Mapa de Temas Prioritários* 2026-2027, publicado en **diciembre de 2025**: la IA es uno de **cuatro ejes** de fiscalización | Vigente como plan, no como norma |

> La afirmación de que la ANPD lista la precificación dinámica entre las decisiones automatizadas de
> impacto significativo aparece **sólo en un blog sin cita de norma**, y por eso **no se afirma acá**.
> El llamado «CDC Digital» es **propuesta, no norma vigente**, y se registra así.

**La trampa de precisión de esta región, en línea con las pasadas anteriores.** Igual que la
Resolución ANAC 813/2026 no era de equipaje (noveno plano), acá el error fácil es presentar al CDC
como si ya resolviera el precio algorítmico. No lo hace de forma específica: lo que hay es el marco
general de práctica abusiva y publicidad engañosa, y análisis que sostienen que el precio dinámico
**es permitido pero encuentra límites severos** en el CDC. Afirmar más que eso es inventar la norma.

**Lo que esta asimetría significa para una propuesta, y es la parte accionable.** En las otras tres
regiones el cliente compra cumplimiento: hay una norma con fecha y el trabajo es satisfacerla. En
LATAM el cliente compra **opcionalidad**: el motor ya está desplegado y la norma llega después, con
tres proyectos que apuntan en la misma dirección (transparencia algorítmica, colusión por algoritmo,
fiscalización por ANPD/Senacon/CADE). Quien hoy registre la decisión de precio —entradas, versión,
*hash*, resultado— no tiene que reconstruir nada cuando el PL 5441/2025 o su sucesor se sancione.
Quien no, va a tener que explicar retroactivamente precios que ya cobró.

**Oportunidad Globant en LATAM, este plano:** el **registro voluntario de decisión de precio**
montado sobre un motor que ya está en producción (Receta 28 + la cuarta salida de la Receta 30). Se
vende hoy como gobierno de dato y defensa reputacional ante Senacon/Procon —no como cumplimiento,
porque no hay de qué cumplir todavía— y se convierte en cumplimiento el día que la ley salga. Es el
mismo argumento que la Receta 22 (sello de estadía verificada) pero sobre el precio: **invertir el
problema y tener la evidencia antes de que la pidan.** Para una aerolínea de la región que ya corre
Fetcherr, es lo único que su equipo legal no puede construir solo.


#### Comprobante fiscal — el primer plano de los once donde LATAM tiene la capa open source más fuerte (undécima pasada, 2026-11-23)

**El hallazgo de la pasada, y es una inversión de la ley de este KB.** En los diez planos
anteriores LATAM apareció como la región que compra, no como la que tiene el código: *«Asia tiene
el código; Europa tiene la regulación; LATAM tiene al Estado comprando»* (tendencia 9). **En el
plano del comprobante eso se da vuelta.** El repo horizontal fiscal más estrellado de todo el plano
es brasileño:

| Repo | Licencia (archivo leído) | Stars | Último push |
| --- | --- | --- | --- |
| [wmixvideo/nfe](https://github.com/wmixvideo/nfe) | **Apache-2.0** | **770** | **2026-11-23** |
| [TadaSoftware/PyNFe](https://github.com/TadaSoftware/PyNFe) | LGPL-3.0 | 599 | 2026-02-20 |
| [OCA/l10n-brazil](https://github.com/OCA/l10n-brazil) | AGPL-3.0 | 376 | **2026-11-23** |
| [nfewizard-org/nfewizard-io](https://github.com/nfewizard-org/nfewizard-io) | GPL-3.0 | 330 | 2026-11-08 |
| [OCA/l10n-mexico](https://github.com/OCA/l10n-mexico) | AGPL-3.0 | 20 | 2026-11-09 |

**770 + 599 + 376 + 330 estrellas de NF-e brasileña supera a cualquier capa fiscal regional de este
plano, incluida la europea.** La causa es histórica y es simple: Brasil obliga desde 2008, así que
la región tuvo dieciocho años para construir la capa que Europa empezó en 2024.

**La brecha interna de LATAM, medida.** Brasil 376★ en Odoo contra México 20★, y en CFDI lo que hay
es chico y disperso: `FiscalAPI/fiscalapi-net` (MPL-2.0, 69★), `bambucode/catalogos_sat_JSON` (82★,
**sin archivo de licencia**), `Timbrix/mcp` (MIT, 0★), `OrtaMarco/mx-fiscal-mcp-server` (MIT, 1★),
`cmendezs/mcp-cfdi-mx` (Apache-2.0, 0★). **`cfdi sat facturacion` devuelve 33 repos en total y
cuatro de los ocho primeros por estrellas no tienen archivo de licencia.** Brasil tiene ecosistema;
México tiene piezas.

**Regulación.** Brasil está en el **año de prueba de CBS/IBS**: 2026 con tasas testigo de 0,9% CBS
y 0,1% IBS y **sin recaudación**, pero con las obligaciones accesorias ya exigibles. ⚠️ **Las
fuentes discrepan sobre la fecha de NFS-e**: 2026-08-01, 2026-10-01 o 2026-12-01 según cuál; una
sitúa la exigibilidad de los documentos fiscales de CBS/IBS con sanciones **desde el 2026-08-01**.
**Ninguna fuente localizada trata hoteles en particular** — el hospedaje es un servicio, así que
caería bajo las reglas generales de NFS-e, pero eso es inferencia y se declara como tal. México
mantiene **CFDI 4.0 con Complemento de Pagos 2.0**.

**La oportunidad, y es la única región donde se puede vender «exportar» en lugar de «cumplir».**
LATAM no necesita que alguien le traiga un motor fiscal: lo tiene, es Apache-2.0 y tiene push de
hoy. Lo que necesita es lo mismo que las otras tres regiones —**el campo de identidad fiscal del
comprador dentro del flujo de reserva** (Receta 31)— más dos cosas propias:

1. **El módulo de hospedaje que le falta a `OCA/l10n-brazil`**, para que un PMS open source emita
   NFS-e de hospedaje correctamente bajo el régimen de 2026. Se publica como módulo Odoo AGPL,
   exactamente el patrón de la pasada cuarta de este KB.
2. **Exportar la madurez.** Un equipo brasileño que ya sabe NF-e es el que mejor puede implementar
   KSeF polaco, Verifactu español o InvoiceNow singapurense: **los esquemas cambian, el problema de
   *clearance* en tiempo real contra una autoridad fiscal es el mismo que Brasil resuelve desde
   2008.** Es el primer argumento de esta KB donde la experiencia regional de LATAM es el activo
   que se vende a EMEA y APAC, y no al revés.

**Gap declarado de la región:** no se localizó nada sobre facturación electrónica de viaje en
**Chile, Argentina, Colombia ni Perú** en esta pasada, pese a que los cuatro tienen regímenes de
documento electrónico vigentes. Las búsquedas de repos de esta pasada no los alcanzaron. **Queda
escrito como lo que falta medir, no como ausencia de mandato.**

**El plano del seguro en LATAM (2026-11-28, duodécima pasada): la región tiene el régimen y, esta
vez, no tiene el código.**

**Lo que está documentado y es verificable.**
- **Brasil, Lei 15.040/2024 («Marco Legal dos Seguros»)**, la primera ley integral de contrato de
  seguro de la región. Lo relevante para un agente: el asegurado **accede a los documentos que la
  aseguradora usó en la regulación del siniestro**, salvo los protegidos por sigilo legal, y la ley
  fija **plazos objetivos** para el análisis de propuestas y reglas uniformes de formación, vigencia
  y extinción del contrato. ⚠️ **Vigencia en conflicto entre fuentes: la mayoría de los análisis
  jurídicos indica el 11-12-2025 (art. 134: un año después de la publicación), mientras la Agência
  Câmara tituló la entrada en vigor el 10-12-2024, que parece un error de la propia agencia.
  Conflicto registrado y no resuelto.** Tampoco se localizó el plazo de regulación de siniestro en
  días.
- **Open Insurance (OPIN) sigue siendo prioridad regulatoria y no despegó.** El Plano de Regulação
  2026 de SUSEP (aprobado por **Resolução Susep nº 72/2025**) incluye la **revisión de la
  regulación de Open Insurance**, y hay normas en movimiento sobre el ecosistema de compartición y
  el **Registro de Operações (SRO)**, con APIs estandarizadas, consentimiento explícito y alcance
  versionado *(análisis de tercero, autoridad incierta — **[sin verificar]**)*. Del otro lado:
  reporte sectorial de junio de 2026 señala **2 SPOCs autorizadas a abril de 2026, baja demanda y
  fricción en la jornada del cliente**.
- **Prima del ramo:** **R$ 965 millones** de primas de seguro de viaje en Brasil en 2024 (HelloSafe
  citando SUSEP vía CNSEG).
- **Adopción de AI en la región:** mercado de AI en turismo de LATAM **~USD 93,7 millones (2024) →
  ~USD 372,6 millones (2029), CAGR ~25,9%** (market vendor); y **89% de familiaridad del consumidor
  con AI, el más alto del mundo** — ⚠️ **estudio patrocinado por Booking.com**, tratar como color.
  Casos de Estado: **Perú** integró un asistente AI en la plataforma oficial `peru.travel` en abril
  de 2026, **Chile** tiene app nacional con asistente, y **Rappi** está armando oferta de viaje con
  loyalty y AI.

**El contraste con la undécima pasada, y es el hallazgo regional.** En el plano del comprobante,
LATAM tenía **la capa open source más fuerte del mundo** (`wmixvideo/nfe`, 770★, Apache-2.0, push
del día) porque Brasil obliga desde 2008. Acá **se invierte**: Brasil tiene el régimen más ambicioso
de la región —OPIN, con APIs estandarizadas y consentimiento, más una ley de contrato nueva— y lo
que hay de código abierto es **un (1) repositorio**: `luciano-coelho/opin-doctor-ppgcc-ufsc` (**MIT**,
creado 2026-07-20, push 2026-11-24), un entorno local completo de OPIN —gateway mTLS, Authorization
Server— publicado **desde un posgrado de la UFSC, con 0★**. ⚠️ Y su archivo MIT dice «Copyright (c)
2025 **Open Insurance Brasil**», una entidad que **no es la que publica el repo**: la licencia es
legítima y la **procedencia no es verificable** (cuarto modo de trampa de licencia de esta KB).

**La oportunidad, y es la más limpia del plano.** **Open Insurance es un riel de distribución que
nadie construyó del lado del agente.** Existen el consentimiento, las APIs estandarizadas y el
registro de operaciones; no existe **un cliente OPIN-nativo de seguro de viaje**. Y el problema de
adopción que reporta el sector —baja demanda, fricción en la jornada— es **exactamente** el problema
que un agente resuelve: el consentimiento OPIN es un flujo tedioso para un humano y trivial para un
agente que ya tiene el contexto del viaje.

El entregable concreto: un cliente OPIN de viaje que (a) use el consentimiento explícito como
mecanismo de autorización, (b) **cotice y no bindee** (Receta 34), y (c) conserve el expediente
exportable al asegurado que la Lei 15.040 vuelve derecho —no buena práctica— (**Receta 35, paso 5**).
`opin-doctor` sirve de entorno de desarrollo local, que es justo lo que falta para empezar sin
homologación.

**Gaps declarados de la región, y uno es llamativo:**
1. No se localizó **ningún lanzamiento de seguro paramétrico de viaje en LATAM**, mientras que esta
   misma pasada midió cuatro en EMEA, North America y APAC (Cover-More, Aviva, Medavie, SCTI). Es
   una **ausencia medida**, no una afirmación de que no exista.
2. No se localizó regulación de seguro de viaje de **México (CNSF), Chile, Argentina, Colombia ni
   Perú** en esta pasada.
3. **Cero repositorios** de seguro de viaje de cualquier país de LATAM, más allá del repo académico
   de OPIN.

## Posicionamiento Globant

1. **Vender la brecha planificación→compra, no "un agente que reserva".** 52/2 en EE.UU.,
   8% de confianza para completar reservas. El entregable honesto termina antes del pago, o lo
   entrega al merchant of record.
2. **Neutralidad de protocolo como habilidad central.** IATA no emitió estándar agentic; MCP
   está en la Linux Foundation; UCP y los MCP propietarios de cada GDS conviven. El cliente
   no necesita que elijamos: necesita no quedar atrapado.
3. **Empezar en la plataforma, no en el framework.** El crecimiento está en plataformas
   verticales que ya traen su MCP (TREK, Kamra, HAIP, OTAIP). La capa agentic se enchufa.
4. **La licencia es arquitectura.** Los tres repos más grandes del vertical son copyleft
   (TREK AGPL-3.0, QloApps OSL-3.0, Kamra AGPL-3.0); los permisivos son la infraestructura.
   Plataforma copyleft como servicio separado + lógica propietaria del cliente en los
   componentes permisivos. Esto se decide el día uno o se paga en la auditoría legal.
5. **Donde no hay open source, hay producto.** Cero resultados medidos en revenue management,
   NDC, ERP de agencia, predicción de demoras, alquiler vacacional **y ahora también APIS,
   PNR, ETIAS, biometría de embarque y reglas de admisión** (medido el 2026-11-23, ver
   `repos/foundations.md`). Ahí pertenece la IP propietaria de Globant, con la evidencia de la
   brecha como argumento de venta.
6. **El plano de frontera es la excepción permisiva del vertical, y conviene entrar por ahí.**
   En todo travel, la plataforma es copyleft y la infraestructura permisiva. El documento de
   viaje rompe el patrón: **lectura de chip (MIT), MRZ (MIT y Apache-2.0), pruebas ZK (MIT y
   Apache-2.0) y el verificador del wallet europeo (Apache-2.0)**. Es el único lugar donde se
   puede armar una capacidad completa sin una sola línea de copyleft, con un regulador
   manteniendo parte del código. Para un primer engagement con restricción de licencia dura,
   es la entrada de menor fricción legal del vertical.
7. **Toda licencia lleva fecha.** Kamra PMS pasó de AGPL-3.0 a Apache-2.0 en 48 horas, entre
   dos ciclos de esta KB. Una licencia verificada no es un hecho permanente: es una medición.
   Esto vale para las 12 industrias de esta red, no solo para travel.

---
*Investigado globalmente y una vez por región el 2026-11-21; ampliado con el plano de frontera
e identidad, también una vez por región, el 2026-11-23. Las cifras sin fuente primaria
localizable están marcadas **[sin verificar]** a propósito, y los límites de alcance del
entorno de ingesta están declarados arriba en lugar de omitidos.*
