---
industry: travel
region: Global
updated: 2026-11-28
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
| **OpenFlights** | [jpatokal/openflights](https://github.com/jpatokal/openflights) | **AGPL-3.0** (34523B leídos el 2026-11-23) | 1686 | Perl/PHP, MySQL | Plataforma de registro y visualización de vuelos, y la fuente del dataset de aeropuertos, aerolíneas y rutas más citado del mundo. Se incorpora en la segunda pasada del 2026-11-23 como **la única plataforma del plano de vuelo**. **AGPL-3.0 = copyleft de red**: ofrecerla como servicio obliga a publicar el fuente modificado. Para el *dato* de rutas conviene además revisar los términos del dataset, que no son el archivo de licencia del repo. |
| **SyncZen Cloud** | [Felix-au/SyncZen-Cloud](https://github.com/Felix-au/SyncZen-Cloud) | MIT | 47 | Next.js | PMS y dashboard de check-in. Chico, pero MIT y moderno: buena base para un piloto de check-in conversacional. |
| **open-hotel-pms** | [peeraseepat-cell/open-hotel-pms](https://github.com/peeraseepat-cell/open-hotel-pms) | MIT | 6 | Next.js + Supabase | PMS operations-first para hoteles independientes. 6★: tratar como referencia de esquema, no como base de producción. |
| **EU Digital Identity Wallet** (capa de librerías) | [eu-digital-identity-wallet](https://github.com/eu-digital-identity-wallet) | **Apache-2.0 las librerías y servicios; EUPL-1.2 las apps; CC BY 4.0 la especificación** | 66 / 64 / 47 / 43 (libs) | Kotlin, Swift, JVM | No es una plataforma de travel, es la **infraestructura de identidad del huésped en EMEA**, mantenida por la Comisión Europea. Un check-in que acepta credenciales del wallet se construye sobre `eudi-srv-verifier-endpoint` y `eudi-lib-jvm-openid4vci-kt`, **ambos Apache-2.0**. ⚠️ **No forkear las apps de referencia: son EUPL-1.2.** Ver `repos/trending.md` → *Estratificación de licencia*. |

## ⚠️ Lo que los listados recomiendan y no conviene tomar

| Plataforma | Por qué aparece | Por qué no |
|------------|-----------------|------------|
| [antonkarasbiz/qloapps-hotel-booking](https://github.com/antonkarasbiz/qloapps-hotel-booking) | 59★, aparece **primero** al buscar "open source hotel PMS booking engine" y se describe igual que el original | Es un **fork** de QloApps, no el upstream. Último push 2026-09-13 frente al 2026-11-20 del original. Partir del fork es heredar el mantenimiento de otro. |
| [digital-druid/hoteldruid](https://github.com/digital-druid/hoteldruid) | Citado en todo listado de "mejores PMS open source 2026" | Mirror de GitHub **sin push desde 2018-07-01** (19★). El proyecto upstream sigue vivo fuera de GitHub, pero este repo no es un punto de partida. Además es AGPL-3.0 y solo back-office: no trae booking engine público. |
| [moizkamran/ExcursioX](https://github.com/moizkamran/ExcursioX) | Es **el único resultado travel-específico** al buscar "travel CRM open source", y una fuente secundaria lo describe explícitamente como **MIT**: CRM de viajes con ticketing, booking y gestión hotelera sobre MERN | **No tiene archivo de licencia.** Probadas `LICENSE`, `LICENSE.md` y `license` en `main` y `master` el 2026-11-23: **404 en las seis**. 22★ y **sin push desde el 2024-03-11**; el propio README dice "we are working on this, please be patient". La fuente secundaria **afirmó una licencia que el repo no tiene** — el motivo exacto por el que esta KB lee el archivo en vez del listado. El hueco de "CRM/back-office de agencia open source" **sigue vacío**, y se cubre con Odoo (LGPL-3.0) + módulos propietarios, como ya indica la tabla de arriba. |

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
5. **Leer dos licencias, no una, cuando el sistema consume una red de datos.** Para una
   plataforma que se instala (QloApps, Odoo, Kamra, HAIP) la licencia del repo es la historia
   completa. Para un componente que es **cliente de un servicio de datos** hay un segundo
   documento que no vive en GitHub: `openskynetwork/opensky-api` es GPL-3.0 impecable **y sus
   términos de dato no licencian el uso comercial**; `FlightRadarAPI` es MIT real **y es un
   cliente no oficial** de un servicio con sus propios ToS. Antes de poner un dato de vuelo en
   una demo de cliente hay que saber en cuál de los dos casos se está. Detalle en
   `repos/foundations.md` → *La licencia del dato no es la licencia del código*.
6. **Human-in-the-loop obligatorio en el pago.** No es una preferencia de diseño: es lo que
   hacen hoy las aerolíneas (United mantiene la intervención humana en la compra) y lo que
   la evidencia de confianza del consumidor exige (ver `intel/trends.md`).

## Lo que cambió entre el 2026-11-21 y el 2026-11-23

Una sola cosa, y vale como advertencia de método para toda la KB: **Kamra PMS pasó de
AGPL-3.0 a Apache-2.0 en 48 horas**, con el archivo en la misma ruta y el mismo nombre
(`license.txt`). Un lector que confiara en la nota del ciclo anterior habría descartado la
mejor opción permisiva del vertical por una licencia que ya no estaba vigente.

**Por eso cada licencia de esta tabla lleva la fecha en que se leyó el archivo, y antes de
comprometer una licencia en una propuesta hay que volver a abrirlo.**

## Lo que agregó la segunda pasada del 2026-11-23


Una plataforma (**OpenFlights**, AGPL-3.0) y **una advertencia que cambia el checklist de
diligencia** de todas las demás.

Hasta hoy, la pregunta de licencia de esta KB era *"¿qué dice el archivo?"* — y esa pregunta
resolvía todos los casos que había medido, incluidos los difíciles (`valhalla` MIT bajo
`NOASSERTION`, Odoo LGPL-3.0 bajo `NOASSERTION`, Kamra relicenciado en 48 horas). El plano de
datos de vuelo trajo el primer caso del vertical en que **la respuesta correcta a esa pregunta
sigue sin autorizar el uso**: el código es GPL-3.0 y cumplible, y el **dato** no está
licenciado para uso comercial.

La diligencia, entonces, pasa a tener dos pasos y no uno:

1. **¿Qué dice el archivo de licencia?** — abrirlo, anotar tamaño y fecha. Sin cambios.
2. **¿Este componente consume una red o un servicio de un tercero?** — si la respuesta es sí,
   buscar los términos de ese servicio, que **no están en el repositorio**. Si no se pueden
   leer, el componente es apto para prototipo interno y **no** para un entregable facturable,
   y así hay que decirlo en la propuesta.

## Lo que agregó la tercera pasada del 2026-11-23

**Ninguna plataforma nueva, y el hallazgo es ese.** La pasada se dedicó al **plano de pago
agentic** (`repos/foundations.md` → *Plano de pago agentic*), y el resultado para este archivo
es negativo y conviene dejarlo escrito: **ninguna de las plataformas verticales de arriba
—QloApps, Odoo, Kamra PMS, HAIP, TREK— documenta soporte para ninguno de los protocolos de
pago agentic** (AP2, ACP, UCP, x402).

Eso no es una falla de las plataformas: es **la distancia real entre las dos capas**. El
discurso de "el agente reserva y paga" supone que el PMS o el motor de reserva sabe recibir un
mandato firmado, y **hoy ninguno sabe**. Para un piloto eso significa que la integración de
pago agentic sobre una de estas plataformas es **desarrollo a medida completo**, no
configuración — y es una de las pocas cosas de esta KB que conviene decir en la primera
reunión, no en la tercera.

La única excepción adyacente es [`Shopify/ucp-cli`](https://github.com/Shopify/ucp-cli) (MIT,
84★), que es el patrón correcto —el comercio expone su inventario como *skill* para agentes—
pero es retail y no travel. **Sirve como referencia de arquitectura para envolver QloApps o
Kamra PMS; no como pieza a desplegar.**
---
*Ver también: `repos/foundations.md` (ruteo, datos e identidad) y `compose/patterns.md`
(recetas concretas).*

## Lo que agregó la cuarta pasada del 2026-11-23

La pasada midió el **plano de visibilidad agentic**, y eso cambia una cosa concreta para las
plataformas verticales que esta KB recomienda: **ninguna emite, de fábrica, el JSON-LD que un
agente necesita para citar la propiedad.**

**La evidencia del problema** *[fuentes secundarias, estudio HotelRank 2026 citado por prensa
de hospitality]*: sobre **121.425 home pages de hotel en 7 países**, **36,3% no tiene ninguna
dato estructurado**; sólo **~10,6%** alcanza una marca "buena"; la **mediana del score de
schema hotelero es 0 sobre 100**; y —el dato que más importa— **41,1% de los sitios que sí
emiten JSON-LD usan el tipo equivocado**, típicamente `Organization` o `LocalBusiness` en lugar
de `Hotel` / `LodgingBusiness`.

**Por qué esto es una oportunidad de customización y no una queja.** El 41,1% es un bug
mecánico, no un problema de contenido: el tipo está mal. Es exactamente la clase de defecto que
se arregla **una vez en la plantilla del PMS y se propaga a todas las propiedades**.

| Plataforma | Lenguaje | Dónde se emite el JSON-LD | Trabajo real |
|------------|----------|---------------------------|--------------|
| [QloApps](https://github.com/Qloapps/QloApps) | PHP (PrestaShop) | Plantillas Smarty del front hotelero | Agregar `@graph` con `Hotel` + `Offer` + `AggregateRating` en el layout de ficha de propiedad. |
| [HotelDruid](https://github.com/digital-druid/hoteldruid) | PHP | Páginas de disponibilidad/reserva | Igual, con menos capa de tema: el riesgo es que el HTML es generado a mano. |
| [Odoo](https://github.com/odoo/odoo) (hotel) | Python / QWeb | Vistas QWeb del website | Heredar la vista y añadir el bloque JSON-LD; es el más limpio de los tres. |

**La pieza que convierte esto en un entregable verificable:**
[`scrapinghub/extruct`](https://github.com/scrapinghub/extruct) (BSD-3-Clause, 985★) extrae el
JSON-LD/microdata/RDFa de una URL, y
[`google/schema-dts`](https://github.com/google/schema-dts) (Apache-2.0, 1262★) convierte
"emitir el tipo correcto" en un **error de compilación** en vez de un hallazgo de auditoría
seis meses después. Para los dos PMS PHP,
[`api-platform/schema-generator`](https://github.com/api-platform/schema-generator) (MIT, 475★)
genera los modelos desde el vocabulario.

⚠️ **Lo que no cambió, y conviene no prometer:** sigue sin existir un channel manager open
source permisivo. Lo medido este ciclo: los módulos de Odoo para conectividad OTA son
**AGPL-3** o **licencia propietaria de Odoo**, y el channel manager de QloApps es **un servicio
SaaS pago**, no software libre. La conectividad de distribución sigue siendo trabajo de
integración presupuestado, no una pieza que se adopta.


## Lo que agregó la quinta pasada del 2026-11-23

**Plano terrestre: hay plataformas desplegables, y la elección es de licencia, no de función.**

Hasta esta pasada este archivo cubría hotelería (QloApps, HotelDruid, Kamra, Odoo) y un solo
ítem de transporte (OpenFlights). El plano terrestre aporta **plataformas completas de grado
operador** —software que ciudades y empresas ferroviarias corren hoy en producción— y las tres
mayores son copyleft:

| Plataforma | Repo | Licencia (archivo leído) | Stars | Qué es | Cómo se customiza con AI |
|------------|------|--------------------------|-------|--------|--------------------------|
| **OneBusAway** | [OneBusAway/onebusaway-application-modules](https://github.com/OneBusAway/onebusaway-application-modules) | **Apache-2.0 por referencia** (`LICENSE.txt`, 547B) | 243 | Suite completa de información al pasajero en tiempo real: backend, APIs, apps Android/iOS. Corre en agencias reales de EE.UU. | **La opción permisiva, y la recomendada.** Se despliega para el cliente, se le agrega un servidor MCP encima sobre sus propias APIs REST |
| **navitia** | [hove-io/navitia](https://github.com/hove-io/navitia) | **AGPL-3.0** (`COPYING`, 34520B) | 456 | Motor de planificación multimodal de grado operador (detrás de Île-de-France Mobilités) | **Como servicio separado, nunca embebido.** El producto del cliente llama a su API HTTP |
| **OpenTripPlanner** | [opentripplanner/OpenTripPlanner](https://github.com/opentripplanner/OpenTripPlanner) | LGPL-3.0 | 2781 | El planificador multimodal de referencia (GTFS + OSM) | LGPL permite enlazar desde software propietario, no derivar. Ya estaba en `repos/foundations.md`; se registra acá como **plataforma desplegable**, no como librería |
| **Ara** | [enroute-mobi/ara](https://github.com/enroute-mobi/ara) | **AGPL-3.0** (`LICENSE`, 34520B) | 22 | Servidor de intercambio de datos en tiempo real por protocolo **SIRI** (el estándar CEN) | Como servicio. Es la pieza que falta cuando el cliente europeo publica SIRI y no GTFS-RT |

**La regla de elección, en una línea:** para un entregable que el cliente **posee y puede
cerrar**, la única plataforma terrestre de la tabla es **OneBusAway**. Las otras tres se
despliegan **al lado** del producto y se consumen por API — exactamente la misma disciplina que
este archivo ya aplica a Nominatim.

⚠️ **Dos advertencias de licencia propias de este plano:**

1. El `LICENSE.txt` de OneBusAway son **547 bytes** cuya primera línea es el token sin expandir
   `COPYRIGHT_SECTION`. La concesión Apache-2.0 está por referencia y es identificable —no es
   un badge vacío— pero **falta el titular del copyright**, y la Apache-2.0 §4(d) obliga a
   propagar avisos de atribución. **Resolver ese string con el proyecto antes de entregar.**
2. **No existe una plataforma vertical de *venta* terrestre, de ninguna licencia.** Las cuatro
   de arriba informan, planifican y distribuyen datos; **ninguna emite un billete.** Para
   hotelería este archivo tiene PMS completos; para tierra no hay equivalente, y la diferencia
   hay que decirla en la primera reunión.

## Lo que agregó la sexta pasada del 2026-11-23

Plano de emisiones y reporte. La pregunta de este archivo es siempre la misma:
qué plataforma real se puede customizar con IA encima. Para este plano la
respuesta tiene una forma distinta a la de los planos anteriores.

### No hay una plataforma vertical de emisiones de viaje que sea open source

Buscado y medido este ciclo: **no existe el "Odoo de la huella de viaje"**. Lo
que hay es un **modelo** (TIM, licencia de contenido, sin código), una
**implementación** de ese modelo (`flightyco2`, MIT) y **wrappers MCP**
(`timcp` Apache-2.0, `climatiq-mcp-server` MIT). Es una librería y un
protocolo, no un sistema con usuarios, roles y pantallas.

Consecuencia para un engagement: el plano de emisiones **no se customiza, se
construye**, y se enchufa a la plataforma que el cliente ya tiene (su sistema
de expense, su PMS, su motor de reservas). Es integración, no implantación.

### Lo que sí es customizable, y dónde enchufa

| Plataforma del cliente | Dónde entra el cálculo | Pieza |
|---|---|---|
| Sistema de expense / viajes corporativos | Una fila por vuelo del expense report → tier 1/2/3 | `abahgat/timcp` (Apache-2.0) |
| Motor de búsqueda y reserva | CO₂ por leg **junto al precio**, en la misma respuesta | `andreacappelletti97/google-flights-mcp` (ISC) |
| Producto propio sin dependencia externa | Motor embebido, sin API key | `dupontcyborg/flightyco2` (MIT) |

### ⚠️ Lo que los listados recomiendan en este plano y no conviene tomar

- **`majidkabir/Sootcase` y `majidkabir/Carbonara`** aparecen descritos como
  "open freight CO₂e calculator" siguiendo GLEC e ISO 14083, están **activos
  hoy** y son las opciones más completas del espacio. Son **PolyForm
  Noncommercial 1.0.0**: Globant **no puede usarlas en trabajo de cliente**.
  Leer el `LICENSE` antes de ponerlas en una propuesta.
- **`google/travel-impact-model`** se cita como si fuera una librería. **No lo
  es**: no contiene código, y su licencia se contradice entre el archivo
  `LICENSE` (CC BY 4.0) y el `README` (CC BY-SA 4.0). No es Apache-2.0 —
  ese Apache-2.0 cubre los íconos de las figuras.
- **`branliu0/flight-calculator`** y **`muhammad7hadii/flight-emissions-app`**
  aparecen en resultados de búsqueda y **no tienen archivo de licencia**. Sin
  licencia explícita, todos los derechos reservados.
- **`VIMS-Coder/Sootcase`** lo devuelve el buscador y **no existe**: `git
  clone` da 404.

### El hueco de producto más claro de este plano

**Emisiones de alojamiento: cero.** No se encontró ningún repo permisivo de
huella de hotel (ni HCMI, ni CHSB, ni ISO 14083 para la cama). El vertical sabe
medir el vuelo con precisión de tres tiers y **no sabe medir la noche de
hotel**. Para un cliente hotelero que necesita reportar bajo CSRD, hoy eso se
resuelve con planilla y consultoría — que es exactamente la definición de un
hueco de producto.

## Lo que agregó la séptima pasada del 2026-11-23

### No hay plataforma vertical de viaje accesible open source — hay piezas

Plano de accesibilidad. Ninguna plataforma de travel open source de las que
esta KB recomienda (QloApps, HotelDruid, Odoo, TREK) trae un **modelo de dato
de accesibilidad física** de primera clase. Lo customizable está en tres
lugares:

| Plataforma | Licencia (archivo) | Qué se customiza con AI encima |
|---|---|---|
| [OpenTripPlanner](https://github.com/opentripplanner/OpenTripPlanner) | LGPL-3.0-or-later | La plataforma de planificación accesible que **ya operan agencias de transporte**. El agente consulta su API con `wheelchair=true`; no se modifica el motor. |
| [openrouteservice](https://github.com/GIScience/openrouteservice) | LGPL-3.0 | Perfil `wheelchair` con pendiente, cordón y superficie. Se corre como servicio sin modificar; el agente lo llama como tool para "el último tramo hasta la puerta del hotel". |
| Wheelmap ([frontend](https://github.com/sozialhelden/wheelmap-frontend), MIT) + [a11yjson](https://github.com/sozialhelden/a11yjson) (MIT) | MIT | El stack de dato de accesibilidad física más maduro y permisivo. Base para la ficha de accesibilidad de una propiedad. |

### ⚠️ Lo que los listados recomiendan en este plano y no conviene tomar

| Recomendado | Problema medido |
|---|---|
| AccessMap (`AccessMap/*`) | Sin licencia y dormido desde 2023. Se mudó a `TaskarCenterAtUW/AccessMap` (GPL-3.0+). |
| accessibility.cloud | Sin archivo de licencia. Consumir la API, no forkear. |
| `axuse` como "browser accesible para agentes" | PolyForm Noncommercial. |
| Workspaces del TDEI (UW Taskar Center) | [Backend](https://github.com/TaskarCenterAtUW/workspaces-backend) MIT, **[frontend](https://github.com/TaskarCenterAtUW/workspaces-frontend) sin licencia**. Medio stack no se puede redistribuir. |

### El hueco de producto más claro de este plano

**Un servicio de "ficha de accesibilidad verificable" por propiedad**: lee los
códigos `DisabilityFeature_Enum` que el hotel ya emite por OTA XML, los
normaliza a `a11yjson` con medidas y fecha de relevamiento, y los expone como
tool MCP de tres estados (`sí / no / desconocido`). No existe en open source
(ver *Brechas* en `repos/foundations.md`). Es la Receta 20.

## Lo que agregó la octava pasada del 2026-11-23

### No hay plataforma vertical de reputación open source — y acá la ausencia es un mercado

| Consulta (`search/repositories`) | Resultado |
|----------------------------------|-----------|
| `reputation management open source stars:>=100` | **0** |
| `review moderation trust safety stars:>=200` | **0** |
| `hotel review analysis stars:>=30` | **1**, sin licencia, último push 2017 |

La gestión de reputación es una categoría de producto que la hotelería **ya compra**
—TrustYou, Revinate, ReviewPro y los módulos de reputación de los PMS— y no tiene **ninguna**
contraparte open source. Es la tercera vez que esta KB mide este patrón (emisiones, séptima
pasada: accesibilidad; ahora reputación) y la lectura se repite: **donde la obligación es
nueva y el comprador tiene presupuesto, el open source no llegó.**

### Dónde enchufa esto en las plataformas que esta KB ya recomienda

La reseña no entra por una plataforma nueva: entra **en la que el cliente ya tiene**.

| Plataforma ya recomendada en este archivo | Dónde vive la reseña | Qué se le agrega con lo medido en la octava pasada |
|-------------------------------------------|----------------------|----------------------------------------------------|
| **QloApps** (hotel booking, basado en PrestaShop) | Módulo de comentarios de producto, con la reserva asociada en la misma base | El **gancho de prueba de estadía** más directo del stack: la reserva y la reseña ya están en la misma tabla. Es exactamente la evidencia que pide la Ley 34/2026 italiana. |
| **HAIP** (Apache-2.0, PMS NestJS multi-tenant) | No trae módulo de reseñas | Punto de integración del folio con la reseña: el folio prueba la estadía sin exponer el documento del huésped. |
| **Odoo** (ERP) | Portal y módulos de rating | Clasificación por aspecto con `ScalaConsultants/ABSA` (Apache-2.0) sobre el texto que ya almacena. |

### ⚠️ Lo que los listados recomiendan en este plano y no conviene tomar

| Lo que aparece recomendado | Por qué no |
|----------------------------|------------|
| `songyouwei/ABSA-PyTorch` como "el estándar de análisis de reseñas" (2112★) | **Archivado, sin archivo de licencia, y su badge muestra la licencia de un paquete PHP ajeno.** Es el repo más recomendado del plano en listados y blogs, y el menos tomable. |
| `TrueStarHQ/browser-extension` como detector de reseñas falsas | MIT real, pero **archivado** desde sep-2025. |
| `SayamAlt/Fake-Reviews-Detection` (109★) | **Sin licencia.** Aparece primero en casi toda búsqueda del tema. |
| `OpinRank` como corpus de entrenamiento de hotel | **Sin licencia**: no se redistribuye ni se entrena para un cliente con él. |
| C2PA vendido como "procedencia de reseñas" | C2PA firma **medios**, no el texto de un formulario. Sirve para la **foto** de la habitación; para la reseña escrita no hay cadena de custodia. |

### El hueco de producto más claro de este plano

**Un "sello de estadía verificada" por propiedad, montado sobre el PMS que el cliente ya
tiene.** No intenta detectar reseñas falsas —no existe la herramienta y la regulación no la
exige—: invierte el problema y **prueba las verdaderas**. El PMS ya sabe quién durmió ahí y qué
noches; la reseña se emite con un atributo verificable de estadía (sin exponer identidad, con
el mismo mecanismo ZK que la séptima pasada registró para el pasaporte:
`zkpassport/circuits`, Apache-2.0), y la foto que la acompaña se firma con C2PA en el
dispositivo del huésped (`c2pa-swift`, MIT *o* Apache-2.0). Es lo único de este plano que
puede construirse **hoy, con licencias limpias, sin pedirle a nadie que detecte un fraude**.
Es la Receta 22.

## Plano del equipaje — qué se puede personalizar y qué hay que comprar (2026-11-23)

El patrón de este archivo es *plataforma real que se puede customizar con IA encima*. En el plano
del equipaje el reparto es inusualmente nítido, y conviene llevarlo así a una primera reunión.

### Lo que existe como plataforma abierta y se puede customizar

| Sistema | Licencia (archivo leído) | Qué cubre del plano | Qué se le puede poner encima |
|---------|--------------------------|---------------------|------------------------------|
| [adamf/jetway](https://github.com/adamf/jetway) | **MIT** (1070B) | **Mensajería y custodia**: Type B/AIRIMP, EDIFACT/PADIS, NDC, `pkg/dcs` de control de salida, y `pkg/baggage` con BSM/BPM/BUM + expedientes AHL/OHD/FWD | La superficie agentic **no viene incluida** (`grep` de `mcp`/`agentic` → cero). Es exactamente el hueco donde se construye: Recetas 25, 26 y 27 |
| [adamf/wholesky](https://github.com/adamf/wholesky) | **MIT** (1070B) | Un día-Tierra de aviación simulado sobre Jetway | El banco de pruebas: se ejercita la integración contra tráfico global sintético **antes** de pedir un enlace a un carrier |
| [AxelUser/carry-fit](https://github.com/AxelUser/carry-fit) | **MIT** (1072B) | Medidas de equipaje de mano por aerolínea | La verificación de franquía de la Receta de LATAM y la transparencia de precio que la reforma EMEA exige |

**`jetway` es, en el sentido de este archivo, el "Odoo" de la mensajería aérea**: una base
permisiva, grande y completa sobre la que se customiza, en un plano donde la alternativa es un
proveedor cerrado. Con una diferencia que hay que decir: **Odoo tiene veinte años y miles de
integradores; `jetway` tiene tres meses, un mantenedor y 5 forks.** Se propone como base, no como
garantía.

### Lo que hay que comprar, porque no existe abierto

| Pieza | Estado abierto medido | Consecuencia |
|-------|----------------------|--------------|
| **WorldTracer** (emparejamiento de expedientes entre aerolíneas) | 4 repos lo nombran, **ninguno pasa de 0★** | Se integra al proveedor. `jetway/pkg/baggage/tracing.go` implementa **el perfil del paquete** y declara que **no** es el formato del proveedor |
| **AODB / A-CDM / gestión de cinta** | `airport operations stars:>=20` → **0** | No hay base abierta de operación aeroportuaria. Se compra |
| **Lectura RFID** | `rfid asset tracking stars:>=50` → **0** | Aun con el mandato de la CAAC vigente (ver APAC en `intel/market.md`), la capa física se compra |
| **Etiqueta de equipaje** | `bag tag IATA` → **0** | El documento que identifica la pieza no tiene implementación abierta |
| **Resolución 753** (el texto) | Documento de pago de IATA | Se licencia. [`Lex-van-Os/Beltline`](https://github.com/Lex-van-Os/Beltline) es el único repo que la nombra y **no tiene licencia** |

### La forma de la propuesta que se deduce de esto

Un engagement de equipaje **no es un reemplazo de plataforma**: es una **capa de registro y de
respuesta** entre sistemas comprados. El cliente ya tiene el AODB, el lector y el contrato con el
proveedor de tracing. Lo que no tiene es **el modelo de evento de custodia que las cuatro
obligaciones regionales consumen** (reloj en NA, liquidación por pasajero en EMEA, rastreo de
proceso completo en APAC, franquía numérica en LATAM). Eso es construible, es MIT, y es la
Receta 27.

## Plano del precio — qué se puede personalizar y qué hay que comprar (2026-11-23, décima pasada)

### No hay plataforma vertical de revenue management open source, y acá la ausencia es casi total

En los planos de emisiones, accesibilidad y reputación este KB encontró «no hay plataforma, hay
piezas». En el plano del precio el hallazgo es más duro: **hay una sola pieza**
(`arikanatakan/revmng`, MIT, 2★) y una capa horizontal gigante. No existe ni un Odoo, ni un
OpenMRS, ni un Moodle del precio de viajes.

### Lo que existe como plataforma abierta y se puede customizar

Las plataformas que este KB ya recomienda **almacenan la tarifa pero no la deciden**. Ahí es donde
enchufa este plano:

| Plataforma | Licencia | Stars | Último push | Qué hace con el precio hoy | Dónde enchufa `revmng` |
| --- | --- | --- | --- | --- | --- |
| [Kamra-PMS/kamra-pms](https://github.com/Kamra-PMS/kamra-pms) | Apache-2.0 | 113 | 2026-11-23 | Guarda tarifas y disponibilidad por habitación y fecha | El PMS pide el *booking limit* por clase tarifaria y fecha; `revmng.emsr_b()` lo devuelve con procedencia. El PMS no cambia su modelo de datos: agrega un campo de decisión y un registro. |
| QloApps / HotelDruid / miniCal *(ya auditados en este archivo)* | ver filas de arriba en este mismo archivo | — | — | Tarifa manual o por temporada | Mismo punto de enchufe: la plataforma sigue siendo la fuente de verdad de la tarifa publicada; el motor sólo propone y deja evidencia. |

> El patrón es deliberadamente conservador: **el motor propone, la plataforma publica**. Es lo que
> permite apagar el motor sin apagar el hotel, y es también lo que permite responderle a un
> regulador qué precio se publicó y de dónde salió.

### Lo que hay que comprar, porque no existe abierto

| Capacidad | Productos de mercado | Por qué no hay alternativa abierta |
| --- | --- | --- |
| RM hotelero de producción | IDeaS (desplegado por **Accor** en su portfolio, citado por ITB y Skift), Duetto, Atomize | Requieren dato de mercado propietario y curvas calibradas por cadena; `revmng` da los métodos, no el dato. |
| Precio aéreo generativo | **Fetcherr** — clientes publicados: Delta, WestJet, Virgin Atlantic, **Azul** (Brasil), **Viva Aerobus** (México) | Es el modelo más la operación de publicación de tarifas; no hay equivalente open source ni cerca. |
| Dato competitivo de producción | Rate shoppers comerciales | Lo abierto (`hotelrate-crawl`, `hotel-price-aggregator`, ambos MIT) es crawling: sirve de esquema, no de fuente contractualmente limpia. |
| Publicación de tarifa a GDS/NDC | Travelport, Amadeus, Sabre | Ya cubierto por el plano de distribución de este KB. |

### ⚠️ Lo que los listados recomiendan en este plano y no conviene tomar

- **`tule2236/Airbnb-Dynamic-Pricing-Optimization` (243★)** aparece primero en casi toda búsqueda de
  precio de viajes. **Sin archivo de licencia y último push 2018-11-14.** No es un punto de partida:
  es un trabajo académico de hace ocho años.
- **`DallasBuyer/awesome-dynamic-pricing` (127★)** es la lista de referencia del campo y **tampoco
  tiene licencia**. Úsese como bibliografía, nunca como dependencia.
- Los cinco repos de RM de viajes **sin licencia** (tabla completa en `repos/foundations.md`): varios
  tienen código técnicamente bueno —EMSR-b con modelo de cancelación XGBoost, DAVN en red— y son
  igualmente inusables en una entrega a cliente.
- **Odoo** aparece con «revenue management» en su vertical de hotel. Lo que se encontró son páginas
  de producto de la edición hosteada, **sin módulo open source de RM confirmado**; y la comunidad es
  LGPL, no permisiva. No se cuenta como motor de precio.

### El hueco de producto más claro de este plano

**Un «registro de decisión de precio» como componente instalable**, agnóstico de motor: recibe el
evento de precio (entradas, modelo, versión, resultado), decide si hay que divulgar y con qué texto
según jurisdicción y **línea de producto**, emite el artefacto regional y guarda la evidencia
consultable.

Tres hechos lo convierten en producto y no en idea:

1. **No existe**: `price explanation transparency algorithm` → 0 repos.
2. **Ya es obligatorio en tres regiones** y hay una multa de RMB 5.200 millones en una de ellas.
3. **La pieza que lo alimenta ya está escrita y es MIT**: `revmng` emite versión, *hash* de entradas
   y *timestamp* en cada resultado. Falta la mitad que traduce eso a la obligación local.

Y la variante más vendible es la de LATAM, porque ahí **todavía no es obligatorio**: se vende como
gobierno de dato sobre un motor ya desplegado, y se convierte en cumplimiento el día que el
PL 5441/2025 o su sucesor salga. Receta 30.

## Plano del comprobante — qué se puede personalizar y qué hay que comprar (2026-11-23, undécima pasada)

### No hay plataforma de facturación de viaje open source — pero sí hay motor fiscal maduro

Es la primera vez en once planos que la ausencia vertical **no duele**: una factura de hotel es una
factura, y los motores fiscales horizontales la emiten igual de bien. Lo que falta no es el motor,
es el **cableado del dato fiscal del comprador en el flujo de reserva**.

| Plataforma / pieza | Licencia (archivo leído) | Qué resuelve del plano | Qué hay que construir encima |
| --- | --- | --- | --- |
| [ZUGFeRD/mustangproject](https://github.com/ZUGFeRD/mustangproject) (497★, Apache-2.0) | Apache-2.0 | Emite y valida Factur-X/ZUGFeRD/XRechnung, con CLI para meter en CI | El mapeo folio→factura: línea de habitación, desayuno, *city tax*, IVA por tasa |
| [wmixvideo/nfe](https://github.com/wmixvideo/nfe) (770★, Apache-2.0) | Apache-2.0 | NF-e brasileña contra SEFAZ, en Java | El modelo de servicio de hospedaje y el régimen CBS/IBS de 2026 |
| [OCA/l10n-brazil](https://github.com/OCA/l10n-brazil) (376★) | **AGPL-3.0** | Localización fiscal brasileña **dentro de Odoo**, mantenida por la OCA | Módulo de hospedaje; se publica como módulo Odoo, igual que el patrón de la pasada cuarta |
| [OCA/l10n-mexico](https://github.com/OCA/l10n-mexico) (20★) | **AGPL-3.0** | Ídem para CFDI 4.0 en Odoo | Ídem. **20★ contra 376★**: México está mucho menos cubierto que Brasil en el ecosistema Odoo |
| [QloApps](https://github.com/Qloapps/QloApps) | **OSL-3.0** (ya catalogada en este KB) | PMS + motor de reserva donde el folio ya existe | El campo de identidad fiscal del comprador **en el momento de la reserva**, que es lo que falta |
| [automationsmanufaktur-labs/open-invoice-germany](https://github.com/automationsmanufaktur-labs/open-invoice-germany) (35★) | **AGPL-3.0** | Facturación self-hosted alemana con E-Rechnung | Nada de viaje. Sirve como referencia de UX de emisión |
| [Speicherstadt/belegt](https://github.com/Speicherstadt/belegt) (8★) | **AGPL-3.0** | Archivo documental con modo **GoBD**: guarda e-facturas y escaneos con requisitos de retención | El lado de retención del plano, que ningún agente cubre |

### ⚠️ Lo que los listados recomiendan en este plano y no conviene tomar

- **[InvoicePlane/InvoicePlane](https://github.com/InvoicePlane/InvoicePlane) (3.289★)** es la
  plataforma de facturación open source más estrellada que devuelve cualquier búsqueda, y su
  `LICENSE.txt` **contiene tres licencias, no una**: (1) una **restricción de marca** que prohíbe
  redistribuir la aplicación bajo el nombre y el logo InvoicePlane, (2) **MIT** para el código de
  InvoicePlane, y (3) **la licencia propietaria de CodeIgniter de EllisLab Inc.** para el framework
  que viene empaquetado, redactada como *«legal agreement between you and EllisLab Inc.»*.
  **Decir «InvoicePlane es MIT» es media verdad.** Es un modo de trampa que esta KB no había visto
  en diez pasadas: no es un badge que miente ni un archivo ausente, es **un archivo de licencia que
  contiene la licencia restrictiva de una dependencia empaquetada**. Si entra a un engagement, el
  framework empaquetado va a revisión legal aparte.
- **`causa-prima-ai/scribo`, `scribo-mcp` y `scribo-skill`** se describen como *«free, AI-native
  EN 16931-compliant e-invoicing»* y sus tres archivos `LICENSE` dicen **«All rights reserved…
  proprietary and confidential. No license is granted»**. Leídos los tres el 2026-11-23.
  **No se pueden usar.** El tercero se distribuye como **skill de Claude/Codex**.
- **`gflohr/e-invoice-eu` (383★, push de hoy)** es técnicamente excelente y su licencia es la
  **WTFPL**, no aprobada por OSI. No es un problema de alcance, es un problema de política de área
  legal: hay que preguntar antes de proponerla.
- **`ConnectingEurope/eInvoicing-EN16931`** son los artefactos oficiales de la Comisión y son
  **EUPL-1.2**, copyleft recíproco. Como gate de validación en CI, limpio. Redistribuidos dentro de
  un entregable cerrado, arrastran reciprocidad.

### El hueco de producto más claro de este plano

**Un adaptador de identidad fiscal del comprador para el momento de la reserva.** No es un motor
fiscal —ésos existen y son Apache-2.0— es el campo que falta antes:

- Recibe el identificador fiscal del comprador (VAT ID, RFC, CUIT, GSTIN, NIF) junto con la
  solicitud de reserva, **no después**.
- Lo valida contra la fuente del país cuando hay una (`OrtaMarco/mx-fiscal-mcp-server` valida RFC;
  en la UE hay servicios de validación de VAT ID).
- Lo pasa al PMS o al canal en el campo que el hotel usa para decidir si emite **factura** o
  **recibo de consumidor**.
- Declara explícitamente *«no se pudo pasar la identidad fiscal, el IVA de esta estadía no va a ser
  recuperable»* cuando el canal no tiene el campo, **antes de confirmar la reserva**.

Esta pieza no existe en GitHub con ninguna licencia: `travel agency invoice billing system`
devuelve **2 repos** (uno GPL de 2017 con 0★, uno sin licencia) y `hotel folio invoice` devuelve
**5**, ninguno de ellos software con licencia. Es el hueco de producto mejor delimitado de los once
planos, porque el motor caro ya está resuelto y lo que falta es un adaptador de un solo campo.

## Plano del seguro — qué se puede personalizar y qué hay que comprar (2026-11-28, duodécima pasada)

### No hay plataforma de seguro de viaje open source — y acá la ausencia es doble

En los planos anteriores la ausencia era de **producto**. Acá es de producto **y de operación**:

- **No existe una plataforma de seguro de viaje open source.** Ni una. Lo más cercano es
  `openimis` (**AGPL v3**, 13★ y **86 forks**, push 2026-11-27), un núcleo de gestión de
  asegurados/pólizas/siniestros de origen salud y financiado por cooperación al desarrollo. Se
  puede adaptar a un producto de viaje, pero **no trae nada de viaje**: ni demora de vuelo, ni
  equipaje, ni red médica internacional, ni tramos.
- **No existe la asistencia.** `travel assistance repatriation` → **0 repositorios**.
  `medical assistance travel api` → **0**. La red médica, la garantía de pago a un hospital en el
  exterior y la repatriación son el corazón operativo del producto y **no tienen una línea de
  código abierto en el mundo**. Esto no se construye en un engagement: **se compra, o se integra
  contra el asistidor del cliente.**

### Lo que existe como plataforma abierta y se puede customizar

| Plataforma | Licencia (archivo) | Estado | Dónde enchufa la capa agentic |
|---|---|---|---|
| `openimis` | **AGPL v3** | 86 forks, push 2026-11-27 | Núcleo de póliza y siniestro. Se corre **como servicio** (AGPL): la capa AI va *al lado*, hablándole por API, no compilada adentro |
| `openl-tablets` | **LGPL-3.0** | 215★, push 2026-11-28 | Reglas de cobertura y tarifa **en tablas que un actuario edita**. Es la pieza que convierte «la póliza dice» en algo ejecutable y auditable. LGPL permite enlazarlo desde producto cerrado |
| `OasisLMF` + `OasisPlatform` | **BSD-3-Clause** | push 2026-11-28 los dos | Sólo si el engagement incluye agregación de riesgo por evento (clima, catástrofe). Permisivo de verdad |
| `phil-cc/voyara-travel-insurance` | **MIT** | 0★, 2026-11-08 | **La referencia de arquitectura**, no una plataforma: copiar su corte (cotiza sí, bindea no) y sus dos canales (MCP + WebMCP) |

### Dónde enchufa esto en las plataformas que esta KB ya recomienda

El seguro no es un sistema aparte: es **un campo en el flujo de reserva que ya existe**.

- **QloApps / Kamra PMS / HAIP** (plano base de esta KB): el seguro entra como *ancillary* en el
  checkout. La regla india lo vuelve concreto: **no puede venir pre-tildado** (ver abajo), así que
  el punto de integración es un *opt-in explícito* con nombre de aseguradora, prima e impuesto
  visibles — tres campos, no un checkbox.
- **Odoo** (plano cuarto y décimo): el siniestro es un caso de uso de *helpdesk* + documentos. El
  módulo que falta es el de **evidencia de siniestro de viaje** (parte médico, notificación del
  transportista, registro meteorológico oficial), que es exactamente lo que `tourclaim` recolecta.
- **El motor de derechos del pasajero de la Receta 10** (EU261): es el vecino de pared. Mismo
  evento, dos derechos, y hoy **ninguna pieza abierta impide cobrar dos veces el mismo gasto**.

### ⚠️ Lo que los listados recomiendan en este plano y no conviene tomar

| Lo que aparece recomendado | Por qué no |
|---|---|
| `HelloSafe/travel-insurance-mcp`, `10Life/10life-travel-mcp` como «MCP open source de seguro» | **No tienen archivo de licencia y no son software**: son manuales de conexión a un endpoint remoto ajeno. El código abierto es de cero bytes. Como *proveedor* de cotizaciones pueden servir; como *base* para construir, no existen |
| `sepehr071/iran-insurance-mcp` (18 tools, compara precios de seguro de viaje) | El archivo de licencia dice **«free for personal and non-commercial use»**. Una consultoría **no puede** embeberlo en un entregable. La API dice `NOASSERTION` y no lo advierte |
| Los DApps de *flight delay insurance* de blockchain (`FlightSurety`, `Degis-Core`, `archwing`, `dkhroad-blockchain/flight-delay-insurance`) | Son la cohorte más poblada de la búsqueda (139 repos) y casi toda es **trabajo académico de 2019-2023, sin mantenimiento**. El único vivo es `Overdoo` (MIT, 2026-11-16) y es de un autor |
| `nemmons/aspire` y `aposin/CalculusPrime-PnC` como motores de tarifación | Permisivos y bien escritos, pero **el último push es de 2021 y 2019**. Referencia de diseño, no dependencia |
| Un «agente que vende seguro de viaje» como entregable | Es el punto del plano entero: **vender —y en varias jurisdicciones también recomendar y comparar— es un acto licenciado**. El entregable es el agente que cotiza, documenta y deriva |

### El hueco de producto más claro de este plano

**El tool de tres estados con destinatario en la negativa.** Los seis repos verticales que existen
implementan el tercer estado (*no puedo venderlo*). **Ninguno implementa el segundo** (*no puedo
responder esto, y acá está quién sí*), aunque hay un regulador que lo exige por norma y nombra el
artefacto: la FCA obliga a derivar al directorio de proveedores especializados de MoneyHelper
cuando la cobertura se rechaza, no se ofrece o se recarga por condición médica preexistente.

Es un hueco chico, barato y defendible: un módulo de derivación con un registro auditable de *qué
preguntó el viajero, qué no se contestó, y a quién se lo derivó*. Es la **Receta 34**, y es la
única pieza del plano que una consultoría puede construir, licenciar como MIT y vender a cuatro
regiones sin pedirle permiso a un regulador — porque **documentar una negativa no es distribuir un
seguro**.

---

## 2026-11-28 — decimotercera pasada · Plataformas de la unidad regulada

### ⚠️ Corrección a esta KB: Kamra es Apache-2.0, no AGPL-3.0

El README de esta KB afirmaba, desde la reescritura del 2026-11-21, que *«los tres repos más
grandes del vertical son copyleft (TREK AGPL-3.0, QloApps OSL-3.0, **Kamra AGPL-3.0**)»*. **La
afirmación sobre Kamra es falsa al día de hoy** y se corrige acá y en el README.

Lo que dice el archivo, leído en un clon `--depth 1` de la rama default (`develop`):

- `license.txt` — **11.358 B, texto íntegro de Apache License 2.0**.
- `pyproject.toml` — `license = { text = "Apache-2.0" }`.
- `TRADEMARK.md` — separa explícitamente el código de la marca: *«The code is Apache-2.0: you may
  use, change, host and sell it under that license. The name "Kamra", "Kamra PMS", "Kamra Agent"
  and the Kamra mark are not part of that license»*, «in the same spirit as Frappe and ERPNext».
- La API de GitHub también dice `Apache-2.0`, y **acierta**.

**Por qué importa comercialmente:** Kamra pasa de ser el PMS que había que descartar por copyleft a
ser **el PMS permisivo más activo del vertical** (116★, commit en `develop` del **2026-11-28**). Se
puede modificar, alojar y revender bajo Apache-2.0. **Lo único que no se puede** es usar el nombre
y la marca: una implementación para cliente se presenta como «runs on Kamra PMS» o «Kamra
implementation by Globant», no como un producto propio llamado Kamra. Eso es exactamente el modelo
Frappe/ERPNext y es un patrón con el que la industria ya sabe trabajar.

**Cómo se produjo el error, para no repetirlo:** el archivo se llama `license.txt` —**minúscula y
con extensión**— y una lista de 13 grafías habituales **no lo encuentra**. Un chequeo automático
habría reportado «sin licencia». Ver el defecto de medición en `agents/top.md`.

### Las plataformas del plano

| Plataforma | Repo | Licencia (**archivo leído**) | ★ | Rama / último commit | Qué se puede hacer con ella |
|---|---|---|---|---|---|
| **Kamra PMS** | [`Kamra-PMS/kamra-pms`](https://github.com/Kamra-PMS/kamra-pms) | **Apache-2.0** (`license.txt`) + `TRADEMARK.md` | 116★ | `develop` / **2026-11-28** | PMS hotelero completo: recepción, folio, POS, pagos anticipados. **Permisivo**: base legítima para un producto de cliente. Trae ramas de `feat/guest-visa-oci` y `feat/kamra-connect`, y un directorio `mcp/` — es decir, **ya tiene superficie agentic propia** |
| **QloApps** | [`Qloapps/QloApps`](https://github.com/Qloapps/QloApps) | **OSL-3.0** (`LICENSE.md`, 10.365 B) | **14.525★** | `develop` / 2026-11-20 | El más maduro del vertical. **OSL-3.0 es copyleft con reciprocidad de red**: sirve para desplegar y customizar para un cliente, **no** para embeber en un producto cerrado propio |
| **Condo** | [`open-condo-software/condo`](https://github.com/open-condo-software/condo) | **MIT** (1.077 B) | 437★ | `main` / **2026-11-28** | Gestión de propiedades multi-inquilino: tickets, residentes, cobros. **MIT y con push de hoy** — la base permisiva más grande para la capa de administración |
| **OpenKos** | [`senatroxx/OpenKos`](https://github.com/senatroxx/OpenKos) | **Apache-2.0** (11.357 B) | 130★ | `main` / 2026-09-28 | Pensiones, alquileres y departamentos. **Nacido en Indonesia**: el único de la lista pensado desde APAC, y el modelo de *kos* se parece más al alquiler urbano latinoamericano que un PMS hotelero |
| **RentTools.io** | [`Gribadan/RentTools.io`](https://github.com/Gribadan/RentTools.io) | **MIT** (1.065 B) | 34★ | **`master`** / **2026-11-28** | Gestor para anfitriones de STR: sincroniza calendarios de Airbnb/Booking/Vrbo por iCal, agenda limpieza y **extrae datos de pasaporte del huésped**. MIT y vivo. Es el candidato más directo para colgarle encima la capa de cumplimiento que falta |
| **CM Free** | [`viljemd-hub/channel-manager`](https://github.com/viljemd-hub/channel-manager) | **AGPL-3.0** (34.523 B) | 7★ | `main` / 2026-11-22 | Channel manager autoalojado mínimo; guarda estado en archivos JSON. **AGPL**: se corre como servicio, no se embebe |
| Demo minpaku | [`OceansCreative/oceans-minpaku-demo`](https://github.com/OceansCreative/oceans-minpaku-demo) | **Apache-2.0** (11.358 B) | 0★ | `main` / 2026-06-07 | ⚠️ Su `NOTICE` (708 B) **se declara publicada «as a portfolio»**. Es material de lectura sobre el flujo minpaku, **no una base de producto** |

### Lo que ninguna de estas plataformas hace

**Ninguna de las siete valida un número de registro contra un registro.** Ninguna emite la
transmisión mensual de actividad que el Reglamento (UE) 2024/1028 pide a las plataformas. Ninguna
calcula una tasa turística europea. Ninguna transmite el parte de viajero a una autoridad policial.
Esa es, literalmente, **la superficie de construcción de este plano**: la capa de operación está
resuelta y permisiva, y **el tramo regulado se agrega encima**, lo que es una posición de partida
mucho mejor que la de los planos donde faltaba la pieza cara.

### La trampa de este plano en verticales

[`ivannikolovbg/repull-channel-manager`](https://github.com/ivannikolovbg/repull-channel-manager)
(6★, commit 2026-11-10) **se describe como «open-source channel manager starter»** y su
`LICENSE.md` de 11.134 B es una licencia propia —«Repull Channel Manager Community License
Agreement»— que **contiene «All rights reserved»**. No se puede usar como base. Es la quinta vez en
esta red de KBs que la descripción dice «open source» y el archivo dice lo contrario.
