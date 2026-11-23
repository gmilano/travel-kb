---
industry: travel
region: Global
updated: 2026-11-23
---

# 🎯 Agentes AI — Travel & Hospitality

> Agentes y herramientas AI open source para la industria. Foco: MIT / Apache 2.0 / BSD.
> **Toda fila fue verificada**: existencia por `git ls-remote`, estrellas y `pushed_at` por
> `search/repositories`, y **licencia leyendo el archivo de licencia**, no el badge de GitHub.
> Cero filas de ejemplo.
>
> **Tercera pasada 2026-11-23:** se agrega el **plano de pago agentic** — la capa que esta
> KB venía nombrando en cada receta ("corte en el pago", "merchant of record") sin una sola
> fila de código.
>
> **Ciclo 2026-11-23:** se re-midieron las filas principales del 2026-11-21 (ver
> *Re-medición* abajo) y se agregó una sección nueva: **identidad y documento de viaje**,
> el plano que esta KB venía nombrando (biometría, visado) sin ninguna fila de código.

## Agentes y herramientas verificadas

| Nombre | Repo | Licencia | Stars | Último push | Descripción |
|--------|------|----------|-------|-------------|-------------|
| fli | [punitarani/fli](https://github.com/punitarani/fli) | MIT | 3513 | 2026-11-11 | Google Flights como MCP server + CLI + librería Python. El acceso a búsqueda de vuelos más usado del ecosistema open source. |
| Tourmind Booking Skills | [tourmind-com/Tourmind-Booking-Skills](https://github.com/tourmind-com/Tourmind-Booking-Skills) | MIT | 2416 | 2026-11-20 | Agent skills de booking end-to-end de hotel y vuelo; compara tarifas de hotel en vivo entre varios proveedores. |
| LetsFG | [LetsFG/LetsFG](https://github.com/LetsFG/LetsFG) | MIT + addendum comercial | 2296 | 2026-11-15 | Búsqueda y reserva agent-native de vuelo/hotel: MCP server, CLI y SDKs Python/JS. **Ver advertencia abajo.** |
| travel-hacking-toolkit | [borski/travel-hacking-toolkit](https://github.com/borski/travel-hacking-toolkit) | MIT | 1041 | 2026-11-16 | Búsqueda con cash, puntos, millas y award flights. Drop-in skill para asistentes. Único repo relevante de loyalty/millas. |
| mcp-google-map | [cablate/mcp-google-map](https://github.com/cablate/mcp-google-map) | MIT | 503 | 2026-10-22 | 18 tools de Google Maps + 3 agent skills: búsqueda de lugares, rutas, planificación de viaje, SEO local. |
| azure-ai-travel-agents | [Azure-Samples/azure-ai-travel-agents](https://github.com/Azure-Samples/azure-ai-travel-agents) | MIT | 483 | 2026-11-20 | Referencia enterprise multiagente sobre MCP, desplegada en Azure Container Apps. El mejor punto de partida "arquitectura de cliente". |
| jianhao-travel-planner | [awangwang123/jianhao-travel-planner](https://github.com/awangwang123/jianhao-travel-planner) | MIT | 449 | 2026-11-16 | Skill de itinerario con verificación cruzada multi-fuente y salida ejecutable. Mercado China (APAC). |
| travel-plan-viz | [zexuanw958-svg/travel-plan-viz](https://github.com/zexuanw958-svg/travel-plan-viz) | MIT | 415 | 2026-11-19 | Renderiza el itinerario como HTML de un solo archivo, offline y mobile-first (mapa + timeline diario). Capa de entrega, no de planning. |
| wanderlog-mcp | [shaikhspeare/wanderlog-mcp](https://github.com/shaikhspeare/wanderlog-mcp) | MIT | 193 | 2026-11-16 | MCP server de Wanderlog: construir y editar itinerarios conversacionalmente. |
| china-travel-kit | [tczyliu/china-travel-kit](https://github.com/tczyliu/china-travel-kit) | MIT | 179 | 2026-08-25 | Datos de turismo receptivo de China con fuente citada: CLI, HTTP API y MCP server. |
| RollingGo-Hotel-MCP-Global | [RollingGo-AI/RollingGo-Hotel-MCP-Global](https://github.com/RollingGo-AI/RollingGo-Hotel-MCP-Global) | MIT | 90 | 2026-11-19 | MCP oficial de booking hotelero: 2M+ hoteles a tarifa mayorista, compatible con 40+ LLMs. |
| flightclaw/agents | [flightclaw/agents](https://github.com/flightclaw/agents) | MIT | 87 | 2026-10-26 | Búsqueda de vuelos, tracking de precio y booking para agentes, con MCP server hosteado. |
| personalized-travel-guide-skill | [TokenHungryMash/personalized-travel-guide-skill](https://github.com/TokenHungryMash/personalized-travel-guide-skill) | MIT | 81 | 2026-11-13 | Skill que genera manuales de viaje personalizados como web mobile-friendly. |
| tripadvisor-mcp | [pab1it0/tripadvisor-mcp](https://github.com/pab1it0/tripadvisor-mcp) | MIT | 64 | 2025-04-13 | MCP server sobre la Tripadvisor Content API. **Dormido ~19 meses**: usar como referencia de esquema, no como dependencia. |
| ns-mcp-server | [r-huijts/ns-mcp-server](https://github.com/r-huijts/ns-mcp-server) | MIT | 64 | 2025-08-26 | MCP de Nederlandse Spoorwegen (ferrocarril holandés). Único MCP ferroviario EMEA encontrado. Dormido ~15 meses. |
| RollingGo-hotel-MCP-CN | [RollingGo-AI/RollingGo-hotel-MCP-CN](https://github.com/RollingGo-AI/RollingGo-hotel-MCP-CN) | MIT | 61 | 2026-11-02 | Variante China: 2M hoteles, 110k contratos directos, precio de canal. |
| viajante | [felipebasurto/viajante](https://github.com/felipebasurto/viajante) | MIT | 60 | 2026-11-19 | Búsqueda de vuelo y hotel para terminal, Python y asistentes AI. Nombre en español, autor europeo. |
| travel-agent (Prism-Shadow) | [Prism-Shadow/travel-agent](https://github.com/Prism-Shadow/travel-agent) | Apache-2.0 | 52 | 2026-09-08 | Agente que opera **sitios web reales en un browser** y se detiene en la página de pago. El patrón honesto para mercados sin API agentic. |
| trip-planner-skill | [skywain/trip-planner-skill](https://github.com/skywain/trip-planner-skill) | MIT | 51 | 2026-10-10 | Skill de planificación portable entre Claude Code, Codex, Gemini CLI, Cursor y Copilot. |
| OTAIP | [TelivityAI/otaip](https://github.com/TelivityAI/otaip) | Apache-2.0 | 47 | 2026-11-21 | Open Travel AI Platform: orquestación de agentes específica del dominio travel. Muy activo, pero chico. |
| voice-and-chat-hotel-assistant | [aws-samples/sample-voice-and-chat-hotel-assistant](https://github.com/aws-samples/sample-voice-and-chat-hotel-assistant) | MIT-0 | 18 | 2026-07-10 | Asistente hotelero de voz y chat en tiempo real con Amazon Bedrock Nova Sonic. MIT-0 = sin obligación de atribución. |

## Identidad y documento de viaje — el plano de frontera

Hasta este ciclo la KB registraba que **la adopción biométrica es la más alta del mundo en
North America** y que **las reglas de entrada disuaden al 43% de los viajeros** (IATA 2026),
sin una sola fila de código. Existe: es el único segmento de travel donde el piso open source
es **permisivo y vivo**. Todas las licencias de abajo fueron leídas del archivo el 2026-11-23.

| Nombre | Repo | Licencia (archivo leído) | Stars | Último push | Descripción |
|--------|------|--------------------------|-------|-------------|-------------|
| NFCPassportReader | [AndyQ/NFCPassportReader](https://github.com/AndyQ/NFCPassportReader) | MIT (`LICENSE`, 1065B) | 867 | 2026-11-16 | Lectura NFC de pasaporte electrónico ICAO 9303 en iOS: BAC, secure messaging y autenticación pasiva. El repo más usado del segmento y el único grande con licencia permisiva real. |
| PassportEye | [konstantint/PassportEye](https://github.com/konstantint/PassportEye) | MIT (`LICENSE`, 1064B) | 471 | 2026-11-22 | Extracción de la MRZ (zona legible por máquina) de pasaportes, visas y documentos de identidad desde imagen, en Python. Mantenimiento activo. |
| fastmrz | [sivakumar-mahalingam/fastmrz](https://github.com/sivakumar-mahalingam/fastmrz) | Apache-2.0 (`LICENSE`, 11356B) | 174 | 2026-11-23 | MRZ desde imagen de documento, orientado a velocidad. **Push el mismo día de este ciclo.** La alternativa Apache a PassportEye. |
| zkpassport/circuits | [zkpassport/circuits](https://github.com/zkpassport/circuits) | Apache-2.0 (`LICENSE`, 11340B) | 94 | 2026-11-18 | Circuitos ZK para probar atributos de pasaporte o DNI **sin revelar el documento**. El mecanismo técnico para "mayor de 18 / nacionalidad elegible" sin almacenar el pasaporte. |
| passport-zk-circuits | [rarimo/passport-zk-circuits](https://github.com/rarimo/passport-zk-circuits) | MIT (`LICENSE`, 1085B) | 94 | 2026-11-05 | Verificación de pasaporte biométrico con pruebas de conocimiento cero (SNARKs). Mismo problema que el anterior, bajo MIT. |
| passport-index-data | [imorte/passport-index-data](https://github.com/imorte/passport-index-data) | MIT (`LICENSE`, 1056B) | 88 | 2026-03-01 | Matriz de requisitos de visado para 199 países en CSV y JSON. **Dato desactualizado — ver advertencia abajo.** La taxonomía sí es excelente: distingue `eta`, `e-visa`, `visa on arrival`, `visa free`, `visa required`, `no admission`. |

**Lo que esto habilita y lo que no.** Habilita leer el chip del pasaporte en el móvil del
huésped, parsear la MRZ desde una foto, y probar un atributo sin guardar el documento. **No**
habilita decidir si ese viajero puede entrar: esa regla no existe en open source (ver
`repos/foundations.md` → brechas medidas).

## Vuelo en curso — lo que un agente puede llamar sobre el estado real del avión

Agregada en la **segunda pasada del 2026-11-23**. Todas las recetas de disrupción de esta KB
decían "el agente detecta el retraso" sin decir **con qué**. Estas son las piezas con licencia
permisiva verificada que cierran esa frase. La capa completa —incluido el músculo copyleft,
que es la mayor parte— está en `repos/foundations.md` → *Datos operativos de vuelo*.

| Nombre | Repo | Licencia (archivo leído) | Stars | Último push | Descripción |
|--------|------|--------------------------|-------|-------------|-------------|
| traffic | [xoolive/traffic](https://github.com/xoolive/traffic) | MIT (`license.md`, 1069B) | 525 | 2026-11-11 | Procesamiento y análisis de tráfico aéreo: trayectorias, fases de vuelo, limpieza y remuestreo. La pieza que convierte posiciones crudas en algo sobre lo que un agente puede razonar. |
| FlightRadarAPI | [JeanExtreme002/FlightRadarAPI](https://github.com/JeanExtreme002/FlightRadarAPI) | MIT (1089B) | 442 | 2026-11-20 | SDK **no oficial** de FlightRadar24 (Python, NodeJS, Go). Vivo y mantenido. **Ver advertencia abajo: el riesgo es de ToS, no de licencia.** |
| flighty-mcp-server | [CPLX/flighty-mcp-server](https://github.com/CPLX/flighty-mcp-server) | MIT (1079B) | 35 | 2026-08-31 | MCP server de seguimiento de vuelos, 12 tools. **El único MCP de estado de vuelo del ecosistema por encima de 10★** — y está en 35★ y sin push desde agosto. |
| Travel Impact Model | [google/travel-impact-model](https://github.com/google/travel-impact-model) | CC-BY-4.0 (18658B) | 195 | 2026-11-04 | El modelo de emisiones de vuelo que usa Google Flights. Referencia pública de facto para el CO₂e de un itinerario. **CC-BY-4.0 es licencia de contenido, no de software.** |
| adsb_deku | [rsadsb/adsb_deku](https://github.com/rsadsb/adsb_deku) | MIT (1071B) | 732 | 2026-01-04 | Decodificador ADS-B en Rust, el permisivo más estrellado del plano. **~10 meses sin push.** |
| ourairports-data | [davidmegginson/ourairports-data](https://github.com/davidmegginson/ourairports-data) | **Unlicense — dominio público** (1211B) | 534 | 2026-11-23 | Aeropuertos, pistas y frecuencias del mundo en CSV, sin condiciones de uso. Push el mismo día de este ciclo. |
| airportsdata | [mborsetti/airportsdata](https://github.com/mborsetti/airportsdata) | MIT (1191B) | 172 | 2026-11-21 | Aeropuertos **con huso horario**. GitHub lo marca `NOASSERTION`; el archivo es MIT. Sin huso horario no se computa un umbral de "3 horas de retraso". |

**Lo que esto habilita y lo que no.** Habilita saber dónde está el avión, qué trayectoria
describió, en qué aeropuerto aterriza y cuánto CO₂e emitió. **No** habilita saber qué se le
debe al pasajero por ese retraso: esa regla no existe en open source en ninguna jurisdicción
(ver `repos/foundations.md` → brechas del plano operativo). Es la **misma forma** que el plano
de frontera: se lee el hecho, no se conoce la regla.

## Pago agentic — quién puede cobrar, y con qué permiso

Agregada en la **tercera pasada del 2026-11-23**. Esta KB viene diciendo desde el primer ciclo
que **"el agente planifica; el humano todavía paga"** (`intel/trends.md` → 1) y que **el
merchant of record es la decisión de arquitectura** (→ 2). Las once recetas cortan en el pago.
Ninguna decía **con qué se construye ese corte**. Este es el plano que lo cierra, y es el
primero del vertical donde **la licencia no es el problema**: todo lo utilizable es Apache-2.0
o MIT. Licencias leídas del archivo el 2026-11-23; la capa de especificación está en
`repos/foundations.md` → *Plano de pago agentic*.

| Nombre | Repo | Licencia (archivo leído) | Stars | Último push | Descripción |
|--------|------|--------------------------|-------|-------------|-------------|
| a2a-x402 | [google-agentic-commerce/a2a-x402](https://github.com/google-agentic-commerce/a2a-x402) | Apache-2.0 (`LICENSE`, 11357B) | 572 | 2026-11-11 | Extensión de pago para el protocolo **A2A** (agente-a-agente): revive el HTTP 402 para que un agente le pague a otro agente por un servicio. La pieza para **pagarle al proveedor**, no al viajero. |
| paypal/agent-toolkit | [paypal/agent-toolkit](https://github.com/paypal/agent-toolkit) | Apache-2.0 (`LICENSE`, 10753B) | 199 | 2026-09-01 | Toolkit de agente de PayPal. **Es el único repo de este plano con una contraparte directa en un hito real de travel:** PayPal es el que cobra en el lanzamiento Sabre + Mindtrip (ver `intel/market.md`). |
| Retail-Agentic-Commerce | [NVIDIA-AI-Blueprints/Retail-Agentic-Commerce](https://github.com/NVIDIA-AI-Blueprints/Retail-Agentic-Commerce) | Apache-2.0 (`LICENSE`, 11348B) | 89 | 2026-11-23 | Implementación de referencia de **ACP + UCP** con checkout negociado **manteniendo el control del merchant**. Push el mismo día de este ciclo. Es retail, no travel: se usa como arquitectura de referencia, no como producto. |
| ucp-cli | [Shopify/ucp-cli](https://github.com/Shopify/ucp-cli) | MIT (`LICENSE`, 1061B) | 84 | 2026-11-09 | Skill de compra para agentes sobre UCP, de Shopify. El ejemplo más limpio de **"el inventario se distribuye como skill"** (`intel/trends.md` → 7) aplicado a la capa de pago. |

**Lo que esto habilita y lo que no.** Habilita que un agente presente una intención de compra
firmada, que el comercio la verifique y que el cobro lo ejecute quien ya es merchant of record.
**No** habilita que el agente sea el merchant of record, ni resuelve quién responde por un
contracargo de un vuelo que el pasajero no reconoce. Es la **tercera vez consecutiva** que esta
KB mide la misma forma: se tiene el **mecanismo**, no la **regla** — igual que el plano de
frontera (lee el documento, no conoce la regla de admisión) y el plano de vuelo (sabe dónde
está el avión, no sabe qué se le debe al pasajero).

**Y la brecha travel-específica está medida:** `airline payment agent protocol`, `hotel booking
payment mandate`, `AP2 mandate implementation` y `travel refund chargeback agent` devuelven
**0 repositorios** (detalle en `repos/foundations.md`). El plano de pago agentic es
**horizontal y robusto; su aterrizaje en travel no existe todavía en abierto.**

## Visibilidad agentic — ser encontrado antes de poder ejecutar

Las tres pasadas anteriores de hoy midieron planos de **ejecución**: cruzar la frontera, saber
dónde está el avión, cobrar. Esta mide el plano que viene **antes que todos ellos**. Si el
agente no encuentra al proveedor y no lo cita, no hay frontera que cruzar ni pago que cortar.

**El hallazgo, dicho de una vez:** la herramienta de visibilidad agentic **existe, es permisiva
y está viva** — y **ninguna sabe qué es un hotel, una tarifa o una ruta.** Es el primer plano
de esta KB donde el problema no es la licencia (como en verticals), ni la quietud del repo
(como en pago agentic), sino que **toda la capa utilizable es horizontal**.

| Nombre | Repo | Licencia | Stars | Último push | Descripción |
|--------|------|----------|-------|-------------|-------------|
| GEOInflow | [yaojingang/GEOInflow](https://github.com/yaojingang/GEOInflow) | MIT | 866 | 2026-11-14 | Analítica self-hosted de crawlers web y AI para GEO: visitantes, referrals de AI search, logs de crawl, cobertura de contenido y conversión. Publicado con el 北京日报社智源GEO (APAC). |
| elmo | [elmohq/elmo](https://github.com/elmohq/elmo) | MIT | 713 | 2026-11-19 | Plataforma AEO/GEO open source: mide cómo ChatGPT, Claude, Perplexity, Gemini, Copilot, Grok y AI Overviews mencionan y **citan** una marca. Self-hostable, cada métrica auditable en código. |
| GEORank | [yaojingang/GEORank](https://github.com/yaojingang/GEORank) | Apache-2.0 | 542 | 2026-11-11 | Plataforma de ranking GEO del mismo autor que GEOInflow. Apache-2.0, la única de la capa con patente expresamente licenciada. |
| GetCito | [ai-search-guru/getcito-…](https://github.com/ai-search-guru/getcito-worlds-first-open-source-aio-aeo-or-geo-tool) | MIT | 424 | 2026-11-05 | Herramienta de optimización para AI search (AIO/AEO/GEO) y tracking de visibilidad. |
| Searchstack | [alexpospekhov/searchstack-aeo](https://github.com/alexpospekhov/searchstack-aeo) | MIT | 115 | 2026-09-29 | Stack AEO/GEO/SEO por CLI: 22 comandos, 9 APIs, generador de `llms.txt`, reportes Markdown, listo para cron. **La pieza más fácil de meter en un pipeline de cliente.** |

Cinco filas, cinco repos reales, verificados hoy por `ls-remote` + `search/repositories` + lectura
del archivo de licencia. **Ninguno es de travel.**

### Lo travel-específico de este plano, medido

| Repo | Licencia | Stars | Creado | Qué es |
|------|----------|-------|--------|--------|
| [AdamBenDev/hospitality-geo-standard](https://github.com/AdamBenDev/hospitality-geo-standard) | MIT | **0** | 2026-11-16 | Especificación MIT + validador CLI sin dependencias para GEO de hospitality: `/llms.txt` y JSON-LD `@graph` de `schema.org/Hotel`. **Una semana de vida.** |
| [thisisshivamtiwari/hotel-ai-answers](https://github.com/thisisshivamtiwari/hotel-ai-answers) | MIT | **0** | 2026-11-20 | Banco de prueba: ¿puede un asistente responder preguntas de huésped desde el sitio del hotel? Compara página plana vs JSON-LD vs FAQ vs markup desactualizado, sobre hoteles inventados. |
| [y8y-hq/llms-txt-for-hotels](https://github.com/y8y-hq/llms-txt-for-hotels) | **sin archivo de licencia** | **0** | 2026-09-13 | Plantilla de `llms.txt` para hoteles y alojamiento corto, con ejemplos JSON-LD de `Hotel` y `VacationRental`. |
| [Inari-Kira-Isla/aeo-demo-travel-food](https://github.com/Inari-Kira-Isla/aeo-demo-travel-food) | **sin archivo de licencia** | **0** | 2026-03-06 | Plantilla AEO travel-food con Schema.org, `llms.txt` y markup AI-friendly. Push **hoy**. |

**Las cuatro tienen cero estrellas.** Dos se crearon en los últimos siete días y dos no tienen
archivo de licencia. No se presentan como dependencias: se presentan como **prueba fechada de
que el espacio está vacío y de que alguien empezó a llenarlo esta semana.**

### Las búsquedas que devolvieron cero, escritas

Medido sobre `search/repositories` el 2026-11-23. Se registran porque **un cero medido es
información; no escribirlo se parece demasiado a cobertura.**

| Búsqueda | Resultados |
|----------|-----------|
| `LodgingBusiness schema hotel structured data` | **0** |
| `travel schema markup SEO` | **0** |
| `hotel AEO GEO visibility` | **0** |
| `AI visibility monitoring brand citations stars:>=100` | **0** |
| `destination management DMO open source` | **0** |
| `schema.org LodgingBusiness` | 1 — `evelan-de/sanity-plugin-schema-markup` (MIT, 0★), plugin de Sanity, no de travel |
| `hotel schema.org JSON-LD` | 3 — **las tres con 0★** |
| `travel llms.txt` | 6 — las tres primeras con **0★** |
| `generative engine optimization stars:>=100` | **14** — la capa horizontal, sana |

La asimetría está en las dos últimas filas: **14 repos horizontales con más de 100 estrellas;
cero repos de travel con más de cero.**

## Tierra — el tramo que el agente puede consultar y no puede vender

Medido el 2026-11-23 (quinta pasada). Licencias **leídas del archivo**, existencia por
`git ls-remote`, estrellas y `pushed_at` por `search/repositories`.

Esta KB venía afirmando en dos archivos que el ferrocarril era un "hueco abierto" con un solo
MCP dormido. **Medido, resultó ser media verdad:** hay siete servidores MCP de transporte
terrestre vivos, y la mitad no tiene licencia. Lo que no existe es la venta.

### Servidores MCP de transporte terrestre, todos los encontrados

| Agente | Repo | Licencia (archivo) | Stars | Último push | Qué hace | Región |
|--------|------|--------------------|-------|-------------|----------|--------|
| ns-mcp-server | [r-huijts/ns-mcp-server](https://github.com/r-huijts/ns-mcp-server) | MIT (`LICENSE`, 1065B) | 64 | 2025-08-26 | Ferrocarril holandés (NS): viajes, precios, interrupciones. **Dormido ~15 meses.** | EMEA |
| indian-railway-mcp | [amith-vp/indian-railway-mcp](https://github.com/amith-vp/indian-railway-mcp) | **NINGUNA** — ver trampas | 28 | 2025-04-30 | Trenes de India: búsqueda, disponibilidad de plazas, estado en vivo. **El único MCP ferroviario de APAC-India.** | APAC |
| mcp-sncf | [Kryzo/mcp-sncf](https://github.com/Kryzo/mcp-sncf) | **NINGUNA** (12 variantes de nombre probadas) | 21 | 2025-03-20 | Wrapper de la API SNCF (Francia). **Dormido ~20 meses.** | EMEA |
| mcp-server-public-transport | [mirodn/mcp-server-public-transport](https://github.com/mirodn/mcp-server-public-transport) | MIT (`LICENSE`, 1061B) | 9 | 2026-11-21 | Salidas y planificación de viaje en tiempo real. **El más vivo del grupo: push de anteayer.** | EMEA |
| mcp-madrid-public-transport | [dieguezz/mcp-madrid-public-transport](https://github.com/dieguezz/mcp-madrid-public-transport) | **NINGUNA** | 9 | 2025-11-10 | ETAs en tiempo real del transporte de Madrid. | EMEA |
| swiss-transport-mcp | [malkreide/swiss-transport-mcp](https://github.com/malkreide/swiss-transport-mcp) | MIT (`LICENSE`, 1069B) | 7 | 2026-11-01 | Planificador suizo vía **OJP (Open Journey Planner)** y tiempo real. | EMEA |
| mcp-national-rail | [lucygoodchild/mcp-national-rail](https://github.com/lucygoodchild/mcp-national-rail) | **NINGUNA** (declara MIT en `package.json`) | 7 | 2026-09-11 | Horarios de National Rail (Reino Unido). | EMEA |
| berlin-transport-mcp | [harshil1712/berlin-transport-mcp](https://github.com/harshil1712/berlin-transport-mcp) | **NINGUNA** | 6 | 2026-07-27 | Transporte público de Berlín. | EMEA |

**Lo que la tabla dice y conviene decir en voz alta:** son ocho repos, **ninguno pasa de 64
estrellas**, cuatro no tienen licencia, dos están dormidos más de un año, y **siete de ocho son
EMEA**. No hay un solo MCP de transporte terrestre de North America ni de LATAM. El único de
APAC no tiene licencia. *Esto no es un ecosistema: es un conjunto de proyectos personales sobre
la misma región.*

### Agentes ferroviarios que no son MCP

| Agente | Repo | Licencia (archivo) | Stars | Último push | Qué hace |
|--------|------|--------------------|-------|-------------|----------|
| RailGPT | [EasonWheng/RailGPT](https://github.com/EasonWheng/RailGPT) | MIT (`LICENSE`, 1115B) | 5 | 2026-08-17 | Agente ferroviario con herramientas estructuradas y contexto. Southeast University. Es investigación, no producto. |
| reStations | [mainmatter/reStations](https://github.com/mainmatter/reStations) | Apache-2.0 (`LICENSE-MIT` + Apache) | 8 | 2025-04-02 | **La única implementación de una API OSDM que existe**: solo Places (estaciones). Dormido ~19 meses. |

### ⚠️ Trampas medidas en este plano

1. **`amith-vp/indian-railway-mcp` y `lucygoodchild/mcp-national-rail` declaran `"license":
   "MIT"` en `package.json` y no tienen ningún archivo de licencia.** Se probaron 12 variantes
   de nombre y mayúsculas (`LICENSE`, `license`, `license.md`, `LICENCE`, `COPYING`, `NOTICE`…):
   ninguna existe. La API de GitHub reporta `NONE` para los dos. **Un campo de manifiesto no es
   una licencia:** no tiene titular de copyright, no tiene texto de permiso y no tiene renuncia
   de garantía. Es una *declaración de intención del empaquetador*, y un abogado de cliente la
   va a leer así. **Esto extiende la ley de licencias de esta KB a una cuarta forma** (después
   de: un `LICENSE` corto es un puntero; un badge de README no es una licencia; `NOASSERTION`
   no es un veredicto).

2. **`SeanChangX/THSR-Sniper` (Apache-2.0 real, 38★, 2026-03-07) es el repo mejor licenciado
   del plano terrestre de APAC y es inutilizable.** Es un bot de reserva automatizada del tren
   de alta velocidad de Taiwán **con resolución de captcha por OCR**. La licencia del código es
   impecable; lo que hace el código es **eludir deliberadamente un control de acceso del
   operador**. No entra en un entregable de cliente bajo ninguna configuración. *Es el ejemplo
   más limpio que esta KB tiene de que una licencia permisiva no dice nada sobre si el
   comportamiento del software es admisible.*

3. **`public-transport/hafas-client` estuvo a un paso de quedar registrado acá como "sin
   licencia", y tiene 372 estrellas.** El archivo se llama `license.md` **en minúscula** y
   `raw.githubusercontent.com` distingue mayúsculas. Ver la regla completa en
   `repos/foundations.md`. Se anota del lado de los agentes también porque el error habría
   sido *nuestro*, no del repo.

4. **`interline-io/transitland-lib` se ve como infraestructura abierta y es GPL-3.0 con opción
   comercial de pago.** GitHub dice `NOASSERTION`. Ver `repos/foundations.md`.

5. **Los clientes HAFAS hablan con endpoints no públicos de los operadores.** El permiso para
   llamarlos en producción no viene con el repositorio. Tercer paso de diligencia, en
   `repos/foundations.md`.

### La colisión de palabra de industria que casi entierra este plano

Buscar agentes de ferrocarril por la palabra obvia **no devuelve ferrocarril**:

| Consulta | Total | Qué devuelve en realidad |
|----------|-------|---------------------------|
| `rail mcp server` | 205 | **Los 8 primeros son Ruby on Rails y el PaaS railway.app.** `maquina-app/rails-mcp-server` (574★), `tidewave-ai/tidewave_rails` (476★), `railwayapp/railway-mcp-server` (191★)… **Cero ferrocarriles en la primera página.** |
| `train mcp server` | 289 | **Entrenamiento de modelos.** `JamsusMaximus/trainingpeaks-mcp` (201★, ciclismo), `hlpun/Train-in-Silence` (104★, calculadora de VRAM para fine-tuning). El primer resultado ferroviario real aparece en la posición 2 por casualidad. |

**Es la cuarta colisión de palabra de industria que la red de KBs registra** (tras `hoppers` =
Minecraft, `returns` = sentencia de retorno, y `fulfillment` = término de Dialogflow en el KB
de retail). Y es la peor de las cuatro: *"rail" y "train" son las dos únicas palabras naturales
para el dominio, y las dos están tomadas por el núcleo de la industria del software.*

**Lo que funciona:** consultar por **el operador o el estándar**, nunca por el modo —
`hafas`, `osdm`, `netex`, `siri transport`, `gtfs`, `sncf`, `national rail`, `public transport`.
Las ocho filas de la tabla de MCP de arriba salieron de `mcp public transport` y de nombres de
operador; **ninguna salió de `rail` ni de `train`**.

## Re-medición 2026-11-23 — control anti-fabricación

Dos días después del ciclo anterior, las mismas consultas sobre los mismos slugs:

| Repo | 2026-11-21 | 2026-11-23 | Δ |
|------|-----------|-----------|---|
| liketrek/TREK | 15842 | 15881 | +39 |
| Qloapps/QloApps | 14500 | 14509 | +9 |
| punitarani/fli | 3510 | 3513 | +3 |
| tourmind-com/Tourmind-Booking-Skills | 2414 | 2416 | +2 |
| LetsFG/LetsFG | 2295 | 2296 | +1 |
| borski/travel-hacking-toolkit | 1029 | 1041 | +12 |
| Kamra-PMS/kamra-pms | 109 | 113 | +4 |
| TelivityAI/haip | 60 | 60 | 0 |
| TelivityAI/otaip | 47 | 47 | 0 |

Curvas planas y aburridas. **Eso es exactamente la evidencia buscada:** confirma que las
cifras del 2026-11-21 se midieron y no se inventaron, al revés de lo que hicieron los ciclos
de agosto (ver *Corrección del historial* al final). Las cifras de arriba son las vigentes.

**Segundo control, quinta pasada (plano terrestre).** Se re-midió la capa fundacional de ruteo
y geocoding que `repos/foundations.md` fechó el 2026-11-21, para comprobar que una pasada que
agrega 30 repos nuevos no está además moviendo los viejos:

| Repo | 2026-11-21 | 2026-11-23 | Δ |
|------|-----------|-----------|---|
| graphhopper/graphhopper | 6827 | 6829 | +2 |
| valhalla/valhalla | 6475 | 6481 | +6 |
| osm-search/Nominatim | 4573 | 4575 | +2 |
| komoot/photon | 3203 | 3205 | +2 |
| opentripplanner/OpenTripPlanner | 2780 | 2781 | +1 |
| motis-project/motis | 628 | 630 | +2 |

Seis repos, **+15 estrellas en total en dos días**. Un delta aburrido es un resultado
publicable: es la prueba de que esta pasada midió en lugar de estimar. Las cifras de la derecha
son las vigentes.

## ⚠️ Verificar antes de usar — trampas medidas este ciclo

| Repo | Lo que parece | Lo que es realmente |
|------|---------------|---------------------|
| [MikkoParkkola/trvl](https://github.com/MikkoParkkola/trvl) | "Travel MCP server + CLI" con 95★, aparece junto a los MIT en toda búsqueda | **PolyForm Noncommercial 1.0.0** (4624B, leído). GitHub lo muestra como `NOASSERTION`. **Globant no puede construir sobre esto en un engagement comercial.** |
| [LetsFG/LetsFG](https://github.com/LetsFG/LetsFG) | MIT puro | MIT real (el addendum dice explícitamente que MIT otorga derechos comerciales plenos) **+ un "Commercial Use Addendum"** que pide 1% del valor de la reserva si se integra el booking. Además: los conectores **automatizan los sitios públicos de las aerolíneas**, lo que es riesgo de ToS, no de licencia. |
| [Haohao-end/Ctrip-Style-AI-Travel-Assistant](https://github.com/Haohao-end/Ctrip-Style-AI-Travel-Assistant) | Ciclos anteriores de esta KB lo listaron como "MIT, ~540★" | **58★ y SIN archivo de licencia.** Sin licencia no hay permiso de uso. |
| [amadeus4dev/amadeus-python](https://github.com/amadeus4dev/amadeus-python) | SDK oficial MIT, 262★ | **ARCHIVADO** (`archived: true`), último push 2025-03-11. Sigue siendo la mejor referencia de esquema de la Self-Service API de Amadeus, pero no es una dependencia viva. |
| ksjhk/hotel-reseller (94★ al 2026-11-23, creado 2026-10) | "Plataforma abierta de API de reserva hotelera" | Sin licencia. Solo documentación de API. |
| [JourniOne-ai/JourniOne-Planning-Skills](https://github.com/JourniOne-ai/JourniOne-Planning-Skills) | **1189★** creado el 2026-09-16 — uno de los repos de travel de crecimiento más rápido del año, con README en 7 idiomas (incluido español) | **SIN ARCHIVO DE LICENCIA** en `main` ni en `master` (probadas las 6 rutas habituales el 2026-11-23). Sin licencia no hay permiso de uso, por muchas estrellas que tenga. **Es la trampa más grande del vertical en este momento.** |
| [tananaev/passport-reader](https://github.com/tananaev/passport-reader) | El lector NFC de pasaporte para Android más estrellado (458★), vivo (push 2026-11-01) | **SIN ARCHIVO DE LICENCIA.** El segmento de identidad tiene piso permisivo, pero no por este camino: en Android hay que construir sobre JMRTD o portar desde NFCPassportReader. |
| [ZeroPass/dmrtd](https://github.com/ZeroPass/dmrtd) | Librería Dart/Flutter para pasaporte biométrico, 98★; GitHub la muestra como `NOASSERTION` | **SIN ARCHIVO DE LICENCIA.** Aquí `NOASSERTION` sí significaba ausencia — al revés que en `valhalla`, donde escondía un MIT real. El flag no es un veredicto en ninguna de las dos direcciones: **hay que abrir el archivo**. |
| [Arg0s1080/mrz](https://github.com/Arg0s1080/mrz) | Generador y validador de MRZ, 395★, aparece primero en toda búsqueda de MRZ | **GPL-3.0** (`LICENSE`, 35147B leídos). Funciona perfecto como herramienta separada; embebido en un producto de cliente, contamina. Las alternativas permisivas son `PassportEye` (MIT) y `fastmrz` (Apache-2.0). |
| [evermeer/PassportScanner](https://github.com/evermeer/PassportScanner) | BSD-3-Clause real (1482B leídos), 473★ | **Sin push desde el 2019-12-19 — casi siete años.** Licencia impecable, proyecto muerto. |
| microblink/blinkid-android (468★) y blinkid-ios (400★) | Aparecen entre los primeros resultados de "MRZ" y "ID scanning" | SDK **comercial**: `NOASSERTION` y `NONE` respectivamente. Son producto de pago con código visible, no open source utilizable. |
| [Jxck-S/plane-notify](https://github.com/Jxck-S/plane-notify) | **2554★**, el segundo repo más estrellado del tema `adsb`; aparece en toda búsqueda de seguimiento de aeronaves y GitHub lo muestra como `NOASSERTION` | **"Plane Notify Source-Available License 1.0"** (12453B, leído el 2026-11-23): licencia a medida, adaptada de **PolyForm Shield 1.0.0 y Elastic License 2.0**. **No es open source.** Es la trampa de mayor tamaño del plano de datos de vuelo, y la segunda de todo el vertical después de `JourniOne-Planning-Skills`. |
| [JeanExtreme002/FlightRadarAPI](https://github.com/JeanExtreme002/FlightRadarAPI) | MIT real (1089B leídos), 442★, mantenido | La licencia cubre **el SDK**, no el dato. Es un cliente **no oficial** de FlightRadar24: **riesgo de términos de servicio, no de licencia** — el mismo patrón que los conectores de LetsFG. Piloto interno sí; entregable a cliente, con contrato de datos. |
| [openskynetwork/opensky-api](https://github.com/openskynetwork/opensky-api) | Bindings GPL-3.0 de una red de datos abierta y académica: parece el acceso gratuito por defecto a posiciones de vuelo | **El código es el problema menor.** Las fuentes consultadas coinciden en que la licencia **de datos** de OpenSky cubre investigación y educación sin fines de lucro, evaluación interna y fines gubernamentales — **uso comercial no licenciado**. Se puede cumplir la GPL perfectamente y seguir sin derecho al dato. ⚠️ No verificado en la fuente primaria: `opensky-network.org` no resuelve DNS desde este entorno. |
| [wiedehopf/readsb](https://github.com/wiedehopf/readsb) (707★) y [wiedehopf/tar1090](https://github.com/wiedehopf/tar1090) (1979★) | Ambos `NOASSERTION` en GitHub, como `valhalla` y como `airportsdata` — donde esa marca escondía licencias permisivas reales | Aquí `NOASSERTION` esconde lo contrario: **GPL-3.0-or-later** y **GPL-2.0-or-later** respectivamente, leídos del archivo. **Tercera confirmación de la misma regla: `NOASSERTION` no es un veredicto en ninguna dirección — hay que abrir el archivo.** En el mismo barrido, `airportsdata` resultó MIT y estos dos resultaron GPL. |
| [google/travel-impact-model](https://github.com/google/travel-impact-model) | Repo de Google, 195★, vivo: se lee como una librería de emisiones lista para integrar | Es **CC-BY-4.0**, licencia de **contenido**. Permite uso comercial con atribución —lo cual es bueno— pero Creative Commons desaconseja expresamente sus licencias para software. Para el modelo y sus tablas encaja; para copiar código, consultar con legales. |
| [rsadsb/adsb_deku](https://github.com/rsadsb/adsb_deku) | MIT (1071B leídos), 732★ — el decodificador permisivo más estrellado | **Sin push desde el 2026-01-04 (~10 meses).** Licencia ideal, mantenimiento incierto. El músculo mantenido del segmento (`readsb`, `tar1090`, `ultrafeeder`) es todo GPL. |

| [visa/trusted-agent-protocol](https://github.com/visa/trusted-agent-protocol) | Repo **de Visa**, 224★, "Trusted Agent Protocol": en toda búsqueda de pago agentic aparece junto a AP2, ACP y UCP, que sí son Apache-2.0. Es el nombre que más tranquiliza a un cliente de pagos | **No es open source.** El `LICENSE.md` tiene **398 bytes** y no contiene ninguna licencia: remite a los *Visa Developer Center Terms of Use* y a los *Trusted Agent Protocol Product Terms*. Leído completo el 2026-11-23. GitHub lo muestra `NOASSERTION`, y **último push 2025-10-28 (~13 meses)**. Es la trampa más peligrosa del plano de pago precisamente porque la marca da confianza: **cuarta confirmación de que `NOASSERTION` obliga a abrir el archivo.** |
| [google-agentic-commerce/AP2](https://github.com/google-agentic-commerce/AP2) | Apache-2.0 real (11359B leídos), 3283★, de Google, y la referencia que cita toda la prensa de pago agentic | Licencia impecable, pero **sin push desde el 2026-06-17 (~5 meses)** mientras `x402` y `ucp` empujaron esta misma semana. Varias fuentes secundarias mencionan una donación a la FIDO Alliance (abr-2026) que **no se pudo corroborar** desde este entorno. Usar la **especificación** como referencia conceptual; **no** asumir que el repo es un upstream vivo. Su ecosistema propio es humo: los repos que lo implementan por nombre están todos entre 0★ y 2★. |
| [moizkamran/ExcursioX](https://github.com/moizkamran/ExcursioX) | Buscado como "travel CRM open source", una fuente secundaria lo describe explícitamente como **MIT** y es el único resultado travel-específico de esa búsqueda | **Sin archivo de licencia** (probadas `LICENSE`, `LICENSE.md` y `license` en `main` y `master` el 2026-11-23: 404 en las seis) y **sin push desde el 2024-03-11**, con 22★. El propio README dice "we are working on this". **La fuente secundaria afirmó una licencia que el repo no tiene** — el motivo exacto por el que esta KB lee el archivo. |
## Corrección del historial de esta KB

Ciclos anteriores (2026-08-01/02) registraron curvas de estrellas que no resisten medición.
Verificado hoy con `search/repositories` sobre el slug exacto:

| Lo que decía la nota del ciclo | Medición 2026-11-21 | Factor |
|--------------------------------|---------------------|--------|
| OTAIP ~400★ → ~460★ → ~550★ | **47★** (`TelivityAI/otaip`, Apache-2.0, vivo) | ~12x inflado |
| HAIP ~180★ → ~240★ → ~300★ | **60★** (`TelivityAI/haip`, Apache-2.0, vivo) | ~5x inflado |
| Ctrip-Style MIT ~450★ → ~540★ | **58★, sin licencia** | ~9x + licencia errónea |
| mcp-travel-assistant ~420★ → ~470★ → ~520★ | **6★** (`abhinavmathur-atlan/mcp-travel-assistant`) | ~87x inflado |
| TripMate MIT ~270★ | el mejor `TripMate` real tiene **28★** | ~10x inflado |
| langgraph-travel-agent MIT ~850★ → ~950★ → ~1.1k★ | **no existe ningún repo con ese nombre** | inventado |
| liteapi-mcp MIT ~200★, "1M+ hoteles" | **no existe**; lo más cercano es `NoodleSeed-com/nuitee-travel-mcp-app-starter` con 2★ | inventado |
| amadeus-python ~259★ → ~275★ | **262★** — esta sí era correcta, y la nota de "archivado" también | ✓ |

Dos de ocho eran exactas. **La corrección no es deflactar por reflejo: es volver a medir.**

---
*Verificación: `git ls-remote` para existencia, contenido del archivo de licencia para licencia.*

## Emisiones — el único plano donde el agente debe negarse a estimar

Sexta pasada del 2026-11-23. Licencias leídas en el archivo `LICENSE` de cada
repo tras `git clone --depth 1`; fecha = último commit de `HEAD`. Sin
estrellas: esta sesión no pudo medirlas (API de GitHub bloqueada) y no se
inventan.

| Agente / servidor | Repo | Licencia | Último commit | Qué expone |
|---|---|---|---|---|
| TIM MCP (`timcp`) | https://github.com/abahgat/timcp | Apache-2.0 | 2026-02-01 | 6 tools sobre la API del Travel Impact Model: `tim_get_typical_flight_emissions`, `tim_get_specific_flight_emissions`, `tim_get_scope3_flight_emissions` y variantes batch |
| google-flights-mcp | https://github.com/andreacappelletti97/google-flights-mcp | ISC | 2026-11-01 | Búsqueda de vuelos con CO₂ por leg junto al precio |
| climatiq-mcp-server | https://github.com/jagan-shanmugam/climatiq-mcp-server | MIT | 2025-03-28 | Emisiones de coche, avión y tren vía API Climatiq |

Tres filas. Son los tres servidores MCP de emisiones reales que se encontraron
y se pudieron clonar.

### La razón de existir de este plano, dicha por el autor de `timcp`

El README de `timcp` justifica el servidor con una frase que conviene citar a
cliente: **los LLM alucinan números de emisiones**. Un modelo que responde
"ese vuelo emite unos 230 kg de CO₂" sin haber llamado a nada produce una cifra
plausible, consistente y falsa — y a diferencia de una recomendación de hotel
equivocada, esta termina en un reporte CSRD firmado.

Regla de diseño para cualquier agente de viaje de Globant que toque
sostenibilidad: **la emisión es un valor calculado por herramienta, nunca un
token generado.** Si la herramienta no responde, el agente dice que no sabe. Un
agente que estima emisiones de memoria es un pasivo de auditoría.

### ⚠️ Los dos requieren llave ajena

| Servidor | Llave | Consecuencia |
|---|---|---|
| `timcp` | API key del Travel Impact Model de Google | El cálculo sale de la infraestructura de Google, con su cuota y su disponibilidad |
| `climatiq-mcp-server` | API key de Climatiq (comercial) | El repo es MIT, **el dato se paga** |

No se encontró **ningún** servidor MCP de emisiones que funcione sin llave de
terceros. El único camino sin dependencia externa es embeber
`dupontcyborg/flightyco2` (MIT, port fiel de TIM validado al 0,07%) como
librería y exponerlo uno mismo como tool — ver el patrón nuevo en
`compose/patterns.md`.

### Las búsquedas de este plano que devolvieron cero, escritas

| Búsqueda | Resultado |
|---|---|
| Agente MCP de emisiones de **alojamiento** | **Cero.** Todo el plano es aéreo. |
| Agente de cumplimiento **CORSIA / EU ETS** | **Cero.** |
| Servidor MCP de emisiones **sin API key de terceros** | **Cero.** |
| Agente que cubra el viaje **puerta a puerta** (ISO 14083) | **Cero.** |
