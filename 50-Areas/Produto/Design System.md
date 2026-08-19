---
id: area-design-system
type: area
title: "Design System"
tags:
  - produto
  - design
updated: 2026-08-18
---

# Design System v0.1

Definido em 26/04/2026. Pacote original conferido arquivo por arquivo em 28/07/2026 — os tokens reconstruídos batem exatamente com os originais.

## Os três princípios

**1. A cor é o personagem, o branco é o palco.**
O roxo `#7C3AED` aparece em botões, labels, badges — nunca como fundo de superfície grande. Antes de usar, perguntar: *estou usando o roxo como ator ou como cenário?* Se for cenário, está errado.

**2. O que acumula é mensurável; o que é mensurável tem rigor tipográfico.**
Plus Jakarta Sans para prosa e narrativa. JetBrains Mono para métricas, scores e dados auditáveis. As duas nunca se misturam na mesma linha.

**3. O sistema responde, não decora.**
Animações e sombras só em resposta a ação do usuário ou mudança de estado. Partículas, gradientes mesh e brilhos são proibidos.

## Tokens de cor

| Token | Hex | Uso |
|---|---|---|
| indigo-500 | `#7C3AED` | CTA primário, núcleo do logo |
| indigo-700 | `#5B21B6` | Hover, texto de ênfase |
| slate-50 | `#FAFAFC` | Fundo de página |
| slate-900 | `#1A1726` | Texto primário |

## Tokens de tipografia

| Estilo | Família | Peso | Tamanho |
|---|---|---|---|
| Display | Plus Jakarta Sans | 800 | 42px |
| Heading 1 | Plus Jakarta Sans | 800 | 28px |
| Body | Plus Jakarta Sans | 400 | 15px |
| Mono impacto | JetBrains Mono | 500 | 44px |
| Mono tabular | JetBrains Mono | 500 | 18px |

## Logo

Logo Constellation, com versionamento rica e compacta. Cinco das seis artes SVG estão recuperadas: `persona-logo-rica`, `persona-logo-rica-dark`, `persona-logo-compacta`, `persona-logo-mono`, `persona-lockup-h`. **[PENDENTE]** `persona-lockup-v.svg` nunca foi localizado — hipótese é que nunca chegou a ser gerado.

## Mascote Xisto

Baseado no ícone de rede neural e constelação da própria logo, não em um personagem novo desconectado da marca. Tom de voz: informal, direto, acolhedor; frases curtas; orienta e comemora, nunca alerta nem pressiona.

Regra de aparição: Xisto aparece **só em resposta a um estado específico**, nunca como enfeite fixo. Qualquer nova aparição exige justificativa registrada.

**[PENDENTE]** No MVP v2 a identidade e o papel do mascote voltaram a ser questão aberta — Xisto é opção em discussão, não decisão fechada.

## Aplicação no Pitch Deck

O regulamento do Empreenda exige padrão de cores e tipografia consistentes, fontes grandes (mínimo 24pt) e mais visual que texto. O Design System resolve isso diretamente — usar sem reinventar.

## Relacionado

[[Persona]] · [[Entregaveis da Semifinal]] · [[MVP v1 - Estado Tecnico]]
