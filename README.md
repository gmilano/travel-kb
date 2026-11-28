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
3. **La licencia es arquitectura.** Los tres repos más grandes del vertical son copyleft
   (TREK AGPL-3.0, QloApps OSL-3.0, Kamra AGPL-3.0); lo permisivo es la infraestructura.
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

## Estructura

```
travel-kb/
├── agents/        # Agentes AI open source verificados + trampas de licencia
├── repos/         # Fundacionales: ruteo, geocoding, GTFS, GDS, identidad, vuelo,
│                 #   pago, visibilidad, plano terrestre + brechas medidas
├── verticals/     # Plataformas reales customizables con AI (QloApps, Odoo, HAIP, Kamra)
├── intel/         # Mercado y tendencias, con oportunidades por región
└── compose/       # 36 recetas concretas con repos nombrados
```

## Uso

1. **Nuevo engagement**: `intel/market.md` (sección de la región del cliente) + `repos/foundations.md`
2. **Proponer solución AI**: `agents/top.md` + `compose/patterns.md`
3. **Antes de comprometer una licencia**: `agents/top.md` → "Verificar antes de usar"
4. **Antes de prometer un alcance**: `compose/patterns.md` → "Lo que NO conviene prometer"

---
*Red de KBs Globant AI Studios → [globant-kb](../globant-kb/)*
