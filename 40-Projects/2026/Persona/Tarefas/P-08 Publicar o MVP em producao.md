---
id: task-2026-p-08
type: task
title: "Publicar o MVP em producao"
project: "[[Persona]]"
year: 2026
status: blocked
deadline: 2026-08-25
prioridade: alta
track: produto
criterio: 7
tags:
  - tarefa
  - empreenda-senac
---

# P-08 — Publicar o MVP em producao

## O que precisa acontecer

Deploy do `apps/web` na Vercel, com variáveis de ambiente reais, URL pública funcionando e URL de redirect do Supabase apontando para produção.

## Por que importa

Sem URL não há teste de protótipo com usuário, não há demonstração para a banca e o critério 7 fica sustentado só por relato. Ver [[F-2026-02 Produto funcional que ninguem consegue abrir]].

## Definição de pronto

Uma pessoa fora da equipe abre o link em outro aparelho, cria conta, registra um log e gera um artefato.

## Bloqueado por

[FATO] Em 28/10/2026, a produção existente continua no commit `06de045`; o candidato com integração NVIDIA está em Preview, não em Production. O build e os testes locais passaram, mas a inferência `z-ai/glm-5.3-flash` não respondeu em até 90 s. O host do Supabase configurado respondeu NXDOMAIN em resolvedores públicos, e o Dashboard exige login para confirmar se o projeto está pausado ou removido. Login Microsoft, persistência e jornadas autenticadas não foram validados nesta rodada.

Não promover o candidato enquanto esses bloqueios permanecerem. Não aplicar a migração da Fase 9 sem seu checkpoint de banco.

## Atualização verificável — 28/10/2026

- [FATO] Preview da branch `codex/persona-preview-20261028`, commit `9c5ce5c`, terminou `READY`; a [tela pública de entrada](https://persona-mvp-v2-git-codex-4430dd-yanguiilhermed42-1689s-projects.vercel.app/) respondeu HTTP 200 e mostrou o login Microsoft.
- [FATO] Isso não comprova callback OAuth, sessão autenticada, persistência, RLS ou chamada do agente.
- [PENDENTE] Yan confirmar no Dashboard Supabase o estado do projeto `pnztzmobiwlblzxcqjna` e reativá-lo somente se a ação não exigir upgrade/custo.
- [PENDENTE] Obter inferência NVIDIA bem-sucedida com chave rotacionada; a chave enviada anteriormente deve ser rotacionada pelo titular e não foi configurada na Vercel. Evidências e plano: [plano operacional no branch de Preview](https://github.com/yan1405/persona_mvp_V2/blob/codex/persona-preview-20261028/docs/plans/2026-10-28-plano-colocar-persona-online.md).
- [PENDENTE] Depois dos bloqueios, executar o fluxo autenticado sintético e cumprir a definição de pronto acima antes de alterar Production.
