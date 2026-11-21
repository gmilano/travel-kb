---
industry: travel
region: Global
updated: 2026-11-21
---

# 📈 Repos trending — Travel & Hospitality

> **Archivo APPEND-ONLY.** Sección fechada nueva arriba, historia debajo.
> Este archivo sigue **repos de infraestructura y plataforma**. Para agentes y skills ver
> `agents/trending.md`. Hasta el 2026-11-21 ambos archivos eran copias idénticas; desde este
> ciclo tienen contenido distinto.

## 2026-11-21

Movimiento en la capa de plataforma, no de agente. Verificado hoy.

| Repo | Licencia | Stars | Último push | Qué cambió |
|------|----------|-------|-------------|------------|
| [liketrek/TREK](https://github.com/liketrek/TREK) | AGPL-3.0 | 15842 | 2026-11-20 | **El repo de travel más grande del ecosistema open source hoy.** Planificador completo con colaboración en tiempo real, bookings, presupuestos, packing list y MCP server "AI-ready". Creado 2026-03-19: 15.8k★ en ocho meses. AGPL-3.0 verificado (34524B) — copyleft de red, decisivo para un SaaS. |
| [Qloapps/QloApps](https://github.com/Qloapps/QloApps) | OSL-3.0 (core) / AFL-3.0 (módulos) | 14500 | 2026-11-20 | Sigue siendo el PMS + booking engine open source más maduro, y sigue activo. |
| [punitarani/fli](https://github.com/punitarani/fli) | MIT | 3510 | 2026-11-11 | Se consolidó como el acceso de facto a inventario aéreo sin contrato de GDS. |
| [headwaymaps/headway](https://github.com/headwaymaps/headway) | Apache-2.0 | 3022 | 2026-11-21 | Push hoy. Stack de mapas self-hosted completo: relevante cuando el cliente no puede enviar ubicaciones de huéspedes a una API de terceros. |
| [Kamra-PMS/kamra-pms](https://github.com/Kamra-PMS/kamra-pms) | AGPL-3.0 | 109 | 2026-11-21 | Push hoy. Se presenta como "el primer PMS open source agentic-AI-ready". 109★ desde julio 2026. Licencia en `license.txt` (minúscula) — el probe habitual de `LICENSE` no la encuentra. |
| [motis-project/motis](https://github.com/motis-project/motis) | MIT | 628 | 2026-11-20 | Ruteo multimodal + geocoding + tiles en un binario, bajo MIT. La salida permisiva frente a OTP (LGPL) y Nominatim (GPL). |
| [BlinkTagInc/node-gtfs](https://github.com/BlinkTagInc/node-gtfs) | MIT | 506 | 2026-11-17 | Mantenimiento activo del puente GTFS → SQL. |
| [TelivityAI/haip](https://github.com/TelivityAI/haip) | Apache-2.0 | 60 | 2026-11-19 | PMS hotelero API-first en TypeScript/NestJS. 60★ (no ~300★ como registraron ciclos previos). La licencia Apache está completa aunque el archivo pese 10760B en lugar de 11357B — es espaciado, no texto faltante. |

**Observación del ciclo:** el crecimiento está en **plataforma vertical con MCP incorporado**
(TREK, Kamra, HAIP, OTAIP), no en frameworks de agentes nuevos. El patrón que se repite es:
sistema operativo real + servidor MCP propio. Para Globant esto es favorable — significa que
la capa agentic se enchufa en lugar de construirse.

**Nota de licencia del ciclo:** los tres repos con más tracción del vertical (TREK 15.8k AGPL-3.0,
QloApps 14.5k OSL-3.0, Kamra 109 AGPL-3.0) son **todos copyleft**. Los permisivos son las piezas
de infraestructura (graphhopper, valhalla, photon, motis, fli). Esa asimetría define la
arquitectura: plataforma copyleft como servicio separado, lógica propietaria del cliente en los
componentes permisivos.

---

## 2026-07-02 *(historia — conservada, con auditoría al 2026-11-21)*

Esta sección era idéntica a la de `agents/trending.md`, lo que significa que el pipeline escribía
el mismo query en dos archivos. Se conserva por integridad del historial.

| Repo | Licencia registrada | Stars registrados | Estado 2026-11-21 |
|------|--------------------|-------------------|-------------------|
| [voyant-travel/voyant](https://github.com/voyant-travel/voyant) | Apache-2.0 | 5 | ❌ **MUERTO** |
| [s6s8/provodnik.app](https://github.com/s6s8/provodnik.app) | ? | 0 | ❌ **MUERTO** |
| [UjjwalSaini07/Wander-Desk](https://github.com/UjjwalSaini07/Wander-Desk) | MIT | 1 | ✅ vivo |
| [liu-dongfang/flight-deal-finder-showcase](https://github.com/liu-dongfang/flight-deal-finder-showcase) | MIT | 0 | ✅ vivo |
| [DIDA-AI/Dida-hotel-MCP-CN](https://github.com/DIDA-AI/Dida-hotel-MCP-CN) | MIT | 0 | ❌ **MUERTO** → rebrand a `RollingGo-AI/RollingGo-hotel-MCP-CN` |
| [SilasUTK/siam-on-cloud](https://github.com/SilasUTK/siam-on-cloud) | ? | 0 | ❌ **MUERTO** |
| [PAC0119/staywisee](https://github.com/PAC0119/staywisee) | ? | 0 | ✅ vivo, sin licencia |
| [atlasforcn/startup-luggage-guardian](https://github.com/atlasforcn/startup-luggage-guardian) | ? | 0 | ✅ vivo, sin licencia |
| [thatskiff33/AlpineClubBookingsNZ](https://github.com/thatskiff33/AlpineClubBookingsNZ) | MIT | 3 | ✅ vivo |
| [jdpangilinan02/family-book](https://github.com/jdpangilinan02/family-book) | MIT | 0 | ❌ **MUERTO**, y nunca fue travel |

Además, las dos filas que `repos/foundations.md` traía del mismo ciclo:

| Repo | Registrado como | Estado 2026-11-21 |
|------|-----------------|-------------------|
| [nicolv23/OpenHotelFR](https://github.com/nicolv23/OpenHotelFR) | "fundacional", MIT, 1★ | ✅ vivo, pero 1★ no es una base fundacional |
| [MewsSystems/fiscalizations](https://github.com/MewsSystems/fiscalizations) | "fundacional", MIT, 62★ | ✅ vivo. Es una librería .NET de **facturación fiscal** de Mews — real y útil para compliance hotelero, pero no es una base de plataforma |

---
*Append-only. No reescribir las secciones de arriba: agregar una nueva fechada.*
