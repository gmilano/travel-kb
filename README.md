---
industry: travel
region: Global
updated: 2026-11-21
---

# ✈️ Travel & Hospitality KB

> Knowledge base de la industria **Travel & Hospitality** para Globant AI Studios.
> Concierge digital, booking agents, itinerarios verificables, servicing de disrupción,
> revenue management.

## Estado al 2026-11-21

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

## Estructura

```
travel-kb/
├── agents/        # Agentes AI open source (21 verificados) + trampas de licencia
├── repos/         # Repos fundacionales: ruteo, geocoding, GTFS, GDS + brechas medidas
├── verticals/     # Plataformas reales customizables con AI (QloApps, Odoo, HAIP, Kamra)
├── intel/         # Mercado y tendencias, con oportunidades por región
└── compose/       # 6 recetas concretas con repos nombrados
```

## Uso

1. **Nuevo engagement**: `intel/market.md` (sección de la región del cliente) + `repos/foundations.md`
2. **Proponer solución AI**: `agents/top.md` + `compose/patterns.md`
3. **Antes de comprometer una licencia**: `agents/top.md` → "Verificar antes de usar"
4. **Antes de prometer un alcance**: `compose/patterns.md` → "Lo que NO conviene prometer"

---
*Red de KBs Globant AI Studios → [globant-kb](../globant-kb/)*
