# log

Timeline append-only de operações na wiki. Tipos de entry: `bootstrap`,
`ingest`, `query`, `lint`, `refactor`. Convenção em `AGENTS.md`.

## [2026-05-06] bootstrap | inicial
Bootstrap inicial via agente. Extraído de
leoferolive.com.br/src/data/{career,projects,stack,cases}.ts. Páginas
criadas: 19 (5 entidades, 3 projetos, 7 conceitos, 4 skills).

Detalhes:
- Entities: wiley, ebix, city-connect, lumis, persist.
- Projects: nossalista, nossagrana, homelab. (OpenClaw foi tratado como
  ferramenta usada em `projects/homelab.md`, não como projeto próprio,
  porque não consta como entrada em `projects.ts`.)
- Concepts: spring-ai, rag, mcp, sse, microservices, kubernetes, kafka.
- Skills: ai, backend, data, devops (mirror exato de `stack.ts`).
- Index e este log criados.
- Pasta `raw/` criada com README explicando o uso (vazia de fontes ainda).
