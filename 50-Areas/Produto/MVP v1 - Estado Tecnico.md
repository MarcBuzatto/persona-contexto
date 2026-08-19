---
id: area-mvp-v1-estado-tecnico
type: area
title: "MVP v1 — estado técnico"
tags:
  - produto
  - tecnico
updated: 2026-08-18
---

# MVP v1 — estado técnico

Repositório de código: `persona_v1`. Documentação de origem: `CLAUDE.md` v2.6, `AGENTS.md`, `docs/PERSONA_STATUS_PRODUTO.md` v2.0, `docs/PERSONA_CHECKLIST_MVP.md` v1.3.

## Stack real

| Camada | Tecnologia |
|---|---|
| Framework | Next.js 14, App Router, TypeScript estrito |
| Estilo | Tailwind CSS com os tokens do [[Design System]], shadcn/ui |
| Banco | PostgreSQL via Supabase, com RLS em todas as tabelas |
| ORM | Prisma, schema versionado em repositório próprio |
| Auth | Supabase Auth (real, não mock) |
| LLM | Groq `llama-3.3-70b-versatile` |
| Embeddings | Nenhum — eliminados por decisão D-022 |
| Instalação | PWA (manifest, service worker, offline, ícones) |
| Gráficos | Recharts |

Custo medido em produção da chamada de LLM: US$ 0,0011 a 0,0012 por chamada.

## O que está construído

- 15 telas do MVP + tela de definir nova senha (D-023) + detalhe de artefato (D-024)
- Navegação inferior fixa: Início · Histórico · Artefatos · Perfil (D-013)
- Narrative Score v1: **Consistência** por cálculo determinístico de regularidade (frequência, intervalo médio, streak) e **Coerência** por julgamento do LLM sobre o texto bruto dos logs. **Credibilidade** fica para a v2.
- Geração de artefato STAR com prompts versionados e few-shot
- Enum de planos (FREE/PRO/PREMIUM/BUSINESS) com limite real de 1 artefato/mês no Free, protegido contra condição de corrida por transação com `pg_advisory_xact_lock`
- Dois usuários de teste reais (PRO e BUSINESS) para demonstração à banca

## O que falta

| Item | Gravidade |
|---|---|
| **Deploy em produção** — nunca configurado, nenhuma URL pública | **Crítica** |
| Teste do PWA em celular físico | Alta |
| Testes automatizados — inexistentes | Média (dívida técnica) |
| `npm audit` — 9 vulnerabilidades nunca tratadas | Média |
| Geradores de carta, portfólio e pitch pessoal — só STAR existe | Média |
| Relatório semanal (prometido no plano Pro) e análise de mercado (Premium) | Média — o paywall promete o que o produto não entrega |
| Revisão jurídica real dos Termos e da Política de Privacidade | Alta, por LGPD, antes de qualquer usuário externo |

> [!danger] Sem deploy, não há validação
> A ausência de URL pública não é só dívida técnica: ela bloqueia diretamente o teste de protótipo com usuários reais, que é o gargalo do projeto inteiro. Resolver o deploy é pré-requisito de [[Pendencias e Riscos]] C-01 e C-17.

## Cópia local incompleta (achado de 18/08/2026)

**[FATO]** A cópia de `persona_v1` na máquina do Markizin está quebrada: o `.git` de `apps/web` não tem nenhum commit e 55 arquivos aparecem como staged-and-deleted. Faltam localmente todos os `app/**/page.tsx`, todo o `app/api/**`, `components/ui/*`, `lib/auth`, `lib/groq`, `lib/narrative-score`, `lib/supabase` e os ícones do PWA. `packages/db` está sem `prisma/schema.prisma` e sem `.git`.

O código íntegro vive em `github.com/yan1405/persona_mvp` e `github.com/yan1405/persona_db`, e na máquina do Yan.

> [!warning] Segurança
> Existem `apps/web/.env.local` e `packages/db/.env` com credenciais reais na pasta. Não commitar, não colar em chat, não subir para lugar nenhum.
