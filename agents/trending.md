---
industry: travel
region: Global
updated: 2026-11-23
---

# 📈 Agentes trending — Travel & Hospitality

> **Archivo APPEND-ONLY.** Cada ciclo agrega una sección fechada arriba y conserva la
> historia debajo. Reescribir el archivo destruye la tendencia que el archivo existe
> para registrar.
> Este archivo sigue **agentes y skills**. Para repos de infraestructura ver `repos/trending.md`
> (hasta hoy los dos archivos eran copias idénticas; desde este ciclo son distintos).

## 2026-11-23 — undécima pasada (plano del comprobante: una familia de 12 MCP por jurisdicción)

**Lo nuevo de la semana, y por una vez es grande:** apareció una **familia completa de servidores
MCP de facturación electrónica, uno por jurisdicción, toda Apache-2.0** — y **diez de los doce
tienen push en los últimos siete días** (2026-11-16 al 2026-11-22). Es el primer plano de esta KB
donde lo nuevo de la semana no es un repo: es una **grilla regulatoria entera** publicada de golpe.

| Novedad | Licencia (archivo leído) | Stars | Último push | Por qué entra |
| --- | --- | --- | --- | --- |
| [cmendezs/mcp-einvoicing-ae](https://github.com/cmendezs/mcp-einvoicing-ae) | Apache-2.0 | 3 | **2026-11-22** | PINT AE / Peppol 5-corner. El mandato de EAU es de 2026 |
| [cmendezs/mcp-invoicenow-sg](https://github.com/cmendezs/mcp-invoicenow-sg) | Apache-2.0 | 0 | **2026-11-22** | InvoiceNow / PINT-SG. IRAS arrancó el 2026-04-01 con los nuevos registrados voluntarios |
| [cmendezs/mcp-einvoicing-de](https://github.com/cmendezs/mcp-einvoicing-de) | Apache-2.0 | 2 | **2026-11-22** | ZUGFeRD 2.x / XRechnung 3.x — y en Alemania **la factura de hotel entra al mandato y el pasaje de avión y de tren no** |
| [cmendezs/mcp-nfe-br](https://github.com/cmendezs/mcp-nfe-br) | Apache-2.0 | 1 | **2026-11-21** | NF-e / NFC-e modelo 55/65 schema 4.0, en el año de prueba de CBS/IBS |
| [cmendezs/mcp-cfdi-mx](https://github.com/cmendezs/mcp-cfdi-mx) | Apache-2.0 | 0 | **2026-11-21** | CFDI 4.0 + Complemento de Pagos 2.0 |
| [cmendezs/mcp-einvoicing-in](https://github.com/cmendezs/mcp-einvoicing-in) | Apache-2.0 | 1 | **2026-11-21** | GST INV-01 v1.1 / IRP-IRN. **Sin IRN válido no hay crédito fiscal** en India |
| [cmendezs/mcp-facturacion-electronica-es](https://github.com/cmendezs/mcp-facturacion-electronica-es) | Apache-2.0 | 3 | **2026-11-21** | El más estrellado de la familia, empatado con PL y AE |
| [cmendezs/mcp-einvoicing-core](https://github.com/cmendezs/mcp-einvoicing-core) | Apache-2.0 | 0 | **2026-11-21** | La base. Declara que **las llaves de firma se quedan con el cliente** |
| [cmendezs/mcp-ksef-pl](https://github.com/cmendezs/mcp-ksef-pl) | Apache-2.0 | 3 | **2026-11-16** | KSeF / FA(2). `ksef faktura` como búsqueda de repos devuelve **0**: este MCP es lo único |
| [cmendezs/mcp-einvoicing-be](https://github.com/cmendezs/mcp-einvoicing-be) | Apache-2.0 | 0 | **2026-11-16** | Peppol BIS 3.0 / Mercurius. Bélgica obliga desde el **2026-01-01** |
| [OrtaMarco/mx-fiscal-mcp-server](https://github.com/OrtaMarco/mx-fiscal-mcp-server) | MIT | 1 | **2026-11-21** | Valida RFC/CURP/CLABE y lee CFDI. El RFC es **el campo que tiene que estar en la reserva** |
| [phax/phive-rules](https://github.com/phax/phive-rules) | Apache-2.0 (`master/LICENSE`) | 55 | **2026-11-23** | Reglas de validación de e-invoice **multi-jurisdicción**, push de hoy. La API dice `NOASSERTION` y es falso |

**La señal de la pasada, en una línea:** los doce **emiten** y **ninguno reserva**. La identidad
fiscal del comprador —RFC, CUIT, VAT ID, GSTIN— **no existe como campo en ningún agente de reserva
de viaje de esta KB**, y es el único dato que, si falta en el momento de reservar, no se puede
agregar después.

**El hueco que esta pasada deja escrito, y está en North America.** La familia tiene doce
jurisdicciones y **no tiene `mcp-einvoicing-us`**. No es un olvido del autor: **EE. UU. no tiene
mandato federal de facturación electrónica B2B** (sin propuesta en trámite a septiembre de 2026),
y la red DBNAlliance es voluntaria. `dbnalliance` como búsqueda de repos devuelve **1 resultado**,
de 2023, sin licencia y sin código de biblioteca. **La ausencia del servidor de EE. UU. es la
medición correcta del mercado de EE. UU., no una falta de la familia.**

**La trampa de la pasada, y es la más grave de las once.** Dos repos de `causa-prima-ai` se
describen como *«free, AI-native EN 16931-compliant e-invoicing»*, tienen archivo `LICENSE`, y ese
archivo dice **«All rights reserved… No license is granted»**. Uno de los dos
([scribo-skill](https://github.com/causa-prima-ai/scribo-skill), 7★) **se distribuye como skill de
Claude/Codex** — el formato que se copia a un agente sin que nadie abra el LICENSE. Es propietario.

## 2026-11-23 — décima pasada (plano del precio: el agente calcula y no explica)

**Lo nuevo de la semana en agentes de precio, y son tres.** Primera pasada de este KB sobre el
precio: ninguno de los nueve planos anteriores lo había tocado.

| Agente / skill | Licencia (leída del archivo) | Stars | Último push | Por qué entra |
| --- | --- | --- | --- | --- |
| [arikanatakan/revmng-mcp](https://github.com/arikanatakan/revmng-mcp) | MIT | 3 | 2026-06-17 | **El único MCP server de revenue management que existe en GitHub.** De `revenue management mcp server` (7 resultados), es el único del tema. |
| [asgard-ai-platform/skills](https://github.com/asgard-ai-platform/skills) | MIT | 249 | 2026-06-06 | Skill `algo-price-dynamic` con referencia de RM. El precio se distribuye como *skill*, igual que el inventario en la tendencia 7. Origen Taiwán. |
| [mtnrabi/travel-agent-skills](https://github.com/mtnrabi/travel-agent-skills) | MIT | 4 | 2026-10-23 | Ocho skills de precio en vivo **con monitorización de paridad tarifaria** — que tras SAMR/Trip.com es conducta observable, no sólo métrica. |

**La señal de la pasada, en una línea:** los tres calculan; **ninguno divulga**.
`price explanation transparency algorithm` devuelve **0 repos** y `algorithmic pricing disclosure`
devuelve **1 que no es del tema**. Cuatro reguladores piden una explicación del precio y la capa
open source que la emitiría está vacía.

**El movimiento regulatorio que empuja esta pasada (todo de 2026, todo nuevo para este KB):**

- **NA:** NY GBL § 349-a en vigor desde el **2025-11-10**, con una frase textual obligatoria y hasta
  USD 1.000 por violación; apelación de la NRF **argumentada el 2026-10-19** sin fallo localizado; y
  la *One Fair Price Act* —que **prohíbe**, no divulga— aprobada en junio de 2026 y **pendiente de
  firma con plazo 2026-12-31**. En paralelo, el Congreso pidió explicaciones a **ocho aerolíneas** y
  el Senado hizo su primera audiencia dedicada a *surveillance pricing* el **2026-08-04**.
- **APAC:** reglas de conducta de precio de plataformas en vigor el **2026-04-10** por cinco años, y
  la decisión de SAMR sobre **Trip.com** (reportada 2026-07-25, **RMB 5.200 millones**) por imponer
  paridad y exclusividad a hoteles **mediante algoritmos**. Es la primera multa del mundo a una
  empresa de viajes por sus algoritmos de precio.
- **EMEA:** la CRD ya obliga a avisar que el precio fue personalizado (y **no** obliga a explicar los
  parámetros); el *Digital Fairness Act* está **en disputa entre fuentes** sobre si ya fue presentado.
- **LATAM:** **ninguna ley sancionada.** Tres proyectos en trámite (PL 1309/2026, PL 1635/2024,
  PL 5441/2025) y el *Mapa de Temas Prioritários* 2026-2027 de la ANPD.

**La inversión que hace notable a esta pasada:** LATAM es, por primera vez en diez planos, la región
que tiene **el despliegue sin la norma** — Azul (Brasil) y Viva Aerobus (México) ya corren el motor
generativo de Fetcherr. En frontera, equipaje y accesibilidad el hallazgo había sido siempre el
contrario.

**Trampa nueva registrada:** `mtnrabi/travel-agent-skills` es MIT sobre RapidAPI de un tercero
(10 búsquedas/día gratis, luego llave, luego USD 10/mes). Tendencia 15 otra vez.

**Nota de método, heredada del noveno plano y aplicada:** no se cerró el plano con búsquedas. Se
leyeron `revmng`, `revmng-mcp` y el skill de Asgard archivo por archivo. La diferencia con equipaje
es que ahí la implementación estaba escondida y apareció; acá, tras leer los tres, **la divulgación
sigue sin existir**.


## 2026-11-23 — novena pasada (plano del equipaje: el agente que no existe sobre la librería que sí)

Noveno ciclo del mismo día. **No reemplaza nada**: las ocho pasadas anteriores quedan intactas
debajo. Foco: **el equipaje** — la única pieza del viaje que es un objeto físico con cadena de
custodia, y que hasta hoy no tenía una sola mención en los ocho archivos. Verificación: 21/21
slugs vivos por `git ls-remote`, métricas por `search/repositories`, **licencias leídas del
archivo**, y en el caso central **el repo se clonó y se leyó el código**.

**El titular del lado agentic es una ausencia medida:** `airline operations agent stars:>=10`
devuelve **0 repos en todo GitHub**. Toda la superficie agentic de este vertical está del lado de
*buscar y reservar*; ninguna del lado de *operar y responder*. Los agentes que entran abajo no
tocan el equipaje — entran porque son la superficie realmente disponible, y porque la Receta 25
los compone con la capa de mensajería que sí lo toca.

| Nombre | Repo | Licencia (archivo leído) | Stars | Último push | Qué cambió |
|--------|------|--------------------------|-------|-------------|------------|
| Award Travel Finder MCP | [AwardTravelFinder/mcp](https://github.com/AwardTravelFinder/mcp) | MIT (1076B) | 17 | 2026-11-20 | Entra por primera vez. MCP de disponibilidad con millas: el primer servidor MCP de *redención*, no de compra, que esta KB mide |
| disruption-rebooking-copilot | [robsarran65/disruption-rebooking-copilot](https://github.com/robsarran65/disruption-rebooking-copilot) | MIT (1075B) | 0 | 2026-08-10 | Entra por primera vez **con 0★ y se dice**: es el **único repo de IROPS agentic con licencia permisiva que existe**. Escasez, no tracción |
| flightradar-mcp-server | [Cyreslab-AI/flightradar-mcp-server](https://github.com/Cyreslab-AI/flightradar-mcp-server) | MIT (1056B) | 7 | 2026-09-20 | Entra por primera vez. MCP sobre AviationStack. **Llave ajena**: el patrón de dependencia que esta KB ya anotó en el plano de emisiones |
| aviasales-mcp | [stufently/aviasales-mcp](https://github.com/stufently/aviasales-mcp) | **GPL-3.0** (35149B) | 9 | 2026-11-09 | Entra por primera vez **y a la tabla de cautelas**: copyleft fuerte sobre un MCP. Se corre como servicio, no se embebe en producto de cliente |
| mcp-delta | [markswendsen-code/mcp-delta](https://github.com/markswendsen-code/mcp-delta) | **NO HAY ARCHIVO** en ninguna ruta estándar | 6 | 2026-03-11 | Entra **solo como descarte**: sin licencia y automatiza el sitio de una aerolínea nombrada. Doble bloqueo |
| LetsFG | [LetsFG/LetsFG](https://github.com/LetsFG/LetsFG) | MIT real (2173B leídos) + addendum comercial del 1% | 2297 | 2026-11-15 | **Re-medición anti-fabricación: 2296 → 2297 en un día, +1.** Registrar un delta plano es la evidencia de que esta pasada no inventó una curva. Lo que la KB ya tenía escrito es correcto y no se cambia |

**La cuarta colisión de palabra de industria, y la peor de las cuatro:** `baggage stars:>=10`
está encabezado por [`w3c/baggage`](https://github.com/w3c/baggage) (62★), que es la
**especificación del W3C de propagación de contexto en distributed tracing**. Las tres anteriores
(hoppers de Minecraft, `return`, webhooks de Dialogflow) eran ruido; esta es un **estándar del
W3C con repo en la organización `w3c`**, así que un compilador que ordene por estrellas la
compila como infraestructura de equipaje. Detalle completo en `agents/top.md`.

## 2026-11-23 — octava pasada (plano de la reseña: la obligación llegó y la herramienta no)

Octavo ciclo del mismo día. **No reemplaza nada**: las siete pasadas anteriores quedan intactas
debajo. Foco: **el insumo que todo agente de esta KB cita al recomendar un hotel** — la reseña —
y que hasta hoy no tenía una sola mención en los ocho archivos. Verificación: 19/19 slugs vivos
por `git ls-remote`, métricas por `search/repositories`, **licencias leídas del archivo**.

| Nombre | Repo | Licencia (archivo leído) | Stars | Último push | Qué cambió |
|--------|------|--------------------------|-------|-------------|------------|
| c2pa-rs | [contentauth/c2pa-rs](https://github.com/contentauth/c2pa-rs) | **MIT *o* Apache-2.0** (los dos archivos presentes) — GitHub dice `NOASSERTION` | 454 | 2026-11-23 | Entra por primera vez. **Push el mismo día de este ciclo.** La capa de procedencia es la más sana que esta KB midió en cualquier plano. |
| c2pa-org/specifications | [c2pa-org/specifications](https://github.com/c2pa-org/specifications) | **CC-BY-4.0** (18650B) | 215 | 2026-11-16 | Entra por primera vez. **Segunda licencia de contenido del vertical** tras Travel Impact Model: se puede citar, no copiar como código. |
| c2patool | [contentauth/c2patool](https://github.com/contentauth/c2patool) | Apache-2.0 | 174 | 2026-11-20 | Entra por primera vez. El CLI: la vía más corta a una prueba de procedencia. |
| c2pa-js | [contentauth/c2pa-js](https://github.com/contentauth/c2pa-js) | MIT | 44 | 2026-11-23 | Entra por primera vez, **con push de hoy**, mientras `c2pa-node` (MIT, 21★) está **archivado** desde sep-2025. El binding vivo de JS no es el que dice "node". |
| Aspect-Based-Sentiment-Analysis | [ScalaConsultants/Aspect-Based-Sentiment-Analysis](https://github.com/ScalaConsultants/Aspect-Based-Sentiment-Analysis) | Apache-2.0 (11357B) | 585 | 2026-09-07 | Entra por primera vez. **El único repo de lectura de reseñas con push en 2026** — de una cohorte de seis que suma 4535★. |
| ABSA-PyTorch | [songyouwei/ABSA-PyTorch](https://github.com/songyouwei/ABSA-PyTorch) | **NO HAY ARCHIVO** — GitHub declara `MIT` | 2112 | 2023-06-12 | **El repo más estrellado que entra a esta KB este ciclo, y entra a la tabla de trampas.** Archivado. Su único rastro de licencia es un badge que renderiza `packagist/l/doctrine/orm.svg`: **la licencia de un paquete PHP ajeno**. |
| browser-extension (TrueStar) | [TrueStarHQ/browser-extension](https://github.com/TrueStarHQ/browser-extension) | MIT (1064B) | 22 | 2025-09-03 | Entra por primera vez y **como medición de escasez**: es el **único repo MIT real de detección de reseñas falsas en todo GitHub**, y está **archivado**. |

**Lo que esta pasada agrega a la tendencia, dicho como tendencia y no como lista.** Los siete
ciclos anteriores midieron planos donde la pregunta era *cómo está repartida la licencia*
(permisivo en frontera, copyleft en datos de vuelo, ausente en terrestre). Este plano se
reparte en un eje distinto: **por estado de mantenimiento, y el estado no correlaciona con la
demanda regulatoria**. Las tres capas, medidas con el mismo método el mismo día:

- **Detectar que una reseña es falsa** → `fake review detection stars:>=20` devuelve **8 repos
  en todo GitHub** (uno de ellos entra por la sigla `FTC` y es de robótica). El más estrellado
  no tiene licencia; el único MIT está archivado.
- **Leer qué dice la reseña** → 6 repos, **4535★ sumadas**, y **un solo push en 2026**. El más
  grande (2112★) está archivado y sin licencia verificable.
- **Probar de dónde vino un contenido** → un org completo, doble licencia permisiva, **dos
  repos con push el día de este ciclo**. Sana. Y **firma medios, no texto**: no resuelve la
  autenticidad de una reseña escrita.

**La asimetría es el hallazgo.** En 2026 la obligación sobre reseñas se volvió vinculante en
tres de las cuatro regiones —Italia (Ley 34/2026, en vigor 7-abr-2026), la regla de la FTC en
EE.UU., las reglas conjuntas de China (jun-2026)— y la Comisión Europea abrió **procedimiento
formal DSA contra Booking.com el 21-oct-2026**. La capa open source que respondería a esa
obligación es la única de las tres que está vacía. **No es un hueco de madurez: es un hueco de
incentivo.** Nadie publica un detector de reseñas falsas porque el que lo tiene bueno lo tiene
cerrado — y eso, para Globant, es la definición de trabajo a medida.

## 2026-11-23 — séptima pasada (plano de accesibilidad: lo que el agente puede auditar y lo que no puede prometer)

**Plano nuevo.** Antes de esta pasada, `wheelchair`, `a11y` y `axe-core` daban
**cero** coincidencias en la KB. Estrellas medidas hoy por `search/repositories`.

| Señal | Repo | Licencia | Stars | Push | Lectura |
|---|---|---|---|---|---|
| Más vivo del plano | [JustasMonkev/mcp-accessibility-scanner](https://github.com/JustasMonkev/mcp-accessibility-scanner) | MIT (motor `axe-core` MPL-2.0) | 59 | 2026-11-23 | Push el mismo día de la medición. El MCP a usar para auditar un flujo de reserva. |
| Más estrellado en MCP con licencia OSI | [ronantakizawa/a11ymcp](https://github.com/ronantakizawa/a11ymcp) | MIT (motor `axe-core` MPL-2.0) | 97 | 2026-03-10 | ~8 meses sin push. |
| Activo | [priyankark/a11y-mcp](https://github.com/priyankark/a11y-mcp) | MPL-2.0 | 53 | 2026-11-22 | Wrapper también MPL. |
| ⚠️ El más estrellado no se puede usar | [ctoldigital/axuse](https://github.com/ctoldigital/axuse) | **PolyForm Noncommercial 1.0.0** | 805 | 2026-11-03 | 8× las estrellas del siguiente; **no comercial**. |
| ⚠️ El oficial no es abierto | [dequelabs/axe-mcp-server-public](https://github.com/dequelabs/axe-mcp-server-public) | **Propietaria** | 10 | 2026-11-17 | Repo público, `LICENSE` "All rights reserved". |

**Ausencia, que es la señal principal de la semana:** `wheelchair accessible
travel agent` → **0 repos**. `disability travel ai` → 5 repos, todos 0★ sin
licencia. **Todo lo agentic de accesibilidad audita páginas; nada razona sobre
acceso físico.**

### Señales generales de esta pasada (búsquedas globales del brief)

| Señal | Fuente | Estado |
|---|---|---|
| [nirbar1985/ai-travel-agent](https://github.com/nirbar1985/ai-travel-agent) — MIT, **811★**, LangGraph | `search/repositories` | Un directorio lo lista con ~745★; la medida real es 811. **Sin push desde 2025-08-21** (~15 meses). Referencia, no dependencia. |
| [michaelpersonal/trip-optimizer](https://github.com/michaelpersonal/trip-optimizer) — "autoresearch pattern" | Listado en Trendshift | 36★, **sin archivo de licencia**, sin push desde 2026-04-02. **"Trending" en un agregador no es vigencia.** |
| Trip.com TripGenie: volumen de órdenes asistidas por AI **~+400% interanual** | Prensa de viajes vía búsqueda | Cifra de la propia empresa; no auditada. |

## 2026-11-23 — sexta pasada (plano de emisiones: lo que el regulador obliga a calcular)

Licencias leídas en el `LICENSE` del repo tras `git clone --depth 1`. Fecha =
último commit de `HEAD`. **Sin estrellas: la API de GitHub estaba bloqueada
para esta sesión y no se inventan números.**

| Agente / servidor MCP | Licencia (archivo leído) | Último commit | Por qué entra |
|---|---|---|---|
| https://github.com/abahgat/timcp | Apache-2.0 | 2026-02-01 | Primer servidor MCP que expone Scope 3 categoría 6 como tool (`tim_get_scope3_flight_emissions` + batch). Convierte el reporte CSRD en algo que un agente puede ejecutar. |
| https://github.com/andreacappelletti97/google-flights-mcp | ISC | 2026-11-01 | Devuelve CO₂ por leg **junto al precio**, en la misma respuesta. Es el primer repo visto que trata la emisión como atributo de compra y no como reporte posterior. |
| https://github.com/jagan-shanmugam/climatiq-mcp-server | MIT | 2025-03-28 | Multimodal (coche, avión, tren). Entra con reserva: ~20 meses sin commits y depende de la API comercial de Climatiq. |

Tres filas, tres repos reales.

**Lo que cambió respecto de lo que esta KB creía.** Hasta esta pasada,
`repos/foundations.md` afirmaba que alrededor del Travel Impact Model "nadie
publicó el tooling". A noviembre de 2026 eso ya no es cierto: hay un port MIT
fiel (`flightyco2`, validado al 0,07% contra el ejemplo de Google) y un
servidor MCP Apache-2.0 (`timcp`). La brecha se cerró y la KB no se había
enterado.

**La tendencia de fondo, no el repo suelto:** el cálculo de emisiones está
pasando de *reporte anual de sostenibilidad* a *tool que se llama en el momento
de la compra*. `google-flights-mcp` devolviendo CO₂ al lado del precio es esa
transición hecha código.

**⚠️ Señal negativa del ciclo:** las dos calculadoras GLEC/ISO 14083 más
activas del espacio (`majidkabir/Sootcase` y `majidkabir/Carbonara`, ambas con
commits del 2026-11-23) son **PolyForm Noncommercial 1.0.0**. Están vivas, son
buenas y Globant no puede usarlas en un engagement. Es el segundo plano de esta
KB donde lo mejor mantenido es lo no comercial.

## 2026-11-23 — quinta pasada (plano terrestre: tren, bus y transporte público)

**Qué se midió:** el tramo que esta KB venía declarando "hueco abierto" en `intel/market.md`
y en `compose/patterns.md` sin haberlo medido nunca. **La declaración era media verdad:** hay
ocho servidores MCP de transporte terrestre vivos, no uno — y ninguno vende nada.

**Lo que está vivo esta semana, verificado:**

| Agente | Licencia (archivo) | Stars | Push | Por qué entra |
|--------|--------------------|-------|------|---------------|
| [mirodn/mcp-server-public-transport](https://github.com/mirodn/mcp-server-public-transport) | MIT (1061B) | 9 | **2026-11-21** | El MCP de transporte terrestre con push más reciente del mundo. Salidas y planificación en tiempo real. |
| [malkreide/swiss-transport-mcp](https://github.com/malkreide/swiss-transport-mcp) | MIT (1069B) | 7 | 2026-11-01 | Primer MCP del plano que habla **OJP (Open Journey Planner)**, el estándar CEN, en vez de una API propietaria de operador. |
| [lucygoodchild/mcp-national-rail](https://github.com/lucygoodchild/mcp-national-rail) | **NINGUNA** (declara MIT en `package.json`) | 7 | 2026-09-11 | Entra como advertencia, no como recomendación. |
| [EasonWheng/RailGPT](https://github.com/EasonWheng/RailGPT) | MIT (1115B) | 5 | 2026-08-17 | Agente ferroviario con herramientas estructuradas (Southeast University). Investigación. |
| [SeanChangX/THSR-Sniper](https://github.com/SeanChangX/THSR-Sniper) | Apache-2.0 (11363B) | 38 | 2026-03-07 | **Entra como trampa:** licencia impecable, y resuelve el captcha del operador taiwanés por OCR. Inutilizable en un entregable. |

**Lo que se apagó, con fecha:** `r-huijts/ns-mcp-server` (64★, el que esta KB citaba como "el
único MCP ferroviario") lleva **15 meses sin push**; `Kryzo/mcp-sncf` (21★), **20 meses**;
`amith-vp/indian-railway-mcp` (28★, el único de APAC), **19 meses**.

**El dato que ordena la sección:** ocho MCP terrestres, **siete son EMEA**, ninguno de North
America ni de LATAM, **cuatro sin ningún archivo de licencia**, y el techo del plano son 64
estrellas. No es un ecosistema; son proyectos personales sobre una sola región.

**Hallazgo de método de esta pasada:** `rail mcp server` devuelve **Ruby on Rails** y el PaaS
`railway.app` en sus ocho primeros resultados; `train mcp server` devuelve **entrenamiento de
modelos**. Cuarta colisión de palabra de industria de la red de KBs, y la peor: las dos
palabras naturales del dominio están tomadas por el núcleo de la industria del software. Se
busca por operador o por estándar (`hafas`, `osdm`, `netex`, `public transport`), nunca por
modo.

## 2026-11-23 — cuarta pasada (plano de visibilidad agentic)

**Qué se midió:** la capa que decide si un proveedor de travel es **encontrado y citado** por
un agente, que es anterior a todo lo que midieron las tres pasadas de hoy.

**Lo que se movió esta semana, verificado:**

| Agente / herramienta | Repo | Licencia | Stars | Push |
|----------------------|------|----------|-------|------|
| elmo (AEO/GEO, mide citas en ChatGPT/Claude/Perplexity/Gemini/Grok) | `elmohq/elmo` | MIT | 713 | 2026-11-19 |
| GEOInflow (analítica de crawlers AI, self-hosted) | `yaojingang/GEOInflow` | MIT | 866 | 2026-11-14 |
| GEORank | `yaojingang/GEORank` | Apache-2.0 | 542 | 2026-11-11 |
| GetCito (AIO/AEO/GEO + tracking de visibilidad) | `ai-search-guru/getcito-…` | MIT | 424 | 2026-11-05 |
| Searchstack (CLI, 22 comandos, cron-ready) | `alexpospekhov/searchstack-aeo` | MIT | 115 | 2026-09-29 |

**La novedad real de la semana, y es chiquita a propósito:** aparecieron los **primeros repos
de visibilidad específicos de hospitality**, todos con **0 estrellas**:

- `AdamBenDev/hospitality-geo-standard` — **MIT**, creado el **2026-11-16** (hace 7 días):
  especificación + validador CLI sin dependencias para `/llms.txt` y `@graph` JSON-LD de
  `schema.org/Hotel`. Es, literalmente, la pieza que el plano no tenía.
- `thisisshivamtiwari/hotel-ai-answers` — **MIT**, creado el **2026-11-20** (hace 3 días):
  banco de prueba que compara página plana vs JSON-LD vs FAQ vs markup viejo sobre hoteles
  inventados. **Metodología de evaluación, que es lo que falta para poder prometer un número.**
- `Inari-Kira-Isla/aeo-demo-travel-food` — **sin licencia**, push **hoy**.
- `y8y-hq/llms-txt-for-hotels` — **sin licencia**, creado 2026-09-13.

**Cómo leer esto sin exagerarlo:** cuatro repos con cero estrellas no son un ecosistema. Son
**una fecha**. Lo que se registra es que entre el 16 y el 23 de noviembre de 2026 aparecieron
dos repos MIT que intentan estandarizar la visibilidad hotelera, y que **hasta este mes no
existía ninguno**. Si el patrón se sostiene, la próxima pasada de travel debería encontrarlos
con estrellas; si no, quedará registrado que el espacio se intentó y no prendió.

**Búsquedas que devolvieron cero, escritas:** `hotel AEO GEO visibility` → **0**;
`travel schema markup SEO` → **0**; `AI visibility monitoring brand citations stars:>=100` → **0**.

## 2026-11-23 — tercera pasada (plano de pago agentic)

Tercer ciclo del mismo día. **No reemplaza a las dos pasadas anteriores**: las secciones de la
mañana (frontera) y de la tarde (vuelo) quedan intactas debajo. Foco: **con qué se construye el
corte en el pago** que las once recetas de esta KB venían nombrando sin instrumentar.
Verificación: 9/9 slugs nuevos vivos por `git ls-remote`, licencias **leídas del archivo**,
métricas por `search/repositories`.

**Lo que entra** (detalle en `agents/top.md` → *Pago agentic*):

| Repo | Licencia | Stars | Push | Nota |
|------|----------|-------|------|------|
| [google-agentic-commerce/a2a-x402](https://github.com/google-agentic-commerce/a2a-x402) | Apache-2.0 | 572 | 2026-11-11 | Pago agente-a-agente sobre A2A. |
| [paypal/agent-toolkit](https://github.com/paypal/agent-toolkit) | Apache-2.0 | 199 | 2026-09-01 | El único con contraparte en un hito real de travel (Sabre + Mindtrip). |
| [NVIDIA-AI-Blueprints/Retail-Agentic-Commerce](https://github.com/NVIDIA-AI-Blueprints/Retail-Agentic-Commerce) | Apache-2.0 | 89 | 2026-11-23 | ACP + UCP con control del merchant. Push el mismo día. |
| [Shopify/ucp-cli](https://github.com/Shopify/ucp-cli) | MIT | 84 | 2026-11-09 | Skill de compra para agentes. |

**Las tres trampas de esta pasada** (detalle en `agents/top.md` → *Verificar antes de usar*):

1. **`visa/trusted-agent-protocol` no es open source.** 224★, marca Visa, y un `LICENSE.md` de
   **398 bytes** que remite a los términos comerciales del Visa Developer Center. Es la cuarta
   vez en tres pasadas que `NOASSERTION` obliga a abrir el archivo, y la primera en que el
   nombre del titular es justamente lo que desarma la sospecha.
2. **`google-agentic-commerce/AP2` tiene licencia impecable y el repo quieto** desde el
   2026-06-17.
3. **`moizkamran/ExcursioX` fue descrito como MIT por una fuente secundaria y no tiene archivo
   de licencia** (404 en las seis rutas probadas), ni push desde 2024.

**El dato que ordena la pasada:** `AP2 mandate implementation stars:>=20` devuelve **0**. El
protocolo más citado del pago agentic no tiene implementación con tracción — ver
`intel/trends.md` → 18.

## 2026-11-23 — segunda pasada (plano operativo de vuelo)

Segundo ciclo del mismo día. **No reemplaza a la pasada anterior**: la sección de la mañana
(plano de frontera) queda intacta debajo. Foco de esta pasada: **de dónde sale el dato de
vuelo** que todas las recetas de disrupción de esta KB venían dando por supuesto.
Verificación: 15/15 slugs nuevos vivos por `git ls-remote`, métricas por
`search/repositories`, licencias **leídas del archivo**.

| Nombre | Repo | Licencia (archivo leído) | Stars | Último push | Qué cambió |
|--------|------|--------------------------|-------|-------------|------------|
| ourairports-data | [davidmegginson/ourairports-data](https://github.com/davidmegginson/ourairports-data) | **Unlicense — dominio público** (1211B) | 534 | 2026-11-23 | Push **hoy**. Entra a la KB por primera vez. Es el único activo de todo el vertical travel **sin ninguna condición de uso**: ni atribución, ni copyleft, ni contrato. |
| traffic | [xoolive/traffic](https://github.com/xoolive/traffic) | MIT (`license.md` minúscula, 1069B) | 525 | 2026-11-11 | Entra por primera vez. La pieza permisiva central del plano de vuelo. **Segunda vez en dos días que la licencia aparece en una ruta no estándar** — después de `license.txt` en Kamra. |
| airportsdata | [mborsetti/airportsdata](https://github.com/mborsetti/airportsdata) | **MIT** (1191B) — GitHub dice `NOASSERTION` | 172 | 2026-11-21 | Entra por primera vez. Tercer caso registrado de `NOASSERTION` escondiendo una licencia permisiva real (tras `valhalla` y `odoo`). |
| plane-notify | [Jxck-S/plane-notify](https://github.com/Jxck-S/plane-notify) | **Source-Available 1.0 — NO open source** (12453B) | 2554 | 2026-11-13 | **El repo más estrellado que entra a esta KB este ciclo, y entra a la tabla de trampas.** Licencia propia derivada de PolyForm Shield + Elastic License 2.0. GitHub lo muestra `NOASSERTION`. |
| flighty-mcp-server | [CPLX/flighty-mcp-server](https://github.com/CPLX/flighty-mcp-server) | MIT (1079B) | 35 | 2026-08-31 | Entra por primera vez, y como **medición de escasez**: es el **único** MCP server de estado de vuelo por encima de 10★ en todo GitHub. El dato más consultado del vertical tiene un solo servidor MCP, con 35★ y tres meses sin push. |
| Travel Impact Model | [google/travel-impact-model](https://github.com/google/travel-impact-model) | **CC-BY-4.0** (18658B) | 195 | 2026-11-04 | Entra por primera vez. Licencia de **contenido**, no de software: el matiz que decide si se puede copiar código de ahí. |

**Lo que esta pasada agrega a la tendencia, dicho como tendencia y no como lista:** el ciclo
de la mañana encontró un plano (frontera) cuyo piso open source es **permisivo, vivo y con más
de un proveedor por problema**. Esta pasada encontró el plano vecino —datos de vuelo— con la
**distribución inversa**: el músculo mantenido (`tar1090` 1979★, `readsb` 707★, `pyModeS`
674★, `ultrafeeder` 608★, `opensky-api` 476★, `openflights` 1686★) es **todo copyleft**, y lo
permisivo es la periferia: datasets de referencia y una caja de herramientas MIT. Dos planos
adyacentes del mismo vertical, medidos con el mismo método con 7 horas de diferencia,
repartidos al revés. **La lectura para Globant no es "travel es copyleft" ni "travel es
permisivo": es que la licencia se distribuye por capa, y hay que medirla por capa.**

## 2026-11-23

Ciclo enfocado en el **plano de frontera e identidad del viajero**. Todas las filas
verificadas hoy: existencia y métricas por `search/repositories`, licencia **leyendo el
archivo** por `raw.githubusercontent.com`.

| Nombre | Repo | Licencia | Stars | Creado | Último push | Qué cambió |
|--------|------|----------|-------|--------|-------------|------------|
| JourniOne Planning Skills | [JourniOne-ai/JourniOne-Planning-Skills](https://github.com/JourniOne-ai/JourniOne-Planning-Skills) | **NINGUNA** | 1189 | 2026-09-16 | 2026-10-28 | **1189★ en nueve semanas** — el crecimiento más rápido del vertical este año, y **sin archivo de licencia**. README en 7 idiomas (en, zh-CN, ja, es, ko, fr, ar): el primer proyecto de travel que trata el español como idioma de lanzamiento, no de traducción tardía. Inutilizable hasta que publiquen licencia. **Vale la pena volver a mirarlo el próximo ciclo: si licencia MIT, pasa directo a `agents/top.md`.** |
| fastmrz | [sivakumar-mahalingam/fastmrz](https://github.com/sivakumar-mahalingam/fastmrz) | Apache-2.0 | 174 | — | 2026-11-23 | Push **hoy**. Extracción de MRZ desde imagen bajo Apache-2.0: la salida permisiva frente a `Arg0s1080/mrz` (GPL-3.0, 395★), que es lo que devuelve primero toda búsqueda de MRZ. |
| NFCPassportReader | [AndyQ/NFCPassportReader](https://github.com/AndyQ/NFCPassportReader) | MIT | 867 | — | 2026-11-16 | El lector de pasaporte electrónico de referencia en iOS, vivo y MIT. Entra a la KB por primera vez: el plano de identidad nunca se había mirado. |
| PassportEye | [konstantint/PassportEye](https://github.com/konstantint/PassportEye) | MIT | 471 | — | 2026-11-22 | Push anteayer tras años de madurez. Parser de MRZ en Python, MIT. |
| zkpassport/circuits | [zkpassport/circuits](https://github.com/zkpassport/circuits) | Apache-2.0 | 94 | — | 2026-11-18 | Pruebas de atributo de pasaporte sin revelar el documento. El único mecanismo medido que permite "verificar sin almacenar". |
| passport-zk-circuits | [rarimo/passport-zk-circuits](https://github.com/rarimo/passport-zk-circuits) | MIT | 94 | — | 2026-11-05 | Mismo problema, bajo MIT. Dos implementaciones independientes con 94★ cada una: el segmento ZK-identidad tiene competencia real, no un único proyecto.|

**Observación del ciclo — el espejo de la observación anterior.** El 2026-11-21 esta KB
registró que *de los agentes nuevos con tracción, ninguno reserva*. Hoy, mirando un plano
distinto: **de todo lo que sí tiene código permisivo y vivo en travel, nada decide.** Los
repos de identidad leen el documento (NFC, MRZ) y prueban atributos (ZK), pero **ninguno
responde "¿este viajero puede entrar a este país?"**. Igual que en el pago, el open source
llega hasta el borde de la decisión y se detiene. La diferencia es que acá el borde no lo
puso la desconfianza del consumidor: lo puso que la regla de admisión es un contrato
comercial (Timatic) y una competencia soberana.

**Trampa de keyword re-medida, y empeoró.** La consulta
`travel OR trip OR itinerary OR hotel OR flight created:>2026-10-01 stars:>=25` devuelve hoy
25 repos y **ninguno es de la industria travel**: un simulador de vuelo vibe-codeado (367★),
una guía de leveling de WoW (351★), un fix de rendimiento de Oblivion (507★), geolocalización
Doppler de ADS-B (696★), arte de drones y un proxy. Novedad de este ciclo: **ahora contamina
también el boom de tooling agentic** — `scasella/claude-flightdeck` (339★, un dashboard para
Claude Code) y `globalmpc/vibe-preflight` (74★, un chequeo pre-deploy) entran en los primeros
puestos por las palabras *flight* y *preflight*. La contaminación de keyword no es estática:
crece con cada moda que tome prestado el vocabulario de la aviación.

---

## 2026-11-21

Lo nuevo de las últimas semanas. Todas las filas verificadas hoy por `git ls-remote` +
`search/repositories`.

| Nombre | Repo | Licencia | Stars | Creado | Último push | Qué cambió |
|--------|------|----------|-------|--------|-------------|------------|
| jianhao-travel-planner | [awangwang123/jianhao-travel-planner](https://github.com/awangwang123/jianhao-travel-planner) | MIT | 449 | 2026-09-23 | 2026-11-16 | 449★ en dos meses. Skill de itinerario con verificación cruzada multi-fuente — vende la *verificabilidad*, no la generación. Señal fuerte de APAC. |
| travel-plan-viz | [zexuanw958-svg/travel-plan-viz](https://github.com/zexuanw958-svg/travel-plan-viz) | MIT | 415 | 2026-06-13 | 2026-11-19 | Entrega el itinerario como HTML offline de un archivo. El problema que resuelve es "el viajero no tiene señal", no "el LLM no sabe planificar". |
| Tourmind Booking Skills | [tourmind-com/Tourmind-Booking-Skills](https://github.com/tourmind-com/Tourmind-Booking-Skills) | MIT | 2414 | — | 2026-11-20 | Un proveedor B2B publicando sus propias agent skills de booking bajo MIT. Patrón nuevo: el inventario llega como skill, no como API. |
| travel-agent (browser) | [Prism-Shadow/travel-agent](https://github.com/Prism-Shadow/travel-agent) | Apache-2.0 | 52 | 2026-08-31 | 2026-09-08 | Opera sitios reales en el browser y **se detiene en la página de pago**. Reconoce el límite real: se puede navegar, no comprar. |
| personalized-travel-guide-skill | [TokenHungryMash/personalized-travel-guide-skill](https://github.com/TokenHungryMash/personalized-travel-guide-skill) | MIT | 81 | 2026-09-04 | 2026-11-13 | Genera el manual de viaje como web mobile. Mismo patrón que travel-plan-viz: el valor está en el artefacto entregado. |
| trip-planner-skill | [skywain/trip-planner-skill](https://github.com/skywain/trip-planner-skill) | MIT | 51 | 2026-08-15 | 2026-10-10 | Portabilidad explícita entre Claude Code, Codex, Gemini CLI, Cursor y Copilot. La neutralidad de runtime empieza a ser un feature vendible. |
| RollingGo Hotel MCP (Global) | [RollingGo-AI/RollingGo-Hotel-MCP-Global](https://github.com/RollingGo-AI/RollingGo-Hotel-MCP-Global) | MIT | 90 | 2026-08-05 | 2026-11-19 | 2M+ hoteles a tarifa mayorista vía MCP. **Es el sucesor renombrado de `DIDA-AI/Dida-hotel-MCP-CN`**, que figura en la historia de abajo y hoy está muerto. |
| viajante | [felipebasurto/viajante](https://github.com/felipebasurto/viajante) | MIT | 60 | 2026-08-10 | 2026-11-19 | Búsqueda de vuelo+hotel para terminal/Python/asistentes. |
| OTAIP | [TelivityAI/otaip](https://github.com/TelivityAI/otaip) | Apache-2.0 | 47 | — | 2026-11-21 | Push hoy mismo. Sigue siendo chico (47★, no ~550★ como registraron ciclos previos) pero es el único intento de plataforma de orquestación específica de travel. |

**Observación del ciclo:** de los agentes nuevos con tracción, **ninguno reserva**. Planifican,
verifican, renderizan y buscan. El que más se acerca (`Prism-Shadow/travel-agent`) se detiene
deliberadamente en el pago. La capacidad escasa no es el agente — es el acceso tipado y
transaccional al inventario.

**Trampa de keyword medida hoy:** la consulta `travel OR trip OR hotel OR flight created:>2026-10-15 stars:>=15`
devuelve 48 repos, y los de arriba son un simulador de vuelo (`Rolandjg/fableflight`, 359★), un
mod de Oblivion (508★), una herramienta de geolocalización Doppler de ADS-B (684★), un proxy
(`SukkaW/hikyaku`, 115★) y arte generativo de drones. **Ninguno es travel.** Lo mismo con
"time travel for AI agents" (`OrcaReplay`, 1070★), que aparece primero en casi toda búsqueda de
"travel AI agent". Verificar que la fila pertenezca a la *industria*, no al *keyword*.

---

## 2026-07-02 *(historia — conservada, con auditoría al 2026-11-21)*

Estas filas las produjo un pipeline automático sin verificación. Se conservan porque la
historia es el valor del archivo, con el resultado de medirlas hoy.

| Nombre | Licencia registrada | Stars registrados | Estado 2026-11-21 |
|--------|--------------------|-------------------|-------------------|
| [voyant-travel/voyant](https://github.com/voyant-travel/voyant) | Apache-2.0 | 5 | ❌ **MUERTO** (`ls-remote` falla). Estaba listado **primero**. |
| [s6s8/provodnik.app](https://github.com/s6s8/provodnik.app) | ? | 0 | ❌ **MUERTO** |
| [UjjwalSaini07/Wander-Desk](https://github.com/UjjwalSaini07/Wander-Desk) | MIT | 1 | ✅ vivo |
| [liu-dongfang/flight-deal-finder-showcase](https://github.com/liu-dongfang/flight-deal-finder-showcase) | MIT | 0 | ✅ vivo |
| [DIDA-AI/Dida-hotel-MCP-CN](https://github.com/DIDA-AI/Dida-hotel-MCP-CN) | MIT | 0 | ❌ **MUERTO** — rebrandeado a `RollingGo-AI/RollingGo-hotel-MCP-CN` (61★, vivo). Un repo muerto puede ser una mudanza, no una desaparición. |
| [SilasUTK/siam-on-cloud](https://github.com/SilasUTK/siam-on-cloud) | ? | 0 | ❌ **MUERTO** |
| [PAC0119/staywisee](https://github.com/PAC0119/staywisee) | ? | 0 | ✅ vivo, sin licencia |
| [atlasforcn/startup-luggage-guardian](https://github.com/atlasforcn/startup-luggage-guardian) | ? | 0 | ✅ vivo, sin licencia |
| [thatskiff33/AlpineClubBookingsNZ](https://github.com/thatskiff33/AlpineClubBookingsNZ) | MIT | 3 | ✅ vivo |
| [jdpangilinan02/family-book](https://github.com/jdpangilinan02/family-book) | MIT | 0 | ❌ **MUERTO** — y nunca fue travel: era un árbol genealógico self-hosted. Colisión de keyword. |

**Auditoría: 5 de 10 filas están muertas hoy**, y al menos una (`family-book`) nunca perteneció
a la industria. Ocho de diez tenían 0–3 estrellas. Un pipeline que ordena por "trending" sin
piso de estrellas ni chequeo de dominio produce ruido con forma de datos.

---
*Append-only. No reescribir las secciones de arriba: agregar una nueva fechada.*
