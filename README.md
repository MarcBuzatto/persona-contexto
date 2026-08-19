# Persona Contexto

Cofre [Obsidian](https://obsidian.md) que guarda a memória de longo prazo dos projetos de empreendedorismo da nossa equipe no **Senac Lapa Tito** — curso Técnico em Inteligência Artificial Integrado ao Ensino Médio.

Ele existe por um motivo específico: em vez de recomeçar do zero a cada edição da competição, queremos que qualquer pessoa — ou qualquer IA que nos ajude — consiga entender em uma leitura o que já foi feito, o que deu errado, o que deu certo e o que ainda está aberto.

## Por onde começar

1. **[`00 COMECE AQUI.md`](./00%20COMECE%20AQUI.md)** — o índice do cofre e a ordem de leitura recomendada
2. **[`AGENTS.md`](./AGENTS.md)** — como usar e alimentar esta base, para qualquer IA
3. **[`CLAUDE.md`](./CLAUDE.md)** — governança específica do Claude Code

Abrindo pelo Obsidian, use `Abrir pasta como cofre` e aponte para a raiz deste repositório. Os arquivos `.base` só renderizam no Obsidian 1.9 ou superior.

## Arquitetura

O cofre combina dois métodos com propósitos diferentes. **PARA** organiza o que tem prazo e exige ação; **Zettelkasten** guarda o que continua verdadeiro depois que o projeto acaba.

```text
00-Inbox/        captura bruta, esvaziar sempre
10-Fleeting/     insights rápidos, processar toda semana
20-Literature/   resumos de fontes externas, com autor e origem
30-Permanent/    notas atômicas evergreen
40-Projects/     projetos por ano, cada um com Feedbacks/, Tarefas/ e Arquivos/
50-Areas/        responsabilidades contínuas: produto, competição, equipe
60-Resources/    referências, dados com fonte e as Bases
70-Archives/     histórico imutável
80-Templates/    modelos com frontmatter pronto
.claude/rules/   regras locais do agente
```

## Convenções

Toda nota começa com frontmatter YAML — é o que faz as Bases funcionarem e o que permite ler só as dez primeiras linhas de um arquivo durante uma busca, em vez do arquivo inteiro.

| Campo | Para que serve |
|---|---|
| `type` | `project`, `feedback`, `task`, `permanent`, `literature`, `area`, `resource`, `moc`, `note` |
| `sentiment` | só em feedbacks: `"Bom"` ou `"Mal"` |
| `status` | varia por tipo — ver `AGENTS.md` |
| `criterio` | qual dos 9 critérios do Empreenda a nota afeta |

Três regras que valem para todo mundo que escrever aqui:

- **Nada é inventado.** Falta informação, escreve `[PENDENTE]`.
- **Fato e hipótese são coisas diferentes** e ficam marcados como tal.
- **Nada é apagado.** O que perde validade vira `[REVOGADO]` com o motivo — o histórico de erro é metade do valor deste cofre.

## Bases

Consultas prontas, que leem o frontmatter das notas:

| Arquivo | Responde |
|---|---|
| `50-Areas/Feedbacks/Feedbacks-2026.base` | o que está indo bem e mal neste ano |
| `50-Areas/Feedbacks/Feedbacks-2025.base` | o mesmo para a edição anterior, para comparar |
| `60-Resources/Bases/Tarefas.base` | backlog por prioridade, track e prazo |
| `60-Resources/Bases/Notas.base` | panorama de tudo por tipo e data |

## Aviso

Repositório privado. Guarda estratégia de competição em andamento — feedback de avaliadores, pendências e projeções. Não tornar público antes do fim da edição, e não versionar aqui código de equipe, credencial ou qualquer segredo do portal.

---

Senac Lapa Tito · Técnico em Inteligência Artificial · Empreenda Senac 19ª edição
