# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Proyecto

**Botificación** — Empresa argentina de soluciones de IA para pequeñas empresas turísticas en países hispanohablantes (mercado inicial: Argentina; expansión planificada: España y resto de LATAM).

Modelo de negocio: SaaS con tiers Starter ($149/mes) → Growth ($349) → Pro ($699) → Enterprise. Ver el plan de negocio completo en `docs/plan-de-negocio.md` (a crear).

## Productos a construir

1. **Bot de atención** — WhatsApp Business API + chat widget web, respuestas 24/7 con LLM, base de conocimiento configurable por cliente
2. **Panel de administración** — Multi-tenant, edición de base de conocimiento, métricas de conversaciones
3. **Sistema de reservas** — Calendario, formulario embebible, pagos (MercadoPago + Stripe), notificaciones automáticas
4. **Automatizaciones de marketing** — n8n self-hosted, flujos post-viaje, recordatorios, reactivación

## Stack tecnológico objetivo

- **Backend:** Node.js / Python + Supabase (PostgreSQL)
- **Frontend:** Next.js
- **LLM:** OpenAI GPT-4o / Anthropic Claude (multi-proveedor)
- **Mensajería:** WhatsApp Business API via 360dialog o Twilio
- **Automatizaciones:** n8n self-hosted
- **Pagos:** MercadoPago (LATAM) + Stripe (internacional)
- **Infra:** Railway / Render / AWS

## Agentes recomendados (disponibles en `~/.claude/agents/`)

Instalados desde `../agency-agents`. Los más relevantes para este proyecto:

- **Producto:** `AI Engineer`, `Backend Architect`, `Frontend Developer`, `MCP Builder`, `Prompt Engineer`
- **Ventas/Marketing:** `Content Creator`, `LinkedIn Content Creator`, `SEO Specialist`, `Outbound Strategist`, `Sales Coach`
- **Operaciones:** `Customer Success Manager`, `Legal Compliance Checker`, `Bookkeeper & Controller`, `Business Strategist`

Para reinstalar agentes: `bash ../agency-agents/scripts/install.sh --tool claude-code --no-interactive`

## Contexto de mercado

- Target: hostales, operadores de turismo de aventura, agencias de viajes, hoteles boutique en Argentina
- Canal principal de comunicación con clientes finales: WhatsApp (>90% penetración en Argentina)
- Pagos en Argentina: MercadoPago es prioritario; considerar restricciones cambiarias al diseñar el modelo de cobro
- Cumplimiento: Ley 25.326 de Protección de Datos Personales (Argentina) aplica desde el día 1
