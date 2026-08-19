---
id: moc-erros-a-nao-repetir
type: moc
title: "Erros a não repetir"
tags:
  - aprendizado
  - critico
updated: 2026-08-18
---

# Erros a não repetir

> [!tip] Índice
> Cada erro abaixo tem uma nota permanente própria e notas de feedback correspondentes em `50-Areas/Feedbacks/`. Consulte `90-Bases/Feedbacks.base`, visão "Pontos a melhorar", para a lista viva.

Notas permanentes derivadas: [[Validacao primaria nao e substituivel por pesquisa secundaria]] · [[Publico se define por gatilho, nao por faixa demografica]] · [[Produto sem unidade de valor central e uma lista de funcoes]] · [[Um numero sem fonte contamina todos os outros]] · [[Software nao publicado nao existe para efeito de avaliacao]] · [[Decisao revogada precisa ser corrigida em todos os documentos no mesmo dia]] · [[Honestidade calibrada e mais forte que promessa ampla]]

Lista curta, de propósito. Se uma IA ou um integrante novo ler só uma nota deste vault, que seja esta.

## 1. Deixar a validação para o fim do cronograma

**O que aconteceu:** no [[Invest AI]], a validação com público-alvo estava na semana 10 de 14. Não foi feita. O projeto foi para a banca sem uma única entrevista.

**Onde estamos repetindo:** no [[Persona]], a validação está marcada como crítica desde 22/04/2026 (decisão D-008: "priorizar validação com usuários antes de qualquer código"). Em 18/08/2026, quatro meses depois, continua em zero — e muito código foi escrito nesse meio-tempo.

**Regra:** validação não é etapa, é pré-requisito. Nenhuma semana de trabalho deveria terminar sem pelo menos uma conversa com uma pessoa real do público-alvo.

## 2. Confundir "dado de mercado" com "evidência de cliente"

**O que aconteceu:** citar IBGE, CNC e Banco Central é responder "esse problema existe?". A banca pergunta outra coisa: "**essas pessoas específicas querem isso e pagariam por isso?**".

**Regra:** para cada número macro no documento, exigir um dado micro correspondente. TAM sem entrevista é metade da resposta.

## 3. Acumular funcionalidade em vez de aprofundar uma

**O que aconteceu:** seis módulos no Invest AI, nenhum insubstituível.

**Regra:** antes de adicionar qualquer função, perguntar se ela fortalece a unidade de valor central ou só aumenta a superfície. No Persona, a unidade é a [[Evidencia Profissional]].

## 4. Publicar número otimista sem lastro

**O que aconteceu:** 8% de conversão apresentado como conservador, contra um benchmark real de 2% a 5%.

**Regra:** todo número tem fonte ao lado, ou a palavra "hipótese" ao lado. Não existe terceira opção.

## 5. Construir produto que ninguém consegue abrir

**O que está acontecendo agora:** o MVP v1 do Persona é funcional, tem backend real, auth real, IA real e PWA — e **nunca foi publicado**. Sem URL, ninguém testa, ninguém valida, a banca não vê funcionando.

**Regra:** deploy é entrega, não polimento. Um produto que só roda no notebook de um integrante, para efeito de avaliação, não existe.

## 6. Deixar a documentação divergir da realidade

**O que aconteceu:** documentos do Persona circularam por semanas citando Claude Sonnet, OpenAI e pgvector depois de todos terem sido substituídos; a nomenclatura de planos "Pro+/B2B" sobreviveu em arquivos usados para apresentação.

**Regra:** ao revogar uma decisão, corrigir no mesmo dia todos os documentos que a citam, ou marcar visivelmente como desatualizados.

## 7. Prometer o que o produto não faz

**Risco atual:** o modo Automático do [[Persona Live]] e a integração com Meet, Zoom e Teams. Um slide entusiasmado vira, na banca, uma pergunta que a equipe não consegue responder — e a credibilidade do resto vai junto.

**Regra:** dizer "no MVP, X é funcional e Y é demonstração controlada" é mais forte do que insinuar que tudo funciona. Bancas premiam honestidade calibrada.

## 8. Escrever o Sumário Executivo antes do resto

O próprio Guia Rápido do Empreenda avisa: escrever o sumário antes de terminar as outras seções transforma o documento em lista de intenções. Ele é o **último** a ser escrito, não o primeiro.

## 9. Parecer um negócio já constituído

**O que aconteceu:** o feedback oficial de 2026 apontou indícios de que o Persona já estaria operando com CNPJ, vendas e clientes ativos — situação que o regulamento não aceita e que leva à desclassificação.

**Por que é fácil cair nisso:** quanto melhor o produto e a marca, mais o projeto parece empresa. Somado a isso, o próprio Portfólio listava "abrir MEI" como próximo passo e já contabilizava o DAS nos custos fixos.

**Regra:** enquanto a competição estiver em curso, o material deve deixar explícito o estágio real — protótipo, sem cobrança ativa, sem cliente pagante — e tratar formalização como passo futuro condicionado. Não abrir MEI ou CNPJ antes do fim da competição.

Ver [[C-19 Eliminar indicios de negocio em operacao]].
