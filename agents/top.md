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
