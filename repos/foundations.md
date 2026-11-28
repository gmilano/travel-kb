---
industry: travel
region: Global
updated: 2026-11-28
---

# 🏗️ Repos fundacionales — Travel & Hospitality

> Bases sobre las cuales construir: ruteo, geocoding, datos de transporte, acceso a GDS e
> **identidad del viajero**. La capa fundacional de travel **no es AI** — es routing, datos
> geoespaciales y documento. Los agentes se montan arriba.
> Filas verificadas el 2026-11-21; identidad, vuelo, pago, visibilidad y **plano terrestre**, el 2026-11-23.

## Ruteo y planificación multimodal

| Repo | Licencia | Stars | Último push | Por qué importa | ¿Base para AI? |
|------|----------|-------|-------------|-----------------|----------------|
| [graphhopper/graphhopper](https://github.com/graphhopper/graphhopper) | Apache-2.0 | 6827 | 2026-11-20 | Motor de ruteo sobre OpenStreetMap, como librería Java o servidor standalone. La licencia más permisiva del segmento. | Sí — tool de ruteo para un agente, sin restricción copyleft |
| [valhalla/valhalla](https://github.com/valhalla/valhalla) | **MIT** | 6475 | 2026-11-20 | Motor de ruteo OSM con matriz de tiempos, isócronas y map-matching. GitHub reporta `NOASSERTION` porque `LICENSE.md` es un puntero de 45 bytes a `COPYING`; **`COPYING` es MIT literal**. | Sí — isócronas y matrices son exactamente lo que un agente de itinerario necesita |
| [opentripplanner/OpenTripPlanner](https://github.com/opentripplanner/OpenTripPlanner) | LGPL-3.0 | 2780 | 2026-11-20 | El planificador multimodal de referencia (GTFS + OSM). Usado por operadores de transporte público reales. | Sí, con cuidado — LGPL permite enlazar desde software propietario, no derivar |
| [motis-project/motis](https://github.com/motis-project/motis) | MIT | 628 | 2026-11-20 | Ruteo multimodal + geocoding + map tiles en un solo binario. La alternativa MIT a OTP. | Sí — el stack completo bajo una licencia permisiva |
| [opentripplanner/otp-react-redux](https://github.com/opentripplanner/otp-react-redux) | MIT | 95 | 2026-11-20 | Front-end de referencia para cualquier backend compatible con OTP. | Sí — UI base donde insertar la capa conversacional |

## Geocoding y mapas self-hosted

| Repo | Licencia | Stars | Último push | Por qué importa | ¿Base para AI? |
|------|----------|-------|-------------|-----------------|----------------|
| [osm-search/Nominatim](https://github.com/osm-search/Nominatim) | GPL-3.0 | 4573 | 2026-11-18 | El geocoder OSM canónico. **GPL-3.0**: se corre como servicio separado, no se embebe. | Como servicio sí; embebido no |
| [komoot/photon](https://github.com/komoot/photon) | Apache-2.0 | 3203 | 2026-11-20 | Geocoder OSM con búsqueda tolerante a tipeo y autocompletado. **La opción permisiva frente a Nominatim.** | Sí — resolución de lugares desde texto libre del usuario |
| [headwaymaps/headway](https://github.com/headwaymaps/headway) | Apache-2.0 | 3022 | 2026-11-21 | Stack de mapas self-hosted completo (tiles + geocoding + ruteo) en contenedores. | Sí — elimina la dependencia de la API de Google en despliegues con datos sensibles |

## Datos de transporte (GTFS)

| Repo | Licencia | Stars | Último push | Por qué importa | ¿Base para AI? |
|------|----------|-------|-------------|-----------------|----------------|
| [BlinkTagInc/node-gtfs](https://github.com/BlinkTagInc/node-gtfs) | MIT | 506 | 2026-11-17 | Importa, valida, consulta y exporta GTFS Schedule y Realtime a SQLite/PostgreSQL. | Sí — convierte horarios en una base consultable por un agente |
| [MobilityData/gtfs-realtime-bindings](https://github.com/MobilityData/gtfs-realtime-bindings) | Apache-2.0 | 446 | 2026-11-16 | Bindings generados del protobuf de GTFS Realtime para los lenguajes principales. Mantenido por MobilityData. | Sí — ingesta de llegadas y alertas en vivo |
| [ibi-group/datatools-ui](https://github.com/ibi-group/datatools-ui) | MIT | 147 | 2026-11-19 | Suite de edición y validación de feeds GTFS de nivel operador. | Indirecta — higiene de datos antes de que el agente los lea |

## Acceso a GDS / distribución aérea

| Repo | Licencia | Stars | Último push | Por qué importa | ¿Base para AI? |
|------|----------|-------|-------------|-----------------|----------------|
| [punitarani/fli](https://github.com/punitarani/fli) | MIT | 3510 | 2026-11-11 | Google Flights como MCP + CLI + librería. Es el camino de menor fricción a inventario aéreo sin contrato de GDS. | Sí — ya es un MCP server |
| [amadeus4dev/amadeus-python](https://github.com/amadeus4dev/amadeus-python) | MIT | 262 | 2025-03-11 | SDK oficial de las Amadeus Self-Service APIs. **ARCHIVADO** (`archived: true`). | Solo como referencia de esquema — no es dependencia viva |

## Identidad del viajero y cruce de frontera

Agregada el 2026-11-23. Es la **única capa fundacional de travel cuyo piso open source es
permisivo, vivo y con más de un proveedor por problema** — al revés que distribución aérea,
donde no hay nada. Licencias leídas del archivo, no del badge.

| Repo | Licencia | Stars | Último push | Por qué importa | ¿Base para AI? |
|------|----------|-------|-------------|-----------------|----------------|
| [AndyQ/NFCPassportReader](https://github.com/AndyQ/NFCPassportReader) | MIT (1065B) | 867 | 2026-11-16 | Lectura del chip ICAO 9303 en iOS: BAC, secure messaging, autenticación pasiva. Es el eslabón que convierte un pasaporte físico en datos tipados. | Sí — da al agente un documento verificado en vez de texto tipeado por el huésped |
| [konstantint/PassportEye](https://github.com/konstantint/PassportEye) | MIT (1064B) | 471 | 2026-11-22 | MRZ desde imagen, en Python. Funciona donde no hay NFC (visas, documentos viejos, escaneos). | Sí — preprocesamiento antes de que el modelo vea nada |
| [sivakumar-mahalingam/fastmrz](https://github.com/sivakumar-mahalingam/fastmrz) | Apache-2.0 (11356B) | 174 | 2026-11-23 | Lo mismo que PassportEye, bajo Apache-2.0, optimizado para latencia. | Sí — la opción Apache cuando el cliente exige esa familia de licencia |
| [eu-digital-identity-wallet/eudi-srv-verifier-endpoint](https://github.com/eu-digital-identity-wallet/eudi-srv-verifier-endpoint) | Apache-2.0 (9425B+) | 66 | 2026-11-17 | Servicio verificador (Relying Party) de credenciales del EU Digital Identity Wallet. Mantenido por la Comisión Europea. | Sí — es el lado que consume la credencial; lo que un hotel o aerolínea necesita operar |
| [eu-digital-identity-wallet/eudi-lib-jvm-openid4vci-kt](https://github.com/eu-digital-identity-wallet/eudi-lib-jvm-openid4vci-kt) | Apache-2.0 | 47 | 2026-11-17 | Implementación de OpenID4VCI (emisión de credenciales verificables) en JVM. | Sí — el protocolo, no el producto: sobrevive a cambios de wallet |
| [zkpassport/circuits](https://github.com/zkpassport/circuits) | Apache-2.0 (11340B) | 94 | 2026-11-18 | Probar un atributo del pasaporte sin revelar el pasaporte. | Sí — permite cumplir una regla sin crear un pasivo de datos |
| [rarimo/passport-zk-circuits](https://github.com/rarimo/passport-zk-circuits) | MIT (1085B) | 94 | 2026-11-05 | Misma capacidad, bajo MIT. Dos implementaciones independientes. | Sí |
| [imorte/passport-index-data](https://github.com/imorte/passport-index-data) | MIT (1056B) | 88 | 2026-03-01 | Matriz de requisitos de visado 199×199 en CSV y JSON, con una taxonomía bien pensada (`eta` / `e-visa` / `visa on arrival` / `visa free` / `visa required` / `no admission`). | **Como esquema sí; como dato, no** — ver abajo |

### La advertencia que acompaña al único dataset de visados

[`imorte/passport-index-data`](https://github.com/imorte/passport-index-data) se describe como
*"updated regularly"* y su README declara **"Last updated: 17 February 2026"**; el último push
al repo es del **2026-03-01**. Son **nueve meses** sin actualizar un dato que cambió varias
veces en 2026. Es la continuación de
[`ilyankou/passport-index-dataset`](https://github.com/ilyankou/passport-index-dataset)
(MIT, 310★), **archivado explícitamente desde enero de 2025**, que apunta a él como sucesor.

Es decir: **la única fuente abierta de requisitos de visado del mundo es una cadena de dos
repos, el primero archivado y el segundo desactualizado nueve meses.** Usar su *taxonomía*
como esquema es una buena decisión de diseño; usar sus *valores* para decirle a un viajero si
puede volar es un riesgo legal. El dato vigente vive en Timatic (IATA) y en los portales
consulares, ambos de acceso contractual o manual.

## Datos operativos de vuelo, aeronave y aeropuerto

Agregada en la **segunda pasada del 2026-11-23**. Es el plano que esta KB venía invocando en
cada receta de disrupción ("el agente detecta el retraso y reacomoda") **sin una sola fila que
dijera de dónde sale el retraso**. Existe, es grande y está vivo — pero su reparto de
licencias es **exactamente el inverso** del plano de frontera, y por eso la tabla va partida
en dos. Las 15 filas de esta sección fueron verificadas el 2026-11-23: existencia por
`git ls-remote` (15/15 vivas), estrellas y `pushed_at` por `search/repositories`, y licencia
**leyendo el archivo**.

### Capa permisiva — se puede embeber en producto de cliente

| Repo | Licencia (archivo leído) | Stars | Último push | Por qué importa | ¿Base para AI? |
|------|--------------------------|-------|-------------|-----------------|----------------|
| [xoolive/traffic](https://github.com/xoolive/traffic) | **MIT** (`license.md` minúscula, 1069B) | 525 | 2026-11-11 | La caja de herramientas de referencia para procesar y analizar tráfico aéreo: trayectorias, limpieza, remuestreo, detección de fases de vuelo. GitHub lo reporta MIT y **el archivo lo confirma**, pero está en `license.md` en minúscula sobre `master` — la misma trampa de ruta que Kamra PMS. | **Sí, y es la pieza central** — convierte posiciones crudas en trayectorias tipadas que un agente puede razonar |
| [davidmegginson/ourairports-data](https://github.com/davidmegginson/ourairports-data) | **Unlicense — dominio público** (1211B) | 534 | 2026-11-23 | Aeropuertos, pistas, frecuencias y países del mundo en CSV. **Push el mismo día de este ciclo.** Sin atribución obligatoria, sin condiciones. | Sí — la tabla de referencia que toda receta de vuelo necesita, con el costo de licencia más bajo posible: cero |
| [mborsetti/airportsdata](https://github.com/mborsetti/airportsdata) | **MIT** (1191B) | 172 | 2026-11-21 | Base de aeropuertos con **husos horarios por aeropuerto**. GitHub lo marca `NOASSERTION`; el archivo es MIT literal. | Sí — sin huso horario no se puede computar "3 horas de retraso", que es el umbral regulatorio de North America |
| [rsadsb/adsb_deku](https://github.com/rsadsb/adsb_deku) | **MIT** (1071B) | 732 | 2026-01-04 | Decodificador ADS-B en Rust. El decodificador permisivo más estrellado del plano. | Con reserva — **~10 meses sin push**. Licencia impecable, mantenimiento dudoso |
| [JeanExtreme002/FlightRadarAPI](https://github.com/JeanExtreme002/FlightRadarAPI) | **MIT** (1089B) | 442 | 2026-11-20 | SDK **no oficial** de FlightRadar24 para Python, NodeJS y Go. Vivo y mantenido. | **El código sí, el acceso no** — ver advertencia abajo |
| [google/travel-impact-model](https://github.com/google/travel-impact-model) | **CC-BY-4.0** (18658B) | 195 | 2026-11-04 | El modelo de estimación de emisiones de vuelo que Google usa en Flights. Es la referencia pública de facto para el CO₂e de un itinerario. | Sí, con la salvedad de que **CC-BY-4.0 es licencia de contenido, no de software** — ver abajo |
| [CPLX/flighty-mcp-server](https://github.com/CPLX/flighty-mcp-server) | **MIT** (1079B) | 35 | 2026-08-31 | MCP server sobre la app de seguimiento de vuelos Flighty, 12 tools. **El único MCP de estado de vuelo encontrado con más de 10★.** | Sí — pero 35★ y sin push desde agosto: referencia de esquema, no dependencia |

### Capa copyleft — se corre como servicio, no se embebe

Aquí está el músculo del plano. Ninguno es inutilizable: **GPL no prohíbe usarlo, prohíbe
embeberlo en un binario propietario.** Corridos como proceso o contenedor separado detrás de
una API, los siete son perfectamente utilizables en un engagement.

| Repo | Licencia (archivo leído) | Stars | Último push | Por qué importa |
|------|--------------------------|-------|-------------|-----------------|
| [wiedehopf/tar1090](https://github.com/wiedehopf/tar1090) | **GPL-2.0-or-later** (18339B) | 1979 | 2026-11-21 | La interfaz web de referencia para decodificadores ADS-B. El repo más estrellado del plano. GitHub lo reporta `NOASSERTION`. |
| [jpatokal/openflights](https://github.com/jpatokal/openflights) | **AGPL-3.0** (34523B) | 1686 | 2026-11-22 | Plataforma de registro de vuelos y el dataset de rutas y aerolíneas más citado del mundo. **AGPL = copyleft de red.** |
| [wiedehopf/readsb](https://github.com/wiedehopf/readsb) | **GPL-3.0-or-later** (2155B, remite a `COPYING`) | 707 | 2026-11-11 | El decodificador ADS-B de producción. GitHub lo reporta `NOASSERTION`; el archivo dice GPL v3 o posterior. |
| [junzis/pyModeS](https://github.com/junzis/pyModeS) | **GPL-3.0** (35140B) | 674 | 2026-11-11 | Decodificador de Mode S y ADS-B en Python. El puente natural hacia un stack de datos en Python. |
| [sdr-enthusiasts/docker-adsb-ultrafeeder](https://github.com/sdr-enthusiasts/docker-adsb-ultrafeeder) | **GPL-3.0** (35149B) | 608 | 2026-11-22 | Contenedor todo-en-uno (readsb + tar1090 + graphs1090). La vía más rápida a un receptor propio funcionando. |
| [openskynetwork/opensky-api](https://github.com/openskynetwork/opensky-api) | **GPL-3.0** (35147B) | 476 | 2026-11-05 | Bindings Python y Java de la API REST de OpenSky Network. **El problema no es esta licencia — ver abajo.** |
| [dirkhh/adsb-feeder-image](https://github.com/dirkhh/adsb-feeder-image) | **GPL-3.0** (35149B) | 407 | 2026-11-22 | Imagen de sistema lista para alimentar redes ADS-B desde un receptor propio. |

### ⚠️ La licencia del dato no es la licencia del código

Es la advertencia más importante de esta sección y la que más fácil se pasa por alto, porque
la herramienta de siempre —mirar el SPDX del repo— **no la detecta**.

[`openskynetwork/opensky-api`](https://github.com/openskynetwork/opensky-api) es **GPL-3.0**,
y eso es manejable: se corre separado. Pero **OpenSky Network es una asociación sin fines de
lucro suiza**, y las fuentes consultadas coinciden en que su licencia **de datos** concede el
uso para **investigación sin fines de lucro, educación sin fines de lucro, evaluación interna
no comercial y fines gubernamentales** — y que **lo que cae fuera de esos propósitos no está
licenciado**. El acceso directo a su base histórica (Impala) está además reservado a
investigación.

Dicho sin rodeos: **se puede cumplir la GPL impecablemente y seguir sin tener derecho a usar
el dato en un producto de cliente.** El código es libre; el dato no.

⚠️ **Límite de verificación declarado.** `opensky-network.org` **no resuelve DNS desde el
entorno de ingesta de esta KB**, igual que los dominios de la UE registrados en el ciclo
anterior. Lo de arriba proviene de fuentes secundarias concordantes (el texto de su
`LICENSE.txt` depositado en Zenodo y literatura académica que lo cita), **no de los términos
oficiales leídos en el sitio**. Zenodo tampoco resultó alcanzable. **Antes de usar OpenSky en
cualquier engagement comercial hay que abrir `opensky-network.org/about/terms-of-use` desde
una red sin esta restricción.** Mientras tanto, la postura segura es: OpenSky para prototipo
interno y evaluación, **no** para producción facturable.

La misma distinción, en dos casos más de esta sección:

- [`google/travel-impact-model`](https://github.com/google/travel-impact-model) es
  **CC-BY-4.0**, una licencia de **contenido**. Permite uso comercial con atribución, lo cual
  es excelente, pero Creative Commons **desaconseja expresamente usar sus licencias para
  software**. Para el modelo y sus tablas es el encaje correcto; si se copia código de ahí a
  un producto, hay que resolverlo con legales, no asumirlo.
- [`JeanExtreme002/FlightRadarAPI`](https://github.com/JeanExtreme002/FlightRadarAPI) es
  **MIT de verdad** — y es un cliente **no oficial** de FlightRadar24. La licencia cubre el
  código del SDK; **no otorga ningún derecho sobre el dato de FR24 ni sobre sus términos de
  servicio.** Es el mismo patrón ya registrado en `agents/top.md` para los conectores de
  LetsFG: **riesgo de ToS, no de licencia.** Para un piloto interno sirve; en un entregable a
  cliente, se cambia por un contrato de datos.

**La regla que conviene llevarse:** en el plano de frontera alcanzaba con abrir el archivo de
licencia. En el plano de datos de vuelo hay que abrir **dos** documentos: la licencia del
código **y** los términos del dato. Esta KB solo puede garantizar hoy la primera.

## Plano de pago agentic

Agregado en la **tercera pasada del 2026-11-23**. Es la capa de **especificación** que hay
debajo de las herramientas listadas en `agents/top.md` → *Pago agentic*. Todas las licencias
fueron leídas del archivo; todos los slugs verificados vivos por `git ls-remote`.

**El hallazgo del plano, dicho primero:** en travel la regla medida durante cuatro ciclos fue
*plataforma copyleft, infraestructura permisiva* (`intel/trends.md` → 8). **El plano de pago
rompe esa regla: es Apache-2.0 de punta a punta.** No por generosidad, sino porque es una
**guerra de estándares entre consorcios** — Google, OpenAI+Stripe, la Linux Foundation y
Shopify necesitan adopción, y una licencia restrictiva la impediría. La consecuencia práctica
para Globant es directa: **en esta capa la pregunta deja de ser "¿podemos usarlo?" y pasa a ser
"¿cuál va a sobrevivir?"**.

| Repo | Licencia (archivo leído) | Stars | Último push | Qué es |
|------|--------------------------|-------|-------------|--------|
| [x402-foundation/x402](https://github.com/x402-foundation/x402) | Apache-2.0 (11324B) | 6822 | 2026-11-20 | Protocolo de pago sobre HTTP: revive el código de estado **402 Payment Required**. Es la capa que **mueve el dinero**. El más estrellado y el más activo del plano. |
| [Universal-Commerce-Protocol/ucp](https://github.com/Universal-Commerce-Protocol/ucp) | Apache-2.0 (11358B) | 3517 | 2026-11-21 | Especificación de UCP. Relevante para travel por una razón concreta: su diseño declarado **deja al comercio como merchant of record**, que es exactamente la restricción que las aerolíneas imponen. |
| [google-agentic-commerce/AP2](https://github.com/google-agentic-commerce/AP2) | Apache-2.0 (11359B) | 3283 | **2026-06-17** | Agent Payments Protocol: capa de **autorización** — probar que el usuario autorizó la compra, vía *mandatos* firmados. Conceptualmente es la pieza central del corte en el pago. **Repo estancado hace ~5 meses — ver advertencia en `agents/top.md`.** |
| [agentic-commerce-protocol/agentic-commerce-protocol](https://github.com/agentic-commerce-protocol/agentic-commerce-protocol) | Apache-2.0 (10947B) | 1609 | **2026-07-18** | ACP: modelo de interacción comprador ↔ agente ↔ comercio. **Mantenido por OpenAI y Stripe**, lo que le da la distribución que a AP2 le sobra en prensa y le falta en commits. También ~4 meses sin push. |
| [forter/trusted-agentic-commerce-protocol](https://github.com/forter/trusted-agentic-commerce-protocol) | MIT (1062B) | 180 | 2026-07-08 | Autenticación y cifrado de datos entre agente, comercio y proveedores del comercio. **La única pieza MIT de la capa de especificación** y la que se ocupa del problema que a travel más le importa: *¿este agente es quien dice ser?* |

**La asimetría que conviene mirar antes de elegir.** Las dos especificaciones que la prensa
cita como centrales —**AP2 y ACP**— llevan **cuatro y cinco meses sin un commit**. Las dos que
están moviéndose esta misma semana —**x402 y UCP**— son las de **rieles y comercio**, no las de
autorización. Dicho de una vez: **la especificación se congeló; los rieles se mueven.** Para un
engagement eso significa no comprometer una arquitectura "AP2-native" sin antes confirmar el
upstream, y tratar la capa de autorización como **diseño propio informado por AP2**, que es
además donde Globant puede poner IP.

### Brechas del plano de pago, medidas el 2026-11-23

Mismo método: `search/repositories`, consultas nuevas. **El contraste es, por tercera vez, el
hallazgo:** el mecanismo horizontal es robusto y permisivo; su aterrizaje en travel no existe.

| Consulta | Resultados | Lectura |
|----------|-----------|---------|
| `airline payment agent protocol stars:>=5` | **0** | Ninguna aerolínea publicó integración agentic de pago. Coherente con la postura medida: las aerolíneas **ceden el agente, no el cobro**. |
| `hotel booking payment mandate stars:>=5` | **0** | Cero implementaciones del concepto de *mandato* (la primitiva central de AP2) aplicadas a hotelería. |
| `AP2 mandate implementation stars:>=20` | **0** | **El protocolo más citado del plano no tiene una sola implementación con tracción.** Los repos que lo nombran están entre 0★ y 2★. |
| `travel refund chargeback agent stars:>=5` | **0** | Nada sobre contracargo o reembolso agentic — el riesgo que un cliente de travel pregunta primero. |
| `travel agentic payment stars:>=5` | 3, **0 utilizables** | `Prism-Shadow/travel-agent` (Apache-2.0, 52★) ya está en `agents/top.md` y **su gracia es justamente detenerse antes de pagar**; `EntNaol/Online-transportation-booking` (10★, sin licencia, muerto desde 2022-08-04); `EGABO-TECH/ExFlo` (6★, **sin licencia**, pagos con MiniPay para mercados emergentes — la idea correcta, sin permiso de uso). |

**La forma de esta brecha:** el open source de pago agentic **sabe cómo cobrar en general, y
nada sobre cobrar un viaje en particular.** Las reglas que hacen distinto al pago de travel
—ticketing con plazo, cobro fraccionado entre aerolínea y OTA, contracargo a 180 días,
reembolso regulado (US DOT, EU261)— **no están en ninguno de estos protocolos**, y es el
mismo lugar donde esta KB ya ubicó la IP defendible del vertical.

## Plano de visibilidad agentic — el vocabulario que el agente lee

Fundacional en el sentido estricto: no son productos de travel, son **el vocabulario y las
herramientas con las que se describe la oferta para que una máquina la entienda**. Todo
verificado el 2026-11-23 leyendo el archivo de licencia, no el badge.

| Repo | Licencia (leída) | Stars | Último push | Para qué sirve en travel |
|------|------------------|-------|-------------|--------------------------|
| [schemaorg/schemaorg](https://github.com/schemaorg/schemaorg) | Apache-2.0 | 6316 | 2026-11-20 | El vocabulario mismo. `Hotel`, `LodgingBusiness`, `VacationRental`, `Trip`, `TouristAttraction` viven acá. Vivo y con push esta semana. |
| [google/schema-dts](https://github.com/google/schema-dts) | Apache-2.0 | 1262 | 2026-11-01 | Tipos TypeScript de Schema.org en JSON-LD. **Convierte "emitir el tipo correcto" en un error de compilación** en vez de un hallazgo de auditoría. |
| [scrapinghub/extruct](https://github.com/scrapinghub/extruct) | BSD-3-Clause | 985 | 2026-10-15 | Extrae metadata embebida (JSON-LD, microdata, RDFa, Open Graph) de HTML. **La pieza con la que se audita la cobertura propia y la del competidor.** |
| [digitalbazaar/jsonld.js](https://github.com/digitalbazaar/jsonld.js) | BSD (leída del archivo) | 1819 | 2026-03-04 | Procesador JSON-LD en JavaScript: expand, compact, normalizar. Necesario para comparar dos documentos sin que gane el que ordenó distinto las claves. |
| [api-platform/schema-generator](https://github.com/api-platform/schema-generator) | MIT (leída del archivo) | 475 | 2026-06-29 | Genera modelos PHP desde Schema.org y otros vocabularios RDF. Relevante porque **los PMS open source del vertical son PHP** (QloApps, HotelDruid). |
| [AnswerDotAI/llms-txt](https://github.com/AnswerDotAI/llms-txt) | Apache-2.0 | 2700 | 2026-09-24 | La propuesta `/llms.txt`. Se incluye **con la advertencia de abajo**, que es la parte importante. |
| [OvertureMaps/schema](https://github.com/OvertureMaps/schema) | **CC-BY-4.0** | 219 | 2026-11-22 | Esquema de Overture Maps (Linux Foundation). Importa a travel porque **OpenTravel se sumó a Overture** para alinear sus esquemas de localización con los GERS IDs. |
| [webmachinelearning/webmcp](https://github.com/webmachinelearning/webmcp) | **W3C Software and Document License** | 5012 | **2026-11-23** | WebMCP: que un sitio le declare sus funciones al agente en vez de que el agente lea la pantalla. Incubación W3C, push **hoy**. |

Ocho filas, ocho repos verificados. Dos advertencias que no se pueden deducir del badge:

### `jsonld.js` y la licencia que la API no sabe leer

La API de GitHub reporta `NOASSERTION` para `digitalbazaar/jsonld.js`. El archivo `LICENSE`
dice, en su primera línea, *"You may use the jsonld.js project under the terms of the BSD
License"*. **No es ambigüedad: es BSD, y el clasificador automático no lo reconoce.** Lo mismo
al revés en `api-platform/schema-generator`, cuyo `LICENSE` es el texto MIT **sin el encabezado
"MIT License"**, por lo que un grep ingenuo lo reporta como sin licencia. Es la regla de esta
KB otra vez: *la licencia se lee en el archivo.*

### `OvertureMaps/schema` y `webmcp` no son Apache ni MIT, y eso cambia el trabajo

- **CC-BY-4.0** (Overture) es una licencia de **contenido**, no de software: obliga a
  **atribuir**. Embeber el esquema en un entregable de cliente exige crédito explícito.
- La **W3C Software and Document License** permite uso y modificación, pero es una licencia de
  **documento de especificación en incubación**. WebMCP no es un estándar: es un borrador con
  5012 estrellas. **No comprometerlo en un roadmap de cliente como si fuera API estable.**

### ⚠️ `llms.txt`: el estándar que se recomienda en todas las guías y que no lee casi nadie

Es el hallazgo más accionable del plano, y va contra lo que dice la prensa de hospitality.
Fuentes secundarias, marcadas como tales:

- **Adopción ~9-10%.** Rankability (scan de septiembre 2026) mide **9,3%** de los top-1000
  dominios con `llms.txt` o `llms-full.txt` confirmado, y **8,3%** en los top-10.000. SE
  Ranking, sobre 300.000 dominios, mide **10,13%**. *[fuentes secundarias, metodologías
  distintas]*
- **Uso ~cero.** En el estudio de Ahrefs sobre ~38.000 dominios con un `llms.txt` válido,
  **el 97% no recibió ni una sola petición del archivo en mayo de 2026**, y el 96% de las
  peticiones que sí llegaron eran de bots. *[fuente secundaria; el sitio del estudio no es
  alcanzable desde este entorno de ingesta — ver límite declarado en `intel/market.md`]*
- **Ningún proveedor grande confirma leerlo** para decidir qué cita. Anthropic publica su
  propio `llms.txt` sin afirmar que sus crawlers usen el estándar; la guía de Google indica
  que archivos de ese tipo **no son necesarios** para aparecer en búsqueda generativa.

**Qué hacer con esto en un engagement.** Publicar `llms.txt` cuesta casi nada y no hace daño:
se deja como apuesta barata. **Lo que no se puede hacer es venderlo como la palanca de
visibilidad** — y es exactamente lo que recomiendan las guías de hospitality que circulan este
año. La palanca medible es el **JSON-LD del tipo correcto**, que sí se sabe que los motores
consumen. Si un cliente llega con "necesitamos `llms.txt`", la respuesta honesta es *sí, y
primero arreglemos el schema, que es donde está el 100% de la evidencia de uso.*

### El cuerpo de estándares del vertical, medido repo por repo

`OpenTravel` es el organismo de estándares de distribución de travel. En agosto de 2025 se sumó
a la **Overture Maps Foundation** bajo el paraguas de la Linux Foundation —el comunicado habla
de *"AI-ready travel infrastructure"*— y su sitio anuncia que pasará a llamarse **Open Travel
Foundation**. Esto es lo que hay en su organización de GitHub, medido el 2026-11-23:

| Repo | Licencia | Stars | Último push |
|------|----------|-------|-------------|
| `OpenTravel/OTM-DE` | **NONE** | 22 | 2020-11-23 |
| `OpenTravel/OTM-DE-Utilities` | **NONE** | 10 | 2024-04-01 |
| `OpenTravel/OpenTravel-Specifications` | **NONE** | 7 | 2024-11-26 |
| `OpenTravel/OTM-DE-Compiler` | NOASSERTION | 5 | 2024-01-31 |
| `OpenTravel/OTM-DE-Docs` | **NONE** | 4 | 2016-05-24 |
| `OpenTravel/OTA-Publication-Site` | **NONE** | 1 | 2024-09-09 |
| `OpenTravel/otm-dex` | Apache-2.0 | 0 | 2020-10-12 |
| `OpenTravel/ota2-repository-playbooks` | Apache-2.0 | 0 | 2024-05-19 |
| `OpenTravel/otm-test-workgroup` | **NONE** | 0 | 2024-03-05 |
| `OpenTravel/otm-workgroup-models` | **NONE** | 0 | 2024-09-12 |
| `OpenTravel/OTM_repo_test_sw` | **NONE** | 0 | 2025-01-16 |
| `OpenTravel/ota2-exporter-utility` | **NONE** | 0 | 2025-01-15 |

Doce repos. **El máximo es 22 estrellas. Ocho no declaran licencia. Nada tuvo push desde enero
de 2025.** La especificación OTA 1.0 se publica además bajo el *OpenTravel License Agreement*,
que **no es una licencia open source** y requiere aceptar términos del consorcio.

**La lectura, y es incómoda:** el vocabulario que efectivamente usan los agentes para encontrar
oferta de travel **no es el del organismo de travel** — es `schema.org`, Apache-2.0, 6316
estrellas, con push esta semana. Para un engagement eso simplifica la decisión: **modelar la
oferta en Schema.org y tratar a OTA/OTM como formato de integración con GDS heredado, no como
capa de descubrimiento.** La alineación con Overture es real y vale seguirla, pero a hoy es un
anuncio con un año y tres meses, no código.

## Plano terrestre — vender el tramo que no es el vuelo

Agregado el 2026-11-23 (quinta pasada). Los cuatro planos anteriores de esta KB (frontera,
vuelo, pago, visibilidad) dejaron un hueco que la propia KB venía declarando en dos archivos:
**el tramo terrestre**. `intel/market.md` lo llamaba "hueco abierto" y `compose/patterns.md`
decía que el único MCP ferroviario del mundo estaba dormido 15 meses. Esta pasada lo midió
en vez de repetirlo, y **la declaración anterior era falsa por el lado del acceso y verdadera
por el lado de la venta**.

La distinción que ordena todo lo que sigue:

- **Consultar** un tren (horario, andén, retraso, precio mostrado) → **existe, es permisivo,
  está vivo y tiene más de un proveedor.**
- **Vender** un tren (oferta, reserva de plaza, emisión, reembolso) → **no existe en open
  source en ninguna región del mundo.** Ver las brechas al final del archivo.

Es la misma ley estructural que el KB de retail formuló para fulfilment: *el piso open source
cubre la matemática y se detiene en el comercio*. Aquí se detiene un paso antes todavía: cubre
**la información** y se detiene en **la oferta**.

### Capa de especificación — y la inversión respecto de otros verticales

| Repo | Licencia (archivo leído) | Stars | Último push | Qué especifica | ¿Se puede vendorizar? |
|------|--------------------------|-------|-------------|----------------|------------------------|
| [UnionInternationalCheminsdeFer/OSDM](https://github.com/UnionInternationalCheminsdeFer/OSDM) | **Apache-2.0** (`LICENSE`, 11374B) | 95 | 2026-11-20 | Open Sales and Distribution Model (UIC IRS 90918-10): API de oferta, tarifa, reserva de plaza y emisión para ferrocarril y multimodal. **El estándar de venta del vertical terrestre.** | **Sí** — licencia de código plena, con concesión de patente |
| [UnionInternationalCheminsdeFer/OSDM-demo-app](https://github.com/UnionInternationalCheminsdeFer/OSDM-demo-app) | Apache-2.0 (`LICENSE`, 11357B) | 5 | 2026-03-26 | App de demostración del propio UIC sobre OSDM. | Sí — pero es demo, no producto |
| [MobilityData/gbfs](https://github.com/MobilityData/gbfs) | **CC BY 3.0** (`LICENSE`, 19467B) | 928 | 2026-11-18 | General Bikeshare Feed Specification: micromovilidad compartida (el último kilómetro del tramo terrestre). | **No como código** — es licencia de documentación: atribución sí, concesión de patente no |
| [transitland/transitland-atlas](https://github.com/transitland/transitland-atlas) | **CC BY 4.0** (`LICENSE.txt`, 18657B) | 200 | 2026-11-22 | Directorio abierto de feeds y operadores de movilidad. | No como código — es un dataset |
| [MobilityData/awesome-transit](https://github.com/MobilityData/awesome-transit) | **CC0-1.0** (`LICENSE.md`, 6974B) | 1870 | 2026-11-18 | El catálogo de referencia del ecosistema de transporte. | Sí, sin condiciones — CC0 es dominio público |

**Hallazgo que corrige una regla heredada de otra industria.** El KB de retail cerró su ciclo 9
con una regla generalizada a las 12 industrias: *"la licencia de una especificación es una
licencia de documentación y arrastra restricciones que las licencias de código no tienen"*
(beckn = CC BY-NC-SA, **no comercial**; ONDC = CC BY-ND, **sin derivados**). **En el plano
terrestre esa regla se invierte: el estándar de venta ferroviaria, OSDM, es Apache-2.0 —
licencia de código, con concesión expresa de patente.** No es una excepción accidental: UIC
la eligió explícitamente para fomentar la adopción por parte de las empresas ferroviarias.

La regla correcta, entonces, no es "las especificaciones son restrictivas" sino **"la licencia
de la especificación se decide por organismo, no por categoría, y hay que leerla una por una"**
— y en este mismo plano conviven las dos familias: OSDM es Apache-2.0 y GBFS, del mismo
ecosistema y con diez veces más estrellas, es CC BY 3.0. *Un cliente que quiera un perfil
propio de GBFS puede publicarlo (CC BY permite derivados); uno que quiera vendorizar el
esquema OSDM en su producto también puede, y además con cobertura de patente. Son permisos
distintos y la diferencia aparece recién en el archivo.*

### Capa de estándar europeo — NeTEx, SIRI, Transmodel y la licencia EUPL

| Repo | Licencia (archivo leído) | Stars | Último push | Para qué sirve | Nota de licencia |
|------|--------------------------|-------|-------------|----------------|------------------|
| [entur/netex-gtfs-converter-java](https://github.com/entur/netex-gtfs-converter-java) | **EUPL-1.2** (`LICENSE.txt`, 13793B) | 13 | 2026-11-23 | Convierte un dataset NeTEx a GTFS. Mantenido por Entur (operador estatal noruego). | Copyleft con cláusula de red — ver abajo |
| [entur/kishar](https://github.com/entur/kishar) | EUPL-1.2 | 12 | 2026-11-23 | Convertidor SIRI → GTFS-Realtime. | Igual |
| [Spillgebees/Transmodel](https://github.com/Spillgebees/Transmodel) | EUPL-1.2 (`LICENSE`, 13792B) | 3 | 2026-11-04 | Bindings C# tipados para NeTEx, SIRI y Transmodel. | Igual |
| [dbinfrago/openstation-docs](https://github.com/dbinfrago/openstation-docs) | Apache-2.0 (`LICENSE`, 11344B) | 38 | 2026-11-16 | API OpenStation de DB InfraGO: datos de estaciones ferroviarias alemanas. | Permisiva |
| [napcore-tools/web-awesome_napcore_tools](https://github.com/napcore-tools/web-awesome_napcore_tools) | MIT (`LICENSE`, 1130B) | 8 | 2026-11-18 | Catálogo público de herramientas de datos de movilidad para los NAP europeos. | Permisiva |
| [enroute-mobi/ara](https://github.com/enroute-mobi/ara) | AGPL-3.0 (`LICENSE`, 34520B) | 22 | 2026-11-14 | Servidor Go de intercambio de datos en tiempo real por protocolo SIRI. | Copyleft de red — como servicio, no embebido |

#### ⚠️ EUPL-1.2 es nueva para esta KB y **se comporta como AGPL, no como LGPL**

Las tres primeras filas traen una familia de licencia que no había aparecido en ninguno de los
cuatro planos anteriores. Vale la pena ser exacto, porque el nombre no lo dice: *European Union
Public Licence* suena institucional y neutro, y es **copyleft fuerte con alcance de red**.
Texto literal del archivo (`entur/netex-gtfs-converter-java/LICENSE.txt`, cláusula de
definiciones):

> — '**Distribution**' or '**Communication**': any act of selling, giving, lending, renting,
> distributing, communicating, transmitting, or otherwise making available, online or offline,
> copies of the Work **or providing access to its essential functionalities** at the disposal
> of any other natural or legal person.

"Providing access to its essential functionalities" es, textualmente, **más amplio que el
gatillo de la AGPL-3.0**: no exige modificar el software ni siquiera distribuirlo — alcanza con
poner sus funcionalidades esenciales a disposición de un tercero. Consecuencia operativa
directa: **un SaaS de cliente que exponga la conversión NeTEx→GTFS de Entur como funcionalidad
dispara la reciprocidad.** La EUPL sí trae un anexo de *licencias compatibles* (permite
redistribuir bajo GPL/AGPL y otras listadas), lo cual ayuda a integrar, no a cerrar.

**Para el estudio:** los convertidores de Entur se usan **como proceso batch fuera del producto**
(entra NeTEx, sale GTFS, el producto consume GTFS), nunca enlazados dentro del servicio que se
le entrega al cliente. Es exactamente la misma disciplina que esta KB ya aplica a Nominatim y
a navitia, con un gatillo más ancho.

### Capa de acceso — lo que sí existe, es permisivo y está vivo

Esta es la capa que la KB daba por inexistente. **No lo es: existe, es ISC/MIT y tiene push
reciente.** Lo que pasa es que no tiene forma de MCP, así que no aparece buscando "agente".

| Repo | Licencia (archivo leído) | Stars | Último push | Qué da | ¿Base para AI? |
|------|--------------------------|-------|-------------|--------|----------------|
| [public-transport/hafas-client](https://github.com/public-transport/hafas-client) | **ISC** (`license.md` minúscula, 727B) | 372 | 2026-08-23 | Cliente JS de las APIs HAFAS: el motor detrás de decenas de operadores europeos (DB, ÖBB, SNCB, regionales). **El repo más grande del plano terrestre de venta/consulta.** | Sí — horarios, trayectos y precios mostrados como herramienta de agente |
| [OpendataCH/Transport](https://github.com/OpendataCH/Transport) | **MIT** (`LICENSE`, 1060B) | 269 | 2026-11-22 | API pública de transporte suizo. Push de esta semana. | Sí — y es la referencia de API limpia del segmento |
| [public-transport/db-vendo-client](https://github.com/public-transport/db-vendo-client) | ISC (`LICENSE.md`, 777B) | 209 | 2026-09-10 | Cliente de las APIs actuales de Deutsche Bahn, sucesor de `db-hafas` tras la migración de DB. | Sí — el camino vivo a inventario ferroviario alemán |
| [public-transport/db-hafas](https://github.com/public-transport/db-hafas) | ISC | 81 | 2025-01-17 | Cliente HAFAS de DB. **Dormido ~22 meses**; reemplazado por `db-vendo-client`. | Solo referencia histórica |
| [schildbach/public-transport-enabler](https://github.com/schildbach/public-transport-enabler) | **GPL-3.0** (`COPYING`, 32473B) | 456 | 2026-11-22 | El equivalente Java de `hafas-client`, con más redes cubiertas. Muy vivo. | Como servicio separado — **GPL-3.0, no se embebe** |
| [hove-io/navitia](https://github.com/hove-io/navitia) | **AGPL-3.0** (`COPYING`, 34520B) | 456 | 2026-11-10 | Motor de planificación multimodal de grado operador (el que corre Île-de-France Mobilités). | Como servicio, nunca embebido |
| [juliuste/interrail](https://github.com/juliuste/interrail) | ISC (`license`, 730B) | 34 | 2020-10-12 | Cliente de la API Interrail/Eurail: estaciones y rutas paneuropeas. **Dormido 6 años.** | No sin reescritura — se cita por ser el único del nicho |

#### ⚠️ La licencia del endpoint: un tercer paso de diligencia, no un segundo

El ciclo anterior de esta KB agregó un segundo paso de diligencia a partir de
`openskynetwork/opensky-api`: *la licencia del código no es la licencia del dato*. **El plano
terrestre obliga a un tercero, más duro: la licencia del código no es la licencia del
endpoint.**

`hafas-client` y `public-transport-enabler` son software limpio y permisivo/GPL que habla con
**endpoints internos de operadores ferroviarios que no están documentados ni publicados como
API pública**. El código se puede usar; **el permiso para llamar a ese endpoint en producción,
a escala y con fines comerciales, no viene con el repo y en general no existe.** Es el mismo
riesgo de términos de servicio que esta KB ya anotó para `LetsFG` y para `punitarani/fli`, y
la misma trampa que `SeanChangX/THSR-Sniper` lleva al extremo (ver `agents/top.md`).

**Regla práctica para un engagement:** `hafas-client` sirve para **prototipar en días** y para
**demostrar la forma del producto**; el contrato de distribución con el operador (o un agregador
licenciado) es lo que lo lleva a producción. Decirlo al presupuestar, no al entregar.

### Capa de datos abiertos — la que sí está contractualmente limpia

Frente a lo anterior, esta capa se apoya en feeds **publicados para ser consumidos**, con
licencia de dato explícita. Es la que se recomienda para producción cuando no hay contrato.

| Repo | Licencia (archivo leído) | Stars | Último push | Qué da |
|------|--------------------------|-------|-------------|--------|
| [MobilityData/gtfs-validator](https://github.com/MobilityData/gtfs-validator) | Apache-2.0 (`LICENSE`, 11327B) | 434 | 2026-11-19 | El validador canónico de GTFS Schedule. Higiene antes de que el agente lea. |
| [MobilityData/mobility-database-catalogs](https://github.com/MobilityData/mobility-database-catalogs) | Apache-2.0 (`LICENSE`, 11357B) | 354 | 2026-11-19 | Catálogo de fuentes de la Mobility Database: dónde está el feed de cada operador. |
| [OneBusAway/onebusaway-application-modules](https://github.com/OneBusAway/onebusaway-application-modules) | Apache-2.0 **por referencia** (`LICENSE.txt`, 547B) | 243 | 2026-11-18 | Suite completa de información al pasajero en tiempo real, grado operador. |
| [OneBusAway/onebusaway-gtfs-modules](https://github.com/OneBusAway/onebusaway-gtfs-modules) | Apache-2.0 por referencia (`LICENSE.txt`, 547B) | 149 | 2026-11-17 | Librería Java de lectura/escritura/transformación de GTFS. |
| [TransitApp/gtfs-fares-v2-validator](https://github.com/TransitApp/gtfs-fares-v2-validator) | MIT (`LICENSE`, 1068B) | 7 | 2025-03-31 | Validador de GTFS-Fares v2 — el modelo abierto de tarifas. **ARCHIVADO** (`archived: true`). |

#### Dos lecturas de licencia que no se ven desde la API de GitHub

1. **`interline-io/transitland-lib` es GPL-3.0 con opción comercial de pago, y GitHub dice
   `NOASSERTION`.** El archivo (35434B) abre así: *"`transitland-lib` is released under a
   'dual license' model: open-source for use by all under the GPLv3 license (which follows
   below) — also available under a flexible commercial license from Interline (contact
   info@interline.io for a quote)"*. **Esto completa la regla de `NOASSERTION` en las dos
   direcciones:** en `valhalla` esa misma bandera escondía un MIT literal (hallazgo del ciclo
   9 de esta KB); aquí esconde un copyleft con peaje. *`NOASSERTION` no informa nada sobre si
   la licencia es buena o mala — solo que GitHub no pudo clasificar el archivo. Hay que
   abrirlo siempre, y en ambos sentidos.*

2. **El `LICENSE.txt` de OneBusAway es una plantilla sin expandir.** Son 547 bytes y su primera
   línea es literalmente el token `COPYRIGHT_SECTION`, seguido del encabezado estándar
   *"Licensed under the Apache License, Version 2.0"* con el enlace a apache.org. **La
   concesión está por referencia y es identificable — a diferencia de un badge, que no
   concede nada** (regla del ciclo 9 de retail). Lo que falta es el titular del copyright, y
   eso importa en concreto: la Apache-2.0 §4(d) obliga a propagar los avisos de atribución, y
   acá no hay aviso que propagar. **Es usable; el string de atribución se resuelve con el
   proyecto antes de entregar, no después.**

#### Método: `raw.githubusercontent.com` distingue mayúsculas, y eso casi cuesta un hallazgo

Buscando el archivo de licencia de `hafas-client` por `LICENSE`, `LICENSE.md`, `LICENSE.txt` y
`COPYING`, los cuatro dieron **404**, y el repo quedó a un paso de registrarse como "sin
licencia" — con 372 estrellas, habría sido una afirmación grave y falsa. **El archivo existe y
se llama `license.md`, en minúscula**: ISC literal, 727 bytes. Esta KB ya tenía el dato suelto
(anotó que Kamra PMS publica su texto AGPL en `license.txt` minúscula) pero no la regla.

**La regla, ahora explícita: la licencia es el archivo, y el archivo distingue mayúsculas.**
Un chequeo que solo prueba `LICENSE*` produce falsos negativos silenciosos. Hay que probar
también `license`, `license.md`, `license.txt`, `licence`, `COPYING` y `NOTICE` antes de
escribir "no tiene licencia" sobre un repositorio ajeno.

## Brechas medidas, no silenciadas

Estas consultas se corrieron sobre `search/repositories` el 2026-11-21 y devolvieron lo que
se indica. Una brecha informada es información; el silencio parece cobertura.

| Consulta | Resultados | Lectura |
|----------|-----------|---------|
| `airline NDC booking stars:>=20` | **0** | No existe implementación open source de NDC con tracción. NDC es XML con esquema licenciado por IATA y acceso contractual — por eso no hay nada en GitHub. **Aquí es donde pertenece la IP propietaria.** |
| `hospitality revenue management stars:>=30` | **0** | Cero revenue management open source. El RM es el centro de beneficio del hotel; nadie lo libera. Es la oportunidad de producto más limpia del vertical. |
| `amadeus sabre travelport sdk stars:>=50` | **0** | Los SDKs de GDS no tienen comunidad abierta; el único relevante (Amadeus) está archivado. |
| `travel agency ERP tour operator open source stars:>=20` | **0** | No hay back-office de agencia/tour operador open source. El hueco equivalente a "Odoo para travel" sigue vacío. |
| `hostel vacation rental booking management stars:>=100` | **0** | Nada en alquiler vacacional por encima de 100★. |
| `airport flight delay prediction stars:>=50` | **0** | Sorprendente: cero. Los datasets existen, los modelos abiertos no. |
| `restaurant reservation booking system stars:>=300` | **0** | Sin base reservable para F&B hotelero. |
| `turismo viajes IA agente` (español) | **1 repo, 0★** | El ecosistema open source de travel **no habla español**. Ver `intel/market.md` → LATAM. |

### Brechas del plano de frontera, medidas el 2026-11-23

Mismo método, consultas nuevas. **El contraste es el hallazgo:** leer el documento tiene seis
repos permisivos; *decidir* con el documento tiene cero.

| Consulta | Resultados | Lectura |
|----------|-----------|---------|
| `APIS advance passenger information stars:>=20` | **0** | Cero implementaciones de APIS/API-PNR. Es el mensaje que toda aerolínea debe transmitir a toda autoridad de frontera del mundo, y no existe en abierto. |
| `timatic travel document check stars:>=20` | **0** | Timatic (IATA) no tiene ni alternativa ni cliente open source. **Es el monopolio de datos más limpio que esta red de KBs midió en cualquier industria.** |
| `etias stars:>=20` | **0** | Cero. Un sistema que afectará a ~1.400M de viajeros no tiene una sola librería preparatoria pública. |
| `biometric boarding airport stars:>=20` | **0** | La biometría de embarque es íntegramente de proveedor (SITA, Idemia, NEC). |
| `passenger name record PNR stars:>=20` | **0** | Ninguna librería de PNR. El formato más viejo y más usado de la industria no tiene parser abierto con tracción. |
| `visa requirements api stars:>=20` | **1, y es colisión** | El único resultado es `jettbrains/-L-` (174★, GPL-3.0), un repo de activación de JetBrains. Nada que ver con visas. **Cero real.** |
| `visa requirements stars:>=10` | 8, **2 utilizables** | Los dos datasets de arriba. El resto: la colisión de JetBrains, una búsqueda de empleo en Berlín y un visualizador 3D (`ThekareemOne/visaverse`, MIT, 23★, lindo y sin dato propio). |

**La forma de la brecha, dicha de una vez:** el open source de frontera **lee el documento y
prueba atributos, pero no conoce la regla**. Entre "sé quién sos" y "podés entrar" hay un
dato — la regla de admisión por par pasaporte×destino, con su fecha de vigencia — que no
existe en abierto, **y esa es la pieza de IP más defendible de todo el vertical travel**,
junto con revenue management.

### Brechas del plano operativo de vuelo, medidas el 2026-11-23

Mismo método, consultas nuevas sobre `search/repositories`. **El contraste vuelve a ser el
hallazgo, y esta vez es interno al propio plano:** el dato *crudo* del vuelo (dónde está el
avión) tiene quince repositorios vivos; el dato *comercial* del vuelo (qué se le debe al
pasajero) tiene cero.

| Consulta | Resultados | Lectura |
|----------|-----------|---------|
| `flight delay prediction stars:>=50` | **1, y no es del vertical** | El único resultado es `kanitvural/aws-data-science-data-engineering-mlops-infra` (59★, MIT): un tutorial de plataforma AWS que *usa* retrasos de vuelo como dataset de ejemplo. **Cero modelos de predicción de retraso reutilizables.** Confirma la medición del 2026-11-21 por segunda vez y con otra consulta. |
| `flight disruption rebooking stars:>=10` | **0** | Nada de reacomodación. La Receta 3 y la Receta 10 se construyen sobre lógica propia por definición. |
| `EU261 flight compensation stars:>=5` | **0** | **Cero.** El régimen de compensación de pasajeros más conocido del mundo, con veinte años de jurisprudencia, no tiene una sola implementación abierta. Lo mismo vale para la regla de reembolso del US DOT. |
| `GDS PNR parser stars:>=5` | **0** | Segunda medición independiente del hueco de PNR ya registrado arriba. |
| `airline schedule SSIM stars:>=5` | **0** | SSIM es **el** formato de horarios de la industria (IATA Standard Schedules Information Manual). Cero parsers abiertos. |
| `IROPS irregular operations airline stars:>=1` | **0** | Ni siquiera con umbral de 1★. El término que la industria usa para su problema más caro no aparece en GitHub. |
| `aviation emissions CO2 stars:>=20` | **0 en su momento — ⚠️ CORREGIDO el 2026-11-23** | Esta fila decía que "nadie publicó el tooling" alrededor de `google/travel-impact-model`. **Es falso a noviembre de 2026**: existe `dupontcyborg/flightyco2` (MIT, port fiel validado al 0,07%, commit 2026-11-16) y `abahgat/timcp` (Apache-2.0). La búsqueda filtraba por estrellas; el tooling existe por debajo de ese umbral. Ver *Plano de emisiones y reporte* al final de este archivo. |
| `travel carbon footprint stars:>=30` | 2, **0 utilizables** | `CarbonFootprintAGU` (GPL-3.0, sin push desde 2021-03-20) y `J0ANMM/carbon-calculator` (MIT, **último commit real 2022-05-28**, no 2023-05-21 como decía esta fila — corregido el 2026-11-23 clonando el repo). Ambos muertos. |
| `flight status MCP server stars:>=10` | **1** | Solo `CPLX/flighty-mcp-server` (35★, MIT, sin push desde 2026-08-31). **El estado de vuelo — el dato que más se consulta en todo travel — tiene un (1) MCP server por encima de 10★.** |

**La forma de esta brecha, dicha de una vez:** el open source de vuelo **sabe dónde está el
avión, pero no sabe qué se le debe al pasajero.** La posición de la aeronave es un bien común
razonablemente bien cubierto; la **regla de compensación** —EU261 en EMEA, la regla de
reembolso automático del DOT en North America, cada una con sus umbrales y sus plazos— no
existe en abierto en ninguna jurisdicción. Es la **misma forma** que el plano de frontera (se
lee el documento, no se conoce la regla) y apunta a la misma conclusión comercial: **el valor
defendible está en el motor de reglas fechadas, no en el acceso al dato.** Con una diferencia
que mejora el caso: aquí la regla **está publicada y es citable** — un reglamento del DOT, un
reglamento de la UE—, al revés de Timatic, que además es propietaria.

### Brechas del plano terrestre, medidas el 2026-11-23

Consultas corridas sobre `search/repositories`. **Todas las que dan 0 son ceros reales, no
consultas que no se hicieron.**

| Consulta | Resultados | Lectura |
|----------|-----------|---------|
| `osdm client implementation` | **0** | **El hallazgo central del plano.** El estándar de venta ferroviaria es Apache-2.0, está publicado en GitHub y tiene 95 estrellas — y **no existe una sola implementación cliente open source**. Lo único que lo toca es `mainmatter/reStations` (Apache-2.0, 8★), que implementa **solo la Places API** —estaciones, no venta— y está **dormido desde 2025-04-02**. |
| `train booking api stars:>=20` | **0** | Nadie publicó un cliente de reserva ferroviaria con tracción mínima, en ninguna región. |
| `fare engine open source` | **0** | No hay motor de tarifas. Es la pieza que convierte un horario en un precio vendible. |
| `ticket vending machine open source` | **0** | No hay emisión. |
| `bus ticketing system stars:>=100` | **0** | Ver el bloque LATAM de `intel/market.md`: el modo dominante de la región no tiene software libre de venta en ninguna parte del mundo. |
| `car rental booking open source stars:>=50` | **0** | El otro medio terrestre tampoco. Un itinerario puerta a puerta no se puede completar con open source en su tramo de alquiler. |
| `mobility as a service maas open source stars:>=50` | **0** | "MaaS" es una categoría comercial, no un cuerpo de código. |
| `intermodal itinerary agent llm` | **0** | No hay agente intermodal. Las recetas 5 y 15 de esta KB hay que construirlas, no adoptarlas. |
| `passenger rights compensation rail` | **0** | Cero, igual que el equivalente aéreo (EU261) medido en la pasada de vuelo. La regla está publicada; el motor no existe en ninguno de los dos modos. |
| `rail revenue management` | 9 | Los cuatro primeros tienen **0 estrellas, sin licencia** y son trabajos académicos o de curso. Equivale a cero, y confirma lo ya medido para hotelería: **el revenue management no se libera en ningún modo de transporte.** |
| `irctc api stars:>=20` | **0** | India: sin API oficial y sin cliente con tracción. Lo que hay son scrapers de terceros. |
| `odpt tokyo transport open data` | **0** | Japón: la plataforma ODPT existe como servicio, pero **no tiene presencia medible en GitHub con ese nombre**. |
| `gtfs latam brasil` | **0** | Ninguna herramienta GTFS con identidad regional LATAM. |
| `rodoviaria passagem api` | 1 | Un repo, 0 estrellas, sin licencia, 2024. |
| `autobus boleto api` | 1 | Un repo, 0 estrellas, sin licencia, 2023. |
| `onibus passagem` | 53 | Los seis primeros: **0–2 estrellas, ninguno con licencia**, trabajos de materia. |

**Lo que estas 16 filas dicen juntas.** El tramo terrestre tiene un estándar de venta abierto
y permisivo (OSDM, Apache-2.0) **sin ninguna implementación**, y una capa de consulta rica,
viva y permisiva **que no puede vender**. La brecha no es de información: es de **oferta,
inventario y emisión**. Para el estudio eso define con precisión dónde está el trabajo
construible y dónde no hay nada que adoptar.

**No examinado en esta pasada, y se dice en vez de omitirse:** China (12306 y los agregadores
locales), Corea, metro/urbano de pago con tarjeta (EMV open loop), carga ferroviaria, y el
estado legislativo posterior al 2026-05-13 de los tres instrumentos europeos de ticketing.

---
*Ver también: `verticals/solutions.md` para plataformas verticales completas.*

## Plano de emisiones y reporte — el tramo que la regulación vuelve obligatorio

Sexta pasada del 2026-11-23. Las cinco pasadas anteriores cubrieron frontera,
operación de vuelo, pago agentic, visibilidad agentic y tierra. Este plano
quedaba abierto, y es el único del vertical donde el entregable no lo pide el
viajero sino el regulador: CSRD/ESRS en EMEA, CORSIA en ICAO, Scope 3
categoría 6 en el reporte corporativo de cualquier cliente con programa de
viajes.

**Esta pasada corrige una brecha que esta misma KB había registrado como
vacía.** La línea 516 de este archivo decía que la búsqueda
`aviation emissions CO2 stars:>=20` devolvía **0** y que "nadie publicó el
tooling alrededor" de `google/travel-impact-model`. Es falso a noviembre de
2026: el tooling existe, es MIT y Apache-2.0, y está vivo. Se listan abajo.

### Método de verificación de esta tabla

Las licencias **no** salen de la descripción del repo ni de la API de GitHub
(bloqueada para esta sesión): salen de `git clone --depth 1` y de leer el
archivo `LICENSE` del repo. La fecha es la del último commit de `HEAD`.
**No se registran estrellas**: esta sesión no tuvo forma de medirlas, y las
estrellas inventadas son exactamente el defecto que el ciclo 9 encontró en los
ciclos 5, 6 y 8 de esta KB.

### Capa usable — permisiva y viva

| Repo | Licencia (leída en LICENSE) | Último commit | Qué es |
|---|---|---|---|
| https://github.com/dupontcyborg/flightyco2 | MIT | 2026-11-16 | Port fiel de TIM 3.0.0 a TypeScript, validado contra el ejemplo publicado de Google **dentro del 0,07%**. Curvas de quemado EEA por aeronave, ajuste de distancia GAIA, conversión well-to-wake CORSIA, asignación por área de asiento. Corre client-side. |
| https://github.com/abahgat/timcp | Apache-2.0 | 2026-02-01 | Servidor MCP sobre la API del Travel Impact Model. 6 tools, entre ellas `tim_get_scope3_flight_emissions` y su variante batch. Es la pieza que convierte el plano en algo que un agente puede llamar. |
| https://github.com/andreacappelletti97/google-flights-mcp | ISC | 2026-11-01 | Servidor MCP de vuelos que devuelve CO₂ por leg junto al precio. ISC es permisiva y OSI, equivalente funcional a MIT. |
| https://github.com/davidmegginson/ourairports-data | Dominio público (Unlicense) | 2026-11-23 | Coordenadas, ICAO e ISO de país de todo aeropuerto con código IATA. Se actualiza a diario — commit del día de esta pasada. Es el join key de todo cálculo de distancia. |

Cuatro filas. Son las cuatro reales, permisivas y vivas que se encontraron.

### Capa de metodología — y la contradicción de licencia que importa

| Repo | Licencia | Último commit | Veredicto |
|---|---|---|---|
| https://github.com/google/travel-impact-model | **Contradictoria — ver abajo** | 2026-11-04 | Metodología, **no código** |

`google/travel-impact-model` no contiene implementación. El repo entero es
`README.md` + `contributing.md` + `images/` + `projects/`. "Usar TIM" significa
una de dos cosas: implementarlo (lo hizo `flightyco2`) o llamar a la API de
Google (lo hace `timcp`).

⚠️ **El repo se contradice a sí mismo sobre su licencia, y nadie lo nota:**

- El archivo `LICENSE` dice `Attribution 4.0 International` — **CC BY 4.0**.
- El `README.md`, línea 694, dice **CC BY-SA 4.0**, con ShareAlike.

No son lo mismo y la diferencia es cara: ShareAlike es vírico sobre el dato
derivado. Si Globant publica una tabla de factores derivada de TIM y aplica
CC BY-SA, se obliga a liberar bajo la misma licencia; si aplica CC BY, puede no
estar cumpliendo. **Resolver con Google/Travalyst por escrito antes de publicar
dato derivado, no elegir la lectura conveniente.**

⚠️ **Y lo que casi todo el mundo infiere mal:** TIM **no es Apache-2.0**. La
única mención de Apache-2.0 en el repo está en las notas al pie 2 y 4, y cubre
**los íconos de las figuras** (Material Design Icons), no el modelo. Un filtro
automático de "Google ⇒ Apache" lo clasifica mal. Ninguna de las dos lecturas
—CC BY o CC BY-SA— es una licencia de software: son licencias de contenido, y
no dan permiso de patente.

### Lo que TIM sí aporta y no hay que reimplementar

`projects/scope3_cat6_flight_emissions.md` define el esquema de **tres tiers**
que el reporte corporativo necesita, y es la parte directamente reutilizable:

| Tier | Cuándo | Insumo |
|---|---|---|
| 1 (alta exactitud) | Hay registro de vuelos pasados concretos | Origen, destino, fecha |
| 2 (fallback) | Se conoce la ruta, no el vuelo | Origen y destino |
| 3 (estimación básica) | Sólo hay agregado | Distancia total recorrida |

TIM descompone en WTT (upstream del combustible), TTW (combustión) y cubre
vuelos comerciales programados desde 2019. Está alineado a **ISO 14083**, que
define el viaje puerta a puerta — y aquí está el límite que hay que decirle al
cliente: **TIM estima sólo el tramo aéreo**. Aeropuerto, tren y coche al
aeropuerto quedan fuera, y ISO 14083 los pide. El viaje completo no lo cubre
ningún repo permisivo encontrado.

### Capa descartada — medida, no asumida

| Repo | Licencia | Último commit | Por qué no |
|---|---|---|---|
| https://github.com/majidkabir/Sootcase | **PolyForm Noncommercial 1.0.0** | 2026-11-23 | Se describe como "open freight CO₂e calculator" y sigue GLEC/ISO 14083, pero **prohíbe uso comercial**. Una consultora no puede usarlo en engagement. Activo hoy mismo — la trampa es que parece la mejor opción. |
| https://github.com/majidkabir/Carbonara | **PolyForm Noncommercial 1.0.0** | 2026-11-23 | Mismo autor, misma licencia, mismo veredicto. Su propio README aclara que no está certificado contra ISO 14083. |
| https://github.com/branliu0/flight-calculator | **SIN archivo de licencia** | 2020-05-25 | Sin licencia = todos los derechos reservados. Muerto hace 6 años. |
| https://github.com/muhammad7hadii/flight-emissions-app | **SIN archivo de licencia** | 2026-10-24 | Activo, pero sin licencia y su propio README dice que no es un modelo regulatorio ni operacional. Educativo. |
| https://github.com/hdykiel/emissions | Apache-2.0 | 2022-01-04 | Licencia correcta, pero WIP declarado y muerto desde 2022. |
| https://github.com/J0ANMM/carbon-calculator | MIT | 2022-05-28 | Multimodal (vuelo, bus, coche, ferry). Muerto. **Corrección:** la línea 517 de este archivo lo daba como "sin push desde 2023-05-21"; el commit real de `HEAD` es **2022-05-28**, un año antes. |
| https://github.com/jagan-shanmugam/climatiq-mcp-server | MIT | 2025-03-28 | Licencia correcta, pero wrapper de la **API comercial de Climatiq**: el repo es libre, el dato se paga. Sin commits en ~20 meses. |
| https://github.com/VIMS-Coder/Sootcase | — | — | **404.** Lo devolvió el buscador; `git clone` falla. No existe. |

### El dato de abajo no es tan libre como el código de arriba

`flightyco2` es MIT, pero su cadena de datos **no es uniforme**, y su propio
`data/README.md` lo documenta con una honestidad que conviene copiar:

| Fuente | Licencia | Estado en el repo |
|---|---|---|
| OurAirports | Dominio público | Se baja fresco en cada corrida |
| GAIA (ratios de distancia/combustible, ADS-B 2019) | CC-BY, registro Zenodo inmutable | Commiteado (~1 MB) |
| Planilla EEA (curvas de quemado por aeronave) | **"murky"**, según el propio repo | **gitignored** — no se puede auto-bajar, se descarga a mano |
| DEFRA 2024 (factores UK) | Gubernamental UK | Regenerable por script |

⚠️ **La planilla EEA es la dependencia operativa real de este plano.** No se
puede automatizar su descarga ("la URL rota"), su licencia está sin aclarar, y
sin ella `flightyco2` cae al fallback DEFRA. Para un entregable de cliente eso
significa: o se resuelve la licencia EEA, o se documenta que una fracción de los
vuelos se calcula con un método menos exacto. El repo ya marca por vuelo qué
método corrió — **esa columna es auditoría, no detalle: no la borren al
integrar.**

### Brechas del plano de emisiones, medidas el 2026-11-23

| Lo que se buscó | Resultado |
|---|---|
| Librería permisiva de emisiones de **hotel** (ISO 14083 / HCMI / CHSB) | **Cero.** Ningún repo MIT/Apache de huella de alojamiento. El vertical mide el vuelo y no mide la cama. |
| Cobertura **puerta a puerta** ISO 14083 en un repo permisivo | **Cero.** TIM cubre sólo el tramo aéreo y lo dice; los repos multimodales permisivos (`J0ANMM`) están muertos. |
| Implementación OSS de cumplimiento **CORSIA** o **EU ETS** (cálculo de obligación, cancelación de EEU) | **Cero.** Hay modelos de estimación, no hay herramienta de cumplimiento. Es software de compliance y vive cerrado. |
| Calculadora GLEC/ISO 14083 con licencia comercialmente usable | **Cero.** Las dos que existen (`Sootcase`, `Carbonara`) son PolyForm Noncommercial. |
| Servidor MCP de emisiones **sin API key de terceros** | **Cero.** `timcp` necesita key de Google; `climatiq-mcp-server` necesita key de Climatiq. El único camino sin key es embeber `flightyco2` (MIT) como librería. |

### ⚠️ Lo que esta sesión NO pudo verificar, dicho en voz alta

La política de egreso de esta sesión devolvió **403 en el CONNECT** para todo
host que no fuera GitHub. Verificado con `curl -sS -I`:

| URL | Resultado |
|---|---|
| `https://travelimpactmodel.org/about-tim` | 403 del proxy — **no verificable aquí** |
| `https://developers.google.com/travel/impact-model` | 403 del proxy — **no verificable aquí** |
| `https://zenodo.org/records/8369564` (GAIA) | 403 del proxy — **no verificable aquí** |
| `https://travalyst.org/work/aviation-industry/` | 403 del proxy — **no verificable aquí** |
| `https://flightyco2.com` | 403 del proxy — **no verificable aquí** |

403 del proxy **no** significa que el sitio esté caído: significa que esta
sesión no tenía permiso de salida. Esas cinco URLs se citan en esta KB como
referencia de contexto y **están sin verificar**. Todas las URLs de GitHub de
este archivo sí se verificaron, con `git ls-remote` o `git clone --depth 1`.

## Plano de accesibilidad — digital resuelto, físico huérfano

Séptima pasada del 2026-11-23. Dos subplanos con licencias y madurez opuestas:

- **Digital** (¿puede un usuario con lector de pantalla completar la reserva?):
  maduro, vivo, con opciones Apache-2.0. Lo empuja la EAA en EMEA desde el
  28-06-2025.
- **Físico** (¿puede una persona en silla de ruedas llegar, entrar y ducharse?):
  sin término en schema.org, con dos motores de ruteo LGPL, un esquema
  norteamericano **No-Derivatives** y cero agentes.

**Método.** `git ls-remote` 27/27 vivos; estrellas y `pushed_at` por
`search/repositories` el 2026-11-23; **licencia leída del archivo**, porque en
este plano **el badge de GitHub se equivoca en ambas direcciones** (ver
`openrouteservice` abajo).

### Capa digital — auditoría del flujo de reserva

| Repo | Licencia (archivo) | Stars | Último push | Rol |
|---|---|---|---|---|
| [GoogleChrome/lighthouse](https://github.com/GoogleChrome/lighthouse) | Apache-2.0 | 31193 | 2026-11-20 | Auditoría con score; su categoría de accesibilidad corre sobre `axe-core`. |
| [dequelabs/axe-core](https://github.com/dequelabs/axe-core) | **MPL-2.0** | 7872 | 2026-11-19 | El motor de reglas WCAG de facto. Copyleft **por archivo**: usar sin modificar, no parchear. |
| [IBMa/equal-access](https://github.com/IBMa/equal-access) | **Apache-2.0** | 788 | 2026-11-13 | El **único motor de reglas de escala con licencia totalmente permisiva**. Segundo motor en CI, o reemplazo si el cliente veta MPL. |
| [pa11y/pa11y](https://github.com/pa11y/pa11y) | LGPL-3.0 | 4604 | 2026-11-16 | Runner de tests. Se corre como herramienta en CI, no se embebe. |
| [pa11y/pa11y-ci](https://github.com/pa11y/pa11y-ci) | LGPL-3.0 | 649 | 2026-11-23 | Runner de CI sobre una lista de URLs (búsqueda → resultados → checkout). |
| [ryersondmp/sa11y](https://github.com/ryersondmp/sa11y) | **GPL-2.0** | 338 | 2026-11-19 | QA visual para editores de contenido. ⚠️ `LICENSE.md`: **v2.0 y anteriores eran MIT**; lo actual es GPL. GitHub muestra `NOASSERTION`. |
| [nvaccess/nvda](https://github.com/nvaccess/nvda) | GPL-2.0-or-later + 2 excepciones (`copying.txt`) | 2692 | 2026-11-23 | Lector de pantalla para la prueba **manual** que ningún escáner reemplaza. Herramienta de QA, nunca dependencia. |

### Capa física — ruteo con perfil de silla de ruedas

| Repo | Licencia (archivo) | Stars | Último push | Rol |
|---|---|---|---|---|
| [GIScience/openrouteservice](https://github.com/GIScience/openrouteservice) | **LGPL-3.0** (`LICENSE` + `LICENSE.LESSER`; cabeceras Java: LGPL-2.1-or-later) | 1996 | 2026-11-23 | Ruteo peatonal con **27 archivos `Wheelchair*`** en el árbol: pendiente (`WheelchairIncline`), cordón (`WheelchairKerb`), superficie, lisura, aptitud. |
| [opentripplanner/OpenTripPlanner](https://github.com/opentripplanner/OpenTripPlanner) | LGPL-3.0-or-later | 2781 | 2026-11-23 | Ruteo multimodal con accesibilidad (`doc/user/Accessibility.md`); modela **desconocido ≠ inaccesible**, pendiente máx. 8,3%, transbordos accesibles pre-calculados opcionales. |
| [MobilityData/gtfs-validator](https://github.com/MobilityData/gtfs-validator) | Apache-2.0 | 434 | 2026-11-19 | Valida el **grafo interior de la estación** (GTFS-Pathways): `PathwayLoop`, `PathwayDanglingGenericNode`, `PathwayReachableLocation`, `PathwayStopAccess`, `PathwayEndpointType`, `MissingLevelId`. Sin esto, el ruteo accesible rutea sobre basura. |
| [MobilityData/mobility-database-catalogs](https://github.com/MobilityData/mobility-database-catalogs) | Apache-2.0 | 354 | 2026-11-19 | Catálogo de feeds GTFS: de dónde sale el dato a validar. |
| [TaskarCenterAtUW/AccessMap](https://github.com/TaskarCenterAtUW/AccessMap) | **GPL-3.0-or-later** (archivo; GitHub: `NOASSERTION`) | 2 | 2026-10-14 | Ruteo de veredas sensible a preferencias de accesibilidad. **Es donde se mudó AccessMap** — ver capa descartada. |

### ⚠️ `openrouteservice`: tres fuentes, tres licencias, ninguna es la del badge

| Fuente | Dice | Es |
|---|---|---|
| Wiki de OpenStreetMap | Apache-2.0 | **Cierto hasta 2018.** El primer `LICENSE` (commit `811c28dee`, 2017-09-13) era Apache. |
| Badge y API de GitHub | GPL-3.0 | **Lectura errónea.** GitHub lee sólo `LICENSE`, que contiene el texto GPL — que es como **LGPL-3.0 se distribuye por convención**. |
| El repo | `LICENSE` + `LICENSE.LESSER` (commit `d81d11794`, 2018-09-20: *"Changed license to LGPL3"*) | **LGPL-3.0.** Las cabeceras de los `.java` dicen LGPL-2.1-or-later. |

Por qué importa más allá de este repo: **un escáner de licencias que lee el badge
bloquea un uso legítimo** (GPL) y **una wiki desactualizada deja pasar
obligaciones** (Apache). Ambos errores son sistemáticos. Para cualquier repo con
`LICENSE.LESSER` o `COPYING.LESSER`, el badge de GitHub dice GPL y miente.

### Capa física — vocabulario y dato

| Repo | Licencia (archivo) | Stars | Último push | Rol |
|---|---|---|---|---|
| [sozialhelden/a11yjson](https://github.com/sozialhelden/a11yjson) | **MIT** | 115 | 2026-10-07 | **El vocabulario que schema.org no tiene.** Interfaces tipadas con unidades físicas: `Room`, `Entrance`, `Door`, `Shower`, `Restroom`, `Toilet`, `GrabBars`, `Stairs`, `Slope`, `Pathways`, `Parking`, `PersonalProfile`. El bloque permisivo central del plano. |
| [sozialhelden/wheelmap-frontend](https://github.com/sozialhelden/wheelmap-frontend) | **MIT** (archivo) | 57 | 2026-11-16 | Frontend React de wheelmap.org. ⚠️ La wiki de OSM dice **GPLv3** para la web: **el archivo dice MIT**. La wiki se equivoca en la dirección opuesta que con `openrouteservice`. |
| [schemaorg/schemaorg](https://github.com/schemaorg/schemaorg) | Apache-2.0 | 6316 | 2026-11-20 | Medido en `data/schema.ttl`: `accessibilityFeature`, `accessibilitySummary` y `accessibilityHazard` tienen **`domainIncludes :CreativeWork`** — documentos y medios, **no lugares**. Para `LodgingBusiness`/`Accommodation` sólo existe `amenityFeature`, texto libre. En los **2483 archivos de `data/`** (incluido `pending`), `wheelchair` aparece **sólo dentro de texto de ejemplo**, nunca como término. |

### ⚠️ El vocabulario de la industria existe — y no tiene licencia

Esta pasada empezó dando por hecho que el estándar de distribución del vertical
no modelaba accesibilidad. **Se clonó y se midió, y el supuesto era falso.**

| Medición en [OpenTravel/OpenTravel-Specifications](https://github.com/OpenTravel/OpenTravel-Specifications) | Resultado |
|---|---|
| Tamaño | 18.817 archivos, 10.848 `.xsd`; último commit 2024-11-26 |
| Tokens | `wheelchair` ×974, `AccessibilityFeatures` ×763, `AccessibleCode` ×507, `DisabilityFeature_Enum` ×256 |
| Definición vigente | `DisabilityFeature_Enum` en OTA 2.0 **2020A** (`CodeList_4_0_0_Trim.xsd`): enumeración **abierta** de **~163 etiquetas** — *Accessible entrance*, *Bathtub grab bars*, *Elevator near accessible rooms*, *Width/diameter of wheelchair turning space in bathroom* |
| OTA 1.0 hotelero | `DisabledInd`, `AccessibilityRequirement`, `AccessibilityCode`, `DisabilityServices` en los esquemas comunes; un *Hotel Disability Project Brief* publicado desde OTA2011B |
| Archivo de licencia | **Ninguno** (los únicos `License*` son `LicensePlate`, de Ground). Coincide con lo que midió la cuarta pasada. |

Dos lecturas para cliente:

1. **El dato hotelero ya viaja con estos códigos** por canales que hablan OTA
   XML. Un agente que los ignora tira información que el hotel ya cargó.
2. **Son etiquetas, no medidas.** *"Door width in inches"* (5 de las ~163
   etiquetas nombran pulgadas) **nombra** la medida pero no tiene campo tipado
   para llevarla, y una etiqueta dice literalmente *"Americans with Disabilities
   Act (ADA) compliance"* — un criterio de un país. `a11yjson` (MIT) lleva la
   medida con unidad (`Length`, `Slope`). **Leer OpenTravel, normalizar a
   `a11yjson`** es el puente — ver Receta 20.

### Capa descartada — medida, no asumida

| Repo | Por qué no | Qué usar en su lugar |
|---|---|---|
| [AccessMap/accessmap](https://github.com/AccessMap/accessmap), [AccessMap/accessmap-webapp](https://github.com/AccessMap/accessmap-webapp) | El router accesible más citado en la literatura. **Sin archivo de licencia**; sin push desde 2023-12 y 2023-04. 27 repos en la org, la mayoría sin licencia. | `TaskarCenterAtUW/AccessMap` (GPL-3.0+, vivo) — el proyecto se mudó, no murió. |
| [OpenSidewalks/OpenSidewalks-Schema](https://github.com/OpenSidewalks/OpenSidewalks-Schema) | El esquema norteamericano de veredas accesibles: **CC BY-ND 4.0** (No-Derivatives). Se puede usar tal cual; **no se puede publicar una versión extendida.** El dato de ejemplo declara ODbL. | Consumirlo sin modificar; extensiones propias en `a11yjson`. |
| [sozialhelden/accessibility-cloud](https://github.com/sozialhelden/accessibility-cloud) | La plataforma de intercambio de dato de accesibilidad física. **Sin archivo de licencia** → todos los derechos reservados. | Consumir su API bajo sus términos; no forkear. |
| [odileeds/OTP4GB](https://github.com/odileeds/OTP4GB) | MIT, OTP para Gran Bretaña con análisis de accesibilidad. **Sin push desde 2021-11.** | Referencia de configuración, no dependencia. |

### Brechas del plano de accesibilidad, medidas el 2026-11-23

| Lo buscado | Resultado |
|---|---|
| Término de schema.org para silla de ruedas / acceso sin escalones en un lugar | **No existe** (medido sobre el TTL, ver arriba). |
| Vocabulario de habitación accesible **de la industria** con licencia OSI | **Cero.** Existe y es rico (`OpenTravel`, ver arriba), pero **sin archivo de licencia**. |
| Motor de ruteo accesible con licencia **permisiva** y vivo | **Cero.** Los dos vivos son LGPL; el MIT (`OTP4GB`) está dormido. |
| Validador de dato de accesibilidad **hotelera** | **Cero.** `gtfs-validator` cubre estaciones; para hoteles no hay nada. |

### ⚠️ Lo que esta sesión NO pudo verificar, dicho en voz alta

- `www.transportation.gov` y `www.planalto.gov.br` **no resuelven** desde la red
  de esta sesión. Las fechas del US DOT (pausa a 2027-04-30) y del Decreto
  9.296 de Brasil en `intel/market.md` vienen de **fuentes secundarias** y así
  están marcadas.
- El backend de Wheelmap: la wiki dice GPLv3, pero la misma wiki se equivocó con
  el frontend. **No se clonó** el backend; no se afirma su licencia.

## Plano de la reseña y la confianza — detección vacía, lectura congelada, procedencia viva

Agregado en la **octava pasada del 2026-11-23**. La reseña es el insumo que cada agente de esta
KB cita cuando recomienda un hotel, y hasta hoy no tenía fila de código en ningún archivo. El
plano se divide en tres capas que **no están en el mismo estado**, y la que la regulación de
2026 vuelve obligatoria es exactamente la que está vacía.

### Método de verificación de esta tabla

Igual que en las siete pasadas anteriores: existencia por `git ls-remote` (19/19 vivos),
estrellas, forks y `pushed_at` por `search/repositories`, y **licencia leída del archivo**
—probando `LICENSE`, `LICENSE.md`, `LICENSE.txt`, `LICENSE-MIT`, `LICENSE-APACHE`, `license` y
`COPYING` sobre `main` y `master`— no el badge ni el campo de la API. En este plano esa
distinción decidió el resultado: **dos repos que la API declara licenciados no tienen archivo
de licencia, y tres que la API declara con una licencia tienen dos.**

### Capa de procedencia — permisiva, viva, y resuelve el problema de al lado

| Repo | Licencia (archivo leído) | Stars | Forks | Último push |
|------|--------------------------|-------|-------|-------------|
| [contentauth/c2pa-rs](https://github.com/contentauth/c2pa-rs) | **MIT *o* Apache-2.0** (`LICENSE-MIT` 1083B + `LICENSE-APACHE`) | 454 | 208 | 2026-11-23 |
| [c2pa-org/specifications](https://github.com/c2pa-org/specifications) | **CC-BY-4.0** (18650B) | 215 | 35 | 2026-11-16 |
| [contentauth/c2patool](https://github.com/contentauth/c2patool) | Apache-2.0 | 174 | 47 | 2026-11-20 |
| [contentauth/c2pa-python](https://github.com/contentauth/c2pa-python) | Apache-2.0 | 110 | 41 | 2026-11-18 |
| [c2pa-org/conformance-public](https://github.com/c2pa-org/conformance-public) | CC-BY-4.0 | 52 | 25 | 2026-11-20 |
| [contentauth/c2pa-js](https://github.com/contentauth/c2pa-js) | MIT | 44 | 30 | 2026-11-23 |
| [contentauth/c2pa-swift](https://github.com/contentauth/c2pa-swift) | **MIT *o* Apache-2.0** (ambos presentes) | 28 | 16 | 2026-11-21 |
| [contentauth/c2pa-cpp](https://github.com/contentauth/c2pa-cpp) | **MIT *o* Apache-2.0** (ambos presentes) | 20 | 14 | 2026-11-16 |

**Lo que habilita en travel, dicho con precisión.** C2PA firma criptográficamente **medios**:
una foto o un video, con quién lo capturó y qué herramientas lo editaron. En travel eso cubre
un caso real y valioso —**la foto de la habitación**, que es la otra mitad de la confianza en
una ficha de hotel, y donde el fraude de listados es justamente lo que la Comisión Europea
puso bajo procedimiento el 21-oct-2026—. **Lo que no cubre:** el texto de una reseña escrita
por una persona en un formulario web. No hay cadena de custodia para eso. Quien venda
"procedencia de reseñas" con C2PA está vendiendo la foto y cobrando el texto.

### Capa de lectura de reseñas — 4535★ y un solo push en 2026

| Repo | Licencia (archivo leído) | Stars | Último push | Nota |
|------|--------------------------|-------|-------------|------|
| [ScalaConsultants/Aspect-Based-Sentiment-Analysis](https://github.com/ScalaConsultants/Aspect-Based-Sentiment-Analysis) | Apache-2.0 (11357B) | 585 | 2026-09-07 | **El único vivo.** Expone pesos de atención por aspecto: interpretable, auditable. |
| [songyouwei/ABSA-PyTorch](https://github.com/songyouwei/ABSA-PyTorch) | **NO HAY ARCHIVO** (API dice `MIT`) | 2112 | 2023-06-12 | **Archivado.** 516 forks. Ver trampa abajo. |
| [HSLCY/ABSA-BERT-pair](https://github.com/HSLCY/ABSA-BERT-pair) | MIT (1062B) | 519 | 2022-01-04 | NAACL-2019. Licencia limpia. |
| [howardhsu/BERT-for-RRC-ABSA](https://github.com/howardhsu/BERT-for-RRC-ABSA) | Apache-2.0 (11357B) | 461 | 2021-02-05 | Post-entrenado sobre reseñas: el más cercano al dominio, el más viejo. |
| [jiangqn/Aspect-Based-Sentiment-Analysis](https://github.com/jiangqn/Aspect-Based-Sentiment-Analysis) | MIT (1067B) | 457 | 2024-03-27 | Colección de implementaciones. |
| [lixin4ever/BERT-E2E-ABSA](https://github.com/lixin4ever/BERT-E2E-ABSA) | Apache-2.0 (11357B) | 401 | 2023-07-09 | End-to-end. |

**Por qué importa que esté congelada y no muerta.** Estos seis repos resuelven bien un problema
que no cambió: extraer aspecto y polaridad de un texto de opinión. Las licencias de cinco de
los seis son limpias y permisivas. **Lo que envejeció no es el método, es el runtime**:
dependencias de PyTorch y `transformers` de 2019-2021. Para Globant el costo real no es
reimplementar el modelo, es **actualizar el entorno** — y eso hay que presupuestarlo como tal,
no como investigación.

### Capa de detección de reseñas falsas — la medición más corta de todo el vertical

| Repo | Licencia (archivo leído) | Stars | Último push | Nota |
|------|--------------------------|-------|-------------|------|
| [SayamAlt/Fake-Reviews-Detection](https://github.com/SayamAlt/Fake-Reviews-Detection) | **NINGUNA** | 109 | 2022-04-14 | El más estrellado de la capa. Sin licencia no hay derecho de uso. |
| [kavgan/OpinRank](https://github.com/kavgan/OpinRank) | **NINGUNA** | 44 | 2021-05-28 | Corpus de reseñas de hotel (TripAdvisor) y de autos. **El único hotel-específico del plano.** |
| [TrueStarHQ/browser-extension](https://github.com/TrueStarHQ/browser-extension) | MIT (1064B) | 22 | 2025-09-03 | **El único MIT real de la capa — y está ARCHIVADO.** |
| [bretthollenbeck/fake-reviews-data](https://github.com/bretthollenbeck/fake-reviews-data) | MIT (1073B) | 12 | 2026-03-15 | Dataset etiquetado real/falsa de un paper de economía. **El único permisivo, vivo y usable. 12★.** |

**`fake review detection stars:>=20` devuelve 8 repos en todo GitHub**, y uno de los 8 es un
repo de robótica escolar que entra por la sigla `FTC`. Esa es la totalidad del piso abierto para
una obligación que en 2026 es vinculante en Italia, EE.UU. y China.

### ⚠️ La trampa inversa: cuando GitHub **afirma** una licencia que no existe

Esta KB registró tres casos de `NOASSERTION` ocultando una licencia permisiva real
(`valhalla`, `odoo`, `airportsdata`). `songyouwei/ABSA-PyTorch` es el caso contrario:

| Comprobación | Resultado |
|--------------|-----------|
| `LICENSE`, `LICENSE.md`, `LICENSE.txt`, `COPYING` en `master` | **404 los cuatro** |
| Rama default | `refs/heads/master` (confirmada por `git ls-remote --symref`) |
| Rastro de licencia en `README.md` | Un badge: `img.shields.io/packagist/l/doctrine/orm.svg` → **la licencia de Doctrine ORM, un paquete PHP ajeno al repo** |
| `license.spdx_id` en la API de GitHub | `MIT` |
| Estado | **Archivado**, 2112★, **516 forks** |

**La regla:** leer el archivo no es solo el remedio para `NOASSERTION`. **Una licencia afirmada
por la API también hay que abrirla**, porque el error existe en las dos direcciones y la segunda
es la cara: en la primera se descarta algo usable, en la segunda se construye sobre un permiso
que nadie otorgó. Con 516 forks, esa afirmación ya se replicó 516 veces.

### ⚠️ Dual licensing que la API no muestra

`c2pa-rs`, `c2pa-swift` y `c2pa-cpp` traen **`LICENSE-MIT` y `LICENSE-APACHE` los dos**. La API
devuelve `NOASSERTION` para el primero y solo `Apache-2.0` para los otros dos. El efecto
práctico no es cosmético: **el proyecto concede elegir y la API esconde la opción.** Si el
contrato de un cliente excluye Apache-2.0 por la cláusula de patentes, leer el badge habría
descartado un stack que sí se podía tomar bajo MIT. Casos 4, 5 y 6 del registro de divergencia
badge-vs-archivo de esta KB.

### Brechas del plano de la reseña, medidas el 2026-11-23

| Consulta (`search/repositories`) | Resultado | Lectura |
|----------------------------------|-----------|---------|
| `fake review detection stars:>=20` | **8** (uno es robótica por la sigla FTC) | El piso de la obligación regulatoria de 2026. |
| `review authenticity provenance stars:>=50` | **0** | Nadie cruzó procedencia con reseñas. El puente hay que construirlo. |
| `review moderation trust safety stars:>=200` | **0** | Sin infraestructura abierta de moderación a ninguna escala. |
| `hotel review analysis stars:>=30` | **1** (`Tony607/Chinese_sentiment_analysis`, sin licencia, 2017) | El vertical más dependiente de la reseña no tiene herramienta propia. |
| `review dataset hotel tripadvisor stars:>=30` | **1** (`OpinRank`, sin licencia) | **No hay corpus de reseñas de hotel redistribuible.** Quien entrene, entrena con dato propio del cliente. |
| `reputation management open source stars:>=100` | **0** | La gestión de reputación —producto que el vertical compra cerrado— no tiene equivalente abierto. |
| `tours activities booking open source stars:>=50` | **0** | Registrado al pasar: el tercer segmento de travel tampoco tiene piso. Candidato a plano futuro. |

**La conclusión de arquitectura.** En este plano no hay nada que adoptar: hay algo que
**construir sobre dos piezas sanas y un dataset de 12★**. `ScalaConsultants/ABSA` (Apache-2.0,
vivo) para leer, el org de C2PA (MIT *o* Apache, vivo) para la procedencia de la foto, y el
dato de reseñas del propio cliente —porque corpus redistribuible no hay—. Todo lo que diga
"detectar reseñas falsas" con licencia utilizable **hay que escribirlo**. Recetas 22 a 24 en
`compose/patterns.md`.

### ⚠️ Lo que esta sesión NO pudo verificar, dicho en voz alta

- `ec.europa.eu` y `www.tripadvisor.com` **no resuelven** desde la red de esta sesión. El
  procedimiento DSA contra Booking.com (21-oct-2026) y las cifras del Transparency Report de
  Tripadvisor están **corroboradas por múltiples fuentes secundarias coincidentes** (incluida
  la página de noticias de `digital-strategy.ec.europa.eu` citada en los resultados, CNBC,
  Phocuswire y Lodging Magazine), pero **no leídas del documento primario**. Se marcan así.
- La **ventana de prueba de estadía** de la ley italiana aparece como **15 días** en el
  borrador de ene-2025 y como **30 días** en coberturas posteriores. **No se pudo leer el texto
  final de la Ley 34/2026**: se registran las dos cifras y ninguna se afirma.
- Las guías de aplicación de AGCM/Agcom para esa ley estaban **pendientes** en las fuentes
  consultadas (consulta pública con comentarios al 15-jul). No se pudo confirmar si se
  emitieron.

## Plano del equipaje — el hallazgo está dentro de un repo que no dice "equipaje"

Noveno plano. Medido el 2026-11-23. **El resultado invierte la conclusión con la que empecé.**

### Método de verificación de esta tabla

Existencia por `git ls-remote` (21/21 vivos). Métricas por `search/repositories` con
`repo:owner/name`. **Licencia leída del archivo**, byte a byte, por `raw.githubusercontent.com`.
Y en el caso central, **el repo se clonó y se leyó el código**: la descripción no alcanzaba.

> ⚠️ **Defecto de método encontrado y corregido en esta pasada.** `gh api repos/<owner>/<name>`
> devuelve **403** para repos fuera del scope de la sesión, mientras `gh api search/repositories`
> funciona. Peor: mi primer script probaba `[ -n "$code" ]` sobre la salida, y el **JSON de
> error** no está vacío — así que imprimió `FOUND` para seis archivos de licencia que **no
> existen**. Si esta KB hubiera salido con esa tanda, habría afirmado licencias inexistentes en
> cinco repos. **Un chequeo de existencia que no distingue "respuesta" de "respuesta afirmativa"
> no es un chequeo.** La vía correcta: `curl -o archivo -w '%{http_code}'` y comparar con `200`.

### Capa de mensajería — el hallazgo del plano

| Repo | Licencia (archivo leído) | Stars | Forks | Creado | Último push | Qué es |
|------|--------------------------|-------|-------|--------|-------------|--------|
| [adamf/jetway](https://github.com/adamf/jetway) | **MIT** (`LICENSE`, 1070B, "Copyright (c) 2026 Adam Fletcher") | 17 | 5 | 2026-08-29 | **2026-11-23** | Gateway de mensajería de reservas de aerolínea y GDS en Go. **72.163 líneas.** v0.1.109 |
| [adamf/wholesky](https://github.com/adamf/wholesky) | **MIT** (`LICENSE`, 1070B) | 4 | 0 | 2026-08-31 | **2026-11-23** | Un día-Tierra de aviación de pasajeros simulado sobre Jetway. Es el **plan de pruebas** del anterior |

**17 estrellas, y es lo más importante que esta KB midió en nueve planos de este vertical.**
Lo que `jetway` habla, leído de `README.md` y de `docs/protocols.md` del clon:

- **Type B / AIRIMP** — el formato teletipo que llevan las redes store-and-forward de SITA y
  ARINC (`pkg/typeb`).
- **UN/EDIFACT / PADIS** — interchanges ISO 9735 con mensajes IATA `PAOREQ`/`PAORES`, y emite y
  consume `CONTRL` (`pkg/padis`, con `pnrgov.go`, `ticket.go`, `divide.go`).
- **NDC** — mensajes de orden IATA sobre HTTP, mapeados al mismo almacén de registros.
- Y además: `pkg/dcs` (departure control: aceptación, asientos, carga), `pkg/mct` (minimum
  connect time), `pkg/prorate`, `pkg/acars`, `pkg/ssim`, `pkg/rescode`, `pkg/avs`.

#### `pkg/baggage` — lo que ninguna búsqueda por "baggage" encuentra

656 líneas en cuatro archivos. **Es la capa de equipaje que esta KB iba a declarar inexistente.**

| Elemento | Qué implementa | Dónde |
|----------|----------------|-------|
| `KindBSM` | **Baggage Source Message** — el mensaje que declara las piezas de un pasajero y su ruta | `pkg/baggage/baggage.go` |
| `KindBPM` | **Baggage Processed Message** — el mensaje de un evento sobre una pieza ya en el sistema | `pkg/baggage/baggage.go` |
| `KindBUM` | **Baggage Unaccompanied Message** — la pieza que viaja sin su pasajero | `pkg/baggage/baggage.go` |
| `Tag{Number, Count}` | La **etiqueta**: el identificador de la pieza física | `pkg/baggage/baggage.go` |
| `FlightLeg` (`Outbound`/`Onward`/`Inbound`) | Los tramos sobre los que la pieza debe viajar | `pkg/baggage/baggage.go` |
| `Build()` / `Parse()` / `IsBaggage()` | Construir, parsear y **clasificar** un mensaje de equipaje | `pkg/baggage/baggage.go` |
| `Station.BSMFor()` | Construye el BSM de un pasajero desde el estado real del vuelo | `pkg/dcs/dcs.go:1086` |
| `Station.ApplyBagReport()` | Aplica un mensaje de equipaje entrante al vuelo | `pkg/dcs/dcs.go:1127` |
| `KindAHL` / `KindOHD` / `KindFWD` | **El sistema de tracing**: expediente de pieza demorada (AHL), de pieza en mano sin dueño (OHD) y de reenvío (FWD), **emparejados por número de etiqueta** | `pkg/baggage/tracing.go` |
| `TracingFile{ColourType, Routing, Contact, Matches, ForwardTo}` | Los elementos de emparejamiento: códigos IATA de color/tipo (`BK22` = negro, rígido vertical), ruta, contacto | `pkg/baggage/tracing.go` |

Y en `pkg/gateway/decode.go:68` el gateway distingue explícitamente el caso:

> *"Baggage is set when the message is a BSM or BPM: about a bag, not a [passenger]"*

cuando no puede decodificar un mensaje de equipaje, **lo conserva** y emite
`unreadable_bag_message` con severidad `warn` (`decode.go:481`) en lugar de descartarlo.

#### La honestidad epistémica del repo, citada porque es el estándar de esta KB encontrado en el mundo

El comentario de cabecera de `pkg/baggage/tracing.go` dice, sobre los formatos de los
expedientes de rastreo:

> *"This is the shape of the industry's tracing system as its published training material
> describes it — the file kinds, the element codes NM, TN, CT, RT, FD, FL, TX — laid out here as
> the dotted element lines the rest of the bag messages use. **The vendor's own record formats
> were not available, so this is this package's profile, and it says so.**"*

Es exactamente la regla de "lo que esta sesión NO pudo verificar, dicho en voz alta" que esta KB
aplica a sí misma, escrita por el autor de la librería dentro del código. **Tratar ese perfil
como el formato del proveedor sería el error; el repo ya avisa que no lo es.**

#### Lo que esto cambia para un engagement

Antes de esta medición, la respuesta a *"¿se puede construir la cadena de custodia de una maleta
con software permisivo?"* era **no**. Ahora es: **sí, desde un repo MIT de 72k líneas con 5 forks
y push del mismo día** — con tres salvedades que hay que decir en la primera reunión:

1. **Es pre-1.0 y lo dice.** Su `CHANGELOG.md` abre con *"Jetway is pre-1.0: the API moves when
   the evidence says it should"*. 17★ y 5 forks: **no hay comunidad todavía**. Riesgo de un solo
   mantenedor, explícito.
2. **El perfil de tracing es del paquete, no del proveedor** (ver cita arriba).
3. **No tiene superficie agentic.** `grep -ril 'mcp|agentic|tool_call'` sobre todo el árbol
   devuelve **cero**. El agente se compone encima; no viene incluido. Es la Receta 25.

### Capa EDIFACT genérica — permisiva, viva y la que no hay que reimplementar

PADIS es EDIFACT. La capa de parseo genérica está **sana**, al contrario que la capa
aeronáutica específica, y eso parte el trabajo en dos: el sobre es commodity, el mensaje no.

| Repo | Licencia (archivo leído) | Stars | Forks | Último push | Para qué |
|------|--------------------------|-------|-------|-------------|----------|
| [jf-tech/omniparser](https://github.com/jf-tech/omniparser) | **MIT** (1070B) | 1085 | 82 | 2026-10-11 | Parser/transformador ETL en streaming, Go. EDI/EDIFACT/X12 entre sus formatos. El más estrellado de la capa |
| [indice-co/EDI.Net](https://github.com/indice-co/EDI.Net) | **MIT** (1074B) | 491 | 172 | 2025-12-01 | Serializador/deserializador .NET de EDIFACT, X12 y TRADACOMS. **172 forks**: la más integrada |
| [michaelachrisco/Electronic-Interchange-Github-Resources](https://github.com/michaelachrisco/Electronic-Interchange-Github-Resources) | **MIT** (1072B) | 353 | 58 | 2026-11-19 | Índice curado de recursos EDI. Punto de partida para buscar un dialecto concreto |
| [nerdocs/pydifact](https://github.com/nerdocs/pydifact) | **MIT** (1081B) | 191 | 54 | **2026-11-23** | Librería EDIFACT en Python. **Push el día de este ciclo.** La vía corta si el stack es Python |
| [php-edifact/edifact](https://github.com/php-edifact/edifact) | **LGPL-3.0** (7632B) | 289 | 89 | 2025-10-30 | Procesamiento EDIFACT en PHP. **Copyleft débil**: se enlaza, no se embebe modificado sin publicar |

> ⚠️ **Medición que tuve que descartar, dicha porque casi entró a esta tabla.** La consulta
> `pyedifact OR edifact parser stars:>=20` devolvió **13.494 resultados** encabezados por
> `Graphify-Labs/graphify` (152k★), `moment/moment` (47k★) y `markedjs/marked` — ninguno tiene
> nada que ver con EDI. **La búsqueda de GitHub no trata `OR` como un operador ahí**: degradó la
> consulta a "parser". La medición válida es `edifact stars:>=30` → **25 repos**. Un total de
> cinco cifras en un plano estrecho es síntoma de consulta rota, no de abundancia.

### Capa de decodificación de mensajería operativa

| Repo | Licencia (archivo leído) | Stars | Forks | Último push | Para qué |
|------|--------------------------|-------|-------|-------------|----------|
| [szpajder/libacars](https://github.com/szpajder/libacars) | **MIT** (`LICENSE.md`, 1076B) | 156 | 33 | 2026-11-22 | Decodifica payloads ACARS. Entra por primera vez: complementa el plano de vuelo en curso con el **canal** por el que esos mensajes llegan |
| [szpajder/dumpvdl2](https://github.com/szpajder/dumpvdl2) | **GPL-3.0** | 263 | 36 | 2026-10-20 | Decodificador VDL Mode 2 del mismo autor. **Copyleft fuerte**: herramienta, no componente de producto |

### Capa de norma y de prueba formal — viva, y sin licencia

| Repo | Licencia | Stars | Creado | Último push | Qué es y por qué no se puede usar |
|------|----------|-------|--------|-------------|-----------------------------------|
| [Lex-van-Os/Beltline](https://github.com/Lex-van-Os/Beltline) | **NO HAY ARCHIVO** en `LICENSE`/`.md`/`.txt`/`COPYING`/`LICENCE` | 0 | 2026-10-21 | 2026-11-18 | Simulación de rastreo de equipaje dirigida por eventos en .NET 10, **explícitamente basada en la Resolución 753 de IATA**. **El único repo en todo GitHub que nombra la norma** — y sin licencia es inusable en un entregable |
| [samdengler/verified-air](https://github.com/samdengler/verified-air) | **NO HAY ARCHIVO** | 1 | 2026-10-24 | 2026-11-10 | Prueba de concepto de reglas de oferta y orden de aerolínea **en Lean, con demostraciones**. Intelectualmente el repo más interesante del plano; contractualmente inservible |
| [OpenTravel/OTM-DE](https://github.com/OpenTravel/OTM-DE) | **NO HAY ARCHIVO** | 22 | 2014-06-10 | **2020-11-23** | Entorno de desarrollo de modelos OpenTravel. Su propia descripción dice *"Maintenance Release ONLY"*. **Seis años sin push**: histórico, no base |

**Tres repos vivos y relevantes, tres sin archivo de licencia.** Es el cuarto plano de esta KB
donde la pieza más cercana al problema es la que no se puede usar. La regla de esta KB se
sostiene sin excepción: **la licencia es el archivo y solo el archivo.**

### Capa de rastreo del lado del pasajero — abundante, y del lado equivocado

| Repo | Licencia (archivo leído) | Stars | Forks | Último push | Qué es |
|------|--------------------------|-------|-------|-------------|--------|
| [seemoo-lab/openhaystack](https://github.com/seemoo-lab/openhaystack) | **AGPL-3.0** (32387B) | 14264 | 719 | 2026-08-17 | Framework para construir "AirTags" propios y rastrear dispositivos Bluetooth por la red Find My de Apple |
| [hybridgroup/go-haystack](https://github.com/hybridgroup/go-haystack) | **MIT** (1071B) | 1546 | 50 | 2026-10-13 | Rastreo por Find My en Go, sobre OpenHaystack. **MIT: es el único de la capa que se puede embeber** |
| [AxelUser/carry-fit](https://github.com/AxelUser/carry-fit) | **MIT** (1072B) | 58 | 5 | 2026-05-29 | Verificador de cumplimiento de medidas de equipaje de mano por aerolínea |

#### La ley estructural, medida ahora en dos verticales independientes

El ciclo 9 de **retail** midió que los únicos rastreadores de paquetes con ≥100★ son
**aplicaciones de consumidor** (`itsvic-dev/deliveries` 258★ GPL-3, `proninyaroslav/libretrack`
371★ GPL-3) y que del lado del comerciante no hay nada: *el rastreo que existe es para la persona
que espera el objeto, no para el operador que responde dónde está*.

**En travel la misma ley se vuelve a medir, con cifras propias y sin reutilizar ninguna fuente:**

| Lado | Lo que existe | Estrellas |
|------|---------------|-----------|
| El pasajero que espera su maleta | `openhaystack` + `go-haystack` | **15.810★ combinadas** |
| El operador que debe responder dónde está | `baggage tracking stars:>=5` → 2 repos muertos sin licencia | **11★ combinadas, cero mantenidas** |

**Tres órdenes de magnitud de diferencia.** Y la asimetría no es de interés: es de **incentivo**.
El rastreo de consumidor resuelve *mi* objeto y lo paga quien lo pierde. La custodia de operador
resuelve *la obligación de un tercero* y **genera responsabilidad legal** (ver el límite de
Montreal en `intel/market.md`). Igual que en retail *"el ruteo es un problema y la promesa es un
compromiso"*: **el rastreo es una comodidad y la custodia es un pasivo**, y el open source
produce comodidades, no pasivos. `jetway` es la excepción que confirma la regla — un solo repo,
un solo mantenedor, pre-1.0.

### Capa descartada — medida, no asumida

| Repo | Estrellas | Por qué se descarta |
|------|-----------|---------------------|
| [w3c/baggage](https://github.com/w3c/baggage) | 62 | **No es de viajes.** Especificación W3C de propagación de contexto en *distributed tracing*. Ver `agents/top.md` → la cuarta colisión |
| [bchhaglani/Baggage-tracking](https://github.com/bchhaglani/Baggage-tracking) | 6 | Sin licencia. Último push **2019-03-21**. Proyecto académico de RFID/IoT |
| [ParameswarKanuparthi/Baggage-Tracking-using-IoT](https://github.com/ParameswarKanuparthi/Baggage-Tracking-using-IoT) | 5 | Sin licencia. Último push **2020-05-31** |

#### ⚠️ `w3c/baggage`: séptimo caso de dual licensing que la API no muestra — y el primero partido por tipo de artefacto

La API de GitHub devuelve `NOASSERTION`. El archivo `LICENSE.md` (341B) dice, textual:

> *"All Reports in this Repository are licensed by contributors under the **W3C Software and
> Document License**. All tests in this Repository are licensed by contributors to be distributed
> under the **W3C 3-clause BSD License**."*

**Dos licencias en un repo, y el límite entre ellas no es por directorio: es por qué tipo de cosa
es el archivo.** Los casos 4, 5 y 6 de esta KB (`c2pa-rs`, `c2pa-swift`, `c2pa-cpp`) eran
*MIT **o** Apache-2.0* a elección del usuario. Este es distinto: **no hay elección**, hay
clasificación — el texto normativo va por una licencia y los tests por otra. Y suma al eje que el
ciclo 9 de retail abrió: **la licencia de una especificación es una licencia de documentación**
(allí `beckn/protocol-specifications` CC BY-NC-SA, `ONDC-Protocol-Specs` CC BY-ND). Aquí el
documento del W3C y sus tests **no comparten licencia**. Un `pip`/`go get` que copie el repo
entero a un entregable mezcla dos regímenes en un mismo árbol.

### Brechas del plano del equipaje, medidas el 2026-11-23

- **No hay implementación abierta de la etiqueta de equipaje** (`bag tag IATA` → 0 repos). El
  documento que identifica la pieza física no tiene una sola librería.
- **No hay cliente abierto de WorldTracer** — el sistema que la industria usa de hecho para
  emparejar expedientes de equipaje extraviado entre aerolíneas. Los 4 repos que lo nombran suman
  0★. `jetway/pkg/baggage/tracing.go` implementa **el perfil del paquete**, no el del proveedor,
  y lo declara.
- **No hay software abierto de operación aeroportuaria** (`airport operations stars:>=20` → 0):
  ni AODB, ni A-CDM, ni gestión de cinta.
- **No hay capa abierta de RFID** (`rfid asset tracking stars:>=50` → 0) **contra una obligación
  regulatoria vigente en China** (ver APAC en `intel/market.md`). Es la contradicción más fuerte
  del plano: hay mandato y no hay código.
- **No hay un solo agente de operación aérea con ≥10★** (`airline operations agent` → 0). Toda la
  capa agentic medida en este vertical está del lado de **buscar y reservar**, ninguna del lado de
  **operar y responder**.
- **Fuera de `jetway`, no hay segunda implementación de BSM/BPM.** Un solo repo, un mantenedor,
  pre-1.0, 5 forks. Es una dependencia de proveedor único con forma de open source.

### ⚠️ Lo que esta sesión NO pudo verificar, dicho en voz alta

- **`transportation.gov` no resuelve desde esta red**, ni `www.federalregister.gov`, ni
  `media.asianaviation.com`. Por eso **las cifras del reglamento de reembolso del DOT y del
  informe SITA 2026 van marcadas como secundarias coincidentes** en `intel/market.md`, nunca como
  leídas del primario. Hay una fuente que afirma un umbral de **6 horas** contra las 12 que dicen
  todas las demás: **se registran las dos y no se afirma ninguna**.
- **No se leyó el texto de la Resolución 753** (es documento de pago de IATA). Los cuatro puntos
  de custodia y el hecho de que **no obliga tecnología** vienen de material secundario
  concordante, incluido el `docs/` de `jetway`.
- **El PDF del informe SITA 2026 no se pudo abrir.** Una fuente describe una cifra de 3,4 por mil
  con alza del 9% que no concuerda con el 4,9 y la baja del 23% de las demás; **lo más probable es
  que sea la cifra de APAC (3,41) leída como global**, pero no se pudo confirmar y queda anotado
  como discrepancia abierta.
- **No examinado en esta pasada, y se dice:** carga aérea (distinta del equipaje), equipaje
  ferroviario, África más allá de la cifra de SITA, y los sistemas de los aeropuertos de Japón y
  Singapur más allá de material secundario.

## Plano del precio — la ley estructural de este KB, en su forma más extrema

Décimo plano, 2026-11-23. Los nueve anteriores encontraron variantes de la misma ley: lo permisivo
está en la infraestructura horizontal, lo copyleft o lo ausente está en el vertical. **Acá la
distancia es la mayor medida hasta ahora**, y se puede poner en dos números: la capa horizontal de
optimización suma **más de 20.000 estrellas bajo Apache-2.0 y MIT**; la única biblioteca de revenue
management de viajes real y permisiva tiene **2**.

### Método de verificación de este plano

1. Existencia: `git ls-remote` sobre cada slug (13 probados, 12 vivos; el único muerto,
   `pymc-devs/pymc-marketing`, era **mi propio error de owner** — es `pymc-labs`, y se corrigió).
2. Estrellas, `pushed_at`, `created_at` y forks: `search/repositories` con `q=repo:<slug>`.
3. **Licencia leyendo el archivo**, no el badge ni el campo de la API: `curl` de
   `LICENSE`, `LICENSE.md`, `LICENSE.txt` y `COPYING` en `main` y en `master`, y se registró la
   primera línea literal. Los `api_license: None` se confirmaron como **ausencia de archivo**, no
   como fallo de la API.

### Capa horizontal — permisiva, viva, enorme, y no sabe nada de viajes

| Repo | Licencia (leída) | Stars | Último push | Para qué sirve en este plano |
| --- | --- | --- | --- | --- |
| [google/or-tools](https://github.com/google/or-tools) | Apache-2.0 (`main/LICENSE`) | 14.433 | 2026-11-23 | El solver. Bid prices de red, asignación de inventario, control de *booking limits* como programa lineal. |
| [Nixtla/statsforecast](https://github.com/Nixtla/statsforecast) | Apache-2.0 (`main/LICENSE`) | 4.984 | 2026-11-19 | Pronóstico de demanda estadístico y rápido: el insumo real de cualquier EMSR (media y desvío por clase tarifaria). |
| [pymc-labs/pymc-marketing](https://github.com/pymc-labs/pymc-marketing) | Apache-2.0 (`main/LICENSE`) | 1.314 | 2026-11-23 | Elasticidad de precio bayesiana con intervalos de credibilidad. La pieza que permite **decir cuánta incertidumbre tiene el precio**, que es lo que un regulador pregunta. |
| [facebook/prophet](https://github.com/facebook/prophet) | MIT (`main/LICENSE`, «Copyright (c) Facebook, Inc. and its affiliates») | **no medido** | **no medido** | Pronóstico con estacionalidad y feriados — la estacionalidad múltiple del viaje. Ver la nota de honestidad abajo. |

> **Nota de honestidad sobre `prophet`:** `git ls-remote` lo da **vivo**, y su `LICENSE` se leyó byte
> a byte (MIT). Pero `search/repositories` con `q=repo:facebook/prophet` devolvió **cero hits** en
> esta sesión, así que **no tengo estrellas ni fecha de push medidas** y no las invento. Es el mismo
> tipo de hueco que el noveno plano declaró con los PDFs de SITA: se dice que no se midió.

### Capa vertical permisiva — existe, es una sola, y es buena

| Repo | Licencia (leída) | Stars | Creado | Último push | Qué trae |
| --- | --- | --- | --- | --- | --- |
| [arikanatakan/revmng](https://github.com/arikanatakan/revmng) | **MIT** (`main/LICENSE`) | **2** | 2026-06-16 | 2026-06-17 | Littlewood, EMSR-a, EMSR-b, **DP exacto**, overbooking (por nivel de servicio o por costo), newsvendor, precio óptimo con demanda lineal o de elasticidad constante, bid prices de red, grupos por análisis de desplazamiento, length-of-stay, y las métricas (RevPAR, yield, load factor, ROM). |

**Las tres propiedades de `revmng` que importan más que sus 2 estrellas**, todas leídas del README y
del código, no del marketing:

1. **El core no tiene dependencias de terceros.** Para una entrega de cliente, eso es la diferencia
   entre embeber y negociar.
2. **Cada resultado lleva procedencia: versión de la biblioteca, *hash* de las entradas y
   *timestamp*, con `to_dict()` serializable a JSON.** Esto no es una comodidad de logging: **es
   exactamente el artefacto de auditoría que el plano regulatorio pide**, y no conozco otra
   biblioteca del vertical que lo emita de fábrica.
3. **Validada contra ejemplos publicados** y con CI. Está en PyPI (`pip install revmng`).

**La propiedad que importa más que las tres juntas, y es de arquitectura:** `revmng` calcula el
precio a partir de **tarifas, demanda, capacidad, no-shows y costos**. No toma ni un atributo de la
persona. Un stack construido sobre él tiene una respuesta estructural —no documental— a la pregunta
del § 349-a de Nueva York, cuyo disparador es *un algoritmo que usa el dato personal del consumidor*.
Elegir RM por capacidad en lugar de precio personalizado **es una postura de cumplimiento**, no sólo
una decisión de modelado. Receta 28.

### Capa de dato competitivo — chica, permisiva y viva

El insumo que el *skill* de Asgard llama «precio de competencia» y sin el cual su «IRON LAW» no se
cumple:

| Repo | Licencia (leída) | Stars | Último push | Qué hace |
| --- | --- | --- | --- | --- |
| [seanbabalala/hotelrate-crawl](https://github.com/seanbabalala/hotelrate-crawl) | MIT (`main/LICENSE`) | 14 | 2026-04-28 | Crawl de tarifas hoteleras. |
| [borzelo/hotel-price-aggregator](https://github.com/borzelo/hotel-price-aggregator) | MIT (`main/LICENSE`) | 11 | 2026-06-04 | Agregación de precio hotelero multi-fuente. |

> ⚠️ **Lo que ninguno de los dos resuelve, y hay que decirlo antes de proponerlo:** *rate shopping*
> por crawling tiene un problema de términos de servicio del lado de la fuente, y en China —tras la
> decisión de SAMR sobre Trip.com— un problema adicional: **el registro de paridad puede ser prueba
> de la conducta, no sólo insumo del precio.** Son útiles como referencia de esquema; el dato de
> producción se compra.

### Capa de simulación — MIT, académica, dormida

| Repo | Licencia (leída) | Stars | Último push | Nota |
| --- | --- | --- | --- | --- |
| [hpi-epic/pricewars](https://github.com/hpi-epic/pricewars) | MIT (`master/LICENSE.md`) | 56 | **2018-10-16** | Plataforma de simulación de competencia de precios del Hasso-Plattner-Institut. **Dormida ~8 años**: sirve para entender la dinámica de competencia algorítmica (el riesgo de colusión implícita que el PL 1635/2024 brasileño quiere tipificar), no como dependencia. |
| [ashenclock/airline-revenue-management-lab](https://github.com/ashenclock/airline-revenue-management-lab) | MIT (`main/LICENSE`, «Copyright (c) 2025 Antonio») | 0 | 2026-10-23 | Laboratorio de RM aéreo. 0★ pero **con licencia y con push reciente**, a diferencia de los cinco de abajo. |

### ⚠️ La auditoría de licencia de este plano — cinco de ocho repos de RM de viajes son inusables

Esta es la medición más decisiva de la pasada para un estudio que tiene que entregar código a un
cliente. De los **ocho** repos de revenue management específicos de viajes que encontré, **cinco no
tienen archivo de licencia en absoluto** — lo que en derecho de autor significa *todos los derechos
reservados*, no «open source sin especificar»:

| Repo | Stars | Último push | Archivo de licencia | Veredicto |
| --- | --- | --- | --- | --- |
| [jdautell/hotel-revenue-management-engine](https://github.com/jdautell/hotel-revenue-management-engine) | 0 | 2026-09-11 | **ninguno** | Inusable. EMSR-b + modelo de cancelación XGBoost (AUC 0,84) + Streamlit, README en español — y no se puede tocar. |
| [normanlrasmussen/airline-revenue-optimizer](https://github.com/normanlrasmussen/airline-revenue-optimizer) | 0 | 2026-09-17 | **ninguno** | Inusable. Compara Open Sales, EMSR-b y DP sobre el mismo flujo simulado, con tests. |
| [shashank0208/airline_revenue_management](https://github.com/shashank0208/airline_revenue_management) | 0 | 2026-10-26 | **ninguno** | Inusable. FCFS vs EMSR-b vs LP con demanda ARIMA y Monte Carlo. |
| [Naresh1401/hotel-revenue-management](https://github.com/Naresh1401/hotel-revenue-management) | 0 | 2026-10-11 | **ninguno** | Inusable. Elasticidad log-log, LightGBM, optimizador de RevPAR. |
| [adhikariprajitraj/AirLine-Revenue-Managment-OR](https://github.com/adhikariprajitraj/AirLine-Revenue-Managment-OR) | 1 | **2025-06-06** | **ninguno** | Inusable y dormido. DAVN + EMSR-b en red; acompaña un tutorial en SSRN. |
| [tule2236/Airbnb-Dynamic-Pricing-Optimization](https://github.com/tule2236/Airbnb-Dynamic-Pricing-Optimization) | **243** | **2018-11-14** | **ninguno** | **El repo de precio de viajes más estrellado que existe, y no se puede usar.** |
| [DallasBuyer/awesome-dynamic-pricing](https://github.com/DallasBuyer/awesome-dynamic-pricing) | 127 | 2022-10-27 | **ninguno** | La lista de referencia del campo tampoco tiene licencia. |

**La conclusión operativa, sin vueltas:** salvo `revmng` y
`ashenclock/airline-revenue-management-lab`, **el revenue management de viajes en GitHub es código
de portfolio sin licencia**. Lo que parece una biblioteca es un trabajo práctico. Para Globant eso
significa que en este plano **no hay nada que forkear**: hay una biblioteca MIT de 2 estrellas para
embeber y una capa horizontal enorme para construir encima. Lo demás se lee y se descarta.

### Brechas del plano del precio, medidas el 2026-11-23

| Brecha | Evidencia | Consecuencia |
| --- | --- | --- |
| **No existe capa de divulgación de precio** | `price explanation transparency algorithm` → 0 repos; `algorithmic pricing disclosure` → 1 y es de otro tema | Hay que escribirla. Es la Receta 29 y es el hueco de producto más claro del plano. |
| No hay plataforma vertical de RM open source | Ver `verticals/solutions.md` | El motor se compra (IDeaS, Duetto, Fetcherr, Atomize) o se arma con `revmng` + horizontal. |
| La única pieza del vertical tiene 5 meses sin commit | `revmng`/`revmng-mcp`, push 2026-06-17 | Fijar versión; presupuestar mantenimiento propio. |
| `prophet` no pudo medirse por la API de búsqueda | `q=repo:facebook/prophet` → 0 hits | Declarado, no estimado. |
| El dato competitivo abierto no es contractualmente limpio | `hotelrate-crawl`, `hotel-price-aggregator` (MIT, crawling) | El código sirve; el dato de producción se compra. |
| Ningún repo del plano implementa paridad **como control auditable** | Sólo monitorización (vía API ajena) | Tras SAMR/Trip.com es una brecha con exposición regulatoria, no sólo técnica. |

## Plano del comprobante — la primera vez que la capa horizontal está *certificada* y no sólo grande

**Undécima pasada, 2026-11-23.** En los diez planos anteriores la ley estructural de esta KB fue
siempre la misma: horizontal grande y permisiva, vertical chica o inexistente. Acá vuelve a
cumplirse —pero con una diferencia que la hace más fuerte: **la capa horizontal de este plano no es
sólo grande, es la que el regulador reconoce.** Las reglas de validación EN 16931 que publica la
Comisión Europea son el artefacto normativo, no una reimplementación de alguien.

### Método de verificación de este plano

- Liveness: `git ls-remote` sobre los **36 repos nuevos** de esta pasada → **36 vivos, 0 muertos**.
- Licencia: `curl` de `LICENSE`/`LICENSE.md`/`LICENSE.txt`/`COPYING` en `main` **y** `master`, y
  **lectura del texto**, no del campo `license` de la API — que en este plano falló cinco veces.
- Estrellas y último push: `search/repositories`, 2026-11-23.

### Capa horizontal — permisiva, viva, enorme, y no sabe nada de viajes

| Repo | Licencia (archivo leído) | Stars | Último push | Qué aporta |
| --- | --- | --- | --- | --- |
| [ZUGFeRD/mustangproject](https://github.com/ZUGFeRD/mustangproject) | Apache-2.0 (`master/LICENSE`) | 497 | **2026-11-23** | **La pieza de referencia del plano.** Biblioteca Java + validador + CLI de Factur-X/ZUGFeRD, UN/CEFACT CII y XRechnung. Push de hoy |
| [wmixvideo/nfe](https://github.com/wmixvideo/nfe) | Apache-2.0 (`master/LICENSE`) | **770** | **2026-11-23** | **El repo más estrellado de todo el plano, y es brasileño.** NF-e en Java, push de hoy |
| [ConnectingEurope/eInvoicing-EN16931](https://github.com/ConnectingEurope/eInvoicing-EN16931) | **EUPL-1.2** (`master/LICENSE.txt`) | 271 | 2026-10-26 | Los **artefactos oficiales de validación** del estándar europeo. Es la norma, no una interpretación. ⚠️ Copyleft recíproco — ver la auditoría abajo |
| [phax/phive-rules](https://github.com/phax/phive-rules) | Apache-2.0 (`master/LICENSE`) | 55 | **2026-11-23** | Reglas de validación de e-invoice **de muchos países** para el motor phive. La capa multi-jurisdicción que no hay que reimplementar |
| [atgp/factur-x](https://github.com/atgp/factur-x) | MIT (texto leído, `master/LICENSE`) | 154 | 2026-08-18 | Factur-X / ZUGFeRD 2.0 en PHP: incrusta y extrae el XML del PDF |
| [TadaSoftware/PyNFe](https://github.com/TadaSoftware/PyNFe) | **LGPL-3.0** | 599 | 2026-02-20 | NF-e en Python. La API dice `NOASSERTION`; el archivo dice LGPL-3.0 — copyleft débil, usable enlazando |
| [bsnsoft/esj](https://github.com/bsnsoft/esj) | Apache-2.0 | 4 | **2026-11-22** | EN 16931 **como JSON por paths** en vez de XML. 4★, pero es la forma en que un agente quiere leer una factura |
| [backoffice-plus/e-invoice-validator](https://github.com/backoffice-plus/e-invoice-validator) | Apache-2.0 | 21 | 2026-10-20 | Validador alemán de E-Rechnung, para usar como gate |
| [Quittio/quittio](https://github.com/Quittio/quittio) | MIT (`master/LICENSE`; **404 en `main`**) | 47 | 2026-11-20 | ZUGFeRD/Factur-X/XRechnung en PHP y Laravel: crear, validar y leer |
| [NemonInvocash/verifactu-php](https://github.com/NemonInvocash/verifactu-php) | MIT | 9 | 2026-07-09 | Cliente de Verifactu y TicketBAI. Chico, y es lo único permisivo del régimen español |
| [nfewizard-org/nfewizard-io](https://github.com/nfewizard-org/nfewizard-io) | **GPL-3.0** (`main/LICENSE.txt`) | 330 | 2026-11-08 | NF-e en Node.js contra SEFAZ. ⚠️ GPL-3.0: no se enchufa en un producto cerrado de cliente |
| [gflohr/e-invoice-eu](https://github.com/gflohr/e-invoice-eu) | **WTFPL v2** | 383 | **2026-11-23** | Genera EN 16931 (Factur-X/ZUGFeRD, UBL). ⚠️ No aprobada por OSI: preguntar al área legal del cliente antes de proponerla |

### Capa vertical de viaje — la medición más corta de las once pasadas

| Búsqueda | Total | Lo que hay |
| --- | --- | --- |
| `travel agency invoice billing system` | **2** | `karlomanson/tour-invoices` (GPL-3.0, **0★, último push 2017-02-27**) y uno sin licencia |
| `hotel folio invoice` | **5** | Cuatro sin archivo de licencia; el único con licencia son **plantillas de factura GST** para hoteles indios, no software |
| `per diem allowance calculator` | **0** | — |
| `airline ticket invoice receipt api` | **0** | — |

**La proporción del plano:** la capa horizontal suma **770 + 497 + 383 + 330 + 271 + 154 + 55 + 47
+ 21 + 9 + 4 estrellas** y tiene push de hoy en cuatro repos; la capa vertical de viaje es **un
repo GPL de 2017 con 0 estrellas**. Es la segunda brecha más grande medida en este KB, después de
la del precio — y a diferencia del precio, acá **la pieza horizontal sí resuelve el problema
completo**: una factura de hotel es una factura. Lo que falta no es el motor fiscal, es el
**cableado del dato fiscal del comprador dentro del flujo de reserva**.

### ⚠️ La auditoría de licencia de este plano — y es la inversa de la de la octava pasada

En el plano de la reseña la trampa era un badge que **afirmaba** una licencia que no existía. Acá
el error va en la otra dirección y se repitió **cinco veces**: el campo `license` de la API dijo
`NOASSERTION` y el archivo existía.

| Repo | API | Archivo leído | Causa medida |
| --- | --- | --- | --- |
| `phax/phive-rules` | `NOASSERTION` | Apache-2.0 | El archivo empieza con una línea `====` y un copyright antes del nombre |
| `Quittio/quittio` | `NOASSERTION` | MIT | Está en `master`; en `main` da 404 |
| `TadaSoftware/PyNFe` | `NOASSERTION` | LGPL-3.0 | Texto completo sin encabezado SPDX |
| `BrasilNFe/brasilnfe-mcp` | `NOASSERTION` | MIT | Está en `master` |
| `DoubleH10/zatca-mcp` | `NOASSERTION` | Apache-2.0 | Texto completo sin encabezado SPDX |

**Sobredeclaraciones en este plano: cero.** Descartar por el campo de la API habría tirado cinco
repos usables, cuatro de ellos permisivos. **La regla operativa que se confirma: en este vertical
la licencia se lee del archivo, en las dos ramas, siempre.**

### ⚠️ Las dos licencias de este plano que hay que mirar dos veces

1. **EUPL-1.2 en `ConnectingEurope/eInvoicing-EN16931`.** Son los artefactos oficiales de la
   Comisión, y son **copyleft recíproco**. Usarlos como gate de validación en CI es limpio;
   redistribuirlos dentro del entregable cerrado de un cliente arrastra la reciprocidad. Es el
   único caso de esta KB donde **la norma misma tiene licencia copyleft**.
2. **WTFPL en `gflohr/e-invoice-eu`** (383★, push de hoy). Permite todo y **no está aprobada por
   OSI**. Técnicamente la más libre del plano; políticamente la que más áreas legales rechazan.

### Brechas del plano del comprobante, medidas el 2026-11-23

| Lo que no existe | Evidencia |
| --- | --- |
| Biblioteca de facturación específica de viaje usable | `travel agency invoice billing system` → **2**, el único con licencia es GPL-3.0 de 2017 con 0★ |
| Modelo de datos abierto de folio hotelero fiscalmente válido | `hotel folio invoice` → **5**, ninguno es software con licencia |
| Capa open source de la red de EE. UU. | `dbnalliance` → **1** repo, de 2023, sin licencia, sin biblioteca |
| Cliente de Access Point Peppol open source | `peppol access point client library` → **0** |
| Calculadora de per diem / viático | `per diem allowance calculator` → **0** |
| Campo de identidad fiscal del comprador en un agente de reserva | **Ninguno** de los agentes de reserva catalogados en los once planos de esta KB lo tiene |

### ⚠️ Lo que esta sesión NO pudo verificar, dicho en voz alta

- **Las fechas de los mandatos salen de cobertura secundaria coincidente** (Sovos, Peppol.nu,
  guías de compliance y blogs de viaje corporativo), **no de los textos oficiales**. Dos puntos
  quedaron con fuentes en conflicto y se registran así: **España** (Verifactu corrido a 2027 por
  decreto de diciembre de 2025 según una fuente, enero de 2026 según otra anterior; B2B el
  2027-10-01 o el 2027-10-06) y **Alemania** (emisión 2027 sobre EUR 800.000 de facturación según
  una fuente, 2027–2028 por tamaño según otra). **No se afirma ninguna.**
- **La regla «hotel sí, pasaje de avión y de tren no» en Alemania** viene de una guía de un
  proveedor de viaje corporativo, no del BMF. Es el dato más accionable del plano y el que más
  conviene confirmar con el área fiscal del cliente antes de usarlo en una propuesta.
- **Brasil 2026 es año de prueba de CBS/IBS** con tasas testigo (0,9% CBS / 0,1% IBS) y las
  fuentes discrepan sobre la fecha de NFS-e (2026-08-01, 2026-10-01 o 2026-12-01 según cuál).
  Ninguna fuente localizada trata **hoteles** en particular.
- **No se leyó código** de ninguno de los doce MCP de `cmendezs`: se verificó licencia, liveness,
  estrellas y fecha de push. Que declaren un esquema no prueba que lo implementen bien.

## Plano del seguro — el primer plano donde la capa vertical es más permisiva que la horizontal

*(duodécima pasada, 2026-11-28. Terreno virgen: `seguro`, `siniestro`, `insurance` y `claim`
aparecían 0 veces en `repos/` antes de esta pasada.)*

### Método de verificación de este plano

24 repos medidos. Existencia por `git ls-remote` (**24/24 LIVE**, 0 muertos). Estrellas, forks,
`created_at` y `pushed_at` por `search/repositories` de la API de GitHub. **Licencia leída del
archivo** (`LICENSE`, `LICENSE.md`, `LICENSE.txt`, probando `main` y `master`), nunca del badge ni
del campo de la API — y en esta pasada **la API se equivocó en dos de las tres licencias que
importaban**, en direcciones opuestas (ver la auditoría más abajo).

Lo que esta pasada **no** pudo hacer: el endpoint de la API `repos/{owner}/{repo}` está fuera del
alcance de GitHub de esta sesión, así que los metadatos salen de `search/repositories`. Las
estrellas se reportan **tal como las devolvió la API el 2026-11-28**, sin curvas ni proyecciones —
esta KB fabricó curvas de estrellas en los ciclos 5, 6 y 8 y no se repite.

### Capa horizontal — núcleo de seguro, reglas y tarifación

| Repo | Licencia (archivo) | ★ / forks | Creado / push | Para qué sirve en travel |
|---|---|---|---|---|
| `openl-tablets/openl-tablets` | **LGPL-3.0** | 215★ 57f | 2015-07-21 / **2026-11-28** | Reglas de póliza y tarifación en tablas que un actuario edita sin programar. Es la pieza horizontal más cercana al problema del vertical |
| `OasisLMF/OasisLMF` | **BSD-3-Clause** | 174★ 78f | 2018-01-15 / **2026-11-28** | Modelado de pérdidas. Permisivo, vivo, y **de catástrofes**: útil si el cliente agrega riesgo de interrupción por evento climático, inútil para una demora de vuelo |
| `OasisLMF/OasisPlatform` | **BSD-3-Clause** | 47★ 24f | 2016-04-27 / **2026-11-28** | Orquestación y API sobre el anterior |
| `openimis/openimis-be_py` | **AGPL v3** | 13★ **86f** | 2019-03-14 / 2026-11-27 | Núcleo de gestión de asegurados, pólizas y siniestros, de origen salud y cooperación. **Más forks que estrellas**: es software que se despliega, no que se mira |
| `bhavek-jamnadas/open-rating-engine` | **Apache-2.0** | 1★ | 2026-10-24 / 2026-11-16 | Motor de tarifación nuevo. Permisivo pero de un solo autor y un mes de vida: **riesgo de autor único declarado** |
| `nemmons/aspire` | MIT | 13★ | 2020-12-07 / **2021-03-01** | Motor de tarifación Python legible. **Dormido hace 5 años** — sirve como referencia de diseño, no como dependencia |
| `aposin/CalculusPrime-PnC` | Apache-2.0 | 6★ | 2019 / **2019-11-28** | Motor de tarifas liberado por un banco. **Muerto hace 7 años** |

### Capa vertical de viaje — existe, es permisiva, y tiene catorce semanas

La tabla completa, con la cita de autolimitación de cada uno, está en
`agents/top.md` → «Seguro y siniestro». Lo foundational es esto:

| Repo | Licencia (archivo) | ★ | Creado | Qué aporta como base |
|---|---|---|---|---|
| `phil-cc/voyara-travel-insurance` | **MIT** | 0★ | 2026-11-08 | **La referencia de arquitectura del plano**: un Quote API con dos canales agentic (MCP + WebMCP) y el binding deliberadamente fuera del alcance del agente |
| `tourclaim/tourclaim-cli` | **MIT** | 0★ | 2026-10-04 | SDK + CLI + MCP de reclamo contra el seguro de la tarjeta; el adjudicador queda afuera |
| `Vujavujavuja/Overdoo` | **MIT** | 4★ 1f | 2026-08-22 | Paramétrico de demora: el disparador es dato de vuelo verificable, no juicio de cobertura |
| `byteball/flight-delays-insurance` | **MIT** (`master/LICENSE`) | 18★ 9f | 2017-07-27 / **2022-11-24** | El antecedente histórico: el paramétrico de demora más estrellado del vertical, **dormido hace 4 años**. Útil como prueba de que la idea no es nueva; inútil como dependencia |

**La inversión, dicha con precisión.** Es el primer plano de los doce donde **lo vertical está mejor
licenciado que lo horizontal**: los cuatro repos verticales usables son **MIT**, mientras que la capa
horizontal viva y cercana al problema es **LGPL-3.0 y AGPL-3.0**. El precio de la inversión es la
madurez: lo vertical MIT suma **4★ entre cuatro repos**.

### ⚠️ La auditoría de licencia de este plano — la API falló en las dos direcciones

En la undécima pasada el error del campo de licencia de la API tuvo **una sola dirección**
(subdeclaró 5/5 veces, sobredeclaró 0). En esta pasada falló en ambas, y eso obliga a corregir la
conclusión anterior de esta KB:

| Repo | Campo de la API | El archivo dice | Causa |
|---|---|---|---|
| `openimis/openimis-be_py` | `NOASSERTION` | **GNU AGPL v3** | Línea de encabezado antes del nombre: «The program users must agree to the following terms». **Confirma la causa que la pasada anterior conjeturó** |
| `sepehr071/iran-insurance-mcp` | `NOASSERTION` | **«Free for personal and non-commercial use… Commercial use…»** → **no es open source** | Licencia propietaria a medida, no detectable |
| `luciano-coelho/opin-doctor-ppgcc-ufsc` | `MIT` | MIT, pero «Copyright (c) 2025 **Open Insurance Brasil**» — titular ≠ publicador | La API no mira el titular |

**Conclusión corregida de esta KB:** `NOASSERTION` **no** significa «probablemente permisiva». Significa
**«abrí el archivo»**, y el archivo puede ir para cualquiera de los dos lados. Y un `MIT` correcto en la
API **tampoco cierra el tema**: hay que leer *de quién* es el copyright.

### Brechas del plano del seguro, medidas el 2026-11-28

| Lo que falta | Medición | Consecuencia para una propuesta |
|---|---|---|
| Asistencia en viaje open source | `travel assistance repatriation` → **0 repos**; `medical assistance travel api` → **0** | El corazón operativo del producto (red médica, repatriación, garantía de pago a un hospital) **no tiene una línea abierta en el mundo**. Se compra. No se promete construir |
| Implementación abierta de ACORD | `ACORD insurance standard` → **3 repos, 0 con licencia** | No hay cómo hablar con un carrier en el formato del sector sin licenciar un toolkit comercial. Tercer organismo de estándares de esta KB en la misma situación |
| El principio indemnizatorio en código | 0 de 6 repos de los tramos seguro + EU261 lo implementan | Un agente que reclame EU261 y seguro por el mismo gasto **expone al cliente a una declaración falsa**. Hay que construirlo (Receta 36) |
| El segundo estado del tool (derivar a quien sí puede) | 0 de 6 repos verticales lo implementan; **un solo regulador en el mundo lo nombra** (FCA/MoneyHelper) | Es el hueco de producto del plano (Receta 34) |
| Capa abierta de seguro de viaje en LATAM | `open insurance brazil opin` → 1 repo académico; **cero repos de seguro de viaje de Brasil, México, Chile, Argentina, Colombia o Perú** | Declarado como ausencia medida, no asumida |

### ⚠️ Lo que esta sesión NO pudo verificar, dicho en voz alta

1. **El estatuto de Florida y sus «seis actividades de solicitation»** (incluido «recomendar» y
   «comparar o interpretar coberturas»): la fuente es el blog de un proveedor de agentes de voz
   citando el estatuto. **No se leyó el texto estatutario.** Es la pieza más citable del plano y la
   que más falta verificar contra la fuente primaria antes de usarla con un cliente.
2. **El umbral de la regla de *signposting* de la FCA.** La norma es de abril de 2021 y el umbral
   reportado en prensa de la época es una **recarga de £100 o más** por condición preexistente; la
   FCA consultó cambios en CP24/26 **con efecto 1 de enero de 2026** que afectan, entre otras
   cosas, ese disparador. **No se localizó el umbral vigente.** Usar «hay un umbral y cambió en
   enero de 2026», no una cifra.
3. **La vigencia de la Lei 15.040/2024 de Brasil.** Las fuentes jurídicas dicen **11/12/2025** (art.
   134: un año después de la publicación); la Agência Câmara tituló la entrada en vigor el
   10/12/2024, que parece un error de la propia agencia. **Conflicto registrado y no resuelto.**
   No se localizó el plazo de regulación de siniestro en días.
4. **La relación entre las Guidelines de AI del MAS (7-10-2026) y los principios FEAT de 2018**: no
   se pudo determinar si los reemplazan, los enmiendan o conviven. Las fechas de exigibilidad que
   dan las fuentes **se contradicen** (una dice vigencia 7-10-2027, otra «cumplimiento desde
   octubre 2027 e implementación plena en octubre 2028»).
5. **El AI Discussion Paper v1.1 de la FSA japonesa (3-3-2026)**: existe y está fechado, pero el
   documento es en japonés y **no se localizó su contenido sobre distribución de seguros**. Se
   reporta su existencia, no su contenido.
