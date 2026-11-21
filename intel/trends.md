---
industry: travel
region: Global
updated: 2026-11-21
---

# 📡 Tendencias — Travel & Hospitality

> Estado del vertical al 2026-11-21. Cada tendencia lleva la evidencia que la sostiene y,
> cuando la evidencia es débil, lo dice.

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

---
*Fuentes: Phocuswright 2026, IATA Global Passenger Survey 2026, Expedia Group APAC 2026,
Criteo, Visa 2026, Agoda, prensa especializada de travel, textos regulatorios de UE/APAC/LATAM,
y medición directa sobre la API de GitHub. Las cifras de proveedor sin informe primario
localizable están marcadas como tales en `intel/market.md`.*
