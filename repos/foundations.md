---
industry: travel
region: Global
updated: 2026-11-23
---

# 🏗️ Repos fundacionales — Travel & Hospitality

> Bases sobre las cuales construir: ruteo, geocoding, datos de transporte, acceso a GDS e
> **identidad del viajero**. La capa fundacional de travel **no es AI** — es routing, datos
> geoespaciales y documento. Los agentes se montan arriba.
> Filas verificadas el 2026-11-21; la sección de identidad y las brechas nuevas, el 2026-11-23.

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
| `aviation emissions CO2 stars:>=20` | **0** | Cero, pese a que el modelo de referencia (`google/travel-impact-model`) existe: nadie publicó el tooling alrededor. |
| `travel carbon footprint stars:>=30` | 2, **0 utilizables** | `CarbonFootprintAGU` (GPL-3.0, sin push desde 2021-03-20) y `J0ANMM/carbon-calculator` (MIT, sin push desde 2023-05-21). Ambos muertos. |
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

---
*Ver también: `verticals/solutions.md` para plataformas verticales completas.*
