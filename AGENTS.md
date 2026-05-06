# AGENTS.md — schema da LLM Wiki

Este arquivo é o **contrato** que sessões de Claude Code (e quaisquer agentes
futuros) devem seguir ao manter esta wiki. Leia antes de tocar em qualquer
arquivo de `wiki/`.

Padrão inspirado em
[Andrej Karpathy — LLM Wiki](https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f).

## Princípios

1. **Síntese sobre acumulação.** A wiki não é dump de fontes; é conhecimento
   destilado, com cross-references entre páginas.
2. **Factual.** Nada que não esteja em `raw/` ou em fontes citadas explicitamente
   no frontmatter `sources`. Quando faltar dado, escreva "informação não
   disponível" — não invente.
3. **Append-only no log, atomizada nas páginas.** Toda mudança gera um entry em
   `wiki/log.md`. Páginas são reescritas inteiras quando atualizadas (não
   acumular changelogs dentro delas).
4. **PT primário.** Conteúdo em português; o backend traduz no idioma da query.
5. **Pequena por design.** Páginas <300 linhas. Se crescer, divida em sub-páginas.

## Estrutura de pastas

```
raw/                fontes imutáveis (CV.pdf, transcripts, READMEs, exports). Read-only.
wiki/
  index.md          catálogo. Lido pelo backend em query-time.
  log.md            timeline append-only.
  entities/         empresas/clientes (uma por arquivo).
  projects/         projetos pessoais.
  concepts/         conceitos técnicos centrais (Spring AI, Kafka, RAG...).
  skills/           agrupamentos de skills (mirror de stack.ts do site).
```

## Nomenclatura

- Arquivos: `kebab-case.md` (ex: `city-connect.md`, `spring-ai.md`).
- IDs nas páginas espelham o `id` da fonte quando existir
  (ex: `cityconnect` no `career.ts` → arquivo `city-connect.md`, com nota no
  frontmatter se houve normalização).
- Cross-references usam wiki-links estilo Obsidian: `[[entities/wiley]]` ou
  `[[wiley]]` quando não-ambíguo.

## Frontmatter (obrigatório em toda página)

```yaml
---
title: Wiley
tags: [empresa, atual, ai-first, sse, rag]
last_updated: 2026-05-06
sources:
  - leoferolive.com.br/src/data/career.ts
  - leoferolive.com.br/src/data/cases.ts
---
```

Campos:
- `title` — humano-legível, usado no `index.md`.
- `tags` — lowercase, kebab-case. Ajudam o retriever a fazer matching por
  keyword overlap. Mín. 3, máx. ~8.
- `last_updated` — `YYYY-MM-DD`. Atualizar a cada reescrita.
- `sources` — paths/URLs das fontes consultadas. Use paths relativos a
  `~/projetos/` quando for repo local; URLs completas quando externo.

## Estrutura de uma página

Todas as páginas seguem este esqueleto (omitir seções vazias):

```markdown
---
<frontmatter>
---

# {title}

## Resumo
1-3 frases. Lead com o "o quê" e o "porquê é relevante".

## Período / Detalhes
Datas, contexto, escopo. Para entities: período + cargo + escala.

## Tecnologias
Lista factual extraída das fontes.

## Achievements / Highlights
Bullets curtos. Citar números quando existirem.

## Cross-references
- [[entities/outra]] — relação em uma linha
- [[concepts/x]] — relação em uma linha
```

## Exemplo de entry no `index.md`

```markdown
## Entidades
- [Wiley](entities/wiley.md) — empresa atual; UAXD platform; AI-First leadership.
- [Ebix](entities/ebix.md) — Bradesco Seguros sinistros, 5 anos como Tech Lead.
```

Cada linha: `- [Title](path) — one-line summary`. Esse formato é parseado pelo
`retriever.py` do backend.

## Exemplo de entry no `log.md`

```markdown
## [2026-05-06] bootstrap | inicial
Bootstrap inicial via agente. Extraído de
leoferolive.com.br/src/data/{career,projects,stack,cases}.ts. Páginas
criadas: 17.

## [2026-05-12] ingest | raw/CV-2026.pdf
Adicionado CV PDF. Atualizado entities/wiley.md (datas), criado
concepts/uaxd.md.
```

Tipos de entry: `bootstrap`, `ingest`, `query` (validações manuais),
`lint` (auditoria), `refactor`.

## Workflows

### ingest
Disparado quando o Leonardo adiciona algo em `raw/` ou pede para incorporar
nova fonte.

1. Ler todo o source em `raw/`.
2. Listar takeaways e propor onde encaixar (entity nova? page existente?).
3. Discutir com o usuário antes de escrever.
4. Atualizar/criar páginas afetadas.
5. Atualizar `index.md` se houve nova página ou mudança de summary.
6. Append entry em `log.md` com tipo `ingest`.

### query
Validação manual da qualidade da wiki.

1. Usuário pergunta no terminal: "como a wiki responderia X?"
2. Agente lê `index.md`, escolhe top-N páginas, simula resposta usando só
   conteúdo da wiki.
3. Identifica gaps ("essa pergunta não está coberta") e sugere refinamentos.
4. Append entry em `log.md` com tipo `query` se algo mudou.

### lint
Auditoria periódica.

1. Procurar contradições entre páginas (ex: datas conflitantes).
2. Listar páginas órfãs (sem incoming links).
3. Listar tags raras (uso único) e propor consolidação.
4. Verificar que todo arquivo em `entities/`/`projects/`/`concepts/`/`skills/`
   está em `index.md`.
5. Verificar que `last_updated` ≤ data do `log.md` mais recente que mencione
   a página.
6. Append entry em `log.md` com tipo `lint`.

## Restrições para agentes

- **Não modifique** `raw/` (fontes imutáveis). Se precisar corrigir uma fonte,
  fale com o usuário.
- **Não invente** datas, números, nomes de pessoas, nomes de produtos.
- **Não duplique** conteúdo entre páginas; cross-reference em vez de copiar.
- **Não escreva** em primeira pessoa (a wiki fala sobre o Leonardo, não como ele).
- **Não use emojis** em conteúdo de página (só em `log.md` se útil para tipo
  de entry, mas evite).

## Checklist antes de commitar

- [ ] Todas as páginas novas/alteradas têm frontmatter completo.
- [ ] `last_updated` atualizado nas páginas tocadas.
- [ ] `index.md` reflete adições/remoções.
- [ ] `log.md` tem entry novo descrevendo a mudança.
- [ ] Cross-references não quebradas (nenhum `[[x]]` apontando para arquivo
      inexistente).
- [ ] Conteúdo é factual e cita `sources` no frontmatter.
