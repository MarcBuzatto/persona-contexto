---
id: note-registro-de-decisoes
type: note
title: "Registro de decisões"
project: "[[Persona]]"
year: 2026
tags:
  - decisao
updated: 2026-08-18
---

# Registro de decisões

Decisões são inegociáveis até serem explicitamente revogadas. Nada aqui é apagado — o que perde validade fica marcado como **[REVOGADO]**, com o motivo.

## Decisões cruzadas (afetam produto e competição)

| ID | Decisão | Data |
|---|---|---|
| **X-001** | O Persona passa a ser definido como **sistema de evidências profissionais**. O [[Persona Live]] apresenta argumentos reais e rascunho curto simultaneamente, mas separados; adapta a extensão priorizando concisão; tem modo Manual sem captura e Automático autorizado. No MVP: Manual funcional, Automático em demonstração controlada | 05/08/2026 |

## Decisões de produto

| ID | Decisão | Data | Situação |
|---|---|---|---|
| D-001 | Cor primária `#7C3AED` | 26/04/2026 | Vigente |
| D-002 | Tipografia Plus Jakarta Sans + JetBrains Mono | 26/04/2026 | Vigente |
| D-003 | Logo Constellation, versões rica e compacta | 26/04/2026 | Vigente |
| D-004 | Direção estética híbrida humano-analítica | 26/04/2026 | Vigente |
| D-005 | LLM: Claude Sonnet via Anthropic | 22/04/2026 | **[REVOGADO]** por D-019 |
| D-006 | Embeddings: text-embedding-3-small (OpenAI) | 22/04/2026 | **[REVOGADO]** por D-021 e D-022 |
| D-007 | Banco: PostgreSQL via Supabase | 22/04/2026 | Vigente |
| D-008 | Priorizar validação com usuários antes de qualquer código | 22/04/2026 | Vigente — **e sistematicamente descumprida** |
| D-009 | Custo operacional máximo de R$ 1.500/mês | 22/04/2026 | Vigente |
| D-010 | Mascote Xisto, base visual de constelação | 14/07/2026 | Vigente na v1; reaberto na v2 |
| D-011 | Interface gerada por IA como referência de layout; tokens do Design System são a fonte de verdade de cor e tipografia | 14/07/2026 | Vigente |
| D-012 | Planos Free / Pro R$ 29,90 / Premium R$ 59,90 / Business sob consulta | 14/07/2026 | Vigente |
| D-013 | Navegação inferior fixa: Início · Histórico · Artefatos · Perfil | 16/07/2026 | Vigente |
| D-014 | Reconstrução dos tokens e do README do Design System | 15/07/2026 | Confirmada por D-026 |
| D-018 | `apps/web` publicado em `github.com/yan1405/persona_mvp` | 23/07/2026 | Vigente |
| D-019 | LLM passa para Groq; revisado no mesmo dia para `llama-3.3-70b-versatile` | 24/07/2026 | Vigente |
| D-020 | Instalação sem Google Play, via PWA | 24/07/2026 | Vigente |
| D-021 | Embeddings passam para Groq `nomic-embed-text-v1_5` | 24/07/2026 | **[REVOGADO]** no mesmo dia — modelo indisponível na conta real |
| D-022 | Narrative Score v1 **sem nenhum provedor de embeddings**: Consistência determinística, Coerência julgada pelo LLM sobre o texto bruto | 24/07/2026 | Vigente |
| D-023 | Nova tela "Definir nova senha", fecha o fluxo de recuperação | 24/07/2026 | Vigente |
| D-024 | Nova tela Detalhe de Artefato | 27/07/2026 | Vigente |
| D-026 | Pacote original do Design System localizado; tokens idênticos à reconstrução; 5 de 6 SVGs recuperados | 28/07/2026 | Vigente |
| D-027 | Commit e push das três entregas pendentes, após revisão de código com 6 correções | 28/07/2026 | Vigente |
| D-028 | Reorganização de pastas: repositório de código separado do material de competição | 29/07/2026 | Vigente |

## Padrão que vale registrar

Três decisões técnicas (D-019, D-021, D-022) foram tomadas com base em pesquisa de terceiros e **revogadas no mesmo dia**, quando testadas contra a API real. A lição virou regra: **testar contra o serviço real antes de registrar como decisão.**
