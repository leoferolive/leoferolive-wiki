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

## [2026-05-08] ingest | raw/interview-{capgemini-persist,ebix-2017,lumis,ebix-latam,city-connect}-*.md
Ingest de 5 entrevistas em voz cobrindo a carreira pré-Wiley (2014–2024).

Mudanças estruturais:
- **Split de `entities/ebix.md`** em duas entities (cada passagem tem
  história própria):
  - `entities/ebix-2017.md` (2017–2018, Pleno, célula de Salvados).
  - `entities/ebix-latam.md` (2019–2024, Sênior / referência técnica).
- Reescritas: `entities/persist.md`, `entities/lumis.md`,
  `entities/city-connect.md` com período preciso, projetos, decisões
  técnicas e achievements das fontes.
- Concepts criados:
  - `concepts/sinistro-re.md` — domínio Bradesco que atravessa
    Capgemini → Persist → Ebix (×2).
  - `concepts/oauth2.md` — impersonação (Lumis) + Client Credentials
    (BFF P8, Ebix LATAM).
- Cross-refs atualizadas em `concepts/microservices.md`,
  `skills/backend.md`, `skills/data.md` (de `entities/ebix` para
  `entities/ebix-latam`).
- `index.md`: ordem cronológica reversa nas entidades, summaries
  refeitos, novos concepts adicionados, `last_updated` atualizado.

Correção factual em relação às fontes em `raw/`:
- Os arquivos de entrevista mencionam **JBoss** como servidor de
  aplicação na Capgemini/Persist e Ebix 2017. Confirmado com Leonardo
  que **a conta Bradesco sempre rodou em WebSphere 8 / 8.5 / 9 e
  Tomcat 8 / 9** — JBoss nunca foi usado. Páginas de wiki refletem o
  stack correto. Os arquivos `raw/` devem ser corrigidos pelo Leonardo
  (regra: agente não modifica `raw/`).

Pendências:
- `pre-carreira` ainda não veio em `raw/`.
- Novo raw da Wiley em preparação — atualizar `entities/wiley.md`
  quando chegar.

## [2026-05-08] ingest | conversa-direta
Adicionada `wiki/about.md` com identidade do Leonardo:
- Nome completo: Leonardo Ferreira Oliveira.
- Data de nascimento: 29/11/1990 (35 anos em 2026-05-08).
Nova seção "Perfil" no `index.md` apontando para `about.md`.
