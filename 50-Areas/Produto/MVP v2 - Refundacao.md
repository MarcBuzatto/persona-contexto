---
id: area-mvp-v2-refundacao
type: area
title: "MVP v2 — refundação"
tags:
  - produto
  - tecnico
updated: 2026-08-18
---

# MVP v2 — refundação

Diretório `persona_mvp_v2`. Estado: **fundação e planejamento. Nenhum código do produto escrito, por decisão.** Contém apenas `AGENTS.md`, `docs/PRODUCT_BRIEF.md`, `docs/plans/2026-08-05-persona-live-design.md` e skills de design.

## Por que existe uma v2

A v1 foi construída em torno do Narrative Score e do Daily Log. O reposicionamento de 05/08/2026 (X-001) moveu o centro do produto para a [[Evidencia Profissional]] e o [[Persona Live]]. A v2 nasce desse novo centro, e não da correção incremental da v1.

Regra explícita: **não copiar automaticamente arquitetura, design, dívida técnica ou escopo da v1.** Reaproveitar só o que for confirmado como válido.

## Escopo

Dois entregáveis: uma **landing page** (explica problema, valor, funcionamento e diferencial; capta interesse) e uma **aplicação web** navegável e responsiva. As duas devem parecer o mesmo produto.

Fluxo prioritário: registrar experiência → transformar em evidência estruturada → consultar a biblioteca → informar uma pergunta no Persona Live → receber argumentos reais e rascunho curto, separados e rastreáveis.

## Restrições da fase

- Uso gratuito; sem cobrança, checkout ou billing real
- Sem integração direta com Meet, Zoom ou Teams
- Sem gravar nem persistir áudio de terceiros
- O modo Automático não pode comprometer a entrega do Manual funcional
- Design original: Notion é referência de **princípios** (clareza, edição contextual, estrutura modular, conteúdo primeiro), nunca modelo de cópia

## Direção obrigatória de design

Toda decisão visual usa as skills `editorial-modular-app-design` e `design-sem-cara-de-ia`. Antes de desenhar telas, é obrigatório fixar: referência de ancoragem, paleta semântica de 4 a 6 cores, papéis tipográficos, princípio de grid e espaçamento, voz da marca e um elemento-assinatura. "Moderno e limpo" não é direção.

Proibições padrão: gradiente roxo-índigo genérico, hero centralizado de altura total seguido de três cards iguais, sombras suaves indiscriminadas, componentes usados só por serem o default da stack, copy vaga tipo "tudo em um só lugar", movimento decorativo repetido.

## Bloqueios antes de escrever código

A implementação não pode começar até que estes itens sejam discutidos e aprovados:

- público prioritário e problema inicial mais específicos
- validação com usuários de que o fluxo evidência → argumentos → rascunho é útil
- mapa de páginas e fluxos da aplicação
- relação entre landing page, cadastro e experiência interna
- stack da v2 e estratégia de reaproveitamento da v1
- identidade visual atualizada
- função, personalidade e linguagem visual do mascote
- critérios de sucesso para banca e para testes com usuários

> [!note] Leitura estratégica
> Esse bloqueio é correto em termos de engenharia, mas cria um risco de calendário: faltando poucas semanas para 09/09/2026, o produto demonstrável da Semifinal continua sendo a v1 — que também não está publicada. Ver [[Pendencias e Riscos]].
