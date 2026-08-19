---
id: note-convencoes-do-vault
type: note
title: "Convenções do vault"
tags:
  - meta
updated: 2026-08-18
---

# Convenções do vault

## Nomes de arquivo

Sem acentos e sem caracteres especiais, para não quebrar links entre sistemas operacionais. O título com acento vai no campo `title` do frontmatter e no H1 da nota.

## Frontmatter

Toda nota começa com:

```yaml
---
title: Título legível
tags: [tag1, tag2]
atualizado: AAAA-MM-DD
---
```

## Tags em uso

`meta`, `projeto`, `produto`, `competicao`, `equipe`, `decisao`, `pendencia`, `aprendizado`, `referencia`, `registro`, `hipotese`, `critico`

## Marcação de confiança

Toda afirmação carrega um destes marcadores quando não for óbvia:

- **[FATO]** — verificável em documento, código ou fonte citada
- **[HIPÓTESE]** — plausível, mas sem evidência
- **[PENDENTE]** — falta fazer
- **[REVOGADO]** — decisão que não vale mais, mantida por rastreabilidade

Nunca apague uma informação errada: marque como revogada e explique o porquê. O histórico de erro é tão útil quanto o acerto.

## Identificadores

- `D-NNN` — decisão de produto
- `C-NN` — pendência do track competição
- `P-NN` — pendência do track produto
- `X-NNN` — decisão cruzada, que afeta os dois tracks

A numeração é sequencial e nunca reutilizada.

## Relacionado

[[Como usar este vault (IA)]] · [[00 COMECE AQUI]]
