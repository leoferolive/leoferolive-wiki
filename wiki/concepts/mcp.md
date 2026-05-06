---
title: MCP (Model Context Protocol)
tags: [conceito, ai, mcp, agentic, em-producao]
last_updated: 2026-05-06
sources:
  - leoferolive.com.br/src/data/stack.ts
  - leoferolive.com.br/src/data/cases.ts
---

# MCP (Model Context Protocol)

## Resumo
Protocolo aberto para conectar LLMs a ferramentas e fontes de dados externas.
O Leonardo aplica MCP em **dois eixos** dentro da Wiley: como interface de
consumo da plataforma RAG (MCP server expondo busca em artigos) e como base
do **agentic workspace** que automatiza support duty E2E.

## Onde foi aplicado
- **[[entities/wiley]] — Agentic Workspace (adotado pelo time):**
  - **Solução:** workspace versionável com skills + AGENTS.md + MCPs (Jira,
    Kibana). Agente executa support duty E2E (issue → logs → fix → comentário
    no Jira).
  - **Impacto:** adotado pelo time, disseminado via [[entities/wiley]] /
    Conselho de IA Wiley Research BR.
- **[[entities/wiley]] — Plataforma RAG (MVP em produção):** MCP server
  expondo consultas em linguagem natural sobre 5+ fontes de artigos. Veja
  [[concepts/rag]].

## Cross-references
- [[skills/ai]]
- [[concepts/rag]]
- [[concepts/spring-ai]] — stack que hospeda os MCP servers.
