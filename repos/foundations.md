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

---
*Ver también: `verticals/solutions.md` para plataformas verticales completas.*
