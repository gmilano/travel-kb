---
industry: travel
region: Global
updated: 2026-11-23
---

# 🏭 Verticales de partida — Travel & Hospitality

> Plataformas verticales reales y funcionales, customizables con una capa agentic arriba.
> Modelo: partir de algo que ya opera un hotel o una agencia, no de un framework vacío.
> Verificadas el 2026-11-21; **re-verificadas el 2026-11-23**, y una cambió de licencia en
> esas 48 horas (Kamra PMS). Existencia, estrellas y **licencia leída del archivo**.

## Plataformas recomendadas

| Plataforma | Repo | Licencia (verificada) | Stars | Stack | Caso de uso |
|------------|------|----------------------|-------|-------|-------------|
| **QloApps** | [Qloapps/QloApps](https://github.com/Qloapps/QloApps) | **OSL-3.0 el core + AFL-3.0 los módulos** | 14500 | PHP (fork de PrestaShop), MySQL | PMS + booking engine + sitio del hotel + channel manager. El "Odoo del hotel": lo más maduro y probado del vertical. **La asimetría de licencia es la clave: los módulos son AFL-3.0 (permisiva), así que la extensión propietaria va en un módulo, no en el core.** |
| **TREK** | [liketrek/TREK](https://github.com/liketrek/TREK) | **AGPL-3.0** (34524B leídos) | 15842 | TypeScript, MCP server incluido | Planificador de viaje completo: colaboración en tiempo real, bookings, presupuestos, packing. Trae su propio MCP server. **AGPL-3.0 = copyleft de red: si se ofrece como servicio, el fuente modificado se debe publicar.** Excelente para PoC y producto interno; revisar con legales antes de un SaaS a cliente. |
| **Odoo** | [odoo/odoo](https://github.com/odoo/odoo) | **LGPL-3.0** (leído del `LICENSE`; GitHub reporta `NOASSERTION`) | 55999 | Python, PostgreSQL | Back-office de agencia de viajes y tour operador: CRM, facturación, contabilidad, compras, RRHH. **LGPL-3.0 significa que los módulos propietarios SÍ están permitidos** — el dato más útil y más mal reportado del espacio. Cubre el hueco de "no existe ERP de travel open source" con un ERP genérico más módulos. |
| **Kamra PMS** | [Kamra-PMS/kamra-pms](https://github.com/Kamra-PMS/kamra-pms) | **Apache-2.0** (`license.txt`, minúscula, 11358B — **leído el 2026-11-23**) | 113 | TypeScript | PMS de hotel y alquiler de corto plazo que se declara "agentic-AI-ready". Push diario. **Relicenciado de AGPL-3.0 a Apache-2.0 el 2026-11-21** (commit `ce8dec8`). Es ahora **el PMS permisivo más grande del vertical** y el único diseñado desde el inicio para que un agente lo opere. **Recomendación por defecto para un piloto de PMS agentic.** |
| **HAIP** | [TelivityAI/haip](https://github.com/TelivityAI/haip) | **Apache-2.0** (texto completo) | 60 | TypeScript, NestJS, PostgreSQL, Drizzle | PMS hotelero API-first con motor de reserva directa. Hasta el 2026-11-21 era **la única** opción de PMS permisiva; desde el relicenciamiento de Kamra ya no lo es. Sigue siendo la opción más limpia si se quiere NestJS/Drizzle, pero con 60★ frente a 113★ es la segunda. |
| **Headway** | [headwaymaps/headway](https://github.com/headwaymaps/headway) | Apache-2.0 | 3022 | Docker, OSM | Stack de mapas self-hosted (tiles + geocoding + ruteo). No es travel per se, pero resuelve el requisito recurrente de "no podemos mandar ubicaciones de huéspedes a Google". |
| **SyncZen Cloud** | [Felix-au/SyncZen-Cloud](https://github.com/Felix-au/SyncZen-Cloud) | MIT | 47 | Next.js | PMS y dashboard de check-in. Chico, pero MIT y moderno: buena base para un piloto de check-in conversacional. |
| **open-hotel-pms** | [peeraseepat-cell/open-hotel-pms](https://github.com/peeraseepat-cell/open-hotel-pms) | MIT | 6 | Next.js + Supabase | PMS operations-first para hoteles independientes. 6★: tratar como referencia de esquema, no como base de producción. |
| **EU Digital Identity Wallet** (capa de librerías) | [eu-digital-identity-wallet](https://github.com/eu-digital-identity-wallet) | **Apache-2.0 las librerías y servicios; EUPL-1.2 las apps; CC BY 4.0 la especificación** | 66 / 64 / 47 / 43 (libs) | Kotlin, Swift, JVM | No es una plataforma de travel, es la **infraestructura de identidad del huésped en EMEA**, mantenida por la Comisión Europea. Un check-in que acepta credenciales del wallet se construye sobre `eudi-srv-verifier-endpoint` y `eudi-lib-jvm-openid4vci-kt`, **ambos Apache-2.0**. ⚠️ **No forkear las apps de referencia: son EUPL-1.2.** Ver `repos/trending.md` → *Estratificación de licencia*. |

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
4. **Verificar identidad sin almacenarla.** Si el flujo necesita documento (check-in,
   cruce de frontera, verificación de edad), el orden es: leer el chip o la MRZ con
   `AndyQ/NFCPassportReader` (MIT) o `fastmrz` (Apache-2.0), **derivar el atributo que la
   regla exige y descartar el documento**. Para el caso en que ni siquiera el atributo deba
   salir del dispositivo, `zkpassport/circuits` (Apache-2.0) y `rarimo/passport-zk-circuits`
   (MIT) permiten probarlo sin revelarlo. En North America esto no es un lujo: es la región
   con la adopción biométrica más alta **y** la preocupación más alta por brechas de datos
   (IATA 2026), y las dos cosas son el mismo cliente.
5. **Human-in-the-loop obligatorio en el pago.** No es una preferencia de diseño: es lo que
   hacen hoy las aerolíneas (United mantiene la intervención humana en la compra) y lo que
   la evidencia de confianza del consumidor exige (ver `intel/trends.md`).

## Lo que cambió entre el 2026-11-21 y el 2026-11-23

Una sola cosa, y vale como advertencia de método para toda la KB: **Kamra PMS pasó de
AGPL-3.0 a Apache-2.0 en 48 horas**, con el archivo en la misma ruta y el mismo nombre
(`license.txt`). Un lector que confiara en la nota del ciclo anterior habría descartado la
mejor opción permisiva del vertical por una licencia que ya no estaba vigente.

**Por eso cada licencia de esta tabla lleva la fecha en que se leyó el archivo, y antes de
comprometer una licencia en una propuesta hay que volver a abrirlo.**

---
*Ver también: `repos/foundations.md` (ruteo, datos e identidad) y `compose/patterns.md`
(recetas concretas).*
