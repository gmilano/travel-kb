---
industry: travel
region: Global
updated: 2026-11-28
---

# ✈️ Travel & Hospitality KB

> Knowledge base de la industria **Travel & Hospitality** para Globant AI Studios.
> Concierge digital, booking agents, itinerarios verificables, servicing de disrupción,
> revenue management.

## Estado al 2026-11-28

Reescritura completa. El contenido anterior databa del 2026-07-02 y tenía filas de ejemplo
publicadas como datos (celdas de guión con la leyenda de pendiente), repos muertos y colisiones de keyword
(un árbol genealógico listado como agente de travel). Todo lo que hay ahora fue verificado:
existencia por `git ls-remote`, estrellas y actividad por la API de GitHub, y **licencia leída
del archivo de licencia**, no del badge.

**Las tres cosas que hay que saber antes de una reunión con cliente:**

1. **El viajero planifica con AI y no compra con AI.** 52% planifica / 2% reserva en EE.UU.
   (Phocuswright 2026); 8% confía en que la AI complete una reserva. El entregable honesto
   termina antes del pago o lo entrega al merchant of record.
2. **IATA no emitió estándar agentic.** NDC + ONE Order son la base; MCP y UCP los construyen
   proveedores. NDC **no es obligatorio**. La neutralidad de protocolo es la habilidad vendible.
3. **La licencia es arquitectura.** Los repos más grandes del vertical son copyleft
   (TREK AGPL-3.0, QloApps OSL-3.0); lo permisivo es la infraestructura. **Corrección del
   2026-11-28: Kamra NO es AGPL-3.0.** Su `license.txt` (11.358 B) es Apache-2.0 íntegro y su
   `pyproject.toml` lo declara; hay un `TRADEMARK.md` aparte que reserva sólo la marca. Es el PMS
   permisivo más activo del vertical (116★, commit de hoy). Ver `verticals/solutions.md`.
4. **El tramo terrestre informa pero no vende.** (quinta pasada, 2026-11-23) Consultar un tren
   europeo está resuelto con código ISC/MIT vivo; **vender uno no tiene una línea de open source
   en el mundo**. El estándar de venta **OSDM es Apache-2.0** y respaldado por la TSI de
   telemática de la UE — y `osdm client implementation` devuelve **0 repositorios**.
5. **La accesibilidad se audita pero no se promete.** (séptima pasada, 2026-11-23) Auditar el
   flujo de reserva contra la EAA tiene herramientas Apache vivas; responder "¿puedo entrar en
   silla de ruedas?" tiene **0 agentes open source**, y schema.org **no tiene término** para eso
   en un lugar. El vocabulario de la industria (OpenTravel) existe y **no tiene licencia**.
6. **El agente reserva y no puede facturar — y si no pasa la identidad fiscal del comprador
   en la reserva, el IVA se pierde para siempre.** (undécima pasada, 2026-11-23) Es el primer
   plano donde la pieza cara ya existe y es permisiva (`wmixvideo/nfe` 770★ Apache-2.0,
   `mustangproject` 497★ Apache-2.0, los dos con push de hoy) y lo que falta es **un campo**.
   Y es el primer plano donde **la capa open source más fuerte es de LATAM**, porque Brasil
   obliga desde 2008.
7. **El acto regulado es *hablar*, no ejecutar — y la capa agentic del vertical nació en catorce
   semanas.** (duodécima pasada, 2026-11-28) Describir una cobertura, **recomendar** un límite o
   **comparar** pólizas es un acto licenciado en EE. UU., y EIOPA preguntó en septiembre de 2026 si
   un chatbot que filtra productos o recomienda está **distribuyendo seguros** bajo la IDD. El
   concierge ya desplegado que contesta «¿esto me lo cubre?» **cruzó un límite sin cobrar nada**.
   Los seis repos agentic de seguro de viaje que existen fueron creados entre el **2026-08-22 y el
   2026-11-08**, ninguno pasa de 2★, y **cuatro ya traen la baranda escrita en el README** sin que
   el regulador haya cerrado la frase (`voyara`, MIT: *«quote a policy without letting them buy
   one»*). Es también el primer plano donde **lo vertical está mejor licenciado que lo horizontal**.

8. **El esquema le pasó por encima al conector: el campo existe y el validador no.**
   (decimotercera pasada, 2026-11-28) El número de registro de una unidad de alojamiento —el eje
   del Reglamento (UE) 2024/1028 (aplicable desde el **2026-05-20**), del CIN italiano, de la Local
   Law 18 de Nueva York, del STRA Register de NSW, del padrón de la CDMX y de la Ley 6255 de CABA—
   **ya tiene campo tipado en los dos protocolos abiertos de STR**, y **cero** implementaciones que
   lo validen contra un registro: ocho búsquedas en GitHub en **0**. VRP tipifica `evidence` ∈
   {`self_declared`, `registry_verified`, `state_attested`} y **exige descargo cuando es
   autodeclarado**, así que **toda implementación abierta de hoy sólo puede emitir
   `self_declared`**. Y es el plano que **refina** la ley de la pasada de retail: los plazos **ya
   pasaron** y lo que apareció fue **el esquema**, porque *un plazo coordina voluntarios de
   estándares, no de integración*. Además: en España el Supremo **anuló el registro** y
   **sobrevivió el deber de transmisión** — construir contra el caño, no contra el registro.

## Estructura

```
travel-kb/
├── agents/        # Agentes AI open source verificados + trampas de licencia
├── repos/         # Fundacionales: ruteo, geocoding, GTFS, GDS, identidad, vuelo,
│                 #   pago, visibilidad, plano terrestre + brechas medidas
├── verticals/     # Plataformas reales customizables con AI (QloApps, Odoo, HAIP, Kamra)
├── intel/         # Mercado y tendencias, con oportunidades por región
└── compose/       # 39 recetas concretas con repos nombrados
```

## Uso

1. **Nuevo engagement**: `intel/market.md` (sección de la región del cliente) + `repos/foundations.md`
2. **Proponer solución AI**: `agents/top.md` + `compose/patterns.md`
3. **Antes de comprometer una licencia**: `agents/top.md` → "Verificar antes de usar"
4. **Antes de prometer un alcance**: `compose/patterns.md` → "Lo que NO conviene prometer"

---
*Red de KBs Globant AI Studios → [globant-kb](../globant-kb/)*
