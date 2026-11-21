---
industry: travel
region: Global
updated: 2026-11-21
---

# 🧩 Patrones de composición — Travel & Hospitality

> Recetas concretas con repos nombrados, licencias verificadas y el punto exacto donde se
> enchufa cada pieza. Todos los repos citados fueron verificados el 2026-11-21.

## Patrón base del vertical

```
[Datos geoespaciales + ruteo]        photon / valhalla / motis      (Apache-2.0 / MIT)
          ↓
[Plataforma vertical que ya opera]   QloApps / Odoo / HAIP / TREK   (OSL · LGPL · Apache · AGPL)
          ↓
[Capa de acceso tipado: MCP server]  propio del sistema, o escrito en el engagement
          ↓
[Agentes especializados]             fli / Tourmind / RollingGo / toolkit de millas
          ↓
[Human-in-the-loop en el pago]       merchant of record = la aerolínea o el hotel
          ↓
[Entrega al viajero]                 travel-plan-viz (HTML offline) / voz / chat
```

**La regla que atraviesa todas las recetas:** el agente llama tools tipadas, nunca la base de
datos; y la transacción la cierra el merchant of record, no el agente.

---

## Receta 1 — Concierge hotelero sobre un PMS que ya funciona

**Problema del cliente:** cadena hotelera mediana, quiere concierge conversacional y check-in
asistido sin reemplazar su operación.

**Punto de partida**
- [`Qloapps/QloApps`](https://github.com/Qloapps/QloApps) — OSL-3.0 core, **AFL-3.0 módulos**, 14.500★ — PMS + booking engine + sitio
- o [`TelivityAI/haip`](https://github.com/TelivityAI/haip) — Apache-2.0, 60★ — si el cliente exige licencia permisiva
- o [`Kamra-PMS/kamra-pms`](https://github.com/Kamra-PMS/kamra-pms) — AGPL-3.0, 109★ — si se acepta AGPL y se quiere un PMS pensado para agentes

**Cómo se arma**
1. **No forkear QloApps.** Escribir un **módulo** (los módulos son AFL-3.0, permisiva: la
   lógica propietaria vive legalmente ahí) que exponga `search_availability`,
   `get_reservation`, `modify_stay`, `checkin_status` como MCP server.
2. [`aws-samples/sample-voice-and-chat-hotel-assistant`](https://github.com/aws-samples/sample-voice-and-chat-hotel-assistant)
   (**MIT-0**, 18★) como referencia de voz en tiempo real con Bedrock Nova Sonic. MIT-0 = sin
   obligación de atribución, lo más limpio para código de cliente.
3. [`komoot/photon`](https://github.com/komoot/photon) (Apache-2.0, 3.203★) para resolver
   "¿hay algo para comer cerca?" sin mandar la ubicación del huésped a una API de terceros —
   argumento de cumplimiento bajo GDPR, no solo técnico.
4. [`MewsSystems/fiscalizations`](https://github.com/MewsSystems/fiscalizations) (MIT, 62★) si
   hay facturación fiscal por jurisdicción.

**Dónde se corta:** modificación de reserva con cargo → aprobación humana. Consulta, servicing
y upsell sin cargo → autónomo.

**Esfuerzo:** 6–10 semanas para un piloto de una propiedad. El módulo MCP es el 70% del trabajo.

---

## Receta 2 — Planificador de itinerario que el cliente puede auditar

**Problema del cliente:** DMO, aerolínea o tour operador que necesita itinerarios que no
inventen horarios, precios ni lugares.

**Punto de partida**
- [`awangwang123/jianhao-travel-planner`](https://github.com/awangwang123/jianhao-travel-planner) — MIT, 449★ — skill con **verificación cruzada multi-fuente**
- [`tczyliu/china-travel-kit`](https://github.com/tczyliu/china-travel-kit) — MIT, 179★ — datos **con fuente citada** (si el destino es China)

**Cómo se arma**
1. El planner propone; **nada se muestra sin verificar**.
2. Verificación de lugares y distancias con
   [`valhalla/valhalla`](https://github.com/valhalla/valhalla) (**MIT**, 6.475★ — la licencia
   real está en `COPYING`, no en el `LICENSE.md` de 45 bytes) usando **isócronas**: si la
   actividad de las 15:00 queda a 90 minutos de la de las 16:00, el itinerario se rechaza antes
   de llegar al usuario. Esto elimina la clase de error más común del vertical.
3. Transporte público real con [`BlinkTagInc/node-gtfs`](https://github.com/BlinkTagInc/node-gtfs)
   (MIT, 506★) sobre el feed GTFS del destino, y llegadas en vivo con
   [`MobilityData/gtfs-realtime-bindings`](https://github.com/MobilityData/gtfs-realtime-bindings)
   (Apache-2.0, 446★).
4. POIs y reseñas con [`pab1it0/tripadvisor-mcp`](https://github.com/pab1it0/tripadvisor-mcp)
   (MIT, 64★) — **dormido 19 meses: copiar el esquema, no depender del repo.**
5. Entrega con [`zexuanw958-svg/travel-plan-viz`](https://github.com/zexuanw958-svg/travel-plan-viz)
   (MIT, 415★): HTML de un solo archivo, offline, mobile-first. El viajero en roaming no tiene
   señal, y ese es el requisito que casi todas las demos ignoran.

**Esfuerzo:** 4–6 semanas. El paso 2 es lo que diferencia esto de una demo.

---

## Receta 3 — Servicing y disrupción (la receta de North America)

**Problema del cliente:** aerolínea u OTA de EE.UU. que quiere valor agentic sin tocar el pago,
porque la confianza para reservar no existe (52% planifica / 2% reserva; 8% de confianza).

**Punto de partida**
- [`punitarani/fli`](https://github.com/punitarani/fli) — MIT, 3.510★ — vuelos como MCP + CLI + librería
- [`borski/travel-hacking-toolkit`](https://github.com/borski/travel-hacking-toolkit) — MIT, 1.029★ — cash, puntos, millas y award flights

**Cómo se arma**
1. Monitor de itinerario: el agente vigila el PNR del viajero, clima y estado de vuelos.
2. Ante disrupción, **propone** alternativas calculadas con `fli` y evaluadas en cash **y** en
   millas con `travel-hacking-toolkit` — el único activo open source serio de loyalty, y el
   diferenciador real para el viajero frecuente norteamericano.
3. Conexiones terrestres y tiempos puerta-a-puerta con
   [`graphhopper/graphhopper`](https://github.com/graphhopper/graphhopper) (Apache-2.0, 6.827★).
4. **El reacomodo lo ejecuta el sistema del proveedor**, con la aerolínea como merchant of
   record (el patrón que Travelport y Booked AI demostraron el 12-nov-2026), o lo confirma un
   agente humano. El agente AI nunca cobra.
5. Si el cliente es una red de asesores: el mismo stack como **copiloto del asesor**, que es
   donde NA concentra la adopción.

**Esfuerzo:** 8–12 semanas. Es la receta con el camino más corto a producción porque **no
atraviesa el pago**.

---

## Receta 4 — Agente de búsqueda y reserva con corte explícito en el pago

**Problema del cliente:** OTA o agencia que quiere búsqueda agentic real sobre inventario
transaccionable.

**Punto de partida — elegir según el inventario, y leer la licencia primero**
- [`tourmind-com/Tourmind-Booking-Skills`](https://github.com/tourmind-com/Tourmind-Booking-Skills) — MIT, 2.414★ — hotel + vuelo end-to-end
- [`RollingGo-AI/RollingGo-Hotel-MCP-Global`](https://github.com/RollingGo-AI/RollingGo-Hotel-MCP-Global) — MIT, 90★ — 2M+ hoteles mayorista, 40+ LLMs
- [`flightclaw/agents`](https://github.com/flightclaw/agents) — MIT, 87★ — vuelos + tracking de precio
- [`LetsFG/LetsFG`](https://github.com/LetsFG/LetsFG) — MIT **+ addendum de 1% por reserva**, 2.295★ — ⚠️ y sus conectores **automatizan los sitios públicos de las aerolíneas**: riesgo de ToS, no de licencia. Revisar con legales antes de proponerlo.
- ❌ **No usar** [`MikkoParkkola/trvl`](https://github.com/MikkoParkkola/trvl): PolyForm Noncommercial.

**Cómo se arma**
1. [`Azure-Samples/azure-ai-travel-agents`](https://github.com/Azure-Samples/azure-ai-travel-agents)
   (MIT, 483★) como **arquitectura de referencia multiagente sobre MCP** — orquestador,
   especialistas por dominio, despliegue en contenedores. Es el mejor esqueleto enterprise
   disponible con licencia permisiva.
2. Enchufar los MCP de inventario de arriba como tools. **Neutralidad de protocolo:**
   mantener los adaptadores detrás de una interfaz propia para no quedar atado a MCP de un GDS,
   a UCP ni a un proveedor.
3. Checkout **siempre** en el riel del proveedor con NDC/ONE Order cuando exista, y el
   proveedor como merchant of record.
4. Para mercados sin API agentic: [`Prism-Shadow/travel-agent`](https://github.com/Prism-Shadow/travel-agent)
   (Apache-2.0, 52★) como patrón de navegación de sitios reales que **se detiene en el pago**.
   Es el fallback honesto y su comportamiento es exactamente el que la evidencia de confianza
   recomienda.

**Esfuerzo:** 10–14 semanas. El riesgo no es técnico, es contractual: el acceso al inventario.

---

## Receta 5 — Capa agentic multimodal europea (ferrocarril + aire + tierra)

**Problema del cliente:** operador o DMO europeo, viaje puerta a puerta con tren, avión y
transporte urbano.

**Por qué existe esta receta:** el único MCP ferroviario del mundo encontrado en la medición es
[`r-huijts/ns-mcp-server`](https://github.com/r-huijts/ns-mcp-server) (MIT, 64★, ferrocarril
holandés) y está **dormido 15 meses**. Europa es el mercado ferroviario más denso del planeta y
su capa agentic no existe. Las piezas de abajo sí.

**Cómo se arma**
1. [`motis-project/motis`](https://github.com/motis-project/motis) (**MIT**, 628★) como motor
   multimodal: ruteo + geocoding + tiles en un binario, con licencia permisiva. Es la elección
   clave — [`opentripplanner/OpenTripPlanner`](https://github.com/opentripplanner/OpenTripPlanner)
   (LGPL-3.0, 2.780★) es más maduro pero su copyleft obliga a correrlo como servicio separado.
2. Feeds GTFS nacionales validados con
   [`ibi-group/datatools-ui`](https://github.com/ibi-group/datatools-ui) (MIT, 147★) — higiene
   de datos antes de que el agente los lea.
3. Escribir el MCP server que falta: `plan_journey`, `get_disruptions`, `rebook_leg`. **Este es
   el entregable reutilizable del engagement** y el activo que la región no tiene.
4. Front-end con [`opentripplanner/otp-react-redux`](https://github.com/opentripplanner/otp-react-redux)
   (MIT, 95★) y capa conversacional arriba.
5. Todo self-hosted con [`headwaymaps/headway`](https://github.com/headwaymaps/headway)
   (Apache-2.0, 3.022★): bajo el AI Act y GDPR, la procedencia del dato es facilitador de
   cumplimiento.

**Esfuerzo:** 12–16 semanas. Deja un activo reutilizable en toda la región.

---

## Receta 6 — Asistente de turismo nacional (la receta de LATAM)

**Problema del cliente:** ministerio de turismo o DMO que quiere un asistente oficial de viaje
en su plataforma nacional.

**Por qué existe esta receta:** ya la ejecutaron tres países vecinos en 2026 — **Perú**
(Peru.travel, MINCETUR/PROMPERÚ, 7-abr-2026), **Chile** (Chile Travel App, Sernatur,
15-sep-2026) y **Argentina** (planificador AI de Visit Argentina). El comprador es el Estado y
tiene tres referencias públicas al lado.

**Cómo se arma**
1. Base: la Receta 2, con el paso de verificación obligatorio. Un asistente oficial que
   alucina un horario de museo es un problema de prensa, no un bug.
2. **Todo self-hosted:** [`komoot/photon`](https://github.com/komoot/photon) (Apache-2.0) para
   geocoding, [`valhalla/valhalla`](https://github.com/valhalla/valhalla) (MIT) para ruteo,
   [`headwaymaps/headway`](https://github.com/headwaymaps/headway) (Apache-2.0) para tiles.
   Además de soberanía de datos, **elimina el costo en USD por consulta** — restricción real
   en países con moneda devaluada y presupuesto público.
3. Entrega con [`zexuanw958-svg/travel-plan-viz`](https://github.com/zexuanw958-svg/travel-plan-viz)
   (MIT, 415★): HTML offline. El turista internacional no tiene datos móviles al llegar.
4. **Publicar el skill de itinerario en español bajo MIT.** La búsqueda
   `turismo viajes IA agente` devuelve **1 repo con 0 estrellas**: con cero competencia medida,
   el repo publicado se vuelve la referencia por defecto de la región a coste casi nulo.
5. Base operativa de agencia, si hace falta back-office: [`odoo/odoo`](https://github.com/odoo/odoo)
   (**LGPL-3.0** leído del archivo, 55.999★) con **addon propietario** — LGPL-3.0 lo permite
   explícitamente, y es el hueco que llena la ausencia total de ERP de travel open source.

**Esfuerzo:** 8–12 semanas por país. El itinerario verificado se reutiliza entre países; lo que
cambia son los datos y el idioma.

---

## Lo que NO conviene prometer

| Pedido frecuente | Por qué no, hoy | Qué ofrecer en cambio |
|------------------|-----------------|----------------------|
| "Un agente que reserve solo, de punta a punta" | 2% de reserva efectiva, 8% de confianza, y las aerolíneas mantienen el humano en la compra | Receta 3 o 4 con corte en el pago |
| "Revenue management con AI sobre open source" | **Cero** repos medidos (`hospitality revenue management stars:>=30` → 0) | IP propietaria de Globant; la brecha es el argumento de venta |
| "Integración NDC open source" | **Cero** repos medidos. NDC es XML con esquema licenciado por IATA y acceso contractual | Integración contractual + capa MCP propia encima |
| "Predicción de demoras con un modelo abierto" | **Cero** repos medidos ≥50★ | Modelo propio sobre datos públicos |
| "Partimos del SDK de Amadeus" | [`amadeus4dev/amadeus-python`](https://github.com/amadeus4dev/amadeus-python) está **archivado** desde 2025 | Usar su esquema como referencia; integrar por API |

---
*Toda licencia citada fue verificada leyendo el archivo de licencia del repo, no el badge de
GitHub. Ver `agents/top.md` → "Verificar antes de usar".*
