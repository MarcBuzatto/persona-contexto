---
id: task-2026-p-08
type: task
title: "Publicar o MVP em producao"
project: "[[Persona]]"
year: 2026
status: todo
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

Build de produção nunca rodado; variáveis reais precisam ser inseridas por quem tem acesso.
