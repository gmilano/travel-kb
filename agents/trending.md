---
industry: travel
region: Global
updated: 2026-11-23
---

# 📈 Agentes trending — Travel & Hospitality

> **Archivo APPEND-ONLY.** Cada ciclo agrega una sección fechada arriba y conserva la
> historia debajo. Reescribir el archivo destruye la tendencia que el archivo existe
> para registrar.
> Este archivo sigue **agentes y skills**. Para repos de infraestructura ver `repos/trending.md`
> (hasta hoy los dos archivos eran copias idénticas; desde este ciclo son distintos).

## 2026-11-23 — segunda pasada (plano operativo de vuelo)

Segundo ciclo del mismo día. **No reemplaza a la pasada anterior**: la sección de la mañana
(plano de frontera) queda intacta debajo. Foco de esta pasada: **de dónde sale el dato de
vuelo** que todas las recetas de disrupción de esta KB venían dando por supuesto.
Verificación: 15/15 slugs nuevos vivos por `git ls-remote`, métricas por
`search/repositories`, licencias **leídas del archivo**.

| Nombre | Repo | Licencia (archivo leído) | Stars | Último push | Qué cambió |
|--------|------|--------------------------|-------|-------------|------------|
| ourairports-data | [davidmegginson/ourairports-data](https://github.com/davidmegginson/ourairports-data) | **Unlicense — dominio público** (1211B) | 534 | 2026-11-23 | Push **hoy**. Entra a la KB por primera vez. Es el único activo de todo el vertical travel **sin ninguna condición de uso**: ni atribución, ni copyleft, ni contrato. |
| traffic | [xoolive/traffic](https://github.com/xoolive/traffic) | MIT (`license.md` minúscula, 1069B) | 525 | 2026-11-11 | Entra por primera vez. La pieza permisiva central del plano de vuelo. **Segunda vez en dos días que la licencia aparece en una ruta no estándar** — después de `license.txt` en Kamra. |
| airportsdata | [mborsetti/airportsdata](https://github.com/mborsetti/airportsdata) | **MIT** (1191B) — GitHub dice `NOASSERTION` | 172 | 2026-11-21 | Entra por primera vez. Tercer caso registrado de `NOASSERTION` escondiendo una licencia permisiva real (tras `valhalla` y `odoo`). |
| plane-notify | [Jxck-S/plane-notify](https://github.com/Jxck-S/plane-notify) | **Source-Available 1.0 — NO open source** (12453B) | 2554 | 2026-11-13 | **El repo más estrellado que entra a esta KB este ciclo, y entra a la tabla de trampas.** Licencia propia derivada de PolyForm Shield + Elastic License 2.0. GitHub lo muestra `NOASSERTION`. |
| flighty-mcp-server | [CPLX/flighty-mcp-server](https://github.com/CPLX/flighty-mcp-server) | MIT (1079B) | 35 | 2026-08-31 | Entra por primera vez, y como **medición de escasez**: es el **único** MCP server de estado de vuelo por encima de 10★ en todo GitHub. El dato más consultado del vertical tiene un solo servidor MCP, con 35★ y tres meses sin push. |
| Travel Impact Model | [google/travel-impact-model](https://github.com/google/travel-impact-model) | **CC-BY-4.0** (18658B) | 195 | 2026-11-04 | Entra por primera vez. Licencia de **contenido**, no de software: el matiz que decide si se puede copiar código de ahí. |

**Lo que esta pasada agrega a la tendencia, dicho como tendencia y no como lista:** el ciclo
de la mañana encontró un plano (frontera) cuyo piso open source es **permisivo, vivo y con más
de un proveedor por problema**. Esta pasada encontró el plano vecino —datos de vuelo— con la
**distribución inversa**: el músculo mantenido (`tar1090` 1979★, `readsb` 707★, `pyModeS`
674★, `ultrafeeder` 608★, `opensky-api` 476★, `openflights` 1686★) es **todo copyleft**, y lo
permisivo es la periferia: datasets de referencia y una caja de herramientas MIT. Dos planos
adyacentes del mismo vertical, medidos con el mismo método con 7 horas de diferencia,
repartidos al revés. **La lectura para Globant no es "travel es copyleft" ni "travel es
permisivo": es que la licencia se distribuye por capa, y hay que medirla por capa.**

## 2026-11-23

Ciclo enfocado en el **plano de frontera e identidad del viajero**. Todas las filas
verificadas hoy: existencia y métricas por `search/repositories`, licencia **leyendo el
archivo** por `raw.githubusercontent.com`.

| Nombre | Repo | Licencia | Stars | Creado | Último push | Qué cambió |
|--------|------|----------|-------|--------|-------------|------------|
| JourniOne Planning Skills | [JourniOne-ai/JourniOne-Planning-Skills](https://github.com/JourniOne-ai/JourniOne-Planning-Skills) | **NINGUNA** | 1189 | 2026-09-16 | 2026-10-28 | **1189★ en nueve semanas** — el crecimiento más rápido del vertical este año, y **sin archivo de licencia**. README en 7 idiomas (en, zh-CN, ja, es, ko, fr, ar): el primer proyecto de travel que trata el español como idioma de lanzamiento, no de traducción tardía. Inutilizable hasta que publiquen licencia. **Vale la pena volver a mirarlo el próximo ciclo: si licencia MIT, pasa directo a `agents/top.md`.** |
| fastmrz | [sivakumar-mahalingam/fastmrz](https://github.com/sivakumar-mahalingam/fastmrz) | Apache-2.0 | 174 | — | 2026-11-23 | Push **hoy**. Extracción de MRZ desde imagen bajo Apache-2.0: la salida permisiva frente a `Arg0s1080/mrz` (GPL-3.0, 395★), que es lo que devuelve primero toda búsqueda de MRZ. |
| NFCPassportReader | [AndyQ/NFCPassportReader](https://github.com/AndyQ/NFCPassportReader) | MIT | 867 | — | 2026-11-16 | El lector de pasaporte electrónico de referencia en iOS, vivo y MIT. Entra a la KB por primera vez: el plano de identidad nunca se había mirado. |
| PassportEye | [konstantint/PassportEye](https://github.com/konstantint/PassportEye) | MIT | 471 | — | 2026-11-22 | Push anteayer tras años de madurez. Parser de MRZ en Python, MIT. |
| zkpassport/circuits | [zkpassport/circuits](https://github.com/zkpassport/circuits) | Apache-2.0 | 94 | — | 2026-11-18 | Pruebas de atributo de pasaporte sin revelar el documento. El único mecanismo medido que permite "verificar sin almacenar". |
| passport-zk-circuits | [rarimo/passport-zk-circuits](https://github.com/rarimo/passport-zk-circuits) | MIT | 94 | — | 2026-11-05 | Mismo problema, bajo MIT. Dos implementaciones independientes con 94★ cada una: el segmento ZK-identidad tiene competencia real, no un único proyecto.|

**Observación del ciclo — el espejo de la observación anterior.** El 2026-11-21 esta KB
registró que *de los agentes nuevos con tracción, ninguno reserva*. Hoy, mirando un plano
distinto: **de todo lo que sí tiene código permisivo y vivo en travel, nada decide.** Los
repos de identidad leen el documento (NFC, MRZ) y prueban atributos (ZK), pero **ninguno
responde "¿este viajero puede entrar a este país?"**. Igual que en el pago, el open source
llega hasta el borde de la decisión y se detiene. La diferencia es que acá el borde no lo
puso la desconfianza del consumidor: lo puso que la regla de admisión es un contrato
comercial (Timatic) y una competencia soberana.

**Trampa de keyword re-medida, y empeoró.** La consulta
`travel OR trip OR itinerary OR hotel OR flight created:>2026-10-01 stars:>=25` devuelve hoy
25 repos y **ninguno es de la industria travel**: un simulador de vuelo vibe-codeado (367★),
una guía de leveling de WoW (351★), un fix de rendimiento de Oblivion (507★), geolocalización
Doppler de ADS-B (696★), arte de drones y un proxy. Novedad de este ciclo: **ahora contamina
también el boom de tooling agentic** — `scasella/claude-flightdeck` (339★, un dashboard para
Claude Code) y `globalmpc/vibe-preflight` (74★, un chequeo pre-deploy) entran en los primeros
puestos por las palabras *flight* y *preflight*. La contaminación de keyword no es estática:
crece con cada moda que tome prestado el vocabulario de la aviación.

---

## 2026-11-21

Lo nuevo de las últimas semanas. Todas las filas verificadas hoy por `git ls-remote` +
`search/repositories`.

| Nombre | Repo | Licencia | Stars | Creado | Último push | Qué cambió |
|--------|------|----------|-------|--------|-------------|------------|
| jianhao-travel-planner | [awangwang123/jianhao-travel-planner](https://github.com/awangwang123/jianhao-travel-planner) | MIT | 449 | 2026-09-23 | 2026-11-16 | 449★ en dos meses. Skill de itinerario con verificación cruzada multi-fuente — vende la *verificabilidad*, no la generación. Señal fuerte de APAC. |
| travel-plan-viz | [zexuanw958-svg/travel-plan-viz](https://github.com/zexuanw958-svg/travel-plan-viz) | MIT | 415 | 2026-06-13 | 2026-11-19 | Entrega el itinerario como HTML offline de un archivo. El problema que resuelve es "el viajero no tiene señal", no "el LLM no sabe planificar". |
| Tourmind Booking Skills | [tourmind-com/Tourmind-Booking-Skills](https://github.com/tourmind-com/Tourmind-Booking-Skills) | MIT | 2414 | — | 2026-11-20 | Un proveedor B2B publicando sus propias agent skills de booking bajo MIT. Patrón nuevo: el inventario llega como skill, no como API. |
| travel-agent (browser) | [Prism-Shadow/travel-agent](https://github.com/Prism-Shadow/travel-agent) | Apache-2.0 | 52 | 2026-08-31 | 2026-09-08 | Opera sitios reales en el browser y **se detiene en la página de pago**. Reconoce el límite real: se puede navegar, no comprar. |
| personalized-travel-guide-skill | [TokenHungryMash/personalized-travel-guide-skill](https://github.com/TokenHungryMash/personalized-travel-guide-skill) | MIT | 81 | 2026-09-04 | 2026-11-13 | Genera el manual de viaje como web mobile. Mismo patrón que travel-plan-viz: el valor está en el artefacto entregado. |
| trip-planner-skill | [skywain/trip-planner-skill](https://github.com/skywain/trip-planner-skill) | MIT | 51 | 2026-08-15 | 2026-10-10 | Portabilidad explícita entre Claude Code, Codex, Gemini CLI, Cursor y Copilot. La neutralidad de runtime empieza a ser un feature vendible. |
| RollingGo Hotel MCP (Global) | [RollingGo-AI/RollingGo-Hotel-MCP-Global](https://github.com/RollingGo-AI/RollingGo-Hotel-MCP-Global) | MIT | 90 | 2026-08-05 | 2026-11-19 | 2M+ hoteles a tarifa mayorista vía MCP. **Es el sucesor renombrado de `DIDA-AI/Dida-hotel-MCP-CN`**, que figura en la historia de abajo y hoy está muerto. |
| viajante | [felipebasurto/viajante](https://github.com/felipebasurto/viajante) | MIT | 60 | 2026-08-10 | 2026-11-19 | Búsqueda de vuelo+hotel para terminal/Python/asistentes. |
| OTAIP | [TelivityAI/otaip](https://github.com/TelivityAI/otaip) | Apache-2.0 | 47 | — | 2026-11-21 | Push hoy mismo. Sigue siendo chico (47★, no ~550★ como registraron ciclos previos) pero es el único intento de plataforma de orquestación específica de travel. |

**Observación del ciclo:** de los agentes nuevos con tracción, **ninguno reserva**. Planifican,
verifican, renderizan y buscan. El que más se acerca (`Prism-Shadow/travel-agent`) se detiene
deliberadamente en el pago. La capacidad escasa no es el agente — es el acceso tipado y
transaccional al inventario.

**Trampa de keyword medida hoy:** la consulta `travel OR trip OR hotel OR flight created:>2026-10-15 stars:>=15`
devuelve 48 repos, y los de arriba son un simulador de vuelo (`Rolandjg/fableflight`, 359★), un
mod de Oblivion (508★), una herramienta de geolocalización Doppler de ADS-B (684★), un proxy
(`SukkaW/hikyaku`, 115★) y arte generativo de drones. **Ninguno es travel.** Lo mismo con
"time travel for AI agents" (`OrcaReplay`, 1070★), que aparece primero en casi toda búsqueda de
"travel AI agent". Verificar que la fila pertenezca a la *industria*, no al *keyword*.

---

## 2026-07-02 *(historia — conservada, con auditoría al 2026-11-21)*

Estas filas las produjo un pipeline automático sin verificación. Se conservan porque la
historia es el valor del archivo, con el resultado de medirlas hoy.

| Nombre | Licencia registrada | Stars registrados | Estado 2026-11-21 |
|--------|--------------------|-------------------|-------------------|
| [voyant-travel/voyant](https://github.com/voyant-travel/voyant) | Apache-2.0 | 5 | ❌ **MUERTO** (`ls-remote` falla). Estaba listado **primero**. |
| [s6s8/provodnik.app](https://github.com/s6s8/provodnik.app) | ? | 0 | ❌ **MUERTO** |
| [UjjwalSaini07/Wander-Desk](https://github.com/UjjwalSaini07/Wander-Desk) | MIT | 1 | ✅ vivo |
| [liu-dongfang/flight-deal-finder-showcase](https://github.com/liu-dongfang/flight-deal-finder-showcase) | MIT | 0 | ✅ vivo |
| [DIDA-AI/Dida-hotel-MCP-CN](https://github.com/DIDA-AI/Dida-hotel-MCP-CN) | MIT | 0 | ❌ **MUERTO** — rebrandeado a `RollingGo-AI/RollingGo-hotel-MCP-CN` (61★, vivo). Un repo muerto puede ser una mudanza, no una desaparición. |
| [SilasUTK/siam-on-cloud](https://github.com/SilasUTK/siam-on-cloud) | ? | 0 | ❌ **MUERTO** |
| [PAC0119/staywisee](https://github.com/PAC0119/staywisee) | ? | 0 | ✅ vivo, sin licencia |
| [atlasforcn/startup-luggage-guardian](https://github.com/atlasforcn/startup-luggage-guardian) | ? | 0 | ✅ vivo, sin licencia |
| [thatskiff33/AlpineClubBookingsNZ](https://github.com/thatskiff33/AlpineClubBookingsNZ) | MIT | 3 | ✅ vivo |
| [jdpangilinan02/family-book](https://github.com/jdpangilinan02/family-book) | MIT | 0 | ❌ **MUERTO** — y nunca fue travel: era un árbol genealógico self-hosted. Colisión de keyword. |

**Auditoría: 5 de 10 filas están muertas hoy**, y al menos una (`family-book`) nunca perteneció
a la industria. Ocho de diez tenían 0–3 estrellas. Un pipeline que ordena por "trending" sin
piso de estrellas ni chequeo de dominio produce ruido con forma de datos.

---
*Append-only. No reescribir las secciones de arriba: agregar una nueva fechada.*
