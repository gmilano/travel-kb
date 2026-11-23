---
industry: travel
region: Global
updated: 2026-11-23
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

### LATAM

**Evidencia — y aquí la narrativa ha ido por delante de los datos durante tres industrias
seguidas en esta red de KBs, así que se separa lo medido de lo afirmado.**

Lo que está documentado y es verificable:
- **Perú: 7-abr-2026.** MINCETUR y PROMPERÚ integraron un asistente virtual de viaje con AI
  directamente en la plataforma oficial **Peru.travel** — descrito como el primer asistente
  conversacional de viaje oficial en una plataforma nacional de turismo de Sudamérica.
- **Chile: 15-sep-2026.** Sernatur lanzó la **Chile Travel App** con asistente AI e información
  personalizada.
- **Argentina.** El gobierno nacional anunció un planificador de viaje con AI para
  **Visit Argentina**, que arma itinerarios según intereses y tiempo disponible.
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
