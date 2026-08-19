---
id: proj-2026-persona
type: project
title: "Persona"
year: 2026
status: active
deadline: 2026-11-26
tags:
  - projeto
  - produto
  - competicao
updated: 2026-08-18
---

# Persona

Projeto atual da equipe no **Empreenda Senac 19ª edição (2026)**, categoria Ensino Médio Técnico. Meta declarada: 1º lugar (prêmio de R$ 35.000).

> [!info] Em uma frase
> O Persona é um sistema de evidências profissionais: registra experiências reais, transforma em evidências estruturadas e recupera os argumentos certos no momento em que a pessoa precisa provar competência.

Proposta institucional: *O sistema operacional da sua identidade profissional.*
Promessa funcional: *Registre uma vez. Prove sempre.*
Frase de diferenciação: *O Persona não começa pela resposta. Começa pela evidência.*

## Índice do projeto

- Produto: [[Definicao do Produto]] · [[Evidencia Profissional]] · [[Persona Live]] · [[Modelo de Negocio]] · [[Design System]]
- Técnico: [[MVP v1 - Estado Tecnico]] · [[MVP v2 - Refundacao]]
- Competição: [[Empreenda Senac]] · [[Entregaveis da Semifinal]] · [[Criterios de Avaliacao]] · [[Feedback dos Avaliadores]]
- Gestão: [[Equipe]] · [[Registro de Decisoes]] · [[Pendencias e Riscos]] · [[Linha do Tempo]]
- Mercado: [[Concorrentes]] · [[Dados e Fontes]]

## Estado em 18/08/2026

| Frente | Situação |
|---|---|
| Posicionamento | **[FATO]** Redefinido em 05/08/2026 (decisão X-001): sistema de evidências profissionais, com o [[Persona Live]] como diferencial |
| Fase da competição | **[FATO]** Classificados para a Semifinal. Entrega em **09/09/2026, 21h** |
| Portfólio de Evidências | **[FATO]** Estruturado nas 10 seções oficiais, com blocos [PENDENTE] nas seções 3 e 4 |
| Pitch Deck | **[PENDENTE]** Existe o roteiro de 12 slides (v1.2), não existe o arquivo montado |
| Vídeo de Apoio | **[PENDENTE]** O vídeo da Fase Inicial provavelmente não reflete mais o produto — precisa de regravação |
| Validação com usuários | **[CRÍTICO]** Zero entrevistas, zero testes de protótipo, zero pesquisa de preço concluída |
| MVP v1 | **[FATO]** Funcional em ambiente local, nunca publicado — sem deploy em produção |
| MVP v2 | **[FATO]** Só documentação e planejamento; nenhum código escrito, por decisão |

## Os dois gargalos que decidem a nota

1. **Ausência de validação primária.** Trava o critério 4, as seções 3 e 4 do Portfólio e o slide 8 do Pitch Deck. É a mesma falha que derrubou o [[Invest AI]] — ver [[Erros a Nao Repetir]].
2. **Ausência de produto publicado.** Sem URL pública, a banca não testa e os usuários não validam. Ver [[MVP v1 - Estado Tecnico]].

## Feedbacks associados ao projeto

```dataview
TABLE date, author, sentiment, status, criterio
FROM "40-Projects/2026/Persona/Feedbacks" OR "50-Areas/Feedbacks"
WHERE project = [[Persona]]
SORT sentiment ASC, date DESC
```

## Tarefas em aberto

```dataview
TABLE deadline, prioridade, track, criterio, status
FROM "40-Projects/2026/Persona/Tarefas"
WHERE status != "done"
SORT deadline ASC
```

> Blocos Dataview exigem o plugin da comunidade instalado. As mesmas visões existem, de forma nativa, em `50-Areas/Feedbacks/Feedbacks-2026.base` e `60-Resources/Bases/Tarefas.base`.

## Os dois tracks

O projeto sempre correu em dois trilhos interdependentes:

- **Track Produto** — construir o MVP real.
- **Track Competição** — vencer o Empreenda Senac.

Regra fixa: quando há conflito, **a competição vence**. O que se constrói no produto vira evidência pontuada na competição.
