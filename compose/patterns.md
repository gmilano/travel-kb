---
industry: travel
region: Global
updated: 2026-11-23
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

## Receta 7 — Identidad verificada sin pasivo de datos (la receta de North America)

**Problema del cliente.** Un hotel, aerolínea o alquiler vacacional necesita verificar
identidad o edad en el check-in digital, y a la vez no quiere ser responsable de custodiar
pasaportes. North America es la región con **la adopción biométrica más alta del mundo y la
preocupación más alta por brechas de datos** (IATA 2026): es el mismo cliente pidiendo las dos
cosas.

**Piezas (todas permisivas, licencias leídas el 2026-11-23):**

| Paso | Componente | Licencia |
|------|-----------|----------|
| Leer el chip del pasaporte en iOS | [`AndyQ/NFCPassportReader`](https://github.com/AndyQ/NFCPassportReader) | MIT |
| Leer la MRZ cuando no hay NFC (visas, documentos viejos, escaneo) | [`konstantint/PassportEye`](https://github.com/konstantint/PassportEye) o [`sivakumar-mahalingam/fastmrz`](https://github.com/sivakumar-mahalingam/fastmrz) | MIT / Apache-2.0 |
| Probar un atributo sin revelar el documento | [`zkpassport/circuits`](https://github.com/zkpassport/circuits) o [`rarimo/passport-zk-circuits`](https://github.com/rarimo/passport-zk-circuits) | Apache-2.0 / MIT |
| PMS donde aterriza el huésped verificado | [`Kamra-PMS/kamra-pms`](https://github.com/Kamra-PMS/kamra-pms) (Apache-2.0 desde el 2026-11-21) o [`TelivityAI/haip`](https://github.com/TelivityAI/haip) | Apache-2.0 |

**Cómo se conecta.**
1. El huésped apoya el pasaporte en el teléfono. `NFCPassportReader` hace BAC/secure messaging
   y autenticación pasiva **en el dispositivo**. Si no hay chip, `fastmrz` saca la MRZ de una
   foto, también en el dispositivo.
2. La app deriva **solo el atributo que la regla pide** — `mayor_de_18: true`,
   `nacionalidad_elegible: true`, `documento_vigente_al: 2027-03-01` — y **descarta el
   documento**. Si el atributo tampoco debe salir del teléfono, se emite como prueba ZK.
3. El backend recibe el atributo firmado, nunca el pasaporte, y lo escribe en el PMS vía su
   tool MCP tipada (`register_guest`), no por SQL.
4. El agente conversacional opera **sobre el atributo**, no sobre el documento. Nunca tiene el
   pasaporte en contexto, lo que además evita que termine en un log de prompts.

**La frase que vende la receta, y es literal:** *el documento nunca llega al servidor.* Con la
Ley 25 de Quebec, las cinco leyes estatales de AI vigentes a agosto-2026 y el GDPR si el
cliente opera también en EMEA, eso es una posición defendible, no un argumento de marketing.

**Esfuerzo:** 5–7 semanas para el flujo de lectura y atributos; +3–4 si se agrega la capa ZK.

**Límite honesto:** esto verifica **quién es** el viajero. **No** dice si puede entrar a un
país — ver Receta 9 y la brecha medida en `repos/foundations.md`.

---

## Receta 8 — Check-in que acepta la credencial del wallet europeo (la receta de EMEA)

**Problema del cliente.** Un operador en EMEA quiere aceptar el **EU Digital Identity Wallet**
en check-in o embarque sin convertirse en integrador de identidad, y sin heredar copyleft.

**La decisión que define la receta — y es puramente de licencia.** La organización oficial de
la Comisión publica en **tres licencias distintas**, verificadas leyendo cada archivo el
2026-11-23:

| Capa | Qué tomar | Licencia |
|------|-----------|----------|
| Especificación (ARF) | leer y citar libremente | **CC BY 4.0** (`LICENCE`, 249B) |
| Apps de referencia (`eudi-app-android-wallet-ui`, `eudi-app-ios-wallet-ui`) | **leer como referencia de UX; NO forkear** | **EUPL-1.2** (13961B) |
| Librerías y servicios (`eudi-srv-verifier-endpoint`, `eudi-lib-jvm-openid4vci-kt`, `eudi-lib-android-wallet-core`, `eudi-lib-ios-wallet-kit`) | **construir acá** | **Apache-2.0** |

**Cómo se conecta.**
1. Desplegar [`eudi-srv-verifier-endpoint`](https://github.com/eu-digital-identity-wallet/eudi-srv-verifier-endpoint)
   (Apache-2.0) como el Relying Party del cliente. Es el servicio que pide la credencial y
   valida la respuesta.
2. Integrar la app del cliente con [`eudi-lib-android-wallet-core`](https://github.com/eu-digital-identity-wallet/eudi-lib-android-wallet-core)
   / [`eudi-lib-ios-wallet-kit`](https://github.com/eu-digital-identity-wallet/eudi-lib-ios-wallet-kit)
   (Apache-2.0), **no copiando la app EUPL-1.2**.
3. Pedir **presentación selectiva**: solo los claims que el flujo necesita.
4. El resultado entra al PMS por tool MCP tipada, igual que en la Receta 7. Las dos recetas
   comparten backend: cambia **de dónde viene** el atributo verificado, no qué se hace con él.

**Control de CI que vale la pena escribir (3 líneas, evita una auditoría legal entera):**
fallar el build si un archivo bajo `vendor/` o `third_party/` contiene la cadena
`EUROPEAN UNION PUBLIC LICENCE`. Es la forma barata de garantizar que nadie copió la app de
referencia dentro del producto del cliente seis meses después de arrancar.

**Esfuerzo:** 6–8 semanas. El riesgo no es técnico sino de calendario: la disponibilidad real
de wallets por Estado miembro es desigual. **Diseñar el flujo con fallback a Receta 7.**

---

## Receta 9 — Itinerario con obligaciones vencibles (la receta de APAC, y la que llega a EMEA)

**Problema del cliente.** Un itinerario moderno no es solo "vuelo, hotel, actividad": arrastra
trámites con **fecha de vencimiento propia**. La SG Arrival Card de Singapur debe presentarse
**dentro de los 3 días previos** a la entrada. Japón tiene Visit Japan Web (opcional). EMEA
sumará **ETIAS** cuando se anuncie la fecha. Un PDF bonito que no modela esto está incompleto.

**Piezas.**

| Paso | Componente | Licencia |
|------|-----------|----------|
| Esquema de requisito de entrada | taxonomía de [`imorte/passport-index-data`](https://github.com/imorte/passport-index-data) (`eta` / `e-visa` / `visa on arrival` / `visa free` / `visa required` / `no admission`) | MIT |
| Ruteo y tiempos del viaje | [`motis-project/motis`](https://github.com/motis-project/motis) o [`valhalla/valhalla`](https://github.com/valhalla/valhalla) | MIT |
| Resolución de lugares desde texto libre | [`komoot/photon`](https://github.com/komoot/photon) | Apache-2.0 |
| Entrega offline del itinerario | patrón de [`zexuanw958-svg/travel-plan-viz`](https://github.com/zexuanw958-svg/travel-plan-viz) | MIT |

**Cómo se conecta.**
1. Del itinerario se derivan los **pares pasaporte×destino** con su fecha de cruce.
2. Para cada par se emite una **tarea fechada**, no un párrafo de texto:
   `{tramite, pais, abre: fecha_cruce - 3d, vence: fecha_cruce, estado}`. La ventana de
   apertura importa tanto como el vencimiento: la tarjeta de Singapur **no se puede presentar
   antes** de los 3 días.
3. El agente vigila las tareas y avisa; **no las completa.** Igual que en el pago, el corte es
   deliberado: presentar una declaración migratoria en nombre de otro tiene consecuencias
   distintas a reservar un hotel en nombre de otro.
4. El itinerario se entrega como HTML offline de un archivo, con las tareas incluidas. El
   viajero que más necesita el dato suele estar sin señal.

**⚠️ La advertencia que hay que leer antes de implementar esto.** Se usa la **taxonomía** de
`passport-index-data`, **nunca sus valores**: su propio README declara el dato al
**17-feb-2026** y el repo no recibe push desde el **2026-03-01**. Son nueve meses, y las
reglas de entrada cambiaron varias veces en 2026. Los valores vigentes salen de **Timatic
(IATA)** por contrato, o del portal consular, o de una curaduría propia del cliente con su
fecha de revisión visible. **Un itinerario que afirma "no necesitás visa" con dato de nueve
meses es un pasivo, no una feature.**

**Esfuerzo:** 4–6 semanas sobre un planificador existente. La fuente de datos de requisitos es
**decisión del cliente y su contrato**, no nuestra.

---

## Receta 10 — Motor de derechos del pasajero con reloj (la segunda receta de North America)

**Problema.** La Receta 3 resuelve el servicing conversacional: el agente explica, contiene y
reacomoda. Pero en North America la disrupción dejó de ser cortesía: la regla de reembolso
automático del US DOT fija **umbrales y plazos que un sistema puede computar**, y la pregunta
del cliente ya no es "¿qué le digo al pasajero?" sino **"¿cuánto le debo y desde cuándo corre
el plazo?"**. Ningún open source responde eso: `EU261 flight compensation stars:>=5` y
`IROPS irregular operations airline stars:>=1` devuelven **cero** (`repos/foundations.md`).

**Piezas.**

- Hecho del vuelo: **receptor propio** con
  [`sdr-enthusiasts/docker-adsb-ultrafeeder`](https://github.com/sdr-enthusiasts/docker-adsb-ultrafeeder)
  (GPL-3.0) corriendo como contenedor separado, o el feed contratado del cliente. **No
  OpenSky** si el entregable se factura — ver la advertencia de términos de dato.
- Trayectoria y fases de vuelo:
  [`xoolive/traffic`](https://github.com/xoolive/traffic) (**MIT**) — se puede embeber.
- Referencia aeroportuaria y **husos horarios**:
  [`mborsetti/airportsdata`](https://github.com/mborsetti/airportsdata) (**MIT**) y
  [`davidmegginson/ourairports-data`](https://github.com/davidmegginson/ourairports-data)
  (**Unlicense**).
- Reglas: **IP propietaria del engagement.** No existe y hay que escribirla.
- Orquestación: el stack agentic que ya use el cliente, exponiendo el motor como tool tipada.

**Cómo se arma.**

1. **Modelar la regla como dato con vigencia, no como código.** Cada regla es una fila:
   jurisdicción, disparador, umbral, plazo de pago, fecha de entrada en vigor, fecha de fin.
   Para el DOT: retraso **≥3 h doméstico** y **≥6 h internacional** cuando el pasajero rechaza
   la alternativa, reembolso en **7 días hábiles** (tarjeta) o **20 días corridos** (otros
   medios), y **cambio de número de vuelo tratado como cancelación**. Las reglas cambian: el
   DOT propuso en marzo de 2026 sumar los retrasos de **120 minutos en pista**. Si la regla
   está en el código, cada cambio regulatorio es un release; si está en una tabla con
   vigencia, es una fila.
2. **Calcular el umbral en hora local del aeropuerto.** Es la razón por la que `airportsdata`
   (MIT, con huso horario) está en la receta y no es un detalle: "3 horas de retraso" sin huso
   horario es una cuenta mal hecha, y mal hecha en la dirección que genera reclamos.
3. **Separar `detectar` de `determinar` de `ejecutar`.** El agente detecta el hecho y
   **determina** el derecho; el desembolso lo dispara un humano o un flujo con control
   explícito. Es la misma frontera que esta KB sostiene en el pago (Receta 4), por la misma
   razón.
4. **Emitir la determinación con su justificación citable**: regla aplicada, versión de la
   regla, hecho observado, hora local, resultado. Si no se puede auditar, no sirve ante el
   regulador ni ante el cliente.

**Qué entrega.** Un motor que dice *"a este pasajero le corresponde X, bajo la regla Y vigente
desde Z, y el plazo vence el W"*, con su traza. **Eso no existe en abierto en ninguna
jurisdicción**, es defendible como IP, y —a diferencia de Timatic— **la regla está publicada y
es citable**, así que se puede construir sin comprar el dato.

⚠️ **Verificar antes de comprometer:** la pausa de fiscalización del DOT para el supuesto
"misma ruta, otro número de vuelo" figura con fin el **2026-06-30** y no se pudo confirmar
desde este entorno si caducó, se extendió o fue reemplazada. Hay que abrir el Federal Register
antes de prometer cobertura de ese caso.

## Receta 11 — Dato de vuelo sin pasivo de licencia (la receta transversal)

**Problema.** Todas las recetas de disrupción de esta KB —3, 9 y 10— dependen de saber dónde
está el avión, y el camino obvio para conseguirlo es el que no se puede facturar. Esta receta
existe para que esa decisión se tome **una vez, al principio**, y no en la semana de entrega.

**El árbol de decisión, en orden de costo creciente.**

1. **¿Alcanza con dato de referencia estático?** (aeropuertos, pistas, husos horarios,
   códigos) → `ourairports-data` (**Unlicense**, dominio público) y `airportsdata` (**MIT**).
   **Costo cero, condiciones cero, uso comercial sin reservas.** Una cantidad sorprendente de
   funcionalidad de itinerario se resuelve acá y nunca necesita una posición en vivo.
2. **¿El cliente ya tiene un contrato de datos** (GDS, Cirium, FlightAware, su propio
   operador)? → Usarlo. El trabajo es el adaptador, no el dato, y el adaptador es trabajo
   facturable sin riesgo.
3. **¿Es un prototipo interno, una evaluación o una demo que no se factura?** → OpenSky con
   [`openskynetwork/opensky-api`](https://github.com/openskynetwork/opensky-api) (GPL-3.0)
   **es exactamente el caso que sus términos contemplan** ("evaluación interna"). **Hay que
   decir en el documento del proyecto que el componente es de evaluación**, para que nadie lo
   promueva a producción por inercia.
4. **¿Hace falta posición en vivo en un producto facturable?** → **Receptor propio.**
   `ultrafeeder` (GPL-3.0) en un contenedor, `tar1090` (GPL-2.0+) para la vista operativa,
   `pyModeS` (GPL-3.0) o `adsb_deku` (MIT) para decodificar, `traffic` (MIT) para analizar.
   Cuesta hardware y cuesta cobertura —un receptor ve su horizonte, no el mundo— pero el dato
   es del cliente y no tiene condición de uso de un tercero.

**La regla de embebido, que es la única parte delicada.** GPL **no prohíbe usar**: prohíbe
embeber en un binario propietario. `ultrafeeder`, `tar1090`, `readsb` y `pyModeS` se corren
como **proceso o contenedor separado detrás de una API interna**, y el producto del cliente
habla con esa API. Lo que sí se puede embeber sin pensarlo es lo MIT y lo de dominio público:
`traffic`, `adsb_deku`, `airportsdata`, `ourairports-data`.

**Emisiones, si el encargo las pide.**
[`google/travel-impact-model`](https://github.com/google/travel-impact-model) (**CC-BY-4.0**)
es la referencia pública del CO₂e de un vuelo. Permite uso comercial **con atribución**; es
licencia de **contenido**, así que el modelo y sus tablas encajan, y copiar código de ahí a un
producto se consulta con legales. El resto del segmento está muerto: las dos únicas
calculadoras de huella de viaje con más de 30★ no reciben push desde 2021 y 2023.

**Qué entrega.** Una decisión de arquitectura tomada con los dos documentos sobre la mesa —la
licencia del código y los términos del dato— y escrita en el documento del proyecto, en vez de
una dependencia barata que alguien tiene que arrancar tres días antes de entregar.

## Receta 12 — Checkout agentic sin tocar el merchant of record (la receta transversal de pago)

Agregada en la **tercera pasada del 2026-11-23**. Las once recetas anteriores terminan con la
frase *"corte en el pago"* o *"se entrega al merchant of record"* y **ninguna dice con qué**.
Esta la cierra. Es transversal: aplica a las cuatro regiones, porque el protocolo es
horizontal y lo regional es el **riel de cobro**, no el diseño.

**El problema real.** El cliente pide "que el agente reserve". Las aerolíneas no ceden el
cobro (`intel/market.md` → Players; United quiere humano en la compra). El agente, entonces,
tiene que poder **probar que el viajero autorizó esta compra concreta** sin ser él quien cobra.
Eso es un problema de *autorización*, no de *pagos*.

**Las piezas, con su licencia leída:**

| Capa | Pieza | Licencia | Por qué esta |
|------|-------|----------|--------------|
| Modelo de autorización | [`google-agentic-commerce/AP2`](https://github.com/google-agentic-commerce/AP2) | Apache-2.0 | Se toma **la especificación de mandatos**, no el repo como dependencia: está quieto desde 2026-06-17 (`intel/trends.md` → 18). |
| Identidad del agente | [`forter/trusted-agentic-commerce-protocol`](https://github.com/forter/trusted-agentic-commerce-protocol) | MIT | Responde *¿este agente es quien dice ser?*, que es la pregunta que hace el fraud team del cliente, no la que hace el CTO. |
| Comercio / merchant of record | [`Universal-Commerce-Protocol/ucp`](https://github.com/Universal-Commerce-Protocol/ucp) | Apache-2.0 | Es la única especificación del plano cuyo diseño declarado **deja al comercio como merchant of record** — la restricción no negociable de travel. |
| Arquitectura de referencia | [`NVIDIA-AI-Blueprints/Retail-Agentic-Commerce`](https://github.com/NVIDIA-AI-Blueprints/Retail-Agentic-Commerce) | Apache-2.0 | ACP + UCP funcionando con control del merchant. **Es retail**: se lee la arquitectura, no se despliega el producto. |
| Riel (solo si aplica) | [`x402-foundation/x402`](https://github.com/x402-foundation/x402) | Apache-2.0 | Para **pagarle a un proveedor**, no para cobrarle al viajero. Ver la advertencia de abajo. |
| Inventario y cobro reales | Sabre / Travelport / PayPal vía contrato | — | El dinero lo mueve quien ya tiene licencia para moverlo. |

**El cableado, en orden:**

1. **El agente arma el carrito** con las piezas que ya están en esta KB (`punitarani/fli` para
   vuelo, `RollingGo-AI/RollingGo-Hotel-MCP-Global` para hotel).
2. **El viajero firma un mandato acotado** — destino, rango de fechas, tope de gasto, vigencia.
   Se implementa con el **modelo** de AP2 sobre firma propia; el mandato se guarda con su hash
   y su vencimiento. **Esta es la pieza de IP:** no hay implementación abierta con tracción
   (`AP2 mandate implementation stars:>=20` → **0**).
3. **El comercio verifica dos cosas distintas**: que el mandato cubre *esta* compra, y que el
   agente es quien dice ser (TACP). Son dos verificaciones separadas y conviene que lo sigan
   siendo: la primera la audita legales, la segunda la audita el equipo de fraude.
4. **El cobro lo ejecuta el merchant of record** — aerolínea, hotel o GDS. El agente nunca
   toca el dinero del viajero. El hito real que valida esto es **Sabre + PayPal + Mindtrip**
   (vuelos, 2026): Mindtrip conversa, Sabre tiene el inventario y **PayPal cobra**. Tres
   actores, y el agente no es ninguno de los que cobra.
5. **Todo mandato se archiva con su vencimiento**, porque la pregunta del contracargo llega
   meses después y la respuesta es el mandato firmado, no el log del chat.

**Lo que esta receta NO resuelve, dicho antes de que lo pregunte el cliente:**

- **El contracargo.** `travel refund chargeback agent stars:>=5` → **0**. Ninguno de estos
  protocolos dice quién responde si el pasajero desconoce el cargo. Es contrato, no código.
- **El reembolso regulado.** Los plazos del US DOT y de EU261 no están en ningún protocolo de
  pago. Eso vive en la **Receta 10**, y se conecta acá: el mandato dice *qué se autorizó*; el
  motor de derechos dice *qué se debe devolver*. Son dos relojes distintos.
- **El pago en cripto como respuesta al cobro del viajero.** `x402` mueve stablecoins y es la
  pieza más viva del plano, pero **un viajero que reclama un vuelo quiere su tarjeta de vuelta,
  no un token**. Usarlo para liquidar entre agentes y proveedores; no proponerlo como checkout
  de consumidor en un engagement de travel sin un motivo muy explícito.
- **El ticketing con plazo.** Un PNR vence; un mandato vence; no vencen juntos. Ninguna
  especificación del plano modela esa doble vigencia — **y es exactamente donde se rompen
  estas integraciones en producción.**

**Qué prometer.** "El viajero autoriza una vez, con límites explícitos y auditables; el agente
opera dentro de esos límites; el cobro lo hace quien hoy ya cobra." Eso es cierto, es
construible con licencias permisivas verificadas, y **no requiere que la aerolínea ceda nada**
— que es la razón por la que es vendible.

## Lo que NO conviene prometer

| Pedido frecuente | Por qué no, hoy | Qué ofrecer en cambio |
|------------------|-----------------|----------------------|
| "Un agente que reserve solo, de punta a punta" | 2% de reserva efectiva, 8% de confianza, y las aerolíneas mantienen el humano en la compra | Receta 3 o 4 con corte en el pago |
| "Revenue management con AI sobre open source" | **Cero** repos medidos (`hospitality revenue management stars:>=30` → 0) | IP propietaria de Globant; la brecha es el argumento de venta |
| "Integración NDC open source" | **Cero** repos medidos. NDC es XML con esquema licenciado por IATA y acceso contractual | Integración contractual + capa MCP propia encima |
| "Predicción de demoras con un modelo abierto" | **Cero** repos medidos ≥50★ | Modelo propio sobre datos públicos |
| "Partimos del SDK de Amadeus" | [`amadeus4dev/amadeus-python`](https://github.com/amadeus4dev/amadeus-python) está **archivado** desde 2025 | Usar su esquema como referencia; integrar por API |
| "El agente le dice al viajero si necesita visa" | El dato abierto está **nueve meses desatrasado** y Timatic no tiene alternativa open source (`timatic travel document check stars:>=20` → **0**) | Receta 9 con dato contractual del cliente y fecha de revisión visible en pantalla |
| "Integramos APIS / PNR con una librería open source" | **Cero** repos medidos en ambas consultas el 2026-11-23 | Integración contractual; la capa agentic va encima |
| "Preparamos el producto para ETIAS con fecha cierta" | A fines de nov-2026 **no hay fecha oficial anunciada**; el objetivo 4T-2026 fue retirado y se espera 2027 | Vender el *servicing* del cambio de requisito, no la fecha |
| "Usamos el lector de pasaporte Android más popular" | [`tananaev/passport-reader`](https://github.com/tananaev/passport-reader) (458★) **no tiene archivo de licencia** | Portar desde `NFCPassportReader` (MIT) o construir sobre JMRTD |
| "Partimos del wallet de identidad europeo" | Las **apps** de referencia son **EUPL-1.2**: forkearlas arrastra copyleft al producto del cliente | Receta 8: construir sobre las librerías y servicios **Apache-2.0** de la misma organización |
| "Traemos datos de vuelo en vivo gratis con OpenSky" | El código es GPL-3.0 y cumplible, pero los **términos de dato** de OpenSky cubren investigación y educación sin fines de lucro, evaluación interna y fines gubernamentales: **el uso comercial no está licenciado** | Receta 11: dato de referencia de dominio público para lo estático, contrato del cliente o receptor propio para lo vivo. OpenSky solo en prototipo interno declarado |
| "Integramos FlightRadar24 con una librería MIT" | La licencia MIT cubre **el SDK no oficial**, no el dato ni los términos de servicio de FR24 | Lo mismo que con los conectores de LetsFG: piloto interno sí, entregable a cliente con contrato de datos |
| "Usamos el proyecto de seguimiento de aeronaves más popular" | [`Jxck-S/plane-notify`](https://github.com/Jxck-S/plane-notify) tiene 2554★ y una **licencia source-available propia** (PolyForm Shield + Elastic 2.0): **no es open source** | `tar1090`/`readsb` (GPL, como servicio separado) o `adsb_deku`/`traffic` (MIT, embebibles) |
| "El AI Act nos obliga a tratar el check-in biométrico como alto riesgo" | El Anexo III punto 7 **excluye la verificación de documentos de viaje** de su literal (d): la verificación **1:1** contra el chip del propio pasaporte queda fuera; el matching **1:N** contra listas queda dentro | Separar los dos productos y presupuestarlos distinto — y confirmar el texto en EUR-Lex, que esta KB no pudo leer por restricción de red |
| "Las obligaciones de alto riesgo del AI Act se aplazaron, hay tiempo" | El Reglamento (UE) 2026/1744 difiere el Anexo III autónomo al **2026-12-02**, pero el **Artículo 50 (transparencia) sigue aplicando desde el 2026-08-02** | Decirlo entero: es una prórroga parcial, no una derogación. Avisar que se habla con una AI y etiquetar lo generado ya es obligatorio |
| "Predecimos el retraso con un modelo open source" | `flight delay prediction stars:>=50` devuelve **un** resultado y es un tutorial de AWS que usa retrasos como dataset de ejemplo. **No hay modelos reutilizables** | Vender el motor de derechos (Receta 10), que opera sobre el hecho ya ocurrido y tiene regla citable, en vez de una predicción sin base abierta |

---
*Toda licencia citada fue verificada leyendo el archivo de licencia del repo, no el badge de
GitHub. Ver `agents/top.md` → "Verificar antes de usar".*
