---
industry: travel
region: Global
updated: 2026-11-28
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
>
> **Séptima pasada 2026-11-23:** se agrega el **plano de accesibilidad** — el primero que
> no tenía ni una mención en la KB. Todo lo agentic que existe audita páginas; para el
> acceso físico hay **cero agentes**. Ver la sección al final.
>
> **Octava pasada 2026-11-23:** se agrega el **plano de la reseña y la confianza** — el
> insumo que todo agente de esta KB cita al recomendar un hotel, y que ninguno puede
> verificar. Tres capas en tres estados distintos (detección **vacía**, lectura
> **congelada**, procedencia **viva pero del problema de al lado**) y la **trampa inversa**
> de licencia: un badge que renderiza la licencia de otro proyecto. Ver la sección al final.

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

## Accesibilidad — el agente audita la página y no puede prometer la habitación

Séptima pasada del 2026-11-23. Es el primer plano de esta KB que **no tenía ni
una mención**: `wheelchair`, `a11y`, `axe-core` y `silla de ruedas` devolvían
cero en los ocho archivos antes de esta pasada.

**Método.** Existencia por `git ls-remote` (27/27 vivos). Estrellas y
`pushed_at` por `search/repositories` el 2026-11-23. **Licencia leída del
archivo de licencia del repo**, y dependencias leídas del `package.json` —
porque en este plano el wrapper y el motor tienen licencias distintas.

### Servidores MCP de accesibilidad — todos auditan **páginas web**

| Servidor | Repo | Licencia (archivo) | Motor debajo | Stars | Último push | Qué hace |
|---|---|---|---|---|---|---|
| mcp-accessibility-scanner | [JustasMonkev/mcp-accessibility-scanner](https://github.com/JustasMonkev/mcp-accessibility-scanner) | MIT | `axe-core` (MPL-2.0) + Playwright | 59 | 2026-11-23 | Escaneo WCAG de una URL desde el agente, con navegador real. El más vivo del plano. |
| a11ymcp | [ronantakizawa/a11ymcp](https://github.com/ronantakizawa/a11ymcp) | MIT | `axe-core` (MPL-2.0) + Puppeteer | 97 | 2026-03-10 | Testing de accesibilidad web como tools MCP. Más estrellas, ~8 meses sin push. |
| a11y-mcp | [priyankark/a11y-mcp](https://github.com/priyankark/a11y-mcp) | **MPL-2.0** | `axe-core` (MPL-2.0) + Puppeteer | 53 | 2026-11-22 | Mismo patrón; el wrapper también es MPL — modificar sus archivos obliga a publicarlos. |

Tres filas. Son los tres servidores MCP de accesibilidad con licencia OSI que
se encontraron, se clonaron y se leyeron.

**Lo que las tres filas tienen en común, y es la tesis de este plano:** las tres
auditan **una página para un usuario ciego o con baja visión**. Ninguna sabe
nada de **un umbral, una rampa, una ducha o un ascensor**.

### ⚠️ Trampas medidas en este plano

| Repo | Lo que parece | Lo que es | Consecuencia |
|---|---|---|---|
| [ctoldigital/axuse](https://github.com/ctoldigital/axuse) | El más estrellado del plano (805★, push 2026-11-03), "accessibility-first browser & computer use for AI agents" | **PolyForm Noncommercial 1.0.0** en `package.json` | **No usar en trabajo de cliente.** Misma trampa que `trvl` en el plano de vuelo. |
| [dequelabs/axe-mcp-server-public](https://github.com/dequelabs/axe-mcp-server-public) | El servidor MCP **oficial** de Deque, autor de `axe-core`, en un repo público | `LICENSE`: **"Proprietary License … All rights reserved"** | Público ≠ abierto. Requiere contrato con Deque. |
| Los dos MCP "MIT" | MIT de punta a punta | MIT el wrapper; **`axe-core` es MPL-2.0** | Usable: MPL es copyleft **por archivo**. Usar `axe-core` sin modificar como dependencia no contamina el producto; **parchear un archivo de `axe-core` obliga a publicar ese archivo.** Hay que decirlo en el SOW. |

### Las búsquedas de este plano que devolvieron cero, escritas

| Búsqueda en `search/repositories` | Resultado |
|---|---|
| `wheelchair accessible travel agent` | **0 repos.** |
| `wheelchair routing llm` | 1 repo, 0★, sin licencia. |
| `disability travel ai` | 5 repos, **todos 0★ y sin licencia**. |
| `accessible hotel` | 170 resultados; **ninguno** es dato de accesibilidad hotelera (menús, sistemas de hospital). |
| Agente que responda "¿puedo entrar en silla de ruedas?" con fuente | **Cero.** |

**El plano físico no tiene un solo agente.** Lo que existe para él está abajo,
en `repos/foundations.md`: un vocabulario MIT (`a11yjson`), uno de la industria rico y **sin licencia**
(`OpenTravel`), dos motores de
ruteo LGPL con perfil de silla de ruedas, y un validador Apache que verifica el
grafo de una estación. El agente hay que escribirlo — ver Receta 20.

### Regla de diseño de este plano

Igual que la emisión en la sexta pasada: **la accesibilidad física es un hecho
devuelto por herramienta, con fuente y fecha de relevamiento, nunca un token
generado.** Y tiene un tercer estado que el agente no puede colapsar:
`sí / no / **desconocido**`. `OpenTripPlanner` ya lo modela así — penaliza lo
desconocido (600 por defecto) distinto que lo inaccesible conocido (3600). Un
agente que responde "sí, es accesible" porque el campo estaba vacío deja a una
persona en la puerta de un hotel.

## Reseña y confianza — el insumo que todo agente cita y ninguno puede verificar

Agregada en la **octava pasada del 2026-11-23**. Es el segundo plano, después del de
accesibilidad, **sin una sola mención previa en esta KB**: las palabras `review`,
`reputación` y `fake review` devolvían cero en los ocho archivos. Y es el plano del que
depende silenciosamente todo lo demás, porque la reseña es **el insumo que cada agente de
esta KB cita cuando recomienda un hotel**.

El hallazgo de esta pasada no es una lista de agentes: es que **no hay agentes**. Lo que hay
son tres capas separadas, medidas el 2026-11-23 con el método de siempre (`git ls-remote`
para existencia, `search/repositories` para métricas, **licencia leída del archivo**), y las
tres están en un estado distinto.

### Capa 1 — Detectar que una reseña es falsa: **vacía**

| Nombre | Repo | Licencia (archivo leído) | Stars | Último push | Estado |
|--------|------|--------------------------|-------|-------------|--------|
| Fake-Reviews-Detection | [SayamAlt/Fake-Reviews-Detection](https://github.com/SayamAlt/Fake-Reviews-Detection) | **NINGUNA** — no existe archivo de licencia en la rama default | 109 | 2022-04-14 | El más estrellado de la capa. **Sin licencia = sin derecho de uso.** 4 años sin push. |
| browser-extension (TrueStar) | [TrueStarHQ/browser-extension](https://github.com/TrueStarHQ/browser-extension) | MIT (`LICENSE`, 1064B) | 22 | 2025-09-03 | **El único MIT real de la capa, y está ARCHIVADO.** Era análisis de reseñas de Amazon en el browser. |
| fake-reviews-data | [bretthollenbeck/fake-reviews-data](https://github.com/bretthollenbeck/fake-reviews-data) | MIT (`LICENSE`, 1073B) | 12 | 2026-03-15 | Dataset de reseñas de Amazon etiquetadas real/falsa, de un paper de economía. **Vivo.** Es un dataset, no un detector. |
| OpinRank | [kavgan/OpinRank](https://github.com/kavgan/OpinRank) | **NINGUNA** | 44 | 2021-05-28 | Dataset clásico de reseñas de hoteles y autos (TripAdvisor, Edmunds). **Es el único activo hotel-específico de toda la capa, y no tiene licencia.** |

### Capa 2 — Leer qué dice la reseña: **abundante y congelada**

Aspect-Based Sentiment Analysis (ABSA) es la técnica que convierte "la habitación era chica
pero el desayuno excelente" en `habitación: negativo / desayuno: positivo`. Es exactamente lo
que un agente de travel necesita, y es la capa con más estrellas del plano. También es la más
vieja.

| Nombre | Repo | Licencia (archivo leído) | Stars | Último push | Estado |
|--------|------|--------------------------|-------|-------------|--------|
| ABSA-PyTorch | [songyouwei/ABSA-PyTorch](https://github.com/songyouwei/ABSA-PyTorch) | **NO HAY ARCHIVO** — GitHub declara `MIT`. Ver trampa abajo. | 2112 | 2023-06-12 | **ARCHIVADO.** El repo más estrellado de todo el plano, y no se puede licenciar con certeza. |
| Aspect-Based-Sentiment-Analysis (Scala) | [ScalaConsultants/Aspect-Based-Sentiment-Analysis](https://github.com/ScalaConsultants/Aspect-Based-Sentiment-Analysis) | Apache-2.0 (`LICENSE`, 11357B) | 585 | 2026-09-07 | **El único de la capa con push en 2026.** Pipeline con interpretabilidad (pesos de atención por aspecto). La pieza utilizable. |
| ABSA-BERT-pair | [HSLCY/ABSA-BERT-pair](https://github.com/HSLCY/ABSA-BERT-pair) | MIT (`LICENSE`, 1062B) | 519 | 2022-01-04 | NAACL-2019. Licencia limpia, 5 años sin push. |
| BERT-for-RRC-ABSA | [howardhsu/BERT-for-RRC-ABSA](https://github.com/howardhsu/BERT-for-RRC-ABSA) | Apache-2.0 (`LICENSE`, 11357B) | 461 | 2021-02-05 | Post-entrenamiento sobre reseñas (*review reading comprehension*). El más cercano al dominio. **Casi 6 años sin push.** |
| jiangqn/ABSA | [jiangqn/Aspect-Based-Sentiment-Analysis](https://github.com/jiangqn/Aspect-Based-Sentiment-Analysis) | MIT (`LICENSE`, 1067B) | 457 | 2024-03-27 | Colección de implementaciones. Licencia limpia. |
| BERT-E2E-ABSA | [lixin4ever/BERT-E2E-ABSA](https://github.com/lixin4ever/BERT-E2E-ABSA) | Apache-2.0 (`LICENSE`, 11357B) | 401 | 2023-07-09 | End-to-end: extrae el aspecto y lo clasifica en un paso. |

### Capa 3 — Probar de dónde vino un contenido: **viva, permisiva y del problema de al lado**

C2PA (*Coalition for Content Provenance and Authenticity*) es el estándar de procedencia
criptográfica de contenido. Es la capa más sana que esta KB midió en cualquier plano: **push
el mismo día de este ciclo** y **doble licencia MIT *o* Apache-2.0**, que deja elegir a quien
integra.

| Nombre | Repo | Licencia (archivos leídos) | Stars | Último push | Descripción |
|--------|------|----------------------------|-------|-------------|-------------|
| c2pa-rs | [contentauth/c2pa-rs](https://github.com/contentauth/c2pa-rs) | **MIT *o* Apache-2.0** (`LICENSE-MIT` 1083B + `LICENSE-APACHE`) — GitHub dice `NOASSERTION` | 454 | 2026-11-23 | Implementación de referencia en Rust: firma y verifica manifiestos de procedencia. **Push el día de este ciclo.** |
| c2pa-org/specifications | [c2pa-org/specifications](https://github.com/c2pa-org/specifications) | **CC-BY-4.0** (`LICENSE`, 18650B) | 215 | 2026-11-16 | La especificación. Licencia de **contenido, no de software** — mismo matiz que Travel Impact Model en la segunda pasada. |
| c2patool | [contentauth/c2patool](https://github.com/contentauth/c2patool) | Apache-2.0 | 174 | 2026-11-20 | CLI para firmar y verificar. La vía más corta a una prueba de concepto. |
| c2pa-python | [contentauth/c2pa-python](https://github.com/contentauth/c2pa-python) | Apache-2.0 | 110 | 2026-11-18 | Binding Python. El que encaja en un pipeline de datos de travel. |
| c2pa-js | [contentauth/c2pa-js](https://github.com/contentauth/c2pa-js) | MIT | 44 | 2026-11-23 | Verificación en el browser. **Push el día de este ciclo.** Es el que iría en una ficha de hotel. |
| c2pa-swift | [contentauth/c2pa-swift](https://github.com/contentauth/c2pa-swift) | **MIT *o* Apache-2.0** (ambos archivos presentes) — GitHub muestra solo `Apache-2.0` | 28 | 2026-11-21 | iOS. Firma la foto **en el dispositivo del huésped**, que es donde la procedencia sirve. |
| c2pa-cpp | [contentauth/c2pa-cpp](https://github.com/contentauth/c2pa-cpp) | **MIT *o* Apache-2.0** (ambos presentes) — GitHub muestra solo `Apache-2.0` | 20 | 2026-11-16 | C++. Para integrar en software de PMS o kiosco existente. |

### ⚠️ Trampas medidas en este plano

1. **`ABSA-PyTorch` (2112★): el badge de licencia del README apunta a otro proyecto.** El
   único rastro de licencia en el repo es un badge de shields.io cuya URL es
   `packagist/l/doctrine/orm.svg` — es decir, **renderiza la licencia de Doctrine ORM, un
   paquete PHP sin relación alguna con el repo**. No hay `LICENSE`, `LICENSE.md`,
   `LICENSE.txt` ni `COPYING` en la rama default (`master`, verificado uno por uno). Y pese a
   eso, la API de GitHub devuelve `MIT`. **Es la trampa inversa a todas las que esta KB
   registró hasta hoy**: hasta ahora el patrón era `NOASSERTION` escondiendo una licencia
   permisiva real (`valhalla`, `odoo`, `airportsdata`). Acá GitHub **afirma** una licencia
   donde no hay texto que la otorgue. Un badge no es una licencia.
2. **Dual licensing invisible en la API.** `c2pa-rs` trae `LICENSE-MIT` **y**
   `LICENSE-APACHE`; la API devuelve `NOASSERTION`. `c2pa-swift` y `c2pa-cpp` traen los dos
   archivos y la API muestra solo `Apache-2.0`. El efecto práctico es que **la API oculta una
   opción que el proyecto concede**: quien integra puede elegir MIT. Cuarto, quinto y sexto
   caso registrado de la etiqueta de GitHub divergiendo del archivo.
3. **`contentauth/c2pa-node` (21★, MIT) está ARCHIVADO** desde 2025-09-19, mientras
   `c2pa-js` (MIT, 44★) tiene push de hoy. Si alguien elige por nombre —"necesito Node"—
   toma el archivado. **En este org el binding vivo de JavaScript no es el que dice Node.**
4. **Las dos piezas hotel-específicas del plano no tienen licencia.** `OpinRank` (44★) y el
   único repo de análisis de reseñas de hotel con ≥30★ (`Tony607/Chinese_sentiment_analysis`,
   47★, 2017, sin licencia). Lo más cercano al dominio es lo menos usable.

### Las búsquedas de este plano que devolvieron cero o casi, escritas

| Consulta (`search/repositories`) | Resultado | Lectura |
|----------------------------------|-----------|---------|
| `fake review detection stars:>=20` | **8 repos en todo GitHub** | Y de los 8, uno es un repo de robótica que entra por la sigla `FTC`. La obligación regulatoria de cuatro regiones se apoya en **siete repos**, casi todos sin licencia y sin push desde 2022-2024. |
| `review authenticity provenance stars:>=50` | **0** | Nadie cruzó las dos palabras. La capa 3 existe para medios, no para reseñas: **hay que cruzarla a mano.** |
| `review moderation trust safety stars:>=200` | **0** | No hay infraestructura abierta de moderación de reseñas a ninguna escala. |
| `hotel review analysis stars:>=30` | **1** (sin licencia, 2017) | El vertical más dependiente de la reseña no tiene herramienta propia. |
| `review dataset hotel tripadvisor stars:>=30` | **1** (`OpinRank`, sin licencia) | No hay corpus de reseñas de hotel redistribuible. |
| `tours activities booking open source stars:>=50` | **0** | Registrado al pasar: el tercer segmento de travel tampoco tiene piso abierto. Candidato a plano futuro. |

### Regla de diseño de este plano

**El agente no puede afirmar que una reseña es auténtica, y no debe intentarlo.** No existe
la herramienta, y la regulación de 2026 castiga la afirmación falsa, no la abstención. Lo que
sí puede hacer, con lo medido arriba: (a) **citar y enlazar** la reseña en lugar de resumirla
sin rastro, (b) **declarar el volumen y la ventana temporal** sobre la que resume, y (c) **no
suprimir la cola negativa** — que es precisamente el hallazgo de Which? de julio-2026 contra
los resúmenes AI de Tripadvisor. Receta completa en `compose/patterns.md` → Recetas 22 y 23.

## Equipaje — la única pieza del viaje que es un objeto físico con cadena de custodia

**Noveno plano, sin una sola mención previa en los ocho archivos de esta KB.** Los ocho planos
anteriores (frontera, vuelo en curso, pago, visibilidad, tierra, emisiones, accesibilidad,
reseña) tratan **información sobre el viaje**. El equipaje es distinto: es **una cosa**, viaja
**separada del pasajero**, y cuando no llega, alguien tiene que responder *dónde está* con un
registro, no con una estimación. Medido el 2026-11-23.

### La corrección que ordena todo este plano, y que yo mismo tuve que hacer a mitad de camino

Empecé midiendo con la palabra de la industria y concluí que el plano estaba **vacío**:

| Búsqueda | Resultado | Lo que yo concluí | Lo que era verdad |
|----------|-----------|-------------------|-------------------|
| `BSM baggage source message` | **0 repos en todo GitHub** | "el mensaje que mueve el equipaje no tiene implementación abierta" | **Falso.** La implementación existe, en `pkg/baggage` de un repo cuya descripción nunca dice *baggage* |
| `bag tag IATA` | **0 repos en todo GitHub** | "no hay nada sobre etiquetas de equipaje" | Cierto como medición del índice; falso como medición del mundo |
| `IATA Resolution 753` | **1 repo**, 0★, sin licencia | "un solo repo nombra la norma" | Cierto, y sigue siendo cierto — pero **no** es el único que la implementa |

**La ley de método, generalizable a los doce verticales:** una búsqueda que devuelve cero es
evidencia sobre **el índice**, no sobre **el mundo**. GitHub indexa descripciones y READMEs, no
árboles de directorios. Encontré `pkg/baggage` **clonando** un repo que había aparecido bajo otra
consulta (`edifact iata type b message`) y haciendo `grep` del árbol. Es la versión fuerte de la
ley que el ciclo de retail dejó escrita como *"un directorio ausente es evidencia sobre tu
conjetura, no sobre el repo"*: aquí era un **resultado cero** el que hablaba de mi conjetura.

### La cuarta colisión de palabra de industria — y la más peligrosa de las cuatro

| Consulta | Total | Resultado #1 por estrellas | Qué es en realidad |
|----------|-------|---------------------------|--------------------|
| `baggage stars:>=10` | 25 repos | [`w3c/baggage`](https://github.com/w3c/baggage) 62★ | **Una especificación del W3C de *distributed tracing*.** `baggage` es el nombre del formato de cabecera HTTP que propaga contexto entre servicios. Nada que ver con aviación |
| `luggage stars:>=10` | 16 repos | [`bevacqua/local-storage`](https://github.com/bevacqua/local-storage) 523★ MIT | Un wrapper de `localStorage`. Entra por el emoji `:left_luggage:` en su descripción |
| `luggage stars:>=10` | — | [`unixorn/luggage`](https://github.com/unixorn/luggage) 392★ | Empaquetado de `.pkg` en macOS |
| `luggage stars:>=10` | — | [`danderfer/Comp_Sci_Sem_2`](https://github.com/danderfer/Comp_Sci_Sem_2) 229★ | El guion de *Bee Movie* ("According to all known laws of aviation…"). Entra por la palabra *aviation* |

Las tres colisiones anteriores de esta KB (hoppers de Minecraft = inventario; *returns* =
sentencias `return`; *fulfillment* = webhooks de Dialogflow) eran ruido. **Esta es peor: la
colisión es ella misma un estándar del W3C**, con repo en la organización `w3c`, 15 forks y
especificación publicada. Un compilador que ordene por estrellas y confíe en la palabra mete
**el formato de propagación de contexto distribuido del W3C** en una KB de viajes como si fuera
infraestructura de equipaje. Queda registrado como descarte explícito, no como ausencia.

**Regla:** consultar el **objeto físico y su documento** (`bag tag`, `BSM`, `AHL`, `WorldTracer`,
`Resolution 753`), nunca el sustantivo común. Y cuando el sustantivo común devuelva repos con
muchas estrellas, **leer la descripción antes que la cifra**.

### Capa de agentes de este plano — lo que existe, medido

Ninguno de estos agentes toca el equipaje. Se listan porque son **la superficie agentic
realmente disponible sobre el viaje aéreo**, y porque la Receta 25 los compone con la capa de
mensajería que sí lo toca.

| Nombre | Repo | Licencia (archivo leído) | Stars | Último push | Qué hace |
|--------|------|--------------------------|-------|-------------|----------|
| Award Travel Finder MCP | [AwardTravelFinder/mcp](https://github.com/AwardTravelFinder/mcp) | MIT (1076B) | 17 | 2026-11-20 | Servidor MCP de disponibilidad de vuelos con millas. Entra por primera vez |
| flightradar-mcp-server | [Cyreslab-AI/flightradar-mcp-server](https://github.com/Cyreslab-AI/flightradar-mcp-server) | MIT (1056B) | 7 | 2026-09-20 | MCP sobre AviationStack: estado de vuelo y horarios. **Llave ajena** |
| aviasales-mcp | [stufently/aviasales-mcp](https://github.com/stufently/aviasales-mcp) | **GPL-3.0** (35149B) | 9 | 2026-11-09 | MCP de precios vía Travelpayouts. Copyleft fuerte: se corre como servicio, no se embebe |
| disruption-rebooking-copilot | [robsarran65/disruption-rebooking-copilot](https://github.com/robsarran65/disruption-rebooking-copilot) | MIT (1075B) | 0 | 2026-08-10 | Copiloto agentic de IROPS (irregular operations) con reruteo explicable. **0★ pero es el único repo de IROPS agentic con licencia permisiva** |
| mcp-delta | [markswendsen-code/mcp-delta](https://github.com/markswendsen-code/mcp-delta) | **NO HAY ARCHIVO** en ninguna ruta estándar | 6 | 2026-03-11 | MCP de Delta Airlines. **Inusable**: sin licencia y automatiza el sitio de una aerolínea nombrada |

### Las búsquedas de este plano que devolvieron cero o casi, escritas

| Consulta | Total | Lectura |
|----------|-------|---------|
| `bag tag IATA` | **0** | La etiqueta — el documento que identifica la pieza — no tiene una sola implementación nombrada |
| `BSM baggage source message` | **0** | Ver la corrección de arriba: cero en el índice, **no** cero en el mundo |
| `chain of custody tracking stars:>=50` | **0** | El concepto central del plano no tiene ninguna librería genérica con tracción |
| `airport operations stars:>=20` | **0** | No existe software de operación aeroportuaria abierto con tracción |
| `rfid asset tracking stars:>=50` | **0** | La tecnología que la CAAC **obliga** en China (ver `intel/market.md` → APAC) no tiene capa abierta |
| `airline operations agent stars:>=10` | **0** | **No hay un solo agente de operación aérea con ≥10★.** El plano agentic de operaciones está sin abrir |
| `baggage tracking stars:>=5` | **2** | `bchhaglani/Baggage-tracking` (6★, sin licencia, último push 2019-03-21) y `ParameswarKanuparthi/...` (5★, sin licencia, 2020-05-31). **Los dos muertos y los dos sin licencia** |
| `WorldTracer` | **4** | Ninguno pasa de 0★. El sistema que la industria usa de hecho para rastrear equipaje perdido no tiene eco abierto |

### Re-medición 2026-11-23 — control anti-fabricación

Los ciclos 5, 6 y 8 de esta KB inventaron curvas de estrellas, y el ciclo 9 lo corrigió. El
control se mantiene: se re-mide lo ya escrito y **se registra el delta aunque sea aburrido**.

| Repo | Ciclo anterior | Hoy | Delta |
|------|---------------|-----|-------|
| LetsFG/LetsFG | 2296 (2026-11-23, octava pasada) | 2297 | +1 |

Un día, +1 estrella. **Registrar un delta plano es la evidencia de que esta pasada no inventó una
curva.** La licencia de `LetsFG` se re-verificó del archivo: `LICENSE` de 2173B que dice
`MIT License / Copyright (c) 2026 LetsFG (MENTAL BALANCE sp. z o.o.)`, mientras la API de GitHub
sigue devolviendo `NOASSERTION` — **lo que esta KB ya tenía escrito es correcto** (MIT real más
el addendum comercial del 1%), y no se cambia.

### Regla de diseño de este plano

Un agente **no puede decir dónde está una maleta**. Puede decir **qué registro existe sobre ella
y de cuándo es** — que es exactamente la forma de tres estados que esta KB ya adoptó para la
ficha de accesibilidad física (Receta 20): `registrado / no registrado / registro vencido`.
La Resolución 753 de IATA da los cuatro puntos de custodia y **no obliga ninguna tecnología**:
código de barras, escaneo manual u OCR son válidos. Por eso el dato siempre tiene una **hora de
último escaneo**, y un agente honesto la devuelve junto con la posición. Receta 25.

## Precio — el plano donde el agente puede calcular y no puede explicar

Décimo plano, 2026-11-23. Ninguno de los nueve anteriores lo tocó: frontera, vuelo, pago,
visibilidad, tierra, emisiones, accesibilidad, reseña y equipaje tratan **qué se vende y cómo se
entrega**. Este trata **cuánto cuesta y por qué** — la única pregunta del viaje cuya respuesta
cuatro reguladores distintos ya quieren por escrito.

### La capa de agentes de este plano — lo que existe, medido

| Nombre | Repo | Licencia (leída del archivo) | Stars | Último push | Descripción |
|--------|------|------------------------------|-------|-------------|-------------|
| revmng-mcp | [arikanatakan/revmng-mcp](https://github.com/arikanatakan/revmng-mcp) | MIT (`main/LICENSE`, «Copyright (c) 2026 Atakan Arikan») | 3 | 2026-06-17 | **El único MCP server de revenue management que existe.** Expone protección de asientos (Littlewood, EMSR-a/b, DP exacto), overbooking, pricing, grupos, length-of-stay y bid prices de red como tools. Declarado en el registro MCP como `io.github.arikanatakan/revmng-mcp`. |
| skills — `algo-price-dynamic` | [asgard-ai-platform/skills](https://github.com/asgard-ai-platform/skills) | MIT (`main/LICENSE`, «Copyright (c) 2026 Asgard Inc. (肆佳科技股份有限公司)») | 249 | 2026-06-06 | Skill de precio dinámico con referencia de revenue management incluida (`algo-price-dynamic/references/revenue-management.md`, HTTP 200 verificado). Dispara ante «surge pricing», «real-time pricing», «demand-based price adjustment». Origen APAC (Taiwán). |
| travel-agent-skills | [mtnrabi/travel-agent-skills](https://github.com/mtnrabi/travel-agent-skills) | MIT (`main/LICENSE`) | 4 | 2026-10-23 | Ocho skills de precio en vivo de vuelo y hotel, **incluida monitorización de paridad tarifaria**. Cada tarifa trae el veredicto `low \| typical \| high` de Google y un link reservable. **Ver la trampa de llave abajo.** |

**Son tres filas porque encontré tres.** No hay una cuarta que sea de viajes, tenga licencia
permisiva verificable y esté viva. Las búsquedas que lo confirman están escritas más abajo.

### La razón de existir de `revmng-mcp`, dicha por su propio autor

El README no vende el servidor como una integración más; explica un modo de falla concreto del
agente, y conviene citarlo porque es el argumento de diseño de todo este plano:

> «Agents asked to set a booking limit or evaluate a group tend to do the arithmetic themselves,
> and the standard methods are easy to get subtly wrong: a protection level computed from the wrong
> tail, a group accepted without costing the demand it displaces, EMSR confused with the optimum.»

La conclusión que saca es la regla: **el cálculo va en una biblioteca determinista, versionada y
validada que el agente llama; al agente le queda elegir el análisis y explicar el resultado.** Es
la misma separación que esta KB ya adoptó para emisiones (no estimar, llamar) y para equipaje (no
afirmar posición, devolver el registro y su hora).

### ⚠️ Trampas medidas en este plano

**1. `travel-agent-skills` es MIT sobre una red medida y ajena.** El código es MIT y está vivo,
pero las ocho skills son cliente de FlightPowers vía RapidAPI: **10 búsquedas por día gratis sin
llave**, después llave propia, después USD 10/mes por 2.500 búsquedas de vuelo o 2.000 de hotel. Es
exactamente el patrón de la tendencia 15 de este KB —la licencia del código deja de alcanzar cuando
el repo es cliente de una red— y acá además la monitorización de paridad tarifaria, que en China es
*conducta sancionable* (ver mapa de mercado, APAC), queda del lado de un tercero.

**2. `revmng-mcp` tiene 3 estrellas y un solo día de pushes.** Creado el 2026-06-16, último push el
2026-06-17. Está en PyPI, tiene CI y está validado contra ejemplos publicados, pero **no tiene
historia de mantenimiento**: cinco meses sin un commit. Se usa fijando versión, no siguiendo `main`.

**3. El *skill* de Asgard es bueno y no es de viajes.** Su «IRON LAW» exige tres flujos de datos en
tiempo real —señal de demanda, inventario, precio de competencia— y da frecuencias por industria
(minutos en ride-sharing, horas en hotel, diario en retail). Sirve como marco; no trae ni una pieza
de distribución aérea ni hotelera. Y advierte explícitamente cuándo **no** usar precio dinámico:
decisiones de precio de una sola vez, y **mercados regulados**.

### Lo que este plano exige y ningún agente open source hace

Ninguna de las tres filas de arriba **divulga** nada. Calculan el precio; no emiten el artefacto que
Nueva York, la CRD europea, las reglas de plataforma de China o los proyectos brasileños piden. La
búsqueda que lo mide está abajo y devuelve cero. **El agente de este plano puede calcular y no puede
explicar**, y esa es la frase que resume el plano entero.

### Las búsquedas de este plano que devolvieron cero o casi, escritas

| Consulta (`search/repositories`) | `total_count` | Lectura |
| --- | --- | --- |
| `price explanation transparency algorithm` | **0** | No existe la categoría. Cero, no «pocos». |
| `algorithmic pricing disclosure` | **1** | Y el único resultado (`Rastaman4e/-1`, 83★, último push 2021-04-16, sin licencia) no es del tema. |
| `personalized pricing audit` | **1** | `mizcausevic-dev/retail-decision-record-audit-str` — MIT, 0★, 2026-08-05. **Es de retail**, el vertical de al lado, no de viajes. |
| `price discrimination detection` | **2** | Ambos irrelevantes (uno de 2013, uno sin licencia). |
| `revenue management mcp server` | **7** | De los siete, **uno** es del tema: `revmng-mcp`. Los demás son AdMob, CRM y gestión de desastres. |

Una búsqueda que devuelve cero es evidencia sobre el índice, no sobre el mundo — la corrección que
ordenó el noveno plano vale igual acá, y por eso el plano se cierra clonando y leyendo, no sólo
buscando. La diferencia con equipaje es que en equipaje la implementación **estaba** escondida
(72.163 líneas de Go en `adamf/jetway`); acá, tras leer `revmng`, `revmng-mcp` y el skill de Asgard
archivo por archivo, **la divulgación sigue sin aparecer en ninguno de los tres**.

### La quinta colisión de palabra de industria, y la primera que pierde contra otro vertical de este KB

Las cuatro anteriores fueron `trip`, `gate`, `review` y `baggage` (esa última contra la spec del
W3C). La quinta es **`dynamic pricing`, y la gana energía**:

| Repo | Stars | Último push | Licencia | De qué es realmente |
| --- | --- | --- | --- | --- |
| [martinarva/dynamic_energy_cost](https://github.com/martinarva/dynamic_energy_cost) | 207 | 2026-11-21 | MIT | Costo de **electricidad** en Home Assistant |
| [corneel27/day-ahead](https://github.com/corneel27/day-ahead) | 188 | 2026-11-22 | Apache-2.0 | Optimización contra el mercado eléctrico **day-ahead** |
| [tule2236/Airbnb-Dynamic-Pricing-Optimization](https://github.com/tule2236/Airbnb-Dynamic-Pricing-Optimization) | 243 | **2018-11-14** | **SIN LICENCIA** | Sí es de viajes, y está muerto hace 8 años |

`dynamic pricing stars:>=50` devuelve **21 repos en todo GitHub**, y los dos únicos con tracción y
mantenimiento real son de tarifas eléctricas. Peor: `pricing mcp server` devuelve **1.619 repos**, y
la cabeza es costo de nube (`aws-samples`, Azure) y finanzas. **En su propio vocabulario, el precio
de viajes es un error de redondeo**, y el repo de viajes más estrellado del plano no tiene licencia.

### Regla de diseño de este plano

El motor de precio y el motor de divulgación son **dos piezas, no una**. La primera existe, es MIT y
es buena (`revmng`); la segunda no existe en ningún lado y hay que escribirla. Y la decisión de
arquitectura que las une es anterior a las dos: **si el precio se calcula desde capacidad, demanda y
tarifa —y no desde la persona— el disparador de Nueva York no se activa.** No es un truco legal: es
elegir qué entradas tiene el modelo, y es la única respuesta *estructural* en lugar de documental
que este plano permite. Recetas 28, 29 y 30.

## Comprobante fiscal — el plano donde el agente reserva y no puede facturar

**Undécima pasada, 2026-11-23.** Ninguno de los diez planos anteriores tocó el comprobante.
El plano existe porque el viaje corporativo tiene **dos documentos, no uno**: la confirmación de
la reserva, que el agente ya sabe producir, y el **comprobante fiscal**, que es el único que
recupera el IVA. No son el mismo artefacto y en 2026 ya no son el mismo régimen legal.

### El modo de falla que define el plano, y es nuevo y es agentic

La regla operativa, coincidente en toda la cobertura de viaje corporativo de 2026: **si el número
de IVA del comprador no llega al hotel en el momento de la reserva, el hotel emite un recibo de
consumidor y el IVA de esa estadía ya no se recupera.** No se arregla después. No lo arregla el
área de gastos. El dato tenía que viajar con la reserva.

Eso convierte al agente de reserva en el punto donde el IVA se pierde: **un agente que reserva
bien y no pasa la identidad fiscal del comprador destruye la recuperación antes del check-in.**
Es el primer plano de esta KB donde el daño lo causa una omisión del agente en el *happy path* —
no un error, no una alucinación: una reserva correcta sin un campo.

### La capa de agentes de este plano — lo que existe, medido

El hallazgo del plano es una **familia de servidores MCP por jurisdicción**, de un solo autor
(`cmendezs`), toda Apache-2.0, y **diez de los doce con push en los últimos siete días**.
Licencia leída de `main/LICENSE` en los doce casos, no del campo de la API.

| Servidor MCP | Licencia (archivo leído) | Stars | Último push | Jurisdicción y esquema | Región |
| --- | --- | --- | --- | --- | --- |
| [cmendezs/mcp-einvoicing-core](https://github.com/cmendezs/mcp-einvoicing-core) | Apache-2.0 | 0 | 2026-11-21 | Paquete base de los demás. Su propia descripción: *compliance logic and signing keys stay with you* | Global |
| [cmendezs/mcp-nfe-br](https://github.com/cmendezs/mcp-nfe-br) | Apache-2.0 | 1 | 2026-11-21 | NF-e / NFC-e, modelo 55/65, schema 4.0 | LATAM |
| [cmendezs/mcp-cfdi-mx](https://github.com/cmendezs/mcp-cfdi-mx) | Apache-2.0 | 0 | 2026-11-21 | CFDI 4.0 + Complemento de Pagos 2.0 | LATAM |
| [cmendezs/mcp-einvoicing-de](https://github.com/cmendezs/mcp-einvoicing-de) | Apache-2.0 | 2 | 2026-11-22 | ZUGFeRD 2.x / XRechnung 3.x | EMEA |
| [cmendezs/mcp-facturacion-electronica-es](https://github.com/cmendezs/mcp-facturacion-electronica-es) | Apache-2.0 | 3 | 2026-11-21 | Facturación electrónica española | EMEA |
| [cmendezs/mcp-ksef-pl](https://github.com/cmendezs/mcp-ksef-pl) | Apache-2.0 | 3 | 2026-11-16 | KSeF / FA(2) | EMEA |
| [cmendezs/mcp-einvoicing-be](https://github.com/cmendezs/mcp-einvoicing-be) | Apache-2.0 | 0 | 2026-11-16 | Peppol BIS 3.0 / PINT-BE / Mercurius | EMEA |
| [cmendezs/mcp-fattura-elettronica-it](https://github.com/cmendezs/mcp-fattura-elettronica-it) | Apache-2.0 | 2 | 2026-09-12 | FatturaPA / SDI | EMEA |
| [cmendezs/mcp-facture-electronique-fr](https://github.com/cmendezs/mcp-facture-electronique-fr) | Apache-2.0 | 1 | 2026-09-12 | NF XP Z12-013 | EMEA |
| [cmendezs/mcp-einvoicing-ae](https://github.com/cmendezs/mcp-einvoicing-ae) | Apache-2.0 | 3 | 2026-11-22 | PINT AE / Peppol 5-corner | EMEA |
| [cmendezs/mcp-einvoicing-in](https://github.com/cmendezs/mcp-einvoicing-in) | Apache-2.0 | 1 | 2026-11-21 | FORM GST INV-01 v1.1 / IRP-IRN | APAC |
| [cmendezs/mcp-invoicenow-sg](https://github.com/cmendezs/mcp-invoicenow-sg) | Apache-2.0 | 0 | 2026-11-22 | InvoiceNow / PINT-SG / Peppol 5-corner | APAC |

> ⚠️ **Las estrellas son las reales: entre 0 y 3.** Esta KB corrigió en el ciclo 9 curvas de
> estrellas fabricadas de pasadas anteriores, y no se repite el error. Esta familia **no tiene
> adopción medible**: su valor es la cobertura jurisdiccional y la licencia, no la madurez.
> Doce repos de un solo autor, el más viejo de septiembre de 2026, son **riesgo de autor único**.
> Se recomiendan como *referencia de esquema y punto de partida*, no como dependencia de producción.

**Otros MCP del plano, verificados uno por uno:**

| Servidor | Licencia (archivo leído) | Stars | Último push | Qué hace | Región |
| --- | --- | --- | --- | --- | --- |
| [Timbrix/mcp](https://github.com/Timbrix/mcp) | MIT | 0 | 2026-09-18 | Timbra, cancela y consulta CFDI 4.0 desde un agente. **Timbrar es el acto legal**, no el PDF | LATAM |
| [OrtaMarco/mx-fiscal-mcp-server](https://github.com/OrtaMarco/mx-fiscal-mcp-server) | MIT | 1 | 2026-11-21 | Valida RFC, CURP, CLABE, NSS y lee CFDI. **El RFC del comprador es el campo que hay que tener en la reserva** | LATAM |
| [BrasilNFe/brasilnfe-mcp](https://github.com/BrasilNFe/brasilnfe-mcp) | MIT (`master/LICENSE`) | 0 | 2026-06-12 | NF-e, NFC-e, NFS-e, CT-e, MDF-e, DC-e en lenguaje natural | LATAM |
| [DoubleH10/zatca-mcp](https://github.com/DoubleH10/zatca-mcp) | Apache-2.0 (`main/LICENSE`) | 5 | 2026-03-03 | ZATCA Arabia Saudita — el más estrellado del plano | EMEA |
| [Haresh-16/receipt-parsing-mcp](https://github.com/Haresh-16/receipt-parsing-mcp) | MIT | 0 | 2025-12-18 | Parseo de recibo y extracción de gasto | Global |
| [AuxiLabs-Auxiliobits/auxilab-mcp-expense-mgmt](https://github.com/AuxiLabs-Auxiliobits/auxilab-mcp-expense-mgmt) | MIT | 0 | 2026-08-05 | Política de gasto, parseo de recibo, clasificación y duplicados | Global |
| [MiniCodeTeam/askais-mcp](https://github.com/MiniCodeTeam/askais-mcp) | MIT | 1 | 2026-07-21 | Genera PDF de recibo. **Genera un PDF, no un comprobante fiscal** — la distinción del plano | Global |

### ⚠️ Trampas medidas en este plano

**La peor de las once pasadas: un repo que dice «free» y cuya licencia dice lo contrario.**

| Repo | Lo que dice de sí mismo | Lo que dice su archivo LICENSE | Consecuencia |
| --- | --- | --- | --- |
| [causa-prima-ai/scribo-mcp](https://github.com/causa-prima-ai/scribo-mcp) (7★) | «free, AI-native EN 16931-compliant e-invoicing» | *«All rights reserved… proprietary and confidential. No license is granted to use, copy, modify, or distribute»* | **Inusable.** Tiene archivo LICENSE, está en GitHub, y es propietario explícito |
| [causa-prima-ai/scribo-skill](https://github.com/causa-prima-ai/scribo-skill) (7★) | Skill de e-invoicing para Claude/Codex, misma descripción «free» | Mismo texto: *All rights reserved* | **Peor que el anterior**: se distribuye con la forma de un skill, el formato que se copia a un agente sin leer la licencia |
| [gflohr/e-invoice-eu](https://github.com/gflohr/e-invoice-eu) (383★, push 2026-11-23) | Generador EN 16931 (Factur-X/ZUGFeRD, UBL) | **WTFPL v2** | Libre en los hechos y **no aprobada por OSI**: varias áreas legales de cliente la rechazan por política, no por alcance. Hay que preguntar antes de proponerla |

**La trampa inversa de este plano, y se repitió cinco veces.** El campo `license` de la API de
GitHub **subdeclaró** la licencia en cinco repos de este plano y la **sobredeclaró en cero**:

| Repo | Lo que dice la API | Lo que dice el archivo |
| --- | --- | --- |
| `phax/phive-rules` | `NOASSERTION` | Apache-2.0 (`master/LICENSE`) |
| `Quittio/quittio` | `NOASSERTION` | MIT (`master/LICENSE` — **404 en `main`**) |
| `TadaSoftware/PyNFe` | `NOASSERTION` | LGPL-3.0 |
| `BrasilNFe/brasilnfe-mcp` | `NOASSERTION` | MIT (`master/LICENSE`) |
| `DoubleH10/zatca-mcp` | `NOASSERTION` | Apache-2.0 |

El patrón es el inverso del de la pasada octava, donde la trampa era un badge que **afirmaba** una
licencia inexistente. Acá descartar por `NOASSERTION` habría tirado cinco repos usables, cuatro de
ellos permisivos. **La causa medida: el archivo está en `master` y no en `main`, o empieza con una
línea de encabezado (`====`, copyright) antes del nombre de la licencia.**

### Las búsquedas de este plano que devolvieron cero o casi, escritas

| Búsqueda (`search/repositories`) | Total | Lectura |
| --- | --- | --- |
| `travel agency invoice billing system` | **2** | Uno GPL-3.0 de **2017** con 0★ (`karlomanson/tour-invoices`), uno sin licencia. **La capa vertical de facturación de viaje no existe** |
| `hotel folio invoice` | **5** | Cuatro sin licencia; el único con licencia son **plantillas** GST para hoteles indios (`roomnexa-official/hotel-gst-invoice-template`, MIT, 0★), no software |
| `per diem allowance calculator` | **0** | La categoría no existe en GitHub |
| `airline ticket invoice receipt api` | **0** | Ídem |
| `ksef faktura krajowy system` | **0** | El mandato polaco entró en febrero de 2026 y **no hay biblioteca en polaco** indexada por este término; sólo el MCP de `cmendezs` |
| `peppol access point client library` | **0** | No hay cliente de Access Point open source bajo ese nombre |
| `dbnalliance` | **1** | Y es un repo de transferencia de archivos de 2023, sin licencia. **La red de EE. UU. no tiene capa open source** |
| `travel expense report management` | **30** | Revisados los 8 primeros por estrellas: **siete sin licencia, 0–1★**. Nada usable |

### Regla de diseño de este plano

1. **El campo fiscal del comprador es parte del payload de la reserva, no del gasto.** Si el
   agente no lo tiene al momento de reservar, la recuperación del IVA ya se perdió. Va en el mismo
   objeto que las fechas y el nombre.
2. **Separar «recibo» de «comprobante fiscal» en el modelo de datos, con dos campos distintos.**
   Una confirmación de pago de hotel no es una factura: sirve para deducir el gasto y **no** para
   recuperar el IVA.
3. **El agente no firma.** La lógica de cumplimiento y las llaves de firma se quedan del lado del
   cliente — es literalmente lo que declara `mcp-einvoicing-core`, y es la postura correcta:
   timbrar, firmar o transmitir a la autoridad es un acto legal con responsable humano.
4. **Un agente no puede decir «ya facturado» sin el acuse de la autoridad.** Igual que en el plano
   del equipaje: tres estados, no dos — *emitido*, *aceptado por la autoridad*, *no se sabe*.

## Seguro y siniestro — el plano donde el acto mismo de recomendar ya está licenciado

*(duodécima pasada, 2026-11-28. Terreno virgen: antes de esta pasada las palabras `seguro`,
`siniestro`, `insurance` y `claim` aparecían 0 veces en `agents/`.)*

En los once planos anteriores el agente fallaba **por omisión**: le faltaba un campo (comprobante),
una categoría (precio), una pieza (equipaje), un vocabulario (accesibilidad). Acá falla **por
hablar**. Describir una cobertura, comparar dos pólizas o recomendar un límite es, en varias
jurisdicciones, **un acto regulado en sí mismo**, independiente de que se cobre o no:

- **EE. UU.:** el estatuto de Florida enumera seis actividades de *solicitation* que exigen
  licencia, y entre ellas están **«recomendar»** y **«comparar o interpretar coberturas»**
  *(fuente: resumen de un proveedor de voice-agents citando el estatuto; no se leyó el texto
  estatutario — **[sin verificar]**, ver «Lo que esta sesión NO pudo verificar»)*.
- **UE:** EIOPA planteó en septiembre de 2026 —en un artículo vinculado a Eurofi— si un chatbot
  que recolecta datos personales, **filtra productos o da recomendaciones** está realizando una
  **actividad de distribución de seguros** bajo la IDD. Es una pregunta abierta de la autoridad,
  **no una norma**: la IDD es tecnológicamente neutral y eso es justamente el problema.

La consecuencia operativa es dura y es nueva para esta KB: **el concierge que ya está desplegado y
que contesta «¿esto me lo cubre el seguro?» cruzó un límite de licencia sin ejecutar ninguna
transacción.** No hace falta que venda. Le basta con responder bien.

### El hallazgo que da vuelta la ley estructural de este KB

En los once planos anteriores la capa vertical agentic estaba **vacía o muerta**. Acá **existe, y
nació anteayer**: los seis repos agentic de seguro de viaje que existen fueron **creados entre el
2026-08-22 y el 2026-11-08** — catorce semanas — y **ninguno pasa de 2★** (el único con 4★ es un
DApp de blockchain). Y lo más importante: **cuatro de los seis ya traen el corte regulatorio
escrito en el propio README**, sin que ningún regulador haya cerrado la frase.

La industria escribió la baranda antes de que el regulador terminara la oración.

### Capa agentic vertical — los seis que existen, todos medidos

| Repo | Licencia **leída del archivo** | ★ / creado / push | Qué hace | El corte que **ya trae** |
|---|---|---|---|---|
| `phil-cc/voyara-travel-insurance` | **MIT** (`main/LICENSE`) | 0★ / 2026-11-08 / 2026-11-08 | MCP + **WebMCP** (Chrome 149+): «one Quote API, two agent channels» | **Es su razón de existir, dicha por el autor:** «a reference build showing how an insurer can let AI agents **quote a policy without letting them buy one**» |
| `tourclaim/tourclaim-cli` | **MIT** (`main/LICENSE`, © Copernican) | 0★ / 2026-10-04 / 2026-11-08 | CLI + SDK Python + MCP para reclamar el seguro **que viene con la tarjeta de crédito** | «the card's benefit administrator, **who decides coverage**». Y declara: en *review mode* desde octubre 2026, API/CLI/MCP crean reclamos **sintéticos** |
| `HelloSafe/travel-insurance-mcp` | ⚠️ **sin archivo de licencia** | 0★ / 2026-08-26 / 2026-08-26 | MCP **hosteado** sobre catálogo multi-aseguradora; **un solo tool: `get_quote`** | No existe tool de compra. Devuelve primas, techos de garantía y links a los documentos de póliza |
| `10Life/10life-travel-mcp` | ⚠️ **sin archivo de licencia** | 0★ / 2026-10-22 / 2026-10-22 | Hong Kong, single-trip, 3 tools **read-only** | El más explícito de los seis: «**Premiums and scores are indicative. The product page is the authority**», prohíbe nombre/teléfono/mail/documento en `callReason`, máximo 5 planes por respuesta, y anual **no disponible** |
| `Vujavujavuja/Overdoo` | **MIT** (`main/LICENSE`) | 4★ 1f / 2026-08-22 / 2026-11-16 | Seguro **paramétrico** de demora sobre Monad: aterriza 3h+ tarde → paga | El disparador es **el dato de vuelo**, no un juicio de cobertura. Por eso no necesita opinar |
| `sepehr071/iran-insurance-mcp` | ⚠️ **NO es open source** — ver trampa 1 | 2★ / 2026-11-01 / 2026-11-17 | 18 tools; compara precios **vivos** de seguro de viaje en dos marketplaces iraníes | «unofficial, read-only»; sin API key |

### Capa agentic adyacente — otra línea de negocio, misma forma, y se puede copiar

Ninguno es de viaje. Los cinco son **la forma del tool** que el plano necesita, ya escrita y
permisiva:

| Repo | Licencia (archivo) | ★ / push | Por qué importa acá |
|---|---|---|---|
| `kentaroajisaka/labor-law-mcp` | MIT | **67★ 8f** / 2026-09-14 | **El MCP de seguros más estrellado que existe no sirve un producto: sirve la *ley*** (derecho laboral y de seguridad social japonés, API e-Gov + 通達 del MHLW). La forma que gana estrellas es «el agente consulta la regla», no «el agente vende» |
| `seaworthy-io/seaworthy-mcp` | MIT | 3★ / 2026-10-21 | Seguro de invalidez con un `quote_request` *agent-callable* + datos de carrier. Publicado por una **agencia de seguros real**: el mismo movimiento de HelloSafe, con licencia |
| `chbhargavareddy/ClaimsProcessingAssistant-MCP` | MIT | 5★ / 2026-08-22 | Capacidades de procesamiento de siniestro expuestas por MCP |
| `the-up/tsb-kasko-mcp` | MIT | 4★ / 2026-11-03 | Valores de referencia de seguro vehicular turco (TSB). EMEA, y es **dato de autoridad sectorial** vía MCP |
| `mahesh7199/fnol-ai-agent` | MIT | 1★ / 2026-08-04 | FNOL (*first notice of loss*): la toma del siniestro, que es el único tramo del plano donde el agente **no** aconseja |

### Los dos *skills* chinos, y lo que prueban

Dos *Agent Skills* MIT, en chino, de octubre y noviembre de 2026. Importan porque **el corte
regulatorio llegó al vertical como *skill*, no como API** —la tendencia 7 de esta KB— y porque
**los dos se autolimitan sin que nadie los obligue**:

| Repo | Licencia | ★ / creado | La autolimitación, textual |
|---|---|---|---|
| `Zenine/china-family-insurance` | MIT | 0★ / 2026-11-20 | Da «coverage-level recommendations (insurance type and sum insured, **no product picks**)» y cierra: «This is a method and toolset, **not licensed insurance advice**» |
| `xuyue9129-ctrl/medical-insurance-product-research` | MIT | 0★ / 2026-10-28 | Pipeline **recomprobable**: ~200 productos en catálogo, 54 campos normalizados, y por cada documento archivado guarda **URL de origen, SHA256, páginas, fecha de obtención y grado de evidencia A/B/C/D** |

El segundo es, de los veinticuatro repos medidos en esta pasada, **el único que trae trazabilidad
criptográfica de la fuente de cada cláusula**. Es una pieza de método, no de producto, y es la que
hay que copiar.

### ⚠️ Trampas medidas en este plano

1. **`sepehr071/iran-insurance-mcp` no es open source, y la API no lo dice.** El campo de licencia
   de la API devuelve `NOASSERTION`. El archivo `main/LICENSE` empieza: *«Required Notice:
   Copyright (c) 2026 Sepehr Radmard. **Free for personal and non-commercial use** under the terms
   below. Commercial use…»*. Una consultoría **no puede** embeberlo en un entregable de cliente.
   Y es la **inversa de la undécima pasada**: allí `NOASSERTION` escondió cinco veces licencias
   reales y permisivas, y cero veces una restrictiva. Conclusión corregida para esta KB:
   **`NOASSERTION` no significa «probablemente permisiva». Significa «abrí el archivo», y el
   archivo puede ir para cualquiera de los dos lados.**
2. **Dos de los cinco MCP de seguro de viaje no tienen archivo de licencia — y no son software.**
   `HelloSafe/travel-insurance-mcp` y `10Life/10life-travel-mcp` son **manuales de conexión a un
   endpoint remoto ajeno** (`https://hellosafe.com/api/mcp-travel`, `https://mcp.10life.com/mcp`).
   Lo «abierto» es el endpoint, no el código: **si lo forkeás te queda un README**. No se puede
   auditar el pricing, no se puede self-hostear, y el servicio puede cambiar o cerrar sin aviso.
   Modo de falla nuevo para esta KB: *el repo existe, está vivo, y no contiene el producto.*
3. **`luciano-coelho/opin-doctor-ppgcc-ufsc`: el titular del copyright no es quien publica.**
   Licencia MIT legítima, pero el archivo dice «Copyright (c) 2025 **Open Insurance Brasil**»
   mientras el repo pertenece a una persona física dentro de un programa de posgrado de la UFSC
   (`ppgcc-ufsc`). No lo vuelve inusable; vuelve **la procedencia no verificable**, y una cesión
   MIT firmada por una entidad que no publicó el repo no es una cesión sobre la que valga la pena
   construir sin preguntar. **Cuarto modo de trampa de licencia de esta KB**, después del badge
   que miente, el archivo ausente y las tres licencias en un archivo.
4. **openIMIS confirma la causa diagnosticada en la undécima pasada.** API: `NOASSERTION`.
   Archivo `main/LICENSE.md`: **GNU AGPL v3** — precedido por la línea «The program users must
   agree to the following terms: License notices». **Es exactamente la causa que la pasada
   anterior conjeturó**: una línea de encabezado antes del nombre de la licencia y el detector se
   cae. Dos pasadas, misma causa, confirmada.

### Las búsquedas de este plano que devolvieron cero o casi, escritas

| Búsqueda (`in:name,description`) | Total | Qué había realmente |
|---|---|---|
| `travel assistance repatriation` | **0** | Cero. La asistencia en viaje —el corazón operativo del producto— no tiene **una línea** de open source |
| `medical assistance travel api` | **0** | Cero |
| `travel insurance api comparison` | 1 | Un perfil de API de un directorio, no software |
| `trip cancellation claim` | 1 | Un trabajo práctico de ML de 2022, sin licencia |
| `visa travel insurance requirement check` | 1 | Un buscador de vuelos chino, colisión de keyword |
| `travel claim assistance` | 6 | Ninguno con licencia, ninguno arriba de 1★, cuatro son sitios web de corredores |
| `ACORD insurance standard` | **3** | **Cero con licencia.** El estándar de datos del propio sector asegurador **no tiene implementación abierta** — el mismo hallazgo que OpenTravel en el plano de accesibilidad y que el organismo de estándares del plano de visibilidad |
| `open insurance brazil opin` | **1** | Un entorno local de OPIN completo (mTLS, Authorization Server), MIT, académico, push 2026-11-24 |

### Regla de diseño de este plano

El tool de seguro **no tiene dos estados ni tres: tiene tres y el tercero es nuevo en esta KB.**
No es `cubierto / no cubierto / no sé`. Es:

```
cotizado            → precio, techos de garantía y link al documento de póliza (no interpretado)
no puedo responderlo→ y acá está QUIÉN sí puede, nominado
no puedo venderlo   → el corte de binding, explícito, con el merchant/intermediario a cargo
```

Lo nuevo es el segundo estado. En los planos anteriores la negativa del agente terminaba en «no
puedo»; **acá la negativa tiene que llevar destinatario**, y hay un solo regulador en el mundo que
nombró el artefacto: la FCA obliga, desde abril de 2021, a **derivar a un directorio de
proveedores especializados** (el de MoneyHelper, del Money and Pensions Service) cuando la
cobertura se rechaza, no se ofrece o se recarga por una condición médica preexistente. Es la
única jurisdicción medida en esta pasada donde **«no puedo ayudarte» es, por norma, una respuesta
incompleta**.

Los cuatro repos que ya traen el corte (`voyara`, `tourclaim`, `10life`, `HelloSafe`) implementan
el tercer estado. **Ninguno de los seis implementa el segundo.** Ése es el hueco de producto del
plano, y está en la Receta 34.
