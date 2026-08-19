---
id: area-persona-live
type: area
title: "Persona Live"
tags:
  - produto
  - decisao
updated: 2026-08-18
---

# Persona Live

O diferencial demonstrável do produto. Design funcional aprovado em 05/08/2026 (decisão X-001), fonte: `persona_mvp_v2/docs/plans/2026-08-05-persona-live-design.md`. **Implementação ainda não iniciada.**

## O que é

Assistente de argumentação para entrevistas, baseado **exclusivamente** nas experiências e evidências autorizadas pelo usuário. Exibe ao mesmo tempo, em áreas separadas:

| Painel | Conteúdo |
|---|---|
| **Argumentos reais** | Experiência recomendada, contexto, ação do usuário, resultado, competências, provas de origem, lacunas e alertas |
| **Rascunho sugerido** | Resposta curta em linguagem natural, montada só a partir dos argumentos acima |

O sistema **não responde pelo usuário**. A interface favorece compreensão rápida e fala natural, não leitura literal.

## Por que essa forma, e não outra

Três abordagens foram consideradas:

- **A. Resposta completa escondida** — alta percepção de impacto, mas genérica, eticamente frágil e parecida com copilotos que prometem respostas indetectáveis. **Rejeitada.**
- **B. Apenas tópicos de evidência** — autêntica e simples, mas insuficiente para quem trava ao transformar fato em resposta. **Não escolhida sozinha.**
- **C. Argumentos e rascunho separados** — equilibra autenticidade e apoio prático. **Aprovada.**

## Regra de extensão

| Tipo de pergunta | Duração alvo |
|---|---:|
| Objetiva | 15 a 25 segundos |
| Comportamental ou STAR | 30 a 45 segundos |
| Complexa | até 60 segundos |

Respostas de 90 segundos nunca são geradas automaticamente. Controles disponíveis: `Encurtar`, `Aprofundar` e `Outra experiência`. `Aprofundar` só adiciona fatos já disponíveis — nunca inventa nem busca fora.

Estrutura mínima do rascunho: contexto em uma frase, ação do usuário, resultado e, só quando relevante, aprendizado.

## Dois modos

| Modo | O que faz | Status no MVP |
|---|---|---|
| **Manual** | O usuário digita, cola ou seleciona a pergunta. Não captura a voz do entrevistador. | **Funcional** |
| **Automático** | Transcreve temporariamente a conversa, identifica uma possível pergunta e prepara a assistência. Exige autorização. | **Demonstração controlada** |

> [!danger] Limite de comunicação
> Não afirmar, em nenhum documento, vídeo ou slide, que a integração produtiva com Google Meet, Zoom ou Microsoft Teams já existe. Isso é versão futura, sujeita a validação técnica e de privacidade.

## Estados e falhas previstos

| Situação | Comportamento esperado |
|---|---|
| Pergunta não compreendida | Permitir correção ou entrada manual |
| Baixa confiança na detecção | Não gerar automaticamente; pedir confirmação |
| Nenhuma evidência relacionada | Informar a lacuna; não inventar |
| Mais de uma experiência forte | Mostrar a principal e permitir `Outra experiência` |
| Falha de áudio | Pausar escuta e manter o modo Manual disponível |
| Falha de geração | Preservar pergunta e argumentos para tentar de novo |
| Fato sem fonte correspondente | Remover do rascunho e sinalizar inconsistência |
| Conexão interrompida | Manter o conteúdo exibido; não prometer processamento contínuo |

## Critérios de aceitação

1. Argumentos e rascunho aparecem simultaneamente e separados.
2. Cada afirmação do rascunho corresponde a um argumento visível.
3. Argumentos mostram sua evidência de origem.
4. O sistema não cria números, responsabilidades ou resultados ausentes.
5. A resposta inicial respeita a faixa curta adequada à pergunta.
6. `Aprofundar` não adiciona fatos externos.
7. `Outra experiência` troca a base e atualiza os dois painéis.
8. Nenhuma evidência encontrada produz um estado honesto, não uma resposta genérica.
9. Falha do modo Automático preserva acesso ao Manual.
10. Encerrar a sessão descarta a transcrição temporária por padrão.

## O que ainda precisa ser validado

Se argumentos reais e rascunho curto, exibidos separadamente, **ajudam de fato** durante a preparação ou a realização de uma entrevista, sem distrair nem incentivar leitura literal. Essa é a pendência C-17 em [[Pendencias e Riscos]] — e sem ela o diferencial é uma aposta, não um resultado.
