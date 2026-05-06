# raw/

Fontes **imutáveis** consumidas pelo workflow `ingest` (ver `AGENTS.md`).
Agentes **não modificam** arquivos aqui — eles apenas leem e sintetizam em `wiki/`.

## O que vai aqui

- CVs em PDF (ex: `CV-2026.pdf`).
- Transcripts de palestras / entrevistas / podcasts.
- READMEs e snapshots de projetos pessoais (`openclaw-readme.md`,
  `nossalista-readme.md`).
- Exports estruturados do site
  (`career.json`, `projects.json`, `stack.json`, `cases.json` derivados de
  `leoferolive.com.br/src/data/*.ts`).
- Posts de blog, threads de Twitter, slides.
- Anotações longas que o Leonardo queira incorporar.

## O que NÃO vai aqui

- Conteúdo já sintetizado (vai em `wiki/`).
- Secrets, chaves de API, dados pessoais sensíveis.
- Binários muito grandes (>5MB) — preferir hospedagem externa e linkar.

## Convenção

Nome de arquivo descreve a fonte: `{tipo}-{slug}-{data}.{ext}`, por exemplo
`cv-leoferolive-2026-05.pdf` ou `talk-ai-first-wiley-2026-04.md`. Sem espaços,
sem caracteres especiais.

## Fluxo típico

1. Leonardo adiciona arquivo aqui.
2. Pede para Claude Code executar workflow `ingest`.
3. Claude lê, sintetiza em `wiki/`, atualiza `index.md` e `log.md`.
4. Commit no repo.

O bootstrap inicial (2026-05-06) extraiu conteúdo direto dos arquivos
`leoferolive.com.br/src/data/*.ts` sem depositar nada aqui ainda — os primeiros
arquivos `raw/` virão quando o Leonardo adicionar CV, transcripts ou READMEs
de projetos.
