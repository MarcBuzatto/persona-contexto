# AGENTS.md — Guia para IAs que vão usar e alimentar esta base

> **Você é uma IA (Claude, ChatGPT, Gemini, Codex, Copilot ou outra) e recebeu acesso a este cofre Obsidian.** Este arquivo ensina, do zero, como ler, contribuir e não estragar nada. É autossuficiente: você não precisa de plugin, skill ou ferramenta especial para seguir estas regras.
>
> Se você é o Claude Code, leia também `CLAUDE.md` — ele tem a governança completa. Este arquivo é a versão operacional e agnóstica de ferramenta.
>
> Versão 1.0 · 18/08/2026 · Idioma de trabalho: português do Brasil.

---

## 1. O que é esta base, em 30 segundos

Memória permanente da equipe **Persona**, do curso Técnico em Inteligência Artificial do **Senac Lapa Tito**, que compete no **Empreenda Senac**.

Ela guarda dois projetos: o **Persona** (2026, em andamento) e o **Invest AI** (2025, que não passou para a final). A base existe para que a equipe não repita, na edição seguinte, o erro que custou a anterior — e para que qualquer IA que entre no meio do caminho saiba exatamente onde as coisas estão.

Comece lendo, nesta ordem: `00 COMECE AQUI.md` → `40-Projects/2026/Persona/Persona.md` → `40-Projects/2026/Persona/Pendencias e Riscos.md`.

---

## 2. Cinco regras inegociáveis

**1. Nunca invente.** Entrevista, depoimento, citação, número, resultado, fonte ou data que você não viu, não existe. Se falta informação, escreva `[PENDENTE]` e diga o que falta. Esta base alimenta documentos entregues a uma banca avaliadora — um dado inventado aqui vira fraude lá.

**2. Separe fato de hipótese.** Use os marcadores no corpo do texto:

| Marcador | Quando usar |
|---|---|
| `[FATO]` | Verificável em documento, código, print ou fonte citada |
| `[HIPÓTESE]` | Plausível, mas sem evidência ainda |
| `[PENDENTE]` | Falta fazer ou falta descobrir |
| `[REVOGADO]` | Não vale mais — mantido por rastreabilidade |

**3. Nada é apagado.** Informação que perdeu validade é marcada `[REVOGADO]` com o motivo e a data. O histórico de erro tem tanto valor quanto o de acerto — é literalmente o propósito desta base.

**4. Toda nota precisa de pelo menos um wikilink no formato `[[nome-da-nota]]`.** Nota órfã não aparece no grafo e some na prática. Se não souber a quem ligar, ligue ao MOC `[[00 COMECE AQUI]]` ou à nota central do projeto.

**5. Sem emoji.** Em nota nenhuma, em material nenhum. Se precisar de ícone, use SVG. Português do Brasil no texto; termos técnicos consagrados ficam em inglês.

---

## 3. Como se orientar sem gastar contexto à toa

**Leia o frontmatter, não a nota inteira.** Toda nota tem um bloco YAML nas primeiras linhas com `type`, `title`, `status`, `sentiment`, `prioridade` e afins. Em varredura ou triagem, leia **só as 10 primeiras linhas** de cada arquivo. Abra a nota inteira apenas quando (a) souber que é aquela, (b) for editá-la, ou (c) precisar citar um trecho literal.

**Antes de sair buscando, veja se já existe uma tabela pronta.** Os arquivos `.base` são bancos de dados dinâmicos que leem o YAML das notas:

| Base | Responde |
|---|---|
| `50-Areas/Feedbacks/Feedbacks-2026.base` | O que está indo bem e mal em 2026, por projeto, autor e critério |
| `50-Areas/Feedbacks/Feedbacks-2025.base` | O mesmo para a edição anterior — serve para comparar |
| `60-Resources/Bases/Tarefas.base` | Backlog por prioridade, track e prazo |
| `60-Resources/Bases/Notas.base` | Panorama de todas as notas por tipo e data |

Se você não consegue renderizar `.base` (é um recurso do app Obsidian), leia o arquivo como YAML: os filtros dizem exatamente que campos importam.

---

## 4. Onde colocar cada coisa

| Se você tem... | Coloque em | `type` |
|---|---|---|
| Uma anotação bruta que ainda não sabe classificar | `00-Inbox/` | `note` |
| Um insight rápido, pensamento solto | `10-Fleeting/` | `note` |
| Resumo de fonte externa (regulamento, artigo, benchmark, vídeo) | `20-Literature/` | `literature` |
| Uma ideia atemporal, que vale mesmo em outro projeto | `30-Permanent/` | `permanent` |
| Feedback sobre um projeto específico | `40-Projects/<ano>/<projeto>/Feedbacks/` | `feedback` |
| Algo a fazer | `40-Projects/<ano>/<projeto>/Tarefas/` | `task` |
| Snippet, anexo ou referência do projeto | `40-Projects/<ano>/<projeto>/Arquivos/` | `note` |
| Conhecimento contínuo sobre produto, competição ou equipe | `50-Areas/<área>/` | `area` |
| Feedback que não é de um projeto só | `50-Areas/Feedbacks/` | `feedback` |
| Dado com fonte, análise de concorrente, referência geral | `60-Resources/` | `resource` |
| Material de ano encerrado que não serve nem de aprendizado | `70-Archives/<ano>/` | qualquer |

**Na dúvida entre `00-Inbox` e o lugar certo:** use `00-Inbox`. É melhor uma nota bruta no lugar temporário certo do que uma nota mal classificada no lugar definitivo errado. Mas avise o humano que deixou algo na Inbox.

**Projeto encerrado não vai para `70-Archives`.** Ele fica em `40-Projects/<ano>/` com `status: archived`, porque o valor dele vira comparação histórica. Só arquive o que não ensina nada.

---

## 5. Receitas passo a passo

Cada receita abaixo é copiável. Substitua o que está entre `<>`.

### 5.1 Registrar um feedback

O caso mais comum. Feedback pode vir de avaliador da competição, mentor, usuário testado ou da própria equipe se autoavaliando.

**Regra de ouro:** um ponto por nota. Se o feedback recebido tem cinco pontos, são cinco notas. Isso é o que permite filtrar por sentimento e critério depois.

1. Escolha a pasta: feedback do Persona vai em `40-Projects/2026/Persona/Feedbacks/`; do Invest AI, em `40-Projects/2025/Invest-AI/Feedbacks/`.
2. Nome do arquivo: `F-<ano>-<NN> <titulo sem acento>.md`, com `NN` sequencial dentro daquele ano (olhe o último e some 1).
3. Cole o modelo:

```yaml
---
id: fb-2026-09-persona
type: feedback
title: "Titulo curto do ponto"
project: "[[Persona]]"
date: 2026-09-15
year: 2026
author: "Nome de quem deu o feedback"
role: "Banca avaliadora"
sentiment: "Mal"
status: "Pendente"
criterio: 4
tags:
  - feedback
  - empreenda-senac
---
```

4. Escreva o corpo com estas três seções, sempre:

```markdown
# Titulo curto do ponto

## O que está indo mal (ponto de dor)

O que foi dito, em texto reescrito com clareza — não copie e cole bruto.
Se houver citação literal do avaliador, use bloco de citação.

## Leitura

O que isso significa na prática para o projeto.

## Plano de ação / próximos passos

O que será feito. Se exigir trabalho, crie também uma tarefa e linke aqui.

## Relacionado

[[Criterios de Avaliacao]] · [[Persona]]
```

Se `sentiment` for `"Bom"`, troque o título da primeira seção para `## O que está indo bem (ponto positivo)` e, no plano de ação, escreva como **repetir** aquilo na edição atual.

**Valores permitidos:**

- `sentiment` — estritamente `"Bom"` ou `"Mal"`. Não invente nível intermediário; nuance vai no corpo.
- `status` — `"Pendente"`, `"Em Análise"` ou `"Resolvido"`.
- `role` — `"Banca avaliadora"`, `"Mentor"`, `"Usuário"`, `"Autoavaliação da equipe"`.
- `criterio` — número de 1 a 9 do critério do Empreenda que o ponto afeta, ou `0` se não se aplica. A lista está em `[[Criterios de Avaliacao]]`.

### 5.2 Criar uma tarefa

1. Pasta: `40-Projects/2026/Persona/Tarefas/`.
2. Nome: `<ID> <titulo sem acento>.md`. O ID segue a numeração existente: `C-` para competição, `P-` para produto, `X-` para cruzada. Olhe a pasta e use o próximo número livre.

```yaml
---
id: task-2026-c-19
type: task
title: "Titulo da tarefa"
project: "[[Persona]]"
year: 2026
status: todo
deadline: 2026-09-09
prioridade: alta
track: competicao
criterio: 4
tags:
  - tarefa
  - empreenda-senac
---
```

3. Corpo:

```markdown
# C-19 — Titulo da tarefa

## O que precisa acontecer

Descreva o resultado esperado, não a tarefa. "Portfólio com a seção 3 preenchida"
é melhor que "trabalhar no portfólio".

## Por que importa

Qual critério, entregável ou risco está preso nisto.

## Definição de pronto

Como saber, sem ambiguidade, que acabou.

## Bloqueado por

O que precisa existir antes. Se nada, escreva "nada".

## Relacionado

[[Pendencias e Riscos]]
```

**Valores permitidos:** `status` em `todo`, `doing`, `blocked`, `paused`, `done`. `prioridade` em `critica`, `alta`, `media`, `baixa`. `track` em `competicao`, `produto`, `ambos`.

### 5.3 Registrar uma decisão

Decisões **não** viram nota nova: elas entram como linha na tabela de `40-Projects/2026/Persona/Registro de Decisoes.md`.

1. Pegue o próximo ID livre: `D-NNN` para produto, `X-NNN` para decisão que afeta produto e competição ao mesmo tempo. **Nunca reutilize um número**, mesmo de decisão revogada.
2. Adicione a linha com ID, decisão, data e situação.
3. Se a decisão nova **revoga** uma antiga, edite a linha antiga para `**[REVOGADO]** por D-NNN` — não apague.
4. Se a decisão contradiz algo escrito em outra nota, corrija a outra nota **na mesma sessão**. Documentação divergente é um erro conhecido desta equipe — ver `[[Decisao revogada precisa ser corrigida em todos os documentos no mesmo dia]]`.

### 5.4 Criar uma nota permanente (Zettelkasten)

Use quando aprender algo que continua verdadeiro **fora** deste projeto. É o conteúdo mais valioso da base a longo prazo.

1. Pasta: `30-Permanent/`.
2. Nome do arquivo = a própria ideia, escrita como afirmação: `Software nao publicado nao existe para efeito de avaliacao.md`.

```yaml
---
id: perm-nome-em-slug
type: permanent
title: "A ideia, em uma frase afirmativa"
origem: "[[nome-da-nota-de-origem]]"
tags:
  - permanent
updated: 2026-09-15
---
```

3. Corpo obrigatório: a afirmação em uma frase, depois `## Por quê` (o raciocínio ou a evidência), depois `## Contraponto` (quando essa ideia **não** vale — toda regra tem borda), depois `## Relacionado`.

**Uma ideia por nota.** Se o título precisa de "e", são duas notas.

### 5.5 Registrar uma fonte externa

1. Pasta: `20-Literature/`.

```yaml
---
id: lit-nome-em-slug
type: literature
title: "Título da fonte"
fonte: "Nome da publicação ou site"
autor: "Autor"
ano: 2026
url: https://exemplo.com
tags:
  - literature
updated: 2026-09-15
---
```

2. Corpo: `## Resumo` (com suas palavras, nunca copiado), `## Trechos relevantes` (aí sim literal, em bloco de citação), `## O que isso muda para nós` e `## Notas permanentes geradas`.

3. **Se a fonte trouxer número que vá para documento da competição**, adicione também a `60-Resources/Dados e Fontes.md`, com valor, fonte e ano. Número que não está naquela tabela não pode ser usado em entregável.

### 5.6 Captura rápida

Não sabe onde vai? `00-Inbox/` com frontmatter mínimo:

```yaml
---
id: note-slug-do-assunto
type: note
title: "Assunto"
tags:
  - inbox
updated: 2026-09-15
---
```

Escreva, adicione um wikilink para algo relacionado e siga. Avise o humano que ficou algo na Inbox.

### 5.7 Atualizar uma nota existente

- **Edite a nota, não crie uma versão paralela.** Nada de `Persona v2.md`.
- Atualize o campo `updated`.
- Se removeu uma afirmação porque ela estava errada, marque `[REVOGADO]` com o motivo em vez de deletar.
- Se a nota ficou grande demais para uma ideia só, quebre em notas menores e transforme a original em índice.

---

## 6. Referência rápida do frontmatter

Todo arquivo `.md` começa com bloco YAML na primeira linha. Sem isso, a nota some das Bases.

| Campo | Onde se aplica | Valores |
|---|---|---|
| `id` | todas | slug único, prefixado pelo tipo (`fb-`, `task-`, `perm-`, `proj-`, `lit-`, `note-`) |
| `type` | todas | `project`, `feedback`, `task`, `permanent`, `literature`, `area`, `resource`, `moc`, `note`, `template` |
| `title` | todas | título legível, com acento, entre aspas |
| `tags` | todas | lista YAML, uma por linha com `  - ` |
| `updated` | todas exceto feedback e task | `AAAA-MM-DD` |
| `project` | feedback, task, notas de projeto | wikilink entre aspas: `"[[Persona]]"` |
| `year` | projeto, feedback, task | número |
| `status` | projeto | `active`, `paused`, `completed`, `archived` |
| `status` | feedback | `"Pendente"`, `"Em Análise"`, `"Resolvido"` |
| `status` | task | `todo`, `doing`, `blocked`, `paused`, `done` |
| `deadline` | projeto, task | `AAAA-MM-DD` |
| `date` | feedback | `AAAA-MM-DD` — quando o feedback foi dado |
| `author`, `role` | feedback | quem deu e em que papel |
| `sentiment` | feedback | `"Bom"` ou `"Mal"`, só isso |
| `criterio` | feedback, task | 1 a 9, ou 0 |
| `prioridade`, `track` | task | ver receita 5.2 |
| `origem` | permanent | wikilink da nota que originou |

**Nomes de arquivo sem acento e sem caractere especial** — o título acentuado vai no campo `title`. Isso evita link quebrado entre Windows, celular e sincronização.

---

## 7. Mover e renomear arquivos

Wikilink do Obsidian resolve por **nome de arquivo**, não por caminho. Consequência prática:

- **Mover** uma nota de pasta, mantendo o nome, não quebra links.
- **Renomear** um arquivo quebra todos os links que apontam para ele.

Por isso, para renomear, use o Obsidian CLI, que atualiza as referências automaticamente:

```bash
obsidian rename file="Nome antigo" name="Nome novo"
obsidian move file="Nome da nota" to="50-Areas/Produto"
```

Requer Obsidian 1.12.7+ com a interface de linha de comando ativada em Configurações → Geral, e o app rodando.

**Se você não tem acesso ao CLI** — o que é o caso da maioria das IAs rodando fora da máquina do usuário — então:

1. Diga isso ao humano antes de mover ou renomear qualquer coisa. Não finja que usou.
2. Prefira **não renomear**. Mover é seguro; renomear não é.
3. Se renomear for inevitável, busque em todo o cofre pelo wikilink com o nome antigo e corrija cada ocorrência manualmente, no mesmo passo.

---

## 8. Checklist antes de salvar qualquer nota

- [ ] Tem frontmatter YAML na primeira linha
- [ ] `type` está preenchido com um valor da lista
- [ ] `title` está entre aspas e com acento correto
- [ ] Nome do arquivo está sem acento
- [ ] Tem pelo menos um wikilink `[[ ]]` no corpo
- [ ] Todo número tem fonte ao lado, ou está marcado como `[HIPÓTESE]`
- [ ] Nada foi inventado
- [ ] Nenhum emoji
- [ ] Se é feedback: `sentiment` é `"Bom"` ou `"Mal"`, e o corpo tem as três seções
- [ ] Se é tarefa: tem `deadline` e `## Definição de pronto`
- [ ] Se contradiz outra nota, a outra nota foi corrigida ou marcada `[REVOGADO]`

---

## 9. Anti-padrões — o que já deu errado antes

| Não faça | Por quê |
|---|---|
| Criar `Nota v2.md` ao lado de `Nota.md` | Duplicata vira duas verdades. Edite a original |
| Colar texto bruto sem reescrever | Colecionismo de dados. Sintetize com suas palavras |
| Juntar cinco pontos de feedback em uma nota | Impede filtrar por sentimento e critério. Um ponto, uma nota |
| Escrever "as pessoas têm dificuldade" | Vago. Diga quem, qual dificuldade e como você sabe |
| Registrar decisão sem data e sem motivo | Daqui a seis meses ninguém sabe por que aquilo foi decidido |
| Apagar informação que ficou errada | O erro é dado. Marque `[REVOGADO]` |
| Afirmar que algo foi validado sem evidência na base | Foi exatamente isso que custou a edição anterior |
| Usar número de projeção sem fonte | Um número sem lastro contamina a credibilidade de todos os outros |
| Deixar nota sem link | Ela desaparece na prática |
| Reutilizar um ID de decisão ou tarefa | Quebra a rastreabilidade histórica |

---

## 10. Antes de encerrar a sessão

Sempre que você fizer algo relevante nesta base, registre — senão a próxima IA refaz o trabalho.

1. **Resuma** em até 10 linhas: o que mudou, o que foi decidido, o que falhou.
2. **Grave** esse resumo no fim de `40-Projects/2026/Persona/Log de Sessoes.md`, no formato já usado lá (`### AAAA-MM-DD — ferramenta / pessoa`).
3. **Termine com o próximo passo concreto.** A próxima sessão começa lendo essa linha.

Se a sua ferramenta tiver comandos de persistência de memória (`/preserve`, `/compress`, `/resume` ou equivalentes), use. Se não tiver, faça manualmente — o que importa é o registro escrito, não o comando.

---

## 11. Quando parar e perguntar ao humano

Interrompa e pergunte antes de: alterar o conceito central do produto, mexer em prazo da competição, assumir custo ou compromisso com terceiro, escrever em nome da equipe algo que a equipe não fez, apagar conteúdo histórico, ou registrar como fato algo que você só deduziu.

Na dúvida entre perguntar e supor, pergunte. Esta base vale pela confiabilidade — uma suposição registrada como fato vale menos que um `[PENDENTE]` honesto.

---

## Relacionado

[[00 COMECE AQUI]] · [[Persona]] · [[Como usar este vault (IA)]] · [[Convencoes do Vault]]
