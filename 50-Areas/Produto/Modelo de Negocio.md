---
id: area-modelo-de-negocio
type: area
title: "Modelo de negócio"
tags:
  - produto
  - hipotese
updated: 2026-08-18
---

# Modelo de negócio

> [!warning] Tudo nesta página é hipótese
> Nenhum preço, limite de plano ou projeção foi validado com usuário real. Enquanto isso não mudar, apresentar como hipótese comercial — nunca como validação. Critério 6 do [[Criterios de Avaliacao]].

## Planos (decisão D-012, 14/07/2026)

| Plano | Preço | Features propostas |
|---|---|---|
| Free | R$ 0 | Registro diário, Narrative Score básico, 1 artefato/mês |
| Pro | R$ 29,90/mês | Artefatos ilimitados, relatório semanal automatizado |
| Premium | R$ 59,90/mês | Tudo do Pro + análise de mercado |
| Business | Sob consulta | Contas em equipe e RH, sem preço fixo exibido |

Nomenclatura anterior "Pro+ / B2B" e preços "R$ 29 / R$ 59" estão **[REVOGADO]** — aparecem em documentos antigos e devem ser corrigidos onde forem encontrados.

## Benchmark de preço (agosto de 2026)

| Referência | Preço mensal | Leitura |
|---|---:|---|
| LinkedIn Premium Career | R$ 159,90 | Teto de mercado, público de maior renda |
| ChatGPT Plus (BR) | R$ 119,90 | Mostra que o brasileiro paga por IA, mas é produto genérico |
| Notion Plus | ~R$ 51 | Cobrado por usuário em contexto de equipe |
| Canva Pro | R$ 26,90 a R$ 34,90 | **Benchmark mais próximo**: SaaS individual pago do próprio bolso |

Conclusão: R$ 29,90 é plausível para o público-alvo. **Isso é benchmark de mercado, não disposição a pagar.** Faixa provisória de teste para a pesquisa: R$ 24,90 a R$ 34,90.

## Estrutura de custos estimada

| Tipo | Item | Valor mensal |
|---|---|---:|
| Fixo | Vercel Pro | ~R$ 102 |
| Fixo | Supabase Pro | ~R$ 128 |
| Fixo | DAS do MEI | R$ 82 a R$ 87 |
| Variável | Groq API (por token) | R$ 50 a R$ 150, depende do uso |

Restrição inegociável (D-009): custo operacional abaixo de **R$ 1.500/mês**.

## Ponto de equilíbrio

Fórmula: custos fixos ÷ (preço − custo variável por usuário).
Cálculo: 315 ÷ (29,90 − 2,00) = 315 ÷ 27,90 ≈ **12 usuários pagantes/mês**.

## Projeção de faturamento em 12 meses

| Cenário | Usuários Free | Conversão | Pagantes | Receita mensal |
|---|---:|---:|---:|---:|
| Pessimista | 300 | 2% | 6 | R$ 179,40 |
| Realista | 600 | 3,5% | 21 | R$ 627,90 |
| Otimista | 1.200 | 5% | 60 | R$ 1.794,00 |

Taxas de conversão vindas de benchmark público de freemium B2C (2% a 5%). Números de usuários Free são metas de captação, não medição.

> [!note] Números antigos congelados
> Um resumo executivo de abril/2026 traz outros números — limites por plano (Free = 30 logs e 1 relatório/mês; Pro = 10 validadores), gatilho de conversão em 25 logs e MRR de R$ 17.400 com 600 assinantes. Decisão de Yan em 30/07/2026: **não usar nenhum desses números** até uma conversa dedicada (pendência C-14).
