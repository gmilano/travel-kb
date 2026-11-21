---
industry: travel
region: Global
updated: 2026-11-21
---

# 🗺️ Mapa de mercado — Travel & Hospitality

> Key players, oportunidades y posicionamiento. Investigado globalmente y luego una vez por
> región el 2026-11-21.
> **Convención de evidencia:** cada cifra lleva su fuente. Lo que solo aparece en blogs de
> proveedor se marca **[sin verificar]** en lugar de presentarse como dato. Ciclos anteriores
> de esta KB citaron cifras de proveedor como hechos establecidos; eso se corrige aquí.

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

**Regulación.** No hay estatuto federal de AI; la obligación vinculante viene de las
legislaturas estatales. Nada específico de travel: aplica derecho de consumidor, privacidad y
seguridad de datos. Canadá opera con un marco de confianza y estándares. El **"AI AGENT Act"
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

### EMEA

**Evidencia.** *[sin verificar]* 38% de adopción de AI en travel en Europa Occidental y 42% en
Medio Oriente, con la transformación digital liderada por el Estado como motor en Medio Oriente
(contenido de proveedor). Encuesta comisionada por Expedia: 53% se siente cómodo con que la AI
*sugiera* opciones — de nuevo, sugerir sí, comprar no. Lufthansa Group: >50% de ventas de
agencia vía NDC (solo su negocio de agencia).

**Regulación — la región más densa, y con una contradicción sin resolver.**
- El **Digital Omnibus on AI, Regulation (EU) 2026/1744**, refina el AI Act.
- Los requisitos de alto riesgo para sistemas **Annex III stand-alone** se corrieron de
  agosto-2026 a **2 de diciembre de 2027**; los **Annex I embebidos** a **2 de agosto de 2028**.
- ⚠️ **Conflicto documentado:** una nota de ciclo previo (retail) registra un plazo
  transitorio del **Art. 50 el 2026-12-02**. Son provisiones distintas con fechas parecidas y
  años distintos. **No conflacionarlas, y confirmar contra el texto oficial antes de
  comprometer un plazo con un cliente.**
- Lectura específica de travel: la mayoría de las herramientas de cara al huésped
  **probablemente no califican como alto riesgo**, así que la postergación importa menos de lo
  que sugiere el titular. Lo que sí aplica siempre es transparencia y GDPR.
- **Medio Oriente:** a junio-2026, **ningún Estado del Golfo ni Israel tiene un estatuto
  horizontal integral de AI**. La norma vinculante más cercana es la **Regulation 10 de las
  DIFC Data Protection Regulations**, que gobierna datos personales procesados por sistemas
  autónomos y semiautónomos en el DIFC de Dubái. En Arabia Saudita el organismo clave es SDAIA.

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
  proyecto basado en riesgo. Perú: ley de AI de 2023, actualizada en 2025. Colombia:
  **CONPES 4144** (feb-2025) hasta 2030, orientado a capacidades y adopción más que a
  obligaciones horizontales inmediatas.

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
   NDC, ERP de agencia, predicción de demoras y alquiler vacacional. Ahí pertenece la IP
   propietaria de Globant, con la evidencia de la brecha como argumento de venta.

---
*Investigado globalmente y una vez por región el 2026-11-21. Las cifras sin fuente primaria
localizable están marcadas **[sin verificar]** a propósito.*
