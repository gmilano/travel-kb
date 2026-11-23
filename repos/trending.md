---
industry: travel
region: Global
updated: 2026-11-23
---

# 📈 Repos trending — Travel & Hospitality

> **Archivo APPEND-ONLY.** Sección fechada nueva arriba, historia debajo.
> Este archivo sigue **repos de infraestructura y plataforma**. Para agentes y skills ver
> `agents/trending.md`. Hasta el 2026-11-21 ambos archivos eran copias idénticas; desde este
> ciclo tienen contenido distinto.

## 2026-11-23 — quinta pasada (plano terrestre: venta y distribución del tramo no aéreo)

| Repo | Licencia (archivo leído) | Stars | Push | Por qué entra |
|------|--------------------------|-------|------|---------------|
| [UnionInternationalCheminsdeFer/OSDM](https://github.com/UnionInternationalCheminsdeFer/OSDM) | **Apache-2.0** (11374B) | 95 | 2026-11-20 | El estándar de **venta** ferroviaria y multimodal (UIC IRS 90918-10), publicado como código. Reconocido por la TSI de telemática de la UE. **Y sin una sola implementación cliente open source.** |
| [entur/netex-gtfs-converter-java](https://github.com/entur/netex-gtfs-converter-java) | **EUPL-1.2** (13793B) | 13 | **2026-11-23** | Push hoy. NeTEx → GTFS, mantenido por el operador estatal noruego. Trae una familia de licencia nueva para esta KB. |
| [entur/kishar](https://github.com/entur/kishar) | EUPL-1.2 | 12 | **2026-11-23** | Push hoy. SIRI → GTFS-Realtime. |
| [OpendataCH/Transport](https://github.com/OpendataCH/Transport) | MIT (1060B) | 269 | 2026-11-22 | API de transporte suizo, viva esta semana. La referencia de API limpia del segmento. |
| [schildbach/public-transport-enabler](https://github.com/schildbach/public-transport-enabler) | **GPL-3.0** (32473B) | 456 | 2026-11-22 | El equivalente Java de `hafas-client`, con más redes. Muy vivo — y copyleft. |
| [transitland/transitland-atlas](https://github.com/transitland/transitland-atlas) | CC BY 4.0 (18657B) | 200 | 2026-11-22 | Directorio abierto de feeds y operadores. Licencia de **dato**, no de código. |
| [MobilityData/gtfs-validator](https://github.com/MobilityData/gtfs-validator) | Apache-2.0 (11327B) | 434 | 2026-11-19 | El validador canónico de GTFS. Higiene antes de que el agente lea. |
| [MobilityData/mobility-database-catalogs](https://github.com/MobilityData/mobility-database-catalogs) | Apache-2.0 (11357B) | 354 | 2026-11-19 | Dónde está el feed de cada operador del mundo. |
| [MobilityData/gbfs](https://github.com/MobilityData/gbfs) | **CC BY 3.0** (19467B) | 928 | 2026-11-18 | Micromovilidad compartida. La API de GitHub dice `NOASSERTION`; el archivo es Creative Commons. |
| [dbinfrago/openstation-docs](https://github.com/dbinfrago/openstation-docs) | Apache-2.0 (11344B) | 38 | 2026-11-16 | API OpenStation de DB InfraGO: datos de estaciones alemanas. |
| [public-transport/hafas-client](https://github.com/public-transport/hafas-client) | ISC (`license.md`, 727B) | 372 | 2026-08-23 | El cliente que habla con decenas de operadores europeos. **El repo más grande del plano.** Ver la advertencia de endpoint. |
| [public-transport/db-vendo-client](https://github.com/public-transport/db-vendo-client) | ISC (777B) | 209 | 2026-09-10 | Sucesor de `db-hafas` tras la migración de Deutsche Bahn. |

**Lo que está dormido y hay que decirlo:** `mainmatter/reStations` (Apache-2.0, 8★), **la única
implementación de una API OSDM que existe en el mundo**, no tiene push desde **2025-04-02** — y
además cubre solo la Places API (estaciones), no la venta. `public-transport/db-hafas` (81★)
quedó obsoleto por `db-vendo-client`. `TransitApp/gtfs-fares-v2-validator` (MIT, 7★) está
**archivado**: el único validador del modelo abierto de tarifas está formalmente muerto.

**Dos lecturas de licencia que no se ven desde la API de GitHub, ambas registradas hoy:**
`interline-io/transitland-lib` reporta `NOASSERTION` y es **GPL-3.0 con opción comercial de
pago**; el `LICENSE.txt` de OneBusAway son 547 bytes cuya primera línea es el token sin
expandir `COPYRIGHT_SECTION`. Detalle completo en `repos/foundations.md`.

**El titular del plano:** el estándar de venta es Apache-2.0, está en GitHub, tiene 95
estrellas — y `osdm client implementation` devuelve **0 repositorios**. La consulta
`fare engine open source` también devuelve **0**. Hay con qué **consultar** un tren en Europa
y no hay con qué **venderlo** en ninguna parte.

## 2026-11-23 — cuarta pasada (plano de visibilidad agentic)

| Repo | Licencia | Stars | Push | Por qué entra |
|------|----------|-------|------|---------------|
| [webmachinelearning/webmcp](https://github.com/webmachinelearning/webmcp) | W3C Software and Document License | 5012 | **2026-11-23** | WebMCP: el sitio le **declara funciones** al agente en vez de que el agente lea la pantalla. Push hoy; incubación W3C, **no es estándar**. |
| [schemaorg/schemaorg](https://github.com/schemaorg/schemaorg) | Apache-2.0 | 6316 | 2026-11-20 | El vocabulario que los motores sí consumen. Vivo. |
| [AnswerDotAI/llms-txt](https://github.com/AnswerDotAI/llms-txt) | Apache-2.0 | 2700 | 2026-09-24 | La propuesta `/llms.txt`. Entra **con la evidencia en contra pegada** (abajo). |
| [OvertureMaps/schema](https://github.com/OvertureMaps/schema) | CC-BY-4.0 | 219 | 2026-11-22 | Donde aterriza la alineación OpenTravel↔Overture (GERS IDs). Licencia **de contenido**: obliga a atribuir. |
| [AdamBenDev/hospitality-geo-standard](https://github.com/AdamBenDev/hospitality-geo-standard) | MIT | **0** | 2026-11-21 | Creado hace 7 días. Primer intento MIT de estandarizar GEO de hospitality. |

### El estándar más recomendado del año tiene la evidencia de uso en contra

`llms.txt` aparece en casi todas las guías de "hotel AI-friendly" de 2026. Lo medido *[fuentes
secundarias]*: adopción **9,3%** en top-1000 dominios (Rankability, sep-2026), y —el dato que
importa— **97% de los ~38.000 dominios con un `llms.txt` válido no recibieron ni una petición
del archivo en mayo de 2026** (Ahrefs), con 96% de las peticiones que sí hubo provenientes de
bots. **Ningún proveedor grande confirma usarlo para decidir citas.**

Se deja publicado como apuesta barata; **no se vende como palanca.** La palanca con evidencia
es el JSON-LD del tipo correcto.

### El generador de `llms.txt` más estrellado no tiene licencia y está quieto

`firecrawl/llmstxt-generator` — **540★, sin archivo de licencia** (`LICENSE`, `LICENSE.md` y
`LICENSE.txt` devuelven 404), **sin push desde 2025-06-17** (17 meses). Mismo caso en
`amplifying-ai/awesome-generative-engine-optimization` (542★, sin licencia). **No usar como
dependencia**: sin licencia no hay permiso de uso, por más público que sea el repo.

### El organismo de estándares del vertical, medido

`OpenTravel` —que se sumó a Overture Maps (Linux Foundation) en agosto de 2025 bajo el título
*"AI-ready travel infrastructure"*— tiene **12 repos en GitHub, máximo 22 estrellas, 8 sin
licencia declarada y ningún push desde enero de 2025**. El detalle repo por repo está en
`repos/foundations.md`. **La capa que la prensa llama infraestructura del vertical es, otra vez,
la que está quieta** — el mismo patrón que la tercera pasada encontró en el plano de pago, con
un agravante: acá además falta el permiso legal de uso.

## 2026-11-23 — tercera pasada (plano de pago agentic)

Tercer ciclo del mismo día; las dos secciones anteriores quedan intactas debajo. **El hallazgo
de esta pasada es una inversión de la regla que esta KB venía midiendo hace cuatro ciclos.**

En travel la regla era *plataforma copyleft, infraestructura permisiva*. El plano de pago
agentic **no tiene una sola pieza copyleft**: las cinco especificaciones con tracción son
Apache-2.0 o MIT. La causa es estructural —es una guerra de estándares entre consorcios, y ahí
la licencia restrictiva es una desventaja— y la consecuencia es que **en esta capa la pregunta
deja de ser legal y pasa a ser de apuesta de arquitectura**.

| Repo | Licencia (leída) | Stars | Último push |
|------|------------------|-------|-------------|
| [x402-foundation/x402](https://github.com/x402-foundation/x402) | Apache-2.0 (11324B) | 6822 | 2026-11-20 |
| [Universal-Commerce-Protocol/ucp](https://github.com/Universal-Commerce-Protocol/ucp) | Apache-2.0 (11358B) | 3517 | 2026-11-21 |
| [google-agentic-commerce/AP2](https://github.com/google-agentic-commerce/AP2) | Apache-2.0 (11359B) | 3283 | **2026-06-17** |
| [agentic-commerce-protocol/agentic-commerce-protocol](https://github.com/agentic-commerce-protocol/agentic-commerce-protocol) | Apache-2.0 (10947B) | 1609 | **2026-07-18** |
| [forter/trusted-agentic-commerce-protocol](https://github.com/forter/trusted-agentic-commerce-protocol) | MIT (1062B) | 180 | 2026-07-08 |

### La capa que la prensa llama central es la que está quieta

Las dos especificaciones de **autorización e interacción** (AP2, ACP) llevan cuatro y cinco
meses sin commit. Las dos de **rieles y comercio** (x402, UCP) empujaron esta semana. Es el
mismo tipo de hallazgo que la segunda pasada registró con las licencias de dato: **lo que se
cita no siempre es lo que se mantiene.** Detalle y cautelas en `intel/trends.md` → 18.

### Brecha travel medida en la misma pasada

`airline payment agent protocol`, `hotel booking payment mandate`, `AP2 mandate implementation`
y `travel refund chargeback agent`: **0 resultados cada una**. El plano de pago es horizontal y
sólido; **su aterrizaje en travel no existe en abierto** (`repos/foundations.md` → *Brechas del
plano de pago*).

## 2026-11-23 — segunda pasada (plano operativo de vuelo)

Segundo ciclo del mismo día; la sección de la mañana queda intacta debajo. **El hallazgo de
esta pasada no es un repo ni un cambio de licencia: es una licencia que no está en el repo.**

| Repo | Licencia (archivo leído) | Stars | Último push | Qué cambió |
|------|--------------------------|-------|-------------|------------|
| [wiedehopf/tar1090](https://github.com/wiedehopf/tar1090) | **GPL-2.0-or-later** (18339B) — GitHub dice `NOASSERTION` | 1979 | 2026-11-21 | Entra por primera vez. El repo más estrellado del plano de datos de vuelo. |
| [jpatokal/openflights](https://github.com/jpatokal/openflights) | AGPL-3.0 (34523B) | 1686 | 2026-11-22 | Entra por primera vez. El dataset de rutas y aerolíneas más citado del mundo, bajo copyleft de red. |
| [wiedehopf/readsb](https://github.com/wiedehopf/readsb) | **GPL-3.0-or-later** (2155B → `COPYING`) — GitHub dice `NOASSERTION` | 707 | 2026-11-11 | Entra por primera vez. El decodificador ADS-B de producción. |
| [junzis/pyModeS](https://github.com/junzis/pyModeS) | GPL-3.0 (35140B) | 674 | 2026-11-11 | Entra por primera vez. El puente hacia un stack de datos de vuelo en Python. |
| [sdr-enthusiasts/docker-adsb-ultrafeeder](https://github.com/sdr-enthusiasts/docker-adsb-ultrafeeder) | GPL-3.0 (35149B) | 608 | 2026-11-22 | Entra por primera vez. Contenedor todo-en-uno para levantar un receptor propio. |
| [openskynetwork/opensky-api](https://github.com/openskynetwork/opensky-api) | GPL-3.0 (35147B) **+ términos de dato no comerciales** | 476 | 2026-11-05 | Entra por primera vez, **y es el caso que da nombre a esta pasada**. Ver abajo. |
| [dirkhh/adsb-feeder-image](https://github.com/dirkhh/adsb-feeder-image) | GPL-3.0 (35149B) | 407 | 2026-11-22 | Entra por primera vez. Imagen de sistema lista para alimentar redes ADS-B. |
| [rsadsb/adsb_deku](https://github.com/rsadsb/adsb_deku) | MIT (1071B) | 732 | 2026-01-04 | Entra por primera vez. El decodificador permisivo más estrellado — y **~10 meses sin push**. |

### La licencia que no está en el repo

Todo el método de verificación que esta KB construyó en noviembre —no confiar en el badge de
GitHub, abrir el archivo de licencia, anotar su tamaño y la fecha en que se leyó— **da el
resultado correcto y aun así insuficiente** en este plano.

`openskynetwork/opensky-api` es GPL-3.0: el archivo está donde debe, dice lo que dice, y
cumplirlo es cuestión de correr el binding como proceso separado. Pero **OpenSky Network es
una asociación suiza sin fines de lucro**, y sus **términos de dato** —según las fuentes
secundarias consultadas— conceden el uso para investigación y educación sin fines de lucro,
evaluación interna no comercial y fines gubernamentales, **sin licenciar el uso comercial**.
El archivo de licencia del repositorio **no dice nada de eso**, porque no es su trabajo
decirlo.

**Regla nueva para esta KB, que vale para todas las industrias de la red:** cuando un repo es
un **cliente de un servicio de datos** —y no una librería autocontenida— hay **dos**
documentos que leer, y el segundo no vive en GitHub. Los repos de esta tabla que son
decodificadores (`readsb`, `pyModeS`, `adsb_deku`, `tar1090`) operan sobre señal que uno mismo
recibe: ahí la licencia del código es toda la historia. Los que son **clientes de red**
(`opensky-api`, y `FlightRadarAPI` en `agents/top.md`) traen una segunda condición que el
badge de GitHub, el archivo de licencia y esta KB **no pueden verificar solos**.

⚠️ **Límite declarado:** `opensky-network.org` y `zenodo.org` no resuelven DNS desde el
entorno de ingesta, igual que los dominios de la UE registrados en la pasada de la mañana. Lo
anterior está corroborado por fuentes secundarias concordantes pero **no leído en la fuente
oficial**, y así debe presentarse a cualquier cliente hasta que se verifique desde una red sin
esta restricción.

## 2026-11-23

**El hallazgo del ciclo es un cambio de licencia, no un repo nuevo.**

| Repo | Licencia | Stars | Último push | Qué cambió |
|------|----------|-------|-------------|------------|
| [Kamra-PMS/kamra-pms](https://github.com/Kamra-PMS/kamra-pms) | **Apache-2.0** (era AGPL-3.0) | 113 | 2026-11-23 | **Relicenciado de AGPL-3.0 a Apache-2.0.** Commit `ce8dec8`, *"chore: relicense Kamra core to Apache-2.0 (#591) (#631)"*, fechado **2026-11-21** — el mismo día en que el ciclo anterior leyó el archivo y encontró AGPL-3.0. Verificado hoy clonando el repo y siguiendo el historial de `license.txt` (11358B, texto Apache completo, en `main` y en `master`). Convierte al único PMS diseñado para ser operado por agentes en **el PMS permisivo más grande del vertical**. |
| [eu-digital-identity-wallet](https://github.com/eu-digital-identity-wallet) (org) | **tres licencias distintas, a propósito** | 780 / 309 / 243 / 66 / 64 / 47 / 43 | 2026-11-17 … 2026-11-23 | Entra a la KB por primera vez. Ver *Estratificación de licencia* abajo: la especificación, las apps de referencia y las librerías **no comparten licencia**, y la diferencia decide la arquitectura. |
| [sivakumar-mahalingam/fastmrz](https://github.com/sivakumar-mahalingam/fastmrz) | Apache-2.0 | 174 | 2026-11-23 | Push hoy. Infraestructura de lectura de documento bajo licencia permisiva. |
| [liketrek/TREK](https://github.com/liketrek/TREK) | AGPL-3.0 | 15881 | 2026-11-22 | +39★ en dos días. Sigue siendo el repo de travel más grande y sigue siendo copyleft de red. |
| [Qloapps/QloApps](https://github.com/Qloapps/QloApps) | OSL-3.0 / AFL-3.0 | 14509 | 2026-11-20 | +9★. Estable. |
| [headwaymaps/headway](https://github.com/headwaymaps/headway) | Apache-2.0 | 3022 | 2026-11-22 | Sin cambio de estrellas en dos días, push activo. |
| [motis-project/motis](https://github.com/motis-project/motis) | MIT | 630 | 2026-11-21 | +2★. |

### Estratificación de licencia del EU Digital Identity Wallet

Leídos los archivos de licencia el 2026-11-23, la organización oficial de la Comisión Europea
usa **tres licencias según la capa**, y esto no es desprolijidad, es diseño:

| Capa | Repos | Licencia (archivo leído) | Qué implica para un engagement |
|------|-------|--------------------------|-------------------------------|
| Especificación (ARF) | [`eudi-doc-architecture-and-reference-framework`](https://github.com/eu-digital-identity-wallet/eudi-doc-architecture-and-reference-framework) (780★) | **CC BY 4.0** (`LICENCE`, 249B) | Documentación con atribución. **Se puede citar, derivar y usar comercialmente.** GitHub la reporta como `NOASSERTION`. |
| Apps de referencia | [`eudi-app-android-wallet-ui`](https://github.com/eu-digital-identity-wallet/eudi-app-android-wallet-ui) (243★), [`eudi-app-ios-wallet-ui`](https://github.com/eu-digital-identity-wallet/eudi-app-ios-wallet-ui) (93★), [`av-app-android-wallet-ui`](https://github.com/eu-digital-identity-wallet/av-app-android-wallet-ui) (309★) | **EUPL-1.2** (`LICENSE.txt`, 13961B) | Copyleft europeo con cláusula de compatibilidad. **Forkear la app arrastra la obligación al producto del cliente.** |
| Librerías y servicios | [`eudi-lib-android-wallet-core`](https://github.com/eu-digital-identity-wallet/eudi-lib-android-wallet-core) (64★), [`eudi-srv-pid-issuer`](https://github.com/eu-digital-identity-wallet/eudi-srv-pid-issuer) (43★), [`eudi-srv-verifier-endpoint`](https://github.com/eu-digital-identity-wallet/eudi-srv-verifier-endpoint) (66★), [`eudi-lib-jvm-openid4vci-kt`](https://github.com/eu-digital-identity-wallet/eudi-lib-jvm-openid4vci-kt) (47★), [`eudi-lib-ios-wallet-kit`](https://github.com/eu-digital-identity-wallet/eudi-lib-ios-wallet-kit) (43★) | **Apache-2.0** (`LICENSE`, 9425–11357B) | Permisivas. **Acá se construye.** |

**Regla operativa, en una línea: integrar contra las librerías y servicios Apache-2.0; tratar
las apps EUPL-1.2 como referencia de UX para leer, no como base para forkear.**

Esto **invierte** el hallazgo que la KB de retail registró el mismo mes sobre beckn/ONDC, donde
la especificación era la pieza restrictiva (CC BY-NC-SA, *NonCommercial*) y las
implementaciones eran permisivas. Acá la especificación es la pieza **más** libre de las tres.
La lección generaliza a las 12 industrias y ya se cumplió en las dos direcciones:
**la licencia de una especificación y la de su implementación son variables independientes —
hay que leer las dos, y no se puede predecir una desde la otra.**

**Nota de método, la más cara de este ciclo.** El ciclo anterior leyó el archivo de licencia de
Kamra correctamente, y **48 horas después el dato era falso**. No fue un error de medición: fue
una medición con fecha de vencimiento. De acá en más, **toda licencia citada en esta KB lleva
la fecha en que se leyó el archivo**, y una licencia verificada hace más de una semana se
vuelve a verificar antes de comprometerla en una propuesta. Un repo puede relicenciarse entre
el kickoff y la firma.

---

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
