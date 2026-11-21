---
industry: travel
region: Global
updated: 2026-11-21
---

# 🏗️ Repos fundacionales — Travel & Hospitality

> Bases sobre las cuales construir: ruteo, geocoding, datos de transporte y acceso a GDS.
> La capa fundacional de travel **no es AI** — es routing y datos geoespaciales. Los agentes
> se montan arriba. Todas las filas verificadas el 2026-11-21.

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

---
*Ver también: `verticals/solutions.md` para plataformas verticales completas.*
