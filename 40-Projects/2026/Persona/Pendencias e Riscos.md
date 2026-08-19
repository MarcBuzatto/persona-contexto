---
id: note-pendencias-e-riscos
type: note
title: "Pendências e riscos"
project: "[[Persona]]"
year: 2026
tags:
  - pendencia
  - critico
updated: 2026-08-18
---

# Pendências e riscos

Estado em 18/08/2026. Prazo da Semifinal: **09/09/2026** — restam cerca de 3 semanas.

## Risco de desclassificação (acima de tudo)

> [!danger] C-19 vem antes de qualquer outra coisa
> O feedback oficial da Fase Inicial registrou **indícios de que o negócio já estaria em operação formal**, o que o regulamento não aceita. O avaliador escreveu que, nesse caso, a equipe poderá ser desclassificada na próxima fase. Ver [[C-19 Eliminar indicios de negocio em operacao]] e [[F-2026-13 ALERTA de indicios de negocio ja em operacao]].
>
> O ponto mais urgente é interno: a seção 8.1 do Portfólio lista "abrir MEI" como ação necessária e a 7.3 já traz o DAS do MEI nos custos fixos. Isso está no documento que será entregue.

## Bloqueio raiz

> [!danger] Uma coisa trava quatro critérios
> Não existe **nenhuma** entrevista, teste de protótipo ou pesquisa de disposição a pagar. Isso trava sozinho os critérios 2, 4, 5 e 6, as seções 3 e 4 do Portfólio e o slide 8 do Pitch Deck. Toda a documentação está pronta para receber esses dados; falta só ir a campo.

## Track Competição

| ID | Pendência | Prioridade |
|---|---|---|
| C-01 | Plano de validação com usuários reais (10 a 15 entrevistas semiestruturadas) | **Crítica** |
| C-02 | Roteiro de entrevistas | Alta |
| C-03 | Landing page de interesse com captura de e-mail (meta: 200 em 30 dias) | Alta |
| C-04 | Texto de amarração com ODS 4 e ODS 8 | Alta |
| C-10 | Montar o Pitch Deck (existe roteiro, não existe arquivo) | Alta |
| C-15 | Equipe cadastrada no portal como **"Personar"** e não "Persona" — afeta a capa dos dois entregáveis | **Alta** |
| C-16 | Escrever o Plano Empreendedor completo — bloqueado mais pela falta de validação do que pela escrita | **Crítica** |
| C-17 | Validar se argumentos reais + rascunho curto ajudam de fato durante entrevista, sem distrair | **Crítica** |
| C-21 | **Regularizar a composição da equipe** — o Portfólio lista 6 integrantes, o portal tem 2, o regulamento permite 4 | **Crítica — capa e conformidade** |
| C-22 | Consumir o Empreenda Flix (progresso atual: **0,00%** de 29 vídeos) e entrar nos plantões ao vivo | Alta |
| C-23 | Termo de Autorização de menores até 03/11/2026 — não entregar desclassifica | Alta |
| C-24 | Corrigir o setor da ideia no portal (hoje: "Construção Civil") | Média |
| C-19 | **Eliminar indícios de negócio em operação** — reescrever seções 7.3 e 8.1 do Portfólio, confirmar ausência de CNPJ/MEI | **Crítica — desclassificação** |
| C-20 | Tornar concreta a explicação da solução — sair do "vago" para o "específico", conforme orientação repetida pelos avaliadores | Alta |
| C-18 | Atualizar Portfólio, Pitch Deck e Vídeo para o novo posicionamento, sem prometer integração com Meet/Zoom/Teams | Alta |
| C-14 | Números de negócio do resumo executivo antigo estão congelados por decisão — não usar até conversa dedicada | Aguardando decisão |

## Track Produto

| ID | Pendência | Prioridade |
|---|---|---|
| P-05 | Nenhuma validação com usuários registrada | **Alta** |
| P-08 | **Nenhum deploy em produção** — sem URL pública, sem teste real, sem demonstração para a banca | **Alta — maior gap técnico** |
| — | Cópia local de `persona_v1` incompleta (55 arquivos ausentes) — ver [[MVP v1 - Estado Tecnico]] | Média |
| — | Revisão jurídica de Termos e Política de Privacidade | Alta antes de usuário externo |
| — | Testes automatizados inexistentes; 9 vulnerabilidades de `npm audit` sem tratamento | Média |
| — | Paywall promete features que não existem (relatório semanal, análise de mercado) | Média |

## Riscos de calendário

1. **Três semanas para o prazo, com quatro entregas em aberto** (validação, Portfólio finalizado, Pitch Deck, vídeo novo) e capacidade de 5 a 10 horas semanais por pessoa.
2. **O MVP v2 está bloqueado por decisão** até aprovar público, validação e stack — o que significa que o produto demonstrável na Semifinal continua sendo a v1, que não está publicada.
3. **O vídeo da Fase Inicial provavelmente não serve mais**, e regravar exige roteiro, gravação, edição e revisão — não é tarefa de última hora.

## Ordem sugerida de ataque

0. **C-19** (indícios de operação) e **C-21** (composição da equipe) — são conformidade, não conteúdo, e ambas podem custar a competição inteira. Resolvem-se em horas, não semanas.
0.5. **C-22** — a trilha Plano Empreendedor do Empreenda Flix cobre exatamente as seções fracas, e o custo é só tempo de assistir.
1. Entrevistas — mesmo que sejam 8 ou 10 em vez de 15. Uma entrevista real vale mais que zero, e o Portfólio já tem onde encaixar.
2. Publicar a v1 em produção. Sem isso não há teste de protótipo possível.
3. Teste de protótipo com quem já foi entrevistado.
4. Pesquisa de preço junto com o teste.
5. Só então fechar Portfólio, Pitch Deck e vídeo, já com dados reais.

> [!tip] Por que essa ordem
> As seções 3, 4 e o slide 8 são as únicas que **não dá para escrever antes** — o resto do material já existe e só precisa de revisão. Inverter a ordem é o erro clássico: chegar no dia 08/09 com um documento bonito e a seção de validação vazia.
