---
industry: travel
region: Global
updated: 2026-11-21
---

# 🏭 Verticales de partida — Travel & Hospitality

> Plataformas verticales reales y funcionales, customizables con una capa agentic arriba.
> Modelo: partir de algo que ya opera un hotel o una agencia, no de un framework vacío.
> Todas verificadas el 2026-11-21: existencia, estrellas y **licencia leída del archivo**.

## Plataformas recomendadas

| Plataforma | Repo | Licencia (verificada) | Stars | Stack | Caso de uso |
|------------|------|----------------------|-------|-------|-------------|
| **QloApps** | [Qloapps/QloApps](https://github.com/Qloapps/QloApps) | **OSL-3.0 el core + AFL-3.0 los módulos** | 14500 | PHP (fork de PrestaShop), MySQL | PMS + booking engine + sitio del hotel + channel manager. El "Odoo del hotel": lo más maduro y probado del vertical. **La asimetría de licencia es la clave: los módulos son AFL-3.0 (permisiva), así que la extensión propietaria va en un módulo, no en el core.** |
| **TREK** | [liketrek/TREK](https://github.com/liketrek/TREK) | **AGPL-3.0** (34524B leídos) | 15842 | TypeScript, MCP server incluido | Planificador de viaje completo: colaboración en tiempo real, bookings, presupuestos, packing. Trae su propio MCP server. **AGPL-3.0 = copyleft de red: si se ofrece como servicio, el fuente modificado se debe publicar.** Excelente para PoC y producto interno; revisar con legales antes de un SaaS a cliente. |
| **Odoo** | [odoo/odoo](https://github.com/odoo/odoo) | **LGPL-3.0** (leído del `LICENSE`; GitHub reporta `NOASSERTION`) | 55999 | Python, PostgreSQL | Back-office de agencia de viajes y tour operador: CRM, facturación, contabilidad, compras, RRHH. **LGPL-3.0 significa que los módulos propietarios SÍ están permitidos** — el dato más útil y más mal reportado del espacio. Cubre el hueco de "no existe ERP de travel open source" con un ERP genérico más módulos. |
| **Kamra PMS** | [Kamra-PMS/kamra-pms](https://github.com/Kamra-PMS/kamra-pms) | **AGPL-3.0** (en `license.txt`, minúscula) | 109 | — | PMS de hotel y alquiler de corto plazo que se declara "agentic-AI-ready". Push diario. Chico pero es el único PMS diseñado desde el inicio para que un agente lo opere. |
| **HAIP** | [TelivityAI/haip](https://github.com/TelivityAI/haip) | **Apache-2.0** (texto completo) | 60 | TypeScript, NestJS, PostgreSQL, Drizzle | PMS hotelero API-first con motor de reserva directa. **La única opción de PMS con licencia permisiva.** Chico (60★, no ~300★ como registraron ciclos previos), pero si el cliente exige licencia permisiva es la única puerta. |
| **Headway** | [headwaymaps/headway](https://github.com/headwaymaps/headway) | Apache-2.0 | 3022 | Docker, OSM | Stack de mapas self-hosted (tiles + geocoding + ruteo). No es travel per se, pero resuelve el requisito recurrente de "no podemos mandar ubicaciones de huéspedes a Google". |
| **SyncZen Cloud** | [Felix-au/SyncZen-Cloud](https://github.com/Felix-au/SyncZen-Cloud) | MIT | 47 | Next.js | PMS y dashboard de check-in. Chico, pero MIT y moderno: buena base para un piloto de check-in conversacional. |
| **open-hotel-pms** | [peeraseepat-cell/open-hotel-pms](https://github.com/peeraseepat-cell/open-hotel-pms) | MIT | 6 | Next.js + Supabase | PMS operations-first para hoteles independientes. 6★: tratar como referencia de esquema, no como base de producción. |

## ⚠️ Lo que los listados recomiendan y no conviene tomar

| Plataforma | Por qué aparece | Por qué no |
|------------|-----------------|------------|
| [antonkarasbiz/qloapps-hotel-booking](https://github.com/antonkarasbiz/qloapps-hotel-booking) | 59★, aparece **primero** al buscar "open source hotel PMS booking engine" y se describe igual que el original | Es un **fork** de QloApps, no el upstream. Último push 2026-09-13 frente al 2026-11-20 del original. Partir del fork es heredar el mantenimiento de otro. |
| [digital-druid/hoteldruid](https://github.com/digital-druid/hoteldruid) | Citado en todo listado de "mejores PMS open source 2026" | Mirror de GitHub **sin push desde 2018-07-01** (19★). El proyecto upstream sigue vivo fuera de GitHub, pero este repo no es un punto de partida. Además es AGPL-3.0 y solo back-office: no trae booking engine público. |

## Cómo customizar con AI

El patrón que funciona con estas plataformas, en orden:

1. **No forkear el core.** QloApps se extiende con un módulo (AFL-3.0); Odoo con un addon
   (LGPL-3.0 permite que sea propietario). Forkear el core convierte cada upgrade upstream en
   un merge manual.
2. **Exponer el sistema como MCP server** antes de escribir un agente. TREK, Kamra, HAIP y
   OTAIP ya traen el suyo; QloApps y Odoo no, y ahí está el trabajo real del engagement.
3. **Agentes especializados sobre las tools tipadas**, no sobre la base de datos. El agente
   debe llamar `search_availability`, no escribir SQL.
4. **Human-in-the-loop obligatorio en el pago.** No es una preferencia de diseño: es lo que
   hacen hoy las aerolíneas (United mantiene la intervención humana en la compra) y lo que
   la evidencia de confianza del consumidor exige (ver `intel/trends.md`).

---
*Ver también: `repos/foundations.md` (ruteo y datos) y `compose/patterns.md` (recetas concretas).*
