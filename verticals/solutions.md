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
