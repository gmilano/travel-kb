---
industry: travel
region: Global
updated: 2026-11-23
---

# 📡 Tendencias — Travel & Hospitality

> Estado del vertical al 2026-11-23. Cada tendencia lleva la evidencia que la sostiene y,
> cuando la evidencia es débil, lo dice. Las tendencias 1–10 se establecieron el 2026-11-21;
> las 11–13 se agregaron el 2026-11-23 al abrir el **plano de frontera e identidad**.

## 1. El agente planifica; el humano todavía paga

La cifra que define el año: **52% de los viajeros de EE.UU. usan AI para planificar y 2%
reserva con ella** (Phocuswright 2026; ~8% contando Google AI Mode). Solo **8% confía en que
la AI complete una reserva**. No es un problema de modelo — es de confianza y de quién responde
si la compra sale mal. Las aerolíneas lo institucionalizaron: United apoya AI para investigación
e inspiración y **mantiene intervención humana en la compra**.

Corolario de ingeniería: el human-in-the-loop en el pago no es una concesión de producto, es el
estado del arte. El agente open source más honesto del ecosistema
([`Prism-Shadow/travel-agent`](https://github.com/Prism-Shadow/travel-agent), Apache-2.0)
navega sitios reales y **se detiene en la página de pago**.

## 2. El merchant of record se volvió la decisión de arquitectura

**12-nov-2026: Travelport y Booked AI completaron una compra de vuelo end-to-end conducida por
AI**, vía NDC sobre Travelport TripServices, **con la aerolínea como merchant of record**. Eso
es exactamente lo que Travelport quería demostrar: que se puede vender por agentes sin que la
aerolínea pierda el control del cobro. Google, en la otra punta, declaró que **no tiene
intención de convertirse en OTA** y que **no es merchant of record**.

Quien diseñe asumiendo que el agente cobra está diseñando contra la postura de todos los
proveedores de inventario a la vez.

## 3. MCP se volvió infraestructura, no experimento

Anthropic **donó MCP a la Agentic AI Foundation (Linux Foundation) en dic-2025**. Lo adoptaron
Sabre, Travelport, Amadeus, Booking.com, Expedia y Turkish Airlines. El **MCP server de Sabre
está en piloto o producción en ~80 empresas de travel** (Virgin Australia, Flight Centre,
Internova), y algunas de esas herramientas corren dentro de ChatGPT y Claude *(fuente
secundaria, sept-2026 — vale confirmarlo contra el press release de Sabre)*.

Travelport lo formuló mejor que nadie en jul-2026: el objetivo es **que la reserva sea
determinística** en lugar de que el modelo infiera el inventario.

## 4. IATA no emitió un estándar agentic — y eso importa

NDC (XML, framework EASD: oferta, orden, pago, servicing, cancelación, reembolso) y ONE Order
son la base. **La capa agentic la construyen proveedores: MCP y UCP, sin aval de IATA.**
TPConnects integró MCP en su plataforma NDC Astra; Amadeus integra NDC y ONE Order para
comercio agentic. Son claims de proveedor, no estándares de la industria.

**Corrección a ciclos previos de esta KB:** se registró "NDC 24.2 obligatorio" y repos
"certificados NDC 24.2". **NDC no es obligatorio.** Su adopción es desigual: Lufthansa Group
reporta >50% de ventas de agencia vía NDC, pero solo de su propio negocio de agencia.

## 5. La demanda agentic llegó antes que la capacidad transaccional

En marzo-2026, en APAC, **ChatGPT superó a Google por 13 puntos porcentuales** en visitas a
páginas de reserva de travel (Criteo). **En el mismo mes, OpenAI retiró la capacidad de reserva
directa de ChatGPT.** El tráfico migró a un asistente que, en ese momento, dejó de poder
cerrar. Ese hueco —intención agentic sin riel transaccional— es el mercado.

## 6. El crecimiento está en plataformas verticales con MCP incorporado

No en frameworks de agentes nuevos. Lo que creció medido en estrellas este año:
[`liketrek/TREK`](https://github.com/liketrek/TREK) (15.842★, AGPL-3.0, creado en marzo-2026 —
15.8k en ocho meses, con MCP server propio), [`Kamra-PMS/kamra-pms`](https://github.com/Kamra-PMS/kamra-pms)
("primer PMS open source agentic-AI-ready"), [`TelivityAI/haip`](https://github.com/TelivityAI/haip),
[`TelivityAI/otaip`](https://github.com/TelivityAI/otaip). El patrón es sistema operativo real +
servidor MCP propio.

Para un engagement esto es buena noticia: la capa agentic se enchufa en lugar de construirse.

## 7. El inventario empieza a distribuirse como *skill*, no como API

[`tourmind-com/Tourmind-Booking-Skills`](https://github.com/tourmind-com/Tourmind-Booking-Skills)
(MIT, 2.414★) es un proveedor B2B publicando sus propias agent skills de booking bajo licencia
permisiva. Los MCP de RollingGo hacen lo mismo con 2M+ hoteles a tarifa mayorista y
compatibilidad con 40+ LLMs. El canal de distribución ya no es "integrá nuestra API": es
"instalá nuestro skill".

## 8. El copyleft domina la plataforma; lo permisivo, la infraestructura

Los tres repos de travel con más tracción son copyleft: TREK (AGPL-3.0, 15.8k★), QloApps
(OSL-3.0 core / AFL-3.0 módulos, 14.5k★), Kamra (AGPL-3.0). Lo permisivo son las piezas de
abajo: graphhopper (Apache-2.0), valhalla (MIT), photon (Apache-2.0), motis (MIT), fli (MIT).

Y hay trampas medidas: [`MikkoParkkola/trvl`](https://github.com/MikkoParkkola/trvl) (95★)
aparece junto a los MIT en toda búsqueda y es **PolyForm Noncommercial 1.0.0** — inutilizable
en un engagement comercial. [`LetsFG/LetsFG`](https://github.com/LetsFG/LetsFG) (2.295★) es MIT
real **más un addendum que pide 1% del valor de la reserva**. QloApps es OSL-3.0 en el core y
AFL-3.0 en los módulos: **la extensión propietaria va en un módulo**.
Ver `agents/top.md` → "Verificar antes de usar".

## 9. Asia tiene el código; Europa tiene la regulación; LATAM tiene al Estado comprando

- **APAC** concentra el open source real de travel (449★, 415★, 179★ y los MCP hoteleros) y la
  adopción más alta medida: **79% de las empresas de travel de APAC ya usan AI, 97% planea**
  (Expedia Group 2026). Singapur publicó en ene-2026 el **marco de gobernanza de AI agentic de
  IMDA**, que cubre cadenas de delegación y coordinación multiagente — el documento regulatorio
  más útil para trabajo con agentes de cualquier región.
- **EMEA** tiene el entorno normativo más denso (Digital Omnibus, Reg. (EU) 2026/1744; alto
  riesgo Annex III corrido a 2-dic-2027 y Annex I embebido a 2-ago-2028) y, a la vez, la
  lectura tranquilizadora de que la mayoría de las herramientas de cara al huésped
  probablemente no son de alto riesgo. En Medio Oriente la única norma vinculante y específica
  sobre sistemas autónomos es la **Regulation 10 del DIFC** de Dubái.
- **LATAM**: Perú (abr-2026), Chile (sep-2026) y Argentina desplegaron asistentes AI de turismo
  nacional en el mismo año. El comprador es el Estado. Y **el open source de travel no habla
  español**: la búsqueda en español devuelve 1 repo con 0 estrellas.

## 10. Lo que no existe, medido

Siete consultas con cero resultados útiles el 2026-11-21: revenue management hotelero,
implementaciones NDC, ERP de agencia / tour operador, predicción de demoras de vuelo, gestión
de alquiler vacacional, reservas de restaurante y SDKs de GDS con comunidad. El detalle está en
`repos/foundations.md` → "Brechas medidas".

**La escasez nunca es el agente: es el acceso tipado y transaccional al dominio.** Es el cuarto
vertical consecutivo de esta red de KBs donde la medición da ese mismo resultado.

Ampliado el 2026-11-23 con seis consultas más, todas del plano de frontera: APIS, PNR, ETIAS,
biometría de embarque, chequeo de documento tipo Timatic y API de requisitos de visado.
**Cero útiles en las seis.**

## 11. El plano de frontera es la excepción permisiva de todo el vertical

En travel, la regla medida durante cuatro ciclos es que **la plataforma es copyleft y la
infraestructura es permisiva** (TREK AGPL-3.0, QloApps OSL-3.0 frente a graphhopper, photon,
motis). El documento de viaje rompe la regla: **todo el segmento es permisivo y está vivo.**

[`AndyQ/NFCPassportReader`](https://github.com/AndyQ/NFCPassportReader) (MIT, 867★, push
2026-11-16) lee el chip ICAO 9303; [`konstantint/PassportEye`](https://github.com/konstantint/PassportEye)
(MIT, 471★) y [`sivakumar-mahalingam/fastmrz`](https://github.com/sivakumar-mahalingam/fastmrz)
(Apache-2.0, 174★, push el 2026-11-23) parsean la MRZ;
[`zkpassport/circuits`](https://github.com/zkpassport/circuits) (Apache-2.0) y
[`rarimo/passport-zk-circuits`](https://github.com/rarimo/passport-zk-circuits) (MIT) prueban
atributos sin revelar el documento; y el verificador del **EU Digital Identity Wallet** es
Apache-2.0, mantenido por la Comisión Europea. **Hay dos implementaciones independientes de
cada problema**, que es la señal de un segmento sano y no de un proyecto solitario.

**Por qué pasa esto y no en otros planos:** la identidad documental es un estándar público
(ICAO 9303) y no un contrato comercial. Donde la especificación es pública, el open source
crece. Donde la especificación es contractual (NDC, Timatic, PNR), no hay nada. **Esa es la
regla predictiva del vertical: el piso open source existe exactamente donde el estándar es
público, y en ningún otro lado.**

## 12. El open source de frontera lee el documento pero no conoce la regla

El complemento exacto de la tendencia 1. Allá, el agente planifica y no paga. Acá, **el
software identifica y no decide.** Entre "sé quién sos" y "podés entrar" hay un dato —la regla
de admisión por par pasaporte×destino con su fecha de vigencia— que no existe en abierto.

La única fuente abierta es una cadena de dos repos: [`ilyankou/passport-index-dataset`](https://github.com/ilyankou/passport-index-dataset)
(MIT, 310★) **archivado desde enero-2025**, que apunta como sucesor a
[`imorte/passport-index-data`](https://github.com/imorte/passport-index-data) (MIT, 88★), que
se declara *"updated regularly"* y cuyo dato lleva **nueve meses sin actualizar** (README:
"Last updated: 17 February 2026"; último push 2026-03-01). Su taxonomía es excelente; sus
valores no sirven para decirle a nadie si puede volar.

El dato vigente vive en **Timatic (IATA)**, de acceso contractual. Es el monopolio de datos
más limpio que esta red de KBs midió en cualquier industria: `timatic travel document check
stars:>=20` devuelve **0**.

## 13. Un estándar de identidad en el que el regulador escribe el código

Nuevo y específico de EMEA: la Comisión Europea no publica solo la norma, **publica la
implementación**, y la estratifica por licencia a propósito — especificación **CC BY 4.0**,
apps de referencia **EUPL-1.2**, librerías y servicios **Apache-2.0**.

Esto invierte el hallazgo que la KB de retail registró el mismo mes sobre beckn/ONDC, donde la
especificación era la pieza *restrictiva* (CC BY-NC-SA, NonCommercial) y las implementaciones
eran permisivas. **La licencia de una especificación y la de su implementación son variables
independientes: hay que leer las dos y no se puede predecir una desde la otra.** La regla ya
se verificó en las dos direcciones, en dos industrias, en el mismo mes.

**Corolario de método, el más caro de este ciclo:** [`Kamra-PMS/kamra-pms`](https://github.com/Kamra-PMS/kamra-pms)
pasó de AGPL-3.0 a Apache-2.0 el **2026-11-21** (commit `ce8dec8`), el mismo día en que el
ciclo anterior leyó el archivo y registró AGPL-3.0 correctamente. **Una licencia verificada no
es un hecho permanente: es una medición con fecha.** Desde este ciclo, toda licencia citada en
esta KB lleva la fecha de lectura del archivo.

---
*Fuentes: Phocuswright 2026, IATA Global Passenger Survey 2026, Expedia Group APAC 2026,
Criteo, Visa 2026, Agoda, prensa especializada de travel, textos regulatorios de UE/APAC/LATAM,
Skift Data + AI Summit Europe (oct-2026), ICAO FALP14 (abr-2026),
y medición directa sobre la API de GitHub y sobre los archivos de licencia en
`raw.githubusercontent.com`. Las cifras de proveedor sin informe primario
localizable están marcadas como tales en `intel/market.md`.*
