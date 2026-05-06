# leoferolive-wiki

LLM Wiki sobre a carreira do **Leonardo Fernandes Oliveira** — Senior Software Engineer
focado em engenharia AI-First. Esta wiki segue o padrão proposto por
[Andrej Karpathy](https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f):
um corpus em markdown sintetizado, cross-referenciado e mantido ao longo do tempo,
consumido em query-time por um backend (`chat-api`) que alimenta o chat de IA do
site `leoferolive.com.br`.

## Como navegar

- `wiki/index.md` — catálogo completo, organizado por categoria. Lido pelo backend
  para selecionar páginas relevantes a cada consulta.
- `wiki/log.md` — timeline append-only de ingestões, queries e lints.
- `wiki/entities/` — uma página por empresa/cliente.
- `wiki/projects/` — uma página por projeto pessoal.
- `wiki/concepts/` — conceitos técnicos centrais (Spring AI, Kafka, Kubernetes...).
- `wiki/skills/` — agrupamentos de skills (backend, ai, data, devops).
- `raw/` — fontes imutáveis (CV, transcripts, READMEs) usadas para ingest.

## Convenções

Veja [`AGENTS.md`](./AGENTS.md) para o schema completo (frontmatter, tags,
nomenclatura, workflows `ingest` / `query` / `lint`). Toda sessão de manutenção
desta wiki deve começar lendo o `AGENTS.md`.

## Idioma

O conteúdo primário é **português**. O backend traduz/responde no idioma da query.
