---
industry: travel
region: Global
updated: 2026-11-21
---

# 📈 Agentes trending — Travel & Hospitality

> **Archivo APPEND-ONLY.** Cada ciclo agrega una sección fechada arriba y conserva la
> historia debajo. Reescribir el archivo destruye la tendencia que el archivo existe
> para registrar.
> Este archivo sigue **agentes y skills**. Para repos de infraestructura ver `repos/trending.md`
> (hasta hoy los dos archivos eran copias idénticas; desde este ciclo son distintos).

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
